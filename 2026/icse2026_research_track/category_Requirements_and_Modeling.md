# ICSE 2026 Research Track — Requirements and Modeling

Source: https://conf.researchr.org/track/icse-2026/icse-2026-research-track?#event-overview

Total in this category: 7 papers

## 1. Bayesian Multi-Level Performance Models for Multi-Factor Variability of Configurable Software Systems

**Authors:** Johannes Dorn (Leipzig University), Stefan Mühlbauer (Leipzig University), Stefan Jahns (Universität Leipzig), Sven Apel (Saarland University), Norbert Siegmund (Leipzig University)

**Categories:** Requirements and Modeling

**中文总结:** 提出 HyPerf 贝叶斯多层性能建模，分层区分配置不变与随 workload 等外部因素变化的性能影响；以更少训练样本实现更准确的配置性能预测。

**Abstract:** Tuning a software system’s configuration is essential to meet performance requirements. However, not only do configuration options affect performance, but also the system’s interaction with external factors such as the workload. Hence, tuning requires understanding how a specific setting of external factors (e.g., a specific workload) in combination with the system configuration influences performance. Current performance modeling approaches usually do not incorporate external factors, for good reasons: training a separate model per setting is costly and is unlikely to generalize, whereas a single model trained on multiple settings fails to capture variations that are specific to a certain setting . To address this shortcoming, we propose HyPerf, a Bayesian multi-level performance modeling approach that systematically distinguishes between setting-invariant and setting-variant influences, that is, influences that remain consistent across settings versus those that exhibit substantial variation. For this purpose, HyPerf employs a hierarchical structure: The upper level captures general performance trends across multiple settings (e.g., across different workloads), while the lower level refines these estimates with setting-specific deviations (e.g., workload-specific performance variations). With HyPerf, we aim at balancing accuracy and efficiency , achieving robust performance predictions with significantly fewer training samples. Unlike the state of the art, HyPerf is able to identify a minimal set of settings that captures essential performance variations, so that developers can approximate whether all setting-variant influences have been accounted for. Empirical evaluations on ten real-world software systems across up to 35 workloads demonstrates that HyPerf matches or outperforms state-of-the-art approaches while requiring fewer measurements. Notably, HyPerf enables interpretable performance reasoning and can identify minimal workload subsets that capture essential performance variations.

## 2. Can SAT Solvers Keep Up With the Linux Kernel's Feature Model?

**Authors:** Elias Kuiter (University of Magdeburg), Urs-Benedict Braun (University of Magdeburg), Thomas Thüm (TU Braunschweig), Sebastian Krieter (TU Braunschweig, Germany), Gunter Saake (University of Magdeburg, Germany)

**Categories:** Requirements and Modeling

**Awards:** Distinguished Paper Award

**中文总结:** 实证分析 Linux 内核 feature model 与历史 SAT 求解器性能，发现即便最优求解器仍无法跟上内核增长，性能约每 7 年减半；警示产品线分析将日益困难。

**Abstract:** The Linux kernel is a highly relevant, yet also highly configurable software system. Kernel developers keep track of this configurability in a feature model, which defines the features of Linux and their dependencies. To support kernel developers in various activities, many (semi-)automated product-line analyses have been proposed over the years. Under the hood, these analyses can often be computed with SAT solvers. Yet, the Linux kernel has constantly been growing in complexity for decades, which increasingly hampers its efficient analysis. At the same time, SAT solvers have been improving in performance for decades, which eases analysis. In this paper, we investigate empirically whether SAT solvers can keep up with the Linux kernel’s feature model. To this end, we analyze historic feature models of Linux with historic SAT solvers from several sources. We find that SAT solvers are generally not able to keep up with Linux. Even the optimal SAT solver is slowing down by 10% every year, meaning that its performance halves every seven years. We conclude that the Linux kernel will become increasingly difficult to analyze if its growth is not counteracted.

## 3. Light over Heavy: Automated Performance Requirements Quantification with Linguistic Inducement

**Authors:** Shihai Wang (University of Electronic Science and Technology of China), Tao Chen (University of Birmingham)

**Categories:** Requirements and Modeling

**中文总结:** 提出 LQPR，用轻量语言学诱导匹配将性能需求量化转为分类问题，在 9 个学习基线上 88%+ 场景为 sole best 且成本约低两个数量级。

