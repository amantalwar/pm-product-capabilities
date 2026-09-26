---
name: talwar-business-case
description: Write an investment justification and ROI analysis for a proposed initiative. Use when the user needs to justify spend, get budget or headcount approval, compare build-vs-buy-vs-partner, or asks "make the case for this," "what's the ROI here," or "write up why we should do this."
---

# Business Case

## Why this matters

A business case that only describes the option the author already wants isn't a case — it's an announcement dressed
up with a spreadsheet. Real credibility comes from showing that alternatives were genuinely weighed, including doing
nothing, and that at least one was rejected with a stated reason. A reader who sees only one option has no way to
tell whether it's actually the best choice or just the first idea that got written down; a reader who sees a
rejected alternative and understands why can trust that the comparison happened. The rejected option is often the
single most persuasive paragraph in the document, because it's proof of judgment, not just enthusiasm.

The other common failure is counting only the build cost and skipping the ongoing one — a project that looks cheap
because the maintenance, support, and opportunity cost never made it into the numbers will blow its ROI within a
year of shipping. A credible case quantifies benefit where it can and is explicit about assumption and confidence
where it can't, rather than forcing a fake number onto something genuinely uncertain.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **Problem statement** and evidence for the cost of doing nothing
- **Options already considered** — if none have been generated yet, run `talwar-solution-options-generator` first
- **Cost data**: one-time (build) and ongoing (run, support, opportunity cost of the team's time)
- **Benefit hypothesis** and how it would be measured or quantified
- **Time horizon** for the ROI/payback calculation
- **Decision-maker and risk tolerance** — who approves this and what they'll push back on

## Process

1. **Write the problem statement** grounded in evidence — a number, a trend, a customer complaint pattern — not
   just an assertion that something is a problem.
2. **List the options considered**, including do-nothing, with one sentence each on why every rejected option was
   rejected. A case with zero rejected alternatives is not yet credible — go find at least one.
3. **Break down cost** into one-time (build) and ongoing (run/support/maintain), plus the opportunity cost of the
   team building this instead of something else.
4. **Quantify expected benefit** wherever data allows; where it can't be quantified yet, state the assumption
   explicitly and name the leading indicator that would validate or kill it early.
5. **Compute a simple ROI or payback period** and show the assumptions behind it — never present the number without
   the inputs that produced it.
6. **Name the risks** that could prevent the benefit from materializing, and how each would be mitigated or
   monitored.
7. **End with a specific recommendation** — a named option and a specific ask (budget amount, headcount, timeline),
   not a summary that leaves the decision to the reader.

## Output template

```markdown
# Business Case: [Initiative name]

## Problem
[1-2 paragraphs, grounded in evidence — cost of inaction stated concretely]

## Options considered
| Option | Summary | Why rejected (or selected) |
|---|---|---|
| Do nothing | | |
| Option A | | |
| Option B (recommended) | | Selected — see below |

## Recommended option
[Which one, and the one-paragraph case for it]

## Cost
- One-time: [build cost, breakdown]
- Ongoing: [run/support/maintenance cost per period]
- Opportunity cost: [what the team isn't doing instead]

## Expected benefit
[Quantified where possible, with assumptions stated. If not quantifiable yet: leading indicator to validate.]

## ROI / payback
[Simple calculation, assumptions shown]

## Risks
| Risk | Likelihood | Mitigation |
|---|---|---|
| | | |

## Recommendation
[Specific ask: what you want approved, how much, by when]
```

## Quality checklist

- [ ] At least one alternative (besides the recommendation) is named and rejected with a real reason
- [ ] Cost includes ongoing/run cost, not just the one-time build estimate
- [ ] Every benefit claim is either quantified or paired with an explicit assumption and validation signal
- [ ] The recommendation is a specific, approvable ask — not a vague "we should probably do this"

## Related skills

- Generate the alternatives this case compares: `talwar-solution-options-generator`
- Rank this initiative against other funding candidates: `talwar-prioritization-matrix`
- Turn the recommendation into a decision record: `talwar-decision-memo`
- Weigh this investment against the broader portfolio: `talwar-portfolio-investment-allocation`
