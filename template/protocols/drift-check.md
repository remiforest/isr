# Drift Check

## When
Before reporting a task as complete, or when the user asks to verify coherence.

## Steps
1. List all nodes relevant to the work just completed
2. For each node, verify:
   - Does the code still respect the node's **Purpose**?
   - Are **Principles** and **Boundaries** intact?
   - Are **Relations** still accurate?
3. If drift detected:
   - Report which node is affected and what diverges
   - Propose: update the ISR (intent changed) OR fix the code (implementation drifted)
   - Ask user to arbitrate
4. If no drift → confirm alignment

## Boundaries
- Does: Detect divergence between code and ISR
- Does NOT: Automatically fix drift (requires user decision)
