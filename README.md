# EpiFlow

## A Human-Led, AI-Assisted Framework for Public Health Outbreak Investigation

> **Project status: Experimental — not validated for operational public health use**

EpiFlow is an open-source framework for exploring how AI-assisted workflows can
support qualified public health professionals during outbreak investigations.

EpiFlow does **not** replace epidemiologists, public health authorities,
laboratory professionals, clinicians, statisticians, or incident commanders.

It does **not** make public health decisions.

The purpose of EpiFlow is to help investigators work more systematically by
supporting activities such as:

- organizing investigation information
- identifying missing information
- documenting assumptions
- checking data quality
- generating reproducible analysis code
- organizing evidence
- maintaining investigation artifacts
- documenting hypotheses
- challenging preliminary interpretations
- supporting literature and guidance review
- preparing draft reports for human review

All consequential epidemiologic interpretations, recommendations, public
communications, and public health actions remain the responsibility of
authorized human professionals.

---

# Why EpiFlow?

AI systems can process large amounts of information quickly and can assist with
research, coding, documentation, data quality review, and repetitive analytical
tasks.

They also have important limitations.

AI systems can:

- produce incorrect information confidently
- invent unsupported facts or citations
- overlook relevant evidence
- misunderstand epidemiologic context
- use inappropriate statistical methods
- confuse association with causation
- fail to recognize bias or confounding
- make incorrect assumptions about missing data
- produce different results from the same general request
- fail silently
- optimize for completing a task rather than protecting public health

These limitations are especially important in outbreak investigations, where
errors can affect human health and public trust.

EpiFlow therefore follows a core principle:

> **AI output is evidence to review, not authority to obey.**

---

# Foundational Principle

EpiFlow separates three responsibilities:

```text
AI
|
|-- organize
|-- search
|-- summarize
|-- generate code
|-- identify possible issues
|-- propose hypotheses
|-- produce drafts
|
v

REPRODUCIBLE TOOLS
|
|-- statistical software
|-- deterministic calculations
|-- validated queries
|-- data-quality checks
|-- tests
|
v

HUMAN EXPERTS
|
|-- interpret evidence
|-- evaluate uncertainty
|-- determine epidemiologic significance
|-- decide whether conclusions are justified
|-- authorize recommendations
|-- make public health decisions
