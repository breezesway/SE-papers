# FSE 2025 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 14 papers

## 1. A New Approach to Evaluating Nullability Inference Tools

**Authors:** Nima Karimipour (University of California, Riverside), Erfan Arvan (New Jersey Institute of Technology), Martin Kellogg (New Jersey Institute of Technology), Manu Sridharan (University of California at Riverside)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715732

**中文总结:** 指出用「类型重建」评估空值注解推断会因开发者为通过检查改代码而产生偏差；提出新的最优推断定义并对三个工具做首次对比，揭示互补优势与不足。

**Abstract:** Null-pointer exceptions are serious problem for Java, and researchers have developed type-based nullness checking tools to prevent them. These tools, however, have a downside: they require developers to write nullability annotations, which is time-consuming and hinders adoption. Researchers have therefore proposed nullability annotation inference tools, whose goal is to (partially) automate the task of annotating a program for nullability. However, prior works rely on differing theories of what makes a set of nullability annotations good, making comparing their effectiveness challenging. In this work, we identify a systematic bias in some prior experimental evaluation of these tools: the use of “type reconstruction” experiments to see if a tool can recover erased developer-written annotations. We show that developers make semantic code changes while adding annotations to facilitate typechecking, leading such experiments to overestimate the effectiveness of inference tools on never-annotated code. We propose a new definition of the “best” inferred annotations for a program that avoids this bias, based on a systematic exploration of the design space. With this new definition, we perform the first head-to-head comparison of three extant nullability inference tools. Our evaluation showed the complementary strengths of the tools, and remaining weaknesses that could be addressed in future work.

## 2. An Empirical Study of Suppressed Static Analysis Warnings

**Authors:** Huimin Hu (University of Stuttgart), Yingying Wang (University of British Columbia), Julia Rubin (The University of British Columbia), Michael Pradel (University of Stuttgart)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Available, Artifact-Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715729

**中文总结:** 首次深入实证研究多语言项目中四类静态分析告警的 suppressions：较常见且随时间增多，50.8% 实际不抑制任何告警却可能无意隐藏未来告警；主因包括误报、配置不当与误导性消息。

**Abstract:** Scalable static analyzers are popular tools for finding incorrect, inefficient, insecure, and hard-to-maintain code early during the development process. Because not all warnings reported by a static analyzer are immediately useful to developers, many static analyzers provide a way to suppress warnings, e.g., in the form of special comments added into the code. Such \emph{suppressions} are an important mechanism at the interface between static analyzers and software developers, but little is currently known about them. This paper presents the first in-depth empirical study of suppressions of static analysis warnings, addressing questions about the prevalence of suppressions, their evolution over time, the relationship between suppressions and warnings, and the reasons for using suppressions. We answer these questions by studying projects written in three popular languages and suppressions for warnings by four popular static analyzers. Our findings show that (i) suppressions are relatively common, e.g., with a total of 7,357 suppressions in 46 Python projects, (ii) the number of suppressions in a project tends to continuously increase over time, (iii) surprisingly, 50.8% of all suppressions do not affect any warning and hence are practically useless, (iv) some suppressions, including useless ones, may unintentionally hide future warnings, and (v) common reasons for introducing suppressions include false positives, suboptimal configurations of the static analyzer, and misleading warning messages. These results have actionable implications, e.g., that developers should be made aware of useless suppressions and the potential risk of unintentional suppressing, that static analyzers should provide better warning messages, and that static analyzers should separately categorize warnings from third-party libraries.

## 3. Blended Analysis for Predictive Execution

**Authors:** Yi Li (University of Texas at Dallas), Hridya Dhulipala (University of Texas at Dallas), Aashish Yadavally (University of Texas at Dallas), Xiaokai Rong (University of Texas at Dallas), Shaohua Wang (Central University of Finance and Economics), Tien N. Nguyen (University of Texas at Dallas)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729402

**中文总结:** 提出 CodEx，将程序分析与 LLM 融合做 Python 预测执行，用确定性路径与按变量的预测后向切片简化估值；相对 SOTA 全轨迹准确率最高相对提升 26%，并可用于静态覆盖与运行时错误预测。

