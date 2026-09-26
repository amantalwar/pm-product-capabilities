---
name: scope-definition
description: Define explicit in-scope vs out-of-scope boundaries for a project or feature. Use when the user is worried about scope creep, needs to draw a hard line on what's included, hands over a fuzzy request that needs bounding before work starts, or asks "what's actually in scope here" or "let's define the boundaries."
---

# Scope Definition

## Why this matters

A long in-scope list feels thorough but leaves everything it didn't mention ambiguous — and ambiguity gets read by
stakeholders as "probably yes," especially once work is visibly underway and the easiest thing to assume is that
their pet request is quietly included. An explicit "we are NOT doing X" removes that reading entirely; it's a
different kind of statement, a decision rather than an omission, and it gives the team something concrete to point
back to when the request resurfaces later ("that was explicitly out of scope, and here's why"). The boundary-cases
section exists for the same reason: recording how a genuinely ambiguous item got resolved, and by whom, means the
decision doesn't get relitigated every time someone new encounters it.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed):

- **The initiative or feature** being scoped
- **Its target outcome** — scope decisions should be judged against this, not against "does it sound reasonable"
- **Requests or asks already floated** that need an explicit scope decision
- **Constraints driving the boundary** — deadline, team capacity, a dependency someone else owns

## Process

1. **Write the target outcome first.** Every scope decision that follows gets judged against whether it serves
   this outcome, not against general usefulness.
2. **List in-scope items** — concrete and short. This is not meant to be exhaustive; it's the headline commitment.
3. **List out-of-scope items explicitly** — specifically the things a reasonable stakeholder might assume are
   included but aren't. This list often matters more than the in-scope one.
4. **Give each out-of-scope item a one-clause reason** — protects the timeline, not yet validated, owned by another
   team, technically infeasible this cycle, etc. A bare "no" invites repeated litigation; a reason ends it.
5. **Identify boundary cases** — items that came up in discussion and were genuinely ambiguous. Record what was
   decided and who decided it, so the reasoning is preserved rather than re-argued from scratch later.
6. **Review the list with the stakeholder most likely to push back** before calling it final — a scope document
   that hasn't been shown to its most likely challenger isn't actually tested yet.
7. **Revisit at major milestones**, not just at kickoff. Scope drifts as work proceeds and new requests surface;
   treat each new ask as a candidate for either the out-of-scope list (with a reason) or the boundary-cases table,
   rather than letting it slide in unrecorded because "it's small."

## Output template

```markdown
# Scope: [Initiative/feature name]

**Target outcome:** [What this work is meant to achieve — the yardstick for every line below]

## In scope
- [Item]
- [Item]

## Out of scope
- [Item] — [reason: protects timeline / not validated / owned elsewhere / infeasible this cycle / etc.]
- [Item] — [reason]

## Boundary cases
| Item (ambiguous at first) | Resolution | Resolved by |
|---|---|---|
| | In scope / Out of scope — [why] | |

## Reviewed with
[Name(s) of stakeholder(s) most likely to push back, and their sign-off or open concern]
```

## Quality checklist

- [ ] Every out-of-scope item has a stated reason, not just a bare exclusion
- [ ] The boundary-cases table isn't empty if any request was actually discussed and disputed
- [ ] Every scope call ties back to the target outcome, not just "seemed reasonable to exclude"
- [ ] The list was reviewed with the stakeholder most likely to contest it, not just written and filed

## Related skills

- Summarize scope headlines inside the fuller kickoff doc: `project-briefing`
- Use the fast one-page version before a greenlight: `initiative-canvas`
- Turn resolved boundaries into detailed acceptance criteria: `requirements-definition`
- Record a contested boundary call as a formal decision: `decision-memo`
