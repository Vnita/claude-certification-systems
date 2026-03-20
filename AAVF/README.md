# AAVF — AI Assessment Validity Framework v1.0

A 5-pillar psychometric validity framework for certification programs 
where an LLM is the primary assessor — addressing novel validity threats 
that existing frameworks were not designed to handle.

## The Problem

Psychometric standards that govern whether a certification is defensible 
were built for human-scored assessments. When an LLM is the primary 
rater, five validity threats emerge that existing frameworks — Messick, 
AERA/APA Standards — do not adequately address.

## The 5 Pillars

| Pillar | Classic Threat | New AI-Specific Threat |
|--------|---------------|----------------------|
| 1. Construct Validity | Does the test measure what it claims? | Style bias as construct contamination |
| 2. Reliability | Consistent scores across instances? | Prompt sensitivity, context position, temperature variance |
| 3. Fairness | Equitable scores across groups? | Inherited training bias embedded in model weights |
| 4. Consequential Validity | Do decisions predict job performance? | No baseline data at launch |
| 5. Temporal Validity ⭐ | — | Original contribution. No equivalent in published literature. |

## What Makes This Framework Different

AAVF does not port classical psychometrics onto AI systems. It identifies 
where classical frameworks break — and builds new standards for those 
specific failure points.

The fifth pillar, Temporal Validity, is an original contribution with 
no equivalent in Messick or the AERA/APA Standards. It defines what 
happens to validity evidence when the assessed product ships a new 
version — a problem that did not exist at scale until AI products began 
shipping on rapid release cycles.

## Minimum Evidence Standard

This framework defines the minimum validity, reliability, and fairness 
evidence required before a certification can be offered publicly.

Meeting this standard means the certification is:
- Defensible under scrutiny
- Honest about its current evidence base
- Operating with a clear plan for collecting additional evidence 
  post-launch

## Relationship to CCEE

AAVF is the governing standard. CCEE is the operational implementation.

- C3 (Quality Auditor) implements Pillars 1, 2, and 3 at the item level
- C4 (Capability Checker) implements Pillar 5 at the item bank level
- Pillar 4 requires post-launch outcome data — collection plan must be 
  designed before first cohort graduates

## Status

AAVF v1.0 addresses launch defensibility.
AAVF v2.0 will address ongoing defensibility — the feedback loop between 
post-launch outcome data and validity claims. This requires empirical 
data from a live program and will be developed in parallel with the 
first certification cohort.
