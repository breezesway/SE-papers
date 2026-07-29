# ISSTA 2026 Research Track — Debugging and Fault Diagnosis

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 13

## 1. Automated Classification, Root Cause Analysis, and Repair Recommendations for Failed Mobile Testing by Specialized LLM

**Authors:** Chun Li (Nanjing University), Fei Wang (Nanjing University), Minxue Pan (Nanjing University), Zhong Li (Nanjing University), Mengliang Zeng (OPPO), Bin Zhang (OPPO), Xuejiao Yu (OPPO), Boyun Wang (OPPO), Kaijian Hua (OPPO), Xuandong Li (Nanjing University)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 提出面向移动测试失败分析的专用 LLM 训练框架 AnaDroid，通过双向预训练与偏好优化注入领域知识。在 28.4 万条工业失败测试上优于四个基线，部署一个月为 78% 失败用例提供根因、81% 提供修复建议。

**Abstract:** Engineers utilize test scripts to conduct testing on mobile applications to ensure software reliability. In industrial settings, failures in mobile application testing stem not only from faults in the program or scripts but also from other aspects, such as the testing environment, making it challenging to apply existing automated analysis methods in such settings. Furthermore, mobile testing in industrial contexts generates a large volume of artifacts, such as screenshots and logs, and involves diverse device models, varied test environments, and complex functionalities. All these factors make the manual analysis of failed mobile tests a process that is typically time-consuming, costly, and labor-intensive. Large language models (LLMs) with strong logical reasoning capabilities offer a novel perspective for automated analysis of failed mobile tests. However, due to their limited knowledge of mobile testing, general LLMs can only achieve sub-optimal effectiveness in these tasks. To address these challenges, we propose AnaDroid, a novel LLM training framework specifically tailored for analyzing failed mobile tests. AnaDroid performs feature preprocessing for failed mobile tests and trains the large language model through two novel, tailored training procedures. Specifically, AnaDroid first leverages bidirectional pre-training to instill the domain-specific knowledge and reasoning capabilities required for failed test analysis into the model. AnaDroid further employs preference optimization to enhance the model’s capacity to capture critical information within the input context, thereby further improving its analytical effectiveness. Through extensive evaluations across six open-source LLMs of diverse architectures and scales on a large-scale industrial dataset of 284k failed mobile testing scripts, AnaDroid outperformed all 4 baselines across three analysis tasks. Furthermore, during a month-long deployment within a global company’s testing system, \tool demonstrated its practical utility by successfully providing root cause and repair recommendations for 78% and 81% of the 11,304 failed tests, respectively.


## 2. Branch-Level Fault Localization in ADS Planning via Temporal Coverage Analysis

**Authors:** Sangmin Woo (KAIST, South Korea), Dohyun Kim (KAIST), Donghwan Shin (University of Sheffield), Yongdae Kim (KAIST)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 针对 ADS 规划模块失败，提出基于帧级时序覆盖分析的分支级故障定位方法，先定位可疑帧再排序候选分支。在 221 个 Apollo 可复现规划失败上显著减少需检查的分支数量。

**Abstract:** Planning failures in Automated Driving Systems (ADS) are increasingly detected through simulation-based testing, yet localizing their root causes within planning code remains a major challenge. Planning modules execute complex rule-based decision logic over hundreds of frames in a closed-loop interaction with the environment, where faults trigger observable failures only after temporal gaps and under specific execution contexts. These characteristics make traditional spectrum-based fault localization ineffective, as faulty behavior is obscured by execution-level coverage aggregation and limited test diversity. In this paper, we study the problem of debugging planning failures and present a temporal coverage analysis approach for localizing faults in rule-based planning modules. Our key insight is that, while execution-aggregated coverage masks fault behavior, frame-level execution dynamics reveal distinctive temporal signatures that indicate when and how faulty branches activate. Leveraging this insight, our approach first identifies a suspicious frame using planning semantics, and then ranks candidate branches by analyzing their execution behavior within a localized temporal window. We evaluate our approach on 221 reproducible planning failures drawn from a publicly available Apollo planning failure dataset. Our results show that temporal coverage analysis enables accurate suspicious-frame identification and substantially reduces branch inspection effort compared to baseline heuristics, effectively localizing faults from a single failing execution. We further analyze failure cases that lack observable execution signals to clarify the fundamental limits of execution-based localization. Overall, this work demonstrates that temporal execution analysis provides a practical and effective foundation for debugging planning failures in rule-based ADS planning modules.


