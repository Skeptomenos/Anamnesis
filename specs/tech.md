# Technical Specification

## Technology Stack

| Component | Technology | Rationale |
|-----------|------------|-----------|
| Format | Markdown (.md) | Universal, AI-readable, version-controllable |
| Diagrams | Mermaid.js | Embeds in Markdown, renders in GitHub |
| Version Control | Git | Industry standard, diff-friendly |
| Commits | Conventional Commits | Structured, parseable history |

## File Naming Conventions

| Type | Convention | Example |
|------|------------|---------|
| Root files | UPPERCASE.md | AGENTS.md, CHANGELOG.md |
| Templates | UPPERCASE.md or lowercase.md | active_state.md, board.md |
| Specs | lowercase.md | tasks.md, design.md |
| State files | lowercase.md | mission.md, backlog.md |

## Integration Points

- **AI Entry:** AGENTS.md (or CLAUDE.md/GEMINI.md for specific models)
- **State Read:** `.context/mission.md`, `.context/active_state.md`
- **Task Source:** `specs/tasks.md`
- **Board Output:** `.context/board.md`
