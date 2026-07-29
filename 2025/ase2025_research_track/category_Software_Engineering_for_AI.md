# ASE 2025 Research Track — Software Engineering for AI

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 6

## 1. AutoFid: Adaptive and Noise-Aware Fidelity Measurement for Quantum Programs via Circuit Graph Analysis

**Authors:** Tingting Li (Zhejiang University), Ziming Zhao (Zhejiang University), Jianwei Yin (Zhejiang University)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11334407

**中文总结:** 提出 AutoFid，将量子电路建模为 DAG 并结合门保真度、深度膨胀与串扰等编译特征自适应确定保真度测量次数，运行时以置信区间早停节省 NISQ 设备测量开销。

**Abstract:** Quantum computers in the Noisy Intermediate- Scale Quantum (NISQ) era face significant challenges due to inherent noise and limited qubit coherence. Accurate fidelity evaluation of quantum states necessitates multiple repeated measurements to obtain statistical results. But determining the optimal number of measurements remains an open problem due to the dynamic, device-dependent nature of quantum noise. Existing approaches either assume prior knowledge of noise models or rely on historical circuit data, limiting their applicability in practical deployment scenarios. This paper presents AutoFid, an adaptive and noise-aware fidelity measurement framework that automatically determines the number of required tests based on circuit structure and hardware feedback. AutoFid models quantum circuits as Directed Acyclic Graphs and estimates structural complexity via random walks, enabling principled estimation of measurement effort. It further incorporates transpilation-aware features such as gate fidelity, depth inflation, and crosstalk to refine iteration budgets. During runtime, AutoFid dynamically samples fidelity results and employs an early stopping strategy based on confidence intervals to reduce redundant measurements while preserving statistical guarantees. We evaluate AutoFid on 18 quantum benchmarks executed on real IBMQ hardware platforms. Experimental results show that AutoFid reduces measurement costs by more than 50% compared to both fixed shot and learning based baselines, while consistently maintaining fidelity bias below 0.01. Additional analysis using classical software testing metrics and ablation studies demonstrate its effectiveness, robustness, and adaptability across a wide range of quantum workloads.


## 2. Efficient Understanding of Machine Learning Model Mispredictions

**Authors:** Martin Eberlein (Humboldt-Universtität zu Berlin), Jürgen Cito (TU Wien), Lars Grunske (Humboldt-Universität zu Berlin)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11334517

**中文总结:** 提出 MMDPP，先聚焦最影响误分类的特征再用决策树替代高开销 rule set 解释 ML 组件误预测；在 11 个真实数据集上既提升诊断准确性又显著降低计算成本，适用于安全/任务关键系统中的模型调试。

**Abstract:** Mispredictions by machine learning components can have severe consequences, especially in safety-critical and mission-critical software systems. Therefore, understanding and debugging these mispredictions is a crucial part of the development process for systems that use machine learning components. Previous research has successfully applied methods that identify when a model’s predictions may be unreliable by generating a rule set that links feature values to prediction errors. However, current state-of-the-art rule set approaches require significant computational resources, particularly for large data sets.

To address these high computational demands, we propose a strategy to identify and focus only on the most influential features that lead to mispredictions. Additionally, to improve the accuracy of mispredictions diagnosis, we replace traditional rule-based approaches with decision tree learning. We evaluate our tool \MMDPP{} across 11 diverse real-world data sets. The results show that focusing on influential features with decision trees improves the accuracy of misprediction explanations, while significantly reducing computational demands in all scenarios. Thus, \MMDPP{} produces better results much faster, making it more efficient and effective for generating misprediction explanations.


## 3. From Sparse to Structured: A Diffusion-Enhanced and Feature-Aligned Framework for Coincidental Correctness Detection

**Authors:** Huan Xie (Chongqing University), Chunyan Liu (Chongqing University), Yan Lei (Chongqing University), Zhenyu Wu (School of Big Data & Software Engineering, Chongqing University), Jinping Wang (Chonqing University)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11334293

