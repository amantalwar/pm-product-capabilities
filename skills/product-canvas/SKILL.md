---
name: product-canvas
description: Condense an entire product's strategic definition onto a single page — problem, target users, value proposition, differentiators, success metrics, key risks. Use when the user wants a one-pager for a whole product (not one initiative or feature), needs to brief a new hire or exec on "what is this product, actually," or asks for a product overview/summary they can hand around without a 20-page strategy doc.
---

# Product Canvas

## Why this matters

A product canvas exists because most people who need to understand a product's strategic shape don't need — and
won't read — the full strategy deck, and shouldn't have to reconstruct it from a roadmap tool. It forces the same
discipline as the vision statement (falsifiable, specific, no filler adjectives) but at product scope: broad enough
to cover everything the product does, tight enough to fit on one page without becoming a table of contents. The
scope boundary is what most people get wrong, so get it right here: this is narrower than a business model canvas
(which is about revenue mechanics and business architecture — how the thing makes money and what it costs to run)
and broader than an initiative canvas (which is about one bet within the product — one feature, one experiment).
A product canvas answers "what is this product and why does it deserve to exist," not "how do we monetize it" or
"what are we building this quarter." When those three documents get confused, teams end up with an initiative
canvas trying to justify a whole product, or a product canvas cluttered with pricing-tier details that belong in
the business model canvas — this skill's job is to keep the altitude right.

## Gather inputs first

Ask if missing (assume and state the assumption if told to proceed):

- **The product** this canvas is for — confirm it's product-level scope, not one feature or initiative (if the
  user actually means one initiative, redirect to `initiative-canvas`)
- **Current target users/segments**, even if imperfectly defined
- **What exists today** — is this a canvas for a live product (grounded in real usage/metrics) or a not-yet-built
  one (grounded in a hypothesis)? This changes how confidently the metrics and differentiators can be stated
- **Any existing strategy/vision material** to stay consistent with

## Process

1. **State the problem/opportunity as something real, not a restatement of the solution.** "Users can't find the
   right file across 5 disconnected tools" is a problem; "we need a unified search product" is the solution wearing
   a problem's clothes — write the former.
2. **Name target users specifically enough to exclude someone.** "Everyone who uses documents" isn't a target user
   segment — it's a refusal to choose one. A real target-user statement should make it obvious who this product is
   NOT for.
3. **Write the value proposition as a change for the user, not a features list.** One or two sentences: what the
   user can do now that they couldn't before, and why that matters to them.
4. **Name differentiators that are actually defensible**, not just true. "We have a clean UI" is true of every
   competitor's marketing page too. A real differentiator survives the question "why can't a competitor just copy
   this next quarter" — because it's structural (data advantage, integration depth, distribution) not cosmetic.
5. **Pick success metrics that would actually move if the value proposition is real** — not vanity metrics (signups,
   page views) unless they're a genuine leading indicator for this product specifically.
6. **Name key risks as things that could specifically invalidate this canvas** — not generic ("execution risk") but
   tied to an assumption this canvas depends on (e.g., "value prop assumes users will change a 10-year habit;
   unvalidated").
7. **Check the altitude.** If a line item reads like it belongs in a pricing/revenue model, move it to
   `business-model-canvas`. If a line item is really about one feature or one experiment, it belongs in
   `initiative-canvas`, not here.

## Output template

```markdown
# Product Canvas: [Product name]

## Problem / opportunity
[The real problem this product addresses — not a restatement of the solution]

## Target users
[Specific enough that it's obvious who this is NOT for]

## Value proposition
[1-2 sentences: what changes for the user]

## Key differentiators
1. [Structural advantage — why a competitor can't just copy this next quarter]
2. [...]
3. [...]

## Success metrics
| Metric | Current (if live) | Target | Why this metric (not a vanity proxy) |
|---|---|---|---|
| | | | |

## Key risks
| Risk | What assumption it threatens | How/when we'd know it materialized |
|---|---|---|
| | | |

## Explicitly out of scope for this product
[What this product deliberately does not try to do — the flip side of the target-user boundary above]
```

## Quality checklist

- [ ] Does the target-user line make it obvious who this product is NOT for?
- [ ] Would each differentiator survive "why can't a competitor copy this next quarter"?
- [ ] Are the success metrics tied to the value proposition, not generic vanity metrics?
- [ ] Is anything about pricing/revenue mechanics moved out to `business-model-canvas` rather than left in here?
- [ ] Is anything about a single feature/experiment moved out to `initiative-canvas` rather than left in here?

## Related skills

- Zoom in to one bet within this product: `initiative-canvas`
- Zoom out to revenue mechanics and business architecture: `business-model-canvas`
- Build the fuller narrative this canvas summarizes: `vision-strategy`
- Turn the success metrics into tracked targets: `okrs-metrics`
