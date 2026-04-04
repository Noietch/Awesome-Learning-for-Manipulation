# Awesome Embodied AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

A curated list of papers and resources on **Embodied AI**, covering Vision-Language-Action models, Video-Action models, World Models, and Unified architectures.

> Maintained by [@Noietch](https://github.com/Noietch). PRs welcome!

---

## 📌 Table of Contents

- [VLA — Vision-Language-Action Models](#vla--vision-language-action-models)
- [VA — Video-Action / Action Prediction](#va--video-action--action-prediction)
- [World Models](#world-models)
- [Unified / Foundation Models](#unified--foundation-models)
- [Benchmarks & Datasets](#benchmarks--datasets)
- [Contributing](#contributing)

---

## VLA — Vision-Language-Action Models

> Models that jointly process vision and language to produce robot actions.

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| OpenVLA: An Open-Source Vision-Language-Action Model | arXiv | 2024 | [Paper](https://arxiv.org/abs/2406.09246) \| [Code](https://github.com/openvla/openvla) | 7B VLA fine-tuned from Prismatic VLM on Open X-Embodiment |
| π0: A Vision-Language-Action Flow Model | arXiv | 2024 | [Paper](https://arxiv.org/abs/2410.24164) \| [Blog](https://www.physicalintelligence.company/blog/pi0) | Flow matching action head on top of PaliGemma; strong dexterous manipulation |
| RoboVLMs: Towards Generalizable & Efficient VLM for Embodied AI | arXiv | 2024 | [Paper](https://arxiv.org/abs/2406.09246) | Systematic study of VLM backbones for robot manipulation |
| Octo: An Open-Source Generalist Robot Policy | arXiv | 2023 | [Paper](https://arxiv.org/abs/2405.12213) \| [Code](https://github.com/octo-models/octo) | Transformer policy trained on 800k robot trajectories (Open X-Embodiment) |
| RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control | CoRL | 2023 | [Paper](https://arxiv.org/abs/2307.15818) | Fine-tuning PaLI-X / PaLM-E as robot policies; emergent chain-of-thought reasoning |

---

## VA — Video-Action / Action Prediction

> Models that predict actions conditioned on video observations, or jointly predict video and action.

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| GROOT: Learning to Follow Instructions by Watching Gameplay Videos | ICLR | 2024 | [Paper](https://arxiv.org/abs/2310.08235) \| [Code](https://github.com/CraftJarvis/GROOT) | Goal-conditioned policy from video; object-centric representation |
| UniSim: Learning Interactive Real-World Simulators | ICLR | 2024 | [Paper](https://arxiv.org/abs/2310.06114) | Unified video prediction model as a world simulator for robot manipulation |
| SuSIE: Zero-Shot Generalization to Novel Robot Environments | arXiv | 2023 | [Paper](https://arxiv.org/abs/2311.01775) | Video diffusion model as high-level planner + low-level policy |
| SWIM: Sliding Window Motion Planning for Action Anticipation | CVPR | 2024 | [Paper](https://arxiv.org/abs/2403.10793) | Sliding window video prediction for anticipating future actions |

---

## World Models

> Models that learn to simulate environment dynamics, enabling planning and policy learning.

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| DreamerV3: Mastering Diverse Domains through World Models | arXiv | 2023 | [Paper](https://arxiv.org/abs/2301.04104) \| [Code](https://github.com/danijar/dreamerv3) | RSSM-based world model; trains policies in imagination; achieves superhuman Atari |
| GAIA-1: A Generative World Model for Autonomous Driving | arXiv | 2023 | [Paper](https://arxiv.org/abs/2309.17080) | Autoregressive video generation as a world model for autonomous driving |
| IRASim: Learning Interactive Real-Robot Action Simulators | arXiv | 2024 | [Paper](https://arxiv.org/abs/2406.14540) | Interactive robot action simulator via video diffusion |
| RoboDreamer: Learning Compositional World Models for Robot Imagination | arXiv | 2024 | [Paper](https://arxiv.org/abs/2404.12377) | Compositional video generation for robot manipulation planning |
| V-JEPA: Revisiting Feature Prediction for Learning Visual Representations from Video | arXiv | 2024 | [Paper](https://arxiv.org/abs/2404.08471) \| [Code](https://github.com/facebookresearch/jepa) | Joint-embedding predictive architecture for video; strong spatiotemporal features |

---

## Unified / Foundation Models

> Models that unify multiple modalities and tasks under a single architecture.

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| Gato: A Generalist Agent | TMLR | 2022 | [Paper](https://arxiv.org/abs/2205.06175) | Single transformer trained on 604 tasks spanning text, images, and robot control |
| PaLM-E: An Embodied Multimodal Language Model | ICML | 2023 | [Paper](https://arxiv.org/abs/2303.03378) | 562B multimodal LLM with direct embodied reasoning; emergent zero-shot robot planning |
| 3D-VLA: A 3D Vision-Language-Action Generative World Model | ICML | 2024 | [Paper](https://arxiv.org/abs/2403.09631) \| [Code](https://github.com/UMass-Foundation-Model/3D-VLA) | Unified 3D perception + VLM + action generation with goal image prediction |
| RoboFlamingo: Vision-Language Models as Policy Networks for Manipulation | arXiv | 2023 | [Paper](https://arxiv.org/abs/2311.01378) \| [Code](https://github.com/RoboFlamingo/RoboFlamingo) | Fine-tuning OpenFlamingo for robot manipulation; strong few-shot generalization |
| OpenVLA-OFT: Efficient Fine-Tuning for VLA Models | arXiv | 2024 | [Paper](https://arxiv.org/abs/2411.19876) | Parallel decoding + action chunking for OpenVLA; 6× speedup |

---

## Benchmarks & Datasets

| Name | Type | Year | Links | Notes |
|------|------|------|-------|-------|
| LIBERO | Benchmark | 2023 | [Paper](https://arxiv.org/abs/2306.03310) \| [Code](https://github.com/Lifelong-Robot-Learning/LIBERO) | Lifelong robot learning benchmark; 130 tasks across 4 task suites |
| Open X-Embodiment | Dataset | 2023 | [Paper](https://arxiv.org/abs/2310.08864) \| [Data](https://robotics-transformer-x.github.io/) | 1M+ robot trajectories from 22 robots, 21 institutions |
| RLBench | Benchmark | 2020 | [Paper](https://arxiv.org/abs/1909.12271) \| [Code](https://github.com/stepjam/RLBench) | 100 diverse manipulation tasks with rich demonstrations |
| CALVIN | Benchmark | 2022 | [Paper](https://arxiv.org/abs/2112.03227) \| [Code](https://github.com/mees/calvin) | Long-horizon language-conditioned manipulation; chained 5-task evaluation |
| MetaWorld | Benchmark | 2019 | [Paper](https://arxiv.org/abs/1910.10897) \| [Code](https://github.com/Farama-Foundation/Metaworld) | 50 tabletop manipulation tasks; standard multi-task RL benchmark |

---

## Contributing

PRs welcome! Please follow the format:

```
| Paper Title | Venue | Year | [Paper](url) \| [Code](url) | One-sentence summary |
```

- Keep entries sorted by year (newest first within each section)
- TL;DR should be ≤ 15 words
- Add code link only if official implementation exists

---

⭐ Star this repo if you find it useful!
