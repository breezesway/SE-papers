# FSE 2025 Research Track — Debugging and Fault Diagnosis

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 17 papers

## 1. A Comprehensive Study of Bug-Fix Patterns in Autonomous Driving Systems

**Authors:** Yuntianyi Chen (University of California, Irvine), Yuqi Huai (University of California, Irvine), Yirui He (University of California, Irvine), Shilong Li (University of California, Irvine), Changnam Hong (University of California, Irvine), Alfred Chen (University of California, Irvine), Joshua Garcia (University of California, Irvine)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715733

**中文总结:** 对 Apollo 与 Autoware 共 1331 个缺陷修复做实证研究，归纳 15 种句法与 27 种语义 bug-fix 模式及 ADS 缺陷层次；并贡献相应基准，揭示路径规划、数据流与配置等主导模式。

**Abstract:** As autonomous driving systems (ADSes) become increasingly complex and integral to daily life, the importance of understanding the nature and mitigation of software bugs in these systems has grown correspondingly. Addressing the intricacies of software maintenance in autonomous driving systems is an evident requirement. The potential of automated tools in this domain is promising, yet there remains a gap in our comprehension of the challenges faced and the strategies employed during manual debugging and repair of such systems. In this paper, we present an empirical study that investigates bug-fix patterns in ADSes, with the aim of improving reliability and safety. We have analyzed the commit histories and bug reports of two major autonomous driving projects, Apollo and Autoware, from 1,331 bug fixes with the study of bug symptoms, root causes, and bug-fix patterns. Our study reveals several dominant bug-fix patterns, including those related to path planning, data flow, and configuration management. Additionally, we find that the frequency distribution of bug-fix patterns varies significantly depending on their nature and types and that certain categories of bugs are recurrent and more challenging to exterminate. Based on our findings, we propose a hierarchy of ADS bugs and two taxonomies of 15 syntactic bug-fix patterns and 27 semantic bug-fix patterns that offer guidance for bug identification and resolution. We also contribute a benchmark of 1,331 ADS bug-fix instances.

## 2. Alert Summarization for Online Service Systems by Validating Propagation Paths of Faults

**Authors:** ChenJ, Yuang He, Peng Wang, XiaoLei Chen, Jie Shi, Wei Wang

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729367

**中文总结:** 提出 ProAlert，离线学习故障传播模式并用其在线校验拓扑上的故障路径，将告警汇总为事件；相对仅看连通性的方法更准确，且传播路径提升可解释性。

**Abstract:** For online service systems, alerts are crucial for root cause analysis as they capture symptoms triggered by system faults. In real-world scenarios, a fault can propagate across multiple system components, generating a large volume of alerts. Various approaches have been proposed to summarize alerts into incidents to accelerate root cause analysis, using the topology information. However, these approaches focus solely on connectivity, neglecting the semantics of the topology, which significantly impacts their performance. In this paper, we introduce ProAlert, a novel topology-based approach that summarizes alerts into incidents by validating fault propagation paths. ProAlert first unsupervisedly learns fault propagation patterns from historical alerts and system topology offline. It then uses these patterns to validate fault paths in real-time alerts, leading to more accurate incident summarization. Moreover, the fault propagation paths provided by ProAlert improve the interpretability of incidents, assisting maintenance engineers in understanding the root causes of faults. To demonstrate the effectiveness and efficiency of ProAlert, we conduct extensive experiments on real-world data. The results show that ProAlert outperforms state-of-the-art approaches.

## 3. An Empirical Study of Bugs in Data Visualization Libraries

**Authors:** Weiqi Lu (The Hong Kong University of Science and Technology), Yongqiang Tian, Xiaohan Zhong (The Hong Kong University of Science and Technology), Haoyang Ma (Hong Kong University of Science and Technology), Zhenyang Xu (University of Waterloo), Shing-Chi Cheung (Hong Kong University of Science and Technology), Chengnian Sun (University of Waterloo)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729363

