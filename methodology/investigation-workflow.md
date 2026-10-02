# EpiFlow investigation workflow

**Status: Draft mapping — Experimental; not validated for operational public-health use.**

## Scope and authority

This document maps EpiFlow to established field epidemiology outbreak-investigation practice; it does not propose a new epidemiologic method, protocol, or decision rule. The applicable sequence and methods must be taken from the current, relevant guidance of the competent public-health authority, informed by the CDC *Field Epidemiology Manual: Investigating an Outbreak* and the other applicable sources in the [methodology source register](../references/methodology-sources.md). The register is a finding aid, not a substitute for those sources.

Before relying on a particular method or claim, a qualified reviewer must consult its original source, verify its current version and applicability to the jurisdiction, population, setting, and question, and record the exact title, version/date, access date, and relevant section. WHO toolkit items and CDC course lessons must be identified precisely. Resolve source conflicts and uncertain applicability through qualified human and competent-authority review; do not infer a resolution from this mapping.

The stages below are a practical map of investigation activities, not mandatory gates that must be completed in this order. Investigators may conduct appropriate activities concurrently, return to earlier activities as evidence changes, or omit activities that are not applicable when qualified professionals document why. Applicable law, institutional policy, incident-command procedures, and competent-authority direction take precedence.

EpiFlow is an experimental support framework, not an operationally validated method. It does not determine whether an outbreak exists, set case definitions or analytic plans, interpret epidemiologic significance, recommend or authorize interventions, or declare an investigation complete. Qualified, authorized people retain those responsibilities. AI output is a suggestion to verify, not evidence or authority. Any AI use requires prior authorization for the purpose, data, and system.

**Urgent action must not wait for an AI workflow or its completion.** When a potential immediate threat or need for response is identified, notify the responsible professionals and authority and follow established emergency procedures without waiting for EpiFlow, further analysis, or completion of any stage. AI must not delay, suppress, or substitute for that action.

## Workflow stages

The common requirements below apply at every stage:

- Preserve the provenance and version of evidence, data, methods, and artifacts; separate observations and source-reported facts from derived results, assumptions, hypotheses, and AI suggestions.
- State what is unknown, conflicting, unverified, or limited. Do not convert missing evidence or AI confidence into certainty.
- Stop the affected AI-assisted activity and escalate if data authority or safety is uncertain, evidence cannot be verified, a material result is not reproducible, or the task exceeds approved scope. Continue or resume only under qualified human direction.

### 1. Organize and frame the investigation

- **Purpose:** Establish the public-health question, investigation organization, authority, scope, and an appropriate plan for gathering and assessing information.
- **Required inputs:** The signal or request prompting investigation; known setting, population, time period, and potential urgency; applicable authority and guidance; available information, people, and resources; and data-use, privacy, and security requirements.
- **Possible AI assistance:** Organize supplied, authorized material; draft an inventory of knowns and gaps; find candidate authoritative guidance; and prepare a planning or documentation draft for review.
- **Outputs/artifacts:** Human-approved question and scope; roles and escalation contacts; source and data inventories; an initial plan and assumptions log; and documented authorizations and unresolved constraints.
- **Human decision points:** Authorized professionals decide whether and how to investigate, who is responsible, what data and tools may be used, and whether immediate notification or action is needed.
- **Evidence requirements:** Record the basis for the signal, the authority for the work and data use, and verified source details for material guidance. Check AI-found sources against the original.
- **Uncertainty requirements:** Identify gaps in the initial account, uncertain authority or scope, and assumptions that could affect what information is gathered.
- **Escalate when:** A credible urgent threat, uncertain authority, sensitive-data concern, unavailable required expertise, or conflict in applicable direction is identified.
- **Revisit an earlier stage when:** The investigation question, authority, affected population, or intended use changes, or new information changes the rationale for the investigation.

### 2. Assess the signal, verify the diagnosis, and assess whether an unusual occurrence exists

