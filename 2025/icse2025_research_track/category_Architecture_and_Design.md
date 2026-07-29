# ICSE 2025 Research Track — Architecture and Design

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 18 papers

## 1. A Catalog of Micro Frontends Anti-patterns

**Authors:** Nabson Silva (UFAM - Federal University of Amazonas), Eriky Rodrigues (UFAM - Federal University of Amazonas Brazil), Tayana Conte (Universidade Federal do Amazonas)

**Categories:** Architecture and Design

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029739

**中文总结:** 基于微服务反模式与行业实践归纳 12 种微前端反模式目录，并经从业者调查验证其在真实项目中的普遍性与危害。

**Abstract:** Micro frontend (MFE) architectures have gained significant popularity for promoting independence and modularity in development. Despite their widespread adoption, the field remains relatively unexplored, especially concerning identifying problems and documenting best practices. Drawing on both established microservice (MS) anti-patterns and the analysis of real problems faced by software development teams that adopt MFE, this paper presents a catalog of 12 MFE anti-patterns. We composed an initial version of the catalog by recognizing parallels between MS anti-patterns and recurring issues in MFE projects to map and adapt MS anti-patterns to the context of MFE. To validate the identified problems and proposed solutions, we conducted a survey with industry practitioners, collecting valuable feedback to refine the anti-patterns. Additionally, we asked participants if they had encountered these problems in practice and to rate their harmfulness on a 10-point Likert scale. The survey results revealed that participants had encountered all the proposed anti-patterns in real-world MFE architectures, with only one reported by less than 50% of participants. They stated that the catalog can serve as a valuable guide for both new and experienced developers, with the potential to enhance MFE development quality. The collected feedback led to the development of a improved version of the anti-patterns catalog. Furthermore, we developed a web application designed to not only showcase the anti-patterns but also to actively foster collaboration and engagement within the MFE community. The proposed catalog is a valuable resource for identifying and mitigating potential pitfalls in MFE development. It empowers developers of all experience levels to create more robust, maintainable, and well-designed MFE applications.

## 2. A Large-Scale Study of Model Integration in ML-Enabled Software Systems

**Authors:** Yorick Sens (Ruhr University Bochum), Henriette Knopp (Ruhr University Bochum), Sven Peldszus (Ruhr University Bochum), Thorsten Berger (Ruhr University Bochum)

**Categories:** Software Engineering for AI, Architecture and Design

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029853

**中文总结:** 大规模研究 ML 赋能软件系统中的模型集成拓扑与工程实践，揭示多模型组合、维护与复用方面的真实特征与挑战。

**Abstract:** The rise of machine learning (ML) and its embedding in software-intensive systems has drastically changed the engineering of such systems. Traditionally, software engineering focuses on manually created artifacts, such as source code, and the process of creating them, as well as best practices for integrating them, i.e., software architectures. In contrast, the development of ML artifacts, i.e., ML models, comes from data science and focuses on the ML models and their training data. However, to deliver value to end users, these ML models must be integrated with traditional software components, often forming complex topologies. In fact, ML-enabled software can easily incorporate many different ML models. While the challenges and practices of building ML-enabled systems have been studied, little is known about the characteristics of real-world ML-enabled systems, beyond isolated examples. Properly embedding ML models in systems so that they can be easily maintained or reused is far from trivial. To improve development processes and architectures for ML-enabled systems, we need to improve our empirical understanding of these systems. We present the first large-scale study of real-world open-source ML-enabled software systems, covering over 2,928 systems on GitHub. We classified and analyzed them to determine their characteristics, as well as their practices for reusing ML models and related code, and the architecture of these systems. Practitioners and researchers benefit from insights into practices for embedding and integrating ML models, bringing data science and software engineering closer together.

## 3. An Exploratory Study on the Engineering of Security Features

**Authors:** Kevin Hermann (Ruhr University Bochum), Sven Peldszus (Ruhr University Bochum), Jan-Philipp Steghöfer (XITASO GmbH IT & Software Solutions), Thorsten Berger (Ruhr University Bochum)

**Categories:** Security and Vulnerability, Architecture and Design

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029861

**中文总结:** 对 26 名从业者开展安全特性工程探索性研究，揭示开发者如何选择、设计、集成与维护加密与访问控制等安全功能的实践与维护代价。

