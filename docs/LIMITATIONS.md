# Limitations and Safety Boundaries

## Purpose of this Document

This document defines the **explicit safety boundaries and limitations** of the Clinical Reflection Band (CRB) concept.

The goal is to clarify what the system **must not do**, preventing misinterpretation of the project as a diagnostic or decision-making AI system.

The CRB model is intentionally designed with strict functional constraints.

---

# Core Limitation

The CRB **does not attempt to solve the clinical case.**

Its purpose is limited to detecting potential **instability in the clinician’s working reasoning frame.**

The system provides **reflection**, not answers.

---

# What the System Does NOT Do

The CRB must not perform the following functions.

## No Diagnosis

The system does not determine or suggest diagnoses.

It does not attempt to classify diseases or identify the underlying pathology of the case.

---

## No Treatment Recommendation

The system does not recommend treatments, medications, or interventions.

All clinical decision-making authority remains with the clinician.

---

## No Clinical Decision Automation

The CRB does not automate clinical decisions.

It does not:

- start treatments
- trigger protocols
- block clinical actions

---

## No Replacement of Clinical Judgment

The system is not designed to replace clinical reasoning.

Its role is strictly reflective.

Clinical authority remains entirely with the physician.

---

# No Continuous Alerting

A central design constraint is that the CRB must **avoid alert fatigue**.

Most clinical AI systems fail because they generate excessive interruptions.

The CRB must therefore remain **silent most of the time**.

Signals should only occur when meaningful frame instability is detected.

---

# Uncertainty and Imperfection

Even if implemented, the CRB system would remain imperfect.

Possible limitations include:

- missed frame instability
- false reflective signals
- inability to interpret complex clinical narratives
- incomplete physiological signal capture

The system should therefore be understood as **a weak signal generator**, not a reliable detector of deterioration.

---

# No Guarantee of Clinical Safety

The CRB cannot guarantee:

- earlier diagnosis
- prevention of clinical deterioration
- improved patient outcomes

It only aims to provide **additional cognitive reflection opportunities** during complex cases.

---

# Implementation Constraints

If explored in the future, any implementation would require careful evaluation in several domains:

- clinical safety
- human factors
- workflow compatibility
- legal responsibility
- regulatory classification

At present, the CRB concept exists **only as a conceptual architecture**.

---

# Ethical Considerations

The CRB concept assumes that clinical responsibility remains fully human.

The system must therefore avoid:

- authority migration
- decision substitution
- hidden influence over clinical reasoning

Signals must remain **neutral and non-directive**.

---

# Conceptual Status

The Clinical Reflection Band should currently be understood as:

- a conceptual architecture
- a research exploration
- a framework for discussing reflective AI in medicine

It is **not a medical product and not a deployable technology.**

---

# Guiding Principle

The CRB concept is guided by a simple constraint:

AI systems that assist clinicians should **reduce cognitive risk without replacing clinical authority.**

The CRB explores whether reflective signals about **reasoning stability** could be one possible path toward that goal.
