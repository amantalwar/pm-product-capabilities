---
name: talwar-pm-okrs-metrics-skill
description: Draft or grade Objectives and Key Results (OKRs) and the success metrics behind them. Use when the user wants quarterly or annual goals written, needs to grade/score existing OKRs, asks "how do we measure success on this," or hands you a list of tasks and says "turn this into OKRs" — even if they call it "goals," "targets," or "our north star metrics" instead of the word OKR.
---

# OKRs & Metrics

## Why this matters

The most common OKR failure isn't a bad objective — it's a Key Result that's secretly a to-do item. "Ship the new
onboarding flow" is a task: it can be marked done regardless of whether it changed anything for the customer or the
business. "Increase activation rate from 42% to 55%" is an outcome: it can only be true if something actually moved.
The test is simple — if a KR could be checked off by an engineer closing a ticket, it's an output; rewrite it as the
change that ticket was supposed to cause. Objectives, by contrast, should NOT be measurable on their own — they're
qualitative and inspiring ("Make onboarding a reason people recommend us"), because their job is to give the KRs a
reason to exist, not to duplicate them.

Grading conventions also carry meaning that's easy to lose. A 0.7 on a Google-style 0.0-1.0 scale is a good result
for an aspirational/moonshot OKR — hitting 1.0 every quarter is itself a signal the team is sandbagging, setting
targets they were already confident they'd clear. A committed OKR (tied to a customer promise, a compliance deadline,
a dependency another team is blocked on) should be graded on a stricter pass/fail basis instead. Decide which kind of
OKR you're writing before you set the target, because it changes what "success" should mean.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **Time horizon** (quarter is standard; confirm if annual or half)
- **Scope** (company, org, team) and how it ladders to existing strategy pillars (see `talwar-pm-vision-strategy-skill`)
- **Baseline data** for any metric being targeted — you cannot set a credible target without knowing the starting point
- **Committed vs aspirational** intent for this cycle, if known
- **Existing OKRs or metrics** from the prior cycle, to check continuity or deliberate departure

## Process

1. **Write the objective** — one sentence, qualitative, inspiring, time-bound, and traceable to a strategic pillar.
   It should NOT contain a number.
2. **Draft candidate KRs.** For each one, ask: "Could this be a task on a sprint board?" If yes, rewrite it as the
   outcome that task was meant to produce. "Launch feature X" becomes "X% of eligible users adopt within 30 days."
3. **Limit to 3-5 KRs per objective.** More than that dilutes focus and usually means two objectives got merged.
4. **Attach a baseline and target to every KR** — no KR is complete without both numbers.
5. **Label each OKR committed or aspirational**, and pick the grading convention accordingly: 0.0-1.0 scale for
   aspirational (0.7 = good), red/yellow/green or pass/fail for committed.
6. **Score initial confidence** (not a grade — a gut-check at planning time) so you can track whether confidence
   tracked reality by the end of the cycle.
7. **Set a check-in cadence** (usually bi-weekly or monthly) before the cycle starts, not reactively when something
   slips.
8. **Stress-test**: could every KR hit 100% and the objective still feel unachieved? If yes, a KR is missing or
   wrong — go back to step 2.

## Output template

```markdown
# [Team/Org] OKRs — [Quarter/Year]

## Objective 1: [Qualitative, inspiring statement — no numbers]
Type: [Committed | Aspirational]  |  Ladders to: [strategic pillar / company OKR]

| Key Result | Baseline | Target | Current | Owner | Confidence (1-10) |
|---|---|---|---|---|---|
| KR1: [measurable outcome, not a task] | | | | | |
| KR2: [...] | | | | | |
| KR3: [...] | | | | | |

## Objective 2: [...]
[repeat structure]

## Grading convention
[State the scale used: 0.0-1.0 (0.7 = success for aspirational) or R/Y/G / pass-fail for committed, and why.]

## Check-in cadence
[Frequency, format, who reviews]
```

## Quality checklist

- [ ] No Key Result could be marked "done" by closing a single ticket — each is an outcome, not a task
- [ ] Every KR has both a baseline and a numeric target
- [ ] Each OKR is explicitly labeled committed or aspirational, with a matching grading scale
- [ ] Hitting every KR at 100% would genuinely satisfy the objective — not just check boxes near it
- [ ] Confidence was scored at planning time, not backfilled after results came in

## Related skills

- Ladder objectives from strategic pillars: `talwar-pm-vision-strategy-skill`
- Sequence the initiatives that will move the KRs: `talwar-pm-roadmapping-skill`
- Decide which initiatives to fund against these targets: `talwar-pm-prioritization-matrix-skill`
- Report progress against these OKRs to stakeholders: `talwar-pm-stakeholder-communication-skill`
