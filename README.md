# Marco Barreto

**Independent Researcher, F51 Darwin-X Laboratory, Montreal — local-only operation**

[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--4477--6863-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-4477-6863)
[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21726235-blue?style=flat)](https://doi.org/10.5281/zenodo.21726235)

---

## Research

### Refuse, Don't Report: Three Integrity Gates for Self-Modifying ML Systems

Published 2026-07-31 — Zenodo · DOI [`10.5281/zenodo.21726235`](https://doi.org/10.5281/zenodo.21726235) · CC-BY-4.0

Three integrity gates — memory organ, transplant ledger, ablation harness —
that refuse to emit artifacts when checks fail. Validated on 1.7B-parameter
models. Finding: information transferred into a model is not reachable in that
model's coordinate space.

### Prefix State Reuse in a Hybrid SSD/Attention Model: A Correctness-First Measurement

August 2026 — Technical report · [`F51-Darwin-SSD`](https://github.com/marcobarreto007/F51-Darwin-SSD)

A correctness-gated measurement of prefix state reuse in a hybrid Selective-State-Space + attention
architecture (153M–517M params, RTX 5060 Ti). Three findings: (1) PyTorch's `is_causal=True` silently
discards the cached prefix when `k_len > q_len` — a silent correctness bug; (2) with an absolute-position
mask, reuse is numerically exact (max |Δlogit| ≤ 2e-6, KL ≤ 4.7e-7); (3) speedup is scale-dependent:
null at 153M, **4.3×–18× at 517M** under a parity gate with negative control.

---

## Active Systems

| System | Description | Stack |
|---|---|---|
| [MIKE](https://github.com/marcobarreto007/mike) | Local AI assistant. Qwen3.6-35B-A3B via llama.cpp. 186 tools, 54 skills, 18 MCP servers. | FastAPI, llama.cpp, Mem0, LightRAG |
| [Epreuve](https://github.com/marcobarreto007/epreuve) | Evidence-guided automotive diagnostics. Bilingual EN/FR. 25 HTTP routes, 50-entry KB, RAG + OCR. | FastAPI, PostgreSQL, DuckDB, llama.cpp |

## Repositories

| Repository | Description |
|---|---|
| [F51-Darwin-SSD](https://github.com/marcobarreto007/F51-Darwin-SSD) | Hybrid SSD/Attention model. Parity-gated benchmarks. Cryptographic neuron catalog. |
| [nelsonmath](https://github.com/marcobarreto007/nelsonmath) | Multi-strategy math reasoning. Bayesian scoring, adversarial critique, Wolfram. |
| [f51-labs](https://github.com/marcobarreto007/f51-labs) | Game generation pipeline. LangGraph multi-node: brain, artist, coder, runner. |

## Technical Principles

- **Local-first.** No model leaves local hardware. Inference stays on-premises.
- **Deterministic verification.** Hash-based cataloging, parity gates, negative controls.
- **Consumer hardware.** RTX 2070 / RTX 5060 Ti. No cloud GPU rental.
- **llama.cpp, not Ollama.** Full control over quantization and GPU offload.
- **Correctness-first.** Every speedup figure gated on output equivalence.

---

F51 Darwin-X Laboratory — Montreal, QC
