# Week 01 — Decide What You're Proving

- **Assignment:** FL-01 — Workflow Audit & Tool Setup
- **Status:** 🚧 In progress — Claude Project screenshot still pending before this is submission-ready

---

## Goal

Produce a 12-15 task workflow audit with classification + rationale for each task, document toolkit setup (accounts, Academy course, Claude Project configuration), and define three target tasks — with specific, checkable "done well" definitions — to reuse for tracking AI-collaboration progress across FL-02 through FL-04.

## What I built

Full deliverable: [`fl-01-workflow-audit.md`](./fl-01-workflow-audit.md)

- A 12-task workflow audit table (narrowed from 21 candidates), classified across FlyRank's four categories using Ethan Mollick's task-delegation framework as the underlying model
- Toolkit setup section: Claude/ChatGPT/Academy accounts, Academy course completion, and Claude Project configuration
- Three target tasks for FL-02 to FL-04 (researching new concepts, writing front-end code, reviewing my own code), each with a measurable "Done Well" definition

## Prompts used, and why

- Asked for a classification *defense* on ambiguous tasks ("is this delegate or collaborate?") rather than accepting the first-pass label — this surfaced that the delegate/collaborate distinction is about *timing* of AI involvement (in-the-loop vs. checked-at-the-end), not output quality.
- Asked for a side-by-side comparison + recommendation when torn between two versions of Target A's definition, instead of picking blind — forced explicit trade-off reasoning between habit-forming consistency and honesty to my actual process.
- Fed peer-review feedback in for independent evaluation rather than blanket acceptance — confirmed accuracy (e.g. the "Collaborate" distribution claim) before adopting any of the suggested wording.

## What I changed or rejected from AI's output

- Rejected a fixed "3 takeaways" metric for Target A; replaced with a flexible "at least one meaningful takeaway" standard, to avoid padding on genuinely hard topics.
- Rejected baking "published to public repo" into Target A's pass/fail bar — publishing is a downstream practice, not the success condition; understanding is.
- Rewrote "assignment" → "task" in targets #3 and #4, for scope durability beyond the internship period itself.
- Reordered the audit table to follow actual build-cycle logic (research → brainstorm → code → debug → organize) instead of the arbitrary grouping AI produced first.
- Declined to add a subfolder for a single screenshot — kept it flat; will revisit if future weeks generate more assets.
- Declined mentioning backend-novice status in the toolkit section — judged it out of scope there, more relevant to an identity/reflection section if one comes up later.
- Let go of an initial "exactly 15 tasks" target once 12 honestly-recurring ones were left after cutting redundant candidates — a forced count would've meant padding the list with tasks that weren't genuinely recurring, which defeats the point of an honest audit.
- Considered adding capstone planning to the recurring-tasks list, then cut it — it's a future task, not something I actually do recurringly yet. Audit should reflect my actual week, not my planned one.

## QA / verification notes

- Task distribution recomputed and confirmed accurate: Just Me (4) · Delegate (2) · Collaborate (6) · Fully Automate (0)
- Cross-checked classification logic against Mollick's original framework directly, not just FlyRank's four-label adaptation
- **Outstanding:** Claude Project configuration screenshot still needs to be captured and dropped into `./screenshots/fl-01-claude-project.png` before this is genuinely submission-ready

## Reflection

The hardest part wasn't classifying tasks — it was defending *why* each classification was right, especially catching that "delegate vs. collaborate" hinges on whether AI is in the loop while I'm working through something versus handed a finished task to check. Also caught myself almost dropping my actual coding work off the task list entirely, which would have undercut the whole audit's credibility for a front-end role.

Two process lessons worth keeping for future audits:
- **Generate first, filter later.** I built an initial list of 15 tasks entirely on my own before bringing in any AI input — that gave me something real to cut down from, rather than trying to write a "correct" list from a blank page. Easier to edit than to originate under pressure.
- **Scope has to mean my actual week, not my internship-only week.** I initially only thought about internship tasks, which produced a narrower, less honest list. Broadening to study, side projects, and LinkedIn is what made the audit actually reflect how I work, not a curated version of it.

## Glossary flags (added to `docs/glossary.md`)

Framework source: Ethan Mollick, ["On-boarding your AI Intern"](https://www.oneusefulthing.org/p/on-boarding-your-ai-intern)

- **Centaur Tasks** (Mollick) → mapped to FlyRank's "Collaborate with AI" — AI woven into the workflow through iteration, not handed a finished ask
- **Delegated Tasks** (Mollick) → mapped to "Delegate with review" — defined handoff, checked at the end
- **Automated Tasks** (Mollick) → "Fully automate" — flagged as a deliberately small, risky category, not a gap in the audit

## Notes on scope decisions

A few wording/structure calls were made during this assignment (task vs. assignment phrasing, target task swaps, table ordering) — these are captured above in "What I changed or rejected," not as separate decision records. They're judgment calls scoped to this one assignment's content, not durable structural choices affecting future work, so they don't warrant their own entry in `docs/decisions/`.

## Links

- Deliverable: [`fl-01-workflow-audit.md`](./fl-01-workflow-audit.md)
- Screenshot (pending): `./screenshots/fl-01-claude-project.png`
