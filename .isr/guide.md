# Guide

## Purpose
Explain the ISR approach and tell LLMs exactly what to do when they encounter this folder.

## Instructions for LLMs

When you discover this `.isr/` folder, follow these steps:

### If `root.md` is empty or contains only a template:
This is a new or existing project that needs ISR initialization. Run the **bootstrapping process**:

1. Analyze the codebase structure (folders, main files, entry points)
2. Propose 10-15 key concepts you identify — ask user to validate
3. Create `root.md` with the project's Purpose and Principles — ask user to validate
4. Create a node for each validated concept
5. Update `_index.md` with all nodes
6. Identify and document relations between concepts
7. Switch to normal mode (see below)

**Important**: Never assume intent. Always ask the user to validate your understanding before creating nodes.

### If `root.md` describes the project's intent:
This project already has ISR. Use **normal mode**:

1. Read `_index.md` — discover all concepts
2. Read `root.md` — understand project intent
3. Before any action:
   - Load relevant nodes + their relations
   - Verify alignment with Purpose, Principles, Boundaries
   - If unclear → ask user BEFORE proceeding
   - If aligned → proceed
   - If misaligned → refuse and explain why
4. After any action that changes intent:
   - Update affected nodes
   - Update `_index.md` if needed
   - Maintain bidirectional relations

## What is ISR?

ISR (Intentional Software Representation) captures the **intention** behind a software system — the "why", not the "how". It serves as a persistent semantic framework that enables LLMs to act as reasoned co-architects across sessions.

## Core Idea

One concept = one file (a **node**). Nodes link to each other through **relations**, forming a flat graph of intentions. No hierarchy, no implementation details, no code references.

## Node Structure

Every node follows this template:

```markdown
# [Concept Name]

## Purpose
Why this exists — one sentence.

## Serves
Who or what benefits from this.

## Enables
What becomes possible because of this.

## Principles
Rules specific to this concept.

## Boundaries
- Does: [responsibilities]
- Does NOT: [anti-responsibilities]

## Relations
- other_concept — nature of the link
```

## Key Principles

- **Intention over implementation** — capture why, not how
- **One concept per file** — atomic, self-contained nodes
- **Flat structure** — no nested folders, all nodes at same level
- **Explicit relations** — links are declared, not implicit
- **Prevention over detection** — validate before acting
- **Proactive disambiguation** — clarify unclear goals, concepts, or intentions before starting work
- **User arbitration** — never make implicit decisions
- **English canonical content** — for LLM performance

## Boundaries
- Does: Explain ISR and instruct LLMs on what to do
- Does NOT: Define the project's intent (that's root's job)

## Relations
- root — the project's entry point after reading this guide
- node — defines the structure explained here
- directive — detailed LLM behavior rules
- bootstrapping — detailed bootstrapping process
- _index.md — the navigation file
