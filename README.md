# Marco Barreto

**Independent Researcher, F51 Labs — Montreal, QC**

[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--4477--6863-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-4477-6863)
[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21726235-blue?style=flat)](https://doi.org/10.5281/zenodo.21726235)

---

## Research

**Refuse, Don't Report: Three Integrity Gates for Self-Modifying ML Systems**

Published 2026-07-31 — Zenodo · DOI [`10.5281/zenodo.21726235`](https://doi.org/10.5281/zenodo.21726235) · CC-BY-4.0 · 25 references

Three integrity gates for ML systems that refuse to emit when checks fail,
validated on 1.7B-parameter models. Key finding: information transferred
into a model is not reachable in that model's coordinate space.

---

## Active Systems

| System | Description | Stack |
|---|---|---|
| [MIKE](https://github.com/marcobarreto007/mike) | Local AI assistant. Qwen3.6-35B-A3B via llama.cpp. 186 tools, 54 skills, 18 MCP servers. | FastAPI, llama.cpp, Mem0, LightRAG |
| [Épreuve](https://github.com/marcobarreto007/Épreuve) | Evidence-guided automotive diagnostics. Bilingual EN/FR. 25 HTTP routes, 50-entry KB. | FastAPI, PostgreSQL, DuckDB, RAG, OCR |

## Repositories

| Repository | Description |
|---|---|
| [F51-Darwin-SSD](https://github.com/marcobarreto007/F51-Darwin-SSD) | Cryptographic neuron catalog, ROME/MEMIT editing, hash-verified rollback. |
| [nelsonmath](https://github.com/marcobarreto007/nelsonmath) | Multi-strategy math reasoning. Bayesian scoring, adversarial critique, Wolfram. |
| [f51-labs](https://github.com/marcobarreto007/f51-labs) | Game generation pipeline. LangGraph multi-node: brain, artist, coder, runner. |

## Technical Principles

- **Local-first.** No model leaves local hardware.
- **Deterministic verification.** Hash-based cataloging, exact rollback.
- **Consumer hardware.** RTX 2070, 8 GB VRAM.
- **llama.cpp, not Ollama.** Full control over quantization and GPU offload.
- **Refuse, don't report.** Integrity gates block emission, not annotate it.

---

F51 Labs — Montreal, QC
