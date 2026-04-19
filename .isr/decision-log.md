# Decision Log

## Purpose
Track significant decisions that shaped the ISR approach itself.

## Serves
Future sessions that need to understand why ISR is designed this way.

## Enables
- Avoiding re-discussion of settled decisions
- Understanding the rationale behind current structure
- Evolving ISR with awareness of past choices

## Principles
- Append-only — decisions are added, not modified
- Rationale required — every decision explains "why"
- Linked to discussion — reference conversation context when possible

## Log

| Date | Decision | Rationale |
|------|----------|-----------|
| 2024-12-05 | Generic types over DDD-specific | ISR must apply to any project, not just domain-driven ones |
| 2024-12-05 | Graph over tree | Concepts have cross-links, hierarchy is too rigid |
| 2024-12-05 | Flat file structure | Simpler navigation, no nested folders to manage |
| 2024-12-05 | Relations in nodes, not central | Keeps related info together, easier maintenance |
| 2024-12-05 | Free-form relation descriptions | LLMs understand natural language, no need for controlled vocabulary |
| 2024-12-05 | One file per node | Isolated updates, granular loading |
| 2024-12-05 | Index as simple mapping | Just discovery, no duplication of content |
| 2024-12-05 | Prevention over detection | LLM validates before acting, not audits after |
| 2024-12-05 | Intent over implementation | ISR is not a spec or documentation, it's a reasoning framework |
| 2026-04-19 | Decompose directive into protocols | Monolithic directive mixed all LLM behaviors; protocols allow targeted loading, independent evolution, and clear triggers. Protocols live in protocols/ subdirectory to distinguish them from concept nodes |
| 2026-04-19 | Schema flexibility — common core + type-specific sections | Uniform schema forced invariants, workflows, and decisions into ill-fitting shapes. Common core (Purpose, Boundaries, Relations) keeps consistency; type-specific sections (Statement, Trigger, Context...) give each type its natural form. Index gains a Type column for triage before loading |

## Boundaries
- Does: Record decisions about ISR design
- Does NOT: Track project-specific decisions (those go in project's own decision-log)

## Relations
- root — decisions shaped the principles in root
- node — decisions defined node structure
