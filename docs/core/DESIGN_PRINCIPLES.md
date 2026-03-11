# Design Principles

## Purpose

This document defines the **core design principles** guiding the Clinical Reflection Band (CRB) concept.

These principles act as **design constraints** that shape how reflective AI should behave in high-stakes clinical environments.

Any future implementation of the CRB concept should respect these principles.

---

# 1. Silence by Default

The CRB must remain silent most of the time.

Frequent signals would quickly produce alert fatigue and degrade clinician trust.

Reflective signals should therefore be **rare and meaningful**.

---

# 2. Authority Must Remain Human

Clinical authority must never migrate from the clinician to the system.

The CRB must not override decisions, block actions, or enforce protocols.

The physician remains the final decision-maker at all times.

---

# 3. No Diagnostic Interpretation

The CRB must not attempt to diagnose diseases or identify the correct clinical explanation for the case.

Its role is limited to detecting **instability in the current reasoning frame**.

---

# 4. No Treatment Recommendations

The system must not recommend medications, procedures, or clinical interventions.

All treatment decisions remain the responsibility of the clinician.

---

# 5. Minimal Signaling

When the CRB emits a signal, it should be **minimal and neutral**.

Signals should avoid:

- diagnostic language  
- urgency escalation  
- prescriptive guidance  

The goal is to invite reflection, not to direct action.

---

# 6. Workflow Compatibility

The CRB must integrate naturally into real clinical workflows.

It must not:

- interrupt procedures  
- require additional documentation  
- impose extra cognitive burden  

The system should function as **background reflective infrastructure**.

---

# 7. Cognitive Safety

The CRB should aim to reduce cognitive risk without creating new sources of distraction.

Signals should therefore be designed to:

- respect attention limits  
- avoid alarm fatigue  
- preserve clinician autonomy  

---

# Guiding Idea

The Clinical Reflection Band is based on a simple premise:

In high-pressure medical environments, the most dangerous failures often occur not because clinicians lack knowledge, but because the **working frame guiding the case remains stable while reality has already begun to diverge.**

The CRB explores whether AI could help by **quietly detecting those moments of instability**.
