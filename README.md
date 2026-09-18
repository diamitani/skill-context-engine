# skill-context-engine

![Category: Project Management](https://img.shields.io/badge/category-Project%20Management-blue) ![Status: Active](https://img.shields.io/badge/status-active-brightgreen)

A Universal AI Agent Skill that turns ephemeral Claude sessions into a persistent, searchable memory layer. Instead of losing context every time a conversation ends, this skill automatically saves, compresses, indexes, and retrieves session history across conversations — so you always know where you left off.

---

## What It Does

- **Saves session context** — Captures what happened, what worked, what failed, decisions made, and next steps into a structured JSON record at the end of every session
- **Context flash** — Instantly loads your last session summary so you can pick up exactly where you left off with a single phrase
- **Progress reports** — Generates structured markdown reports across multiple sessions (weekly summaries, troubleshooting logs, decision journals)
- **Searchable index** — Queries past sessions by tag, keyword, date range, or tool name so you can find "when we fixed the Clay webhook" without scrolling through old chats
- **Scheduled memory** — Can trigger automatic session reports on a recurring schedule (daily, weekly) to keep a running log of all project activity

---

## How to Use

1. Install the skill file (`SKILL.md`) into your `.claude/skills/context-engine/` directory
2. Open Claude Code in any project
3. Use any trigger phrase (see below) — Claude will automatically enter the right mode
4. Session data is stored in `.context-engine/` in your project root and persists across all future sessions

**Storage structure created automatically:**
```
.context-engine/
├── sessions/        # One .json file per session
├── index/
│   └── master.jsonl # Append-only index of all sessions
├── reports/         # Generated markdown reports
├── cache/
│   └── last.json    # Quick-load snapshot of most recent session
└── CONTEXT.md       # Human-readable running state doc
```

---

## Trigger Phrases

| Phrase | What happens |
|---|---|
| `"save this session"` / `"cache what we did"` | Saves current session to the index |
| `"context flash"` / `"what did we work on"` | Loads last session and shows what to do next |
| `"generate a report"` / `"progress report"` | Builds a structured markdown report across sessions |
| `"find when we fixed X"` / `"search sessions for..."` | Queries index by keyword, tag, or date |
| `"schedule weekly report"` | Sets up recurring auto-reports |
| `"what's our current state"` / `"recap what worked"` | Quick status read from CONTEXT.md |
| `"troubleshooting log"` / `"memory report"` | Full session history with failures and blockers |

---

## Category

Project Management

---

## Author: Patrick Diamitani

GTM AI & Automation Manager at Enterprise Platform — building skills and agent workflows for teams of 50+ non-technical users.

- GitHub: [diamitani](https://github.com/diamitani)
- LinkedIn: [linkedin.com/in/diamitani](https://linkedin.com/in/diamitani)

---

> Built with Claude Code · Part of the [Patrick's Skills Library](https://github.com/diamitani)
