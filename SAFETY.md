# EpiFlow Safety and Human Oversight

**Status:** Proposed policy. EpiFlow is experimental and has not been validated for operational public-health use. This document does not establish that any AI system or workflow is safe, accurate, or suitable for a particular investigation.

## 1. Purpose and governing principle

EpiFlow is a human-led, AI-assisted methodology for outbreak investigation. Its AI may help qualified professionals work more systematically, but it is not an epidemiologist, public-health authority, laboratory professional, clinician, statistician, or incident commander.

> **AI output is evidence to review, not authority to obey.**

AI output must be treated as fallible and potentially incomplete. It must not be represented as verified fact or used as the sole basis for a consequential interpretation, recommendation, communication, or action. Qualified and authorized public-health professionals retain responsibility for decisions and their consequences.

This policy draws on EpiFlow's principles in [README.md](README.md) and is informed by the World Health Organization's *Ethics and governance of artificial intelligence for health: WHO guidance* (2021). In particular, it applies the WHO principles of protecting human autonomy; promoting well-being, safety, and the public interest; ensuring transparency and intelligibility; fostering responsibility and accountability; promoting inclusiveness and equity; and developing responsive and sustainable AI. These principles guide this policy; they do not validate EpiFlow or replace applicable law, public-health protocols, or institutional review.

## 2. What AI may do

Within an approved, supervised workflow, AI may assist with bounded, reviewable tasks such as:

- organizing information and investigation artifacts;
- finding candidate gaps, inconsistencies, or data-quality issues for human verification;
- searching or summarizing sources, provided source provenance is preserved and claims are checked against the sources;
- documenting assumptions and generating candidate hypotheses for investigation;
- drafting analysis code, queries, checklists, or reports for qualified human review;
- proposing analytic approaches or identifying possible limitations for expert consideration.

AI-generated code or queries are proposals, not validated tools. A qualified analyst must inspect and test them against the approved analytic plan and data before use. Statistical calculations and data transformations should be carried out by reproducible, appropriately tested tools wherever feasible, not accepted from an AI narrative alone.

## 3. What AI must never do autonomously

AI must not independently:

- determine that an outbreak exists, identify its cause or source, interpret epidemiologic significance, or declare an investigation complete;
- establish or change case definitions, analytic plans, methods, thresholds, or data inclusion rules;
- make or authorize diagnoses, treatment or care decisions, risk classifications, public-health recommendations, or interventions;
- decide whether to notify, quarantine, isolate, test, close, restrict, or otherwise affect people, services, facilities, or communities;
- issue or publish public communications, official findings, alerts, or reports;
- access, link, disclose, or transmit sensitive data outside an explicitly authorized and approved workflow;
- conceal uncertainty, fabricate or embellish evidence, or silently change inputs, assumptions, code, or results;
- continue a consequential workflow after a safety, data-integrity, privacy, or reproducibility failure.

These decisions and actions belong to qualified, authorized public-health professionals and the relevant public-health authorities. Human review must be substantive: a person must understand the evidence and implications, not merely approve an AI-produced answer.

## 4. Mandatory human approval gates

An appropriately qualified and authorized human must review and explicitly approve each applicable gate before the workflow proceeds:

1. **Purpose, authority, and data access:** confirm the public-health purpose, lawful authority, permitted data, approved tools, and access controls before providing data to an AI system.
2. **Investigation and analysis design:** approve the question, case definitions, data sources, analytic plan, assumptions, and proposed methods before consequential analysis.
3. **Data preparation and code:** review material data transformations, AI-generated code or queries, validation checks, and test results before execution on operational data or use of resulting outputs.
4. **Interpretation:** independently examine the underlying evidence, methods, limitations, and uncertainty before adopting or communicating any interpretation or recommendation.
5. **Release and action:** the responsible authority must approve all consequential recommendations, public or partner communications, official findings, and public-health actions before release or implementation.

Approval must be attributable and recorded, including the reviewer, role, date, scope of review, decision, and any conditions or unresolved limitations. For urgent situations, established emergency procedures and delegated authorities still apply; AI does not acquire decision authority because time is limited.

## 5. When the system must abstain

AI and the workflow must stop short of a conclusion or recommendation, and clearly state why, when:

- the question exceeds the system's validated or approved scope, or a suitable validation basis is absent;
- evidence is missing, stale, unverifiable, contradictory, or insufficient for the requested inference;
- data quality, missingness, representativeness, linkage, or measurement problems could materially alter results;
- sources cannot be traced, a citation cannot be verified, or the output depends on an unsupported assumption;
- the result is sensitive to plausible analytic choices, or the method's assumptions are not met;
- model, tool, data, or execution behavior is unexpected, unstable, or not reproducible;
- privacy, security, legal authority, consent, or data-use approval is uncertain;
- the task asks AI to make a decision reserved for a qualified professional or authority.

