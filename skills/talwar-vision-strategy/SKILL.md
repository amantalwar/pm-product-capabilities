---
name: talwar-vision-strategy
description: Draft or sharpen a product's North Star vision statement and the strategic roadmap that ladders up to it. Use whenever the user wants a vision statement, "where are we headed" narrative, 3-5 year strategic direction, strategic pillars, or the opening framing of a strategy doc — even if they never say the word "vision," e.g. "align the team on our direction," "write the intro for our strategy deck," or "what's our North Star."
---

# Vision & Strategy

## Why this matters

A vision that reads like a mission-statement generator ("be the leading provider of...") doesn't help anyone make a
decision. A good vision is a falsifiable bet about the future: it names who wins, what changes for them, and — by
implication — what the team will NOT do. Treat this skill as writing a decision filter, not a slogan.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if the user wants you to proceed
without asking):

- **Who** this is for (whole company, one product line, one team)
- **Time horizon** (most vision statements target 3-5 years out; okay to confirm)
- **Current state**: what exists today, what's working, what's broken
- **Any existing strategy artifacts** (OKRs, past vision docs, exec statements) to stay consistent with or explicitly
  depart from
- **Constraints**: budget, team size, market realities that a "any vision goes" draft would ignore

## Process

1. **Anchor on the customer change, not the company's ambition.** Ask: "In 3-5 years, what can our customer do that
   they can't do today, and why does that matter to their life or business?" That sentence is the seed of the vision.
2. **Draft the vision statement** — one to two sentences, concrete enough to be wrong. Avoid: "world-class,"
   "seamless," "empower," "leading," "innovative" — these words survive in every draft because they mean nothing and
   commit to nothing. If removing an adjective doesn't change the sentence's truth value, cut it.
3. **Define 3-4 strategic pillars** — the few bets that ladder up to the vision. Each pillar should be something the
   team could organize a roadmap around, not a restatement of the vision in different words.
4. **Name the non-goals.** A vision without an explicit "and therefore we will NOT..." usually isn't a real choice.
   This is often the most valuable paragraph in the doc because it's the part stakeholders will push back on — which
   means it's doing its job.
5. **Stress-test it**: could a competitor's vision statement be identical to this one with the company name swapped?
   If yes, it's not specific enough — go back to step 1.

## Output template

Use this structure unless the user's context clearly calls for something shorter (e.g. a one-slide version):

```markdown
# [Product/Org] Vision & Strategy

## Vision statement
[1-2 sentences: the customer change we're betting on]

## Why now
[2-4 sentences: what's true today that makes this the right bet — market shift, technology inflection, customer
behavior change. This is what makes the vision falsifiable rather than aspirational.]

## Strategic pillars
1. **[Pillar name]** — [1-2 sentences: what this pillar means in practice]
2. **[Pillar name]** — [...]
3. **[Pillar name]** — [...]

## What this means we will NOT do
- [Explicit non-goal and the tradeoff it protects]
- [...]

## How we'll know it's working
[2-3 leading indicators — not vanity metrics — that would show the bet is paying off before the lagging outcome
metrics move. Link to [[okrs-metrics]] if the user wants full OKRs built from this.]
```

## Quality checklist before you hand it back

- [ ] Could you delete the company name and have a reader still not mistake this for a competitor's vision?
- [ ] Does at least one sentence name something the team will stop doing or deliberately not pursue?
- [ ] Is "why now" grounded in something observable (a number, a trend, a customer quote) rather than asserted?
- [ ] Would a skeptical exec reading this be able to argue with a specific claim — i.e., is it falsifiable?

## Related skills

- Turn the pillars into measurable targets: `talwar-okrs-metrics`
- Sequence the pillars into a time-boxed roadmap: `talwar-roadmapping`
- Justify the investment behind a pillar: `talwar-business-case`
