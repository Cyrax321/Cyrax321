# Hello, I'm [Beans](https://github.com/Cyrax321)

I'm an ML Researcher and Systems Engineer focused on AI agent infrastructure, LLM domain adaptation, computer vision, and high-performance algorithms.

## Research and Engineering Categories

### 1. Agent Runtime and Systems Infrastructure (Flagship Work)

#### <span style="color:#22c55e">Currently shipping realtime open source</span> <img src="assets/blinking-dot.gif" width="10" height="10" alt="live" style="vertical-align:middle">

- **[CONTINUUM](https://github.com/Cyrax321/CONTINUUM)** · [[Live Demo](https://continuum-nu-six.vercel.app)] · [[PyPI](https://pypi.org/project/continuum-agent/)] · [[Docker GHCR](https://github.com/Cyrax321/CONTINUUM/pkgs/container/continuum)]  
  *Production-grade infrastructure for verifiable semantic recovery of long-running autonomous AI agents.*  
  **Apache 2.0 · Python 3.11+ · 28★ · 55 forks · ~2,240+ tests · 14 Phase 6 recovery scenarios**
  
  Solves the multi-hour agent crash failure mode: replaces naive context replay and token-burning hallucinated recoveries with deterministic, verifiable resumption.
  - **Zero Side-Effect Duplication**: Cryptographically tamper-evident SHA-256 hash-chained event logs paired with an idempotent action ledger physically preventing duplicate mutations (e.g. double billing, duplicate API writes).
  - **Semantic Checkpoints and Environment Revalidation**: Resumes from compact, versioned state contracts rather than lossy conversation dumps, enforcing staleness propagation across external dependency graphs before execution resumes.
  - **Deny-by-Default MCP Server (12 Tools)**: Native drop-in integration for Claude Code, Cursor, and Anthropic toolchains with sub-second deterministic rollbacks.
  - **Rigorous Battle Testing**: 14 Phase 6 recovery scenarios 100% verified inside real Claude Code agent sessions; automated Docker builds on GHCR and interactive web demo.

- **[SNAGLINE](https://github.com/Cyrax321/SNAGLINE)** · [[Documentation](https://cyrax321.github.io/SNAGLINE/)] · [[PyPI](https://pypi.org/project/snagline/)]  
  *Zero-dependency, microsecond-scale real-time failure detection and guardrails for LLM agents.*  
  **MIT · Python 3.10+ · 13★ · 9 forks · Zero dependencies · 1.70 - 2.43 μs median latency**
  
  Eliminates the silent budget-burn problem: catches infinite loops, tool thrashing, latency spikes, and reasoning collapse in real time in <1ms without expensive LLM-as-a-judge calls.
  - **Microsecond-Scale Zero Overhead**: Runs $O(1)$ amortized statistical detectors using strictly the Python standard library, benchmarked at **1.70 - 2.43 μs median / 27.71 μs p99** over 200,000 synthetic steps on Apple Silicon.
  - **Deterministic Multi-Vector Anomaly Trapping**: Real-time detection across infinite loops (sliding-window novelty), error cascades, statistical CUSUM latency regressions, semantic goal drift, tool meltdown/entropy collapse, and token runaway.
  - **Universal Framework Interoperability**: Zero vendor lock-in. Drop-in companion for LangGraph, LangChain, AutoGen, CrewAI, and custom raw Python loops, with native HTTP sidecar bridges for non-Python agents (Claude Code, OpenClaw, Hermes).

- **[kibo-v7-](https://github.com/Cyrax321/kibo-v7-)**  
  *Career orchestration platform.*  
  TypeScript, React 18, Vite, TanStack Query, PostgreSQL with Supabase Realtime sub-100ms CDC, Tailwind CSS, Shadcn UI, Recharts for garden graphs and leaderboards, v5.0.0 MIT.

---

### 2. LLM Research and Domain Specialization

- **[QwerySmith Model Family](https://github.com/Cyrax321/QwerySmith-1.0)** · [[Research Paper (PDF)](https://drive.google.com/file/d/1sN1eVn7LpOi6cLEI1euxOT2cByBoXLlg/view?usp=sharing)] · [[GitHub Codebase](https://github.com/Cyrax321/QwerySmith-1.0)]  
  *Production Text-to-SQL research pipeline and self-healing autonomous database agent (Qwen3-4B base foundation + QLoRA via Unsloth and TRL).*  
  **MIT · Python 3.10+ · 88.5% In-Dist Acc · 55.7% Enterprise Acc (+43 wins vs 18 losses on Gretel, p=0.0019) · Zero-Shot Reasoning**
  
  Addresses single-source catastrophic overfitting in domain-adapted LLMs by engineering a balanced multi-source curriculum (`b-mc2` + `gretelai`), enforcing leak-proof split carving, and formalizing the Few-Shot Paradox. Ships with an interactive, autonomous CLI agent featuring schema introspection and execution-guided self-healing error recovery.
  
  - **QwerySmith 1.1**:
    - [LoRA Adapter](https://huggingface.co/Cyrax321/QwerySmith-1.1/tree/main): 132 MB parameter-efficient adapter weights trained on balanced multi-source curriculum.
    - [Merged Model](https://huggingface.co/Cyrax321/QwerySmith-1.1-Merged): Full 16-bit standalone model for vLLM, TGI, and Transformers.
    - [GGUF Quantized Model](https://huggingface.co/Cyrax321/QwerySmith-1.1-GGUF/tree/main): Quantized 4-bit (`q4_k_m`) model for local offline inference via Ollama and llama.cpp.
  - **QwerySmith 1.0**:
    - [LoRA Adapter](https://huggingface.co/Cyrax321/QwerySmith-1.0): 132 MB parameter-efficient adapter weights (single-source training).
    - [Merged Model](https://huggingface.co/Cyrax321/QwerySmith-1.0-Merged): Standalone 16-bit model checkpoint.
    - [GGUF Quantized Model](https://huggingface.co/Cyrax321/QwerySmith-1.0-GGUF): Quantized 4-bit (`q4_k_m`) model for local offline inference.

---

### 3. Computer Vision and Rare Disease Imaging

- **[wave-coAtNet](https://github.com/Cyrax321/wave-coAtNet)**  
  *Wavelet-enhanced hybrid CNN-Transformer with 2D Discrete Wavelet Transform (DWT) subband decomposition.*  
  Features MBConv depthwise separable convolution, cross-attention, relative position bias, and prototype selection. Evaluated on 13 model benchmarks with 5-fold cross-validation, achieving 0.942 Quadratic Weighted Kappa across rare ichthyosis subtypes.

- **[H-CoAtNet-Ichthyosis](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis)**  
  *Hierarchical hybrid CNN-Transformer for 5 ichthyosis subtypes.*  
  Benchmarked on 1,580 clinical images using PyTorch and timm, integrating convolutional stems with transformer blocks and squeeze-and-excitation modules.

- **HI-MobileNet** · [[IEEE Publication](https://ieeexplore.ieee.org/document/11332605)] · [[Codebase](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Models)]  
  *MobileNetV2 architecture for Harlequin Ichthyosis classification.*  
  IEEE DOI 11332605, achieving 99.96% accuracy on clinical diagnostic subsets.

- **[H-CoAtNet-Ichthyosis-Classification](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Classification)**  
  *Training and evaluation harness for WaveCoAtNet architectures.*  
  Supports 7 pretrained and scratch baselines with automated stratified validation splits.

---

### 4. Temporal Modeling and Video Analysis

- **HAR from Video** · [[IEEE PICC 2025 Publication](https://ieeexplore.ieee.org/document/11291542)] · [[Codebase](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition)]  
  *Sample-efficient 7-class human activity recognition benchmark.*  
  IEEE PICC 2025 DOI 11291542. Evaluated on 1,113 videos using CNN-LSTM architectures reaching 96.23% classification accuracy in Python, TensorFlow, and PyTorch.

---

### 5. High-Performance Algorithms and Compact Data Structures

- **[SPPS-Mac-Os-Code-Base](https://github.com/Cyrax321/SPPS-Mac-Os-Code-Base)**  
  *Succinct Path Partition Serialization: Bijective O(n) tree serialization.*  
  Benchmarked on Apple M1 arm64 across 8 memory blocks versus LOUDS, FlatBuffers, and Protobuf. ESA 2026 Track E submission.

- **[spps-linux-experiment-results](https://github.com/Cyrax321/spps-linux-experiment-results)**  
  *Cross-platform algorithmic validation on AMD EPYC 7763 Ubuntu 24.04.*  
  12,006 of 12,006 test suites verified passing (100% deterministic conformance).

- **[spps-experiments](https://github.com/Cyrax321/spps-experiments)**  
  *ESA 2026 submission benchmarks on AMD Ryzen 5 7235HS platform.*

---

### 6. Open Source Core Contributions

- **[tensorflow](https://github.com/tensorflow/tensorflow)** (197,312 stars, 76,097 forks)  
  Core contributions in upstream TensorFlow across tensor math, gradient stability, and XLA compilers. Fork: [Cyrax321/tensorflow](https://github.com/Cyrax321/tensorflow) (24 merged and upstream fixes).

  - fix-weighted-moments-tensor-axes: [#122402](https://github.com/tensorflow/tensorflow/pull/122402) - Fix TypeError when axes is Tensor or ndarray. Normalize via constant_value and tolist. Add 3 tests.
  - fix-linalg-det-singular-gradient: [#122823](https://github.com/tensorflow/tensorflow/pull/122823) - Fix singular matrix crash. Use SVD det times A inverse H plus pinv instead of matrix_inverse.
  - fix-topk-grad-int64-dtype: [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype) - Fix hardcoded int32 offset. Use dynamic index_type for top_k.
  - fix-grappler-argmax-saturating-ops: [#122826](https://github.com/tensorflow/tensorflow/pull/122826) - Fix wrong results for saturating ops in float32.
  - fix-igamma-domain-nan: [#124927](https://github.com/tensorflow/tensorflow/pull/124927) - Fix domain check for NaN boundary handling.

  <details>
  <summary>View all 24 fixes</summary>

  - fix-weighted-moments-tensor-axes: [#122402](https://github.com/tensorflow/tensorflow/pull/122402)
  - fix-linalg-det-singular-gradient: [#122823](https://github.com/tensorflow/tensorflow/pull/122823)
  - fix-topk-grad-int64-dtype: [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype)
  - fix-grappler-argmax-saturating-ops: [#122826](https://github.com/tensorflow/tensorflow/pull/122826)
  - fix-igamma-domain-nan: [#124927](https://github.com/tensorflow/tensorflow/pull/124927)
  - fix-grappler-reciprocal-involution: [#123195](https://github.com/tensorflow/tensorflow/pull/123195)
  - fix-floordiv-negative-infinity: [#123862](https://github.com/tensorflow/tensorflow/pull/123862)
  - fix-resource-sparse-adagrad-dtype-mismatch: [#124233](https://github.com/tensorflow/tensorflow/pull/124233)
  - fix-xla-transpose-negative-perm: [#124586](https://github.com/tensorflow/tensorflow/pull/124586)
  - fix-xla-tensorarray-unstack-scalar: [#124929](https://github.com/tensorflow/tensorflow/pull/124929)
  - fix-numpy-cross-xla-static-shape: [#124588](https://github.com/tensorflow/tensorflow/pull/124588)
  - fix-mlir-reciprocal-involution: [#123282](https://github.com/tensorflow/tensorflow/pull/123282)
  - fix-igamma-grad-nan-boundary: [#123803](https://github.com/tensorflow/tensorflow/pull/123803)
  - fix-cumulative-logsumexp-nan: [#115554](https://github.com/tensorflow/tensorflow/pull/115554)
  - fix-speech-commands-exception-types: [#117858](https://github.com/tensorflow/tensorflow/pull/117858)
  - fix-speech-commands-python-idioms: [#117894](https://github.com/tensorflow/tensorflow/pull/117894)
  - fix-tools-exception-types: [#117895](https://github.com/tensorflow/tensorflow/pull/117895)
  - fix-generic-exceptions-python: [#117860](https://github.com/tensorflow/tensorflow/pull/117860)
  - fix-cmake-overridable-fetchcontent-doc: [#124407](https://github.com/tensorflow/tensorflow/pull/124407)
  - fix-doc-typos: [#124450](https://github.com/tensorflow/tensorflow/pull/124450)
  - fix-misc-typos: [#115560](https://github.com/tensorflow/tensorflow/pull/115560)
  - fix-posixpath-sys-path: [#115551](https://github.com/tensorflow/tensorflow/pull/115551)
  - fix/weighted-moments-tensor-axes: [#122402](https://github.com/tensorflow/tensorflow/pull/122402)
  - revert-115560-fix-misc-typos: [branch](https://github.com/Cyrax321/tensorflow/tree/revert-115560-fix-misc-typos)

  </details>

---

## Engineering and AI Workflow

I actively experiment with state of the art foundation models, coding agents, and multi-agent workflows. My development methodology pairs agentic execution with human oversight: system architectures, invariant tests, and complex edge cases are designed, steered, and reviewed by me, while autonomous agents accelerate implementation, exploration, and refactoring loops. This human-in-the-loop workflow allows me to prototype rapidly, test novel research hypotheses, and maintain rigorous engineering standards across codebases.

---

## Get in Touch

Portfolio: https://sx3svi1pkrbco9gt.vercel.app/ · LinkedIn: https://linkedin.com/in/anandhupshaji · Email: cyrax8590@gmail.com
