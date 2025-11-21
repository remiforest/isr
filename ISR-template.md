# ISR – Intentional Software Representation
## [Project Name]

---

## 1. Overview
- Purpose:
- Functional Scope:
- **Design Principles (Architectural Intentions):** *(E.g., DDD, Hexagonal, Simplicity)*
- **Global Constraints (Limitations):** *(E.g., Performance, Security, Interoperability)*

---

## 2. Glossary
| Canonical Name | Type (Module, Entity, Workflow, Invariant, Decision, **Command, Event, Service**...) | Definition | **Key Attributes/State (for Entities)** | Forbidden Synonyms (optional) |
|---------------|-------------------------------------------------------------------------------------|------------|----------------------------------------|------------------------------|
|               |                                                                                     |            |                                        |                              |

---

## 3. Invariants / Business Rules (Elevated)
| Brief Description | Related to (Workflow/Module) | Verification (Test Code Ref) |
|-------------------|------------------------------|------------------------------|

---

## 4. Modules
### [Module Name]
- Role:
- Main Responsibilities:
- What it must *not* do:
- Authorized Dependencies:
- Interfaces / Entry Points:
- Code Traceability: (format `[path/file#Function/Class.method()]`)

*(Duplicate for other modules)*

---

## 5. Workflows / Use Cases
### [Workflow Name]
- Goal:
- Trigger:
- Main Steps:
- Involved Modules:
- Associated Invariants:
- Code Correspondence: (format `[path/file#Function/Class.method()]`)

---

## 6. Architectural Decisions (ADR)
| Decision | Impact | Replaces | Status (Active/Obsolete) |
|----------|--------|----------|--------------------------|

---

## 7. Intention ↔ Code Traceability
| ISR Element (Glossary Ref, Module, Workflow, ADR) | Implementation (Code/Test) (format `[path/file#Function/Class.method()]`) | **Conformity Status** (Conforming/Partial/Divergent) |
|-------------|---------------------------------------------------------------------|---------------------------------------------------|

---

## 8. Non-Functional Constraints (optional)
| Type | Description | Architectural Impact |
|------|-------------|----------------------|

---

## 9. Controlled History (optional)
| Change | Impact | Date or Context |
|--------|--------|-----------------|