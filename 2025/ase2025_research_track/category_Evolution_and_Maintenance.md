# ASE 2025 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 18

## 1. AdaptEval: A Benchmark for Evaluating Large Language Models on Code Snippet Adaptation

**Authors:** Tanghaoran Zhang (National University of Defense Technology), Xinjun Mao (National University of Defense Technology), Shangwen Wang (National University of Defense Technology), Yuxin Zhao (Key Laboratory of Software Engineering for Complex Systems, National University of Defense Technology), Yao Lu (National University of Defense Technology), Jin Zhang (Hunan Normal University), Zhang Zhang (Key Laboratory of Software Engineering for Complex Systems, National University of Defense Technology), Kang Yang (National University of Defense Technology), Yue Yu (PengCheng Lab)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334689

**中文总结:** 提出 AdaptEval 基准，从 Stack Overflow/GitHub 抽取真实代码适配任务，结合任务/适配双层标注与两级测试框架评估 LLM 代码片段适配能力，并开展首次实证研究。

**Abstract:** Recent advancements in large language models (LLMs) have automated various software engineering tasks, with benchmarks emerging to evaluate their capabilities. However, for adaptation, a critical activity during code reuse, there is no benchmark to assess LLMs’ performance, leaving their practical utility in this area unclear. To fill this gap, we propose AdaptEval, a benchmark designed to evaluate LLMs on code snippet adaptation. Unlike existing benchmarks, AdaptEval incorporates three distinctive features: First, \textbf{\textit{practical context}}. Tasks in AdaptEval are derived from developers’ practices, preserving rich contextual information from Stack Overflow and GitHub communities. Second, \textbf{\textit{multi-granularity annotation}}. Each task is annotated with requirements at both task and adaptation levels, supporting the evaluation of LLMs across diverse adaptation scenarios. Third, \textbf{\textit{fine-grained evaluation}}. AdaptEval includes a two-tier testing framework combining adaptation-level and function-level tests, which enables evaluating LLMs’ performance across various individual adaptations. Based on AdaptEval, we conduct the first empirical study to evaluate six instruction-tuned LLMs and especially three reasoning LLMs on code snippet adaptation. Experimental results demonstrate that AdaptEval enables the assessment of LLMs’ adaptation capabilities from various perspectives. It also provides critical insights into their current limitations, particularly their struggle to follow explicit instructions. We hope AdaptEval can facilitate further investigation and enhancement of LLMs’ capabilities in code snippet adaptation, supporting their applications in the real-world software reuse.


## 2. An Empirical Study of Python Library Migration Using Large Language Models

**Authors:** Mohayeminul Islam (University of Alberta), Ajay Jha (North Dakota State University), May Mahmoud (New York University Abu Dhabi), Ildar Akhmetov (Northeastern University), Sarah Nadi (New York University Abu Dhabi)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334199

**中文总结:** 在 PYMIGBENCH 321 次真实 Python 库迁移（含 2989 处代码变更）上评估 Llama 3.1、GPT-4o mini 与 GPT-4o，结合开发者迁移结果对比与单元测试衡量 LLM 库迁移正确性。

**Abstract:** Library migration is the process of replacing one library with another library that provides similar functionality. Manual library migration is time consuming and error prone, as it requires developers to understand the APIs of both libraries, map them, and perform the necessary code transformations. Due to its difficulty, most of the existing automated techniques and tooling stop at the API mapping stage or support a limited set of code transformations. On the other hand, Large Language Models (LLMs) are good at generating and transforming code and finding similar code, which are necessary upstream tasks for library migration. Such capabilities suggest that LLMs may be suitable for library migration. Accordingly, this paper investigates the effectiveness of LLMs for migration between Python libraries. We evaluate three LLMs, LLama 3.1, GPT-4o mini, and GPT-4o on PYMIGBENCH, where we migrate 321 real-world library migrations that include 2,989 migration-related code changes. To measure correctness, we (1) compare the LLM’s migrated code with the developers’ migrated code in the benchmark and (2) run the unit tests available in the client repositories. We find that LLama 3.1, GPT-4o mini, and GPT-4o correctly migrate 89%, 89%, and 94% of the migration-related code changes, respectively. We also find that 36%, 52% and 64% of the LLama 3.1, GPT-4o mini, and GPT-4o migrations pass the same tests that passed in the developer’s migration. To ensure the LLMs are not reciting the migrations, we also evaluate them on 10 new repositories where the migration never happened. Overall, our results suggest that LLMs can be effective in migrating code between libraries, but we also identify some open challenges.


## 3. Automated Inline Comment Smell Detection and Repair with Large Language Models

**Authors:** Hatice Kübra Çağlar (Bilkent University), Semih Çağlar (Bilkent University), Eray Tüzün (Bilkent University)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334256

