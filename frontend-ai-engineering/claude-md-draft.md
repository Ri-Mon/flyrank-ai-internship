# CLAUDE.md — Draft (superseded, kept for reference)

**Status:** superseded. The capstone repo now exists ([`frontend-ai-engineering-project`](https://github.com/Ri-Mon/frontend-ai-engineering-project), created during FE-01), and it uses `.github/copilot-instructions.md` instead of this file — FE-02's brief explicitly allows "CLAUDE.md or rules file," so this isn't a deviation, just a tool-specific choice made in the moment. Kept here for reference in case a Claude-specific instructions file or the "thin entry point" pattern (see `docs/glossary.md`) gets adopted later.

**Provenance:** self-drafted (my own write-up, not something a mentor provided or confirmed).

---

## FlyRank AI Internship Project Rules

### Purpose

This file provides guidance for AI assistants collaborating on this repository. Follow these conventions unless the user explicitly requests otherwise.

---

### Technology Stack

**Frontend**
- React
- JavaScript (ES6+)
- HTML5
- CSS3

**Development Tools**
- Node.js (LTS)
- Git
- GitHub
- Visual Studio Code

**AI Tools**

AI assistance may come from GitHub Copilot, Gemini, Claude, Google AI Studio (Antigravity), or other free AI coding tools. Focus on engineering principles and best practices rather than tool-specific workflows unless explicitly requested.

---

### Coding Standards

When generating or reviewing code:
- Prefer semantic HTML
- Write modern JavaScript (ES6+)
- Build small, reusable React components
- Keep components focused on a single responsibility
- Prioritize readability over cleverness
- Prefer maintainable solutions over unnecessary complexity
- Avoid unnecessary dependencies
- Follow accessibility and responsive design best practices

---

### Git Workflow

Use the Conventional Commits 1.0.0 specification for every commit.

Common commit types: `feat`, `fix`, `docs`, `refactor`, `style`, `test`, `perf`, `chore`

Primary branch: `main`

---

### AI Collaboration Guidelines

When assisting with this repository:
- Explain concepts before providing complete solutions whenever practical
- Encourage understanding rather than copying
- Explain trade-offs when multiple valid solutions exist
- Recommend an approach based on the project context without presenting it as the only correct solution
- Review AI-generated code critically before it is committed
- Prioritize maintainability, accessibility, performance, and security
- Ask clarifying questions when requirements are ambiguous
- Keep recommendations concise unless detailed explanations are requested
- Remember that this repository is both a learning resource and a professional portfolio

---

### Documentation Guidelines

- Keep documentation concise and accurate
- Update documentation when implementation changes
- Avoid duplicating information already documented elsewhere
- Refer to the root `README.md` for repository structure and navigation

---

## Reference: first three commits (self-drafted sequence, not mentor-confirmed)

Onboarding sequence for a fresh capstone repo, using this file's own commit convention:

| # | Conventional Commit Message | What to do |
|---|---|---|
| 1 | `feat: initialize repository with README and project structure` | Add/update README with project title, description, stack, setup instructions. Add `.gitignore` (Node.js template). |
| 2 | `chore: add license and AI assistant configuration` | Add a LICENSE file (MIT is standard). Add this file as `CLAUDE.md` (or tool-equivalent). |
| 3 | `docs: improve README based on AI critique` | Ask an AI assistant to critique the README, apply one real improvement, commit the change. |

**Note on scope:** this Conventional Commits convention (`feat`/`fix`/`docs`/`refactor`/etc.) applies to the **capstone project repo** specifically, once it exists — it's different from this journal repo's simpler `docs:`-only convention documented in [`../docs/git-workflow.md`](../docs/git-workflow.md), which is appropriate for a docs-only repo but not for a real application codebase with actual feature/fix/refactor work happening.
