# ISSTA 2025 Research Track — Awarded Papers

Source: https://www2.sigsoft.org/awards/distinguishedpaper/ (ACM SIGSOFT Distinguished Paper Award list; Program page had no award badges)

## Award breakdown

| Award | # Papers |
| --- | ---: |
| ACM SIGSOFT Distinguished Paper Award | 9 |

Total awarded papers: 9

## 1. Assessing Scene Generation Techniques for Testing COLREGS-Compliance of Autonomous Surface Vehicles

**Authors:** Dominik Frey (Linköping University), Ulf Kargén (Linköping University), Daniel Varro (Linköping University / McGill University)

**Categories:** Systems, Mobile, and Autonomy

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728919

**中文总结:** 提出面向自主水面艇（ASV）COLREGS 合规测试的基于模型场景生成方法：多步细化从功能场景到逻辑几何约束，再用搜索算法生成精确初始船位。评估表明可在数分钟内为含六船的高风险相遇生成多样化初始场景。

**Abstract:** Autonomous surface vehicles (ASVs) need to complete missions without posing risks to other maritime traffic. Safe traffic is controlled by the International Regulations for Preventing Collisions at Sea (COLREGS) formulated by the International Maritime Organization (IMO). Being designed with human operators in mind, the COLREGS are intentionally underspecified, which may result in ambiguous requirements for correct behaviour for ASVs. Hence the systematic testing of such ambiguous situations is particularly important. This paper presents a model-based test generation approach for automatically deriving initial scenes of complex sea encounters involving multiple vessels by a multi-step refinement approach. First, a diverse set of functional scenarios are derived automatically. Then, we provide a mapping from functional scenarios to logical scenarios that capture geometrical constraints between potentially unsafe ship encounters. Finally, initial scenes with precise vessel placements are generated from logical scenarios by search-based algorithms. Our extensive evaluation shows that our approach derives a diverse set of initial scenes with high risk levels within few minutes, even for six vessel encounters.

## 2. BinDSA: Efficient, Precise Binary-Level Pointer Analysis with Context-Sensitive Heap Reconstruction

**Authors:** Lian Gao (University of California, Riverside), Heng Yin (University of California at Riverside)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728928

**中文总结:** 提出面向二进制的指针分析 BinDSA，在无符号与类型信息下采用域敏感、上下文敏感 unify 分析及上下文敏感堆重建，联合恢复数据结构与 points-to 关系，以精度与效率优先于 soundness。比 SOTA 约快 5 倍且更精确，并成功用于 CVE 可达性分析与漏洞检测。

**Abstract:** Pointer analysis serves as a fundamental component in the realm of binary code reverse engineering. It can be leveraged to reconstruct a binary program’s call graph and can be further applied to various security analyses. However, the absence of symbols and type information within binary code presents formidable challenges to effective pointer analysis. Existing works often apply approximations when performing pointer analysis on binary. Nevertheless, these methods tend to be inefficient and produce numerous false positive targets. In this paper, we propose BinDSA, a novel model tailored for binary pointer analysis. BinDSA prioritizes precision and efficiency over soundness. It is field- and context-sensitive, employing unification-based techniques and reconstructing a context-sensitive heap. It jointly recovers data structure and points-to relations so that precision can be further improved. In evaluation, we demonstrate that BinDSA is 5 times more efficient and notably more precise than the current state-of-the-art technique without significantly sacrificing soundness. We also apply BinDSA on CVE reachability analysis and vulnerability detection, demonstrating its effective application to security tasks.

## 3. Bridging the Gaps Between Graph Neural Networks and Data-Flow Analysis: The Closer, the Better