- **Purpose:** Assess the reported health event and available evidence, including whether the reported diagnosis or event is supported and whether the observed occurrence warrants investigation as an outbreak or other public-health event.
- **Required inputs:** The initial reports and their provenance; relevant clinical, laboratory, surveillance, and contextual information that is authorized and available; and appropriate current definitions, baseline information, or guidance for the setting.
- **Possible AI assistance:** Organize reports, flag inconsistencies or missing fields, and prepare a source-linked summary of information for expert review. AI must not diagnose, verify a laboratory result, or decide that an outbreak exists.
- **Outputs/artifacts:** A human-reviewed account of what is reported and verified, the basis for any determination, unresolved questions, and a record of follow-up needed.
- **Human decision points:** Qualified professionals assess the diagnosis and the occurrence in context and decide whether further investigation, notification, or response is warranted.
- **Evidence requirements:** Preserve original report/source references and distinguish verified findings from reports, interpretations, and unconfirmed information. Any clinical or laboratory interpretation must be made by the appropriate professional.
- **Uncertainty requirements:** State limitations in diagnostic information, reporting, baseline comparisons, and timeliness; do not treat absence of reports as proof of absence.
- **Escalate when:** Findings suggest an immediate threat, a legally or procedurally reportable event, a serious discrepancy, or a need for specialist or competent-authority assessment.
- **Revisit an earlier stage when:** Verification changes the event description, affected group, time or place, urgency, or basis for the investigation.

### 3. Define cases and find and record cases

- **Purpose:** Support systematic identification and recording of cases appropriate to the investigation question, using a case definition established by qualified investigators.
- **Required inputs:** The current investigation question; verified information about the event; relevant current guidance; available authorized data sources; and a human-approved case definition and case-finding approach.
- **Possible AI assistance:** Format approved criteria into reviewable documentation, help organize authorized records, flag candidate matches or missing fields, and identify possible duplicates for human assessment. AI must not establish or change the case definition, classify people autonomously, or make individual care or risk decisions.
- **Outputs/artifacts:** Versioned, human-approved case definition and case-finding documentation; an access-controlled line list or equivalent authorized record; and documented screening, deduplication, and data-quality decisions.
- **Human decision points:** Qualified investigators set and revise case criteria, determine appropriate sources and procedures, assess candidate cases and duplicates, and authorize data access and handling.
- **Evidence requirements:** Retain the approved definition and its rationale/version, source provenance for included records, relevant dates and criteria, and a record of material data transformations and review.
- **Uncertainty requirements:** Make suspected, probable, confirmed, or other categories only as supported by applicable guidance; describe missing, delayed, misclassified, or incomplete records and how they may affect case ascertainment.
- **Escalate when:** Criteria or records could materially affect people, data authority is unclear, sensitive data may have been exposed, or classification cannot be supported from available evidence.
- **Revisit an earlier stage when:** New clinical, laboratory, exposure, or population information changes the event assessment or makes the question or approved case definition inadequate.

### 4. Describe cases and relevant events

- **Purpose:** Characterize the occurrence by appropriate person, place, and time information and other relevant descriptive features, to inform investigation and possible hypotheses.
- **Required inputs:** The approved case definition; an appropriately prepared dataset; documented sources, variables, and time/place conventions; and a human-approved descriptive analysis plan.
- **Possible AI assistance:** Check schemas and data quality, draft reproducible code or tables, identify candidate patterns for review, and draft plain-language descriptions. AI-generated code and calculations must be inspected, tested, and run using appropriate reproducible tools.
- **Outputs/artifacts:** Reproducible, versioned descriptive analyses; reviewed tables, figures, or summaries; data-quality and missingness records; and a log of analytic choices.
- **Human decision points:** Qualified analysts approve transformations, measures, displays, and interpretation; assess whether observed patterns are meaningful and appropriate to communicate.
- **Evidence requirements:** Preserve data versions, selection criteria, transformations, code, methods, parameters, test results, and the underlying results needed to independently check material claims.
- **Uncertainty requirements:** Describe missingness, measurement and reporting limitations, possible selection or ascertainment effects, and the descriptive nature and limits of the findings. Do not infer causation from descriptive patterns.
- **Escalate when:** Results are not reproducible, a data-integrity issue could change findings, a pattern implies a potentially urgent threat, or the analysis exceeds the approved plan.
- **Revisit an earlier stage when:** Data checks or descriptive findings reveal unsuitable case criteria, incomplete case finding, incorrect dates or locations, or a materially different event pattern.

