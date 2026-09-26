---
name: talwar-pre-mortem
description: Run a pre-mortem — imagine the project has already failed and work backward to find out why, before launch rather than after. Use when the user wants a risk assessment, says "what could go wrong," is about to greenlight a big bet, asks to "stress-test this plan," or is planning a launch/migration/re-org and needs the risks surfaced while there's still time to act on them.
---

# Pre-Mortem

## Why this matters

A standard "what could go wrong?" brainstorm invites hedged, generic answers ("resourcing might be tight") because
admitting a real risk feels like betting against the plan you're supposedly there to support — nobody wants to be
the one who talked the project down. Gary Klein's pre-mortem technique (prospective hindsight) sidesteps this by
changing the premise: instead of asking whether the project will fail, it declares the project has already failed —
typically 6-12 months out — and asks the team to explain why. That single reframe unlocks specificity, because
"why did we fail" is a factual, retrospective-sounding question, not an act of disloyalty. It also directly attacks
optimism bias and groupthink: people are far better at generating plausible causes for an outcome they're told
already happened than at forecasting an uncertain future one. The output is only useful if it goes somewhere —
a pre-mortem that ends at "here's a scary list" is just anxiety with extra steps. The real deliverable is the subset
of failure stories that are both plausible and severe, converted into a mitigation or an owner now, while the cost
of acting is still low.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **What the project/initiative is** and its stated goal or success definition
- **The time horizon for "failure"** — pick a concrete future date (e.g., "it's 9 months from now")
- **Who's in the room** — pre-mortems work best with the people who'll actually execute, not just leadership,
  because they know where the bodies are buried
- **Anything already flagged as risky** so you don't waste slots restating the obvious

## Process

1. **Set the premise as fact, not hypothesis.** Open with: "It's [date, 6-12 months out]. [Project] has failed —
   not underperformed, failed: canceled, rolled back, or missed its goal so badly it's considered a mistake. Nobody
   in this room is being blamed; we're just documenting what happened." The declarative framing is what makes this
   work — a conditional framing ("might fail") collapses back into a normal risk brainstorm.
2. **Generate failure stories, not risk categories.** Push for specific, causal narratives ("the migration ran over
   because the legacy data had three undocumented edge cases finance depended on") rather than abstract labels
   ("data quality risk"). A story can be checked for plausibility; a label can't.
3. **Cover the usual blind spots explicitly** if the group's list clusters in one area: technical execution,
   external dependencies (vendors, partners, regulation), adoption/behavior change, organizational (a reorg, a
   champion leaving, budget cut), and competitive/market timing.
4. **Rate each failure story on plausibility and severity.** Discard the vivid-but-unlikely ones (don't let a good
   story crowd out a boring but probable one) and the plausible-but-shrug ones (low severity, not worth a mitigation).
5. **Convert the top stories into action now.** For each, name one of: a mitigation to reduce likelihood, a leading
   indicator to detect it early, an owner accountable for watching it, or — if it's severe enough — a change to the
   plan itself. A failure story with no owner and no indicator is just decoration.
6. **Re-run the goal check.** If three or more top stories point at the same root cause (e.g., an unvalidated
   assumption about a partner API), that's a sign the plan itself, not just its risk register, needs to change.

## Output template

```markdown
# Pre-Mortem: [Project/Initiative]

## Premise
It is [date]. [Project] has failed: [what "failed" concretely means — canceled, rolled back, missed target by X].

## Failure stories

| # | Story (what happened, causally) | Category | Plausibility | Severity |
|---|---|---|---|---|
| 1 | [specific narrative] | [technical/external/adoption/org/market] | [Low/Med/High] | [Low/Med/High] |
| 2 | [...] | | | |
| 3 | [...] | | | |

## Top risks converted to action

| Failure story | Mitigation now | Leading indicator to watch | Owner |
|---|---|---|---|
| [# from above] | [specific action, not "monitor closely"] | [signal that would show this is happening] | [name/role] |
| | | | |

## Plan changes triggered by this exercise
[Any change to scope, sequencing, or approach the pre-mortem surfaced — or "none; existing plan holds" if genuinely
none did]

## Root cause pattern (if any)
[If multiple failure stories trace to one unvalidated assumption or single point of failure, name it here]
```

## Quality checklist

- [ ] Was the failure declared as fact ("has failed"), not framed as a hypothetical risk brainstorm?
- [ ] Are the failure stories specific causal narratives, not generic risk-category labels?
- [ ] Does every top-severity story have a named owner and a leading indicator, not just a mitigation in theory?
- [ ] Did at least one story surface something the group hadn't already flagged before this exercise?
- [ ] If multiple stories share a root cause, is that pattern called out rather than left buried in the table?

## Related skills

- Compare the plan against alternative approaches before it's locked in: `talwar-solution-options-generator`
- Turn the top risks into a stakeholder-facing risk section: `talwar-decision-memo`
- Build ongoing monitoring for the leading indicators identified here: `talwar-okrs-metrics`
- Feed unresolved organizational risks into engagement planning: `talwar-stakeholder-management`
