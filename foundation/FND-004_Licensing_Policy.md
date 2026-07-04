---
id: "FND-004"
title: "Licensing Policy"
type: foundation
version: "2026.07"
revision: 1
status: draft
created: "2026-07-04"
updated: "2026-07-04"
owner: "@founder"
reviewers: []
tier: 0
requires:
  - "FND-001"
references:
  - "SYS-000"
  - "FND-003"
triggered_by: null
obsoletes: null
source_rfc: null
tags:
  - "foundation"
  - "licensing"
  - "legal"
  - "bedrock"
summary: >
  The official licensing policy for the OpenTamilOCR organization.
  Defines the licensing strategy for source code, documentation, datasets,
  trained models, third-party dependencies, contributor submissions, and
  organizational assets across the entire ecosystem.
  This is a Tier 0 bedrock document — immutable after ratification.
quality_gate:
  metadata_valid: true
  dependencies_resolved: true
  peer_reviewed: false
  ai_consistency_checked: false
---

# FND-004 — Licensing Policy

> **FND-004 · 2026.07-r1 · Tier 0 — Bedrock**
>
> The official licensing policy for the OpenTamilOCR organization.
> This document is immutable after ratification by the Steering Council.
> Changes require a formal RFC, Steering Council approval, and a superseding document.

---

## 1. Purpose

This document defines how intellectual property is licensed across the entire OpenTamilOCR ecosystem — from source code and trained models to documentation, datasets, and organizational assets.

It ensures that:

- Every artifact has a clear, unambiguous license.
- Contributors understand their rights and obligations before contributing.
- Downstream users can confidently use, modify, and redistribute project outputs.
- The project's open-source mission (FND-001, Section 3) is permanently protected.
- Third-party dependencies are compatible with the project's licensing strategy.

This policy is not legal advice.
Contributors with legal questions should consult their own legal counsel.

---

## 2. Scope

This policy covers all artifacts produced, curated, or distributed by the OpenTamilOCR organization:

- Source code across all repositories.
- Documentation in TamilOCR OS and all other repositories.
- Datasets collected, curated, annotated, or synthesized by the project.
- Trained models, weights, and checkpoints.
- Benchmark suites and evaluation scripts.
- Schemas, templates, configuration files, and scripts.
- AI-generated content produced by project AI agents.
- Organizational assets (logos, branding, website content).
- Third-party dependencies included in or required by project artifacts.

---

## 3. Licensing Philosophy

### 3.1 Principles

OpenTamilOCR's licensing strategy is governed by four principles:

| # | Principle | Rationale |
|---|-----------|-----------|
| L1 | **Maximize openness.** | The project exists to serve the public. Permissive licenses maximize the number of people and organizations that can benefit. |
| L2 | **Protect contributors.** | Contributors must receive explicit patent protection and clear attribution rights. |
| L3 | **Enable commercial use.** | Commercial adoption increases impact. The project does not restrict commercial use, even though commercial development is not a project goal (FND-001, Section 6, N3). |
| L4 | **Minimize license complexity.** | The project uses exactly two licenses for its own artifacts. This reduces contributor confusion and downstream compliance burden. |

### 3.2 License Selection Rationale

| License | Applied To | Why Selected |
|---------|-----------|--------------|
| **Apache License 2.0** | Source code, trained models | Permissive. Includes explicit patent grant protecting users and contributors. Compatible with most open-source licenses. Industry-standard for ML projects. |
| **CC-BY-4.0** | Documentation, datasets | Purpose-built for non-software creative works. Requires attribution, which ensures the project and its contributors receive credit. Compatible with academic and institutional use. |

This dual-license strategy is locked as architectural decision D5 (SYS-000, Section 12).

---

## 4. License Assignments

### 4.1 Repository Licensing Matrix

| Repository | Primary License | Applies To |
|------------|----------------|------------|
| `tamilocr-os` | CC-BY-4.0 | Documentation, YAML, templates. Apache 2.0 for Python scripts. |
| `tamilocr-core` | Apache 2.0 | All source code, configuration, and scripts. |
| `tamilocr-datasets` | CC-BY-4.0 | Dataset files, annotations, and metadata. Apache 2.0 for tooling scripts. |
| `tamilocr-community` | CC-BY-4.0 | Meeting notes, governance discussions, RFC mirrors. |
| `tamilocr-benchmarks` | Apache 2.0 | Evaluation scripts and tooling. CC-BY-4.0 for benchmark result reports. |
| `tamilocr-models` | Apache 2.0 | Model weights, checkpoints, and serving code. CC-BY-4.0 for model cards. |
| `tamilocr-training` | Apache 2.0 | Training pipeline code and configuration. |
| `tamilocr-docs-site` | Apache 2.0 | Website source code. CC-BY-4.0 for rendered content. |
| `tamilocr-backend` | Apache 2.0 | API source code and configuration. |
| `tamilocr-playground` | Apache 2.0 | Application source code. |

