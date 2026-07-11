# vibecode-workflow v2.0.0

**The AI Agent Absolute Defense Circle (AI Agent 絕對防禦圈)**

A disciplined, enterprise-grade coding methodology designed to tame AI laziness, prevent "hallucination-driven development," and ensure production-ready stability.

> "不准偷跑、不准幻覺、不准鬼打牆。每一行代碼都必須經過規劃 $\rightarrow$ 搜尋 $\rightarrow$ 實作 $\rightarrow$ 斷言 $\rightarrow$ 驗證。"

---

## 🛡️ The 4-Layer Defense Architecture

v2.0.0 transforms the workflow from a "guideline" into a "strict protocol" using four layers of constraints:

### 1. 防偷跑 (State Lock)
Prevents the AI from jumping straight to implementation.
- **Status Tagging**: Every response MUST start with `[CURRENT_PHASE: X]`.
- **Hard Gating**: No advancement to Phase $N+1$ without explicit user approval.
- **Zero-Code Lock**: Absolute prohibition of implementation code in Phases 1 & 2.

### 2. 防失控 (Stability Lock)
Ensures the code actually works and doesn't break the system.
- **Impact Analysis**: Pre-emptive assessment of regressions in shared utilities.
- **Logic Assertions**: Replaces simple syntax checks with "Expected Output" verification.
- **Circuit Breaker**: Mandatory rollback to Phase 1 after 3 consecutive test failures.

### 3. 防稀釋 (Attention Lock)
Maintains LLM focus in large-scale projects.
- **Context Pruning**: Explicit definition of the absolute minimum file-set.
- **Noise Reduction**: Mandatory exclusion of irrelevant files to prevent attention dilution.

### 4. 防腐蝕 (Hygiene Lock)
Ensures long-term maintainability and clean history.
- **Micro-Commits**: One logical unit per response $\rightarrow$ STOP $\rightarrow$ Test.
- **Commit Hygiene**: Single-purpose commits following standard conventions (`feat:`, `fix:`).
- **Technical Debt Ledger**: Mandatory logging of all Ponytail shortcuts in `DEBT.md`.

---

## 🔄 The Five Phases (Iterative)

| Phase | Name | Core Objective | Key Constraint |
|---|---|---|---|
| **0** | **State Machine** | Establish Context | `[CURRENT_PHASE: X]` tagging |
| **1** | **Global Route Planning** | Architecture & Impact | **Zero-Code Lock** + Sign-off Blueprint |
| **2** | **Ponytail + Search** | Minimalist Discovery | **Tool-use Enforcement** (Search logs) |
| **3** | **Implementation** | Atomic Development | **Micro-Commit Rule** (1 unit $\rightarrow$ STOP) |
| **4** | **Incremental Testing** | Logic Verification | **Logic Assertions** (Expected Output) |
| **5** | **Full Verification** | System Sign-off | **Debt Ledger** + Commit Hygiene |

**Phase 3 $\leftrightarrow$ Phase 4 Loop**: Implement one $\rightarrow$ Assert $\rightarrow$ Pass $\rightarrow$ Next. Fail $\rightarrow$ Fix $\rightarrow$ Retest. (3 fails $\rightarrow$ Circuit Breaker $\rightarrow$ Phase 1).

---

## 🚀 Quick Start

Clone this repo and integrate `SKILL.md` into your AI Agent's system prompt or knowledge base:

```bash
git clone https://github.com/GangYuanFan/vibecode-workflow.git
# Read SKILL.md to internalize the protocol
cat SKILL.md
```

---

## 🏆 Why v2.0.0?

Most AI agents suffer from **"The Completion Bias"** — the urge to provide a complete answer immediately, regardless of correctness. `vibecode-workflow` replaces this bias with **"Engineering Discipline"**:

- **From "It looks right" $\rightarrow$ "It is asserted right"** (Logic Assertions).
- **From "I'll fix it later" $\rightarrow$ "It is logged in DEBT.md"** (Debt Ledger).
- **From "Let me try again" $\rightarrow$ "I must rethink the architecture"** (Circuit Breaker).

---

## License

MIT
