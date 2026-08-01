Independent researcher working on verification, provenance, and correctness
for machine learning systems. All experiments run locally on consumer hardware.

My work focuses on two areas:

**Integrity gates for self-modifying ML systems** — mechanisms that refuse to
emit an artifact when a check fails rather than detecting anomalies after the fact.
Published "Refuse, Don't Report: Three Integrity Gates for Self-Modifying ML Systems"
(Zenodo, July 2026). Validated on 1.7B-parameter models with fully reproducible benchmarks.

**Prefix state reuse in hybrid architectures** — a correctness-first measurement
of caching in Selective-State-Space + attention models. Identified a silent bug in
PyTorch's causal masking that discards cached prefixes without warning. Measured
speedup of 4.3x to 18x at 517M parameters under a parity gate with negative control.

I also build local AI systems: a household assistant running Qwen 35B via llama.cpp
with 186 tools and 54 skills on 8 GB of VRAM, and an evidence-guided automotive
diagnostic platform combining FastAPI, PostgreSQL, DuckDB, and RAG.

I work in English, French, and Brazilian Portuguese. Based in Montreal.