**Authors:** Qingchen Yu (Zhejiang University), Xin Liu (Lanzhou University), Qingguo Zhou (Lanzhou University), Chunming Wu (Zhejiang University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728906

**中文总结:** 基于 Neural Algorithmic Reasoning 的算法对齐思想，设计 DFA-GNN^-、DFA-GNN、DFA-GNN^+ 三档 GNN 逐步贴近经典数据流分析（DFA），解决位向量非干扰与外部信息分阶段处理等难点。对齐度更高的 DFA-GNN^+ 泛化与样本效率最佳，仅用输入输出对即可在 10 倍规模输入上接近轨迹监督训练的模型。

**Abstract:** Recent advances in applying deep neural networks to programming tasks have achieved remarkable success in practice, prompting interest in exploring how well these models can perform traditional program analysis techniques. Data-flow analysis (DFA), a classic and well-established approach for analyzing programs, presents an opportunity to assess the capabilities of neural networks in this domain. Given the structural similarities between DFA and Graph Neural Networks (GNNs), we explore the extent to which GNNs can effectively model the DFA algorithm. Building on the concept of algorithmic alignment from Neural Algorithmic Reasoning (NAR), we identify two key challenges: the noninterference property of the bit-vectors used in DFA and the complex handling of external information at different stages of the algorithm. Addressing these gaps, we propose three GNN architectures — $\text{DFA-GNN}^-$, DFA-GNN, and $\text{DFA-GNN}^{+}$ — that progressively align with the DFA algorithm. Our evaluations emphasize the generalization capacity of these models, particularly in scenarios where training occurs on smaller samples while testing on much larger inputs. Results demonstrate that GNNs with higher algorithmic alignment, such as $\text{DFA-GNN}^{+}$, exhibit superior generalization and sample efficiency, accurately scaling to 10 times larger inputs with minimal training data. Notably, we show that GNNs trained with only input-output pairs can perform competitively with models trained using full execution trajectory supervision, a common practice in recent NAR studies. This finding highlights the efficiency and robustness of GNNs in reasoning tasks when algorithmically aligned with the target algorithm.

## 4. Hulk: Exploring Data-Sensitive Performance Anomalies in DBMSs via Data-Driven Analysis

**Authors:** Zhiyong Wu (Tsinghua University, China), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Mingzhe Wang (Tsinghua University), Yu Jiang (Tsinghua University)

**Categories:** Systems, Mobile, and Autonomy

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728973

**中文总结:** HULK 随数据集演化追踪 CBO 引发的数据敏感性能异常：先估计各数据规模的合理响应时间以定位性能 cliff，再对照期望计划判断是否偏离设计。在 MySQL 等 6 款 DBMS 上报 135 个异常（129 个确认为新 bug，含 14 个 CVE），其中 94 个为数据敏感性能缺陷。

**Abstract:** Performance is crucial for database management systems (DBMSs), and they are always designed to handle ever-changing workloads efficiently. However, the complexity of the cost-based optimizer (CBO) and its interactions can introduce implementation errors, leading to data-sensitive performance anomalies. These anomalies may cause significant performance degradation compared to the expected design under certain datasets. To diagnose performance issues, DBMS developers often rely on intuitions or compare execution times to a baseline DBMS. These approaches overlook the impact of datasets on performance. As a result, only a subset of performance issues is identified and resolved.

In this paper, we propose HULK to automatically explore these data-sensitive performance anomalies via data-driven analysis. The key idea is to identify performance anomalies as the dataset evolves. Specifically, HULK estimates a reasonable response time range for each data volume to pinpoint performance cliffs. Then performance cliffs are checked for deviations from expected performance by finding a reasonable plan that aligns with performance expectations. We evaluate HULK on six widely-used DBMSs, namely MySQL, MariaDB, Percona, TiDB, PostgreSQL, and Antdb. \tool{} reports 135 anomalies, with 129 have been confirmed as new bugs, including 14 CVEs. Among them, 94 are data-sensitive performance bugs.

## 5. LLM4SZZ: Enhancing SZZ Algorithm with Context-Enhanced Assessment on Large Language Models

**Authors:** Lingxiao Tang (Zhejiang University), Jiakun Liu (Singapore Management University), Zhongxin Liu (Zhejiang University), Xiaohu Yang (Zhejiang University), Lingfeng Bao (Zhejiang University)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728885

**中文总结:** LLM4SZZ 结合 rank-based 与 context-enhanced 两种 LLM 策略定位 bug-inducing commit，并利用 commit message 与补丁上下文弥补传统 SZZ 变体不足。三个数据集上 F1 提升 8.9%–16.4% 且 recall 未显著下降，还能发现基线漏检的 2.5%–7.8% 诱导提交。

**Abstract:** The SZZ algorithm is the dominant technique for identifying bug-inducing commits and serves as a foundation for many software engineering studies, such as bug prediction and static code analysis, thereby enhancing software quality and facilitating better maintenance practices. Researchers have proposed many variants to enhance the SZZ algorithm’s performance since its introduction. The majority of them rely on static techniques or heuristic assumptions, making them easy to implement, but their performance improvements are often limited. Recently, a deep learning-based SZZ algorithm has been introduced to enhance the original SZZ algorithm performance. However, it requires complex preprocessing and is restricted to a single programming language. Additionally, while it enhances precision, it sacrifices recall. Furthermore, most of variants overlook crucial information, such as commit messages and patch context, and are limited to bug-fixing commits involving deleted lines.

The emergence of large language models (LLMs) offers an opportunity to address these drawbacks. In this study, we investigate the strengths and limitations of LLMs and propose LLM4SZZ, which employs two approaches (i.e., rank-based identification and context-enhanced identification) to handle different types of bug-fixing commits. We determine which approach to adopt based on the LLM’s ability to comprehend the bug and identify whether the bug is present in a commit. The context-enhanced identification provides the LLM with more context and requires it to find the bug-inducing commit among a set of candidate commits. In rank-based identification, we ask the LLM to select buggy statements from the bug-fixing commit and rank them based on their relevance to the root cause.  Experimental results show that LLM4SZZ outperforms all baselines across three datasets, improving F1-score by 8.9% to 16.4% without significantly sacrificing recall. Additionally, LLM4SZZ can identify many bug-inducing commits that the baselines fail to detect, accounting for 7.8%, 7.4% and 2.5% of the total bug-inducing commits across three datasets, respectively.

## 6. Reinforcement Learning-based Fuzz Testing for the Gazebo Robotic Simulator

**Authors:** Zhilei Ren (Dalian University of Technology), Yitao Li (Dalian University of Technology), Xiaochen Li (Dalian University of Technology), Guanxiao Qi (Dalian University of Technology), Jifeng Xuan (Wuhan University), He Jiang (Dalian University of Technology)

**Categories:** Systems, Mobile, and Autonomy

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728942

**中文总结:** 提出首个面向 Gazebo 的模糊测试框架 GzFuzz：语法感知的可行命令生成应对严格输入结构，强化学习驱动的命令生成器选择高效探索状态空间。12 小时内平均发现 9.6 个独特 bug，代码覆盖率较 AFL++、Fuzzotron 提升约 234%–360%；半年内发现 25 个崩溃，19 个已修复或确认。

**Abstract:** Gazebo, being the most widely utilized simulator in robotics, plays a pivotal role in developing and testing robotic systems. Given its impact on the safety and reliability of robotic operations, early bug detection is critical. However, due to the challenges of strict input structures and vast state space, it is not effective to directly use existing fuzz testing approach to Gazebo. In this paper, we present GzFuzz, the first fuzz testing framework designed for Gazebo. GzFuzz addresses these challenges through a syntax-aware feasible command generation mechanism to handle strict input requirements, and a reinforcement learning-based command generator selection mechanism to efficiently explore the state space. By combining the two mechanisms under a unified framework, GzFuzz is able to detect bugs in Gazebo effectively. In extensive experiments, GzFuzz is able to detect an average of 9.6 unique bugs in 12 hours, and exhibits a substantial increase in code coverage than existing fuzzers AFL++ and Fuzzotron, with a proportionate improvement of approximately 234%-360%. In less than six months, GzFuzz uncovered 25 unique crashes in Gazebo, 19 of which have been fixed or confirmed. Our results highlight the importance of directly fuzzing Gazebo, thereby presenting a novel and potent methodology that serves as an inspiration for enhancing testing across a broader range of simulators.

## 7. RouthSearch: Inferring PID Parameter Specification for Flight Control Program by Coordinate Search

**Authors:** Siao Wang (Fudan University), Zhen Dong (Fudan University), Hui Li (Fudan University, China), Liwei Shen (Fudan University, China), Xin Peng (Fudan University), Dongdong She (HKUST (The Hong Kong University of Science and Technology))

**Categories:** Systems, Mobile, and Autonomy

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728904

**中文总结:** 针对 UAV 飞控程序中 PID 参数误配置导致的输入校验漏洞，提出 RouthSearch：先用 Routh-Hurwitz 稳定性判据确定理论边界，再用坐标搜索精化三维 PID 有效范围。在 PX4 与 ArduPilot 上有效范围推断准确率达 92%，48 小时内发现 3853 组误配置，较 PGFuzz 提升 8.58 倍，并确认 3 个程序缺陷。

**Abstract:** Flight control programs are widely used in unmanned aerial vehicles (UAVs) to manage and maintain UAVs’ flying behaviors dynamically. These flight control programs include a PID control module that takes three user-configurable PID parameters: Proportional (P), Integral (I), and Derivative (D). Users can also adjust these PID parameters during flight to suit the needs of various flight tasks. However, flight control programs do not have sufficient safety checks on the user-provided PID parameters, leading to a severe vulnerability of UAV—input validation bug. It happens when the user misconfigures PID parameters and causes the UAV to enter a dangerous state, such as deviation from the expected path, loss of control, or even crash.

Prior works use random testing approaches like fuzzing to identify invalid PID parameters from user input. However, they are not effective in the three-dimensional search space of PID parameters. Meanwhile, each dynamic execution of the UAV test is very expensive, further affecting the performance of random testing.

In this work, we address the problem of PID parameter misconfiguration by combining the Routh-Hurwitz stability criterion with coordinate search, introducing a method called RouthSearch. Instead of identifying misconfigured PID parameters in an ad-hoc fashion, RouthSearch principledly determines valid ranges for three-dimensional PID parameters. We first leverage the Routh-Hurwitz Criterion to identify a theoretical PID parameter boundary. We then refine the boundary using an efficient coordinate search. The valid range of three-dimensional PID parameters determined by RouthSearch can filter out misconfigured PID parameters from users during flight and further help to discover logical bugs in popular flight control programs.

We evaluated RouthSearch across eight flight modes in two popular flight control programs, PX4 and Ardupilot. The results show that RouthSearch can determine the valid ranges of the three-dimensional PID parameters with an accuracy of 92. 0% when compared to the ground truth. In terms of the total number of misconfigured PID parameters, RouthSearch discovers 3,853 sets of PID misconfigurations within 48 hours, while the STOA work PGFuzz only discovers 449 sets of PID misconfigurations, significantly outperforming prior works by 8.58 times. Additionally, our method helps to detect three bugs in ArduPilot and PX4.

## 8. SWE-GPT: A Process-Centric Language Model for Automated Software Improvement

**Authors:** Yingwei Ma (Alibaba Group), Rongyu Cao (Tongyi Lab, Alibaba, China), Yongchang Cao (Tongyi Lab, Alibaba, China), Yue Zhang (Tongyi Lab, Alibaba, China), Jue Chen (Tongyi Lab, Alibaba, China), Yibo Liu (Tongyi Lab, Alibaba, China), Yuchen Liu (Tongyi Lab, Alibaba, China), Binhua Li (Tongyi Lab, Alibaba, China), Fei Huang (Tongyi Lab, Alibaba, China), Yongbin Li (Tongyi Lab, Alibaba, China)

**Categories:** Evolution and Maintenance

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728981

**中文总结:** 发布开源软件改进专用模型 SWE-GPT（7B/72B），从真实代码提交活动中学习仓库理解、缺陷定位、补丁生成等动态流程。SWE-GPT 72B 在 SWE-bench Verified 上解决 30.20% 的 GitHub issue，相对 Llama 3.1 405B 提升 22.76%，接近 GPT-4o 的 31.80%。

**Abstract:** Large language models (LLMs) have demonstrated remarkable performance in code generation, significantly enhancing the coding efficiency of developers. Recent advancements in LLM-based agents have led to significant progress in end-to-end automatic software engineering (ASE), particularly in software maintenance (e.g., fixing software issues) and evolution (e.g., adding new features). Despite these encouraging advances, current research faces two major challenges. First, state-of-the-art performance primarily depends on closed-source models like GPT-4, which significantly limits the technology’s accessibility, and potential for customization in diverse software engineering tasks. This dependence also raises concerns about data privacy, particularly when handling sensitive codebases. Second, these models are predominantly trained on static code data, lacking a deep understanding of the dynamic interactions, iterative problem-solving processes, and evolutionary characteristics inherent in software development. Consequently, they may face challenges in navigating complex project structures and generating contextually relevant solutions, which can affect their practical utility in real-world scenarios.

To address these challenges, our study adopts a software engineering perspective. We recognize that real-world software maintenance and evolution processes encompass not only static code data but also developers’ thought processes, utilization of external tools, and the interaction between different functional personnel. Our objective is to develop an open-source large language model specifically optimized for software improvement, aiming to match the performance of closed-source alternatives while offering greater accessibility and customization potential. Consequently, we introduce the \textbf{SWE-GPT} series, comprising SWE-GPT 7B and SWE-GPT 72B. By learning from and simulating real-world code submission activities, SWE-GPT systematically incorporates the dynamic interactions and iterative problem-solving inherent in software development process—such as repository understanding, fault localization, and patch generation—thereby achieving a more comprehensive understanding of software improvement processes. We conducted experimental evaluations using SWE-bench Verified benchmark (comprising 500 real GitHub issues), recently proposed by OpenAI. The results demonstrate that \textbf{SWE-GPT 72B successfully resolves 30.20% of the GitHub issues}, marking a significant improvement in automatic issue resolution (22.76% relative improvement compared to Llama 3.1 405B), approaching the performance of closed-source models (31.80% issues of GPT-4o resolved). Notably, SWE-GPT 7B resolves 18.20% of the issues, surpassing the 17.20% resolution rate of Llama 3.1 70B, highlighting the potential for applying smaller models to ASE tasks.

## 9. Top Score on the Wrong Exam: On Benchmarking in Machine Learning for Vulnerability Detection

**Authors:** Niklas Risse (Max-Planck-Institute for Security and Privacy), Jing Liu (Max Planck Institute for Security and Privacy), Marcel Böhme (MPI for Security and Privacy)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728887

**中文总结:** 质疑主流 ML4VD 将漏洞检测建模为函数级二分类的合理性：分析表明多数样本缺乏足够上下文，所谓“漏洞函数”常依赖调用上下文才成立。高准确率可能来自词频等伪相关而非真实漏洞语义，呼吁重新定义问题与更严格的基准评估方法论。

**Abstract:** According to our survey of machine learning for vulnerability detection (ML4VD), 9 in every 10 papers published in the past five years define ML4VD as a function-level binary classification problem:

Given a function, does it contain a security flaw?

From our experience as security researchers, faced with deciding whether a given function makes the program vulnerable to attacks, we would often first want to understand the context in which this function is called.

In this paper, we study how often this decision can really be made without further context and study both vulnerable and non-vulnerable functions in the most popular ML4VD datasets. We call a function vulnerable if it was involved in a patch of an actual security flaw and confirmed to cause the program’s vulnerability. It is non-vulnerable otherwise. We find that in almost all cases this decision cannot be made without further context. Vulnerable functions are often vulnerable only because a corresponding vulnerability-inducing calling context exists while non-vulnerable functions would often be vulnerable if a corresponding context existed.

But why do ML4VD techniques achieve high accuracy even though there is demonstrably not enough information in these samples? Spurious correlations: We find that high accuracy can be achieved even when only word counts are available. This shows that these datasets can be exploited to achieve high accuracy without actually detecting any security vulnerabilities.

We conclude that the prevailing problem statement of ML4VD is ill-defined and call into question the internal validity of this growing body of work. Constructively, we call for more effective benchmarking methodologies to evaluate the true capabilities of ML4VD, propose alternative problem statements, and examine broader implications for the evaluation of machine learning and programming analysis research.
