# [Project Name]

> **Root File:** This file is auto-loaded by AI CLI tools (OpenCode, Gemini CLI, Claude Code).
> Keep it concise (<100 lines). For detailed protocols, see referenced files.

---

## Project Overview

[2-3 sentences: What is this project? What problem does it solve?]

## Tech Stack

- **Language:** [e.g., Python 3.11+ / TypeScript 5.0+]
- **Framework:** [e.g., FastAPI / React 18 / None]
- **Database:** [e.g., PostgreSQL / SQLite / None]
- **Key Libraries:** [e.g., Pydantic, Zod]

## Directory Structure

```
[Customize per project]
src/           # Source code
tests/         # Test files
docs/          # Documentation
  specs/       # Specifications (SDD)
.context/      # AI session state
coding/        # AI framework files
```

---

## Working Protocol

### Golden Rules

1. **State Continuity:** Read `.context/active_state.md` at session start. Update before session end.
2. **Spec-Driven:** Complex tasks (>1 hour) require specs in `docs/specs/`. No code without spec.
3. **Consensus Gate:** Present plan summary and WAIT for user approval before coding.
4. **Epilogue:** Update docs, archive state, and synthesize learnings before ending.

### Escape Hatch

For simple questions or read-only tasks, skip the full protocol and act immediately.

### Progressive Disclosure

| When | Read |
|------|------|
| New idea, new feature, major refactor | `coding/THINKING_DIRECTIVES.md` |
| Complex bug (root cause unclear) | `coding/THINKING_DIRECTIVES.md` (Phase T1-RCA) |
| Implementation of defined plan | `coding/EXECUTION_DIRECTIVES.md` |
| Writing/reviewing code | `coding/CODING_STANDARDS.md` |
| Project-specific constraints | `PROJECT_LEARNINGS.md` |

---

## Common Commands

```bash
# [Customize per project]

# Build
[command]

# Test
[command]

# Lint
[command]

# Run
[command]
```

---

## Key Constraints

- [Project-specific constraint 1]
- [Project-specific constraint 2]
- [Add constraints from PROJECT_LEARNINGS.md as project evolves]

---

## Context Files

| File | Purpose |
|------|---------|
| `.context/active_state.md` | Current session state (hot) |
| `.context/handover.md` | Previous session summary (baton) |
| `.context/history/` | Archived session states |
| `PROJECT_LEARNINGS.md` | Cumulative project wisdom |
| `docs/specs/tasks.md` | Current execution plan |

---

## CLI Tool Configuration

**OpenCode:** Works natively with this file.

**Gemini CLI:** Add to `~/.gemini/settings.json`:
```json
{
  "context": {
    "fileName": ["AGENTS.md", "GEMINI.md"]
  }
}
```

**Claude Code:** Create `CLAUDE.md` with single line: `@AGENTS.md`
