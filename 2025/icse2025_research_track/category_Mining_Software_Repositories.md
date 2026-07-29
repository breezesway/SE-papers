# ICSE 2025 Research Track — Mining Software Repositories

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 12 papers

## 1. An Empirical Study of Proxy Smart Contracts at the Ethereum Ecosystem Scale

**Authors:** Mengya Zhang (The Ohio State University), Preksha Shukla (George Mason University), Wuqi Zhang (Mega Labs), Zhuo Zhang (Purdue University), Pranav Agrawal (George Mason University), Zhiqiang Lin (The Ohio State University), Xiangyu Zhang (Purdue University), Xiaokuan Zhang (George Mason University)

**Categories:** Security and Vulnerability, Mining Software Repositories

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029936

**中文总结:** 提出字节码级代理合约检测框架 ProxyEx（准确率超 99%），并对以太坊上 203 万余代理合约开展首次系统性实证研究。

**Abstract:** Proxy has been introduced as a design pattern to separate data and code in an application to two different types of smart contracts, namely proxy and logic contracts, respectively. Data is stored in the proxy contracts, while the code to be executed is fetched from the logic contracts. Proxy patterns facilitate the flexibility of smart contract development by enabling upgradeability, extensibility, code reuse, etc. Despite its popularity and importance, there is currently no systematic study to understand the prevalence, use scenarios, and development pitfalls of proxies. In this work, we conduct the first comprehensive study on Ethereum proxies. To collect a comprehensive dataset of proxies, we propose ProxyEx, the first framework designed to detect proxy directly from bytecode. Our evaluation shows that ProxyEx achieves over 99% accuracy. With ProxyEx, we collect a large-scale dataset of 2,031,422 proxies from all contracts in Ethereum and conduct the first systematic empirical study. We first measure the total number of proxies and their transaction traffic, to obtain an overall understanding of the status quo of proxies on Ethereum. Then, we categorize the design pattern and use scenarios of proxies into four types: upgradeability, extensibility, code-sharing, and code-hiding. We further identify three types of common pitfalls in proxies: proxy-logic storage collision, logic-logic storage collision, and uninitialized contracts. We also design three checkers for these common pitfalls in proxies by replaying historical transactions. Our study leads to many interesting findings. For instance, we find that upgradeability is not the only reason that developers adopt the proxy pattern in developing Decentralized Applications (DApps). We also find that many proxies suffer from bugs such as storage collision and uninitialized contracts. Our study sheds light on the proxies landscape, and provides valuable insights to future smart contract research on the development, usage, quality assurance, and bug detection of proxies.

## 2. An Empirical Study on Package-Level Deprecation in Python Ecosystem

**Authors:** Zhiqing Zhong (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Shilin He (Microsoft Research), Haoxuan Wang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), BoXi Yu (The Chinese University of Hong Kong, Shenzhen), Haowen Yang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** Evolution and Maintenance, Human and Social Aspects, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029884

**中文总结:** 混合方法实证研究 Python 生态包级 deprecation 的发布、接收与处理现状、对不活跃包的益处及开发者面临的挑战。

**Abstract:** Open-source software (OSS) plays a crucial role in modern software development. Utilizing OSS code can greatly accelerate software development, reduce redundancy, and enhance reliability. Python, a widely adopted programming language, is particularly renowned for its extensive and diverse third-party package ecosystem. However, a significant number of OSS packages within the Python ecosystem are in poor maintenance, leading to potential risks in terms of functionality and security. Consequently, it is essential to establish a deprecation mechanism that assists package developers and users in effectively managing these packages. To facilitate the establishment of the package-level deprecation mechanism, this paper presents a mixed-method empirical study, including data analysis and surveys. We investigate the current practices of announcing, receiving, and handling package-level deprecation in the Python ecosystem. We also assess the benefits of having deprecation announcements for inactively maintained packages. Furthermore, we investigate the challenges faced by package developers and users and their expectations for future deprecation practices. Our findings reveal valuable insights. For instance, 75.4\% of inactive package developers have no intention of releasing deprecation declarations for various reasons, while 89.5\% of users express a desire to be notified about the deprecation, highlighting a gap between developers and users; In many cases, no alternative solutions are available when deprecation occurs, emphasizing the need to explore practical approaches that enable seamless package handover and require less maintenance effort. We anticipate that our work will enhance the understanding of existing package-level deprecation patterns within the Python OSS realm and facilitate the development of deprecation practices for the Python community in the future.

