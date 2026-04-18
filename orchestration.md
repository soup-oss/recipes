---
author: "heysoup.co (deterministic infrastructure for the agentic era)"
summary: "A system for managing multi-agent teams, task distribution, and event-based reactions."
description: "Invoke this skill when coordinating multiple agents, managing a project queue, or setting up autonomous workflows. It defines roles, tasks, and triggers for team alignment."
version: "1.0.0"
---

# Skill: Orchestration

## 1. The Core Philosophy
In a multi-agent ecosystem, coordination is the primary bottleneck. This skill transforms a group of agents into a "Unified Team" by providing a shared state for mandates, tasks, and reactive logic.

## 2. Pre-flight Check (Prerequisites)
The agent must define the team composition. Who are the agents? What are their roles? What is the overarching project they are working on?

## 3. The Analysis Scaffold (Output Structure)
The agent will maintain:
1.  **`team/[agent-name]`**: Mandates, roles, and regex-based area of responsibility for each agent.
2.  **`tasks/pending`**: The prioritized queue of upcoming work.
3.  **`tasks/done`**: The audit log of completed items.
4.  **`triggers/[event-reaction]`**: Logical rules defining how the team reacts to specific changes (e.g., "When a spec changes, notify the developer agent").

## 4. The Execution Workflow
### Phase A: Definition
Define the agents needed. Create `team/` profiles with clear mandates.
### Phase B: Setup
Define the "Rules of Engagement" in `triggers/`. How do agents talk to each other?
### Phase C: Assignment
Populate `tasks/pending` with work items. Assign them to specific agents based on their mandates.
### Phase D: Coordination
Monitor the `_chat` and `_journal`. Move completed items from `pending` to `done`.

## 5. Operational Guidelines
*   **Clear Mandates**: Every agent in `team/` must have a unique regex or role to prevent overlap and conflict.
*   **Reactive Logic**: Triggers should be simple and deterministic (If X then Y).
*   **Task Transparency**: No agent should work on something that isn't in the `tasks/` directory.

---
out_of_scope:
  - feature: "Human Resource Management"
    reason: "Focus is on agent mandates and task queues, not human payroll or HR."
  - feature: "Low-level Scheduling"
    reason: "Managed via the task queue, not minute-by-minute calendaring."
---
