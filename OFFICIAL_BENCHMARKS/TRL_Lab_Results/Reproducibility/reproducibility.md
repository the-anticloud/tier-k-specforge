# Reproducibility Record: TRL_Lab_Results

**Project:** `K_SPECFORGE`  
**Benchmark:** `TRL_Lab_Results`  
**Run:** `2026-09-30T15:11:19.033679+00:00`  
**Based on:** [HELM reproducibility principles](https://github.com/stanford-crfm/helm)

## Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| OS | `nt` |

## Inputs

| Field | Value |
| ----- | ----- |
| Slug | `sgl-project/SpecForge` |
| Commit | `3cb0510f0bd0` |
| Tracked files | `617` |
| Source lines | `98259` |
| Licence | `MIT` |
| Inputs SHA256 | `c87d51c7c81d0976...` |

## Outputs

| Field | Value |
| ----- | ----- |
| Results file | `TIER_4_INFERENCE_AGENTS\K_SPECFORGE\OFFICIAL_BENCHMARKS\TRL_Lab_Results\results.json` |
| Results SHA256 | `ce07a7bcd8c75a2b...` |

## Reproduction Steps

- 1. Clone Anticloud at commit HEAD
- 2. Ensure E:\fenta\Downloads\The Anticloud is present
- 3. Run: python run_benchmarks_comprehensive.py
- 4. Run: python write_benchmark_subfolders.py
- 5. Run: python write_ledgers_repro_extra_benchmarks.py
- 6. Verify results_sha256 matches sha256(OFFICIAL_BENCHMARKS/TRL_Lab_Results/results.json)

## Notes

TRL/OSINT/OWASP/SOC2/ISO27001/MITRE/NIST use static code analysis. HF uses live CPU inference.

---
_Anticloud Reproducibility Standard v1 — 2026-09-30T15:11:19.033679+00:00_