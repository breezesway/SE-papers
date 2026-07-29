# ICSE 2025 Research Track — Testing and Quality

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 77 papers

## 1. A Differential Testing Framework to Identify Critical AV Failures Leveraging Arbitrary Inputs

**Authors:** Trey Woodlief (University of Virginia), Carl Hildebrandt (University of Virginia), Sebastian Elbaum (University of Virginia)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029848

**中文总结:** 提出 DiffTest4AV 差分测试框架，利用开放数据集探索自动驾驶长尾输入并在缺乏显式预言机时识别关键失效。

**Abstract:** The proliferation of autonomous vehicles (AVs) has made their failures increasingly evident. Testing efforts aimed at identifying the inputs leading to those failures are challenged by the input's long-tail distribution, whose area under the curve is dominated by rare scenarios. We hypothesize that leveraging emerging open-access datasets can accelerate the exploration of long-tail inputs. Having access to diverse inputs, however, is not sufficient to expose failures; an effective test also requires an oracle to distinguish between correct and incorrect behaviors. Current datasets lack such oracles and developing them is notoriously difficult. In response, we propose DiffTest4AV, a differential testing framework designed to address the unique challenges of testing AV systems: 1) for any given input, many outputs may be considered acceptable, 2) the long-tail contains an insurmountable number of inputs to explore, and 3) the AV's continuous execution loop requires for failures to persist in order to affect the system. DiffTest4AV integrates statistical analysis to identify meaningful behavioral variations, judges their importance in terms of the severity of these differences, and incorporates sequential analysis to detect persistent errors indicative of potential system-level failures. Our study on 5 versions of the commercially-available, road-deployed comma.ai OpenPilot system, using 3 available image datasets, demonstrates the capabilities of the framework to detect high-severity, high-confidence, long-running test failures.

## 2. A Little Goes a Long Way: Tuning Configuration Selection for Continuous Kernel Fuzzing

**Authors:** Sanan Hasanov (University of Central Florida), Stefan Nagy (University of Utah), Paul Gazzillo (University of Central Florida)

**Categories:** Testing and Quality, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029826

**中文总结:** 针对持续内核模糊测试中预定义配置覆盖不足、难以纳入新补丁的问题，提炼连续 fuzz 六项需求并提出配置选择调优方法以提升覆盖。

**Abstract:** The Linux kernel is actively-developed and widely-used. It supports billions of devices of all classes, from high-performance computing to the Internet-of-Things, in part because of its sophisticated configuration system, which automatically tailors the source code according to thousands of user-provided configuration options. Fuzzing has been highly successful at finding kernel bugs, being among the top bug reporters. Since the kernel receives 100s of patches per day, fuzzers run continuously, stopping regularly to rebuild the kernel with the latest changes before restarting fuzzing. But kernel fuzzers currently use predefined configuration settings that, as we show, exclude the majority of new patches from the kernel binary, nullifying the benefits of continuous fuzzing. Unfortunately, state-of-the-art configuration testing techniques are generally ill-suited to the needs of continuous fuzzing, excluding necessary options or requiring too many configuration files to be tractible. We distill down the needs of continuous testing into six properties with the most impact, systematically analyze the space of configuration selection strategies, and provide actionable recommendations. Through our analysis, we discover that continuous fuzzers can improve configuration variety without sacrificing performance. We empirically evaluate our discovery by modifying the configuration selection strategy for syzkaller, the most popular Linux kernel fuzzer, which subsequently found more than twice as many new bugs (35 vs. 13) than with the original configuration file and 12x more (24 vs. 2) when considering only unique bugs---with one security vulnerability being assigned a CVE.

## 3. A Multi-Agent Approach for REST API Testing with Semantic Graphs and LLM-Driven Inputs

**Authors:** Myeongsoo Kim (Georgia Institute of Technology), Tyler Stennett (Georgia Institute of Technology), Saurabh Sinha (IBM Research), Alessandro Orso (Georgia Institute of Technology)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029879

**中文总结:** 提出 AutoRestTest 黑盒 REST API 测试框架，以多智能体强化学习、语义属性依赖图与大语言模型协同优化接口探索与故障检测。

**Abstract:** As modern web services increasingly rely on REST APIs, their thorough testing has become crucial. Furthermore, the advent of REST API specifications such as OpenAPI ones has led to the emergence of many black-box REST API testing tools. However, these tools often focus on individual test elements in isolation (e.g., APIs, parameters, values), resulting in lower coverage and less effectiveness in detecting faults (i.e., 500 response codes). To address these limitations, we present AutoRestTest, the first black-box framework to adopt a dependency-embedded multi-agent approach for REST API testing, integrating Multi-Agent Reinforcement Learning (MARL) with a Semantic Property Dependency Graph (SPDG) and Large Language Models (LLMs). Our approach treats REST API testing as a separable problem, where four agents---API, dependency, parameter, and value---collaborate to optimize API exploration. LLMs handle domain-specific value restrictions, the SPDG model simplifies the search space for dependencies using a similarity score between API operations, and MARL dynamically optimizes the agents' behavior. Evaluated on 12 real-world REST services, AutoRestTest outperforms the four leading black-box REST API testing tools, including those assisted by RESTGPT (which augments realistic test inputs using LLMs), in terms of code coverage, operation coverage, and fault detection. Notably, AutoRestTest is the only tool able to identify an internal server error in Spotify. Our ablation study underscores the significant contributions of the agent learning, SPDG, and LLM components.

## 4. A Tale of Two DL Cities: When Library Tests Meet Compiler

**Authors:** Qingchao Shen (Tianjin University), Yongqiang Tian, Haoyang Ma (Hong Kong University of Science and Technology), Junjie Chen (Tianjin University), Lili Huang (College of Intelligence and Computing, Tianjin University), Ruifeng Fu (Tianjin University), Shing-Chi Cheung (Hong Kong University of Science and Technology), Zan Wang (Tianjin University)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029788

**中文总结:** 提出 OPERA，将深度学习库测试迁移到编译器模型加载阶段并做测试优先级排序；首次实证研究该知识迁移在 TVM、TensorRT 等前端上的有效性与效率。

**Abstract:** Deep Learning (DL) compilers typically load a DL model and optimize it with intermediate representation. Existing DL compiler testing techniques mainly focus on model optimization stages, but rarely explore bug detection at the model loading stage. Effectively testing the model loading stage requires covering diverse usages of each DL operator from various DL libraries, which shares a common objective with DL library testing, indicating that the embedded knowledge in DL library tests could potentially be beneficial for testing the model loading stage of DL compilers. Thus, we conducted the first empirical study to investigate the effectiveness and efficiency of migrating the knowledge embedded in DL library tests to test the model loading stage. To support the conduct of this study, we develop a technique, called OPERA, consisting of test migration (regarding effectiveness investigation) and test prioritization (regarding efficiency investigation). We considered three sources of tests in DL libraries for migration and used eight frontends from three DL compilers (e.g., TVM, TensorRT, and OpenVINO) for evaluation. The migrated tests with the aid of OPERA detected 170 previously unknown bugs in total, 90 of which have been confirmed/fixed by developers, demonstrating the effectiveness of such the migration-based idea. The test prioritization strategy in OPERA improves testing efficiency with migrated tests by 11.9%~47.4% on average compared to general test prioritization strategies. Finally, we obtained 7 major findings and provided a set of guidelines for future work from this study.

## 5. Accessibility Issues in Ad-Driven Web Applications

**Authors:** Abdul Haddi Amjad (Virginia Tech), Muhammad Danish (Virginia Tech), Bless Jah (Virginia Tech), Muhammad Ali Gulzar (Virginia Tech)

**Categories:** Testing and Quality, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029732

**中文总结:** 大规模检测 43 万网页元素，发现 67% 网站因第三方广告引入更多无障碍违规，常见违反 WCAG 焦点可见与输入响应规则。

**Abstract:** Website accessibility is essential for inclusiveness and regulatory compliance. Although third-party advertisements (ads) are a vital revenue source for free web services, they introduce significant accessibility challenges. Leasing a website’s space to ad-serving technologies like DoubleClick results in developers losing control over ad content accessibility. Even on highly accessible websites, third-party ads can undermine adherence to Web Content Accessibility Guidelines (WCAG). We conduct the first-of-its-kind large-scale investigation of 430K website elements, including nearly 100K ad elements, to understand the accessibility of ads on websites. We seek to understand the prevalence of inaccessible ads and their overall impact on the accessibility of websites. Our findings show that 67% of websites experience increased accessibility violations due to ads, with common violations including Focus Visible (WCAG 2.4.7) and On Input (WCAG 3.2.2). Popular ad-serving technologies like Taboola, DoubleClick, and RevContent often serve ads that fail to comply with WCAG standards. Even when ads are WCAG compliant, 27% of them have alternative text in ad images that misrepresents information, potentially deceiving users. Manual inspection of a sample of these misleading ads revealed that user-identifiable data is collected on 94% of websites through interactions, such as hovering or pressing enter. Since users with disabilities often rely on tools like screen readers that require hover events to access website content, they have no choice but to compromise their privacy in order to navigate website ads. Based on our findings, we further dissect the root cause of these violations and provide design guidelines to both website developers and ad-serving technologies to achieve WCAG-compliant ad integration.

## 6. Analyzing the Feasibility of Adopting Google's Nonce-Based CSP Solutions on Websites

**Authors:** Mengxia Ren (Colorado School of Mines), Anhao Xiang (Colorado School of Mines), Chuan Yue (Colorado School of Mines)

**Categories:** Testing and Quality, Security and Vulnerability

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029938

**中文总结:** 评估 Google 四类基于 nonce 的 CSP 方案在 Tranco 前 1 万网站上的可落地性，通过爬取与分析揭示 nonce-CSP 广泛推广的可行路径与主要障碍。

**Abstract:** Content Security Policy (CSP) is a leading security mechanism for mitigating content injection attacks such as Cross-Site Scripting (XSS). Nevertheless, despite efforts from academia and industry, CSP policies (in short, CSPs) are not widely deployed on websites, and deployed CSPs often have security issues or errors. Such low and insecure CSP deployment problems are mainly due to the complexity of the CSP mechanism. Google recently proposed four nonce-based CSP solutions which are simpler and more secure compared to traditional whitelisting-based CSP solutions. Google successfully deployed their nonce- based CSP solutions on over 160 services, covering 62% of all outgoing Google traffic. These nonce-based CSP solutions use simple CSPs but provide fine-grained control of web resources; therefore, if widely adopted on many other websites, they can be very helpful on addressing the low and insecure CSP deployment problems. In this paper, we evaluate the feasibility of adopting Google's nonce-based CSP solutions on the Tranco top 10K websites. We construct a crawling tool to automatically visit websites, simulate user interactions, and insert four CSPs to collect the CSP violations triggered under them. We investigate the adoptability of the nonce-based CSP solutions, adoption issues, and the stability of adopting them on websites by analyzing the CSP violations triggered under the inserted CSPs. We found that most websites can adopt the nonce-based CSP solutions on all their webpages visited in our study. For websites that cannot, usually the adoption is hard on around 40% of their webpages. Overall, our results are very encouraging and can be helpful in promoting the proper deployment of CSPs on many websites.

## 7. Automated Accessibility Analysis of Dynamic Content Changes on Mobile Apps

**Authors:** Forough Mehralian (University of California at Irvine), Ziyao He (University of California, Irvine), Sam Malek (University of California at Irvine)

**Categories:** Testing and Quality, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029844

**中文总结:** 针对 Android 应用动态内容变化对读屏用户的无障碍障碍，先做形成性用户研究，再提出自动化检测框架 TIMESTUMP。

**Abstract:** With mobile apps playing an increasingly vital role in our daily lives, the importance of ensuring their accessibility for users with disabilities is also growing. Despite this, app developers often overlook the accessibility challenges encountered by users of assistive technologies, such as screen readers. Screen reader users typically navigate content sequentially, focusing on one element at a time, unaware of changes occurring elsewhere in the app. While dynamic changes to content displayed on an app’s user interface may be apparent to sighted users, they pose significant accessibility obstacles for screen reader users. Existing accessibility testing tools are unable to identify challenges faced by blind users resulting from dynamic content changes. In this work, we first conduct a formative user study on dynamic changes in Android apps and their accessibility barriers for screen reader users. We then present TIMESTUMP, an automated framework that leverages our findings in the formative study to detect accessibility issues regarding dynamic changes. Finally, we empirically evaluate TIMESTUMP on real-world apps to assess its effectiveness and efficiency in detecting such accessibility issues.

## 8. Automated Test Generation For Smart Contracts via On-Chain Test Case Augmentation and Migration

**Authors:** Jiashuo Zhang (Peking University, China), Jiachi Chen (Sun Yat-sen University), John Grundy (Monash University), Jianbo Gao (Peking University), Yanlin Wang (Sun Yat-sen University), Ting Chen (University of Electronic Science and Technology of China), Zhi Guan (Peking University), Zhong Chen

**Categories:** Testing and Quality, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029866

**中文总结:** 提出 SolMigrator，从链上合约真实使用场景提取测试用例并迁移至功能相似的新合约，自动生成表达力强、与功能相关的智能合约测试，弥补现有方法偏重漏洞检测的不足。

**Abstract:** Pre-deployment testing has become essential to ensure the functional correctness of smart contracts. However, since smart contracts are stateful programs integrating many different functionalities, manually writing test cases to cover all potential usages requires significant effort from developers, leading to insufficient testing and increasing risks in practice. Although several testing techniques for smart contracts have been proposed, they primarily focus on detecting common low-level vulnerabilities such as re-entrancy, rather than generating expressive and function-relevant test cases that can reduce manual testing efforts. To bridge the gap, we propose SolMigrator, an automated technique designed to generate expressive and representative test cases for smart contracts. To our knowledge, SolMigrator is the first migration-based test generation technique for smart contracts, which extracts test cases from real-world usages of on-chain contracts and migrates them to test newly developed smart contracts with similar functionalities. Given a target smart contract to be tested and an on-chain similar source smart contract, SolMigrator first transforms the on-chain usage of the source contract into off-chain executable test cases based on on-chain transaction replay and dependency analysis. It then employs fine-grained static analysis to migrate the augmented test cases from the source to the target smart contract. We built a prototype of SolMigrator and have evaluated it on real-world smart contracts within the two most popular categories, ERC20 and ERC721. Our evaluation results demonstrate that SolMigrator effectively extracts test cases from existing on-chain smart contracts and accurately migrates them across different smart contracts, achieving an average precision of 96.3% and accuracy of 93.6%. Furthermore, the results indicate that these migrated test cases effectively cover common key functionalities of the target smart contracts. This provides promising evidence that real-world usages of existing smart contracts can be transformed into effective test cases for other newly developed smart contracts.

## 9. Automating a Complete Software Test Process Using LLMs: An Automotive Case Study

**Authors:** Shuai Wang, Yinan Yu (Chalmers University of Technology), Robert Feldt (Chalmers | University of Gothenburg), Dhasarathy Parthasarathy (Volvo Group)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029843

**中文总结:** 面向车载 API 测试，将流程拆分为子任务并交由 LLM 分步完成，在 100 余个 API 上验证可稳定自动化整车软件测试链路。

**Abstract:** Vehicle API testing verifies whether the interactions between a vehicle's internal systems and external applications meet expectations, ensuring that users can access and control various vehicle functions and data. However, this task is inherently complex, requiring the alignment and coordination of API systems, communication protocols, and even vehicle simulation systems to develop valid test cases. In practical industrial scenarios, inconsistencies, ambiguities, and interdependencies across various documents and system specifications pose significant challenges. This paper presents a system designed for the automated testing of in-vehicle APIs. By clearly defining and segmenting the testing process, we enable Large Language Models (LLMs) to focus on specific tasks, ensuring a stable and controlled testing workflow. Experiments conducted on over 100 APIs demonstrate that our system effectively automates vehicle API testing. The results also confirm that LLMs can efficiently handle mundane tasks requiring human judgment, making them suitable for complete automation in similar industrial contexts.

## 10. Boosting Code-line-level Defect Prediction with Spectrum Information and Causality Analysis

**Authors:** Shiyu Sun, Yanhui Li (Nanjing University), Lin Chen (Nanjing University), Yuming Zhou (Nanjing University), Jianhua Zhao (Nanjing University, China)

**Categories:** Testing and Quality, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029896

**中文总结:** 提出 SOUND，结合谱信息与因果分析利用历史行级缺陷标签量化 token 贡献，提升代码行级缺陷预测效果。

**Abstract:** Code-line-level defect prediction (CLDP) is an effective technique to incorporate comprehensive measures for buggy line identification to optimize efforts in Software Quality Assurance activities. Most CLDP methods either consider the textual information of the code or rely merely on file-level label information, which have not fully leveraged the essential information in the CLDP context, with historical \textit{code-line-level labels} being incredibly overlooked in their application. Due to the vast number of code lines and the sparsity of the tokens they contain, leveraging historical code-line-level label information remains a significant challenge. To address this issue, we propose a novel CLDP method, \textbf{S}pectrum inf\textbf{O}rmation and ca\textbf{U}sality a\textbf{N}alysis based co\textbf{D}e-line-level defect prediction ($\mathsf{SOUND}$). $\mathsf{SOUND}$ incorporates two key ideas: (a) it introduces a spectrum information perspective, utilizing labels from historical defective lines to quantify the contribution of tokens to line-level defects, and (b) it applies causal analysis to obtain a more systematic and comprehensive understanding of the causal relationships between tokens and defects. After conducting a comprehensive study involving 142 releases across 19 software projects, the experimental results show that our method significantly outperforms existing state-of-the-art (SOTA) CLDP baseline methods in terms of its ability to rank defective lines under three indicators, IFA, Recall@Top20\%LOC, and Effort@Top20\%Recall. Notably, in terms of IFA, our method achieves a score of 0 in most cases, indicating that the first line in the ranking list generated by our method is actually defective, significantly enhancing its practicality.

