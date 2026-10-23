# Notion Daily · Weekly · Monthly Planner

An AI-assisted, reusable planning skill for organizing **daily, weekly, and monthly plans in a single Notion task database**. It helps structure goals, check task status, review progress, and carry unfinished work into the next planning cycle.

> **Status:** v0.1 — planning skill and Notion CSV template, not a standalone application. The core skill instructions are currently written in Chinese.

## What it does

- Keeps daily, weekly, and monthly plans in **one database**, categorized by planning period.
- Breaks monthly outcomes into weekly deliverables and daily actions.
- Uses actual task **Status** or **Checkbox** fields to check progress.
- Supports weekly/monthly reviews and rescheduling without erasing history.
- Helps prevent duplicate tasks and preserves existing Notion content.

**Important:** The skill does not monitor Notion continuously or run automatically. Your AI assistant must have access to your Notion workspace, and you must request or separately authorize actions.

## Files

| File | Purpose |
| --- | --- |
| [`SKILL.md`](SKILL.md) | Main reusable AI skill instructions |
| [`docs/QUICKSTART.zh-CN.md`](docs/QUICKSTART.zh-CN.md) | Chinese setup and example prompts |
| [`templates/notion_tasks_template.csv`](templates/notion_tasks_template.csv) | Sample rows and headers for a Notion database |

## Quick start

1. Copy [`SKILL.md`](SKILL.md) into an AI assistant or agent that supports custom instructions / skills, following its specific setup process.
2. Prepare an existing Notion task database, or import [`notion_tasks_template.csv`](templates/notion_tasks_template.csv) as a starting point.
3. In Notion, use columns for **Task**, **Category**, **Date**, **Priority**, **Status**, **Project**, and **Notes** (the template uses Chinese column names). Confirm property types after CSV import.
4. If you want the assistant to read/write your Notion tasks, connect your own Notion account and grant the required permissions.
5. Ask the assistant to create your plan or review the current week.

### Example prompt (Chinese)

```text
请使用这个每日 / 每周 / 本月统一计划 Skill。
请根据我提供的 Notion 数据库、目标和截止日期，生成本周和每日计划。
保留历史记录，避免重复任务，并按实际状态追踪完成情况。
```

## Design principles

- One database, three categories: 每日计划 → 每周计划 → 本月计划.
- Priority levels: P0 (critical) through P3 (optional).
- Only mark a task complete based on the configured Status/Checkbox source of truth.
- Read the real Notion database schema before editing; preserve existing content.
- Never assume permission to edit, publish, or share someone's private information.
- Recurring checks need an external scheduler; a Markdown skill alone does not schedule them.

## Roadmap

- [ ] Add an English version of the skill instructions.
- [ ] Collect feedback from users setting up the Notion workflow.
- [ ] Improve sample data and setup guidance based on testing.

## Contributing

Issues and suggestions are welcome. Please remove personal information and private Notion URLs before posting examples.

## License

No license has been selected yet. If you want others to reuse or modify the files under a standard open-source license, add a LICENSE file (for example, MIT) after reviewing your preferred terms.
