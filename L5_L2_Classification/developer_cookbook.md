# Developer Cookbook — K_SPECFORGE
**Stack:** Python 3.11, asyncio, PAX 27B, tree search (beam/MCTS), AIOSS_FORMAT
**Domain:** Speculative execution forge: parallel hypothesis generation for PAX 27B multi-path reasoning

## Multi-hypothesis generation
```python
from k_specforge import SpecForge

forge = SpecForge(
    pax_model="./pax-27b-q4.gguf",
    n_hypotheses=5,
    aioss_chain="./specforge.aioss"
)

result = forge.generate(
    query="Differential diagnosis for irregular EEG pattern: high theta, low alpha",
    domain="clinical",
    max_tokens_per_hypothesis=128
)

print("SELECTED:", result.best_hypothesis.text)
print(f"Confidence: {result.best_hypothesis.score:.2f}")
print("All hypotheses:")
for i, h in enumerate(result.all_hypotheses):
    print(f"  [{i+1}] ({h.score:.2f}) {h.text[:80]}")
print(f"Chain: {result.chain_hash}")
```

## Beam search reasoning
```python
result = forge.beam_search(
    query="Optimal navigation path for robot in dynamic environment",
    beam_width=4, depth=3
)
print(result.best_path)
```

## Tune hypothesis diversity
```python
forge.set_config(temperature=0.8, top_p=0.9, diversity_penalty=0.3)
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
