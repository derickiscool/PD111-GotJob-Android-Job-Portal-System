# Analyzing Phase Methodology (BCIC)

## 1. Overview & Purpose
The purpose of the **Analyzing Phase** is to deliver a **regulated-revision** of the customer’s Project Specification (PS) for the *GotJob?* application. 

Our objective was to check, correct, and enhance the requirements to ensure they are clear, complete, consistent, and implementable, while strictly retaining alignment with the customer’s original business intent. The output of this phase is a revised requirement baseline, loaded into this Repository, which serves as the input for the specifying phase.

## 2. Scope & Methodology
We reviewed both business operations and technical requirements using the **BCIC (Breakdown, Clarify, Interpret, Categorize)** method.

### The Role of the IRC (Incongruous Requirements Checklist)
To support the **Breakdown** step, we utilized a custom **Incongruous Requirements Checklist (IRC)**. This checklist served as our primary filter to detect requirements that were:
* **Imperative:** Lacking proper strictness (e.g., "should" vs "shall").
* **Contextual:** Ambiguous, unverifiable, or substantively invalid.
* **Atomic:** Bundling too many operations into a single clause.

*The full definition of our IRC criteria can be found in  `analyzing-output/irc-checklist.md/` .*

## 3. Phase Structure
This directory is organized according to the BCIC workflow:

| Folder | Description |
| :--- | :--- |
| **[breakdown/](./breakdown/)** | Contains the Incongruity Log made from using the IRC checklist on the requirements from the PS |
| **[clarify/](./clarify/)** | Documentation of stakeholder meetings. |
| **[interpret/](./interpret/)** |The revised requirements, translated from the client's language into professional technical language. |
| **[categorize/](./categorize/)** | The final mapping of requirements into the IEEE 830 standard structure for the SRS |