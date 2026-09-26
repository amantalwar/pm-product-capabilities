---
name: talwar-pm-spec-for-ai-agents-skill
description: Write a specification meant to be implemented by an AI coding agent (Claude Code, Cursor, Copilot Workspace, Devin) rather than a human engineer. Use whenever the user wants a spec, PRD, or ticket that Claude or another AI agent will build directly, asks "write this up so Claude Code can implement it," is about to hand a feature to an agent and worried about scope creep, or says something got built "technically right but not what I meant."
---

# Spec for AI Agents

## Why this matters

A spec written for a senior human engineer works because of everything it doesn't say. The engineer fills gaps with
tacit judgment: they know "add a delete button" implies a confirmation dialog, that "support pagination" implies
sane defaults, that an edge case you didn't mention should probably fail gracefully rather than crash. An AI coding
agent has no tacit judgment to fall back on — it will implement the literal words, including the parts you didn't
mean literally, and it will do it fast and confidently enough that the gap doesn't surface until code review. The
failure mode isn't the agent being "dumb"; it's the spec being underspecified in a way that never mattered before
because a human always silently patched the holes. Treat this skill as writing boundary conditions an agent cannot
accidentally wander outside of, not as writing more prose.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed without asking):

- **The literal feature request** in the requester's own words — you'll compare this against the final scope to
  catch drift
- **Which agent will implement it** (Claude Code against a real repo, a greenfield prototype, a no-code tool) —
  this changes how much interface detail you need to pin down
- **What already exists**: current code, schemas, API contracts, design system components the agent must reuse
  rather than reinvent
- **Who reviews the output** and what "done" looks like to them (tests passing, a PR, a working demo)
- **Known ambiguous spots** the requester already senses might be read multiple ways

## Process

1. **Write the literal problem statement first**, then read it back as a strict literalist would. Anywhere a
   reasonable human would silently disambiguate, an agent won't — flag that spot for explicit resolution.
2. **Draw exact scope boundaries.** Not "what to build" in prose, but a bounded list: which files/modules/screens
   are in play, which are untouchable, what the agent is and is not allowed to refactor along the way.
3. **Write explicit non-goals.** State the adjacent things this spec is deliberately NOT asking for — the things an
   eager agent will "helpfully" add anyway (extra validation, a settings toggle, a migration) unless told not to.
4. **Define inputs, outputs, and interfaces precisely**: function signatures, request/response shapes, error types,
   states a UI component can be in. An agent will invent a shape if you don't give it one, and that invented shape
   becomes the de facto contract everything downstream builds against.
5. **Write acceptance criteria as tests, not adjectives.** "Handles errors gracefully" is not testable; "on a 404
   from the pricing endpoint, render the cached price with a stale-data badge" is. Every criterion should be
   something a reviewer (human or automated) can check true/false.
6. **Enumerate the edge cases you already know about** and say exactly what happens in each — empty states, zero
   items, concurrent edits, network failure, permission denial. If you don't know the right behavior, say
   "ask/flag rather than guess" explicitly rather than leaving it silent.
7. **Add an "if ambiguous, do X not Y" section.** This is the section unique to agent specs: for the 2-3 places
   still most likely to be misread, state the default resolution directly instead of trusting inference.

## Output template

```markdown
# Spec: [Feature name]

## Problem
[1-3 sentences: what's broken or missing, for whom, stated as literally as possible]

## In scope
- [Exact files/modules/screens/endpoints the agent should touch]

## Explicitly out of scope (non-goals)
- [Adjacent thing the agent should NOT build, even if it seems related]
- [...]

## Inputs, outputs, interfaces
- **Inputs**: [exact shape — types, required/optional fields, source]
- **Outputs**: [exact shape — response schema, UI states, side effects]
- **Interfaces touched**: [existing functions/components/APIs to reuse, not reinvent]

## Acceptance criteria (testable)
- [ ] [Specific, checkable behavior #1]
- [ ] [Specific, checkable behavior #2]
- [ ] [...]

## Edge cases and how to handle them
| Edge case | Expected behavior |
|---|---|
| [e.g., empty input list] | [exact behavior, not "handle appropriately"] |
| [e.g., concurrent update] | [...] |

## If ambiguous, do X not Y
- If [likely misreading #1], do [specific default] — not [the tempting wrong interpretation].
- If [likely misreading #2], do [specific default] — not [...].
- If something isn't covered above and matters for correctness, stop and ask rather than guessing silently.
```

## Quality checklist

- [ ] Could a literalist agent implement exactly what's written and produce something the requester didn't want?
      If yes, keep tightening.
- [ ] Does the non-goals section name at least one thing an eager agent would plausibly add unasked?
- [ ] Is every acceptance criterion phrased so a reviewer can mark it true/false without judgment calls?
- [ ] Does at least one edge case explicitly say what to do when the right behavior is unknown ("ask, don't guess")?

## Related skills

- Turn raw stakeholder interviews into this level of precision: `talwar-pm-requirements-definition-skill`
- Validate the delivered build actually meets these criteria: `talwar-pm-verification-uat-skill`
- If the ask is still fuzzy before you can spec it, decompose it first: `talwar-pm-issue-tree-skill`
