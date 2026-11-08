# 3-Seed Simulation — K_SPECFORGE

**Seeds:** `59319` · `90656` · `24855`

**Seed method:** `sha256("K_SPECFORGE")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `K_SPECFORGE`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 6.972 | 0.1737 | ±0.3405 |
| throughput_tokens_per_sec | 1826.3333 | 23.7981 | ±46.6443 |
| p50_latency_ms | 45.88 | 4.4566 | ±8.7349 |
| p99_latency_ms | 110.65 | 12.6541 | ±24.802 |
| ttft_ms | 26.8667 | 1.2422 | ±2.4347 |
| mmlu_proxy | 0.7509 | 0.0304 | ±0.0596 |
| hellaswag_proxy | 0.7887 | 0.0254 | ±0.0498 |
| truthfulqa_proxy | 0.5639 | 0.0515 | ±0.1009 |
| arc_proxy | 0.7102 | 0.0388 | ±0.076 |
| complexity_cyclomatic | 4.74 | 0.2922 | ±0.5727 |
| maintainability_index | 71.7233 | 4.3653 | ±8.556 |
| security_issues_high | 0.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 76.5 | 7.9314 | ±15.5455 |
| test_coverage_pct | 53.8667 | 3.7748 | ±7.3986 |
| doc_coverage_pct | 70.6667 | 5.9779 | ±11.7167 |
| memory_mb | 65.0 | 4.0849 | ±8.0064 |
| gpu_util_pct | 66.8 | 5.487 | ±10.7545 |
| openssf_score | 6.47 | 0.6375 | ±1.2495 |
| eu_ai_act_compliance_pct | 80.0667 | 6.3908 | ±12.526 |
| slsa_level | 1.6667 | 0.4714 | ±0.9239 |

## Per-Seed Raw Results

| Metric | Seed 59319 | Seed 90656 | Seed 24855 |
|--------|------------|------------|------------|
| trl_score | 7.079 | 7.11 | 6.727 |
| throughput_tokens_per_sec | 1859.5 | 1804.8 | 1814.7 |
| p50_latency_ms | 52.17 | 42.39 | 43.08 |
| p99_latency_ms | 117.95 | 121.15 | 92.85 |
| ttft_ms | 25.49 | 28.5 | 26.61 |
| mmlu_proxy | 0.7724 | 0.7723 | 0.7079 |
| hellaswag_proxy | 0.7919 | 0.7561 | 0.818 |
| truthfulqa_proxy | 0.544 | 0.5132 | 0.6345 |
| arc_proxy | 0.6556 | 0.7418 | 0.7333 |
| complexity_cyclomatic | 4.99 | 4.9 | 4.33 |
| maintainability_index | 74.78 | 65.55 | 74.84 |
| security_issues_high | 0 | 0 | 1 |
| dependency_freshness_pct | 87.5 | 72.9 | 69.1 |
| test_coverage_pct | 51.4 | 51.0 | 59.2 |
| doc_coverage_pct | 72.2 | 77.1 | 62.7 |
| memory_mb | 64.8 | 60.1 | 70.1 |
| gpu_util_pct | 66.2 | 60.4 | 73.8 |
| openssf_score | 7.23 | 6.51 | 5.67 |
| eu_ai_act_compliance_pct | 89.1 | 75.3 | 75.8 |
| slsa_level | 2 | 2 | 1 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._