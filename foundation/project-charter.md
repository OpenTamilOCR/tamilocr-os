---
id: "FND-001"
title: "Project Charter"
type: foundation
version: "2026.07"
revision: 1
status: draft
created: "2026-07-04"
updated: "2026-07-04"
owner: "@founder"
reviewers: []
tier: 0
requires: []
references:
  - "SYS-000"
triggered_by: null
obsoletes: null
source_rfc: null
tags:
  - "foundation"
  - "charter"
  - "mission"
  - "bedrock"
summary: >
  The founding charter of the OpenTamilOCR organization.
  Defines the project's mission, scope, strategic objectives,
  success criteria, organizational responsibilities, and
  governance relationships.
  This is a Tier 0 bedrock document — immutable after ratification.
quality_gate:
  metadata_valid: true
  dependencies_resolved: true
  peer_reviewed: false
  ai_consistency_checked: false
---

# Project Charter

> **FND-001 · 2026.07-r1 · Tier 0 — Bedrock**
>
> The founding charter of the OpenTamilOCR organization.
> This document is immutable after ratification by the Steering Council.
> Changes require a formal RFC, Steering Council approval, and a superseding charter.

---

## 1. Purpose

This charter establishes the OpenTamilOCR organization, defines its mission, authorizes its governance structure, and sets the boundaries within which all organizational activity must operate.

Every repository, document, dataset, model, benchmark, contributor, and AI agent within OpenTamilOCR operates under the authority of this charter.

---

## 2. Authority

This charter is the highest-authority document in TamilOCR OS.

It is a **Tier 0 — Bedrock** document, which means:

- It is immutable after ratification.
- It cannot be amended through normal processes.
- Modification requires a formal RFC (`tamilocr-os://rfcs/`), Steering Council vote, and a superseding charter document.
- All other documents in TamilOCR OS must be consistent with this charter.
- If a conflict exists between this charter and any other document, this charter prevails.

---

## 3. Mission

**Improve an existing open-source OCR framework to become one of the best open-source Tamil OCR projects available.**

OpenTamilOCR does not build an OCR engine from scratch.
We improve an existing framework through better datasets, preprocessing, post-processing, training, benchmarking, documentation, and engineering.

---

## 4. Scope

### 4.1 Version 1 Scope

Version 1 of OpenTamilOCR targets **printed Tamil documents**.

This includes:

- Printed Tamil text in scanned documents, books, and official records.
- Preprocessing pipelines for image cleaning, binarization, and deskewing.
- Post-processing pipelines for error correction and script normalization.
- Training pipelines for improving recognition accuracy on printed Tamil.
- Benchmarking suites for measuring OCR quality against standard datasets.
- Documentation, standards, and contributor infrastructure.

### 4.2 Future Scope

The following are anticipated future extensions, not committed deliverables:

- Handwritten Tamil recognition.
- Mixed Tamil-English documents.
- Scene text recognition (signboards, labels, embedded text in images).
- Historical manuscript OCR.
- Additional Indic language support.

Future scope extensions require a formal RFC and a Vision document update (`tamilocr-os://planning/vision/`).

### 4.3 Language Scope

- **Primary working language:** English.
- **First-class supported script:** Tamil.
- Tamil terms include transliterations on first use throughout all documentation.
- All user-facing tools and outputs must support Tamil Unicode (UTF-8).

---

## 5. Strategic Objectives

| # | Objective | Measured By |
|---|-----------|-------------|
| O1 | Achieve state-of-the-art accuracy on printed Tamil OCR benchmarks. | Character Error Rate (CER) and Word Error Rate (WER) on standardized test sets. |
| O2 | Curate high-quality, openly licensed Tamil OCR datasets. | Dataset volume, annotation accuracy, and diversity metrics. |
| O3 | Build a reproducible, well-documented training and evaluation pipeline. | Pipeline documentation completeness, reproducibility rate. |
| O4 | Establish a contributor-friendly open-source community. | Active contributors, PR merge rate, time-to-first-contribution. |
| O5 | Maintain engineering standards comparable to leading open-source foundations. | Documentation coverage, test coverage, CI pass rate. |
| O6 | Produce AI-native organizational knowledge that any agent can navigate. | AI Memory freshness, knowledge graph completeness. |

