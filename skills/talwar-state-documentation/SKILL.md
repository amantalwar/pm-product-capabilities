---
name: talwar-state-documentation
description: Document current state (as-is), target state (to-be), and the concrete gap between them. Use when the user asks for a current-state assessment, wants to document "how things work today" before proposing a change, needs a gap analysis for a migration or re-org, or says "let's write down what's actually happening before we argue about what to do about it."
---

# State Documentation (As-Is / To-Be / Gap)

## Why this matters

Most disagreements about what to change are actually undiagnosed disagreements about what currently exists. Two
people can debate a re-org for an hour while silently picturing different org charts. Documenting the as-is state
solves this by pinning down a shared, checkable description of reality before anyone proposes a fix — and it only
works if it stays factual. The moment an as-is document drifts into "the previous team never prioritized this
properly," it stops being a shared reference and starts being an argument, and the people whose work is being
described will (correctly) stop trusting it and start contesting it line by line. Facts are falsifiable and
attributable to a source (a system, a log, an interview, a document); opinions about whose fault the current state
is are neither, and they derail the exercise from "what do we change" into "who do we blame." The gap analysis is
the actual payoff — it's not "as-is is bad, to-be is good," it's a concrete, actionable list of what specifically
has to change (a process, a system, a skill, a policy) to get from one to the other, which is what a project plan
can actually be built from.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **Scope** — what system, process, team, or product area this covers (state boundaries explicitly; scope creep
  here produces an unreviewable document)
- **Sources for as-is** — who to interview, what systems/docs to pull from, so claims can be attributed
- **The target state**, if already decided elsewhere (a strategy doc, an exec mandate) — don't invent one if it's
  not this skill's job to define it; if genuinely undefined, flag that as a prerequisite
- **Audience** — who reads this and what decision it feeds (a migration plan, a budget request, a re-org proposal)

## Process

1. **Document as-is as observable fact, attributed to a source.** Every claim should be checkable: "per the Q3
   incident log, average time-to-resolve is 6 hours" not "the on-call process is a mess." If you don't have a
   source for a claim, either get one or mark it explicitly as unverified rather than stating it as fact.
2. **Separate fact from interpretation visually.** If interpretation is useful (and often it is — "this suggests X"),
   put it in a clearly labeled "implications" note, never blended into the same sentence as the fact itself.
3. **Strip blame-coded language on sight.** "Nobody owns this," "the team never documented it," "this was built
   wrong" are opinions wearing fact clothing — rewrite as what's observably true instead ("no documented owner
   exists for X as of [date]"; "no runbook exists for Y").
4. **Document to-be with the same rigor** — specific and checkable, not aspirational. "Faster" isn't a to-be state;
   "time-to-resolve under 1 hour for P1 incidents" is.
5. **Build the gap as a list of concrete changes, not a restatement of the difference.** For each gap, name what
   has to change — a system, a process, a role, a skill, a policy — and roughly what that change requires. "As-is
   has no on-call rotation, to-be needs 24/7 coverage" is a difference; "stand up a rotation across 3 timezones,
   requires hiring 2 additional engineers or a vendor contract" is a gap you can plan against.
6. **Flag gaps with no clear owner or no clear path** rather than papering over them with a vague action item — an
   honest "we don't yet know how to close this gap" is more useful downstream than a fabricated plan.

## Output template

```markdown
# State Documentation: [Scope]

## Scope
[What this covers and explicitly does not cover]

## Current state (as-is)
[Organized by relevant sub-area — system, process, team, etc. Every claim attributed to a source.]

### [Sub-area 1]
- [Fact], per [source, date]
- [Fact], per [source, date]

### [Sub-area 2]
- [...]

## Target state (to-be)
[Same structure, specific and checkable — not aspirational adjectives]

### [Sub-area 1]
- [Specific target]

## Gap analysis

| Sub-area | As-is | To-be | What has to change | Rough effort/owner |
|---|---|---|---|---|
| | | | | |
| | | | | |

## Unresolved gaps
[Gaps with no clear path to closure yet — named honestly rather than papered over]

## Sources
[List of systems, documents, and people consulted for the as-is state]
```

## Quality checklist

- [ ] Is every as-is claim attributed to a source, and free of blame-coded language ("nobody bothered to...")?
- [ ] Is the to-be state specific and checkable, not a list of adjectives ("faster," "more scalable")?
- [ ] Does each gap row name a concrete change (system/process/role/policy), not just restate the difference?
- [ ] Are unresolved gaps (no known path to close) stated honestly rather than filled with a vague action item?
- [ ] Could someone named in the as-is section read it without feeling blamed?

## Related skills

- Turn the gap list into a sequenced execution plan: `talwar-roadmapping`
- Justify the investment needed to close the gap: `talwar-business-case`
- Use this as the foundation for a requirements doc on the to-be state: `talwar-requirements-definition`
- Stress-test whether the to-be plan will actually close the gap: `talwar-pre-mortem`
