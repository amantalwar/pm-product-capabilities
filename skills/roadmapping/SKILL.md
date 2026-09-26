---
name: roadmapping
description: Build a Now/Next/Later outcome-based product roadmap. Use when the user asks for "a roadmap," wants to replace a date-and-feature roadmap with something more honest, needs to align stakeholders on priorities across a quarter or year, or says "what are we building next" or "lay out the plan for the next two quarters."
---

# Roadmapping

## Why this matters

A date-and-feature roadmap ("Search redesign — Q3," "Mobile app — Q4") reads as precise, which is exactly the
problem: it presents a guess as a commitment. The date implies certainty about effort the team hasn't validated yet,
and the feature name implies the solution is already decided before discovery has happened. When reality changes —
and it always does — the team either ships the wrong thing on time to protect the roadmap, or misses the date and
burns trust, and either way the roadmap taught stakeholders to expect promises the team can't actually keep.

An outcome-based Now/Next/Later roadmap fixes this by communicating confidence honestly instead of hiding it behind
false precision. "Now" items are committed because they're already validated and in motion. "Later" items are
directional because that's genuinely all that's known about them yet. Organizing by outcome rather than feature also
keeps the solution space open — the team can change how it solves a problem without having to renegotiate the
roadmap, because the roadmap was never promising a specific solution in the first place.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **Strategic pillars or OKRs** this roadmap should ladder from (see `vision-strategy`, `okrs-metrics`)
- **Current initiatives in flight** and their real status
- **Constraints**: team capacity, known dependencies, hard external deadlines (compliance, partner commitments)
- **Audience**: exec/board (needs less detail, more confidence framing) vs. the team itself (needs more nuance)
- **Time span** "Later" should reasonably cover — usually no more than 2-3 quarters out before it's just noise

## Process

1. **List candidate items as outcomes or problems**, not features. "Reduce checkout abandonment" not "Add
   one-click checkout" — the solution stays open until the team is actually building it.
2. **Bucket into Now / Next / Later**:
   - *Now*: committed, in progress or about to start, solution largely known
   - *Next*: validated and prioritized, not yet started, solution still being shaped
   - *Later*: directionally likely given current strategy, genuinely uncertain on timing or approach
3. **State confidence explicitly per bucket** rather than letting the bucket imply it silently — Now is high
   confidence, Later is low, and stakeholders should see that stated, not have to infer it.
4. **Link every item to the pillar or OKR it serves.** An item that can't be linked is either mis-scoped or
   shouldn't be on the roadmap.
5. **Avoid calendar dates beyond the Now bucket.** If a stakeholder pushes for a date on a Next/Later item, give a
   quarter-level range with an explicit "this could move" caveat rather than a specific day.
6. **Name the signal that would move an item between buckets** — what needs to be true (a discovery result, a
   dependency clearing, capacity freeing up) for Later to become Next.
7. **Set a review cadence** (monthly is typical) to actually re-bucket items — a Now/Next/Later roadmap that never
   gets revisited decays into the same false-certainty problem it was meant to solve.

## Output template

```markdown
# [Product/Team] Roadmap — [Date last updated]

## Now (committed, in progress)
| Outcome | Why it matters / pillar link | Confidence | Owner |
|---|---|---|---|
| [Outcome, not a feature name] | | High | |

## Next (validated, prioritized, not started)
| Outcome | Why it matters / pillar link | Confidence | Signal that would change this |
|---|---|---|---|
| | | Medium | [what needs to be true to promote or drop this] |

## Later (directional)
| Outcome | Why it matters / pillar link | Confidence | Signal that would change this |
|---|---|---|---|
| | | Low | |

## Explicitly not on this roadmap
[Optional: items stakeholders might expect to see, and why they aren't here — link `scope-definition` if useful]

## Review cadence
[How often this gets re-bucketed, and by whom]
```

## Quality checklist

- [ ] No row describes a feature/solution instead of an outcome or problem
- [ ] No date appears beyond the Now bucket without an explicit "this could move" caveat
- [ ] Every item traces to a named strategic pillar or OKR
- [ ] Confidence level is stated per item, not left for the reader to guess from the bucket name
- [ ] A review cadence is specified so the roadmap doesn't calcify into the same false certainty it replaced

## Related skills

- Ladder roadmap items from the strategy that justifies them: `vision-strategy`
- Set the measurable targets each outcome is meant to move: `okrs-metrics`
- Decide which candidate outcomes get funded first: `prioritization-matrix`
- Communicate roadmap changes to stakeholders: `stakeholder-communication`
