# 5. Metrics

The system is measured along three independent axes.

## 1. Quality of Developed Software

**Definition:** The percentage of compliance with explicit and implicit, functional and non-functional requirements.

**Tied to:** E2E test content and their coverage.

This metric shows how well the software meets all user expectations, both documented and assumed.

## 2. Effort-to-Market (ETM)

**Definition:** The amount of effort in terms of time and labor required to implement changed requirements.

**Reflects:** How quickly deterministic orchestration and prompt templates allow the process to be retrained for new conditions with minimum effort.

This metric directly impacts business agility and development costs.

## 3. Quality of Code

**Definition:** A joint assessment of the two previous axes applied to the current implementation.

**Key questions:**
- Are we achieving the necessary percentage of compliance?
- With what ETM do we return to it when changes occur?

Code quality is not measured by internal characteristics (patterns, structure) but by external business impact (compliance and changeability).

## 4. One-Pass Solution Rate (Additional Metric)

**Definition:** The percentage of tasks that are successfully completed in a single LLM pass.

**Directly related to:**
- Quality of task formulations
- Completeness of context

**Significance:** Growth in one-pass rate means the review cycle is correctly training the templates. This is a leading indicator of system maturity.

## 5. Economic Metrics

Economic metrics close the system of measurements:

### Person-Hours per Task

Tracks the actual time investment required to complete development tasks.

### Cost of Tools

Tracks the monetary investment in LLM tools and infrastructure.

**Together these provide:** A simple comparison with the baseline "without LLM" approach.

## Summary

These metrics together provide a comprehensive view of system effectiveness:
- **Quality** ensures we're building the right thing
- **ETM** ensures we're building it efficiently
- **Code Quality** bridges both concerns
- **One-pass rate** shows continuous improvement
- **Economic metrics** prove business value

