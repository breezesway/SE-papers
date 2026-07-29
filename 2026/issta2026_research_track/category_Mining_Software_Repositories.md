# ISSTA 2026 Research Track — Mining Software Repositories

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 5

## 1. Deprecated but Not Abandoned: A Large-Scale Empirical Study on Growing-user-demand Deprecated NPM Packages

**Authors:** Zezhou Tang (National University of Defense Technology), Yang Zhang (National University of Defense Technology, China), Xinjun Mao (National University of Defense Technology), Tanghaoran Zhang (National University of Defense Technology), Changrong Xie (National University of Defense Technology), Wenyu Xu (National University of Defense Technology), Simeng Yao (National University of Defense Technology), Yiwen Wu (National University of Defense Technology)

**Categories:** Mining Software Repositories

**中文总结:** 本文识别 825 个已弃用但下载量持续增长的 NPM 包（GDNP），结合维护者与用户调查分析其社区参与度下降与依赖树复杂性导致的持续使用原因。GDNP 每月带来超 1.26 亿次高危漏洞暴露，社区讨论却极少关注安全问题。

**Abstract:** Package deprecation in ecosystems like NPM signals the termination of maintenance, and continued use of such packages poses potential sustainability and security risks to dependent projects. We observe a counter-intuitive phenomenon from widely-used deprecated packages whose user demand continues to grow after deprecation; we define these as Growing-user-demand Deprecated NPM Packages (GDNPs). Despite this clear contradiction between deprecation and growing user demand, the community engagement, reasons, and challenges of GDNPs have not been systematically examined. To bridge this gap, we conduct a mixed‑method empirical study that identifies and analyzes 825 GDNPs from 4,011 widely‑used deprecated packages, alongside surveys of 76 maintainers and 67 users. We find that GDNPs grow on average by 82,811 download counts per month after deprecation, yet repository‑level community engagement declines significantly, revealing an expanding maintenance gap. Quantitatively, GDNPs contribute to over 126 million monthly exposures to high-severity vulnerabilities. Surveys indicate that continued reliance stems primarily from the complexity of the dependency tree and user inertia, leading to reactive maintenance and the accumulation of technical debt. Furthermore, topic modeling of post-deprecation discussions of GDNP repositories shows that community discussions heavily prioritize functional errors while seldom discussing security vulnerabilities, highlighting a misalignment between perceived and actual risk.  Based on the results, we provide actionable implications that can facilitate future research and assist stakeholders in improving the maintenance of GDNP.


## 2. Hidden Licensing Risks in the PTMware Ecosystem

**Authors:** Bo Wang (Beijing Jiaotong University), Yueyang Chen (Beijing Jiaotong University), Jieke Shi (Singapore Management University), Minghui Li (Beijing Jiaotong University), Yunbo Lyu (Singapore Management University), Yinan Wu (North Carolina State University), Youfang Lin (Beijing Jiaotong University), Zhou Yang (University of Alberta; CIFAR AI Chair; Alberta Machine Intelligence Institute)

**Categories:** Mining Software Repositories

**中文总结:** 构建 GitHub+Hugging Face 上 12000+ LLMware 供应链数据集并分析许可证实践；提出 LiAgent 做生态级 license 兼容性分析，F1 达 87%，已提交 60 个 incompatibility issue。

**Abstract:** Large Language Models (LLMs) have been increasingly integrated into software systems, giving rise to a new class of software referred to as LLMware. In addition to traditional software components composed solely of source code, LLMware also embeds or interacts with LLMs that depend on other models and datasets, forming complex supply chains involving open-source software (OSS) libraries, LLMs, and datasets. However, the licensing issues arising from these intertwined dependencies remain largely unexplored.

Leveraging GitHub and Hugging Face, two premier hubs for code and models, we curate a large- scale dataset capturing the supply chains of LLMware. Our dataset comprises 12,180 OSS repositories from GitHub, 3,988 LLMs, and 708 datasets from Hugging Face. We analyze license distributions in the LLMware ecosystem and find that licensing practices differ markedly from those in traditional OSS communities. We further examine license-related issues and identify license selection and maintenance as the primary pain points, with 84% of cases involving discussions about adding appropriate licenses or resolving conflicts in existing ones. We then study license incompatibility in LLMware and evaluate the state-of-the-art approaches, finding that they perform poorly in this setting and achieve only 58% and 76% F1 scores, respectively. These results motivate us to propose LiAgent, which explores the potential of LLM-based agents for ecosystem-level license compatibility analysis, achieves an F1 score of 87%, and improves performance by 14 percentage points over prior approaches. We submit 60 license incompatibility issues detected by LiAgent, of which 11 have been confirmed by developers. Two LLMs with license conflicts have more than 107 million and 5 million downloads on Hugging Face, respectively, suggesting the issues may impact a large number of downstream applications. We conclude by discussing implications and providing recommendations to support the healthy growth of the LLMware ecosystem.


## 3. Mind the Gap: An Empirical Study of Synchronization Gaps, Delays, and Missed Opportunities in Software Forks

**Authors:** Jiaying Zhu (Nanyang Technological University), Lyuye Zhang (Nanyang Technological University), Wu Jiahui (Nanyang Technological University, Singapore), CHENGYUE LIU, Yang Liu (Nanyang Technological University)

**Categories:** Mining Software Repositories