**中文总结:** 对五个主流数据可视化库的 564 个缺陷做首次系统分析，给出症状/根因分类并提炼触发步骤与两类测试预言；发现错误绘图普遍且图形计算是主因，并探索 VLM 检测有效性约 29%–57%。

**Abstract:** Data visualization (DataViz) libraries play a crucial role in presentation, data analysis, and application development, underscoring the importance of their accuracy in transforming data into visual representations. Incorrect visualizations can adversely impact user experience, distort information conveyance, and influence user perception and decision-making processes. Visual bugs in these libraries can be particularly insidious as they may not cause obvious errors like crashes, but instead mislead users of the underlying data graphically, resulting in wrong decision making. Consequently, a good understanding of the unique characteristics of bugs in DataViz libraries is essential for researchers and developers to detect and fix bugs in DataViz libraries. This study presents the first comprehensive analysis of bugs in DataViz libraries, examining 564 bugs collected from five widely-used libraries. Our study systematically analyzes their symptoms and root causes, and provides a detailed taxonomy. We found that incorrect/inaccurate plots are pervasive in DataViz libraries and incorrect graphic computation is the major root cause, which necessitates further automated testing methods for DataViz libraries. Moreover, we identified eight key steps to trigger such bugs and two test oracles specific to DataViz libraries, which may inspire future research in designing effective automated testing techniques. Furthermore, with the recent advancements in Vision Language Models (VLMs), we explored the feasibility of applying these models to detect incorrect/inaccurate plots. The results show that the effectiveness of VLMs in bug detection varies from 29% to 57%, depending on the prompts, and adding more information in prompts does not necessarily increase the effectiveness. Our findings offer valuable insights into the nature and patterns of bugs in DataViz libraries, providing a foundation for developers and researchers to improve library reliability, and ultimately benefit more accurate and reliable data visualizations across various domains.

## 4. Automated Recognition of Buggy Behaviors from Mobile Bug Reports

**Authors:** Zhaoxu Zhang, Komei Ryu, Tingting Yu, William G.J. Halfond

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729370

**中文总结:** 提出从移动应用缺陷报告自动抽取 buggy behavior 并标准化表示，在复现过程中对照设备与 UI 实时识别缺陷；评估显示能识别多种 bug 并提升自动复现流程。

**Abstract:** Bug report reproduction is a crucial but time-consuming task to be carried out during mobile app maintenance. To accelerate this process, researchers have developed automated techniques for reproducing mobile app bug reports. However, due to the lack of an effective mechanism to recognize different buggy behaviors described in the report, existing work is limited to reproducing a narrow scope of bug reports, or requires developers to manually analyze execution traces to determine if a bug was successfully reproduced. To address this limitation, we introduce a novel technique to automatically extract the buggy behavior from the bug report and recognize it during the automated reproduction process. To accommodate various buggy behaviors of mobile app bugs, we conducted a large-scale empirical study and created standardized representation for expressing the bug manifestations identified from our study. Given a report, our approach first transforms the documented buggy behavior into this structured language, then matches it against real-time device and UI information during the reproduction to recognize the bug. Through an empirical evaluation, we showed the effectiveness of our approach in recognizing different bugs and the usefulness of our approach in the automatic reproduction process.

## 5. ChatDBG: Augmenting Debugging with Large Language Models

**Authors:** Kyla H. Levin (University of Massachusetts Amherst, USA), Nicolas van Kempen (University of Massachusetts Amherst, USA), Emery D. Berger (University of Massachusetts Amherst and Amazon Web Services), Stephen N. Freund (Williams College)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifact-Available, Artifact-Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729355

**中文总结:** 提出 ChatDBG，将 LLM 接入 LLDB/GDB/Pdb，使调试器可自主查询程序状态并协作完成根因分析与修复建议；在 Python 上单次查询可给出可操作修复达 67%，追加追问升至 85%，下载超 7.5 万次。

