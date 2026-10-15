# Agent Entry Point

Canonical agent-facing config lives in `_agent/`:

- Core (auto-loaded truth): @_agent/rules/core.md
- `_agent/skills/` — project skills

Agent-specific dirs (`.devin/`, `.agents/`, `.claude/`, `.commandcode/`,
`.windsurf/`) are symlinks into `_agent/` — edit there, never in the linked
dirs.

Links are committed to git; if a surface link is missing run `just agent-links`.