**Abstract:** Software security is of utmost importance for most software systems. Developers must systematically select, plan, design, implement, and especially maintain and evolve security features - functionalities to mitigate attacks or protect personal data such as cryptography or access control, to ensure the security of their software. While security features are usually available in libraries, additional code needs to be written and maintained to integrate security features and not all desired features can be reused this way. While there have been studies on the use of such libraries, surprisingly little is known about how developers engineer security features, how they select what security features to implement, and the implications on maintenance. We therefore currently rely on assumptions that are largely based on common sense or individual examples. However, researchers require hard empirical data to understand what practitioners need and how they view security, which we currently lack to provide them with effective solutions. We contribute an exploratory study with 26 knowledgeable industrial participants. We study how security features of software systems are selected and engineered in practice, what their code-level characteristics are, and the challenges practitioners face. Based on the empirical data gathered, we validate four common assumptions and gain insights into engineering practices.

## 4. An LLM-Based Agent-Oriented Approach for Automated Code Design Issue Localization

**Authors:** Fraol Batole (Tulane University), David OBrien (Iowa State University), Tien N. Nguyen (University of Texas at Dallas), Robert Dyer (University of Nebraska-Lincoln), Hridesh Rajan (Tulane University)

**Categories:** AI for Software Engineering, Architecture and Design

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029742

**中文总结:** 提出 LOCALIZEAGENT 多智能体框架，将程序分析输出转为 LLM 可理解的抽象表示并协同定位模块化差、复杂度过高等设计问题，克服大代码库超出上下文窗口的局限。

**Abstract:** Maintaining software design quality is crucial for the long-term maintainability and evolution of systems. However, design issues such as poor modularity and excessive complexity often emerge as codebases grow. Developers rely on external tools, such as program analysis techniques, to identify such issues. This work investigates an automated approach for analyzing and localizing design issues using Large Language Models (LLMs). Large language models have demonstrated significant performance on coding tasks, but directly leveraging them for design issue localization is challenging. Large codebases exceed typical LLM context windows, and program analysis tool outputs in non-textual modalities (e.g., graphs or interactive visualizations) are incompatible with LLMs’ natural language inputs. To address these challenges, we propose LOCALIZEAGENT, a novel multi-agent framework for effective design issue localization. LOCALIZEAGENT integrates specialized agents that (1) analyze code to identify potential code design issues, (2) transform program analysis outputs into abstraction-aware LLM-friendly natural language summaries, (3) generate context-aware prompts tailored to specific refactoring types, and (4) leverage LLMs to locate and rank the localized issues based on their relevance. Our evaluation using diverse real-world codebases demonstrates significant improvements over baseline approaches, with LOCALIZEAGENT achieving 138%, 166%, and 206% relative improvements in exact match accuracy for localizing information hiding, complexity, and modularity issues, respectively.

## 5. Are LLMs Correctly Integrated into Software Systems?

**Authors:** Yuchen Shao (East China Normal University), Yuheng Huang (the University of Tokyo), Jiawei Shen (East China Normal University), Lei Ma (The University of Tokyo & University of Alberta), Ting Su (East China Normal University), Chengcheng Wan (East China Normal University)

**Categories:** Software Engineering for AI, Architecture and Design

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029854

**中文总结:** 研究 100 个集成 LLM 与 RAG 的开源应用，识别 18 种集成缺陷模式（77% 应用含三种以上），提出修复指南并构建缺陷库 Hydrangea。

**Abstract:** Large language models (LLMs) provide effective solutions in various application scenarios, with the support of retrieval-augmented generation (RAG). However, developers face challenges in integrating LLM and RAG into software systems, due to lacking interface specifications, various requirements from software context, and complicated system management. In this paper, we have conducted a comprehensive study of 100 open-source applications that incorporate LLMs with RAG support, and identified 18 defect patterns. Our study reveals that 77% of these applications contain more than three types of integration defects that degrade software functionality, efficiency, and security. Guided by our study, we propose systematic guidelines for resolving these defects in software life cycle. We also construct an open-source defect library Hydrangea.

## 6. Coni: Detecting Database Connector Bugs via State-Aware Test Case Generation

**Authors:** Wenqian Deng (Tsinghua University), Zhiyong Wu (Tsinghua University, China), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Mingzhe Wang (Tsinghua University), Yu Jiang (Tsinghua University)

