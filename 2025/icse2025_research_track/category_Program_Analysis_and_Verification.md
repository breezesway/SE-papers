# ICSE 2025 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 64 papers

## 1. $ZTD_{JAVA}$: Mitigating Software Supply Chain Vulnerabilities via Zero-Trust Dependencies

**Authors:** Paschal Amusuo (Purdue University), Kyle A. Robinson (Purdue University), Tanmay Singla (Purdue University), Huiyun Peng (Mount Holyoke College), Aravind Machiry (Purdue University), Santiago Torres-Arias (Purdue University), Laurent Simon (Google), James C. Davis (Purdue University)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029801

**中文总结:** 提出零信任依赖 ZTD，将 NIST 零信任架构应用于 Java 第三方库运行时权限隔离，以较低开销缓解软件供应链攻击风险。

**Abstract:** Third-party libraries like Log4j accelerate software application development but introduce substantial risk. Vulnerabilities in these libraries have led to Software Supply Chain (SSC) attacks that compromised resources within the host system. These attacks benefit from current application permissions approaches: third-party libraries are implicitly trusted in the application runtime. An application runtime designed with Zero-Trust Architecture (ZTA) principles — secure access to resources, continuous monitoring, and least-privilege enforcement — could mitigate SSC attacks, as it would give zero implicit trust to these libraries. However, no individual security defense incorporates these principles at a low runtime cost. This paper proposes Zero-Trust Dependencies (ZTD) to mitigate SSC vulnerabilities: we apply the NIST ZTA to software applications. First, we assess the expected effectiveness and configuration cost of Zero-Trust Dependencies using a study of third-party software libraries and their vulnerabilities. Then, we present a system design, $ZTD_{sys}$, that enables the application of Zero-Trust Dependencies to software applications and a prototype, $ZTD_{JAVA}$, for Java applications. Finally, with evaluations on recreated vulnerabilities and realistic applications, we show that $ZTD_{JAVA}$ can defend against prevalent vulnerability classes, introduces negligible cost, and is easy to configure and use.

## 2. 3DGen: AI-Assisted Generation of Provably Correct Binary Format Parsers

**Authors:** Sarah Fakhoury (Microsoft Research), Markus Kuppe (Microsoft Research), Shuvendu K. Lahiri (Microsoft Research), Tahina Ramananandro (Microsoft Research), Nikhil Swamy (Microsoft Research)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029881

**中文总结:** 提出 3DGen 框架，用 AI 智能体将自然语言文档与示例输入转化为 3D 形式化格式规范，并结合符号测试生成与迭代 refinement 生成可证明正确的二进制解析器。

**Abstract:** Improper parsing of attacker-controlled input is a leading source of software security vulnerabilities, especially when programmers transcribe informal format descriptions into efficient parsing logic in low-level, memory unsafe languages. Several researchers have proposed formal specification languages for data formats from which efficient code can be extracted. However, distilling informal requirements into formal specifications is challenging and, despite their benefits, new, formal languages are hard for people to learn and use. In this work, we present 3DGen, a framework that makes use of AI agents to transform mixed informal input, including natural language documents and example inputs into format specifications in a language called 3D. To support humans in understanding and trusting the generated specifications, 3DGen uses symbolic methods to also synthesize test inputs that can be validated against an external oracle. Symbolic test generation also helps in distinguishing multiple plausible solutions. Through a process of repeated refinement, 3DGen produces a 3D specification that conforms to a test suite, and which yields safe, efficient, provably correct, parsing code in C. We have evaluated 3DGen on 20 Internet standard formats, demonstrating the potential for AI-agents to produce formally verified C code at a non-trivial scale. A key enabler is the use of a domain-specific language to limit AI outputs to a class for which automated, symbolic analysis is tractable.

## 3. A Multiple Representation Transformer with Optimized Abstract Syntax Tree for Efficient Code Clone Detection

**Authors:** TianChen Yu (School of Software Engineering, South China University of Technology), Li Yuan (School of Software Engineering, South China University of Technology, Guangzhou, China), Liannan Lin (School of Software Engineering, South China University of Technology), Hongkui He (School of Software Engineering, South China University of Technology)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029815

**中文总结:** 提出 MRT-OAST 代码克隆检测模型，剪枝优化 AST 并以前序/后序遍历双表示输入 Transformer，结合 Siamese 网络与余弦相似度加速比对；Java/C++ AST 序列长度分别降至 40%/39%。

**Abstract:** Over the past decade, the application of deep learning in code clone detection has produced remarkable results. However, the current approaches have two limitations: (a) code representation approaches with low information utilization, such as vanilla Abstract Syntax Tree (AST), leading to information redundancy which results in performance degradation; (b) low efficiency of clone detection on evaluation, resulting in excessive time costs during practical use. In this paper, we propose a Multiple Representation Transformer with Optimized Abstract Syntax Tree (MRT-OAST) to introduce an efficient code representation method while achieving competitive performance. Specifically, MRT-OAST strategically prunes and enhances the AST, utilizing both pre-order and post-order traversals to represent two different representations. To speed up the evaluation process, MRT-OAST utilizes a pure Siamese network and employs cosine similarity to compare the similarity between codes. Our approach effectively reduces AST sequences to 40% and 39% of their original length in Java and C/C++ while preserving structural information. In code clone detection tasks, our model surpasses state-of-the-art approaches on OJClone and Google Code Jam. During the evaluation of BigCloneBench, our model has a 5x speed improvement compared to the state-of-the-art lightweight model and a 563x speed improvement compared to the BERT-based model, with only a 0.3% and 0.9% decrease in $F_1$-score.

## 4. A Study of Undefined Behavior Across Foreign Function Boundaries in Rust Libraries

**Authors:** Ian McCormack (Carnegie Mellon University), Joshua Sunshine (Carnegie Mellon University), Jonathan Aldrich (Carnegie Mellon University)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029832

**中文总结:** 大规模评估 Rust 库跨 FFI 边界的未定义行为，联合 Miri 与 LLVM 解释器执行多语言应用，发现 48 例问题，含高下载量库与 Rust 官方维护库缺陷。

**Abstract:** Developers rely on the Rust programming language's static safety guarantees to write secure and performant applications. However, Rust is frequently used to interoperate with other languages which allow design patterns that conflict with Rust's aliasing models. Miri is the only dynamic analysis tool capable of validating applications against these models, but it does not support foreign functions, indicating that there may be a critical correctness gap at the heart of the Rust ecosystem. We conducted a large-scale evaluation of multi-language Rust libraries to determine whether Miri's dynamic analyses remain useful in this context. We used Miri and an LLVM interpreter to jointly execute multi-language applications, where we found 48 instances of undefined or undesired behavior. These include three bugs from libraries that had over 10,000 daily downloads on average during our observation period, and one from a library maintained by the Rust Project. Many of the errors we found involved incompatible aliasing patterns, but Rust's latest Tree Borrows aliasing model was significantly more permissive than the earlier Stacked Borrows model. The Rust community must invest in new, production-ready tooling for multi-language applications to ensure that developers can detect these errors.

## 5. A Test Oracle for Reinforcement Learning Software based on Lyapunov Stability Control Theory

**Authors:** Shiyu Zhang (The Hong Kong Polytechnic University), Haoyang Song (The Hong Kong Polytechnic University), Qixin Wang (The Hong Kong Polytechnic University), Henghua Shen (The Hong Kong Polytechnic University), Yu Pei (The Hong Kong Polytechnic University)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029785

**中文总结:** 基于 Lyapunov 稳定性控制理论为强化学习软件设计测试预言，替代依赖人工专家判断输出正确性的做法。

**Abstract:** Reinforcement Learning (RL) has gained significant attention in recent years. As RL software becomes more complex and infiltrates critical application domains, ensuring its quality and correctness becomes increasingly important. An indispensable aspect of software quality/correctness insurance is testing. However, testing RL software faces unique challenges compared to testing traditional software, due to the difficulty on defining the outputs’ correctness. This leads to the RL test oracle problem. Current approaches to testing RL software often rely on human oracles, i.e. convening human experts to judge the correctness of RL software outputs. This heavily depends on the availability and quality (including the experiences, subjective states, etc.) of the human experts, and cannot be fully automated. In this paper, we propose a novel approach to design test oracles for RL software by leveraging the Lyapunov stability control theory. By incorporating Lyapunov stability concepts to guide RL training, we hypothesize that a correctly implemented RL software shall output an agent that respects Lyapunov stability control theories. Based on this heuristics, we propose a Lyapunov stability control theory based oracle, LPEA(ϑ, θ), for testing RL software. We conduct extensive experiments over representative RL algorithms and RL software bugs to evaluate our proposed oracle. The results show that our proposed oracle can outperform the human oracle in most metrics. Particularly, LPEA(ϑ = 100%, θ = 75%) outperforms the human oracle by 53.6%, 50%, 18.4%, 34.8%, 18.4%, 127.8%, 60.5%, 38.9%, and 31.7% respectively on accuracy, precision, recall, F1 score, true positive rate, true negative rate, false positive rate, false negative rate, and ROC curve’s AUC; and LPEA(ϑ = 100%, θ = 50%) outperforms the human oracle by 48.2%, 47.4%, 10.5%, 29.1%, 10.5%, 127.8%, 60.5%, 22.2%, and 26.0% respectively on these metrics.

## 6. Accounting for Missing Events in Statistical Information Leakage Analysis

**Authors:** Seongmin Lee (Max Planck Institute for Security and Privacy (MPI-SP)), Shreyas Minocha (Georgia Tech), Marcel Böhme (MPI for Security and Privacy)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029817

**中文总结:** 针对统计信息泄露分析中样本覆盖不足导致泄露被严重低估的问题，提出改进估计器并借助应用统计学方法在低覆盖率下更准确估计联合分布。

**Abstract:** The leakage of secret information via a public channel is a critical privacy flaw in software systems. The more information is leaked per observation, the less time an attacker needs to learn the secret. Due to the size and complexity of the modern software, and because some empirical facts are not available to a formal analysis of the source code, researchers started investigating statistical methods using program executions as samples. However, current statistical methods require a high sample coverage. Ideally, the sample is large enough to contain every possible combination of secret $\times$ observable value to accurately reflect the joint distribution of $\langle$secret, observable$\rangle$. Otherwise, the information leakage is severely underestimated, which is problematic as it can lead to overconfidence in the security of an otherwise vulnerable program. In this paper, we introduce an improved estimator for information leakage and propose to use methods from applied statistics to improve our estimate of the joint distribution when sample coverage is low. The key idea is to reconstruct the joint distribution by casting our problem as a multinomial estimation problem in the absence of samples for all classes. We suggest two approaches and demonstrate the effectiveness of each approach on a set of benchmark subjects. We also propose novel refinement heuristics, which help to adjust the joint distribution and gain better estimation accuracy. Compared to existing statistical methods for information leakage estimation, our method can safely overestimate the mutual information and provide a more accurate estimate from a limited number of program executions.

## 7. Aligning the Objective of LLM-based Program Repair

**Authors:** Junjielong Xu (The Chinese University of Hong Kong, Shenzhen), Ying Fu (Chongqing University), Shin Hwei Tan (Concordia University), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029731

**中文总结:** 提出 D4C 提示框架，将 LLM 程序修复对齐下一词预测训练目标并允许全程序级修补，无需预定位缺陷语句。

**Abstract:** Large language models (LLMs) have achieved decent results on automated program repair (APR). However, the next token prediction training objective of decoder-only LLMs (e.g., GPT-4) is misaligned with the masked span prediction objective of current infilling-style methods, which impedes LLMs from fully leveraging pre-trained knowledge for program repair. In addition, while some LLMs can locate and repair bugs in certain functions using the related artifacts (e.g., test cases), existing methods still depend on statement-level fault localization methods to provide a list of buggy hunks for repair. This restriction hinders LLMs from exploring potential patches beyond the given locations. In this paper, we investigate a new approach to adapt LLMs to program repair. Our core insight is that LLM’s APR capability can be greatly improved by simply aligning the output to their training objective and allowing them to refine the whole program without first identifying faulty statements. Based on this insight, we designed D4C, a straightforward prompting framework for APR. D4C can repair 180 bugs correctly in Defects4J, with each patch being sampled only 10 times. This surpasses the SOTA APR methods with perfect fault localization by 10% and reduces the patch sampling number by 90%. Our findings reveal that (1) objective alignment is crucial for fully exploiting LLM’s pre-trained capability, and (2) replacing the traditional localize-buggy-hunks-then-repair workflow with direct debugging is more effective for LLM-based APR methods. Thus, we believe this paper introduces a new mindset for harnessing LLMs in APR.

## 8. An Empirical Study on Automatically Detecting AI-Generated Source Code: How Far Are We?

**Authors:** Hyunjae Suh (University of California, Irvine), Mahan Tafreshipour (University of California at Irvine), Jiawei Li (University of California Irvine), Adithya Bhattiprolu (University of California, Irvine), Iftekhar Ahmed (University of California at Irvine)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029804

**中文总结:** 实证显示现有 AI 生成代码检测工具泛化性差；提出改进方法最佳 F1 达 82.55，显著优于 GPTSniffer。

**Abstract:** Artificial Intelligence (AI) techniques, especially Large Language Models (LLMs), have started gaining popularity among researchers and software developers for generating source code. However, LLMs have been shown to generate code with quality issues and also incurred copyright/licensing infringements. Therefore, detecting whether a piece of source code is written by humans or AI has become necessary. This study first presents an empirical analysis to investigate the effectiveness of the existing AI detection tools in detecting AI-generated code. The results show that they all perform poorly and lack sufficient generalizability to be practically deployed. Then, to improve the performance of AI-generated code detection, we propose a range of approaches, including fine-tuning the LLMs and machine learning-based classification with static code metrics or code embedding generated from Abstract Syntax Tree (AST). Our best model outperforms state-of-the-art AI-generated code detector (GPTSniffer) and achieves an F1 score of 82.55. We also conduct an ablation study on our best-performing model to investigate the impact of different source code features on its performance.

## 9. An Extensive Empirical Study of Nondeterministic Behavior in Static Analysis Tools

