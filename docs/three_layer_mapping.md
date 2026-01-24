# Reflection Band — Three-Layer Mapping

This document maps the Reflection Band concept to a three-layer model commonly used in workflow and safety-critical system design.

The intent is not to define a system, but to make explicit where each design element operates — and where it must not leak.

---

## Layer 1 — Interface / Interaction

What the clinician perceives in real time.

- Dedicated, single-purpose interface (wristband-style).
- Color-based signaling as the primary channel.
- Silence (steady green) as the default state.
- Visual signals appear only at clinically meaningful inflection points.
- No mandatory interaction, data entry, or acknowledgment required.

This layer exists to **preserve attention**, not to demand it.

---

## Layer 2 — Intelligence / Interpretation

What the system infers or prioritizes internally.

- Pattern aggregation across available signals.
- Detection of contradictions with the current working plan.
- Identification of classic high-risk pattern mismatches.
- Regret-oriented reflection: “what would be hardest to miss later?”
- Conservative thresholds focused on reversibility, not prediction.

This layer is intentionally restrained and **does not generate decisions**.

---

## Layer 3 — Authority / Responsibility

Who decides, and who remains accountable.

- All clinical judgment remains with the human clinician.
- The system cannot block, enforce, or override actions.
- Alerts acknowledge risk but do not prescribe behavior.
- Acceptance of trade-offs is explicitly human.
- Responsibility, liability, and authorship stay entirely outside the system.

This layer is **non-negotiable**.

---

## Boundary Conditions

If any element of the design:
- competes with clinical judgment,
- forces interaction under time pressure,
- or shifts responsibility away from the clinician,

then the system has crossed its intended boundary and failed its purpose.
