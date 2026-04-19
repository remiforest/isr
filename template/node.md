# Node

## Purpose
The atomic unit of intention representation — one concept, one file.

## Serves
Both humans and LLMs who need to understand a specific concept.

## Enables
- Granular navigation through the project's intent
- Isolated updates without affecting unrelated concepts
- Loading only relevant context for a given task

## Principles
- Self-contained — a node has all info needed to understand the concept
- Uniform structure — every node follows the same template
- Explicit relations — links to other nodes are declared, not implicit
- Flat storage — all nodes at same directory level (no nested folders)

## Structure

### Common core (all nodes)
```markdown
# [Name]

## Purpose
Why this exists — one sentence.

## Boundaries
- Does: [responsibilities]
- Does NOT: [anti-responsibilities]

## Relations
- other_concept — nature of the link
```

### Common optional (most nodes)
```markdown
## Serves
Who or what benefits from this.

## Enables
What becomes possible because of this.

## Principles
Rules specific to this concept.
```

### Type-specific sections

**Invariant** — a rule that must always hold:
```markdown
## Statement
The rule in plain language.

## Applies to
Which concepts this rule constrains.

## Verified by
How this is checked (test reference, or "semantic").
```

**Workflow** — a sequence of actions:
```markdown
## Trigger
What initiates this workflow.

## Steps
Ordered sequence of actions.

## Involves
Which concepts participate.
```

**Decision** — an architectural choice:
```markdown
## Context
What prompted this decision.

## Decision
What was decided.

## Consequences
What follows from this choice.

## Status
Active | Superseded by [ref]
```

## Boundaries
- Does: Represent one concept's intention completely
- Does NOT: Contain implementation details, code references, or specs

## Relations
- index — registers this node for discovery
- relation — links this node to others
