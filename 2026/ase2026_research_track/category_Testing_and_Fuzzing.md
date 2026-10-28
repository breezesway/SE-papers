# ASE 2026 Research Track — Testing and Fuzzing

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 40

## 1. Accurate and Low-Cost Residual Risk Assessment via Sampled Profiling and Structure-Aware Coverage Amplification

**Authors:** Seongmin Lee (University of California at Los Angeles, USA), Işıl Özgü (University of California at Los Angeles, USA), Marcel Böhme (MPI-SP - CISPA Helmholtz Center for Information Security, Germany, Germany), Miryung Kim (University of California at Los Angeles, USA)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837519

**中文总结:** 在黑盒 fuzz 中用硬件 IP 采样替代全量 coverage 插桩，并以 must-execute 静态分析从稀疏采样补全必经路径以估计残余风险；相对完整插桩吞吐约 4.27×，更快达到停止阈值且相对误差约 1.73，同预算下可更早触发更多 bug（最高约 10×）。

**Abstract:** Estimating the residual risk of undiscovered bugs—and thus when to stop fuzzing—is critical for determining testing adequacy. Traditionally, this assessment relies on coverage instrumentation, which records complete coverage of every execution but imposes a 60-70% performance slowdown, reducing fuzzing throughput and delaying bug discovery. This overhead raises a fundamental question: can partial observation provide high-fidelity confidence at a fraction of the coverage instrumentation cost? We propose a risk assessment method in the context of black-box fuzzing that leverages hardware-enabled performance profiling —replacing coverage instrumentation with instruction pointer (IP) sampling—as the core mechanism for low-overhead observation. To recover the accuracy inevitably lost to the sparse nature of sampling, we employ must-execute analysis , a static control-flow analysis that identifies all statements and basic blocks that must have executed to reach, or must execute after, an observed sample, effectively reconstructing missing execution paths from partial observations. Despite the partial coverage inherent to profiler-based sampling, our risk estimation method achieves 4.27× higher throughput than complete-coverage instrumentation, enabling fuzzing campaigns to reach stopping thresholds 2× faster while maintaining high accuracy (1.73 average relative error compared to the ground truth). Ultimately, this efficiency translates into superior bug discovery, triggering more bugs with speedups of up to 10× within the same time budget.


## 2. Breaking the Isolation: Coordinated Multi-agent Fuzzing for Smart Contracts with Multi-dimensional Objective Learning

