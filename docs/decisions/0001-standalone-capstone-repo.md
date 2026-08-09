# 0001. Standalone repo for the FE capstone, not the journal monorepo

- **Date:** 2026-07-30 (recorded; original decision made during FE-01)
- **Status:** Accepted

## Context

FE-01 required scaffolding the actual project that becomes the FE capstone (routes, config, deployment eventually). The journal repo (`flyrank-ai-internship`) already existed as a documentation-only repo. Question: does the capstone code live inside a folder of the journal repo, or in its own separate repo?

## Options considered

1. **Folder inside the journal monorepo** — one repo total, everything in one place; but mixes real application code (package.json, routes, dependencies) with pure documentation, and makes the journal repo's commit history noisy with implementation commits instead of write-up commits
2. **Standalone repo for the capstone** — clean separation: the journal stays documentation-only, the capstone repo is a real, deployable app with its own accurate Conventional Commits history; costs an extra repo to maintain and cross-link

## Decision

Standalone repo: [`frontend-ai-engineering-project`](https://github.com/Ri-Mon/frontend-ai-engineering-project).

## Why

Two concrete reasons, not just a preference for tidiness:

1. **Commit semantics matter for the assignment itself.** FE assignments are graded partly on accurate Conventional Commits (`feat:`, `chore:`, `docs:`, etc.) reflecting real work. A commit like `"feat: initialize repository with README and project structure"` is only true if a repository is actually being initialized — inside an already-initialized monorepo, that claim would be false.
2. **Deployment requires a real, independent app.** FE-04 onward connects the project to Vercel/Netlify with live preview URLs on every push. That needs its own `package.json`, its own build config, its own dependency tree — not a subfolder sharing a monorepo's root config.

## Consequences

- Two repos to keep in sync: the journal documents *why* and *what was learned*, the capstone repo *is* the actual product. Cross-linked both directions (journal → capstone repo in `frontend-ai-engineering/README.md`; capstone repo → journal in its own "Documentation & Process" section).
- Git conventions genuinely differ between the two repos (`docs:`-only in the journal vs. full Conventional Commits in the capstone repo) — documented explicitly in `docs/git-workflow.md`'s scope note, so this isn't a silent inconsistency.
- Standalone throwaway assignments (e.g. FE-03) get their own additional one-off repos, created reactively per assignment brief — not pre-built speculatively.
