# Git Workflow — Step by Step

A checklist to follow every time a task/assignment write-up is finished, from local files to a merged PR. Written for someone new to Git — every command is spelled out, nothing assumed.

Matches the convention set in the root README: **one branch, one PR, per week/module.**

---

## 0. One-time setup (skip if already done)

```bash
git clone https://github.com/<your-username>/flyrank-ai-internship.git
cd flyrank-ai-internship
```

If the repo's already cloned and connected locally (it is), skip this.

---

## The checklist — run every time something's finished

### 1. Make sure you're starting from a clean, up-to-date `main`

```bash
git checkout main
git pull origin main
```
**Why:** starting a new branch from an outdated `main` can cause messy conflicts later. This takes five seconds and prevents that.

### 2. Create the branch

```bash
git checkout -b ai-fluency/week-01
```
(or `git checkout -b frontend-ai-engineering/module-01`, matching whichever track/week you just finished)

**Why a new branch instead of working directly on `main`:** it keeps `main` always in a clean, working state, and gives each week its own reviewable unit of change — the actual habit we're building.

### 3. Add the new/updated files

```bash
git add ai-fluency/week-01-proof-statement/
```
Point this at whatever folder or file actually changed — I'll always tell you the exact path when I hand off files.

**Check what's staged before committing (good habit, catches mistakes):**
```bash
git status
```

### 4. Commit with a clear message

```bash
git commit -m "docs: add AI Fluency Week 1 — Proof Statement"
```
**Why this format:** `docs:` prefix signals "this is documentation, not code" at a glance — useful once you have dozens of commits. Keep the message short and specific: what was added, not "update files."

### 5. Push the branch to GitHub

```bash
git push -u origin ai-fluency/week-01
```
The `-u` links your local branch to the remote one — after this, plain `git push` works for this branch without repeating the full command.

### 6. Open the Pull Request

Easiest: GitHub will show a yellow banner with a **"Compare & pull request"** button right after you push — click it.

Fill in:
- **Title:** `AI Fluency – Week 01: Proof Statement` (track, week/module, short title)
- **Description:** 2-3 lines — what was done, link to the write-up folder

Click **Create pull request**.

### 7. Review your own PR before merging

Open the "Files changed" tab, read through your own diff once. This is the moment to catch a stray typo, a leftover placeholder, or something you meant to remove. Treat it like the final proofread.

### 8. Merge

Click **Merge pull request** → **Confirm merge**.

### 9. Clean up

```bash
git checkout main
git pull origin main
git branch -d ai-fluency/week-01
```
Pulls the merged change back into your local `main`, and deletes the now-unneeded local branch. On GitHub, there's usually a **"Delete branch"** button right on the merged PR page too — click that as well.

---

## Quick reference (once this feels familiar)

```bash
git checkout main && git pull origin main
git checkout -b <track>/<week-or-module>
git add <path>
git commit -m "docs: <what was added>"
git push -u origin <track>/<week-or-module>
# open PR on GitHub, review, merge
git checkout main && git pull origin main
git branch -d <track>/<week-or-module>
```

## Common early mistakes (so they're not a surprise)

- **Forgetting `git pull origin main` before branching** — leads to a PR that looks like it's changing more than it actually is.
- **Vague commit messages** ("update", "fix stuff") — costs you later when you're trying to find when something changed.
- **Committing straight to `main`** — breaks the entire point of this workflow. If it happens once, no disaster — just start the branch/PR habit again next time.
- **Forgetting to delete the branch after merging** — harmless, just clutter. Clean up when you notice.
