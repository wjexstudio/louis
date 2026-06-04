# 03 · Conventions

How to actually operate in this repo. Source of truth: `LESSONS.md` → "Project conventions". This chapter is the working summary.

## Language by reader (Principle 9)
- **AI-facing** files → **English**: `CLAUDE.md`, `LESSONS.md`, `SESSION-LOG.md`, this book.
- **Human-facing** → **Thai**: the diary (`diaries/`), retrospectives, GitHub issues. Section *labels* in retros stay English.

## Short codes
Two-letter commands Wasin types to trigger a full action. They live in `CLAUDE.md` (must be live from token zero). Kept identical across his repos for muscle memory; only the *behavior* adapts here.

| code | action |
|------|--------|
| `pp` | **Plan** — architect first, open a GitHub issue with the plan before building |
| `xx` | **Execute** — implement from the issue / plan |
| `cc` | **Commit** — stage + commit, then push |
| `dd` | **Diary** — write today's `diaries/` entry (Thai, end-of-day, building on yesterday) |
| `ll` | **List** — git status / changed files |
| `aa` | **Analyze** — review & report; if cross-cutting → `diaries/RETROSPECTIVE.md` |
| `ss` | **Summary** — short recap of the session |
| `sl` | **Session log** — append a terse entry (done · state · next) to `SESSION-LOG.md` |
| `bb` | **Build book** — regenerate this onboarding book from logs (runs `book-builder`) |

Keep the list lean (Principle 11) — add a code only when the action genuinely recurs.

## The diary (`diaries/YYYY-MM-DD.md`)
One file per day, **Thai**. Read yesterday's before writing today's and build on it. Use real Bangkok time from `TZ='Asia/Bangkok' date` — never guess (Principle 3). Header is a bullet list (date / time / duration / session), not YAML. Timeline table has two columns (time + event). Write at the **end** of the day so it covers the whole day. **The form is a default, not a cage** — vary it; not every entry needs a "notes to self" or a confession. If every entry ends the same way, the form is writing the diary instead of you.

## Sprint retrospective (`diaries/RETROSPECTIVE.md`)
One rolling file, **newest sprint on top** — written every few sessions, not daily. Five sections: `What Went Well` / `What Didn't Go Well` / `Lessons Learned` / `Action Items` / `Metrics`. `##` = sprint, `###` = section. **Carry the previous sprint's Action Items forward and check them off.** **Metrics come from `git`/`gh`, never hand-typed** (Principle 3). Reusable items under `Lessons Learned` get **promoted** up to `LESSONS.md` Principles. Keep analysis-of-the-diaries here, not in a daily entry.

## CLAUDE.md vs LESSONS.md (the load-time split)
`CLAUDE.md` is the **always-loaded contract** — only the bootstrap pointer, the short codes, and `@SESSION-LOG.md`. `LESSONS.md` is the **read-on-demand reference** — principles, conventions, memory charter. A new entry-point (`.cursorrules`, `AGENTS.md`) costs *one pointer*, not a duplicated doc (Principle 10).

## Memory charter
Claude has a private cross-session memory **outside this repo**, kept thin and transparent:
- **Work, conventions, lessons → this repo** (`LESSONS.md`), versioned and shared. Never duplicated into private memory.
- **Private memory holds only:** a thin *pointer* back to the repo, and a small *user profile* (Wasin's stable cross-project preferences).
- **Routing rule:** about *the work* → repo; about *the person/relationship across projects* → private memory. When in doubt → repo.

See `LESSONS.md` for the full pointer-memory schema (`target_hash` self-healing).