**Categories:** Testing and Quality, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029870

**中文总结:** 提出 CONI，面向数据库连接器做状态感知测试生成，并通过与参考连接器对比结果找逻辑缺陷；在 5 个主流 JDBC 驱动上发现 44 个未知缺陷（34 个已确认）。

**Abstract:** Database connectors are widely used in many applications to facilitate flexible and convenient database interactions. Potential vulnerabilities in database connectors can lead to various abnormal behaviors within applications, such as returning incorrect results or experiencing unexpected connection interruption. However, existing fuzzing works cannot be directly applied to testing database connectors as they mainly focus on SQL generation and use a small subset of database connector interfaces to execute SQLs. Due to a lack of domain knowledge, automated test case generation also struggles to generate complex test cases that explore connectors' deep logic. The main challenge in testing database connectors is to generate semantically correct test cases that can trigger a wide range of connector state transitions. To address that, we propose CONI, a framework designed for detecting logic bugs of database connectors with state-aware test case generation. First, we define the database connector state model by analyzing the corresponding specification. Building upon this model, CONI generates interface call sequences within test cases to encompass more connector state transitions. After that, CONI generates suitable parameter values based on the parameter information and contextual information collected during runtime. Then the test cases are executed on a target and a reference database connector. Inconsistent results indicate potential logic bugs. We evaluate CONI on 5 widely-used JDBC database connectors, namely MySQL Connector/J, MariaDB Connector/J, AWS JDBC Driver for MySQL, PGJDBC NG, and PostgreSQL JDBC Driver. In total, CONI successfully detected 44 previously unknown bugs, of which 34 have been confirmed.

## 7. DesignRepair: Dual-Stream Design Guideline-Aware Frontend Repair with Large Language Models

