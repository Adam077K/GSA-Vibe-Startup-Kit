# GSA Startup Kit — Green Startup Academy

קיט לבניית סטארטאפים עם AI Agents. מתאים ל-Claude Code ו-Antigravity.

A production-ready AI agent kit for building startups. Built for [Green Startup Academy](https://www.kfar-hayarok.org.il/) (כפר הירוק) — Israel's youth startup school.

## Quick Start (5 minutes)

1. **Clone**
   ```bash
   git clone https://github.com/Adam077K/GSA-Vibe-Startup-Kit.git
   cd GSA-Vibe-Startup-Kit
   ```

2. **Optional:** Run `./scripts/setup.sh` to verify structure and create memory files

3. **Open** in Claude Code or Antigravity

4. **Start** with: "CEO, אני רוצה לבנות [X]" or "CEO, I want to build [X]"

## Installation Options

### Option 1 — Clone (recommended, full kit)
```bash
git clone https://github.com/Adam077K/GSA-Vibe-Startup-Kit.git
cd GSA-Vibe-Startup-Kit
```
Open in Claude Code. CLAUDE.md + agents load automatically for this project.

### Option 2 — NPX into any existing project
```bash
npx gsa-startup-kit --claude
```
Copies `.claude/agents/`, `.claude/commands/`, `.claude/get-shit-done/`, hooks, and `CLAUDE.md`
into your current project folder.

### Option 3 — Global (agents in every project, no per-project setup)
```bash
npx gsa-startup-kit --claude --global
```
Installs agents and commands into `~/.claude/` — Claude Code uses them automatically in every project.
See [docs/GLOBAL_SETUP.md](docs/GLOBAL_SETUP.md) for manual setup instructions.

---

## For Green Startup Academy (כפר הירוק)

- [Getting Started](docs/GETTING_STARTED.md) — Full onboarding
- [Quick Reference](docs/QUICK_REFERENCE.md) — One-pager cheat sheet
- Slash commands: `/build` `/fix` `/design` `/review` `/daily` `/plan` `/ship` `/audit` `/research`
- [Agent team](AGENTS.md)

## Tool Support

| Tool | Setup |
|------|-------|
| **Claude Code** | Auto-loads CLAUDE.md, agents, and hooks |
| **Antigravity** | Open folder; skills load from `.agent/skills/` |

## What's Inside

- **31 agents** — CEO (entry point), 9 Team Leads, 9 Workers, 12 GSD execution agents
- **426+ skills** — Expert knowledge for planning, coding, security, SEO, and more
- **Get-Shit-Done** workflows — Phase planning, execution, verification

### The 3-Layer Team

```
Layer 1 ── CEO
              │ Entry point. Reads context, assembles team, delegates, synthesizes.
              │
Layer 2 ── Team Leads (9)
              │ build-lead · research-lead · design-lead · qa-lead · devops-lead
              │ data-lead  · product-lead  · growth-lead · business-lead
              │
Layer 3 ── Workers (21)
              backend-developer · frontend-developer · database-engineer · ai-engineer
              security-engineer · test-engineer · code-reviewer · researcher · technical-writer
              + 12 GSD execution agents (planner, executor, debugger, verifier, and more)
```

See [AGENTS.md](AGENTS.md) for the full routing table and examples.

## Skills (426+)

- Browse: [.agent/skills/README.md](.agent/skills/README.md)
- Bundles: [.agent/skills/docs/BUNDLES.md](.agent/skills/docs/BUNDLES.md)
- Workflows: [docs/workflow-bundles.md](docs/workflow-bundles.md)

## Requirements

- **Node.js 18+** (for Get-Shit-Done hooks)

## License & Contributing

- [LICENSE](LICENSE) — MIT
- [CONTRIBUTING.md](CONTRIBUTING.md) — How to contribute
