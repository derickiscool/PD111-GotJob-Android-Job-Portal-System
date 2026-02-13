# PD111-GotJob: Android Job Portal System
**Requirements Analysis Repository for Team 2634C (GotJob Project)**

## Project Overview
GotJob is a dedicated native Android job portal system developed for **Uwais Hiring Agency**. This system bridges the gap between job seekers and recruiters by providing a centralized platform for profile management, job postings, automated discovery, and real-time communication. 

This repository serves as the content for the project's **Software Requirements Specification (SRS)**, documenting the transformation of raw customer needs into highly structured, verifiable engineering standards.

## The Team (Team 2634C, NexaSpring)
| Name | Role / Focus Area |
| :--- | :--- |
| **Cheng Yi Zhen** | Requirements Analysis Lead |
| **Derick Lee** | Business Analysis & Requirements Engineering |
| **Muhammad Lutfi Lais** | Systems & Technical Analysis |
| **Tan Yu Xuan** | Process Modelling & Documentation |
| **Uwais Alqarni Bin Abdul Rahman** | Stakeholder & Domain Analysis |
| **Sarah Tan** | Account Manager |

## Methodology: BCIC Framework
To ensure a rigorous and traceable requirements engineering process, our team applied the **BCIC Method**:
1. **[Breakdown](./analyzing-output/breakdown/):** Deconstructing the initial Project Specification (PS) into atomic, testable statements and flagging incongruent requirements.
2. **[Clarify](./analyzing-output/clarify/):** Resolving ambiguities (e.g., matching logic, PDPA retention) directly with stakeholders via face-to-face meetings and 2D paper-napkin modeling.
3. **[Interpret](./analyzing-output/interpret/):** Rewriting clarified requirements using strict imperative language ("shall/must") and applying a flat, sequential codification scheme (`SRS01`, `SRS02`, etc.).
4. **[Categorize](./analyzing-output/categorize/):** Structuring the final requirement baseline logically in preparation for formal specification.

## Repository Structure & IEEE 830 Standard
We have structured our final deliverables in strict accordance with the **IEEE 830-1998 Recommended Practice for Software Requirements Specifications**.

You can navigate our repository using the directory tree below:

```text
PD111-GotJob-Repository
 ┣ 📂 analyzing-output/             # The raw BCIC process evidence
 ┃ ┣ 📂 breakdown/                  # IRC checklists and raw logs
 ┃ ┣ 📂 clarify/                    # Meeting notes and paper-napkin prototypes
 ┃ ┣ 📂 interpret/                  # Requirement mapping matrix & codification scheme
 ┃ ┗ 📂 categorize/                 # Final routing matrix to the IEEE 830 standard
 ┃
 ┗ 📂 categorized-requirements/     # The Final SRS Document Baseline
   ┣ 📂 1-introduction/
   ┣ 📂 2-overall-description/
   ┣ 📂 3-system-features/         
   ┣ 📂 4-external-interface-requirements/ 
   ┣ 📂 5-other-non-functional-requirements/ 
   ┣ 📂 6-other-requirements/
   ┗ 📂 appendices/     
   ```           