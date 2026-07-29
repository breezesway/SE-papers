# ISSTA 2026 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 16

## 1. A Closer Look at the Use of Reinforcement Learning for Speeding Up Runtime Verification of Software Tests (Experience Paper)

**Authors:** Shinhae Kim (Cornell University), Saikat Dutta (Cornell University), Owolabi Legunsen (Cornell University)

**Categories:** Program Analysis and Verification

**中文总结:** 本文首次深入评估基于强化学习的运行时验证方法 Valg，在 58 个 Java 项目上量化其与最优基线的性能差距及时间开销分布。结果表明 RL-RV 虽有前景，但在唯一 trace 保留、测试非确定性等方面仍有显著改进空间。

**Abstract:** Runtime verification (RV) found many bugs by monitoring passing tests against formal specifications (specs), but it is slow. Researchers have recently shown that reinforcement learning (RL) can be used to speed up by RV during testing—by up to 551.5x, finding 99.6% of spec violations. We call this approach, “RL-based RV”; it aims to probabilistically monitor most unique traces—sequences of events like method calls—and monitor fewer redundant ones. But, there was no detailed study to understand remaining challenges in RL-based RV, towards finding insights and opportunities for improvement. We conduct the first in-depth study of RL-based RV. In particular, we focus on the only RL-based RV technique, Valg, and answer five main questions, using 58 Java projects. (i) How much slower is Valg than two optimal baselines? Up to 323.8x, or 3.2 hours (vs. running tests without RV), and up to 9.6x, or 25.3 minutes (vs. a theoretically optimal baseline that monitors only unique traces). (ii) Where does Valg spend its time? 48.6% (or 1.9 hours) is spent on monitoring, and 24.1% (or, 48.5 minutes) is also spent on signaling events to monitors. (iii) What characterizes code where Valg monitors too many redundant traces or misses unique ones? Across 100 code locations, at least 67.8% of redundant traces are due to limitations of the convergence heuristic, and 41.3% of missed unique traces occur when Valg’s assumption do not hold. (iv) How much do test non-determinism and the stochasticity of RL algorithm affect unique trace preservation? We see up to 95.5pp swings in the rate of unique trace preservation on the same project. (v) How do other off-the shelf RL algorithms compare with Valg? Only two of 11 RL algorithms that we survey are feasible in continuous integration; both are slower than Valg and miss more unique traces. So, custom RL algorithms for RV are needed. Overall, RL-based RV is promising, but there is plenty of room to improve it. We highlight several exciting directions for future research on doing so.


## 2. Applying System Call Filtering to Real-World Binaries (Experience Paper)

**Authors:** Soumyakant Priyadarshan (Bloomberg), Seyedhamed Ghavamnia (Bloomberg)

**Categories:** Program Analysis and Verification

**中文总结:** 经验性评估多种二进制分析工具在真实程序上的系统调用推断效果。发现针对单次调用的 CFG 精化提升有限，而减少 address-taken 函数集合的全局技术（如重定位信息）可显著缩小 syscall 集合。

**Abstract:** System call filtering restricts applications to the system calls they require, but inferring accurate syscall sets for binary-only programs remains challenging. A central difficulty lies in recovering precise control-flow information from binaries: over-approximation leads to overly permissive syscall filters, while missed control-flow edges result in unsound policies. Although many techniques have been proposed to improve control-flow recovery in binaries, their practical impact on syscall inference remains poorly understood. In this work, we conduct an empirical study of syscall inference from binaries using multiple off-the-shelf binary analysis tools. We evaluate how different control-flow refinement techniques affect inferred syscall sets in practice.

Our experiments on real-world applications show that refinements targeting individual control- flow transfers (e.g., call-site and callee argument matching) substantially improve per-call target precision but often do not reduce the overall syscall set. In contrast, techniques that reduce the global set of address-taken functions—such as leveraging relocation information to accurately identify code pointers—yield the most significant syscall reductions. Finally, we identify a practical lower bound on syscall reduction achievable via sound static binary analysis alone, and show that further improvements are likely to require configuration or workload-aware specialization.