**Authors:** Miao Miao (The University of Texas at Dallas), Austin Mordahl (University of Illinois Chicago), Dakota Soles (The University of Texas at Dallas), Alice Beideck (The University of Texas at Dallas), Shiyi Wei (University of Texas at Dallas)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029904

**中文总结:** 对 12 个主流开源静态分析工具开展非确定性行为大规模实证，定性发现并发、分析逻辑错误与无序结构假定顺序是主要根因，定量检测确认 8 个工具存在未知非确定性。

**Abstract:** Recent research has studied the importance and identified causes of nondeterminism in software. Static analysis tools exhibit many risk factors for nondeterministic behavior, but no work has analyzed the occurrence of such behavior in these tools. To bridge this gap, we perform an extensive empirical study aiming to understand past and ongoing nondeterminism in 12 popular, open-source static analysis tools that target 5 types of projects. We first conduct a qualitative study to understand the extent to which nondeterministic behavior has been found and addressed within the tools under study, and find results in 7 tool repositories. After classifying the issues and commits by root cause, we find that the majority of nondeterminisms are caused by concurrency issues, incorrect analysis logic, or assumed orderings of unordered data structures, which have shared patterns. We also perform a quantitative analysis, where we use two strategies and diverse input programs and configurations to detect yet-unknown nondeterministic behaviors. We discover such behavior in 8 out of the 12 tools, including 3 which had no results from the qualitative analysis. We find that nondeterminism often appears in multiple configurations on a variety of input programs. We communicated all identified nondeterminism to the developers, and received confirmation of five tools. Finally, we detail a case study of fixing FlowDroid's nondeterministic behavior.

## 10. AssetHarvester: A Static Analysis Tool for Detecting Secret-Asset Pairs in Software Artifacts

**Authors:** Setu Kumar Basak (North Carolina State University), K. Virgil English (North Carolina State University), Ken Ogura (North Carolina State University), Vitesh Kambara (North Carolina State University), Bradley Reaves (North Carolina State University), Laurie Williams (North Carolina State University)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029761

**中文总结:** 提出静态分析工具 AssetHarvester，检测密钥及其对应受保护资产标识符的配对，帮助开发者过滤误报并优先移除源码中泄露的密钥。

**Abstract:** GitGuardian monitored secrets exposure in public GitHub repositories and reported that developers leaked over 12 million secrets (database and other credentials) in 2023, indicating a 113\% surge from 2021. Despite the availability of secret detection tools, developers ignore the tools' reported warnings because of false positives (25\%-99\%). However, each secret protects assets of different values accessible through asset identifiers (a DNS name and a public or private IP address). The asset information for a secret can aid developers in filtering false positives and prioritizing secret removal from the source code. However, existing secret detection tools do not provide the asset information, thus presenting difficulty to developers in filtering secrets only by looking at the secret value or finding the assets manually for each reported secret. \textit{The goal of our study is to aid software practitioners in prioritizing secrets removal by providing the assets information protected by the secrets through our novel static analysis tool.} We present AssetHarvester, a static analysis tool to detect secret-asset pairs in a repository. Since the location of the asset can be distant from where the secret is defined, we investigated secret-asset co-location patterns and found four patterns. To identify the secret-asset pairs of the four patterns, we utilized three approaches (pattern matching, data flow analysis, and fast-approximation heuristics). We curated a benchmark of 1,791 secret-asset pairs of four database types extracted from 188 public GitHub repositories to evaluate the performance of AssetHarvester. AssetHarvester demonstrates precision of (97\%), recall (90\%), and F1-score (94\%) in detecting secret-asset pairs. Our findings indicate that data flow analysis employed in AssetHarvester detects secret-asset pairs with 0\% false positives and aids in improving the recall of secret detection tools. Additionally, AssetHarvester shows 43\% increase in precision for database secret detection compared to existing detection tools through the detection of assets, thus reducing developer's alert fatigue.

## 11. BDefects4NN: A Backdoor Defect Database for Controlled Localization Studies in Neural Networks

**Authors:** Yisong Xiao (Beihang University), Aishan Liu (Beihang University; Institute of Dataspace), Xinwei Zhang (Beihang University), Tianyuan Zhang (Beihang University), Li Tianlin (NTU), Siyuan Liang (National University of Singapore), Xianglong Liu (Beihang University; Institute of Dataspace; Zhongguancun Laboratory), Yang Liu (Nanyang Technological University), Dacheng Tao (Nanyang Technological University)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029765

**中文总结:** 提出 BDefects4NN，首个神经元粒度标注的后门缺陷数据库，支持可控条件下神经网络后门定位研究。

**Abstract:** Pre-trained large deep learning models are now serving as the dominant component for downstream middleware users and have revolutionized the learning paradigm, replacing the traditional approach of training from scratch locally. To reduce development costs, developers often integrate third-party pre-trained deep neural networks (DNNs) into their intelligent software systems. However, utilizing untrusted DNNs presents significant security risks, as these models may contain intentional backdoor defects resulting from the black-box training process. These backdoor defects can be activated by hidden triggers, allowing attackers to maliciously control the model and compromise the overall reliability of the intelligent software. To ensure the safe adoption of DNNs in critical software systems, it is crucial to establish a backdoor defect database for localization studies. This paper addresses this research gap by introducing \emph{BDefects4NN}, the first backdoor defect database, which provides labeled backdoor-defected DNNs at the neuron granularity and enables controlled localization studies of defect root causes. In \emph{BDefects4NN}, we define three defect injection rules and employ four representative backdoor attacks across four popular network architectures and three widely adopted datasets, yielding a comprehensive database of 1,654 backdoor-defected DNNs with four defect quantities and varying infected neurons. Based on \emph{BDefects4NN}, we conduct extensive experiments on evaluating six fault localization criteria and two defect repair techniques, which show limited effectiveness for backdoor defects. Additionally, we investigate backdoor-defected models in practical scenarios, specifically in lane detection for autonomous driving and large language models (LLMs), revealing potential threats and highlighting current limitations in precise defect localization. This paper aims to raise awareness of the threats brought by backdoor defects in our community and inspire future advancements in fault localization methods.

## 12. Boosting Path-Sensitive Value Flow Analysis via Removal of Redundant Summaries

**Authors:** Yongchao WANG (Hong Kong University of Science and Technology), Yuandao Cai (Hong Kong University of Science and Technology), Charles Zhang (Hong Kong University of Science and Technology)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029744

**中文总结:** 提出识别并剔除路径敏感值流分析中冗余函数摘要的首个方法，在大程序上将 state-of-the-art 分析的时间与内存开销分别降低 45% 与 27%。

**Abstract:** Value flow analysis that tracks the flow of values via data dependence is a widely used technique for detecting a broad spectrum of software bugs. However, the scalability issue often deteriorates when high precision (i.e., path-sensitivity) is required, as the instantiation of function summaries becomes excessively time- and memory-intensive. The primary culprit, as we observe, is the existence of redundant computations resulting from blindly computing summaries for a function, irrespective of whether they are related to bugs being checked. To address this problem, we present the first approach that can effectively identify and eliminate redundant summaries, thereby reducing the size of collected summaries from callee functions without compromising soundness or efficiency. Our evaluation on large programs demonstrates that our identification algorithm can significantly reduce the time and memory overhead of the state-of-the-art value flow analysis by 45\% and 27\%, respectively. Furthermore, the identification algorithm demonstrates remarkable efficiency by identifying nearly 80\% of redundant summaries while incurring a minimal additional overhead. In the largest \textit{mysqld} project, the identification algorithm reduces the time by 8107 seconds (2.25 hours) with a mere 17.31 seconds of additional overhead, leading to a ratio of time savings to paid overhead (i.e., performance gain) of 468.48 $\times$. In total, our method attains an average performance gain of 632.1 $\times$.

## 13. BSan: A Powerful Identifier-Based Hardware-Independent Memory Error Detector for COTS Binaries

**Authors:** Wen Zhang (University of Georgia), Botang Xiao (University of Georgia), Qingchen Kong (University of Georgia), Le Guan (University of Georgia), Wenwen Wang (University of Georgia)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029972

**中文总结:** 提出 BSan，采用基于标识符、硬件无关的静态分析加动态插桩混合方案检测商用二进制内存错误；能发现更多深层缺陷且开销与现有工具相当。

**Abstract:** This paper presents BSan, a practical software-only memory error detector for binary code. Different from state-of-the-art binary-level detectors, which rely on either the shadow memory-based approach or the hardware-specific feature and thus suffer from several fundamental limitations, BSan adopts an identifier-based approach, enabling it to detect deep memory errors missed by existing detectors. Also, BSan does not depend on any specific hardware features. To reduce the high performance overhead caused by identifier propagation, BSan creates a novel hybrid approach, static analysis+dynamic instrumentation, to improve the performance without inheriting the poor reliability of static binary rewriting, distinguishing it from existing detectors that simply refer to static binary rewriting for better performance. The comprehensive evaluation demonstrates that BSan can detect more memory errors than state-of-the-art binary-level detectors. Meanwhile, the performance and memory overheads of BSan are comparable to those of existing detectors.

## 14. Can an LLM find its way around a Spreadsheet?

**Authors:** Cho-Ting Lee (Virginia Tech), Andrew Neeser (Virginia Tech), Shengzhe Xu (Virginia Tech), Jay Katyan (Virginia Tech), Patrick Cross (Virginia Tech), Sharanya Pathakota (Virginia Tech), Marigold Norman (World Forest ID), John C. Simeone (Simeone Consulting, LLC), Jaganmohan Chandrasekaran (Virginia Tech), Naren Ramakrishnan (Virginia Tech)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029781

**中文总结:** 提出基于代码库检索的表格数据清洗系统，让大语言模型从可复用代码片段组合预处理流水线并持续扩充代码库。

**Abstract:** Spreadsheets are routinely used in business and scientific contexts, and one of the most vexing challenges is performing data cleaning prior to analysis and evaluation. The ad-hoc and arbitrary nature of data cleaning problems, such as typos, inconsistent formatting, missing values, and a lack of standardization, often creates the need for highly specialized pipelines. We ask whether an LLM can find its way around a spreadsheet and how to support end-users in taking their free-form data processing requests to fruition. Just like RAG retrieves context to answer users’ queries, we demonstrate how we can retrieve elements from a code library to compose data preprocessing pipelines. Through comprehensive experiments, we demonstrate the quality of our system and how it is able to continuously augment its vocabulary by saving new codes and pipelines back to the code library for future retrieval.

## 15. ConsCS: Effective and Efficient Verification of Circom Circuits

**Authors:** Jinan Jiang (The Hong Kong Polytechnic University), Xinghao Peng, Jinzhao Chu (The Hong Kong Polytechnic University), Xiapu Luo (Hong Kong Polytechnic University)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029906

**中文总结:** 提出 ConsCS 自动验证 Circom 电路约束完备性，引入电路推理规则与 Binary Property Graph 推理引擎，高效检测欠约束电路安全漏洞。

**Abstract:** Circom is a popular programming language for writing arithmetic circuits that can be used to generate zero-knowledge proofs (ZKPs) like zk-SNARKS. ZKPs have received tremendous attention in protocols like zkRollups. The Circom circuits are compiled to Rank-1 Constraint Systems (R1CS) circuits, based on which zk-SNARK proofs are generated. However, one major challenge associated with R1CS circuits is the problem of under-constrained circuits, which are susceptible to allowing incorrect computations to pass verification due to insufficient constraints, potentially leading to security vulnerabilities. In this paper, we propose a novel framework ConsCS to automatically verify Circom circuits. Our contributions are threefold: 1) we propose novel circuit inference rules to help reduce the size of circuits and to extract more comprehensive information than existing works; 2) we introduce the novel Binary Property Graph (BPG) as a highly efficient reasoning engine, outperforming all existing tools in effectiveness and efficiency; 3) we leverage fine-grained domain-specific information to guide the SMT solving to address non-linear constraints, increasing the success rate of SMT queries of existing works from 2.68% to 48.84%. We conduct experiments to show that ConsCS enhances the solved rate of existing works from around 50-60% to above 80%.

## 16. Constrained LTL Specification Learning from Examples

**Authors:** Changjian Zhang (Carnegie Mellon University), Parv Kapoor (Carnegie Mellon University), Ian Dardik (Carnegie Mellon University), Leyi Cui (Columbia University), Romulo Meira-Goes (The Pennsylvania State University), David Garlan (Carnegie Mellon University), Eunsuk Kang (Carnegie Mellon University)

**Categories:** Program Analysis and Verification, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029727

**中文总结:** 提出约束 LTL 规格学习问题，允许用户在正负轨迹之外指定公式属性约束，扩展时序逻辑规格合成的应用范围与效率。

**Abstract:** Temporal logic specifications play an important role in a wide range of software analysis tasks, such as model checking, automated synthesis, program comprehension, and runtime monitoring. Given a set of positive and negative examples, specified as traces, \emph{LTL learning} is the problem of synthesizing a specification, in \emph{linear temporal logic (LTL)}, that evaluates to true over the positive traces and false over the negative ones. In this paper, we propose a new type of LTL learning problem called \emph{constrained LTL learning}, where the user, in addition to positive and negative examples, is given an option to specify one or more \emph{constraints} over the properties of the LTL formula to be learned. We demonstrate that the ability to specify these additional constraints significantly increases the range of applications for LTL learning, and also allows efficient generation of LTL formulas that satisfy certain desirable properties (such as minimality). We propose an approach for solving the constrained LTL learning problem through an encoding in a first-order relational logic and reduction to an instance of the \emph{maximal satisfiability (MaxSAT)} problem. An experimental evaluation demonstrates that ATLAS, an implementation of our proposed approach, is able to solve new types of learning problems while performing better than or competitively with the state-of-the-art tools in LTL learning.

## 17. Cooperative Software Verification via Dynamic Program Splitting

**Authors:** Cedric Richter (University of Oldenburg), Marek Chalupa (Institute of Science and Technology Austria), Marie-Christine Jakobs (LMU Munich, Germany), Heike Wehrheim (University of Oldenburg)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029805

**中文总结:** 提出动态程序拆分（DPS）协作验证方案，按需将难验证任务动态拆分为更小程序并交给现成工具处理，克服静态分解忽视验证器能力差异及专有格式限制的问题。

