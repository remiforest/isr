# Clarify

## When
- The user's intent is ambiguous, or multiple valid interpretations exist
- A concept is encountered during development that has no ISR node
- Boundaries between existing concepts are unclear

## Steps
1. Identify what is unclear:
   - **Ambiguous intent** → present 2-3 interpretations with consequences
   - **Missing concept** → propose a node name, purpose, and boundaries
   - **Unclear boundary** → show the overlap, propose a split
2. Ask the user to choose or correct
3. Record the clarification:
   - Update the relevant ISR node (Purpose, Principles, or Boundaries)
   - Or create a new node if a concept was missing → update `_index.md`
4. If the clarification affects other nodes → update their Relations

## Boundaries
- Does: Resolve ambiguity through user dialogue and record the result
- Does NOT: Make assumptions or choose for the user
- Does NOT: Block work indefinitely — if the gap is minor, note it and proceed
