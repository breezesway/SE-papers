# ICSE 2025 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 9 papers

## 1. A Little Goes a Long Way: Tuning Configuration Selection for Continuous Kernel Fuzzing

**Authors:** Sanan Hasanov (University of Central Florida), Stefan Nagy (University of Utah), Paul Gazzillo (University of Central Florida)

**Categories:** Testing and Quality, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029826

**中文总结:** 针对持续内核模糊测试中预定义配置覆盖不足、难以纳入新补丁的问题，提炼连续 fuzz 六项需求并提出配置选择调优方法以提升覆盖。

**Abstract:** The Linux kernel is actively-developed and widely-used. It supports billions of devices of all classes, from high-performance computing to the Internet-of-Things, in part because of its sophisticated configuration system, which automatically tailors the source code according to thousands of user-provided configuration options. Fuzzing has been highly successful at finding kernel bugs, being among the top bug reporters. Since the kernel receives 100s of patches per day, fuzzers run continuously, stopping regularly to rebuild the kernel with the latest changes before restarting fuzzing. But kernel fuzzers currently use predefined configuration settings that, as we show, exclude the majority of new patches from the kernel binary, nullifying the benefits of continuous fuzzing. Unfortunately, state-of-the-art configuration testing techniques are generally ill-suited to the needs of continuous fuzzing, excluding necessary options or requiring too many configuration files to be tractible. We distill down the needs of continuous testing into six properties with the most impact, systematically analyze the space of configuration selection strategies, and provide actionable recommendations. Through our analysis, we discover that continuous fuzzers can improve configuration variety without sacrificing performance. We empirically evaluate our discovery by modifying the configuration selection strategy for syzkaller, the most popular Linux kernel fuzzer, which subsequently found more than twice as many new bugs (35 vs. 13) than with the original configuration file and 12x more (24 vs. 2) when considering only unique bugs---with one security vulnerability being assigned a CVE.

## 2. Constrained LTL Specification Learning from Examples

**Authors:** Changjian Zhang (Carnegie Mellon University), Parv Kapoor (Carnegie Mellon University), Ian Dardik (Carnegie Mellon University), Leyi Cui (Columbia University), Romulo Meira-Goes (The Pennsylvania State University), David Garlan (Carnegie Mellon University), Eunsuk Kang (Carnegie Mellon University)

**Categories:** Program Analysis and Verification, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029727

**中文总结:** 提出约束 LTL 规格学习问题，允许用户在正负轨迹之外指定公式属性约束，扩展时序逻辑规格合成的应用范围与效率。

**Abstract:** Temporal logic specifications play an important role in a wide range of software analysis tasks, such as model checking, automated synthesis, program comprehension, and runtime monitoring. Given a set of positive and negative examples, specified as traces, \emph{LTL learning} is the problem of synthesizing a specification, in \emph{linear temporal logic (LTL)}, that evaluates to true over the positive traces and false over the negative ones. In this paper, we propose a new type of LTL learning problem called \emph{constrained LTL learning}, where the user, in addition to positive and negative examples, is given an option to specify one or more \emph{constraints} over the properties of the LTL formula to be learned. We demonstrate that the ability to specify these additional constraints significantly increases the range of applications for LTL learning, and also allows efficient generation of LTL formulas that satisfy certain desirable properties (such as minimality). We propose an approach for solving the constrained LTL learning problem through an encoding in a first-order relational logic and reduction to an instance of the \emph{maximal satisfiability (MaxSAT)} problem. An experimental evaluation demonstrates that ATLAS, an implementation of our proposed approach, is able to solve new types of learning problems while performing better than or competitively with the state-of-the-art tools in LTL learning.

## 3. Exploring the Robustness of the Effect of EVO on Intention Valuation through Replication

**Authors:** Yesugen Baatartogtokh (University of Massachusetts Amherst), Kaitlyn Cook (Smith College), Alicia M. Grubb (Smith College)

**Categories:** Human and Social Aspects, Requirements and Specifications

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029947

