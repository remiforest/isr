# ISR – Intentional Software Representation  
## Vision Document

### 1. Definition

**ISR (Intentional Software Representation)** is an AI-assisted design approach aimed at maintaining a clear, concise, and living representation of a software system's intention, independent of its technical implementation.

This representation serves as a **central reference** between the human designer and the AI, and captures:
- what the system must do (functional and business logic),
- **the principles by which it is built (Architectural Intentions),**
- how it must be structured (architecture),
- why certain decisions are made (intention and constraints),
- the principles according to which it must evolve (invariants, limits, and coherence).

---

### 2. Problem Statement

In development with AI:
- The AI loses context between sessions and must reinterpret the code.
- Design intent is not preserved or becomes diluted over time.
- Code represents what is done, not why or how it should evolve.
- Human documentation is often verbose, imprecise, and quickly outdated.

**ISR provides a structured response to these limitations.**

---

### 3. Objectives of the Approach

ISR aims to:
1. **Preserve design intent throughout the project.**
2. **Provide the AI with a sustainable semantic framework,** allowing it to act without having to re-scan the code.
3. **Facilitate architectural understanding** without exhaustive analysis.
4. **Ensure alignment between intention and implementation** (code conforms to design).
5. **Allow the natural evolution of the system,** taking into account the decisions made.
6. **Make the human designer the arbiter of ambiguities or structural choices.**

---

### 4. Fundamental Principles

- **Intentional Orientation**: Priority to meaning, business logic, and architecture, rather than technical details.
- **Concise, structured, non-redundant representation**, understandable by both AI and human.
- **Controlled terminology** via a central glossary.
- **Dynamic updating** with every decision impacting the intention or architecture.
- **Bidirectional verifications**:
  - *Code → ISR*: Does the code respect the intention?
  - *ISR → Code*: Is the intention correctly implemented?
- **User arbitration** in case of ambiguity or multiple interpretations.

---

### 5. What ISR is Not

ISR **is not**:
- narrative technical or functional documentation,
- a duplicate of the code or its exact behavior,
- a rigid modeling system (UML/MDE type),
- automatic code generation without reasoning,
- a reconstruction based solely on existing code.

ISR is **a living representation**, aligned with the design intent.

---

### 6. Expected Benefits

| Benefit | Impact |
|----------|--------|
| Conceptual Stability | The system evolves without loss of meaning |
| Architectural Coherence | AI proposals remain aligned |
| Improved Dialogue | Less file exploration or clarification iterations |
| Controlled Refactoring | Intent guides changes |
| Simplified Handover | ISR allows quick onboarding for a human or an AI |
| Technological Adaptability | Possibility to re-implement in another language without losing the model |
| **Living Conformity Report** | **Alignment between code and design is continuously checked and displayed.** |

---

### 7. Concrete Uses

ISR allows:
- quickly explaining the architecture or behavior to the AI or a human;
- generating code while ensuring consistency;
- detecting semantic inconsistencies (e.g., misplaced responsibility);
- propagating a technical or functional decision throughout the system;
- limiting code scanning and avoiding design drifts.

---

### 8. Synthesis

> **ISR transforms the AI into a reasoned co-architect**, responsible for preserving and leveraging the design intent throughout the project lifecycle.

ISR allows:
- *capturing the designer's intent*,
- *using this intent as a permanent framework for reasoning*,
- *and guiding code evolution without loss of meaning*.

It is an AI-assisted project structuring method, where design is considered the source of truth before implementation.

---

### 9. Document Status

This document describes the vision of the ISR approach.
It does not yet define the structured representation format or the application guidelines (see `ISR-directive-LLM.md` and `ISR-template.md` for that).
It serves as a conceptual basis and general introduction to the method.