# Mitc HQ Notion

This repo belongs to the Mitc company project below. Keep HQ Notion honest when you work here (Cursor, cloud agent, or Grok Bot).

## Project
- **Company:** Ullas opskrifter
- **HQ Project:** https://app.notion.com/p/3e0bceba2b21816882e4e638d298cb38
- **HQ Tasks database:** https://app.notion.com/p/3e0bceba2b2180aa9e29cb4d447148bf
- **HQ Projects database:** https://app.notion.com/p/3e0bceba2b2180749cdbe4a7846a20c7

## Rules (short)
These apply to every agent working in this repo: Grok Bot fleet bots, Cursor, Claude Code, or any other coding agent.
1. Before starting real work: create or reuse an HQ **Task** with **Project** = this company, **Kind=Task**, and set **Status=In progress** the same day.
2. **In progress only while someone is actively working on it.** If it's waiting on Svend, a client, a secret, a login or another task, set **Blocked** and fill in **Blocked on** with one line. If it's queued or paused, set **Up next** (P0/P1) or **Not started**. Shipped and live-checked means **Done**. Merged but not yet deployed stays **In progress**.
3. **Comment on every status move.** Add a page comment on the Task in this form:
   `<d Mon HH:MM CET>, <old> → <new>, <who>: <one-line reason or PR link>`
   Example: `14 Nov 20:09 CET, Up next → In progress, Claude Code: started PR #12`. The comments are the task's timeline, so never move a card without one.
4. Every PR body must include this line:
   `Notion: https://app.notion.com/p/<task-page-id>`
   (the alias `HQ-Task:` also works).
5. Use the Notion MCP or connector. **If you have no Notion access**, put these lines in the PR body (or the final report), and the fleet will apply the status move and the comment for you:
   `Notion-status: <old> → <new>`
   `Notion-comment: <one-line reason>`
6. Forever watches and holds are **Kind=Standing**, not board noise.
7. No secrets, private personal or health facts, or invented public contacts on HQ cards.

## Gold standard
Denmark Globe Project page shape is the template for briefs.