### 4.2 Mixed-License Repositories

Some repositories contain artifacts under both licenses.
When this occurs:

- The repository root `LICENSE` file contains the primary license.
- A `LICENSE-DOCS` or `LICENSE-DATA` file contains the secondary license.
- Individual directories may include a `LICENSE` file clarifying which license applies.
- The repository `README.md` explicitly states the licensing split.
- File headers indicate the applicable license where ambiguity could arise.

---

## 5. Code Licensing

### 5.1 License

All source code is licensed under the **Apache License 2.0**.

The full license text is included in the `LICENSE` file at the root of every code repository.

### 5.2 File Headers

Every source code file should include a license header.

**Python example:**

```python
# Copyright 2026 The OpenTamilOCR Authors
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
```

### 5.3 Configuration Files

Configuration files (YAML, JSON, TOML) that are integral to source code functionality are covered by Apache 2.0.
Standalone data files in YAML or JSON format that represent documentation or dataset metadata are covered by CC-BY-4.0.

---

## 6. Documentation Licensing

### 6.1 License

All documentation is licensed under **Creative Commons Attribution 4.0 International (CC-BY-4.0)**.

This includes:

- All markdown documents in TamilOCR OS.
- All documents in the `tamilocr-community` repository.
- Model cards and dataset cards.
- Research notes, education materials, and experiment reports.
- Rendered website content on the documentation site.
- Schemas (`.schema.json`) are considered documentation infrastructure and are covered by CC-BY-4.0.

### 6.2 Attribution Requirements

Users who redistribute or adapt OpenTamilOCR documentation must:

- Credit "The OpenTamilOCR Authors" or the specific author(s).
- Provide a link to the original document or the project repository.
- Indicate if changes were made.
- Not imply endorsement by OpenTamilOCR.

### 6.3 AI-Generated Documentation

Documentation produced by AI agents operating within OpenTamilOCR is treated identically to human-authored documentation.

- It is licensed under CC-BY-4.0.
- It is attributed to "The OpenTamilOCR Authors."
- It is subject to the same quality gates and review processes.
- The use of AI in generating content is disclosed in the document's metadata or contribution history.

---

## 7. Dataset Licensing

### 7.1 License

All datasets produced by OpenTamilOCR are licensed under **CC-BY-4.0**.

### 7.2 Dataset Cards

Every released dataset must include a dataset card conforming to SCH-003 (`tamilocr-os://schemas/dataset-card`) that specifies:

- The license under which the dataset is released.
- The provenance of every data source.
- Any third-party license obligations inherited from source materials.
- Any restrictions on use imposed by source licenses.

### 7.3 Third-Party Data

When third-party data is incorporated into project datasets:

| Source License | Compatibility | Action Required |
|---------------|---------------|-----------------|
| Public domain | Compatible | Document source. No additional obligations. |
| CC0 | Compatible | Document source. No additional obligations. |
| CC-BY (any version) | Compatible | Provide attribution as required by the source license. |
| CC-BY-SA | Partially compatible | Share-alike obligation applies to derivatives. Must be documented. Isolate if possible. |
| CC-BY-NC | Incompatible | Cannot be included in project datasets. Non-commercial restriction conflicts with open-access philosophy. |
| CC-BY-ND | Incompatible | Cannot be included. No-derivatives restriction prevents annotation and preprocessing. |
| Custom/Unknown | Requires review | Must be reviewed by a maintainer before inclusion. Document the license terms. |

### 7.4 Synthetic Data

Synthetic data generated by the project is licensed under CC-BY-4.0.
The fonts, templates, and generation scripts used must themselves be compatibly licensed.
The generation method and source assets are documented in the dataset card.

---

## 8. Model Licensing

### 8.1 License

All trained models (weights, checkpoints, architectures) produced by OpenTamilOCR are licensed under **Apache 2.0**.

### 8.2 Model Cards

Every released model must include a model card conforming to SCH-002 (`tamilocr-os://schemas/model-card`) that specifies:

- The license under which the model is released.
- The training data used and its license.
- The base framework and its license.
- Any inherited license obligations.

### 8.3 Base Framework License

