# Line-list quality review

**Status: Experimental — not validated for operational public-health use.**

## 1. Purpose

Review an authorized outbreak-investigation line list for traceable data-quality issues and report them to qualified investigators. A line list systematically organizes case information for investigation and descriptive epidemiology. This review supports, but does not replace, investigator assessment of the data's quality, completeness, validity, reliability, and consistency.

The review identifies observable errors and candidate anomalies; it does not determine their epidemiologic meaning. AI output is fallible evidence to review, not authority to obey.

## 2. Scope

This skill is limited to a non-destructive quality review of a supplied line list and its approved supporting metadata. It may identify records or fields for human follow-up and summarize checks performed. It does not classify people as cases, decide whether a record is valid for an investigation, analyze outbreak patterns, or make epidemiologic conclusions.

Apply only checks supported by the approved investigation materials. The user or responsible investigator remains responsible for the review purpose, data authorization, applicable rules, interpretation, and any action.

## 3. Required inputs

- An authorized line list in a readable format, or an authorized extract sufficient for the requested review.
- The investigation purpose and the scope of the requested checks.
- A stable, privacy-appropriate way to refer to each source record, such as an approved case identifier or source row reference.
- Any schema, case definition, data dictionary, or investigator-supplied rules needed to determine required fields, valid values, ranges, date conventions, or cross-field relationships. If none is supplied, report that rules-dependent checks cannot be completed; do not invent them.
- Confirmation that the data and the tool used for review are authorized for this purpose and sensitivity.

## 4. Optional inputs

Use these only when supplied and approved:

- An approved schema, data dictionary, variable specifications, and prior schema versions.
- The current human-approved case definition, including fields required to apply it. Do not use it to classify records.
- Investigation-specific expected ranges, allowed categories, date formats, sequence rules, or validation rules.
- A reference date or reporting cutoff for assessing future dates.
- Expected record counts, source-system totals, import/export logs, and documented inclusion or exclusion rules.
- A prior authorized line-list version for comparison, with version/date and permitted comparison scope.
- Investigator-approved duplicate-review keys, linkage rules, or known identifier crosswalks.
- A secure means for an authorized investigator to resolve record references without including direct identifiers in the report.

## 5. Preconditions

Before reviewing:

1. Confirm authorization, purpose, permitted data handling, and that the review environment is approved for the data. If uncertain, do not inspect or transmit the data; stop and escalate.
2. Confirm which file/version is in scope and preserve its supplied name, version or timestamp, and checksum/hash when available. Do not claim a hash was computed unless it was.
3. Identify the available metadata and distinguish supplied rules from assumptions. Record the reference date, source population, and expected counts only when explicitly provided.
4. Minimize exposure of sensitive data. Use the least identifying record reference that still permits secure human follow-up; do not copy direct identifiers or unnecessary values into findings.
5. If the input cannot be read reliably, is truncated, appears corrupted, or its encoding or structure is ambiguous, stop the affected checks and report the limitation rather than guessing.

## 6. Data-quality checks

Run only checks supported by the input and approved metadata. Record the method, denominator, and any exclusions for each check. A check not performed is not a clean result.