**Abstract:** Elicited performance requirements need to be quantified for compliance in different engineering tasks, e.g., configuration tuning and performance testing. Much existing work has relied on manual quantification, which is expensive and error-prone due to the imprecision. In this paper, we present LQPR, a highly efficient automatic approach for performance requirements quantification. LQPR relies on a new theoretical framework that converts quantification as a classification problem. Despite the prevalent applications of Large Language Models (LLMs) for requirement analytics, LQPR takes a different perspective to address the classification: we observed that performance requirements can exhibit strong patterns and are often short/concise, therefore we design a lightweight linguistically induced matching mechanism. We compare LQPR against nine state-of-the-art learning-based approaches over diverse datasets, demonstrating that it is ranked as the sole best for 88% or more cases with two orders less cost. Our work proves that, at least for performance requirement quantification, specialized methods can be more suitable than the general LLM-driven approaches.

## 4. LikeThis! Empowering App Users to Submit UI Improvement Suggestions Instead of Complaints

**Authors:** Jialiang Wei (Hasso Plattner Institute), Ali Ebrahimi Pourasad (University of Hamburg), Walid Maalej (University of Hamburg)

**Categories:** Requirements and Modeling

**中文总结:** 提出 LikeThis!，用 GenAI 根据用户评论与截图生成 UI 改进方案供选择，GPT-Image-1 在基准与用户/开发者研究中均显著提升反馈可理解性与可执行性。

**Abstract:** User feedback is crucial for the evolution of mobile apps. However, research suggests that users tend to submit uninformative, vague, or destructive feedback. Unlike recent AI4SE approaches that focus on generating code and other development artifacts, our work aims at empowering users to submit better and more constructive UI feedback with concrete suggestions on how to improve the app. We propose LikeThis!, a GenAI-based approach that takes a user comment with the corresponding screenshot to immediately generate multiple improvement alternatives, from which the user can easily choose their preferred option. To evaluate LikeThis!, we first conducted a model benchmarking study based on a public dataset of carefully critiqued UI designs. The results show that GPT-Image-1 significantly outperformed three other state-of-the-art image generation models in improving the designs to address UI issues while keeping the fidelity and without introducing new issues. An intermediate step in LikeThis! to generate a solution specification before changing the design was key to achieving effective improvement. Second, we conducted a user study with 10 production apps, where 15 users used LikeThis! to submit their feedback on encountered issues. Later, the developers of the apps assessed the understandability and actionability of the feedback with and without generated improvements. The results show that our approach helps generate better feedback from both user and developer perspectives, paving the way for AI-assisted user-developer collaboration.

## 5. Modeling Like Peeling an Onion: Layerwise Analysis-Driven Automatic Behavioral Model Generation

**Authors:** Yike Huang (East China Normal University), Ming Hu (East China Normal University, China), Xiaohong Chen (East China Normal University), Zhi Jin (Peking University, Wuhan University), Shuyuan Xiao (East China Normal University)

**Categories:** Requirements and Modeling

**中文总结:** 提出 LATO 分层分析驱动方法，模仿“剥洋葱”逐步分解需求并生成 UML 活动图，在开源与工业数据集上节点/关系 F1 相对 SOTA 最高提升 71.1%/52.4%。

**Abstract:** As software complexity skyrockets and requirements evolve at breakneck speed, traditional human-centric behavioral modeling can no longer keep pace in terms of efficiency, accuracy, and scalability. While existing automated approaches can produce models, they still struggle with deep semantic understanding of textual requirements or with reasoning about intricate system logic, especially nested relationships. Inspired by the way experienced analysts “peel back” layers of a problem, we propose LATO, a \textbf{L}ayerwise \textbf{A}nalysis-Driven Au\textbf{T}omatic Behavioral M\textbf{O}deling approach. It employs a progressive decomposition strategy to guide large language models in incrementally parsing requirement structures, deconstructing behavioral dependencies, and ultimately generating executable UML activity diagrams. Comprehensive evaluations on four open-source datasets and two real-world industrial systems show that LATO comprehensively outperforms state-of-the-art baselines in accuracy, completeness, and syntactic compliance: $F_1$ scores for behavioral node-extraction improve by up to 71.1%, relation-extraction $F_1$ by 52.4 % relatively, and syntactic pass rates remain above 96.67%. The framework also exhibits strong robustness to input perturbations, confirming its cross-domain generalizability. This paper is the first to tightly fuse human-inspired strategies with LLMs in behavior modeling, yielding an intelligent infrastructure that exhibits expert-level logical understanding and generalization. By closing the modeling-skills gap, LATO delivers a next-generation, low-cost, and explainable solution for requirements engineering and AI-native software development.

