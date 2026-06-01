# CLAUDE.md

**Read [LESSONS.md](./LESSONS.md) before doing anything in this repo.** It is the single source of truth — principles, project conventions, and the session log. When a session produces a lesson, add it to the Session Log there.

If another agent-entry file is added (`.cursorrules`, `AGENTS.md`, …), make it a thin pointer to `LESSONS.md` too — never duplicate content (Principle 10).

## Short Codes

Typed shortcuts that fire a known workflow — send the code on its own as the message.

| Code | Action |
|---|---|
| `pp` | **Plan** — create a GitHub issue for the work (Thai, per Principle 9) |
| `xx` | **Execute** — read the issue I name (e.g. `xx 3`), open a branch, implement |
| `cc` | **Commit** — commit (with `closes #N` when relevant) **and** push |
| `dd` | **Diary** — write the day's diary (read yesterday first, real Bangkok time, end-of-day) |
| `ss` | **Summary** — summarize the current session into the Session Log (`LESSONS.md`) |
