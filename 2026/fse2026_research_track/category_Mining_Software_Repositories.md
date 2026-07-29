# FSE 2026 Research Track — Mining Software Repositories

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 4 papers

## 1. Characterizing and Mitigating False-Positive Bug Reports in the Linux Kernel

**Authors:** jiashuo tian (Tianjin University), Dong Wang (Tianjin University), Chen Yang (Tianjin University), Haichi Wang (Tianjin University), Zan Wang (Tianjin University), Junjie Chen (Tianjin University)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797082

**中文总结:** 首次系统刻画 Linux 内核误报缺陷报告：构建含 497 个误报的 2006 条报告数据集，发现误报耗时与真实缺陷相当且多见于文件系统/驱动；RAG 辅助 LLM 缓解误报可达 91% 召回与 88% F1。

**Abstract:** False-positive bug reports represent a significant yet underexplored challenge in the development and maintenance of the Linux kernel. They occur when correct system behavior is mistakenly flagged as a defect, consuming developer effort without leading to actual code improvements. Such reports can mislead developers, waste debugging resources, and delay the resolution of real bugs. In this paper, we present the first comprehensive empirical study of false-positive bug reports in the Linux kernel. We manually construct a dataset of 2,006 bug reports comprising 1,509 genuine bugs and 497 false positives collected from Bugzilla and Syzkaller. Our analysis indicates that false positives demand effort comparable to real bugs, often requiring extended discussions and non-trivial closure time. They occur in several components, especially File Systems and Drivers, mainly due to external dependencies and semantic misunderstandings. To address this challenge, we evaluate large language models (LLMs) for automated false-positive bug report mitigation. Among various prompting strategies, retrieval-augmented generation (RAG) performs best, achieving 91% recall and an F1 score of 88%. These findings highlight the non-negligible cost of false positive bug reports and show the promise of LLMs for more efficient false positive mitigation in the Linux kernel.

## 2. How Low Can You Go? The Data-Light SE Challenge

**Authors:** Kishan Kumar Ganguly (NC State), Tim Menzies (North Carolina State University)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808192

**中文总结:** 在百余项 SE 优化任务上表明，仅用数十个标签的简单方法即可达到最佳报告结果的 90% 以上，且不劣于 SMAC/TPE 等复杂优化器；据此提出 data-light challenge，并开源形式化、基线算法与公开数据实验。

**Abstract:** Much of software engineering (SE) research assumes that progress depends on massive datasets and CPU-intensive optimizers. Yet has this assumption been rigorously tested?

The counter-evidence presented in this paper suggests otherwise. For over 100 optimization tasks from recent SE papers (including software configuration,  performance tuning, product line engineering, project health forecasting, defect prediction, software testing, software process and cost estimation, and cross-domain generalization datasets), even with just a few dozen labels, very simple methods (e.g., diversity sampling, a minimal Bayesian learner, its distance-based non-parametric variant, or random probes) achieve over 90% of the best reported results. Furthermore, these simple methods perform just as well as more complex state-of-the-art optimizers like SMAC, TPE, DEHB, etc. While some tasks would require better outcomes and more sampling, these results seen after a few dozen samples would suffice for many engineering needs (particularly when the goal is rapid and cost-efficient guidance rather than slow and exhaustive optimization).

To say that another way,  at least some SE tasks are better served by lightweight approaches that demand fewer labels and far less computation.  We hence propose the data-light challenge: when will a handful of  labels suffice for SE tasks? To enable a large-scale investigation of this issue, we contribute (1) a mathematical formalization of labeling, (2) lightweight baseline algorithms, and (3) results on public-domain data showing the conditions under which lightweight methods excel or fail.

For the purposes of open science, our scripts and data are online at https://github.com/KKGanguly/NEO .

## 3. LinkAnchor: An Autonomous LLM-Based Agent for Issue-to-Commit Link Recovery

**Authors:** Arshia Akhavan (San Diego State University), Alireza Hoseinpour (Bowling Green State University), Abbas Heydarnoori (Bowling Green State University), Hamid Bagheri (University of Nebraska-Lincoln), Mehdi Keshani (University of Zurich, Zurich, Switzerland)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808191

