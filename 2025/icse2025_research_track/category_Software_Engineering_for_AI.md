# ICSE 2025 Research Track — Software Engineering for AI

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 34 papers

## 1. A Large-Scale Study of Model Integration in ML-Enabled Software Systems

**Authors:** Yorick Sens (Ruhr University Bochum), Henriette Knopp (Ruhr University Bochum), Sven Peldszus (Ruhr University Bochum), Thorsten Berger (Ruhr University Bochum)

**Categories:** Software Engineering for AI, Architecture and Design

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029853

**中文总结:** 大规模研究 ML 赋能软件系统中的模型集成拓扑与工程实践，揭示多模型组合、维护与复用方面的真实特征与挑战。

**Abstract:** The rise of machine learning (ML) and its embedding in software-intensive systems has drastically changed the engineering of such systems. Traditionally, software engineering focuses on manually created artifacts, such as source code, and the process of creating them, as well as best practices for integrating them, i.e., software architectures. In contrast, the development of ML artifacts, i.e., ML models, comes from data science and focuses on the ML models and their training data. However, to deliver value to end users, these ML models must be integrated with traditional software components, often forming complex topologies. In fact, ML-enabled software can easily incorporate many different ML models. While the challenges and practices of building ML-enabled systems have been studied, little is known about the characteristics of real-world ML-enabled systems, beyond isolated examples. Properly embedding ML models in systems so that they can be easily maintained or reused is far from trivial. To improve development processes and architectures for ML-enabled systems, we need to improve our empirical understanding of these systems. We present the first large-scale study of real-world open-source ML-enabled software systems, covering over 2,928 systems on GitHub. We classified and analyzed them to determine their characteristics, as well as their practices for reusing ML models and related code, and the architecture of these systems. Practitioners and researchers benefit from insights into practices for embedding and integrating ML models, bringing data science and software engineering closer together.

## 2. A Tale of Two DL Cities: When Library Tests Meet Compiler

**Authors:** Qingchao Shen (Tianjin University), Yongqiang Tian, Haoyang Ma (Hong Kong University of Science and Technology), Junjie Chen (Tianjin University), Lili Huang (College of Intelligence and Computing, Tianjin University), Ruifeng Fu (Tianjin University), Shing-Chi Cheung (Hong Kong University of Science and Technology), Zan Wang (Tianjin University)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029788

**中文总结:** 提出 OPERA，将深度学习库测试迁移到编译器模型加载阶段并做测试优先级排序；首次实证研究该知识迁移在 TVM、TensorRT 等前端上的有效性与效率。

**Abstract:** Deep Learning (DL) compilers typically load a DL model and optimize it with intermediate representation. Existing DL compiler testing techniques mainly focus on model optimization stages, but rarely explore bug detection at the model loading stage. Effectively testing the model loading stage requires covering diverse usages of each DL operator from various DL libraries, which shares a common objective with DL library testing, indicating that the embedded knowledge in DL library tests could potentially be beneficial for testing the model loading stage of DL compilers. Thus, we conducted the first empirical study to investigate the effectiveness and efficiency of migrating the knowledge embedded in DL library tests to test the model loading stage. To support the conduct of this study, we develop a technique, called OPERA, consisting of test migration (regarding effectiveness investigation) and test prioritization (regarding efficiency investigation). We considered three sources of tests in DL libraries for migration and used eight frontends from three DL compilers (e.g., TVM, TensorRT, and OpenVINO) for evaluation. The migrated tests with the aid of OPERA detected 170 previously unknown bugs in total, 90 of which have been confirmed/fixed by developers, demonstrating the effectiveness of such the migration-based idea. The test prioritization strategy in OPERA improves testing efficiency with migrated tests by 11.9%~47.4% on average compared to general test prioritization strategies. Finally, we obtained 7 major findings and provided a set of guidelines for future work from this study.

## 3. A Test Oracle for Reinforcement Learning Software based on Lyapunov Stability Control Theory

**Authors:** Shiyu Zhang (The Hong Kong Polytechnic University), Haoyang Song (The Hong Kong Polytechnic University), Qixin Wang (The Hong Kong Polytechnic University), Henghua Shen (The Hong Kong Polytechnic University), Yu Pei (The Hong Kong Polytechnic University)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029785

**中文总结:** 基于 Lyapunov 稳定性控制理论为强化学习软件设计测试预言，替代依赖人工专家判断输出正确性的做法。

**Abstract:** Reinforcement Learning (RL) has gained significant attention in recent years. As RL software becomes more complex and infiltrates critical application domains, ensuring its quality and correctness becomes increasingly important. An indispensable aspect of software quality/correctness insurance is testing. However, testing RL software faces unique challenges compared to testing traditional software, due to the difficulty on defining the outputs’ correctness. This leads to the RL test oracle problem. Current approaches to testing RL software often rely on human oracles, i.e. convening human experts to judge the correctness of RL software outputs. This heavily depends on the availability and quality (including the experiences, subjective states, etc.) of the human experts, and cannot be fully automated. In this paper, we propose a novel approach to design test oracles for RL software by leveraging the Lyapunov stability control theory. By incorporating Lyapunov stability concepts to guide RL training, we hypothesize that a correctly implemented RL software shall output an agent that respects Lyapunov stability control theories. Based on this heuristics, we propose a Lyapunov stability control theory based oracle, LPEA(ϑ, θ), for testing RL software. We conduct extensive experiments over representative RL algorithms and RL software bugs to evaluate our proposed oracle. The results show that our proposed oracle can outperform the human oracle in most metrics. Particularly, LPEA(ϑ = 100%, θ = 75%) outperforms the human oracle by 53.6%, 50%, 18.4%, 34.8%, 18.4%, 127.8%, 60.5%, 38.9%, and 31.7% respectively on accuracy, precision, recall, F1 score, true positive rate, true negative rate, false positive rate, false negative rate, and ROC curve’s AUC; and LPEA(ϑ = 100%, θ = 50%) outperforms the human oracle by 48.2%, 47.4%, 10.5%, 29.1%, 10.5%, 127.8%, 60.5%, 22.2%, and 26.0% respectively on these metrics.

## 4. Answering User Questions about Machine Learning Models through Standardized Model Cards

**Authors:** Tajkia Rahman Toma (University of Alberta), Balreet Grewal (University of Alberta), Cor-Paul Bezemer (University of Alberta)

**Categories:** Software Engineering for AI, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029847

**中文总结:** 分析 Hugging Face 上 11,278 条模型讨论，发现 40.1% 用户问题未获回复，标准化模型卡片可减轻社区答疑负担。

**Abstract:** Reusing pre-trained machine learning models is becoming very popular due to model hubs such as Hugging Face (HF). However, similar to when reusing software, many issues may arise when reusing an ML model. In many cases, users resort to asking questions on discussion forums such as the HF community forum. In this paper, we study how we can reduce the community's workload in answering these questions and increase the likelihood that questions receive a quick answer. We analyze 11,278 discussions from the HF model community that contain user questions about ML models. We focus on the effort spent handling questions, the high-level topics of discussions, and the potential for standardizing responses in model cards based on a model card template. Our findings indicate that there is not much effort involved in responding to user questions, however, 40.1% of the questions remain open without any response. A topic analysis shows that discussions are more centered around technical details on model development and troubleshooting, indicating that more input from model providers is required. We show that 42.5% of the questions could have been answered if the model provider followed a standard model card template for the model card. Based on our analysis, we recommend that model providers add more development-related details on the model's architecture, algorithm, data preprocessing and training code in existing documentation (sub)sections and add new (sub)sections to the template to address common questions about model usage and hardware requirements.

## 5. Are LLMs Correctly Integrated into Software Systems?

