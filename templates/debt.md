# Technical Debt Ledger (`DEBT.md`)

| Date | Module/Line | Shortcut Taken | Reason/Blocker | Upgrade Path (How to fix) | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 2026-07-12 | `utils/math.js:42` | Hardcoded timeout (5s) | API unstable, needed quick fix | Implement configurable timeout in `.env` | Low |
| 2026-07-12 | `api/user.js` | Skipped input validation | Prototype phase, trust internal call | Add Joi/Zod schema validation | High |

---
*Note: All `ponytail:` comments in code must have a corresponding entry here.*
