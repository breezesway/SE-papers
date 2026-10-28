# ISSTA 2026 Research Track — Awarded Papers

Source: https://www.conference-publishing.com/toc/ISSTA26/noabs (ACM SIGSOFT Distinguished Paper Award badges); research track: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Total: 19 papers

## Award breakdown

| Award | # Papers |
| --- | ---: |
| ACM SIGSOFT Distinguished Paper Award | 19 |

## Papers

## 1. Are We Stuck? Modeling and Detecting Deadlocks in Multi-Autonomous Vehicle Systems

**Authors:** Mingfei Cheng (Singapore Management University), Xiaofei Xie (Singapore Management University), Lili Quan (Singapore Management University (SMU)), Yuan Zhou (Zhejiang Sci-Tech University)

**Categories:** Systems, Mobile, and UI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832177

**中文总结:** 首次形式化多自动驾驶车辆系统中的死锁问题，并提出 WaitWatch 测试框架，通过时空轨迹交叉对齐与定向变异诱导循环等待。在三种 ADS 上平均生成 2.28 倍于最佳基线的死锁场景，揭示现有系统协作活性不足。

**Abstract:** Autonomous driving system (ADS) testing is essential to ensure the safety and reliability of autonomous vehicles (AVs) prior to deployment. As ADSs are increasingly deployed in multi-AV traffic environments, it becomes crucial to assess their cooperative performance, particularly with respect to deadlock, a fundamental liveness issue in concurrent systems that can lead to traffic congestion and prolonged stalling. However, the analysis and testing of ADSs’ cooperative capabilities with respect to deadlock remain largely underexplored. In this work, we present the first systematic study of deadlock in multi-AV systems. We formalize deadlock in autonomous driving using a time-indexed wait-for relation grounded in vehicles’ planned trajectories and road-region occupancy. Building on this formalization, we propose WaitWatch, a wait-for–oriented testing framework that steers scenario generation via spatio-temporal intersection alignment of executed trajectories to induce circular wait patterns. WaitWatch integrates a Deadlock Judge, Intersection Alignment Feedback, and Intersection Oriented Mutation to efficiently uncover latent deadlock scenarios. We conduct an extensive evaluation on three representative ADSs. Experimental results show that, on average, WaitWatch generates 2.28×more deadlock scenarios (DLSs) than the best-performing baseline. By shifting the focus from single-AV evaluation to multi-AV cooperation, our approach identifies a range of previously unknown deadlock behaviors, revealing significant limitations in the cooperative and liveness capabilities of current ADSs. Our findings highlight a fundamental safety–liveness trade-off in deadlock resolution and emonstrate the need for systematic deadlock-aware testing in the development and validation of autonomous driving systems.


## 2. Beyond Similarity Scores: Evidence-Based Third-Party Library Detection for C/C++ Binaries

**Authors:** CHENGYUE LIU, Zhengzi Xu (Imperial Global Singapore), Lyuye Zhang (Nanyang Technological University), Wu Jiahui (Nanyang Technological University, Singapore), Kaixuan Li (Nanyang Technological University), Yang Liu (Nanyang Technological University)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832125

**中文总结:** 提出 BLADE，将 C/C++ 二进制第三方库检测重构为多源证据验证流程，用 LLM 结构化工作流过滤误报。在 3403 二进制/1016 库基准上 F1 达 95.63%，较最佳基线提升 41.83 个百分点，已商用部署。

**Abstract:** Detecting third-party libraries (TPLs) in C/C++ binaries is essential for software supply chain security, enabling vulnerability identification and license compliance. Existing methods predominantly rely on similaritymatching: extracting features from binaries and comparing them against library databases. However, similarityscores alone cannot reliably determine library presence. Low similarity causes false negatives when matchablefeatures are limited. More critically, high similarity does not guarantee accuracy: libraries often share featuresthrough shared dependencies, forks, or similar functionality, causing multiple candidates to match even whenonly one is present. These issues suggest that similarity matching is effective for narrowing candidates butinsufficient as the final decision mechanism. Rather than relying solely on similarity scores, reliable detectionrequires multi-source evidence to verify each candidate.

To this end, we propose BLADE, which reframes TPL detection as evidence-based candidate verification.Instead of relying on similarity scores to make final decisions, BLADE retrieves candidates broadly to mitigatefalse negatives, and then collects evidence from multiple sources, which an LLM analyzes through structuredverification workflows to filter false positives: first confirming candidates with clear identity markers, thensystematically checking remaining candidates against common false positive patterns. To evaluate BLADE,we build the largest C/C++ binary TPL benchmark to date, comprising 3,403 binaries and 1,016 libraries.Results show that BLADE achieves 97.60% precision and 93.74% recall (F1: 95.63%), improving F1-score by 41.83percentage points over the best baseline. The average cost is $0.0378 per binary. BLADE has been deployed ina commercial software composition analysis product, demonstrating practical feasibility at scale.


## 3. Characterizing and Repairing Obsolete Android GUI Tests under UI Evolution