**Authors:** Yuchen Shao (East China Normal University), Yuheng Huang (the University of Tokyo), Jiawei Shen (East China Normal University), Lei Ma (The University of Tokyo & University of Alberta), Ting Su (East China Normal University), Chengcheng Wan (East China Normal University)

**Categories:** Software Engineering for AI, Architecture and Design

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029854

**中文总结:** 研究 100 个集成 LLM 与 RAG 的开源应用，识别 18 种集成缺陷模式（77% 应用含三种以上），提出修复指南并构建缺陷库 Hydrangea。

**Abstract:** Large language models (LLMs) provide effective solutions in various application scenarios, with the support of retrieval-augmented generation (RAG). However, developers face challenges in integrating LLM and RAG into software systems, due to lacking interface specifications, various requirements from software context, and complicated system management. In this paper, we have conducted a comprehensive study of 100 open-source applications that incorporate LLMs with RAG support, and identified 18 defect patterns. Our study reveals that 77% of these applications contain more than three types of integration defects that degrade software functionality, efficiency, and security. Guided by our study, we propose systematic guidelines for resolving these defects in software life cycle. We also construct an open-source defect library Hydrangea.

## 6. Automated, Unsupervised, and Auto-parameterized Inference of Data Patterns and Anomaly Detection

**Authors:** Qiaolin Qin (Polytechnique Montréal), Heng Li (Polytechnique Montréal), Ettore Merlo (Polytechnique Montreal), Maxime Lamothe (Polytechnique Montreal)

**Categories:** Software Engineering for AI, Security and Vulnerability, Mining Software Repositories

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029754

**中文总结:** 提出 RIOLU，无需标注与人工参数配置即可从未清洗数据自动推断正则数据模式并检测异常，在多领域数据集上 F1 达 97.2%，优于现有方法。

**Abstract:** With the advent of data-centric and machine learning (ML) systems, data quality is playing an increasingly critical role for ensuring the overall quality of software systems. Alas, data preparation, an essential step towards high data quality, is known to be a highly effort-intensive process. Although prior studies have dealt with one of the most impacting issues, data pattern violations, we observe that these studies usually require data-specific configurations (i.e., parameterized) or a certain set of fully curated data as learning examples (i.e., supervised). Both approaches require domain knowledge and depend on users' deep understanding of their data, and are often effort-intensive. In this paper, we introduce RIOLU: Regex Inferencer autO-parameterized Learning with Uncleaned data. RIOLU is fully automated, is automatically parameterized, and does not need labeled samples. We observe that RIOLU can generate precise patterns from datasets in various domains, with a high F1 score of 97.2%, exceeding the state-of-the-art baseline. In addition, according to our experiment on five datasets with anomalies, RIOLU can automatically estimate a data column's error rate, draw normal patterns, and predict anomalies from unlabeled data with higher performance (up to 800.4% improvement in terms of F1) than the state-of-the-art baseline. Furthermore, RIOLU can even outperform ChatGPT in terms of both accuracy (12.3% higher F1) and efficiency (10% less inference time). With user involvement, a variation (a guided version) of RIOLU can further boost its precision (up to 37.4% improvement in terms of F1). Our evaluation in an industrial setting further demonstrates the practical benefits of RIOLU.

## 7. BDefects4NN: A Backdoor Defect Database for Controlled Localization Studies in Neural Networks

**Authors:** Yisong Xiao (Beihang University), Aishan Liu (Beihang University; Institute of Dataspace), Xinwei Zhang (Beihang University), Tianyuan Zhang (Beihang University), Li Tianlin (NTU), Siyuan Liang (National University of Singapore), Xianglong Liu (Beihang University; Institute of Dataspace; Zhongguancun Laboratory), Yang Liu (Nanyang Technological University), Dacheng Tao (Nanyang Technological University)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029765

**中文总结:** 提出 BDefects4NN，首个神经元粒度标注的后门缺陷数据库，支持可控条件下神经网络后门定位研究。

**Abstract:** Pre-trained large deep learning models are now serving as the dominant component for downstream middleware users and have revolutionized the learning paradigm, replacing the traditional approach of training from scratch locally. To reduce development costs, developers often integrate third-party pre-trained deep neural networks (DNNs) into their intelligent software systems. However, utilizing untrusted DNNs presents significant security risks, as these models may contain intentional backdoor defects resulting from the black-box training process. These backdoor defects can be activated by hidden triggers, allowing attackers to maliciously control the model and compromise the overall reliability of the intelligent software. To ensure the safe adoption of DNNs in critical software systems, it is crucial to establish a backdoor defect database for localization studies. This paper addresses this research gap by introducing \emph{BDefects4NN}, the first backdoor defect database, which provides labeled backdoor-defected DNNs at the neuron granularity and enables controlled localization studies of defect root causes. In \emph{BDefects4NN}, we define three defect injection rules and employ four representative backdoor attacks across four popular network architectures and three widely adopted datasets, yielding a comprehensive database of 1,654 backdoor-defected DNNs with four defect quantities and varying infected neurons. Based on \emph{BDefects4NN}, we conduct extensive experiments on evaluating six fault localization criteria and two defect repair techniques, which show limited effectiveness for backdoor defects. Additionally, we investigate backdoor-defected models in practical scenarios, specifically in lane detection for autonomous driving and large language models (LLMs), revealing potential threats and highlighting current limitations in precise defect localization. This paper aims to raise awareness of the threats brought by backdoor defects in our community and inspire future advancements in fault localization methods.

## 8. ChatGPT Inaccuracy Mitigation during Technical Report Understanding: Are We There Yet?

**Authors:** Salma Begum Tamanna (University of Calgary, Canada), Gias Uddin (York University, Canada), Song Wang (York University), Lan Xia (IBM, Canada), Longyu Zhang (IBM, Canada)

**Categories:** Software Engineering for AI, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029792

**中文总结:** 构建 412 组技术报告问答基准，发现 RAG 增强 ChatGPT 仅 36.4% 回答正确；提出 CHIME，用 CFG 解析堆栈跟踪并改进查询验证以缓解技术文本理解幻觉。

**Abstract:** Hallucinations, the tendency to produce irrelevant/incorrect responses, are prevalent concerns in generative AI-based tools like ChatGPT. Although hallucinations in ChatGPT are studied for textual responses, it is unknown how ChatGPT hallucinates for technical texts that contain both textual and technical terms. We surveyed 47 software engineers and produced a benchmark of 412 Q&A pairs from the bug reports of two OSS projects. We find that a RAG-based ChatGPT (i.e., ChatGPT tuned with the benchmark issue reports) is 36.4% correct when producing answers to the questions, due to two reasons 1) limitations to understand complex technical contents in code snippets like stack traces, and 2) limitations to integrate contexts denoted in the technical terms and texts. We present CHIME (ChatGPT Inaccuracy Mitigation Engine) whose underlying principle is that if we can preprocess the technical reports better and guide the query validation process in ChatGPT, we can address the observed limitations. CHIME uses context-free grammar (CFG) to parse stack traces in technical reports. CHIME then verifies and fixes ChatGPT responses by applying metamorphic testing and query transformation. In our benchmark, CHIME shows 30.3% more correction over ChatGPT responses. In a user study, we find that the improved responses with CHIME are considered more useful than those generated from ChatGPT without CHIME

## 9. CodeImprove: Program Adaptation for Deep Code Models

**Authors:** Ravishka Rathnasuriya (University of Texas at Dallas), zijie zhao, Wei Yang (UT Dallas)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11029799

**中文总结:** 提出 CodeImprove，通过输入校验识别超出模型能力的程序，并将越界输入适配为模型可处理输入，避免频繁重训代码深度学习模型。

