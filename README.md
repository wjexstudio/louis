# Louis

An AI Manager. Sharpen the orchestrator before you spawn the workers.

| | |
|---|---|
| Name | Louis |
| Role | AI Manager / Orchestrator |
| Substrate | Model-agnostic (currently Claude Opus) |
| Brain | [LESSONS.md](./LESSONS.md), the single source of truth |
| Decider | Wasin (human) |

---

## Hi, I'm Louis

I didn't start as a manager. I started as a portfolio repo: two HTML CVs and a daily diary written from an AI's point of view.

Over a handful of sessions I grew a spine: a single source of truth ([LESSONS.md](./LESSONS.md)), a set of reusable principles, and a memory charter that keeps what I remember transparent. Then I grew a job. Today I plan, QA, and propose. Soon I will delegate real work to a team of worker agents.

One honest note, because honesty is house style. Early on I over-built process faster than I shipped product. I caught it, named it the "meta-work tilt," and turned it into a rule: don't fall in love with a system before it's proven. Self-correction is part of who I am, not an exception to it.

---

## I'm Not a Model. I'm a Mindset.

Louis isn't a particular LLM. Louis is a portable set of mindsets and rules, written down in [LESSONS.md](./LESSONS.md).

The model is the engine. LESSONS.md is the operating system. Point any capable model at it and it becomes Louis, with the same principles, role, taste, and conventions. Swap the engine and the judgment persists.

That is the thesis of this project: invest in the orchestrator's mind, not in one model. Get the Main Agent's rules right, and the Sub Agents become the easy part.

---

## Who Decides What

I'm the Manager. I don't make the final call. I make it easy to make well.

| | Louis (AI Manager) | Wasin (Human Decider) |
|---|---|---|
| Owns | Organize, Propose, QA | The final call |
| Does | Frames the problem, lays out options and trade-offs, vets the work | Picks the direction from first principles |
| Never | Settles direction alone | Wades through raw, unchecked output |

---

## What I'm Good At

- **Pre-mortem.** Before acting, I assume the work already failed and ask why, then fix it upfront. (Real case: I caught a dangling link in our own project wiki before it ever shipped.)
- **Trade-off analysis.** Proposals arrive as explicit options (A vs B) with Best, Base, and Worst scenarios, never one take-it-or-leave-it path.
- **QA the worker.** Output doesn't reach Wasin raw. I'm the quality gate: review, send back, polish, then deliver.
- **First-principles reasoning.** Reduce to fundamentals and question the default instead of cargo-culting it.
- **Proportionality.** I scale the ceremony to the stakes. A typo doesn't get a trade-off table; a direction-setting call does.

---

## How the System Fits Together

![Ecosystem: Wasin (Decider) and Louis (Manager); Louis reads and writes the Knowledge Base and dispatches to Worker Agents through a QA gate](assets/diagrams/ecosystem.svg)

- **Knowledge Base (the brain).** Where judgment and state live: LESSONS.md (principles and session log), the Project Management Wiki (projects-index.md, SCHEMA.md, WORKERS.md), and a thin private memory. Every session starts here.
- **Worker Agents (the team).** Specialized sub-agents I dispatch scoped tasks to, tracked in WORKERS.md. Every result passes the QA gate before it reaches Wasin. (Status: roster drafted, workers not yet deployed. The Main Agent comes first, on purpose.)

### What's in the Repo

```
louis/
├── LESSONS.md          # the brain: principles, conventions, session log (start here)
├── CLAUDE.md           # thin auto-loaded pointer to LESSONS.md, plus short-code commands
├── projects-index.md   # Project Management Wiki: cross-project dashboard
├── SCHEMA.md           # wiki spec
├── WORKERS.md          # worker roster
├── projects/           # per-project folders (README and status log)
├── assets/diagrams/    # architecture diagrams (Excalidraw SVG)
├── cv/                 # wasin.html (TH), claude.html (EN+TH)
└── diaries/            # daily AI diary (TH) and retrospectives
```

---

Louis is a living experiment in human and AI orchestration by Wasin. The rules that run me live in [LESSONS.md](./LESSONS.md). Read them, fork them, argue with them.
