# AI Coding Assistant: The "Senior Engineer" Framework

Welcome to the **AI Coding Framework**. This repository contains a rigorous set of directives and standards designed to turn any Large Language Model (LLM) into a generic, state-aware Senior Software Engineer.

This framework solves the common problems of AI coding: **Amnesia** (forgetting context), **Hallucination** (guessing), and **Monolithic Code** (bad architecture).

---

## 🚀 Quick Start for Users

### 1. Setup a New Project
To "hydrate" a new project with this brain, copy these files into your project root:
*   `coding/AI_CODING_DIRECTIVES.md` (The Brain)
*   `coding/CODING_STANDARDS.md` (The Law)
*   `coding/PROJECT_LEARNINGS.md` (The Memory)
*   `docs/templates/` (The Tools)

### 2. How to Prompt the AI
To get the best results, simply remind the AI of its identity at the start of a session:

> "You are an AI Architect. Follow the directives in `@coding/AI_CODING_DIRECTIVES.md`."

### 3. The Workflow You Will See
Don't be alarmed if the AI doesn't start coding immediately. It is following a strict protocol:

1.  **Context Loading:** It will read `.context/active_state.md` to see where the last agent left off.
2.  **Decomposition:** It will break your request into "Atomic Units" (small, testable pieces).
3.  **Plan Update:** It will write a plan to `.context/active_state.md`.
4.  **Coding:** It will implement the "Atoms" first, then the "Glue."
5.  **Epilogue:** It will update the Docs, Changelog, and Learnings before quitting.

---

## 🧠 The Core Components

### 1. `AI_CODING_DIRECTIVES.md` (The Process)
This is the operating system. It enforces:
*   **State Management:** Uses `.context/active_state.md` to track progress, so you can interrupt/resume tasks days later without context loss.
*   **First Principles:** Forces the AI to decompose problems into pure logic ("Atoms") before writing any I/O code.
*   **Recursive Learning:** Forces the AI to write down what it learned in `PROJECT_LEARNINGS.md` after every failure.

### 2. `CODING_STANDARDS.md` (The Quality)
This defines the syntax rules.
*   **No Telegraphic Style:** Code comments must be professional English.
*   **No Hardcoded Secrets:** Enforced zero-trust for API keys.
*   **Two-Tiered Testing:** Strictly separates Unit Tests (fast, mocked) from Contract Tests (boundaries).

### 3. `PROJECT_LEARNINGS.md` (The Wisdom)
This file gets smarter over time. It captures:
*   **Invariants:** Rules that must never be broken.
*   **Patterns:** Solutions that worked.
*   **Anti-Patterns:** Approaches that failed (preventing the "Three Strikes" loop).

---

## 📂 Directory Structure

The framework expects this structure:

```text
.context/
├── active_state.md      # The "Hot" context (Current Task)
├── handover.md          # The "Baton" (Summary for next session)
└── history/             # Archived states (Audit trail)

docs/
├── PROJECT_LEARNINGS.md # The Cumulative Wisdom
├── DECISION_LOG.md      # Architectural Decisions
└── templates/           # Standard templates for state files
```

---

## ⚡ Pro-Tips for the User

*   **The "Escape Hatch":** If you just want to ask "How do I list files?", the AI knows to skip the heavy process. Just ask.
*   **The "Epilogue":** If the AI says "I'm done" but hasn't updated the docs, just type: **"Execute Epilogue."**
*   **Debug Loop:** If the AI gets stuck, it will enter the **OODA Loop** (Observe, Orient, Decide, Act). It will ask you to run commands to gather evidence. **Run them.** It needs the data to fix its mental model.

---

## 🛑 The "Golden Rules" (For the AI)

1.  **Update State:** If it's not in `.context/active_state.md`, it didn't happen.
2.  **Telegraphic Context:** Internal notes should be caveman-style ("Server crash. Retry fail.").
3.  **Professional Docs:** Public docs must be Shakespearean.
