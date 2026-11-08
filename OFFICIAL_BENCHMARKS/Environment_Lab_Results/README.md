# Environment Lab Results — K_SPECFORGE
**Benchmark type:** Local static analysis (Bandit + Radon)
**Date:** 2026-10-01
**Note:** GPU inference metrics (tok/s, latency, KV cache) available only for T4-scanned projects.

## Static Analysis

| Tool | Metric | Value |
|------|--------|-------|
| Bandit | HIGH findings | 2 |
| Bandit | MEDIUM findings | 92 |
| Bandit | Status | ⚠️ fail |
| Radon CC | Avg complexity grade | 2.931781516478451 |
| Radon MI | Avg maintainability | None |

## Code Metrics

| Metric | Value |
|--------|-------|
| Python files | 358 |
| Python LOC (est.) | 53,438 |
| Total files | 950 |

## Anticloud Integration

This project's AIOSS integration layer (`aioss_integration.py`) uses SHA3-256
chain hashing for tamper-evident audit. See `SECURITY_PATCHES.md` for any upstream
Bandit findings documented and mitigated in the Anticloud wrapper.

---
*Anticloud FZ LLE | Apache-2.0 OR LicenseRef-Anticommons-Enterprise-1.0*