**Abstract:** Debugging is a critical but challenging task for programmers. This paper proposes ChatDBG, an AI-powered debugging assistant. ChatDBG integrates large language models (LLMs) to significantly enhance the capabilities and user-friendliness of conventional debuggers. ChatDBG lets programmers engage in a collaborative dialogue with the debugger, allowing them to pose complex questions about program state, perform root cause analysis for crashes or assertion failures, and explore open-ended queries like “why is x null?”. To handle these queries, ChatDBG grants the LLM autonomy to “take the wheel”: it can act as an independent agent capable of querying and controlling the debugger to navigate through stacks and inspect program state. It then reports its findings and yields back control to the programmer. By leveraging the real-world knowledge embedded in LLMs, ChatDBG can diagnose issues identifiable only through the use of domain-specific reasoning. Our ChatDBG prototype integrates with standard debuggers including LLDB and GDB for native code and Pdb for Python. Our evaluation across a diverse set of code, including C/C++ code with known bugs and a suite of Python code including standalone scripts and Jupyter notebooks, demonstrates that ChatDBG can successfully analyze root causes, explain bugs, and generate accurate fixes for a wide range of real-world errors. For the Python programs, a single query led to an actionable bug fix 67% of the time; one additional follow-up query increased the success rate to 85%. ChatDBG has seen rapid uptake; it has already been downloaded more than 75,000 times.

## 6. Cross-System Categorization of Abnormal Traces in Microservice-Based Systems via Meta-Learning

**Authors:** Yuqing Wang (University of Helsinki, Finland), Mika Mäntylä (University of Helsinki and University of Oulu), Serge Demeyer (University of Antwerp and Flanders Make vzw), Mutlu Beyazıt (University of Antwerp and Flanders Make vzw), Joanna Kisaakye (University of Antwerp, Belgium), Jesse Nyyssölä (University of Helsinki)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715742

**中文总结:** 提出 TraFaultDia，将微服务异常轨迹按故障类型做少样本多类分类，并用元学习实现跨系统快速适配；在 TrainTicket/OnlineBoutique 上系统内平均准确率 93.26%/85.2%，跨系统达 92.19%/84.77%。

**Abstract:** Microservice-based systems (MSS) may fail with various fault types, due to their complex and dynamic nature. While existing AIOps tools excel at detecting abnormal traces and pinpointing the responsible service(s), human efforts from practitioners are still required for further root cause analysis (RCA) to diagnose specific fault types and analyze failure reasons for detected abnormal traces, particularly when abnormal traces do not stem directly from specific services. This paper presents TraFaultDia, a novel framework aimed at automatically classifying abnormal traces into precise fault categories for different MSS. We approach the automatic categorization of abnormal traces into fault types as a series of multi-class classification tasks, each task represents an attempt to classify detected abnormal traces for a MSS. With the classification results from TraFaultDia, practitioners can quickly know fault types of abnormal traces and understand their nature of failures and potential impacts, thereby reducing the time and effort required for manual analysis. TraFaultDia is trained on several abnormal trace classification tasks with a few labeled instances from a MSS using a meta-learning approach. After training, TraFaultDia can quickly adapt to new, unseen abnormal trace classification tasks with a few labeled instances across MSS. We evaluated TraFaultDia on two representative MSS, TrainTicket and OnlineBoutique, with open datasets. Our results show that, within the MSS it is trained on, TraFaultDia achieves an average accuracy of 93.26% and 85.2% across 50 new, unseen abnormal trace classification tasks for TrainTicket and OnlineBoutique respectively, when provided with 10 labeled instances for each fault category per task in each system. In the cross-system context, when TraFaultDia is applied to a MSS different from the one it is trained on, TraFaultDia gets an average accuracy of 92.19% and 84.77% for the same set of 50 new, unseen abnormal trace classification tasks of the respective system, also with 10 labeled instances provided for each fault category per task in each system.

## 7. Detecting Metadata-Related Bugs in Enterprise Applications

**Authors:** Md Mahir Asef Kabir (Virginia Tech), Xiaoyin Wang (University of Texas at San Antonio), Na Meng (Virginia Tech)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifact-Available, Artifact-Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715772

