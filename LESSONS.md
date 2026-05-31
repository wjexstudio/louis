# Lessons Learned

Reusable lessons from **Wasin × Claude** working sessions — distilled into principles that carry over to any task or project.

> This is **not the diary** (the diary lives in `diaries/` — story and feeling, written in Thai for Wasin to read). This file holds **actionable principles only**, in English because its reader is the AI.

---

## How to use this file

- **Before starting new work** → read the "Principles" section below.
- **At the end of a session with a lesson** → add an entry to the "Session Log".
- **If a lesson is generic enough** → promote it up into "Principles" (note which session it came from).

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

---

## Project conventions

This file is the **single source of truth**. Agent entry-point files (`CLAUDE.md`, and any future `.cursorrules` / `AGENTS.md`) are thin pointers here — do not duplicate content into them.

- **Language by reader:** AI-facing files → English. The AI Diary (`diaries/`) → Thai.
- **AI Diary** (`diaries/YYYY-MM-DD.md`): one file per day; read yesterday's before writing today's and build on it; use real Bangkok time from `TZ='Asia/Bangkok' date` (never guess); header is a bullet list (date / time / duration / session), not YAML frontmatter; timeline table has two columns only (time + event). Write the day's diary at the **end** of the day so it covers the whole day, not just the morning.
- **Retrospective** (`diaries/retrospective/YYYY-MM-DD.md`): a separate genre from the daily diary — a cross-cutting review written every few sessions, not every day. Keep analysis-of-the-diaries here, NOT in a daily entry (a diary that analyses the diaries is a mirror-in-a-mirror and deepens self-referential drift). Thai, since the reader is Wasin.
- **Repo contents:** `cv/wasin.html` (Wasin's CV, Thai), `cv/claude.html` (Claude's own CV, EN+TH), `README.md` (repo docs), `diaries/` (diary), `LESSONS.md` (this file), `CLAUDE.md` (pointer).

---

## Session Log

### 2026-05-31 — CV review + AI Diary system
**Context:** Started with a blunt review of the CV (now `cv/wasin.html`), then built the AI Diary in `diaries/`.

**What happened:** The diary work took ~4 rounds — (1) written but not pushed, so it was invisible; (2) guessed the time instead of running `date`; (3) chose YAML frontmatter that GitHub renders as an ugly table; (4) had to rework the timeline format and set up the everyday-diary system.

**Lessons →** distilled into Principles 1–8 above. Root cause: "executing instructions literally instead of understanding the real need from the start."

**Later in the same session:** discussed who actually reads `LESSONS.md` (answer: future-me, the AI — not the public) and that it should be wired into `CLAUDE.md` to guarantee it gets read; also decided AI-facing files should be English → Principle 9, and this file was translated to English.

**Outcome:** Set the diary convention (one file per day, read the previous day before writing, real timestamps from `date`, "less but real" format), created this `LESSONS.md`, and wired it into `CLAUDE.md`.

**Open work:** Fix CV issues 1–3 (experience ordering, duplicate entry, the "8+ years" overclaim).
