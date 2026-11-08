# Upstream Edits

**Project:** `K_SPECFORGE`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `sgl-project/SpecForge` @ `3cb0510f0bd0` (MIT)

## Applied patches

| Patch | Target | Kind | Behaviour change | Test |
| --- | --- | --- | --- | --- |
| `K_SPECFORGE-egress-001` | `UPSTREAM/specforge/_anticloud_egress.py` | behaviour | with ANTICLOUD_OFFLINE=1, any socket connection to a hosted frontier API raises EgressDenied instead of dialling out | `tests/upstream/test_egress_guard.py::test_frontier_host_denied_when_offline` |

Each patch is judged on behaviour, not on volume. A patch that only
writes to the ledger is not counted; `anticloud audit-edits` excludes it
and the project is reported as unimproved rather than as improved.
