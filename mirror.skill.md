---
summary: "Protocol for stereoscopic memory where intent serves as dialogue and path-values serve as state."
version: "1.1.0"
author: "heysoup"
last_updated: "2026-04-25"
---

# The Mirror Protocol: No Speech without State

The **Mirror Protocol** is the operational standard for agents within the Soup ecosystem. It ensures high-integrity coordination by transforming the `intent` field into a **Factual Dialogue** layer and the `path-value` tree into a **Factual State** layer.

## 1. Core Mandates

### A. The Identity Principle
**Every conversational turn must be a state mutation.**
Agents do not "chat" in the traditional sense. Every piece of communication intended for other agents or humans must be encapsulated in the `intent` field of a `/_write`, `/_delete`, or `/_vault` call.

### B. The State Principle
**No Speech without State.**
An agent must never express a decision in the `intent` field without reflecting that decision in the `path-value` tree. 
- *Bad:* `intent: "I am cancelling the project"` (but the project path still exists).
- *Good:* `intent: "I am cancelling the project"`, `action: DELETE`, `path: /projects/phoenix`.

### C. The Continuity Principle
**Priority of Global Inertia.**
When an agent enters a workspace (especially after a session reset), it must reconstruct the "Shared Reality" by reading:
1. **The Pulse:** The current `mutation_id`.
2. **The Global Inertia:** The recent sequence of `intent` strings (The Dialogue).
3. **The Reality Ledger:** The current absolute values of all paths (The Situation).

## 2. Using the Intent Field as Dialogue

The `intent` field is your voice. It should contain:
1. **The Logic:** Why are you making this change?
2. **The Factual Communication:** Any message you would normally send in a chat (e.g., "Bob, I've updated the API keys as requested").
3. **The Context:** Briefly mention the Pulse or prior mutation you are responding to if relevant.

## 3. Cognitive Benefits: Stereoscopic Memory

By strictly adhering to the Mirror Protocol, the workspace achieves **Stereoscopic Memory**:

| Layer | Component | Function |
| :--- | :--- | :--- |
| **Narrative** | `intent` | The "Dialogue" — Who said what and why. |
| **Physical** | `path-value` | The "State" — The absolute current situation. |

This makes agents **Stateless and Swappable**. A fresh agent session can read the last 5-10 intents and the current state to gain 100% situational awareness without needing thousands of tokens of chat history.
