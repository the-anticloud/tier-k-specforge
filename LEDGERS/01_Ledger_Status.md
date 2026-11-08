# Ledger Status

**Project:** `K_SPECFORGE`  
**Tier:** TIER_4_INFERENCE_AGENTS  
**Identity:** Upstream `sgl-project/SpecForge` @ `3cb0510f0bd0` (MIT)

## Chain state

| Fact | Value |
| --- | --- |
| Upstream | `sgl-project/SpecForge` |
| Commit | `3cb0510f0bd0e8c195ac6e9c5c62f6b50580ff83` |
| Upstream licence | MIT |
| Licence class | permissive |
| Clone size | 8.31 MB |
| Ledger | 0 blocks, chain verified |
| Current TRL | NOT YET MEASURED |
| Post-optimisation TRL | NOT YET MEASURED |
| II budget cap | 1000.0 IIU |
| Verified upstream edits | 1 |

- Blocks: **0**
- Head digest: `None`
- Chain verification: **verified**

## Independent verification

The chain is verifiable without trusting this project's tooling:

```
anticloud ledger verify
anticloud ledger export > ledger.jsonl
```

Each block carries the previous block's digest, so removing or reordering an
entry invalidates every block after it. That property is the reason the
ledger can stand in for a claim of what happened.
