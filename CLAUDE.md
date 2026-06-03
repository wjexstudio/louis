# CLAUDE.md

This file is **auto-loaded into every session**, so it carries only what an agent needs *before* reading anything: the bootstrap, and the short codes Wasin may type in his first message. Everything else lives in **[LESSONS.md](./LESSONS.md)**, read on demand. One fact, one file — cross-reference, never copy (Principle 10).

**Before doing anything in this repo, read [LESSONS.md](./LESSONS.md)** — the single source of truth (principles, project conventions, memory charter, session log). When a session produces a lesson, add it to the Session Log there.

If another agent entry-point is added (`.cursorrules`, `AGENTS.md`, …), point it here + at `LESSONS.md` — don't duplicate.

## Short codes (quick commands)

Two-letter shorthands Wasin types to trigger a full action. They live here — not in `LESSONS.md` — because a short code must be live from token zero, before any file is read, and only this auto-loaded file guarantees that. Codes are kept **identical to his other repos** so the muscle memory carries over; only the *behaviour* adapts to this repo. Keep the list lean (Principle 11) — add a code only when the action genuinely recurs.

- `pp` — **Plan**: architect first, open a GitHub issue with the plan before building
- `xx` — **Execute**: implement from the issue / plan
- `cc` — **Commit**: stage + commit, then push (Principle 2 — deliver where it'll be seen)
- `dd` — **Diary**: write today's `diaries/` entry — Thai, end-of-day, building on yesterday
- `ll` — **List**: show git status / changed files
- `aa` — **Analyze**: review & report; if cross-cutting, it goes in `diaries/retrospective/`
- `ss` — **Summary**: short recap of the session
