# ASE 2025 Research Track — Awarded Papers

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Total awarded papers: 21

## Award breakdown

| Award | # Papers |
| --- | ---: |
| ACM SIGSOFT Distinguished Paper Award | 21 |

## 1. Bridging Natural Language and Formal Specification - Automated Translation of Software Requirements to LTL via Hierarchical Semantics Decomposition Using LLMs

**Authors:** Zhi Ma (Xidian University), Cheng Wen (Xidian University), Zhexin Su (Xidian University), Xiao Liang (Xidian University), Cong Tian (Xidian University), Shengchao Qin (Xidian University), Mengfei Yang (China Academy of Space Technology)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334235

**中文总结:** 提出 Req2LTL，通过层次中间表示 OnionL 将 LLM 语义分解与确定性 LTL 规则合成结合；在航空航天真实需求上达 88.4% 语义准确率与 100% 语法正确率，显著优于现有方法。

**Abstract:** Automating the translation of natural language (NL) software requirements into formal specifications remains a critical challenge in scaling formal verification practices to industrial settings, particularly in safety-critical domains. Existing approaches, both rule-based and learning-based, face significant limitations. While large language models (LLMs) like GPT-4o demonstrate proficiency in semantic extraction, they still encounter difficulties in addressing the complexity, ambiguity, and logical depth of real-world industrial requirements. In this paper, we propose \textbf{Req2LTL}, a modular framework that bridges NL and Linear Temporal Logic (LTL) through a hierarchical intermediate representation called \textit{OnionL}. \textbf{Req2LTL} leverages LLMs for semantic decomposition and combines them with deterministic rule-based synthesis to ensure both syntactic validity and semantic fidelity. Our comprehensive evaluation demonstrates that \textbf{Req2LTL} achieves 88.4% semantic accuracy and 100% syntactic correctness on real-world aerospace requirements, significantly outperforming existing methods.


## 2. Characterizing Multi-Hunk Patches: Divergence, Proximity, and LLM Repair Challenges

**Authors:** Noor Nashid (University of British Columbia), Daniel Ding (University of British Columbia), Keheliya Gallaba (Centre for Software Excellence), Ahmed E. Hassan (Queen’s University), Ali Mesbah (University of British Columbia)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334668

**中文总结:** 基于 372 个真实缺陷构建多 hunk 补丁数据集 HUNK4J，提出 hunk divergence 与空间邻近度分类刻画跨文件编辑复杂度；对六种 LLM 的实证显示修复成功率随 divergence 与空间分散度上升而下降，最分散 Fragment 类纯 LLM 无一成功。

**Abstract:** Multi-hunk bugs, where fixes span disjoint regions of code, are common in practice, yet remain underrepresented in automated repair. Existing techniques and benchmarks pre-dominantly target single-hunk scenarios, overlooking the added complexity of coordinating semantically related changes across the codebase. In this work, we characterize HUNK4J, a dataset of multi-hunk patches derived from 372 real-world defects. We propose hunk divergence, a metric that quantifies the variation among edits in a patch by capturing lexical, structural, and file-level differences, while incorporating the number of hunks involved. We further define spatial proximity, a classification that models how hunks are spatially distributed across the program hierarchy. Our empirical study spanning six LLMs reveals that model success rates decline with increased divergence and spatial dispersion. Notably, when using the LLM alone, no model succeeds in the most dispersed Fragment class. These findings highlight a critical gap in LLM capabilities and motivate divergence-aware repair strategies.


## 3. Clarifying Semantics of In-Context Examples for Unit Test Generation