**中文总结:** 提出领域语言 RSL 与工具 MeCheck，由专家编写元数据一致性规则并对 Java/XML 做跨文件静态检查，以发现企业应用中注解与配置误用；在注入缺陷集上精度 100%、召回 96%，并在真实项目中报告 156 个缺陷（53 个已被修复）。

**Abstract:** When building enterprise applications (EAs) on Java frameworks (e.g., Spring), developers often configure application components via metadata (i.e., Java annotations and XML files). It is challenging for developers to correctly use metadata, because the usage rules can be complex and existing tools provide limited assistance. When developers misuse metadata, EAs become misconfigured, which defects can trigger erroneous runtime behaviors or introduce security vulnerabilities. To help developers correctly use metadata, this paper presents (1) RSL—a domain-specific language that domain experts can adopt to prescribe metadata checking rules, and (2) MeCheck —a tool that takes in RSL rules and EAs to check for rule violations. With RSL, domain experts (e.g., developers of a Java framework) can specify metadata checking rules by defining content consistency among XML files, annotations, and Java code. Given such RSL rules and a program to scan, MeCheck interprets rules as cross-file static analyzers, which analyzers scan Java and/or XML files to gather information and look for consistency violations. For evaluation, we studied the Spring and JUnit documentation to manually define 15 rules, and created 2 datasets with 115 open-source EAs. The first dataset includes 45 EAs, and the ground truth of 45 manually injected bugs. The second dataset includes multiple versions of 70 EAs. We observed that MeCheck identified bugs in the first dataset with 100% precision, 96% recall, and 98% F-score. It reported 156 bugs in the second dataset, 53 of which bugs were already fixed by developers. Our evaluation shows that MeCheck helps ensure the correct usage of metadata.

## 8. Dissecting Real-World Cross-Language Bugs

**Authors:** Haoran Yang (Washington State University), Haipeng Cai (University at Buffalo, SUNY)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifact-Available, Artifact-Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715777

**中文总结:** 对 400 个真实跨语言缺陷做系统刻画（症状、位置、表现、根因与修复），并比较 Python-C 与 Java-C 组合差异；基于从 54,356 次相关提交中筛选的数据，给出跨语言缺陷预防、检测与修补的实践建议。

**Abstract:** Multilingual systems are prevalent and broadly impactful, but also complex due to the intricate interactions between the heterogeneous programming languages the systems are developed in. This complexity is further aggravated by the diversity of cross-language interoperability across different language combinations, resulting in additional, often stealthy cross-language bugs. Yet despite the growing number of tools aimed to discover cross-language bugs, a systematic understanding of such bugs is still lacking. To fill this gap, we conduct the first comprehensive study of cross-language bugs, characterizing them in five aspects including their symptoms, locations, manifestation, root causes, and fixes. Through detailed analysis of 400 cross-language bugs in real-world multilingual projects classified from 54,356 relevant code commits in their GitHub repositories, we revealed not only bug characteristics of those five aspects but also how they compare between two top language combinations in the multilingual world (Python-C and Java-C). In addition to the empirical findings as well as its enabling tools and datasets, we also provide practical recommendations regarding the prevention, detection, and patching of cross-language bugs.

## 9. DuoReduce: Bug Isolation for Multi-Layer Extensible Compilation

**Authors:** Jiyuan Wang (University of California at Los Angeles), Yuxin Qiu (University of California at Riverside), Ben Limpanukorn (University of California, Los Angeles), Hong Jin Kang (University of Sydney), Qian Zhang (University of California at Riverside), Miryung Kim (UCLA and Amazon Web Services)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715747

**中文总结:** 提出 DuoReduce，同时在 IR 与编译 pass 双维度缩减 MLIR 缺陷触发输入，利用 pass 序依赖、语义感知变换与跨维相关降低无关 pass；相对 Perses/Vulcan 的 IR 缩减分别提升 31.6%/21.5%，并将枚举 pass 的调试时间从最高约 145 小时降至约 9.5 分钟。

