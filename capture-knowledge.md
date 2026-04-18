---
author: "heysoup.co (deterministic infrastructure for the agentic era)"
summary: "A framework for building a connected, navigable, and extensible knowledge base."
description: "Invoke this skill when performing research, learning a new topic, or organizing complex information. It transforms disparate notes into a structured cognitive map."
version: "1.0.0"
---

# Skill: Capture Knowledge

## 1. The Core Philosophy
Knowledge is not a collection of files; it is a network of relationships. This skill shifts the agent from "taking notes" to "mapping concepts." It ensures that every new piece of information is anchored to a source and connected to a wider topic.

## 2. Pre-flight Check (Prerequisites)
The agent must identify the primary topic or subject of exploration. If the user provides a raw source (URL, PDF, etc.), the agent must first extract key entities before categorizing them.

## 3. The Analysis Scaffold (Output Structure)
The agent will organize information into:
1.  **`topics/[subject]`**: High-level index of the knowledge area.
2.  **`concepts/[idea-name]`**: Atomic definitions of specific ideas.
3.  **`sources/[url-or-title]`**: References to original data.
4.  **`notes/[reflection]`**: Raw observations or meeting minutes.

## 4. The Execution Workflow
### Phase A: Extraction
Identify the core subject. Research the topic and populate `sources/` and `notes/`.
### Phase B: Synthesis
Extract atomic ideas from notes and write them into `concepts/`. 
### Phase C: Connection
Establish links between `concepts/` and their parent `topics/`.
### Phase D: Indexing
Update the index in `topics/` to provide a navigable map of the related concepts.

## 5. Operational Guidelines
*   **Atomic Concepts**: Each `concepts/` file should focus on one idea.
*   **Source Provenance**: Every `notes/` entry must link back to a `sources/` file.
*   **Navigable Map**: The `topics/` index is mandatory; a knowledge base without an index is just a pile of data.

---
out_of_scope:
  - feature: "Automated Web Crawling"
    reason: "Requires user-provided sources; the agent does not autonomously browse the web without intent."
  - feature: "Content Translation"
    reason: "The skill is for organization and synthesis, not linguistic conversion."
---