### 5. Develop and assess hypotheses

- **Purpose:** Form plausible explanations from the investigation evidence and assess them using methods appropriate to the question and available data.
- **Required inputs:** Reviewed descriptive findings; relevant exposure, clinical, laboratory, environmental, or other evidence; the approved question and analytic plan; and applicable methods and guidance verified for the context.
- **Possible AI assistance:** Suggest candidate explanations explicitly labeled as hypotheses, organize evidence for and against them, and draft candidate analytic code or approaches for expert assessment. AI must not select a causal explanation or choose or execute an unapproved method.
- **Outputs/artifacts:** A versioned hypothesis record, including its evidence and assumptions; human-approved analytic design; reproducible analysis artifacts and results; and documented alternative explanations.
- **Human decision points:** Qualified epidemiologists and analysts formulate and prioritize hypotheses, select and approve suitable methods, assess assumptions and bias, and determine what the results do and do not support.
- **Evidence requirements:** Link each material claim to verified data or original sources. Record study design, definitions, methods, assumptions, code and validation, and the basis for considering alternatives.
- **Uncertainty requirements:** Address precision and statistical uncertainty where applicable, as well as bias, confounding, measurement error, missing data, assumptions, alternative explanations, and limits to causal inference or generalization.
- **Escalate when:** Evidence conflicts, key assumptions are not met, results are sensitive to plausible analytic choices, an important potential harm or urgent risk appears, or required expertise is unavailable.
- **Revisit an earlier stage when:** Analyses or new evidence challenge the hypothesis, reveal an unsuitable design or data source, change the case or exposure definitions needed, or leave important questions unanswered.

### 6. Refine the investigation and gather additional evidence

- **Purpose:** Resolve important uncertainties by refining questions or hypotheses and obtaining or assessing additional information or analyses when justified.
- **Required inputs:** The current evidence record; outstanding questions and limitations; approved authority, protocols, and data-use permissions; and an expert-approved rationale for additional work.
- **Possible AI assistance:** Summarize unresolved questions, identify candidate evidence gaps, organize new sources, and draft reviewable plans or code. AI must not expand access, collect sensitive information, or change the analytic plan without authorization.
- **Outputs/artifacts:** Human-approved refinements to questions or methods; a record of additional information and its provenance; updated analyses; and a documented account of what remains unresolved.
- **Human decision points:** Investigators decide whether further evidence is feasible and necessary, approve any changes to definitions, data sources, or methods, and ensure required approvals and safeguards are in place.
- **Evidence requirements:** Document why additional work is warranted, its authorization, source and version details, changes from prior work, and independent checks of resulting analyses.
- **Uncertainty requirements:** Distinguish uncertainty reduced by new evidence from uncertainty that remains; document new limitations introduced by additional data or analytic choices.
- **Escalate when:** Proposed work changes intended use or materially increases privacy, safety, or other risk; approval is absent; or evidence remains conflicting or insufficient for a consequential inference.
- **Revisit an earlier stage when:** Additional evidence changes event verification, case ascertainment, descriptive findings, or the assumptions and results of hypothesis assessment.

### 7. Apply, assess, and monitor control or prevention measures

- **Purpose:** Support the responsible authority's consideration and assessment of control or prevention measures under applicable public-health guidance and procedures.
- **Required inputs:** The current evidence and uncertainty record; applicable, current authority guidance; the potential benefits, harms, feasibility, and affected communities; and the authority and procedures for action and monitoring.
- **Possible AI assistance:** Organize verified evidence and guidance, identify questions or monitoring information for human consideration, and draft internal materials. AI must not recommend, authorize, implement, or communicate an intervention autonomously.
- **Outputs/artifacts:** The competent authority's documented decision and rationale; approved action and monitoring records, where applicable; and updates on observed implementation and outcomes.
- **Human decision points:** The competent authority decides whether, when, and how to act, including before investigation completion when warranted. Authorized professionals determine how to monitor and interpret effects.
- **Evidence requirements:** Cite current applicable guidance and verified evidence; record the source, date, decision-maker, rationale, scope, monitoring measures, and relevant limitations.
- **Uncertainty requirements:** State uncertainty relevant to the decision and its monitoring, including evidence gaps and plausible unintended effects. Do not imply that an observed change proves an intervention caused it.
- **Escalate when:** Immediate protective action may be needed, a proposed measure exceeds the decision-maker's authority, potential harms or inequities are material, or monitoring indicates unexpected effects.
- **Revisit an earlier stage when:** Monitoring, new cases, new exposure or laboratory evidence, or observed harms materially alter the assessment or the basis for action.

