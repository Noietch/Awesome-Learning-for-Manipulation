# Awesome Learning for Manipulation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![Stars](https://img.shields.io/github/stars/Noietch/Awesome-Learning-for-Manipulation)

> A curated list of papers on learning-based robot manipulation, covering VLA, video-action models, visuomotor policies, world models, simulators, benchmarks, and industry tech reports.
> Maintained by [@Noietch](https://github.com/Noietch). PRs welcome!

## Table of Contents

- [🤖 VLA — Vision-Language-Action Models](#-vla--vision-language-action-models)
- [🎬 VA — Video-Action Models](#-va--video-action-models)
- [🦾 Visuomotor Policies](#-visuomotor-policies)
- [🏭 Robot Foundation Model Tech Reports](#-robot-foundation-model-tech-reports)
- [🌍 World Models](#-world-models)
- [📊 Benchmarks & Datasets](#-benchmarks--datasets)
  - [Manipulation Benchmarks](#manipulation-benchmarks)
  - [Robot Datasets](#robot-datasets)
  - [Whole-body / Humanoid Benchmarks](#whole-body--humanoid-benchmarks)
- [🔧 Simulators & Data Engines](#-simulators--data-engines)
- [📚 Survey](#-survey)
  - [Manipulation & Robot Learning](#manipulation--robot-learning-survey)
  - [Embodied AI General](#embodied-ai-general-survey)
- [🏢 Companies & Labs](#-companies--labs)
- [Contributing](#contributing)

---

## 🤖 VLA — Vision-Language-Action Models

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [OpenVLA: An Open-Source Vision-Language-Action Model](https://arxiv.org/abs/2406.09246) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2406.09246) \| [Project](https://openvla.github.io/) | 7B VLA fine-tuned from Prismatic VLM; fully open-source |
| [Octo: An Open-Source Generalist Robot Policy](https://arxiv.org/abs/2405.12213) | RSS | 2024 | [Paper](https://arxiv.org/abs/2405.12213) \| [Project](https://octo-models.github.io/) | Transformer policy trained on Open X-Embodiment data |
| [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) | ICRA Best Paper | 2024 | [Paper](https://arxiv.org/abs/2310.08864) \| [Project](https://robotics-transformer-x.github.io/) | Cross-embodiment dataset + RT-X models at scale |
| [RT-2: Vision-Language-Action Models Transfer Web Knowledge to Robotic Control](https://arxiv.org/abs/2307.15818) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2307.15818) | VLM co-fine-tuned as action predictor; web knowledge → robotics |
| [PaLM-E: An Embodied Multimodal Language Model](https://arxiv.org/abs/2303.03378) | ICML | 2023 | [Paper](https://arxiv.org/abs/2303.03378) | 562B multimodal model for embodied reasoning and planning |
| [UniPi: Learning Universal Policies via Text-Guided Video Generation](https://arxiv.org/abs/2302.00111) | NeurIPS | 2023 | [Paper](https://arxiv.org/abs/2302.00111) | Plan via video generation; actions extracted from video |
| [RT-1: Robotics Transformer for Real-World Control at Scale](https://arxiv.org/abs/2212.06817) | CoRL | 2022 | [Paper](https://arxiv.org/abs/2212.06817) | Transformer trained on 130k real-robot demos for multi-task control |

### 2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Towards Generalist Robot Policies: What Matters in Building Vision-Language-Action Models](https://arxiv.org/abs/2412.14058) | Nature MI | 2024 | [Paper](https://arxiv.org/abs/2412.14058) | Systematic study of design choices for generalist VLA |
| [TraceVLA: Visual Trace Prompting Enhances Spatial-Temporal Awareness](https://arxiv.org/abs/2412.10345) | ICLR 2025 | 2024 | [Paper](https://arxiv.org/abs/2412.10345) | Visual traces as prompts for better spatial reasoning |
| [Moto: Latent Motion Token as the Bridging Language for Robot Manipulation](https://arxiv.org/abs/2412.04445) | ICCV 2025 | 2024 | [Paper](https://arxiv.org/abs/2412.04445) | Discrete latent motion tokens bridge VLM and action |
| [Diffusion-VLA: Scaling Robot Foundation Models via Unified Diffusion and Autoregression](https://arxiv.org/abs/2412.03293) | ICML 2025 | 2024 | [Paper](https://arxiv.org/abs/2412.03293) | Unifies diffusion and autoregressive VLA in one model |
| [Latent Action Pretraining from Videos](https://arxiv.org/abs/2410.11758) | ICLR 2025 | 2024 | [Paper](https://arxiv.org/abs/2410.11758) | Learns latent actions from internet videos for zero-shot transfer |
| [GR-2: Generative Video-Language-Action Model with Web-Scale Knowledge](https://arxiv.org/abs/2410.06158) | Tech Report | 2024 | [Paper](https://arxiv.org/abs/2410.06158) | Video generation as world model for robot manipulation |
| [HiRT: Enhancing Robotic Control with Hierarchical Robot Transformers](https://arxiv.org/abs/2410.05273) | CoRL 2024 | 2024 | [Paper](https://arxiv.org/abs/2410.05273) | Two-level hierarchy: high-level VLM + low-level policy |
| [HPT: Scaling Proprioceptive-Visual Learning with Heterogeneous Pre-Training](https://arxiv.org/abs/2409.20537) | NeurIPS | 2024 | [Paper](https://arxiv.org/abs/2409.20537) | Unified pre-training for diverse robot embodiments |
| [TinyVLA: Towards Fast, Data-Efficient Vision-Language-Action Models](https://arxiv.org/abs/2409.12514) | RA-L | 2024 | [Paper](https://arxiv.org/abs/2409.12514) | Efficient VLA without large-scale robot pre-training |
| [Robotic Control via Embodied Chain-of-Thought Reasoning](https://arxiv.org/abs/2407.08693) | CoRL 2024 | 2024 | [Paper](https://arxiv.org/abs/2407.08693) | ECoT: step-by-step reasoning improves robot manipulation |
| [LLaRA: Supercharging Robot Learning Data for Vision-Language Policy](https://arxiv.org/abs/2406.20095) | ICLR 2025 | 2024 | [Paper](https://arxiv.org/abs/2406.20095) | Data augmentation for VLA with interleaved language |
| [Manipulate-Anything](https://arxiv.org/abs/2406.18915) | CoRL, Nov | 2024 | [Paper](https://arxiv.org/abs/2406.18915) | Generalizable manipulation of arbitrary objects via VLM-guided affordance |
| [3D-VLA: A 3D Vision-Language-Action Generative World Model](https://arxiv.org/abs/2403.09631) | ICML | 2024 | [Paper](https://arxiv.org/abs/2403.09631) | Grounded 3D perception with VLA and world model |
| [RT-H: Action Hierarchies Using Language](https://arxiv.org/abs/2403.01823) | RSS 2025 | 2024 | [Paper](https://arxiv.org/abs/2403.01823) | Hierarchical language-conditioned RT for long-horizon tasks |
| [General Flow as Foundation Affordance for Scalable Robot Learning](https://arxiv.org/abs/2401.11439) | CoRL 2024 | 2024 | [Paper](https://arxiv.org/abs/2401.11439) \| [Project](https://general-flow.github.io/) | Optical flow as general robot affordance representation |
| [QUAR-VLA: Vision-Language-Action Model for Quadruped Robots](https://arxiv.org/abs/2312.14457) | ECCV 2024 | 2024 | [Paper](https://arxiv.org/abs/2312.14457) | VLA adapted for quadruped locomotion and navigation |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [OpenVLA-OFT: Fine-Tuning Vision-Language-Action Models: Optimizing Speed and Success](https://arxiv.org/abs/2502.19645) | RSS | 2025 | [Paper](https://arxiv.org/abs/2502.19645) \| [Project](https://openvla-oft.github.io/) | Parallel decoding + fine-tuning for fast OpenVLA |
| [RDT-1B: a Diffusion Foundation Model for Bimanual Manipulation](https://arxiv.org/abs/2410.07864) | ICLR | 2025 | [Paper](https://arxiv.org/abs/2410.07864) \| [Project](https://rdt-robotics.github.io/rdt-robotics/) | 1B diffusion transformer for bimanual robot arms |
| [InternVLA-M1: Spatially Guided VLA Framework for Generalist Robot Policy](https://arxiv.org/abs/2510.13778) | — | 2025 | [Paper](https://arxiv.org/abs/2510.13778) \| [Code](https://github.com/InternRobotics/InternVLA-M1) | InternRobotics' spatially grounded VLA framework |
| [X-VLA: Soft-Prompted Transformer as Scalable Cross-Embodiment VLA](https://arxiv.org/abs/2510.10274) | — | 2025 | [Paper](https://arxiv.org/abs/2510.10274) \| [Code](https://github.com/2toinf/X-VLA) | Cross-embodiment VLA via soft prompt adaptation |
| [Long-VLA: Unleashing Long-Horizon Capability for Robot Manipulation](https://arxiv.org/abs/2508.19958) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2508.19958) \| [Project](https://long-vla.github.io/) | VLA for long-horizon multi-step manipulation tasks |
| [Embodied-R1: Reinforced Embodied Reasoning for General Robotic Manipulation](https://arxiv.org/abs/2508.13998) | — | 2025 | [Paper](https://arxiv.org/abs/2508.13998) \| [Code](https://github.com/pickxiguapi/Embodied-R1) | R1-style reasoning reinforcement for embodied manipulation |
| [WorldVLA: Towards Autoregressive Action World Model](https://arxiv.org/abs/2506.21539) | — | 2025 | [Paper](https://arxiv.org/abs/2506.21539) \| [Code](https://github.com/alibaba-damo-academy/WorldVLA) | Unifies world model prediction with VLA action generation |
| [UniVLA: Unified Vision-Language-Action Model](https://arxiv.org/abs/2506.19850) | — | 2025 | [Paper](https://arxiv.org/abs/2506.19850) \| [Code](https://github.com/baaivision/UniVLA) | Single model unifying diverse manipulation tasks |
| [RoboMonkey: Scaling Test-Time Sampling and Verification for VLAs](https://arxiv.org/abs/2506.17811) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2506.17811) \| [Code](https://github.com/robomonkey-vla/RoboMonkey) | Test-time compute scaling via sampling+verification |
| [BridgeVLA: Input-Output Alignment for Efficient 3D Manipulation](https://arxiv.org/abs/2506.07961) | NeurIPS | 2025 | [Paper](https://arxiv.org/abs/2506.07961) \| [Project](https://bridgevla.github.io/) | Aligns 3D inputs/outputs for efficient VLA learning |
| [SmolVLA: A vision-language-action model for affordable and efficient robotics](https://arxiv.org/abs/2506.01844) | — | 2025 | [Paper](https://arxiv.org/abs/2506.01844) \| [Code](https://github.com/huggingface/lerobot) | HuggingFace compact VLA; integrates with LeRobot |
| [VLA-RL: Towards Masterful and General Robotic Manipulation with Scalable RL](https://arxiv.org/abs/2505.18719) | — | 2025 | [Paper](https://arxiv.org/abs/2505.18719) \| [Code](https://github.com/GuanxingLu/vlarl) | RL fine-tuning of VLA for general manipulation |
| [GraspVLA: a Grasping Foundation Model Pre-trained on Billion-scale Synthetic Data](https://arxiv.org/abs/2505.03233) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2505.03233) \| [Code](https://github.com/PKU-EPIC/GraspVLA) | Billion-scale synthetic pre-training for universal grasping |
| [NORA: A Small Open-Sourced Generalist VLA Model for Embodied Tasks](https://arxiv.org/abs/2504.19854) | — | 2025 | [Paper](https://arxiv.org/abs/2504.19854) \| [Project](https://declare-lab.github.io/nora) | Lightweight open-source VLA for diverse robot tasks |
| [CoT-VLA: Visual Chain-of-Thought Reasoning for Vision-Language-Action Models](https://arxiv.org/abs/2503.22020) | CVPR | 2025 | [Paper](https://arxiv.org/abs/2503.22020) \| [Project](https://cot-vla.github.io/) | Explicit visual reasoning chain improves VLA performance |
| [HybridVLA: Collaborative Diffusion and Autoregression in a Unified VLA Model](https://arxiv.org/abs/2503.10631) | — | 2025 | [Paper](https://arxiv.org/abs/2503.10631) \| [Project](https://hybrid-vla.github.io/) | Jointly leverages diffusion and AR for robust policies |
| [RoboBrain: A Unified Brain Model for Robotic Manipulation from Abstract to Concrete](https://arxiv.org/abs/2502.21257) | CVPR | 2025 | [Paper](https://arxiv.org/abs/2502.21257) \| [Project](https://superrobobrain.github.io/) | Unified cognition-to-action model for manipulation |
| [Hi Robot: Open-Ended Instruction Following with Hierarchical VLAs](https://arxiv.org/abs/2502.19417) | ICML 2025 | 2025 | [Paper](https://arxiv.org/abs/2502.19417) \| [Project](https://www.pi.website/research/hirobot) | Two-level VLA: semantic planner + low-level controller |
| [DexVLA: Vision-Language Model with Plug-In Diffusion Expert for Robot Control](https://arxiv.org/abs/2502.05855) | CoRL 2025 | 2025 | [Paper](https://arxiv.org/abs/2502.05855) | Modular VLA with plug-in diffusion action expert |
| [ConRFT: A Reinforced Fine-tuning Method for VLA Models via Consistency Policy](https://arxiv.org/abs/2502.05450) | RSS | 2025 | [Paper](https://arxiv.org/abs/2502.05450) \| [Project](https://cccedric.github.io/conrft/) | Consistency-based RL fine-tuning improves VLA robustness |
| [SpatialVLA: Exploring Spatial Representations for Visual-Language-Action Model](https://arxiv.org/abs/2501.15830) | MDPI Robotics | 2025 | [Paper](https://arxiv.org/abs/2501.15830) | 3D-aware spatial tokens for better manipulation |
| [π0-FAST: Efficient Action Tokenization for Vision-Language-Action Models](https://arxiv.org/abs/2501.09747) | — | 2025 | [Paper](https://arxiv.org/abs/2501.09747) | Frequency-based action tokenization for fast π0 inference |

### RL Fine-tuning

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [RLinf-VLA: A Unified and Efficient Framework for VLA+RL Training](https://arxiv.org/abs/2510.06710) | — | 2025 | [Paper](https://arxiv.org/abs/2510.06710) | Unified infrastructure for efficient VLA reinforcement learning training |
| [VLA-RFT: Vision-Language-Action Reinforcement Fine-tuning with Verified Rewards in World Simulators](https://arxiv.org/abs/2510.00406) | — | 2025 | [Paper](https://arxiv.org/abs/2510.00406) | RL fine-tuning of VLAs using verified rewards from world simulators |
| [World-Env: Leveraging World Model as a Virtual Environment for VLA Post-Training](https://arxiv.org/abs/2509.24948) | — | 2025 | [Paper](https://arxiv.org/abs/2509.24948) | World model as virtual env for scalable VLA post-training |
| [RLinf: Reinforcement Learning Infrastructure for Agentic AI](https://arxiv.org/abs/2509.15965) | — | 2025 | [Paper](https://arxiv.org/abs/2509.15965) | Scalable RL infrastructure designed for agentic AI systems |
| [Self-Improving Embodied Foundation Models](https://arxiv.org/abs/2509.15155) | NeurIPS | 2025 | [Paper](https://arxiv.org/abs/2509.15155) | Embodied models improve themselves via self-generated experience |
| [SimpleVLA-RL: Scaling VLA Training via Reinforcement Learning](https://arxiv.org/abs/2509.09674) | — | 2025 | [Paper](https://arxiv.org/abs/2509.09674) | Simple and scalable RL recipe for VLA training |
| [Balancing Signal and Variance: Adaptive Offline RL Post-Training for VLA Flow Models](https://arxiv.org/abs/2509.04063) | — | 2025 | [Paper](https://arxiv.org/abs/2509.04063) | Adaptive offline RL balances reward signal and variance in flow VLAs |
| [CO-RFT: Efficient Fine-Tuning of Vision-Language-Action Models through Chunked Offline Reinforcement Learning](https://arxiv.org/abs/2508.02219) | — | 2025 | [Paper](https://arxiv.org/abs/2508.02219) | Chunked offline RL for efficient VLA fine-tuning |
| [What Can RL Bring to VLA Generalization? An Empirical Study](https://arxiv.org/abs/2505.19789) | NeurIPS | 2025 | [Paper](https://arxiv.org/abs/2505.19789) | Empirical analysis of RL's role in improving VLA generalization |
| [ReinboT: Amplifying Robot Visual-Language Manipulation with Reinforcement Learning](https://arxiv.org/abs/2505.07395) | ICML | 2025 | [Paper](https://arxiv.org/abs/2505.07395) | RL amplifies VL manipulation performance via reward-guided exploration |
| [MoRE: Unlocking Scalability in Reinforcement Learning for Quadruped Vision-Language-Action Models](https://arxiv.org/abs/2503.08007) | ICRA | 2025 | [Paper](https://arxiv.org/abs/2503.08007) | Scalable RL framework for quadruped VLA locomotion and manipulation |
| [SafeVLA: Towards Safety Alignment of Vision-Language-Action Model via Constrained Learning](https://arxiv.org/abs/2503.03480) | NeurIPS | 2025 | [Paper](https://arxiv.org/abs/2503.03480) | Constrained RL aligns VLA models with safety objectives |
| [Improving Vision-Language-Action Model with Online Reinforcement Learning](https://arxiv.org/abs/2501.16664) | RA-L | 2025 | [Paper](https://arxiv.org/abs/2501.16664) | Online RL fine-tuning boosts VLA performance on real robot tasks |
| [RLDG: Robotic Generalist Policy Distillation via Reinforcement Learning](https://arxiv.org/abs/2412.09858) | RSS | 2024 | [Paper](https://arxiv.org/abs/2412.09858) | RL distills task-specific experts into a generalist robot policy |
| [Steering Your Generalists: Improving Robotic Foundation Models via Value Guidance](https://arxiv.org/abs/2410.13816) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2410.13816) | Value function guidance steers generalist robot policies at test time |
| [FLaRe: Achieving Masterful and Adaptive Robot Policies with Large-Scale Reinforcement Learning Fine-Tuning](https://arxiv.org/abs/2409.16578) | ICRA 2025 Best Paper Finalist | 2024 | [Paper](https://arxiv.org/abs/2409.16578) | Large-scale RL fine-tuning achieves masterful dexterous robot control |
| [GeRM: A Generalist Robotic Model with Mixture-of-experts for Quadruped Robot](https://arxiv.org/abs/2403.13358) | IROS | 2024 | [Paper](https://arxiv.org/abs/2403.13358) | MoE-based generalist model for diverse quadruped locomotion tasks |
| [Offline Actor-Critic Reinforcement Learning Scales to Large Models](https://arxiv.org/abs/2402.05546) | ICML | 2024 | [Paper](https://arxiv.org/abs/2402.05546) | Offline actor-critic RL scales effectively to billion-parameter models |

### 2026 (Preprints)

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [DIAL: Decoupling Intent and Action via Latent World Modeling for End-to-End VLA](https://arxiv.org/abs/2603.29844) | — | 2026 | [Paper](https://arxiv.org/abs/2603.29844) | Bridges high-level intent and low-level actions via latent world model bottleneck |
| [FocusVLA: Focused Visual Utilization for Vision-Language-Action Models](https://arxiv.org/abs/2603.28740) | — | 2026 | [Paper](https://arxiv.org/abs/2603.28740) | Directs model attention to task-relevant visual patches to improve action quality |
| [ProgressVLA: Progress-Guided Diffusion Policy for Vision-Language Robotic Manipulation](https://arxiv.org/abs/2603.27670) | — | 2026 | [Paper](https://arxiv.org/abs/2603.27670) | Integrates task progress estimation as differentiable guidance for VLA policies |
| [VLA-OPD: Bridging Offline SFT and Online RL for VLA Models via On-Policy Distillation](https://arxiv.org/abs/2603.26666) | — | 2026 | [Paper](https://arxiv.org/abs/2603.26666) | On-policy distillation with reverse-KL combines SFT efficiency and RL robustness |
| [MMaDA-VLA: Large Diffusion VLA with Unified Multi-Modal Instruction and Generation](https://arxiv.org/abs/2603.25406) | — | 2026 | [Paper](https://arxiv.org/abs/2603.25406) | Native discrete diffusion unifies language, images, and robot actions in one backbone |
| [StarVLA: A Lego-like Codebase for Vision-Language-Action Model Developing](https://arxiv.org/abs/2604.05014) | — | 2026 | [Paper](https://arxiv.org/abs/2604.05014) \| [Project](https://starvla.github.io/) | Modular open-source codebase unifying VLA training across architectures |
| [StarVLA-α: Reducing Complexity in Vision-Language-Action Systems](https://arxiv.org/abs/2604.11757) | — | 2026 | [Paper](https://arxiv.org/abs/2604.11757) | Systematic simplification of VLA training pipeline without sacrificing performance |
| [Robotic Manipulation is Vision-to-Geometry Mapping (f(v)→G)](https://arxiv.org/abs/2604.12908) | — | 2026 | [Paper](https://arxiv.org/abs/2604.12908) | Argues geometry-aware backbones outperform language/video pretrained VLA backbones |
| [RDT2: Scaling Limit of UMI Data Towards Zero-Shot Cross-Embodiment](https://arxiv.org/abs/2602.03310) | — | 2026 | [Paper](https://arxiv.org/abs/2602.03310) \| [Code](https://github.com/thu-ml/RDT2) | Next-gen RDT scaling for cross-embodiment generalization |
| [PokeVLA: Empowering Pocket-Sized Vision-Language-Action Model with Comprehensive World Knowledge Guidance](https://arxiv.org/abs/2604.20834) | — | 2026 | [Paper](https://arxiv.org/abs/2604.20834) | Lightweight VLA infused with world knowledge for efficient embodied manipulation |
| [RL Token: Bootstrapping Online RL with Vision-Language-Action Models](https://arxiv.org/abs/2604.23073) | — | 2026 | [Paper](https://arxiv.org/abs/2604.23073) | RL token enables sample-efficient online RL fine-tuning of VLAs in hours |
| [CF-VLA: Efficient Coarse-to-Fine Action Generation for VLA Policies](https://arxiv.org/abs/2604.24622) | — | 2026 | [Paper](https://arxiv.org/abs/2604.24622) \| [Code](https://github.com/) | Coarse-to-fine flow-based VLA reduces latency 75% while matching multi-step quality |
| [GazeVLA: Learning Human Intention for Robotic Manipulation](https://arxiv.org/abs/2604.22615) | — | 2026 | [Paper](https://arxiv.org/abs/2604.22615) | Gaze-based intention bridging enables human-to-robot VLA manipulation transfer |
| [VLA Foundry: A Unified Framework for Training Vision-Language-Action Models](https://arxiv.org/abs/2604.19728) | — | 2026 | [Paper](https://arxiv.org/abs/2604.19728) | Open-source unified LLM/VLM/VLA training stack from pretraining to action fine-tuning |
| [Long-Horizon Manipulation via Trace-Conditioned VLA Planning](https://arxiv.org/abs/2604.21924) | — | 2026 | [Paper](https://arxiv.org/abs/2604.21924) \| [Project Page](https://trace-conditioned-vla.github.io/) | Trace-conditioned planning enables long-horizon manipulation with VLA-level reasoning |
| [ResVLA: From Noise to Intent — Anchoring Generative VLA Policies with Residual Bridges](https://arxiv.org/abs/2604.21391) | — | 2026 | [Paper](https://arxiv.org/abs/2604.21391) | Refinement-from-Intent paradigm anchors generative VLA on low-frequency motion intent |
| [Temporal Difference Calibration in Sequential Tasks for VLA Models](https://arxiv.org/abs/2604.20472) | — | 2026 | [Paper](https://arxiv.org/abs/2604.20472) | Conformal TD calibration improves uncertainty quantification in sequential VLA tasks |
| [The Compression Gap: Why Discrete Tokenization Limits VLA Scaling](https://arxiv.org/abs/2604.03191) | — | 2026 | [Paper](https://arxiv.org/abs/2604.03191) | Shows discrete action tokenization creates information bottleneck limiting vision encoder scaling |
| [Adaptive Action Chunking at Inference-Time for VLA Models](https://arxiv.org/abs/2604.04161) | — | 2026 | [Paper](https://arxiv.org/abs/2604.04161) | Dynamically adjusts action chunk size at inference balancing responsiveness and stability |
| [ProGAL-VLA: Grounded Alignment via Prospective Reasoning in VLAs](https://arxiv.org/abs/2604.09824) | — | 2026 | [Paper](https://arxiv.org/abs/2604.09824) | 3D entity-centric graph with prospective reasoning fixes language ignorance in VLAs |
| [VLA-Forget: Unlearning for Embodied Foundation Models](https://arxiv.org/abs/2604.03956) | — | 2026 | [Paper](https://arxiv.org/abs/2604.03956) | Removes unsafe or spurious behaviors from deployed VLA models via unlearning |
| [Libra-VLA: Achieving Learning Equilibrium via Asynchronous Coarse-to-Fine Dual-System](https://arxiv.org/abs/2604.24921) | ACL 2026 | 2026 | [Paper](https://arxiv.org/abs/2604.24921) \| [Project](https://libra-vla.github.io/) | Coarse-to-fine dual-system VLA with asynchronous execution for open-world manipulation |
| [M²-VLA: Boosting VLMs for Generalizable Manipulation via Layer Mixture and Meta-Skills](https://arxiv.org/abs/2604.24182) | — | 2026 | [Paper](https://arxiv.org/abs/2604.24182) | Preserves VLM generalization via MoL feature extraction and meta-skill trajectory learning |
| [CodeGraphVLP: Code-as-Planner Meets Semantic-Graph State for Non-Markovian VLA](https://arxiv.org/abs/2604.22238) | — | 2026 | [Paper](https://arxiv.org/abs/2604.22238) | Semantic-graph state + code planner enables reliable non-Markovian long-horizon manipulation |
| [EmbodiedMidtrain: Bridging VLM and VLA via Mid-training](https://arxiv.org/abs/2604.20012) | — | 2026 | [Paper](https://arxiv.org/abs/2604.20012) | Data engine curates VLM mid-training to bridge distribution gap before VLA fine-tuning |
| [LaST-R1: Reinforcing Action via Adaptive Physical Latent Reasoning for VLA Models](https://arxiv.org/abs/2604.28192) | — | 2026 | [Paper](https://arxiv.org/abs/2604.28192) | R1-style latent reasoning + online RL enables adaptive VLA action refinement |
| [PRTS: A Primitive Reasoning and Tasking System via Contrastive Representations](https://arxiv.org/abs/2604.27472) | — | 2026 | [Paper](https://arxiv.org/abs/2604.27472) | Contrastive primitive representations enable goal-reaching reasoning for robot tasking |
| [AnchorRefine: Synergy-Manipulation Based on Trajectory Anchor and Residual Refinement for VLA](https://arxiv.org/abs/2604.17787) | — | 2026 | [Paper](https://arxiv.org/abs/2604.17787) | Trajectory anchor + residual refinement decouples macro transport from micro correction |
| [How VLAs (Really) Work In Open-World Environments](https://arxiv.org/abs/2604.21192) | — | 2026 | [Paper](https://arxiv.org/abs/2604.21192) | Empirical analysis revealing failure modes and success factors of VLAs in the wild |
| [Being-H0.7: A Latent World-Action Model from Egocentric Videos](https://arxiv.org/abs/2605.00078) | — | 2026 | [Paper](https://arxiv.org/abs/2605.00078) | Latent world-action model brings future-aware reasoning into VLA without visual rollout |
| [LWD: Learning While Deploying — Fleet-Scale RL for Generalist Robot Policies](https://arxiv.org/abs/2605.00416) | — | 2026 | [Paper](https://arxiv.org/abs/2605.00416) | Fleet-scale offline-to-online RL for continual VLA post-training across 16 robots |
| [MoT-HRA: Learning Human-Intention Priors from Large-Scale Human Demonstrations](https://arxiv.org/abs/2604.24681) | — | 2026 | [Paper](https://arxiv.org/abs/2604.24681) | Hierarchical VLA learning human-intention priors from 2.2M human video episodes |

---

## 🎬 VA — Video-Action Models

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Video Generators Are Robot Policies](https://arxiv.org/abs/2406.16862) | CoRL 2024 | 2024 | [Paper](https://arxiv.org/abs/2406.16862) \| [Project](https://videopolicy.cs.columbia.edu/) \| [Code](https://github.com/cvlab-columbia/videopolicy) | Video generation models directly serve as robot policies |
| [IRASim: Learning Interactive Real-Robot Action Simulators](https://arxiv.org/abs/2406.14540) | ICCV 2025 | 2024 | [Paper](https://arxiv.org/abs/2406.14540) | Interactive video generation model for robot simulation |
| [GR-1: Unleashing Large-Scale Video Generative Pre-training for Visual Robot Manipulation](https://arxiv.org/abs/2312.13139) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2312.13139) | Video prediction pretraining transferable to manipulation |
| [SuSIE: Zero-Shot Robotic Manipulation with Pretrained Image-Editing Diffusion Models](https://arxiv.org/abs/2311.01775) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2311.01775) | Editing diffusion models as zero-shot robot subgoal generators |
| [GROOT: Learning to Follow Instructions by Watching How Things Are Done](https://arxiv.org/abs/2310.08235) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2310.08235) | Segment-then-follow paradigm from observation videos |

### 2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Video Prediction Policy: A Generalist Robot Policy with Predictive Visual Representations](https://arxiv.org/abs/2412.14803) | ICML 2025 | 2024 | [Paper](https://arxiv.org/abs/2412.14803) | Video future prediction as policy representation |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Chain-of-Action: Trajectory Autoregressive Modeling for Robotic Manipulation](https://arxiv.org/abs/2506.09990) | — | 2025 | [Paper](https://arxiv.org/abs/2506.09990) \| [Project](https://chain-of-action.github.io/) | ByteDance Seed's autoregressive action trajectory model |
| [Unified World Models: Coupling Video and Action Diffusion for Robot Pretraining](https://arxiv.org/abs/2504.02792) | — | 2025 | [Paper](https://arxiv.org/abs/2504.02792) \| [Project](https://weirdlabuw.github.io/uwm/) | Joint video-action diffusion for large-scale pretraining |
| [Unified Video Action Model](https://arxiv.org/abs/2503.00200) | RSS | 2025 | [Paper](https://arxiv.org/abs/2503.00200) \| [Project](https://unified-video-action-model.github.io/) | Joint video+action model for scalable robot learning |
| [Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation](https://arxiv.org/abs/2412.15109) | ICLR 2025 | 2025 | [Paper](https://arxiv.org/abs/2412.15109) \| [Project](https://nimolty.github.io/Seer/) | Predictive inverse dynamics for scalable manipulation |

### 2026

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [EgoSim: Egocentric World Simulator for Embodied Interaction Generation](https://arxiv.org/abs/2604.01001) | — | 2026 | [Paper](https://arxiv.org/abs/2604.01001) | Closed-loop egocentric simulator with updatable 3D scene state for interaction |
| [VAMPO: Policy Optimization for Improving Visual Dynamics in Video Action Models](https://arxiv.org/abs/2603.19370) | — | 2026 | [Paper](https://arxiv.org/abs/2603.19370) | Post-trains video action models with GRPO rewards over visual dynamics quality |
| [EVA: Aligning Video World Models with Executable Robot Actions via Inverse Dynamics Rewards](https://arxiv.org/abs/2603.17808) | — | 2026 | [Paper](https://arxiv.org/abs/2603.17808) | RL post-training aligns video generation with kinematically executable actions |
| [GigaWorld-Policy: An Efficient Action-Centered World-Action Model](https://arxiv.org/abs/2603.17240) | — | 2026 | [Paper](https://arxiv.org/abs/2603.17240) | Decouples video generation from action decoding for 9x faster inference |
| [DiT4DiT: Jointly Modeling Video Dynamics and Actions for Generalizable Robot Control](https://arxiv.org/abs/2603.10448) | — | 2026 | [Paper](https://arxiv.org/abs/2603.10448) | Couples video DiT and action DiT in a cascaded framework for joint training |
| [Causal World Modeling for Robot Control (LingBot-VA)](https://arxiv.org/abs/2601.21998) | — | 2026 | [Paper](https://arxiv.org/abs/2601.21998) \| [Code](https://github.com/robbyant/lingbot-va) | Causal video world model enables action learning without explicit action labels |

---

## 🦾 Visuomotor Policies

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [ACT: Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware](https://arxiv.org/abs/2304.13705) | RSS | 2023 | [Paper](https://arxiv.org/abs/2304.13705) \| [Code](https://github.com/tonyzhaozh/act) | CVAE + transformer for bimanual imitation |
| [Diffusion Policy: Visuomotor Policy Learning via Action Diffusion](https://arxiv.org/abs/2303.04137) | RSS | 2023 | [Paper](https://arxiv.org/abs/2303.04137) \| [Code](https://github.com/columbia-ai-robotics/diffusion_policy) | DDPM-based policy for robot manipulation |

### 2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [One-Step Diffusion Policy: Fast Visuomotor Policies via Diffusion Distillation](https://arxiv.org/abs/2410.21257) | ICML 2025 | 2024 | [Paper](https://arxiv.org/abs/2410.21257) | Single-step inference for diffusion policy |
| [Data Scaling Laws in Imitation Learning for Robotic Manipulation](https://arxiv.org/abs/2410.18647) | ICLR 2025 | 2024 | [Paper](https://arxiv.org/abs/2410.18647) | Empirical data scaling laws for imitation learning |
| [GenDP: 3D Semantic Fields for Category-Level Generalizable Diffusion Policy](https://arxiv.org/abs/2410.17488) | CoRL 2024 | 2024 | [Paper](https://arxiv.org/abs/2410.17488) | Generalizable diffusion via 3D semantic feature fields |
| [Generalizable Humanoid Manipulation with Improved 3D Diffusion Policies](https://arxiv.org/abs/2410.10803) | IROS 2025 | 2024 | [Paper](https://arxiv.org/abs/2410.10803) | 3D diffusion policy adapted for humanoid whole-body |
| [Scaling Diffusion Transformer to 1B Parameters for Robotic Manipulation](https://arxiv.org/abs/2409.14411) | ICRA 2025 | 2024 | [Paper](https://arxiv.org/abs/2409.14411) | Scaling study for diffusion transformer policies |
| [Diffusion Policy Policy Optimization](https://arxiv.org/abs/2409.00588) | ICLR | 2025 | [Paper](https://arxiv.org/abs/2409.00588) | RL fine-tuning of diffusion policies |
| [Bidirectional Decoding: Improving Action Chunking via Closed-Loop Resampling](https://arxiv.org/abs/2408.17355) | ICLR 2025 | 2024 | [Paper](https://arxiv.org/abs/2408.17355) | Bidirectional rollout improves temporal consistency |
| [In-Context Imitation Learning via Next-Token Prediction](https://arxiv.org/abs/2408.15980) | ICRA 2025 | 2024 | [Paper](https://arxiv.org/abs/2408.15980) \| [Project](https://icrt.dev/) | In-context robot learning via demo-conditioned autoregression |
| [Consistency Policy: Accelerated Visuomotor Policies via Consistency Distillation](https://arxiv.org/abs/2405.07503) | RSS 2025 | 2024 | [Paper](https://arxiv.org/abs/2405.07503) | One-step diffusion policy via consistency model distillation |
| [3D Diffusion Policy: Generalizable Visuomotor Policy Learning via 3D Representations](https://arxiv.org/abs/2403.03954) | RSS | 2025 | [Paper](https://arxiv.org/abs/2403.03954) | Point cloud observations for 3D-aware diffusion policies |
| [3D Diffuser Actor: Policy Diffusion with 3D Scene Representations](https://arxiv.org/abs/2402.10885) | CoRL 2024 | 2024 | [Paper](https://arxiv.org/abs/2402.10885) | Language-conditioned diffusion in 3D scene feature space |

### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [GauDP: Multi-Agent Collaboration through Gaussian-Image Synergy in Diffusion Policies](https://arxiv.org/abs/2511.00998) | NeurIPS | 2025 | [Paper](https://arxiv.org/abs/2511.00998) \| [Project](https://ziyeeee.github.io/gaudp.io/) | Gaussian splatting + diffusion for multi-robot policies |
| [Spatial Policy: Spatially-Aware Visuomotor Policy for Manipulation](https://arxiv.org/abs/2508.15874) | — | 2025 | [Paper](https://arxiv.org/abs/2508.15874) \| [Code](https://github.com/PlantPotatoOnMoon/SpatialPolicy) | Spatial reasoning integration into visuomotor policies |
| [DiWA: Diffusion Policy Adaptation with World Models](https://arxiv.org/abs/2508.03645) | CoRL | 2025 | [Paper](https://arxiv.org/abs/2508.03645) \| [Code](https://github.com/acl21/diwa) | World model-guided diffusion policy adaptation |
| [Dex1B: Learning with 1B Demonstrations for Dexterous Manipulation](https://arxiv.org/abs/2506.17198) | RSS | 2025 | [Paper](https://arxiv.org/abs/2506.17198) \| [Project](https://jianglongye.com/dex1b/) | 1-billion demo pre-training for dexterous hands |
| [Streaming Flow Policy: Treating Action Trajectories as Flow Trajectories](https://arxiv.org/abs/2505.21851) | CoRL Oral | 2025 | [Paper](https://arxiv.org/abs/2505.21851) \| [Project](https://siddancha.github.io/streaming-flow-policy/) | Simplifies diffusion policies via streaming flow |
| [UniSkill: Imitating Human Videos via Cross-Embodiment Skill Representations](https://arxiv.org/abs/2505.08787) | CoRL 2025 | 2025 | [Paper](https://arxiv.org/abs/2505.08787) \| [Project](https://kimhanjung.github.io/UniSkill/) | Cross-embodiment skill transfer from human video |
| [H3DP: Triply-Hierarchical Diffusion Policy for Visuomotor Learning](https://arxiv.org/abs/2505.07819) | — | 2025 | [Paper](https://arxiv.org/abs/2505.07819) \| [Project](https://lyy-iiis.github.io/h3dp/) | Three-level hierarchy in diffusion policy |
| [CLAM: Continuous Latent Action Models for Robot Learning from Unlabeled Demos](https://arxiv.org/abs/2505.04999) | — | 2025 | [Paper](https://arxiv.org/abs/2505.04999) \| [Project](https://clamrobot.github.io/) | Continuous latent actions learned from unlabeled video |
| [Latent Diffusion Planning for Imitation Learning](https://arxiv.org/abs/2504.16925) | ICML 2025 | 2025 | [Paper](https://arxiv.org/abs/2504.16925) \| [Project](https://amberxie88.github.io/ldp/) | Latent space diffusion for long-horizon robot planning |
| [Sim-and-Real Co-Training: A Simple Recipe for Vision-Based Robotic Manipulation](https://arxiv.org/abs/2503.24361) | — | 2025 | [Paper](https://arxiv.org/abs/2503.24361) \| [Project](https://co-training.github.io/) | Simple co-training bridge between sim and real |
| [ZeroMimic: Distilling Robotic Manipulation Skills from Web Videos](https://arxiv.org/abs/2503.23877) | ICRA 2025 | 2025 | [Paper](https://arxiv.org/abs/2503.23877) \| [Project](https://zeromimic.github.io/) | Zero-shot manipulation from web video via distillation |
| [ManipTrans: Efficient Dexterous Bimanual Manipulation Transfer via Residual Learning](https://arxiv.org/abs/2503.21860) | CVPR 2025 | 2025 | [Paper](https://arxiv.org/abs/2503.21860) \| [Project](https://maniptrans.github.io/) | Residual learning for bimanual dexterous transfer |
| [Humanoid Policy ~ Human Policy](https://arxiv.org/abs/2503.13441) | — | 2025 | [Paper](https://arxiv.org/abs/2503.13441) \| [Project](https://human-as-robot.github.io/) | Direct transfer from human motion policy to humanoid |
| [Dense Policy: Bidirectional Autoregressive Learning of Actions](https://arxiv.org/abs/2503.13217) | — | 2025 | [Paper](https://arxiv.org/abs/2503.13217) \| [Project](https://selen-suyue.github.io/DspNet/) | Bidirectional AR action sequence for rich action learning |
| [Reactive Diffusion Policy: Slow-Fast Visual-Tactile Policy for Contact-Rich Manipulation](https://arxiv.org/abs/2503.02881) | RSS | 2025 | [Paper](https://arxiv.org/abs/2503.02881) \| [Project](https://reactive-diffusion-policy.github.io/) | Dual-speed diffusion policy with tactile feedback |
| [Phantom: Training Robots Without Robots Using Only Human Videos](https://arxiv.org/abs/2503.00779) | — | 2025 | [Paper](https://arxiv.org/abs/2503.00779) \| [Project](https://phantom-human-videos.github.io/) | Robot policy from human videos without robot data |
| [ASAP: Aligning Simulation and Real-World Physics for Humanoid Whole-Body Skills](https://arxiv.org/abs/2502.01143) | RSS 2025 | 2025 | [Paper](https://arxiv.org/abs/2502.01143) | Sim-to-real alignment for agile humanoid locomotion |
| [MoDE: Mixture of Experts Diffusion Policy for Multitask Learning](https://arxiv.org/abs/2412.12953) | ICLR | 2025 | [Paper](https://arxiv.org/abs/2412.12953) \| [Project](https://mbreuss.github.io/MoDE_Diffusion_Policy/) | MoE-based diffusion transformer for multi-task policies |
| [FlowPolicy: Fast 3D Flow-Based Policy via Consistency Flow Matching](https://arxiv.org/abs/2412.04987) | AAAI | 2025 | [Paper](https://arxiv.org/abs/2412.04987) \| [Code](https://github.com/zql-kk/FlowPolicy) | Consistency flow matching for fast 3D robot control |

### 2026

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [HiFlow: Tokenization-Free Scale-Wise Autoregressive Policy Learning via Flow Matching](https://arxiv.org/abs/2603.27281) | — | 2026 | [Paper](https://arxiv.org/abs/2603.27281) | Coarse-to-fine autoregressive policy on continuous actions without tokenization |
| [One-Step Flow Policy: Self-Distillation for Fast Visuomotor Policies](https://arxiv.org/abs/2603.12480) | — | 2026 | [Paper](https://arxiv.org/abs/2603.12480) | Single-step action generation via self-consistency + self-guided mode sharpening |
| [Ada3Drift: Adaptive Training-Time Drifting for One-Step 3D Visuomotor Manipulation](https://arxiv.org/abs/2603.11984) | — | 2026 | [Paper](https://arxiv.org/abs/2603.11984) | Shifts iterative denoising from inference to training for 1-NFE 3D policy |
| [VPWEM: Non-Markovian Visuomotor Policy with Working and Episodic Memory](https://arxiv.org/abs/2603.04910) | — | 2026 | [Paper](https://arxiv.org/abs/2603.04910) | Combines sliding-window working memory and compressed episodic memory in diffusion policy |
| [Robot-DIFT: Distilling Diffusion Features for Geometrically Consistent Visuomotor Control](https://arxiv.org/abs/2602.11934) | — | 2026 | [Paper](https://arxiv.org/abs/2602.11934) | Distills generative diffusion geometry priors into a deterministic control backbone |
| [Gated Memory Policy](https://arxiv.org/abs/2604.18933) | — | 2026 | [Paper](https://arxiv.org/abs/2604.18933) | Adaptive gating selects Markovian vs. history-dependent policy per task context |
| [OmniUMI: Towards Physically Grounded Robot Learning via Human-Aligned Multimodal Interaction](https://arxiv.org/abs/2604.10647) | — | 2026 | [Paper](https://arxiv.org/abs/2604.10647) | Extends UMI with force/tactile sensing for contact-rich manipulation |
| [Cosmos Policy: Fine-Tuning Video Models for Visuomotor Control and Planning](https://arxiv.org/abs/2601.16163) | — | 2026 | [Paper](https://arxiv.org/abs/2601.16163) | Adapts large pretrained video model into robot policy via single-stage fine-tuning |
| [VADF: Vision-Adaptive Diffusion Policy Framework for Efficient Robotic Manipulation](https://arxiv.org/abs/2604.15938) | — | 2026 | [Paper](https://arxiv.org/abs/2604.15938) | Vision-driven dual-adaptive diffusion policy reducing convergence time and inference timeouts |
| [VistaBot: View-Robust Robot Manipulation via Spatiotemporal-Aware View Synthesis](https://arxiv.org/abs/2604.21914) | ICRA | 2026 | [Paper](https://arxiv.org/abs/2604.21914) | Spatiotemporal view synthesis enables view-robust real-world manipulation |
| [DockAnywhere: Data-Efficient Visuomotor Policy for Mobile Manipulation](https://arxiv.org/abs/2604.15023) | RA-L | 2026 | [Paper](https://arxiv.org/abs/2604.15023) | Novel demonstration generation enables data-efficient mobile manipulation policy learning |
| [Referring-Aware Visuomotor Policy for Closed-Loop Manipulation](https://arxiv.org/abs/2604.05544) | — | 2026 | [Paper](https://arxiv.org/abs/2604.05544) | Referring expression guidance enhances robustness to OOD execution errors and re-routing |
| [BridgeACT: Bridging Human Demonstrations to Robot Actions via Affordances](https://arxiv.org/abs/2604.23249) | — | 2026 | [Paper](https://arxiv.org/abs/2604.23249) | Affordance framework learns manipulation from human videos without robot data |

---

## 🏭 Robot Foundation Model Tech Reports

| System | Organization | Year | Links | TL;DR |
|--------|-------------|------|-------|-------|
| [Causal World Modeling for Robot Control (LingBot-VA)](https://arxiv.org/abs/2601.21998) | RobbyAnt (Xiaomi) | 2026 | [Paper](https://arxiv.org/abs/2601.21998) \| [Project](https://technology.robbyant.com/lingbot-va) \| [Code](https://github.com/robbyant/lingbot-va) | Video world modeling + VL pre-training for robot learning |
| [A Pragmatic VLA Foundation Model (LingBot-VLA)](https://arxiv.org/abs/2601.18692) | RobbyAnt (Xiaomi) | 2026 | [Paper](https://arxiv.org/abs/2601.18692) \| [Project](https://technology.robbyant.com/lingbot-vla/) \| [Code](https://github.com/Robbyant/lingbot-vla/) | Xiaomi RobbyAnt's pragmatic VLA foundation model for robot manipulation |
| [GigaBrain-0: A World Model-Powered Vision-Language-Action Model](https://arxiv.org/abs/2510.19430) | GigaAI | 2025 | [Paper](https://arxiv.org/abs/2510.19430) \| [Code](https://github.com/open-gigaai/giga-brain-0) | World model-powered VLA |
| [Being-H0: Vision-Language-Action Pretraining from Large-Scale Human Videos](https://arxiv.org/abs/2507.15597) | BeingBeyond | 2025 | [Paper](https://arxiv.org/abs/2507.15597) \| [Code](https://github.com/BeingBeyond/Being-H0) | Humanoid pretraining from egocentric human video |
| [GR-3 Technical Report](https://arxiv.org/abs/2507.15493) | ByteDance Seed | 2025 | [Paper](https://arxiv.org/abs/2507.15493) \| [Project](https://seed.bytedance.com/GR3) | ByteDance Seed's third-gen generative robot policy |
| [π0.5: A Vision-Language-Action Model with Open-World Generalization](https://arxiv.org/abs/2504.16054) | Physical Intelligence | 2025 | [Paper](https://arxiv.org/abs/2504.16054) \| [Project](https://www.pi.website/blog/pi05) | π0 generalized to open-world settings |
| [GR00T N1: An Open Foundation Model for Generalist Humanoid Robots](https://arxiv.org/abs/2503.14734) | NVIDIA | 2025 | [Paper](https://arxiv.org/abs/2503.14734) \| [Code](https://github.com/NVIDIA/Isaac-GR00T) | NVIDIA open humanoid foundation model |
| [EnerVerse: Envisioning Embodied Future Space for Robotics Manipulation](https://arxiv.org/abs/2501.01895) | AgiBot (星动纪元) | 2025 | [Paper](https://arxiv.org/abs/2501.01895) | AgiBot's generative future-state model for manipulation |
| [π0: A Vision-Language-Action Flow Model for General Robot Control](https://arxiv.org/abs/2410.24164) | Physical Intelligence | 2024 | [Paper](https://arxiv.org/abs/2410.24164) | Flow-matching VLA; dexterous multi-task control |
| [Gemini Robotics: Bringing AI into the Physical World](https://storage.googleapis.com/deepmind-media/gemini-robotics/gemini_robotics_report.pdf) | Google DeepMind | 2025 | [Report](https://storage.googleapis.com/deepmind-media/gemini-robotics/gemini_robotics_report.pdf) | Google DeepMind multimodal robot control system |
| [Helix: A Vision-Language-Action Model for Generalist Humanoid Control](https://www.figure.ai/news/helix) | Figure AI | 2025 | [Report](https://www.figure.ai/news/helix) | Figure AI's dual-system VLA for humanoid control |
| [JoyAI-RA 0.1: A Foundation Model for Robotic Autonomy](https://arxiv.org/abs/2604.20100) | — | 2026 | [Paper](https://arxiv.org/abs/2604.20100) | VLA foundation model addressing data diversity and cross-embodiment generalization |
| [ST-π: Structured SpatioTemporal VLA for Robotic Manipulation](https://arxiv.org/abs/2604.17880) | arXiv | 2026 | [Paper](https://arxiv.org/abs/2604.17880) \| [Code](https://github.com/chuanhaoma/ST-pi) | Structured spatiotemporal VLA with spatial-temporal attention for manipulation |
| [HiVLA: Hierarchical VLA for Long-Horizon Manipulation Tasks](https://arxiv.org/abs/2604.14125) | arXiv | 2026 | [Paper](https://arxiv.org/abs/2604.14125) \| [Project Page](https://tianshuoy.github.io/HiVLA-page/) | Hierarchical VLA combining high-level planning and low-level control |
| [AnchorVLA: Anchored Diffusion for Efficient Mobile Manipulation](https://arxiv.org/abs/2604.01567) | arXiv | 2026 | [Paper](https://arxiv.org/abs/2604.01567) \| [Code](https://github.com/jason-lim26/AnchorVLA) | Anchored diffusion VLA for mobile manipulation with residual drift correction |

---

## 🌍 World Models

### Seminal / Foundational

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [DreamerV3: Mastering Diverse Domains through World Models](https://arxiv.org/abs/2301.04104) | arXiv | 2023 | [Paper](https://arxiv.org/abs/2301.04104) \| [Code](https://github.com/danijar/dreamerv3) | Learns world model in latent space; zero-shot transfer |

### 2023–2024

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [IRASim: Learning Interactive Real-Robot Action Simulators](https://arxiv.org/abs/2406.14540) | ICCV 2025 | 2024 | [Paper](https://arxiv.org/abs/2406.14540) | Action-conditioned interactive simulation for robots |
| [RoboDreamer: Learning Compositional World Models for Robot Imagination](https://arxiv.org/abs/2404.12377) | ICML 2025 | 2024 | [Paper](https://arxiv.org/abs/2404.12377) | Compositional video-based world model for robot planning |
| [UniSim: Learning Interactive Real-World Simulators](https://arxiv.org/abs/2310.06114) | ICLR | 2024 | [Paper](https://arxiv.org/abs/2310.06114) | Universal simulator trained on real-world video data |
| [Genesis: A Generative and Universal Physics Engine for Robotics](https://genesis-embodied-ai.github.io/) | — | 2024 | [Project](https://genesis-embodied-ai.github.io/) | Generative physics engine for robot simulation |


### 2025

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [World4Omni: Zero-Shot Framework from Image Generation World Model to Robotic Manipulation](https://arxiv.org/abs/2506.23919) | — | 2025 | [Paper](https://arxiv.org/abs/2506.23919) \| [Project](https://world4omni.github.io/) | Image generation world model for zero-shot manipulation |
| [WorldVLA: Towards Autoregressive Action World Model](https://arxiv.org/abs/2506.21539) | — | 2025 | [Paper](https://arxiv.org/abs/2506.21539) \| [Code](https://github.com/alibaba-damo-academy/WorldVLA) | Autoregressive VLA that jointly models world states |
| [GAF: Gaussian Action Field as a Dynamic World Model for Robotic Manipulation](https://arxiv.org/abs/2506.14135) | — | 2025 | [Paper](https://arxiv.org/abs/2506.14135) | Gaussian splatting as dynamic world model |
| [V-JEPA 2: Self-Supervised Video Models Enable Understanding, Prediction and Planning](https://arxiv.org/abs/2506.09985) | — | 2025 | [Paper](https://arxiv.org/abs/2506.09985) \| [Code](https://github.com/facebookresearch/vjepa2) | Action-conditioned V-JEPA for robot planning |
| [3DFlowAction: Cross-Embodiment Manipulation from 3D Flow World Model](https://arxiv.org/abs/2506.06199) | — | 2025 | [Paper](https://arxiv.org/abs/2506.06199) \| [Code](https://github.com/Hoyyyaard/3DFlowAction/) | 3D flow world model for cross-embodiment manipulation |
| [Evaluating Robot Policies in a World Model](https://arxiv.org/abs/2506.00613) | — | 2025 | [Paper](https://arxiv.org/abs/2506.00613) \| [Project](https://world-model-eval.github.io/) | World model as robot policy evaluation environment |
| [LaDi-WM: Latent Diffusion-based World Model for Predictive Manipulation](https://arxiv.org/abs/2505.11528) | CoRL 2025 | 2025 | [Paper](https://arxiv.org/abs/2505.11528) | Latent diffusion world model for manipulation prediction |
| [FlowDreamer: RGB-D World Model with Flow-based Motion for Manipulation](https://arxiv.org/abs/2505.10075) | RA-L 2025 | 2025 | [Paper](https://arxiv.org/abs/2505.10075) \| [Project](https://sharinka0715.github.io/FlowDreamer/) | Optical flow-based RGB-D world model for manipulation |
| [EWMBench: Evaluating Scene, Motion, and Semantic Quality in Embodied World Models](https://arxiv.org/abs/2505.09694) | — | 2025 | [Paper](https://arxiv.org/abs/2505.09694) \| [Code](https://github.com/AgibotTech/EWMBench) | Benchmark for evaluating embodied world models |
| [Unified World Models: Coupling Video and Action Diffusion for Robot Pretraining](https://arxiv.org/abs/2504.02792) | — | 2025 | [Paper](https://arxiv.org/abs/2504.02792) \| [Project](https://weirdlabuw.github.io/uwm/) | Joint video+action diffusion for world model pretraining |
| [AdaWorld: Learning Adaptable World Models with Latent Actions](https://arxiv.org/abs/2503.18938) | ICML 2025 | 2025 | [Paper](https://arxiv.org/abs/2503.18938) \| [Project](https://adaptable-world-model.github.io/) | Adaptable world models via latent action discovery |
| [DyWA: Dynamics-adaptive World Action Model for Non-prehensile Manipulation](https://arxiv.org/abs/2503.16806) | — | 2025 | [Paper](https://arxiv.org/abs/2503.16806) \| [Project](https://pku-epic.github.io/DyWA/) | Dynamics-adaptive world model for pushing tasks |
| [Generalist World Model Pre-Training for Efficient Reinforcement Learning](https://arxiv.org/abs/2502.19544) | — | 2025 | [Paper](https://arxiv.org/abs/2502.19544) | Generalist world model pretraining for RL policies |
| [Robotic World Model: Neural Network Simulator for Policy Optimization](https://arxiv.org/abs/2501.10100) | — | 2025 | [Paper](https://arxiv.org/abs/2501.10100) | Neural network as high-fidelity robotic world simulator |
| [Cosmos: World Foundation Model Platform for Physical AI](https://arxiv.org/abs/2501.03575) | — | 2025 | [Paper](https://arxiv.org/abs/2501.03575) \| [Code](https://github.com/nvidia-cosmos/cosmos-predict1) | NVIDIA's world foundation model for physical AI |

### 2026

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [HCLSM: Hierarchical Causal Latent State Machines for Object-Centric World Modeling](https://arxiv.org/abs/2603.29090) | — | 2026 | [Paper](https://arxiv.org/abs/2603.29090) | Three-level temporal dynamics with slot attention for causal object-centric world model |
| [Kinema4D: Kinematic 4D World Modeling for Spatiotemporal Embodied Simulation](https://arxiv.org/abs/2603.16669) | — | 2026 | [Paper](https://arxiv.org/abs/2603.16669) | URDF-driven 4D robot trajectory controls generative model for robot-world interaction |
| [PlayWorld: Learning Robot World Models from Autonomous Play](https://arxiv.org/abs/2603.09030) | — | 2026 | [Paper](https://arxiv.org/abs/2603.09030) | Trains high-fidelity video world models entirely from unsupervised robot self-play |
| [PointWorld: Scaling 3D World Models for In-The-Wild Robotic Manipulation](https://arxiv.org/abs/2601.03782) | — | 2026 | [Paper](https://arxiv.org/abs/2601.03782) \| [Project](https://point-world.github.io/) | 3D point cloud world models at scale |
| [Cortex 2.0: Grounding World Models in Real-World Industrial Deployment](https://arxiv.org/abs/2604.20246) | — | 2026 | [Paper](https://arxiv.org/abs/2604.20246) | World model addressing compounding failures in long-horizon industrial manipulation |
| [UniT: Toward a Unified Physical Language for Human-to-Humanoid Policy Learning and World Modeling](https://arxiv.org/abs/2604.19734) | — | 2026 | [Paper](https://arxiv.org/abs/2604.19734) \| [Project](https://arxiv.org/abs/2604.19734) | Unified latent action tokenizer bridging human-to-humanoid policy and world modeling |
| [Mask World Model: Predicting What Matters for Robust Robot Policy Learning](https://arxiv.org/abs/2604.19683) | — | 2026 | [Paper](https://arxiv.org/abs/2604.19683) | Masks irrelevant factors in video world model prediction for better generalization |
| [Hi-WM: Human-in-the-World-Model for Scalable Robot Post-Training](https://arxiv.org/abs/2604.21741) | — | 2026 | [Paper](https://arxiv.org/abs/2604.21741) \| [Project Page](https://hi-wm.github.io/) | Human feedback scales world model post-training for robot policy improvement |
| [VLA-World: Vision-Language-Action World Models for Autonomous Driving](https://arxiv.org/abs/2604.09059) | — | 2026 | [Paper](https://arxiv.org/abs/2604.09059) | Integrates VLA reasoning with video world model for consistent autonomous driving decisions |

---

## 📊 Benchmarks & Datasets

### Manipulation Benchmarks

| Benchmark | Venue | Year | Links | Description |
|-----------|-------|------|-------|-------------|
| [RoboArena: Distributed Real-World Evaluation of Generalist Robot Policies](https://arxiv.org/abs/2506.18123) | — | 2025 | [Paper](https://arxiv.org/abs/2506.18123) \| [Project](https://robo-arena.github.io/) | Distributed real-world evaluation platform |
| [RoboTwin 2.0: Scalable Data Generator and Benchmark with Strong Domain Randomization](https://arxiv.org/abs/2506.18088) | — | 2025 | [Paper](https://arxiv.org/abs/2506.18088) \| [Project](https://robotwin-platform.github.io/) | Extended RoboTwin with large-scale domain randomization |
| [RoboCerebra: Large-scale Benchmark for Long-horizon Robotic Manipulation](https://arxiv.org/abs/2506.06677) | — | 2025 | [Paper](https://arxiv.org/abs/2506.06677) \| [Project](https://robocerebra.github.io/) | Long-horizon manipulation evaluation with dense annotations |
| [ManipBench: Benchmarking VLMs for Low-Level Robot Manipulation](https://arxiv.org/abs/2505.09698) | — | 2025 | [Paper](https://arxiv.org/abs/2505.09698) \| [Project](https://manipbench.github.io/) | VLM capability evaluation for manipulation |
| [AutoEval: Autonomous Evaluation of Generalist Robot Manipulation Policies in Real World](https://arxiv.org/abs/2503.24278) | — | 2025 | [Paper](https://arxiv.org/abs/2503.24278) \| [Project](https://auto-eval.github.io/) | Automated real-world manipulation policy evaluation |
| [BOSS: Benchmark for Observation Space Shift in Long-Horizon Tasks](https://arxiv.org/abs/2502.15679) | — | 2025 | [Paper](https://arxiv.org/abs/2502.15679) | Benchmark for handling observation distribution shift |
| [VLABench: Large-Scale Benchmark for Language-Conditioned Robotics Manipulation](https://arxiv.org/abs/2412.18194) | — | 2024 | [Paper](https://arxiv.org/abs/2412.18194) | Long-horizon language-conditioned manipulation evaluation |
| [ManiSkill3: GPU Parallelized Robotics Simulation and Rendering](https://arxiv.org/abs/2410.00425) | — | 2024 | [Paper](https://arxiv.org/abs/2410.00425) \| [Code](https://github.com/haosulab/ManiSkill) | GPU-accelerated simulation benchmark; v1-v3 series |
| [RoboTwin: Dual-Arm Robot Benchmark with Generative Digital Twins](https://arxiv.org/abs/2409.02920) | CVPR | 2025 | [Paper](https://arxiv.org/abs/2409.02920) \| [Code](https://github.com/TianxingChen/RoboTwin) | Dual-arm manipulation with generative digital twin data |
| [SimplerEnv: Simulated Manipulation Policy Evaluation Environments for Real Robot Setups](https://arxiv.org/abs/2405.05941) | CoRL 2024 | 2024 | [Paper](https://arxiv.org/abs/2405.05941) \| [Code](https://github.com/simpler-env/SimplerEnv) | Sim evaluation mirroring real-world robot setups |
| [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) | ICRA | 2024 | [Paper](https://arxiv.org/abs/2310.08864) \| [Project](https://robotics-transformer-x.github.io/) | Cross-embodiment dataset with 500k+ real-robot demos |
| [LIBERO: Benchmarking Knowledge Transfer for Lifelong Robot Learning](https://arxiv.org/abs/2306.03310) | NeurIPS | 2023 | [Paper](https://arxiv.org/abs/2306.03310) \| [Code](https://github.com/Lifelong-Robot-Learning/LIBERO) | Lifelong learning benchmark with 130 robot manipulation tasks |
| [FurnitureBench: Reproducible Real-World Benchmark for Long-Horizon Complex Manipulation](https://arxiv.org/abs/2305.12556) | RSS | 2023 | [Paper](https://arxiv.org/abs/2305.12556) \| [Code](https://github.com/clvrai/furniture-bench) | Assembly of real IKEA furniture; long-horizon challenge |
| [CALVIN: A Benchmark for Language-Conditioned Policy Learning for Long-Horizon Robot Manipulation](https://arxiv.org/abs/2112.03227) | ICRA | 2022 | [Paper](https://arxiv.org/abs/2112.03227) \| [Code](https://github.com/mees/calvin) | Long-horizon language-conditioned manipulation chains |
| [MetaWorld: A Benchmark and Evaluation for Multi-Task and Meta Reinforcement Learning](https://arxiv.org/abs/1910.10897) | — | 2019 | [Paper](https://arxiv.org/abs/1910.10897) \| [Code](https://github.com/Farama-Foundation/Metaworld) | 50 diverse robot arm tasks for meta/multi-task RL |
| [RLBench: The Robot Learning Benchmark & Learning Environment](https://arxiv.org/abs/1909.12271) | — | 2019 | [Paper](https://arxiv.org/abs/1909.12271) \| [Code](https://github.com/stepjam/RLBench) | 100 robot manipulation tasks in CoppeliaSim |
| [RoboVerse: Unified Platform, Dataset and Benchmark for Scalable Robot Learning](https://roboverseorg.github.io/) | — | 2025 | [Paper](https://roboverseorg.github.io/static/pdfs/paper_supp_20250405_1820.pdf) \| [Code](https://github.com/RoboVerseOrg/RoboVerse) | Unified sim-to-real benchmark and dataset platform |
| [RoboWM-Bench: Manipulation-Centric Benchmark for World Models in Robotics](https://arxiv.org/abs/2604.19092) | arXiv | 2026 | [Paper](https://arxiv.org/abs/2604.19092) \| [Project Page](https://robowm-bench.github.io/RoboWM-Bench/) | Manipulation-centric benchmark for evaluating world models in robotics |

### Robot Datasets

| Dataset | Venue | Year | Links | Description |
|---------|-------|------|-------|-------------|
| [AgiBot World Alpha](https://arxiv.org/abs/2503.06669) | — | 2025 | [Paper](https://arxiv.org/abs/2503.06669) \| [Project](https://agibot-world.com/) | 1M+ demonstrations from 100 robots, 217 tasks |
| [Open-H-Embodiment: Large-Scale Dataset for Foundation Models in Medical Robotics](https://arxiv.org/abs/2604.21017) | — | 2026 | [Paper](https://arxiv.org/abs/2604.21017) | Multi-institution consortium dataset enabling foundation models for medical robotics |
| [EgoMimic: Scaling Imitation Learning via Egocentric Video](https://arxiv.org/abs/2410.24221) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2410.24221) | Egocentric human video for robot imitation learning |
| [DROID: A Large-Scale In-the-Wild Robot Manipulation Dataset](https://arxiv.org/abs/2403.12945) | RSS | 2024 | [Paper](https://arxiv.org/abs/2403.12945) \| [Project](https://droid-dataset.github.io/) | 76k demonstrations across 86 environments |
| [Open X-Embodiment: Robotic Learning Datasets and RT-X Models](https://arxiv.org/abs/2310.08864) | ICRA Best Paper | 2024 | [Paper](https://arxiv.org/abs/2310.08864) \| [Project](https://robotics-transformer-x.github.io/) | 1M+ real-robot demos from 22 robots and 21 institutions |
| [BridgeData V2: A Dataset for Robot Learning at Scale](https://arxiv.org/abs/2308.12952) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2308.12952) \| [Project](https://rail-berkeley.github.io/bridgedata/) | 60k+ kitchen manipulation demonstrations |
| [RH20T: A Comprehensive Robotic Dataset for Learning Diverse Skills](https://arxiv.org/abs/2307.00595) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2307.00595) \| [Project](https://rh20t.github.io/) | 110k+ multi-task demonstrations with rich annotations |
| [Learning Fine-Grained Bimanual Manipulation with Low-Cost Hardware (ALOHA)](https://arxiv.org/abs/2304.13705) | RSS | 2023 | [Paper](https://arxiv.org/abs/2304.13705) \| [Code](https://github.com/tonyzhaozh/aloha) | Bimanual ALOHA robot teleoperation dataset |
| [Something-Something v2: A Compositional Video-Text Dataset](https://arxiv.org/abs/1706.04261) | ICCV | 2017 | [Paper](https://arxiv.org/abs/1706.04261) | Large-scale human-object interaction video dataset |

### Whole-body / Humanoid Benchmarks

| Benchmark | Venue | Year | Links | Description |
|-----------|-------|------|-------|-------------|
| [BEHAVIOR Robot Suite: Real-World Whole-Body Manipulation for Household Activities](https://arxiv.org/abs/2503.05652) | RSS | 2025 | [Paper](https://arxiv.org/abs/2503.05652) \| [Project](https://behavior-robot-suite.github.io/) | Real-world household whole-body manipulation tasks |
| [HumanPlus: Humanoid Shadowing and Imitation from Humans](https://arxiv.org/abs/2406.10454) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2406.10454) \| [Code](https://github.com/MarkFzp/humanplus) | Whole-body humanoid policy from human shadowing |
| [OmniH2O: Universal and Dexterous Human-to-Humanoid Whole-Body Teleoperation](https://arxiv.org/abs/2406.08858) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2406.08858) \| [Code](https://github.com/LeCAR-Lab/human2humanoid) | Universal human-to-humanoid whole-body teleoperation |
| [HumanoidBench: Simulated Humanoid Benchmark for Whole-Body Locomotion and Manipulation](https://arxiv.org/abs/2403.10506) | — | 2024 | [Paper](https://arxiv.org/abs/2403.10506) \| [Code](https://github.com/carlosferrazza/humanoid-bench) | 27 tasks for full-body humanoid control |
| [BEHAVIOR-1K: A Human-Centered Embodied AI Benchmark](https://arxiv.org/abs/2403.09227) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2403.09227) | 1000 daily activities for embodied AI evaluation |
| [ExBody: Expressive Whole-Body Control for Humanoid Robots](https://arxiv.org/abs/2402.16796) | CoRL | 2024 | [Paper](https://arxiv.org/abs/2402.16796) \| [Code](https://github.com/WangZiyi9143/ExBody) | Whole-body expressive motion control for humanoids |
| [SMPL-X: Expressive Body Capture: 3D Hands, Face, and Body from a Single Image](https://arxiv.org/abs/1904.05866) | CVPR | 2019 | [Paper](https://arxiv.org/abs/1904.05866) \| [Code](https://github.com/vchoutas/smplx) | Expressive parametric human body model |
| [LocoMuJoCo: A Comprehensive Imitation Learning Benchmark for Locomotion](https://loco-mujoco.readthedocs.io/) | — | 2025 | [Docs](https://loco-mujoco.readthedocs.io/) \| [Code](https://github.com/robfiras/loco-mujoco) | Comprehensive locomotion benchmark in MuJoCo |

---

## 🔧 Simulators & Data Engines

### Simulators

| Simulator | Organization | Year | Links | TL;DR |
|-----------|-------------|------|-------|-------|
| [Genesis: A Generative and Universal Physics Engine](https://arxiv.org/abs/2501.08949) | Genesis Team | 2025 | [Paper](https://arxiv.org/abs/2501.08949) \| [Project](https://genesis-embodied-ai.github.io/) | Ultra-fast generative physics engine for robot learning |
| [ManiSkill2: A Unified Benchmark for Generalizable Manipulation Skills](https://arxiv.org/abs/2302.04143) | UCSD | 2023 | [Paper](https://arxiv.org/abs/2302.04143) \| [Project](https://maniskill2.github.io/) | Large-scale manipulation benchmark with 2000+ object assets |
| [Isaac Gym: High Performance GPU-Based Physics Simulation For Robot Learning](https://arxiv.org/abs/2108.10470) | NVIDIA | 2021 | [Paper](https://arxiv.org/abs/2108.10470) | GPU-accelerated physics sim for massively parallel robot RL |
| [robosuite: A Modular Simulation Framework and Benchmark for Robot Learning](https://arxiv.org/abs/2009.12293) | ARISE | 2020 | [Paper](https://arxiv.org/abs/2009.12293) \| [Project](https://robosuite.ai/) | Modular robot manipulation benchmark built on MuJoCo |
| [SAPIEN: A SimulAted Part-based Interactive ENvironment](https://arxiv.org/abs/2003.08515) | UCSD | 2020 | [Paper](https://arxiv.org/abs/2003.08515) \| [Project](https://sapien.ucsd.edu/) | Articulated object sim with realistic physics for manipulation |
| [MuJoCo: A physics engine for model-based control](https://ieeexplore.ieee.org/document/6386109) | DeepMind | 2012 | [Paper](https://ieeexplore.ieee.org/document/6386109) \| [Docs](https://mujoco.org) | Fast, accurate physics engine; standard benchmark for robot learning |

### Data Generation Engines

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [RoboVerse: Towards a Unified Platform, Dataset, and Benchmark for Scalable and Generalizable Robot Learning](https://arxiv.org/abs/2504.00461) | — | 2025 | [Paper](https://arxiv.org/abs/2504.00461) | Unified sim platform + dataset + benchmark for generalizable robot learning |
| [GeniSim: Generalizing Robot Manipulation Skills via Large Language Model-Based Data Generation](https://arxiv.org/abs/2311.11714) | — | 2023 | [Paper](https://arxiv.org/abs/2311.11714) | LLM generates novel manipulation tasks in simulation for data augmentation |
| [RoboGen: Towards Unleashing Infinite Data for Automated Robot Learning via Generative Simulation](https://arxiv.org/abs/2311.01455) | ICML | 2024 | [Paper](https://arxiv.org/abs/2311.01455) \| [Project](https://robogen-ai.github.io/) | LLM-driven task + asset + reward generation in IsaacGym |
| [MimicGen: A Data Generation System for Scalable Robot Learning using Human Demonstrations](https://arxiv.org/abs/2310.17596) | CoRL | 2023 | [Paper](https://arxiv.org/abs/2310.17596) \| [Project](https://mimicgen.github.io/) | Automatically generates large-scale demos from few human examples |
| [Lucid-XR: An Extended-Reality Data Engine for Robotic Manipulation](https://arxiv.org/abs/2605.00244) | — | 2026 | [Paper](https://arxiv.org/abs/2605.00244) \| [Project](https://lucidxr.github.io/) | XR headset-based physics sim + video gen for zero-shot sim-to-real transfer |

---

## 📚 Survey

### Manipulation & Robot Learning Survey

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Diffusion Models for Robots: A Survey](https://arxiv.org/abs/2504.11002) | — | 2025 | [Paper](https://arxiv.org/abs/2504.11002) | Comprehensive survey of diffusion models in robotics |
| [World Model for Robot Learning: A Comprehensive Survey](https://arxiv.org/abs/2605.00080) | — | 2026 | [Paper](https://arxiv.org/abs/2605.00080) | Comprehensive survey of world models for robot learning, covering paradigms and applications |
| [Vision-Language-Action in Robotics: A Survey of Datasets, Benchmarks, and Data Engines](https://arxiv.org/abs/2604.23001) | TMLR | 2026 | [Paper](https://arxiv.org/abs/2604.23001) | Data-centric analysis of VLA datasets, benchmarks, and data engines |
| [From Text to Motion: A Survey on Foundation Models for Robot Manipulation](https://arxiv.org/abs/2501.04838) | — | 2025 | [Paper](https://arxiv.org/abs/2501.04838) | Survey of foundation models for robot manipulation |
| [A Survey on Vision-Language-Action Models for Embodied AI](https://arxiv.org/abs/2405.14093) | — | 2024 | [Paper](https://arxiv.org/abs/2405.14093) | Comprehensive survey on VLA model architectures |
| [Robot Learning from Human Demonstrations: A Survey](https://arxiv.org/abs/2311.07474) | — | 2023 | [Paper](https://arxiv.org/abs/2311.07474) | Survey on human demonstration-based robot learning |
| [A Survey on Embodied AI: From Simulators to Research Challenges](https://arxiv.org/abs/2103.04918) | IEEE TPAMI | 2022 | [Paper](https://arxiv.org/abs/2103.04918) | Foundational survey covering simulators and challenges |
| [A Survey of Robot Learning from Demonstration](https://www.cs.cmu.edu/~mmv/papers/09ras-survey.pdf) | Robotics and Autonomous Systems | 2009 | [Paper](https://www.cs.cmu.edu/~mmv/papers/09ras-survey.pdf) | Foundational survey on imitation learning for robotics |
| [Imitation Learning: A Survey of Learning Methods](https://dl.acm.org/doi/10.1145/3054912) | ACM Computing Surveys | 2018 | [Paper](https://dl.acm.org/doi/10.1145/3054912) | Comprehensive survey on imitation learning methods |

### Embodied AI General Survey

| Paper | Venue | Year | Links | TL;DR |
|-------|-------|------|-------|-------|
| [Towards Generalist Robots: A Survey on Foundation Models in Robotics](https://arxiv.org/abs/2312.08782) | — | 2024 | [Paper](https://arxiv.org/abs/2312.08782) | Broad survey on foundation model integration in robotics |
| [Foundation Models in Robotics: Applications, Challenges, and the Future](https://arxiv.org/abs/2312.07843) | — | 2023 | [Paper](https://arxiv.org/abs/2312.07843) | Foundation models applied to robotics: applications, challenges, future |
| [A Survey on Large Language Models for Robotics](https://arxiv.org/abs/2311.07226) | — | 2023 | [Paper](https://arxiv.org/abs/2311.07226) | LLMs as planners, coders, and reasoners for robots |
| [A Survey on Embodied AI: From Simulators to Research Challenges](https://arxiv.org/abs/2103.04918) | IEEE TPAMI | 2022 | [Paper](https://arxiv.org/abs/2103.04918) | Covers simulators, tasks, algorithms for embodied AI |
| [3D Generation for Embodied AI and Robotic Simulation: A Survey](https://arxiv.org/abs/2604.26509) | — | 2026 | [Paper](https://arxiv.org/abs/2604.26509) \| [Project](https://3dgen4robot.github.io) | Comprehensive survey of 3D generation methods for embodied AI and robot simulation |
| [Embodied Intelligence via Learning and Evolution](https://arxiv.org/abs/2102.02202) | Nature Comm. | 2021 | [Paper](https://arxiv.org/abs/2102.02202) | Evolution and learning for embodied intelligence |



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

[![Star History Chart](https://api.star-history.com/svg?repos=Noietch/Awesome-Learning-for-Manipulation&type=Date)](https://star-history.com/#Noietch/Awesome-Learning-for-Manipulation&Date)
