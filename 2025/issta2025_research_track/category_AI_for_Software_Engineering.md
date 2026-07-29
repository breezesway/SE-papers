# ISSTA 2025 Research Track — AI for Software Engineering

Source: https://conf.researchr.org/track/issta-2025/issta-2025-papers#event-overview

Count: 11

## 1. AdverIntent-Agent: Adversarial Reasoning for Repair Based on Inferred Program Intent

**Authors:** He Ye (University College London (UCL)), Aidan Z.H. Yang (Carnegie Mellon University), Chang Hu (Macau University of Science and Technology), Yanlin Wang (Sun Yat-sen University), Tao Zhang (Macau University of Science and Technology), Claire Le Goues (Carnegie Mellon University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728939

**中文总结:** 提出多智能体自动修复框架 AdverIntent-Agent：推理智能体生成互斥的程序意图，测试智能体为各意图构造对抗性测试，修复智能体再生成满足意图与测试的补丁，以缓解仅依赖不完整测试套件导致的过拟合。在 Defects4J 2.0 与 HumanEval-Java 上分别正确修复 83 与 121 个 bug，非过拟合正确率达 53.5% 与 82.9%，均为最优。

**Abstract:** Automated program repair (APR) has shown promising results, particularly with the use of neural networks. Currently, most APR tools focus on code transformations specified by test suites, rather than reasoning about the program’s intent and the high-level bug specification. Without a proper understanding of program intent, these tools tend to generate patches that overfit incomplete test suites and fail to reflect the developer’s intentions. However, reasoning about program intent is challenging. In our work, we propose an approach called AdverIntent-Agent, based on critique and adversarial reasoning. Our approach is novel to shift the focus from generating multiple APR patches to inferring multiple potential program intents. Each intent is adversarial to the others, ensuring at least one aligns closely with the developer’s original intent. AdverIntent-Agent is a multi-agent approach consisting of three agents: a reasoning agent, a test agent, and a repair agent. First, the reasoning agent generates adversarial program intents along with the corresponding faulty statements. Next, the test agent produces adversarial test cases that align with each inferred intent, constructing oracles that use the same inputs but have different expected outputs. Finally, the repair agent uses dynamic and precise LLM prompts to generate patches that satisfy both the inferred program intent and the generated tests. In this setting, each individual program intent provides ground-truth oracles that help eliminate overfitting patches. AdverIntent-Agent was evaluated on two benchmarks: Defects4J 2.0 and HumanEval-Java. AdverIntent- Agent correctly repaired the most number of bugs, 83 and 121 bugs, and achieved the highest correct (i.e. non-overfitting) rates 53.5% and 82.9% in both benchmarks, respectively. Compared to related work, AdverIntent-Agent uniquely repaired 21 and 4 bugs in two benchmarks, that had not been addressed by previous approaches, thanks to its adversarial reasoning and diversity exploration. Our work suggests a shift in developer interaction on patch acceptance by offering a comprehensive package of program intent, tests, and patches.

## 2. Can LLMs replace Human Evaluators? An Empirical Study of LLM-as-a-Judge in Software Engineering Tasks

**Authors:** Ruiqi Wang (Harbin Institute of Technology, Shenzhen), Jiyu Guo (Harbin Institute of Technology, Shenzhen), Cuiyun Gao (Harbin Institute of Technology), Guodong Fan (Shandong Agriculture and Engineering University), Chun Yong Chong (Huawei), Xin Xia (Zhejiang University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728963

**中文总结:** 在代码翻译、生成与摘要三类 SE 任务上，实证比较 7 种通用 LLM-as-a-judge 与 2 个微调评测模型相对人工评分的一致性。output-based 方法在代码翻译/生成上 Pearson 相关达 81.32/68.51，明显优于 ChrF++ 等传统指标，表明当前 SOTA LLM 评判在部分 SE 评测场景可接近甚至替代人工。

**Abstract:** Recently, large language models (LLMs) have been deployed to tackle various software engineering (SE) tasks like code generation, significantly advancing the automation of SE tasks. However, assessing the quality of these LLM-generated code and text remains challenging. The commonly used Pass@k metric necessitates extensive unit tests and configured environments, demands a high labor cost, and is not suitable for evaluating LLM-generated text. Conventional metrics like BLEU, which measure only lexical rather than semantic similarity, have also come under scrutiny. In response, a new trend has emerged to employ LLMs for automated evaluation, known as LLM-as-a-judge. These LLM-as-a-judge methods are claimed to better mimic human assessment than conventional metrics without relying on high-quality reference answers. Nevertheless, their exact human alignment in SE tasks remains unexplored.

In this paper, we empirically explore LLM-as-a-judge methods for evaluating SE tasks, focusing on their alignment with human judgments. We select seven LLM-as-a-judge methods that utilize general-purpose LLMs, alongside two LLMs specifically fine-tuned for evaluation. After generating and manually scoring LLM responses on three recent SE datasets of code translation, code generation, and code summarization, we then prompt these methods to evaluate each response. Finally, we compare the scores generated by these methods with human evaluation. The results indicate that output-based methods reach the highest Pearson correlation of 81.32 and 68.51 with human scores in code translation and generation, achieving near-human evaluation, noticeably outperforming ChrF++, one of the best conventional metrics, at 34.23 and 64.92. Such output-based methods prompt LLMs to output judgments directly, and exhibit more balanced score distributions that resemble human score patterns. Finally, we provide insights and implications, concluding that current state-of-the-art LLM-as-a-judge methods can potentially replace human evaluations in certain SE tasks.

## 3. Causality-Aided Evaluation and Explanation of Large Language Model-based Code Generation

**Authors:** Zhenlan Ji (The Hong Kong University of Science and Technology), Pingchuan Ma (HKUST), Li Zongjie (Hong Kong University of Science and Technology), Zhaoyu Wang (HKUST), Shuai Wang (Hong Kong University of Science and Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728938

**中文总结:** 提出基于因果图的 LLM 代码生成评估与解释框架，在细粒度可理解概念上刻画 prompt 与生成代码的因果关系，以应对 LLM 黑盒不透明带来的质量评估难题。对 3 个流行 LLM 与 12 余种 prompt 调整策略的分析表明，该方法可解释模型行为，并通过 prompt 校准提升生成代码质量。

**Abstract:** While code generation has been widely used in various software development scenarios, the quality of the generated code is not guaranteed. This has been a particular concern in the era of large language models (LLMs)-based code generation, where LLMs, deemed a complex and powerful black-box model, are instructed by a high-level natural language specification, namely a prompt, to generate code. Nevertheless, effectively evaluating and explaining the code generation capability of LLMs is inherently challenging, given the complexity of LLMs and the lack of transparency.

Inspired by the recent progress in causality analysis and its application in software engineering, this paper launches a causality analysis-based approach to systematically analyze the causal relations between the LLM input prompts and the generated code. To handle various technical challenges in this study, we first propose a novel causal graph-based representation of the prompt and the generated code, which is established over the fine-grained, human-understandable concepts in the input prompts. The formed causal graph is then used to identify the causal relations between the prompt and the derived code. We illustrate the insights that our framework can provide by studying over three popular LLMs with over 12 prompt adjustment strategies. The results of these studies illustrate the potential of our technique to provide insights into LLM effectiveness, and aid end-users in understanding predictions. Additionally, we demonstrate that our approach provides actionable insights to improve the quality of the LLM-generated code by properly calibrating the prompt.

## 4. ClassEval-T: Evaluating Large Language Models in Class-Level Code Translation

**Authors:** Pengyu Xue (Shandong University), Linhao Wu (Shandong University), Zhen Yang (Shandong University), Chengyi Wang (Shandong University), Xiang Li (Shandong University), Yuxiang Zhang (Shandong University), Jia Li (Tsinghua University), Ruikai Jin (Shandong University), Yifei Pei (Shandong University), Zhaoyan Shen (Shandong University), Xiran Lyu (Shandong University), Jacky Keung (City University of Hong Kong)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728940

**中文总结:** 作者基于 ClassEval 构建类级代码翻译基准 ClassEval-T，手工将 Python 样本迁移到 Java 与 C++ 并配套测试，比较 holistic、min-dependency、standalone 三种翻译策略下 8 个 LLM 的表现。实验显示类级翻译相较方法级基准性能显著下降且模型差异明显，并对 1243 个失败案例做了系统分类。

**Abstract:** In recent years, Large Language Models (LLMs) have dramatically advanced the performance of automated code translation, making their computational accuracy score reach up to over 80% on many previous benchmarks. However, most code samples in these benchmarks are short, standalone, statement/method-level, and algorithmic, which is not aligned with practical coding tasks. Therefore, it is still unknown the actual capability of LLMs in translating code samples written for daily development.

To achieve this, we construct a class-level code translation benchmark, ClassEval-T, and make the first attempt to extensively assess recent LLMs’ performance on class-level code translation. ClassEval-T is extended from ClassEval, a well-known class-level Python code generation benchmark consisting of multiple practical coding topics, such as database operation and game design, and diverse contextual dependencies (e.g., fields, methods, and libraries). It cost us 360 person-hours to accomplish the manual migration to Java and C++ with complete code samples and associated test suites. Subsequently, we design three translation strategies (i.e., holistic, min-dependency, and standalone) for class-level code translations and evaluate eight recent LLMs of commercial, general, and code kinds in diverse families and sizes on ClassEval-T. Experimental results demonstrate a remarkable performance drop compared with the most widely studied method-level code translation benchmark, and obvious discrepancies among LLMs appear, showing the effectiveness of ClassEval-T in measuring recent LLMs. Afterwards, we further discuss the usage scenarios for diverse translation strategies and LLMs’ ability to dependency awareness when translating class samples. Finally, 1,243 failure cases made by the best-performing LLM under test are thoroughly analyzed and categorized in this paper for practical guidance and future enlightenment.

## 5. ConTested: Consistency-Aided Tested Code Generation with LLM

**Authors:** Jinhao Dong (Peking University), Jun Sun (Singapore Management University), Wenjie Zhang (National University of Singapore), Jin Song Dong (National University of Singapore), Dan Hao (Peking University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728902

**中文总结:** 针对 LLM 生成测试不可靠导致 consistency 投票失效的问题，提出 ConTested：以少量用户反馈引导 rank-correct-fix 协同演化，迭代提升代码与测试质量。在 GPT-3.5/GPT-4o 上分别提升 32.9%/16.97%，4 轮交互即优于 MPSC 等后处理 SOTA。

**Abstract:** Recent advancements in large language models (LLMs) have significantly improved code generation, which generates code snippets automatically based on natural language requirements. Despite achieving state-of-the-art performance, LLMs often struggle to generate accurate and reliable code, requiring developers to spend substantial effort debugging and evaluating the generated output. Researchers have proposed leveraging Consistency to select code that passes more tests (inter-consistency) and demonstrates consistent behavior across more counterparts (intra-consistency). However, since the tests themselves are also generated by LLMs, relying on majority voting based on incorrect tests leads to unreliable results. To address this, we propose a lightweight interaction framework that incorporates user feedback to effectively guide consistency. Our results demonstrate that, with minimal human effort, performance can be significantly improved. In each iteration, we introduce a rank-correct-fix co-evolution process between code and tests. This process iteratively enhances the quality of both, making the consistency voting between code and tests more reliable.

We evaluate ConTested through extensive experiments, demonstrating its effectiveness across multiple LLMs, including GPT-3.5 and GPT-4o. Our results show improvements of 32.9% over GPT-3.5 and 16.97% over GPT-4o. Additionally, ConTested achieves an 11.1% improvement over the SOTA post-processing technique, MPSC. This improvement is achieved with only a 4-round interaction with users, requiring minimal user effort. A user study further confirms the feasibility and cost-effectiveness of ConTested, highlighting its ability to enhance code generation without introducing substantial overhead.

## 6. Enhanced Prompting Framework for Code Summarization with Large Language Models

**Authors:** Minying Fang (Qingdao University of Science and Technology), Xing Yuan (Qingdao University of Science and Technology), Yuying Li (Qingdao University of Science and Technology), Haojie Li (Qingdao University of Science and Technology), Chunrong Fang (Nanjing University), Junwei Du (Qingdao University of Science and Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728949

**中文总结:** EP4CS 结合连续提示优化的 Mapper 与解析程序结构的 Struct-Agent，缓解 LLM 在代码摘要任务上的语义对齐不足。BLEU、METEOR、ROUGE-L 分别提升 4.45%、3.77%、10.32%。

**Abstract:** Code summarization is essential for enhancing the efficiency of software development, enabling developers to swiftly comprehend and maintain software projects.  Recent efforts utilizing large language models (LLMs) for generating precise code summaries have shown promising performance, primarily due to their advanced generative capabilities.  LLMs that employ continuous prompting techniques can explore a broader problem space, potentially unlocking greater capabilities.  However, they also present specific challenges, particularly in aligning with task-specific situations—a strength of discrete prompts.  Additionally, the inherent differences between programming languages and natural languages can complicate comprehension for LLMs, impacting the accuracy and relevance of the summaries in complex programming scenarios.  These challenges may result in outputs that do not align with actual task needs, underscoring the necessity for further research to enhance the effectiveness of LLMs in code summarization. To address these limitations, we propose an enhanced prompting framework for Code Summarization with Large Language Models(EP4CS). Firstly, we design \textit{\textbf{Mapper}}, which undergoes pre-training on code corpora and facilitates the optimization and updating of prompt vectors based on the outputs of LLMs. Additionally, we developed a \textit{\textbf{Struct-Agent}} that enables LLMs to more accurately interpret the complex semantic structures of programming languages by in-depth analysis of their syntax and structural characteristics. Experimental results indicate that, compared to existing baseline methods, our enhanced prompting learning framework significantly improves performance while maintaining the same parameter scale. Specifically, our framework improves scores by 4.45%, 3.77%, and 10.32% on the standard machine translation evaluation metrics BLEU, METEOR, and ROUGE-L, respectively.

## 7. LLM4SZZ: Enhancing SZZ Algorithm with Context-Enhanced Assessment on Large Language Models

**Authors:** Lingxiao Tang (Zhejiang University), Jiakun Liu (Singapore Management University), Zhongxin Liu (Zhejiang University), Xiaohu Yang (Zhejiang University), Lingfeng Bao (Zhejiang University)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728885

**中文总结:** LLM4SZZ 结合 rank-based 与 context-enhanced 两种 LLM 策略定位 bug-inducing commit，并利用 commit message 与补丁上下文弥补传统 SZZ 变体不足。三个数据集上 F1 提升 8.9%–16.4% 且 recall 未显著下降，还能发现基线漏检的 2.5%–7.8% 诱导提交。

**Abstract:** The SZZ algorithm is the dominant technique for identifying bug-inducing commits and serves as a foundation for many software engineering studies, such as bug prediction and static code analysis, thereby enhancing software quality and facilitating better maintenance practices. Researchers have proposed many variants to enhance the SZZ algorithm’s performance since its introduction. The majority of them rely on static techniques or heuristic assumptions, making them easy to implement, but their performance improvements are often limited. Recently, a deep learning-based SZZ algorithm has been introduced to enhance the original SZZ algorithm performance. However, it requires complex preprocessing and is restricted to a single programming language. Additionally, while it enhances precision, it sacrifices recall. Furthermore, most of variants overlook crucial information, such as commit messages and patch context, and are limited to bug-fixing commits involving deleted lines.

The emergence of large language models (LLMs) offers an opportunity to address these drawbacks. In this study, we investigate the strengths and limitations of LLMs and propose LLM4SZZ, which employs two approaches (i.e., rank-based identification and context-enhanced identification) to handle different types of bug-fixing commits. We determine which approach to adopt based on the LLM’s ability to comprehend the bug and identify whether the bug is present in a commit. The context-enhanced identification provides the LLM with more context and requires it to find the bug-inducing commit among a set of candidate commits. In rank-based identification, we ask the LLM to select buggy statements from the bug-fixing commit and rank them based on their relevance to the root cause.  Experimental results show that LLM4SZZ outperforms all baselines across three datasets, improving F1-score by 8.9% to 16.4% without significantly sacrificing recall. Additionally, LLM4SZZ can identify many bug-inducing commits that the baselines fail to detect, accounting for 7.8%, 7.4% and 2.5% of the total bug-inducing commits across three datasets, respectively.

## 8. LLM Hallucinations in Practical Code Generation: Phenomena, Mechanism, and Mitigation

**Authors:** Ziyao Zhang (Sun Yat-sen University), Chong Wang (Nanyang Technological University), Yanlin Wang (Sun Yat-sen University), Ensheng Shi (Xi’an Jiaotong University), Yuchi Ma (Huawei Cloud Computing Technologies), Wanjun Zhong (Sun Yat-sen University), Jiachi Chen (Sun Yat-sen University), Mingzhi Mao (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728894

**中文总结:** 在仓库级代码生成场景下，对六种主流 LLM 的 hallucination 做实证：建立分类体系、分析分布与四类成因，并提出 RAG 缓解方案。RAG 对所有被测模型均有一致改善，Replication package 已公开。

**Abstract:** Code generation aims to automatically generate code from input requirements, significantly enhancing development efficiency. Recent large language models (LLMs) based approaches have shown promising results and revolutionized code generation task. Despite the promising performance, LLMs often generate contents with hallucinations, especially for the code generation scenario requiring the handling of complex contextual dependencies in practical development process. Although previous study has analyzed hallucinations in LLM-powered code generation, the study is limited to standalone function generation. In this paper, we conduct an empirical study to study the phenomena, mechanism, and mitigation of LLM hallucinations within more practical and complex development contexts in repository-level generation scenario. First, we manually examine the code generation results from six mainstream LLMs to establish a hallucination taxonomy of LLM- generated code. Next, we elaborate on the phenomenon of hallucinations, analyze their distribution across different models. We then analyze causes of hallucinations and identify four potential factors contributing to hallucinations. Finally, we propose an RAG-based mitigation method, which demonstrates consistent effectiveness in all studied LLMs. The replication package including code, data, and experimental results is anonymously available at https://anonymous.4open.science/r/LLMCodingHallucination/ .

## 9. OmniGIRL: A Multilingual and Multimodal Benchmark for GitHub Issue Resolution

**Authors:** Lianghong Guo (Sun Yat-sen University), Wei Tao (Independent Researcher), Runhan Jiang (Sun Yat-sen University), Yanlin Wang (Sun Yat-sen University), Jiachi Chen (Sun Yat-sen University), Xilin Liu (Huawei Cloud), Yuchi Ma (Huawei Cloud Computing Technologies), Mingzhi Mao (Sun Yat-sen University), Hongyu Zhang (Chongqing University), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728871

**中文总结:** 构建多语言、多模态、多领域 GitHub Issue 解决基准 OmniGIRL，含959个任务实例，覆盖 Python、JavaScript、TypeScript、Java 及8个领域。当前 LLM 表现有限：GPT-4o 仅解决8.6%问题，含图像 issue 上 Claude-3.5-Sonnet 最高仅10.5%。

**Abstract:** The GitHub issue resolution task aims to resolve issues reported in repositories automatically. With advances in large language models (LLMs), this task has gained increasing attention, and several benchmarks are proposed to evaluate the issue resolution ability of LLMs. However, existing benchmarks have three main limitations. First, current benchmarks focus on a single programming language, limiting the evaluation of issues from repositories across different languages. Second, they usually cover a narrow range of domains, which may fail to represent the diversity of real-world issues. Third, existing benchmarks rely solely on textual information in issue descriptions, overlooking multimodal information such as images in issues. In this paper, we propose OmniGIRL, a GitHub Issue ResoLution benchmark that is multilingual, multimodal, and multi-domain. OmniGIRL includes 959 task instances, which are collected from repositories across four programming languages (i.e., Python, JavaScript, TypeScript, and Java) and eight different domains. Our evaluation shows that current LLMs show limited performances on OmniGIRL. Notably, the best-performing model, GPT-4o, resolves only 8.6% of the issues. Besides, we find that current LLMs struggle to resolve issues requiring understanding images. The best performance is achieved by Claude-3.5-Sonnet, which resolves only 10.5% of the issues with image information. Finally, we analyze the reasons behind current LLMs’ failure on OmniGIRL, providing insights for future improvements.

## 10. The First Prompt Counts the Most! An Evaluation of Large Language Models on Iterative Example-based Code Generation

**Authors:** Yingjie Fu (Peking University), Bozhou Li (Peking University), Linyi Li (Simon Fraser University), Wentao Zhang (Peking University), Tao Xie (Peking University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728947

**中文总结:** 首次大规模评估 LLM 基于迭代 I/O 示例的代码生成能力；相较自然语言描述，模型得分下降超 60%，且 95% 以上成功实现的功能均在第一轮完成，说明 LLM 难以有效利用后续补充示例。结合（即使不精确的）自然语言可显著提升表现，初始示例选择对部分功能高度敏感。

**Abstract:** The capabilities of Large Language Models (LLMs) in code generation, particularly for implementing target functionalities from natural language descriptions, have been extensively studied. As an alternative form of natural language, input-output examples (I/O examples) provide an accessible, unambiguous, and flexible way to describe functionalities, but the diversity, sparseness, and incompleteness of I/O examples also place challenges on understanding and implementing requirements. Therefore, generating code from input-output examples (i.e., example-based code generation) provides a new perspective, allowing us to evaluate LLMs’ capability to infer target functionalities from limited information and to process new-form requirements. However, related research about LLMs in example-based code generation remains largely unexplored. To fill this gap, this paper presents the first comprehensive study on example-based code generation using LLMs. To address the incorrectness caused by the incompleteness of I/O examples, we adopt an iterative evaluation framework and formalize the objective of example-based code generation as two sequential sub-objectives: generating code conforming to given examples and generating code that successfully implements the target functionalities from (iteratively) given examples. We assess six state-of-the-art LLMs using a new benchmark of 168 diverse target functionalities (derived from HumanEval and CodeHunt). The results demonstrate that when requirements were described using iterative input-output examples rather than natural language, the LLMs’ score decreased by over 60%, indicating that example-based code generation remains challenging for the evaluated LLMs. More interestingly, the vast majority (even over 95%) of successfully implemented functionalities are achieved in the first round of iterations, suggesting that the LLMs struggle to effectively utilize the iteratively supplemented requirements. Furthermore, we find that combining I/O examples with even imprecise natural language descriptions significantly improves LLM performance, and that while the choice of initial I/O examples has a limited impact on the score for most functionalities, a subset of functionalities shows high sensitivity to the initial examples, suggesting opportunities for prompt optimization. These findings highlight the importance of early prompts during interactions and offer critical insights and implications for enhancing LLM-driven code generation.

## 11. VerLog: Enhancing Release Note Generation for Android Apps using Large Language Models

**Authors:** Jiawei Guo (University at Buffalo, SUNY), Haoran Yang (Washington State University), Haipeng Cai (University at Buffalo, SUNY)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728961

**中文总结:** VerLog 以 few-shot 自适应提示激发 LLM 图推理能力，融合细粒度代码变更与高阶非代码工件生成 Android 发布说明。在 248 个应用的 42 次发布上，precision/recall/F1 较基线提升 18%–21%，完整性与可读性显著更好。

**Abstract:** Release notes are essential documents that communicate the details of software updates to users and developers, yet their generation remains a time-consuming and error-prone process. In this paper, we present VerLog, a novel technique that enhances the generation of software release notes using Large Language Models (LLMs). VerLog leverages few-shot in-context learning with adaptive prompting to facilitate the graph reasoning capabilities of LLMs, enabling them to accurately interpret and document the semantic information of code changes. Additionally, VerLog incorporates multi-granularity information, including fine-grained code modifications and high-level non-code artifacts, to guide the generation process and ensure comprehensive, accurate, and readable release notes. We applied VerLog to the 42 releases of 248 unique Android applications and conducted extensive evaluations. Our results demonstrate that VerLog significantly (up to 18%–21% higher precision, recall, and F1) outperforms state-of-the-art baselines in terms of completeness, accuracy, readability, and overall quality of the generated release notes, in both controlled experiments with high-quality reference release notes and in-the-wild evaluations.
