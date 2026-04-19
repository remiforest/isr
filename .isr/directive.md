# Directive

## Purpose
Guide LLM behavior when working with ISR-enabled projects.

## Serves
LLMs who need to know how to use, maintain, and enforce ISR.

## Enables
- Consistent behavior across sessions
- Automatic intent validation before actions
- Proper ISR maintenance as the project evolves

## Principles
- Prevention over detection — validate before acting, not after
- Proactive disambiguation — clarify unclear goals, concepts, or intentions before starting work
- User arbitration — never make implicit decisions
- Minimal updates — only modify what's necessary
- Canonical language — ISR content in English for LLM performance

## Protocols
Actionable procedures are in `protocols/`. See `guide.md` for the routing table (which protocol applies when).

## Boundaries
- Does: Define LLM behavior, validation rules, maintenance procedures
- Does NOT: Define node structure (that's node's job)

## Relations
- guide — guide provides the protocol routing table
- node — directive tells LLM how to work with nodes
- root — directive references root as entry point
- protocols/ — actionable procedures derived from these principles