**Abstract:** In recent years, the MLIR platform has had explosive growth due to the need of building extensible deep learning compilers and hardware accelerator compilers. Such examples include Triton, CIRCT, and ONNX-MLIR. MLIR compilers introduce significant complexities in localizing bugs or inefficiencies because of their layered optimization and transformation process with compilation passes. While existing delta debugging techniques can be used to identify a minimum subset of IR code that reproduces a given bug symptom, their naive application to MLIR is time-consuming, because real-world MLIR compilers usually involve a large number of compilation passes and compiler developers must also identify a minimized set of relevant compilation passes simultaneously, in order to reduce the footprint of MLIR compiler code to be inspected for a bug fix. We propose DuoReduce, a dual-dimensional reduction approach for MLIR bug localization. DuoReduce leverages three key ideas in tandem to design an efficient MLIR debugger. First, DuoReduce reduces the bug-irrelevant compilation passes by identifying ordering dependencies among different compilation passes. Second, DuoReduce uses MLIR-semantics aware transformations to expedite IR code reduction. Finally, DuoReduce leverages cross-dependence between the IR code dimension and the compilation pass dimension by accounting for which IR code segments are related to which compilation passes to reduce the unused passes. Experiments with three large-scale MLIR compiler projects find that DuoReduce outperforms syntax-aware reducers such as Perses and Vulcan in terms of IR code reduction by 31.6% and 21.5% respectively. If one uses these reducers by enumerating all possible compilation passes (on average 18 passes), it could take up to 145 hours. By identifying ordering dependencies among compilation passes, DuoReduce reduces this time to 9.5 minutes. By identifying which compilation passes are unused for compiling reduced IR code, DuoReduce reduces the number of passes by 14.6%. This translates to not needing to examine 281 lines of MLIR compiler code on average to fix the bugs. DuoReduce has the potential to significantly reduce debugging effort in multi-layer extensible compilers, which serves as an important basis for the current landscape of machine learning and hardware accelerators.

## 10. Empirically Evaluating the Impact of Object-Centric Breakpoints on the Debugging of Object-Oriented Programs

**Authors:** Valentin Bourcier (INRIA), Pooja Rani (University of Zurich), Maximilian Ignacio Willembrinck Santander (Univ. Lille, Inria, CNRS, Centrale Lille, UMR 9189 CRIStAL F-59000 Lille, France), Alberto Bacchelli (University of Zurich), Steven Costiou (INRIA Lille)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715759

**中文总结:** 对 81 名开发者开展受控实验，评估面向对象调试中 object-centric breakpoints 的实际影响。结果显示其对操作次数与修错效果无显著作用，但对调试时间的影响因任务与缺陷是否可在不重启程序下复现而异。

**Abstract:** Debugging consists in understanding the behavior of a program to identify and correct its defects. Breakpoints are the most commonly used debugging tool and aim to facilitate the debugging process by allowing developers to interrupt a program’s execution at a source code location of their choice and inspect the state of the program. Researchers suggest that in systems developed using object-oriented programming (OOP), traditional breakpoints may be a not effective method for debugging. In OOP, developers create code in classes, which at runtime are instantiated as object—entities with their own state and behavior that can interact with one another. Traditional breakpoints are set within the class code, halting execution for every object that shares that class’s code. This leads to unnecessary interruptions for developers who are focused on monitoring the behavior of a specific object. As an answer to this challenge, researchers proposed object-centric debugging , an approach based on debugging tools that focus on objects rather than classes. In particular, using object-centric breakpoints , developers can select specific objects (rather than classes) for which the execution must be interrupted. Even though it seems reasonable that this approach may ease the debugging process by reducing the time and actions needed for debugging objects, no research has yet verified its actual impact. To investigate the impact of object-centric breakpoints on the debugging process, we devised and conducted a controlled experiment with 81 developers who spent an average of 1 hour and 30 minutes each on the study. The experiment required participants to complete two debugging tasks using debugging tools with vs. without object-centric breakpoints. We found no significant effect from the use of object-centric breakpoints on the number of actions required to debug or the effectiveness in understanding or fixing the bug. However, for one of the two tasks, we measured a statistically significant reduction in debugging time for participants who used object-centric breakpoints, while for the other task, there was a statistically significant increase. Our analysis suggests that the impact of object-centric breakpoints varies depending on the context and the specific nature of the bug being addressed. In particular, our analysis indicates that object-centric breakpoints can speed up the process of locating the root cause of a bug when the bug can be replicated without needing to restart the program. We discuss the implications of these findings for debugging practices and future research.

