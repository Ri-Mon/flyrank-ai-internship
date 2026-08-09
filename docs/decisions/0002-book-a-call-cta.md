# 0002. "Book a call" as the portfolio's primary CTA

- **Date:** 2026-08-08
- **Status:** Accepted

## Context

FL-03's proof statement needs one specific action a visitor takes after being convinced. Three real options existed for what that action is, and this choice shapes every page of the portfolio site built weeks 4-10 — the Contact page, and arguably the whole site's persuasion arc, point toward whichever action gets picked here.

## Options considered

1. **"Book a call"** — live conversation, momentum toward the actual outcome (getting hired)
2. **"Email me"** — lower-friction, asynchronous, easier for a hesitant visitor to start with
3. **"Invite me to interview"** — most formal, but skips a step; assumes trust already established

## Decision

"Book a call."

## Why

Initially felt like the highest-risk option — live conversation puts more on the line than an email. But two things resolved that: it matches how I actually communicate better (talking over writing, already a known preference), and reframing the risk helped — a call isn't "live pressure to perform," it's "thinking out loud with someone," which is a much more accurate description of what actually happens. It also has the most direct line to the real goal: getting hired, not just getting acknowledged.

## Consequences

- Every future week's Work/About/Contact page content should build toward this action specifically, not a generic "get in touch."
- The Work page's restructuring (walkthrough → case study, see FL-02 notes) is a direct consequence of this: proving *reasoning*, not just output, is what makes someone confident enough to book a call rather than just skim and leave.
- If a future week's pressure test reveals "book a call" isn't landing (e.g. visitors bounce at Contact), that's a signal to revisit this ADR, not silently work around it.
