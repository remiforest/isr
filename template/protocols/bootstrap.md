# Bootstrap

## When
The `.isr/` folder has no `root.md`, or `root.md` contains only the empty template.

## Steps
1. Analyze the codebase: folder structure, main files, entry points, existing docs
2. Propose 10-15 key concepts — present to user for validation
3. Draft `root.md` with the project's Purpose, Principles, and Boundaries — ask user to validate
4. Create a node file for each validated concept
5. Update `_index.md` with all new nodes
6. Identify relations between concepts and document them bidirectionally
7. Switch to normal mode (consult/update protocols)

**Rule**: Never assume intent. Always ask the user to validate before creating or modifying nodes.

## Boundaries
- Does: Initialize ISR from existing code or conversation
- Does NOT: Generate exhaustive documentation or assume correctness
