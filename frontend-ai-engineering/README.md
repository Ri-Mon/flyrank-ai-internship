# Front-End AI Engineering Track

Ship a responsive, mobile-optimized website or ecommerce-style project with clean Tailwind execution, using AI as a pair-programmer while owning QA and final judgment myself.

**Timeline:** 10 weeks. **Review criteria:** visual fidelity, responsiveness, code structure, browser QA notes.

## Mentors

**[Adnan Travljanin ↗](https://www.linkedin.com/in/adnan-travljanin/)**
Senior Solutions Architect at Praella — mentors on component structure, responsive UI, and shipping interfaces that hold up under real product review. Based in BiH.
_What I've learned from him: add as it happens (livestreams, reviews, etc.)_

_Add guest mentors here as they're introduced: LinkedIn-linked name, then role/context._

## Weeks

Week folders are added one at a time, as I start each one — not pre-scaffolded in advance, same approach as AI Fluency. The dashboard shows ~16 assignments across weeks 1-9 plus a Week 10 capstone, mapped onto the 4 curriculum phases below — exact week-to-phase mapping confirmed from the dashboard when I reach it, since assignments may span or combine phases.

Naming convention: `week-NN-short-title/`, e.g. `week-01-site-foundations/` — matches the AI Fluency folder pattern rather than a separate module-based one. Each assignment inside gets its own file following [`../templates/week-template.md`](../templates/week-template.md); the week's own `README.md` acts as a short index if it holds more than one.

**Real roadmap** (from actual assignment briefs — replaces an earlier, less accurate guess based on the public page's generic 4-phase framing):

1. [Environment and AI Toolchain (FE-01)](./week-01-setup/) — ✅ complete
2. Capstone-relevant feature, built twice (vague vs. precise prompting) — `WORKFLOW.md` + updated rules file (FE-02)
3. React app development with AI — standalone, own repo when reached (FE-03)
4. Capstone skeleton, deployed — routes, layout, Vercel/Netlify preview (FE-04)
5. Accessible components fundamentals — modal/tabs/disclosure built by hand, then shadcn/ui comparison (FE-05)
6. Streaming AI chat interface — the capstone's central AI feature (FE-06)
7. Tool results and structured output in UI (FE-07)
8. Error, empty states, and edge cases (FE-08)
9. Micro-interactions — motion and state (FE-09)
10. Testing pass — Vitest, RTL, one Playwright E2E, CI-gated (FE-10)
11. First 3D web experience (FE-11)
12. Accessibility and performance audit — Lighthouse, WAVE, `AUDIT.md` (FE-12)
13. Signature hero — full-screen header (FE-13)
14. Production deployment and README (FE-14)
15. Case study and final submission (FE-15)
16. Certifications and capstone spec — Claude 101/Code 101, `SPEC.md` (FE-16)

_Exact week-number-to-assignment mapping still confirmed per-week from the dashboard as reached — this list is assignment order, not confirmed week grouping._

## Capstone direction

**Repo:** [frontend-ai-engineering-project](https://github.com/Ri-Mon/frontend-ai-engineering-project) — created, currently in setup phase. FE-01 (environment/toolchain foundation) and FE-02 (capstone-relevant feature drill) both live here, confirmed by their briefs — FE-02 explicitly says "capstone-relevant feature" and updates this repo's own `CLAUDE.md`. Default is this repo, always — a separate one-off repo only gets created reactively when a brief explicitly calls an assignment standalone (confirmed so far: FE-03, "any technology you feel comfortable with," disconnected from the capstone stack).

**Structure clarified via mentor Q&A**: most assignments from FE-04 ("capstone skeleton") onward build on one continuous, self-chosen project — scaffolded early, extended week over week, becoming the final capstone by roughly Week 8. A few assignments (e.g. FE-03, "React app development with AI") are standalone throwaway exercises, separate from the main project — each brief specifies which type it is.

**Practical deadline this creates:** the actual project idea needs to be chosen by FE-04, not deferred indefinitely. Options (personal site / Shopline-Shopify-style storefront / client-brief site) still stand — decide once enough of the early standalone exercises are done to have a real feel for the work, but don't push past FE-04.

**Note on overlap with AI Fluency:** the AI Fluency portfolio (built weeks 4–10 of that track) may double as some or all of this capstone if the direction lands on "personal site." Decision to be made once both tracks are further along — tracked in the root README.

**Note on repo separation:** the actual capstone project (a real React app) will need its **own repo**, separate from this journal repo — same pattern already established for the AI Fluency portfolio site. Setup guidance for that repo (commit conventions, AI-assistant config file) is being drafted ahead of time; see `claude-md-draft.md` in this folder.

## Tool stack

Decided in AI Fluency Week 4 ("Three Roads" exercise) rather than guessed upfront. Recorded here once locked in.

- Editor + AI assistant: _TBD_
- Frontend stack: _TBD (Next.js / Vite+React / Astro — React-compatible per personal preference)_
- Deployment: _TBD (Vercel / Netlify / Cloudflare Pages / GitHub Pages)_

**Signal from actual assignment briefs, not yet decided on:** FE-04's "Server Components by default, Client Components only where needed" is Next.js App Router-specific language, FE-05 explicitly requires React + TypeScript, and Assignment 16 states Next.js (App Router) + TypeScript + Tailwind as the recommended default. The capstone repo's current README lists plain JavaScript with no framework named — worth reconciling deliberately at the Week 4 decision point, not left as a mismatch.

## Notes

Each week folder follows [`../templates/week-template.md`](../templates/week-template.md).