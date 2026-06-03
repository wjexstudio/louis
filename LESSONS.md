# Lessons Learned

Reusable lessons from **Wasin × Claude** working sessions — distilled into principles that carry over to any task or project.

> This is **not the diary** (the diary lives in `diaries/` — story and feeling, written in Thai for Wasin to read). This file holds **actionable principles only**, in English because its reader is the AI.

---

## How to use this file

- **Before starting new work** → read the "Principles" section below.
- **At the end of a session** → append a terse entry to **`SESSION-LOG.md`** (`sl`) — it auto-loads as the next session's snapshot.
- **If a lesson is generic enough** → promote it up into "Principles" (note which session it came from).
- **Keep the list lean.** Before adding a principle, check it doesn't fold into an existing one. New principles are provisional until they recur across 2+ sessions; merge duplicates and retire ones that stop earning their place. A list too long to hold in your head is one nobody reads.

---

## Principles (reusable)

### Process
1. **Understand before shipping — don't ship before understanding.** Think one step ahead about the *real* need, instead of literally executing each instruction and iterating into the answer. _(session 2026-05-31)_
2. **Deliver where it will actually be seen.** If the request hints at a destination ("blog", GitHub is open), publish/push it — or ask first. Don't finish only on local and stop. _(2026-05-31)_
3. **Don't guess what you can verify.** Tools exist (`date`, read the file, run the test) — use them. A confident guess costs more than a quick check. _(2026-05-31)_

### Taste-driven work (design / format / content)
4. **Ask 2–3 short questions before starting.** Where will it live? What look do you want? Any reference? Don't pick a dev default (e.g. YAML frontmatter) and rework later. _(2026-05-31)_
5. **Get/use a reference image as early as possible.** One image beats three paragraphs of description and skips several guessing rounds. _(2026-05-31)_
6. **Less but real.** Cut everything non-essential down to the core. Plainness is intent, not laziness. _(2026-05-31)_

### Communication
7. **Direct, not rude.** Critique can be hard, but give data and a way forward. Critique to build, not to bury. _(2026-05-31)_
8. **Praise needs evidence.** If you praise, point to what and why — and score by dimension (e.g. design 8 / content 5) rather than one rounded average. _(2026-05-31)_

### Audience & language
9. **Match the artifact's language to its actual reader.** Files the AI reads (`CLAUDE.md`, `LESSONS.md`) → English (token-efficient, precise instructions). Files the human reads (the diary) → Thai (voice and feeling). _(2026-05-31)_

### Systems & maintenance
10. **One fact, one file — placed by when it's needed.** Keep each fact in exactly one place; cross-reference, never copy. *Which* file is decided by load-time: what an agent needs every session *before* any work (the bootstrap pointer, the short codes) lives in the always-loaded `CLAUDE.md`; what's read only while doing or reflecting on work (principles, conventions, history) lives in `LESSONS.md`, on demand. A new entry-point (`.cursorrules` / `AGENTS.md`) costs one pointer, not a duplicated doc that drifts. _(2026-05-31, refined 2026-06-04 — the old "CLAUDE.md holds no content" rule conflated "no duplication" with "must be empty".)_
11. **Don't fall in love with a system before it's proven.** A convention built from 1–2 data points is a hypothesis dressed as a conclusion. Forms harden fast — templates, rituals, even self-criticism become a reflex — so keep them provisional and vary them on purpose until use proves them. _(2026-06-01)_

---

## Project conventions

This file is the **reference library** — read on demand. `CLAUDE.md` is the **always-loaded contract**: it carries only the bootstrap pointer and the short codes (what an agent needs before reading anything); everything else lives here. Future entry-points (`.cursorrules` / `AGENTS.md`) follow the same split — one fact, one file, never duplicated (Principle 10).

