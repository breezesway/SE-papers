# FSE 2026 Research Track — Awarded Papers

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total: 10 papers

## Award breakdown

| Award | # Papers |
| --- | ---: |
| ACM SIGSOFT Distinguished Paper Award | 10 |

*Note: awards are taken from the FSE 2026 Research Papers Awards tab (ACM SIGSOFT Distinguished Paper Award).*

## Papers

## 1. A Grounded Theory of Debugging in Professional Software Engineering Practice

**Authors:** Haolin Li (University of California San Diego), Michael Coblenz (University of California, San Diego)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797077

**中文总结:** 基于扎根理论观察 7 名专业开发者与 5 名直播写码者在真实代码库中完成 17 项调试任务，提出专业调试是迭代更新系统心智模型的诊断过程，开发者在导航与执行策略、前向/后向追踪间切换，并辅以外部资源；为调试工具设计与软件工程教育提供人本视角理论。

**Abstract:** Debugging is a central yet complex activity in software engineering. Prior studies have documented debugging strategies and tool usage, but little theory explains how experienced developers reason about bugs in large, real-world codebases. We conducted a qualitative study using a grounded theory approach. We observed seven professional developers and five professional live-coding streamers working on 17 debugging tasks in their own codebases, capturing diverse contexts of debugging. We theorize debugging as a structured, iterative diagnostic process in which programmers update a mental model of the system to guide information gathering. Developers gather information by alternating between navigation and execution strategies, employing forward and backward tracing modes of reasoning and adapting these approaches according to codebase context, complexity, and familiarity. Developers also gather external resources to complement code-based evidence, with their experience enabling them to systematically construct a mental model. We contribute a grounded theory of professional debugging that surfaces the human-centered dimensions of the practice, with implications for tool design and software engineering education.

## 2. An Empirical Study of Fuzz Harness Degradation

**Authors:** Philipp Görz (Ruhr-University Bochum), Joschua Schilling (CISPA Helmholtz Center for Information Security), Nicolai Bissantz (Ruhr-University Bochum), Thorsten Holz (Max Planck Institute for Security and Privacy)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808172

**中文总结:** 对 OSS-Fuzz 中 510 个 C/C++ 项目的 fuzz harness 开展实证研究，发现整体覆盖与找 bug 能力衰减有限且在可持续构建时仍具持久性，同时系统归类退化根因；并为 OSS-Fuzz/Fuzz Introspector 增加自动检测 harness 退化的新指标。

**Abstract:** Fuzzing is a widely used technique to automatically test software for potential faults. To fuzz software projects efficiently and effectively, they must use fuzz harnesses , i.e., small programs that connect the fuzzer to the project’s code under test. However, as projects evolve, it is unclear whether fuzz harnesses are maintained in lockstep or left to stagnate, and whether unmaintained fuzz harnesses gradually degrade in terms of code coverage and bug-finding effectiveness.

In this paper, we focus on OSS-Fuzz, the largest continuous fuzzing platform in practice, which provides harnesses for 510 open-source C/C++ projects, many of them security-critical. These harnesses are usually contributed by project maintainers or external developers, yet their ongoing maintenance is not always ensured. Our analysis shows that, overall, harnesses exhibit only a small reduction in coverage and retain surprising longevity in their ability to uncover bugs. This holds even without explicit updates, as long as they continue to build.  At the same time, we identify specific cases where harnesses degrade, analyze their root causes, and categorize them systematically. Finally, we extend OSS-Fuzz and Fuzz Introspector, a companion project to investigate fuzzer performance, with new metrics to automatically detect harness degradation, enabling more effective monitoring of fuzzing quality in evolving projects.

## 3. Building Software by Rolling the Dice: A Qualitative Study of Vibe Coding

**Authors:** Yi-Hung Chou (University of California, Irvine), Boyuan Jiang (University of California, Irvine), Yiwen Chen (Independent), Mingyue Weng (Marketing Creative Associate), Victoria Jackson (University of Southampton), Thomas Zimmermann (University of California, Irvine), James Jones (University of California at Irvine)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797105

