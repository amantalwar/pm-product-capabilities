---
name: product-market-fit
description: Assess product-market fit with a scored, multi-signal evaluation rather than a gut-feel yes/no. Use when the user asks "do we have PMF," wants to run or interpret a Sean Ellis survey, needs to read retention curves for signs of fit, or asks "are we ready to scale" before pouring money into growth.
---

# Product-Market Fit

## Why this matters

PMF is not a single bit that flips from off to on. Teams that treat it as binary either declare victory the moment
one metric crosses a popular threshold, or wait forever for a certainty that never fully arrives. Treating it
instead as several converging signals — a quantitative survey result, the shape of the retention curve, and
qualitative evidence of pull from customers — lets you say something more useful than "yes" or "no": how much fit
there is, and specifically where the evidence is still weak. That framing also protects against the most common
mistake, which is over-trusting one strong signal (a great survey score from an unrepresentative sample of power
users) while ignoring a contradicting one (a retention curve that's still decaying toward zero).

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **Sean Ellis survey results** if run — % of active users who'd be "very disappointed" without the product
- **Retention/cohort data** if available — even rough numbers are useful
- **Evidence of organic pull** — referrals, inbound interest, unprompted use-case expansion, willingness to pay
  increasing over time
- **Competitive/substitute context** — what users would do instead if this didn't exist
- **Product stage** — pre-launch, early usage, or mature with a real usage history, since this changes how much
  weight each signal deserves

## Process

1. **Run or interpret the Sean Ellis test.** The commonly cited threshold is 40% "very disappointed," but treat it
   as one input, not a certificate — check whether the sample is genuinely active users (not everyone who ever
   signed up) and whether the response count is large enough to trust.
2. **Plot retention by cohort over time.** Look specifically for the curve flattening into an asymptote above zero.
   A curve that keeps decaying toward zero indicates weak fit no matter how good the survey score looks, because it
   means the product isn't holding the users it already won.
3. **Look for qualitative pull** — organic or referral growth without paid acquisition driving it, users applying
   the product to use cases it wasn't designed for, unprompted requests to expand usage, or willingness to pay
   increasing. These are evidence the market is pulling the product forward rather than the team pushing it.
4. **Score each signal independently** rather than blending them into a single gut-feel number too early — a
   survey score, a retention-curve read, and a qualitative-pull read are three different kinds of evidence.
5. **Weight the signals by product stage.** Early-stage products should lean more on survey and qualitative pull
   since retention history is still thin; mature products should weight the retention curve shape heavily since
   there's now enough data for it to be trustworthy.
6. **State the overall read with an explicit weakest-signal flag** — name which of the three signals is thinnest,
   and what evidence would most change the assessment next.

## Output template

```markdown
# Product-Market Fit Assessment: [Product name] — [Date]

## Signal 1: Sean Ellis survey
- % "very disappointed": [X%]  (40% is the commonly cited threshold — treat as a signal, not a verdict)
- Sample: [n, and whether it's genuinely active users]
- Read: [Strong / Mixed / Weak], because [...]

## Signal 2: Retention curve
- Cohort(s) examined: [...]
- Shape: [Flattening above zero / Still decaying / Too early to tell]
- Read: [Strong / Mixed / Weak], because [...]

## Signal 3: Qualitative pull
- Evidence: [organic growth %, referral source, unprompted expansion examples, pricing power]
- Read: [Strong / Mixed / Weak], because [...]

## Overall assessment
[Strong fit / Partial fit / Not yet] — weighted for product stage: [reasoning]

## Weakest signal
[Which of the three is thinnest, and what evidence would most change the read]
```

## Quality checklist

- [ ] No single metric stands in for the whole assessment — all three signal types are addressed
- [ ] The retention curve was checked for flattening over time, not just read as a point-in-time percentage
- [ ] Qualitative pull evidence cites specific instances, not a vague impression of "customers seem happy"
- [ ] The write-up names the weakest signal and what would most change the assessment next

## Related skills

- Design the next experiment if a signal is weak: `product-discovery`
- Ground the assessment in independent customer evidence: `market-research`
- Set the metrics that will track fit going forward: `okrs-metrics`
- Revisit the revenue/segment assumptions if pull is weak: `business-model-canvas`
