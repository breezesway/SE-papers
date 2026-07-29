# FSE 2026 Research Track — Debugging and Fault Diagnosis

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 15 papers

## 1. A Grounded Theory of Debugging in Professional Software Engineering Practice

**Authors:** Haolin Li (University of California San Diego), Michael Coblenz (University of California, San Diego)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797077

**中文总结:** 基于扎根理论观察 7 名专业开发者与 5 名直播写码者在真实代码库中完成 17 项调试任务，提出专业调试是迭代更新系统心智模型的诊断过程，开发者在导航与执行策略、前向/后向追踪间切换，并辅以外部资源；为调试工具设计与软件工程教育提供人本视角理论。

**Abstract:** Debugging is a central yet complex activity in software engineering. Prior studies have documented debugging strategies and tool usage, but little theory explains how experienced developers reason about bugs in large, real-world codebases. We conducted a qualitative study using a grounded theory approach. We observed seven professional developers and five professional live-coding streamers working on 17 debugging tasks in their own codebases, capturing diverse contexts of debugging. We theorize debugging as a structured, iterative diagnostic process in which programmers update a mental model of the system to guide information gathering. Developers gather information by alternating between navigation and execution strategies, employing forward and backward tracing modes of reasoning and adapting these approaches according to codebase context, complexity, and familiarity. Developers also gather external resources to complement code-based evidence, with their experience enabling them to systematically construct a mental model. We contribute a grounded theory of professional debugging that surfaces the human-centered dimensions of the practice, with implications for tool design and software engineering education.

## 2. CrossFit: Demystifying VM Callback Bugs in Interpreters

**Authors:** Chibin Zhang (EPFL), Qiang Liu (EPFL), Mathias Payer (EPFL)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808111

**中文总结:** 提出 CrossFit，经上下文链接分析关联脚本侧回调与原生调用点，再定向模糊生成带副作用的 PoC 以触发解释器回调缺陷；相对已有工具 callsite 覆盖最高提升 12.04%，并在 PHP/Python/Ruby 中发现 20 个新缺陷。

**Abstract:** Scripting languages like Python, Ruby, and PHP are integral to modern software development. Despite security measures like memory safety and sandboxing, vulnerabilities within these engines can lead to critical issues such as remote code execution or sandbox escapes. A particularly pervasive class of vulnerabilities is callback bugs, which occur when user-defined callbacks violate runtime invariants, such as freeing an internal object still in use or modifying a data structure during traversal. These violations can result in severe consequences, including use-after-free, null-pointer dereferences, and type confusion, often leading to crashes, memory corruption, or even exploitable vulnerabilities. Detecting callback bugs remains challenging due to a lack of general understanding, as they have not been formally characterized or systematically studied. As such, existing tools lack the ability to (1) establish clear links between script-side callbacks and their native-side invokers, and (2) generate scripts that systematically satisfy preconditions required to trigger these bugs. We propose CrossFit, a novel 2-tier approach combining static analysis and targeted fuzzing to systemati- cally detect callback bugs. CrossFit first establishes links between script-side callbacks and their native-side invokers through context link analysis, enabling targeted exploration of high-risk code paths. It then generates proof-of-concept scripts with custom classes and magic methods, introducing side-effect operations to violate runtime invariants. Our evaluation shows that CrossFit effectively outperforms existing tools by up to 12.04% in terms of callsite coverage (i.e., potential sites where callback bugs may occur). We also identified 20 new bugs in PHP, Python, and Ruby, many of which are severe memory corruptions. Moreover, we provide a comprehensive benchmark totaling 150 proof-of-concepts to improve interpreter security

## 3. Debugging Engine Enhanced by Prior Knowledge: Can We Teach LLM How to Debug?