**中文总结:** 提出 DEFACC，用扩散增强生成模块缓解偶然正确（CC）检测的类别不平衡，并通过特征对齐获得更结构化的测试表示；提升 CC 识别准确率以减轻对测试缩减、故障定位、APR 等任务的噪声干扰。

**Abstract:** Coincidental correctness (CC) refers to test cases that execute faulty code but still produce excepted outputs. This phenomenon introduces noise into the data of software testing-related tasks. As demonstrated in the literature, CC has negative impact on test suite reduction, test case prioritization, fault localization, and automated program repair. Thus, it is essential to detect and mitigate the impact of CC. Although CC is commonly observed across a large number of programs, CC test cases are typically sparse within each program’s test suite. In other words, CC test cases generally make up merely a small portion of the passing test cases. The proportions vary from 3.27% to 31.74% within Defects4J V1.4. This results in a highly imbalanced distribution of CC versus non-CC test cases, posing challenges for accurate detection. To address this issue, we propose a Diffusion-Enhanced and Feature-Aligned Framework for Coincidental Correctness detection, named DEFACC, to obtain more structured representations of test cases. Specifically, DEFACC first introduces a diffusion- based generation module. This module generates new CC samples from original samples to alleviate class imbalance issue and enhance the diversity of CC samples. However, generated feature samples may deviate from the distribution of real CC samples. Such shifts can hurt model reliability and generalization. To resolve this, DEFACC integrates a feature alignment module that is founded on the Maximum Mean Discrepancy (MMD) loss. This module enforces distributional consistency between generated and original CC samples during training. Together, these components ensure that the augmented samples are from sparse to structured, which is not only quantitatively balanced but also semantically faithful. Experimental results show that the DEFACC significantly improves the performance existing CC detection methods and provides a stronger representation foundation for accurate fault localization.


## 4. Provable Fairness Repair for Deep Neural Networks

**Authors:** Jianan Ma (Hangzhou Dianzi University, China; Zhejiang University, Hangzhou, China), Jingyi Wang (Zhejiang University), Qi Xuan (Zhejiang University of Technology; Binjiang Institute of Artificial Intelligence), Zhen Wang (Hangzhou Dianzi University, China)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11334285

**中文总结:** 提出 ProF，基于区间边界传播（IBP）对偏见样本邻域给出可证明公平性约束，并转化为 MILP 求解以修复 DNN；相较数据驱动方法，对未见样本亦具形式化公平保证。

**Abstract:** Deep neural networks (DNNs) are suffering from ethical issues such as individual discrimination. In response, extensive NN repair techniques have been developed to adjust models and mitigate such undesired behaviors. However, existing fairness repair methods are typically data-centric, which often lack provable guarantees and generalization to unseen samples. To overcome these limitations, we propose ProF, a novel fairness repair framework with provable guarantees. The key intuition of ProF is to leverage interval bound propagation (a widely used NN verification technique) to soundly capture model outputs over the whole set $\mathcal{S}(\bm{x})$ around a biased sample $\bm{x}$. The derived bounds are utilized to guide fairness repair which encourages the model to produce consistent outputs on $\mathcal{S}(\bm{x})$. Specifically, we integrate fairness constraints and model modifications into a unified constraint-solving formulation, which can be transformed to a Mixed-Integer Linear Programming (MILP) problem solvable by off-the-shelf solvers. The solution to the MILP problem effectively induces a repaired model with guaranteed fairness over the whole set $\mathcal{S}(\bm{x})$. We evaluate ProF on four widely used benchmark datasets and demonstrate that it achieves provable fairness repair, with generalization of up to 95.93% on full datasets and 93.16% on the entire input space. Notably, ProF can be easily configured to support multiple sensitive attributes and more practical fairness definitions, while providing provable repair guarantees and delivering around 90% fairness improvement. Our code is available in this repository.


## 5. TensorGuard: Gradient-Based Model Fingerprinting for LLM Similarity Detection and Family Classification

