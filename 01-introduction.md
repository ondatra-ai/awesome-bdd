# 1. Introduction

This article examines an approach to automating custom software development using a combination of **deterministic** and **non-deterministic** systems.

## Definitions

**Deterministic systems** are traditional scripts and process orchestration tools that guarantee repeatability and task completion. They follow predictable patterns and produce consistent results.

**Non-deterministic systems** refer to LLM-based code generation tools such as Codex and Claude Code, which provide creativity and generate novel code solutions. Their outputs can vary based on context and have inherent randomness.

### Example in Practice

Consider implementing a new feature like user authentication. A **deterministic orchestration script** manages the entire workflow in predictable steps:

1. Takes the task specification
2. Calls the **LLM** (non-deterministic) to generate E2E tests from requirements
3. Runs the tests (they fail—feature not implemented yet)
4. Calls the **LLM** again to implement the feature based on failing tests
5. Runs tests again, captures failures
6. Calls the **LLM** to fix the code until tests pass
7. Runs the linter, calls the **LLM** to fix any issues
8. Validates everything passes, marks task complete

The **deterministic** part ensures the process always completes these steps in order and reaches a "done" state. The **non-deterministic LLM** provides creativity at each step—generating different test scenarios, various implementation approaches, or alternative fixes—but only when explicitly called. This combination gives you both control and innovation.

## The Goal

The material in this article focuses on how to connect these approaches to:

- **Reduce manual labor** in software development
- **Decrease Effort-to-Market (ETM)** — the time, effort, and cost required to implement changes
- **Maintain quality control** throughout the development process

By combining the reliability of deterministic orchestration with the creative power of LLMs, we can build a system that scales development efficiency while keeping quality standards high.