**中文总结:** 大规模实证研究 3820 个活跃 fork 的同步行为，揭示仅 6.92% fork 本地提交进入 PR 的同步悖论，并构建三阶段 syncability 评估流水线。在 50 万 fork 本地提交中筛出 12284 个可同步对，人工确认 83 个潜在 1-day 漏洞。

**Abstract:** Fork-based development enables parallel evolution of software, but unsynchronized contributions create persistent divergence: security patches, bug fixes, and quality improvements often fail to propagate across fork families, leaving downstream users exposed to known vulnerabilities or bugs and missing massive opportunities to improve the other repositories in the family. We present the first large-scale empirical study of fork synchronization, analyzing popular GitHub fork families with 3,820 actively maintained forks, and developed a monitoring platform to mine the valuable commits and promote their swift merging.

Our findings reveal a synchronization paradox: while 90% of submitted pull requests are merged, only 6.92% of fork commits ever appear in PRs, leaving massive fork development permanently unsynchronized across the families. Synchronization delay is pervasive and structurally uneven where fork propagation accounts for 72.9% of end-to-end commit lifecycle delay. Contrary to common assumptions, PR rejection is rarely caused by technical incorrectness; instead, 65% of rejections stem from superseded contributions, process violations, or maintainer policy decisions.

Based on these insights, we develop a three-stage syncability assessment pipeline that identifies fork-local commits that are both sync-worthy (broadly beneficial) and sync-eligible (technically and policy-compatibly portable). Applied to 0.5 million fork-local commits, our pipeline surfaces 12,284 sync-ready commit–repository pairs, demonstrating that our approach identifies practically valuable changes. To further validate the security impact, we manually reviewed 153 security-related commit–repository pairs and confirmed 83 as potential 1-day vulnerabilities, for which we produced 35 proof-of-concept demonstrations and filed issues to the affected repositories. Our monitoring platform enables continuous, near-real-time detection of synchronization opportunities across fork families, improving the sustainability of fork-based open-source ecosystems.


## 4. Paired Code Smells and Test Smells: A Fine-Grained Longitudinal Empirical Study

**Authors:** Ziwen Cai (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen))

**Categories:** Mining Software Repositories

**中文总结:** 对 19 个 Java 仓库 128417 次提交做细粒度纵向研究，分析生产代码 smell 与测试 smell 的配对共演化、生存期与移除动机。发现 30 条显著关联规则且配对 smell 寿命通常更短，常触发风险驱动重构。

**Abstract:** As software systems grow in complexity, ensuring maintainability is essential, but often hindered by various quality issues. Among them, code smells and test smells are widely recognized indicators of technical debt that degrade system quality. While production code and test suites are intrinsically coupled and evolve together, existing research predominantly studies code smells and test smells in isolation, ignoring their underlying connection over time.

To bridge this gap, this paper presents a fine-grained longitudinal study on the co-evolutionary dynamics of “paired smells”, which refer to cases where code and test smells exist concurrently in linked production and test code. By analyzing 128,417 commits across 19 long-lived open-source Java repositories, we investigate the statistical associations, survival lifespans, and removal motivations of these paired flaws. As a result, we identify 30 statistically significant rules where specific test smells imply the presence of underlying production code smells and our survival analysis reveals that in most of repositories, paired smells have relatively shorter lifespans than unpaired ones. To explain this phenomenon, our manual inspection reveals that paired smells often signal deeper structural issues, prompting explicit risk-driven refactoring. Finally, we discuss the implications of these results for code quality analysis and continuous integration tools, suggesting that they should link related smell findings between production and test code and guide synchronized refactoring.


## 5. Towards Understanding the Bugs in Verilator, a Hardware Description Language Compiler

**Authors:** Songyan Jiang (State Key Laboratory for Novel Software Technology, Nanjing University), Maolin Sun (Nanjing University), Kang Chen (State Key Laboratory for Novel Software Technology, Nanjing University), Qingyang Li (Nanjing University), Yibiao Yang (Nanjing University), Yuming Zhou (Nanjing University)

**Categories:** Mining Software Repositories

**中文总结:** 对 Verilator HDL 编译器 488 个已确认 bug 进行首个系统实证研究，分析症状、根因与触发用例特征并评估现有测试技术有效性。为 HDL 编译器可靠性改进与针对性自动化测试方法设计提供可操作建议。

**Abstract:** Verilator is the premier open-source Hardware Description Language (HDL) compiler. It transforms Verilog and SystemVerilog designs into optimized C++ or SystemC models, enabling high-speed, cycle-accurate simulation prior to large-scale production. As a cornerstone of the hardware verification ecosystem, the correctness of Verilator is paramount; compiler faults can lead to silent simulation errors or unexpected failures, undermining the integrity of the hardware development lifecycle. Unlike traditional software compilers, HDL compilers manage unique concurrency and synthesis semantics, potentially introducing distinct bug patterns and complexities. However, while prior research has explored testing techniques for HDL toolchains, there remains a lack of systematic empirical studies characterizing the specific nature of bugs in Verilator. This knowledge gap hinders the development of targeted improvements in compiler robustness and testing strategies. To address this, we present the first comprehensive empirical study of Verilator bugs. We manually collected, analyzed, and categorized a dataset of 488 confirmed bugs from the official repository over three years. Our study investigates bug symptoms, root causes, and the characteristics of triggering test cases, while also evaluating the effectiveness of existing testing techniques. Based on our findings, we provide actionable guidance for developers to enhance Verilator’s reliability and for researchers to design more effective automated testing methodologies for HDL compilers.

