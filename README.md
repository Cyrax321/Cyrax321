# Hello, I'm [Beans](https://github.com/Cyrax321)

I'm an ML Researcher focused on computer vision, temporal modeling and agent infrastructure. I build research that ships.

## Research and Publications

**Areas: LLM Fine-Tuning & Text-to-SQL · Agent Infrastructure · Sample-Efficient HAR · Rare Disease Imaging · Hybrid CNN-Transformer**

- HAR from Video - IEEE PICC 2025 - DOI 11291542 - [ieee](https://ieeexplore.ieee.org/document/11291542) - 7 class HAR, 1,113 videos, CNN-LSTM 96.23% - Code: [HAR-Sample-Efficient-Activity-Recognition](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition)
- HI-MobileNet - IEEE - DOI 11332605 - [ieee](https://ieeexplore.ieee.org/document/11332605) - Harlequin Ichthyosis, MobileNetV2 99.96% - Code: [H-CoAtNet-Ichthyosis-Models](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Models)
- [HAR-Sample-Efficient-Activity-Recognition](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition) - 7 class video HAR benchmark, Python, TensorFlow, PyTorch, 96.23% CNN-LSTM
- [H-CoAtNet-Ichthyosis](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis) - Hierarchical hybrid CNN-Transformer for 5 ichthyosis subtypes on 1,580 images, Python, PyTorch, timm, conv stem plus transformer plus SE
- [wave-coAtNet](https://github.com/Cyrax321/wave-coAtNet) - Wavelet enhanced successor with cross attention and prototype selection, 13 model kappa, 5 fold CV
- [H-CoAtNet-Ichthyosis-Classification](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Classification) - Training harness for WaveCoAtNet, 7 pretrained plus scratch baselines
- [SPPS-Mac-Os-Code-Base](https://github.com/Cyrax321/SPPS-Mac-Os-Code-Base) - SPPS O(n) tree serialization on Apple M1 arm64, 8 blocks vs LOUDS, FlatBuffers, Protobuf, ESA 2026 Track E
- [spps-linux-experiment-results](https://github.com/Cyrax321/spps-linux-experiment-results) - Cross platform validation on EPYC 7763 Ubuntu 24.04, 12006 of 12006 PASS
- [spps-experiments](https://github.com/Cyrax321/spps-experiments) - ESA 2026 submission on Ryzen 5 7235HS, bijective O(n)
- QwerySmith: Multi-Source Curriculum Fine-Tuning and Robust Evaluation for Text-to-SQL - 2026 - [[Research Paper (PDF)]](https://drive.google.com/file/d/1sN1eVn7LpOi6cLEI1euxOT2cByBoXLlg/view?usp=sharing) · [[Code]](https://github.com/Cyrax321/QwerySmith-1.0) - Qwen3-4B + QLoRA, 88.5% in-dist, 55.7% enterprise, self-healing SQL agent

### LLM Research & Fine-Tuning

I fine-tune, specialize, and evaluate open-source language models with a focus on sample efficiency, domain generalization, and deterministic SQL execution.

- **[QwerySmith 1.0 & 1.1](https://github.com/Cyrax321/QwerySmith-1.0)** · [[Research Paper (PDF)](https://drive.google.com/file/d/1sN1eVn7LpOi6cLEI1euxOT2cByBoXLlg/view?usp=sharing)] · [[GitHub Codebase](https://github.com/Cyrax321/QwerySmith-1.0)]  
  *Production Text-to-SQL research pipeline & self-healing autonomous database agent (Qwen3-4B + QLoRA via Unsloth & TRL).*  
  **MIT · Python 3.10+ · 88.5% In-Dist Acc · 55.7% Enterprise Acc (+43 wins vs 18 losses on Gretel, $p=0.0019$) · Zero-Shot Reasoning**
  
  Addresses single-source catastrophic overfitting in domain-adapted LLMs by engineering a balanced multi-source curriculum (`b-mc2` + `gretelai`), enforcing leak-proof split carving, and formalizing the *Few-Shot Paradox*. Ships with an interactive, autonomous CLI agent featuring schema introspection and execution-guided self-healing error recovery.
  
  - **QwerySmith 1.1 (Latest / Production)**:
    - [LoRA Adapter](https://huggingface.co/Cyrax321/QwerySmith-1.1/tree/main) - 132 MB parameter-efficient adapter weights trained on balanced multi-source curriculum.
    - [Merged Model](https://huggingface.co/Cyrax321/QwerySmith-1.1-Merged) - Full 16-bit standalone model for vLLM, TGI, and Transformers.
    - [GGUF Quantized Model](https://huggingface.co/Cyrax321/QwerySmith-1.1-GGUF/tree/main) - Quantized 4-bit (`q4_k_m`) model for local offline inference via Ollama & llama.cpp.
  - **QwerySmith 1.0 (Baseline)**:
    - [LoRA Adapter](https://huggingface.co/Cyrax321/QwerySmith-1.0) - Single-source baseline adapter.
    - [Merged Model](https://huggingface.co/Cyrax321/QwerySmith-1.0-Merged) - Standalone v1.0 checkpoint.
    - [GGUF Quantized Model](https://huggingface.co/Cyrax321/QwerySmith-1.0-GGUF) - Local baseline GGUF.

### Engineering - Agent Infrastructure
#### <span style="color:#22c55e">Currently shipping</span> <img src="assets/blinking-dot.gif" width="10" height="10" alt="live" style="vertical-align:middle">

- **[CONTINUUM](https://github.com/Cyrax321/CONTINUUM)** · [[Live Demo](https://continuum-nu-six.vercel.app)] · [[PyPI](https://pypi.org/project/continuum-agent/)] · [[Docker GHCR](https://github.com/Cyrax321/CONTINUUM/pkgs/container/continuum)]  
  *Production-grade infrastructure for verifiable semantic recovery of long-running autonomous AI agents.*  
  **Apache 2.0 · Python 3.11+ · 28★ · 55 forks · ~2,240+ tests · 14 Phase 6 recovery scenarios**
  
  Solves the multi-hour agent crash failure mode: replaces naive context replay and token-burning hallucinated recoveries with deterministic, verifiable resumption.
  - **Zero Side-Effect Duplication**: Cryptographically tamper-evident SHA-256 hash-chained event logs paired with an idempotent action ledger physically preventing duplicate mutations (e.g. double billing, duplicate API writes).
  - **Semantic Checkpoints & Environment Revalidation**: Resumes from compact, versioned state contracts rather than lossy conversation dumps, enforcing staleness propagation across external dependency graphs before execution resumes.
  - **Deny-by-Default MCP Server (12 Tools)**: Native drop-in integration for Claude Code, Cursor, and Anthropic toolchains with sub-second deterministic rollbacks.
  - **Rigorous Battle Testing**: 14 Phase 6 recovery scenarios 100% verified inside real Claude Code agent sessions; automated Docker builds on GHCR and interactive web demo.
  
- **[SNAGLINE](https://github.com/Cyrax321/SNAGLINE)** · [[Documentation](https://cyrax321.github.io/SNAGLINE/)] · [[PyPI](https://pypi.org/project/snagline/)]  
  *Zero-dependency, microsecond-scale real-time failure detection & guardrails for LLM agents.*  
  **MIT · Python 3.10+ · 13★ · 9 forks · Zero dependencies · 1.70 – 2.43 μs median latency**
  
  Eliminates the silent budget-burn problem: catches infinite loops, tool thrashing, latency spikes, and reasoning collapse in real time **in <1ms without expensive LLM-as-a-judge calls**.
  - **Microsecond-Scale Zero Overhead**: Runs $O(1)$ amortized statistical detectors using strictly the Python standard library—benchmarked at **1.70 – 2.43 μs median / 27.71 μs p99** over 200,000 synthetic steps on Apple Silicon.
  - **Deterministic Multi-Vector Anomaly Trapping**: Real-time detection across infinite loops (sliding-window novelty), error cascades, statistical CUSUM latency regressions, semantic goal drift, tool meltdown/entropy collapse, and token runaway.
  - **Universal Framework Interoperability**: Zero vendor lock-in. Drop-in companion for LangGraph, LangChain, AutoGen, CrewAI, and custom raw Python loops, with native HTTP sidecar bridges for non-Python agents (Claude Code, OpenClaw, Hermes).
#### Kibo
- [kibo-v7-](https://github.com/Cyrax321/kibo-v7-) - Career orchestration platform, TypeScript, React 18, Vite, TanStack Query, PostgreSQL with Supabase Realtime sub 100ms CDC, Tailwind plus Shadcn plus Recharts for Garden graph and leaderboard, v5.0.0 MIT
  
### Open Source Contributions 
- [tensorflow](https://github.com/tensorflow/tensorflow) - An Open Source ML Framework - 197,312 stars, 76,097 forks. My fork [Cyrax321/tensorflow](https://github.com/Cyrax321/tensorflow) has 25 fixes
- fix-weighted-moments-tensor-axes - [#122402](https://github.com/tensorflow/tensorflow/pull/122402) - Fix TypeError when axes is Tensor or ndarray. Normalize via constant_value and tolist. Add 3 tests
- fix-linalg-det-singular-gradient - [#122823](https://github.com/tensorflow/tensorflow/pull/122823) - Fix singular crash. Use SVD det times A inverse H plus pinv instead of matrix_inverse
- fix-topk-grad-int64-dtype - [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype) - Fix hardcoded int32 offset. Use dynamic index_type for top_k
- fix-grappler-argmax-saturating-ops - [#122826](https://github.com/tensorflow/tensorflow/pull/122826) - Fix wrong results for saturating ops in float32
- fix-igamma-domain-nan - [#124927](https://github.com/tensorflow/tensorflow/pull/124927) - Fix a less equal 0 to not a greater than 0 for NaN handling
<details>
<summary>View all 24 fixes</summary>

- fix-weighted-moments-tensor-axes - [#122402](https://github.com/tensorflow/tensorflow/pull/122402)
- fix-linalg-det-singular-gradient - [#122823](https://github.com/tensorflow/tensorflow/pull/122823)
- fix-topk-grad-int64-dtype - [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype)
- fix-grappler-argmax-saturating-ops - [#122826](https://github.com/tensorflow/tensorflow/pull/122826)
- fix-igamma-domain-nan - [#124927](https://github.com/tensorflow/tensorflow/pull/124927)
- fix-grappler-reciprocal-involution - [#123195](https://github.com/tensorflow/tensorflow/pull/123195)
- fix-floordiv-negative-infinity - [#123862](https://github.com/tensorflow/tensorflow/pull/123862)
- fix-resource-sparse-adagrad-dtype-mismatch - [#124233](https://github.com/tensorflow/tensorflow/pull/124233)
- fix-xla-transpose-negative-perm - [#124586](https://github.com/tensorflow/tensorflow/pull/124586)
- fix-xla-tensorarray-unstack-scalar - [#124929](https://github.com/tensorflow/tensorflow/pull/124929)
- fix-numpy-cross-xla-static-shape - [#124588](https://github.com/tensorflow/tensorflow/pull/124588)
- fix-mlir-reciprocal-involution - [#123282](https://github.com/tensorflow/tensorflow/pull/123282)
- fix-igamma-grad-nan-boundary - [#123803](https://github.com/tensorflow/tensorflow/pull/123803)
- fix-cumulative-logsumexp-nan - [#115554](https://github.com/tensorflow/tensorflow/pull/115554)
- fix-speech-commands-exception-types - [#117858](https://github.com/tensorflow/tensorflow/pull/117858)
- fix-speech-commands-python-idioms - [#117894](https://github.com/tensorflow/tensorflow/pull/117894)
- fix-tools-exception-types - [#117895](https://github.com/tensorflow/tensorflow/pull/117895)
- fix-generic-exceptions-python - [#117860](https://github.com/tensorflow/tensorflow/pull/117860)
- fix-cmake-overridable-fetchcontent-doc - [#124407](https://github.com/tensorflow/tensorflow/pull/124407)
- fix-doc-typos - [#124450](https://github.com/tensorflow/tensorflow/pull/124450)
- fix-misc-typos - [#115560](https://github.com/tensorflow/tensorflow/pull/115560)
- fix-posixpath-sys-path - [#115551](https://github.com/tensorflow/tensorflow/pull/115551)
- fix/weighted-moments-tensor-axes - [#122402](https://github.com/tensorflow/tensorflow/pull/122402)
- revert-115560-fix-misc-typos - [branch](https://github.com/Cyrax321/tensorflow/tree/revert-115560-fix-misc-typos)

</details>

## Get in Touch

Portfolio: https://sx3svi1pkrbco9gt.vercel.app/ · LinkedIn: https://linkedin.com/in/anandhupshaji · Email: cyrax8590@gmail.com
