# Index

## Purpose
Provide a single entry point mapping all concepts to their files.

## Serves
LLMs starting a session who need to discover the project's structure.

## Enables
- Instant overview of all concepts
- Navigation without guessing file names
- Detection of orphan or missing concepts

## Principles
- Single source of truth for concept-to-file mapping
- Updated whenever a node is added or removed
- No duplication of node content — just references

## Structure
```markdown
# ISR Index — [Project Name]

| Concept | Type | File |
|---------|------|------|
| concept_a | concept | concept_a.md |
| rule_x | invariant | rule_x.md |
| checkout | workflow | checkout.md |
| chose_postgres | decision | chose_postgres.md |
```

Types: `concept` (default), `invariant`, `workflow`, `decision`, `protocol`

## Boundaries
- Does: Map concepts to files
- Does NOT: Describe concepts, store relations, contain intent

## Relations
- node — each entry points to a node file
- guide — first file to read after index for understanding ISR
- root — the project's entry point after understanding ISR
