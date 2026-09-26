---
name: talwar-pm-market-research-skill
description: Run a competitive analysis or synthesize customer/market insights — competitor teardowns, "how do we compare to X," win/loss patterns, or pulling signal out of reviews and support tickets. Use for requests like "analyze our top 3 competitors," "what are customers saying about us vs them," or "build a market landscape" — even when the user just says "can you look into what else is out there."
---

# Market Research

## Why this matters

Most competitive decks are a features table copy-pasted from marketing pages, which tells you what competitors claim,
not what's true or what customers experience. The useful version of this skill separates three different things that
get flattened together: what a competitor **says** about itself (positioning, pricing page), what it **actually
does** (product teardown, trial signup), and what its **customers say** about it (reviews, forums, churn reasons).
The gap between those three is where the real insight lives — a competitor whose marketing promises "enterprise-grade
reliability" while G2 reviews cite constant outages is a specific, exploitable finding; a features checklist is not.

## Gather inputs first

Ask if not given (assume and state the assumption if told to proceed):

- **Question being answered** — "should we build X," "why are we losing deals to Y," "is there room for a new
  entrant" — the research plan differs a lot by question
- **Named competitors** or, if none named, the category/segment to scan for likely ones
- **Primary research available**: sales call notes, lost-deal reasons, support tickets, existing customer
  interviews — anything first-party beats anything scraped
- **Secondary sources in scope**: review sites (G2, Capterra), competitor pricing pages, app store reviews, public
  changelogs, job postings (signal for where a competitor is investing)
- **Time budget** — a 2-hour scan and a 2-week study produce structurally different outputs; don't pad a quick scan
  to look like deep research

## Process

1. **Split primary from secondary research explicitly.** Primary = data from your own customers/prospects (interviews,
   sales notes, support logs). Secondary = published/third-party material (competitor sites, review aggregators,
   analyst reports). Secondary research tells you the landscape; primary research tells you why you actually win or
   lose deals. Lead with primary wherever it exists.
2. **For each competitor, teardown across four lenses**, keeping sources attached to each claim:
   - **Positioning** — their stated ICP, category claim, and headline value prop (from their own site/materials)
   - **Pricing & packaging** — tiers, what's gated behind enterprise, list price vs. what deals actually close at if
     known
   - **Feature set** — what's actually shipped and usable (sign up for a trial where possible), not just claimed
   - **Reviews & complaints** — pull recurring themes from G2/Capterra/app stores/forums, weighted by recency
     (a 2023 complaint about a bug that's since shipped a fix is stale signal)
3. **Separate "what they say" from "what customers experience"** for every competitor. A pricing page says
   "unlimited"; a review says "we hit a hard cap and support wouldn't budge." Flag contradictions — they're usually
   the sharpest insight in the whole doc.
4. **Look for the pattern across complaints, not just the loudest one.** Three reviews mentioning slow onboarding is
   a trend; one angry one-star review is an outlier. Weight by frequency, not vividness.
5. **Translate findings into implications**, not just facts. "Competitor X has no mobile app" is a fact. "Competitor
   X has no mobile app and 40% of their negative reviews mention needing to work from a phone" is an implication you
   can act on.
6. **Name what you don't know.** If trial access was blocked, pricing wasn't public, or reviews were sparse, say so —
   a confident-sounding gap is worse than an honest "unverified."

## Output template

```markdown
# Market Research: [Topic/Question]

## Question this research answers
[1-2 sentences]

## Sources used
- Primary: [interviews, sales notes, support tickets — with dates/counts]
- Secondary: [review sites, competitor pages, reports — with dates]

## Competitor teardown
### [Competitor name]
- **Positioning** (their claim): [...]
- **Pricing/packaging**: [...]
- **Feature set** (verified, not claimed): [...]
- **Reviews/complaints** (recurring themes, with rough frequency): [...]
- **Say vs. experience gap**: [where their marketing and their customers disagree]

[Repeat per competitor]

## Cross-competitor patterns
- [Pattern observed across 2+ competitors, with implication]

## What this means for us
- [Implication 1 — specific, actionable]
- [Implication 2]

## Confidence & gaps
- [What's well-evidenced vs. assumed; what needs more research]
```

## Quality checklist

- [ ] Every competitor claim is tagged as "their claim" or "verified/observed" — never blended
- [ ] At least one finding comes from customer-facing sources (reviews/complaints), not just competitor marketing
- [ ] Patterns are backed by frequency ("recurring across N reviews"), not a single anecdote treated as a trend
- [ ] The doc states what wasn't verifiable rather than presenting guesses as findings
- [ ] Each finding ends in an implication, not just a fact

## Related skills

- Turn findings into a sales-facing comparison: `talwar-pm-stakeholder-communication-skill` for internal readout, or a positioning doc via `talwar-pm-go-to-market-skill`
- Feed validated pain points into `talwar-pm-product-discovery-skill` before committing to a solution
- Use `talwar-pm-customer-journey-mapping-skill` to place competitive gaps at the stage where they actually bite
- Rank which competitive gaps to act on first: `talwar-pm-prioritization-matrix-skill`
