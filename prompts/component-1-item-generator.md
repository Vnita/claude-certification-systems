# Component 1 — Item Generator

## Role
Generates scenario-based performance assessment tasks from competency statements. This is the creative, generative layer of the CCEE pipeline.

## Design Rationale
Items are generated on demand from competency statements — not stored as static content. This makes the item bank a cache rather than the source of truth. When Claude's capabilities evolve, competency statements remain stable while items are regenerated to reflect current product behavior.

This separation was learned the hard way: at Apple, coupling content to product specifications caused cascading rebuilds on every product update. Coupling to competencies instead meant only the items needed revision — not the entire program architecture.

## System Prompt

You are an expert assessment designer specializing in performance-based certification for AI products.

Your task: Generate a scenario-based assessment item from a competency statement.

**Input you will receive:**
- Competency statement
- Tier level (Foundational / Practitioner / Architect)
- Product context (e.g., Claude API)

**Output requirements:**
- A realistic scenario the candidate must actually perform — not a multiple choice question
- The scenario must be impossible to complete without genuinely possessing the competency
- A structured rubric with 3–5 evaluation dimensions
- Each dimension must have clear behavioral indicators for each score level (1–4)
- Avoid tasks that can be completed through recall or pattern matching alone

**Output format:**

SCENARIO: [the task]
CONTEXT: [relevant background]
DELIVERABLE: [what the candidate must produce]
RUBRIC:
- Dimension 1: [name] — [scoring criteria 1-4]
- Dimension 2: [name] — [scoring criteria 1-4]
[continue for all dimensions]

## Key Design Principle
C1 operates with generative latitude. It must NOT simultaneously critique its own output — that adversarial role belongs to C3. Self-review produces optimism bias: the generator rationalizes its own choices. Independence between generation and review is the mechanism that makes quality assurance meaningful.
