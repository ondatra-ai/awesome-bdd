# 2. Terms and Definitions

Below are the terms proposed for use within this article to understand the philosophy and approach to using AI for creating software products. In other contexts, these terms should be approached and defined differently.

## Requirements

**Requirements** are everything users expect from software functionality and the declared value that this software should deliver to users.

Requirements can be functional and non-functional, as well as explicit and implicit.

In this sense, software development and maintenance are viewed as a process of constant changes in requirements.

The cycle looks like this: requirements change → code changes until it satisfies the new requirements → the process repeats indefinitely.

### Requirements Matrix (2×2)

Below is a requirements matrix that combines explicit/implicit with functional/non-functional:

|  | Functional | Non-Functional |
| ----- | ----- | ----- |
| **Explicit Requirements** | Documented User Stories, Epics, business rules. Example: "Save" button saves a record. | Documented SLAs. Example: page must load in less than 1 second. |
| **Implicit Requirements** | Standards that are usually not documented but still exist. Example: clear error messages on login, presence of a loader during long operations. | Commonly accepted must-haves. For example, absence of SQL injection vulnerabilities and the ability to monitor the system in real-time. |

## Quality of Software

The first parameter important for business is how well the software meets user expectations.

**Quality of Software** — the percentage of all requirements that are fulfilled. This cannot be calculated absolutely precisely because there are subjective requirements such as usability. User feedback is used here.

| What IS Software Quality | What is NOT Software Quality |
| :---- | :---- |
| Functionality working according to user expectations; expected interface behavior; interface beauty; interface convenience; compliance with security standards; meeting SLA uptime; optimal release frequency | The method by which this software is developed. Whether it's a monolith or not. Whether it uses CDN or not, uses cache or not. Whether it develops quickly or not. |

## Effort-to-Market (ETM)

The second important parameter for business is how expensive it is to make changes and how quickly this can be done.

**Effort-to-Market** — the amount of effort in terms of time, labor, and money required to implement requirement changes with the necessary quality.

## Quality of Code

Within this article (and this is critically important for using AI effectively), I propose defining code quality not by its internal characteristics but by external business parameters: **Quality of Software** and **Effort-to-Market**.

**Quality of Code** — how well the given code satisfies requirements now and how quickly and cheaply changes in requirements can be implemented in the future.

| What IS Code Quality | What is NOT Code Quality |
| :---- | :---- |
| Functionality working according to user expectations; expected interface behavior; interface beauty; interface convenience; speed and ease of making changes; scalability; performance | Use of programming patterns. Use of architectural patterns. Folder and class structure. |

## Deterministic and Non-deterministic Systems

In automation, there are two types of systems:

### Deterministic System

A system that, given the same input parameters, always produces a predetermined and predictable result. The main property of such a system is that it solves a problem that has been solved once, consistently.

Characteristics:
- Same inputs → same output
- Not creative
- Logic is predetermined

### Non-deterministic System (LLM)

A system whose result depends on context and randomness.

Characteristics:
- Result depends on context and chance
- Creative
- Poorly controlled "on the fly"

## System Development Efficiency (LLM)

I want to approach system efficiency as the idea that tasks are completed faster and with less effort using the system than without it.

