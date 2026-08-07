# Evidence and Maturity Status

## Purpose

This inventory distinguishes what is present in the Clinical Reflection Band (CRB) repository from what is proposed for future research. It is intended to prevent architectural descriptions from being read as implemented capabilities.

## Current classification

- **Asset type:** research concept / conceptual architecture
- **Evidence level:** design rationale and research proposal
- **Clinical-use status:** not for clinical use
- **Implementation status:** no executable implementation
- **Validation status:** no technical, clinical, or human-factors validation reported
- **Deployment status:** no deployment reported
- **Regulatory status:** no medical-device or regulatory claim

## Evidence inventory

| Artifact | Present | What it supports | What it does not support |
|---|---:|---|---|
| Conceptual architecture | Yes | A structured design hypothesis | Technical feasibility or clinical benefit |
| Clinical workflow rationale | Yes | Motivation from emergency and prehospital contexts | Generalizability or outcome improvement |
| Mathematical notation for $\sigma$ | Yes | A proposed relationship among conceptual variables | An implemented, calibrated, or validated score |
| Failure-mode analysis | Yes | Anticipated human-factors and authority risks | Evidence that the risks are controlled |
| Proposed validation strategy | Yes | A staged research plan | Completion of any validation stage |
| Companion manuscript PDF | Yes | A longer exposition of the concept | Peer-review status, clinical validation, or implementation |
| Source code or executable prototype | No | — | Implemented capability |
| Model weights or algorithm | No | — | Model performance |
| Dataset or benchmark output | No | — | Reproducible empirical results |
| Clinical or simulation study | No | — | Safety, usability, effectiveness, or workflow benefit |
| QMS or regulatory dossier | No | — | Compliance or regulatory readiness |

## Permitted descriptions

The project may be described as:

- a research-stage conceptual architecture;
- a structured research proposal for reflective clinical AI;
- an exploration of human oversight, signal restraint, and clinical authority boundaries;
- a clinically grounded design and failure-mode analysis;
- a proposed staged validation pathway.

## Descriptions not supported by this repository

The project must not be described as:

- implemented, deployed, production-ready, or clinically integrated;
- validated clinical AI;
- a safe clinical system or demonstrated cognitive safety layer;
- a system that detects case drift, prevents error, reduces risk, or improves outcomes;
- a medical device, regulatory-ready product, or compliant system;
- a completed study or proven novel clinical-AI category.

## Evidence needed for maturity progression

Progression beyond concept status would require, at minimum:

1. operational definitions and falsifiable hypotheses;
2. an auditable prototype with versioned logic and tests;
3. appropriate data provenance and governance;
4. prespecified technical evaluation and error analysis;
5. human-factors evaluation of signal interpretation, burden, and authority migration;
6. safety, privacy, workflow, and regulatory assessment matched to the intended context of use;
7. external review and transparent reporting of negative as well as positive findings.

No item in this list is claimed as completed by the current repository.
