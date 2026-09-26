---
name: portfolio-investment-allocation
description: Allocate budget or headcount across a portfolio of initiatives using a common comparison basis, instead of funding whichever team argued loudest. Use when the user is planning annual/quarterly investment across multiple products or teams, asks "how should we split the budget," wants a run/grow/transform breakdown, or needs to compare initiatives from different business units that don't share the same metrics.
---

# Portfolio Investment Allocation

## Why this matters

Single-initiative prioritization (ICE, RICE, a 2x2) breaks down at the portfolio level because the initiatives being
compared often don't share units — a platform reliability project measured in incident-hours avoided sits next to a
new-market bet measured in projected revenue, next to a compliance requirement with no upside at all, just a
deadline. Without a common basis, allocation decisions collapse into whichever team tells the most compelling story
or has the most senior sponsor in the room — funding follows volume, not expected value. Two disciplines fix this.
First, bucket-level allocation (run the business / grow the business / transform the business, often shorthanded
70/20/10) forces an explicit, defensible split of the whole budget before any single initiative is discussed, so
"keep the lights on" work isn't silently crowded out by the newest exciting bet, and moonshots aren't silently
starved because every dollar went to safe, incremental grow-bucket work. Second, within each bucket, initiatives get
scored on a normalized common basis — typically some form of risk-adjusted expected value versus cost — so a
platform team's incident-reduction case and a growth team's revenue case can be ranked against each other honestly,
even though their native metrics don't match.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **Total budget/headcount envelope** being allocated and the time period it covers
- **The list of candidate initiatives**, ideally already scoped enough to estimate cost, with which business unit
  or team owns each
- **Bucket definitions** if the org already has a run/grow/transform (or equivalent) split defined — don't invent a
  new taxonomy if one exists
- **How each initiative's value is currently expressed** — revenue, cost avoidance, risk reduction, compliance
  requirement — since this is exactly what needs normalizing
- **Any non-negotiables** — compliance deadlines, contractual commitments — that are funded before the ranking
  exercise, not as part of it

## Process

1. **Set the bucket split before ranking anything inside it.** Default framing: run (keep current product/business
   operating — maintenance, support, compliance), grow (extend what's working — expansion, optimization), transform
   (new bets — new markets, new product lines). A common starting ratio is roughly 70/20/10, but the right split is
   whatever the business's stage and risk appetite justify — state the reasoning, don't just cite the ratio.
2. **Pull out non-negotiables first.** Regulatory deadlines and contractual commitments get funded outside the
   ranking — including them in a "compare expected value" exercise treats a legal requirement as optional, which
   it isn't.
3. **Normalize value to a common basis** before comparing across business units. A workable default: expected value
   (probability-weighted upside, in dollars or a dollar-equivalent proxy) divided by cost, with a risk adjustment
   for confidence in the estimate. State the proxy explicitly when using one (e.g., "1 incident-hour avoided ≈ $X in
   support cost + reputational risk") so the comparison is inspectable, not hidden inside a black-box score.
4. **Rank within each bucket on the normalized basis**, not across buckets — a run-bucket reliability fix and a
   transform-bucket new-market bet are answering different questions and shouldn't be forced onto one ranked list.
5. **Name the loudest-team problem explicitly if it's present.** If an initiative's case rests mainly on sponsor
   seniority or the team's track record of asking rather than on its own expected value, flag it — that's a signal
   the estimate needs more rigor, not a reason to fund it as-is.
6. **Show what got cut and why**, not just what got funded. The rejected list, with its reasoning, is what makes the
   allocation defensible later when someone asks why their initiative didn't make it.

## Output template

```markdown
# Portfolio Investment Allocation: [Period]

## Total envelope
[Budget/headcount] over [period]

## Bucket split
| Bucket | % of envelope | $ / headcount | Rationale |
|---|---|---|---|
| Run | | | |
| Grow | | | |
| Transform | | | |

## Non-negotiables (funded outside ranking)
| Initiative | Owner | Cost | Why non-negotiable |
|---|---|---|---|
| | | | |

## Ranked initiatives by bucket

### [Bucket name]
| Initiative | Owner/BU | Cost | Expected value (normalized) | Confidence | EV/Cost | Funded? |
|---|---|---|---|---|---|---|
| | | | | | | |

## Cut or deferred
| Initiative | Owner/BU | Why it didn't make the cut |
|---|---|---|

## Flags
[Any initiative whose case leans on sponsor seniority/volume rather than a defensible expected-value estimate]
```

## Quality checklist

- [ ] Was the bucket split (run/grow/transform or equivalent) set before initiatives were ranked, not derived from the ranking?
- [ ] Is value expressed on one normalized basis across business units, with any proxy conversion stated explicitly?
- [ ] Are non-negotiables (compliance, contracts) funded outside the ranking rather than competing on expected value?
- [ ] Does the output show what was cut and why, not just the funded list?
- [ ] Is any initiative whose case rests mainly on sponsor volume/seniority flagged rather than silently funded?

## Related skills

- Build the underlying business case for a transform-bucket bet: `business-case`
- Rank initiatives inside one bucket with a lighter-weight method: `prioritization-matrix`
- Stress-test a large transform bet before committing budget: `pre-mortem`
- Turn the funded list into a sequenced roadmap: `roadmapping`