The base OCR framework that OpenTamilOCR improves must be licensed under a compatible open-source license.
Compatibility with Apache 2.0 is a mandatory criterion for framework selection (DEC-001).

### 8.4 Fine-Tuned Models

Models fine-tuned from third-party pretrained weights inherit the license obligations of the original weights.
If the original weights use a license more restrictive than Apache 2.0, this must be documented in the model card and the release must comply with the more restrictive terms.

---

## 9. Third-Party Dependencies

### 9.1 Compatibility Policy

All third-party dependencies must have licenses compatible with Apache 2.0.

**Compatible licenses include:**

- Apache 2.0
- MIT
- BSD (2-clause, 3-clause)
- ISC
- Python Software Foundation License
- Unlicense / Public Domain

**Incompatible licenses include:**

- GPL (v2, v3) — copyleft obligation conflicts with Apache 2.0 distribution.
- AGPL — network copyleft obligation conflicts with project distribution model.
- SSPL — not an open-source license by OSI definition.
- Proprietary — incompatible with open-source mission.
- CC-BY-NC — non-commercial restriction conflicts with open-access philosophy.

**Special cases:**

- LGPL — permitted for dynamically linked libraries only. Must not be statically linked.
- MPL 2.0 — permitted. File-level copyleft is manageable with proper isolation.

### 9.2 Dependency Review

- New dependencies must be reviewed for license compatibility before inclusion.
- The tool inventory (`tamilocr-os://references/tool-inventory`, REF-003) tracks all dependencies with their licenses.
- CI pipelines should include automated license scanning where feasible.
- Dependencies with ambiguous or missing licenses must not be used until their license status is clarified.

### 9.3 Transitive Dependencies

License compatibility requirements apply transitively.
If dependency A is MIT-licensed but depends on B which is GPL-licensed, the GPL obligation propagates.
Dependency trees must be reviewed, not just direct dependencies.

---

## 10. Contributor Rights and Obligations

### 10.1 Developer Certificate of Origin (DCO)

OpenTamilOCR uses the **Developer Certificate of Origin (DCO)** instead of a Contributor License Agreement (CLA).

The DCO is a lightweight mechanism that confirms:

- The contributor has the right to submit the contribution.
- The contribution is made under the project's applicable license.
- The contributor understands the contribution will be publicly available.

Contributors signify agreement by adding a `Signed-off-by` line to their commit messages:

```
Signed-off-by: Name <email@example.com>
```

This is enforced by CI (using tools such as the DCO GitHub App).

### 10.2 Why DCO Instead of CLA

| Factor | CLA | DCO |
|--------|-----|-----|
| Legal complexity | High — requires legal review and often a signed agreement. | Low — a certification included in the commit message. |
| Contributor friction | High — deters casual contributors. | Low — no separate agreement to sign. |
| Corporate compatibility | Requires corporate CLA for employed contributors. | Commits from employed contributors are covered by the signoff. |
| IP assignment | Often transfers IP to the project or foundation. | No IP transfer. Contributors retain copyright. |
| Community standard | Used by some foundations (Apache, Google). | Used by Linux kernel, Git, many CNCF projects. |

The DCO aligns with the project's principle of progressive complexity (P5, FND-001) and minimizes barriers to contribution.

### 10.3 Copyright Ownership

- Contributors retain copyright over their contributions.
- Copyright is attributed to "The OpenTamilOCR Authors" collectively in file headers and license notices.
- No individual or organization claims exclusive copyright over the project.
- This collective attribution model follows the practice used by Kubernetes, TensorFlow, and other major open-source projects.

### 10.4 Contribution License

- Code contributions are licensed under Apache 2.0.
- Documentation contributions are licensed under CC-BY-4.0.
- Dataset contributions are licensed under CC-BY-4.0.
- By submitting a contribution with a DCO signoff, the contributor certifies that the contribution is made under the applicable license.

---

## 11. Patents

### 11.1 Apache 2.0 Patent Grant

The Apache License 2.0 includes an explicit patent grant:

- Every contributor grants a perpetual, worldwide, non-exclusive, royalty-free patent license for their contributions.
- This grant covers the contribution itself and its combination with the project as it existed at the time of contribution.
- The grant terminates automatically if the licensee initiates patent litigation against the project.

### 11.2 Patent Policy

- OpenTamilOCR does not file patents.
- The project relies on the defensive patent provisions of Apache 2.0.
- Contributors must not knowingly contribute code that infringes third-party patents.
- If a patent concern is identified, it must be reported to the Steering Council.

