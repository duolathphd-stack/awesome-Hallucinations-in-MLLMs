# Awesome-MLLMs-Hallucination [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)



---
- [Awesome MLLMs Hallucination](#awesome-Hallucinations-in-MLLMs)
     - [Survey](#Survey)
     - [Hallucination Mitigation](#Mitigation_Method)
     - [Hallucination Benchmark](#Evaluation_Benchmark)


## Survey


1. [A Survey on Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2402.00253.pdf) (2024.02.01)
2. [Visual Hallucination: Definition, Quantification, and Prescriptive Remediations](https://arxiv.org/pdf/2403.17306.pdf) (2024.03.26)
3. [Hallucination of Multimodal Large Language Models: A Survey](https://arxiv.org/pdf/2404.18930) (2024.04.29)
4. [Unveiling Hallucination in Text, Image, Video, and Audio Foundation Models: A Comprehensive Survey](https://arxiv.org/pdf/2405.09589) (2024.05.20)
5. [Benchmark Evaluations, Applications, and Challenges of Large Vision Language Models: A Survey](https://arxiv.org/pdf/2501.02189) (2025.01.04)
6. [Exploring Hallucination of Large Multimodal Models in Video Understanding: Benchmark, Analysis and Mitigation](https://arxiv.org/pdf/2503.19622) (2025.03.25)
7. [Why Contrastive Decoding Fails to Address Multimodal Hallucination](https://arxiv.org/pdf/2504.10020) (2025.04.18)
8. [A Survey of Multimodal Hallucination Evaluation and Detection](https://arxiv.org/pdf/2507.19024) (2025.07.25)
9. [Review of Hallucination Understanding in Large Language and Vision Models](https://arxiv.org/pdf/2510.00034) (2025.09.26)


## Mitigation_Method

| Method | Pub | Date |
| ------ | ---- | ---- |
| [ObjMLM: Plausible May Not Be Faithful: Probing Object Hallucination in Vision-Language Pre-training](https://arxiv.org/pdf/2210.07688.pdf) | arXiv'23 | 2023.2.10 |
| [MMCoT: Multimodal Chain-of-Thought Reasoning in Language Models](https://arxiv.org/pdf/2302.00923.pdf) | arXiv'23 | 2023.2.17 |
| [LRV-GAVIE: Mitigating Hallucination in Large Multi-Modal Models via Robust Instruction Tuning](https://arxiv.org/pdf/2306.14565.pdf) | **ICLR'24** | 2023.6.26 |
| [LLaVA-RLHF: Aligning Large Multimodal Models with Factually Augmented RLHF](https://arxiv.org/pdf/2309.14525.pdf) | **ACL'24** | 2023.9.25 |
| [LURE: Analyzing and Mitigating Object Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2310.00754.pdf) | **ICLR'23** | 2023.10.1 |
| [HallE-Switch: Controlling Object Hallucination in Large Vision Language Models](https://arxiv.org/pdf/2310.01779.pdf) | arXiv'23 | 2023.10.3 |
| [Woodpecker: Hallucination Correction for Multimodal Large Language Models](https://arxiv.org/abs/2310.16045) | **SCIS'24** | 2023.10.24 |
| [VOLCANO: Mitigating Multimodal Hallucination through Self-Feedback Guided Revision](https://arxiv.org/pdf/2311.07362.pdf) | **NAACL'24** | 2023.11.14 |
| [HalluciDoctor: Mitigating Hallucinatory Toxicity in Visual Instruction Data](https://arxiv.org/pdf/2311.13614.pdf) | **CVPR'24** | 2023.11.22 |
| [RAH-Bench: Mitigating Hallucination in Visual Language Models with Visual Supervision](https://arxiv.org/pdf/2311.16479.pdf) | arXiv'23 | 2023.11.27 |
| [HA-DPO: Beyond Hallucinations: Enhancing LVLMs through Hallucination-Aware Direct Preference Optimization](https://arxiv.org/pdf/2311.16839.pdf) | **ICME'24** | 2023.11.28 |
| [VCD: Mitigating Object Hallucinations in Large Vision-Language Models through Visual Contrastive Decoding](https://arxiv.org/pdf/2311.16922.pdf) | **CVPR'24** | 2023.11.28 |
| [FGHE: Mitigating Fine-Grained Hallucination by Fine-Tuning Large Vision-Language Models with Caption Rewrites](https://arxiv.org/pdf/2312.01701.pdf) | arXiv'23 | 2023.12.4 |
| [RLHF-V: Towards Trustworthy MLLMs via Behavior Alignment from Fine-grained Correctional Human Feedback](https://arxiv.org/pdf/2312.00849.pdf) | **CVPR'24** | 2023.12.1 |
| [MOCHa: Mitigating Open-Vocabulary Caption Hallucinations](https://arxiv.org/pdf/2312.03631.pdf) | arXiv'23 | 2023.12.6 |
| [HACL: Hallucination Augmented Contrastive Learning for Multimodal Large Language Model](https://arxiv.org/pdf/2312.06968.pdf) | arXiv'23 | 2023.12.12 |
| [SILKIE: Preference Distillation for Large Visual Language Models](https://arxiv.org/pdf/2312.10665.pdf) | arXiv'23 | 2023.12.17 |
| [OPERA: Alleviating Hallucination in Multi-Modal Large Language Models via Over-Trust Penalty and Retrospection-Allocation](https://arxiv.org/pdf/2311.17911.pdf) | **CVPR'24** | 2024.1.1 |
| [KAM-CoT: Knowledge Augmented Multimodal Chain-of-Thoughts Reasoning](https://arxiv.org/pdf/2401.12863.pdf) | arXiv'24 | 2024.1.23 |
| [Enhancing Multimodal Large Language Models with Vision Detection Models: An Empirical Study](https://arxiv.org/pdf/2401.17981.pdf) | arXiv'24 | 2024.1.31 |
| [ViGoR: Improving Visual Grounding of Large Vision Language Models with Fine-Grained Reward Modeling](https://arxiv.org/pdf/2402.06118.pdf) | arXiv'24 | 2024.2.9 |
| [SKIP \N: A Simple Method to Reduce Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2402.01345.pdf) | arXiv'24 | 2024.2.12 |
| [MARINE: Mitigating Object Hallucination in Large Vision-Language Models via Classifier-Free Guidance](https://arxiv.org/pdf/2402.08680.pdf) | arXiv'24 | 2024.2.13 |
| [IDK-Instructions: Visually Dehallucinative Instruction Generation: Know What You Don’t Know](https://arxiv.org/pdf/2402.09717.pdf) | arXiv'24 | 2024.2.15 |
| [EFUF: Efficient Fine-grained Unlearning Framework for Mitigating Hallucinations in Multimodal Large Language Models](https://arxiv.org/pdf/2402.09801.pdf) | arXiv'24 | 2024.2.15 |
| [LogicCheckGPT: Logical Closed Loop: Uncovering Object Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2402.11622.pdf) | arXiv'24 | 2024.2.18 |
| [POVID: Aligning Modalities in Vision Large Language Models via Preference Fine-tuning](https://arxiv.org/pdf/2402.11411.pdf) | arXiv'24 | 2024.2.18 |
| [Less is More: Mitigating Multimodal Hallucination from an EOS Decision Perspective](https://arxiv.org/pdf/2402.14545.pdf) | **ACL'24** | 2024.2.22 |
| [CGD: Seeing is Believing: Mitigating Hallucination in Large Vision-Language Models via CLIP-Guided Decoding](https://arxiv.org/pdf/2402.15300.pdf) | arXiv'24 | 2024.2.23 |
| [IBD: Alleviating Hallucinations in Large Vision-Language Models via Image-Biased Decoding](https://arxiv.org/pdf/2402.18476.pdf) | arXiv'24 | 2024.2.28 |
| [HALC: Object Hallucination Reduction via Adaptive Focal-Contrast Decoding](https://arxiv.org/pdf/2403.00425.pdf) | arXiv'24 | 2024.3.1 |
| [Evaluating and Mitigating Number Hallucinations in Large Vision-Language Models: A Consistency Perspective](https://arxiv.org/pdf/2403.01373.pdf) | arXiv'24 | 2024.3.3 |
| [AIT: Mitigating Dialogue Hallucination for Large Multi-modal Models via Adversarial Instruction Tuning](https://arxiv.org/pdf/2403.10492.pdf) | arXiv'24 | 2024.3.15 |
| [DVP: What if...?: Counterfactual Inception to Mitigate Hallucination Effects in Large Multimodal Models](https://arxiv.org/pdf/2403.13513.pdf) | arXiv'24 | 2024.3.20 |
| [M3ID: Multi-Modal Hallucination Control by Visual Information Grounding](https://arxiv.org/pdf/2403.14003.pdf) | **CVPR'24** | 2024.3.20 |
| [PENSIEVE: Retrospect-then-Compare Mitigates Visual Hallucination](https://arxiv.org/pdf/2403.14401.pdf) | arXiv'24 | 2024.3.21 |
| [ESREAL: Exploiting Semantic Reconstruction to Mitigate Hallucinations in Vision-Language Models](https://arxiv.org/pdf/2403.16167.pdf) | arXiv'24 | 2024.3.26 |
| [ICD: Mitigating Hallucinations in Large Vision-Language Models with Instruction Contrastive Decoding](https://arxiv.org/pdf/2403.18715.pdf) | **ACL'24** | 2024.3.27 |
| [FGAIF: Aligning Large Vision-Language Models with Fine-grained AI Feedback](https://arxiv.org/pdf/2404.05046.pdf) | arXiv'24 | 2024.4.7 |
| [Prescribing the Right Remedy: Mitigating Hallucinations in Large Vision-Language Models via Targeted Instruction Tuning](https://arxiv.org/pdf/2404.10332.pdf) | arXiv'24 | 2024.4.16 |
| [FACT: Teaching MLLMs with Faithful, Concise and Transferable Rationales](https://arxiv.org/pdf/2404.11129) | arXiv'24 | 2024.4.17 |
| [TVP: Exploring the Transferability of Visual Prompting for Multimodal Large Language Models](https://arxiv.org/pdf/2404.11207) | arXiv'24 | 2024.4.17 |
| [TextSquare: Scaling up Text-Centric Visual Instruction Tuning](https://arxiv.org/pdf/2404.12803) | arXiv'24 | 2024.4.19 |
| [HSA-DPO: Detecting and Mitigating Hallucination in Large Vision Language Models via Fine-Grained AI Feedback](https://arxiv.org/pdf/2404.14233) | arXiv'24 | 2024.4.22 |
| [Visual Fact Checker: Enabling High-Fidelity Detailed Caption Generation](https://arxiv.org/pdf/2404.19752) | **CVPR'24** | 2024.4.30 |
| [CSR: Calibrated Self-Rewarding Vision Language Models](https://arxiv.org/pdf/2405.14622) | arXiv'24 | 2024.5.23 |
| [HIO: Alleviating Hallucinations in Large Vision-Language Models through Hallucination-Induced Optimization](https://arxiv.org/pdf/2405.15356) | arXiv'24 | 2024.5.24 |
| [VDGD: Mitigating LVLM Hallucinations in Cognitive Prompts by Bridging the Visual Perception Gap](https://arxiv.org/pdf/2405.15683) | arXiv'24 | 2024.5.24 |
| [RLAIF-V: Aligning MLLMs through Open-Source AI Feedback for Super GPT-4V Trustworthines](https://arxiv.org/pdf/2405.17220) | arXiv'24 | 2024.5.27 |
| [AvisC: Don’t Miss the Forest for the Trees: Attentional Vision Calibration for Large Vision Language Models](https://arxiv.org/pdf/2405.17820) | arXiv'24 | 2024.5.28 |
| [RITUAL: Random Image Transformations as a Universal Anti-hallucination Lever in LVLMs](https://arxiv.org/pdf/2405.17821) | arXiv'24 | 2024.5.28 |
| [HALVA: Mitigating Object Hallucination via Data Augmented Contrastive Tuning](https://arxiv.org/pdf/2405.18654) | arXiv'24 | 2024.5.28 |
| [NoiseBoost: Alleviating Hallucination with Noise Perturbation for Multimodal Large Language Models](https://arxiv.org/pdf/2405.20081) | arXiv'24 | 2024.5.30 |
| [CODE: Contrasting Self-generated Description to Combat Hallucination in Large Multi-modal Model](https://arxiv.org/pdf/2406.01920v1) | arXiv'24 | 2024.6.4 |
| [mDPO: Conditional Preference Optimization for Multimodal Large Language Models](https://arxiv.org/pdf/2406.11839) | arXiv'24 | 2024.6.17 |
| [DBD: Do More Details Always Introduce More Hallucinations in LVLM-based Image Captioning?](https://arxiv.org/pdf/2406.12663) | arXiv'24 | 2024.6.18 |
| [AGLA: Mitigating Object Hallucinations in Large Vision-Language Models with Assembly of Global and Local Attention](https://arxiv.org/pdf/2406.12718) | **CVPR'25** | 2024.6.18 |
| [Residual Visual Decoding: Investigating and Mitigating the Multimodal Hallucination Snowballing in Large Vision-Language Models](https://arxiv.org/pdf/2407.00569) | **ACL'24** | 2024.6.30 |
| [BDHS: UNDERSTANDING ALIGNMENT IN MULTIMODAL LLMS: A COMPREHENSIVE STUDY](https://arxiv.org/pdf/2407.02477) | arXiv'24 | 2024.7.2 |
| [REVERIE: Reflective Instruction Tuning: Mitigating Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2407.11422) | **ECCV'24** | 2024.7.16 |
| [VACoDe: Visual Augmented Contrastive Decoding](https://arxiv.org/pdf/2408.05337) | arXiv'24 | 2024.7.26 |
| [PAI: Paying More Attention to Image: A Training-Free Method for Alleviating Hallucination in LVLMs](https://arxiv.org/pdf/2407.21771) | **ECCV'24** | 2024.7.31 |
| [MHR: Mitigating Multilingual Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2408.00550) | arXiv'24 | 2024.8.1 |
| [ARA: Alleviating Hallucination in Large Vision-Language Models with Active Retrieval Augmentation](https://arxiv.org/pdf/2408.00555) | **TOMM'25** | 2024.8.1 |
| [SID: Self-Introspective Decoding: Alleviating Hallucinations for Large Vision-Language Models](https://arxiv.org/pdf/2408.02032) | arXiv'24 | 2024.8.4 |
| [LCD: Mitigating Hallucinations in Large Vision-Language Models (LVLMs) via Language-Contrastive Decoding](https://arxiv.org/pdf/2408.04664) | arXiv'24 | 2024.8.6 |
| [Detect-then-Calibrate: A Comprehensive Benchmark for Relation Hallucination Evaluation, Analysis and Mitigation in Multimodal Large Language Models](https://arxiv.org/pdf/2408.09429) | arXiv'24 | 2024.8.18 |
| [CLIP-DPO: Vision-Language Models as a Source of Preference for Fixing Hallucinations in LVLMs](https://arxiv.org/pdf/2408.10433) | arXiv'24 | 2024.8.19 |
| [LQCD: Towards Analyzing and Mitigating Sycophancy in Large Vision-Language Models](https://arxiv.org/pdf/2408.11261) | arXiv'24 | 2024.8.21 |
| [RoVRM: A Robust Visual Reward Model Optimized via Auxiliary Textual Preference Data](https://arxiv.org/pdf/2408.12109) | arXiv'24 | 2024.8.22 |
| [ConVis: Contrastive Decoding with Hallucination Visualization for Mitigating Hallucinations in Multimodal Large Language Models](https://arxiv.org/pdf/2408.13906) | **AAAI'25** | 2024.8.25 |
| [See or Guess: Counterfactually Regularized Image Captioning](https://arxiv.org/pdf/2408.16809) | arXiv'24 | 2024.8.29 |
| [Look, Compare, Decide: Alleviating Hallucination in Large Vision-Language Models via Multi-View Multi-Path Reasoning](https://arxiv.org/pdf/2408.17150) | arXiv'24 | 2024.8.30 |
| [FaithD2T: Generating Faithful and Salient Text from Multimodal Data](https://arxiv.org/pdf/2409.03961) | arXiv'24 | 2024.9.6 |
| [RBD: Mitigating Hallucination in Visual-Language Models via Re-Balancing Contrastive Decoding](https://arxiv.org/pdf/2409.06485) | arXiv'24 | 2024.9.10 |
| [PACU: Effectively Enhancing Vision Language Large Models by Prompt Augmentation and Caption Utilization](https://arxiv.org/pdf/2409.14484) | arXiv'24 | 2024.9.22 |
| [Dentist: A Unified Hallucination Mitigation Framework for Large Vision-Language Models](https://arxiv.org/pdf/2409.16494) | **TMLR'24** | 2024.9.24 |
| [TCD: Diagnosing Event Hallucinations in Video LLMs](https://arxiv.org/pdf/2409.16597) | arXiv'24 | 2024.9.25 |
| [HELPD: Mitigating Hallucination of LVLMs by Hierarchical Feedback Learning with Vision-enhanced Penalty Decoding](https://arxiv.org/pdf/2409.20429) | arXiv'24 | 2024.9.30 |
| [PROJECTAWAY: Interpreting and Editing Vision-Language Representations to Mitigate Hallucinations](https://arxiv.org/pdf/2410.02762) | arXiv'24 | 2024.10.3 |
| [OHD-Caps: Investigating and Mitigating Object Hallucinations in Pretrained Vision-Language (CLIP) Models](https://arxiv.org/pdf/2410.03176) | **EMNLP'24** | 2024.10.4 |
| [LOOK TWICE BEFORE YOU ANSWER: Memory-Space Visual Retracing for Hallucination Mitigation in Multimodal Large Language Models](https://arxiv.org/pdf/2410.03577) | arXiv'24 | 2024.10.4 |
| [DAMRO: Dive into the Attention Mechanism of LVLM to Reduce Object Hallucination](https://arxiv.org/pdf/2410.04514) | **EMNLP'24** | 2024.10.6 |
| [CAUSALMM: Mitigating Modality Prior-Induced Hallucinations in Multimodal Large Language Models via Deciphering Attention Causality](https://arxiv.org/pdf/2410.04780) | **ICLR'25** | 2024.10.7 |
| [FROM PIXELS TO TOKENS: Revisiting Object Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2410.06795) | arXiv'24 | 2024.10.9 |
| [VHExpansion: Automatically Generating Visual Hallucination Test Cases for Multimodal Large Language Models](https://arxiv.org/pdf/2410.11242) | arXiv'24 | 2024.10.15 |
| [SGD: Mitigating Hallucinations in Large Vision-Language Models via Summary-Guided Decoding](https://arxiv.org/pdf/2410.13321) | arXiv'24 | 2024.10.17 |
| [Fine-Grained Verifiers: Preference Modeling as Next-token Prediction in Vision-Language Alignment](https://arxiv.org/pdf/2410.14148) | arXiv'24 | 2024.10.18 |
| [MFPO: Modality-Fair Preference Optimization for Trustworthy MLLM Alignment](https://arxiv.org/pdf/2410.15334) | arXiv'24 | 2024.10.20 |
| [CCA: Mitigating Object Hallucination via Concentric Causal Attention](https://arxiv.org/pdf/2410.15926) | **NIPS'24** | 2024.10.21 |
| [VTI: Reducing Hallucinations in Vision-Language Models via Latent Space Steering](https://arxiv.org/pdf/2410.15778) | arXiv'24 | 2024.10.22 |
| [V-DPO: Mitigating Hallucination in Large Vision Language Models via Vision-Guided Direct Preference Optimization](https://arxiv.org/pdf/2411.02712) | **EMNLP'24** | 2024.11.5 |
| [EAH: Seeing Clearly by Layer Two: Enhancing Attention Heads to Alleviate Hallucination in LVLMs](https://arxiv.org/pdf/2411.09968) | arXiv'24 | 2024.11.15 |
| [HDPO: Mitigating Hallucination in Multimodal Large Language Model via Hallucination-targeted Direct Preference Optimization](https://arxiv.org/pdf/2411.10436) | arXiv'24 | 2024.11.15 |
| [Thinking Before Looking: Improving Multimodal LLM Reasoning via Mitigating Visual Hallucination](https://arxiv.org/pdf/2411.12591) | arXiv'24 | 2024.11.15 |
| [CATCH: Complementary Adaptive Token-level Contrastive Decoding to Mitigate Hallucinations in LVLMs](https://arxiv.org/pdf/2411.12713) | arXiv'24 | 2024.11.19 |
| [Looking Beyond Text: Reducing Language bias in Large Vision-Language Models via Multimodal Dual-Attention and Soft-Image Guidance](https://arxiv.org/pdf/2411.14279) | arXiv'24 | 2024.11.21 |
| [ICT: Image-Object Cross-Level Trusted Intervention for Mitigating Object Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2411.15268) | arXiv'24 | 2024.11.22 |
| [VaLiD: Mitigating the Hallucination of Large Vision Language Models by Visual Layer Fusion Contrastive Decoding](https://arxiv.org/pdf/2411.15839) | arXiv'24 | 2024.11.24 |
| [Devils in Middle Layers of Large Vision-Language Models: Interpreting, Detecting and Mitigating Object Hallucinations via Attention Lens](https://arxiv.org/pdf/2411.16724) | arXiv'24 | 2024.11.23 |
| [TPO: A Topic-level Self-Correctional Approach to Mitigate Hallucinations in MLLMs](https://arxiv.org/pdf/2411.17265) | arXiv'24 | 2024.11.26 |
| [WhoBrings the Frisbee: Probing Hidden Hallucination Factors in Large Vision-Language Model via Causality Analysis](https://arxiv.org/pdf/2412.02946) | arXiv'24 | 2024.12.3 |
| [VisVM: Scaling Inference-Time Search with Vision Value Model for Improved Visual Comprehension](https://arxiv.org/pdf/2412.03704) | arXiv'24 | 2024.12.6 |
| [Verb Mirage: Unveiling and Assessing Verb Concept Hallucinations in Multimodal Large Language Models](https://arxiv.org/pdf/2412.04939) | arXiv'24 | 2024.12.6 |
| [From Uncertainty to Trust: Enhancing Reliability in Vision-Language Models with Uncertainty-Guided Dropout Decoding](https://arxiv.org/pdf/2412.06474) | arXiv'24 | 2024.12.9 |
| [VCD Analysis: Delve into Visual Contrastive Decoding for Hallucination Mitigation of Large Vision-Language Models](https://arxiv.org/pdf/2412.06775) | arXiv'24 | 2024.12.9 |
| [DEHALL: Combating Multimodal LLM Hallucination via Bottom-Up Holistic Reasoning](https://arxiv.org/pdf/2412.11124) | arXiv'24 | 2024.12.15 |
| [Nullu: Mitigating Object Hallucinations in Large Vision-Language Models via HalluSpace Projection](https://arxiv.org/pdf/2412.13817) | **CVPR'25** | 2024.12.18 |
| [VHD: Cracking the Code of Hallucination in LVLMs with Vision-aware Head Divergence](https://arxiv.org/pdf/2412.13949) | arXiv'24 | 2024.12.18 |
| [TPO: Token Preference Optimization with Self-Calibrated Visual-Anchored Rewards for Hallucination Mitigation](https://arxiv.org/pdf/2412.14487) | arXiv'24 | 2024.12.19 |
| [Toward Robust Hyper-Detailed Image Captioning: A Multiagent Approach and Dual Evaluation Metrics for Factuality and Coverage](https://arxiv.org/pdf/2412.15484) | arXiv'24 | 2024.12.20 |
| [VORD: Visual Ordinal Calibration for Mitigating Object Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2412.15739) | arXiv'24 | 2024.12.20 |
| [SENA: BeyondHuman Data: Aligning Multimodal Large Language Models by Iterative Self-Evolution](https://arxiv.org/pdf/2412.15650) | arXiv'24 | 2024.12.20 |
| [IMCCD: Mitigating Hallucination for Large Vision Language Model by Inter-Modality Correlation Calibration Decoding](https://arxiv.org/pdf/2501.01926) | arXiv'25 | 2025.1.3 |
| [EAGLE: Enhanced Visual Grounding Minimizes Hallucinations in Instructional Multimodal Models](https://arxiv.org/pdf/2501.02699) | arXiv'25 | 2025.1.6 |
| [Socratic Questioning: Learn to Self-guide Multimodal Reasoning in the Wild](https://arxiv.org/pdf/2501.02964) | arXiv'25 | 2025.1.7 |
| [VASparse: Towards Efficient Visual Hallucination Mitigation for Large Vision-Language Model via Visual-Aware Sparsification](https://arxiv.org/pdf/2501.06553) | **CVPR'25** | 2025.1.11 |
| [OPA-DPA: Mitigating Hallucinations in Large Vision-Language Models via DPO: On-Policy Data Hold the Key](https://arxiv.org/search/cs?query=hallucination+vision+&searchtype=all&abstracts=show&order=-announced_date_first&size=50) | **CVPR'25** | 2025.1.16 |
| [MIAVLM: Mitigating Hallucinations on Object Attributes using Multiview Images and Negative Instructions](https://arxiv.org/pdf/2501.10011) | arXiv'25 | 2025.1.17 |
| [llava-fix-hallucination: Fixing Imbalanced Attention to Mitigate In-Context Hallucination of Large Vision-Language Model](https://arxiv.org/pdf/2501.12206) | arXiv'25 | 2025.1.21 |
| [CHiP: Cross-modal Hierarchical Direct Preference Optimization for Multimodal LLMs](https://arxiv.org/pdf/2501.16629) | arXiv'25 | 2025.1.28 |
| [Poison as Cure: Visual Noise for Mitigating Object Hallucinations in LVMs](https://arxiv.org/pdf/2501.19164) | arXiv'25 | 2025.1.31 |
| [MINT: Mitigating Hallucinations in Large Vision-Language Models via Token Reduction](https://arxiv.org/pdf/2502.00717) | arXiv'25 | 2025.2.2 |
| [IFCD: Mitigating Hallucinations in Large Vision-Language Models with Internal Fact-based Contrastive Decoding](https://arxiv.org/pdf/2502.01056) | arXiv'25 | 2025.2.3 |
| [UAC/DAC: Mitigating Object Hallucinations in Large Vision-Language Models via Attention Calibration](https://arxiv.org/pdf/2502.01969) | arXiv'25 | 2025.2.4 |
| [VISTA: The Hidden Life of Tokens: Reducing Hallucination of Large Vision-Language Models via Visual Information Steering](https://arxiv.org/pdf/2502.03628) | arXiv'25 | 2025.2.5 |
| [DeGF: Self-Correcting Decoding with Generative Feedback for Mitigating Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2502.06130) | **ICLR'25** | 2025.2.10 |
| [CAP: Mitigating Hallucinations in Multimodal Spatial Relations through Constraint-Aware Prompting](https://arxiv.org/pdf/2502.08317) | arXiv'25 | 2025.2.12 |
| [RE-ALIGN: Aligning Vision Language Models via Retrieval-Augmented Direct Preference Optimization](https://arxiv.org/pdf/2502.13146) | arXiv'25 | 2025.2.18 |
| [Symmetrical Visual Contrastive Optimization (S-VCO): Aligning Vision-Language Models with Minimal Contrastive Images](https://arxiv.org/pdf/2502.13928) | arXiv'25 | 2025.2.19 |
| [API Cutoff: The Role of Background Information in Reducing Object Hallucination in Vision-Language Models: Insights from Cutoff API Prompting](https://arxiv.org/pdf/2502.15389) | arXiv'25 | 2025.2.21 |
| [Exploring Causes and Mitigation of Hallucinations in Large Vision Language Models](https://arxiv.org/pdf/2502.16842) | arXiv'25 | 2025.2.24 |
| [F-CLipScore: Vision-Encoders (Already) Know What They See: Mitigating Object Hallucination via Simple Fine-Grained CLIPScore](https://arxiv.org/pdf/2502.20034) | arXiv'25 | 2025.2.27 |
| [ADAVIB: Mitigating Hallucinations in Large Vision-Language Models by Adaptively Constraining Information Flow](https://arxiv.org/pdf/2502.20750) | **AAAI'25** | 2025.2.28 |
| [Octopus: Alleviating Hallucination via Dynamic Contrastive Decoding](https://arxiv.org/pdf/2503.00361) | **CVPR'25** | 2025.3.1 |
| [TPC: Cross-Temporal Prediction Connection for Vision-Language Model Hallucination Reduction](https://arxiv.org/pdf/2503.04457) | arXiv'25 | 2025.3.6 |
| [Treble Counterfactual VLMs: A Causal Approach to Hallucination](https://arxiv.org/pdf/2503.06169) | arXiv'25 | 2025.3.6 |
| [PerturboLLaVA: Reducing Multimodal Hallucinations with Perturbative Visual Training](https://arxiv.org/pdf/2503.06486) | arXiv'25 | 2025.3.9 |
| [EAZY: Eliminating Hallucinations in LVLMs by Zeroing out Hallucinatory Image Tokens](https://arxiv.org/pdf/2503.07772) | arXiv'25 | 2025.3.10 |
| [Attention Reallocation: Towards Zero-cost and Controllable Hallucination Mitigation of MLLMs](https://arxiv.org/pdf/2503.08342) | arXiv'25 | 2025.3.12 |
| [Attention Hijackers: Detect and Disentangle Attention Hijacking in LVLMs for Hallucination Mitigation](https://arxiv.org/pdf/2503.08216) | arXiv'25 | 2025.3.14 |
| [Through the Magnifying Glass: Adaptive Perception Magnification for Hallucination-Free VLM Decoding](https://arxiv.org/pdf/2503.10183) | arXiv'25 | 2025.3.14 |
| [TruthPrInt: Mitigating LVLM Object Hallucination Via Latent Truthful-Guided Pre-Intervention](https://arxiv.org/pdf/2503.10602) | arXiv'25 | 2025.3.14 |
| [ClearSight: Visual Signal Enhancement for Object Hallucination Mitigation in Multimodal Large Language Models](https://arxiv.org/pdf/2503.13107) | **CVPR'25** | 2025.3.14 |
| [MFP: Mitigating Object Hallucinations in MLLMs via Multi-Frequency Perturbations](https://arxiv.org/pdf/2503.14895) | arXiv'25 | 2025.3.19 |
| [IAVA: Instruction-Aligned Visual Attention for Mitigating Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2503.18556) | arXiv'25 | 2025.3.24 |
| [HLPU: Mitigating Low-Level Visual Hallucinations Requires Self-Awareness: Database, Model and Training Strategy](https://arxiv.org/pdf/2503.20673) | arXiv'25 | 2025.3.27 |
| [TARAC: Mitigating Hallucination in LVLMs via Temporal Attention Real-time Accumulative Connection](https://arxiv.org/pdf/2504.04099) | arXiv'25 | 2025.4.5 |
| [Decoupling Contrastive Decoding: Robust Hallucination Mitigation in Multimodal Large Language Models](https://arxiv.org/pdf/2504.08809) | arXiv'25 | 2025.4.9 |
| [ECD: Efficient Contrastive Decoding with Probabilistic Hallucination Detection - Mitigating Hallucinations in Large Vision Language Models](https://arxiv.org/pdf/2504.12137) | arXiv'25 | 2025.4.16 |
| [Generate, but Verify: Reducing Hallucination in Vision-Language Models with Retrospective Resampling](https://arxiv.org/pdf/2504.13169) | arXiv'25 | 2025.4.17 |
| [Hydra: An Agentic Reasoning Approach for Enhancing Adversarial Robustness and Mitigating Hallucinations in Vision-Language Models](https://arxiv.org/pdf/2504.14395) | arXiv'25 | 2025.4.19 |
| [BBVPE: Black-Box Visual Prompt Engineering for Mitigating Object Hallucination in Large Vision Language Models](https://arxiv.org/pdf/2504.21559) | arXiv'25 | 2025.4.30 |
| [TTA Framework: Mitigating Image Captioning Hallucinations in Vision-Language Models](https://arxiv.org/pdf/2505.03420) | arXiv'25 | 2025.5.6 |
| [Critique Before Thinking: Mitigating Hallucination through Rationale-Augmented Instruction Tuning](https://arxiv.org/pdf/2505.07172) | arXiv'25 | 2025.5.12 |
| [DCLA: Mitigating Hallucinations via Inter-Layer Consistency Aggregation in Large Vision-Language Models](https://arxiv.org/pdf/2505.12343) | arXiv'25 | 2025.5.18 |
| [CICD: Cross-Image Contrastive Decoding: Precise, Lossless Suppression of Language Priors in Large Vision-Language Models](https://arxiv.org/pdf/2505.10634) | arXiv'25 | 2025.5.20 |
| [SEVI: Aligning Attention Distribution to Information Flow for Hallucination Mitigation in Large Vision-Language Models](https://arxiv.org/pdf/2505.14257) | arXiv'25 | 2025.5.20 |
| [OViP: Online Vision-Language Preference Learning](https://arxiv.org/pdf/2505.15963) | arXiv'25 | 2025.5.21 |
| [SSL: Steering LVLMs via Sparse Autoencoder for Hallucination Mitigation](https://arxiv.org/pdf/2505.16146) | arXiv'25 | 2025.5.22 |
| [SPIN: Mitigating Hallucinations in Vision-Language Models through Image-Guided Head Suppression](https://arxiv.org/pdf/2505.16411) | arXiv'25 | 2025.5.22 |
| [ED: Do You Keep an Eye on What I Ask? Mitigating Multimodal Hallucination via Attention-Guided Ensemble Decoding](https://arxiv.org/pdf/2505.17529) | arXiv'25 | 2025.5.23 |
| [VaLSe: Seeing It or Not? Interpretable Vision-aware Latent Steering to Mitigate Object Hallucinations](https://arxiv.org/pdf/2505.17812) | arXiv'25 | 2025.5.23 |
| [CGC: Image Tokens Matter: Mitigating Hallucination in Discrete Tokenizer-based Large Vision-Language Models via Latent Editing](https://arxiv.org/pdf/2505.21547) | arXiv'25 | 2025.5.24 |
| [EVRB: Enhancing Visual Reliance in Text Generation: A Bayesian Perspective on Mitigating Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2505.19498) | arXiv'25 | 2025.5.26 |
| [C-PMI: Grounding Language with Vision: A Conditional Mutual Information Calibrated Decoding Strategy for Reducing Hallucinations in LVLMs](https://arxiv.org/pdf/2505.19678) | arXiv'25 | 2025.5.26 |
| [CAAC: Mitigating Hallucination in Large Vision-Language Models via Adaptive Attention Calibration](https://arxiv.org/pdf/2505.21472) | arXiv'25 | 2025.5.27 |
| [RVCD: Retrieval Visual Contrastive Decoding to Mitigate Object Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2505.20569) | arXiv'25 | 2025.5.29 |
| [BIMA: Bijective Maximum Likelihood Learning Approach to Hallucination Prediction and Mitigation in Large Vision-Language Models](https://arxiv.org/pdf/2505.24649) | arXiv'25 | 2025.5.30 |
| [CLAIM: Mitigating Multilingual Object Hallucination in Large Vision-Language Models with Cross-Lingual Attention Intervention](https://arxiv.org/pdf/2506.11073) | arXiv'25 | 2025.6.3 |
| [EMPO: Mitigating Hallucinations in Large Vision-Language Models via Entity-Centric Multimodal Preference Optimization](https://arxiv.org/pdf/2506.04039) | arXiv'25 | 2025.6.4 |
| [When Semantics Mislead Vision: Mitigating Large Multimodal Models Hallucinations in Scene Text Spotting and Understanding](https://arxiv.org/pdf/2506.05551) | arXiv'25 | 2025.6.5 |
| [LPS: Mitigating Object Hallucination via Robust Local Perception Search](https://arxiv.org/pdf/2506.06729) | arXiv'25 | 2025.6.7 |
| [Seeing Far and Clearly: Mitigating Hallucinations in MLLMs with Attention Causal Decoding](https://arxiv.org/pdf/2505.16652) | arXiv'25 | 2025.6.7 |
| [SHE: Mitigating Behavioral Hallucination in Multimodal Large Language Models for Sequential Images](https://arxiv.org/pdf/2506.07184) | arXiv'25 | 2025.6.8 |
| [SECOND: Mitigating Perceptual Hallucination in Vision-Language Models via Selective and Contrastive Decoding](https://arxiv.org/pdf/2506.08391) | arXiv'25 | 2025.6.10 |
| [MoD: Mixture of Decoding: An Attention-Inspired Adaptive Decoding Strategy to Mitigate Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2505.17061) | **ACL'25** | 2025.6.10 |
| [ReVisiT: Revisit What You See: Disclose Language Prior in Vision Tokens for Efficient Guided Decoding of LVLMs](https://arxiv.org/pdf/2506.09522) | arXiv'25 | 2025.6.11 |
| [HalLoc: Token-level Localization of Hallucinations for Vision Language Models](https://arxiv.org/pdf/2506.10286) | arXiv'25 | 2025.6.12 |
| [TL-DPO: Stop learning it all to mitigate visual hallucination, Focus on the hallucination target.](https://arxiv.org/pdf/2506.11417) | arXiv'25 | 2025.6.13 |
| [TAI & HAI: Not All Tokens and Heads Are Equally Important: Dual-Level Attention Intervention for Hallucination Mitigation](https://arxiv.org/pdf/2506.12609) | arXiv'25 | 2025.6.14 |
| [ASCD: Attention-Steerable Contrastive Decoding for Reducing Hallucination in MLLM](https://arxiv.org/pdf/2506.14766) | arXiv'25 | 2025.6.17 |
| [HalluRNN: Mitigating Hallucinations via Recurrent Cross-Layer Reasoning in Large Vision-Language Models](https://arxiv.org/pdf/2506.17587) | arXiv'25 | 2025.6.21 |
| [MDSAM: Memory-Driven Sparse Attention Matrix for LVLMs Hallucination Mitigation](https://arxiv.org/pdf/2506.17664) | arXiv'25 | 2025.6.21 |
| [PostAlign: Multimodal Grounding as a Corrective Lens for MLLMs](https://arxiv.org/pdf/2506.17901) | arXiv'25 | 2025.6.22 |
| [GRPO: Seeing is Believing? Mitigating OCR Hallucinations in Multimodal Large Language Models](https://arxiv.org/pdf/2506.20168) | arXiv'25 | 2025.6.25 |
| [DLC: Mitigating Hallucination of Large Vision-Language Models via Dynamic Logits Calibration](https://arxiv.org/pdf/2506.21509) | arXiv'25 | 2025.6.26 |
| [ReCo: Reminder Composition Mitigates Hallucinations in Vision-Language Models](https://arxiv.org/pdf/2506.22636) | arXiv'25 | 2025.6.27 |
| [Preemptive Hallucination Reduction: An Input-Level Approach for Multimodal Language Model](https://arxiv.org/pdf/2506.22636) | arXiv'25 | 2025.6.27 |
| [CAI: Caption-Sensitive Attention Intervention for Mitigating Object Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2506.23590) | arXiv'25 | 2025.6.30 |
| [ONLY: One-Layer Intervention Sufficiently Mitigates Hallucinations in Large Vision-Language Models](http://arxiv.org/pdf/2507.00898) | arXiv'25 | 2025.7.1 |
| [SEED: Identify, Isolate, and Purge: Mitigating Hallucinations in LVLMs via Self-Evolving Distillation](https://arxiv.org/pdf/2507.04680) | arXiv'25 | 2025.7.7 |
| [ReLoop: "Seeing Twice and Thinking Backwards" via Closed-loop Training to Mitigate Hallucinations in Multimodal understanding](https://arxiv.org/pdf/2507.04943) | arXiv'25 | 2025.7.7 |
| [Energy-Guided Decoding for Object Hallucination Mitigation](https://arxiv.org/pdf/2507.07731) | arXiv'25 | 2025.7.10 |
| [SENTINEL: Mitigating Object Hallucinations via Sentence-Level Early Intervention](https://arxiv.org/pdf/2507.12455) | **ICCV'25** | 2025.7.16 |
| [EVA: Extracting Visual Facts from Intermediate Layers for Mitigating Hallucinations in Multimodal Large Language Models](https://arxiv.org/pdf/2507.15652) | arXiv'25 | 2025.7.21 |
| [INTER: Mitigating Hallucination in Large Vision-Language Models by Interaction Guidance Sampling](https://arxiv.org/pdf/2507.05056) | arXiv'25 | 2025.7.22 |
| [MCA-LLaVA: Manhattan Causal Attention for Reducing Hallucination in Large Vision-Language Models](https://arxiv.org/pdf/2507.09184) | **ACMMM'25** | 2025.7.23 |
| [LISA: A Layer-wise Integration and Suppression Approach for Hallucination Mitigation in Multimodal Large Language Models](https://arxiv.org/pdf/2507.19110) | arXiv'25 | 2025.7.25 |
| [SENITEL: Mitigating Object Hallucinations via Sentence-Level Early Intervention](http://arxiv.org/pdf/2507.12455) | arXiv'25 | 2025.7.26 |
| [ViHallu: See Different, Think Better: Visual Variations Mitigating Hallucinations in LVLMs](https://arxiv.org/pdf/2507.22003) | arXiv'25 | 2025.7.30 |
| [MAP: Mitigating Hallucinations in Large Vision-Language Models with Map-Level Attention Processing](https://arxiv.org/pdf/2508.01653) | arXiv'25 | 2025.8.3 |
| [Prompt-in-Image: Cure or Poison? Embedding Instructions Visually Alters Hallucination in Vision-Language Models](https://arxiv.org/pdf/2508.01678) | arXiv'25 | 2025.8.3 |
| [Modality Bias in LVLMs: Analyzing and Mitigating Object Hallucination via Attention Lens](https://arxiv.org/pdf/2508.02419) | arXiv'25 | 2025.8.4 |
| [SAVER: Mitigating Hallucinations in Large Vision-Language Models via Style-Aware Visual Early Revision](https://arxiv.org/pdf/2508.03177) | arXiv'25 | 2025.8.5 |
| [IKOD: Mitigating Visual Attention Degradation in Large Vision-Language Models](https://arxiv.org/pdf/2508.03469) | arXiv'25 | 2025.8.5 |
| [Hacking Hallucinations of MLLMs with Causal Sufficiency and Necessity](https://arxiv.org/pdf/2508.04182) | arXiv'25 | 2025.8.6 |
| [Obliviate: Analyzing and Mitigating Object Hallucination: A Training Bias Perspective](https://arxiv.org/pdf/2508.04567) | arXiv'25 | 2025.8.6 |
| [TARS: MinMax Token-Adaptive Preference Strategy for MLLM Hallucination Reduction](https://arxiv.org/pdf/2507.21584) | arXiv'25 | 2025.8.9 |
| [MRFD: Multi-Region Fusion Decoding with Self-Consistency for Mitigating Hallucinations in LVLMs](https://arxiv.org/pdf/2508.10264) | arXiv'25 | 2025.8.14 |
| [MRGD: Controlling Multimodal LLMs via Reward-guided Decoding](https://arxiv.org/pdf/2508.11616) | arXiv'25 | 2025.8.15 |
| [CHAIR-DPO: Mitigating Hallucinations in Multimodal LLMs via Object-aware Preference Optimization](https://arxiv.org/pdf/2508.20181) | arXiv'25 | 2025.8.27 |
| [VPFC: Two Causes, Not One: Rethinking Omission and Fabrication Hallucinations in MLLMs](https://arxiv.org/pdf/2509.00371) | arXiv'25 | 2025.8.30 |
| [D-LEAF: Localizing and Correcting Hallucinations in Multimodal LLMs via Layer-to-head Attention Diagnostics](https://arxiv.org/pdf/2509.07864) | arXiv'25 | 2025.9.9 |
| [APASI: Mitigating Hallucinations in Large Vision-Language Models by Self-Injecting Hallucinations](https://arxiv.org/pdf/2509.11287) | arXiv'25 | 2025.9.14 |
| [VisionWeaver: Diving into Mitigating Hallucinations from a Vision Perspective for Large Vision-Language Models](https://arxiv.org/pdf/2509.13836) | **EMNLP'25** | 2025.9.17 |
| [Exposing Hallucinations To Suppress Them: VLMs Representation Editing With Generative Anchors](https://arxiv.org/pdf/2509.21997) | arXiv'25 | 2025.9.26 |
| [Self-Consistency as a Free Lunch: Reducing Hallucinations in Vision-Language Models via Self-Reflection](https://arxiv.org/pdf/2509.23236) | arXiv'25 | 2025.9.27 |
| [SCPO: Mitigating Visual Hallucinations via Semantic Curriculum Preference Optimization in MLLMs](https://arxiv.org/pdf/2509.24491) | arXiv'25 | 2025.9.29 |
| [LayerCD: Mitigating Hallucination in Multimodal LLMs with Layer Contrastive Decoding](https://arxiv.org/pdf/2509.25177) | arXiv'25 | 2025.9.29 |
| [GACD: Mitigating Multimodal Hallucinations via Gradient-based Self-Reflection](https://arxiv.org/pdf/2509.03113) | arXiv'25 | 2025.10.1 |
| [MaskCD: Mitigating LVLM Hallucinations by Image Head Masked Contrastive Decoding](https://arxiv.org/pdf/2510.02790v1) | arXiv'25 | 2025.10.3 |
| [ChainMPQ: Interleaved Text-Image Reasoning Chains for Mitigating Relation Hallucinations](https://arxiv.org/pdf/2510.06292v1) | arXiv'25 | 2025.10.7 |
| [On Epistemic Uncertainty of Visual Tokens for Object Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2510.09008v1) | arXiv'25 | 2025.10.10 |
| [Hallu-Steer: Steering Multimodal LLMs Away from Hallucinations via Latent Intervention](https://arxiv.org/pdf/2510.11842v1) | arXiv'25 | 2025.10.13 |
| [Mitigating Hallucination in Multimodal Reasoning via Functional Attention Control](https://arxiv.org/pdf/2510.10285v1) | arXiv'25 | 2025.10.11 |
| [When Images Speak Louder: Mitigating Language Bias-induced Hallucinations in VLMs through Cross-Modal Guidance](https://arxiv.org/pdf/2510.10466v1) | arXiv'25 | 2025.10.12 |
| [Vision Language Models Map Logos to Text via Semantic Entanglement in the Visual Projector](https://arxiv.org/pdf/2510.12287v1) | arXiv'25 | 2025.10.14 |
| [Self-Augmented Visual Contrastive Decoding](https://arxiv.org/pdf/2510.13315v1) | arXiv'25 | 2025.10.15 |
| [Watermarking for Factuality: Guiding Vision-Language Models Toward Truth via Tri-layer Contrastive Decoding](https://arxiv.org/pdf/2510.14304v1) | arXiv'25 | 2025.10.16 |
| [Suppressing Hallucinations In LVLM Encoders via Bias and Vulnerability Defense](https://arxiv.org/pdf/2510.16596v1) | arXiv'25 | 2025.10.18 |
| [Token-Level Inference-Time Alignment for Vision-Language Models](https://arxiv.org/pdf/2510.21794) | arXiv'25 | 2025.10.20 |
| [Beyond Single Models: Mitigating Multimodal Hallucinations via Adaptive Token Ensemble Decoding](https://arxiv.org/pdf/2510.18321v1) | arXiv'25 | 2025.10.21 |
| [PruneHal: Reducing Hallucinations in Multi-modal Large Language Models through Adaptive KV Cache Pruning](https://arxiv.org/pdf/2510.19183v1) | arXiv'25 | 2025.10.22 |
| [Why LVLMs Are More Prone to Hallucinations in Longer Responses: The Role of Context](https://arxiv.org/pdf/2510.20229v1) | arXiv'25 | 2025.10.23 |
| [Generating Accurate and Detailed Captions for High-Resolution Images](https://arxiv.org/pdf/2510.27164v1) | arXiv'25 | 2025.10.31 |
| [Towards Mitigating Hallucinations in Large Vision-Language Models by Refining Textual Embeddings](https://arxiv.org/pdf/2511.05017v1) | arXiv'25 | 2025.11.07 |
| [Causal Tracing of Object Representations in Large Vision Language Models: Mechanistic Interpretability and Hallucination Mitigation](https://arxiv.org/pdf/2511.05923v3) | arXiv'25 | 2025.11.08 |
| [Capturing Gaze Shifts for Guidance: Cross-Modal Fusion Enhancement for VLM Hallucination Mitigation](https://arxiv.org/pdf/2510.22067) | arXiv'25 | 2025.11.10 |
| [Causally-Grounded Dual-Path Attention Intervention for Object Hallucination Mitigation in LVLMs](https://arxiv.org/pdf/2511.09018v1) | arXiv'25 | 2025.11.12 |
| [Taming Object Hallucinations with Verified Atomic Confidence Estimation](https://arxiv.org/pdf/2511.09228v1) | arXiv'25 | 2025.11.12 |
| [Adaptive Residual-Update Steering for Low-Overhead Hallucination Mitigation in Large Vision Language Models](https://arxiv.org/pdf/2511.10292v1) | arXiv'25 | 2025.11.13 |
| [Suppressing VLM Hallucinations with Spectral Representation Filtering](https://arxiv.org/pdf/2511.12220v1) | arXiv'25 | 2025.11.15 |
| [Unified Mitigation of LVLM Hallucinations across Alignment Formats](https://arxiv.org/pdf/2511.17254v2) | arXiv'25 | 2025.11.21 |
| [Attention Guided Alignment in Efficient Vision-Language Models](https://arxiv.org/pdf/2511.17793v1) | arXiv'25 | 2025.11.21 |
| [Tell Model Where to Look: Mitigating Hallucinations in MLLMs by Vision-Guided Attention](https://arxiv.org/pdf/2511.20032v1) | arXiv'25 | 2025.11.25 |
| [Optimizing LVLMs with On-Policy Data for Effective Hallucination Mitigation](https://arxiv.org/pdf/2512.00706v1) | arXiv'25 | 2025.11.30 |
| [Hallucination Mitigation via Introspection and Cross-Modal Multi-Agent Collaboration](https://arxiv.org/pdf/2512.02981v1) | arXiv'25 | 2025.12.02 |
| [Mitigating Hallucinations in Multimodal Large Language Models via Visual Inference-Time Intervention](https://arxiv.org/pdf/2512.03542v1) | arXiv'25 | 2025.12.03 |
| [Mitigating Object and Action Hallucinations in Multimodal LLMs via Self-Augmented Contrastive Alignment](https://arxiv.org/pdf/2512.04356v1) | arXiv'25 | 2025.12.04 |
| [Conscious Gaze: Adaptive Attention Mechanisms for Hallucination Mitigation in Vision-Language Models](https://arxiv.org/pdf/2512.05546v1) | arXiv'25 | 2025.12.05 |
| [Toward More Reliable Artificial Intelligence: Reducing Hallucinations in Vision-Language Models](https://arxiv.org/pdf/2512.07564v1) | arXiv'25 | 2025.12.08 |
| [Sparse Autoencoder-Driven Visual Information Enhancement for Mitigating Object Hallucination](https://arxiv.org/pdf/2512.07730v2) | arXiv'25 | 2025.12.08 |
| [VEGAS: Mitigating Hallucinations in Large Vision-Language Models via Vision-Encoder Attention Guided Adaptive Steering](https://arxiv.org/pdf/2512.12089v1) | arXiv'25 | 2025.12.12 |
| [Revealing Perception and Generation Dynamics in LVLMs: Mitigating Hallucinations via Validated Dominance Correction](https://arxiv.org/pdf/2512.18813v1) | arXiv'25 | 2025.12.21 |
| [Watch Closely: Mitigating Object Hallucinations in Large Vision-Language Models with Disentangled Decoding](https://arxiv.org/pdf/2512.19070v1) | arXiv'25 | 2025.12.22 |
| [Look Closer! An Adversarial Parametric Editing Framework for Hallucination Mitigation in VLMs](https://arxiv.org/pdf/2512.21999v1) | arXiv'25 | 2025.12.26 |
| [CoFi-Dec: Hallucination-Resistant Decoding via Coarse-to-Fine Generative Feedback in Large Vision-Language Models](https://arxiv.org/pdf/2512.23453v1) | arXiv'25 | 2025.12.29 |
| [Cost-efficient Difficulty-aware Preference Optimization for Reducing MLLM Hallucinations](https://arxiv.org/pdf/2601.00623v1) | arXiv'26 | 2026.01.02 |
| [A Training-Free Hallucination Mitigation Framework for Vision-Language Models](https://arxiv.org/pdf/2601.00659v1) | arXiv'26 | 2026.01.02 |
| [Mitigating the Object Hallucination of LVLM via Adaptive Factual-Guided Activation Editing](https://arxiv.org/pdf/2601.01957v1) | arXiv'26 | 2026.01.05 |
| [Text-Guided Layer Fusion Mitigates Hallucination in Multimodal LLMs](https://arxiv.org/pdf/2601.03100v1) | arXiv'26 | 2026.01.06 |
| [Structure-Disrupted Contrastive Decoding for Mitigating Hallucinations in Large Vision-Language Models](https://arxiv.org/pdf/2601.03500v1) | arXiv'26 | 2026.01.07 |
| [Vision-Language Introspection: Mitigating Overconfident Hallucinations in MLLMs via Interpretable Bi-Causal Steering](https://arxiv.org/pdf/2601.05159v1) | arXiv'26 | 2026.01.08 |
| [VIB-Probe: Detecting and Mitigating Hallucinations in Vision-Language Models via Variational Information Bottleneck](https://arxiv.org/pdf/2601.05547v1) | arXiv'26 | 2026.01.09 |
| [Ground What You See: Hallucination-Resistant MLLMs via Caption Feedback, Diversity-Aware Sampling, and Conflict Regularization](https://arxiv.org/pdf/2601.06224) | arXiv'26 | 2026.01.09 |
| [Context-Aware Decoding for Faithful Vision-Language Generation](https://arxiv.org/pdf/2601.05939v1) | arXiv'26 | 2026.01.09 |
| [Attention-space Contrastive Guidance for Efficient Hallucination Mitigation in LVLMs](https://arxiv.org/pdf/2601.13707v1) | arXiv'26 | 2026.01.20 |
| [Beyond Superficial Unlearning: Sharpness-Aware Robust Erasure of Hallucinations in Multimodal LLMs](https://arxiv.org/pdf/2601.16527v1) | arXiv'26 | 2026.01.23 |
| [Hallucination Begins Where Saliency Drops](https://arxiv.org/pdf/2601.20279v1) | arXiv'26 | 2026.01.28 |
| [Countering the Over-Reliance Trap: Mitigating Object Hallucination for LVLMs via a Self-Validation Framework](https://arxiv.org/pdf/2601.22451v1) | arXiv'26 | 2026.01.30 |
| [One-shot Optimized Steering Vector for Hallucination Mitigation for VLMs](https://arxiv.org/pdf/2601.23041v1) | arXiv'26 | 2026.01.30 |
| [Towards Interpretable Hallucination Analysis and Mitigation in LVLMs via Contrastive Neuron Steering](https://arxiv.org/pdf/2602.00621v1) | arXiv'26 | 2026.01.31 |
| [Residual Decoding: Mitigating Hallucinations in Large Vision-Language Models via History-Aware Residual Guidance](https://arxiv.org/pdf/2602.01047v1) | arXiv'26 | 2026.02.01 |
| [Model-Aware Contrastive Decoding via Counterfactual Data](https://arxiv.org/pdf/2602.01740v1) | arXiv'26 | 2026.02.02 |
| [KVSmooth: Mitigating Hallucination in Multi-modal Large Language Models through Key-Value Smoothing](https://arxiv.org/pdf/2602.04268v1) | arXiv'26 | 2026.02.04 |

---

## Evaluation_Benchmark

| Benchmark | Pub | Date | Size | Task | Metric | Object | Attribute | Relation | Other | LLM Free | Human Annotation Free |
|-----------|-----|------|------|------|--------|--------|-----------|----------|-------|----------|------------------------|
| [CHAIR](https://arxiv.org/abs/1809.02156) | EMNLP'18 | 2018.09 | 5,000 | Gen | CHAIR | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ |
| [POPE](https://arxiv.org/pdf/2305.10355.pdf) | EMNLP'23 | 2023.05 | 3,000 | Dis | Acc/P/R/F1 | ✅ | ❌ | ❌ | ❌ | ✅ | ✅ |
| [MME](https://arxiv.org/pdf/2306.13394.pdf) | NeurIPS’25 | 2023.06.23 | 1,457 | Dis | Acc/Score | ✅ | ✅ | ❌ | ❌ | ✅ | ❌ |
| [M-HalDetect](https://arxiv.org/pdf/2308.06394.pdf) | AAAI'24 | 2023.08 | 16,000 | Dis | Reward Score | ✅ | ✅ | ✅ | Fine-grained | ❌ | ❌ |
| [CIEM](https://arxiv.org/pdf/2309.02301.pdf) | NeurIPS-W'23| 2023.09 | 40,367 | Dis | Acc/P/R/F1/Specificity | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ |
| [HaELM](https://arxiv.org/pdf/2308.15126.pdf) | arXiv'23 | 2023.10.10 | 25,000 | Gen | LLM Rating | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| [MMHal-Bench](https://arxiv.org/pdf/2309.14525.pdf) | ACL'24 | 2023.09.25 | 96 | Gen | LLM Rating | ✅ | ❌ | ❌ | Model Bias | ❌ | ✅ |
| [GAVIE](https://arxiv.org/pdf/2306.14565.pdf) | ICLR'24 | 2023.09.29 | 1,000 | Gen | LLM Rating | ✅ | ✅ | ✅ | Env/Action/Comp | ❌ | ✅ |
| [NOPE](https://arxiv.org/pdf/2310.05338.pdf) | ACL-W'24 | 2023.10.09 | 29,500 | Dis | Acc/METEOR | ✅ | ❌ | ❌ | Negative Pronoun | ❌ | ✅ |
| [FAITHSCORE](https://arxiv.org/pdf/2311.01477.pdf) | EMNLP'24 | 2023.11.02 | 2,000 | Gen | FaithScore | ✅ | ✅ | ✅ | Obj. Counting | ❌ | ❌ |
| [AMBER](https://arxiv.org/pdf/2311.07397.pdf) | arXiv'23 | 2023.11.13 | 15,202 | Dis & Gen | AMBER Score | ✅ | ✅ | ✅ | ❌ | ✅ | ❌ |
| [Bingo](https://arxiv.org/pdf/2311.03287.pdf) | arXiv'23 | 2023.11.07 | 370 | Gen | Human Assessment | ❌ | ❌ | ❌ | Model Bias | ✅ | ❌ |
| [HallusionBench](https://arxiv.org/pdf/2310.14566.pdf) | CVPR'24 | 2023.11.28 | 1,129 | Gen | LLM Rating | ❌ | ❌ | ❌ | Visual Illusion | ✅ | ❌ |
| [RAH-Bench](https://arxiv.org/pdf/2311.16479.pdf) | arXiv'23 | 2023.11.27 | 3,000 | Dis | False Positive Rate | ✅ | ✅ | ✅ | ❌ | ❌ | ✅ |
| [CCeval](https://arxiv.org/pdf/2310.01779.pdf) | arXiv'23 | 2023.12.03 | 100 | Gen | CHAIR/Coverage | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| [MERLIM](https://arxiv.org/pdf/2312.02219.pdf) | CVPR'25 | 2023.12.03 | 31,373 | Dis | Accuracy | ✅ | ❌ | ✅ | Visual Grounding | ✅ | ❌ |
| [FGHE](https://arxiv.org/pdf/2312.01701.pdf) | MMM'24 | 2023.12.04 | 200 | Dis | Acc/P/R/F | ✅ | ✅ | ✅ | Behaviour | ❌ | ❌ |
| [OpenCHAIR](https://arxiv.org/pdf/2312.03631.pdf) | EMNLP'24 | 2023.12.06 | 2,000 | Gen | OpenCHAIR | ✅ | ✅ | ❌ | Open-Vocabulary | ❌ | ✅ |
| [CorrelationQA](https://arxiv.org/pdf/2402.03757.pdf) | arXiv'24 | 2024.02.06 | 7,308 | Dis | Acc | ✅ | ❌ | ❌ | Spurious Images | ❌ | ✅ |
| [ViGoR](https://arxiv.org/pdf/2402.06118.pdf) | arXiv'24 | 2024.02.09 | 16,000 | Gen | Fine-Grained Reward| ✅ | ✅ | ✅ | Grounding | ❌ | ❌ |
| [VQAv2-IDK](https://arxiv.org/pdf/2402.09717.pdf) | ICASSP'24 | 2024.02.15 | 6,624 | Dis | Acc | ❌ | ❌ | ❌ | IDK (IK) | ✅ | ❌ |
| [MHaluBench](https://arxiv.org/pdf/2402.03190.pdf) | ACL'24 | 2024.02.20 | 1,860 | Gen | Acc/P/R/F | ✅ | ✅ | ❌ | T2I | ✅ | ✅ |
| [MAD-Bench](https://arxiv.org/pdf/2402.13220.pdf) | arXiv'24 | 2024.02.20 | 1,000 | Gen | Acc | ✅ | ✅ | ❌ | Deceptive Prompts | ✅ | ✅ |
| [VHTest](https://arxiv.org/pdf/2402.14683v1.pdf) | ACL'24 | 2024.02.22 | 1,200 | Dis & Gen | Acc | ✅ | ✅ | ❌ | Visual Hallucination | ❌ | ❌ |
| [Hal-Eval](https://arxiv.org/pdf/2402.15721.pdf) | ACMMM'24 | 2024.02.24 | 10,000 | Dis & Gen | Acc/Score | ✅ | ✅ | ✅ | Event Hallucination | ✅ | ❌ |
| [Number Hallucinations](https://arxiv.org/pdf/2403.01373.pdf) | arXiv'24 | 2024.03.03 | 20,000 | Dis | Acc / Consistency | ✅ | ✅ | ❌ | Object Counting | ❌ | ✅ |
| [EvalDial](https://arxiv.org/pdf/2403.10492.pdf) | arXiv'24 | 2024.03.15 | N/A | Dis & Gen| Acc | ✅ | ✅ | ❌ | Dialogue Hallucination| ❌ | ✅ |
| [PHD](https://arxiv.org/pdf/2403.11116.pdf) | CVPR'25 | 2024.03.17 | 102,564 | Dis | PhD Index | ✅ | ✅ | ✅ | Sentiment | ❌ | ❌ |
| [MM-UPD](https://arxiv.org/pdf/2403.20331) | arXiv'24 | 2024.03.29 | 2,095 | Dis | Acc | ❌ | ❌ | ❌ | Unsolvable (UPD) | ❌ | ❌ |
| [ALOHa](https://arxiv.org/pdf/2404.02904v1.pdf) | arXiv'24 | 2024.04.03 | N/A | Gen | ALOHa | ✅ | ❌ | ❌ | Captioning Metric | ❌ | ❌ |
| [VALOR-EVAL](https://arxiv.org/pdf/2404.13874) | ACL'24 | 2024.04.22 | 211 | Gen | Faithfulness & Coverage | ✅ | ✅ | ✅ | ❌ | ❌ | ❌ |
| [THRONE](https://arxiv.org/pdf/2405.05256) | CVPR'24 | 2024.05.08 | 5,000 | Gen | P/R/F | ✅ | ❌ | ❌ | Free-form Generations | ❌ | ✅ |
| [MRHal-Bench](https://arxiv.org/pdf/2405.11165) | NeurIPS'24 | 2024.05.18 | N/A | Gen | Preference Score | ✅ | ✅ | ❌ | Multi-round Conv | ❌ | ✅ |
| [VLind-Bench](https://arxiv.org/pdf/2406.08702) | arXiv'24 | 2024.06.13 | 2,576 | Dis | Acc (Y/N) | ✅ | ❌ | ❌ | Language Priors | ❌ | ✅ |
| [MMRel](https://arxiv.org/pdf/2406.09121) | arXiv'24 | 2024.06.13 | 22,500 | Dis & Gen | Acc | ✅ | ❌ | ✅ | Relation Understanding| ❌ | ❌ |
| [Med-HallMark](https://arxiv.org/pdf/2406.10185) | arXiv'24 | 2024.06.14 | 889,125 | Dis & Gen | MediHall Score | ✅ | ✅ | ❌ | Medical Context | ❌ | ✅ |
| [AutoHallusion](https://arxiv.org/pdf/2406.10900) | EMNLP'24 | 2024.06.16 | 5,000 | Dis | ASR/MASR/CASR | ✅ | ❌ | ❌ | ❌ | ❌ | ✅ |
| [MFC Bench](https://arxiv.org/pdf/2406.11288) | arXiv'24 | 2024.06.17 | 35,000 | Dis & Gen | Acc/F1 | ❌ | ❌ | ❌ | Manipulation/OOC/Veracity | ❌ | ❌ |
| [CHAIR-MEN](https://arxiv.org/pdf/2406.14492) | arXiv'24 | 2024.06.20 | N/A | Gen | CHAIR-MEN / FaithScore | ✅ | ❌ | ❌ | Metric Method | ✅ | ✅ |
| [HQHBench](https://arxiv.org/pdf/2406.17115) | arXiv'24 | 2024.06.24 | 4,000 | Dis & Gen | Hallucination Rate | ✅ | ✅ | ✅ | OCR/Action/Counting | ❌ | ✅ |
| [VideoHallucer](https://arxiv.org/pdf/2406.16338) | arXiv'24 | 2024.06.24 | 1,800 | Dis & Gen | Acc | ✅ | ❌ | ✅ | Temporal/Extrinsic | ❌ | ❌ |
| [R-Bench](https://arxiv.org/pdf/2406.16449) | ICML'24 | 2024.06.24 | 8,030 | Dis | Acc/P/R/F1 | ✅ | ❌ | ✅ | ❌ | ❌ | ❌ |
| [MMHalSnowball](https://arxiv.org/pdf/2407.00569) | arXiv'24 | 2024.06.30 | 4,973 | Dis | Acc | ✅ | ✅ | ❌ | Generated Distractions | ❌ | ✅ |
| [MedVH](https://arxiv.org/pdf/2407.02730) | arXiv'24 | 2024.07.03 | 2,000 | Dis & Gen | Characterization Score| ✅ | ✅ | ❌ | Medical Context | ❌ | ❌ |
| [ROPE](https://arxiv.org/abs/2407.06192) | NeurIPS'24 | 2024.07.08 | 5,000 | Gen | Accuracy | ✅ | ✅ | ✅ | Multi-Object | ✅ | ✅ |
| [BEAF](https://arxiv.org/pdf/2407.13442) | ECCV'24 | 2024.07.18 | 26,064 | Dis | TU/IG/SB/ID | ✅ | ❌ | ❌ | Before-After Changes | ❌ | ✅ |
| [HaloQuest](https://arxiv.org/pdf/2407.15680) | ECCV'24 | 2024.07.22 | 7,748 | Gen | Acc | ✅ | ❌ | ❌ | Synthetic Images / VQA | ❌ | ❌ |
| [MMINSTRUCT](https://arxiv.org/pdf/2407.15838) | arXiv'24 | 2024.07.22 | 973,000 | Gen | Acc | ✅ | ✅ | ✅ | Instruction Tuning | ❌ | ❌ |
| [Hallu-PI](https://arxiv.org/pdf/2408.01355) | arXiv'24 | 2024.08.02 | 1,260 | Dis | Acc | ✅ | ✅ | ✅ | Perturbed Inputs | ❌ | ✅ |
| [Reefknot](https://arxiv.org/pdf/2408.09429) | ACL'25 | 2024.08.18 | 21,880 | Dis & Gen | R-score | ❌ | ❌ | ✅ | Perceptive / Cognitive | ❌ | ✅ |
| [Pfram](https://arxiv.org/pdf/2409.01151) | arXiv'24 | 2024.09.02 | N/A | Dis | Pfram | ✅ | ❌ | ❌ | Alignment Method | ✅ | ✅ |
| [ODE](https://arxiv.org/abs/2409.09318) | CVPR'25 | 2024.09.14 | 8,786 | Dis & Gen | AMBER/Acc | ✅ | ✅ | ❌ | Open-Set | ✅ | ❌ |
| [LLSAVisionQA](https://arxiv.org/pdf/2409.09748) | arXiv'24 | 2024.09.15 | 4,989 | Gen | Acc | ❌ | ✅ | ❌ | Low-level Perception | ❌ | ❌ |
| [CAST](https://arxiv.org/pdf/2409.11007) | arXiv'24 | 2024.09.17 | 15,000 | Dis & Gen | Similarity | ✅ | ✅ | ✅ | Self-consistency | ❌ | ✅ |
| [FIHA](https://arxiv.org/pdf/2409.13612) | arXiv'24 | 2024.09.20 | N/A | Dis & Gen | Acc/P/R/F1 | ✅ | ✅ | ✅ | Eval Method | ✅ | ✅ |
| [EventHallusion](https://arxiv.org/pdf/2409.16597) | arXiv'24 | 2024.09.25 | 711 | Dis & Gen | Accuracy | ❌ | ❌ | ❌ | Video Event | ❌ | ❌ |
| [JourneyBench](https://arxiv.org/pdf/2409.12953) | arXiv'24 | 2024.09.25 | 13,500 | Dis & Gen | Acc | ✅ | ✅ | ❌ | Imaginary VQA | ❌ | ❌ |
| [TUBench](https://arxiv.org/pdf/2410.04107) | arXiv'24 | 2024.10.05 | 2,354 | Dis | Acc | ✅ | ❌ | ✅ | Unanswerable Qs | ❌ | ❌ |
| [LongHallGen](https://arxiv.org/pdf/2410.09962) | arXiv'24 | 2024.10.13 | 6,485 | Dis & Gen | Accuracy | ✅ | ✅ | ❌ | Long Context | ❌ | ✅ |
| [MM-SY](https://arxiv.org/pdf/2410.11302) | arXiv'24 | 2024.10.15 | N/A | Dis | Sycophancy Rate | ✅ | ✅ | ✅ | Sycophancy Eval | ❌ | ✅ |
| [Magnifier Prompt](https://arxiv.org/pdf/2410.11701) | arXiv'24 | 2024.10.15 | N/A | Gen | Acc | ✅ | ❌ | ❌ | Prompt Method | ✅ | ✅ |
| [DeCo](https://arxiv.org/pdf/2410.11779) | arXiv'24 | 2024.10.15 | N/A | Gen | Acc | ✅ | ❌ | ❌ | Decoding Method | ✅ | ✅ |
| [CMM](https://arxiv.org/pdf/2410.12787) | arXiv'24 | 2024.10.16 | 2,400 | Dis | PA/HR | ❌ | ❌ | ❌ | Modality Dominance | ✅ | ❌ |
| [Trust but Verify](https://arxiv.org/pdf/2410.13121) | arXiv'24 | 2024.10.17 | 10,500 | Gen | hscore/tscore | ✅ | ✅ | ❌ | In the Wild Eval | ❌ | ✅ |
| [Tri-HE](https://arxiv.org/pdf/2410.23114) | arXiv'24 | 2024.11.03 | 1,920 | Dis | Acc | ✅ | ❌ | ✅ | Triplet-Level Eval | ❌ | ❌ |
| [H-POPE](https://arxiv.org/pdf/2411.04077) | arXiv'24 | 2024.11.06 | 1,920 | Dis | Acc/P/R/F1 | ✅ | ✅ | ❌ | Coarse-to-fine | ✅ | ❌ |
| [VIDHAL](https://arxiv.org/pdf/2411.16771) | arXiv'24 | 2024.11.25 | 1,000 | Dis | NDCG | ✅ | ✅ | ❌ | Video Action | ❌ | ❌ |
| [HALLUCINOGEN](https://arxiv.org/pdf/2412.20622) | arXiv'24 | 2024.12.29 | 90,000 | Dis & Gen | Acc | ✅ | ❌ | ❌ | Object Hallucination | ❌ | ✅ |
| [CAOS](https://arxiv.org/pdf/2501.15046) | arXiv'25 | 2025.01.25 | 2,000 | Gen | CAOS Score | ✅ | ❌ | ❌ | Object Similarities | ❌ | ✅ |
| [Mirage in the Eyes](https://arxiv.org/pdf/2501.15269) | arXiv'25 | 2025.01.25 | 1,000 | Dis | Acc / HR | ✅ | ✅ | ✅ | Attack/Attention Sink | ✅ | ✅ |
| [LanP](https://arxiv.org/pdf/2502.12359) | arXiv'25 | 2025.02.17 | 340 | Dis | Acc | ✅ | ❌ | ❌ | Language Priors | ❌ | ❌ |
| [MedHallTune](https://arxiv.org/pdf/2502.20780) | arXiv'25 | 2025.02.28 | 1,000,000 | Dis & Gen | Acc | ✅ | ✅ | ❌ | Medical Context | ❌ | ✅ |
| [RePOPE](https://arxiv.org/pdf/2504.15707) | arXiv'25 | 2025.04.22 | 3,000 | Dis | Acc/F1 | ✅ | ❌ | ❌ | Annotation Errors | ✅ | ❌ |
| [Antidote](https://arxiv.org/pdf/2504.20468) | CVPR'25 | 2025.05.07 | N/A | Gen | Acc | ✅ | ❌ | ❌ | CP-Bench Mitigation | ✅ | ✅ |
| [QAVisualGenome & QA-FB15k](https://arxiv.org/pdf/2505.01958) | arXiv'25 | 2025.05.04 | N/A | Dis & Gen | Acc | ✅ | ✅ | ✅ | Visual Object Eval | ❌ | ❌ |
| [Localizing Before Answering](https://arxiv.org/pdf/2505.00744) | arXiv'25 | 2025.05.05 | 67,000 | Gen | Acc / Loc | ✅ | ❌ | ❌ | Grounded Medical | ❌ | ❌ |
| [EmotionHallucer](https://arxiv.org/pdf/2505.11405) | arXiv'25 | 2025.05.16 | 2,742 | Dis | Acc | ❌ | ✅ | ❌ | Emotion Psychology | ❌ | ❌ |
| [MIRAGE](https://arxiv.org/pdf/2505.24238) | arXiv'25 | 2025.06.02 | 1,329 | Dis & Gen | Acc / Factuality | ❌ | ❌ | ✅ | Reasoning Chains | ❌ | ❌ |
| [MMMC](https://arxiv.org/pdf/2507.07151) | arXiv'25 | 2025.07.09 | 5,000 | Dis & Gen | Acc | ✅ | ✅ | ✅ | Modality Conflict | ❌ | ✅ |
| [LOTUS](https://arxiv.org/pdf/2507.19362) | arXiv'25 | 2025.07.25 | N/A | Dis | Alignment/Bias| ❌ | ❌ | ❌ | Societal Bias/Pref | ❌ | ❌ |
| [MIHBench](https://arxiv.org/pdf/2508.00726) | arXiv'25 | 2025.08.01 | 3,000 | Dis & Gen | Acc | ✅ | ❌ | ❌ | Multi-Image Reasoning | ❌ | ❌ |
| [HOPE](https://arxiv.org/pdf/2508.06530) | arXiv'25 | 2025.08.03 | N/A | Gen | Precision Drop| ✅ | ✅ | ❌ | Misleading Distractors | ❌ | ✅ |
| [SHALE](https://arxiv.org/pdf/2508.09584) | arXiv'25 | 2025.08.14 | 30,100 | Dis & Gen | Acc | ✅ | ✅ | ✅ | Fine-grained | ❌ | ✅ |
| [HUmbleBench](https://arxiv.org/pdf/2509.09658) | arXiv'25 | 2025.09.11 | 22,831 | Dis | Rejection Acc | ✅ | ✅ | ✅ | Epistemic Humility | ❌ | ✅ |
| [VHBench-10](https://arxiv.org/pdf/2509.13836) | arXiv'25 | 2025.09.17 | 10,000 | Dis | Acc | ✅ | ✅ | ✅ | Vision Perspective | ❌ | ❌ |
| [ChartHal](https://arxiv.org/pdf/2509.17481) | arXiv'25 | 2025.09.22 | 1,062 | Dis & Gen | Acc | ❌ | ❌ | ❌ | Chart Understanding | ❌ | ❌ |
| [ColorBlindnessEval](https://arxiv.org/pdf/2509.19070) | arXiv'25 | 2025.09.23 | 500 | Dis & Gen | Acc | ❌ | ✅ | ❌ | Color Blindness Tests | ✅ | ❌ |
| [Common-O Bench](https://arxiv.org/pdf/2511.03768v1) | arXiv'25 | 2025.11.05 | 10,500 | Dis & Gen | Acc | ✅ | ❌ | ✅ | Reasoning Across Scenes| ❌ | ❌ |
| [Causal-HalBench](https://arxiv.org/pdf/2511.10268v1) | arXiv'25 | 2025.11.13 | N/A | Gen | Acc | ✅ | ❌ | ❌ | Causal Intervention | ❌ | ✅ |
| [What Color Is It](https://arxiv.org/pdf/2511.13400v2) | arXiv'25 | 2025.11.17 | N/A | Dis | Acc | ❌ | ✅ | ❌ | Text-Interference | ❌ | ✅ |
| [MVI-Bench](https://arxiv.org/pdf/2511.14159v1) | arXiv'25 | 2025.11.18 | 1,248 | Dis & Gen | MVI-Sensitivity | ✅ | ✅ | ✅ | Misleading Visual | ❌ | ❌ |
| [PIH](https://arxiv.org/pdf/2601.05201v1) | arXiv'26 | 2026.01.08 | N/A | Gen | PIH Ablation | ✅ | ❌ | ❌ | Prompt-Induced | ✅ | ✅ |
| [CFHR](https://arxiv.org/pdf/2602.05437v1) | arXiv'26 | 2026.02.05 | N/A | Dis | CFHR | ❌ | ❌ | ❌ | Counterfactual | ❌ | ❌ |


| year | Method | Benchmark | summary | 
|------|--------|-----------|---------|
| 2023 | 11     | 11        | 28      | 
| 2024 | 89     | 43        | 139     | 
| 2025 | 144    | 22        | 167     | 
| 2026 | 18     | 2         | 20      | 
| summary | 262    | 79         | 355     |