## 3. AsyncLeakBench: A Curated Benchmark of Asynchronous Resource Leaks in Open-Source Java Projects

**Authors:** Jinyoung Kim (Sungkyunkwan University), Jinseok Heo (Sungkyunkwan University, South Korea), Dongwook Choi (SungKyunKwan University), Eunseok Lee (Sungkyunkwan University, South Korea)

**Categories:** Program Analysis and Verification

**中文总结:** 发布异步 Java 资源泄漏基准 AsyncLeakBench，含 572 组来自 18 个开源项目的缺陷-补丁对并划分 11 类异步触发模式。评估显示现有检测器对取消、超时等异步事件触发的泄漏检测能力严重不足。

**Abstract:** Asynchronous programming has become a core execution model in modern Java software, powering server-side processing, network I/O, reactive streams, task scheduling, and RPC communication. In such asynchronous executions, resource creation and release are no longer confined to a single call stack; instead, they are distributed across heterogeneous execution contexts such as callbacks, Future/Promise chains, and scheduler boundaries. As a result, a resource lifecycle can be determined non-deterministically by events such as execution ordering, races, cancellation, and timeouts, making resource leaks a critical source of performance degradation and failures. However, prior research and public datasets on resource leaks have largely focused on synchronous settings, where defects typically manifest as missing \texttt{close} calls or omitted exceptional paths. In synchronous programs, release logic is often located within the same thread and call stack, allowing leaks to be defined and analyzed by tracking \texttt{close} invocations along normal and exceptional control-flow paths. In contrast, in asynchronous environments, resource release depends on the execution of callbacks on different threads, Future completion events, or scheduler decisions, and the release path itself may vary under cancellation, timeouts, or changes in execution order. Therefore, existing synchronous leak datasets fail to adequately represent the conditions and repair strategies of asynchronous resource leaks, hindering quantitative and fair evaluation of detection and automated repair techniques. To bridge this gap, we present \textbf{AsyncLeakBench}, a public benchmark that systematically curates real-world asynchronous resource leak defects that have been fixed in open-source Java projects. We collect \textbf{572} defect–patch pairs from \textbf{18} representative projects via a semi-automatic workflow, and refine them into high-quality ground truth through iterative filtering and manual validation. We further categorize the collected cases into \textbf{11} categories, summarizing key triggers and repair strategies driven by asynchronous events such as cancellation, timeouts, and scheduler boundaries. Moreover, an initial evaluation on existing resource leak detectors confirms that their detection performance is limited, particularly for leak patterns activated by asynchronous events such as cancellation and timeouts, highlighting the need for a dedicated benchmark for this defect class. AsyncLeakBench provides a realistic and reproducible evaluation basis for asynchronous resource leak detection and automated repair, static and dynamic analysis, fault localization, and LLM-based debugging. By establishing asynchronous resource leaks as a distinct defect class and offering a standardized benchmark for systematic study, this work contributes to advancing future research in software analysis and testing.


## 4. avaCGs: Version-Aware Call Graphs for Efficient Version-Range Queries

**Authors:** Johannes Düsing (Universität Stuttgart), Dominik Helm (University of Stuttgart), Ben Hermann (University of Stuttgart)

**Categories:** Program Analysis and Verification

**中文总结:** 提出 artifact 版本感知调用图 avaCG，将软件 artifact 所有版本的 call graph 合并为单一结构以支持版本区间可达性查询。增量 RTA 构造比逐版本全量构建快最多 79%，查询性能提升最多 9.58 倍。

