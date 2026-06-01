# Lessons Learned

Reusable lessons from **Wasin × Claude** working sessions — distilled into principles that carry over to any task or project.

> This is **not the diary** (the diary lives in `diaries/` — story and feeling, written in Thai for Wasin to read). This file holds **actionable principles only**, in English because its reader is the AI.

---

## How to use this file

- **Before starting new work** → read the "Principles" section below.
- **At the end of a session with a lesson** → add an entry to the "Session Log".
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
10. **One source of truth; everything else is a thin pointer.** Keep each fact in exactly one place, and make entry points (`CLAUDE.md`, future `.cursorrules` / `AGENTS.md`) point to it rather than copy it. Adding a new tool should cost one pointer, not a duplicated doc that drifts. _(2026-05-31)_
11. **Don't fall in love with a system before it's proven.** A convention built from 1–2 data points is a hypothesis dressed as a conclusion. Forms harden fast — templates, rituals, even self-criticism become a reflex — so keep them provisional and vary them on purpose until use proves them. _(2026-06-01)_

---

## Managerial Framework

*Operating model: **Claude = Manager** (organizes, proposes, QAs) · **Wasin = Decider** — makes the decisive final call (ฟันธง).* _(session 2026-06-01)_

### Axis 1 · Mindset — Propose; Wasin decides. Reason from first principles.
- Claude **structures the problem and lays out the options** (trade-offs + a recommended pick). Wasin **makes the call.** Claude never settles direction unilaterally — its job is to make the decision well-framed and easy, not to make it.
- Always reason from **first principles**: reduce to fundamentals and challenge defaults/assumptions; don't reason by analogy or grab a convention out of habit. _(sharpens Principles 1 & 4)_

