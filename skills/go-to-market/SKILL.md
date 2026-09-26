---
name: go-to-market
description: Define GTM strategy — positioning, channel choice, and launch tiering — for a product or feature. Use for "how should we position this," "what channels should we use to launch," "write our positioning statement," or "what tier of launch does this deserve" — the strategy layer, as distinct from the full launch execution plan (see `go-to-market-launch` for the multi-step orchestration).
---

# Go-to-Market Strategy

## Why this matters

GTM failures are rarely a channel problem — they're a positioning problem wearing a channel costume. If the
positioning doesn't name a specific alternative the buyer is currently using and a specific reason to switch, no
channel mix fixes that; the message just fails faster or slower depending on the channel. Get positioning right first
and channel selection becomes mostly mechanical (go where the target buyer already looks for solutions to this
problem). Launch tiering matters for a different reason: not every release deserves a full launch motion, and
over-launching small changes trains your audience to tune out the next announcement, while under-launching a real
step-change wastes the moment when switching costs for the buyer are lowest.

## Gather inputs first

Ask if not given (assume and state it if told to proceed):

- **What's launching**: new product, new feature, repositioning of something existing
- **Target buyer/segment** for this specific launch (may differ from the overall ICP)
- **Named alternative** they use today (a competitor, a workaround, or "nothing/manual process")
- **Differentiator** — the specific, defensible reason this wins for that buyer against that alternative
- **Constraints**: launch date pressure, sales team readiness, support readiness, existing channel investments
- **Signal on scale of the change**: is this a step-change for the target segment or an incremental improvement —
  this drives the tiering call in step 4

## Process

1. **Write the positioning statement in the standard structural form**, then stress-test each slot:
   *For [target] who [need], [product] is a [category] that [benefit]. Unlike [alternative], we [differentiator].*
   The "unlike" clause is the one teams skip or soften — without a named alternative, the statement is just a
   description, not a positioning claim.
2. **Validate the differentiator is actually defensible**, not just true today. Ask: could the named alternative
   close this gap in one release? If yes, the differentiator is a feature lead, not a position — note that
   explicitly rather than overselling its durability.
3. **Select channels by where the target buyer already looks for this category of solution**, not by which channels
   the team has used before. A channel choice inherited from the last launch is a habit, not a strategy.
4. **Tier the launch deliberately**:
   - **Major** — step-change for the segment, coordinated across sales/support/marketing/press, dedicated assets
   - **Minor** — meaningful improvement, in-app + changelog + lightweight external note, no full press motion
   - **Silent** — ships without announcement (internal tooling, incremental fix, or a change you're deliberately not
     drawing attention to, e.g. a competitive response still being finalized)
   Match the tier to the actual size of the change for the target buyer, not to internal enthusiasm about the work.
5. **Define what "working" looks like before launch**, not after — the adoption/activation metric this GTM motion is
   supposed to move, so the retro has something concrete to check against.
6. **Hand off to execution.** This skill produces the strategy; sequencing the actual launch checklist, asset list,
   and cross-team timeline is `go-to-market-launch`.

## Output template

```markdown
# GTM Strategy: [Product/Feature]

## Positioning statement
For [target] who [need], [product] is a [category] that [benefit].
Unlike [named alternative], we [differentiator].

## Differentiator durability check
[Is this defensible for 2+ competitor release cycles, or a feature lead that will close? State plainly.]

## Target buyer for this launch
[Segment — may be narrower than overall ICP]

## Channels
| Channel | Why the buyer is already there | Owner |
|---|---|---|

## Launch tier: [Major / Minor / Silent]
Reasoning: [why this tier matches the actual scale of change for this buyer]

## Success metric
[The one adoption/activation number this motion should move, with a target and timeframe]

## Handoff
Execution plan (asset list, cross-team timeline, checklist): see `go-to-market-launch`
```

## Quality checklist

- [ ] The positioning statement names a real, specific alternative — not "the status quo" or left blank
- [ ] The differentiator has an explicit durability call (defensible vs. feature-lead), not just asserted as unique
- [ ] Channel choices are justified by buyer behavior, not by "what we did last time"
- [ ] The launch tier decision states the reasoning, not just the label
- [ ] A specific success metric with a target exists before launch, not defined retroactively

## Related skills

- Execute the full multi-step launch plan from this strategy: `go-to-market-launch`
- Validate the differentiator against real competitive data first: `market-research`
- Get the pricing/packaging locked before channel messaging: `pricing-monetization-strategy`
- Brief stakeholders on the plan: `stakeholder-communication`
