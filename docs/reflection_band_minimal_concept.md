# Reflection Band — Minimal Concept v0.1

## 1) Problem Statement

In high-urgency clinical environments, the primary challenge is not the lack of information, but **cognitive interruption**.

Traditional AI systems often introduce friction because they require structured input or interactive engagement at moments when clinicians have no available cognitive bandwidth.

This concept aims to support clinicians **without competing with judgment**, by offering minimal, non-intrusive intelligence signals only at critical inflection points.

---

## 2) Design Principles

- **Silence as default**  
  Reassurance comes from the absence of interruption.

- **Non-competitive support**  
  The system must never override, constrain, or compete with clinical judgment.

- **Minimal intervention**  
  Intervene only when uncertainty is high and reversibility is still plausible.

- **Authority remains human**  
  Responsibility and accountability remain with the clinician at all times.

---

## 3) Proposed Interface

### Form factor
- Dedicated wristband-style device (conceptual only).

### Primary signal (color-based)
- 🟢 **Green** — stability / silence  
- 🟡 **Yellow** — possible imminent complication (>75% estimated risk)  
- 🔴 **Red** — critical contradiction with high risk  

Signals appear only when a clinically significant inflection point is detected.

---

## 4) Reflection Mode — Minimal Rules

The system operates in a **reflection mode** focused on surface checks, not recommendations.

1. **Contradiction check**  
   Is there any single feature (symptom, vital sign, lab, or context) that would make the current plan unsafe?

2. **Pattern mismatch**  
   Is there a classic high-risk pattern that does not fully fit the working hypothesis and is commonly overlooked under time pressure?

3. **Regret test**  
   If the outcome were poor despite appropriate care, what is the most likely thing a clinician would wish they had paused to verify?

### Constraints
- Do not generate diagnoses.
- Do not expand differentials unless explicitly prompted.
- Do not suggest management unless a clear contradiction exists.
- Keep responses concise and clinically grounded.

---

## 5) What This Is Not

This concept is not:
- a diagnostic system,
- a traditional clinical decision support tool,
- a workflow automation engine,
- a personal wearable outside institutional context.

It is a **cognitive support artifact** designed to reduce noise while preserving human authority.

---

## 6) Minimal Reference Scenario

### Acute myocardial infarction — first hour

Even when evidence-based care is delivered correctly, early AMI evolution is often chaotic.

The objective is not prediction, but to surface only those signals that still fall within **reversible bounds** during the first hour.

---

## 7) Status

This document is a **thinking artifact**.  
No implementation is implied.  
No deployment assumptions are made.