**Authors:** Mingyue Yuan (The university of new South Wales), Jieshan Chen (CSIRO's Data61), Zhenchang Xing (CSIRO's Data61), Aaron Quigley (CSIRO's Data61), Yuyu Luo (HKUST (GZ)), Tianqi Luo (HKUST (GZ)), Gelareh Mohammadi (The university of new South Wales), Qinghua Lu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** Testing and Quality, Program Analysis and Verification, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11030228

**中文总结:** 提出 DesignRepair 双流前端修复系统，结合 Material Design 知识库、大语言模型与 Playwright 从代码与渲染页两面对齐设计规范。

**Abstract:** The rise of Large Language Models (LLMs) has streamlined frontend interface creation through tools like Vercel's V0, yet surfaced challenges in design quality (e.g., accessibility, and usability). Current solutions, often limited by their focus, generalisability, or data dependency, fall short in addressing these complexities comprehensively. Moreover, none of them examine the quality of LLM-generated UI design. In this work, we introduce DesignRepair, a novel dual-stream design guideline-aware system to examine and repair the UI design quality issues from both code aspect and rendered page aspect. We utilised the mature and popular Material Design as our knowledge base to guide this process. Specifically, we first constructed a comprehensive knowledge base encoding Google's Material Design principles into low-level component knowledge base and high-level system design knowledge base. After that, DesignRepair employs a LLM for the extraction of key components and utilizes the Playwright tool for precise page analysis, aligning these with the established knowledge bases. Finally, we integrate Retrieval-Augmented Generation with state-of-the-art LLMs like GPT-4 to holistically refine and repair frontend code through a strategic divide and conquer approach. Our extensive evaluations validated the efficacy and utility of our approach, demonstrating significant enhancements in adherence to design guidelines, accessibility, and user experience metrics.

## 8. Distilled Lifelong Self-Adaptation for Configurable Systems

**Authors:** Yulong Ye (University of Birmingham), Tao Chen (University of Birmingham), Miqing Li (University of Birmingham)

**Categories:** AI for Software Engineering, Architecture and Design

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029783

**中文总结:** 提出 DLiSA 框架，通过终身规划与蒸馏知识播种使可配置系统在时变负载下持续自适配并优化运行时与吞吐量等性能。

**Abstract:** Modern configurable systems provide tremendous opportunities for engineering future intelligent software systems. A key difficulty thereof is how to effectively self-adapt the configuration of a running system such that its performance (e.g., runtime and throughput) can be optimized under time-varying workloads. This unfortunately remains unaddressed in existing approaches as they either overlook the available past knowledge or rely on static exploitation of past knowledge without reasoning the usefulness of information when planning for self-adaptation. In this paper, we tackle this challenging problem by proposing DLiSA, a framework that self-adapts configurable systems. DLiSA comes with two properties: firstly, it supports lifelong planning, and thereby the planning process runs continuously throughout the lifetime of the system, allowing dynamic exploitation of the accumulated knowledge for rapid adaptation. Secondly, the planning for a newly emerged workload is boosted via distilled knowledge seeding, in which the knowledge is dynamically purified such that only useful past configurations are seeded when necessary, mitigating misleading information. Extensive experiments suggest that the proposed DLiSA significantly outperforms state-of-the-art approaches, demonstrating a performance improvement of up to 255\% and a resource acceleration of up to 2.22$\times$ on generating promising adaptation configurations. All data and sources can be found at our anonymous site: https://github.com/Anonymous-DLiSA/DLiSA.

## 9. Enhancing Fault Localization in Industrial Software Systems via Contrastive Learning

**Authors:** Chun Li (Nanjing University), Hui Li (Samsung Electronics (China) R&D Centre), Zhong Li, Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Program Analysis and Verification, Evolution and Maintenance, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029934

**中文总结:** 提出 FALCON，将工业日志组织为图并用对比学习区分通过/失败运行以定位故障；相较 34 种谱方法与 4 种学习方法整体表现最优。

**Abstract:** Engineers utilize logs as a primary resource for fault localization in large-scale software and system testing, a process that is notoriously time-consuming, costly, and labor-intensive. Despite considerable progress in automated fault localization approaches, their applicability remains limited in such settings, due to the unavailability of fine-grained features in logs essential for most existing fault localization methods. In response, we introduce FALCON, a novel log-based fault localization framework. FALCON organizes complex semantic log information into graphical representations and employs contrastive learning to capture the differences between passed and failed logs, enabling the identification of crucial fault-related features. It also incorporates a specifically designed transitive analysis-based adaptive graph augmentation to minimize the influence of fault-unrelated log information on contrastive learning. Through extensive evaluations against 34 spectrum-based and 4 learning-based fault localization methods, FALCON demonstrates superior performance by outperforming all the methods in comparison. In addition, FALCON demonstrated its practical value by successfully identifying 71 out of 90 faults with a file-level Top-1 accuracy rate during a one-month deployment within a global company’s testing system.

## 10. Fidelity of Cloud Emulators: The Imitation Game of Testing Cloud-based Software

**Authors:** Anna Mazhar (Cornell University), Saad Sher Alam (University of Illinois Urbana-Champaign), William Zheng (University of Illinois Urbana-Champaign), Yinfang Chen (University of Illinois at Urbana-Champaign), Suman Nath (Microsoft Research), Tianyin Xu (University of Illinois at Urbana-Champaign)

**Categories:** Testing and Quality, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029917

**中文总结:** 系统分析 Azure 与 AWS 五类云服务的 255 个 API，发现 37% 在模拟器与真实服务间行为不一致，威胁离线测试可信度。

**Abstract:** Modern software projects have been increasingly using cloud services as important components. The cloud-based programming practice greatly simplifies software development by harvesting cloud benefits (e.g., high availability and elasticity). However, it imposes new challenges for software testing and analysis, due to opaqueness of cloud backends and monetary cost of invoking cloud services for continuous integration and deployment. As a result, cloud emulators are developed for offline development and testing, before online testing and deployment. This paper presents a systematic analysis of cloud emulators from the perspective of cloud-based software testing. Our goal is to (1) understand the discrepancies introduced by cloud emula- tion with regard to software quality assurance and deployment safety and (2) address inevitable gaps between emulated and real cloud services. The analysis results are concerning. Among 255 APIs of five cloud services from Azure and Amazon Web Services (AWS), we detected discrepant behavior between the emulated and real services in 94 (37%) of the APIs. These discrepancies lead to inconsistent testing results, threatening deployment safety, introducing false alarms, and creating debuggability issues. The root causes are diverse, including accidental implementation defects and essential emulation challenges. We discuss potential solutions and develop a practical mitigation technique to address discrepancies of cloud emulators for software testing.

## 11. Formally Verified Cloud-Scale Authorization

**Authors:** Aleks Chakarov (Amazon Web Services), Jaco Geldenhuys (Amazon Web Services), Matthew Heck (Amazon Web Services), MIchael Hicks (Amazon), Samuel Huang (Amazon Web Services), Georges-Axel Jaloyan (Amazon Web Services), Anjali Joshi (Amazon), K. Rustan M. Leino (Amazon), Mikael Mayer (Automated Reasoning Group, Amazon Web Services), Sean McLaughlin (Amazon Web Services), Akhilesh Mritunjai (Amazon.com), Clement Pit-Claudel (EPFL), Sorawee Porncharoenwase (Amazon Web Services), Florian Rabe (Amazon Web Services), Marianna Rapoport (Amazon Web Services), Giles Reger (Amazon Web Services), Cody Roux (Amazon Web Services), Neha Rungta (Amazon Web Services), Robin Salkeld (Amazon Web Services), Matthias Schlaipfer (Amazon Web Services), Daniel Schoepe (Amazon), Johanna Schwartzentruber (Amazon Web Services), Serdar Tasiran (Amazon, n.n.), Aaron Tomb (Amazon), Emina Torlak (Amazon Web Services, USA), Jean-Baptiste Tristan (Amazon), Lucas Wagner (Amazon Web Services), Michael Whalen (Amazon Web Services and the University of Minnesota), Remy Willems (Amazon), Tongtong Xiang (Amazon Web Services), Taejoon Byun (University of Minnesota), Joshua M. Cohen (Princeton University), Ruijie Fang (University of Texas at Austin), Junyoung Jang (McGill University), Jakob Rath (TU Wien), Hira Taqdees Syeda, Dominik Wagner (University of Oxford), Yongwei Yuan (Purdue University)

**Categories:** Security and Vulnerability, Evolution and Maintenance, Human and Social Aspects, Architecture and Design

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029876

**中文总结:** 使用 Dafny 形式化验证重建每秒十亿次调用的云级授权引擎，2024 年无事故上线并使客户性能提升三倍。

**Abstract:** All critical systems must evolve to meet the needs of a growing and diversifying user base. But supporting that evolution is challenging at increasing scale: Maintainers must find a way to ensure that each change does only what is intended, and will not inadvertently change behavior for existing users. This paper presents how we addressed this challenge for a cloud-scale authorization engine, invoked 1 billion times per second, by using formal verification. Over a period of four years, we built a new authorization engine, one that behaves functionally the same as its predecessor, using the verification-aware programming language Dafny. We can now confidently deploy enhancements and optimizations while maintaining the highest assurance of both correctness and backward compatibility. We deployed the new engine in 2024 without incident and customers immediately enjoyed a threefold performance improvement. The methodology we followed to build this new engine was not an off-the-shelf application of an existing verification tool, and this paper presents several key insights: 1) Rather than prove correct the existing engine, written in Java, we found it more effective to \emph{write a new engine} in Dafny, a language built for \emph{verification from the ground up}, and then compile the result to Java. 2) To ensure performance, debuggability, and to gain trust from stakeholders, we needed to generate readable, \emph{idiomatic} Java code, essentially a transliteration of the source Dafny. 3) To ensure that the specification matches the system's actual behavior, we performed \emph{extensive differential and shadow testing} throughout the development process, ultimately comparing against $10^{15}$ production samples prior to deployment. Our approach demonstrates how formal verification can be effectively applied to evolve critical legacy software at scale.

