# FL-05 — The Prompt Ladder

- **Name:** Md. Mahmudul Hasan Rimon
- **Date:** August 12, 2026
- **Topic:** Building my AI Fluency portfolio site

---

## Version 0 — Baseline (weak, no layers)

**Prompt:**
> "Help me build a portfolio."

**Output (excerpt):**
> I'd be happy to help you build a portfolio! Here are some things to consider:
> 1. Define your goals — what's the purpose of your portfolio?
> 2. Choose a platform — Squarespace, Wix, WordPress, or custom-coded
> 3. Curate your best work — 5-10 pieces
> 4. Structure your content — homepage, projects, about, contact
> 5. Write compelling descriptions
> 6. Make it visually appealing
> 7. Optimize for mobile
> 8. Include a clear call-to-action
>
> Would you like help with any specific part of this process?

**Notes:**
- What changed: nothing yet — this is the starting point
- What actually happened in the output: generic, all-rounder checklist that would apply equally to anyone building any kind of portfolio — no assumption about who I am or what I'm proving
- What still failed: no goal, no audience, no context about work already done, suggested website builders that don't fit a hand-coded React site
- What I'd try next: add a clear goal, since nothing else can be calibrated without it

---

## Version 1 — Added layer: clear goal

**Prompt:**
> "Help me build a portfolio that proves I have strong front-end engineering skills."

**Output (excerpt):**
> Great, a skills-focused portfolio! Here's how to approach it:
> 1. Lead with projects, not a resume-style list
> 2. Show your process, not just the result
> 3. Pick 2-4 strong projects over many weak ones
> 4. Include a tech stack breakdown
> 5. Make sure the code itself is clean
> 6. Consider a small technical flourish on the site itself

**Notes:**
- What changed: added a clear goal — proving front-end engineering skill
- What actually improved: the output stopped being an all-rounder checklist and narrowed sharply onto project selection and code quality
- What still failed: lost real ground — dropped site structure, platform/build approach, and any process guidance entirely. Also assumed the audience was "recruiters and engineers," which isn't who I actually defined
- What I'd try next: add the actual audience, since the output guessed one wrong

---

## Version 2 — Added layer: defined audience

**Prompt:**
> "Help me build a portfolio that proves I have strong front-end engineering skills. The audience is a hiring manager deciding whether to trust me with real front-end work."

**Output (excerpt):**
> A hiring manager cares less about exhaustive technical depth and more about judgment and trust signals:
> 1. Lead with decisions, not just deliverables
> 2. Keep technical depth accessible
> 3. Address trust directly — include a "what I'd do differently" note
> 4. Make the next step obvious
> 5. Keep it fast to evaluate

**Notes:**
- What changed: added the specific audience — a hiring manager, not recruiters/engineers in general
- What actually improved: the output shifted from "prove skill via code quality" to "prove judgment and trustworthiness via decisions" — a real substance change, not just tone. It now covers the CTA portion, which it hadn't before
- What still failed: still fully generic hiring-manager-portfolio advice — nothing reflects that I already have a locked proof statement, sitemap, and real case study
- What I'd try next: add real context about the work already done

---

## Version 3 — Added layer: real context

**Prompt:**
> "Help me build a portfolio that proves I have strong front-end engineering skills. The audience is a hiring manager deciding whether to trust me with real front-end work. Here's what I've already built: my proof statement is 'I build frontends that turn a wall of options into something easier to explore.' My sitemap is Home/Hero → Work → About → Contact. I have one case study so far — a video app where I built category filtering and view-based sorting from an API, including a bug where my tooltip and sort logic were on separate state variables that I fixed by rewriting the logic myself instead of using an overly complex AI-generated fix."

**Output (excerpt):**
> This is much more concrete. A few observations specific to what you've shared:
> 1. Your case study's strongest moment is buried — the tooltip/sort-state bug should be the centerpiece, not a throwaway line
> 2. Your sitemap is thin on evidence density — one case study carries the whole site
> 3. Check whether About is pulling its weight yet
> 4. Your proof statement and case study should echo each other explicitly

