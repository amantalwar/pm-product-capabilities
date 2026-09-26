---
name: talwar-pm-behavioral-science-economics-skill
description: Apply behavioral economics — nudges, defaults, framing, friction design — to a product or growth decision. Use for "how do we get more people to complete X," "should this be opt-in or opt-out," "why aren't people upgrading," or any request to make a flow more persuasive — even phrased as "make this converts better" or "reduce drop-off at signup."
---

# Behavioral Science & Economics

## Why this matters

Behavioral economics gives real, well-replicated levers over decisions — but the same mechanism (a default, a
scarcity cue, a framing choice) can either help someone make a choice they'd endorse on reflection, or manipulate
them into one they wouldn't. The difference isn't the technique, it's the direction: a nudge is legitimate when it
reduces friction toward what the user already wants or would rationally choose if fully informed and unhurried; it
becomes a dark pattern when it works by exploiting a bias against the user's own interest, hiding information they'd
want, or making the thing they'd actually prefer harder to reach. This skill is only useful if it keeps that line
explicit, because "does this work" is a much easier question than "should we do this" and it's easy to answer only
the first one.

## Gather inputs first

Ask if not given (assume and state it if told to proceed):

- **The decision or behavior** in question (complete signup, upgrade tier, keep subscription, share the product)
- **Who benefits from the desired outcome** — the user, the business, or ostensibly both — this determines how much
  scrutiny the "is this ethical" question needs
- **Current flow/copy**, if one exists, so the change is additive rather than a rewrite from nothing
- **Any regulatory or trust constraints** (subscription cancellation law, data consent requirements, prior user
  complaints about pushiness) that bound what's usable regardless of what would convert best

## Process

1. **Name the target behavior precisely** — not "increase engagement" but the exact action (e.g. "complete the
   second onboarding step within 24 hours").
2. **Pick the mechanism deliberately, not by grabbing whatever's trendy**:
   - **Default effects** — set the pre-selected option to whatever serves the user's likely actual preference (most
     people stick with defaults, so the default carries real weight and real responsibility)
   - **Loss aversion** — frame in terms of what's lost by inaction, used honestly (a real trial expiring) rather than
     invented urgency (a fake countdown)
   - **Anchoring** — a reference point shown before a price or option, used to give honest context (typical usage,
     real comparison), not to make an inflated number look small
   - **Social proof** — real, current, verifiable numbers or examples; stale or fabricated proof collapses the
     moment it's discovered and burns more trust than it built
   - **Friction/ease** — reduce steps for actions that serve the user; this is the least ethically fraught lever and
     often the highest-leverage one
3. **Apply the "endorse on reflection" test before shipping**: if the user saw exactly how this nudge works and
   what it's optimizing for, would they still be glad it exists? If the honest answer is "they'd feel tricked,"
   that's the signal to redesign, not to hide the mechanism better.
4. **Check the reversibility and visibility of the opposite path.** A legitimate nudge makes the recommended path
   easier without making the alternative path deceptive, hidden, or artificially punishing (e.g. cancel should be as
   findable as subscribe).
5. **Instrument it as an experiment**, not a one-way ship. Behavioral effects vary by context and decay with
   repetition — treat the change as a hypothesis to measure, and set a threshold for reverting it if it lifts the
   metric but tanks trust signals (support complaints, opt-out rate, brand sentiment).

## Output template

```markdown
# Behavioral Design: [Flow/Decision]

## Target behavior
[Precise action and desired outcome]

## Who this serves
[User benefit] / [Business benefit] — [note if these diverge, and how]

## Mechanism(s) applied
| Lever | How it's applied here | Why this direction serves the user |
|---|---|---|

## Dark-pattern check
- Endorse-on-reflection test: [would the user be glad this exists if shown how it works? Y/N + why]
- Is the alternative path (opt-out, cancel, skip) equally visible and easy? [Y/N]
- Is every claim (scarcity, social proof, urgency) literally true and current? [Y/N]

## Experiment design
- Metric moved: [...]
- Trust/backlash guardrail metric: [support tickets, opt-outs, complaints — with a revert threshold]
- Test duration / sample: [...]

## Copy/flow changes
[Specific before/after]
```

## Quality checklist

- [ ] Every mechanism used passes the "would the user endorse this on reflection" test, stated explicitly, not assumed
- [ ] The opt-out/alternative path is exactly as easy to find and complete as the promoted path
- [ ] Every scarcity, urgency, or social-proof claim is factually true at the moment it's shown
- [ ] A trust/backlash guardrail metric exists alongside the conversion metric, with a threshold for reverting
- [ ] The doc names who benefits (user vs. business) rather than assuming they're always the same

## Related skills

- Ground the nudge in a real customer pain point first: `talwar-pm-customer-journey-mapping-skill`
- Test the change with rigor before rolling out broadly: `talwar-pm-prioritization-matrix-skill` for what to test first
- Apply pricing-specific framing (anchoring, tiering) with: `talwar-pm-pricing-monetization-strategy-skill`
- Run a pre-mortem on backlash risk before shipping: `talwar-pm-pre-mortem-skill`
