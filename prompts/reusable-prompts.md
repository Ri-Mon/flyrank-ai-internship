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