**中文总结:** 提出 LinkAnchor，首个面向 issue–commit 链接恢复的自治 LLM agent，以 lazy-access 动态检索相关上下文并定位最终解决提交以重建提交链；在六个大型开源项目上 Hit@1 相对 SOTA 提升 41%–714%，单 issue 成本约 0.01 美元。

**Abstract:** Issue-to-commit link recovery plays a central role in software traceability and project management, yet it remains a challenging task. Prior studies show that only about 42.2% of issues on GitHub are correctly linked to their commits, highlighting the need for more effective solutions. Existing work has explored a range of ML/DL approaches, and more recently, large language models (LLMs) have been applied to this problem. However, these methods face two major limitations. First, LLMs are restricted by limited context windows and cannot simultaneously process all available data sources, such as long commit histories, extensive issue discussions, and large code repositories. Second, most approaches operate on individual issue–commit pairs, where the model determines for each pair whether the commit is related to the issue. While straightforward in design, this strategy quickly becomes impractical in repositories with tens of thousands of commits, as it requires exhaustively evaluating an enormous number of candidate pairs. To address these challenges, we present LinkAnchor, the first autonomous LLM-based agent designed specifically for issue-to-commit link recovery. LinkAnchor introduces a lazy-access architecture that allows the underlying LLM to dynamically retrieve only the most relevant contextual data, such as commits, issue comments, and code files, without exceeding token limits. Unlike prior approaches, LinkAnchor does not exhaustively score every possible pair but instead efficiently identifies the last resolving commit of an issue, enabling the complete reconstruction of the resolving commit chain and retrieval of all relevant commits. Our evaluations show that LinkAnchor outperforms state-of-the-art baselines by 41–714% in Hit@1 across six large-scale open-source projects, while costing only about 0.01 US dollars per issue. Finally, LinkAnchor is designed and tested for both GitHub and Jira, and its modular architecture makes it straightforward to extend to other platforms.

## 4. Mining Long Tail Bugs: Identifying Rare and Overlooked Issues in Code

**Authors:** Wentao Liang (Institute of Software, Chinese Academy of Sciences), Yanjun Wu (Institute of Software, Chinese Academy of Sciences), Xiang Ling (Institute of Software, Chinese Academy of Sciences), Tianyue Luo (Institute of Software, Chinese Academy of Sciences), Dinghao Liu (Shandong University), Haotian Zhang (Institute of Software, Chinese Academy of Sciences), Jingzheng Wu (Institute of Software, The Chinese Academy of Sciences)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797071

**中文总结:** 提出 LTMiner，从大规模项目挖掘稀有代码模式并检测其违反，结合实例排序过滤与 LLM 审计抑制模式爆炸与误报；在 Linux 6.12.1 上发现 42 个未知缺陷，其中 27 个已获开发者确认。

**Abstract:** Using data mining to extract frequent code patterns for bug detection has proven effective. However, prior studies have overlooked the prevalence of infrequent (rare) patterns, even though violations of such patterns can also lead to bugs.

In this paper, we present LTMiner, which mines rare patterns from large-scale projects and detects potential bugs by checking for violations of these patterns. In practice, rare patterns far outnumber frequent ones and lack strong statistical support. Consequently, we face a pattern explosion, and many rare patterns and their violations are uninteresting. LTMiner addresses this by using instance-based ranking and filtering to prioritize violations of rare patterns. It further employs a large language model (LLM) as a domain expert to audit top-ranked violations; mined information supports in-context learning, and task decomposition and self-reflection mitigate possible hallucinations. This pipeline effectively curbs pattern explosion and false positives, uncovering previously unknown bugs in large-scale projects at an acceptable cost.

Applied to Linux 6.12.1, LTMiner identified 42 previously unknown bugs, 27 of which have been confirmed by developers. These results indicate that, although rare-pattern bugs are sparse, a considerable number remain and exhibit a non-negligible long tail. We believe that rare-pattern bugs constitute a promising blue ocean for bug detection.