**Abstract:** Developers employ version ranges to specify a range of valid versions for software libraries their projects depend on. While this can yield benefits like automatic adoption of library updates, it complicates method reachability analysis: a sound whole-program analysis must consider method invocations of every library release within that range. Such releases might themselves introduce transitive ranged dependencies to a project, leading to a combinatorial blow-up in the number of configurations to analyze. If developers wanted to soundly determine whether a critical method might be reachable via a ranged library dependency, they would have to build the individual call graphs for every release within that range, and perform reachability analysis on each one of them. As call-graph construction is an expensive operation, this approach is rarely practical. To enable direct version-range queries, we introduce artifact version-aware call graphs (avaCGs) that comprise call graph information about all versions of a software artifact in a single graph structure. Further, we propose a novel approach that incrementally computes call graphs based on Rapid Type Analysis (RTA) , implement it for the JVM platform, and show that it yields identical results to full RTA call-graph builds. Our evaluation shows that on our benchmarks, avaCGs can improve the performance of reachability queries by up to 9.58x, while our incremental construction is up to 79% faster compared to full builds for each release. We also observe that for real-world libraries hosted on Maven Central, almost 80% of all releases do not change the RTA call graph compared to their previous release, further justifying the use of incremental approaches.


## 5. Characterizing Real-World Bugs in Tile Programs for Automated Bug Detection

**Authors:** Ravishka Rathnasuriya (The University of Texas - Dallas), Zihe Song (University of Texas at Dallas), Nidhi Majoju (University of Texas at Dallas), Tingxi Li (The University of Texas at Dallas), Aaryaa Moharir (The University of Texas at Dallas), Wei Yang (UT Dallas), Tao Xie (Peking University)

**Categories:** Program Analysis and Verification

**中文总结:** 本文首次系统刻画 Tile 编程框架中的代码生成缺陷，分析 GitHub 上 301 个真实 bug 报告并归纳根因、症状、触发 oracle 与修复策略。为 Tile 编译器基础设施的调试、测试与修复工具提供基础实证依据。

**Abstract:** Tile-based programming frameworks are increasingly adopted to write high-performance GPU kernels in domains such as deep learning and scientific computing. While these frameworks enhance productivity and hardware utilization, their multi-stage compilation pipelines introduce distinct code generation bugs that are tightly coupled to input shapes, data types, and backend targets. These bugs often manifest as silent correctness or performance issues, making them difficult to detect using existing compiler testing tools. Additionally, the unique programming conventions of tile domain specific languages complicate root cause identification, while fixing such bugs demands specialized knowledge of tile abstractions and compilation pipelines. Despite the growing adoption of tile-based systems, their code generation bugs remain largely unexplored.

This paper presents the first systematic study of tile-program code generation bugs. We analyze 301 real-world bug reports from GitHub and categorize their root causes, symptoms, input patterns, test oracles that trigger these bugs and the strategies used to fix them. Our study provides foundational insights for building debugging, testing, and repair tools tailored to tile-based compiler infrastructures.


## 6. CLASScanner: Efficient C++ Class Recovery from Binaries Driven by Object Flow Graphs

**Authors:** JiaMing Wang (Tsinghua University), GongMing Wang (Huazhong University of Science and Technology), Songtao Yang (Zhongguancun Laboratory), Xi Cao (Science City (Guangzhou) Digital Technology Group Co., Ltd.), Chao Zhang (Tsinghua University)

**Categories:** Program Analysis and Verification

**中文总结:** CLASScanner 提出 Object Flow Graph 抽象对象生命周期数据流，结合静态分析与 LLM 推理从剥离二进制中恢复 C++ 类及其继承与组合关系。在 167,982 个函数的真实二进制上属性与构造/析构函数 F1 均超过 93%。

**Abstract:** C++ class recovery is fundamental to reverse engineering, serving as a basis for critical downstream tasks such as vulnerability analysis, malware comprehension, and decompiler output optimization. Existing approaches face several challenges, including dependency on virtual function tables and a lack of support for non-polymorphic classes, dependency on high-quality test cases for dynamic analysis, and dependency on computationally expensive reasoning. Furthermore, existing rule-based techniques fail to recover class relationships in non-polymorphic classes, including inheritance and composition, thereby reducing fidelity to original program semantics. To address these problems, we propose CLASScanner, a novel approach for recovering C++ classes from stripped binaries. We design a data-flow abstraction, \textit{Object Flow Graph} (OFG), to model the behaviors of objects across different contexts throughout their lifecycles. Driven by the OFG, CLASScanner identifies classes and recovers their attributes and methods. We further propose a progressive framework that synergizes static analysis with LLM-based reasoning to infer class inheritance and composition relationships. We evaluate CLASScanner on a dataset of real-world binaries comprising 167,982 functions. It achieved F1-scores of 95.4, 93.7, 75.4, 89.9, and 92.7 in recovering attributes, constructors, destructors, class inheritance, and class composition, respectively. Compared to state-of-the-art approaches, CLASScanner significantly improves the F1-scores while reducing runtime overhead, requiring only 10.3% of the execution time on average, making it promising for real-world reverse engineering tasks.


