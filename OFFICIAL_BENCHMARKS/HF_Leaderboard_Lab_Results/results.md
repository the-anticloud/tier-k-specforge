# HF_Leaderboard_Lab_Results

**Project:** `K_SPECFORGE`  
**Tier:** `TIER_4_INFERENCE_AGENTS`  
**Slug:** `sgl-project/SpecForge`  
**Commit:** `3cb0510f0bd0`  
**Run:** `2026-09-30T15:07:07.146295+00:00`  

## Isolation Environment

| Field | Value |
| ----- | ----- |
| Platform | `win32` |
| Python | `3.12.10` |
| HF model | `distilbert-base-uncased` |
| HF load time | `4.42s` |
| Inference device | `cpu` |

## Results

**Framework:** [HuggingFace Open LLM Leaderboard (proxy via distilbert-base-uncased)](https://huggingface.co/docs/leaderboards/en/open_llm_leaderboard/archive)

**Model used:** `distilbert-base-uncased`

### Inference Latency (Classification)

| Metric | Value |
| ------ | ----- |
| Avg latency | **48.98 ms** |
| Min latency | 42.49 ms |
| Max latency | 55.82 ms |
| Samples | 5 |

### Real Tokenization Results

| Field | Value |
| ----- | ----- |
| Token count | **38** |
| Tokenization latency | 1.0 ms |
| Classification label | `LABEL_0` |
| Classification score | 0.5861 |
| Classification latency | 73.98 ms |
| Status | **PASS** |

**Input text tokenized:**
```
K_SPECFORGE (sgl-project/SpecForge) — 617 files, 98259 source lines, licence MIT, primary language ['Python']
```

**First 20 tokens:**
```
['[CLS]', 'k', '_', 'spec', '##for', '##ge', '(', 'sg', '##l', '-', 'project', '/', 'spec', '##for', '##ge', ')', '—', '61', '##7', 'files']
```

> Full MMLU/HellaSwag/TruthfulQA/ARC/Winogrande/GSM8K require dedicated GPU.
> These results are CPU inference proxy metrics using distilbert-base-uncased.

---
_Anticloud Benchmark Suite — isolation log — 2026-09-30T15:07:07.146295+00:00_