**Abstract:** Although Large Language Models (LLMs) are highly proficient in understanding source code and descriptive texts, they have limitations in reasoning on dynamic program behaviors, such as execution trace and code coverage prediction, and runtime error prediction, which usually require actual program execution. To advance the ability of LLMs in predicting dynamic behaviors, we leverage the strengths of both approaches, Program Analysis (PA) and LLM, in building CodEx, a predictive executor for Python. Our principle is a blended analysis between PA and LLM to use PA to guide the LLM in predicting execution traces. We break down the task of predictive execution into smaller sub-tasks and leverage the deterministic nature when an execution order can be deterministically decided. When it is not certain, we use predictive backward slicing per variable, i.e., slicing the prior trace to only the parts that affect each variable separately breaks up the valuation prediction into significantly simpler problems. Our empirical evaluation on real-world datasets shows that CodEx achieves up to 26% relatively higher accuracy in predicting full execution traces than the state-of-the-art models. It also produces up to 41.7% correct execution trace prefixes than those baselines. In predicting next executed statements, its relative improvement over the baselines is up to 82.1%. Finally, we show CodEx’s usefulness in two tasks: static code coverage analysis and prediction of run-time errors for (in)complete code snippets.

## 4. CKTyper: Enhancing Type Inference for Java Code Snippets by Leveraging Crowdsourcing Knowledge in Stack Overflow

**Authors:** Anji Li, Neng Zhang, Ying Zou, Zhixiang Chen, Jian Wang, Zibin Zheng

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715724

**中文总结:** 提出 CKTyper，从 Stack Overflow 众包帖子检索相似代码片段并构建上下文，结合 ChatGPT 与 API 类型字典为 Java 代码片段推断 API 类型；在两个开源数据集上精度/召回最高达 97.80%/95.54%，显著优于现有基线。

**Abstract:** Code snippets are widely used in technical forums to demonstrate solutions to programming problems. They can be leveraged by developers to accelerate problem-solving. However, code snippets often lack concrete types of the APIs used in them, which impedes their understanding and resue. To enhance the description of a code snippet, a number of approaches are proposed to infer the types of APIs. Although existing approaches can achieve good performance, their performance is limited by ignoring other information outside the input code snippet (e.g., the descriptions of similar code snippets) that could potentially improve the performance. In this paper, we propose a novel type inference approach, named CKTyper, by leveraging crowdsourcing knowledge in technical posts. The key idea is to generate a relevant context for a target code snippet from the posts containing similar code snippets and then employ the context to promote the type inference with large language models (e.g., ChatGPT). More specifically, we build a crowdsourcing knowledge base (CKB) by extracting code snippets from a large set of posts and index the CKB using Lucene. An API type dictionary is also built from a set of API libraries. Given a code snippet to be inferred, we first retrieve a list of similar code snippets from the indexed CKB. Then, we generate a crowdsourcing knowledge context (CKC) by extracting and summarizing useful content (e.g., API-related sentences) in the posts that contain the similar code snippets. The CKC is subsequently used to improve the type inference of ChatGPT on the input code snippet. The hallucination of ChatGPT is eliminated by employing the API type dictionary. Evaluation results on two open-source datasets demonstrate the effectiveness and efficiency of CKTyper. CKTyper achieves the optimal precision/recall of 97.80% and 95.54% on both datasets, respectively, significantly outperforming three state-of-the-art baselines and ChatGPT.

## 5. DyLin: A Dynamic Linter for Python

**Authors:** Aryaz Eghbali (University of Stuttgart), Felix Burk (University of Stuttgart), Michael Pradel (University of Stuttgart)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729395

**中文总结:** 提出 Python 首个动态 linter DyLin，通过运行时检查 15 类难以静态发现的语言特有反模式。在超 683k 行开源与 Kaggle 代码上报告 68 个问题，精度 86.8%，并与静态工具形成互补。

