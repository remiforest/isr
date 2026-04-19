# Guide

## Purpose
Explain the ISR approach and tell LLMs exactly what to do when they encounter this folder.

## Instructions for LLMs

When you discover this `.isr/` folder:

1. Read `_index.md` — discover all concepts
2. Read `root.md` — understand project intent
3. Apply the appropriate protocol based on the situation:

| Situation | Protocol |
|---|---|
| `.isr/` is empty or `root.md` has no intent | `protocols/bootstrap.md` |
| About to write, modify, or delete code | `protocols/consult.md` |
| A decision changed the project's intent | `protocols/update.md` |
| Finishing a task, about to report done | `protocols/drift-check.md` |
| User's intent is unclear or ambiguous | `protocols/clarify.md` |

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
- directive — LLM behavior principles
- protocols/ — actionable procedures triggered by situation
- _index.md — the navigation file
