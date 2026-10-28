# ASE 2026 Research Track — Mining Software Repositories

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 6

## 1. ATLAS: Agentic Taxonomy of LArge-Scale Software Ecosystems

**Authors:** Junyi Lu (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Mengyao Lyu (Nanyang Technological University, Singapore), Jiahui Wu (Nanyang Technological University, Singapore), Lei Yu (Institute of Software at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Chengwei Liu (Nankai University, China), Fengjun Zhang (Institute of Software at Chinese Academy of Sciences, China), Li Yang (Institute of Software at Chinese Academy of Sciences, China), Chun Zuo (Sinosoft, China), Yang Liu (Nanyang Technological University, Singapore)

**Categories:** Mining Software Repositories

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834361

**中文总结:** 提出 agent 框架 ATLAS，结合 LLM 全局知识与真实仓库分布迭代构建 GitHub 软件层次 taxonomy 并端到端分类；在 2001 仓库基准上 TQF 83.13%，软件替代品发现 P@1 85.71%，优于人工 curated 列表与多种基线。

**Abstract:** The open-source ecosystem on GitHub lacks a systematic hierarchical taxonomy of software repositories. GitHub Topics, the dominant organizational mechanism, is flat, inconsistent, and covers only 67% of repositories. We present ATLAS, the first framework that automatically constructs a hierarchical taxonomy for software repositories and classifies repositories into it end-to-end. By combining LLM global knowledge with real repository distributions, ATLAS proposes meaningful splitting dimensions and iteratively corrects those that fail to accommodate real repositories. A Designer Agent proposes splitting dimensions while a Classifier Agent assigns repositories; a self-corrective refinement loop uses classification failures to drive dimension revision through escalating strategies. We evaluate ATLAS on 54,387 GitHub repositories against six baselines spanning four paradigm families, two downstream software engineering tasks, and three model families. On a stratified 2,001-repository benchmark, ATLAS achieves a Taxonomy Quality F-score (TQF) of 83.13%, outperforming the best baseline by 15 percentage points (on the full 54k corpus the approximate TQF is 73.0%, a gap driven by Path Granularity's all-or-nothing scoring on longer paths rather than lower classification accuracy; see Section 4.5). It is the only method to simultaneously achieve high structural quality and high practical applicability. On downstream tasks, the ATLAS taxonomy enables software alternative discovery with P@1 = 85.71%, surpassing even human-curated lists (62.34%), and achieves the highest P@1 for repository retrieval. The taxonomy further reveals structural ecosystem trends that are difficult to obtain from flat tags or similarity methods: the shift from libraries to AI/ML applications (now 61% of newly community-adopted projects) becomes visible only through hierarchical, type-based categorization. An interactive taxonomy explorer is available at https://atlas-taxonomy.netlify.app/.


## 2. AutoSQL: Extracting SQL Templates from Imperative ORM Code in Large-Scale Repositories

**Authors:** Junsong Pu (Sun Yat-sen University, Zhuhai, China), Yichen Li (Chinese University of Hong Kong, Hong Kong), Zhuangbin Chen (Sun Yat-sen University, Zhuhai, China), Zhihan Jiang (Chinese University of Hong Kong, Hong Kong), Zibin Zheng (Sun Yat-sen University, Zhuhai, China)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837420

**中文总结:** 针对 Go ORM 命令式拼 SQL，构建 Code Index 图并配合 Hybrid Context Retrieval 的 LLM agent 合成 SQL 模板（AutoSQL）；在五大仓库 579 入口点上 recall 68%–72%，较静态可达性与既有方法提升约 9–22 个百分点。

**Abstract:** Suboptimal SQL queries can significantly degrade the performance of cloud systems, motivating the extraction and auditing of SQL statements before deployment. However, Go ORM frameworks construct SQL imperatively through scattered method-call sequences, making it difficult to statically recover the resulting SQL templates. We present AutoSQL, a system that reconstructs SQL templates from Go ORM code. AutoSQL constructs a Code Index, a directed graph that captures structural dependencies between functions, types, and global variables as navigable edges. It then traces upstream call chains from ORM invocation sites to identify database-interacting functions as entry points. For each entry point, an LLM agent traverses the Code Index to collect code slices that influence SQL generation, switching to pattern-based search when the graph cannot resolve a retrieval goal. We call this strategy Hybrid Context Retrieval. Once sufficient context is collected, the agent synthesizes SQL templates. Evaluation on a benchmark of 579 test-covered entry points and 1,186 runtime-traced SQL statements from five large-scale Go repositories shows that AutoSQL achieves 68.04% to 72.18% recall, exceeding the static reachability baseline by 11.80% to 15.94% and outperforming existing methods by 8.52% to 21.50%.


## 3. Characterizing the Landscape of Open-Source Satellite Software

**Authors:** Jinfeng Wen (Beijing University of Posts and Telecommunications, China), Qi Liang (Beijing University of Posts and Telecommunications, China), Yuehan Sun (Beijing University of Posts and Telecommunications, China), Federica Sarro (University College London, UK), Ao Zhou (Beijing University of Posts and Telecommunications, China), Xuanzhe Liu (Peking University, China), Shangguang Wang (Beijing University of Posts and Telecommunications, China)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834343

**中文总结:** 首次对开源卫星软件进行大规模实证刻画，挖掘并分析 GitHub 上 22,286 个相关项目。研究揭示其 popularity 上升、43 类软件目标分类体系，以及 66 种语言构成的异构生态与开发实践特征。

**Abstract:** Satellites have become fundamental components of modern technological systems, supporting critical infrastructure in communication, navigation, Earth observation, and scientific research. As space exploration advances and demand for satellite-enabled services grows, reliance on complex, heterogeneous satellite software continues to increase. A systematic understanding of the satellite software landscape is therefore increasingly important, yet existing studies still lack a comprehensive empirical examination. To address this gap, we present the first characterization study of open-source satellite software, examining its ecosystem and development practices. We mine and analyze 22,286 satellite-related GitHub projects through three research questions on popularity trends (RQ1), software goals (RQ2), and development practices (RQ3). First, we characterize the temporal evolution of projects and active developers, revealing increasing popularity. Second, through manual inspection of 646 projects, we construct a taxonomy of 43 software-goal categories spanning conceptual design, datasets, system implementation, simulation, testing, and tools. Third, we conduct an in-depth analysis of projects with source code, revealing a highly heterogeneous and task-specialized ecosystem with 66 programming languages and diverse implementation strategies. Finally, we summarize key findings and derive actionable implications for satellite developers and researchers.


## 4. Implicit, Yet Impactful: Understanding Hidden Dependencies in Java Projects

**Authors:** Lyuye Zhang (Nankai University, China / Nanyang Technological University, Singapore), Chengwei Liu (Nankai University, China), Fangyuan Zhang (Nankai University, China / Nanyang Technological University, Singapore), Yiran Zhang (Nanyang Technological University, Singapore), Yuan Zhou (Zhejiang Sci-Tech University, China), Yang Liu (Nanyang Technological University, Singapore)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837552

**中文总结:** 首次以 Maven 隐式依赖（代码使用但未声明）为焦点，分析 1157 库与 972 GitHub 模块；34.12% 存在隐式依赖，48% 因版本漂移引入破坏性变更，36 个 CVE 相关方法被根项目直接调用，并归纳四类对策。

**Abstract:** As software usage continues to expand, package managers automatically resolve dependencies to construct a dependency graph based on user-specified requirements. These explicitly declared dependencies, known as direct dependencies, receive significant attention in terms of maintainability and security. However, implicit dependencies, which are not explicitly defined by users but are still directly utilized or referenced in their project code due to oversight, remain largely unnoticed. Unlike ordinary transitive dependencies, which may remain unused and invisible to the root, implicit dependencies are actively used yet undeclared, leaving their versions outside the project’s direct control. This lack of awareness poses substantial challenges related to security and maintainability. In this study, we present the first study to treat implicit dependencies as the focal phenomenon and quantitatively characterize their lifecycle consequences for the Maven ecosystem. We meticulously collected and built a large-scale dataset with 1,157 libraries with 19,812 versions from the Maven Central Repository and 972 modules from GitHub. Our findings reveal that 34.12% of the analyzed dataset contains implicit dependencies, with two primary causes identified as key contributors to the issue. Among these, 48% introduce breaking changes due to version drift, and 36 CVEs have vulnerable methods directly used by root projects; 30.28% of implicit dependencies are affected by known vulnerabilities under the version-range convention SCA tools use for declared dependencies. Finally, we identified and analyzed four major countermeasures, providing actionable insights and practical implications for addressing this overlooked issue for stakeholders within the OSS ecosystem.


## 5. Recovering Revisions of Pull Requests with Altered History

**Authors:** Gengyi Sun (University of Waterloo, Canada), Georges Aaron Randrianaina (University of Waterloo, Canada), Tao Xiao (Kyushu University, Japan), Yasutaka Kamei (Kyushu University, Japan), Shane McIntosh (University of Waterloo, Canada)

**Categories:** Mining Software Repositories

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837417

**中文总结:** 基于 93 万+ GitHub PR 实证发现 force-push 常把 PR 变更与基线分支更新混在同一 diff 中；提出 AntiDiffamine，通过对齐共同祖先隔离 PR 专属变更，可自动解混 98.1% 修订并将 diff 缩小 1–3 个数量级，并提供 GitHub Action 模板便于落地。

**Abstract:** In pull-based development, Pull Requests (PRs) undergo peer review. To address review feedback, authors may "force-push" after amending, squashing, or rebasing commits. Such revisions can conflate PR-specific changes with updates on the base branch, hindering further review and introducing noise into PR-based datasets. In this paper, we empirically study 935,011 PRs from 1,445 well-maintained GitHub projects. We observe 568,218 force-push events in 242,624 PRs that span 1,366 projects. We denote the HEAD commits of the PR before and after force-pushing as a force-push pair, and observe that 210,837 pairs (37.1%) have a relationship that conflates PR changes with updates to the base branch. To systematically isolate PR-specific changes in such revisions, we propose AntiDiffamine---an ancestry-based approach that aligns commits on a common reference. AntiDiffamine can automatically deconflate 98.1% of the studied revisions, decreasing the diff size by one to three orders of magnitude. We also evaluate AntiDiffamine on fail-fix pairs, i.e., revisions that fix failing builds. A case study of Kubernetes reveals that 130 of 523 pairs have conflated diffs. Moreover, the fixing files identified when AntiDiffamine is applied overlap more with a human-labelled ground truth than when conflation is untreated or excluded. AntiDiffamine is a first attempt at addressing force-push-based diff conflation, which is having a real-world impact on practical and research workflows. To ease practical adoption, we provide a template GitHub Action, which scans PR updates for force-push events and applies AntiDiffamine to deconflate the diff.


## 6. SustainSR: Interpretable OSS Sustainability Prediction via Symbolic Regression

**Authors:** Yang Deng (Wuhan University, China / Duke Kunshan University, China), Mustafa Misir (Duke Kunshan University, China), Jinfu Chen (Wuhan University, China), Jifeng Xuan (Wuhan University, China)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834366

**中文总结:** 提出 SustainSR，用遗传编程学习显式可持续性的符号表达式并 Taylor 展开量化特征重要性与交互；在 Apache/GitHub 项目上 AUC 较最佳基线 +1%–4%、F1 +3%–7%，提供可行动风险洞察。

**Abstract:** Open-source software (OSS) has become a foundational component of modern software ecosystems. Early prediction of OSS sustainability is crucial for identifying potential risks and supporting timely intervention.Existing approaches formulate OSS sustainability prediction task as a binary classification problem using Deep Learning (DL) models.However, their black-box nature obscures the decision process and undermines the credibility of the predictions.To address this limitation, we propose SustainSR, an interpretable symbolic regression–based method for OSS sustainability prediction.SustainSR reformulates prediction task as a function-learning problem and uses Genetic Programming (GP) algorithm to learn explicit sustainability expressions.We further apply Taylor expansion to quantify feature importance and pairwise interactions.The quantified results facilitate early risk identification and actionable intervention guidance.We evaluate SustainSR on Apache and GitHub projects from three dimensions: fitting performance, predictive performance, and interpretability.Results show that SustainSR significantly outperforms most baselines, it improves AUC by 1%-4% and F 1 avg by 3%-7% over the best-performing baseline.Case studies further demonstrate that SustainSR offers actionable sustainability insights to support risk identification, project selection, and community governance.Overall, SustainSR provides an effective and interpretable solution for OSS sustainability analysis, bridging the gap between predictive performance and interpretability.