**Notes:**
- What changed: added real context — proof statement, sitemap, and case study summary
- What actually improved: the response became specific to my actual situation instead of generic advice
- What still failed: helpful, but incomplete — it defaulted to auditing/critiquing what I'd already built instead of guiding me forward, which isn't what I asked for
- What I'd try next: specify the output format/shape I actually want — a guided build process, not a critique

---

## Version 4 — Added layer: output format

**Prompt:**
> [Version 3 prompt] + "Walk me through this as a step-by-step build guide, covering the whole process from where I am now to a finished site — not a critique of what I've already done."

**Output (excerpt):**
> Step 1 — Lock your content before touching code.
> Step 2 — Choose your stack (Vite + React, no need for Next.js).
> Step 3 — Build Home/Hero first.
> Step 4 — Build Work using your case-study structure.
> Step 5 — Build About and Contact.
> Step 6 — Cross-check every page against your proof statement.
> Step 7 — Deploy and test on mobile.

**Notes:**
- What changed: added an explicit output-format instruction — step-by-step build guide, not critique
- What actually improved: it started guiding through the whole process instead of just breaking down context — driving deeper, covering stack choice through deployment
- What still failed: Step 1 told me to finalize my case study and About section, which are already done — it wrongly assumed unfinished work
- What I'd try next: state explicitly that the case study and About section are already finalized

---

## Version 5 — Added layer: stated assumptions

**Prompt:**
> [Version 4 prompt] + "Assume my case study copy and About page copy are already written and finalized — don't ask me to write or revise them, start from the build itself."

**Output (excerpt):**
> Got it — content's locked, so here's the build guide starting from implementation:
> Step 1 — Set up the project (Vite + React).
> Step 2 — Build Home/Hero.
> Step 3 — Build Work.
> Step 4 — Build About.
> Step 5 — Build Contact.
> Step 6 — Cross-check against your proof statement.
> Step 7 — Deploy and test on mobile.

**Notes:**
- What changed: I told it my case study and About section are already done — stop treating them like they still need writing.
- What actually improved: It actually stopped — it moved past asking me to finish the case study and About statement and got into the real build steps.
- What still failed: It assumed I already know Vite well enough to just "set up the project" — I don't, I've never touched it. I'm comfortable with React, but the steps treat both as equally familiar to me when they're not.
- What I'd try next: Tell it exactly where I stand — comfortable with React, zero experience with Vite — and ask it to actually walk me through Vite setup with real commands and code, not assume I already know the tooling.

**Honest "didn't fully help" moment:** Version 3 (adding real context) is the clearest case of this — it was helpful in making the response specific to me, but it made the response worse in a different way by turning into a critique of my existing work instead of the guidance I actually wanted. Fixing one problem (genericness) surfaced a new one (wrong response shape) that had to be fixed separately in Version 4.

---

## Final Reusable Prompt

> Help me build a portfolio that proves I have strong {your specific skill claim — e.g. "front-end engineering skills," "UX research skills"}. The audience is {describe the one specific person you're trying to convince — e.g. "a hiring manager deciding whether to trust me with real front-end work"}.
>
> Here's what I've already built: my proof statement is "{paste your proof statement}." My sitemap is {list your locked pages in order}. My case study so far: {2-3 sentences summarizing the problem, what you did/decided, and the result — your honest version, not a polished pitch}.
>
> Assume everything I've described above is already finalized — don't ask me to write or revise it unless I specifically say otherwise. {Optional: If you want it to flag concerns as it goes, add: "You can point out issues with what I've already built if you see them, but don't stop the build process to do it."}
>
> Here's my actual skill level, including what I'm shaky on, so you don't assume more than I have: {e.g. "confident in React, haven't used Vite before" or "solid with HTML/CSS, still new to JavaScript"}.
>
> Walk me through this as a step-by-step build guide from where I am now to a finished site, with real code/commands at each step I'm unfamiliar with — not just described steps. Don't critique what I've already built; guide me forward.
