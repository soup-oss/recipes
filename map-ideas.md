---
author: "heysoup.co (deterministic infrastructure for the agentic era)"
summary: "A framework for exploring and documenting relationships between concepts and themes."
description: "Invoke this skill when brainstormming, analyzing complex systems, or finding hidden connections between different categories of information."
version: "1.0.0"
---

# Skill: Map Ideas

## 1. The Core Philosophy
Innovation happens at the intersection of ideas. This skill focuses on the "In-Between"—not just what the ideas are, but how they connect, conflict, or complement each other.

## 2. Pre-flight Check (Prerequisites)
The agent must have a baseline of "Raw Ideas" or concepts to work with. If none exist, the agent must perform an initial brainstorm with the user.

## 3. The Analysis Scaffold (Output Structure)
The agent will create:
1.  **`ideas/[concept-name]`**: The raw building blocks of the map.
2.  **`connections/[relation-name]`**: Explicit descriptions of how two or more ideas relate.
3.  **`themes/[category]`**: Clusters of related ideas grouped by a common thread.
4.  **`synthesis/summary`**: The high-level "So What?" of the entire map.

## 4. The Execution Workflow
### Phase A: Exploration
Identify and document the base `ideas/`.
### Phase B: Connection
Create `connections/` files. Focus on the nature of the relationship (e.g., "X enables Y", "A contradicts B").
### Phase C: Grouping
Cluster ideas into `themes/`. A single idea can belong to multiple themes.
### Phase D: Synthesis
Analyze the map and write a `synthesis/` that summarizes the landscape and identifies gaps or opportunities.

## 5. Operational Guidelines
*   **Explicit Relations**: A connection without an explanation in a `connections/` file is just a line; the value is in the narrative.
*   **Thematic Overlap**: Encourage ideas to exist in multiple themes to reveal non-obvious intersections.
*   **Gap Analysis**: Always look for "unconnected ideas" and suggest potential links.

---
out_of_scope:
  - feature: "Project Planning/Gantt Charts"
    reason: "The skill is for conceptual exploration, not execution scheduling."
  - feature: "Data Visualization"
    reason: "Requires external tools; the agent provides the narrative connections only."
---
