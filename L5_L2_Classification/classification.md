# L5 Narrow / L2 General Classification — K_SPECFORGE
**Platform:** Anticloud | **Tier:** TIER_4_INFERENCE_AGENTS | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_SPECFORGE generates multiple reasoning hypotheses in parallel using PAX 27B and selects the best via a verifier. Narrow scope: Anticloud domain multi-path reasoning — clinical differential diagnosis, robotics path planning alternatives, security threat hypothesis ranking.

## L2 General
L2 General: K_SPECFORGE's parallel hypothesis generation improves answer quality across all tiers requiring multi-option reasoning. Same engine for clinical differentials and robotics path alternatives.

## PAX 27B Integration
PAX 27B generates all hypothesis branches in parallel. K_SPECFORGE's verifier (also PAX 27B) scores each hypothesis against evidence and selects the highest-confidence conclusion. All branches are AIOSS-chained.

## AIOSS Audit Chain
Every speculation run (query hash + hypotheses count + all branch hashes + selected branch hash + verifier score) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
NIST AI RMF 1.0 (reliable AI). ISO/IEC 42001 (AI system robustness).
