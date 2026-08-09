# FL-02 — Sitemap Pressure Test

**Name:** Md. Mahmudul Hasan Rimon
**Date:** July 2026

---

## Prompt Used

> This is my proof statement: "I build frontends that turn a wall of options into something easier to explore. I'm proving this to a hiring manager deciding whether to trust me with real front-end work, so they'll book a call." This is my sitemap: Home/Hero → Work → About → Contact, with tech-stack badges merged into the Work page instead of a separate page. Does this sitemap walk my one person from landing, to believing me, to taking my one action, and does it actually prove my claim? Tell me which pages earn their place, which are wasted, and what is missing. Be specific, not encouraging.

---

## Output (AI)

**Short answer: the sitemap structure is sound. Landing → proof → trust → action is the right order. But one page is at risk of not doing its job, and I want to flag it before you build it.**

**Page by page:**

- **Home/Hero** — earns its place, but only if it stays lean: claim + who it's for + a nudge into Work. If it starts explaining or justifying the claim, it's stealing Work's job. Its only function is orientation and a doorway.

- **Work** — this is the page your entire claim rests on, and right now the sitemap only says "walkthrough." That word is doing a lot of unexamined work. A walkthrough of screenshots proves you can *build* a filter/sort UI. It does not prove *"how I think about turning messy data into something useful,"* which is literally your one-line why. Those are different claims. If Work is a demo tour, you've proven output, not thinking — and thinking is the thing a resume can't show, per your own reasoning. For this page to actually earn the claim, it needs a case-study structure: the wall of options as a stated problem → the specific reasoning behind what you chose to sort/filter by and why → what you rejected and why → the result. Without that reasoning trail, the page shows the same thing a GitHub repo screenshot would.

- **About** — you've justified this well (thin evidence base, one project can't carry trust alone), and I agree with the reasoning. My pushback is on scope, not placement: this page will drift toward generic bio content ("I'm passionate about tech, here's my journey...") unless you hold it to one job — answering *"why should I trust this specific person with front-end work,"* not *"tell me about yourself."* If it starts listing hobbies or a general career narrative, it dilutes the narrow claim you fought to keep narrow.

- **Contact** — earns its place, no notes. One CTA, no fragmentation, correctly matches your stated action.

**What's missing isn't a page — it's a structural requirement on Work.** The sitemap has the right shape, but as written, Work could be built as either a proof of thinking or just a proof of output, and only one of those satisfies your claim. That's a content decision you'll need to nail down before you build it, not after.

**One risk to name now, for later weeks:** your whole site is a single point of failure — one project carrying the entire claim. That's an accepted tradeoff given a 10-week scope, and About is doing real work to offset it. But watch for the temptation in week 4 or 5 to add a second project "for balance." If you do, it has to prove the *same* specific skill (reducing noise/options), or it just dilutes the claim you've spent multiple rounds narrowing.

---

## My Note — What I'm Changing (Required Deliverable)

> The Work page can't be a screenshot walkthrough. My proof statement's whole "why" is that a portfolio shows how I think, not just what I built — but a walkthrough only proves output, not reasoning. I'm restructuring Work as a case study: the wall of options as a stated problem → why I chose these specific sort/filter criteria → what I considered and rejected → the result. Without that reasoning trail, Work proves the same thing a GitHub screenshot would, which defeats the point of having a portfolio at all.
