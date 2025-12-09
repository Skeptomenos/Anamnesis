# Anamnesis

> A stateful, spec-driven framework for AI-assisted software engineering.

> **⚠️ META-PROJECT:** This IS the framework source. Changes propagate to all downstream projects.

## Overview

Anamnesis solves core AI-assisted coding problems:
- **Amnesia** → Persistent state (`.context/`)
- **Hallucination** → Spec-Driven Development (`specs/`)
- **Vibe Coding** → Consensus Gates
- **Monolithic Code** → Atomic decomposition

**Version:** 4.3

## Tech Stack

- **Format:** Markdown (.md)
- **Diagrams:** Mermaid.js
- **Version Control:** Git with Conventional Commits

## Repository Structure

```
knowledge_base/                    # META-PROJECT (this repo)
├── anamnesis_starter/             # DISTRIBUTABLE STARTER (copy to new projects)
│   ├── anamnesis/                 # The framework
│   │   ├── .context/              # Project state
│   │   │   ├── workstreams/       # Parallel work contexts
│   │   │   ├── mission.md         # Living objective
│   │   │   ├── backlog.md         # Deferred ideas
│   │   │   └── tech-stack.md      # Approved tools
│   │   ├── directives/
│   │   │   ├── THINKING.md        # First Principles & Design
│   │   │   └── EXECUTION.md       # Build & Deliver
│   │   ├── docs/
│   │   │   └── MIGRATION.md       # Version migration guide
│   │   ├── specs/                 # Feature specifications
│   │   │   └── tasks.md           # Implementation plan (v4.3 format)
│   │   ├── standards/
│   │   │   ├── INDEX.md           # Quality rules index
│   │   │   ├── global.md          # Language-agnostic
│   │   │   ├── python.md          # Python-specific
│   │   │   └── typescript.md      # TypeScript-specific
│   │   ├── templates/
│   │   │   ├── board.md           # Kanban board template
│   │   │   └── workstream.md      # Workstream context template
│   │   ├── DECISION_LOG.md
│   │   ├── PROJECT_LEARNINGS.md
│   │   └── README.md
│   ├── AGENTS.md                  # AI entry point
│   └── CHANGELOG.md
├── specs/                         # Meta-project specifications
│   ├── tasks.md                   # Implementation plan
│   ├── problem.md                 # Problem statement
│   ├── product.md                 # Product definition
│   ├── requirements.md            # Requirements
│   ├── design.md                  # Design specification
│   ├── options.md                 # Options analysis
│   └── tech.md                    # Technical specification
├── docs/research/                 # Framework research (meta-project only)
├── .context/                      # This project's state
│   ├── workstreams/               # Parallel work contexts
│   ├── board.md                   # Auto-generated kanban
│   ├── mission.md                 # Living objective
│   ├── handover.md                # Session handover
│   └── backlog.md                 # Deferred ideas
├── AGENTS.md                      # THIS FILE (meta-project entry)
├── CHANGELOG.md
├── DECISION_LOG.md
├── PROJECT_LEARNINGS.md
└── README.md
```

---

## Protocol

### Golden Rules

1. **State:** Read `.context/active_state.md` at start, update at end
2. **Non-Destructive:** Never delete documentation—append or refine
3. **Naming:** UPPERCASE.template.md for root files, lowercase for specs
4. **Epilogue:** MANDATORY after feature/design completion. Includes reflective thinking (T-RFL), not just documentation.
5. **Dogfooding:** This project follows its own framework
6. **NO IMPLEMENTATION WITHOUT APPROVAL:** ⚠️ CRITICAL ⚠️
   - Planning, reading, and research: ALWAYS allowed
   - Writing, editing, or deleting files: REQUIRES explicit user approval
   - You MUST present your plan and ask "Ready to proceed?" or similar
   - WAIT for user to say "go", "proceed", "do it", "yes", or clear equivalent
   - Do NOT interpret your own confidence or plan completeness as approval
   - **HANDSHAKE RULE:** You CANNOT plan and implement in the same response.
     If you just finished planning → STOP. Do not continue to implementation.

> **Models prone to eager execution:** This means YOU. Plan. Present. Ask. Wait.

> **ESCAPE HATCH:** Simple questions or read-only tasks → skip protocol, act immediately.

### When to Read

| Task | File |
|------|------|
| Session start | `anamnesis/.context/mission.md` + `anamnesis/.context/active_state.md` |
| New feature, refactor | `anamnesis/directives/THINKING.md` |
| Complex bug | `anamnesis/directives/THINKING.md` (T1-RCA) |
| Implementation | `anamnesis/directives/EXECUTION.md` |
| Code review | `anamnesis/standards/INDEX.md` |
| Python code | `anamnesis/standards/global.md` + `anamnesis/standards/python.md` |
| TypeScript code | `anamnesis/standards/global.md` + `anamnesis/standards/typescript.md` |
| Project constraints | `PROJECT_LEARNINGS.md` |

> **Note:** For this meta-project, reference files inside `anamnesis_starter/anamnesis/`. For downstream projects, paths are simply `anamnesis/...`.

---

## Commands

```bash
git status                    # Check state
git diff                      # Review changes
ls anamnesis_starter/         # Inspect distributable framework
```

## Constraints

- **Meta-project** - Changes affect all downstream projects
- **Append-only** - Never delete sections without permission
- **Template naming** - Conventions must be followed

## State Files

`.context/active_state.md` (current) | `.context/handover.md` (previous) | `PROJECT_LEARNINGS.md` (wisdom)

## Long-Term Context

| File | Purpose | Update Frequency |
|------|---------|------------------|
| `.context/mission.md` | Living objective, evolves with understanding | When objective pivots significantly |
| `.context/backlog.md` | Deferred ideas and future work | When parking ideas for later |
| `DECISION_LOG.md` | Architectural decisions | When making structural choices |
| `PROJECT_LEARNINGS.md` | Process wisdom and constraints | After completing work (Epilogue) |

## Task Management (v4.3)

### Task States

| Status | Meaning | Next Action |
|--------|---------|-------------|
| `Backlog` | Idea captured, not prioritized | Prioritize or park |
| `Open` | Ready to work, dependencies met | Start work |
| `In Progress` | Currently being worked on | Complete or block |
| `Blocked` | Cannot proceed, waiting | Resolve blocker |
| `Done` | Verified complete | Archive when ready |
| `Archive` | Historical reference | None |

### Rules

1. **Check dependencies** before starting any task
2. **One task In Progress** at a time per workstream
3. **Update status immediately** when state changes
4. **Archive completed tasks** periodically to reduce noise

### User Commands

| Command | Action |
|---------|--------|
| "Generate board" | Regenerate `.context/board.md` from `specs/tasks.md` |
| "Next task" | Suggest highest-priority Open task with met dependencies |
| "Switch to [workstream]" | Change active workstream context |
| "Archive done tasks" | Move Done tasks to Archive section |