**Authors:** Shiwen Song (Singapore Management University), Yiheng Xiong (Singapore Management University), Wenbo Guo (Nanyang Technological University), Manqi Sun (The University of Hong Kong), Jiaolong Kong (Singapore Management University), Xiaofei Xie (Singapore Management University)

**Categories:** Systems, Mobile, and UI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832300

**中文总结:** 本文构建含 736 个过时 Android GUI 测试的基准，并提出 GUIRevive，通过语义感知推理与目标导向 UI 探索修复控件识别歧义和控件不可达问题。成功修复 86.4% 的过时测试，工业部署修复率达 93%。

**Abstract:** Graphical user interface (GUI) tests are widely used in regression testing of mobile applications (apps) to validate app behavior from the user’s perspective. However, frequent app evolution, such as UI redesigns and feature updates, often renders existing GUI tests obsolete, even when underlying functionality remains unchanged. Automatically repairing such tests is critical for maintaining test suites and reducing substantial manual effort. Despite the practical importance, there is still a lack of a systematic understanding of the characteristics of obsolete GUI tests and a publicly available benchmark to support their study. To fill this gap, we construct a benchmark comprising 736 obsolete GUI tests collected from 36 real-world mobile apps across 668 historical versions. We then conduct a large-scale empirical study that reveals two major challenges in repairing obsolete GUI tests: First, identifying the intended target widget is difficult because widget attributes are frequently missing or unstable, and visually similar widgets may correspond to different functionalities. Second, the target widget is often no longer directly reachable from the failure state, as it may be hidden behind additional UI interactions or relocated to another screen. To address these challenges, we further propose GUIRevive, an automated GUI test repair approach that addresses semantic ambiguity in widget identification and target unreachability under UI evolution by integrating semantic-aware reasoning, functionality-preserving validation, and goal-guided UI exploration. Our evaluation shows that GUIRevive successfully repairs 86.4% of obsolete GUI tests and significantly outperforms state-of-the-art repair techniques by up to 220%.  Moreover, GUIRevive has been deployed in industrial settings, achieving a 93% repair success rate on industrial mobile apps.


## 4. Characterizing Real-World Bugs in Tile Programs for Automated Bug Detection