## 3. An Empirical Study on Reproducible Packaging in Open-Source Ecosystems

**Authors:** Giacomo Benedetti (University of Genoa), Oreofe Solarin (Case Western Reserve University), Courtney Miller (Carnegie Mellon University), Greg Tystahl (NCSU), William Enck (North Carolina State University), Christian Kästner (Carnegie Mellon University), Alexandros Kapravelos (NCSU), Alessio Merlo (CASD - School of Advanced Defense Studies), Luca Verderame (University of Genoa)

**Categories:** Mining Software Repositories

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029905

**中文总结:** 对 npm、Maven、PyPI、Go、RubyGems、Cargo 六大生态各 4000 个包的可复现构建进行实证分析，揭示不同生态间复现率差异显著。

**Abstract:** The integrity of software builds is fundamental to the security of the software supply chain. While Thompson first raised the potential for attacks on build infrastructure in 1984, limited attention has been given to build integrity in the past 40 years, enabling recent attacks on SolarWinds, event-stream, and xz. The best-known defense against build system attacks is creating \emph{reproducible builds}; however, achieving them can be complex for both technical and social reasons and thus is often viewed as impractical to obtain. In this paper, we analyze reproducibility of builds in a novel context: reusable \emph{components} distributed as \emph{packages} in six popular software ecosystems (npm, Maven, PyPI, Go, RubyGems, and Cargo). Our quantitative study on a representative sample of 4000 packages in each ecosystem raises concerns: Rates of reproducible builds vary widely between ecosystems, with some ecosystems having all packages reproducible whereas others have \issues in nearly every package. However, upon deeper investigation, we identified that with relatively straightforward infrastructure configuration and patching of build tools, we can achieve very high rates of reproducible builds in all studied ecosystems. We conclude that if the ecosystems adopt our suggestions, the build process of published packages can be independently confirmed for nearly all packages without individual developer actions, and doing so will prevent significant future software supply chain attacks.

## 4. Answering User Questions about Machine Learning Models through Standardized Model Cards

**Authors:** Tajkia Rahman Toma (University of Alberta), Balreet Grewal (University of Alberta), Cor-Paul Bezemer (University of Alberta)

**Categories:** Software Engineering for AI, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029847

**中文总结:** 分析 Hugging Face 上 11,278 条模型讨论，发现 40.1% 用户问题未获回复，标准化模型卡片可减轻社区答疑负担。

**Abstract:** Reusing pre-trained machine learning models is becoming very popular due to model hubs such as Hugging Face (HF). However, similar to when reusing software, many issues may arise when reusing an ML model. In many cases, users resort to asking questions on discussion forums such as the HF community forum. In this paper, we study how we can reduce the community's workload in answering these questions and increase the likelihood that questions receive a quick answer. We analyze 11,278 discussions from the HF model community that contain user questions about ML models. We focus on the effort spent handling questions, the high-level topics of discussions, and the potential for standardizing responses in model cards based on a model card template. Our findings indicate that there is not much effort involved in responding to user questions, however, 40.1% of the questions remain open without any response. A topic analysis shows that discussions are more centered around technical details on model development and troubleshooting, indicating that more input from model providers is required. We show that 42.5% of the questions could have been answered if the model provider followed a standard model card template for the model card. Based on our analysis, we recommend that model providers add more development-related details on the model's architecture, algorithm, data preprocessing and training code in existing documentation (sub)sections and add new (sub)sections to the template to address common questions about model usage and hardware requirements.