## 7. Defusing Logic Bombs in Symbolic Execution with LLM-Generated Ghost Code

**Authors:** Dimitrios Stamatios Bouras, Sergey Mechatev (Peking University)

**Categories:** Program Analysis and Verification

**中文总结:** Gordian 在 KLEE 符号执行中有选择地调用 LLM 生成 ghost code 辅助 SMT 求解器处理求解困难片段，保留全局精确推理能力。在 FDLibM 等基准上覆盖率较传统符号执行提升 52%–84%，LLM token 消耗降低 90%–96%。

**Abstract:** Symbolic execution is a powerful program analysis technique, but its effectiveness is fundamentally limited by solver-hostile program fragments, complex numerical reasoning, and unbounded heap structures. Recent work proposed replacing constraint solvers with large language models (LLMs) to bypass these limitations, but such approaches struggle to analyze real-world codebases, where deep execution paths require globally consistent reasoning across many interacting constraints. We present Gordian, a hybrid symbolic execution framework that uses LLMs selectively to generate lightweight ghost code that aids an SMT solver in handling solver-hostile code fragments, while preserving its precise, global reasoning capability. In particular, we propose three types of ghost code: (1) inversion of difficult code fragments with iterative bidirectional constraint propagation, (2) modeling via solver-friendly surrogates while preserving relevant behavior, and (3) semantic partitioning of unbounded heap spaces. We implemented Gordian on top of the KLEE symbolic execution engine and evaluated it on synthetic “logic bombs” capturing distinct symbolic reasoning challenges, a popular mathematical library FDLibM, and three structured-input programs (libexpat, jq, and bc). Across all benchmarks, Gordian improves coverage on average by 52-84% over traditional symbolic execution baselines, and by 86-419% over LLM-based techniques, while reducing LLM token usage by an average of 90-96%. This highlights the practicality and effectiveness of this approach in real-world settings.


## 8. Efficient Predictive Monitoring of Message Passing Interface Programs

**Authors:** Jiaqiang Yao (College of Computer, National University of Defense Technology), Haocheng Geng (College of Computer Science and Technology, National University of Defense Technology), Zhenbang Chen (College of Computer, National University of Defense Technology)

**Categories:** Program Analysis and Verification

**中文总结:** MPI-PRV 从单次 MPI 程序执行迹出发，基于迹等价预测合法调度变体并检验时序属性，用向量时钟强制执行 MPI 语义依赖约束。在 13 个真实应用的 38 组配置上全部成功分析，运行时间与内存较 MPI-SV 降低数个数量级。

**Abstract:** The Message Passing Interface (MPI) is the standard programming model for high-performance computing, yet nondeterministic scheduling in concurrent executions makes reliability assurance highly challenging. Beyond deadlocks, property-related bugs such as modifying a send buffer before a nonblocking send completes or accessing a freed RMA window are often hard to reproduce and validate, as they typically manifest only under rare event interleavings and can be both latent and catastrophic. Existing dynamic checkers usually cover only the observed schedule of a single execution; dynamic verification largely focuses on deadlocks; and static techniques scale poorly to medium-to-large programs, often timing out or running out of memory. Overall, existing techniques do not support scalable analysis of temporal properties in large MPI programs.

