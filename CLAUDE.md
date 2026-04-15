# CLAUDE.md

This repo stores Claude Code custom slash command skills. The files here are prompt templates, not executable code.

## Repo Structure

```
skills/
  <skill-name>/
    SKILL.md    # Required: YAML frontmatter + skill instructions
```

## Conventions

- Each skill lives in its own directory under `skills/`
- The skill prompt file is always named `SKILL.md` and must contain YAML frontmatter with `name` and `description` fields
- The `name` field in frontmatter must match the directory name (lowercase letters, numbers, and hyphens only)
- Skills use `$ARGUMENTS` to accept user input from the slash command invocation
- Skills that manage data (e.g., standup history) reference relative paths for their data directories — these directories are created in the target project, not in this repo
- Write prompts in plain markdown with clear step-by-step instructions

## Commits

This project uses [conventional commits](https://www.conventionalcommits.org/) with sv4git (see `.sv4git.yml`).

- `feat`: new skill or significant new capability (bumps minor)
- `fix`: bug fix in an existing skill (bumps patch)
- `chore`, `refactor`, `docs`, `ci`, `build`, `test`, `perf`: other changes (bumps patch)
- Format: `<type>: <description>` (e.g., `feat: add standup skill`)