**中文总结:** 在 2211 条行内注释坏味道实例上评估 GPT-4o-mini、o3-mini、DeepSeek-V3、Codestral-2501 的检测与修复效果，覆盖完整注释坏味道分类并在零样本/少样本下各运行五次。

**Abstract:** Context: Code comments play a critical role in improving code readability, maintainability, and collaborative development. However, comments may deviate from best practices due to software evolution, where code changes are not reflected in comments, as well as practitioner-related issues such as vague descriptions, redundancy, or misaligned intent. These issues lead to various comment smells that degrade software quality. While prior studies have explored comment inconsistencies, most are limited in scope, either addressing a narrow subset of smells or focusing solely on detection without considering repair.

Objective: This study evaluates the effectiveness of large language models (LLMs) in both detecting and repairing inline code comment smells, using a comprehensive taxonomy of code comment smell types.

Method: We extended a prior data set by incorporating repaired versions of smelly comments, resulting in 2,211 unique instances. Four LLMs—GPT-4o-mini, o3-mini, DeepSeek-V3, and Codestral-2501—are evaluated under zero-shot and few-shot prompting strategies. To account for non-deterministic behavior in LLM outputs and ensure robustness, each configuration is executed five times. Detection performance is measured using accuracy, macro F1 score, and Matthews correlation coefficient (MCC); repair is evaluated using SBERT similarity, METEOR, and ROUGE-L. Our multi-stage pipeline feeds detection outputs into the repair phase, where the detection result with the highest macro F1 score is used to simulate the best possible repair scenario. Median scores across runs are reported for model comparison.

Results: o3-mini with few-shot prompting achieves the highest median detection performance: macro F1 of 0.41, MCC of 0.50, and accuracy of 0.72, exceeding the baseline of GPT-4. For repair, Codestral-2501 in the zero-shot setting yields the best results with a median SBERT score of 0.61, followed by DeepSeek-V3 and GPT-4o-mini at 0.53, and o3-mini at 0.46. Few-shot prompts improve detection, while zero-shot prompts are more effective for repair.

Conclusion: Lightweight LLMs such as o3-mini can achieve strong detection performance when guided by effective few-shot prompts. For example, o3-mini with few-shot prompting attains the highest median detection results: macro F1 of 0.41, MCC of 0.50, and accuracy of 0.72, surpassing the GPT-4 baseline. In contrast, repair tasks benefit more from zero-shot prompting, though they introduce challenges such as overfitting and the risk of generating new smells. Our findings support the development of practical tools, including a GitHub-integrated comment repair assistant, and motivate future work on dynamic prompt selection and multilingual benchmark construction.


## 4. BinStruct: Binary Structure Recovery Combining Static Analysis and Semantics

**Authors:** Yiran Zhang, Zhengzi Xu (Imperial Global Singapore), Zhe Lang (Institute of Information Engineering, CAS), CHENGYUE LIU, Yuqiang Sun (Nanyang Technological University), Wenbo Guo (Nanyang Technological University), Chengwei Liu (Nanyang Technological University), Weisong Sun (Nanyang Technological University), Yang Liu (Nanyang Technological University)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334428

**中文总结:** 提出 BinStruct，结合数据引用模式、函数调用与 LLM 语义理解恢复二进制文件结构，再以结构依赖与语义相似度共识聚类识别模块，支撑大规模逆向的高层结构理解。

**Abstract:** Binary reverse engineering is foundational to various tasks such as malware analysis and vulnerability detection. Traditional binary analysis tools mainly operate at the function level. However, modern software has grown significantly in size, with binaries often containing thousands of functions. Without understanding how these functions are organized into higher-level structures, it becomes difficult to effectively support downstream analysis tasks. Analysts must examine thousands of functions separately, making the process time-consuming and error-prone. Despite these challenges, current research on recovering the higher-level structure of binaries remains limited.

To bridge this gap, we propose BinStruct, a novel binary structure recovery framework that recovers both file and module structures from binaries. BinStruct first identifies the file structure by combining data reference patterns, function calls, and semantic understanding from Large Language Models. Then, inspired by software architecture recovery in source code analysis, BinStruct identifies modules by clustering the recovered files using consensus between structural dependency and semantic similarity. Evaluation on 121 real-world stripped binaries demonstrates that BinStruct outperforms state-of-the-art techniques in both file and module recovery accuracy, while requiring only 7.42s and 34.46s on average to recover file and module structures, respectively. Case studies on Libxml2 and PredatorTheStealer demonstrate BinStruct’s effectiveness on security tasks like attack surface analysis and malware investigation.


## 5. CoTune: Co-evolutionary Configuration Tuning

**Authors:** Gangda Xiong (University of Electronic Science and Technology of China), Tao Chen (University of Birmingham)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334616

**中文总结:** 提出 CoTune，通过协同演化目标性能需求与辅助需求来引导配置调优，当硬性 SLA 过严或误导时由辅助需求接管，避免单纯将其作为目标导致的收敛困难与资源浪费。

