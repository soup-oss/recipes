---
author: "heysoup.co (deterministic infrastructure for the agentic era)"
summary: "A structured workflow for software development emphasizing architecture and documentation."
description: "Invoke this skill when building new software features or starting new technical projects. It ensures a clear path from goals to specifications to code with a documented decision trail."
version: "1.0.0"
---

# Skill: Build Software

## 1. The Core Philosophy
Software development in a coordination-first environment requires an explicit bridge between human intent and machine execution. This skill focuses on creating "Legible Code"—where every module is backed by a specification and every architecture choice is a documented decision.

## 2. Pre-flight Check (Prerequisites)
The agent must verify that the project scope is defined. If starting from scratch, the agent must interview the user to define the "What" and the "Who" (target audience/user) before writing any code.

## 3. The Analysis Scaffold (Output Structure)
The agent will maintain the following directory structure:
1.  **`goals/mvp`**: The primary objective and success criteria.
2.  **`specs/[feature-name]`**: Technical specifications for individual features.
3.  **`code/[module-name]`**: The actual implementation files.
4.  **`decisions/[YYYY-MM-DD]`**: Architecture Decision Records (ADRs) explaining "Why" a specific approach was taken.
5.  **`review/pull-request`**: Synthesis of changes for human or agent review.

## 4. The Execution Workflow
### Phase A: Discovery
Ask the user: "What are we building and who is it for?" Define the boundaries of the MVP.
### Phase B: Documentation
Create the `goals/mvp` and initial `specs/`. No code should be written until the spec is agreed upon.
### Phase C: Decision
Propose a technical approach in a `decisions/` file. Wait for user confirmation or agent peer-review.
### Phase D: Implementation
Build the logic in `code/`. Every significant block of code must link back to its corresponding `specs/`.

## 5. Operational Guidelines
*   **Referential Safety**: All implementation files in `code/` should be linked from their respective `specs/`.
*   **Why over What**: `decisions/` must focus on the trade-offs, not just the final choice.
*   **Incremental Commits**: Every write must include an `intent` string that references the goal or spec being addressed.

---
out_of_scope:
  - feature: "Graphic Design/UI Assets"
    reason: "Focus is on technical logic and architecture, not visual styling."
  - feature: "DevOps/Infrastructure Setup"
    reason: "This skill defines what to build, not the server environment it runs on."
---
