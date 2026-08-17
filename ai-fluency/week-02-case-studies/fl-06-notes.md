# FL-06 — Prompting Fundamentals on Real Tasks v2

- **Assignment:** FL-06 — Prompting Fundamentals on Real Tasks v2
- **Status:** ✅ Complete

## Cross-track connection, worth noting explicitly

The "real task" here is literally FE-02's actual work — email validation on the settings form (`App.jsx`) in the capstone repo. **FE-02 itself hasn't been formally wrapped up in this journal yet** (no `frontend-ai-engineering/week-0X/` folder for it exists as of this entry), so this note is a forward pointer, not a substitute for that write-up. When FE-02 gets its own wrap-up session, that entry should cross-reference this one — the Zod schema, the `npm install zod` dependency fix, and the validation logic itself all originate from this FL-06 session, not separately from FE-02's own work.

## Goal

Build a six-run prompt iteration log (naive baseline + 5 named-technique versions) around a real FL-01 target task, run the final stacked prompt on both Claude and ChatGPT for an honest cross-model comparison, and produce a stranger-usable reusable template.

## What I built

Full deliverable: [`fl-06-prompt-iteration-log.md`](./fl-06-prompt-iteration-log.md)

- Selected Target C (reviewing my own code for bugs) as the FL-01 task, applied to a genuine gap in FE-02's settings form
- Baseline + five versions, each tied to exactly one named technique: role assignment → context/motivation → few-shot examples → step decomposition → output structure
- Actually implemented and manually tested each version's code live in the running app, not just reasoned about abstractly
- Cross-model comparison: same final stacked prompt run on Claude and ChatGPT against the real `App.jsx` code
- Final reusable template with placeholders — now also added to [`prompts/reusable-prompts.md`](../../prompts/reusable-prompts.md)

## Prompts used, and why

- Each technique chosen reactively based on the previous version's diagnosed weakness, not pre-planned — role first (to set approach before adding constraints), then context/motivation (to supply the Zod requirement naturally), then few-shot examples (once two prior techniques failed to fix the same bug, indicating the actual boundary had never been specified).
- Test cases were real, adversarial inputs (`a.a@a`, `A@A.A`, `0@gmail.com`, `Name@gmail.com`) manually run in the live app at every version, not assumed from reading code.

## What I changed or rejected from AI's output

- Rejected treating `0@gmail.com` and `Name@gmail.com` as bugs after checking real-world email rules — confirmed both were correct behavior (valid short local part; case normalization, not rejection), preventing a false "still failing" note from entering the log.
- Corrected two of my own notes mid-session — "detail-oriented" and "changed the tone" replaced with the actual named technique, since notes need to identify the lever pulled, not describe the vibe of the result.
- Redirected two attempted "what I'd try next" answers that were actually product/feature ideas (an edit button, form security restructuring) back to prompting techniques — the ladder's next-step notes have to stay about the prompt, not the app.
- Declined to accept "no need to worry" as a two-word approval for Version 0 — pushed for a specific technical reaction before letting the note stand.

## QA / verification notes

- Caught a real environment bug independent of the prompting exercise: `zod` was never installed as a dependency, causing `npm run build` to fail even though dev/preview worked — resolved via `npm install zod`.
- Verified all four originally-failing test cases were manually confirmed rejected in the live app once Version 3 shipped, not just assumed from reading the refine logic.
- Cross-model differences (normalization gap, accessibility attributes, schema scope, error granularity) read directly from ChatGPT's actual returned code, not inferred.

## Reflection

The strongest finding this session was that the same core bug survived two separate named techniques in a row (role, then context/motivation) before few-shot examples actually fixed it — a clean demonstration that some techniques change *how* the model talks about a problem without changing whether it can actually solve it. The real fix was specifying a boundary that had never been stated, not applying more pressure with a different technique.

## Glossary flags (added to `docs/glossary.md`)

- **Step Decomposition** — instructing the model to produce and justify a plan before any implementation, so a wrong plan can be caught before code is written, not after.
- **Few-Shot Examples as Boundary-Setting** — per Anthropic's own guidance, most reliable specifically when a rule is hard to state abstractly (like "realistic domain shape") — confirmed directly by this session.

## Decisions made this session

- Target C chosen over A/B specifically because debugging is inherently sequential, giving the strongest natural fit for step decomposition
- Declined testing both a portfolio task and a CV task, or multiple projects — kept scoped to one real, working piece of code
- Treated the role-assignment version's persona-without-substance result as the honest "didn't help" moment, since it survived two techniques, not one

All scoped methodology calls, not repo/site architecture — kept here rather than as ADRs, same bar as every prior week.

## Links

- Deliverable: [`fl-06-prompt-iteration-log.md`](./fl-06-prompt-iteration-log.md)
- Final reusable prompt also lives in: [`prompts/reusable-prompts.md`](../../prompts/reusable-prompts.md)
- Connects forward to: FE-02 (not yet documented in this journal)
