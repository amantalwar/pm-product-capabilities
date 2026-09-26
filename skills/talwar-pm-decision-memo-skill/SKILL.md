---
name: talwar-pm-decision-memo-skill
description: Write a one-page executive memo built to get a Yes / No / Modified decision, not to inform or impress. Use whenever the user needs to ask an executive or committee to approve, fund, or greenlight something, says "I need to get sign-off on," "write this up for the steering committee," or has a decision stuck in limbo because nobody has forced the actual ask onto one page.
---

# Decision Memo

## Why this matters

A memo that asks for three things gets zero decisions. Executives don't reject well-argued memos — they set them
aside, because a memo with multiple asks forces the reader to do the prioritization work the writer should have
done. The single biggest failure mode isn't weak analysis; it's an unclear or compound ask buried after three pages
of context the reader has to wade through to even find out what's being requested. A decision memo exists to make
saying "yes" (or a clean "no") the path of least resistance for a time-constrained reader who may only read the
first paragraph.

## Gather inputs first

Before drafting, get (ask if not given, and make a reasonable assumption out loud if told to proceed without asking):

- **The exact decision** you need made — phrased as a question with a Yes/No/Modified answer space, not a topic
- **Who decides** (one person, a committee) and what they already know or don't about the background
- **The recommendation** you're making, even if the user hasn't fully committed to it yet — a memo without a stated
  recommendation isn't a decision memo, it's a briefing
- **The real alternatives considered** and why they lost, so the ask doesn't look like a false binary
- **The cost of delay** — what happens if this decision doesn't get made this week

## Process

1. **State the ask as one sentence, one decision.** If there are genuinely three decisions, write three memos or
   pick the one that unblocks the other two. A memo that asks for budget AND headcount AND a timeline extension
   will get none of the three approved cleanly.
2. **Lead with the recommendation, not the analysis.** Bottom-line-up-front (BLUF): the first paragraph should let a
   reader who stops there still know what's being asked and what you recommend. Analysis exists to let a skeptical
   reader check your reasoning — it is not the thing being delivered.
3. **Name the real alternatives and why they lost**, in one line each. This pre-empts the most common derailment:
   an exec proposing an option you already considered and rejected, restarting the conversation from zero.
4. **State the cost of each answer** — cost of doing it, cost of not doing it, cost of delaying the decision itself.
   A "no cost to waiting" framing is why decisions rot in inboxes.
5. **Make the ask literally answerable in the room.** End with the decision restated plus what you need from the
   reader specifically (an email reply, a signature, a verbal yes in the meeting) — don't make them infer the next
   step.
6. **Cut anything that doesn't serve the decision.** Interesting context that doesn't change the Yes/No calculus
   belongs in an appendix or nowhere, not in the one page that's supposed to get read.

## Output template

```markdown
# Decision needed: [one-sentence question with a Yes/No/Modified answer]

**Ask:** [Exactly what you need approved, funded, or greenlit — one sentence]
**Recommendation:** [Your recommended answer, stated plainly]
**Decide by:** [Date] — because [cost of delay in one clause]

## Why
[2-4 sentences: the situation and why this decision matters now]

## Recommendation and reasoning
[The recommended path, with the 2-3 supporting reasons that matter most — not everything you know]

## Alternatives considered
| Option | Why not |
|---|---|
| [Alternative 1] | [1 line] |
| [Alternative 2] | [1 line] |

## Cost of each answer
- **If yes:** [cost/commitment]
- **If no:** [what we lose or keep doing instead]
- **If we wait:** [concrete cost of delay, not "opportunity cost" hand-waving]

## What I need from you
[The literal action: approve via reply, sign, say yes in Thursday's meeting]

---
*Appendix (optional, not required reading): [supporting data, detailed analysis, links]*
```

## Quality checklist

- [ ] Is there exactly one decision being asked for, phrased as a question with a clean answer space?
- [ ] Does the first paragraph alone tell the reader what's being asked and what you recommend?
- [ ] Are the rejected alternatives named specifically enough that "why didn't we just do X" is already answered?
- [ ] Is the cost of delay concrete (a number, a date, a missed window) rather than asserted?

## Related skills

- Structure the surrounding narrative for a bigger audience: `talwar-pm-executive-storyline-skill`
- Choose between the alternatives before writing the ask: `talwar-pm-decision-framework-skill`
- Justify the investment behind a larger ask: `talwar-pm-business-case-skill`