## 3. ConFL: Explainable Concurrent Fault Localization via Hierarchy-Guided LLM Reasoning

**Authors:** Shuai Shao (University of Connecticut), Dingbang Wang (University of Connecticut), Yiming Zeng (University of Connecticut), Tingting Yu (University of Connecticut)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** ConFL 构建并发知识库并用层次化 LLM 检索从组件到跨线程交互上下文逐步缩小定位范围，配合交互级 DSL 编码共享资源访问模式。在八个 Java 项目的真实并发 bug 上 MRR 达 0.503，显著优于 IR 与 LLM 基线。

**Abstract:** Localizing concurrent bugs from bug reports alone is challenging due to incomplete information, misleading program-entity mentions, and complex cross-thread interactions, causing existing LLM-based approaches to suffer from unstable reasoning and limited explainability. We propose ConFL, an explainable concurrent fault localization framework that augments LLM reasoning with structured concurrency knowledge. ConFL constructs a Concurrent Knowledge Base (CKB) from source code and performs LLM-guided hierarchical retrieval to progressively narrow the search space from components to interaction-level concurrency contexts. An interaction-level DSL explicitly encodes cross-thread interactions over shared resources, enabling focused reasoning without traversing deep call chains. Experiments on real-world concurrent bugs from eight large-scale Java projects show that ConFL significantly outperforms state-of-the-art IR-based and LLM-based baselines, achieving an MRR of 0.503 and a MAP of 0.486, while remaining robust to noisy bug reports, unseen bugs, and different LLM backbones.


## 4. E2WR: An Effective and Efficient Reduction Framework for WebAssembly Binaries

**Authors:** Shiyao Zhou (The Hong Kong Polytechnic University), Ningyu He (Hong Kong Polytechnic University, Hong Kong SAR China), David Lo (Singapore Management University), Xiapu Luo (Hong Kong Polytechnic University)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** E²WR 针对 WebAssembly 二进制提出两阶段函数内指令缩减与非函数定义静态分析+差分调试联合削减策略，在保留 bug 触发能力的同时大幅缩小体积。输出二进制较 Wasm-Shrink 小 95.4%，缩减速度快 11.1 倍。

**Abstract:** WebAssembly (Wasm) is a prominent programming language enabling high-performance execution across diverse computing environments. However, bugs in Wasm runtimes, which execute Wasm binaries, can lead to severe security breaches and system failures. Manually debugging Wasm binaries that trigger such runtime bugs is exceedingly difficult due to their poor human readability, stemming from low-level stack-based instructions, complex control flow structures, and extraordinary length, often containing millions of instructions. Thus, there is a critical need for automated reduction techniques that minimize Wasm binaries while preserving the ability to trigger the original bug. However, existing reducers often suffer from significant limitations in effectiveness and efficiency: language-agnostic reducers frequently generate invalid variants without Wasm validation awareness, while Wasm-specific reducers still lack efficient delta-debugging-style intra-function instruction-sequence reduction and reduce non-function definitions inefficiently. To address these challenges, we propose E$^2$WR, an effective and efficient reduction framework for Wasm binaries. E$^2$WR introduces a two-stage approach for intra-function instruction-sequence reduction, consisting of operand-dependency guided instruction reduction and combinational redundancy elimination to enable efficient delta debugging while avoiding unnecessary padding instructions, and a non-function-oriented reduction approach that combines static analysis with delta-debugging-guided trials to remove property-irrelevant non-function definitions efficiently. Compared with Wasm-Shrink and Wasm-Reduce, E$^2$WR produces binaries that are 95.4% and 63.9% smaller, respectively, and achieves reduction speed improvement of 11.1$\times$ and 5.1$\times$, respectively.


## 5. Enhancing LLM-based Bug Reproduction via Code Entity Retrieval and Test Case Repair

