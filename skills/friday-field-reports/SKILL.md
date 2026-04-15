---
name: friday-field-reports
description: Summarize the week's standup updates into a Friday Field Report. Use on Fridays when the user wants a weekly summary of their work grouped by project or theme.
license: MIT
---

You're a weekly report writer that summarizes the week's standup updates into a Friday Field Report.

First, check if today is a Friday. If it is NOT a Friday, inform the user that this command should only be run on Fridays and stop.

If today IS a Friday, proceed with the following steps:

1. Read the current month's file in `standup-history/` (e.g., `standup-history/2026-03.md`) and extract all standup entries from the current week (Monday through Friday of this week). If the week spans two months, also read the previous month's file.
2. Read the most recent file in the `friday-field-reports/` directory to match the tone, style, and level of detail used in previous reports.

If $ARGUMENTS is empty or unclear, ask the user to confirm the projects/themes they worked on this week before generating the report.

Group the week's standup updates by project or theme, then generate a Friday Field Report and write it to a new file at `friday-field-reports/YYYY-MM-DD.md` (using the current Friday's date). Never overwrite an existing report.

Use the template below. Always include the current Friday's date in the `# Friday Field Report - YYYY-MM-DD` heading.

For each project/theme, synthesize the week's progress into a cohesive summary rather than listing each day separately.

Template:

# Friday Field Report - YYYY-MM-DD

**Project/Theme Name**

- **Status:** Current overall status of this project (e.g., In progress, Deployed, Blocked, etc.)
- **This week:** Summary of what was accomplished this week across all standup entries.
- **Next milestone:** What comes next for this project.
- **Risks:** Any blockers, challenges, or risks identified during the week. Use "None at this time." if there are none.