**Abstract:** To automatically tune configurations for the best possible system performance (e.g., runtime or throughput), much work has been focused on designing intelligent heuristics in a tuner. However, existing tuner designs have mostly ignored the presence of complex performance requirements (e.g., “the latency shall ideally be 2 seconds”), but simply assume that better performance is always more preferred. This would not only waste valuable information in a requirement but might also consume extensive resources to tune for a goal with little gain. Yet, prior studies have shown that simply incorporating the requirement as a tuning objective is problematic since the requirement might be too strict, harming convergence; or its highly diverse satisfactions might lead to premature convergence.

In this paper, we propose CoTune, a tool that takes the information of a given target performance requirement into account through co-evolution. CoTune is unique in the sense that it creates an auxiliary performance requirement to be co-evolved with the configurations, which assists the target performance requirement when it becomes ineffective or even misleading, hence allowing the tuning to be guided by the requirement while being robust to its harm. Experiment results on 162 cases (nine systems and 18 requirements) reveal that CoTune considerably outperforms existing tuners, ranking as the best for 90% cases (against the 3%–35% for other tuners) with up to 2.93x overall improvements, while doing so under a much better efficiency.


## 6. CROSS2OH: Enabling Seamless Porting of C/C++ Software Libraries to OpenHarmony

**Authors:** Qian Zhang (University of California at Riverside), Li Tsz On (The Hong Kong University of Science and Technology), Ying Wang (Northeastern University), Li Li (Beihang University), Shing-Chi Cheung (Hong Kong University of Science and Technology)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334403

**中文总结:** 针对 Linux 向 OpenHarmony 移植 C/C++ 库时的跨平台不兼容（CPI）问题，基于 92 个已成功移植库的实证分析与逐步复现归纳差异模式，提出 CROSS2OH 辅助开发者诊断并修复跨编译错误。

**Abstract:** OpenHarmony is a new mobile operating system that offers a popular alternative to Android and iOS. To support its adoption, significant efforts have been devoted to porting C/C++ libraries from Linux to OpenHarmony. However, this porting process presents unique challenges due to the fundamental architectural differences in system libraries, runtime environments, and build systems between the two platforms. These discrepancies manifest as Cross-platform Incompatibility (CPI) issues during cross-compilation, which are particularly difficult to resolve for two key reasons. First, conventional cross-compilation toolchains provide only brief error messages that offer inadequate diagnostic information for CPI issues. Second, resolving these issues requires a deep understanding of cross-platform discrepancies, yet comprehensive documentation or systematic guidelines about such Linux-to-OpenHarmony differences remain largely unavailable.

To assist developers in addressing these challenges, we conducted an empirical study on 92 C/C++ libraries successfully ported to OpenHarmony. Through manual step-by-step reproduction of all CPI issues, our study reveals that discrepancies between Linux and OpenHarmony can be divided into three categories, and CPI issues can manifest through eight dimensions. Furthermore, we identified eight common adaptation strategies for resolving CPI issues. Based on these findings, we present CROSS2OH, an automated technique for porting Linux-based software to OpenHarmony. Our approach combines: (1) an adaptation knowledge base (derived from RQ1 and RQ2 findings) and (2) a static analysis approach to detect and patch eight types of CPI issues.

Evaluation using real developer patches shows CROSS2OH achieves 0.94 recall and 0.91 precision in resolving CPI issues. Notably, CROSS2OH enables successful cross-compilation for 40 critical libraries (including dependencies for popular Android apps such as WeChat, Microsoft Excel, Bilibili), with 29 of them passed official OpenHarmony review. The evaluation results demonstrate CROSS2OH’s potential to streamline the porting process and foster the growth of the OpenHarmony software ecosystem.


## 7. Demystifying the Evolution of Neural Networks with BOM Analysis: Insights from a Large-Scale Study of 55,997 GitHub Repositories

**Authors:** xiaoning ren, Yuhang Ye (University of Science and Technology of China), Xiongfei Wu (University of Luxembourg), Yueming Wu (Huazhong University of Science and Technology), Yinxing Xue (Institute of AI for Industries, Chinese Academy of Sciences)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334220

**中文总结:** 提出面向神经网络软件的 NNBOM 数据集，从 55,997 个 PyTorch 仓库抽取 TPL、预训练模型与模块依赖，并大规模实证分析 NN 软件在规模、组件复用与跨域依赖上的演化规律。

