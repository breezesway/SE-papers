# ASE 2026 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 32

## 1. Adaptive Proof Refinement with LLM-Guided Strategy Selection

**Authors:** Minghai Lu (Purdue University, USA), Zhe Zhou (Purdue University, USA), Danning Xie (Meta, USA), Songlin Jia (Purdue University, USA), Benjamin Delaware (Purdue University, USA), Tianyi Zhang (Purdue University, USA)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834382

**中文总结:** 提出 Adapt：由 LLM 决策器据证明助手状态与错误证明上下文动态选择 refinement 策略；在两套 benchmark 上较最佳基线多证明 11.26% 与 18.58% 定理，并在六种 LLM 上展示可迁移性。

**Abstract:** Formal verification via theorem proving enables rigorous proofs of software correctness, but it is difficult to scale due to the significant manual effort and expertise required. While Large Language Models (LLMs) have shown potential in automating proof generation, they frequently produce incorrect proofs on the first attempt that require iterative refinement to fix. However, most existing approaches employ fixed refinement strategies and cannot dynamically choose an effective strategy, which limits their performance. To overcome this limitation, we introduce Adapt, a novel proof refinement framework that leverages an LLM-guided decision-maker to dynamically select a suitable refinement strategy according to the state of the proof assistant and available context of an incorrect proof. We evaluate Adapt on two benchmark suites against five existing methods and find that it significantly outperforms the best baseline on both by proving 11.26% and 18.58% more theorems, respectively. Furthermore, we demonstrate Adapt’s generalizability by evaluating it across six different LLMs. We also conduct ablation studies to measure the contribution of each component and compare the trade-offs of alternative decision-maker designs.


## 2. All or Nothing: How Library Type Annotations Affect Client-Side Errors in Python

**Authors:** Eric Asare (New York University Abu Dhabi, United Arab Emirates), Luca Di Grazia (University of St. Gallen, Switzerland), Sarah Nadi (New York University Abu Dhabi, United Arab Emirates)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834434

**中文总结:** 首次大规模用 Pyright 分析 13751 个客户端与 4178 个库的类型标注对下游错误的影响；70% 客户端存在第三方 API 相关类型错误，库端标注覆盖率需 ≥90% 才可见明显风险下降，且仅约 10% 库—客户端组合达到「高标注+客户端开 checker」的理想状态。

**Abstract:** Python’s gradual typing promises that library-side type annotations will propagate safety benefits to downstream clients. Despite over 83% of popular libraries now containing annotations, no empirical  
evidence exists on whether these efforts actually reduce type errors in client code. We present the first large-scale empirical study of this downstream impact, analyzing the interaction between 13,751 actively maintained client repositories and over 4,178 distinct third-party libraries using the Pyright static type checker. Our results show that (i) 70% of client repositories contain at least one type error stemming from third-party API usage, (ii) the error distribution is heavily skewed, with a small subset of widely used libraries, i.e., numpy, django, pandas, and pytorch, accounting for a disproportionate share of the ecosystem-wide error burden, (iii) measurable benefits of reduced error risks and propagation can only be seen with near-complete annotation coverage (≥ 90%), and (iv) although 60% of library-client pairs are aligned in their typing efforts, only 10% achieve the ideal scenario where highly annotated libraries meet client-side static type checking. Our findings expose a pervasive ecosystem gap: client adoption of static type checking outpaces library annotation efforts, with 19% of cases representing missed opportunities where clients use type checkers but their dependencies lack sufficient annotations. These results call for prioritizing comprehensive annotation of widely used libraries to unlock the full potential of Python’s gradual typing.


## 3. Automated Lemma Discovery in Agentic Program Verification

**Authors:** Huan Zhao (National University of Singapore, Singapore), Haoxin Tu (National University of Singapore, Singapore), Zhengyao Liu (National University of Singapore, Singapore), Martin C. Rinard (Massachusetts Institute of Technology, USA), Abhik Roychoudhury (National University of Singapore, Singapore)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834356

**中文总结:** 提出 LLM Agent LemmaNet，结合源码语义离线与证明过程在线发现/适配辅助引理，加速 deductive verification。在 SV-COMP 及 Linux kernel 等真实项目上显著优于现有 proof agent。

**Abstract:** Deductive verification provides strong correctness guarantees for code by extracting verification conditions (VCs) and writing formal proofs for them. The expertise-intensive task of VC proving is the main bottleneck in this process, and has been partly automated owing to recent advances in Large Language Model (LLM) agents. However, existing proof agents are not able to discover helper lemmas – auxiliary lemmas that aid in proving – and thus fall short as programs grow in size and complexity. In this paper, we argue that VC proving for program verification is more than a purely mathematical task, and benefits considerably from program comprehension. Our key insight is that human proof engineers often discover and apply helper lemmas based on their understanding of the program semantics, which are not directly reflected in the VCs produced by VC generators. Inspired by this insight, we propose an LLM agent, LemmaNet, that discovers helper lemmas in two ways. Specifically, the agent first synthesizes lemmas offline by directly analyzing the source code and specifications and then relating this semantic understanding to the mechanical, verbose encoding produced by VC generators. As the proof unfolds, LemmaNet then adapts existing helper lemmas online to accommodate evolving proof states, enabling the agent to effectively discharge complex VCs on-the-fly. We implement LemmaNet on top of an existing proof agent AutoRocq for Rocq and the Frama-C ecosystem, and evaluate it on SV-COMP and established real-world subjects, including modules of the Linux kernel, Contiki OS, standard C++ library, and X.509 parser. Our experimental results demonstrate that LemmaNet significantly outperforms state-of-the-art approaches, highlighting the importance of program comprehension-aided lemma discovery in agentic program verification.


## 4. Best-Effort GR(1) Synthesis: Exploiting Environmental Cooperation under Unrealizability

**Authors:** Sirui Liu (National University of Defense Technology, China), Yating Zhang (National University of Defense Technology, China), Chi Hu (China Academy of Engineering Physics, China), Wei Dong (National University of Defense Technology, China)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837439

**中文总结:** 对不可实现 GR(1) 规约提出 best-effort 合成：在环境可合作假设下最大化系统 justice 可延续性，并用三层嵌套 µ-calculus 刻画 winning region；在 Spectra 中实现，SYNTECH/AMBA/GenBuf 上表明该类可实现性在 well-separated 不可实现规约中较常见。

**Abstract:** Reactive synthesis automatically derives correct-by-construction controllers from temporal logic specifications. GR(1) synthesis is widely adopted due to its polynomial-time complexity and practical expressiveness. In practice, however, a significant proportion of GR(1) specifications are unrealizable. Conventional synthesis tools report failure in such cases, yet real-world environments are often governed by their own objectives rather than purely adversarial behavior, presenting opportunities for the system to leverage environmental cooperation toward satisfying its justice guarantees. For unrealizable GR(1) specifications, this paper proposes best-effort GR(1) synthesis. The approach requires the system strategy to satisfy two properties: best-effort extensibility, which preserves at every state reached by the play the possibility of satisfying all system justice guarantees, and persistent satisfiability of environment assumptions, which ensures that environmental cooperation does not preclude the environment from satisfying its own justice assumptions. For unrealizable but well-separated specifications, we construct a 3-nested µ-calculus fixpoint formula that characterizes the best-effort system winning region and prove its soundness and completeness. The resulting algorithm performs O ( n | Q |) symbolic next-state computations, compared with O ( mn | Q | 2 ) for standard GR(1) synthesis. We further analyze the relationship between the best-effort and standard GR(1) winning regions through finite cooperative reachability, yielding a hierarchical classification of dependence on environmental cooperation at the region and initial-state levels for well-separated but unrealizable specifications, thereby quantifying the degree of unrealizability. We implement best-effort checking, controller construction, and classification in the Spectra GR(1) synthesizer and evaluate the approach on a diversified corpus of SYNTECH, AMBA, and GenBuf specifications. Experimental results demonstrate that best-effort realizability is common among well-separated but unrealizable specifications and that all top-level unrealizability categories occur in the combined benchmark corpus.


