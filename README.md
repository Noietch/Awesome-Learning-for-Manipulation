# Awesome Embodied AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![Stars](https://img.shields.io/github/stars/Noietch/Awesome-Embodied-AI)

> A comprehensive curated list of papers and resources on Embodied AI, covering VLA, VA, VLN, World Models, Benchmarks, Surveys, and leading Companies & Labs.
> Maintained by [@Noietch](https://github.com/Noietch). PRs welcome!

## Table of Contents

- [🤖 VLA — Vision-Language-Action Models](#-vla--vision-language-action-models)
- [🎬 VA — Video-Action Models](#-va--video-action-models)
- [🦾 Visuomotor Policies](#-visuomotor-policies)
- [🏭 Robot Foundation Model Tech Reports](#-robot-foundation-model-tech-reports)
- [🧭 VLN — Vision-Language Navigation](#-vln--vision-language-navigation)
- [🌍 World Models](#-world-models)
- [📊 Benchmarks & Datasets](#-benchmarks--datasets)
  - [Manipulation Benchmarks](#manipulation-benchmarks)
  - [Robot Datasets](#robot-datasets)
  - [Whole-body / Humanoid Benchmarks](#whole-body--humanoid-benchmarks)
  - [Autonomous Driving Benchmarks](#autonomous-driving-benchmarks)
- [📚 Survey](#-survey)
  - [Manipulation & Robot Learning](#manipulation--robot-learning-survey)
  - [Embodied AI General](#embodied-ai-general-survey)
  - [Autonomous Driving](#autonomous-driving-survey)
- [🏢 Companies & Labs](#-companies--labs)
- [🔗 Related Resources](#-related-resources)
- [Contributing](#contributing)

---

## 🤖 VLA — Vision-Language-Action Models

> Vision-Language-Action models that jointly process visual observations and language instructions to produce robot actions.

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [RT-1: Robotics Transformer for Real-World Control at Scale](https://arxiv.org/abs/2212.06817) | CoRL | 2022 | [Paper](https://arxiv.org/abs/2212.06817) | Transformer trained on 130k real-robot demos for multi-task control |
| [RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://arxiv.org/abs/2307.15818) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2307.15818) | VLM co-fine-tuned as action predictor; web knowledge → robotics |
| [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) | ICRA Best Paper | 2024 | [Paper](https://arxiv.org/abs/2310.08864) \| [Project](https://robotics-transformer-x.github.io/) | Cross-embodiment dataset + RT-X models at scale |
| [Octo: An Open-Source Generalist Robot Policy](https://arxiv.org/abs/2405.12213) | RSS | 2024 | [Paper](https://arxiv.org/abs/2405.12213) \| [Project](https://octo-models.github.io/) | Transformer policy trained on Open X-Embodiment data |
| [OpenVLA: An Open-Source Vision-Language-Action Model](https://arxiv.org/abs/2406.09246) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2406.09246) \| [Project](https://openvla.github.io/) | 7B VLA fine-tuned from Prismatic VLM; fully open-source |
| [UniPi: Learning Universal Policies via Text-Guided Video Generation](https://arxiv.org/abs/2302.00111) | NeurIPS | 2023 | [Paper](https://arxiv.org/abs/2302.00111) | Plan via video generation; actions extracted from video |
| [PaLM-E: An Embodied Multimodal Language Model](https://arxiv.org/abs/2303.03378) | ICML | 2023 | [Paper](https://arxiv.org/abs/2303.03378) | 562B multimodal model for embodied reasoning and planning |

### 2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [RDT-1B: a Diffusion Foundation Model for Bimanual Manipulation](https://arxiv.org/abs/2410.07864) | ICLR | 2025 | [Paper](https://arxiv.org/abs/2410.07864) \| [Project](https://rdt-robotics.github.io/rdt-robotics/) | 1B diffusion transformer for bimanual robot arms |
| [CogACT: A Foundational Vision-Language-Action Model for Synergizing Cognition and Action](https://arxiv.org/abs/2411.19650) | — | 2024 | [Paper](https://arxiv.org/abs/2411.19650) | Decouples cognition (VLM) from action via diffusion head |
| [HPT: Scaling Proprioceptive-Visual Learning with Heterogeneous Pre-Training](https://arxiv.org/abs/2409.20537) | NeurIPS | 2024 | [Paper](https://arxiv.org/abs/2409.20537) | Unified pre-training for diverse robot embodiments |
| [GR-2: Generative Video-Language-Action Model with Web-Scale Knowledge](https://arxiv.org/abs/2410.06158) | — | 2024 | [Paper](https://arxiv.org/abs/2410.06158) | Video generation as world model for robot manipulation |
| [3D-VLA: A 3D Vision-Language-Action Generative World Model](https://arxiv.org/abs/2403.09631) | ICML | 2024 | [Paper](https://arxiv.org/abs/2403.09631) | Grounded 3D perception with VLA and world model |
| [TinyVLA: Towards Fast, Data-Efficient Vision-Language-Action Models](https://arxiv.org/abs/2409.12514) | — | 2024 | [Paper](https://arxiv.org/abs/2409.12514) | Efficient VLA without large-scale robot pre-training |
| [Diffusion-VLA: Scaling Robot Foundation Models via Unified Diffusion and Autoregression](https://arxiv.org/abs/2412.03293) | — | 2024 | [Paper](https://arxiv.org/abs/2412.03293) | Unifies diffusion and autoregressive VLA in one model |
| [RT-H: Action Hierarchies Using Language](https://arxiv.org/abs/2403.01823) | — | 2024 | [Paper](https://arxiv.org/abs/2403.01823) | Hierarchical language-conditioned RT for long-horizon tasks |
| [OpenVLA-OFT: Fine-Tuning Vision-Language-Action Models: Optimizing Speed and Success](https://arxiv.org/abs/2502.19645) | RSS | 2025 | [Paper](https://arxiv.org/abs/2502.19645) \| [Project](https://openvla-oft.github.io/) | Parallel decoding + fine-tuning for fast OpenVLA |
| [Latent Action Pretraining from Videos](https://arxiv.org/abs/2410.11758) | — | 2024 | [Paper](https://arxiv.org/abs/2410.11758) | Learns latent actions from internet videos for zero-shot transfer |
| [HiRT: Enhancing Robotic Control with Hierarchical Robot Transformers](https://arxiv.org/abs/2410.05273) | — | 2024 | [Paper](https://arxiv.org/abs/2410.05273) | Two-level hierarchy: high-level VLM + low-level policy |
| [Robotic Control via Embodied Chain-of-Thought Reasoning](https://arxiv.org/abs/2407.08693) | — | 2024 | [Paper](https://arxiv.org/abs/2407.08693) | ECoT: step-by-step reasoning improves robot manipulation |
| [Moto: Latent Motion Token as the Bridging Language for Robot Manipulation](https://arxiv.org/abs/2412.04445) | — | 2024 | [Paper](https://arxiv.org/abs/2412.04445) | Discrete latent motion tokens bridge VLM and action |
| [TraceVLA: Visual Trace Prompting Enhances Spatial-Temporal Awareness](https://arxiv.org/abs/2412.10345) | — | 2024 | [Paper](https://arxiv.org/abs/2412.10345) | Visual traces as prompts for better spatial reasoning |
| [LLaRA: Supercharging Robot Learning Data for Vision-Language Policy](https://arxiv.org/abs/2406.20095) | — | 2024 | [Paper](https://arxiv.org/abs/2406.20095) | Data augmentation for VLA with interleaved language |
| [QUAR-VLA: Vision-Language-Action Model for Quadruped Robots](https://arxiv.org/abs/2312.14457) | — | 2024 | [Paper](https://arxiv.org/abs/2312.14457) | VLA adapted for quadruped locomotion and navigation |
| [General Flow as Foundation Affordance for Scalable Robot Learning](https://arxiv.org/abs/2401.11439) | — | 2024 | [Paper](https://arxiv.org/abs/2401.11439) \| [Project](https://general-flow.github.io/) | Optical flow as general robot affordance representation |
| [Towards Generalist Robot Policies: What Matters in Building Vision-Language-Action Models](https://arxiv.org/abs/2412.14058) | — | 2024 | [Paper](https://arxiv.org/abs/2412.14058) | Systematic study of design choices for generalist VLA |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [π0-FAST: Efficient Action Tokenization for Vision-Language-Action Models](https://arxiv.org/abs/2501.09747) | — | 2025 | [Paper](https://arxiv.org/abs/2501.09747) | Frequency-based action tokenization for fast π0 inference |
| [SpatialVLA: Exploring Spatial Representations for Visual-Language-Action Model](https://arxiv.org/abs/2501.15830) | — | 2025 | [Paper](https://arxiv.org/abs/2501.15830) | 3D-aware spatial tokens for better manipulation |
| [CoT-VLA: Visual Chain-of-Thought Reasoning for Vision-Language-Action Models](https://arxiv.org/abs/2503.22020) | CVPR | 2025 | [Paper](https://arxiv.org/abs/2503.22020) \| [Project](https://cot-vla.github.io/) | Explicit visual reasoning chain improves VLA performance |
| [RoboBrain: A Unified Brain Model for Robotic Manipulation from Abstract to Concrete](https://arxiv.org/abs/2502.21257) | CVPR | 2025 | [Paper](https://arxiv.org/abs/2502.21257) \| [Project](https://superrobobrain.github.io/) | Unified cognition-to-action model for manipulation |
| [HybridVLA: Collaborative Diffusion and Autoregression in a Unified VLA Model](https://arxiv.org/abs/2503.10631) | — | 2025 | [Paper](https://arxiv.org/abs/2503.10631) \| [Project](https://hybrid-vla.github.io/) | Jointly leverages diffusion and AR for robust policies |
| [Hi Robot: Open-Ended Instruction Following with Hierarchical VLAs](https://arxiv.org/abs/2502.19417) | — | 2025 | [Paper](https://arxiv.org/abs/2502.19417) \| [Project](https://www.pi.website/research/hirobot) | Two-level VLA: semantic planner + low-level controller |
| [DexVLA: Vision-Language Model with Plug-In Diffusion Expert for Robot Control](https://arxiv.org/abs/2502.05855) | — | 2025 | [Paper](https://arxiv.org/abs/2502.05855) | Modular VLA with plug-in diffusion action expert |
| [BridgeVLA: Input-Output Alignment for Efficient 3D Manipulation](https://arxiv.org/abs/2506.07961) | NeurIPS | 2025 | [Paper](https://arxiv.org/abs/2506.07961) \| [Project](https://bridgevla.github.io/) | Aligns 3D inputs/outputs for efficient VLA learning |
| [UniVLA: Unified Vision-Language-Action Model](https://arxiv.org/abs/2506.19850) | — | 2025 | [Paper](https://arxiv.org/abs/2506.19850) \| [Code](https://github.com/baaivision/UniVLA) | Single model unifying diverse manipulation tasks |
| [VLA-RL: Towards Masterful and General Robotic Manipulation with Scalable RL](https://arxiv.org/abs/2505.18719) | — | 2025 | [Paper](https://arxiv.org/abs/2505.18719) \| [Code](https://github.com/GuanxingLu/vlarl) | RL fine-tuning of VLA for general manipulation |
| [WorldVLA: Towards Autoregressive Action World Model](https://arxiv.org/abs/2506.21539) | — | 2025 | [Paper](https://arxiv.org/abs/2506.21539) \| [Code](https://github.com/alibaba-damo-academy/WorldVLA) | Unifies world model prediction with VLA action generation |
| [SmolVLA: A vision-language-action model for affordable and efficient robotics](https://arxiv.org/abs/2506.01844) | — | 2025 | [Paper](https://arxiv.org/abs/2506.01844) \| [Code](https://github.com/huggingface/lerobot) | HuggingFace compact VLA; integrates with LeRobot |
| [ConRFT: A Reinforced Fine-tuning Method for VLA Models via Consistency Policy](https://arxiv.org/abs/2502.05450) | RSS | 2025 | [Paper](https://arxiv.org/abs/2502.05450) \| [Project](https://cccedric.github.io/conrft/) | Consistency-based RL fine-tuning improves VLA robustness |
| [NORA: A Small Open-Sourced Generalist VLA Model for Embodied Tasks](https://arxiv.org/abs/2504.19854) | — | 2025 | [Paper](https://arxiv.org/abs/2504.19854) \| [Project](https://declare-lab.github.io/nora) | Lightweight open-source VLA for diverse robot tasks |
| [Embodied-R1: Reinforced Embodied Reasoning for General Robotic Manipulation](https://arxiv.org/abs/2508.13998) | — | 2025 | [Paper](https://arxiv.org/abs/2508.13998) \| [Code](https://github.com/pickxiguapi/Embodied-R1) | R1-style reasoning reinforcement for embodied manipulation |
| [InternVLA-M1: Spatially Guided VLA Framework for Generalist Robot Policy](https://arxiv.org/abs/2510.13778) | — | 2025 | [Paper](https://arxiv.org/abs/2510.13778) \| [Code](https://github.com/InternRobotics/InternVLA-M1) | InternRobotics' spatially grounded VLA framework |
| [X-VLA: Soft-Prompted Transformer as Scalable Cross-Embodiment VLA](https://arxiv.org/abs/2510.10274) | — | 2025 | [Paper](https://arxiv.org/abs/2510.10274) \| [Code](https://github.com/2toinf/X-VLA) | Cross-embodiment VLA via soft prompt adaptation |
| [RoboMonkey: Scaling Test-Time Sampling and Verification for VLAs](https://arxiv.org/abs/2506.17811) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2506.17811) \| [Code](https://github.com/robomonkey-vla/RoboMonkey) | Test-time compute scaling via sampling+verification |
| [GraspVLA: a Grasping Foundation Model Pre-trained on Billion-scale Synthetic Data](https://arxiv.org/abs/2505.03233) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2505.03233) \| [Code](https://github.com/PKU-EPIC/GraspVLA) | Billion-scale synthetic pre-training for universal grasping |
| [Long-VLA: Unleashing Long-Horizon Capability for Robot Manipulation](https://arxiv.org/abs/2508.19958) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2508.19958) \| [Project](https://long-vla.github.io/) | VLA for long-horizon multi-step manipulation tasks |
### 2026 (Preprints)

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [RDT2: Scaling Limit of UMI Data Towards Zero-Shot Cross-Embodiment](https://arxiv.org/abs/2602.03310) | — | 2026 | [Paper](https://arxiv.org/abs/2602.03310) \| [Code](https://github.com/thu-ml/RDT2) | Next-gen RDT scaling for cross-embodiment generalization |
| [DIAL: Decoupling Intent and Action via Latent World Modeling for End-to-End VLA](https://arxiv.org/abs/2603.29844) | — | 2026 | [Paper](https://arxiv.org/abs/2603.29844) | Bridges high-level intent and low-level actions via latent world model bottleneck |
| [FocusVLA: Focused Visual Utilization for Vision-Language-Action Models](https://arxiv.org/abs/2603.28740) | — | 2026 | [Paper](https://arxiv.org/abs/2603.28740) | Directs model attention to task-relevant visual patches to improve action quality |
| [MMaDA-VLA: Large Diffusion VLA with Unified Multi-Modal Instruction and Generation](https://arxiv.org/abs/2603.25406) | — | 2026 | [Paper](https://arxiv.org/abs/2603.25406) | Native discrete diffusion unifies language, images, and robot actions in one backbone |
| [ProgressVLA: Progress-Guided Diffusion Policy for Vision-Language Robotic Manipulation](https://arxiv.org/abs/2603.27670) | — | 2026 | [Paper](https://arxiv.org/abs/2603.27670) | Integrates task progress estimation as differentiable guidance for VLA policies |
| [VLA-OPD: Bridging Offline SFT and Online RL for VLA Models via On-Policy Distillation](https://arxiv.org/abs/2603.26666) | — | 2026 | [Paper](https://arxiv.org/abs/2603.26666) | On-policy distillation with reverse-KL combines SFT efficiency and RL robustness |

---

## 🎬 VA — Video-Action Models

> Models where video generation or video prediction is the core mechanism — video frames are the primary output or intermediate representation for robot action.

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [GR-1: Unleashing Large-Scale Video Generative Pre-training for Visual Robot Manipulation](https://arxiv.org/abs/2312.13139) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2312.13139) | Video prediction pretraining transferable to manipulation |
| [GROOT: Learning to Follow Instructions by Watching How Things Are Done](https://arxiv.org/abs/2310.08235) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2310.08235) | Segment-then-follow paradigm from observation videos |
| [SuSIE: Zero-Shot Robotic Manipulation with Pretrained Image-Editing Diffusion Models](https://arxiv.org/abs/2311.01775) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2311.01775) | Editing diffusion models as zero-shot robot subgoal generators |
| [IRASim: Learning Interactive Real-Robot Action Simulators](https://arxiv.org/abs/2406.14540) | — | 2024 | [Paper](https://arxiv.org/abs/2406.14540) | Interactive video generation model for robot simulation |
| [Video Generators Are Robot Policies](https://arxiv.org/abs/2406.16862) | — | 2025 | [Paper](https://arxiv.org/abs/2406.16862) \| [Project](https://videopolicy.cs.columbia.edu/) \| [Code](https://github.com/cvlab-columbia/videopolicy) | Video generation models directly serve as robot policies |

### 2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Video Prediction Policy: A Generalist Robot Policy with Predictive Visual Representations](https://arxiv.org/abs/2412.14803) | — | 2024 | [Paper](https://arxiv.org/abs/2412.14803) | Video future prediction as policy representation |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Unified Video Action Model](https://arxiv.org/abs/2503.00200) | RSS | 2025 | [Paper](https://arxiv.org/abs/2503.00200) \| [Project](https://unified-video-action-model.github.io/) | Joint video+action model for scalable robot learning |
| [Chain-of-Action: Trajectory Autoregressive Modeling for Robotic Manipulation](https://arxiv.org/abs/2506.09990) | — | 2025 | [Paper](https://arxiv.org/abs/2506.09990) \| [Project](https://chain-of-action.github.io/) | ByteDance Seed's autoregressive action trajectory model |
| [Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation](https://arxiv.org/abs/2412.15109) | — | 2025 | [Paper](https://arxiv.org/abs/2412.15109) \| [Project](https://nimolty.github.io/Seer/) | Predictive inverse dynamics for scalable manipulation |
| [Unified World Models: Coupling Video and Action Diffusion for Robot Pretraining](https://arxiv.org/abs/2504.02792) | — | 2025 | [Paper](https://arxiv.org/abs/2504.02792) \| [Project](https://weirdlabuw.github.io/uwm/) | Joint video-action diffusion for large-scale pretraining |

### 2026

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Causal World Modeling for Robot Control (LingBot-VA)](https://arxiv.org/abs/2601.21998) | — | 2026 | [Paper](https://arxiv.org/abs/2601.21998) \| [Code](https://github.com/robbyant/lingbot-va) | Causal video world model enables action learning without explicit action labels |
| [VAMPO: Policy Optimization for Improving Visual Dynamics in Video Action Models](https://arxiv.org/abs/2603.19370) | — | 2026 | [Paper](https://arxiv.org/abs/2603.19370) | Post-trains video action models with GRPO rewards over visual dynamics quality |
| [GigaWorld-Policy: An Efficient Action-Centered World-Action Model](https://arxiv.org/abs/2603.17240) | — | 2026 | [Paper](https://arxiv.org/abs/2603.17240) | Decouples video generation from action decoding for 9x faster inference |
| [DiT4DiT: Jointly Modeling Video Dynamics and Actions for Generalizable Robot Control](https://arxiv.org/abs/2603.10448) | — | 2026 | [Paper](https://arxiv.org/abs/2603.10448) | Couples video DiT and action DiT in a cascaded framework for joint training |
| [EVA: Aligning Video World Models with Executable Robot Actions via Inverse Dynamics Rewards](https://arxiv.org/abs/2603.17808) | — | 2026 | [Paper](https://arxiv.org/abs/2603.17808) | RL post-training aligns video generation with kinematically executable actions |
| [EgoSim: Egocentric World Simulator for Embodied Interaction Generation](https://arxiv.org/abs/2604.01001) | — | 2026 | [Paper](https://arxiv.org/abs/2604.01001) | Closed-loop egocentric simulator with updatable 3D scene state for interaction |

---

## 🦾 Visuomotor Policies

> Action policy models using diffusion, flow matching, or transformer-based imitation learning — without video generation as a core component.

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Diffusion Policy: Visuomotor Policy Learning via Action Diffusion](https://arxiv.org/abs/2303.04137) | RSS | 2023 | [Paper](https://arxiv.org/abs/2303.04137) \| [Code](https://github.com/columbia-ai-robotics/diffusion_policy) | DDPM-based policy for robot manipulation |
| [ACT: Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware](https://arxiv.org/abs/2304.13705) | RSS | 2023 | [Paper](https://arxiv.org/abs/2304.13705) \| [Code](https://github.com/tonyzhaozh/act) | CVAE + transformer for bimanual imitation |

### 2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [3D Diffusion Policy: Generalizable Visuomotor Policy Learning via 3D Representations](https://arxiv.org/abs/2403.03954) | RSS | 2025 | [Paper](https://arxiv.org/abs/2403.03954) | Point cloud observations for 3D-aware diffusion policies |
| [3D Diffuser Actor: Policy Diffusion with 3D Scene Representations](https://arxiv.org/abs/2402.10885) | — | 2024 | [Paper](https://arxiv.org/abs/2402.10885) | Language-conditioned diffusion in 3D scene feature space |
| [Consistency Policy: Accelerated Visuomotor Policies via Consistency Distillation](https://arxiv.org/abs/2405.07503) | — | 2024 | [Paper](https://arxiv.org/abs/2405.07503) | One-step diffusion policy via consistency model distillation |
| [One-Step Diffusion Policy: Fast Visuomotor Policies via Diffusion Distillation](https://arxiv.org/abs/2410.21257) | — | 2024 | [Paper](https://arxiv.org/abs/2410.21257) | Single-step inference for diffusion policy |
| [In-Context Imitation Learning via Next-Token Prediction](https://arxiv.org/abs/2408.15980) | — | 2024 | [Paper](https://arxiv.org/abs/2408.15980) \| [Project](https://icrt.dev/) | In-context robot learning via demo-conditioned autoregression |
| [Diffusion Policy Policy Optimization](https://arxiv.org/abs/2409.00588) | ICLR | 2025 | [Paper](https://arxiv.org/abs/2409.00588) | RL fine-tuning of diffusion policies |
| [Generalizable Humanoid Manipulation with Improved 3D Diffusion Policies](https://arxiv.org/abs/2410.10803) | — | 2024 | [Paper](https://arxiv.org/abs/2410.10803) | 3D diffusion policy adapted for humanoid whole-body |
| [Bidirectional Decoding: Improving Action Chunking via Closed-Loop Resampling](https://arxiv.org/abs/2408.17355) | — | 2024 | [Paper](https://arxiv.org/abs/2408.17355) | Bidirectional rollout improves temporal consistency |
| [GenDP: 3D Semantic Fields for Category-Level Generalizable Diffusion Policy](https://arxiv.org/abs/2410.17488) | — | 2024 | [Paper](https://arxiv.org/abs/2410.17488) | Generalizable diffusion via 3D semantic feature fields |
| [Scaling Diffusion Transformer to 1B Parameters for Robotic Manipulation](https://arxiv.org/abs/2409.14411) | — | 2024 | [Paper](https://arxiv.org/abs/2409.14411) | Scaling study for diffusion transformer policies |
| [Data Scaling Laws in Imitation Learning for Robotic Manipulation](https://arxiv.org/abs/2410.18647) | — | 2024 | [Paper](https://arxiv.org/abs/2410.18647) | Empirical data scaling laws for imitation learning |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Reactive Diffusion Policy: Slow-Fast Visual-Tactile Policy for Contact-Rich Manipulation](https://arxiv.org/abs/2503.02881) | RSS | 2025 | [Paper](https://arxiv.org/abs/2503.02881) \| [Project](https://reactive-diffusion-policy.github.io/) | Dual-speed diffusion policy with tactile feedback |
| [Streaming Flow Policy: Treating Action Trajectories as Flow Trajectories](https://arxiv.org/abs/2505.21851) | CoRL Oral | 2025 | [Paper](https://arxiv.org/abs/2505.21851) \| [Project](https://siddancha.github.io/streaming-flow-policy/) | Simplifies diffusion policies via streaming flow |
| [H3DP: Triply-Hierarchical Diffusion Policy for Visuomotor Learning](https://arxiv.org/abs/2505.07819) | — | 2025 | [Paper](https://arxiv.org/abs/2505.07819) \| [Project](https://lyy-iiis.github.io/h3dp/) | Three-level hierarchy in diffusion policy |
| [MoDE: Mixture of Experts Diffusion Policy for Multitask Learning](https://arxiv.org/abs/2412.12953) | ICLR | 2025 | [Paper](https://arxiv.org/abs/2412.12953) \| [Project](https://mbreuss.github.io/MoDE_Diffusion_Policy/) | MoE-based diffusion transformer for multi-task policies |
| [FlowPolicy: Fast 3D Flow-Based Policy via Consistency Flow Matching](https://arxiv.org/abs/2412.04987) | AAAI | 2025 | [Paper](https://arxiv.org/abs/2412.04987) \| [Code](https://github.com/zql-kk/FlowPolicy) | Consistency flow matching for fast 3D robot control |
| [Dex1B: Learning with 1B Demonstrations for Dexterous Manipulation](https://arxiv.org/abs/2506.17198) | RSS | 2025 | [Paper](https://arxiv.org/abs/2506.17198) \| [Project](https://jianglongye.com/dex1b/) | 1-billion demo pre-training for dexterous hands |
| [Dense Policy: Bidirectional Autoregressive Learning of Actions](https://arxiv.org/abs/2503.13217) | — | 2025 | [Paper](https://arxiv.org/abs/2503.13217) \| [Project](https://selen-suyue.github.io/DspNet/) | Bidirectional AR action sequence for rich action learning |
| [Phantom: Training Robots Without Robots Using Only Human Videos](https://arxiv.org/abs/2503.00779) | — | 2025 | [Paper](https://arxiv.org/abs/2503.00779) \| [Project](https://phantom-human-videos.github.io/) | Robot policy from human videos without robot data |
| [UniSkill: Imitating Human Videos via Cross-Embodiment Skill Representations](https://arxiv.org/abs/2505.08787) | — | 2025 | [Paper](https://arxiv.org/abs/2505.08787) \| [Project](https://kimhanjung.github.io/UniSkill/) | Cross-embodiment skill transfer from human video |
| [ZeroMimic: Distilling Robotic Manipulation Skills from Web Videos](https://arxiv.org/abs/2503.23877) | — | 2025 | [Paper](https://arxiv.org/abs/2503.23877) \| [Project](https://zeromimic.github.io/) | Zero-shot manipulation from web video via distillation |
| [DiWA: Diffusion Policy Adaptation with World Models](https://arxiv.org/abs/2508.03645) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2508.03645) \| [Code](https://github.com/acl21/diwa) | World model-guided diffusion policy adaptation |
| [CLAM: Continuous Latent Action Models for Robot Learning from Unlabeled Demos](https://arxiv.org/abs/2505.04999) | — | 2025 | [Paper](https://arxiv.org/abs/2505.04999) \| [Project](https://clamrobot.github.io/) | Continuous latent actions learned from unlabeled video |
| [Spatial Policy: Spatially-Aware Visuomotor Policy for Manipulation](https://arxiv.org/abs/2508.15874) | — | 2025 | [Paper](https://arxiv.org/abs/2508.15874) \| [Code](https://github.com/PlantPotatoOnMoon/SpatialPolicy) | Spatial reasoning integration into visuomotor policies |
| [Latent Diffusion Planning for Imitation Learning](https://arxiv.org/abs/2504.16925) | — | 2025 | [Paper](https://arxiv.org/abs/2504.16925) \| [Project](https://amberxie88.github.io/ldp/) | Latent space diffusion for long-horizon robot planning |
| [Sim-and-Real Co-Training: A Simple Recipe for Vision-Based Robotic Manipulation](https://arxiv.org/abs/2503.24361) | — | 2025 | [Paper](https://arxiv.org/abs/2503.24361) \| [Project](https://co-training.github.io/) | Simple co-training bridge between sim and real |
| [Humanoid Policy ~ Human Policy](https://arxiv.org/abs/2503.13441) | — | 2025 | [Paper](https://arxiv.org/abs/2503.13441) \| [Project](https://human-as-robot.github.io/) | Direct transfer from human motion policy to humanoid |
| [GauDP: Multi-Agent Collaboration through Gaussian-Image Synergy in Diffusion Policies](https://arxiv.org/abs/2511.00998) | NeurIPS | 2025 | [Paper](https://arxiv.org/abs/2511.00998) \| [Project](https://ziyeeee.github.io/gaudp.io/) | Gaussian splatting + diffusion for multi-robot policies |
| [ASAP: Aligning Simulation and Real-World Physics for Humanoid Whole-Body Skills](https://arxiv.org/abs/2502.01143) | — | 2025 | [Paper](https://arxiv.org/abs/2502.01143) | Sim-to-real alignment for agile humanoid locomotion |
| [ManipTrans: Efficient Dexterous Bimanual Manipulation Transfer via Residual Learning](https://arxiv.org/abs/2503.21860) | — | 2025 | [Paper](https://arxiv.org/abs/2503.21860) \| [Project](https://maniptrans.github.io/) | Residual learning for bimanual dexterous transfer |

### 2026

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Cosmos Policy: Fine-Tuning Video Models for Visuomotor Control and Planning](https://arxiv.org/abs/2601.16163) | — | 2026 | [Paper](https://arxiv.org/abs/2601.16163) | Adapts large pretrained video model into robot policy via single-stage fine-tuning |
| [Robot-DIFT: Distilling Diffusion Features for Geometrically Consistent Visuomotor Control](https://arxiv.org/abs/2602.11934) | — | 2026 | [Paper](https://arxiv.org/abs/2602.11934) | Distills generative diffusion geometry priors into a deterministic control backbone |
| [One-Step Flow Policy: Self-Distillation for Fast Visuomotor Policies](https://arxiv.org/abs/2603.12480) | — | 2026 | [Paper](https://arxiv.org/abs/2603.12480) | Single-step action generation via self-consistency + self-guided mode sharpening |
| [Ada3Drift: Adaptive Training-Time Drifting for One-Step 3D Visuomotor Manipulation](https://arxiv.org/abs/2603.11984) | — | 2026 | [Paper](https://arxiv.org/abs/2603.11984) | Shifts iterative denoising from inference to training for 1-NFE 3D policy |
| [HiFlow: Tokenization-Free Scale-Wise Autoregressive Policy Learning via Flow Matching](https://arxiv.org/abs/2603.27281) | — | 2026 | [Paper](https://arxiv.org/abs/2603.27281) | Coarse-to-fine autoregressive policy on continuous actions without tokenization |
| [VPWEM: Non-Markovian Visuomotor Policy with Working and Episodic Memory](https://arxiv.org/abs/2603.04910) | — | 2026 | [Paper](https://arxiv.org/abs/2603.04910) | Combines sliding-window working memory and compressed episodic memory in diffusion policy |

---

## 🏭 Robot Foundation Model Tech Reports

> Technical reports and system papers from industry organizations and robot companies, describing large-scale foundation models for robotics.

| System | Organization | Year | Links | TL;DR |
|--------|-------------|------|-------|-------|
| [π0: A Vision-Language-Action Flow Model for General Robot Control](https://arxiv.org/abs/2410.24164) | Physical Intelligence | 2024 | [Paper](https://arxiv.org/abs/2410.24164) | Flow-matching VLA; dexterous multi-task control |
| [π0.5: A Vision-Language-Action Model with Open-World Generalization](https://arxiv.org/abs/2504.16054) | Physical Intelligence | 2025 | [Paper](https://arxiv.org/abs/2504.16054) \| [Project](https://www.pi.website/blog/pi05) | π0 generalized to open-world settings |
| [GR00T N1: An Open Foundation Model for Generalist Humanoid Robots](https://arxiv.org/abs/2503.14734) | NVIDIA | 2025 | [Paper](https://arxiv.org/abs/2503.14734) \| [Code](https://github.com/NVIDIA/Isaac-GR00T) | NVIDIA open humanoid foundation model |
| [Gemini Robotics: Bringing AI into the Physical World](https://storage.googleapis.com/deepmind-media/gemini-robotics/gemini_robotics_report.pdf) | Google DeepMind | 2025 | [Report](https://storage.googleapis.com/deepmind-media/gemini-robotics/gemini_robotics_report.pdf) | Google DeepMind multimodal robot control system |
| [Helix: A Vision-Language-Action Model for Generalist Humanoid Control](https://www.figure.ai/news/helix) | Figure AI | 2025 | [Report](https://www.figure.ai/news/helix) | Figure AI's dual-system VLA for humanoid control |
| [GR-3 Technical Report](https://arxiv.org/abs/2507.15493) | ByteDance Seed | 2025 | [Paper](https://arxiv.org/abs/2507.15493) \| [Project](https://seed.bytedance.com/GR3) | ByteDance Seed's third-gen generative robot policy |
| [EnerVerse: Envisioning Embodied Future Space for Robotics Manipulation](https://arxiv.org/abs/2501.01895) | AgiBot (星动纪元) | 2025 | [Paper](https://arxiv.org/abs/2501.01895) | AgiBot's generative future-state model for manipulation |
| [Being-H0: Vision-Language-Action Pretraining from Large-Scale Human Videos](https://arxiv.org/abs/2507.15597) | BeingBeyond | 2025 | [Paper](https://arxiv.org/abs/2507.15597) \| [Code](https://github.com/BeingBeyond/Being-H0) | Humanoid pretraining from egocentric human video |
| [GigaBrain-0: A World Model-Powered Vision-Language-Action Model](https://arxiv.org/abs/2510.19430) | GigaAI | 2025 | [Paper](https://arxiv.org/abs/2510.19430) \| [Code](https://github.com/open-gigaai/giga-brain-0) | World model-powered VLA |
| [A Pragmatic VLA Foundation Model (LingBot-VLA)](https://arxiv.org/abs/2601.18692) | RobbyAnt (Xiaomi) | 2026 | [Paper](https://arxiv.org/abs/2601.18692) \| [Project](https://technology.robbyant.com/lingbot-vla/) \| [Code](https://github.com/Robbyant/lingbot-vla/) | Xiaomi RobbyAnt's pragmatic VLA foundation model for robot manipulation |
| [Causal World Modeling for Robot Control (LingBot-VA)](https://arxiv.org/abs/2601.21998) | RobbyAnt (Xiaomi) | 2026 | [Paper](https://arxiv.org/abs/2601.21998) \| [Project](https://technology.robbyant.com/lingbot-va) \| [Code](https://github.com/robbyant/lingbot-va) | Video world modeling + VL pre-training for robot learning |

---

## 🧭 VLN — Vision-Language Navigation

> Models for navigating environments guided by natural language instructions.

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [VLN-BERT: Improving Vision-and-Language Navigation with Image-Text Pairs from the Web](https://arxiv.org/abs/2004.14973) | CVPR | 2021 | [Paper](https://arxiv.org/abs/2004.14973) | BERT pretrained on image-text for VLN |
| [DUET: Dual-Scale Graph Transformer for Vision-and-Language Navigation](https://arxiv.org/abs/2202.11742) | CVPR | 2022 | [Paper](https://arxiv.org/abs/2202.11742) | Fine- and coarse-grained dual-scale navigation transformer |
| [NavGPT: Explicit Reasoning in Vision-and-Language Navigation with LLMs](https://arxiv.org/abs/2305.16986) | AAAI | 2024 | [Paper](https://arxiv.org/abs/2305.16986) | GPT-based zero-shot navigation via explicit reasoning |
| [MapGPT: Map-Guided Prompting with Adaptive Path Planning for VLN](https://arxiv.org/abs/2401.07314) | ACL | 2024 | [Paper](https://arxiv.org/abs/2401.07314) | Map-conditioned LLM prompting for VLN path planning |
| [EmbodiedScan: A Holistic Multi-Modal 3D Perception Suite for Embodied AI](https://arxiv.org/abs/2312.16170) | CVPR | 2024 | [Paper](https://arxiv.org/abs/2312.16170) | Multi-modal 3D scene understanding for embodied agents |

### 2023–2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Bridging Zero-shot Object Navigation and Foundation Models through Pixel-Guided Navigation Skill](https://arxiv.org/abs/2309.10309) | ICRA | 2024 | [Paper](https://arxiv.org/abs/2309.10309) | Pixel-level affordance for zero-shot object navigation |
| [Mobility VLA: Multimodal Instruction Navigation with Long-Context VLMs and Topological Graphs](https://arxiv.org/abs/2407.07775) | — | 2024 | [Paper](https://arxiv.org/abs/2407.07775) | Long-context VLM over topological graph for navigation |
| [NaViD: Video-based VLM Plans the Next Step for Vision-and-Language Navigation](https://arxiv.org/abs/2402.15852) | RSS | 2024 | [Paper](https://arxiv.org/abs/2402.15852) | Video-conditioned VLM plans navigation waypoints |
| [The One RING: a Robotic Indoor Navigation Generalist](https://arxiv.org/abs/2412.14401) | — | 2024 | [Paper](https://arxiv.org/abs/2412.14401) | Generalist indoor navigation model |
| [CANVAS: Commonsense-Aware Navigation System for Intuitive Human-Robot Interaction](https://arxiv.org/abs/2410.01273) | — | 2024 | [Paper](https://arxiv.org/abs/2410.01273) \| [Project](https://worv-ai.github.io/canvas/) | Commonsense-guided navigation for human-robot interaction |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [NaVILA: Legged Robot Vision-Language-Action Model for Navigation](https://arxiv.org/abs/2412.04453) | RSS | 2025 | [Paper](https://arxiv.org/abs/2412.04453) \| [Project](https://navila-bot.github.io/) | VLA adapted for legged robot navigation |
| [OctoNav: Towards Generalist Embodied Navigation](https://arxiv.org/abs/2506.09839) | — | 2025 | [Paper](https://arxiv.org/abs/2506.09839) \| [Project](https://buaa-colalab.github.io/OctoNav/) | Generalist navigation model for diverse tasks |
| [UniGoal: Towards Universal Zero-shot Goal-oriented Navigation](https://arxiv.org/abs/2503.10630) | — | 2025 | [Paper](https://arxiv.org/abs/2503.10630) \| [Project](https://bagh2178.github.io/UniGoal/) | Zero-shot universal goal-oriented navigation |
| [WMNav: Integrating VLMs into World Models for Object Goal Navigation](https://arxiv.org/abs/2503.02247) | — | 2025 | [Paper](https://arxiv.org/abs/2503.02247) \| [Project](https://b0b8k1ng.github.io/WMNav/) | World model-guided VLM for object navigation |
| [MapNav: Memory Representation via Annotated Semantic Maps for VLM-based VLN](https://arxiv.org/abs/2502.13451) | — | 2025 | [Paper](https://arxiv.org/abs/2502.13451) | Semantic map memory for VLM-based navigation |
| [OpenFly: Large-scale Benchmark for Aerial Vision-Language Navigation](https://arxiv.org/abs/2502.18041) | — | 2025 | [Paper](https://arxiv.org/abs/2502.18041) | UAV VLN benchmark with diverse aerial scenarios |
| [ApexNav: Adaptive Exploration Strategy for Zero-Shot Object Navigation](https://arxiv.org/abs/2504.14478) | RA-L | 2025 | [Paper](https://arxiv.org/abs/2504.14478) \| [Project](https://robotics-star.com/ApexNav) | Adaptive semantic fusion for zero-shot navigation |
| [TopV-Nav: Top-View Spatial Reasoning for Zero-shot Object Navigation](https://arxiv.org/abs/2411.16425) | — | 2025 | [Paper](https://arxiv.org/abs/2411.16425) | Bird's-eye view spatial reasoning for MLLM navigation |
| [VL-Nav: Real-time Vision-Language Navigation with Spatial Reasoning](https://arxiv.org/abs/2502.00931) | — | 2025 | [Paper](https://arxiv.org/abs/2502.00931) | Spatial reasoning VLN for real-time robot navigation |
| [CityNavAgent: Aerial VLN with Hierarchical Semantic Planning](https://arxiv.org/abs/2505.05622) | — | 2025 | [Paper](https://arxiv.org/abs/2505.05622) \| [Code](https://github.com/VinceOuti/CityNavAgent) | Hierarchical planning for city-scale aerial navigation |
| [Embodied Navigation Foundation Model](https://arxiv.org/abs/2509.12129) | — | 2025 | [Paper](https://arxiv.org/abs/2509.12129) \| [Project](https://pku-epic.github.io/NavFoM-Web/) | Large foundation model for embodied navigation |
| [GC-VLN: Instruction as Graph Constraints for Training-free VLN](https://arxiv.org/abs/2509.10454) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2509.10454) \| [Code](https://github.com/bagh2178/GC-VLN) | Graph constraint-based training-free VLN |
| [OmniVLA: Omni-Modal VLA Model for Robot Navigation](https://arxiv.org/abs/2509.19480) | — | 2025 | [Paper](https://arxiv.org/abs/2509.19480) \| [Code](https://github.com/NHirose/OmniVLA) | Omni-modal inputs for unified robot navigation |
| [Ground Slow, Move Fast: Dual-System Foundation Model for Generalizable VLN](https://arxiv.org/abs/2512.08186) | — | 2025 | [Paper](https://arxiv.org/abs/2512.08186) \| [Code](https://github.com/InternRobotics/InternNav) | System 1/2 VLN: fast movement + slow grounding |
| [JanusVLN: Decoupling Semantics and Spatiality for Vision-Language Navigation](https://arxiv.org/abs/2509.22548) | — | 2025 | [Paper](https://arxiv.org/abs/2509.22548) \| [Code](https://github.com/MIV-XJTU/JanusVLN) | Dual implicit memory for semantic/spatial decoupling |
| [ForesightNav: Learning Scene Imagination for Efficient Exploration](https://arxiv.org/abs/2504.16062) | — | 2025 | [Paper](https://arxiv.org/abs/2504.16062) \| [Code](https://github.com/uzh-rpg/foresight-nav) | Future scene imagination for efficient navigation |
| [NavDP: Sim-to-Real Navigation Diffusion Policy](https://arxiv.org/abs/2505.08712) | — | 2025 | [Paper](https://arxiv.org/abs/2505.08712) | Diffusion policy with privileged info for robot navigation |
| [TRAVEL: Training-Free Retrieval and Alignment for VLN](https://arxiv.org/abs/2502.07306) | — | 2025 | [Paper](https://arxiv.org/abs/2502.07306) | Training-free retrieval augmentation for VLN agents |
| [LOVON: Legged Open-Vocabulary Object Navigator](https://arxiv.org/abs/2507.06747) | — | 2025 | [Paper](https://arxiv.org/abs/2507.06747) \| [Project](https://daojiepeng.github.io/LOVON/) | Legged robot open-vocabulary object navigation |
| [CorrectNav: Self-Correction Flywheel for Vision-Language-Action Navigation](https://arxiv.org/abs/2508.10416) | — | 2025 | [Paper](https://arxiv.org/abs/2508.10416) \| [Project](https://correctnav.github.io/) | Self-correction loop for robust VLA navigation |
| [TrackVLA++: Reasoning and Memory for Embodied Visual Tracking](https://arxiv.org/abs/2510.07134) | — | 2025 | [Paper](https://arxiv.org/abs/2510.07134) \| [Project](https://pku-epic.github.io/TrackVLA-plus-plus-Web/) | Extended VLA for visual object tracking in navigation |

### 2026

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [LatentPilot: Scene-Aware VLN by Dreaming Ahead with Latent Visual Reasoning](https://arxiv.org/abs/2603.29165) | — | 2026 | [Paper](https://arxiv.org/abs/2603.29165) | Flywheel training + action-conditioned latent tokens let agent dream ahead without future frames |
| [AgentVLN: Towards Agentic Vision-and-Language Navigation](https://arxiv.org/abs/2603.17670) | — | 2026 | [Paper](https://arxiv.org/abs/2603.17670) | VLM-as-Brain with cross-space 3D waypoint mapping and QD-PCoT for edge deployment |
| [OmniVLN: Omnidirectional 3D Perception for VLN across Air and Ground Platforms](https://arxiv.org/abs/2603.17351) | — | 2026 | [Paper](https://arxiv.org/abs/2603.17351) | LiDAR + panoramic vision with hierarchical DSG reasoning for token-efficient navigation |
| [Language-Conditioned World Modeling for Visual Navigation (LCVN)](https://arxiv.org/abs/2603.26741) | — | 2026 | [Paper](https://arxiv.org/abs/2603.26741) | Diffusion world model + actor-critic trained in latent space for instruction-conditioned navigation |
| [PiJEPA: Policy-Guided World Model Planning for Language-Conditioned Visual Navigation](https://arxiv.org/abs/2603.25981) | — | 2026 | [Paper](https://arxiv.org/abs/2603.25981) | Policy priors warm-start MPPI planning over JEPA world model for faster convergence |
| [SpatialPoint: Spatial-aware Point Prediction for Embodied Localization](https://arxiv.org/abs/2603.26690) | — | 2026 | [Paper](https://arxiv.org/abs/2603.26690) | RGB-D VLM framework predicting 3D touchable/air points for navigation and grasping |

---

## 🌍 World Models

> Models that learn to simulate the world, predict future states, or enable planning through internal simulation.

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [DreamerV3: Mastering Diverse Domains through World Models](https://arxiv.org/abs/2301.04104) | — | 2023 | [Paper](https://arxiv.org/abs/2301.04104) \| [Code](https://github.com/danijar/dreamerv3) | Learns world model in latent space; zero-shot transfer |
| [GAIA-1: A Generative World Model for Autonomous Driving](https://arxiv.org/abs/2309.17080) | — | 2023 | [Paper](https://arxiv.org/abs/2309.17080) | Waymo's generative video world model for autonomous driving |
| [V-JEPA: Self-Supervised Learning from Video by Predicting Latent Representations](https://arxiv.org/abs/2404.08471) | NeurIPS | 2024 | [Paper](https://arxiv.org/abs/2404.08471) \| [Code](https://github.com/facebookresearch/jepa) | Efficient video understanding via latent prediction |
| [Pandora: Towards General World Model with Natural Language Actions and Video States](https://arxiv.org/abs/2406.09455) | — | 2024 | [Paper](https://arxiv.org/abs/2406.09455) | Language-action conditioned video world model |

### 2023–2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [RoboDreamer: Learning Compositional World Models for Robot Imagination](https://arxiv.org/abs/2404.12377) | — | 2024 | [Paper](https://arxiv.org/abs/2404.12377) | Compositional video-based world model for robot planning |
| [UniSim: Learning Interactive Real-World Simulators](https://arxiv.org/abs/2310.06114) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2310.06114) | Universal simulator trained on real-world video data |
| [IRASim: Learning Interactive Real-Robot Action Simulators](https://arxiv.org/abs/2406.14540) | — | 2024 | [Paper](https://arxiv.org/abs/2406.14540) | Action-conditioned interactive simulation for robots |
| [Genesis: A Generative and Universal Physics Engine for Robotics](https://genesis-embodied-ai.github.io/) | — | 2024 | [Project](https://genesis-embodied-ai.github.io/) | Generative physics engine for robot simulation |
| [Wan2.1: Open and Advanced Large-Scale Video Generative Models](https://arxiv.org/abs/2503.20314) | — | 2025 | [Paper](https://arxiv.org/abs/2503.20314) \| [Code](https://github.com/Wan-Video/Wan2.1) | Wan2.1 powerful open video world model |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning](https://arxiv.org/abs/2506.09985) | — | 2025 | [Paper](https://arxiv.org/abs/2506.09985) \| [Code](https://github.com/facebookresearch/vjepa2) | Action-conditioned V-JEPA for robot planning |
| [Cosmos: World Foundation Model Platform for Physical AI](https://arxiv.org/abs/2501.03575) | — | 2025 | [Paper](https://arxiv.org/abs/2501.03575) \| [Code](https://github.com/nvidia-cosmos/cosmos-predict1) | NVIDIA's world foundation model for physical AI |
| [Sora (Technical Report)](https://openai.com/sora) | — | 2024 | [Blog](https://openai.com/sora) | OpenAI's large-scale text-to-video world model |
| [EWMBench: Evaluating Scene, Motion, and Semantic Quality in Embodied World Models](https://arxiv.org/abs/2505.09694) | — | 2025 | [Paper](https://arxiv.org/abs/2505.09694) \| [Code](https://github.com/AgibotTech/EWMBench) | Benchmark for evaluating embodied world models |
| [AdaWorld: Learning Adaptable World Models with Latent Actions](https://arxiv.org/abs/2503.18938) | — | 2025 | [Paper](https://arxiv.org/abs/2503.18938) \| [Project](https://adaptable-world-model.github.io/) | Adaptable world models via latent action discovery |
| [DyWA: Dynamics-adaptive World Action Model for Non-prehensile Manipulation](https://arxiv.org/abs/2503.16806) | — | 2025 | [Paper](https://arxiv.org/abs/2503.16806) \| [Project](https://pku-epic.github.io/DyWA/) | Dynamics-adaptive world model for pushing tasks |
| [Generalist World Model Pre-Training for Efficient Reinforcement Learning](https://arxiv.org/abs/2502.19544) | — | 2025 | [Paper](https://arxiv.org/abs/2502.19544) | Generalist world model pretraining for RL policies |
| [Unified World Models: Coupling Video and Action Diffusion for Robot Pretraining](https://arxiv.org/abs/2504.02792) | — | 2025 | [Paper](https://arxiv.org/abs/2504.02792) \| [Project](https://weirdlabuw.github.io/uwm/) | Joint video+action diffusion for world model pretraining |
| [FlowDreamer: RGB-D World Model with Flow-based Motion for Manipulation](https://arxiv.org/abs/2505.10075) | — | 2025 | [Paper](https://arxiv.org/abs/2505.10075) \| [Project](https://sharinka0715.github.io/FlowDreamer/) | Optical flow-based RGB-D world model for manipulation |
| [WorldVLA: Towards Autoregressive Action World Model](https://arxiv.org/abs/2506.21539) | — | 2025 | [Paper](https://arxiv.org/abs/2506.21539) \| [Code](https://github.com/alibaba-damo-academy/WorldVLA) | Autoregressive VLA that jointly models world states |
| [Robotic World Model: Neural Network Simulator for Policy Optimization](https://arxiv.org/abs/2501.10100) | — | 2025 | [Paper](https://arxiv.org/abs/2501.10100) | Neural network as high-fidelity robotic world simulator |
| [World4Omni: Zero-Shot Framework from Image Generation World Model to Robotic Manipulation](https://arxiv.org/abs/2506.23919) | — | 2025 | [Paper](https://arxiv.org/abs/2506.23919) \| [Project](https://world4omni.github.io/) | Image generation world model for zero-shot manipulation |
| [Evaluating Robot Policies in a World Model](https://arxiv.org/abs/2506.00613) | — | 2025 | [Paper](https://arxiv.org/abs/2506.00613) \| [Project](https://world-model-eval.github.io/) | World model as robot policy evaluation environment |
| [3DFlowAction: Cross-Embodiment Manipulation from 3D Flow World Model](https://arxiv.org/abs/2506.06199) | — | 2025 | [Paper](https://arxiv.org/abs/2506.06199) \| [Code](https://github.com/Hoyyyaard/3DFlowAction/) | 3D flow world model for cross-embodiment manipulation |
| [LaDi-WM: Latent Diffusion-based World Model for Predictive Manipulation](https://arxiv.org/abs/2505.11528) | — | 2025 | [Paper](https://arxiv.org/abs/2505.11528) | Latent diffusion world model for manipulation prediction |
| [PointWorld: Scaling 3D World Models for In-The-Wild Robotic Manipulation](https://arxiv.org/abs/2601.03782) | — | 2026 | [Paper](https://arxiv.org/abs/2601.03782) \| [Project](https://point-world.github.io/) | 3D point cloud world models at scale |
| [GAF: Gaussian Action Field as a Dynamic World Model for Robotic Manipulation](https://arxiv.org/abs/2506.14135) | — | 2025 | [Paper](https://arxiv.org/abs/2506.14135) | Gaussian splatting as dynamic world model |

### 2026

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [PlayWorld: Learning Robot World Models from Autonomous Play](https://arxiv.org/abs/2603.09030) | — | 2026 | [Paper](https://arxiv.org/abs/2603.09030) | Trains high-fidelity video world models entirely from unsupervised robot self-play |
| [Kinema4D: Kinematic 4D World Modeling for Spatiotemporal Embodied Simulation](https://arxiv.org/abs/2603.16669) | — | 2026 | [Paper](https://arxiv.org/abs/2603.16669) | URDF-driven 4D robot trajectory controls generative model for robot-world interaction |
| [HCLSM: Hierarchical Causal Latent State Machines for Object-Centric World Modeling](https://arxiv.org/abs/2603.29090) | — | 2026 | [Paper](https://arxiv.org/abs/2603.29090) | Three-level temporal dynamics with slot attention for causal object-centric world model |

---

## 📊 Benchmarks & Datasets

### Manipulation Benchmarks

| Benchmark | Year | Links | Description |
|-----------|------|-------|-------------|
| [RLBench: The Robot Learning Benchmark & Learning Environment](https://arxiv.org/abs/1909.12271) | 2019 | [Paper](https://arxiv.org/abs/1909.12271) \| [Code](https://github.com/stepjam/RLBench) | 100 robot manipulation tasks in CoppeliaSim |
| [MetaWorld: A Benchmark and Evaluation for Multi-Task and Meta Reinforcement Learning](https://arxiv.org/abs/1910.10897) | 2019 | [Paper](https://arxiv.org/abs/1910.10897) \| [Code](https://github.com/Farama-Foundation/Metaworld) | 50 diverse robot arm tasks for meta/multi-task RL |
| [CALVIN: A Benchmark for Language-Conditioned Policy Learning for Long-Horizon Robot Manipulation](https://arxiv.org/abs/2112.03227) | ICRA 2022 | [Paper](https://arxiv.org/abs/2112.03227) \| [Code](https://github.com/mees/calvin) | Long-horizon language-conditioned manipulation chains |
| [LIBERO: Benchmarking Knowledge Transfer for Lifelong Robot Learning](https://arxiv.org/abs/2306.03310) | NeurIPS 2023 | [Paper](https://arxiv.org/abs/2306.03310) \| [Code](https://github.com/Lifelong-Robot-Learning/LIBERO) | Lifelong learning benchmark with 130 robot manipulation tasks |
| [SimplerEnv: Simulated Manipulation Policy Evaluation Environments for Real Robot Setups](https://arxiv.org/abs/2405.05941) | — | 2024 | [Paper](https://arxiv.org/abs/2405.05941) \| [Code](https://github.com/simpler-env/SimplerEnv) | Sim evaluation mirroring real-world robot setups |
| [FurnitureBench: Reproducible Real-World Benchmark for Long-Horizon Complex Manipulation](https://arxiv.org/abs/2305.12556) | RSS | 2023 | [Paper](https://arxiv.org/abs/2305.12556) \| [Code](https://github.com/clvrai/furniture-bench) | Assembly of real IKEA furniture; long-horizon challenge |
| [ManiSkill3: GPU Parallelized Robotics Simulation and Rendering](https://arxiv.org/abs/2410.00425) | — | 2024 | [Paper](https://arxiv.org/abs/2410.00425) \| [Code](https://github.com/haosulab/ManiSkill) | GPU-accelerated simulation benchmark; v1-v3 series |
| [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) | ICRA | 2024 | [Paper](https://arxiv.org/abs/2310.08864) \| [Project](https://robotics-transformer-x.github.io/) | Cross-embodiment dataset with 500k+ real-robot demos |
| [VLABench: Large-Scale Benchmark for Language-Conditioned Robotics Manipulation](https://arxiv.org/abs/2412.18194) | — | 2024 | [Paper](https://arxiv.org/abs/2412.18194) | Long-horizon language-conditioned manipulation evaluation |
| [RoboTwin: Dual-Arm Robot Benchmark with Generative Digital Twins](https://arxiv.org/abs/2409.02920) | CVPR | 2025 | [Paper](https://arxiv.org/abs/2409.02920) \| [Code](https://github.com/TianxingChen/RoboTwin) | Dual-arm manipulation with generative digital twin data |
| [RoboTwin 2.0: Scalable Data Generator and Benchmark with Strong Domain Randomization](https://arxiv.org/abs/2506.18088) | — | 2025 | [Paper](https://arxiv.org/abs/2506.18088) \| [Project](https://robotwin-platform.github.io/) | Extended RoboTwin with large-scale domain randomization |
| [RoboVerse: Unified Platform, Dataset and Benchmark for Scalable Robot Learning](https://roboverseorg.github.io/) | — | 2025 | [Paper](https://roboverseorg.github.io/static/pdfs/paper_supp_20250405_1820.pdf) \| [Code](https://github.com/RoboVerseOrg/RoboVerse) | Unified sim-to-real benchmark and dataset platform |
| [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://arxiv.org/abs/2506.18123) | — | 2025 | [Paper](https://arxiv.org/abs/2506.18123) \| [Project](https://robo-arena.github.io/) | Distributed real-world evaluation platform |
| [RoboCerebra: Large-scale Benchmark for Long-horizon Robotic Manipulation](https://arxiv.org/abs/2506.06677) | — | 2025 | [Paper](https://arxiv.org/abs/2506.06677) \| [Project](https://robocerebra.github.io/) | Long-horizon manipulation evaluation with dense annotations |
| [ManipBench: Benchmarking VLMs for Low-Level Robot Manipulation](https://arxiv.org/abs/2505.09698) | — | 2025 | [Paper](https://arxiv.org/abs/2505.09698) \| [Project](https://manipbench.github.io/) | VLM capability evaluation for manipulation |
| [BOSS: Benchmark for Observation Space Shift in Long-Horizon Tasks](https://arxiv.org/abs/2502.15679) | — | 2025 | [Paper](https://arxiv.org/abs/2502.15679) | Benchmark for handling observation distribution shift |
| [AutoEval: Autonomous Evaluation of Generalist Robot Manipulation Policies in Real World](https://arxiv.org/abs/2503.24278) | — | 2025 | [Paper](https://arxiv.org/abs/2503.24278) \| [Project](https://auto-eval.github.io/) | Automated real-world manipulation policy evaluation |

### Robot Datasets

| Dataset | Venue | Year | Links | Description |
|---------|-------|------|-------|-------------|
| [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) | ICRA Best Paper | 2024 | [Paper](https://arxiv.org/abs/2310.08864) \| [Project](https://robotics-transformer-x.github.io/) | 1M+ real-robot demos from 22 robots and 21 institutions |
| [BridgeData V2: A Dataset for Robot Learning at Scale](https://arxiv.org/abs/2308.12952) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2308.12952) \| [Project](https://rail-berkeley.github.io/bridgedata/) | 60k+ kitchen manipulation demonstrations |
| [DROID: A Large-Scale In-the-Wild Robot Manipulation Dataset](https://arxiv.org/abs/2403.12945) | RSS | 2024 | [Paper](https://arxiv.org/abs/2403.12945) \| [Project](https://droid-dataset.github.io/) | 76k demonstrations across 86 environments |
| [RH20T: A Comprehensive Robotic Dataset for Learning Diverse Skills](https://arxiv.org/abs/2307.00595) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2307.00595) \| [Project](https://rh20t.github.io/) | 110k+ multi-task demonstrations with rich annotations |
| [Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware (ALOHA)](https://arxiv.org/abs/2304.13705) | RSS | 2023 | [Paper](https://arxiv.org/abs/2304.13705) \| [Code](https://github.com/tonyzhaozh/aloha) | Bimanual ALOHA robot teleoperation dataset |
| [Something-Something v2: A Compositional Video-Text Dataset](https://arxiv.org/abs/1706.04261) | ICCV | 2017 | [Paper](https://arxiv.org/abs/1706.04261) | Large-scale human-object interaction video dataset |
| [EgoMimic: Scaling Imitation Learning via Egocentric Video](https://arxiv.org/abs/2410.24221) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2410.24221) | Egocentric human video for robot imitation learning |
| [AgiBot World Alpha](https://arxiv.org/abs/2503.06669) | — | 2025 | [Paper](https://arxiv.org/abs/2503.06669) \| [Project](https://agibot-world.com/) | 1M+ demonstrations from 100 robots, 217 tasks |

### Whole-body / Humanoid Benchmarks

| Benchmark | Year | Links | Description |
|-----------|------|-------|-------------|
| [HumanoidBench: Simulated Humanoid Benchmark for Whole-Body Locomotion and Manipulation](https://arxiv.org/abs/2403.10506) | — | 2024 | [Paper](https://arxiv.org/abs/2403.10506) \| [Code](https://github.com/carlosferrazza/humanoid-bench) | 27 tasks for full-body humanoid control |
| [ExBody: Expressive Whole-Body Control for Humanoid Robots](https://arxiv.org/abs/2402.16796) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2402.16796) \| [Code](https://github.com/WangZiyi9143/ExBody) | Whole-body expressive motion control for humanoids |
| [SMPL-X: Expressive Body Capture: 3D Hands, Face, and Body from a Single Image](https://arxiv.org/abs/1904.05866) | CVPR | 2019 | [Paper](https://arxiv.org/abs/1904.05866) \| [Code](https://github.com/vchoutas/smplx) | Expressive parametric human body model |
| [BEHAVIOR-1K: A Human-Centered Embodied AI Benchmark](https://arxiv.org/abs/2403.09227) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2403.09227) | 1000 daily activities for embodied AI evaluation |
| [BEHAVIOR Robot Suite: Real-World Whole-Body Manipulation for Household Activities](https://arxiv.org/abs/2503.05652) | RSS | 2025 | [Paper](https://arxiv.org/abs/2503.05652) \| [Project](https://behavior-robot-suite.github.io/) | Real-world household whole-body manipulation tasks |
| [OmniH2O: Universal and Dexterous Human-to-Humanoid Whole-Body Teleoperation](https://arxiv.org/abs/2406.08858) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2406.08858) \| [Code](https://github.com/LeCAR-Lab/human2humanoid) | Universal human-to-humanoid whole-body teleoperation |
| [LocoMuJoCo: A Comprehensive Imitation Learning Benchmark for Locomotion](https://loco-mujoco.readthedocs.io/) | — | 2025 | [Docs](https://loco-mujoco.readthedocs.io/) \| [Code](https://github.com/robfiras/loco-mujoco) | Comprehensive locomotion benchmark in MuJoCo |

| [HumanPlus: Humanoid Shadowing and Imitation from Humans](https://arxiv.org/abs/2406.10454) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2406.10454) \| [Code](https://github.com/MarkFzp/humanplus) | Whole-body humanoid policy from human shadowing |

### Autonomous Driving Benchmarks

| Benchmark | Year | Links | Description |
|-----------|------|-------|-------------|
| [nuScenes: A Multimodal Dataset for Autonomous Driving](https://arxiv.org/abs/1812.01051) | CVPR | 2020 | [Paper](https://arxiv.org/abs/1812.01051) \| [Project](https://www.nuscenes.org/) | 1000 scenes with 3D object detection and tracking |
| [CARLA: An Open Urban Driving Simulator](https://arxiv.org/abs/1711.03938) | CoRL | 2017 | [Paper](https://arxiv.org/abs/1711.03938) \| [Code](https://github.com/carla-simulator/carla) | Open-source urban driving simulation environment |
| [nuPlan: A Closed-Loop ML-Based Planning Benchmark for Autonomous Driving](https://arxiv.org/abs/2106.11810) | ECCV | 2021 | [Paper](https://arxiv.org/abs/2106.11810) \| [Project](https://www.nuplan.org/) | Closed-loop autonomous driving planning benchmark |
| [DriveLM: Driving with Graph Visual Question Answering](https://arxiv.org/abs/2312.14150) | ECCV | 2024 | [Paper](https://arxiv.org/abs/2312.14150) \| [Code](https://github.com/OpenDriveLab/DriveLM) | Language-driven driving understanding via scene graphs |
| [NAVSIM: Data-Driven Non-Reactive Autonomous Vehicle Simulation](https://arxiv.org/abs/2406.15349) | NeurIPS | 2024 | [Paper](https://arxiv.org/abs/2406.15349) \| [Code](https://github.com/autonomousvision/navsim) | Reactive simulation benchmark for autonomous driving |
| [Bench2Drive: Are We Ready for Autonomous Driving? The CARLA Benchmark](https://arxiv.org/abs/2406.03877) | NeurIPS | 2024 | [Paper](https://arxiv.org/abs/2406.03877) \| [Code](https://github.com/Thinklab-SJTU/Bench2Drive) | Comprehensive CARLA-based autonomous driving benchmark |
| [WOMD: Waymo Open Motion Dataset: An Interactive Motion Prediction Challenge](https://arxiv.org/abs/2104.10133) | ICRA | 2022 | [Paper](https://arxiv.org/abs/2104.10133) \| [Project](https://waymo.com/open/data/motion/) | Large-scale real-world motion prediction dataset |
| [Waymax: An Accelerated, Data-Driven Simulator for Large-Scale Autonomous Driving Research](https://arxiv.org/abs/2310.08710) | NeurIPS | 2023 | [Paper](https://arxiv.org/abs/2310.08710) \| [Code](https://github.com/waymo-research/waymax) | JAX-based accelerated autonomous driving simulator |

---

## 📚 Survey

### Manipulation & Robot Learning Survey

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [A Survey of Robot Learning from Demonstration](https://www.cs.cmu.edu/~mmv/papers/09ras-survey.pdf) | Robotics and Autonomous Systems | 2009 | [Paper](https://www.cs.cmu.edu/~mmv/papers/09ras-survey.pdf) | Foundational survey on imitation learning for robotics |
| [Diffusion Models for Robots: A Survey](https://arxiv.org/abs/2504.11002) | — | 2025 | [Paper](https://arxiv.org/abs/2504.11002) | Comprehensive survey of diffusion models in robotics |
| [Robot Learning from Human Demonstrations: A Survey](https://arxiv.org/abs/2311.07474) | — | 2023 | [Paper](https://arxiv.org/abs/2311.07474) | Survey on human demonstration-based robot learning |
| [A Survey on Vision-Language-Action Models for Embodied AI](https://arxiv.org/abs/2405.14093) | — | 2024 | [Paper](https://arxiv.org/abs/2405.14093) | Comprehensive survey on VLA model architectures |
| [From Text to Motion: A Survey on Foundation Models for Robot Manipulation](https://arxiv.org/abs/2501.04838) | — | 2025 | [Paper](https://arxiv.org/abs/2501.04838) | Survey of foundation models for robot manipulation |
| [A Survey on Embodied AI: From Simulators to Research Challenges](https://arxiv.org/abs/2103.04918) | IEEE TPAMI | 2022 | [Paper](https://arxiv.org/abs/2103.04918) | Foundational survey covering simulators and challenges |
| [Imitation Learning: A Survey of Learning Methods](https://dl.acm.org/doi/10.1145/3054912) | ACM Computing Surveys | 2018 | [Paper](https://dl.acm.org/doi/10.1145/3054912) | Comprehensive survey on imitation learning methods |

### Embodied AI General Survey

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [A Survey on Embodied AI: From Simulators to Research Challenges](https://arxiv.org/abs/2103.04918) | IEEE TPAMI | 2022 | [Paper](https://arxiv.org/abs/2103.04918) | Covers simulators, tasks, algorithms for embodied AI |
| [Foundation Models in Robotics: Applications, Challenges, and the Future](https://arxiv.org/abs/2312.07843) | — | 2023 | [Paper](https://arxiv.org/abs/2312.07843) | Foundation models applied to robotics: applications, challenges, future |
| [A Survey on Large Language Models for Robotics](https://arxiv.org/abs/2311.07226) | — | 2023 | [Paper](https://arxiv.org/abs/2311.07226) | LLMs as planners, coders, and reasoners for robots |
| [Towards Generalist Robots: A Survey on Foundation Models in Robotics](https://arxiv.org/abs/2312.08782) | — | 2024 | [Paper](https://arxiv.org/abs/2312.08782) | Broad survey on foundation model integration in robotics |
| [Embodied Intelligence via Learning and Evolution](https://arxiv.org/abs/2102.02202) | Nature Comm. | 2021 | [Paper](https://arxiv.org/abs/2102.02202) | Evolution and learning for embodied intelligence |
| [Semantic Mapping in Indoor Embodied AI: A Comprehensive Survey](https://arxiv.org/abs/2501.05750) | — | 2025 | [Paper](https://arxiv.org/abs/2501.05750) | Survey of indoor semantic mapping for embodied AI |

### Autonomous Driving Survey

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [End-to-End Autonomous Driving: Challenges and Frontiers](https://arxiv.org/abs/2306.16927) | IEEE TPAMI | 2023 | [Paper](https://arxiv.org/abs/2306.16927) | Comprehensive survey on end-to-end AD methods |
| [A Survey on Multimodal Large Language Models for Autonomous Driving](https://arxiv.org/abs/2311.12320) | WACV | 2024 | [Paper](https://arxiv.org/abs/2311.12320) | MLLMs for perception, planning, and control in AD |
| [DriveVLM: The Convergence of Autonomous Driving and Large Vision-Language Models](https://arxiv.org/abs/2402.12289) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2402.12289) | VLMs as reasoning modules for autonomous driving |
| [Generalized Autonomous Driving: A Survey on Vision-Centric Methods](https://arxiv.org/abs/2312.04512) | — | 2023 | [Paper](https://arxiv.org/abs/2312.04512) | Survey on camera-centric methods for autonomous driving |
| [World Models for Autonomous Driving: An Initial Survey](https://arxiv.org/abs/2403.02622) | — | 2024 | [Paper](https://arxiv.org/abs/2403.02622) | Survey on world models applied to autonomous driving |

---

## 🏢 Companies & Labs

| Organization | Type | Focus | Links |
|---|---|---|---|
| [Physical Intelligence (π)](https://www.physicalintelligence.company/) | Startup | General-purpose robot learning (π0, π0-FAST) | [Website](https://www.physicalintelligence.company/) \| [Blog](https://www.physicalintelligence.company/blog) |
| [1X Technologies](https://www.1x.tech/) | Startup | Humanoid robot learning at scale (NEO, EVE) | [Website](https://www.1x.tech/) \| [Blog](https://www.1x.tech/discover) |
| [Figure AI](https://www.figure.ai/) | Startup | Humanoid robot for industrial use (Figure 02, Helix) | [Website](https://www.figure.ai/) \| [Blog](https://www.figure.ai/news) |
| [Agility Robotics](https://agilityrobotics.com/) | Startup | Bipedal humanoid for logistics (Digit) | [Website](https://agilityrobotics.com/) |
| [Unitree Robotics (宇树科技)](https://www.unitree.com/) | Company | Quadruped & humanoid (Go2, H1, G1) | [Website](https://www.unitree.com/) |
| [Boston Dynamics](https://bostondynamics.com/) | Company | Advanced dynamic robots (Spot, Atlas, Stretch) | [Website](https://bostondynamics.com/) |
| [Tesla Optimus](https://www.tesla.com/optimus) | Company | Humanoid robot for manufacturing | [Website](https://www.tesla.com/optimus) |
| [Google DeepMind Robotics](https://deepmind.google/research/robotics/) | Research Lab | Foundation models for robotics (RT-2, RT-X, Gemini Robotics) | [Website](https://deepmind.google/research/robotics/) |
| [NVIDIA Isaac / GR00T](https://developer.nvidia.com/isaac) | Company | Robot simulation & foundation models (GR00T N1) | [Website](https://developer.nvidia.com/isaac) \| [GitHub](https://github.com/NVIDIA/Isaac-GR00T) |
| [AgileX / Agilex Robotics](https://agilex.ai/) | Company | Open-platform mobile manipulation robots | [Website](https://agilex.ai/) |
| [Fourier Intelligence (傅利叶智能)](https://www.fourierintelligence.com/) | Startup | Humanoid robots for rehabilitation and service | [Website](https://www.fourierintelligence.com/) |
| [DEEP Robotics (深势科技)](https://www.deeprobotics.cn/) | Company | Quadruped robots for field deployment | [Website](https://www.deeprobotics.cn/) |
| [Zhiyuan Robot (智元机器人)](https://www.zhiyuan-robot.com/) | Startup | General-purpose humanoid (ARRT remote) | [Website](https://www.zhiyuan-robot.com/) |
| [AgiBot (星动纪元)](https://agibot.com/) | Startup | Humanoid robots for industrial scenarios | [Website](https://agibot.com/) |
| [Galbot (加速进化)](https://www.galbot.com/) | Startup | Wheeled humanoid robots with advanced manipulation | [Website](https://www.galbot.com/) |
| [Apptronik](https://apptronik.com/) | Startup | Humanoid robots for supply chain (Apollo) | [Website](https://apptronik.com/) |
| [Sanctuary AI](https://sanctuary.ai/) | Startup | Human-like general-purpose robots (Phoenix) | [Website](https://sanctuary.ai/) |
| [Hugging Face LeRobot](https://huggingface.co/lerobot) | Open Source | Open-source robot learning library & datasets | [HuggingFace](https://huggingface.co/lerobot) \| [GitHub](https://github.com/huggingface/lerobot) |
| [Stanford IRIS Lab](https://irislab.stanford.edu/) | Academic Lab | Robot learning, VLA, manipulation (OpenVLA team) | [Website](https://irislab.stanford.edu/) |
| [CMU Robotics Institute](https://www.ri.cmu.edu/) | Academic | Foundational robotics research across all domains | [Website](https://www.ri.cmu.edu/) |
| [MIT CSAIL Robotics](https://www.csail.mit.edu/research/robotics) | Academic | Robot learning, perception, interaction | [Website](https://www.csail.mit.edu/research/robotics) |
| [UC Berkeley RAIL / RoboLearn](https://rail.eecs.berkeley.edu/) | Academic | RL, imitation learning, robot learning (ACT, Diffusion Policy) | [Website](https://rail.eecs.berkeley.edu/) |
| [Columbia Robot Learning Lab](https://robotlearning.cs.columbia.edu/) | Academic | Manipulation, video-based policies, UMI | [Website](https://robotlearning.cs.columbia.edu/) |
| [University of Washington Robot Learning Lab](https://robotlearning.cs.washington.edu/) | Academic | Physical AI, robot manipulation, generalization | [Website](https://robotlearning.cs.washington.edu/) |
| [PKU EPIC Lab](https://pku-epic.github.io/) | Academic | Dexterous manipulation, embodied AI, GraspNet | [Website](https://pku-epic.github.io/) |
| [OpenRobotics / Open Source Robotics Foundation](https://www.openrobotics.org/) | Non-profit | ROS, Gazebo, open-source robot infrastructure | [Website](https://www.openrobotics.org/) |
| [AgiBot World](https://agibot-world.com/) | Startup | Large-scale robot teleoperation data platform | [Website](https://agibot-world.com/) |

---

## 🔗 Related Resources

### Similar Awesome Lists

- [jonyzhang2023/awesome-embodied-vla-va-vln](https://github.com/jonyzhang2023/awesome-embodied-vla-va-vln) — Regularly updated VLA/VA/VLN paper list
- [haosulab/awesome-vision-language-action-model](https://github.com/haosulab/awesome-vision-language-action-model) — VLA model collection
- [GT-RIPL/Awesome-LLM-Robotics](https://github.com/GT-RIPL/Awesome-LLM-Robotics) — LLM for robotics resources
- [robotics-survey/Awesome-Robotics-Foundation-Models](https://github.com/robotics-survey/Awesome-Robotics-Foundation-Models) — Foundation models for robotics
- [knightnemo/Awesome-World-Models](https://github.com/knightnemo/Awesome-World-Models) — World models collection
- [leofan90/Awesome-World-Models](https://github.com/leofan90/Awesome-World-Models) — World models for robotics
- [cheryyunl/awesome-generalist-agents](https://github.com/cheryyunl/awesome-generalist-agents) — Generalist agent papers
- [AoqunJin/Awesome-VLA-Post-Training](https://github.com/AoqunJin/Awesome-VLA-Post-Training) — VLA post-training methods
- [XiaoWei-i/Awesome-VLA-RL](https://github.com/XiaoWei-i/Awesome-VLA-RL) — VLA with RL
- [Jiaaqiliu/Awesome-VLA-Robotics](https://github.com/Jiaaqiliu/Awesome-VLA-Robotics) — VLA for robotics
- [OpenDCAI/OpenWorldLib](https://github.com/OpenDCAI/OpenWorldLib) — Open world model library

### Simulators

| Simulator | Year | Links | Description |
|-----------|------|-------|-------------|
| [MuJoCo: A Physics Engine for Model-Based Control](https://mujoco.readthedocs.io/) | 2012 | [Docs](https://mujoco.readthedocs.io/) \| [Code](https://github.com/google-deepmind/mujoco) | State-of-the-art physics simulation for robotics |
| [Genesis: A Generative and Universal Physics Engine](https://genesis-embodied-ai.github.io/) | 2024 | [Project](https://genesis-embodied-ai.github.io/) | Generative physics engine with GPU acceleration |
| [ManiSkill3: GPU Parallelized Robotics Simulation](https://arxiv.org/abs/2410.00425) | 2024 | [Paper](https://arxiv.org/abs/2410.00425) \| [Code](https://github.com/haosulab/ManiSkill) | GPU-parallel manipulation simulation (v1-v3) |
| [NVIDIA Isaac Lab](https://github.com/isaac-sim/IsaacLab) | 2024 | [Docs](https://isaac-sim.github.io/IsaacLab/) \| [Code](https://github.com/isaac-sim/IsaacLab) | Isaac Sim-based GPU robot learning framework |
| [PyBullet](https://pybullet.org/) | 2016 | [Docs](https://pybullet.org/) \| [Code](https://github.com/bulletphysics/bullet3) | Python bindings for Bullet physics engine |
| [Gazebo / Ignition](https://gazebosim.org/) | 2002 | [Website](https://gazebosim.org/) | Open-source 3D robot simulation for ROS |
| [MuJoCo MJX (Jax-accelerated)](https://mujoco.readthedocs.io/en/stable/mjx.html) | 2024 | [Docs](https://mujoco.readthedocs.io/en/stable/mjx.html) | JAX-native MuJoCo for GPU-accelerated simulation |
| [MuJoCo Playground](https://arxiv.org/abs/2502.08844) | 2025 | [Paper](https://arxiv.org/abs/2502.08844) | Interactive playground for robot learning in MuJoCo |
| [CARLA Simulator](https://github.com/carla-simulator/carla) | 2017 | [Docs](https://carla.readthedocs.io/) \| [Code](https://github.com/carla-simulator/carla) | Open-source urban driving simulation |

### Tools & Libraries

| Tool | Links | Description |
|------|-------|-------------|
| [LeRobot](https://github.com/huggingface/lerobot) | [GitHub](https://github.com/huggingface/lerobot) \| [HuggingFace](https://huggingface.co/lerobot) | HuggingFace open-source robot learning library |
| [Lerobot Datasets](https://huggingface.co/datasets?search=lerobot) | [HuggingFace](https://huggingface.co/datasets?search=lerobot) | Community robot datasets on HuggingFace |

---

## Contributing

We welcome contributions! Please:

1. Fork this repository
2. Add your paper/resource to the appropriate section
3. Follow the existing table format
4. Submit a Pull Request with a brief description

For papers, please include:
- Title with arxiv/project link
- Venue and year
- A ≤15-word TL;DR

For companies/labs, include official website and brief description.

---

⭐ If you find this list helpful, please consider starring the repository!

[![Star History Chart](https://api.star-history.com/svg?repos=Noietch/Awesome-Embodied-AI&type=Date)](https://star-history.com/#Noietch/Awesome-Embodied-AI&Date)
