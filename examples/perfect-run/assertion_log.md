# [Phase 4] Logic Assertion Log - Example

## 🧪 Unit Verification: `getUserProfile()`

- **Test Case:** Valid User ID
- **Input:** `userId: "user_01"`
- **Expected Output:** `{ name: "Jerry", email: "jerry@example.com" }`
- **Actual Output:** `{ name: "Jerry", email: "jerry@example.com" }`
- **Verdict:** ✅ PASS

- **Test Case:** Non-existent User ID
- **Input:** `userId: "unknown"`
- **Expected Output:** `404 Not Found`
- **Actual Output:** `404 Not Found`
- **Verdict:** ✅ PASS

---
**Decision:** [PASS $\rightarrow$ Next Unit]
