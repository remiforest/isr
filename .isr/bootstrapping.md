# Bootstrapping

## Purpose
Initialize ISR for an existing codebase by extracting intent from code.

## Serves
Developers applying ISR to brownfield projects.

## Enables
- Retrofitting ISR without starting from scratch
- Discovering implicit intent in existing code
- Gradual formalization of design decisions

## Principles
- Deduction, not description — extract the "why", not the "what"
- Human validation required — never assume intent without confirmation
- Incremental — start with core concepts, expand progressively
- Imperfect is OK — bootstrapped ISR will need refinement

## Process
See `protocols/bootstrap.md` for the step-by-step procedure.

## Boundaries
- Does: Extract intent, propose structure, ask for validation
- Does NOT: Generate exhaustive documentation, assume correctness

## Relations
- directive — bootstrapping leads into normal directive mode
- node — bootstrapping creates initial nodes
- index — bootstrapping generates initial index