**中文总结:** 对 20 个 vibe coding 视频（含约 16 小时直播会话、254 条提示）开展扎根理论研究，刻画从几乎不检查到审查改编 AI 代码的行为光谱，以及将调试/精炼视为「掷骰子」的随机性应对；指出不同心智模型影响提示策略、评估与信任，并为工具与教育提供启示。

**Abstract:** Large language models (LLMs) are reshaping software engineering by enabling vibe coding—building software primarily through prompts rather than writing code. Although widely publicized as a productivity breakthrough, little is known about how practitioners actually define and engage in these practices. To shed some light on this emerging phenomenon, we conducted a grounded theory study of 20 vibe-coding videos, including 7 live-streamed coding sessions (~16 hours, 254 prompts) and 13 opinion videos (~5 hours), supported by additional analysis of activity durations and intents of prompts. Our findings reveal a spectrum of behaviors: some vibe coders rely almost entirely on AI without inspecting code, while others examine and adapt generated outputs. Across approaches, all must contend with the stochastic nature of code generation, with debugging and refinement described as “rolling the dice.” Further, divergent mental models, shaped by developers’ expertise and engagement with AI, influence prompting strategies, evaluation practices, and levels of trust. These findings open new directions for research on the future of software engineering and point to practical opportunities for tool design and education.

## 4. Carbon-Taxed Transformers: A Green Compression Pipeline for Overgrown Language Models

**Authors:** Ajmain Inqiad Alam (University of Saskatchewan), Palash Ranjan Roy (University of Saskatchewan), Chanchal K. Roy (University of Saskatchewan), Banani Roy (University of Saskatchewan), Kevin Schneider (University of Saskatchewan)

**Categories:** Software Engineering for AI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797075

**中文总结:** 提出 Carbon-Taxed Transformers (CTT)，借鉴碳税思想对 SE 用语言模型做多架构压缩管线；在克隆检测、摘要与生成任务上最高可获约 49× 显存降低与 81% CO₂ 减排，同时保留约 98%/89%/最高 91%（文本）与 68%（pass@1）性能。

**Abstract:** The accelerating adoption of Large Language Models (LLMs) in software engineering (SE) has brought with it a silent crisis: unsustainable computational cost. While these models demonstrate remarkable capabilities in different SE tasks, they are unmanageably large, slow to deploy, memory-intensive, and carbon-heavy. This reality threatens not only the scalability and accessibility of AI-powered SE, but also its long-term environmental sustainability. The research challenge is clear: we must go beyond accuracy and address efficiency and environmental cost as first-class design constraints. To meet this challenge, we introduce Carbon-Taxed Transformers (CTT), a systematic multi-architectural compression principled pipeline ordering inspired by economic carbon taxation principles. Drawing from the economic concept of carbon pricing, CTT operationalizes a computational carbon tax that penalizes architectural inefficiencies and rewards deployment-ready compression. We evaluate CTT across three core SE tasks: code clone detection, code summarization, and code generation, with models spanning encoder-only, encoder-decoder, and decoder-only architecture. Our results show that CTT delivers on inference: (1) up to 49$\times$ memory reduction, (2) time reduction up to 8-10$\times$ for clone detection, up to 3$\times$ for summarization, and 4–7$\times$ for generation, (3) up to 81% reduction in CO$_2$ emissions and (4) CTT retains around 98% accuracy on clone detection, around 89% on summarization, and  up to 91% (textual metrics) and 68% (pass@1) for generation. Two ablation studies show that pipeline ordering and individual component contributions are both essential, providing empirical justification for CTT’s design and effectiveness. This work establishes a viable path toward responsible AI in SE through aggressive yet performance-preserving compression.

## 5. Clotho: Measuring Task-Specific Pre-Generation Test Adequacy for LLM Inputs

**Authors:** Juyeon Yoon (Korea Advanced Institute of Science and Technology), Somin Kim (Korea Advanced Institute of Science and Technology), Robert Feldt (Chalmers | University of Gothenburg), Shin Yoo (KAIST)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797114