## 5. Beyond Text Matching: Towards Reference-Free Evaluation for Human-Oriented Binary Reverse Engineering

**Authors:** Xiuwei Shang (University of Science and Technology of China, China / Singapore Management University, Singapore), Li Hu (University of Science and Technology of China, China), Xiao Jiang (University of Science and Technology of China, China), Jieke Shi (Singapore Management University, Singapore), Junda He (Singapore Management University, Singapore), Zhou Yang (University of Alberta, Canada), Shaoyin Cheng (University of Science and Technology of China, China / Anhui Province Key Laboratory of Digital Security, Hefei, China), Guoqiang Chen (University of Science and Technology of China, China), Weiming Zhang (University of Science and Technology of China, China / Anhui Province Key Laboratory of Digital Security, Hefei, China), David Lo (Singapore Management University, Singapore)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834339

**中文总结:** 系统研究 LLM-as-a-Judge 在无参考 HOBRE 评估（函数名恢复、反编译摘要、反编译优化），发布 BinJudgeBench；LLM 评判与人类相关约 63.2%，路由式 BinJudge 再提 4.5%–24.7% 相关并显著降 API 成本。

**Abstract:** Human-Oriented Binary Reverse Engineering (HOBRE) aims to transform decompiled pseudocode into a more human-friendly representation, thereby reducing the cognitive burden of reverse analysis and improving efficiency. However, reliably evaluating HOBRE outputs remains a fundamental challenge. On one hand, human evaluation is costly, time-consuming, as well as difficult to scale. On the other hand, existing automated metrics either rely on executable test cases and runtime environments, which are often unavailable for real-world binaries, or depend on high-quality source code references that are typically inaccessible and fail to capture semantically equivalent but lexically diverse outputs. Although the emerging LLM-as-a-Judge paradigm is naturally well-suited to HOBRE evaluation, its effectiveness has not yet been fully studied. This paper presents the first systematic investigation of the LLM-as-a-Judge paradigm for HOBRE, covering three representative tasks: function name recovery, binary code summarization, and decompilation optimization. We introduce BinJudgeBench, the first expert-annotated, reference-free evaluation benchmark based on multi-dimensional human judgment. Our empirical study reveals that LLM-as-a-Judge achieves an average correlation of 63.20% with human judgment, significantly outperforming traditional automated metrics at 35.04%. By analyzing the impact of various judge configurations, including backbone LLMs, prompting strategies, and decoding temperatures, on both correlation and cost, we find that no “one-size-fits-all” configuration exists, as the optimal setup varies across tasks and individual samples. To address this, we propose BinJudge, which employs a lightweight routing mechanism to adaptively select the optimal judge configuration for each specific task and sample. BinJudge improves correlation with human experts by 4.5%–24.7% and reduces API cost to 0.06×–0.84× of that of static best configurations, providing a scalable, cost-effective, and high-fidelity automated evaluation scheme for HOBRE.


## 6. Certified Program Synthesis with a Multi-modal Verifier

**Authors:** Yueyang Feng (National University of Singapore, Singapore), Dipesh Kafle (National University of Singapore, Singapore), Vladimir Gladshtein (National University of Singapore, Singapore), Vitaly Kurin (Neapolis University Pafos, Cyprus), George Pîrlea (National University of Singapore, Singapore), Qiyuan Zhao (National University of Singapore, Singapore), Peter Müller (ETH Zurich, Switzerland), Ilya Sergey (National University of Singapore, Singapore)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837559

**中文总结:** 围绕 Lean 上多模态验证器 Velvet 构建 agent 流水线 LeetProof：先用随机测试筛规约缺陷，再分阶段合成程序与证明并委派 residual obligation；较单模式基线在固定预算下显著提高 fully certified 解比例，并暴露既有 benchmark 规约问题。

**Abstract:** Certified program synthesis (a.k.a. vericoding ) is the process of automatically generating a program, its formal specification, and a machine-checkable proof of program/specification alignment from a natural-language task description.  
  
Two key challenges make vericoding difficult. First, specifications synthesised from natural language descriptions are often either too weak to be meaningful or too strong to be implementable, yet existing approaches lack systematic means to detect such defects. Second, the program verifiers used to validate results are fragmented: each tool supports a particular reasoning mode— auto-active (e.g., Dafny, Verus) or interactive (e.g., Rocq, Lean)—with its own trade-off between automation and expressivity. This forces each synthesis methodology to target a single paradigm, limiting the tasks it can handle.  
  
We overcome both challenges by structuring the synthesis workflow in stages around a multi-modal verifier —a single tool that combines dynamic validation, automated proofs, and interactive proof scripting within one foundational framework.  
  
We realise this idea in LeetProof, a new agentic pipeline built on Velvet, a multi-modal program verifier built in the Lean theorem prover. Multi-modality enables LeetProof to validate generated specifications via randomised property-based testing before any code is synthesised, decompose the synthesis task into sub-problems guided by verification conditions, and delegate residual proof obligations to frontier AI provers specialised for Lean.  
  
We evaluate LeetProof on an extensive benchmark suite derived from prior work on certified synthesis. Our specification validation uncovers defects in existing reference benchmarks, and LeetProof's staged pipeline achieves a significantly higher rate of fully certified solutions than a single-mode baseline at the same fixed budget—consistently across two different frontier LLM backends.


## 7. Clarity: From Formal System Designs to Verified RL Controllers

**Authors:** Austin O'Quinn (Ohio State University, USA), Conor Snedeker (Ohio State University, USA), Max Taylor (Boise State University, USA), Lance Joneckis (Idaho National Lab, USA), Christopher Stewart (Ohio State University, USA)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834429

**中文总结:** CLARITY 从 SysML v2 设计经翻译语义接入 nuXmv 验证安全需求，再合成 RL 流水线并生成运行时 monitor，实现设计—学习—运行保障的可追踪闭环；在三档复杂度 CPS 基准上验证需求、控制器与轻量监控一体化可行。

**Abstract:** Safety-critical cyber-physical systems increasingly use reinforcement learning-based controllers, yet existing engineering methodologies cannot assure these systems’ safety. Assuring safety requires connecting three concerns that are currently addressed in isolation: the system’s design, the reinforcement learning pipeline, and runtime verification. This paper introduces CLARITY, a system that ingests designs written in SysML v2 and, through novel translational semantics to the nuXmv model checker, verifies safety requirements, synthesizes a reinforcement learning pipeline, and generates a runtime monitor. CLARITY enables fully traceable safety assurance arguments for reinforcement learning-based systems, closing the gap between system design, controller synthesis, and  
runtime assurance. We validate CLARITY on three CPS benchmarks of increasing complexity, demonstrating verified safety requirements, effective learned controllers, and lightweight runtime monitoring from a single SysML v2 specification.