## 12. PairSmell: A Novel Perspective Inspecting Software Modular Structure

**Authors:** Chenxing Zhong (Nanjing University), Daniel Feitosa (University of Groningen), Paris Avgeriou (Univ. of Gronningen), Huang Huang (State Grid Nanjing Power Supply Company), Yue Li (Nanjing University), He Zhang (Nanjing University)

**Categories:** Evolution and Maintenance, Architecture and Design

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029796

**中文总结:** 提出 PairSmell 概念，以实体对的模块化关系（应分离或共置）与多工具共识的“适宜关系”对比识别需重构的架构决策；在 20 个 C/C++ 系统上实证评估。

**Abstract:** Enhancing the modular structure of existing systems has attracted substantial research interest, focusing on two main methods: (1) software modularization and (2) identifying design issues (e.g., smells) as refactoring opportunities. However, re-modularization solutions often require extensive modifications to the original modules, and the design issues identified are generally too coarse to guide refactoring strategies. Combining the above two methods, this paper introduces a novel concept, \emph{PairSmell}, which exploits modularization to pinpoint design issues necessitating refactoring. We concentrate on a granular but fundamental aspect of modularity principles---\emph{modular relation (MR)}, i.e., \emph{whether a pair of entities are separated or collocated}. The main assumption is that, if the actual MR of a pair violates its `apt MR', i.e., an MR agreed on by multiple modularization tools (as raters), it can be deemed likely a flawed architectural decision that necessitates further examination. To quantify and evaluate \emph{PairSmell}, we conduct an empirical study on 20 C/C++ and Java projects, using 4 established modularization tools to identify two forms of \emph{PairSmell}: inapt separated pairs $\mathit{InSep}$ and inapt collocated pairs $\mathit{InCol}$. Our study on 260,003 instances reveals that their architectural impacts are substantial: (1) on average, 14.60\% and 20.44\% of software entities are involved in $\mathit{InSep}$ and $\mathit{InCol}$ MRs respectively; (2) $\mathit{InSep}$ pairs are associated with 190\% more co-changes than properly separated pairs, while $\mathit{InCol}$ pairs are associated with 35\% fewer co-changes than properly collocated pairs, both indicating a successful identification of modular structures detrimental to software quality; and (3) both forms of \emph{PairSmell} persist across software evolution. This evidence strongly suggests that \emph{PairSmell} can provide meaningful insights for inspecting modular structure, with the identified issues being both granular and fundamental, making the enhancement of modular design more efficient.

## 13. Pattern-based Generation and Adaptation of Quantum Workflows

**Authors:** Martin Beisel (Institute of Architecture of Application Systems (IAAS), University of Stuttgart), Johanna Barzen (University of Stuttgart), Frank Leymann (University of Stuttgart), Lavinia Stiliadou (Institute of Architecture of Application Systems (IAAS), University of Stuttgart), Daniel Vietz (University of Stuttgart), Benjamin Weder (Institute of Architecture of Application Systems (IAAS), University of Stuttgart)

**Categories:** Evolution and Maintenance, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029719

**中文总结:** 基于量子计算模式语言，自动从模式生成并适配编排异质量子组件的量子工作流，降低手工建模与配置的复杂度与出错率。

**Abstract:** Building quantum applications requires deep knowledge of quantum computing and software engineering. Hence, an abstraction layer reducing the complexity for non-experts is needed. Patterns are an established concept for the abstract description of proven solutions to recurring problems. Therefore, the quantum computing patterns, a pattern language for the quantum computing domain, can be used to define the building blocks and the structure of hybrid quantum applications. Furthermore, concrete software artifacts can be associated with patterns to solve the corresponding problem. However, these software artifacts are usually heterogeneous, e.g., using different data formats. Quantum workflows enable a robust and scalable orchestration of these heterogeneous software artifacts. However, manually modeling and configuring such quantum workflows is a complex, error-prone, and time-consuming task. To overcome this issue, we present an approach that automates the generation and adaptation of quantum workflows using the quantum computing patterns. We provide an architecture realizing our approach, a corresponding prototype, as well as an evaluation comprising different use cases, a runtime comparison, and a user study.

## 14. Puppy: Finding Performance Degradation Bugs in DBMSs via Limited-Optimization Plan Construction

**Authors:** Zhiyong Wu (Tsinghua University, China), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Mingzhe Wang (Tsinghua University), Yu Jiang (Tsinghua University)

**Categories:** Evolution and Maintenance, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029960

**中文总结:** 提出 Puppy，通过对比「全优化」与「受限优化」执行计划来发现 DBMS 性能退化缺陷（PDB）；在多个数据库上检出 62 个 PDB，其中 54 个为未知缺陷。

**Abstract:** Database management systems (DBMSs) consistently strive for enhanced performance. For a given query, the optimizer of a DBMS aims to construct an optimal execution plan that incorporates multiple optimization operations. However, the resulting plan may sometimes perform worse than even if no optimizations were applied. This occurs because the interactions between optimizations are complex and some situations might be overlooked in the implementation. We refer to these issues as Performance Degradation Bugs (PDBs). PDBs can result in significant consequences from decreased system efficiency and prolonged query processing times to potential disruptions in critical business operations. In this paper, we present Puppy, an automated approach for detecting PDBs in DBMSs using limited-optimization plan construction. The key idea is to compare the performance with the plan generated with all optimization operations enabled, against the plan generated with only a subset of optimization operations in the same DBMS. If the response time of the plan with the limited optimization set is shorter than that of the fully optimized plan, it indicates a potential PDB. Specifically, Puppy first generates queries that incorporate multiple optimization sequences, guided by optimization operation sequence coverage. Secondly, Puppy analyzes the query plan and selectively disables specific optimizations to construct the limited optimization plan. We evaluate Puppy on five widely-used DBMSs, namely MySQL, Percona, TiDB, PolarDB, and PostgreSQL against the state-of-the-art DBMS performance testing tools APOLLO and AMOEBA. Puppy detected 26 and 25 more performance anomalies, covered 151,201 and 173,798 more branches than APOLLO and AMOEBA in 48 hours, respectively. More importantly, Puppy reports 62 PDBs, with 54 anomalies confirmed as previously unknown bugs.

## 15. Thanos: DBMS Bug Detection via Storage Engine Rotation Based Differential Testing

**Authors:** Ying Fu (National University of Defense Technology), Zhiyong Wu (Tsinghua University, China), Yuanliang Zhang (National University of Defense Technology), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Yu Jiang (Tsinghua University), Shanshan Li (National University of Defense Technology), Liao Xiangke (National University of Defense Technology)

**Categories:** Testing and Quality, Architecture and Design

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029942

**中文总结:** 提出 Thanos，通过轮换同一 DBMS 的不同存储引擎构造等价系统做差分测试，在 MySQL、MariaDB、Percona 等广泛测试的数据库上发现缺陷。

**Abstract:** Differential testing is a prevalent strategy for establishing test oracles in automated DBMS testing. However, meticulously selecting equivalent DBMSs with diverse implementations and compatible input syntax requires huge manual efforts. In this paper, we propose Thanos, a framework that finds DBMS bugs via storage engine rotation based differential testing. Our key insight is that a DBMS with different storage engines must provide consistent basic storage functionalities. Therefore, it’s feasible to construct equivalent DBMSs based on storage engine rotation, ensuring that the same SQL test cases to these equivalent DBMSs yield consistent results. The framework involves four main steps: 1) select the appropriate storage engines; 2) extract equivalence information among the selected storage engines; 3) synthesize feature-orient test cases that ensure the DBMS equivalence; and 4) send test cases to the DBMSs with selected storage engines and compare the results. We evaluate Thanos on three widely used and extensively tested DBMSs, namely MySQL, MariaDB, and Percona against state-of-the-art fuzzers SQLancer, SQLsmith, and Squirrel. Thanos outperforms them on branch coverage by 24%–116%, and also finds many bugs missed by other fuzzers. More importantly, the vendors have confirmed 32 previously unknown bugs found by Thanos, with 29 verified as Critical.

## 16. The Design Smells Breaking the Boundary between Android Variants and AOSP

**Authors:** Wuxia Jin (Xi'an Jiaotong University), Jiaowei Shang (Xi'an Jiaotong University), Jianguo Zheng (Xi'an Jiaotong University), Mengjie Sun (Xi’an Jiaotong University), Zhenyu Huang (Honor Device Co., Ltd.), Ming Fan (Xi'an Jiaotong University), Ting Liu (Xi'an Jiaotong University)

**Categories:** Evolution and Maintenance, Architecture and Design, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029784

**中文总结:** 刻画破坏 Android 定制版与 AOSP 设计边界的反复设计坏味道，提出 DroidDS 自动检测并验证其与高维护成本相关。

**Abstract:** Phone vendors customize their Android variants to enhance system functionalities based on the Android Open Source Project (AOSP). While independent development, Android variants have to periodically evolve with the upstream AOSP and merge code changes from AOSP. Vendors have invested great effort to maintain their variants and resolve merging conflicts. In this paper, we characterize the design smells with recurring patterns that break the design boundary between Android variants and AOSP. These smells are manifested as problematic dependencies across the boundary, hindering Android variants' maintainability and co-evolution with AOSP. We propose the DroidDS for automatically detecting design smells. We collect 22 Android variant versions and 22 corresponding AOSP versions, involving 4 open-source projects and 1 industrial project. Our results demonstrate that: files involved in design smells consume higher maintenance costs than other files; these infected files are not merely the files with large code size, increased complexity, and object-oriented smells; the infected files have been involved in more than half of code conflicts induced by re-applying AOSP's changes to Android variants; a substantial portion of design issues could be mitigable. Practitioners can utilize our DroidDS to pinpoint and prioritize design problems for Android variants. Refactoring these problems will help keep a healthy coupling between diverse variants and AOSP, potentially improving maintainability and reducing conflict risks.

## 17. The Same Only Different: On Information Modality for Configuration Performance Analysis

**Authors:** Hongyuan Liang (University of Electronic Science and Technology of China), Yue Huang (University of Electronic Science and Technology of China), Tao Chen (University of Birmingham)

**Categories:** Testing and Quality, Architecture and Design

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029750

**中文总结:** 在 10 个系统、1694 个配置项上实证比较手册与源码两种信息模态在配置性能分析中的作用，澄清二者在不同分析任务中的互补性与局限。

**Abstract:** Configuration in software systems helps to ensure efficient operation and meet diverse user needs. Yet, some, if not all, configuration options have profound implications for the system's performance. Configuration performance analysis, wherein the key is to understand (or infer) the configuration options' relations and their impacts on performance, is crucial. Two major modalities exist that serve as the source information in the analysis: either the manual or source code. However, it remains unclear what roles they play in configuration performance analysis. Much work that relies on manuals claims their benefits of information richness and naturalness; while work that trusts the source code more prefers the structural information provided therein and criticizes the timeliness of manuals. To fill such a gap, in this paper, we conduct an extensive empirical study over 10 systems, covering 1,694 options, 106,798 words in the manual, and 22,859,552 lines-of-code for investigating the usefulness of manual and code in two important tasks of configuration performance analysis, namely performance-sensitive options identification and the associated dependencies extraction. We reveal several new findings and insights, such as it is beneficial to fuse the manual and code modalities for both tasks; the current automated tools that rely on a single modality are far from being practically useful and generally remain incomparable to human analysis. All those pave the way for further advancing configuration performance analysis.

## 18. Understanding Architectural Complexity, Maintenance Burden, and Developer Sentiment---a Large-Scale Study

**Authors:** Yuanfang Cai (Drexel University), Lanting He (Google), Yony Kochinski (Google), Jun Qian (Google), Ciera Jaspan (Google), Nan Zhang (Google), Antonio Bianco (Google)

**Categories:** Evolution and Maintenance, Human and Social Aspects, Mining Software Repositories, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029733

**中文总结:** 对某公司 1252 个 C++/Java 项目开展大规模研究，量化架构复杂度、维护活动与 7200 份开发者调查情感之间的统计关联。

**Abstract:** Intuitively, the more complex a software system is, the harder it is to maintain. Statistically, it is not clear which complexity metrics correlate with maintenance effort; in fact, it is not even clear how to objectively measure maintenance burden, so that developers' sentiment and intuition can be supported by numbers. Without effective complexity and maintenance metrics, it remains difficult to objectively monitor maintenance, control complexity, or justify refactoring. In this paper, we report a large-scale study of 1252 projects written in C++ and Java from Company_X. We collected three categories of metrics: (1) architectural complexity, measured using propagation cost (PC), decoupling level (DL), and structural anti-patterns; (2) maintenance activity, measured using the number of changes, lines of code (LOC) written, and active coding time (ACT) spent on feature-addition vs. bug-fixing, and (3) developer sentiment on complexity and productivity, collected from 7200 survey responses. We statistically analyzed the correlations among these metrics and obtained significant evidence of the following findings: 1) the more complex the architecture is (higher propagation cost, more instances of anti-patterns), the more LOC is spent on bug-fixing, rather than adding new features; 2) developers who commit more changes for features, spend more lines of code on features, or spend more time on features also feel that they are less hindered by technical debt and complexity. To the best of our knowledge, this is the first large-scale empirical study establishing the statistical correlation among architectural complexity, maintenance activity, and developer sentiment. The implication is that, instead of solely relying upon developer sentiment and intuition to detect degraded structure or increased burden to evolve, it is possible to objectively and continuously measure and monitor architectural complexity and maintenance difficulty, increasing feature delivery efficiency by reducing architectural complexity and anti-patterns.
