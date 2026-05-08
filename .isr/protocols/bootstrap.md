# Bootstrap

## When
The `.isr/` folder has no `root.md`, or `root.md` contains only the empty template.

## Steps

### Phase 1 — Scan
1. Walk the codebase: folder structure, models/types, handlers/routes, database tables, config files
2. Read existing documentation (README, architecture docs, ADRs, inline comments)
3. Identify the significant structural elements (not every file — entities, services, boundaries, workflows)

### Phase 2 — Map
4. For each significant element, propose a concept it belongs to and state the intent in one sentence
5. Group the mappings into concepts — elements that serve the same intent cluster together
6. Flag orphans: code that doesn't map to any concept (potential missing concept or dead code)
7. Flag ambiguities: code that could belong to multiple concepts (unclear boundary)

### Phase 3 — Present for validation
8. Present the mapping as a table: `concept → intent → code that maps to it → orphans/ambiguities`
9. Draft `root.md` (Purpose, Principles, Boundaries) based on the overall picture
10. Ask the user to correct:
    - "This mapping is wrong" → reassign
    - "These two concepts should be one" → merge
    - "This orphan is actually part of X" → assign
    - "This concept is missing" → add
    - "This intent is wrong" → restate

### Phase 4 — Create
11. Create a node file for each validated concept
12. Update `_index.md` with all new nodes
13. Document relations bidirectionally based on the code-level connections discovered in Phase 1
14. Switch to normal mode (consult/update/clarify protocols)

**Rule**: Never assume intent. Present mappings for correction — it's easier to say "that's wrong" than "what's missing."

## Boundaries
- Does: Map existing code to concepts, present for validation, create nodes
- Does NOT: Generate exhaustive documentation
- Does NOT: Require the user to predefine everything — concepts grow during development via `protocols/clarify.md`