**Abstract:** Python is a dynamic language with applications in many domains, and one of the most popular languages in recent years. To achieve higher code quality, developers have turned to “linters” that statically analyze the source code and warn about potential programming problems. However, the inherent limitations of static analysis and the dynamic nature of Python make it difficult or even impossible for static analysis to detect some problems. This paper presents DyLin, the first dynamic linter for Python. Similar to a traditional linter, the approach has an extensible set of checkers, which, unlike in traditional linters, search for specific programming anti-patterns by analyzing the program as it executes. A key contribution of this paper is a set of 15 Python-specific anti-patterns that are hard to find statically but amenable to dynamic analysis, along with corresponding checkers to detect them. Our evaluation applies DyLin to 37 popular open-source Python projects on GitHub and to a dataset of code submitted to Kaggle machine learning competitions, totaling over 683k lines of Python code. The approach reports a total of 68 problems, 59 of which are previously unknown true positives, i.e., a precision of 86.8%. The detected problems include bugs that cause incorrect values, such as inf, incorrect behavior, e.g., missing out on relevant events, unnecessary computations that slow down the program, and unintended data leakage from test data to the training phase of machine learning pipelines. These issues remained unnoticed in public repositories for more than 3.5 years, on average, despite the fact the corresponding code has been exercised by the developer-written tests. A comparison with popular static linters and a type checker shows that DyLin complements these tools by detecting problems that are missed statically. Based on our reporting of 42 issues to the developers, 23 issues have so far been fixed.

## 6. Dynamic Taint Tracking for Modern Java Virtual Machines

**Authors:** Katherine Hough (Northeastern University), Jonathan Bell (Northeastern University)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Available, Artifact-Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729349

**中文总结:** 提出 Galette，融合 shadowing 与 mirroring 以在现代 JVM 上实现精确且稳健的动态污点传播。在 3451 个合成程序上跨四个 Java LTS 版本达到完美精度，并在真实程序上保持与现有系统相当的开销。

**Abstract:** Dynamic taint tracking is a program analysis that traces the flow of information through a program. In the Java virtual machine (JVM), there are two prominent approaches for dynamic taint tracking: “shadowing” and “mirroring”. Shadowing is able to precisely track information flows, but is also prone to disrupting the semantics of the program under analysis. Mirroring is better able to preserve program semantics, but often inaccurate. The limitations of these approaches are further exacerbated by features introduced in the latest Java versions. In this paper, we propose Galette, an approach for dynamic taint tracking in the JVM that combines aspects of both shadowing and mirroring to provide precise, robust taint tag propagation in modern JVMs. On a benchmark suite of 3,451 synthetic Java programs, we found that Galette was able to propagate taint tags with perfect accuracy while preserving program semantics on all four active long-term support versions of Java. We also found that Galette’s runtime and memory overheads were competitive with that of two state-of-the-art dynamic taint tracking systems on a benchmark suite of twenty real-world Java programs.

## 7. Expressing and Checking Statistical Assumptions

