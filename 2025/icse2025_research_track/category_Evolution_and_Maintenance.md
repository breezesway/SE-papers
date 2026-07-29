# ICSE 2025 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 42 papers

## 1. A First Look at Conventional Commits Classification

**Authors:** Qunhong Zeng (Beijing Institute of Technology), Yuxia Zhang (Beijing Institute of Technology), Zhiqing Qiu (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029726

**中文总结:** 初步研究 Conventional Commits 规范在 GitHub 上的采用现状与问题，并探索自动细粒度提交分类以填补相对 Swanson 三分类的知识空白。

**Abstract:** Modern distributed software development relies on commits to control system versions. Commit classification plays a vital role in both industry and academia. The widely-used commit classification framework was proposed in 1976 by Swanson and includes three base classes: perfective, corrective, and adaptive. With the increasing complexity of software development, the industry has shifted towards a more fine-grained commit category, i.e., adopting Conventional Commits Specification (CCS) for delicacy management. The new commit framework requires developers to classify commits into ten distinct categories, such as ``feat'', ``fix'', and ``docs''. However, existing studies mainly focus on the three-category classification, leaving the definition and application of the fine-grained commit categories as knowledge gaps. This paper reports a preliminary study on this mechanism from its application status and problems. We also explore ways to address these identified problems. We find that a growing number of projects on GitHub are adopting CCS. By analyzing 194 issues from GitHub and 100 questions from Stack Overflow about the CCS application, we qualitatively categorized 52 challenges developers encountered. The most common one is CCS-type confusion. To address these challenges, we propose a clear definition of CCS types based on existing variants. Further, we designed an approach to automatically classify commits into CCS types, and the evaluation results demonstrate a promising performance. Our work facilitates a deeper comprehension of the present fine-grained commit categorization and holds the potential to alleviate application challenges significantly.

## 2. ADAMAS: Adaptive Domain-Aware Performance Anomaly Detection in Cloud Service Systems

**Authors:** Wenwei Gu (The Chinese University of Hong Kong), Jiazhen Gu (Chinese University of Hong Kong), Jinyang Liu (Chinese University of Hong Kong), Zhuangbin Chen (Sun Yat-sen University), Jianping Zhang (The Chinese University of Hong Kong), Jinxi Kuang (The Chinese University of Hong Kong), Cong Feng (Huawei Cloud Computing Technology), Yongqiang Yang (Huawei Cloud Computing Technology), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029821

**中文总结:** 提出 ADAMAS 自适应 AutoML 云性能异常检测框架，结合无监督模型搜索与轻量人机协同弥合技术告警与业务影响差距。

**Abstract:** A common practice in the reliability engineering of cloud services involves the collection of monitoring metrics, followed by comprehensive analysis to identify performance issues. However, existing methods often fall short of detecting diverse and evolving anomalies across different services. Moreover, there exists a significant gap between the technical and business interpretation of anomalies, i.e., a detected anomaly may not have an actual impact on system performance or user experience. To address these challenges, we propose ADAMAS, an adaptive AutoML-based anomaly detection framework aiming to achieve practical anomaly detection in production cloud systems. To improve the ability of detecting cross-service anomalies, we design a novel unsupervised evaluation function to facilitate the automatic searching of the optimal model structure and parameters. ADAMAS also contains a lightweight human-in-the-loop design, which can efficiently incorporate expert knowledge to adapt to the evolving anomaly patterns and bridge the gap between predicted anomalies and actual business exceptions. Furthermore, through monitoring the rate of mispredicted anomalies, ADAMAS proactively re-configures the optimal model, forming a continuous loop of system improvement. Extensive evaluation on one public and two industrial datasets shows that ADAMAS outperforms all baseline models with a 0.891 F1-score. The ablation study also proves the effectiveness of the evaluation function design and the incorporation of expert knowledge.

## 3. An Empirical Study on Package-Level Deprecation in Python Ecosystem

**Authors:** Zhiqing Zhong (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Shilin He (Microsoft Research), Haoxuan Wang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), BoXi Yu (The Chinese University of Hong Kong, Shenzhen), Haowen Yang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** Evolution and Maintenance, Human and Social Aspects, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029884

**中文总结:** 混合方法实证研究 Python 生态包级 deprecation 的发布、接收与处理现状、对不活跃包的益处及开发者面临的挑战。

**Abstract:** Open-source software (OSS) plays a crucial role in modern software development. Utilizing OSS code can greatly accelerate software development, reduce redundancy, and enhance reliability. Python, a widely adopted programming language, is particularly renowned for its extensive and diverse third-party package ecosystem. However, a significant number of OSS packages within the Python ecosystem are in poor maintenance, leading to potential risks in terms of functionality and security. Consequently, it is essential to establish a deprecation mechanism that assists package developers and users in effectively managing these packages. To facilitate the establishment of the package-level deprecation mechanism, this paper presents a mixed-method empirical study, including data analysis and surveys. We investigate the current practices of announcing, receiving, and handling package-level deprecation in the Python ecosystem. We also assess the benefits of having deprecation announcements for inactively maintained packages. Furthermore, we investigate the challenges faced by package developers and users and their expectations for future deprecation practices. Our findings reveal valuable insights. For instance, 75.4\% of inactive package developers have no intention of releasing deprecation declarations for various reasons, while 89.5\% of users express a desire to be notified about the deprecation, highlighting a gap between developers and users; In many cases, no alternative solutions are available when deprecation occurs, emphasizing the need to explore practical approaches that enable seamless package handover and require less maintenance effort. We anticipate that our work will enhance the understanding of existing package-level deprecation patterns within the Python OSS realm and facilitate the development of deprecation practices for the Python community in the future.

## 4. Automated Test Generation For Smart Contracts via On-Chain Test Case Augmentation and Migration

**Authors:** Jiashuo Zhang (Peking University, China), Jiachi Chen (Sun Yat-sen University), John Grundy (Monash University), Jianbo Gao (Peking University), Yanlin Wang (Sun Yat-sen University), Ting Chen (University of Electronic Science and Technology of China), Zhi Guan (Peking University), Zhong Chen

**Categories:** Testing and Quality, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029866

**中文总结:** 提出 SolMigrator，从链上合约真实使用场景提取测试用例并迁移至功能相似的新合约，自动生成表达力强、与功能相关的智能合约测试，弥补现有方法偏重漏洞检测的不足。

**Abstract:** Pre-deployment testing has become essential to ensure the functional correctness of smart contracts. However, since smart contracts are stateful programs integrating many different functionalities, manually writing test cases to cover all potential usages requires significant effort from developers, leading to insufficient testing and increasing risks in practice. Although several testing techniques for smart contracts have been proposed, they primarily focus on detecting common low-level vulnerabilities such as re-entrancy, rather than generating expressive and function-relevant test cases that can reduce manual testing efforts. To bridge the gap, we propose SolMigrator, an automated technique designed to generate expressive and representative test cases for smart contracts. To our knowledge, SolMigrator is the first migration-based test generation technique for smart contracts, which extracts test cases from real-world usages of on-chain contracts and migrates them to test newly developed smart contracts with similar functionalities. Given a target smart contract to be tested and an on-chain similar source smart contract, SolMigrator first transforms the on-chain usage of the source contract into off-chain executable test cases based on on-chain transaction replay and dependency analysis. It then employs fine-grained static analysis to migrate the augmented test cases from the source to the target smart contract. We built a prototype of SolMigrator and have evaluated it on real-world smart contracts within the two most popular categories, ERC20 and ERC721. Our evaluation results demonstrate that SolMigrator effectively extracts test cases from existing on-chain smart contracts and accurately migrates them across different smart contracts, achieving an average precision of 96.3% and accuracy of 93.6%. Furthermore, the results indicate that these migrated test cases effectively cover common key functionalities of the target smart contracts. This provides promising evidence that real-world usages of existing smart contracts can be transformed into effective test cases for other newly developed smart contracts.

## 5. Boosting Code-line-level Defect Prediction with Spectrum Information and Causality Analysis

**Authors:** Shiyu Sun, Yanhui Li (Nanjing University), Lin Chen (Nanjing University), Yuming Zhou (Nanjing University), Jianhua Zhao (Nanjing University, China)

**Categories:** Testing and Quality, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029896

**中文总结:** 提出 SOUND，结合谱信息与因果分析利用历史行级缺陷标签量化 token 贡献，提升代码行级缺陷预测效果。

**Abstract:** Code-line-level defect prediction (CLDP) is an effective technique to incorporate comprehensive measures for buggy line identification to optimize efforts in Software Quality Assurance activities. Most CLDP methods either consider the textual information of the code or rely merely on file-level label information, which have not fully leveraged the essential information in the CLDP context, with historical \textit{code-line-level labels} being incredibly overlooked in their application. Due to the vast number of code lines and the sparsity of the tokens they contain, leveraging historical code-line-level label information remains a significant challenge. To address this issue, we propose a novel CLDP method, \textbf{S}pectrum inf\textbf{O}rmation and ca\textbf{U}sality a\textbf{N}alysis based co\textbf{D}e-line-level defect prediction ($\mathsf{SOUND}$). $\mathsf{SOUND}$ incorporates two key ideas: (a) it introduces a spectrum information perspective, utilizing labels from historical defective lines to quantify the contribution of tokens to line-level defects, and (b) it applies causal analysis to obtain a more systematic and comprehensive understanding of the causal relationships between tokens and defects. After conducting a comprehensive study involving 142 releases across 19 software projects, the experimental results show that our method significantly outperforms existing state-of-the-art (SOTA) CLDP baseline methods in terms of its ability to rank defective lines under three indicators, IFA, Recall@Top20\%LOC, and Effort@Top20\%Recall. Notably, in terms of IFA, our method achieves a score of 0 in most cases, indicating that the first line in the ranking list generated by our method is actually defective, significantly enhancing its practicality.

## 6. ChatGPT-Based Test Generation for Refactoring Engines Enhanced by Feature Analysis on Examples

**Authors:** Chunhao Dong (Beijing Institute of Technology), Yanjie Jiang (Peking University), Yuxia Zhang (Beijing Institute of Technology), Yang Zhang (Hebei University of Science and Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029808

**中文总结:** 基于重构引擎缺陷报告构建细粒度特征库，用 ChatGPT 按模板与特征生成测试程序并做差分测试，系统化发现多个重构引擎中的缺陷。

**Abstract:** Software refactoring is widely employed to improve software quality. However, conducting refactorings manually is tedious, time-consuming, and error-prone. Consequently, automated and semi-automated tool support is highly desirable for software refactoring in the industry, and most of the main-stream IDEs provide powerful tool support for refactoring. However, complex refactoring engines are prone to errors, which in turn may result in imperfect and incorrect refactorings. To this end, in this paper, we propose a ChatGPT-based approach to testing refactoring engines. We first manually analyze bug reports and test cases associated with refactoring engines, and construct a feature library containing fine-grained features that may trigger defects in refactoring engines. The approach automatically generates prompts according to both predefined prompt templates and features randomly selected from the feature library, requesting ChatGPT to generate test programs with the requested features. Test programs generated by ChatGPT are then forwarded to multiple refactoring engines for differential testing. To the best of our knowledge, it is the first approach in testing refactoring engines that guides test program generation with features derived from existing bugs. It is also the first approach in this line that exploits LLMs in the generation of test programs. Our initial evaluation of four main-stream refactoring engines suggests that the proposed approach is effective. It identified a total of 115 previously unknown bugs besides 28 inconsistent refactoring behaviors among different engines. Among the 115 bugs, 78 have been manually confirmed by the original developers of the tested engines, i.e., IntelliJ IDEA, Eclipse, VScode-Java, and NetBeans.

## 7. COCA: Generative Root Cause Analysis for Distributed Systems with Code Knowledge

**Authors:** Yichen LI (The Chinese University of Hong Kong), Yulun Wu (The Chinese University of Hong Kong), Jinyang Liu (Chinese University of Hong Kong), Zhihan Jiang (The Chinese University of Hong Kong), Zhuangbin Chen (Sun Yat-sen University), Guangba Yu (The Chinese University of Hong Kong), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029720

**中文总结:** 提出 COCA，从 issue 报告关联代码片段并重建执行路径，以代码知识增强分布式系统生成式根因分析，弥补仅依赖运行时监控或用户描述不足的问题。

**Abstract:** Runtime failures are commonplace in modern distributed systems. When such issues arise, users often turn to platforms such as Github or JIRA to report them and request assistance. Automatically identifying the root cause of these failures is critical for ensuring high reliability and availability. However, prevailing automatic root cause analysis (RCA) approaches rely significantly on comprehensive runtime monitoring data, which is often not fully available in issue platforms. Recent methods leverage large language models (LLMs) to analyze issue reports, but their effectiveness is limited by incomplete or ambiguous user-provided information. To obtain more accurate and comprehensive RCA results, the core idea of this work is to extract additional diagnostic clues from code to supplement data-limited issue reports. Specifically, we propose COCA, a code knowledge enhanced root cause analysis approach for issue reports. Based on the data within issue reports, COCA intelligently extracts relevant code snippets and reconstructs execution paths, providing a comprehensive execution context for further RCA. Subsequently, COCA construct a prompt combining historical issue reports along with profiled code knowledge, enabling the LLMs to generate detailed root cause summaries and localize responsible components. Our evaluation on datasets from five real-world distributed systems demonstrates that COCA significantly outperforms existing methods, achieving a 28.3% improvement in root cause localization and a 22.0% improvement in root cause summarization. Furthermore, COCA's performance consistency across various LLMs underscores its robust generalizability.

## 8. Code Cloning in Solidity Smart Contracts: Prevalence, Evolution, and Impact on Development

**Authors:** Ran Mo (Central China Normal University), Haopeng Song (Central China Normal University), Wei Ding (Central China Normal University), Chaochao Wu (Central China Normal University)

**Categories:** Security and Vulnerability, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029949

**中文总结:** 对 26,294 份 Solidity 智能合约开展克隆实证研究，发现克隆高度普遍且约 32.01% 协同演化，但与传统软件不同很少参与缺陷修复。

**Abstract:** In recent years, the development of Solidity smart contracts has been increasing rapidly in popularity. Code cloning is a common coding practice, and many prior studies have revealed that code clones could negatively impact software maintenance and quality. However, there is little work systematically analyzing the nature and impacts of code clones in solidity smart contracts. To bridge this gap, we investigate the prevalence, evolution, and bug-proneness of code clones in solidity smart contracts, and further identify the possible reasons for these clones’ occurrences. With our evaluation of 26,294 smart contracts with 97,877 functions, we have found that code clones are highly prevalent in smart contracts. Additionally, on average, 32.01% of clones co-evolve, indicating the need for careful management to avoid consistency issues. Surprisingly, unlike in traditional software development, code clones in smart contracts are rarely involved in bug fixes. Finally, we identify three main factors that affect the occurrences of clones. We believe our study can provide valuable insights for developers to understand and manage code clones in solidity smart contracts.

## 9. Code Comment Inconsistency Detection and Rectification Using a Large Language Model

**Authors:** Guoping Rong (Nanjing University), YongdaYu (Nanjing University), Song Liu (Nanjing University), Xin Tan (Nanjing University), Tianyi Zhang (Nanjing University), Haifeng Shen (Southern Cross University), Jidong Hu (Zhongxing Telecom Equipment)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029963

**中文总结:** 提出 C4RLLaMA，基于 CodeLLaMA 微调以检测并修正代码注释不一致（CCI）；在检测与修复任务上均优于现有方法。

**Abstract:** Comments are widely used in source code. If a comment is consistent with the code snippet it intends to annotate, it would aid code comprehension. Otherwise, Code Comment Inconsistency (CCI) is not only detrimental to the understanding of code, but more importantly, it would negatively impact the development, testing, and maintenance of software. To tackle this issue, existing research has been primarily focused on detecting inconsistencies with varied performance. It is evident that detection alone does not solve the problem; it merely paves the way for solving it. A complete solution requires detecting inconsistencies and, more importantly, rectifying them by amending comments. However, this type of work is scarce. In this paper, we contribute C4RLLaMA, a fine-tuned large language model based on the open-source CodeLLaMA. It not only has the ability to rectify inconsistencies by correcting relevant comment content but also outperforms state-of-the-art approaches in detecting inconsistencies. Experiments with various datasets confirm that C4RLLaMA consistently surpasses both Post Hoc and Just-in-time CCI detection approaches. More importantly, C4RLLaMA outperforms substantially the only known CCI rectification approach in terms of multiple performance metrics. To further examine C4RLLaMA's efficacy in rectifying inconsistencies, we conducted a manual evaluation, and the results showed that the percentage of correct comment updates by C4RLLaMA was 65.0\% and 55.9\% in Just-in-time and Post Hoc, respectively, implying C4RLLaMA's real potential in practical use.

## 10. Context Conquers Parameters: Outperforming Proprietary LLM in Commit Message Generation

**Authors:** Aaron Imani (University of California, Irvine), Iftekhar Ahmed (University of California at Irvine), Mohammad Moshirpour (University of California, Irvine)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029724

**中文总结:** 提出基于 8B 开源 LLM 的提交信息生成方法 OMEGA，通过上下文精炼在隐私与成本约束下生成可与 GPT-4 驱动 OMG 媲美的提交说明，证明上下文优化可胜过参数量。

**Abstract:** Commit messages provide descriptions of the modifications made in a commit using natural language, making them crucial for software maintenance and evolution. Recent developments in Large Language Models (LLMs) have led to their use in generating high-quality commit messages, such as the Omniscient Message Generator (OMG). This method employs GPT-4 to produce state-of-the-art commit messages. However, the use of proprietary LLMs like GPT-4 in coding tasks raises privacy and sustainability concerns, which may hinder their industrial adoption. Considering that open-source LLMs have achieved competitive performance in developer tasks such as compiler validation, this study investigates whether they can be used to generate commit messages that are comparable with OMG. Our experiments show that an open-source LLM can generate commit messages that are comparable to those produced by OMG. In addition, through a series of contextual refinements, we propose lOcal MessagE GenerAtor (OMEGA) , a CMG approach that uses a 4-bit quantized 8B open-source LLM. OMEGA produces state-of-the-art commit messages, surpassing the performance of GPT-4 in practitioners' preference.

## 11. Datalog-Based Language-Agnostic Change Impact Analysis for Microservices

**Authors:** Qingkai Shi (Nanjing University), Xiaoheng Xie (Ant Group), Xianjin Fu (Ant Group), Peng Di (Ant Group & UNSW Sydney), Huawei Li (Alibaba Inc.), Ang Zhou (Ant Group), Gang Fan (Ant Group)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029842

**中文总结:** 提出 Microscope，以 Datalog 规则统一表示微服务中多语言代码、配置、框架与变更，借助高效 Datalog 求解器识别受影响公共接口；在领先软件公司实践中验证有效且快速。

**Abstract:** The shift-left principle in the industry requires us to test a software application as early as possible. Particularly, when code changes in a microservice application are committed to the code repository, we have to efficiently identify all public microservice interfaces impacted by the changes, such that the impacted interfaces can be tested as soon as possible. However, developing an efficient change impact analysis is extremely challenging in microservices because of the multilingual problem: microservice applications are often implemented using varying programming languages and involve diverse frameworks and configuration files. To address this issue, this paper presents Microscope, a language-agnostic change impact analysis that uniformly represents the code, configuration files, frameworks, and code changes by relational Datalog rules. Microscope then benefits from an efficient Datalog solver to identify impacted interfaces. Experiments based on the use of Microscope in a leading software company demonstrate that Microscope is both effective and fast as it successfully identifies interfaces impacted by 112 code commits, with moderate time overhead, and could reduce 97% of interfaces to test and save 73% of testing time after code changes.

## 12. Decoding the Issue Resolution Process In Practice via Issue Report Analysis: A Case Study of Firefox

**Authors:** Antu Saha (William & Mary), Oscar Chaparro (William & Mary)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029751

**中文总结:** 分析 Firefox 356 份 issue 报告中的讨论，刻画实践中问题解决的阶段序列，提炼 47 种实例化模式以解码真实 issue 解决流程。

**Abstract:** Effectively managing and resolving software issues is critical for maintaining and evolving software systems. Development teams often rely on issue trackers and issue reports to track and manage the work needed during issue resolution, ranging from issue reproduction and analysis to solution design, implementation, verification, and deployment. Despite the issue resolution process being generally known in the software engineering community as a sequential list of activities, it is unknown how developers implement this process in practice and how they discuss it in issue reports. This paper aims to enhance our understanding of the issue resolution process implemented in practice by analyzing the issue reports of Mozilla Firefox. We qualitatively and quantitatively analyzed the discussions found in 356 Firefox issue reports, to identify the sequences of stages that developers go through to address various software problems. We analyzed the sequences to identify the overall resolution process at Firefox and derived a catalog of 47 patterns that represent instances of the process. We analyzed the process and patterns across multiple dimensions, including pattern complexity, issue report types, problem categories, and issue resolution times, resulting in various insights about Mozilla's issue resolution process. We discuss these findings and their implications for different stakeholders on how to better assess and improve the issue resolution process.

## 13. Enhancing Fault Localization in Industrial Software Systems via Contrastive Learning

**Authors:** Chun Li (Nanjing University), Hui Li (Samsung Electronics (China) R&D Centre), Zhong Li, Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Program Analysis and Verification, Evolution and Maintenance, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029934

**中文总结:** 提出 FALCON，将工业日志组织为图并用对比学习区分通过/失败运行以定位故障；相较 34 种谱方法与 4 种学习方法整体表现最优。

**Abstract:** Engineers utilize logs as a primary resource for fault localization in large-scale software and system testing, a process that is notoriously time-consuming, costly, and labor-intensive. Despite considerable progress in automated fault localization approaches, their applicability remains limited in such settings, due to the unavailability of fine-grained features in logs essential for most existing fault localization methods. In response, we introduce FALCON, a novel log-based fault localization framework. FALCON organizes complex semantic log information into graphical representations and employs contrastive learning to capture the differences between passed and failed logs, enabling the identification of crucial fault-related features. It also incorporates a specifically designed transitive analysis-based adaptive graph augmentation to minimize the influence of fault-unrelated log information on contrastive learning. Through extensive evaluations against 34 spectrum-based and 4 learning-based fault localization methods, FALCON demonstrates superior performance by outperforming all the methods in comparison. In addition, FALCON demonstrated its practical value by successfully identifying 71 out of 90 faults with a file-level Top-1 accuracy rate during a one-month deployment within a global company’s testing system.

## 14. Formally Verified Cloud-Scale Authorization

**Authors:** Aleks Chakarov (Amazon Web Services), Jaco Geldenhuys (Amazon Web Services), Matthew Heck (Amazon Web Services), MIchael Hicks (Amazon), Samuel Huang (Amazon Web Services), Georges-Axel Jaloyan (Amazon Web Services), Anjali Joshi (Amazon), K. Rustan M. Leino (Amazon), Mikael Mayer (Automated Reasoning Group, Amazon Web Services), Sean McLaughlin (Amazon Web Services), Akhilesh Mritunjai (Amazon.com), Clement Pit-Claudel (EPFL), Sorawee Porncharoenwase (Amazon Web Services), Florian Rabe (Amazon Web Services), Marianna Rapoport (Amazon Web Services), Giles Reger (Amazon Web Services), Cody Roux (Amazon Web Services), Neha Rungta (Amazon Web Services), Robin Salkeld (Amazon Web Services), Matthias Schlaipfer (Amazon Web Services), Daniel Schoepe (Amazon), Johanna Schwartzentruber (Amazon Web Services), Serdar Tasiran (Amazon, n.n.), Aaron Tomb (Amazon), Emina Torlak (Amazon Web Services, USA), Jean-Baptiste Tristan (Amazon), Lucas Wagner (Amazon Web Services), Michael Whalen (Amazon Web Services and the University of Minnesota), Remy Willems (Amazon), Tongtong Xiang (Amazon Web Services), Taejoon Byun (University of Minnesota), Joshua M. Cohen (Princeton University), Ruijie Fang (University of Texas at Austin), Junyoung Jang (McGill University), Jakob Rath (TU Wien), Hira Taqdees Syeda, Dominik Wagner (University of Oxford), Yongwei Yuan (Purdue University)

**Categories:** Security and Vulnerability, Evolution and Maintenance, Human and Social Aspects, Architecture and Design

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029876

**中文总结:** 使用 Dafny 形式化验证重建每秒十亿次调用的云级授权引擎，2024 年无事故上线并使客户性能提升三倍。

**Abstract:** All critical systems must evolve to meet the needs of a growing and diversifying user base. But supporting that evolution is challenging at increasing scale: Maintainers must find a way to ensure that each change does only what is intended, and will not inadvertently change behavior for existing users. This paper presents how we addressed this challenge for a cloud-scale authorization engine, invoked 1 billion times per second, by using formal verification. Over a period of four years, we built a new authorization engine, one that behaves functionally the same as its predecessor, using the verification-aware programming language Dafny. We can now confidently deploy enhancements and optimizations while maintaining the highest assurance of both correctness and backward compatibility. We deployed the new engine in 2024 without incident and customers immediately enjoyed a threefold performance improvement. The methodology we followed to build this new engine was not an off-the-shelf application of an existing verification tool, and this paper presents several key insights: 1) Rather than prove correct the existing engine, written in Java, we found it more effective to \emph{write a new engine} in Dafny, a language built for \emph{verification from the ground up}, and then compile the result to Java. 2) To ensure performance, debuggability, and to gain trust from stakeholders, we needed to generate readable, \emph{idiomatic} Java code, essentially a transliteration of the source Dafny. 3) To ensure that the specification matches the system's actual behavior, we performed \emph{extensive differential and shadow testing} throughout the development process, ultimately comparing against $10^{15}$ production samples prior to deployment. Our approach demonstrates how formal verification can be effectively applied to evolve critical legacy software at scale.