**中文总结:** 对目标建模可视化工具 EVO 进行伪精确复现研究（n=60），检验其对意图评估加速效应的稳健性；即便被试对需求工程熟悉度较低，使用 EVO 仍显著更快完成目标建模决策且未损害质量。

**Abstract:** The development of high-quality software depends on precise and comprehensive requirements that meet the objectives of stakeholders. Goal modeling techniques have been developed to fill this gap by capturing and analyzing stakeholders' needs and allowing them to make trade-off decisions; yet, goal modeling analysis is often difficult for stakeholders to interpret. Recent work found that when subjects are given minimal training on goal modeling and access to a color visualization, called EVO, they are able to use EVO to make goal modeling decisions faster without compromising quality. In this paper, we evaluate the robustness of the empirical evidence for EVO and question the underlying color choices made by the initial designers of EVO. We conduct a pseudo-exact replication ($n = 60$) of the original EVO study, varying the experimental site and the study population. Even in our heterogeneous sample with less a priori familiarity with requirements and goal modeling, we find that individuals using EVO answered the goal-modeling questions significantly faster than those using the control, expanding the external validity of the original results. However, we find some evidence that the chosen color scheme is not intuitive and make recommendations for the goal modeling community.

## 4. FairSense: Long-Term Fairness Analysis of ML-Enabled Systems

**Authors:** Yining She (Carnegie Mellon University), Sumon Biswas (Carnegie Mellon University), Christian Kästner (Carnegie Mellon University), Eunsuk Kang (Carnegie Mellon University)

**Categories:** Software Engineering for AI, Security and Vulnerability, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029915

**中文总结:** 提出仿真框架 FairSense，通过蒙特卡洛仿真与敏感性分析检测机器学习系统在反馈循环下长期运行时的公平性违规。

**Abstract:** Algorithmic fairness of machine learning (ML) models has raised significant concern in the recent years. Many testing, verification, and bias mitigation techniques have been proposed to identify and reduce fairness issues in ML models. The existing methods are *model-centric* and designed to detect fairness issues under *static settings*. However, many ML-enabled systems operate in a dynamic environment where the predictive decisions made by the system *impact* the environment, which in turn affects future decision-making. Such a self-reinforcing *feedback loop* can cause fairness violations in the long term, even if the immediate outcomes are fair. In this paper, we propose a simulation-based framework called FairSense to detect and analyze long-term unfairness in ML-enabled systems. In particular, the framework targets systems with an ML model that is trained over tabular data using supervised learning. Given a fairness requirement, FairSense performs *Monte-Carlo simulation* to enumerate evolution traces for each system configuration. Then, FairSense performs *sensitivity analysis* on the space of system parameters to understand the impact of configuration decisions on long-term fairness of the system. We demonstrate FairSense's potential utility through three real-world case studies: Loan lending, opioids risk scoring, and predictive policing.

## 5. From Bugs to Benefits: Improving User Stories by Leveraging Crowd Knowledge with CrUISE-AC

**Authors:** Stefan Schwedt (Heriot-Watt University, UK), Thomas Ströder (FHDW Mettmann)

**Categories:** AI for Software Engineering, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029950

**中文总结:** 提出 CrUISE-AC，从同领域公开 issue 追踪器挖掘群体知识，自动为用户故事生成非平凡验收标准，减少因需求不完整导致的缺陷。

**Abstract:** Costs for resolving software defects increase exponentially in late stages. Incomplete or ambiguous requirements are one of the biggest sources for defects, since stakeholders might not be able to communicate their needs or fail to share their domain specific knowledge. Combined with insufficient developer experience, teams are prone to constructing incorrect or incomplete features. To prevent this, requirements engineering has to explore knowledge sources beyond stakeholder interviews. Publicly accessible issue trackers for systems within the same application domain hold essential information on identified weaknesses, edge cases, and potential error sources, all documented by actual users. Our research aims at (1) identifying, and (2) leveraging such issues to improve an agile requirements artifact known as a “user story”. We present CrUISE-AC (Crowd and User Informed Suggestion Engine for Acceptance Criteria) as a fully automated method that investigates issues and generates non-trivial additional acceptance criteria for a given user story by employing NLP techniques and an ensemble of LLMs. CrUISE-AC was evaluated by five independent experts in two distinct business domains. Our findings suggest that issue trackers hold valuable information pertinent to requirements engineering. Our evaluation shows that 80–82% of the generated acceptance criteria add relevant requirements to the user stories. Limitations are the dependence on accessible input issues and the fact that we do not check generated criteria for being conflict-free or non-overlapping with criteria from other user stories.