## 5. Automated, Unsupervised, and Auto-parameterized Inference of Data Patterns and Anomaly Detection

**Authors:** Qiaolin Qin (Polytechnique Montréal), Heng Li (Polytechnique Montréal), Ettore Merlo (Polytechnique Montreal), Maxime Lamothe (Polytechnique Montreal)

**Categories:** Software Engineering for AI, Security and Vulnerability, Mining Software Repositories

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029754

**中文总结:** 提出 RIOLU，无需标注与人工参数配置即可从未清洗数据自动推断正则数据模式并检测异常，在多领域数据集上 F1 达 97.2%，优于现有方法。

**Abstract:** With the advent of data-centric and machine learning (ML) systems, data quality is playing an increasingly critical role for ensuring the overall quality of software systems. Alas, data preparation, an essential step towards high data quality, is known to be a highly effort-intensive process. Although prior studies have dealt with one of the most impacting issues, data pattern violations, we observe that these studies usually require data-specific configurations (i.e., parameterized) or a certain set of fully curated data as learning examples (i.e., supervised). Both approaches require domain knowledge and depend on users' deep understanding of their data, and are often effort-intensive. In this paper, we introduce RIOLU: Regex Inferencer autO-parameterized Learning with Uncleaned data. RIOLU is fully automated, is automatically parameterized, and does not need labeled samples. We observe that RIOLU can generate precise patterns from datasets in various domains, with a high F1 score of 97.2%, exceeding the state-of-the-art baseline. In addition, according to our experiment on five datasets with anomalies, RIOLU can automatically estimate a data column's error rate, draw normal patterns, and predict anomalies from unlabeled data with higher performance (up to 800.4% improvement in terms of F1) than the state-of-the-art baseline. Furthermore, RIOLU can even outperform ChatGPT in terms of both accuracy (12.3% higher F1) and efficiency (10% less inference time). With user involvement, a variation (a guided version) of RIOLU can further boost its precision (up to 37.4% improvement in terms of F1). Our evaluation in an industrial setting further demonstrates the practical benefits of RIOLU.

## 6. Exposing the Hidden Layer: Software Repositories in the Service of SEO Manipulation

**Authors:** Mengying Wu (Fudan University), Geng Hong (Fudan University), Wuyuao Mai (Fudan University), Xinyi Wu (Fudan University), Lei Zhang (Fudan University), Yingyuan Pu (QI-ANXIN Technology Research Institute), Huajun Chai (QI-ANXIN Technology Research Institute), Lingyun Ying (Qi An Xin Group Corp.), Haixin Duan (Institute for Network Science and Cyberspace, Tsinghua University; Qi An Xin Group Corp.), Min Yang (Fudan University)

**Categories:** Security and Vulnerability, Mining Software Repositories

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029819

**中文总结:** 揭示软件仓库黑帽 SEO（RepSEO）新型攻击向量，开发检测工具并在 npm、Docker Hub、NuGet 十年数据中发现 380 万余滥用包，分析其供应链 tactics 与牟利模式。

**Abstract:** Distinct from traditional malicious packages, this paper uncovers a novel attack vector named “blackhat Search Engine Optimization through REPositories (RepSEO)”. In this approach, attackers carefully craft packages to manipulate search engine results, exploiting the credibility of software repositories to promote illicit websites. Our research presents a systematic analysis of the underground ecosystem of RepSEO, identifying key players such as account providers, advertisers, and publishers. We developed an effective detection tool, applied to a ten-year large-scale dataset of npm, Docker Hub, and NuGet software repositories. This investigation led to the startling discovery of 3,801,682 abusive packages, highlighting the widespread nature of this attack. Our study also delves into the supply chain tactics of these attacks, revealing strategies like the use of self-hosted email services for account registration, redirection methods to obscure landing pages, and rapid deployment techniques by aggressive attackers. Additionally, we explore the profit motives behind these attacks, identifying two primary types of advertisers: survey-based advertisers and malware distribution advertisers. We reported npm, NuGet, and Docker Hub about the RepSEO packages and the related supply chain vulnerabilities of Google, and received their acknowledgments. Software repositories have started removing the abusive packages as of this paper’s submission. We also open-source our code and data to facilitate future research.