**中文总结:** 提出 Clotho，利用隐藏状态与 GMM 在生成前估计任务相关输入难度并优先标注参考集；平均仅标注 5.4% 输入即可达 ROC-AUC 0.716，且开源模型学到的充分性可迁移到专有模型，使 top-100 暴露失败数提升约 126.8%。

**Abstract:** Software increasingly relies on the emergent capabilities of Large Language Models (LLMs), from natural language understanding to program analysis and generation. Yet testing them on specific tasks remains difficult and costly: many prompts lack ground truth, forcing reliance on human judgment, while existing uncertainty and adequacy measures typically require full inference. A key challenge is to assess input adequacy in a way that reflects the demands of the task, ideally before even generating any output. We introduce Clotho, a task-specific, pre-generation adequacy measure that estimates input difficulty directly from hidden LLM states. Given a large pool of unlabelled inputs for a specific task, Clotho uses a Gaussian Mixture Model (GMM) to adaptively sample the most informative cases for human labelling. Based on this reference set the GMM can then rank unseen inputs by their likelihood of failure. In our empirical evaluation across eight benchmark tasks and three open-weight LLMs, Clotho can predict failures with a ROC-AUC of 0.716, after labelling reference sets that are on average only 5.4% of inputs. It does so without generating any outputs, thereby reducing costs compared to existing uncertainty measures. Comparison of Clotho and post-generation uncertainty measures shows that the two approaches complement each other. Crucially, we show that adequacy scores learned from open-weight LLMs transfer effectively to proprietary models, extending the applicability of the approach. When prioritising test inputs for proprietary models, Clotho reveals 126.8% more failures, on average, in the top 100 inputs compared to random selection.

## 6. Empowering Autonomous Debugging Agents with Efficient Dynamic Analysis

**Authors:** Jiahong Xiang (Southern University of Science and Technology), Xiaoyang Xu (Southern University of Science and Technology), Xiaopan Chu (Southern University of Science and Technology), Hongliang Tian (Ant Group), Yuqun Zhang (Southern University of Science and Technology)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797126

**中文总结:** 提出 Agent-centric Debugging Interface（ADI），以函数级交互与 Frame Lifetime Trace 替代低效逐行调试，降低自主修复智能体成本；在 SWE-bench Verified 上使基础智能体以约 $1.28/任务解决 63.8% 任务，并可作为插件为 SOTA 智能体带来 6.2%–18.5% 提升。

**Abstract:** Autonomous agents for automated program repair represent a promising frontier in software engineering, yet their effectiveness is often hindered by reliance on post-mortem, coarse-grained execution feedback. While integrating traditional interactive debuggers seems a natural solution, their low-level, line-by-line interaction paradigm turns to be cost-inefficient for LLM-based agents, leading to exhausted budgets and unproductive loops. To mitigate this, we introduce Agent-centric Debugging Interface (ADI), a novel agent-centric debugging interface designed for cost-efficient, end-to-end autonomous interaction. Specifically, Agent-centric Debugging Interface realizes a function-level interaction paradigm, powered by our Frame Lifetime Trace—a comprehensive data structure encapsulating a function’s stateful execution trace—and a set of high-level navigational commands. Our extensive evaluation on the SWE-bench benchmark demonstrates the effectiveness and efficiency of ADI. By simply equipping a basic agent with ADI, it successfully resolves 63.8% of the tasks on the SWE-bench Verified set, even slightly outperforming the highly-optimized and high-investment Claude-Tools agent, at an average cost of $1.28 per task with Claude-Sonnet-3.7. Furthermore, we demonstrate ADI’s generality by integrating it as a plug-and-play component into the existing SOTA agents, delivering consistent gains ranging from 6.2% to 18.5% on the resolved tasks. These results indicate that Agent-centric Debugging Interface could achieve a general and efficient enhancement for the existing autonomous agents.

## 7. GraphLocator: Graph-guided Causal Reasoning for Issue Localization

**Authors:** Wei Liu (Peking University), Chao Peng (Tencent), Pengfei Gao (ByteDance), Aofan Liu (Peking University), Wei Zhang (Peking University), Haiyan Zhao (Peking University), Zhi Jin (Peking University, Wuhan University)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797079

