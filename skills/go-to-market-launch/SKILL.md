---
name: go-to-market-launch
description: Run the full multi-stage GTM launch orchestration — strategy, pricing, risk-testing, internal alignment, launch day, and post-launch measurement — this is a multi-stage workflow for the larger end-to-end job, so use it for broader asks like "help me run this whole launch," "take this from GTM strategy to launch day," or "get us ready to actually ship this to market," not a single narrow ask like "just write the positioning" or "just check our pricing," which should use the standalone `go-to-market` skill instead.
---

# Go-to-Market Launch

## What this orchestrates

This is the full end-to-end version of the standalone `go-to-market` strategy skill: it doesn't stop at a written
strategy, it carries the launch through pricing decisions, a pre-mortem risk pass, internal stakeholder alignment,
launch-day execution, and a post-launch check against the plan. Use the standalone `go-to-market` skill alone when
someone just needs the strategy document; use this workflow when the ask is the whole launch, start to finish —
the job this completes is "get this thing safely into the market and know whether it worked," not "write the
positioning deck."

## Stages

1. **Strategy and positioning** — `go-to-market`
   Define the target segment, positioning, messaging, and channel plan. Everything downstream — pricing, risk,
   internal messaging — reacts to what gets decided here, so treat this as the load-bearing stage even though it's
   only the first one.
   **Gate to proceed:** the strategy names a specific beachhead segment and a differentiated message — not a
   generic "we're launching to everyone" plan.

2. **Pricing and monetization (if applicable)** — `pricing-monetization-strategy`
   Set or validate the price point and packaging against the positioning from stage 1.
   **Gate to proceed:** the price/packaging has been checked against at least one real willingness-to-pay signal
   (comparable, research, or a pricing test) — not set by gut feel alone. Skip this stage entirely if the launch
   involves no new pricing decision, and say so explicitly rather than silently omitting it.

3. **Risk the launch before it ships** — `pre-mortem`
   Run a pre-mortem: imagine the launch has failed and work backward to the causes, then mitigate the highest-risk
   ones. Do this while there's still time to change the plan, not as a retrospective exercise once launch-day
   logistics are already locked.
   **Gate to proceed:** the top 3 failure modes each have either a mitigation or an explicit accepted-risk
   decision — not just a list of things that could go wrong with no owner.

4. **Align internal stakeholders** — `stakeholder-communication`
   Brief sales, support, and other internal stakeholders on positioning, pricing, and what to expect at launch,
   including the risks surfaced in stage 3 so they know what to watch for.
   **Gate to proceed:** sales/support can answer the 3-5 most likely customer questions without escalating — verify
   this with a dry run or FAQ review, not just "the deck was sent."

5. **Launch day execution**
   No dedicated atomic skill; this is coordinated execution against the plan from stages 1-4 — publishing,
   enablement go-live, monitoring channels for the mitigated risks from stage 3.
   **Gate to proceed:** the launch-day checklist is complete and the risks flagged in stage 3 are being actively
   watched, not just documented.

6. **Post-launch metric check against the plan**
   No dedicated atomic skill; compare actual performance against the targets implied by stage 1's strategy. This
   is what closes the loop — without it, the workflow ends at "we launched" rather than "we launched and here's
   whether it worked."
   **Gate to proceed:** there's a dated check-in (typically 2-4 weeks out) where actuals are compared to the
   original plan and a clear call is made — on track, needs adjustment, or needs escalation.

## Sequencing notes

- Stages 1-2 are sequential (pricing decisions should react to positioning, not the reverse), but stage 3
  (pre-mortem) can start as soon as a draft of stages 1-2 exists — running it in parallel with stakeholder drafts
  is fine as long as mitigations feed back into stage 4's briefing before it goes out. Stages 5 and 6 are
  inherently sequential and separated in time — stage 6 typically can't happen until weeks after stage 5, and
  trying to call it early produces a verdict based on noise rather than signal.
- Stage 4 must finish before stage 5 — launching before internal teams are briefed is the single fastest way to
  turn a manageable launch-day issue into a customer-facing one, since the first line of defense (sales and
  support) won't know what's expected or what's already been flagged as a risk.
- **The most common skipped stage is #3 (pre-mortem)** — teams under launch-date pressure treat risk-listing as a
  nice-to-have rather than a gate. What breaks downstream: the failure modes that would have been caught in a
  30-minute pre-mortem instead surface live on launch day, at which point stage 4's internal briefing is already
  out of date and support/sales are caught flat-footed in front of customers.

## Final output

A complete launch package plus a post-launch verdict: the GTM strategy (stage 1), pricing/packaging decision if
applicable (stage 2), the pre-mortem risk log with mitigations (stage 3), the internal stakeholder briefing record
(stage 4), the launch-day execution checklist (stage 5), and a dated post-launch review comparing actuals to plan
(stage 6) — handed back as the record of what was decided, what was risked, and how it actually performed. This
package is also the input for the next launch: the pre-mortem risks that materialized and the ones that didn't are
exactly the calibration data the next `pre-mortem` pass should start from.

## Quality checklist

- [ ] Does the pricing decision (if applicable) trace back to the positioning, rather than being set independently?
- [ ] Were the pre-mortem's top risks actually mitigated or explicitly accepted — not just listed and forgotten?
- [ ] Could sales/support answer a customer's hardest likely question the day of launch without escalating?
- [ ] Is there a scheduled post-launch review date, not an open-ended "we'll check on it sometime"?
- [ ] Does the post-launch review compare actuals against the specific targets stage 1 implied, rather than
      against a vague sense of "how did it go"?
