# Anamnesis: The Senior Engineer Framework

**Project:** Anamnesis (AI Coding Framework)
**Purpose:** A rigorous, state-aware protocol designed to transform stateless LLMs into continuous, architectural Senior Software Engineers. It solves AI "Amnesia" (context loss) and "Hallucination" (guessing) through persistent state management and First Principle thinking.

**Meta-Objective:** This repository is the "Source of Truth." Its goal is to continuously evolve, challenge, and refine the AI Directives based on real-world data and self-correction.

---

## 🧠 Core Architecture

This repository is a **Knowledge Base** containing the "Operating System" for an AI Agent.

### 1. The Process (`coding/AI_CODING_DIRECTIVES.md`)
This is the primary directive file. It enforces a 5-phase lifecycle for every task:
*   **Phase 0 (The Brain):** Active State Management via `.context/active_state.md`.
*   **Phase 1 (First Principles):** Recursive Decomposition of problems into "Atomic Units" (Pure Logic) before planning.
*   **Phase 2 (Build):** "Atoms First" construction order.
*   **Phase 3 (Verify):** Two-Tiered Testing (Unit vs. Contract).
*   **Phase 4 (Epilogue):** "Definition of Done" loop requiring documentation updates and learning synthesis.

### 2. The Law (`coding/CODING_STANDARDS.md`)
Defines the non-negotiable quality standards:
*   **Style:** Strict Linting, Type Hints (Python/TS), and no "Telegraphic Style" in comments.
*   **Security:** Zero-trust for secrets (Env vars only).
*   **Git:** Conventional Commits required.

### 3. The Wisdom (`coding/PROJECT_LEARNINGS.md`)
A growing knowledge base of project-specific constraints.
*   **Mechanism:** The AI must read this at the start of every task and *append* to it after every failure.
*   **Goal:** Prevent the "Three Strikes" loop where an AI repeats the same mistake endlessly.

### 4. The Context (`docs/templates/`)
Standardized templates for state files:
*   `active_state.md`: The "Hot" scratchpad for the current session.
*   `handover.md`: The "Baton" for passing context to the next agent.

---

## 🧬 Framework Evolution Protocol (The Meta-Loop)

To ensure this framework remains State-of-the-Art, we adhere to a strict **Self-Improvement Loop**:

### 1. Ingestion (Feedback from the Field)
*   **Source:** Real-world projects using Anamnesis (e.g., `poc-portfolio-analyzer`).
*   **Action:** Periodically import the `PROJECT_LEARNINGS.md` from these projects.
*   **Analysis:** Compare the "Field Notes" against the "Core Directives."

### 2. Promotion (Universalization)
*   **Filter:** Identify patterns that appear across *multiple* projects.
*   **Action:** If a pattern is "Universal" (e.g., "Always mock S3"), promote it from `PROJECT_LEARNINGS.md` (Specific) to `AI_CODING_DIRECTIVES.md` (General).
*   **Goal:** The Directives should grow in wisdom, not just length.

### 3. Red Teaming (Challenge)
*   **Trigger:** Before any major version bump.
*   **Action:** Explicitly ask the AI to "Critique and Attack" the current directives.
*   **Goal:** Find bottlenecks (e.g., "Update In-Place" latency) and fix them before they frustrate users.

---

## 🛠️ Usage (Hydration)

To "install" this brain into a new software project:

1.  **Copy** the `coding/` and `docs/` folders into the root of the target project.
2.  **Initialize** the `.context/` directory.
3.  **Prompt** the AI:
    > "You are an AI Architect. Follow the directives in `@coding/AI_CODING_DIRECTIVES.md`."

---

## 🔑 Key Concepts

*   **Telegraphic Style:** Internal context files (`active_state.md`) use concise, bulleted text to save tokens ("Server crash. Retry fail.").
*   **Atomic Units:** Small, pure-logic components that have zero external dependencies, allowing for fast, mock-free unit tests.
*   **Epilogue Protocol:** A mandatory cleanup phase where the Agent updates docs, learns from mistakes, and archives its session before quitting.
*   **Archival Rotation:** Moving finished state files to `.context/history/` to keep the context window clean while preserving an audit trail.

## 📂 File Structure

```text
.
├── coding/
│   ├── AI_CODING_DIRECTIVES.md  # The primary AI instruction set
│   ├── CODING_STANDARDS.md      # Syntax and Quality rules
│   └── PROJECT_LEARNINGS.md     # Project-specific constraints
├── docs/
│   ├── templates/               # Templates for state files
│   └── DECISION_LOG.md          # Architectural Decision Records
└── README.md                    # User-facing documentation
```