# FL-06 — Prompting Fundamentals on Real Tasks v2

**Name:** Md. Mahmudul Hasan Rimon
**Date:** August 16, 2026
**FL-01 target task used:** Target C — Reviewing my own code for bugs
**Real task:** Adding email validation to the settings form's email field (`App.jsx`, FE-02), which currently has no real validation beyond HTML5's loose `type="email"`.

Anthropic Prompt Engineering Interactive Tutorial (basics chapters) — completed separately as required by the brief.

---

## Version 0 — Baseline (naive prompt)

**Prompt:**
> "Add email validation to this form. [pasted `App.jsx`]"

**Output (excerpt):** A hand-rolled regex (`/^[^\s@]+@[^\s@]+\.[^\s@]+$/`) added inline in `handleSubmit`.

**Notes:**
- What changed: nothing — naive baseline
- What actually happened in the output: got a working regex instead of the Zod-based validation I specifically planned to use
- What still failed: the regex passes implausible addresses like `a.a@a`, and treats `A@A.A` as valid with no case handling
- What I'd try next: the model never knew I specifically wanted Zod — that's a missing constraint, not yet a named technique

---

## Version 1 — Added technique: role assignment

**Prompt:**
> "You are a senior front-end engineer who specializes in form validation and writes production-quality React code. Add email validation to this form. [same code]"

**Output (excerpt):** Improved regex with normalization, plus the model mentioning Zod/Yup as the "real" production approach and offering to show that version — but still regex-based.

**Notes:**
1. What changed: added a role — "senior front-end engineer who specializes in form validation"
2. What actually improved: the model named Zod unprompted and offered to show that version — talked like an expert, flagging real limitations of its own regex
3. What still failed: same core issue as baseline — `a.a@a`, `A@A.A`, `A@A.a` all still pass; role changed the tone, not the actual validation logic
4. What I'd try next: give the model real project context so it builds toward what I actually need instead of just describing what it would do

---

## Version 2 — Added technique: context and motivation

**Prompt:**
> [Role from V1] + "This is a real settings form from an internship capstone project — a live account settings page users will actually save data through. Right now email validation is essentially non-existent, and I'm planning to fix it using Zod, since I want consistent, schema-based validation I can maintain and extend to other fields later, not a one-off regex. Add proper email validation to this form. [same code]"

**Output (excerpt):** Full Zod schema implementation using `.email()` with `.trim().toLowerCase()` normalization.

**Notes:**
1. What changed: included real context for the project and how I wanted to resolve the issue, explicitly naming the tool
2. What actually improved: got the real Zod implementation I originally planned, with normalization (trim/lowercase) built in
3. What still failed: same issue as before — `a.a@a`, `A@A.A`, `A@A.a`, `a@a.a` all still passed as valid
4. What I'd try next: specify the actual boundary — the model has no way to know these should fail unless shown explicitly

