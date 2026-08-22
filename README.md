<style>
@keyframes blink { 0%,100% { opacity: 1 } 50% { opacity: 0.15 } }
</style>

# Hello, I'm [Beans](https://github.com/Cyrax321)

I'm an ML Researcher focused on computer vision, temporal modeling and agent infrastructure. I work on research that ships - benchmarking models from scratch in PyTorch and turning them into production systems in TypeScript.

My work spans sample efficient HAR, rare disease imaging, O(n) tree serialization and verifiable agent infrastructure.

## Research and Publications

**Two IEEE papers as undergrad.**

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

### Engineering - Agent Infrastructure <span style="display:inline-block;width:8px;height:8px;background:#22c55e;border-radius:50%;animation:blink 1s step-end infinite;vertical-align:middle;margin-left:6px"></span> <span style="font-size:12px;color:#22c55e;animation:blink 1s step-end infinite">Currently shipping</span>

My current focus is verifiable infrastructure for long running agents.

- [CONTINUUM](https://github.com/Cyrax321/CONTINUUM) - Verifiable semantic recovery for long running agents. 19 stars, 15 forks, Apache 2.0, Python 3.11, [demo](https://continuum-nu-six.vercel.app). Semantic checkpoints not transcript dumps, hash chained log with 32 event types, MCP server with 10 tools deny by default, adapters for Generic Python, OpenAI Agents SDK, LangGraph, LangChain, Docker, K8s and Browser. Verified on Claude Code Opus 4.8 with 7 of 7 mechanics and 1038 tests passing.
- [SNAGLINE](https://github.com/Cyrax321/SNAGLINE) - Lightweight zero dependency realtime failure detection. 4 stars, MIT, Python 3.10. O(1) per step about 1 microsecond, fail open, loops, cascades and CUSUM, median 1.9 microsecond per step over 200k steps.

SNAGLINE detects. CONTINUUM recovers. Built to run together.

### Kibo

- [kibo-v7-](https://github.com/Cyrax321/kibo-v7-) - Career orchestration platform, TypeScript, React 18, Vite, TanStack Query, PostgreSQL with Supabase Realtime sub 100ms CDC, Tailwind plus Shadcn plus Recharts for Garden graph and leaderboard, v5.0.0 MIT. Canonical of 12 plus variants.

### Open Source

I've contributed to open source primarily through fixes on large codebases.

- [tensorflow](https://github.com/Cyrax321/tensorflow) - Fork of tensorflow/tensorflow, 25 fix branches, branch stage behind upstream 1793 on master as of Aug 2026

| Fix | Commit | Summary |
| :--- | :--- | :--- |
| tf.nn.weighted_moments | a7a234b | Fix TypeError when axes is Tensor or ndarray. Normalize via constant_value and tolist. Add 3 tests |
| tf.linalg.det gradient | 2033cc7 | Fix singular crash. Use SVD det times A inverse H plus pinv |
| top_k int64 | d511f44 | Fix hardcoded int32 offset. Use dynamic index_type |
| Grappler ArgMax | 1581c76 | Fix wrong results for saturating ops in float32 |
| igamma NaN | 713375a | Fix a less equal 0 to not a greater than 0 for NaN |

Plus 20 cleanups: floordiv MLIR, logsumexp, reciprocal involution, numpy cross XLA, sparse adagrad, speech commands and typo sweeps. Browse at `github.com/Cyrax321/tensorflow/tree/fix-weighted-moments-tensor-axes`

## Get in Touch

- Portfolio: https://sx3svi1pkrbco9gt.vercel.app/
- LinkedIn: https://linkedin.com/in/anandhupshaji
- Email: cyrax8590@gmail.com
- GitHub: https://github.com/Cyrax321