## 7. SOEN-101: Code Generation by Emulating Software Process Models Using Large Language Model Agents

**Authors:** Feng Lin (Concordia University), Dong Jae Kim (DePaul University), Tse-Hsun (Peter) Chen (Concordia University)

**Categories:** AI for Software Engineering, Software Engineering for AI, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029771

**中文总结:** 提出 FlowGen 多智能体框架，模拟瀑布、TDD 与 Scrum 流程生成代码；FlowGen_Scrum 在 HumanEval 等基准 Pass@1 达 75.2。

**Abstract:** Software process models are essential to facilitate collaboration and communication among software teams to solve complex development tasks. Inspired by these software engineering practices, we present FlowGen – a code generation framework that emulates software process models based on multiple Large Language Model (LLM) agents. We emulate three process models, FlowGen$_{Waterfall}$, FlowGen$_{TDD}$, and FlowGen$_{Scrum}$, by assigning LLM agents to embody roles (i.e., requirement engineer, architect, developer, tester, and scrum master) that correspond to everyday development activities and organize their communication patterns. The agents work collaboratively using chain-of-thought and prompt composition with continuous self-refinement to improve the code quality. We use GPT-3.5 as our underlying LLM and several baselines (RawGPT, CodeT, Reflexion) to evaluate code generation on four benchmarks: HumanEval, HumanEval-ET, MBPP, and MBPP-ET. Our findings show that FlowGen$_{Scrum}$ excels compared to other process models, achieving a Pass@1 of 75.2, 65.5, 82.5, and 56.7 in HumanEval, HumanEval-ET, MBPP, and MBPP-ET, respectively (an average of 15% improvement over RawGPT). Compared with other state-of-the-art techniques, FlowGen$_{Scrum}$ achieves a higher Pass@1 in MBPP compared to CodeT, with both outperforming Reflexion. Notably, integrating CodeT into FlowGen$_{Scrum}$ resulted in statistically significant improvements, achieving the highest Pass@1 scores. Our analysis also reveals that the development activities impacted code smell and exception handling differently, with design and code review adding more exception handling and reducing code smells. Finally, FlowGen models maintain stable Pass@1 scores across GPT-3.5 versions and temperature values, highlighting the effectiveness of software process models in enhancing the quality and stability of LLM-generated code.

## 8. The Product Beyond the Model -- An Empirical Study of Repositories of Open-Source ML Products

**Authors:** Nadia Nahar (Carnegie Mellon University), Haoran Zhang (Carnegie Mellon University), Grace Lewis (Carnegie Mellon Software Engineering Institute), Shurui Zhou (University of Toronto), Christian Kästner (Carnegie Mellon University)

**Categories:** Software Engineering for AI, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029840

**中文总结:** 从 GitHub 50 万+ ML 相关项目中识别 262 个开源 ML 产品并深入分析 30 个，报告 21 项发现（如数据科学家参与有限、ML/非 ML 模块化低、测试与监控实践不足）。

**Abstract:** Machine learning (ML) components are increasingly incorporated into software products for end-users, but developers face challenges in transitioning from ML prototypes to products. Academics have limited access to the source of commercial ML products, challenging research progress. In this study, first, we contribute a novel process to identify 262 open-source ML products among more than half a million ML-related projects on GitHub. Then, we qualitatively and quantitatively analyze 30 open-source ML products to answer six broad research questions about development practices and system architecture. We find that the majority of the ML products in our sample represent startup-style development reported in past interview studies. We report 21 findings, including limited involvement of data scientists in many ML products, unusually low modularity between ML and non-ML code, diverse architectural choices on incorporating models into products, and limited prevalence of industry best practices such as model testing, pipeline automation, and monitoring. Additionally, we discuss 7 implications of this study on research, development, and education, including the need for tools to assist teams without data scientists, education opportunities, and open-source-specific research for privacy-preserving telemetry.