To address these limitations, we propose the first efficient predictive monitoring approach for temporal properties in MPI programs. From a single execution, we collect an event trace and use trace equivalence to predict the set of legal equivalent executions under the same input. We then check whether any predicted execution satisfies the target property. To make this process sound, we formalize three correctness criteria for MPI trace reordering and enforce them through MPI-semantics-driven dependency extraction, tracked with vector clocks. To improve efficiency, we exploit the bounded length of a pattern language and reduce long-trace reordering to reordering short patterns. We implement our approach in MPI-PRV, instantiate ten representative MPI bug properties, and evaluate it on 13 real-world MPI applications with 38 configurations. MPI-PRV successfully and correctly analyzes all $38$ tasks, whereas MPI-SV and MUST analyze only $14$ and $11$ tasks, respectively. MPI-PRV also achieves orders-of-magnitude reductions in runtime and memory usage, demonstrating strong efficiency and scalability for large MPI programs.


## 9. Multi-Stage On-Demand Program Slicing for Modular Analysis of Multi-Threaded Programs

**Authors:** Jiawei Yang (UNSW), Xiao Cheng (Macquarie University), Jiawei Wang (UNSW), Xiapu Luo (Hong Kong Polytechnic University), Yulei Sui (University of New South Wales)

**Categories:** Program Analysis and Verification

**中文总结:** MSli 在 SVF 中实现多阶段按需切片，分阶段提取 ILA 与 FSPTA 相关片段以模块化分析多线程程序。相较全程序 FSAM，ICFG 分析规模降至 5.4%/25.7%，总耗时降至 20.8% 且数据竞争告警结果一致。

**Abstract:** Precise analysis of multi-threaded programs requires combining flow-sensitive pointer analysis (FSPTA) with interleaving and lock analysis (ILA) to reason about cross-thread value flows under feasible concurrent executions. ILA computes may-happen-in-parallel (MHP) relations and lock-release spans to determine when shared accesses can occur concurrently. Unfortunately, these analyses are both expensive and tightly coupled: FSPTA needs ILA to rule out infeasible inter-thread def-use relations, while ILA needs alias information to identify interference-relevant interactions. As a result, whole-program analyses often spend most of their time on code that is irrelevant to the client query. We present MSli, an on-demand slicing framework for modular analysis of multi-threaded programs. It extracts compact, query-relevant program slices while preserving the answers of downstream analyses. Unlike single-pass slicing over a unified dependence graph, MSli performs multi-stage slicing with analysis-specific criteria. Concretely, a lightweight pre-analysis establishes an over-approximation of inter-thread value flows and performs ILA slicing source extraction to identify the MHP and lock-span queries required later for ILA slicing. The refined main-phase ILA results then enable reconstruction of a thread-aware value-flow graph to guide FSPTA slicing, supporting modular analysis and downstream clients. We implement MSli in SVF and evaluate it on ten large real-world projects with data race detection as a representative client. Compared with the unsliced baseline (FSAM), MSli reduces the analyzed ICFG to 5.4% (ILA) and 25.7% (FSPTA), reduces ILA/FSPTA runtimes to 4.7%/18.3%, and cuts total analysis time to 20.8% on average, while producing identical query outcomes and race alarms.


## 10. RecurIC3: Exploiting Structural Lemma Reuse to Accelerate IC3

**Authors:** Yuhan Li, Liangze Yin (National University of Defense Technology), Xinyi Gong (National University of Defense Technology), Liu Minghao, Tun Li (National University of Defense Technology), Wei Dong (National University of Defense Technology), Ji Wang (National University of Defense Technology)

**Categories:** Program Analysis and Verification

**中文总结:** 提出 RecurIC3，以 Bad State Tree 持久化 CTI 及其 blocking chain 结构并复用历史候选，减少 IC3/PDR 冗余探索。在 Kind2 上触发复用时节点数降 27%、累计加速 1.42×，并额外解出 16 个实例。

