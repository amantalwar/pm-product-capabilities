---
name: talwar-verification-uat
description: Design user acceptance testing (UAT) that validates a feature solves the actual business problem, not just that it works as coded. Use when the user needs UAT scenarios written from acceptance criteria, is planning sign-off before a launch, asks "how do we know this is actually ready," or conflates "QA passed" with "the business is ready to accept this."
---

# Business Verification & UAT Design

## Why this matters

QA and UAT answer different questions, and treating them as the same gate is how teams ship something that works
perfectly and still fails the business. QA asks "does this do what we built it to do" — verified by engineers or
testers against the spec, in a test environment, using test data. UAT asks "does this solve the problem we set out
to solve" — verified by real business users, against real (or realistic) scenarios, using data and workflows that
look like their actual day. A feature can pass every QA test and still fail UAT: the login flow works flawlessly
but the finance team can't actually close the month with it, because the spec captured what was easy to define, not
what finance actually does. UAT is also the last checkpoint before the business, not just the build, owns the
outcome — which is why sign-off has to come from the people who'll live with the result, using scenarios that stress
their real edge cases, not a happy-path click-through that was really just QA repeated by a different person.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **The acceptance criteria or requirements** this feature was built against — UAT scenarios should trace back to
  these, not be invented fresh
- **Who the real business users are** — the specific people or roles who'll sign off, not "the team"
- **Realistic scenarios and data** — actual workflows, edge cases, and volumes these users deal with, not idealized
  test data
- **What "done" means for the business**, if different from what's in the ticket — sometimes the written acceptance
  criteria miss a workflow step everyone assumed was obvious

## Process

1. **Confirm QA is complete before UAT starts.** UAT is not a place to catch build bugs — if QA hasn't verified the
   feature works as specced, UAT will surface noise (crashes, broken buttons) that drowns out the real question
   (does this solve the business problem).
2. **Derive UAT scenarios from acceptance criteria, but write them as business stories, not technical checks.**
   Acceptance criterion "system supports bulk invoice upload up to 500 rows" becomes a UAT scenario: "AP clerk
   uploads last month's real batch of ~450 vendor invoices, including the 12 that historically fail validation, and
   confirms the exception report matches what they'd expect to see."
3. **Include the edge cases the business actually hits**, not just the happy path — the transaction that always
   needs a manual override, the customer type that doesn't fit the standard flow, the month-end volume spike. These
   are usually known to the business users and absent from the original spec.
4. **Use real or realistic data**, not synthetic test fixtures — UAT run on clean, idealized data validates nothing
   the business couldn't already assume from QA passing.
5. **Have the actual business user execute it**, not a proxy (a BA or PM standing in). If the real user's schedule
   is the constraint, that's worth surfacing as a project risk, not a reason to substitute someone else's judgment
   for theirs.
6. **Define sign-off criteria before testing starts**, not after — what counts as pass (all critical scenarios pass,
   no P1 issues open), who has authority to sign off, and what happens to a scenario that partially fails (blocks
   launch vs. logged as a known-issue with a follow-up date).

## Output template

```markdown
# UAT Plan: [Feature/Release]

## Scope
[What's being validated, and what's explicitly out of scope for this UAT round]

## Prerequisite: QA status
[Confirmation QA is complete, with a link/reference — UAT does not start until this is true]

## UAT scenarios

| # | Business scenario (user's real workflow) | Traces to acceptance criterion | Data used | Expected business outcome | Pass/Fail |
|---|---|---|---|---|---|
| 1 | [e.g., "AP clerk uploads last month's real invoice batch including known exception cases"] | [ref] | [real/realistic] | [what the user should be able to conclude] | |
| 2 | | | | | |

## Business users executing UAT
| Role | Name | Scenarios owned |
|---|---|---|
| | | |

## Sign-off criteria
- Pass condition: [e.g., "all critical scenarios pass, zero open P1 issues"]
- Partial-fail handling: [blocks launch / logged as known issue with owner + target date]
- Sign-off authority: [name/role who can formally accept]

## Sign-off record
| Signed off by | Date | Conditions attached (if any) |
|---|---|---|
| | | |
```

## Quality checklist

- [ ] Does every UAT scenario read as a business workflow a real user would recognize, not a re-run of a QA test case?
- [ ] Are real business users executing it, not a PM/BA proxy standing in for them?
- [ ] Do scenarios include known edge cases and realistic data volumes, not just the happy path on clean fixtures?
- [ ] Were sign-off criteria (pass condition, partial-fail handling, sign-off authority) set before testing started?
- [ ] Is it clear QA was completed first, so UAT results reflect business fit, not build defects?

## Related skills

- Pull acceptance criteria this UAT plan traces back to: `talwar-requirements-definition`
- Use the as-is/to-be gap to confirm UAT scenarios cover the real change: `talwar-state-documentation`
- Escalate a failed sign-off through the stakeholder engagement plan: `talwar-stakeholder-management`
- Feed unresolved UAT risk into a pre-launch check: `talwar-pre-mortem`
