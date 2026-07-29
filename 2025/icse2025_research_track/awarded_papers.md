# ICSE 2025 Research Track — Awarded Papers

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total: 25 papers

## Award breakdown

| Award | # Papers |
| --- | ---: |
| Award Winner | 25 |
| Best Artifact | 2 |

*Note: a paper may receive more than one award.*

## Papers

## 1. A Test Oracle for Reinforcement Learning Software based on Lyapunov Stability Control Theory

**Authors:** Shiyu Zhang (The Hong Kong Polytechnic University), Haoyang Song (The Hong Kong Polytechnic University), Qixin Wang (The Hong Kong Polytechnic University), Henghua Shen (The Hong Kong Polytechnic University), Yu Pei (The Hong Kong Polytechnic University)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029785

**中文总结:** 基于 Lyapunov 稳定性控制理论为强化学习软件设计测试预言，替代依赖人工专家判断输出正确性的做法。

**Abstract:** Reinforcement Learning (RL) has gained significant attention in recent years. As RL software becomes more complex and infiltrates critical application domains, ensuring its quality and correctness becomes increasingly important. An indispensable aspect of software quality/correctness insurance is testing. However, testing RL software faces unique challenges compared to testing traditional software, due to the difficulty on defining the outputs’ correctness. This leads to the RL test oracle problem. Current approaches to testing RL software often rely on human oracles, i.e. convening human experts to judge the correctness of RL software outputs. This heavily depends on the availability and quality (including the experiences, subjective states, etc.) of the human experts, and cannot be fully automated. In this paper, we propose a novel approach to design test oracles for RL software by leveraging the Lyapunov stability control theory. By incorporating Lyapunov stability concepts to guide RL training, we hypothesize that a correctly implemented RL software shall output an agent that respects Lyapunov stability control theories. Based on this heuristics, we propose a Lyapunov stability control theory based oracle, LPEA(ϑ, θ), for testing RL software. We conduct extensive experiments over representative RL algorithms and RL software bugs to evaluate our proposed oracle. The results show that our proposed oracle can outperform the human oracle in most metrics. Particularly, LPEA(ϑ = 100%, θ = 75%) outperforms the human oracle by 53.6%, 50%, 18.4%, 34.8%, 18.4%, 127.8%, 60.5%, 38.9%, and 31.7% respectively on accuracy, precision, recall, F1 score, true positive rate, true negative rate, false positive rate, false negative rate, and ROC curve’s AUC; and LPEA(ϑ = 100%, θ = 50%) outperforms the human oracle by 48.2%, 47.4%, 10.5%, 29.1%, 10.5%, 127.8%, 60.5%, 22.2%, and 26.0% respectively on these metrics.

## 2. Automated Generation of Accessibility Test Reports from Recorded User Transcripts

**Authors:** Syed Fatiul Huq (University of California, Irvine), Mahan Tafreshipour (University of California at Irvine), Kate Kalcevich (Fable Tech Labs Inc.), Sam Malek (University of California at Irvine)

**Categories:** AI for Software Engineering, Human and Social Aspects

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029798

**中文总结:** 提出 Reca11，利用 GPT-4 等 LLM 从无障碍用户测试录音转写中自动提取可访问性与可用性问题，简化测试报告生成。

**Abstract:** Testing for accessibility is a significant step when developing software, as it ensures that all users, including those with disabilities, can effectively engage with web and mobile applications. While automated tools exist to detect accessibility issues in software, none are as comprehensive and effective as the process of user testing, where testers with various disabilities evaluate the application for accessibility and usability issues. However, user testing is not popular with software developers as it requires conducting lengthy interviews with users and later parsing through large recordings to derive the issues to fix. In this paper, we explore how large language models (LLMs) like GPT 4.0, which have shown promising results in context comprehension and semantic text generation, can mitigate this issue and streamline the user testing process. Our solution, called Reca11, takes in informal transcripts of test recordings and extracts the accessibility and usability issues mentioned by the tester. Our systematic prompt engineering determines the optimal configuration of input, instruction, context and demonstrations for best results. We evaluate Reca11's effectiveness on 36 user testing sessions across three applications. Based on the findings, we investigate the strengths and weaknesses of using LLMs in this space.

## 3. Demystifying and Detecting Cryptographic Defects in Ethereum Smart Contracts

**Authors:** Jiashuo Zhang (Peking University, China), Yiming Shen (Sun Yat-sen University), Jiachi Chen (Sun Yat-sen University), Jianzhong Su (Sun Yat-sen University), Yanlin Wang (Sun Yat-sen University), Ting Chen (University of Electronic Science and Technology of China), Jianbo Gao (Peking University), Zhong Chen

**Categories:** Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029839

**中文总结:** 分析 2406 份真实安全报告归纳 9 类以太坊智能合约密码学缺陷，并提出模糊测试工具 CrySol 自动检测相关缺陷。

**Abstract:** To enhance smart contracts with cryptographic capabilities, Ethereum has officially provided a set of system-level cryptographic APIs, such as ecrecover. These APIs have been utilized in over 10% of Ethereum transactions, motivating developers to implement various on-chain cryptographic tasks, such as digital signatures. However, since developers may not always be cryptographic experts, their ad-hoc and potentially defective implementations could compromise the theoretical guarantees of cryptography, leading to real-world security issues. To mitigate this threat, we conducted the first study aimed at demystifying and detecting cryptographic defects in smart contracts. Through the analysis of 2,406 real-world security reports, we defined nine types of cryptographic defects in smart contracts with detailed descriptions and practical detection patterns. Based on this categorization, we proposed CrySol, a fuzzing-based tool to automate the detection of cryptographic defects in smart contracts. It combines transaction replaying and dynamic taint analysis to extract fine-grained crypto-related semantics and employs crypto-specific strategies to guide the test case generation process. urthermore, we collected a large-scale dataset containing 25,745 real-world crypto-related smart contracts and evaluated CrySol's effectiveness on it. The result demonstrated that CrySol achieves an overall precision of 95.4% and a recall of 91.2%. Notably, CrySol revealed that 5,847 (22.7%) out of 25,745 contracts contain at least one cryptographic defect, highlighting the prevalence of these defects.