## 9. Towards Understanding the Characteristics of Code Generation Errors Made by Large Language Models

**Authors:** Zhijie Wang (University of Alberta), Zijie Zhou (University of Illinois Urbana-Champaign), Da Song (University of Alberta), Yuheng Huang (University of Alberta, Canada), Shengmai Chen (Purdue University), Lei Ma (The University of Tokyo & University of Alberta), Tianyi Zhang (Purdue University)

**Categories:** AI for Software Engineering, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029951

**中文总结:** 在 HumanEval 上对六种 LLM 的代码生成错误做系统分析，建立涵盖语义与语法维度的错误分类体系，揭示错误多为跨行、多位置且与任务复杂度相关。

**Abstract:** Large Language Models (LLMs) have demonstrated unprecedented capabilities in code generation. However, there remains a limited understanding of code generation errors that LLMs can produce. To bridge the gap, we conducted an in-depth analysis of code generation errors across six representative LLMs on the HumanEval dataset. Specifically, we first employed open coding and thematic analysis to distill a comprehensive taxonomy of code generation errors. We analyzed two dimensions of error characteristics---semantic characteristics and syntactic characteristics. Our analysis revealed that LLMs often made non-trivial, multi-line code generation errors in various locations and with various root causes. We further analyzed the correlation between these errors and task complexity as well as test pass rate. Our findings highlight several challenges in locating and fixing code generation errors made by LLMs. In the end, we discussed several future directions to address these challenges.

## 10. Understanding and Detecting Peer Dependency Resolving Loop in npm Ecosystem

**Authors:** Xingyu Wang (Zhejiang University), MingSen Wang (Zhejiang University), Wenbo Shen (Zhejiang University), Rui Chang (Zhejiang University)

**Categories:** Evolution and Maintenance, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029857

**中文总结:** 首次系统研究 npm 生态中 peer 依赖解析陷入无限循环的 PeerSpin 问题，提出基于目录树节点替换冲突的检测方法 NRCPD，可准确高效识别该缺陷。

**Abstract:** As the default package manager for Node.js, npm has become one of the largest package management systems in the world. To facilitate dependency management for developers, npm supports a special type of dependency, Peer Dependency, whose installation and usage differ from regular dependencies. However, conflicts between peer dependencies can trap the npm client into infinite loops, leading to resource exhaustion and system crashes. We name this problem PeerSpin. Although PeerSpin poses a severe risk to ecosystems, it was overlooked by previous studies, and its impacts have not been explored. To bridge this gap, this paper conducts the first in-depth study to understand and detect PeerSpin in the npm ecosystem. First, by systematically analyzing the npm dependency resolution, we identify the root cause of PeerSpin and characterize two peer dependency patterns to guide detection. Second, we propose a novel technique called Node-Replacement-Conflict based PeerSpin Detection, which leverages the state of the directory tree during dependency resolution to achieve accurate and efficient PeerSpin detection. Based on this technique, we developed a tool called PeerChecker to detect PeerSpin. Finally, we apply PeerChecker to the entire NPM ecosystem and find that 5,662 packages, totaling 72,968 versions, suffer from PeerSpin. Up until now, we confirmed 28 real PeerSpin problems by reporting them to the package maintainer. We also open source all PeerSpin analysis implementations, tools, and data sets to the public to help the community detect PeerSpin issues and enhance the reliability of the npm ecosystem.

## 11. Understanding Architectural Complexity, Maintenance Burden, and Developer Sentiment---a Large-Scale Study

