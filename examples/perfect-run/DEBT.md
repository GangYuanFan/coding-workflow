# Technical Debt Ledger

| Date | Module/Line | Shortcut Taken | Reason/Blocker | Upgrade Path | Priority |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 2026-07-12 | `user_service.js:12` | Used `findOne()` without projection | Quick prototype | Implement projection to return only needed fields | Low |
