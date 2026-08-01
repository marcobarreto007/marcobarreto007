# Marco Barreto

**Local-first AI systems. Inference on consumer hardware. Zero cloud dependency.**

---

## Current Work

I build and operate personal AI infrastructure that runs entirely on a Windows desktop
with a single RTX 2070 (8 GB VRAM). The stack is llama.cpp, PyTorch, and FastAPI.
No Ollama. No cloud GPU rental. Every component is designed to work offline and
stay under local hardware constraints.

### Active production system: MIKE

MIKE is a local AI assistant serving my household. It runs a single
Qwen3.6-35B-A3B GGUF model (18.2 GB, UD-IQ4_XS quantization) via `llama-server`
with hybrid CPU/GPU offload — the dense layers live on GPU, MoE experts on CPU.

It exposes 186 tools across 18 MCP servers, loads 54 skills, and integrates
Gmail, Google Calendar, Google Drive, and local email through OAuth. Memory is
SQLite + Mem0 + LightRAG. Autonomy and governance are baked into the runtime.
234 unit tests passing as of July 30, 2026.

---

## Research Projects

### F51 Darwin-X — Cryptographic Circuit Catalog

A pipeline for cataloging every neuron in a transformer with SHA-256 hashes,
performing surgical knowledge editing via ROME and MEMIT, and proving that
nothing else changed through exact hash-verified rollback. 196,608 neurons
stamped. 136 tests passing. Runs on 2 consumer GPUs.

Stack: PyTorch 2.13, safetensors, tokenizers, transformers 5.14, numpy 2.5,
pytest 9.1. Python 3.12.

### VeriBay — Evidence-Guided Automotive Diagnostics

A bilingual (EN/FR) multi-brand diagnostic CDF system for workshops. Built on a
local AI runtime using its own tools: knowledge base with 50 indexed entries,
BM25 + optional dense RAG retrieval, OCR via Tesseract, local vision through
llama.cpp multimodal handlers, and PostgreSQL canonical storage.

25 HTTP routes (FastAPI). Deterministic IRS MeF-inspired classification engine
with VB-* rules, regex catalogs, and five approved sources. Mike LoRA v4 text
adapter trained and exported to GGUF; vision adapter in progress.

Stack: FastAPI 0.115, PostgreSQL (asyncpg + SQLAlchemy async), DuckDB 1.2,
llama-cpp-python, Playwright for E2E/accessibility/visual testing.

### CompilAI — Automated TMC Video Analysis

Turning Movement Count engine for traffic engineering. YOLO-based detection,
BoT-SORT tracking, geometric calibration, and reporting (Excel, PDF, CSV).
Optional VLM grounding pipeline and copilot training modules.

Stack: Flask 3.0, OpenCV 4.9, scikit-learn 1.5, pandas 2.2, EasyOCR,
CairoSVG, Shapely. Python 3.12.

### NelsonMath — Mathematical Reasoning Pipeline

Experimental multi-strategy reasoning system for competition-style math problems.
Candidate generation and scoring, adversarial checking, diversity-ensured
reasoning paths, and optional Wolfram symbolic verification.

Stack: PyTorch 2.0+, transformers 4.40+, llama-cpp-python, exllamav2,
SymPy 1.12, scipy 1.13. Python 3.12.

### F51 Labs — Game Generation R&D

Multi-node pipeline for generating playable games from natural language prompts:
brain (planning with LangGraph), artist (asset generation with ComfyUI),
coder (script generation), runner (launch). Offline-friendly with deterministic
fallbacks when local services are unavailable.

Stack: LangGraph 0.2+, ChromaDB 0.5, Mem0, Pygame CE 2.5, httpx. Python 3.12+.

### Xubuget — Personal Budget Application

Android budget management application built with Kotlin and Jetpack Compose.
Modern Material Design UI with local data persistence.

Stack: Kotlin 2.2, Compose, KSP 2.2, Android Gradle Plugin 8.13.

---

## Technical Principles

- **Local-first.** No model leaves this machine. Inference, training, and data
  stay on local hardware. The cloud is for email and calendar sync only.
- **Deterministic verification.** Every critical pipeline includes hash-based
  cataloging, deterministic tests, and exact rollback capabilities.
- **Consumer hardware.** Everything runs on an RTX 2070 with 8 GB VRAM.
  If it cannot run here, the architecture is wrong.
- **llama.cpp, not Ollama.** Direct control over quantization, context size,
  GPU offload layers, and the full GGUF runtime.
- **Bilingual engineering.** Code, docs, and architecture in English and
  French. Team communication in Brazilian Portuguese.

---

## Languages and Tools

- **Python** (primary): FastAPI, Flask, PyTorch, transformers, llama-cpp-python,
  OpenCV, pandas, numpy, scipy, SymPy, LangGraph, ChromaDB, pytest
- **Databases**: PostgreSQL (async), SQLite, DuckDB, ChromaDB (vector)
- **Kotlin**: Android development with Jetpack Compose
- **TypeScript / JavaScript**: Frontend tooling, Playwright E2E testing
- **Infrastructure**: llama.cpp server, ComfyUI, Docker, Git, PowerShell

---

## Hardware

- Windows 10/11 desktop
- NVIDIA RTX 2070 (8 GB VRAM)
- 24+ GB system RAM
- Hybrid CPU/GPU inference with MoE offloading

---

*Nothing goes to the cloud unless strictly necessary.*
