# ISSTA 2026 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 4

## 1. Automated Dependency Optimization for Artifact-Based Build Systems

**Authors:** Hongxu Xu (University of Waterloo), Zhenyang Xu (University of Waterloo), Shane McIntosh (University of Waterloo), Chengnian Sun (University of Waterloo)

**Categories:** Evolution and Maintenance

**中文总结:** 提出语言无关的依赖优化方法 DepReduce，通过拓扑序上的依赖提升与扁平化最小化重建代价并证明最优性。BazelDepReduce 在 14 个项目中移除 250 个冗余依赖，9 个 PR 已合并，后续提交受影响比例中位数 26.3%。

**Abstract:** As projects grow, the maintenance of intra- and inter-project dependencies declarations becomes increasingly complex. If dependency maintenance is lax, redundant dependencies may accrue, inflating incremental build and test latencies. The heterogeneity of language- and tool-specific dependency expressions and the complexity of the dependency graphs that they specify exacerbate the challenge of identifying and removing redundant dependencies. To address these challenges, this paper introduces DepReduce, a dependency optimization approach designed to be language-agnostic and compatible with all languages supported by the underlying build system. We formalized the dependency optimization objective as minimizing rebuild cost. To achieve this objective, DepReduce performs dependency lifting and dependency flattening operations on the dependency graph in a topological order, and we proved that DepReduce is both correct and optimal.

To empirically evaluate the approach, we implemented BazelDepReduce, an automated dependency optimization tool for Bazel. Bazel is a modern build system with native support for multiple programming languages. We evaluated BazelDepReduce on 14 open-source projects written in five programming languages, with eleven of them achieving reductions in rebuild cost. In total, BazelDepReduce identified and removed 250 redundant dependencies, which we used to produce eleven Pull Requests (PRs). Nine PRs have been merged by the target projects, including Angular and Apache RocketMQ. These contributions affected up to 57.6% of subsequent commits, with a median of 26.3%. The two other PRs remain open, awaiting a response from project maintainers. We also adapted BazelDepReduce to support Buck and Cargo, further demonstrating the generalizability of our approach. These results demonstrate the effectiveness of our approach in optimizing dependencies across projects with different programming languages.


## 2. BCaLLM: Call Graph-Guided Python Breaking Change Detection with Large Language Models

**Authors:** Wei Cheng (Nanjing University), Chen Shen (Nanjing University), Huan Zhang (Nanjing University), Yuhan Wu (Nanjing University), Jingyue Yang (Nanjing University), Wei Hu (Nanjing University)

**Categories:** Evolution and Maintenance

**中文总结:** 提出 BCaLLM，融合 call graph 范围剪枝与 LLM 推理检测 Python 包 API 的细粒度 breaking change。在 PyBCEval 588 个 API 上 F1 较文本基线提升 3.71%–10.16%。

**Abstract:** Software libraries frequently evolve, introducing breaking changes that disrupt client applications. Existing detection approaches primarily target static programming languages or focus on syntactic changes, leaving behavioral breaking changes in dynamic languages such as Python underexplored. This task is particularly challenging due to two critical factors often overlooked in existing Python-centric research: side effects and call relationships, which implicitly alter API behaviors and propagate change impact. To address these challenges, we propose a generalized taxonomy of function API breaking changes. Grounded in Hyrum’s Law, our taxonomy is defined from the client’s perspective of observable behaviors and unifies both syntactic and behavioral categories in a multi‑label formulation. Furthermore, we present BCaLLM, a novel framework to detect fine-grained \underline{b}reaking \underline{c}hanges in Python packages by leveraging c\underline{a}ll graphs and \underline{l}arge \underline{l}anguage \underline{m}odels (LLMs). BCaLLM constructs a fused call graph to scope change impact, prunes compatible APIs and code context via memory‑based heuristics, and employs an LLM to detect specific breaking changes. We construct PyBCEval, a manually annotated benchmark of 588 APIs from 27 version pairs of 19 widely used Python packages. Experiments with diverse LLMs show that BCaLLM outperforms text-based baselines by 3.71%-10.16% and LLM-based baselines by 1.60%-4.83% in F1-score.


