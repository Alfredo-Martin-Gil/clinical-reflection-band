# System Flow

## Overview

This document describes the conceptual flow of the **Clinical Reflection Band (CRB)** system.

The CRB operates as a **Layer-2 reflective infrastructure** placed above the normal clinical workflow. Its role is not to generate diagnoses or recommendations, but to monitor **coherence between the clinician’s working frame and the evolving patient data**.

The system remains silent by default and emits signals only when **frame instability reaches a meaningful threshold**.

---

# High-Level System Flow

The CRB architecture can be described as a monitoring pipeline.

Clinical Environment  
↓  
Data Streams  
↓  
Frame Construction Model  
↓  
Frame Stability Monitor  
↓  
Reflection Gate  
↓  
Reflective Signal or Silence

---

# Step 1 — Clinical Environment

The process begins inside the clinical workflow itself.

Examples:

- emergency department
- prehospital emergency medicine
- intensive care units
- acute care hospital wards

Clinicians gather information, form hypotheses, and manage the case.

The CRB does not interfere with this workflow.

---

# Step 2 — Data Streams

Multiple categories of signals may feed the reflective layer.

Physiological signals

- heart rate
- blood pressure
- oxygen saturation
- monitoring trends

Clinical narrative signals

- spoken reasoning
- documentation patterns
- hypothesis updates

Workflow signals

- order changes
- repeated reassessment
- escalation patterns

The system observes **patterns and trajectories**, not isolated data points.

---

# Step 3 — Frame Construction Model

The system maintains an approximation of the **current clinical frame**.

A frame includes:

- the assumed clinical explanation
- expected physiological behavior
- anticipated treatment response
- predicted trajectory of the case

The model does not attempt to determine the correct diagnosis.  
It only attempts to infer **the structure of the working frame guiding the clinician’s decisions**.

---

# Step 4 — Frame Stability Monitor

The reflective layer continuously compares:

Expected signals under the current frame

versus

Observed signals from the clinical environment.

Indicators of instability may include:

- unexplained physiological drift
- contradictory signals
- repeated reinterpretation of the same data
- deviation from expected trajectory

The system evaluates **frame coherence**, not diagnostic accuracy.

---

# Step 5 — Reflection Gate

To prevent alert fatigue, all potential signals pass through a strict **reflection gate**.

The gate suppresses signals when:

- instability is minimal
- instability is already obvious
- the clinician is already adapting the frame

The gate allows signals only when:

- frame instability is increasing
- workflow continues under the original frame

---

# Step 6 — Reflective Signal

If the reflection gate activates, the CRB emits a **minimal reflective signal**.

Examples of signal formats:

- subtle vibration on a wearable device
- visual indicator
- neutral message

Example message:

Frame instability detected

The signal contains **no interpretation, no diagnosis, and no recommendation**.

---

# Silence as Default Behavior

The CRB is designed to remain silent most of the time.

Frequent signals would degrade trust and increase cognitive burden.

The system should therefore operate as a **background reflective layer** rather than an alerting system.

---

# Authority Boundary

The CRB never replaces the clinician’s authority.

The system:

- does not block clinical actions
- does not enforce protocols
- does not override decisions

Its role is limited to **highlighting potential instability in the current reasoning frame**.

---

# Conceptual Status

The CRB flow described here represents a **conceptual architecture** intended for exploration and discussion.

No implementation is currently included in this repository.