**Authors:** Yuanfang Cai (Drexel University), Lanting He (Google), Yony Kochinski (Google), Jun Qian (Google), Ciera Jaspan (Google), Nan Zhang (Google), Antonio Bianco (Google)

**Categories:** Evolution and Maintenance, Human and Social Aspects, Mining Software Repositories, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029733

**中文总结:** 对某公司 1252 个 C++/Java 项目开展大规模研究，量化架构复杂度、维护活动与 7200 份开发者调查情感之间的统计关联。

**Abstract:** Intuitively, the more complex a software system is, the harder it is to maintain. Statistically, it is not clear which complexity metrics correlate with maintenance effort; in fact, it is not even clear how to objectively measure maintenance burden, so that developers' sentiment and intuition can be supported by numbers. Without effective complexity and maintenance metrics, it remains difficult to objectively monitor maintenance, control complexity, or justify refactoring. In this paper, we report a large-scale study of 1252 projects written in C++ and Java from Company_X. We collected three categories of metrics: (1) architectural complexity, measured using propagation cost (PC), decoupling level (DL), and structural anti-patterns; (2) maintenance activity, measured using the number of changes, lines of code (LOC) written, and active coding time (ACT) spent on feature-addition vs. bug-fixing, and (3) developer sentiment on complexity and productivity, collected from 7200 survey responses. We statistically analyzed the correlations among these metrics and obtained significant evidence of the following findings: 1) the more complex the architecture is (higher propagation cost, more instances of anti-patterns), the more LOC is spent on bug-fixing, rather than adding new features; 2) developers who commit more changes for features, spend more lines of code on features, or spend more time on features also feel that they are less hindered by technical debt and complexity. To the best of our knowledge, this is the first large-scale empirical study establishing the statistical correlation among architectural complexity, maintenance activity, and developer sentiment. The implication is that, instead of solely relying upon developer sentiment and intuition to detect degraded structure or increased burden to evolve, it is possible to objectively and continuously measure and monitor architectural complexity and maintenance difficulty, increasing feature delivery efficiency by reducing architectural complexity and anti-patterns.

## 12. When Quantum Meets Classical: Characterizing Hybrid Quantum-Classical Issues Discussed in Developer Forums

**Authors:** Jake Zappin (William and Mary), Trevor Stalnaker (William & Mary), Oscar Chaparro (William & Mary), Denys Poshyvanyk (William & Mary)

**Categories:** Program Analysis and Verification, Human and Social Aspects, Mining Software Repositories

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029802

**中文总结:** 对 531 个开发者论坛问题进行首个混合量子-经典计算实证研究，构建涵盖软件故障、硬件失败、库错误与开发者失误的分类体系。

**Abstract:** Recent advances in quantum computing have sparked excitement that this new computing paradigm could solve previously intractable problems. However, due to the faulty nature of current quantum hardware and quantum-intrinsic noise, the full potential of quantum computing is still years away. Hybrid quantum-classical computing has emerged as a possible compromise that achieves the best of both worlds. In this paper, we look at hybrid quantum-classical computing from a software engineering perspective and present the first empirical study focused on characterizing and evaluating recurrent issues faced by developers of hybrid quantum-classical applications. The study comprised a thorough analysis of 531 real-world issues faced by developers -- including software faults, hardware failures, quantum library errors, and developer mistakes -- documented in discussion threads from forums dedicated to quantum computing. By qualitatively analyzing such forum threads, we derive a comprehensive taxonomy of recurring issues in hybrid quantum-classical applications that can be used by both application and platform developers to improve the reliability of hybrid applications. The study considered how these recurring issues manifest and their causes, determining that hybrid applications are crash-dominant (74% of studied issues) and that errors were predominantly introduced by application developers (70% of issues). We conclude by identifying recurring obstacles for developers of hybrid applications and actionable recommendations to overcome them.
