# 🛡️ Guardrail Layer

Guardrails enforce **structural, logical, and safety constraints** after each agent step.

---

## A0 — Input & Output Guardrail

**Controls**
- deduplicate RSS items
- filter spam / promotional content
- validate schema completeness
- ensure traceability to source

---

## A1 — Draft Validation Guardrail

**Controls**
- required fields present
- minimum content quality
- banned overclaim detection:
  - "fully compliant"
  - "guaranteed safe"
  - "zero risk"
- source traceability enforcement

---

## A2 — Reviewer Guardrail

**Controls**
- enforce valid decision states
- validate score format
- ensure issue classification completeness
- check consistency between score and status

---

## A3 — Revision Guardrail

**Controls**
- score/status must remain unchanged
- ensure revision addresses reviewer findings
- prevent reintroduction of overclaims
- validate revision completeness

---

## Design Principle

Guardrails act as:

> **runtime enforcement layer between AI outputs and downstream decisions**