## 3. From Custom Logic to APIs: Understanding and Recommending API Replacement Refactorings

**Authors:** Bridget Nyirongo (Beijing Institute of Technology), Yanjie Jiang (Tianjin University), Yuxia Zhang (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** Evolution and Maintenance

**中文总结:** 首次大规模实证 API replacement refactoring 并提出 AKIRA 混合推荐框架；在手工数据集上 recall/precision 达 90%/88%，在 RETIWA 上将 recall 从 21% 提升至 81%。

**Abstract:** Software refactoring is essential for maintaining code quality. However, API replacement refactoring, which replaces custom logic with  API calls, remains less underexplored. Existing refactoring tools often fail to detect such opportunities due to their reliance on rigid templates and their inability to capture complex, multi-statement semantic equivalents. To bridge this gap, we conduct the first empirical study of API replacement refactorings, analyzing 166,299 commits across six open-source Java projects to quantify their occurrence and to characterize their scope, categories, and recurring patterns. Based on these insights, we propose AKIRA (Adaptive Knowledge Discovery and Retrieval), a hybrid framework that integrates pattern-deterministic heuristics with a refactoring-aware knowledge base to assess the practical feasibility of recommending API replacement refactorings. Our evaluation shows that AKIRA achieves 90% recall and 88% precision on a manually curated dataset. Furthermore, on the external RETIWA dataset, AKIRA significantly improves the state of the art by increasing recall from 21% to 81% and precision from 40% to 78%. These results demonstrate the effectiveness of combining static pattern matching with semantic reasoning to support the automation of recommending complex API replacement refactorings.


## 4. Guarding the Lifeline: A First Look and Automated Defect Diagnosis for ROS Central Index

**Authors:** Weijie Sun (State Key Lab for Novel Software Technology and School of Computer Science, Nanjing University, China), Huiyan Wang (Nanjing University), Ying Wang (Northeastern University), Chang Xu (Nanjing University)

**Categories:** Evolution and Maintenance

**中文总结:** 首次系统研究 ROS central index 缺陷并提出 RosdepAuditor，用跨仓库 hybrid scoring 推断包等价关系；映射准确率 95.2%，在 live index 发现 3062 个潜在缺陷。

**Abstract:** The Robot Operating System (ROS) relies on a centralized dependency index, rosdistro \emph{central index}, to manage packages across its heterogeneous software ecosystem, which integrates independently evolving Operating System (OS) repositories for system libraries, ROS repositories for domain-specific support, and Programming Language (PL) repositories for functional modules. While this design enables portability, it introduces a critical fragility since the entire ROS dependency management depends on this manually curated, static index that must map packages across independently evolving, multi-source repositories. This leads to persistent defects in the central index, such as missing, incorrect, or outdated installation rules, which undermine the reliability of ROS dependency management. To address this problem, we conducted the first in-depth empirical study of 863 real-world maintenance cases for the ROS central index. We categorize defects into coverage and correctness types, identify their root structural causes, and demonstrate that manual maintenance is bottlenecked by the difficulty of identifying equivalent packages across repositories. Motivated by these findings, we propose RosdepAuditor, an automated auditing framework that introduces a cross-repository mapping mechanism with hybrid scoring to infer package equivalence and detect defects. Evaluated on a ground-truth dataset, RosdepAuditor achieves 95.2% mapping accuracy without generating non-existent packages, outperforming existing pattern-based and upstream-based approaches, and leading LLM models. When applied to the live index, it uncovered 3,062 potential defects across 2,121 entries, 46 of which have been verified and fixed, demonstrating its practical usefulness in strengthening ROS dependency management.

