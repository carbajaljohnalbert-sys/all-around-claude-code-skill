# All-Around Claude Code Skill

A comprehensive Claude Code setup with curated skills, plugins, and configurations for maximum productivity.

## Quick Start

1. **Install Claude Code** — see [Claude Code docs](https://docs.anthropic.com/en/docs/claude-code)
2. **Clone this repo** into `~/.claude/` (or merge into your existing one):
   ```bash
   git clone https://github.com/carbajaljohnalbert-sys/all-around-claude-code-skill.git
   ```
3. **Copy the files** you need into your `~/.claude/` directory. At minimum, grab:
   - `CLAUDE.md` — core instructions and skill auto-trigger rules
   - `settings.json` — plugin config and environment setup
   - `skills/` — custom skill definitions

## What's Included

### CLAUDE.md — Global Instructions

The `CLAUDE.md` file sets global behavior rules. Key auto-trigger:

| Trigger | Action |
|---------|--------|
| Any prompt writing/editing request | Automatically invokes `prompt-master` skill |

### Skills

| Skill | Purpose |
|-------|---------|
| **prompt-master** | Generates optimized prompts for LLMs, image AI, coding agents, and more. Detects the target AI tool and adapts the prompt accordingly. |

### Plugins

| Plugin | Description |
|--------|-------------|
| **superpowers** | Development workflow skills — TDD, debugging, code review, planning, brainstorming, git worktrees, and more |
| **context7** | Fetches up-to-date library/framework documentation on demand |
| **ui-ux-pro-max** | UI/UX design intelligence — 50+ styles, 161 color palettes, 57 font pairings across 10 stacks |
| **skill-creator** | Create, edit, and benchmark custom skills |

### Settings

Key configurations in `settings.json`:

- **Theme**: Dark mode
- **Auto-updates**: Latest channel
- **Plugins**: All four plugins enabled
- **Environment variables**: Pre-configured for local proxy setups and token management

## Directory Structure

```
.claude/
├── CLAUDE.md              # Global instructions & skill triggers
├── settings.json          # Plugin, theme, and environment config
├── settings.local.json    # Local permission overrides
└── skills/
    └── prompt-master/     # AI prompt optimization skill
        ├── SKILL.md
        └── references/
            ├── patterns.md
            └── templates.md
```

## Security

- `settings.json` is **included** in the repo. Before pushing your own config, review it for tokens or credentials.
- Use `settings.local.json` for machine-specific settings and permissions (not shared).
- The following are **excluded** from version control:
  - `history.jsonl` (conversation history)
  - `cache/`, `sessions/`, `jobs/` (runtime data)
  - `daemon.*` (process management)

## Contributing

Fork → Clone → Add your skill → PR. Keep skills self-contained in their own folders under `skills/`.

## License

MIT