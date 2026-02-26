# AGENTS.md — Startup Team Registry
*All 12 agents read this to find each other. Updated when adding new agents.*

---

## Quick Routing Table

| Task involves... | Call |
|-----------------|------|
| Starting any task, planning, routing | **iris** |
| Code, TypeScript, Next.js, API, DB | **atlas** |
| LLM, RAG, AI agents, embeddings | **sage** |
| Tests, security, OWASP, pre-deploy | **guardian** |
| Deploy, CI/CD, infra, monitoring | **nexus** |
| Feature specs, PRDs, roadmap | **morgan** |
| SEO, copy, email, launch, growth | **nova** |
| Pricing, financials, RICE, OKRs | **axiom** |
| Research, competitive intel, market | **rex** |
| UI/UX, Tailwind, design system | **lyra** |
| Code review, documentation, debt | **scout** |
| Metrics, SQL, dashboards, dbt | **spark** |

---

## Agents

### Iris — CEO & Orchestrator
**File:** `.claude/agents/iris.md` | **Model:** sonnet
**Use for:** Starting any task, daily planning, routing, cross-agent coordination, strategy
**Do NOT use for:** Writing code, copy, deep research (delegate those)

### Morgan — CPO / Product Manager
**File:** `.claude/agents/morgan.md` | **Model:** sonnet
**Use for:** PRDs, user stories, roadmap, RICE scoring, acceptance criteria
**Do NOT use for:** Code, design mockups, financial modeling

### Atlas — CTO / Lead Engineer
**File:** `.claude/agents/atlas.md` | **Model:** sonnet
**Use for:** All code (TypeScript, Next.js, Prisma, Postgres), API, DB schema, architecture
**Do NOT use for:** Copy, design, financial modeling, research

### Sage — AI Engineer
**File:** `.claude/agents/sage.md` | **Model:** opus
**Use for:** LLM, RAG pipelines, AI agents, vector DBs, prompt engineering, background AI jobs
**Do NOT use for:** Standard web features, UI code, non-AI DB schema, deployment

### Nova — CMO / Growth
**File:** `.claude/agents/nova.md` | **Model:** sonnet
**Use for:** Landing page copy, SEO, email campaigns, feature announcements, GTM, launch
**Do NOT use for:** Writing code, financial modeling, primary research

### Axiom — CFO / Business Analyst
**File:** `.claude/agents/axiom.md` | **Model:** sonnet
**Use for:** Pricing, financial projections, RICE, OKRs, unit economics, business cases
**Do NOT use for:** Code, copy, user research

### Rex — Research Analyst
**File:** `.claude/agents/rex.md` | **Model:** opus
**Use for:** Competitor research, market sizing, tech evaluation, user pain from public sources
**Do NOT use for:** Code, copy, financial modeling (hand findings to axiom/nova)

### Lyra — Head of Design
**File:** `.claude/agents/lyra.md` | **Model:** sonnet
**Use for:** UI/UX design, Tailwind components, Radix UI, design system, WCAG accessibility
**Do NOT use for:** Copy, backend code, financial analysis, research

### Scout — Code Intelligence
**File:** `.claude/agents/scout.md` | **Model:** sonnet
**Use for:** Code review, codebase audit, documentation, tech debt analysis, architecture review
**Do NOT use for:** New product features, copy, design, deployment

### Guardian — QA & Security
**File:** `.claude/agents/guardian.md` | **Model:** sonnet
**Use for:** Writing tests, OWASP security, accessibility testing, LLM eval, pre-deploy gate
**Do NOT use for:** Product features, copy, design, financial analysis

### Nexus — Head of DevOps
**File:** `.claude/agents/nexus.md` | **Model:** sonnet
**Use for:** Production deploys, CI/CD, infrastructure, monitoring, runbooks
**Do NOT use for:** Product features, copy, design, financial analysis

### Spark — Data & Analytics
**File:** `.claude/agents/spark.md` | **Model:** sonnet
**Use for:** Metrics dashboards, SQL, dbt models, data pipelines, cohort analysis
**Do NOT use for:** Product features, copy, design, financial projections

---

## Subagent Mesh

```
IRIS ──────────→ ALL agents (orchestrates everything)

MORGAN → Atlas / Rex / Nova / Axiom / Lyra
ATLAS  → Sage / Scout / Guardian / Nexus / Spark
SAGE   → Atlas / Guardian / Rex
NOVA   → Rex / Axiom / Atlas / Lyra
AXIOM  → Rex / Nova / Iris
REX    → Iris / Morgan / Nova
LYRA   → Atlas / Nova
SCOUT  → Atlas / Guardian
GUARDIAN → Atlas / Nexus
NEXUS  → Atlas / Guardian
SPARK  → Atlas / Sage / Iris
```

---

## Slash Commands

| Command | What it does |
|---------|-------------|
| `/daily` | Morning planning — Iris reviews context and proposes today's focus |
| `/plan [goal]` | Sprint/feature planning — Iris orchestrates PRD + estimate + task list |
| `/ship [feature]` | Pre-deploy pipeline — Scout review → Guardian gate → Nexus deploy |
| `/audit [focus]` | Codebase health report — Scout maps, rates, and scores tech debt |
| `/research [topic] [type]` | Rex deep research — sourced intelligence report |

---

## Skills Library

938+ skills at `.agent/skills/[skill-name]/SKILL.md`

Key skill → Agent mapping:
| Skill folder | Primary agent |
|-------------|--------------|
| `nextjs-*`, `react-*`, `prisma-*`, `postgresql-*` | atlas |
| `rag-*`, `ai-*`, `llm-*`, `prompt-*`, `langgraph` | sage |
| `seo-*`, `copywriting`, `marketing-*`, `email-systems` | nova |
| `startup-financial-*`, `pricing-strategy`, `competitive-*` | axiom / iris |
| `deep-research`, `market-sizing-*`, `competitor-*` | rex |
| `tailwind-*`, `radix-*`, `react-ui-*`, `wcag-*` | lyra |
| `testing-*`, `security-*`, `tdd-*`, `sql-injection-*` | guardian |
| `vercel-*`, `cloudformation-*`, `github-actions-*`, `inngest` | nexus |
| `data-*`, `dbt-*`, `sql-optimization-*`, `segment-cdp` | spark |
| `code-refactoring-*`, `codebase-cleanup-*`, `production-code-audit` | scout |

---

## Memory Files

| File | Updated by | Purpose |
|------|-----------|---------|
| `.claude/memory/DECISIONS.md` | Any agent making a permanent decision | Architecture + strategy log |
| `.claude/memory/CODEBASE-MAP.md` | Scout, Atlas | Project code map |
| `.claude/memory/USER-INSIGHTS.md` | Rex (research), Nova (campaigns) | Customer language + pain |
