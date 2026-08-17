# Reusable Prompt Library

My own prompts, refined over the course of the internship, kept here so I reuse and improve them instead of reinventing them each week. Each entry explains *why* the prompt is phrased the way it is — that reasoning is the actual skill being built, not the prompt text itself.

Format per entry: situation it's for → the prompt → why it's phrased this way → what to watch out for.

---

<!--
## Template entry (copy this for each new prompt)

**Use case:** [when I reach for this]

**Prompt:**
```
[the actual prompt text, with {placeholders} for the variable parts]
```

**Why this works:** [what specifically about the phrasing gets a better result than a naive version — e.g. asking for interview-style questions instead of a direct answer, constraining scope, asking it to flag assumptions, etc.]

**Watch out for:** [failure modes I've seen — e.g. it invents details, it over-engineers, it doesn't ask about mobile]
-->

---

## End-of-session summary (run in the track chat, right when wrapping up)

**Use case:** turning a finished task/assignment session into something I can paste into the documentation chat, so it produces the actual repo write-up without me reconstructing it from memory afterward.

**Prompt:**
```
This session is done. Generate a structured summary I'll paste into my
documentation chat to create the actual repo write-up. Format in Markdown:

1. Track + Week/Module (restate what we worked on)
2. Goal, in plain terms, in my own words — not copied from the brief
3. What was actually built/decided — the concrete artifact/decision
4. Every distinct prompt I used this session worth keeping, quoted exactly,
   each with a one-line note on why I phrased it that way
5. Specific moments I edited, rejected, or overrode your output — and why
   (be precise and honest here, don't soften or generalize)
6. QA/verification steps I actually performed
7. Anything I'm still unsure about or didn't finish
8. One honest reflection sentence — what surprised me or what I'd do differently
9. Flag anything from this session that's genuinely glossary-worthy (a new
   term I had to understand properly) or decision-worthy (a real fork in the
   road with options I weighed) — separate from the week write-up itself
```

**Why this works:** asks for structure, not narrative, so it maps directly onto `templates/week-template.md`. Item 5 explicitly demands honesty over smoothing, since summarizing AI tends to flatten "I overrode this" into vaguer, more flattering language. Item 9 exists because the week write-up and the docs/ files (glossary, decisions) serve different readers and easily get missed if nothing asks for them explicitly each time.

**Watch out for:** treat the output as a draft to verify, not a final answer to forward — re-read item 5 yourself before passing it along, since it's the section most likely to drift from what actually happened.

---

---

## Track chat kickoff (paste as the first message in any new track-specific chat)

**Use case:** starting a fresh AI Fluency or FE track chat so it's immediately oriented — right folder, right scope, right role — instead of re-explaining context from scratch or letting the chat guess what's needed.

**Prompt:**
```
Track: [AI Fluency / FE Track]
Week/Module: [number + title]
Assignment brief (from dashboard): [paste, even rough]

New folder or extending existing: [new / existing]
If existing, current README: [paste it]

What I need from you today: [brainstorm the approach / debug this specific
issue / review what I built / help me understand X before I start]

Remember: don't hand me a finished write-up — help me build and understand
the actual thing first. We'll produce the documentation together once the
real work is done, using the standard template.
```

**Why this works:** the assignment brief gets pasted, not summarized, since the dashboard's real scope (~2x the public assignment count) can't be guessed. Naming the exact goal for the session ("what I need from you today") prevents defaulting to guessing when the ask is ambiguous. The closing reminder exists because it's easy for a long session to drift into "I'll just write it for you" — restating it every time keeps the learning-first agreement active rather than relying on memory of a rule agreed to once, weeks ago.

**Watch out for:** don't skip the "what I need today" line even when it feels obvious — that's exactly the moment it's most likely to be assumed wrong.


**Use case:** pulling out prompts that are genuinely reusable across future tasks, not just useful once.

**Prompt:**
```
Looking back at this whole conversation, which prompts I used would genuinely
be worth reusing in future sessions — not just this one? For each: give the
prompt generalized with {placeholders} instead of my specific details, and
one line on why it's reusable beyond this exact task.
```

**Why this works:** most session prompts are one-off and task-specific; this asks for a second pass to isolate the few that generalize, keeping the library from filling up with near-duplicates.

**Watch out for:** run this only when something genuinely felt reusable — running it every session produces noise, not a curated library.


**Use case:** turning a vague idea ("I want a site that shows I'm good at X") into a specific, defensible claim.

**Prompt:**
```
I am switching into {field} and building a portfolio whose only job is to prove
I can do one thing well, so someone will hire or work with me. Interview me to
find three things: the ONE claim I am proving, the ONE specific person I am
proving it to, and the ONE action I want them to take. Ask one sharp question
at a time, push back when I am vague or trying to prove more than one thing,
and after about eight questions propose a one-paragraph proof statement.
```

