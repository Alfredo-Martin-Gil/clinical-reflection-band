# Clinical Reflection Band (CRB)

## A research concept for reflective clinical AI

The **Clinical Reflection Band (CRB)** is a conceptual architecture and research proposal about a narrow clinical-AI question:

> Could a non-directive system surface when the interpretive frame guiding care appears to be losing coherence with the patient's observed trajectory?

CRB explores *epistemic tension*: possible divergence between an inferred active clinical frame, the trajectory expected under that frame, and the trajectory observed in the available data. The proposed response is a minimal cue for human reassessment—not a diagnosis, prediction, treatment recommendation, or safety assurance.

> [!IMPORTANT]
> **Current evidence status:** concept only. This repository contains no executable implementation, trained model, clinical dataset, benchmark result, human-factors study, clinical validation, deployment, or medical-device evidence. The equations, stages, signals, and metrics are proposed design objects, not implemented capabilities.

## Why the concept matters

In time-pressured care, an initial interpretation may remain plausible while new observations become progressively less compatible with it. This repository calls that proposed failure pattern **case drift**. Whether case drift can be operationalized, detected, and surfaced usefully remains an open research question.

The concept is grounded in clinical workflow analysis from emergency and prehospital practice. That clinical grounding motivates the research problem; it does not constitute validation of the proposed architecture.

## Proposed architecture

CRB separates three boundaries:

1. **Interaction** — a minimal, non-directive cue, with silence as the default output.
2. **Reflection** — a proposed comparison between inferred frame-conditioned expectations and observed evolution.
3. **Clinical authority** — interpretation, reassessment, action, and responsibility remain human.

A conceptual operational pipeline is described in five stages:

1. acquisition of available physiological, narrative, and workflow signals;
2. probabilistic inference of the active clinical frame;
3. generation of a frame-conditioned expected trajectory;
4. comparison with the observed trajectory under data-quality constraints;
5. a reflection gate that either remains silent or permits a minimal cue.

None of these stages is implemented in this repository.

## Conceptual formalism

The proposed **Epistemic Tension Index** is represented as:

$$
\sigma(t) = \int_{t-\Delta t}^{t} q(\tau)\,\lambda(\tau)\,D\big(S_{exp}(F,\tau),\,S_{obs}(\tau)\big)\,d\tau
$$

Where:

- $F$ is an inferred active clinical frame;
- $S_{exp}$ is an expected trajectory conditioned on that frame;
- $S_{obs}$ is the observed trajectory;
- $D$ is an unspecified divergence function;
- $q$ represents data-quality constraints;
- $\lambda$ represents temporal weighting.

This is a **conceptual expression**, not an implemented or calibrated score. The repository does not establish that the proposed variables can be inferred reliably or that $\sigma$ has clinical validity.

## Safety and authority boundaries

CRB is not presented as:

- a clinical decision-support system;
- a diagnostic, triage, deterioration, or risk-prediction system;
- a treatment recommender;
- a validated clinical AI system;
- a safety layer with demonstrated risk reduction;
- a deployable product, wearable, or medical device;
- a system suitable for patient care.

Silence must never be interpreted as reassurance, validation of the current frame, absence of risk, or adequate data quality. A future implementation could miss meaningful tension, signal unnecessarily, distort clinician attention, or cause authority and vigilance to migrate toward the system.

## Research path—not current evidence

The repository proposes a staged path that would need to begin before any clinical-use claim could be considered:

1. formal definitions and falsifiable hypotheses;
2. retrospective feasibility work with appropriate governance;
3. error analysis, including false silence and signal burden;
4. simulation and human-factors evaluation;
5. silent or shadow-mode evaluation;
6. regulatory, privacy, safety, and implementation assessment before any prospective signalling.

See [Validation Strategy](docs/research/validation_strategy.md). This path is a proposal; no stage is reported as completed here.

## Start here

| Need | Document |
|---|---|
| Scope and non-claims | [Project scope](docs/core/PROJECT_SCOPE.md) |
| Evidence inventory | [Evidence and maturity status](docs/EVIDENCE_AND_MATURITY.md) |
| Boundaries and limitations | [Limitations](docs/core/LIMITATIONS.md) |
| Conceptual architecture | [System model](docs/core/system_model.md) and [system flow](docs/core/system_flow.md) |
| Failure analysis | [Failure modes](docs/concepts/failure_modes.md) |
| Research questions | [Research questions](docs/research/research_questions_and_contributions.md) |
| Proposed evaluation path | [Validation strategy](docs/research/validation_strategy.md) |
| Portfolio role | [Portfolio connection](docs/PORTFOLIO_CONNECTION.md) |
| Companion manuscript | [`paper/Paper V8 eng.pdf`](paper/Paper%20V8%20eng.pdf) |

The complete documentation map is available in [`docs/README.md`](docs/README.md).

## Reproducibility statement

There is currently no executable analysis to reproduce. A reader can audit conceptual consistency by tracing the scope, system model, failure modes, proposed research questions, and validation path through the documents above. Any future code, data, experiment, or result should be versioned separately with provenance, environment instructions, tests, and an explicit evidence label.

## Role in the Clinical AI portfolio

CRB is the **research-concept** component of a three-project narrative:

- [`clinical-nlp-triage-open-source`](https://github.com/Alfredo-Martin-Gil/clinical-nlp-triage-open-source) — an applied, auditable research prototype using synthetic data;
- **Clinical Reflection Band** — a conceptual exploration of human oversight, cognitive failure modes, signal restraint, and authority boundaries;
- [`prehospital-clinical-decision-uncertainty`](https://github.com/Alfredo-Martin-Gil/prehospital-clinical-decision-uncertainty) — the clinical-operational foundation for reasoning under uncertainty in prehospital workflows.

Together they connect prototype evaluation, human-factors and governance questions, and frontline workflow analysis. They do not represent clinical implementation or validation.

## Professional description

> **Clinical Reflection Band is a research-stage conceptual architecture exploring whether non-directive AI cues could surface tension between a clinician's active interpretive frame and a patient's observed trajectory. It demonstrates clinical workflow analysis, human-oversight design, failure-mode reasoning, and a staged validation proposal; it does not contain an implemented or clinically validated system.**

## Licence

See [`LICENSE`](LICENSE).