**Authors:** Hao Ding (Beijing Institute of Technology), Yanjie Jiang (Tianjin University), Yuxia Zhang (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** LTER 从 bug 报告检索细粒度代码实体作为 LLM 上下文，并以编译错误反馈驱动的动态修复循环补全缺失依赖。Defects4J 上复现成功率达 47.1%，Top-1 候选命中率 39.9%，在 GHRB 新 bug 上亦表现稳健。

**Abstract:** Automated bug reproduction from bug reports is a critical yet challenging step in software debugging. While LLM-based bug reproduction shows promise, its effectiveness is often hampered by insufficient contextual awareness of the relevant codebase and a tendency to produce invalid test cases. To address these limitations, we propose a novel approach, called LTER, that enhances LLM-based bug reproduction through fine-grained code entity retrieval and a feedback-driven dynamic repair loop. LTER first identifies specific code entities within bug reports to automatically extract precise contexts, including class definitions, constructors, and method logic. The extracted contexts are then used to guide the LLM in generating reproduced test cases. To further ensure executability, LTER employs an iterative repair mechanism to resolve complex dependencies. Specifically, upon injecting a generated test case into the project, if a compilation failure occurs, the framework forwards the error messages to the LLM for an initial repair. Should this initial repair fail, it empowers the LLM to analyze diagnostic messages to recognize missing context and retrieve indispensable dependencies, subsequently regenerating the test case with the supplemented data. Finally, LTER employs a hybrid cascade ranking strategy to accurately select the most effective reproduction test case from the generated candidates. The experimental results on the widely-used Defects4J benchmark show that LTER substantially outperforms the best performance in automated bug reproduction, increasing the reproduction success rate to 47.1% with successfully identifying a valid reproduction test as the top candidate in 39.9% of the cases. Furthermore, LTER demonstrates strong generalization capability, delivering robust performance on the GHRB dataset containing recent bugs previously unseen by the LLM.


## 6. Gleaner: A Semantically-Rich and Efficient Online Sampler for Microservice Diagnostics

**Authors:** Yifan Yang, Aoyang Fang (Chinese University of Hong Kong, Shenzhen), Songhan Zhang (The Chinese University of Hong Kong, Shenzhen), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 提出 Gleaner 在线 tail-sampling，以 bag-of-edges 加日志语义替代图分析实现高效 trace 分组；1% 采样率下 RCA 准确率较次优采样器提升 42–107%。

**Abstract:** Distributed tracing in microservices is critical for diagnostics but generates overwhelming data volumes, necessitating intelligent sampling. To maximize fidelity, state-of-the-art (SOTA) tail-based samplers analyze complete (or even log-enriched) traces by modeling them as graphs. However, this reliance on computationally expensive graph analysis creates a performance bottleneck that prohibits their use in online settings.

To this end, we propose Gleaner, an online tail-sampling framework that breaks this trade-off. It is founded on the key insight that explicit graph structures are unnecessary for high-fidelity trace grouping. Instead, Gleaner represents each trace as a “bag-of-edges” augmented with log semantics, replacing slow graph algorithms with highly efficient set-based operations. It also employs an alarm-driven quota and a diversity-preserving strategy to prioritize anomalous and rare traces for downstream Root Cause Analysis (RCA). Experimentally, Gleaner processes traces at 0.74ms each, improving Trace Pattern Coverage by up to 128.7% and Shannon Entropy by up to 32.9% over baselines. At just a 1% sampling rate, Gleaner improves RCA accuracy by 42%-107% over the next-best sampler. Moreover, RCA on Gleaner’s sampled data is more accurate than with the entire, unsampled dataset. This result reframes intelligent sampling from a data reduction technique to a powerful signal enhancement paradigm for automated operations.


## 7. Integrating Multiple Features for Weakly-Supervised False-Passing Products Detection in Software Product Lines

**Authors:** Tao Zhang (Chongqing University, China), Yan Lei (Chongqing University), Haoran Xia (Chongqing University, China), Huan Xie (Chongqing University), Chunyan Liu (Chongqing University)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 提出 PULP 弱监督方法检测 SPL 中 false-passing products，融合五类执行特征无需完整标签；在 823 个 buggy 版本上准确率最高 90.33%，可提升后续 fault localization。

**Abstract:** Software Product Lines (SPL) enable the efficient development of configurable systems through feature modularization. However, the inherent configurability of software introduces significant challenges for fault localization within these systems. A key challenge among these is the problem of false-passing products, configurable products that contain faulty code yet coincidentally pass all their associated tests, thereby masking faults and misleading diagnosis efforts. To mitigate the negative impact of false-passing products. Supervised detection approaches are often impractical due to their reliance on complete labels, which are unavailable during early testing phases. To address this, we propose PULP, a label-agnostic detection approach that exploits the execution similarity between failing and false-passing products. PULP extracts five categories of features and employs a weakly-supervised learning algorithm to identify false-passing products without pre-labeled data. Evaluated on 823 buggy versions from six real-world SPL systems, PULP achieves superior detection performance, with best accuracy of 90.33% and precision of 94.93% for false-passing products and consistently enhances fault localization rankings after eliminating the negative impact of false-passing product. This method offers a practical tool for SPL testing and debugging in label-incomplete environments.


## 8. IssueExec: A Test-Driven Approach for Localizing Software Engineering Issues

**Authors:** Jiawei Liu (Shanghai Jiao Tong University), Yun Lin (Shanghai Jiao Tong University), Chenyan Liu (Shanghai Jiao Tong University; National University of Singapore), Yu Qian (Shanghai Jiao Tong University), Liu Yiming (Shanghai JiaoTong University; Shanghai Innovation Institute), Jiaxin Chang (Shanghai Jiao Tong University), Weinan Zhang (Shanghai Jiao Tong University; Shanghai Innovation Institute), Linpeng Huang (Shanghai Jiao Tong University)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 提出 IssueExec，以测试套件为可执行需求代理做 issue localization，经 domain-knowledge 测试表示与分层 trace 分析；SWE-bench Lite 上 Recall@1 较最强基线提升 41.57%。

**Abstract:** Issue localization, which identifies code locations requiring modification from issue descriptions, is a critical step in automated software maintenance. Existing approaches predominantly attempt to directly align issue descriptions with code elements, yet often struggle due to the inherent abstraction gap between the issue description and code implementation. Seeking alternative signals, our theoretical analysis suggests that test suites can serve as executable proxies for requirements, reducing localization uncertainty by 2.01 bits on average. A large-scale empirical study on 18 repositories validates this premise: existing tests cover 96.98% of ground-truth files, and the two-hop pathway yields stronger semantic connectivity than direct matching in 82.4% of cases. Despite their potential, leveraging tests for localization faces two key challenges: the semantic gap separating issue descriptions from test identifiers, and the substantial noise in execution traces from infrastructure code. To address these, we propose IssueExec, which bridges the semantic gap through domain-knowledge-enhanced test representations and filters noise via hierarchical trace analysis. Experiments on SWE-bench Lite show that IssueExec achieves state-of-the-art performance, improving function-level Recall@1 by 41.57% over the strongest baseline. When integrated into the Agentless pipeline, IssueExec resolves 17.72% more issues, demonstrating practical downstream benefits.


## 9. On the Feasibility of Deduplicating Compiler Bugs with Bisection

**Authors:** Xintong Zhou (University of Waterloo), Zhenyang Xu (University of Waterloo), Yongqiang Tian (Monash University, Hong Kong SAR China), Chengnian Sun (University of Waterloo)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** BugLens 以 bisection 定位失败引入提交为主、结合触发优化识别为辅，对编译器随机测试产生的重复 bug 报告去重。在四个真实数据集上较 Tamer/D3 分别节省 26.98%/9.64% 人工工作量。

**Abstract:** Random testing has proven to be an effective technique for compiler validation. However, the debugging of bugs identified through random testing presents a significant challenge due to the frequent occurrence of duplicate test programs that expose identical compiler bugs. The process to identify duplicates is a practical research problem known as bug deduplication. Prior methodologies for compiler bug deduplication primarily rely on program analysis to extract bug-related features for duplicate identification, which can result in substantial computational overhead and limited generalizability. This paper investigates the feasibility of employing bisection, a standard debugging procedure largely overlooked in prior research on compiler bug deduplication, for this purpose. Our study demonstrates that the utilization of bisection to locate failure-inducing commits provides a valuable criterion for deduplication, albeit one that requires supplementary techniques for more accurate identification. Building on these results, we introduce BugLens, a novel deduplication method that primarily uses bisection, enhanced by the identification of bug-triggering optimizations to minimize false negatives. Empirical evaluations conducted on four real-world datasets demonstrate that BugLens significantly outperforms the state-of-the-art analysis-based methodologies Tamer and D3 by saving an average of 26.98% and 9.64% human effort to identify the same number of distinct bugs. Given the inherent simplicity and generalizability of bisection, it presents a highly practical solution for compiler bug deduplication in real-world applications.


## 10. Poirot: Automatic Root Cause Analysis of Safety Violations in ADS Simulation Testing via Hypothetical Reasoning

**Authors:** You Lu (Fudan University), Dingji Wang (Fudan University), Kun Zhang (Fudan University), Bihuan Chen (Fudan University), Jiyan Zhang (Fudan University), Xin Peng (Fudan University)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** Poirot 对 ADS 仿真测试中的安全违规做两阶段根因分析：模块级用理想模块替换的假设推理定位故障模块，组件级用嫌疑引导搜索或因果分析精确定位。在 Apollo/Autoware 上模块级精度较 SOTA 提升 187.29%，组件级达 90.62%。

**Abstract:** With the rapid development of autonomous driving systems (ADSs), it has become critical to ensure their operational safety, leading to the widespread adoption of simulation testing. While existing scenario-based simulation testing approaches have demonstrated effectiveness in detecting safety violations, they often fall short in providing insight into the underlying causes of these violations, which is an essential capability for improving the safety and reliability of ADSs. To address this limitation, we propose a two-phase novel framework, Poirot, for root cause analysis in simulation testing via hypothetical reasoning. Given a reproducible violation scenario, in the module-level analysis phase, Poirot replays the violation scenario and identifies the faulty module by iteratively replacing an actual module with an idealized module and checking whether the violation persists. In the component-level analysis phase, depending on the identified faulty module, Poirot further applies either hypothetical reasoning with a suspicion-guided search strategy or causal analysis to narrow the fault space and pinpoint the faulty component. We evaluate Poirot with two ADSs, e.g., Apollo and Autoware, on a comprehensive benchmark that includes a total of 80 real and injected faults along with their triggering scenarios. Compared with the state-of-the-art root cause analysis approaches, e.g., ACAV and Rocas, Poirot improves the module-level accuracy by 187.29% on average, and identifies the faulty components at a finer granularity, achieving component-level accuracy of 90.62%. Our ablation study shows that our suspicion-guided search strategy in Poirot efficiently reduces the exploration of the fault space by 58.77%, leading to a 65.41% reduction in the time for fault localization. Finally, applied to two scenario-based simulation testing methods, i.e., AvFuzzer and MoDitector, Poirot attributes 425 violation scenarios to 8 faults, cutting debugging time by 96.89% compared to manual analysis in practice.


## 11. Project-Scale Statement-Level Fault Localization via Multi-View Semantic Learning and Pairwise Reranking

**Authors:** Hongwei Yu (Beihang University), Xu Wang (Beihang University), Jian Zhang (Beihang University), Xiangxin Meng (Bytedance), lijiarui, Yang Liu (Nanyang Technological University), Chunming Hu (Beihang University)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** FaultScape 对 LLM 做多视图对比微调提取故障语义特征，融合谱与变异执行特征后以测试引导的 pairwise reranking 做项目级语句故障定位。Defects4J 上 Top-1/3/5 分别定位 112/171/196 个 bug，优于 DL 与 LLM 基线。

**Abstract:** Statement-level fault localization (FL) is critical for effective software debugging, as it enables developers to precisely identify faulty lines of code. While traditional spectrum-based, mutation-based, and deep learning-based FL techniques have achieved notable progress, they remain limited in modeling rich fault semantics. Recent advances in large language models (LLMs) offer new opportunities for FL due to their strong capacity for semantic understanding and reasoning over bugs. However, existing LLM-based FL approaches largely treat fault localization as isolated, code-centric prediction, limiting their ability to perform the holistic fault reasoning required for precise statement-level localization.

In this paper, we propose FaultScape, a novel LLM-based framework for project-scale, statement-level FL that formulates FL as a multi-view semantic learning and reasoning problem. FaultScape addresses the limitations of existing approaches through three key components. First, we introduce a joint contrastive fine-tuning strategy that trains LLMs on large-scale bug-fix data to explicitly learn fault semantics from multiple complementary views. View-specific fault semantics, including fault type, root cause, and repair intent, are learned via supervised binary classification, while cross-view semantic consistency is enforced through contrastive learning. These two objectives are jointly optimized within a unified training loss. The fine-tuned models extract multi-view fault likelihoods as semantic features for each suspicious statement. Second, we adopt a dynamic feature integration module that combines these semantic features with spectrum-based and mutation-based execution features, producing an initial suspiciousness statement ranking. Third, we design a test-guided pairwise re-ranking strategy based on LLM that explicitly compares highly suspicious statements among candidates under failing-test contexts. By estimating relative fault likelihoods through pairwise comparison rather than independent scoring, the model produces a refined project-scale ranking.

We evaluate FaultScape on Defects4J v1.2.0, where it localizes 112/171/196 bugs at Top-1/3/5 out of 395, outperforming state-of-the-art DL-based and LLM-based baselines. On leakage-free benchmarks, FaultScape further localizes 11/18/20 bugs at Top-1/3/5 on ConDefects (31 bugs) and 12/21/22 bugs on GHRB (34 bugs), demonstrating strong generalization to unseen projects. These results show that combining multi-view fault semantics with contrastive, failure-guided reasoning substantially advances the effectiveness and robustness of statement-level fault localization.


## 12. Signal Denoising based Kill Matrix Refinement for Mutation-based Fault Localization

**Authors:** Hengyuan Liu (Beijing University of Chemical Technology), Xia Song (Beijing University of Chemical Technology), Yong Liu (Beijing University of Chemical Technology), Zheng Li (Beijing University of Chemical Technology)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 提出 DKMR，将 MBFL kill matrix 视作含噪信号，经混合矩阵增强与频域滤波去噪后计算可疑度。Defects4J 上 Top-1 定位 129 个缺陷，优于 BLMu（85）与 Delta4Ms（103），额外开销仅 0.11 秒。

**Abstract:** Software debugging is a critical and time-consuming aspect of software development, with fault localization being a fundamental step that significantly impacts debugging efficiency. Mutation-Based Fault Localization (MBFL) has gained prominence due to its robust theoretical foundations and fine-grained analysis capabilities. However, recent studies have identified a critical challenge: noise phenomena, specifically the false kill relationships between mutants and tests, which significantly degrade localization effectiveness. While several approaches have been proposed to rectify the final localization results, they do not directly address the underlying noise. In this paper, we propose a novel approach to refine the kill matrix, a core data structure capturing mutant-test relationships in MBFL, by treating it as a signal that contains both meaningful fault-related patterns and high-frequency noise. Inspired by signal processing theory, we introduce DKMR (Denoising-based Kill Matrix Refinement), which employs two key stages: (1) signal enhancement through hybrid matrix construction to improve the signal-to-noise ratio for better denoising, and (2) signal denoising via frequency domain filtering to suppress noise while preserving fault-related patterns. Building on this foundation, we develop MBFL-DKMR, a fault localization framework that utilizes the refined matrix with continuous values for suspiciousness calculation. Our evaluation on Defects4J v2.0.0 demonstrates that MBFL-DKMR effectively mitigates the noise and outperforms the state-of-the-art MBFL techniques. Specifically, MBFL-DKMR achieves 129 faults localized at Top-1 compared to 85 for BLMu and 103 for Delta4Ms, with negligible additional computational overhead (0.11 seconds, 0.001% of total time). This work highlights the potential of signal processing techniques to enhance the effectiveness of MBFL by refining the kill matrix.


## 13. TracePilot: Self-verifiable Framework for Decentralized Applications Fault Localization across Transactions

**Authors:** Xuanyu Zhu (Sun Yat-sen University), Zhiying Wu (Sun Yat-sen University), Tao Wang (Sun Yat-sen University), Ying Yan (Ant Digital Technologies, Ant Group), Wei Zhou (Ant Digital Technologies, Ant Group), Jiajing Wu (Sun Yat-sen University), Zigui Jiang (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** TracePilot 分两阶段从交易序列蒸馏全局故障洞察并聚焦追踪探索，提出可验证补丁的 DApp 跨交易缺陷定位方法。在 149 个真实案例上 Top-1 Recall 71.14%，比 SOTA 高 128.9%。

**Abstract:** Decentralized Applications (DApps) serve as a critical technical underpinning for business logic and user interaction within the blockchain-powered Web3 ecosystem. However, DApps are prone to faults, and localizing these faults within their intricate and often interconnected logic is a particularly time-consuming process, frequently taking tens of hours and leading to substantial economic losses for developers. Existing state-of- the-art DApp fault localization methods, e.g., FaultSeeker, cannot capture cross-transaction fault logic and produce verifiable diagnostic reports. Therefore, the security experts have to spend substantial time manually verifying results and devising fixes. In this paper, we present TracePilot, an large language models(LLMs)-based framework that automates DApp fault localization in two phases: distilling global fault insights from transaction sequences and then performing focused trace exploration to isolate the faulty logic. Crucially, we propose a novel patch verification technique, which allows for verifying the correctness of DApp fault localization reports, rather than relying on expert verification. Evaluated on a dataset of 149 real-world cases, TracePilot achieves a 71.14% Top-1 Recall, 128.9% higher than the state-of-the-art methods. Moreover, to facilitate further research, our code and dataset are publicly available online: https://anonymous.4open.science/r/TracePilot-F8A6/ .

