# pm-product-capabilities

A Claude Code plugin of 37 product-management skills — the "Product Capabilities" tier of a
larger AI Operating System skills list (Delivery and Transformation tiers are planned as
follow-up plugins; see [Roadmap](#roadmap)).

Each skill packages a specific PM framework (OKRs, RICE, Pyramid Principle, JTBD-style story
mapping, pre-mortems, and more) as instructions Claude follows on request — so instead of
re-explaining a framework every time, you ask for the artifact and Claude applies it correctly,
with a consistent output template and a built-in quality checklist.

## What's included

32 single-purpose skills plus 5 end-to-end workflow skills that sequence several of the atomic
ones together for a larger job-to-be-done (marked **[workflow]** below).

| Skill | What it does |
|---|---|
| `vision-strategy` | North Star vision statement and the strategic pillars that ladder up to it |
| `okrs-metrics` | Objectives, key results, and confidence scoring |
| `roadmapping` | Now/Next/Later outcome-based roadmap |
| `business-case` | Investment justification and ROI analysis |
| `business-model-canvas` | Osterwalder's 9-block value/revenue architecture |
| `initiative-canvas` | Single-page strategic initiative definition |
| `project-briefing` | Consolidated stakeholder project brief |
| `scope-definition` | In-scope vs out-of-scope boundaries |
| `product-discovery` | Rapid idea validation and lightweight experiments |
| `product-market-fit` | PMF assessment (Sean Ellis test, retention, qualitative signals) |
| `market-research` | Competitive analysis and customer insights |
| `customer-journey-mapping` | End-to-end customer experience visualisation |
| `behavioral-science-economics` | Nudges, behavioural economics, and the dark-pattern line |
| `pricing-monetization-strategy` | Pricing models and monetisation strategy |
| `go-to-market` | GTM strategy, positioning, and launch planning |
| `feature-story-mapping` | Jeff Patton-style story mapping and MVP slicing |
| `backlog-management` | INVEST user stories and Definition of Ready |
| `prioritization-matrix` | RICE, MoSCoW, and DVF prioritisation |
| `decision-framework` | One-way vs two-way door decisions and decision records |
| `solution-options-generator` | Generate and evaluate genuinely distinct alternatives |
| `pre-mortem` | Gary Klein-style pre-mortem risk surfacing |
| `stakeholder-mapper` | Power/interest matrix and engagement strategy |
| `stakeholder-management` | Ongoing stakeholder engagement and communication planning |
| `portfolio-investment-allocation` | Portfolio-level resource allocation across initiatives |
| `state-documentation` | Current state vs future state gap analysis |
| `technical-debt-prioritization` | Tech debt quantified in business terms and ranked |
| `verification-uat` | UAT scenario design and sign-off criteria |
| `product-canvas` | Single-page strategic product definition |
| `spec-for-ai-agents` | Specs written for AI coding agents (explicit boundaries, non-goals) |
| `decision-memo` | One-page BLUF memo to drive a Yes/No/Modified decision |
| `executive-storyline` | Pyramid Principle and SCQA narrative structure |
| `issue-tree` | MECE problem decomposition into testable hypotheses |
| `discovery-to-backlog` **[workflow]** | Validated insight → sprint-ready backlog |
| `requirements-definition` **[workflow]** | Interviews → signed-off requirements |
| `initiative-kickoff` **[workflow]** | Idea → approved, delivery-ready initiative |
| `go-to-market-launch` **[workflow]** | Full GTM launch, end to end |
| `stakeholder-communication` **[workflow]** | Ongoing stakeholder engagement programme |

## Installation

**As a Claude Code plugin marketplace:**

```
/plugin marketplace add <your-github-username>/pm-product-capabilities
/plugin install pm-product-capabilities
```

**Manually (no plugin system, just the skills):**

```bash
git clone https://github.com/<your-github-username>/pm-product-capabilities.git
cp -r pm-product-capabilities/skills/* ~/.claude/skills/
```

Either way, each skill triggers automatically when your request matches its description — you
don't need to invoke them by name, though `/skill-name` works too.

## How a skill is structured

Every `skills/<name>/SKILL.md` follows the same shape:

1. **Why this matters** — the reasoning behind the framework, not just the steps
2. **Gather inputs first** — what context to collect before drafting
3. **Process** — numbered steps grounded in a named framework
4. **Output template** — an exact markdown structure to fill in
5. **Quality checklist** — the failure modes to check for before handing work back
6. **Related skills** — where to go next

Workflow skills (`discovery-to-backlog`, `requirements-definition`, `initiative-kickoff`,
`go-to-market-launch`, `stakeholder-communication`) instead describe a staged sequence of the
atomic skills above, with a decision gate between each stage.

## Roadmap

This repo covers only the Product Capabilities tier. Delivery Capabilities (sprint planning,
RAID logs, incident management, ...) and Transformation Capabilities (change management,
negotiation, org design, ...) are planned as separate follow-up plugins.

## License

MIT — see [LICENSE](LICENSE).

Built by [Aman Talwar](https://amantalwar.com).

