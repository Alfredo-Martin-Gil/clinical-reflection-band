# System Model

## Purpose

The **Clinical Reflection Band (CRB)** is a conceptual **reflective AI architecture** designed to monitor the stability of the clinician’s active interpretive frame during patient care.

The system does not generate diagnoses, treatment recommendations, or automated management decisions.

Its function is limited to detecting **loss of coherence between the clinical frame currently guiding care and the patient’s evolving physiological trajectory**.

When such loss of coherence becomes meaningful under acceptable signal conditions, the CRB may emit a **minimal reflective signal**.

---

# Core Concept

The CRB is based on a simple premise:

> a case can remain clinically plausible while the frame guiding interpretation progressively loses coherence with the patient’s observed physiological evolution.

This condition is referred to as **Case Drift**.

The system is therefore not designed to answer:

- What is the diagnosis?
- What treatment should be given?
- What action is recommended next?

It is designed to ask a different question:

- Is the current interpretive frame still coherently explaining the case?

---

# What the System Monitors

The CRB does not monitor deterioration in the ordinary sense.

It monitors **epistemic tension**.

That means it evaluates the divergence between:

1. the **expected physiological trajectory** implied by the inferred active clinical frame, and
2. the **observed physiological trajectory** of the patient.

This distinction matters.

A patient may deteriorate without epistemic tension if the deterioration is expected under the current frame.

Conversely, epistemic tension may rise before overt deterioration becomes obvious if observed evolution is no longer matching what the active frame would predict.

---

# Architectural Interpretation

The CRB can be understood through two complementary architectural descriptions.

## A. Boundary Architecture — Three Layers

### Layer 1 — Interaction

This layer defines how a reflective signal reaches the clinician.

Possible formats include:

- wearable haptic cue
- ambient visual marker
- EHR-integrated neutral indicator

The signal must remain minimal and non-directive.

### Layer 2 — Reflection

This is the core reflective layer.

It:

- infers the active clinical frame
- generates expected trajectory models conditioned on that frame
- compares expected and observed physiological evolution
- computes epistemic tension
- determines whether a reflective signal is warranted

### Layer 3 — Clinical Authority

The clinician remains the sole decision authority.

The CRB never:

- issues diagnostic statements
- proposes treatments
- blocks workflow
- overrides decisions

---

## B. Operational Architecture — Five Stages

### Stage 1 — Multimodal Data Acquisition

The reflective layer observes signals already generated during care, such as:

- vital signs
- monitoring trends
- laboratory updates
- documentation
- order-entry activity
- intervention patterns
- spoken reasoning when available

### Stage 2 — Probabilistic Frame Inference

The system infers the active clinical frame **F** from multimodal contextual evidence.

The objective is not certainty, but an operational estimate of the frame currently structuring care.

### Stage 3 — Expected Trajectory Generation

Given inferred frame **F**, the system generates the **expected physiological trajectory**:

**S_exp(F)**

This represents the trajectory that would be coherent with the current frame if the frame remained valid.

### Stage 4 — Divergence Monitoring

The system continuously compares:

- **S_exp(F)** = expected physiological trajectory under the active frame
- **S_obs** = observed physiological trajectory

This comparison is weighted by time, context, and signal quality.

### Stage 5 — Reflective Signal Emission

If divergence exceeds calibrated thresholds and workflow inertia persists, the system may emit a **minimal reflective signal**.

The default state remains **silence**.

---

# Formal Model

## Conceptual Variables

- **F** = inferred active clinical frame
- **S_exp(F,t)** = expected physiological trajectory at time **t**, conditioned on frame **F**
- **S_obs(t)** = observed physiological trajectory at time **t**
- **D(·)** = divergence function between expected and observed trajectories
- **q(t)** = signal-quality factor
- **\lambda(t)** = temporal weighting factor
- **\Delta t** = observation window

---

## Epistemic Tension Index

The central quantity in the CRB architecture is the **Epistemic Tension Index (σ)**.

A simplified conceptual formulation is:

$$
\sigma(t) = \int_{t-\Delta t}^{t} q(\tau)\,\lambda(\tau)\,D\big(S_{exp}(F,\tau),\,S_{obs}(\tau)\big)\,d\tau
$$

This formulation encodes a critical conceptual boundary:

> **σ does not measure physiological deterioration itself.  
> σ measures divergence between the physiological trajectory expected under the active clinical frame and the trajectory actually observed.**

This is what makes the variable **epistemic** rather than merely physiological.

---

# Practical Interpretation of σ

A low **σ** suggests that observed evolution remains broadly coherent with the active frame.

A rising **σ** suggests that the frame may be losing explanatory power.

A high **σ** does not mean that the system knows the correct diagnosis.

It means that the **current frame may no longer be adequately explaining the patient’s evolution**.

The role of the signal is therefore to support **reassessment**, not substitution of judgment.

---

# Reflection Gate

Because reflective signaling can itself become harmful if overused, every candidate signal passes through a **reflection gate**.

The gate suppresses signals when:

- divergence is minimal
- data quality is poor
- the mismatch is already obvious
- the team is already adapting the frame
- the expected benefit of signaling is low

The gate allows signaling only when:

- epistemic tension is rising
- workflow remains organized around the original frame
- the mismatch has not yet been meaningfully integrated into ongoing reasoning
- signal timing is likely to be useful rather than disruptive

---

# Signal Properties

A CRB signal must be:

- minimal
- non-diagnostic
- non-recommendatory
- non-interruptive
- rare

Examples:

- subtle haptic pulse
- neutral visual marker
- short non-directive phrase

Examples of acceptable signal language:

- **FRAME UNDER EPISTEMIC TENSION**
- **COHERENCE GAP DETECTED**
- **TRAJECTORY-FRAME DIVERGENCE RISING**

Examples of unacceptable signal language:

- **Consider pulmonary embolism**
- **Escalate treatment now**
- **Sepsis likely**

The system must never cross from reflection into recommendation.

---

# Why the Model Is Not Traditional Decision Support

Traditional Clinical Decision Support Systems (CDSS) attempt to improve clinical direction by suggesting diagnoses, treatments, or actions.

The CRB operates in a different space.

It does not optimize decisions directly.

It monitors the **stability of the perceptual and interpretive structure from which decisions are being made**.

Its target is not the decision itself.

Its target is the **coherence of the frame underlying the decision**.

---

# Success Conditions

The CRB should not be judged primarily by conventional predictive accuracy metrics.

Relevant evaluation targets include:

- earlier frame reassessment
- meaningful signal relevance
- low false-positive burden
- preservation of workflow compatibility
- post hoc cognitive transparency

The architecture succeeds if it helps teams recognize **frame instability earlier** without adding significant cognitive burden.

---

# Conceptual Status

This system model represents a **research-stage conceptual architecture**.

It is intended to support:

- theoretical clarification
- research discussion
- architecture design
- future validation planning

It is **not** an implementation, a deployable device, or a validated clinical system.
