# Project Objective: Anamnesis Framework

> **Purpose:** To solve the core problems of AI-assisted coding (Amnesia, Hallucination, Vibe Coding, Monoliths) through a stateful, spec-driven framework.

---

## Current Focus

**Phase:** v4.2 Framework Restructuring

We are separating the "Meta-Project" (this repository, which develops the framework) from the "Distributable Framework" (the starter kit for new projects).

## Success Looks Like

- [x] **Separation:** `anamnesis_starter/` is a standalone, copy-pasteable directory.
- [x] **Cleanup:** Old `coding/` and `docs/product/` directories are removed.
- [ ] **Dogfooding:** This repository uses the new v4.2 structure itself.
- [ ] **Documentation:** `README.md` and `AGENTS.md` accurately reflect the new structure.

## Constraints

- **Meta-Project:** Changes here propagate to the definition of the framework.
- **Backwards Compatibility:** We should be careful about breaking changes for existing users (though v4.2 is a breaking change).
