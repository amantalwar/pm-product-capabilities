---
name: technical-debt-prioritization
description: Translate technical debt into business terms (velocity drag, incident risk, security exposure, onboarding cost) and rank it against feature work on comparable units. Use when engineering wants budget or roadmap time for debt paydown, a PM needs to defend a "boring" infrastructure item against flashy feature asks, or the user says "how do we convince leadership this refactor matters" or "help me prioritize our debt backlog."
---

# Technical Debt Prioritization

## Why this matters

"It's messy" and "we should really fix this" lose every roadmap argument against a feature with a customer name
attached to it, not because debt doesn't matter but because it's being pitched in a currency leadership can't
spend — engineering aesthetics instead of business risk. The fix is translation, not advocacy: every piece of debt
has a business cost even when no one has priced it yet, and the job is to make that cost legible in the same units
used to justify feature work — money, time, risk. "This module is a mess" becomes "this module causes an average of
2 extra engineer-days per feature touching it, and it's touched by 40% of our roadmap this quarter" — a sentence
a non-engineer can weigh against a feature's revenue case. Once debt is priced, it can be ranked against features on
one list instead of living in a separate, perpetually-deprioritized backlog that only gets attention after an
incident forces the issue. The scoring doesn't need to be precise to be useful — it needs to be consistent and
defensible enough that a debt item and a feature request can be compared without one side having a structural home-
field advantage.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **The debt inventory** — specific items (a module, a dependency, a missing test suite, a manual process), not a
  vague "our codebase has debt"
- **Who's affected** — which teams/features touch this code or process, and how often
- **Any incident or support history** tied to the debt item (postmortems, support ticket volume, on-call pages)
- **The comparison set** — the feature backlog or roadmap this debt needs to be ranked against, and who makes the
  final tradeoff call

## Process

1. **Name each debt item concretely**, scoped to something fixable — "the auth service" is too broad to price or
   schedule; "the auth service's token refresh has no test coverage and has caused 3 P1 incidents this year" is
   scoped enough to act on.
2. **Translate to business-risk categories.** For each item, estimate:
   - **Velocity drag** — extra engineer-time this debt adds to work that touches it (a rough multiplier or
     days/month is fine; cite the basis)
   - **Incident risk** — frequency and severity of past incidents traceable to this item, or a reasoned estimate if
     none have happened yet
   - **Security exposure** — whether this item is a known or plausible vector, and what's exposed if exploited
   - **Hiring/onboarding cost** — extra ramp time this debt adds for new engineers touching this area
3. **Convert to a comparable score.** A workable default: estimate a rough dollar or engineer-time cost per quarter
   for each category, sum them, and treat that as the "cost of not fixing this" — the same unit a feature's
   business case uses for its upside. State assumptions plainly; a defensible rough number beats a precise-looking
   but fabricated one.
4. **Rank debt items against feature work on that shared basis** — cost-of-inaction for debt versus expected value
   for features, both roughly denominated in engineer-time or dollars per quarter. This is what makes "fund the
   auth refactor over feature Y" a comparison instead of a plea.
5. **Distinguish "fix now" from "fix eventually" from "accept and monitor."** Not all debt clears the bar for
   immediate paydown — some belongs on a watch list with a named trigger (e.g., "revisit if incident count doubles")
   rather than competing for this quarter's capacity.
6. **Pair every "fix now" item with a plan a non-engineer can approve** — scope, cost, and what specifically
   improves (not "cleaner code," but "reduces P1 incidents in this area from 3/quarter to near-zero").

## Output template

```markdown
# Technical Debt Prioritization

## Debt inventory

| Item | Scope | Velocity drag (eng-days/qtr) | Incident risk (history + severity) | Security exposure | Onboarding cost | Est. cost of inaction (per qtr) |
|---|---|---|---|---|---|---|
| | | | | | | |
| | | | | | | |

## Ranked against feature backlog

| Item (debt or feature) | Type | Est. value / cost-of-inaction (per qtr) | Cost to address | Recommendation |
|---|---|---|---|---|
| | Debt | | | Fix now / Fix next quarter / Monitor |
| | Feature | | | |

## Fix-now plan
| Item | Scope of fix | Cost | Concrete improvement (measurable) | Owner |
|---|---|---|---|---|
| | | | | |

## Monitor list (not funded this cycle)
| Item | Trigger that would escalate it |
|---|---|
| | |
```

## Quality checklist

- [ ] Is every debt item scoped concretely, not a vague "the codebase is messy" umbrella?
- [ ] Is the cost expressed in business terms (eng-time, incidents, dollars) with a stated basis, not just asserted severity?
- [ ] Are debt items ranked against features on the same unit, not living in a separate never-funded list?
- [ ] Does every "fix now" item name a measurable improvement a non-engineer could verify later?
- [ ] Are lower-priority items given a named monitoring trigger rather than silently dropped?

## Related skills

- Use the ranked list to allocate quarterly capacity across debt and features: `portfolio-investment-allocation`
- Document the as-is architecture this debt lives in before scoping the fix: `state-documentation`
- Rank debt items against each other with a lighter-weight matrix: `prioritization-matrix`
- Stress-test what happens if the highest-risk item isn't funded: `pre-mortem`