**Authors:** Ruichao Liang (Wuhan University, China), Ruochen Cao (Wuhan University, China), Jing Chen (Wuhan University, China), Kun He (Wuhan University, China), Yebo Feng (Nanyang Technological University, Singapore), Yue Xue (MetaTrust Labs, Singapore), Cong Wu (Wuhan University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837466

**中文总结:** SynerFuzz 将智能合约 fuzz 建模为 Dec-POMDP，多 DRL agent 分别优化语义/状态/经济等目标并协同生成交易序列；较 9 个 SOTA 最多多检 4.2× 漏洞，复现 33 起历史 DeFi 攻击并发现 17 个 0-day（管理资产约 1.798 亿美元）。

**Abstract:** Smart contracts manage critical assets in decentralized systems but are prone to vulnerabilities. While fuzzing has proven effective in software testing, existing contract fuzzers often rely on ad-hoc optimization strategies with limited objective guidance, typically driven by coverage or simple heuristics. This narrow focus leads to high false negative rates, as important perspectives of smart contracts, like semantic, state, and economic effects, are overlooked during transaction sequence generation. Moreover, coordinating these dimensions into fuzzing is challenging because their divergent objectives and complex interactions make ad-hoc adaptations to fitness functions or mutation strategies largely ineffective. To fill the gaps, we propose SynerFuzz, a multi-agent deep reinforcement learning-based fuzzer. We formulate fuzzing as a Decentralized Partially Observable Markov Decision Process, where each agent is assigned a distinct testing objective extracted from the target contract. Through coordinated learning, DRL agents integrate multi-dimensional signals to construct high-quality sequences, enabling SynerFuzz to uncover both subtle semantic flaws and economically profitable behaviors. Compared to 9 SOTA tools, SynerFuzz detects up to 4.2× more vulnerabilities while reducing time and transaction overhead by 70.6% and 86.8%. In real-world scenarios, SynerFuzz reproduces 33 historical DeFi exploits with over $40 million losses and discovers 17 0-day vulnerabilities in 4 projects managing over $179.8 million, earning $3,800 bug bounties.


## 3. ConfFuzz: Parameter-Aware Greybox Fuzzing for Configurable Cloud Systems

**Authors:** Shuai Wang (University of Illinois at Urbana-Champaign, USA), Hao Wang (University of California at Berkeley, USA), Darko Marinov (University of Illinois at Urbana-Champaign, USA), Tianyin Xu (University of Illinois at Urbana-Champaign, USA), Yongle Zhang (Purdue University, USA)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837476

**中文总结:** 将灰盒 fuzz 用于云系统配置测试，以单元测试为驱动并做参数感知变异与能量分配；在 9 个云系统上分支覆盖约为基线 3.2 倍，共发现 125 个缺陷（14 已修复、12 已确认）。

**Abstract:** Cloud systems are highly configurable, with hundreds to thousands of configuration parameters. Configuration-related bugs are major sources of cloud failures, yet most tests only run under default configurations, leaving systems vulnerable to untested configurations.  
This paper applies coverage-based greybox fuzzing to configuration testing of cloud systems. We use developer-written unit tests as fuzz drivers: they avoid the cluster-initialization overhead of system tests and thus provide the high test execution speed that greybox fuzzing demands. Since cloud systems expose hundreds to thousands of configuration parameters but any unit test typically exercises only a small subset of them (15.14% on average), we design parameter-aware mutation and fuzzing energy allocation strategies: (1) we restrict mutation to only the configuration parameters exercised by each seed, and (2) we incorporate both code coverage and configuration parameter coverage into fuzzing energy allocation, giving more effort to seeds that explore more code and parameters.  
We implement these ideas in ConfFuzz and evaluate it on nine widely used cloud systems. Compared with a greybox fuzzing baseline without parameter-aware mutation and energy allocation,  
ConfFuzz covers roughly 3.2 times more branches while exploring substantially more configuration parameters. In total, ConfFuzz and its variants have detected 125 bugs, of which 14 have been fixed and 12 more have been confirmed.


## 4. CTForge: Automatically Generating Test Suites for Software Configuration

**Authors:** Yuanliang Zhang (National University of Defense Technology, China), Zhizheng Zheng (National University of Defense Technology, China), Shanshan Li (National University of Defense Technology, China), Zhouyang Jia (National University of Defense Technology, China), Chaopeng Luo (National University of Defense Technology, China), Liqian Chen (National University of Defense Technology, China), Zhenbang Chen (National University of Defense Technology, China), Ji Wang (National University of Defense Technology, China), Xiangke Liao (National University of Defense Technology, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837484

**中文总结:** 提出 LLM 框架 CTForge，经三阶段配置感知优化（覆盖、断言校验、配置敏感性）自动生成配置专项测试；在 5 个大型系统上检出 79 个真实配置问题中的 63 个，F1 0.88，并发现 6 个未知缺陷。

**Abstract:** Software configuration plays a critical role in modern software systems, yet it also frequently leads to severe failures. Existing approaches, whether static analysis or LLM-based validation, struggle to capture implicit semantic constraints and validate configuration-code interactions. Leveraging existing unit tests is also insufficient due to their lack of configuration-specific focus. Thus, we present CTForge, an LLM-powered framework that automatically generates configuration-specific test suites. Its core innovation is a three-stage configuration-aware optimization pipeline that moves beyond vanilla test generation, specifically using parameter semantics to improve LLM outputs. This optimization pipeline iteratively aligns tests through: (1)enhance configuration-related code coverage to ensure relevance, (2) assertion validation across valid parameter values to eliminate false assertions, and (3) configuration-sensitivity verification to select tests that semantically exercise the intended configuration behavior. Evaluated on five large-scale systems, CTForge detects 63 out of 79 real-world configuration issues and achieves an F1-score of 0.88 in misconfiguration detection. CTForge also uncovers six previously unknown defects. Our work demonstrates that structured configuration-aware refinement is essential for LLM to produce effective test suites.


## 5. CtxFuzz: Context-Aware Directed Fuzzing via Runtime Fuzzer-Agent Cooperation

**Authors:** Jiho Kim (Georgia Institute of Technology, USA), Dongkwan Kim (Georgia Institute of Technology, USA), HyungSeok Han (Microsoft, USA), Youngjoon Kim (Georgia Institute of Technology, USA), Soyeon Park (Independent Researcher, USA), Sangwoo Ji (Samsung Electronics, Republic of Korea), Joshua Wang (Georgia Institute of Technology, USA), Dae R. Jeong (Seoul National University, Republic of Korea), Taesoo Kim (Georgia Institute of Technology, USA)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834365

**中文总结:** 提出 CtxFuzz，让 LLM agent 与定向 fuzzer 迭代交换执行与语义上下文并生成可执行变异脚本；在 AIxCC 62 个漏洞上触发 61 个（29 个为现有定向 fuzz 未达），并经真实报告管线暴露 2 个零日。

**Abstract:** Automated tools produce vulnerability reports at unprecedented scale, but turning a report into a confirmed proof-of-vulnerability remains challenging. Directed grey-box fuzzers are widely used for validation but lack the ability to consume the rich context these reports carry, reducing each target to a bare location. In contrast, LLM-based approaches can consume this context but are often unable to identify the true triggering mechanism or to synthesize a working proof-of-vulnerability. We present CtxFuzz, a context-aware directed fuzzer that enables an LLM agent and a coverage-guided fuzzer to iteratively exchange and refine bug-triggering context throughout the campaign. The fuzzer contributes execution context, such as what inputs were tried and how the program behaved, grounding the agent’s reasoning in concrete evidence. The agent contributes semantic context, including hypotheses about the triggering conditions, explanations of failed attempts, and targeted mutations to overcome them, guiding the fuzzer toward relevant regions of the input space. Failed attempts are not discarded but decomposed into mutation scripts that translate each identified blocker into a fuzzer-executable strategy. This iterative exchange enables CtxFuzz to trigger vulnerabilities that neither directed fuzzers nor LLM agents reach independently. On 62 vulnerabilities across 16 open-source projects from the AIxCC Final competition (39 C, 23 Java), CtxFuzz exposes 61 of 62 targets, including 29 that no state-of-the-art directed fuzzer reaches, and exposes two zero-day vulnerabilities through a real-world vulnerability report validation pipeline.


## 6. Don’t Retest Everything: Auditable Regression Scoping for Safety-Critical Systems

**Authors:** Francesco Basciani (Gran Sasso Science Institute, Italy), Daniele Masti (Gran Sasso Science Institute, Italy), Patrizio Pelliccione (Gran Sasso Science Institute, Italy), Alberto Petrucci (Gran Sasso Science Institute, Italy), Franco Raimondi (Gran Sasso Science Institute, Italy), Emerson Sales (Gran Sasso Tech, Italy), Paolo Serri (Thales Alenia Space Italia, Italy)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837416

**中文总结:** 与 Thales Alenia Space 合作提出 CoCoS，用语义差分、AST 与调用图传播跨仓库推导可审计、可解释的保守回归测试范围，满足航电等认证与可追溯要求。

**Abstract:** In safety-critical software development, changes often span technical and organisational boundaries, e.g., repositories, interfaces, libraries, and teams. Under certification and traceability requirements, these changes create a difficult regression-testing problem: organisations must determine what must be revalidated and provide an auditable justification for those decisions. In practice, the resulting uncertainty often drives overly conservative strategies, where large portions of the system are retested after changes or updates, even when a narrower scope would suffice. In this paper, we present CoCoS, an automated regression-testing approach for safety-critical systems written in C and developed under traceability and certification constraints. Developed end-to-end with Thales Alenia Space Italia, a large international aerospace company, and grounded in avionics practice, CoCoS addresses real certification-driven needs rather than an abstract setting. It combines semantic differencing, abstract syntax tree analysis, and function-level call-graph propagation to identify semantically relevant changes across repository and component boundaries, and to derive conservative regression scopes with human-readable justifications. CoCoS prioritizes conservativeness, explainability, and auditability, thereby supporting defensible regression-scoping decisions in regulated workflows. We evaluate CoCoS in an industrial setting with Thales Alenia Space Italia, using a realistic multi-repository aerospace software environment involving application code and external libraries. The results show that CoCoS supports the conservative bounding of regression scopes while preserving compliance-oriented reasoning and providing practical evidence for test planning in safety-critical environments.


## 7. DynCA: An Effective Algorithm for 3-Wise Combinatorial Interaction Testing in Highly Configurable Systems

**Authors:** Ruizhi Shi (Beihang University, China), Shuangyu Lyu (Beihang University, China), Renyu Yang (Beihang University, China), Wei Wu (Central South University, China), Chanjuan Liu (Dalian University of Technology, China), Chunming Hu (Beihang University, China), Chuan Luo (Beihang University, China)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834349

**中文总结:** 提出 DynCA 用于大规模 3-wise 约束覆盖阵列生成，在真实可配置系统上较 SOTA 测试集规模再减 10.8%，且用时约为一半即可得到更小阵列。

**Abstract:** With the increasing demand for software customization, highly configurable systems have become increasingly important. Combinatorial interaction testing (CIT) is widely recognized as an effective technique for testing such systems. The most critical problem in CIT is constrained covering array generation (CCAG), which aims to construct a t -wise covering array (CA) with as small a size as possible, where t denotes the testing strength. Compared with the widely adopted pairwise testing ( 2-wise CIT), 3-wise CIT is capable of detecting more faults and provides greater practical benefits. However, it also introduces significantly higher computational complexity. Although many existing algorithms perform well on 2-wise CCAG, current state-of-the-art CCAG algorithms still suffer from the severe scalability challenge in 3-wise CCAG and have difficulty generating small-sized CAs for large-scale instances. Since the size of a CA directly affects testing efficiency in practice, generating small-sized 3-wise CAs is of great importance. In this work, we propose , a novel 3-wise CCAG algorithm that effectively generates small-sized CAs for large-scale instances. Experimental results on extensive real-world highly configurable systems demonstrate that, compared with existing state-of-the-art algorithms, reduces the size of generated 3-wise CAs by 10.8%. Moreover, is efficient, requiring only half of the running time to generate smaller 3-wise CAs than existing algorithms.


## 8. Escaping the Self-Repair Trap: Improving Test Oracle Generation via Dual-Context Awareness

**Authors:** Kefan Li (Beihang University, China), Hongyue Yu (Beihang University, China), Yuan Yuan (Beihang University, China)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834421

**中文总结:** 指出迭代自修复 oracle 易陷入「Self-Repair Trap」，提出非迭代的 DCAware，融合静态结构与选择性动态状态；在变异/执行实验中 fault-revealing 更强且算力远低于 repair 类方法。

**Abstract:** Large Language Models (LLMs) have shown strong potential for regression-oracle completion, where a test prefix is given and the current program version is treated as expected behavior. Recent approaches increasingly rely on iterative self-repair and execution feedback, but optimizing execution success does not necessarily yield strong fault-revealing oracles. This objective, widely adopted in repair-based methods, serves only as a proxy and may be misaligned with the true goal of oracle generation. Such misalignment biases the repair process, giving rise to a feedback-driven degeneration that we term the Self-Repair Trap, where iterative repair progressively drives models toward assertions that are easier to satisfy but less effective at detecting faults. To address this issue, we propose DCAware, a computationally efficient, non-iterative framework that prioritizes high signal-to-noise contextual grounding over multi-round repair. DCAware integrates structured static context with selectively retrieved dynamic states, enabling precise and robust oracle generation without iterative feedback loops. Extensive experiments based on execution and mutation testing show that DCAware consistently improves fault-revealing effectiveness while maintaining high execution success, outperforming prior methods with substantially lower computational cost. Our results suggest that improving contextual quality is more effective than adding iterative repair complexity in the studied regression-oracle setting.


## 9. Every Scenario Matters: Scenario-Guided White-Box Testing for Static Code Checkers Powered by LLMs

**Authors:** Jun Liu (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Liqiang Ji (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Jiwei Yan (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China / Beijing Key Laboratory of Intelligent Software Engineering, China), Linjie Pan (Huawei Technologies, China), Jinsong Ren (Huawei Technologies, China), Jun Yan (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China / Beijing Key Laboratory of Intelligent Software Engineering, China), Jian Zhang (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834381

**中文总结:** 提出 ScenSCT，将 checker 源码转为 CheckerIR 抽取检查场景并生成对齐/增强测试；五款 Java 静态分析工具上平均每 checker ~9 场景/~39 测试，发现 270 处潜在问题（精度 86.4%）及 177 处跨工具能力差异。

**Abstract:** In static analysis tools, each detection rule corresponds to a dedicated code checker. The checker's quality directly determines the validity of reported defects. Thus, comprehensive testing of these checkers is crucial. Existing checker testing approaches usually generate test cases from high-level rule descriptions while treating checkers as black boxes. However, these descriptions usually omit implementation-level conditions and checking scenarios. To bridge this gap, our key insight is that the rule description and checker implementation provide complementary information for comprehensive testing. The implementation supplies concrete checking logic, while the rule anchors the intended semantics. Building on this, we propose ScenSCT, a novel scenario-guided white-box checker testing approach powered by LLMs. ScenSCT first translates the checker's source code into a unified logic-based representation (CheckerIR) and applies both logic-decomposition and scenario-validation strategies to extract concrete checking scenarios. It then converts these scenarios into test cases through execution-feedback-guided test alignment to instantiate scenario constraints and scenario-invariant test augmentation to generate variants that preserve the target scenario. We evaluate ScenSCT on real-world Java checkers from five mainstream static analysis tools. In single-tool evaluation, ScenSCT extracts an average of ~9 scenarios and generates ~39 tests per checker, uncovering 270 potential issues (58 false positives and 212 false negatives) with an overall precision of 86.4%. Furthermore, cross-tool evaluation reveals 177 capability differences among shared checkers. Overall, ScenSCT offers a systematic testing method to improve the reliability of static analysis tools.


## 10. ExcavatorFuzz: LLM-Guided Path-Difficulty-Driven Directed Greybox Fuzzing

**Authors:** Kaiyu Xie (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Siyuan Li (Shandong University, China), Jiaqian Peng (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Yun Yang (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Yaowen Zheng (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Kai Cheng (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Jiayu Zhang (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Shizhao Tian (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Yubo Li (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China), Hongsong Zhu (Institute of Information Engineering at Chinese Academy of Sciences, Beijing, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837497

**中文总结:** 提出 ExcavatorFuzz，CLI 可行路径过滤、路径难度排序，并在阻塞时用 LLM 合成/ refine seed；30 个 C/C++ 基准 24h 内触发 29/30 已知漏洞，平均曝光时间快 4.34×，并获 3 个新漏洞（2 个 CVE）。

**Abstract:** Directed greybox fuzzing (DGF) is effective at steering mutations toward vulnerable code regions, but its efficiency is often limited by two bottlenecks: misprioritized target-reaching paths and hard-to-satisfy blocking predicates. We present ExcavatorFuzz, an LLM-assisted DGF framework that addresses both challenges in a unified workflow. ExcavatorFuzz first performs CLI-aware feasibility filtering to prune configuration-infeasible paths, and then ranks the remaining candidate paths using a lightweight difficulty metric that approximates their relative tractability based on explicit predicate complexity and implicit data-dependency complexity. During fuzzing, ExcavatorFuzz monitors line-level progress to detect blocked paths and invokes the LLM to synthesize or refine seeds for unsatisfied predicates using structured feedback. We evaluate ExcavatorFuzz on 30 real-world C/C++ benchmarks. ExcavatorFuzz triggers 29 out of 30 known vulnerabilities within 24 hours and achieves an average 4.34x speedup in time-to-exposure over seven state-of-the-art fuzzers. It also discovered three previously unknown vulnerabilities in open-source projects, two of which have been assigned CVE IDs.


## 11. FAiLGen: Calibrating LLM for Failing Test Generation with Monte Carlo Tree Search

**Authors:** Tsz-On Li (Hong Kong University of Science and Technology, Hong Kong / Guangzhou HKUST Fok Ying Tung Research Institute, China), Xiaochuan Yan (Northeastern University, China), Dehui Yi (Northeastern University, China), Yuhang Jiang (Northeastern University, China), Kexin Li (Northeastern University, China), Congying Xu (Hong Kong University of Science and Technology, Hong Kong / Guangzhou HKUST Fok Ying Tung Research Institute, China), Ying Wang (Northeastern University, China), Shing-Chi Cheung (Hong Kong University of Science and Technology, Hong Kong / Guangzhou HKUST Fok Ying Tung Research Institute, China)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837478

**中文总结:** 提出 FAiLGen，用 LLM 作替代 oracle 并通过 MCTS 校准推理步骤，在差分测试框架下生成 failing test，缓解一致输出或预置测试不足带来的误判。

**Abstract:** Failing test generation is an important yet challenging task in software engineering. It involves searching a vast space to identify fault-triggering test inputs and the oracles that assert these faulty executions. Several approaches have been proposed for generating failing tests. Specifically, given a program-under-test (PUT) and its requirements, these approaches leverage large language models (LLMs) to generate alternative implementations of the PUT that comply with the requirements, followed by differential testing between the PUT and the alternative implementations. Failing tests can be constructed by adopting the inconsistency-revealing inputs as the test inputs and treating the outputs returned by the alternative implementations as expected outputs. As alternative implementations may also contain faults and thus return incorrect outputs, current methods rely on either output consistency across alternative implementations or pre-constructed test cases for validation. However, the former is susceptible to LLM training biases or stochasticity, while the latter can be impractical due to the scarcity or unavailability of pre-constructed test cases in real-world scenarios.  
To address existing works’ limitations, we employ LLM as an alternative oracle for output validation, and calibrate its reasoning steps to reduce its susceptibility to LLM training biases or stochasticity. One critical challenge is that the calibration process inherently requires correct input-output pairs for the output validation task as ground-truth for reference when validating/calibrating LLMs’ reasoning, yet correct input-outputs (i.e., passing tests) are often scarce or unavailable in real-world scenarios. To address this challenge, our insight is that outputs consistently returned by both the PUT and all alternative implementations have a high probability of being the correct outputs of the PUT, as the PUT and alternative implementations are generated by independent agents (i.e., human developers and LLMs). Based on this insight, we propose FAiLGen, a novel approach that calibrates LLM’s reasoning for failing tests generation via a representative reasoning calibration paradigm, Monte Carlo Tree Search. We evaluate FAiLGen on 100 subjects from CodeForces and 100 subjects from SWE-Bench-Live. Our evaluation results show that FAiLGen achieves a recall of 58.1%, which is 62.4% higher than that of the best baseline (35.8%). Meanwhile, FAiLGen attains a precision of 75.2%, favorably compared to the best baseline (61.1%).


## 12. Feature-Focused Test Generation

**Authors:** José Antonio Zamudio Amaya (CISPA Helmholtz Center for Information Security, Germany), Gaetano Sapia (CISPA Helmholtz Center for Information Security, Germany / MPI-SP, Germany), Alexi Turcotte (CISPA Helmholtz Center for Information Security, Germany), David Benavides (Universidad de Sevilla, Spain), Marcel Böhme (CISPA Helmholtz Center for Information Security, Germany / MPI-SP, Germany), Andreas Zeller (CISPA Helmholtz Center for Information Security, Germany)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837479

**中文总结:** 提出 FFTG，从输入规格抽取 feature model，按测试者选定 feature 特化规格以生成聚焦切片；原型 Compás 可保持有效性、覆盖 feature 相关代码并支持用少量 slice 保留全集覆盖的用例最小化。

**Abstract:** Specification-based test generators use input specifications to produce valid tests for complex systems, covering the entire input space of the system under test. This broad generation capability, however, can become a burden when one wants to focus test generation on a particular subset of the input space, say, a feature whose implementation has recently changed or is particularly critical. In this paper, we propose Feature-Focused Test Generation (FFTG), an approach that treats specification-based test generation as a configuration problem. From the input specification, FFTG first extracts a feature model that represents alternate and optional expansions as possible feature values. After the tester selects which features to focus upon, FFTG specializes the specification accordingly, generating inputs in which only the focused features vary. We implement FFTG in a prototype named Compás. In our evaluation, we find that Compás-generated slices (1) effectively focus test generation on specific features, preserving validity; (2) exercise unique code locations associated with the targeted features and thus enable traceability of features; and (3) enable test suite minimization, with a small set of slices retaining the aggregate coverage of the full suite while requiring fewer tests. To the best of our knowledge, this is the first work to apply product line engineering techniques to specification-based testing.


## 13. Finding Typing-Related Bugs in JVM Implementations

**Authors:** Yanzhou Lu (Tianjin University, China), Junjie Chen (Tianjin University, China), Yingquan Zhao (Tianjin University, China), Tianchang Gao (Tianjin University, China), Zan Wang (Tianjin University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834396

**中文总结:** 提出 Caster，依 JLS 类型规范与 LLM 编排 feature primitive 生成 bytecode 测试并在多 JVM 间比对结果；在 HotSpot/OpenJ9/Dragonwell 上发现 21 个未知 JVM 缺陷（18 已确认或修复）。

**Abstract:** As an object-oriented language, Java relies heavily on its type system. Existing testing efforts mainly target type-related implementations in the Java compiler, while the substantially different type-related implementations in the Java Virtual Machine (JVM) remain insufficiently tested. Although many techniques have been proposed for direct JVM testing, they mostly focus on specific components such as the JIT compiler or garbage collector, leaving type-related implementations underexplored. In this paper, we present Caster, the first technique for testing JVM type-related implementations by directly generating bytecode test programs guided by type specifications in the Java Language Specification (JLS). Specifically, Caster designs a set of feature primitives to encapsulate the operations needed for type-related testing, and leverages a Large Language Model (LLM) to identify type-related test scenarios from the JLS and guide primitive composition. Based on these scenarios, Caster organizes the selected primitive combinations into a multi-unit test-program generator, whose Cartesian-product expansion produces a large number of concrete test programs. To support large-scale execution, Caster dynamically loads these generated programs from memory and invokes them via reflection across different JVM implementations, collects their result lists, and compares them to identify inconsistencies and detect potential JVM bugs. Extensive experiments on four Long-Term Support OpenJDK versions of three popular JVM implementations (i.e., HotSpot, OpenJ9, and Dragonwell) demonstrate that Caster outperforms the state-of-the-art techniques in detecting more JVM inconsistencies. Moreover, Caster has uncovered a total of 21 previously unknown defects in the latest JVM releases, among which 18 have been confirmed or fixed by developers.


## 14. GraphDroid: Asynchronous LLM-Based Mobile App GUI Testing via History-Aware Exploration and Hybrid Intent Fulfillment

**Authors:** Xiaolei Li (Hong Kong University of Science and Technology, China / Southern University of Science and Technology, China / Guangzhou HKUST Fok Ying Tung Research Institute, China), Jialun Cao (Hong Kong University of Science and Technology, China / Guangzhou HKUST Fok Ying Tung Research Institute, China), Zhijian Hou (City University of Hong Kong, China), Yuzhi Zhao (City University of Hong Kong, China), Yepang Liu (Southern University of Science and Technology, China), Shing-Chi Cheung (Hong Kong University of Science and Technology, China / Guangzhou HKUST Fok Ying Tung Research Institute, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837449

**中文总结:** 提出 GraphDroid：聚类记忆识别未覆盖功能、异步意图生成与混合意图 fulfillment（复杂意图用 LLM、简单意图用启发式）；在 41 个 Android 应用上代码覆盖率最高提升 36.4%、成本低于纯 LLM 基线的八分之一，发现 19 个 bug（7 个为新报且 4 个已确认修复）。

**Abstract:** Automated GUI testing is a widely adopted technique for ensuring mobile application quality by simulating user interactions to exercise functionalities. Despite the research breakthroughs in the past decades, covering complex functionalities that require multi-step action sequences still remains challenging. Traditional tools lack semantic understanding capability and can rarely synthesize such action sequences. Recent LLM-based tools can generate test intents describing target functionalities and leverage the LLM to fulfill the intents, but suffer from three key limitations: 1) loss of historical context for identifying uncovered functionalities, 2) synchronous intent generation that blocks exploration, and 3) per-step LLM-driven fulfillment incurring high cost and latency. To address these limitations, we propose GraphDroid, an intent-driven GUI testing framework that integrates a cluster-based memory mechanism to effectively identify uncovered functionalities from historically visited states for comprehensive application testing. For improving testing efficiency, GraphDroid adopts an asynchronous intent generation paradigm that eliminates the latency bottleneck and a hybrid intent fulfillment strategy that reserves the LLM for fulfilling complex intents while delegating simple intents to a lightweight heuristic algorithm. We evaluate GraphDroid on 41 real-world Android apps against six state-of-the-art baselines. Results show that GraphDroid outperforms all baselines, achieving up to 36.4% higher code coverage while incurring less than one eighth of the cost of the best pure LLM-based baseline. GraphDroid also exposes 19 bugs in the 41 apps and detects 13 of 52 crashes in the Themis bug benchmark, surpassing all the six baselines. Seven of the 19 bugs were previously unknown and we reported them to the developers. So far, four bugs have been confirmed and fixed.


## 15. Gray-Box Fuzzing in Local Space

**Authors:** Martin Jonáš (Masaryk University, Czech Republic), Jan Strejček (Masaryk University, Czech Republic), Marek Trtík (Masaryk University, Czech Republic)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837510

**中文总结:** 将「沿固定路径在分支点翻转判定」的覆盖问题通过数值方法与线性代数变换到 local space 再 fuzz；在 Test-Comp 2025 基准上相对标准位翻转、随机 fuzz 与梯度下降在覆盖子问题与最大分支覆盖测试生成上有所改进。

**Abstract:** This paper formally defines and tackles a key problem of automated test generation. The coverage problem is specified by a program execution path leading to a certain branching point and an input vector of this execution. The goal is to modify the input vector such that the program running on the modified input follows the same path but the branching point is evaluated to the opposite truth value. Standard fuzzing techniques use bit flips, random fuzzing, and gradient descent to solve this problem. We present an approach that uses numerical methods and linear algebra to transform the problem to so-called local space and applies the mentioned techniques there. An experimental evaluation on the Test-Comp 2025 benchmarks shows some improvements over the standard fuzzing techniques, both for the studied coverage problem and for the problem of test generation for maximal branch coverage.


## 16. Hybrid Fuzzing in Input Generation Logic

**Authors:** Siwei Wei (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Shihao Zhu (Institute of Software at Chinese Academy of Sciences, China), Ruijie Meng (National University of Singapore, Singapore), Yan Cai (Institute of Software at Chinese Academy of Sciences, China)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834412

**中文总结:** 提出 hybrid generator space fuzzing：以输入生成器（非字节级种子）为求解单元、用 LLM 作约束求解器演化生成器，实现 GenEvo；在大量真实程序上显著优于通用、混合与生成式 fuzz 基线，兼顾语法合法与语义多样性。

**Abstract:** The core challenge of fuzzing is to consistently generate test inputs that are both syntactically valid and semantically diverse. However, mutation-based coverage-guided fuzzing often struggles to achieve this, especially for highly structured formats. Two lines of work have emerged to address this challenge: (1) hybrid fuzzing uses constraint solving to drive execution toward hard-to-cover program states to increase semantic diversity, and (2) generator-based fuzzing relies on predefined or synthesized input-generation programs to ensure syntactic validity. Both approaches, however, have significant limitations. (1) In hybrid fuzzing, solved inputs are fed back into the fuzzing queue for byte-level mutation, which often breaks syntactic structure (e.g., checksums and cross-field dependencies) and causes early rejection. (2) In generator-based fuzzing, semantic diversity is constrained by static generators based on domain knowledge; although recent work introduces generator mutations, they remain blind and therefore have limited adaptability to the target program’s logic. In this paper, we present hybrid generator space fuzzing, a method that combines the strengths of hybrid fuzzing and generator-based fuzzing to improve the syntactic validity and semantic diversity of test inputs. The key idea is to treat input generators, rather than test inputs, as the unit of targeted solving, and to use the LLM as constraint solver to derive new generators. This design offers two benefits. First, compared with hybrid fuzzing, it preserves syntactic validity because inputs are generated directly from evolving generators rather than through byte-level mutation of solved seeds. Second, compared with generator-based fuzzing, it overcomes the limitations of static generators and blind generator mutations, enabling the fuzzer to adapt to target program logic and explore a broader semantic space. Building on this concept, we implement GenEvo, an LLM-driven hybrid generator space fuzzer. Our evaluation on a large set of real-world programs shows that GenEvo, using a locally deployed medium-sized LLM, significantly outperforms competitive baselines (including general-purpose, hybrid, structure-aware, and LLM-assisted fuzzers) in both branch coverage (with an average improvement of 98.3%) and vulnerability discovery. Furthermore, GenEvo has discovered 25 previously unknown vulnerabilities in these extensively-tested programs.


## 17. IcFuzz: Fuzzing Isaac Sim with Semantic Stage Guidance and Multi-level Mutation

**Authors:** Zhixiang Chen (Sun Yat-sen University, China), Zhuangbin Chen (Sun Yat-sen University, China), Ruoxi Jia (Sun Yat-sen University, China), Zeqin Liao (Nanyang Technological University, Singapore), Wei Li (Sun Yat-sen University, China), Jinyang Liu (Chinese University of Hong Kong, Hong Kong), Zibin Zheng (Sun Yat-sen University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837550

**中文总结:** 首个针对 NVIDIA Isaac Sim 的 IcFuzz：LLM 语义阶段分割、多级变异与多臂 bandit 调度算子；覆盖率约为基线 190%–205%，12 小时三轮平均发现 3.7 个独有 crash（基线为 0），四个月确认/修复 9/11 个 bug。

**Abstract:** Robotics simulators serve as a foundational infrastructure for embodied AI, facilitating safe and scalable robotic system development. NVIDIA Isaac Sim has emerged as one of the most popular simulators, distinguished by its GPU-accelerated physics engine and photorealistic rendering, which enable high-fidelity modeling of complex environments. However, its inherent complexity inevitably introduces software bugs that can compromise simulation reliability. Existing fuzzing approaches struggle to test Isaac Sim effectively due to challenges of context-aware object semantics, hierarchical simulation control, and a vast simulation state space. In this paper, we propose IcFuzz, the first fuzzing approach for Isaac Sim. IcFuzz first performs an LLM-based semantic stage segmentation, decomposing simulation programs into structured stages that capture context-aware object semantics. Guided by this information, IcFuzz designs multi-level mutation operators to systematically exercise the simulator across hierarchical granularities. To efficiently navigate the vast simulation state space, IcFuzz employs a multi-armed bandit algorithm to adaptively schedule mutation operators. Experimental results show that IcFuzz outperforms the baselines in terms of both code coverage and bug detection. Specifically, IcFuzz achieves approximately 190%–205% of the code coverage of the baselines and detects an average of 3.7 unique crashes over three rounds of 12-hour tests, while no crashes are detected by the baselines. Moreover, IcFuzz has uncovered 11 bugs over approximately four months, 9 of which have been confirmed or fixed by the developers.


## 18. KQFuzz: Knowledge-Guided Fuzzing for Quantum Libraries via Large Language Models

**Authors:** Fuyuan Xia (Shanghai Jiao Tong University, China), Qixin Zhang (Nanyang Technological University, Singapore), Chenhao Ying (Shanghai Jiao Tong University, China), Haojin Zhu (Shanghai Jiao Tong University, China), Shuai Wang (Hong Kong University of Science and Technology, Hong Kong), Yuan Luo (Shanghai Jiao Tong University, China), Pingchuan Ma (Zhejiang University of Technology, China), Yuxuan Du (Nanyang Technological University, Singapore)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834392

**中文总结:** 提出 KQFuzz，以 LLM 与代码库知识引导量子库模糊测试，结合适应度评估与两级变异。在 Qiskit 等库上覆盖率最高提升 18.44%，确认 13 个缺陷。

**Abstract:** As quantum computing continually improves, ensuring the reliability and correctness of quantum libraries has become increasingly critical. To this end, many LLM-based fuzzing approaches towards quantum libraries have been proposed to uncover potential bugs. However, these methods still suffer from limitations such as insufficient flexibility and low efficiency, which hinder the progress of the quantum computing field. To address these challenges, we propose KQFuzz, a novel knowledge-guided fuzzer for quantum libraries. It leverages comprehensive codebase knowledge to ground LLM-based test generation, synergizing this with fitness-guided evaluation and two-level mutations to explore complex execution paths and trigger potential bugs. Firstly, KQFuzz introduces a novel prompting scheme tailored to quantum programs, which strategically incorporates knowledge of the codebase to efficiently generate high-quality quantum seed programs. Moreover, we develop evaluation and mutation strategies to handle the generated seed programs, facilitating efficient fuzzing execution while further enriching the diversity of the resulting test cases. We implement KQFuzz and conduct fuzzing on three popular quantum libraries, including Qiskit, PennyLane, and Cirq. Experimental results demonstrate that our approach significantly outperforms other state-of-the-art methods, with coverage improved by up to 18.44%. During the development of KQFuzz, we discovered 13 bugs, all of which have been confirmed and 12 have already been fixed by the developers.


## 19. Piece by Piece: Automating Combination Interaction GUI Testing via Planning and Dual Memory

**Authors:** Zhe Liu (Institute of Software at Chinese Academy of Sciences, China), Oujin Wang (Tsinghua University, China), Junjie Wang (Institute of Software at Chinese Academy of Sciences, China), Chunyang Chen (TU Munich, Germany), Mengzhuo Chen (Institute of Software at Chinese Academy of Sciences, China), Boyu Wu (University of Chinese Academy of Sciences, Beijing, China), Yuekai Huang (University of Chinese Academy of Sciences, Beijing, China / Institute of Software at Chinese Academy of Sciences, China), Qing Wang (Institute of Software at Chinese Academy of Sciences, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837553

**中文总结:** 提出 COMBDroid：识别组合交互模式、生成页面级计划并落地为控件动作，以 context/experience 双记忆协调执行；在 100 应用 100 个组合功能上通过率较最佳基线高约 103%，集成后 activity 覆盖升 65%–100% 并发现 37 个新 crash（26 已修）。

**Abstract:** Combination interactions require coordinated operations across multiple GUI widgets within a page to complete a functional task, which are common in modern mobile apps. However, due to widget dependencies, dynamic interface transitions, and context-sensitive execution, existing automated GUI testing approaches based on predefined models or state exploration struggle to reliably complete such interactions. LLM-based GUI testing methods improve semantic understanding but often generate inconsistent actions due to the lack of coordination modeling and interaction context. To address these challenges, this paper proposes COMBDroid, an automated GUI testing approach that enables reliable completion of combination interactions through structured planning and dual memory. COMBDroid first detects combination interaction patterns from GUI structure, then generates page-level interaction plans and grounds them into widget-level executable actions. Inspired by Sudoku solving, COMBDroid maintains a dual-memory mechanism, where context memory preserves execution states within a functionality and experience memory captures reusable interaction patterns. COMBDroid is designed as an integrable module that activates when combination interactions are detected and allows existing testing tools to resume exploration after completion. We evaluate COMBDroid on 100 combination interaction functionalities collected from 100 mobile apps, comparing it with 15 state-of-the-art GUI testing baselines. COMBDroid achieves 103% higher passing rate than the best baseline and improves activity coverage by 65%-100% when integrated with existing testing tools. Furthermore, GUI testing tools integrated with COMBDroid detect 37 new crash bugs in real-world apps, with 26 fixed and the remaining confirmed by developers, demonstrating its effectiveness in improving GUI testing.


## 20. Planner-Fuzz: Overcoming Diagnostic Saturation in UAV Planners via Boundary-Oriented Fuzzing

**Authors:** Rongbo Chen (Zhejiang University, China), Chengcheng Zhao (Zhejiang University, China), Peng Cheng (Zhejiang University, China), Jiming Chen (Zhejiang University, China), Taegyu Kim (Pennsylvania State University, USA)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834389

**中文总结:** 针对 UAV planner 参数 fuzz 中“深入失败区”导致诊断饱和的问题，提出 Planner-Fuzz 在安全边界窄带搜索多样边界配置，并做灵敏度、交互与反事实三层诊断；在三款开源 planner、四类异常上比失败驱动基线得到更多可解释边界与更强干预恢复证据。

**Abstract:** UAV planners are safety-critical software components whose behavior depends on high-dimensional, continuously tunable parameters. While existing fuzzing approaches focus on discovering failures, configurations deep inside failure regions are often diagnostically uninformative.Once the planner moves far beyond the safety boundary, parameter sensitivity diminishes, and inter-parameter dependencies become obscured.We refer to this phenomenon as diagnostic saturation and observe that configurations near the safe-unsafe transition preserve informative parameter sensitivity and interaction structure, making them more suitable for root-cause analysis. To this end, we propose Planner-Fuzz, a boundary-oriented fuzzing framework. It steers search toward a narrow band around the safety boundary while preventing convergence to a single configuration to enable the exploration of diverse boundary behaviors. Using the collected boundary configuration, Planner-Fuzz performs three-level diagnosis through sensitivity analysis, interaction mining, and counterfactual validation to identify and validate the parameters responsible for failure behavior.  
We evaluate the approach on three open-source UAV planners under four anomaly types. The results show that Planner-Fuzz discovers more diverse and diagnostically useful boundary configurations than failure-driven baselines, provides stronger signals for identifying influential parameters and interactions, and yields stronger intervention-based recovery evidence.  
These findings suggest that fuzzing for safety-critical planners should go beyond failure discovery and explicitly support diagnosis.


## 21. Predicate-Guided Synthesis of Input Generators via Gentoo

**Authors:** Vasudev Vikram (Carnegie Mellon University, USA), Rohan Padhye (Carnegie Mellon University, USA)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837441

**中文总结:** 提出 Gentoo，让 LLM coding agent 在终端访问目标与可选谓词级覆盖反馈下迭代合成 Java 库 fuzz 输入生成器；7 库基准上 agent 生成器在 4/7 超过人工生成器，且 agent 生成器几乎不依赖 coverage guidance，而人工生成器仍显著受益。

**Abstract:** Modern generator-based fuzzing techniques combine lightweight input generators with coverage-guided mutation as a method of exploring deep execution paths in a target program. A complementary approach in prior research focuses on creating highly customized, domain-specific generators that encode structural and semantic logic sufficient enough to reach deep program states; the challenge comes from the overhead of writing and testing these complex generators. We investigate whether AI coding agents can automatically synthesize such target-specific generators, and whether the resulting generators are strong enough to obviate the need for coverage guidance and mutation entirely. Our approach, Gentoo, is comprised of an LLM coding agent (provided terminal access and source code of the fuzz target and its library) instructed to iteratively synthesize and refine an input generator, and optionally provided fine-grained predicate-level coverage feedback. We evaluate three configurations of Gentoo against human-written generators on fuzz targets for 7 real-world Java libraries. Our findings show that agent-synthesized generators achieve statistically significantly higher branch coverage than human-written baseline generators on 4 of 7 benchmarks. Critically, the use of coverage guidance and mutation strategies is not statistically significantly beneficial for agent-synthesized generators, but is significant for all human-written generators, suggesting that structural and semantic logic encoded in the agent generators makes coverage guidance largely unnecessary.


## 22. Property-Based Testing of Wafer Handling Robots via Model-Based Planning and Fuzzing

**Authors:** Ruiyang Xu (East China Normal University, China), Jingjing Liang (East China Normal University, China), Guoyue Zheng (East China Normal University, China), Geguang Pu (East China Normal University, China), Ting Su (East China Normal University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834360

**中文总结:** 提出面向 wafer handling robot（WHR）的 property-based testing，结合 model-based planning 与 fuzzing 生成有效测试输入。ArmGo 在生产 WHR 上发现 21 个已确认缺陷（15 个已修复）并部署于工业 CI 流水线。

**Abstract:** Wafer handling robots (WHRs) in semiconductor manufacturing require ultra-precise control software, where bugs can cause severe mechanical damage and costly downtime, making reliability validation critical. Yet no existing work addresses WHR validation. In this experience paper, we introduce a property-based testing approach for WHRs. Our key observation is that the system requirements of WHRs could be used as the properties for bug detection.However, applying property-based testing to WHR systems is challenging due to the input generation challenge. Complex action dependencies make it difficult to generate valid test inputs, while enormous state spaces hinder achieving adequate test coverage. To address this, we propose model-based planning and fuzzing. Our insight is that the WHR can be represented as a state-based model. Based on this model, we systematically generate valid test inputs through backward planning, then explore diverse scenarios through parameter and environment mutation. We implemented our approach as the ArmGo tool and evaluated it on a production WHR deployed in industrial lithography equipment. ArmGo discovered 21 previously unknown bugs (all confirmed, 15 fixed), including axis limit violations, entanglement issues, and missing interlock checks. ArmGo has been deployed in the continuous integration (CI) pipeline of our industrial partner and is actively used for validating WHRs. We also have distilled a number of practical lessons learned based on our investigation.


## 23. PropGen: Automated Property Generation for Property-Based Testing of Mobile Apps

**Authors:** Yiheng Xiong (Singapore Management University, Singapore), Shiwen Song (Singapore Management University, Singapore), Bo Ma (East China Normal University, China), Ting Su (East China Normal University, China), Xiaofei Xie (Singapore Management University, Singapore)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837536

**中文总结:** 提出 PropGen：从 GUI 假设功能、执行取证、LLM 合成性质并以测试反馈精炼，支撑移动 app 基于性质测试；12 款 Android app 上推断 1,210 个有效功能、生成 912/985 有效性质，发现 25 个此前未知功能 bug。

**Abstract:** Mobile apps often suffer from functional bugs that do not cause crashes but instead manifest as incorrect behaviors under specific user interactions. Such bugs are difficult to detect by conventional automatic testing techniques because they often lack explicit test oracles . Property-based testing can effectively expose them by specifying intended behavior as properties and checking them under diverse interactions. However, its practical use is limited by the reliance on manually written properties, which are difficult and expensive to construct. To address this limitation, this paper explores the use of large language models (LLMs) to automate property construction for property-based testing of mobile apps. This is challenging in two ways. First , it is difficult to systematically uncover and execute diverse app functionalities. Second , it is difficult to derive valid properties from functionality execution results. To address these challenges, we introduce PropGen, which infers candidate app functionalities as hypotheses from GUI states, validates each hypothesis by executing it to collect behavioral evidence, synthesizes properties from the collected evidence, and refines imprecise properties based on testing feedback. We implemented PropGen and evaluated it on 12 real-world Android apps. The results show that PropGen can effectively identify and execute app functionalities, generate valid properties, and refine most imprecise ones. Across all apps, PropGen inferred 1,210 valid functionalities and correctly executed 977 of them, compared with 491 and 187 for the baseline. It generated 985 properties, 912 of which were valid, and successfully refined 118 of 127 imprecise ones exposed during testing. Using the resulting properties, we found 25 previously unknown functional bugs, many of which were missed by existing testing techniques.


## 24. PWCC: Probability-Weighted Combinatorial Coverage for Risk-Informed Scenario Testing of Autonomous Systems

**Authors:** Borhaneddine Hamadou (Université Paris-Saclay, France / CEA List, France), Chokri Mraidha (Université Paris-Saclay, France / CEA List, France), Nikolaos Matragkas (Université Paris-Saclay, France / CEA List, France)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837443

**中文总结:** 提出 PWCC，用运营剖面概率为 t-way 场景组合赋权，当未覆盖风险质量低于阈值时给出“测够了吗”的停止准则；在四套自动驾驶数据上对故障发现 Spearman 最高 0.981，并消除组合覆盖常见的虚假充分（DeepScenario FSR/UFC=0）。

**Abstract:** Scenario-based testing of autonomous systems faces a fundamental unsolved problem: knowing when to stop. Existing coverage metrics measure either structural diversity or combinatorial breadth, but neither tells you how much of the system’s expected real-world operation remains untested. A test suite can score well on every existing metric while systematically missing the conditions the system will actually encounter. We introduce Probability-Weighted Combinatorial Coverage (PWCC), a metric that simultaneously measures coverage of the Op- erational Design Domain (ODD) and test adequacy. PWCC learns a probabilistic model of expected operating conditions from oper- ational profiling data, uses it to assign probability mass to 𝑡-way combinations of scenario features, and declares testing adequate when the uncovered mass falls below a risk-calibrated threshold. This gives practitioners something no existing metric provides: a principled, quantitative answer to “have we tested enough?” Evaluated on four autonomous driving datasets against seven baselines, PWCC demonstrates three properties. First, it is the strongest predictor of fault detection where the operational dis- tribution carries signal, reaching Spearman 𝑟𝑠 = +0.981 on Deep- Collision — 0.167 above the best combinatorial baseline at a lower interaction order. Second, it suppresses false sufficiency: on Deep- Scenario, PWCC achieves FSR = UFC = 0 across all splits versus CC’s mean UFC ≥ 95.8%, false sufficiency eliminated entirely, and, judged at its own stopping point, surfaces 99.6% of failure-triggering com- binations where combinatorial saturation stops after 6.4% of the campaign; on failure-rich datasets UFC drops by up to 4.9×. Third, it is stable: the score varies by at most 0.006 across a ten-fold increase in Monte Carlo sample size and grows monotonically with suite size. These results show that operational probability weighting is the decisive factor in avoiding dangerous false sufficiency verdicts; and that PWCC transforms coverage from a descriptive statistic into a risk-informed stopping decision.


## 25. QDoctor: Probe-Based Testing for Quantum Programs

**Authors:** Qichen Wang (Kyushu University, Japan), Shangzhou Xia (Kyushu University, Japan), Xiaoyu Guo (Kyushu University, Japan), Jianjun Zhao (Kyushu University, Japan)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837488

**中文总结:** 提出黑盒框架 QDoctor，用 property-based probe 联合设计输入与测量基，并支持语义约束的部分等价 oracle 降误报；基准上 F1 99.06%、AUC 0.9988，联合强化输入与测量将 recall 提至 99.728% 且 SWAP 等价 mutant 零误报。

**Abstract:** Testing quantum programs in a black-box setting is difficult because bug-relevant behavioral differences may be missed at two levels: the chosen inputs may fail to trigger faulty behavior, and even when faults are triggered, the chosen measurements may fail to make the resulting differences observable. Existing methods have mainly strengthened either input generation or measurement design in isolation, leaving their coupling insufficiently addressed. In this paper, we present QDoctor, a probe-based black-box testing framework that wraps the program under test with a variety of property-based probes, thereby effectively extracting program information and exploring its behavior. A probe integrates two components: test-case generation and the specification of the measurement basis. To reduce false positive rate, QDoctor also supports semantic-aware partial equivalence testing through constrained probe-oracle design. Experimental results on benchmark suites show that QDoctor achieves the best balanced performance among representative black-box baselines, reaching 99.89% recall, 98.23% precision, 99.06% F1, and 0.9988 AUC. Ablation shows that jointly strengthening inputs and measurements raises recall from 85.280% to 99.728% with zero false positives, while semantic probes drive the false-positive rate to zero on SWAP-induced equivalent mutants.


## 26. Quantum Squeeziness: An Information Theoretical Metric for Quantum Software Testability

**Authors:** Avner Bensoussan (King's College London, UK), Hector Menendez (King's College London, UK), Mohammad Reza Mousavi (King's College London, UK)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834341

**中文总结:** 首次形式化量子软件可测试性，提出信息论指标 Quantum Squeeziness 量化故障掩蔽程度；在 5 万余变异体上其与变异分数强负相关，FastSqueeziness 将平均计算时间从 3200s 降至 189s（约 16.9 倍加速）。

**Abstract:** Testability—the degree to which faults can be revealed and diagnosed—has long been fundamental in software engineering but remains largely unexplored for quantum software. This work presents the first formalisation of testability for quantum programs, adapting classical concepts to quantum computation. We introduce Quantum Squeeziness, an information-theoretic metric inspired by classical squeeziness, to quantify how faults are masked and prevented from propagating to observable outcomes. We treat it as an inverse measure of testability: higher squeeziness implies stronger fault masking and reduced detectability. We propose an efficient method to compute Quantum Squeeziness and validate it through large-scale quantum mutation analysis. Across more than 50k mutants, we observe a strong negative correlation between squeeziness and mutation score, showing that higher squeeziness predicts lower testability. We further introduce a technique that constrains where and how perturbations are injected, reducing cost while preserving accuracy. The computation is 15% faster than a standard error-propagation baseline, while the optimised variant, FastSqueeziness, reduces mean runtime from 3200s to 189s (16.9 times speedup) with 95% accuracy. By establishing a rigorous foundation of testability for quantum software, this work opens new directions at the intersection of software engineering, quantum information theory, and testing. Beyond testing and debugging, it also supports applications in quantum error mitigation and correction, enabling principled assessment and improvement of program robustness.


## 27. RamFuzz: LLM-Guided Greybox Fuzzing for Spatial Memory Corruption via Valid Range Violation

**Authors:** Shangzhi Xu (University of New South Wales, Australia / CSIRO's Data61, Australia), Wei Song (University of New South Wales, Australia / CSIRO's Data61, Australia), Yuekang Li (University of New South Wales, Australia), Nan Sun (University of New South Wales, Australia), Muhammad Ejaz Ahmed (CSIRO's Data61, Australia), Willy Susilo (University of Wollongong, Australia), Benjamin Turnbull (University of New South Wales, Australia), Xiao Cheng (Macquarie University, Australia), Siqi Ma (University of Wollongong, Australia)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837447

**中文总结:** 提出 RamFuzz，利用 LLM 枚举格式合法范围并在种子中故意赋非法值以触发 spatial corruption（72.7% CVE 与此相关）；在 15 个高星项目上发现 104 个未知内存破坏（39 确认、33 已修）。

**Abstract:** Spatial memory corruptions remain among the most prevalent software vulnerabilities, consistently ranking among the top CWE categories. These vulnerabilities are closely tied to the values processed by the program: when input-derived values fall outside expected ranges, memory operations may be performed beyond their allocated bounds, leading to corruption. Our pilot study on 132 realworld CVEs shows that 72.7% of spatial memory corruptions stem from such valid value violations. Although fuzzing is widely used to expose exploitable memory corruptions, systematically detecting spatial memory corruptions through fuzzing remains challenging, as it requires generating inputs that conform to complex structural formats while violating valid value ranges. Recent work leverages LLMs to generate structured inputs based on format knowledge, yet LLMs exhibit a strong bias toward well-formed outputs, leaving systematic range violations largely unexplored. In this paper, we propose RamFuzz, an approach that exploits rather than mitigates this bias to guide the fuzzing process. RamFuzz prompts LLMs to enumerate valid ranges of target file formats and deliberately assigns invalid values to seeds during fuzzing, systematically triggering spatial memory corruptions. We evaluated RamFuzz on 15 popular real-world projects with more than 1,000 stars on GitHub, RamFuzz discovered 104 previously unknown memory corruptions, of which 39 have been confirmed, and 33 have been fixed by developers.


## 28. Real-World Perturbation Testing of Autonomous Driving Systems

**Authors:** Stefano Carlo Lambertenghi (TU Munich, Germany / fortiss, Germany), Matthias Weil (TU Munich, Germany), Andrea Stocco (TU Munich, Germany / fortiss, Germany)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834418

**中文总结:** 对 72 种相机/LiDAR 扰动在离线模型、HIL 与封闭环路实车三层次做大规模对比；相机端到端系统离线影响小扰动仍可致实车失控，LiDAR 感知退化与系统级失败相关性弱，强调仅模型指标不足以代表实车鲁棒性。

**Abstract:** Autonomous Driving Systems (ADS) must operate reliably under diverse conditions, yet representative data for rare or adverse scenarios is difficult to obtain. Perturbation-based testing is widely used to assess robustness, but most studies focus on offline datasets or simulation, leaving open questions about how such results translate to real-world driving. We present a large-scale study of 72 camera and LiDAR perturbations, evaluated across three testing modalities: offline model-level analysis, hardware-in-the-loop execution, and closed-loop system-level testing on a full-scale autonomous vehicle. The study covers both an end-to-end vision-based driving model and a modular LiDAR-based perception and planning stack. Our results reveal a clear gap between testing levels. For camera-based systems, perturbations with limited offline impact can still induce unstable control and failures in real-world driving. For LiDAR-based systems, degradation is more consistent at the perception level but weakly predictive of system-level failures. Across both modalities, model-level metrics alone are insufficient to identify the most harmful perturbations.We further show that real-time feasibility is a key constraint in real-world testing, and that robustness observations obtained from recorded data do not consistently transfer to closed-loop behavior on a physical vehicle, highlighting the importance of complementary real-world, system-level evaluation.


## 29. RustGTC: Constraint-Guided Test Generation for Rust APIs via Comment Analysis and Code Context

**Authors:** Yichi Zhang (Peking University, China), Jinhao Huang (Institute of Software at Chinese Academy of Sciences, China), Yang Feng (Nanjing University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837531

**中文总结:** 提出 RustGTC，从 API 注释抽取文档化参数约束、围绕边界构造测试并修复编译；在 12 个 crate 上高覆盖并发现 41 个缺陷，132 个提交测例中 123 被接受，揭示注释–代码在边界处的不一致。

**Abstract:** Manually crafting test cases for Rust APIs is labor-intensive and error-prone, especially because of Rust’s advanced features and complex trait system. Recent advances in large language models (LLMs) have shown promise in automated test generation; however, existing approaches often underuse documented input requirements embedded in API comments. We present RustGTC, a framework that uses API comments to guide Rust API test generation. RustGTC extracts documented parameter constraints from comments, constructs tests around boundary cases, and repairs generated tests to improve compilability. We evaluate RustGTC on 12 Rust crates, achieving high coverage and uncovering 41 defects. Additionally, we submitted 132 test cases; 123 were accepted, 9 were rejected. These results show that RustGTC uses documented constraints to guide Rust API test generation and reveal comment-code inconsistencies around boundary cases.


## 30. SpecTrum: Specification-Guided Differential Fuzzing for Ethereum Consensus Clients

**Authors:** Seokhun Jeong (KAIST, Republic of Korea), Gyeongmin Dan (Sungkyunkwan University, Republic of Korea), Sukyoung Ryu (KAIST, Republic of Korea), Sungjae Hwang (Sungkyunkwan University, Republic of Korea)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834406

**中文总结:** 提出 Consensus-SpecTec 将以太坊共识 validity 显式化为 if-premise，定义 premise coverage 并生成补覆盖测试；在五大共识客户端发现 27 个跨客户端分歧（22 个依赖新 mechanization），且 fork 扩展成本与规范差异成正比。

**Abstract:** Ethereum's consensus safety relies on independent consensus client implementations agreeing on every state transition. When they diverge due to implementation errors, the network can fork, finality can stall, and severe attacks are possible. To prevent such consensus divergences, Ethereum provides a Python reference implementation (consensus-spec), which acts as a specification, and a hand-crafted official test suite (spectests). However, as an executable implementation, Ethereum's specification defines validity implicitly through runtime behavior. As a result, it lacks a systematic way to ensure that all validity conditions are thoroughly evaluated. We present SpecTrum, a framework that addresses this problem in three stages. First, we introduce Consensus-SpecTec, a mechanized specification of the Ethereum consensus algorithm, which makes validity conditions explicit as if-premises. Second, we define premise coverage, a metric that measures which if-premises are evaluated to true and false across spectests. Third, we develop a specification-based test generator that extracts constraints on premises not evaluated to false by spectests and generates inputs to evaluate them. Applying SpecTrum to five major Ethereum consensus clients, we identify 27 cross-client divergence cases, 22 of which cannot be found without the premises inserted in our mechanization. All 27 cases reproduce across fork versions, and extending the mechanized specification to a new fork takes modest effort proportional to the specification difference.


## 31. Stop When It Matters: Detectability-Guided Microbenchmarking for Performance Regression Testing

**Authors:** Zongxiong Chen (Fraunhofer FOKUS, Germany), Derui Zhu (Rochester Institute of Technology, USA), Jinfu Chen (Wuhan University, China), Kundi Yao (Ontario Tech University, Canada), Alexander Pretschner (TU Munich, Germany / fortiss, Germany), Weiyi Shang (University of Waterloo, Canada), Manfred Hauswirth (Fraunhofer FOKUS, Germany / Technische Universität Berlin, Germany), Sonja Schimmler (Fraunhofer FOKUS, Germany / Technische Universität Berlin, Germany)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834367

**中文总结:** 将性能微基准执行形式化为最小可检测效应（MDE）两阈值问题，分两阶段自适应停采与回归判定并给出误差界；1702 个微基准上执行时间最高降 93%，FPR 与 power 贴近理论目标。

**Abstract:** Performance microbenchmarks are widely used for detecting performance regressions in continuous integration, yet existing execution policies remain computationally expensive. We present detectability-guided microbenchmarking, a principled framework that reformulates benchmark execution as a Minimum-Detectable-Effect (MDE) problem, achieving substantial speedups with formal statistical guarantees. Our approach introduces a two-threshold specification: a lower threshold, δ 0 , for negligible slowdowns, and an upper threshold, δ 1 , for meaningful regressions. We theoretically and empirically show that this specification enables bounded false-positive rates below δ 0 and guaranteed statistical power around δ 1 , while dramatically reducing execution time. To realize this framework, we propose a two-phase procedure: Phase 1 adaptively controls execution via online sample-size re-estimation guided by minimum detectable effect, enabling early stop when sufficient statistical resolution is reached and futile abort when target detectability is unattainable within the execution budget; Phase 2 performs regression analysis under the same specification, yielding decisions with provable error bounds. Experiments on 1702 microbenchmarks from three large-scale open-source projects demonstrate up to 93% reduction in execution time while empirical false-positive rates and power closely match their theoretical targets. Our findings reveal that detectability-guided execution offers a theoretically grounded yet practical path toward efficient microbenchmark-based regression detection.


## 32. TDiFf: Detecting Bugs in DataFrame Systems via Transferred DBMS Test Cases

**Authors:** Jiaxin Hu (Xiamen University, China), Shaowei Chen (Fujian Agriculture and Forestry University, China), Rongxin Wu (Xiamen University, China)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837548

**中文总结:** 提出 TDiFf，将 SQL 结合文档特征知识与查询计划数据流图翻译为 Python DataFrame 差分测试；六套系统（Pandas/Dask/CuDF 等）生成用例 >99% 有效，确认 35 个 unique bug，相对 SOTA 高 2.5×–14×。

**Abstract:** DataFrame systems are core components of modern data analytics platforms and achieve high performance through various optimization techniques. However, these optimizations can introduce subtle defects that are difficult to detect, undermining system reliability. Existing testing approaches primarily rely on manually written unit tests or automated unit test generation tools, which often produce invalid or low-quality test cases and have limited ability to exercise complex API sequences and optimization-induced behaviors. In this paper, we present TDiFf, a novel LLM-based testing framework for DataFrame systems. TDiFf leverages the database-like characteristics of DataFrame systems by translating SQL query statements into Python DataFrame test cases for differential testing. To address limitations of LLMs in mapping SQL constructs to DataFrame APIs and preserving semantic consistency, TDiFf incorporates feature knowledge extracted from SQL and DataFrame API documentation. In addition, it utilizes data flow graphs derived from SQL query plans to guide the generation of syntactically valid and semantically consistent DataFrame API sequences. We evaluate TDiFf on six widely used DataFrame systems: Pandas, Dask, CuDF, Modin, PySpark, and Polars. The results show that more than 99% of the generated DataFrame test cases are valid. Using these test cases, TDiFf uncovers 35 unique and previously unknown bugs confirmed by developers, and outperforms state-of-the-art baseline approaches by 2.5× to 14×.


## 33. TDRepro: A Neurosymbolic Approach to Reproducing Timing-Dependent Flaky Test Failures

**Authors:** Shanto Rahman (University of Texas at Austin, USA), Talank Baral (George Mason University, USA), August Shi (University of Texas at Austin, USA), Wing Lam (George Mason University, USA)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834384

**中文总结:** 提出 TDRepro：并发方法筛选 + 嵌入相似度排序 + LLM 定位延迟注入点并迭代验证；82 个 Java TD flaky 测试上相对 FlakeRake 多复现 100% 失败，55 个测试复现率 >99%，重复复现时间约为重跑测试的 1/1482。

**Abstract:** Tests that nondeterministically pass or fail on the same version of code are known as flaky tests, and their failures substantially hinder regression testing and debugging. Reproducing failures from timing-dependent (TD) flaky tests is particularly challenging because these failures depend on rare thread interleavings that may not occur even after running the test many times. Prior approaches reproduce such failures by searching for locations at which to inject delays during execution, but this search process can be expensive. We present TDRepro, an automated approach that leverages large-language models (LLMs) and program analysis to efficiently reproduce TD-test failures. TDRepro first identifies relevant methods by collecting executed methods during the test run and identifying those that execute concurrently with other methods. It then ranks these methods by computing the embedding similarity between each method’s code and the observed failure log. Finally, TDRepro uses an LLM to identify candidate locations for delay injection within the top-ranked methods. TDRepro validates these candidates by injecting delays and rerunning the test, iteratively refining the candidate locations based on unsuccessful attempts until the target failure is reproduced or the maximum number of iterations is reached. We evaluate TDRepro on 82 TD tests across 25 modules from open-source Java Maven projects. TDRepro reproduces 100% more failures than the prior state-of-the-art approach, FlakeRake, and achieves more reliable reproduction, with 55 tests reaching a failure reproduction rate of >99%, compared with 30 tests for FlakeRake. Repeatedly reproducing failures with TDRepro requires 1482.1× and 10.4× less time and costs 888.4× and 9.6× less than repeatedly rerunning tests and using FlakeRake, respectively.


## 34. Testing IFrame Rendering in Web Browsers

**Authors:** Dahyeon Park (UNIST, Republic of Korea), Yuseok Jeon (Korea University, Republic of Korea), Seongil Wi (UNIST, Republic of Korea), Mijung Kim (UNIST, Republic of Korea)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834417

**中文总结:** 提出 ICheck，通过对比同一 HTML 在顶层页与 iframe 中的渲染结果实现跨上下文 oracle，并做布局感知的输入缩减以定位致错元素；在 Chrome 与 Firefox 上确认 21 个未知 iframe 专属渲染缺陷，缺陷发现量约为 SOTA 的 3.8×，DOM 缩减约 93%。

**Abstract:** Iframes are widely used in modern web development, but their separation from the parent page can lead to iframe-specific rendering bugs, which occur only when content is embedded within an iframe. These bugs may degrade user experience and, in some cases, lead to serious security vulnerabilities. However, existing rendering bug detection techniques are largely ineffective since their oracles compare rendering outputs only within the same context and fail to capture discrepancies across different rendering contexts. This paper presents ICheck, an automated testing technique for iframe rendering in web browsers. Specifically, given an HTML document, ICheck introduces a cross-context oracle that detects inconsistencies by comparing the same HTML content in both top-level and iframe contexts. To further assist debugging, ICheck performs layout-aware input reduction by redefining the effective search space of bug-inducing elements. As a result, ICheck helps developers more effectively and efficiently identify and diagnose iframe-specific rendering bugs. Evaluated on the most popular browsers, Chrome and Firefox, ICheck detected 21 previously unknown bugs, all of which were confirmed. On average, ICheck uncovered 3.8× more bugs than state-of-the-art rendering bug detection work. In addition, ICheck effectively reduced HTML inputs by 93% in DOM nodes while achieving up to 10.1× faster reduction time compared with state-of-the-art delta debugging approaches.


## 35. Testing Static Analyzers via Semantic-Preserving Mutators Learned from Real-World Refactoring Practice

**Authors:** Meilin Li (Chongqing University, China), Kaixuan Li (Nanyang Technological University, Singapore), Zifan Xie (Chongqing University, China), Shiyu Qiu (Huazhong University of Science and Technology, China), Ming Wen (Huazhong University of Science and Technology, China), Maolin Sun (Nanjing University, China), Hongyu Zhang (Chongqing University, China)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837544

**中文总结:** 提出 SAFuzzer，从真实重构实践中挖掘并泛化语义保持变异算子用于静态分析器的蜕变测试；生成 313 个 mutator，在 5 款主流 Java 静态分析器上发现 42 个未知缺陷，优于五种 SOTA 基线。

**Abstract:** Static analyzers reason about program behavior without execution and report issues when code violates predefined rules. A key limitation is their production of inaccurate, incomplete results, generating spurious warnings and missing critical issues. Metamorphic testing is the most commonly used method to efficiently detect bugs in static analyzers. It requires designing a set of semantic-preserving mutators. When a mutator is applied to a seed program, any discrepancy in the analyzer's reports for the original and mutated versions indicates a potential bug. Thus, efficiently generating large numbers of semantic-preserving mutators is critical. We observe that during routine software maintenance, developers often restructure code to improve readability or optimize it without changing external program behavior. Our key insight is that mining and generalizing these patterns from real-world refactoring practice enables the automatic construction of numerous mutators that reflect the distribution of real-world code variants. We present SAFuzzer, a framework that mines such refactoring practice and distills these edits into semantic-preserving mutators. We ultimately generate 313 mutators and apply them to detect bugs in five widely used Java static analyzers. SAFuzzer detects 42 previously unknown bugs. Compared with five state-of-the-art baselines, SAFuzzer detects the most bugs, demonstrating the value of learning diverse mutators from real-world refactoring practice.


## 36. TrackTest: Trajectory Generation and Prioritization for Testing Multiple Object Tracking System

**Authors:** Xinyu Gao (Nanjing University, China), Haoxin Chen (Nanjing University, China), Shuoxiao Zhang (Nanjing University, China), Enyi Tang (Nanjing University, China), Hengrui Xu (Nanjing University, China), Haoxiang Tian (Nanyang Technological University, Singapore), Minghui Wei (Nanjing University, China), An Guo (Hong Kong Polytechnic University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837540

**中文总结:** 提出 TrackTest，将真实种子场景转为六种驾驶模式约束优化下的物理可行、行为多样轨迹，并用 prioritization 聚焦高风险用例以暴露 MOT 失败；在六种 SOTA MOT 系统上有效生成多样轨迹并揭示多种跟踪失败。

**Abstract:** Multiple Object Tracking (MOT) is a fundamental component of the perception stack in Autonomous Driving Systems (ADS), providing essential state estimation for downstream decision-making. Despite the adoption of multi-sensor fusion to enhance reliability, MOT systems remain susceptible to tracking failures, which can lead to catastrophic safety incidents. Current perception testing and evaluation predominantly rely on manually annotated real-world datasets, which are behaviorally imbalanced, prohibitively expensive to scale, and insufficient to cover diverse dynamic interactions. To bridge this gap, we propose TrackTest, an automated testing framework designed to systematically expose tracking failures in MOT systems. TrackTest transforms real-world seed scenarios into challenging test cases by synthesizing physically feasible and behaviorally diverse trajectories. We formulate six representative driving patterns as constraint-based optimization problems for behavior-controllable trajectory generation. To reduce computational overhead, we introduce a trajectory prioritization strategy that identifies high-risk scenarios most likely to trigger tracking failures. We evaluate TrackTest on six state-of-the-art MOT systems. Experimental results show that TrackTest effectively generate behavior-diverse trajectories and uncover diverse tracking failures.


## 37. WebCQ: Cooperative Multi-agent Deep Reinforcement Learning for Scalable Web GUI Testing

**Authors:** Yujia Fan (Southern University of Science and Technology, China), Sinan Wang (Southern University of Science and Technology, China), Zebang Fei (Southern University of Science and Technology, China), Yao Qin (Southern University of Science and Technology, China), Huaxuan Li (Southern University of Science and Technology, China), Yepang Liu (Southern University of Science and Technology, China)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834374

**中文总结:** 提出 WebCQ，以 QTRAN 协调多 agent DQN，在异步 Web 场景下用语义与探索特征构成动态动作空间；在 8 个大型商业网站相对 MARG 多探索 33.3% 状态、多执行 42.2% 唯一动作，20 小时长跑中吞吐与扩展性更优。

**Abstract:** Multi-agent reinforcement learning (MARL)-based techniques have shown promise for GUI testing. However, as the complexity of modern GUI software increases, existing MARL-based approaches (e.g., MARG and Fastbot ) struggle to scale due to the inherent limitations of their underlying tabular reinforcement learning algorithms. This limits their applicability to large-scale commercial GUI software, especially web applications with vast state spaces and many interactive elements. To fill this gap, we propose WebCQ , a novel MARL-based approach for scalable web GUI testing. WebCQ incorporates QTRAN for multi-agent coordination and a lightweight synchronization mechanism, allowing it to work under asynchronous web testing scenarios. It extracts semantic and exploration features for each UI event to form an action vector. This vector is concatenated with the current state vector and fed into the policy network, enabling DQN-based decision making within a dynamic action space. We evaluated WebCQ on eight large-scale commercial websites. Under the same time budget and agent count, WebCQ explored 33.3% more states and executed 42.2% more unique actions than MARG , while triggering more failures on six of the eight websites under test. It also demonstrated strong scalability, maintaining higher action throughput during 20-hour experiments, and achieving greater performance improvements as the number of agents increased. These results show that WebCQ overcomes key limitations of existing MARL-based approaches, providing a scalable and effective solution to enhance modern web GUI testing.


## 38. When Knowledge Changes: Metamorphic Testing of RAG Systems with Mutations

**Authors:** Jinhan Kim (USI Lugano, Switzerland), Samuele Pasini (USI Lugano, Switzerland), Paolo Tonella (USI Lugano, Switzerland)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837543

**中文总结:** 提出面向语料演化的 RAG 蜕变测试框架，含故障分类与 11 个索引/上下文级 mutation 算子；五数据集 2.8 万+ mutant 上违规率 4.9%–10.2%，蜕变 oracle F1 达 0.927–1.000，显著优于 RAGAS 最佳 0.570。

**Abstract:** Retrieval-Augmented Generation (RAG)-based LLM systems rely on external document corpora that can evolve and change over time. However, current evaluation methodologies (e.g., RAGAS) assess correctness against static snapshots, failing to detect faults when routine updates, factual changes, or noise alter the underlying data. We introduce a metamorphic testing framework that evaluates the consistency of RAG systems under corpus evolution. We formalise a fault taxonomy and 11 mutation operators that systematically perturb the system at both the pre-chunk (retrieval index) and post-chunk (retrieved context) levels. An empirical evaluation across five datasets and over 28k mutants reveals metamorphic violation rates of 4.9-10.2%. In a meta-evaluation against ground truth, our metamorphic oracle achieves F1 scores of 0.927-1.000, while the best RAGAS metric reaches only 0.570. Finally, we provide actionable insights into mitigating these faults through retrieval re-configuration, generator upgrades, and LLM-based reranking.


## 39. Where Does Balance Break? Boundary Discovery for Game Balance Testing under a Finite Simulation Budget

**Authors:** Hiroki Mukai (Ritsumeikan University, Japan), Yusaku Kato (Ritsumeikan University, Japan), Norihiro Yoshida (Ritsumeikan University, Japan), Erina Makihara (Ritsumeikan University, Japan), Katsuro Inoue (Ritsumeikan University, Japan)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834407

**中文总结:** 将多人竞技游戏的平衡回归测试建模为有限仿真预算下的边界发现问题，提出 BBExplorer，结合多方向候选生成、预算感知两阶段筛选与自适应步长收缩来高效定位平衡与失衡区域的分界。在两个复杂度不同的游戏上验证有效，且在未见随机种子与阈值设定下边界行为稳定。

**Abstract:** Software testing often relies on assumptions such as reproducible executions and stable correctness criteria.  
However, many modern software systems exhibit non-deterministic executions and large behavior spaces, making exhaustive exploration impractical and single-run judgments unreliable.  
These characteristics make it difficult to identify where acceptable behavior ends and problematic behavior begins.  
Competitive multiplayer games represent a challenging instance of such systems, where balance must be maintained so that no single strategy dominates.  
Even small parameter changes can trigger abrupt balance disruption, yet detecting such failures requires repeated simulations under non-deterministic outcomes and high-dimensional parameter spaces.  
In this paper, we formulate game balance regression testing as a boundary-discovery problem under a finite simulation budget.  
The objective is to efficiently identify inputs near the boundary that separates balanced and unbalanced regions.  
To address this problem, we propose BBExplorer, which combines multi-directional candidate generation, budget-aware two-stage screening, and adaptive step-size shrinkage for boundary refinement.  
Experimental results on two games with different levels of complexity show that the approach is strong in low-dimensional settings and remains effective in higher-dimensional ones.  
It also exhibits stable boundary behavior across unseen random seeds and threshold settings.  
These results indicate that BBExplorer is effective for practical balance regression testing and, more broadly, for boundary-oriented testing in non-deterministic, budget-constrained systems.


## 40. WiDepFuzz: Finding Wi-Fi Protocol Bugs in Mobile Hotspot via Field Dependency Model

**Authors:** Yuanliang Chen (Renmin University of China, China), Fuchen Ma (Tsinghua University, China), Taotao Gu (Tsinghua University, China), Yu Jiang (Tsinghua University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837483

**中文总结:** 提出 WiDepFuzz，依 IEEE 802.11 构建字段依赖模型 FDModel 并做依赖组合引导 fuzz，配合活跃度与依赖检测器；在六款主流手机热点相对 Peach、OwFuzz 等 SOTA 多发现 15 个 bug、平均提速 37%，共 20 个新缺陷。

**Abstract:** Wi-Fi is a widely used wireless protocol, and mobile hotspot functionality has become essential for on-the-go connectivity. Bugs in the hotspot protocol stack can cause crashes, performance degradation, and semantic inconsistencies. Fuzzing is a promising technique for detecting such vulnerabilities. However, existing fuzzers typically test by modeling protocol inputs but ignore some critical dependencies among Wi-Fi fields, leading to inefficient testing. In this work, we present WiDepFuzz, a fuzzing framework designed to detect bugs in Mobile Hotspot implementations by modeling field dependencies in the Wi-Fi protocol. First, WiDepFuzz automatically identifies the semantic dependencies among Wi-Fi fields based on the IEEE 802.11 standard and constructs a Field Dependency Model (FDModel) to characterize various direct and indirect dependencies. Second, leveraging the FDModel, WiDepFuzz utilizes dependency-combination guided fuzzing to constantly generate Wi-Fi test frames that efficiently explore deep paths and trigger hidden bugs. Finally, we propose liveness and dependency detectors that enable real-time monitoring to identify abnormal states and uncover potential bugs in mobile hotspots. We implemented WiDepFuzz and evaluated it in six widely used mobile hotspots, covering major smartphone manufacturers, including Samsung, Xiaomi, OPPO, Honor, Huawei, and Nokia. Compared to SOTA Wi-Fi fuzzers like Peach, OwFuzz, wpaspy, and Greyhound, WiDepFuzz detects 15 more bugs and improves bug detection speed by 37% on average. In total, it uncovered 20 new bugs.

