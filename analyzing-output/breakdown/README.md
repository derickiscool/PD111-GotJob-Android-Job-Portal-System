# Breakdown Phase Methodology

## 1. Purpose & Objective
In the **Breakdown** step, the team will separate the **Cogent Requirements** from the **Incongruent Requirements** across both business and technical specifications. 

The primary objective is to filter the Project Specification (PS) so that:
1.  **Cogent Items** are loaded directly into the Repository with minimal changes.
2.  **Incongruent Items** are isolated for "regulated-revision" (Clarify, Interpret, or Split) in subsequent BCIC steps.

## 2. Approach & Methodology
The Breakdown was executed by the Lead Business Analyst (BA) using the **Incongruous Requirements Checklist (IRC)** as the primary screening tool. 

### The Process
1.  **Screening:** Each requirement in the original PS was reviewed against the IRC criteria (Imperative, Contextual, Atomicity).
2.  **Tagging:** Requirements were tagged as either:
    * **Cogent:** No IRC flags raised; sufficiently clear and consistent.
    * **Incongruent:** Flagged for specific issues (e.g., Ambiguity, Verifiability).
3.  **Action Assignment:** For every incongruent item, the BA assigned a specific remedial action:
    * **Revise:** Rewrite for clarity or professional tone.
    * **Clarify:** Consult stakeholders to resolve ambiguity (see `../clarify/`).
    * **Split:** Decompose compound requirements into atomic statements.
4.  **Gap Analysis:** The BA cross-checked the PS against industry-standard job portal expectations to identify omissions.

## 3. Breakdown Outputs

###  [Cogent Log](./cogent-log.xlsx)
This file contains the requirements from the PS that were deemed cogent by the BA. These requirements will be moved to the repository with minimal changes
 
###  [Incongruity Log](./incongruity-log.xlsx)
This file contains the complete audit trail of the Breakdown process. It lists:
* **Req ID:** The original identifier from the Project Specification.
* **IRC Flags:** Specific violation codes (e.g., `AMB`, `VER`, `IMP`).
* **Issue Summary:** A brief description of *why* the requirement was flagged.
* **Required Action:** The specific step taken next (Revise, Clarify, Split, Others).

*This log ensures we prevent unclear requirements from propagating into the repository baseline.*

### [IRC Definitions](../irc-checklist.md)
A reference document defining the specific criteria used for screening (e.g., what constitutes an "Ambiguous" requirement).

## 4. Summary of Findings

| Category | Definition | Action Taken |
| :--- | :--- | :--- |
| **(A) Cogent Requirements** | Requirements assessed as sufficiently clear, consistent, and ready. | Carried forward to the Repository requirements folder. 
| **(B) Incongruent Requirements** | Requirements flagged by the IRC for issues such as weak imperatives or lack of verifiability. | Subjected to **Regulated Revision** before being loaded into the Repository. |