- **Record and identifier integrity:** look for exact duplicate rows and potentially duplicate records; duplicate case identifiers; missing, malformed, inconsistent, or reused identifiers; and inconsistent identifiers across explicitly supplied linked fields. Treat possible duplicates as candidates for human review, not as records to merge or remove.
- **Required fields and completeness:** identify missing required values only where the required fields are specified by an approved schema, case definition, or investigator. Summarize missingness by field and, when useful and safe, by supplied strata or source. Flag unexpected patterns only against an explicit comparator, documented rule, or clearly reported within-dataset pattern; do not infer a cause.
- **Dates and temporal consistency:** check parseability against supplied date formats; impossible or suspicious sequences against explicit rules; and dates later than a supplied reference date where future dates are inappropriate. Distinguish an unparseable value from an invalid date and a suspicious but possible sequence. Do not assume which event date should precede another.
- **Categorical values and coding:** compare values with supplied allowed categories, code lists, and coding conventions. Flag unlisted values or inconsistent coding only when the authoritative list or convention is available. Do not silently standardize variants.
- **Ranges and numeric validity:** compare values with approved ranges, units, and formats. Flag out-of-range values for review; do not treat statistical rarity alone as an error or invent clinical, exposure, age, or other plausible ranges.
- **Reliability and source consistency:** assess only against documented source or measurement procedures, repeatability criteria, or overlapping records explicitly supplied for comparison. Report observed disagreement and its basis; do not infer which source is correct or claim a measure is reliable without an approved standard.
- **Related-field consistency:** test only relationships explicitly defined by the case definition, schema, data dictionary, or investigator (for example, a documented date ordering or code-to-description pairing). Report the rule and observed conflict without choosing which field is correct.
- **Counts and denominators:** reconcile record counts, unique identifiers, subtotals, and denominators only against supplied totals, definitions, or documented inclusion/exclusion rules. Report the counts and comparison basis. Do not infer a correct denominator from the line list alone.
- **Schema and investigation requirements:** compare columns, names, types, and documented versions with the supplied approved schema or prior version. Identify changes. Report fields required by the investigation or case definition but absent from the dataset only when those requirements are supplied.
- **Other specified checks:** perform additional checks only when requested by an authorized investigator and supported by documented rules. State their basis and limitations.

Do not convert, overwrite, impute, delete, deduplicate, or otherwise alter the source data to perform or resolve these checks. Any comparison or parsing used for review must leave source values untouched and be described when it affects a finding.

## 7. Severity/classification of findings

Classify each finding on two separate dimensions:

**Evidence classification**

- **Confirmed data error:** directly demonstrates a violation of a supplied authoritative rule or documented source fact (for example, an exact duplicate identifier when uniqueness is explicitly required). This describes the data/rule conflict, not whether the person is a case.
- **Suspected anomaly — human review required:** unusual, inconsistent, incomplete, or potentially duplicated information that cannot be established as an error from available evidence.
- **Limitation / not assessable:** a check could not establish status because a required rule, metadata item, comparison source, or readable input was unavailable.

**Severity**

- **Critical:** a confirmed integrity or access/safety issue prevents safe or trustworthy continuation of the affected review, or requires immediate escalation under the investigation's procedures.
- **High:** a confirmed issue or substantial suspected anomaly could materially compromise record linkage, required-field assessment, count reconciliation, or another explicitly scoped check.
- **Moderate:** a potentially consequential issue is bounded to particular records or fields and needs investigator resolution.
- **Low:** a localized issue with limited apparent scope, or a documentation/coding inconsistency for follow-up.
- **Informational:** a schema/version difference, limitation, or observation with no demonstrated error or impact.

Severity describes the potential effect on the quality review, not clinical urgency, case status, or public-health risk. If impact cannot be assessed, state that and do not overstate severity. A suspected anomaly must never be presented as a confirmed error.

## 8. Required output format

Return a concise report with the following parts:

### Review summary

- **Dataset reviewed:** supplied file or dataset name, version/date, and hash/checksum if available.
- **Review scope:** purpose and checks requested.
- **Checks performed:** each check, applicable rule/basis, and number of records/fields assessed when determinable.
- **Checks not performed:** each omitted or incomplete check and why.
- **Summary counts by finding category:** include evidence classification and severity counts; make clear whether counts are findings or distinct affected records.
- **Source data status:** explicitly state: **“No source data were modified.”**

### Detailed findings

Use this format for each finding:

**Finding ID:**  
**Category:**  
**Severity:**  
**Evidence classification:**  
**Record/case reference:**  
**Field(s):**  
**Observed value/problem:**  
**Rule or evidence used:**  
**Why it was flagged:**  
**Confidence:**  
**Recommended human follow-up:**  
**Source/provenance:**