**Honest "didn't help" moment:** the same core failure survived two separate named techniques (role, then context/motivation) across two different implementations (regex, then Zod's built-in validator). This wasn't a prompting failure — it revealed that "valid email" was never precisely specified, so no technique short of explicit examples could fix a target that was never defined.

---

## Version 3 — Added technique: few-shot examples

**Prompt:**
> [Role + context from V2] + explicit `<examples>` block with 6 labeled valid/invalid email pairs, including the exact failing cases (`a.a@a`, `A@A.A`, `A@A.a`, `a@a.a`) with one-line reasons for each.

**Output (excerpt):** Added a `.refine()` step checking TLD length ≥ 2 and requiring all domain labels to be longer than 1 character.

**Notes:**
1. What changed: added few-shot examples — explicit valid/invalid email pairs, including the exact failing cases from Version 2
2. What actually improved: all four originally-failing cases (`a.a@a`, `A@A.A`, `A@A.a`, `a@a.a`) now get correctly rejected in the running app — confirmed by manually testing each in the live form
3. What still failed: nothing from my original test batch — this version passed clean. (Later tested `0@gmail.com` and confirmed it correctly passes, since a single-character local part is a legitimately valid email — not a gap, just a boundary I hadn't tested yet.)
4. What I'd try next: move to step decomposition — have the model reason through the plan before writing code

---

## Version 4 — Added technique: step decomposition

**Prompt:**
> [Role + context + examples from V3] + "Before writing any code, first walk through your plan: list each validation rule you intend to implement, and for each one, explain what it catches and why it's needed based on the examples I gave you. Present this plan as a numbered list. Only after the plan is complete, write the implementation — and make sure the code matches the plan exactly, rule for rule."

**Output (excerpt):** A four-point numbered plan (format check, normalization, TLD length, domain label length) followed by code that matched the plan point for point.

**Notes:**
1. What changed: added step decomposition — required the model to plan and justify each validation rule against my examples before writing any code
2. What actually improved: now it explains what it's doing and why before showing code, not just after — makes the reasoning visible instead of buried in a paragraph
3. What still failed: clean — same working result as Version 3, just with visible reasoning now
4. What I'd try next: output structure — separate the response into clearly labeled Plan, Code, and Test Cases sections

---

## Version 5 — Added technique: output structure

**Prompt:**
> [Role + context + examples + step decomposition from V4] + "Structure your response into exactly three labeled sections: **Plan** (numbered list, as before), **Code** (the implementation, matching the plan exactly), and **Test Cases** (a short table or list of example inputs and whether each should pass or fail, based on the validation rules in your plan)."

**Output (excerpt):** Clean three-section response — numbered plan, code block, and a markdown test-case table with 6 rows.

**Notes:**
1. What changed: added output structure — required three labeled sections (Plan, Code, Test Cases) instead of mixed prose and code
2. What actually improved: far easier to scan and reuse — the test-case table let me spot and resolve a question about `Name@gmail.com` (uppercase) in seconds, without re-reading paragraphs of explanation
3. What still failed: nothing — confirmed the uppercase-acceptance behavior was correct (case normalization via `.toLowerCase()`, not rejection), not an actual bug. Real-world email providers treat case-insensitively, so this matched what I actually needed once I checked my own assumption
4. What I'd try next: this closes the ladder for Claude — final step was running the same fully-stacked prompt on ChatGPT for comparison

---

## Cross-Model Comparison (Claude vs. ChatGPT)

Same final stacked prompt (role + context + examples + step decomposition + output structure) run on both, against the same `App.jsx` code.

**Tone:** Claude's plan reads conversationally, closer to a colleague reasoning out loud. ChatGPT's plan reads more like formal spec documentation — short, declarative statements. Neither is wrong, but Claude's register is closer to my own voice card (plain-spoken, conversational).

**Structure compliance:** Both followed the exact three-section format (Plan/Code/Test Cases) without deviation — the output-structure technique transferred cleanly across models.

**Accuracy on my defined test cases:** Functionally equivalent — both correctly rejected all four target failing cases and accepted the valid examples. No difference in outcome on the cases I specified.

**Real differences:**
1. **Normalization:** Claude's schema chains `.trim().toLowerCase()` before validating. ChatGPT's validates the raw string as typed, with no normalization step — a real, structural difference in production-readiness that neither of us explicitly tested against a whitespace/case edge case, but is visible directly in the code.
2. **Accessibility:** ChatGPT's version unprompted added `aria-invalid`, `aria-describedby`, `role="alert"` on the error message, and `noValidate` on the form to prevent the browser's native validation from conflicting with the custom Zod error. Claude's version added none of this. This is a genuine, real quality difference in ChatGPT's favor — more aligned with the "production-quality" role both models were assigned.
3. **Schema scope:** Claude wrapped the email rule in `z.object({ email: ... })`, anticipating future field validation. ChatGPT validated the email string directly — tighter, more scoped to exactly what was asked, no anticipatory design.
4. **Error granularity:** ChatGPT split the domain-shape check into three separate `.refine()` calls with three distinct error messages. Claude used one combined check with one generic message — ChatGPT's version gives the user a more specific reason when validation fails.

**Overall:** Both models responded well to the same stacked prompt and produced functionally correct, structurally compliant output. The differences that emerged weren't about whether the techniques worked, but about each model's own defaults — ChatGPT leaned more toward defensive/accessible production code without being asked, Claude leaned toward conversational reasoning and forward-looking schema design.

---

## Final Reusable Prompt Template

> You are a senior front-end engineer who specializes in {relevant specialty — e.g. "form validation," "state management," "accessibility"} and writes production-quality {language/framework} code.
>
> This is real code from {brief description of the actual project and its stakes — e.g. "a live settings form users will save real data through"}. Right now {describe the current gap or weak point}, and I'm planning to fix it using {your intended tool/approach, if you have one} because {why — what property you actually need: maintainability, consistency, etc.}.
>
> {Describe the specific task.} Here are concrete examples of what should pass and fail, to guide the logic precisely rather than relying on a generic check:
>
> <examples>
> <example>{input} → {valid/invalid, with a one-line reason}</example>
> {add 3-5 examples covering your real edge cases}
> </examples>
>
> Before writing any code, walk through your plan: list each rule you intend to implement, and for each one, explain what it catches and why, based on the examples above. Present this as a numbered list. Only after the plan is complete, write the implementation — and make sure the code matches the plan exactly.
>
> Every part of your response — plan, code, and test cases — should make the reasoning visible, not just the result. Don't just tell me what the solution is; make sure I understand why it exists in that form, so I could explain it to someone else myself.
>
> Structure your response into exactly three labeled sections: **Plan**, **Code**, and **Test Cases** (a short table of example inputs and whether each should pass or fail).
>
> Here's the current code:
> {paste only the relevant file/function/component — not the whole project}
