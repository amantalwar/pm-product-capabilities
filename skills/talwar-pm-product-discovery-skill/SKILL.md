---
name: talwar-pm-product-discovery-skill
description: Design a lightweight discovery experiment to validate an idea before committing engineering time to it. Use when the user wants to "test an idea before building it," de-risk a feature, asks "how do we validate this without writing code," or needs a fake-door, concierge, Wizard of Oz, or prototype test designed. Distinct from delivery — this is about knowing before building, not shipping.
---

# Product Discovery

## Why this matters

Marty Cagan's discovery/delivery split exists because the two activities de-risk different things and cost wildly
different amounts. Discovery's job is to de-risk value (will anyone actually want this), usability (can they figure
out how to use it), feasibility (can it be built with what the team has), and business viability (does it work for
the business) — all *before* delivery spends weeks turning a guess into shipped code. Skip discovery and the team
still discovers these risks; they just discover them the expensive way, after the code is written, the sprint is
spent, and reversing course means throwing away real work instead of a afternoon's worth of a fake landing page.

The skill in designing an experiment isn't making it convincing — it's making it cheap. The right experiment is the
smallest, fastest one that could actually change the team's decision, sized to the risk being tested: a reversible,
low-stakes idea deserves a quick fake-door test, while an idea that would trigger a large, hard-to-unwind commitment
(a pricing change, a platform bet) deserves a slower, more rigorous test even if it costs more, because being wrong
at that scale costs far more than the test does.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **The idea or hypothesis** being tested
- **Which risk is most in question** — value, usability, feasibility, or business viability (usually value risk
  matters most to test first)
- **Existing conviction level** — a well-established pattern needs a lighter test than a total unknown
- **Timeline pressure** and what's realistically testable in that window
- **What decision the result will actually change** — if nothing changes regardless of outcome, this isn't worth
  running

## Process

1. **State the hypothesis** as if/then/because: "If we [do X], then [Y happens], because [Z]."
2. **Identify the dominant risk type.** Most ideas fail on value risk (nobody wants it) before they ever reach
   usability or feasibility risk, so test value first unless there's a specific reason feasibility is the real
   unknown.
3. **Choose the smallest experiment that could falsify the hypothesis**:
   - *Fake door* — measure click-through/signup demand for something that doesn't exist yet
   - *Concierge* — manually deliver the service to a handful of real users, no automation
   - *Wizard of Oz* — a real-looking UI backed by a human doing the work behind the scenes
   - *Prototype test* — a clickable mock with no working backend, watched or measured
4. **Size the experiment to the risk.** Higher cost of being wrong, or a decision that's expensive to reverse later,
   justifies a bigger sample or longer run; a cheap, reversible bet doesn't need much rigor to greenlight.
5. **Set the success/kill threshold before running it** — deciding what counts as validated after seeing the
   results is how teams talk themselves into shipping things the data didn't actually support.
6. **Define what happens on each outcome** — proceed to build, iterate and re-test, or kill — so the experiment
   produces a decision, not just a data point nobody acts on.

## Output template

```markdown
# Discovery Experiment: [Idea name]

## Hypothesis
If we [do X], then [Y happens], because [Z].

## Risk being tested
[Value | Usability | Feasibility | Business viability] — and why this is the dominant risk right now

## Experiment design
- Type: [Fake door | Concierge | Wizard of Oz | Prototype test]
- What we'll actually do: [...]
- Who it's run with: [sample/segment]
- Duration: [...]

## Success threshold (set before running)
[The specific number or observation that would count as validated — decided now, not after seeing results]

## Decision per outcome
- If validated: [proceed to build / expand test]
- If inconclusive: [iterate how, or re-test]
- If invalidated: [what gets killed or rethought]
```

## Quality checklist

- [ ] The success threshold was written before the experiment ran, not fitted to the results afterward
- [ ] The experiment type matches the risk actually being tested, not just the easiest one to build
- [ ] There's a stated decision for a failed/invalidated result, not only a plan for success
- [ ] The experiment is genuinely cheaper and faster than building the real thing

## Related skills

- Stress-test the idea for failure modes before or alongside the experiment: `talwar-pm-pre-mortem-skill`
- Decide which validated ideas get built first: `talwar-pm-prioritization-matrix-skill`
- Read PMF-level signals once an idea is live with real usage: `talwar-pm-product-market-fit-skill`
- Generate alternative approaches if the first hypothesis fails: `talwar-pm-solution-options-generator-skill`
