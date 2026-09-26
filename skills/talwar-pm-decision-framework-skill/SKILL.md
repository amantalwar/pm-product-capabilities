---
name: talwar-pm-decision-framework-skill
description: Structure a high-stakes or contentious decision — which option to pick, how much process it deserves, and how to document it. Use for "help me think through this decision," "we're stuck choosing between these options," "how much sign-off does this actually need," or "write up why we decided this" — especially when a decision is stalling in endless debate.
---

# Decision Framework

## Why this matters

Most decision paralysis comes from applying uniform process to decisions that don't deserve uniform process. Jeff
Bezos's one-way/two-way door framing is the useful lever here: a two-way door — reversible, cheap to undo, low
blast radius — should be decided fast, by the people closest to it, with a lightweight record, because the cost of a
wrong call is just "change it back." A one-way door — irreversible, expensive or impossible to undo, wide blast
radius — deserves real deliberation, broader input, and explicit sign-off, because the cost of a wrong call is
stuck with. The failure mode in both directions is common: treating a reversible pricing experiment like a
constitutional amendment (weeks of committee review for something you could A/B test in a day), or treating an
irreversible architecture choice or public commitment like a quick Slack poll. The amount of process should scale
with reversibility and the cost of being wrong — not with how senior the requester is or how long the debate has
already dragged on.

## Gather inputs first

Ask if not given (assume and state it if told to proceed):

- **The decision** and the options actually on the table (not just the two people are debating loudest — there may
  be a third nobody's named)
- **What triggers the decision** — a deadline, a blocked team, a customer commitment
- **Reversibility**: can this be undone, at what cost, over what timeframe, if it turns out wrong
- **Blast radius**: who is affected if this is wrong — one team, the whole product, customers, external partners
- **Who actually needs to be involved** — versus who's currently in the room out of habit

## Process

1. **Classify the door type first, before debating options.** Ask explicitly: if we pick wrong, can we reverse this,
   and what would that cost in time/money/trust? A "yes, within a sprint, no customer impact" answer means this is a
   two-way door. A "no, or only at major cost/embarrassment" answer means one-way.
2. **Scale process to the classification, not to the loudest opinion in the room**:
   - **Two-way door** — assign a single decision-owner, set a short deadline, decide with available information,
     document briefly, move on. Revisit only if new information actually contradicts the choice.
   - **One-way door** — widen input deliberately (the people who'd bear the cost of being wrong), lay out real
     alternatives with tradeoffs, and get explicit sign-off from whoever owns the consequence, before proceeding.
3. **List the real options, including "do nothing"** as an explicit option with its own cost — teams often compare
   one action against an unstated status quo instead of stating the status quo's cost plainly.
4. **State the criteria before comparing options**, not after picking a favorite and reverse-engineering
   justification. Criteria should be the 2-4 things that actually matter for this decision (cost, speed, reversibility
   itself, customer impact, team capacity) — not a generic checklist copied from the last decision doc.
5. **Make the call and write down why**, including what would change your mind later. The reasoning is more valuable
   than the choice — it's what lets someone revisit the decision intelligently if circumstances shift, instead of
   re-litigating from scratch.
6. **Set a revisit trigger only for one-way doors or explicitly time-boxed two-way-door experiments** — not a vague
   "let's check in sometime," but a specific date or metric threshold that would prompt reconsideration.

## Output template

```markdown
# Decision Record: [Decision name]

## Door type: [One-way / Two-way]
Reasoning: [reversibility and blast radius if wrong]

## Decision
[The specific choice being made]

## Options considered
| Option | Pros | Cons | Reversibility |
|---|---|---|---|
| [Option A] | | | |
| [Option B] | | | |
| Do nothing | | | |

## Criteria used
[The 2-4 things that actually mattered for this call, stated before the choice]

## Chosen option
[Which one, and the one-paragraph "why" — the reasoning, not just the label]

## What would change this
[Specific information or metric that would trigger a revisit — omit for two-way doors decided and closed]

## Owner & sign-off
[Who owns this decision, who else signed off if it was a one-way door]
```

## Quality checklist

- [ ] The door type (one-way/two-way) is classified explicitly, before process is applied
- [ ] "Do nothing" appears as a real option with its own stated cost, not left implicit
- [ ] Criteria are stated before the chosen option is justified, not reverse-engineered after
- [ ] The record captures why, not just what — enough for someone else to revisit it later without re-litigating
- [ ] Process weight (input breadth, sign-off, deadline) actually matches the door classification, not the seniority of who's asking

## Related skills

- Stress-test a one-way-door choice before committing: `talwar-pm-pre-mortem-skill`
- Generate the real option set before applying this framework: `talwar-pm-solution-options-generator-skill`
- Turn the decision into a broader executive narrative: `talwar-pm-decision-memo-skill`
- Score multiple candidate options against criteria: `talwar-pm-prioritization-matrix-skill`
