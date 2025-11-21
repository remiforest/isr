# 💡 ISR: Intentional Software Representation

**ISR (Intentional Software Representation)** is an AI-assisted architectural approach that establishes a clear, concise, and living representation of a software system's core intention, serving as the single source of truth for AI co-architecting.

## Why ISR?

Traditional software development using LLMs suffers from:
* **Context Loss:** AI forgets the overarching design between sessions.
* **Diluted Intent:** Code often reflects *what* is done, not *why* it was designed that way.
* **Architectural Drift:** Changes often violate initial principles without detection.

ISR solves this by providing the AI with a structured, durable semantic framework, enabling it to act as a **reasoned co-architect**.

---

## ⚙️ Core Components

This repository provides the core documents for implementing the ISR approach. Note that the **canonical language for the structured ISR content is English** for optimal LLM performance, although user dialogue can be multilingual.

| Document Name | Content Role | Audience |
| :--- | :--- | :--- |
| `ISR-vision.md` | **Conceptual Vision** | Human Designer |
| `ISR-template.md` | **Structured Format** (The Data Model) | LLM / Human |
| `ISR-directive-LLM.md` | **Continuous Management Rules** | LLM Engine |
| `ISR-bootstrapping.md` | **Reverse-Engineering Protocol** (Brownfield Start) | LLM Engine |

---

## 🚀 Getting Started: Two Workflows

The starting procedure depends on the status of your project.

### Scenario 1: Starting a New Project (Greenfield)
The process is **Design-Forward**: Intention drives Implementation.

1.  **Initial Definition:** Manually fill Sections 1 (Overview) and 2 (Glossary) of the `ISR-template.md` with your initial design intentions.
2.  **LLM Activation:** Feed the LLM the four core documents and the partially filled template.
3.  **Collaborative Design:** Instruct the LLM to assist in formalizing the rest of the ISR (Workflows, Invariants) **before** writing code (See **Prompt A** below).
4.  **Continuous Maintenance:** Use the LLM's verification capabilities (Code ↔ ISR checks) to ensure the implementation strictly follows the ISR.

### Scenario 2: Applying ISR to an Existing Project (Brownfield)
The process is **Reverse-Engineering**: Code reveals the Intention (which must be validated).

1.  **Provide Context:** Give the LLM access to the existing codebase, file structure, and any legacy documentation.
2.  **Launch Bootstrapping:** Initiate the LLM using the `ISR-bootstrapping.md` protocol (See **Prompt B** below).
3.  **Human Arbitration:** The LLM will follow a rigorous 4-phase extraction process. At critical junctures (Glossary, Invariants), the LLM will **pause and ask you for validation** to correct ambiguous or divergent code intentions.
4.  **Maintenance:** Once the ISR is filled and validated, the LLM switches to the standard **Continuous Maintenance** mode.

---

## 🗣️ Initial Prompts

Use these prompts to initialize the LLM for the respective scenario.

### Prompt A: Greenfield Initialization


**Instruction: Initialize ISR for New Project (Greenfield)**

"You have been provided with the full ISR documentation set: the Vision, Template, and Directives. Your current mode is Design-Forward. Your primary goal is to collaboratively populate the `ISR-Template.md` structure by working with the human designer.

Action: Acknowledge all ISR documents and request the user to provide the initial content for Section 1. Overview and Section 2. Glossary."


### Prompt B: Brownfield Initialization

**Instruction: Initialize ISR for Existing Project (Brownfield)**

"You have been provided with the full ISR documentation set, including the critical `ISR-bootstrapping.md` directive. Your current mode is Bootstrapping / Reverse-Engineering.

Action: Confirm you are ready to execute the `ISR-bootstrapping.md` protocol. Immediately request the user to provide access to the source code and any existing documentation needed to begin Phase 1: Semantic Extraction."