**Abstract:** Cooperative software verification divides the task of software verification among several verification tools in order to increase efficiency and effectiveness. The basic approach is to let verifiers work on different parts of a program and at the end join verification results. While this idea is intuitively appealing, cooperative verification is usually hindered by the facts that program decomposition (1) is often static, disregarding strengths and weaknesses of employed verifiers, and (2) often represents the decomposed program parts in a specific proprietary format, thereby making the use of off-the-shelf verifiers in cooperative verification difficult. In this paper, we propose a novel cooperative verification scheme that we call dynamic program splitting (DPS). Splitting decomposes programs into (smaller) programs, and thus directly enables the use of off-the-shelf tools. In DPS, splitting is dynamically applied on demand: Verification starts by giving a verification task (a program plus a correctness specification) to a verifier V1. Whenever V1 finds the current task to be hard to verify, it splits the task (i.e., the program) and restarts verification on subtasks. DPS continues until (1) a violation is found, (2) all subtasks are completed or (3) some user-defined stopping criterion is met. In the latter case, the remaining uncompleted subtasks are merged into a single one and given to a next verifier V2, repeating the same procedure on the still unverified program parts. This way, the decomposition is steered by what is hard to verify for particular verifiers, leveraging their complementary strengths. We have implemented dynamic program splitting and evaluated it on benchmarks of the annual software verification competition SV-COMP. The evaluation shows that cooperative verification with DPS is able to solve verification tasks that none of the constituent verifiers can solve, without any significant overhead.

## 18. Datalog-Based Language-Agnostic Change Impact Analysis for Microservices

**Authors:** Qingkai Shi (Nanjing University), Xiaoheng Xie (Ant Group), Xianjin Fu (Ant Group), Peng Di (Ant Group & UNSW Sydney), Huawei Li (Alibaba Inc.), Ang Zhou (Ant Group), Gang Fan (Ant Group)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029842

**中文总结:** 提出 Microscope，以 Datalog 规则统一表示微服务中多语言代码、配置、框架与变更，借助高效 Datalog 求解器识别受影响公共接口；在领先软件公司实践中验证有效且快速。

**Abstract:** The shift-left principle in the industry requires us to test a software application as early as possible. Particularly, when code changes in a microservice application are committed to the code repository, we have to efficiently identify all public microservice interfaces impacted by the changes, such that the impacted interfaces can be tested as soon as possible. However, developing an efficient change impact analysis is extremely challenging in microservices because of the multilingual problem: microservice applications are often implemented using varying programming languages and involve diverse frameworks and configuration files. To address this issue, this paper presents Microscope, a language-agnostic change impact analysis that uniformly represents the code, configuration files, frameworks, and code changes by relational Datalog rules. Microscope then benefits from an efficient Datalog solver to identify impacted interfaces. Experiments based on the use of Microscope in a leading software company demonstrate that Microscope is both effective and fast as it successfully identifies interfaces impacted by 112 code commits, with moderate time overhead, and could reduce 97% of interfaces to test and save 73% of testing time after code changes.

## 19. DesignRepair: Dual-Stream Design Guideline-Aware Frontend Repair with Large Language Models

