# ASE 2025 Research Track — AI for Software Engineering

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 45

## 1. AlignCoder: Aligning Retrieval with Target Intent for Repository-Level Code Completion

**Authors:** Tianyue Jiang (Sun Yat-sen University), Yanli Wang (Sun Yat-sen University), Yanlin Wang (Sun Yat-sen University), Daya Guo, Ensheng Shi (Huawei), Yuchi Ma (Huawei Cloud Computing Technologies), Jiachi Chen (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334411

**中文总结:** 提出 AlignCoder 仓库级代码补全框架，以多候选补全增强检索查询并用强化学习训练 AlignRetriever，缓解 RAG 检索与目标代码语义不对齐问题。

**Abstract:** Repository-level code completion remains a challenging task for existing code large language models (code LLMs) due to their limited understanding of repository-specific context and domain knowledge. While retrieval-augmented generation (RAG) approaches have shown promise by retrieving relevant code snippets as cross-file context, they suffer from two fundamental problems: misalignment between the query and the target code in the retrieval process, and the inability of existing retrieval methods to effectively utilize the inference information. To address these challenges, we propose AlignCoder, a repository-level code completion framework that introduces a query enhancement mechanism and a reinforcement learning based retriever training method. Our approach generates multiple candidate completions to construct an enhanced query that bridges the semantic gap between the initial query and the target code. Additionally, we employ reinforcement learning to train an AlignRetriever that learns to leverage inference information in the enhanced query for more accurate retrieval. We evaluate AlignCoder on two widely-used benchmarks (CrossCodeEval and RepoEval) across five backbone code LLMs, demonstrating an 18.1% improvement in EM score compared to baselines on the CrossCodeEval benchmark. The results show that our framework achieves superior performance and exhibits high generalizability across various code LLMs and programming languages.


## 2. Aligning LLMs to Fully Utilize the Cross-file Context in Repository-level Code Completion

**Authors:** Jia Li (Tsinghua University), Hao Zhu (Peking University), Huanyu Liu, Xianjie Shi (Peking University), He Zong (aiXcoder), Yihong Dong (Peking University), Kechi Zhang (Peking University, China), Siyuan Jiang, Zhi Jin (Peking University), Ge Li (Peking University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334425

**中文总结:** 提出 CoLA 长上下文对齐方法，构建含最长 128K tokens 跨文件上下文的 CoLA-132K 数据集，经两阶段训练使 LLM 更好利用跨文件 API 与相似代码片段完成仓库级补全。

**Abstract:** Large Language Models (LLMs) have shown promising results in repository-level code completion, which completes code based on the in-file and cross-file context of a repository. The cross-file context typically contains different types of information (e.g., relevant APIs and similar code) and is lengthy. In this paper, we found that LLMs struggle to fully utilize the information in the cross-file context. We hypothesize that one of the root causes of the limitation is the misalignment between pre-training (i.e., relying on nearby context) and repo-level code completion (i.e., frequently attending to long-range cross-file context).

To address the above misalignment, we propose \textbf{Co}de \textbf{L}ong-context \textbf{A}lignment - CoLA, a purely data-driven approach to explicitly teach LLMs to focus on the cross-file context. Specifically, CoLA constructs a large-scale repo-level code completion dataset - CoLA-132K, where each sample contains the long cross-file context (up to 128K tokens) and requires generating context-aware code (i.e., cross-file API invocations and code spans similar to cross-file context). Through a two-stage training pipeline upon CoLA-132K, LLMs learns the capability of finding relevant information in the cross-file context, thus aligning LLMs with repo-level code completion. We apply CoLA to multiple popular LLMs (e.g., aiXcoder-7B) and extensive experiments on CoLA-132K and a public benchmark - CrossCodeEval. Our experiments yield the following results. (1) \textit{Effectiveness.} CoLA substantially improves the performance of multiple LLMs in repo-level code completion. For example, it improves aiXcoder-7B by up to 19.7% in exact match. (2) \textit{Generalizability.} The capability learned by CoLA can generalize to new languages (i.e., languages not in training data). (3) \textit{Enhanced Context Utilization Capability.} We design two probing experiments, which show CoLA improves the capability of LLMs in utilizing the information (i.e., relevant APIs and similar code) in cross-file context. Our datasets and model weights are released in the replication package.


## 3. Amur: Fixing Multi-Resource Leaks Guided by Resource Flow Analysis

**Authors:** Jinyoung Kim (Sungkyunkwan University), Eunseok Lee (Sungkyunkwan University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334565

**中文总结:** 提出 Amur，基于资源流分析（RFA）静态识别泄漏点并约束 LLM 生成语义保持补丁，在 NJR-1 与 JLeaks 多资源泄漏基准上显著优于现有修复方法。

**Abstract:** Resource leaks pose a persistent threat to software reliability, resulting in resource exhaustion, performance degradation, and system crashes. Existing automated repair approaches, primarily based on rigid templates, are limited in handling complex or multi-resource leak scenarios and often compromise program semantics. Although recent advances in Large language models show promise in program repair, existing LLM-based methods frequently generate semantically invalid patches for resource leaks. This paper presents \textit{Amur}, a semantics-aware patching framework that leverages static analysis to guide LLMs in repairing both single- and multi-resource leaks. At the core of Amur is a novel \textit{Resource Flow Analysis (RFA)}, a flow-sensitive and inter-resource-aware static analysis that captures resource usage patterns and dependencies. RFA identifies potential leak points and enforces semantic constraints to guide LLMs in synthesizing semantics-preserving patches. We evaluate Amur on the NJR-1 dataset and the new \textbf{JLeaks} benchmark (ICSE 2024), which targets realistic multi-resource leak scenarios. Amur achieves substantial improvements over state-of-the-art methods, improving patch accuracy by 33% over RLFixer and 24% over LLM-only baselines in single-resource leak cases. For multi-resource leaks, Amur generates patches in 96% of cases and achieves 80% correctness, outperforming RLFixer and LLM-only baselines by 76% and 16%, respectively. These results demonstrate that integrating RFA into LLM-guided repair significantly enhances the correctness and generalizability of automated resource leak fixes.


## 4. An Agent-based Evaluation Framework for Complex Code Generation

**Authors:** Xinchen Wang (Harbin Institute of Technology), Pengfei Gao (ByteDance), Chao Peng (ByteDance), Ruida Hu (Harbin Institute of Technology, Shenzhen), Cuiyun Gao (Harbin Institute of Technology, Shenzhen)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334422

**中文总结:** 提出 CodeVisionary 智能体代码评估框架，先分解任务需求制定评估计划并逐步蒸馏多维度上下文，再对复杂多需求代码生成提供细粒度可解释评估。

**Abstract:** Large language models (LLMs) have demonstrated strong capabilities in code generation, underscoring the critical need for rigorous and comprehensive evaluation. Existing evaluation approaches fall into three categories, including human-centered, metric-based, and LLM-based. Considering that human-centered approaches are labour-intensive and metric-based ones overly rely on reference answers, LLM-based approaches are gaining increasing attention due to their stronger contextual understanding capabilities. However, they generally evaluate the generated code based on static prompts, and tend to fail for complex code scenarios which typically involve multiple requirements and require more contextual information. In addition, these approaches lack fine-grained evaluation for complex code, resulting in limited explainability.

To mitigate the limitations, we propose \textbf{CodeVisionary}, the first agent-based evaluation framework for complex code generation. CodeVisionary consists of two stages: \textbf{(1) \textit{Requirement-guided multi-dimensional context distillation stage}}, which first formulates a detailed evaluation plan by decomposing task requirements, and then stepwise collects multi-dimensional contextual information for each requirement. \textbf{(2) \textit{Fine-grained scoring and summarization stage}}, which defines self-directed and negotiation-based actions, allowing multiple judges to comprehend complex code from fine-grained and diverse viewpoints, and reach a consensus through discussion. A comprehensive evaluation report is also generated for enhanced explainability. For validation, we construct a new benchmark consisting of 363 samples spanning 37 coding scenarios and 23 programming languages. Extensive experiments demonstrate that \framework achieves the best performance among three baselines for evaluating complex code generation, outperforming the best baseline with average improvements of 0.217, 0.163, and 0.141 in Pearson, Spearman, and Kendall-Tau coefficients, respectively. The resources of CodeVisionary are available at https://anonymous.4open.science/r/CodeVisionary .


## 5. An LLM-based multi-agent framework for agile effort estimation

**Authors:** Long Bui (University of Wollongong), Hoa Khanh Dam (University of Wollongong), Rashina Hoda (Monash University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334617

**中文总结:** 提出 LLM 多智能体敏捷工时估算框架，可与开发者及其他 agent 协调讨论并达成共识；在真实数据集上多数指标优于 SOTA，从业者协作体验积极。

**Abstract:** Effort estimation is a crucial activity in agile software development, where teams collaboratively review, discuss, and estimate the effort required to complete user stories in a product backlog. Current practices in agile effort estimation heavily rely on subjective assessments, leading to inaccuracies and inconsistencies in the estimates. While recent machine learning-based methods show promising accuracy, they cannot explain or justify their estimates and lack the capability to interact with human team members. Our paper fills this significant gap by leveraging the powerful capabilities of Large Language Models (LLMs). We propose a novel LLM-based multi-agent framework for agile estimation that not only can produce estimates, but also can coordinate, communicate and discuss with human developers and other agents to reach a consensus. Evaluation results on a real-life dataset show that our approach outperforms state-of-the-art techniques across all evaluation metrics in the majority of the cases. Our human study with software development practitioners also demonstrates an overwhelmingly positive experience in collaborating with our agents in agile effort estimation.


## 6. Automated Repair of Ambiguous Problem Descriptions for LLM-Based Code Generation

**Authors:** Haoxiang Jia (Peking University), Robbie Morris (University College London), He Ye (University College London (UCL)), Federica Sarro (University College London), Sergey Mechtaev (Peking University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334557

**中文总结:** 将模糊 NL 需求修复分解为程序分布分析与基于 IO 示例的需求对齐两阶段，避免直接让 LLM 做元认知式歧义消解，以降低 LLM 代码生成的解释不确定性。

**Abstract:** The widespread adoption of large language models (LLMs) in software engineering has amplified the role of natural language (NL). However, the inherent ambiguity of NL threatens software quality, because ambiguous requirements may lead to faulty program generation. The complexity of ambiguity detection and resolution motivates us to introduce the problem of automated repair of ambiguous NL requirements, which we approach by reducing code generation uncertainty and aligning NL with input-output examples.

Repairing ambiguity in requirements is a difficult challenge for LLMs, as it demands metacognition — the model must understand how its own interpretation changes when the text is altered. Our experiments show that directly prompting an LLM to detect and resolve ambiguities results in irrelevant or inconsistent clarifications. The key novelty we propose is a method of decomposing this problem into simpler sub-problems that do not require metacognitive reasoning. First, we analyze and repair the LLM’s interpretation of requirements embodied by the distribution of programs they induce using traditional testing and program repair methods. Second, we repair requirements based on the changes to the distribution via what we refer to as contrastive specification inference. This decomposition enables targeted, minimal requirement repairs that yield cross-model performance gains in code generation.

This approach is implemented as the tool SpecFix, and evaluated using three state‐of‐the‐art LLMs, GPT-4o, DeepSeek-V3 and Qwen2.5-Coder-32b-Instruct, across two widely used code generation benchmarks: HumanEval+ and MBPP+. Our results show that SpecFix, operating autonomously without human intervention or external information, modifies 23.93% of the requirements, leading to a 33.66% improvement in model Pass@1 on the modified requirements. Across the entire benchmark, this corresponds to an absolute increase of 4.3% in overall Pass@1.


## 7. Automated Repair of OpenID Connect Programs

**Authors:** Tamjid Al Rahat (UCLA), Yanju Chen (University of California, San Diego), Yu Feng (University of California at Santa Barbara), Yuan Tian

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334406

**中文总结:** 提出 AuthFix 反例引导的 OpenID Connect 程序修复引擎，结合 LLM 补丁合成与 Petri 网模型检验验证；在 23 个 OpenID 缺陷中 74%（17 个）生成语义等价于开发者补丁的正确修复。

**Abstract:** OpenID Connect has revolutionized single sign-on (SSO)-based online authentication by providing a secure and convenient method for accessing multiple services with a single set of credentials. Despite its widespread adoption, critical security bugs in OpenID Connect have resulted in significant financial losses and security breaches, highlighting the need for robust mitigation strategies. Automated program repair presents a promising solution for generating candidate patches for OpenID programs. However, challenges such as domain-specific complexities and the necessity for precise fault localization and patch verification must be addressed. We propose AuthFix, a counter-example guided repair engine leveraging LLMs for automated OpenID bug fixing. AuthFix integrates three key components: fault localization, patch synthesis, and patch verification. By employing a novel Petri-net-based model checker, AuthFix ensures the correctness of patches through effective interaction modeling. Our evaluation on a dataset of OpenID bugs demonstrates that AuthFix successfully generates correct patches for 17 out of 23 bugs (74%), with a high percentage of semantic equivalence to manual developer patches.


## 8. Automatic Fixing of Missing Dependency Errors

**Authors:** Jun Lyu (Nanjing University), He Zhang (Nanjing University), Lanxin Yang (Nanjing University), Yue Li (Nanjing University), Chenxing Zhong (Nanjing University), Manuel Rigger (National University of Singapore)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334645

**中文总结:** 提出 MDfixer，基于声明图与距离度量识别 Makefile 依赖声明风格，为缺失依赖（MD）错误生成同风格补丁，应对 Makefile 复杂语义与多样声明方式带来的自动修复难题。

**Abstract:** Many build systems, such as Make, rely on build scripts that are written by users to specify dependencies. As a serious dependency error in Makefiles, Missing Dependencies (MDs) can result in compiling and linking outdated artifacts in incremental builds, preventing software project updates from being applied correctly. Many studies have explored the detection of MDs. Automatically fixing those missing build dependency errors has become an apparent but challenging task. The challenges mainly result from Makefiles having complex semantics and project maintainers declaring dependencies in a variety of ways. To address these challenges, we propose a new approach to fixing MDs called MDfixer. The core idea of MDfixer is to identify the dependency declaration style in a Makefile and generate patches for the same declaration style based on declaration graphs and automatic prompt generation. Specifically, MDfixer locates dependency declarations for targets that have errors in the Makefile based on error reports, and then builds a declaration graph for each build target with errors and identifies the target’s declaration style based on a distance metric between the target and the dependencies. Based on the declaration graph and automatic prompt generation, MDfixer generates patches with the same style for the dependencies that need to be added. We evaluated the effectiveness and efficiency of MDfixer with 25 well-known projects. The evaluation results show that MDfixer can fix all of MDs. We submitted fixes for 620 individual dependency issues across 7 projects, with six of them merging our pull requests, resulting in a total of 581 errors being fixed. MDfixer consumes an average time of 1.31 min for fixing a project, with a median of 0.013s. It can assist practitioners in the effective and efficient fixing of MDs.


## 9. Can Mamba Be Better? An Experimental Evaluation of Mamba in Code Intelligence

**Authors:** Shuo Liu (City University of Hong Kong), Jacky Keung (City University of Hong Kong), Zhen Yang (Shandong University), Zhenyu Mao (City University of Hong Kong), Yicheng Sun (City University of Hong Kong)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334474

**中文总结:** 首次系统评估 Mamba/Mamba-2 在代码补全与生成任务上的效果与效率；全量微调、PEFT 及代码语料预训练下均 consistently 优于同等规模 Transformer 基线。

**Abstract:** The Transformer architecture and its core attention mechanism form the foundation of Code Language Models (code LMs) and have driven their remarkable progress across a wide range of code intelligence tasks. However, the quadratic complexity inherent in the attention mechanism poses scalability challenges. Recently, subquadratic architectures such as Mamba and Mamba-2 have emerged as compelling alternatives to the Transformer. While they have shown promising results and attracted increasing academic interest, their effectiveness in code intelligence tasks remains unexplored.

To fill this gap, we present the first experimental evaluation of Mamba-based models on two representative code intelligence tasks: line-level code completion and code generation, delving into their effectiveness and efficiency. We begin by evaluating Mamba and Mamba-2 under both full Fine-Tuning (FT) and Parameter-Efficient Fine-Tuning (PEFT) settings. We further pre-train the models on code corpora to boost their capacity in code comprehension. Our results consistently show that Mamba-based models outperform their Transformer-based counterparts. Furthermore, to explore whether the observed superiority stems from the Mamba architecture and to mitigate the influence of varying pre-training datasets, we pre-train CodeGPT, Mamba, and Mamba-2 from scratch on identical code corpora. Our findings reveal that the Mamba-2 block achieves the highest capability in code modeling. Besides, Mamba-based blocks exhibit advantages in terms of memory efficiency. We also evaluate performance in low-resource scenarios and at larger model scales, where Mamba-based models demonstrate consistent robustness. This work provides a comprehensive investigation into Mamba-based models in the context of code intelligence, uncovering their strengths and promising potential for future applications.


## 10. Characterizing Multi-Hunk Patches: Divergence, Proximity, and LLM Repair Challenges

**Authors:** Noor Nashid (University of British Columbia), Daniel Ding (University of British Columbia), Keheliya Gallaba (Centre for Software Excellence), Ahmed E. Hassan (Queen’s University), Ali Mesbah (University of British Columbia)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334668

**中文总结:** 基于 372 个真实缺陷构建多 hunk 补丁数据集 HUNK4J，提出 hunk divergence 与空间邻近度分类刻画跨文件编辑复杂度；对六种 LLM 的实证显示修复成功率随 divergence 与空间分散度上升而下降，最分散 Fragment 类纯 LLM 无一成功。

**Abstract:** Multi-hunk bugs, where fixes span disjoint regions of code, are common in practice, yet remain underrepresented in automated repair. Existing techniques and benchmarks pre-dominantly target single-hunk scenarios, overlooking the added complexity of coordinating semantically related changes across the codebase. In this work, we characterize HUNK4J, a dataset of multi-hunk patches derived from 372 real-world defects. We propose hunk divergence, a metric that quantifies the variation among edits in a patch by capturing lexical, structural, and file-level differences, while incorporating the number of hunks involved. We further define spatial proximity, a classification that models how hunks are spatially distributed across the program hierarchy. Our empirical study spanning six LLMs reveals that model success rates decline with increased divergence and spatial dispersion. Notably, when using the LLM alone, no model succeeds in the most dispersed Fragment class. These findings highlight a critical gap in LLM capabilities and motivate divergence-aware repair strategies.


## 11. Code-DiTing: Automatic Evaluation of Code Generation without References or Test Cases

**Authors:** Guang Yang, Yu Zhou (Nanjing University of Aeronautics and Astronautics), Xiang Chen (Nantong University), Wei Zheng (Northwestern Polytechnical University), Xing Hu (Zhejiang University), Xin Zhou (Singapore Management University, Singapore), David Lo (Singapore Management University), Taolue Chen (Birkbeck, University of London)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334693

**中文总结:** 系统评估 LLM-as-Judge 代码评测方法的优劣后，提出 CODE-DITING，以数据蒸馏框架在无需参考解或测试用例的情况下兼顾准确性、效率与可解释性，平衡通用模型与推理模型的各自局限。

**Abstract:** Trustworthy evaluation methods for code snippets play a crucial role in neural code generation. Traditional methods, which either rely on reference solutions or require executable test cases, have inherent limitation in flexibility and scalability. The recent LLM-as-Judge methodology offers a promising alternative by directly evaluating functional consistency between the problem description and the generated code. To systematically understand the landscape of these LLM-as-Judge methods, we conduct a comprehensive empirical study across three diverse datasets. Our investigation reveals the pros and cons of two categories of LLM-as-Judge methods: the methods based on general foundation models can achieve good performance but require complex prompts and lack explainability, while the methods based on reasoning foundation models provide better explainability with simpler prompts but demand substantial computational resources due to their large parameter sizes.

To address these limitations, we propose CODE-DITING, a novel code evaluation method that balances accuracy, efficiency and explainability. We develop a data distillation framework that effectively transfers reasoning capabilities from DeepSeek-R1671B to our CODE-DITING 1.5B and 7B models, significantly enhancing evaluation explainability and reducing the computational cost. With the majority vote strategy in the inference process, CODE-DITING 1.5B outperforms all models with the same magnitude of parameters and achieves performance which would normally exhibit in a model with 5 times of parameter scale. CODE-DITING 7B surpasses GPT-4o and DeepSeek-V3 671B, even though it only uses 1% of the parameter volume of these large models. Further experiments show that CODEDITING is robust to preference leakage and can serve as a promising alternative for code evaluation.


## 12. Coding-Fuse: Efficient Fusion of Code Pre‑Trained Models for Classification Tasks

**Authors:** Yu Zhao, Lina Gong (Nanjing University of Aeronautics and Astronautic), Zhiqiu Huang (Nanjing University of Aeronautics and Astronautics), Yuchen Jin (Nanjing University of Aeronautics and Astronautics), Mingqiang Wei (Nanjing University of Aeronautics and Astronautics)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334555

**中文总结:** 发现融合多个代码预训练模型可显著提升 SE 分类任务性能但带来微调与推理开销；提出 Coding-Fuse，以证据理论评估各层输出特征适配性，实现更绿色高效的代码 PTM 融合框架。

**Abstract:** Software engineering (SE) classification tasks play a vital role in improving software quality. Nevertheless, SE researchers and practitioners tend to rely on a single code pre-trained model (PTM) for downstream classification tasks. Previous studies have found that different code PTMs yield different performance in SE classification tasks, which triggers our thinking of whether the integration of multiple code PTMs improves the performance of classification tasks. Therefore, we first conduct preliminary exploratory research to analyze the impact of fusing multiple PTMs on code classification tasks. The result shows that compared to the single code PTM, the fusion of multiple code PTMs can significantly improve the performance of SE classification tasks. However, the performance improvement also brings about the problem of increased finetuning resources and reduced reasoning efficiency, which does not meet the greenness requirements. In order to address these issues, we propose Coding-Fuse, a framework of efficient fusion of code PTMs for SE classification tasks. Coding-Fuse first introduces evidence theory to evaluate the adaptability of the output features of each layer of code PTMs and data labels, and locates the potential best performance layer of different code PTMs. Then, Coding-Fuse uses a soft voting strategy to fuse the outputs of these layers to obtain a new model. We conduct experiments for effectiveness by comparing Coding-Fuse with the full PTM fusion method and the original single PTM using five different code PTMs on three different SE classification tasks and two task scenarios. The results show that Coding-Fuse can achieve better performance than the full PTM fusion method with higher efficiency and fewer hardware resources, and can achieve better performance than the original single PTM at the same efficiency and hardware resource level. We encourage SE practitioners to use our Coding-Fuse method in practice to fully utilize the advantages of each code PTM in the PTM repository according to task requirements to easily create new SE intelligent PTMs to achieve performance and greenness improvements.


## 13. Coverage-Based Harmfulness Testing for LLM Code Transformation

**Authors:** Honghao Tan (Concordia University), Haibo Wang (Concordia University), Diany Pressato (Concordia University), Yisen Xu (Software PErformance, Analysis, and Reliability (SPEAR) lab, Concordia University, Montreal, Canada), Shin Hwei Tan (Concordia University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334609

**中文总结:** 发现 Code LLM 程序变换可经 32 类操作向源码注入有害内容；提出覆盖引导框架 CHT，用多样化有害关键词模板合成提示并对生成输出做危害度量，而非仅检测内容审核是否被绕过。

**Abstract:** Harmful content embedded in program elements within source code may have detrimental impact on mental health of software developers, and promote harmful behavior. Our key insight is that software developers may introduce harmful content into source code when using Code Large Language Models (Code LLMs) to perform program transformations tasks. To understand the space of program transformations that may be used to introduce harmful content into auto-generated code, we conduct a preliminary study that revealed 32 different types of transformations that can be used to introduce harmful content in source code. Based on our study, we propose CHT, a novel coverage-guided harmfulness testing framework that automatically synthesizes prompts using a set of prompt templates injected with diverse harmful keywords to perform various types of transformations on a set of mined benign programs. Instead of checking if the content moderation has been bypassed as prior approaches, CHT performs output damage measurement to assess potential harm that can be introduced by the generated outputs (i.e., natural language explanation and modified code). By considering output damage, CHT revealed several problems in Code LLMs: (1) bugs in content moderation for code (Code LLMs produce the harmful code without providing any warning), (2) inadequacy in performing code-related task (e.g., Code LLMs may resort to explaining the given code instead of performing the instructed transformation task), and (3) lenient content moderation (gives warning but the modified code with harmful content is still produced). Our evaluations of CHT on four Code LLMs and gpt-4o-mini (general LLM) show that content moderation in Code LLMs is relatively easy to bypass where LLMs may generate harmful keywords embedded within identifier names or code comments without giving any warning (65.93% in our evaluation). To improve the robustness of content moderation in code-related tasks, we propose a two-phrase approach that checks if the prompt contains any harmful content before generating any output. Our evaluation shows that our proposed approach improves the content moderation of Code LLM by 483.76%.


## 14. Defects4C: Benchmarking Large Language Model Repair Capability with C/C++ Bugs

**Authors:** Jian Wang (Nanyang Technological University), Xiaofei Xie (Singapore Management University), Qiang Hu (Tianjin University), Shangqing Liu (Nanjing University), Jiongchi Yu (Singapore Management University), Jiaolong Kong (Singapore Management University), Yi Li (Nanyang Technological University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334503

**中文总结:** 发布 C/C++ 程序修复基准 Defects4C，含 900 万条缺陷相关提交、248 个高质量缺陷函数、102 个漏洞函数及可复现测试；并据此评估 24 个 SOTA LLM 的修复能力，填补 Java Defects4J 以外 APR 评测空白。

**Abstract:** Automated Program Repair (APR) plays a critical role in enhancing the quality and reliability of software systems. While substantial progress has been made in Java-based APR, largely facilitated by benchmarks like Defects4J, there remains a significant gap in research on C/C++ program repair, despite the widespread use of C/C++ and the prevalence of associated vulnerabilities. This gap is primarily due to the lack of high-quality, open-source benchmarks tailored for C/C++.

To address this issue, we introduce \textbf{\textit{Defects4C}}, a comprehensive and executable benchmark specifically designed for C/C++ program repair. Our dataset is constructed from real-world C/C++ repositories and includes a large collection of bug-relevant commits (\textbf{9M} in total), \textbf{248} high-quality buggy functions, and \textbf{102} vulnerable functions, all paired with test cases for reproduction. These resources enable rigorous evaluation of repair techniques and support the retraining of learning-based approaches for enhanced performance.

Using \textbf{\textit{Defects4C}}, we conduct a comprehensive empirical study evaluating the effectiveness of \textbf{24} state-of-the-art large language models (LLMs) in repairing C/C++ faults. Our findings offer valuable insights into the strengths and limitations of current LLM-based APR techniques in this domain, highlighting both the need for more robust methods and the critical role of Defects4C in advancing future research.


## 15. DLBENCH: A Comprehensive Benchmark for SQL Translation with Large Language Models

**Authors:** Li Lin (Xiamen University), Hongqiao Chen (School of Informatics, Xiamen University), Qinglin Zhu (School of Informatics, Xiamen University), Liehang Chen (School of Informatics, Xiamen University), Linlong Tang (School of Informatics, Xiamen University), Rongxin Wu (Xiamen University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334627

**中文总结:** 发布首个面向 LLM 的 SQL 方言翻译综合基准 DLBENCH，含 BIRDTRANS（七个 DBMS 真实查询场景）与 BUTTERTRANS（更广 SQL 类型与方言特性），经多步清洗与 LLM/人工标注保证翻译质量。

**Abstract:** In recent years, the growing complexity of database management systems (DBMSs) and the proliferation of SQL dialects have created significant challenges for database migration, federation, and integration. These challenges arise from the disparities between SQL dialects across different DBMSs, hindering seamless communication and system interoperability. SQL translation, the process of converting SQL queries from a source dialect DBMS to a target dialect DBMS, plays a crucial role in addressing these challenges. To facilitate this process, we introduce DLBENCH, the first comprehensive benchmark designed to evaluate the SQL translation capabilities of Large Language Models (LLMs). The benchmark includes two datasets: BIRDTRANS, which covers real-world database query scenarios across seven DBMSs, and BUTTERTRANS, which spans a broader spectrum of SQL types and encompasses extensive DBMS dialect features. We collect high-quality databases and SQL statements, applying a rigorous multi-step cleaning process that ensures data quality through SQL-92–based checks and dialect-specific parser validation. Additionally, both LLM-based and human annotations are used to guarantee the correctness and completeness of the dataset. We demonstrate the utility of DLBENCH through extensive experiments, which show that the benchmark effectively evaluates the SQL translation ability of LLMs. The results highlight the potential of LLMs for SQL translation tasks and provide insights into areas for further improvement.


## 16. Effective Code Membership Inference for Code Completion Models via Adversarial Prompts

**Authors:** Yuan Jiang (Harbin Institute of Technology), Zehao Li (Harbin Institute of Technology), Shan Huang (Harbin Institute of Technology), Christoph Treude (Singapore Management University), Xiaohong Su (Harbin Institute of Technology), Tiantian Wang (Harbin Institute of Technology)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334379

**中文总结:** 提出 AdvPrompt-MIA，用代码专用对抗 prompt 诱发补全模型输出变化并训练分类器推断训练集成员身份，在 Code Llama 7B 等模型上较现有黑/灰盒 MIA 更准确捕捉 over-parameterized 代码模型的 memorization 模式。

**Abstract:** Membership inference attacks (MIAs) on code completion models offer an effective way to assess privacy risks by inferring whether a given code snippet was part of the training data. Existing black- and gray-box MIAs rely on expensive surrogate models or manually crafted heuristic rules, which limit their ability to capture the nuanced memorization patterns exhibited by over-parameterized code language models. To address these challenges, we propose AdvPrompt-MIA, a method specifically designed for code completion models, combining code-specific adversarial perturbations with deep learning. The core novelty of our method lies in designing a series of adversarial prompts that induce variations in the victim code model’s output. By comparing these outputs with the ground-truth completion, we construct feature vectors to train a classifier that automatically distinguishes member from non-member samples. This design allows our method to capture richer memorization patterns and accurately infer training set membership. We conduct comprehensive evaluations on widely adopted models, such as Code Llama 7B, over the APPS and HumanEval benchmarks. The results show that our approach consistently outperforms state-of-the-art baselines, with AUC gains of up to 102%. In addition, our method exhibits strong transferability across different models and datasets, underscoring its practical utility and generalizability.


## 17. EfficientEdit: Accelerating Code Editing via Edit-Oriented Speculative Decoding

**Authors:** Peiding Wang (Beihang university), Li Zhang (Beihang University), Fang Liu (Beihang University), Yinghao Zhu (Beihang University), Wang Xu (Tsinghua University), Lin Shi (Beihang University), Xiaoli Lian (Beihang University, China), Minxiao Li (Beihang university), Bo Shen (Huawei Cloud Computing Technologies Co., Ltd.), Binzhang Fu (Huawei Technologies, n.n.)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334358

**中文总结:** 提出 EfficientEdit，针对代码编辑局部变更特点，在 speculative decoding 中复用原代码片段并由 edit-oriented draft 模型生成草稿，配合动态验证机制；在 CanItEdit 等任务上相对自回归解码最高加速 10.38×–13.09×。

**Abstract:** Large Language Models (LLMs) have demonstrated remarkable capabilities in code editing, substantially enhancing software development productivity. However, the inherent complexity of code editing tasks forces existing approaches to rely on LLMs’ autoregressive end-to-end generation, where decoding speed plays a critical role in efficiency. While inference acceleration techniques like speculative decoding are applied to improve the decoding efficiency, these methods fail to account for the unique characteristics of code editing tasks where changes are typically localized and existing code segments are reused. To address this limitation, we propose EfficientEdit, a novel method that improves LLM-based code editing efficiency through two key mechanisms based on speculative decoding: (1) effective reuse of original code segments while identifying potential edit locations, and (2) efficient generate edit content via high-quality drafts from edit-oriented draft models and a dynamic verification mechanism that balances quality and acceleration. Experimental results show that EfficientEdit can achieve up to 10.38× and 13.09× speedup compared to standard autoregressive decoding in CanItEdit and CodeIF-Bench, respectively, outperforming state-of-the-art inference acceleration approaches by up to 90.6%. The code and data are available at the anonymous link: https://anonymous.4open.science/r/EfficientEdit .


## 18. Enhancing LLM to Decompile Optimized PTX to Readable CUDA for Tensor Programs

**Authors:** Xinyu Sun (University of Science and Technology of China), Fugen Tang (University of Science and Technology of China), Yu Zhang (University of Science and Technology of China), Han Shen (Kuaishou Technology), Chengru Song (Kuaishou Technology), Di Zhang (Kuaishou Technology)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334294

**中文总结:** 提出 PtxDec，通过编译器数据增强构建 40 万 CUDA-PTX 对齐训练集，并引入 Rolled-PTX 中间表示（启发式循环重卷），显著增强 LLM 将高度优化 PTX 反编译为可读 CUDA 的能力。

**Abstract:** The growing demand for high-performance tensor programs on GPUs, especially for large language models (LLMs), necessitates advanced compilation and optimization techniques. However, the critical task of analyzing optimized, low-level PTX code for performance tuning or understanding poses significant challenges. While LLMs hold promise for PTX-to-CUDA decompilation to improve code intelligibility, their effectiveness is severely limited by the scarcity of aligned training data and the inherent complexity of highly optimized, unrolled PTX code.

In this work, we explore methodologies to significantly enhance LLM capabilities for accurate and readable PTX-to-CUDA decompilation and present PtxDec, a decompilation prototype implementing our approach. To overcome the critical barrier of data scarcity, we develop a compiler-based data augmentation framework coupled with rigorous post-processing, enabling the creation of a large-scale, high-quality dataset of 400K aligned CUDA-PTX kernel pairs for effective LLM training. Furthermore, to empower LLMs to handle the complexity of optimized PTX, we introduce Rolled-PTX—an intermediate representation generated through heuristic loop rerolling during preprocessing. Rolled-PTX condenses unrolled patterns, drastically simplifying the input structure presented to the LLM and aligning it better with higher-level loop constructs.

Comprehensive evaluation demonstrates that PtxDec achieves substantial performance gains: our approach yields a 2.3×–3.1× improvement in functional accuracy over baseline methods, alongside significant enhancements in generated code readability and scheduling consistency with the original optimized kernels. Ablation studies further validate the contribution of each proposed component to the overall performance.

To the best of our knowledge, this is the first work tackling PTX-to-CUDA decompilation, specifically focusing on and demonstrating effective strategies for augmenting LLMs to overcome the key challenges in this domain.


## 19. Evaluating and Improving Framework-based Parallel Code Completion with Large Language Models

**Authors:** Ke Liu, Qinglin Wang (Shandong Normal University), Xiang Chen (Nantong University), Guang Yang, YiGui Feng (National University of Defense Technology), Gencheng Liu (National University of Defense Technology), Jie Liu (Institute of Software, Chinese Academy of Sciences)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334593

**中文总结:** 形式化框架级并行代码补全（FPCC）三子任务，构建覆盖六种并行框架的 16,615 对高质量数据集；实验显示主流 LLM 在 FPCC 上表现较差，并提出针对性改进方法以提升插入点识别与指令补全准确率。

**Abstract:** Modern computing architectures (e.g., multi-core CPUs, GPUs, distributed systems) rely on parallel code implemented via frameworks such as OpenMP, MPI, and CUDA. While large language models (LLMs) have shown strong performance in general code generation, they struggle with the structured reasoning required for parallel programming, such as handling concurrency, synchronization, and framework-specific semantics. In practical parallel code development, a common workflow begins with sequential code and incrementally introduces parallel directive codes. We formalize this process as the task of \textbf{framework-based parallel code completion} (FPCC), which involves three subtasks: identifying insertion points, selecting parallel frameworks, and completing parallel directive codes.

To support this task, we construct a high-quality dataset of 16,615 framework-based parallel code pairs across six widely used frameworks, labeled with directive points, parallel frameworks, and the code of parallel directives. Empirical results show that six popular LLMs perform poorly on FPCC, particularly struggling with identifying insertion points and completing correct directive codes.

To address these limitations, we propose HPCL, a curriculum-based fine-tuning framework that progressively improves model capabilities in insertion point identification, parallel framework selection, and parallel directive code completion. Our approach achieves substantial improvements, yielding an 17.82% increase in EM and a 5.43% improvement in DIR scores over LLM-based baselines. Finally, expert-guided error analysis reveals common failure patterns and suggests future directions in retrieval-augmented completion and consistency-aware training.


## 20. FastCoder: Accelerating Repository-level Code Generation via Efficient Retrieval and Verification

**Authors:** Qianhui Zhao (Beihang University), Li Zhang (Beihang University), Fang Liu (Beihang University), Xiaoli Lian (Beihang University, China), Meng Qiaoyuanhe (Beihang University), Ziqian Jiao (Beihang University), Zetong Zhou (Beihang University), Jia Li, Lin Shi (Beihang University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334326

**中文总结:** 提出 FastCoder，面向仓库级代码生成采用 draft-verification 范式，构建多源 datastore 做高效检索与验证；在不牺牲生成质量的前提下显著降低 LLM 推理延迟。

**Abstract:** Code generation is a latency-sensitive task that demands high timeliness. However, with the growing interest and inherent difficulty in repository-level code generation, most existing code generation studies focus on improving the correctness of generated code while overlooking the inference efficiency, which is substantially affected by the overhead during LLM generation. Although there has been work on accelerating LLM inference, these approaches are not tailored to the specific characteristics of code generation, instead treating code the same as natural language sequences and ignoring its unique syntax and semantic characteristics, which are also crucial for improving efficiency. Consequently, these approaches exhibit limited effectiveness in code generation tasks, particularly for repository-level scenarios with considerable complexity and difficulty. To alleviate this issue, following draft-verification paradigm, we propose FastCoder, a simple yet highly efficient inference acceleration approach specifically designed for code generation, without compromising the quality of the output. FastCoder constructs a multi-source datastore, providing access to both general and project-specific knowledge, facilitating the retrieval of high-quality draft sequences. Moreover, FastCoder reduces the retrieval cost by controlling retrieval timing, and enhances efficiency through parallel retrieval and a context- and LLM preference-aware cache. Experimental results show that FastCoder can reach up to $2.53 \times$ and $2.54\times$ speedup compared to autoregressive decoding in repository-level and standalone code generation tasks, respectively, outperforming state-of-the-art inference acceleration approaches by up to $88%$. FastCoder can also be integrated with existing correctness-focused code generation approaches to accelerate the LLM generation process, and reach a speedup exceeding $2.6 \times$.


## 21. FGIT: Fault-Guided Fine-Tuning for Code Generation

**Authors:** Lishui Fan (Zhejiang University), Zhongxin Liu (Zhejiang University), Haoye Wang (Hangzhou City University), Lingfeng Bao (Zhejiang University), Xin Xia (Zhejiang University), Shanping Li (Zhejiang University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334630

**中文总结:** 提出 FGIT（Fault-Guided Fine-Tuning），提取正确与相似错误实现的多粒度差异并动态加权损失以强调易错片段；在 7 个 LLM、3 个 benchmark 上 pass@1 平均相对提升 6.9%。

**Abstract:** Modern instruction-tuned large language models (LLMs) have made remarkable progress in code generation. However, these LLMs fine-tuned with standard supervised fine-tuning (SFT) sometimes generate plausible-looking but functionally incorrect code variants. This issue likely stems from the limitation of standard SFT, which treats all tokens equally during optimization and fails to emphasize the error-sensitive segments—specific code differences between correct implementations and similar incorrect variants. To address this problem, we propose \underline{F}ault-\underline{G}uided F\underline{i}ne-\underline{T}uning (\FGit), a novel fine-tuning technique that enhances LLMs’ code generation by (1) extracting multi-granularity (line/token-level) differences between correct and incorrect yet similar implementations to identify error-sensitive segments, and (2) dynamically prioritizing those segments during training via dynamic loss weighting. Through extensive experiments on seven LLMs across three widely-used benchmarks, our method achieves an average relative improvement of 6.9% on pass@1, with some enhanced 6.7B LLMs outperforming closed-source models, e.g., GPT-3.5-Turbo. Furthermore, our fine-tuning technique demonstrates strong generalization with performance improvements ranging from 3.8% to 19.1% across diverse instruction-tuned LLMs, and our ablation studies confirm the contributions of different granularities of differences and hyperparameters.


## 22. Fixing Broken Graphs: LLM-Powered Automatic Code Optimization for DNN Programs

**Authors:** Haotian Wang (Nankai University), Yicheng Sui (Nankai University), Yudong Xie (Nankai University), Yicong Liu (Nankai University), Yufei Sun (Nankai University), Changqing Shi (Nankai University), Yuzhi Zhang (Nankai University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334418

**中文总结:** 提出 GraphGlue 多智能体系统，用 graph-break cause mining 定位 DNN 程序图断裂原因，并以 self-correction with reject sampling 修复代码使深度学习编译器完整捕获计算图；优化后平均加速 1.23x、最高 2.19x。

**Abstract:** Deep learning compilers optimize DNN program execution by capturing them as operator-based computation graphs. However, developers’ deep learning programs often contain complex Python language features that prevent compilers from recognizing the entire program as a complete computation graph, resulting in sub-optimal performance. Our analysis reveals that actual capture failures involve only a few lines of code, we believe this problem can be addressed through code repair rather than extensive compiler improvements. To address this challenge, we introduce GraphGlue, a multi-agent system that leverages LLMs to repair and optimize DNN programs for compiler requirements, thereby maximizing the performance benefits of deep learning compilers. GraphGlue employs (1) graph-break cause mining (GCM) to identify hidden causes of computation graph breaks and facilitate LLM-based repair, and (2) self-correction with reject sampling (SRS) to alternate between code debugging and regeneration, effectively avoiding ineffective feedback attempts caused by incorrect initial optimization strategies. Experimental results demonstrate that programs optimized by GraphGlue achieve up to 2.19x (1.23x on average) speedup compared to using TorchDynamo directly, and deliver up to 15.77x (8.74x on average) memory savings compared to state-of-the-art AI compiler frontends. GraphGlue exhibits strong generalization capabilities across 1,411 real-world user programs, successfully optimizing 92.63% of them. Code is available at https://anonymous.4open.science/r/GraphGlue-5163/ .


## 23. Forcrat: Automatic I/O API Translation from C to Rust via Origin and Capability Analysis

**Authors:** Jaemin Hong (KAIST), Sukyoung Ryu (KAIST)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334512

**中文总结:** 提出 Forcrat，通过 origin/capability 分析与 error source 分析，将 C2Rust 生成代码中的 libc I/O API 自动替换为语义等价的 Rust std 实现，解决两套 I/O 类型与错误处理机制不一致的迁移难题。

**Abstract:** Translating C to Rust is a promising way to enhance the reliability of legacy system programs. Although the industry has developed an automatic C-to-Rust translator, C2Rust, its translation remains unsatisfactory. One major reason is that C2Rust retains C standard library (libc) function calls instead of replacing them with functions from the Rust standard library (Rust std). However, little work has been done on replacing library functions in C2Rust-generated code. In this work, we focus on replacing the I/O API, an important subset of library functions. This poses challenges due to the semantically different designs of I/O APIs in libc and Rust std. First, the two APIs offer different sets of types that represent the \emph{origins} (e.g., standard input, files) and \emph{capabilities} (e.g., read, write) of streams used for I/O. Second, they use different error-checking mechanisms: libc uses internal indicators, while Rust std uses return values. To address these challenges, we propose two static analysis techniques, \emph{origin and capability analysis} and \emph{error source analysis}, and use their results to replace the I/O API. Our evaluation shows that the proposed approach is (1) correct, with all 32 programs that have test suites passing the tests after transformation, (2) efficient, analyzing and transforming 422k LOC in 14 seconds, and (3) widely applicable, replacing 82% of I/O API calls.


## 24. Hierarchical Knowledge Injection for Improving LLM-based Program Repair

**Authors:** Ramtin Ehsani (Drexel University), Esteban Parra Rodriguez (Belmont University), Sonia Haiduc (Florida State University), Preetha Chatterjee (Drexel University, USA)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334717

**中文总结:** 提出分层知识注入框架，依次注入 Bug、Repository、Project 三层结构化上下文增强 LLM 程序修复；在 BugsInPy 314 bug 上 Llama 3.3 修复率达 79%，比仅局部上下文提升 23%。

**Abstract:** Prompting LLMs with bug-related context (e.g., error messages, stack traces) improves automated program repair, but many bugs still remain unresolved. In real-world projects, developers often rely on broader repository and project-level context beyond the local code to resolve such bugs. In this paper, we investigate how automatically extracting and providing such knowledge can improve LLM-based program repair. We propose a layered knowledge injection framework that incrementally augments LLMs with structured context. It starts with the Bug Knowledge Layer, which includes information such as the buggy function and failing tests; expands to the Repository Knowledge Layer, which adds structural dependencies, related files, and commit history; and finally injects the Project Knowledge Layer, which incorporates relevant details from documentation and previously fixed bugs. We evaluate this framework on a dataset of 314 bugs from BugsInPy using two LLMs (Llama 3.3 and GPT-4o-mini), and analyze fix rates across six bug types. By progressively injecting knowledge across layers, our approach achieves a fix rate of 79% (250/314) using Llama 3.3, a significant improvement of 23% over previous work. All bug types show improvement with the addition of repository-level context, while only a subset benefit further from project-level knowledge, highlighting that different bug types require different levels of contextual information for effective repair. We also analyze the remaining unresolved bugs and find that more complex and structurally isolated bugs, such as Program Anomaly and GUI bugs, remain difficult even after injecting all available information. Our results show that layered context injection improves program repair and suggest the need for interactive and adaptive APR systems.


## 25. iKnow: an Intent-Guided Chatbot for Cloud Operations with Retrieval-Augmented Generation

**Authors:** Junjie Huang (The Chinese University of Hong Kong), Yuedong Zhong (Sun Yat-sen University), Guangba  Yu (The Chinese University of Hong Kong), Zhihan Jiang (The Chinese University of Hong Kong), Minzhi Yan (HCC Lab, Huawei Cloud Computing Technology Co., Ltd), Wenfei Luan (HCC Lab, Huawei Cloud Computing Technology Co., Ltd), Tianyu Yang (HCC Lab, Huawei Cloud Computing Technology Co., Ltd), Rui Ren (Computing and Networking Innovation Lab, Huawei Cloud Computing Technology Co., Ltd), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334651

**中文总结:** 基于 2,000 条大型云厂商真实运维查询识别五类 OpsQA 意图与六类 chatbot 失败根因，提出 intent-guided RAG 聊天机器人 iKnow，针对查询补全、检索与生成各环节提升云运维问答可靠性。

**Abstract:** Managing complex cloud services requires standard operational documentation, but its sheer volume often hinders cloud engineers from efficient knowledge acquisition. Retrieval-Augmented Generation (RAG) can streamline this process by retrieving relevant knowledge and generating concise, referenced answers. However, deploying a reliable RAG-based chatbot for cloud operation remains a challenge. In this experience paper, we analyze the development and deployment of RAG-based chatbots for operational question answering (OpsQA) at a large-scale cloud vendor. Through an empirical study of 2,000 real-world queries across three operational teams, we identify five unique OpsQA intent types (e.g., symptom analysis and terminology explanation) and their corresponding requirements for a satisfactory answer, which differ from general software engineering queries. Our analysis further uncovers six root causes leading to chatbot failures—over half stem from query issues (i.e., incompleteness, out-of-scope, or invalid queries), while others are from retrieval or generation issues. To address these issues, we propose iKnow, an intent-guided RAG-based chatbot that integrates intent detection, query rewriting tailored to each intent, and missing knowledge detection to enhance answer quality. In internal evaluations, iKnow improves average answer accuracy from 65.8% to 81.3% with only a modest increase in latency. iKnow has been deployed for six months at CloudA, supporting thousands of cloud engineers in daily operations. We discuss lessons learned from real-world deployment, providing valuable insights for future research and practical implementations in similar domains.


## 26. LAURA: Enhancing Code Review Generation with Context-Enriched Retrieval-Augmented LLM

**Authors:** Yuxin Zhang (Beijing Institute of Technology), Yuxia Zhang (Beijing Institute of Technology), Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Yanjie Jiang (Peking University), Hui Liu (Beijing Institute of Technology)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334572

**中文总结:** 提出 LAURA，面向代码审查生成的检索增强 LLM 框架，融合审查样例检索、变更上下文增强与系统化引导，并构建高质量数据集；在 ChatGPT-4o 与 DeepSeek v3 上显著优于仅依赖历史变更与评论的基线。

**Abstract:** Code review is critical for ensuring software quality and maintainability. With the rapid growth in software scale and complexity, code review has become a bottleneck in the development process because of its time-consuming and knowledge-intensive nature and the shortage of experienced reviewers. Several approaches have been proposed for automatically generating code reviews based on retrieval, neural machine translation, pre-trained models, or large language models (LLMs). These approaches mainly leverage historical code changes and review comments. However, a large amount of crucial information for code review, such as the context of code changes and prior review knowledge, has been overlooked. This paper proposes an LLM-based review knowledge-augmented, context-aware framework for code review generation, named LAURA. The framework integrates review exemplar retrieval, context augmentation, and systematic guidance to enhance the performance of ChatGPT-4o and DeepSeek v3 in generating code review comments. Besides, given the extensive low-quality reviews in existing datasets, we also constructed a high-quality dataset. Experimental results show that for both models, LAURA generates review comments that are either completely correct or at least helpful to developers in 42.2% and 40.4% of cases, respectively, significantly outperforming SOTA baselines. Furthermore, our ablation studies demonstrate that all components of LAURA contribute positively to improving comment quality.


## 27. Learning Project-wise Subsequent Code Edits via Interleaving Neural-based Induction and Tool-based Deduction

**Authors:** Chenyan Liu (Shanghai Jiao Tong University; National University of Singapore), Yun Lin (Shanghai Jiao Tong University), Yuhuan Huang (Shanghai Jiao Tong University), Jiaxin Chang (Shanghai Jiao Tong University), Binhang Qi (National University of Singapore), Bo Jiang (Bytedance Network Technology), Zhiyong Huang (National University of Singapore), Jin Song Dong (National University of Singapore)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334574

**中文总结:** 提出 TRACE，通过交替「神经归纳（语义编辑预测）」与「工具演绎（语法编辑预测）」预测项目级后续代码编辑，兼顾跨文件范围、准确性与效率；在真实工业/开源场景下优于 Cursor、CoEdPilot 等局部或低效方案。

**Abstract:** In industrial and open-source software engineering tasks, developers often perform project-wise code editing tasks, including feature enhancement, refactoring, and bug fixing, where the leading AI models are expected to support the productivity. Hence, researchers and practitioners have proposed and adopted many LLM-based solutions to facilitate their real- world development. However, they largely suffer from the balance among predicting scope, accuracy, and efficiency. For example, solutions like Cursor achieve high accuracy only in a local editing scope while its performance drops on cross-file edits. In contrast, solutions like CoEdPilot exhibit efficiency limitations when used to predict project-wise edits. In this work, we propose TRACE (Tool-integrated Recom- mendAtion for Code Editing), a novel subsequent code editing solution to push the boundary of scope, accuracy, and effi- ciency. Our rationale lies in that code edits are triggered for either semantic or syntactic reasons. Therefore, TRACE predicts subsequent edits by interleaving neural-based induction for semantic edit prediction and tool-based deduction for syntactic edit prediction. The tools can be any IDE facilities, such as refactoring tools (e.g., rename) or linting tools (e.g., use-def), providing decent performance of deducing edit-location and edit- generation. Technically, we address the challenge of (1) when to interleave between neural-based and tool-based prediction and (2) how to further improve the performance of neural-based prediction. As for the former, we learn a neural model to detect when to invoke IDE editing tools. As for the latter, we propose a novel and fine-grained editing representation to further boost the performance of neural editing models. Our extensive experiments show that, in comparison to the state-of-the-arts such as CoEdPilot, GrACE, and CCT5, TRACE significantly improves the performance of edit location (by 43.76%) and edit generation (by 11.16%). Our simulation experi- ment on an interactive editing setting shows that TRACE achieves an acceptance rate 6.15% higher than Cursor. Moreover, our user study consists of 24 participants on Cursor, CoEdPilot, and TRACE, on three code editing tasks. The results show that the experimental group with TRACE achieves leading performance on cross-file global edits. In addition, we observe concerning user behaviours on how participants deal with false predictions by the tools, shedding light on the design of future code-editing tools.


## 28. LLMPort: Cross-file Patch Porting via Task Decomposition and Self-correction

**Authors:** Bofei Chen (Fudan University), Lei Zhang (Fudan University), Peng Deng (Fudan University), Nan Wang (Fudan University), Haoyu Xu (Fudan University), Mingda Guo (Fudan Universityv), Yuan Zhang (Fudan University), Min Yang (Fudan University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334236

**中文总结:** 提出 LLMPort 跨文件安全补丁移植框架：将复杂补丁分解为原子子任务、提取最小相关上下文并注入领域知识，再以渐进式自校正评估与修正各子任务输出；在 Java 等多文件真实补丁上优于基于规则的移植方法。

**Abstract:** Security patch porting aims to adapt patches developed for one software version so they can be used in another version. This approach is crucial for maintaining the security of software systems over time. However, existing works often rely on predefined rules to understand patches, limiting their generalizability and portability. Additionally, they are ineffective when porting complex patches that involve numerous modified code lines across multiple files, which is common in real-world software, especially Java applications.

To overcome these obstacles, we propose a novel patch porting framework, called LLMPort. First, LLMPort breaks down the complex patch porting task into distinct subtasks, each containing an atomic code unit from the original patch. This enhances the LLMs’ focus. Second, for each subtask, LLMPort extracts the minimal patch-related code context and constructs a prompt with task-specific domain knowledge to guide the LLM in porting the patch code to the target version. Third, LLMPort implements a progressive self-correction system to automatically assess the correctness of the generated patch, and identify and correct error subtasks based on LLMs’ self-correction capabilities.

We evaluate LLMPort for porting Java language patches on a large-scale dataset, including 1,992 unique patch file pairs, and it successfully ports 91.92% of them. To assess the portability of LLMPort, we also evaluate its capability to port C language patches. The results show that it outperforms state-of-the-art approaches, including TSBPORT and FixMorph. LLMPort also discovers five 0-day vulnerabilities due to incomplete patches and the developers received and merged the new patches generated by LLMPort into the official code branches.


## 29. LongCodeZip: Compress Long Context for Code Language Models

**Authors:** Yuling Shi (Shanghai Jiao Tong University), Yichun Qian (Stanford University), Hongyu Zhang (Chongqing University), Beijun Shen (Shanghai Jiao Tong University), Xiaodong Gu (Shanghai Jiao Tong University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334583

**中文总结:** 提出 LongCodeZip 面向代码 LLM 的即插即用长上下文压缩：粗粒度按指令条件困惑度保留相关函数，细粒度在自适应 token 预算内选块；在代码补全、摘要与问答等任务上 一致地优于 LLMLingua 等通用压缩方法。

**Abstract:** Code generation under long contexts is becoming increasingly critical as Large Language Models (LLMs) are required to reason over extensive information in the codebase. While recent advances enable code LLMs to process long inputs, high API costs and generation latency remain substantial bottlenecks. Existing context pruning techniques, such as LLMLingua, achieve promising results for general text but overlook code-specific structures and dependencies, leading to suboptimal performance in programming tasks. In this paper, we propose LongCodeZip, a novel plug-and-play code compression framework designed specifically for code LLMs. LongCodeZip employs a dual-stage strategy: (1) coarse-grained compression, which identifies and ranks function-level chunks using conditional perplexity with respect to the instruction, retaining only the most relevant functions; and (2) fine-grained compression, which segments retained functions into blocks based on perplexity and selects an optimal subset under an adaptive token budget to maximize relevance. Evaluations across multiple tasks, including code completion, summarization, and question answering, show that LongCodeZip consistently outperforms baseline methods, achieving up to a 5.6x compression ratio without degrading task performance. By effectively reducing context size while preserving essential information, LongCodeZip enables LLMs to better scale to real-world, large-scale code scenarios, advancing the efficiency and capability of code intelligence applications. Our code and data are available at https://github.com/YerbaPage/LongCodeZip .


## 30. Mixture-of-Experts Low-Rank Adaptation for Multilingual Code Summarization

**Authors:** Tianchen Yu (School of Software Engineering, South China University of Technology), Li Yuan (School of Software Engineering, South China University of Technology, Guangzhou, China), Hailin Huang (South China University of Technology), Jiexin Wang (South China University of Technology), Yi Cai (School of Software Engineering, South China University of Technology, Guangzhou, China)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334619

**中文总结:** 提出 MMLoRA（Mixture-of-Experts Multilingual LoRA），以通用专家加语言专精专家缓解多语言代码摘要 PEFT 的梯度冲突与共性丢失，并设计 expert loss 保持专家多样性；在多语言代码摘要上达到 SOTA。

**Abstract:** As Code Language Models (CLMs) are increasingly used to automate multilingual code intelligence tasks, Full-Parameter Fine-Tuning (FPFT) of CLMs has become a widely adopted approach, which is both time-consuming and resource-intensive. Parameter-Efficient Fine-Tuning (PEFT) provides a more efficient alternative to FPFT. However, it struggles to capture common features shared across languages, leading to performance degradation. Recent studies have explored mixed-language training with PEFT to avoid the loss of common features. However, these methods can result in gradient conflicts due to the diverse language-specific features, causing suboptimal performance particularly for low-resource languages. In this paper, we propose Mixture-of-Experts Multilingual Low-Rank Adaptation (MMLoRA). MMLoRA addresses gradient conflicts while preserving common features shared across languages by combining a universal expert with a set of specialized linguistic experts. Additionally, we introduce an expert loss function that maintains the diversity of specialized linguistic experts while balancing the learning progress. Experimental results indicate that MMLoRA achieves state-of-the-art performance in multilingual code summarization while maintaining efficient fine-tuning. The performance improvement is particularly significant in low-resource languages such as Ruby.


## 31. PEACE: Towards Efficient Project-Level Performance Optimization via Hybrid Code Editing

**Authors:** Xiaoxue Ren (Zhejiang University), Jun Wan (Zhejiang University), Yun Peng (The Chinese University of Hong Kong), Zhongxin Liu (Zhejiang University), Ming Liang (Ant Group), Dajun Chen (Ant Group), Wei Jiang (Ant Group), Yong Li (Ant Group)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334295

**中文总结:** 提出 PEACE 项目级性能优化混合代码编辑框架，分三阶段：依赖感知优化函数序列、识别有效关联编辑、性能编辑迭代，并构建含 146 项真实 GitHub Python 优化任务的 PEACExec 基准；在保持项目正确性前提下实现跨函数协同优化。

**Abstract:** Large Language Models (LLMs) have demonstrated significant capability in code generation, but their potential in code optimization remains underexplored. Previous LLM-based code optimization approaches exclusively focus on function-level optimization and overlook interaction between functions, failing to generalize to real-world development scenarios. Code editing techniques show great potential for conducting project-level code optimization, yet they face challenges associated with invalid edits and suboptimal internal functions. To address these gaps, we propose PEACE, a novel hybrid framework for \textbf{P}roject-level p\textbf{E}rformance optimization through \textbf{A}utomatic \textbf{C}ode \textbf{E}diting, which also ensures the overall correctness and integrity of the project. PEACE integrates three key phases: dependency-aware optimizing function sequence construction, valid associated edits identification, and performance editing iteration. To rigorously evaluate the effectiveness of PEACE, we construct PEACExec, the first benchmark comprising 146 real-world optimization tasks from 47 high-impact GitHub Python projects, along with highly qualified test cases and executable environments. Extensive experiments demonstrate PEACE’s superiority over the state-of-the-art baselines, achieving a 69.2% correctness rate (pass@1) and +46.9% opt rate in execution efficiency. Notably, our PEACE outperforms all baselines by significant margins, particularly in complex optimization tasks with multiple functions. Moreover, extensive experiments are also conducted to validate the contributions of each component in PEACE, as well as the rationale and effectiveness of our hybrid framework design.


## 32. Polyglot: An Extensible Framework to Benchmark Code Translation with LLMs

**Authors:** Marco Vieira (University of North Carolina at Charlotte), Priyam Ashish Shah (University of North Carolina at Charlotte), Bhavain Shah (University of North Carolina at Charlotte), Rrezarta Krasniqi (University of North Carolina at Charlotte)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334550

**中文总结:** 提出 Polyglot，基于 IBM CodeNet 构建可扩展的多语言代码翻译评测框架，从语法、执行、语义与静态指标评估 LLM 将 C 译为 Java/Python/Rust 的能力；结果显示简单翻译可行，但复杂逻辑与跨范式翻译仍受限。

**Abstract:** Large Language Models (LLMs) show great potential for automating code-related tasks. However, sound assessments are necessary to understand their true capabilities, particularly in code translation, where reliability is crucial. This paper studies the performance of LLMs in code translation by introducing a well-defined, automated, multi-language framework, referred to as Polyglot, that is adaptable to various programming languages and translation scenarios. Leveraging the IBM CodeNet Project, an extensive collection of coding problems in multiple languages, we assess translation quality using syntactic correctness, execution reliability, semantic preservation, and static code metrics. Our evaluation focuses on translating C to Java, Python, and Rust, languages that follow distinct paradigms and represent alternatives to modernize C-based systems. We evaluate open-source LLMs using three prompting strategies to understand the impact on translation performance. Our findings highlight that while LLMs show promising results for simple code translation, their limitations regarding complex logic and distinct language paradigms require further analysis.


## 33. PseudoFix: Refactoring Distorted Structures in Decompiled C Pseudocode

**Authors:** Gangyang Li (University of Science and Technology of China), Xiuwei Shang (University of Science and Technology of China), Shaoyin Cheng (University of Science and Technology of China), junqi zhang (University of Science and Technology of China), Li Hu, Xu Zhu (University of Science and Technology of China), Weiming Zhang (University of Science and Technology of China), Nenghai Yu (School of Cyber Security, University of Science and Technology of China)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334626

**中文总结:** 系统刻画反编译 C 伪代码的六种结构失真类型，提出 PseudoFix，以检索式 in-context 学习结合 LLM 重构失真控制流与结构，提升可读性。

**Abstract:** Decompilation can convert binary programs into clear C-style pseudocode, which is of great value in a wide range of security applications.  Existing research primarily focuses on recovering symbolic information in pseudocode, such as function names, variable names, and data types, but neglecting structural information. We observe that even when symbolic information is fully preserved, severe and complex structure distortions remain in the pseudocode, greatly impairing code readability and comprehension. In this work, we first systematically investigate structure distortions in decompiled pseudocode, revealing their variation patterns through quantitative analysis. Using open coding, we derive a taxonomy comprising six top-level categories of structure distortions. Building upon this taxonomy, we propose PseudoFix, a novel framework that combines large language models (LLMs) with retrieval-based in-context learning. PseudoFix employs semantic retrieval to select the most relevant few-shot examples that provide structure distortion knowledge, and combines this with the well-structured coding patterns learned by LLMs from vast source code repositories, to efficiently refactor distorted pseudocode. Comprehensive evaluations demonstrate that PseudoFix significantly improves pseudocode readability, achieving up to a 34% reduction in Halstead Complexity Effort and a 105% increase in BLEU-4 score. Notably, it significantly outperforms state-of-the-art approaches in both temporary variable elimination and goto statement removal tasks. Additionally, human evaluations yield consistently positive feedback from users across readability, consistency, and reasonability.


## 34. QuanBench: Benchmarking Quantum Code Generation with Large Language Models

**Authors:** Xiaoyu Guo (Kyushu University), Minggu Wang (Kyushu University), Jianjun Zhao (Kyushu University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334507

**中文总结:** 发布 QuanBench，含 44 项量子编程任务，以 Pass@K 与 Process Fidelity 评估 LLM 生成量子代码；当前模型整体准确率低于 40%，常见错误包括过时 API 与电路/算法逻辑错误。

**Abstract:** Large language models (LLMs) have shown good performance in general code generation, but their capability in quantum code generation remains insufficiently studied. This paper presents QuanBench, a benchmark for evaluating LLMs on quantum code generation. QuanBench includes 44 programming tasks covering quantum algorithms, state preparation, gate decomposition, and quantum machine learning. Each task has an executable canonical solution and is evaluated by functional correctness (Pass@K) and quantum semantic equivalence (Process Fidelity). We evaluate several recent LLMs, including general-purpose and code-specialized models. The results show that current LLMs have limited capability in generating correct quantum code, with overall accuracy below 40% and frequent semantic errors. We also analyze common failure cases, such as outdated API usage, circuit construction errors, and incorrect algorithm logic. QuanBench provides a basis for future work on improving quantum code generation with LLMs.


## 35. RealisticCodeBench: Towards More Realistic Evaluation of Large Language Models for Code Generation

**Authors:** Xiao Yu (Zhejiang University), Haoxuan Chen (Wuhan University of Technology), Lei Liu (Xi’an Jiaotong University), Xing Hu (Zhejiang University), Jacky Keung (City University of Hong Kong), Xin Xia (Zhejiang University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334662

**中文总结:** 提出 RealisticCodeBench，从高星 GitHub 仓库挖掘开发者实际用 LLM 解决的代码生成任务，弥补 HumanEval/ClassEval 等与真实使用场景脱节的问题。

**Abstract:** Evaluating the code generation capabilities of Large Language Models (LLMs) remains an open question. Existing benchmarks like HumanEval and MBPP focus primarily on algorithmic and basic programming tasks, which do not fully capture the intricacies of real-world coding challenges. Recently, more advanced benchmarks—such as CoderEval, EvoCodeBench, and ClassEval—have been introduced to address this gap, evaluating LLMs on practical coding tasks from GitHub repositories, such as non-standalone function generation and class-level code generation. However, even the most sophisticated LLMs struggle with these complex tasks; for instance, GPT-4 achieves only a 37.0% pass@1 on ClassEval. Prior studies show that developers often discard LLM-generated code or abandon code generation models when outputs are incorrect or require extensive debugging, which leads them to rely on LLMs primarily for simpler tasks that high-performing models can handle reliably.

In response to this gap, we introduce RealisticCodeBench, a benchmark specifically designed to reflect the types of problems developers commonly tackle with LLMs. By mining high-star GitHub repositories for code samples tagged as generated by ChatGPT or Copilot, we collect real-world coding tasks that capture typical LLM usage scenarios. We modify these tasks, generate reference solutions and test cases, and adapt the problems into multiple programming languages. This effort results in RealisticCodeBench, comprising a total of 417 programming problems translated across multiple languages: 392 in Python, 376 in JavaScript, 372 in TypeScript, 339 in Java, and 353 in C++, each with corresponding reference solutions and test cases. We evaluate 12 general-purpose and code-specific LLMs on RealisticCodeBench. Our findings reveal that GPT-4.1 achieves the highest average pass@1 score across languages, closely followed by DeepSeek-V3-671B, suggesting that DeepSeek-V3-671B provides a viable open-source alternative to GPT-4.1 for large companies with sufficient GPU resources and privacy concerns. CodeGeeX4-9B, a cost-effective model, emerges as a suitable substitute for GPT-3.5 for individual developers and smaller organizations with similar privacy considerations. Additionally, LLM performance discrepancies between HumanEval and RealisticCodeBench suggest that some LLMs are either overly specialized for HumanEval-style problems or insufficiently optimized for real-world coding challenges. Finally, we analyze failed cases, summarize common LLM limitations, and provide implications for researchers and practitioners.


## 36. Repairing Leaks in Resource Wrappers

**Authors:** Sanjay Malakar (University of California, Riverside), Martin Kellogg (New Jersey Institute of Technology), Michael D. Ernst (University of Washington), Manu Sridharan (University of California at Riverside)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334447

**中文总结:** 面向资源包装器场景改进资源泄漏自动修复：集成资源管理规约推断、程序变体变换与 Field Containment Analysis，使检测与修复能处理 wrapper 字段中的资源生命周期。

**Abstract:** A resource leak occurs when a program fails to release finite resources such as sockets, file descriptors, database connections, etc. While sound static analysis tools can detect all leaks, automatically repairing them remains challenging. Prior work took the output of a detection tool and attempted to repair only leaks of a hard-coded list of library resource types. This approach limits the scope of repairable leaks: real-world code uses resource wrappers that store a resource in a field and must themselves be closed.

This paper makes four key contributions to improve resource leak repair in the presence of wrappers. (1) It integrates inference of resource management specifications into the repair pipeline, enabling extant fixing approaches to reason about wrappers. (2) It transforms programs into variants that are easier to analyze, making inference, detection, and fixing tools more effective; for instance, it makes detection tools report problems closer to the root cause, often in a client of a resource wrapper rather than within the wrapper class itself. (3) A novel Field Containment Analysis reasons more precisely about resource lifetimes, enabling repair of more leaks involving resources stored in fields. (4) It introduces a new repair pattern and more precise reasoning to better handle resources stored in non-final fields.

Prior work fixed 41% of resource leak warnings in the NJR benchmark suite; our implementation Arodnap fixes 69%.


## 37. RustAssure: Differential Symbolic Testing for LLM-Transpiled C-to-Rust Code

**Authors:** Yubo Bai (University of California, Davis), Tapti Palit (University of California, Davis)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334436

**中文总结:** 提出 RustAssure，用 LLM 将 C 转译为 Rust 并通过差分符号测试验证语义等价；在五个真实项目上 89.8% 函数可编译，其中 69.9% 符号返回值与原版 C 等价。

**Abstract:** Rust is a memory-safe programming language that significantly improves software security. Existing codebases written in unsafe memory languages, such as C, must first be transpiled to Rust to take advantage of Rust’s improved safety guarantees. RustAssure presents a system that uses Large Language Models (LLMs) to automatically transpile existing C codebases to Rust. RustAssure uses prompt engineering techniques to maximize the chances of the LLM generating idiomatic and safe Rust code. Moreover, because LLMs often generate code with subtle bugs that can be missed under traditional unit or fuzz testing, RustAssure performs differential symbolic testing to establish the semantic similarity between the original C and LLM-transpiled Rust code. We evaluated RustAssure with five real-world applications and libraries, and showed that our system is able to generate compilable Rust functions for 89.8% of all C functions, of which 69.9% produced equivalent symbolic return values for both the C and Rust functions.


## 38. RustRepoTrans: Repository-level Context Code Translation Benchmark Targeting Rust

**Authors:** Guangsheng Ou (Sun Yat-sen University), Mingwei Liu (Sun Yat-Sen University), Yuxuan Chen, Yanlin Wang (Sun Yat-sen University), Xin Peng (Fudan University), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334552

**中文总结:** 发布 RustRepoTrans，首个面向增量、仓库级上下文的 Rust 代码翻译基准，含 375 项任务，覆盖依赖、跨模块引用与架构差异等真实迁移难点。

**Abstract:** Recent advancements in large language models (LLMs) have demonstrated impressive capabilities in code translation, typically evaluated using benchmarks like CodeTransOcean and RepoTransBench. However, dependency-free benchmarks fail to capture real-world complexities by focusing primarily on simple function-level translations and overlooking repository-level context (e.g., dependencies). Full-repository translation benchmarks significantly exceed the current capabilities of existing models, resulting in performance bottlenecks that fail to provide actionable insights for guiding model development. Furthermore, existing benchmarks do not account for the scenario of incrementally translating new or modified modules from the source to the target language, which demands careful handling of repository-level contexts such as dependencies, cross-module references, and architectural divergence. Moreover, LLMs’ effectiveness in translating to newer, low-resource languages like Rust remains largely underexplored.

To address these gaps, we introduce RustRepoTrans, the first repository-level context code translation benchmark targeting incremental translation, comprising 375 tasks translating into Rust from C, Java, and Python. Using this benchmark, we evaluate seven representative LLMs, analyzing their errors to assess limitations in complex translation scenarios. Among them, DeepSeek-R1 performs best with 51.5% Pass@1, excelling in both basic functionality and additional translation abilities, such as noise robustness and syntactical difference identification. However, even DeepSeek-R1 experiences a 22.2% performance drop (Pass@1 from 73.7% to 51.5%) when handling repository-level context compared to previous benchmarks without such context. Meanwhile, we propose a set of more fine-grained evaluation metrics and an enhanced evaluation framework, enabling a more comprehensive analysis of LLMs’ performance in repository-level context code translation tasks to provide fine-grained insights that can effectively inform the development of code translation techniques.


## 39. Seeing is Fixing: Cross-Modal Reasoning with Multimodal LLMs for Visual Software Issue Repair

**Authors:** Kevin Huang, Jian Zhang (Nanyang Technological University), Xiaofei Xie (Singapore Management University), Chunyang Chen (TU Munich)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334310

**中文总结:** 提出 GUIRepair，以 Image2Code 将 GUI 视觉症状转为可执行复现代码、Code2Image 回放验证补丁，实现多模态软件缺陷的跨模态推理与自动修复。

**Abstract:** Large language model (LLM)-based automated program repair (APR) techniques have shown promising results in resolving real-world github issue tasks. Existing APR systems are primarily evaluated in unimodal settings (e.g., SWE-bench), relying solely on textual issue descriptions and source code. However, these autonomous systems struggle to resolve multimodal problem scenarios (e.g., SWE-bench M) due to limitations in interpreting and leveraging visual information. In multimodal scenarios, LLMs need to rely on visual information in the graphical user interface (GUI) to understand bugs and generate fixes. To bridge this gap, we propose GUIRepair, a cross-modal reasoning approach for resolving multimodal issue scenarios by understanding and capturing visual information. Specifically, GUIRepair integrates two key components, Image2Code and Code2Image—to enhance fault comprehension and patch validation. Image2Code extracts relevant project documents based on the issue report, then applies these domain knowledge to generate the reproduced code responsible for the visual symptoms, effectively translating GUI images into executable context for better fault comprehension. Code2Image replays the visual issue scenario using the reproduced code and captures GUI renderings of the patched program to assess whether the fix visually resolves the issue, providing feedback for patch validation. We evaluate GUIRepair on SWE bench M, and the approach demonstrates significant effectiveness. When utilizing GPT-4o as the base model, GUIRepair solves 157 instances, outperforming the best open-source baseline by 26 instances. Furthermore, when using o4-mini as the base model, GUIRepair can achieve even better results and solve 175 instances, outperforming the top commercial system by 22 instances. This emphasizes the success of our new perspective on incorporating cross-modal reasoning by understanding and capturing visual information to resolve multimodal issues.


## 40. SE-Jury: An LLM-as-Ensemble-Judge Metric for Narrowing the Gap with Human Evaluation in SE

**Authors:** Xin Zhou (Singapore Management University, Singapore), Kisub Kim (DGIST), Ting Zhang (Monash University), Martin Weyssow (Singapore Management University), Luis F. Gomes (Carnegie Mellon University), Guang Yang, Kui Liu (Huawei), Xin Xia (Zhejiang University), David Lo (Singapore Management University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334309

**中文总结:** 提出 SE-Jury，以五种独立评判策略组成的 LLM 集成法官，经动态团队选择对生成代码/补丁/摘要等软件产物打分；在多项 SE 基准上更接近人工评估。

**Abstract:** Large Language Models (LLMs) and other automated techniques have been increasingly used to support software developers by generating software artifacts such as code snippets, patches, and comments. However, accurately assessing the correctness of these generated artifacts remains a significant challenge. On one hand, human evaluation provides high accuracy but is labor-intensive and lacks scalability. On the other hand, many automatic evaluation metrics are scalable and require minimal human effort, but they often fail to accurately reflect the actual correctness of generated software artifacts.

In this paper, we present SE-Jury, the first evaluation metric for LLM-as-Ensemble-Judge specifically designed to accurately assess the correctness of generated software artifacts. SE-Jury first defines five distinct evaluation strategies, each implemented as an independent judge. A dynamic team selection mechanism then identifies the most appropriate subset of judges as a team to produce a final correctness score through ensembling. We evaluate SE-Jury across a diverse set of software engineering (SE) benchmarks, including CoNaLa, Card2Code, HumanEval-X, APPS, APR-Assess, and Summary-Assess, which span three popular SE tasks: code generation, automated program repair, and code summarization. Experimental results demonstrate that SE-Jury consistently achieves a higher correlation with human judgments, with improvements ranging from 34.4% to 113.0% over existing automatic metrics. Furthermore, SE-Jury reaches agreement levels with human annotators that are close to inter-annotator agreement in code generation and program repair tasks. These findings underscore SE-Jury’s potential as a scalable and reliable alternative to human evaluation in these SE tasks.


## 41. SemGuard: Real-Time Semantic Evaluator for Correcting LLM-Generated Code

**Authors:** Qinglin Wang (Shandong Normal University), Zhihong Sun (Shandong Normal University), Ruyun Wang (Institute of Information Engineering, Chinese Academy of Sciences), Tao Huang (Shandong Normal University), Zhi Jin (Peking University), Ge Li (Peking University), Chen Lyu (Shandong Normal University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334346

**中文总结:** 提出 SemGuard，在 LLM 解码过程中以行级语义评估器实时干预，并构建带细粒度语义标注的数据集 SemDiff；针对编译通过但行为错误的语义缺陷，优于事后执行反馈的 RCODE 等方案。

**Abstract:** \textit{Large Language Models} (LLMs) can translate natural language requirements into code, yet empirical analyses of representative models reveal that \emph{semantic errors}—programs that compile but behave incorrectly—constitute the majority of observed faults (e.g., $>$60% on DeepSeek-Coder-6.7B and QwenCoder-7B). Post-hoc repair pipelines detect such faults only \emph{after} execution, incurring latency, relying on incomplete test suites, and often mis-localizing the defect. Since semantic drift originates in the autoregressive decoding process, \emph{intervening while the code is being generated} is a direct way to stop error propagation.  Constrained-decoding approaches such as ROCODE attempt this, but still wait until the entire program runs to obtain feedback and use entropy heuristics that do not truly capture semantics.  A more effective solution must inject \emph{semantic} signals—early and precisely—into the decoding process.We present \textbf{SemGuard}, a semantic-evaluator-driven framework that performs real-time, line-level semantic supervision.  To train the evaluator, we build \textit{SemDiff}, the first dataset with fine-grained annotations that mark the exact line where a correct and an incorrect implementation diverge.  The evaluator, once embedded in the LLM’s decoder, flags deviations on partial code, rolls back to the faulty line, and guides regeneration—without executing the program or requiring test cases. Across four benchmarks, SemGuard consistently outperforms state-of-the-art baselines.  It lowers the semantic error rate by \textbf{19.86%} on \textit{SemDiff} relative to ROCODE, and lifts Pass@1 by \textbf{48.92%} on the real-world \textit{LiveCodeBench} with CodeLlama-7B.  Similar gains hold for StarCoder2-7B on \textit{MBPP} and for DeepSeekCoder-6.7B on the Java benchmark \textit{SemDiff-Java}, demonstrating model- and language-agnostic effectiveness.


## 42. SPICE : An Automated SWE-Bench Labeling Pipeline for Issue Clarity, Test Coverage, and Effort Estimation

**Authors:** Aaditya Bhatia (Queen's University), Gustavo A. Oliva (Centre for Software Excellence, Huawei Canada), Gopi Krishnan Rajbahadur (Centre for Software Excellence, Huawei, Canada), Haoxiang Zhang (Huawei), Yihao Chen (Center for Software Excellence, Huawei Canada), Zhilong Chen (Center for Software Excellence, Huawei Canada), Arthur Leung (Center for Software Excellence, Huawei Canada), Dayi Lin (Centre for Software Excellence, Huawei Canada), Boyuan Chen (Centre for Software Excellence, Huawei Canada), Ahmed E. Hassan (Queen’s University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334598

**中文总结:** 提出 SPICE，自动为 SWE-bench 风格数据标注 issue 清晰度、测试覆盖与工作量估计；与人工标注高度一致，1000 条实例标注成本从约 10 万美元降至 5.10 美元。

**Abstract:** High-quality labeled datasets are crucial for training and evaluating foundation models in software engineering, but creating them is often prohibitively expensive and labor-intensive. We introduce SPICE, a scalable, automated pipeline for labeling SWE-bench-style datasets with annotations for issue clarity, test coverage, and effort estimation. SPICE combines context-aware code navigation, rationale-driven prompting, and multi-pass consensus to produce labels that closely approximate expert annotations. SPICE’s design was informed by our own experience and frustration in labeling more than 800 tasks from SWE-Gym. SPICE achieves strong agreement with human-labeled SWE-bench Verified data while reducing the cost of labeling 1,000 instances from around $100,000 (manual annotation) to just $5.10. These results demonstrate SPICE’s potential to enable cost-effective, large-scale dataset creation for SE-focused FMs.


## 43. Token Sugar: Making Source Code Sweeter for LLMs through Token-Efficient Shorthand

**Authors:** Zhensu Sun (Singapore Management University), Chengran Yang (Singapore Management University, Singapore), Xiaoning Du (Monash University), Zhou Yang (University of Alberta, Alberta Machine Intelligence Institute), Li Li (Beihang University), David Lo (Singapore Management University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334281

**中文总结:** 提出 Token Sugar，将高频冗长代码模式映射为可逆、省 token 的简写并融入 LLM 预训练；从语料挖掘 799 组简写映射，在语义层显著降低输入与生成 token 数以缓解推理成本。

**Abstract:** Large language models (LLMs) have shown exceptional performance in code generation and understanding tasks, yet their high computational costs hinder broader adoption. One important factor is the inherent verbosity of programming languages, such as unnecessary formatting elements and lengthy boilerplate code. This leads to inflated token counts in both input and generated outputs, which increases inference costs and slows down the generation process. Prior work improves this through simplifying programming language grammars, reducing token usage across both code understanding and generation tasks. However, it is confined to syntactic transformations, leaving significant opportunities for token reduction unrealized at the semantic level.

In this work, we propose \textit{Token Sugar}, a novel concept that replaces frequent and verbose code patterns with reversible, token-efficient shorthand in the source code. To realize this concept in practice, we designed a systematic solution that mines high-frequency, token-heavy patterns from a code corpus, maps each to a unique shorthand, and integrates them into LLM pretraining via code transformation. With this solution, we obtain 799 (code pattern, shorthand) pairs, which can reduce up to 15.1% token count in the source code and is complementary to existing syntax-focused methods. We further trained three widely used LLMs on Token Sugar-augmented data. Experimental results show that these models not only achieve significant token savings (up to 11.2% reduction) during generation but also maintain near-identical Pass@1 scores compared to baselines trained on unprocessed code.


## 44. Understanding Software Engineering Agents: A Study of Thought-Action-Result Trajectories

**Authors:** Islem BOUZENIA (University of Stuttgart), Michael Pradel (CISPA Helmholtz Center for Information Security)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334353

**中文总结:** 统一 RepairAgent、AutoCodeRover、OpenHands 的 thought-action-result 轨迹（120 条轨迹、2822 次 LLM 交互）并做大规模实证；量化迭代、token 与动作模式，揭示推理连贯性与反馈整合等关键特征及失败模式。

**Abstract:** Large Language Model (LLM)-based agents are increasingly employed to automate complex software engineering tasks such as program repair and issue resolution. These agents operate by autonomously generating natural language thoughts, invoking external tools, and iteratively refining their solutions. Despite their widespread adoption, the internal decision-making processes of these agents remain largely unexplored, limiting our understanding of their operational dynamics and failure modes. In this paper, we present a large-scale empirical study of the thought-action-result trajectories of three state-of-the-art LLM-based agents: RepairAgent, AutoCodeRover, and OpenHands. We unify their interaction logs into a common format, capturing 120 trajectories and 2822 LLM interactions focused on program repair and issue resolution. Our study combines quantitative analyses of structural properties, action patterns, and token usage with qualitative assessments of reasoning coherence and feedback integration. We identify key trajectory characteristics such as iteration counts and token consumption, recurring action sequences, and the semantic coherence linking thoughts, actions, and their results. Our findings reveal behavioral motifs and anti-patterns that distinguish successful from failed executions, providing actionable insights for improving agent design, including prompting strategies, failure diagnosis, and anti-pattern detection. We release our dataset and annotation framework to support further research on transparent and robust autonomous software engineering agents.


## 45. Watson: A Cognitive Observability Framework for the Reasoning of LLM-Powered Agents

**Authors:** Benjamin Rombaut (Centre for Software Excellence, Huawei Canada), Sogol Masoumzadeh (Mcgill University), Kirill Vasilevski (Huawei Canada), Dayi Lin (Centre for Software Excellence, Huawei Canada), Ahmed E. Hassan (Queen’s University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11334632

**中文总结:** 提出 cognitive observability 概念及框架 Watson，在不改变 agent 行为的前提下用 prompt attribution 回溯推断 fast-thinking LLM agent 的推理轨迹；在 MMLU 与 AutoCodeRover/SWE-bench-lite 上支持人工调试与自动修正。

**Abstract:** Large language models (LLMs) are increasingly integrated into autonomous systems, giving rise to a new class of software known as “Agentware”, where LLM-powered agents perform complex, open-ended tasks in domains such as software engineering, customer service, and data analysis. However, their high autonomy and opaque reasoning processes pose significant challenges for traditional software observability methods. To address this, we introduce the concept of cognitive observability - the ability to recover and inspect the implicit reasoning behind agent decisions. We present Watson, a general-purpose framework for observing the reasoning processes of fast-thinking LLM agents without altering their behavior. Watson retroactively infers reasoning traces using prompt attribution techniques. We evaluate Watson in both manual debugging and automated correction scenarios across the MMLU benchmark and the AutoCodeRover agent on the SWE-bench-lite dataset. In both static and dynamic settings, Watson surfaces actionable reasoning insights and supports targeted interventions, demonstrating its practical utility for improving transparency and reliability in Agentware systems.