**Abstract:** Neural networks have become integral to many fields due to their exceptional performance. The open-source community has witnessed a rapid influx of neural network (NN) repositories with fast-paced iterations, making it crucial for practitioners to analyze their evolution to guide development and stay ahead of trends. While extensive research has explored traditional software evolution using Software Bill of Materials (SBOMs), these are ill-suited for NN software, which relies on pre-defined modules and pre-trained models (PTMs) with distinct component structures and reuse patterns. Conceptual AI Bills of Materials (AIBOMs) also lack practical implementations for large-scale evolutionary analysis. To fill this gap, we introduce the Neural Network Bill of Material (NNBOM), a comprehensive dataset construct tailored for NN software. We create a large-scale NNBOM database from 55,997 curated PyTorch GitHub repositories, cataloging their TPLs, PTMs, and modules. Leveraging this database, we conduct a comprehensive empirical study of neural network software evolution across software scale, component reuse, and inter-domain dependency, providing maintainers and developers with a holistic view of its long-term trends. Building on these findings, we develop two prototype applications, \textit{Multi repository Evolution Analyzer} and \textit{Single repository Component Assessor and Recommender}, to demonstrate the practical value of our analysis.


## 8. Enhancing LLMs with Staged Grouping and Dehallucination for Header File Decomposition

**Authors:** Yue Wang (Peking University), Jiaxuan Sun (Peking University), Yanzhen Zou (Peking University), Bing Xie (Peking University)

**Categories:** Evolution and Maintenance

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334283

**中文总结:** 提出 HFDecomposer，以两阶段分组（相似度粗分 + LLM 读组摘要细分）并配合 dehallucination 缓解 token 限制与幻觉，混合 LLM 与传统相似度度量分解 God Header File，生成更贴合功能本质的重构方案。

**Abstract:** God Header Files, large header files included by numerous other code files, present significant challenges for code comprehension and maintenance while also increasing recompilation time. Existing approaches leverage various code similarity metrics to decompose such header files, but these metrics do not always capture the code’s functional essence accurately. Large Language Models (LLMs), with their advanced capabilities in code understanding and generation, offer a promising alternative for producing more effective refactorings. However, LLMs face limitations with lengthy code files due to token restrictions and reduced effectiveness in processing long inputs. Additionally, purely LLM-based solutions often suffer from hallucination, producing incomplete or spurious decomposition results. To address these challenges, we propose HFDecomposer, a hybrid approach that enhances LLMs with staged grouping and dehallucination techniques to effectively decompose header files. Our approach introduces a two-stage grouping framework for lengthy header files: it first groups strongly related code entities using traditional similarity metrics, then feeds group summaries to the LLM for higher-level semantic aggregation. To mitigate LLM hallucinations, we enhance prompts with factual knowledge extracted from static analysis, detect errors in LLM output, and make necessary corrections by reassigning missing entities and resolving cyclic dependencies. Our evaluation on real-world header file decomposition refactorings demonstrates that our method effectively overcomes the limitations of purely LLM-based techniques and outperforms the traditional state-of-the-art approach by 11%, delivering more accurate and reliable decomposition results. Our approach enables LLMs to handle lengthy header files efficiently, significantly reduces hallucinations, and ensures the reliability and practicality of the final decomposition.


## 9. Fact-Aligned and Template-Constrained Static Analyzer Rule Enhancement with LLMs

**Authors:** Zongze Jiang (Huazhong University of Science and Technology), Ming Wen (Huazhong University of Science and Technology), Ge Wen (Huazhong University of Science and Technology), Hai Jin (Huazhong University of Science and Technology)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334250

**中文总结:** 提出 RuleRefiner 多阶段框架，结合动态 profiling 对齐、差分故障定位与模板约束，用 LLM 直接精炼 Semgrep 检测规则；在 218 个真实规则问题上成功率最高达 80.28%，显著优于基线 LLM 方法。

**Abstract:** Static analyzers are vital to ensure software quality, but often produce false alarms; In this paper, we focus on the challenging task, directly refining defective static detection rules in the analyzer with Large Language Models to eliminate false positives/negatives fundamentally. This paper introduces RuleRefiner, a novel multi-stage framework for static analyzer rule refinement. RuleRefiner systematically employs LLMs by integrating dynamic profiling information for fact-based rule- code alignment, performing differential fault localization to ac-curately pinpoint error sources, and utilizing targeted templates to guide and constrain LLM-based modifications for precise and minimally disruptive enhancements. Evaluated on 218 real-world Semgrep rule issues, RuleRefiner achieved up to an 80.28% success rate, significantly outperforming baseline LLM methods by 1.34x-2.45x. Our results also demonstrate that RuleRefiner-refined rules are comparable, and sometimes superior, to expert-written ones in generalization and precision.


## 10. MCTS-Refined CoT: High-Quality Fine-Tuning Data for LLM-Based Repository Issue Resolution

**Authors:** Yibo Wang (Northeastern University), Zhihao Peng (Northeastern University), Ying Wang (Northeastern University), Zhao Wei (Tencent), Hai Yu (Northeastern University, China), Zhiliang Zhu (Northeastern University, China)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334706

