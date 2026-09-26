---
name: talwar-pm-feature-story-mapping-skill
description: Build a user story map to find a coherent MVP slice — backbone activities, steps beneath them, and prioritized rows. Use for "map out the user journey into stories," "what's the minimum we need to ship," "help me find our MVP," or "break this feature down into a backlog" when the goal is a walking skeleton, not just a flat list of tickets.
---

# Feature Story Mapping

## Why this matters

A flat backlog sorted by priority hides the thing that matters most: whether the top N tickets, taken together,
form something a user could actually complete end to end. You can build the ten highest-priority stories in a flat
list and still ship something with no coherent path through it — great login, great settings page, no way to
actually finish the core task. Jeff Patton's story mapping method fixes this by keeping the user's narrative flow
(the backbone) visible at all times, so prioritization happens as horizontal slices across that flow rather than
vertical cherry-picking. The MVP isn't "the most important individual stories" — it's the thinnest complete slice
across the whole backbone, the walking skeleton that lets a real user go from start to finish, however roughly.

## Gather inputs first

Ask if not given (assume and state it if told to proceed):

- **The user journey in scope** and the persona doing it (map one persona's flow at a time — mixing personas
  produces a backbone that doesn't narrate anyone's actual experience)
- **Existing research or journey map** to ground the backbone in real behavior rather than an assumed flow (link to
  `talwar-pm-customer-journey-mapping-skill` output if one exists)
- **Current backlog**, if one exists, to mine for steps/details rather than starting from zero
- **MVP constraint**: timebox, team size, or a specific "must be true by X date" that bounds how thin the walking
  skeleton needs to be

## Process

1. **Build the backbone first**: the user's activities in narrative left-to-right order — the big verbs of what
   they're trying to accomplish (e.g. "Find a product," "Configure it," "Check out," "Track the order"). This is a
   story, not a sitemap — read it aloud and it should describe what someone does, in order.
2. **Add steps beneath each activity**: the specific tasks that make up that activity, still in roughly the order
   a user would do them. This is still structural — not yet prioritized, just decomposed.
3. **Write stories beneath each step**: the actual candidate backlog items, in user-story form, that could
   accomplish that step at varying levels of sophistication.
4. **Arrange stories into rows by priority/sophistication**, top row = the simplest version that still lets the user
   complete that step, lower rows = more sophisticated versions added later. This turns the map into a 2D grid:
   backbone across the top, depth of capability going down.
5. **Slice horizontally to find the walking skeleton.** The MVP slice is the top row across the *entire* backbone —
   the crudest version of every step, strung together — not the top N stories regardless of which step they belong
   to. If a slice has gaps (an activity with no simple version selected), the user hits a dead end; fill the gap
   before adding sophistication elsewhere.
6. **Name the release slices below the MVP explicitly** (Release 2, Release 3), so "not in MVP" doesn't silently
   mean "forgotten" — the map should show the whole roadmap's shape, not just the first cut.

## Output template

```markdown
# Story Map: [Product/Feature] — [Persona]

## Backbone (user activities, left to right)
[Activity 1] → [Activity 2] → [Activity 3] → [Activity 4]

## Steps and stories
### [Activity 1]
Steps: [Step 1a] | [Step 1b] | [Step 1c]

| Row | [Step 1a] | [Step 1b] | [Step 1c] |
|---|---|---|---|
| MVP (top row) | [story] | [story] | [story] |
| Release 2 | [story] | [story] | [story] |
| Release 3 | [story] | [story] | [story] |

[Repeat structure per activity]

## Walking-skeleton MVP slice
[Confirm the top row is complete across every activity with no gaps — list the full set of stories that make up
the MVP release]

## Release plan
- **Release 1 (MVP)**: [stories] — lets the user [complete the full journey, crudely]
- **Release 2**: [stories] — adds [what sophistication]
- **Release 3**: [stories] — adds [...]

## Gaps / open questions
[Any step with no viable "simplest version" yet identified]
```

## Quality checklist

- [ ] The backbone reads as a narrative of user activities, not a list of app features or screens
- [ ] The MVP slice has no gaps — every backbone activity has at least a crude version included
- [ ] Stories are written in user-story form, not as internal technical tasks
- [ ] Rows below the MVP are named and kept visible, not dropped once the MVP is chosen
- [ ] The map was built from real user research where available, not solely from internal assumption

## Related skills

- Ground the backbone in real customer behavior first: `talwar-pm-customer-journey-mapping-skill`
- Turn the MVP slice into INVEST-quality tickets: `talwar-pm-backlog-management-skill`
- Rank stories within a row when there are too many candidates: `talwar-pm-prioritization-matrix-skill`
- Scope the MVP release formally: `talwar-pm-scope-definition-skill`
