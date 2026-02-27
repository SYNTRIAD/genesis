# Example: Autonomous Mathematical Discovery

This example shows SYNTRIAD applied to mathematical research—specifically, the autonomous discovery of patterns in digit-operation dynamical systems.

---

## Context

**The Problem:** Given a space of digit operations (reverse, sum, multiply, etc.), find fixed points, attractors, and structural relationships.

**The Starting Point:** The classic "1089 trick" — the number 1089 satisfies 1089 × 9 = 9801 = reverse(1089). Is this an isolated curiosity, or part of a larger structure?

---

## Application of the Pattern

### Φ₁ INTAKE

**State (S):**
- Known: 1089-trick exists
- Unknown: Are there other fixed points? What structure do they share?

**Intention (I):**
- Discover all fixed points for digit-operation pipelines
- Find structural relationships to known sequences (OEIS)
- Produce publication-ready mathematical results

**Constraints (C):**
- Must be mathematically rigorous
- Must be computationally verifiable
- Must be reproducible

---

### Φ₂ DECOMPOSE

Break into atomic research questions:

1. What operations preserve digit structure?
2. What are the fixed points for each operation?
3. What families exist among the fixed points?
4. What are the basin sizes for each attractor?
5. Do the families relate to known OEIS sequences?

---

### Φ₃ UNTANGLE

Resolve dependencies:

```
GPU-exhaustive search
        ↓
Fixed point enumeration
        ↓
Family classification
        ↓
OEIS matching
        ↓
Algebraic proof
```

Each step depends on the previous. The plan is sequential with validation gates.

---

### Φ₄ TRANSFORM

Execute the P,V-loop:

**Iteration 1:**
```
P: Generate candidate fixed points via GPU search (10^9 integers)
V: Verify each candidate satisfies the fixed-point equation
→ Result: Enumerated list of all fixed points
```

**Iteration 2:**
```
P: Hypothesize family structure from the enumerated data
V: Test hypothesis against all known fixed points
→ Result: Family classification with generating formula
```

**Iteration 3:**
```
P: Search OEIS for sequences matching the family structure
V: Verify structural relationship algebraically
→ Result: Discovery of A001232 relationship
```

**Iteration 4:**
```
P: Formalize the relationship as a theorem
V: Construct rigorous proof
→ Result: Publication-ready theorem with proof
```

---

### Φ₅ OUTPUT

**Results:**

1. **Complete characterization** of the 1089-trick family
2. **Novel discovery:** n_k = 10 × A001232(k-4) for k ≥ 5
3. **Two publication-ready papers** with formal proofs

**V++ (Validation Loop):**

| Criterion | Status |
|-----------|--------|
| Does it work? | ✓ All results GPU-verified |
| Does it match the intention? | ✓ Novel mathematical discoveries achieved |
| Does it respect the constraints? | ✓ Rigorous, verifiable, reproducible |

---

## The Key Insight

The P,V-loop is not just a process pattern—it's a **discovery engine**.

When applied to open mathematical questions, it systematically:

1. **Generates hypotheses** (P-phase) — exploring the possibility space
2. **Tests them rigorously** (V-phase) — contracting to validated knowledge
3. **Iterates** — until convergence to publishable results

The pattern doesn't guarantee discovery, but it **maximizes the probability** of discovery by ensuring:
- Systematic exploration (no gaps)
- Rigorous validation (no false positives)
- Cumulative progress (V++ preserves gains)

---

## Comparison to Ad-Hoc Research

| Aspect | Ad-Hoc Approach | SYNTRIAD Approach |
|--------|-----------------|-------------------|
| Exploration | Intuition-driven, may miss cases | Systematic, exhaustive |
| Validation | Manual checking, error-prone | GPU-verified, reproducible |
| Progress tracking | Mental notes, scattered | Explicit state, auditable |
| Reproducibility | Difficult | Built-in (V++ artifacts) |

---

## Artifacts Produced

The V++ phase produced:

- `paper_A.tex` — Fixed Points of Digit-Operation Pipelines
- `paper_B.tex` — Attractor Spectra of Digit-Operation Pipelines
- `proof_engine.py` — Automated proof verification
- `experiment_runner.py` — Reproducible experiment framework
- SQLite database with all intermediate results

---

## References

- See `evidence/digit-dynamics.md` for more details
- [Empirical Thermodynamic Convergence (Zenodo)](https://zenodo.org/records/17618998)
- [OEIS A001232](https://oeis.org/A001232)