## 8. Conflict Extraction in Probabilistic Datalog Analyses

**Authors:** Siyu Chen (Purdue University, USA), Chungha Sung (Amazon Web Services, USA), Xuyang Li (Purdue University, USA), Jingbo Wang (Purdue University, USA)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834404

**中文总结:** 针对概率 Datalog 静态分析中告警边际独立但联合不可满足的问题，提出 PPProbe，利用 Datalog 推导图结构抽取最小不可满足子集；在 70 个基准上吞吐为现有 MUS 枚举器 2.5–24 倍，平均可过滤 47.7% 互斥告警。

**Abstract:** Probabilistic extensions of Datalog enable static analyses such as pointer analysis, data race detection, and side-channel analysis to rank alarms by likelihood, but this added expressiveness also introduces a new challenge absent from deterministic analyses: the final output may contain alarms that are individually plausible yet mutually inconsistent, because marginal probabilities do not guarantee joint satisfiability. As a result, developers may spend effort investigating combinations of alarms that can never co-occur in any possible world. We address this problem by formalizing such inconsistencies as minimal unsatisfiable subsets (MUSes) and introducing PPProbe, a conflict extractor specialized for probabilistic Datalog analyses. Rather than improving MUS enumeration in general, PPProbe exploits the structure of Datalog derivation graphs to guide the search toward likely conflicts and prune the search space through bottom-up UNSAT inference. We evaluate PPProbe on 70 benchmarks from power side-channel analysis, data race detection, semantic diffing, and Bayesian-network inference. The results show that PPProbe achieves 2.5–24× higher throughput than state-of-the-art MUS enumerators, and that the conflicts it identifies yield a conservative estimate of false-positive reduction, filtering out an average of 47.7% of mutually inconsistent alarms.


## 9. Formal Verification-Integrated Reinforcement Learning for Automated ORM Schema Synthesis

**Authors:** Md Rashedul Hasan (University of Nebraska-Lincoln, USA), Hamid Bagheri (University of Nebraska-Lincoln, USA)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837501

**中文总结:** 提出 ReinforceORM，用 RL 搜索 ORM 映射策略并以 Alloy 有界验证保证结构/语义，多目标优化插入、查询与存储；15 个真实系统上找回超 80% Pareto 最优配置，相对 Hibernate 等提升约 18 倍，运行时间与内存较规格搜索降四至五个数量级。

**Abstract:** Object-relational mapping (ORM) frameworks are widely used to bridge object-oriented models and relational databases, but conventional tools generate only single point solutions and often miss optimal trade-offs between performance and storage consumption. Exhaustive tradespace analysis can discover Pareto-optimal database designs, but it is computationally prohibitive for realistic systems. This paper introduces ReinforceORM, an automated and scalable framework that formulates ORM schema synthesis as a multi-objective optimization problem solved via reinforcement learning with formal verification. Our approach integrates multiple RL algorithms to efficiently search the vast space of mapping strategies, balancing insertion time, query performance, and storage consumption, while employing Alloy-based formal analysis to provide bounded verification of structural and semantic correctness in generated schemas. Evaluation across fifteen diverse, real-world software systems shows that ReinforceORM identifies over 80% of ground-truth Pareto-optimal ORM configurations—an 18-fold improvement over leading ORM frameworks such as Hibernate, Django ORM, SQLAlchemy, and Entity Framework. Compared to state-of-the-art specification-driven search, ReinforceORM reduces analysis runtime and memory usage by four and five orders of magnitude, respectively, while maintaining near-optimal solution quality.


## 10. From Thread to Pool: Modeling and Static Detection of Thread Pool Misuses in Java Programs

