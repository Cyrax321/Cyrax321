<img align="left" src="https://raw.githubusercontent.com/Cyrax321/Cyrax321/refs/heads/main/assets/ratatui-spin-dark.gif#gh-dark-mode-only">
<img align="left" src="https://raw.githubusercontent.com/Cyrax321/Cyrax321/refs/heads/main/assets/ratatui-spin-light.gif#gh-light-mode-only">

### Hey!

👾 I'm **Beans**.

🔬 ML researcher with 2x IEEE as undergrad. I work on computer vision, temporal modeling and agent infrastructure. I cook at [Cyrax321](https://github.com/Cyrax321).

[![views](https://komarev.com/ghpvc/?username=Cyrax321&style=flat&color=313131&label=views&abbreviated=true)](https://github.com/Cyrax321) [![pgp](https://img.shields.io/badge/email-cyrax8590@gmail.com-313131?style=flat&labelColor=545454&color=313131)](mailto:cyrax8590@gmail.com) [![IEEE](https://img.shields.io/badge/IEEE-2x_published-00629B?style=flat&labelColor=545454&color=00629B)](https://ieeexplore.ieee.org/document/11291542)

<br>
<br>

#### ⚡ Stats

I joined GitHub **3** years ago and have since pushed **1546** commits, opened **173** issues, submitted **80** pull requests, and earned **25** stars across **159** personal projects, with contributions to **5** public repositories.

Current streak is **4** days, max streak is **19** days.

#### 🌀 Projects

| **Research** | **Engineering** |
| :--- | :--- |
| • [HAR-Sample-Efficient-Activity-Recognition](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition) - 7 class video HAR benchmark, 1,113 videos, CNN-LSTM 96.23% vs 3D CNN, VideoMAE, V-JEPA2. IEEE PICC 2025 [11291542](https://ieeexplore.ieee.org/document/11291542)<br>• [H-CoAtNet-Ichthyosis](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis) - Hierarchical hybrid CNN-Transformer for 5 ichthyosis subtypes on 1,580 images, review only<br>• [wave-coAtNet](https://github.com/Cyrax321/wave-coAtNet) - Wavelet enhanced successor with cross attention and prototype selection, 13 model kappa, 5 fold CV<br>• [H-CoAtNet-Ichthyosis-Classification](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Classification) - Training harness for WaveCoAtNet, 7 pretrained plus scratch baselines<br>• [H-CoAtNet-Ichthyosis-Models](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Models) - Original docx training code for HI-MobileNet, IEEE [11332605](https://ieeexplore.ieee.org/document/11332605) 99.96% MobileNetV2<br>• [SPPS-Mac-Os-Code-Base](https://github.com/Cyrax321/SPPS-Mac-Os-Code-Base) - SPPS O(n) tree serialization on Apple M1 arm64, 8 blocks vs LOUDS, FlatBuffers, Protobuf<br>• [spps-linux-experiment-results](https://github.com/Cyrax321/spps-linux-experiment-results) - SPPS cross platform validation on EPYC 7763 Ubuntu 24.04, 12006 of 12006 PASS<br>• [spps-experiments](https://github.com/Cyrax321/spps-experiments) - SPPS ESA 2026 Track E on Ryzen 5 7235HS, bijective O(n) | • [CONTINUUM](https://github.com/Cyrax321/CONTINUUM) - Verifiable semantic recovery for long running agents, 19 stars, 15 forks, Apache 2.0, Python 3.11, [demo](https://continuum-nu-six.vercel.app) - semantic checkpoints, hash chained log, MCP 10 tools, 1038 tests<br>• [SNAGLINE](https://github.com/Cyrax321/SNAGLINE) - Lightweight zero dependency realtime failure detection, 4 stars, MIT, Python 3.10 - loops, cascades, CUSUM, 1 microsecond per step<br>• [kibo-v7-](https://github.com/Cyrax321/kibo-v7-) - Career orchestration platform, TypeScript, React 18, Vite, TanStack Query, Supabase Realtime, sub 100ms CDC, canonical of 12 plus variants<br>• [tensorflow](https://github.com/Cyrax321/tensorflow) - Fork of tensorflow/tensorflow, 25 fix branches - weighted_moments a7a234b, linalg.det 2033cc7, top_k d511f44, Grappler 1581c76, igamma 713375a plus 20 cleanups |

Tip: Run `gh repo clone Cyrax321/CONTINUUM` to try the recovery demo.

#### 📈 Contributions

![Activity Graph](https://github-readme-activity-graph.vercel.app/graph?username=Cyrax321&bg_color=0d1117&color=4e9bff&line=4e9bff&point=ffffff&hide_border=true)
![Contribs](https://github-contributor-stats.vercel.app/api?username=Cyrax321&show_icons=true&theme=tokyonight&hide_border=true)

**TensorFlow** - [Cyrax321/tensorflow](https://github.com/Cyrax321/tensorflow) - 25 fix branches on tensorflow/tensorflow

| Fix | Commit | Summary |
| :--- | :--- | :--- |
| tf.nn.weighted_moments | a7a234b | Fix TypeError when axes is Tensor or ndarray. Normalize via constant_value and tolist. Add 3 tests. Fix Bazel deps |
| tf.linalg.det gradient | 2033cc7 | Fix singular crash. Use SVD det times A inverse H plus pinv instead of matrix_inverse |
| top_k int64 | d511f44 | Fix hardcoded int32 offset. Use dynamic index_type |
| Grappler ArgMax | 1581c76 | Fix wrong results for saturating ops in float32 |
| igamma NaN | 713375a | Fix a less equal 0 to not a greater than 0 for NaN. Add graph and eager Jacobian test |

Plus 20 cleanups: floordiv MLIR, logsumexp, reciprocal involution, numpy cross XLA, sparse adagrad, speech commands, typo sweeps, cmake. Browse at `github.com/Cyrax321/tensorflow/tree/fix-weighted-moments-tensor-axes`

#### 🛠️ What am I working on?

| **Category** | **Description** |
| :--- | :--- |
| **Researching** | [SPPS](https://github.com/Cyrax321/SPPS-Mac-Os-Code-Base) - Signed Positional Prufer Sequences, O(n) tree serialization. ESA 2026 Track E. |
| **Maintaining** | [CONTINUUM](https://github.com/Cyrax321/CONTINUUM) - Agent recovery. [SNAGLINE](https://github.com/Cyrax321/SNAGLINE) - Agent failure detection. |
| **Building** | [Kibo](https://github.com/Cyrax321/kibo-v7-) - Gamified career platform with Realtime, Garden graph and leaderboard. |
| **Contributing** | [tensorflow/tensorflow](https://github.com/Cyrax321/tensorflow) - 25 fix branches on upstream, weighted_moments, linalg.det, top_k. |
| **Writing** | [Portfolio](https://sx3svi1pkrbco9gt.vercel.app/) and IEEE papers [11291542](https://ieeexplore.ieee.org/document/11291542) [11332605](https://ieeexplore.ieee.org/document/11332605). |
| **Reaching** | [LinkedIn](https://linkedin.com/in/anandhupshaji) / [Email](mailto:cyrax8590@gmail.com) / [GitHub](https://github.com/Cyrax321). |

---

<div align="right">

**~** [_sx3svi1pkrbco9gt.vercel.app_](https://sx3svi1pkrbco9gt.vercel.app/)

</div>