**Authors:** Alexi Turcotte (CISPA), Zheyuan Wu (Saarland University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729391

**中文总结:** 提出为统计库函数标注假设并自动插入假设检验的方法，实现为 Python/R 工具 prob-check-py 与 prob-check-r。在 128 个 Kaggle notebook 中发现 84.38% 至少违反一项假设，且在 11.51% 情形下若选对检验会得出不同结论。

**Abstract:** Literate programming environments like Jupyter and R Markdown notebooks, coupled with easy-to-use languages like Python and R, put a plethora of statistical methods right at a data analyst’s fingertips. But are these methods being used correctly? Statistical methods make statistical assumptions about samples being analyzed, and in many cases produce reasonable looking results even if assumptions are not met. We propose an approach that allows library developers to annotate functions with statistical assumptions, phrases them as hypotheses about the data, and inserts hypothesis tests investigating the likelihood that the assumption is met. As a proof of concept, we implement this approach in two tools: prob-check-py for Python, and prob-check-r for R. To evaluate these, we identify common hypothesis testing and statistical modeling functions in Python and R, annotate them with the relevant statistical assumptions, and run 128 Kaggle notebooks that use those methods to identify misuses. Our investigation reveals that at least one statistical assumption was violated in 84.38% of surveyed notebooks, and that assumptions were violated in 53.36% of calls to annotated functions. Moreover, had the appropriate hypothesis testing method been chosen given the characteristics of the data, a different conclusion would have been drawn in 11.51% of cases.

## 8. HornBro: Homotopy-like Method for Automated Quantum Program Repair

**Authors:** Siwei Tan (Zhejiang University), Liqiang Lu (Zhejiang University), Debin Xiang (Zhejiang University), Tianyao Chu (Zhejiang University), Congliang Lang (Zhejiang University), Jintao Chen (Zhejiang University), Xing Hu (Zhejiang University), Jianwei Yin (Zhejiang University)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715751

**中文总结:** 提出 HornBro，以 homotopy 式在经典与量子部分间迭代，将量子程序自动修复的指数开销降至多项式复杂度。相对既有技术修复成功率提高超 62.5%，并实现约 35.7× 加速与 99.9% 的补丁门电路精简。

**Abstract:** Quantum programs provide exponential speedups compared to classical programs in certain areas, But they also inevitably encounter logical faults. Automatically repairing quantum programs is much more challenging than repairing classical programs due to the non-replicability of data, the vast search space of program inputs, and the new programming paradigm. Existing works based on semantic-based or learning-based program repair techniques are fundamentally limited in repairing efficiency and effectiveness. In this work, we propose HornBro, the first work that reduces the exponential overhead of the automated quantum repair to a polynomial complexity. The key insight of HornBro lies in the homotopy-like method, which iteratively switches between the classical part and the quantum part. This approach allows the repair tasks to be efficiently offloaded to the most suitable platforms, enabling a progressive convergence toward the correct program. We start by designing an implication assertion pragma to enable rigorous specifications of quantum program behavior, which helps to automatically generate a quantum test suite. This suite leverages the orthonormal bases of quantum programs to accommodate different encoding schemes. Given a fixed number of test cases, it allows the maximum input coverage of potential counter-example candidates. Then, we develop a Clifford approximation method with SMT-based search to transform the fault localization program into a symbolic reasoning problem. Finally, we offload the computationally intensive repair of gate parameters to quantum hardware by leveraging the differentiability of quantum gates. Experiments suggest that HornBro increases the repair success rate by more than 62.5% compared to the existing repair techniques, supporting more types of quantum bugs. It also achieves 35.7$\times$ speedup in the repair and 99.9% gate reduction of the patch.

## 9. PDCAT: Preference-Driven Compiler Auto-Tuning

**Authors:** Mingxuan Zhu (Peking University), Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Dan Hao (Peking University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715756

**中文总结:** PDCAT 通过文档中的组合约束、公共/探索优化划分，以及偏置的启用概率，压缩编译器优化序列搜索空间。在 GCC 最新版与 cBench/PolyBench 上显著优于含 SRTuner 在内的四种方法，且各组件可提升对照技术的加速效果。

**Abstract:** Compilers are crucial software tools that usually convert programs in high-level languages into machine code. A compiler provides hundreds of optimizations to improve the performance of the compiled code, which are controlled by enabled or disabled optimization flags. However, the vast number of combinations of these flags makes it extremely challenging to select the desired settings for compiler optimization flags (i.e., an optimization sequence) for a given target program. In the literature, many auto-tuning techniques have been proposed to select a desired optimization sequence via different strategies across the entire optimization space. However, due to the huge optimization space, these techniques commonly suffer from the widely-recognized efficiency problem. To address this problem, in this paper, we propose a preference-driven selection approach PDCAT, which reduces the search space of optimization sequences through the following three components. In particular, PDCAT first identifies combined optimizations based on compiler documentation to exclude the optimization sequences violating the combined constraints, and then categorizes the optimizations into a common optimization set (whose optimization flags are fixed) and an exploration set containing the remaining optimizations. Finally, within the search process, PDCAT assigns distinct enable probabilities to the explored optimization flags and finally selects a desired optimization sequence. The former two components reduce the search space by removing invalid optimization sequences and fixing some optimization flags, whereas the latter performs a biased search in the search space. To evaluate the performance of the proposed approach PDCAT, we conduct an extensive experimental study on the latest version of the compiler GCC with two widely used benchmarks cBench and PolyBench. The results show that PDCAT significantly outperforms the four compared techniques, including the state-of-art technique SRTuner. Moreover, each component of PDCAT not only contributes to its performance but also improves the acceleration performance of compared techniques.

## 10. QSF: Multi-Objective Optimization based Efficient Solving for Floating-Point Constraints

**Authors:** Xu Yang (College of Computer Science and Technology, National University of Defense Technology), Zhenbang Chen (College of Computer, National University of Defense Technology), Wei Dong (National University of Defense Technology), Ji Wang (National University of Defense Technology)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715739

**中文总结:** QSF 将浮点约束求解建模为多目标优化（未满足约束数量与违规模之和），并设计面向浮点数的进化变异算子。在 SMT-COMP 与真实浮点程序基准上相对 SOTA 加速可达数十至上百倍，并提升浮点程序符号执行性能。

**Abstract:** Floating-point constraint solving is challenging due to the complex representation and non-linear computations. Search-based constraint solving provides an effective method for solving floating-point constraints. In this paper, we propose QSF to improve the efficiency of search-based solving for floating-point constraints. The key idea of QSF is to model the floating-point constraint solving problem as a multi-objective optimization problem. Specifically, QSF considers both the number of unsatisfied constraints and the sum of the violation degrees of unsatisfied constraints as the objectives for search-based optimization. Besides, we propose a new evolutionary algorithm in which the mutation operators are specially designed for floating-point numbers, aiming to solve the multi-objective problem more efficiently. We have implemented QSF and conducted extensive experiments on both the SMT-COMP benchmark and the benchmark from real-world floating-point programs. The results demonstrate that compared to SOTA floating-point solvers, QSF achieved an average speedup of 15.72X under a 60-second timeout and an impressive 87.48X under a 600-second timeout on the first benchmark. Similarly, on the second benchmark, QSF delivered an average speedup of 25.74X and 106.76X, respectively, under the two timeout configurations. Furthermore, QSF has also enhanced the performance of symbolic execution for floating-point programs.

## 11. Revisiting Optimization-Resilience Claims in Binary Diffing Tools: Insights from LLVM Peephole Optimization Analysis

**Authors:** Xiaolei Ren (Macau University of Science and Technology), Mengfei Ren (University of Alabama in Huntsville), Jeff Yu Lei (University of Texas at Arlington), Jiang Ming (Tulane University, USA)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729389

**中文总结:** 本文用定制 LLVM 翻译验证工具剖析 peephole 优化对二进制比对的影响，发现其贯穿优化过程且主要造成过程内差异，现有基本块中心比对工具难以全覆盖。并发布 peephole-oriented 测试套件，挑战既有“对优化免疫”的宣称。

**Abstract:** Binary diffing technique aims to identify differences/similarities in executable files without source code access. Its potential applications in various software security tasks, such as vulnerability search, code clone detection, and malware analysis have generated a large body of literature over the past few years. A recurring theme in binary diffing research is to evaluate the resilience against the impact of compiler optimization, which is the most common source leading to syntactic differences in binary code. Despite claims by most binary diffing papers that they are immune to compiler optimization, recent studies have highlighted a pressing need for the research community to revisit these optimization-resilience claims. In this paper, we investigate peephole optimization’s impact on binary diffing. Mainstream compilers feature a multitude of peephole optimization rules, facilitating local rewriting of input programs to replace instruction sequences within a window (i.e., peephole) with shorter and/or faster equivalents. Our research reveals that peephole optimization primarily affects binary code differences at the intra-procedural level, which contradicts the assumptions made by basic-block centric comparison approaches. We customized an LLVM translation validation tool to investigate the impact of peephole optimization from the overall optimization process. Our experimental results demonstrate 1) peephole optimization modifies binary code during the whole optimization process, and 2) no existing basic-block centric comparison tools can properly deal with all changes caused by peephole optimization, leading to further performance loss in downstream applications. Our study introduces a ``peephole-oriented'' test suite, designed to isolate and measure the impact of peephole optimizations on binary code. This suite provides a new perspective for evaluating the resilience of binary diffing tools against subtle, intra-procedural code changes, setting a new benchmark for future tool development. Our findings reveal critical insights that challenge existing assumptions in binary diffing, highlighting the need for more robust analysis techniques.