---

## 6. Non-Goals

The following are explicitly outside the scope of this project:

| # | Non-Goal | Rationale |
|---|----------|-----------|
| N1 | Building a new OCR engine from scratch. | The mission is to improve an existing framework, not create a competing one. |
| N2 | General-purpose OCR for all languages. | The project focuses on Tamil first. Other languages are future extensions. |
| N3 | Commercial product development. | OpenTamilOCR is an open-source project. Commercial use is permitted by the license but is not a project goal. |
| N4 | Real-time OCR for mobile or embedded devices. | Version 1 targets offline batch processing of scanned documents. |
| N5 | Competing with or replacing existing OCR frameworks. | The project builds on top of an existing framework, complementing rather than replacing it. |

---

## 7. Success Criteria

### 7.1 Version 1 Success

Version 1 is considered successful when all of the following are met:

| # | Criterion |
|---|-----------|
| S1 | A publicly available, openly licensed Tamil OCR dataset exists with at least 10,000 annotated text-line images. |
| S2 | A trained model achieves a CER below 5% on the project's standard printed Tamil test set. |
| S3 | The training pipeline is fully documented and reproducible from a clean environment. |
| S4 | The evaluation benchmark suite produces automated, comparable results. |
| S5 | TamilOCR OS contains all Tier 0–3 documents in approved status. |
| S6 | At least 3 external contributors have successfully submitted merged contributions. |

### 7.2 Long-Term Success

| # | Criterion | Timeframe |
|---|-----------|-----------|
| L1 | CER below 2% on printed Tamil. | 3 years |
| L2 | Handwritten Tamil recognition capability. | 5 years |
| L3 | Active community of 50+ contributors. | 5 years |
| L4 | Adoption by at least one Tamil-language digitization initiative. | 3 years |

---

## 8. Governing Principles

All organizational activity is guided by 10 governing principles.
These principles are defined in SYS-000 and reproduced here as the charter's authoritative copy.

| # | Principle |
|---|-----------|
| P1 | **Single Source of Truth** — TamilOCR OS is the canonical origin of all organizational knowledge. |
| P2 | **Knowledge Graph First** — every document is a node, every cross-reference is an edge. |
| P3 | **AI-Native Design** — any AI agent can understand the project by reading TamilOCR OS. |
| P4 | **OCR Mission Primacy** — everything exists to serve the OCR engine. |
| P5 | **Progressive Complexity** — start simple, add complexity only when earned. |
| P6 | **Reproducibility** — every experiment, benchmark, and training run must be reproducible. |
| P7 | **Language Inclusivity** — English-primary with Tamil as a first-class language. |
| P8 | **Decision Traceability** — every significant choice is recorded with rationale. |
| P9 | **Organizational Resilience** — the project survives changes in personnel and infrastructure. |
| P10 | **Measurable Progress** — organizational health and OCR quality are quantified over time. |

---

## 9. Organizational Structure

### 9.1 Roles

| Role | Responsibility | Initial Holder |
|------|----------------|----------------|
| **Founder** | Charter authority, Steering Council chair, final architectural decisions. | @founder |
| **Steering Council** | Governance oversight, RFC approval, architecture review, release authorization. | Formed when ≥3 maintainers exist. |
| **Maintainers** | Code review, PR merges, standard enforcement, mentoring. | Appointed by Steering Council. |
| **Contributors** | Code, data, documentation, research, testing. | Open to all under DCO. |
| **AI Agents** | Automated documentation, consistency checking, research assistance. | Governed by `tamilocr-os://ai/roles/agent-roles`. |

### 9.2 Decision Authority

