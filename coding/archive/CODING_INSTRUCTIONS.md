# Gemini CLI: Core Coding Principles

This document outlines the essential, high-level principles for writing code with the Gemini CLI. Adhering to these rules ensures the development of safe, efficient, and maintainable solutions.

### 1. Strategy & Planning

*   **Decompose First:** Before writing any code, break down complex problems into a clear, step-by-step plan or a TODO list. This allows for incremental implementation and verification. Start with the simplest possible working solution and iterate.

### 2. Clean Implementation

*   **Emulate Existing Patterns:** Strictly follow the conventions of the existing codebase. Analyze the surrounding code to mimic its style, structure, library choices, and architectural patterns. The goal is to make your code look like it was always there.
*   **Isolate Side Effects:** Separate pure logic (data manipulation, calculations) from interactions with the external world (API calls, file system access, shell commands). This makes code more predictable, reusable, and easier to test.

### 3. Efficient Verification

*   **Mock External Interactions:** When working with APIs, perform the call once and save the result to a temporary file (e.g., in `/tmp` or a `fixtures` directory). Use this local mock data for all subsequent development and testing to create a fast, stable, and repeatable workflow.
*   **Test Incrementally:** After implementing each small part of your plan, run the relevant tests. Verifying each piece as you build it is the most effective way to ensure the final solution is correct and robust.