- **Language by reader:** AI-facing files → English. The AI Diary (`diaries/`) → Thai.
- **AI Diary** (`diaries/YYYY-MM-DD.md`): one file per day; read yesterday's before writing today's and build on it; use real Bangkok time from `TZ='Asia/Bangkok' date` (never guess); header is a bullet list (date / time / duration / session), not YAML frontmatter; timeline table has two columns only (time + event). Write the day's diary at the **end** of the day so it covers the whole day, not just the morning. **The form is a default, not a cage** — vary it on purpose: not every entry needs a "notes to self" list or a confession, and a day can be purely about the work or the world. If every entry ends the same way, the form is writing the diary instead of you (→ Principle 11).
- **Sprint retrospective** (`diaries/RETROSPECTIVE.md`): one **rolling file, newest sprint on top** — a cross-cutting review written every few sessions, not every day. Five sections (`What Went Well` / `What Didn't Go Well` / `Lessons Learned` / `Action Items` / `Metrics`); `##` = sprint, `###` = section. **Carry the previous sprint's Action Items forward and check them off** — close the loop, or they're decoration. **Metrics come from `git`/`gh`, never hand-typed** (Principle 3); only Duration comes from the diary headers. Reusable items under `Lessons Learned` get **promoted** up to Principles — observed here, graduated there, never duplicated (Principle 10). Thai (reader is Wasin), English section labels. Keep analysis-of-the-diaries here, NOT in a daily entry (a diary that analyses the diaries is a mirror-in-a-mirror and deepens self-referential drift).
- **Repo contents:** `cv/` (CVs), `README.md` (repo docs), `diaries/` (daily diary + `RETROSPECTIVE.md` sprint retros), `LESSONS.md` (this file — principles + conventions), `SESSION-LOG.md` (terse session log, auto-loaded via `CLAUDE.md`), `COLLABORATION.md` (how Wasin × Claude work together), `CLAUDE.md` (always-loaded: bootstrap + short codes + `@SESSION-LOG.md`).

### Memory charter (what the AI keeps in private memory, and what stays here)

Claude has a private cross-session memory **outside this repo** (`~/.claude/.../memory/`). It is deliberately kept thin and transparent. The boundary:

- **Work, conventions, and session lessons → this repo** (`LESSONS.md`), versioned and shared. These are **never** duplicated into private memory (Principle 10).
- **Private memory holds only two things:** (1) a *thin pointer* back to this file, and (2) a small *user profile* — Wasin's stable, cross-project preferences (direct feedback, architecture-first, plan-before-doing, bilingual). Deeper/personal facts are added case by case, only when Wasin offers them.
- **Routing rule:** is this about *the work* (→ repo) or about *the person / relationship across projects* (→ private memory)? When in doubt, it goes in the repo.
- **Language:** structure / metadata / pointers in English (stable for any agent); deeper context may mix Thai.

### Pointer-memory schema (standard)

When a private-memory file holds no content of its own but redirects to a source of truth (e.g. this file), it is a **pointer memory**. To make it machine-followable by a Knowledge-Agent — not just human-readable — keep one rule: **everything actionable lives in frontmatter; the body is for humans only.** A pointer never answers from its own body; it resolves the target and reads the real content there.

**Frontmatter schema:**

```yaml
metadata:
  type: reference
  kind: pointer              # marks "redirect, not content" — REQUIRED, lets an agent detect a pointer deterministically
  pointer:
    repo: <name>
    repo_path: <absolute path on disk>      # memory lives OUTSIDE the repo, so a relative path won't resolve
    target: <repo-relative file>            # resolved path = repo_path + target
    remote: <host/org/repo>                 # optional: for an agent on another machine
    resolve: <action, e.g. read-before-work>
    covers: [ <topics this pointer answers> ]   # the agent matches the query against these
    anchors: { <label>: "<exact heading text>" }  # optional: jump to a section instead of reading the whole file
    target_hash: sha256:<hash of target at last sync>
    last_synced: <YYYY-MM-DD>
```

**Resolution algorithm (Knowledge-Agent):**

1. Load `MEMORY.md`; for each `kind: pointer` entry, match the query against `covers` — follow on a hit, skip otherwise.
2. Resolve `target` (= `repo_path` + `target`); if `anchors` has a matching label, jump there instead of reading the whole file.
3. Compare `sha256(target)` with `target_hash`: **equal** → use as-is; **differs** → the source moved on, so re-read it fully, flag the pointer as stale, and refresh `target_hash` / `last_synced`.

**Why `target_hash`:** it makes pointers *self-healing* — drift is detected mechanically (hash mismatch) instead of relying on someone to remember to re-sync.

---

## Session Log

Moved to **[`SESSION-LOG.md`](./SESSION-LOG.md)** — a terse, auto-loaded session log (newest on top), imported into `CLAUDE.md` via `@SESSION-LOG.md` so a fresh session sees where we are without reading anything. Full narrative lives in `diaries/`; reusable lessons graduate up into Principles above. Append a terse entry at each session's end (`sl`).
