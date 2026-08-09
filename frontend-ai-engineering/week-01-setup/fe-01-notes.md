# Week 01 — Environment and AI Toolchain

- **Assignment:** FE-01 — Environment and AI Toolchain
- **Status:** ✅ Complete

## Goal

Set up a working AI-assisted dev environment, a standalone capstone repo with required files, and 3+ Conventional Commits documenting the setup.

## What I built

Full work: [frontend-ai-engineering-project](https://github.com/Ri-Mon/frontend-ai-engineering-project), branch `setup/environment-and-toolchain`

- New standalone repo (not the journal monorepo — deliberate, see decision flag below)
- `README.md`, `.gitignore` (Node.js), `LICENSE` (MIT)
- `.github/copilot-instructions.md` — Copilot-native rules file covering stack, coding standards, commit/branch convention, AI collaboration guidelines
- Toolchain decision: VS Code + GitHub Copilot as primary editor/critique tool, Antigravity as primary agent for build work — based on free-tier volume comparison (Copilot: 50 chat/agent requests/month; Antigravity: ~20/day, roughly 10x more headroom despite reliability caveats)
- Four Conventional Commits, one branch, one PR (`FE Track – Setup: Environment and AI Toolchain`)

## Prompts used, and why

- To Copilot Chat: *"Please critique my root README.md for the Frontend-ai-engineering-project repository. Focus on clarity, professionalism, and completeness. Suggest one specific improvement."* — scoping to 3 named criteria plus forcing "one specific improvement" prevented vague blanket praise and produced one genuinely actionable suggestion (a roadmap section) instead of ten soft ones.

## What I changed or rejected from AI's output

- Rejected Copilot's "sound more confident and outcome-focused" feedback — too vague to act on, noted but not applied
- Rejected a "Project Goal" section Copilot suggested independently — premature, since capstone direction isn't chosen yet, and would contradict the existing "Setup phase" status
- Accepted but reshaped the roadmap suggestion — turned a vague "add a section" into a concrete 6-item checklist tied to the real track structure, since it self-updates across 10 weeks instead of needing rewritten prose each time
- Caught and fixed my own factual error from an earlier draft — had conflated "Google AI Studio" and "Antigravity" in the first rules-file pass
- Reversed an earlier structural call — initially planned to skip LICENSE/.gitignore assuming monorepo inheritance, corrected once the standalone-repo decision was made
- Declined to manufacture a flaw in the README before asking for critique — used a genuine first draft, since deliberately degrading it would test nothing real

## QA / verification notes

- Confirmed Copilot only auto-loads `.github/copilot-instructions.md` at that exact path, not any arbitrary filename
- Verified via VS Code's References list that Copilot is actually using the instructions file, not just assumed
- Flagged: downloaded files lose their folder path — `.github/copilot-instructions.md` must be manually placed in a `.github/` folder after download

## Reflection

Delegate-vs-collaborate showed up concretely here: the README critique was a genuine delegate step (Copilot returned a finished suggestion I evaluated), while the rules-file refinement was collaborative — iterative back-and-forth that caught a real factual error. Also built a habit worth keeping: attributing commits to the *specific* tool ("Copilot critique" vs. "Claude review") rather than a generic "AI" — small thing, but it's the difference between a trustworthy git history and a vague one.

## Decisions made this session

- **Standalone repo for the capstone, not the journal monorepo** — durable enough to warrant its own record; see [ADR-0001](../../docs/decisions/0001-standalone-capstone-repo.md)
- Branching: one feature branch per task, no module-number prefix — differs from this journal's `week-NN` folder naming, which is fine, since these are two different repos serving two different purposes (see `docs/git-workflow.md` scope note)
- Screenshots live at `docs/screenshots/<branch-name>/` in the capstone repo — corrects an earlier flat-file suggestion from the documentation chat, which assumed a prefix convention this repo doesn't actually use
- Rules file: `.github/copilot-instructions.md` for now, chosen over promoting the journal's `claude-md-draft.md` into a `CLAUDE.md` — FE-02's brief explicitly allows either ("CLAUDE.md or rules file"), so this isn't a deviation from the assignment, just a tool-specific choice
- "Thin entry point" pattern (one `AGENTS.md` as source of truth, tool-specific files as short pointers to it) — noted for later, not yet implemented

## Links

- Repo: [frontend-ai-engineering-project](https://github.com/Ri-Mon/frontend-ai-engineering-project)
- Branch/PR: `setup/environment-and-toolchain` — "FE Track – Setup: Environment and AI Toolchain"
