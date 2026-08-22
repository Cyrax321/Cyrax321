<style>
@keyframes blink { 0%,100% { opacity: 1 } 50% { opacity: 0.15 } }
</style>

# Hello, I'm [Beans](https://github.com/Cyrax321)

I'm an ML Researcher focused on computer vision, temporal modeling and agent infrastructure. I build research that ships.

## Research and Publications

**Areas: Sample-Efficient HAR · Rare Disease Imaging · Hybrid CNN-Transformer · O(n) Tree Serialization · Agent Infrastructure**

- HAR from Video - IEEE PICC 2025 - DOI 11291542 - [ieee](https://ieeexplore.ieee.org/document/11291542) - 7 class HAR, 1,113 videos, CNN-LSTM 96.23% - Code: [HAR-Sample-Efficient-Activity-Recognition](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition)
- HI-MobileNet - IEEE - DOI 11332605 - [ieee](https://ieeexplore.ieee.org/document/11332605) - Harlequin Ichthyosis, MobileNetV2 99.96% - Code: [H-CoAtNet-Ichthyosis-Models](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Models)
- [HAR-Sample-Efficient-Activity-Recognition](https://github.com/Cyrax321/HAR-Sample-Efficient-Activity-Recognition) - 7 class video HAR, Python/TF/PyTorch, 96.23%
- [H-CoAtNet-Ichthyosis](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis) - Hybrid CNN-Transformer, 5 subtypes, 1,580 images, PyTorch/timm
- [wave-coAtNet](https://github.com/Cyrax321/wave-coAtNet) - Wavelet successor, cross attention, 13 model kappa
- [H-CoAtNet-Ichthyosis-Classification](https://github.com/Cyrax321/H-CoAtNet-Ichthyosis-Classification) - Training harness, 7 pretrained + scratch baselines
- [SPPS-Mac-Os-Code-Base](https://github.com/Cyrax321/SPPS-Mac-Os-Code-Base) - SPPS O(n) on M1, 8 blocks vs LOUDS/FlatBuffers/Protobuf
- [spps-linux-experiment-results](https://github.com/Cyrax321/spps-linux-experiment-results) - SPPS validation on EPYC 7763, 12006/12006 PASS
- [spps-experiments](https://github.com/Cyrax321/spps-experiments) - SPPS ESA 2026, bijective O(n), Ryzen 5 7235HS
### Engineering - Agent Infrastructure
#### <span style="animation:blink 1s step-end infinite;color:#22c55e">Currently shipping</span> <img src="assets/blinking-dot.gif" width="10" height="10" alt="live" style="vertical-align:middle">
- [CONTINUUM](https://github.com/Cyrax321/CONTINUUM) - Verifiable recovery for agents, 19 stars, Python 3.11, checkpoints, hash chain, MCP 10 tools, 1038 tests
- [SNAGLINE](https://github.com/Cyrax321/SNAGLINE) - Realtime failure detection, 4 stars, MIT, O(1) 1 microsecond
### Kibo
- [kibo-v7-](https://github.com/Cyrax321/kibo-v7-) - Career platform, TypeScript/React, Supabase Realtime, v5.0.0
### Open Source
- [tensorflow](https://github.com/tensorflow/tensorflow) - An Open Source ML Framework - 197,312 stars, 76,097 forks. My fork [Cyrax321/tensorflow](https://github.com/Cyrax321/tensorflow) has 25 fixes
- fix-weighted-moments-tensor-axes - [#122402](https://github.com/tensorflow/tensorflow/pull/122402) - Tensor axes TypeError
- fix-linalg-det-singular-gradient - [#122823](https://github.com/tensorflow/tensorflow/pull/122823) - Singular crash with SVD
- fix-topk-grad-int64-dtype - [branch](https://github.com/Cyrax321/tensorflow/tree/fix-topk-grad-int64-dtype) - int32 offset
- fix-grappler-argmax-saturating-ops - [#122826](https://github.com/tensorflow/tensorflow/pull/122826) - Saturating ops fix
- fix-igamma-domain-nan - [#124927](https://github.com/tensorflow/tensorflow/pull/124927) - NaN handling
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

- Portfolio: https://sx3svi1pkrbco9gt.vercel.app/
- LinkedIn: https://linkedin.com/in/anandhupshaji
- Email: cyrax8590@gmail.com
- GitHub: https://github.com/Cyrax321
