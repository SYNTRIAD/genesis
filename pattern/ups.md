# Universal Prompt Structure (UPS)

The Universal Prompt Structure (UPS) is a concrete instantiation of the metapattern.

It standardizes **how work is structured**, not **what the work contains**.
The same structure applies to AI prompts, project plans, analyses, designs, and reviews.

Copy it. Fill it. Reuse it.

---

## The Structure

Each section corresponds to one or more phases of the metapattern (Φ₁–Φ₅).

```
## STATE

## INTENTION

## CONSTRAINTS

## DECOMPOSITION

## DEPENDENCIES

## TRANSFORMATION

## OUTPUT

## VALIDATION
```

---

## Φ₁ — INTAKE

### STATE

Describe the current situation.

Include:
- relevant context
- available inputs or materials
- known assumptions

Avoid interpretation or solutioning.

---

### INTENTION

State the desired outcome.

The intention should be:
- explicit
- testable
- direction-setting, not solution-specific

If the intention cannot be validated, it is underspecified.

---

### CONSTRAINTS

Define the boundaries of acceptable output.

Constraints may include:
- domain limits
- required formats
- exclusions or prohibitions
- quality thresholds

Constraints determine what will be rejected during validation.

---

## Φ₂ — DECOMPOSE

### DECOMPOSITION

Break the task into atomic parts.

Each part should:
- be independently understandable
- have a clear purpose
- not depend on hidden assumptions

Good decomposition reduces cognitive load and enables parallel work.

---

## Φ₃ — UNTANGLE

### DEPENDENCIES

Identify relationships between parts.

Include:
- ordering constraints
- prerequisite relationships
- feedback loops

Resolve circular dependencies where possible.
If not, make them explicit.

---

## Φ₄ — TRANSFORM

### TRANSFORMATION

Execute the work according to the established plan.

During execution:
- follow the resolved order
- respect constraints continuously
- validate intermediate results when possible

Transformation without validation accumulates drift.

---

## Φ₅ — OUTPUT

### OUTPUT

Assemble the results.

The output should:
- directly address the intention
- respect all constraints
- be complete enough to validate

---

### VALIDATION

Evaluate the output against Φ₁.

Ask explicitly:
- Does it work?
- Does it match the intention?
- Does it respect the constraints?

If validation fails, return to the appropriate phase and iterate.

Successful validation increments the version (V++).

---

## Notes on Use

- The structure is invariant; the content is not.
- Sections may be brief or extensive depending on task complexity.
- The same structure can be nested recursively.

If a section feels unnecessary, leave it empty—but do not remove it.

Empty sections are signals.
Missing sections are blind spots.

