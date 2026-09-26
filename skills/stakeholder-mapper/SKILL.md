---
name: stakeholder-mapper
description: Identify every stakeholder on an initiative and plot them on a power/interest matrix to decide who needs hands-on management versus a monthly email. Use when the user asks "who do I need to get on board," wants a stakeholder map or RACI-adjacent snapshot, is kicking off a new initiative and needs to know who matters, or says "who's going to block this if I don't loop them in."
---

# Stakeholder Mapper

## Why this matters

Most stakeholder problems aren't caused by ignoring stakeholders — they're caused by treating them all the same.
Sending everyone the same weekly update is really a decision to under-invest in the few people who could kill the
project and over-invest in people who were never going to object anyway. The power/interest matrix (a staple of
change-management and project literature) forces a cheap but real triage: power is their ability to help or block
the outcome (budget authority, veto rights, control of a dependency), interest is how much they care about this
specific outcome either way. Crossing those two axes produces four genuinely different engagement postures, not
four synonyms for "communicate." The riskiest cell is not the noisy low-power complainer — it's the high-power,
low-interest stakeholder who isn't paying attention yet, because their silence today is not the same as their
support, and the first time they do pay attention might be to kill the project in one meeting. This skill produces
a snapshot; if the user needs the ongoing cadence and message-by-quadrant plan built from it, that's a separate,
living document — see `stakeholder-management`.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **The initiative or decision** this map is for — stakeholder relevance is always relative to a specific thing
- **Who plausibly has a stake** — direct team, adjacent teams, budget owners, legal/compliance, end users or their
  representatives, external partners/vendors
- **What "power" means in this context** — budget sign-off, veto over launch, control of a dependency, influence
  over other stakeholders
- **Any known history** — a past version of this initiative that stalled, a stakeholder who's blocked similar work
  before

## Process

1. **List every plausible stakeholder before filtering.** Cast wide first — include people who are only tangentially
   affected — then cut. It's cheaper to remove a row than to discover a missed stakeholder after launch.
2. **Score power independently of how much you like or agree with them.** Power is structural (do they control
   budget, a dependency, a veto, or another stakeholder's opinion), not a measure of how reasonable their position is.
3. **Score interest as-is, not as you wish it were.** A stakeholder who should care but currently doesn't is scored
   low-interest today — the map reflects current reality so the gap is visible, not an aspirational future state.
4. **Plot into the four quadrants** and assign the standard engagement posture per quadrant:
   - **High power, high interest** — manage closely: regular direct engagement, involve in decisions
   - **High power, low interest** — keep satisfied: enough visibility that they're never surprised, not so much
     that you waste their attention
   - **Low power, high interest** — keep informed: they can't block or help much but can shift sentiment; regular
     updates cost little and build goodwill
   - **Low power, low interest** — monitor: minimal effort, watch for a change in either axis
5. **Flag the dangerous cell explicitly.** Anyone high-power/low-interest gets a specific note on why they're
   disengaged and what would change that — this is the group most likely to surprise you late.
6. **Note direction of movement**, not just current position — a stakeholder trending from low to high interest
   (a reorg, a budget cycle, a public incident) needs a plan before they arrive in a new quadrant, not after.

## Output template

```markdown
# Stakeholder Map: [Initiative]

## Power/interest matrix

| Stakeholder | Role/team | Power (Low/Med/High) | Interest (Low/Med/High) | Quadrant | Engagement posture |
|---|---|---|---|---|---|
| [Name/role] | | | | [Manage closely / Keep satisfied / Keep informed / Monitor] | [1 line] |
| | | | | | |

## High-power, low-interest — the risk cell
| Stakeholder | Why disengaged now | What would activate their interest | What to do before that happens |
|---|---|---|---|
| | | | |

## Stakeholders trending toward a different quadrant
[Anyone whose power or interest is likely to shift soon, and why]

## Gaps to close before proceeding
[Any stakeholder category that's missing entirely — e.g., no one from legal/compliance mapped, no end-user voice]
```

## Quality checklist

- [ ] Is power scored on structural ability to help/block, not on how much you agree with the stakeholder?
- [ ] Is at least one high-power/low-interest stakeholder identified and given an explicit "why disengaged" note?
- [ ] Does the list include stakeholders outside the immediate team (legal, ops, external partners) where relevant?
- [ ] Is the posture per stakeholder specific enough to act on, not just the quadrant label restated?

## Related skills

- Turn this snapshot into an ongoing cadence, channel, and message plan: `stakeholder-management`
- Feed unresolved stakeholder risk into a pre-launch risk check: `pre-mortem`
- Use the map to decide who signs off on scope: `scope-definition`
- Reference the map when building the project's kickoff brief: `initiative-kickoff`
