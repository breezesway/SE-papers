# FSE 2026 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 17 papers

## 1. Accelerating Policy Synthesis in Large-Scale MDPs via Hierarchical Adaptive Refinement

**Authors:** Alexandros Evangelidis (University of York, UK), Gricel Vázquez (University of York, UK), Simos Gerasimou (Cyprus University of Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808203

**中文总结:** 提出面向大规模 MDP 的层次自适应精炼策略综合方法，仅在必要时动态精炼最脆弱区域以兼顾精度与效率，并形式证明合成策略在标准假设下近优；在至多约 100 万状态的案例上相对 PRISM 最高约 2× 加速。

**Abstract:** Software-intensive systems, such as software product lines and robotics, utilise Markov decision processes (MDPs) to capture uncertainty and analyse sequential decision-making problems. Despite the usefulness of conventional policy synthesis methods, they fail to scale to large state spaces. Our approach addresses this issue and accelerates policy synthesis in large MDPs by dynamically refining the MDP and iteratively selecting the most fragile MDP regions for refinement. This iterative procedure offers a balance between accuracy and efficiency, as refinement occurs only when necessary. We formally show that the composed policy is near-optimal under standard assumptions, with error bounded by the local solver tolerance and boundary mismatch. Across diverse case studies and MDPs up to 1M states, we demonstrate that our approach achieves up to 2x speedup over PRISM, offering a competitive solution for real-world policy synthesis in large MDPs.

## 2. Active Learning of Symbolic Automata for Reactive Programs via Dynamic Symbolic Mapper

**Authors:** Yoel Kim (Kyungpook National University), Yunja Choi (Kyungpook National University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808154

**中文总结:** 提出面向反应式程序的符号自动机主动学习扩展算法，引入粒度感知的动态符号 mapper，以谓词诱导的布尔抽象在教学时粗、学习时细地按需精炼；在 120 个基准上比现有方法多学到 32 个符号自动机，平均主动学习时间降低 55.6%。

**Abstract:** Active learning of formal behavior models from program source code is a powerful approach for a wide range of software analysis, validation, and verification tasks, including understanding system intent, automating specification mining, generating test oracles, and checking formal properties. Recent advances in active learning of symbolic automata, powered by program synthesis and model checking, provide both rich expressiveness and soundness guarantees for the learned models. However, these techniques often encounter significant performance bottlenecks, particularly when dealing with reactive programs that expose many program variables with large value domains.

This work introduces an extended active learning algorithm tailored for reactive programs by incorporating a novel dynamic symbolic mapper for learning symbolic automata. The mapper abstracts program behavior using learner-inferred predicates over program variables, encodes each valuation of these variables as a Boolean vector induced by these predicates (Boolean abstraction), and dynamically refines the abstraction in response to missing behaviors identified by the teacher. The mapper is granularity-aware: for teaching, it employs the coarsest predicates sufficient to expose missing behaviors, enabling broad exploration; for learning, it refines the abstraction only to the finest predicates necessary to resolve the uncovered gaps, trying to avoid refinements that could otherwise be triggered by coarse abstraction.

We evaluated our approach on 120 benchmarks, including SV-COMP tasks, Simulink model-driven programs, LeetCode problems, and representative embedded control software. The results show that our method learns 32 more symbolic automata and reduces the average active learning time by 55.6% compared to the state-of-the-art.

## 3. Agentic Verification of Software Systems

**Authors:** Haoxin Tu (National University of Singapore), Huan Zhao (National University of Singapore), Yahui Song (Standard Chartered Bank), Mehtab Zafar (National University of Singapore), Ruijie Meng (CISPA Helmholtz Center for Information Security), Abhik Roychoudhury (National University of Singapore)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808164

**中文总结:** 提出首个用于程序验证的 LLM agent，通过与 Rocq（原 Coq）交互获取上下文并在迭代精炼环中即时学习构造可机器检查的证明树；在 SV-COMP 与 Linux 内核模块上展示有效性，可与编码 agent 组成 generate-and-validate 闭环。

**Abstract:** Automatically generated code is gaining traction recently owing to prevalence of Large Language Models (LLMs). Further, the AlphaProof initiative has demonstrated the possibility of using AI for general mathematical reasoning. Reasoning about computer programs (software) can be accomplished via such general mathematical reasoning, however, it tends to be more structured. The structure of the program can be used to structure the proof as well as its intermediate lemmas.

In this work, we present a first LLM agent for conducting program verification. Unlike past works which rely on extensive training of LLMs on proof examples, our agent learns on-the-fly and improves the proof via an iterative refinement loop. The iterative improvement of the proof is achieved by the proof agent communicating with Rocq (formerly Coq) theorem prover to get additional context. The final result of the iteration is a proof derivation checked by the Rocq theorem prover. In this way, our proof construction involves autonomous collaboration between the proof agent and the theorem prover. This autonomy facilitates the search for proofs and decision-making in deciding on the structure of the proof tree.

Experimental evaluation on SV-COMP benchmarks, as well as on Linux kernel modules, shows promising efficacy in achieving agentic program verification. As automation in code generation becomes more widespread, we posit that our proof agent can be potentially integrated with AI coding agents to achieve a generate-and-validate loop, thereby moving closer to the vision of trusted automatic programming.

## 4. DiverFPS: Generating Diverse Solutions for Floating-Point SMT Formulas

**Authors:** Shuangyu Lyu (Beihang University), Chuan Luo (Beihang University), Ruizhi Shi (Beihang University), Zhuo Su (Beihang University), Chunming Hu (Beihang University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797081

**中文总结:** 提出 DiverFPS，经探索与剪枝两阶段为浮点 SMT 生成小而高 AST 覆盖的多样解集，并引入重启、上下文感知编码与覆盖驱动剪枝；在 QF_FP/QF_BVFP 基准上覆盖更多公式且解集可缩小最高 92.9%。

**Abstract:** Satisfiability Modulo Theories (SMT) is a fundamental technique underpinning a wide range of applications in software engineering and testing. Among various SMT theories, the theory of floating-point plays a crucial role in practical software systems, yet reasoning about floating-point constraints remains challenging. Although existing SMT solvers are capable of producing single solutions, many applications, particularly in software testing and verification, require diverse sets of solutions to adequately exercise program behaviors. While achieving high diversity is essential for exploring system behaviors, it is also important to limit the number of generated solutions, as overly large solution sets can considerably increase testing time and resource consumption, thereby diminishing efficiency. In this work, we propose DiverFPS, a novel floating-point SMT sampler designed to generate small solution sets that achieve high target abstract syntax tree (AST)-coverage, which is commonly regarded as the standard metric for assessing solution diversity in the SMT sampling domain. DiverFPS operates in two stages: an exploration stage that aims to achieve the target AST-coverage as fully as possible, and a pruning stage that prunes redundant solutions while preserving the target AST-coverage. We further introduce three novel techniques, namely solution-driven restart strategy, context-aware encoding technology, and coverage-driven pruning strategy, which enhance the performance of DiverFPS. Extensive experiments on publicly available SMT-LIB benchmarks for QF_FP and QF_BVFP logics demonstrate that DiverFPS outperforms state-of-the-art SMT samplers. It successfully achieves the target AST-coverage on a larger number of benchmarks, which existing samplers fail to reach, while producing solution sets that are up to 92.9% smaller, the former improving the effectiveness of practical software testing and verification, and the latter improving testing efficiency and reducing resource consumption. These results demonstrate that DiverFPS is a high-performing sampler for floating-point SMT sampling.

## 5. Event-B Agent: Towards LLM Agent for Formal Model Synthesis and Repair

**Authors:** Hongshu Wang (National University of Singapore), Xinyue Zuo (National University of Singapore), Yuhan Sun (East China Normal University), Qin Li (Shanghai Key Laboratory of Trustworthy Computing, East China Normal University), Yamine AIT AMEUR (IRIT - National Polytechnic Institute of Toulouse), Jin Song Dong (National University of Singapore)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808218

**中文总结:** 提出 Event-B Agent，从自然语言需求出发，结合模型检测与定理证明反馈迭代合成并修复 Event-B 模型；在多复杂度系统上端到端模型合成与修复显著优于基线，展示 LLM 智能体推动正确性构造的潜力。

**Abstract:** Building software that is correct by construction is a long-standing goal in software engineering, as it ensures that reliability is achieved during design rather than after deployment. Formal methods realize this vision by allowing system behavior and requirements to be expressed in mathematics, enabling correctness to be guaranteed through proofs and verification. However, the steep learning curve and demand for mathematical expertise hinder its widespread adoption. Large language models (LLMs) have recently shown promise in bridging this gap through autoformalization, but existing approaches often address isolated tasks, such as theorem proving or model synthesis verified by model checking. While valuable, these single-perspective efforts do not fully exploit the potential of a more comprehensive framework where models and proofs evolve together. To address this gap, we propose \textbf{Event-B Agent}, a novel framework inspired by the interleaved nature of software design. From natural language requirements, Event-B Agent constructs an initial model and iteratively adjusts it using feedback from model checking and theorem proving. Adjusting and refining the model, in turn, simplifies proof discharge that ensures correctness with respect to requirements. Evaluation across systems of varying complexity shows that Event-B Agent substantially outperforms baselines in end-to-end model synthesis and repair. These results show a promising direction into achieving correctness-by-construction through probabilistic approaches like LLM agents.

## 6. GPU-Accelerated Flow-Sensitive Pointer Analysis for C/C++ Programs

**Authors:** Jiaqi He (University of Alberta), Karim Ali (NYU Abu Dhabi)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808145

**中文总结:** 提出 GPA，用 GPU 加速流敏感指针分析，并以图神经网络预测每变量负载以动态平衡计算；在大型程序（≥275 KLOC）上相对 CPU SOTA 提速约 1.3×–14×，使高精度指针信息在工业规模代码上更可行。

**Abstract:** Flow-sensitive pointer analysis offers highly precise results that are essential for various security analyses, bug detection tools, and compiler optimizations. However, its high computational cost often leads to prohibitively long analysis times, especially for large, real-world programs. Despite decades of research, state-of-the-art algorithms still struggle to achieve acceptable performance at industrial scale, forcing developers to choose less precise alternatives.

To overcome these limitations, we present GPA a GPU-accelerated flow-sensitive pointer analysis for C/C++ programs. To maximize hardware utilization, GPA dynamically balances computation by combining the massive parallelism of GPUs with a graph neural network that predicts per-variable workloads. Compared to state-of-the-art CPU-based analyses, GPA improves runtime performance by a factor of $1.3\times$ to $14\times$ on large programs (i.e., ≥275~KLOC) without sacrificing precision. However, on most small programs (i.e., <100~KLOC) and some medium ones (i.e., 100–275~KLOC), traditional algorithms run faster due to the overhead of memory management on GPUs that GPA incurs. By making the computation of highly precise pointer information more tractable, GPA enables running analyses and developer tools that were previously infeasible on large codebases.

## 7. Improving Data Leakage Detection in Machine Learning Notebooks through Static Slicing and Structured LLM Prompts

**Authors:** Taha Draoui (University of Michigan-Flint), Mohamed Wiem Mkaouer (University of Michigan-Flint), Christian D. Newman (Rochester Institute of Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808199

**中文总结:** 提出将 Datalog 静态切片与结构化 LLM 提示结合的方法，抽取训练–评估相关的 provenance-aware 代码切片并逐步推理数据泄漏；在 Kaggle/GitHub notebook 基准上于预处理与重叠泄漏检测达到 SOTA，优于端到端提示与规则基线。

**Abstract:** Data leakage remains a critical yet under-diagnosed issue in machine learning pipelines, leading to inflated results and unreliable deployments. Existing detection approaches rely on static rules that often miss open-coded manipulations and fail to capture the diversity of real-world notebooks. This paper introduces a novel methodology that integrates static slicing with large language models (LLMs) to improve leakage detection. We use a Datalog-based static analysis that isolates compact, provenance-aware slices corresponding to model training and evaluation pairs, and we pair these with structured LLM prompts that guide step-by-step reasoning about potential leakage for each isolated slice. Evaluated on a curated benchmark of Python notebooks from Kaggle and GitHub, our approach achieves state-of-the-art performance in both preprocessing and overlap leakage detection, substantially outperforming end-to-end prompting and the rule-based baseline. Our findings highlight the effectiveness of combining program slicing and prompt engineering for data leakage detection and establish the first systematic LLM-based solution for detecting data leakage in machine learning code.

## 8. JavaScript Pointer Analysis with Adaptive Heap Abstraction

**Authors:** Wenyuan Xu (Aarhus University), Anders Møller (Aarhus University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797133

**中文总结:** 提出面向 JavaScript 的自适应堆抽象，在分析过程中发现并合并相似抽象对象以降低复杂度；在 96 个挑战程序上平均加速约 2×（最高 17×），精度损失可忽略。

**Abstract:** The conventional approach to represent objects in static program analysis is to use allocation-site abstraction. This design choice may lead to redundant computations when many abstract objects are similar. Existing mechanisms that aim to merge such objects are not effective for JavaScript. We propose a novel adaptive heap abstraction technique that during analysis discovers and merges similar abstract objects, thereby reducing the analysis complexity while preserving most of the precision.

The technique has been implemented in a state-of-the-art program analyzer for JavaScript. On a collection of 96 challenging programs, it yields a 2X speedup on average (up to 17X) with a negligible loss of precision. The experimental results also show the effects of various analysis configurations.

## 9. Large Language Models for Opaque Predicate Resolution: A Universal Control Flow Deobfuscation Framework

**Authors:** Xiao Chen, Wang Qiuyun (Institute of Information Engineering, Chinese Academy of Sciences;and University of Chinese Academy of Sciences), Wang Shuwei (Institute of Information Engineering, Chinese Academy of Sciences;and University of Chinese Academy of Sciences), Zhang Weize (Institute of Information Engineering, Chinese Academy of Sciences;and University of Chinese Academy of Sciences), Yuling Liu (Institute of Information Engineering, Chinese Academy of Sciences; School of Cyber Security, University of Chinese Academy of Sciences} \city{Beijing), Baoxu Liu (Institute of Information Engineering, Chinese Academy of Sciences), Jiang Zhengwei (Institute of Information Engineering, Chinese Academy of Sciences;and University of Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808099

**中文总结:** 提出结合 LLM 与反编译代码的通用控制流去混淆框架，形式化任务并适配多种混淆的谓词关系推断；在 780 个采用 13 种混淆的二进制上平均降低圈复杂度 52.4%，53.8% 完全去混淆，并将虚假控制流导致的 TFPS 膨胀抑制逾 99%。

**Abstract:** Code obfuscation is a process that complicates reverse engineering, protects intellectual property, and conceals malware. However, traditional deobfuscation methods are not universally applicable and can be easily circumvented. It is evident that advanced techniques, such as symbolic execution and SMT solvers, encounter difficulties when confronted with out-of-distribution code and particular obfuscation strategies. This hinders their efficacy to a considerable extent. This paper proposes a novel approach that integrates Large Language Models (LLMs) with decompiled code analysis to enhance understanding of control flow structures. Contributions include the formalisation of control flow deobfuscation tasks with new evaluation metrics and the proposal of a general predicate relationship inference method that adapts to diverse obfuscation techniques. The innovative model architecture combines linear LLM access with non-linear execution path expansion, thereby generating security-expert-friendly C pseudocode. Comprehensive evaluation on 780 binaries employing 13 distinct obfuscation techniques demonstrates that our method reduces average cyclomatic complexity by 52.4%, achieves full deobfuscation in 53.8% of cases, and suppresses Topological Feasible Path Set (TFPS) inflation caused by bogus control flow by over 99%. The framework demonstrates superiority over existing state-of-the-art tools in terms of both generality and semantic consistency, thus evidencing the transformative potential of LLMs in facilitating scalable malware reverse engineering.

## 10. NESA: Relational Neuro-Symbolic Static Program Analysis

**Authors:** Chengpeng Wang (National University of Singapore), Yifei Gao (Purdue University), Wuqi Zhang (MegaETH), Xuwei Liu (Purdue University, USA), Jinyao Guo (Purdue University), Mingwei Zheng (Purdue University), Qingkai Shi (Nanjing University), Xiangyu Zhang (Purdue University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808161

**中文总结:** 提出 NESA，用受限 Datalog 分析策略语言将静态分析分解为语法/语义子问题，结合解析与惰性增量 LLM 提示实现免编译、可定制分析并缓解幻觉；在 TaintBench 自定义污点检测 F1 达 0.72，并发现 13 个已修复的真实内存泄漏。

**Abstract:** Static program analysis plays an essential role in program optimization, bug detection, and debugging. However, reliance on compilation and limited customization hinder its adoption in the real world. This paper presents a compositional neuro-symbolic approach named NESA that facilitates compilation-free and customizable static program analysis using large language models (LLMs) with mitigated hallucinations. Specifically, we propose an analysis policy language, a restricted form of Datalog, to support users decomposing a static program analysis problem into several sub-problems that target simpler syntactic or semantic properties upon smaller code snippets. The problem decomposition enables the LLMs to target more manageable semantic-related sub-problems with reduced hallucinations, while the syntactic ones are resolved by parsing-based analysis without hallucinations. An analysis policy then is evaluated with lazy and incremental prompting, which significantly mitigates the hallucinations and improves the performance. We evaluate NESA for program slicing and bug detection upon benchmark and real-world programs. Evaluation results show that while NESA supports compilation-free and customizable analysis, it can still achieve comparable and even better performance than existing techniques. In a customized taint vulnerability detection upon TaintBench, for example, NESA achieves a precision of 66.27%, a recall of 78.57%, and an F1 score of 0.72, surpassing an industrial approach by 0.20 in F1 score. NESA also detects 13 real-world memory leak bugs, which have been fixed by developers.

## 11. Precondition Synthesis for Deep Neural Networks with Statistical Guarantees

**Authors:** Zengyu Liu (National University of Defense Technology), Bai Xue (Institute of Software at Chinese Academy of Sciences, China), Pengfei Yang (College of Computer and Information Science, Software College, Southwest University), Ji Wang (National University of Defense Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797151

**中文总结:** 提出 StatPre，以 select-and-solve 与 Box 抽象为 DNN 自动合成带统计保证、尽量宽松且准确的前置条件；在多基准上覆盖更广，并能处理高维、非 ReLU 的复杂网络。

**Abstract:** Deep neural networks (DNNs) are increasingly being deployed in safety-critical systems. However, existing formal verification methods provide limited quantitative guarantees for their reliable specification, and emerging precondition synthesis techniques are hindered by the scalability and architectural limitations of DNNs. In this paper, we propose a select-and-solve framework, StatPre, to automatically synthesize preconditions with statistical guarantees. StatPre aims to maximally weaken the synthesized preconditions while keeping them as accurate as possible to the real preconditions through a Box-based abstraction. The framework operates in two phases: the center selection phase, which identifies potential center points using a cluster-based heuristic with potential assessment, and the expansion solution phase, which solves the problem of optimizing maximal preconditions by employing statistical model approximation, equivalent constraint transformation, and automatic iterative execution. We evaluated StatPre on 15 models with 27 properties from 6 benchmarks and compared it with 4 existing deterministic and statistical schemes. The results demonstrate that StatPre effectively synthesizes preconditions with broader coverage while accurately approximating the real preconditions in practice. Additionally, StatPre exhibits competitive performance in handling high-dimensional, non-ReLU, complex-structured neural networks.

## 12. Property Refinement in Linear Temporal Logic: Formal Semantics and Algorithms for Software Verification

**Authors:** Luca Brodo (Hochschule Hamm-Lippstadt), Giuseppe Scalora (Hamm-Lippstadt University of Applied Sciences), Stefan Henkler (Hochschule Hamm-Lippstadt)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808127

**中文总结:** 提出 LTL 性质精化的形式理论与方法，按原子命题划分等价类并分析精化关系以剔除冗余验证性质；可将验证任务减少至多 75%，模型检测加速可达三个数量级，且精化分析开销极低。

**Abstract:** Model checking using temporal logic is a key aspect of formal verification of modern complex software systems. These systems are often result of distributed development processes, involving multiple teams and iterative design cycles. This complexity is mirrored in the corresponding formal specifications, which often consist of a large number of temporal logic properties that need to be verified against a system model. Many of these properties overlap semantically, yet traditional verification treats them as independent, resulting in redundant checks that waste computational resources and inflate engineering effort

We address this by introducing and operationalizing a formal theory of \emph{property refinement} for temporal logic into a concrete methodology that automatically identifies and eliminates redundant properties from a verification suite. This is achieved by first partitioning specifications into equivalence classes based on shared atomic propositions, followed by an analysis of intra-class refinement relations to construct the minimal sufficient subset. Our extensive empirical evaluation confirms the practical viability of our approach, demonstrating it can reduce the number of required verification tasks by up to 75% and accelerate model checking by up to three orders of magnitude, with a one-time associated overhead cost of 0.035% for the refinement analysis. The results of the evaluation confirm that the benefits of this approach are threefold: it reduces the computational requirements for formal verification; it allows engineers to focus on the core requirements of the system, hereby reducing engineering effort; finally, the one-time negligible investment in refinement yields compounding returns, making it particularly advantageous for agile and long-term development lifecycles.

This work thus establishes property refinement analysis as a key technique for scaling requirement engineering and software verification to modern complex software systems

## 13. Satisfiability Solving with LLMs

**Authors:** Leizhen Zhang, Shuhan Chen, Sheng Chen

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808209

**中文总结:** 系统评估 LLM 在 2/3-SAT 及 Vertex Cover、三维装箱等归约任务上的推理，并提出成对公式协议与 Accurate Differentiation Rate；发现传统指标易误导，ADR 更能区分真实推理与启发式。

**Abstract:** Large language models (LLMs) are increasingly used for tasks that implicitly reduce to Boolean satisfiability (SAT), yet their reasoning ability on SAT remains unclear. We present a systematic study of LLMs on 2-SAT and 3-SAT, together with two canonical reductions—Vertex Cover and a discrete 3D-packing formulation—designed to probe representation-invariant reasoning. Our evaluation begins with the conventional lens (accuracy/precision/recall/F1) and the phase-transition setting. We find that traditional metrics are frequently misleading: models exhibit a strong SAT bias, fail to reproduce the classical easy–hard–easy signature around the 3-SAT threshold, and degrade sharply as the number of variables N grows.

To address this, we introduce a distribution-agnostic paired-formula protocol (minimally different SAT/UNSAT instances) and a new measure, Accurate Differentiation Rate (ADR), which requires getting both members of each pair correct. ADR cleanly separates reasoning-oriented models from heuristic ones and correlates with witness validity (truth assignments that actually satisfy the formula). Extending beyond CNF, we test cross-representation consistency via standard reductions: (i) CNF → Vertex Cover and (ii) 3-SAT → discrete 3D packing with verifiable placement constraints. Decisions made on CNF and on their graph/packing counterparts agree for most models on >80% of instances, revealing stable decision rules across representations. A leading model (e.g., GPT-5) achieves both high invariance and correctness at small N, but still suffers scale-induced degradation.

Taken together, our results support the thesis that SAT is a foundational probe for LLM reasoning: performance on SAT predicts transfer to other NP-style reductions, while paired evaluation with ADR provides a faithful, representation-robust assessment beyond conventional metrics.

## 14. Semantics-Guided Control-Flow Reconstruction for Firmware Binaries via Static Analysis

**Authors:** Fengjuan Gao (Nanjing University of Science and Technology), Qingjie Zhu (Nanjing University), Yi Zhang (Nanjing University), Yu Wang (Nanjing University), Xuandong Li (Nanjing University), Ke Wang (Nanjing University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797130

**中文总结:** 提出 Scarf，面向剥离 ELF 与 raw 固件的语义引导静态控制流重建，结合过程内不动点值流分析与过程间间接调用解析；在 300+ 真实固件上较主流反编译工具更精确恢复间接跳转、调用返回与间接调用。

**Abstract:** Control-flow reconstruction is a fundamental yet challenging problem in firmware analysis, particularly for stripped  or raw-format binaries that lack symbolic metadata. Existing methods typically rely on syntax heuristics or format-specific patterns, which are inadequate for real-world firmware that includes indirect jumps, manually crafted assembly, and limited metadata.

We present a semantics-guided static analysis framework for accurate control-flow reconstruction in stripped ELF and raw-format firmware binaries. Our approach consists of two complementary components: (i) an intra-procedural control-flow reconstruction method that incrementally recovers direct branches, indirect jumps, and call-return flows via fixpoint-guided value-flow analysis; and (ii) an inter-procedural analysis that resolves indirect calls through cross-function value tracking and loop-structure matching. By decoupling control-flow reasoning from instruction semantics and function abstraction, our framework robustly handles tightly intertwined control-flow patterns and mitigates the impact of misanalysis.

We implement our approach in Scarf (\textit{\underline{S}emantics-guided} \textit{\underline{C}ontrol-flow} \textit{\underline{A}nalysis} for \textit{\underline{R}aw and} \textit{\underline{F}irmware binaries}) and evaluate it on over 300 real-world firmware binaries in both ELF and raw formats. Compared with state-of-the-art reverse engineering tools, Scarf consistently achieves higher precision in control-flow recovery and demonstrates clear advantages on raw firmware, especially in resolving indirect jumps, call–return flows, and indirect calls. These results demonstrate that semantics-guided analysis provides a robust and scalable foundation for control flow reconstruction in metadata-deficient firmware.

## 15. Sound Termination and Non-Termination Analysis of C Programs with Bit-Precise Bounded Semantics and Advanced Constructs

**Authors:** Negar Fathi (University of Nebraska–Lincoln), Hiroshi Unno (Tohoku University), Tachio Terauchi (Waseda University), Rahul Purandare (University of Nebraska-Lincoln)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808205

**中文总结:** 提出 Athena，以指针到数组改写、有界整数/位向量语义与 LTS 翻译支撑含指针、数组与位运算的 C 程序可靠终止/非终止分析；在真实非终止基准上正确率 62.39%，TermCOMP 达 75.60%，且两套评测均无错误结论。

**Abstract:** Program termination and non-termination analysis is a foundational problem in formal verification with important implications for software safety and reliability. Despite extensive research, existing techniques struggle with real-world C programs that manipulate complex data types such as pointers, arrays, and structures, or that perform low-level operations such as bitwise arithmetic and bounded integer computations. This paper introduces Athena, a framework for sound termination and non-termination analysis of C programs that faithfully captures concrete C semantics and supports advanced constructs. Athena combines pointer-to-array rewriting, bounded integer semantics via modulo arithmetic or bit-vector semantics, and an extended translation to Labeled Transition Systems (LTS), yielding structured, analyzable representations suitable for logic-based reasoning. Our analysis engine builds on MuVal, a modular verification engine based on the first-order fixpoint logic μCLP with background theories, and extends it with support for array, tuple, and bit-vector theories in ranking function synthesis and recurrent set detection. We evaluate Athena on the 2024 Termination Competition (TermCOMP) and on 117 real-world benchmarks featuring 445 non-termination bugs. On real-world benchmarks, it achieves the highest correctness (62.39%), surpassing the well-established tools UAutomizer and AProVE. On TermCOMP, it attains 75.60%, outperforming AProVE, while producing zero wrong results across both suites. These results demonstrate that Athena advances the state of the art by providing a strong combination of precision and soundness in the analysis of complex C programs.

## 16. TypePro: Boosting LLM-Based Type Inference via Inter-Procedural Slicing

**Authors:** linTeyu (Xiamen University), Minghao Fan (Xiamen University), Huaxun Huang (Xiamen University), Zhirong Shen (Xiamen University), Rongxin Wu (Xiamen University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808124

**中文总结:** 提出 TypePro，通过过程间切片补全上下文并由切片中的结构信息生成候选复杂类型，提升动态语言 LLM 类型推断；在 ManyTypes4Py/ManyTypes4TypeScript 上 Top-1 EM 达 88.9%/86.6%，较次优分别高 7.1 与 10.3 个百分点。

**Abstract:** Dynamic languages (such as Python and JavaScript) offer flexibility and simplified type handling for programming, but this can also lead to an increase in type-related errors and additional overhead for compile-time type inference. As a result, type inference for dynamic languages has become a popular research area. Existing approaches typically achieve type inference through static analysis, machine learning, or large language models (LLMs). However, current work only focuses on the direct dependencies of variables related to type inference as the context, resulting in incomplete contextual information and thus affecting the accuracy of type inference. To address this issue, this paper proposes a method called TypePro, which leverages LLMs for type inference in dynamic languages. TypePro supplements contextual information by conducting inter-procedural code slicing. Then, TypePro proposes a set of candidate complex types based on the structural information of data types implied in the slices, thereby addressing the lack of domain knowledge of LLMs. We conducted experiments on the ManyTypes4Py and ManyTypes4TypeScript datasets, achieving Top-1 exact match (EM) rates of 88.9% and 86.6%, respectively. Notably, TypePro improves the Top-1 Exact Match by 7.1 and 10.3 percentage points over the second-best approach, showing the effectiveness and robustness of TypePro.

## 17. Understanding Code Similarity across Instruction Set Architectures: An Empirical Study

**Authors:** Haonan Yu (Institute of Software Chinese Academy of Sciences), Jiaxin Zhu (Institute of Software at Chinese Academy of Sciences), Yingying Zheng (Institute of Software at Chinese Academy of Sciences), Yuwei Zhang (Institute of Software Chinese Academy of Sciences), Wei Wang (Institute of Software at Chinese Academy of Sciences), Jun Wei (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Tao Huang (Institute of Software at Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808119

**中文总结:** 对 20 个支持多 ISA 的开源基础软件项目开展实证研究，确认需保留独立 ISA 实现的同时发现跨 ISA 加权平均相似度约 21.7%；并观察到跨 ISA 协同变更与共同参与模式，为 ISA 相关维护提供证据。

**Abstract:** Software interacts with hardware through Instruction Set Architectures (ISAs), such as x86, ARM, and RISC-V. Although many developers may be unaware of ISA heterogeneity, ISA-specific code is pervasive in foundational software systems that underpin the digital infrastructure of human society. Maintaining separate implementations is common when supporting multiple ISAs in such a foundational software project. This may introduce substantial additional effort. Meanwhile, separate ISA-specific implementations frequently exhibit code similarities across ISAs. To understand ISA-specific code and their similarities, and to gain insights for better management, we conducted an empirical study of 20 open-source foundational projects that support multiple ISAs. We confirmed the need for separate ISA-specific implementations, yet our analysis revealed a weighted average similarity of 21.7% across ISAs. We also observed cross-ISA co-change and cross-ISA participation patterns in the development and maintenance of ISA-specific code. This study offers the first systematic investigation of ISA-specific code similarities, yielding evidence that can be leveraged by practitioners and researchers working on ISA-related software engineering.
