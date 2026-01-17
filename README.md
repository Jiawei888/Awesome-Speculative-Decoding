# Awesome-Speculative-Decoding

A curated list of research papers, systems, and resources on **Speculative Decoding** and its variants for efficient LLM inference.

Speculative decoding is a key technique for accelerating autoregressive generation by leveraging draft models, verification strategies, and parallelism, and has become increasingly important in large-scale and edge inference systems.

---

## Contents

- [Survey & Overview](#survey--overview)
- [Core Speculative Decoding](#core-speculative-decoding)
- [Verification & Token Acceptance](#verification--token-acceptance)
- [Multi-Draft & Cascaded Speculation](#multi-draft--cascaded-speculation)
- [Tree-based & Parallel Verification](#tree-based--parallel-verification)
- [System & Engine Support](#system--engine-support)
- [Related Topics](#related-topics)

---

## Survey & Overview

Papers that provide surveys, unified perspectives, or high-level analysis of speculative decoding and related acceleration techniques.

| Date    | Title | Venue | Paper | Code |
|---------|-------|-------|-------|------|
| YYYY.MM | Paper Title | Conference / Journal | [Paper](link) | [Code](link) |

---

## Core Speculative Decoding

Foundational works that introduce or formalize speculative decoding, including basic draft–target frameworks.

| Date    | Title | Venue | Paper | Code |
|---------|-------|-------|-------|------|
| 2023.07 | Fast Inference from Transformers via Speculative Decoding | ICML 2023 | [Paper](https://openreview.net/pdf?id=C9NEblP8vS) | - |
| 2025.02 | PEARL: PARALLEL SPECULATIVE DECODING WITH ADAPTIVE DRAFT LENGTH | ICLR 2025 | [Paper](https://arxiv.org/pdf/2408.11850) | [Code](https://github.com/smart-lty/ParallelSpeculativeDecoding) |
| 2025.03 | EAGLE: Speculative Sampling Requires Rethinking Feature Uncertainty | ICML 2024 | [Paper](https://arxiv.org/pdf/2401.15077) | [Code](https://github.com/SafeAILab/EAGLE) |
| 2024.06 | EAGLE-2: Faster Inference of Language Models with Dynamic Draft Trees | EMNLP 2024 | [Paper](https://arxiv.org/pdf/2406.16858) | [Code](https://github.com/SafeAILab/EAGLE) |
| 2025.04 | EAGLE-3: Scaling up Inference Acceleration of Large Language Models via Training-Time Test | NeurIPS 2025 | [Paper](https://openreview.net/pdf?id=C9NEblP8vS) | [Code](https://github.com/SafeAILab/EAGLE) |
| 2024.07 | MEDUSA: Simple LLM Inference Acceleration Framework with Multiple Decoding Heads | ICML 2024 | [Paper](https://arxiv.org/pdf/2401.10774) | [Code](https://github.com/FasterDecoding/Medusa) |
| 2025.04 | EdgeLLM: Fast On-Device LLM Inference With Speculative Decoding | TMC 2025 | [Paper](https://ieeexplore.ieee.org/document/10812936) | - |
| 2024.04 | SpecInfer: Accelerating Large Language Model Serving with Tree-based Speculative Inference and Verification | ASPLOS 2024 | [Paper](https://openreview.net/pdf?id=C9NEblP8vS) | - |
| 2025.11 | Dovetail: A CPU/GPU Heterogeneous Speculative Decoding for LLM inference | EMNLP 2025 | [Paper](https://aclanthology.org/2025.emnlp-main.879.pdf) | [Code](https://github.com/ddInference/Dovetail) |
| 2025.07 | Growing a Twig to Accelerate Large Vision-Language Models | ICCV 2025 | [Paper](https://openaccess.thecvf.com/content/ICCV2025/papers/Shao_Growing_a_Twig_to_Accelerate_Large_Vision-Language_Models_ICCV_2025_paper.pdf) | [Code](https://github.com/MILVLG/twigvlm) |
| 2025.06 | SpecEE: Accelerating Large Language Model Inference with Speculative Early Exiting | ISCA 2025 | [Paper](https://dl.acm.org/doi/10.1145/3695053.3730996) | - |
| 2023.12 | Accelerating Mobile Language Model via Speculative Decoding and NPU-Coordinated Execution | ARXIV | [Paper](https://arxiv.org/pdf/2510.15312) | - |
| 2024.12 | Cascade Speculative Drafting for Even Faster LLM Inference | NeurIPS 2024 | [Paper](https://arxiv.org/pdf/2312.11462) | [Code](https://github.com/lfsszd/CS-Drafting) |
| 2024.05 | Accelerating Speculative Decoding using Dynamic Speculation Length | ARXIV | [Paper](https://arxiv.org/pdf/2405.04304v1) | - |
| 2025.04 | Hierarchical Speculative Decoding with Dynamic Windows for Efficient Language Model Inference | NAACL 2025 | [Paper](https://aclanthology.org/2025.findings-naacl.462.pdf) | - |
| 2025.07 | PipeSpec: Breaking Stage Dependencies in Hierarchical LLM Decoding | ACL 2025 | [Paper](https://aclanthology.org/anthology-files/pdf/findings/2025.findings-acl.669.pdf) | [Code](https://github.com/BradMcDanel/PipeSpec) |
| 2024.04 | On Speculative Decoding for Multimodal Large Language Models | CVPR 2024 | [Paper](https://aclanthology.org/2025.findings-naacl.462.pdf) | - |
| 2025.09 | CAS-Spec: Cascade Adaptive Self-Speculative Decoding for On-the-Fly Lossless Inference Acceleration of LLMs | NeurIPS 2025 | [Paper](https://openreview.net/pdf?id=m0bR0sxhfL) | - |
| 2025.07 | SuffixDecoding: Extreme Speculative Decoding for Emerging AI Applications | NeurIPS 2025 | [Paper](https://arxiv.org/pdf/2411.04975) | [Code](https://github.com/snowflakedb/ArcticInference) |
| 2025.07 | SEQUOIA: Scalable and Robust Speculative Decoding | NAACL 2025 | [Paper](https://openreview.net/pdf?id=rk2L9YGDi2) | - |
| 2024.07 | SpecExec: Massively Parallel Speculative Decoding for Interactive LLM Inference on Consumer Devices | NeurIPS 2024 | [Paper](https://proceedings.neurips.cc/paper_files/paper/2024/file/1d91d5689e251d27993a3c2182dddcf7-Paper-Conference.pdf) | - |
| 2025.06 | SwiftSpec: Ultra-Low Latency LLM Decoding by Scaling Asynchronous Speculative Decoding | ARXIV | [Paper](https://arxiv.org/pdf/2506.11309) | - |
| 2024.11 | PipeInfer: Accelerating LLM Inference using Asynchronous Pipelined Speculation| SC 2024 | [Paper](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10793190) | - |
| 2025.05 | Speculative Decoding Meets Quantization: Compatibility Evaluation and Hierarchical Framework Design | ARXIV | [Paper](https://arxiv.org/pdf/2505.22179) | [Code](https://github.com/AI9Stars/SpecMQuant) |




---

## Verification & Token Acceptance

Works focusing on token verification rules, acceptance probability modeling, relaxed matching, or correctness guarantees.

| Date    | Title | Venue | Paper | Code |
|---------|-------|-------|-------|------|
| YYYY.MM | Paper Title | Conference / Journal | [Paper](link) | [Code](link) |

---

## Multi-Draft & Cascaded Speculation

Approaches using multiple draft models, cascaded verification, or hierarchical speculative pipelines.

| Date    | Title | Venue | Paper | Code |
|---------|-------|-------|-------|------|
| YYYY.MM | Paper Title | Conference / Journal | [Paper](link) | - |

---

## Tree-based & Parallel Verification

Techniques that construct token trees or batch multiple candidate sequences to improve verification efficiency.

| Date    | Title | Venue | Paper | Code |
|---------|-------|-------|-------|------|
| YYYY.MM | Paper Title | Conference / Journal | [Paper](link) | [Code](link) |

---

## System & Engine Support

Systems and inference engines that implement or optimize speculative decoding in practice.

| Name | Type | Paper | Code |
|------|------|-------|------|
| vLLM | Inference Engine | - | https://github.com/vllm-project/vllm |
| llama.cpp | Inference Engine | - | https://github.com/ggerganov/llama.cpp |
| System / Engine Name | System | [Paper](link) | [Code](link) |

---

## Related Topics

Closely related techniques that interact with speculative decoding.

- Draft model compression
- Partial-layer execution
- Early-exit and adaptive decoding
- Heterogeneous and edge inference
- Multimodal speculative decoding

---

## Contributing

Contributions are welcome. Please feel free to submit a pull request to add new papers, systems, or resources.

---

## License

This repository is licensed under the MIT License.
