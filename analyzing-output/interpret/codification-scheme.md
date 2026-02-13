# Requirement Codification Scheme

## 1. Purpose
To ensure strict traceability between the customer's original Project Specification (PS) and the final Software Requirements Specification (SRS), NexaSpring applies a standardized codification scheme during the **Interpret** phase.

The customer's original IDs (e.g., `SC01.3a`, `RE04`) contain inconsistencies, mixed formats, and gaps due to requirements that were deleted, merged, or split during the Breakdown and Clarify phases. To resolve this, we convert all requirements into a unified, flat numbering system.

## 2. Format
All interpreted requirements are assigned a new, purely sequential ID using the following flat format:

**Format:** `SRS##` (e.g., `SRS01`, `SRS02`, `SRS15`)

### Codification Rules:
* **Flat Structure:** We do not use category-specific prefixes (like `FUNC` or `SEC`) at this stage. All requirements—whether Business (Biz) or Technical (Tech)—share the same sequential numbering pool.
* **Continuous Numbering:** IDs are assigned sequentially from top to bottom based on the logical flow of the system's workflows, removing any gaps left by incongruent requirements.

## 3. Traceability Maintenance
Because the new IDs are completely flat, traceability back to the customer's original intent is maintained entirely through the **Interpret Phase Mapping Matrix** (`revised-reqrs-logs.xlsx`).

**Traceability Rules:**
No original requirement is permanently deleted without a trace. The mapping file tracks the evolution of the requirements in three specific ways:
1. **Direct Translation:** A single original ID maps perfectly to a single new ID (e.g., `SC01.1` becomes `SRS01`).
2. **Merging Logic:** Multiple redundant or granular original IDs are combined into a single new atomic ID (e.g., `RE03.1` and `RE03.2` are merged into `SRS19`).
3. **Level 0 Grouping:** High-level parent IDs (e.g., `SC01`, `RE01`) are intentionally stripped of sequential SRS IDs (marked with a `-`) and retained purely as categorical headers to define the scope.