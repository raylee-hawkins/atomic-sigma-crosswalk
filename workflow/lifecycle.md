# Detection Engineering Lifecycle

## Objective

Provide a repeatable workflow for developing, translating, validating, and documenting detection content using evidence-based engineering practices.

---

# Lifecycle

```
Candidate Intake
-> ATT&CK Mapping
-> Telemetry Analysis
-> Detection Design
-> Platform Translation
-> Validation
-> Evidence Capture
-> Documentation
-> Review and Merge
```cls]

---

## Stage 1: Candidate Intake

Purpose:
Define the adversary behavior being investigated.

Outputs:
- Candidate identifier
- ATT&CK mapping
- Detection hypothesis
- Expected behavior
- References

---

## Stage 2: Telemetry Analysis

Purpose:
Determine whether required telemetry exists.

Outputs:
- Required event sources
- Required fields
- Correlation identifiers
- Telemetry assumptions
- Blind spots

---

## Stage 3: Detection Design

Purpose:
Define detection logic and confidence boundaries.

Outputs:
- Primitive detection logic
- Correlation logic
- Assumptions
- Limitations

---

## Stage 4: Platform Translation

Purpose:
Implement equivalent logic across platforms.

Outputs:
- Sigma
- Splunk SPL
- Sentinel KQL
- Translation notes
- Platform limitations

---

## Stage 5: Validation

Purpose:
Measure expected versus observed behavior.

Outputs:
- Validation status
- Expected events
- Observed events
- False positives
- False negatives
- Validation notes

---

## Stage 6: Evidence Capture

Purpose:
Provide evidence supporting detection claims.

Outputs:
- Query output
- Redacted telemetry
- Screenshots
- Notes
- Validation artifacts

---

## Stage 7: Documentation

Purpose:
Preserve implementation details and engineering decisions.

Outputs:
- Detection documentation
- Telemetry documentation
- Translation notes
- Validation documentation

---

## Stage 8: Review and Merge

Purpose:
Verify quality and maintain evidence boundaries.

Outputs:
- Peer review
- Approved changes
- Merge decision
- Follow-up work items

---

## Engineering Principles

- Do not claim validation without evidence.
- Separate detection logic from correlation logic.
- Document assumptions explicitly.
- Preserve public-safe boundaries.
- Prefer incremental improvements over rewrites.
- Treat detections as measurable systems.