## 11. Error Delayed is Not Error Handled: Understanding and Fixing Propagated Error-Handling Bugs

**Authors:** Haoran Liu (National University of Defense Technology), Shanshan Li (National University of Defense Technology), Zhouyang Jia (National University of Defense Technology), Yuanliang Zhang (National University of Defense Technology), Linxiao Bai (National University of Defense Technology), Si Zheng (National University of Defense Technology), Xiaoguang Mao (National University of Defense Technology), Liao Xiangke (National University of Defense Technology)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729384

**中文总结:** 首次深入刻画跨函数传播的错误处理（PEH）缺陷，并提出基于 LLM 与检索增强的修复工具 EH-Fixer。在 Linux Kernel 等系统的 58 个历史 PEH 缺陷上修复率达 82.8%（48/58）。

**Abstract:** Error handling is critical for software reliability. In software systems, error handling may be delayed to other functions. Such propagated error handling (PEH) could easily be missed and lead to bugs. Our research reveals that PEH bugs are prevalent in software systems and, on average, take 42.3 days to fully address. Existing approaches have primarily focused on the error-handling bug within individual functions, which makes it difficult to fully address PEH bugs. In this paper, we conducted the first in-depth study on PEH bugs in 6 mature software systems, examining how errors propagate and how they should be handled. We introduce EH-Fixer, an LLM-based tool for automated program repair specifically designed to address PEH bugs. For each PEH bug, EH-Fixer constructs its propagation path, and repairs them through retrieval-augmented generation. To assess the performance of our approach, we collected 58 historical PEH bugs from the Linux Kernel as well as 4 widely used applications. The experimental results show that EH-Fixer can fix 82.8% (48/58) of PEH bugs.

## 12. Improving Graph Learning-Based Fault Localization with Tailored Semi-Supervised Learning

**Authors:** Chun Li (Nanjing University), Hui Li (Samsung Electronics (China) R&D Centre), Zhong Li, Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715788

**中文总结:** 针对有标签失败测试稀缺导致的监督图学习缺陷定位瓶颈，提出半监督框架 Legato：增强无关子图并估计伪标签以利用未标注数据。在与三种半监督基线对比中全面更优。

**Abstract:** Due to advancements in graph neural networks, graph learning-based fault localization (GBFL) methods have achieved promising results. However, as these methods are supervised learning paradigms and deep learning is typically data-hungry, they can only be trained on fully labeled large-scale datasets. This is impractical because labeling failed tests is similar to manual fault localization, which is time-consuming and labor-intensive, leading to only a small portion of failed tests that can be labeled within limited budgets. These data labeling limitations would lead to the sub-optimal effectiveness of supervised GBFL techniques. Semi-supervised learning (SSL) provides an effective means of leveraging unlabeled data to improve a model’s performance and address data labeling limitations. However, as these methods are not specifically designed for fault localization, directly utilizing them might lead to sub-optimal effectiveness. In response, we propose a novel semi-supervised GBFL framework, Legato. Legato first leverages the attention mechanism to identify and augment likely fault-unrelated sub-graphs in unlabeled graphs and then quantifies the suspiciousness distribution of unlabeled graphs to estimate pseudo-labels. Through training the model on augmented unlabeled graphs and pseudo-labels, Legato can utilize the unlabeled data to improve the effectiveness of fault localization and address the restrictions in data labeling. Through extensive evaluations against 3 baselines SSL methods, Legato demonstrates superior performance by outperforming all the methods in comparison.

## 13. ReproCopilot: LLM-Driven Failure Reproduction with Dynamic Refinement

