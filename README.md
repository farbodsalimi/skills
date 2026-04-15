# Skills

A collection of Claude Code custom slash command skills for daily engineering workflows.

## Available Skills

| Skill | Command | Description |
|-------|---------|-------------|
| [Standup](skills/standup-history/standup.md) | `/standup` | Write and log a daily standup update to a monthly file |
| [Friday Field Report](skills/friday-field-reports/friday-field-report.md) | `/friday-field-report` | Summarize the week's standups into a Friday field report |

## Usage

To use these skills in a project, copy or symlink the skill files into your project's `.claude/commands/` directory:

```sh
# Copy a single skill
cp skills/standup-history/standup.md /path/to/project/.claude/commands/standup.md

# Or symlink the whole collection
ln -s /path/to/skills/skills/standup-history/standup.md /path/to/project/.claude/commands/standup.md
```

Then invoke the skill in Claude Code with `/<skill-name>`:

```
/standup Worked on auth module, planning to review PRs today
/friday-field-report
```

## Adding a New Skill

1. Create a directory under `skills/` named after the skill
2. Add a markdown file with the skill prompt (same name as the directory)
3. Update this README with the new skill

## License

MIT