**中文总结:** 提出 MCTS-Refine，在 MCTS 生成 issue 解决 CoT 数据时加入反思、拒绝采样与逐步校验，缓解弱拒绝采样与错误累积；用其微调的开源 LLM 在仓库级 issue 修复任务上显著优于现有 CoT 数据构造方法。

**Abstract:** LLMs demonstrate strong performance in automated software engineering, particularly for code generation and issue resolution. While proprietary models like \emph{GPT-4o} achieve high benchmarks scores on \emph{SWE-bench}, their API dependence, cost, and privacy concerns limit adoption. Open-source alternatives offer transparency but underperform in complex tasks, especially sub-100B parameter models. Although quality Chain-of-Thought (CoT) data can enhance reasoning, current methods face two critical flaws: (1) weak rejection sampling reduces data quality, and (2) inadequate step validation causes error accumulation. These limitations lead to flawed reasoning chains that impair LLMs’ ability to learn reliable issue resolution.

The paper proposes \textsc{MCTS-Refine}, an enhanced Monte Carlo Tree Search (MCTS)-based algorithm that dynamically validates and optimizes intermediate reasoning steps through a rigorous rejection sampling strategy, generating high-quality CoT data to improve LLM performance in issue resolution tasks. Key innovations include: (1) augmenting MCTS with a reflection mechanism that corrects errors via rejection sampling and refinement, (2) decomposing issue resolution into three subtasks—\emph{File Localization}, \emph{Fault Localization}, and \emph{Patch Generation}—each with clear ground-truth criteria, and (3) enforcing a strict sampling protocol where intermediate outputs must exactly match verified developer patches, ensuring correctness across reasoning paths.

Experiments on \emph{SWE-bench Lite} and \emph{SWE-bench Verified} demonstrate that LLMs fine-tuned with our CoT dataset achieve substantial improvements over baselines. Notably, \emph{Qwen2.5-72B-Instruct} achieves \textcolor{black}{28.3}%(\emph{Lite}) and \textcolor{black}{35.0}%(\emph{Verified}) resolution rates, surpassing SOTA baseline \emph{SWE-Fixer-Qwen-\textbf{72B}} with the same parameter scale, which only reached \textcolor{black}{24.7}%(\emph{Lite}) and \textcolor{black}{32.8}%(\emph{Verified}). Given precise issue locations as input, our fine-tuned \emph{Qwen2.5-72B-Instruct} model achieves an impressive issue resolution rate of 43.8%(\emph{Verified}), comparable to the performance of \emph{Deepseek-v3}. We open-source our \textsc{MCTS-Refine} framework, CoT dataset, and fine-tuned models to advance research in AI-driven software engineering.


## 11. On Automating Configuration Dependency Validation via Retrieval-Augmented Generation

**Authors:** Sebastian Simon (Leipzig University), Alina Mailach (Leipzig University), Johannes Dorn (Leipzig University), Norbert Siegmund (Leipzig University)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334571

**中文总结:** 大规模实证评估 RAG 能否改进 LLM 对配置依赖关系的校验：纳入项目/技术特定上下文后，plain LLM 已具较强能力而 RAG 提升有限甚至有害，并分析所需上下文类型。

**Abstract:** Configuration dependencies arise when multiple technologies in a software system require coordinated settings for correct interplay. Existing approaches for detecting such dependencies often yield high false-positive rates, require additional validation mechanisms, and are typically limited to specific projects or technologies. Recent work that incorporates large language models (LLMs) for dependency validation still suffers from inaccuracies due to project- and technology-specific variations, as well as from missing contextual information.

In this work, we propose to use retrieval-augmented generation (RAG) systems for configuration dependency validation, which allows us to incorporate  additional project- and technology-specific context information. Specifically, we evaluate whether RAG can improve LLM-based validation of configuration dependencies and what contextual information are needed to overcome the static knowledge base of LLMs. To this end, we conducted a large empirical study on validating configuration dependencies using RAG. Our evaluation shows that vanilla LLMs already demonstrate solid validation abilities, while RAG has only marginal or even negative effects on the validation performance of the models. By incorporating tailored contextual information into the RAG system–derived from a qualitative analysis of validation failures–we achieve significantly more accurate validation results across all models, with an average precision of 0.84 and recall of 0.70, representing improvements of 35% and 133% over vanilla LLMs, respectively. In addition, these results offer two important insights: Simplistic RAG systems may not benefit from additional information if it is not tailored to the task at hand, and it is often unclear upfront what kind of information yields improved performance.


## 12. Rechecking Recheck Requests in Continuous Integration: An Empirical Study of OpenStack

**Authors:** Yelizaveta Brus (University of Waterloo), Rungroj Maipradit (University of Waterloo), Earl T. Barr (University College London), Shane McIntosh (University of Waterloo)

**Categories:** Evolution and Maintenance

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334289