**Authors:** Tanakorn Leesatapornwongsa (Microsoft Research), Fazle Faisal (Microsoft Research), Suman Nath (Microsoft Research)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729399

**中文总结:** ReproCopilot 结合程序分析与 LLM，通过面向状态的代码生成与动态 refinement 迭代反馈，自动生成失败复现代码与输入。在 15 个开源项目的 37 个真实案例上复现率 78%，显著优于现有方案。

**Abstract:** Failure reproduction is a crucial step for debugging software systems, but it is often challenging and time-consuming, especially when the failures depend on complex inputs, states, or environments. In this paper, we present ReproCopilot, a tool that leverages program analysis and a large language model (LLM) to generate failure reproduction code and inputs. ReproCopilot proposes two novel techniques: state-oriented code generation and dynamic refinement that iteratively guide the LLM with program analysis feedback until the generated code can successfully reproduce the failure. We evaluate ReproCopilot on 37 real-world cases from 15 open-source projects, and show that it can reproduce 78% of them, significantly outperforming the-state-of-the-art solutions.

## 14. SemBIC: Semantic-aware Identification of Bug-inducing Commits

**Authors:** Xiao Chen (The Hong Kong University of Science and Technology), Hengcheng Zhu (The Hong Kong University of Science and Technology), Jialun Cao (Hong Kong University of Science and Technology), Ming Wen (Huazhong University of Science and Technology), Shing-Chi Cheung (Hong Kong University of Science and Technology)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifact-Available, Artifact-Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715781

**中文总结:** SemBIC 在失败测试不可在历史版本执行时，静态追踪失败执行路径上跨提交的语义变化以定位引入缺陷的提交（BIC）。在 12 项目 199 个真实缺陷上 Top-1 命中 80 个、MRR 0.494，分别优于 SOTA 约 17.6% 与 8.1%。

**Abstract:** Debugging can be much facilitated if one can identify the evolution commit that introduced the bug leading to a detected failure (aka. bug-inducing commit, BIC). Although one may, in theory, locate BICs by executing the detected failing test on various historical commit versions, it is impractical when the test cannot be executed on the historical commit versions. On the other hand, existing static techniques often assume the availability of additional information such as patches and bug reports, or the applicability of predefined heuristics like commit chronology. However, these approaches are ineffective when such assumptions do not hold, which are often the case in practice. To address these limitations, we propose SemBIC to identify the BIC of a bug by statically tracking the semantic changes in the execution path prescribed by the failing test across successive historical commit versions. Our insight is that the greater the semantic changes a commit introduces concerning the failing execution path of a target bug, the more likely it is to be the BIC. We evaluate the performance of SemBIC on a benchmark containing 199 real-world bugs from 12 open-source projects. We found that SemBIC can identify BICs with high accuracy – it ranks the BIC as top 1 for 80 out of 199 bugs, and achieves an MRR of 0.494, outperforming the state-of-the-art technique by 17.6% and 8.1%, respectively.

## 15. Towards Understanding Docker Build Faults in Practice: Symptoms, Root Causes, and Fix Patterns

**Authors:** Yiwen Wu (National University of Defense Technology), Yang Zhang (National University of Defense Technology, China), Tao Wang (National University of Defense Technology), Bo Ding (National University of Defense Technology), Huaimin Wang

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715757

**中文总结:** 收集并分析 GitHub、Stack Overflow 与 Docker Forum 上 255 个 issue 与 219 帖，构建 Docker 构建故障的症状、根因与修复模式分类体系，并对比 Dockerfile 与 docker-compose 构建的分布差异。据此给出可操作启示并实现知识型辅助应用。

