# Project Management Wiki — Schema & Workflow

**Owner:** Claude (AI Manager)  
**Purpose:** Central dashboard for tracking projects, agents, and task flow  
**Last updated:** 2026-06-01

---

## How This Wiki Works

The wiki has 3 layers:

1. **projects-index.md** — single source of truth, cross-project dashboard
2. **projects/<PROJECT-SLUG>/** — individual project folders (README.md + status.md)
3. **WORKERS.md** — agent roster with roles & capacity

---

## Status Levels

- `todo` — not started
- `in-progress` — actively worked on
- `blocked` — waiting on something
- `done` — completed

---

## Granularity

The dashboard tracks **one row per project** — its current headline focus only. Per-task detail (e.g. louis's CV / diary / wiki workstreams) lives in that project's `status.md`, so the board stays a fast overview, not a task tracker. The hand-counted status tally line was dropped for the same reason — the columns are the source of truth. _(decided 2026-06-01, first ingest test)_

---

## Update Flows

### When a goal arrives (Wasin → Claude)
1. Add to `projects-index.md` (To-Do section)
2. Create project folder if substantial: `projects/<PROJECT-SLUG>/README.md`
3. Note owner (agent name) and due date (if any)

### When an agent reports status
1. Update status in `projects-index.md` (move between columns as needed)
2. Append to `projects/<PROJECT-SLUG>/status.md` with timestamp & agent name
3. Update `WORKERS.md` if agent's capacity changed

---

## File Format Standards

**Dates:** ISO 8601 (YYYY-MM-DD)  
**Times:** Bangkok timezone, 24hr (HH:MM น.)  
**Timestamps:** When logging, always use `TZ='Asia/Bangkok' date` (Principle 3)  
**Format:** Markdown only, links are relative (`../projects/...`)

---

## Maintenance

- Lint monthly: check for stale entries, contradictions, orphan projects
- Archive completed projects: move to `projects/archive/` if not active
- Keep index updated: it's the only dashboard people see
