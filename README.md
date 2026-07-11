# Coding Workflow

**Version 1.0.3**

A disciplined coding methodology that ensures every task is planned,
researched, built minimally, tested incrementally, and verified fully.

> "寫 code 前先想清楚，能搜就搜不重造輪子，寫一個測一個，
> 全部完成再全面驗證。"

---

## The Five Phases (Iterative)

| # | Phase | What You Do |
|---|-------|-------------|
| 1 | **Global Route Planning** | Plan architecture, data flow, files to touch, functions to create |
| 2 | **Ponytail + GitHub Search** | Search for existing code, apply ponytail ladder, build minimum |
| 3 | **Implementation** | Implement one module/block at a time |
| 4 | **Incremental Testing** | Test that module immediately — loop back to 3 for next block |
| 5 | **Full Verification** | All endpoints, all features, no regression, no dead code |

**Phase 3 and Phase 4 form an iterative loop:**
implement one → test it → pass → next module → fail → fix → retest → repeat
→ all done → Phase 5.

---

## Quick Start

Clone this repo and read `SKILL.md`:

```bash
git clone https://github.com/GangYuanFan/vibecode-workflow.git
cat SKILL.md
```

---

## Why This Workflow

- **Prevents over-engineering** — ponytail mindset keeps code minimal
- **Prevents rework** — search before building means no wasted effort
- **Catches bugs early** — test each unit before building the next
- **Ensures delivery quality** — full verification before sign-off

---

## License

MIT