**Abstract:** IC3/PDR has become a widely adopted technique for safety model checking due to its high efficiency. Despite its success, the algorithm often suffers from redundant exploration due to the lack of a cross-level memory mechanism. This results in the repetitive discovery of highly similar CTIs (Counterexamples to Induction), forcing the solver to waste computational effort traversing overlapping blocking chains. We propose RecurIC3, a framework that alleviates this bottleneck via structural reuse. RecurIC3 maintains a Bad State Tree ($\mathcal{G} {bad}$) that persistently records CTIs together with their level-aligned predecessor–successor links along blocking chains, turning the blocking phase into a history-aware process. To reduce solver calls, RecurIC3 first retrieves and rechecks lightweight candidates from $\mathcal{G} {bad}$, and falls back to solver queries only when reuse is exhausted.This approach can significantly reduce the search space, thereby enhancing the verification efficiency of IC3.

We implemented RecurIC3 in the state-of-the-art model checker Kind2 and evaluated it on the official benchmark suite. On instances where reuse is triggered, RecurIC3 reduces the number of explored tree nodes by \textbf{27%}, achieves a \textbf{1.42$\times$} cumulative speedup, and solves \textbf{16} additional instances (\textbf{13} \textsc{safe} and \textbf{3} \textsc{unsafe}) within the same timeout. These results suggest that structural reuse can substantially accelerate IC3.


## 11. Rust's Type Checker Implementation is Unsound: An Empirical Study on Soundness Bugs in rustc

**Authors:** Yusung Sim (KAIST), Sukyoung Ryu (KAIST, South Korea), Jaemin Hong (UNIST, South Korea)

**Categories:** Program Analysis and Verification

**中文总结:** 对 2022–2025 年 rustc 中 23 个潜在 soundness bug 做实证研究，分析触发特征、后果与生命周期。发现 implied bounds、trait objects 等常破坏内存安全，Miri 可检部分缺陷而 Chalk/a-mir-formality 仍不成熟。

**Abstract:** Rust is claimed to be a \emph{type-sound} language capable of preventing various undesirable behaviors, including memory bugs. However, rustc , the official Rust compiler, is not immune to defects; it contains \emph{soundness bugs}, where the compiler accepts programs that should be rejected during type checking. In this work, we present an empirical study of 23 issues that report potential soundness bugs in rustc , collected from the GitHub issue tracker between January 1, 2022 and September 1, 2025. We analyze each issue in depth, focusing on its \emph{affected feature}, \emph{symptom} (how the feature is mishandled), \emph{consequence} (the resulting undesirable behavior), \emph{triggering features}, \emph{community consensus} regarding whether it is a bug, and \emph{lifecycle}, including introduction, discovery, and fix. Furthermore, we investigate existing artifacts, including implementations such as Miri, Chalk, and a-mir-formality, alongside documentation such as the Rust Reference, the FLS, and Rust RFCs to assess their potential as oracles for testing the type soundness of rustc . Our key findings indicate that: (1) Certain soundness bugs, typically triggered by \emph{implied bounds} or \emph{trait objects}, compromise memory safety. (2) Sound type checking is challenged by edge cases involving \emph{associated types} and the interaction between \emph{lifetimes} and \emph{traits}. (3) Most bugs persist from the initial introduction of the relevant features and require significant time to be discovered. (4) While Miri can detect soundness bugs that lead to memory bugs, a-mir-formality and Chalk are currently immature despite their potential to identify other bug categories. (5) Existing documentation frequently fails to provide precise explanations of the language semantics.


## 12. Scitix: Scalable Constraint-Based Type Inference for Code Snippets with Missing Types

**Authors:** Yiwen Dong (University of Waterloo), Zhenyang Xu (University of Waterloo), Yongqiang Tian (Monash University, Hong Kong SAR China), Edward Lee (University of Toronto at Scarborough), Ondřej Lhoták (University of Waterloo), Chengnian Sun (University of Waterloo)

**Categories:** Program Analysis and Verification

**中文总结:** 提出 Scitix，以 Any 表示缺失类型并迭代求解约束，实现可扩展的代码片段类型推断。在 3000+ jar 知识库上 Stack Overflow F1 达 94.8%，SnR 超时近 0%，错误率较 GPT-4o 最多降 78%。

