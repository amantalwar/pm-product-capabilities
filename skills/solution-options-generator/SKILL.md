---
name: solution-options-generator
description: Generate and compare genuinely distinct solution alternatives before committing to a build, instead of rubber-stamping the first idea that came up in the meeting. Use when the user asks "what are our options here," wants a build-vs-buy or make-vs-partner comparison, says "am I missing a better approach," or jumps straight to "let's build X" and needs to be slowed down to check X against real alternatives.
---

# Solution Options Generator

## Why this matters

The most expensive failure mode in product work isn't picking the wrong solution — it's never seriously considering
more than one. Teams anchor on the first plausible idea (usually whoever spoke first in the room) and then spend the
rest of the meeting refining it instead of testing whether it's the right idea at all. This is anchoring bias plus
sunk cost showing up before any cost has actually been sunk. The fix isn't "brainstorm more ideas" — three options
that are the same UI with different button colors don't count. The fix is forcing genuine variation across a
dimension that matters: who does the work (build vs. buy vs. partner), how much you commit (pilot vs. full rollout),
or what you're willing to trade away (speed vs. control vs. cost). A real option set makes the tradeoffs visible;
a fake one just makes the chosen answer look considered.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **The problem statement**, not a pre-baked solution — if the user opens with "let's build X," first restate the
  underlying problem X is meant to solve
- **Constraints that are real** (budget, timeline, team skills, regulatory limits) vs. constraints that are just
  habit ("we always build in-house")
- **Decision-maker and decision deadline** — who has to be convinced and by when
- **What's already been tried or ruled out**, so you don't waste a slot re-proposing a dead option

## Process

1. **Restate the problem, not the solution.** If the request arrived as "build a recommendation engine," rewrite it
   as "users can't find relevant items after page 1" — the problem statement is what you generate options against.
2. **Force variation across a real axis**, not cosmetic variation. Useful axes: who builds it (in-house / vendor /
   partner), how big a bet (spike or pilot / phased / full commitment), where the effort goes (fix the workflow /
   fix the data / fix the UI), or what you protect (speed / cost / quality). Pick the axis that matters most for this
   decision and generate one option per position on it.
3. **Include the null option.** "Do nothing / defer" is a legitimate row in the comparison — it's the baseline every
   other option has to beat, and naming it explicitly stops the group from treating action as automatically better
   than inaction.
4. **Score each option on the same dimensions** — cost, risk, reversibility, expected impact — so the comparison
   isn't apples to oranges. Reversibility matters as much as impact: a cheap, low-impact, fully reversible option
   (a pilot) can be the right first move even when a competitor option scores higher on raw expected impact.
5. **Name what you'd have to believe** for each option to be the right call — the assumption that, if false, breaks
   it. This surfaces which option is actually the safest bet given what you don't yet know.
6. **Recommend one, and say why the runner-up lost.** A comparison without a recommendation just moves the work of
   deciding onto the reader; the point of this exercise is to make the decision easier, not to present a menu.

## Output template

```markdown
# Solution Options: [Problem/Decision]

## Problem statement
[The underlying problem, not a pre-chosen solution]

## Constraints
- [Real constraint 1 — budget/timeline/skills/regulatory]
- [Real constraint 2]

## Options considered

| Option | Description | Cost | Risk | Reversibility | Expected impact | Key assumption |
|---|---|---|---|---|---|---|
| A — [name] | [1 sentence] | [$/effort] | [Low/Med/High] | [Easy/Hard to undo] | [Low/Med/High] | [what has to be true] |
| B — [name] | [...] | | | | | |
| C — [name] | [...] | | | | | |
| Do nothing / defer | [what happens if we wait] | [~$0] | [cost of inaction] | [trivially reversible] | [...] | [...] |

## Recommendation
**Go with [Option X]** because [1-2 sentences tied to the constraints above, not generic praise].

Runner-up [Option Y] loses because [specific reason — cost, risk, or a broken assumption].

## What would change the recommendation
[The condition under which you'd switch to a different option — a budget change, a new constraint, new data]
```

## Quality checklist

- [ ] Are the options different on a real axis (who/how much/what's protected), not the same idea with different UI?
- [ ] Is "do nothing" scored as a real option, not omitted?
- [ ] Does every option have a named assumption that could turn out to be false?
- [ ] Is there an actual recommendation, not just a table left for the reader to interpret?
- [ ] Would a domain expert recognize the cost/risk scores as realistic rather than hand-waved?

## Related skills

- Stress-test the chosen option's failure modes before committing: `pre-mortem`
- Rank options with weighted criteria when more than 3-4 are on the table: `prioritization-matrix`
- Formalize the choice and rationale for stakeholders: `decision-memo`
- Build the financial case for the recommended option: `business-case`