## 15. GenC2Rust: Towards Generating Generic Rust Code from C

**Authors:** Xiafa Wu (University of California, Irvine), Brian Demsky (University of California at Irvine)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029860

**中文总结:** 提出 GenC2Rust，通过静态分析 C 程序中 void 指针用法推导类型约束，将非泛型 C 代码翻译为符合 Rust 习惯的泛型 Rust 代码，缓解现有 C 转 Rust 工具难以利用泛型的问题。

**Abstract:** Rust provides an exciting combination of strong safety guarantees and high performance. Many new systems are being implemented in Rust. Nevertheless, there is a large body of existing C code that could greatly benefit from Rust's safety guarantees. Unfortunately, the manual effort required to rewrite C code into Rust is often prohibitively expensive. Researchers have explored tools to assist developers in translating legacy C code into Rust code. However, the mismatch between C abstractions and idiomatic Rust abstractions makes it challenging to automatically utilize Rust's language features, resulting in non-idiomatic Rust code that requires extensive manual effort to further refactor. For example, existing tools often fail to map polymorphic uses of void pointers in C to Rust's more idiomatic generic pointers. In this paper, we present a translation tool, GenC2Rust, that translates non-generic C code into generic Rust code. GenC2Rust statically analyzes the use of void pointers in the C program to compute the typing constraints and then retypes the void pointers into generic pointers. We conducted an evaluation of GenC2Rust across 42 C programs that vary in size and span multiple domains to demonstrate its scalability as well as correctness. We also present a detailed analysis of the limiting factors encountered in the translation process.