**Abstract:** Code snippets are commonly used in online developer communities to help communicate ideas and algorithms. However, contextual information, like dependencies and the exact types, are often missing in code snippets, which makes their reuse difficult. Some of the most successful automated techniques use logical constraints to infer the types and dependencies, but they do not work in practice because they require an exact knowledge base that contains all possible dependencies and exact types. However, such a knowledge base is both computationally expensive for constraint solving and impossible to achieve in the presence of missing types (e.g., user-defined types) in code snippets.

To this end, this paper proposes a novel, scalable technique named Scitix. Our insight is two-fold. First, inspired by gradual typing, we represent certain missing types as Any, ignoring such types during constraint solving, improving performance and scalability. Second, our novel, iterative constraint-solving approach saves on computation and skips constraints involving these missing types. Our extensive evaluations show that our insights improve both performance and scalability compared to SnR (the state of the art). Specifically, Scitix achieves F1-scores of 94.8% and 86.8% on Stack Overflow and generated code snippets, respectively, using a large knowledge base of over 3,000 jars. In contrast, SnR consistently times out, yielding F1-scores close to 0%. Even with the smallest knowledge base, where SnR does not time out, Scitix reduces the number of errors by 77% and 45% compared to SnR. Compared to state-of-the-art large language models (LLMs) like GPT-4o and LLM-based ZS4C, Scitix achieves up to 78% reduction in error rates. Scitix’s strong performance highlights its potential as a practical technique for type inference in real-world code snippets.


## 13. SemantiX: A Compatibility Checker between Applications and Compositions of Distributed Systems

**Authors:** Yifei Sun (Inria, ENS de Lyon, Univ. Grenoble Alpes), Ji-Yong Shin (Northeastern University)

**Categories:** Program Analysis and Verification

**中文总结:** 提出 SemantiX，以 AppGraph 建模应用并与形式化分布式一致性语义模块做兼容性检查或搜索可行组合。三个案例研究显示可快速验证流媒体、电商与跨服务因果存储的设计语义匹配。

**Abstract:** Modern distributed applications compose multiple services with different consistency guarantees. Mismatches between application requirements and chosen system semantics can introduce subtle bugs, but verifying compatibility across complex applications is both challenging and time-consuming. In particular, existing approaches on testing or rigorous formal verification lack flexibility and cannot promptly provide correctness guarantees on multi-semantic compositions.

We present SemantiX, a framework for checking semantic compatibility between applications and compositions of distributed systems with heterogeneous consistency models. SemantiX embeds formally defined distributed system modules of consistency semantics which include the first formal definition of visibility constraints. SemantiX introduces the AppGraph approach for systematically modeling complex applications. Applications modeled using AppGraphs can be checked for their compatibility against a combination of distributed system modules. Alternatively, SemantiX can search for combinations of modules compatible to the application. We present three case studies on a movie streaming service, an e-commerce platform, and a cross-service causal distributed storage service. We demonstrate that SemantiX can capture complex service compositions with minimal encoding effort and quickly check compositional compatibility with underlying systems or find the compatible system sets. SemantiX enables developers to efficiently verify distributed application designs and explore alternative consistency configurations, supporting more agile development.


## 14. Solving String Split Constraints via Structural Relaxation

