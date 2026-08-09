# FL-02 — Draw the Path

- **Assignment:** FL-02 — Sitemap + Portfolio Claude Project + Pressure Test
- **Status:** ✅ Complete

## Goal

Draw a minimal portfolio sitemap, configure a dedicated "Portfolio Build" Claude Project, and pressure-test the sitemap against the proof statement's actual claim.

## What I built

Full deliverable: [`fl-02-sitemap-pressure-test.md`](./fl-02-sitemap-pressure-test.md)

- Locked 4-page sitemap: Home/Hero → Work → About → Contact, with tech-stack badges merged into Work instead of a standalone page
- Dedicated "Portfolio Build" Claude Project instructions ([`fl-02-portfolio-project-instructions.md`](./fl-02-portfolio-project-instructions.md)) — proof statement, reasoning trail, locked sitemap, working preferences, scoped resource links
- Ran the required pressure-test prompt inside that Project; captured prompt + output + resulting change note in one file

## Prompts used, and why

- Pressure-test prompt explicitly requested "be specific, not encouraging" — a deliberate choice to prevent the exact failure mode of an agreeable pressure test that confirms nothing instead of actually stress-testing the sitemap.

## What I changed or rejected from AI's output

- Rejected a standalone Tech Stack page — merged into Work as badges instead, since a checklist page doesn't move a visitor toward believing or acting.
- Rejected treating the Work page as a screenshot "walkthrough" after the pressure test surfaced the distinction — restructured as a case study (problem → reasoning → rejected alternatives → result), since a walkthrough only proves output, not the thinking the proof statement actually claims.
- Rejected including backend/Django background in the Portfolio Project's instructions — no solid artifact currently backs that claim in this specific build's context.
- Trimmed the Portfolio Project's resource links to only AI Fluency + portfolio-relevant material, cutting Mollick, the Academy course, the Claude Projects doc, and the FE track as out of scope for this specific Project.

## QA / verification notes

- Sitemap checked against the brief's "every page earns its place" bar via the pressure test itself.
- **Filename convention note:** an earlier draft of this session's handoff suggested folder/file names that didn't match this repo's actual convention (including an incorrectly-numbered `fl-01-` prefix for what is really FL-02/FL-03 work). Ignored that suggestion entirely — filed here as `fl-02-*`, inside the existing `week-01-proof-statement/` index, per the convention already established for FL-01.

## Reflection

The pressure test's challenge to "walkthrough" was the sharpest moment here — a single word in the sitemap was quietly letting the Work page prove the wrong thing (output, not reasoning). Catching that before building anything, rather than after, is exactly what the pressure-test assignment is for.

## Decisions made this session

- Tech Stack merged into Work as badges, not a standalone page
- Work page restructured from walkthrough to case study — see [ADR context in FL-03 notes](./fl-03-notes.md) for the reasoning trail this connects to

## Links

- Deliverable: [`fl-02-sitemap-pressure-test.md`](./fl-02-sitemap-pressure-test.md)
- Portfolio Project instructions: [`fl-02-portfolio-project-instructions.md`](./fl-02-portfolio-project-instructions.md)
- Screenshots (pending): `./screenshots/fl-02-sitemap-sketch.png`, `./screenshots/fl-02-portfolio-project-config.png`
