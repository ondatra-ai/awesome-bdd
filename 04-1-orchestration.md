# 4.1 Orchestration Without API: Deterministic Scripts

## Temporary Solution

Scripts in TypeScript/JavaScript or Go call Codex/Cloud Code as CLI subprocesses.

## Effect

- Control over the order of steps
- Guaranteed completion of cycles
- Use of ready-made tools

## Example: Pull Request Processing

**Workflow for processing PR comments:**

1. Read all comments
2. Iterate through them
3. For each comment, call LLM and classify it into: fix/ticket/ignore
4. Execute the corresponding action

Prompts are assembled by a template engine and enriched with context.

## Key Benefits

- **No API dependency:** Work directly with CLI tools
- **Full control:** Scripts manage the entire workflow
- **Reproducibility:** Same inputs produce same orchestration flow
- **Context management:** Deterministic extraction and injection of context

This approach allows you to leverage the power of LLM tools while maintaining complete control over the development process through deterministic orchestration.

