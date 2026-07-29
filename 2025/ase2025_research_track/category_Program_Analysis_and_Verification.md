# ASE 2025 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 35

## 1. Agentic Specification Generator for Move Programs

**Authors:** Yu-Fu Fu (Georgia Institute of Technology), Meng Xu (University of Waterloo), Taesoo Kim (Georgia Institute of Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334481

**中文总结:** 提出 MSG，面向 Move 智能合约的 LLM 智能体化规约生成工具；84% 测试函数可生成可验证规约，模块化设计与验证工具链反馈分别带来 57% 与 30% 可验证子句提升。

**Abstract:** While LLM-based specification generation is gaining traction, existing tools primarily focus on mainstream programming languages like C, Java, and even Solidity, leaving emerging and yet verification-oriented languages like Move underexplored.  In this paper, we introduce MSG, an automated specification generation tool designed for Move smart contracts.  MSG aims to highlight key insights that uniquely present when applying LLM-based specification generation to a new ecosystem.  Specifically, MSG demonstrates that LLMs exhibit robust code comprehension and generation capabilities even for non-mainstream languages.  MSG successfully generates verifiable specifications for 84% of tested Move functions and even identifies clauses previously overlooked by experts.  Additionally, MSG shows that explicitly leveraging specification language features through an agentic, modular design improves specification quality substantially (generating 57% more verifiable clauses than conventional designs).  Incorporating feedback from the verification toolchain further enhances the effectiveness of MSG, leading to a 30% increase in generated verifiable specifications.


## 2. Automated Insertion of Flushes and Fences for Persistency

**Authors:** Yutong Guo (University of California, Irvine), Weiyu Luo (University of California, Irvine), Brian Demsky (University of California at Irvine)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334229

**中文总结:** 提出 PMRobust 编译器，静态分析自动插入 flush/fence 以确保 CXL 共享内存与持久内存代码无遗漏刷写缺陷；在持久内存库与数据结构上几何平均开销仅 0.26%。

**Abstract:** CXL shared memory and persistent memory allow the contents of memory to persist beyond crashes.  Stores to persistent or CXL memory are typically not immediately made persistent; developers must manually flush the corresponding cache lines to force the data to be written to the underlying storage. Correctly using flush and fence operations is known to be challenging.  While state-of-the-art tools can find missing flush instructions, they often require bug-revealing test cases.  No existing tools can ensure the absence of missing flush bugs.

In this paper, we present PMRobust, a compiler that automatically inserts flush and fence operations to ensure that code using persistent memory is free from missing flush and fence bugs. PMRobust employs a novel static analysis with optimizations that target newly allocated objects. We have evaluated PMRobust on persistent memory libraries and several persistent memory data structures and measured a geometric mean overhead of 0.26%relative to the original benchmarks with hand-placed flush and fence operations.


## 3. Belief Propagation with Local Structure and Its Applications in Program Analysis

**Authors:** Yiqian Wu (Peking University, China), Yifan Chen (Peking University), Yingfei Xiong (Peking University), Xin Zhang (Peking University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334350

**中文总结:** 提出基于 if-then 规则编码因子局部结构的高效 loopy belief propagation 算法，在两个概率程序分析任务上分别平均加速 5.11 倍与 2.31 倍。

**Abstract:** In program analysis, there is an emerging trend to apply probabilistic reasoning. In general, these approaches build their models based on probabilistic graphical models because they can express local correlations through factors in a compositional manner, which is suitable for program analysis. These models commonly use the loopy belief propagation algorithm to infer the marginal probability distribution for efficiency. However, the efficiency of loopy belief propagation is still affected by large factors. To address this challenge, our insight is that we can exploit the local structure of probabilistic constraints to speed up the inference. To realize this idea, we use if-then rules to encode the factors with local structures and propose an efficient loopy belief propagation algorithm based on it. We also discuss the inference algorithm complexity and prove some applicable conditions of our approach. Our approach is evaluated on two existing program analysis works based on probabilistic graphical models. The results show that our approach can be 5.11 and 2.31 times faster than the original loopy belief propagation algorithm on average, respectively.


## 4. Breaking the Traffic Barrier: Unveiling Multi-Format of Protocols via Autonomous Program Exploration

**Authors:** Dingzhao Xue (Institute of Information Engineering of CAS, College of Cyberspace Security, Chinese Academy of Sciences), Yibo Qu (Institute of Information Engineering of CAS, College of Cyberspace Security, Chinese Academy of Sciences), Bowen Jiang (Institute of Information Engineering of CAS, College of Cyberspace Security, Chinese Academy of Sciences), Xin Chen, Shuaizong Si (Institute of Information Engineering of CAS, College of Cyberspace Security, Chinese Academy of Sciences), Shichao Lv (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Zhiqiang Shi (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Limin Sun (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334354

**中文总结:** 提出 ProbePRE，自主生成数据包探索协议处理器，结合隐式数据流追踪、结构感知约束提取与约束组合算法支持多格式协议逆向；字段分割准确率优于 4 个 SOTA PRE 工具。

**Abstract:** Protocol reverse engineering (PRE) aims to infer the protocol formats of unknown protocols. Existing techniques, whether Network-trace based or Execution-trace based methods, face two main limitations: a reliance on the quality and scale of traffic datasets, which often leads to low accuracy and poor generalization; and a failure to adequately consider the multi-format characteristic prevalent in real-world protocols (i.e., the same protocol may support multiple different formats).

To address these challenges, we propose ProbePRE—a PRE tool that performs multi-format extraction on protocol handlers by autonomously generating packets. ProbePRE employs three key techniques: (1) an execution tracing strategy enhanced with implicit data flow analysis to obtain more detailed execution information; (2) constraint extraction methods tailored for different program structures to pass protocol validation; and (3) an innovative constraint combination algorithm to construct effective packets that guide the protocol handler to execute diverse protocol parsing paths. In our experimental evaluation, we compared ProbePRE with 4 state-of-the-art PRE tools in terms of field segmentation accuracy. The results demonstrated that ProbePRE achieved an F1 score of 0.88, significantly outperforming existing methods. Furthermore, evaluations on 6 protocol handlers indicated that ProbePRE attained 83% completeness in multi-format extraction tasks. Notably, in basic block coverage tests, ProbePRE achieved a 67% improvement over traditional traffic dataset methods, which fully validates the effectiveness of its path exploration capabilities.


## 5. Bridging Natural Language and Formal Specification - Automated Translation of Software Requirements to LTL via Hierarchical Semantics Decomposition Using LLMs

**Authors:** Zhi Ma (Xidian University), Cheng Wen (Xidian University), Zhexin Su (Xidian University), Xiao Liang (Xidian University), Cong Tian (Xidian University), Shengchao Qin (Xidian University), Mengfei Yang (China Academy of Space Technology)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334235

**中文总结:** 提出 Req2LTL，通过层次中间表示 OnionL 将 LLM 语义分解与确定性 LTL 规则合成结合；在航空航天真实需求上达 88.4% 语义准确率与 100% 语法正确率，显著优于现有方法。

**Abstract:** Automating the translation of natural language (NL) software requirements into formal specifications remains a critical challenge in scaling formal verification practices to industrial settings, particularly in safety-critical domains. Existing approaches, both rule-based and learning-based, face significant limitations. While large language models (LLMs) like GPT-4o demonstrate proficiency in semantic extraction, they still encounter difficulties in addressing the complexity, ambiguity, and logical depth of real-world industrial requirements. In this paper, we propose \textbf{Req2LTL}, a modular framework that bridges NL and Linear Temporal Logic (LTL) through a hierarchical intermediate representation called \textit{OnionL}. \textbf{Req2LTL} leverages LLMs for semantic decomposition and combines them with deterministic rule-based synthesis to ensure both syntactic validity and semantic fidelity. Our comprehensive evaluation demonstrates that \textbf{Req2LTL} achieves 88.4% semantic accuracy and 100% syntactic correctness on real-world aerospace requirements, significantly outperforming existing methods.


## 6. Destabilizing Neurons to Generate Challenging Neural Network Verification Benchmarks

**Authors:** Linhan Li (George Mason University), ThanhVu Nguyen (George Mason University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334329

**中文总结:** 提出 ReluSplitter，通过对稳定 ReLU 神经元做语义保持的 destabilize 变换自动生成更难但 ground truth 不变的 DNN 验证基准，用于在不丢失可验证标签的前提下评估验证器正确性与性能。

**Abstract:** Neural Network Verification has made significant progress in recent years, with the development of numerous verification techniques and tools. However, the field still lacks high-quality benchmarks for systematically evaluating and improving these tools. As verification techniques advance, many existing benchmarks have become too trivial, while the harder ones often remain unsolvable. Several recent efforts have attempted to address this gap, typically by retraining or distilling neural networks to create new benchmarks. However, such approaches are computationally expensive and often produce benchmarks with unknown or unverifiable ground truth. In this paper, we introduce ReluSplitter, an automatic benchmark generation tool for DNN verifiers. ReluSplitter takes existing verification benchmarks as input and strategically destabilizes stable neurons to increase verification difficulty. This transformation is semantics-preserving by construction: every ReluSplitter-generated benchmark is guaranteed to have exactly the same ground truth as the original benchmark. This makes ReluSplitter particularly valuable for assessing verifier correctness and performance. Our evaluation demonstrates that ReluSplitter can significantly increase the difficulty of existing benchmarks, effectively challenging state-of-the-art DNN verifiers. We believe ReluSplitter offers a practical and principled way to generate benchmarks with tunable difficulty and verifiable ground truth, contributing a much-needed resource for the neural network verification community.


## 7. Detecting Semantic Clones of Unseen Functionality

**Authors:** Konstantinos Kitsios (University of Zurich), Francesco Sovrano (Collegium Helveticum, ETH Zurich, Switzerland; Department of Informatics, University of Zurich, Switzerland), Earl T. Barr (University College London), Alberto Bacchelli (University of Zurich)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334643

**中文总结:** 重新评估语义克隆检测在「未见功能」场景下的泛化：任务专用模型 F1 平均下降 31%（最高 48%），而 LLM 平均仅降 3%；并提出相应改进以更好检测训练时未见过功能的克隆。

**Abstract:** Semantic code clone detection is the task of detecting whether two snippets of code implement the same functionality (e.g., Sort Array). Recently, many neural models achieved near- perfect performance on this task. These models seek to make inferences based on their training data. Consequently, they better detect clones similar to those they have seen during training and may struggle to detect those they have not. Developers seeking clones are, of course, interested in both sorts of clones. We confirm this claim with a literature review, finding three practical clone detection tasks where the model’s goal is to detect clones of a functionality even if it was trained on clones of different functionalities. In light of this finding, we re-evaluate six state-of-the-art models, including both task-specific models and generative LLMs, on the task of detecting clones of unseen functionality. Our experiments reveal a drop in F1 of up to 48% (average 31%) for task-specific models. LLMs perform on par with task-specific models without explicit training for clone detection, but generalize better to unseen functionalities, where F1 drops up to 5% (average 3%) instead. We propose and evaluate the use of contrastive learning to improve the performance of existing models on clones of unseen functionality. We draw inspiration from the computer vision and natural language processing fields where contrastive learning excels at measuring similarity between two objects, even if they come from classes unseen during training. We replace the final classifier of the task-specific models with a contrastive classifier, while for the generative LLMs we propose contrastive in-context learning, which guides the LLMs to focus on the differences between clones and non-clones. The F1 on clones of unseen functionality is improved by up to 26% (average 9%) for task- specific models and up to 5% (average 3%) for LLMs.


## 8. Diagnosing Performance Differences in Model Checkers via Runtime-Guided Problem Generation

**Authors:** Yibo Dong (National University of Singapore), Yicong Xu (East China Normal University), Wenjing Deng (East China Normal University), Yu Chen (Chuzhou University), Xiaoyu Zhang (East China Normal University), Jianwen Li (East China Normal University, China), Chengyu Zhang (Loughborough University), Geguang Pu (East China Normal University, China)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334686

**中文总结:** 提出 AIGROW，基于运行时反馈演化生成硬件模型检测问题，在体积缩小两个数量级以上的同时仍能揭示不同 checker 间的显著性能差异，便于诊断优化与实现细节对求解性能的影响。

**Abstract:** Model checking has achieved remarkable success in the hardware domain, largely due to the accumulation of intricate optimizations and finely tuned implementation details. As tools evolve, diagnosing performance differences to better understand the interplay of these factors has become increasingly important. Yet existing problems that reveal such differences are often too large for meaningful inspection, limiting their diagnostic value.

To address the problem, this experience paper proposes AIGROW, a framework for generating hardware model checking problems, and introduces our experience on diagnosing performance differences in model checkers with the generated problems. AIGROW uses a feedback-guided process that evolves problems based on runtime information, selectively retaining those that become more difficult for a target checker. Performance differences are then revealed by evaluating these problems across hardware model checkers that have similar algorithms.

Our evaluation demonstrates that AIGROW generates problems that are more than 100 times smaller than those produced by existing generators,  while still revealing substantial performance differences. Diagnosing the performance differences has led to concrete improvements in CAR-based checkers: (1) uncovering structural inefficiencies in their exploration strategies, (2) solving 18 previously unsolvable HWMCC’24 problems, and (3) reducing runtime from hours to minutes in several cases.


## 9. DIFFFIX: Incrementally Fixing AST Diffs via Context and Type Information

**Authors:** Guofeng Zeng (University of Science and Technology Beijing), Chang-ai Sun (University of Science and Technology Beijing), Kai Gao (University of Science and Technology Beijing), Huai Liu (Swinburne University of Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334623

**中文总结:** 提出 DIFFFIX，利用 AST 节点的上下文与类型约束迭代修复五种 SOTA ASTDiff 工具产生的不完美 diff，将完美 diff 率提升 5.25%–51.12%，时间开销可忽略。

**Abstract:** The abstract syntax tree differencing (ASTDiff) technique aims to capture syntactic code changes in terms of comparing the differences between a pair of ASTs of a program, which has been widely used in various program analysis or testing tasks, such as code review, clone detection, and regression testing. A key issue to ASTDiff lies in the accurate mappings between nodes of two ASTs. However, most existing approaches often fail to generate such perfect diffs due to the gap between diverse code changes and unsound node matching heuristics. Our in-depth investigation reveals that most inaccurate mappings are caused by the ignorance of context- and type-specific constraints. Accordingly, we propose an AST diff fixing approach DIFFFIX that leverages both node’s context and type constraints to iteratively and incrementally fix imperfect diffs. Comprehensive experiments have been conducted to evaluate the effectiveness of DIFFFIX through the application of it to fix diffs generated by five state-of-the-art ASTDiff techniques. The experimental results demonstrate that DIFFFIX can improve the perfect diff rate of these baseline techniques by 5.25% to 51.12% with negligible time overhead.


## 10. EditFusion: Resolving Code Merge Conflicts via Edit Selection

**Authors:** Changxin Wang (Nanjing University), Yiming Ma (Nanjing University), Lei Xu (Nanjing University), Weifeng Zhang (Nanjing University of Posts and Telecommunications)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334381

**中文总结:** 提出 EditFusion，将合并冲突解决建模为对行级 edit script 的二元接受/拒绝选择，尤其针对占比高且可用简单模式解决的相邻行冲突，相比多类分类或整段生成更可解释、更易人工复核。

**Abstract:** Merge conflicts in distributed version control systems (DVCS) like Git are a persistent challenge in software development lifecycle. If not handled properly or overlooked, they can lead to issues like hindering collaboration and introducing errors. While automated resolution methods exist, prevailing approaches—such as multi‑class classification and direct code generation—often suffer from limited interpretability, demanding substantial manual effort to refine predictions, and risk producing subtly flawed code. Critically, existing research often overlooks a prevalent conflict type: adjacent-line conflicts, where independent edits to contiguous lines are flagged by tools like Git. Our empirical analysis reveals that these make up a substantial portion of all conflicts. Moreover, they can often be resolved using simple patterns.

Motivated by these limitations and empirical findings, we propose a novel approach: modeling merge conflict resolution as edit script selection. Instead of predicting abstract categories or generating code de novo, our method makes a binary decision for each atomic line-level edit script contributing to the conflict: accept or reject. Our method inherently makes the reasoning behind proposed solutions transparent, as decisions directly correspond to individual, developer-authored code modifications. It also aligns closely with how developers naturally approach conflict analysis by considering each change in context. Our method applies for the vast majority (94.18%) of conflicts that do not require entirely new code; this selection process directly yields the resolved code by applying the chosen subset of existing edits.

As an implementation of our proposed method, we developed EditFusion, a deep learning model that performs edit script selection by leveraging semantic embeddings and edit metadata. Extensive evaluation on large-scale, real-world datasets demonstrates both the prevalence of adjacent-line conflicts and EditFusion’s superior performance in accurately resolving conflicts compared to baselines. Our work represents an attempt towards more transparent, intuitive, and practical automated merge conflict resolution.


## 11. Efficient and Verifiable Proof Logging for MaxSAT Solving

**Authors:** Raoul van Doren (ETH Zurich), Timos Antonopoulos (Yale University), Ruzica Piskac (Yale University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334432

**中文总结:** 为 core-guided OLL MaxSAT 求解器提出首个专用可验证证明日志框架，形式化 cores/cliques/hardenings/totalizer 等推理规则并在 EvalMaxSAT 实现可读与紧凑二进制 DAG 日志；在 2024 MaxSAT 竞赛数据集上验证可行性与可扩展性。

**Abstract:** MaxSAT solvers are increasingly used as back-ends in software engineering tools. Yet their results have lacked automatically checkable certificates of optimality. While SAT solvers emit DRAT proofs of (un)satisfiability, MaxSAT must additionally prove that no lower-cost solution exists. Existing approaches either cover only isolated solving paradigms or reduce MaxSAT reasoning to heavyweight pseudo-Boolean proofs, yielding impractical verification overhead. We present the first MaxSAT-specific proof-logging framework for core-guided OLL solvers. We formalize native inference rules for cores, cliques, hardenings, totalizer updates, and bound adjustments, and implement both a human-readable logger and a compact binary DAG logger in EvalMaxSAT. Evaluation on the 2024 MaxSAT competition dataset confirm the practicality and scalability of our certification pipeline, paving the way for trustworthy, solver use.


## 12. EPSO: A Caching-Based Efficient Superoptimizer for BPF Bytecode

**Authors:** Qian Zhu (Nanjing University), Yuxuan Liu (Nanjing University), Ziyuan Zhu (Nanjing University), Shangqing Liu (Nanjing University), Lei Bu (Nanjing University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334267

**中文总结:** 提出 EPSO，离线超优化发现 eBPF 字节码重写规则并缓存复用，在 Linux 内核及 Cilium、Katran 等项目上实现接近超优化质量且运行时开销极低的优化。

**Abstract:** Extended Berkeley Packet Filter (eBPF) allows developers to extend Linux kernel functionality without modifying its source code. To ensure system safety, an in-kernel safety checker, the verifier, enforces strict safety constraints (e.g., a limited program size) on eBPF programs loaded into the kernel. These constraints, combined with eBPF’s performance-critical use cases, make effective optimization essential. However, existing compilers (e.g., Clang) offer limited optimization support, and many semantics-preserving transformations are rejected by the verifier, which makes handcrafted optimization rule design both challenging and limited in effectiveness.

Superoptimization overcomes the limitations of rule-based methods by automatically discovering optimal transformations, but its high computational cost limits scalability. To address this, we propose EPSO, a caching-based superoptimizer that discovers rewrite rules via offline superoptimization, and reuses them to achieve high-quality optimizations with minimal runtime overhead. We evaluate EPSO on benchmarks from the Linux kernel and several eBPF-based projects, including Cilium, Katran, hXDP, Sysdig, Tetragon, and Tracee. EPSO discovers 624 rewrite rules and achieves up to 68.87% (avg. 20.01%) reduction in program size compared to Clang’s best output, outperforming the state-of-the-art BPF optimizer K2 on all benchmarks and Merlin on 81.60% of them. Additionally, EPSO reduces program runtime by an average of 6.60%, improving throughput and lowering latency in network applications.


## 13. Evolution-Aware Heuristics for GR(1) Realizability Checking

**Authors:** Dor Ma'ayan (Tel Aviv University), Shahar Maoz (Tel Aviv University), Jan Oliver Ringert (Bauhaus-University Weimar)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334501

**中文总结:** 提出演化感知的 GR(1) 可实现性检验启发式，对前后版本规格做局部语义 diff 并复用上次检验中间结果；在迭代式规格开发场景下显著缩短可实现性检查时间。

**Abstract:** Reactive synthesis is an automated procedure to obtain a correct-by-construction reactive system from its temporal logic specification. Despite significant research progress over the past few decades, reactive synthesis is still in its early stages of practical adoption. One significant barrier to using reactive synthesis outside academia is the long realizability checking and synthesis time of specifications.

This paper introduces a novel, evolution-aware approach for realizability checking. Our approach leverages the key observation that realizability checking is an operation that developers frequently perform during iterative specification development; therefore, utilizing intermediate data from previous realizability checks can substantially improve running times. Our approach computes a local semantic diff between previous and current versions of the specification, and, based on the diff and the previous realizability checking result, applies a set of sound heuristics. These heuristics reuse intermediate data collected during the original specification’s realizability checking to accelerate the evolved specification’s realizability checking. Our evaluation demonstrates that these heuristics are applicable in 70% of cases from a real-world dataset containing thousands of specifications, and that their application significantly improves the running time of realizability checking.


## 14. Exploring Static Taint Analysis in LLMs: A Dynamic Benchmarking Framework for Measurement and Enhancement

**Authors:** Haoran Zhao (Fudan University), Lei Zhang (Fudan University), Keke Lian (Fudan University), Fute Sun (Fudan University), Bofei Chen (Fudan University), Yongheng Liu (Fudan University), Zhiyu Wu (Fudan University), Yuan Zhang (Fudan University), Min Yang (Fudan University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334601

**中文总结:** 提出 LLMCAPLENS 动态基准生成框架，建模影响 LLM 静态污点分析能力的因素，采用基本单元生成与轻量动态污点验证，系统测量并增强 LLM 污点分析能力。

**Abstract:** LLMs offer a promising avenue to overcome the limitations of traditional taint analysis techniques, with a growing number of studies leveraging LLMs for taint analysis and its downstream applications. However, these studies lack a systematic understanding of LLMs’ taint analysis capabilities, limiting their transferability and reliability. To bridge this gap and better apply LLMs to static taint analysis, we aim to comprehensively measure and understand LLMs’ taint analysis capabilities.

Using existing benchmarks is a straightforward approach, but they are unsuitable due to issues such as training data leakage, not accounting for LLMs’ features, and improper assessment criteria. Manually constructing new benchmarks is not only labor-intensive but also struggles to remain effective as LLMs evolve. To address these, we propose LLMCAPLENS, a dynamic benchmark generation framework to systematically measure and enhance LLMs’ capabilities. LLMCAPLENS models influencing factors of LLMs’ taint analysis capabilities, employing a Basic Unit-Based generation method and a lightweight dynamic taint analysis-based verification method to implement the automated generation of targeted benchmarks, ensuring both diversity and correctness. Furthermore, LLMCAPLENS proposes a measurement-driven, training-free, model-specific enhancement approach.

We apply LLMCAPLENS to 10 mainstream LLMs, revealing how they perform under various influencing factors and identifying unique characteristics, such as the underlying error causes for each model. Notably, our enhancement approach significantly improves LLM performance—GPT-4 Turbo, for instance, achieved improvements across 16 out of 19 factors, with an average True Negative Rate increase of 21.29 %. Finally, we validate the real-world impact of our method by applying enhanced LLMs to vulnerability detection, demonstrating a substantial improvement over prior approaches.


## 15. Faster Runtime Verification during Testing via Feedback-Guided Selective Monitoring

**Authors:** Shinhae Kim (Cornell University), Saikat Dutta (Cornell University), Owolabi Legunsen (Cornell University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334469

**中文总结:** 提出 Valg，首个基于强化学习的测试时选择性运行时验证技术，利用 monitor 冗余反馈仅创建必要 monitor；在 64 个 Java 开源项目上比 JavaMOP 快最多 20.2 倍、比 TraceMOP 快最多 555.6 倍。

**Abstract:** Runtime verification (RV) uses monitors, which are dynamically created based on formal specifications (specs), to check running programs against specs. RV of passing tests in many open-source projects found hundreds of new bugs. But, high overheads make it hard to use RV for testing in practice. We propose Valg, the first on-the-fly selective RV technique for testing, and the first to use reinforcement learning (RL) to speed up RV. Valg leverages a recent finding: 99.87% of monitors are redundant for testing; they wastefully re-check unique traces—sequences of events, e.g., method calls—that the other necessary 0.13% already checked. Valg uses feedback about redundancy of prior monitors and events to selectively monitor only necessary ones subsequently. A key idea in Valg is our novel formulation of selective monitor creation as a two-armed bandit RL problem that rewards necessary monitors, and penalizes redundant ones. We implement Valg for Java and compare it with state-of-the-art RV tools on one revision each of 64 open-source projects. With default RL hyperparameters, Valg is up to 20.2x and 555.6x faster than JavaMOP and TraceMOP, respectively. For example, Valg takes only 54.8 minutes in total to monitor three projects where TraceMOP takes 3.02 days in total. Valg finds 99.6% of JavaMOP and TraceMOP’s spec violations, but it only checks 76.7% of their unique traces on average. After tuning hyperparameters, Valg checks 95.1% of unique traces on average with little loss in speed. Using tuned hyperparameters from one revision “into the future” as code evolves preserves Valg’s high rate of checked unique traces and speedups, without needing frequent re-tuning.


## 16. How Big is the Automaton? Certified Lower Bounds on the Size of Presburger DFAs

**Authors:** Nicolas Amat (ONERA - The French Aerospace Lab), Pierre Ganty (IMDEA Software Institute, Spain), Alessio Mansutti (IMDEA Software Institute)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334328

**中文总结:** 提出全自动方法计算 Presburger 算术公式对应最小 DFA 大小的可验证下界证书，并支持 union 操作进一步收紧界；在 SMT-LIB 5000+ 公式上常接近真实最小自动机规模。

**Abstract:** Lower bounds provide essential insights into the minimal computational resources required for algorithm execution. This paper focuses on logical theories, a domain where estimating resources is particularly difficult, and provides a novel, fully-automated method for computing lower bounds on memory usage, serving as a proxy for the computational resources required to perform logical reasoning.

Specifically, our method provides a lower bound on the size of the minimal deterministic finite automaton that encodes the solution set of a given Presburger arithmetic (also known as linear integer arithmetic) formula. The lower bounds are accompanied by independently verifiable certificates which also support a union-like operation that can be used to further increase the computed bounds.

We conducted an extensive empirical evaluation of our method using over 5000 formulae from the quantifier-free fragment of Presburger arithmetic, sourced from the SMT-LIB repository. The results show that our method often produces lower bounds that are close to the actual size of the minimal deterministic finite automaton. Moreover, it succeeds in computing non-trivial bounds even for instances that are out of reach (by several orders of magnitude) for the existing state-of-the-art automata-based tools for solving Presburger arithmetic.


## 17. Improving NLSAT for Nonlinear Real Arithmetic

**Authors:** Zhonghan Wang (Institute of Software, Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334661

**中文总结:** 提出 clauseSMT，在 NLSAT 框架下引入子句级可行集 lookahead 与算术传播分支启发式，利用子句对算术变量的约束改进 literal 决策；在非线性实算术可满足实例上优于 CVC5、Z3、YICES2。

**Abstract:** The Model-Constructing Satisfiability Calculus (MCSAT) framework has been applied to SMT problems over various arithmetic theories. NLSAT, an implementation using cylindrical algebraic decomposition (CAD) for explanation, is especially competitive for nonlinear real arithmetic (NRA) constraints. However, current Conflict-Driven Clause Learning (CDCL)-style algorithms only consider literal information when making decisions, and thus ignore the influence of clauses on arithmetic variables. This limitation may lead NLSAT to encounter unnecessary conflicts due to suboptimal literal choices. To address this issue, we analyze conflicts caused by literal decisions and incorporate clause-level information that directly affects arithmetic variables. We propose two main algorithmic improvements: a clause-level feasible-set-based look-ahead mechanism and an arithmetic propagation-based branching heuristic. We implement our solver, named clauseSMT, based on a dynamic variable ordering framework. Experiments indicate that clauseSMT is competitive on nonlinear real arithmetic problems compared with existing SMT solvers (CVC5, Z3, YICES2), and it outperforms all of them on satisfiable instances of SMT(QF_NRA) in SMT-LIB. We also evaluate the effectiveness of our proposed methods.


## 18. Incremental Program Analysis in the Wild: An Empirical Study on Real-World Program Changes

**Authors:** Xizao Wang (Nanjing University), Xiangrong Bin (Nanjing University), Lanxin Huang (Nanjing University), Shangqing Liu (Nanjing University), Jianhua Zhao (Nanjing University, China), Lei Bu (Nanjing University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334347

**中文总结:** 构建含 4,084 个来自 20 个 Java 开源项目真实变更的大规模 IPA 基准与统一评估框架，系统评估两种代表性增量分析工具；揭示现有 IPA 研究缺乏真实变更基准与评估指标不均衡的问题。

**Abstract:** Incremental Program Analysis (IPA) has gained increasing attention as an effective technique for maintaining up-to-date code insights by leveraging previously computed analysis results in response to program modifications. Consequently, a variety of IPA algorithms and tools have been proposed. However, their empirical performance in practical, real-world scenarios remains insufficiently investigated. To address this gap, this study presents a comprehensive examination of the current state-of-the-art in IPA evaluation. Specifically, we identify two critical limitations: (1) the lack of standardized benchmarks reflecting real-world program changes, and (2) the inadequacy and uneven distribution of evaluation metrics.

To overcome these challenges, we propose an automated pipeline for constructing realistic program change benchmarks and develop a unified evaluation framework compatible with a range of IPA tools. Using this infrastructure, we curated a large-scale benchmark dataset comprising 4,084 real-world program changes drawn from 20 open-source Java projects, and systematically evaluated two representative IPA tools. The results demonstrate that, although incremental analysis substantially improves efficiency compared to exhaustive analysis, existing IPA tools exhibit inconsistencies and markedly higher peak memory consumption. Finally, we distill practical insights from our findings to inform future research and development in the field of incremental program analysis.


## 19. Latra: A Template-Based Language-Agnostic Transformation Framework for Effective Program Reduction

**Authors:** Zhenyang Xu (University of Waterloo), Yiran Wang (University of Waterloo), Yongqiang Tian (Monash University), Mengxiao Zhang (University of Waterloo), Chengnian Sun (University of Waterloo)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334681

**中文总结:** 提出 Latra 模板化语言无关程序化简框架，用匹配/重写 DSL 定义语言特定变换，在通用性与有效性间取得平衡；在 C 与 SMT-LIB 上比 Vulcan 多化简 33.77%/9.17% token，并接近 C-Reduce、ddSMT 等语言专用工具效果。

**Abstract:** Essential for debugging compilers and interpreters, existing reduction tools face a fundamental trade-off. Language-specific reducers, such as C-Reduce and ddSMT, offer highly effective reductions but require substantial engineering effort for each target language. Conversely, language-agnostic reducers, like Vulcan, sacrifice effectiveness for broad applicability.

To bridge this gap, we present Latra, a novel template-based framework that balances both aspects, enabling general, effective, targeted program reduction. Latra combines language-agnostic reduction with user-defined, language-specific transformations. It facilitates user-defined transforms through a user-friendly domain-specific language based on simple matching and rewriting templates, minimizing the need for deep formal grammar knowledge. Latra empowers users to tailor reductions to specific languages with reduced implementation overhead.

Evaluation shows that Latra significantly outperforms Vulcan, reducing 33.77% more tokens in C and 9.17% more tokens in SMT-LIB, with 32.27% faster execution in SMT-LIB. Notably, Latra closely matches the effectiveness of language-specific reducers C-Reduce and ddSMT (89 vs. 85, 103 vs. 109 tokens), while significantly reducing engineering effort (167 vs. 5,508, 62 vs. 118 lines of code). We strongly believe that Latra provides a practical and cost-efficient approach to program reduction, effectively balancing language-specific effectiveness with language-agnostic generality.


## 20. LLM-Assisted Synthesis of High-Assurance C Programs

**Authors:** Prasita Mukherjee (Purdue University), Minghai Lu (Purdue University), Benjamin Delaware (Purdue University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334588

**中文总结:** 提出 SYNVER，结合两个 LLM 与 Verified Software Toolchain：一个生成满足可验证语法约束的 C 程序候选，另一个在 Rocq 中辅助证明，并与符号推理引擎协同处理证明义务；在 deductive synthesis 基准上生成带机器检验正确性证明的程序。

**Abstract:** We present SYNVER - a novel, general purpose synthesizer for C programs with machine-checked proofs of their correctness using the Verified Software Toolchain framework. To do so, SYNVER employs two Large Language Models: the first is used to generate candidate programs from a user-provided specification, and the second helps to automatically generate proofs of correctness in the Rocq proof assistant. SYNVER ensures that generated programs adhere to a set of syntactic criteria that make candidate programs amenable to automated verification. To verify programs, SYNVER uses a novel proof generation strategy which combines a symbolic reasoning engine, specialized to reasoning about proof obligations generated by our verification framework, and a language model that handles obligations the symbolic engine cannot. We demonstrate the applicability of SYNVER using a diverse set of benchmarks drawn from the deductive program synthesis literature.


## 21. Loupe: End-to-End Learning of Loop Unrolling Heuristics for Abstract Interpretation

**Authors:** Maykel Mattar (Université Paris-Saclay, CEA, List / Université Bretagne Sud, IRISA), Michele Alberti (Université Paris-Saclay, CEA, List), Valentin Perrelle (CEA, LIST, France), Salah Sadou (IRISA & CNRS, Universite Bretagne Sud,France)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334363

**中文总结:** 提出 Loupe，用 GNN 从程序图表示端到端学习抽象解释中的循环展开启发式，并由 Frama-C/EVA 自动标注训练数据；最佳模型 GINE 在真实 C 程序上较内置启发式减少 1.5× 误报、分析耗时降低 56%，且接近专家决策。

**Abstract:** While static program analyzers based on abstract interpretation implement precision-improving techniques to reduce false alarms, such as loop unrolling, their computational cost requires carefully devised heuristics for selective application. Manually designing such heuristics is non-trivial and error-prone, possibly leading to state explosion.

This paper presents Loupe, a novel end-to-end approach for automatically learning loop unrolling heuristics for static program analysis. Unlike previous data-driven methods, Loupe leverages Graph Neural Networks (GNNs) to learn directly from graph-based program representations. To enable supervised learning, we use the static analyzer itself to automatically label training data. We implement Loupe on top of Frama-C/EVA, an open source C static analyzer, and demonstrate that the best performing heuristic (GINE) outperforms the Frama-C/EVA built-in heuristic on real-world programs, reducing false alarms by 1.5x while improving analysis performance by 56%. Remarkably, GINE accurately predicts loop unrolling decisions made by expert Frama-C/EVA engineers, while maintaining acceptable false-positive rates. Finally, we show that Loupe can effectively learn heuristics for other static analyzers such as Mopsa.


## 22. Non-termination Witnesses and their Validation

**Authors:** Zsófia Ádám (Department of Measurement and Information Systems, Budapest University of Technology and Economics), Paulína Ayaziová (Masaryk University, Czechia), Levente Bajczi (Budapest University of Technology and Economics), Dirk Beyer (LMU Munich), Marek Jankola (LMU Munich), Marian Lingsch-Rosenfeld (LMU Munich), Jan Strejcek (Masaryk University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334721

**中文总结:** 扩展软件验证 witness 格式 2.0 以支持非终止 witness，给出语义定义及生成/校验方法，填补 SV-COMP 等生态在非终止证书方面的空白；并概述当前工具支持现状。

**Abstract:** Designing algorithms for complex problems as certifying algorithms is an important approach to ensure correctness of computational results. Instead of producing an output y for an input x, a certifying algorithm produces as output for x not only y but also a witness w. The witness w (also called certificate) can now be used to check that y is indeed the correct output for input x. Witnesses and their validation also exist in the area of automatic software verification, and a large number of tools support verification witnesses. SV-COMP 2025 reports 62 verifiers producing witnesses and 18 tools for witness validation. In 2023, a new version 2.0 of the witness format for software verification was introduced to overcome several problems with the previous format, and this new format is now widely supported. However, there is no format with a clear definition and semantics for witnesses of non-termination. This paper closes this gap by presenting an extension of the witness format 2.0 to support program non-termination. Besides explaining the design of this extension, we describe various approaches to generate and validate non-termination witnesses. We also give an overview of current tool support of the extended format, i.e., the verifiers that can generate non-termination witnesses and the witness validators able to analyze these witnesses. Finally, we present an experimental evaluation showing the performance of these tools on program-termination tasks of SV-COMP 2025.


## 23. On the Correctness of Software Merge

**Authors:** Akira Mori (National Institute of Advanced Industrial Science and Technology (AIST)), Masatomo Hashimoto (Chiba Institute of Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334536

**中文总结:** 基于范畴论 pushout 提出三路合并结果应「可解析且 universal（恰合并各分支编辑、公共编辑只应用一次）」的语法正确性准则，并实现结构合并工具；在 76 个 Java 项目 43774 次合并中发现 Git 等现有工具大量不合规结果。

**Abstract:** Three-way merge tools play crucial roles in modern software development, where a developer forks a branch to make local modifications and requests it to be merged into the main branch via a “pull request.” Despite its importance, the task has traditionally been defined in an intuitive manner, and the results of merge tools are often accepted without scrutiny. In this paper, we present a new structural merge tool in comparison with existing tools based on the syntactic criteria we propose for evaluating the merge results. We require the merge result to be both parsable and universal. Being parsable means that the result is syntactically valid according to the grammar of the programming language. Being universal means that the result incorporates all and the only edit operations occurring in each branch while ensuring that edits common to both branches are applied only once. This requirement can be precisely defined using the notion of pushouts in category theory. In a large-scale experiment involving 43,774 file merge scenarios from 76 open-source Java projects, we found a number of incorrect results reported by the existing tools such as the Git companion merge tool, whereas our tool reports none. We expect that the proposed criterion will help in developing reliable merge tools in the future.


## 24. PAT-Agent: Autoformalization for Model Checking

**Authors:** Xinyue Zuo (National University of Singapore), Yifan Zhang (National University of Singapore), Hongshu Wang (National University of Singapore), Yufan Cai (National University of Singapore), Zhe Hou (Griffith University), Jing Sun (School of Computer Science, University of Auckland), Jin Song Dong (National University of Singapore)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334568

**中文总结:** 提出 PAT-Agent 端到端自然语言 autoformalization 与模型修复：Planning LLM 生成建模计划，Code Generation LLM 合成 PAT 模型 checker 可验证的形式化模型，违例时基于反例迭代 Repair Loop；并提供面向非形式化方法专家的 Web 界面。

**Abstract:** Recent advances in large language models (LLMs) offer promising potential for automating formal methods. However, applying them to formal verification remains challenging due to the complexity of specification languages, the risk of hallucinated output, and the semantic gap between natural language and formal logic. We introduce PAT-Agent, an end-to-end framework for natural language autoformalization and formal model repair that combines the generative capabilities of LLMs with the rigor of formal verification to automate the construction of verifiable formal models. In PAT-Agent, a \emph{Planning LLM} first extracts key modeling elements and generates a detailed plan using semantic prompts, which then guides a \emph{Code Generation LLM} to synthesize syntactically correct and semantically faithful formal models. The resulting code is verified using \emph{the PAT model checker} against user-specified properties, and when violations occur, a \emph{Repair Loop} is triggered to iteratively correct the model using counterexamples. To improve flexibility, we built a web-based interface that enables users, particularly non-FM-experts, to describe, customize, and verify system behaviors through user-LLM interactions. Experimental results on 40 systems show that PAT-Agent consistently outperforms baselines, achieving high verification success with superior efficiency. The ablation studies confirm the importance of both planning and repair components, and the user study demonstrates that our interface is accessible and supports effective formal modeling, even for users with limited formal methods experience.


## 25. Programmers’ Visual Attention on Function Call Graphs During Code Summarization

**Authors:** Samantha McLoughlin (Vanderbilt University), Zachary Karas (Vanderbilt University), Robert Wallace (University of Notre Dame), Aakash Bansal (Louisiana State University), Collin McMillan (University of Notre Dame), Yu Huang (Vanderbilt University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334538

**中文总结:** 研究程序员在代码摘要任务中对函数调用图的视觉注意力，用图遍历深度、覆盖率等指标量化项目级上下文理解；基于既有眼动数据（n=10）重新分析并扩展相关发现。

**Abstract:** This paper studies programmer visual attention on function call graphs during code summarization. Programmer visual attention refers to where people look when performing a software engineering task, and code summarization is the task of writing a natural language description about a section of source code. Prior work has studied programmers’ visual attention during code summarization, with the vast majority of research effort placed on details in single functional units of code. There have not been any techniques developed to understand code comprehension at the project level due to the difficulty of this task, despite the nature of most real-world methods as embedded within complex project context. This paper focuses on the visual attention paid to the call graph context in which a method sits. We analyze visual attention coverage of call graphs with graph-based metrics, such as the depth that programmers traverse or the amount of coverage they attain. We use these metrics, among other means, to reevaluate an existing dataset from a previous eye-tracking study of programmers ($n=10$) that considered basic properties of programmer visual attention in a project context. We then created a new dataset ($n=12$) using the same procedures specifically for this paper, resulting in a total of 88 hours of recorded visual behavior on source code.  We used our proposed metrics to analyze how participants’ visual strategies correlated with their code summary quality, and confidence in their summaries. Interestingly, we found that higher coverage of the call graph was associated with \textit{decreases} in both summary quality and participants’ confidence.


## 26. Protecting Source Code Privacy When Hunting Memory Bugs

**Authors:** Jielun Wu (Nanjing University), Bing Shui (Nanjing University), Hongcheng Fan (Nanjing University), Shengxin Wu (Nanjing University), Rongxin Wu (Xiamen University), Yang Feng (Nanjing University), Baowen Xu (Nanjing University), Qingkai Shi (Nanjing University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334312

**中文总结:** 提出 DIReducer，在保留内存缺陷检测能力的前提下从非 strip 二进制中削减 debug 信息，通过选择性剪枝与 NP-hard 的类型最小化（归约为 set cover）平衡源码隐私与第三方审计需求。

**Abstract:** When proving to a third party that a software system is free from critical memory bugs, software vendors often face the problem of having to reveal their source code, so that the third party can scan the source code using static analysis tools. However, such transparency poses a significant threat to vendors, as the source code typically contains proprietary algorithms, core technical innovations, or trade secrets, exposing them to potential intellectual property risks. In this paper, we present a novel solution that offers a balance between transparency and code privacy, so that software vendors can provide minimal source code information but can justify the sufficiency of bug detection. To this end, we propose DIReducer, which reduces source code information, a.k.a. debug information, from non-stripped binaries while preserving its utility for memory bug detection. DIReducer consists of two components: selective pruning and type minimization. The former eliminates redundant debug information, and the latter is proved to be NP-hard and minimizes type-related debug information by reducing it to the classic set-cover problem, which offers feasible and near-optimal solutions. Experimental results show that we can reduce over 90% of debug information while maintaining similar bug detection capability compared to using full debug information.


## 27. R3-Bench: Reproducible Real-world Reverse Engineering Dataset for Symbol Recovery

**Authors:** Muzhi Yu (Peking University and Alibaba Group), Zhengran Zeng (Peking University), Wei Ye (Peking University), Jinan Sun (Peking University), Xiaolong Bai (Alibaba Group), Shikun Zhang (Peking University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334366

**中文总结:** 提出 AST-Align 跨架构/语言对齐变量与 struct 访问表达式，并构建含千万级函数、可复现的 R3-Bench 符号恢复数据集；相较既有方法捕获约 4 倍 struct 字段 ground truth。

**Abstract:** Symbol recovery in reverse engineering is crucial for restoring variable and data structure information in compiled binaries. While learning-based methods have shown promise in recovering both semantic information (names and types) and syntactic information (shapes), they require comprehensive datasets where expressions in binary code are precisely aligned with their source code equivalents. Current techniques for generating such alignments struggle with complex data access patterns, resulting in incomplete training data and consequently hampering model performance and recovery accuracy. We present AST-Align, a novel technique unifying alignment of variables and struct access expressions across multiple architectures (x86 and ARM) and languages (C/C++/Rust). AST-Align significantly improves the number of generated ground truths, capturing four times more struct fields than previous methods. Using this algorithm, we develop R3-Bench, a metadata-rich, extensible dataset with explicit project inclusion criteria and reproducible processing pipeline, comprising over 10 million functions across multiple architectures. Our evaluation establishes baseline performance by testing various approaches from n-gram models to Large Language Models. The results show that while general LLMs initially perform poorly, their effectiveness dramatically improves with proper demonstration. R3-Bench provides a robust foundation for assessing model capabilities and serves as a valuable reference for future symbol recovery research.


## 28. RELIA: Accelerating Analysis of Cloud Access Control Policies

**Authors:** Dan Wang (Xi'an Jiaotong University), Peng Zhang (Xi'an Jiaotong University), Zhenrong Gu (Xi'an Jiaotong University), Weibo Lin (Huawei Cloud), Shibiao Jiang (Huawei Cloud), Zhu He (Huawei Cloud), Xu Du (Huawei Cloud), Longfei Chen (Huawei Cloud), Jun Li (Huawei), Xiaohong Guan (Xi'an Jiaotong University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334240

**中文总结:** 提出 RELIA，预计算正则表达式对应的 String Equivalence Classes 并将正则约束改写为整数约束，加速云访问控制策略的 SMT 分析；作为透明层接入现有分析器与 Z3/CVC 求解器。

**Abstract:** With the diversification of cloud services, cloud providers offer flexible access control by letting users apply fine-grained cloud access control policies to secure their cloud resources. However, flexibility comes with the cost that configuring cloud access control policies is error-prone. Therefore, cloud providers have developed SMT-based tools to formally analyze the user-defined policies. Unfortunately, we find these analyzers slow, due to the complex \emph{regular expression matching} conditions in policies. To this end, this paper introduces RELIA, a general method to speed up the analysis of cloud access control policies. The key idea of RELIA is to pre-compute a set of \emph{String Equivalence Classes (SECs)} based on the regular expressions in a policy, assign a unique integer to each SEC, and rewrite the regular constraints into equivalent integer constraints, which are easier to solve. We implement RELIA as a transparent layer between our in-house access analyzer and off-the-shelf SMT solvers. Based on real policies from a large public cloud provider, we show that: when enabling RELIA, our in-house portfolio solver (consisting of Z3, CVC4, and CVC5) can speed up the analysis process for nearly 95% of all cases, with an average speedup of $8.21\times$. (2) for 95.0% of cases, RELIA can speed up the portfolio solver.


## 29. ScaleCirc: Scaling the Analysis over Circom Circuits

**Authors:** Jinan Jiang (The Hong Kong Polytechnic University), Haoran Qin (The Hong Kong Polytechnic University), Xiapu Luo (Hong Kong Polytechnic University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334720

**中文总结:** 提出 ScaleCirc，通过电路去重、约束可满足性传播与可扩展分析框架加速 Circom 零知识电路分析；评测 691 个真实电路并发现 Circomlib 中 3 个此前未报告的欠约束缺陷。

**Abstract:** Zero-knowledge proof (ZKP) circuits implemented in programming languages like Circom are fundamental to blockchain and privacy-preserving applications. These codes often suffer from constraint-related issues where constraints fail to accurately specify intended computations. While existing analysis tools have been proposed, they struggle with large-scale circuits containing complex template embeddings. We present ScaleCirc, a novel framework that addresses such limitations through: 1) systematic management of analysis redundancy via circuit deduplication strategies; 2) constrainedness propagation methods leveraging source code semantic information; and 3) a generalizable framework for different circuit analysis tasks. Evaluation on 691 real-world circuits shows ScaleCirc demonstrates higher efficiency, and successfully analyzes many Circom programs that existing works failed on. We also identified 3 previously unreported under-constrained bugs in the Circomlib library.


## 30. SMTgazer: Learning to Schedule SMT Algorithms via Bayesian Optimization

**Authors:** Chuan Luo (Beihang University), Shaoke Cui (Beihang University), Jianping Song (Beihang University), Xindi Zhang (State Key Laboratory of Computer Science, Institute of Software, Chinese Academy of Sciences, China), Wei Wu (Central South University; Xiangjiang Laboratory), Chanjuan Liu (Dalian University of Technology), Shaowei Cai (Institute of Software at Chinese Academy of Sciences), Chunming Hu (Beihang University)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334368

**中文总结:** 提出 SMTgazer，将 SMT 求解建模为超参优化下的求解器序列调度问题，用贝叶斯优化学习全局鲁棒调度策略，克服单求解器难以通吃各类实例的局限。

**Abstract:** Satisfiability Modulo Theories (SMT) plays a critical role in various software engineering applications, including program verification, symbolic execution, and automated test generation. Over the years, a wide range of SMT solvers has been developed, typically designed for general purposes or tailored to specific background theories, such as bit-vectors or nonlinear arithmetic. Due to the diversity and complexity of SMT instances, no single solver consistently outperforms others across all problem domains. This motivates the need for algorithm selection strategies that can adaptively choose solvers based on the characteristics of the instances.

To overcome the limitations of single-solver selection, solving SMT as a scheduling problem, enabling a more fault-tolerant and effective use of multiple solvers in sequence. We model algorithm scheduling as a hyperparameter optimization problem, enabling efficient black-box search over solver sequences while treating the dataset as a whole, thus achieving globally optimized and robust scheduling strategies. The resulting scheduler called SMTgazer. To further enhance scheduling efficiency and solver performance, we propose two optimizations: leveraging unsupervised X-means clustering to create semantically coherent instance groups for localized model training, and augmenting the Bayesian optimization surrogate with boosting and bagging ensembles to improve generalization and mitigate overfitting, thereby yielding more reliable performance predictions for the sequential portfolio scheduler.

Extensive experiments are conducted to evaluate the performance of SMTgazer, utilizing six SMT benchmarks derived from real-world applications. It show that our approach consistently outperforms current state-of-the-art methods. Particularly, SMTgazer achieves a 44.65% reduction in PAR-2 score and 69.11% decrease in the number of unsolved instances, compared to the strongest competitor, Sibyl, demonstrating the effectiveness of formulating SMT algorithm scheduling as a hyperparameter optimization problem. We further analyze the generated scheduling sequences to uncover the design principles that explain the success of our method. Finally, we also empirically show that our approach is both robust and generalizable, and the proposed strategies are effective.


## 31. Spinner: Detecting Locking Violations in the eBPF Runtime

**Authors:** Priya Govindasamy (University of California, Irvine), Joseph Bursey (University of California, Irvine), Hsin-Wei Hung (Meta), Ardalan Amiri Sani (University of California, Irvine)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334301

**中文总结:** 提出 Gopher（论文标题 Spinner），用静态分析检测 eBPF runtime 中的锁违规，包括上下文混淆误用锁原语与嵌套 eBPF 导致的递归加锁；已发现 34 个锁相关缺陷。

**Abstract:** The eBPF technology is widely used for many applications including tracing, packet filtering, network usage monitoring, and so on. The versatility of eBPF allows the kernel’s capabilities to be extended without needing to modify source code or load kernel modules. However, the eBPF subsystem may introduce new bugs that could lead to crashes, data loss, and other issues that can negatively impact system stability, reliability, availability, security, and overall performance. Specifically, locking violations, which occur when locks are not used correctly, can lead to problems like deadlocks and system hangs. Since eBPF operates at the kernel level, errors here have far-reaching consequences.

To tackle this issue, we present Gopher, a tool for detecting locking violations in the eBPF runtime. Gopher uses static analysis to (1) detect cases of context confusion where incorrect locking primitives are used in eBPF helper functions given their execution context, and (2) identify locks in helper functions that can be called recursively using nested eBPF programs. Both of these situations could result in deadlocks. So far, Gopher has identified 34 locking violation bugs in the eBPF subsystem in Linux, only 5 of which were previously found by Syzbot.


## 32. Towards More Accurate Static Analysis for Taint-style Bug Detection in Linux Kernel

**Authors:** Haonan Li (University of California at Riverside, USA), Hang Zhang (Indiana University), Kexin Pei (The University of Chicago), Zhiyun Qian (University of California at Riverside, USA)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334600

**中文总结:** 提出 BugLens 后处理框架，引导 LLM 按结构化步骤评估 Linux 内核污点类静态分析告警的安全影响与约束有效性；将精度从 0.10 提升至约 0.72（约 7 倍），并新发现 4 个未报告漏洞。

**Abstract:** Static analysis plays a crucial role in software vulnerability detection, yet faces a persistent precision-scalability trade-off. In large codebases like the Linux kernel, traditional static analysis tools often generate excessive false positives due to simplified vulnerability modeling and over-approximation of path and data constraints. While Large Language Models (LLMs) demonstrate promising code understanding capabilities, their direct application to program analysis remains unreliable due to inherent reasoning limitations.

We introduce BugLens, a post-refinement framework that significantly enhances static analysis precision for bug detection. BugLens guides LLMs through structured reasoning steps to assess security impact and validate constraints from the source code. When evaluated on Linux kernel’s taint-style bugs detected by static analysis tools, BugLens improves precision approximately 7-fold (from 0.10 to 0.72), substantially reducing false positives while uncovering four previously unreported vulnerabilities. Our results demonstrate that a well-structured, fully-automated LLM-based workflow can effectively complement and enhance traditional static analysis techniques.


## 33. Uncovering Discrimination Clusters: Quantifying and Explaining Systematic Fairness Violations

**Authors:** Ranit Debnath Akash (University of Illinois Chicago), Ashish Kumar (Pennsylvania State University), Verya Monjezi (University of Illinois Chicago), Ashutosh Trivedi (University of Colorado Boulder), Gang (Gary) Tan (Pennsylvania State University), Saeid Tizpaz-Niari (University of Illinois Chicago)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334575

**中文总结:** 提出 discrimination clustering 概念，将个体公平性违规推广为输入空间中受保护属性微扰导致输出形成 k 个显著不同簇的系统歧视模式；可量化并解释算法决策中的聚类式不公平。

**Abstract:** Fairness in algorithmic decision-making is often framed in terms of individual fairness, which requires that similar individuals receive similar outcomes. A system violates individual fairness if there exists a pair of inputs differing only in protected attributes (such as race or gender) that lead to significantly different outcomes—for example, one favorable and the other unfavorable. While this notion highlights isolated instances of unfairness, it fails to capture broader patterns of systematic or \emph{clustered discrimination} that may affect entire subgroups.

We introduce and motivate the concept of \emph{discrimination clustering}, a generalization of individual fairness violations. Rather than detecting single counterfactual disparities, we seek to uncover regions of the input space where small perturbations in protected features lead to \emph{k-significantly distinct clusters} of outcomes. That is, for a given input, we identify a local neighborhood—differing only in protected attributes—whose members’ outputs separate into many distinct clusters. These clusters reveal significant arbitrariness in treatment solely based on protected attributes that help expose patterns of algorithmic bias that elude pairwise fairness checks.

We present HyFair, a hybrid technique that combines formal symbolic analysis (via SMT and MILP solvers) to certify individual fairness with randomized search to discover discriminatory clusters. This combination enables both formal guarantees—when no counterexamples exist—and the detection of severe violations that are computationally challenging for symbolic methods alone. Given a set of inputs exhibiting high k-unfairness, we introduce a novel explanation method to generate interpretable, decision-tree-style artifacts. Our experiments demonstrate that HyFair outperforms state-of-the-art fairness verification and local explanation methods. In particular, HyFair reveals that some benchmarks exhibit significant discrimination clustering, while others show limited or no disparities with respect to protected attributes. It also provides intuitive explanations to support understanding and mitigation of unfairness.


## 34. VERT: Polyglot Verified Equivalent Rust Transpilation with Large Language Models

**Authors:** Aidan Z.H. Yang (Carnegie Mellon University), Yoshiki Takashima (Yale Law School), Brandon Paulsen (Amazon), Joey Dodds (Amazon), Daniel Kroening (Amazon)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334597

**中文总结:** 提出 VERT 多语言经形式验证的 Rust 转译器：经 WASM 编译得到 oracle Rust，LLM 生成更地道候选实现，再用模型检测证明等价；支持任意可编译至 WASM 的源语言并兼顾安全性与可维护性。

**Abstract:** Rust is a programming language that combines memory safety and low-level control, providing C-like performance while guaranteeing the absence of undefined behaviors by default. Rust’s growing popularity has prompted research on correct and idiomatic transpiling of existing code-bases to Rust. Existing work falls into two categories: rule-based and large language model (LLM)-based. While rule-based approaches are theoretically sound, they often yield unidiomatic and unsafe Rust code while targeting a few source languages, hindering maintainability and industrial application. In contrast, LLM-based approaches, while providing no guarantees, are polyglot and typically produce more idiomatic and safe Rust code. In this work, we present VERT, a formally correct, polyglot Rust translator with more idiomatic outputs. VERT supports any language that compiles to Web Assembly. Using the Web Assembly compiler, VERT obtains an oracle Rust program. Leveraging the LLM, VERT generates an idiomatic candidate Rust program. This candidate is verified against the oracle with model-checking to ensure equivalence.


## 35. When Control Flows Deviate: Directed Grey-box Fuzzing with Probabilistic Reachability Analysis

**Authors:** Peihong Lin (National University of Defense Technology), Pengfei Wang (National University of Defense Technology), Xu Zhou (National University of Defense Technology), Wei Xie (University of Science and Technology of China), Xin Ren (National University of Defense Technology), Kai Lu (National University of Defense Technology, China)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11334417

**中文总结:** 提出 BinGo 二进制定向灰盒 fuzzer，用贝叶斯方法融合静态先验与动态观测估计间接边置信度，并引入 region 图与 probabilistic reachability 适应 COTS 二进制 CFG 不精确；提升目标可达性分析准确性与效率。

**Abstract:** Directed grey-box fuzzing (DGF) steers testing toward high-value targets, but developing effective DGF for commercial off-the-shelf (COTS) binaries is challenging due to the lack of accurate structural information (e.g., control-flow and call graphs), which causes control flows to deviate and misguide DGF’s reachability analysis. In this paper, we introduce BinGo, a tailored binary-level directed grey-box fuzzer, which can accommodate the flawed CFGs of COTS binaries and realize accurate and efficient reachability analysis. First, to quantify the inevitable inaccuracies of unexecuted indirect edges and analyze their impact on the reachability of basic blocks, we propose a Bayesian-based method. This method combines prior knowledge from static analysis with dynamic observations from fuzzing to estimate the confidence in correctly recovering indirect edges. Then, we present a new concept called \textit{region}, which redefines granularity for efficient reachability analysis by transforming the control-flow graph (CFG) into a region graph. Using the Bayesian results and region graph, we propose a custom fitness metric for binary-level DGF, termed \textit{probabilistic reachability}. This metric, based on a dynamically updated region graph and reachability scores, is adaptive, lightweight, and accommodates the inaccurate binary-level CFG. We implemented a prototype tool, BinGo, and evaluated it in the CGC dataset, CVE-Benchmark, and UniBench benchmark. Experimental results show that BinGo surpasses baseline fuzzers (AFL++, AFLGo, PDGF, UAFuzz, and 1dVul) in reaching target locations and triggering known vulnerabilities. Additionally, BinGo uncovered three new vulnerabilities in the real-world application cscope-15.9.

