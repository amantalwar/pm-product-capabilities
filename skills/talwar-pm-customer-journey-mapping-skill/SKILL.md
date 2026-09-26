---
name: talwar-pm-customer-journey-mapping-skill
description: Map the end-to-end customer experience across stages, touchpoints, emotions, and pain points. Use for "map out the customer journey," "where are we losing people," "walk through the experience from signup to renewal," or when a discussion about a specific pain point needs to be placed in the context of the whole experience — even if the user just describes a funnel or a single bad moment.
---

# Customer Journey Mapping

## Why this matters

A journey map is only as good as what it's built from. The failure mode is a room of internal stakeholders drawing
boxes and guessing how customers feel at each stage — "users probably feel confused here" — and shipping that as if
it were research. A map built entirely from internal assumptions is close to worthless: it mostly reflects what the
team already believes, which is exactly the thing a journey map is supposed to test. The map's job is to make the
customer's actual experience visible, including the parts that contradict the internal narrative. That only works if
real customer data — interview quotes, support transcripts, session recordings, survey verbatims — sits underneath
each stage, and the map is honest about which parts have that evidence and which are still guesses.

## Gather inputs first

Ask if not given (assume and state it if told to proceed without asking):

- **Which journey**: a specific flow (onboarding, upgrade, churn/win-back) or the full lifecycle
- **Persona/segment**: journeys differ by user type; a map that tries to cover everyone usually describes no one
- **Evidence available**: interview transcripts, support tickets, NPS verbatims, session recordings, sales call
  notes, churn survey responses — the more of this exists, the less the map has to rely on assumption
- **Existing data on drop-off points**: funnel analytics, support ticket volume by stage, churn timing — quantitative
  signal for where to focus qualitative attention
- **Purpose**: is this diagnosing a known problem, or exploratory groundwork before a discovery effort

## Process

1. **Define the stages first, in the customer's language, not the org chart's.** Stages should describe what the
   customer is trying to accomplish (e.g. "deciding whether to trust this tool with real data"), not internal phases
   like "Activation" that mean something to PM but nothing to the user.
2. **For each stage, fill four rows**: touchpoints (what they interact with), actions (what they actually do),
   thoughts/emotions (what's going through their mind — pulled from real quotes wherever possible), and pain points
   (where the experience breaks down).
3. **Attach evidence to every claim about thoughts or emotions.** A row that says "frustrated — 'I had to re-enter
   my card three times' (support ticket #4021, March)" is usable. A row that just says "frustrated" with nothing
   behind it is a guess wearing the format of a finding.
4. **Explicitly tag each cell as Evidence or Assumption.** Where there's no data yet, say so plainly rather than
   filling the cell with a plausible-sounding sentence — an honest blank is more useful than false confidence, and it
   tells you exactly where to send the next research effort.
5. **Find the moments of truth** — the 1-3 points where the experience disproportionately determines whether the
   customer stays, upgrades, or churns. These are usually where emotion is highest and evidence is richest (heavy
   support volume, strong verbatims either way), not necessarily where the org has historically focused.
6. **Connect pain points to owners and to already-known data**, e.g. link a stage's drop-off to the analytics number
   that shows it, so the map argues with numbers, not just narrative.

## Output template

```markdown
# Customer Journey Map: [Persona/Segment] — [Journey name]

## Evidence base
[List sources used: interviews (n=), support tickets (date range), analytics, etc. State plainly if this map is
mostly assumption-based pending research.]

## Stages
| Stage | [Stage 1] | [Stage 2] | [Stage 3] | [Stage 4] |
|---|---|---|---|---|
| **Touchpoints** | | | | |
| **Customer actions** | | | | |
| **Thoughts & emotions** (Evidence/Assumption tagged) | | | | |
| **Pain points** (Evidence/Assumption tagged) | | | | |

## Moments of truth
1. **[Stage/moment]** — why this disproportionately matters, with the evidence behind it
2. **[Stage/moment]** — [...]

## Pain points ranked by evidence strength
| Pain point | Stage | Evidence | Assumption or confirmed |
|---|---|---|---|

## What we still don't know
[Stages/cells that are assumption-only — this is the research backlog this map generates]
```

## Quality checklist

- [ ] Every emotion/thought cell is tagged Evidence or Assumption — none are unlabeled
- [ ] At least one direct customer quote appears per moment of truth
- [ ] Stages are named in customer terms, not internal process/team names
- [ ] The map includes an explicit "what we still don't know" section rather than looking complete
- [ ] Pain points tie to a number (support volume, drop-off rate, churn rate) where that data exists

## Related skills

- Turn assumption-tagged gaps into a real research plan: `talwar-pm-product-discovery-skill`
- Validate specific pain points with structured interviews before building: `talwar-pm-market-research-skill`
- Feed confirmed moments of truth into launch sequencing: `talwar-pm-go-to-market-skill`
- Prioritize which pain points to fix first: `talwar-pm-prioritization-matrix-skill`