**Abstract:** Leveraging deep learning (DL)-based code analysis tools to solve software engineering tasks is becoming increasingly popular. Code models often suffer performance degradation due to various reasons (e.g., code data shifts). Retraining is often required to address these issues, but frequent model updates are costly in labeling and deployment. In this paper, we explore an alternative solution: Adapting the program inputs to the code models. This can be achieved by two steps: 1) input validation that focuses on identifying whether an input is an out-of-scope input program that are beyond a model’s handling capability, and 2) input adaptation that adapts out-of-scope inputs to become in-scope inputs. Validating program input is challenging, as current techniques focus on continuous inputs such as image data and fail with discrete inputs like code data, which have unique characteristics and are processed differently by deep learning models. Adapting out-of-scope programs is also challenging due to their vast search spaces. Therefore, in this paper, we propose CodeImprove, which distinguishes out-of-scope from normal inputs and converts such out-of-scope inputs back to in-scope inputs through program transformation. In particular, we propose a validity score metric to identify out-of-scope inputs and leverage genetics algorithms to apply semantic preserving program transformation to convert out-of-scope inputs to in-scope inputs. Our experimental results show CodeImprove can enhance upto 8.78% of accuracy, and 51.28% of relative improvements in three code models on two SE tasks. Additionally, our input validation is promising in detecting outof-scope inputs (AUC score of 0.924).

## 10. Decictor: Towards Evaluating the Robustness of Decision-Making in Autonomous Driving Systems

**Authors:** Mingfei Cheng (Singapore Management University), Xiaofei Xie (Singapore Management University), Yuan Zhou (Zhejiang Sci-Tech University), Junjie Wang (Tianjin University), Guozhu Meng (Institute of Information Engineering, Chinese Academy of Sciences), Kairui Yang (DAMO Academy, Alibaba Group, China)

**Categories:** Software Engineering for AI, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029758

**中文总结:** 提出 Decictor 评估自动驾驶路径规划决策鲁棒性，通过非侵入变异与一致性检查生成使系统做出非最优决策的测试场景。

**Abstract:** Autonomous Driving System (ADS) testing is crucial in ADS development, with the current primary focus being on safety. However, the evaluation of non-safety-critical performance, particularly the ADS’s ability to make optimal decisions and produce optimal paths for autonomous vehicles (AVs), is also vital to ensure the intelligence and reduce risks of AVs. Currently, there is little work dedicated to assessing the robustness of ADSs’ path-planning decisions (PPDs), i.e., whether an ADS can maintain the optimal PPD after an insignificant change in the environment. The key challenges include the lack of clear oracles for assessing PPD optimality and the difficulty in searching for scenarios that lead to non-optimal PPDs. To fill this gap, in this paper, we focus on evaluating the robustness of ADSs’ PPDs and propose the first method, Decictor, for generating non-optimal decision scenarios (NoDSs), where the ADS does not plan optimal paths for AVs. Decictor comprises three main components: Non-invasive Mutation, Consistency Check, and Feedback. To overcome the oracle challenge, Non-invasive Mutation is devised to implement conservative modifications, ensuring the preservation of the original optimal path in the mutated scenarios. Subsequently, the Consistency Check is applied to determine the presence of non-optimal PPDs by comparing the driving paths in the original and mutated scenarios. To deal with the challenge of large environment space, we design Feedback metrics that integrate spatial and temporal dimensions of the AV’s movement. These metrics are crucial for effectively steering the generation of NoDSs. Therefore, Decictor can generate NoDSs by generating new scenarios and then identifying NoDSs in the new scenarios. We evaluate Decictor on Baidu Apollo, an open-source and production-grade ADS. The experimental results validate the effectiveness of Decictor in detecting non-optimal PPDs of ADSs. It generates 63.9 NoDSs in total, while the best-performing baseline only detects 35.4 NoDSs.

## 11. Dissecting Global Search: A Simple yet Effective Method to Boost Individual Discrimination Testing and Repair

**Authors:** Lili Quan (Tianjin University), Li Tianlin (NTU), Xiaofei Xie (Singapore Management University), Zhenpeng Chen (Nanyang Technological University), Sen Chen (Nankai University), Lingxiao Jiang (Singapore Management University), Xiaohong Li (Tianjin University)

**Categories:** Software Engineering for AI

**PDF:** https://ieeexplore.ieee.org/document/11029797

**中文总结:** 发现个体歧视测试中全局搜索阶段是主要瓶颈，提出 GRFT，以遗传算法强化全局搜索，显著提升个体公平性测试与修复效率。

**Abstract:** Deep Learning (DL) has achieved significant success in socially critical decision-making applications but often exhibits unfair behaviors, raising social concerns. Among these unfair behaviors, individual discrimination—examining inequalities between instance pairs with identical profiles differing only in sensitive attributes such as gender, race, and age—is extremely socially impactful. Existing methods have made significant and commendable efforts in testing individual discrimination before deployment. However, their efficiency and effectiveness remain limited, particularly when evaluating relatively fairer models. It remains unclear which phase of the existing testing framework (global or local) is the primary bottleneck limiting performance. Facing the above issues, we first identify that enhancing the global phase consistently improves overall testing effectiveness compared to enhancing the local phase. This motivates us to propose Genetic-Random Fairness Testing (GRFT), an effective and efficient method. In the global phase, we use a genetic algorithm to guide the search for more global discriminatory instances. In the local phase, we apply a light random search to explore the neighbors of these instances, avoiding time-consuming computations. Additionally, based on the fitness score, we also propose a straightforward yet effective repair approach. For a thorough evaluation, we conduct extensive experiments involving 6 testing methods, 5 datasets, 261 models (including 5 naively trained, 64 repaired, and 192 quantized for on-device deployment), and sixteen combinations of sensitive attributes, showing the superior performance of GRFT and our repair method.

## 12. Diversity Drives Fairness: Ensemble of Higher Order Mutants for Intersectional Fairness of Machine Learning Software