---

## 12. Trademarks

### 12.1 Project Marks

The following are trademarks of the OpenTamilOCR project:

- The name "OpenTamilOCR."
- The project logo (when designed).
- The names of project repositories (e.g., "tamilocr-core", "tamilocr-os").

### 12.2 Usage Policy

- Trademarks are not covered by Apache 2.0 or CC-BY-4.0.
- Use of project trademarks to identify the project or attribute work is permitted.
- Use of project trademarks to imply endorsement, affiliation, or sponsorship without authorization is prohibited.
- Modified versions of the project must not use the OpenTamilOCR name or logo without permission.
- Formal trademark guidelines will be published if the project reaches a scale where trademark protection becomes necessary.

---

## 13. Distribution

### 13.1 Distribution Rights

All project artifacts may be freely:

- Used for any purpose, including commercial use.
- Modified and adapted.
- Redistributed in original or modified form.

Subject to the terms of the applicable license (Apache 2.0 or CC-BY-4.0).

### 13.2 Attribution in Distribution

- Redistributions of code must include the `LICENSE` file and copyright notices.
- Redistributions of documentation must provide attribution as specified in Section 6.2.
- Redistributions of datasets must include the dataset card and license file.
- Redistributions of models must include the model card and license file.

### 13.3 No Warranty

All project artifacts are provided "as is" without warranty of any kind.
The Apache 2.0 and CC-BY-4.0 licenses both disclaim warranties.
This disclaimer is not optional and must not be removed from distributed artifacts.

---

## 14. Licensing Governance

### 14.1 License Change Process

Changes to the project's licensing strategy are architectural-level decisions.

- A license change requires a formal RFC.
- The RFC must demonstrate that the change serves the project's mission and principles.
- Steering Council approval is required.
- The decision is recorded as a DEC-NNN record.
- Existing artifacts retain their original license. New artifacts adopt the new license.

### 14.2 License Compliance

- Maintainers are responsible for verifying license compliance in code reviews.
- CI pipelines should include automated license scanning for dependencies.
- License violations discovered in project artifacts must be remediated promptly.
- License violations reported by third parties are handled by the Steering Council.

### 14.3 Future Considerations

- If a project foundation is established, copyright assignment or a CLA may be reconsidered through the RFC process.
- If the project adopts additional artifact types (mobile apps, browser extensions), their licensing will be determined through the RFC process.
- The default assumption for any new artifact type is Apache 2.0 for executable artifacts and CC-BY-4.0 for content artifacts.

---

## 15. Governance Relationship

This policy is authorized by the Project Charter (FND-001, Sections 11 and 12).

| Document | Relationship |
|----------|-------------|
| FND-001 — Project Charter | Parent. Defines the licensing commitment in Section 11 and grants authority for this policy. |
| FND-003 — Ethics Framework | Sibling. Section 5.4 references this policy for dataset licensing obligations. |
| GOV-004 — Release Governance | Downstream. Release processes must verify license compliance before publication. |
| STD-003 — Dataset Standards | Downstream. Implements dataset licensing requirements from Section 7. |
| STD-004 — Model Standards | Downstream. Implements model licensing requirements from Section 8. |
| REF-003 — Tool Inventory | Downstream. Tracks third-party dependencies with their licenses per Section 9. |

---

## 16. Related Documents

| Document | Relationship |
|----------|-------------|
| SYS-000 — Master Index | Root. This document is registered under the SYS-000 knowledge graph. |
| FND-001 — Project Charter | Required. Grants authority and defines the licensing commitment. |
| FND-003 — Ethics Framework | Reference. Defines ethical obligations for data and model licensing. |
| GOV-004 — Release Governance | Reference. Release process enforces licensing compliance. |

---

## 17. Review Policy

This policy is a Tier 0 bedrock document.

- **Review frequency:** Every 2 years or upon a significant licensing event (foundation formation, major partnership, license dispute).
- **Amendment process:** Formal RFC → Steering Council ratification vote → superseding document.
- **Minor corrections:** Typographical corrections may be applied without RFC, but require Steering Council acknowledgment.
- **Dependency license table updates:** Updates to the compatibility table (Section 9.1) are operational corrections that do not require an RFC, but do require maintainer review.

---

## 18. Document History

| Version | Date | Summary |
|---------|------|---------|
| 2026.07-r1 | 2026-07-04 | Initial draft. Founding licensing policy for the OpenTamilOCR organization. |

---

> **Ratified by:** Pending Steering Council ratification.
> **Effective date:** Upon ratification.