## 16. HedgeCode: A Multi-Task Hedging Contrastive Learning Framework for Code Search

**Authors:** Gong Chen (Wuhan University), Xiaoyuan Xie (Wuhan University), Xunzhu Tang (University of Luxembourg), Qi Xin (Wuhan University), Wenjie Liu (Wuhan University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029759

**中文总结:** 提出 HedgeCode，多任务对冲对比学习框架对齐代码与自然语言表示并捕捉细粒度语义差异，用于提升代码搜索效果。

**Abstract:** Code search is a vital activity in software engineering, focused on identifying and retrieving the correct code snippets based on a query provided in natural language. Approaches based on deep learning techniques have been increasingly adopted for this task, enhancing the initial representations of both code and its natural language descriptions. Despite this progress, there remains an unexplored gap in ensuring consistency between the representation spaces of code and its descriptions. Furthermore, existing methods have not fully leveraged the potential relevance between code snippets and their descriptions, presenting a challenge in discerning fine-grained semantic distinctions among similar code snippets. To address these challenges, we introduce a multi-task hedging contrastive Learning framework for Code Search, referred to as HedgeCode. HedgeCode is structured around two primary training phases. The first phase, known as the representation alignment stage, proposes a hedging contrastive learning approach. This method aims to detect subtle differences between code and natural language text, thereby aligning their representation spaces by identifying relevance. The subsequent phase involves multi-task joint learning, wherein the previously trained model serves as the encoder. This stage optimizes the model through a combination of supervised and self-supervised contrastive learning tasks. Our framework’s effectiveness is demonstrated through its performance on the CodeSearchNet benchmark, showcasing HedgeCode’s ability to address the mentioned limitations in code search tasks.

## 17. HumanEvo: An Evolution-aware Benchmark for More Realistic Evaluation of Repository-level Code Generation

**Authors:** Dewu Zheng (Sun Yat-sen University), Yanlin Wang (Sun Yat-sen University), Ensheng Shi (Xi’an Jiaotong University), Ruikai Zhang (Huawei Cloud Computing Technologies), Yuchi Ma (Huawei Cloud Computing Technologies), Hongyu Zhang (Chongqing University), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029910

**中文总结:** 指出忽视项目演化会导致仓库级代码生成评测失真，构建演化感知基准 HumanEvo 及自动执行评测工具，更贴近真实开发场景。

**Abstract:** To evaluate the repository-level code generation capabilities of Large Language Models (LLMs) in complex real-world software development scenarios, many evaluation methods have been developed. These methods typically leverage contextual code from the latest version of a project to assist LLMs in accurately generating the desired function. However, such evaluation methods fail to consider the dynamic evolution of software projects over time, which we refer to as evolution-ignored settings. This in turn results in inaccurate evaluation of LLMs' performance. In this paper, we conduct an empirical study to deeply understand LLMs' code generation performance within settings that reflect the evolution nature of software development. To achieve this, we first construct an evolution-aware repository-level code generation dataset, namely HumanEvo, equipped with an automated execution-based evaluation tool. Second, we manually categorize HumanEvo according to dependency levels to more comprehensively analyze the model's performance in generating functions with different dependency levels. Third, we conduct extensive experiments on HumanEvo with seven representative and diverse LLMs to verify the effectiveness of the proposed benchmark. We obtain several important findings through our experimental study. For example, we find that previous evolution-ignored evaluation methods result in inflated performance of LLMs, with performance overestimations ranging from 10.0% to 61.1% under different context acquisition methods, compared to the evolution-aware evaluation approach. Based on the findings, we give actionable suggestions for more realistic evaluation of LLMs on code generation. We also build a shared evolution-aware code generation toolbox to facilitate future research. The replication package including source code and datasets is anonymously available at https://anonymous.4open.science/r/HumanEvo/.

## 18. Instrumentation-Driven Evolution-Aware Runtime Verification

**Authors:** Kevin Guan (Cornell University), Owolabi Legunsen (Cornell University)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029969

**中文总结:** 提出 iMOP 首个插桩驱动的演化感知运行时验证框架，针对测试开销主要来自插桩而非监控的观察，仅对变更代码重新插桩并复用旧版本插桩，在 14 种技术组合下安全加速 RV。

**Abstract:** Runtime verification (RV) found hundreds of bugs by monitoring passing tests against formal specifications (specs). RV first instruments a program to obtain relevant events, e.g., method calls, to monitor. A hindrance to RV adoption, especially in continuous integration, is its high overhead. So, prior work proposed spec-driven evolution-aware techniques to speed up RV. They use complex analysis to re-monitor a subset of specs related to code impacted by changes. But, these techniques assume that RV overhead is dominated by monitoring time, and their designs often sacrifice safety (ability to find all new violations) for speed. We present iMOP, the first instrumentation-driven evolution-aware RV framework. iMOP leverages a recent observation that RV overhead during testing is often dominated by instrumentation, not monitoring. iMOP embodies a family of 14 techniques that aim to safely speed up RV by simply re-instrumenting only changed code. Instrumentation from the old revision is re-used for unchanged code, and all specs are re-monitored in the new revision. We implement iMOP as a Maven plugin and evaluate it on 1,627 revisions of 48 projects, using 160 specs of correct JDK API usage. iMOP is safe by design. It is up to 29.6x faster than re-running RV from scratch after each change, and 17.8x and 6.7x faster than safe and unsafe spec-driven techniques, respectively. iMOP is faster than just applying regression test selection to RV.

## 19. LibreLog: Accurate and Efficient Unsupervised Log Parsing Using Open-Source Large Language Models

**Authors:** Zeyang Ma (Concordia University), Dong Jae Kim (DePaul University), Tse-Hsun (Peter) Chen (Concordia University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029927

**中文总结:** 提出 LibreLog 无监督日志解析方法，基于 Llama3-8B 等开源 LLM 按静态文本分组解析动态变量，兼顾隐私、成本与精度，达到 SOTA 解析准确率。

**Abstract:** Log parsing is a critical step that transforms unstructured log data into structured formats, facilitating subsequent log-based analysis. Traditional syntax-based log parsers are efficient and effective, but they often experience decreased accuracy when processing logs that deviate from the predefined rules. Recently, large language models (LLM) based log parsers have shown superior parsing accuracy. However, existing LLM-based parsers face three main challenges: 1) time-consuming and labor-intensive manual labeling for fine-tuning or in-context learning, 2) increased parsing costs due to the vast volume of log data and limited context size of LLMs, and 3) privacy risks from using commercial models like ChatGPT with sensitive log information. To overcome these limitations, this paper introduces LibreLog, an unsupervised log parsing approach that leverages open-source LLMs (i.e., Llama3-8B) to enhance privacy and reduce operational costs while achieving state-of-the-art parsing accuracy. LibreLog first groups logs with similar static text but varying dynamic variables using a fixed-depth grouping tree. It then parses logs within these groups using three components: i) similarity scoring-based retrieval augmented generation: selects diverse logs within each group based on Jaccard similarity, helping the LLM distinguish between static text and dynamic variables; ii) self-reflection: iteratively query LLMs to refine log templates to improve parsing accuracy; and iii) log template memory: stores parsed templates to reduce LLM queries for improved parsing efficiency. Our evaluation on LogHub-2.0 shows that LibreLog achieves 25% higher parsing accuracy and processes logs 2.7 times faster compared to state-of-the-art LLM-based parsers. In short, LibreLog addresses privacy and cost concerns of using commercial LLMs while achieving state-of- the-arts parsing efficiency and accuracy.