**Authors:** Zhenpeng Chen (Nanyang Technological University), Xinyue Li (Peking University), Jie M. Zhang (King's College London), Federica Sarro (University College London), Yang Liu (Nanyang Technological University)

**Categories:** Software Engineering for AI, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029827

**中文总结:** 提出 FairHOME，在推理阶段对输入做高阶变异并集成同一模型预测以提升交叉公平性，在 24 项决策任务上优于六种先进方法。

**Abstract:** Intersectional fairness is a critical requirement for Machine Learning (ML) software, demanding fairness across subgroups defined by multiple protected attributes. This paper introduces FairHOME, a novel ensemble approach using higher order mutation of inputs to enhance intersectional fairness of ML software during the inference phase. Inspired by social science theories highlighting the benefits of diversity, FairHOME generates mutants representing diverse subgroups for each input instance, thus broadening the array of perspectives to foster a fairer decision-making process. Unlike conventional ensemble methods that combine predictions made by different models, FairHOME combines predictions for the original input and its mutants, all generated by the same ML model, to reach a final decision. Notably, FairHOME is even applicable to deployed ML software as it bypasses the need for training new models. We extensively evaluate FairHOME against six state-of-the-art fairness improvement methods across 24 decision-making tasks using widely adopted metrics. FairHOME consistently outperforms existing methods across all metrics considered. On average, it enhances intersectional fairness by 47.3%, surpassing the currently best-performing method by 10.1 percentage points.

## 13. Fairness Testing through Extreme Value Theory

**Authors:** Verya Monjezi (University of Texas at El Paso), Ashutosh Trivedi (University of Colorado Boulder), Vladik Kreinovich (University of Texas at El Paso), Saeid Tizpaz-Niari (University of Illinois Chicago)

**Categories:** Software Engineering for AI, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029970

**中文总结:** 基于极值理论提出极端反事实歧视（ECD）公平性准则，估计受保护群体在最坏情况下的结果劣势，并结合搜索式测试与生成式 AI 采样分布尾部样本进行公平性测试。

**Abstract:** Data-driven software is increasingly being used as a critical component of automated decision-support systems. Since this class of software learns its logic from historical data, it can encode or amplify discriminatory practices. Previous research on algorithmic fairness has focused on improving “average-case” fairness. On the other hand, fairness at the extreme ends of the spectrum, which often signifies lasting and impactful shifts in societal attitudes, has received significantly less emphasis. Leveraging the statistics of extreme value theory (EVT), we propose a novel fairness criterion called extreme counterfactual discrimination (ECD). This criterion estimates the worst-case amounts of disadvantage in outcomes for individuals solely based on their memberships in a protected group. Utilizing tools from search-based software engineering and generative AI, we present a randomized algorithm that samples a statistically significant set of points from the tail of ML outcome distributions even if the input dataset lacks a sufficient number of relevant samples. We conducted several experiments on four ML models (deep neural networks, logistic regression, and random forests) over 10 socially relevant tasks from the literature on algorithmic fairness. First, we evaluate the generative AI methods and find that they generate sufficient samples to infer valid EVT distribution in 95% of cases. Remarkably, we found that the prevalent bias mitigators reduce the average-case discrimination but increase the worst-case discrimination significantly in 35% of cases. We also observed that even the tail-aware mitigation algorithm MiniMax-Fairness—increased the worst-case discrimination in 30% of cases. We propose a novel ECD-based mitigator that improves fairness in the tail in 90% of cases with no degradation of the average-case discrimination. We hope that the EVT framework serves as a robust tool for evaluating fairness in both average-case and worst-case discrimination.

## 14. FairQuant: Certifying and Quantifying Fairness of Deep Neural Networks

**Authors:** Brian Hyeongseok Kim (University of Southern California), Jingbo Wang (University of Southern California), Chao Wang (University of Southern California)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029755

**中文总结:** 提出 FairQuant，用符号区间抽象与迭代精化形式化认证并量化深度神经网络个体公平性（给出可证公平比例），在 5 个公平数据集上更准确且更可扩展。

**Abstract:** We propose a method for formally certifying and quantifying individual fairness of a deep neural network (DNN). Individual fairness guarantees that any two individuals who are identical except for some protected input attribute (e.g., gender or race) receive the same treatment. While there are existing techniques that provide such a guarantee, they suffer from lack of scalability or accuracy as the size and input dimension of the DNN increase. Our method overcomes this limitation by applying abstraction to a symbolic interval based analysis of the DNN followed by iterative refinement guided by the fairness property. Furthermore, our method lifts the interval based analysis from the conventional qualitative certification to quantitative certification, by computing the percentage of individuals whose classification outputs are provably fair, instead of merely deciding if the DNN is fair. We have implemented our method and evaluated it on deep neural networks trained on five popular fairness research datasets. The experimental results show that our method is not only more accurate than state-of-the-art techniques but also several orders-of-magnitude faster.

## 15. FairSense: Long-Term Fairness Analysis of ML-Enabled Systems

**Authors:** Yining She (Carnegie Mellon University), Sumon Biswas (Carnegie Mellon University), Christian Kästner (Carnegie Mellon University), Eunsuk Kang (Carnegie Mellon University)

**Categories:** Software Engineering for AI, Security and Vulnerability, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029915

**中文总结:** 提出仿真框架 FairSense，通过蒙特卡洛仿真与敏感性分析检测机器学习系统在反馈循环下长期运行时的公平性违规。

**Abstract:** Algorithmic fairness of machine learning (ML) models has raised significant concern in the recent years. Many testing, verification, and bias mitigation techniques have been proposed to identify and reduce fairness issues in ML models. The existing methods are *model-centric* and designed to detect fairness issues under *static settings*. However, many ML-enabled systems operate in a dynamic environment where the predictive decisions made by the system *impact* the environment, which in turn affects future decision-making. Such a self-reinforcing *feedback loop* can cause fairness violations in the long term, even if the immediate outcomes are fair. In this paper, we propose a simulation-based framework called FairSense to detect and analyze long-term unfairness in ML-enabled systems. In particular, the framework targets systems with an ML model that is trained over tabular data using supervised learning. Given a fairness requirement, FairSense performs *Monte-Carlo simulation* to enumerate evolution traces for each system configuration. Then, FairSense performs *sensitivity analysis* on the space of system parameters to understand the impact of configuration decisions on long-term fairness of the system. We demonstrate FairSense's potential utility through three real-world case studies: Loan lending, opioids risk scoring, and predictive policing.

## 16. FixDrive: Automatically Repairing Autonomous Vehicle Driving Behaviour for $0.08 per Violation

**Authors:** Yang Sun (Singapore Management University), Chris Poskitt (Singapore Management University), Kun Wang (Zhejiang University), Jun Sun (Singapore Management University)

**Categories:** Software Engineering for AI, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029921

**中文总结:** 提出 FixDrive，分析近失或违规驾驶记录，用 μDrive 领域语言生成可泛化、可解释的自动驾驶策略修复，单次违规修复成本约 0.08 美元。

**Abstract:** Autonomous Vehicles (AVs) are advancing rapidly, with Level-4 AVs already operating in real-world conditions. Current AVs, however, still lag behind human drivers in adaptability and performance, often exhibiting overly conservative behaviours and occasionally violating traffic laws. Existing solutions, such as runtime enforcement, mitigate this by automatically repairing the AV's planned trajectory at runtime, but such approaches lack transparency and should be a measure of last resort. It would be preferable for AV repairs to generalise beyond specific incidents and to be interpretable for users. In this work, we propose FixDrive, a framework that analyses driving records from near-misses or law violations to generate AV driving strategy repairs that reduce the chance of such incidents occurring again. These repairs are captured in $\mu$Drive, a high-level domain-specific language for specifying driving behaviours according to event-based triggers. Implemented for the state-of-the-art autonomous driving system Apollo, FixDrive identifies and visualises critical moments from driving records, then uses a Multimodal Large Language Model (MLLM) with zero-shot learning to generate $\mu$Drive programs. We tested FixDrive on various benchmark scenarios, and found that the generated repairs improved the AV's performance with respect to following traffic laws, avoiding collisions, and successfully reaching destinations. Furthermore, the direct costs of repairing an AV---15 minutes of offline analysis and \$0.08 per violation---are reasonable in practice.

## 17. Fixing Large Language Models' Specification Misunderstanding for Better Code Generation

**Authors:** Zhao Tian (Tianjin University), Junjie Chen (Tianjin University), Xiangyu Zhang (Purdue University)

**Categories:** AI for Software Engineering, Software Engineering for AI, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029745

**中文总结:** 提出 μFiX 提示技术，结合思维引导与细粒度反馈修复大语言模型对编程规格的理解偏差以提升代码生成质量。

**Abstract:** Code generation is to automatically generate source code conforming to a given programming specification, which has received extensive attention especially with the development of large language models (LLMs). Due to the inherent difficulty of code generation, the code generated by LLMs may not be aligned with the specification. Although thought-eliciting prompting techniques have been proposed to enhance the code generation performance of LLMs, producing correct understanding for complicated programming problems remains challenging, resulting in unsatisfactory performance. Also, some feedback-based prompting techniques have been proposed to fix incorrect code using error messages produced by test execution. However, when the generated code deviates significantly from the ground truth, they encounter difficulties in improving performance based on such coarse-grained information. In this work, we propose a novel prompting technique, called μFiX, to improve the code generation performance of LLMs by devising both sophisticated thought-eliciting prompting and feedback-based prompting and making the first exploration on their synergy. It first exploits test case analysis to obtain specification understanding and enables a self-improvement process to identify and refine the misunderstanding in the thought-eliciting prompting phase. μFiX further fixes the specification understanding towards the direction reducing the gap between the provided understanding (from the first phase) and the actual understanding implicitly utilized by LLMs for code generation in the feedback-based prompting phase. By improving the understanding with μFiX, the code generation performance of LLMs can be largely improved. Our evaluation on two advanced LLMs (ChatGPT and DeepSeek-Coder) with six widely-used benchmarks by comparing with 15 baselines, demonstrates the effectiveness of μFiX. For example, μFiX outperforms the most effective baseline with an average improvement of 35.62% in terms of Pass@1 across all subjects.

## 18. HIFI: Explaining and Mitigating Algorithmic Bias through the Lens of Game-Theoretic Interactions

**Authors:** Lingfeng Zhang (East China Normal University), Zhaohui Wang (Software Engineering Institute, East China Normal University), Yueling Zhang (East China Normal University), Min Zhang (East China Normal University), Jiangtao Wang (Software Engineering Institute, East China Normal University)

**Categories:** Software Engineering for AI, Security and Vulnerability

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029886

**中文总结:** 从博弈论 Harsanyi 交互视角解码公平性指标中的敏感信息编码机制，提出训练中偏差缓解方法 HIFI，在多种数据集与公平准则上优于现有方法。

**Abstract:** Machine Learning (ML) algorithms are increasingly used in decision-making process across various social-critical domains, but they often somewhat inherit and amplify bias from their training data, leading to unfair and unethical outcomes. This issue highlights the urgent need for effective methods to detect, explain, and mitigate bias to ensure the fairness of ML systems. Previous studies are prone to analyze the root causes of algorithmic bias from a statistical perspective. However, to the best of our knowledge, none of them has discussed how sensitive information inducing the final discriminatory decision is encoded by ML models. In this work, we attempt to explain and mitigate algorithmic bias from a game-theoretic view. We mathematically decode an essential and common component of sensitive information implicitly defined by various fairness metrics with Harsanyi interactions, and on this basis, we propose an in-processing method HIFI for bias mitigation. We conduct an extensive evaluation of HIFI with 11 state-of-the-art methods, 5 real-world datasets, 4 fairness criteria, and 5 ML performance metrics, while also considering intersectional fairness for multiple protected attributes. The results show that HIFI surpasses state-of-the-art in-processing methods in terms of fairness improvement and fairness-performance trade-off, and also achieves notable effectiveness in reducing violations of individual fairness simultaneously.

## 19. Improved Detection and Diagnosis of Faults in Deep Neural Networks Using Hierarchical and Explainable Classification

**Authors:** Sigma Jahan (Dalhousie University), Mehil Shah (Dalhousie University), Parvez Mahbub (Dalhousie University), Masud Rahman (Dalhousie University)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029901

**中文总结:** 提出 DEFault，先以训练期动态特征做层次化故障检测，再结合静态特征与 SHAP 等可解释方法定位 DNN 程序根因，覆盖文献中主要故障类型。

**Abstract:** Deep Neural Networks (DNN) have found numerous applications in various domains, including fraud detection, medical diagnosis, facial recognition, and autonomous driving. However, DNN-based systems often suffer from reliability issues due to their inherent complexity and the stochastic nature of their underlying models. Unfortunately, existing techniques to detect faults in DNN programs are either limited by the types of faults (e.g., hyperparameter or layer) they support or the kind of information (e.g., dynamic or static) they use. As a result, they might fall short of comprehensively detecting and diagnosing the faults. In this paper, we present DEFault (Detect and Explain Fault) -- a novel technique to detect and diagnose faults in DNN programs. It first captures dynamic (i.e., runtime) features during model training and leverages a hierarchical classification approach to detect all major fault categories from the literature. Then, it captures static features (e.g., layer types) from DNN programs and leverages explainable AI methods (e.g., SHAP) to narrow down the root cause of the fault. We train and evaluate DEFault on a large, diverse dataset of ~14.5K DNN programs and further validate our technique using a benchmark dataset of 52 real-life faulty DNN programs. Our approach achieves ~94% recall in detecting real-world faulty DNN programs and ~63% recall in diagnosing the root causes of the faults, demonstrating 3.92%--11.54% higher performance than that of state-of-the-art techniques. Thus, DEFault has the potential to significantly improve the reliability of DNN programs by effectively detecting and diagnosing the faults.

## 20. Iterative Generation of Adversarial Example for Deep Code Models

**Authors:** Li Huang, Weifeng Sun, Meng Yan (Chongqing University)

**Categories:** Software Engineering for AI, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029806

**中文总结:** 提出 ITGen 黑盒对抗样本生成方法，以位向量表示代码变体并结合失败攻击反馈，用增强贝叶斯优化迭代选取最有希望的变体，缓解局部最优与效率困境。

**Abstract:** Deep code models are vulnerable to adversarial attacks, making it possible for semantically identical inputs to trigger different responses. Current black-box attack methods typically prioritize the impact of identifiers on the model based on custom importance scores or program context and incrementally replace identifiers to generate adversarial examples. However, these methods often fail to fully leverage feedback from failed attacks to guide subsequent attacks, resulting in problems such as local optima bias and efficiency dilemmas. In this paper, we introduce ITGen, a novel black-box adversarial example generation method that iteratively utilizes feedback from failed attacks to refine the generation process. It employs a bitvector-based representation of code variants to mitigate local optima bias. By integrating these bit vectors with feedback from failed attacks, ITGen uses an enhanced Bayesian optimization framework to efficiently predict the most promising code variants, significantly reducing the search space and thus addressing the efficiency dilemma. We conducted experiments on a total of nine deep code models for both understanding and generation tasks, demonstrating ITGen's effectiveness and efficiency, as well as its ability to enhance model robustness through adversarial fine-tuning. For example, on average, ITGen improves the attack success rate by 47.98% and 69.70% over the state-of-the-art techniques (i.e., ALERT and BeamAttack), respectively.

## 21. Lightweight Concolic Testing via Path-Condition Synthesis for Deep Learning Libraries

**Authors:** Sehoon Kim, Yonghyeon Kim (UNIST), Dahyeon Park (UNIST), Yuseok Jeon (UNIST), Jooyong Yi (UNIST), Mijung Kim (UNIST)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029909

**中文总结:** 提出首个面向深度学习库的轻量级混合测试：用归纳程序合成近似路径条件替代全符号执行，在可接受开销下更有效探索复杂库的执行路径。

**Abstract:** Many techniques have been recently developed for testing deep learning (DL) libraries, recently. Although these techniques have effectively improved API and code coverage and detected unknown bugs, they rely on black-box fuzzing for input generation. Concolic testing (also known as dynamic symbolic execution) can be more effective in exploring diverse execution paths, but applying it to DL libraries is extremely challenging due to their inherent complexity. In this paper, we introduce the first concolic testing technique for DL libraries. Our technique offers a lightweight approach that significantly reduces the heavy overhead associated with traditional concolic testing. While symbolic execution maintains symbolic expressions for every variable with non-concrete values to build a path condition, our technique computes approximate path conditions by inferring branch conditions via inductive program synthesis. Despite potential imprecision from approximation, our method's light overhead allows for effective exploration of diverse execution paths within the complex implementations of DL libraries. We have implemented our tool, PathFinder, and evaluated it on PyTorch and TensorFlow. Our results show that PathFinder outperforms existing API-level DL library fuzzers by achieving 57\% more branch coverage on average; up to 58\% higher than TitanFuzz and 125\% higher than FreeFuzz. PathFinder is also effective in bug detection, uncovering 61 crash bugs, 59 of which were confirmed by developers as previously unknown, with 32 already fixed.

## 22. MARQ: Engineering Mission-Critical AI-based Software with Automated Result Quality Adaptation

**Authors:** Uwe Gropengießer (Technical University of Darmstadt), Elias Dietz (Technical University of Darmstadt), Florian Brandherm (Technical University of Darmstadt), Achref Doula (Technical University of Darmstadt), Osama Abboud (Munich Research Center, Huawei), Xun Xiao (Munich Research Center, Huawei), Max Mühlhäuser (Technical University of Darmstadt)

**Categories:** Software Engineering for AI, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029961

**中文总结:** 提出 MARQ 框架，支持工程师声明不同结果质量与资源需求的 AI 服务链，并在运行时根据资源约束自动优化切换，适用于边缘与移动等场景。

**Abstract:** AI-based mission-critical software exposes a blessing and a curse: its inherent statistical nature allows for flexibility in result quality, yet the mission-critical importance demands adherence to stringent constraints such as execution deadlines. This creates a space for trade-offs between the Quality of Result (QoR)—a metric that quantifies the quality of a computational outcome—and other application attributes like execution time and energy, particularly in real-time scenarios. Fluctuating resource constraints, such as data transfer to a remote server over unstable network connections, are prevalent in mobile and edge computing environments—encompassing use cases like Vehicle-to-Everything, drone swarms, or social-VR scenarios. We introduce a novel approach that enables software engineers to easily specify alternative AI service chains—sequences of AI services encapsulated in microservices aiming to achieve a predefined goal—with varying QoR and resource requirements. Our methodology facilitates dynamic optimization at runtime, which is automatically driven by the MARQ framework. Our evaluations show that MARQ can be used effectively for the dynamic selection of AI service chains in real-time while maintaining the required application constraints of mission-critical AI software. Notably, our approach achieves a 100x acceleration in service chain selection and an average 10% improvement in QoR compared to existing methods.

## 23. Mock Deep Testing: Toward Separate Development of Data and Models for Deep Learning

**Authors:** Ruchira Manke (Tulane University, USA), Mohammad Wardat (Oakland University, USA), Foutse Khomh (Polytechnique Montréal), Hridesh Rajan (Tulane University)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029789

**中文总结:** 提出 mock 深度测试方法论，通过 mock 数据与 mock 模型解耦数据准备与模型设计，支持深度学习应用组件的独立单元测试与并行开发。

**Abstract:** While deep learning (DL) has permeated, and become an integral component of many critical software systems, today software engineering research hasn’t explored how to separately test data and models that are integral for DL approaches to work effectively. The main challenge in independently testing these components arises from the tight dependency between data and models. This research explores this gap, introducing our methodology of mock deep testing for unit testing of DL applications. To enable unit testing, we introduce a design paradigm that decomposes the workflow into distinct, manageable components, minimizes sequential dependencies, and modularizes key stages of the DL, including data preparation and model design. For unit testing these components, we propose modeling their dependencies using mocks. In the context of DL, mocks refer to mock data and mock model that mimic the behavior of the original data and model, respectively. This modular approach facilitates independent development and testing of the components, ensuring comprehensive quality assurance throughout the development process. We have developed KUnit, a framework for enabling mock deep testing for the Keras library, a popular library for developing DL applications. We empirically evaluated KUnit to determine the effectiveness of mocks in independently testing data and models. Our assessment of 50 DL programs obtained from Stack Overflow and GitHub shows that mocks effectively identified 10 issues in the data preparation stage and 53 issues in the model design stage. We also conducted a user study with 36 participants using KUnit to perceive the effectiveness of our approach. Participants using KUnit successfully resolved 25 issues in the data preparation stage and 38 issues in the model design stage. We also found that mock objects provide a lightweight emulation of the dependencies for unit testing, facilitating early bug detection. Lastly, to evaluate the usability of KUnit, we conducted a post-study survey. The results reveal that KUnit is helpful to DL application developers, enabling them to independently test each component (data and model) and resolve issues effectively in different stages.

## 24. Navigating the Testing of Evolving Deep Learning Systems: An Exploratory Interview Study

**Authors:** Hanmo You (Tianjin University), Zan Wang (Tianjin University), Bin Lin (Hangzhou Dianzi University), Junjie Chen (Tianjin University)

**Categories:** Software Engineering for AI, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029900

**中文总结:** 对 22 名工业界深度学习开发者进行半结构化访谈，探索持续演化 DL 系统的测试挑战、现有应对实践与未来支持需求，总结最佳实践与研究方向。

**Abstract:** Deep Learning (DL) systems have been widely adopted across various industrial domains such as autonomous driving and intelligent healthcare. As with traditional software, DL systems also need to constantly evolve to meet ever-changing user requirements. However, ensuring the quality of these continuously evolving systems presents significant challenges, especially in the context of testing. Understanding how industry developers address these challenges and what extra obstacles they are facing could provide valuable insights for further safeguarding the quality of DL systems. To reach this goal, we conducted semi-structured interviews with 22 DL developers from diverse domains and backgrounds. More specifically, our study focuses on exploring the challenges developers encounter in testing evolving DL systems, the practical solutions they employ, and their expectations for extra support. Our results highlight the difficulties in testing evolving DL systems and identify the best practices for DL developers to address them. Additionally, we pinpoint potential future research directions to enhance testing effectiveness in evolving DL systems.

## 25. On the Mistaken Assumption of Interchangeable Deep Reinforcement Learning Implementations

**Authors:** Rajdeep Singh Hundal (National University of Singapore), Yan Xiao (Sun Yat-sen University), Xiaochun Cao (Sun Yat-Sen University), Jin Song Dong (National University of Singapore), Manuel Rigger (National University of Singapore)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029867

**中文总结:** 通过差分测试揭示同一 DRL 算法（如 DQN、PPO）不同实现存在显著性能差异，挑战其可互换假设并影响既有研究结论的可信度。

**Abstract:** \emph{Deep Reinforcement Learning} (DRL) is a paradigm of artificial intelligence where an \emph{agent} uses a neural network to learn which actions to take in a given \emph{environment}. DRL has recently gained traction from being able to solve complex environments like driving simulators, 3D robotic control, and multiplayer-online-battle-arena video games. Numerous \emph{implementations} of the state-of-the-art algorithms responsible for training these agents, like the \emph{Deep Q-Network} (DQN) and \emph{Proximal Policy Optimization} (PPO) algorithms, currently exist. However, studies make the mistake of assuming implementations of the same algorithm to be consistent and thus, \emph{interchangeable}. In this paper, through a \emph{differential testing} lens, we present the results of studying the extent of implementation inconsistencies, their effect on the implementations' performance, as well as their impact on the conclusions of prior studies under the assumption of interchangeable implementations. The outcome of our differential tests showed significant discrepancies between the tested algorithm implementations, indicating that they are \textit{not} interchangeable. In particular, out of the five PPO implementations tested on 56 games, three implementations achieved superhuman performance for 50\% of their total trials while the other two implementations only achieved superhuman performance for less than 15\% of their total trials. Furthermore, the performance among the high-performing PPO implementations was found to differ significantly in nine games. As part of a meticulous manual analysis of the implementations' source code, we analyzed implementation discrepancies and determined that code-level inconsistencies primarily caused these discrepancies. Lastly, we replicated a study and showed that this assumption of implementation interchangeability was sufficient to \emph{flip} experiment outcomes. Therefore, this calls for a shift in how implementations are being used. In addition, we recommend for (1) replicability studies for studies mistakenly assuming implementation interchangeability, (2) DRL researchers and practitioners to adopt the differential testing methodology proposed in this paper to combat implementation inconsistencies, and (3) the use of large environment suites.

## 26. Patch Synthesis for Property Repair of Deep Neural Networks

**Authors:** Zhiming Chi (Institute of Software, Chinese Academy of Sciences), Jianan Ma (Hangzhou Dianzi University, China; Zhejiang University, Hangzhou, China), Pengfei Yang (Institute of Software at Chinese Academy of Sciences, China), Cheng-Chao Huang (Nanjing Institute of Software Technology, ISCAS), Renjue Li (Institute of Software at Chinese Academy of Sciences, China), Jingyi Wang (Zhejiang University), Xiaowei Huang (University of Liverpool), Lijun Zhang (Institute of Software, Chinese Academy of Sciences)

**Categories:** Software Engineering for AI, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029971

**中文总结:** 提出 PatchPro，以可形式验证的补丁模块做 DNN 局部鲁棒性属性级修复，在保持原网性能的同时对邻域样本提供可证明的修复保证。

**Abstract:** Deep neural networks (DNNs) are prone to various dependability issues, such as adversarial attacks, which hinder their adoption in safety-critical domains. Recently, NN repair techniques have been proposed to address these issues while preserving original performance by locating and modifying guilty neurons and their parameters. However, existing repair approaches are often limited to specific data sets and do not provide theoretical guarantees for the effectiveness of the repairs. To address these limitations, we introduce PatchPro, a novel patch-based approach for property-level repair of DNNs, focusing on local robustness. The key idea behind PatchPro is to construct patch modules that, when integrated with the original network, provide specialized repairs for all samples within the robustness neighborhood while maintaining the network's original performance. Our method incorporates formal verification and a heuristic mechanism for allocating patch modules, enabling it to defend against adversarial attacks and generalize to other inputs. PatchPro demonstrates superior efficiency, scalability, and repair success rates compared to existing DNN repair methods, i.e., realizing provable property-level repair for 100% cases across multiple high-dimensional datasets.

## 27. RUG: Turbo LLM for Rust Unit Test Generation

**Authors:** Xiang Cheng (Georgia Institute of Technology), Fan Sang (Georgia Institute of Technology), Yizhuo Zhai (Georgia Institute of Technology), Xiaokuan Zhang (George Mason University), Taesoo Kim (Georgia Institute of Technology)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029738

**中文总结:** 提出 RUG 端到端方案，针对 Rust 复杂类型系统自动生成可编译且高覆盖率的单元测试，克服传统工具与简单 LLM 提示的局限。

**Abstract:** Unit testing improves software quality by evaluating isolated sections of the program. This approach alleviates the need for comprehensive program-wide testing and confines the potential error scope within the software. However, unit test development is time-consuming, requiring developers to create appropriate test contexts and determine input values to cover different code regions. This problem is particularly pronounced in Rust due to its intricate type system, making traditional unit test generation tools ineffective in Rust projects. Recently, LLM have demonstrated their proficiency in understanding programming language and completing software engineering tasks. However, merely prompting LLM with a basic prompt like "generate unit test for the following source code" often results in code with compilation errors. In addition, LLM-generated unit tests often have limited test coverage. To bridge this gap and harness the capabilities of LLM, we design and implement RUG, an end-to-end solution to automatically generate the unit test for Rust projects. To help LLM's generated test pass Rust strict compilation checks, RUG designs a semantic-aware bottom-up approach to divide the context construction problem into dependent sub-problems. It solves these sub-problems sequentially using an LLM and merges them to a complete context. To increase test coverage, RUG integrates coverage-guided fuzzing with LLM to prepare fuzzing harnesses. Applying RUG on 17 real-world Rust programs (average 24,937 LoC), we show that RUG can achieve a high code coverage, up to 71.37%, closely comparable to human effort (73.18%). We submitted 113 unit tests generated by RUG covering the new code: 53 of them have been accepted, 17 were rejected, and 43 are pending for review.

## 28. SOEN-101: Code Generation by Emulating Software Process Models Using Large Language Model Agents

**Authors:** Feng Lin (Concordia University), Dong Jae Kim (DePaul University), Tse-Hsun (Peter) Chen (Concordia University)

**Categories:** AI for Software Engineering, Software Engineering for AI, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029771

**中文总结:** 提出 FlowGen 多智能体框架，模拟瀑布、TDD 与 Scrum 流程生成代码；FlowGen_Scrum 在 HumanEval 等基准 Pass@1 达 75.2。

**Abstract:** Software process models are essential to facilitate collaboration and communication among software teams to solve complex development tasks. Inspired by these software engineering practices, we present FlowGen – a code generation framework that emulates software process models based on multiple Large Language Model (LLM) agents. We emulate three process models, FlowGen$_{Waterfall}$, FlowGen$_{TDD}$, and FlowGen$_{Scrum}$, by assigning LLM agents to embody roles (i.e., requirement engineer, architect, developer, tester, and scrum master) that correspond to everyday development activities and organize their communication patterns. The agents work collaboratively using chain-of-thought and prompt composition with continuous self-refinement to improve the code quality. We use GPT-3.5 as our underlying LLM and several baselines (RawGPT, CodeT, Reflexion) to evaluate code generation on four benchmarks: HumanEval, HumanEval-ET, MBPP, and MBPP-ET. Our findings show that FlowGen$_{Scrum}$ excels compared to other process models, achieving a Pass@1 of 75.2, 65.5, 82.5, and 56.7 in HumanEval, HumanEval-ET, MBPP, and MBPP-ET, respectively (an average of 15% improvement over RawGPT). Compared with other state-of-the-art techniques, FlowGen$_{Scrum}$ achieves a higher Pass@1 in MBPP compared to CodeT, with both outperforming Reflexion. Notably, integrating CodeT into FlowGen$_{Scrum}$ resulted in statistically significant improvements, achieving the highest Pass@1 scores. Our analysis also reveals that the development activities impacted code smell and exception handling differently, with design and code review adding more exception handling and reducing code smells. Finally, FlowGen models maintain stable Pass@1 scores across GPT-3.5 versions and temperature values, highlighting the effectiveness of software process models in enhancing the quality and stability of LLM-generated code.

## 29. Testing and Understanding Deviation Behaviors in FHE-hardened Machine Learning Models

**Authors:** Yiteng Peng (Hong Kong University of Science and Technology), Daoyuan Wu (Hong Kong University of Science and Technology), Zhibo Liu (Hong Kong University of Science and Technology), Dongwei Xiao (Hong Kong University of Science and Technology), Zhenlan Ji (The Hong Kong University of Science and Technology), Juergen Rahmel (HSBC), Shuai Wang (Hong Kong University of Science and Technology)

**Categories:** Software Engineering for AI, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029814

**中文总结:** 提出 HEDiff 差分测试工具，以明文模型的 margin 指标引导在全同态加密加固 ML 模型上定向搜索偏差触发输入，系统揭示 FHE 模型与明文模型输出不一致的偏差行为。

**Abstract:** Fully homomorphic encryption (FHE) is a promising cryptographic primitive that enables secure computation over encrypted data. A primary use of FHE is to support privacy-preserving machine learning (ML) on public cloud infrastructures. Despite the rapid development of FHE-based ML (or HE-ML) in recent years, the community still lacks a systematic understanding of their robustness. In this paper, we aim to systematically test and understand the deviation behaviors of HE-ML models, where the same input causes deviant outputs between FHE-hardened models and their plaintext versions, leading to completely incorrect model predictions. To effectively uncover deviation-triggering inputs under the constraints of expensive FHE computation, we design a novel differential testing tool called HEDiff, which leverages the margin metric on the plaintext model as guidance to drive targeted testing on FHE models. For the identified deviation inputs, we further analyze them to determine whether they exhibit general noise patterns that are transferable. We evaluate HEDiff using three popular HE-ML frameworks, covering 12 different combinations of models and datasets. HEDiff successfully detected hundreds of deviation inputs across almost every tested FHE framework and model. We also quantitatively show that the identified deviation inputs are (visually) meaningful in comparison to regular inputs. Further schematic analysis reveals the root cause of these deviant inputs and allows us to generalize their noise patterns for more directed testing.

## 30. The Product Beyond the Model -- An Empirical Study of Repositories of Open-Source ML Products

**Authors:** Nadia Nahar (Carnegie Mellon University), Haoran Zhang (Carnegie Mellon University), Grace Lewis (Carnegie Mellon Software Engineering Institute), Shurui Zhou (University of Toronto), Christian Kästner (Carnegie Mellon University)

**Categories:** Software Engineering for AI, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029840

**中文总结:** 从 GitHub 50 万+ ML 相关项目中识别 262 个开源 ML 产品并深入分析 30 个，报告 21 项发现（如数据科学家参与有限、ML/非 ML 模块化低、测试与监控实践不足）。

**Abstract:** Machine learning (ML) components are increasingly incorporated into software products for end-users, but developers face challenges in transitioning from ML prototypes to products. Academics have limited access to the source of commercial ML products, challenging research progress. In this study, first, we contribute a novel process to identify 262 open-source ML products among more than half a million ML-related projects on GitHub. Then, we qualitatively and quantitatively analyze 30 open-source ML products to answer six broad research questions about development practices and system architecture. We find that the majority of the ML products in our sample represent startup-style development reported in past interview studies. We report 21 findings, including limited involvement of data scientists in many ML products, unusually low modularity between ML and non-ML code, diverse architectural choices on incorporating models into products, and limited prevalence of industry best practices such as model testing, pipeline automation, and monitoring. Additionally, we discuss 7 implications of this study on research, development, and education, including the need for tools to assist teams without data scientists, education opportunities, and open-source-specific research for privacy-preserving telemetry.

## 31. Towards More Trustworthy Deep Code Models by Enabling Out-of-Distribution Detection

**Authors:** Yanfu Yan (William & Mary), Viet Duong (William & Mary), Huajie Shao (College of William & Mary), Denys Poshyvanyk (William & Mary)

**Categories:** Software Engineering for AI, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029813

**中文总结:** 为代码深度学习模型提出无监督与弱监督分布外检测方法，使模型能识别分布偏移样本并拒绝预测或转发至合适模型，提升可信度。

**Abstract:** Numerous machine learning (ML) models have been developed, including those for software engineering (SE) tasks, under the assumption that training and testing data come from the same distribution. However, train and test distributions often differ, as training datasets rarely encompass the entire distribution, while test distribution tends to shift over time. Hence, when confronted with out-of-distribution (OOD) instances that differ from the training data, a reliable and trustworthy SE ML model must be capable of detecting them to either abstain from making predictions, or potentially forward these OODs to appropriate models handling other categories or tasks. In this paper, we develop two types of SE-specific OOD detection models, unsupervised and weakly-supervised OOD detection for code. The unsupervised OOD detection approach is trained solely on in-distribution samples while the weakly-supervised approach utilizes a tiny number of OOD samples to further enhance the detection performance in various OOD scenarios. Extensive experimental results demonstrate that our proposed methods significantly outperform the baselines in detecting OOD samples from four different scenarios simultaneously and also positively impact a main code understanding task.

## 32. TraceFL: Interpretability-Driven Debugging in Federated Learning via Neuron Provenance

**Authors:** Waris Gill (Virginia Tech), Ali Anwar (University of Minnesota), Muhammad Ali Gulzar (Virginia Tech)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029768

**中文总结:** 提出 TraceFL，通过神经元溯源机制在联邦学习中追溯全局模型预测至具体客户端，支持可解释调试与责任定位。

**Abstract:** In Federated Learning, clients train models on local data and send updates to a central server, which aggregates them into a global model using a fusion algorithm. This collaborative yet privacy-preserving training comes at a cost—FL developers face significant challenges in attributing global model predictions to specific clients. Localizing responsible clients is a crucial step towards (a) excluding clients primarily responsible for incorrect predictions and (b) encouraging clients who contributed high quality models to continue participating in the future. Existing ML explainability approaches are inherently inapplicable as they are designed for single-model, centralized training. We introduce TraceFL, a fine-grained neuron provenance capturing mechanism that identifies clients responsible for the global model’s prediction by tracking the flow of information from individual clients to the global model. Since inference on different inputs activates a different set of neurons of the global model, TraceFL dynamically quantifies the significance of the global model’s neurons in a given prediction. It then selectively picks a slice of the most crucial neurons in the global model and maps them to the corresponding neurons in every participating client to determine each client’s contribution, ultimately localizing the responsible client. We evaluate TraceFL on six datasets, including two real-world medical imaging datasets and four neural networks, including advanced models such as GPT. TraceFL achieves 99% accuracy in localizing the responsible client in FL tasks spanning both image and text classification tasks. At a time when state-of-the-art ML debugging approaches are mostly domain-specific (e.g., image classification only), TraceFL is the first technique to enable highly accurate automated reasoning across a wide range of FL applications.

## 33. Understanding the Effectiveness of Coverage Criteria for Large Language Models: A Special Angle from Jailbreak Attacks

**Authors:** shide zhou (Huazhong University of Science and Technology), Li Tianlin (NTU), Kailong Wang (Huazhong University of Science and Technology), Yihao Huang (NTU), Ling Shi (Nanyang Technological University), Yang Liu (Nanyang Technological University), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI, Security and Vulnerability

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029795

**中文总结:** 实证表明 LLM 隐藏状态聚类可区分正常与 jailbreak 查询，传统覆盖率准则在神经元、层与 token 层面能揭示安全测试不足并指导 LLM 测试。

**Abstract:** Large language models (LLMs) have revolutionized artificial intelligence, but their increasing deployment across critical domains has raised concerns about their abnormal behaviors when faced with malicious attacks. Such vulnerability alerts the widespread inadequacy of pre-release testing. In this paper, we conduct a comprehensive empirical study to evaluate the effectiveness of traditional coverage criteria in identifying such inadequacies, exemplified by the significant security concern of jailbreak attacks. Our study begins with a clustering analysis of the hidden states of LLMs, revealing that the embedded characteristics effectively distinguish between different query types. We then systematically evaluate the performance of these criteria across three key dimensions: criterion level, layer level, and token level. Our research uncovers significant differences in the sets of neurons covered when LLMs process normal versus jailbreak queries, aligning with our clustering experiments. Leveraging these findings, we propose three practical applications of coverage criteria in the context of LLM security testing. Specifically, we develop a real-time jailbreak detection mechanism that achieves high accuracy (93.61% on average) in classifying queries as normal or jailbreak. Furthermore, we explore the use of coverage levels to prioritize test cases, improving testing efficiency by focusing on high-risk interactions and removing redundant tests. Lastly, we introduce a coverage-guided approach for generating jailbreak attack examples, enabling systematic refinement of prompts to uncover new vulnerabilities. This study improves our understanding of LLM security testing, enhances their safety, and provides a foundation for developing more robust AI applications.

## 34. µPRL: A Mutation Testing Pipeline for Deep Reinforcement Learning based on Real Faults

**Authors:** Deepak-George Thomas (Tulane University), Matteo Biagiola (Università della Svizzera italiana), Nargiz Humbatova (Università della Svizzera italiana), Mohammad Wardat (Oakland University, USA), Gunel Jahangirova (King's College London), Hridesh Rajan (Tulane University), Paolo Tonella (USI Lugano)

**Categories:** Software Engineering for AI, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029852

**中文总结:** 提出 µPRL 变异测试流水线，基于仓库挖掘的真实强化学习故障分类设计变异算子；实验表明能有效区分强/弱测试生成器并反馈测试充分性。

**Abstract:** Reinforcement Learning (RL) is increasingly adopted to train agents that can deal with complex sequential tasks, such as driving an autonomous vehicle or controlling a complex environment. Correspondingly, novel approaches are needed to ensure that RL agents have been tested adequately before going to production. Among them, mutation testing is quite promising, especially under the assumption that the injected faults (mutations) mimic the real ones. In this paper, we first describe a taxonomy of real RL faults obtained by repository mining. Then, we present the mutation operators derived from such real faults and implemented in the tool µPRL. Finally, we discuss the experimental results, which show that µPRL is extremely effective at discriminating strong from weak test generators, hence providing useful feedback to developers about the adequacy of the test scenarios generated and executed so far.
