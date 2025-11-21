# CONTRIBUTING.md

## 🤝 Welcome to the ISR Contribution Guide!

We welcome contributions aimed at refining the **Intentional Software Representation (ISR)** methodology. Our goal is to make ISR the most efficient and robust framework for AI-assisted architecture.

Before submitting a Pull Request (PR), please read this guide and ensure your contribution aligns with the core principles of the ISR approach.

---

## 🎯 Areas of Contribution

Contributions are primarily sought in the following high-impact areas:

### 1. ⚙️ LLM Directive and Protocol Refinements (`ISR-directive-LLM.md`, `ISR-bootstrapping.md`)

* **Improvement of Verification Methods:** Proposals for new, more rigorous checks that the LLM can perform (e.g., specific code patterns that reliably indicate a divergence from an Invariant).
* **Ambiguity Management:** Enhancing the LLM's protocol for identifying, quantifying, and presenting structural or semantic ambiguities to the user.
* **Performance Optimization:** Suggesting clearer, more concise wording that aids the LLM's reasoning engine while maintaining precision.

### 2. 📝 Template Structure (`ISR-template.md`)

* **Refining Semantic Types:** Proposing additions or modifications to the types available in the Glossary (e.g., adding `Policy`, `Value Object`, or `Saga` if they improve architectural clarity).
* **New Sections:** Suggesting new structured sections to capture critical architectural intent that is currently missing (e.g., a section dedicated to Security Boundaries or Data Flow across modules).
* **Traceability Enhancements:** Improving the format or data points required for better bidirectional traceability between code and intent.

### 3. 📖 Documentation (`README.md`, `ISR-vision.md`)

* **Clarity and Accessibility:** Enhancing the explanation of complex concepts (Invariants, Intentional Orientation) for a broader audience.
* **Workflow Examples:** Providing detailed, practical examples of the ISR process applied to common architectural patterns (e.g., Microservices, Event Sourcing).

---

## 📏 Contribution Guidelines

To maintain the integrity and precision of the ISR methodology, please adhere to these specific guidelines:

### 1. Language and Terminology

* **English Only:** All structural elements, sections, and primary content within the ISR directive and template documents **must be in English** to ensure maximum LLM reasoning performance.
* **Canonical Terminology:** Use clear, accepted terminology from the fields of Software Architecture (e.g., Domain-Driven Design, Clean Architecture, SOLID).

### 2. Conciseness and Non-Redundancy

* **Directive-Driven:** Contributions to the directives must be actionable instructions for an AI, not narrative documentation.
* **Single Source of Truth:** Do not propose content that duplicates information already captured in another section of the ISR (e.g., a rule should be an Invariant, not repeated in a Workflow).

### 3. Verification Focus

* Every proposed addition to the **Template** must be **verifiable**. If a new field is added, you must specify how the LLM can check this intent against the source code or existing documentation.
* New directives must focus on **guarding the coherence** between intent and implementation.

---

## 🛠️ How to Submit a Contribution

1.  **Fork** the repository.
2.  **Create a new branch** for your feature or fix (`git checkout -b feature/my-new-directive`).
3.  **Implement your changes.** If you are proposing a new feature, explain its architectural justification.
4.  **Update the README (if necessary)** to reflect any major changes in the process.
5.  **Submit a Pull Request (PR)** against the `main` branch.

In your PR description, please clearly articulate:
* **[Context]** What problem does this contribution solve in the ISR workflow?
* **[Impact]** Which LLM capability (precision, traceability, verification) does this enhance?
* **[Justification]** Why is this change necessary from an architectural or semantic standpoint?

Thank you for helping us define the future of AI-assisted software architecture!