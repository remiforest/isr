# ISR: Intentional Software Representation

ISR captures the **intention** behind a software system — the "why", not the "how". It enables LLMs to act as reasoned co-architects across sessions.

## The Problem

- LLMs lose context between sessions
- Design intent gets diluted over time
- Code shows *what* is done, not *why*
- Architectural drift goes undetected

## The Solution

A `.isr/` folder containing a **graph of intention nodes**:
- One concept = one file
- Flat structure, no hierarchy
- Explicit relations between concepts
- LLM validates actions against intent before executing

## Repository Structure

```
isr/
├── README.md           # This file
├── AGENTS.md           # Entry point for any coding agent
├── CONTRIBUTING.md     # How to contribute
├── template/           # Files to copy into your project
│   ├── _index.md       # Navigation (customize)
│   ├── root.md         # Project intent (customize)
│   ├── guide.md        # ISR approach + protocol routing
│   ├── node.md         # Node definition
│   ├── index.md        # Index definition
│   ├── relation.md     # Relation definition
│   ├── directive.md    # LLM behavior principles
│   ├── bootstrapping.md # Bootstrapping concept
│   └── protocols/      # Actionable LLM procedures
│       ├── consult.md
│       ├── update.md
│       ├── bootstrap.md
│       ├── drift-check.md
│       └── clarify.md
└── .isr/               # ISR of this project (meta example)
```

## Quick Start

### For Humans

1. Copy the `template/` folder into your project as `.isr/`
2. Edit `root.md` with your project's intent
3. Update `_index.md` with your project name
4. Start a session with your LLM

### For LLMs

To implement ISR on a project, read the `.isr/` files in this order:
1. `_index.md` — discover all concepts
2. `guide.md` — understand the approach
3. `directive.md` — learn the behavior rules
4. `bootstrapping.md` — if applying to an existing codebase

Then follow the directive to build the project's ISR.

## Node Template

Every node follows this structure:

```markdown
# [Concept Name]

## Purpose
Why this exists — one sentence.

## Serves
Who or what benefits.

## Enables
What becomes possible.

## Principles
Rules for this concept.

## Boundaries
- Does: [responsibilities]
- Does NOT: [anti-responsibilities]

## Relations
- other_concept — nature of the link
```

## Key Principles

- **Intention over implementation** — capture why, not how
- **One concept per file** — atomic, self-contained
- **Flat graph** — no hierarchy, concepts link freely
- **Concise and non-redundant** — no narrative documentation
- **Living document** — evolves with the project
- **Prevention over detection** — validate before acting
- **User arbitration** — never make implicit decisions
- **English canonical content** — for optimal LLM performance

## LLM Workflow Summary

```
1. Start of session:
   - Read _index.md → know all concepts
   - Read guide.md → understand ISR approach + protocol routing
   - Read root.md → understand project intent

2. Match the situation to a protocol:
   - Empty ISR?          → protocols/bootstrap.md
   - About to code?      → protocols/consult.md
   - Intent changed?     → protocols/update.md
   - Task finishing?     → protocols/drift-check.md
   - Ambiguous intent?   → protocols/clarify.md

3. Follow the protocol steps
```

## Meta Note

This repository uses ISR to describe itself. The `.isr/` folder contains the ISR representation of the ISR project — a recursive example. The `template/` folder is what you copy to start fresh on your own project.

## License

MIT
