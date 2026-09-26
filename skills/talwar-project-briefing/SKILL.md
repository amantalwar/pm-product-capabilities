---
name: talwar-project-briefing
description: Write a consolidated, stakeholder-facing project brief once an initiative has been greenlit. Use when the user needs a fuller kickoff document than a one-pager, has to align a cross-functional team and stakeholders before work starts, or asks for "a project brief," "kickoff doc," or "write up the background and plan for this project."
---

# Project Briefing

## Why this matters

This is the shared reference multiple functions will still be relying on months into the project — someone joining
late, a stakeholder catching up before a review, an exec skimming before a decision — so it needs enough context
that a newcomer can orient without a meeting. That's the difference from `talwar-initiative-canvas`: the canvas exists to
get a fast yes/no before work starts, while this exists to keep a team and its stakeholders aligned once work is
underway and the cost of a misunderstanding has gone up. Getting the stakeholder map or communication plan wrong here
is expensive precisely because misalignment discovered mid-project — the wrong person left out of a decision, an
update that never reached someone who needed it — costs far more to fix than misalignment caught at kickoff.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **Background/context** — what led here, what's been tried before
- **Objectives**, and the strategic pillar or OKR they ladder to
- **Scope headlines** — pull from `talwar-scope-definition` if that work has already happened
- **Stakeholder list** with roles and decision rights — pull from `talwar-stakeholder-mapper` if available
- **Target milestones** and **success criteria**
- **Known risks** and who owns tracking each one
- **Update cadence expectations** — how often, to whom, in what format

## Process

1. **Write the background** — enough that someone with zero context understands what led to this project and why
   now, not just what the project is.
2. **State objectives** and tie them explicitly to the strategic pillar or OKR they serve.
3. **Summarize scope** at the headline level; link out to the full `talwar-scope-definition` artifact if the boundaries are
   contentious or detailed.
4. **List stakeholders** with role, stake, and decision rights — not just names. Distinguish who decides from who's
   informed.
5. **Set milestones** — key checkpoints, not a full project plan; this is a brief, not a Gantt chart.
6. **Define success criteria** — ideally the same metric as the target outcome from the initiative canvas, so
   nothing shifts silently between greenlight and kickoff.
7. **List top risks** with a named owner for tracking each one, not just a description.
8. **Write the communication plan** — cadence, channel, and audience per type of update (weekly team standup vs.
   monthly exec summary are different audiences with different content).

## Output template

```markdown
# Project Brief: [Project name]

## Background
[Context a newcomer needs — what led here, what's been tried]

## Objectives
[What this project achieves, tied to pillar/OKR: link]

## Scope
- In scope (headline): [...]
- Out of scope (headline): [...]
- Full boundary detail: [link to scope-definition doc if applicable]

## Stakeholders
| Name/Role | Stake | Decision rights |
|---|---|---|
| | | |

## Milestones
| Milestone | Target date/range | Owner |
|---|---|---|
| | | |

## Success criteria
[How we'll know this worked — measurable]

## Risks
| Risk | Owner | Mitigation |
|---|---|---|
| | | |

## Communication plan
| Update type | Cadence | Channel | Audience |
|---|---|---|---|
| | | | |
```

## Quality checklist

- [ ] A stakeholder unfamiliar with the project could read this and know who to ask about what
- [ ] Success criteria are measurable, not a restatement of the objective in vaguer terms
- [ ] The communication plan names cadence, channel, and audience per update type — not just "we'll keep people posted"
- [ ] Every listed risk has a named owner, not just a description

## Related skills

- Use the fast version of this before a greenlight exists: `talwar-initiative-canvas`
- Build the stakeholder table from a proper mapping exercise: `talwar-stakeholder-mapper`
- Resolve ambiguous scope before finalizing the brief: `talwar-scope-definition`
- Execute the communication plan once the project is live: `talwar-stakeholder-communication`
