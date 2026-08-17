# FL-04 — Frame It as Cases

- **Assignment:** FL-04 — Frame Your Work as Case Studies
- **Status:** ✅ Complete

## Goal

Write a voice card, interview one real piece of work into a three-beat case study, draft bio + CTA copy, and produce a before/after showing edited vs. generic AI output.

## What I built

Full deliverable: [`fl-04-frame-cases.md`](./fl-04-frame-cases.md)

- Voice card (7 words, deliberately ordered: confidence/thoughtfulness as prerequisites, then delivery style) — now a standing instruction in the Portfolio Build Project
- One case study (Tuber, the YouTube-replica video app), interviewed one question at a time until the problem, decisions, and result were concrete
- Bio and CTA copy, corrected once for wrong tonal register
- A before/after comparison built from a real rejection in this session, not manufactured after the fact
- Updated [`fl-02-portfolio-project-instructions.md`](../week-01-proof-statement/fl-02-portfolio-project-instructions.md) (lives in the Week 1 folder, since it's the same evolving artifact created there — not duplicated here) with the voice card and refined sitemap section labels (Landing/Believing/Trusting/Action)

## Prompts used, and why

- Interview-style, one question at a time, pushing back when answers stayed at the "assignment description" level instead of reaching an actual problem — matches the brief's explicit warning against letting AI write from a vague prompt.
- Verified the technical story against the actual repo code (`project.js`) rather than taking the bug description at face value — confirmed the tooltip/sort-order split was real, not misremembered.

## What I changed or rejected from AI's output

- Rejected the first case-study draft outright — accurate facts, but sounded rushed and generic; slower rewrite preserved the same content but let the reasoning actually show.
- Rejected three bio drafts for reading as backend/data-engineer tone rather than front-end — caught "messy data" framing overshadowing "interface," rewrote around what's actually built, not just what's processed.
- Kept my own bio phrasing ("the decisions behind the interface") over AI-drafted alternatives once it was clearly stronger and more consistent with the case study's actual point.
- Declined adding an explicit "I'm looking for a front-end role" line to the bio — redundant against the CTA's implicit context.
- Locked CTA Option 2 over Option 1 specifically because it echoes the Week 1 CTA reasoning (communicates better talking than writing) — see [ADR-0002](../../docs/decisions/0002-book-a-call-cta.md), this reaffirms it rather than reopening it.

## QA / verification notes

- Case study checked against the assignment's own pass/revise bar: three beats present, could only describe this specific project, sounds like a specific person, before/after shows real contrast, points at the one action.
- Technical claims cross-checked against the actual public repo rather than trusted from memory alone.
- **Open item, deliberately surfaced rather than smoothed over:** the project is three years old. Chose not to treat this as a liability — reasoning that no one questions a project's age until they try to use it regularly and it fails them.

## Reflection

The bio tone-check was the sharpest catch this session — "messy data" and "pile of data" sound like backend framing even when describing the same underlying work. Worth watching going forward: word choice can accidentally shift what role a reader assumes you're pitching for, independent of whether the sentence is technically true.

## Glossary flags (added to `docs/glossary.md`)

- **Voice Card** — five to seven words for how writing should sound, given to AI as a standing instruction. Adjectives about the prose, not the person.
- **The Three Beats** — the fixed shape every case study takes: the problem, what I did and decided, what came of it.

## Decisions made this session

- Voice card ordering, and proceeding with the 3-year-old Tuber project as evidence — scoped content judgment calls, not repo/site architecture, so kept here rather than as separate ADRs (same bar set in FL-01/FL-03).
- CTA Option 2 — reaffirms [ADR-0002](../../docs/decisions/0002-book-a-call-cta.md), doesn't warrant a new one.

## Links

- Deliverable: [`fl-04-frame-cases.md`](./fl-04-frame-cases.md)
- Updated Portfolio Project instructions: [`../week-01-proof-statement/fl-02-portfolio-project-instructions.md`](../week-01-proof-statement/fl-02-portfolio-project-instructions.md)
