# Program Resources (Cached Snapshot)

Official pages move / get gated behind login as cohorts change, so key facts are captured here in my own words, with links to the live source. Treat this file as "true as of the date noted," not live-synced — re-check the source links periodically and update if something material changes.

Last verified: 2026-07-25

## Official sources

- AI Fluency Track: https://aifluency.flyrank.ai/
- Front-End AI Engineering Track: https://internship.flyrank.ai/tracks/fe
- All six tracks overview: https://internship.flyrank.ai/tracks
- AI Builder Ladder (skill rubric): https://internship.flyrank.ai/ladder

## AI Fluency Track — key facts

- 10-week, project-based program. The single deliverable across all 10 weeks is one live portfolio site.
- Mentor: Léo Yiğit Ekiz, Director of AI Enablement.
- Structure: Weeks 1-3 setup/foundations, Weeks 4-6 build, Weeks 7-9 make-it-real + launch prep, Week 10 capstone.
- Two gated checkpoints: Week 7 (design review) and Week 9 (hardening / "try to break your own site" review). Both must pass before Week 10 counts.
- Public page listed 17 total assignments across weeks 1-9 — **my actual dashboard shows ~30**, so the live portal is the accurate count, not this page. See `../frontend-ai-engineering/README.md` note on the same mismatch.
- Week 4 ("Pick the Stack") is a structured "Three Roads" exercise: AI proposes three stack options, you pressure-test them against your own constraints, and write a rationale for the one you pick. Don't pre-decide a stack before this week.

## Front-End AI Engineering Track — key facts

- Timeline: 10 weeks — **dashboard-confirmed**, mirrors AI Fluency's length. The public page only states a ~6-10 hrs/week pace with no fixed week count; the actual program has a real 10-week structure not visible on the public page.
- Curriculum: (1) Site foundations, (2) Responsive execution, (3) Storefront patterns (Shopline/Shopify-style), (4) AI implementation QA.
- Capstone options: personal site / Shopline-Shopify-style storefront / client-brief site.
- Review criteria: visual fidelity, responsiveness, code structure, browser QA notes.
- Approved stack examples: Next.js/React, Vite+React, Astro, Tailwind, Liquid — framework choice matters less than clean, responsive execution.
- Public page gave no assignment count — my dashboard shows ~16.

## AI Builder Ladder — key facts

- Skill progression: Curious → Tinkerer → Builder → Shipper, scored across mindset, practice, output, judgment.
- Most applicants enter at Curious/Tinkerer; the internship's explicit goal is to land you at Builder by the end.
- FE-specific Builder signal: a deployed app (Vercel/Netlify) built with AI as co-pilot, with the ability to articulate what AI got right vs. what had to be rewritten.
- FE-specific Shipper signal: shipping UI fast and confidently, maintaining a personal stack of patterns/components/prompts that compound across projects — this is the direct justification for keeping `../prompts/reusable-prompts.md`.

## Known discrepancies between public pages and dashboard

| Fact | Public page said | Dashboard says | Which one's trusted |
|---|---|---|---|
| AI Fluency assignment count | 17 (weeks 1-9) | ~30 (weeks 1-9) | Dashboard |
| FE track assignment count | Not listed | ~16 (weeks 1-9) | Dashboard |

Rule going forward: dashboard > public pages, always, for anything cohort-specific (counts, deadlines, exact titles). Public pages are trusted for the general shape of the program (phases, review criteria, stack options, ladder rubric) since those are unlikely to be cohort-specific.
