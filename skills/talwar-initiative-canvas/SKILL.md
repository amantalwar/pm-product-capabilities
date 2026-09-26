---
name: talwar-initiative-canvas
description: Produce a single-page strategic initiative definition to get an idea greenlit fast. Use when the user needs a quick one-pager to pitch a new initiative before writing anything heavier, wants to get a yes/no before investing more time, or asks "can you draft a one-pager for this," "initiative canvas," or "quick pitch doc." Not the same as a full project brief — this is the fast version used before approval.
---

# Initiative Canvas

## Why this matters

This exists specifically to be read in under two minutes by someone who will say yes, no, or not-now — which means
every section earns its place by forcing clarity the author would otherwise defer. A hypothesis that isn't stated as
falsifiable ("if we do X, Y happens, because Z") lets the pitch survive on vibes instead of a testable claim. Scope
boundaries stated even briefly stop the reader from assuming a bigger commitment than what's being asked. This is
deliberately the fast, cheap artifact used to get a decision before the fuller work — see `talwar-project-briefing` — gets
written; if it takes more than one page, it's no longer doing its job.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **The problem or opportunity**, in one or two sentences, with a shred of evidence behind it
- **The hypothesis** — what the team believes will happen if this is pursued
- **A single owner** — initiatives without one owner rarely survive the greenlight
- **Rough timeline** — order of magnitude, not a date
- **Any hard constraints** already known (budget ceiling, dependency, deadline)

## Process

1. **State the problem** in one sentence, tied to evidence — a number, a complaint pattern, a competitive gap.
2. **Write the hypothesis** as "if we do X, then Y happens, because Z" — if it can't be phrased this way, it isn't
   specific enough yet to greenlight.
3. **Name the target outcome** — the single metric or observable change that would prove or disprove the
   hypothesis. One, not five.
4. **Draw scope boundaries** — one line of headline in-scope, one explicit non-goal. (Full detail belongs in
   `talwar-scope-definition`; this is the summary.)
5. **List key risks** — the top two or three that could sink this, not an exhaustive risk register.
6. **Name the owner and rough timeline.**
7. **End with an explicit decision ask** — what you want the reader to approve, specifically.
8. **Cut ruthlessly** until it fits one page. If a section needs more than 2-3 sentences, that detail belongs in the
   fuller brief that gets written after the greenlight, not here.

## Output template

```markdown
# Initiative Canvas: [Name]

**Owner:** [Name]  |  **Timeline:** [Rough duration, e.g. "6-8 weeks"]

## Problem
[1-2 sentences, with evidence]

## Hypothesis
If we [do X], then [Y happens], because [Z].

## Target outcome
[The single metric/observable change that proves or disproves the hypothesis]

## Scope
- In scope (headline): [...]
- Explicitly NOT in scope: [...]

## Key risks
1. [...]
2. [...]
3. [...]

## Decision requested
[Exactly what you want approved — budget, headcount, go-ahead to start discovery, etc.]
```

## Quality checklist

- [ ] Fits on one page — if it doesn't, cut, don't add a second page
- [ ] The hypothesis is phrased as if/then/because and is falsifiable
- [ ] At least one explicit non-goal is stated, not just a list of what's included
- [ ] A single named owner, not a team or "TBD"
- [ ] Ends with a specific, answerable decision ask

## Related skills

- Write the fuller version once this gets a yes: `talwar-project-briefing`
- Expand the scope boundary into a full in/out list: `talwar-scope-definition`
- Build the ROI case if the decision needs budget justification: `talwar-business-case`
- Stress-test the hypothesis before committing resources: `talwar-pre-mortem`
