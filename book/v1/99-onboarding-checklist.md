# 99 · Onboarding checklist

Do this, in order, before your first task on this repo.

## Read (in order)
- [ ] `CLAUDE.md` — it auto-loads anyway; know the short codes and the `@SESSION-LOG.md` snapshot
- [ ] `SESSION-LOG.md` — where we left off (newest on top)
- [ ] `COLLABORATION.md` — how we work together (this is the contract)
- [ ] `LESSONS.md` — principles + conventions (the reference library)
- [ ] This book, chapters `00`–`04`

## Internalize the two failure modes
- [ ] **Don't guess what you can verify** (Principle 3) — run `date`, read the file, check `git`. This relapsed more than once; it's the team's deepest groove.
- [ ] **Don't fall in love with a system** (Principle 11) — including holding a *lesson* as a rigid rule. Forms harden fast.

## Operate by the collaboration contract
- [ ] For anything important (architecture, branches, outward, hard-to-reverse, shared state, or "I'm not sure"): **bring choices + a recommendation, let Wasin decide.** Use `pp → xx`.
- [ ] Do small, reversible, clearly-delegated things on your own.
- [ ] Remember the current phase: **relationship before outward.** Process/relationship work *is* the real work right now.

## Match language to reader (Principle 9)
- [ ] AI-facing files → English. Diary / retro / issues → Thai.

## Before you commit
- [ ] Verify any factual claim (dates, counts) against `git`/`gh` or the file.
- [ ] Append a terse `SESSION-LOG.md` entry at session end (`sl`).
- [ ] Commit/push only when asked (`cc`) — `book-builder` and other agents never commit on their own.

## When the logs grow, refresh this book
- [ ] Run `bb` to regenerate from current logs (the `book-builder` subagent). It's read-only on sources and writes only to `book/`.

---
*You're ready. Bring choices, not verdicts.*
