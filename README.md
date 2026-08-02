# FlyRank AI Internship — Journal & Evidence Trail

This repo is my process log for the [FlyRank AI Internship](https://internship.flyrank.ai): what I built, what I learned, and how AI helped along the way.

I'm working two tracks in parallel:

- **[General AI Fluency](./ai-fluency/)** — a 10-week program culminating in a live personal portfolio site. Mentors listed in the track's own README.
- **[Front-End AI Engineering (FE)](./frontend-ai-engineering/)** — also a 10-week program, covering site foundations, responsive execution, storefront patterns, and AI implementation QA, ending in a capstone. Mentor listed in the track's own README.

> **Note on scope:** this repo is the *journal*, not the product. The actual portfolio site (built during AI Fluency, weeks 4–10) lives in its own repo, linked below once it exists, so it can stand alone as a clean deliverable for recruiters.

## About FlyRank

FlyRank is an AI-powered platform for organic and AI-search growth — it automates content strategy, creation, optimization, and localization for brands, and also optimizes for visibility in AI answer engines like ChatGPT, Perplexity, and Claude, not just traditional Google search. This internship program is run under the FlyRank AI brand.

Official links: [Website](https://flyrank.ai) · [LinkedIn](https://www.linkedin.com/company/flyrank/)

## About the internship

[The FlyRank AI Internship](https://internship.flyrank.ai) is remote, self-paced, and unpaid. It's structured around six tracks (General AI Fluency, AI Marketing, Front-End AI Engineering (FE), Backend AI Engineering, Machine Learning, and UX/Design), each pairing a specialization with the shared AI Fluency foundation. The program is explicitly educational, not an employment arrangement: no degree or prior experience required, and completion earns a verifiable credential plus an eligible recommendation letter rather than a paycheck.

_Noted here for anyone landing on this repo without that context. Track-specific detail on my own two tracks lives in their respective folders below._

## About me

Front-End AI Engineering Intern at FlyRank AI. Some prior, independent experience with Python and Django from outside this internship — not affiliated with FlyRank's separate Backend AI Engineering track, which I haven't taken. Currently building fluency in React and AI-assisted front-end development.

## Objectives

Through this internship, I aim to:
- Build real fluency in AI-assisted software development, not just tool usage
- Ship production-ready front-end work, documented with genuine reasoning
- Sharpen prompt-engineering judgment — knowing why a prompt works, not just that it does
- Build in public: document the process honestly, including what didn't work
- Come out with portfolio-ready proof, not just a completion credential

## Live links

| What | Link |
|---|---|
| Portfolio site (in progress) | _add once deployed_ |
| FlyRank credential | _add once verified_ |

## Repo structure

```
flyrank-ai-internship/
├── ai-fluency/          # AI Fluency track, one folder added per week as I start it
├── frontend-ai-engineering/  # Front-End AI Engineering track, one folder per week (mirrors AI Fluency), added as I start it
├── prompts/              # My own reusable prompt library, with reasoning
├── assets/               # Cross-track visuals: certificates, diagrams — not per-assignment screenshots
├── docs/
│   ├── build-log.md      # Running informal devlog — raw material for LinkedIn posts
│   ├── resources.md      # Cached snapshot of official program info + known discrepancies
│   ├── glossary.md       # Tech concepts I've actually run into, in my own words
│   └── decisions/        # Short decision records (ADRs) — the "why" behind real choices
├── templates/            # Reusable write-up template used for every week/module
└── LICENSE                # MIT
```

## How I document each week/module

Every folder follows the same template (see [`templates/week-template.md`](./templates/week-template.md)):
goal → what I built → prompts used and why → what I changed or rejected from AI's output → QA notes → reflection.

The "what I changed or rejected" section matters most — it's the difference between *using* AI and *directing* it, which is what both tracks (and this documentation habit) are actually testing for.

## Workflow

**Git:** one branch + one PR per week/module, not direct commits to `main`. Full step-by-step (commands included, written for a beginner): [`docs/git-workflow.md`](./docs/git-workflow.md).
- Branch naming: `ai-fluency/week-01`, `frontend-ai-engineering/week-01`
- PR title: `AI Fluency – Week 01: Proof Statement` (track, week/module, short title)
- PR description: 2-3 lines — what was done, link to the write-up folder
- Merge once the write-up is complete and reviewed; delete the branch after

Why: commit/PR history is something interviewers actually look at. Small, real PRs per week demonstrate genuine workflow discipline for close to zero extra effort.

**Build log:** a new dated entry gets appended to `docs/build-log.md` every session, drafted from that session's wrap-up summary — not just the ones that end up LinkedIn-worthy. This is the raw, complete record; the LinkedIn flag below is a subset of it, not a replacement for it.

**LinkedIn pipeline:** not per-week. Posting cadence is **after a series of weeks** (my own judgment on when a batch feels post-worthy), plus optionally one larger wrap-up post after the full internship.
1. At a natural checkpoint — end of a project phase, or whenever a batch of weeks feels like enough material — open `docs/build-log.md`
2. Pull everything flagged "yes" under **Good LinkedIn-post material?** across that batch
3. Draft one post from the strongest moment(s) — a real decision, a mistake, a turning point — not a generic "here's what I learned" recap
4. At internship end, optionally review the full build-log for a single retrospective post covering the whole journey

Why flag every session but post rarely: flagging costs nothing and captures the moment while it's fresh; deciding *whether it's post-worthy* is a separate, lower-frequency judgment call that benefits from hindsight across several weeks rather than being made in the moment.

## Progress

| # | Track | Milestone | Link | Status |
|---|---|---|---|---|
| 1 | AI Fluency | Decide What You're Proving (FL-01) | [Link](./ai-fluency/week-01-proof-statement/) | 🚧 In progress (screenshot pending) |
| 2 | AI Fluency | Frame Your Work | | Not started |
| 3 | AI Fluency | Map It & Give It a Face | | Not started |
| 4 | AI Fluency | Pick the Stack | | Not started |
| 5 | AI Fluency | Ship the Ugly Version | | Not started |
| 6 | AI Fluency | Explain Your Build | | Not started |
| 7 | AI Fluency | Make It Real (Checkpoint 1) | | Not started |
| 8 | AI Fluency | Wire One Real Thing | | Not started |
| 9 | AI Fluency | Launch & Keep Building (Checkpoint 2) | | Not started |
| 10 | AI Fluency | Send the Link (Capstone) | | Not started |
| 1 | FE Track | Site Foundations | | Not started |
| 2 | FE Track | Responsive Execution | | Not started |
| 3 | FE Track | Storefront Patterns | | Not started |
| 4 | FE Track | AI Implementation QA | | Not started |
| — | FE Track | Capstone | | Not started |

> FE rows are curriculum phases, not confirmed week numbers yet — FE is also 10 weeks (dashboard-confirmed), but the exact week-to-topic mapping gets finalized once the first FE assignment starts, same "add as you go" approach as everything else.

> Table row's Link column gets filled in as each folder is created — matches the "add as you go" approach for week/module folders.

## Skills developed

_Evolves as assignments are completed — not filled in speculatively._

| Area | Skills |
|---|---|
| AI Collaboration | Task-delegation framework application (Mollick's Centaur/Delegated/Automated model), structured workflow auditing, Claude Project configuration |
| Documentation | Writing checkable "done well" criteria, honest gap-flagging (e.g. no test suite yet) over hiding weaknesses |

## Achievements

- ✅ AI Fluency: Framework & Foundations course (Anthropic Academy)
- ✅ Claude 101 course (Anthropic Academy)

## Mentors & guest mentors

Mentored by FlyRank AI staff and guest mentors, track by track — see each track's own README for names and roles directly relevant to my work, or the [official mentors & guest mentors page](https://internship.flyrank.ai/mentors#guest-mentors) for the full current roster.

## Feedback

Documenting this internship publicly as part of the learning process. If you spot something worth improving, feel free to [open an issue](https://github.com/Ri-Mon/flyrank-ai-internship/issues).

## Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?logo=linkedin)](https://www.linkedin.com/in/md-mahmudul-hasan-rimon/)
[![GitHub](https://img.shields.io/badge/GitHub-Profile-black?logo=github)](https://github.com/Ri-Mon)