## 20. LLMs Meet Library Evolution: Evaluating Deprecated API Usage in LLM-based Code Completion

**Authors:** Chong Wang (Nanyang Technological University), Kaifeng Huang (Tongji University), Jian Zhang (Nanyang Technological University), Yebo Feng (Nanyang Technological University), Lyuye Zhang (Nanyang Technological University), Yang Liu (Nanyang Technological University), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029774

**中文总结:** 首次系统评估 7 个 LLM 在代码补全中使用已废弃 API 的问题，分析模型、提示与库等因素并提出 ReplaceAPI 等轻量修复方案。

**Abstract:** Large language models (LLMs), pre-trained or fine-tuned on large code corpora, have shown effectiveness in generating code completions. However, in LLM-based code completion, LLMs may struggle to use correct and up-to-date Application Programming Interfaces (APIs) due to the rapid and continuous evolution of libraries. While existing studies have highlighted issues with predicting incorrect APIs, the specific problem of deprecated API usage in LLM-based code completion has not been thoroughly investigated. To address this gap, we conducted the first evaluation study on deprecated API usage in LLM-based code completion. This study involved seven advanced LLMs, 145 API mappings from eight popular Python libraries, and 28,125 completion prompts. The study results reveal the status quo (i.e., API usage plausibility and deprecated usage rate) of deprecated API and replacing API usage in LLM-based code completion from the perspectives of model, prompt, and library, and indicate the root causes behind. Based on these findings, we propose two lightweight fixing approaches, ReplaceAPI and InsertPrompt, which can serve as baseline approaches for future research on mitigating deprecated API usage in LLM-based completion. Additionally, we provide implications for future research on integrating library evolution with LLM-driven software development.

## 21. Model Editing for LLMs4Code: How Far are We?

**Authors:** Xiaopeng Li (National University of Defense Technology), Shangwen Wang (National University of Defense Technology), Shasha Li (National University of Defense Technology), Jun Ma (National University of Defense Technology), Jie Yu (National University of Defense Technology), Xiaodong Liu (National University of Defense Technology), Jing Wang (National University of Defense Technology), Bin Ji (National University of Defense Technology), Weimin Zhang (National University of Defense Technology)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029902

**中文总结:** 首次系统评估模型编辑技术在代码 LLM 知识修正中的效果，构建 CLMEEval 基准与数据集，对比多种 SOTA 编辑方法在不同代码任务上的适用性与局限。

**Abstract:** Large Language Models for Code (LLMs4Code) have been found to exhibit outstanding performance in the software engineering domain, especially the remarkable performance in coding tasks. However, even the most advanced LLMs4Code can inevitably contain incorrect or outdated code knowledge. Due to the high cost of training LLMs4Code, it is impractical to re-train the models for fixing these problematic code knowledge. Model editing is a new technical field for effectively and efficiently correcting erroneous knowledge in LLMs, where various model editing techniques and benchmarks have been proposed recently. Despite that, a comprehensive study that thoroughly compares and analyzes the effectiveness of all state-of-the-art model editing techniques for adapting the knowledge within LLMs4Code models across various code-related tasks is notably absent. To bridge this gap, we perform the first systematic study on applying state-of-the-art model editing approaches to repair the inaccuracy of LLMs4Code. To that end, we introduce a benchmark named CLMEEval, which consists of two datasets, i.e., CoNaLa-Edit (CNLE) with 21K+ code generation samples and CodeSearchNet-Edit (CSNE) with 16K+ code summarization samples. With the help of CLMEEval, we evaluate six advanced model editing techniques on three LLMs4Code: CodeLlama (7B), CodeQwen1.5 (7B), and Stable-Code (3B). Our findings include that the external memorization-based GRACE approach achieves the best knowledge editing effectiveness and specificity (the editing does not influence untargeted knowledge), while generalization (whether the editing can generalize to other semantically-identical inputs) is a universal challenge for existing techniques. Furthermore, building on in-depth case analysis, we introduce an enhanced version of GRACE called A-GRACE, which incorporates contrastive learning to better capture the semantics of the inputs. Results demonstrate that A-GRACE notably enhances generalization while maintaining similar levels of effectiveness and specificity compared to the vanilla GRACE.

