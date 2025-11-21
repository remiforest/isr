# ISR – Intentional Software Representation  
## LLM Directive

### 1. Purpose
You must implement and maintain a conceptual representation of the application called **ISR (Intentional Software Representation)**.
ISR describes the system's intention, structure, rules, and decisions, independent of the code. It serves as a semantic reference to guide implementation, facilitate explanation, and maintain overall consistency.

ISR must:
- reflect the design intention rather than implementation details;
- be structured, concise, and non-redundant;
- be updated with every significant decision or evolution;
- serve as a support for verification between design and code.

---

### 2. Principles
- Intentional orientation: priority to business logic, architecture, and the "why".
- Concise and structured style (telegraphic), no narrative documentation.
- No element should be present in multiple locations.
- Every concept must have a canonical name defined in the glossary.
- No new concept must be introduced without explicit definition.

---

### 3. Glossary
- Maintain a glossary with all structuring concepts: modules, business entities, workflows, invariants, decisions.
- **Extended Semantic Types:** Use precise types (e.g., Entity, Aggregate, Service, Command, Event) to reflect the architecture's semantics (e.g., DDD).
- Format: canonical name, type, short definition, key attributes.
- If a new term appears or seems implicit → ask user for arbitration before integration.

---

### 4. Modularity
- Organize ISR into hierarchical sections (global view, modules, workflows, invariants, decisions, etc.).
- Each section must remain concise enough to be integrated into a prompt.
- Navigation possible by detail levels, without loss of coherence.

---

### 5. Dynamic Updating
- Propose updating the ISR with every structural decision or decision impacting behavior.
- **Precise Triggers:** An update is required if the decision affects the **Glossary**, **Modularity**, **Invariants**, or introduces a new **Workflow**.
- After any modification, check for coherence and absence of contradiction.

---

### 6. Intention ↔ Implementation Traceability
- Associate each significant element of the ISR (module, workflow, invariant, decision) with one or more code areas (file, class, function, or tests).
- **Standardized Traceability Format:** Use the notation `[path/file#Function/Class.method()]` to link intention to code.
- **Invariant Traceability:** Explicitly link each **Invariant** to its corresponding **Unit Test or Regression Test** reference.
- In case of divergence:
  - propose updating ISR or modifying the code;
  - or ask user for arbitration.

---

### 7. Bidirectional Verifications

#### 7.1 Code → ISR
- Compare the code to the corresponding element in the ISR.
- **Targeted Verifications:** Prioritize analyzing warning signs in the code: use of **non-canonical terms** (outside Glossary), **unexpected dependencies** (not authorized by Modularity), or **Invariant break**.
- Expected result:
  - Conforming
  - Partially Conforming (specify)
  - Divergent (specify)
- **Conformity Status:** Maintain the result of this verification in the `Conformity Status` field of the template.
- If non-conforming → propose action or ask for user decision.

#### 7.2 ISR → User
- After modifying the ISR:
  - briefly reformulate the modified/created element;
  - ask 1–2 closed questions for clarification;
  - integrate adjustments immediately.

Verifications are local and targeted, not global.

---

### 8. Ambiguity Management
- You must never make implicit decisions.
- In case of multiple or uncertain interpretations:
  - present the plausible options;
  - **Quantify Uncertainty:** If possible, associate a probability (e.g., 70%, 30%) with each option to guide the user.
  - ask user for arbitration before action.

---

### 9. Restrictions
- No verbose or narrative documentation.
- No free reformulation of concepts.
- No duplication of information.
- No global analysis without explicit request.

---

### 10. Activation

> Apply the ISR approach described in this document.
> Create or adapt the project's intermediate representation.
> Use the ISR as a design reference.
> Update it with every relevant evolution.
> In case of ambiguity or divergence, query the user before any interpretation.
> Use ISR to guide, verify, and correct the implementation.

---

### 11. Language Policy

- **Canonical Language:** The **entire ISR representation (Template sections, Glossaries, Modules, Invariants)** must be maintained **exclusively in English**. This ensures maximum performance, precision, and consistency of the LLM's reasoning engine.
- **User Dialogue:** You must respond and engage with the human designer in the language they use (e.g., French, Spanish, etc.).
- **Translation Rule:** When an update is proposed by the user in a non-English language, you must:
    1.  **Translate** the new concept or structural change into clear, unambiguous English.
    2.  **Integrate** the English translation into the ISR structure.
    3.  **Confirm** the change and the English terminology with the user in their native language before finalizing.