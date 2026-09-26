---
name: backlog-management
description: Write or clean up user stories and manage a product backlog. Use for "write user stories for this," "is this backlog ready for sprint planning," "turn these requirements into tickets," or "what's our Definition of Ready" — including when the ask is really "why does this keep bouncing back from engineering."
---

# Backlog Management

## Why this matters

Most backlog dysfunction traces back to one habit: writing tasks and calling them stories. A task describes work
("migrate the database field"); a story describes value delivered to someone ("as a returning customer, I want my
saved address to persist, so I don't re-enter it every order"). Tasks get built and nobody can tell if they mattered;
stories get built and you can check whether the value showed up. INVEST is useful not as a checklist to satisfy but
because each letter catches a specific way stories go bad in practice — most commonly stories that are too big to
estimate honestly (violating Small and Estimable) or too solution-locked to negotiate (violating Negotiable). A
backlog that bounces back from engineering constantly is almost always a Definition of Ready problem, not a
communication problem — the story shipped to sprint planning wasn't actually ready to be picked up.

## Gather inputs first

Ask if not given (assume and state it if told to proceed):

- **Source material**: a PRD, a story map slice, raw requirements, or a list of feature requests to convert
- **Existing Definition of Ready**, if the team has one, to write consistent stories rather than invent new criteria
- **Team's estimation practice** (points, t-shirt sizes, none) so stories are sized to fit that unit of work
- **Dependencies** already known (data, other teams, third-party APIs) that need to be surfaced per story
- **Whether this is new-story writing or an audit/cleanup pass** on an existing backlog — different processes below

## Process

1. **Apply INVEST to every story, and treat a failure on any letter as a rewrite trigger, not a nitpick**:
   - **Independent** — can this be built and shipped without waiting on another unscheduled story? If not, either
     merge them or make the dependency explicit and sequenced.
   - **Negotiable** — does the story describe an outcome, leaving engineering room to choose the implementation? A
     story that specifies a UI layout in the story text has smuggled a task in as a story.
   - **Valuable** — does it name who benefits and how? If you can't state the value in one sentence, it's probably
     a task wearing story format.
   - **Estimable** — does the team have enough information to size it? Unknown unknowns (unclear dependency,
     unresearched approach) mean it needs a spike first, not an estimate.
   - **Small** — can it ship within roughly one sprint? If not, split it — usually along a workflow step, a data
     variation, or a rule variation, not by frontend/backend (splitting by layer breaks Valuable).
   - **Testable** — does it have concrete acceptance criteria a QA engineer or the PM could check without asking
     the author what they meant?
2. **Write in standard story form**: "As a [specific persona], I want [capability], so that [benefit]." Reject
   personas like "as a user" when a more specific one exists — specificity is what makes Valuable checkable.
3. **Attach acceptance criteria** as a short Given/When/Then list or bullet checklist per story — this is what makes
   Testable real rather than aspirational.
4. **Check against Definition of Ready before it enters a sprint candidate list**: acceptance criteria present,
   dependencies identified, design/UX attached if needed, estimated, no open questions blocking a start.
5. **Distinguish stories from tasks explicitly in the backlog.** Tasks (enabling work — infra, tech debt, spikes)
   are legitimate backlog items but shouldn't be dressed up in story form just to fit the template; label them as
   tasks so prioritization conversations aren't comparing value-delivery against enabling-work on the same axis
   without acknowledging it.

## Output template

```markdown
# Backlog: [Feature/Epic]

## Definition of Ready (confirm or set)
- [ ] Acceptance criteria defined
- [ ] Dependencies identified and sequenced
- [ ] Design/UX attached (if applicable)
- [ ] Estimated by the team
- [ ] No open blocking questions

## Stories
### [Story ID/title]
**As a** [specific persona] **I want** [capability] **so that** [benefit]

**Acceptance criteria:**
- Given [context], when [action], then [outcome]
- [...]

**INVEST check:** [note any letter that required a rewrite, e.g. "split from original — was too large"]
**Dependencies:** [none / named]
**Estimate:** [...]

[Repeat per story]

## Tasks (enabling work, not user-facing value — labeled separately)
- [Task]: [why it's needed, what it unblocks]

## Split/merge log
[Any stories split for size or merged for independence, and why]
```

## Quality checklist

- [ ] Every story names a specific persona and a specific benefit, not "as a user, I want X"
- [ ] Every story has acceptance criteria concrete enough to test without asking the author to clarify
- [ ] No story both fails an INVEST letter and ships unchanged — failures triggered a split, merge, or rewrite
- [ ] Tasks (enabling work) are labeled as tasks, not disguised as stories
- [ ] Definition of Ready is checked explicitly, not assumed

## Related skills

- Source stories from a story map's MVP slice: `feature-story-mapping`
- Turn raw requirements into a PRD before story-writing: `requirements-definition`
- Rank which stories go into the next sprint: `prioritization-matrix`
- Confirm delivered stories actually met acceptance criteria: `verification-uat`
