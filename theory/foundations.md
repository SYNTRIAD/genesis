# Theoretical Foundations

The SYNTRIAD pattern is grounded in a formal theory of semantic thermodynamics. This document summarizes the foundational axioms.

**Epistemic note:** These axioms range from formally supported (G₂, G₃) to hypothesized (G₁, G₄). Labels indicate the current evidence status. See `evidence/publications.md` for the underlying papers.

---

## The Four Axioms

### G₁: Convergence Phenomenology [HYPOTHESIZED]

> **Convergence phenomenology is the observable effect when a system simultaneously decreases energy and increases coherence while having reflexive capacity.**

When a system:
1. Decreases energy: `E(x_{t+1}) < E(x_t)`
2. Increases coherence: `Ψ(x_{t+1}) > Ψ(x_t)`
3. Has reflexive capacity (can observe itself)

...it exhibits **convergence phenomenology**—the measurable shift toward stability, alignment, and reduced semantic tension.

| Domain | Manifestation |
|--------|---------------|
| Individual | Flow states, creative breakthrough |
| Team | Shared understanding, reduced coordination friction |
| Organization | Alignment, cultural coherence, institutional learning |
| System | Reduced entropy, stable equilibrium under drift |

---

### G₂: Triadic Unification [SUPPORTED]

> **Complex systems can be modeled as evolving through variation, selection, and integration. The Production-Validation (P,V) loop operationalizes this pattern.**

```
        CHAOS
      (Possibility)
         ↓ P
        ORDER
     (Structure)
         ↓ V
      SYNTHESIS
    (Integration)
         ↓ P'
     NEW CHAOS
   (Expanded Possibility)
         ↓
        ...
```

**Formal Expression:**

```
S_{n+1} = V(P(S_n))
```

Where:
- `S_n` = system state at iteration n
- `P` = Production operator (generates candidates from chaos)
- `V` = Validation operator (selects for coherence)

**Scale Invariance:**

| Scale | Chaos | Order | Synthesis |
|-------|-------|-------|-----------|
| Quantum | Superposition | Measurement | Eigenstate |
| Evolution | Mutation | Selection | Adaptation |
| Science | Hypothesis | Experiment | Theory |
| Mind | Imagination | Reason | Understanding |
| Organization | Innovation | Process | Culture |

---

### G₃: Semantic Thermodynamics

> **Semantic energy provides a quantitative proxy for coherence. Systems naturally evolve toward states that minimize semantic energy while preserving coherence. Understanding correlates with compression. Intelligence can be modeled as the optimization of the Coherence-to-Complexity Ratio (CCR).** [HYPOTHESIZED]

See `theory/hamiltonian.md` for the formal energy function.

**The Optimization Principle:**

```
x* = argmax_x CCR(x) = argmax_x Ψ(x)/K(x)
```

Intelligence, in this model, is the search for the **Minimum Viable Model (MVM)**—the peak of the CCR curve. [HYPOTHESIZED]

---

### G₄: Scale-Relative Evaluation

> **In this framework, "good" at a given scale is defined as that which increases coherence at that scale without destroying coherence at other scales. This is a modeling choice, not an ethical theory.** [HYPOTHESIZED]

**Goodness at scale s:**
```
G_s(a) = ΔΨ_s(a)
```

**Wisdom (cross-scale coherence):**
```
W(a) = Σ w_s · ΔΨ_s(a)
```

**Ethical Constraint:**
```
∀s: ΔΨ_s(a) ≥ -ε_s
```

An action is fully ethical only if it does not catastrophically reduce coherence at any scale.

| Scale | Coherence Definition | Typical Timeframe |
|-------|---------------------|-------------------|
| Micro (Self) | Internal consistency, wellbeing | Seconds to days |
| Meso (Relation) | Mutual understanding, trust | Days to months |
| Macro (System) | Organizational health, efficiency | Months to years |
| Meta (Ecology) | Systemic sustainability, resilience | Years to generations |

---

## The Mandala

```
              G₁ (Convergence Phenomenology)
                    /           \
                   /             \
                  /               \
 G₄ (Scale Ethics) ←———————————→ G₂ (Triadic Unification)
                  \               /
                   \             /
                    \           /
              G₃ (Semantic Thermodynamics)
```

The four axioms form a quaternion:
- **G₁** [HYPOTHESIZED] provides the phenomenological anchor (convergence effects)
- **G₂** [SUPPORTED] provides the dynamic engine (P,V loops)
- **G₃** [HYPOTHESIZED] provides the measurement framework (energy, coherence, CCR)
- **G₄** [HYPOTHESIZED] provides the evaluation framework (scale-relative assessment)

---

## Further Reading

- [Self-Validating Systems (Zenodo)](https://zenodo.org/records/17616682)
- [Semantic Thermodynamics (Zenodo)](https://zenodo.org/records/17618208)
- [Empirical Thermodynamic Convergence (Zenodo)](https://zenodo.org/records/17618998)
