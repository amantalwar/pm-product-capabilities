# pm-product-capabilities

A Claude Code plugin of 37 product-management skills, the "Product Capabilities" tier of a
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
| `talwar-pm-vision-strategy-skill` | North Star vision statement and the strategic pillars that ladder up to it |
| `talwar-pm-okrs-metrics-skill` | Objectives, key results, and confidence scoring |
| `talwar-pm-roadmapping-skill` | Now/Next/Later outcome-based roadmap |
| `talwar-pm-business-case-skill` | Investment justification and ROI analysis |
| `talwar-pm-business-model-canvas-skill` | Osterwalder's 9-block value/revenue architecture |
| `talwar-pm-initiative-canvas-skill` | Single-page strategic initiative definition |
| `talwar-pm-project-briefing-skill` | Consolidated stakeholder project brief |
| `talwar-pm-scope-definition-skill` | In-scope vs out-of-scope boundaries |
| `talwar-pm-product-discovery-skill` | Rapid idea validation and lightweight experiments |
| `talwar-pm-product-market-fit-skill` | PMF assessment (Sean Ellis test, retention, qualitative signals) |
| `talwar-pm-market-research-skill` | Competitive analysis and customer insights |
| `talwar-pm-customer-journey-mapping-skill` | End-to-end customer experience visualisation |
| `talwar-pm-behavioral-science-economics-skill` | Nudges, behavioural economics, and the dark-pattern line |
| `talwar-pm-pricing-monetization-strategy-skill` | Pricing models and monetisation strategy |
| `talwar-pm-go-to-market-skill` | GTM strategy, positioning, and launch planning |
| `talwar-pm-feature-story-mapping-skill` | Jeff Patton-style story mapping and MVP slicing |
| `talwar-pm-backlog-management-skill` | INVEST user stories and Definition of Ready |
| `talwar-pm-prioritization-matrix-skill` | RICE, MoSCoW, and DVF prioritisation |
| `talwar-pm-decision-framework-skill` | One-way vs two-way door decisions and decision records |
| `talwar-pm-solution-options-generator-skill` | Generate and evaluate genuinely distinct alternatives |
| `talwar-pm-pre-mortem-skill` | Gary Klein-style pre-mortem risk surfacing |
| `talwar-pm-stakeholder-mapper-skill` | Power/interest matrix and engagement strategy |
| `talwar-pm-stakeholder-management-skill` | Ongoing stakeholder engagement and communication planning |
| `talwar-pm-portfolio-investment-allocation-skill` | Portfolio-level resource allocation across initiatives |
| `talwar-pm-state-documentation-skill` | Current state vs future state gap analysis |
| `talwar-pm-technical-debt-prioritization-skill` | Tech debt quantified in business terms and ranked |
| `talwar-pm-verification-uat-skill` | UAT scenario design and sign-off criteria |
| `talwar-pm-product-canvas-skill` | Single-page strategic product definition |
| `talwar-pm-spec-for-ai-agents-skill` | Specs written for AI coding agents (explicit boundaries, non-goals) |
| `talwar-pm-decision-memo-skill` | One-page BLUF memo to drive a Yes/No/Modified decision |
| `talwar-pm-executive-storyline-skill` | Pyramid Principle and SCQA narrative structure |
| `talwar-pm-issue-tree-skill` | MECE problem decomposition into testable hypotheses |
| `talwar-pm-discovery-to-backlog-skill` **[workflow]** | Validated insight → sprint-ready backlog |
| `talwar-pm-requirements-definition-skill` **[workflow]** | Interviews → signed-off requirements |
| `talwar-pm-initiative-kickoff-skill` **[workflow]** | Idea → approved, delivery-ready initiative |
| `talwar-pm-go-to-market-launch-skill` **[workflow]** | Full GTM launch, end to end |
| `talwar-pm-stakeholder-communication-skill` **[workflow]** | Ongoing stakeholder engagement programme |

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

Workflow skills (`talwar-pm-discovery-to-backlog-skill`, `talwar-pm-requirements-definition-skill`, `talwar-pm-initiative-kickoff-skill`,
`talwar-pm-go-to-market-launch-skill`, `talwar-pm-stakeholder-communication-skill`) instead describe a staged sequence of the
atomic skills above, with a decision gate between each stage.

## Roadmap

This repo covers only the Product Capabilities tier. 
Other Capabilities (sprint planning, RAID logs, incident management, ...) and 
Transformation Capabilities (change management, negotiation, org design, ...) are planned as separate follow-up plugins.

## License

MIT — see [LICENSE](LICENSE).

Built by [Aman Talwar](https://amantalwar.com).