**Authors:** Ravishka Rathnasuriya (The University of Texas - Dallas), Zihe Song (University of Texas at Dallas), Nidhi Majoju (University of Texas at Dallas), Tingxi Li (The University of Texas at Dallas), Aaryaa Moharir (The University of Texas at Dallas), Wei Yang (UT Dallas), Tao Xie (Peking University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832271

**中文总结:** 本文首次系统刻画 Tile 编程框架中的代码生成缺陷，分析 GitHub 上 301 个真实 bug 报告并归纳根因、症状、触发 oracle 与修复策略。为 Tile 编译器基础设施的调试、测试与修复工具提供基础实证依据。

**Abstract:** Tile-based programming frameworks are increasingly adopted to write high-performance GPU kernels in domains such as deep learning and scientific computing. While these frameworks enhance productivity and hardware utilization, their multi-stage compilation pipelines introduce distinct code generation bugs that are tightly coupled to input shapes, data types, and backend targets. These bugs often manifest as silent correctness or performance issues, making them difficult to detect using existing compiler testing tools. Additionally, the unique programming conventions of tile domain specific languages complicate root cause identification, while fixing such bugs demands specialized knowledge of tile abstractions and compilation pipelines. Despite the growing adoption of tile-based systems, their code generation bugs remain largely unexplored.

This paper presents the first systematic study of tile-program code generation bugs. We analyze 301 real-world bug reports from GitHub and categorize their root causes, symptoms, input patterns, test oracles that trigger these bugs and the strategies used to fix them. Our study provides foundational insights for building debugging, testing, and repair tools tailored to tile-based compiler infrastructures.


## 5. Code-MUE: Measuring Code LLMs’ Uncertainty through Execution-Based Semantic Interaction Graphs

**Authors:** xiaoning ren, Yinxing Xue (Institute of AI for Industries, Chinese Academy of Sciences), Lei Ma (The University of Tokyo & University of Alberta), Yuheng Huang (The University of Tokyo)

**Categories:** Software Engineering for AI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832276

**中文总结:** Code-MUE 基于执行结果构建语义交互图，用 Von Neumann 熵量化 Code LLM 输出的语义不确定性，无需访问模型内部。在八个 LLM 上与功能正确性的 Spearman 相关最高达 -0.98，显著优于文本与嵌入基线。

**Abstract:** As Code Large Language Models (LLMs) become central to modern software engineering, their inherent stochasticity poses significant real-world risks, where even minor errors can lead to severe functional, security, or safety consequences. Reliable automation, therefore, demands the ability to distinguish between confident, well-supported predictions and stochastic guessing. However, existing uncertainty estimation methods face a critical gap: white and grey-box techniques are often inapplicable to closed-source models, while standard “black-box” text metrics fail to capture the unique fragility of code, where syntactic variation does not always imply semantic divergence. To bridge this syntax-semantics gap, we introduce Code-MUE, a purely black-box framework that measures uncertainty through execution-based Semantic Interaction Graphs. Unlike prior approaches that rely on superficial textual similarity, Code-MUE grounds uncertainty in observable runtime behavior, calculating the Von Neumann entropy of the solution space to quantify global semantic diversity. A large-scale empirical study across eight state-of-the-art LLMs demonstrates that Code-MUE achieves a strong negative correlation with functional correctness (Spearman’s correlation up to -0.98), significantly outperforming lexical and embedding-based baselines while enabling robust risk detection and selective prediction in practical workflows.


## 6. Do Coverage and Mutation Scores of LLM-Generated Test Suites Correlate With Their Effectiveness? (Replicability Study)

**Authors:** Junda Zhao (Department of Mechanical and Industrial Engineering, University of Toronto), Shurui Zhou (University of Toronto), Eldan Cohen (Department of Mechanical and Industrial Engineering, University of Toronto)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832093

**中文总结:** 本文大规模复现 Inozemtseva 与 Papadakis 两项研究，检验 LLM 生成测试套件中覆盖率、变异分与真实缺陷检出率的相关性。发现这些代理指标的有效性高度依赖场景：回归测试设定下仍有参考价值，但被测代码本身含 bug 时则不可靠。

**Abstract:** Recent advances in large language models (LLMs) have driven growing interest in using LLMs to automate test generation. Prior work commonly evaluates generated test suites using proxy metrics such as code coverage and mutation score. However, studies by Inozemtseva et al. and Papadakis et al. show that, for human-written tests, correlations among coverage, mutation, and real-bug detection can largely vanish once test suite size is controlled, raising concerns about the validity of evaluations based on proxy metrics. It also remains unclear whether these conclusions carry over to LLM-generated tests, given that prevailing LLM-based test-generation workflows differ substantially from traditional approaches.

In this paper, we conduct a large-scale replication study of these two prior works using a wide range of test suites generated by a diverse set of LLMs, and re-examine the relationships among coverage, mutation, and real-bug detection effectiveness. Our findings diverge substantially from prior results. We show that the usefulness of coverage and mutation is highly context-dependent: in regression-style settings where the code provided to the LLM can be reasonably assumed bug-free, these metrics can provide meaningful signals when comparing across models; in another common scenario where the code-under-test may already be buggy and the goal is to expose the bug within code-under-test, they no longer serve as reliable indicators. We also find little evidence that test suite size is a dominant confounder for correlations among coverage, mutation, and real-bug detection for LLM-generated tests. Based on these findings, we discuss how to interpret results from prior studies and provide actionable guidance for evaluating LLM-based test generation.


## 7. Efficient Predictive Monitoring of Message Passing Interface Programs

**Authors:** Jiaqiang Yao (College of Computer, National University of Defense Technology), Haocheng Geng (College of Computer Science and Technology, National University of Defense Technology), Zhenbang Chen (College of Computer, National University of Defense Technology)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832278

**中文总结:** MPI-PRV 从单次 MPI 程序执行迹出发，基于迹等价预测合法调度变体并检验时序属性，用向量时钟强制执行 MPI 语义依赖约束。在 13 个真实应用的 38 组配置上全部成功分析，运行时间与内存较 MPI-SV 降低数个数量级。

**Abstract:** The Message Passing Interface (MPI) is the standard programming model for high-performance computing, yet nondeterministic scheduling in concurrent executions makes reliability assurance highly challenging. Beyond deadlocks, property-related bugs such as modifying a send buffer before a nonblocking send completes or accessing a freed RMA window are often hard to reproduce and validate, as they typically manifest only under rare event interleavings and can be both latent and catastrophic. Existing dynamic checkers usually cover only the observed schedule of a single execution; dynamic verification largely focuses on deadlocks; and static techniques scale poorly to medium-to-large programs, often timing out or running out of memory. Overall, existing techniques do not support scalable analysis of temporal properties in large MPI programs.

To address these limitations, we propose the first efficient predictive monitoring approach for temporal properties in MPI programs. From a single execution, we collect an event trace and use trace equivalence to predict the set of legal equivalent executions under the same input. We then check whether any predicted execution satisfies the target property. To make this process sound, we formalize three correctness criteria for MPI trace reordering and enforce them through MPI-semantics-driven dependency extraction, tracked with vector clocks. To improve efficiency, we exploit the bounded length of a pattern language and reduce long-trace reordering to reordering short patterns. We implement our approach in MPI-PRV, instantiate ten representative MPI bug properties, and evaluate it on 13 real-world MPI applications with 38 configurations. MPI-PRV successfully and correctly analyzes all $38$ tasks, whereas MPI-SV and MUST analyze only $14$ and $11$ tasks, respectively. MPI-PRV also achieves orders-of-magnitude reductions in runtime and memory usage, demonstrating strong efficiency and scalability for large MPI programs.


## 8. Evaluating the Impact of Explainable AI on Trust in AI-Assisted Code Review

**Authors:** Zhenhan Gao (Technical University of Munich), Marvin Muñoz Barón, Umm-e Habiba (Technical University Munich), Daniel Graziotin (University of Hohenheim), Stefan Wagner (Technical University of Munich)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832184

**中文总结:** 通过 34 人 within-subjects 用户研究评估 XAI 对 AI 辅助 code review 中开发者信任与采纳的影响；完整解释提升信任但 moderate 解释获最高 AI 一致率（89.22%）。

**Abstract:** Background: The use of large language models (LLMs) for automated code review has brought significant change to a time-consuming part of software engineering. Prior work has shown that LLM-based code tools can improve code quality and enable more robust software development processes. As the tools get more powerful, the explanations behind their decisions remain hard to understand. Developers struggle to assess the validity of LLM-generated code reviews, making it difficult to gauge how much trust they should place in them. While the application of automated code review with LLMs has been extensively researched, the inclusion of Explainable AI (XAI) for transparency in code reviews and its impact on trust are yet to be explored. Objective: We aim to address this research gap by collecting empirical evidence on the influence of XAI on the trust of software developers in AI-assisted code reviews. Method: We conducted a within-subjects user study with 34 participants from diverse programming backgrounds, comparing three experimental LLM-based automated code review systems with varying levels of XAI support: Condition A (detailed explanation and review feedback), Condition B (review feedback only), and Condition C (no explanations). Participants were shown a series of real-world code change requests along with the AI-generated code reviews. During the study, we measured trust perceptions for each system using a questionnaire, agreement with the AI recommendation, the reasoning for accepting or rejecting the code change, and the time taken to review the code change. Results: Our quantitative results show that the level of explanation significantly influences both the level of trust of software developers and their agreement with AI recommendations, but in different ways. Full explanations (Condition A) yield the highest perceived trust (M = 3.99/5) but not the highest agreement with AI recommendations, whereas moderate explanations (Condition B) achieve the highest AI agreement (89.22%). This could suggest that more explanations prompt developers to question AI recommendations more frequently. In contrast, providing no explanations (Condition C) results in the lowest levels of trust and agreement. We also find that the level of explanation did not significantly impact the time taken to accept or reject a code change. Across all conditions, the most commonly cited reasons for code change decisions were changes in code readability and the correctness of the implementation. Conclusion: Overall, these findings indicate that incorporating XAI into the code review process significantly changes the trust perceptions and agreement with AI recommendations for software developers. These results provide insights for the design and evaluation of trustworthy AI-based code review systems, and support researchers in the design of studies on the human factors of AI-assisted software development.


## 9. How Does Killing Surviving Mutants Help Detect Real Bugs with Assertion Generation? A Controlled Experiment

**Authors:** Hang Du (University of California at Irvine), Vijay Krishna Palepu, James Jones (University of California at Irvine)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832232

**中文总结:** 首次大规模 controlled experiment 直接度量 killing surviving mutants 对真实 bug 检测的因果影响；642 个 Defects4J bug 中 63 个可通过 principled mutant killing 检出。

**Abstract:** Killing surviving mutants is a central activity of mutation testing. This activity is motivated by the coupling-effect hypothesis: tests that expose simple artificial faults can also detect more complex, previously unseen real bugs. Despite these claimed benefits, automated studies have not directly measured the causal impact of mutant killing on real-bug detection. This limitation stems from open-ended mutant-killing strategies and a fundamental evaluation asymmetry that obscures causal attribution. In this work, we present the first large-scale controlled experiment that directly measures whether killing surviving mutants, without knowledge of future real bugs, would have enabled their detection. We model mutant killing as a selective, incremental process under realistic budget constraints, and we restrict test improvements to assertion augmentation. This restriction enables precise attribution of each test augmentation to a specific mutant-killing action. To support the experiment, we design a fully automated, fault-based assertion-augmentation technique that operates uniformly on mutants and real bugs and integrate it into Defects4J. Our controlled experiment yields several key empirical insights: (1) Across 642 Defects4J bugs, we find that 104 bugs would become detectable by adding an additional assertion to an existing passing, non-triggering test. (2) When coupling exists, a real bug is, on average, coupled with 21 surviving mutants, through which mutant killing can produce triggering tests. This number is substantially higher than the average of two mutants reported in prior studies. In those studies, coupling is inferred solely from documented bug-fixing tests rather than from tests derived via mutant killing. (3) Among these bugs, 63 of the 104 are detectable through principled mutant-killing (test augmentation) process. Notably, killing a randomly selected 30% of relevant surviving mutants, using only one assertion per mutant, suffices to detect 84.5% of these bugs. (4) By substituting mutants with real bugs and comparing their resulting assertion augmentation outputs, we find that real bugs induce broader behavioral effects than mutants, affecting more memory state locations, variables, and tests. (5) When mutation-derived assertions detect real bugs, they validate program outputs that overlap with, and are often strict subsets of, those affected by the real bugs. This offers a mechanistic explanation for why killing simple mutants can enable the detection of more complex real bugs.


## 10. Industrial Practice of LLM-based Test Case Carving and Assertion Generation (Experience Paper)

**Authors:** Haozhen You (Fudan University), Zhen Dong (Fudan University), Jingjing Wang (ByteDance), Qiang Li (ByteDance), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832099

**中文总结:** 提出工业实践 NL2Test，从自然语言场景与 traffic capture 生成可回放 API 回归测试与 assertion；51 个场景 exact-match 82.4%，9 个月生产部署生成 3196 用例且采纳率 85.4%。

**Abstract:** Enterprise regression testing for microservice systems is often constrained by incomplete or outdated documentation. In practice, QA engineers frequently rely on real execution traffic to reconstruct business scenarios; however, turning raw traffic into replayable regression tests with stable validation logic remains labor-intensive and error-prone.

This paper presents NL2Test, an end-to-end approach and tool that generates executable API regression tests from (i) a natural-language scenario description and (ii) a traffic capture recorded while executing the scenario. NL2Test addresses two coupled tasks: test case carving, which extracts a minimal replayable request sequence and reconstructs data dependencies so that dynamic values are bound from their responses rather than hard-coded; and assertion generation, which produces assertions aligned with business intent while avoiding non-deterministic fields and hallucinated paths. To improve reliability, NL2Test uses LLMs for semantic interpretation and constrained code synthesis, and uses deterministic algorithms for request filtering, dependency confirmation via value consistency, and assertion-path validation.

We evaluate NL2Test on 51 industrial regression scenarios extracted from a large consumer-facing Internet company. NL2Test achieves an exact-match rate of 82.4% (42/51), and produces a functionally usable draft in 98.0% (50/51) of scenarios when allowing minor post-edits. In a 9-month production deployment starting in March 2025, NL2Test generated 3,196 test cases with an overall code adoption rate of 85.4%. These results indicate that traffic-grounded generation with deterministic guardrails can substantially reduce manual effort while improving regression automation in complex microservice environments.


## 11. Lingxi: Repository-Level Issue Resolution Framework Enhanced by Procedural Knowledge Guided Scaling

**Authors:** Xu Yang (University of Manitoba), Jiayuan Zhou (Huawei), Michael Pacheco (Centre for Software Excellence, Huawei), Wenhan Zhu (Huawei Canada), Pengfei He (University of Manitoba), Shaowei Wang (University of Manitoba), Kui Liu (Huawei), Ruiqi Pan (Huawei Technologies Co., Ltd.)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832270

**中文总结:** Lingxi 从历史 issue 修复数据抽取程序性知识，离线分层抽象、在线知识驱动扩展，指导仓库级 issue 修复。在 SWE-bench Verified Past@1 上解决 74.6% bug，显著优于五种 SOTA 方法。

**Abstract:** Driven by the advancements of Large Language Models (LLMs), LLM-powered agents are making significant improvements in software engineering tasks, yet struggle with complex, repository-level issue resolution. Existing agent-based methods have two key limitations. First, they lack of procedural knowledge (i.e., how an issue is fixed step-by-step and rationales behind it) to learn and leverage for issue resolution. Second, they rely on massive computational power to blindly explore the solution space. To address those limitations, we propose Lingxi, an issue resolution framework that leverages procedural knowledge extracted from historical issue-fixing data to guide agents in solving repository-level issues. Lingxi first constructs this knowledge offline through a hierarchical abstraction mechanism, enabling agents to learn the how and why behind a fix, not just the final solution. During online application, it employs a knowledge-driven scaling method that leverages the procedural knowledge of similar issues to intelligently analyze the target issue from multiple perspectives, in sharp contrast to undirected, brute-force exploration. Lingxi successfully resolves 74.6% of bugs on the SWE-bench Verified benchmark in Past@1 setting, outperforming five state-of-the-art techniques by a significant margin (5.4% to 14.9%). Our comprehensive ablation study confirmed that the success of Lingxi comes directly from its use of procedural knowledge. Without it, the performance gains from scaling alone is negligible. Our qualitative study further shows that the ‘‘design patterns & coding practices’’ is the most critical knowledge aspect, and that the roles of different knowledge aspects switch across different stages (i.e., analysis, planning, and fixing).


## 12. Poirot: Automatic Root Cause Analysis of Safety Violations in ADS Simulation Testing via Hypothetical Reasoning

**Authors:** You Lu (Fudan University), Dingji Wang (Fudan University), Kun Zhang (Fudan University), Bihuan Chen (Fudan University), Jiyan Zhang (Fudan University), Xin Peng (Fudan University)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832179

**中文总结:** Poirot 对 ADS 仿真测试中的安全违规做两阶段根因分析：模块级用理想模块替换的假设推理定位故障模块，组件级用嫌疑引导搜索或因果分析精确定位。在 Apollo/Autoware 上模块级精度较 SOTA 提升 187.29%，组件级达 90.62%。

**Abstract:** With the rapid development of autonomous driving systems (ADSs), it has become critical to ensure their operational safety, leading to the widespread adoption of simulation testing. While existing scenario-based simulation testing approaches have demonstrated effectiveness in detecting safety violations, they often fall short in providing insight into the underlying causes of these violations, which is an essential capability for improving the safety and reliability of ADSs. To address this limitation, we propose a two-phase novel framework, Poirot, for root cause analysis in simulation testing via hypothetical reasoning. Given a reproducible violation scenario, in the module-level analysis phase, Poirot replays the violation scenario and identifies the faulty module by iteratively replacing an actual module with an idealized module and checking whether the violation persists. In the component-level analysis phase, depending on the identified faulty module, Poirot further applies either hypothetical reasoning with a suspicion-guided search strategy or causal analysis to narrow the fault space and pinpoint the faulty component. We evaluate Poirot with two ADSs, e.g., Apollo and Autoware, on a comprehensive benchmark that includes a total of 80 real and injected faults along with their triggering scenarios. Compared with the state-of-the-art root cause analysis approaches, e.g., ACAV and Rocas, Poirot improves the module-level accuracy by 187.29% on average, and identifies the faulty components at a finer granularity, achieving component-level accuracy of 90.62%. Our ablation study shows that our suspicion-guided search strategy in Poirot efficiently reduces the exploration of the fault space by 58.77%, leading to a 65.41% reduction in the time for fault localization. Finally, applied to two scenario-based simulation testing methods, i.e., AvFuzzer and MoDitector, Poirot attributes 425 violation scenarios to 8 faults, cutting debugging time by 96.89% compared to manual analysis in practice.


## 13. Profiling-Guided Bayesian Optimization of JVM Configurations

**Authors:** Abdelrahman Baz (The University of Texas at Austin), Wing Lam (George Mason University), August Shi (The University of Texas at Austin)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832253

**中文总结:** PROBO 采集 44 项 JVM 运行时指标，经 metrics 模型与 performance 模型两阶段贝叶斯优化搜索降低回归测试时间。在 16 个 Java 项目上平均测试时间降 10.7%，较随机搜索与 BOCA 分别快 1.85× 与 2.49×。

**Abstract:** Regression testing is essential for maintaining software quality but often incurs substantial time costs. Prior work has demonstrated that tuning Java Virtual Machine (JVM) configuration flags can reduce test execution time, yet finding effective flag combinations remains challenging due to the vast configuration space and complex interactions between flags. Random search and direct modeling approaches that map flags to testing time have shown limited effectiveness in navigating this complex optimization landscape. We present PROBO (PROfiling-Guided Bayesian Optimization), an iterative approach that leverages JVM runtime metrics (such as garbage collection frequency, just-in-time (JIT) compilation rates, and memory allocation) to guide Bayesian optimization for testing time reduction. Unlike prior work that directly models the relationship from flags to testing time, PROBO decomposes the prediction problem through observable runtime behaviors: a metrics model predicts how flag configurations affect runtime metrics, and a performance model predicts how those metrics affect testing time. PROBO collects 44 runtime metrics using a profiler during test execution, and propagates feature importance scores through both models to identify which flags most strongly influence testing time-predictive metrics. Finally, PROBO generates candidate flag configurations through three complementary strategies guided by expected testing time improvement. We evaluate PROBO on 16 open-source Java projects, comparing against random search and BOCA (a Bayesian optimization baseline). PROBO achieves an average testing time reduction of 10.7% across all projects, outperforming random search (5.8%) by 1.85× and BOCA (4.3%) by 2.49×. PROBO successfully generates configurations that substantially reduce testing time for all 16 projects, with reductions ranging up to 27.4%. With a one-hour time budget for search, PROBO maintains its advantage with 8.0% average reduction, demonstrating practical applicability. Moreover, PROBO-generated configurations remain effective across software evolution, maintaining 8.8% average reduction over 88 future commits per project. Our analysis reveals that JIT compilation metrics, particularly Total Compilation Rate (methods compiled per second) and C1 Compilation Rate (first-tier JIT compilation rate), are the strongest predictors of testing time, accounting for 67.2% of consistently important metrics across projects.


## 14. Re-evaluating Detection of Equivalent Mutants Using LLMs: We Should Properly Measure How Far We Are

**Authors:** Arjun Tandon (Indraprastha Institute of Information Technology Delhi), Mehmet Fırat Dündar, Milkiyas Gebremichael Gebru, Darko Marinov (University of Illinois at Urbana-Champaign), Yiling Lou (University of Illinois at Urbana-Champaign), Wenxi Wang (University of Virgina)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832250

**中文总结:** 重新评估 LLM 等价 mutant 检测（EMD）的泛化能力，发现原数据集存在 method 级数据泄露且 LLM 依赖多数投票捷径。跨算子、语言与新项目数据集上性能显著下降，呼吁采用更真实的跨方法评估设置。

**Abstract:** Mutation testing is a widely used approach for measuring quality of test suites. Equivalent mutant detection (EMD), i.e., determining if a mutant semantically behaves the same as the original code despite some syntactic differences, is a critical problem in mutation testing. A recent study has shown the great promise of LLM-based EMD techniques, reporting substantial improvements over traditional compiler- and machine-learning–based approaches. In this work, we revisit prior results and evaluate the generalization capabilities of LLM-based EMD techniques across two new datasets that differ from the original dataset in mutation operators, programming languages, and source projects. Contrary to prior findings, all studied LLM-based EMD techniques suffer substantial performance degradation on the new datasets. Through extensive analysis, we identify original-method–level data leakage in the original dataset as a key factor inflating earlier results and show that LLMs often rely on a method-wise majority-voting shortcut rather than reasoning about the semantic effects of individual mutations. Based on these findings, we call for the adoption of realistic cross-method evaluation settings and the development of mutation-centric semantic reasoning in future LLM-based EMD research.


## 15. RPCSpecter: Detecting Blockchain RPC Bugs through a Specification-Driven, Constraint-Aware Fuzzing Approach

**Authors:** Yuming Xiao (Sun Yat-sen University), Yuhong Nan (Sun Yat-sen University), Zhijie Zhong (Sun Yat-sen University), Mingxi Ye (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832105

**中文总结:** 提出 RPCSpecter，从 RPC 规范抽取约束、约束引导变异与双向断言三阶段 fuzz 区块链 RPC 实现。在 Ethereum/Solana 共 6 个客户端上发现 26 个未知 bug，其中 1 个获 $3000 漏洞赏金。

**Abstract:** Blockchain Remote Procedure Calls (RPCs) serve as the primary interface for interaction between decentralized applications and blockchain networks. Despite their critical role, existing RPC implementations are prone to bugs that are often challenging to detect using traditional testing methods. In this paper, we introduce RPCSpecter, an automated framework for constraint-aware fuzz testing of blockchain RPC Implementations. The core of RPCSpecter is a three-stage process: (1) Constraint Extraction, where implicit semantic dependencies from the documented RPC specifications are parsed and converted into executable constraints, (2) Constraint-Guided Mutation, which generates diverse and semantically valid test inputs based on these constraints, and (3) Bidirectional Assertion, which validates both valid and invalid RPC responses through dynamic checks and self-learning mechanisms. We evaluate RPCSpecter   on both Ethereum and Solana, two predominant platforms in the Blockchain ecosystem, with a total of 6 clients, such as Geth, Besu and Agave. The results show that RPCSpecter uncovers a total of 26 previously unknown bugs, including critical errors that are undetectable by existing fuzzers or manual testing, as well as multiple silent semantic inconsistencies. Particularly, 4 of them have been acknowledged, and one of the bugs affecting three major Ethereum clients is confirmed as a vulnerability, with a $3,000 bounty-award. Additionally, we demonstrate how RPCSpecter’s constraint-driven approach significantly improves the efficiency and effectiveness of fuzz testing by systematically guiding mutation to explore boundary conditions and rare edge cases. Our research provides a more robust, scalable, and automated solution for enhancing the reliability and security of blockchain RPC implementations.


## 16. SemantiX: A Compatibility Checker between Applications and Compositions of Distributed Systems

**Authors:** Yifei Sun (Inria, ENS de Lyon, Univ. Grenoble Alpes), Ji-Yong Shin (Northeastern University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832138

**中文总结:** 提出 SemantiX，以 AppGraph 建模应用并与形式化分布式一致性语义模块做兼容性检查或搜索可行组合。三个案例研究显示可快速验证流媒体、电商与跨服务因果存储的设计语义匹配。

**Abstract:** Modern distributed applications compose multiple services with different consistency guarantees. Mismatches between application requirements and chosen system semantics can introduce subtle bugs, but verifying compatibility across complex applications is both challenging and time-consuming. In particular, existing approaches on testing or rigorous formal verification lack flexibility and cannot promptly provide correctness guarantees on multi-semantic compositions.

We present SemantiX, a framework for checking semantic compatibility between applications and compositions of distributed systems with heterogeneous consistency models. SemantiX embeds formally defined distributed system modules of consistency semantics which include the first formal definition of visibility constraints. SemantiX introduces the AppGraph approach for systematically modeling complex applications. Applications modeled using AppGraphs can be checked for their compatibility against a combination of distributed system modules. Alternatively, SemantiX can search for combinations of modules compatible to the application. We present three case studies on a movie streaming service, an e-commerce platform, and a cross-service causal distributed storage service. We demonstrate that SemantiX can capture complex service compositions with minimal encoding effort and quickly check compositional compatibility with underlying systems or find the compatible system sets. SemantiX enables developers to efficiently verify distributed application designs and explore alternative consistency configurations, supporting more agile development.


## 17. The Illusion of Success: Learning-Based Android Malware Detectors (Replicability Study)

**Authors:** Michael Tegegn (University of British Columbia), Julia Rubin (The University of British Columbia)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Published Artifact, Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832233

**中文总结:** 对 Android 机器学习恶意软件检测工具进行系统文献综述与纵向评估，发现即便控制已知偏置，召回率仍在 56%–94% 间大幅波动。故意使用不可靠包名特征的缺陷分类器表现接近甚至优于部分工具，揭示评估方法的根本缺陷。

**Abstract:** Machine learning (ML) approaches have shown impressive performance in Android malware detection and have become the scalable alternatives to signature and heuristic-based methods. ML-based detectors typically collect large amounts of benign and malware applications from popular data sources, split the collected dataset into training and testing subsets, train a binary classifier, and report test set performance. While these tools report 95%+ recall, several recent works have shed light on flaws in experiment setup or evaluation methods questioning the trustworthiness of their results. In an effort to further understand the true performance of the tools, we conduct a systematic literature review of tools and design large-scale longitudinal evaluation using widely used datasets and detection approaches. Even after carefully accounting for the known biases in experiment setup and evaluation, we observe that tools achieve significantly diverging classification performance (ranging from 56% to 94% recall) even on different subsets of the same dataset. Surprisingly, we also find that a deliberately flawed classifier that uses unreliable class package names as features performs nearly as good, sometimes better, than the set of tools we evaluated on these datasets, showing the untrustworthiness of tool-reported results. Our results further establish that there is still much room for improvement in ML-based AMD towards creating semantic-aware detectors and more reliable evaluation methodologies.


## 18. Towards Understanding the Bugs in Verilator, a Hardware Description Language Compiler

**Authors:** Songyan Jiang (State Key Laboratory for Novel Software Technology, Nanjing University), Maolin Sun (Nanjing University), Kang Chen (State Key Laboratory for Novel Software Technology, Nanjing University), Qingyang Li (Nanjing University), Yibiao Yang (Nanjing University), Yuming Zhou (Nanjing University)

**Categories:** Mining Software Repositories

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832226

**中文总结:** 对 Verilator HDL 编译器 488 个已确认 bug 进行首个系统实证研究，分析症状、根因与触发用例特征并评估现有测试技术有效性。为 HDL 编译器可靠性改进与针对性自动化测试方法设计提供可操作建议。

**Abstract:** Verilator is the premier open-source Hardware Description Language (HDL) compiler. It transforms Verilog and SystemVerilog designs into optimized C++ or SystemC models, enabling high-speed, cycle-accurate simulation prior to large-scale production. As a cornerstone of the hardware verification ecosystem, the correctness of Verilator is paramount; compiler faults can lead to silent simulation errors or unexpected failures, undermining the integrity of the hardware development lifecycle. Unlike traditional software compilers, HDL compilers manage unique concurrency and synthesis semantics, potentially introducing distinct bug patterns and complexities. However, while prior research has explored testing techniques for HDL toolchains, there remains a lack of systematic empirical studies characterizing the specific nature of bugs in Verilator. This knowledge gap hinders the development of targeted improvements in compiler robustness and testing strategies. To address this, we present the first comprehensive empirical study of Verilator bugs. We manually collected, analyzed, and categorized a dataset of 488 confirmed bugs from the official repository over three years. Our study investigates bug symptoms, root causes, and the characteristics of triggering test cases, while also evaluating the effectiveness of existing testing techniques. Based on our findings, we provide actionable guidance for developers to enhance Verilator’s reliability and for researchers to design more effective automated testing methodologies for HDL compilers.


## 19. Uncovering Business Logic Bugs via Semantics-Driven Unit Test Generation (Experience Paper)

**Authors:** Chen Yang (Tianjin University), Junjie Chen (Tianjin University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832192

**中文总结:** SeGa 从产品需求文档构建语义知识库，检索功能条目并推导细粒度业务场景引导 LLM 生成单元测试以暴露业务逻辑 bug。在 4 个工业 Go 项目 60 个真实 bug 上比 4 种 LLM 方法多检出 22–25 个，生产部署另发现 16 个已确认 bug。

**Abstract:** Business logic bugs violate intended business semantics and are particularly prevalent in enterprise software. Yet most existing unit test generation techniques are code-centric, making such bugs difficult to expose. We present SeGa, a semantics-driven unit test generation technique for uncovering business logic bugs. SeGa constructs a semantic knowledge base from product requirement documents, represented as a set of functionality entries that group related requirements under a common business intent. Given a focal method, SeGa retrieves the relevant functionality entries and derives fine-grained business scenarios with explicit preconditions, triggering actions, expected outcomes, and semantic constraints to guide LLM-based test generation. We evaluate SeGa on four industrial Go projects containing 60 real-world business logic bugs. SeGa detects 22~25 more bugs than four state-of-the-art LLM-based techniques and improves precision by 26.9%~34.3%. Deployment across 6 production repositories further uncovers 16 previously unknown business logic bugs that were confirmed and fixed by developers, demonstrating SeGa’s practical value. From our industrial study, we summarize a series of lessons and suggestions for practical use and future research.
