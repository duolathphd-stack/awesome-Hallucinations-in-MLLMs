# Awesome-MLLMs-Hallucination [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)



---
- [Awesome MLLMs Hallucination](#awesome-mllms-hallucination)
    - [Survey](#survey)
    - [Hallucination Mitigation](#hallucination-mitigation)
        - [Training & Alignment](#training--alignment)
        - [Decoding Strategies](#decoding-strategies)
        - [Attention & Architecture Intervention](#attention--architecture-intervention)
        - [External Augmentation & Prompting](#external-augmentation--prompting)
    - [Hallucination Benchmark](#hallucination-benchmark)


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


## Hallucination Mitigation 

### Training & Alignment
| Method | Pub | Date | 核心机制 (Methodology) |
| :--- | :--- | :--- | :--- |
| [ObjMLM](https://arxiv.org/pdf/2210.07688.pdf) | arXiv'23 | 2023.2.10 | **预训练**：提出了一种全新的视觉-语言预训练目标 (VLP objective) 来抑制幻觉。 |
| [MMCoT](https://arxiv.org/pdf/2302.00923.pdf) | arXiv'23 | 2023.2.17 | **微调**：采用两阶段微调框架，专门训练模型先生成 CoT 推理过程，再输出答案。 |
| [LRV-GAVIE](https://arxiv.org/pdf/2306.14565.pdf) | **ICLR'24** | 2023.6.26 | **指令微调**：构建了包含正负样本的 Robust 指令微调数据集并更新模型。 |
| [LLaVA-RLHF](https://arxiv.org/pdf/2309.14525.pdf) | **ACL'24** | 2023.9.25 | **强化学习**：引入事实增强机制，利用人类反馈强化学习来对齐模型。 |
| [VOLCANO](https://arxiv.org/pdf/2311.07362.pdf) | **NAACL'24** | 2023.11.14 | **微调**：专门训练 MLLM 生成自我反馈（Self-feedback），然后基于该反馈进行修改。 |
| [HalluciDoctor](https://arxiv.org/pdf/2311.13614.pdf) | **CVPR'24** | 2023.11.22 | **数据构造**：清理现有视觉指令数据集中的“幻觉毒性”，并生成反事实数据用于微调。 |
| [RAH-Bench](https://arxiv.org/pdf/2311.16479.pdf) | arXiv'23 | 2023.11.27 | **指令微调**：构建细粒度 RAI-30k 数据集，并在指令微调阶段融合了 SAM 模型。 |
| [HA-DPO](https://arxiv.org/pdf/2311.16839.pdf) | **ICME'24** | 2023.11.28 | **偏好优化**：构建幻觉感知的数据对，直接应用 DPO 算法更新模型权重。 |
| [FGHE](https://arxiv.org/pdf/2312.01701.pdf) | arXiv'23 | 2023.12.4 | **微调**：使用 ChatGPT 重写图像 Caption 构建数据，并进行两阶段微调。 |
| [RLHF-V](https://arxiv.org/pdf/2312.00849.pdf) | **CVPR'24** | 2023.12.1 | **强化学习**：收集细粒度的片段级人类纠正反馈，进行奖励模型训练和 PPO 优化。 |
| [MOCHa](https://arxiv.org/pdf/2312.03631.pdf) | arXiv'23 | 2023.12.6 | **强化学习**：训练一个基于自然语言推理 (NLI) 的奖励模型，并使用强化学习对 LVLM 进行微调。 |
| [HACL](https://arxiv.org/pdf/2312.06968.pdf) | arXiv'23 | 2023.12.12 | **对比学习**：在训练阶段引入幻觉增强的对比学习损失函数。 |
| [SILKIE](https://arxiv.org/pdf/2312.10665.pdf) | arXiv'23 | 2023.12.17 | **偏好蒸馏**：使用 AI 构建 VLFeedback 数据集，通过 DPO 算法将偏好蒸馏到模型中。 |
| [KAM-CoT](https://arxiv.org/pdf/2401.12863.pdf) | arXiv'24 | 2024.1.23 | **联合训练**：联合训练语言模型、视觉编码器和图神经网络 (GNN)，融入知识图谱进行推理。 |
| [ViGoR](https://arxiv.org/pdf/2402.06118.pdf) | **CVPR'24** | 2024.2.9 | **奖励建模**：训练细粒度的视觉奖励模型来引导模型实现更好的视觉对齐。 |
| [IDK-Instructions](https://arxiv.org/pdf/2402.09717.pdf) | **ACL'24** | 2024.2.15 | **指令微调**：通过专门的指令微调，教会模型在证据不足时主动输出“不知道”以拒绝回答。 |
| [EFUF](https://arxiv.org/pdf/2402.09801.pdf) | arXiv'24 | 2024.2.15 | **非学习**：提出一种高效的细粒度非学习 (Unlearning) 框架，通过反向更新参数来“遗忘”产生幻觉的倾向。 |
| [POVID](https://arxiv.org/pdf/2402.11411.pdf) | **NeurIPS'24** | 2024.2.18 | **偏好微调**：构建基于偏好的数据集，通过偏好微调促使模型向高质量图像描述对齐。 |
| [Less is More](https://arxiv.org/pdf/2402.14545.pdf) | **ACL'24** | 2024.2.22 | **指令微调**：重构微调数据集，让模型学会在产生幻觉之前尽早输出结束符 (EOS) 来截断生成。 |
| [AIT](https://arxiv.org/pdf/2403.10492.pdf) | **ACL'24** | 2024.3.15 | **指令微调**：引入对抗性指令微调，提高模型对具有误导性的用户提问的鲁棒性。 |
| [FGAIF](https://arxiv.org/pdf/2404.05046.pdf) | arXiv'24 | 2024.4.7 | **偏好优化**：利用细粒度的 AI 反馈构建偏好数据，并使用 DPO 进行对齐训练。 |
| [Prescribing the Right Remedy](https://arxiv.org/pdf/2404.10332.pdf) | arXiv'24 | 2024.4.16 | **微调**：针对不同的幻觉类型构建针对性的修复指令数据集，对模型进行靶向微调。 |
| [FACT](https://arxiv.org/pdf/2404.11129) | arXiv'24 | 2024.4.17 | **理性训练**：在训练时引入忠实且简明的推理基本原理 (Rationales) 作为监督信号，增强生成的逻辑性。 |
| [TextSquare](https://arxiv.org/pdf/2404.12803) | arXiv'24 | 2024.4.19 | **指令微调**：大规模扩展以文本为中心的视觉指令微调数据，专门解决模型在 OCR 任务上的文本幻觉。 |
| [HSA-DPO](https://arxiv.org/pdf/2404.14233) | arXiv'24 | 2024.4.22 | **偏好优化**：提出幻觉感知的直接偏好优化，利用细粒度 AI 反馈构建正负样本对更新权重。 |
| [CSR](https://arxiv.org/pdf/2405.14622) | **NeurIPS'24** | 2024.5.23 | **自我奖励学习**：提出自我校准奖励机制，让模型通过迭代式自我生成反馈并进行偏好对齐训练。 |
| [HIO](https://arxiv.org/pdf/2405.15356) | arXiv'24 | 2024.5.24 | **对比微调**：在训练阶段引入幻觉诱导机制构造正负样本对，进行优化以更新模型参数。 |
| [RLAIF-V](https://arxiv.org/pdf/2405.17220) | arXiv'24 | 2024.5.27 | **强化学习**：利用开源 AI 提供的细粒度反馈构建偏好数据集，并使用对齐算法更新模型权重。 |
| [HALVA](https://arxiv.org/pdf/2405.18654) | arXiv'24 | 2024.5.28 | **对比微调**：通过数据增强技术构造难负样本，并在微调阶段引入对比损失函数来强化视觉接地。 |
| [mDPO](https://arxiv.org/pdf/2406.11839) | arXiv'24 | 2024.6.17 | **偏好优化**：提出基于条件的偏好优化算法，在减少幻觉的同时防止模型在常规任务上的能力退化。 |
| [BDHS](https://arxiv.org/pdf/2407.02477) | arXiv'24 | 2024.7.2 | **基准与微调**：系统性构建涵盖多种对齐策略的数据集，通过实际微调验证不同对齐方案对幻觉的影响。 |
| [REVERIE](https://arxiv.org/pdf/2407.11422) | **ECCV'24** | 2024.7.16 | **指令微调**：构建反思性指令数据集，训练模型学会在输出最终答案前先进行内部的视觉事实核查。 |
| [MHR](https://arxiv.org/pdf/2408.00550) | arXiv'24 | 2024.8.1 | **指令微调**：专门针对多语言场景构建纠错指令微调数据集，以减轻由于语言偏差引起的多模态跨语言幻觉。 |
| [CLIP-DPO](https://arxiv.org/pdf/2408.10433) | arXiv'24 | 2024.8.19 | **偏好优化**：直接利用预训练的 CLIP 模型作为无需人工干预的“裁判”，生成偏好对进行 DPO 训练。 |
| [RoVRM](https://arxiv.org/pdf/2408.12109) | arXiv'24 | 2024.8.22 | **奖励建模**：在 RLHF 阶段，利用辅助的纯文本偏好数据优化视觉奖励模型，提升其对幻觉的判别力。 |
| [See or Guess](https://arxiv.org/pdf/2408.16809) | arXiv'24 | 2024.8.29 | **正则化训练**：在训练过程中引入反事实正则化项，强制模型区分真实看到的视觉内容和凭借语言先验猜测的内容。 |
| [FaithD2T](https://arxiv.org/pdf/2409.03961) | arXiv'24 | 2024.9.6 | **微调**：通过构建多模态事实一致性数据集并进行微调，以提高数据到文本生成的忠实度。 |
| [HELPD](https://arxiv.org/pdf/2409.20429) | arXiv'24 | 2024.9.30 | **反馈学习**：提出视觉增强惩罚解码结合层次化反馈学习的微调框架，在训练阶段对齐模型行为。 |
| [OHD-Caps](https://arxiv.org/pdf/2410.03176) | **EMNLP'24** | 2024.10.4 | **预训练干预**：通过清理并重写 CLIP 预训练数据中的标题，从源头减少视觉语言预训练阶段的物体幻觉。 |
| [Fine-Grained Verifiers](https://arxiv.org/pdf/2410.14148) | arXiv'24 | 2024.10.18 | **偏好建模**：将偏好建模转化为预测下一个 Token 的任务，通过细粒度验证器数据更新模型。 |
| [MFPO](https://arxiv.org/pdf/2410.15334) | arXiv'24 | 2024.10.20 | **偏好优化**：提出模态公平的偏好优化算法，在微调时平衡不同模态的惩罚以防止语言先验主导。 |
| [V-DPO](https://arxiv.org/pdf/2411.02712) | **EMNLP'24** | 2024.11.5 | **偏好优化**：利用视觉引导机制构建高质量的正负偏好数据对，直接对模型进行 DPO。 |
| [HDPO](https://arxiv.org/pdf/2411.10436) | arXiv'24 | 2024.11.15 | **偏好优化**：专门针对幻觉生成靶向偏好数据，通过 DPO 算法直接惩罚模型产生幻觉特征的倾向。 |
| [Verb Mirage](https://arxiv.org/pdf/2412.04939) | arXiv'24 | 2024.12.6 | **指令微调**：构建专门针对动词概念幻觉的数据集，通过针对性的指令微调纠正模型对动作理解的偏差。 |
| [TPO](https://arxiv.org/pdf/2412.14487) | arXiv'24 | 2024.12.19 | **偏好优化**：提出基于自校准视觉锚点奖励的 Token 级偏好优化策略，细粒度地更新模型权重。 |
| [SENA](https://arxiv.org/pdf/2412.15650) | arXiv'24 | 2024.12.20 | **自我进化学习**：通过迭代式的自我进化机制生成和筛选高质量对齐数据，实现无需人工标注的模型微调。 |
| [OPA-DPA](https://arxiv.org/search/cs?query=hallucination+vision+&searchtype=all&abstracts=show&order=-announced_date_first&size=50) | **CVPR'25** | 2025.1.16 | **偏好优化**：证明了策略内 (On-Policy) 数据在 DPO 中的关键作用，并构建策略内偏好数据更新模型参数。 |
| [CHiP](https://arxiv.org/pdf/2501.16629) | arXiv'25 | 2025.1.28 | **偏好优化**：提出跨模态分层直接偏好优化，在微调时对全局图文匹配和局部物体特征施加不同层级的惩罚。 |
| [RE-ALIGN](https://arxiv.org/pdf/2502.13146) | arXiv'25 | 2025.2.18 | **偏好优化**：将检索增强生成 (RAG) 引入偏好数据构建，利用检索到的外部知识指导 DPO 训练过程。 |
| [Symmetrical Visual Contrastive Optimization](https://arxiv.org/pdf/2502.13928) | arXiv'25 | 2025.2.19 | **对比优化**：提出对称视觉对比优化，通过使用极简的对比图像对模型进行对齐微调以降低对语言的依赖。 |
| [PerturboLLaVA](https://arxiv.org/pdf/2503.06486) | arXiv'25 | 2025.3.9 | **视觉扰动训练**：在训练前向传播中引入微小的视觉扰动，强制模型学习更鲁棒的视觉表示以抵抗幻觉。 |
| [HLPU](https://arxiv.org/pdf/2503.20673) | arXiv'25 | 2025.3.27 | **负样本微调**：构建底层视觉幻觉数据库，并通过特定的负样本训练策略提升模型对底层特征的感知能力。 |
| [Critique Before Thinking](https://arxiv.org/pdf/2505.07172) | arXiv'25 | 2025.5.12 | **指令微调**：采用基于原理增强的指令微调，让模型在微调阶段学会在给出答案前先生成批评反思逻辑。 |
| [OViP](https://arxiv.org/pdf/2505.15963) | arXiv'25 | 2025.5.21 | **偏好学习**：提出在线视觉-语言偏好学习框架，在训练时动态生成偏好对而非依赖静态离线数据集。 |
| [BIMA](https://arxiv.org/pdf/2505.24649) | arXiv'25 | 2025.5.30 | **极大似然学习**：采用双射最大似然学习方法，通过优化视觉和文本特征之间的联合概率分布来抑制幻觉生成。 |
| [EMPO](https://arxiv.org/pdf/2506.04039) | arXiv'25 | 2025.6.4 | **偏好优化**：提出以实体为中心的多模态偏好优化，在微调时将惩罚粒度精确聚焦到具体的视觉实体 Token 上。 |
| [TL-DPO](https://arxiv.org/pdf/2506.11417) | arXiv'25 | 2025.6.13 | **目标定位 DPO**：停止学习冗余背景，强制权重更新聚焦于产生幻觉的目标区域。 |
| [SEED](https://arxiv.org/pdf/2507.04680) | arXiv'25 | 2025.7.7 | **知识蒸馏**：通过识别并清洗微调数据中的幻觉样本，使用提纯后的高质量数据进行知识蒸馏。 |
| [ReLoop](https://arxiv.org/pdf/2507.04943) | arXiv'25 | 2025.7.7 | **闭环训练**：提出一种闭环训练框架，让模型生成预测后进行逆向验证，将验证误差作为训练信号。 |
| [Obliviate](https://arxiv.org/pdf/2508.04567) | arXiv'25 | 2025.8.6 | **去偏微调**：深入分析预训练阶段引入的物体偏见，并在微调阶段通过反向目标函数进行去偏。 |
| [TARS](https://arxiv.org/pdf/2507.21584) | arXiv'25 | 2025.8.9 | **自适应偏好策略**：采用自适应的 MinMax Token 偏好策略调整奖励分配。 |
| [CHAIR-DPO](https://arxiv.org/pdf/2508.20181) | arXiv'25 | 2025.8.27 | **物体感知 DPO**：结合 CHAIR 评测指标，将物体级别的匹配度作为 DPO 的偏好奖励。 |
| [VPFC](https://arxiv.org/pdf/2509.00371) | arXiv'25 | 2025.8.30 | **解耦微调**：区分“遗漏”和“捏造”两种幻觉成因，并分别构建对应的微调数据进行双管齐下的训练。 |
| [SCPO](https://arxiv.org/pdf/2509.24491) | arXiv'25 | 2025.9.29 | **课程偏好优化**：提出语义课程偏好优化策略，按难度递增的方式训练模型以更平滑地消除幻觉。 |
| [Unified Mitigation](https://arxiv.org/pdf/2511.17254v2) | arXiv'25 | 2025.11.21 | **通用对齐框架**：提出一种跨越多种不同对齐格式的通用训练框架来消除视觉语言偏差。 |
| [Attention Guided Alignment](https://arxiv.org/pdf/2511.17793v1) | arXiv'25 | 2025.11.21 | **注意力引导对齐**：在微调阶段引入基于注意力的正则化项，强迫模型对齐正确的视觉区域。 |
| [Optimizing LVLMs with On-Policy Data](https://arxiv.org/pdf/2512.00706v1) | arXiv'25 | 2025.11.30 | **策略内优化**：进一步强调在进行对齐微调时，使用由模型自身即时生成的数据以解决分布偏移问题。 |
| [Mitigating Object and Action Hallucinations](https://arxiv.org/pdf/2512.04356v1) | arXiv'25 | 2025.12.04 | **对比对齐**：通过自增强机制构造多模态动作和物体对比数据进行对齐训练。 |
| [Cost-efficient Difficulty-aware Preference Optimization](https://arxiv.org/pdf/2601.00623v1) | arXiv'26 | 2026.01.02 | **难度感知 DPO**：引入难度感知机制进行低成本的偏好优化，优先解决高难度幻觉样本。 |
| [Beyond Superficial Unlearning](https://arxiv.org/pdf/2601.16527v1) | arXiv'26 | 2026.01.23 | **鲁棒非学习**：提出感知锐度的非学习机制，彻底抹除模型参数中引起幻觉的深层关联。 |

---

### Decoding Strategies

| Method | Pub | Date | 核心机制 (Methodology) |
| :--- | :--- | :--- | :--- |
| [HallE-Switch](https://arxiv.org/pdf/2310.01779.pdf) | arXiv'23 | 2023.10.3 | **推理干预**：在解码阶段引入控制参数，强制模型在“纯上下文描述”与“参数化知识想象”之间切换。 |
| [VCD](https://arxiv.org/pdf/2311.16922.pdf) | **CVPR'24** | 2023.11.28 | **对比解码**：在推理时，通过对比原始图像和失真图像在 Logit 层的输出分布，进行惩罚解码。 |
| [MARINE](https://arxiv.org/pdf/2402.08680.pdf) | **CVPR'24** | 2024.2.13 | **推理引导**：在推理阶段引入无分类器引导 (CFG)，放大视觉特征在生成过程中的影响力。 |
| [CGD](https://arxiv.org/pdf/2402.15300.pdf) | arXiv'24 | 2024.2.23 | **外部引导解码**：在解码阶段引入外部 CLIP 模型对候选 Token 进行打分引导，以提高图文一致性。 |
| [IBD](https://arxiv.org/pdf/2402.18476.pdf) | **ECCV'24** | 2024.2.28 | **图像偏置解码**：通过对比有图像和无图像输入的 Logits 进行解码以惩罚纯语言先验。 |
| [HALC](https://arxiv.org/pdf/2403.00425.pdf) | **ICML'24** | 2024.3.1 | **焦点对比解码**：提出自适应焦点对比解码，在局部 Token 级别细粒度地抑制幻觉。 |
| [M3ID](https://arxiv.org/pdf/2403.14003.pdf) | **CVPR'24** | 2024.3.20 | **视觉信息对比**：在解码阶段引入视觉信息的 Grounding 机制，通过对比不同信息流来修正偏倚。 |
| [ICD](https://arxiv.org/pdf/2403.18715.pdf) | **ACL'24** | 2024.3.27 | **指令对比解码**：构建正向和负向指令，在推理时对比两者的 Logits 进行解码。 |
| [CODE](https://arxiv.org/pdf/2406.01920v1) | arXiv'24 | 2024.6.4 | **对比解码**：对比模型基于原图和基于自生成描述的 Logits 分布，从而惩罚过度依赖文本的 Token。 |
| [Residual Visual Decoding](https://arxiv.org/pdf/2407.00569) | **ACL'24** | 2024.6.30 | **残差解码**：引入残差视觉连接，将早期的视觉特征直接添加到后续的解码计算中。 |
| [VACoDe](https://arxiv.org/pdf/2408.05337) | arXiv'24 | 2024.7.26 | **视觉增强对比解码**：对比视觉增强图像与原始图像的 Logits，惩罚不一致的生成。 |
| [SID](https://arxiv.org/pdf/2408.02032) | arXiv'24 | 2024.8.4 | **自内省解码**：通过模型自身的内省机制对比不同生成路径的置信度，以过滤幻觉词汇。 |
| [LCD](https://arxiv.org/pdf/2408.04664) | arXiv'24 | 2024.8.6 | **语言对比解码**：构建无图像纯文本输入作为负向参考，计算 Logit 时减去语言先验分数。 |
| [LQCD](https://arxiv.org/pdf/2408.11261) | arXiv'24 | 2024.8.21 | **对比解码**：针对迎合用户的幻觉，引入语言对比解码机制削弱问题本身的误导性先验。 |
| [ConVis](https://arxiv.org/pdf/2408.13906) | **AAAI'25** | 2024.8.25 | **可视化对比解码**：利用注意力可视化技术定位幻觉区域，构造干扰图像进行对比解码。 |
| [RBD](https://arxiv.org/pdf/2409.06485) | arXiv'24 | 2024.9.10 | **重平衡对比解码**：在推理阶段动态调整文本与图像特征的 Logits 权重分布。 |
| [TCD](https://arxiv.org/pdf/2409.16597) | arXiv'24 | 2024.9.25 | **时间对比解码**：通过对比完整视频与被截断视频的输出概率来抑制事件幻觉。 |
| [SGD](https://arxiv.org/pdf/2410.13321) | arXiv'24 | 2024.10.17 | **摘要引导解码**：利用图像摘要作为引导信号，干预输出概率保持上下文一致性。 |
| [CATCH](https://arxiv.org/pdf/2411.12713) | arXiv'24 | 2024.11.19 | **自适应对比解码**：根据 Token 局部特征动态切换对比惩罚强度。 |
| [VaLiD](https://arxiv.org/pdf/2411.15839) | arXiv'24 | 2024.11.24 | **层级融合对比解码**：在解码时融合深浅层视觉信号进行对比，惩罚语言幻觉。 |
| [From Uncertainty to Trust](https://arxiv.org/pdf/2412.06474) | arXiv'24 | 2024.12.9 | **Dropout 引导解码**：利用不确定性机制，动态丢弃高不确定性 Token。 |
| [VCD Analysis](https://arxiv.org/pdf/2412.06775) | arXiv'24 | 2024.12.9 | **机制优化**：剖析视觉对比解码机理，优化超参数和采样分布以提升解码抑制效果。 |
| [VORD](https://arxiv.org/pdf/2412.15739) | arXiv'24 | 2024.12.20 | **视觉序数校准**：在生成阶段直接对 Logits 进行后处理校准，缓解过度自信。 |
| [IMCCD](https://arxiv.org/pdf/2501.01926) | arXiv'25 | 2025.1.3 | **相关性校准解码**：动态调整文本 Token 生成概率与视觉输入的相关性权重。 |
| [IFCD](https://arxiv.org/pdf/2502.01056) | arXiv'25 | 2025.2.3 | **内部事实对比解码**：提取内部生成事实作为参考，进行对比解码以抑制过度外推。 |
| [DeGF](https://arxiv.org/pdf/2502.06130) | **ICLR'25** | 2025.2.10 | **自纠正解码**：引入生成式反馈环路，实时检测并修正当前 Token 的概率分布。 |
| [Octopus](https://arxiv.org/pdf/2503.00361) | **CVPR'25** | 2025.3.1 | **动态对比解码**：根据图像复杂度和局部特征自适应调节对比惩罚力度。 |
| [Decoupling Contrastive Decoding](https://arxiv.org/pdf/2504.08809) | arXiv'25 | 2025.4.9 | **解耦对比解码**：将对比解码中的语言惩罚与视觉增强解耦，处理更复杂的幻觉。 |
| [ECD](https://arxiv.org/pdf/2504.12137) | arXiv'25 | 2025.4.16 | **高效对比解码**：结合概率检测，仅在发现高幻觉风险 Token 时触发对比计算。 |
| [CICD](https://arxiv.org/pdf/2505.10634) | arXiv'25 | 2025.5.20 | **跨图像对比解码**：通过对比语义相似但输入不同的图像 Logits，无损抑制语言先验。 |
| [ED](https://arxiv.org/pdf/2505.17529) | arXiv'25 | 2025.5.23 | **注意力引导集成解码**：整合多个经过不同注意力遮蔽处理的生成路径。 |
| [C-PMI](https://arxiv.org/pdf/2505.19678) | arXiv'25 | 2025.5.26 | **互信息校准解码**：通过量化图文条件互信息 (PMI) 重塑解码候选词概率。 |
| [RVCD](https://arxiv.org/pdf/2505.20569) | arXiv'25 | 2025.5.29 | **检索视觉对比解码**：对比原图与检索到的相似参考图的 Logits 来突出核心事实。 |
| [SECOND](https://arxiv.org/pdf/2506.08391) | arXiv'25 | 2025.6.10 | **选择性对比解码**：仅对特定感知类别的词汇触发惩罚计算，避免破坏语法。 |
| [MoD](https://arxiv.org/pdf/2505.17061) | **ACL'25** | 2025.6.10 | **混合解码策略**：根据注意力强弱自适应切换不同的采样算法。 |
| [ReVisiT](https://arxiv.org/pdf/2506.09522) | arXiv'25 | 2025.6.11 | **语言先验引导解码**：暴露视觉 Token 中的语言先验，并利用其引导解码方向。 |
| [ASCD](https://arxiv.org/pdf/2506.14766) | arXiv'25 | 2025.6.17 | **可操控对比解码**：根据底层注意力流向动态改变对比的负样本分布。 |
| [DLC](https://arxiv.org/pdf/2506.21509) | arXiv'25 | 2025.6.26 | **动态 Logits 校准**：直接根据多模态特征响应对输出词表进行实时校准。 |
| [Energy-Guided Decoding](https://arxiv.org/pdf/2507.07731) | arXiv'25 | 2025.7.10 | **能量引导解码**：引入基于能量模型的概率重整项进行解码约束。 |
| [INTER](https://arxiv.org/pdf/2507.05056) | arXiv'25 | 2025.7.22 | **交互引导采样**：动态评估视觉与文本特征的交互强度，以此为权重修改采样概率。 |
| [MRFD](https://arxiv.org/pdf/2508.10264) | arXiv'25 | 2025.8.14 | **多区域融合解码**：结合自我一致性，融合图像不同局部区域的特征 Logits。 |
| [MRGD](https://arxiv.org/pdf/2508.11616) | arXiv'25 | 2025.8.15 | **奖励引导解码**：引入轻量级奖励模型，实时对候选 Token 进行打分和概率重塑。 |
| [LayerCD](https://arxiv.org/pdf/2509.25177) | arXiv'25 | 2025.9.29 | **层级对比解码**：通过对比模型深层（语言先验）与浅层（视觉特征）的 Logits 实施惩罚。 |
| [MaskCD](https://arxiv.org/pdf/2510.02790v1) | arXiv'25 | 2025.10.3 | **掩码对比解码**：遮蔽特定的图像处理头部构造负面分布，进行对比计算。 |
| [Self-Augmented Visual Contrastive Decoding](https://arxiv.org/pdf/2510.13315v1) | arXiv'25 | 2025.10.15 | **自增强对比解码**：模型自行利用内部特征生成增强和衰减的视觉表示进行对比解码。 |
| [Watermarking for Factuality](https://arxiv.org/pdf/2510.14304v1) | arXiv'25 | 2025.10.16 | **三层对比解码**：结合事实水印技术，在三层概率空间的对比中引导真实事实。 |
| [Token-Level Inference-Time Alignment](https://arxiv.org/pdf/2510.21794) | arXiv'25 | 2025.10.20 | **推断时对齐**：在生成每个 Token 时应用轻量级分类器干预。 |
| [Beyond Single Models](https://arxiv.org/pdf/2510.18321v1) | arXiv'25 | 2025.10.21 | **自适应集成解码**：自回归中自适应集成多个模型的 Token 概率分布。 |
| [Visual Inference-Time Intervention](https://arxiv.org/pdf/2512.03542v1) | arXiv'25 | 2025.12.03 | **推理干预**：在解码瞬间利用视觉特征实时反馈阻断文本生成惯性。 |
| [Watch Closely](https://arxiv.org/pdf/2512.19070v1) | arXiv'25 | 2025.12.22 | **解耦解码**：将注意力机制与输出概率解耦进行独立校准。 |
| [CoFi-Dec](https://arxiv.org/pdf/2512.23453v1) | arXiv'25 | 2025.12.29 | **由粗到细反馈解码**：多粒度层级生成反馈并动态纠正输出。 |
| [Structure-Disrupted Contrastive Decoding](https://arxiv.org/pdf/2601.03500v1) | arXiv'26 | 2026.01.07 | **结构破坏对比解码**：对比原始图像与结构被打破的图像以突出实体逻辑。 |
| [Context-Aware Decoding](https://arxiv.org/pdf/2601.05939v1) | arXiv'26 | 2026.01.09 | **上下文感知解码**：根据已生成的上下文长度动态调节视觉与语言 Logits 之间的融合比例。 |
| [Attention-space Contrastive Guidance](https://arxiv.org/pdf/2601.13707v1) | arXiv'26 | 2026.01.20 | **注意力对比引导**：将对比机制的作用域从输出层前移至注意力空间。 |
| [Residual Decoding](https://arxiv.org/pdf/2602.01047v1) | arXiv'26 | 2026.02.01 | **残差引导解码**：利用历史感知的残差信息指导当前 Token 生成以保持一致性。 |
| [Model-Aware Contrastive Decoding](https://arxiv.org/pdf/2602.01740v1) | arXiv'26 | 2026.02.02 | **模型感知对比解码**：利用反事实数据作为负参考，根据模型感知倾向进行对比惩罚。 |

---

### Attention & Architecture Intervention


| Method | Pub | Date | 核心机制 (Methodology) |
| :--- | :--- | :--- | :--- |
| [OPERA](https://arxiv.org/pdf/2311.17911.pdf) | **CVPR'24** | 2024.1.1 | **注意力惩罚**：提取自注意力矩阵，发现并惩罚过度依赖总结性 Token 的注意力流。 |
| [AvisC](https://arxiv.org/pdf/2405.17820) | arXiv'24 | 2024.5.28 | **注意力校准**：校准注意力头的权重分配，减弱语言先验对视觉输入的隐式覆盖。 |
| [AGLA](https://arxiv.org/pdf/2406.12718) | **CVPR'25** | 2024.6.18 | **注意力融合**：在模型内部融合全局和局部注意力特征矩阵增强感知。 |
| [PAI](https://arxiv.org/pdf/2407.21771) | **ECCV'24** | 2024.7.31 | **注意力放大**：调整跨模态注意力，在注意力层中强行放大视觉 Token 的权重。 |
| [PROJECTAWAY](https://arxiv.org/pdf/2410.02762) | arXiv'24 | 2024.10.3 | **表征编辑**：识别并编辑模型中间层中代表幻觉的视觉-语言特征向量。 |
| [DAMRO](https://arxiv.org/pdf/2410.04514) | **EMNLP'24** | 2024.10.6 | **注意力屏蔽**：潜入 LVLM 内部屏蔽被文本过度主导的特定注意力连接。 |
| [CAUSALMM](https://arxiv.org/pdf/2410.04780) | **ICLR'25** | 2024.10.7 | **因果注意力断开**：基于因果分析，在推理时阻断导致幻觉的特定因果注意力路径。 |
| [FROM PIXELS TO TOKENS](https://arxiv.org/pdf/2410.06795) | arXiv'24 | 2024.10.9 | **早期层干预**：定位物体特征演变，通过早期层干预纠正视觉 Token。 |
| [CCA](https://arxiv.org/pdf/2410.15926) | **NIPS'24** | 2024.10.21 | **同心因果注意力**：在注意力计算中强化局部视觉特征与全局语义的因果关联。 |
| [VTI](https://arxiv.org/pdf/2410.15778) | arXiv'24 | 2024.10.22 | **隐空间引导**：向隐空间注入预训练的控制向量 (Steering vector) 引导生成偏离幻觉。 |
| [EAH](https://arxiv.org/pdf/2411.09968) | arXiv'24 | 2024.11.15 | **头部干预**：准确定位关键注意力头并在前向传播时针对性地增强或抑制。 |
| [Looking Beyond Text](https://arxiv.org/pdf/2411.14279) | arXiv'24 | 2024.11.21 | **双注意力平衡**：引入双注意力机制在架构内部重新平衡文本先验与图像特征。 |
| [ICT](https://arxiv.org/pdf/2411.15268) | arXiv'24 | 2024.11.22 | **跨层级阻断**：提出跨层可信干预，阻断物体表示向错误文本先验的漂移。 |
| [Devils in Middle Layers](https://arxiv.org/pdf/2411.16724) | arXiv'24 | 2024.11.23 | **中间层屏蔽**：利用透镜技术定位中间层幻觉特征，通过特征屏蔽进行纠错。 |
| [WhoBrings the Frisbee](https://arxiv.org/pdf/2412.02946) | arXiv'24 | 2024.12.3 | **因果注意力干预**：实施因果干预切断隐藏在注意力矩阵中的虚假特征图。 |
| [Nullu](https://arxiv.org/pdf/2412.13817) | **CVPR'25** | 2024.12.18 | **隐空间正交化**：将隐状态投影到幻觉空间并进行正交化剥离以清除幻觉。 |
| [VHD](https://arxiv.org/pdf/2412.13949) | arXiv'24 | 2024.12.18 | **注意力头修剪**：量化感知散度，动态屏蔽那些丢失视觉对齐的特定 Head。 |
| [VASparse](https://arxiv.org/pdf/2501.06553) | **CVPR'25** | 2025.1.11 | **稀疏化丢弃**：引入视觉感知的稀疏化，直接丢弃容易诱发幻觉的无关视觉 Token。 |
| [llava-fix-hallucination](https://arxiv.org/pdf/2501.12206) | arXiv'25 | 2025.1.21 | **注意力再平衡**：修正计算分配，防止上下文中长文本前缀“劫持”视觉注意力。 |
| [MINT](https://arxiv.org/pdf/2502.00717) | arXiv'25 | 2025.2.2 | **Token 缩减**：在深层执行动态缩减，去除被语言模型过度关联的图像特征。 |
| [UAC/DAC](https://arxiv.org/pdf/2502.01969) | arXiv'25 | 2025.2.4 | **双向校准**：通过向上的和向下的注意力机制实时双向修正注意力偏移。 |
| [VISTA](https://arxiv.org/pdf/2502.03628) | arXiv'25 | 2025.2.5 | **视觉控制向量**：利用视觉信息 Steering vector 强行引导隐藏状态忠实于图像。 |
| [ADAVIB](https://arxiv.org/pdf/2502.20750) | **AAAI'25** | 2025.2.28 | **信息流约束**：自适应约束模型层间信息流转，阻断导致幻觉的虚假因果路径。 |
| [TPC](https://arxiv.org/pdf/2503.04457) | arXiv'25 | 2025.3.6 | **跨时间步连接**：建立跨时间步网络，传递早期视觉锚点以约束后续 Token。 |
| [EAZY](https://arxiv.org/pdf/2503.07772) | arXiv'25 | 2025.3.10 | **激活值清零**：极简干预架构，直接将导致幻觉的特定图像 Token 激活值清零。 |
| [Attention Reallocation](https://arxiv.org/pdf/2503.08342) | arXiv'25 | 2025.3.12 | **重分配注意力**：推理时重新分配 Attention Maps，将错位注意力拉回视觉目标。 |
| [Attention Hijackers](https://arxiv.org/pdf/2503.08216) | arXiv'25 | 2025.3.14 | **劫持解绑**：探测并消除模型架构内部的注意力“劫持”现象。 |
| [Through the Magnifying Glass](https://arxiv.org/pdf/2503.10183) | arXiv'25 | 2025.3.14 | **感知放大**：在特征层自适应放大目标感知区域的视觉特征强度。 |
| [TruthPrInt](https://arxiv.org/pdf/2503.10602) | arXiv'25 | 2025.3.14 | **潜在真相引导**：在生成第一个 Token 前实施干预，向深层注入真实视觉向量。 |
| [ClearSight](https://arxiv.org/pdf/2503.13107) | **CVPR'25** | 2025.3.14 | **信号增强**：在多模态层放大底层视觉信号以对抗深层语言特征稀释。 |
| [IAVA](https://arxiv.org/pdf/2503.18556) | arXiv'25 | 2025.3.24 | **对齐注意力遮蔽**：根据指令焦点动态遮蔽模型架构内无关图像块的注意力流。 |
| [TARAC](https://arxiv.org/pdf/2504.04099) | arXiv'25 | 2025.4.5 | **累积连接**：建立时间注意力实时累积连接增强记忆事实。 |
| [DCLA](https://arxiv.org/pdf/2505.12343) | arXiv'25 | 2025.5.18 | **层间聚合**：实施层间一致性聚合，融合不同深度表达纠正单一层漂移。 |
| [SEVI](https://arxiv.org/pdf/2505.14257) | arXiv'25 | 2025.5.20 | **流对齐**：强制多模态注意力分布与正确信息流对齐，阻断虚构特征映射。 |
| [SSL](https://arxiv.org/pdf/2505.16146) | arXiv'25 | 2025.5.22 | **SAE 引导**：利用预训练稀疏自编码器 (SAE) 提取并引导内部隐状态。 |
| [SPIN](https://arxiv.org/pdf/2505.16411) | arXiv'25 | 2025.5.22 | **动态抑制头**：通过图像特征精确识别并动态抑制前向传播中被语言主导的头。 |
| [VaLSe](https://arxiv.org/pdf/2505.17812) | arXiv'25 | 2025.5.23 | **潜在反事实干预**：在隐层生成反事实向量进行减法干预 (Latent Steering)。 |
| [CGC](https://arxiv.org/pdf/2505.21547) | arXiv'25 | 2025.5.24 | **离散映射编辑**：在隐空间编辑离散视觉 Token 的映射关系来消除幻觉。 |
| [CAAC](https://arxiv.org/pdf/2505.21472) | arXiv'25 | 2025.5.27 | **自适应校准**：根据特征偏置程度自适应触发注意力权重校准机制。 |
| [CLAIM](https://arxiv.org/pdf/2506.11073) | arXiv'25 | 2025.6.3 | **跨语言注意力干预**：在模型内部切断多语言转换时带来的隐式语义偏差。 |
| [Seeing Far and Clearly](https://arxiv.org/pdf/2505.16652) | arXiv'25 | 2025.6.7 | **注意力因果解码**：重构注意力的因果连接链条，增强视觉依赖。 |
| [HalLoc](https://arxiv.org/pdf/2506.10286) | arXiv'25 | 2025.6.12 | **Token 定位剪枝**：精确定位幻觉源头的 Token 并执行前向切除。 |
| [TAI & HAI](https://arxiv.org/pdf/2506.12609) | arXiv'25 | 2025.6.14 | **双级注意力干预**：在 Token 和 Head 两个粒度级别同时进行注意力干预。 |
| [HalluRNN](https://arxiv.org/pdf/2506.17587) | arXiv'25 | 2025.6.21 | **递归跨层干预**：构建循环推理结构，在 Transformer 层间反复校对特征向量。 |
| [MDSAM](https://arxiv.org/pdf/2506.17664) | arXiv'25 | 2025.6.21 | **记忆驱动稀疏化**：用记忆驱动的方法构造稀疏注意力矩阵，屏蔽冗余输入。 |
| [CAI](https://arxiv.org/pdf/2506.23590) | arXiv'25 | 2025.6.30 | **敏感注意力拦截**：针对 Caption 敏感的注意力分支进行强制性拦截截断。 |
| [ONLY](http://arxiv.org/pdf/2507.00898) | arXiv'25 | 2025.7.1 | **单层精准干预**：证明仅对模型中特定的单一关键层干预就足以大幅抑制物体幻觉。 |
| [EVA](https://arxiv.org/pdf/2507.15652) | arXiv'25 | 2025.7.21 | **中间特征覆盖**：在中间层提取真实事实特征，强制覆盖深层的偏倚特征。 |
| [MCA-LLaVA](https://arxiv.org/pdf/2507.09184) | **ACMMM'25** | 2025.7.23 | **曼哈顿因果替换**：采用基于曼哈顿距离的因果矩阵重构多模态注意力。 |
| [LISA](https://arxiv.org/pdf/2507.19110) | arXiv'25 | 2025.7.25 | **层级积分抑制**：在架构中实施逐层特征累积与语言先验动态抑制。 |
| [MAP](https://arxiv.org/pdf/2508.01653) | arXiv'25 | 2025.8.3 | **图级平滑**：对注意力热力图进行空间平滑过滤，消除导致幻觉的注意力尖峰。 |
| [Modality Bias in LVLMs](https://arxiv.org/pdf/2508.02419) | arXiv'25 | 2025.8.4 | **偏见透镜干预**：使用注意力透镜解析模态偏见并进行底层向量阻断。 |
| [IKOD](https://arxiv.org/pdf/2508.03469) | arXiv'25 | 2025.8.5 | **注意力退化恢复**：恢复模型在长上下文生成时逐渐退化丢失的视觉注意力。 |
| [D-LEAF](https://arxiv.org/pdf/2509.07864) | arXiv'25 | 2025.9.9 | **层头诊断拦截**：定位发生幻觉的具体层和特定头，在推理时实施动态拦截。 |
| [VisionWeaver](https://arxiv.org/pdf/2509.13836) | **EMNLP'25** | 2025.9.17 | **纯视觉强化**：从视觉处理架构入手，从根本上改变模型获取视觉信息的方式。 |
| [Exposing Hallucinations](https://arxiv.org/pdf/2509.21997) | arXiv'25 | 2025.9.26 | **隐层代数编辑**：利用锚点暴露隐空间幻觉向量，在前向传播时进行代数相减。 |
| [On Epistemic Uncertainty](https://arxiv.org/pdf/2510.09008v1) | arXiv'25 | 2025.10.10 | **不确定性丢弃**：计算内部 Token 认知不确定性，丢弃高不确定性视觉特征。 |
| [Hallu-Steer](https://arxiv.org/pdf/2510.11842v1) | arXiv'25 | 2025.10.13 | **隐层引导注入**：在隐状态空间注入预先计算好的反幻觉引导向量。 |
| [Functional Attention Control](https://arxiv.org/pdf/2510.10285v1) | arXiv'25 | 2025.10.11 | **功能硬编码**：将多模态推理功能硬编码到注意力控制流，屏蔽干扰。 |
| [Semantic Entanglement](https://arxiv.org/pdf/2510.12287v1) | arXiv'25 | 2025.10.14 | **投影器解缠**：分析并解耦视觉投影器中的语义纠缠，净化输入的视觉 Token。 |
| [Suppressing Hallucinations](https://arxiv.org/pdf/2510.16596v1) | arXiv'25 | 2025.10.18 | **编码器底层防御**：在视觉编码器端部署防御机制阻断幻觉源头污染。 |
| [PruneHal](https://arxiv.org/pdf/2510.19183v1) | arXiv'25 | 2025.10.22 | **KV Cache 修剪**：在推理中动态识别并修剪代表纯语言偏置的 KV Cache 节点。 |
| [Refining Textual Embeddings](https://arxiv.org/pdf/2511.05017v1) | arXiv'25 | 2025.11.07 | **输入净化**：在架构底层净化文本嵌入特征，减弱其对视觉特征的压制。 |
| [Causal Tracing](https://arxiv.org/pdf/2511.05923v3) | arXiv'25 | 2025.11.08 | **因果截断**：追踪物体表征在层间的流动，实施基于机制解释的精确截断。 |
| [Causally-Grounded Dual-Path](https://arxiv.org/pdf/2511.09018v1) | arXiv'25 | 2025.11.12 | **双路分离流**：建立双路注意力机制，彻底分离真实视觉信息和虚假推理流。 |
| [Adaptive Residual-Update](https://arxiv.org/pdf/2511.10292v1) | arXiv'25 | 2025.11.13 | **自适应残差注入**：在 Transformer 残差连接处极低成本注入自适应引导向量。 |
| [Spectral Representation Filtering](https://arxiv.org/pdf/2511.12220v1) | arXiv'25 | 2025.11.15 | **高频滤波**：利用频域谱分析技术对隐特征进行滤波，滤除引发幻觉的高频噪声。 |
| [Tell Model Where to Look](https://arxiv.org/pdf/2511.20032v1) | arXiv'25 | 2025.11.25 | **硬掩码约束**：在架构内强加硬注意力掩码，强制模型遵循图像显著区域。 |
| [Conscious Gaze](https://arxiv.org/pdf/2512.05546v1) | arXiv'25 | 2025.12.05 | **模拟注视重聚焦**：引入自适应重聚焦模块，模拟人类注视收束散乱注意力。 |
| [Sparse Autoencoder-Driven](https://arxiv.org/pdf/2512.07730v2) | arXiv'25 | 2025.12.08 | **SAE 特征增强**：使用 SAE 提取视觉激活特征并在前向传递时放大强度。 |
| [VEGAS](https://arxiv.org/pdf/2512.12089v1) | arXiv'25 | 2025.12.12 | **编码器引导调控**：利用视觉编码器注意力分布直接调控大语言模型层生成方向。 |
| [Look Closer!](https://arxiv.org/pdf/2512.21999v1) | arXiv'25 | 2025.12.26 | **对抗性参数编辑**：定位储存错误关联的参数，通过对抗编辑直接修正权重分布。 |
| [Adaptive Factual-Guided](https://arxiv.org/pdf/2601.01957v1) | arXiv'26 | 2026.01.05 | **神经元激活编辑**：在事实依据引导下，前向传播中动态修改和编辑神经元激活值。 |
| [Text-Guided Layer Fusion](https://arxiv.org/pdf/2601.03100v1) | arXiv'26 | 2026.01.06 | **动态层融合**：在文本指令指导下动态融合 Transformer 不同层视觉特征。 |
| [Vision-Language Introspection](https://arxiv.org/pdf/2601.05159v1) | arXiv'26 | 2026.01.08 | **双向因果干预**：提出双向因果推断内省机制，在隐空间干预降低模型过度自信。 |
| [VIB-Probe](https://arxiv.org/pdf/2601.05547v1) | arXiv'26 | 2026.01.09 | **信息瓶颈探针**：在层间插入信息瓶颈，压缩掉引发幻觉的冗余多模态互信息。 |
| [One-shot Optimized Steering](https://arxiv.org/pdf/2601.23041v1) | arXiv'26 | 2026.01.30 | **一次性引导计算**：一次性算出最优反幻觉控制向量并在推理时作为偏置注入。 |
| [Contrastive Neuron Steering](https://arxiv.org/pdf/2602.00621v1) | arXiv'26 | 2026.01.31 | **神经元向量引导**：精确定位到产生差异的单个神经元级别，并实施向量引导。 |
| [KVSmooth](https://arxiv.org/pdf/2602.04268v1) | arXiv'26 | 2026.02.04 | **数值平滑**：对 Transformer 的 KV Cache 实施平滑操作，缓解极端激活值崩溃。 |

---

### External Augmentation & Prompting

| Method | Pub | Date | Methodology |
| :--- | :--- | :--- | :--- |
| [LURE](https://arxiv.org/pdf/2310.00754.pdf) | **ICLR'23** | 2023.10.1 | **事后修正**：训练独立 Reviser 模型，专门用于检测和重构输出中的幻觉实体。 |
| [Woodpecker](https://arxiv.org/abs/2310.16045) | **SCIS'24** | 2023.10.24 | **Agent 修正**：调用外部视觉基础模型验证实体事实，最后用 LLM 重写修正。 |
| [Enhancing Multimodal Large Language Models with Vision Detection Models](https://arxiv.org/pdf/2401.17981.pdf) | arXiv'24 | 2024.1.31 | **外部视觉引导**：将外部目标检测模型识别的信息作为上下文直接喂给 MLLM。 |
| [SKIP \N](https://arxiv.org/pdf/2402.01345.pdf) | arXiv'24 | 2024.2.12 | **提示打断**：在输入 Prompt 中添加换行符打断上下文格式，减轻模型语言惯性。 |
| [LogicCheckGPT](https://arxiv.org/pdf/2402.11622.pdf) | arXiv'24 | 2024.2.18 | **逻辑闭环验证**：利用外部语言模型对生成的声明提出问题并自我校验。 |
| [Evaluating and Mitigating Number Hallucinations](https://arxiv.org/pdf/2403.01373.pdf) | arXiv'24 | 2024.3.3 | **多次采样校验**：针对数量幻觉设计基于多次采样一致性检验的提示修复策略。 |
| [DVP](https://arxiv.org/pdf/2403.13513.pdf) | arXiv'24 | 2024.3.20 | **反事实提示**：引入“What if”提示策略，促使模型对初始判断进行自我反思。 |
| [PENSIEVE](https://arxiv.org/pdf/2403.14401.pdf) | arXiv'24 | 2024.3.21 | **多步回顾提示**：采用“回顾后比较”多步提示机制，让模型重审视觉细节修正错误。 |
| [ESREAL](https://arxiv.org/pdf/2403.16167.pdf) | arXiv'24 | 2024.3.26 | **语义打分重构**：提取文本进行重构，配合外部验证器对输出正确性打分拦截。 |
| [TVP](https://arxiv.org/pdf/2404.11207) | arXiv'24 | 2024.4.17 | **原图提示叠加**：在原图上叠加视觉提示（如画圈框选）引导模型强制关注。 |
| [Visual Fact Checker](https://arxiv.org/pdf/2404.19752) | **CVPR'24** | 2024.4.30 | **流水线 Agent**：构建包含声明提取、外部检测验证和修正生成的 Pipeline 系统。 |
| [VDGD](https://arxiv.org/pdf/2405.15683) | arXiv'24 | 2024.5.24 | **感知细节补充**：在输入提示中预先补充缺失的底层视觉感知细节来桥接鸿沟。 |
| [RITUAL](https://arxiv.org/pdf/2405.17821) | arXiv'24 | 2024.5.28 | **多视图一致性**：对图像施加随机几何变换构造多视图，利用一致性校验纠错。 |
| [NoiseBoost](https://arxiv.org/pdf/2405.20081) | arXiv'24 | 2024.5.30 | **噪声集成降低置信度**：输入适度噪声，通过集成多次输出降低模型过度自信。 |
| [DBD](https://arxiv.org/pdf/2406.12663) | arXiv'24 | 2024.6.18 | **提示限制控制**：通过 Prompt 严格控制要求输出的细节数量，平衡丰富度与幻觉率。 |
| [ARA](https://arxiv.org/pdf/2408.00555) | **TOMM'25** | 2024.8.1 | **动态 RAG 补充**：评估模型不确定性并主动触发知识库检索补充实体纠错。 |
| [Detect-then-Calibrate](https://arxiv.org/pdf/2408.09429) | arXiv'24 | 2024.8.18 | **外部检测校准**：利用外部检测器定位错误的关系幻觉，再通过模板二次修正。 |
| [Look, Compare, Decide](https://arxiv.org/pdf/2408.17150) | arXiv'24 | 2024.8.30 | **多路径投票**：采用多视图提示和多路径推理策略，集成比较不同生成路径答案。 |
| [PACU](https://arxiv.org/pdf/2409.14484) | arXiv'24 | 2024.9.22 | **联合辅助描述**：强化输入提示设计并联合图像辅助描述提供更丰富视觉锚点。 |
| [Dentist](https://arxiv.org/pdf/2409.16494) | **TMLR'24** | 2024.9.24 | **外部判别系统**：构建统一的跨模态诊断与缓解 Pipeline，利用外部判别器拦截修改。 |
| [LOOK TWICE BEFORE YOU ANSWER](https://arxiv.org/pdf/2410.03577) | arXiv'24 | 2024.10.4 | **记忆回溯确认**：利用 Prompt 引导模型生成中主动重新提取视觉线索二次确认。 |
| [VHExpansion](https://arxiv.org/pdf/2410.11242) | arXiv'24 | 2024.10.15 | **测试用例对抗**：自动生成具有对抗性的复杂提示词扩充促使模型规避幻觉。 |
| [Thinking Before Looking](https://arxiv.org/pdf/2411.12591) | arXiv'24 | 2024.11.15 | **显式 CoT 约束**：引入思维链提示，强制模型在输出最终答案前写出推理步骤。 |
| [TPO: A Topic-level Self-Correctional Approach](https://arxiv.org/pdf/2411.17265) | arXiv'24 | 2024.11.26 | **主题级打分自我修正**：模型生成草稿后，针对各个子主题进行独立的回顾与自我打分。 |
| [VisVM](https://arxiv.org/pdf/2412.03704) | arXiv'24 | 2024.12.6 | **外部打分搜索**：引入外部视觉价值模型辅助树搜索，引导自回归生成正确路径。 |
| [DEHALL](https://arxiv.org/pdf/2412.11124) | arXiv'24 | 2024.12.15 | **多视角交叉核对**：利用自下而上的整体推理框架配合多视角提示验证来核对事实。 |
| [Toward Robust Hyper-Detailed Image Captioning](https://arxiv.org/pdf/2412.15484) | arXiv'24 | 2024.12.20 | **Multi-Agent 辩论**：部署扮演不同角色的多 Agent 系统进行生成与交叉辩论纠错。 |
| [EAGLE](https://arxiv.org/pdf/2501.02699) | arXiv'25 | 2025.1.6 | **结构化坐标要求**：通过改进提示结构，要求模型输出附带视觉接地 (Grounding) 坐标。 |
| [Socratic Questioning](https://arxiv.org/pdf/2501.02964) | arXiv'25 | 2025.1.7 | **多轮苏格拉底追问**：采用苏格拉底式提问提示，通过多轮自我追问过滤幻觉。 |
| [MIAVLM](https://arxiv.org/pdf/2501.10011) | arXiv'25 | 2025.1.17 | **负向指令约束**：在系统提示中显式引入负向约束指令，结合多视图验证。 |
| [Poison as Cure](https://arxiv.org/pdf/2501.19164) | arXiv'25 | 2025.1.31 | **物理加噪反向激发**：在输入原图中显式注入特定视觉噪声激发模型规避能力。 |
| [CAP](https://arxiv.org/pdf/2502.08317) | arXiv'25 | 2025.2.12 | **空间逻辑规则提示**：在 Prompt 中显式加入空间关系逻辑规则约束以纠正错乱。 |
| [API Cutoff](https://arxiv.org/pdf/2502.15389) | arXiv'25 | 2025.2.21 | **API 截断关注**：利用特定 Cutoff 提示截断背景处理，强制模型只描述前景目标。 |
| [Treble Counterfactual VLMs](https://arxiv.org/pdf/2503.06169) | arXiv'25 | 2025.3.6 | **反事实推理注入**：通过在输入端加入因果推理提示框架让模型识别假象。 |
| [MFP](https://arxiv.org/pdf/2503.14895) | arXiv'25 | 2025.3.19 | **多频率共识校验**：在输入端施加多频扰动，通过对比不同频率下的答案获取共识。 |
| [Generate, but Verify](https://arxiv.org/pdf/2504.13169) | arXiv'25 | 2025.4.17 | **重采样验证**：生成初始结果后，进行针对性的回顾重采样验证过滤错误。 |
| [Hydra](https://arxiv.org/pdf/2504.14395) | arXiv'25 | 2025.4.19 | **Agent 交互防线**：部署包含推理、提问和总结的 Agent 代理对抗输入攻击。 |
| [BBVPE](https://arxiv.org/pdf/2504.21559) | arXiv'25 | 2025.4.30 | **自动化补丁搜索**：通过黑盒优化自动搜索能够抑制幻觉的特定“视觉提示补丁”。 |
| [EVRB](https://arxiv.org/pdf/2505.19498) | arXiv'25 | 2025.5.26 | **贝叶斯概率校验**：应用贝叶斯视角在生成端强化模型对视觉特征依赖的检验。 |
| [When Semantics Mislead Vision](https://arxiv.org/pdf/2506.05551) | arXiv'25 | 2025.6.5 | **场景文本特别处理**：针对 OCR 场景在输入端增加对语义误导的特别拦截提示。 |
| [LPS](https://arxiv.org/pdf/2506.06729) | arXiv'25 | 2025.6.7 | **外部局部锁定**：回答前先利用外部检索系统锁定原图中的局部事实细节。 |
| [PostAlign](https://arxiv.org/pdf/2506.17901) | arXiv'25 | 2025.6.22 | **Grounding 透镜纠正**：利用多模态 Grounding 作为外部透镜在生成最终文本前替换实体。 |
| [ReCo](https://arxiv.org/pdf/2506.22636) | arXiv'25 | 2025.6.27 | **备忘录组合提示**：在提示中附带结构化的“备忘录”强制模型检查必备要素。 |
| [Preemptive Hallucination Reduction](https://arxiv.org/pdf/2506.22636) | arXiv'25 | 2025.6.27 | **先发制人输入拦截**：在提示词和初始输入预处理阶段设置拦截机制。 |
| [SENTINEL](https://arxiv.org/pdf/2507.12455) | **ICCV'25** | 2025.7.16 | **早期句子截断**：在文本生成早期句子阶段实施事实性截断提示，防止错误蔓延。 |
| [ViHallu](https://arxiv.org/pdf/2507.22003) | arXiv'25 | 2025.7.30 | **变体输入交叉比对**：在输入端构造图像扰动变体，交叉比对变体输出以过滤非事实。 |
| [Prompt-in-Image](https://arxiv.org/pdf/2508.01678) | arXiv'25 | 2025.8.3 | **物理像素嵌入**：将文本指令直接渲染并嵌入到图像像素中强制模型遵循。 |
| [SAVER](https://arxiv.org/pdf/2508.03177) | arXiv'25 | 2025.8.5 | **风格提前预告**：外部模块提前识别图像风格实体，将正确信息通过 Prompt 喂给模型。 |
| [Hacking Hallucinations](https://arxiv.org/pdf/2508.04182) | arXiv'25 | 2025.8.6 | **因果要素拆解打分**：从黑盒输入端用外部算法执行因果充分性与必要性打分。 |
| [APASI](https://arxiv.org/pdf/2509.11287) | arXiv'25 | 2025.9.14 | **陷阱预埋规避**：故意让模型先生成幻觉陷阱，再通过提示指令让其自我规避。 |
| [Self-Consistency as a Free Lunch](https://arxiv.org/pdf/2509.23236) | arXiv'25 | 2025.9.27 | **一致性自反思**：在纯黑盒设定下利用自我一致性投票进行反思判断。 |
| [GACD](https://arxiv.org/pdf/2509.03113) | arXiv'25 | 2025.10.1 | **梯度指导反思**：结合外部计算出的梯度信息反馈作为 Prompt，触发模型深度纠错。 |
| [ChainMPQ](https://arxiv.org/pdf/2510.06292v1) | arXiv'25 | 2025.10.7 | **交错步骤约束**：要求模型严格按文本-图像交错步骤输出推理链来验证关系。 |
| [When Images Speak Louder](https://arxiv.org/pdf/2510.10466v1) | arXiv'25 | 2025.10.12 | **外部参照物约束**：在输入端提供强跨模态检索信息作为参照物，约束自由发散。 |
| [Why LVLMs Are More Prone to Hallucinations in Longer Responses](https://arxiv.org/pdf/2510.20229v1) | arXiv'25 | 2025.10.23 | **记忆管理提示**：针对长文本分析雪球效应，提出基于 Prompt 的长上下文截断策略。 |
| [Capturing Gaze Shifts for Guidance](https://arxiv.org/pdf/2510.22067) | arXiv'25 | 2025.11.10 | **人类眼动轨迹输入**：将人类观察图像时的眼动轨迹作为额外特征输入给模型引导注意。 |
| [Taming Object Hallucinations](https://arxiv.org/pdf/2511.09228v1) | arXiv'25 | 2025.11.12 | **原子粒度拆解打分**：要求模型对回答进行原子级拆解附带置信度，外部工具辅助校验。 |
| [Hallucination Mitigation via Introspection](https://arxiv.org/pdf/2512.02981v1) | arXiv'25 | 2025.12.02 | **跨模态内省辩论**：部署由内省 Agent 和外部验证 Agent 组成的网络，进行交互辩论。 |
| [Ground What You See](https://arxiv.org/pdf/2601.06224) | arXiv'26 | 2026.01.09 | **多样化外部反馈**：结合多样性采样和外部反馈闭环在生成端进行黑盒优化。 |
| [Hallucination Begins Where Saliency Drops](https://arxiv.org/pdf/2601.20279v1) | arXiv'26 | 2026.01.28 | **显著性拦截门**：基于外部计算的图像显著性，在阈值过低时主动拒绝回答。 |
| [Countering the Over-Reliance Trap](https://arxiv.org/pdf/2601.22451v1) | arXiv'26 | 2026.01.30 | **流水线自验证**：设计包含命题提取、重查和逻辑判定的黑盒自验证 Pipeline。 |
| [A Training-Free Hallucination Mitigation Framework](https://arxiv.org/pdf/2601.00659v1) | arXiv'26 | 2026.01.02 | **黑盒通用框架**：整合多种即插即用的外部免训练手段形成通用抑制框架。 |

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