## 11. Chord: Towards a Unified Detection of Blockchain Transaction Parallelism Bugs

**Authors:** Yuanhang Zhou (Tsinghua University), Zhen Yan (Tsinghua University), Yuanliang Chen (Tsinghua University), Fuchen Ma (Tsinghua University), Ting Chen (University of Electronic Science and Technology of China), Yu Jiang (Tsinghua University)

**Categories:** Testing and Quality, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029924

**中文总结:** 分析四种商业区块链交易并行 bug，提出 Chord 统一冲突交易模型与动态提交策略，以检测资产损失、双花等并行处理缺陷。

**Abstract:** Blockchain systems have implemented various transaction parallelism mechanisms to improve the system throughput and reduce the latency. However, they inevitably introduce bugs. Such bugs can result in severe consequences such as asset loss, double spending, consensus failure, and DDoS. Unfortunately, they have been little analyzed about their symptoms and root causes, leading to a lack of effective detection methods. In this work, we conduct a thorough analysis of historical transaction parallelism bugs in four commercial blockchains. Results show that most of them arise from mishandling conflicting transactions and manifest without obvious phenomena. However, given the heterogeneity of blockchains, it is challenging to trigger conflict handling in a unified way. Effectively identifying these bugs is also hard. Inspired by the findings, we propose Chord, aiming at detecting blockchain transaction parallelism bugs. Chord proposes a unified conflict transaction model to generate various conflict transactions. Chord also dynamically adjust the transaction submission and inserts proactive reverts during transaction execution to conduct thorough testing. Besides, Chord incorporates a local-remote differential oracle and a TPS oracle to capture the bugs. Our evaluation shows that Chord successfully detects 54 transaction parallelism bugs. Besides, Chord outperforms the existing methods by decreasing the TPS by 49.7% and increasing the latency by 388.0%, showing its effectiveness in triggering various conflict scenarios and exposing the bugs.

## 12. ClozeMaster: Fuzzing Rust Compiler by Harnessing LLMs for Infilling Masked Real Programs