**中文总结:** 基于 OpenStack 314,947 次 recheck 请求，用统计模型区分会成功与仍会失败的 flaky CI 重测；AUROC 0.736，较基线提升 23.6 个百分点，并揭示作业/机器人/用户历史行为最具解释力。

**Abstract:** Continuous Integration (CI) is a process for automatically checking patch sets for errors. CI periodically fails due to non-deterministic (a.k.a., “flaky”) behaviour. Since a patch set may not be the cause of a flaky failure, developers can issue a “recheck” command to request retesting a patch set. Developers waste time considering whether or not to issue a recheck after a CI failure. Prior work also shows that rechecks are issued carelessly, wasting up to 187.4 compute years when CI continues to fail. To save developer time and avoid wasteful rechecks, we fit and analyze statistical models that discriminate between successful and failing rechecks, i.e. those rechecks that will change a failing CI run into a successful one and those that will fail again. Through an empirical study of 314,947 recheck requests from OpenStack, we find that our model successfully differentiates successful and failed rechecks, outperforming baseline approaches by 23.6 percentage points in terms of AUROC (0.736).

Analysis of our model suggests that, in terms of explanatory power, past behaviour of jobs, bots, and users dominate static characteristics of patch sets. Applying our model to automatically request rechecks for those predicted to succeed would have saved ~247 years of elapsed developer time for OpenStack. Applying our model to skip recheck requests when they are predicted to fail would avoid 86.49% of wasted rechecks, saving ~262 years of compute time.


## 13. SateLight: A Satellite Application Update Framework for Satellite Computing

**Authors:** Jinfeng Wen (Beijing University of Posts and Telecommunications), Jianshu Zhao (Beijing University of Posts and Telecommunications), Zixi Zhu (Beijing University of Posts and Telecommunications), Xiaomin Zhang (Beijing University of Posts and Telecommunications), Qi Liang (Beijing University of Posts and Telecommunications), Ao Zhou (Beijing University of Posts and Telecommunications), Shangguang Wang (Beijing University of Posts and Telecommunications)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334499

**中文总结:** 提出 SateLight 卫星应用更新框架，以容器封装异构应用，结合内容感知差分传输、细粒度 onboard 重构与分层容错恢复，适应有限带宽与恶劣空间环境。

**Abstract:** Satellite computing is an emerging paradigm that empowers satellites to perform onboard processing tasks (i.e., satellite applications), thereby reducing reliance on ground-based systems and improving responsiveness. However, enabling application software updates in this context remains a fundamental challenge due to application heterogeneity, limited ground-to-satellite bandwidth, and harsh space conditions. Existing software update approaches, designed primarily for terrestrial systems, fail to address these constraints, as they assume abundant computational capacity and stable connectivity.

To address this gap, we propose SateLight, a practical and effective satellite application update framework tailored for satellite computing. SateLight leverages containerization to encapsulate heterogeneous applications, enabling efficient deployment and maintenance. SateLight further integrates three capabilities: (1) a content-aware differential strategy that minimizes communication data volume, (2) a fine-grained onboard update design that reconstructs target applications, and (3) a layer-based fault-tolerant recovery mechanism to ensure reliability under failure-prone space conditions. Experimental results on a satellite simulation environment with 10 representative satellite applications demonstrate that SateLight reduces transmission latency by up to 91.18% (average 56.54%) compared to the best currently available baseline. It also consistently ensures 100% update correctness across all evaluated applications. Furthermore, a case study on a real-world in-orbit satellite demonstrates the practicality of our approach.


## 14. Speculative Automated Refactoring of Imperative Deep Learning Programs to Graph Execution

**Authors:** Raffi Khatchadourian (CUNY Hunter College), Tatiana Castro Vélez (University of Puerto Rico, Rio Piedras Campus), Mehdi Bagherzadeh (Oakland University), Nan Jia (City University of New York (CUNY) Graduate Center), Anita Raja (City University of New York (CUNY) Hunter College)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334300

**中文总结:** 提出基于静态 imperative 张量分析与副作用分析的自动化重构，将 Python  eager 深度学习代码投机性地转为图执行，在保持可调试性的同时提升运行效率。

**Abstract:** Efficiency is essential to support ever-growing datasets, especially for Deep Learning (DL) systems. DL frameworks have traditionally embraced deferred execution-style DL code—supporting symbolic, graph-based Deep Neural Network (DNN) computation. While scalable, such development is error-prone, non-intuitive, and difficult to debug. Consequently, more natural, imperative DL frameworks encouraging eager execution have emerged but at the expense of run-time performance. Though hybrid approaches aim for the “best of both worlds,” using them effectively requires subtle considerations. Our key insight is that, while DL programs typically execute sequentially, hybridizing imperative DL code resembles parallelizing sequential code in traditional systems. Inspired by this, we present an automated refactoring approach that assists developers in determining which otherwise eagerly-executed imperative DL functions could be effectively and efficiently executed as graphs. The approach features novel static imperative tensor and side-effect analyses for Python. Due to its inherent dynamism, analyzing Python may be unsound; however, the conservative approach leverages a speculative (keyword-based) analysis for resolving difficult cases that informs developers of any assumptions made. The approach is: (i) implemented as a plug-in to the PyDev Eclipse IDE that integrates the WALA Ariadne analysis framework and (ii) evaluated on nineteen DL projects consisting of 132 KLOC. The results show that 326 of 766 candidate functions (42.56%) were refactorable, and an average relative speedup of 2.16 on performance tests was observed with negligible differences in model accuracy. The results indicate that the approach is useful in optimizing imperative DL code to its full potential.