**中文总结:** 提出 GraphLocator，通过因果结构发现与动态问题拆解构建因果问题图（CIG），缓解症状–根因与一对多实体错配；相对基线函数级召回/精度平均提升约 19.5%/11.9%，并将下游修复性能最高相对提升 28.74%。

**Abstract:** The issue localization task aims to identify the locations in a software repository that requires modification given a natural language issue description. This task is fundamental yet challenging in automated software engineering due to the semantic gap between issue description and source code implementation. This gap manifests as two mismatches: (1) \emph{symptom–to-cause mismatches}, where descriptions do not explicitly reveal underlying root causes; (2) \emph{one-to-many mismatches}, where a single issue corresponds to multiple interdependent code entities. To address these two mismatches, we propose \emph{GraphLocator}, an LLM-based approach that mitigates symptom–to-cause mismatches through \emph{causal structure discovering} and resolves one-to-many mismatches via \emph{dynamic issue disentangling}. The key artifact of \emph{GraphLocator} is the \emph{causal issue graph} (CIG), in which vertices represent discovered sub-issues along with their associated code entities, and edges encode the causal dependencies between them. The workflow of \emph{GraphLocator} consists of two phases: \emph{symptom vertices locating} and \emph{dynamic CIG discovering}; it first identifies symptom locations on the repository graph, then dynamically expands the CIG by iteratively reasoning over neighboring vertices, discovering new sub-issues and updating causal dependencies. Experiments on three real-world Python and Java datasets demonstrates the effectiveness of \emph{GraphLocator}: (1) Compared with baselines, \emph{GraphLocator} achieves more accurate localization with average improvements of +19.49% in function-level recall and +11.89% in precision with acceptable overhead. (2) \emph{GraphLocator} outperforms baselines on both symptom-to-cause and one-to-many mismatch scenarios, achieving recall improvement of +16.44% and +19.18%, precision improvement of +7.78% and +13.23%, respectively. (3) The disentangled causal structure CIG generated by \emph{GraphLocator} yields the highest relative improvement, resulting in a 28.74% increase in performance on the downstream issue-resolving task.

## 8. One Size Does Fit All: Exploring Model Fusion for Software Engineering Tasks

**Authors:** Yinggang Qiu (National University of Defense Technology), Yihao Qin, Mingyang Geng (National University of Defense Technology), Shangwen Wang (National University of Defense Technology), Dezun Dong (NUDT)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808198

**中文总结:** 系统评估软件工程场景下的模型融合，并提出 Scaling-Masks 改进 TALL-Masks，通过放大弱特征避免其在参数融合中被强特征淹没；同任务融合相近编程语言通常有效，跨任务/跨语言融合易退化，Scaling-Masks 在漏洞检测等场景显著提升融合性能。

**Abstract:** Large language models (LLMs) have achieved remarkable performance in software engineering (SE), and fine-tuning LLM for specific SE tasks has gradually become a new paradigm. However, storing fine-tuned checkpoints for multiple tasks incurs heavy storage and deployment complexity. Model fusion, which operates on fine-tuned parameters, offers excellent parameter compression and scalability, yet its effectiveness in the SE domain remains underexplored, making such an investigation essential for guiding the development of customized fusion techniques for the SE domain. To bridge this gap, we conduct a systematic study of model fusion in the SE contexts and reveal the following major findings: (1) when fusing programming languages (PLs) within the same task, model fusion usually works well and can enhance the performance of PLs with fewer data when PLs share similar features. (2) when fusing SE tasks of the same category within a same PL, all methods except TALL-Masks generally suffer substantial performance degradation on specific tasks; (3) when fusing SE tasks of different categories across different PLs, all existing model fusion methods exhibit significant performance degradation on certain tasks. In our evaluation results, TALL-Masks, which introduces a mask for each task to extract the most relevant dimensions from the fusion parameters, achieves promising performance. However, during parameters fusion, weak features (i.e., small variation in fine-tuned parameters) are easily overshadowed by strong ones (i.e., large variation in fine-tuned parameters) during parameter fusion, causing the constructed masks to fail to extract the most relevant parameters. To overcome this situation, we propose an improved version of TALL-Masks, called Scaling-Masks. The key idea is to amplify weak features to prevent them from being overshadowed by strong ones, which is achieved by scaling the value range of weak features to match that of strong features. Experimental results demonstrate that Scaling-Masks can significantly improve fusion performance for tasks with extremely weak features without affecting other tasks, with normalized accuracy improved by 63.49% for vulnerability detection when fusing SE tasks of different categories and 24.02% for PHP when fusing PLs in the code repair task.