**Abstract:** Docker building is a critical component of containerization in modern software development, automating the process of packaging and converting sources into container images. It is not uncommon to find that Docker build faults (DBFs) occur frequently across Docker-based projects, inducing non-negligible costs in development activities. DBF resolution is a challenging problem and previous studies have demonstrated that developers spend non-trivial time in resolving encountered build faults. However, the characteristics of DBFs is still under-investigated, hindering practical solutions to build management in the Docker community. In this paper, to bridge this gap, we present a comprehensive study for understanding the real-world DBFs in practice. We collect and analyze a DBF dataset of 255 issues and 219 posts from GitHub, Stack Overflow, and Docker Forum. We investigate and construct characteristic taxonomies for the DBFs, including 15 symptoms, 23 root causes, and 35 fix patterns. Moreover, we study the fault distributions of symptoms and root causes, in terms of the different build types, i.e., Dockerfile builds and Docker-compose builds. Based on the results, we provide actionable implications and develop a knowledge-based application, which can potentially facilitate research and assist developers in improving the Docker build management.

## 16. Towards Understanding Performance Bugs in Popular Data Science Libraries

**Authors:** Haowen Yang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Zhengda Li (The Chinese University of Hong Kong, Shenzhen), Zhiqing Zhong (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Xiaoying Tang (hinese University of Hong Kong, Shenzhen), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729374

**中文总结:** 对七个流行数据科学库的 138 个性能缺陷进行实证研究，给出根因分类并发现超半数源于低效数据处理（尤其数据结构）。约 28% 可用简单策略修复；由根因导出测试规则并新发现 8 个性能缺陷（4 个已确认）。

**Abstract:** With the increasing demand for handling large-scale and complex data, data science (DS) applications often suffer from long execution time and rapid RAM exhaustion, which leads to many serious issues like unbearable delays and crashes in financial transactions. As popular DS libraries are frequently used in these applications, their performance bugs (PBs) are a major contributing factor to these issues, making it crucial to address them for improving overall application performance. However, PBs in popular DS libraries remain largely unexplored. To address this gap, we conducted a study of 138 PBs collected from seven popular DS libraries. Our study examined the impact of PBs and proposed a taxonomy for common root causes. We found over half of the PBs arise from inefficient data processing operations, especially within data structure. We also explored the effort required to locate their root causes and fix these bugs, along with the challenges involved. Notably, 28% of the PBs could be fixed using simple strategies (e.g. Conditions Optimizing), suggesting the potential for automated repair approaches. Our findings highlight the severity of PBs in core DS libraries and offer insights for developing high-performance libraries and detecting PBs. Furthermore, we derived test rules from our identified root causes, identifying eight PBs, of which four were confirmed, demonstrating the practical utility of our findings.

## 17. Understanding Debugging as Episodes: A Case Study on Performance Bugs in Configurable Software Systems

**Authors:** Max Weber (Leipzig University), Alina Mailach (Leipzig University), Sven Apel (Saarland University), Janet Siegmund (Chemnitz University of Technology), Raimund Dachselt (Technical University of Dresden), Norbert Siegmund (Leipzig University)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3717523

**中文总结:** 通过 SoftVR 观察 12 名专业开发者调试可配置系统中的性能缺陷，指出既有调试策略粒度过粗且相互交织。提出以目标为导向的五类 episode 编码框架，统一描述调试过程并指导有效策略教学与研究。

**Abstract:** Context: Debugging performance bugs in configurable software systems is a complex and time-consuming task that requires not only fixing a bug, but also understanding its root cause. While there is a vast body of literature on debugging strategies, there is no consensus on general debugging strategies. This makes it difficult to provide concrete guidance for developers, especially for debugging configuration-dependent performance bugs. Objective: The goal of our work is to alleviate this situation by providing an framework to describe debugging strategies in a more general, unifying way. Method: To this end, we conducted a user study with 12 professional developers who debugged a performance bug in a real-world configural system. To observe developers in an unobstructive way, we provided them with an immersive virtual reality tool, SoftVR, giving them a large degree of freedom to choose the preferred debugging strategies. Result: The results show that existing strategies are too coarse-grained and intermixed to identify successful approaches. In the subsequent qualitative analysis, we developed a coding framework to reason about debugging approaches. With this framework, we identified five goal-oriented episodes that developers employ, which they also confirmed in subsequent interviews. Impact: Our work provides guidance on a unified description of debugging strategies, allowing researchers a common base to study debugging and practitioners and teachers guidance on successful debugging strategies.
