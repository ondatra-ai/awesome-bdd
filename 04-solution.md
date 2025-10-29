# 4. Solution

Automating development requires both repeatability and the ability to generate something new. Repeatability is provided by deterministic cycles, where the order of steps and completion criteria are defined by code. The ability to create new things is provided by a non-deterministic system (LLM), which inserts creative content at the necessary points.

## Architectural Principle

The architectural principle is simple: **deterministic orchestration manages the process from idea to deployment**, while **LLM is engaged only where result variability is needed** (formulating user stories, designing interfaces, selecting implementations, refactoring under constraints).

## One-Pass Task Formulation

For this principle to produce predictable results, the task for the LLM must be formulated "for one pass." The model is poorly controlled mid-execution, so correcting its responses on the spot is inefficient.

Consequently, the entire managed layer — context preparation, prompt structure, expected response format — must be fixed in advance in deterministic code and templates. This way, we move variability to strictly designated points and keep all cycles and checks controlled.

## E2E Tests as Problem Definition

LLMs are better at solving problems than constructing solutions from scratch, so first you need to create a verifiable "problem." This role is fulfilled by end-to-end tests.

### Two-Step Process

1. **First step:** E2E tests are formed from the specification, describing system behavior at the level of user scenarios. These tests intentionally fail because the function is not yet implemented.

2. **Second step:** LLM changes the code, not the tests, until all tests pass. This way, we fix the readiness criterion in advance and eliminate "adjusting" the verification to the implementation.

## Deterministic Orchestration

Orchestration of the entire process remains in the deterministic layer. Scripts in TypeScript/Go manage the order of steps, extract context from the repository and PRs, generate prompts from templates, call LLM as a CLI subprocess, and record results.

This guarantees:
- Completion of each cycle
- Reproducibility: if an error occurs somewhere, you can deterministically roll back the state (to branch/PR deletion), adjust the task formulation, and restart the cycle with updated context

## Review Process

After each pass, a review is required. Its purpose is not to correct the LLM response "on the spot," but to improve the task formulation for the next run.

### Review Workflow

1. Review can be done by a human or another LLM
2. Remarks are saved
3. Current result is canceled
4. Then identified conditions, edge cases, and format requirements are added to templates and context

Thus, each iteration increases the probability of success "from the first try" in the next cycle.

## Focused Manual Control

Finally, manual control concentrates not on the generated code, but on the quality of E2E tests. This scales: the volume of code can grow by orders of magnitude, but the layer of user scenarios remains manageable and controllable.

**If tests are correct and fully cover requirements, passing tests serves as an objective "done" criterion.**

