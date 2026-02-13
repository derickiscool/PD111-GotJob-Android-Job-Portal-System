# Incongruous Requirements Checklist (IRC)

This document defines the criteria used by the analysis team to flag "Incongruent" requirements during the Breakdown phase.

| Category | Code | Checklist Criteria (What we check) |
| :--- | :--- | :--- |
| **Imperative** | **IMP-1** | Check the appropriateness of the imperative level and priority, from highest to lowest strictness. (Shall, Must/must not, Is required to, Are applicable, Responsible for, Will, Should) |
| **Imperative** | **IMP-2** | Check that there are no mixed imperatives within one requirement. |
| **Continuance** | **CN** | Verify that use of continuance phrases do not create unnecessary complexity in any reqrs. (Below, As follows, Following, Listed, In particular, Supported by). If used, ensure it is explicitly traceable. |
| **Contextual** | **CS** | Check **consistency** with related reqrs, processes and models. |
| **Contextual** | **TST** | Check the reqr is **testable** by defining observable behavior and clear pass or fail criteria, where appropriate. |
| **Contextual** | **PRI** | Check that **priority** is explicitly stated where required, and is **consistent** with the imperative level used. |
| **Contextual**| **AMB** | Check the reqr is **unambiguous** and uses defined terms consistently. (No vague words). |
| **Contextual** | **VER** | Check the reqr is **verifiable** against customer policy, regulations, or business rules, and state the evidence (if required). |
| **Contextual**| **SUB** | Check that the reqr is necessary, meaningful and aligns with the PS scope. (**Substantive Validity**) |
| **Contextual** | **CMP** | Check the reqr is **complete**, including conditions, exceptions or edge cases if implied in the PS workflow. |
| **Contextual** | **FEA** | Check **feasibility** and **realism** (against known constraints). |
| **Contextual**| **REA** | Check **readability** and correctness (grammar, typos, missing words) to support regulated-revision quality. |
| **Atomicity** | **ATM** | Check **atomicity**. Each reqr should express one primary idea and avoid bundling multiple behaviours. |

## Findings Log
The actual application of this checklist to the Project Specification is documented in the **Incongruity Log**.

* **Location:** `analyzing-output/breakdown/incongruity-log.xlsx`
* **Format:** The log tracks each incongruent requirement using the following structure:

| Req ID | IRC Code | Issue Summary | Action |
| :--- | :--- | :--- | :--- |
| *[Original PS ID]* | *[IMP-1 / AMB]* | *[Description of the flaw]* | *[Revise / Clarify / Split / Others]* |
