# FL-05 — The Prompt Ladder

- **Assignment:** FL-05 — The Prompt Ladder
- **Status:** ✅ Complete

## Goal

Build a six-run prompt ladder (baseline + 5 versions) around a real, reusable task — building the portfolio — isolating exactly one layer per version, comparing real outputs side by side, and producing a final prompt usable by a stranger on the track.

## What I built

Full deliverable: [`fl-05-prompt-ladder.md`](./fl-05-prompt-ladder.md)

- Baseline prompt ("Help me build a portfolio") run cold, producing genuinely generic, all-rounder advice
- Five versions, each adding exactly one layer in the order the actual weaknesses demanded: goal → audience → real context → output format → stated assumptions
- Notes per version, written in first person, revised to strip generic/report-style phrasing
- One explicitly identified "helped but also broke something" moment (Version 3)
- A final, cleaned-up, placeholder-based reusable prompt, stress-tested against the "works for a stranger" bar — now also added to [`prompts/reusable-prompts.md`](../../prompts/reusable-prompts.md), since that's exactly what it's for

## Prompts used, and why

- Refused to pre-script all six versions in advance, even though it would've been faster — the brief's design specifically requires each layer to be chosen reactively, based on the previous version's actual output, or the "diagnosis" isn't real.
- Wrote my own diagnosis before accepting AI's, at every version — that's the actual skill FL-05 grades, not the final prompt itself.

## What I changed or rejected from AI's output

- Rejected doing this exercise on both a portfolio prompt and a CV prompt simultaneously — same "narrow beats broad" principle as Week 1, chose portfolio only since it compounds into real future work.
- Corrected an early self-diagnosis ("was my prompt too good to be vague?") — reframed: the all-rounder, generic-feeling output was itself the signature of vagueness, not evidence the baseline was well-written.
- Caught and named a real regression in Version 3 (context added specificity but shifted the response into unwanted critique) rather than smoothing it into a pure "improvement" — this became the required honest "didn't fully help" moment.
- Rejected removing skill *gaps* from the final reusable prompt, keeping only comfort areas — this would have silently recreated the exact Vite-blind-spot bug the ladder just spent a full version diagnosing.
- Multiple tone passes on Version 5's notes to strip generic-sounding phrasing until it matched my actual voice, written directly by me in the final pass.

## QA / verification notes

- Verified count: baseline + 5 versions = 6 runs total, matching the assignment's explicit requirement.
- Confirmed each version is tied to exactly one named layer, with no bundling.
- Confirmed the honest failure moment is real, not manufactured — Version 3 genuinely did what was diagnosed.
- Final prompt checked against "usable by a stranger" — no placeholder secretly assumes shared context from this conversation (e.g., "your one person from Week 1" was caught and replaced with a self-contained instruction).

## Reflection

The sharpest moment wasn't a prompting technique — it was catching, twice, that fixing one wrong assumption (case study/About being unfinished) can silently leave a second, different wrong assumption standing (Vite fluency). That's a transferable lesson beyond this one ladder: solving a visible problem doesn't guarantee nearby invisible ones are also solved.

## Glossary flags (added to `docs/glossary.md`)

- **Prompt Layer** — one isolated addition to a prompt (goal, audience, context, format, constraints, examples, quality criteria, review instructions, stated assumptions, or verification requirements) — never bundled with another layer in the same version.
- **Isolation Discipline** — the practice of changing exactly one variable at a time so a specific output change can be attributed to a specific prompt change, rather than guessed at.

## Decisions made this session

- Portfolio-only scope (not portfolio + CV), refusing to pre-plan the ladder's layers in advance, and keeping skill gaps in the final prompt — all scoped methodology/content calls, not repo or site architecture, so kept here rather than as ADRs (same bar as FL-01/FL-03/FL-04).

## Links

- Deliverable: [`fl-05-prompt-ladder.md`](./fl-05-prompt-ladder.md)
- Final reusable prompt also lives in: [`prompts/reusable-prompts.md`](../../prompts/reusable-prompts.md)
