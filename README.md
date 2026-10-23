# Notion Daily · Weekly · Monthly Planner

An AI-assisted, reusable planning skill for organizing **daily, weekly, and monthly plans in a single Notion task database**.

It helps users structure goals, prioritize tasks, track progress, review completed work, and carry unfinished tasks into the next planning cycle.

> **Status:** v0.1.0 — Initial public release. This project provides reusable AI skill instructions and a Notion CSV template, not a standalone application. The core skill instructions are currently written in Chinese.

## What It Does

- **Unified Planning:** Manage daily, weekly, and monthly plans in one Notion database.
- **Goal Breakdown:** Turn monthly goals into weekly deliverables and daily actions.
- **Task Prioritization:** Organize tasks using priority levels from P0 (critical) to P3 (optional).
- **Progress Tracking:** Read actual Notion Status or Checkbox fields to identify completed and unfinished tasks.
- **Weekly & Monthly Reviews:** Evaluate progress and identify what needs attention.
- **Task Rollover:** Reschedule unfinished tasks without deleting historical records.
- **Duplicate Prevention:** Help avoid creating repeated tasks when updating plans.

**Important:** This skill does not continuously monitor Notion or execute scheduled tasks on its own. An AI assistant needs authorized access to the user's Notion workspace. Recurring automatic reviews require a separate scheduling service.

## Project Files

| File | Description |
|---|---|
| [SKILL.md](SKILL.md) | Main reusable AI skill instructions |
| [QUICKSTART.zh-CN.md](QUICKSTART.zh-CN.md) | Chinese setup guide and example prompts |
| [notion_tasks_template.csv](notion_tasks_template.csv) | Reusable CSV template for a Notion task database |
| [LICENSE](LICENSE) | MIT open-source license |

All files are located in the repository's root directory.

## Quick Start

### 1. Get the Skill

Download this repository or open [SKILL.md](SKILL.md).

Copy the instructions into an AI assistant or agent that supports custom instructions or reusable skills, following that tool's setup process.

### 2. Prepare Your Notion Database

You can use an existing Notion task database or import the provided [Notion CSV template](notion_tasks_template.csv).

The recommended database structure is:

| Property | Purpose |
|---|---|
| Task | Task name and description |
| Category | Daily Plan / Weekly Plan / Monthly Plan |
| Date | Scheduled date or deadline |
| Priority | P0 / P1 / P2 / P3 |
| Status | Not Started / In Progress / Completed |
| Project | Related goal or project |
| Notes | Additional instructions or context |

The included CSV template uses Chinese column names. Confirm the property types after importing it into Notion.

### 3. Connect Your Notion Workspace

If you want an AI assistant to read or update tasks directly, connect your own Notion account through a supported integration and grant the necessary permissions.

Each user should connect their own workspace. This project does not include personal Notion data, credentials, or API keys.

### 4. Start Planning

Tell your AI assistant about your goals, deadlines, priorities, and available time.

The assistant can use the skill to structure your daily, weekly, and monthly plans.

### Example Prompt (Chinese)

```text
请使用 Notion Daily · Weekly · Monthly Planner Skill。

根据我的目标、截止日期和可用时间，
帮我建立每日、每周和本月计划。

要求：
1. 所有计划放在同一个 Notion 数据库中。
2. 按照每日计划、每周计划、本月计划分类。
3. 使用 P0–P3 设置优先级。
4. 根据实际完成状态追踪任务。
5. 保留历史记录，避免创建重复任务。
6. 每周复盘未完成事项，并制定下周计划。
7. 每月检查目标完成情况并调整下月计划。
```

## Planning Workflow

The skill follows a repeating planning cycle:

**Monthly Goals → Weekly Tasks → Daily Actions → Progress Tracking → Weekly Review → Monthly Review**

### Daily Planning

Break weekly tasks into realistic daily actions based on available time, urgency, and priorities.

### Weekly Planning

Review unfinished work, identify important deadlines, and distribute tasks across the coming week.

### Monthly Planning

Set broader goals, monitor progress, and adjust priorities based on actual results.

### Progress Reviews

Use the task database's actual Status or Checkbox values to determine completion. Do not assume that a task has been completed based only on its title or scheduled date.

## Design Principles

- **One Database:** Keep daily, weekly, and monthly plans in a single task database.
- **Three Categories:** Daily Plan → Weekly Plan → Monthly Plan.
- **Clear Priorities:** Use P0 for critical tasks and P3 for optional tasks.
- **Accurate Tracking:** Determine completion from actual task properties.
- **Preserve History:** Keep previous records when updating future plans.
- **Avoid Duplicates:** Check existing tasks before creating new ones.
- **User Control:** Do not modify or share private Notion content without authorization.
- **Realistic Scheduling:** Adjust workloads according to deadlines and available time.

## Limitations

- This is an **AI planning skill**, not an independently hosted application.
- It requires a compatible AI assistant to interpret and follow the instructions.
- Direct Notion updates require a supported Notion integration and appropriate permissions.
- The skill cannot monitor task changes continuously by itself.
- Automated scheduled reviews require an external scheduling tool.
- The initial version has not yet been validated through a formal external user study.

## Roadmap

- [ ] Add a complete English version of `SKILL.md`.
- [ ] Collect feedback from real users.
- [ ] Improve task prioritization and workload distribution.
- [ ] Expand setup examples and documentation.
- [ ] Improve task rollover and progress review guidance.

## Contributing

Feedback, suggestions, and contributions are welcome.

If you encounter an issue or have an idea for improvement, feel free to open a GitHub Issue.

Please remove personal information, private Notion URLs, and sensitive data before sharing examples.

## License

This project is licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for details.