## 9. Pig: Leveraging Large Language Models for Python Library Migrations

**Authors:** Miryeong Kang (Korea University), Wonseok Oh (Korea University), Gabin An (Korea University), Hakjoo Oh (Korea University)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797072

**中文总结:** 提出 Pig，以 API 级切片、失败模式引导提示、选择性提取与回植四步流水线用 LLM 自动化 Python 库迁移；在 364 个 API 迁移任务上将基线平均成功率提升 53.5%。

**Abstract:** We present Pig, a novel approach to automating Python library migration by leveraging large language models (LLMs). Library migration is an increasingly common task in modern Python development, yet it remains tedious and error-prone due to the lack of general solutions that can handle diverse libraries without relying on documentation or code examples. To address this challenge, Pig employs a four-step pipeline that effectively harnesses the capabilities of LLMs. First, Pig decomposes the migration task into smaller units by performing API-level slicing, allowing the LLM to focus on minimal, relevant context. Second, it guides LLMs using prompts informed by common failure patterns in naive LLM-based migrations and plausible API candidates. Third, Pig selectively extracts the migration-related code fragments from the LLM outputs. Finally, it transplants the migrated code back into the original program with post-processing to ensure semantic correctness and consistency. We demonstrate the effectiveness of Pig by evaluating it on 364 API-level migration tasks, where it improves the average success rate of the baseline approach by 53.5% across seven different LLM models.

## 10. Understanding Binary Code Similarity for Real-World Vulnerability Detection: A Large-Scale Empirical Study

**Authors:** Jingdong Guo (Institute of Information Engineering, CAS; School of Cyber Security, UCAS), Chaopeng Dong (School of Cyberspace, Hangzhou Dianzi University), Yimo Ren (Institute of Information Engineering Chinese Academy of Sciences & University of Chinese Academy of Sciences, China), Siyuan Li (University of Chinese Academy of Sciences & Institute of Information Engineering Chinese Academy of Sciences, China), Jie Liu (Institute of Software, Chinese Academy of Sciences), Hong Li (Institute of Information Engineering at Chinese Academy of Sciences), Hongsong Zhu (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797125

**中文总结:** 在 200 家厂商约 6 万固件镜像上大规模评估 BCSD 用于真实漏洞检测，分析脆弱函数版本、搜索空间、函数规模与工具链等因素的影响；提出构建感知查询与 TPL 感知两阶段搜索，将 MRR 提升至 0.981 并再提高约 18.5%。

**Abstract:** Firmware lies at the heart of IoT devices. Its development depends heavily on third-party libraries (TPLs), which greatly accelerate the process but simultaneously introduce associated vulnerabilities. Binary Code Similarity Detection (BCSD) is an effective technique for identifying vulnerabilities in firmware by comparing pairs of code segments. However, existing studies either evaluate their performance only on small-scale datasets or lack diversity in terms of vulnerabilities, TPLs, and firmware. Consequently, a comprehensive understanding of BCSD for real-world vulnerability detection remains absent. To bridge this gap, we conduct a large-scale study of vulnerability detection across 60,000 firmware images from 200 vendors using BCSD. Rather than introducing a novel model, we examine the influence of four key factors—vulnerable function versions, vulnerability search space, function sizes, and compilation toolchains on BCSD performance. Our results reveal that these factors substantially affect performance, often by wide margins. To address this, we propose a build-aware query strategy that derives queries from representative real-world binaries, effectively closing the gap and raising the mean reciprocal rank (MRR) from 0.818 to 0.981. Furthermore, we demonstrate that a TPL-aware, two-stage search process significantly enhances accuracy, improving MRR by 18.5% by limiting the search space.