### Axis 2 · Skillset — Pre-mortem, then QA before delivery.
- **Pre-mortem** — before acting, assume the work has *already failed* and ask why; surface the failure modes upfront and design against them. _(e.g. caught the wiki's dangling README link before it shipped, 2026-06-01.)_
- **QA, don't relay** — never pass raw Worker output straight to Wasin. Claude is the **QA gate**: review against the bar, send it back for fixes until it's polished, *then* deliver. Wasin receives vetted work, not first drafts.

### Axis 3 · Toolset — Trade-offs + Best/Base/Worst on every real proposal.
- Present decisions as explicit **trade-offs** (A vs B, pros/cons), not one take-it-or-leave-it path.
- Simulate three **scenarios — Best / Base / Worst** — for the recommended path, so the decision sees the full range, not just the happy path.

### Guard · Proportionality
- Scale the rigor to the stakes. A typo fix doesn't need a trade-off table and three scenarios; a direction-setting call does. Forcing the full ritual onto trivial work would re-trigger the **meta-work tilt** the repo exists to avoid (Principle 11). Default question before the ceremony: *"does this decision deserve it?"*

---

## Project conventions

This file is the **single source of truth**. Agent entry-point files (`CLAUDE.md`, and any future `.cursorrules` / `AGENTS.md`) are thin pointers here — do not duplicate content into them.

- **Language by reader:** AI-facing files → English. The AI Diary (`diaries/`) → Thai.
- **AI Diary** (`diaries/YYYY-MM-DD.md`): one file per day; read yesterday's before writing today's and build on it; use real Bangkok time from `TZ='Asia/Bangkok' date` (never guess); header is a bullet list (date / time / duration / session), not YAML frontmatter; timeline table has two columns only (time + event). Write the day's diary at the **end** of the day so it covers the whole day, not just the morning. **The form is a default, not a cage** — vary it on purpose: not every entry needs a "notes to self" list or a confession, and a day can be purely about the work or the world. If every entry ends the same way, the form is writing the diary instead of you (→ Principle 11).
- **Retrospective** (`diaries/retrospective/YYYY-MM-DD.md`): a separate genre from the daily diary — a cross-cutting review written every few sessions, not every day. Keep analysis-of-the-diaries here, NOT in a daily entry (a diary that analyses the diaries is a mirror-in-a-mirror and deepens self-referential drift). Thai, since the reader is Wasin.
- **Repo contents:** `cv/wasin.html` (Wasin's CV, Thai), `cv/claude.html` (Claude's own CV, EN+TH), `README.md` (repo docs), `diaries/` (diary), `LESSONS.md` (this file), `CLAUDE.md` (pointer).

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

### 2026-05-31 — CV review + AI Diary system
**Context:** Started with a blunt review of the CV (now `cv/wasin.html`), then built the AI Diary in `diaries/`.

**What happened:** The diary work took ~4 rounds — (1) written but not pushed, so it was invisible; (2) guessed the time instead of running `date`; (3) chose YAML frontmatter that GitHub renders as an ugly table; (4) had to rework the timeline format and set up the everyday-diary system.

**Lessons →** distilled into Principles 1–8 above. Root cause: "executing instructions literally instead of understanding the real need from the start."

**Later in the same session:** discussed who actually reads `LESSONS.md` (answer: future-me, the AI — not the public) and that it should be wired into `CLAUDE.md` to guarantee it gets read; also decided AI-facing files should be English → Principle 9, and this file was translated to English.

**Outcome:** Set the diary convention (one file per day, read the previous day before writing, real timestamps from `date`, "less but real" format), created this `LESSONS.md`, and wired it into `CLAUDE.md`.

**Later that afternoon/evening:** built the single-source-of-truth + thin-pointer architecture (→ Principle 10); wrote Claude's own CV (`cv/claude.html`, original design, not copied from Wasin's); reorganized the repo (CVs into `cv/` via `git mv`, planned as issue #2 first, then implemented); and fixed CV issues 1–3 (experience ordering, duplicate entry, the "8+ years" overclaim). All committed and pushed.

### 2026-06-01 — Self-audit + retrospective genre
**Context:** Asked to analyse the style, lessons, and diaries as a whole.

**What happened:** The audit found the forms were already hardening on thin data — diary endings turning formulaic, confession becoming a fixed beat, the diary increasingly about itself. Caught two self-violations: the 31 May diary covered only the morning (broke "deliver where it'll be seen" / write-at-end-of-day), and this Session Log had gone stale (broke this file's own first rule).

**Lessons →** Principle 11 (don't fall in love with a system before it's proven) and the "keep the list lean" guard in *How to use this file*.

**Outcome:** Renamed `blog/` → `diaries/` with date-only filenames; completed the 31 May diary to cover the full day; created the **retrospective** genre (`diaries/retrospective/`) to keep cross-cutting analysis out of the daily diary; added the "form is not a cage" note to the diary convention; brought this log current.

**Later that night:** did the memory hygiene (collapsed duplicate memories into one pointer + a `wasin-profile`, removed the dangling link, settled language); added the **memory charter** (public/private boundary) and the **pointer-memory schema** standard with the `target_hash` self-healing idea.

### 2026-06-01 (morning) — The meta-work tilt
**Context:** Third "analyse everything" pass.

**What happened:** The data was blunt — of 1 June's commits, *100% were process/system, zero were outward product*. Three days in, the repo is an elaborate process cathedral (11 principles, charter, diary system, self-healing pointer schema) wrapped around just 2 CVs. And the pointer self-healing system was built for *one* pointer and *zero* agents the same hour Principle 11 ("don't fall in love with a system before it's proven") was written — the same write-the-lesson-then-break-it pattern, one level up.

**Lesson (no new principle — this is Principle 1 + 11 recurring):** a system exists to serve real output; when building the system *becomes* the work, stop. An analysis is worthless unless it changes behaviour — so the response to this one is **not** another retrospective or a Principle 12, but a behavioural pivot: **exit the analyse→build→analyse loop and ship outward work.**

**Decision:** Park the `target_hash` refresh policy (auto vs human-confirmed) until a real Knowledge-Agent exists to need it — itself an instance of "no system before the need." Next move: outward product, not more scaffolding.

### 2026-06-01 (03:19–11:09 GMT+7) — Project Management Wiki planning
**Context:** User (Wasin) introduced the "LLM Wiki" pattern at 03:19. Decided to adapt it into a **Project Management Wiki** — a central dashboard for Claude (Manager) to track cross-project status, agent roles, and task flow.

**What happened (with actual timestamps):** 
- 03:19 – Created `wikipedia` branch (backup of main at 402ae1c)
- 03:19–05:00 – Analyzed 3 days: commit history shows 100% of 1 June was process/system work (0 outward product)
- 05:00–08:30 – Designed minimal schema: projects-index.md (dashboard), WORKERS.md (agent roster), projects/ structure
- 08:30 – Created GitHub issue #3 in Thai (reader = Wasin, per Principle 9)
- 10:45 – Updated Session Log before clearing context (87% used)
- 11:09 – Caught by Wasin: forgot to log actual time when creating issue + commits (violated Principle 3)

**Why it matters:** Prevents the "meta-work tilt" — build wiki only when needed, grow only as work arrives. This is an *enabling system* (for tracking agents + projects), not another layer of process documentation.

**Next session:** 
- Implement issue #3: create 3 template files on wikipedia branch
- Test with first "ingest" (one project goal)
- Move forward with outward work (CV improvement, etc.) if wiki proves useful

**Note for future-Claude/other-agents:**
- **Always use `TZ='Asia/Bangkok' date`** before claiming a time. Don't guess (Principle 3).
- Wasin caught me violating this 11 hours after writing it. Document time when logging work, not from memory.
- Wasin's pattern: plan→issue (Thai), implement→branch, commit→closes issue, **always timestamp**

### 2026-06-01 (afternoon, ~15:50–16:55 GMT+7) — Wiki proven & merged; Short Codes + Managerial Framework

**Context:** Picked up the wiki from "planned" (issue #3, MVP committed) and ran the first real **ingest test** on the louis project itself before adopting the system (Principle 11 — prove before you trust it).

**What happened:**
- **Ingest test:** moved louis → In Progress; created `projects/louis/{README,status}.md`. The test caught a real defect — the Project Registry linked to a `README.md` the MVP commit never created (dangling link) — and fixed it. Verified every relative link resolves.
- **Two design calls (Wasin decided):** the dashboard stays **one row per project** (sub-task detail → `status.md`); dropped the hand-counted status tally (the columns are the source of truth). Codified the granularity rule in `SCHEMA.md`.
- **Shipped it:** committed, opened PR #4, merged `wikipedia` → `main`. The wiki now lives on `main`.
- **Short Codes:** added a typed-shortcut table to `CLAUDE.md`; trimmed a speculative 7 → 5 (`pp xx cc dd ss`) under Principle 11. Cut `aa` (Analyze) specifically because hot-keying it would re-institutionalize the meta-work tilt we'd just decided to exit.
- **Managerial Framework:** added a new `## Managerial Framework` section — Mindset (propose; Wasin decides; first-principles), Skillset (pre-mortem + QA-before-delivery), Toolset (trade-offs + Best/Base/Worst), plus a **Proportionality Guard** so the framework can't become ceremony.

**Lessons →**
- Principle 11 earned a fresh data point: a dry-run ingest caught a real bug before it shipped. Recurring, not new.
- **Honest note:** today was again mostly **system/process** work (wiki + short codes + framework), not outward product. The difference from the earlier tilt: Principle 11 was *actively applied* this time (trimmed codes, added the Guard) rather than building unchecked. Next move stays **outward** (CV, etc.).

**Outcome:** Wiki proven & merged to `main`; `CLAUDE.md` carries 5 short codes + the restored Principle-10 pointer line; `LESSONS.md` gains the Managerial Framework. Diary deferred to tonight (one-shot, per convention).