## 12. ROSCallBaX: Statically Detecting Inconsistencies In Callback Function Setup of Robotic Systems

**Authors:** Sayali Kate (Purdue University), Yifei Gao (Purdue University), Shiwei Feng (Purdue University), Xiangyu Zhang (Purdue University)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Available, Artifact-Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715748

**中文总结:** ROSCallBaX 静态抽取 ROS 回调及其执行配置的组合视图，并对照跨 ROS1/ROS2、C++/Python 的语义约定检测不一致。在开发者论坛与公开 ROS 项目数据集上可检出真实不一致，包括运行时不报错的隐患。

**Abstract:** Increasingly popular Robot Operating System (ROS) framework allows building robotic systems by integrating newly developed and/or reused modules, where the modules can use different versions of the framework (e.g., ROS1 or ROS2) and programming language (e.g. C++ or Python). The majority of such robotic systems’ work happens in callbacks. The framework provides various elements for initializing callbacks and for setting up the execution of callbacks. It is the responsibility of developers to compose callbacks and their execution setup elements, and hence can lead to inconsistencies related to the setup of callback execution due to developer’s incomplete knowledge of the semantics of elements in various versions of the framework. Some of these inconsistencies do not throw errors at runtime, making their detection difficult for developers. We propose a static approach to detecting such inconsistencies by extracting a static view of the composition of robotic system’s callbacks and their execution setup, and then checking it against the composition conventions based on the elements’ semantics. We evaluate our ROSCallBaX prototype on the dataset created from the posts on developer forums and ROS projects that are publicly available. The evaluation results show that our approach can detect real inconsistencies.

