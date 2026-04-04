# claude-meta-toolkit

Tools that improve Claude Code itself -- observability, session hooks, marketplace maintenance (`Leolebleis/claude-meta-toolkit`).

## Structure

```
.claude-plugin/marketplace.json   # Plugin metadata + version
skills/<name>/SKILL.md            # One directory per skill
configs/<name>/                   # Backup configs for external tools
hooks/                            # SessionStart hooks (context injection)
  md-hygiene.md                   # Session guidance (injected at session start via hook)
plugins.md                        # Recommended plugins for new machines
README.md                         # Public-facing install instructions
```

## Skills

| Skill | Purpose |
|-------|---------|
| observer-setup | OTEL telemetry setup for new machines. |
| marketplace-feedback | Act on feedback about any Leolebleis plugin -- find repo, apply fix, raise PR or issue. |

## Configs

| Config | Purpose |
|--------|---------|
| ccstatusline | Backup of ccstatusline status bar settings. |

## Hooks

The plugin injects session guidance at start via a `SessionStart` hook. This reminds Claude to suggest relevant skills at natural checkpoints (end of session, first time in a repo, before PRs, etc.). See `hooks/md-hygiene.md` for the full reference.

## Rules

- **Always increment the version** in `.claude-plugin/marketplace.json` when modifying skills or adding new ones. Use semver: patch for fixes, minor for new skills or features, major for breaking changes.
- **Never push directly to main.** Create a branch and open a PR.
- **Update README.md** when adding or removing skills.
