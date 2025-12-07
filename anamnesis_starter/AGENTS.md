# [Project Name]

> **Root File:** Auto-loaded by AI CLI tools. Keep concise (<80 lines).

## Overview

[2-3 sentences: What is this? What problem does it solve?]

## Tech Stack

- **Language:** [e.g., Python 3.11+]
- **Framework:** [e.g., FastAPI]
- **Database:** [e.g., PostgreSQL]

## Structure

```
src/               # Source code
tests/             # Tests
anamnesis/         # AI framework
├── .context/      # Session state
├── directives/    # THINKING.md, EXECUTION.md
├── standards/     # Code quality rules
├── specs/         # Feature specifications
└── templates/     # Recreatable file templates
```

---

## Protocol

### Golden Rules

1. **State:** Read `anamnesis/.context/mission.md` at session start
2. **Specs:** Complex tasks (>1hr) require `anamnesis/specs/`. No code without spec.
3. **Consensus:** Present plan, WAIT for approval before coding
4. **Epilogue:** MANDATORY after feature/design completion.
5. **NO IMPLEMENTATION WITHOUT APPROVAL:** Do NOT write, edit, or delete any files until user explicitly says "go ahead", "proceed", "do it", or similar. Planning and reading are always allowed. Coding requires explicit green light.
   - **HANDSHAKE RULE:** You CANNOT plan and implement in the same response.
     If you just finished planning → STOP. Do not continue to implementation.

> **ESCAPE HATCH:** Simple questions or read-only tasks → skip protocol, act immediately.

### When to Read

| Task | File |
|------|------|
| Session start | `anamnesis/.context/mission.md` |
| New feature, refactor | `anamnesis/directives/THINKING.md` |
| Complex bug | `anamnesis/directives/THINKING.md` (T1-RCA) |
| Implementation | `anamnesis/directives/EXECUTION.md` |
| Code review | `anamnesis/standards/INDEX.md` |
| Project constraints | `anamnesis/PROJECT_LEARNINGS.md` |

---

## Commands

```bash
# Build: [cmd]    Test: [cmd]    Lint: [cmd]    Run: [cmd]
```

## Constraints

- [Project-specific constraint 1]
- [Project-specific constraint 2]

## State Files

`anamnesis/.context/active_state.md` (current) | `anamnesis/.context/handover.md` (previous) | `anamnesis/specs/tasks.md` (plan)