## 13. Towards Diverse Program Transformations for Program Simplification

**Authors:** Haibo Wang (Concordia University), Zezhong Xing (Southern University of Science and Technology), Chengnian Sun (University of Waterloo), Zheng Wang (University of Leeds), Shin Hwei Tan (Concordia University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715730

**中文总结:** 通过分析 382 个 PR 刻画真实开发者的程序简化变换与动机，并据此提出 SimpT5，结合修改行定位与质量检查器自动生成语义等价且行数更少的简化程序。在大规模简化数据集上优于已有自动化简化方法。

**Abstract:** By reducing the number of lines of code, program simplification reduces code complexity, improving software maintainability and code comprehension. While several existing techniques can be used for automatic program simplification, there is no consensus on the effectiveness of these approaches. We present the first study on how real-world developers simplify programs in open-source software projects. By analyzing 382 pull requests from 296 projects, we summarize the types of program transformations used, the motivations behind simplifications, and the set of program transformations that have not been covered by existing refactoring types. As a result of our study, we submitted eight bug reports to a widely used refactoring detection tool, RefactoringMiner where seven were fixed. Our study also identifies gaps in applying existing approaches for automating program simplification and outlines the criteria for designing automatic program simplification techniques. In light of these observations, we propose SimpT5, a tool to automatically produce simplified programs that are semantically equivalent programs with reduced lines of code. SimpT5 is trained on our collected dataset of 92,485 simplified programs with two heuristics: (1) modified line localization that encodes lines changed in simplified programs, and (2) checkers that measure the quality of generated programs. Experimental results show that SimpT5 outperforms prior approaches in automating developer-induced program simplification.

## 14. Why the Proof Fails in Different Versions of Theorem Provers: An Empirical Study of Compatibility Issues in Isabelle

**Authors:** Xiaokun Luan (Peking University), David Sanan (Singapore Institute of Technology), Zhe Hou (Griffith University), Qiyuan Xu (Nanyang Technological University), Chengwei Liu (Nanyang Technological University), Yufan Cai (National University of Singapore), Yang Liu (Nanyang Technological University), Meng Sun (Peking University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715787

**中文总结:** 以 Isabelle 为例，构建回归测试框架从 Archive of Formal Proofs 自动收集 12,079 个证明助手版本兼容性问题，归纳类型、症状、根因与修复策略。为缓解形式化证明维护中的兼容性障碍提供实证基础。

**Abstract:** Proof assistants are software tools for formal modeling and verification of software, hardware, design, and mathematical proofs. Due to the growing complexity and scale of formal proofs, compatibility issues frequently arise when using different versions of proof assistants. These issues result in broken proofs, disrupting the maintenance of formalized theories and hindering the broader dissemination of results within the community. Although existing works have proposed techniques to address specific types of compatibility issues, the overall characteristics of these issues remain largely unexplored. To address this gap, we conduct the first extensive empirical study to characterize compatibility issues, using Isabelle as a case study. We develop a regression testing framework to automatically collect compatibility issues from the Archive of Formal Proofs, the largest repository of formal proofs in Isabelle. By analyzing 12,079 collected issues, we identify their types and symptoms and further investigate their root causes. We also extract updated proofs that address these issues to understand the applied resolution strategies. Our study provides an in-depth understanding of compatibility issues in proof assistants, offering insights that support the development of effective techniques to mitigate these issues.
