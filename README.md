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
| `talwar-vision-strategy` | North Star vision statement and the strategic pillars that ladder up to it |
| `talwar-okrs-metrics` | Objectives, key results, and confidence scoring |
| `talwar-roadmapping` | Now/Next/Later outcome-based roadmap |
| `talwar-business-case` | Investment justification and ROI analysis |
| `talwar-business-model-canvas` | Osterwalder's 9-block value/revenue architecture |
| `talwar-initiative-canvas` | Single-page strategic initiative definition |
| `talwar-project-briefing` | Consolidated stakeholder project brief |
| `talwar-scope-definition` | In-scope vs out-of-scope boundaries |
| `talwar-product-discovery` | Rapid idea validation and lightweight experiments |
| `talwar-product-market-fit` | PMF assessment (Sean Ellis test, retention, qualitative signals) |
| `talwar-market-research` | Competitive analysis and customer insights |
| `talwar-customer-journey-mapping` | End-to-end customer experience visualisation |
| `talwar-behavioral-science-economics` | Nudges, behavioural economics, and the dark-pattern line |
| `talwar-pricing-monetization-strategy` | Pricing models and monetisation strategy |
| `talwar-go-to-market` | GTM strategy, positioning, and launch planning |
| `talwar-feature-story-mapping` | Jeff Patton-style story mapping and MVP slicing |
| `talwar-backlog-management` | INVEST user stories and Definition of Ready |
| `talwar-prioritization-matrix` | RICE, MoSCoW, and DVF prioritisation |
| `talwar-decision-framework` | One-way vs two-way door decisions and decision records |
| `talwar-solution-options-generator` | Generate and evaluate genuinely distinct alternatives |
| `talwar-pre-mortem` | Gary Klein-style pre-mortem risk surfacing |
| `talwar-stakeholder-mapper` | Power/interest matrix and engagement strategy |
| `talwar-stakeholder-management` | Ongoing stakeholder engagement and communication planning |
| `talwar-portfolio-investment-allocation` | Portfolio-level resource allocation across initiatives |
| `talwar-state-documentation` | Current state vs future state gap analysis |
| `talwar-technical-debt-prioritization` | Tech debt quantified in business terms and ranked |
| `talwar-verification-uat` | UAT scenario design and sign-off criteria |
| `talwar-product-canvas` | Single-page strategic product definition |
| `talwar-spec-for-ai-agents` | Specs written for AI coding agents (explicit boundaries, non-goals) |
| `talwar-decision-memo` | One-page BLUF memo to drive a Yes/No/Modified decision |
| `talwar-executive-storyline` | Pyramid Principle and SCQA narrative structure |
| `talwar-issue-tree` | MECE problem decomposition into testable hypotheses |
| `talwar-discovery-to-backlog` **[workflow]** | Validated insight → sprint-ready backlog |
| `talwar-requirements-definition` **[workflow]** | Interviews → signed-off requirements |
| `talwar-initiative-kickoff` **[workflow]** | Idea → approved, delivery-ready initiative |
| `talwar-go-to-market-launch` **[workflow]** | Full GTM launch, end to end |
| `talwar-stakeholder-communication` **[workflow]** | Ongoing stakeholder engagement programme |

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

Workflow skills (`talwar-discovery-to-backlog`, `talwar-requirements-definition`, `talwar-initiative-kickoff`,
`talwar-go-to-market-launch`, `talwar-stakeholder-communication`) instead describe a staged sequence of the
atomic skills above, with a decision gate between each stage.

## Roadmap

This repo covers only the Product Capabilities tier. 
Other Capabilities (sprint planning, RAID logs, incident management, ...) and 
Transformation Capabilities (change management, negotiation, org design, ...) are planned as separate follow-up plugins.

## License

MIT — see [LICENSE](LICENSE).

Built by [Aman Talwar](https://amantalwar.com).

