# CLAUDE.md

This repo stores Claude Code custom slash command skills. The files here are prompt templates, not executable code.

## Repo Structure

```
skills/
  <skill-name>/
    <skill-name>.md    # The skill prompt file
```

## Conventions

- Each skill lives in its own directory under `skills/`
- The prompt file name should match the directory name
- Skills use `$ARGUMENTS` to accept user input from the slash command invocation
- Skills that manage data (e.g., standup history) reference relative paths for their data directories — these directories are created in the target project, not in this repo
- Write prompts in plain markdown with clear step-by-step instructions

## Commits

This project uses [conventional commits](https://www.conventionalcommits.org/) with sv4git (see `.sv4git.yml`).

- `feat`: new skill or significant new capability (bumps minor)
- `fix`: bug fix in an existing skill (bumps patch)
- `chore`, `refactor`, `docs`, `ci`, `build`, `test`, `perf`: other changes (bumps patch)
- Format: `<type>: <description>` (e.g., `feat: add standup skill`)