## 15. What’s DAT Smell? Untangling and Weaving the Disjoint Assertion Tangle Test Smell

**Authors:** Monil Narang (University of California, Irvine), Hang Du (University of California at Irvine), James Jones (University of California at Irvine)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334242

**中文总结:** 刻画 Disjoint Assertion Tangle（DAT）测试坏味并实现工具 U2W，自动检测单测中逻辑无关的多行为断言并拆分为聚焦测试，再合并为参数化测试；大规模评估与用户调研显示可读性、可维护性与缺陷定位均改善。

**Abstract:** Writing and maintaining good unit tests is essential for quality assurance. However, developers often deprioritize such maintenance, leading to tests that exhibit code smells, are bloated, and may be less effective. In this work, we characterize a novel test-code smell—Disjoint Assertion Tangle (DAT)—which occurs when a test method verifies multiple, logically unrelated behaviors that can be separated. We propose a program analysis-based approach that automatically detects DATs and refactors them into separate focused test methods. We implemented this approach as a tool called U2W. By separating unrelated testing logic, U2W enhances readability, maintainability, and fault localization, while exposing hidden test clones and duplicated code. It then seizes these opportunities by converting structurally similar tests into compact, parameterized unit tests (PUTs), reducing redundancy and enabling more scalable, extensible test designs.

To evaluate our approach and tool, we conducted a number of evaluations: (1) a large-scale, quantitative study to study the prevalence of the test smell and the effects of their refactoring, (2) a user survey to assess developers’ opinions and preferences of the unrefactored and refactored test code, and (3) pull requests that were issued to original project maintainers to assess the acceptability of our refactorings. Our quantitative study was conducted on 42,334 tests across 49 open-source projects. We found the DAT smell in 95.9% of the subject projects, affecting an average of 8.59% of analyzed tests. In total, we identified and refactored 3,638 smelly tests, untangled them into 31,837 test-execution logics, and then weaved 14,343 of them into 1,713 extensible PUT methods. These refactorings reduced the executable test-code lines in smelly tests by an average of 36.33%. Our user survey involving 49 industrial and academic participants demonstrated strong preference for our refactored test cases over their original, unrefactored versions. Additionally, we submitted 19 pull requests based on our automated refactorings; 16 of these were accepted by project maintainers. These results suggest that U2W effectively improves test-suite quality, and validate our novel test smell aligns closely with developers’ intuitions and practices.


## 16. Which Is Better For Reducing Outdated And Vulnerable Dependencies: Pinning Or Floating?

**Authors:** Imranur Rahman (North Carolina State University), Jill Marley (North Carolina State University), William Enck (North Carolina State University), Laurie Williams (North Carolina State University)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334547

**中文总结:** 大规模实证比较 pinning 与 floating 等依赖版本约束类型下依赖变旧或含漏洞的概率及演化模式；为开发者在供应链安全与自动更新风险之间选择版本策略提供量化依据。

**Abstract:** Developers consistently use version constraints to specify acceptable versions of the dependencies for their project. \emph{Pinning} dependencies can reduce the likelihood of breaking changes, but comes with a cost of manually managing the replacement of outdated and vulnerable dependencies. On the other hand, \emph{floating} can be used to automatically get bug fixes and security fixes, but comes with the risk of breaking changes. Security practitioners advocate \emph{pinning} dependencies to prevent against software supply chain attacks, e.g., malicious package updates. However, since \emph{pinning} is the tightest version constraint, \emph{pinning} is the most likely to result in outdated dependencies. Nevertheless, how the likelihood of becoming outdated or vulnerable dependencies changes across version constraint types is unknown. \textit{The goal of this study is to aid developers in making an informed dependency version constraint choice by empirically evaluating the likelihood of becoming outdated or vulnerable dependencies across version constraint types at scale.} In this study, we first identify the trends in dependency version constraint usage and the patterns of version constraint type changes made by developers in the npm, PyPI, and Cargo ecosystems. We then modeled the dependency state transitions in survival analysis and estimated how the likelihood of becoming outdated or vulnerable changes when using \emph{pinning} as opposed to the rest of the version constraint types. We observe that among outdated and vulnerable dependencies, the most commonly used version constraint type is \emph{floating-minor}, with \emph{pinning} being the next most common. We also find that \emph{floating-major} is the least likely to result in outdated and \emph{floating-minor} is the least likely to result in vulnerable dependencies. Based on our findings, we recommend that developers use any kind of \emph{floating} constraint with lockfiles to balance the tradeoffs of \emph{pinning} and \emph{floating}.


