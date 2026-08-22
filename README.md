<div align="center">
  <img src="assets/banner.svg" width="1280" alt="Anandhu P Shaji — ML Researcher"/>
</div>
<div align="center">

# Anandhu P Shaji — Beans
### ML Researcher · BTech CSE (Pre-Final Year) · College of Engineering Munnar, APJ KTU

**Computer Vision · Temporal Modeling · Theoretical CS · Full-Stack Engineering**

<a href="https://linkedin.com/in/anandhupshaji"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white"/></a>
<a href="mailto:cyrax8590@gmail.com"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white"/></a>
<a href="https://sx3svi1pkrbco9gt.vercel.app/"><img src="https://img.shields.io/badge/Portfolio-0A0A0A?style=for-the-badge&logo=vercel&logoColor=white"/></a>
<a href="https://github.com/Cyrax321"><img src="https://img.shields.io/badge/GitHub-Cyrax321-181717?style=for-the-badge&logo=github&logoColor=white"/></a>

<br/>

<a href="https://ieeexplore.ieee.org/document/11291542"><img src="https://img.shields.io/badge/IEEE_Paper_1-HAR_96.23%25-00629B?style=flat-square&logo=ieee&logoColor=white"/></a>
<a href="https://ieeexplore.ieee.org/document/11332605"><img src="https://img.shields.io/badge/IEEE_Paper_2-HI--MobileNet_99.96%25-00629B?style=flat-square&logo=ieee&logoColor=white"/></a>
<img src="https://img.shields.io/badge/ACSES-Joint_Secretary-ffd060?style=flat-square"/>
<img src="https://img.shields.io/badge/Focus-Theoretical_CS-b040ff?style=flat-square"/>

<br/>
<sub>2× IEEE published as undergrad · 159 public repos · Contributor to TensorFlow · Builder of agent infrastructure (CONTINUUM 19★ · SNAGLINE 4★)</sub>

</div>

---

## About

Pre-final year CSE at **College of Engineering Munnar (APJ KTU), Kerala** and **Joint Secretary, ACSES**. I work at the intersection of **computer vision, temporal learning, and theory** — benchmarking architectures from scratch in PyTorch/TensorFlow and shipping production systems in React/TypeScript.

- 🔬 **Published 2× IEEE** as undergrad — sample-efficient video HAR + lightweight medical imaging for ultra-rare disease
- 🧱 **Engineering:** Verifiable agent recovery (CONTINUUM), real-time failure detection (SNAGLINE), full-stack career platform (Kibo)
- 🌲 **Theory:** Signed Positional Prüfer Sequences (SPPS) — novel O(n) tree serialization (ESA 2026 Track E)
- 🎯 **Next:** Mastering Theoretical CS — algorithms, structure, elegance

> `i love learning` — open to research collaborations and internships.

---

## Research — Published

