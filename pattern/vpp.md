# V++ — Selection and Validation Loop

V++ defines how learning occurs inside the metapattern.

It is not an optimization heuristic.
It is a **selection mechanism**.

Only validated work is allowed to persist.

---

## 1. Why V++ Exists

Without explicit validation, systems drift.

They may:
- appear productive
- accumulate complexity
- converge internally

…but fail to improve.

V++ introduces a mandatory selection gate after every transformation cycle.

---

## 2. The V++ Increment

Each completed Φ₁–Φ₅ cycle ends with a validation decision.

If validation succeeds, the version increments:

```
V → V+1  (V++)
```

If validation fails:
- the output is rejected
- the version does not increment
- the process returns to the appropriate phase

Progress is defined by validated increments, not by activity.

---

## 3. Validation Criteria

Validation answers three questions:

1. **Does it work?**
2. **Does it match the intention?**
3. **Does it respect the constraints?**

All three must be satisfied.

If any answer is negative, validation fails.

---

## 4. Auditability

For validation to be meaningful, the process must be auditable.

At minimum, an auditable cycle supports:

- **replay()** — reconstruct how the output was produced
- **diff()** — compare versions meaningfully
- **explain()** — justify why decisions were made

Work that cannot be replayed, diffed, or explained cannot learn.

---

## 5. Selection Pressure

V++ introduces selection pressure by design.

- Not all outputs survive
- Not all iterations count
- Only validated changes persist

This prevents:
- silent degradation
- uncontrolled accumulation
- false convergence

---

## 6. Cumulative Improvement

Because versions increment only after validation:

- improvements accumulate
- regressions are detectable
- learning becomes traceable

V++ enables systems to improve without centralized control.

---

## 7. Minimal Implementation

A minimal V++ implementation requires only:

- explicit intention and constraints (Φ₁)
- a recorded output (Φ₅)
- a validation decision

Everything else scales from there.

---

## 8. Canonical Role

V++ is inseparable from the metapattern.

Without V++:
- recursion becomes noise
- iteration becomes motion without progress

With V++:
- learning is enforced
- evolution is possible

V++ defines when a transformation **counts**.
