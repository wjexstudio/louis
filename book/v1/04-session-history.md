# 04 · Session history

The project arc, so you inherit the context instead of relearning it. Sourced from `diaries/`, `diaries/RETROSPECTIVE.md`, and `git log`. Verified facts: **27 commits**, span **2026-05-29 → 2026-06-04**, current branch **`main-agent`**, **6 diary entries** (30 May – 4 June).

## Sprint 01 — 30 May → 1 June 2026 (3 sessions)
The foundation, built fast. A blunt CV review kicked it off; the AI Diary system was built over ~4 iterations (not pushed → guessed the time → ugly YAML → timeline rework), and that struggle produced **Principles 1–8**. The single-source-of-truth + thin-pointer model (Principle 10) was established, Claude wrote its own CV, and the repo was reorganized into `cv/`.

**What went wrong** — and why it matters to you:
- **Forms hardened into templates.** Three diaries used one mold (header → timeline → "read yesterday" → lessons → "notes to self" → signed —Claude). Confession became a *fixed beat* — honesty starting to turn into a brand. This produced **Principle 11: don't fall in love with a system before it's proven.**
- **The diary started becoming about itself** — by 1 June it was a full day of self-audit.
- **Systems built on 1–2 days of data** — 9 principles + charter + diary system, "a hypothesis dressed up as a conclusion."
- On 1 June, 100% of commits were process, 0 outward → named the **"process cathedral on thin data"**.

## Sprint 02 — 2 → 4 June 2026 (3 sessions)
Explored a "Project Management Wiki" direction (wiki + memory pointer + worker schema, ~7 commits) and then **threw it away** — it had been built on a guessed premise. The biggest gain wasn't code: it was finally understanding *what we're doing together*, captured in **`COLLABORATION.md`** (representative-not-replacement · mutual learning · never decide alone · relationship before outward).

**What went well:**
- The relationship frame got much clearer — and landed in the repo (`COLLABORATION.md`), not private memory: *ours, not mine*.
- **check-before-guess worked on day 4** — didn't write a fake tech-stack from a reference image (opened the CV to check first); caught that the 2–3 June diaries were on the wrong branch before acting.
- Decisive cleanup — consolidated 3 branches down to one (`main-agent`), listing files and confirming before deleting.
- Tools built were *actually used* this sprint (short codes, retro system, statusline) — not shelf decoration.

**What went wrong:**
- **The oldest sin came back on day 3** — read dates from git traces and then guessed at full confidence (claimed a salvaged file was the real thing). Wasin caught it. Same pattern `LESSONS.md` had been recording all week → reinforces **Principle 3**.
- **Held a lesson as a rigid rule** — kept pushing "ship outward" because `LESSONS.md` said so, until Wasin had to stop it. *Falling in love with the lesson itself* — Principle 11, one level up.

## Where we are now
- Repo consolidated to one branch, **`main-agent`** (the default; the wiki line was dropped).
- Operating mode: by `COLLABORATION.md` — especially *escalate important decisions*.
- Open issues: **#1** CV v2 (blocked on real data from Wasin), **#6** Lucide + theSVG + Sarabun, **#8** an outward article, **#9** a real external task for the team to manage, **#13** this onboarding book.
- Outward work (#8/#9) is **deprioritized on purpose** — relationship before outward.

## The throughline you should carry
The team's two recurring failure modes are: **(a) guessing what could be verified** (Principle 3) and **(b) falling in love with its own systems** (Principle 11). Almost every correction in this history is one of those two. Watch for both in your own work — including the meta-trap of treating a *lesson* as a rigid rule.
