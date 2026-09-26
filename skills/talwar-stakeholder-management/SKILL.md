---
name: talwar-stakeholder-management
description: Build the ongoing engagement plan — cadence, channel, and tailored message per stakeholder — that keeps a power/interest map from going stale. Use when the user wants a communication plan, asks "how often should I update X," needs to handle a stakeholder who's gone quiet despite being important, or says "I mapped stakeholders but don't know what to actually do with them week to week."
---

# Stakeholder Management

## Why this matters

A stakeholder map is a photograph; this skill is the ongoing film. The map tells you a stakeholder is high-power and
currently low-interest — it doesn't tell you what to send them next Tuesday or what to do the day they suddenly
start paying attention. Most stakeholder failures happen not because nobody made a map, but because the plan built
from it never adapted: the same monthly all-hands deck goes to the exec who could kill the project and the junior
analyst who's just curious, and neither gets what they actually need. Cadence and channel are not administrative
details — they're the mechanism by which "keep satisfied" or "manage closely" becomes a real behavior instead of a
label in a spreadsheet. The single highest-leverage move in this skill is handling the high-power/low-interest
stakeholder correctly: they are the most dangerous to manage badly, because under-engaging them feels safe (they
haven't asked for anything) right up until they weigh in late, with full authority and none of the context, and the
project absorbs the cost of catching them up under pressure instead of on a schedule you controlled.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **An existing stakeholder map** (power/interest quadrants) — if none exists, run `talwar-stakeholder-mapper` first;
  this skill assumes the snapshot is already done
- **Current state of engagement** — what's already happening today per stakeholder (nothing, an ad hoc Slack, a
  standing meeting) so the plan is a change from reality, not a restatement of it
- **Upcoming decision points or milestones** that will need specific stakeholder sign-off or awareness
- **Known friction** — a stakeholder who's been burned before, one who reads status updates and one who ignores them

## Process

1. **Assign cadence and channel per quadrant, not per person, then adjust for individuals.** As a default: manage-
   closely gets a recurring 1:1 or working session; keep-satisfied gets a periodic executive-level summary (not the
   detailed working doc); keep-informed gets a lightweight broadcast (digest, wiki update); monitor gets nothing
   proactive beyond being on a distribution list. Adjust from there for someone's actual preference (some execs want
   the detail; some ICs want less).
2. **Tailor the message, not just the frequency.** The same underlying status translates differently: a budget
   owner needs cost/timeline/risk; an engineering lead needs technical dependencies and blockers; an end-user
   representative needs what's changing for their day-to-day. Write the one-line "what they actually care about"
   for each stakeholder before drafting any update.
3. **Build the specific plan for high-power/low-interest stakeholders.** This is the quadrant most plans skip
   because "they don't seem to want updates." Give them a short, infrequent, high-signal touchpoint (a two-line
   email before a milestone, not a meeting invite) so they're never blindsided and never asked to spend attention
   they haven't offered. State explicitly what would trigger moving them into more active management (a scope
   change that touches their budget, a delay that affects their commitments).
4. **Set a two-way channel, not just outbound broadcast**, for anyone in manage-closely — a plan that only pushes
   information out can't surface a stakeholder's objection before it becomes a blocker.
5. **Revisit the map on a schedule**, not only when something goes wrong. Interest and power shift with reorgs,
   budget cycles, and incidents; a plan built on a stale map re-creates the exact blind spot the map was meant to
   fix.
6. **Define an escalation path** for when a stakeholder disagrees with direction — who resolves it, and by when —
   so disagreement doesn't sit unresolved until it becomes a public blocker.

## Output template

```markdown
# Stakeholder Engagement Plan: [Initiative]

## Engagement plan by stakeholder

| Stakeholder | Quadrant | Cadence | Channel | What they actually care about | Owner of this relationship |
|---|---|---|---|---|---|
| [Name/role] | [from map] | [Weekly/Biweekly/Monthly/As-needed] | [1:1 / exec summary / digest / none proactive] | [1 line] | [name] |
| | | | | | |

## High-power, low-interest — specific handling
| Stakeholder | Light-touch plan (what, how often) | Trigger that would escalate them to closer management |
|---|---|---|
| | | |

## Two-way channels for "manage closely" stakeholders
[How they can raise an objection or question outside the scheduled cadence, and who monitors that channel]

## Escalation path
[Who resolves a stakeholder disagreement, in what forum, and within what timeframe]

## Map review schedule
[When the underlying power/interest map gets re-checked — e.g., "before each major milestone" or "monthly"]
```

## Quality checklist

- [ ] Does every stakeholder have a cadence and channel, not just a quadrant label?
- [ ] Is the message content tailored per stakeholder's actual concern, not one deck sent to everyone?
- [ ] Does the high-power/low-interest quadrant have an explicit light-touch plan and an escalation trigger?
- [ ] Is there a two-way channel for stakeholders in manage-closely, not only outbound updates?
- [ ] Is there a stated schedule for re-checking the map, so the plan doesn't quietly go stale?

## Related skills

- Build the underlying power/interest snapshot this plan is based on: `talwar-stakeholder-mapper`
- Use this plan's cadence to structure recurring status content: `talwar-stakeholder-communication`
- Feed a disengaged high-power stakeholder into a pre-launch risk check: `talwar-pre-mortem`
- Formalize a stakeholder disagreement into a documented decision: `talwar-decision-memo`