## 4. Does GenAI Make Usability Testing Obsolete?

**Authors:** Ali Ebrahimi Pourasad, Walid Maalej (University of Hamburg)

**Categories:** AI for Software Engineering, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029918

**中文总结:** 提出视觉语言模型工具 UX-LLM 预测 iOS 应用可用性问题，精确率 0.61–0.66、召回率 0.35–0.38，尚无法取代传统可用性测试。

**Abstract:** Ensuring usability is crucial for the success of mobile apps. Usability issues can compromise user experience and negatively impact the perceived app quality. This paper presents UX-LLM, a novel tool powered by a Large Vision-Language Model that predicts usability issues in iOS apps. To evaluate the performance of UX-LLM we predicted usability issues in two open-source apps of a medium complexity and asked usability experts to assess the predictions. We also performed traditional usability testing and expert review for both apps and compared the results to those of UX-LLM. UX-LLM demonstrated precision ranging from 0.61 and 0.66 and recall between 0.35 and 0.38, indicating its ability to identify valid usability issues, yet failing to capture the majority of issues. Finally, we conducted a focus group with an app development team of a capstone project developing a transit app for visually impaired persons. The focus group expressed positive perceptions of UX-LLM as it identified unknown usability issues in their app. However, they also raised concerns about its integration into the development workflow, suggesting potential improvements. Our results show that UX-LLM cannot fully replace traditional usability evaluation methods but serves as a valuable supplement particularly for small teams with limited resources, to identify issues in less common user paths, due to its ability to inspect the source code.

## 5. Early Detection of Performance Regressions by Bridging Local Performance Data and Architectural Models

**Authors:** Lizhi Liao (Memorial University of Newfoundland), Simon Eismann (University of Würzburg), Heng Li (Polytechnique Montréal), Cor-Paul Bezemer (University of Alberta), Diego Elias Costa (Concordia University, Canada), André van Hoorn (University of Hamburg, Germany), Weiyi Shang (University of Waterloo)

**Categories:** Testing and Quality, Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029855

**中文总结:** 提出桥接本地性能数据与架构模型的方法，在系统未完全部署前早期检测性能回归，弥补系统级与组件级测试的不足。

**Abstract:** During software development, developers often make numerous modifications to the software to address existing issues or implement new features. However, certain changes may inadvertently have a detrimental impact on the overall system performance. To ensure that the performance of new software releases does not degrade (i.e., absence of performance regressions), existing practices rely on system-level performance testing, such as load testing, or component-level performance testing, such as microbenchmarking, to detect performance regressions. However, performance testing for the entire system is often expensive and time-consuming, posing challenges to adapting to the rapid release cycles common in modern DevOps practices. In addition, system-level performance testing cannot be conducted until the system is fully built and deployed. On the other hand, component-level testing focuses on isolated components, neglecting overall system performance and the impact of system workloads. In this paper, we propose a novel approach to early detection of performance regressions by bridging the local performance data generated by component-level testing and the system-level architectural models. Our approach uses local performance data to identify deviations at the component level, and then propagate these deviations to the architectural model. We then use the architectural model to predict regressions in the performance of the overall system. In an evaluation of our approach on two representative open-source benchmark systems, we show that it can effectively detect end-to-end system performance regressions from local performance deviations with different intensities and under various system workloads. More importantly, our approach can detect regressions as early as in the development phase, in contrast to existing approaches that require the system to be fully built and deployed. Our approach is lightweight and can complement traditional system performance testing when testing resources are scarce.

## 6. Enhancing The Open Network: Definition and Automated Detection of Smart Contract Defects

**Authors:** Hao Song, Teng Li (University of Electronic Science and Technology of China), Jiachi Chen (Sun Yat-sen University), Ting Chen (University of Electronic Science and Technology of China), Beibei Li (Sichuan University), Zhangyan Lin (University of Electronic Science and Technology of China), Yi Lu (BitsLab), Pan Li (MoveBit), Xihan Zhou (TonBit)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029871

**中文总结:** 总结 TON 链 FunC 智能合约 8 类缺陷并定义检测规范，提出静态分析框架 TONScanner，复用 FunC 编译器前端生成 IR/CFG/SSA 以自动检测这些缺陷。

**Abstract:** The Open Network (TON), designed to support Telegram's extensive user base of hundreds of millions, has garnered considerable attention since its launch in 2022. \textit{FunC} is the most popular programming language for writing smart contracts on TON. It is distinguished by a unique syntax compared to other smart contract languages. Despite growing interest, research on the practical defects of TON smart contracts is still in its early stages. In this paper, we summarize eight smart contract defects identified from TON's official blogs and audit reports, each with detailed definitions and code examples. Furthermore, we propose a static analysis framework called TONScanner to facilitate the detection of these defects. Specifically, TONScanner reuses \textit{FunC} compiler's frontend code to transform the \textit{FunC} contract code into \textit{FunC} intermediate representation (IR) in the form of a directed acyclic graph (DAG). Based on this IR, TONScanner constructs a control flow graph (CFG), then transforms it into a static single assignment (SSA) form to simplify further analysis. TONScanner also integrates Data Dependency, Call Graph, Taint Analysis, and Cell Construct, which are specifically tailored for TON blockchain's unique data structures. These components finally facilitate the identification of the eight defects. We evaluate the effectiveness of TONScanner by applying it to 1,640 smart contracts and find a total of 14,995 defects. Through random sampling and manual labeling, we find that TONScanner achieves an overall precision of 97.49%. The results reveal that current TON contracts contain numerous defects, indicating that developers are prone to making errors. TONScanner has proven its ability to accurately identify these defects, thereby aiding in their correction.

## 7. Exploring the Robustness of the Effect of EVO on Intention Valuation through Replication

**Authors:** Yesugen Baatartogtokh (University of Massachusetts Amherst), Kaitlyn Cook (Smith College), Alicia M. Grubb (Smith College)

**Categories:** Human and Social Aspects, Requirements and Specifications

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029947