**Authors:** Chen Yang (Tianjin University), Lin Yang (Tianjin University), Ziqi Wang (Tianjin University), Dong Wang (Tianjin University), Jianyi Zhou (Huawei Cloud Computing Technologies Co., Ltd.), Junjie Chen (Tianjin University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334234

**中文总结:** 提出 CLAST，通过程序分析与 LLM 重写将复杂单元测试分解并澄清语义，使其更适合作为 ICL 示例；在四个开源与三个工业项目中全面优于 UTgen，在保留原测试有效性的同时显著提升语义清晰度。

**Abstract:** Recent advances in large language models (LLMs) have enabled promising performance in unit test generation through in-context learning (ICL). However, the quality of in-context examples significantly influences the effectiveness of generated tests—poorly structured or semantically unclear test examples often lead to suboptimal outputs. In this paper, we propose CLAST, a novel technique that systematically refines unit tests to improve their semantic clarity, thereby enhancing their utility as in-context examples. The approach decomposes complex tests into logically clearer ones and improves semantic clarity through a combination of program analysis and LLM-based rewriting. We evaluated CLAST on four open-source and three industrial projects. The results demonstrate that CLAST largely outperforms UTgen, the state-of-the-art refinement technique, in both preserving test effectiveness and enhancing semantic clarity. Specifically, CLAST fully retains the original effectiveness of unit tests, while UTgen reduces compilation success rate (CSR), pass rate (PR), and test coverage (Cov) by an average of 12.90%, 35.82%, an 4.65%, respectively. Over 85.33% of participants in our user study preferred the semantic clarity of CLAST-refined tests. Notably, incorporating \tech-refined tests as examples effectively improves ICL-based unit test generation approaches such as RAGGen and TELPA, resulting in an average increase of 25.97% in CSR, 28.22% in PR, and 45.99% in Cov for generated tests, compared to incorporating UTgen-refined tests. The insights from the follow-up user study not only reinforce CLAST’s potential impact in software testing practice but also illuminate avenues for future research.


## 4. DualFuzz: Detecting Vulnerability in Wi-Fi NICs through Dual-Directional Fuzzing

**Authors:** Yuanliang Chen (Tsinghua University), Fuchen Ma (Tsinghua University), Yanyang Zhao (Tsinghua University), Yuanyi Li (Shuimu Yulin Technology Co., Ltd), Yu Jiang (Tsinghua University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334315

**中文总结:** 提出 DualFuzz，构建传输-接收交互模型 TRModel 并同步 fuzz Wi-Fi NIC 收发双向逻辑，配合延迟引导 fuzz 与活性/等价检测；在 8 款主流 NIC 上发现传统单向 fuzz 遗漏的漏洞。

**Abstract:** Wi-Fi Network Interface Cards (NICs) are vital for enabling wireless connectivity across a wide range of devices. Ensuring their security is critical, as vulnerabilities can expose entire networks to threats. Fuzzing is a promising technique for detecting such flaws. However, existing Wi-Fi fuzzers typically test transmission and reception separately, overlooking their interactions and resulting in inefficient testing.

In this work, we present DualFuzz, a dual-directional fuzzing framework designed to simultaneously test both transmission and reception processes in Wi-Fi NICs. First, DualFuzz automatically identifies interaction behaviors within Wi-Fi NICs and constructs a Transmission-Reception Model (TRModel) to characterize Wi-Fi frames that influence these interactions. Leveraging this model, DualFuzz utilizes latency guided fuzzing to efficiently coordinate exploring transmission and reception interaction logics. Finally, we propose liveness and equivalence detectors that enable real-time monitoring to identify abnormal states and uncover potential vulnerabilities in Wi-Fi NICs. We implemented and evaluated DualFuzz on eight widely used Wi-Fi NICs, incorporating chipsets from various manufacturers (e.g., Intel and Realtek). Compared to state-of-the-art Wi-Fi fuzzers like OwFuzz, wpaspy, and Greyhound, DualFuzz detects 75%, 163%, and 250% more vulnerabilities, respectively. In total, it uncovered 21 previously unknown vulnerabilities, 7 of which have been assigned CVEs. All have been confirmed and fixed by the corresponding maintainers.


## 5. Efficient and Verifiable Proof Logging for MaxSAT Solving

**Authors:** Raoul van Doren (ETH Zurich), Timos Antonopoulos (Yale University), Ruzica Piskac (Yale University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334432

**中文总结:** 为 core-guided OLL MaxSAT 求解器提出首个专用可验证证明日志框架，形式化 cores/cliques/hardenings/totalizer 等推理规则并在 EvalMaxSAT 实现可读与紧凑二进制 DAG 日志；在 2024 MaxSAT 竞赛数据集上验证可行性与可扩展性。

**Abstract:** MaxSAT solvers are increasingly used as back-ends in software engineering tools. Yet their results have lacked automatically checkable certificates of optimality. While SAT solvers emit DRAT proofs of (un)satisfiability, MaxSAT must additionally prove that no lower-cost solution exists. Existing approaches either cover only isolated solving paradigms or reduce MaxSAT reasoning to heavyweight pseudo-Boolean proofs, yielding impractical verification overhead. We present the first MaxSAT-specific proof-logging framework for core-guided OLL solvers. We formalize native inference rules for cores, cliques, hardenings, totalizer updates, and bound adjustments, and implement both a human-readable logger and a compact binary DAG logger in EvalMaxSAT. Evaluation on the 2024 MaxSAT competition dataset confirm the practicality and scalability of our certification pipeline, paving the way for trustworthy, solver use.


## 6. Enhancing LLMs with Staged Grouping and Dehallucination for Header File Decomposition

**Authors:** Yue Wang (Peking University), Jiaxuan Sun (Peking University), Yanzhen Zou (Peking University), Bing Xie (Peking University)

**Categories:** Evolution and Maintenance

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334283

**中文总结:** 提出 HFDecomposer，以两阶段分组（相似度粗分 + LLM 读组摘要细分）并配合 dehallucination 缓解 token 限制与幻觉，混合 LLM 与传统相似度度量分解 God Header File，生成更贴合功能本质的重构方案。

**Abstract:** God Header Files, large header files included by numerous other code files, present significant challenges for code comprehension and maintenance while also increasing recompilation time. Existing approaches leverage various code similarity metrics to decompose such header files, but these metrics do not always capture the code’s functional essence accurately. Large Language Models (LLMs), with their advanced capabilities in code understanding and generation, offer a promising alternative for producing more effective refactorings. However, LLMs face limitations with lengthy code files due to token restrictions and reduced effectiveness in processing long inputs. Additionally, purely LLM-based solutions often suffer from hallucination, producing incomplete or spurious decomposition results. To address these challenges, we propose HFDecomposer, a hybrid approach that enhances LLMs with staged grouping and dehallucination techniques to effectively decompose header files. Our approach introduces a two-stage grouping framework for lengthy header files: it first groups strongly related code entities using traditional similarity metrics, then feeds group summaries to the LLM for higher-level semantic aggregation. To mitigate LLM hallucinations, we enhance prompts with factual knowledge extracted from static analysis, detect errors in LLM output, and make necessary corrections by reassigning missing entities and resolving cyclic dependencies. Our evaluation on real-world header file decomposition refactorings demonstrates that our method effectively overcomes the limitations of purely LLM-based techniques and outperforms the traditional state-of-the-art approach by 11%, delivering more accurate and reliable decomposition results. Our approach enables LLMs to handle lengthy header files efficiently, significantly reduces hallucinations, and ensures the reliability and practicality of the final decomposition.


## 7. Faster Runtime Verification during Testing via Feedback-Guided Selective Monitoring

**Authors:** Shinhae Kim (Cornell University), Saikat Dutta (Cornell University), Owolabi Legunsen (Cornell University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334469

**中文总结:** 提出 Valg，首个基于强化学习的测试时选择性运行时验证技术，利用 monitor 冗余反馈仅创建必要 monitor；在 64 个 Java 开源项目上比 JavaMOP 快最多 20.2 倍、比 TraceMOP 快最多 555.6 倍。

**Abstract:** Runtime verification (RV) uses monitors, which are dynamically created based on formal specifications (specs), to check running programs against specs. RV of passing tests in many open-source projects found hundreds of new bugs. But, high overheads make it hard to use RV for testing in practice. We propose Valg, the first on-the-fly selective RV technique for testing, and the first to use reinforcement learning (RL) to speed up RV. Valg leverages a recent finding: 99.87% of monitors are redundant for testing; they wastefully re-check unique traces—sequences of events, e.g., method calls—that the other necessary 0.13% already checked. Valg uses feedback about redundancy of prior monitors and events to selectively monitor only necessary ones subsequently. A key idea in Valg is our novel formulation of selective monitor creation as a two-armed bandit RL problem that rewards necessary monitors, and penalizes redundant ones. We implement Valg for Java and compare it with state-of-the-art RV tools on one revision each of 64 open-source projects. With default RL hyperparameters, Valg is up to 20.2x and 555.6x faster than JavaMOP and TraceMOP, respectively. For example, Valg takes only 54.8 minutes in total to monitor three projects where TraceMOP takes 3.02 days in total. Valg finds 99.6% of JavaMOP and TraceMOP’s spec violations, but it only checks 76.7% of their unique traces on average. After tuning hyperparameters, Valg checks 95.1% of unique traces on average with little loss in speed. Using tuned hyperparameters from one revision “into the future” as code evolves preserves Valg’s high rate of checked unique traces and speedups, without needing frequent re-tuning.


## 8. Finding Bugs in MLIR Compiler Infrastructure via Lowering Space Exploration

**Authors:** Jingjing Liang (East China Normal University), Shan Huang (East China Normal University), Ting Su (East China Normal University)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334563

**中文总结:** 提出 lowering space exploration 并实现 LOBE，利用同一 MLIR 程序多条合法 lowering 路径应语义等价的不变性，自适应构造多样化 lowering 路径并对比执行结果发现编译基础设施 bug。

**Abstract:** MLIR is a widely adopted compiler infrastructure that supports multi-level IRs and reusable components. Ensuring its correctness is critical, as bugs can propagate to downstream systems. MLIR provides a lowering mechanism that transforms high-level programs into low-level representations through configurable sequences of passes, and allows multiple valid lowering paths for a given program. This gives rise to a lowering equivalence property: all valid lowering paths for the same MLIR program should produce semantically equivalent results. In this paper, we leverage this property and propose lowering space exploration, to effectively test the MLIR infrastructure. Our approach dynamically constructs diverse lowering paths in an adaptive, stepwise manner using atomic lowering rules combined with a feedback-based scheduling mechanism. It finds bugs by comparing the execution results across these paths. Any inconsistencies indicate potential bugs in the MLIR infrastructure. To the best of our knowledge, this is the first work to test MLIR from the perspective of exploring its compilation space. We implement our approach in a tool named LOBE and evaluate it on latest MLIR versions. LOBE discovers 40 previously unknown bugs, including 10 miscompilations and 30 crash bugs, with 25 confirmed/fixed.


## 9. FlakyGuard: Automatically Fixing Flaky Tests at Industry Scale

**Authors:** Chengpeng Li (University of Texas at Austin), Farnaz Behrang (Uber Technologies), August Shi (The University of Texas at Austin), Peng Liu (Uber Technologies)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334450

**中文总结:** 提出 FlakyGuard，将代码建模为图并选择性图遍历为 LLM 提供恰当上下文以修复 flaky test；在工业仓库上修复 47.6% 可复现 flaky test，51.8% 补丁被开发者接受，成功率比 SOTA 至少高 22%。

**Abstract:** Flaky tests that non-deterministically pass or fail waste developer time and slow release cycles. While large language models (LLMs) show promise for automatically repairing flaky tests, existing approaches like FlakyDoctor fail in industrial settings due to the context problem: providing either too little context (missing critical production code) or too much context (overwhelming the LLM with irrelevant information). We present FlakyGuard, which addresses this problem by treating code as a graph structure and using selective graph exploration to find only the most relevant context. Evaluation on real-world flaky tests from industrial repositories shows that FlakyGuard repairs 47.6% of reproducible flaky tests with 51.8% of the fixes accepted by developers. Besides it outperforms state-of-the-art approaches by at least 22% in repair success rate. Developer surveys confirm that 100% find FlakyGuard’s root cause explanations useful.


## 10. iKnow: an Intent-Guided Chatbot for Cloud Operations with Retrieval-Augmented Generation

**Authors:** Junjie Huang (The Chinese University of Hong Kong), Yuedong Zhong (Sun Yat-sen University), Guangba  Yu (The Chinese University of Hong Kong), Zhihan Jiang (The Chinese University of Hong Kong), Minzhi Yan (HCC Lab, Huawei Cloud Computing Technology Co., Ltd), Wenfei Luan (HCC Lab, Huawei Cloud Computing Technology Co., Ltd), Tianyu Yang (HCC Lab, Huawei Cloud Computing Technology Co., Ltd), Rui Ren (Computing and Networking Innovation Lab, Huawei Cloud Computing Technology Co., Ltd), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334651

**中文总结:** 基于 2,000 条大型云厂商真实运维查询识别五类 OpsQA 意图与六类 chatbot 失败根因，提出 intent-guided RAG 聊天机器人 iKnow，针对查询补全、检索与生成各环节提升云运维问答可靠性。

**Abstract:** Managing complex cloud services requires standard operational documentation, but its sheer volume often hinders cloud engineers from efficient knowledge acquisition. Retrieval-Augmented Generation (RAG) can streamline this process by retrieving relevant knowledge and generating concise, referenced answers. However, deploying a reliable RAG-based chatbot for cloud operation remains a challenge. In this experience paper, we analyze the development and deployment of RAG-based chatbots for operational question answering (OpsQA) at a large-scale cloud vendor. Through an empirical study of 2,000 real-world queries across three operational teams, we identify five unique OpsQA intent types (e.g., symptom analysis and terminology explanation) and their corresponding requirements for a satisfactory answer, which differ from general software engineering queries. Our analysis further uncovers six root causes leading to chatbot failures—over half stem from query issues (i.e., incompleteness, out-of-scope, or invalid queries), while others are from retrieval or generation issues. To address these issues, we propose iKnow, an intent-guided RAG-based chatbot that integrates intent detection, query rewriting tailored to each intent, and missing knowledge detection to enhance answer quality. In internal evaluations, iKnow improves average answer accuracy from 65.8% to 81.3% with only a modest increase in latency. iKnow has been deployed for six months at CloudA, supporting thousands of cloud engineers in daily operations. We discuss lessons learned from real-world deployment, providing valuable insights for future research and practical implementations in similar domains.


## 11. LogMoE: Lightweight Expert Mixture for Cross-System Log Anomaly Detection

**Authors:** Jiaxing Qi (Beihang University), Zhongzhi Luan (Beihang University), Shaohan Huang (Beihang University), Carol Fung (Concordia University), Yuchen Wang (Beihang University), Aibin Wang (Beihang University), Hongyu Zhang (Chongqing University), Hailong Yang (Beihang University, China), Depei Qian (Beihang University, China)

**Categories:** Debugging and Fault Diagnosis

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334514

**中文总结:** 提出 LogMoE，无解析、轻量 Mixture-of-Experts 跨系统日志异常检测：用多成熟系统标注日志训练专家并通过门控集成，适应未见目标系统与异构日志格式；在八种数据集、三种泛化场景下，尤其在目标标注稀缺时保持稳健泛化。

**Abstract:** Robust anomaly detection in system logs plays a crucial role in maintaining stable and reliable software operations. However, existing methods often struggle to accommodate evolving log formats and distributional shifts across systems, as they heavily rely on large volumes of labeled data, log parsing, and predefined event templates. To address these challenges, we propose LogMoE, a scalable and parsing-free log anomaly detection framework. LogMoE utilizes labeled logs from multiple mature systems to train a set of lightweight expert models, which are integrated via a gating mechanism within a Mixture-of-Experts (MoE) architecture. This design enables LogMoE to generalize effectively to previously unseen target systems. By eliminating the need for log parsing, our approach remains robust against the heterogeneity of log formats and syntactic structures. We conduct extensive evaluations on eight log datasets under varying generalization scenarios: single-system, homogeneous-system, and heterogeneous-system. Experimental results demonstrate that LogMoE consistently achieves robust generalization, particularly under conditions with scarce labeled data in the target system. As such, LogMoE provides a scalable, parsing-free, and generalization-capable solution tailored for complex and continuously evolving software system environments, positioning it as a future-ready approach to log anomaly detection.


## 12. LOSVER: Line-Level Modifiability Signal-Guided Vulnerability Detection and Classification

**Authors:** Doha Nam (Korea Advanced Institute of Science and Technology), Jongmoon Baik (Korea Advanced Institute of Science and Technology)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334430

**中文总结:** 提出 LOSVER 两阶段漏洞检测/分类框架：先定位「可修改性」较高的不稳定代码行，再在 PLM 分析中赋予这些行更高权重；相比无显式脆弱区域引导的 PLM 方法，漏洞检测与分类更准确。

**Abstract:** The increasing prevalence of software vulnerabilities continues to pose serious threats to system security, underscoring the need for accurate and scalable techniques for vulnerability detection and classification. While Pre-trained Language Models (PLMs) have shown strong potential in vulnerability analysis, most existing methods provide no explicit guidance on which parts of the input code are more likely to be vulnerable. As a result, the model must infer token-level relevance without any indication of which parts are important, making it harder to learn the characteristics of vulnerable code during training. To address this limitation, we propose LOSVER (Line-level mOdifiability Signal-guided VulnERability analyzer), a novel two-stage framework that enhances PLM-based vulnerability analysis by incorporating line-level modifiability signals. In the first stage, LOSVER localizes modifiable lines. These are code segments likely to be changed in the future due to instability or complexity, which are often associated with vulnerabilities. In the second stage, the model assigns greater importance to the predicted modifiable lines, allowing the PLM to focus on potentially vulnerable regions during both training and inference. We evaluated LOSVER with two widely used benchmark datasets: Devign, for function-level vulnerability detection, and Big-Vul, for function-level vulnerability classification with Common Weakness Enumeration (CWE) ID labels. Experimental results show that LOSVER improves detection accuracy on Devign by approximately 4 percentage points and increases the weighted F1-score for CWE ID classification on Big-Vul by over 2 points, when applied on top of the UniXcoder baseline. We also conducted experiments on the PrimeVul dataset, which focuses on vulnerability–patch pairs, and observed meaningful improvements in pair-wise detection. These results demonstrate that integrating line-level modifiability signals significantly enhances the effectiveness of PLM-based software vulnerability analysis across both detection and classification tasks.


## 13. "My productivity is boosted, but ..." Demystifying Users’ Perception on AI Coding Assistants

**Authors:** Yunbo Lyu (Singapore Management University), Zhou Yang (University of Alberta, Alberta Machine Intelligence Institute), Jieke Shi (Singapore Management University), Chang Jianming, Yue Liu (Monash University), David Lo (Singapore Management University)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334533

**中文总结:** 分析 VS Code Marketplace 中 1085 个 AI 编码助手（90% 近两年发布）及 32 个高安装量产品的用户评论，构建开发者真实使用场景下的关切与满意度分类体系；揭示「生产力提升但……」等典型价值与痛点。

**Abstract:** This paper aims to explore fundamental questions in the era when AI coding assistants like GitHub Copilot are widely adopted: \textit{what do developers truly value and criticize in AI coding assistants, and what does this reveal about their needs and expectations in real-world software development?} Unlike previous studies that conduct observational research in controlled and simulated environments, we analyze extensive, first-hand user reviews of AI coding assistants, which capture developers’ authentic perspectives and experiences drawn directly from their actual day-to-day work contexts. We identify 1,085 AI coding assistants from the Visual Studio Code Marketplace. Although they only account for 1.64% of all extensions, we observe a surge in these assistants: over 90% of them are released within the past two years. We then manually analyze the user reviews sampled from 32 AI coding assistants that have sufficient installations and reviews to construct a comprehensive taxonomy of user concerns and feedback about these assistants. We manually annotate each review’s attitude when mentioning certain aspects of coding assistants, yielding nuanced insights into user satisfaction and dissatisfaction regarding specific features, concerns, and overall tool performance. Built on top of the findings—including how users demand not just intelligent suggestions but also context-aware, customizable, and resource-efficient interactions—we propose five practical implications and suggestions to guide the enhancement of AI coding assistants that satisfy user needs.


## 14. Not Every Patch is an Island: LLM-Enhanced Identification of Multiple Vulnerability Patches

**Authors:** Yi Song (School of Computer Science, Wuhan University), Dongchen Xie (School of Cyber Science and Engineering, Wuhan University), Lin Xu (School of Cyber Science and Engineering, Wuhan University), He Zhang (School of Computer Science, Wuhan University), Chunying Zhou (School of Computer Science, Wuhan University), Xiaoyuan Xie (Wuhan University)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334340

**中文总结:** 提出 SHIP，面向「一漏洞多补丁」静默漏洞补丁识别（SVPI）：利用 LLM 建模补丁间关联而非逐条相似度排序；在含多补丁 CVE 场景下显著优于假设单补丁的现有 SVPI 技术。

**Abstract:** For a vulnerability reported as an item of platforms such as CVE or NVD, software maintainers need to submit patches (in the form of \emph{code commit}) to fix it, which is often performed silently for the sake of keeping products’ reputation or avoiding malicious attacks. But such a silent practice keeps patches hidden from affected downstream software maintainers, thus they have to identify patches in a large corpus of code commits manually, i.e., silent vulnerability patch identification (SVPI). Existing techniques in this field were often developed under the assumption that a vulnerability is matched to one patch, thus output a ranking list that simply reflects the similarity between one individual patch and the vulnerability. However, previous research has demonstrated that many vulnerabilities correspond to more than one patch in practice, this phenomenon largely threatens the effectiveness of existing SVPI techniques because they typically ignore the correlation between patches. In this paper, we propose \textbf{SHIP}, a \textbf{S}ilent vulnerability patc\textbf{H} \textbf{I}dentification approach suited for multi\textbf{P}le-patch scenarios, to make patches corresponding to a vulnerability no longer isolated islands. For a vulnerability item, we first obtain several highly-relevant code commits by measuring heuristic features, and then employ a large language model (i.e., DeepSeek-V3) to predict both the link between a code commit and the vulnerability as well as the link between a pair of code commits, and thus deliver candidate groups each containing one or more code commits that could be patches of the vulnerability. Finally, we perform the max-pooling strategy on the features of code commit(s) contained in each candidate group to determine the ranking of groups, the Top-1 group will be output. The experimental results demonstrate the promise of SHIP: on the benchmark consisting of 4,631 vulnerability items, it can achieve 84.30%, 59.14%, and 69.51% of Recall, Precision, and F1-Score, respectively, outperforming the state-of-the-art SVPI techniques by 37.54%, 28.71%, and 32.35%, respectively.


## 15. Programmers’ Visual Attention on Function Call Graphs During Code Summarization

**Authors:** Samantha McLoughlin (Vanderbilt University), Zachary Karas (Vanderbilt University), Robert Wallace (University of Notre Dame), Aakash Bansal (Louisiana State University), Collin McMillan (University of Notre Dame), Yu Huang (Vanderbilt University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334538

**中文总结:** 研究程序员在代码摘要任务中对函数调用图的视觉注意力，用图遍历深度、覆盖率等指标量化项目级上下文理解；基于既有眼动数据（n=10）重新分析并扩展相关发现。

**Abstract:** This paper studies programmer visual attention on function call graphs during code summarization. Programmer visual attention refers to where people look when performing a software engineering task, and code summarization is the task of writing a natural language description about a section of source code. Prior work has studied programmers’ visual attention during code summarization, with the vast majority of research effort placed on details in single functional units of code. There have not been any techniques developed to understand code comprehension at the project level due to the difficulty of this task, despite the nature of most real-world methods as embedded within complex project context. This paper focuses on the visual attention paid to the call graph context in which a method sits. We analyze visual attention coverage of call graphs with graph-based metrics, such as the depth that programmers traverse or the amount of coverage they attain. We use these metrics, among other means, to reevaluate an existing dataset from a previous eye-tracking study of programmers ($n=10$) that considered basic properties of programmer visual attention in a project context. We then created a new dataset ($n=12$) using the same procedures specifically for this paper, resulting in a total of 88 hours of recorded visual behavior on source code.  We used our proposed metrics to analyze how participants’ visual strategies correlated with their code summary quality, and confidence in their summaries. Interestingly, we found that higher coverage of the call graph was associated with \textit{decreases} in both summary quality and participants’ confidence.


## 16. Rechecking Recheck Requests in Continuous Integration: An Empirical Study of OpenStack

**Authors:** Yelizaveta Brus (University of Waterloo), Rungroj Maipradit (University of Waterloo), Earl T. Barr (University College London), Shane McIntosh (University of Waterloo)

**Categories:** Evolution and Maintenance

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334289

**中文总结:** 基于 OpenStack 314,947 次 recheck 请求，用统计模型区分会成功与仍会失败的 flaky CI 重测；AUROC 0.736，较基线提升 23.6 个百分点，并揭示作业/机器人/用户历史行为最具解释力。

**Abstract:** Continuous Integration (CI) is a process for automatically checking patch sets for errors. CI periodically fails due to non-deterministic (a.k.a., “flaky”) behaviour. Since a patch set may not be the cause of a flaky failure, developers can issue a “recheck” command to request retesting a patch set. Developers waste time considering whether or not to issue a recheck after a CI failure. Prior work also shows that rechecks are issued carelessly, wasting up to 187.4 compute years when CI continues to fail. To save developer time and avoid wasteful rechecks, we fit and analyze statistical models that discriminate between successful and failing rechecks, i.e. those rechecks that will change a failing CI run into a successful one and those that will fail again. Through an empirical study of 314,947 recheck requests from OpenStack, we find that our model successfully differentiates successful and failed rechecks, outperforming baseline approaches by 23.6 percentage points in terms of AUROC (0.736).

Analysis of our model suggests that, in terms of explanatory power, past behaviour of jobs, bots, and users dominate static characteristics of patch sets. Applying our model to automatically request rechecks for those predicted to succeed would have saved ~247 years of elapsed developer time for OpenStack. Applying our model to skip recheck requests when they are predicted to fail would avoid 86.49% of wasted rechecks, saving ~262 years of compute time.


## 17. Seeing is Fixing: Cross-Modal Reasoning with Multimodal LLMs for Visual Software Issue Repair

**Authors:** Kevin Huang, Jian Zhang (Nanyang Technological University), Xiaofei Xie (Singapore Management University), Chunyang Chen (TU Munich)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334310

**中文总结:** 提出 GUIRepair，以 Image2Code 将 GUI 视觉症状转为可执行复现代码、Code2Image 回放验证补丁，实现多模态软件缺陷的跨模态推理与自动修复。

**Abstract:** Large language model (LLM)-based automated program repair (APR) techniques have shown promising results in resolving real-world github issue tasks. Existing APR systems are primarily evaluated in unimodal settings (e.g., SWE-bench), relying solely on textual issue descriptions and source code. However, these autonomous systems struggle to resolve multimodal problem scenarios (e.g., SWE-bench M) due to limitations in interpreting and leveraging visual information. In multimodal scenarios, LLMs need to rely on visual information in the graphical user interface (GUI) to understand bugs and generate fixes. To bridge this gap, we propose GUIRepair, a cross-modal reasoning approach for resolving multimodal issue scenarios by understanding and capturing visual information. Specifically, GUIRepair integrates two key components, Image2Code and Code2Image—to enhance fault comprehension and patch validation. Image2Code extracts relevant project documents based on the issue report, then applies these domain knowledge to generate the reproduced code responsible for the visual symptoms, effectively translating GUI images into executable context for better fault comprehension. Code2Image replays the visual issue scenario using the reproduced code and captures GUI renderings of the patched program to assess whether the fix visually resolves the issue, providing feedback for patch validation. We evaluate GUIRepair on SWE bench M, and the approach demonstrates significant effectiveness. When utilizing GPT-4o as the base model, GUIRepair solves 157 instances, outperforming the best open-source baseline by 26 instances. Furthermore, when using o4-mini as the base model, GUIRepair can achieve even better results and solve 175 instances, outperforming the top commercial system by 22 instances. This emphasizes the success of our new perspective on incorporating cross-modal reasoning by understanding and capturing visual information to resolve multimodal issues.


## 18. TEPHRA: Principled Discovery of Fuzzer Limitations

**Authors:** Vasil Sarafov (μCSRL, CODE Research Institute, University of the Bundeswehr Munich), David Markvica (μCSRL, CODE Research Institute, University of the Bundeswehr Munich), Stefan Brunthaler (Munich Computer Systems Research Laboratory (uCSRL), CODE Research Institute, University of the Bundeswehr Munich)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334676

**中文总结:** 提出 TEPHRA 方法论，用语义引导合成生成含各类障碍的无 bug 程序以系统评估 fuzzer 能力；对 31 个当代 fuzz 系统消耗 37.4 CPU 年评估，揭示浮点条件、字符串等共性盲区并发现 AFL++ 等 fuzzer 自身缺陷。

**Abstract:** Fuzz testing has proven effective in discovering non- trivial bugs in complex, real-world systems, with coverage-guided greybox fuzzing being a key contributor to this success. Existing research has largely focused on developing new heuristics to increase code coverage, and current benchmarks measure coverage increase or the number of bugs found. However, there is a notable lack of investigation into programming constructs that systematically hinder or prevent fuzzing heuristics from achieving coverage, commonly referred to as “obstacles” or “roadblocks”.

This work makes two key contributions. First, we introduce TEPHRA, a principled methodology that uses semantics-guided synthesis to generate bug-free programs with diverse obstacles and evaluate a fuzzer’s ability to overcome them. Second, we use TEPHRA to generate obstacles and empirically evaluate 31 contemporary fuzzing systems, consuming 37.4 CPU years. Our analysis reveals limitations in current fuzzing heuristics and uncovers bugs in the fuzzers themselves, including AFL++. All evaluated fuzzers struggle with certain obstacles, such as floating- point conditionals and character strings. We also find that signed integers are more challenging than unsigned, and some heuristics are overtuned for 32- and 64-bit types, neglecting 8- and 16- bit integers. Overall, we observe a single difficult construct can significantly degrade a fuzzer’s performance.


## 19. Understanding Software Engineering Agents: A Study of Thought-Action-Result Trajectories

**Authors:** Islem BOUZENIA (University of Stuttgart), Michael Pradel (CISPA Helmholtz Center for Information Security)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334353

**中文总结:** 统一 RepairAgent、AutoCodeRover、OpenHands 的 thought-action-result 轨迹（120 条轨迹、2822 次 LLM 交互）并做大规模实证；量化迭代、token 与动作模式，揭示推理连贯性与反馈整合等关键特征及失败模式。

**Abstract:** Large Language Model (LLM)-based agents are increasingly employed to automate complex software engineering tasks such as program repair and issue resolution. These agents operate by autonomously generating natural language thoughts, invoking external tools, and iteratively refining their solutions. Despite their widespread adoption, the internal decision-making processes of these agents remain largely unexplored, limiting our understanding of their operational dynamics and failure modes. In this paper, we present a large-scale empirical study of the thought-action-result trajectories of three state-of-the-art LLM-based agents: RepairAgent, AutoCodeRover, and OpenHands. We unify their interaction logs into a common format, capturing 120 trajectories and 2822 LLM interactions focused on program repair and issue resolution. Our study combines quantitative analyses of structural properties, action patterns, and token usage with qualitative assessments of reasoning coherence and feedback integration. We identify key trajectory characteristics such as iteration counts and token consumption, recurring action sequences, and the semantic coherence linking thoughts, actions, and their results. Our findings reveal behavioral motifs and anti-patterns that distinguish successful from failed executions, providing actionable insights for improving agent design, including prompting strategies, failure diagnosis, and anti-pattern detection. We release our dataset and annotation framework to support further research on transparent and robust autonomous software engineering agents.


## 20. WEST: Specification-Based Test Generation for WebAssembly

**Authors:** Dongjun Youn (KAIST), Shin Wonho (KAIST), Sukyoung Ryu (KAIST)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334667

**中文总结:** 提出 WEST，从 SpecTec 机械化 Wasm 规范自动生成符合语法/验证规则并覆盖执行语义的测试程序；可灵活适配完整或子集规范并集成多种测试生成策略，减轻运行时一致性测试的手工负担。

**Abstract:** WebAssembly (Wasm) is a low-level binary instruction format designed for safe and high-performance execution across diverse computing environments and runtimes. As Wasm evolves with new features and proposals, testing the correctness and conformance of Wasm runtimes has become increasingly complex. Manually constructing test suites is labor-intensive and difficult to scale, especially as the specification grows in complexity. While fuzzing-based approaches offer partial automation, they often lack a principled connection to the formal specification, and adapting to evolving or restricted subsets of the specification typically requires manual intervention.

In this paper, we present WEST, a specification-based test generation framework that automatically produces Wasm test cases from mechanized specifications written in SpecTec, a Wasm-specific specification language. Given any full or subset variant of the Wasm specification as input, WEST aims to systematically generate test programs that conform to the input grammar and validation rules, and capture the runtime behavior defined by its execution semantics. The framework allows flexible integration of different test generation strategies. For instance, we demonstrate both top-down and bottom-up approaches for generating Wasm modules, but the architecture is compatible with other generation techniques as well. The framework enables the creation of customized test cases for engines that support only subsets of the Wasm specification. We evaluate WEST across multiple specification variants and engine configurations, demonstrating that it produces valid and diverse test cases. As a result, it reveals 18 bugs across five Wasm engine implementations, 10 of which are confirmed and fixed. We believe that this work provides a solid foundation for future specification-driven test generation and fuzzing.


## 21. WingMuzz: Blackbox Testing of IoT Protocols via Two-dimensional Fuzzing Schedule

**Authors:** Xiaogang Zhu (Adelaide University), Enze Dai (Swinburne University of Technology), Xiaotao Feng (360 Vulnerability Research Institute), Shaohua Wang (Central University of Finance and Economics), Xin Xia (Zhejiang University), Sheng Wen (Swinburne University of Technology), Kwok-Yan Lam (Nanyang Technological University, Singapore), Yang Xiang (Digital Research & Innovation Capability Platform, Swinburne University of Technology)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334343

**中文总结:** 提出 WINGMUZZ，利用与 IoT 协议同规的开源实现的 greybox 覆盖率反馈指导闭源 IoT 协议黑盒 fuzz，采用二维调度（wingmate 选择与开源侧覆盖引导）；提升无源码 IoT 协议 fuzz 的有效反馈与探索效率。

**Abstract:** The Internet of Things (IoT) is widely used in various sectors but is often prone to vulnerabilities. With the proprietary nature of IoT devices, their source code and firmware are frequently unavailable for open review, rendering blackbox fuzzing a viable approach. However, the effectiveness of blackbox fuzzing is often challenging due to the lack of feedback, especially the information of code coverage. In this paper, we propose WINGMUZZ to provide blackbox fuzzing of IoT protocols with effective feedback. The key is to guide blackbox fuzzing by utilizing runtime information from greybox fuzzing on counterpart open-source code. This is based on our observation that IoT protocols and open-source code conform to the same specifications, indicating that inputs exploring different code regions on open-source code may also discover new coverage on IoT protocols. WINGMUZZ uses a two-dimensional fuzzing schedule to optimize the process of fuzzing IoT protocols. The first dimension involves scheduling open-source implementations, referred to as wingmates, so that similar ones are preferred to guide blackbox fuzzing. The second dimension utilizes coverage-guided greybox fuzzing to test open-source code. This solution can bridge the performance gap between blackbox fuzzing and greybox fuzzing on IoT protocols. We evaluate the performance of WINGMUZZ across eight IoT protocols and compare it with six widely-used blackbox fuzzers. On average, WINGMUZZ can discover 42.1%, 26.92%, 25.01%, 34.95%, 23.56% and 11.63% more edges than Boofuzz, Spike, Peach, SNIPUZZ, Pulsar and ChatAFL, respectively. Additionally, WINGMUZZ exposes 10 bugs in IoT protocols while other fuzzers expose no more than 3 bugs. It also exposes 2 new protocol vulnerabilities in IoT devices while other fuzzers cannot identify any.

