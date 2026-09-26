---
name: stakeholder-communication
description: Run an ongoing stakeholder engagement programme — mapping, per-quadrant engagement design, a recurring narrative, and a review cadence that checks whether stakeholders are actually moving — this is a multi-stage, ongoing workflow for the larger job of managing stakeholders over time, so use it for broader asks like "help me build out a stakeholder communication plan for this initiative" or "I need an ongoing way to keep stakeholders aligned," not a single narrow ask like "just map my stakeholders" (use `stakeholder-mapper`) or "just write this one update" (use `executive-storyline`).
---

# Stakeholder Communication

## What this orchestrates

This is a running programme, not a one-time document: it maps stakeholders, designs a specific engagement plan per
quadrant, structures the recurring narrative used to update them, and — critically — reviews on a cadence whether
the engagement is actually working, i.e. whether stakeholders are moving in the direction you need (a
disengaged-but-powerful stakeholder becoming engaged, a skeptical one becoming neutral). A stakeholder map made
once and never revisited is a snapshot, not a communication plan. Use this workflow for an initiative or
relationship that will run for months and needs ongoing tending; use the standalone `stakeholder-mapper` or
`stakeholder-management` skills alone for a one-time mapping exercise or a single engagement plan with no review
loop attached.

## Stages

1. **Map** — `stakeholder-mapper`
   Plot stakeholders by power/interest (or influence/alignment) into quadrants. Base placement on observed
   behavior — meeting attendance, questions asked, past decisions — rather than assumed org-chart seniority.
   **Gate to proceed:** every stakeholder who could block or meaningfully slow the initiative is on the map with a
   current (not assumed) quadrant placement — verified against recent behavior, not reputation.

2. **Design the per-quadrant engagement plan** — `stakeholder-management`
   For each quadrant, define the specific engagement approach: manage-closely for high-power/high-interest,
   keep-satisfied for high-power/low-interest, and so on — with a specific cadence and channel per stakeholder, not
   a generic policy per quadrant. Two stakeholders in the same quadrant can still need different treatment if their
   underlying concerns differ.
   **Gate to proceed:** every high-power stakeholder has a named engagement owner and a specific next touchpoint on
   the calendar — not just a quadrant label.

3. **Structure the recurring narrative** — `executive-storyline`
   Build the SCQA/pyramid structure that will be reused across recurring updates to these stakeholders, so each
   update doesn't get rebuilt from scratch and stays consistent in what it leads with. A consistent structure also
   makes it easier for a returning stakeholder to spot what's actually changed since the last update.
   **Gate to proceed:** there's a reusable update template with the governing thought slot clearly defined — a
   structure the next update can be dropped into within an hour, not rebuilt from a blank page.

4. **Cadence and review** — no dedicated atomic skill; this is the review loop itself
   On a set schedule (typically monthly or per milestone), re-plot each stakeholder's actual quadrant against their
   prior position and check: is the disengaged-but-powerful stakeholder moving toward engaged? Is a
   previously-skeptical stakeholder softening or hardening? Adjust the engagement plan (stage 2) for anyone who
   moved the wrong direction. This is the stage that turns a map into a programme — everything before it is setup.
   **Gate to proceed:** the review has produced at least one explicit change to the engagement plan (a new
   touchpoint, a changed owner, an escalation) — a review that changes nothing is a status check, not a working
   review loop.

## Sequencing notes

- Stages 1-3 are sequential the first time through (you can't design engagement before mapping, can't structure a
  narrative usefully before knowing who it's for) — but stage 4 is not a one-time stage, it's a recurring loop that
  restarts at stage 1's re-plotting each cycle. Think of stages 1-3 as setting up the programme and stage 4 as the
  programme itself, running for as long as the initiative or relationship does.
- Stage 3 (narrative structure) only needs to be built once and then reused across every stage-4 review cycle —
  don't rebuild it each cadence, refine it if the audience's skepticism pattern changes. Rebuilding it from scratch
  every cycle is itself a sign the earlier structure wasn't actually reusable.
- **The most common skipped stage is #4 (cadence and review)** — teams build a thorough map and engagement plan
  once at kickoff and treat it as done. What breaks downstream: stakeholder positions are not static — a
  disengaged executive can become actively blocking without anyone noticing until it surfaces as a stalled
  approval, because nobody re-plotted the map after the initial pass. The map silently goes stale and the team is
  managing stakeholders as they were three months ago, not as they are now.

## Final output

A running stakeholder communication plan, not a single document: the current stakeholder map (stage 1, versioned
over time), the per-quadrant engagement plan with named owners and touchpoints (stage 2), the reusable narrative
template (stage 3), and a log of review cycles showing how stakeholders have moved and what was adjusted each time
(stage 4) — handed back as a living plan with its next scheduled review date attached, not a one-time deliverable.
Anyone taking over the stakeholder relationship mid-programme should be able to see not just who the stakeholders
are today, but the trend — who's moving toward or away from engagement, and what's already been tried.

## Quality checklist

- [ ] Is the stakeholder map dated, with evidence it's been re-checked at least once since the initiative started,
      rather than frozen from kickoff?
- [ ] Does every high-power stakeholder have a named owner and a specific next touchpoint, not just a quadrant
      label?
- [ ] Does the review log show at least one instance of the engagement plan actually changing in response to a
      stakeholder moving quadrants?
- [ ] Is there a next review date already on the calendar, rather than "we'll revisit this periodically"?
- [ ] Would a skeptical stakeholder recognize the recurring narrative as addressing their actual concerns, rather
      than reusing the same talking points regardless of how their position has shifted?