| Decision Type | Authority |
|---------------|-----------|
| Bedrock changes (Tier 0) | Steering Council ratification vote |
| Governance changes (Tier 1) | Steering Council approval |
| Architecture changes (Tier 2) | RFC → DEC → Steering Council |
| Standard changes (Tier 3) | RFC → 1 maintainer + Steering Council member |
| Knowledge additions (Tier 4) | 1 maintainer |
| Planning updates (Tier 5) | Steering Council |
| Operational updates (Tier 6) | 1 maintainer |
| Reference updates (Tier 7) | Any contributor |

Until the Steering Council is formed, the Founder holds all decision authority.

---

## 10. Repositories

The organization operates across 10 repositories deployed in three phases.
Full repository descriptions and governance mappings are defined in SYS-000, Section 6.

| Phase | Repositories |
|-------|-------------|
| **1 — Foundation** | `tamilocr-os`, `tamilocr-core`, `tamilocr-datasets`, `tamilocr-community` |
| **2 — Capability** | `tamilocr-benchmarks`, `tamilocr-models`, `tamilocr-training`, `tamilocr-docs-site` |
| **3 — Scale** | `tamilocr-backend`, `tamilocr-playground` |

---

## 11. Licensing

| Artifact Type | License |
|---------------|---------|
| Source code | Apache License 2.0 |
| Trained models | Apache License 2.0 |
| Documentation | Creative Commons Attribution 4.0 International (CC-BY-4.0) |
| Datasets | Creative Commons Attribution 4.0 International (CC-BY-4.0) |

All contributors must agree to the Developer Certificate of Origin (DCO) before contributing.
Licensing policy details are defined in `tamilocr-os://foundation/licensing-policy` (FND-004).

---

## 12. Governance Relationship

This charter authorizes the creation of the governance structure defined in:

- `tamilocr-os://governance/governance-model` (GOV-001)
- `tamilocr-os://governance/business-continuity` (GOV-002)
- `tamilocr-os://governance/decision-process` (GOV-003)
- `tamilocr-os://governance/release-governance` (GOV-004)

The governance documents implement the authority granted by this charter.
They may not exceed, contradict, or diminish the charter's provisions.

---

## 13. Ethics

OpenTamilOCR is committed to ethical AI development.

- OCR systems must not be designed or trained to enable surveillance, censorship, or discrimination.
- Datasets must respect privacy, consent, and intellectual property rights.
- Research and development must consider the impact on Tamil-speaking communities.
- Bias in training data and model outputs must be actively measured and mitigated.

The full ethics framework is defined in `tamilocr-os://foundation/ethics-framework` (FND-003).

---

## 14. Related Documents

| Document | Relationship |
|----------|-------------|
| SYS-000 — Master Index | Parent. This charter is registered under the SYS-000 knowledge graph. |
| FND-002 — Code of Conduct | Sibling. Defines behavioral expectations for contributors. |
| FND-003 — Ethics Framework | Sibling. Expands on the ethics commitments in Section 13. |
| FND-004 — Licensing Policy | Sibling. Expands on the licensing summary in Section 11. |
| GOV-001 — Governance Model | Child. Implements the governance authority granted by Section 12. |

---

## 15. Review Policy

This charter is a Tier 0 bedrock document.

- **Review frequency:** Every 2 years or upon a major organizational change.
- **Amendment process:** Formal RFC → Steering Council ratification vote → superseding document.
- **Minor corrections:** Typographical and formatting corrections may be applied without RFC, but require Steering Council acknowledgment.
- **Supersession:** A new charter supersedes this one via the `obsoletes` frontmatter field. The superseded charter is preserved with `status: superseded`.

---

## 16. Document History

| Version | Date | Summary |
|---------|------|---------|
| 2026.07-r1 | 2026-07-04 | Initial draft. Founding charter for the OpenTamilOCR organization. |

---

> **Ratified by:** Pending Steering Council ratification.
> **Effective date:** Upon ratification.
