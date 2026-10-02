# EpiFlow Governance

**Status:** Proposed policy. EpiFlow is experimental and has not been validated for operational public-health use. This policy governs project changes; it does not grant authority to conduct an investigation, use data, or make public-health decisions.

## 1. Governing principles

EpiFlow is a human-led, AI-assisted framework. AI output is fallible evidence to review, not authority to obey. Qualified, authorized people remain responsible for epidemiologic interpretations, recommendations, communications, and actions. Governance review does not replace applicable law, institutional approval, or public-health authority.

This policy should be read with [README.md](README.md) and [SAFETY.md](SAFETY.md). Where requirements differ, follow the more protective requirement and applicable law or institutional policy.

## 2. Who approves changes

Changes are proposed and reviewed through a pull request with a clear rationale, scope, impact, evidence, and any required review records. Authors must not be the sole approver of their own changes.

- **Routine project changes** may be approved by a project maintainer who is not the author.
- **Core-methodology changes** require approval from a project maintainer and an independent reviewer with relevant epidemiology expertise. The reviewer must be qualified to assess the affected methods and their intended public-health use. Their role and basis for qualification must be recorded in the review. If a suitably qualified reviewer is unavailable, the change must not be accepted as approved methodology.
- **Safety, privacy, or security-sensitive changes** require review by a person with relevant expertise in the affected area, in addition to maintainer approval. Seek more than one specialist review when the change has substantial potential impact or unresolved risks.
- A person with more than one relevant qualification may cover multiple review areas, but the review must explicitly address each area. Approval records must identify reviewers, roles, date, scope, decision, and conditions or unresolved limitations.

These requirements define the minimum review process; they do not imply that EpiFlow currently has designated epidemiology, privacy, safety, or security officers.

## 3. Changes requiring specialist review

### Epidemiology review

Obtain epidemiology review for changes that define, alter, or make claims about:

- investigation questions, case definitions, inclusion or exclusion criteria, data sources, or analytic plans;
- epidemiologic, statistical, causal, surveillance, or outbreak-detection methods, assumptions, thresholds, or interpretations;
- the meaning, limitations, or intended use of outputs or recommendations;
- validation design, performance measures, evidence of validity, or claims about generalizability.

Reviewers should assess appropriateness for the stated population, setting, data, and purpose; uncertainty, bias, confounding, and alternative explanations; and whether the method could be mistaken for an authoritative decision.

### Safety and privacy review

Obtain safety and privacy review for changes that affect:

- the handling, collection, linkage, retention, disclosure, or transmission of personal, health, location, or other sensitive data;
- data access, consent or other legal basis, de-identification, security controls, vendors, logs, or user permissions;
- human approval gates, abstention, escalation, incident response, or the ability to stop consequential workflows;
- AI autonomy, automation, public communications, interventions, or other pathways that could materially affect people or communities;
- foreseeable risks of inequity, stigmatization, misuse, or unsafe reliance.

Changes that introduce or materially change software, infrastructure, or data flows must also receive security review appropriate to their risks. If the applicable authority, protections, or review are uncertain, do not proceed with the affected data or workflow until resolved.

## 4. Experimental features and claims

Every feature, method, workflow, or result that has not met the validation requirements in section 8 must be explicitly labeled **Experimental — not validated for operational public-health use** wherever it is introduced or presented. Keep the label visible in relevant documentation and user-facing materials; do not rely on a distant disclaimer.

Describe the intended scope, known limitations, and required human review alongside the label. Do not imply that a feature is safe, accurate, approved, recommended, or ready for operational use merely because it is implemented, tested, or reviewed. Remove or update the label only through the review and evidence requirements in this policy.

## 5. Public-health guidance and citations

When a claim relies on public-health guidance, cite the original authoritative publication or issuing authority, not an AI summary or an uncited secondary account. Prefer the current guidance from the competent public-health authority for the jurisdiction and question; where applicable, consult recognized national or international public-health agencies and clearly explain why the source is relevant.

For each material guidance citation, record the issuing body or author, exact title, publication or update date and version, stable link or identifier, access date, and relevant page, section, or recommendation. Verify that the source is authentic, current for the stated use, and actually supports the claim. Note jurisdiction, population, scope, and any known superseding or conflicting guidance. Preserve dated sources when documenting what guidance applied to a past decision.

AI-generated citations and summaries must be checked against the source. If the source cannot be verified or does not support the claim, correct or remove the claim, or clearly mark it unverified; do not invent or infer a citation.

## 6. Conflicts with established guidance

AI-generated recommendations do not override established public-health guidance, law, institutional protocols, or decisions of the competent authority. If an AI output conflicts with applicable guidance:

1. Do not present, implement, or communicate the AI output as a recommendation.
2. Record the conflicting output and the relevant guidance, including source, jurisdiction, date, and scope.
3. Escalate the discrepancy to the responsible qualified professional and, when consequential or unresolved, the appropriate public-health authority.
4. Follow the applicable authority's current direction. Any departure from established guidance must be explicitly justified, documented, and authorized by the competent human authority under applicable procedures; AI output alone is not justification.
5. Correct or withdraw affected drafts or outputs and document the resolution.

When guidance itself is conflicting, outdated, or inapplicable, abstain from resolving the conflict through AI-generated judgment. Seek direction from the competent authority and make uncertainty explicit.

## 7. Versioning and change review

Use version control and reviewable pull requests for changes to methodology, policy, documentation, and implementation. The change record must summarize what changed and why, identify affected intended uses, link supporting evidence and specialist reviews, describe tests or validation performed, and disclose limitations, risks, and migration or communication needs. Material outputs and decisions should retain enough version and provenance information to identify the methodology and guidance used.

Use semantic versioning (`MAJOR.MINOR.PATCH`) for published EpiFlow releases: increment **MAJOR** for incompatible or materially changed methodology or policy; **MINOR** for backward-compatible capabilities or guidance updates that affect use; and **PATCH** for compatible corrections that do not change intended use or methodological meaning. A change to core methodology must never be characterized as a routine patch. Document methodological and policy changes in release notes, including their rationale and review.

Review governance and safety policies at least annually and after a material safety, privacy, methodological, or regulatory change, or a relevant incident. Record the review date and resulting decision, including when no change is made. Urgent changes must still receive the required review before they are represented as approved; interim mitigations must be clearly identified.

## 8. Requirements for describing something as validated

Implementation, unit tests, internal review, plausible outputs, or agreement between AI runs do not by themselves establish validation. A feature, method, or workflow may be described as **validated** only for a clearly stated intended use and only after the supporting evidence and reviews are documented.

At minimum, the record must include:

- the specific intended use, population, setting, inputs, and boundaries for which validity is claimed;
- a prespecified evaluation protocol, appropriate reference standard or comparator, justified performance measures, acceptance criteria, and representative data independent of development where feasible;
- reproducible results, documented data and method versions, error and failure analysis, uncertainty, limitations, and assessment of relevant subgroups and foreseeable harms;
- independent review by a qualified epidemiology reviewer and any other relevant domain experts, with safety, privacy, and security review proportionate to the workflow;
- confirmation that required legal, institutional, and public-health approvals are in place for the proposed operational use.

The claim must identify what was evaluated, by whom, when, and for which scope, and must not imply validity beyond the evidence. If evidence is incomplete, the feature remains experimental and its limitations must be stated. Validation does not grant operational authorization or replace ongoing monitoring and re-evaluation when data, models, methods, guidance, or intended use change.