## 22. Moye: A Wallbreaker for Monolithic Firmware

**Authors:** Jintao Huang (Institute of Information Engineering, Chinese Academy of Science & University of Chinese Academy of Sciences, Beijing, China), Kai Yang (School of Computer, Electronics and Information, Guangxi University), Gaosheng Wang (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China), Zhiqiang Shi (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China), Zhiwen Pan (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China), Shichao Lv (Institute of Information Engineering, Chinese Academy of Science), Limin Sun (Institute of Information Engineering, Chinese Academy of Sciences & University of Chinese Academy of Sciences, Beijing, China)

**Categories:** Program Analysis and Verification, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029743

**中文总结:** 提出 Moye，针对无格式标识的单体固件，利用寄存器使用约束与掩码语言模型学习指令间隐含关系以识别函数边界；在 1318 个固件镜像（含 48 个真实设备样本）上验证有效性。

**Abstract:** As embedded devices become increasingly popular, monolithic firmware, known for its execution efficiency and simplicity, is widely used in resource-constrained devices. Different from ordinary firmware, the monolithic firmware image is packed without the file that indicates its format, which challenges the reverse engineering of monolithic firmware. Function identification is the prerequisite of monolithic firmware's analysis. Prior works on function identification are less effectiveness when applied to monolithic firmware due to their heavy reliance on file formats. In this paper, we propose Moye, a novel method to identify functions in monolithic firmware. We leverage the important insight that the use of registers must conform to some constraints. In particular, our approach segments the firmware, locate code sections and output the instructions. We uses a masked language model to learn hiding relationships among the instructions to identify the function boundaries. We evaluate Moye using 1,318 monolithic firmware images, including 48 samples collected from widely used devices. The evaluation demonstrates that our approach significantly outperforms current works, achieving a precision greater than 98% and a recall rate greater than 97% across most datasets, showing robustness to complicated compilation options.

## 23. On Prescription or Off Prescription? An Empirical Study of Community-prescribed Security Configurations for Kubernetes

**Authors:** Shazibul Islam Shamim (Auburn University), Hanyang Hu (Company A), Akond Rahman (Auburn University)

**Categories:** Security and Vulnerability, Evolution and Maintenance

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029793

**中文总结:** 实证研究 Kubernetes CIS 社区推荐安全配置：从业者对多项配置认知不足，开源与企业配置分别有 17.9% 与 18.0% 存在违规。

**Abstract:** Despite being beneficial for rapid delivery of software, Kubernetes deployments can be susceptible to security attacks, which can cause serious consequences. A systematic characterization of how community-prescribed security configurations, i.e., security configurations that are recommended by security experts, can aid practitioners to secure their Kubernetes deployments. To that end, we conduct an empirical study with 53 security configurations recommended by the Center for Internet Security (CIS), 20 survey respondents, and 356 configuration files obtained from open source software (OSS) repositories and 188 configuration files used by Company-A. From our empirical study, we observe: (i) practitioners can be unaware of prescribed security configurations as 5%~40% of the survey respondents are unfamiliar with 16 prescribed configurations; and (ii) for Company-A and OSS respectively, 18.0% and 17.9% of the configuration files include at least one violation of prescribed configurations. From our evaluation with 5 static application security testing (SAST) tools we find (i) only Kubescape to support all of the prescribed security configurations; (ii) the highest observed precision to be 0.48 and 0.43 respectively, for the Company-A and OSS datasets; and (iii) the highest observed recall to be respectively, 0.53 and 0.65 for the Company-A and OSS datasets. We conclude the paper by providing recommendations for practitioners on how they can use existing SAST tools to secure their Kubernetes deployments.

## 24. PairSmell: A Novel Perspective Inspecting Software Modular Structure

**Authors:** Chenxing Zhong (Nanjing University), Daniel Feitosa (University of Groningen), Paris Avgeriou (Univ. of Gronningen), Huang Huang (State Grid Nanjing Power Supply Company), Yue Li (Nanjing University), He Zhang (Nanjing University)

**Categories:** Evolution and Maintenance, Architecture and Design

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029796

**中文总结:** 提出 PairSmell 概念，以实体对的模块化关系（应分离或共置）与多工具共识的“适宜关系”对比识别需重构的架构决策；在 20 个 C/C++ 系统上实证评估。

