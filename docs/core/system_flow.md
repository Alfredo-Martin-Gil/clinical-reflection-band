# System Flow

## Overview

This document describes the conceptual operating flow of the **Clinical Reflection Band (CRB)**.

The CRB functions as a **reflective Layer-2 infrastructure** operating alongside normal clinical workflow. Its role is not to generate diagnoses, treatment recommendations, or risk classifications, but to monitor whether the **active clinical frame** continues to remain coherent with the patient’s evolving physiological trajectory.

The system is designed to remain **silent by default** and emit a reflective signal only when epistemic tension becomes clinically meaningful.

---

# High-Level Flow

The CRB can be described as a five-stage reflective pipeline:

Clinical Environment  
↓  
Multimodal Data Acquisition  
↓  
Probabilistic Frame Inference  
↓  
Expected Trajectory Generation  
↓  
Frame-Conditioned Divergence Monitoring  
↓  
Reflection Gate  
↓  
Reflective Signal or Silence

---

# Stage 1 — Clinical Environment

The process begins inside the real clinical workflow.

Examples include:

- emergency departments
- prehospital emergency medicine
- intensive care units
- acute care hospital wards

Clinicians gather information, construct hypotheses, order tests, initiate treatment, and update management plans.

The CRB does not control this process.

It observes it.

---

# Stage 2 — Multimodal Data Acquisition

The reflective layer receives signals already generated during patient care.

## Physiological signals

- heart rate
- blood pressure
- respiratory rate
- oxygen saturation
- ETCO₂
- monitoring trends

## Contextual and narrative signals

- triage notes
- handoff documentation
- progress notes
- structured EHR entries
- spoken clinical reasoning when available

## Workflow and action signals

- CPOE activity
- medication choices
- procedural actions
- escalation patterns
- timing and rhythm of reassessment

The CRB is therefore not dependent on a single modality.

It relies on the convergence of multiple weak but meaningful signals.

---

# Stage 3 — Probabilistic Frame Inference

The system estimates the **active clinical frame** currently guiding care.

A clinical frame may include:

- the assumed explanation of the case
- expected physiological behavior
- anticipated response to intervention
- the logic underlying current workflow continuity

This frame is not entered manually.

It is inferred passively from multimodal evidence such as:

- language in notes
- order-entry semantics
- intervention patterns
- repeated references in handoffs
- treatment pathways already activated

The output of this stage is an operational estimate of the active frame:

**F**

This estimate may remain probabilistic rather than fully resolved.

---

# Stage 4 — Expected Trajectory Generation

Once frame **F** is estimated, the system derives the physiological trajectory that would be expected if that frame remained valid.

This expected trajectory can be represented conceptually as:

**S_exp(F)**

Examples:

- if the active frame implies septic shock, certain intervention-response patterns become more plausible
- if the active frame implies bronchospasm, different response trajectories become expected
- if the active frame implies uncomplicated pain without systemic compromise, ongoing physiological drift may become harder to reconcile

The purpose of this stage is not to create a full physiological simulator.

The purpose is to establish what kind of evolution would remain coherent under the current frame.

---

# Stage 5 — Divergence Monitoring

The reflective layer compares:

- **S_exp(F)** = expected physiological trajectory under the active frame
- **S_obs** = observed physiological trajectory

This comparison is performed over time rather than as an isolated snapshot.

Potential indicators of divergence include:

- unexplained physiological drift
- contradictory response to treatment
- repeated local reinterpretation without frame revision
- growing mismatch between expected and actual evolution

This produces a dynamic estimate of **epistemic tension**.

Important boundary:

> the system is not asking whether the patient is deteriorating in general;  
> it is asking whether the patient is evolving in a way that remains coherent with the frame currently organizing clinical action.

---

# Stage 6 — Reflection Gate

Not every divergence event should generate a signal.

To prevent alert fatigue and preserve trust, all candidate signals pass through a **reflection gate**.

The gate suppresses signaling when:

- divergence is weak
- data quality is poor
- mismatch is already obvious to the clinician
- the team has already begun adapting the frame
- signaling would add noise rather than value

The gate allows signaling only when:

- epistemic tension is increasing
- the original frame still appears to be governing workflow
- the mismatch is not yet fully integrated into decision-making
- the signal is likely to support reassessment without distraction

---

# Stage 7 — Reflective Signal

If the reflection gate activates, the CRB emits a **minimal reflective signal**.

Possible signal formats:

- subtle wearable vibration
- ambient visual marker
- neutral short message in the interface

Examples of acceptable signal language:

- **FRAME UNDER EPISTEMIC TENSION**
- **COHERENCE GAP DETECTED**
- **TRAJECTORY-FRAME DIVERGENCE RISING**

The signal must contain:

- no diagnosis
- no recommendation
- no suggested action
- no forced interpretation

Its function is to trigger **reassessment**.

---

# Silence as Default Behavior

The CRB should remain silent most of the time.

Silence is not an absence of function.

It is an intentional safety property.

Frequent signaling would collapse the distinction between reflective infrastructure and ordinary alerting systems.

For this reason, silence is the default operating mode.

---

# Authority Boundary

The CRB never replaces the clinician’s authority.

The system:

- does not block actions
- does not enforce protocols
- does not assign diagnoses
- does not suggest treatments
- does not convert uncertainty into direction

Its role is limited to indicating that the **current frame may be losing coherence with the patient’s observed evolution**.

---

# Flow Summary

The operating logic of the CRB can be summarized as:

1. observe clinical and physiological data
2. infer the active frame
3. generate the trajectory expected under that frame
4. compare expected and observed evolution
5. estimate epistemic tension
6. suppress or permit signaling through the reflection gate
7. emit a minimal reflective cue only when justified

---

# Conceptual Status

The flow described here represents a **conceptual research architecture**.

It is intended to clarify the operating logic of the CRB and align the repository with the broader reflective AI framework.

No deployable implementation is currently included in this repository.