**Authors:** Mingyue Yuan (The university of new South Wales), Jieshan Chen (CSIRO's Data61), Zhenchang Xing (CSIRO's Data61), Aaron Quigley (CSIRO's Data61), Yuyu Luo (HKUST (GZ)), Tianqi Luo (HKUST (GZ)), Gelareh Mohammadi (The university of new South Wales), Qinghua Lu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** Testing and Quality, Program Analysis and Verification, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11030228

**中文总结:** 提出 DesignRepair 双流前端修复系统，结合 Material Design 知识库、大语言模型与 Playwright 从代码与渲染页两面对齐设计规范。

**Abstract:** The rise of Large Language Models (LLMs) has streamlined frontend interface creation through tools like Vercel's V0, yet surfaced challenges in design quality (e.g., accessibility, and usability). Current solutions, often limited by their focus, generalisability, or data dependency, fall short in addressing these complexities comprehensively. Moreover, none of them examine the quality of LLM-generated UI design. In this work, we introduce DesignRepair, a novel dual-stream design guideline-aware system to examine and repair the UI design quality issues from both code aspect and rendered page aspect. We utilised the mature and popular Material Design as our knowledge base to guide this process. Specifically, we first constructed a comprehensive knowledge base encoding Google's Material Design principles into low-level component knowledge base and high-level system design knowledge base. After that, DesignRepair employs a LLM for the extraction of key components and utilizes the Playwright tool for precise page analysis, aligning these with the established knowledge bases. Finally, we integrate Retrieval-Augmented Generation with state-of-the-art LLMs like GPT-4 to holistically refine and repair frontend code through a strategic divide and conquer approach. Our extensive evaluations validated the efficacy and utility of our approach, demonstrating significant enhancements in adherence to design guidelines, accessibility, and user experience metrics.

## 20. Dockerfile Flakiness: Characterization and Repair

**Authors:** Taha Shabani (University of British Columbia), Noor Nashid (University of British Columbia), Parsa Alian (University of British Columbia), Ali Mesbah (University of British Columbia)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029932

**中文总结:** 首次系统研究 Dockerfile  flaky 构建：8132 个项目中约 10% 存在 flaky，提出分类学及修复框架 FLAKIDOCK，修复准确率达 73.55%。

**Abstract:** Dockerfile flakiness—unpredictable temporal build failures caused by external dependencies and evolving environments—undermines deployment reliability and increases debugging overhead. Unlike traditional Dockerfile issues, flakiness occurs without modifications to the Dockerfile itself, complicating its resolution. In this work, we present the first comprehensive study of Dockerfile flakiness, featuring a nine-month analysis of 8,132 Dockerized projects, revealing that around 10% exhibit flaky behavior. We propose a taxonomy categorizing common flakiness causes, including dependency errors and server connectivity issues. Existing tools fail to effectively address these challenges due to their reliance on pre-defined rules and limited generalizability. To overcome these limitations, we introduce FLAKIDOCK, a novel repair framework combining static and dynamic analysis, similarity retrieval, and an iterative feedback loop powered by Large Language Models (LLMs). Our evaluation demonstrates that FLAKIDOCK achieves a repair accuracy of 73.55%, significantly surpassing state-of-the-art tools and baselines.

## 21. DPFuzzer: Discovering Safety Critical Vulnerabilities for Drone Path Planners

**Authors:** Yue Wang, Chao Yang (Xidian University), Xiaodong Zhang, Yuwanqi Deng (Xidian University), Jianfeng Ma (Xidian University)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029794

**中文总结:** 提出 DPFuzzer，用进化算法与 Environmental Risk Factor 指标生成多样危险障碍场景，测试无人机路径规划器的安全关键漏洞。

**Abstract:** State-of-the-art drone path planners enable drones to autonomously navigate around obstacles in GPS-denied, uncharted and cluttered environments. However, our investigation shows that path planners fail to maneuver drones correctly in specific scenarios, leading to incidents such as collisions. To minimize such risks, drone path planners should be tested thoroughly against diverse scenarios before deployment. Existing research for testing drones to uncover safety-critical vulnerabilities is only focused on the flight control programs and is limited in the capability to generate diverse obstacle scenarios for testing drone path planners. In this work, we propose \textit{DPFuzzer}, an automated framework for testing drone path planners. \textit{DPFuzzer} is an evolutionary algorithm (EA) based testing framework. It aims to uncover vulnerabilities in drone path planners by generating diverse critical scenarios that can trigger vulnerabilities. To better guide the critical scenario generation, we introduce \textit{Environmental Risk Factor (ERF)}, a metric we propose, to abstract potential safety threats of scenarios. We evaluate \textit{DPFuzzer} on state-of-the-art drone path planners and the experimental result shows that \textit{DPFuzzer} can effectively find diverse vulnerabilities. Additionally, we demonstrate that these vulnerabilities are exploitable in the real world on commercial drones.

## 22. EffBT: An Efficient Behavior Tree Reactive Synthesis and Execution Framework

**Authors:** Ziji Wu (National University of Defense Technology), yu huang (National University of Defense Technology), peishan huang (National University of Defense Technology), shanghua wen (National University of Defense Technology), minglong li (National University of Defense Technology), Ji Wang (National University of Defense Technology)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029907

**中文总结:** 提出 EffBT，从 GR(1) 形式规约自动合成语义正确且高效可执行的行为树，并引入剪枝与 Parallel 节点优化执行。

**Abstract:** Behavior Trees (BTs), originated from the control of Non-Player-Characters (NPCs), have been widely embraced in robotics and software engineering communities due to their modularity, reactivity, and other beneficial characteristics. It is highly desirable to synthesize BTs automatically. The consequent challenges are to ensure the generated BTs semantically correct, well-structured, and efficiently executable. To address these challenges, in this paper, we present a novel reactive synthesis method for BTs, namely EffBT, to generate correct and efficient controllers from formal specifications in GR(1) automatically. The idea is to construct BTs soundly from the intermediate strategies derived during the algorithm of GR(1) realizability check. Additionally, we introduce pruning strategies and use of \textit{Parallel} nodes to improve BT execution, while none of the priors explored before. We prove the soundness of the EffBT method, and experimental results across various scenarios and datasets demonstrate its effectiveness.

## 23. Enhancing Code Generation via Bidirectional Comment-Level Mutual Grounding

**Authors:** Yifeng Di (Purdue University), Tianyi Zhang (Purdue University)

**Categories:** AI for Software Engineering, Program Analysis and Verification, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029958

**中文总结:** 提出基于代码注释的双向互 grounding 交互式代码生成方法，通过迭代注释与反馈对齐开发者意图，显著提升多种 LLM 的 Pass@1。

**Abstract:** Large Language Models (LLMs) have demonstrated unprecedented capability in code generation. However, LLM-generated code is still plagued with a wide range of functional errors, especially for complex programming tasks that LLMs have not seen before. Recent studies have shown that developers often struggle with inspecting and fixing incorrect code generated by LLMs, diminishing their productivity and trust in LLM-based code generation. Inspired by the mutual grounding theory in communication, we propose an interactive approach that leverages code comments as a medium for developers and LLMs to establish a shared understanding. Our approach facilitates iterative grounding by interleaving code generation, inline comment generation, and contextualized user feedback through editable comments to align generated code with developer intent. We evaluated our approach on two popular benchmarks and demonstrated that our approach significantly improved multiple state-of-the-art LLMs, e.g., 16.9\% Pass@1 improvement for code-davinci-002 on HumanEval. Furthermore, we conducted a user study with 12 participants in comparison to two baselines: (1) interacting with GitHub Copilot, and (2) interacting with a multi-step code generation paradigm called Multi-Turn Program Synthesis. Participants completed the given programming tasks 16.7\% faster and with 10.5\% improvement in task success rate when using our approach. Both results show that interactively refining code comments enables the collaborative establishment of mutual grounding, leading to more accurate code generation and higher developer confidence.

## 24. Enhancing Fault Localization in Industrial Software Systems via Contrastive Learning

**Authors:** Chun Li (Nanjing University), Hui Li (Samsung Electronics (China) R&D Centre), Zhong Li, Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Program Analysis and Verification, Evolution and Maintenance, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029934

**中文总结:** 提出 FALCON，将工业日志组织为图并用对比学习区分通过/失败运行以定位故障；相较 34 种谱方法与 4 种学习方法整体表现最优。

**Abstract:** Engineers utilize logs as a primary resource for fault localization in large-scale software and system testing, a process that is notoriously time-consuming, costly, and labor-intensive. Despite considerable progress in automated fault localization approaches, their applicability remains limited in such settings, due to the unavailability of fine-grained features in logs essential for most existing fault localization methods. In response, we introduce FALCON, a novel log-based fault localization framework. FALCON organizes complex semantic log information into graphical representations and employs contrastive learning to capture the differences between passed and failed logs, enabling the identification of crucial fault-related features. It also incorporates a specifically designed transitive analysis-based adaptive graph augmentation to minimize the influence of fault-unrelated log information on contrastive learning. Through extensive evaluations against 34 spectrum-based and 4 learning-based fault localization methods, FALCON demonstrates superior performance by outperforming all the methods in comparison. In addition, FALCON demonstrated its practical value by successfully identifying 71 out of 90 faults with a file-level Top-1 accuracy rate during a one-month deployment within a global company’s testing system.

## 25. Enhancing The Open Network: Definition and Automated Detection of Smart Contract Defects

**Authors:** Hao Song, Teng Li (University of Electronic Science and Technology of China), Jiachi Chen (Sun Yat-sen University), Ting Chen (University of Electronic Science and Technology of China), Beibei Li (Sichuan University), Zhangyan Lin (University of Electronic Science and Technology of China), Yi Lu (BitsLab), Pan Li (MoveBit), Xihan Zhou (TonBit)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029871

**中文总结:** 总结 TON 链 FunC 智能合约 8 类缺陷并定义检测规范，提出静态分析框架 TONScanner，复用 FunC 编译器前端生成 IR/CFG/SSA 以自动检测这些缺陷。

**Abstract:** The Open Network (TON), designed to support Telegram's extensive user base of hundreds of millions, has garnered considerable attention since its launch in 2022. \textit{FunC} is the most popular programming language for writing smart contracts on TON. It is distinguished by a unique syntax compared to other smart contract languages. Despite growing interest, research on the practical defects of TON smart contracts is still in its early stages. In this paper, we summarize eight smart contract defects identified from TON's official blogs and audit reports, each with detailed definitions and code examples. Furthermore, we propose a static analysis framework called TONScanner to facilitate the detection of these defects. Specifically, TONScanner reuses \textit{FunC} compiler's frontend code to transform the \textit{FunC} contract code into \textit{FunC} intermediate representation (IR) in the form of a directed acyclic graph (DAG). Based on this IR, TONScanner constructs a control flow graph (CFG), then transforms it into a static single assignment (SSA) form to simplify further analysis. TONScanner also integrates Data Dependency, Call Graph, Taint Analysis, and Cell Construct, which are specifically tailored for TON blockchain's unique data structures. These components finally facilitate the identification of the eight defects. We evaluate the effectiveness of TONScanner by applying it to 1,640 smart contracts and find a total of 14,995 defects. Through random sampling and manual labeling, we find that TONScanner achieves an overall precision of 97.49%. The results reveal that current TON contracts contain numerous defects, indicating that developers are prone to making errors. TONScanner has proven its ability to accurately identify these defects, thereby aiding in their correction.

## 26. Evaluating Garbage Collection Performance Across Managed Language Runtimes

**Authors:** Yicheng Wang (Institute of Software Chinese Academy of Sciences), Wensheng Dou (Institute of Software Chinese Academy of Sciences), Yu Liang (Institute of Software Chinese Academy of Sciences), Yi Wang (Institute of Software Chinese Academy of Sciences), Wei Wang (Institute of Software at Chinese Academy of Sciences), Jun Wei (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Tao Huang (Institute of Software Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029923

**中文总结:** 提出 GEAR，用运行时无关的内存操作原语构造一致 GC 负载并自动翻译到 Java、Go、C# 等运行时，实现跨托管语言 GC 性能的可比评估。

**Abstract:** Modern managed language runtimes (e.g., Java, Go and C#) rely on garbage collection (GC) mechanisms to automatically allocate and reclaim in-memory objects. The efficiency of GC implementations can greatly impact the overall performance of runtime-based applications. To improve GC performance, the academic and industrial communities have proposed several approaches to evaluate the GC implementations in an individual runtime. However, these approaches target a specific managed language (e.g., Java), and cannot be used to compare the GC implementations in different runtimes. In this paper, we propose GEAR, an automated approach to construct consistent GC workloads for different managed language runtimes, which can further be used to evaluate GC implementations across different runtimes. Specifically, we design a group of runtime-agnostic Memory Operation Primitives (MOP), which can portray the memory usage information that influences GC. GEAR can further automatically convert a MOP program into runtime-specific programs for the target runtimes, which serve as a consistent GC workload for different runtimes. To build MOP programs with real-world GC workloads, we instrument the commonly-used runtime Java Virtual Machine (JVM) to collect the memory operation trace during a Java application’s execution, and then transform the memory operation trace into a MOP program. The experimental result on three widely-used runtimes (i.e., Java, Go and C#) shows that GEAR can generate consistent GC workloads for different runtimes. We further conduct a comprehensive study on these three runtimes, and reveal some interesting findings about their GC performance, providing useful guidance for improving their GC implementations.

## 27. Execution Trace Reconstruction Using Diffusion-Based Generative Models

**Authors:** Madeline Janecek (Brock University), Naser Ezzati-Jivan, Abdelwahab Hamou-Lhadj (Concordia University, Montreal, Canada)

**Categories:** AI for Software Engineering, Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029922

**中文总结:** 首次系统评估扩散模型重建不完整执行追踪序列，SSSD^S4 在九个 Phoronix 数据集上于多种缺失比例下表现最优。

**Abstract:** Execution tracing is essential for understanding system and software behaviour, yet lost trace events can significantly compromise data integrity and analysis. Existing solutions for trace reconstruction often fail to fully leverage available data, particularly in complex and high-dimensional contexts. Recent advancements in generative artificial intelligence, particularly diffusion models, have set new benchmarks in image, audio, and natural language generation. This study conducts the first comprehensive evaluation of diffusion models for reconstructing incomplete trace event sequences. Using nine distinct datasets generated from the Phoronix Test Suite, we rigorously test these models on sequences of varying lengths and missing data ratios. Our results indicate that the SSSD$^{S4}$ model, in particular, achieves superior performance, in terms of accuracy, perfect rate, and ROUGE-L score across diverse imputation scenarios. These findings underscore the potential of diffusion-based models to accurately reconstruct missing events, thereby maintaining data integrity and enhancing system monitoring and analysis.

## 28. FairChecker: Detecting Fund-stealing Bugs in DeFi Protocols via Fairness Validation

**Authors:** Yi Sun (Purdue University, USA), Zhuo Zhang (Purdue University), Xiangyu Zhang (Purdue University)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029916

**中文总结:** 提出 FairChecker，通过公平性验证检测 DeFi 协议中因关键状态变量未正确维护导致的盗资缺陷，弥补传统分析工具难以捕获领域特定功能 bug 的不足。

**Abstract:** Decentralized Finance (DeFi) is an emerging paradigm within the blockchain space that aims to revolutionize conventional financial systems through the application of blockchain technology. The substantial value of digital assets managed by DeFi protocols makes it a lucrative target for attacks. Despite the human resources and the application of automated tools, frequent attacks still cause significant fund losses to DeFi participants. Existing tools primarily rely on oracles similar to those used in traditional software analysis, making it challenging for them to detect functional bugs specific to the DeFi domain. Since blockchain functions as a distributed ledger system, the foundation of any DeFi protocol is the accurate maintenance of key state variables representing user funds. If these variables are not properly updated or designed to reflect the intended flow of funds, attackers can exploit these flaws to steal assets. From the study of popular DeFi protocols, we observe that, in DeFi systems, to ensure a transaction does not misappropriate someone's fund, the direction of changes (increase or decrease) of values associated with the amount of asset or debt of a user has to adhere to some fairness properties. We propose a concept called fairness bug which allows attackers to gain profit without cost. We propose an inter-procedural and inter-contract static analysis technique that utilizes symbolic execution and an SMT solver to automatically detect fairness bugs in DeFi smart contracts. We have implemented our fairness-checking approach in our tool, named FairChecker. We evaluate our tool on a benchmark of 113 real-world DeFi protocols with 34 fairness bugs. The results show that our tool can detect 32 bugs with a recall of 94.1\% and a precision of 46.4\%, demonstrating its effectiveness.

## 29. FairQuant: Certifying and Quantifying Fairness of Deep Neural Networks

**Authors:** Brian Hyeongseok Kim (University of Southern California), Jingbo Wang (University of Southern California), Chao Wang (University of Southern California)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029755

**中文总结:** 提出 FairQuant，用符号区间抽象与迭代精化形式化认证并量化深度神经网络个体公平性（给出可证公平比例），在 5 个公平数据集上更准确且更可扩展。

**Abstract:** We propose a method for formally certifying and quantifying individual fairness of a deep neural network (DNN). Individual fairness guarantees that any two individuals who are identical except for some protected input attribute (e.g., gender or race) receive the same treatment. While there are existing techniques that provide such a guarantee, they suffer from lack of scalability or accuracy as the size and input dimension of the DNN increase. Our method overcomes this limitation by applying abstraction to a symbolic interval based analysis of the DNN followed by iterative refinement guided by the fairness property. Furthermore, our method lifts the interval based analysis from the conventional qualitative certification to quantitative certification, by computing the percentage of individuals whose classification outputs are provably fair, instead of merely deciding if the DNN is fair. We have implemented our method and evaluated it on deep neural networks trained on five popular fairness research datasets. The experimental results show that our method is not only more accurate than state-of-the-art techniques but also several orders-of-magnitude faster.

## 30. Fixing Large Language Models' Specification Misunderstanding for Better Code Generation

**Authors:** Zhao Tian (Tianjin University), Junjie Chen (Tianjin University), Xiangyu Zhang (Purdue University)

**Categories:** AI for Software Engineering, Software Engineering for AI, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029745

**中文总结:** 提出 μFiX 提示技术，结合思维引导与细粒度反馈修复大语言模型对编程规格的理解偏差以提升代码生成质量。

**Abstract:** Code generation is to automatically generate source code conforming to a given programming specification, which has received extensive attention especially with the development of large language models (LLMs). Due to the inherent difficulty of code generation, the code generated by LLMs may not be aligned with the specification. Although thought-eliciting prompting techniques have been proposed to enhance the code generation performance of LLMs, producing correct understanding for complicated programming problems remains challenging, resulting in unsatisfactory performance. Also, some feedback-based prompting techniques have been proposed to fix incorrect code using error messages produced by test execution. However, when the generated code deviates significantly from the ground truth, they encounter difficulties in improving performance based on such coarse-grained information. In this work, we propose a novel prompting technique, called μFiX, to improve the code generation performance of LLMs by devising both sophisticated thought-eliciting prompting and feedback-based prompting and making the first exploration on their synergy. It first exploits test case analysis to obtain specification understanding and enables a self-improvement process to identify and refine the misunderstanding in the thought-eliciting prompting phase. μFiX further fixes the specification understanding towards the direction reducing the gap between the provided understanding (from the first phase) and the actual understanding implicitly utilized by LLMs for code generation in the feedback-based prompting phase. By improving the understanding with μFiX, the code generation performance of LLMs can be largely improved. Our evaluation on two advanced LLMs (ChatGPT and DeepSeek-Coder) with six widely-used benchmarks by comparing with 15 baselines, demonstrates the effectiveness of μFiX. For example, μFiX outperforms the most effective baseline with an average improvement of 35.62% in terms of Pass@1 across all subjects.

## 31. Formally Verified Binary-level Pointer Analysis

**Authors:** Freek Verbeek (Open Universiteit & Virginia Tech), Ali Shokri (Virginia Tech), Daniel Engel (Open University Of The Netherlands), Binoy Ravindran (Virginia Tech)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029887

**中文总结:** 提出可形式化证明正确的二进制级指针分析，先定义抽象域通用证明义务再实例化不同精度域，在可扩展性与分析结果可信性间取得平衡。

**Abstract:** Binary-level pointer analysis can be of use in symbolic execution, testing, verification, and decompilation of software binaries. In various such contexts, it is crucial that the result is trustworthy, i.e., it can be formally established that the pointer designations are overapproximative. This paper presents an approach to formally proven correct binary-level pointer analysis. A salient property of our approach is that it first generically considers what proof obligations a generic abstract domain for pointer analysis must satisfy. This allows easy instantiation of different domains, varying in precision, while preserving the correctness of the analysis. In the trade-off between scalability and precision, such customization allows ``meaningful'' precision (sufficiently precise to ensure basic sanity properties, such as that relevant parts of the stack frame are not overwritten during function execution) while also allowing coarse analysis when pointer computations have become too obfuscated during compilation for sound and accurate bounds analysis. We experiment with three different abstract domains with high, medium, and low precision. Evaluation shows that our approach is able to derive designations for memory writes soundly in COTS binaries, in a context-sensitive interprocedural fashion.

## 32. GenC2Rust: Towards Generating Generic Rust Code from C

**Authors:** Xiafa Wu (University of California, Irvine), Brian Demsky (University of California at Irvine)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029860

**中文总结:** 提出 GenC2Rust，通过静态分析 C 程序中 void 指针用法推导类型约束，将非泛型 C 代码翻译为符合 Rust 习惯的泛型 Rust 代码，缓解现有 C 转 Rust 工具难以利用泛型的问题。

**Abstract:** Rust provides an exciting combination of strong safety guarantees and high performance. Many new systems are being implemented in Rust. Nevertheless, there is a large body of existing C code that could greatly benefit from Rust's safety guarantees. Unfortunately, the manual effort required to rewrite C code into Rust is often prohibitively expensive. Researchers have explored tools to assist developers in translating legacy C code into Rust code. However, the mismatch between C abstractions and idiomatic Rust abstractions makes it challenging to automatically utilize Rust's language features, resulting in non-idiomatic Rust code that requires extensive manual effort to further refactor. For example, existing tools often fail to map polymorphic uses of void pointers in C to Rust's more idiomatic generic pointers. In this paper, we present a translation tool, GenC2Rust, that translates non-generic C code into generic Rust code. GenC2Rust statically analyzes the use of void pointers in the C program to compute the typing constraints and then retypes the void pointers into generic pointers. We conducted an evaluation of GenC2Rust across 42 C programs that vary in size and span multiple domains to demonstrate its scalability as well as correctness. We also present a detailed analysis of the limiting factors encountered in the translation process.

## 33. Gpass: a Goal-adaptive Neural Theorem Prover based on Coq for Automated Formal Verification

**Authors:** Yizhou Chen (Peking University), Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Guoqing Wang (Peking University), Dan Hao (Peking University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029939

**中文总结:** 提出面向 Coq 的目标自适应神经定理证明器 Gpass，通过滑动窗口编码与目标自适应特征融合自动生成长证明步骤，克服现有自动定理证明器的局限。

**Abstract:** Formal verification is a crucial means to assure software quality. Regrettably, the manual composition of verification scripts proves to be both laborious and time-consuming. In response, researchers have put forth automated theorem prover approaches; however, these approaches still grapple with several limitations. These limitations encompass insufficient handling of lengthy proof steps, difficulty in aligning the various components of a Coq program with the requirements and constraints of the proof goal, and inefficiencies. To surmount these limitations, we present Gpass, a goal-adaptive neural theorem prover based on deep learning technology. Firstly, we design a unique sequence encoder for Gpass that completely scans previous proof tactics through multiple sliding windows and provides information related to the current proof step. Secondly, Gpass incorporates a goal-adaptive feature integration module to align the reasoning process with the requirements of the proof goal. Finally, we devise a parameter selection method based on loss values and loss slopes to procure parameter sets with diverse distributions, thereby facilitating the exploration of various proof tactics. Experimental results demonstrate that Gpass attains better performance on the extensive CoqGym benchmark and proves 11.03\%-96.37\% more theorems than the prior work most closely related to ours. We find that the orthogonality between Gpass and CoqHammer proves their complementary capabilities, and together they prove a total of 3,774 theorems, which is state-of-the-art performance. In addition, we propose an efficiency optimisation approach that allows Gpass to achieve performance beyond Diva at one-sixth of the parameter sets.

## 34. Hetrify: Efficient Verification of Heterogeneous Programs on RISC-V

**Authors:** Yiwei Li (School of Computer, National Univer sity of Defense Technology), Liangze Yin (School of Computer, National Univer sity of Defense Technology), Wei Dong (National University of Defense Technology), Jiaxin Liu (National University of Defense Technology), Yanfeng Hu (School of Computer, National Univer sity of Defense Technology), Shanshan Li (National University of Defense Technology)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029929

**中文总结:** 提出 Hetrify 异构程序验证方法，将多语言/汇编/闭源库等编译为 RISC-V 二进制后在语义等价保证下转为可验证 C 代码，实现通用异构程序的形式化验证。

**Abstract:** The heterogeneous nature of contemporary software, comprising components like closed-source libraries, embedded assembly snippets, and modules written in multiple programming languages, leads to significant verification challenges. Currently, There are no mature and available methods to effectively address such problems. To bridge this gap, we propose a verification approach capable of effectively verifying heterogeneous programs. This approach is universally applicable. It theoretically supports the verification of any heterogeneous program that can be compiled into binary code, without being constrained by any specific programming language. The approach begins by compiling the entire program or its unverifiable segments into binary format. Under guarantees of semantic equivalence, these binaries are converted into verifiable C code, which can then be verified using existing C verification tools. Based on the RISC-V architecture, we developed the Hetrify tool to implement this verification approach. The tool is supported by rigorous mathematical proofs to ensure operational semantic equivalence between the converted C programs and their original counterparts. To validate our approach, we conducted verification experiments on 130 programs, including 100 assembly programs and 30 large heterogeneous programs with missing critical function source code, demonstrating the effectiveness of our approach.

## 35. Hyperion: Unveiling DApp Inconsistencies using LLM and Dataflow-Guided Symbolic Execution

**Authors:** Shuo Yang (Sun Yat-sen University), Xingwei Lin (Ant Group), Jiachi Chen (Sun Yat-sen University), Qingyuan Zhong (Sun Yat-sen University), Lei Xiao (Sun Yat-sen University), renke huang (Sun Yat-sen University), Yanlin Wang (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11030227

**中文总结:** 归纳 7 类 DApp 前后端功能不一致并提出 Hyperion，用微调 LLaMA2 分析前端描述、数据流引导符号执行分析合约字节码以自动检测不一致。

**Abstract:** The rapid advancement of blockchain platforms has significantly accelerated the growth of decentralized applications (DApps). Similar to traditional applications, DApps integrate front-end descriptions that showcase their features to attract users, and back-end smart contracts for executing their business logic. However, inconsistencies between the features promoted in front-end descriptions and those actually implemented in the contract can confuse users and undermine DApps's trustworthiness. In this paper, we first conducted an empirical study to identify seven types of inconsistencies, each exemplified by a real-world DApp. Furthermore, we introduce Hyperion, an approach designed to automatically identify inconsistencies between front-end descriptions and back-end code implementation in DApps. This method leverages a fine-tuned large language model LLaMA2 to analyze DApp descriptions and employs dataflow-guided symbolic execution for contract bytecode analysis. Finally, Hyperion reports the inconsistency based on predefined detection patterns. The experiment on our ground truth dataset consisting of 54 DApps shows that Hyperion reaches 84.06\% overall recall and 92.06\% overall precision in reporting DApp inconsistencies. We also implement Hyperion to analyze 835 real-world DApps. The experimental results show that Hyperion discovers 459 real-world DApps containing at least one inconsistency.

## 36. Instrumentation-Driven Evolution-Aware Runtime Verification

**Authors:** Kevin Guan (Cornell University), Owolabi Legunsen (Cornell University)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029969

**中文总结:** 提出 iMOP 首个插桩驱动的演化感知运行时验证框架，针对测试开销主要来自插桩而非监控的观察，仅对变更代码重新插桩并复用旧版本插桩，在 14 种技术组合下安全加速 RV。

**Abstract:** Runtime verification (RV) found hundreds of bugs by monitoring passing tests against formal specifications (specs). RV first instruments a program to obtain relevant events, e.g., method calls, to monitor. A hindrance to RV adoption, especially in continuous integration, is its high overhead. So, prior work proposed spec-driven evolution-aware techniques to speed up RV. They use complex analysis to re-monitor a subset of specs related to code impacted by changes. But, these techniques assume that RV overhead is dominated by monitoring time, and their designs often sacrifice safety (ability to find all new violations) for speed. We present iMOP, the first instrumentation-driven evolution-aware RV framework. iMOP leverages a recent observation that RV overhead during testing is often dominated by instrumentation, not monitoring. iMOP embodies a family of 14 techniques that aim to safely speed up RV by simply re-instrumenting only changed code. Instrumentation from the old revision is re-used for unchanged code, and all specs are re-monitored in the new revision. We implement iMOP as a Maven plugin and evaluate it on 1,627 revisions of 48 projects, using 160 specs of correct JDK API usage. iMOP is safe by design. It is up to 29.6x faster than re-running RV from scratch after each change, and 17.8x and 6.7x faster than safe and unsafe spec-driven techniques, respectively. iMOP is faster than just applying regression test selection to RV.

## 37. Interactive Cross-Language Pointer Analysis for Resolving Native Code in Java Programs

**Authors:** Chenxi Zhang (Nanjing University), Yufei Liang (Nanjing University), Tian Tan (Nanjing University), Chang Xu (Nanjing University), Shuangxiang Kan (UNSW), Yulei Sui (University of New South Wales), Yue Li (Nanjing University)

**Categories:** Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029730

**中文总结:** 提出 JNIFER 首个交互式跨语言指针分析，联合 Java 与 C 指针分析并通过 JNI 函数分析在交互点构建跨语言 points-to 与调用图，评估显示优于现有方法。

**Abstract:** Java offers the Java Native Interface (JNI), which allows programs running in the Java Virtual Machine to invoke and be manipulated by native applications and libraries written in other languages, typically C. While JNI mechanism significantly enhances the Java platform's capabilities, it also presents challenges for static analysis of Java programs due to the complex behaviors introduced by native code. Therefore, effectively resolving the interactions between Java and native code is crucial for static analysis. In this paper, we introduce JNIFER, the first interactive cross-language pointer analysis for resolving native code in Java programs. JNIFER integrates both Java and C pointer analyses, equipped with advanced native call and JNI function analyses, enabling the simultaneous analysis of both Java and native code. During the analysis of cross-language interactions, the two analyzers interact with each other, constructing cross-language points-to relations and call graphs, thereby approximating the runtime behavior at the interaction sites. Our evaluation shows that JNIFER outperforms state-of-the-art approaches in terms of soundness while maintaining high precision and comparable efficiency, as evidenced by extensive experiments on OpenJDK and real-world Java applications.

## 38. IRFuzzer: Specialized Fuzzing for LLVM Backend Code Generation

**Authors:** Yuyang Rong (University of California, Davis), Zhanghan Yu (University of California, Davis), Zhenkai Weng (University of California, Davis), Stephen Neuendorffer (Advanced Micro Devices, Inc.), Hao Chen (University of California at Davis)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029772

**中文总结:** 提出 IRFuzzer 面向 LLVM 后端代码生成的专用模糊测试，以约束变异保证 IR 合法并引入指令选择覆盖反馈。

**Abstract:** Modern compilers, such as LLVM, are complex. Due to their complexity, manual testing is unlikely to suffice, yet formal verification is difficult to scale. End-to-end fuzzing can be used, but it has difficulties in discovering LLVM backend problems for two reasons. First, frontend preprocessing and middle optimization shield the backend from seeing diverse inputs. Besides, edge coverages cannot provide an effective feedback as LLVM backend contains much reusable code. In this paper, we implement IRFuzzer to investigate the need of specialized fuzzing of the LLVM compiler backend. We focus on two approaches to improve the fuzzer: guaranteed input validity using constrained mutations to improve input diversity and new metrics to improve feedback quality. The mutator in IRFuzzer is capable of generating a wide range of LLVM IR inputs, including structured control flow, vector types, and function definitions. The system instruments coding patterns in the compiler to monitor the execution status of instruction selection. The instrumentation not only provides a new coverage feedback called matcher table coverage, but also provides an architecture specific guidance to the mutator. We show that IRFuzzer is more effective than existing fuzzers by fuzzing on 29 mature LLVM backend targets. In the process, we reported 78 confirmed new bugs in LLVM upstream, out of which 57 have been fixed, five have been back ported to LLVM 15, showing that specialized fuzzing provides useful and actionable insights to LLVM developers.

## 39. Knowledge-Enhanced Program Repair for Data Science Code

**Authors:** Shuyin Ouyang (King's College London), Jie M. Zhang (King's College London), Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Albert Merono Penuela (King's College London)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029882

**中文总结:** 提出 DSrepair，以数据科学知识图谱 RAG 与 AST 级错误定位增强 LLM 修复提示；在 DS-1000 上相较最优基线多修复 14.2%–44.4% 的缺陷代码。

**Abstract:** This paper introduces DSrepair, a knowledge-enhanced program repair method designed to repair the buggy code generated by LLMs in the data science domain. DSrepair uses knowledge graph based RAG for API knowledge retrieval as well as bug knowledge enrichment to construct repair prompts for LLMs. Specifically, to enable knowledge graph based API retrieval, we construct DS-KG (Data Science Knowledge Graph) for widely used data science libraries. For bug knowledge enrichment, we employ an abstract syntax tree (AST) to localize errors at the AST node level. DSrepair's effectiveness is evaluated against five state-of-the-art LLM-based repair baselines using four advanced LLMs on the DS-1000 dataset. The results show that DSrepair surpasses all five baselines. Specifically, when compared to the second-best baseline, DSrepair demonstrates significant improvements, fixing 44.4%, 14.2%, 20.6%, and 32.1% more buggy code snippets for each of the four evaluated LLMs, respectively. Additionally, it achieves greater efficiency, reducing the number of tokens required per code task by 17.49%, 34.24%, 24.71%, and 17.59%, respectively.

## 40. Leveraging Propagated Infection to Crossfire Mutants

**Authors:** Hang Du (University of California at Irvine), Vijay Krishna Palepu (Microsoft), James Jones (University of California at Irvine)

**Categories:** Testing and Quality, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029834

**中文总结:** 研究发现最多 84% 存活变异体可通过断言放大检测，提出基于内存状态分析识别候选断言并结合交叉击杀模型的测试增强技术。

**Abstract:** Mutation testing was proposed to identify weaknesses in test suites by repeatedly generating artificially faulty versions of the software (i.e., *mutants*) and determining if the test suite is sufficient to detect them (i.e., *kill* them). When the tests are insufficient, each surviving mutant provides an opportunity to improve the test suite. We conducted a study and found that many such surviving mutants (up to 84% for the subjects of our study) are detectable by simply augmenting existing tests with additional assertions, or *assertion amplification*. Moreover, we find that many of these mutants are detectable by multiple existing tests, giving developers options for how to detect them. To help with these challenges, we created a technique that performs memory-state analysis to identify candidate assertions that developers can use to detect the surviving mutants. Additionally, we build upon prior research that identifies "crossfiring" opportunities -- tests that coincidentally kill multiple mutants. To this end, we developed a theoretical model that describes the varying granularities that crossfiring can occur in the existing test suite, which provide opportunities and options for how to kill surviving mutants. We operationalize this model to an accompanying technique that optimizes the assertion amplification of the existing tests to crossfire multiple mutants with fewer added assertions, optionally concentrated within fewer tests. Our experiments show that we can kill *all* surviving mutants that are detectable with existing test data with only 1.1% of the identified assertion candidates, and increasing by a factor of 6x, on average, the number of killed mutants from amplified tests, over tests that do not crossfire.

## 41. LLM-aided Automatic Modeling for Security Protocol Verification

**Authors:** Ziyu Mao (Zhejiang University), Jingyi Wang (Zhejiang University), Jun Sun (Singapore Management University), Shengchao Qin (Xidian University), Jiawen Xiong (East China Normal University)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029741

**中文总结:** 将自然语言协议描述的分阶段分解为增量形式化建模任务，用 LLM 辅助自动生成 Tamarin/ProVerif 等符号协议验证模型，降低手工建模门槛。

**Abstract:** Symbolic protocol analysis serves as a pivotal technique for protocol design, security analysis, and the safeguarding of information assets. Several modern tools such as Tamarin and ProVerif have been proven successful in modeling and verifying real-world protocols, including complex protocols like TLS 1.3 and 5G AKA. However, developing formal models for protocol verification is a non-trivial task, which hinders the wide adoption of these powerful tools in practical protocol analysis. In this work, we aim to bridge the gap by developing an automatic method for generating symbolic protocol models using Large Language Models (LLMs) from protocol descriptions in natural language document. Although LLMs are powerful in various code generation tasks, it is shown to be ineffective in generating symbolic models (according to our empirical study). Therefore, rather than applying LLMs naively, we carefully decompose the symbolic protocol modelling task into several stages so that a series of formal models are incrementally developed towards generating the final correct symbolic model. Specifically, we apply LLMs for semantic parsing, enable lightweight manual interaction for disambiguation, and develop algorithms to transform the intermediate models for final symbolic model generation. To ensure the correctness of the generated symbolic model, each stage is designed based on a formal execution model and the model transformations are proven sound. To the best of our knowledge, this is the first work aiming to generate symbolic models for protocol verification from natural language documents. We also introduce a benchmark for symbolic protocol model generation, with 18 real-world security protocol's text description and their corresponding symbolic models. We then demonstrate the potential of our tool, which successfully generated correct models of moderate scale in 10 out of 18 cases.

## 42. Module-Aware Context Sensitive Pointer Analysis

**Authors:** Haofeng Li (SKLP, Institute of Computing Technology, CAS), Chenghang Shi (SKLP, Institute of Computing Technology, CAS), Jie Lu (SKLP, Institute of Computing Technology, CAS), Lian Li (Institute of Computing Technology at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Zixuan Zhao (Huawei Technologies Co. Ltd)

**Categories:** Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029851

**中文总结:** 提出模块感知指针分析 MPA，建模 JPMS 的 provides/uses 语义恢复缺失指向关系，在 Tai-e 上兼顾精度、完备性与效率。

**Abstract:** The Java Platform Module System (JPMS) has found widespread applications since introduced in Java 9. However, existing pointer analyses fail to leverage the semantics of JPMS. This paper presents a novel module-aware approach to improving the soundness and performance of pointer analysis. For soundness, we model the semantics of keywords provides and uses in JPMS to recover missing points-to relations. For performance, we design a module-aware context-sensitive analysis, which can propagate and apply critical contexts (by exploiting modularity) to balance precision and efficiency better. We have implemented our module-aware pointer analysis named MPA in Tai-e and conducted extensive experiments to compare it with standard object-sensitive approaches. The evaluation results demonstrate that MPA improves soundness and enhances existing context-sensitivity, striking a good balance between efficiency and precision. In terms of soundness, MPA can increase the number of reachable methods up to 90.9 × 90.9× ( lombok lombok) under the same analysis. Performance-wise, MPA is nearly as fast as context-insensitivity for most benchmarks, while its precision is superior to that of 1-object-sensitivity on average.

## 43. Moye: A Wallbreaker for Monolithic Firmware

**Authors:** Jintao Huang (Institute of Information Engineering, Chinese Academy of Science & University of Chinese Academy of Sciences, Beijing, China), Kai Yang (School of Computer, Electronics and Information, Guangxi University), Gaosheng Wang (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China), Zhiqiang Shi (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China), Zhiwen Pan (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China), Shichao Lv (Institute of Information Engineering, Chinese Academy of Science), Limin Sun (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029743

**中文总结:** 提出 Moye，针对无格式标识的单体固件，利用寄存器使用约束与掩码语言模型学习指令间隐含关系以识别函数边界；在 1318 个固件镜像（含 48 个真实设备样本）上验证有效性。

**Abstract:** As embedded devices become increasingly popular, monolithic firmware, known for its execution efficiency and simplicity, is widely used in resource-constrained devices. Different from ordinary firmware, the monolithic firmware image is packed without the file that indicates its format, which challenges the reverse engineering of monolithic firmware. Function identification is the prerequisite of monolithic firmware's analysis. Prior works on function identification are less effectiveness when applied to monolithic firmware due to their heavy reliance on file formats. In this paper, we propose Moye, a novel method to identify functions in monolithic firmware. We leverage the important insight that the use of registers must conform to some constraints. In particular, our approach segments the firmware, locate code sections and output the instructions. We uses a masked language model to learn hiding relationships among the instructions to identify the function boundaries. We evaluate Moye using 1,318 monolithic firmware images, including 48 samples collected from widely used devices. The evaluation demonstrates that our approach significantly outperforms current works, achieving a precision greater than 98% and a recall rate greater than 97% across most datasets, showing robustness to complicated compilation options.

## 44. Neurosymbolic Modular Refinement Type Inference

**Authors:** Georgios Sakkas (UC San Diego), Pratyush Sahu (UC San Diego), Kyeling Ong (University of California, San Diego), Ranjit Jhala (University of California at San Diego)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029908

**中文总结:** 提出神经符号代理 XO，用大语言模型为 Haskell 包自动生成精炼类型注解并以 LiquidHaskell 验证，将原本需专家数天至数周的标注工作自动化。

**Abstract:** Refinement types -- a type-based generalization of Floyd-Hoare logics -- are an expressive and modular means of statically ensuring a wide variety of correctness, safety, and security properties of software. However, their expressiveness and modularity means that to use them, a developer must laboriously \emph{annotate} all the functions in their code with potentially complex type specifications that specify the contract for that function. We present XO, a neurosymbolic agent that uses LLMs to automatically generate refinement type annotations for all the functions in an entire package or module, using the refinement type checker LiquidHaskell as an oracle to verify the correctness of the generated specifications. We curate a dataset of three Haskell packages where refinement types are used to enforce a variety of correctness properties from data structure invariants to low-level memory safety and use this dataset to evaluate XO. Previously these packages required expert users several days to weeks to annotate with refinement types. Our evaluation shows that when even using models with relatively smaller models like the 3 billion parameter StarCoder LLM, by using fine-tuning, carefully chosen contexts, our neurosymbolic agent generates refinement types for up to 94\% of the functions across entire libraries automatically in just a few hours, thereby showing that LLMs can drastically shrink the human effort needed to use formal verification.

## 45. Patch Synthesis for Property Repair of Deep Neural Networks

**Authors:** Zhiming Chi (Institute of Software, Chinese Academy of Sciences), Jianan Ma (Hangzhou Dianzi University, China; Zhejiang University, Hangzhou, China), Pengfei Yang (Institute of Software at Chinese Academy of Sciences, China), Cheng-Chao Huang (Nanjing Institute of Software Technology, ISCAS), Renjue Li (Institute of Software at Chinese Academy of Sciences, China), Jingyi Wang (Zhejiang University), Xiaowei Huang (University of Liverpool), Lijun Zhang (Institute of Software, Chinese Academy of Sciences)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029971

**中文总结:** 提出 PatchPro，以可形式验证的补丁模块做 DNN 局部鲁棒性属性级修复，在保持原网性能的同时对邻域样本提供可证明的修复保证。

**Abstract:** Deep neural networks (DNNs) are prone to various dependability issues, such as adversarial attacks, which hinder their adoption in safety-critical domains. Recently, NN repair techniques have been proposed to address these issues while preserving original performance by locating and modifying guilty neurons and their parameters. However, existing repair approaches are often limited to specific data sets and do not provide theoretical guarantees for the effectiveness of the repairs. To address these limitations, we introduce PatchPro, a novel patch-based approach for property-level repair of DNNs, focusing on local robustness. The key idea behind PatchPro is to construct patch modules that, when integrated with the original network, provide specialized repairs for all samples within the robustness neighborhood while maintaining the network's original performance. Our method incorporates formal verification and a heuristic mechanism for allocating patch modules, enabling it to defend against adversarial attacks and generalize to other inputs. PatchPro demonstrates superior efficiency, scalability, and repair success rates compared to existing DNN repair methods, i.e., realizing provable property-level repair for 100% cases across multiple high-dimensional datasets.

## 46. Planning a Large Language Model for Static Detection of Runtime Errors in Code Snippets

**Authors:** Smit Soneshbhai Patel (University of Texas at Dallas), Aashish Yadavally (University of Texas at Dallas), Hridya Dhulipala (University of Texas at Dallas), Tien N. Nguyen (University of Texas at Dallas)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029953

**中文总结:** 提出 ORCA，引导 LLM 在控制流图上自主规划并模拟执行代码片段，以静态方式检测在线代码片段中的运行时错误。

**Abstract:** Large Language Models (LLMs) have been excellent in generating and reasoning about source code and the textual descriptions. They can recognize patterns, syntax, and semantics in code, making them effective in several software engineering tasks. However, they exhibit weaknesses in reasoning about the program execution. They primarily operate on static code representations, failing to capture the dynamic behavior and state changes that occur during program execution. In this paper, we advance the capabilities of LLMs in reasoning about program execution. We propose ORCA, a novel approach that instructs an LLM to autonomously formulate a plan to navigate through a control flow graph (CFG) for predictive execution of (in)complete code snippets. It acts as a predictive interpreter to ``execute'' the code. As a downstream task, we use ORCA to statically identify any runtime errors for online code snippets. Early detection of runtime errors and defects in these snippets is crucial to prevent costly fixes later in the development cycle after they were adapted into a codebase. In our novel technique, we guide the LLM to pause at the branching point, focusing on the state of the symbol tables for variables' values, thus minimizing error propagation in the LLM's computation. We also instruct the LLM not to stop at each step in its execution plan, resulting the use of only one prompt to the LLM, thus much cost-saving. Our empirical evaluation showed that ORCA is effective and improves over the state-of-the-art approaches in predicting the execution traces and in runtime error detection.

## 47. Preserving Privacy in Software Composition Analysis: A Study of Technical Solutions and Enhancements

**Authors:** Huaijin Wang (Ohio State University), Zhibo Liu (Hong Kong University of Science and Technology), Yanbo Dai (The Hong Kong University of Science and Technology (Guangzhou)), Shuai Wang (Hong Kong University of Science and Technology), Qiyi Tang (Tencent Security Keen Lab), Sen Nie (Tencent Security Keen Lab), Shi Wu (Tencent Security Keen Lab)

**Categories:** Program Analysis and Verification, Evolution and Maintenance, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029940

**中文总结:** 系统梳理软件成分分析（SCA）中的隐私保护技术方案，分析工业界“轻量本地 SCA”与远程深度分析在隐私、精度与厂商资产保护之间的权衡，并提出增强思路。

**Abstract:** Software composition analysis (SCA) denotes the process of identifying open-source software components in an input software application. SCA has been extensively developed and adopted by academia and industry. However, we notice that the modern SCA techniques in industry scenarios still need to be improved due to privacy concerns. Overall, SCA requires the users to upload their applications’ source code to a remote SCA server, which then deeply inspects the applications and reports the component usage to users. This process is privacy-sensitive since the applications may contain sensitive information, such as proprietary algorithms, trade secrets, and user data. Moreover, applications' source code is generally deemed proprietary, and users do not want to share it with the SCA vendor. To protect customers' privacy, contemporary SCA vendors often propose to deploy a "lite" version of SCA service on the customer side. To avoid the leakage of SCA vendors' valuable assets (e.g., code, model, and data), the "lite" SCA usually only performs a shallow analysis with limited accuracy. Privacy concerns have prevented the SCA technology from being used in real-world scenarios. Therefore, academia and the industry demand privacy-preserving SCA solutions. For the first time, we analyze the privacy requirements of SCA and provide a landscape depicting possible technical solutions with varying privacy gains and overheads. In particular, given that de facto SCA frameworks are primarily driven by code similarity-based techniques, we explore combining several privacy-preserving protocols to encapsulate the similarity-based SCA framework. Among all viable solutions, we find that multi-party computation (MPC) offers the strongest privacy guarantee and plausible accuracy; it, however, incurs high overhead ($184\times$). We optimize the MPC-based SCA framework by reducing the amount of crypto protocol transactions using program analysis techniques. The evaluation results show that our proposed optimizations can reduce the MPC-based SCA overhead to only 8.5% without sacrificing SCA’s privacy guarantee or accuracy.

## 48. QEDCartographer: Automating Formal Verification Using Reward-Free Reinforcement Learning

**Authors:** Alex Sanchez-Stern (University of Massachusetts at Amherst), Abhishek Varghese (University of Massachusetts), Zhanna Kaufman (University of Massachusetts), Shizhuo Zhang (University of Illinois Urbana-Champaign), Talia Lily Ringer (University of Illinois Urbana-Champaign), Yuriy Brun (University of Massachusetts)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029816

**中文总结:** 提出 QEDCartographer，结合监督与强化学习并利用证明分支结构做无奖励搜索以自动合成 Coq 证明；在 CoqGym 上比基线多证明 186 个定理。

**Abstract:** Formal verification is a promising method for producing highly reliable software, but the difficulty of manually writing verification proofs severely limits its utility in practice. Recent methods have automated some proof synthesis by guiding a search through the proof space using machine learning and a theorem prover. Unfortunately, the theorem prover provides only the crudest estimate of progress, resulting in effectively undirected search. This makes proofs hard to find, and, when they are found, longer than necessary. Reinforcement learning could help estimate progress, but sparse rewards make this method ineffective. To address this problem, we create QEDCartographer, an novel automated proof-synthesis tool that combines supervised and reinforcement learning. QEDCartographer's key insight is that incorporating the branching structure of proofs into its learning enables reward-free search, mitigating the sparse reward challenge. We evaluate QEDCartographer on the CoqGym benchmark of 68,501 theorems from 124 open-source Coq projects. QEDCartographer proves 186 more theorems than Proverbot9001, a state-of-the-art proof synthesis tool, an increase of 8%. Further, the tools are complementary, together proving 12% more theorems than Proverbot9001 alone. For theorems both can prove, QEDCartographer produces 26% shorter proofs 27% faster.

## 49. Rango: Adaptive Retrieval-Augmented Proving for Automated Software Verification

**Authors:** Kyle Thompson (University of California, San Diego), Nuno Saavedra (INESC-ID and IST, University of Lisbon), Pedro Carrott (Imperial College London), Kevin Fisher (University of California San Diego), Alex Sanchez-Stern (University of Massachusetts), Yuriy Brun (University of Massachusetts), João F. Ferreira (INESC-ID and IST, University of Lisbon), Sorin Lerner (University of California at San Diego), Emily First (University of California, San Diego)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029818

**中文总结:** 提出 Coq 自动证明合成工具 Rango，每步检索相关前提与项目内相似证明并自适应微调 LLM 上下文；发布 CoqStoq 数据集，在基准上合成 27.7% 证明，较先前方法多 10%。

**Abstract:** Formal verification using proof assistants, such as Coq, allows for high-quality software. However, the verification process is expensive, requiring significant expertise and manual effort to write proofs. Recent work has explored automating proof synthesis using machine learning, and even more recently, large language models (LLMs), showing that retrieving relevant premises (such as lemmas and definitions) is helpful for these models. We present Rango, a fully automated proof synthesis tool for Coq that uses, not only relevant premises but also similar proofs from the current project. Rango uses retrieval augmentation at every step of the proof to automatically determine which proofs and premises to include in the context of its fine-tuned LLM. In this way, Rango adapts to the project _and_ to the evolving state of the proof. We create a new dataset, CoqStoq, of 2,205 open-source Coq projects from GitHub, which includes both training data and a curated evaluation benchmark of well-maintained projects. On this benchmark, Rango synthesizes 27.7% of the proofs, which is 10% more proofs than prior state-of-the-art tool Tactician. Our evaluation also shows that adding relevant proofs to the context in Rango leads to a 45% increase in the number of theorems proven.

## 50. Ranking Relevant Tests for Order-Dependent Flaky Tests

**Authors:** Shanto Rahman (The University of Texas at Austin), Bala Naren Chanumolu (George Mason University), Suzzana Rafi (George Mason University), August Shi (The University of Texas at Austin), Wing Lam (George Mason University)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029933

**中文总结:** 提出 RankF，按测试成为顺序依赖 flaky 测试相关测试的可能性排序，帮助开发者更快定位首个顺序相关测试。

**Abstract:** One major challenge of regression testing is the presence of flaky tests, i.e., tests that may pass in one run but fail in another run for the same version of code. One prominent category of flaky tests are order-dependent (OD) flaky tests, which are tests that can pass or fail depending on the test-order in which the tests are run. To help developers debug and fix OD tests, prior work has attempted to automatically find OD-relevant tests, i.e., tests that will determine whether an OD test passes or fails depending on whether the OD-relevant tests are run before or after the OD test in the test-order. Prior work finds OD-relevant tests by running tests before the OD test, without regards to the tests’ likelihood of being OD-relevant tests. We propose RankF to rank tests in order of likelihood of being OD-relevant tests, so a developer can find the first OD-relevant test more quickly, without running tests as often. We propose two ranking approaches, each requiring different information. Our first approach, RankFL, relies on training a large-language model that analyzes test code. Our second approach, RankFO, relies on the analysis of prior test-order execution information. We evaluate our approaches on 155 OD tests from 34 modules across 24 open-source projects. We compare RankF against prior work baselines in terms of the time for finding the first OD-relevant test for an OD test. RankF on average finds the first OD-relevant test faster than the best of the baselines, providing speedups of 1.9X, 1.7X, and 2.6X for the three different types of OD-relevant tests we evaluate.

## 51. RepairAgent: An Autonomous, LLM-Based Agent for Program Repair

**Authors:** Islem BOUZENIA (University of Stuttgart), Prem Devanbu (University of California at Davis), Michael Pradel (University of Stuttgart)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029914

**中文总结:** 提出首个基于 LLM 的自主程序修复智能体 RepairAgent，可自主规划并调用工具收集信息、生成修复并验证，在 Defects4J 上取得优异修复效果。

**Abstract:** Automated program repair has emerged as a powerful technique to mitigate the impact of software bugs on system reliability and user experience. This paper introduces RepairAgent, the first work to address the program repair challenge through an autonomous agent based on a large language model (LLM). Unlike existing deep learning-based approaches, which prompt a model with a fixed prompt or in a fixed feedback loop, our work treats the LLM as an agent capable of autonomously planning and executing actions to fix bugs by invoking suitable tools. RepairAgent freely interleaves gathering information about the bug, gathering repair ingredients, and validating fixes, while deciding which tools to invoke based on the gathered information and feedback from previous fix attempts. Key contributions that enable RepairAgent include a set of tools that are useful for program repair, a dynamically updated prompt format that allows the LLM to interact with these tools, and a finite state machine that guides the agent in invoking the tools. Our evaluation on the popular Defects4J dataset demonstrates RepairAgent’s effectiveness in autonomously repairing 164 bugs, including 39 bugs not fixed by prior techniques. Interacting with the LLM imposes an average cost of 270,000 tokens per bug, which, under the current pricing of OpenAI’s GPT-3.5 model, translates to 14 cents per bug. To the best of our knowledge, this work is the first to present an autonomous, LLM-based agent for program repair, paving the way for future agent-based techniques in software engineering.

## 52. Revisiting Unnaturalness for Automated Program Repair in the Era of Large Language Models

**Authors:** Aidan Z.H. Yang (Carnegie Mellon University), Sophia Kolak (Carnegie Mellon University), Vincent J. Hellendoorn (Carnegie Mellon University), Ruben Martins (Carnegie Mellon University), Claire Le Goues (Carnegie Mellon University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029753

**中文总结:** 利用大语言模型熵值改进自动程序修复的缺陷定位、补丁生成与排序，仅依赖上下文前缀后缀以降低训练数据泄露风险。

**Abstract:** Language models have improved by orders of magnitude with the recent emergence of Transformer-based Large Language Models (LLMs). LLMs have demonstrated their ability to generate "natural" code that is highly similar to code written by professional developers. One intermediate value an LLM can emit is entropy, which measures the naturalness of a token of code. We hypothesize that entropy can be used to improve the performance of Automated Program Repair (APR) tasks. While much progress has been made in Automated Program Repair (APR), fault localization techniques suffer from a lack of diversity in ranking scores, patch generation tools tend to be inefficient as all tests need to run before determining if a patch is likely to be correct, and patch ranking often suffers from the test-suite over-fitting problem. However, using an LLM directly for APR introduces concerns for training data leakage. In this work, we introduce a novel way of using the entropy of LLMs in combination with prior APR tools to improve all stages of APR. By using only the prefix and suffix context of a line or block of code to describe naturalness, we can use LLMs to localize faults and rank patches all while eliminating the dependency for test-suites. We show that entropy is highly complementary with prior fault localization tools. Our proposed method achieves a 108% top-1 score improvement over SBFL. When using entropy for patch ranking and classification, our proposed method can rank correct patches more effectively than state-of-the-art machine learning tools with an 49% improvement in top-1. Our work suggests that LLMs can be an effective addition to compliment prior APR tasks while minimizing both the test-suite over-fitting problem and the LLM data leakage problem.

## 53. ROCODE: Integrating Backtracking Mechanism and Program Analysis in Large Language Models for Code Generation

**Authors:** Xue Jiang, Yihong Dong (Peking University), Yongding Tao (University of Electronic Science and Technology of China), Huanyu Liu (Xidian University), Zhi Jin (Peking University), Ge Li (Peking University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029868

**中文总结:** 提出 ROCODE，在 LLM 代码生成过程中集成回溯机制与程序分析，一旦出错立即回滚修正而非事后修订，避免自回归生成中错误累积与资源浪费。

**Abstract:** Large language models (LLMs) have achieved impressive performance in code generation recently, offering programmers revolutionary assistance in software development. However, due to the auto-regressive nature of LLMs, they are susceptible to error accumulation during code generation. Once an error is produced, LLMs can merely continue to generate the subsequent code conditioned on it, given their inability to adjust previous outputs. This generation process differs from the common practice in human coding, which involves review and adjustment during the coding process according to quality and requirements. Existing LLM-based approaches that typically consider post-revising after code generation fail to resolve errors in time, leading to the challenging resolution of accumulated errors and the significant wastage of resources. Ideally, LLMs should rollback and resolve the occurred error immediately during code generation, rather than proceed on the basis of the error and wait for post-revising after generation. In this paper, we propose \ourapproachbf, which integrates the backtracking mechanism and program analysis into LLMs for code generation. Specifically, we employ program analysis to perform incremental error detection during the generation process. When an error is detected, the backtracking mechanism is triggered to priming rollback strategies and constraint regeneration, thereby avoiding the recurrence of the same error. Experiments on multiple code generation benchmarks show that \ourapproachbf can significantly reduce the errors generated by LLMs, with a compilation pass rate of over 98.9\%. The test pass rate is improved by up to 23.8\% compared to the best baseline approach. Compared to the post-revising baseline, the cost is reduced by 19.3\%. Moreover, our approach is model-agnostic and achieves consistent improvements across six LLMs.

## 54. Selecting Initial Seeds for Better JVM Fuzzing

**Authors:** Tianchang Gao (Tianjin University), Junjie Chen (Tianjin University), Dong Wang (Tianjin University), Yile Guo (College of Intelligence and Computing, Tianjin University), Yingquan Zhao (Tianjin University), Zan Wang (Tianjin University)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029820

**中文总结:** 设计 10 种 JVM fuzz 初始种子选择方法（覆盖、预 fuzz、程序特征等），并在 3 个 JVM 实现上与 JavaTailor、VECT 做系统实证比较。

**Abstract:** JVM fuzzing techniques serve as a cornerstone for guaranteeing the quality of implementations. In typical fuzzing workflows, initial seeds are crucial as they form the basis of the process. Literature in traditional program fuzzing has confirmed that effectiveness is largely impacted by redundancy among initial seeds, thereby proposing a series of seed selection methods. JVM fuzzing, compared to traditional ones, presents unique characteristics, including large-scale and intricate code, and programs with both syntactic and semantic features. However, it remains unclear whether the existing initial seed selection methods are suitable for JVM fuzzing and whether utilizing program features can enhance effectiveness. To address this, we devised a total of 10 initial seed selection methods, comprising coverage-based, prefuzz-based, and program-feature-based methods. We then conducted an empirical study on three JVM implementations to extensively evaluate the performance of the initial seed selection methods within two state-of-the-art fuzzing techniques (JavaTailor and VECT). Specifically, we examine performance from three aspects: (i) effectiveness and efficiency using widely studied initial seeds, (ii) effectiveness using the programs in the wild, and (iii) the ability to detect new bugs. Evaluation results first show that the program-feature-based method that utilizes the control flow graph not only has a significantly lower time overhead (i.e., 30s), but also outperforms other methods, achieving 142% to 269% improvement compared to the full set of initial seeds. Second, results reveal that the initial seed selection greatly improves the quality of wild programs and exhibits complementary effectiveness by detecting new behaviors. Third, results demonstrate that given the same testing period, initial seed selection improves the JVM fuzzing techniques by detecting more unknown bugs. Particularly, 16 out of the 25 detected bugs have been confirmed or fixed by developers. This work takes the first look at initial seed selection in JVM fuzzing, confirming its importance in fuzzing effectiveness and efficiency.

## 55. SmartReco: Detecting Read-Only Reentrancy via Fine-Grained Cross-DApp Analysis

**Authors:** Jingwen Zhang (School of Software Engineering, Sun Yat sen University), Zibin Zheng (Sun Yat-sen University), Yuhong Nan (Sun Yat-sen University), Mingxi Ye (Sun Yat-sen University), Kaiwen Ning (Sun Yat-sen University), Yu Zhang (Harbin Institute of Technology), Weizhe Zhang (Harbin Institute of Technology)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029779

**中文总结:** 提出 SmartReco 框架，通过跨 DApp 静动态分析检测只读重入漏洞；该漏洞三年已致 DApp 生态约 3000 万美元损失。

**Abstract:** Despite the increasing popularity of Decentralized Applications (DApps), they are suffering from various vulnerabilities that can be exploited by adversaries for profits. Among such vulnerabilities, Read-Only Reentrancy (called ROR in this paper), is an emerging type of vulnerability that arises from the complex interactions between DApps. In recent three years, attack incidents of ROR have already caused around 30M USD losses to the DApp ecosystem. Existing techniques for vulnerability detection in smart contracts can hardly detect Read-Only Reentrancy attacks, due to the lack of tracking and analyzing the complex interactions between multiple DApps. In this paper, we propose SmartReco, a new framework for detecting Read-Only Reentrancy vulnerability in DApps through a novel combination of static and dynamic analysis (i.e., fuzzing) over smart contracts. The key design behind SmartReco is threefold: (1) SmartReco identifies the boundary between different DApps from the heavy-coupled cross-contract interactions. (2) SmartReco performs fine-grained static analysis to locate points of interest (i.e., entry functions) that may lead to ROR. (3) SmartReco utilizes the on-chain transaction data and performs multi-function fuzzing (i.e., the entry function and victim function) across different DApps to verify the existence of ROR. Our evaluation of a manual-labeled dataset with 45 RORs shows that SmartReco achieves an accuracy of 88.63% and a recall of 86.36%. In addition, SmartReco successfully detects 43 new RORs from 123 popular DApps. The total assets affected by such RORs reach around 520,000 USD.

## 56. SpecGen: Automated Generation of Formal Program Specifications via Large Language Models

**Authors:** Lezhi Ma (Nanjing University), Shangqing Liu (Nanyang Technological University), Yi Li (Nanyang Technological University), Xiaofei Xie (Singapore Management University), Lei Bu (Nanjing University)

**Categories:** AI for Software Engineering, Program Analysis and Verification, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029962

**中文总结:** 提出 SpecGen，利用 LLM 代码理解能力通过对话式两阶段流程自动生成复杂程序的形式化规范，摆脱对预定义模板与语法的依赖。

**Abstract:** In the software development process, formal program specifications play a crucial role in various stages, including requirement analysis, software testing, and verification. However, manually crafting formal program specifications is rather difficult, making the job time-consuming and labor-intensive. Moreover, it is even more challenging to write specifications that correctly and comprehensively describe the semantics of complex programs. To reduce the burden on software developers, automated specification generation methods have emerged. However, existing methods usually rely on predefined templates or grammar, making them struggle to accurately describe the behavior and functionality of complex real-world programs. To tackle this challenge, we introduce SpecGen, a novel technique for formal program specification generation based on Large Language Models (LLMs). Our key insight is to overcome the limitations of existing methods by leveraging the code comprehension capability of LLMs. The process of SpecGen consists of two phases. The first phase employs a conversational approach that guides the LLM to generate appropriate specifications for a given program, aiming to utilize the ability of LLM to generate high-quality specifications. The second phase, designed for where the LLM fails to generate correct specifications, applies four mutation operators to the model-generated specifications and selects verifiable specifications from the mutated ones through a novel heuristic selection strategy by assigning different weights of variants in an efficient manner. We evaluate SpecGen on two datasets, including the SV-COMP Java category benchmark and a manually constructed dataset containing 120 programs. Experimental results demonstrate that SpecGen succeeds in generating verifiable specifications for 279 out of 385 programs, outperforming the existing LLM-based approaches and conventional specification generation tools like Houdini and Daikon. Further investigations on the quality of generated specifications indicate that SpecGen can comprehensively articulate the behaviors of the input program.

## 57. Static Analysis of Remote Procedure Call in Java Programs

**Authors:** Baoquan Cui (Institute of Software at Chinese Academy of Sciences, China), RongQu (State Key Laboratory of Computer Science, Institute of Software Chinese Academy of Sciences, University of Chinese Academy of Sciences, Beijing, China), Zhen Tang (Key Laboratory of System Software (Chinese Academy of Sciences), State Key Laboratory of Computer Science, Institute of Software Chinese Academy of Sciences, University of Chinese Academy of Sciences, Beijing, China), Jian Zhang (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029756

**中文总结:** 提出 RPCBridge，以适配器统一建模 Java RPC 框架的基本操作并用逻辑规则精确刻画 RPC 语义，实现 Java 程序中远程过程调用的静态分析与客户端—服务端关联建立。

**Abstract:** The Remote Procedure Call (RPC) is commonly used for inter-process communications over network, allowing a program to invoke a procedure in another address space even another machine as if it were a local call within the same address space. Its convenience comes from encapsulating network communication. However, for the same reason, it cannot be penetrated by current static analyzers. Since the RPC programs/frameworks play a more important role in various domains, the static analysis of RPC is significant and cannot be ignored. We have observed that many of the existing RPC frameworks/programs written in Java are based on explicit protocols, which makes them possible to be modelled for static analysis. The challenges are how to identify RPC operations in different frameworks/programs and how to automatically establish relationships between clients and servers. In this paper, we propose a novel approach, RPCBridge, which uses an adapter to unify the most basic operations during the RPC process. It models the RPC with logic rules in a straightforward and precise way based on its semantics, performs points-to analysis and constructs RPC edges in the call graph, making it more complete. The evaluation on real-world large-scale Java programs based on 5 common RPC frameworks shows that our approach can effectively capture the operations of the RPC (263 matched protocols and 1,098 RPCs), and construct critical links (2,578 edges in the call graph) between clients and servers, in which 60.1% are the true caller-callee pairs after execution. Our approach is expected to bring significant benefits (+24.3% leakage paths for the taint analyzer) for previously incompletely modelled code with a very little memory and time overhead, and connect the modules in a system, so that it can be statically analyzed more holistically.

## 58. TacDroid: Detection of Illicit Apps through Hybrid Analysis of UI-based Transition Graphs

**Authors:** Yanchen Lu (Zhejiang University), Hongyu Lin (Zhejiang University), Zehua He (Zhejiang University), Haitao Xu (Zhejiang University), Zhao Li (Hangzhou Yugu Technology), Shuai Hao (Old Dominion University), Liu Wang (Beijing University of Posts and Telecommunications), Haoyu Wang (Huazhong University of Science and Technology), Kui Ren (Zhejiang University)

**Categories:** Program Analysis and Verification, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029913

**中文总结:** 提出 TacDroid，融合动态与静态分析构建 UI 转移图，检测依赖动态资源加载的非法应用（色情、赌博、诈骗等）。

**Abstract:** Illicit apps have emerged as a thriving underground industry, driven by their substantial profitability. These apps either offer users restricted services (e.g., porn and gambling) or engage in fraudulent activities like scams. Despite the widespread presence of illicit apps, scant attention has been directed towards this issue, with several existing detection methods predominantly relying on static analysis alone. However, given the burgeoning trend wherein an increasing number of mobile apps achieve their core functionality through dynamic resource loading, depending solely on static analysis proves inadequate. To address this challenge, in this paper, we introduce TacDroid, a novel approach that integrates dynamic analysis for dynamic content retrieval with static analysis to mitigate the limitations inherent in both methods, i.e., the low coverage of dynamic analysis and the low accuracy of static analysis. Specifically, TacDroid conducts both dynamic and static analyses on an Android app to construct dynamic and static User Interface Transition Graphs (UTGs), respectively. These two UTGs are then correlated to create an intermediate UTG. Subsequently, TacDroid embeds graph structure and utilizes an enhanced Graph Autoencoder (GAE) model to predict transitions between nodes. Through link prediction, TacDroid effectively eliminates false positive transition edges stemming from misjudgments in static analysis and supplements false negative transition edges overlooked in the intermediate UTG, thereby generating a comprehensive and accurate UTG. Finally, TacDroid determines the legitimacy of an app and identifies its category based on the app's UTG. Our evaluation results highlight the outstanding accuracy of TacDroid in detecting illicit apps. It significantly surpasses the state-of-the-art work, achieving an F1-score of 96.73%. This work represents a notable advancement in the identification and categorization of illicit apps.

## 59. The Fact Selection Problem in LLM-Based Program Repair

**Authors:** Nikhil Parasaram (Uber Amsterdam), Huijie Yan (University College London), Boyu Yang (University College London), Zineb Flahy (University College London), Abriele Qudsi (University College London), Damian Ziaber (University College London), Earl T. Barr (University College London), Sergey Mechtaev (Peking University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029841

**中文总结:** 对 314 个 Python 缺陷开展 1.9 万余次提示实验，揭示七种缺陷相关事实对 LLM 程序修复均有益但事实数量与效果呈非单调关系。

**Abstract:** Recent research has shown that incorporating bug- related facts, such as stack traces and GitHub issues, into prompts enhances the bug-fixing capabilities of large language models (LLMs). Considering the ever-increasing context window of these models, a critical question arises: what and how many facts should be included in prompts to maximise the chance of correctly fixing bugs? To answer this question, we conducted a large-scale study, employing over 19K prompts featuring various combinations of seven diverse facts to rectify 314 bugs from open-source Python projects within the BugsInPy benchmark. Our findings revealed that each fact, ranging from simple syntactic details like code context to semantic information previously unexplored in the context of LLMs such as angelic values, is beneficial. Specifically, each fact aids in fixing some bugs that would remain unresolved or only be fixed with a low success rate without it. Importantly, we discovered that the effectiveness of program repair prompts is non-monotonic over the number of used facts; using too many facts leads to subpar outcomes. These insights led us to define the fact selection problem: determining the optimal set of facts for inclusion in a prompt to maximise LLM’s performance on a given task instance. We found that there is no one-size- fits-all set of facts for bug repair. Therefore, we developed a basic statistical model, named MANIPLE, which selects facts specific to a given bug to include in the prompt. This model significantly surpasses the performance of the best generic fact set. To underscore the significance of the fact selection problem, we benchmarked MANIPLE against the state-of-the-art zero-shot, non- conversational LLM-based bug repair methods. On our testing dataset of 157 bugs, MANIPLE repairs 88 bugs, 17% above the best configuration.

## 60. TIGER: A Generating-Then-Ranking Framework for Practical Python Type Inference

**Authors:** Chong Wang (Nanyang Technological University), Jian Zhang (Nanyang Technological University), Yiling Lou (Fudan University), Mingwei Liu (Fudan University), Weisong Sun (Nanyang Technological University), Yang Liu (Nanyang Technological University), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029957

**中文总结:** 提出 TIGER 生成—排序两阶段 Python 类型推断框架，微调生成与相似度模型；在用户/库自定义类型 Top-5 准确率分别提升 11.2% 与 20.1%。

**Abstract:** Python’s dynamic typing system offers flexibility and expressiveness but can lead to type-related errors, prompting the need for automated type inference despite efforts like Python Enhancement Proposals (PEPs) to enhance type hinting. While existing learning-based approaches show promising inference accuracy, they struggle with practical challenges in comprehensively handling various types, including complex generics and (unseen) user/library-defined types. To address these challenges, we introduce TIGER, employing a two-stage generating-then-ranking (GTR) framework. By fine-tuning pre-trained code models, TIGER trains a generation model with a generative span masking objective and a similarity model with a contrastive training objective. This enables TIGER to execute the GTR inference, generating diverse candidates and then ranking them alongside user/library-defined types. Evaluation on the ManyTypes4Py dataset demonstrates TIGER’s effectiveness across different type categories, particularly excelling in (unseen) user-defined types (with improvements of 11.2% and 20.1% in Top-5 Exact Match). The evaluation results also confirm the robustness and efficiency of TIGER, highlighting the contributions of the employed two stages.

## 61. Toward a Better Understanding of Probabilistic Delta Debugging

**Authors:** Mengxiao Zhang, Zhenyang Xu (University of Waterloo), Yongqiang Tian, Xinru Cheng (University of Waterloo), Chengnian Sun (University of Waterloo)

**Categories:** Testing and Quality, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029925

**中文总结:** 首次对概率 Delta Debugging 算法 ProbDD 做深入理论分析，简化其概率模型并阐明概率与子集规模变化趋势，辅以成功率、消融与权衡实验验证其优势与局限。

**Abstract:** Given a list L of elements and a property ψ that L exhibits, ddmin is a classic test input minimization algorithm that aims to automatically remove ψ-irrelevant elements from L. This algorithm has been widely adopted in domains such as test input minimization and software debloating. Recently, ProbDD, a variant of ddmin, has been proposed and achieved stateof- the-art performance. By employing Bayesian optimization, ProbDD estimates the probability of each element in L being relevant to ψ, and statistically decides which and how many elements should be deleted together each time. However, the theoretical probabilistic model of ProbDD is rather intricate, and the underlying details for the superior performance of ProbDD have not been adequately explored. In this paper, we conduct the first in-depth theoretical analysis of ProbDD, clarifying the trends in probability and subset size changes and simplifying the probability model. We complement this analysis with empirical experiments, including success rate analysis, ablation studies, and examinations of trade-offs and limitations, to further comprehend and demystify this state-of- the-art algorithm. Our success rate analysis reveals how ProbDD effectively addresses bottlenecks that slow down ddmin by skipping inefficient queries that attempt to delete complements of subsets and previously tried subsets. The ablation study illustrates that randomness in ProbDD has no significant impact on efficiency. These findings provide valuable insights for future research and applications of test input minimization algorithms. Based on the findings above, we propose CDD, a simplified version of ProbDD, reducing the complexity in both theory and implementation. CDD assists in 1 validating the correctness of our key findings, e.g., that probabilities in ProbDD essentially serve as monotonically increasing counters for each element, and 2 identifying the main factors that truly contribute to ProbDD’s superior performance. Our comprehensive evaluations across 76 benchmarks in test input minimization and software debloating demonstrate that CDD can achieve the same performance as ProbDD, despite being much simplified.

## 62. Tumbling Down the Rabbit Hole: How do Assisting Exploration Strategies Facilitate Grey-box Fuzzing?

**Authors:** Mingyuan Wu (Southern University of Science and Technology), Jiahong Xiang (Southern University of Science and Technology), Kunqiu Chen (Southern University of Science and Technology), Peng Di (Ant Group & UNSW Sydney), Shin Hwei Tan (Concordia University), Heming Cui (University of Hong Kong), Yuqun Zhang (Southern University of Science and Technology)

**Categories:** Testing and Quality, Program Analysis and Verification

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029740

**中文总结:** 首次全面评估 9 种灰盒 fuzz 辅助探索策略在 21 个真实项目上的效果、通用性与局限，为后续策略设计提供统一基准与洞察。

**Abstract:** Many assisting exploration strategies have been proposed to assist grey-box fuzzers in exploring program states guarded by tight and complex branch conditions such as equality constraints. Although they have shown promising results in their original papers, their evaluations seldom follow equivalent protocols, e.g., they are rarely evaluated on identical benchmarks. Moreover, there is a lack of sufficient investigations on the specifics of the program states explored by these strategies which can obfuscate the future application and development of such strategies. Consequently, there is a pressing need for a comprehensive study of assisting exploration strategies on their effectiveness, versatility, and limitations to enlighten their future development. To this end, we perform the first comprehensive study about the assisting exploration strategies for grey-box fuzzers. Specifically, we first collect nine recent fuzzers representing the mainstream assisting exploration strategies as our studied subjects and 21 real-world projects to form our benchmark suite. After evaluating the subjects on the benchmark suite, we then surprisingly find that the dictionary strategy is the most promising since it not only achieves similar or even slightly better performance over the other studied assisting exploration strategies in terms of exploring program states but also is more practical to be enhanced. Accordingly, we propose CDFUZZ, which generates a customized dictionary for each seed upon the baseline fuzzer AFL to improve over the original dictionary strategy. The evaluation results demonstrate that CDFUZZ increases the edge coverage by 16.1% on average for all benchmark projects over the best performer in our study (i.e., AFL++ with the dictionary strategy). CDFUZZ also successfully exposed 37 previously unknown bugs, with nine confirmed and seven fixed by the corresponding developers.

## 63. Unavoidable Boundary Conditions: A Control Perspective on Goal Conflicts

**Authors:** Sebastian Uchitel (Universidad de Buenos Aires / Imperial College), Francisco Cirelli (Universidad de Buenos Aires), Dalal Alrajeh (Imperial College London)

**Categories:** Program Analysis and Verification, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029722

**中文总结:** 从反应式合成视角提出更强「不可避免边界条件」(UBC) 定义以精简需求冲突边界条件，实验显示能显著减少无关条件并关联 unrealizable core 等概念。

**Abstract:** Boundary Conditions (BCs) express situations under which requirements specifications conflict. They are used within a broader conflict management process to produce less idealized specifications. Several approaches have been proposed to identify BCs automatically. Some introduce a prioritization criteria to reduce the number of BCs presented to an engineer. However, identifying the few, relevant boundary conditions remains an open challenge. In this paper, we argue that one of the problems of the state of the art is with the definition of BC itself -- it is too weak. We propose a stronger definition for the few, relevant BCs, which we refer to as Unavoidable Boundary Conditions (UBCs), which utilizes the notion of realizability in reactive synthesis. We show experimentally that UBCs non-trivially reduce the number of conditions produced by existing BC identification techniques. We also relate UBCs to existing concepts in reactive synthesis used to provide feedback for unrealizable specifications (including counter-strategies and unrealizable cores). We then show that UBCs provide a targeted form of feedback for repairing unrealizable specifications.

## 64. When Quantum Meets Classical: Characterizing Hybrid Quantum-Classical Issues Discussed in Developer Forums

**Authors:** Jake Zappin (William and Mary), Trevor Stalnaker (William & Mary), Oscar Chaparro (William & Mary), Denys Poshyvanyk (William & Mary)

**Categories:** Program Analysis and Verification, Human and Social Aspects, Mining Software Repositories

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029802

**中文总结:** 对 531 个开发者论坛问题进行首个混合量子-经典计算实证研究，构建涵盖软件故障、硬件失败、库错误与开发者失误的分类体系。

**Abstract:** Recent advances in quantum computing have sparked excitement that this new computing paradigm could solve previously intractable problems. However, due to the faulty nature of current quantum hardware and quantum-intrinsic noise, the full potential of quantum computing is still years away. Hybrid quantum-classical computing has emerged as a possible compromise that achieves the best of both worlds. In this paper, we look at hybrid quantum-classical computing from a software engineering perspective and present the first empirical study focused on characterizing and evaluating recurrent issues faced by developers of hybrid quantum-classical applications. The study comprised a thorough analysis of 531 real-world issues faced by developers -- including software faults, hardware failures, quantum library errors, and developer mistakes -- documented in discussion threads from forums dedicated to quantum computing. By qualitatively analyzing such forum threads, we derive a comprehensive taxonomy of recurring issues in hybrid quantum-classical applications that can be used by both application and platform developers to improve the reliability of hybrid applications. The study considered how these recurring issues manifest and their causes, determining that hybrid applications are crash-dominant (74% of studied issues) and that errors were predominantly introduced by application developers (70% of issues). We conclude by identifying recurring obstacles for developers of hybrid applications and actionable recommendations to overcome them.