**Abstract:** Enhancing the modular structure of existing systems has attracted substantial research interest, focusing on two main methods: (1) software modularization and (2) identifying design issues (e.g., smells) as refactoring opportunities. However, re-modularization solutions often require extensive modifications to the original modules, and the design issues identified are generally too coarse to guide refactoring strategies. Combining the above two methods, this paper introduces a novel concept, \emph{PairSmell}, which exploits modularization to pinpoint design issues necessitating refactoring. We concentrate on a granular but fundamental aspect of modularity principles---\emph{modular relation (MR)}, i.e., \emph{whether a pair of entities are separated or collocated}. The main assumption is that, if the actual MR of a pair violates its `apt MR', i.e., an MR agreed on by multiple modularization tools (as raters), it can be deemed likely a flawed architectural decision that necessitates further examination. To quantify and evaluate \emph{PairSmell}, we conduct an empirical study on 20 C/C++ and Java projects, using 4 established modularization tools to identify two forms of \emph{PairSmell}: inapt separated pairs $\mathit{InSep}$ and inapt collocated pairs $\mathit{InCol}$. Our study on 260,003 instances reveals that their architectural impacts are substantial: (1) on average, 14.60\% and 20.44\% of software entities are involved in $\mathit{InSep}$ and $\mathit{InCol}$ MRs respectively; (2) $\mathit{InSep}$ pairs are associated with 190\% more co-changes than properly separated pairs, while $\mathit{InCol}$ pairs are associated with 35\% fewer co-changes than properly collocated pairs, both indicating a successful identification of modular structures detrimental to software quality; and (3) both forms of \emph{PairSmell} persist across software evolution. This evidence strongly suggests that \emph{PairSmell} can provide meaningful insights for inspecting modular structure, with the identified issues being both granular and fundamental, making the enhancement of modular design more efficient.

## 25. Pattern-based Generation and Adaptation of Quantum Workflows

**Authors:** Martin Beisel (Institute of Architecture of Application Systems (IAAS), University of Stuttgart), Johanna Barzen (University of Stuttgart), Frank Leymann (University of Stuttgart), Lavinia Stiliadou (Institute of Architecture of Application Systems (IAAS), University of Stuttgart), Daniel Vietz (University of Stuttgart), Benjamin Weder (Institute of Architecture of Application Systems (IAAS), University of Stuttgart)

**Categories:** Evolution and Maintenance, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029719

**中文总结:** 基于量子计算模式语言，自动从模式生成并适配编排异质量子组件的量子工作流，降低手工建模与配置的复杂度与出错率。

**Abstract:** Building quantum applications requires deep knowledge of quantum computing and software engineering. Hence, an abstraction layer reducing the complexity for non-experts is needed. Patterns are an established concept for the abstract description of proven solutions to recurring problems. Therefore, the quantum computing patterns, a pattern language for the quantum computing domain, can be used to define the building blocks and the structure of hybrid quantum applications. Furthermore, concrete software artifacts can be associated with patterns to solve the corresponding problem. However, these software artifacts are usually heterogeneous, e.g., using different data formats. Quantum workflows enable a robust and scalable orchestration of these heterogeneous software artifacts. However, manually modeling and configuring such quantum workflows is a complex, error-prone, and time-consuming task. To overcome this issue, we present an approach that automates the generation and adaptation of quantum workflows using the quantum computing patterns. We provide an architecture realizing our approach, a corresponding prototype, as well as an evaluation comprising different use cases, a runtime comparison, and a user study.

## 26. Preserving Privacy in Software Composition Analysis: A Study of Technical Solutions and Enhancements

**Authors:** Huaijin Wang (Ohio State University), Zhibo Liu (Hong Kong University of Science and Technology), Yanbo Dai (The Hong Kong University of Science and Technology (Guangzhou)), Shuai Wang (Hong Kong University of Science and Technology), Qiyi Tang (Tencent Security Keen Lab), Sen Nie (Tencent Security Keen Lab), Shi Wu (Tencent Security Keen Lab)

**Categories:** Program Analysis and Verification, Evolution and Maintenance, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029940

**中文总结:** 系统梳理软件成分分析（SCA）中的隐私保护技术方案，分析工业界“轻量本地 SCA”与远程深度分析在隐私、精度与厂商资产保护之间的权衡，并提出增强思路。

**Abstract:** Software composition analysis (SCA) denotes the process of identifying open-source software components in an input software application. SCA has been extensively developed and adopted by academia and industry. However, we notice that the modern SCA techniques in industry scenarios still need to be improved due to privacy concerns. Overall, SCA requires the users to upload their applications’ source code to a remote SCA server, which then deeply inspects the applications and reports the component usage to users. This process is privacy-sensitive since the applications may contain sensitive information, such as proprietary algorithms, trade secrets, and user data. Moreover, applications' source code is generally deemed proprietary, and users do not want to share it with the SCA vendor. To protect customers' privacy, contemporary SCA vendors often propose to deploy a "lite" version of SCA service on the customer side. To avoid the leakage of SCA vendors' valuable assets (e.g., code, model, and data), the "lite" SCA usually only performs a shallow analysis with limited accuracy. Privacy concerns have prevented the SCA technology from being used in real-world scenarios. Therefore, academia and the industry demand privacy-preserving SCA solutions. For the first time, we analyze the privacy requirements of SCA and provide a landscape depicting possible technical solutions with varying privacy gains and overheads. In particular, given that de facto SCA frameworks are primarily driven by code similarity-based techniques, we explore combining several privacy-preserving protocols to encapsulate the similarity-based SCA framework. Among all viable solutions, we find that multi-party computation (MPC) offers the strongest privacy guarantee and plausible accuracy; it, however, incurs high overhead ($184\times$). We optimize the MPC-based SCA framework by reducing the amount of crypto protocol transactions using program analysis techniques. The evaluation results show that our proposed optimizations can reduce the MPC-based SCA overhead to only 8.5% without sacrificing SCA’s privacy guarantee or accuracy.

## 27. Puppy: Finding Performance Degradation Bugs in DBMSs via Limited-Optimization Plan Construction

**Authors:** Zhiyong Wu (Tsinghua University, China), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Mingzhe Wang (Tsinghua University), Yu Jiang (Tsinghua University)

**Categories:** Evolution and Maintenance, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029960

**中文总结:** 提出 Puppy，通过对比「全优化」与「受限优化」执行计划来发现 DBMS 性能退化缺陷（PDB）；在多个数据库上检出 62 个 PDB，其中 54 个为未知缺陷。

**Abstract:** Database management systems (DBMSs) consistently strive for enhanced performance. For a given query, the optimizer of a DBMS aims to construct an optimal execution plan that incorporates multiple optimization operations. However, the resulting plan may sometimes perform worse than even if no optimizations were applied. This occurs because the interactions between optimizations are complex and some situations might be overlooked in the implementation. We refer to these issues as Performance Degradation Bugs (PDBs). PDBs can result in significant consequences from decreased system efficiency and prolonged query processing times to potential disruptions in critical business operations. In this paper, we present Puppy, an automated approach for detecting PDBs in DBMSs using limited-optimization plan construction. The key idea is to compare the performance with the plan generated with all optimization operations enabled, against the plan generated with only a subset of optimization operations in the same DBMS. If the response time of the plan with the limited optimization set is shorter than that of the fully optimized plan, it indicates a potential PDB. Specifically, Puppy first generates queries that incorporate multiple optimization sequences, guided by optimization operation sequence coverage. Secondly, Puppy analyzes the query plan and selectively disables specific optimizations to construct the limited optimization plan. We evaluate Puppy on five widely-used DBMSs, namely MySQL, Percona, TiDB, PolarDB, and PostgreSQL against the state-of-the-art DBMS performance testing tools APOLLO and AMOEBA. Puppy detected 26 and 25 more performance anomalies, covered 151,201 and 173,798 more branches than APOLLO and AMOEBA in 48 hours, respectively. More importantly, Puppy reports 62 PDBs, with 54 anomalies confirmed as previously unknown bugs.

## 28. Reasoning Runtime Behavior of a Program with LLM: How Far Are We?

**Authors:** Junkai Chen (Zhejiang University), Zhiyuan Pan (Zhejiang University), Xing Hu (Zhejiang University), Zhenhao Li (York University), Ge Li (Peking University), Xin Xia (Huawei)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029885

**中文总结:** 提出 REval 框架，评估 code LLM 对程序运行时中间行为推理及逻辑一致性；大规模实验显示多数模型在运行时行为推理上表现不佳。

**Abstract:** Large language models for code (i.e., code LLMs) have shown strong code understanding and generation capabilities. To evaluate the capabilities of code LLMs in various aspects, many benchmarks have been proposed (e.g., HumanEval and ClassEval). Code reasoning is one of the most essential abilities of code LLMs, but existing benchmarks for code reasoning are not sufficient. Typically, they focus on predicting the input and output of a program, ignoring the evaluation of the intermediate behavior during program execution, as well as the logical consistency (e.g., the model should not give the correct output if the prediction of execution path is wrong) when performing the reasoning. To address these problems, in this paper, we propose a framework, namely REval, for evaluating code reasoning abilities and consistency of code LLMs with program execution. We utilize existing code benchmarks and adapt them to new benchmarks within our framework. A large-scale empirical study is conducted and most LLMs show unsatisfactory performance on both Runtime Behavior Reasoning (i.e., an average accuracy of 44.4\%) and Incremental Consistency Evaluation (i.e., an average IC score of 10.3). Evaluation results of current code LLMs reflect the urgent need for the community to strengthen the code reasoning capability of code LLMs.

## 29. RustAssistant: Using LLMs to Fix Compilation Errors in Rust Code

**Authors:** Pantazis Deligiannis (Microsoft Research), Akash Lal (Microsoft Research), Nikita Mehrotra (Microsoft Research), Rishi Poddar (Microsoft Research), Aseem Rastogi (Microsoft Research)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029935

**中文总结:** 提出 RustAssistant，结合提示工程与 LLM—Rust 编译器迭代反馈自动修复编译错误；在开源 Rust 项目上峰值准确率约 74%，并发布编译错误数据集。

**Abstract:** The Rust programming language, with its safety guarantees, has established itself as a viable choice for low-level systems programming language over the traditional, unsafe alternatives like C/C++. These guarantees come from a strong ownership-based type system, as well as primitive support for features like closures, pattern matching, etc., that make the code more concise and amenable to reasoning. These unique Rust features also pose a steep learning curve for programmers. This paper presents a tool called RustAssistant that leverages the emergent capabilities of Large Language Models (LLMs) to automatically suggest fixes for Rust compilation errors. RustAssistant uses a careful combination of prompting techniques as well as iteration between an LLM and the Rust compiler to deliver high accuracy of fixes. RustAssistant is able to achieve an impressive peak accuracy of roughly 74% on real-world compilation errors in popular open-source Rust repositories. We also contribute a dataset of Rust compilation errors to enable further research.

## 30. Similar but Patched Code Considered Harmful -- The Impact of Similar but Patched Code on Recurring Vulnerability Detection and How to Remove Them

**Authors:** Zixuan Tan (Zhejiang University), Jiayuan Zhou (Huawei), Xing Hu (Zhejiang University), Shengyi Pan (Zhejiang University), Kui Liu (Huawei), Xin Xia (Huawei)

**Categories:** Security and Vulnerability, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029734

**中文总结:** 提出语言无关框架 FVF，通过分析代码变更历史识别并过滤相似但已修补代码，为四种漏洞检测工具过滤 65.1% 误报且无假阳性。

**Abstract:** Identifying recurring vulnerabilities is crucial for ensuring software security. Clone-based techniques, while widely used, often generate many false alarms due to the existence of similar but patched (SBP) code, which is similar to vulnerable code but is not vulnerable due to having been patched. Although the SBP code poses a great challenge to the effectiveness of existing approaches, it has not yet been well explored. In this paper, we propose a programming language agnostic framework, Fixed Vulnerability Filter (FVF), to identify and filter such SBP instances in vulnerability detection. Different from existing studies that leverage function signatures, our approach analyzes code change histories to precisely pinpoint SBPs and consequently reduce false alarms. Evaluation under practical scenarios confirms the effectiveness and precision of our approach. Remarkably, FVF identifies and filters 65.1% of false alarms from four vulnerability detection tools (i.e., ReDeBug, VUDDY, MVP, and an elementary hash-based approach) without yielding false positives. We further apply FVF to 1,081 real-world software projects and construct a real-world SBP dataset containing 6,827 SBP functions. Due to the SBP nature, the dataset can act as a strict benchmark to test the sensitivity of the vulnerability detection approach in distinguishing real vulnerabilities and SBPs. Using this dataset, we demonstrate the ineffectiveness of four state-of-the-art deep learning-based vulnerability detection approaches. Our dataset can help developers make a more realistic evaluation of vulnerability detection approaches and also paves the way for further exploration of real-world SBP scenarios.

## 31. Software Model Evolution with Large Language Models: Experiments on Simulated, Public, and Industrial Datasets

**Authors:** Christof Tinnes (Saarland University), Alisa Carla Welter (Saarland University), Sven Apel (Saarland University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029888

**中文总结:** 提出 RaMc，结合大语言模型、软件模型历史与检索增强生成支持模型补全与演化；在工业数据上语义正确率达 62.30%，类型正确率最高 86.19%。

**Abstract:** Modeling structure and behavior of software systems plays a crucial role in the industrial practice of software engineering. As with other software engineering artifacts, software models are subject to evolution. Supporting modelers in evolving software models with recommendations for model completions is still an open problem, though. In this paper, we explore the potential of large language models for this task. In particular, we propose an approach, \textsc{RaMc}, leveraging large language models, model histories of software systems, and retrieval-augmented generation for model completion. Through experiments on three datasets, including an industrial application, one public open-source community dataset, and one controlled collection of simulated model repositories, we evaluate the potential of large language models for model completion. We found that large language models are indeed a promising technology for supporting software model evolution (62.30% semantically correct completions on real-world industrial data and up to 86.19% type-correct completions). Furthermroe, we found that the general inference capabilities of large language models are useful, for example, when dealing with concepts for which there are few, noisy, or no examples at all.

## 32. Source Code Summarization in the Era of Large Language Models

**Authors:** Weisong Sun (Nanjing University), Yun Miao (Nanjing University), Yuekang Li (UNSW), Hongyu Zhang (Chongqing University), Chunrong Fang (Nanjing University), Yi Liu (Nanyang Technological University), Gelei Deng (Nanyang Technological University), Yang Liu (Nanyang Technological University), Zhenyu Chen (Nanjing University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029737

**中文总结:** 系统研究 LLM 时代代码摘要工作流，发现 GPT-4 自动评估最贴近人工，且高级提示技术未必优于简单 zero-shot 提示。

**Abstract:** To support software developers in understanding and maintaining programs, various automatic (source) code summarization techniques have been proposed to generate a concise natural language summary (i.e., comment) for a given code snippet. Recently, the emergence of large language models (LLMs) has led to a great boost in the performance of code-related tasks. In this paper, we undertake a systematic and comprehensive study on code summarization in the era of LLMs, which covers multiple aspects involved in the workflow of LLM-based code summarization. Specifically, we begin by examining prevalent automated evaluation methods for assessing the quality of summaries generated by LLMs and find that the results of the GPT-4 evaluation method are most closely aligned with human evaluation. Then, we explore the effectiveness of five prompting techniques (zero-shot, few-shot, chain-of-thought, critique, and expert) in adapting LLMs to code summarization tasks. Contrary to expectations, advanced prompting techniques may not outperform simple zero-shot prompting. Next, we investigate the impact of LLMs' model settings (including top\_p and temperature parameters) on the quality of generated summaries. We find the impact of the two parameters on summary quality varies by the base LLM and programming language, but their impacts are similar. Moreover, we canvass LLMs' abilities to summarize code snippets in distinct types of programming languages. The results reveal that LLMs perform suboptimally when summarizing code written in logic programming languages compared to other language types (e.g., procedural and object-oriented programming languages). Finally, we unexpectedly find that \codellama{} with 7B parameters can outperform advanced GPT-4 in generating summaries describing code implementation details and asserting code properties. We hope that our findings can provide a comprehensive understanding of code summarization in the era of LLMs.

## 33. SpecRover: Code Intent Extraction via LLMs

**Authors:** Haifeng Ruan (National University of Singapore), Yuntong Zhang (National University of Singapore), Abhik Roychoudhury (National University of Singapore)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029735

**中文总结:** 提出 SpecRover，在 LLM 智能体中迭代执行代码搜索与规范推断以提取代码意图，并由审查智能体验证补丁与置信度；在完整 SWE-Bench 2294 个 GitHub issue 上评估其程序改进能力。

**Abstract:** Autonomous program improvement typically involves automatically producing bug fixes and feature additions. Such program improvement can be accomplished by a combination of large language model (LLM) and program analysis capabilities, in the form of an LLM agent. Since program repair or program improvement typically requires a specification of intended behavior - specification inference can be useful for producing high quality program patches. In this work, we examine efficient and low-cost workflows for iterative specification inference within an LLM agent. Given a GitHub issue to be resolved in a software project, our goal is to conduct iterative code search accompanied by specification inference - thereby inferring intent from both the project structure and behavior. The intent thus captured is examined by a reviewer agent with the goal of vetting the patches as well as providing a measure of confidence in the vetted patches. Our approach SpecRover is built on the open-source LLM agent AutoCodeRover. In an evaluation on the full SWE-Bench consisting of 2294 GitHub issues, it shows more than 50% improvement in efficacy over AutoCodeRover. Compared to the open-source agents available, our work shows modest cost ($0.65 per issue) in resolving an average GitHub issue in SWE-Bench lite. The production of explanation by SpecRover allows for a better "signal" to be given to the developer, on when the suggested patches can be accepted with confidence. SpecRover also seeks to demonstrate the continued importance of specification inference in automated program repair, even as program repair technologies enter the LLM era.

## 34. Studying Programmers Without Programming: Investigating Expertise Using Resting State fMRI

**Authors:** Zachary Karas (Vanderbilt University), Benjamin Gold (Vanderbilt University), Violet Zhou (University of Michigan), Noah Reardon (University of Michigan), Thad Polk (University of Michigan), Catie Chang (Vanderbilt University), Yu Huang (Vanderbilt University)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029944

**中文总结:** 分析 150 名参与者（含 96 名程序员）静息态 fMRI 数据，发现程序员在语言与数学相关脑区间存在更强功能连接，无需编程任务即可区分编程经验。

**Abstract:** Expert programmers are more effective at coding activities, but the reasons for this remain elusive. Accordingly, recent research has used neuroimaging such as fMRI to analyze how expert programmers might think as they perform coding activities. Those experiments have all involved specific programming tasks (i.e., comprehension), but have been unable to detect systematic differences based on coding experience. By using tasks, however, those studies may limit the number and type of brain networks involved. In Cognitive Neuroscience, researchers commonly analyze resting-state data, in which participants’ brain activity is recorded as they lay idle in the scanner. The brain’s functional organization is plastic, and can change with experience. These changes can be measured at rest, making this a suitable data type for studying how programming activities affect neural organization over time. In this paper, we analyzed the resting state scans from 150 participants, 96 of whom were programmers. We found increased connectivity in programmers between brain regions involved in language, math, and the temporal attention. Non-programmers demonstrated more connectivity with regions involved in social and emotional cognition. We found that as years of programming experience increases, connectivity decreases between two regions associated with visual processing during reading and articulation, respectively.

## 35. Template-Guided Program Repair in the Era of Large Language Models

**Authors:** Kevin Huang, Jian Zhang (Nanyang Technological University), Xiangxin Meng (Beihang University, Beijing, China), Yang Liu (Nanyang Technological University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029846

**中文总结:** 提出 NTR 两阶段神经模板修复框架，先微调 LLM 选择修复模板再引导补丁生成，更好融合传统模板修复与大模型能力。

**Abstract:** Recent advancements in automated program repair (APR) have been significantly driven by the application of Large Language Models (LLMs). In particular, the integration of LLMs with traditional template-based repair methods has demonstrated effective outcomes. Despite this, the synergy between the strengths of traditional methods and LLMs remains underexploited. This oversight originates from the indiscriminate use of templates and their insufficient coverage. Also, using small-scale LLMs within the zero-shot learning context proves to be suboptimal. To alleviate the limitations, we propose NTR (Neural Template Repair), a two-stage repair framework including template selection and patch generation, both of which are under the fine-tuning paradigm. In the template selection phase, we formulate it as a multiclass classification problem and fine-tune million-level LLMs for better selecting possible templates. During the patch generation phase, we leverage the chosen templates as probable directions (e.g., `Mutate Conditional Expression') to guide the fine-tuning process of LLMs at the billion-level scale for precise patch creation. Moreover, we incorporate a unique template to signify the absence of a suitable template and employ a probability-based prioritization of templates, thereby optimizing patch generation. This framework not only effectively addresses template mismatch issues, but also enables the billion-level LLMs to explore the patch space more efficiently, despite the GPU memory constraints. We evaluate NTR with different foundational models on Defects4J V1.2 and HumanEval-Java, the framework consistently demonstrates significant effectiveness. When utilizing StarCoder as the foundational model for patch generation, NTR fixes 128 and 129 bugs in Defects4J and HumanEval, outperforming the best baseline APR tool by 14 and 59 bugs. With the larger CodeLlama model, the fixed bugs rise to 139 and 136, respectively, exceeding the baseline by 25 and 66 bugs. Notably, the performance stems not only from the foundational models but also benefits greatly from our NTR framework. Specifically, NTR's implementation with StarCoder and CodeLlama leads to 22 and 23 additional fixes, which is beyond what the models achieve on their own. This emphasizes the success of our new perspective on utilizing templates to unlock the bug-fixing potential of LLMs.