## 6. Synthesizing Hardware-Specific Instructions for Efficient Code Generation of Simulink

**Authors:** Zehong Yu (KLISS, BNRist, School of Software, Tsinghua University), Zhuo Su (Beihang University), Rui Wang (Capital Normal University, Beijing, China), Yu Jiang (Tsinghua University)

**Categories:** Requirements and Modeling

**中文总结:** 提出 Simulink 代码生成器 AMICA，利用模型语义与数据流图规则合成硬件专用指令，在多个平台上比 Embedded Coder/Mercury 快 1.20–6.54 倍并缩小代码体积。

**Abstract:** Simulink has become a pivotal tool in embedded scenarios, offering a model-driven approach for embedded software development. Given the tight performance and resource constraints in embedded applications, it is crucial to ensure the efficiency of the code generated from Simulink models. Code generators implement various optimizations to enhance performance. However, they neglect the potential of hardware-specific instructions available in modern processors, such as saturation-type instructions, which accomplish complex operations in fewer cycles. Moreover, relying on state-of-the-art compilers to use these instructions is also not as effective as expectation, due to their complex semantics. This paper proposes AMICA, an efficient code generator for Simulink models with hardware-specific instruction synthesis. The key insight of AMICA is to leverage model semantics to effectively synthesize the appropriate instructions. AMICA first converts the model into the dataflow graph and crafts a series of optimization rules represented as dataflow subgraph with constraints related to block parameters, data types, and other critical properties. Then, AMICA iteratively matches these rules with dataflow graph to obtain the optimizable candidates. The candidate that maximizes latency reduction is chosen to update the dataflow graph. Finally, AMICA synthesizes the appropriate instructions for optimizable blocks in accordance with instruction syntax and block properties. We implemented and evaluated AMICA on benchmark Simulink models. Compared with the state-of-the-art code generators Simulink Embedded Coder and Mercury, the code generated by AMICA is 1.20$\times$ - 6.54$\times$ faster in terms of execution time across different platforms. Besides, AMICA reduces 6% - 53% assembly code size of the compiled programs, while performing similarly in terms of data segment size and BSS segment size.

## 7. Unlocking the Silent Needs: Business-Logic-Driven Iterative Requirements Auto-completion

**Authors:** Zhujun Wu (East China Normal University Shanghai, China), Xiaohong Chen (East China Normal University), Zhi Jin (Peking University, Wuhan University), Ming Hu (East China Normal University, China), Dongming Jin (Peking University, China)

**Categories:** Requirements and Modeling

**中文总结:** 提出 ReqCompleter，以用例-实体-操作闭环融合用例模型、E-R 图与 CRUD 矩阵迭代补全需求，完整性提升 20–88% 且幻觉率下降 2.4–13.9%。

**Abstract:** To tackle the dual challenges of incomplete requirements and hallucinations in large language models (LLMs), this paper proposes a business-logic-driven iterative requirements auto-completion approach named ReqCompleter. By treating the use case – entity– operation” triplet as the smallest computable closed loop, ReqCompleter adopts a model-driven iterative mechanism. First, a use-case model, an E-R diagram, and a CRUD (Create, Read, Update, Delete) matrix are fused into a unified semantic framework. Next, gaps in the CRUD matrix act as triggers to iteratively detect missing functionalities, while the E-R diagram delimits entity boundaries to steer the LLM toward generating requirements within a controlled scope. We evaluate our approach across seven cases in e-commerce, logistics, public safety and other domains. Compared to general-purpose LLMs, it improves requirements completeness rate by 20%-88% while reducing hallucination rate by 2.4%-13.9%. To the best of our knowledge, this work represents the first tight coupling of classical requirements engineering models with generative AI, establishing an automated closed-loop system that delivers what’s missing, as needed" under explicit business logic constraints. This opens a new and practical technical pathway for high-quality, explainable, and continuously evolvable requirements engineering.