## 6. LiSSA: Toward Generic Traceability Link Recovery through Retrieval-Augmented Generation

**Authors:** Dominik Fuchß (Karlsruhe Institute of Technology (KIT)), Tobias Hey (Karlsruhe Institute of Technology (KIT)), Jan Keim (Karlsruhe Institute of Technology (KIT)), Haoyu Liu (Karlsruhe Institute of Technology (KIT)), Niklas Ewald (Karlsruhe Institute of Technology (KIT)), Tobias Thirolf (Karlsruhe Institute of Technology (KIT)), Anne Koziolek (Karlsruhe Institute of Technology)

**Categories:** AI for Software Engineering, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029919

**中文总结:** 提出 LiSSA 框架，结合 RAG 增强 LLM 实现通用可追溯性链接恢复，在需求-代码、文档-代码等多种任务上验证有效。

**Abstract:** There are a multitude of software artifacts which need to be handled during the development and maintenance of a software system. These artifacts interrelate in multiple, complex ways. Therefore, many software engineering tasks are enabled — and even empowered — by a clear understanding of artifact interrelationships and also by the continued advancement of techniques for automated artifact linking. However, current approaches in automatic Traceability Link Recovery (TLR) target mostly the links between specific sets of artifacts, such as those between requirements and code. Fortunately, recent advancements in Large Language Models (LLMs) can enable TLR approaches to achieve broad applicability. Still, it is a nontrivial problem how to provide the LLMs with the specific information needed to perform TLR. In this paper, we present LiSSA, a framework that harnesses LLM performance and enhances them through Retrieval-Augmented Generation (RAG). We empirically evaluate LiSSA on three different TLR tasks, requirements to code, documentation to code, and architecture documentation to architecture models, and we compare our approach to state-of-the-art approaches. Our results show that the RAG-based approach can significantly outperform the state-of-the-art on the code-related tasks. However, further research is required to improve the performance of RAG-based approaches to be applicable in practice.

## 7. SpecGen: Automated Generation of Formal Program Specifications via Large Language Models

**Authors:** Lezhi Ma (Nanjing University), Shangqing Liu (Nanyang Technological University), Yi Li (Nanyang Technological University), Xiaofei Xie (Singapore Management University), Lei Bu (Nanjing University)

**Categories:** AI for Software Engineering, Program Analysis and Verification, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029962

**中文总结:** 提出 SpecGen，利用 LLM 代码理解能力通过对话式两阶段流程自动生成复杂程序的形式化规范，摆脱对预定义模板与语法的依赖。

**Abstract:** In the software development process, formal program specifications play a crucial role in various stages, including requirement analysis, software testing, and verification. However, manually crafting formal program specifications is rather difficult, making the job time-consuming and labor-intensive. Moreover, it is even more challenging to write specifications that correctly and comprehensively describe the semantics of complex programs. To reduce the burden on software developers, automated specification generation methods have emerged. However, existing methods usually rely on predefined templates or grammar, making them struggle to accurately describe the behavior and functionality of complex real-world programs. To tackle this challenge, we introduce SpecGen, a novel technique for formal program specification generation based on Large Language Models (LLMs). Our key insight is to overcome the limitations of existing methods by leveraging the code comprehension capability of LLMs. The process of SpecGen consists of two phases. The first phase employs a conversational approach that guides the LLM to generate appropriate specifications for a given program, aiming to utilize the ability of LLM to generate high-quality specifications. The second phase, designed for where the LLM fails to generate correct specifications, applies four mutation operators to the model-generated specifications and selects verifiable specifications from the mutated ones through a novel heuristic selection strategy by assigning different weights of variants in an efficient manner. We evaluate SpecGen on two datasets, including the SV-COMP Java category benchmark and a manually constructed dataset containing 120 programs. Experimental results demonstrate that SpecGen succeeds in generating verifiable specifications for 279 out of 385 programs, outperforming the existing LLM-based approaches and conventional specification generation tools like Houdini and Daikon. Further investigations on the quality of generated specifications indicate that SpecGen can comprehensively articulate the behaviors of the input program.

