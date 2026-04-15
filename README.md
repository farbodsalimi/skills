# Skills

A collection of Claude Code custom slash command skills for daily engineering workflows.

## Available Skills

| Skill | Command | Description |
|-------|---------|-------------|
| [Standup](skills/standup/SKILL.md) | `/standup` | Write and log a daily standup update to a monthly file |
| [Friday Field Report](skills/friday-field-reports/SKILL.md) | `/friday-field-report` | Summarize the week's standups into a Friday field report |
| [Review RFC](skills/review-rfc/SKILL.md) | `/review-rfc` | Deep structured review of software RFC documents. Inspired by [A Thorough Team Guide to RFCs](https://medium.com/juans-and-zeroes/a-thorough-team-guide-to-rfcs-8aa14f8e757c) |

## Usage

To use these skills in a project, copy or symlink the skill files into your project's `.claude/commands/` directory:

```sh
# Copy a single skill
cp skills/standup/SKILL.md /path/to/project/.claude/commands/standup.md

# Or symlink the whole collection
ln -s /path/to/skills/skills/standup/SKILL.md /path/to/project/.claude/commands/standup.md
```

Then invoke the skill in Claude Code with `/<skill-name>`:

```
/standup Worked on auth module, planning to review PRs today
/friday-field-report
/review-rfc ./docs/rfc-042.md
```

## Specification

Skills in this repo follow the [Agent Skills specification](https://agentskills.io/specification). Each skill is a directory containing a `SKILL.md` file with YAML frontmatter (`name`, `description`) followed by Markdown instructions.

## Adding a New Skill

1. Create a directory under `skills/` named after the skill (lowercase, hyphens only)
2. Add a `SKILL.md` file with YAML frontmatter (`name`, `description`) followed by the skill instructions
3. Update this README with the new skill

## License

MIT
