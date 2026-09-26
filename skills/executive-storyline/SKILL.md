---
name: executive-storyline
description: Structure a board deck, exec update, or strategy narrative using the Pyramid Principle and SCQA so a time-constrained executive gets the point in the first slide, not the last. Use whenever the user is preparing a board-ready deck, exec narrative, or "tell the story of" a project, or when a draft reads as a chronology ("first we did X, then Y, then Z") and needs restructuring around the actual argument.
---

# Executive Storyline

## Why this matters

Chronology is the natural way humans tell stories and the wrong way to brief executives. "First we investigated,
then we found this, then we tried that, and eventually we recommend..." forces the reader to hold the whole story
in memory to reach the punchline — and a reader with six minutes before the next meeting will skim for the
punchline and miss the argument entirely. Barbara Minto's Pyramid Principle inverts this: state the governing
thought first, then let the reader descend into supporting arguments only as deep as they need to verify it. The
narrative isn't dishonest for skipping the journey — it's structured for how someone under time pressure actually
reads.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed without asking):

- **The single governing thought** — if you can't state the one-sentence conclusion yet, get that clear before
  structuring anything else
- **The audience** and what they already believe or are skeptical of — this shapes the Complication in SCQA
- **The supporting arguments** currently in hand (data, project history, evidence) — raw material to group, not to
  present in the order it happened
- **Time/format constraint**: a 5-slide exec update and a 40-slide board deck use the same spine, different depth
- **Any decision this narrative needs to drive** — a storyline that isn't in service of a decision or belief change
  tends to drift back into chronology

## Process

1. **Find the governing thought.** One sentence that is the entire point — if a reader saw only this sentence, what
   would they need to know? Everything else in the pyramid exists to support or explain this sentence.
2. **Open with SCQA**, not a chronology:
   - **Situation**: the stable, agreed-upon context (short — this is not where the tension lives)
   - **Complication**: what changed or what's at risk — the reason this narrative exists at all
   - **Question**: the question the Complication raises in the reader's mind
   - **Answer**: the governing thought — your answer to that question
3. **Group supporting arguments beneath the governing thought**, and make each grouping MECE (Mutually Exclusive,
   Collectively Exhaustive) — no argument sits in two groups, and no obvious counter-argument is left ungrouped
   and therefore looking dodged.
4. **Order groupings by what the reader needs to believe first**, not by when you did the work. Usually: why this
   matters, what we found, what we recommend, what it costs/risks — but let the audience's skepticism dictate order,
   not your project timeline.
5. **Descend only as deep as evidence requires.** Each supporting point should be provable with one level below it
   (a chart, a data point, a named example) — if a reader wants to go deeper, the appendix is there; the main
   narrative stops at "trust me, and here's why in one line."
6. **Delete the journey.** The fact that you tried three things before finding the right one is process, not
   argument — it belongs in an appendix or nowhere, unless the failed attempts are themselves evidence for the
   governing thought.

## Output template

```markdown
# [Narrative title stating the governing thought, not the topic]

## Opening (SCQA)
- **Situation:** [stable context, 1-2 sentences]
- **Complication:** [what changed / what's at risk]
- **Question:** [the question this raises]
- **Answer / Governing thought:** [your one-sentence conclusion — this is the headline of everything below]

## Supporting argument 1: [MECE grouping name]
[The claim, then 1-3 pieces of evidence — data, example, quote]

## Supporting argument 2: [MECE grouping name]
[...]

## Supporting argument 3: [MECE grouping name]
[...]

## So what (recommendation / ask)
[What we want the reader to decide or believe, restated plainly — link to `decision-memo` if this needs a formal ask]

---
*Appendix: [detailed data, methodology, the "how we got here" journey for anyone who wants it]*
```

## Quality checklist

- [ ] Can you delete every slide/section except the opening and still have the reader know your conclusion?
- [ ] Do the supporting groupings pass MECE — no argument in two buckets, no obvious rebuttal left unaddressed?
- [ ] Is the order of groupings driven by what the skeptical reader needs to believe next, not by project chronology?
- [ ] Does the Complication actually create tension, or does it just restate the Situation more urgently?

## Related skills

- Turn the "so what" into a single approvable ask: `decision-memo`
- Build the MECE argument structure this narrative sits on top of: `issue-tree`
- Ground the narrative in a market/competitive picture: `market-research`