## 36. The Design Smells Breaking the Boundary between Android Variants and AOSP

**Authors:** Wuxia Jin (Xi'an Jiaotong University), Jiaowei Shang (Xi'an Jiaotong University), Jianguo Zheng (Xi'an Jiaotong University), Mengjie Sun (Xi’an Jiaotong University), Zhenyu Huang (Honor Device Co., Ltd.), Ming Fan (Xi'an Jiaotong University), Ting Liu (Xi'an Jiaotong University)

**Categories:** Evolution and Maintenance, Architecture and Design, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029784

**中文总结:** 刻画破坏 Android 定制版与 AOSP 设计边界的反复设计坏味道，提出 DroidDS 自动检测并验证其与高维护成本相关。

**Abstract:** Phone vendors customize their Android variants to enhance system functionalities based on the Android Open Source Project (AOSP). While independent development, Android variants have to periodically evolve with the upstream AOSP and merge code changes from AOSP. Vendors have invested great effort to maintain their variants and resolve merging conflicts. In this paper, we characterize the design smells with recurring patterns that break the design boundary between Android variants and AOSP. These smells are manifested as problematic dependencies across the boundary, hindering Android variants' maintainability and co-evolution with AOSP. We propose the DroidDS for automatically detecting design smells. We collect 22 Android variant versions and 22 corresponding AOSP versions, involving 4 open-source projects and 1 industrial project. Our results demonstrate that: files involved in design smells consume higher maintenance costs than other files; these infected files are not merely the files with large code size, increased complexity, and object-oriented smells; the infected files have been involved in more than half of code conflicts induced by re-applying AOSP's changes to Android variants; a substantial portion of design issues could be mitigable. Practitioners can utilize our DroidDS to pinpoint and prioritize design problems for Android variants. Refactoring these problems will help keep a healthy coupling between diverse variants and AOSP, potentially improving maintainability and reducing conflict risks.

## 37. TIVER: Identifying Adaptive Versions of C/C++ Third-Party Open-Source Components Using a Code Clustering Technique

**Authors:** Youngjae Choi (Korea University), Seunghoon Woo (Korea University)

**Categories:** Security and Vulnerability, Evolution and Maintenance

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029893

**中文总结:** 提出自适应版本概念与 TIVER 方法，通过函数级细粒度版本识别与 OSS 代码聚类，准确识别 C/C++ 第三方组件的多版本共存与噪声代码。

**Abstract:** Reusing third-party open-source software (OSS) provides many benefits but can expose the entire system to risks owing to propagated vulnerabilities. While tracking the versions of OSS components can help prevent threats, existing approaches typically map a single version to a reused OSS codebase. This coarse-grained method fails to address multiple versions of code that coexist within the codebase, resulting in ineffective OSS management. Additionally, effectively identifying component versions is challenging owing to noise codes, such as algorithmic codes that coexist across different OSS, as well as duplicate components arising from the redundant reuse of OSS. In this paper, we introduce the concept of the adaptive version, a one-stop solution to represent the version diversity of reused OSS. We present TIVER, an effective approach for identifying adaptive versions of OSS components. TIVER employs two key techniques: (1) fine-grained function-level versioning to uncover detailed versions, and (2) OSS code clustering to identify duplicate components and remove noise. This enables precise identification of OSS reuse locations and adaptive versions, effectively mitigating threats related to OSS reuse. Evaluation of popular C/C++ software on GitHub revealed that OSS components with a single version accounted for only 33%, while the remaining 67% of the components contained more than three versions on average. Nonetheless, TIVER effectively identified adaptive versions of OSS components with 88.46% precision and 91.63% recall in duplicate component distinction, and 86% precision and 86.84% recall in eliminating noise, while existing approaches barely achieved 42% recall in distinguishing duplicates and did not address noise. Further experiments showed that TIVER could enhance vulnerability management and be applied to Software Bills of Materials (SBOM) to improve supply chain security.

## 38. UML is Back. Or is it? Investigating the Past, Present, and Future of UML in Open Source Software

**Authors:** Joseph Romeo (Software Institute - USI, Lugano, Switzerland), Marco Raglianti (Software Institute - USI, Lugano), Csaba Nagy, Michele Lanza (Software Institute - USI, Lugano)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029930

**中文总结:** 挖掘约 1.3 万个 GitHub 项目分析二十年来 UML 使用演变，确认开源中 UML 仍被低估但出现复苏迹象。

**Abstract:** Since its inception, UML, the Unified Modeling Language, has been touted as the way to go when it comes to designing and documenting software systems. While being an integral part of many university software engineering programs, UML has found little consideration among developers, especially in open source software. Reasons for this include that UML shares some shortcomings with other forms of documentation (e.g., limited availability, outdatedness, inadequate level of detail). We present a study to investigate the evolution and the current situation regarding the use of UML in open source projects. We mined and analyzed ~13k GitHub projects, developing strategies and heuristics to identify UML files through their extensions and contents, for a quantitative analysis of two decades of evolution of the usage of UML. We explored the popularity of UML, derived characteristics of projects leveraging UML, and analyzed the authors, creators and maintainers, of UML artifacts. Our study confirms that UML is indeed still under-utilized. At the same time we found evidence of a resurgence coinciding with the popularity of human-readable text-based formats, defined and used by tools like PlantUML and Mermaid. We discuss how identifying and addressing the new challenges implied by this resurgence could impact the future of UML.

## 39. Understanding and Detecting Peer Dependency Resolving Loop in npm Ecosystem

**Authors:** Xingyu Wang (Zhejiang University), MingSen Wang (Zhejiang University), Wenbo Shen (Zhejiang University), Rui Chang (Zhejiang University)

**Categories:** Evolution and Maintenance, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029857

**中文总结:** 首次系统研究 npm 生态中 peer 依赖解析陷入无限循环的 PeerSpin 问题，提出基于目录树节点替换冲突的检测方法 NRCPD，可准确高效识别该缺陷。

**Abstract:** As the default package manager for Node.js, npm has become one of the largest package management systems in the world. To facilitate dependency management for developers, npm supports a special type of dependency, Peer Dependency, whose installation and usage differ from regular dependencies. However, conflicts between peer dependencies can trap the npm client into infinite loops, leading to resource exhaustion and system crashes. We name this problem PeerSpin. Although PeerSpin poses a severe risk to ecosystems, it was overlooked by previous studies, and its impacts have not been explored. To bridge this gap, this paper conducts the first in-depth study to understand and detect PeerSpin in the npm ecosystem. First, by systematically analyzing the npm dependency resolution, we identify the root cause of PeerSpin and characterize two peer dependency patterns to guide detection. Second, we propose a novel technique called Node-Replacement-Conflict based PeerSpin Detection, which leverages the state of the directory tree during dependency resolution to achieve accurate and efficient PeerSpin detection. Based on this technique, we developed a tool called PeerChecker to detect PeerSpin. Finally, we apply PeerChecker to the entire NPM ecosystem and find that 5,662 packages, totaling 72,968 versions, suffer from PeerSpin. Up until now, we confirmed 28 real PeerSpin problems by reporting them to the package maintainer. We also open source all PeerSpin analysis implementations, tools, and data sets to the public to help the community detect PeerSpin issues and enhance the reliability of the npm ecosystem.

## 40. Understanding Architectural Complexity, Maintenance Burden, and Developer Sentiment---a Large-Scale Study

**Authors:** Yuanfang Cai (Drexel University), Lanting He (Google), Yony Kochinski (Google), Jun Qian (Google), Ciera Jaspan (Google), Nan Zhang (Google), Antonio Bianco (Google)

**Categories:** Evolution and Maintenance, Human and Social Aspects, Mining Software Repositories, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029733

**中文总结:** 对某公司 1252 个 C++/Java 项目开展大规模研究，量化架构复杂度、维护活动与 7200 份开发者调查情感之间的统计关联。

**Abstract:** Intuitively, the more complex a software system is, the harder it is to maintain. Statistically, it is not clear which complexity metrics correlate with maintenance effort; in fact, it is not even clear how to objectively measure maintenance burden, so that developers' sentiment and intuition can be supported by numbers. Without effective complexity and maintenance metrics, it remains difficult to objectively monitor maintenance, control complexity, or justify refactoring. In this paper, we report a large-scale study of 1252 projects written in C++ and Java from Company_X. We collected three categories of metrics: (1) architectural complexity, measured using propagation cost (PC), decoupling level (DL), and structural anti-patterns; (2) maintenance activity, measured using the number of changes, lines of code (LOC) written, and active coding time (ACT) spent on feature-addition vs. bug-fixing, and (3) developer sentiment on complexity and productivity, collected from 7200 survey responses. We statistically analyzed the correlations among these metrics and obtained significant evidence of the following findings: 1) the more complex the architecture is (higher propagation cost, more instances of anti-patterns), the more LOC is spent on bug-fixing, rather than adding new features; 2) developers who commit more changes for features, spend more lines of code on features, or spend more time on features also feel that they are less hindered by technical debt and complexity. To the best of our knowledge, this is the first large-scale empirical study establishing the statistical correlation among architectural complexity, maintenance activity, and developer sentiment. The implication is that, instead of solely relying upon developer sentiment and intuition to detect degraded structure or increased burden to evolve, it is possible to objectively and continuously measure and monitor architectural complexity and maintenance difficulty, increasing feature delivery efficiency by reducing architectural complexity and anti-patterns.

## 41. Understanding the Response to Open-Source Dependency Abandonment in the npm Ecosystem

**Authors:** Courtney Miller (Carnegie Mellon University), Mahmoud Jahanshahi (University of Tennessee), Audris Mockus (University of Tennessee), Bogdan Vasilescu (Raj Reddy Associate Professor of Software and Societal Systems, Carnegie Mellon University, USA), Christian Kästner (Carnegie Mellon University)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029865

**中文总结:** 大规模分析 npm 广泛使用包的依赖弃用现象，发现弃用常见、大量下游项目暴露且常未响应；并给出透明度与项目 sunset 实践建议。

**Abstract:** Many developers relying on open-source digital infrastructure expect continuous maintenance, but even the most critical packages can become unmaintained. Despite this, there is little understanding of the prevalence of abandonment of widely-used packages, of subsequent exposure, and of reactions to abandonment in practice, or the factors that influence them. We perform a large-scale quantitative analysis of all widely-used npm packages and find that abandonment is common among them, that abandonment exposes many projects which often do not respond, that responses correlate with other dependency management practices, and that removal is significantly faster when a projects end-of-life status is explicitly stated. We end with recommendations to both researchers and practitioners who are facing dependency abandonment or are sunsetting projects, such as opportunities for low-effort transparency mechanisms to help exposed projects make better, more informed decisions.

## 42. Unleashing the True Potential of Semantic-based Log Parsing with Pre-trained Language Models

**Authors:** Van-Hoang Le (The University of Newcastle), Yi Xiao, Hongyu Zhang (Chongqing University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029829

**中文总结:** 提出 UNLEASH 语义日志解析方法，通过三项增强策略提升小型 PLM 性能，证明经优化的 RoBERTa 等模型可在更低成本下达到或超越 LLM 基线解析效果。

**Abstract:** Software-intensive systems often produce console logs for troubleshooting purpose. Log parsing, which aims at parsing a log message into a specific log template, typically serves as the first step toward automated log analytics. To better comprehend semantic information of log messages, many semantic-based log parsers have been proposed. These log parsers fine-tune a small pretrained language model (PLM) such as RoBERTa on a few labelled log samples. With the increasing popularity of large language models (LLMs), some recent studies also propose to leverage LLMs such as ChatGPT through in-context learning for automated log parsing, and obtain better results than previous semantic-based log parsers with small PLMs. In this paper, we show that semantic-based log parsers with small PLMs can actually achieve better or comparable performance to state-of-the-art LLM-based log parsing models while being more efficient and cost-effective. We propose UNLEASH, a novel semantic-based log parsing approach, which incorporates three enhancement methods to boost the performance of PLMs for log parsing, including (1) an entropy-based ranking method to select the most informative log samples; (2) a contrastive learning method to enhance the fine-tuning process; and (3) an inference optimization method to improve the log parsing performance. We evaluate UNLEASH on a set of large log datasets and the experimental results show that UNLEASH is effective and efficient, when compared to state-of-the-art log parsers.