**中文总结:** 对目标建模可视化工具 EVO 进行伪精确复现研究（n=60），检验其对意图评估加速效应的稳健性；即便被试对需求工程熟悉度较低，使用 EVO 仍显著更快完成目标建模决策且未损害质量。

**Abstract:** The development of high-quality software depends on precise and comprehensive requirements that meet the objectives of stakeholders. Goal modeling techniques have been developed to fill this gap by capturing and analyzing stakeholders' needs and allowing them to make trade-off decisions; yet, goal modeling analysis is often difficult for stakeholders to interpret. Recent work found that when subjects are given minimal training on goal modeling and access to a color visualization, called EVO, they are able to use EVO to make goal modeling decisions faster without compromising quality. In this paper, we evaluate the robustness of the empirical evidence for EVO and question the underlying color choices made by the initial designers of EVO. We conduct a pseudo-exact replication ($n = 60$) of the original EVO study, varying the experimental site and the study population. Even in our heterogeneous sample with less a priori familiarity with requirements and goal modeling, we find that individuals using EVO answered the goal-modeling questions significantly faster than those using the control, expanding the external validity of the original results. However, we find some evidence that the chosen color scheme is not intuitive and make recommendations for the goal modeling community.

## 8. Formally Verified Cloud-Scale Authorization

**Authors:** Aleks Chakarov (Amazon Web Services), Jaco Geldenhuys (Amazon Web Services), Matthew Heck (Amazon Web Services), MIchael Hicks (Amazon), Samuel Huang (Amazon Web Services), Georges-Axel Jaloyan (Amazon Web Services), Anjali Joshi (Amazon), K. Rustan M. Leino (Amazon), Mikael Mayer (Automated Reasoning Group, Amazon Web Services), Sean McLaughlin (Amazon Web Services), Akhilesh Mritunjai (Amazon.com), Clement Pit-Claudel (EPFL), Sorawee Porncharoenwase (Amazon Web Services), Florian Rabe (Amazon Web Services), Marianna Rapoport (Amazon Web Services), Giles Reger (Amazon Web Services), Cody Roux (Amazon Web Services), Neha Rungta (Amazon Web Services), Robin Salkeld (Amazon Web Services), Matthias Schlaipfer (Amazon Web Services), Daniel Schoepe (Amazon), Johanna Schwartzentruber (Amazon Web Services), Serdar Tasiran (Amazon, n.n.), Aaron Tomb (Amazon), Emina Torlak (Amazon Web Services, USA), Jean-Baptiste Tristan (Amazon), Lucas Wagner (Amazon Web Services), Michael Whalen (Amazon Web Services and the University of Minnesota), Remy Willems (Amazon), Tongtong Xiang (Amazon Web Services), Taejoon Byun (University of Minnesota), Joshua M. Cohen (Princeton University), Ruijie Fang (University of Texas at Austin), Junyoung Jang (McGill University), Jakob Rath (TU Wien), Hira Taqdees Syeda, Dominik Wagner (University of Oxford), Yongwei Yuan (Purdue University)

**Categories:** Security and Vulnerability, Evolution and Maintenance, Human and Social Aspects, Architecture and Design

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029876

**中文总结:** 使用 Dafny 形式化验证重建每秒十亿次调用的云级授权引擎，2024 年无事故上线并使客户性能提升三倍。

**Abstract:** All critical systems must evolve to meet the needs of a growing and diversifying user base. But supporting that evolution is challenging at increasing scale: Maintainers must find a way to ensure that each change does only what is intended, and will not inadvertently change behavior for existing users. This paper presents how we addressed this challenge for a cloud-scale authorization engine, invoked 1 billion times per second, by using formal verification. Over a period of four years, we built a new authorization engine, one that behaves functionally the same as its predecessor, using the verification-aware programming language Dafny. We can now confidently deploy enhancements and optimizations while maintaining the highest assurance of both correctness and backward compatibility. We deployed the new engine in 2024 without incident and customers immediately enjoyed a threefold performance improvement. The methodology we followed to build this new engine was not an off-the-shelf application of an existing verification tool, and this paper presents several key insights: 1) Rather than prove correct the existing engine, written in Java, we found it more effective to \emph{write a new engine} in Dafny, a language built for \emph{verification from the ground up}, and then compile the result to Java. 2) To ensure performance, debuggability, and to gain trust from stakeholders, we needed to generate readable, \emph{idiomatic} Java code, essentially a transliteration of the source Dafny. 3) To ensure that the specification matches the system's actual behavior, we performed \emph{extensive differential and shadow testing} throughout the development process, ultimately comparing against $10^{15}$ production samples prior to deployment. Our approach demonstrates how formal verification can be effectively applied to evolve critical legacy software at scale.

## 9. Hetrify: Efficient Verification of Heterogeneous Programs on RISC-V

**Authors:** Yiwei Li (School of Computer, National Univer sity of Defense Technology), Liangze Yin (School of Computer, National Univer sity of Defense Technology), Wei Dong (National University of Defense Technology), Jiaxin Liu (National University of Defense Technology), Yanfeng Hu (School of Computer, National Univer sity of Defense Technology), Shanshan Li (National University of Defense Technology)

**Categories:** Security and Vulnerability, Program Analysis and Verification

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029929

**中文总结:** 提出 Hetrify 异构程序验证方法，将多语言/汇编/闭源库等编译为 RISC-V 二进制后在语义等价保证下转为可验证 C 代码，实现通用异构程序的形式化验证。

**Abstract:** The heterogeneous nature of contemporary software, comprising components like closed-source libraries, embedded assembly snippets, and modules written in multiple programming languages, leads to significant verification challenges. Currently, There are no mature and available methods to effectively address such problems. To bridge this gap, we propose a verification approach capable of effectively verifying heterogeneous programs. This approach is universally applicable. It theoretically supports the verification of any heterogeneous program that can be compiled into binary code, without being constrained by any specific programming language. The approach begins by compiling the entire program or its unverifiable segments into binary format. Under guarantees of semantic equivalence, these binaries are converted into verifiable C code, which can then be verified using existing C verification tools. Based on the RISC-V architecture, we developed the Hetrify tool to implement this verification approach. The tool is supported by rigorous mathematical proofs to ensure operational semantic equivalence between the converted C programs and their original counterparts. To validate our approach, we conducted verification experiments on 130 programs, including 100 assembly programs and 30 large heterogeneous programs with missing critical function source code, demonstrating the effectiveness of our approach.

