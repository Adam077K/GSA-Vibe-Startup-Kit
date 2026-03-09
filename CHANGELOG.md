# Changelog

All notable changes to GSA Startup Kit are documented here.

Format follows [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).

---

## [1.0.0] — 2026-02-28

### Added
- 12-agent autonomous startup team (Iris, Atlas, Sage, Guardian, Nexus, Scout, Spark, Axiom, Morgan, Nova, Rex, Lyra)
- GSA workflow: 28 slash commands (`/gsa:new-project`, `/gsa:plan-phase`, `/gsa:execute-phase`, etc.)
- `bin/install.js` — NPX CLI installer with `--claude`, `--cursor`, `--antigravity` flags
- 5 top-level commands: `/daily`, `/plan`, `/ship`, `/audit`, `/research`
- `.cursor/rules/` — Cursor integration
- 938+ skills via `antigravity-awesome-skills` (installed separately)
- GSA internals: templates, references, workflows, hooks
- Memory system: `DECISIONS.md`, `CODEBASE-MAP.md`, `USER-INSIGHTS.md`

---

## [1.1.1] — 2026-03-10

### Changed
- Migrated agents from `.claude/agents/` to `.agent/agents/` (31 agent definitions)
- Migrated commands from `.claude/commands/gsa/` to `.agent/commands/`
- Added `.agent/hooks/` (gsa-check-update, gsa-context-monitor, gsa-statusline)
- Added `.agent/memory/AUDIT_LOG.md`, `LONG-TERM.md`

### Removed
- `.claude/get-shit-done/` — GSD tooling removed; workflow moved to `.agent/`
- `.claude/agents/archive/` — archived agents consolidated
- `.claude/commands/gsa/` — commands migrated to `.agent/commands/`
- Duplicate `workflow-*README.md` files from skills

---

## [1.1.0] — 2026-03-09

### Changed
- Agent system upgraded from 12-agent flat team to 3-layer CEO → Team Leads → Workers architecture
- CEO replaces Iris as entry point for all tasks
- 9 named Team Leads replace individual named agents (iris→ceo, atlas→build-lead, etc.)
- 9 Worker agents + 12 GSD execution agents replace old gsa-* execution agents
- Slash commands expanded: added `/build`, `/fix`, `/design`, `/review`
- README, QUICK_REFERENCE, GETTING_STARTED updated to reflect new architecture
- package.json version bumped to 1.1.0, repository URL fixed, Cursor removed from keywords

### Removed
- `.cursor/rules/` folder — Cursor integration removed; Claude Code + Antigravity are primary tools
- `.vscode/settings.json` — not needed for public kit
- `all_skills_stored/` excluded via .gitignore (55MB stale backup; live skills remain at `.agent/skills/`)

### Fixed
- package.json repository URL (was `YOUR_ORG` placeholder, now points to correct repo)
- Old agent name references (Iris, Atlas, Morgan, etc.) across all public docs

---

*Older entries will be added as the kit evolves.*