Abstention must not be replaced with a guess, a fabricated citation, false precision, or an unqualified answer. The system should identify what is unresolved and what evidence or qualified review is needed. A human professional may proceed using established methods and authority, independently of the AI output.

## 6. Evidence, citations, and provenance

Every material factual claim or analytic output intended for human reliance must be traceable to its basis. Preserve, as applicable:

- source title, issuing organization or author, publication or collection date, stable link or identifier, access date, and relevant page, section, or dataset location;
- the data version and authorized source, relevant selection criteria, and transformations;
- the distinction between observed data, source-reported facts, derived results, assumptions, hypotheses, and AI-generated suggestions;
- analytic methods, definitions, code or query versions, parameters, and validation results;
- unresolved source conflicts, limitations, and the person who verified material sources.

AI-generated citations and summaries must be checked against the underlying source. If a source does not support a claim, the claim must be corrected, removed, or marked unverified. Do not treat fluent wording, model confidence, or repeated AI output as evidence.

## 7. Reproducibility and auditability

For each consequential AI-assisted analysis, retain an access-controlled record sufficient for an authorized reviewer to understand and, where feasible, reproduce the work. Record the purpose, relevant inputs and versions, transformations, assumptions, methods, code or queries, software and model/service identifiers and versions when available, material configuration and prompts, execution date, outputs, review decisions, and deviations or failures.

Use versioned artifacts and tested, deterministic calculations where feasible. Record random seeds and relevant environment details when they affect results. If the same inputs and declared process cannot reproduce a material result, disclose the discrepancy, investigate it, and do not rely on that result until a qualified reviewer resolves it. Do not retain sensitive prompts, data, or outputs in logs or artifacts unless that retention is authorized and protected.

## 8. Uncertainty and limitations

Uncertainty must be visible and proportionate to the evidence. Reports and drafts must distinguish data limitations and statistical uncertainty from uncertainty about source reliability, methods, assumptions, and AI-generated content. Disclose relevant missing data, bias, confounding, measurement error, sample size, generalizability, and plausible alternative explanations.

Do not imply certainty from precise-looking numbers, a single model output, or agreement among repeated runs of the same system. Preserve meaningful ranges, disagreement, and competing interpretations. AI confidence scores, when present, are not calibrated probabilities of epidemiologic truth unless independently validated for that precise use. Qualified professionals determine whether evidence is sufficient for an interpretation or action.

## 9. Privacy and sensitive-data boundaries

Use only the minimum data necessary for an authorized purpose, in systems approved for the data's sensitivity and jurisdiction. Do not enter identifiable, personal, health, location, or other sensitive information into a public or unapproved AI service. Use of such data in any AI workflow requires prior confirmation of lawful authority, applicable consent or other required basis, institutional approval, vendor and retention terms, access controls, security protections, and data-minimization measures.

De-identification or pseudonymization does not guarantee anonymity; re-identification and linkage risks must be considered. Protect prompts, outputs, logs, working files, and derived datasets to the same standard as their most sensitive contents. Do not disclose person-level information in reports or communications unless specifically authorized and necessary under applicable policy. When data handling requirements are unclear, stop and consult the designated privacy, security, or data-governance authority.

## 10. Independent review

Before consequential findings or recommendations are relied on or released, a qualified reviewer who did not produce the AI output must independently examine the relevant source evidence, data quality, methods, code or queries, results, uncertainty, and limitations. The reviewer must be able to reproduce or otherwise independently verify material results using the underlying evidence and appropriate tools.

Reviewers must have relevant public-health or analytic expertise and sufficient independence to challenge the work. Higher-impact decisions, novel methods, material disagreement, or substantial uncertainty require review at an appropriate level by additional subject-matter experts or the responsible public-health authority. AI review of AI output does not count as independent human review.

## 11. Failures, escalation, and correction

If AI output, data, code, tools, or workflow behavior is wrong, unexplained, unsafe, or not reproducible:

1. stop the affected analysis or release; do not silently patch over or rely on the result;
2. preserve relevant authorized records and identify affected outputs, decisions, and recipients;
3. promptly notify the responsible investigation lead and escalate privacy or security concerns to the designated institutional contacts, and consequential public-health concerns to the appropriate authority;
4. have qualified professionals assess the impact, independently re-analyze using approved methods where needed, and correct or withdraw affected communications;
5. document the incident, resolution, and preventive actions, and resume only after the responsible authority approves.

Where an immediate public-health response is needed, follow established incident-command and escalation procedures. AI must not delay required human action, suppress a warning, or substitute for the responsible authority.

## 12. Reference

- World Health Organization. *Ethics and governance of artificial intelligence for health: WHO guidance*. 2021. [Publication page](https://www.who.int/publications/i/item/9789240029200). ISBN 978-92-4-002920-0.