## 10. Increasing the Effectiveness of Automatically Generated Tests by Improving Class Observability

**Authors:** Geraldine Galindo-Gutierrez (Centro de Investigación en Ciencias Exactas e Ingenierías, Universidad Católica Boliviana), Juan Pablo Sandoval Alcocer (Pontificia Universidad Católica de Chile), Nicolas Jimenez-Fuentes (Pontificia Universidad Católica de Chile), Alexandre Bergel (University of Chile), Gordon Fraser (University of Passau)

**Categories:** Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029845

**中文总结:** 针对 EvoSuite 自动生成测试可观测性不足的问题，通过代码变换与扩展机制提升测试缺陷发现能力。

**Abstract:** Automated unit test generation consists of two complementary challenges: Finding sequences of API calls that exercise the code of a class under test, and finding assertion statements that validate the behaviour of the class during execution. The former challenge is often addressed using meta-heuristic search algorithms optimising tests for code coverage, which are then annotated with regression assertions to address the latter challenge, i.e., assertions that capture the states observed during test generation. While the resulting tests tend to achieve high coverage, their fault finding potential is often inhibited by poor or difficult observability of the codebase. That is, relevant attributes and properties may either not be exposed adequately at all, or only in ways that the test generator is unable to handle. In this paper, we investigate the influence of observability in the context of the EvoSuite search-based Java test generator, which we extend in two complementary ways to study and improve observability: First, we apply a transformation to code under test to expose encapsulated attributes to the test generator; second, we address EvoSuite's limited capability of asserting the state of complex objects. Our evaluation demonstrates that together these observability improvements lead to significantly increased mutation scores, underscoring the importance of considering the class observability in the test generation process.

## 11. Interactive Cross-Language Pointer Analysis for Resolving Native Code in Java Programs

**Authors:** Chenxi Zhang (Nanjing University), Yufei Liang (Nanjing University), Tian Tan (Nanjing University), Chang Xu (Nanjing University), Shuangxiang Kan (UNSW), Yulei Sui (University of New South Wales), Yue Li (Nanjing University)

**Categories:** Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029730

**中文总结:** 提出 JNIFER 首个交互式跨语言指针分析，联合 Java 与 C 指针分析并通过 JNI 函数分析在交互点构建跨语言 points-to 与调用图，评估显示优于现有方法。

**Abstract:** Java offers the Java Native Interface (JNI), which allows programs running in the Java Virtual Machine to invoke and be manipulated by native applications and libraries written in other languages, typically C. While JNI mechanism significantly enhances the Java platform's capabilities, it also presents challenges for static analysis of Java programs due to the complex behaviors introduced by native code. Therefore, effectively resolving the interactions between Java and native code is crucial for static analysis. In this paper, we introduce JNIFER, the first interactive cross-language pointer analysis for resolving native code in Java programs. JNIFER integrates both Java and C pointer analyses, equipped with advanced native call and JNI function analyses, enabling the simultaneous analysis of both Java and native code. During the analysis of cross-language interactions, the two analyzers interact with each other, constructing cross-language points-to relations and call graphs, thereby approximating the runtime behavior at the interaction sites. Our evaluation shows that JNIFER outperforms state-of-the-art approaches in terms of soundness while maintaining high precision and comparable efficiency, as evidenced by extensive experiments on OpenJDK and real-world Java applications.

## 12. Iterative Generation of Adversarial Example for Deep Code Models

**Authors:** Li Huang, Weifeng Sun, Meng Yan (Chongqing University)

**Categories:** Software Engineering for AI, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029806

**中文总结:** 提出 ITGen 黑盒对抗样本生成方法，以位向量表示代码变体并结合失败攻击反馈，用增强贝叶斯优化迭代选取最有希望的变体，缓解局部最优与效率困境。

**Abstract:** Deep code models are vulnerable to adversarial attacks, making it possible for semantically identical inputs to trigger different responses. Current black-box attack methods typically prioritize the impact of identifiers on the model based on custom importance scores or program context and incrementally replace identifiers to generate adversarial examples. However, these methods often fail to fully leverage feedback from failed attacks to guide subsequent attacks, resulting in problems such as local optima bias and efficiency dilemmas. In this paper, we introduce ITGen, a novel black-box adversarial example generation method that iteratively utilizes feedback from failed attacks to refine the generation process. It employs a bitvector-based representation of code variants to mitigate local optima bias. By integrating these bit vectors with feedback from failed attacks, ITGen uses an enhanced Bayesian optimization framework to efficiently predict the most promising code variants, significantly reducing the search space and thus addressing the efficiency dilemma. We conducted experiments on a total of nine deep code models for both understanding and generation tasks, demonstrating ITGen's effectiveness and efficiency, as well as its ability to enhance model robustness through adversarial fine-tuning. For example, on average, ITGen improves the attack success rate by 47.98% and 69.70% over the state-of-the-art techniques (i.e., ALERT and BeamAttack), respectively.

## 13. PacDroid: A Pointer-Analysis-Centric Framework for Security Vulnerabilities in Android Apps

**Authors:** Menglong Chen (Nanjing University), Tian Tan (Nanjing University), Minxue Pan (Nanjing University), Yue Li (Nanjing University)

**Categories:** Security and Vulnerability, Systems, Mobile, and Autonomy

**Awards:** Best Artifact, Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029859

**中文总结:** 提出以指针分析为核心的 Android 静态分析框架 PacDroid，统一处理别名、过程间传播与 ICC 等特性，在精度、速度与鲁棒性上优于 FlowDroid 等主流框架。

