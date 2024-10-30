### **Manifest Specification Quick Guide**

***Purpose:***

- Defines the **Manifest**, a central JSON-based artifact for the **Accelerated IT Product Development Platform**.
- Ensures clear collaboration between **Editorial** and **Generator Teams** using **Domain-Driven Design (DDD)** principles.

***Structure:***

- **Hierarchical JSON Directories:**
    - `entities/` – Domain entities
    - `valueObjects/` – Immutable value types
    - `workflows/` – Business process sequences
    - `services/` – Business logic and APIs
        - `apis/` – External interactions
        - `triggers/` – Event-driven workflows
    - `tests/` – Validation scenarios
    - `manifest.json` – Global settings

***Key Rules:***

- **Naming Conventions:** Use **PascalCase** for all names (e.g., `CustomerOrder`, `ProcessPayment`).
- **Data Types:**
    - **Primitive:** String, Integer, Float, Decimal, Boolean, Date, DateTime, Enum
    - **Complex:** Value Objects, Entity References, Collections (`Type[]`)

***Component Schemas:***

- **Entities & Value Objects:** Define attributes with types, defaults, and documentation.
- **Workflows:** Outline inputs, outputs, steps, and mappings.
- **Activities:**
    - **Definition:** Fundamental building blocks in creating workflows.
    - **Function:** Represent individual, reusable tasks or operations that can be configured and combined to develop complex business processes.
    - **Organization:** Categorized into Data Operations, Flow Control, Logical Operations, etc.
    - **Configuration:** Each activity type has specific configurable settings, inputs, and outputs that dictate its functionality within a workflow.
- **Services:** Specify exposed workflows and middleware.
- **APIs:** Detail endpoints, methods, parameters, responses, and workflow integrations.
- **Triggers:** Link events to workflows with conditions and mappings.
- **Tests:** Describe workflows, inputs, expected outputs for validation.

***Usage:***

- Organize application components clearly within the Manifest.
- Follow structured JSON schemas for consistency.
- Adhere to naming and data type standards for seamless team collaboration.