**Authors:** Hongyan Gao (State Key Laboratory for Novel Software Technology, Nanjing University), Yibiao Yang (Nanjing University), Maolin Sun (Nanjing University), Jiangchang Wu (State Key Laboratory for Novel Software Technology, Nanjing University), Yuming Zhou (Nanjing University), Baowen Xu (State Key Laboratory for Novel Software Technology, Nanjing University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029729

**中文总结:** 提出 ClozeMaster，基于 clozeMask 策略从历史 issue 提取真实 Rust 程序并掩码关键片段，借助 LLM 填空生成有效测试用例以模糊测试 Rust 编译器，克服直接生成 Rust 程序大量无效的问题。

**Abstract:** Ensuring the reliability of the Rust compiler is of paramount importance, as the Rust language is increasingly being adopted for developing critical systems due to its emphasis on memory and thread safety. However, due to Rust’s complex syntax and strict requirements, generating valid test programs for the Rust compiler poses significant challenges. Currently, with the growing popularity of large language models (LLMs), much research in software testing has explored the use of LLMs to generate test cases. Despite this, directly using LLMs to generate Rust programs often results in a large number of invalid test cases. Existing studies have indicated that test cases triggering historical compiler bugs can assist in software testing. Our investigation into Rust compiler bug issues further supports this observation. Inspired by existing work and our empirical research, we introduce a bracket-based masking and filling strategy called clozeMask. The clozeMask strategy involves extracting test code from historical issue reports, identifying and masking code snippets with specific structures, and utilizing an LLM to fill in the masked portions for synthesizing new test programs. This approach harnesses the generative capabilities of LLMs while retaining the ability to trigger Rust compiler bugs. Ultimately, it enables comprehensive testing of the compiler’s behavior, particularly in exploring corner cases. We implemented our approach as a prototype CLOZEMASTER. CLOZEMASTER has identified 27 confirmed bugs for rustc and mrustc, of which 10 have been fixed by developers. Furthermore, our experimental results indicate that CLOZEMASTER outperforms existing generative fuzzers in terms of code coverage and effectiveness.

## 13. Coni: Detecting Database Connector Bugs via State-Aware Test Case Generation

**Authors:** Wenqian Deng (Tsinghua University), Zhiyong Wu (Tsinghua University, China), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Mingzhe Wang (Tsinghua University), Yu Jiang (Tsinghua University)

**Categories:** Testing and Quality, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029870

**中文总结:** 提出 CONI，面向数据库连接器做状态感知测试生成，并通过与参考连接器对比结果找逻辑缺陷；在 5 个主流 JDBC 驱动上发现 44 个未知缺陷（34 个已确认）。

**Abstract:** Database connectors are widely used in many applications to facilitate flexible and convenient database interactions. Potential vulnerabilities in database connectors can lead to various abnormal behaviors within applications, such as returning incorrect results or experiencing unexpected connection interruption. However, existing fuzzing works cannot be directly applied to testing database connectors as they mainly focus on SQL generation and use a small subset of database connector interfaces to execute SQLs. Due to a lack of domain knowledge, automated test case generation also struggles to generate complex test cases that explore connectors' deep logic. The main challenge in testing database connectors is to generate semantically correct test cases that can trigger a wide range of connector state transitions. To address that, we propose CONI, a framework designed for detecting logic bugs of database connectors with state-aware test case generation. First, we define the database connector state model by analyzing the corresponding specification. Building upon this model, CONI generates interface call sequences within test cases to encompass more connector state transitions. After that, CONI generates suitable parameter values based on the parameter information and contextual information collected during runtime. Then the test cases are executed on a target and a reference database connector. Inconsistent results indicate potential logic bugs. We evaluate CONI on 5 widely-used JDBC database connectors, namely MySQL Connector/J, MariaDB Connector/J, AWS JDBC Driver for MySQL, PGJDBC NG, and PostgreSQL JDBC Driver. In total, CONI successfully detected 44 previously unknown bugs, of which 34 have been confirmed.

## 14. Critical Variable State-Aware Directed Greybox Fuzzing

**Authors:** Xu Chen (Institute of Information Engineering at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Ningning Cui (Institute of Information Engineering at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Zhe Pan (Institute of Information Engineering at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Liwei Chen (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Gang Shi (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Dan Meng (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029824

**中文总结:** 提出 CSFuzz，提取目标站点关键变量并自适应划分值域以监控程序状态，改进定向灰盒模糊测试对复杂漏洞的触发能力。

**Abstract:** Directed fuzzing is an effective software testing method that guides the fuzzing campaign towards user-defined target sites of interest, enabling the discovery of vulnerabilities relevant to those sites. However, even though the generated test cases cover the code near the target sites, complex vulnerabilities remain untriggered. By focusing only on test cases that cover new edges, the program states related to the targets are overlooked, resulting in insufficient testing of the targets and failure to capture complex vulnerabilities. In this paper, we propose a novel directed fuzzing solution named CSFuzz, which considers program states associated with the targets. First, CSFuzz extracts critical variables related to the target sites from the program using static analysis. Then, CSFuzz monitors the runtime values of these critical variables and infers the program states associated with the targets by adaptively partitioning the range of variable values. This allows CSFuzz to store interesting seeds in the state corpus that trigger new states near the target sites. Lastly, CSFuzz employs dynamic scheduling techniques to guide the fuzzing campaign in selecting different corpora and prioritizing seeds. This ensures more adequate testing of the target sites. We have implemented a prototype of CSFuzz and evaluated it on 2 benchmarks and widely fuzzed real-world software. Evaluation results show that CSFuzz outperforms state-of-the-art fuzzers in terms of vulnerability detection capability, achieving a maximum speedup of 219%. Moreover, CSFuzz has discovered 4 new bugs, including 2 CVE IDs assigned.

## 15. Definition and Detection of Centralization Defects in Smart Contracts

**Authors:** Zewei Lin (Sun Yat-sen University), Jiachi Chen (Sun Yat-sen University), Jiajing Wu (Sun Yat-sen University), Weizhe Zhang (Harbin Institute of Technology), Zibin Zheng (Sun Yat-sen University)

**Categories:** Testing and Quality, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029945

**中文总结:** 定义六种智能合约中心化缺陷并提出检测工具 CDRipper，基于 597 条 Stack Exchange 帖子与 117 份审计报告归纳缺陷模式。

**Abstract:** In recent years, security incidents stemming from centralization defects in smart contracts have led to substantial financial losses. A centralization defect refers to any error, flaw, or fault in a smart contract’s design or development stage that introduces a single point of failure. Such defects allow a specific account or user to disrupt the normal operations of smart contracts, potentially causing malfunctions or even complete project shutdowns. Despite the significance of this issue, most current smart contract analyses overlook centralization defects, focusing primarily on other types of defects. To address this gap, our paper introduces six types of centralization defects in smart contracts by manually analyzing 597 Stack Exchange posts and 117 audit reports. For each defect, we provide a detailed description and code examples to illustrate its characteristics and potential impacts. Additionally, we introduce a tool named CDRipper (Centralization Defects Ripper) designed to identify the defined centralization defects. Specifically, CDRipper constructs a permission dependency graph (PDG) and extracts the permission dependencies of functions from the source code of smart contracts. It then detects the sensitive operations in functions and identifies centralization defects based on predefined patterns. We conduct a large-scale experiment using CDRipper on 244,424 real-world smart contracts and evaluate the results based on a manually labeled dataset. Our findings reveal that 82,446 contracts contain at least one of the six centralization defects, with our tool achieving an overall precision of 93.7%.

## 16. DesignRepair: Dual-Stream Design Guideline-Aware Frontend Repair with Large Language Models

**Authors:** Mingyue Yuan (The university of new South Wales), Jieshan Chen (CSIRO's Data61), Zhenchang Xing (CSIRO's Data61), Aaron Quigley (CSIRO's Data61), Yuyu Luo (HKUST (GZ)), Tianqi Luo (HKUST (GZ)), Gelareh Mohammadi (The university of new South Wales), Qinghua Lu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** Testing and Quality, Program Analysis and Verification, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11030228

**中文总结:** 提出 DesignRepair 双流前端修复系统，结合 Material Design 知识库、大语言模型与 Playwright 从代码与渲染页两面对齐设计规范。

**Abstract:** The rise of Large Language Models (LLMs) has streamlined frontend interface creation through tools like Vercel's V0, yet surfaced challenges in design quality (e.g., accessibility, and usability). Current solutions, often limited by their focus, generalisability, or data dependency, fall short in addressing these complexities comprehensively. Moreover, none of them examine the quality of LLM-generated UI design. In this work, we introduce DesignRepair, a novel dual-stream design guideline-aware system to examine and repair the UI design quality issues from both code aspect and rendered page aspect. We utilised the mature and popular Material Design as our knowledge base to guide this process. Specifically, we first constructed a comprehensive knowledge base encoding Google's Material Design principles into low-level component knowledge base and high-level system design knowledge base. After that, DesignRepair employs a LLM for the extraction of key components and utilizes the Playwright tool for precise page analysis, aligning these with the established knowledge bases. Finally, we integrate Retrieval-Augmented Generation with state-of-the-art LLMs like GPT-4 to holistically refine and repair frontend code through a strategic divide and conquer approach. Our extensive evaluations validated the efficacy and utility of our approach, demonstrating significant enhancements in adherence to design guidelines, accessibility, and user experience metrics.

## 17. Does GenAI Make Usability Testing Obsolete?

**Authors:** Ali Ebrahimi Pourasad, Walid Maalej (University of Hamburg)

**Categories:** AI for Software Engineering, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029918

**中文总结:** 提出视觉语言模型工具 UX-LLM 预测 iOS 应用可用性问题，精确率 0.61–0.66、召回率 0.35–0.38，尚无法取代传统可用性测试。

**Abstract:** Ensuring usability is crucial for the success of mobile apps. Usability issues can compromise user experience and negatively impact the perceived app quality. This paper presents UX-LLM, a novel tool powered by a Large Vision-Language Model that predicts usability issues in iOS apps. To evaluate the performance of UX-LLM we predicted usability issues in two open-source apps of a medium complexity and asked usability experts to assess the predictions. We also performed traditional usability testing and expert review for both apps and compared the results to those of UX-LLM. UX-LLM demonstrated precision ranging from 0.61 and 0.66 and recall between 0.35 and 0.38, indicating its ability to identify valid usability issues, yet failing to capture the majority of issues. Finally, we conducted a focus group with an app development team of a capstone project developing a transit app for visually impaired persons. The focus group expressed positive perceptions of UX-LLM as it identified unknown usability issues in their app. However, they also raised concerns about its integration into the development workflow, suggesting potential improvements. Our results show that UX-LLM cannot fully replace traditional usability evaluation methods but serves as a valuable supplement particularly for small teams with limited resources, to identify issues in less common user paths, due to its ability to inspect the source code.

## 18. DPFuzzer: Discovering Safety Critical Vulnerabilities for Drone Path Planners

**Authors:** Yue Wang, Chao Yang (Xidian University), Xiaodong Zhang, Yuwanqi Deng (Xidian University), Jianfeng Ma (Xidian University)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029794

**中文总结:** 提出 DPFuzzer，用进化算法与 Environmental Risk Factor 指标生成多样危险障碍场景，测试无人机路径规划器的安全关键漏洞。

**Abstract:** State-of-the-art drone path planners enable drones to autonomously navigate around obstacles in GPS-denied, uncharted and cluttered environments. However, our investigation shows that path planners fail to maneuver drones correctly in specific scenarios, leading to incidents such as collisions. To minimize such risks, drone path planners should be tested thoroughly against diverse scenarios before deployment. Existing research for testing drones to uncover safety-critical vulnerabilities is only focused on the flight control programs and is limited in the capability to generate diverse obstacle scenarios for testing drone path planners. In this work, we propose \textit{DPFuzzer}, an automated framework for testing drone path planners. \textit{DPFuzzer} is an evolutionary algorithm (EA) based testing framework. It aims to uncover vulnerabilities in drone path planners by generating diverse critical scenarios that can trigger vulnerabilities. To better guide the critical scenario generation, we introduce \textit{Environmental Risk Factor (ERF)}, a metric we propose, to abstract potential safety threats of scenarios. We evaluate \textit{DPFuzzer} on state-of-the-art drone path planners and the experimental result shows that \textit{DPFuzzer} can effectively find diverse vulnerabilities. Additionally, we demonstrate that these vulnerabilities are exploitable in the real world on commercial drones.

## 19. Early Detection of Performance Regressions by Bridging Local Performance Data and Architectural Models

**Authors:** Lizhi Liao (Memorial University of Newfoundland), Simon Eismann (University of Würzburg), Heng Li (Polytechnique Montréal), Cor-Paul Bezemer (University of Alberta), Diego Elias Costa (Concordia University, Canada), André van Hoorn (University of Hamburg, Germany), Weiyi Shang (University of Waterloo)

**Categories:** Testing and Quality, Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029855

**中文总结:** 提出桥接本地性能数据与架构模型的方法，在系统未完全部署前早期检测性能回归，弥补系统级与组件级测试的不足。

**Abstract:** During software development, developers often make numerous modifications to the software to address existing issues or implement new features. However, certain changes may inadvertently have a detrimental impact on the overall system performance. To ensure that the performance of new software releases does not degrade (i.e., absence of performance regressions), existing practices rely on system-level performance testing, such as load testing, or component-level performance testing, such as microbenchmarking, to detect performance regressions. However, performance testing for the entire system is often expensive and time-consuming, posing challenges to adapting to the rapid release cycles common in modern DevOps practices. In addition, system-level performance testing cannot be conducted until the system is fully built and deployed. On the other hand, component-level testing focuses on isolated components, neglecting overall system performance and the impact of system workloads. In this paper, we propose a novel approach to early detection of performance regressions by bridging the local performance data generated by component-level testing and the system-level architectural models. Our approach uses local performance data to identify deviations at the component level, and then propagate these deviations to the architectural model. We then use the architectural model to predict regressions in the performance of the overall system. In an evaluation of our approach on two representative open-source benchmark systems, we show that it can effectively detect end-to-end system performance regressions from local performance deviations with different intensities and under various system workloads. More importantly, our approach can detect regressions as early as in the development phase, in contrast to existing approaches that require the system to be fully built and deployed. Our approach is lightweight and can complement traditional system performance testing when testing resources are scarce.

## 20. Efficient Domain Augmentation for Autonomous Driving Testing Using Diffusion Models

**Authors:** Luciano Baresi (Politecnico di Milano), Davide Yi Xian Hu (Politecnico di Milano), Andrea Stocco (Technical University of Munich, fortiss), Paolo Tonella (USI Lugano)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029946

**中文总结:** 将扩散模型与物理仿真结合做自动驾驶 ODD 域增强，评估指令编辑、inpainting 等策略的有效性与开销，并验证合成场景对系统级泛化测试的价值。

**Abstract:** Simulation-based testing is widely used to assess the reliability of Autonomous Driving Systems (ADS), but its effectiveness is limited by the operational design domain (ODD) conditions available in such simulators. To address this limitation, in this work, we explore the integration of generative artificial intelligence techniques with physics-based simulators to enhance ADS system-level testing. Our study evaluates the effectiveness and computational overhead of three generative strategies based on diffusion models, namely instruction-editing, inpainting, and inpainting with refinement. Specifically, we assess these techniques' capabilities to produce augmented simulator-generated images of driving scenarios representing new ODDs. We employ a novel automated detector for invalid inputs based on semantic segmentation to ensure semantic preservation and realism of the neural generated images. We then perform system-level testing to evaluate the ADS's generalization ability to newly synthesized ODDs. Our findings show that diffusion models help increase the ODD coverage for system-level testing of ADS. Our automated semantic validator achieved a percentage of false positives as low as 3\%, retaining the correctness and quality of the generated images for testing. Our approach successfully identified new ADS system failures before real-world testing.

## 21. EP-Detector: Automatic Detection of Error-prone Operation Anomalies in Android Applications

**Authors:** Chenkai Guo (Nankai University, China), Qianlu Wang (College of Cyber Science, Nankai University), Naipeng Dong (The University of Queensland, Australia), Lingling Fan (Nankai University), Tianhong Wang (College of Computer Science, Nankai University), Weijie Zhang (College of Computer Science, Nankai University), EnBao Chen (College of Cyber Science, Nankai University), Zheli Liu (Nankai University), Lu Yu (National University of Defense Technology; Anhui Province Key Laboratory of Cyberspace Security Situation Awareness and Evaluation)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029849

**中文总结:** 首次系统刻画 Android 易误操作异常（EPA），从主体、客体与环境三维度归因，并提出动态 GUI 测试工具 EP-Detector 自动检测。

**Abstract:** Android applications are pervasively adopted and heavily relied on in our daily life, leading to the growing demand for enhanced user experiences, such as ease for operation and robustness. Nevertheless, developers continue to prioritize traditional functionality and performance, overlooking the pivotal role of user experience in real-world scenarios. For example, poorly designed page elements can lead to user confusion, resulting in unexpected outcomes, termed as the error-prone operation anomalies (EPAs). In this work, we undertake the first effort to uncover the underlying essence of the EPA problem. To achieve this objective, we investigated the root causes of EPAs from three dimensions, i.e., subject, object and environment. These causes were identified by multi-stage attribute capturing and precise similarity computation. In this process, the causes are categorized into fine-grained classes, namely confusing behaviours, unsuitable layout, and resource overload. Building upon these insights, we propose a dynamic GUI-based testing tool EP-Detector to facilitate detecting the EPAs in real-world apps. The EP-Detector is equipped with widget-exploration based target navigation and automatic test oracle, enabling it to detect error-prone page elements and simulate events with both comprehensiveness and precision. To systematically study the prevalence and severity of real-world EPAs, we conducted experiments on 53 popular Android apps with EP-Detector. The confirmed results not only validate the high precision and completeness of EP-Detector but also highlight that EPAs are prevalent in current apps, with at least one EPA existing in every two page widgets on average, and 28.3% of them may lead to security and functionality issues or risks. The EP-Detector is available at https://github.com/WordDealer/EP-Detector.

## 22. Execution Trace Reconstruction Using Diffusion-Based Generative Models

**Authors:** Madeline Janecek (Brock University), Naser Ezzati-Jivan, Abdelwahab Hamou-Lhadj (Concordia University, Montreal, Canada)

**Categories:** AI for Software Engineering, Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029922

**中文总结:** 首次系统评估扩散模型重建不完整执行追踪序列，SSSD^S4 在九个 Phoronix 数据集上于多种缺失比例下表现最优。

**Abstract:** Execution tracing is essential for understanding system and software behaviour, yet lost trace events can significantly compromise data integrity and analysis. Existing solutions for trace reconstruction often fail to fully leverage available data, particularly in complex and high-dimensional contexts. Recent advancements in generative artificial intelligence, particularly diffusion models, have set new benchmarks in image, audio, and natural language generation. This study conducts the first comprehensive evaluation of diffusion models for reconstructing incomplete trace event sequences. Using nine distinct datasets generated from the Phoronix Test Suite, we rigorously test these models on sequences of varying lengths and missing data ratios. Our results indicate that the SSSD$^{S4}$ model, in particular, achieves superior performance, in terms of accuracy, perfect rate, and ROUGE-L score across diverse imputation scenarios. These findings underscore the potential of diffusion-based models to accurately reconstruct missing events, thereby maintaining data integrity and enhancing system monitoring and analysis.

## 23. exLong: Generating Exceptional Behavior Tests with Large Language Models

**Authors:** Jiyang Zhang (University of Texas at Austin), Yu Liu (Meta), Pengyu Nie (University of Waterloo), Junyi Jessy Li (University of Texas at Austin, USA), Milos Gligoric (The University of Texas at Austin)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029954

**中文总结:** 提出 EXLÓNG，基于 CodeLlama 微调的大模型自动生成异常行为测试，弥补开发者主要测试正常路径而忽视异常路径的不足。

**Abstract:** Many popular programming languages, including C#, Java, and Python, support exceptions. Exceptions are thrown during program execution if an unwanted event happens, e.g., a method is invoked with an illegal argument value. Software developers write exceptional behavior tests (EBTs) to check that their code detects unwanted events and throws appropriate exceptions. Prior research studies have shown the importance of EBTs, but those studies also highlighted that developers put most of their efforts on “happy paths”, e.g., paths without unwanted events. To help developers fill the gap, we present the first framework, dubbed EXLÓNG, that automatically generates EBTs. EXLÓNG is a large language model instruction-tuned from CodeLlama and embeds reasoning about traces that lead to throw statements, conditional expressions that guard throw statements, and non-exceptional behavior tests that execute similar traces. We compare EX LÓNG with the state-of-the-art models for test generation (CAT-LM) and one of the strongest foundation models (GPT3.5), as well as with analysis-based tools for test generation (Randoop and EvoSuite). Our results show that EXLÓNG outperforms existing models and tools. Furthermore, we contributed several pull requests to open-source projects and 23 EBTs generated by EXLÓNG were already accepted.

## 24. Faster Configuration Performance Bug Testing with Neural Dual-level Prioritization

**Authors:** Youpeng Ma (University of Electronic Science and Technology of China), Tao Chen (University of Birmingham), Ke Li (University of Exeter)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029809

**中文总结:** 提出 NDP，在配置项与取值范围两个层级用神经网络优先排序并自动估计测试预言，显著加速配置性能缺陷（CPBug）检测。

**Abstract:** As software systems become more complex and configurable, more performance problems tend to arise from the configuration designs. This has caused some configuration options to unexpectedly degrade performance which deviates from their original expectations designed by the developers. Such discrepancies, namely configuration performance bugs (CPBugs), are devastating and can be deeply hidden in the source code. Yet, efficiently testing CPBugs is difficult, not only due to the test oracle is hard to set, but also because the configuration measurement is expensive and there are simply too many possible configurations to test. As such, existing testing tools suffer from lengthy runtime or have been ineffective in detecting CPBugs when the budget is limited, compounded by inaccurate test oracle. In this paper, we seek to achieve significantly faster CPBug testing by neurally prioritizing the testing at both the configuration option and value range levels with automated oracle estimation. Our proposed tool, dubbed NDP, is a general framework that works with different heuristic generators. The idea is to leverage two neural language models: one to estimate the CPBug types that serve as the oracle while, more vitally, the other to infer the probabilities of an option being CPBug-related, based on which the options and the value ranges to be searched can be prioritized. Experiments on several widely-used systems of different versions reveal that NDP can, in general, better predict CPBug type in 87% cases and find more CPBugs with up to 88.88$\times$ testing efficiency speedup over the state-of-the-art tools.

## 25. Feature-Driven End-To-End Test Generation

**Authors:** Parsa Alian (University of British Columbia), Noor Nashid (University of British Columbia), Mobina Shahbandeh (University of British Columbia), Taha Shabani (University of British Columbia), Ali Mesbah (University of British Columbia)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029959

**中文总结:** 提出 AUTOE2E，利用 LLM 推断 Web 应用功能并生成语义化端到端测试，同时发布 E2EBENCH 基准；平均功能覆盖率达 79%，较最佳基线提升 558%。

**Abstract:** End-to-end (E2E) testing is essential for ensuring web application quality. However, manual test creation is time-consuming and current test generation techniques produce random tests. In this paper, we present AUTOE2E, a novel approach that leverages Large Language Models (LLMs) to automate the generation of semantically meaningful feature-driven E2E test cases for web applications. AUTOE2E intelligently infers potential features within a web application and translates them into executable test scenarios. Furthermore, we address a critical gap in the research community by introducing E2EBENCH, a new benchmark for automatically assessing the feature coverage of E2E test suites. Our evaluation on E2EBENCH demonstrates that AUTOE2E achieves an average feature coverage of 79%, outperforming the best baseline by 558%, highlighting its effectiveness in generating high-quality, comprehensive test cases.

## 26. Fidelity of Cloud Emulators: The Imitation Game of Testing Cloud-based Software

**Authors:** Anna Mazhar (Cornell University), Saad Sher Alam (University of Illinois Urbana-Champaign), William Zheng (University of Illinois Urbana-Champaign), Yinfang Chen (University of Illinois at Urbana-Champaign), Suman Nath (Microsoft Research), Tianyin Xu (University of Illinois at Urbana-Champaign)

**Categories:** Testing and Quality, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029917

**中文总结:** 系统分析 Azure 与 AWS 五类云服务的 255 个 API，发现 37% 在模拟器与真实服务间行为不一致，威胁离线测试可信度。

**Abstract:** Modern software projects have been increasingly using cloud services as important components. The cloud-based programming practice greatly simplifies software development by harvesting cloud benefits (e.g., high availability and elasticity). However, it imposes new challenges for software testing and analysis, due to opaqueness of cloud backends and monetary cost of invoking cloud services for continuous integration and deployment. As a result, cloud emulators are developed for offline development and testing, before online testing and deployment. This paper presents a systematic analysis of cloud emulators from the perspective of cloud-based software testing. Our goal is to (1) understand the discrepancies introduced by cloud emula- tion with regard to software quality assurance and deployment safety and (2) address inevitable gaps between emulated and real cloud services. The analysis results are concerning. Among 255 APIs of five cloud services from Azure and Amazon Web Services (AWS), we detected discrepant behavior between the emulated and real services in 94 (37%) of the APIs. These discrepancies lead to inconsistent testing results, threatening deployment safety, introducing false alarms, and creating debuggability issues. The root causes are diverse, including accidental implementation defects and essential emulation challenges. We discuss potential solutions and develop a practical mitigation technique to address discrepancies of cloud emulators for software testing.

## 27. Fork State-Aware Differential Fuzzing for Blockchain Consensus Implementations

**Authors:** Won Hoi Kim (KAIST), Hocheol Nam (KAIST), Muoi Tran (ETH Zurich), Amin Jalilov (KAIST), Zhenkai Liang (National University of Singapore), Sang Kil Cha (KAIST), Min Suk Kang (KAIST)

**Categories:** Testing and Quality, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029786

**中文总结:** 提出 Forky 分叉状态感知差分模糊测试框架，以分叉感知变异与反馈检测比特币、以太坊等区块链共识实现的分叉处理差异。

**Abstract:** Blockchain networks allow multiple client implementations of the same consensus algorithm by different developers to coexist in the same system. Ensuring correct implementations among these heterogeneous clients is crucial, as even slight semantic discrepancies in their implementations can lead to safety failures. While existing fuzzing frameworks have discovered implementation flaws in blockchain, they suffer from several challenges in testing them with sequences of conflicting blocks, called forks. Existing tools fail to adequately assess the fork-handling processes in blockchain implementations when relying on traditional code coverage feedback, which lacks the granularity needed to navigate the diverse and complex fork-handling scenarios. This paper introduces Forky, a fork state-aware differential fuzzing framework designed to detect implementation discrepancies within the critical fork-handling process with its novel fork-aware mutation and fork-diversifying feedback mechanisms. We test Forky on the two most influential blockchain projects: Bitcoin and Ethereum, which are the representatives of the two major blockchain consensus algorithm families, Proofof-Work (PoW) and Proof-of-Stake (PoS) consensus algorithms.

## 28. Fuzzing MLIR Compilers with Custom Mutation Synthesis

**Authors:** Ben Limpanukorn (UCLA), Jiyuan Wang (University of California at Los Angeles), Hong Jin Kang (University of Sydney), Zitong Zhou (UCLA), Miryung Kim (UCLA and Amazon Web Services)

**Categories:** Testing and Quality, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029941

**中文总结:** 提出 SYNTHFUZZ，从现有测试自动推断参数化、上下文相关的 MLIR 方言定制变异，无需为每种新方言手写变异逻辑。

**Abstract:** A growing trend in compiler design is to enable modular extensions to intermediate representations (IRs). Multi- Level Intermediate Representation (MLIR) is a new effort to enable faster compiler development by providing an extensible framework for downstream developers to define custom IRs with MLIR dialects. Sets of MLIR dialects define new IRs that are tailored for specific domains. The diversity and rapid evolution of these IRs make it impractical to pre-define custom test generator logic for every available dialect. We design a new approach called SYNTHFUZZ that automatically infers and applies custom mutations from existing tests. The key essence of SYNTHFUZZ is that inferred custom mutations are parameterized and context-dependent such that they can be concretized differently depending on the target context. By doing this, we obviate the need to manually write custom mutations for newly introduced MLIR dialects. Further, SYNTHFUZZ increases the chance of finding effective edit locations and reduces the chance of inserting invalid edit content by performing k-ancestor- prefix and l-sibling-postfix matching. We compare SYNTHFUZZ to three baselines: Grammarinator—a grammar-based fuzzer without custom mutators, MLIRSmith—a custom test generator for MLIR, and NeuRI—a custom test generator with support for parameterized generation. We conduct this comprehensive comparison on 4 different MLIR projects where each project defines a new set of MLIR dialects that would take months of effort to manually write custom input generation and mutation logic. Our evaluation shows that SYNTHFUZZ on average improves input diversity by 1.51×, which increases branch coverage by 1.16×. Further, we show that our context dependent custom mutation increases the proportion of valid tests by up to 1.11×, indicating that SYNTHFUZZ correctly concretizes its parameterized mutations with respect to the target context. Parameterization of the mutations reduces the fraction of tests violating general MLIR constraints by 0.57×, increasing the time spent fuzzing dialect-specific code.

## 29. GARL: Genetic Algorithm-Augmented Reinforcement Learning to Detect Violations in Marker-Based Autonomous Landing Systems

**Authors:** Linfeng Liang (Macquarie University), Yao Deng (Macquarie University), Kye Morton (Skyy Network), Valtteri Kallinen (Skyy Network), Alice James (Macquarie University), Avishkar Seth (Macquarie University), Endrowednes Kuantama (Macquarie University), Subhas Mukhopadhyay (Macquarie University), Richard Han (Macquarie University), Xi Zheng (Macquarie University)

**Categories:** AI for Software Engineering, Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029873

**中文总结:** 提出 GARL 框架，将遗传算法与强化学习结合高效生成无人机自主着陆系统违规场景，性能较现有方法最高提升 18.35%。

**Abstract:** Automated Uncrewed Aerial Vehicle (UAV) landing is crucial for autonomous UAV services such as monitoring, surveying, and package delivery. It involves detecting landing targets, perceiving obstacles, planning collision-free paths, and controlling UAV movements for safe landing. Failures can lead to significant losses, necessitating rigorous simulation-based testing for safety. Traditional offline testing methods, limited to static environments and predefined trajectories, may miss violation cases caused by dynamic objects like people and animals. Conversely, online testing methods require extensive training time, which is impractical with limited budgets. To address these issues, we introduce GARL, a framework combining a genetic algorithm (GA) and reinforcement learning (RL) for efficient generation of diverse and real landing system failures within a practical budget. GARL employs GA for exploring various environment setups offline, reducing the complexity of RL's online testing in simulating challenging landing scenarios. Our approach outperforms existing methods by up to 18.35% in violation rate and 58% in diversity metric. We validate most discovered violation types with real-world UAV tests, pioneering the integration of offline and online testing strategies for autonomous systems. This method opens new research directions for online testing, with our code available at https://anonymous.4open.science/r/drone_testing-5CF0/.

## 30. Improved Detection and Diagnosis of Faults in Deep Neural Networks Using Hierarchical and Explainable Classification

**Authors:** Sigma Jahan (Dalhousie University), Mehil Shah (Dalhousie University), Parvez Mahbub (Dalhousie University), Masud Rahman (Dalhousie University)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029901

**中文总结:** 提出 DEFault，先以训练期动态特征做层次化故障检测，再结合静态特征与 SHAP 等可解释方法定位 DNN 程序根因，覆盖文献中主要故障类型。

**Abstract:** Deep Neural Networks (DNN) have found numerous applications in various domains, including fraud detection, medical diagnosis, facial recognition, and autonomous driving. However, DNN-based systems often suffer from reliability issues due to their inherent complexity and the stochastic nature of their underlying models. Unfortunately, existing techniques to detect faults in DNN programs are either limited by the types of faults (e.g., hyperparameter or layer) they support or the kind of information (e.g., dynamic or static) they use. As a result, they might fall short of comprehensively detecting and diagnosing the faults. In this paper, we present DEFault (Detect and Explain Fault) -- a novel technique to detect and diagnose faults in DNN programs. It first captures dynamic (i.e., runtime) features during model training and leverages a hierarchical classification approach to detect all major fault categories from the literature. Then, it captures static features (e.g., layer types) from DNN programs and leverages explainable AI methods (e.g., SHAP) to narrow down the root cause of the fault. We train and evaluate DEFault on a large, diverse dataset of ~14.5K DNN programs and further validate our technique using a benchmark dataset of 52 real-life faulty DNN programs. Our approach achieves ~94% recall in detecting real-world faulty DNN programs and ~63% recall in diagnosing the root causes of the faults, demonstrating 3.92%--11.54% higher performance than that of state-of-the-art techniques. Thus, DEFault has the potential to significantly improve the reliability of DNN programs by effectively detecting and diagnosing the faults.

## 31. Increasing the Effectiveness of Automatically Generated Tests by Improving Class Observability

**Authors:** Geraldine Galindo-Gutierrez (Centro de Investigación en Ciencias Exactas e Ingenierías, Universidad Católica Boliviana), Juan Pablo Sandoval Alcocer (Pontificia Universidad Católica de Chile), Nicolas Jimenez-Fuentes (Pontificia Universidad Católica de Chile), Alexandre Bergel (University of Chile), Gordon Fraser (University of Passau)

**Categories:** Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029845

**中文总结:** 针对 EvoSuite 自动生成测试可观测性不足的问题，通过代码变换与扩展机制提升测试缺陷发现能力。

**Abstract:** Automated unit test generation consists of two complementary challenges: Finding sequences of API calls that exercise the code of a class under test, and finding assertion statements that validate the behaviour of the class during execution. The former challenge is often addressed using meta-heuristic search algorithms optimising tests for code coverage, which are then annotated with regression assertions to address the latter challenge, i.e., assertions that capture the states observed during test generation. While the resulting tests tend to achieve high coverage, their fault finding potential is often inhibited by poor or difficult observability of the codebase. That is, relevant attributes and properties may either not be exposed adequately at all, or only in ways that the test generator is unable to handle. In this paper, we investigate the influence of observability in the context of the EvoSuite search-based Java test generator, which we extend in two complementary ways to study and improve observability: First, we apply a transformation to code under test to expose encapsulated attributes to the test generator; second, we address EvoSuite's limited capability of asserting the state of complex objects. Our evaluation demonstrates that together these observability improvements lead to significantly increased mutation scores, underscoring the importance of considering the class observability in the test generation process.

## 32. InSVDF: Interface-State-Aware Virtual Device Fuzzing

**Authors:** Zexiang Zhang (National University of Defense Technology), Gaoning Pan (Hangzhou Dianzi University), Ruipeng Wang (National University of Defense Technology), Yiming Tao (Zhejiang University), Zulie Pan (National University of Defense Technology), Cheng Tu (National University of Defense Technology), Min Zhang (National University of Defense Technology), Yang Li (National University of Defense Technology), Yi Shen (National University of Defense Technology), Chunming Wu (Zhejiang University)

**Categories:** Testing and Quality, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029782

**中文总结:** 提出 InSVDF，面向虚拟设备 DMA 接口做状态感知模糊测试，通过异步状态快照与深度感知种子保留缓解交互时机与深度不确定导致的效率问题。

**Abstract:** Hypervisor is the core technology of virtualization for emulating independent hardware resources for each virtual machine. Virtual devices serve as the main interface of the hypervisor, making the security of virtual devices crucial, as any vulnerabilities can impact the entire virtualization environment and pose a threat to the host machine's security. Direct Memory Access (DMA) is the interface of virtual devices, enabling communication with the host machine. Recently, many efforts have focused on fuzzing against DMA to discover the hypervisor's vulnerabilities. However, the lack of sensitivity to the DMA state causes these efforts to be hindered in efficiency during fuzzing. Specifically, there are two main issues: the uncertain interaction moment and the unclear interaction depth. In this paper, we introduce InSVDF, a DMA interface state-aware fuzzing engine. InSVDF first models the intra-interface state of the DMA interface and incorporates an asynchrony-aware state snapshot mechanism along with a depth-aware seed preservation mechanism. To validate our approach, we compare InSVDF with a state-of-the-art fuzzer. The results demonstrate that InSVDF significantly enhances vulnerability discovery speed, with improvements of up to 24.2x in the best case. Furthermore, InSVDF has identified 2 new vulnerabilities, one of which has been assigned a CVE ID.

## 33. Invivo Fuzzing by Amplifying Actual Executions

**Authors:** Octavio Galland (Canonical), Marcel Böhme (MPI for Security and Privacy)

**Categories:** Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029862

**中文总结:** 提出 Invivo 库模糊测试方法，放大宿主程序真实执行上下文对目标函数进行覆盖引导模糊测试，减少手工编写驱动成本。

**Abstract:** A major bottleneck that remains when fuzzing software libraries is the need for _fuzz drivers_, i.e., the glue code between the fuzzer and the library. Despite years of fuzzing, critical security flaws are still found, e.g., by manual auditing, because the fuzz drivers do not cover the complex interactions between the library and the host programs using it. In this work we propose an alternative approach to library fuzzing, which leverages a valid execution context that is set up by a given program using the library (the _host_), and _amplify_ its execution. More specifically, we execute the host until a designated function from a list of _target_ functions has been reached, and then perform coverage-guided function-level fuzzing on it. Once the fuzzing quota is exhausted, we move on to fuzzing the next target from the list. In this way we not only reduce the amount of manual work needed by a developer to incorporate fuzzing into their workflow, but we also allow the fuzzer to explore parts of the library as they are used in real-world programs that may otherwise not have been tested due to the simplicity of most fuzz drivers.

## 34. IRFuzzer: Specialized Fuzzing for LLVM Backend Code Generation

**Authors:** Yuyang Rong (University of California, Davis), Zhanghan Yu (University of California, Davis), Zhenkai Weng (University of California, Davis), Stephen Neuendorffer (Advanced Micro Devices, Inc.), Hao Chen (University of California at Davis)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029772

**中文总结:** 提出 IRFuzzer 面向 LLVM 后端代码生成的专用模糊测试，以约束变异保证 IR 合法并引入指令选择覆盖反馈。

**Abstract:** Modern compilers, such as LLVM, are complex. Due to their complexity, manual testing is unlikely to suffice, yet formal verification is difficult to scale. End-to-end fuzzing can be used, but it has difficulties in discovering LLVM backend problems for two reasons. First, frontend preprocessing and middle optimization shield the backend from seeing diverse inputs. Besides, edge coverages cannot provide an effective feedback as LLVM backend contains much reusable code. In this paper, we implement IRFuzzer to investigate the need of specialized fuzzing of the LLVM compiler backend. We focus on two approaches to improve the fuzzer: guaranteed input validity using constrained mutations to improve input diversity and new metrics to improve feedback quality. The mutator in IRFuzzer is capable of generating a wide range of LLVM IR inputs, including structured control flow, vector types, and function definitions. The system instruments coding patterns in the compiler to monitor the execution status of instruction selection. The instrumentation not only provides a new coverage feedback called matcher table coverage, but also provides an architecture specific guidance to the mutator. We show that IRFuzzer is more effective than existing fuzzers by fuzzing on 29 mature LLVM backend targets. In the process, we reported 78 confirmed new bugs in LLVM upstream, out of which 57 have been fixed, five have been back ported to LLVM 15, showing that specialized fuzzing provides useful and actionable insights to LLVM developers.

## 35. Iterative Generation of Adversarial Example for Deep Code Models

**Authors:** Li Huang, Weifeng Sun, Meng Yan (Chongqing University)

**Categories:** Software Engineering for AI, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029806

**中文总结:** 提出 ITGen 黑盒对抗样本生成方法，以位向量表示代码变体并结合失败攻击反馈，用增强贝叶斯优化迭代选取最有希望的变体，缓解局部最优与效率困境。

**Abstract:** Deep code models are vulnerable to adversarial attacks, making it possible for semantically identical inputs to trigger different responses. Current black-box attack methods typically prioritize the impact of identifiers on the model based on custom importance scores or program context and incrementally replace identifiers to generate adversarial examples. However, these methods often fail to fully leverage feedback from failed attacks to guide subsequent attacks, resulting in problems such as local optima bias and efficiency dilemmas. In this paper, we introduce ITGen, a novel black-box adversarial example generation method that iteratively utilizes feedback from failed attacks to refine the generation process. It employs a bitvector-based representation of code variants to mitigate local optima bias. By integrating these bit vectors with feedback from failed attacks, ITGen uses an enhanced Bayesian optimization framework to efficiently predict the most promising code variants, significantly reducing the search space and thus addressing the efficiency dilemma. We conducted experiments on a total of nine deep code models for both understanding and generation tasks, demonstrating ITGen's effectiveness and efficiency, as well as its ability to enhance model robustness through adversarial fine-tuning. For example, on average, ITGen improves the attack success rate by 47.98% and 69.70% over the state-of-the-art techniques (i.e., ALERT and BeamAttack), respectively.

## 36. Janus: Detecting Rendering Bugs in Web Browsers via Visual Delta Consistency

**Authors:** Chijin Zhou (Tsinghua University), Quan Zhang (Tsinghua University), Bingzhou Qian (National University of Defense Technology), Yu Jiang (Tsinghua University)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029880

**中文总结:** 提出视觉增量一致性测试准则，并实现浏览器渲染模糊测试器 Janus；通过对比轻微修改 HTML 后各浏览器渲染变化是否一致来发现渲染缺陷。

**Abstract:** Rendering lies at the heart of our modern web experience. However, the correctness of browser rendering is not always guaranteed, often leading to rendering bugs. Traditional differential testing, while successful in various domains, falls short when applied to rendering bug detection because an HTML file is likely yield different rendered outcomes across different browsers. This paper introduces Visual Delta Consistency, a test oracle to detect rendering bugs in web browsers, aiming to make rendered pages across browsers comparable. Our key insight is that any modifications made to an HTML file should uniformly influence rendering outcomes across browsers. Specifically, when presented with two HTML files that differ only by minor modifications, the reaction of all browsers should be consistent, i.e., either all browsers render them identically or all render them differently. Based on this insight, We implemented it as a practical fuzzer named Janus. It constructs pairs of slightly modified HTML files and observes the change statuses of the corresponding rendered pages across browsers for bug detection. We evaluated it on three widely-used browsers, i.e., Chrome, Safari, and Firefox. In total, Janus detected 34 rendering bugs, out of which 26 confirmed with 8 fixed by the developers.

## 37. Leveraging Large Language Models for Enhancing the Understandability of Generated Unit Tests

**Authors:** Amirhossein Deljouyi (Delft University of Technology), Roham Koohestani (Delft University of Technology), Mali Izadi (Delft University of Technology), Andy Zaidman (TU Delft)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029767

**中文总结:** 提出 UTGen，结合 EvoSuite 与 LLM 为自动生成单元测试补充上下文、命名与注释；用户实验显示修复 bug 数最多增 33%、耗时降 20%。

**Abstract:** Automated unit test generators, particularly search-based software testing tools like EvoSuite, are capable of generating tests with high coverage. Although these generators alleviate the burden of writing unit tests, they often pose challenges for software engineers in terms of understanding the generated tests. To address this, we introduce UTGen, which combines search-based software testing and large language models to enhance the understandability of automatically generated test cases. We achieve this enhancement through contextualizing test data, improving identifier naming, and adding descriptive comments. Through a controlled experiment with 32 participants, we investigate how the understandability of unit tests affects a software engineer's ability to perform bug-fixing tasks. We selected bug-fixing to simulate a real-world scenario that emphasizes the importance of understandable test cases. We observe that participants working on assignments with test cases fix up to 33% more bugs and use up to 20\% less time when compared to baseline test cases. From the post-test questionnaire, we gathered that participants found that enhanced test names, test data, and variable names improved their bug-fixing process.

## 38. Leveraging Propagated Infection to Crossfire Mutants

**Authors:** Hang Du (University of California at Irvine), Vijay Krishna Palepu (Microsoft), James Jones (University of California at Irvine)

**Categories:** Testing and Quality, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029834

**中文总结:** 研究发现最多 84% 存活变异体可通过断言放大检测，提出基于内存状态分析识别候选断言并结合交叉击杀模型的测试增强技术。

**Abstract:** Mutation testing was proposed to identify weaknesses in test suites by repeatedly generating artificially faulty versions of the software (i.e., *mutants*) and determining if the test suite is sufficient to detect them (i.e., *kill* them). When the tests are insufficient, each surviving mutant provides an opportunity to improve the test suite. We conducted a study and found that many such surviving mutants (up to 84% for the subjects of our study) are detectable by simply augmenting existing tests with additional assertions, or *assertion amplification*. Moreover, we find that many of these mutants are detectable by multiple existing tests, giving developers options for how to detect them. To help with these challenges, we created a technique that performs memory-state analysis to identify candidate assertions that developers can use to detect the surviving mutants. Additionally, we build upon prior research that identifies "crossfiring" opportunities -- tests that coincidentally kill multiple mutants. To this end, we developed a theoretical model that describes the varying granularities that crossfiring can occur in the existing test suite, which provide opportunities and options for how to kill surviving mutants. We operationalize this model to an accompanying technique that optimizes the assertion amplification of the existing tests to crossfire multiple mutants with fewer added assertions, optionally concentrated within fewer tests. Our experiments show that we can kill *all* surviving mutants that are detectable with existing test data with only 1.1% of the identified assertion candidates, and increasing by a factor of 6x, on average, the number of killed mutants from amplified tests, over tests that do not crossfire.

## 39. Lightweight Concolic Testing via Path-Condition Synthesis for Deep Learning Libraries

**Authors:** Sehoon Kim, Yonghyeon Kim (UNIST), Dahyeon Park (UNIST), Yuseok Jeon (UNIST), Jooyong Yi (UNIST), Mijung Kim (UNIST)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029909

**中文总结:** 提出首个面向深度学习库的轻量级混合测试：用归纳程序合成近似路径条件替代全符号执行，在可接受开销下更有效探索复杂库的执行路径。

**Abstract:** Many techniques have been recently developed for testing deep learning (DL) libraries, recently. Although these techniques have effectively improved API and code coverage and detected unknown bugs, they rely on black-box fuzzing for input generation. Concolic testing (also known as dynamic symbolic execution) can be more effective in exploring diverse execution paths, but applying it to DL libraries is extremely challenging due to their inherent complexity. In this paper, we introduce the first concolic testing technique for DL libraries. Our technique offers a lightweight approach that significantly reduces the heavy overhead associated with traditional concolic testing. While symbolic execution maintains symbolic expressions for every variable with non-concrete values to build a path condition, our technique computes approximate path conditions by inferring branch conditions via inductive program synthesis. Despite potential imprecision from approximation, our method's light overhead allows for effective exploration of diverse execution paths within the complex implementations of DL libraries. We have implemented our tool, PathFinder, and evaluated it on PyTorch and TensorFlow. Our results show that PathFinder outperforms existing API-level DL library fuzzers by achieving 57\% more branch coverage on average; up to 58\% higher than TitanFuzz and 125\% higher than FreeFuzz. PathFinder is also effective in bug detection, uncovering 61 crash bugs, 59 of which were confirmed by developers as previously unknown, with 32 already fixed.

## 40. LLM Based Input Space Partitioning Testing for Library APIs

**Authors:** Jiageng Li (Fudan University), Zhen Dong (Fudan University), Chong Wang (Nanyang Technological University), Haozhen You (Fudan University), Cen Zhang (Georgia Institute of Technology), Yang Liu (Nanyang Technological University), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029822

**中文总结:** 提出 LISP，利用 LLM 理解库 API 代码并进行输入空间划分，再据此引导各分区测试输入生成，缓解传统搜索式方法易生成无效输入、符号执行难以扩展的问题。

**Abstract:** Automated library APIs testing is difficult as it requires exploring a vast space of parameter inputs that may involve objects with complex data types. Existing search based approaches, with limited knowledge of relations between object states and program branches, often suffer from the low efficiency issue, i.e., tending to generate invalid inputs. Symbolic execution based approaches can effectively identify such relations, but fail to scale to large programs. In this work, we present an LLM-based input space partitioning testing approach, LISP, for library APIs. The approach leverages LLMs to understand the code of a library API under test and perform input space partitioning based on its understanding and rich common knowledge. Specifically, we provide the signature and code of the API under test to LLMs, with the expectation of obtaining a text description of each input space partition of the API under test. Then, the generated text description is employed to guide the input generation process for each partition, ultimately resulting in test suites that systematically explore the program behavior of the API. We evaluate LISP on 10 popular open-source Java libraries (e.g., apache/commons-lang with 2.6k stars, guava with 48.8k stars on GitHub). Our experiment results show that LISP is effective in library API testing. It significantly outperforms state-of-the-art tool EvoSuite in terms of branch coverage. On average, LISP achieves 67.82% branch coverage, surpassing EvoSuite by 1.21 times. In total, LISP triggers 404 exceptions or errors in the experiments, and discovers 13 previously unknown vulnerabilities during evaluation, which have been assigned CVE IDs.

## 41. LWDIFF: An LLM-Assisted Differential Testing Framework for WebAssembly Runtimes

**Authors:** Shiyao Zhou (The Hong Kong Polytechnic University), Jincheng Wang (Hong Kong Polytechnic University), He Ye (University College London (UCL)), Hao Zhou (The Hong Kong Polytechnic University), Claire Le Goues (Carnegie Mellon University), Xiapu Luo (Hong Kong Polytechnic University)

**Categories:** Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029747

**中文总结:** 提出 LWDIFF，用 LLM 从 Wasm 规范抽取知识并驱动变异，对解码、验证与执行三阶段做差分测试；在八个 Wasm 运行时上发现更多缺陷。

**Abstract:** WebAssembly (Wasm) runtimes execute Wasm programs, a popular low-level language for efficiently executing high-level languages in browsers, with broad applications across diverse domains. The correctness of those runtimes is critical for both functionality and security of Wasm execution, motivating testing approaches that target Wasm runtimes specifically. However, existing Wasm testing frameworks fail to generate test cases that effectively test all three phases of runtime, i.e., decoding, validation, and execution. To address this research gap, we propose a new differential testing framework for Wasm runtimes, which leverages knowledge from the Wasm language specification that prior techniques overlooked, enhancing comprehensive testing of runtime functionality. Specifically, we first use a large language model to extract that knowledge from the specification. We use that knowledge in the context of multiple novel mutation operators that generate test cases with diverse features to test all three runtime phases. We evaluate LWDIFF by applying it to eight Wasm runtimes. Compared with the state-of-the-art Wasm testers, LWDIFF achieves the highest branch coverage and identifies the largest number of bugs. In total, LWDIFF discovers 31 bugs across eight runtimes, all of which are confirmed, with 25 of them previously undiscovered.

## 42. Metamorphic-Based Many-Objective Distillation of LLMs for Code-related Tasks

**Authors:** Annibale Panichella (Delft University of Technology)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029766

**中文总结:** 发现蒸馏后代码 LLM 对等价蜕变代码的鲁棒性显著下降，提出 MORPH，将蜕变测试与多目标优化结合，在代码克隆与漏洞检测蒸馏中平衡准确率、效率与鲁棒性。

**Abstract:** Knowledge distillation compresses large language models (LLMs) into more compact and efficient versions that achieve similar accuracy on code-related tasks. However, as we demonstrate in this study, compressed models are four times less robust than the original LLMs when evaluated with metamorphic code. They have a 440% higher probability of misclassifying code clones due to minor changes in the code fragment under analysis, such as replacing parameter names with synonyms. To address this issue, we propose MORPH, a method that combines metamorphic testing with many-objective optimization for a robust distillation of LLMs for code. MORPH efficiently explores the models’ configuration space and generates Paretooptimal models that effectively balance accuracy, efficiency, and robustness to metamorphic code. Metamorphic testing measures robustness as the number of code fragments for which a model incorrectly makes different predictions between the original and their equivalent metamorphic variants (prediction flips). We evaluate MORPH on two tasks—code clone and vulnerability detection—targeting CodeBERT and GraphCodeBERT for distillation. Our comparison includes MORPH, the state-of-theart distillation method AVATAR, and the fine-tuned non-distilled LLMs. Compared to AVATAR, MORPH produces compressed models that are (i) 47% more robust, (ii) 25% more efficient (fewer FLOPs), while maintaining (iii) equal or higher accuracy (up to +6%), and (iv) similar model size.

## 43. Mobile Application Coverage: The 30% Curse and Ways Forward

**Authors:** Faridah Akinotcho (University of British Columbia, Canada), Lili Wei (McGill University), Julia Rubin (The University of British Columbia)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029955

**中文总结:** 通过两位专家深入探索 103 个 Android 应用的大规模实验，揭示 GUI 驱动测试约 30% 覆盖率上限的根因：设备配置与外部资源依赖使即便人工也难以覆盖剩余 70% 代码。

**Abstract:** Testing, security analysis, and other dynamic quality assurance approaches rely on mechanisms that invoke software under test, aiming to achieve high code coverage. A large number of invocation mechanisms proposed in the literature, in particular for Android mobile applications, employ GUI-driven application exploration. However, studies show that even the most advanced GUI exploration techniques can cover only around 30% of a real- world application. This paper aims to investigate “the remaining 70%”. By conducting a large-scale experiment involving two human experts, who thoroughly explored 61 benchmark and 42 popular apps from Google Play, we show that achieving a substantially larger coverage for real-world applications is impractical even if we factor out known GUI-based exploration issues, such as the inability to provide semantic inputs and the right order of events. The main reasons preventing humans from covering the entire application include application dependencies on device configurations and external resources. Thus, future investment into GUI-based exploration strategies is unlikely to lead to substantial improvements in coverage. To chart possible ways forward and explore approaches to satisfy/bypass these dependencies, we thoroughly analyze code-level properties guarding them. Our analysis shows that a large fraction of the dependencies could actually be successfully bypassed with relatively simple beyond- GUI exploration techniques. We hope our study can inspire future work in this area and also provide a realistic benchmark for evaluating this work.

## 44. Mock Deep Testing: Toward Separate Development of Data and Models for Deep Learning

**Authors:** Ruchira Manke (Tulane University, USA), Mohammad Wardat (Oakland University, USA), Foutse Khomh (Polytechnique Montréal), Hridesh Rajan (Tulane University)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029789

**中文总结:** 提出 mock 深度测试方法论，通过 mock 数据与 mock 模型解耦数据准备与模型设计，支持深度学习应用组件的独立单元测试与并行开发。

**Abstract:** While deep learning (DL) has permeated, and become an integral component of many critical software systems, today software engineering research hasn’t explored how to separately test data and models that are integral for DL approaches to work effectively. The main challenge in independently testing these components arises from the tight dependency between data and models. This research explores this gap, introducing our methodology of mock deep testing for unit testing of DL applications. To enable unit testing, we introduce a design paradigm that decomposes the workflow into distinct, manageable components, minimizes sequential dependencies, and modularizes key stages of the DL, including data preparation and model design. For unit testing these components, we propose modeling their dependencies using mocks. In the context of DL, mocks refer to mock data and mock model that mimic the behavior of the original data and model, respectively. This modular approach facilitates independent development and testing of the components, ensuring comprehensive quality assurance throughout the development process. We have developed KUnit, a framework for enabling mock deep testing for the Keras library, a popular library for developing DL applications. We empirically evaluated KUnit to determine the effectiveness of mocks in independently testing data and models. Our assessment of 50 DL programs obtained from Stack Overflow and GitHub shows that mocks effectively identified 10 issues in the data preparation stage and 53 issues in the model design stage. We also conducted a user study with 36 participants using KUnit to perceive the effectiveness of our approach. Participants using KUnit successfully resolved 25 issues in the data preparation stage and 38 issues in the model design stage. We also found that mock objects provide a lightweight emulation of the dependencies for unit testing, facilitating early bug detection. Lastly, to evaluate the usability of KUnit, we conducted a post-study survey. The results reveal that KUnit is helpful to DL application developers, enabling them to independently test each component (data and model) and resolve issues effectively in different stages.

## 45. NIODebugger: A Novel Approach to Repair Non-Idempotent-Outcome Tests with LLM-Based Agent

**Authors:** Kaiyao Ke (University of Illinois at Urbana-Champaign)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029812

**中文总结:** 提出 NIODebugger，首个面向非幂等结果（NIO） flaky 测试的 LLM 智能体修复框架，经检测、探索、修复三阶段定位并消除状态污染根因。

**Abstract:** Flaky tests, characterized by inconsistent results across repeated executions, present significant challenges in software testing, especially during regression testing. Recently, there has been emerging research interest in non-idempotent-outcome (NIO) flaky tests—tests that pass on the initial run but fail on subsequent executions within the same environment. Despite progress in utilizing Large Language Models (LLMs) to address flaky tests, existing methods have not tackled NIO flaky tests. The limited context window of LLMs restricts their ability to incorporate relevant source code beyond the test method itself, often overlooking crucial information needed to address state pollution, which is the root cause of NIO flakiness. This paper introduces NIODebugger, the first framework to utilize an LLM-based agent for fixing flaky tests. NIODebugger features a three-phase design: detection, exploration, and fixing. In the detection phase, dynamic analysis provides critical information (such as stack traces and custom test execution logs) from multiple test runs, which helps in understanding accumulative state pollution. During the exploration phase, the LLM-based agent identifies and provides instructions for extracting relevant source code associated with test flakiness. In the fixing phase, NIODebugger repairs the tests using the information gathered from the previous phases. NIODebugger can be integrated with multiple LLMs, achieving patching success rates ranging from 11.63% to 58.72%. Its best-performing variant, NIODebugger-GPT-4, successfully generated correct patches for 101 out of 172 previously unknown NIO tests across 20 large-scale open-source projects. We submitted pull requests for all generated patches; 58 have been merged, only 1 was rejected, and the remaining 42 are pending. The implementation of NIODebugger is provided as a Maven plugin accessible at https://github.com/NIOTester/NIODebugger.

## 46. No Harness, No Problem: Oracle-guided Harnessing for Auto-generating C API Fuzzing Harnesses

**Authors:** Gabriel Sherman (University of Utah), Stefan Nagy (University of Utah)

**Categories:** Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029825

**中文总结:** 提出 Oracle 引导的 C API 模糊测试 harness 自动生成方法，解决现有学习式 harness 语义缺失导致误报崩溃的问题，使 fuzzing 能覆盖更多关键库 API。

**Abstract:** Library APIs are used by virtually every modern application and system, making them among today’s most security-critical software. In recent years, library bug-finding efforts have overwhelmingly adopted the powerful testing strategy of coverage-guided fuzzing. At its core, API fuzzing operates on harnesses: wrapper programs that initialize an API before feeding random inputs to its functions. Successful fuzzing demands correct and thorough harnesses, making manual harnessing challenging without sufficient domain expertise. To overcome this, recent strategies propose “learning” libraries’ intended usage to automatically generate their fuzzing harnesses. Yet, despite their high code coverage, resulting harnesses frequently miss key API semantics—bringing with them invalid, unrealistic, or otherwise-impossible data and call sequences—derailing fuzzing with false-positive crashes. Thus, without a precise, semantically-correct harnessing, many critical APIs will remain beyond fuzzing’s reach—leaving their hidden vulnerabilities ripe for attackers. This paper introduces Oracle-guided Harnessing: a technique for fully-automatic, semantics-aware API fuzzing harness synthesis. At a high level, Oracle-guided Harnessing mimics the trial-and-error process of manual harness creation—yet automates it via fuzzing. Specifically, we leverage information from API headers to mutationally stitch-together candidate harnesses; and evaluate their validity via a set of Correctness Oracles: compilation, execution, and changes in coverage. By keeping— and further mutating—only correct candidates, our approach produces a diverse set of semantically-correct harnesses for complex, real-world libraries in as little as one hour. We integrate Oracle-guided Harnessing as a prototype, OGHARN; and evaluate it alongside today’s leading fully-automatic harnessing approach, Hopper, and a plethora of developer-written harnesses from OSS-Fuzz. Across 20 real-world APIs, OGHARN outperforms developer-written harnesses by a median 14% code coverage, while uncovering 31 and 30 more vulnerabilities than both Hopper and developer-written harnesses, respectively—with zero false-positive crashes. Of the 41 new vulnerabilities found by OGHARN, all 41 are confirmed by developers—40 of which are since fixed—with many found in APIs that, until now, lacked harnesses whatsoever.

## 47. On the Mistaken Assumption of Interchangeable Deep Reinforcement Learning Implementations

**Authors:** Rajdeep Singh Hundal (National University of Singapore), Yan Xiao (Sun Yat-sen University), Xiaochun Cao (Sun Yat-Sen University), Jin Song Dong (National University of Singapore), Manuel Rigger (National University of Singapore)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029867

**中文总结:** 通过差分测试揭示同一 DRL 算法（如 DQN、PPO）不同实现存在显著性能差异，挑战其可互换假设并影响既有研究结论的可信度。

**Abstract:** \emph{Deep Reinforcement Learning} (DRL) is a paradigm of artificial intelligence where an \emph{agent} uses a neural network to learn which actions to take in a given \emph{environment}. DRL has recently gained traction from being able to solve complex environments like driving simulators, 3D robotic control, and multiplayer-online-battle-arena video games. Numerous \emph{implementations} of the state-of-the-art algorithms responsible for training these agents, like the \emph{Deep Q-Network} (DQN) and \emph{Proximal Policy Optimization} (PPO) algorithms, currently exist. However, studies make the mistake of assuming implementations of the same algorithm to be consistent and thus, \emph{interchangeable}. In this paper, through a \emph{differential testing} lens, we present the results of studying the extent of implementation inconsistencies, their effect on the implementations' performance, as well as their impact on the conclusions of prior studies under the assumption of interchangeable implementations. The outcome of our differential tests showed significant discrepancies between the tested algorithm implementations, indicating that they are \textit{not} interchangeable. In particular, out of the five PPO implementations tested on 56 games, three implementations achieved superhuman performance for 50\% of their total trials while the other two implementations only achieved superhuman performance for less than 15\% of their total trials. Furthermore, the performance among the high-performing PPO implementations was found to differ significantly in nine games. As part of a meticulous manual analysis of the implementations' source code, we analyzed implementation discrepancies and determined that code-level inconsistencies primarily caused these discrepancies. Lastly, we replicated a study and showed that this assumption of implementation interchangeability was sufficient to \emph{flip} experiment outcomes. Therefore, this calls for a shift in how implementations are being used. In addition, we recommend for (1) replicability studies for studies mistakenly assuming implementation interchangeability, (2) DRL researchers and practitioners to adopt the differential testing methodology proposed in this paper to combat implementation inconsistencies, and (3) the use of large environment suites.

## 48. Parametric Falsification of Many Probabilistic Requirements under Flakiness

**Authors:** Matteo Camilli (Politecnico di Milano), Raffaela Mirandola (Karlsruhe Institute of Technology (KIT))

**Categories:** Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029952

**中文总结:** 结合参数化模型检测与多目标优化，离线预计算多条概率需求约束，在 flaky 仿真下高效 falsify 网络物理系统的多条独立需求。

**Abstract:** Falsification is a popular simulation-based testing method for Cyber-Physical Systems to find inputs that violate a formal requirement. It employs optimization algorithms to minimize a robustness metric that defines the satisfaction of a given property over an execution trace. Despite falsification representing an established approach, detecting violations considering many, possibly independent, requirements simultaneously, under flaky simulations is an open problem. We address this problem by proposing a novel approach that combines parametric model checking and many-objective optimization. We use parametric model checking to shift part of the complexity of the problem offline. We pre-compute numeric constraints for the satisfaction of all requirements on a parametric specification of the testing scenario. Flaky violations are then detected using many-objective optimization to explore the space of changing factors in the scenario and push the parameters out of all precomputed constraints. The results of our empirical evaluation using four open-source evaluation subjects with increasing complexity (number of requirements) show that our approach can falsify many requirements simultaneously, without hiding their individual contribution. The effectiveness, in terms of quantity and severity of violations, is significantly higher than random search as well as two selected state-of-the-art baseline approaches. Furthermore, the extra offline computation yields a negligible cost.

## 49. Practical Object-Level Sanitizer With Aggregated Memory Access and Custom Allocator

**Authors:** Xiaolei wang (National University of Defense Technology), Ruilin Li (National University of Defense Technology), Bin Zhang (National University of Defense Technology), Chao Feng (National University of Defense Technology), Chaojing Tang (National University of Defense Technology)

**Categories:** Testing and Quality, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029965

**中文总结:** 提出对象级地址消毒器 OLASan，在函数级聚合同对象内存访问并按需检查，在保持细粒度检测（含对象内溢出）的同时降低性能开销。

**Abstract:** To mitigate potential memory safety vulnerabilities, recently there have been significant advances in sanitizers for pre-production bug detection. However, the limited inability to balance performance and detection accuracy still holds. The main reason is due to excessive reliance on shadow memory and a large number of memory access checks at runtime, incurring a significant performance overhead (if fine-grained memory safety detection is performed, the overhead will be even greater). In this paper, we propose a novel Object-Level Address Sanitizer OLASan to reduce performance overhead further while implementing accurate memory violations (including intra-object overflow) detection. Unlike previous sanitizers ignoring the correlation between memory access and objects, OLASan aggregates multiple memory accesses of same object at function level to perform on-demand targeted sanitization, thus avoiding examining most memory accesses at runtime. Specifically, OLASan characterizes various memory access patterns to identify those which can be aggregated, and implements memory safety checks with customized memory tagging. We implement OLASan atop the LLVM framework and evaluate it on SPEC CPU benchmarks. Evaluations show that OLASan outperforms the state-of-the-art methods with 51.18%, 25.20% and 6.52% less runtime overhead than ASan, ASan−− and GiantSan respectively. Moreover, aided by customized memory tagging, OLASan achieves zero false negatives for the first time when testing Juliet suites. Finally, we confirm that OLASan also offers comparable detection capabilities on real bugs.

## 50. Ranking Relevant Tests for Order-Dependent Flaky Tests

**Authors:** Shanto Rahman (The University of Texas at Austin), Bala Naren Chanumolu (George Mason University), Suzzana Rafi (George Mason University), August Shi (The University of Texas at Austin), Wing Lam (George Mason University)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029933

**中文总结:** 提出 RankF，按测试成为顺序依赖 flaky 测试相关测试的可能性排序，帮助开发者更快定位首个顺序相关测试。

**Abstract:** One major challenge of regression testing is the presence of flaky tests, i.e., tests that may pass in one run but fail in another run for the same version of code. One prominent category of flaky tests are order-dependent (OD) flaky tests, which are tests that can pass or fail depending on the test-order in which the tests are run. To help developers debug and fix OD tests, prior work has attempted to automatically find OD-relevant tests, i.e., tests that will determine whether an OD test passes or fails depending on whether the OD-relevant tests are run before or after the OD test in the test-order. Prior work finds OD-relevant tests by running tests before the OD test, without regards to the tests’ likelihood of being OD-relevant tests. We propose RankF to rank tests in order of likelihood of being OD-relevant tests, so a developer can find the first OD-relevant test more quickly, without running tests as often. We propose two ranking approaches, each requiring different information. Our first approach, RankFL, relies on training a large-language model that analyzes test code. Our second approach, RankFO, relies on the analysis of prior test-order execution information. We evaluate our approaches on 155 OD tests from 34 modules across 24 open-source projects. We compare RankF against prior work baselines in terms of the time for finding the first OD-relevant test for an OD test. RankF on average finds the first OD-relevant test faster than the best of the baselines, providing speedups of 1.9X, 1.7X, and 2.6X for the three different types of OD-relevant tests we evaluate.

## 51. REDII: Test Infrastructure to Enable Deterministic Reproduction of Failures for Distributed Systems

**Authors:** Yang Feng (Nanjing University), Zheyuan Lin (Nanjing University), Dongchen Zhao (Nanjing University), Mengbo Zhou (Nanjing University), Jia Liu (Nanjing University), James Jones (University of California at Irvine)

**Categories:** Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029968

**中文总结:** 提出 REDII 分布式系统回归测试基础设施及 REDIT 框架，提供真实缺陷数据集与可泛化机制，支持失败的可确定复现与防回归。

**Abstract:** Despite the fact that distributed systems have become a crucial aspect of modern technology and support many of the software systems that enable modern life, developers experience challenges in performing regression testing of these systems. Existing solutions for testing distributed systems are often either: (1) specialized testing environments that are created specifically for each system by its development team, which requires substantial effort for each team, with little-to-no sharing of this effort across teams; or (2) randomized injection tools that are often computationally expensive and offer no guarantees of preventing regressions, due to their randomness. The challenge of providing a generalized and practical solution to trigger bugs for reproducing and demonstrating failures, as well as to guard against regressions, is largely unaddressed. In this work, we present REDII, an infrastructure for supporting regression testing of distributed systems. REDII contains a dataset of real bugs on common distributed systems, along with a generalizable testing framework REDIT that enables developers to write tests that can reproduce failures by providing ways to deterministically control distributed execution. In addition to the real failures in REDII from multiple distributed systems, REDIT provides a reusable, programmable, platform-agnostic, deterministic regression-testing framework for developers of distributed systems. It can help automate the running of such tests, for both practitioners and researchers. We demonstrate REDIT with 63 bugs that we selected in JIRA on 7 large and widely used distributed systems. Our case studies show that REDII can be used to allow developers to write tests that effectively reproduce bugs on distributed systems and generate specific scenarios for regression testing, as well as providing deterministic failure injection that can help developers and researchers to better understand deterministic failures that may occur in distributed systems in the future. Additionally, our studies show that REDII is efficient for real-world system regression testing, providing a powerful tool for all participants in this area.

## 52. Reduce Dependence for Sound Concurrency Bug Prediction

**Authors:** Shihao Zhu (State Key Laboratory of Computer Science,Institute of Software,Chinese Academy of Sciences,China), Yuqi Guo (Institute of Software, Chinese Academy of Sciences), Yan Cai (Institute of Software at Chinese Academy of Sciences), Bin Liang (Renmin University of China), Long Zhang (Institute of Software, Chinese Academy of Sciences), Rui Chen (Beijing Institute of Control Engineering; Beijing Sunwise Information Technology), Tingting Yu (Beijing Institute of Control Engineering; Beijing Sunwise Information Technology)

**Categories:** Testing and Quality, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029874

**中文总结:** 针对并发缺陷预测中“任意读均可影响后续执行”的过度保守假设导致漏报的问题，基于静态语义精炼读写依赖关系，在保持 soundness 前提下扩大线程交错探索空间以发现更多并发缺陷。

**Abstract:** Recently, dynamic concurrency bug predictions have kept making notable progress in improving concurrency coverage while ensuring soundness. Most of them rely solely on dynamic information in traces and overlook the static semantics of the program when predicting bugs. To ensure soundness, they assume that \textbf{any (memory) read can fully affect subsequent program execution via control-flow and data-flow}. However, the assumption over-approximates constraints among (memory) writes and reads and hence limits reordering space over thread interleaving, ultimately leading to false negatives. From program semantics, only a subset of reads actually affect their subsequent executions. Therefore, by refining dependencies between reads and subsequent executions based on static program semantics, one can refine the assumption and eliminate unnecessary constraints while still guaranteeing soundness. This can bring a chance to explore more thread interleaving space and uncover more concurrency bugs. However, refining dependencies can compromise soundness and bring heavy overhead. To tackle these challenges, this paper introduces the concept of Necessary Consistent Read Event (NRE) and a hybrid analysis algorithm. NRE refines dependencies between reads and their subsequent events and is used to identify necessary constraints where a read probably affects the execution of its subsequent events. Next, we design an efficient and accurate hybrid analysis algorithm to calculate NREs for each event in the trace. The hybrid analysis algorithm maps events to program SSA instructions and simulates executions based on the original trace. We focused on data race and developed NRE and the algorithm as a prototype tool ReconP on top of a recent work M2. We conducted a set of comparative experiments on MySQL with M2 and SeqCheck. The results show that ReconP can detect 46.9\% and 22.4\% more data races than M2 and SeqCheck, respectively. And the hybrid algorithm only accounts for 34\% of the total time cost.

## 53. ROSA: Finding Backdoors with Fuzzing

**Authors:** Dimitri Kokkonis (Université Paris-Saclay, CEA, List), Michaël Marcozzi (Université Paris-Saclay, CEA, List), Emilien Decoux (Université Paris-Saclay, CEA List), Stefano Zacchiroli (LTCI, Télécom Paris, Institut Polytechnique de Paris, Palaiseau, France)

**Categories:** Testing and Quality, Security and Vulnerability

**Awards:** Best Artifact, Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029775

**中文总结:** 提出 ROSA，将 AFL++ 灰盒模糊测试与 metamorphic 测试结合，在运行时检测代码级后门触发行为。

**Abstract:** A code-level backdoor is a hidden access, programmed and concealed within the code of a program. For instance, hard-coded credentials planted in the code of an FTP server would enable maliciously logging into all the deployed instances of this server. Confirmed software supply-chain attacks have led to the injection of backdoors into popular open-source projects, and backdoors have been discovered in various router firmware. Manual code auditing for backdoors is challenging and existing semi-automated approaches can handle only a limited amount of programs and backdoors, while requiring manual reverse-engineering of the audited (binary) program. Graybox fuzzing (automated semi-randomized testing) has grown in popularity due to its success in discovering vulnerabilities and hence stands as a strong candidate for improved backdoor detection. However, current fuzzing knowledge does not offer any means to detect the triggering of a backdoor at runtime. In this work we introduce ROSA, a novel approach (and tool) which combines a state-of-the-art fuzzer (AFL++) with a new metamorphic test oracle, capable of detecting runtime backdoor triggers. To facilitate the evaluation of ROSA, we have created ROSARUM, the first openly available benchmark for assessing the detection of various backdoors in diverse programs. Experimental evaluation shows that ROSA has a level of robustness, speed and automation similar to classical fuzzing. Compared to existing detection tools, it can handle a diversity of backdoors and programs and it does not rely on manually reverse-engineering the fuzzed binary code.

## 54. RUG: Turbo LLM for Rust Unit Test Generation

**Authors:** Xiang Cheng (Georgia Institute of Technology), Fan Sang (Georgia Institute of Technology), Yizhuo Zhai (Georgia Institute of Technology), Xiaokuan Zhang (George Mason University), Taesoo Kim (Georgia Institute of Technology)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029738

**中文总结:** 提出 RUG 端到端方案，针对 Rust 复杂类型系统自动生成可编译且高覆盖率的单元测试，克服传统工具与简单 LLM 提示的局限。

**Abstract:** Unit testing improves software quality by evaluating isolated sections of the program. This approach alleviates the need for comprehensive program-wide testing and confines the potential error scope within the software. However, unit test development is time-consuming, requiring developers to create appropriate test contexts and determine input values to cover different code regions. This problem is particularly pronounced in Rust due to its intricate type system, making traditional unit test generation tools ineffective in Rust projects. Recently, LLM have demonstrated their proficiency in understanding programming language and completing software engineering tasks. However, merely prompting LLM with a basic prompt like "generate unit test for the following source code" often results in code with compilation errors. In addition, LLM-generated unit tests often have limited test coverage. To bridge this gap and harness the capabilities of LLM, we design and implement RUG, an end-to-end solution to automatically generate the unit test for Rust projects. To help LLM's generated test pass Rust strict compilation checks, RUG designs a semantic-aware bottom-up approach to divide the context construction problem into dependent sub-problems. It solves these sub-problems sequentially using an LLM and merges them to a complete context. To increase test coverage, RUG integrates coverage-guided fuzzing with LLM to prepare fuzzing harnesses. Applying RUG on 17 real-world Rust programs (average 24,937 LoC), we show that RUG can achieve a high code coverage, up to 71.37%, closely comparable to human effort (73.18%). We submitted 113 unit tests generated by RUG covering the new code: 53 of them have been accepted, 17 were rejected, and 43 are pending for review.

## 55. SAND: Decoupling Sanitization from Fuzzing for Low Overhead

**Authors:** Ziqiao Kong (Nanyang Technological University), Shaohua Li (The Chinese University of Hong Kong), Heqing Huang (City University of Hong Kong), Zhendong Su (ETH Zurich)

**Categories:** Testing and Quality, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029723

**中文总结:** 提出 SAND，将 sanitizer 检查从 fuzzing 主循环解耦，仅在候选输入上启用插桩版本；基于 AFL++ 在 24 小时内以更低开销发现更多漏洞且无漏报。

**Abstract:** Sanitizers provide robust test oracles for various vulnerabilities. Fuzzing on sanitizer-enabled programs has been the best practice to find software bugs. Since sanitizers require heavy program instrumentation to insert run-time checks, sanitizer-enabled programs have much higher overhead compared to normally built programs. In this paper, we present SAND, a new fuzzing framework that decouples sanitization from the fuzzing loop. SAND performs fuzzing on a normally built program and only invokes the sanitizer-enabled program when input is shown to be interesting. Since most of the generated inputs are not interesting, i.e., not bug-triggering, SAND allows most of the fuzzing time to be spent on the normally built program. We further introduce execution pattern to practically and effectively identify interesting inputs. We implement SAND on top of AFL++ and evaluate it on 20 real-world programs. Our extensive evaluation highlights its effectiveness: in 24 hours, compared to all the baseline fuzzers, SAND significantly discovers more bugs while not missing any.

## 56. Scenario-Driven and Context-Aware Automated Accessibility Testing for Android Apps

**Authors:** Yuxin Zhang (Tianjin University), Sen Chen (Nankai University), Xiaofei Xie (Singapore Management University), Zibo Liu (College of Intelligence and Computing, Tianjin University), Lingling Fan (Nankai University)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029746

**中文总结:** 提出 A11yScan，以场景驱动 UI 探索提升 Android 无障碍测试覆盖率，并以运行时上下文感知检测降低误报与漏报。

**Abstract:** Mobile accessibility is increasingly important nowadays as it enables people with disabilities to use mobile applications to perform daily tasks. Ensuring mobile accessibility not only benefits those with disabilities but also enhances the user experience for all users, making applications more intuitive and user-friendly. Although numerous tools are available for testing and detecting accessibility issues in Android applications, a large number of false negatives and false positives persist due to limitations in the existing approaches, i.e., low coverage of UI scenarios and lack of consideration of runtime context. To address these problems, in this paper, we propose a scenario-driven exploration method for improving the coverage of UI scenarios, thereby detecting accessibility issues within the application, and ultimately reducing false negatives. Furthermore, to reduce false positives caused by not considering the runtime context, we propose a context-aware detection method that provides a more fine-grained detection capability. Our experimental results reveal that A11yScan can detect 1.7X more issues surpassing current state-of-the-art approaches like Xbot (3,991 vs. 2,321), thereby reducing the false negative rate by 41.84\%. Additionally, it outperforms established UI exploration techniques such as SceneDroid (952 vs. 661 UI scenarios), while achieving comparable activity coverage to recent leading GUI testing tools like GPTDroid on the available dataset (73\% vs. 71\%). Meanwhile, with the context-aware detection method, A11yScan effectively reduces the false positive rate by 21\%, validated with a 90.56\% accuracy rate through a user study.

## 57. SeeAction: Towards Reverse Engineering How-What-Where of HCI Actions from Screencasts for UI Automation

**Authors:** Dehai Zhao (CSIRO's Data61), Zhenchang Xing (CSIRO's Data61), Qinghua Lu (Data61, CSIRO), Xiwei (Sherry) Xu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** AI for Software Engineering, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029891

**中文总结:** 提出 SeeAction 视觉模型，从录屏中识别 11 种命令、11 种控件并生成位置描述，联合学习实现 UI 操作结构化还原；在 7260 条跨 Word、Firefox 等应用的录屏—动作对上验证有效性与泛化性。

**Abstract:** UI automation is a useful technique for UI testing, bug reproduction and robotic process automation. Recording the user actions with an application assists rapid development of UI automation scripts, but existing recording techniques are intrusive, rely on OS or GUI framework accessibility support or assume specific app implementations. Reversing-engineering user actions from screencasts is non-intrusive, but a key reverse-engineering step is currently missing - recognize human-understandable structured user actions ([command] [widget][location]) from action screencasts. To fill the gap, we propose a deep learning-based computer vision model which can recognize 11 commands and 11 widgets, and generate location phrases from action screencasts, through joint learning and multi-task learning. We label a large dataset with 7260 video-action pairs, which record the user interactions with Word, Zoom, Firefox, Photoshop, and Window 10 Settings. Through extensive experiments, we confirm the effectiveness and generality of our model, and demonstrate the usefulness of a screencast-to-action-script tool built upon our model for bug reproduction.

## 58. Selecting Initial Seeds for Better JVM Fuzzing

**Authors:** Tianchang Gao (Tianjin University), Junjie Chen (Tianjin University), Dong Wang (Tianjin University), Yile Guo (College of Intelligence and Computing, Tianjin University), Yingquan Zhao (Tianjin University), Zan Wang (Tianjin University)

**Categories:** Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029820

**中文总结:** 设计 10 种 JVM fuzz 初始种子选择方法（覆盖、预 fuzz、程序特征等），并在 3 个 JVM 实现上与 JavaTailor、VECT 做系统实证比较。

**Abstract:** JVM fuzzing techniques serve as a cornerstone for guaranteeing the quality of implementations. In typical fuzzing workflows, initial seeds are crucial as they form the basis of the process. Literature in traditional program fuzzing has confirmed that effectiveness is largely impacted by redundancy among initial seeds, thereby proposing a series of seed selection methods. JVM fuzzing, compared to traditional ones, presents unique characteristics, including large-scale and intricate code, and programs with both syntactic and semantic features. However, it remains unclear whether the existing initial seed selection methods are suitable for JVM fuzzing and whether utilizing program features can enhance effectiveness. To address this, we devised a total of 10 initial seed selection methods, comprising coverage-based, prefuzz-based, and program-feature-based methods. We then conducted an empirical study on three JVM implementations to extensively evaluate the performance of the initial seed selection methods within two state-of-the-art fuzzing techniques (JavaTailor and VECT). Specifically, we examine performance from three aspects: (i) effectiveness and efficiency using widely studied initial seeds, (ii) effectiveness using the programs in the wild, and (iii) the ability to detect new bugs. Evaluation results first show that the program-feature-based method that utilizes the control flow graph not only has a significantly lower time overhead (i.e., 30s), but also outperforms other methods, achieving 142% to 269% improvement compared to the full set of initial seeds. Second, results reveal that the initial seed selection greatly improves the quality of wild programs and exhibits complementary effectiveness by detecting new behaviors. Third, results demonstrate that given the same testing period, initial seed selection improves the JVM fuzzing techniques by detecting more unknown bugs. Particularly, 16 out of the 25 detected bugs have been confirmed or fixed by developers. This work takes the first look at initial seed selection in JVM fuzzing, confirming its importance in fuzzing effectiveness and efficiency.

## 59. Synthesizing Document Database Queries using Collection Abstractions

**Authors:** Qikang Liu (Simon Fraser University), Yang He (Simon Fraser University), Yanwen Cai (Simon Fraser University), Byeongguk Kwak (Simon Fraser University), Yuepeng Wang (Simon Fraser University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029877

**中文总结:** 提出面向文档数据库的查询合成方法，通过代数式 DSL 与集合抽象剪枝搜索空间，从少量输入输出示例自动生成查询；在 110 个基准中成功合成 108 个，平均耗时数十秒。

**Abstract:** Document databases are increasingly popular in various applications, but their queries are challenging to write due to the flexible and complex data model underlying document databases. This paper presents a synthesis technique that aims to generate document database queries from input-output examples automatically. A new domain-specific language is designed to express a representative set of document database queries in an algebraic style. Furthermore, the synthesis technique leverages a novel abstraction of collections for deduction to efficiently prune the search space and quickly generate the target query. An evaluation of 110 benchmarks from various sources shows that the proposed technique can synthesize 108 benchmarks successfully. On average, the synthesizer can generate document database queries from a small number of input-output examples within tens of seconds.

## 60. Test Intention Guided LLM-based Unit Test Generation

**Authors:** Zifan Nan (Huawei), Zhaoqiang Guo (Software Engineering Application Technology Lab, Huawei, China), Kui Liu (Huawei), Xin Xia (Huawei)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029762

**中文总结:** 提出 IntUT，以显式测试意图（输入、mock 行为、期望结果）引导 LLM 生成单元测试；分支覆盖率提升 94%，行覆盖率提升 49%。

**Abstract:** The emergence of Large Language Models (LLMs) has accelerated the progress of intelligent software engineering technologies, which brings promising possibility for unit test generation. However, existing approaches on unit tests directly generated from Large Language Models (LLMs) often prove impractical due to their low coverage and insufficient mocking capabilities. This paper proposes IntUT, a novel approach that utilizes explicit test intentions (e.g. test inputs, mock behaviors, and expected results) to effectively guide the LLM to generate high-quality test cases. Our experimental results on three industry Java projects and live study demonstrate that prompting LLM with test intention can generate high-quality test cases for developers. Specifically, it achieves the improvements on branch coverage by 94% and line coverage by 49%. Eventually, we obtain developers' feedback on using IntUT to generate cases for 3 newly Java projects with over 80% line coverage and 30% efficiency improvement on writing unit test cases.

## 61. Testing and Understanding Deviation Behaviors in FHE-hardened Machine Learning Models

**Authors:** Yiteng Peng (Hong Kong University of Science and Technology), Daoyuan Wu (Hong Kong University of Science and Technology), Zhibo Liu (Hong Kong University of Science and Technology), Dongwei Xiao (Hong Kong University of Science and Technology), Zhenlan Ji (The Hong Kong University of Science and Technology), Juergen Rahmel (HSBC), Shuai Wang (Hong Kong University of Science and Technology)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029814

**中文总结:** 提出 HEDiff 差分测试工具，以明文模型的 margin 指标引导在全同态加密加固 ML 模型上定向搜索偏差触发输入，系统揭示 FHE 模型与明文模型输出不一致的偏差行为。

**Abstract:** Fully homomorphic encryption (FHE) is a promising cryptographic primitive that enables secure computation over encrypted data. A primary use of FHE is to support privacy-preserving machine learning (ML) on public cloud infrastructures. Despite the rapid development of FHE-based ML (or HE-ML) in recent years, the community still lacks a systematic understanding of their robustness. In this paper, we aim to systematically test and understand the deviation behaviors of HE-ML models, where the same input causes deviant outputs between FHE-hardened models and their plaintext versions, leading to completely incorrect model predictions. To effectively uncover deviation-triggering inputs under the constraints of expensive FHE computation, we design a novel differential testing tool called HEDiff, which leverages the margin metric on the plaintext model as guidance to drive targeted testing on FHE models. For the identified deviation inputs, we further analyze them to determine whether they exhibit general noise patterns that are transferable. We evaluate HEDiff using three popular HE-ML frameworks, covering 12 different combinations of models and datasets. HEDiff successfully detected hundreds of deviation inputs across almost every tested FHE framework and model. We also quantitatively show that the identified deviation inputs are (visually) meaningful in comparison to regular inputs. Further schematic analysis reveals the root cause of these deviant inputs and allows us to generalize their noise patterns for more directed testing.

## 62. Thanos: DBMS Bug Detection via Storage Engine Rotation Based Differential Testing

**Authors:** Ying Fu (National University of Defense Technology), Zhiyong Wu (Tsinghua University, China), Yuanliang Zhang (National University of Defense Technology), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Yu Jiang (Tsinghua University), Shanshan Li (National University of Defense Technology), Liao Xiangke (National University of Defense Technology)

**Categories:** Testing and Quality, Architecture and Design

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029942

**中文总结:** 提出 Thanos，通过轮换同一 DBMS 的不同存储引擎构造等价系统做差分测试，在 MySQL、MariaDB、Percona 等广泛测试的数据库上发现缺陷。

**Abstract:** Differential testing is a prevalent strategy for establishing test oracles in automated DBMS testing. However, meticulously selecting equivalent DBMSs with diverse implementations and compatible input syntax requires huge manual efforts. In this paper, we propose Thanos, a framework that finds DBMS bugs via storage engine rotation based differential testing. Our key insight is that a DBMS with different storage engines must provide consistent basic storage functionalities. Therefore, it’s feasible to construct equivalent DBMSs based on storage engine rotation, ensuring that the same SQL test cases to these equivalent DBMSs yield consistent results. The framework involves four main steps: 1) select the appropriate storage engines; 2) extract equivalence information among the selected storage engines; 3) synthesize feature-orient test cases that ensure the DBMS equivalence; and 4) send test cases to the DBMSs with selected storage engines and compare the results. We evaluate Thanos on three widely used and extensively tested DBMSs, namely MySQL, MariaDB, and Percona against state-of-the-art fuzzers SQLancer, SQLsmith, and Squirrel. Thanos outperforms them on branch coverage by 24%–116%, and also finds many bugs missed by other fuzzers. More importantly, the vendors have confirmed 32 previously unknown bugs found by Thanos, with 29 verified as Critical.

## 63. The Power of Types: Exploring the Impact of Type Checking on Neural Bug Detection in Dynamically Typed Languages

**Authors:** Boqi Chen (McGill University), José Antonio Hernández López (Linköping University), Gunter Mussbacher (McGill University), Daniel Varro (Linköping University / McGill University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029776

**中文总结:** 研究类型检查对 Python 神经缺陷检测器的影响，指出将类型检查器易发现的缺陷纳入训练与评估会扭曲检测器性能估计。

**Abstract:** [Motivation] Automated bug detection in dynamically typed languages such as Python is essential for maintaining code quality. The lack of mandatory type annotations in such languages can lead to errors that are challenging to identify early with traditional static analysis tools. Recent progress in deep neural networks has led to increased use of neural bug detectors. In statically typed languages, a type checker is integrated into the compiler and thus taken into consideration when the neural bug detector is designed for these languages. [Problem] However, prior studies overlook this aspect during the training and testing of neural bug detectors for dynamically typed languages. When an optional type checker is used, assessing existing neural bug detectors on bugs easily detectable by type checkers may impact their performance estimation. Moreover, including these bugs in the training set of neural bug detectors can shift their detection focus toward the wrong type of bugs. [Contribution] We explore the impact of type checking on various neural bug detectors for variable misuse bugs, a common type targeted by neural bug detectors. Existing synthetic and real-world datasets are type-checked to evaluate the prevalence of type-related bugs. Then, we investigate how type-related bugs influence the training and testing of the neural bug detectors. [Findings] Our findings indicate that existing bug detection datasets contain a significant proportion of type-related bugs. Building on this insight, we discover integrating the neural bug detector with a type checker can be beneficial, especially when the code is annotated with types. Further investigation reveals neural bug detectors perform better on type-related bugs than other bugs. Moreover, removing type-related bugs from the training data helps improve neural bug detectors’ ability to identify bugs beyond the scope of type checkers.

## 64. The Same Only Different: On Information Modality for Configuration Performance Analysis

**Authors:** Hongyuan Liang (University of Electronic Science and Technology of China), Yue Huang (University of Electronic Science and Technology of China), Tao Chen (University of Birmingham)

**Categories:** Testing and Quality, Architecture and Design

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029750

**中文总结:** 在 10 个系统、1694 个配置项上实证比较手册与源码两种信息模态在配置性能分析中的作用，澄清二者在不同分析任务中的互补性与局限。

**Abstract:** Configuration in software systems helps to ensure efficient operation and meet diverse user needs. Yet, some, if not all, configuration options have profound implications for the system's performance. Configuration performance analysis, wherein the key is to understand (or infer) the configuration options' relations and their impacts on performance, is crucial. Two major modalities exist that serve as the source information in the analysis: either the manual or source code. However, it remains unclear what roles they play in configuration performance analysis. Much work that relies on manuals claims their benefits of information richness and naturalness; while work that trusts the source code more prefers the structural information provided therein and criticizes the timeliness of manuals. To fill such a gap, in this paper, we conduct an extensive empirical study over 10 systems, covering 1,694 options, 106,798 words in the manual, and 22,859,552 lines-of-code for investigating the usefulness of manual and code in two important tasks of configuration performance analysis, namely performance-sensitive options identification and the associated dependencies extraction. We reveal several new findings and insights, such as it is beneficial to fuse the manual and code modalities for both tasks; the current automated tools that rely on a single modality are far from being practically useful and generally remain incomparable to human analysis. All those pave the way for further advancing configuration performance analysis.

## 65. The Seeds of the FUTURE Sprout from History: Fuzzing for Unveiling Vulnerabilities in Prospective Deep-Learning Libraries

**Authors:** Zhiyuan Li, Jingzheng Wu (Institute of Software, The Chinese Academy of Sciences), Xiang Ling (Institute of Software, Chinese Academy of Sciences), Tianyue Luo (Institute of Software, Chinese Academy of Sciences), ZHIQING RUI (Institute of Software, Chinese Academy of Sciences; University of Chinese Academy of Sciences), Yanjun Wu (Institute of Software, Chinese Academy of Sciences)

**Categories:** AI for Software Engineering, Testing and Quality, Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029791

**中文总结:** 提出 FUTURE 通用深度学习库模糊测试框架，利用已有库历史缺陷信息并微调 LLM 生成针对性 API 序列，面向新兴 DL 库在信息有限时高效发现安全漏洞。

**Abstract:** The widespread application of Large Language Models (LLMs) underscores the importance of Deep Learning (DL) technologies that rely on foundational DL libraries such as PyTorch and TensorFlow. Despite their robust features, these libraries face challenges with scalability and adaptation to rapid advancements in the LLM community. In response, tech giants like Apple and Huawei are developing their own DL libraries to enhance performance, increase scalability, and safeguard intellectual property. Ensuring the security of these libraries is crucial, with fuzzing being a vital solution. However, existing fuzzing frameworks struggle with target flexibility, effectively testing bug-prone API sequences, and leveraging the limited available information in new libraries. To address these limitations, we propose FUTURE, the first universal DL library fuzzing framework tailored for newly introduced and prospective DL libraries. FUTURE leverages historical bug information from existing libraries and fine-tunes LLMs for specialized code generation. This strategy helps identify vulnerabilities in new libraries and uses insights from these libraries to enhance security in existing ones, creating a cycle from history to future and back. To evaluate FUTURE's effectiveness, we conduct comprehensive evaluations on three newly introduced DL libraries. Results demonstrate that FUTURE significantly outperforms existing fuzzers in bug detection, success rate of bug reproduction, validity rate of code generation, and API coverage. Notably, FUTURE has detected 148 bugs across 452 targeted APIs, including 142 previously unknown bugs. Among these, 10 have been assigned CVE IDs. Additionally, FUTURE detects 7 bugs in PyTorch, demonstrating its ability to enhance security in existing libraries in reverse.

## 66. TOGLL: Correct and Strong Test Oracle Generation with LLMs

**Authors:** Soneya Binta Hossain (University of Virginia), Matthew B Dwyer (University of Virginia)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029748

**中文总结:** 大规模评估 LLM 生成测试预言的能力，微调 7 个代码 LLM 与 6 种提示后提出 TOGLL，可生成正确、多样且更强的测试预言以有效发现独特缺陷。

**Abstract:** Test oracles play a crucial role in software testing, enabling effective bug detection. Despite initial promise, neural methods for automated test oracle generation often result in a large number of false positives and weaker test oracles. While LLMs have shown impressive effectiveness in various software engineering tasks, including code generation, test case creation, and bug fixing, there remains a notable absence of large-scale studies exploring their effectiveness in test oracle generation. The question of whether LLMs can address the challenges in effective oracle generation is both compelling and requires thorough investigation. In this research, we present the first comprehensive study to investigate the capabilities of LLMs in generating correct, diverse, and strong test oracles capable of effectively identifying a large number of unique bugs. To this end, we fine-tuned seven code LLMs using six distinct prompts on a large dataset consisting of 110 Java projects. Utilizing the most effective fine- tuned LLM and prompt pair, we introduce TOGLL, a novel LLM-based method for test oracle generation. To investigate the generalizability of TOGLL, we conduct studies on 25 unseen large-scale Java projects. Besides assessing the correctness, we also assess the diversity and strength of the generated oracles. We compare the results against EvoSuite and the state-of-the-art neural method, TOGA. Our findings reveal that TOGLL can produce 3.8 times more correct assertion oracles and 4.9 times more exception oracles. Regarding bug detection effectiveness, TOGLL can detect 1,023 unique mutants that EvoSuite cannot, which is ten times more than what the previous SOTA neural-based method, TOGA, can detect. Additionally, TOGLL significantly outperforms TOGA in detecting real bugs from the Defects4J dataset.

## 67. TopSeed: Learning Seed Selection Strategies for Symbolic Execution from Scratch

**Authors:** Jaehyeok Lee (Sungkyunkwan University), Sooyoung Cha (Sungkyunkwan University)

**Categories:** Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029780

**中文总结:** 提出 TopSeed，通过在线学习从符号执行交互中自动筛选最优种子，在 17 个开源 C 程序上显著提升符号执行效果。

**Abstract:** We present TopSeed, a new approach that automatically selects optimal seeds to enhance symbolic execution. Recently, the performance of symbolic execution has significantly improved through various state-of-the-art techniques, including search strategies and state-pruning heuristics. However, these techniques have typically demonstrated their effectiveness without considering “seeding”, which efficiently initializes program states for exploration. This paper aims to select valuable seeds from candidate inputs generated during interactions with any symbolic execution technique, without the need for a predefined seed corpus, thereby maximizing the technique’s effectiveness. One major challenge is the vast number of candidates, making it difficult to identify promising seeds. To address this, we introduce a customized online learning algorithm that iteratively groups candidate inputs, ranks each group, and selects a seed from the top-ranked group based on data accumulated during symbolic execution. Experimental results on 17 open-source C programs show that TopSeed significantly enhances four distinct cutting-edge techniques, implemented on top of two symbolic executors, in terms of branch coverage and bug-finding abilities.

## 68. Toward a Better Understanding of Probabilistic Delta Debugging

**Authors:** Mengxiao Zhang, Zhenyang Xu (University of Waterloo), Yongqiang Tian, Xinru Cheng (University of Waterloo), Chengnian Sun (University of Waterloo)

**Categories:** Testing and Quality, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029925

**中文总结:** 首次对概率 Delta Debugging 算法 ProbDD 做深入理论分析，简化其概率模型并阐明概率与子集规模变化趋势，辅以成功率、消融与权衡实验验证其优势与局限。

**Abstract:** Given a list L of elements and a property ψ that L exhibits, ddmin is a classic test input minimization algorithm that aims to automatically remove ψ-irrelevant elements from L. This algorithm has been widely adopted in domains such as test input minimization and software debloating. Recently, ProbDD, a variant of ddmin, has been proposed and achieved stateof- the-art performance. By employing Bayesian optimization, ProbDD estimates the probability of each element in L being relevant to ψ, and statistically decides which and how many elements should be deleted together each time. However, the theoretical probabilistic model of ProbDD is rather intricate, and the underlying details for the superior performance of ProbDD have not been adequately explored. In this paper, we conduct the first in-depth theoretical analysis of ProbDD, clarifying the trends in probability and subset size changes and simplifying the probability model. We complement this analysis with empirical experiments, including success rate analysis, ablation studies, and examinations of trade-offs and limitations, to further comprehend and demystify this state-of- the-art algorithm. Our success rate analysis reveals how ProbDD effectively addresses bottlenecks that slow down ddmin by skipping inefficient queries that attempt to delete complements of subsets and previously tried subsets. The ablation study illustrates that randomness in ProbDD has no significant impact on efficiency. These findings provide valuable insights for future research and applications of test input minimization algorithms. Based on the findings above, we propose CDD, a simplified version of ProbDD, reducing the complexity in both theory and implementation. CDD assists in 1 validating the correctness of our key findings, e.g., that probabilities in ProbDD essentially serve as monotonically increasing counters for each element, and 2 identifying the main factors that truly contribute to ProbDD’s superior performance. Our comprehensive evaluations across 76 benchmarks in test input minimization and software debloating demonstrate that CDD can achieve the same performance as ProbDD, despite being much simplified.

## 69. Towards High-strength Combinatorial Interaction Testing for Highly Configurable Software Systems

**Authors:** Chuan Luo (Beihang University), Shuangyu Lyu (Beihang University), Wei Wu (Central South University; Xiangjiang Laboratory), Hongyu Zhang (Chongqing University), Dianhui Chu (Harbin Institute of Technology), Chunming Hu (Beihang University)

**Categories:** Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029736

**中文总结:** 针对 4-wise/5-wise 组合交互测试覆盖数组生成的高强度挑战，提出局部搜索算法 HSCA 及三项新策略，显著提升高强度 CCAG 问题的求解效率与效果。

**Abstract:** Highly configurable software systems are crucial in practice to satisfy the rising demand for software customization, and combinatorial interaction testing (CIT) is an important methodology for testing such systems. Constrained covering array generation (CCAG), as the core problem in CIT, is to construct a t-wise covering array (CA) of minimum size, where t represents the testing strength. Extensive studies have demonstrated that high-strength CIT (e.g., 4-wise and 5-wise CIT) has stronger fault detection capability than low-strength CIT (i.e., 2-wise and 3-wise CIT), and there exist certain critical faults that can be disclosed through high-strength CIT. Although existing CCAG algorithm has exhibited effectiveness in solving the low-strength CCAG problem, they suffer the severe high-strength challenge when solving 4-wise and 5-wise CCAG, which urgently calls for effective solutions to solving 4-wise and 5-wise CCAG problems. To alleviate the high-strength challenge, we propose a novel and effective local search algorithm dubbed HSCA. Particularly, HSCA incorporates three new and powerful techniques, i.e., multi-round CA generation mechanism, dynamic priority assigning technique, and variable grouping strategy, to improve its performance. Extensive experiments on 35 real-world and synthetic instances demonstrate that HSCA can generate significantly smaller 4-wise and 5-wise CAs than existing state-of-the-art CCAG algorithms. More encouragingly, out of all 35 instances, HSCA successfully constructs 4-wise and 5-wise CAs for 11 and 15 instances, respectively, where existing CCAG algorithms fail. Our results indicate that HSCA can effectively mitigate the high-strength challenge.

## 70. TraceFL: Interpretability-Driven Debugging in Federated Learning via Neuron Provenance

**Authors:** Waris Gill (Virginia Tech), Ali Anwar (University of Minnesota), Muhammad Ali Gulzar (Virginia Tech)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029768

**中文总结:** 提出 TraceFL，通过神经元溯源机制在联邦学习中追溯全局模型预测至具体客户端，支持可解释调试与责任定位。

**Abstract:** In Federated Learning, clients train models on local data and send updates to a central server, which aggregates them into a global model using a fusion algorithm. This collaborative yet privacy-preserving training comes at a cost—FL developers face significant challenges in attributing global model predictions to specific clients. Localizing responsible clients is a crucial step towards (a) excluding clients primarily responsible for incorrect predictions and (b) encouraging clients who contributed high quality models to continue participating in the future. Existing ML explainability approaches are inherently inapplicable as they are designed for single-model, centralized training. We introduce TraceFL, a fine-grained neuron provenance capturing mechanism that identifies clients responsible for the global model’s prediction by tracking the flow of information from individual clients to the global model. Since inference on different inputs activates a different set of neurons of the global model, TraceFL dynamically quantifies the significance of the global model’s neurons in a given prediction. It then selectively picks a slice of the most crucial neurons in the global model and maps them to the corresponding neurons in every participating client to determine each client’s contribution, ultimately localizing the responsible client. We evaluate TraceFL on six datasets, including two real-world medical imaging datasets and four neural networks, including advanced models such as GPT. TraceFL achieves 99% accuracy in localizing the responsible client in FL tasks spanning both image and text classification tasks. At a time when state-of-the-art ML debugging approaches are mostly domain-specific (e.g., image classification only), TraceFL is the first technique to enable highly accurate automated reasoning across a wide range of FL applications.

## 71. TransferFuzz: Fuzzing with Historical Trace for Verifying Propagated Vulnerability Code

**Authors:** Siyuan Li (University of Chinese Academy of Sciences & Institute of Information Engineering Chinese Academy of Sciences, China), Yuekang Li (UNSW), Zuxin Chen (Institute of Information Engineering Chinese Academy of Sciences & University of Chinese Academy of Sciences, China), Chaopeng Dong (Institute of Information Engineering Chinese Academy of Sciences & University of Chinese Academy of Sciences, China), Yongpan Wang (University of Chinese Academy of Sciences & Institute of Information Engineering Chinese Academy of Sciences, China), Hong Li (Institute of Information Engineering at Chinese Academy of Sciences), Yongle Chen (Taiyuan University of Technology, China), Hongsong Zhu (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Testing and Quality, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029778

**中文总结:** 提出 TransferFuzz，利用 CVE 原始二进制历史执行轨迹引导变异，验证代码复用传播漏洞在新软件中是否可被触发。

**Abstract:** Code reuse in software development frequently facilitates the spread of vulnerabilities, making the scope of affected software in CVE reports imprecise. Traditional methods primarily focus on identifying reused vulnerability code within target software, yet they cannot verify if these vulnerabilities can be triggered in new software contexts. This limitation often results in false positives. In this paper, we introduce TransferFuzz, a novel vulnerability verification framework, to verify whether vulnerabilities propagated through code reuse can be triggered in new software. Innovatively, we collected runtime information during the execution or fuzzing of the basic binary (the vulnerable binary detailed in CVE reports). This process allowed us to extract historical traces, which proved instrumental in guiding the fuzzing process for the target binary (the new binary that reused the vulnerable function). TransferFuzz introduces a unique Key Bytes Guided Mutation strategy and a Nested Simulated Annealing algorithm, which transfers these historical traces to implement trace-guided fuzzing on the target binary, facilitating the accurate and efficient verification of the propagated vulnerability. Our evaluation, conducted on widely recognized datasets, shows that TransferFuzz can quickly validate vulnerabilities previously unverifiable with existing techniques. Its verification speed is 2.5 to 26.2 times faster than existing methods. Moreover, TransferFuzz has proven its effectiveness by expanding the impacted software scope for 15 vulnerabilities listed in CVE reports, increasing the number of affected binaries from 15 to 53. The datasets and source code used in this article are available at https://anonymous.4open.science/r/TransferFuzz-E9B3.

## 72. Treefix: Enabling Execution with a Tree of Prefixes

**Authors:** Beatriz Souza (Universität Stuttgart), Michael Pradel (University of Stuttgart)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029828

**中文总结:** 提出 Treefix，利用 LLM 迭代生成前缀树以启用不完整代码片段的执行，通过执行反馈逐步扩展可执行行数，优于 LExecutor 等学习引导执行方法。

**Abstract:** The ability to execute code is a prerequisite for various dynamic program analyses. Learning-guided execution has been proposed as an approach to enable the execution of arbitrary code snippets by letting a neural model predict likely values for any missing variables. Although state-of-the-art learning-guided execution approaches, such as LExecutor, can enable the execution of a relative high amount of code, they are limited to predicting a restricted set of possible values and do not use any feedback from previous executions to execute even more code. This paper presents Treefix, a novel learning-guided execution approach that leverages LLMs to iteratively create code prefixes that enable the execution of a given code snippet. The approach addresses the problem in a multi-step fashion, where each step uses feedback about the code snippet and its execution to instruct an LLM to improve a previously generated prefix. This process iteratively creates a tree of prefixes, a subset of which is returned to the user as prefixes that maximize the number of executed lines in the code snippet. In our experiments with two datasets of Python code snippets, Treefix achieves 25% and 7% more coverage relative to the current state of the art in learning- guided execution, covering a total of 84% and 82% of all lines in the code snippets.

## 73. Tumbling Down the Rabbit Hole: How do Assisting Exploration Strategies Facilitate Grey-box Fuzzing?

**Authors:** Mingyuan Wu (Southern University of Science and Technology), Jiahong Xiang (Southern University of Science and Technology), Kunqiu Chen (Southern University of Science and Technology), Peng Di (Ant Group & UNSW Sydney), Shin Hwei Tan (Concordia University), Heming Cui (University of Hong Kong), Yuqun Zhang (Southern University of Science and Technology)

**Categories:** Testing and Quality, Program Analysis and Verification

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029740

**中文总结:** 首次全面评估 9 种灰盒 fuzz 辅助探索策略在 21 个真实项目上的效果、通用性与局限，为后续策略设计提供统一基准与洞察。

**Abstract:** Many assisting exploration strategies have been proposed to assist grey-box fuzzers in exploring program states guarded by tight and complex branch conditions such as equality constraints. Although they have shown promising results in their original papers, their evaluations seldom follow equivalent protocols, e.g., they are rarely evaluated on identical benchmarks. Moreover, there is a lack of sufficient investigations on the specifics of the program states explored by these strategies which can obfuscate the future application and development of such strategies. Consequently, there is a pressing need for a comprehensive study of assisting exploration strategies on their effectiveness, versatility, and limitations to enlighten their future development. To this end, we perform the first comprehensive study about the assisting exploration strategies for grey-box fuzzers. Specifically, we first collect nine recent fuzzers representing the mainstream assisting exploration strategies as our studied subjects and 21 real-world projects to form our benchmark suite. After evaluating the subjects on the benchmark suite, we then surprisingly find that the dictionary strategy is the most promising since it not only achieves similar or even slightly better performance over the other studied assisting exploration strategies in terms of exploring program states but also is more practical to be enhanced. Accordingly, we propose CDFUZZ, which generates a customized dictionary for each seed upon the baseline fuzzer AFL to improve over the original dictionary strategy. The evaluation results demonstrate that CDFUZZ increases the edge coverage by 16.1% on average for all benchmark projects over the best performer in our study (i.e., AFL++ with the dictionary strategy). CDFUZZ also successfully exposed 37 previously unknown bugs, with nine confirmed and seven fixed by the corresponding developers.

## 74. WDD: Weighted Delta Debugging

**Authors:** Xintong Zhou (University of Waterloo), Zhenyang Xu (University of Waterloo), Mengxiao Zhang (University of Waterloo), Yongqiang Tian, Chengnian Sun (University of Waterloo)

**Categories:** Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029863

**中文总结:** 提出加权 Delta Debugging（WDD），考虑测试输入片段权重差异以改进 ddmin、ProbDD 等算法在元素大小不均时的分区与删除策略，提升最小化效率与效果。

**Abstract:** Delta Debugging is a widely used family of algorithms (e.g., ddmin and ProbDD) to automatically minimize bug-triggering test inputs, thus to facilitate debugging. It takes a list of elements with each element representing a fragment of the test input, systematically partitions the list at different granularities, identifies and deletes bug-irrelevant partitions. Prior delta debugging algorithms assume there are no differences among the elements in the list, and thus treat them uniformly during partitioning. However, in practice, this assumption usually does not hold, because the size (referred to as weight) of the fragment represented by each element can vary significantly. For example, a single element representing 50% of the test input is much more likely to be bug-relevant than elements representing only 1%. This assumption inevitably impairs the efficiency or even effectiveness of these delta debugging algorithms. This paper proposes Weighted Delta Debugging (WDD), a novel concept to help prior delta debugging algorithms overcome the limitation mentioned above. The key insight of WDD is to assign each element in the list a weight according to its size, and distinguish different elements based on their weights during partitioning. We designed two new minimization algorithms, Wddmin and WProbDD, by applying WDD to ddmin and ProbDD respectively. We extensively evaluated Wddmin and WProbDD in two representative applications, HDD and Perses, on 62 benchmarks across two languages. On average, with Wddmin, HDD and Perses took 51.31% and 7.47% less time to generate 9.12% and 0.96% smaller results than with ddmin, respectively. With WProbDD, HDD and Perses used 11.98% and 9.72% less time to generate 13.40% and 2.20% smaller results than with ProbDD, respectively. The results strongly demonstrate the value of WDD. We firmly believe that WDD opens up a new dimension to improve test input minimization techniques.

## 75. What You See Is What You Get: Attention-based Self-guided Automatic Unit Test Generation

**Authors:** Xin Yin (Zhejiang University), Chao Ni (Zhejiang University), xiaodanxu (College of Computer Science and Technology, Zhejiang university), Xiaohu Yang (Zhejiang University)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029864

**中文总结:** 提出 AUGER 两阶段方法：先用注意力机制预测缺陷倾向，再自引导生成单元测试触发错误，兼顾缺陷检测置信度与测试生成效率。

**Abstract:** Software defects heavily affect software's functionalities and may cause huge losses. Recently, many AI-based approaches have been proposed to detect defects, which can be divided into two categories: software defect prediction and automatic unit test generation. While these approaches have made great progress in software defect detection, they still have several limitations in practical application, including the low confidence of prediction models and the inefficiency of unit testing models. To address these limitations, we propose a WYSIWYG (i.e., What You See Is What You Get) approach: \textbf{A}ttention-based Self-guided Automatic \textbf{U}nit Test \textbf{G}en\textbf{ER}ation (AUGER), which contains two stages: defect detection and error triggering. In the former stage, \toolname first detects the proneness of defects. Then, in the latter stage, it guides to generate unit tests for triggering such an error with the help of critical information obtained by the former stage. To evaluate the effectiveness of \toolname, we conduct a large-scale experiment by comparing with the state-of-the-art (SOTA) approaches on the widely used datasets (i.e., Bears, Bugs.jar, and Defects4J). AUGER makes great improvements by 4.7\% to 35.3\% and 17.7\% to 40.4\% in terms of F1-score and Precision in defect detection, and can trigger 23 to 84 more errors than SOTAs in unit test generation. Besides, we also conduct a further study to verify the generalization in practical usage by collecting a new dataset from real-world projects.

## 76. Your Fix Is My Exploit: Enabling Comprehensive DL Library API Fuzzing with Large Language Models

**Authors:** Kunpeng Zhang (The Hong Kong University of Science and Technology), Shuai Wang (Hong Kong University of Science and Technology), Jitao Han (Central University of Finance and Economics), Xiaogang Zhu (The University of Adelaide), Xian Li (Swinburne University of Technology), Shaohua Wang (Central University of Finance and Economics), Sheng Wen (Swinburne University of Technology)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029835

**中文总结:** 提出基于 LLM 的深度学习库 API 全面模糊测试方法，应对 TensorFlow、PyTorch 等上千 API 与复杂输入/用法模式的测试难题。

**Abstract:** Deep learning (DL) libraries are widely used to form the basis of various AI applications in computer vision, natural language processing, and software engineering domains. Despite their popularity, DL libraries are known to have vulnerabilities, such as buffer overflows, use-after-free, and integer overflows, that can be exploited to compromise the security or effectiveness of the underlying libraries. While traditional fuzzing techniques have been used to find bugs in software, they are not well-suited for DL libraries. In general, the complexity of DL libraries and the diversity of their APIs make it challenging to test them thoroughly. To date, mainstream DL libraries like TensorFlow and PyTorch have featured over 1,000 APIs, and the number of APIs is still growing. Fuzzing all these APIs is a daunting task, especially when considering the complexity of the input data and the diversity of the API usage patterns. Recent advances in large language models (LLMs) have illustrated the high potential of LLMs in understanding and synthesizing human-like code. Despite their high potential, we find that emerging LLM-based fuzzers are less optimal for DL library API fuzzing, given their lack of in-depth knowledge on API input edge cases and inefficiency in generating test inputs. In this paper, we propose DFUZZ, a LLM-driven DL library fuzzing approach. We have two key insights: (1) With high reasoning ability, LLMs can replace human experts to reason edge cases (likely error-triggering inputs) from checks in an API's code, and transfer the extracted knowledge to test other (new or rarely-tested) APIs. (2) With high generation ability, LLMs can synthesize initial test programs with high accuracy that automates API testing. DFUZZ provides LLMs with a novel ''white-box view'' of DL library APIs, and therefore, can leverage LLMs' reasoning and generation abilities to achieve comprehensive fuzzing. Our experimental results on popular DL libraries demonstrate that DFUZZ is able to cover more APIs than SOTA (LLM-based) fuzzers on TensorFlow and PyTorch, respectively. Moreover, DFUZZ successfully detected 37 bugs, with 17 already confirmed as previously unknown bugs.

## 77. µPRL: A Mutation Testing Pipeline for Deep Reinforcement Learning based on Real Faults

**Authors:** Deepak-George Thomas (Tulane University), Matteo Biagiola (Università della Svizzera italiana), Nargiz Humbatova (Università della Svizzera italiana), Mohammad Wardat (Oakland University, USA), Gunel Jahangirova (King's College London), Hridesh Rajan (Tulane University), Paolo Tonella (USI Lugano)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029852

**中文总结:** 提出 µPRL 变异测试流水线，基于仓库挖掘的真实强化学习故障分类设计变异算子；实验表明能有效区分强/弱测试生成器并反馈测试充分性。

**Abstract:** Reinforcement Learning (RL) is increasingly adopted to train agents that can deal with complex sequential tasks, such as driving an autonomous vehicle or controlling a complex environment. Correspondingly, novel approaches are needed to ensure that RL agents have been tested adequately before going to production. Among them, mutation testing is quite promising, especially under the assumption that the injected faults (mutations) mimic the real ones. In this paper, we first describe a taxonomy of real RL faults obtained by repository mining. Then, we present the mutation operators derived from such real faults and implemented in the tool µPRL. Finally, we discuss the experimental results, which show that µPRL is extremely effective at discriminating strong from weak test generators, hence providing useful feedback to developers about the adequacy of the test scenarios generated and executed so far.