**Abstract:** General frameworks such as FlowDroid, IccTA, P/Taint, Amandroid, and DroidSafe have significantly advanced the development of static analysis tools for Android security by providing fundamental facilities for them. However, while these frameworks have been instrumental in fostering progress, they often operate with inherent inefficiencies, such as redundant computations, reliance on separate tools, and unnecessary complexity, which are rarely scrutinized by the analysis tools that depend on them. This paper introduces PacDroid, a new static analysis framework for detecting security vulnerabilities in Android apps. PacDroid employs a simple yet effective pointer-analysis-centric approach that naturally manages alias information, interprocedural value propagation, and all Android features it supports (including ICC, lifecycles, and miscs), in a unified manner. Our extensive evaluation reveals that PacDroid not only outperforms state-of-the-art frameworks in achieving a superior trade-off between soundness and precision (F-measure) but also surpasses them in both analysis speed and robustness; moreover, PacDroid successfully identifies 77 real security vulnerability flows across 23 real-world Android apps that were missed by all other frameworks. With its ease of extension and provision of essential facilities, PacDroid is expected to serve as a foundational framework for various future analysis applications for Android.

## 14. PairSmell: A Novel Perspective Inspecting Software Modular Structure

**Authors:** Chenxing Zhong (Nanjing University), Daniel Feitosa (University of Groningen), Paris Avgeriou (Univ. of Gronningen), Huang Huang (State Grid Nanjing Power Supply Company), Yue Li (Nanjing University), He Zhang (Nanjing University)

**Categories:** Evolution and Maintenance, Architecture and Design

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029796

**中文总结:** 提出 PairSmell 概念，以实体对的模块化关系（应分离或共置）与多工具共识的“适宜关系”对比识别需重构的架构决策；在 20 个 C/C++ 系统上实证评估。

