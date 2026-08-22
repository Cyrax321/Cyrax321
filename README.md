<style>
@keyframes blink { 0%,100% { opacity: 1 } 50% { opacity: 0.15 } }
</style>

# Hello, I'm [Beans](https://github.com/Cyrax321)

I'm an ML Researcher focused on computer vision, temporal modeling and agent infrastructure. I work on research that ships - benchmarking models from scratch in PyTorch and turning them into production systems in TypeScript.

My work spans sample efficient HAR, rare disease imaging, O(n) tree serialization and verifiable agent infrastructure.

## Research and Publications

**Areas: Sample-Efficient HAR · Rare Disease Imaging · Hybrid CNN-Transformer · O(n) Tree Serialization · Agent Infrastructure**

- HAR from Video - Deep Temporal Representation Learning for Sample-Efficient HAR - IEEE PICC 2025 - DOI 11291542 - [ieee](https://ieeexplore.ieee.org/document/11291542) - 7 class video HAR on 1,113 videos, CNN-LSTM 96.23% and 0.9628 F1 - Code: [HAR-Sample-Efficient-Activity-Recognition](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition)
- HI-MobileNet - Lightweight DL for Harlequin Ichthyosis - IEEE - DOI 11332605 - [ieee](https://ieeexplore.ieee.org/document/11332605) - MobileNetV2 99.96%, lightweight and deployable - Code: [H-CoAtNet-Ichthyosis-Models](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Models)
- [HAR-Sample-Efficient-Activity-Recognition](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition) - 7 class video HAR benchmark, Python, TensorFlow, PyTorch, 96.23% CNN-LSTM
- [H-CoAtNet-Ichthyosis](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis) - Hierarchical hybrid CNN-Transformer for 5 ichthyosis subtypes on 1,580 images, Python, PyTorch, timm, conv stem plus transformer plus SE and progressive token selection
- [wave-coAtNet](https://github.com/Cyrax321/wave-coAtNet) - Wavelet enhanced successor with cross attention and prototype selection, 13 model kappa, 5 fold CV
- [H-CoAtNet-Ichthyosis-Classification](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Classification) - Training harness for WaveCoAtNet, 7 pretrained plus scratch baselines
- [SPPS-Mac-Os-Code-Base](https://github.com/Cyrax321/SPPS-Mac-Os-Code-Base) - SPPS O(n) tree serialization on Apple M1 arm64, 8 blocks vs LOUDS, FlatBuffers, Protobuf, ESA 2026 Track E
- [spps-linux-experiment-results](https://github.com/Cyrax321/spps-linux-experiment-results) - Cross platform validation on EPYC 7763 Ubuntu 24.04, 12006 of 12006 PASS
- [spps-experiments](https://github.com/Cyrax321/spps-experiments) - ESA 2026 submission on Ryzen 5 7235HS, bijective O(n)

SPPS extends Prufer with direction and rank. Three repos are one project with different hardware. Blocks are correctness, linearity, real data bench, LOUDS, compression, tail latency, downstream and worked examples.

### Engineering - Agent Infrastructure

My current focus is verifiable infrastructure for long running agents.

#### <span style="animation:blink 1s step-end infinite;color:#22c55e">Currently shipping</span> <img src="assets/blinking-dot.gif" width="10" height="10" alt="live" style="vertical-align:middle">
- [CONTINUUM](https://github.com/Cyrax321/CONTINUUM) - Verifiable semantic recovery for long running agents. 19 stars, 15 forks, Apache 2.0, Python 3.11, [demo](https://continuum-nu-six.vercel.app). Semantic checkpoints not transcript dumps, hash chained log with 32 event types, MCP server with 10 tools deny by default, adapters for Generic Python, OpenAI Agents SDK, LangGraph, LangChain, Docker, K8s and Browser. Verified on Claude Code Opus 4.8 with 7 of 7 mechanics and 1038 tests passing.
- [SNAGLINE](https://github.com/Cyrax321/SNAGLINE) - Lightweight zero dependency realtime failure detection. 4 stars, MIT, Python 3.10. O(1) per step about 1 microsecond, fail open, loops, cascades and CUSUM, median 1.9 microsecond per step over 200k steps.

SNAGLINE detects. CONTINUUM recovers. Built to run together.

### Kibo
- [kibo-v7-](https://github.com/Cyrax321/kibo-v7-) - Career orchestration platform, TypeScript, React 18, Vite, TanStack Query, PostgreSQL with Supabase Realtime sub 100ms CDC, Tailwind plus Shadcn plus Recharts for Garden graph and leaderboard, v5.0.0 MIT. Canonical of 12 plus variants.

### Open Source

I've contributed to open source primarily through fixes on large codebases.
- [tensorflow](https://github.com/tensorflow/tensorflow) - An Open Source Machine Learning Framework for Everyone - 197,312 stars, 76,097 forks upstream. My fork [Cyrax321/tensorflow](https://github.com/Cyrax321/tensorflow) has 25 fix branches, branch stage behind upstream 1793 on master as of Aug 2026
- fix-weighted-moments-tensor-axes - [#122402](https://github.com/tensorflow/tensorflow/pull/122402) - Fix TypeError when axes is Tensor or ndarray
- fix-linalg-det-singular-gradient - [#122823](https://github.com/tensorflow/tensorflow/pull/122823) - Fix singular crash with SVD
- fix-topk-grad-int64-dtype - [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype) - Fix hardcoded int32 offset for top_k
- fix-grappler-argmax-saturating-ops - [#122826](https://github.com/tensorflow/tensorflow/pull/122826) - Fix saturating ops in float32
- fix-igamma-domain-nan - [#124927](https://github.com/tensorflow/tensorflow/pull/124927) - Fix NaN handling for igamma
<details>
<summary>View all 24 fixes</summary>

- fix-weighted-moments-tensor-axes - [#122402](https://github.com/tensorflow/tensorflow/pull/122402) - Fix TypeError when axes is Tensor or ndarray
- fix-linalg-det-singular-gradient - [#122823](https://github.com/tensorflow/tensorflow/pull/122823) - Fix singular crash with SVD
- fix-topk-grad-int64-dtype - [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype) - Fix hardcoded int32 offset for top_k
- fix-grappler-argmax-saturating-ops - [#122826](https://github.com/tensorflow/tensorflow/pull/122826) - Fix saturating ops in float32
- fix-igamma-domain-nan - [#124927](https://github.com/tensorflow/tensorflow/pull/124927) - Fix NaN handling for igamma
- fix-grappler-reciprocal-involution - [#123195](https://github.com/tensorflow/tensorflow/pull/123195) - Exact tensor equality for reciprocal
- fix-floordiv-negative-infinity - [#123862](https://github.com/tensorflow/tensorflow/pull/123862) - MLIR FloorDiv infinity correction
- fix-resource-sparse-adagrad-dtype-mismatch - [#124233](https://github.com/tensorflow/tensorflow/pull/124233) - Validate dtypes in training ops
- fix-xla-transpose-negative-perm - [#124586](https://github.com/tensorflow/tensorflow/pull/124586) - Normalize negative perm in XLA
- fix-xla-tensorarray-unstack-scalar - [#124929](https://github.com/tensorflow/tensorflow/pull/124929) - Scatter and disable control flow
- fix-numpy-cross-xla-static-shape - [#124588](https://github.com/tensorflow/tensorflow/pull/124588) - Static last dim size
- fix-mlir-reciprocal-involution - [#123282](https://github.com/tensorflow/tensorflow/pull/123282) - Float test coverage
- fix-igamma-grad-nan-boundary - [#123803](https://github.com/tensorflow/tensorflow/pull/123803) - Run Jacobian test in graph and eager
- fix-cumulative-logsumexp-nan - [#115554](https://github.com/tensorflow/tensorflow/pull/115554) - Fix NaN for plus infinity
- fix-speech-commands-exception-types - [#117858](https://github.com/tensorflow/tensorflow/pull/117858) - Assert specific exception types
- fix-speech-commands-python-idioms - [#117894](https://github.com/tensorflow/tensorflow/pull/117894) - Update recognize_commands idioms
- fix-tools-exception-types - [#117895](https://github.com/tensorflow/tensorflow/pull/117895) - Update setup.py
- fix-generic-exceptions-python - [#117860](https://github.com/tensorflow/tensorflow/pull/117860) - Generic Exception to specific types
- fix-cmake-overridable-fetchcontent-doc - [#124407](https://github.com/tensorflow/tensorflow/pull/124407) - Fix override comment
- fix-doc-typos - [#124450](https://github.com/tensorflow/tensorflow/pull/124450) - Fix docstring typos
- fix-misc-typos - [#115560](https://github.com/tensorflow/tensorflow/pull/115560) - Fix ouput accomodate typos
- fix-posixpath-sys-path - [#115551](https://github.com/tensorflow/tensorflow/pull/115551) - Fix PosixPath in sys.path
- fix/weighted-moments-tensor-axes - [#122402](https://github.com/tensorflow/tensorflow/pull/122402) - Duplicate of rank 1
- revert-115560-fix-misc-typos - [branch](https://github.com/Cyrax321/tensorflow/tree/revert-115560-fix-misc-typos) - Revert misc typos

</details>

## Get in Touch

- Portfolio: https://sx3svi1pkrbco9gt.vercel.app/
- LinkedIn: https://linkedin.com/in/anandhupshaji
- Email: cyrax8590@gmail.com
- GitHub: https://github.com/Cyrax321