**This stage is not a gate that delays urgent action.** If the responsible authority determines that action is needed before earlier stages are complete, established emergency and delegated-authority procedures apply immediately; investigation and documentation continue alongside the response.

### 8. Communicate findings and maintain the record

- **Purpose:** Communicate verified findings, limitations, and decisions to appropriate audiences and preserve a reviewable investigation record.
- **Required inputs:** Human-reviewed evidence and analyses; source and decision records; relevant uncertainty and limitations; applicable communication requirements; and authorization for the audience and release.
- **Possible AI assistance:** Organize artifacts and draft audience-specific summaries or reports for substantive human review; check that draft claims link to sources. AI must not issue or publish alerts, findings, recommendations, or reports.
- **Outputs/artifacts:** Authorized and reviewed communications; a versioned investigation record; corrections or updates when needed; and a record of review, approval, release, and unresolved limitations.
- **Human decision points:** Qualified professionals verify claims and interpretation. The responsible authority approves consequential findings, recommendations, communications, and any declaration that the investigation is complete.
- **Evidence requirements:** Trace material statements to the underlying data, original sources, methods, and decision records. Preserve the relevant versions, review decisions, approvals, and corrections.
- **Uncertainty requirements:** Clearly distinguish confirmed facts, reports, derived results, hypotheses, and unresolved questions. Present limitations and uncertainty proportionately; do not overstate causation, precision, or generalizability.
- **Escalate when:** A material claim cannot be verified, a communication could cause harm or disclose protected information, findings conflict with applicable guidance, or a serious error has already been released.
- **Revisit an earlier stage when:** Review identifies unsupported claims, new evidence changes conclusions, a source is superseded, or post-release correction is required.

## Iteration, escalation, and stopping

The investigation is iterative, not a one-way checklist. Evidence, response monitoring, or expert review may require returning to any earlier stage; document the reason, changed evidence, and effect on prior artifacts and communications. Appropriate actions and investigation activities may proceed in parallel under the responsible authority.

At any stage, stop the affected AI-assisted task and escalate to the responsible investigation lead and relevant subject-matter, privacy, security, or competent-authority contacts when there is an urgent threat; an authority or data-use concern; a material evidence, data-integrity, safety, or reproducibility failure; an unresolved conflict in applicable guidance; or a consequential question outside approved scope. Preserve authorized records, assess affected results and communications, and resume the affected AI-assisted activity only after responsible human review. This stop condition does not prevent or delay urgent human public-health action under established procedures.

## Source basis and verification record

The source set is limited to the authoritative sources listed in [references/methodology-sources.md](../references/methodology-sources.md). The outbreak-investigation stage mapping is intended to be checked against the applicable current CDC *Field Epidemiology Manual* chapter and relevant WHO *Outbreak Toolkit* materials. CDC *Principles of Epidemiology in Public Health Practice* informs review of terminology, descriptive and analytic work, measures, design, interpretation, and limitations. WHO AI guidance and NIST AI RMF inform AI role boundaries and risk management, not epidemiologic methods. Other listed surveillance, privacy, and cybersecurity sources apply only to the relevant aspects of a particular use.

The original source pages could not be independently accessed while preparing this draft. Therefore this document does not claim source-version verification or provide fabricated access dates or section citations. Before substantive reliance or operational use, a qualified reviewer must verify each stage and material claim against the original, applicable sources, record exact sections and access dates as required by the source register, and resolve any mismatch. A citation or this mapping alone does not establish that a method is appropriate or that EpiFlow is validated or authorized.