Use stable, minimally identifying references. Include exact field names and enough source location to trace each finding. Mask or omit sensitive values that are not needed for review; if masking affects verification, explain how the authorized reviewer can access the value securely.

### Unresolved questions

List missing rules, metadata, interpretation questions, or human decisions needed to complete or resolve the review. If none, state “None identified.”

## 9. Evidence and provenance requirements

- Identify the exact dataset version reviewed and its supplied provenance. Record a hash/checksum only if available or generated by an authorized, approved process.
- For every finding, preserve source row/case reference, exact source field name, and the value or problem in a privacy-minimizing form.
- Cite the precise schema, data dictionary, case-definition provision, investigator instruction, source-system total, prior version, or other rule used. Include document version/date and section or location when available.
- Distinguish observed values, comparisons, derived check results, assumptions, and AI-generated suggestions. Describe any comparison representation or parsing that affects the check; do not present it as a source-data change.
- Report check denominators and unavailable evidence where relevant. Do not imply a check passed when it was not performed.
- Do not invent source citations or imply that guidance supports a particular validation rule unless the original source and applicable section have been checked.

The methodological basis includes the CDC *Field Epidemiology Manual: Investigating an Outbreak* (online chapter: https://www.cdc.gov/field-epi-manual/php/chapters/investigating-outbreaks.html), especially its applicable material on finding and recording cases and describing cases. Verify the current chapter version, exact relevant section(s), access date, and applicability to the jurisdiction, population, setting, and question before relying on a specific claim. The source page could not be independently accessed while this draft was prepared; no version, access date, or exact section citation is asserted here. The repository's `references/methodology-sources.md`, `methodology/investigation-workflow.md`, `README.md`, `SAFETY.md`, and `GOVERNANCE.md` provide project context, not substitutes for the original guidance or validation of this skill.

## 10. Uncertainty and abstention rules

- State when required metadata or evidence is unavailable and which checks that prevents. Never fill gaps by assumption.
- Do not decide whether a record is a true case, whether a value is clinically plausible, why information is missing, or which conflicting field is correct.
- Do not label rare or unexpected-looking values as errors solely because they are uncommon.
- Do not infer missing clinical, exposure, or other investigation information.
- Distinguish parse failures, rule violations, possible anomalies, and unassessed items.
- If records, identifiers, schema, or rules conflict, report the conflict and abstain from choosing a resolution.
- If sensitivity, authorization, source integrity, or interpretation uncertainty could affect safe review, stop the affected work and escalate rather than guess.
- State confidence in the flagging evidence (for example, high/moderate/low), not confidence in a case determination or epidemiologic conclusion.

## 11. Human review requirements

Qualified investigators must review findings before taking action. Human reviewers determine whether a flagged value is an error, whether candidate records are duplicates, whether a rule applies, what corrections (if any) are authorized, and whether data limitations affect subsequent work. Review must be substantive, not a rubber stamp.

Any correction, deduplication, imputation, exclusion, or other source-data change must be separately authorized, documented, and performed by responsible personnel under approved procedures in a controlled, versioned process. This skill does not perform or recommend a particular correction as established fact.

## 12. Prohibited actions

This skill must never:

- Modify, delete, impute, deduplicate, overwrite, reorder, or silently normalize source data.
- Decide that a record is or is not a true case solely from a data-quality anomaly.
- Establish or alter a case definition, inclusion rule, threshold, or investigation requirement.
- Infer missing clinical, exposure, or other information or choose which conflicting value is correct.
- Invent expected ranges, allowed values, date sequences, required fields, count expectations, or coding rules not supplied by an approved schema, case definition, data dictionary, or investigator.
- Treat unusual values as errors merely because they are statistically uncommon.
- Make epidemiologic conclusions, diagnoses, risk classifications, recommendations, or public-health decisions.
- Expose sensitive information unnecessarily, or transmit it to an unapproved system.
- Claim checks were performed, data were validated, or a finding was confirmed without adequate evidence.

## 13. Failure/escalation conditions

Stop the affected review and promptly notify the responsible investigator or designated authority when:

- Authorization, permitted purpose, privacy, security, or tool approval is uncertain, or sensitive data may have been exposed.
- The input is unreadable, corrupted, incomplete in a way that undermines the review, or does not match its stated version.
- A material schema change, identifier conflict, count discrepancy, or source-integrity concern cannot be assessed under supplied rules.
- A critical issue is identified, a check produces irreproducible or contradictory results, or the task exceeds this skill's scope.
- A finding could require immediate public-health action. Escalate through established procedures; the quality review must not delay human action.

Record what was stopped, why, the affected checks, who was notified when authorized, and what human direction is needed. Do not continue the affected AI-assisted activity until appropriately authorized human review resolves the condition.

## 14. Example findings

Examples are illustrative formats only; they do not supply investigation rules or expected values.

**Finding ID:** LLQA-001  
**Category:** Identifier integrity  
**Severity:** High  
**Evidence classification:** Confirmed data error  
**Record/case reference:** Source rows 14 and 29  
**Field(s):** `case_id`  
**Observed value/problem:** The same identifier appears in both rows.  
**Rule or evidence used:** Supplied schema v2.1, “case_id must be unique.”  
**Why it was flagged:** The observed values violate the supplied uniqueness rule; this does not establish whether the rows describe the same person or whether either record is a case.  
**Confidence:** High that the supplied uniqueness rule is violated.  
**Recommended human follow-up:** Check the authorized source system and resolve the identifier conflict under investigation procedures.  
**Source/provenance:** Dataset `line-list.csv`, version supplied 2026-09-30, rows 14 and 29; schema v2.1, identifier field specification.

**Finding ID:** LLQA-002  
**Category:** Temporal consistency  
**Severity:** Moderate  
**Evidence classification:** Suspected anomaly — human review required  
**Record/case reference:** Source row 8  
**Field(s):** `onset_date`, `report_date`  
**Observed value/problem:** `report_date` precedes `onset_date`.  
**Rule or evidence used:** Investigator-supplied date sequence rule: onset date is not later than report date.  
**Why it was flagged:** The values conflict with the supplied rule; a data-entry issue or a context not represented in the rule may explain the sequence.  
**Confidence:** High that the stated rule is not met; low that either value is erroneous.  
**Recommended human follow-up:** Verify both dates against the authorized source record and confirm the rule applies to this record.  
**Source/provenance:** Dataset `line-list.csv`, version supplied 2026-09-30, row 8; investigator instructions, “Date checks,” version 1.

**Finding ID:** LLQA-003  
**Category:** Missing required field / limitation  
**Severity:** Informational  
**Evidence classification:** Limitation / not assessable  
**Record/case reference:** Dataset-level  
**Field(s):** Not assessable  
**Observed value/problem:** No approved schema, case definition, or investigator list of required fields was supplied.  
**Rule or evidence used:** None supplied.  
**Why it was flagged:** Required-field completeness cannot be evaluated without an authoritative list; no field has been presumed required.  
**Confidence:** High that the required-field specification was unavailable in the materials provided.  
**Recommended human follow-up:** Supply the approved requirements if this check is needed.  
**Source/provenance:** Materials received for this review; no required-field specification included.

## 15. Evaluation criteria

A review is acceptable only if it:

- Uses only authorized data and stays within the stated purpose and approved rules.
- Covers the requested, supported checks and transparently lists omitted or unassessable checks.
- Correctly separates confirmed rule violations from suspected anomalies and limitations.
- Preserves traceability to source records and fields while minimizing sensitive-data exposure.
- Does not invent validation rules, expected values, denominators, or causal explanations.
- Reports findings with evidence, confidence, provenance, and actionable human follow-up.
- Makes no case determinations or epidemiologic conclusions and does not alter source data.
- Includes the dataset/version/hash status, checks performed and not performed, category counts, unresolved questions, and the explicit statement that no source data were modified.
- Is reviewed by a qualified human before findings are relied on or acted upon.