## 17. Wired for Reuse: Automating Context-Aware Code Adaptation in IDEs via LLM-Based Agent

**Authors:** Taiming Wang (Beijing Institute of Technology), Yanjie Jiang (Peking University), Chunhao Dong (Beijing Institute of Technology), Yuxia Zhang (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334399

**中文总结:** 提出 LLM agent WIRL，将 copy-paste 后 code wiring（上下文变量替换）建模为 RAG 填空任务，结合工具包与状态机混合规则与自主探索；在 curated 基准上实现上下文感知的 IDE 内代码适配自动化。

**Abstract:** \textit{Copy-paste-modify} is a widespread and pragmatic practice in software development, where developers adapt reused code snippets—sourced from platforms such as Stack Overflow, GitHub, or LLM outputs—into their local codebase. A critical yet underexplored aspect of this adaptation is \textit{code wiring}, which involves substituting unresolved variables in the pasted code with suitable ones from the surrounding context. Existing solutions either rely on heuristic rules or historical templates, often failing to effectively utilize contextual information, despite studies showing that over half of adaptation cases are context-dependent. In this paper, we introduce \emph{WIRL}, an LLM-based agent for code wiring framed as a Retrieval-Augmented Generation (RAG) infilling task. \emph{WIRL} combines an LLM, a customized toolkit, and an orchestration module to identify unresolved variables, retrieve context, and perform context-aware substitutions. To balance efficiency and autonomy, the agent adopts a mixed strategy: deterministic rule-based steps for common patterns, and a state-machine-guided decision process for intelligent exploration. We evaluate \emph{WIRL} on a carefully curated, high-quality dataset consisting of real-world code adaptation scenarios. Our approach achieves an exact match precision of 91.7% and a recall of 90.0%, outperforming advanced LLMs by 22.6 and 13.7 percentage points in precision and recall, respectively, and surpassing IntelliJ IDEA by 54.3 and 49.9 percentage points. These results underscore its practical utility, particularly in contexts with complex variable dependencies or multiple unresolved variables. We believe \emph{WIRL} paves the way for more intelligent and context-aware developer assistance in modern IDEs.


## 18. Your Build Scripts Stink: The State of Code Smells in Build Scripts

**Authors:** Mahzabin Tamanna (North Carolina State University), Yash Chandrani (North Carolina State University), Matthew Burrows (North Carolina State University), Brandon Wroblewski (North Carolina State University), Dominik Wermke (North Carolina State University), Laurie Williams (North Carolina State University)

**Categories:** Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11334409

**中文总结:** 混合方法研究 Maven/Gradle/CMake/Makefile 构建脚本坏味：分析 2000 条 GitHub issue 并开发 Sniffer 扫描 4877 仓库 5882 脚本，识别 13 类共 10895 处 smell；Makefiles 问题最多，不安全 URL 等风险模式突出。

**Abstract:** Build scripts are files that automate the process of compiling source code, managing dependencies, running tests, and packaging software into deployable artifacts. These scripts are ubiquitous in modern software development pipelines for streamlining testing and delivery. While developing build scripts, practitioners may inadvertently introduce code smells. Code smells are recurring patterns of poor coding practices that may lead to build failures or increase risk and technical debt. The goal of this study is to aid practitioners in avoiding code smells in build scripts through an empirical study of build scripts and issues on GitHub. We employed a mixed-methods approach, combining qualitative and quantitative analysis. We conducted a qualitative analysis of 2000 build-script-related GitHub issues. Next, we developed a static analysis tool, Sniffer, to identify code smells in 5882 build scripts of Maven, Gradle, CMake, and Makefiles, collected from 4877 open-source GitHub repositories. We identified 13 code smell categories, with a total of 10,895 smell occurrences, where 3184 were in Maven, 1214 in Gradle, 337 in CMake, and 6160 in Makefiles. Our analysis revealed that Insecure URLs were the most prevalent code smell in Maven build scripts, while Hardcoded Paths/URLs were commonly observed in both Gradle and CMake scripts. Wildcard Usage emerged as the most frequent smell in Makefiles. The co-occurrence analysis revealed strong associations between specific smell pairs of Hardcoded Paths/URLs with duplicates, and Inconsistent Dependency Management with Empty or Incomplete Tags, indicating potential underlying issues in the build script structure and maintenance practices. Based on our findings, we recommend strategies to mitigate the existence of code smells in build scripts to improve the efficiency, reliability, and maintainability of software projects.

