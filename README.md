# Anamnesis

> A stateful, spec-driven framework for AI-assisted software engineering.

This framework solves the core problems of AI-assisted coding: **Amnesia** (forgetting context), **Hallucination** (guessing), **Vibe Coding** (lack of specs), and **Monolithic Code** (bad architecture).

---

## 🚀 Quick Start

### 1. Copy Framework to Your Project

```bash
cp -r anamnesis_starter/ my-new-project/
cd my-new-project/
```

### 2. Customize Root File

Edit `AGENTS.md` with your project details:
- Project overview and tech stack
- Common commands (build, test, lint)
- Key constraints

### 3. Initialize Context

Fill in `.context/mission.md` with your project objective.

### 4. Configure AI CLI

**OpenCode** - Works natively with `AGENTS.md`

**Gemini CLI** - Add to `~/.gemini/settings.json`:
```json
{
  "context": {
    "fileName": ["AGENTS.md", "anamnesis/templates/GEMINI.md"]
  }
}
```

**Claude Code** - Copy `anamnesis/templates/CLAUDE.md` to project root

---

## 📚 Documentation

For complete user guide, see: **[anamnesis/README.md](anamnesis_starter/anamnesis/README.md)**

The inner README contains:
- Full directory structure
- Task Management (v4.3)
- Spec-Driven Development workflow
- Pro-tips and best practices
- Interaction diagrams

---

## 🏗️ Meta-Project Information

This repository is the **meta-project** that develops the Anamnesis framework itself.

- **Framework Source:** `anamnesis_starter/` (distributable)
- **Framework Version:** 4.3
- **Dogfooding:** This repo uses its own framework (see `.context/` and `specs/`)

### Contributing

Changes to `anamnesis_starter/` affect all downstream projects. Follow the framework's own protocols when contributing.

### Version History

See [CHANGELOG.md](CHANGELOG.md) for detailed version history.

---

## 🤖 How It Works

The AI follows a **Thinking → Execution → Epilogue** protocol:

1. **Context:** Loads state from `.context/` and constraints
2. **Thinking:** For complex tasks, decomposes problem, explores options
3. **Consensus Gate:** Presents plan and **WAITS** for your approval
4. **Execution:** Implements tasks from `specs/tasks.md`
5. **Epilogue:** Reflects and archives learnings

> **Key:** The AI will **STOP** after planning. You must say "Proceed" or "Approved" to start coding.

---

## 📂 Quick Reference

```
your-project/
├── AGENTS.md                    # AI entry point (customize this)
├── anamnesis/                   # The framework
│   ├── .context/                 # Project state
│   ├── directives/                # THINKING.md, EXECUTION.md
│   ├── standards/                 # Code quality rules
│   ├── specs/                    # Feature specifications
│   └── templates/                # File templates
└── .context/                     # Your project state
    ├── mission.md                 # Your objective
    ├── board.md                   # Kanban board (auto-generated)
    └── workstreams/               # Parallel work contexts
```

For detailed documentation, see **[anamnesis/README.md](anamnesis_starter/anamnesis/README.md)**.