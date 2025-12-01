# Anamnesis

> A stateful, spec-driven framework for AI-assisted software engineering.

> **⚠️ META-PROJECT WARNING:**
> This IS the framework source. Changes here propagate to all downstream projects.
> Exercise extra caution when modifying `coding/` files.

---

## Project Overview

Anamnesis solves the core problems of AI-assisted coding:
- **Amnesia** → Persistent state management (`.context/`)
- **Hallucination** → Spec-Driven Development (`docs/specs/`)
- **Vibe Coding** → Consensus Gates and structured protocols
- **Monolithic Code** → Atomic decomposition and modularity

**Version:** 3.1

## Tech Stack

- **Format:** Markdown (.md)
- **Diagrams:** Mermaid.js
- **Version Control:** Git with Conventional Commits

## Directory Structure

```
coding/                      # The Framework (distributable)
├── AI_CODING_DIRECTIVES.md  # Core process (v3.1)
├── CODING_STANDARDS.md      # Quality rules (v3.1)
└── templates/               # All templates (13 files)

docs/                        # Research and documentation
.context/                    # Session state management

Root:
├── AGENTS.md                # This file (root context)
├── README.md                # User documentation  
├── PROJECT_LEARNINGS.md     # Framework evolution
├── DECISION_LOG.md          # Architectural decisions
└── CHANGELOG.md             # Version history
```

---

## Working Protocol

### Golden Rules

1. **State Continuity:** Read `.context/active_state.md` at session start
2. **Non-Destructive:** Never delete documentation - append or refine
3. **Consistency:** Follow naming conventions (UPPERCASE.template.md, lowercase spec_*)
4. **Version Tracking:** Update version refs when making significant changes

### Escape Hatch

For simple questions or read-only tasks, skip the full protocol and act immediately.

### Progressive Disclosure

| When | Read |
|------|------|
| Modifying framework | `coding/AI_CODING_DIRECTIVES.md` |
| Writing documentation | `coding/CODING_STANDARDS.md` |
| Understanding history | `PROJECT_LEARNINGS.md` |

---

## Common Commands

```bash
# This is a documentation project - no build/test commands

# Git workflow
git status
git diff
git log --oneline -10

# Template inspection
ls coding/templates/
```

---

## Key Constraints

- **Meta-project** - Changes affect all downstream projects using this framework
- **Append-only docs** - Never delete existing sections without explicit permission
- **Template naming** - UPPERCASE.template.md for root files, lowercase for specs
- **Dogfooding** - This project follows its own framework

---

## Context Files

| File | Purpose |
|------|---------|
| `.context/active_state.md` | Current session state |
| `.context/handover.md` | Previous session summary |
| `PROJECT_LEARNINGS.md` | Framework evolution history |
| `DECISION_LOG.md` | Architectural decisions |