**Authors:** Baoquan Cui (Institute of Software at Chinese Academy of Sciences, Beijing, China), Yucheng Qiu (Hangzhou Institute for Advanced Study at University of Chinese Academy of Sciences, Hangzhou, China), Rui Han (Hangzhou Institute for Advanced Study at University of Chinese Academy of Sciences, Hangzhou, China), Hang Gao (Institute of Software at Chinese Academy of Sciences, Beijing, China / University of Chinese Academy of Sciences, China), Jian Zhang (Institute of Software at Chinese Academy of Sciences, Beijing, China / University of Chinese Academy of Sciences, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837508

**中文总结:** 提出七类 Java ExecutorService/线程池管理误用分类并形式化为资源管理模型，实现静态分析框架 PoolGuard；在基准与大规模开源项目中优于 SpotBugs、Infer 等工具，发现 50 个未知问题（24 个已修复或确认）。

**Abstract:** Asynchronous programming is fundamental to modern software performance, and Java ExecutorService-based executors have become a standard abstraction for managing concurrent tasks. While existing research has extensively studied traditional concurrency bugs, management misuses of executors remain under-analyzed. These defects arise not from the business logic of asynchronous tasks, but from how executors are configured, used, and terminated. We present a taxonomy of seven executor-management misuse patterns and formalize them using a resource-management model. Based on this, we develop PoolGuard, a static analysis framework for detecting both executor-generic lifecycle/result-handling defects and ThreadPoolExecutor-specific configuration misuses. Extensive evaluation on a benchmark suite with real-world defects shows that PoolGuard is better than specialized async detectors as well as general-purpose analyzers such as SpotBugs and Infer. Applying PoolGuard to large-scale open-source systems, we identified 50 previously unknown issues, 24 of which have already been fixed or confirmed by developers, demonstrating the practical value of semantic analysis for executor-management defects.


## 11. Fully Automating Template Polyhedral Analysis by Leveraging LLMs

**Authors:** Renjie Huang (National University of Defense Technology, China), Liqian Chen (National University of Defense Technology, China), Hongfei Fu (Shanghai University of Finance and Economics, China), Banghu Yin (National University of Defense Technology, China), Dengping Wei (National University of Defense Technology, China), Ji Wang (National University of Defense Technology, China)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837472

**中文总结:** 提出基于 LLM 的自底向上方法自动生成 template polyhedra 线性模板，并实现 IKOSplus，在 IKOS 上支持全自动上下文敏感与过程间 template polyhedral 分析；在多种基准与真实程序上平衡精度与可扩展性。

**Abstract:** Abstract interpretation provides a generic framework to design static analysis, and has been widely applied in analysis of real-world programs. The scalability and precision of these analyses depend largely on the chosen abstract domain. The template polyhedra domain is well-known for offering a compelling trade-off between scalability and precision. However, designing effective templates currently requires intensive manual effort and domain expertise. In this paper, we propose a bottom-up approach based on Large Language Models (LLMs) to automatically generate linear templates for the template polyhedral analysis. By leveraging the advanced code comprehension capabilities of LLMs, our approach automatically generates highly relevant templates. Based on this approach, we have implemented IKOSplus, a program analyzer supporting fully automated context-sensitive and interprocedural template polyhedral analysis, on top of IKOS. We evaluated IKOSplus on a variety of small-scale benchmark programs and complex real-world programs. Experimental results demonstrate that IKOSplus effectively balances analytical precision and scalability in the template polyhedral analysis.


## 12. Generating Loop Invariants for Deductive Verification using Iterator Profiles

**Authors:** Keisuke Nishimura (Inria, France), Jean-Pierre Lozi (Inria, France), Julia Lawall (Inria, France)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837530

**中文总结:** 引入 iterator profile 作为迭代模式的循环不变式模板，结合循环体自动分析实现工具 LoopAnnotator；在既有基准与 Linux 内核 245 个循环上超过 70% 成功生成不变式。

**Abstract:** Recent advances in deductive verification have gradually made it practical to verify the functional correctness of real-world software. However, creating loop invariants still requires manual effort. We propose to reduce this burden by automatically generating invariants. In the context of generating invariants for real-world software, the key requirements are to support diverse index iteration patterns and to capture precise information about loop behaviors. In this paper, we introduce the idea of an iterator profile : a loop-invariant template for an iteration pattern. Once a user writes a profile, it can be reused for any iterator-based loop that shares the same iteration pattern. We present LoopAnnotator, a tool that generates loop invariants for iterator-based loops by combining an iterator profile with the result of automatic program analysis of the loop body. LoopAnnotator successfully generates invariants for more than 70% of the loops in benchmarks from prior work and 245 loops extracted from the Linux kernel.


## 13. GPU-Accelerated Belief Propagation for Program Analysis

**Authors:** Haoyu Feng (Peking University, China), Xin Zhang (Peking University, China)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834444

**中文总结:** 提出 GPU 加速信念传播框架 FastLBP，支持灵活更新策略与逻辑约束的程序分析。在 SmartFL 与 BINGO 上分别获得平均 17.42× 与 2.82× 加速，且保持精度。

**Abstract:** Belief Propagation (BP) is a widely used approximate inference algorithm in probabilistic graphical models (PGMs), but it is computationally expensive when applied to large-scale program analysis. Existing GPU-based approaches are unable to support flexible update strategies and have yet to integrate logical constraints with GPU acceleration, leading to challenges in both generality and efficiency. We present FastLBP, a GPU-accelerated BP framework for program analysis. We propose a unified representation for specifying flexible update strategies required in program analysis, along with a dependency analysis algorithm to enable parallel execution. Furthermore, we implement BP with local structures on GPUs by assigning individual threads to message computations and utilizing a memory-efficient representation. Experiments on SmartFL and Bingo show that FastLBP achieves average speedups of 17.42× and 2.82× over CPU-based approaches on SmartFL and Bingo, respectively, and 6.14× over the GPU-based approach on SmartFL, while preserving accuracy. Moreover, FastLBP supports update strategies that existing GPU-based approaches cannot support, demonstrating its improved generality for real-world program analysis.


## 14. IncSFS: Incremental Full-Sparse Flow-Sensitive Pointer Analysis for C/C++

**Authors:** Kunlin Liu (National University of Defense Technology, China), Zhenbang Chen (National University of Defense Technology, China), Piyi Zu (National University of Defense Technology, China), Yide Du (National University of Defense Technology, China), Ji Wang (National University of Defense Technology, China)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837496

**中文总结:** 提出首个 C/C++ 增量全稀疏流敏感指针分析 IncSFS：约束图 SCC 检测与 points-to 增减交错传播，支持单遍内删插代码；六大真实项目平均较全量流敏感分析加速 9.60×、较传统增量 5.84×。

**Abstract:** Pointer analysis is the fundamental technique for compiler optimization and program analysis. Flow sensitive pointer analysis provides high precision but hard to scale to large-size projects. Tailored for rapid iteration scenarios where software evolves continuously, we introduce IncSFS, the first incremental full-sparse flow-sensitive pointer analysis algorithm for C/C++ programs. The algorithm contains two main steps. It first transforms the value-flow graph of a program into a constraint graph, on which a strongly-connected component detection is performed to ensure precision. It then propagates increases and decreases in points-to set in an interleaving manner to support both code deletion and insertion within a single analysis pass. IncSFS is guaranteed to terminate and compute the least fixed point when point-to relation during the analysis is object-acyclic. Experimental results on six large-scale real-world projects show that IncSFS is both precise and efficient, achieving average speedups of 9.60 x over full flow-sensitive pointer analysis and of 5.84 x over the traditional reset-recompute incremental approach. Furthermore, IncSFS improves efficiency by 15.8% compared with state-of-the-art incremental pointer analysis algorithms that also propagate changes in points-to sets.


## 15. Inferring the Shape of Data Frames in R Programs using Abstract Interpretation

**Authors:** Oliver Gerstl (Ulm University, Germany), Florian Sihler (Ulm University, Germany), Matthias Tichy (Ulm University, Germany)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834445

**中文总结:** 用抽象解释推断 R 程序中 data frame 的列名与行列规模形状；78 个可执行脚本上保持 sound，33314 脚本大规模实验中推断出具体形状约束的比例显著，并发现 40 个潜在非法访问脚本。

**Abstract:** Data frames are a fundamental data structure in many data analysis tasks and are widely used in programming languages like R. Due to their omnipresence in data analysis, there are many functions that operate on their shape and content, for example, to clean and transform study data. However, languages like R do not offer static guarantees on data frames making it difficult to reason about their shape at a specific point in the program. In this paper, we present a novel static analysis to infer the shape of data frames in R programs using abstract interpretation by tracking the ensured and potential column names, as well as the potential number of columns and rows. For this, we use a reduced product domain and define abstract semantics for the most commonly used data frame operations, such as mutating, filtering, and subsetting. We evaluate the correctness and accuracy of our analysis on a selection of 78 executable real-world R scripts achieving empirical evidence for soundness by never under-approximating the data frame shape. Additionally, we demonstrate the ability of our analysis to infer the shape of data frames on a large dataset of 33,314 real-world R scripts by inferring concrete shape constraints for 42.1 % and exact shapes for 0.9 % of the data frame operations, improving to 58.7 % and 4.2 % if all datasets read in these scripts are available to our analysis. Using the inferred data frame shapes, we identified 40 real-world R scripts containing potential invalid data frame accesses. This shows the potential of our analysis to significantly support researchers in using data frames in data analysis.


## 16. Large Language Model Enabled Symbolic Execution for Automated Functional Analysis

**Authors:** Meixi Liu (National University of Defense Technology, China), Zhenbang Chen (National University of Defense Technology, China), Xudong Wang (National University of Defense Technology, China), Ziran He (National University of Defense Technology, China), Jiachen Gu (National University of Defense Technology, China), Minghui Chen (National University of Defense Technology, China), Lei Wang (National University of Defense Technology, China), Wei Dong (National University of Defense Technology, China)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837524

**中文总结:** FuSE 用 LLM 为符号执行路径标注功能描述与前后条件，基于 UnitTestBot 在 C/C++/Java/Python 上标注成功率 87%–98%；用户研究中多识别 21.67% 功能缺陷、功能覆盖 +15.83%。

**Abstract:** Symbolic execution shows promise in automated program analysis by systematically exploring the path space of the program. However, due to the inherent limitations of program analysis techniques, symbolic execution cannot understand the program’s functionality, which hinders its application in functional analysis and defect detection. This paper introduces FuSE, a method that enhances symbolic execution with Large Language Models (LLMs) to automatically annotate program paths with functional specifications. A program path is annotated with a natural language description of its functionality, a precondition, and a postcondition. Our method significantly reduces the effort required for functional testing and defect detection. Based on UnitTestBot, FuSE can successfully annotate functional specifications for C, C++, Java, and Python programs, with success rates of 98.2%, 95.52%, 87%, and 95.37%, respectively. In our user study with professional developers and testers, FuSE helps users identify 21.67% more functional defects and improves functional coverage by 15.83%, demonstrating its practical utility.


## 17. Learning the Lexical Structure of Black-Box Systems by Parsing Systematic String Edit Mutations

**Authors:** Moeketsi Raselimo (Humboldt University of Berlin, Germany), Lars Grunske (Humboldt University of Berlin, Germany), Bernd Fischer (Stellenbosch University, South Africa)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834391

**中文总结:** 通过系统字符串编辑变异构造 membership query，从黑盒系统正例学习词法 token；在 TinyC、JSON、C 等多语言上与 oracle lexer 高度一致，并显著提升 Kedavra 学 cJSON 文法的 F1（0.93→1.00）。

**Abstract:** We describe and evaluate an approach to learn the lexical structure of  
black-box systems from a set of positive training examples. Our core idea is  
to use the  
system as oracle for repeated membership queries  
which we construct by systematically mutating the training examples using  
different string edit operations. We then learn the elements of the lexical structure by  
generalizing from the oracle responses to the mutated training examples. We have applied this  
approach to several  
systems with target languages of varying complexity, such as TinyC, JSON, AMPL,  
Modula-2, Oberon, Zig, or C.  
We show that the learned tokens are similar, and in many cases  
identical, to those of the oracle lexers. Their inspection can  
indicate where the systems under test deviate from the lexical structure of  
their respective target languages; the learned tokens can thus serve as precise test oracles for lexers.  
We show that the segmentations induced by lexing the validation sets with the  
learned and oracle lexers, respectively, are identical in many cases and that  
the non-identical parts affect on average between zero and about  
15 percent of the characters. We finally demonstrate that using the learned tokens substantially improves the  
quality of the context-free grammar that the state-of-the-art grammar learner  
Kedavra learns for cJSON, increasing the average F1-score of the grammars  
learned in five runs from 0.93 to 1.00.


## 18. Leveraging System-Level Observations to Inform Bayesian Learning of Model Parameters for Quantitative Verification

**Authors:** Simos Gerasimou (Cyprus University of Technology, Cyprus), Xingyu Zhao (Wuhan University, China / University of Warwick, UK)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837529

**中文总结:** EPIK 用可观测的系统级性质（而非形式模型转移参数） elicit 贝叶斯先验，双目标优化未知转移分布并嵌入定量验证；多类真实案例变体上验证有效性与泛化性。

**Abstract:** Combining Bayesian learning and quantitative verification is a powerful toolset for analysing key quantitative properties of software systems, like reliability and response time. However, the accuracy and robustness of verification results strongly depend on the prior knowledge (PK) underlying Bayesian inference. This knowledge reflects original beliefs about the probability of events and typically depends on domain expertise. Using inaccurate or uninformative PK can negatively affect quantitative analysis, yielding incorrect verification results. Our EPIK approach tackles this important challenge by eliciting and embedding PK in quantitative verification equipped with Bayesian estimators. Unlike existing approaches that require PK on formal model transition parameters, EPIK leverages system-level properties that are directly observable and are linked to real-world semantics. EPIK formulates a twofold optimisation problem to derive the distributions of unknown transition parameters and then embeds these distributions to verify new or difficult-to-measure (elusive) properties. The detailed experimental evaluation using multiple variants of real-world case studies and diverse EPIK instantiations shows its effectiveness, flexibility and generality.


## 19. Maximal Format-Free Data Repair

**Authors:** Zijian Luo (University of Sydney, Australia), Xi Wu (University of Sydney, Australia), Hong Jin Kang (University of Sydney, Australia), Alan Fekete (University of Sydney, Australia), Rahul Gopinath (University of Sydney, Australia)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834354

**中文总结:** 提出无格式规格的最优数据修复算法 βMAX，在示例数据意义下最大化恢复、最小化 parser 约束；修复 corrupt 记录成功率 83%、为 eREPAIR 的 1.77×，oracle 调用少 27.7×。

**Abstract:** Modern data-processing pipelines rely on input records conforming to strict format specifications. In practice, however, data corruption can occur at numerous stages including data-entry error, corruption during input processing and retransmission, inconsistent formatting, and incompatible specifications. Such corrupted data can result in loss of records, reducing the accuracy of processing. Rather than discarding corrupted records and losing valuable information, one can attempt to repair the data. Data-repair solutions such as regular expression based repair and error-correcting parsers require a specification to perform structural repairs. Specification-free techniques such as ddmax and eREPAIR are limited in repair operations, repair location, and require specific parser properties that are often unavailable. To tackle this challenge, we introduce βMAX, a novel format-free data repair algorithm optimal with respect to the provided example data, with maximal data-recovery and minimal parser constraints. Despite requiring less information than eREPAIR, βMAX repairs 83% of all corrupt records—1.77× the rate achieved by eREPAIR—while using 27.7× fewer oracle calls.


## 20. Mining Tactics for Automated Theorem Proving

**Authors:** Jian Fang (Ministry of Education, China / Peking University, China), Yixun Yao (Ministry of Education, China / Peking University, China), Yingfei Xiong (Ministry of Education, China / Peking University, China / Zhongguancun Laboratory, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837528

**中文总结:** 提出 LLM2Ltac：用 LLM 从形式化证明语料中挖掘并形式化为可复用 Ltac 策略，经校验后注入 Rocq 符号证明器而非端到端推理；在 CompCert 等四个项目上使 CoqHammer 多证 23.87% 定理，与 Claude Code 联用时总证明量再增 9.90%。

**Abstract:** Automated theorem proving is essential for the formal verification of safety-critical systems. As the corpus of formal proofs grows, a natural paradigm is to learn from existing proofs. However, current learning-based approaches predominantly train Large Language Models (LLMs) as end-to-end provers, which yields resource-intensive, opaque systems. Conversely, while traditional symbolic provers are computationally efficient, how to automatically improve these solvers from data remains an open challenge. This paper bridges this gap by proposing LLM2Ltac, a novel approach that leverages the reasoning power of LLMs not as end-to-end provers, but as intelligent synthesizers to mine purely symbolic tactics from data. Given a corpus of formal proofs, LLM2Ltac asks an LLM to identify latent proof strategies and formalize them into reusable tactics. These tactics are verified for validity and generalizability, and finally integrated into symbolic provers to enhance their automated proving capabilities without the runtime cost of LLMs. We implement LLM2Ltac on Rocq 8.20.0 and mine tactics from 11,725 theorems in the standard library. We evaluate our approach on 6,199 theorems from four large real-world verification projects, namely, CompCert, Coq-Art, Ext-Lib, and VFA. Results show that the mined tactics improve CoqHammer to prove 23.87% more theorems, and when integrating the improved CoqHammer with Claude Code, the overall proved theorems increases by 9.90%, indicating the effectiveness of LLM2Ltac.


## 21. MiniPoly: Automatic Extraction of Efficient JavaScript Polyfill from Language Specification

**Authors:** Jungwoong Kim (Korea University, Republic of Korea), Youngmin Cho (Korea University, Republic of Korea), Jihyeok Park (Korea University, Republic of Korea)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837549

**中文总结:** 提出首个从 ECMA-262 规范自动编译生成 polyfill 的 MiniPoly：静态分析解析 completion records 并映射为 JavaScript，再用重写规则优化瓶颈；为 ES2025 生成 89 个内置 API 的 polyfill，规范符合度优于 core-js/es-shims 且性能可竞争。

**Abstract:** A polyfill is a JavaScript implementation of built-in APIs for older execution environments lacking native support. Because developers rely on them to run modern features everywhere, strict conformity to the official language specification (ECMA-262) is crucial. However, manual implementation remains the industry standard; this process is labor-intensive, inherently error-prone, and frequently leads to spec-miscompliance bugs in production. To address this, we present MiniPoly, the first compilation framework to automatically extract correct and optimized polyfills directly from the ECMA-262 specification. To ensure correct generation, MiniPoly employs a static analysis that resolves the specification’s internal control-flow representations (i.e., completion records) and translates them into equivalent JavaScript constructs. Furthermore, it utilizes rewrite rules to apply user-defined optimization patterns, replacing algorithmic bottlenecks in the specification with highly efficient implementations. Evaluation shows that MiniPoly successfully generates polyfills for 89 built-in APIs in ECMAScript 2025 (ES2025) using 17 user-defined rewrite rules. It produces a more spec-compliant polyfill than production-standard libraries like core-js and es-shims with a competitive performance profile. Additionally, we demonstrate that MiniPoly can generate polyfills even for the next draft release of ECMA-262 and early-stage proposals, highlighting its potential to future-proof development.


## 22. On the Effects of Customized Configurations of Static Code Analysis Tools: A Prospective Cohort Study of SonarQube Cloud

**Authors:** Sabato Nocera (University of Salerno, Italy), Sira Vegas (Polytechnic University of Madrid, Spain), Giuseppe Scanniello (University of Salerno, Italy)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834408

**中文总结:** 对 230 个 GitHub 开源项目做 SonarQube Cloud quality gate 定制的前瞻性队列研究；仅观察到较宽松安全配置对安全指标有显著因果效应，可靠性与可维护性定制影响不显著，提示开发者可能更优先响应“可达成”的安全门槛。

**Abstract:** Static Code Analysis (SCA) tools are used to detect issues and enforce code quality standards in software projects. SCA tools like SonarQube Cloud provide predefined configurations that project owners can customize depending on the goal of the project at hand. One such configuration is the quality gate, which defines the set of conditions that source code must satisfy to pass automated quality checks during software development. This paper investigates the impact of customizing SonarQube Cloud quality gates on security, reliability, and maintainability. We employ a prospective cohort study design to explore causal relationships using observational data. We track 230 open-source GitHub projects forward in time, monitoring transitions in configurations to ensure consistent adherence to either customized or predefined ones. A significant effect was observed only for security under less strict configurations, suggesting that developers could be more motivated to fix security issues when the requirements are perceived as attainable. For reliability and maintainability customizations, we speculate that the lack of impact may stem from these quality attributes being perceived as less essential or pressing compared to security.


## 23. Orbis: Guiding Symbolic Execution Techniques to Maximize Option-Related Branch Coverage

**Authors:** Minjong Kim (Sungkyunkwan University, Republic of Korea), Sungjae Hwang (Sungkyunkwan University, Republic of Korea), Sooyoung Cha (Sungkyunkwan University, Republic of Korea)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837526

**中文总结:** 提出 Orbis，从动态迹识别程序 option 及关联分支并随机组合 option 参数引导符号执行，兼顾潜力和 SMT 调用削减；在 15 个 C 程序上与四种 SOTA 结合后 option 分支覆盖提升至 323%、总分支覆盖 +112.1%，平均多发现 5 个独有 bug。

**Abstract:** We present Orbis, a complementary approach that guides symbolic execution techniques toward maximizing option-related branch (OB) coverage. Although state-of-the-art symbolic execution techniques have substantially improved code coverage and bug detection, existing techniques often fail to exercise core program functionalities, which are frequently exposed as program options. To quantify this limitation, we evaluate how effectively current techniques cover option-related branches and find that they reach only 8.0% of the targeted OBs, which are accessible only through specific options. Orbis overcomes this challenge by systematically guiding symbolic execution to improve OB coverage. For a given program, Orbis automatically identifies all defined options and determines their associated branches by analyzing dynamic execution traces. It then iteratively constructs target option arguments by stochastically combining identified options according to their estimated potential, directs symbolic execution to explore states influenced by these arguments, and refines their potential while simultaneously reducing SMT-solver invocations using data accumulated during symbolic execution. Experimental results on 15 open-source C programs show that integrating Orbis with four independent state-of-the-art techniques significantly increases OB coverage to 323.0%, boosts total branch coverage by 112.1%, and detects five additional unique bugs on average compared to the standalone techniques.


## 24. PL4SA: Optimized Partial Library Selection for Efficient Static Analysis

**Authors:** Guohao Feng (Nanjing University, China), Yifei Lu (Nanjing University, China), Minxue Pan (Nanjing University, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834431

**中文总结:** 提出 PL4SA，用细粒度全程序 points-to 与 extended pointers 渐进扩展，按与分析相关性排序仅纳入必要库方法；仅含约 12%–17% 库方法即相对全程序分析获 24.6×/9.0× 加速且变量类型与空指针分析 recall 99%、precision 100%。

**Abstract:** With the rapid advancements in modern software engineering practices, software applications have become increasingly dependent on external libraries, making the choice between whole-program and application-only analysis more critical: the former often leads to timeouts due to high computational overhead, while the latter risks missing library-induced bugs. Recent research has explored a compromise path, i.e., partial inclusion of libraries to balance analysis efficiency and recall. However, achieving a more precise relevance analysis that enables a more balanced and accurate library selection while minimizing the associated overhead remains a significant challenge. This paper proposes PL4SA, a novel partial library selection approach that establishes precise relevance between client analyses and library methods using fine-grained whole-program points-to information. The key point of PL4SA lies in integrating points-to analysis with the partial library selection process in a progressively expanding manner. During this process, pointers are ranked according to their relevance to the client analysis; in each iteration, the most relevant pointer as well as its corresponding library is selected, while pointers dependent on the selected pointer are further expanded to reveal their points-to information. To support this analysis, extended pointers , a pointer-based abstraction that summarizes additional information flows into/out of method invocations and array accesses, serve as anchors for the progressive expansion of points-to information. Furthermore, PL4SA organizes this analysis in three steps, leveraging summarization techniques to enable the reuse of time-critical intra-procedural points-to analysis results within libraries across different projects, due to the inherent stability of library code. Collectively, these design choices contribute to PL4SA’s high efficiency. Our experimental results demonstrate that by including only 12% and 17% library methods, PL4SA achieves 24.6x, 9.0x speedup, and 99.0% recall, and both 100% precision for variable-type analysis and null-pointer analysis compared to whole-program analysis, significantly outperforming existing baselines.


## 25. Precise and Efficient Static Data Race Detection

**Authors:** Pei Wang (Tsinghua University, China / Key Laboratory for Information System Security, China / Beijing National Research Center for Information Science and Technology, China), Zhihang Sun (Tsinghua University, China / Key Laboratory for Information System Security, China / Beijing National Research Center for Information Science and Technology, China), Fei He (Tsinghua University, China / Key Laboratory for Information System Security, China / Beijing National Research Center for Information Science and Technology, China)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837438

**中文总结:** 基于事件级顺序约束精确建模数据竞争且无需额外插桩，集成并发验证框架并增强 ordering 理论求解与 value-critical 事件编码优化；原型 Deagle-DR 与 Dartagnan、Ugemcutter 等 SOTA 工具对比显示竞争力。

**Abstract:** Data races pose a serious threat to the correctness of concurrent programs. Traditional model-checking-based race detection techniques typically encode race detection as assertion verification, but this introduces substantial overhead due to numerous auxiliary variables and statements. In this paper, we present a precise modeling of data races based on event-level ordering constraints, which avoids any instrumentation while capturing the exact semantics and covering all potential race occurrences within the given bounded scope. We integrate it into a concurrent program verification framework and prove its correctness. Moreover, we enhance the existing theory solvers for ordering consistency theory with two new components, enabling effective reasoning about data races. Finally, we introduce an encoding optimization that leverages the novel concept of value-critical events to eliminate redundant value constraints. We implement our approach in a prototype tool, Deagle-DR, and compare it against state-of-the-art tools, including Dartagnan, Ugemcutter, Cseq-DR, LaDR, and Iekke. Experiments show that our approach is competitive with state-of-the-art methods.


## 26. Quick Bug Detection through Black-Box Checking: A Systematic Evaluation

**Authors:** Bram Pellen (Radboud University, Netherlands), María Belén Rodríguez (University of Twente, Netherlands), Frits Vaandrager (Radboud University, Netherlands), Petra van den Bos (University of Twente, Netherlands)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834347

**中文总结:** 对 Peled 等提出的 black-box checking（BBC，对每个假设模型做模型检测）在 77 个真实协议/控制器模型上首次系统评估；全模型可学时时 BBC 用约 3% 查询即可发现规约违背，RERS 2019 LTL 工业基准检出 96% 违规，深 bug 发现优于常规模型测试。

**Abstract:** Combinations of active automata learning, model-based testing and model checking have been successfully used in numerous applications, e.g., for spotting bugs in implementations of major network protocols and to support refactoring of embedded controllers. However, in the large majority of these applications, model checking is only used at the very end, when no counterexample can be found anymore for the latest hypothesis model. This contrasts with the original proposal of black-box checking (BBC) by Peled, Vardi & Yannakakis, which applies model checking for all hypotheses, also the intermediate ones. In this article, we present the first systematic evaluation of the ability of BBC to find bugs quickly, based on 77 benchmark models from real protocol implementations and controllers for which specifications of safety properties are available. Our main finding are: (a) In cases where the full model can be learned, BBC detects violations of the specifications with just 3% of the queries needed by an approach in which model checking is only used for the full model. (b) Even when the full model cannot be learned, BBC is still able to detect many violations of the specification. In particular, BBC manages to detect 96% of the safety property violations in the challenging RERS 2019 industrial LTL benchmarks. (c) Our results also confirm that BBC is way more effective than existing model-based testing algorithms in finding deep bugs in implementations.


## 27. RFC2TLA+: Extracting and Verifying Formal Models from RFC Documents using Continuous LLM Feedback

**Authors:** Guozhen Ding (University of Toronto, Canada), Kexin Li (University of Toronto, Canada), Ilya Grishchenko (University of Toronto, Canada), David Lie (University of Toronto, Canada)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837453

**中文总结:** 提出 RFC2TLA+ 三阶段流水线（状态/转移/不变式），以细粒度工具调用、轻量校验与连续反馈约束 LLM，将 RFC 提取为 CFSM 并确定性译为 TLA+ 用 TLC 验证；在 14 个 RFC 上模型更完整，并可检测注入故障，合成 RFC 进一步缓解记忆化质疑。

**Abstract:** Extracting natural-language protocol specifications such as Requests for Comments (RFCs) into formally verifiable models is a challenging and labor-intensive process that requires significant expertise. Recent advances in large language models (LLMs) and agents show promise in automating this task. However, existing automated approaches suffer from insufficient structural consistency, hallucinations, and limited scalability. Moreover, the ability to pass such automatically extracted models into formal verification tools such as model checkers has not been demonstrated. We present RFC2TLA+, a three-stage pipeline for automatically extracting RFCs into automatically verifiable models. RFC2TLA+ achieves this by providing fine-grain and continuous feedback to the LLM throughout the extraction process. It decomposes the extraction process into three passes—states, transitions, and invariants—while constraining LLM generation through fine-grained tool calls, lightweight validation, and iterative feedback. This design enables early error detection and correction, mitigating hallucinations and preventing syntactic and semantic inconsistencies. The resulting communicating finite-state machines (CFSMs) are deterministically translated into TLA + and verified using the TLC model checker. We evaluate RFC2TLA+ on a benchmark of 14 RFCs and their accompanying human-crafted FSMs and show that it generates more complete models than the baseline. In addition, our tool extracts invariants, enabling a model checker to detect injected faults. To minimize the effects of LLM memorization, we additionally generate synthetic RFCs and evaluate the tool on them, demonstrating its effectiveness in both model extraction and error detection.


## 28. Safe Multi-site Binary Instrumentation of Running x86-64 Programs

**Authors:** Jihun Baek (UNIST, Republic of Korea), Sanghoon Han (UNIST, Republic of Korea), Hyungon Moon (UNIST, Republic of Korea)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837494

**中文总结:** 提出 DIBE 运行时框架：管理进程离线解析多站点补丁与 trampoline 元数据，目标进程按序重放 E9Patch 多站点改写，77%–90% 覆写用硬件原子完成；在 SPEC CPU2006、Nginx 与 Chrome 渲染进程上覆盖近全、几何平均开销 <0.5%，Nginx 负载下零 trap。

**Abstract:** Applying binary instrumentation to a running x86-64 process is difficult because variable-length instructions and weak alignment guarantees prevent safe in-place code modification under concurrent execution. Existing run-time approaches either trap concurrent threads on every overwrite or require global synchronization, limiting scalability. This paper presents DIBE, a run-time binary editing framework that safely instruments running x86-64 programs without trapping in the common case.  
An admin process resolves all instrumentation decisions, including multi-site patching tactics and trampoline placement, and exports them as metadata. A lightweight runtime inside the target process replays these edits, safely activating E9Patch's multi-site rewriting tactics on the live process by applying their dependent overwrites in an order that keeps every intermediate program state correct under concurrent execution, a guarantee that single-site punning and offline rewriting do not provide.  
It applies 77-90% of overwrites using hardware atomic primitives invisible to concurrent threads, with a trap-based fallback only for the remaining cross-boundary cases. We evaluate DIBE on 28 SPEC CPU2006 benchmarks and a multi-process Nginx server, and demonstrate it at browser scale on a running Chrome renderer and as a live memory-safety checker. DIBE matches static E9Patch on both instrumentation coverage (near-complete) and execution time overhead (within 0.5% at the geometric mean), keeps per-instruction overwrite latency sub-microsecond, and records zero trap hits across all Nginx configurations under sustained load.


## 29. SIMD-Accelerated Sparse Bit-Vectors for Pointer Analysis

**Authors:** Zhaoyang Tan (Zhejiang University, China), Peisen Yao (Zhejiang University, China), Kui Ren (Zhejiang University, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837421

**中文总结:** 将稀疏位向量指针分析中的索引匹配 recast 为无分支 SIMD 原语，并行扫描 allocation-site 索引并掩码更新块；在 12 个程序上相对传统稀疏位向量分析时间几何平均降 2.0×、峰值内存降 58%。

**Abstract:** Pointer analysis is a core component of program-analysis frameworks. Inclusion-based solvers repeatedly update points-to sets, and the resulting set operations frequently dominate end-to-end runtime. In existing sparse bit-vector representations, we find that the main cost is not bitmap arithmetic but irregular index matching: identifying allocation-site representatives shared by two operands before combining their corresponding blocks. We accelerate this kernel by recasting index matching as a branch-free SIMD primitive. The key is a sparse layout that stores allocation-site indices and their blocks in contiguous arrays, enabling parallel scans over indices and masked SIMD updates of blocks while preserving sparsity. We evaluate the technique on 12 real-world programs under both context-insensitive and context-sensitive variants. Compared to a conventional sparse bit-vector baseline, our approach reduces analysis time by up to 3.8× (geomean: 2.0×) and peak memory by up to 86% (geomean: 58%), with larger gains for more precise analyses. The improvements persist across alternative set representations and constraint solving strategies.


## 30. Sound and Efficient Statistical Model Checking for Probabilities and Bounded Rewards

**Authors:** Hao Bu (Ant Group, China / Zhejiang University, China), Lin Huang (Ant Group, China), Tao Wei (Ant Group, China), Jingyi Wang (Zhejiang University, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834371

**中文总结:** 为概率与有界期望奖励在绝对/相对误差点估计与区间估计六类问题给出既 sound 又高效的统计模型检验算法，并对奖励估计提出从概率算法 lifting 的三套新算法并形式证明 soundness。

**Abstract:** Statistical model checking estimates quantitative properties of stochastic systems, such as the probability that a given property holds and the expected rewards. Ideally, an estimation algorithm should be both sound (i.e. satisfying the given confidence bound) and efficient (i.e. using fewer simulations or producing narrower confidence intervals). However, many existing algorithms are either unsound (e.g. relying on asymptotic approximations like the central limit theorem) or inefficient (e.g. using conservative bounds like the Hoeffding bound). In this paper, we present sound and efficient algorithms for estimating probabilities and bounded expected rewards under three settings: point estimation with absolute error, point estimation with relative error, and interval estimation, yielding six problems in total. For estimating probabilities, we employ a hybrid strategy integrating two existing algorithms in the point estimation with absolute error setting. We adopt suitable existing algorithms in the other two settings. For estimating bounded expected rewards, the unknown distribution shape makes it challenging to design sound and efficient algorithms. To address this, we propose a lifting framework to lift the three algorithms for estimating probabilities to three new algorithms for estimating bounded expected rewards. We formally prove the soundness of the three lifted algorithms and demonstrate their efficiency through experiments.


## 31. VARIES: Verification Harness Synthesis and Efficient Scheduling for Unsoundness Detection in Rust Libraries

**Authors:** Huan Li (Zhejiang University, China), Xing Hu (Zhejiang University, China), Xin Xia (Zhejiang University, China / Hangzhou High-Tech Zone (Binjiang) Institute of Blockchain and Data Security, China), Xinyu Wang (Zhejiang University, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837450

**中文总结:** 提出基于 BMC 的 Varies，为 Rust 库 API 合成种子 harness 并经 mutator 扩展成树，以反馈驱动剪枝调度验证以检测 unsoundness；在 benchmark 上覆盖更多 crate 且误报低，在 crates.io 流行库中发现 10 个 crate 的未知 unsoundness（6 个已获维护者确认）。

**Abstract:** Rust provides strong compile-time safety guarantees, but unsafe code in real-world libraries can still introduce unsoundness bugs that may undermine this guarantee. Compared with prior work, 
bounded model checking (BMC) offers a promising direction by adapting formal verification to unsoundness detection. In practice, however, BMC requires harnesses that are tedious to construct, and many unsoundness bugs arise only under specific program states that a single harness may miss. To this end, we propose Varies, a BMC-based framework that treats unsoundness detection in Rust libraries as a joint problem of harness synthesis and budget-aware verification. During the synthesis stage, Varies builds seed harnesses for each target API and then expands them into derived harnesses through mutator injection. Over the resulting harness derivation tree, Varies applies feedback-driven pruning strategies to schedule verification efficiently. In our benchmark, Varies identifies defects involving target APIs in more evaluated crates than any baseline while maintaining a low false-positive rate. In a broader deployment on popular crates.io libraries, it identifies previously unknown unsoundness in 10 crates, with reports for 6 crates acknowledged by maintainers. The results indicate that stateful harness synthesis and feedback-driven scheduling can make BMC practical for targeted unsoundness detection in Rust libraries.


## 32. Verifier-in-the-Loop LLM Solving of Heap Constraints for Concolic Execution

**Authors:** Shaoran Xia (Fudan University, China), Leyi Cheng (Soochow University, China), Caihua Dong (Fudan University, China), Dongdong She (Hong Kong University of Science and Technology, China), Bo Wang (Beijing Jiaotong University, China), Xin Peng (Fudan University, China), Zhen Dong (Fudan University, China)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834410

**中文总结:** 提出 COHEC，将路径条件拆为 SMT 可解的原语部分与由 HCS 处理的堆约束，LLM 提议堆模型与初始化代码、可信验证器执行校验后再采纳；在 6750 个 Java API 上相对 JDart 显著增路径探索，相对 CONCOLLMIC 更高覆盖且时间与 token 成本更低。

**Abstract:** Concolic execution systematically explores program paths by solving symbolic constraints, but in object-oriented software its practical effectiveness is often limited by heap constraints over objects and heap structure, such as nullness, aliasing, runtime types, and field reachability. These constraints form a systematic bottleneck in real-world software because satisfying them requires constructing a concrete heap model rather than merely computing primitive valuations, which existing SMT-based concolic engines and symbolic heap techniques do not handle effectively. We present COHEC, a hybrid concolic architecture that decomposes each target path condition into a primitive component solved by an SMT solver and a heap component handled by a Heap Constraint Solver (HCS). Given extracted heap constraints, HCS uses an LLM to propose candidate heap models and initialization code, while a trusted verifier executes and verifies the generated code, admitting only models whose initialization code constructs states that satisfy all constraints and keeping the LLM outside the trusted computing base. We implement COHEC on top of JDart/JPF and evaluate it on 6,750 APIs from ten Java libraries, together with a stratified sample from commons-lang3 against the LLM-assisted baseline CONCOLLMIC. The results show that COHEC substantially improves path exploration and concrete valuation generation over native JDart, while achieving higher coverage than CONCOLLMIC at lower time and token cost. Overall, the findings indicate that treating heap constraint solving as verified heap model construction is a practical and effective way to extend concolic execution to the object-sensitive behaviors pervasive in modern software.

