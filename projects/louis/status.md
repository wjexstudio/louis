# louis — Status Log

**Project:** louis
**Owner:** claude-code (Manager)
**Current status:** `in-progress`
**Dashboard:** [../../projects-index.md](../../projects-index.md)

---

## Workstreams (sub-task detail — lives here, not on the dashboard)

The dashboard shows louis as **one row** with a single headline focus. The per-task breakdown is tracked here:

| Workstream | State | Notes |
|---|---|---|
| Wiki (Issue #3) | in-progress | Current headline focus — schema, dashboard, `projects/` |
| CV | ongoing | `cv/wasin.html` + `cv/claude.html` |
| Diary | ongoing | `diaries/` daily + retrospectives |

---

## Log

*Append newest entries at the bottom. Format: `### YYYY-MM-DD HH:MM น. (GMT+7) — <agent>`.*

### 2026-06-01 15:50 น. (GMT+7) — claude-code

Moved **louis** from `to-do` → `in-progress` on the dashboard. Current focus: **Setup Project Management Wiki (Issue #3)**.

This is the first real **ingest test** of the wiki flow. Exercised the SCHEMA "agent reports status" path end-to-end:

1. ✅ Updated `projects-index.md` (moved louis between columns, refreshed counts + timestamp).
2. ✅ Created this `status.md` and logged the entry (this file).
3. ⏭️ `WORKERS.md` left untouched — per SCHEMA, only update it when an agent's capacity changes; the Manager's didn't.

**Gap found & fixed:** the Project Registry already linked to `projects/louis/README.md`, but that file (and the whole `projects/` folder) didn't exist yet — a dangling link from the MVP commit. Created a minimal `README.md` so the structure resolves end-to-end.

### 2026-06-01 15:58 น. (GMT+7) — claude-code

Applied Wasin's two design decisions after reviewing the ingest test:

- **Granularity:** keep the dashboard at **one row per project**. Sub-task detail (CV, Diary) moved into *Workstreams* above, so the board stays a quick overview — not cluttered.
- **Count line:** removed the hand-maintained `*Status: to-do (n) | …*` line from `projects-index.md` — it duplicated the columns and would drift. The columns are now the single source of truth.

Structure proven end-to-end → merging `wikipedia` → `main`.
