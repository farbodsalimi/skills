# Skills

A collection of Claude Code custom slash command skills for daily engineering workflows.

## Available Skills

| Skill | Command | Description |
|-------|---------|-------------|
| [Standup](skills/standup/SKILL.md) | `/standup` | Write and log a daily standup update to a monthly file |
| [Friday Field Report](skills/friday-field-reports/SKILL.md) | `/friday-field-report` | Summarize the week's standups into a Friday field report |
| [Review RFC](skills/review-rfc/SKILL.md) | `/review-rfc` | Deep structured review of software RFC documents. Inspired by [A Thorough Team Guide to RFCs](https://medium.com/juans-and-zeroes/a-thorough-team-guide-to-rfcs-8aa14f8e757c) |
| [Conventional Commits](skills/conventional-commits/SKILL.md) | `/conventional-commits` | Generate a Conventional Commits message from staged changes and create the commit |

## Installation

### Via the plugin marketplace (recommended)

Add this repository as a plugin marketplace and install the plugin from within Claude Code:

```
/plugin marketplace add farbodsalimi/skills
/plugin install skills@farbodsalimi-skills
```

This installs all skills at once and keeps them updatable via `/plugin`.

### Manual install

Alternatively, copy or symlink individual skills into your project's (or `~/.claude/`) `skills/` directory:

```sh
# Copy a single skill into the project
cp -r skills/standup /path/to/project/.claude/skills/standup

# Or symlink it
ln -s /path/to/skills/skills/standup /path/to/project/.claude/skills/standup
```

## Usage

Invoke a skill in Claude Code with `/<skill-name>`:

```
/standup Worked on auth module, planning to review PRs today
/friday-field-report
/review-rfc ./docs/rfc-042.md
/conventional-commits
```

## Specification

Skills in this repo follow the [Agent Skills specification](https://agentskills.io/specification). Each skill is a directory containing a `SKILL.md` file with YAML frontmatter (`name`, `description`) followed by Markdown instructions.

## Adding a New Skill

1. Create a directory under `skills/` named after the skill (lowercase, hyphens only)
2. Add a `SKILL.md` file with YAML frontmatter (`name`, `description`) followed by the skill instructions
3. Update this README with the new skill
4. Bump the `version` in `.claude-plugin/plugin.json` so marketplace users receive the update

## License

MIT
