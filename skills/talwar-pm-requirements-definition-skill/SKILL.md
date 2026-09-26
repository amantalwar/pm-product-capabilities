---
name: talwar-pm-requirements-definition-skill
description: Run the full multi-stage journey from raw stakeholder interviews/notes to a signed-off requirements document — this is a multi-stage workflow for a larger end-to-end job, so trigger it on broader asks like "turn these interviews into requirements," "get this signed off before we build," or "help me go from notes to a spec the team can build from," not on a single narrow ask like "just write the acceptance criteria."
---

# Requirements Definition

## What this orchestrates

This is a sequence, not a single technique: raw, messy input (interview notes, stakeholder rambling, an old system
that half-works) becomes a bounded, testable, signed-off requirements document. Each stage narrows the ambiguity the
previous stage left behind — skip one and the ambiguity just shows up later, more expensively, during build or UAT.
The end-to-end job this completes is "turn scattered stakeholder input into something a team can build against and
be measured against" — it's the right skill when nothing built yet has been agreed to, not when you already have a
requirements doc and just need one section tightened.

## Stages

1. **Gather raw input** — interviews, notes, existing tickets, support logs
   No dedicated atomic skill; this is data collection. Capture verbatim quotes and specific examples, not
   paraphrased summaries — paraphrasing at this stage loses the detail later stages need, and a requirement traced
   back to "users said X" is far more defensible later than one traced to "the team felt X."
   **Gate to proceed:** you have input from more than one source/stakeholder (single-source requirements tend to
   encode one person's assumptions as fact) and at least a few concrete examples, not just opinions.

2. **Map as-is / to-be gap** — `talwar-pm-state-documentation-skill`
   Document the current state precisely, the desired future state, and the specific gap between them. This stage
   is what turns "the process is broken" into something you can actually scope.
   **Gate to proceed:** the gap is stated as a concrete difference (a process step that doesn't exist, a data field
   that isn't captured) — not as a vague pain point like "the current process is inefficient."

3. **Draw scope boundaries** — `talwar-pm-scope-definition-skill`
   Decide what's in and out for this effort specifically, separate from the full to-be vision — the to-be state
   from stage 2 is usually bigger than what any single effort should attempt at once.
   **Gate to proceed:** there's an explicit in/out line reviewed by the requester — if everything from stage 2's
   to-be state is "in scope," this stage hasn't actually happened yet.

4. **Write the requirements doc** — `talwar-pm-spec-for-ai-agents-skill` if the build target is an AI coding agent, otherwise a
   general requirements/PRD document at the same rigor
   Translate the bounded scope into inputs/outputs, interfaces, and behavior specific enough to build from. The
   choice of technique here matters: a literalist AI agent needs the extra boundary conditions and non-goals that
   `talwar-pm-spec-for-ai-agents-skill` forces, while a human team can work from a lighter document that leans on shared context.
   **Gate to proceed:** a reader unfamiliar with the original interviews could implement (or clearly know what to
   ask) from the document alone.

5. **Define acceptance and get sign-off** — `talwar-pm-verification-uat-skill`
   Write the test scenarios and acceptance criteria that will be used to confirm the build matches the requirement,
   and route for formal sign-off. Sign-off belongs here, on the testable scenarios, rather than on the prose
   requirements — a stakeholder who signs off on paragraphs can still disagree later about what those paragraphs
   meant in practice.
   **Gate to proceed:** the stakeholder(s) who requested this have explicitly signed off on the acceptance
   scenarios themselves, before build starts — not just on the prose requirements.

## Sequencing notes

- Stages 1-3 are strictly sequential — you cannot bound scope (stage 3) before you know the gap (stage 2), and you
  cannot know the gap before you've gathered more than one perspective (stage 1). Trying to compress these into one
  pass usually means scope gets bounded around whoever spoke loudest in stage 1, not around the actual gap.
- Stage 4's choice of technique depends on stage 3's output, but once chosen, stages 4 and 5 can partially overlap:
  drafting acceptance scenarios alongside the requirements doc often surfaces gaps in the doc itself, which is a
  feature, not a sequencing violation — just don't route either for sign-off until both are internally consistent.
  Treat any acceptance scenario that can't be written cleanly as a signal the requirements doc still has a gap.
- **The most common skipped stage is #3 (scope definition)** — teams move straight from gap analysis to writing
  requirements, because the gap already feels bounded in someone's head. What breaks downstream: without an
  explicit in/out line, the requirements doc silently expands to cover the full to-be vision, which then fails
  acceptance testing (stage 5) not because the build was wrong but because it was never scoped to what stage 5 is
  testing against.
- A related trap at stage 4: writing the requirements doc before deciding who's building it. The rigor a human
  team needs and the rigor an AI coding agent needs are different in kind, not just degree — deciding late means
  redoing stage 4's work once the build target becomes clear.

## Final output

A signed-off requirements package: the as-is/to-be gap summary (stage 2), the explicit scope boundary (stage 3),
the requirements/spec document (stage 4), and the acceptance test scenarios with stakeholder sign-off (stage 5) —
handed to the delivery team as the agreed contract for what "done" means. This package should be self-contained
enough that a build team, or an AI coding agent, can start from it without needing to re-run the original
interviews to resolve ambiguity.

## Quality checklist

- [ ] Does the final requirements doc trace every requirement back to a specific gap or interview finding, not a
      general aspiration?
- [ ] Is the in/out scope boundary explicit enough that a new stakeholder joining late couldn't argue for scope
      creep by pointing to the to-be vision?
- [ ] Has sign-off happened on the acceptance criteria specifically, not just on the narrative requirements prose?
- [ ] Could someone hand this package to a different team/agent and get a comparable build without re-interviewing
      the original stakeholders?
- [ ] If the build target is an AI coding agent, does the requirements doc name explicit non-goals and edge-case
      handling rather than assuming an engineer's judgment will fill the gaps?