### 📄 Paper 1 — Deep Temporal Representation Learning for Sample-Efficient HAR
**IEEE PICC 2025 — DOI [10.1109/PICC67314.2025.11291542](https://ieeexplore.ieee.org/document/11291542)** — Palliparambil, **Shaji**, Rajan

Benchmarked **3D CNN · CNN-LSTM · VideoMAE · V-JEPA2** on a 7-class activity dataset (1,113 videos: Clapping, Meet and Split, Sitting, Standing Still, Walking, Walking While Reading Book, Walking While Using Phone) under stratified 70/15/15 splits.

| Architecture | Accuracy | Macro F1 |
|:---|:---:|:---:|
| 3D CNN | 83.00% | 0.70 |
| **CNN-LSTM** | **96.23%** | **0.9628** |
| VideoMAE | 94.00% | 0.92 |
| V-JEPA2 | 91.00% | 0.90 |

**Finding:** CNN-LSTM hybrid beats transformers for long-range temporal modeling under low-sample regime.

→ **Code:** [`HAR-Sample-Efficient-Activity-Recognition`](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition) — `Python` — `3d_cnn.py` + dataset splits — [Kaggle source](https://www.kaggle.com/datasets/sharjeelmazhar/human-activity-recognition-video-dataset)

```bibtex
@inproceedings{palliparambil2025deep,
  title={Deep Temporal Representation Learning for Sample-Efficient HAR},
  author={Palliparambil, Athul Joe Joseph and Shaji, Anandhu P and Rajan, Rajeev},
  booktitle={2025 International Conf. on Power, Instrumentation, Control, and Computing (PICC)},
  year={2025}, doi={10.1109/PICC67314.2025.11291542}
}
```

---

### 🧬 Paper 2 — HI-MobileNet: Lightweight DL for Harlequin Ichthyosis
**IEEE — DOI [10.1109/...11332605](https://ieeexplore.ieee.org/document/11332605)** — Lightweight transfer learning for **Harlequin Ichthyosis**, an ultra-rare condition with extreme data scarcity.

- **Model:** MobileNetV2 (transfer learning)
- **Result:** **99.96% accuracy** — lightweight and deployable
- **Context:** Part of the Ichthyosis program alongside H-CoAtNet (below); HI-MobileNet is the efficient baseline that proved robust under limited data.

→ **Code reference:** [`H-CoAtNet-Ichthyosis-Models`](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Models) (original .docx training code, review-only)

---

## Research — Codebases

All research code is **review-only / reproducibility-first** (explicit permission required for redistribution).

| Project | Focus | Stack | Highlight | Repo |
|:---|:---|:---|:---|:---|
| **HAR-Sample-Efficient-Activity-Recognition** | 7-class video HAR benchmark | Python · TensorFlow · PyTorch · HF | CNN-LSTM 96.23% vs 3D CNN / VideoMAE / V-JEPA2 | [→](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition) |
| **H-CoAtNet-Ichthyosis** | Hierarchical hybrid CNN-Transformer for ichthyosis (5 classes: HI, IV, LI, NS, Healthy) on 1,580 images (224², 70/15/15) | Python · PyTorch · timm · Roboflow | Conv stem + Transformer + SE + token selection — verification/benchmarking suite | [→](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis) |
| **WaveCoAtNet** | Wavelet-enhanced successor to H-CoAtNet — cross-attention + prototype-anchored token selection | Python · PyTorch | 13-model kappa comparison, 5-fold CV + McNemar, Grad-CAM, f1 heatmaps — next-gen architecture diagrams | [→](https://github.com/Cyrax321/wave-coAtNet) |
| **SPPS-Mac-Os-Code-Base** | SPPS on Apple M1 (arm64) — primary benchmark | C++17 · Apple Clang 17 · Protobuf 34 · FlatBuffers 25.12 · zstd 1.5.7 | 8 blocks: correctness, O(n) linearity, 4-method real-data bench, LOUDS O(1), compression, tail latency, downstream, worked examples | [→](https://github.com/Cyrax321/SPPS-Mac-Os-Code-Base) |
| **spps-linux-experiment-results** | SPPS cross-platform validation | C++ · GCC 13.3 · Ubuntu 24.04 (EPYC 7763) | 12,006/12,006 PASS — parity with M1, custom static builds, datasets: Django 2.3M, sqlite3 503k, XMark 500k | [→](https://github.com/Cyrax321/spps-linux-experiment-results) |
| **spps-experiments** | SPPS ESA 2026 Track E submission | C++ · GCC 11 · Ryzen 5 7235HS | Bijective O(n) encoding — `PLATFORM.md` + `EXPERIMENTS.md`, perf/uProf profiling | [→](https://github.com/Cyrax321/spps-experiments) |
| **H-CoAtNet-Ichthyosis-Classification** | WaveCoAtNet training harness (scratch + pretrained) | Python | `train_wavecoatnet.py` + 7 pretrained baselines (EfficientNet-B0, Swin-T, ViT-B/16, BiomedCLIP, DINOv2) + scratch variants | [→](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Classification) |

**Datasets:** HAR via Kaggle; Ichthyosis via [Roboflow](https://universe.roboflow.com/hi-l9ueo/ich-s-7lnsj) (API key required); SPPS via `datasets/{real_ast_benchmark.txt, sqlite3_ast_edges.txt, xmark_edges.txt}`.

<details>
<summary><b>SPPS — 8 Experiment Blocks at a Glance</b></summary>

- **A Correctness** — fuzzing + worked examples (12k tests)
- **B O(n) Linearity** — regression across 4 topologies
- **C Real-Dataset Benchmarks** — SPPS vs LOUDS vs FlatBuffers vs Protobuf (Arena)
- **D LOUDS Baseline** — 64-bit packed + `__builtin_popcountll`
- **E Compression** — zstd apples-to-apples
- **F Tail Latency** — CV% stability
- **G Downstream Macro-Benchmark** — end-to-end pipeline
- **H Worked Examples** — step-by-step encode/decode traces

All SPPS repos carry `⚠️ REVIEW-ONLY NOTICE`.

</details>

---

## Engineering — Current Projects

### CONTINUUM — Verifiable Semantic Recovery for Agents
**[`Cyrax321/CONTINUUM`](https://github.com/Cyrax321/CONTINUUM) · 19★ · 15 forks · Apache-2.0 · Python 3.11+ · [Live Demo](https://continuum-nu-six.vercel.app)**

Long-running agents crash after hundreds of LLM calls and DB writes. Replay duplicates side effects. CONTINUUM asks: *can an agent resume from compact verified task state?*

**Not a framework — three differentiators:**
1. **Semantic checkpoints** — versioned, minimal, inspectable (not transcript dumps)
2. **Environment revalidation** — every component verified against the live world before resume (staleness propagates via dependency graph)
3. **Provenance-aware state** — agent claims = `REQUIRES_REVIEW`, never self-certifying

| Capability | Detail |
|:---|:---|
| Idempotent ledger | 2-phase claim→complete, refuses duplicates, surfaces `uncertain` for reconciliation |
| Tamper-evident log | Hash-chained, 32 event types, `verify_events().ok` |
| Recovery engine | 7 recovery modes, sealed next-action contract |
| MCP server | 10 tools (3 read-only / 7 mutating, deny-by-default `CONTINUUM_MCP_MUTATING_CLIENTS`), stdio JSON-RPC |
| Adapters | Generic Python, OpenAI Agents SDK, LangGraph, LangChain, Docker, K8s, Browser (Playwright) |
| Security | Secure planning loop (2-signal perception), periodic revalidation every 25 steps |

**Verified:** Claude Code Opus 4.8 E2E (invoice batch + `SIGKILL`, **7/7 mechanics**), Gemini CLI + Kilo Code, `CONTINUUM-Bench` 5 scenarios (0 dup work), MCP adversarial audit, **1038 tests passing** (hypothesis, concurrency).

```python
from continuum import EventType, Run, SQLiteStorage, project
store = SQLiteStorage("agent.db")
store.create_run(Run(run_id="run_4821", goal="Analyze 10,000 documents"))
# ... analyze, store.append_event(WORK_COMPLETED)
state = project("run_4821", store.read_events("run_4821"))  # resume after crash
assert store.verify_events("run_4821").ok  # chain intact
```

---

### SNAGLINE — Real-Time Failure Detection for Agents
**[`Cyrax321/SNAGLINE`](https://github.com/Cyrax321/SNAGLINE) · 4★ · 3 forks · MIT · Python 3.10+**

A **zero-dependency, O(1)/step (~1 µs)** companion that watches any agent's execution stream and flags failures before they waste hours. **Fail-open:** detector/sink exceptions never propagate to the host.

| Detector | Catches | Method |
|:---|:---|:---|
| **Loop** | Retry storms | Sliding window N repeats in W steps |
| **Error Cascade** | Fast + slow-burn degradations | N consecutive or N-in-window |
| **Latency Anomaly** | Sustained regression | Welford mean/var + frozen baseline + CUSUM |
| **Goal-Drift** *(opt-in)* | Divergence from healthy profile | `BaselineProfile` via `snagline baseline run.jsonl` |
| **ML Ensemble** *(opt-in)* | Stronger combined signal | Noisy-OR over base detectors |

**Sinks:** Console (default), webhook (stdlib `urllib`), extensible — only `FailureRisk` fields sent, **no content retention**.

**Adapters:** Raw loop (`watch`), LangChain `SnaglineCallbackHandler`, LangGraph stream wrapper, HTTP sidecar / file-tail for Claude Code.

**Perf:** Median 1.9 µs/step, p99 33.9 µs over 200k steps. Verified on LangChain `create_agent`, Claude Code hooks, real OpenRouter LLMs.

```python
from snagline import Monitor
from snagline.adapters.raw import watch
monitor = Monitor.default()
with watch(monitor, "ep-1") as step:
    step("tool_call", tool_name="search", args="query", latency_ms=120, error=False)
    # loop detector fires after 3 identical tool_calls
```

*SNAGLINE detects, CONTINUUM recovers — designed to run together.*

---

## Project — Kibo

**[`kibo-v7-`](https://github.com/Cyrax321/kibo-v7-) · TypeScript · Production-grade Career Orchestration Platform**

Full-stack engine to optimize the technical recruitment lifecycle for software engineers — gamification + real-time analytics driving consistent productivity.

| Layer | Stack | Purpose |
|:---|:---|:---|
| Frontend | React 18, TypeScript, Vite | Modularity, HMR |
| State | TanStack Query | Optimistic mutations, caching |
| DB / Realtime | PostgreSQL (Supabase) + logical replication | Sub-100ms CDC via WebSockets |
| Styling | TailwindCSS + Shadcn | Accessible design system |
| Viz | Recharts | Trends, leaderboard, "The Garden" contribution graph |

**Core:** Real-time Event Bus, Gamification Protocol (XP / streaks / achievements), Analytics Dashboard, Global Leaderboard, Mission Control.

**Status:** Build passing · v5.0.0 · MIT · Vitest. Canonical repo is `kibo-v7-` (12+ `kibo-*` variants are historical iterations — see repo for history).

---

## Open Source — TensorFlow

**Fork:** [`Cyrax321/tensorflow`](https://github.com/Cyrax321/tensorflow) — fork of `tensorflow/tensorflow` (76k forks upstream)

**25 fix branches** — contributions are branch-stage (fork behind upstream ~1793 on master as of Aug 2026; awaiting upstream review). All authored as `Cyrax321`/`Beans`.

**Top 5 substantive fixes (feature in profile):**

| Fix | Commit | What it fixes |
|:---|:---|:---|
| **tf.nn.weighted_moments** | `a7a234b` | `TypeError` when `axes` is `tf.Tensor` / `numpy.ndarray` — normalize via `tensor_util.constant_value` + `.tolist()`, add 3 regression tests (`testNumpyArrayAxesKeepdimsFalse`, `testScalarTensorAxesKeepdimsFalse`, `testMultiAxisTensorKeepdimsFalse`), Bazel `strict_deps` fix |
| **tf.linalg.det gradient** | `2033cc7` | Singular matrix crash — replace `matrix_inverse` (raises `InvalidArgumentError`) with SVD (`det * A^{-H}`) + `pinv` for `LogMatrixDeterminant` |
| **top_k int64 dtype** | `d511f44` | Hardcoded int32 offset → dynamic `index_type`, fixes type mismatch when adding indices |
| **Grappler ArgMax saturating ops** | `1581c76` | Wrong results for float32 saturating ops |
| **igamma NaN domain** | `713375a` | `a <= 0` → `!(a > 0)` for correct NaN handling; `f833857` adds graph+eager Jacobian test |

**Plus 20 cleanups:** Floordiv infinity MLIR kernel, cumulative logsumexp, mlir reciprocal involution (exact bitwise test), numpy cross XLA static shape, resource sparse adagrad dtype, speech_commands exception types/python idioms, Grappler reciprocal, typo sweeps, cmake doc.

→ **Browse:** `https://github.com/Cyrax321/tensorflow/tree/fix-weighted-moments-tensor-axes` (replace branch name for each fix)

---

## Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-000000?style=flat-square&logo=anthropic&logoColor=white)

---

## GitHub Stats

<div align="center">

![Stats](https://github-readme-stats.vercel.app/api?username=Cyrax321&show_icons=true&theme=tokyonight&hide_border=true&include_all_commits=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=Cyrax321&layout=compact&theme=tokyonight&hide_border=true)
![Streak](https://github-readme-streak-stats.herokuapp.com/?user=Cyrax321&theme=tokyonight&hide_border=true)

</div>

---

## Connect

- **Portfolio:** https://sx3svi1pkrbco9gt.vercel.app/
- **LinkedIn:** https://linkedin.com/in/anandhupshaji
- **Email:** cyrax8590@gmail.com
- **Location:** CEM · Kerala — open to research collaborations & internships

<div align="center">
<sub>Built with rigor — from PyTorch from scratch to MCP servers. "i love learning" — Beans</sub>
<br/>
<sub>Last updated: Aug 2026 · Profile repo: <a href="https://github.com/Cyrax321/Cyrax321">Cyrax321/Cyrax321</a></sub>
</div>
