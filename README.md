# Marco Barreto

**Independent Researcher, F51 Labs — Montreal, QC**

[![ORCID](https://img.shields.io/badge/ORCID-0009--0003--4477--6863-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0003-4477-6863)
[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.21726235-blue?style=flat)](https://doi.org/10.5281/zenodo.21726235)
[![License](https://img.shields.io/badge/paper-CC--BY--4.0-lightgrey?style=flat)](https://creativecommons.org/licenses/by/4.0/)

---

## Research

### Refuse, Don't Report: Three Integrity Gates for Self-Modifying ML Systems

**Published 2026-07-31** — Zenodo · DOI [`10.5281/zenodo.21726235`](https://doi.org/10.5281/zenodo.21726235) · CC-BY-4.0 · 25 references

Instrumented machine-learning systems detect anomalies and then produce a result anyway.
This paper takes the opposite stance: **refuse to emit**.

Three integrity gates are described and empirically validated on a 1.7B-parameter model:

| Gate | Mechanism |
|---|---|
| **Memory organ** | Refuses snapshots with mismatched digests or diverged key-encoders |
| **Transplant ledger** | Blocks weight records without provenance certificates or with measured drift |
| **Ablation harness** | Emits no artifact when arms disagree on seed, cursor, checkpoint, or contract |

**Key empirical result:** Information transferred into a model is not reachable in that model's
coordinate space. A cross-lineage FFN graft scored 11.2166 against 11.2163 for norm-matched noise,
despite the learned router opening its gate to 0.773 for the real donor and 0.015 for noise.
Sixteen facts installed by rank-1 edit yielded three, while prefixing every unrelated answer
with the same attractor. Routers and edits both worked. Both failed at **addressability**.

The entire paper is reproducible from the
[F51-Darwin-SSD](https://github.com/marcobarreto007/F51-Darwin-SSD) repository.
Every figure and number is produced by a script under `src/tools/` or `research/`.

**Keywords:** machine learning, verification, provenance, model editing, reproducibility,
integrity, self-modifying systems, ablation.

---

## Active Systems

### MIKE — Local AI Assistant (Production)

Personal household AI assistant running a single Qwen3.6-35B-A3B GGUF model
(18.2 GB, UD-IQ4_XS quantization) via `llama-server`. Hybrid CPU/GPU offload
on an RTX 2070 (8 GB VRAM, 24+ GB system RAM). Dense layers on GPU, MoE
experts on CPU.

- 186 tools across 18 MCP servers
- 54 loaded skills
- SQLite + Mem0 + LightRAG memory stack
- Gmail, Google Calendar, Google Drive, and local email via OAuth
- Full autonomy and governance runtime
- 234 unit tests passing (2026-07-30)

Stack: FastAPI, llama.cpp, Qwen GGUF, JavaScript PWA dashboard.

### VeriBay — Evidence-Guided Automotive Diagnostics

Bilingual (EN/FR) multi-brand diagnostic CDF system for workshops. Local AI
runtime with extensive tool surface: 50-entry KB with BM25 + optional dense
RAG, Tesseract OCR, llama.cpp multimodal vision, and PostgreSQL canonical
storage. 25 HTTP routes (FastAPI). Deterministic IRS MeF-inspired classification
engine with VB-* rules, regex catalogs, and five approved sources. Mike LoRA
v4 text adapter trained and exported to GGUF.

Stack: FastAPI 0.115, asyncpg + SQLAlchemy async, DuckDB 1.2, llama-cpp-python,
Playwright E2E/accessibility/visual testing.

---

## Projects

| Project | Description | Key Stack |
|---|---|---|
| [F51-Darwin-SSD](https://github.com/marcobarreto007/F51-Darwin-SSD) | Cryptographic neuron catalog, ROME/MEMIT surgical editing, hash-verified rollback. 196K neurons stamped, 136 tests. | PyTorch 2.13, safetensors, transformers 5.14 |
| [CompilAI](https://github.com/marcobarreto007/compilai-local) | Automated TMC video analysis. YOLO detection, BoT-SORT tracking, geometric calibration. | Flask 3.0, OpenCV 4.9, scikit-learn 1.5, EasyOCR |
| [NelsonMath](https://github.com/marcobarreto007/nelsonmath) | Multi-strategy math reasoning pipeline. Candidate scoring, adversarial checking, diversity paths, optional Wolfram verification. | PyTorch 2.0+, SymPy 1.12, exllamav2, llama-cpp-python |
| [F51 Labs](https://github.com/marcobarreto007/f51-labs) | Game generation R&D. Multi-node pipeline: brain (LangGraph), artist (ComfyUI), coder, runner. | LangGraph 0.2, ChromaDB 0.5, Pygame CE 2.5 |
| [Xubuget](https://github.com/marcobarreto007/xubuget) | Personal budget app for Android. | Kotlin 2.2, Jetpack Compose, KSP |

---

## Technical Principles

- **Local-first.** No model leaves local hardware. Inference, training, and data stay on-premises.
- **Deterministic verification.** Every critical pipeline includes hash-based cataloging, deterministic tests, and exact rollback capabilities.
- **Consumer hardware.** RTX 2070 with 8 GB VRAM. If it cannot run here, the architecture is wrong.
- **llama.cpp, not Ollama.** Direct control over quantization, context size, GPU offload layers, and the full GGUF runtime.
- **Refuse, don't report.** Integrity checks should block emission, not annotate it after the fact.

---

## Languages

Python (primary) · Kotlin (Android) · TypeScript / JavaScript (frontend tooling) · English · French · Brazilian Portuguese

---

*F51 Labs — Montreal, QC. Nothing goes to the cloud unless strictly necessary.*
