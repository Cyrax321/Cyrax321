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

- [tensorflow](https://github.com/Cyrax321/tensorflow) - Fork of tensorflow/tensorflow, 25 fix branches, branch stage behind upstream 1793 on master as of Aug 2026. Ranked by weight.

| Rank | Branch | Commit | Links | Summary |
| :---: | :--- | :---: | :--- | :--- |
| 1 | fix-weighted-moments-tensor-axes | a7a234b | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-weighted-moments-tensor-axes) [commit](https://github.com/Cyrax321/tensorflow/commit/a7a234b1f3b17b2b22041c9a10e562b5d1a78863) | Fix TypeError when axes is Tensor or ndarray. Normalize via constant_value and tolist. Add 3 tests. Fix Bazel deps |
| 2 | fix-linalg-det-singular-gradient | 2033cc7 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-linalg-det-singular-gradient) [commit](https://github.com/Cyrax321/tensorflow/commit/2033cc76b2315f61a5a1ec1af1ddc05ac9dd8d08) | Fix singular crash. Use SVD det times A inverse H plus pinv instead of matrix_inverse |
| 3 | fix-topk-grad-int64-dtype | d511f44 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype) [commit](https://github.com/Cyrax321/tensorflow/commit/d511f4415e674de6c91f964fa523695b41420a79) | Fix hardcoded int32 offset. Use dynamic index_type for top_k |
| 4 | fix-grappler-argmax-saturating-ops | 1581c76 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-grappler-argmax-saturating-ops) [commit](https://github.com/Cyrax321/tensorflow/commit/1581c762ce7e6619373bf4f5ffaa8741c63da20c) | Fix wrong results for saturating ops in float32 |
| 5 | fix-igamma-domain-nan | 713375a | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-igamma-domain-nan) [commit](https://github.com/Cyrax321/tensorflow/commit/713375a3f62cc6e544ce18f1437455dc40713094) | Fix a less equal 0 to not a greater than 0 for NaN handling |
| 6 | fix-grappler-reciprocal-involution | 8ccc030 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-grappler-reciprocal-involution) [commit](https://github.com/Cyrax321/tensorflow/commit/8ccc030f82456f48ea30a0e637a01c455a63c549) | Use exact tensor equality for reciprocal involution test |
| 7 | fix-floordiv-negative-infinity | 5fad2d9 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-floordiv-negative-infinity) [commit](https://github.com/Cyrax321/tensorflow/commit/5fad2d98dda05e746f5b5a96015fe19e0971566e) | Apply infinity correction in MLIR FloorDiv kernel |
| 8 | fix-resource-sparse-adagrad-dtype-mismatch | 511d5f2 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-resource-sparse-adagrad-dtype-mismatch) [commit](https://github.com/Cyrax321/tensorflow/commit/511d5f231db5356d96b41b425b22b64200a91b1a) | Validate resource variable dtypes in training ops |
| 9 | fix-xla-transpose-negative-perm | 9c0abb6 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-xla-transpose-negative-perm) [commit](https://github.com/Cyrax321/tensorflow/commit/9c0abb6ffc886f4eeef952601bbdb18e0057c833) | Normalize negative perm indices in XLA Transpose |
| 10 | fix-xla-tensorarray-unstack-scalar | c8fa9e1 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-xla-tensorarray-unstack-scalar) [commit](https://github.com/Cyrax321/tensorflow/commit/c8fa9e1a08ca4c2c99f6d3b834cbcade81ad4729) | Use scatter and disable control flow in scalar test |
| 11 | fix-numpy-cross-xla-static-shape | 82deac6 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-numpy-cross-xla-static-shape) [commit](https://github.com/Cyrax321/tensorflow/commit/82deac60d3d044603960cf4c4180d682fd6a72d0) | Use static last dim size in numpy cross |
| 12 | fix-mlir-reciprocal-involution | 2f8a402 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-mlir-reciprocal-involution) [commit](https://github.com/Cyrax321/tensorflow/commit/2f8a402f8e2a4f557dbe1d63eeda857e6d8015ca) | Add float test coverage for reciprocal involution |
| 13 | fix-igamma-grad-nan-boundary | f833857 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-igamma-grad-nan-boundary) [commit](https://github.com/Cyrax321/tensorflow/commit/f833857f58d05361067623cd8af263491fe5ea9e) | Run igamma Jacobian test in graph and eager modes |
| 14 | fix-cumulative-logsumexp-nan | f3a4b92 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-cumulative-logsumexp-nan) [commit](https://github.com/Cyrax321/tensorflow/commit/f3a4b924f43241d48d02edf1f27b1a2776ac0b7b) | Fix line too long in testPlusInfinity pylint |
| 15 | fix-speech-commands-exception-types | ce9a2cc | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-speech-commands-exception-types) [commit](https://github.com/Cyrax321/tensorflow/commit/ce9a2cc3f36b8ba0de0b376e85050eec8907e89e) | Assert specific exception types in tests |
| 16 | fix-speech-commands-python-idioms | ae6a0ef | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-speech-commands-python-idioms) [commit](https://github.com/Cyrax321/tensorflow/commit/ae6a0ef07f8f1d653f52e4b9192b6aafb5b301f3) | Update recognize_commands.py idioms |
| 17 | fix-tools-exception-types | 69f6e75 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-tools-exception-types) [commit](https://github.com/Cyrax321/tensorflow/commit/69f6e75023ea3f410a421793cfee9abb18007530) | Update redundant_tf_nightly_gpu setup.py |
| 18 | fix-generic-exceptions-python | 4b0ab3a | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-generic-exceptions-python) [commit](https://github.com/Cyrax321/tensorflow/commit/4b0ab3af8ee4a91300de060f321e1ea3df82e13c) | Merge master for generic exception handling |
| 19 | fix-cmake-overridable-fetchcontent-doc | 09156c4 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-cmake-overridable-fetchcontent-doc) [commit](https://github.com/Cyrax321/tensorflow/commit/09156c462f435fe8a14a79ee57b2ddf7c518aa7c) | Fix override comment and stray in foreach loop |
| 20 | fix-doc-typos | cc763e8 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-doc-typos) [commit](https://github.com/Cyrax321/tensorflow/commit/cc763e85ffba08501051b28c0939bd9784fe7b43) | Fix documentation typos in docstrings |
| 21 | fix-misc-typos | c9175fc | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-misc-typos) [commit](https://github.com/Cyrax321/tensorflow/commit/c9175fcf89f5a47c606e03f3e207f0e9b24843d9) | Fix ouput accomodate occured typos |
| 22 | fix-posixpath-sys-path | d9c0743 | [branch](https://github.com/Cyrax321/tensorflow/tree/fix-posixpath-sys-path) [commit](https://github.com/Cyrax321/tensorflow/commit/d9c0743842ff2a14347abc8c8901843084d6e982) | Trigger CLA re-check for posixpath |
| 23 | fix/weighted-moments-tensor-axes | a02a4bc | [branch](https://github.com/Cyrax321/tensorflow/tree/fix/weighted-moments-tensor-axes) [commit](https://github.com/Cyrax321/tensorflow/commit/a02a4bc6ad30aa4a09bb102ab87cc5fbd00e9360) | Duplicate of rank 1 with slash path |
| 24 | revert-115560-fix-misc-typos | d2cc61a | [branch](https://github.com/Cyrax321/tensorflow/tree/revert-115560-fix-misc-typos) [commit](https://github.com/Cyrax321/tensorflow/commit/d2cc61aaf3b5ea2c5e122ec9faf93f5881166fc8) | Revert misc typos fix |

Browse any fix at `github.com/Cyrax321/tensorflow/tree/<branch-name>`

## Get in Touch

- Portfolio: https://sx3svi1pkrbco9gt.vercel.app/
- LinkedIn: https://linkedin.com/in/anandhupshaji
- Email: cyrax8590@gmail.com
- GitHub: https://github.com/Cyrax321

