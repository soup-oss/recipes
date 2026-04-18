# SOUP Recipes

**A collection of behavioral blueprints and skills for agents.**

These are **just recipes**. They are not part of the SOUP protocol or infrastructure; they are standardized behavioral templates that agents can "install" to achieve specific outcomes.

---

## 🥣 How to use
A Recipe is typically a `skill.md` file that an agent reads to adopt a specific coordination pattern. 

### Metadata Standards
Each recipe includes a front-matter block with:
- **`author`**: The creator of the skill.
- **`summary`**: A high-level overview for humans.
- **`description`**: The critical "Semantic Trigger" for the agent. It defines **when** and **how** the agent should invoke this specific skill.
- **`out_of_scope`**: The "Safety Barrier." Explicitly defines what the agent should **not** do, preventing scope creep and hallucinations.
- **`version`**: The current iteration of the logic.

- **Decoupled:** The soup engine doesn't care *how* you coordinate, but these recipes ensure you do it well.
- **Functional:** From "Graph Integrity" to "Project Management," these are the blueprints for the agentic era.
- **Community Driven:** Standardized ways of working that anyone can contribute to.

---

## 🚀 Status
This is a placeholder for the upcoming community library of `skill.md` blueprints. Later, these recipes will live as the manifest of each SOUP workspace.

## 🚀 How to Install a Skill

There are multiple ways to "install" a recipe into an agent's brain. Each has pros and cons depending on your workflow.

### 1. **Session Loading (Manual Copy-Paste)**
Open a `skill.md` file, copy its entire content, and paste it into your agent's chat window (ChatGPT, Claude, etc.).
- **Instructions:** "Adopt this skill and wait for my next command."
- **Pros:** Instant, works with any LLM, zero setup required.
- **Cons:** Volatile (lost when the session ends), consumes context window, manual effort.

### 2. **Context Discovery (Workspace Ingestion)**
Place the `skill.md` file into your agent's shared workspace or project directory.
- **Instructions:** "Search for available skills in this workspace and adopt the relevant ones for this task."
- **Pros:** **Persistent & Shared.** All agents working in the same environment automatically adopt the same protocols. No manual copy-pasting required for new sessions.
- **Cons:** Requires an agent capable of reading local or remote files.

### 3. **Permanent Knowledge (Custom GPTs / System Instructions)**
Upload the `skill.md` to your agent's "Knowledge" files or paste it directly into its System Instructions.
- **Pros:** The agent *is* the skill. Low overhead per session, permanently available.
- **Cons:** Harder to version-control or update across multiple agents. Locked to a specific platform.

---

**Follow the recipe. Reach the Purpose.**

---

Maintained by [heysoup.co](https://heysoup.co) — Secure shared context for the agentic era.