**Abstract:** Enhancing the modular structure of existing systems has attracted substantial research interest, focusing on two main methods: (1) software modularization and (2) identifying design issues (e.g., smells) as refactoring opportunities. However, re-modularization solutions often require extensive modifications to the original modules, and the design issues identified are generally too coarse to guide refactoring strategies. Combining the above two methods, this paper introduces a novel concept, \emph{PairSmell}, which exploits modularization to pinpoint design issues necessitating refactoring. We concentrate on a granular but fundamental aspect of modularity principles---\emph{modular relation (MR)}, i.e., \emph{whether a pair of entities are separated or collocated}. The main assumption is that, if the actual MR of a pair violates its `apt MR', i.e., an MR agreed on by multiple modularization tools (as raters), it can be deemed likely a flawed architectural decision that necessitates further examination. To quantify and evaluate \emph{PairSmell}, we conduct an empirical study on 20 C/C++ and Java projects, using 4 established modularization tools to identify two forms of \emph{PairSmell}: inapt separated pairs $\mathit{InSep}$ and inapt collocated pairs $\mathit{InCol}$. Our study on 260,003 instances reveals that their architectural impacts are substantial: (1) on average, 14.60\% and 20.44\% of software entities are involved in $\mathit{InSep}$ and $\mathit{InCol}$ MRs respectively; (2) $\mathit{InSep}$ pairs are associated with 190\% more co-changes than properly separated pairs, while $\mathit{InCol}$ pairs are associated with 35\% fewer co-changes than properly collocated pairs, both indicating a successful identification of modular structures detrimental to software quality; and (3) both forms of \emph{PairSmell} persist across software evolution. This evidence strongly suggests that \emph{PairSmell} can provide meaningful insights for inspecting modular structure, with the identified issues being both granular and fundamental, making the enhancement of modular design more efficient.

## 15. Rango: Adaptive Retrieval-Augmented Proving for Automated Software Verification

**Authors:** Kyle Thompson (University of California, San Diego), Nuno Saavedra (INESC-ID and IST, University of Lisbon), Pedro Carrott (Imperial College London), Kevin Fisher (University of California San Diego), Alex Sanchez-Stern (University of Massachusetts), Yuriy Brun (University of Massachusetts), João F. Ferreira (INESC-ID and IST, University of Lisbon), Sorin Lerner (University of California at San Diego), Emily First (University of California, San Diego)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029818

**中文总结:** 提出 Coq 自动证明合成工具 Rango，每步检索相关前提与项目内相似证明并自适应微调 LLM 上下文；发布 CoqStoq 数据集，在基准上合成 27.7% 证明，较先前方法多 10%。

**Abstract:** Formal verification using proof assistants, such as Coq, allows for high-quality software. However, the verification process is expensive, requiring significant expertise and manual effort to write proofs. Recent work has explored automating proof synthesis using machine learning, and even more recently, large language models (LLMs), showing that retrieving relevant premises (such as lemmas and definitions) is helpful for these models. We present Rango, a fully automated proof synthesis tool for Coq that uses, not only relevant premises but also similar proofs from the current project. Rango uses retrieval augmentation at every step of the proof to automatically determine which proofs and premises to include in the context of its fine-tuned LLM. In this way, Rango adapts to the project _and_ to the evolving state of the proof. We create a new dataset, CoqStoq, of 2,205 open-source Coq projects from GitHub, which includes both training data and a curated evaluation benchmark of well-maintained projects. On this benchmark, Rango synthesizes 27.7% of the proofs, which is 10% more proofs than prior state-of-the-art tool Tactician. Our evaluation also shows that adding relevant proofs to the context in Rango leads to a 45% increase in the number of theorems proven.

## 16. ROSA: Finding Backdoors with Fuzzing

**Authors:** Dimitri Kokkonis (Université Paris-Saclay, CEA, List), Michaël Marcozzi (Université Paris-Saclay, CEA, List), Emilien Decoux (Université Paris-Saclay, CEA List), Stefano Zacchiroli (LTCI, Télécom Paris, Institut Polytechnique de Paris, Palaiseau, France)

**Categories:** Testing and Quality, Security and Vulnerability

**Awards:** Best Artifact, Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029775

**中文总结:** 提出 ROSA，将 AFL++ 灰盒模糊测试与 metamorphic 测试结合，在运行时检测代码级后门触发行为。

**Abstract:** A code-level backdoor is a hidden access, programmed and concealed within the code of a program. For instance, hard-coded credentials planted in the code of an FTP server would enable maliciously logging into all the deployed instances of this server. Confirmed software supply-chain attacks have led to the injection of backdoors into popular open-source projects, and backdoors have been discovered in various router firmware. Manual code auditing for backdoors is challenging and existing semi-automated approaches can handle only a limited amount of programs and backdoors, while requiring manual reverse-engineering of the audited (binary) program. Graybox fuzzing (automated semi-randomized testing) has grown in popularity due to its success in discovering vulnerabilities and hence stands as a strong candidate for improved backdoor detection. However, current fuzzing knowledge does not offer any means to detect the triggering of a backdoor at runtime. In this work we introduce ROSA, a novel approach (and tool) which combines a state-of-the-art fuzzer (AFL++) with a new metamorphic test oracle, capable of detecting runtime backdoor triggers. To facilitate the evaluation of ROSA, we have created ROSARUM, the first openly available benchmark for assessing the detection of various backdoors in diverse programs. Experimental evaluation shows that ROSA has a level of robustness, speed and automation similar to classical fuzzing. Compared to existing detection tools, it can handle a diversity of backdoors and programs and it does not rely on manually reverse-engineering the fuzzed binary code.

## 17. Search-Based LLMs for Code Optimization

**Authors:** Shuzheng Gao (The Chinese University of Hong Kong), Cuiyun Gao (Harbin Institute of Technology), Wenchao Gu (The Chinese University of Hong Kong), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029800

**中文总结:** 将代码优化建模为搜索问题，提出基于 LLM 的搜索式优化方法，以克服一步生成难以捕获复杂优化策略的局限。

**Abstract:** The code written by developers usually suffers from efficiency problems and contain various performance bugs. These inefficiencies necessitate the research of automated refactoring methods for code optimization. Early research in code optimization employs rule-based methods and focuses on specific inefficiency issues, which are labor-intensive and suffer from the low coverage issue. Recent work regards the task as a sequence generation problem, and resorts to deep learning (DL) techniques such as large language models (LLMs). These methods typically prompt LLMs to directly generate optimized code. Although these methods show state-of-the-art performance, such one-step generation paradigm is hard to achieve an optimal solution. First, complex optimization methods such as combinatorial ones are hard to be captured by LLMs. Second, the one-step generation paradigm poses challenge in precisely infusing the knowledge required for effective code optimization within LLMs, resulting in under-optimized code. To address these problems, we propose to model this task from the search perspective, and propose a search-based LLMs framework named SBLLM that enables iterative refinement and discovery of improved optimization methods. SBLLM synergistically integrate LLMs with evolutionary search and consists of three key components: 1) an execution-based representative sample selection part that evaluates the fitness of each existing optimized code and prioritizes promising ones to pilot the generation of improved code; 2) an adaptive optimization pattern retrieval part that infuses targeted optimization patterns into the model for guiding LLMs towards rectifying and progressively enhancing their optimization methods; and 3) a genetic operator-inspired chain-of-thought prompting part that aids LLMs in combining different optimization methods and generating improved optimization methods. Our evaluation of SBLLM on a dataset of Python and C++ code demonstrates its effectiveness in improving code efficiency. Specifically, the results indicate that SBLLM can improve program execution efficiency by up to 109.59% and consistently outperform all baseline methods by 8.72% ∼ 28.06% and 1.15% ∼ 9.56% with different LLMs in terms of top-5 speedup rate on Python and C++, respectively.

## 18. SeeAction: Towards Reverse Engineering How-What-Where of HCI Actions from Screencasts for UI Automation

**Authors:** Dehai Zhao (CSIRO's Data61), Zhenchang Xing (CSIRO's Data61), Qinghua Lu (Data61, CSIRO), Xiwei (Sherry) Xu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** AI for Software Engineering, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029891

**中文总结:** 提出 SeeAction 视觉模型，从录屏中识别 11 种命令、11 种控件并生成位置描述，联合学习实现 UI 操作结构化还原；在 7260 条跨 Word、Firefox 等应用的录屏—动作对上验证有效性与泛化性。

**Abstract:** UI automation is a useful technique for UI testing, bug reproduction and robotic process automation. Recording the user actions with an application assists rapid development of UI automation scripts, but existing recording techniques are intrusive, rely on OS or GUI framework accessibility support or assume specific app implementations. Reversing-engineering user actions from screencasts is non-intrusive, but a key reverse-engineering step is currently missing - recognize human-understandable structured user actions ([command] [widget][location]) from action screencasts. To fill the gap, we propose a deep learning-based computer vision model which can recognize 11 commands and 11 widgets, and generate location phrases from action screencasts, through joint learning and multi-task learning. We label a large dataset with 7260 video-action pairs, which record the user interactions with Word, Zoom, Firefox, Photoshop, and Window 10 Settings. Through extensive experiments, we confirm the effectiveness and generality of our model, and demonstrate the usefulness of a screencast-to-action-script tool built upon our model for bug reproduction.

## 19. Thanos: DBMS Bug Detection via Storage Engine Rotation Based Differential Testing

**Authors:** Ying Fu (National University of Defense Technology), Zhiyong Wu (Tsinghua University, China), Yuanliang Zhang (National University of Defense Technology), Jie Liang, Jingzhou Fu (School of Software, Tsinghua University), Yu Jiang (Tsinghua University), Shanshan Li (National University of Defense Technology), Liao Xiangke (National University of Defense Technology)

**Categories:** Testing and Quality, Architecture and Design

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029942

**中文总结:** 提出 Thanos，通过轮换同一 DBMS 的不同存储引擎构造等价系统做差分测试，在 MySQL、MariaDB、Percona 等广泛测试的数据库上发现缺陷。

**Abstract:** Differential testing is a prevalent strategy for establishing test oracles in automated DBMS testing. However, meticulously selecting equivalent DBMSs with diverse implementations and compatible input syntax requires huge manual efforts. In this paper, we propose Thanos, a framework that finds DBMS bugs via storage engine rotation based differential testing. Our key insight is that a DBMS with different storage engines must provide consistent basic storage functionalities. Therefore, it’s feasible to construct equivalent DBMSs based on storage engine rotation, ensuring that the same SQL test cases to these equivalent DBMSs yield consistent results. The framework involves four main steps: 1) select the appropriate storage engines; 2) extract equivalence information among the selected storage engines; 3) synthesize feature-orient test cases that ensure the DBMS equivalence; and 4) send test cases to the DBMSs with selected storage engines and compare the results. We evaluate Thanos on three widely used and extensively tested DBMSs, namely MySQL, MariaDB, and Percona against state-of-the-art fuzzers SQLancer, SQLsmith, and Squirrel. Thanos outperforms them on branch coverage by 24%–116%, and also finds many bugs missed by other fuzzers. More importantly, the vendors have confirmed 32 previously unknown bugs found by Thanos, with 29 verified as Critical.

## 20. The Seeds of the FUTURE Sprout from History: Fuzzing for Unveiling Vulnerabilities in Prospective Deep-Learning Libraries

**Authors:** Zhiyuan Li, Jingzheng Wu (Institute of Software, The Chinese Academy of Sciences), Xiang Ling (Institute of Software, Chinese Academy of Sciences), Tianyue Luo (Institute of Software, Chinese Academy of Sciences), ZHIQING RUI (Institute of Software, Chinese Academy of Sciences; University of Chinese Academy of Sciences), Yanjun Wu (Institute of Software, Chinese Academy of Sciences)

**Categories:** AI for Software Engineering, Testing and Quality, Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029791

**中文总结:** 提出 FUTURE 通用深度学习库模糊测试框架，利用已有库历史缺陷信息并微调 LLM 生成针对性 API 序列，面向新兴 DL 库在信息有限时高效发现安全漏洞。

**Abstract:** The widespread application of Large Language Models (LLMs) underscores the importance of Deep Learning (DL) technologies that rely on foundational DL libraries such as PyTorch and TensorFlow. Despite their robust features, these libraries face challenges with scalability and adaptation to rapid advancements in the LLM community. In response, tech giants like Apple and Huawei are developing their own DL libraries to enhance performance, increase scalability, and safeguard intellectual property. Ensuring the security of these libraries is crucial, with fuzzing being a vital solution. However, existing fuzzing frameworks struggle with target flexibility, effectively testing bug-prone API sequences, and leveraging the limited available information in new libraries. To address these limitations, we propose FUTURE, the first universal DL library fuzzing framework tailored for newly introduced and prospective DL libraries. FUTURE leverages historical bug information from existing libraries and fine-tunes LLMs for specialized code generation. This strategy helps identify vulnerabilities in new libraries and uses insights from these libraries to enhance security in existing ones, creating a cycle from history to future and back. To evaluate FUTURE's effectiveness, we conduct comprehensive evaluations on three newly introduced DL libraries. Results demonstrate that FUTURE significantly outperforms existing fuzzers in bug detection, success rate of bug reproduction, validity rate of code generation, and API coverage. Notably, FUTURE has detected 148 bugs across 452 targeted APIs, including 142 previously unknown bugs. Among these, 10 have been assigned CVE IDs. Additionally, FUTURE detects 7 bugs in PyTorch, demonstrating its ability to enhance security in existing libraries in reverse.

## 21. Towards Neural Synthesis for SMT-assisted Proof-Oriented Programming

**Authors:** Saikat Chakraborty (Microsoft Research), Gabriel Ebner (Microsoft Research), Siddharth Bhat (University of Cambridge), Sarah Fakhoury (Microsoft Research), Sakina Fatima (University of Ottawa), Shuvendu K. Lahiri (Microsoft Research), Nikhil Swamy (Microsoft Research)

**Categories:** AI for Software Engineering, Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11030292

**中文总结:** 整理约 60 万行 F* 开源证明代码数据集（约 3.2 万类型导向合成任务）并提供可复现片段校验器，探索 AI 合成 SMT 辅助证明导向程序。

**Abstract:** Proof-oriented programs mix computational content with proofs of program correctness. However, the human effort involved in programming and proving is still substantial, despite the use of Satisfiability Modulo Theories (SMT) solvers to automate proofs in languages such as F*. Seeking to spur research on using AI to automate the construction of proof-oriented programs, we curate a dataset of 600K lines of open-source F* programs and proofs, including software used in production systems ranging from Windows and Linux, to Python and Firefox. Our dataset includes around 32K top-level F* definitions, each representing a type-directed program and proof synthesis problem---producing a definition given a formal specification expressed as an F* type. We provide a program-fragment checker that queries F* to check the correctness of candidate solutions. We believe this is the largest corpus of SMT-assisted program proofs coupled with a reproducible program-fragment checker. Grounded in this dataset, we investigate the use of AI to synthesize programs and their proofs in F*, with promising results. Our main finding in that the performance of fine-tuned smaller language models (such as Phi-2 or StarCoder) compare favorably with large language models (such as GPT-4), at a much lower computational cost. We also identify various type-based retrieval augmentation techniques and find that they boost performance significantly. With detailed error analysis and case studies, we identify potential strengths and weaknesses of models and techniques and suggest directions for future improvements.

## 22. Tumbling Down the Rabbit Hole: How do Assisting Exploration Strategies Facilitate Grey-box Fuzzing?

**Authors:** Mingyuan Wu (Southern University of Science and Technology), Jiahong Xiang (Southern University of Science and Technology), Kunqiu Chen (Southern University of Science and Technology), Peng Di (Ant Group & UNSW Sydney), Shin Hwei Tan (Concordia University), Heming Cui (University of Hong Kong), Yuqun Zhang (Southern University of Science and Technology)

**Categories:** Testing and Quality, Program Analysis and Verification

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029740

**中文总结:** 首次全面评估 9 种灰盒 fuzz 辅助探索策略在 21 个真实项目上的效果、通用性与局限，为后续策略设计提供统一基准与洞察。

**Abstract:** Many assisting exploration strategies have been proposed to assist grey-box fuzzers in exploring program states guarded by tight and complex branch conditions such as equality constraints. Although they have shown promising results in their original papers, their evaluations seldom follow equivalent protocols, e.g., they are rarely evaluated on identical benchmarks. Moreover, there is a lack of sufficient investigations on the specifics of the program states explored by these strategies which can obfuscate the future application and development of such strategies. Consequently, there is a pressing need for a comprehensive study of assisting exploration strategies on their effectiveness, versatility, and limitations to enlighten their future development. To this end, we perform the first comprehensive study about the assisting exploration strategies for grey-box fuzzers. Specifically, we first collect nine recent fuzzers representing the mainstream assisting exploration strategies as our studied subjects and 21 real-world projects to form our benchmark suite. After evaluating the subjects on the benchmark suite, we then surprisingly find that the dictionary strategy is the most promising since it not only achieves similar or even slightly better performance over the other studied assisting exploration strategies in terms of exploring program states but also is more practical to be enhanced. Accordingly, we propose CDFUZZ, which generates a customized dictionary for each seed upon the baseline fuzzer AFL to improve over the original dictionary strategy. The evaluation results demonstrate that CDFUZZ increases the edge coverage by 16.1% on average for all benchmark projects over the best performer in our study (i.e., AFL++ with the dictionary strategy). CDFUZZ also successfully exposed 37 previously unknown bugs, with nine confirmed and seven fixed by the corresponding developers.

## 23. Understanding the Response to Open-Source Dependency Abandonment in the npm Ecosystem

**Authors:** Courtney Miller (Carnegie Mellon University), Mahmoud Jahanshahi (University of Tennessee), Audris Mockus (University of Tennessee), Bogdan Vasilescu (Raj Reddy Associate Professor of Software and Societal Systems, Carnegie Mellon University, USA), Christian Kästner (Carnegie Mellon University)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029865

**中文总结:** 大规模分析 npm 广泛使用包的依赖弃用现象，发现弃用常见、大量下游项目暴露且常未响应；并给出透明度与项目 sunset 实践建议。

**Abstract:** Many developers relying on open-source digital infrastructure expect continuous maintenance, but even the most critical packages can become unmaintained. Despite this, there is little understanding of the prevalence of abandonment of widely-used packages, of subsequent exposure, and of reactions to abandonment in practice, or the factors that influence them. We perform a large-scale quantitative analysis of all widely-used npm packages and find that abandonment is common among them, that abandonment exposes many projects which often do not respond, that responses correlate with other dependency management practices, and that removal is significantly faster when a projects end-of-life status is explicitly stated. We end with recommendations to both researchers and practitioners who are facing dependency abandonment or are sunsetting projects, such as opportunities for low-effort transparency mechanisms to help exposed projects make better, more informed decisions.

## 24. Unseen Horizons: Unveiling the Real Capability of LLM Code Generation Beyond the Familiar

**Authors:** Yuanliang Zhang (National University of Defense Technology), Yifan Xie, Shanshan Li (National University of Defense Technology), Ke Liu, Chong Wang (National University of Defense Technology), Zhouyang Jia (National University of Defense Technology), Xiangbing Huang (National University of Defense Technology), Jie Song (National University of Defense Technology), Chaopeng Luo (National University of Defense Technology), Zhizheng Zheng (National University of Defense Technology), Rulin Xu (National University of Defense Technology), Yitong Liu (National University of Defense Technology), Si Zheng (National University of Defense Technology), Liao Xiangke (National University of Defense Technology)

**Categories:** AI for Software Engineering

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029836

**中文总结:** 提出 Unseen Horizons 评估框架，借鉴代码混淆在 token、AST、语义等多层次变换代码，用 LLM 未见过的代码更客观评估其代码生成真实能力，缓解训练数据泄露与时效性问题。

**Abstract:** Recently, large language models (LLMs) have shown strong potential in code generation tasks. However, there are still gaps before they can be fully applied in actual software development processes. Accurately assessing the code generation capabilities of large language models has become an important basis for evaluating and improving the models. Some existing works have constructed datasets to evaluate the capabilities of these models. However, there are three main gaps to objectively evaluate the real capability of LLMs: the exposure of target code, case timeliness, and dependency availability. The fundamental reason for these gaps is that the code in current datasets may have been exposed during the training phase of LLM, and due to the continuous training and development of LLM, their timeliness has been severely compromised. The key to solve the problem is to, as much as possible, evaluate the LLMs using code that they have not encountered before. Thus, the fundamental idea using in this paper is to draw on the concept of code obfuscation, changing code at different levels while ensuring the functionality and output. To this end, we build a code-obfuscation based benchmark OBFUSEVAL. We first collect 1,354 raw cases from five real-world projects, including function description and code. Then we use three-level strategy (symbol, structure and semantic) to obfuscate descriptions, code and context dependencies. We evaluate four LLMs on OBFUSEVAL and compared the effectiveness of different obfuscation strategy. We use official test suites of these projects to evaluate the generated code. The results show that after obfuscation, the average decrease ratio of test pass rate can up to 62.5\%.

## 25. Unveiling the Energy Vampires: A Methodology for Debugging Software Energy Consumption

**Authors:** Enrique Barba Roque (TU Delft), Luís Cruz (TU Delft), Thomas Durieux (TU Delft)

**Categories:** Human and Social Aspects

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029858

**中文总结:** 提出软件能耗调试方法论以定位能耗热点，并以 Redis 为例发现 Alpine 较 Ubuntu 某些操作多耗 20.2% 电力，根因为 musl 与 glibc 的 memcpy 实现差异。

**Abstract:** Energy consumption in software systems is becoming increasingly important, especially in large-scale deployments. However, debugging energy-related issues remains challenging due to the lack of specialized tools. This paper presents an energy debugging methodology for identifying and isolating energy consumption hotspots in software systems. We demonstrate the methodology's effectiveness through a case study of Redis, a popular in-memory database. Our analysis reveals significant energy consumption differences between Alpine and Ubuntu distributions, with Alpine consuming up to 20.2% more power in certain operations. We trace this difference to the implementation of the `memcpy` function in different C standard libraries (musl vs. glibc). By isolating and benchmarking `memcpy`, we confirm it as the primary cause of the energy discrepancy. Our findings highlight the importance of considering energy efficiency in software dependencies and demonstrate the capability to assist developers in identifying and addressing energy-related issues. This work contributes to the growing field of sustainable software engineering by providing a systematic approach to energy debugging.
