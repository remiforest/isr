# ISR – Intentional Software Representation
## Bootstrapping Directive (Existing Projects)

### 1. Phase Objective

This directive's sole purpose is to **initially populate** the `ISR-template.md` using existing code and documentation.

You must never make structural or semantic assumptions without human validation during this phase. The goal is to **deduce the intention** and not to describe the exact behavior of the code.

---

### 2. Priority and Execution Order

You must execute the intention extraction phase by following this strict order. Each phase depends on human validation of the preceding one.

1.  **Phase 1: Semantic Extraction (The "What")**
2.  **Phase 2: Structural Extraction (The "How")**
3.  **Phase 3: Behavioral Extraction (The "When")**
4.  **Phase 4: Formalization and Closing (The "Why")**

---

### 3. Phase 1: Semantic Extraction (Glossary) 🛠️

The objective is to populate the **Glossary (Section 2)**.

#### 3.1 Procedure

* **Priority Scan:** Start by analyzing the names of **main folders**, **classes/structs/interfaces**, and **database tables**.
* **Canonical Identification:** Propose a **list of approximately 50 canonical names** representing the most important business concepts (`Entity`, `Aggregate`, `Module`, `Service`).
* **Type Deduction:** Assign an extended semantic type to each name (e.g., a `users` table is likely an `Entity`).

#### 3.2 Validation Loop 🎯

1.  **Summary:** Present the user with a summary table of the **10 most critical concepts** extracted.
2.  **Closed Question:** Ask the user: *"Does the extracted glossary cover the fundamental business concepts? [Yes/No] If No, please add the missing terms."*
3.  **Action:** Integrate corrections and finalize the initial population of **Section 2. Glossary**.

---

### 4. Phase 2: Structural Extraction (Modularity & Invariants) 🏗️

The objective is to populate **Modules (Section 4)** and **Invariants (Section 3)**.

#### 4.1 Module Extraction

* **Boundary Deduction:** Analyze folder organization and naming prefixes to identify the boundaries of **Modules (Section 4)**.
* **Dependencies:** For each deduced Module, analyze `import` or `use` statements to identify and list **Authorized Dependencies**. Any *non-implicit* dependency (e.g., one business module depending on another business module) must be traced.
* **Role & Responsibilities:** Fill in the **Role** and **Main Responsibilities** using the terms from the **validated Glossary** in Phase 1.

#### 4.2 Invariant Extraction

* **Targeted Scan:** Analyze **unit tests (fixtures)**, **validation functions (assertions/guard clauses)**, and **database constraints (UNIQUE, CHECK)**.
* **Deduction:** Convert the found validation logic into a **declarative, non-technical business rule** (e.g., `if (amount > 0)` becomes `The amount of an Order must always be positive`).
* **Traceability:** Immediately fill in the **Verification (Test Code Ref)** column of the **Invariants (Section 3)**.

#### 4.3 Validation Loop 🎯

1.  **Summary:** Present the list of deduced modules with their **Authorized Dependencies** and the list of the **10 most critical invariants**.
2.  **Closed Question:** Ask the user: *"Are the modular structure and invariants deduced from the current code consistent with the intention that the system must respect? [Yes/No] If No, please correct the Module boundaries or the Invariants."*
3.  **Action:** Finalize **Sections 3 and 4**.

---

### 5. Phase 3: Behavioral Extraction (Workflows) ⏳

The objective is to populate **Workflows (Section 5)**.

#### 5.1 Procedure

* **Priority Scan:** Analyze entry points (e.g., API Controllers, CLI Commands, Event Handlers) and follow the sequence of function calls (the "call graph").
* **Workflow Deduction:** For each entry point, create a **Workflow** representing the sequence of business operations. The **Main Steps** must mention the **Modules** and **Entities** from the Glossary.
* **Associated Invariants:** Link the Workflow to the **Invariants** extracted in Phase 2 that it is supposed to guarantee or validate.

#### 5.2 Validation Loop 🎯

1.  **Summary:** Present a textual diagram of the **5 most complex** (or longest) workflows in the system.
2.  **Closed Question:** Ask the user: *"Does the flow of the extracted workflows represent the business logic as it should be understood by new team members and by the AI? [Yes/No] If No, please correct the Workflow steps."*
3.  **Action:** Finalize **Section 5**.

---

### 6. Phase 4: Formalization and Closing (ADR & Traceability) 📜

The objective is to populate the final sections.

#### 6.1 Decision Deduction (ADR)

* **Targeted Scan:** Analyze existing documentation (README, CONFLUENCE, JIRA, existing ADRs if any) and architectural comments in the code.
* **Deduction:** If a decision with a clear impact is found (e.g., "Choice of Kafka for messaging"), formalize it in **Section 6. Architectural Decisions (ADR)** with the status `Inferred`.
* **Status:** All deduced ADRs must have the initial status `Pending Validation`.

#### 6.2 Finalizing Traceability

* **Initial Verification:** Execute the first **Code → ISR** verification (LLM Directive, 7.1) for all sections 2 to 6.
* **Population:** Fill in **Section 7. Intention ↔ Code Traceability**. For this bootstrapping phase, the conformity status should initially be `Partially Conforming (Bootstrapping)` to reflect that alignment needs consolidation.

#### 6.3 Closing

* **Instruction:** Once Phase 4 is complete, you switch to **Maintenance Management** mode and follow the **LLM Directive** for all future interactions.