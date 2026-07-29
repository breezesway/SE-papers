# ISSTA 2025 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/issta-2025/issta-2025-papers#event-overview

Count: 21

## 1. Adding Spatial Memory Safety to EDK II through Checked C (Experience Paper)

**Authors:** Sourag Cherupattamoolayil (Purdue University), Arunkumar Bhattar (Purdue University), Connor Everett Glosner (Purdue University), Aravind Machiry (Purdue University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728929

**中文总结:** 本文首次报告将开源 UEFI 实现 EDK II 迁移至 Checked C 的实践经验，总结嵌入式系统在资源受限、缺乏标准 OS 支持条件下引入空间内存安全注解与运行时检查的主要挑战。作者还提出增强型自动化标注工具 e3c，使向 Checked C 的转换成功率提升 25%。

**Abstract:** Embedded software, predominantly written in C, is prone to memory corruption vulnerabilities due to spatial memory issues. Although various memory safety techniques exist, they are often unsuitable for embedded systems due to resource constraints and a lack of standardized OS support. Checked C, a backward-compatible, memory-safe C dialect, offers a potential solution by using pointer annotations for runtime checks to enhance spatial memory safety with minimal overhead. This paper provides the first experience report of porting EDK2 (an open-source UEFI implementation), an exemplary embedded codebase to Checked C, highlighting challenges and providing insights into applying Checked C to similar embedded systems. We also provide an enhanced automated annotation tool e3c, which improves the conversion rate by 25%, enabling easier conversion to Checked C.

## 2. BinDSA: Efficient, Precise Binary-Level Pointer Analysis with Context-Sensitive Heap Reconstruction

**Authors:** Lian Gao (University of California, Riverside), Heng Yin (University of California at Riverside)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728928

**中文总结:** 提出面向二进制的指针分析 BinDSA，在无符号与类型信息下采用域敏感、上下文敏感 unify 分析及上下文敏感堆重建，联合恢复数据结构与 points-to 关系，以精度与效率优先于 soundness。比 SOTA 约快 5 倍且更精确，并成功用于 CVE 可达性分析与漏洞检测。

**Abstract:** Pointer analysis serves as a fundamental component in the realm of binary code reverse engineering. It can be leveraged to reconstruct a binary program’s call graph and can be further applied to various security analyses. However, the absence of symbols and type information within binary code presents formidable challenges to effective pointer analysis. Existing works often apply approximations when performing pointer analysis on binary. Nevertheless, these methods tend to be inefficient and produce numerous false positive targets. In this paper, we propose BinDSA, a novel model tailored for binary pointer analysis. BinDSA prioritizes precision and efficiency over soundness. It is field- and context-sensitive, employing unification-based techniques and reconstructing a context-sensitive heap. It jointly recovers data structure and points-to relations so that precision can be further improved. In evaluation, we demonstrate that BinDSA is 5 times more efficient and notably more precise than the current state-of-the-art technique without significantly sacrificing soundness. We also apply BinDSA on CVE reachability analysis and vulnerability detection, demonstrating its effective application to security tasks.

## 3. BinQuery: A Novel Framework for Natural Language-Based Binary Code Retrieval

**Authors:** Bolun Zhang (Institute of Information Engineering, Chinese Academy of Sciences. School of Cyber Security, University of Chinese Academy of Sciences, China), Zeyu Gao (Tsinghua University), Hao Wang (Tsinghua University), Yuxin Cui (Institute for Network Sciences and Cyberspace, Tsinghua University), Siliang Qin (Institute of Information Engineering, Chinese Academy of Sciences. School of Cyber Security, University of Chinese Academy of Sciences, China), Chao Zhang (Tsinghua University), Kai Chen (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Beibei Zhao (Institute of Information Engineering, Chinese Academy of Sciences. School of Cyber Security, University of Chinese Academy of Sciences, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728927

**中文总结:** 提出自然语言驱动的二进制函数检索框架 BinQuery，桥接二进制与自然语言语义鸿沟，实现细粒度对齐，并借助 LLM 优化查询与生成多样化描述。在 ViC 上 recall@1 提升 42.55%，在 Magma 上约 4 倍，优于现有 BFR 方法。

**Abstract:** Binary Function Retrieval (BFR) is crucial in reverse engineering for identifying specific functions in binary code, especially those associated with malicious behavior or vulnerabilities. Traditional BFR methods rely on heuristics, often lacking the efficiency and adaptability needed for large-scale or diverse binary analysis tasks. To address these challenges, we present BinQuery, a Natural Language-based BFR (NL-based BFR) framework that uses natural language queries to retrieve relevant binary functions with improved flexibility and precision. BinQuery introduces innovative techniques to bridge information gaps between binary code and natural language, achieves fine-grained alignment for enhanced retrieval accuracy, and leverages Large Language Models (LLMs) to refine queries and generate diverse descriptions. Tested on the ViC and Magma datasets, BinQuery surpasses current state-of-the-art methods, achieving a 42.55% increase in recall@1 on ViC and a 4x improvement on Magma. Our framework marks a significant advancement for NL-based BFR, enhancing the efficacy of binary analysis for both general reverse engineering and vulnerability discovery.

## 4. Bridge the Islands: Pointer Analysis for Microservice Systems

**Authors:** Teng Zhang (Nanjing University), Yufei Liang (Nanjing University), Ganlin Li (Nanjing University), Tian Tan (Nanjing University), Chang Xu (Nanjing University), Yue Li (Nanjing University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728896

**中文总结:** 提出首个面向微服务系统的指针分析 Micans，建模 RPC、消息通信、依赖注入与 Web 端点配置等跨服务值流，弥补单体分析无法连通“孤岛服务”的不足。在多个领域真实基准上显著优于 SOTA，可有效构建 call graph 并支撑污点分析等下游任务。

**Abstract:** Microservice architecture has revolutionized enterprise software, providing scalability and flexibility by decomposing applications into loosely coupled services. However, this paradigm shift introduces unique challenges for pointer analysis, a foundational static analysis crucial for supporting various client analyses. Existing fundamental analyses, primarily designed for monolithic enterprise applications, fall short in handling complex service communications—such as remote procedure call and message-based communication—and essential programming paradigms, like dependency injection and web endpoint configuration. This paper introduces Micans, the first pointer analysis specifically crafted to address these challenges in microservice systems, capable of constructing comprehensive value flows across services. We extensively evaluated Micans on real-world benchmarks from multiple domains, focusing on its effectiveness in resolving service communications, constructing essential program information like call graphs, and supporting client analyses such as taint analysis. Micans consistently and significantly outperforms state-of-the-art approaches, demonstrating its capacity to handle complex cross-service communications and diverse programming paradigms. These results highlight Micans’ potential as a robust foundational analysis, advancing static analysis capabilities to meet the complexities of modern microservices.

## 5. Bridging the Gaps Between Graph Neural Networks and Data-Flow Analysis: The Closer, the Better

**Authors:** Qingchen Yu (Zhejiang University), Xin Liu (Lanzhou University), Qingguo Zhou (Lanzhou University), Chunming Wu (Zhejiang University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728906

**中文总结:** 基于 Neural Algorithmic Reasoning 的算法对齐思想，设计 DFA-GNN^-、DFA-GNN、DFA-GNN^+ 三档 GNN 逐步贴近经典数据流分析（DFA），解决位向量非干扰与外部信息分阶段处理等难点。对齐度更高的 DFA-GNN^+ 泛化与样本效率最佳，仅用输入输出对即可在 10 倍规模输入上接近轨迹监督训练的模型。

**Abstract:** Recent advances in applying deep neural networks to programming tasks have achieved remarkable success in practice, prompting interest in exploring how well these models can perform traditional program analysis techniques. Data-flow analysis (DFA), a classic and well-established approach for analyzing programs, presents an opportunity to assess the capabilities of neural networks in this domain. Given the structural similarities between DFA and Graph Neural Networks (GNNs), we explore the extent to which GNNs can effectively model the DFA algorithm. Building on the concept of algorithmic alignment from Neural Algorithmic Reasoning (NAR), we identify two key challenges: the noninterference property of the bit-vectors used in DFA and the complex handling of external information at different stages of the algorithm. Addressing these gaps, we propose three GNN architectures — $\text{DFA-GNN}^-$, DFA-GNN, and $\text{DFA-GNN}^{+}$ — that progressively align with the DFA algorithm. Our evaluations emphasize the generalization capacity of these models, particularly in scenarios where training occurs on smaller samples while testing on much larger inputs. Results demonstrate that GNNs with higher algorithmic alignment, such as $\text{DFA-GNN}^{+}$, exhibit superior generalization and sample efficiency, accurately scaling to 10 times larger inputs with minimal training data. Notably, we show that GNNs trained with only input-output pairs can perform competitively with models trained using full execution trajectory supervision, a common practice in recent NAR studies. This finding highlights the efficiency and robustness of GNNs in reasoning tasks when algorithmically aligned with the target algorithm.

## 6. Clause2Inv: A Generate-Combine-Check Framework for Loop Invariant Inference

**Authors:** Weining Cao (Nanjing University, China), Guangyuan Wu (Nanjing University, China), Tangzhi Xu (Nanjing University, China), Yuan Yao (Nanjing University), Hengfeng Wei (State Key Laboratory for Novel Software Technology, Nanjing University), Taolue Chen (Birkbeck, University of London), Xiaoxing Ma (Nanjing University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728920

**中文总结:** 提出 generate-combine-check 框架及 Clause2Inv：用 LLM 生成子句，再借反例驱动组合成完整循环不变式。在线性/非线性任务上分别比现有方法多解 93 与 16 题，并将 Code2Inv 从 210 题、137.6s 平均耗时提升至 252 题、17.8s。

**Abstract:** Loop invariant inference is a fundamental, yet challenging, problem in program verification. Recent work adopts the guess-and-check framework, where candidate loop invariants are iteratively generated in the guess step and verified in the check step. A major challenge of this general framework is to produce high-quality candidate invariants in each iteration so that the inference procedure can converge quickly. Empirically, we observe that existing approaches may struggle with guessing the complete invariant due to the complexity of logical connectives, but usually, all the clauses of the correct loop invariant have already appeared in the previous guesses. This motivates us to refine the guess-and-check framework, resulting in a generate-combine-check framework, where the loop invariant inference task is divided into clause generation and clause combination. Specifically, we propose a novel loop invariant inference approach Clause2Inv under the new framework, which consists of an LLM-based clause generator and a counterexample-driven clause combinator. As the clause generator, Clause2Inv leverages LLMs to generate a multitude of clauses; as the clause combinator, Clause2Inv leverages counterexamples from the previous rounds to convert generated clauses into invariants. Our experiments show that Clause2Inv significantly outperforms existing loop invariant inference approaches. For example, Clause2Inv solved 312 (out of 316) linear invariant generation tasks and 44 (out of 50) nonlinear invariant generation tasks, which is at least 93 and 16 more than the existing baselines, respectively. By design, the generate-combine-check framework is flexible to accommodate various existing approaches which are currently under the guess-and-check framework by splitting the guessed candidate invariants into clauses. The evaluation shows that our approach can, with minor adaptation,  improve existing loop invariant inference approaches in both effectiveness and efficiency. For example, Code2Inv which solved 210 problems with an average solving time of 137.6 seconds can be improved to solve 252 problems with an average solving time of 17.8 seconds.

## 7. DataHook: An Efficient and Lightweight System Call Hooking Technique without Instruction Modification

**Authors:** Quan Hong (Institute of Information Engineering, Chinese Academy of Sciences & School of Cyber Security, University of Chinese Academy of Sciences), Jiaqi Li (Institute of Information Engineering, Chinese Academy of Sciences), Wen Zhang (China Unicom Online Information Technology CO.,Ltd), Lidong Zhai (Institute of Information Engineering, Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728874

**中文总结:** DataHook 针对 32 位程序利用系统调用间接跳转的数据依赖做 hook，仅改数据不改指令，避免二进制重写带来的多线程冲突。相较现有技术 hook 开销降低 5.4–1429 倍；用于用户态网络栈时服务器性能约提升 4.3 倍，Redis 上性能损失仅 4%。

**Abstract:** System calls serve as the primary interface for interaction between user-space programs and the operating system (OS) kernel. By hooking system calls, it is possible to analyze and modify the behavior of user-space programs. This paper proposes DataHook, an efficient and lightweight system call hooking technique for 32-bit programs. Compared to existing system call hooking techniques, DataHook achieves hooking with extremely low hook overhead by modifying only a few data elements without altering any program instructions. This unique characteristic not only avoids the multithreading conflicts associated with binary rewriting but also provides support for programs to apply more efficient user-space OS subsystems. However, existing system call hooking techniques struggle to meet these goals simultaneously. While techniques like syscall user dispatch (SUD) and \texttt{ptrace} do not require rewriting process instructions, they introduce significant hook overhead. On the other hand, low-overhead techniques typically involve binary rewriting of multiple bytes or instructions, which introduces its own set of challenges. DataHook cleverly addresses these issues by leveraging the specific behavior of 32-bit programs during system calls. In short, unlike 64-bit programs, 32-bit programs use an indirect call instruction to jump to the function executing the \texttt{syscall}/\texttt{sysenter} when making a system call. This paper achieves system call hooking by manipulating the data dependencies involved in the indirect call process. This characteristic is present in 32-bit programs on glibc-based Linux systems, whether running on x86 or x86-64 architectures. Therefore, DataHook can be deployed on these systems. Experimental results demonstrate that DataHook reduces hook overhead by $5.4$ to $1,429.0$ times compared to existing techniques. When DataHook was applied to a server program to make it use the user-space network stack, the server performance was improved by approximately $4.3$ times. Additionally, when applied to Redis, DataHook resulted in only a $4.0$% performance loss, compared to $8.0$% to $94.7$% with other techniques.

## 8. DecLLM: LLM-Augmented Recompilable Decompilation for Enabling Programmatic Use of Decompiled Code

**Authors:** Wai Kin Wong (Hong Kong University of Science and Technology), Daoyuan Wu (Hong Kong University of Science and Technology), Huaijin Wang (Ohio State University), Li Zongjie (Hong Kong University of Science and Technology), Zhibo Liu (Hong Kong University of Science and Technology), Shuai Wang (Hong Kong University of Science and Technology), Qiyi Tang (Tencent Security Keen Lab), Sen Nie (Tencent Security Keen Lab), Shi Wu (Tencent Security Keen Lab)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728958

**中文总结:** DecLLM 以静态重编译与动态运行反馈为 oracle，迭代修复 IDA/Ghidra 等反编译输出使其可重新编译，便于 CodeQL 等程序化分析。GPT-3.5/4 在 C 基准与真实二进制上可将约 70% 原本不可编译样本修复成功，且语义与源码分析结果一致。

**Abstract:** Decompilers are widely used in reverse engineering (RE) to convert compiled executables into human-readable pseudocode and support various security analysis tasks. Existing decompilers, such as IDA Pro and Ghidra, focus on enhancing the readability of decompiled code rather than its recompilability, which limits further programmatic use, such as for CodeQL-based vulnerability analysis that requires compilable versions of the decompiled code. Recent LLM-based approaches for enhancing decompilation results, while useful for human RE analysts, unfortunately also follow the same path.

In this paper, we explore, for the first time, how off-the-shelf large language models (LLMs) can be used to enable recompilable decompilation—automatically correcting decompiler outputs into compilable versions. We first show that this is non-trivial through a pilot study examining existing rule-based and LLM-based approaches. Based on the lessons learned, we design DecLLM, an iterative LLM-based repair loop that utilizes both static recompilation and dynamic runtime feedback as oracles to iteratively fix decompiler outputs. We test DecLLM on popular C benchmarks and real-world binaries using two mainstream LLMs, GPT-3.5 and GPT-4, and show that off-the-shelf LLMs can achieve an upper bound of around 70% recompilation success rate, i.e., 70 out of 100 originally non-recompilable decompiler outputs are now recompilable. We also demonstrate the semantic consistency of using this recompilable code for CodeQL-based vulnerability analysis compared to the ground-truth source code. For the remaining 30% of hard cases, we further delve into their errors to gain insights for future improvements in decompilation-oriented LLM design.

## 9. Doctor: Optimizing Container Rebuild Efficiency by Instruction Re-Orchestration

**Authors:** Zhiling Zhu (Zhejiang University of Technology), Tieming Chen (Zhejiang University of Technology), Chengwei Liu (Nanyang Technological University), Han Liu (The Hong Kong University of Science and Technology), Qijie Song (Zhejiang University of Technology), Zhengzi Xu (Nanyang Technological University; Imperial Global Singapore), Yang Liu (Nanyang Technological University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728870

**中文总结:** Doctor 基于 Dockerfile 依赖分类与历史修改频率，用加权拓扑排序重排指令以降低后续重建成本并保持行为等价。千个 GitHub 仓库实验中 88.66% Dockerfile 受益，平均重建时间降 24.5%，14.39% 文件降幅超 50%。

**Abstract:** Containerization has revolutionized software deployment, with Docker leading the way due to its ease of use and consistent runtime environment. As Docker usage grows, optimizing Dockerfile performance, particularly by reducing rebuild time, has become essential for maintaining efficient CI/CD pipelines. However, existing optimization approaches primarily address single builds without considering the recurring rebuild costs associated with modifications and evolution, limiting long-term efficiency gains. To bridge this gap, we present Doctor, a method for improving Dockerfile build efficiency through instruction re-ordering that addresses key challenges: identifying instruction dependencies, predicting future modifications, ensuring behavioral equivalence, and managing the optimization’s computational complexity. We developed a comprehensive dependency taxonomy based on Dockerfile syntax and a historical modification analysis to prioritize frequently modified instructions. Using a weighted topological sorting algorithm, Doctor optimizes instruction order to reduce future rebuild time while preserving functionality. Experimental results on 1,000 popular GitHub repositories demonstrate that Doctor improves 88.66% of Dockerfiles, achieving an average 24.5% reduction in rebuild time, with 14.39% of files experiencing over 50% reduction, all while preserving functional equivalence in 86.2% of cases. These findings highlight best practices for Dockerfile management, enabling developers to enhance Docker efficiency through informed optimization strategies.

## 10. Finding 709 Defects in 258 Projects: An Experience Report on Applying CodeQL to Open-Source Embedded Software (Experience Paper)

**Authors:** Mingjie Shen (Purdue University), Akul Abhilash Pillai (Purdue University), Brian A. Yuan (Purdue University), James C. Davis (Purdue University), Aravind Machiry (Purdue University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728923

**中文总结:** 对 258 个热门 EMBOSS 项目的经验研究表明，仅 3% 使用高级 SAST；作者用 CodeQL 扫描后报告 709 个真实缺陷（误报率 34%），其中 376 个已获确认并合入 PR，还促成 2 个 CVE 与 37 个 CI 工作流合并。

**Abstract:** Embedded software is deployed in billions of devices worldwide, including in safety-sensitive systems like medical devices and autonomous vehicles. Defects in embedded software can have severe consequences. Many embedded software products incorporate Open-Source Embedded Software (EMBOSS), so it is important for EMBOSS engineers to use appropriate mechanisms to avoid defects. One of the common security practices is to use Static Application Security Testing (SAST) tools, which help identify commonly occurring vulnerabilities. Existing research related to SAST tools focuses mainly on regular (or non-embedded) software. There is a lack of knowledge about the use of SAST tools in embedded software. Furthermore, embedded software greatly differs from regular software in terms of semantics, software organization, coding practices, and build setup. All of these factors influence SAST tools and could potentially affect their usage.

In this experience paper, we report on a large-scale empirical study of Static Application Security Testing (SAST) in EMBOSS repositories. We collected a corpus of 258 of the most popular EMBOSS projects, and then measured their use of SAST tools via program analysis and a survey (N=25) of their developers. Advanced SAST tools are rarely used – only 3% of projects go beyond trivial compiler analyses. Developers cited the perception of ineffectiveness and false positives as reasons for limited adoption. Motivated by this deficit, we applied the state-of-the-practice CodeQL SAST tool and measured its ease of use and actual effectiveness. Across the 258 projects, CodeQL reported 709 true defects with a false positive rate of 34%. There were 535 (75%) likely security vulnerabilities, including in major projects maintained by Microsoft, Amazon, and the Apache Foundation. EMBOSS engineers have confirmed 376 (53%) of these defects, mainly by accepting our pull requests. Two CVEs were issued. Based on these results, we proposed pull requests to include our Workflows as part of EMBOSS Continuous Integration (CI) pipeline, 37 (71% of active repos) of these are already merged. In summary, we urge EMBOSS engineers to adopt the current generation of SAST tools, which offer low false positive rates and are effective at finding security-relevant defects.

## 11. Freesia: Verifying Correctness of TEE Communication with Concurrent Separation Logic

**Authors:** Fanlang Zeng (Zhejiang University), Rui Chang (Zhejiang University), Hongjian Liu (Zhejiang University, Hangzhou, China)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728967

**中文总结:** Freesia 针对 GlobalPlatform TEE 通信接口的并发数据竞争与共享内存一致性问题，基于并发分离逻辑形式化建模并在 Iris 中验证，原型已集成到 OP-TEE。案例研究与性能评估表明其能有效保障 TEE 并发正确性。

**Abstract:** The Trusted Execution Environment (TEE), a security extension in modern processors, provides a secure runtime environment for sensitive code and data. Although TEEs are designed to protect applications and their private data, their large code bases often harbor vulnerabilities that could compromise data security. Even though some formal verification efforts have been directed toward the functionality and security of TEE standards and implementations, the verification of TEE correctness in concurrent scenarios remains insufficient. This paper introduces an enhancement for ensuring concurrency safety in TEEs, named Freesia, which is formally verified using concurrent separation logic. Through a thorough analysis of the GlobalPlatform TEE standards, Freesia addresses data race issues in the TEE communication interfaces and ensures consistency protection for shared memory between the client and the TEE. A prototype of Freesia is implemented in the open-source TEE platform, OP-TEE. Additionally, the concurrency correctness of Freesia is modeled and verified using the Iris concurrent separation logic framework. The effectiveness and efficiency of Freesia are further demonstrated through real-world case study and performance evaluations.

## 12. Identifying Multi-Parameter Constraint Errors in Python Data Science Library API Documentations

**Authors:** Xiufeng Xu (Nanyang Technological University), Fuman Xie (University of Queensland), Chenguang Zhu (Meta AI), Guangdong Bai (University of Queensland), Sarfraz Khurshid (University of Texas at Austin), Yi Li (Nanyang Technological University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728945

**中文总结:** MPChecker 用符号执行从代码提取多参数约束，用 LLM 从文档抽取对应约束，再以模糊约束逻辑比对二者不一致。在四个流行数据科学库数据集上精确率 92.8%，已向开发者报告 14 个问题且 11 个已获确认。

**Abstract:** Modern AI- and Data-intensive software systems rely heavily on data science and machine learning libraries that provide essential algorithmic implementations and computational frameworks. These libraries expose complex APIs whose correct usage has to follow constraints among multiple interdependent parameters. Developers using these APIs are expected to learn about the constraints through the provided documentations and any discrepancy may lead to unexpected behaviors. However, maintaining correct and consistent multi-parameter constraints in API documentations remains a significant challenge for API compatibility and reliability. To address this challenge, we propose MPChecker, for detecting inconsistencies between code and documentation, specifically focusing on multi-parameter constraints. MPChecker identifies these constraints at the code level by exploring execution paths through symbolic execution and further extracts corresponding constraints from documentation using large language models (LLMs). We propose a customized fuzzy constraint logic to reconcile the unpredictability of LLM outputs and detects logical inconsistencies between the code and documentation constraints. We collected and constructed two datasets from four popular data science libraries and evaluated MPChecker on them. The results demonstrate that MPChecker can effectively detect inconsistency issues with the precision of 92.8%. We further report 14 detected inconsistency issues to the library developers, who have confirmed 11 issues at the time of writing.

## 13. Incremental Verification of Concurrent Programs through Refinement Constraint Adaptation

**Authors:** Liangze Yin (National University of Defense Technology), Yiwei Li, Kun Chen (National University of Defense Technology), Wei Dong (National University of Defense Technology), Ji Wang (National University of Defense Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728976

**中文总结:** 针对基于调度约束的抽象精化验证，论文提出按程序修改自适应复用历史 refinement constraints 的增量方法，支持各类变更。SV-COMP 2024 基准显示多数旧约束可迁移，复杂程序相对从头验证可快一个数量级。

**Abstract:** Programs evolve continuously throughout their life cycles. Verifying each version from scratch is usually impractical, especially for concurrent programs. Designing efficient incremental verification techniques for concurrent programs is highly desired. We focus on the abstraction refinement technique for concurrent program verification. When a program is modified, those refinement constraints generated in those verifications of former versions are adapted to the new program to avoid redundant analysis. We propose a kernel source based refinement constraint adaptation approach for the scheduling constraint based abstraction refinement method, one of the most efficient abstraction refinement methods for concurrent program verification. Our method  supports all kinds of program modifications, and generates adapted refinement constraints according to the modifications. Evaluation on the benchmarks from SV-COMP 2024 show promising results of our method. Most of the refinement constraints generated in the verification of previous versions can be adapted to the modified program in our experiments. Compared with verifying the modified program from scratch, our incremental verification method can achieve an order of magnitude speedup for those complex programs.

## 14. LogBase: A Large-Scale Benchmark for Semantic Log Parsing

**Authors:** Chenbo Zhang (Fudan University), Wenying Xu (Fudan University), Jinbu Liu (Alibaba), Lu Zhang (Fudan University), Guiyang Liu (Alibaba), Jihong Guan (Tongji University), Qi Zhou (Alibaba), Shuigeng Zhou (Fudan University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728969

**中文总结:** 面向下一代语义日志解析，作者构建首个大规模基准 LogBase，覆盖130个开源项目的85,300条语义标注模板，并设计 GenLog 框架，结合 GitHub 挖掘、CoT 与 LLM 生成及人工反馈自动化构数据集。基于 LogBase 对15种现有解析器系统评估，揭示其在复杂场景下的真实能力边界。

**Abstract:** Logs generated by large-scale software systems contain a huge amount of useful information. As the first step of automated log analysis, log parsing has been extensively studied. General log parsing techniques focus on identifying static templates from raw logs, but overlook the more important semantics implied in dynamic log parameters. With the popularity of Artificial Intelligence for IT Operations (AIOps),  traditional log parsing methods no longer meet the requirements of various downstream tasks. Researchers are now exploring the next generation of log parsing techniques, i.e., semantic log parsing, to identify both log templates and semantics in log parameters. However, the absence of semantic annotations in existing datasets hinders the training and evaluation of semantic log parsers, thereby stalling the progress of semantic log parsing.

To fill this gap and advance the field of semantic log parsing, we construct LogBase, the first semantic log parsing benchmark dataset. LogBase consists of logs from 130 popular open-source projects, containing 85,300 semantically annotated log templates, surpassing existing datasets in both log source diversity and template richness. To build Logbase, we develop the framework GenLog for constructing semantic log parsing datasets. GenLog mines log template-parameter-context triplets from popular open-source repositories on GitHub, and uses chain-of-thought (CoT) techniques with large language models (LLMs) to generate high-quality logs. Meanwhile, GenLog employs human feedback to improve the quality of the generated data and ensure its reliability. GenLog is highly automated and cost-effective, enabling researchers to easily and efficiently construct semantic log parsing datasets. Furthermore, we also design a set of comprehensive evaluation metrics for LogBase, including general log parser metrics and the metrics specifically for semantic log parsers and LLM-based parsers.

With LogBase, we extensively evaluate 15 existing log parsers, revealing their true performance in complex scenarios. We believe that this work provides researchers with valuable data, reliable tools, and insightful findings to support and guide the future research of semantic log parsing.

## 15. Model Checking Guided Incremental Testing for Distributed Systems

**Authors:** Yu Gao (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Dong Wang (Institute of software, Chinese academy of sciences), Wensheng Dou (Institute of Software Chinese Academy of Sciences), Wenhan Feng (Institute of Software, Chinese Academy of Sciences), Yu Liang (Institute of Software Chinese Academy of Sciences), Yuan Feng (Wuhan Dameng Database Co., Ltd), Jun Wei (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728883

**中文总结:** 针对分布式系统演化后模型检测引导测试（MCGT）需全量重跑的问题，提出增量方法 iMocket：提取形式规约与实现变更，仅对受影响抽象状态生成测试用例。在12个真实变更场景中，测试用例数量平均减少74.83%。

**Abstract:** Recently, model checking guided testing (MCGT) approaches have been proposed to systematically test distributed systems. MCGT automatically generates test cases by traversing the entire verified abstract state space derived from a distributed system’s formal specification, and it checks whether the target system behaves correctly during testing. Despite the effectiveness of MCGT, testing a distributed system with MCGT is often costly and can take weeks to complete. This inefficiency is exacerbated when distributed systems evolve, such as when new features are introduced or bugs are fixed. We must re-run the entire testing process for the evolved system to ensure its correctness, rendering MCGT not only resource-intensive but also inefficient. To reduce the overhead of model checking guided testing during distributed system evolution, we propose iMocket, a novel model checking guided incremental testing approach for distributed systems. We first extract the changes from both the formal specification and system implementation. We then identify the affected states within the abstract state space and generate incremental test cases that specifically target these states, thereby avoiding redundant testing of unaffected states. We evaluate iMocket using 12 real-world change scenarios drawn from three popular distributed systems. The experimental results demonstrate that iMocket can reduce the number of test cases by 74.83%, highlighting its effectiveness in lowering testing costs for distributed systems.

## 16. Program Analysis Combining Generalized Bit-Level and Word-Level Abstractions

**Authors:** Guangsheng Fan (National University of Defense Technology), Liqian Chen (National University of Defense Technology), Banghu Yin (College of Computer, National University of Defense Technology, Changsha, China), Wenyu Zhang (National University of Defense Technology), Peisen Yao (Zhejiang University), Ji Wang (National University of Defense Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728905

**中文总结:** 泛化 Linux eBPF 验证器的位级抽象为标准抽象域，并设计与有符号 word-level 域的 reduced product，以同时捕获机器整数语义下的位向量与边界信息。在 Crab 与 PREVAL 中实现，对 SV-COMP、eBPF 验证及硬件设计分析均展现有效性。

**Abstract:** Abstract interpretation is widely used to determine programs’ numerical properties. However, current abstract domains primarily focus on mathematical semantics, which do not fully capture the complexities of real-world programs relying on machine integer semantics and involving extensive bit-vector operations. This paper presents a solution that combines a bit-level abstraction and a word-level abstraction to capture machine integer semantics. First, we generalize the bit-level abstraction used in the Linux eBPF verifier for determining known and unknown bits of real-world programs, by supplementing all required operations as a standard abstract domain. Based on this abstraction, we design an abstract domain that is signedness-aware and simultaneously retains both the above bit-level and the world-level bound information. These two levels of information cooperate via a standard reduced product operation to improve analysis precision. We implement the proposed domains in the Crab analyzer and the out-of-kernel eBPF verifier PREVAL. Experiments demonstrate their effectiveness in analyzing SV-COMP benchmark programs, assisting hardware designs, and eBPF verification.

## 17. Safe4U: Identifying Unsound Safe Encapsulations of Unsafe Calls in Rust using LLMs

**Authors:** Huan Li (Zhejiang University, China), Bei Wang (Zhejiang University, China), Xing Hu (Zhejiang University), Xin Xia (Zhejiang University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728890

**中文总结:** 提出 Safe4U，结合静态分析、领域知识与 LLM 推理，识别 Rust 中不安全的 safe encapsulation of unsafe calls（EUC）。框架将 contract 细粒度分解后逐条验证；在 CVE 中识别 8/11 个 unsound EUC，并在高下载量 crate 中新发现 22 个（13 个已确认）。

**Abstract:** Rust is an emerging programming language that ensures safety through strict compile-time checks. A Rust function marked as unsafe indicates it has additional safety requirements (e.g., initialized, not null), known as contracts in the community. These unsafe functions can only be called within explicit unsafe blocks and the contracts must be guaranteed by the caller. To reuse and reduce unsafe code, the community recommends using safe encapsulation of unsafe calls (EUC) in practice. However, an EUC is unsound if any contract is not guaranteed and could lead to undefined behaviors in safe Rust, thus breaking Rust’s safety promise. It is challenging to identify unsound EUCs with conventional techniques due to the limitation in cross-lingual comprehension of code and natural language. Large language models (LLMs) have demonstrated impressive capabilities, but their performance is unsatisfactory owing to the complexity of contracts and the lack of domain knowledge. To this end, we propose a novel framework, Safe4U, which incorporates LLMs, static analysis tools, and domain knowledge to identify unsound EUCs. Safe4U first utilizes static analysis tools to retrieve relevant context. Then, it decomposes the primitive contract description into several fine-grained classified contracts. Ultimately, Safe4U introduces domain knowledge and invokes the reasoning capability of LLMs to verify every fine-grained contract. The evaluation results show that Safe4U brings a general performance improvement and the fine-grained results are constructive for locating specific unsound sources. In real-world scenarios, Safe4U can identify 8 out of 11 unsound EUCs from CVE. Furthermore, Safe4U detected 22 new unsound EUCs in the most downloaded crates, 13 of which have been confirmed.

## 18. Static Program Reduction via Type-Directed Slicing

**Authors:** Loi Ngo Duc Nguyen (University of California, Riverside), Tahiatul Islam (New Jersey Institute of Technology), Theron Wang (The Academy for Mathematics, Science & Engineering, USA), Sam Lenz (New Jersey Institute of Technology), Martin Kellogg (New Jersey Institute of Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728968

**中文总结:** 提出 type-directed slicing：静态保留特定位置上的类型检查语义（而非运行时语义），无需反复运行 typechecker 即可缩减大型程序。Java 原型在三个主流 typechecker 的 28 个历史 bug 中 89% 成功保留误报行为，百万行级基准可在 CI 免费 runner 上一分钟内完成。

**Abstract:** A traditional program slicer constructs a smaller variant of a target program that computes the same result with respect to some target variable—that is, program slicing preserves the original program’s \emph{run-time semantics}. We propose \emph{type-directed slicing}, which constructs a smaller program that guarantees that a typechecker will produce the same result on the sliced program when considering only a target program location—that is, a type-directed slicer preserves the target program’s \emph{compile-time semantics}, from the view of a specific typechecker, with respect to some location.

Type-directed slicing is a useful debugging aid for designers and maintainers of typecheckers. When a typechecker produces an unexpected result (a crash, a false positive warning, a missed warning, etc.) on a large codebase, the user typically reports a bug to the maintainers of the typechecker without an accompanying test case showing the analysis’ misbehavior in isolation. State-of-the-art approaches to this \emph{program reduction problem} are dynamic: they require repeatedly running the typechecker on the full program. A type-directed slicer solves this problem statically, without rerunning the typechecker, by exploiting the modularity inherent in a typechecker’s type rules. Our prototype type-directed slicer for Java is fully-automatic, can operate on incomplete programs, and is fast. It automatically produces a small test case that preserves typechecker misbehavior for 25 of 28 (89%) historical bugs from the issue trackers of three widely-used typecheckers: the Java compiler itself, NullAway, and the Checker Framework; in each of these 25 cases, it preserved the typechecker’s behavior even without the classpath of the target program. And, it runs in under a minute on each benchmark, whose size ranges up to millions of lines of code, on a free-tier CI runner.

## 19. Tracezip: Efficient Distributed Tracing via Trace Compression

**Authors:** Zhuangbin Chen (Sun Yat-sen University), Junsong Pu (Beijing University of Posts and Telecommunication), Zibin Zheng (Sun Yat-sen University)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728888

**中文总结:** Tracezip 通过 trace 压缩提升分布式追踪效率，在服务侧用 Span Retrieval Tree（SRT）消除 span 间冗余并轻量化传输，后端可无损重建完整 trace。已在 OpenTelemetry Collector 中实现，在微服务基准与生产 trace 上显著降低采集开销且几乎无额外成本。

**Abstract:** Distributed tracing serves as a fundamental building block in the monitoring and testing of cloud service systems. To reduce computational and storage overheads, the \textit{de facto} practice is to capture fewer traces via sampling. However, existing work faces a trade-off between the completeness of tracing and system overhead. On one hand, \textit{head-based sampling} indiscriminately selects requests to trace when they enter the system, which may miss critical events. On the other hand, \textit{tail-based sampling} traces all requests and selectively persist the edge-case traces, which entails the overheads related to trace collection and ingestion. Taking a different path, in this paper we propose Tracezip to enhance the efficiency of distributed tracing via \textit{trace compression}. Our key insight is that there exists significant redundancy among traces, which results in repetitive transmission of identical data between the services and backend. We design a new data structure named Span Retrieval Tree (SRT) to continuously encapsulates such redundancy at the service side and transforms trace spans into a lightweight form. At the backend, the full traces can be seamlessly reconstructed by retrieving the common data already delivered by previous spans. Tracezip includes a series of strategies to optimize the structure of SRT and a differential update mechanism to efficiently synchronize SRT between services and backend. Our evaluation on microservices benchmarks, popular cloud service systems, and production trace data demonstrate that Tracezip can achieve substantial performance gains in trace collection, with negligible overhead. We have implemented Tracezip inside OpenTelemetry Collector, making it compatible with existing tracing APIs.

## 20. Type-Alias Analysis: Enabling LLVM IR with Accurate Types

**Authors:** Jinmeng Zhou (Zhejiang University), Ziyue Pan (Zhejiang University), Wenbo Shen (Zhejiang University), Xingkai Wang (Zhejiang University), Kangjie Lu (University of Minnesota), Zhiyun Qian (University of California at Riverside, USA)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728974

**中文总结:** 针对 LLVM IR 单类型设计与 opaque pointer 导致类型信息丢失的问题，提出 type-alias analysis 并为 IR 变量维护类型别名集。原型工具 TypeCopilot 在 C 编译产物上达 98.57% 准确率与 94.98% 覆盖率，使既有类型分析在 opaque pointer 环境下仍可用。

**Abstract:** LLVM IR is a critical component of the LLVM compiler infrastructure. Its Static Single Assignment (SSA) form and strong type system make it ideal for program analysis. However, LLVM IR features a single-type design, where each IR variable is tagged with a single type. In some cases, an IR variable can correspond to multiple types. Such a single-type design cannot represent multiple types. Even worse, after the introduction of a new feature (opaque pointer), obtaining the pointers’ pointee types is no longer feasible. All pointers correspond to a single generic type, i.e., opaque pointer type (ptr), which renders type-based analyses ineffective. To address the limitations of single-type design, we propose type-alias analysis. This approach features a multiple-type design, maintaining type-alias sets for IR variables and performing type inference across various IR instructions. We implement a prototype, TypeCopilot, to specify types of generic pointers in the opaque-pointer-enabled LLVM IR compiled from C source code. Our results demonstrate that TypeCopilot achieves an overall accuracy of 98.57% and coverage of 94.98%. Additionally, TypeCopilot allows existing tools to continue their effectiveness in the presence of opaque pointers. To support the security community, we open-source TypeCopilot, providing a practical tool for enhancing type-based security analyses.

## 21. Wemby’s Web: Hunting for Memory Corruption in WebAssembly

**Authors:** Oussama Draissi (University of Duisburg-Essen), Tobias Cloosters (University of Duisburg-Essen), David Klein (TU Braunschweig), Michael Rodler (Amazon Web Services), Marius Musch (TU Braunschweig), Martin Johns (TU Braunschweig), Lucas Davi (University of Duisburg-Essen)

**Categories:** Program Analysis and Verification

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728937

**中文总结:** 大规模分析 37,797 个域名发现 77.81% 网站隐式信任可能受攻击者控制的 WebAssembly 内存数据，内存破坏可经 eval/innerHTML 等路径触发 XSS。Wemby 通过二进制级 WASM 插桩与 fuzzing  holistic 检测远程内存错误，平均比 SOTA fuzzer 快 232 倍、覆盖率多 46%，并在 Zoom 等平台发现关键漏洞。

**Abstract:** WebAssembly enables fast execution of performance-critical in web applications utilizing native code. However, recent research has demonstrated the potential for memory corruption errors within WebAssembly modules to exploit web applications. In this work, we present the first systematic analysis of memory corruption in WebAssembly, unveiling the prevalence of a novel threat model where memory corruption enables code injection on a victim’s browser. Our large-scale analysis across 37 797 domains reveals that an alarming 29 411 (77.81 %) of those fully trust data coming from potentially attacker-controlled sources. As a result, an attacker can exploit memory errors to manipulate the WebAssembly memory, where the data is implicitly trusted and frequently passed into security-sensitive functions such as eval or directly into the DOM via innerHTML. Thus, an attacker can abuse this trust to gain JavaScript code execution, i.e., Cross-Site Scripting (XSS).

To tackle this issue, we present Wemby, the first viable approach to efficiently analyze WebAssembly-powered websites holistically. We demonstrate that Wemby is proficient at detecting remotely exposed memory corruption errors in web applications through fuzzing. For this purpose, we implement binary-only WebAssembly instrumentation that provides fine-grained memory corruption oracles. We applied Wemby to different websites, uncovering several security-critical functions and memory corruption bugs, including one on the Zoom platform. In terms of performance, our ablation study demonstrates that Wemby outperforms cuurent WebAssembly fuzzers. Specifically, Wemby achieves an average speed improvement of 232 times and delivers 46% greater code coverage compared to the state-of-the-art.
