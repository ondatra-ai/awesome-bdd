# Applying LLMs to Automate Custom Software Development

An awesome list and comprehensive guide on leveraging Large Language Models (LLMs) to automate custom software development through the combination of deterministic and non-deterministic systems.

## Content

1. [Introduction](01-introduction.md)
   - Overview of combining deterministic and non-deterministic systems
   - Reducing Effort-to-Market (ETM) while maintaining quality control

2. [Terms and Definitions](02-terms.md)
   - Requirements (functional/non-functional, explicit/implicit)
   - Quality of Software
   - Effort-to-Market (ETM)
   - Quality of Code
   - Deterministic and Non-deterministic Systems

3. [Problem Statement](03-problem-statement.md)
   - Current limitations of LLM in production software development
   - Challenges with repeatability and control
   - The need for a hybrid approach

4. [Solution](04-solution.md)
   - Deterministic orchestration with LLM creativity
   - "One-pass" approach to task formulation
   - E2E tests as problem definition
   - Review cycles for improving task formulation

   4.1. [Orchestration Without API: Deterministic Scripts](04-1-orchestration.md)
   
   4.2. [Tools and Recommendations](04-2-tools.md)

5. [Metrics](05-metrics.md)
   - Software Quality measurement
   - Effort-to-Market (ETM) tracking
   - Code Quality assessment
   - One-pass solution rate
   - Economic metrics

6. [Conclusion](06-conclusion.md)
   - Summary of the deterministic-orchestration + LLM approach
   - Scalability and control considerations

## About

This repository explores a philosophy and approach to using AI for creating software products. The core idea is to combine:

- **Deterministic systems** (scripts, process orchestration) that guarantee repeatability and task completion
- **Non-deterministic systems** (LLM-based code generation tools like Codex and Claude) that provide creativity and new code generation

The goal is to reduce manual labor, decrease Effort-to-Market, and maintain quality control throughout the software development lifecycle.

## License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.