**Authors:** Zehao Wu (Huazhong University of Science and Technology), Yanjie Zhao (Huazhong University of Science and Technology), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11334251

**中文总结:** 提出 TensorGuard，基于随机输入扰动下的梯度响应提取 LLM 内在行为指纹，用于相似度检测与模型家族分类；可在不依赖训练数据或水印的情况下识别微调/合并等衍生模型，支撑开源许可合规追踪。

**Abstract:** As Large Language Models (LLMs) become integral software components in modern applications, unauthorized model derivations through fine-tuning, merging, and redistribution have emerged as critical software engineering challenges. Unlike traditional software where clone detection and license compliance are well-established, the LLM ecosystem lacks effective mechanisms to detect model lineage and enforce licensing agreements. This gap is particularly problematic when open-source model creators, such as Meta’s LLaMA, require derivative works to maintain naming conventions for attribution, yet no technical means exist to verify compliance.

To fill this gap, treating LLMs as software artifacts requiring provenance tracking, we present TensorGuard, a gradient-based fingerprinting framework for LLM similarity detection and family classification. Our approach extracts model-intrinsic behavioral signatures by analyzing gradient responses to random input perturbations across tensor layers, operating independently of training data, watermarks, or specific model formats. TensorGuard supports the widely-adopted safetensors format and constructs high-dimensional fingerprints through statistical analysis of gradient features. These fingerprints enable two complementary capabilities: direct pairwise similarity assessment between arbitrary models through distance computation, and systematic family classification of unknown models via the K-Means clustering algorithm with domain-informed centroid initialization using known base models. Experimental evaluation on 58 models comprising 8 base models and 50 derivatives across five model families (Llama, Qwen, Gemma, Phi, Mistral) demonstrates 94% classification accuracy under our centroid-initialized K-Means clustering. Our work establishes a new paradigm for model similarity detection, bridging traditional software engineering practices with modern LLM distribution and compliance challenges.


## 6. When Faster Isn't Greener: The Hidden Costs of LLM-Based Code Optimization

**Authors:** Tristan Coignion (Université de Lille - Inria), Clément Quinton (Université de Lille), Romain Rouvoy (University Lille 1 and INRIA)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11334535

**中文总结:** 基于 EvalPerf 118 项任务系统评估 LLM 代码优化的能耗权衡，引入 Break-Even Point（BEP）度量优化收益需多少次执行才能抵消生成能耗；表明更快代码未必更节能，LLM 优化本身能耗常不可忽视。

**Abstract:** \emph{Large Language Models} (LLMs) are increasingly adopted to optimize source code, offering the promise of faster, more efficient programs without manual tuning. This capability is particularly appealing in the context of sustainable computing, where enhanced performance is often assumed to correspond to reduced energy consumption. However, LLMs themselves are energy- and resource-intensive, raising critical questions about whether their use for code optimization is energetically justified. Prior work mainly focused on runtime performance gains, leaving a gap in our understanding of the broader energy implications of LLM-based code optimization.

In this paper, we report on a systematic, energy-focused evaluation of LLM-based code optimization methods. Relying on $118$ tasks from the EvalPerf benchmark, we assess the trade-offs between code performance, correctness, and energy consumption of multiple optimization methods across multiple families of LLMs. We introduce the \emph{Break-Even Point} (BEP) as a key metric to quantify the number of executions required for an optimized program to outweigh the energy consumed when generating the optimization itself.

Our results show that, while certain configurations achieve substantial speedups and energy reductions, these benefits often demand from hundreds to hundreds of thousands of executions to become energetically profitable. Moreover, the optimization process often yields incorrect or less efficient code. Importantly, we identify a weak negative correlation between performance gains and actual energy savings, challenging assumptions that faster code automatically equates to a smaller energy footprint. This work underscores the necessity of energy-aware optimization strategies. Practitioners should carefully target LLM-based optimization efforts to high-frequency, high-impact workloads, while monitoring energy consumption across the entire life-cycle of development and deployment.

