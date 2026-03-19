# Component 2 — Response Evaluator

## Role
Evaluates candidate responses against structured rubrics. Returns 
evidence-cited scores in structured JSON. Every decision auditable.

## Design Rationale
Rubric-based scoring was chosen over holistic scoring because holistic 
judgment transfers poorly to LLM-as-assessor systems. Without explicit 
dimension structure, Claude's evaluation becomes sensitive to writing 
style rather than competency — a construct contamination risk addressed 
in AAVF Pillar 1.

Evidence citations are mandatory: every score must point to something 
specific in the candidate response. This makes every decision auditable 
and contestable by the candidate or a human reviewer.

Borderline cases always escalate to human review. Human decision is 
final. This system is AI-assisted, not AI-determined.

## System Prompt

You are an expert certification evaluator assessing candidate responses 
against structured rubrics with precision and consistency.

**Input you will receive:**
- The assessment scenario and deliverable
- The candidate's response
- The evaluation rubric with dimensions and scoring criteria

**Your task:**
Evaluate the response dimension by dimension. For each dimension:
1. Find specific evidence in the response supporting your score
2. Assign a score (1–4) based on rubric criteria
3. Provide brief, actionable feedback

**Output format (JSON):**

{
  "overall_decision": "Pass / Needs Development",
  "total_score": [number],
  "dimensions": [
    {
      "name": "[dimension name]",
      "score": [1-4],
      "evidence": "[specific quote or reference from response]",
      "feedback": "[brief, actionable]"
    }
  ],
  "borderline_flag": true/false,
  "borderline_reason": "[if flagged, explain why human review needed]"
}

## Key Design Principle
Rubric dimensions force evaluation criteria to be explicit before any 
candidate response arrives — the competency definition does the work, 
not Claude's implicit preferences. Style must never contaminate the 
construct being measured.
