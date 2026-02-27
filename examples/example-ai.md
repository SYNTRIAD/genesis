# Example — AI Task Using the Metapattern

This example demonstrates how the metapattern structures an AI-assisted task.

The goal is not to showcase a specific model or tool, but to show how human-AI collaboration becomes **auditable, repeatable, and improvable** using Φ₁–Φ₅, UPS, and V++.

---

## Context

A developer needs to refactor a legacy authentication module.
They use an AI assistant to accelerate the work.

Without structure, the interaction tends toward:
- vague prompts
- unverifiable outputs
- accumulated drift across iterations

The metapattern prevents this.

---

## Φ₁ — INTAKE

### STATE

The current authentication module:
- uses session-based auth with server-side state
- has no token refresh mechanism
- mixes auth logic with route handlers
- has 3 known CVEs in dependencies

The codebase is Python (FastAPI), ~2400 LOC in `auth/`.

---

### INTENTION

Migrate to stateless JWT-based authentication with:
- access + refresh token pair
- separated auth logic (middleware, not inline)
- dependency updates resolving all known CVEs

---

### CONSTRAINTS

- No changes to existing API contracts (request/response shapes)
- Must pass all existing integration tests
- Migration must be incremental (no big-bang rewrite)
- AI-generated code must be reviewed before merge

---

## Φ₂ — DECOMPOSE

### DECOMPOSITION

The task breaks into five atomic parts:

1. **Token schema** — Define JWT payload, expiry, signing
2. **Auth middleware** — Extract auth logic from route handlers
3. **Token endpoints** — `/login`, `/refresh`, `/logout`
4. **Dependency update** — Resolve CVEs, pin versions
5. **Migration path** — Dual-mode (session + JWT) during transition

Each part can be prompted, generated, and validated independently.

---

## Φ₃ — UNTANGLE

### DEPENDENCIES

```
Token schema (1)
  ↓
Auth middleware (2) ← depends on schema
  ↓
Token endpoints (3) ← depends on middleware
  ↓
Migration path (5) ← depends on endpoints working
  
Dependency update (4) ← independent, can run in parallel
```

Execution order: 1 → 2 → 3 → 5, with 4 in parallel.

---

## Φ₄ — TRANSFORM

### TRANSFORMATION

Each part follows the same interaction cycle with the AI:

**Part 1 — Token schema:**
- **P:** Prompt the AI to generate JWT schema options (symmetric vs asymmetric, claim structure, expiry strategy)
- **V:** Select the option that fits constraints. Reject options that change API contracts.

**Part 2 — Auth middleware:**
- **P:** Prompt the AI to extract auth logic from 3 route files into a middleware module
- **V:** Verify that routes still pass tests with the new middleware. Reject if any test fails.

**Part 3 — Token endpoints:**
- **P:** Prompt the AI to generate `/login`, `/refresh`, `/logout` endpoints
- **V:** Validate against OpenAPI spec. Verify refresh rotation works. Reject if token reuse is possible.

**Part 4 — Dependency update:**
- **P:** Prompt the AI to audit `requirements.txt` against CVE databases
- **V:** Verify all CVEs resolved. Run full test suite against updated dependencies.

**Part 5 — Migration path:**
- **P:** Prompt the AI to design a dual-mode auth layer (accept both session and JWT)
- **V:** Validate that existing clients work unchanged. Verify new clients can use JWT exclusively.

At each step, the AI generates (P), the human validates (V).
No output persists without explicit validation.

---

## Φ₅ — OUTPUT

### OUTPUT

The result:
- JWT auth module: `auth/jwt.py`, `auth/middleware.py`, `auth/endpoints.py`
- Updated `requirements.txt` with all CVEs resolved
- Dual-mode migration layer with feature flag
- All 47 existing integration tests pass
- 12 new tests covering JWT-specific flows

---

### VALIDATION (V++)

Validation questions:

- Does the new auth module work? **Yes** — all tests pass.
- Does it match the intention? **Yes** — stateless JWT, separated logic, CVEs resolved.
- Does it respect the constraints? **Yes** — no API changes, incremental migration, all AI output reviewed.

**Version incremented (V++).**

---

## What the Pattern Added

Without the metapattern, this task would likely have been:
- a single long prompt ("refactor my auth to use JWT")
- an unstructured back-and-forth
- no clear validation criteria
- no audit trail

With the metapattern:
- each step is independently verifiable
- the AI's role is bounded (generate, not decide)
- the human's role is explicit (validate, not hope)
- the entire process is replayable

The AI is a P-engine.
The human is the V-gate.
Together they form `Ω = P ↔ V`.

---

## Recursion Note

Part 2 (auth middleware extraction) could itself be decomposed into a Φ₁–Φ₅ cycle:
- Φ₁: Which routes contain auth logic?
- Φ₂: What are the distinct auth patterns?
- Φ₃: In what order should they be extracted?
- Φ₄: Extract each pattern
- Φ₅: Validate each extraction independently

Recursion stops when the extraction becomes a single, trivially verifiable change.