**Authors:** Rui Han (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Ziheng Wang (Hangzhou Institute for Advanced Study, University of Chinese Academy of Sciences, Hangzhou, China), Baoquan Cui (Institute of Software at Chinese Academy of Sciences, China), Yuhang Dong (Laboratory of Parallel Software and Computational Science, Institution of Software Chinese Academy of Sciences, University of Chinese Academy of Sciences, Beijing, China), Fuqi Jia (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Feifei Ma (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Jian Zhang (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**中文总结:** 提出 structural relaxation 编码，将 split 结构从严格长度要求解耦并按需物化段，支持复杂正则分隔符的 SMT-LIB 合规 split 约束。580 个基准中解出 157/168 个真实案例，并暴露 12 个主流字符串求解器实现 bug。

**Abstract:** String operations are integral to program analysis, yet reasoning about the ubiquitous \texttt{split} operation remains a challenge. SMT solvers have difficulty with \texttt{split} because it transforms a string into a \emph{variable-length sequence}, creating a structural mismatch that leads to uninterpreted abstractions or unsound bounded approximations. In this paper, we bridge this gap with a precise, SMT-LIB-compliant encoding. Our key insight is \emph{structural relaxation}: exploiting the sparsity of real-world constraints, we decouple the split structure from strict length requirements, materializing segments only on demand. We further introduce position-aware constraints to handle complex regex-based delimiters without overlaps.

We evaluated our framework on 580 benchmarks using four leading string solvers. Our encoding enables off-the-shelf solvers to handle split constraints, solving 157 out of 168 real-world benchmarks and outperforming current baselines. Notably, our framework involves complex string operations, thereby revealing 12 previously unknown implementation bugs in mainstream solvers.


## 15. The Unseen Delta: Characterizing the Compiler Optimization Landscape via Top-Down Differential Analysis

**Authors:** Zhibo Liu (Nanjing University), Huaijin Wang (Shandong University), Shuai Wang (Hong Kong University of Science and Technology)

**Categories:** Program Analysis and Verification

**中文总结:** 提出自顶向下差分分析方法论，用层次化微架构指标校准 GCC 与 Clang 生成二进制的性能差异并定位关键代码片段。发现显著且意外的优化差距，并通过二进制补丁框架移植更优代码序列修复性能问题。

**Abstract:** Compiler optimizations are essential for achieving high performance in modern software. However, recent studies highlight the persistence of performance bugs, i.e., subtle defects where the compiler generates functionally correct but computationally inefficient code, leading to significant performance degradation. Existing detection and testing methods typically employ a bottom-up approach, focusing on specific low-level code properties and remaining confined to known optimization rules. Consequently, they struggle to quantify the holistic impact of identified issues and often overlook critical microarchitectural inefficiencies.

We observe a key indicator of untapped potential: different compilers often produce binaries with significant performance differences for identical source code. However, the root causes of these discrepancies remain largely unexplored and difficult to pinpoint using current techniques. To bridge this gap, we introduce a top-down differential analysis methodology. This approach calibrates compiler optimization differences with fine-grained, hierarchical microarchitectural metrics, offering a comprehensive view of runtime behavior. Using a sampling-based approach, this method efficiently pinpoints the critical code snippets responsible for performance differences, enabling targeted root cause analysis.

Our empirical evaluation uncovers substantial and often surprising performance differences between binaries generated by GCC and Clang. A categorization of root causes reveals systemic challenges in compiler optimizations. To quantitatively validate our findings and demonstrate practical impact, we developed a binary patching framework that fixes identified performance issues by transplanting superior code sequences from competing compilers. This work provides a novel lens for understanding and analyzing optimization defects.


## 16. Vbox: Efficient Black-Box Serializability Verification

**Authors:** Weihua Sun (Harbin Institute of Technology), Zhaonian Zou (Harbin Institute of Technology)

**Categories:** Program Analysis and Verification

**中文总结:** Vbox 提出支持谓词操作、利用交易时序信息并以 SAT 求解的黑盒可串行化验证方法。理论分析与实验均表明其正确高效，检测更广范围数据异常且不依赖特定并发控制协议。

**Abstract:** Verifying the serializability of transaction histories is essential for assessing whether a database management system (DBMS) correctly enforces the claimed serializable isolation level. Black-box serializability verification provides a practical means for such validation without relying on internal system details. Existing approaches often suffer from limitations including incomplete anomaly detection, high verification overhead, excessive memory consumption, or dependence on specific concurrency control protocols. This paper presents \textsf{Vbox}, a black-box serializability verification method that incorporates support for predicate database operations, systematic use of transaction timing information, and a satisfiability (SAT)-based formulation with an efficient solver. Both theoretical analysis and experimental evaluation show that \textsf{Vbox} is correct and efficient, detects a broader range of data anomalies, and does not rely on any particular concurrency control protocol.

