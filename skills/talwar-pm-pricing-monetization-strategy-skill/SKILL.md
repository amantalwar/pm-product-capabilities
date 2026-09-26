---
name: talwar-pm-pricing-monetization-strategy-skill
description: Design or rework pricing, packaging, and monetization strategy. Use for "how should we price this," "what should our tiers look like," "are we leaving money on the table," or "should this feature be gated" — even when phrased as a packaging question like "what goes in the free plan" rather than an explicit pricing request.
---

# Pricing & Monetization Strategy

## Why this matters

The most common pricing mistake is pricing from the inside out: start from cost structure ("this feature costs us $X
to run, so charge $X plus margin") or from what a competitor charges, and never actually ask what the customer
believes the outcome is worth to them. Cost-plus tells you the floor below which you lose money; it says nothing
about the ceiling. Competitor-based pricing anchors you to someone else's strategy, which may itself be wrong.
Value-based pricing — starting from the economic or emotional outcome the customer gets — is harder to research but
is the only one of the three that scales with what you actually deserve to capture. Packaging (what's in which tier)
is a second, separate decision: it's about segmenting customers by willingness to pay and use pattern, not about
where features happened to land in the build order.

## Gather inputs first

Ask if not given (assume and state it if told to proceed):

- **What's being priced**: new product, new tier, a feature being gated, or a full repricing
- **Cost basis**, if relevant (so a floor can be set), but treat this as a constraint, not the anchor
- **Competitor pricing** for comparable offerings, as one input among several — not the starting point
- **Customer segments** and any existing signal on willingness to pay (deal data, past price-sensitivity feedback,
  win/loss notes citing price)
- **Willingness-to-pay research available or feasible** — Van Westendorp survey data, conjoint studies, or whether
  one needs to be run before committing to a number
- **Business model constraints**: margin targets, sales motion (self-serve vs. sales-led), existing customer
  contracts that a repricing would need to grandfather

## Process

1. **Quantify the value delivered before naming a number.** For B2B, this is usually a hard economic outcome (hours
   saved × loaded cost, revenue enabled, risk avoided). For B2C, it's often a willingness-to-pay range from direct
   research. Either way, this becomes the ceiling reference — pricing should capture some fraction of the value
   created, not just cover the cost of creating it.
2. **Run or reference Van Westendorp (or equivalent WTP research)** when there's no existing price point to anchor
   to: ask "too cheap to trust," "a bargain," "getting expensive," and "too expensive" price points across a sample,
   and use the range between the intersection points as the viable pricing band — not a single number pulled from
   internal debate.
3. **Choose a pricing model** — flat, per-seat, usage-based, tiered-with-overage — based on what metric correlates
   with the value the customer gets, not what's easiest to bill. Usage-based pricing that doesn't track value (e.g.
   billing on a metric the customer can't predict or control) creates resentment even when the average revenue is
   fine.
4. **Design packaging around segments, not feature inventory.** Each tier should target a specific buyer with a
   specific use case and willingness to pay — not just be "free tier minus some stuff, paid tier plus some stuff."
   Ask: what does each segment need to say yes, and what would make them upgrade naturally as their usage grows.
5. **Sanity-check against cost and competitors last, as guardrails, not inputs.** Confirm the floor covers cost with
   target margin, and that the position relative to competitors is intentional (premium, parity, or aggressive) —
   not accidental.
6. **Plan the migration** for existing customers before finalizing: grandfathering, notice period, and how the
   change will be communicated — a pricing change that surprises existing customers creates churn risk independent
   of whether the new price is fair.

## Output template

```markdown
# Pricing & Monetization: [Product/Feature]

## Value basis
[Quantified value delivered per segment — economic outcome or WTP research summary]

## Willingness-to-pay research
[Van Westendorp results or equivalent: too cheap / bargain / expensive / too expensive price points, and the
resulting acceptable range. Note if this is pending and what's assumed in the meantime.]

## Pricing model
[Flat / per-seat / usage-based / hybrid] — why this metric tracks value for this customer

## Packaging
| Tier | Target segment | What's included | Price | Why they'd upgrade from the tier below |
|---|---|---|---|---|

## Guardrails checked
- Cost floor / target margin: [...]
- Competitor position (premium/parity/aggressive) — intentional, not accidental: [...]

## Migration plan for existing customers
[Grandfathering approach, notice period, communication plan]

## Risks & open questions
[What's unvalidated — e.g. WTP research still needed, model untested at scale]
```

## Quality checklist

- [ ] The starting point was customer-perceived value or WTP data, not internal cost structure or a competitor's price
- [ ] Packaging tiers map to distinct buyer segments, not just a feature list split in two
- [ ] The billing metric correlates with value the customer experiences, not just what's easy to meter
- [ ] Existing-customer migration is addressed, not left as an afterthought
- [ ] Cost and competitor pricing appear only as guardrails, explicitly labeled as such

## Related skills

- Get WTP signal from real customers first: `talwar-pm-market-research-skill`
- Apply anchoring/framing to how tiers are presented: `talwar-pm-behavioral-science-economics-skill`
- Sequence a pricing change into launch communication: `talwar-pm-go-to-market-skill`
- Build the financial case for a repricing: `talwar-pm-business-case-skill`