**Authors:** Kunyi Li (Zhejiang University, China), Sai Wu (Zhejiang University), Xiu Tang (Zhejiang University), Chang Yao (Zhejiang University), Songhao Bu (Zhejiang University), Quanqing Xu (OceanBase, Ant Group), Gang Chen (Zhejiang University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797110

**中文总结:** 提出 DeepK，从大规模缺陷修复语料中提炼并验证可复用调试知识，以可解释推理轨迹指导 LLM 自动程序修复；在 ACPR/Atcoder 上结合 GPT-4o 与 DeepSeek-v3 持续优于现有 APR 系统。

**Abstract:** Automated Program Repair (APR) powered by Large Language Models (LLMs) has shown strong potential for improving software reliability. However, existing LLM-based APR approaches underutilize the rich debugging knowledge latent in large-scale bug-fix corpora. Prior work has primarily advanced APR through multi-agent coordination, prompt engineering, task decomposition, or model training. While effective to some extent, these methods rely heavily on the implicit reasoning capacity of LLMs, without explicitly modeling the debugging knowledge that underlies successful program repair. We present DeepK, a novel framework that systematically extracts, validates, and reuses debugging knowledge to guide LLMs in APR. Rather than treating historical bug-fix pairs solely as contextual exemplars, DeepK distills them into a structured knowledge base of verified debugging knowledge. This knowledge base can be seamlessly integrated into diverse APR pipelines, providing interpretable reasoning traces and step-wise repair strategies that enhance the repair performance.

We evaluate DeepK on multiple benchmarks (ACPR, Atcoder) using both GPT-4o and DeepSeek-v3. Results show that DeepK consistently surpasses state-of-the-art APR systems in repair accuracy. Ablation studies confirm the importance of edit description generation, multi-perspective retrieval, and two-fold debugging knowledge. Varying the number of retrieved entries further highlights the trade-off between informativeness and noise. These findings emphasize the essential contribution of explicit debugging knowledge in advancing LLM-based APR and establish DeepK as an extensible framework for building more reliable repair systems.

## 4. Empowering Autonomous Debugging Agents with Efficient Dynamic Analysis

**Authors:** Jiahong Xiang (Southern University of Science and Technology), Xiaoyang Xu (Southern University of Science and Technology), Xiaopan Chu (Southern University of Science and Technology), Hongliang Tian (Ant Group), Yuqun Zhang (Southern University of Science and Technology)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797126

**中文总结:** 提出 Agent-centric Debugging Interface（ADI），以函数级交互与 Frame Lifetime Trace 替代低效逐行调试，降低自主修复智能体成本；在 SWE-bench Verified 上使基础智能体以约 $1.28/任务解决 63.8% 任务，并可作为插件为 SOTA 智能体带来 6.2%–18.5% 提升。

**Abstract:** Autonomous agents for automated program repair represent a promising frontier in software engineering, yet their effectiveness is often hindered by reliance on post-mortem, coarse-grained execution feedback. While integrating traditional interactive debuggers seems a natural solution, their low-level, line-by-line interaction paradigm turns to be cost-inefficient for LLM-based agents, leading to exhausted budgets and unproductive loops. To mitigate this, we introduce Agent-centric Debugging Interface (ADI), a novel agent-centric debugging interface designed for cost-efficient, end-to-end autonomous interaction. Specifically, Agent-centric Debugging Interface realizes a function-level interaction paradigm, powered by our Frame Lifetime Trace—a comprehensive data structure encapsulating a function’s stateful execution trace—and a set of high-level navigational commands. Our extensive evaluation on the SWE-bench benchmark demonstrates the effectiveness and efficiency of ADI. By simply equipping a basic agent with ADI, it successfully resolves 63.8% of the tasks on the SWE-bench Verified set, even slightly outperforming the highly-optimized and high-investment Claude-Tools agent, at an average cost of $1.28 per task with Claude-Sonnet-3.7. Furthermore, we demonstrate ADI’s generality by integrating it as a plug-and-play component into the existing SOTA agents, delivering consistent gains ranging from 6.2% to 18.5% on the resolved tasks. These results indicate that Agent-centric Debugging Interface could achieve a general and efficient enhancement for the existing autonomous agents.

## 5. EventADL: Open-Box Anomaly Detection and Localization Framework for Events in Cloud-Based Service Systems

**Authors:** Luan Pham (University of New South Wales, Australia), Victor Nicolet (Amazon), Joey Dodds (Amazon, Inc.), Hui Guan (Amazon Web Services, USA), Daniel Kroening (Amazon)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808186

**中文总结:** 提出 EventADL，首个面向云服务事件数据的开放箱异常检测与定位框架，学习语义/频率模式并用 Intervention Graph 做根因定位；在真实云系统上异常检测 F1≥90%，定位 top-3 准确率达 100%。

**Abstract:** Anomaly detection and localization (ADL) is critical for maintaining high reliability and availability in cloud-based systems. Recent ADL developments focus on metric and log data, leaving event data relatively unexplored. To address this gap, we propose EventADL, the first open-box ADL framework for events in cloud-based service systems. To motivate the design of our framework, we conduct a systematic analysis on 520 real-world incidents, and provide several important insights into how anomalies and their root causes manifest through event data. The EventADL framework has three phases: offline training, online anomaly detection, and anomaly localization. During the training phase, EventADL learns Event Semantic Patterns (ESPs) for pointwise anomaly detection and Event Frequency Patterns (EFPs) for frequency-based anomaly detection using unlabelled historical data. In the online anomaly detection phase, any data in the event stream that deviates significantly from these patterns is identified as anomalous. In the localization phase, EventADL constructs an Intervention Graph that models the relationships between recent interventions (i.e., system changes visible through events) and the detected anomalies for automatic root cause localization. The framework is designed to operate efficiently without labeled data , and to produce interpretable results. Our evaluation on three real cloud-based service systems and two real-world incidents, compared against ten state-of-the-art baselines, demonstrates that EventADL outperforms existing methods, achieving F1-scores of at least 90% for anomaly detection and 100% top-3 accuracy in anomaly localization.

## 6. GraphLocator: Graph-guided Causal Reasoning for Issue Localization

**Authors:** Wei Liu (Peking University), Chao Peng (Tencent), Pengfei Gao (ByteDance), Aofan Liu (Peking University), Wei Zhang (Peking University), Haiyan Zhao (Peking University), Zhi Jin (Peking University, Wuhan University)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797079

**中文总结:** 提出 GraphLocator，通过因果结构发现与动态问题拆解构建因果问题图（CIG），缓解症状–根因与一对多实体错配；相对基线函数级召回/精度平均提升约 19.5%/11.9%，并将下游修复性能最高相对提升 28.74%。

**Abstract:** The issue localization task aims to identify the locations in a software repository that requires modification given a natural language issue description. This task is fundamental yet challenging in automated software engineering due to the semantic gap between issue description and source code implementation. This gap manifests as two mismatches: (1) \emph{symptom–to-cause mismatches}, where descriptions do not explicitly reveal underlying root causes; (2) \emph{one-to-many mismatches}, where a single issue corresponds to multiple interdependent code entities. To address these two mismatches, we propose \emph{GraphLocator}, an LLM-based approach that mitigates symptom–to-cause mismatches through \emph{causal structure discovering} and resolves one-to-many mismatches via \emph{dynamic issue disentangling}. The key artifact of \emph{GraphLocator} is the \emph{causal issue graph} (CIG), in which vertices represent discovered sub-issues along with their associated code entities, and edges encode the causal dependencies between them. The workflow of \emph{GraphLocator} consists of two phases: \emph{symptom vertices locating} and \emph{dynamic CIG discovering}; it first identifies symptom locations on the repository graph, then dynamically expands the CIG by iteratively reasoning over neighboring vertices, discovering new sub-issues and updating causal dependencies. Experiments on three real-world Python and Java datasets demonstrates the effectiveness of \emph{GraphLocator}: (1) Compared with baselines, \emph{GraphLocator} achieves more accurate localization with average improvements of +19.49% in function-level recall and +11.89% in precision with acceptable overhead. (2) \emph{GraphLocator} outperforms baselines on both symptom-to-cause and one-to-many mismatch scenarios, achieving recall improvement of +16.44% and +19.18%, precision improvement of +7.78% and +13.23%, respectively. (3) The disentangled causal structure CIG generated by \emph{GraphLocator} yields the highest relative improvement, resulting in a 28.74% increase in performance on the downstream issue-resolving task.

## 7. GREClue: Failure Indexing with Graph-based Failure Representation and Entropy-based Deep Clustering

**Authors:** Zhenyu Yang (Shandong University), Zhongxing Yu (Shandong University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808118

**中文总结:** 提出 GREClue，用失败语义图（FSG）刻画失败语义与运行信息，并结合无需预设中心的熵驱动深度聚类做失败索引；相对 SOTA 在故障数估计与聚类效果上提升 10%–41%，并有效支撑并行调试。

**Abstract:** Failure indexing aims to group multiple failures according to their root causes and is an essential step in parallel debugging. Failure indexing consists mainly of two steps: failure representation and failure clustering. While many research efforts have been devoted to these two steps, serious issues still exist. For failure representation, existing works use coverage or program memory information, which unfortunately can not capture deep failure semantic. For failure clustering, advanced failure indexing methods use clustering algorithms with preset cluster centers, but this kind of clustering algorithm can handle spherical clusters well but performs poorly when handling clusters of other shapes. To address these issues, this paper proposes GREClue, a novel failure indexing approach with Graph-based failure Representation and Entropy-based deep Clustering. GREClue overcomes the issues in order. For failure representation, GREClue designs the failure semantic graph (FSG), a new graph representation that effectively contains semantic information and runtime information of failures. Based on FSG, GREClue further consists of an entropy-based deep clustering component, which can accurately cluster failed tests without presetting cluster centers. An extensive evaluation of GREClue shows that compared to the state-of-the-art failure indexing method, GREClue improves both the performance of estimating the number of faults and the clustering effectiveness by 10% to 41%. Moreover, it has also been shown that GREClue can effectively facilitate parallel debugging.

## 8. MetaRCA: A Generalizable Root Cause Analysis Framework for Cloud-Native Systems Powered by Meta Causal Knowledge

**Authors:** Shuai Liang (Sun Yat-sen University; China Unicom Software Research Institute: Beijing, CN), Pengfei Chen (Sun Yat-sen University), Bozhe Tian (China Unicom Software Research Institute: Beijing, CN), Gou Tan (School of Systems Science and Engineering, Sun Yat-sen University, Guangzhou, China), Maohong Xu (China Unicom Software Research Institute: Beijing, CN), Youjun Qu (China Unicom Software Research Institute: Beijing, CN), Yahui Zhao (China Unicom Software Research Institute: Beijing, CN), Yiduo Shang (China Unicom Software Research Institute: Beijing, CN), Chongkang Tan (Individual Researcher)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797069

**中文总结:** 提出 MetaRCA，离线构建可复用的元数据级 Meta Causal Graph（融合 LLM、故障报告与可观测数据），在线按上下文实例化并剪枝因果边做根因定位；在公开与生产故障上服务级/指标级准确率分别超最强基线 29 与 48 个百分点，跨系统准确率保持逾 80%。

**Abstract:** The dynamics and complexity of cloud-native systems present significant challenges for Root Cause Analysis (RCA). While causality-based RCA methods have shown significant progress in recent years, their practical adoption is fundamentally limited by three intertwined challenges: poor scalability against system complexity, brittle generalization across different system topologies, and inadequate integration of domain knowledge. These limitations create a vicious cycle, hindering the development of robust and efficient RCA solutions. This paper introduces MetaRCA, a generalizable RCA framework for cloud-native systems. MetaRCA first constructs a Meta Causal Graph (MCG) offline, a reusable knowledge base defined at the metadata level. To build the MCG, we propose an evidence-driven algorithm that systematically fuses knowledge from Large Language Models (LLMs), historical fault reports, and observability data. When a fault occurs, MetaRCA performs a lightweight online inference by dynamically instantiating the MCG into a localized graph based on the current context, and then leverages real-time data to weight and prune causal links for precise root cause localization. Evaluated on 252 public and 59 production failures, MetaRCA demonstrates state-of-the-art performance. It surpasses the strongest baseline by 29 percentage points in service-level and 48 percentage points in metric-level accuracy. This performance advantage widens as system complexity increases, with its overhead scaling near-linearly. Crucially, MetaRCA shows robust cross-system generalization, maintaining over 80% accuracy across diverse systems.

## 9. Rethinking the Evaluation of Microservice RCA with a Fault Propagation-Aware Benchmark

**Authors:** Aoyang Fang (Chinese University of Hong Kong, Shenzhen), Songhan Zhang (The Chinese University of Hong Kong, Shenzhen), Yifan Yang, Haotong Wu (The Chinese University of Hong Kong, Shenzhen), Junjielong Xu (The Chinese University of Hong Kong, Shenzhen), Xuyang Wang (The Chinese University of Hong Kong, Shenzhen), Rui Wang (The Chinese University of Hong Kong, Shenzhen), Manyi Wang (The Chinese University of Hong Kong, Shenzhen), Qisheng Lu (The Chinese University of Hong Kong, Shenzhen), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797100

**中文总结:** 揭示现有微服务根因分析基准过度简化，并提出故障传播感知的自动基准生成框架与含 1430 例的新数据集；11 个 SOTA 模型 Top@1 平均仅 0.21，暴露可扩展性与可观测性等瓶颈。

**Abstract:** While cloud-native microservice architectures have revolutionized software development, their inherent operational complexity makes failure Root Cause Analysis (RCA) a critical yet challenging task. Numerous data-driven RCA models have been proposed to address this challenge. However, we find that the benchmarks used to evaluate these models are often too simple to reflect real-world scenarios. Our preliminary study reveals that simple rule-based methods can achieve performance comparable to or even surpassing state-of-the-art (SOTA) models on four widely used public benchmarks. This finding suggests that the oversimplification of existing benchmarks might lead to an overestimation of the performance of RCA methods.

To further investigate the oversimplification issue, we conduct a systematic analysis of popular public RCA benchmarks, identifying key limitations in their fault infjection strategies, call graph structures, and telemetry signal patterns. Based on these insights, we propose an automated framework for generating more challenging and comprehensive benchmarks that include complex fault propagation scenarios. Our new dataset contains 1,430 validated failure cases from 9,152 fault injections, covering 25 fault types across 6 categories, dynamic workloads, and hierarchical ground-truth labels that map failures from services down to code-level causes. Crucially, to ensure the failure cases are relevant to IT operations, each case is validated to have a discernible impact on user-facing SLIs.

Our re-evaluation of 11 SOTA models on this new benchmark shows that they achieve low Top@1 accuracies, averaging 0.21 with the best-performing model reaching merely 0.37 and execution times escalating from seconds to hours. From this analysis, we identify three critical failure patterns common to current models: scalability issues, observability blind spots and modeling bottlenecks. Based on these findings, we provide actionable guidelines for future RCA research. We emphasize the need for robust algorithms and the co-development of challenging benchmarks. To facilitate further research, we publicly release our benchmark generation framework, the new dataset, and our implementations of the evaluated SOTA models.

## 10. Spectrum-based Failure Attribution for Multi-Agent Systems

**Authors:** Yu Ge (Nanjing University), Linna Xie (Nanjing University), Zhong Li (Nanjing University), Yu Pei (Hong Kong Polytechnic University), Tian Zhang (Nanjing University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797113

**中文总结:** 提出 FAMAS，首个面向多智能体系统的谱系式失败归因方法，通过轨迹重放抽象与定制可疑度公式估计各智能体动作责任；在 Who&When 基准上相对 12 个基线全面领先。

**Abstract:** Large Language Model Powered Multi-Agent Systems (MASs) are increasingly employed to automate complex real-world problems, such as programming and scientific discovery. Despite their promising, MASs are not without their flaws. However, failure attribution in MASs—pinpointing the specific agent actions responsible for failures—remains underexplored and labor-intensive, posing significant challenges for debugging and system improvement. To bridge this gap, we propose FAMAS, the first spectrum-based failure attribution approach for MASs, which operates through systematic trajectory replay and abstraction, followed by spectrum analysis. The core idea of FAMAS is to estimate, from variations across repeated MAS executions, the likelihood that each agent action is responsible for the failure. In particular, we propose a novel suspiciousness formula tailored to MASs, which integrates two key factor groups, namely the agent behavior group and the action behavior group, to account for the agent activation patterns and the action activation patterns within the execution trajectories of MASs. Through expensive evaluations against 12 baselines on the Who&When benchmark, FAMAS demonstrates superior performance by outperforming all the methods in comparison.

## 11. StepFly: Agentic Troubleshooting Guide Automation for Incident Diagnosis

**Authors:** Jiayi Mao (Tsinghua University), Liqun Li (Microsoft Research), Yanjie Gao (Microsoft Research), Zegang Peng (Tsinghua University), Shilin He (Microsoft Research), Chaoyun Zhang (Microsoft), Si Qin (Microsoft Research), Samia Khalid (Microsoft), Qingwei Lin (Microsoft), Saravan Rajmohan (Microsoft), Sitaram Lanka (Microsoft), Dongmei Zhang (Microsoft)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808143

**中文总结:** 提出 StepFly，面向运维排障指南（TSG）的端到端智能体框架，含 TSG Mentor 质量改进、离线 DAG/查询插件抽取与在线 DAG 调度并行执行；在真实 TSG/事故上 GPT-4.1 成功率约 94%，可并行 TSG 执行时间降低 32.9%–70.4%。

**Abstract:** Effective incident management in large-scale IT systems relies on troubleshooting guides (TSGs), but their manual execution is slow and error-prone. While recent advances in LLMs offer promise for automating incident management tasks, existing LLM-based solutions lack specialized support for several key challenges, including managing TSG quality issues, interpreting complex control flow, handling data-intensive queries, and exploiting execution parallelism. We first conducted an empirical study on 92 real-world TSGs, and, guided by our findings, we present StepFly, a novel end-to-end agentic framework for troubleshooting guide automation. Our approach features a three-stage workflow: the first stage provides a comprehensive guide together with a tool, TSG Mentor, to assist SREs in improving TSG quality; the second stage performs offline preprocessing using LLMs to extract structured execution DAGs from unstructured TSGs and to create dedicated Query Preparation Plugins (QPPs); and the third stage executes online using a DAG-guided scheduler-executor framework with a memory system to guarantee correct workflow and support parallel execution of independent steps. Our empirical evaluation on a collection of real-world TSGs and incidents demonstrates that StepFly achieves a ∼94% success rate on GPT-4.1, outperforming baselines with less time and token consumption. Furthermore, it achieves a remarkable execution time reduction of 32.9% to 70.4% for parallelizable TSGs.

## 12. TORAI: Multi-Source Root Cause Analysis for Blind Spots in the Microservice Service Call Graph

**Authors:** Luan Pham (University of New South Wales, Australia), Huong Ha (RMIT University), Xiuzhen Zhang (RMIT University), Hongyu Zhang (Chongqing University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808137

**中文总结:** 提出 TORAI，在服务调用图存在无追踪盲区时，不依赖完整调用图，而用多源遥测异常严重度聚类与因果排序定位细粒度根因；在三个基准与真实故障上显著优于 SOTA，且常在 Top-3 命中根因。

**Abstract:** Typical multi-source root cause analysis (RCA) methods for microservice systems assume all services have traces to construct a service call graph. However, this assumption is not practical as microservice systems evolve rapidly and may contain blackbox services without traces, such as compiled software or unsupported services. We refer to these services as \textit{blind spots}. In the presence of blind spots, the performance of existing multi-source RCA methods may be affected, as they only diagnose \textit{visible} services on the call graph. To overcome this limitation, we propose TORAI, a novel unsupervised approach that effectively pinpoints fine-grained root causes without relying on the service call graph. Instead, TORAI first measures anomaly severity using available multi-source telemetry data. It then performs clustering to group services based on their severity symptoms and conducts causal analysis to rank services within each severity cluster. Finally, TORAI aggregates the cluster rankings and uses hypothesis testing to identify fine-grained root causes. TORAI provides an unsupervised approach that leverages available multi-source telemetry data for RCA without requiring a constructed service call graph or further intrusive actions, thus addressing the limitations of existing methods. Our experiments on three benchmark systems demonstrate that TORAI outperforms state-of-the-art baselines remarkably in the presence of blind spots. Performance on real-world failures further shows that TORAI can accurately pinpoint the root causes in top-3 recommendations.

## 13. Towards the Localization of Multi-Root-Cause Failures in Microservice Systems: An Active Intervention Framework

**Authors:** Yazhuo Gao, Lin Yang, Lianxiao Meng, Ran Zhu, Yining Cao

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808180

**中文总结:** 提出基于主动干预的多根因定位框架，用分层强化学习推断根因、用 Intervention-enhanced Graph Attention 预测故障场景并与实时状态迭代比对；在公开与自建数据集上相对次优方法单根因 PR@1 至少高 22%，多根因 RE@3 高 51.7%。

**Abstract:** In large-scale microservice systems, multi-root-cause failures often intertwine, significantly increasing overall system risk and triggering a deluge of cascading alerts that pose serious challenges to fault diagnosis and recovery. Existing root-cause localization techniques remain largely passive, relying on rule-based pattern recognition or graph-based propagation inference, and thus falter when faced with the complexity of multi–root-cause failures. To address these challenges, this paper introduces a novel active-intervention-based framework for root-cause localization. This framework uses Hierarchical Reinforcement Learning (HRL) to infer root causes and employs an Intervention-enhanced Graph ATtention network (IGAT) to predict the fault scenarios each cause may trigger. By iteratively comparing these predicted scenarios against the system’s real-time state, the framework dynamically refines its localization model. Experimental results on two public datasets and a constructed dataset show that our method outperforms the second-best method by at least 22% on the PR@1 metric in single root cause scenarios and leads by 51.7% on the RE@3 metric in multiple root cause scenarios. This fully demonstrates its significant advantages in the field of fault root cause analysis.

## 14. Understanding Performance Problems in CUDA Programs

**Authors:** Yuyang Bi, Junming Cao (Fudan University), You Lu (Fudan University), Bihuan Chen (Fudan University), Tianwei Gan (Fudan University), Dingji Wang (Fudan University), Xin Peng (Fudan University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797143

**中文总结:** 首次系统刻画 CUDA 性能问题：从 StackOverflow 与 NVIDIA 论坛收集 216 例分析症状与根因，并在 69 个可复现案例上测量修复加速比与现有分析方法能力；为开发者与后续性能分析研究提供实证指引。

**Abstract:** With the wide adoption of GPUs in high-performance computing, CUDA programming has become essential for leveraging GPU parallelism. However, its complex programming model poses challenges in performance optimization. Consequently, CUDA programs often suffer from performance problems. In that sense, it is crucial to understand the performance problems specific to CUDA programming. Unfortunately, no systematic study has been conducted in literature.

To bridge this gap, we conduct the first systematic study to 1) characterize the symptoms and root causes of 216 performance problems collected from 55 StackOverflow posts and 122 NVIDIA forum posts, and 2) measure the speedup of fixing performance problems, and assess the capability of existing performance analysis methods using a dataset of 69 reproduced performance problems. Our findings provide practical guidance for developers, and opportunities for researchers to advance performance analysis.

## 15. When Shared Worlds Break: Demystifying Defects in Multi-User Extended Reality Software Systems

**Authors:** Shuqing Li (The Chinese University of Hong Kong), Chenran Zhang (Harbin Institute of Technology), Binchang Li (Harbin Institute of Technology), Cuiyun Gao (Harbin Institute of Technology, Shenzhen), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797131

**中文总结:** 对多用户 XR 系统开展大规模实证研究，基于 2,649 条真实缺陷报告构建涵盖症状表现、根因来源与后果严重性的分类体系；揭示同步失效、状态不一致等独特缺陷模式，为提升多用户 XR 可靠性提供实证依据。

**Abstract:** Multi-user Extended Reality (XR) systems enable transformative shared experiences but introduce unique software defects that compromise user experience. Understanding software defects in multi-user XR systems is crucial for enhancing system reliability, yet remains underexplored. To fill the gap, this paper presents the first large-scale empirical study of multi-user XR defects, analyzing 2,649 real-world bug reports from diverse sources, including developer forums, GitHub repositories, and app reviews on mainstream XR app stores. Through rigorous qualitative analysis using iterative open coding, we develop a comprehensive taxonomy that classifies multi-user XR bugs along three dimensions: Symptom Manifestation, Root Cause Origin, and Consequence Severity. Our findings reveal that synchronization inconsistencies and avatar-related anomalies are the most prevalent symptoms, while network/synchronization logic defects and session management flaws emerge as dominant root causes. Critically, over 34% of analyzed bugs lead to severe consequences that fundamentally break the shared experience, including system crashes, persistent disconnections, and complete interaction breakdowns, etc. We also identify concerning privacy and health implications unique to multi-user XR contexts. Based on our findings of defect analysis, we provide actionable recommendations for developers, platform vendors, and researchers. Our results demonstrate that multi-user XR systems face distinct challenges at the intersection of distributed systems, real-time 3D interaction, and immersive experiences, necessitating specialized approaches to testing, debugging, and quality assurance. Our datasets and results are released to facilitate follow-up studies: https://sites.google.com/view/multi-user-xr-study .
