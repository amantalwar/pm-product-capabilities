---
name: talwar-pm-discovery-to-backlog-skill
description: Run the full multi-stage journey from a validated product idea to a sprint-ready backlog — this is a multi-stage workflow for the larger end-to-end job, not a single technique, so use it for broader asks like "take this idea from discovery to backlog," "get this ready for the team to build," or "help me go from idea to sprint-ready," rather than a single narrow request like "just prioritize this list" or "just write these stories."
---

# Discovery to Backlog

## What this orchestrates

This is a sequence, not a single technique: it takes a raw product idea through validation, insight-building,
shaping, prioritization, and story-writing, ending in a backlog engineering can actually pull from. Each stage
produces an artifact the next stage consumes — skipping a stage means the next one is working from guesses instead
of evidence. The end-to-end job this completes is "turn a hunch into a sprint," and it's meant for the moment a
team has an idea worth pursuing but nothing yet that a sprint could start against — not for touching up a backlog
that already exists.

## Stages

1. **Validate the idea** — `talwar-pm-product-discovery-skill`
   Test the idea's core assumptions (desirability, viability, feasibility) before investing further. This is
   deliberately cheap and fast — a handful of user conversations, a landing-page test, a look at existing usage
   data — because everything downstream gets more expensive to redo the later a bad idea is caught.
   **Gate to proceed:** at least the riskiest assumption has been tested with real signal (user conversations,
   a smoke test, existing data) — not just internal conviction. If the idea fails validation, stop here; don't
   carry an unvalidated idea into shaping. A "we think this is promising but haven't checked" is not a pass.

2. **Build insight** — `talwar-pm-market-research-skill` and/or `talwar-pm-customer-journey-mapping-skill`
   Deepen the picture of who this is for, what alternatives they use today, and where in their journey the problem
   actually bites. Market research answers "how big and how competitive is this space"; journey mapping answers
   "where exactly does the friction happen and how painful is it relative to everything else in that journey."
   **Gate to proceed:** you can name the specific user segment and the specific moment in their journey this
   addresses — not "users want this," but "users in situation X, at step Y, currently do Z instead."

3. **Shape into a walking skeleton** — `talwar-pm-feature-story-mapping-skill`
   Map the end-to-end user journey through the new capability and organize it into release-sized slices, with a
   thin "walking skeleton" that proves the whole path works before adding depth. The skeleton should touch every
   step of the journey shallowly rather than perfecting one step and leaving others unbuilt.
   **Gate to proceed:** there's an agreed walking skeleton slice that is small enough to ship first and still
   demonstrates real user value end-to-end.

4. **Rank** — `talwar-pm-prioritization-matrix-skill`
   Score the shaped slices/features against value and effort (or the framework that fits — RICE, ICE, value/effort)
   to decide what actually goes first. This stage exists specifically to resist the temptation to build everything
   from the story map in the order it was drawn.
   **Gate to proceed:** there's a ranked list with an explicit cutline — what's in the next release vs. explicitly
   deferred, not just a sorted list nobody drew a line on.

5. **Write INVEST stories** — `talwar-pm-backlog-management-skill`
   Turn the top-ranked slice into Independent, Negotiable, Valuable, Estimable, Small, Testable stories with
   acceptance criteria. Only the slice(s) above the cutline from stage 4 get written up in full — don't
   pre-write stories for deferred work just because the story map already implies them.
   **Gate to proceed:** every story in the next sprint's candidate set meets Definition of Ready — acceptance
   criteria written, dependencies called out, sized small enough to estimate confidently.

## Sequencing notes

- Stages 1-2 are sequential (you can't build insight into a segment before you know the idea is worth pursuing at
  all), but stage 2's two techniques (`talwar-pm-market-research-skill` and `talwar-pm-customer-journey-mapping-skill`) can run in parallel if you
  have resourcing for both.
- Stages 3-5 are strictly sequential — story-writing before ranking produces beautifully written stories for
  features that shouldn't ship yet, and ranking before shaping ranks vague ideas instead of real slices. Each of
  these three stages depends on a concrete artifact from the one before it (a slice, then a rank, then a story),
  so reordering them isn't a shortcut, it's redoing the work with less information.
- **The most common skipped stage is #2 (insight-building)** — teams go straight from "the idea tested okay" to
  story-mapping because discovery felt like enough validation. What breaks downstream: story-mapping without a
  specific segment/journey moment produces a feature that solves the idea in the abstract but misses the actual
  friction point, which surfaces expensively after launch rather than cheaply in discovery.
- A second, smaller trap: running stage 4 (ranking) against the whole story map instead of against release-sized
  slices from stage 3. Ranking individual stories before they're grouped into a coherent walking skeleton produces
  a backlog that's internally ranked but doesn't hang together as a shippable release.

## Final output

A backlog folder/doc set containing: the discovery validation summary (stage 1), the insight brief naming
segment + journey moment (stage 2), the story map with the walking skeleton and release slices marked (stage 3),
the ranked/cutlined feature list (stage 4), and the sprint-ready story set with acceptance criteria meeting
Definition of Ready (stage 5) — handed to the team as the single source of truth for what gets built first and why.
Anyone joining the effort mid-stream should be able to open this set and answer, without asking around: what
problem is this, for whom, why this slice first, and what "done" looks like for the next sprint.

## Quality checklist

- [ ] Does every story in the final backlog trace back to a validated assumption and a named segment/journey
      moment, rather than floating free of the earlier stages?
- [ ] Is there an explicit cutline showing what's deferred, not just an unordered "everything we thought of" list?
- [ ] Would a new engineer joining the team be able to read the story map and understand the walking skeleton
      without a verbal explanation?
- [ ] Has at least one stage gate been visibly checked off (not silently skipped) before moving to the next?
- [ ] If the idea failed validation at stage 1, was the workflow actually stopped there rather than pushed
      forward on momentum?
