# Build Log

A running, chronological, informal log — separate from the polished week/module write-ups. This is where the honest, in-the-moment notes go: what broke, what clicked, what took way longer than expected. It's raw material for LinkedIn posts and interview stories, so it's fine for this to be messier than the rest of the repo.

Format: one entry per session, newest at the top.

---

<!--
### yyyy-mm-dd

**Session focus:** [what I worked on]

**Notes:**
-

**Good LinkedIn-post material?** [yes/no — flag anything that'd make a decent build-in-public post]

**🏆 Badge earned?** [none / name it if a GitHub achievement genuinely unlocked this session — no manufacturing activity just to trigger one]
-->

<!-- Add new entries above this line -->

### 2026-08-12

**Session focus:** FL-05 (The Prompt Ladder) — AI Fluency Week 2

**Notes:**
- Built a six-run prompt ladder (baseline + 5 versions), isolating exactly one layer per version: goal → audience → real context → output format → stated assumptions
- Refused to pre-script all six versions in advance, even though it would've been faster — reactive diagnosis based on each version's actual output was treated as non-negotiable to the exercise being real
- Caught a genuine regression at Version 3: adding real context made the response specific, but shifted it into unwanted critique instead of guidance — fixed separately at Version 4, not smoothed over as a clean improvement
- Kept skill gaps (not just comfort areas) in the final reusable prompt, resisting the instinct to drop them for a cleaner-looking prompt — omitting them would've reproduced the exact Vite-blind-spot bug the ladder just diagnosed
- Final prompt added to `prompts/reusable-prompts.md` — genuinely reusable, not just an assignment artifact
- Correct assignment numbering (FL-05) carried through cleanly this time — the earlier correction to that chat held

**Good LinkedIn-post material?** yes — "fixing one wrong assumption can leave a second, different wrong assumption standing" is a transferable insight beyond just this exercise

### 2026-08-10

**Session focus:** FL-04 (Frame It as Cases) — AI Fluency Week 2

**Notes:**
- Wrote a 7-word voice card, now a standing instruction in the Portfolio Build Claude Project
- Interviewed the Tuber project (video streaming app) into a three-beat case study — problem, decision, result — one question at a time rather than letting AI draft from a vague prompt
- Verified the technical bug story (tooltip/sort-order state split) against the actual repo code, not just memory
- Rejected three bio drafts for reading as backend/data-focused tone instead of front-end — caught "messy data" framing overshadowing "interface"
- Built a real before/after: rejected a generic AI-drafted paragraph, rewrote it slower to let the actual reasoning show instead of compressing to ad-copy pacing
- Surfaced rather than hid an honest weak point: the case-study project is three years old — decided not to treat that as a liability
- Corrected a third recurring numbering error: this session's work was mislabeled FL-02 (already used) instead of FL-04 — flagged directly to the source chat this time, not just fixed silently

**Good LinkedIn-post material?** yes — the "word choice can shift what role a reader assumes you're pitching for" bio catch is genuinely specific and non-generic

### 2026-08-08

**Session focus:** FL-02 (Draw the Path) + FL-03 (What Are You Proving) — AI Fluency Week 1, closing out

**Notes:**
- Finalized proof statement + one-line why through a multi-round interview process: vague claims → narrowed audience → evidence check → CTA trade-off → length cut → peer review
- Locked 4-page sitemap (Home/Hero → Work → About → Contact), tech-stack badges merged into Work rather than a standalone page
- Configured a dedicated "Portfolio Build" Claude Project and ran the required pressure-test prompt against the sitemap
- Pressure test caught a real gap: Work page was planned as a screenshot "walkthrough," which only proves output, not the reasoning the proof statement actually claims — restructured to a case-study format instead
- Recorded ADR-0002 (CTA choice: "book a call") — durable enough to affect every future week's site content
- Caught and corrected a filename-numbering suggestion from another chat that would have misnumbered this work as `fl-01-` instead of `fl-02-`/`fl-03-`
- Outstanding: `fl-03-proof-statement.md` deliverable file and `fl-02-portfolio-project-instructions.md` still pending upload; sitemap sketch and Portfolio Project screenshots not yet captured

**Good LinkedIn-post material?** yes — the "walkthrough proves output, not reasoning" catch is a genuinely specific, well-explained insight, good candidate once batched with more weeks

### 2026-07-30

**Session focus:** Repo housekeeping — build-log template update

**Notes:**
- Added an optional "🏆 Badge earned?" field to the build-log template, same spirit as the LinkedIn flag: honest record-keeping only, no gaming achievements for their own sake

**Good LinkedIn-post material?** no — too minor, internal template tweak

**🏆 Badge earned?** YOLO (first merged PR without review, from FL-01)

### 2026-07-26

**Session focus:** FL-01 — Workflow Audit & Tool Setup (AI Fluency Week 1)

**Notes:**
- Built an initial 15-task list independently before any AI input, expanded to 21 candidates while mapping my actual week, then narrowed to the 12 final tasks below — cutting redundant or non-recurring ones rather than forcing a specific target count
- Classified all 12 using Mollick's task-delegation framework adapted to FlyRank's four categories
- Documented toolkit setup: Claude/ChatGPT/Academy accounts, AI Fluency course completion, Claude Project custom instructions
- Defined three target tasks (research, front-end code, code review) with measurable "Done Well" criteria, to reuse across FL-02–04
- Rejected AI's first-pass fixed-count metric for Target A in favor of a flexible depth-based standard — prioritized honesty to actual process over a clean-looking number
- Broadened task scope beyond internship-only work (study, side projects, LinkedIn) after an initial draft was too narrow to be an honest audit
- Added three glossary entries (Centaur/Delegated/Automated Tasks) mapping Mollick's framework to FlyRank's labels
- Outstanding: Claude Project screenshot still needs capturing before this is submission-ready

**Good LinkedIn-post material?** yes — the "delegate vs. collaborate hinges on timing, not output quality" realization is a genuinely specific, non-generic insight worth a post once batched with a few more weeks