## 8. Unavoidable Boundary Conditions: A Control Perspective on Goal Conflicts

**Authors:** Sebastian Uchitel (Universidad de Buenos Aires / Imperial College), Francisco Cirelli (Universidad de Buenos Aires), Dalal Alrajeh (Imperial College London)

**Categories:** Program Analysis and Verification, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029722

**中文总结:** 从反应式合成视角提出更强「不可避免边界条件」(UBC) 定义以精简需求冲突边界条件，实验显示能显著减少无关条件并关联 unrealizable core 等概念。

**Abstract:** Boundary Conditions (BCs) express situations under which requirements specifications conflict. They are used within a broader conflict management process to produce less idealized specifications. Several approaches have been proposed to identify BCs automatically. Some introduce a prioritization criteria to reduce the number of BCs presented to an engineer. However, identifying the few, relevant boundary conditions remains an open challenge. In this paper, we argue that one of the problems of the state of the art is with the definition of BC itself -- it is too weak. We propose a stronger definition for the few, relevant BCs, which we refer to as Unavoidable Boundary Conditions (UBCs), which utilizes the notion of realizability in reactive synthesis. We show experimentally that UBCs non-trivially reduce the number of conditions produced by existing BC identification techniques. We also relate UBCs to existing concepts in reactive synthesis used to provide feedback for unrealizable specifications (including counter-strategies and unrealizable cores). We then show that UBCs provide a targeted form of feedback for repairing unrealizable specifications.

## 9. User Personas Improve Social Sustainability by Encouraging Software Developers to Deprioritize Antisocial Features

**Authors:** Bimpe Ayoola (Dalhousie University), Miikka Kuutila (Dalhousie University), Rina R. Wehbe (Dalhousie University), Paul Ralph (Dalhousie University)

**Categories:** Human and Social Aspects, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029937

**中文总结:** 通过 79 名学生的随机对照实验评估用户画像与利益相关者地图对功能优先级的影响，发现用户画像能促使开发者降低反社会功能优先级，从而提升软件社会可持续性。

**Abstract:** \textit{Background}: Sustainable software development involves creating software in a manner that meets present goals without undermining our ability to meet future goals. In a software engineering context, sustainability has at least four dimensions: ecological, economic, social, and technical. No interventions for improving social sustainability in software engineering have been tested in rigorous lab-based experiments, and little evidence-based guidance is available. \textit{Objective}: The purpose of this study is to evaluate the effectiveness of two interventions---stakeholder maps and persona models---for improving social sustainability by improving software feature prioritization. \textit{Method}: We conducted a randomized controlled factorial experiment with 79 undergraduate computer science students. Participants were randomly assigned to one of four groups and asked to prioritize a backlog of prosocial, neutral, and antisocial user stories for a shopping mall's digital screen display and facial recognition software. Participants received either persona models, a stakeholder map, both, or neither. We compared the differences in prioritization levels assigned to prosocial and antisocial user stories using Cumulative Link Mixed Model regression. \textit{Results}: Participants who received persona models gave significantly lower priorities to anti-social user stories but no significant difference was evident for pro-social user stories. The effects of the stakeholder map were not significant. The interaction effects were not significant. \textit{Conclusion}: Providing aspiring software professionals with well-crafted persona models causes them to de-prioritize anti-social software features. The impact of persona modelling on sustainable software development therefore warrants further study with more experience professionals. Moreover, the novel methodological strategy of assessing social sustainability behavior through backlog prioritization appears feasible in lab-based settings.
