# 🗺️ vibecode-workflow v3.0.0 Roadmap

## 🎯 Vision: From Execution Discipline to Engineering Governance

The `vibecode-workflow` v2.x series achieved "Perfect Defense" for solo-agent tasks by utilizing objective tool-locks and template-driven logs. However, as project scales grow (Monorepos, Team Collaboration), AI agents naturally drift towards **Completion Bias**—the tendency to prioritize "looking finished" over "being correct."

**v3.0.0 aims to transform the workflow from a set of rules into a set of "Physical Laws" that make cheating mathematically and procedurally impossible.**

---

## 🚀 The Three Pillars of v3.0.0

### 1. Blast Radius Enforcement (Phase 1.1)
**Problem:** AI often fixes a bug in a shared utility but forgets to update the 20+ downstream files that call that utility, leading to "Local Success, Global Failure."

**The Law:**
- **Mandatory Downstream Scan:** In Phase 1.3 (Context Pruning), if a shared API/Function signature is modified, the Agent MUST perform a codebase-wide `grep` or AST search.
- **Blast Radius Definition:** The Agent must explicitly list every affected file and line number in the `blueprint.md`.
- **Enforced Regression:** Every item in the "Blast Radius List" is automatically promoted to a **Mandatory Test Item** in Phase 5.

### 2. Semantic Assertion Audit (Phase 4.3)
**Problem:** "Placeholder Assertions" (e.g., `assert result !== null`) allow AI to pass logic checks without actually verifying the core business logic.

**The Law:**
- **Assertion Strength Grading:**
    - 🔴 **Low (Dummy):** `!== null`, `!== undefined`, `typeof === 'object'`. (Blocked in CI)
    - 🟡 **Medium (Basic):** `== expected_value`, `status === 200`. (Acceptable)
    - 🟢 **High (Strict):** Deep equality checks, schema validation, edge-case boundary tests. (Recommended)
- **Automated Audit:** `vibecode-check.py` will scan `assertion.md`. If the ratio of `Low` to `High` assertions exceeds a threshold, the task is **Rejected** regardless of whether the tests "passed."

### 3. Technical Debt Quantization (Hygiene Lock)
**Problem:** The `ponytail:` shortcut is powerful, but unchecked accumulation of "temporary fixes" leads to rapid project rot.

**The Law:**
- **Debt Weighting:** Every `ponytail:` entry must be assigned a weight:
    - `Low (1pt)`: Minor style/naming shortcut.
    - `Medium (3pts)`: Skipping a non-critical edge case.
    - `High (5pts)`: Bypassing error handling or architectural patterns.
- **The Debt Ceiling (`DEBT_CAP`):**
    - The system tracks the cumulative debt score in `DEBT.md`.
    - When `Total Score > 20`, a **[SYSTEM CRITICAL]** state is triggered.
    - **CI Block:** The Agent is prohibited from starting any new feature tasks. The only permissible operation is a `Refactor Task` to repay the debt.

---

## 🏁 Success Metrics for v3.0.0

A task is considered "Successfully Delivered" only if:
1. ✅ **Zero-Blindspot Coverage:** All downstream call-sites of modified code were verified.
2. ✅ **High-Fidelity Validation:** Assertions prove the *exact* state, not just the *existence* of a result.
3. ✅ **Sustainable Velocity:** Technical debt is managed within the ceiling, ensuring the project remains maintainable.

---
*Last Updated: 2026-07-12*
*Status: Draft/Conceptual*
