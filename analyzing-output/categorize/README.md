# Categorize Phase Methodology

## 1. Purpose & Objective
The final step of the BCIC method involves systematically organizing all checked, clarified, and revised requirements into a standardized framework. 

The purpose of the **Categorize** phase is to ensure that the repository baseline is logically structured, traceable, and completely prepared for the subsequent **Specifying** phase. Every requirement must have a logical "home" before detailed specification begins.

## 2. Approach & Standard Selection
NexaSpring has selected the **IEEE 830-1998** Recommended Practice for Software Requirements Specifications as our target standard. 

By mapping our revised requirements into this established framework, we guarantee a high-integrity SRS structure within our repository. This ensures the final requirement baseline is consistent, complete, and easily navigable by both technical and business stakeholders.

## 3. High-Level Categorization Rationale
To align with the IEEE 830 standard, we mapped the Interpreted requirements into the following major categories:

* **System Features (Section 3):** Our core business scenarios (SC01 to SC04 / SRS01 to SRS13) were mapped directly to this section. They represent the primary functional behaviors, inputs, and outputs for the application.
* **External Interface Requirements (Section 4):** Technical requirements (AR01 to AR05 / SRS14 to SRS17) were placed here. They capture specific constraints required by the client, such as hardware limitations (Android OS) and the necessary API/database interfaces the system must adhere to.
* **Security Requirements (Section 5.3):** Regulatory and compliance requirements revolving around data protection rules (PDPA, data retention, secure authentication) were mapped here as non-functional security constraints.
* **Design & Implementation Constraints (Section 2.5):** Requirements dictating specific technical limitations—such as 5MB file size limits and specific input validation logic—were isolated into this section to clearly define restrictions on development options.

## 4. Directory Outputs

| File / Link | Description |
| :--- | :--- |
| **[ieee-mapping-matrix.xlsx](./ieee-mapping-matrix.xlsx)** | The master routing table. This Excel file maps every original Level 0 and Level 1 requirement to its new SRS ID, its target IEEE 830 section, and its exact folder destination in the repository. |
| **[categorized-requirements/](../../categorized-requirements/)** | The final destination of the BCIC process. This folder contains the actual markdown files for every requirement, structurally organized according to the mapping matrix. |

## 5. Next Steps
With the categorization complete, the Analyzing Phase is concluded. The repository is now formally handed over to the **Specifying** team to elaborate these baseline statements into full use cases, workflows, and technical parameters.