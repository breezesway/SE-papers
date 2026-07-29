# ASE 2025 Research Track — Debugging and Fault Diagnosis

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 24

## 1. Agents in the Sandbox: End-to-End Crash Bug Reproduction for Minecraft

**Authors:** Eray Yapağcı (Bilkent University), Yavuz Alp Sencer Öztürk (Bilkent University), Eray Tüzün (Bilkent University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334697

**中文总结:** 提出 BugCraft 两阶段框架：LLM 将 Minecraft 崩溃报告合成为结构化复现步骤，再由视觉 LLM 智能体在沙盒中执行以触发崩溃，并发布 BugCraft-Bench 数据集。

**Abstract:** Reproducing game bugs, particularly crash bugs in continuously evolving games like Minecraft, is a notoriously manual, time-consuming, and challenging process to automate; insights from a key decision maker from Minecraft we interviewed confirm this, highlighting that a substantial portion of crash reports necessitate manual scenario reconstruction. Despite the success of LLM-driven bug reproduction in other software domains, games, with their complex interactive environments, remain largely unaddressed. This paper introduces BugCraft, a novel end-to-end framework designed to automate the reproduction of crash bugs in Minecraft directly from user-submitted bug reports, addressing the critical gap in automated game bug reproduction. BugCraft employs a two-stage approach: first, a Step Synthesizer leverages LLMs and Minecraft Wiki knowledge to transform bug reports into high-quality, structured steps to reproduce (S2R). Second, an Action Model, powered by a vision-based LLM agent and a custom macro API, executes these S2R steps within Minecraft to trigger the reported crash. To facilitate evaluation, we introduce BugCraft-Bench, a curated dataset of Minecraft crash bug reports. On BugCraft-Bench, our framework end-to-end reproduced 34.9% of crash bugs with GPT-4.1, outperforming baseline computer-use models by 37%. BugCraft demonstrates the feasibility of automated reproduction of crash bugs in complex game environments using LLMs, opening promising avenues for game testing and development. Finally, we make our code open at: https://bugcraft2025.github.io


## 2. AlertGuardian: Intelligent Alert Life-Cycle Management for Large-scale Cloud Systems

**Authors:** Guangba  Yu (The Chinese University of Hong Kong), Genting Mai (Sun Yat-sen University), Rui Wang (Tencent), Ruipeng Li (Tencent), Pengfei Chen (Sun Yat-sen University), Long Pan (Tencent), Ruijie Xu (Tencent)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334669

**中文总结:** 提出 AlertGuardian，LLM 与轻量图模型协同优化告警降噪、RAG 摘要与多智能体规则 refinement 三阶段；在真实云服务上实现 94.8% 告警削减与 90.5% 诊断准确率，375 条规则被 SRE 采纳。

**Abstract:** Alerts are critical for detecting anomalies in large-scale cloud systems, ensuring reliability and user experience. However, current systems generate overwhelming volumes of alerts, degrading operational efficiency due to ineffective alert life-cycle management. This experience paper details the efforts of Company-X to optimize alert life-cycle management, addressing alert fatigue in cloud systems. We propose AlertGuardian, a framework collaborating large language models (LLMs) and lightweight graph models to optimize the alert life-cycle through three phases: Alert Denoise uses graph learning model with virtual noise to filter noise, Alert Summary employs Retrieval Augmented Generation (RAG) with LLMs to create actionable alert summary, and Alert Rule Refinement leverages multi-agent iterative feedbacks to improve alert rule quality. Evaluated on four real-world datasets from Company-X’s services, AlertGuardian significantly mitigates alert fatigue (94.8% alert reduction ratios) and accelerates fault diagnosis (90.5% diagnosis accuracy). Moreover, AlertGuardian improves 1,174 alert rules, with 375 accepted by SREs (32% acceptance rate). Finally, we share success stories and lessons learned about alert life-cycle management from the deployment of AlertGuardian at Company-X.


## 3. CollaborLog: Efficient-Generalizable Log Anomaly Detection via Large-Small Model Collaboration in Software Evolution

**Authors:** Pei Xiao (Peking University), Chiming Duan (Peking University), Minghua He (Peking University), Tong Jia (Institute for Artificial Intelligence, Peking University, Beijing, China), Yifan Wu (Peking University), Jing Xu (ByteDance), Gege Gao (ByteDance), Lingzhe Zhang (Peking University, China), Weijie Hong (Peking university), Ying Li (School of Software and Microelectronics, Peking University, Beijing, China), Gang Huang (Peking University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334611

**中文总结:** 提出 CollaborLog，用自适应协调器在日志演化场景下协同小模型与 LLM：未演化日志走高效 SM，演化日志经 Evol-CoT 由 LLM 推理，并通过自适应演化机制 AEM 逐步将 LLM 判断迁移回 SM 以兼顾效率与泛化。

**Abstract:** Frequent software updates lead to log evolution, posing generalization challenges for current log anomaly detection. Traditional log anomaly detection research focuses on using small deep learning models (SMs), but these models inherently lack generalization due to their closed-world assumption. Large Language Models (LLMs) exhibit strong semantic understanding and generalization capabilities, making them promising for log anomaly detection. However, they suffer from computational inefficiencies. To balance efficiency and generalization, we propose a collaborative log anomaly detection scheme using an adaptive coordinator to integrate SM and LLM. The coordinator determines if incoming logs have evolved. Non-evolutionary los routed to the SM, while evolutionary logs are directed to the LLM for detailed inference using the constructed Evol-CoT. To gradually adapt to evolution, we introduce the adaptive evolve mechanism (AEM) updates the coordinator to redirect evolutionary logs identified by the LLM to the SM. Simultaneously, the SM is fine-tuned to inherit the LLM’s judgment on these logs. Extensive experiments on real-world log evolution dataset demonstrate that \method  achieves superior F1-scores in both intra-version and inter-version anomaly detection. Additionally, \method reduces processing time by 91.63% and token consumption by 85.59% compared to using an LLM alone.


## 4. Defects4Log: Benchmarking LLMs for Logging Code Defect Detection and Reasoning

**Authors:** Xin Wang (Changsha University of Science and Technology), Zhenhao Li (York University), Zishuo Ding (The Hong Kong University of Science and Technology (Guangzhou))

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334466

**中文总结:** 归纳涵盖 7 类 14 场景的日志代码缺陷 taxonomy，构建含 164 个经开发者验证真实缺陷的 Defects4Log 基准，并系统评估多种 prompt 策略下 LLM 在日志缺陷检测与推理上的能力与局限。

**Abstract:** Logging code is written by developers to capture system runtime behavior and plays a vital role in debugging, performance analysis, and system monitoring. However, defects in logging code can undermine the usefulness of logs and lead to misinterpretations. Although prior work has identified several logging defect patterns and provided valuable insights into logging practices, these studies often focus on a narrow range of defect patterns derived from limited sources (e.g., commit histories) and lack a systematic and comprehensive analysis. Moreover, large language models (LLMs) have demonstrated promising generalization and reasoning capabilities across a variety of coderelated tasks, yet their potential for detecting logging code defects remains largely unexplored.

In this experience paper, we derive a comprehensive taxonomy of logging code defects, which encompasses seven logging code defect patterns with 14 detailed scenarios. We further construct a benchmark dataset, Defects4Log, consisting of 164 developer verified real-world logging defects. Then we propose an automated framework that leverages various prompting strategies and contextual information to evaluate LLMs’ capability in detecting and reasoning logging code defects. Experimental results reveal that LLMs generally struggle to accurately detect and reason logging code defects based on the source code only. However, incorporating proper knowledge (e.g., detailed scenarios of defect patterns) can lead to 10.9% improvement in detection accuracy. Overall, our findings provide actionable guidance for practitioners to avoid common defect patterns and establish a foundation for improving LLM-based reasoning in logging code defect detection.


## 5. Explainable Fault Localization for Programming Assignments via LLM-Guided Annotation

**Authors:** Fang Liu (Beihang University), Tianze Wang (Beihang University), Li Zhang (Beihang University), Zheyu Yang (Beihang University), Jing Jiang (Beihang University), Zian Sun (Beihang University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334657

**中文总结:** 提出 FLAME，通过 LLM 引导标注与模型集成实现面向编程作业的可解释细粒度故障定位，在行级给出错误位置与自然语言解释，克服现有方法粒度粗或不适配 LLM 的问题。

**Abstract:** Providing timely and personalized guidance for students’ programming assignments, particularly by indicating fine-grained error locations with explanations, offers significant practical value for helping students complete assignments and enhance their learning outcomes. In recent years, various automated Fault Localization (FL) techniques, particularly those leveraging Large Language Models (LLMs), have demonstrated promising results in identifying errors in programs. However, existing fault localization techniques face challenges when applied to educational contexts. Most approaches operate at the method-level without explanatory feedback, resulting in granularity too coarse for students who need actionable insights to identify and fix their errors. While some approaches attempt line-level fault localization, they often depend on predicting line numbers directly in numerical form, which is ill-suited to LLMs. To address these challenges, we propose FLAME, a fine-grained, explainable Fault Localization method tailored for programming assignments via LLM-guided Annotation and Model Ensemble. FLAME leverages rich contextual information specific to programming assignments to guide LLMs in identifying faulty code lines. Instead of directly predicting line numbers, we prompt the LLM to annotate faulty code lines with detailed explanations, enhancing both localization accuracy and educational utility. To further improve reliability, we introduce a weighted multi-model voting strategy that aggregates results from multiple LLMs to determine the suspiciousness of each code line. Extensive experimental results demonstrate that FLAME outperforms state-of-the-art fault localization baselines on programming assignments, successfully localizing 207 more faults at top-1 over the best-performing baseline. Beyond educational contexts, FLAME also generalizes effectively to general-purpose software codebases, outperforming all baselines on the Defects4J benchmark.


## 6. FaultSeeker: LLM-Empowered Framework for Blockchain Transaction Fault Localization

**Authors:** Kairan Sun (Nanyang Technological University), Zhengzi Xu (Imperial Global Singapore), Kaixuan Li (Nanyang Technological University), Lyuye Zhang (Nanyang Technological University), Yuqiang Sun (Nanyang Technological University), Liwei Tan (MetaTrust Labs), Yang Liu (Nanyang Technological University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334320

**中文总结:** 提出 FaultSeeker，LLM 驱动的区块链交易故障定位框架，面向 DeFi 等 Web3 攻击事件自动识别脆弱函数与攻击向量；可将原本平均 16.7 分析师小时的定位工作大幅自动化。

**Abstract:** Web3 applications, particularly decentralized finance (DeFi) protocols, have grown rapidly with over $100 billion locked in smart contracts, attracting sophisticated attacks causing billions in losses. When attack occur, security analysts need to perform fault localization to identify vulnerable functions and understand attack vectors. This critical process currently requires an average of 16.7 analyst hours per incident due to complex blockchain execution models, rapidly evolving protocol interactions, and multi-contract attack patterns that exceed existing analytical capabilities. Despite its critical importance, blockchain fault localization has received limited attention due to fundamental challenges requiring semantic understanding of economic models and protocol-specific logic. Existing blockchain-specific tools target only single vulnerability types, while the only comprehensive solution, DAppFL, relies on machine learning model that may miss sophisticated exploits and lacks interpretability in results. Recent advances in large language models (LLMs) demonstrate remarkable code comprehension capabilities, but existing applications focus on proactive vulnerability detection with minimal exploration of post-incident fault localization.

We present FaultSeeker, an LLM-empowered framework for blockchain transaction fault localization. Inspired by cognitive science memory and attention mechanisms, our two-stage architecture combines transaction-level forensics for strategic scoping with coordinated specialist agents for sustained reasoning. This design provides long-term memory management via orchestrator agents and specialized attention allocation through coordinated workers, enabling comprehensive analysis across complex multi-contract transactions without context loss. We evaluate FaultSeeker on a compiled dataset of 115 real-world malicious transactions with expert-validated annotations spanning diverse attack patterns and complexity levels. Results demonstrate that FaultSeeker significantly outperforms existing approaches, including DAppFL and leading native LLMs (GPT-4o, Claude 3.7 Sonnet, DeepSeek R1), while maintaining practical efficiency (4.4-8.6 minutes) and cost-effectiveness ($1.55-$4.53 per transaction).


## 7. Finding Bugs in MLIR Compiler Infrastructure via Lowering Space Exploration

**Authors:** Jingjing Liang (East China Normal University), Shan Huang (East China Normal University), Ting Su (East China Normal University)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334563

**中文总结:** 提出 lowering space exploration 并实现 LOBE，利用同一 MLIR 程序多条合法 lowering 路径应语义等价的不变性，自适应构造多样化 lowering 路径并对比执行结果发现编译基础设施 bug。

**Abstract:** MLIR is a widely adopted compiler infrastructure that supports multi-level IRs and reusable components. Ensuring its correctness is critical, as bugs can propagate to downstream systems. MLIR provides a lowering mechanism that transforms high-level programs into low-level representations through configurable sequences of passes, and allows multiple valid lowering paths for a given program. This gives rise to a lowering equivalence property: all valid lowering paths for the same MLIR program should produce semantically equivalent results. In this paper, we leverage this property and propose lowering space exploration, to effectively test the MLIR infrastructure. Our approach dynamically constructs diverse lowering paths in an adaptive, stepwise manner using atomic lowering rules combined with a feedback-based scheduling mechanism. It finds bugs by comparing the execution results across these paths. Any inconsistencies indicate potential bugs in the MLIR infrastructure. To the best of our knowledge, this is the first work to test MLIR from the perspective of exploring its compilation space. We implement our approach in a tool named LOBE and evaluate it on latest MLIR versions. LOBE discovers 40 previously unknown bugs, including 10 miscompilations and 30 crash bugs, with 25 confirmed/fixed.


## 8. Finding Bugs in WebAssembly Interface Type Binding Generators

**Authors:** Ethan Stanley (University of Utah), Eric Eide (University of Utah)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334429

**中文总结:** 对 wit-bindgen 与 wit-bindgen-go 两个 WIT 绑定生成器实施随机差分测试，首次系统发现 WebAssembly Component Model 绑定代码生成中的运行时缺陷（含崩溃与静默数据损坏）。

**Abstract:** The WebAssembly Component Model is an emerging standard for assembling applications from parts that are implemented in WebAssembly. Unlike ordinary WebAssembly modules, components implement their interfaces in a standardized way, enabling the interoperation of software parts compiled to WebAssembly from different programming languages. A component essentially wraps an ordinary module with binding code , created by a WebAssembly Interface Type (WIT) binding generator , to adapt the module to the WebAssembly component standard. Errors in the generation of binding code can lead to hard-to-diagnose run-time errors, including crashes and silent data corruption, in applications built from WebAssembly components. Prior published work on WebAssembly testing has focused on finding bugs in WebAssembly compilers and runtimes, and has overlooked the potential for bugs in the generation of binding code. In this experience paper, we detail and evaluate our approach to addressing this oversight.

We implemented a system to perform random differential testing for two WIT binding generators, called wit-bindgen and wit-bindgen-go. Our system uses these binding generators to produce multiple WebAssembly components with the same behavior from programs written in different high-level languages. If the components’ run-time behaviors differ, we expect that there is a bug in one of the generated bindings. Using our framework, we discovered seven previously unknown code-generation defects in wit-bindgen and wit-bindgen-go. We analyze these bugs in this paper and, in addition, share lessons learned that can guide future efforts to test binding generators.


## 9. Hypergraph Neural Network-based Multi-Granular Root Cause Localization for Microservice Systems

**Authors:** Yaxiao Li (Xidian University), Lu Wang (Xidian University), Chenxi Zhang (Xidian University), Qingshan Li (Xidian University), Siming Rong (Xidian University), Baiyang Wen (Xidian University), Xuyang Li (Purdue University), Kun Ma (Xidian University), Quanwei Du (Xidian University), KeYang Li (Xidian University), Lingfeng Pan (Xidian University), Xinyue Li (Peking University), MingXuan Hui (Xidian University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334405

**中文总结:** 提出 HyperRCA，用超图神经网络建模微服务一对多部署/依赖/从属关系，实现节点、服务、实例多粒度根因定位；克服普通图难以表达复杂组件交互的局限。

**Abstract:** Modern enterprises are increasingly adopting microservice architectures for their flexibility and scalability. However, in the face of ever-changing business requirements, the relationships between system components have become increasingly complex, resulting in significant challenges in maintaining system robustness. In recent years, multimodal data-driven approaches based on graph neural networks have emerged as a predominant solution for root cause localization in microservice systems. Our detailed analysis of architectural characteristics and existing research reveals two critical limitations. First, ordinary graph is insufficient to represent the one-to-many relationships inherent in microservice component interactions , such as deployment, subordinate, and dependency. Secondly, the current multimodal data-based method has difficulty in performing localization on faults occurring on nodes, services, and instances at the same time.

To address these challenges, we propose HyperRCA, a novel multi-granular root cause analysis approach based on hypergraph neural networks. Our approach models system states during faults via a hypergraph with instances as nodes, explicitly capturing heterogeneous relationships through three innovative hyperedge designs: deployment hyperedges for infrastructure dependencies, subordinate hyperedges for service hierarchies, and dependency hyperedges for inter-component interactions. We used hypergraph neural networks and multi-layer perceptrons to train a root cause localization model based on hyperedge features to achieve multi-granularity root cause localization. Experimental evaluations demonstrate significant performance improvements over state-of-the-art approaches. HyperRCA achieves a maximum HR@5 improvement of 40.43% on single-granularity datasets and 203.57% in multi-granularity scenarios.


## 10. Improving LLM-based Log Parsing by Learning from Errors in Reasoning Traces

**Authors:** Wang Jialai (National University of Singapore), Juncheng Lu (Southeast University), Jie Yang (Wuhan University), Junjie Wang (Institute of Software at Chinese Academy of Sciences), Zeyu Gao (Tsinghua University), Chao Zhang (Tsinghua University), Zhenkai Liang (NUS), Ee-Chien Chang (School of Computing, NUS)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334402

**中文总结:** 提出 TraceDoctor，分析 LLM 日志解析推理 trace 中的失败原因并归纳为 29 类高层错误类型，据此定向生成 log variant 微调模型；五个 SOTA 推理 LLM 的 PA/GA 平均最高分别提升 17.3% 与 16.3%。

**Abstract:** Recent advances in reasoning-capable large language models (LLMs) have led to their application in a wide range of tasks, including log parsing. These LLMs generate intermediate reasoning traces during inference, offering a unique opportunity to analyze and improve their performance. In this work, we investigate how reasoning traces can be leveraged to enhance LLM-based log parsers. We propose TraceDoctor, a framework that analyzes reasoning traces associated with parsing errors to understand the causes of failure. We categorize these error causes into high-level error types and design targeted log variant generation strategies guided by these high-level error types. The generated variants are then used to fine-tune the LLMs. We instantiate five state-of-the-art (SOTA) reasoning-capable LLMs as log parsers and identify 29 distinct high-level error types. Our approach improves their average parsing accuracy by up to 17.3% and 16.3% on parsing accuracy (PA) and group accuracy (GA), respectively.


## 11. Issue Localization via LLM-Driven Iterative Code Graph Searching

**Authors:** Zhonghao Jiang (Zhejiang University), Xiaoxue Ren (Zhejiang University), Meng Yan (Chongqing University), Wei Jiang (Ant Group), Yong Li (Ant Group), Zhongxin Liu (Zhejiang University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334338

**中文总结:** 提出 IGSIL，无需训练或索引，通过「模块调用图文件级广度探索 + 函数级深度分析」的两阶段代码图搜索，平衡 LLM 驱动 issue 定位的搜索广度与深度；在 SWE-bench 等基准上优于现有方法。

**Abstract:** Issue solving aims to generate patches to fix reported issues in real-world code repositories according to issue descriptions. Issue localization forms the basis for accurate issue solving. Recently, large language model (LLM) based issue localization methods have demonstrated state-of-the-art performance. However, these methods either search from files mentioned in issue descriptions or in the whole repository and struggle to balance the breadth and depth of the search space to converge on the target efficiently. Moreover, they allow LLM to explore whole repositories freely, making it challenging to control the search direction to prevent the LLM from searching for incorrect targets. Meanwhile, because LLMs may not correctly produce the required interaction formats with the environment, they suffer from search failures.

This paper introduces IGSIL, an LLM-driven, powerful function-level issue localization method without training or indexing. To balance search breadth and depth, IGSIL employs a two-phase code graph search strategy. It first conducts broad exploration at the file level using dynamically constructed module call graphs, and then performs in-depth analysis at the function level by expanding the module call graph into a function call graph and executing iterative searches. To precisely control the search direction, IGSIL designs a pruner to filter unrelated directions and irrelevant contexts. To avoid incorrect interaction formats in long contexts, IGSIL introduces a reflection mechanism that uses additional independent queries in short contexts to enhance formatted abilities. Experiment results demonstrate that IGSIL achieves a Top-1 localization accuracy of 43.3% and 44.6% on SWE-bench Lite and SWE-bench Verified, respectively, with Qwen2.5-Coder-32B, average outperforming the state-of-the-art methods by 96.04%. When IGSIL is integrated into an issue-solving method, Agentless, the issue resolution rate improves by 2.98%–30.5%.


## 12. Let the Code Speak: Incorporating Program Dynamic State for Better Method-Level Fault Localization

**Authors:** Yihao Qin, Shangwen Wang (National University of Defense Technology), Bo Lin (National University of Defense Technology), Xin Peng, Sheng Ouyang (National University of Defense Technology), Liqian Chen (National University of Defense Technology), Xiaoguang Mao (National University of Defense Technology)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334296

**中文总结:** 提出 PingFL，首个将 print debugging 引入 LLM 故障定位的系统：FL agent 分析根因并提名可疑位置，PD agent 多轮插入打印验证动态程序状态；相比仅静态分析的 LLMFL，显著降低误报与幻觉。

**Abstract:** Fault localization (FL) is a critical but time-consuming part of software debugging. With the continuous improvement of the Large Language Models (LLMs) in their code capabilities, the increasing demand for automated software development and maintenance has encouraged more researchers to focus on building LLM-based Fault Localization (LLMFL) systems. However, existing LLMFL techniques are typically restricted to predicting bug locations by analyzing static code , while overlooking crucial dynamic program state of the software. This lack of context makes LLMs prone to generating “hallucinations”, incorrectly identifying bug-free code as suspicious. To address this, this paper introduces PingFL, the first LLMFL system that incorporates print debugging techniques for more accurate fault localization. PingFL comprises a Fault Localization (FL) agent and a Print Debugging (PD) agent. The FL agent is tasked with understanding the root cause through a set of callable tools. When the FL agent nominates a location as suspicious, it would entrust the PD agent to verify the suspected issue through multiple rounds of print debugging. In particular, these two agents communicate and collaborate efficiently by conveying the textual thought generated by the LLM. The evaluation on 812 real-world bugs from the Defects4J benchmark shows that PingFL can localize 450 bugs within Top-1, which significantly outperforms other LLM-based approaches by 41% to 122%. It also consistently surpasses traditional FL techniques in cross-project scenarios. A deeper dive into PingFL’s performance reveals that it exhibits specific FL strategies and tool usage patterns even without explicit instructions. Finally, PingFL proves to be cost-effective, spending an average of $0.22 and 104.62 seconds per bug, with the print debugging mechanism accounting for only $0.07 and 51.62 seconds.


## 13. LineBreaker: Finding Token-Inconsistency Bugs using Large Language Models

**Authors:** Hongbo Chen (Indiana University Bloomington), Yifan Zhang (San Diego State University), Xing Han (The Hong Kong University of Science and Technology), Tianhao Mao (Indiana University), Huanyao Rong (Indiana University Bloomington), Yuheng Zhang (Tsinghua University), Hang Zhang (Indiana University), XiaoFeng Wang (ACM member), Luyi Xing (Indiana University Bloomington/University of Illinois Urbana-Champaign), Xun Chen (Samsung Research America)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334273

**中文总结:** 系统评估 LLM 检测 token 不一致性缺陷（TIB）的能力后，提出级联系统 LineBreaker，缓解 GPT-4 关注非 TIB 片段及成本/规模问题；在真实代码库上实现更高精度与可扩展的 TIB 检测。

**Abstract:** Token-inconsistency bugs (TIBs) involve the misuse of syntactically valid yet incorrect code tokens, such as misused variables and erroneous function invocations, which can often lead to software bugs. Unlike simple syntactic bugs, TIBs occur at the semantic level and are subtle - sometimes remain undetected for years. Traditional detection methods, such as static analysis and dynamic testing, often struggle with TIBs due to their versatile and context-dependent nature. However, advancements in large language models (LLMs) like GPT-4 present new opportunities for automating TIB detection by leveraging these models’ semantic understanding capabilities.

This paper reports the first systematic measurement of LLMs’ capabilities in detecting TIBs, revealing that while GPT-4 shows promise, it exhibits limitations in precision and scalability. Specifically, its detection capability is undermined by the model’s tendency to focus on the code snippets that do not contain TIBs; its scalability concern arises from GPT-4’s high cost and the massive amount of code requiring inspection. To address these challenges, we introduce LineBreaker, a novel and cascaded TIB detection system. LineBreaker leverages smaller, code-specific, and highly efficient language models to filter out large numbers of code snippets unlikely to contain TIBs, thereby significantly enhancing the system’s performance in terms of precision, recall, and scalability. We evaluated LineBreaker on 154 Python and C GitHub repositories, each with over 1,000 stars, uncovering 123 new flaws, 45% of which could be exploited to disrupt program functionalities. Out of our 69 submitted fixes, 41 have already been confirmed or merged


## 14. LLM-Based Identification of Null Pointer Exception Patches

**Authors:** Tahir Ullah (Beijing Institute of Technology), Waseem Akram (Beijing Institute of Technology), Fiza Khaliq (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334495

**中文总结:** 提出 AACC（Augmented Agentic Commit Classification），利用 commit 消息与代码结构语义，通过优质样例筛选、增强知识库、优先级 agent 与迭代 refinement，从大规模不平衡 commit 中准确识别 NPE 修复补丁。

**Abstract:** Null Pointer Exceptions (NPEs) are one of the leading causes of software crashes and runtime errors, posing significant challenges for developers. Although existing methods attempt to detect and classify NPE fixes, they often fall short due to irrelevant or noisy data, a lack of contextual understanding, and inefficiency in processing large and imbalanced datasets. To overcome these challenges, we propose an approach, called \textit{ Augmented Agentic Commit Classification} (\textit{AACC} for short), to accurately categorize commit patches as NPE fixes or non-NPE. \textit{AACC} leverages the code structure and contextual insights from commit messages to capture the semantic intent behind code modifications. It features four key advancements: (1) Best example selection that filters high-quality, contextually relevant commits to ensure the model learns from contextual rich and accurate data; (2) an augmented knowledge base that enriches classification by combining contextual metadata, program semantics, and bug fix patterns; (3) a prioritize agent that ranks commits based on relevance and impact, optimizing resource allocation and boosting efficiency; and (4) an iterative refinement process that enables the model to learn from feedback to correct misclassifications, reducing false negative rates. Our evaluation results on ChatGPT-4o suggest that it outperforms the state-of-the-art approaches by improving the F1 score from 72.07% to 98.03%.


## 15. LLM-Powered Multi-Agent Collaboration for Intelligent Industrial On-Call Automation

**Authors:** Ruowei Fu (Nankai University), Yang Zhang (ByteDance Inc.), Zeyu Che (Nankai University), Xin Wu (ByteDance Inc.), Zhenyu Zhong (Nankai University), Zhiqiang Ren (ByteDance Inc.), Shenglin Zhang (Nankai University), Feng Wang (ByteDance Inc.), Yongqian Sun (Nankai University), Xiaozhou Liu (ByteDance Inc.), Kexin Liu (Nankai University), Yu Zhang (ByteDance Inc.)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334482

**中文总结:** 提出 OncallX 端到端工业 on-call 自动化系统，结合外部知识库增强查询、多轮对话与基于树搜索的多专家 agent 协作生成处置方案，并在无法自动解决时精准分派团队；在头部在线视频服务商生产环境验证响应与分派效果。

**Abstract:** In large-scale enterprises, on-call engineers (OCEs) are critical for ensuring service availability and reliability. However, as incidents grow in volume and complexity, traditional manual on-call processes are becoming increasingly inadequate. Recent advances in large language models (LLMs) have demonstrated remarkable capabilities in reasoning and multi-agent collaboration, presenting new opportunities for automation. We propose OncallX, an end-to-end automated on-call system designed for real-world industrial scenarios that integrates LLMs with multi-agent cooperation to enable intelligent and efficient incident management. OncallX first enhances user queries by leveraging external knowledge bases and multi-turn dialogue interactions. Subsequently, multiple expert agents collaborate through tree-search-based mechanisms to generate effective responses and solutions. When incidents cannot be resolved automatically, OncallX accurately assigns them to the most appropriate teams. Comprehensive experiments conducted in the real-world production environment of a top-tier global online video service provider demonstrate that OncallX efficiently responds to incidents and accurately triages tickets, significantly outperforming existing methods in both automated metrics and human evaluations. Furthermore, OncallX has been successfully deployed in production for two months, during which it has substantially enhanced on-call efficiency, reducing average incident response time to just 21 seconds and average triage time to 4 seconds—representing a transformative improvement in operational excellence.


## 16. LogAction: Consistent Cross-system Anomaly Detection through Logs via Active Domain Adaptation

**Authors:** Chiming Duan (Peking University), Minghua He (Peking University), Pei Xiao (Peking University), Tong Jia (Institute for Artificial Intelligence, Peking University, Beijing, China), Xin Zhang (Peking University), Zhewei Zhong (Bytedance), Xiang Luo (Bytedance), Yan Niu (Bytedance), Lingzhe Zhang (Peking University, China), Yifan Wu (Peking University), Siyu Yu (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Weijie Hong (Peking university), Ying Li (School of Software and Microelectronics, Peking University, Beijing, China), Gang Huang (Peking University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334497

**中文总结:** 提出 LogAction，基于主动域自适应的日志异常检测：用成熟系统标注数据缓解冷启动，并以 free energy 与不确定性采样选取分布边界日志做少量人工标注，弥合源/目标系统分布差异；在六组跨系统数据集上优于迁移/主动学习基线。

**Abstract:** Log-based anomaly detection is a essential task for ensuring the reliability and performance of software systems. However, the performance of existing anomaly detection methods heavily relies on labeling, while labeling a large volume of logs is highly challenging. To address this issue, many approaches based on transfer learning and active learning have been proposed. Nevertheless, their effectiveness is hindered by issues such as the gap between source and target system data distributions and cold-start problems. In this paper, we propose LogAction, a novel log-based anomaly detection model based on active domain adaptation. LogAction integrates transfer learning and active learning techniques. On one hand, it uses labeled data from a mature system to train a base model, mitigating the cold-start issue in active learning. On the other hand, LogAction utilize free energy-based sampling and uncertainty-based sampling to select logs located at the distribution boundaries for manual labeling, thus addresses the data distribution gap in transfer learning with minimal human labeling efforts. Experimental results on six different combinations of datasets demonstrate that LogAction achieves an average 93.01% F1 score with only 2% of manual labels, outperforming some state-of-the-art methods by 26.28%. Website: https://logaction.github.io/


## 17. LogMoE: Lightweight Expert Mixture for Cross-System Log Anomaly Detection

**Authors:** Jiaxing Qi (Beihang University), Zhongzhi Luan (Beihang University), Shaohan Huang (Beihang University), Carol Fung (Concordia University), Yuchen Wang (Beihang University), Aibin Wang (Beihang University), Hongyu Zhang (Chongqing University), Hailong Yang (Beihang University, China), Depei Qian (Beihang University, China)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334514

**中文总结:** 提出 LogMoE，无解析、轻量 Mixture-of-Experts 跨系统日志异常检测：用多成熟系统标注日志训练专家并通过门控集成，适应未见目标系统与异构日志格式；在八种数据集、三种泛化场景下，尤其在目标标注稀缺时保持稳健泛化。

**Abstract:** Robust anomaly detection in system logs plays a crucial role in maintaining stable and reliable software operations. However, existing methods often struggle to accommodate evolving log formats and distributional shifts across systems, as they heavily rely on large volumes of labeled data, log parsing, and predefined event templates. To address these challenges, we propose LogMoE, a scalable and parsing-free log anomaly detection framework. LogMoE utilizes labeled logs from multiple mature systems to train a set of lightweight expert models, which are integrated via a gating mechanism within a Mixture-of-Experts (MoE) architecture. This design enables LogMoE to generalize effectively to previously unseen target systems. By eliminating the need for log parsing, our approach remains robust against the heterogeneity of log formats and syntactic structures. We conduct extensive evaluations on eight log datasets under varying generalization scenarios: single-system, homogeneous-system, and heterogeneous-system. Experimental results demonstrate that LogMoE consistently achieves robust generalization, particularly under conditions with scarce labeled data in the target system. As such, LogMoE provides a scalable, parsing-free, and generalization-capable solution tailored for complex and continuously evolving software system environments, positioning it as a future-ready approach to log anomaly detection.


## 18. Root Cause Analysis of RISC-V Build Failures via LLM and MCTS Reasoning

**Authors:** Weipeng Shuai (Institute of Software, Chinese Academy of Sciences), Jie Liu (Institute of Software, Chinese Academy of Sciences), Zhirou Ma (Institute of Software, Chinese Academy of Sciences), Liangyi Kang (Institute of Software, Chinese Academy of Sciences), Zehua Wang (Institute of Software, Chinese Academy of Sciences), Shuai Wang (Institute of Software, Chinese Academy of Sciences), Dan Ye (Institute of Software at Chinese Academy of Sciences), Hui Li, Wei Wang (Institute of Software at Chinese Academy of Sciences), Jiaxin Zhu (Institute of Software at Chinese Academy of Sciences)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334506

**中文总结:** 提出两阶段 RISC-V 构建失败根因分析：RV-LAD 做模板压缩与阶段感知 LLM 异常检测，MCTS-RCA 结合领域知识库与 MCTS 多源推理；在 117 个标注案例上诊断准确率 75.2%。

**Abstract:** Build failures are a major obstacle in RISC-V software migration, often involving complex interactions across logs, configurations, and environments. Traditional diagnostic tools struggle with the unstructured, multi-phase nature of build logs and lack semantic reasoning. We propose a two-stage framework for automated root cause analysis. RV-LAD compresses logs using template-based filtering and applies phase-aware anomaly detection via few-shot LLM prompting. MCTS-RCA integrates a domain-specific knowledge base with Monte Carlo Tree Search to perform LLM-guided multi-source reasoning under classification constraints. To support evaluation, we construct a curated dataset of 117 real-world RISC-V build failures, each annotated with logs, spec files, and repair records. Experiments show our approach achieves 75.2% diagnosis accuracy, surpassing prior LLM-based and rule-based methods. It also offers interpretable reasoning traces, enabling practical and transparent diagnosis. This work provides an effective and extensible solution for RCA in emerging software ecosystems like RISC-V, bridging large language models with domain-aware inference.


## 19. Sifting Truth from Coincidences: A Two-Stage Positive and Unlabeled Learning Model for Coincidental Correctness Detection

**Authors:** Chunyan Liu (Chongqing University), Huan Xie (Chongqing University), Yan Lei (Chongqing University), Zhenyu Wu (School of Big Data & Software Engineering, Chongqing University), Jinping Wang (Chonqing University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334663

**中文总结:** 提出 EVANS，将失败用例作正样本、通过用例作无标签数据，用两阶段 PU 学习检测故障定位中的 coincidental correctness，以提升 FL 因果推断可靠性。

**Abstract:** Fault localization (FL) can identify the fault’s location by analyzing the execution information from test cases in the program. This execution information serves as the foundation for FL to infer latent causal relationships between fault entities and failed results. However, this execution information contains coincidental correctness (CC), which reduces the accuracy of FL. CC arises when a test case executes faulty program entities but still produces the correct output, leading to misleading FL inferences. In widely used datasets, the presence of CC compromises the reliability of passed test cases (i.e., negative labels). In contrast, failed test cases (i.e., positive labels) remain definitive. In FL scenarios, unlabeled data is typically abundant and primarily consists of passed test cases. Therefore, systematically leveraging positive and unlabeled data for accurate CC detection is essential, which is beneficial to FL. To tackle the problem, we propose a two-stagE positiVe and unlAbeled learning model for coiNcidental correctneSs detection, EVANS. EVANS defines failed test cases as positive samples and treats the remaining ones as unlabeled data. It comprises two core modules: (1) A module for selecting high-quality pseudo-negative samples. This module leverages vector distance metrics to identify high-quality pseudo-negative test cases, using inter-class distances computed via a pre-trained model. (2) A weakly supervised contrastive learning module. This module utilizes the labeled samples from Stage (1) to train a contrastive learning model, which then detects CC in unlabeled test cases. Experimental results demonstrate that EVANS significantly outperforms current CC detection methods.


## 20. SSR: Safeguarding Staking Rewards by Defining and Detecting Logical Defects in DeFi Staking

**Authors:** Zewei Lin (Sun Yat-sen University), Jiachi Chen (Sun Yat-sen University), Jingwen Zhang (School of Software Engineering, Sun Yat sen University), Zexu Wang (Sun Yat-sen University), Yuming Feng (Peng Cheng Laboratory), Weizhe Zhang (Harbin Institute of Technology), Zibin Zheng (Sun Yat-sen University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334683

**中文总结:** 基于 54 起安全事件与 144 份审计报告定义 DeFi staking 六类逻辑缺陷，提出 SSR 静态分析工具：LLM 抽取质押逻辑并建模，再检测奖励操纵、重复领取等漏洞。

**Abstract:** Decentralized Finance (DeFi) staking is one of the most prominent applications within the DeFi ecosystem, where DeFi projects enable users to stake tokens on the platform and reward participants with additional tokens. However, logical defects in DeFi staking could enable attackers to claim unwarranted rewards by manipulating reward amounts, repeatedly claiming rewards, or engaging in other malicious actions. To mitigate these threats, we conducted the first study focused on defining and detecting logical defects in DeFi staking. Through the analysis of 54 security incidents and 144 audit reports, we identified six distinct types of logical defects, each accompanied by detailed descriptions and code examples. Building on this empirical research, we developed SSR (Safeguarding Staking Reward), a static analysis tool designed to detect logical defects in DeFi staking contracts. SSR utilizes a large language model (LLM) to extract fundamental information about staking logic and constructs a DeFi staking model. It then identifies logical defects by analyzing the model and the associated semantic features. We constructed a ground truth dataset based on known security incidents and audit reports to evaluate the effectiveness of SSR. The results indicate that SSR achieves an overall precision of 90.91%, a recall of 86.03%, and an F1-score of 86.66%. Additionally, to assess the prevalence of logical defects in real-world smart contracts, we compiled a large-scale dataset of 15,992 DeFi staking contracts. SSR detected that 3,557 (22.24%) of these contracts contained at least one logical defect.


## 21. The Fault in our Stats

**Authors:** Alexi Turcotte (CISPA), Neev Nirav Mehta (Saarland University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334421

**中文总结:** 提出统计中间表示 SIR 及静态检查工具 stat-lint，快速检测数据科学程序是否满足统计方法假设与多重比较校正等最佳实践；评估 45 个 Python notebook 显示仅 11 个完全履行全部统计义务，过半义务未被检查。

**Abstract:** Data analysts need to be careful when they apply statistical inference techniques to data, as misuse of statistical inference methods can lead an analyst to draw the wrong conclusions. They need to be careful because, in the general case, misuse of statistics does not result in obvious problems; the numbers returned often look reasonable, and programs with misuses of statistics do not crash. In this work, we propose a technique to quickly and statically check data science programs for compliance with statistics best practice rules, including checking all assumptions made by statistical methods, as well as correcting for the multiple comparison problem, or “data dredging”. This technique is predicated on a novel statistics intermediate representation, called SIR , that encodes the details most salient to statistics. We implement this technique in a tool called stat-lint , the first statistics linter, and evaluate stat-lint on 45 Python data science notebooks, finding that only 11 fully check all obligations, only two apply any correction for multiple comparisons, and over half of obligations go unchecked.


## 22. Triangle: Empowering Incident Triage with Multi-Agent

**Authors:** Zhaoyang Yu (Tsinghua University), Aoyang Fang (Chinese University of Hong Kong, Shenzhen), Minghua Ma (Microsoft), Jaskaran Singh Walia (Microsoft), Chaoyun Zhang (Microsoft), Shu Chi (Tsinghua University), Ze Li (Microsoft Azure), Murali Chintalapati (Microsoft Azure), Xuchao Zhang (Microsoft), Rujia Wang (Microsoft), Chetan Bansal (Microsoft Research), Saravan Rajmohan (Microsoft), Qingwei Lin (Microsoft), Shenglin Zhang (Nankai University), Dan Pei (Tsinghua University), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334691

**中文总结:** 提出 Triangle 多智能体端到端云事故分诊系统，以语义蒸馏缓解异构事故数据、多角色代理与协商机制模拟工程师协作，并自动收集排障与缓解信息；在真实云环境中提升分诊准确性与效率。

**Abstract:** Experience Paper

As cloud service systems grow in scale and complexity, incidents that indicate unplanned interruptions and outages become unavoidable. Rapid and accurate triage of these incidents to the appropriate responsible teams is crucial to maintain service reliability and prevent significant financial losses. However, existing incident triage methods relying on manual operations and predefined rules often struggle with efficiency and accuracy due to the heterogeneity of incident data and the dynamic nature of domain knowledge across multiple teams.

To solve these issues, we propose Triangle, an end-to-end incident triage system based on a Multi-Agent framework. Triangle leverages a semantic distillation mechanism to tackle the issue of semantic heterogeneity in incident data, enhancing the accuracy of incident triage. Additionally, we introduce multi-role agents and a negotiation mechanism to emulate human engineers’ workflows, effectively handling decentralized and dynamic domain knowledge from multiple teams. Furthermore, our system incorporates an automated troubleshooting information collection and mitigation mechanism, reducing the reliance on human labor and enabling fully automated end-to-end incident triage. Extensive experiments conducted on a real-world cloud production environment demonstrate that Triangle significantly improved incident triage accuracy (up to 97%) and reduced Time to Engage (TTE) by as much as 91%, demonstrating substantial operational impact across diverse cloud services.


## 23. United We Stand: Towards End-to-End Log-based Fault Diagnosis via Interactive Multi-Task Learning

**Authors:** Minghua He (Peking University), Chiming Duan (Peking University), Pei Xiao (Peking University), Tong Jia (Institute for Artificial Intelligence, Peking University, Beijing, China), Siyu Yu (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Lingzhe Zhang (Peking University, China), Weijie Hong (Peking university), Jing Han (ZTE Corporation), Yifan Wu (Peking University), Ying Li (School of Software and Microelectronics, Peking University, Beijing, China), Gang Huang (Peking University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334674

**中文总结:** 提出 Chimera，以交互式多任务学习在数据、特征与诊断结果层面双向耦合异常检测与根因定位，实现端到端日志故障诊断；在两个公开数据集与一个工业数据集上整体优于现有任务独立方法。

**Abstract:** Log-based fault diagnosis is essential for maintaining software system availability. However, existing fault diagnosis methods are built using a task-independent manner, which fails to bridge the gap between anomaly detection and root cause localization in terms of data form and diagnostic objectives, resulting in three major issues: 1) Diagnostic bias accumulates in the system; 2) System deployment relies on expensive monitoring data; 3) The collaborative relationship between diagnostic tasks is overlooked. Facing this problems, we propose a novel end-to-end log-based fault diagnosis method, Chimera, whose key idea is to achieve end-to-end fault diagnosis through bidirectional interaction and knowledge transfer between anomaly detection and root cause localization. Chimera is based on interactive multi-task learning, carefully designing interaction strategies between anomaly detection and root cause localization at the data, feature, and diagnostic result levels, thereby achieving both sub-tasks interactively within a unified end-to-end framework. Evaluation on two public datasets and one industrial dataset shows that Chimera outperforms existing methods in both anomaly detection and root cause localization, achieving improvements of over 2.92%~5.00% and 19.01%~37.09%, respectively. It has been successfully deployed in production, serving an industrial cloud platform. Website: https://chimera4log.github.io/


## 24. When AllClose Fails: Round-Off Error Estimation for Deep Learning Programs

**Authors:** Qi Zhan (Zhejiang University), Xing Hu (Zhejiang University), Yuanyi Lin (Huawei Technologies), Tongtong Xu (Huawei), Xin Xia (Zhejiang University), Shanping Li (Zhejiang University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://ieeexplore.ieee.org/document/11334424

**中文总结:** 提出 RENDER，结合动态区间算术与舍入误差分析估计深度学习两实现间的最大浮点误差，区分可接受数值偏差与实现 bug；较 SATIRE 多识别 40% 误差且平均快 19 倍。

**Abstract:** Deep learning programs are continually enhanced for improved performance through the use of kernel-level optimizations, parallel training, and low-precision arithmetic. These optimizations provide different implementations that are mathematically equivalent. Round-off error in floating-point computations can lead to differences in the outputs of these implementations, even when the mathematical equivalence holds. When the outputs of customized and reference implementations exceed the tolerance thresholds, it is difficult for developers to distinguish between acceptable round-off errors and implementation bugs. This paper proposes an approach called RENDER to classify the numerical errors between two implementations based on estimating the maximum round-off error. RENDER combines dynamic interval arithmetic and round-off error analysis to compute scalable and tight output bounds. We demonstrate the effectiveness of our method on real-world issues by comparing it with the state-of-the-art tool, SATIRE. Experimental results show that our approach identifies 40% more errors and achieves an average speedup of 19× compared to the baseline, enabling developers to debug and optimize implementations more efficiently.

