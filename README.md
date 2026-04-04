# claude-meta-toolkit

Tools that improve Claude Code itself -- observability, session hooks, marketplace maintenance.

## Install

```bash
claude plugin install Leolebleis/claude-meta-toolkit
```

## Skills

- **observer-setup** -- Set up OTEL telemetry export for Claude Code on a new machine.
- **marketplace-feedback** -- Act on feedback about any Leolebleis plugin. Finds the repo locally, applies the fix and raises a PR, or files an issue if the repo isn't available.

## Configs

- **ccstatusline** -- Backup of [ccstatusline](https://www.npmjs.com/package/ccstatusline) status bar configuration.

## Session Guidance (auto-injected)

At session start, the plugin injects guidance so Claude suggests the right skill at natural checkpoints:

- `/revise-claude-md` -- after productive sessions with new learnings
- `/claude-md-improver` -- when entering a repo or auditing CLAUDE.md quality
- `/skill-creator` -- after creating or modifying skills
- `/claude-automation-recommender` -- when setting up Claude Code for a new project
- `/simplify` -- before creating a PR (code reuse, quality, efficiency review)

## Recommended Plugins

See `plugins.md` for recommended Claude Code plugin install commands.
