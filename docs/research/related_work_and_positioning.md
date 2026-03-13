# Related Work and Positioning

## Purpose

This document positions the **Clinical Reflection Band (CRB)** relative to adjacent classes of clinical systems.

The goal is to clarify what the CRB is, what it is not, and why it should not be read as a variant of ordinary alerting, prediction, or recommendation infrastructure.

---

# Positioning Statement

The CRB is best understood as a **reflective clinical AI architecture**.

It does not primarily evaluate the patient in isolation.

It evaluates the relationship between:

- the patient’s observed physiological evolution
- the expected evolution implied by the clinician’s active interpretive frame

This makes the CRB conceptually different from systems that focus only on deterioration, risk, or treatment optimization.

---

# Comparison with Adjacent System Classes

## 1. Early Warning Scores

Early Warning Scores are designed to detect physiological deterioration using threshold-based or score-based logic.

Typical output:

- alert
- score
- escalation trigger

Their focus is the patient’s current physiological risk.

They do **not** attempt to determine whether the observed evolution is coherent with the clinician’s current interpretive frame.

### Boundary with CRB

An Early Warning Score asks:

- Is this patient deteriorating?

The CRB asks:

- Is this patient evolving in a way that remains coherent with the frame currently guiding care?

These are not the same question.

---

## 2. Predictive Machine Learning Models

Predictive ML systems aim to estimate outcomes such as:

- mortality
- ICU transfer
- sepsis risk
- decompensation probability
- readmission

Typical output:

- probability
- risk score
- prediction

These systems estimate future states of the patient.

They do not primarily evaluate the **stability of the clinician’s active frame**.

### Boundary with CRB

A predictive model asks:

- What is likely to happen?

The CRB asks:

- Is the current frame still coherently explaining what is already happening?

---

## 3. Clinical Decision Support Systems

Clinical Decision Support Systems (CDSS) typically attempt to influence care direction.

Typical functions include:

- suggesting diagnoses
- recommending treatments
- enforcing pathways
- warning against contraindications
- reducing variability in management

These systems participate, directly or indirectly, in the decision space.

### Boundary with CRB

A CDSS asks:

- What should be considered or done?

The CRB asks:

- Does the structure currently organizing interpretation appear to be losing coherence?

The CRB is therefore **reflective**, not directive.

---

## 4. Explainable AI and Governance-Oriented Clinical AI

Recent work in clinical AI has increasingly focused on:

- explainability
- transparency
- accountability
- workflow integration
- uncertainty awareness
- human-in-the-loop oversight

The CRB is compatible with this broader movement.

However, it targets a more specific level of the problem:

- not just whether an output can be explained
- but whether the clinician’s active interpretive frame is remaining stable under real-world pressure

In that sense, the CRB belongs near governance-aware AI, but occupies a distinct conceptual niche.

---

# Comparative Summary

## Early Warning Scores

- **Primary target:** physiological deterioration
- **Typical output:** alarm or score
- **Metacognitive focus:** no

## Predictive ML Models

- **Primary target:** future risk or outcome
- **Typical output:** probability or class
- **Metacognitive focus:** no

## Clinical Decision Support Systems

- **Primary target:** decision optimization
- **Typical output:** recommendation or guidance
- **Metacognitive focus:** no

## Clinical Reflection Band

- **Primary target:** frame stability
- **Typical output:** reflective signal
- **Metacognitive focus:** yes

---

# Why This Positioning Matters

Without this distinction, the CRB can be misread as one of three things:

- a deterioration alert
- an anomaly detector
- a recommendation system with unusual wording

All three readings are wrong.

The conceptual novelty of the CRB depends on preserving one key structure:

> the system monitors divergence between observed physiology and the physiology expected under the clinician’s active interpretive frame.

That is the defining feature of the architecture.

---

# Relationship to Existing Repository Concepts

This positioning is fully consistent with other repository documents, especially:

- boundary discipline
- reflection vs decision support
- signal eligibility
- three-layer mapping
- system model
- system flow

Those documents define the operating boundaries.

This document clarifies the external conceptual neighborhood.

---

# Final Position

The CRB should be understood as a **reflective cognitive safety architecture** for clinical environments under uncertainty and cognitive pressure.

Its purpose is not to provide better answers directly.

Its purpose is to detect when the current interpretive frame may no longer be adequately explaining the case.

That positioning is what distinguishes the CRB from conventional clinical AI categories.