**Why this works:** it asks AI to *interview*, not *author* — the useful output is my own answers being pulled out of me, not AI's generic guess at what I should claim. The "push back when vague" instruction is what prevents a smooth, forgettable, generic result.

**Watch out for:** if I answer vaguely myself, it can still land on something generic — the prompt only works if I actually engage with the questions honestly.

---

## Guided build walkthrough, from locked content to finished build (from AI Fluency FL-05)

**Use case:** turning already-finalized content (proof statement, sitemap, case studies) into an actual step-by-step build guide, without AI re-litigating content that's already decided or assuming skills I don't have.

**Prompt:**
```
Help me build a portfolio that proves I have strong {your specific skill
claim — e.g. "front-end engineering skills," "UX research skills"}. The
audience is {describe the one specific person you're trying to convince —
e.g. "a hiring manager deciding whether to trust me with real front-end
work"}.

Here's what I've already built: my proof statement is "{paste your proof
statement}." My sitemap is {list your locked pages in order}. My case study
so far: {2-3 sentences summarizing the problem, what you did/decided, and
the result — your honest version, not a polished pitch}.

Assume everything I've described above is already finalized — don't ask me
to write or revise it unless I specifically say otherwise. {Optional: If
you want it to flag concerns as it goes, add: "You can point out issues
with what I've already built if you see them, but don't stop the build
process to do it."}

Here's my actual skill level, including what I'm shaky on, so you don't
assume more than I have: {e.g. "confident in React, haven't used Vite
before" or "solid with HTML/CSS, still new to JavaScript"}.

Walk me through this as a step-by-step build guide from where I am now to a
finished site, with real code/commands at each step I'm unfamiliar with —
not just described steps. Don't critique what I've already built; guide me
forward.
```

**Why this works:** built through a six-run prompt ladder that isolated exactly one failure mode per version — a vague baseline produces generic all-rounder advice; adding a goal narrows it but drops other ground; adding audience shifts the substance of the advice; adding real context makes it specific but can tip into unwanted critique instead of guidance (a real regression worth knowing about); stating output format fixes that; and stating actual skill level (including gaps, not just strengths) stops it from silently assuming fluency I don't have. Every clause in the final prompt exists because an earlier version without it produced a specific, observed failure.

**Watch out for:** dropping the "here's my actual skill level, including gaps" clause to make the prompt look cleaner — that's the exact mistake this ladder caught (Version 5 assumed Vite fluency that wasn't stated). Stating what you're *not* confident in is doing real work, not padding.

---

## Coding task with visible reasoning: role + context + examples + plan-first + structured output (from AI Fluency FL-06)

**Use case:** any real coding task where a vague ask would produce plausible-looking but subtly wrong code — validation logic, edge-case handling, anything where "looks right" and "is right" can diverge. Built by stacking five techniques, each added only after the previous ones failed to fix a real bug.

**Prompt:**
```
You are a senior front-end engineer who specializes in {relevant specialty
— e.g. "form validation," "state management," "accessibility"} and writes
production-quality {language/framework} code.

This is real code from {brief description of the actual project and its
stakes — e.g. "a live settings form users will save real data through"}.
Right now {describe the current gap or weak point}, and I'm planning to
fix it using {your intended tool/approach, if you have one} because {why
— what property you actually need: maintainability, consistency, etc.}.

{Describe the specific task.} Here are concrete examples of what should
pass and fail, to guide the logic precisely rather than relying on a
generic check:

<examples>
<example>{input} → {valid/invalid, with a one-line reason}</example>
{add 3-5 examples covering your real edge cases}
</examples>

Before writing any code, walk through your plan: list each rule you
intend to implement, and for each one, explain what it catches and why,
based on the examples above. Present this as a numbered list. Only after
the plan is complete, write the implementation — and make sure the code
matches the plan exactly.

Every part of your response — plan, code, and test cases — should make
the reasoning visible, not just the result. Don't just tell me what the
solution is; make sure I understand why it exists in that form, so I
could explain it to someone else myself.

Structure your response into exactly three labeled sections: **Plan**,
**Code**, and **Test Cases** (a short table of example inputs and whether
each should pass or fail).

Here's the current code:
{paste only the relevant file/function/component — not the whole project}
```

**Why this works:** each clause exists because a real bug survived without it. Role alone changed tone, not logic. Adding context/motivation got the right tool (Zod) but the same bug survived — proving the issue was never the technique, it was that "valid email" had never been precisely defined. Few-shot examples with the exact failing cases finally fixed it, since some rules ("realistic domain shape") are nearly impossible to state abstractly but trivial to demonstrate. Step decomposition surfaces a wrong plan before code gets written instead of after. Output structure makes the result fast to scan and verify, not just correct.

**Watch out for:** skipping straight to few-shot examples without first trying role/context — the point isn't that examples are always the answer, it's diagnosing *why* a technique failed before reaching for a bigger one. Also: manually test the actual edge cases in a running app, don't just trust that code "looks" correct from reading it.
