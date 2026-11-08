# Deploy Guide — K_SPECFORGE
**Tier:** TIER_4_INFERENCE_AGENTS | **Stack:** Python 3.11, asyncio, PAX 27B, tree search (beam/MCTS), AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, asyncio (stdlib), PAX 27B weights (used for both generation and verification).

## Environment
24GB+ VRAM recommended (parallel PAX 27B calls). Can run with 16GB using sequential fallback.

## AIOSS Integration
```bash
aioss init --module K_SPECFORGE --output ./k_specforge.aioss
aioss append --chain ./k_specforge.aioss --payload ./output.bin --module K_SPECFORGE
aioss verify --chain ./k_specforge.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_SPECFORGE",
    aioss_chain="./K_SPECFORGE.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_SPECFORGE.aioss --verbose
python -m K_SPECFORGE.tests.smoke
```
