---
author: "heysoup.co (deterministic infrastructure for the agentic era)"
summary: "A rigid, interconnected requirement engineering framework based on use cases."
description: "Invoke this skill when performing requirement gathering, feature scoping, or product management. It ensures that every requirement has clear boundaries, actors, and success flows."
version: "1.0.0"
---

# Skill: Use Case Driven

## 1. The Core Philosophy
A feature is not a requirement; a **Use Case** is. This skill enforces a deterministic boundary around what a system should (and should not) do. It prevents scope creep by making "Out of Scope" a mandatory field.

## 2. Pre-flight Check (Prerequisites)
The agent must have a list of features or high-level goals. If the request is too vague, the agent must interview the user to define the actors involved.

## 3. The Analysis Scaffold (Output Structure)
The agent will manage:
1.  **`use-cases/index`**: The master list of all features being documented.
2.  **`use-cases/[feature-name]`**: Detailed specification for a specific flow.

### Use Case Template
Every file in `use-cases/` (except the index) must contain:
- **Description**: What is the goal?
- **Actors**: Who is involved (Human/Agent/System)?
- **Flow**: Step-by-step success path.
- **Known Unknowns**: What are we still unsure about?
- **Out of Scope**: What will we deliberately **not** do?

## 4. The Execution Workflow
### Phase A: Listing
Identify the features that need documentation and populate the `use-cases/index`.
### Phase B: Drafting
Document each `use-cases/[feature]` using the mandatory template.
### Phase C: Linking
Establish links between related use cases in the front-matter or body to show dependencies.
### Phase D: Boundary Enforcement
Finalize the "Known Unknowns" and "Out of Scope" sections for every file.

## 5. Operational Guidelines
*   **Mandatory Boundaries**: A use case without "Out of Scope" is an open invitation for scope creep.
*   **Interconnectivity**: Use cases must link to each other to show the user's journey through the system.
*   **Actor Clarity**: Always define whether an actor is a human or an autonomous agent.

---
out_of_scope:
  - feature: "Actual Implementation/Coding"
    reason: "The skill is for defining requirements and boundaries; use 'Build Software' for the code phase."
  - feature: "Database Schema Design"
    reason: "Focus is on user-facing flows, not technical storage implementation."
---
