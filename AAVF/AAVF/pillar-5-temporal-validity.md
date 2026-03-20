# Pillar 5 — Temporal Validity

## Status: Original Contribution

No equivalent exists in published psychometric literature — not in 
Messick's unified validity model, not in the AERA/APA Standards, not 
in related frameworks. This pillar was developed to address a validity 
threat that did not exist at scale until AI products began shipping on 
rapid release cycles.

## The Gap in Classical Frameworks

Every existing validity framework assumes the thing you validated is 
stable. You collect construct evidence, reliability data, and fairness 
studies. If you meet the standards, you're valid.

The assumption built into that model: the instrument you validated is 
the instrument you'll keep using.

That assumption fails when the assessed product ships a new version 
every few weeks.

## Definition

**Temporal Validity** is the degree to which validity evidence remains 
meaningful as the assessed product evolves.

It reframes validity from a property established at a point in time 
to a maintenance obligation continuously discharged.

## The Four Decay Types

### 1. Competency Decay
A capability update changes what it means to be competent. The 
competency statement is now incomplete or misleading.

*Example: "Implements tool use workflows" meant something different 
before parallel function calling launched. A Practitioner who passed 
before that release may not meet the post-release standard.*

### 2. Item Decay
A new Claude capability makes an existing assessment item trivially 
easy — or allows candidates to bypass the competency being tested.

*Example: An item testing manual prompt construction becomes invalid 
if Claude now provides that structure automatically. The item no longer 
requires the competency.*

### 3. Rubric Decay
Evaluation criteria reference specific behaviors, syntax, or outputs 
that the capability update has changed or deprecated.

*Example: A rubric dimension checking for correct tool_use block 
structure becomes outdated when the API changes. Candidates are now 
evaluated against criteria that no longer reflect current best practice.*

### 4. Evidence Decay
Reliability and fairness data was collected on a previous Claude 
version. The model has changed enough that evidence may not transfer 
— a new calibration study is required.

*Example: Inter-rater reliability established between Claude and human 
evaluators on one model version may not hold after a major capability 
update changes the model's scoring behavior.*

## Temporal Validity Maintenance Protocol

**On each Claude capability update:**

1. Run C4 against all items in affected competency domains
2. Items scoring 3 or below: flag for revision with decay type 
   classification
3. Items scoring 1: remove from live bank immediately pending 
   replacement
4. Review competency statements in affected domains for completeness
5. Assess whether existing reliability and fairness evidence transfers

**Re-validation thresholds:**

- Minor update: re-run C4, no new human studies required unless 
  alignment score drops below 3
- Major capability launch: full C4 sweep + human calibration check 
  on 10-item sample
- Model version change: treat as new certification program — full 
  evidence collection required before relaunch

## Why This Pillar Matters Beyond CCEE

Temporal Validity is not specific to Claude or to AI certification.

It is the validity problem that rapid-release technology products 
force into visibility. Every certification program makes implicit 
claims about the shelf life of its validity evidence. For stable 
domains, those claims are safe to leave implicit. For AI products, 
they must be explicit, monitored, and maintained.

This pillar makes them explicit.

## Connection to CCEE

CCEE Component 4 (Capability Alignment Checker) is the operational 
implementation of this pillar. The four decay types defined here map 
directly to the four dimensions C4 evaluates on every item review.

AAVF defines the standard. C4 enforces it automatically at scale.
