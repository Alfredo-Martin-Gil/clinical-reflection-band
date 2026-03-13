# Research Questions and Contributions

## Purpose

This document aligns the repository with the formal research framing of the **Clinical Reflection Band (CRB)** paper.

The purpose is to make explicit that the CRB is not only a conceptual design artifact, but also a structured research proposal within the broader space of reflective clinical AI.

---

# Research Questions

## RQ1

Can divergence between the physiological trajectory expected under the active clinical frame and the trajectory actually observed serve as a meaningful signal of instability in that frame?

This is the foundational question of the CRB concept.

The claim is not that divergence automatically reveals the correct diagnosis, but that it may reveal when the **current frame is losing explanatory coherence**.

---

## RQ2

Can reflective signals improve clinician awareness of frame instability without reproducing the harms of ordinary alerting systems?

This question addresses a central design tension.

If the CRB emits signals too often, too strongly, or too interpretively, it collapses into another source of cognitive burden.

The architecture therefore depends on:

- rarity
- minimalism
- timing discipline
- non-directive signaling

---

## RQ3

Can reflective monitoring be integrated into existing workflows without requiring explicit frame entry or adding meaningful operational friction?

The CRB assumes that frame inference must be **passive** and **workflow-compatible**.

A system that depends on repeated explicit user labeling of the frame would not be viable in high-pressure environments such as emergency medicine or prehospital care.

---

## RQ4

Can a reflective monitoring layer function as **cognitive safety infrastructure** rather than as a diagnostic or treatment recommendation system?

This question defines the conceptual boundary of the CRB.

The goal is not to produce answers.

The goal is to create a technical mechanism capable of detecting when the clinician’s active interpretive frame may be losing coherence with the patient’s evolution.

---

# Core Contributions

## 1. Formalization of Case Drift

The CRB introduces **Case Drift** as a specific form of clinical frame instability.

Case Drift occurs when:

- an active clinical frame remains in place
- that frame remains plausible enough to sustain workflow
- the patient’s physiological trajectory progressively diverges from what the frame would predict
- the workflow continues without meaningful reframing

This is the structural problem the CRB is designed to monitor.

---

## 2. Proposal of Reflective Clinical AI

The repository defines the CRB as part of a broader conceptual class:

**Reflective Clinical AI**

This class is distinct from:

- predictive AI
- recommendation systems
- standard Clinical Decision Support Systems
- deterioration alerts

Its target is not disease classification or management optimization.

Its target is **coherence monitoring at the level of the active interpretive frame**.

---

## 3. Definition of the Epistemic Tension Index

The CRB introduces a formal monitoring target:

**Epistemic Tension Index (σ)**

This index does not represent deterioration alone.

It represents divergence between:

- the expected physiological trajectory conditioned on the inferred frame
- the observed physiological trajectory of the patient

This distinction is what gives the variable its epistemic character.

---

## 4. Layer-2 Reflective Architecture

The repository defines the CRB as a **Layer-2 reflective architecture** that operates alongside ordinary clinical workflow.

Its task is not to guide the decision itself, but to monitor the stability of the structure from which the decision is being made.

This design preserves:

- human authority
- minimal signal burden
- compatibility with real clinical environments
- conceptual separation from recommendation systems

---

## 5. Workflow-Compatible Passive Inference

The CRB is explicitly designed around passive multimodal inference.

The active frame is not expected to be entered manually.

Instead, it is inferred from signals already generated during care, such as:

- notes
- CPOE patterns
- intervention pathways
- handoffs
- physiological evolution
- spoken reasoning when available

This is essential for emergency and critical care compatibility.

---

# Why These Contributions Matter

Most clinical AI systems attempt to answer questions such as:

- What is the likely diagnosis?
- What is the patient’s risk?
- What intervention should be considered?

The CRB asks a different question:

> Is the frame currently guiding interpretation still coherent with the patient’s observed evolution?

This reframing opens a different research direction.

Instead of optimizing the answer, the system monitors the **stability of the question structure itself**.

---

# Repository Relevance

Within this repository, these research questions and contributions serve three purposes:

1. they anchor the conceptual work in an explicit research agenda
2. they align the repository with the paper’s formal structure
3. they clarify that the CRB should be read as a serious reflective AI proposal rather than as a generic idea artifact

---

# Current Status

These research questions and contributions are conceptual and architectural.

They do not claim that the CRB has already been validated.

They define the structure of the research program that would be required to evaluate whether reflective clinical AI can function as useful cognitive safety infrastructure.
