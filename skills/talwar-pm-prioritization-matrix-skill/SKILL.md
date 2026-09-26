---
name: talwar-pm-prioritization-matrix-skill
description: Prioritize a list of features, ideas, or backlog items using RICE, MoSCoW, or DVF. Use for "help me rank these," "what should we cut from this release," "score these ideas," or "we have 20 requests and need to pick 5" — even when the user doesn't name a framework, since picking the right one is part of the job.
---

# Prioritization Matrix

## Why this matters

The three common frameworks aren't interchangeable — using the wrong one produces a confident-looking ranking that
answers the wrong question. RICE (Reach, Impact, Confidence, Effort) is built for ranking many comparable items
against each other when you have enough data to estimate the inputs — it answers "which of these many things is
worth doing first." MoSCoW (Must/Should/Could/Won't) is built for scoping a single release or negotiation — it
answers "what's actually in versus out of this specific thing we're shipping," and it works even with rough
judgment rather than hard numbers. DVF (Desirability/Viability/Feasibility) is built for early-stage ideas that don't
have enough evidence yet to support a RICE score — it's a screen for "is this worth investigating further," not a
final ranking. Picking RICE for a scoping conversation produces false precision on numbers nobody can actually
defend; picking MoSCoW for ranking fifty backlog items produces a pile of "Musts" with no ordering inside that pile.

## Gather inputs first

Ask if not given (assume and state it if told to proceed):

- **The actual question**: ranking many items against each other (→ RICE), scoping one release (→ MoSCoW), or
  screening early ideas with thin evidence (→ DVF)
- **The list of items** to prioritize
- **Available data**: usage/traffic numbers (for Reach), past experiment results or benchmarks (for Impact/Confidence),
  engineering estimates (for Effort) — RICE without any of this is just RICE-shaped guessing
- **Constraints**: a hard capacity number, a date, or a "must include X regardless of score" from leadership that
  should be stated up front rather than discovered after the ranking is built

## Process

1. **Pick the framework based on the actual question**, per Why This Matters above, and say which one and why before
   running it — don't silently default to RICE because it looks the most rigorous.
2. **For RICE**: score each item on
   - **Reach** — how many users/customers per time period (a real number or estimate, with unit stated)
   - **Impact** — effect per user when it hits (use a defined scale, e.g. 3=massive, 2=high, 1=medium, 0.5=low,
     0.25=minimal — consistent scale across all items)
   - **Confidence** — how much you trust the Reach/Impact estimates (100%/80%/50% — be honest, don't default to 100%
     just because the number exists)
   - **Effort** — person-time to build (in a consistent unit, e.g. person-months)
   Score = (Reach × Impact × Confidence) / Effort. Rank descending. Flag any score built on a Confidence below 50% as
   needing more evidence before being acted on, not just ranked and shipped.
3. **For MoSCoW**: sort items into Must (release fails without it), Should (important, painful to cut, but release
   survives), Could (nice-to-have, first cut if time runs short), Won't (explicitly out of scope for this release,
   stated so it's a decision, not a silent drop). Cap the Must list against real capacity — if everything is Must,
   the exercise wasn't done.
4. **For DVF**: screen each idea against Desirability (do customers want this — any evidence at all?), Viability
   (does this make business sense — cost, margin, strategic fit), Feasibility (can it actually be built with
   available tech/skills/time). An idea needs a credible yes on all three to advance to real scoping (RICE/MoSCoW);
   a firm no on any one kills it before more analysis is wasted on it.
5. **Show your inputs, not just the output score.** A ranked list with no visible Reach/Impact/Effort numbers (or
   Must/Should reasoning) invites "why is this above that" arguments with no way to resolve them. The scoring
   inputs are the actual deliverable; the sorted list is just a view on them.
6. **Re-run the ranking when a real input changes** (new usage data, a revised effort estimate) — don't treat the
   first pass as permanent just because it's already in a doc.

## Output template

```markdown
# Prioritization: [Release/Backlog/Idea set]

## Framework used and why
[RICE / MoSCoW / DVF — one line on why this framework fits this question]

## RICE (if used)
| Item | Reach | Impact | Confidence | Effort | Score | Notes |
|---|---|---|---|---|---|---|

## MoSCoW (if used)
| Item | Must / Should / Could / Won't | Reasoning |
|---|---|---|

## DVF (if used)
| Idea | Desirability | Viability | Feasibility | Advance? |
|---|---|---|---|---|

## Low-confidence flags
[Items whose score rests on Confidence < 50% or thin evidence — needs validation before acting]

## Final call
[The actual prioritized list/cut line, with capacity or date constraint stated]
```

## Quality checklist

- [ ] The framework choice is stated and justified, not defaulted to whichever looks most rigorous
- [ ] RICE inputs are shown per item, not just the final score
- [ ] MoSCoW's Must list is checked against real capacity, not just optimism
- [ ] Low-confidence estimates are flagged rather than presented with the same certainty as solid data
- [ ] The output ends in an actual decision (a cut line, an order), not just a table

## Related skills

- Screen very early ideas before they reach this stage: `talwar-pm-product-discovery-skill`
- Feed a story map's MVP slice into RICE/MoSCoW for release scoping: `talwar-pm-feature-story-mapping-skill`
- Build the business case behind a high-scoring item: `talwar-pm-business-case-skill`
- Stress-test the top-ranked choice before committing: `talwar-pm-pre-mortem-skill`
