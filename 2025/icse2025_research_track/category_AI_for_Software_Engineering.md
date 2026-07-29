# ICSE 2025 Research Track — AI for Software Engineering

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 102 papers

## 1. 3DGen: AI-Assisted Generation of Provably Correct Binary Format Parsers

**Authors:** Sarah Fakhoury (Microsoft Research), Markus Kuppe (Microsoft Research), Shuvendu K. Lahiri (Microsoft Research), Tahina Ramananandro (Microsoft Research), Nikhil Swamy (Microsoft Research)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029881

**中文总结:** 提出 3DGen 框架，用 AI 智能体将自然语言文档与示例输入转化为 3D 形式化格式规范，并结合符号测试生成与迭代 refinement 生成可证明正确的二进制解析器。

**Abstract:** Improper parsing of attacker-controlled input is a leading source of software security vulnerabilities, especially when programmers transcribe informal format descriptions into efficient parsing logic in low-level, memory unsafe languages. Several researchers have proposed formal specification languages for data formats from which efficient code can be extracted. However, distilling informal requirements into formal specifications is challenging and, despite their benefits, new, formal languages are hard for people to learn and use. In this work, we present 3DGen, a framework that makes use of AI agents to transform mixed informal input, including natural language documents and example inputs into format specifications in a language called 3D. To support humans in understanding and trusting the generated specifications, 3DGen uses symbolic methods to also synthesize test inputs that can be validated against an external oracle. Symbolic test generation also helps in distinguishing multiple plausible solutions. Through a process of repeated refinement, 3DGen produces a 3D specification that conforms to a test suite, and which yields safe, efficient, provably correct, parsing code in C. We have evaluated 3DGen on 20 Internet standard formats, demonstrating the potential for AI-agents to produce formally verified C code at a non-trivial scale. A key enabler is the use of a domain-specific language to limit AI outputs to a class for which automated, symbolic analysis is tractable.

## 2. A First Look at Conventional Commits Classification

**Authors:** Qunhong Zeng (Beijing Institute of Technology), Yuxia Zhang (Beijing Institute of Technology), Zhiqing Qiu (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029726

**中文总结:** 初步研究 Conventional Commits 规范在 GitHub 上的采用现状与问题，并探索自动细粒度提交分类以填补相对 Swanson 三分类的知识空白。

**Abstract:** Modern distributed software development relies on commits to control system versions. Commit classification plays a vital role in both industry and academia. The widely-used commit classification framework was proposed in 1976 by Swanson and includes three base classes: perfective, corrective, and adaptive. With the increasing complexity of software development, the industry has shifted towards a more fine-grained commit category, i.e., adopting Conventional Commits Specification (CCS) for delicacy management. The new commit framework requires developers to classify commits into ten distinct categories, such as ``feat'', ``fix'', and ``docs''. However, existing studies mainly focus on the three-category classification, leaving the definition and application of the fine-grained commit categories as knowledge gaps. This paper reports a preliminary study on this mechanism from its application status and problems. We also explore ways to address these identified problems. We find that a growing number of projects on GitHub are adopting CCS. By analyzing 194 issues from GitHub and 100 questions from Stack Overflow about the CCS application, we qualitatively categorized 52 challenges developers encountered. The most common one is CCS-type confusion. To address these challenges, we propose a clear definition of CCS types based on existing variants. Further, we designed an approach to automatically classify commits into CCS types, and the evaluation results demonstrate a promising performance. Our work facilitates a deeper comprehension of the present fine-grained commit categorization and holds the potential to alleviate application challenges significantly.

## 3. A Multi-Agent Approach for REST API Testing with Semantic Graphs and LLM-Driven Inputs

**Authors:** Myeongsoo Kim (Georgia Institute of Technology), Tyler Stennett (Georgia Institute of Technology), Saurabh Sinha (IBM Research), Alessandro Orso (Georgia Institute of Technology)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029879

**中文总结:** 提出 AutoRestTest 黑盒 REST API 测试框架，以多智能体强化学习、语义属性依赖图与大语言模型协同优化接口探索与故障检测。

**Abstract:** As modern web services increasingly rely on REST APIs, their thorough testing has become crucial. Furthermore, the advent of REST API specifications such as OpenAPI ones has led to the emergence of many black-box REST API testing tools. However, these tools often focus on individual test elements in isolation (e.g., APIs, parameters, values), resulting in lower coverage and less effectiveness in detecting faults (i.e., 500 response codes). To address these limitations, we present AutoRestTest, the first black-box framework to adopt a dependency-embedded multi-agent approach for REST API testing, integrating Multi-Agent Reinforcement Learning (MARL) with a Semantic Property Dependency Graph (SPDG) and Large Language Models (LLMs). Our approach treats REST API testing as a separable problem, where four agents---API, dependency, parameter, and value---collaborate to optimize API exploration. LLMs handle domain-specific value restrictions, the SPDG model simplifies the search space for dependencies using a similarity score between API operations, and MARL dynamically optimizes the agents' behavior. Evaluated on 12 real-world REST services, AutoRestTest outperforms the four leading black-box REST API testing tools, including those assisted by RESTGPT (which augments realistic test inputs using LLMs), in terms of code coverage, operation coverage, and fault detection. Notably, AutoRestTest is the only tool able to identify an internal server error in Spotify. Our ablation study underscores the significant contributions of the agent learning, SPDG, and LLM components.

## 4. A Multiple Representation Transformer with Optimized Abstract Syntax Tree for Efficient Code Clone Detection

**Authors:** TianChen Yu (School of Software Engineering, South China University of Technology), Li Yuan (School of Software Engineering, South China University of Technology, Guangzhou, China), Liannan Lin (School of Software Engineering, South China University of Technology), Hongkui He (School of Software Engineering, South China University of Technology)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029815

**中文总结:** 提出 MRT-OAST 代码克隆检测模型，剪枝优化 AST 并以前序/后序遍历双表示输入 Transformer，结合 Siamese 网络与余弦相似度加速比对；Java/C++ AST 序列长度分别降至 40%/39%。

**Abstract:** Over the past decade, the application of deep learning in code clone detection has produced remarkable results. However, the current approaches have two limitations: (a) code representation approaches with low information utilization, such as vanilla Abstract Syntax Tree (AST), leading to information redundancy which results in performance degradation; (b) low efficiency of clone detection on evaluation, resulting in excessive time costs during practical use. In this paper, we propose a Multiple Representation Transformer with Optimized Abstract Syntax Tree (MRT-OAST) to introduce an efficient code representation method while achieving competitive performance. Specifically, MRT-OAST strategically prunes and enhances the AST, utilizing both pre-order and post-order traversals to represent two different representations. To speed up the evaluation process, MRT-OAST utilizes a pure Siamese network and employs cosine similarity to compare the similarity between codes. Our approach effectively reduces AST sequences to 40% and 39% of their original length in Java and C/C++ while preserving structural information. In code clone detection tasks, our model surpasses state-of-the-art approaches on OJClone and Google Code Jam. During the evaluation of BigCloneBench, our model has a 5x speed improvement compared to the state-of-the-art lightweight model and a 563x speed improvement compared to the BERT-based model, with only a 0.3% and 0.9% decrease in $F_1$-score.

## 5. ADAMAS: Adaptive Domain-Aware Performance Anomaly Detection in Cloud Service Systems

**Authors:** Wenwei Gu (The Chinese University of Hong Kong), Jiazhen Gu (Chinese University of Hong Kong), Jinyang Liu (Chinese University of Hong Kong), Zhuangbin Chen (Sun Yat-sen University), Jianping Zhang (The Chinese University of Hong Kong), Jinxi Kuang (The Chinese University of Hong Kong), Cong Feng (Huawei Cloud Computing Technology), Yongqiang Yang (Huawei Cloud Computing Technology), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029821

**中文总结:** 提出 ADAMAS 自适应 AutoML 云性能异常检测框架，结合无监督模型搜索与轻量人机协同弥合技术告警与业务影响差距。

**Abstract:** A common practice in the reliability engineering of cloud services involves the collection of monitoring metrics, followed by comprehensive analysis to identify performance issues. However, existing methods often fall short of detecting diverse and evolving anomalies across different services. Moreover, there exists a significant gap between the technical and business interpretation of anomalies, i.e., a detected anomaly may not have an actual impact on system performance or user experience. To address these challenges, we propose ADAMAS, an adaptive AutoML-based anomaly detection framework aiming to achieve practical anomaly detection in production cloud systems. To improve the ability of detecting cross-service anomalies, we design a novel unsupervised evaluation function to facilitate the automatic searching of the optimal model structure and parameters. ADAMAS also contains a lightweight human-in-the-loop design, which can efficiently incorporate expert knowledge to adapt to the evolving anomaly patterns and bridge the gap between predicted anomalies and actual business exceptions. Furthermore, through monitoring the rate of mispredicted anomalies, ADAMAS proactively re-configures the optimal model, forming a continuous loop of system improvement. Extensive evaluation on one public and two industrial datasets shows that ADAMAS outperforms all baseline models with a 0.891 F1-score. The ablation study also proves the effectiveness of the evaluation function design and the incorporation of expert knowledge.

## 6. Aligning the Objective of LLM-based Program Repair

**Authors:** Junjielong Xu (The Chinese University of Hong Kong, Shenzhen), Ying Fu (Chongqing University), Shin Hwei Tan (Concordia University), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029731

**中文总结:** 提出 D4C 提示框架，将 LLM 程序修复对齐下一词预测训练目标并允许全程序级修补，无需预定位缺陷语句。

**Abstract:** Large language models (LLMs) have achieved decent results on automated program repair (APR). However, the next token prediction training objective of decoder-only LLMs (e.g., GPT-4) is misaligned with the masked span prediction objective of current infilling-style methods, which impedes LLMs from fully leveraging pre-trained knowledge for program repair. In addition, while some LLMs can locate and repair bugs in certain functions using the related artifacts (e.g., test cases), existing methods still depend on statement-level fault localization methods to provide a list of buggy hunks for repair. This restriction hinders LLMs from exploring potential patches beyond the given locations. In this paper, we investigate a new approach to adapt LLMs to program repair. Our core insight is that LLM’s APR capability can be greatly improved by simply aligning the output to their training objective and allowing them to refine the whole program without first identifying faulty statements. Based on this insight, we designed D4C, a straightforward prompting framework for APR. D4C can repair 180 bugs correctly in Defects4J, with each patch being sampled only 10 times. This surpasses the SOTA APR methods with perfect fault localization by 10% and reduces the patch sampling number by 90%. Our findings reveal that (1) objective alignment is crucial for fully exploiting LLM’s pre-trained capability, and (2) replacing the traditional localize-buggy-hunks-then-repair workflow with direct debugging is more effective for LLM-based APR methods. Thus, we believe this paper introduces a new mindset for harnessing LLMs in APR.

## 7. An Empirical Study on Automatically Detecting AI-Generated Source Code: How Far Are We?

**Authors:** Hyunjae Suh (University of California, Irvine), Mahan Tafreshipour (University of California at Irvine), Jiawei Li (University of California Irvine), Adithya Bhattiprolu (University of California, Irvine), Iftekhar Ahmed (University of California at Irvine)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029804

**中文总结:** 实证显示现有 AI 生成代码检测工具泛化性差；提出改进方法最佳 F1 达 82.55，显著优于 GPTSniffer。

**Abstract:** Artificial Intelligence (AI) techniques, especially Large Language Models (LLMs), have started gaining popularity among researchers and software developers for generating source code. However, LLMs have been shown to generate code with quality issues and also incurred copyright/licensing infringements. Therefore, detecting whether a piece of source code is written by humans or AI has become necessary. This study first presents an empirical analysis to investigate the effectiveness of the existing AI detection tools in detecting AI-generated code. The results show that they all perform poorly and lack sufficient generalizability to be practically deployed. Then, to improve the performance of AI-generated code detection, we propose a range of approaches, including fine-tuning the LLMs and machine learning-based classification with static code metrics or code embedding generated from Abstract Syntax Tree (AST). Our best model outperforms state-of-the-art AI-generated code detector (GPTSniffer) and achieves an F1 score of 82.55. We also conduct an ablation study on our best-performing model to investigate the impact of different source code features on its performance.

## 8. An Empirical Study on Commit Message Generation using LLMs via In-Context Learning

**Authors:** Yifan Wu (Peking University), Yunpeng Wang (Ant Group), Ying Li (School of Software and Microelectronics, Peking University, Beijing, China), Wei Tao (Independent Researcher), Siyu Yu (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Haowen Yang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Wei Jiang, Jianguo Li (Ant Group)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11029897

**中文总结:** 系统评估大语言模型结合上下文学习自动生成提交信息的能力，分析不同提示与示例设置对生成质量的影响。

**Abstract:** Commit messages concisely describe code changes in natural language and are important for software maintenance. Several approaches have been proposed to automatically generate commit messages, but they still suffer from critical limitations, such as time-consuming training and poor generalization ability. To tackle these limitations, we propose to borrow the weapon of large language models (LLMs) and in-context learning (ICL). Our intuition is based on the fact that the training corpora of LLMs contain extensive code changes and their pairwise commit messages, which makes LLMs capture the knowledge about commits, while ICL can exploit the knowledge hidden in the LLMs and enable them to perform downstream tasks without model tuning. However, it remains unclear how well LLMs perform on commit message generation via ICL. Therefore, in this paper, we conduct a comprehensive empirical study to investigate the capability of LLMs to generate commit messages via ICL. Specifically, we first explore the impact of different settings on the performance of ICL-based commit message generation. We then compare ICL-based commit message generation with state-of-the-art approaches on a popular multilingual dataset and a new dataset we created to mitigate potential data leakage. The results show that ICL-based commit message generation significantly outperforms state-of-the-art approaches on subjective evaluation and achieves better generalization ability. We further analyze the root causes for LLM’s underperformance and propose several implications, which shed light on future research directions for using LLMs to generate commit messages.

## 9. An Exploratory Study of ML Sketches and Visual Code Assistants

**Authors:** Luis F. Gomes (Carnegie Mellon University), Vincent J. Hellendoorn (Carnegie Mellon University), Jonathan Aldrich (Carnegie Mellon University), Rui Abreu (Faculty of Engineering of the University of Porto, Portugal)

**Categories:** AI for Software Engineering, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029898

**中文总结:** 探索 IDE 内视觉代码助手原型，对 19 名数据科学家开展实验，发现 ML 工作流草图中流程图（52.6%）最常用并评估草图转代码可行性。

**Abstract:** This paper explores the integration of Visual Code Assistants in Integrated Development Environments (IDEs). In Software Engineering, whiteboard sketching is often the initial step before coding, serving as a crucial collaboration tool for developers. Previous studies have investigated patterns in SE sketches and how they are used in practice, yet methods for directly using these sketches for code generation remain limited. The emergence of visually-equipped large language models presents an opportunity to bridge this gap, which is the focus of our research. In this paper, we built a first prototype of a Visual Code Assistant to get user feedback regarding in-IDE sketch-to-code tools. We conduct an experiment with 19 data scientists, most of whom regularly sketch as part of their job. We investigate developers' mental models by analyzing patterns commonly observed in their sketches when developing an ML workflow. Analysis indicates that diagrams were the preferred organizational component (52.6\%), often accompanied by lists (42.1\%) and numbered points (36.8\%). Our tool converts their sketches into a Python notebook by querying an LLM. We use an LLM-as-judge setup to score the quality of the generated code, finding that even brief sketching can effectively generate useful code outlines. We also find a significant, positive correlation between sketch time and the quality of the generated code. We conclude the study by conducting extensive interviews to assess the tool's usefulness, explore potential use cases, and understand developers' needs. As noted by participants, promising applications for these assistants include education, prototyping, and collaborative settings. Our findings signal promise for the next generation of Code Assistants to integrate visual information, both to improve code generation and to better leverage developers' existing sketching practices.

## 10. An LLM-Based Agent-Oriented Approach for Automated Code Design Issue Localization

**Authors:** Fraol Batole (Tulane University), David OBrien (Iowa State University), Tien N. Nguyen (University of Texas at Dallas), Robert Dyer (University of Nebraska-Lincoln), Hridesh Rajan (Tulane University)

**Categories:** AI for Software Engineering, Architecture and Design

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029742

**中文总结:** 提出 LOCALIZEAGENT 多智能体框架，将程序分析输出转为 LLM 可理解的抽象表示并协同定位模块化差、复杂度过高等设计问题，克服大代码库超出上下文窗口的局限。

**Abstract:** Maintaining software design quality is crucial for the long-term maintainability and evolution of systems. However, design issues such as poor modularity and excessive complexity often emerge as codebases grow. Developers rely on external tools, such as program analysis techniques, to identify such issues. This work investigates an automated approach for analyzing and localizing design issues using Large Language Models (LLMs). Large language models have demonstrated significant performance on coding tasks, but directly leveraging them for design issue localization is challenging. Large codebases exceed typical LLM context windows, and program analysis tool outputs in non-textual modalities (e.g., graphs or interactive visualizations) are incompatible with LLMs’ natural language inputs. To address these challenges, we propose LOCALIZEAGENT, a novel multi-agent framework for effective design issue localization. LOCALIZEAGENT integrates specialized agents that (1) analyze code to identify potential code design issues, (2) transform program analysis outputs into abstraction-aware LLM-friendly natural language summaries, (3) generate context-aware prompts tailored to specific refactoring types, and (4) leverage LLMs to locate and rank the localized issues based on their relevance. Our evaluation using diverse real-world codebases demonstrates significant improvements over baseline approaches, with LOCALIZEAGENT achieving 138%, 166%, and 206% relative improvements in exact match accuracy for localizing information hiding, complexity, and modularity issues, respectively.

## 11. Are We Learning the Right Features? A Framework for Evaluating DL-Based Software Vulnerability Detection Solutions

**Authors:** Satyaki Das (University of Southern California), Syeda Tasnim Fabiha (University of Southern California), Saad Shafiq (University of Southern California), Nenad Medvidović (University of Southern California)

**Categories:** AI for Software Engineering, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029773

**中文总结:** 提出评估深度学习漏洞检测方法的统一框架，通过特征保留与特征消除两类代码扰动区分真实漏洞特征与伪相关特征，为可复现、可信的评测奠定基础。

**Abstract:** Recent research has revealed that the reported results of an emerging body of deep learning-based techniques for detecting software vulnerabilities are not reproducible, either across different datasets or on unseen samples. This paper aims to provide the foundation for properly evaluating the research in this domain. We do so by analyzing prior work and existing vulnerability datasets for the syntactic and semantic features of code that contribute to vulnerability, as well as features that falsely correlate with vulnerability. We provide a novel, uniform representation to capture both sets of features, and use this representation to detect the presence of both vulnerability and spurious features in code. To this end, we design two types of code perturbations: feature preserving perturbations (FPP) ensure that the vulnerability feature remains in a given code sample, while feature eliminating perturbations (FEP) eliminate the feature from the code sample. These perturbations aim to measure the influence of spurious and vulnerability features on the predictions of a given vulnerability detection solution. To evaluate how the two classes of perturbations influence predictions, we conducted a large-scale empirical study on five state-of-the-art DL-based vulnerability detectors. Our study shows that, for vulnerability features, only ~2% of FPPs yield the undesirable effect of a prediction changing among the five detectors on average. However, on average, ~84% of FEPs yield the undesirable effect of retaining the vulnerability predictions. For spurious features, we observed that FPPs yielded a drop in recall up to 29% for graph-based detectors. We present the reasons underlying these results and suggest strategies for improving DNN-based vulnerability detectors. We provide our perturbation-based evaluation framework as a public resource to enable independent future evaluation of vulnerability detectors.

## 12. Automated Generation of Accessibility Test Reports from Recorded User Transcripts

**Authors:** Syed Fatiul Huq (University of California, Irvine), Mahan Tafreshipour (University of California at Irvine), Kate Kalcevich (Fable Tech Labs Inc.), Sam Malek (University of California at Irvine)

**Categories:** AI for Software Engineering, Human and Social Aspects

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029798

**中文总结:** 提出 Reca11，利用 GPT-4 等 LLM 从无障碍用户测试录音转写中自动提取可访问性与可用性问题，简化测试报告生成。

**Abstract:** Testing for accessibility is a significant step when developing software, as it ensures that all users, including those with disabilities, can effectively engage with web and mobile applications. While automated tools exist to detect accessibility issues in software, none are as comprehensive and effective as the process of user testing, where testers with various disabilities evaluate the application for accessibility and usability issues. However, user testing is not popular with software developers as it requires conducting lengthy interviews with users and later parsing through large recordings to derive the issues to fix. In this paper, we explore how large language models (LLMs) like GPT 4.0, which have shown promising results in context comprehension and semantic text generation, can mitigate this issue and streamline the user testing process. Our solution, called Reca11, takes in informal transcripts of test recordings and extracts the accessibility and usability issues mentioned by the tester. Our systematic prompt engineering determines the optimal configuration of input, instruction, context and demonstrations for best results. We evaluate Reca11's effectiveness on 36 user testing sessions across three applications. Based on the findings, we investigate the strengths and weaknesses of using LLMs in this space.

## 13. Between Lines of Code: Unraveling the Distinct Patterns of Machine and Human Programmers

**Authors:** Yuling Shi (Shanghai Jiao Tong University), Hongyu Zhang (Chongqing University), Chengcheng Wan (East China Normal University), Xiaodong Gu (Shanghai Jiao Tong University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029948

**中文总结:** 分析人机代码在词法多样性、简洁性、句法分段等差异，提出 DetectCodeGPT 改进 DetectGPT 以检测机器生成代码。

**Abstract:** Large language models have catalyzed an unprecedented wave in code generation. While achieving significant advances, they blur the distinctions between machine- and human-authored source code, causing integrity and authenticity issues of software artifacts. Previous methods such as DetectGPT have proven effective in discerning machine-generated texts, but they do not identify and harness the unique patterns of machine-generated code. Thus, its applicability falters when applied to code. In this paper, we carefully study the specific patterns that characterize machine and human-authored code. Through a rigorous analysis of code attributes such as lexical diversity, conciseness, and naturalness, we expose unique patterns inherent to each source. We particularly notice that the syntactic segmentation of code is a critical factor in identifying its provenance. Based on our findings, we propose a novel machine-generated code detection method called DetectCodeGPT, which improves DetectGPT by capturing the distinct stylized patterns of code. Diverging from conventional techniques that depend on external LLMs for perturbations, DetectCodeGPT perturbs the code corpus by strategically inserting spaces and newlines, ensuring both efficacy and efficiency. Experiment results show that our approach significantly outperforms state-of-the-art techniques in detecting machine-generated code.

## 14. Boosting Static Resource Leak Detection via LLM-based Resource-Oriented Intention Inference

**Authors:** Chong Wang (Nanyang Technological University), Jianan Liu (Fudan University), Xin Peng (Fudan University), Yang Liu (Nanyang Technological University), Yiling Lou (Fudan University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029833

**中文总结:** 提出 InferROI，用大语言模型推断资源获取、释放与可达性验证意图，再辅以两阶段静态分析检测资源泄漏。

**Abstract:** Resource leaks, caused by resources not being released after acquisition, often lead to performance issues and system crashes. Existing static detection techniques rely on mechanical matching of predefined resource acquisition/release APIs and null-checking conditions to find unreleased resources, suffering from both (1) false negatives caused by the incompleteness of predefined resource acquisition/release APIs and (2) false positives caused by the incompleteness of resource reachability validation identification. To overcome these challenges, we propose InferROI, a novel approach that leverages the exceptional code comprehension capability of large language models (LLMs) to directly infer resource-oriented intentions (acquisition, release, and reachability validation) in code. InferROI first prompts the LLM to infer involved intentions for a given code snippet, and then incorporates a two-stage static analysis approach to check control-flow paths for resource leak detection based on the inferred intentions. We evaluate the effectiveness of InferROI in both resource-oriented intention inference and resource leak detection. Experimental results on the DroidLeaks and JLeaks datasets demonstrate InferROI achieves promising bug detection rate (59.3% and 62.5%) and false alarm rate (18.6% and 19.5%). Compared to three industrial static detectors, InferROI detects 14~45 and 149~485 more bugs in DroidLeaks and JLeaks, respectively. When applied to real-world open-source projects, InferROI identifies 29 unknown resource leak bugs (verified by authors), with 7 of them being confirmed by developers. In addition, the results of an ablation study underscores the importance of combining LLM-based inference with static analysis. Finally, manual annotation indicated that InferROI achieved a precision of 74.6% and a recall of 81.8% in intention inference, covering more than 60% resource types involved in the datasets.

## 15. Calibration and Correctness of Language Models for Code

**Authors:** Claudio Spiess (University of California, Davis), David Gros (University of California, Davis), Kunal Suresh Pai (UC Davis), Michael Pradel (University of Stuttgart), Rafiqul Rabin (UL Research Institutes), Amin Alipour (University of Houston), Susmit Jha (SRI), Prem Devanbu (University of California at Davis), Toufique Ahmed (IBM Research)

**Categories:** AI for Software Engineering

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029728

**中文总结:** 建立代码语言模型校准性评估框架，研究生成代码置信度与正确性的关联，为开发者决定直接使用、审查或丢弃模型输出提供依据。

**Abstract:** Machine learning models are widely used but can also often be wrong. Users would benefit from a reliable indication of whether a given output from a given model should be trusted, so a rational decision can be made whether to use the output or not. For example, outputs can be associated with a \emph{confidence measure}; if this confidence measure is strongly associated with \emph{likelihood of correctness}, then the model is said to be \emph{well-calibrated}. In this case, the confidence measure can serve as a basis for rational graduated decision making on how much review and care is needed. \emph{Calibration} has so far been studied in mostly non-generative (\emph{e.g.}, classification) settings, especially in Software Engineering. However, generated code can quite often be wrong: Given generated code developers must decide whether to directly use, use after varying intensity of careful review, or discard model-generated code; thus calibration is vital in generative settings. In this paper we make several contributions. We develop a framework for evaluating the calibration of code-generating models. We consider several tasks, correctness criteria, datasets, and approaches, and find that by and large generative code models are \textbf{\textit{\underline{not}}} well-calibrated out of the box. We then show how calibration can be improved, using standard methods such as Platt scaling. Since Platt scaling relies on the prior availability of correctness data, we evaluate the applicability and generalizability of Platt scaling in Software Engineering, discuss settings where it has good potential for practical use, and settings where it does not. Our contributions will lead to better-calibrated decision-making in the current use of code generated by language models, and offers a framework for future research to further improve calibration methods for generative models in Software Engineering.

## 16. Can an LLM find its way around a Spreadsheet?

**Authors:** Cho-Ting Lee (Virginia Tech), Andrew Neeser (Virginia Tech), Shengzhe Xu (Virginia Tech), Jay Katyan (Virginia Tech), Patrick Cross (Virginia Tech), Sharanya Pathakota (Virginia Tech), Marigold Norman (World Forest ID), John C. Simeone (Simeone Consulting, LLC), Jaganmohan Chandrasekaran (Virginia Tech), Naren Ramakrishnan (Virginia Tech)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029781

**中文总结:** 提出基于代码库检索的表格数据清洗系统，让大语言模型从可复用代码片段组合预处理流水线并持续扩充代码库。

**Abstract:** Spreadsheets are routinely used in business and scientific contexts, and one of the most vexing challenges is performing data cleaning prior to analysis and evaluation. The ad-hoc and arbitrary nature of data cleaning problems, such as typos, inconsistent formatting, missing values, and a lack of standardization, often creates the need for highly specialized pipelines. We ask whether an LLM can find its way around a spreadsheet and how to support end-users in taking their free-form data processing requests to fruition. Just like RAG retrieves context to answer users’ queries, we demonstrate how we can retrieve elements from a code library to compose data preprocessing pipelines. Through comprehensive experiments, we demonstrate the quality of our system and how it is able to continuously augment its vocabulary by saving new codes and pipelines back to the code library for future retrieval.

## 17. ChatGPT-Based Test Generation for Refactoring Engines Enhanced by Feature Analysis on Examples

**Authors:** Chunhao Dong (Beijing Institute of Technology), Yanjie Jiang (Peking University), Yuxia Zhang (Beijing Institute of Technology), Yang Zhang (Hebei University of Science and Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029808

**中文总结:** 基于重构引擎缺陷报告构建细粒度特征库，用 ChatGPT 按模板与特征生成测试程序并做差分测试，系统化发现多个重构引擎中的缺陷。

**Abstract:** Software refactoring is widely employed to improve software quality. However, conducting refactorings manually is tedious, time-consuming, and error-prone. Consequently, automated and semi-automated tool support is highly desirable for software refactoring in the industry, and most of the main-stream IDEs provide powerful tool support for refactoring. However, complex refactoring engines are prone to errors, which in turn may result in imperfect and incorrect refactorings. To this end, in this paper, we propose a ChatGPT-based approach to testing refactoring engines. We first manually analyze bug reports and test cases associated with refactoring engines, and construct a feature library containing fine-grained features that may trigger defects in refactoring engines. The approach automatically generates prompts according to both predefined prompt templates and features randomly selected from the feature library, requesting ChatGPT to generate test programs with the requested features. Test programs generated by ChatGPT are then forwarded to multiple refactoring engines for differential testing. To the best of our knowledge, it is the first approach in testing refactoring engines that guides test program generation with features derived from existing bugs. It is also the first approach in this line that exploits LLMs in the generation of test programs. Our initial evaluation of four main-stream refactoring engines suggests that the proposed approach is effective. It identified a total of 115 previously unknown bugs besides 28 inconsistent refactoring behaviors among different engines. Among the 115 bugs, 78 have been manually confirmed by the original developers of the tested engines, i.e., IntelliJ IDEA, Eclipse, VScode-Java, and NetBeans.

## 18. Closing the Gap: A User Study on the Real-world Usefulness of AI-powered Vulnerability Detection & Repair in the IDE

**Authors:** Benjamin Steenhoek (Microsoft), Siva Sivaraman (Microsoft), Renata Saldivar Gonzalez (Microsoft), Yevhen Mohylevskyy (Microsoft), Roshanak Zilouchian Moghaddam (Microsoft), Wei Le (Iowa State University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029760

**中文总结:** 在 IDE 中集成漏洞检测与修复工具 DEEPVULGUARD，对 17 名专业开发者在真实项目上进行首次实证研究，评估 AI 驱动漏洞检测与修复在实践中的可用性与价值。

**Abstract:** Security vulnerabilities impose significant costs on users and organizations. Detecting and addressing these vulnera bilities early is crucial to avoid exploits and reduce development costs. Recent studies have shown that deep learning models can effectively detect security vulnerabilities. Yet, little research explores how to adapt these models from benchmark tests to practical applications, and whether they can be useful in practice. This paper presents the first empirical study of a vulnerability detection and fix tool with professional software developers on real projects that they own. We implemented DEEPVULGUARD, an IDE-integrated tool based on state-of-the-art detection and fix models, and show that it has promising performance on bench marks of historic vulnerability data. DEEPVULGUARD scans code for vulnerabilities (including identifying the vulnerability type and vulnerable region of code), suggests fixes, provides natural- language explanations for alerts and fixes, leveraging chat inter faces. We recruited 17 professional software developers, observed their usage of the tool on their code, and conducted interviews to assess the tool’s usefulness, speed, trust, relevance, and workflow integration. We also gathered detailed qualitative feedback on users’ perceptions and their desired features. Study participants scanned a total of 24 projects, 6.9k files, and over 1.7 million lines of source code, and generated 170 alerts and 50 fix suggestions. We find that although state-of-the-art AI-powered detection and fix tools show promise, they are not yet practical for real-world use due to a high rate of false positives and non-applicable fixes. User feedback reveals several actionable pain points, ranging from incomplete context to lack of customization for the user’s codebase. Additionally, we explore how AI features, including confidence scores, explanations, and chat interaction, can apply to vulnerability detection and fixing. Based on these insights, we offer practical recommendations for evaluating and deploying AI detection and fix models. Our code and data are available at this link: https://figshare.com/s/77992badb1e37c09e4eb. We plan to release our tool as open-source to support further user studies for other AI based tools.

## 19. ClozeMaster: Fuzzing Rust Compiler by Harnessing LLMs for Infilling Masked Real Programs

**Authors:** Hongyan Gao (State Key Laboratory for Novel Software Technology, Nanjing University), Yibiao Yang (Nanjing University), Maolin Sun (Nanjing University), Jiangchang Wu (State Key Laboratory for Novel Software Technology, Nanjing University), Yuming Zhou (Nanjing University), Baowen Xu (State Key Laboratory for Novel Software Technology, Nanjing University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029729

**中文总结:** 提出 ClozeMaster，基于 clozeMask 策略从历史 issue 提取真实 Rust 程序并掩码关键片段，借助 LLM 填空生成有效测试用例以模糊测试 Rust 编译器，克服直接生成 Rust 程序大量无效的问题。

**Abstract:** Ensuring the reliability of the Rust compiler is of paramount importance, as the Rust language is increasingly being adopted for developing critical systems due to its emphasis on memory and thread safety. However, due to Rust’s complex syntax and strict requirements, generating valid test programs for the Rust compiler poses significant challenges. Currently, with the growing popularity of large language models (LLMs), much research in software testing has explored the use of LLMs to generate test cases. Despite this, directly using LLMs to generate Rust programs often results in a large number of invalid test cases. Existing studies have indicated that test cases triggering historical compiler bugs can assist in software testing. Our investigation into Rust compiler bug issues further supports this observation. Inspired by existing work and our empirical research, we introduce a bracket-based masking and filling strategy called clozeMask. The clozeMask strategy involves extracting test code from historical issue reports, identifying and masking code snippets with specific structures, and utilizing an LLM to fill in the masked portions for synthesizing new test programs. This approach harnesses the generative capabilities of LLMs while retaining the ability to trigger Rust compiler bugs. Ultimately, it enables comprehensive testing of the compiler’s behavior, particularly in exploring corner cases. We implemented our approach as a prototype CLOZEMASTER. CLOZEMASTER has identified 27 confirmed bugs for rustc and mrustc, of which 10 have been fixed by developers. Furthermore, our experimental results indicate that CLOZEMASTER outperforms existing generative fuzzers in terms of code coverage and effectiveness.

## 20. COCA: Generative Root Cause Analysis for Distributed Systems with Code Knowledge

**Authors:** Yichen LI (The Chinese University of Hong Kong), Yulun Wu (The Chinese University of Hong Kong), Jinyang Liu (Chinese University of Hong Kong), Zhihan Jiang (The Chinese University of Hong Kong), Zhuangbin Chen (Sun Yat-sen University), Guangba Yu (The Chinese University of Hong Kong), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029720

**中文总结:** 提出 COCA，从 issue 报告关联代码片段并重建执行路径，以代码知识增强分布式系统生成式根因分析，弥补仅依赖运行时监控或用户描述不足的问题。

**Abstract:** Runtime failures are commonplace in modern distributed systems. When such issues arise, users often turn to platforms such as Github or JIRA to report them and request assistance. Automatically identifying the root cause of these failures is critical for ensuring high reliability and availability. However, prevailing automatic root cause analysis (RCA) approaches rely significantly on comprehensive runtime monitoring data, which is often not fully available in issue platforms. Recent methods leverage large language models (LLMs) to analyze issue reports, but their effectiveness is limited by incomplete or ambiguous user-provided information. To obtain more accurate and comprehensive RCA results, the core idea of this work is to extract additional diagnostic clues from code to supplement data-limited issue reports. Specifically, we propose COCA, a code knowledge enhanced root cause analysis approach for issue reports. Based on the data within issue reports, COCA intelligently extracts relevant code snippets and reconstructs execution paths, providing a comprehensive execution context for further RCA. Subsequently, COCA construct a prompt combining historical issue reports along with profiled code knowledge, enabling the LLMs to generate detailed root cause summaries and localize responsible components. Our evaluation on datasets from five real-world distributed systems demonstrates that COCA significantly outperforms existing methods, achieving a 28.3% improvement in root cause localization and a 22.0% improvement in root cause summarization. Furthermore, COCA's performance consistency across various LLMs underscores its robust generalizability.

## 21. Code Comment Inconsistency Detection and Rectification Using a Large Language Model

**Authors:** Guoping Rong (Nanjing University), YongdaYu (Nanjing University), Song Liu (Nanjing University), Xin Tan (Nanjing University), Tianyi Zhang (Nanjing University), Haifeng Shen (Southern Cross University), Jidong Hu (Zhongxing Telecom Equipment)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029963

**中文总结:** 提出 C4RLLaMA，基于 CodeLLaMA 微调以检测并修正代码注释不一致（CCI）；在检测与修复任务上均优于现有方法。

**Abstract:** Comments are widely used in source code. If a comment is consistent with the code snippet it intends to annotate, it would aid code comprehension. Otherwise, Code Comment Inconsistency (CCI) is not only detrimental to the understanding of code, but more importantly, it would negatively impact the development, testing, and maintenance of software. To tackle this issue, existing research has been primarily focused on detecting inconsistencies with varied performance. It is evident that detection alone does not solve the problem; it merely paves the way for solving it. A complete solution requires detecting inconsistencies and, more importantly, rectifying them by amending comments. However, this type of work is scarce. In this paper, we contribute C4RLLaMA, a fine-tuned large language model based on the open-source CodeLLaMA. It not only has the ability to rectify inconsistencies by correcting relevant comment content but also outperforms state-of-the-art approaches in detecting inconsistencies. Experiments with various datasets confirm that C4RLLaMA consistently surpasses both Post Hoc and Just-in-time CCI detection approaches. More importantly, C4RLLaMA outperforms substantially the only known CCI rectification approach in terms of multiple performance metrics. To further examine C4RLLaMA's efficacy in rectifying inconsistencies, we conducted a manual evaluation, and the results showed that the percentage of correct comment updates by C4RLLaMA was 65.0\% and 55.9\% in Just-in-time and Post Hoc, respectively, implying C4RLLaMA's real potential in practical use.

## 22. Combining Fine-Tuning and LLM-based Agents for Intuitive Smart Contract Auditing with Justifications

**Authors:** Wei Ma, Daoyuan Wu (Hong Kong University of Science and Technology), Yuqiang Sun (Nanyang Technological University), Tianwen Wang (National University of Singapore), Shangqing Liu (Nanyang Technological University), Jian Zhang (Nanyang Technological University), Yue Xue, Yang Liu (Nanyang Technological University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029966

**中文总结:** 提出 iAudit，结合两阶段微调（检测器+推理器）与 LLM agent 做带理由的智能合约审计，以提升通用 LLM 审计精度不足的问题。

**Abstract:** Smart contracts are decentralized applications built atop blockchains like Ethereum. Recent research has shown that large language models (LLMs) have potential in auditing smart contracts, but the state-of-the-art indicates that even GPT-4 can achieve only 30% precision (when both decision and justification are correct). This is likely because off-the-shelf LLMs were primarily pre-trained on a general text/code corpus and not fine- tuned on the specific domain of Solidity smart contract auditing. In this paper, we propose iAudit, a general framework that combines fine-tuning and LLM-based agents for intuitive smart contract auditing with justifications. Specifically, iAudit is inspired by the observation that expert human auditors first perceive what could be wrong and then perform a detailed analysis of the code to identify the cause. As such, iAudit employs a two-stage fine-tuning approach: it first tunes a Detector model to make decisions and then tunes a Reasoner model to generate causes of vulnerabilities. However, fine-tuning alone faces challenges in accurately identifying the optimal cause of a vulnerability. Therefore, we introduce two LLM-based agents, the Ranker and Critic, to iteratively select and debate the most suitable cause of vulnerability based on the output of the fine-tuned Reasoner model. To evaluate iAudit, we collected a balanced dataset with 1,734 positive and 1,810 negative samples to fine-tune iAudit. We then compared it with traditional fine-tuned models (CodeBERT, GraphCodeBERT, CodeT5, and UnixCoder) as well as prompt learning-based LLMs (GPT4, GPT-3.5, and CodeLlama-13b/34b). On a dataset of 263 real smart contract vulnerabilities, iAudit achieves an F1 score of 91.21% and an accuracy of 91.11%. The causes generated by iAudit achieved a consistency of about 38% compared to the ground truth causes.

## 23. Context Conquers Parameters: Outperforming Proprietary LLM in Commit Message Generation

**Authors:** Aaron Imani (University of California, Irvine), Iftekhar Ahmed (University of California at Irvine), Mohammad Moshirpour (University of California, Irvine)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029724

**中文总结:** 提出基于 8B 开源 LLM 的提交信息生成方法 OMEGA，通过上下文精炼在隐私与成本约束下生成可与 GPT-4 驱动 OMG 媲美的提交说明，证明上下文优化可胜过参数量。

**Abstract:** Commit messages provide descriptions of the modifications made in a commit using natural language, making them crucial for software maintenance and evolution. Recent developments in Large Language Models (LLMs) have led to their use in generating high-quality commit messages, such as the Omniscient Message Generator (OMG). This method employs GPT-4 to produce state-of-the-art commit messages. However, the use of proprietary LLMs like GPT-4 in coding tasks raises privacy and sustainability concerns, which may hinder their industrial adoption. Considering that open-source LLMs have achieved competitive performance in developer tasks such as compiler validation, this study investigates whether they can be used to generate commit messages that are comparable with OMG. Our experiments show that an open-source LLM can generate commit messages that are comparable to those produced by OMG. In addition, through a series of contextual refinements, we propose lOcal MessagE GenerAtor (OMEGA) , a CMG approach that uses a 4-bit quantized 8B open-source LLM. OMEGA produces state-of-the-art commit messages, surpassing the performance of GPT-4 in practitioners' preference.

## 24. Decoding Secret Memorization in Code LLMs Through Token-Level Characterization

**Authors:** Yuqing Nie (Beijing University of Posts and Telecommunications), Chong Wang (Nanyang Technological University), Kailong Wang (Huazhong University of Science and Technology), Guoai Xu (Harbin Institute of Technology, Shenzhen), Guosheng Xu (Key Laboratory of Trustworthy Distributed Computing and Service (MoE), Beijing University of Posts and Telecommunications), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029894

**中文总结:** 基于 token 概率识别真实与幻觉密钥的四项特征，提出 DESEC 两阶段方法引导解码，高效提取 Code LLM 记忆的敏感信息。

**Abstract:** Code Large Language Models (LLMs) have demonstrated remarkable capabilities in generating, understanding, and manipulating programming code. However, their training process inadvertently leads to the memorization of sensitive information, posing severe privacy risks. Existing studies on memorization in LLMs primarily rely on prompt engineering techniques, which suffer from limitations such as widespread hallucination and inefficient extraction of the target sensitive information. In this paper, we present a novel approach to characterize real and fake secrets generated by Code LLMs based on token probabilities. We identify four key characteristics that differentiate genuine secrets from hallucinated ones, providing insights into distinguishing real and fake secrets. To overcome the limitations of existing works, we propose DESEC, a two-stage method that leverages token-level features derived from the identified characteristics to guide the token decoding process. DESEC consists of constructing an offline token scoring model using a proxy Code LLM and employing the scoring model to guide the decoding process by reassigning token likelihoods. Through extensive experiments on four state-of-the-art Code LLMs using a diverse dataset, we demonstrate the superior performance of DESEC in achieving a higher plausible rate and extracting more real secrets compared to existing baselines. Our findings highlight the effectiveness of our token-level approach in enabling an extensive assessment of the privacy leakage risks associated with Code LLMs.

## 25. Deep Learning-based Code Reviews: A Paradigm Shift or a Double-Edged Sword?

**Authors:** Rosalia Tufano (Università della Svizzera Italiana), Alberto Martin-Lopez (Software Institute - USI, Lugano), Ahmad Tayeb, Ozren Dabic (Software Institute, Università della Svizzera italiana (USI), Switzerland), Sonia Haiduc, Gabriele Bavota (Software Institute @ Università della Svizzera Italiana)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029823

**中文总结:** 通过对照实验评估深度学习自动代码审查对审查质量、审查耗时与审查者信心的影响，揭示 AI 生成审查意见融入代码审查流程的实际效应与潜在风险。

**Abstract:** Several techniques have been proposed to (partially) automate code review. Early support consisted in recommending the most suited reviewer for a given change or in prioritizing the review tasks. With the advent of deep learning in software engineering, the level of automation has been pushed to new heights, with approaches able to provide feedback on source code in natural language as a human reviewer would do. Also, recent work documented open source projects adopting Large Language Models (LLMs) as co-reviewers. Although the research in this field is very active, little is known about the actual impact of including automatically generated code reviews in the code review process. While there are many aspects worth investigating (e.g., is knowledge transfer between developers affected?), in this work we focus on three of them: (i) review quality, i.e., the reviewer's ability to identify issues in the code; (ii) review cost, i.e., the time spent reviewing the code; and (iii) reviewer’s confidence, i.e., how confident is the reviewer about the provided feedback. We run a controlled experiment with 29 professional developers who reviewed different programs with/without the support of an automatically generated code review. During the experiment we monitored the reviewers’ activities, for over 50 hours of recorded code reviews. We show that reviewers consider valid most of the issues automatically identified by the LLM and that the availability of an automated review as a starting point strongly influences their behavior: Reviewers tend to focus on the code locations indicated by the LLM rather than searching for additional issues in other parts of the code. The reviewers who started from an automated review identified a higher number of low-severity issues while, however, not identifying more high- severity issues as compared to a completely manual process. Finally, the automated support did not result in saved time and did not increase the reviewers’ confidence.

## 26. Distilled Lifelong Self-Adaptation for Configurable Systems

**Authors:** Yulong Ye (University of Birmingham), Tao Chen (University of Birmingham), Miqing Li (University of Birmingham)

**Categories:** AI for Software Engineering, Architecture and Design

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029783

**中文总结:** 提出 DLiSA 框架，通过终身规划与蒸馏知识播种使可配置系统在时变负载下持续自适配并优化运行时与吞吐量等性能。

**Abstract:** Modern configurable systems provide tremendous opportunities for engineering future intelligent software systems. A key difficulty thereof is how to effectively self-adapt the configuration of a running system such that its performance (e.g., runtime and throughput) can be optimized under time-varying workloads. This unfortunately remains unaddressed in existing approaches as they either overlook the available past knowledge or rely on static exploitation of past knowledge without reasoning the usefulness of information when planning for self-adaptation. In this paper, we tackle this challenging problem by proposing DLiSA, a framework that self-adapts configurable systems. DLiSA comes with two properties: firstly, it supports lifelong planning, and thereby the planning process runs continuously throughout the lifetime of the system, allowing dynamic exploitation of the accumulated knowledge for rapid adaptation. Secondly, the planning for a newly emerged workload is boosted via distilled knowledge seeding, in which the knowledge is dynamically purified such that only useful past configurations are seeded when necessary, mitigating misleading information. Extensive experiments suggest that the proposed DLiSA significantly outperforms state-of-the-art approaches, demonstrating a performance improvement of up to 255\% and a resource acceleration of up to 2.22$\times$ on generating promising adaptation configurations. All data and sources can be found at our anonymous site: https://github.com/Anonymous-DLiSA/DLiSA.

## 27. Does GenAI Make Usability Testing Obsolete?

**Authors:** Ali Ebrahimi Pourasad, Walid Maalej (University of Hamburg)

**Categories:** AI for Software Engineering, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029918

**中文总结:** 提出视觉语言模型工具 UX-LLM 预测 iOS 应用可用性问题，精确率 0.61–0.66、召回率 0.35–0.38，尚无法取代传统可用性测试。

**Abstract:** Ensuring usability is crucial for the success of mobile apps. Usability issues can compromise user experience and negatively impact the perceived app quality. This paper presents UX-LLM, a novel tool powered by a Large Vision-Language Model that predicts usability issues in iOS apps. To evaluate the performance of UX-LLM we predicted usability issues in two open-source apps of a medium complexity and asked usability experts to assess the predictions. We also performed traditional usability testing and expert review for both apps and compared the results to those of UX-LLM. UX-LLM demonstrated precision ranging from 0.61 and 0.66 and recall between 0.35 and 0.38, indicating its ability to identify valid usability issues, yet failing to capture the majority of issues. Finally, we conducted a focus group with an app development team of a capstone project developing a transit app for visually impaired persons. The focus group expressed positive perceptions of UX-LLM as it identified unknown usability issues in their app. However, they also raised concerns about its integration into the development workflow, suggesting potential improvements. Our results show that UX-LLM cannot fully replace traditional usability evaluation methods but serves as a valuable supplement particularly for small teams with limited resources, to identify issues in less common user paths, due to its ability to inspect the source code.

## 28. Enhancing Code Generation via Bidirectional Comment-Level Mutual Grounding

**Authors:** Yifeng Di (Purdue University), Tianyi Zhang (Purdue University)

**Categories:** AI for Software Engineering, Program Analysis and Verification, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029958

**中文总结:** 提出基于代码注释的双向互 grounding 交互式代码生成方法，通过迭代注释与反馈对齐开发者意图，显著提升多种 LLM 的 Pass@1。

**Abstract:** Large Language Models (LLMs) have demonstrated unprecedented capability in code generation. However, LLM-generated code is still plagued with a wide range of functional errors, especially for complex programming tasks that LLMs have not seen before. Recent studies have shown that developers often struggle with inspecting and fixing incorrect code generated by LLMs, diminishing their productivity and trust in LLM-based code generation. Inspired by the mutual grounding theory in communication, we propose an interactive approach that leverages code comments as a medium for developers and LLMs to establish a shared understanding. Our approach facilitates iterative grounding by interleaving code generation, inline comment generation, and contextualized user feedback through editable comments to align generated code with developer intent. We evaluated our approach on two popular benchmarks and demonstrated that our approach significantly improved multiple state-of-the-art LLMs, e.g., 16.9\% Pass@1 improvement for code-davinci-002 on HumanEval. Furthermore, we conducted a user study with 12 participants in comparison to two baselines: (1) interacting with GitHub Copilot, and (2) interacting with a multi-step code generation paradigm called Multi-Turn Program Synthesis. Participants completed the given programming tasks 16.7\% faster and with 10.5\% improvement in task success rate when using our approach. Both results show that interactively refining code comments enables the collaborative establishment of mutual grounding, leading to more accurate code generation and higher developer confidence.

## 29. Execution Trace Reconstruction Using Diffusion-Based Generative Models

**Authors:** Madeline Janecek (Brock University), Naser Ezzati-Jivan, Abdelwahab Hamou-Lhadj (Concordia University, Montreal, Canada)

**Categories:** AI for Software Engineering, Testing and Quality, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029922

**中文总结:** 首次系统评估扩散模型重建不完整执行追踪序列，SSSD^S4 在九个 Phoronix 数据集上于多种缺失比例下表现最优。

**Abstract:** Execution tracing is essential for understanding system and software behaviour, yet lost trace events can significantly compromise data integrity and analysis. Existing solutions for trace reconstruction often fail to fully leverage available data, particularly in complex and high-dimensional contexts. Recent advancements in generative artificial intelligence, particularly diffusion models, have set new benchmarks in image, audio, and natural language generation. This study conducts the first comprehensive evaluation of diffusion models for reconstructing incomplete trace event sequences. Using nine distinct datasets generated from the Phoronix Test Suite, we rigorously test these models on sequences of varying lengths and missing data ratios. Our results indicate that the SSSD$^{S4}$ model, in particular, achieves superior performance, in terms of accuracy, perfect rate, and ROUGE-L score across diverse imputation scenarios. These findings underscore the potential of diffusion-based models to accurately reconstruct missing events, thereby maintaining data integrity and enhancing system monitoring and analysis.

## 30. exLong: Generating Exceptional Behavior Tests with Large Language Models

**Authors:** Jiyang Zhang (University of Texas at Austin), Yu Liu (Meta), Pengyu Nie (University of Waterloo), Junyi Jessy Li (University of Texas at Austin, USA), Milos Gligoric (The University of Texas at Austin)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029954

**中文总结:** 提出 EXLÓNG，基于 CodeLlama 微调的大模型自动生成异常行为测试，弥补开发者主要测试正常路径而忽视异常路径的不足。

**Abstract:** Many popular programming languages, including C#, Java, and Python, support exceptions. Exceptions are thrown during program execution if an unwanted event happens, e.g., a method is invoked with an illegal argument value. Software developers write exceptional behavior tests (EBTs) to check that their code detects unwanted events and throws appropriate exceptions. Prior research studies have shown the importance of EBTs, but those studies also highlighted that developers put most of their efforts on “happy paths”, e.g., paths without unwanted events. To help developers fill the gap, we present the first framework, dubbed EXLÓNG, that automatically generates EBTs. EXLÓNG is a large language model instruction-tuned from CodeLlama and embeds reasoning about traces that lead to throw statements, conditional expressions that guard throw statements, and non-exceptional behavior tests that execute similar traces. We compare EX LÓNG with the state-of-the-art models for test generation (CAT-LM) and one of the strongest foundation models (GPT3.5), as well as with analysis-based tools for test generation (Randoop and EvoSuite). Our results show that EXLÓNG outperforms existing models and tools. Furthermore, we contributed several pull requests to open-source projects and 23 EBTs generated by EXLÓNG were already accepted.

## 31. FAMOS: Fault diagnosis for Microservice Systems through Effective Multi-modal Data Fusion

**Authors:** Chiming Duan (Peking University), Yong Yang (Peking University), Tong Jia (Institute for Artificial Intelligence, Peking University, Beijing, China), Guiyang Liu (Alibaba), Jinbu Liu (Alibaba), Huxing Zhang (Alibaba Group), Qi Zhou (Alibaba), Ying Li (School of Software and Microelectronics, Peking University, Beijing, China), Gang Huang (Peking University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029787

**中文总结:** 提出 FAMOS 微服务故障诊断方法，为 trace、日志、指标等多模态数据设计独立特征提取器并引入高斯过程融合跨模态关系，准确诊断故障根因。

**Abstract:** Accurately diagnosing the fault that causes the failure is crucial for maintaining the reliability of a microservice system after a failure occurs. Mainstream fault diagnosis approaches are data-driven and mainly rely on three modalities of runtime data: traces, logs, and metrics. Diagnosing faults with multiple modalities of data in microservice systems has been an clear trend in recent years because different types of faults and corresponding failures tend to manifest in data of various modalities. Accurately diagnosing faults by fully leveraging multiple modalities of data is confronted with two challenges: 1)how to minimize information loss when extracting features for data of each modality; 2)how to correctly capture andutilize the relationships among data of different modalities. To address these challenges, we propose FAMOS, a Fault diagnosis Approach for MicrOservice Systems through effective multi-modal data fusion. On the one hand, FAMOS employs independent feature extractors to preserve the intrinc features for each modality. On the other hand, FAMOS introduces a new Gaussian-attention mechanism to accurately correlate data of different modalities and then captures the inter-modality relationship with a cross-attention mechanism. We evaluated FAMOS on two datasets constructed by injecting comprehensive and abundant faults into an open-source microservice system and a real-world industrial microservice system. Experimental results demonstrate the FAMOS’s effectiveness in fault diagnosis, achieving significant improvements in F1 scores compared to state-of-the-art (SOTA) methods, with an increase of 20.33%.

## 32. Faster Configuration Performance Bug Testing with Neural Dual-level Prioritization

**Authors:** Youpeng Ma (University of Electronic Science and Technology of China), Tao Chen (University of Birmingham), Ke Li (University of Exeter)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029809

**中文总结:** 提出 NDP，在配置项与取值范围两个层级用神经网络优先排序并自动估计测试预言，显著加速配置性能缺陷（CPBug）检测。

**Abstract:** As software systems become more complex and configurable, more performance problems tend to arise from the configuration designs. This has caused some configuration options to unexpectedly degrade performance which deviates from their original expectations designed by the developers. Such discrepancies, namely configuration performance bugs (CPBugs), are devastating and can be deeply hidden in the source code. Yet, efficiently testing CPBugs is difficult, not only due to the test oracle is hard to set, but also because the configuration measurement is expensive and there are simply too many possible configurations to test. As such, existing testing tools suffer from lengthy runtime or have been ineffective in detecting CPBugs when the budget is limited, compounded by inaccurate test oracle. In this paper, we seek to achieve significantly faster CPBug testing by neurally prioritizing the testing at both the configuration option and value range levels with automated oracle estimation. Our proposed tool, dubbed NDP, is a general framework that works with different heuristic generators. The idea is to leverage two neural language models: one to estimate the CPBug types that serve as the oracle while, more vitally, the other to infer the probabilities of an option being CPBug-related, based on which the options and the value ranges to be searched can be prioritized. Experiments on several widely-used systems of different versions reveal that NDP can, in general, better predict CPBug type in 87% cases and find more CPBugs with up to 88.88$\times$ testing efficiency speedup over the state-of-the-art tools.

## 33. Feature-Driven End-To-End Test Generation

**Authors:** Parsa Alian (University of British Columbia), Noor Nashid (University of British Columbia), Mobina Shahbandeh (University of British Columbia), Taha Shabani (University of British Columbia), Ali Mesbah (University of British Columbia)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029959

**中文总结:** 提出 AUTOE2E，利用 LLM 推断 Web 应用功能并生成语义化端到端测试，同时发布 E2EBENCH 基准；平均功能覆盖率达 79%，较最佳基线提升 558%。

**Abstract:** End-to-end (E2E) testing is essential for ensuring web application quality. However, manual test creation is time-consuming and current test generation techniques produce random tests. In this paper, we present AUTOE2E, a novel approach that leverages Large Language Models (LLMs) to automate the generation of semantically meaningful feature-driven E2E test cases for web applications. AUTOE2E intelligently infers potential features within a web application and translates them into executable test scenarios. Furthermore, we address a critical gap in the research community by introducing E2EBENCH, a new benchmark for automatically assessing the feature coverage of E2E test suites. Our evaluation on E2EBENCH demonstrates that AUTOE2E achieves an average feature coverage of 79%, outperforming the best baseline by 558%, highlighting its effectiveness in generating high-quality, comprehensive test cases.

## 34. Fixing Large Language Models' Specification Misunderstanding for Better Code Generation

**Authors:** Zhao Tian (Tianjin University), Junjie Chen (Tianjin University), Xiangyu Zhang (Purdue University)

**Categories:** AI for Software Engineering, Software Engineering for AI, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029745

**中文总结:** 提出 μFiX 提示技术，结合思维引导与细粒度反馈修复大语言模型对编程规格的理解偏差以提升代码生成质量。

**Abstract:** Code generation is to automatically generate source code conforming to a given programming specification, which has received extensive attention especially with the development of large language models (LLMs). Due to the inherent difficulty of code generation, the code generated by LLMs may not be aligned with the specification. Although thought-eliciting prompting techniques have been proposed to enhance the code generation performance of LLMs, producing correct understanding for complicated programming problems remains challenging, resulting in unsatisfactory performance. Also, some feedback-based prompting techniques have been proposed to fix incorrect code using error messages produced by test execution. However, when the generated code deviates significantly from the ground truth, they encounter difficulties in improving performance based on such coarse-grained information. In this work, we propose a novel prompting technique, called μFiX, to improve the code generation performance of LLMs by devising both sophisticated thought-eliciting prompting and feedback-based prompting and making the first exploration on their synergy. It first exploits test case analysis to obtain specification understanding and enables a self-improvement process to identify and refine the misunderstanding in the thought-eliciting prompting phase. μFiX further fixes the specification understanding towards the direction reducing the gap between the provided understanding (from the first phase) and the actual understanding implicitly utilized by LLMs for code generation in the feedback-based prompting phase. By improving the understanding with μFiX, the code generation performance of LLMs can be largely improved. Our evaluation on two advanced LLMs (ChatGPT and DeepSeek-Coder) with six widely-used benchmarks by comparing with 15 baselines, demonstrates the effectiveness of μFiX. For example, μFiX outperforms the most effective baseline with an average improvement of 35.62% in terms of Pass@1 across all subjects.

## 35. From Bugs to Benefits: Improving User Stories by Leveraging Crowd Knowledge with CrUISE-AC

**Authors:** Stefan Schwedt (Heriot-Watt University, UK), Thomas Ströder (FHDW Mettmann)

**Categories:** AI for Software Engineering, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029950

**中文总结:** 提出 CrUISE-AC，从同领域公开 issue 追踪器挖掘群体知识，自动为用户故事生成非平凡验收标准，减少因需求不完整导致的缺陷。

**Abstract:** Costs for resolving software defects increase exponentially in late stages. Incomplete or ambiguous requirements are one of the biggest sources for defects, since stakeholders might not be able to communicate their needs or fail to share their domain specific knowledge. Combined with insufficient developer experience, teams are prone to constructing incorrect or incomplete features. To prevent this, requirements engineering has to explore knowledge sources beyond stakeholder interviews. Publicly accessible issue trackers for systems within the same application domain hold essential information on identified weaknesses, edge cases, and potential error sources, all documented by actual users. Our research aims at (1) identifying, and (2) leveraging such issues to improve an agile requirements artifact known as a “user story”. We present CrUISE-AC (Crowd and User Informed Suggestion Engine for Acceptance Criteria) as a fully automated method that investigates issues and generates non-trivial additional acceptance criteria for a given user story by employing NLP techniques and an ensemble of LLMs. CrUISE-AC was evaluated by five independent experts in two distinct business domains. Our findings suggest that issue trackers hold valuable information pertinent to requirements engineering. Our evaluation shows that 80–82% of the generated acceptance criteria add relevant requirements to the user stories. Limitations are the dependence on accessible input issues and the fact that we do not check generated criteria for being conflict-free or non-overlapping with criteria from other user stories.

## 36. GARL: Genetic Algorithm-Augmented Reinforcement Learning to Detect Violations in Marker-Based Autonomous Landing Systems

**Authors:** Linfeng Liang (Macquarie University), Yao Deng (Macquarie University), Kye Morton (Skyy Network), Valtteri Kallinen (Skyy Network), Alice James (Macquarie University), Avishkar Seth (Macquarie University), Endrowednes Kuantama (Macquarie University), Subhas Mukhopadhyay (Macquarie University), Richard Han (Macquarie University), Xi Zheng (Macquarie University)

**Categories:** AI for Software Engineering, Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029873

**中文总结:** 提出 GARL 框架，将遗传算法与强化学习结合高效生成无人机自主着陆系统违规场景，性能较现有方法最高提升 18.35%。

**Abstract:** Automated Uncrewed Aerial Vehicle (UAV) landing is crucial for autonomous UAV services such as monitoring, surveying, and package delivery. It involves detecting landing targets, perceiving obstacles, planning collision-free paths, and controlling UAV movements for safe landing. Failures can lead to significant losses, necessitating rigorous simulation-based testing for safety. Traditional offline testing methods, limited to static environments and predefined trajectories, may miss violation cases caused by dynamic objects like people and animals. Conversely, online testing methods require extensive training time, which is impractical with limited budgets. To address these issues, we introduce GARL, a framework combining a genetic algorithm (GA) and reinforcement learning (RL) for efficient generation of diverse and real landing system failures within a practical budget. GARL employs GA for exploring various environment setups offline, reducing the complexity of RL's online testing in simulating challenging landing scenarios. Our approach outperforms existing methods by up to 18.35% in violation rate and 58% in diversity metric. We validate most discovered violation types with real-world UAV tests, pioneering the integration of offline and online testing strategies for autonomous systems. This method opens new research directions for online testing, with our code available at https://anonymous.4open.science/r/drone_testing-5CF0/.

## 37. Gpass: a Goal-adaptive Neural Theorem Prover based on Coq for Automated Formal Verification

**Authors:** Yizhou Chen (Peking University), Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Guoqing Wang (Peking University), Dan Hao (Peking University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029939

**中文总结:** 提出面向 Coq 的目标自适应神经定理证明器 Gpass，通过滑动窗口编码与目标自适应特征融合自动生成长证明步骤，克服现有自动定理证明器的局限。

**Abstract:** Formal verification is a crucial means to assure software quality. Regrettably, the manual composition of verification scripts proves to be both laborious and time-consuming. In response, researchers have put forth automated theorem prover approaches; however, these approaches still grapple with several limitations. These limitations encompass insufficient handling of lengthy proof steps, difficulty in aligning the various components of a Coq program with the requirements and constraints of the proof goal, and inefficiencies. To surmount these limitations, we present Gpass, a goal-adaptive neural theorem prover based on deep learning technology. Firstly, we design a unique sequence encoder for Gpass that completely scans previous proof tactics through multiple sliding windows and provides information related to the current proof step. Secondly, Gpass incorporates a goal-adaptive feature integration module to align the reasoning process with the requirements of the proof goal. Finally, we devise a parameter selection method based on loss values and loss slopes to procure parameter sets with diverse distributions, thereby facilitating the exploration of various proof tactics. Experimental results demonstrate that Gpass attains better performance on the extensive CoqGym benchmark and proves 11.03\%-96.37\% more theorems than the prior work most closely related to ours. We find that the orthogonality between Gpass and CoqHammer proves their complementary capabilities, and together they prove a total of 3,774 theorems, which is state-of-the-art performance. In addition, we propose an efficiency optimisation approach that allows Gpass to achieve performance beyond Diva at one-sixth of the parameter sets.

## 38. GVI: Guided Vulnerability Imagination for Boosting Deep Vulnerability Detectors

**Authors:** Heng Yong (Nanjing University), Zhong Li, Minxue Pan (Nanjing University), Tian Zhang (Nanjing University), Jianhua Zhao (Nanjing University, China), Xuandong Li (Nanjing University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029920

**中文总结:** 提出 GVI，通过引导式“漏洞想象”合成更贴近真实分布的漏洞样本，缓解深度漏洞检测器训练数据类别不平衡问题。

**Abstract:** The use of deep learning to achieve automated software vulnerability detection has been a longstanding interest within the software security community. These deep vulnerability detectors are mostly trained in a supervised manner, which heavily relies on large-scale, high-quality vulnerability datasets. However, the vulnerability datasets used to train deep vulnerability detectors frequently exhibit class imbalance due to the inherent nature of vulnerability data, where vulnerable cases are significantly rarer than non-vulnerable cases. This imbalance adversely affects the effectiveness of these detectors. A promising solution to address the class imbalance problem is to artificially generate vulnerable samples to enhance vulnerability datasets, yet existing vulnerability generation techniques are not satisfactory due to their inadequate representation of real-world vulnerabilities or their reliance on large-scale vulnerable samples for training the generation model. This paper proposes GVI, a novel approach aimed at generating vulnerable samples to boost deep vulnerability detectors. GVI takes inspiration from human learning with imagination and proposes exploring LLMs to imagine and create new, informative vulnerable samples from given seed vulnerabilities. Specifically, we design a Chain-of-Thought inspired prompt in GVI that instructs the LLMs to first analyze the seed to retrieve attributes related to vulnerabilities and then generate a set of vulnerabilities based on the seed’s attributes. Our extensive experiments on three vulnerability datasets (i.e., Devign, ReVeal, and BigVul) and across three deep vulnerability detectors (i.e., Devign, ReVeal, and LineVul) demonstrate that the vulnerable samples generated by GVI are not only more accurate but also more effective in enhancing the performance of deep vulnerability detectors.

## 39. HedgeCode: A Multi-Task Hedging Contrastive Learning Framework for Code Search

**Authors:** Gong Chen (Wuhan University), Xiaoyuan Xie (Wuhan University), Xunzhu Tang (University of Luxembourg), Qi Xin (Wuhan University), Wenjie Liu (Wuhan University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029759

**中文总结:** 提出 HedgeCode，多任务对冲对比学习框架对齐代码与自然语言表示并捕捉细粒度语义差异，用于提升代码搜索效果。

**Abstract:** Code search is a vital activity in software engineering, focused on identifying and retrieving the correct code snippets based on a query provided in natural language. Approaches based on deep learning techniques have been increasingly adopted for this task, enhancing the initial representations of both code and its natural language descriptions. Despite this progress, there remains an unexplored gap in ensuring consistency between the representation spaces of code and its descriptions. Furthermore, existing methods have not fully leveraged the potential relevance between code snippets and their descriptions, presenting a challenge in discerning fine-grained semantic distinctions among similar code snippets. To address these challenges, we introduce a multi-task hedging contrastive Learning framework for Code Search, referred to as HedgeCode. HedgeCode is structured around two primary training phases. The first phase, known as the representation alignment stage, proposes a hedging contrastive learning approach. This method aims to detect subtle differences between code and natural language text, thereby aligning their representation spaces by identifying relevance. The subsequent phase involves multi-task joint learning, wherein the previously trained model serves as the encoder. This stage optimizes the model through a combination of supervised and self-supervised contrastive learning tasks. Our framework’s effectiveness is demonstrated through its performance on the CodeSearchNet benchmark, showcasing HedgeCode’s ability to address the mentioned limitations in code search tasks.

## 40. HumanEvo: An Evolution-aware Benchmark for More Realistic Evaluation of Repository-level Code Generation

**Authors:** Dewu Zheng (Sun Yat-sen University), Yanlin Wang (Sun Yat-sen University), Ensheng Shi (Xi’an Jiaotong University), Ruikai Zhang (Huawei Cloud Computing Technologies), Yuchi Ma (Huawei Cloud Computing Technologies), Hongyu Zhang (Chongqing University), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029910

**中文总结:** 指出忽视项目演化会导致仓库级代码生成评测失真，构建演化感知基准 HumanEvo 及自动执行评测工具，更贴近真实开发场景。

**Abstract:** To evaluate the repository-level code generation capabilities of Large Language Models (LLMs) in complex real-world software development scenarios, many evaluation methods have been developed. These methods typically leverage contextual code from the latest version of a project to assist LLMs in accurately generating the desired function. However, such evaluation methods fail to consider the dynamic evolution of software projects over time, which we refer to as evolution-ignored settings. This in turn results in inaccurate evaluation of LLMs' performance. In this paper, we conduct an empirical study to deeply understand LLMs' code generation performance within settings that reflect the evolution nature of software development. To achieve this, we first construct an evolution-aware repository-level code generation dataset, namely HumanEvo, equipped with an automated execution-based evaluation tool. Second, we manually categorize HumanEvo according to dependency levels to more comprehensively analyze the model's performance in generating functions with different dependency levels. Third, we conduct extensive experiments on HumanEvo with seven representative and diverse LLMs to verify the effectiveness of the proposed benchmark. We obtain several important findings through our experimental study. For example, we find that previous evolution-ignored evaluation methods result in inflated performance of LLMs, with performance overestimations ranging from 10.0% to 61.1% under different context acquisition methods, compared to the evolution-aware evaluation approach. Based on the findings, we give actionable suggestions for more realistic evaluation of LLMs on code generation. We also build a shared evolution-aware code generation toolbox to facilitate future research. The replication package including source code and datasets is anonymously available at https://anonymous.4open.science/r/HumanEvo/.

## 41. Instruct or Interact? Exploring and Eliciting LLMs’ Capability in Code Snippet Adaptation Through Prompt Engineering

**Authors:** Tanghaoran Zhang (National University of Defense Technology), Yue Yu (PengCheng Lab), Xinjun Mao (National University of Defense Technology), Shangwen Wang (National University of Defense Technology), Kang Yang (National University of Defense Technology), Yao Lu (National University of Defense Technology), Zhang Zhang (Key Laboratory of Software Engineering for Complex Systems, National University of Defense Technology), Yuxin Zhao (Key Laboratory of Software Engineering for Complex Systems, National University of Defense Technology)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11029912

**中文总结:** 实证比较 LLM 在代码片段适配与自由生成任务上的表现，发现适配能力弱约 15% pass@1 且更易出现上下文相关错误，并归纳三类失败原因及提示工程改进方向。

**Abstract:** Code snippet adaptation is a fundamental activity in the software development process. Unlike code generation, code snippet adaptation is not a ``free creation'', which requires developers to tailor a given code snippet in order to fit specific requirements and the code context. Recently, large language models (LLMs) have confirmed their effectiveness in the code generation task with promising results. However, their performance on code snippet adaptation, a reuse-oriented and context-dependent code change prediction task, is still unclear. To bridge this gap, we conduct an empirical study to investigate the performance and issues of LLMs on the adaptation task. We first evaluate the adaptation performances of three popular LLMs and compare them to the code generation task. Our result indicates that their adaptation ability is weaker than generation, with a nearly 15\% decrease on pass@1 and more context-related errors. By manually inspecting 200 cases, we further investigate the causes of LLMs’ sub-optimal performance, which can be classified into three categories, \emph{i.e.,} \textit{Unclear Requirement}, \textit{Requirement Misalignment} and \textit{Context Misapplication}. Based on the above empirical research, we propose an interactive prompting approach to eliciting LLMs' ability on the adaptation task. Specifically, we enhance the prompt by enriching the context and decomposing the task, which alleviates context misapplication and improves requirement understanding. Besides, we enable LLMs' reflection by requiring them to interact with a human or a LLM counselor, compensating for unclear requirement. Our experimental result reveals that our approach greatly improve LLMs' adaptation performance. The best-performing Human-LLM interaction successfully solves 159 out of the 202 identified defects and improves the pass@1 and pass@5 by over 40\% compared to the initial instruction-based prompt. Considering human efforts, we suggest multi-agent interaction as a trade-off, which can achieve comparable performance with excellent generalization ability. We deem that our approach could provide methodological assistance for autonomous code snippet reuse and adaptation with LLMs.

## 42. Intention is All You Need: Refining Your Code from Your Intention

**Authors:** Qi Guo (Tianjin University), Xiaofei Xie (Singapore Management University), Shangqing Liu (Nanyang Technological University), Ming Hu (Nanyang Technological University), Xiaohong Li (Tianjin University), Lei Bu (Nanjing University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11029878

**中文总结:** 提出基于意图的代码精炼：先将注释分类为八类意图再由 LLM 生成修改，意图提取准确率 79%，代码精炼生成最高 66%。

**Abstract:** This paper proposes an intention-based code refinement technique, transforming the conventional code refinement process from comment to code to intention to code. The process is decomposed into two phases: Intention Extraction and Intention Guided Code Modification Generation. Intention Extraction categorizes comments using predefined templates, while the latter employs large language models (LLMs) to generate revised code based on these defined intentions. Three categories with eight subcategories are designed for comment transformation, followed by a hybrid approach that combines rule-based and LLM-based classifiers for accurate classification. Extensive experiments with five LLMs (GPT4o, GPT3.5, DeepSeekV2, DeepSeek7B, CodeQwen7B) under different prompting settings demonstrate that our approach achieves 79% accuracy in intention extraction and up to 66% in code refinement generation. Our results underscore the potential of this approach in enhancing data quality and improving code refinement processes.

## 43. InterTrans: Leveraging Transitive Intermediate Translations to Enhance LLM-based Code Translation

**Authors:** Marcos Macedo (Queen's University), Yuan Tian (Queen's University, Kingston, Ontario), Pengyu Nie (University of Waterloo), Filipe Cogo (Centre for Software Excellence, Huawei Canada), Bram Adams (Queen's University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11029964

**中文总结:** 提出 InterTrans，用 Tree of Code Translation 规划经中间语言的翻译路径，利用 LLM 多语言能力缓解源目标语言间语法语义鸿沟。

**Abstract:** Code translation aims to convert a program from one programming language (PL) to another. This long-standing software engineering task is crucial for modernizing legacy systems, ensuring cross-platform compatibility, enhancing performance, and more. However, automating this process remains challenging due to many syntactic and semantic differences between PLs. Recent studies show that even advanced techniques such as large language models (LLMs), especially open-source LLMs, still struggle with the task. Currently, code LLMs are trained with source code from multiple programming languages, thus presenting multilingual capabilities. In this paper, we investigate whether such capabilities can be harnessed to enhance code translation. To achieve this goal, we introduce InterTrans, an LLM-based automated code translation approach that, in contrast to existing approaches, leverages intermediate translations to bridge the syntactic and semantic gaps between source and target PLs. InterTrans contains two stages. It first utilizes a novel Tree of Code Translation (ToCT) algorithm to plan transitive intermediate translation sequences between a given source and target PL, then validates them in a specific order. We evaluate InterTrans with three open LLMs on three benchmarks (i.e., CodeNet, HumanEval-X, and TransCoder) involving six PLs. Results show an absolute improvement of 18.3% to 43.3% in Computation Accuracy (CA) for InterTrans over Direct Translation with 10 attempts. The best-performing variant of InterTrans(with the Magicoder LLM) achieved an average CA of 87.3%-95.4% on three benchmarks.

## 44. Knowledge-Enhanced Program Repair for Data Science Code

**Authors:** Shuyin Ouyang (King's College London), Jie M. Zhang (King's College London), Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Albert Merono Penuela (King's College London)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029882

**中文总结:** 提出 DSrepair，以数据科学知识图谱 RAG 与 AST 级错误定位增强 LLM 修复提示；在 DS-1000 上相较最优基线多修复 14.2%–44.4% 的缺陷代码。

**Abstract:** This paper introduces DSrepair, a knowledge-enhanced program repair method designed to repair the buggy code generated by LLMs in the data science domain. DSrepair uses knowledge graph based RAG for API knowledge retrieval as well as bug knowledge enrichment to construct repair prompts for LLMs. Specifically, to enable knowledge graph based API retrieval, we construct DS-KG (Data Science Knowledge Graph) for widely used data science libraries. For bug knowledge enrichment, we employ an abstract syntax tree (AST) to localize errors at the AST node level. DSrepair's effectiveness is evaluated against five state-of-the-art LLM-based repair baselines using four advanced LLMs on the DS-1000 dataset. The results show that DSrepair surpasses all five baselines. Specifically, when compared to the second-best baseline, DSrepair demonstrates significant improvements, fixing 44.4%, 14.2%, 20.6%, and 32.1% more buggy code snippets for each of the four evaluated LLMs, respectively. Additionally, it achieves greater efficiency, reducing the number of tokens required per code task by 17.49%, 34.24%, 24.71%, and 17.59%, respectively.

## 45. Large Language Models as Configuration Validators

**Authors:** Xinyu Lian (University of Illinois at Urbana-Champaign), Yinfang Chen (University of Illinois at Urbana-Champaign), Sam Cheng (University of Illinois at Urbana-Champaign), Jie Huang (University of Illinois at Urbana-Champaign), Parth Thakkar (Meta Platforms, Inc.), Minjia Zhang (UIUC), Tianyin Xu (University of Illinois at Urbana-Champaign)

**Categories:** AI for Software Engineering, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029850

**中文总结:** 提出 Ciri 框架，探索 LLM 做配置校验的可行性与有效性；通过少样本提示与输出校验缓解幻觉，并在 8 个 LLM、10 个系统配置上评估。

**Abstract:** Misconfigurations are major causes of software failures. Existing practices rely on developer-written rules or test cases to validate configurations, which are expensive. Machine learning (ML) for configuration validation is considered a promising direction, but has been facing challenges such as the need of large-scale field data and system-specific models. Recent advances in Large Language Models (LLMs) show promise in addressing some of the long-lasting limitations of ML-based configuration validation. We present a first analysis on the feasibility and effectiveness of using LLMs for configuration validation. We empirically evaluate LLMs as configuration validators by developing a generic LLM-based configuration validation framework, named Ciri. Ciri employs effective prompt engineering with few-shot learning based on both valid configuration and misconfiguration data. Ciri checks outputs from LLMs when producing results, addressing hallucination and nondeterminism of LLMs. We evaluate Ciri’s validation effectiveness on eight popular LLMs using configuration data of ten widely deployed open-source systems. Our analysis (1) confirms the potential of using LLMs for configuration validation, (2) explores design space of LLMbased validators like Ciri, and (3) reveals open challenges such as ineffectiveness in detecting certain types of misconfigurations and biases towards popular configuration parameters.

## 46. Large Language Models for Safe Minimization

**Authors:** Aashish Yadavally (University of Texas at Dallas), Xiaokai Rong (The University of Texas at Dallas), Phat Nguyen (The University of Texas at Dallas), Tien N. Nguyen (University of Texas at Dallas)

**Categories:** AI for Software Engineering

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029830

**中文总结:** 提出 SafeMin，让 LLM 与 SMT 求解器协同进行不可行字符串约束的安全最小化；在 LeetCode 字符串基准上 94.3% 可安全最小化，相对 MUS 平均压缩比达 98%。

**Abstract:** Several tasks in program analysis, verification, and testing are modeled as constraint solving problems, utilizing SMT solvers as the reasoning engine. In this work, we aim to investigate the reasoning capabilities of large language models (LLMs) toward reducing the size of an infeasible string constraint system by exploiting inter-constraint interactions such that the remaining ones are still unsatisfiable. We term this safe minimization. Motivated by preliminary observations of hallucination and error propagation in LLMs, we design SafeMin, a framework leveraging an LLM and SMT solver in tandem to ensure a safe and correct minimization. We test the applicability of our approach on string benchmarks from LeetCode in the computation of minimal unsatisfiable subsets (MUSes). We observed that SafeMin helps safely minimize 94.3% of these constraints, with an average minimization ratio of 98% relative to the MUSes. In addition, we assess SafeMin's capabilities in partially enumerating non-unique MUSes, which is baked into our approach via a "sample-and-enumerate'" decoding strategy. Overall, we captured 42.1% more non-unique MUSes than without such LLM-based macro-reasoning. Finally, we demonstrate SafeMin's usefulness in detecting infeasible paths in programs.

## 47. Leveraging Large Language Models for Enhancing the Understandability of Generated Unit Tests

**Authors:** Amirhossein Deljouyi (Delft University of Technology), Roham Koohestani (Delft University of Technology), Mali Izadi (Delft University of Technology), Andy Zaidman (TU Delft)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029767

**中文总结:** 提出 UTGen，结合 EvoSuite 与 LLM 为自动生成单元测试补充上下文、命名与注释；用户实验显示修复 bug 数最多增 33%、耗时降 20%。

**Abstract:** Automated unit test generators, particularly search-based software testing tools like EvoSuite, are capable of generating tests with high coverage. Although these generators alleviate the burden of writing unit tests, they often pose challenges for software engineers in terms of understanding the generated tests. To address this, we introduce UTGen, which combines search-based software testing and large language models to enhance the understandability of automatically generated test cases. We achieve this enhancement through contextualizing test data, improving identifier naming, and adding descriptive comments. Through a controlled experiment with 32 participants, we investigate how the understandability of unit tests affects a software engineer's ability to perform bug-fixing tasks. We selected bug-fixing to simulate a real-world scenario that emphasizes the importance of understandable test cases. We observe that participants working on assignments with test cases fix up to 33% more bugs and use up to 20\% less time when compared to baseline test cases. From the post-test questionnaire, we gathered that participants found that enhanced test names, test data, and variable names improved their bug-fixing process.

## 48. Leveraging Large Language Models to Detect npm Malicious Packages

**Authors:** Nusrat Zahan (North Carolina State University), Philipp Burckhardt (Socket, Inc), Mikola Lysenko (Socket, Inc), Feross Aboukhadijeh (Socket, Inc), Laurie Williams (North Carolina State University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029752

**中文总结:** 提出 SecurityAI 工作流，用 ChatGPT 辅助检测 npm 恶意包；在 5115 个包基准上与 CodeQL 静态分析对比评估检测效果。

**Abstract:** Existing malicious code detection techniques can aid the manual review process by predicting which packages are likely to be malicious. However, these techniques often suffer from high misclassification rates. Therefore, malicious code detection techniques could be enhanced by adopting advanced, more automated approaches to achieve high accuracy and a low misclassification rate. The goal of this study is to assist security analysts in detecting malicious packages through the empirical study of using Large Language Models (LLMs) to detect malicious code in the npm ecosystem. We present SecurityAI, a malicious code review workflow to detect malicious code using ChatGPT. We leverage a benchmark dataset of 5,115 npm packages, of which 2,180 packages have malicious code. We conducted a baseline comparison of GPT-3 and GPT-4 models with the state-of-the-art CodeQL static analysis tool, using 39 custom CodeQL rules developed in prior research to detect malicious Javascript code. We compare the effectiveness of static analysis as a pre-screener with SecurityAI workflow, measuring the number of files that need to be analyzed and the associated costs. Additionally, we performed a qualitative study to understand the types of malicious packages detected or missed by our workflow. Our baseline comparison demonstrates a 16% and 9% improvement over static analysis in precision and F1 scores, respectively. We attained precision and F1 scores of 91% and 94% for GPT-3, and 99% & 97% for GPT-4, respectively, with GPT-3 offering a cost-effective balance. Pre-screening files with a static analyzer reduces the number of files requiring LLM analysis by 77.9% and decreases costs by 60.9% for GPT-3 and 76.1% for GPT-4. Our qualitative analysis identified data theft, hidden backdoors, and suspicious domain connection categories as the top detected malicious packages. The lack of diversity in model-generated responses led to hallucinations, resulting in misclassification cases, with GPT-3 hallucinating more frequently.

## 49. LibreLog: Accurate and Efficient Unsupervised Log Parsing Using Open-Source Large Language Models

**Authors:** Zeyang Ma (Concordia University), Dong Jae Kim (DePaul University), Tse-Hsun (Peter) Chen (Concordia University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029927

**中文总结:** 提出 LibreLog 无监督日志解析方法，基于 Llama3-8B 等开源 LLM 按静态文本分组解析动态变量，兼顾隐私、成本与精度，达到 SOTA 解析准确率。

**Abstract:** Log parsing is a critical step that transforms unstructured log data into structured formats, facilitating subsequent log-based analysis. Traditional syntax-based log parsers are efficient and effective, but they often experience decreased accuracy when processing logs that deviate from the predefined rules. Recently, large language models (LLM) based log parsers have shown superior parsing accuracy. However, existing LLM-based parsers face three main challenges: 1) time-consuming and labor-intensive manual labeling for fine-tuning or in-context learning, 2) increased parsing costs due to the vast volume of log data and limited context size of LLMs, and 3) privacy risks from using commercial models like ChatGPT with sensitive log information. To overcome these limitations, this paper introduces LibreLog, an unsupervised log parsing approach that leverages open-source LLMs (i.e., Llama3-8B) to enhance privacy and reduce operational costs while achieving state-of-the-art parsing accuracy. LibreLog first groups logs with similar static text but varying dynamic variables using a fixed-depth grouping tree. It then parses logs within these groups using three components: i) similarity scoring-based retrieval augmented generation: selects diverse logs within each group based on Jaccard similarity, helping the LLM distinguish between static text and dynamic variables; ii) self-reflection: iteratively query LLMs to refine log templates to improve parsing accuracy; and iii) log template memory: stores parsed templates to reduce LLM queries for improved parsing efficiency. Our evaluation on LogHub-2.0 shows that LibreLog achieves 25% higher parsing accuracy and processes logs 2.7 times faster compared to state-of-the-art LLM-based parsers. In short, LibreLog addresses privacy and cost concerns of using commercial LLMs while achieving state-of- the-arts parsing efficiency and accuracy.

## 50. LiCoEval: Evaluating LLMs on License Compliance in Code Generation

**Authors:** Weiwei Xu (Peking University), Kai Gao (Peking University), Hao He (Carnegie Mellon University), Minghui Zhou (Peking University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029777

**中文总结:** 建立 LiCoEval 基准评估 LLM 生成代码的许可证合规性，定义“显著相似”标准以判定复制关系；评估 14 个主流 LLM，发现即使最优模型仍有 0.88%–2.01% 输出与开源代码显著相似。

**Abstract:** Recent advances in Large Language Models (LLMs) have revolutionized code generation, leading to widespread adoption of AI coding tools by developers. However, LLMs can generate license-protected code without providing the necessary license information, leading to potential intellectual property violations during software production. This paper addresses the critical, yet underexplored, issue of license compliance in LLM-generated code by establishing a benchmark to evaluate the ability of LLMs to provide accurate license information for their generated code. To establish this benchmark, we conduct an empirical study to identify a reasonable standard for "striking similarity" that excludes the possibility of independent creation, indicating a copy relationship between the LLM output and certain open-source code. Based on this standard, we propose an evaluation benchmark LiCoEval, to evaluate the license compliance capabilities of LLMs. Using LiCoEval, we evaluate 14 popular LLMs, finding that even top-performing LLMs produce a non-negligible proportion (0.88% to 2.01%) of code strikingly similar to existing open-source implementations. Notably, most LLMs fail to provide accurate license information, particularly for code under copyleft licenses. These findings underscore the urgent need to enhance LLM compliance capabilities in code generation tasks. Our study provides a foundation for future research and development to improve license compliance in AI-assisted software development, contributing to both the protection of open-source software copyrights and the mitigation of legal risks for LLM users.

## 51. LiSSA: Toward Generic Traceability Link Recovery through Retrieval-Augmented Generation

**Authors:** Dominik Fuchß (Karlsruhe Institute of Technology (KIT)), Tobias Hey (Karlsruhe Institute of Technology (KIT)), Jan Keim (Karlsruhe Institute of Technology (KIT)), Haoyu Liu (Karlsruhe Institute of Technology (KIT)), Niklas Ewald (Karlsruhe Institute of Technology (KIT)), Tobias Thirolf (Karlsruhe Institute of Technology (KIT)), Anne Koziolek (Karlsruhe Institute of Technology)

**Categories:** AI for Software Engineering, Requirements and Specifications

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029919

**中文总结:** 提出 LiSSA 框架，结合 RAG 增强 LLM 实现通用可追溯性链接恢复，在需求-代码、文档-代码等多种任务上验证有效。

**Abstract:** There are a multitude of software artifacts which need to be handled during the development and maintenance of a software system. These artifacts interrelate in multiple, complex ways. Therefore, many software engineering tasks are enabled — and even empowered — by a clear understanding of artifact interrelationships and also by the continued advancement of techniques for automated artifact linking. However, current approaches in automatic Traceability Link Recovery (TLR) target mostly the links between specific sets of artifacts, such as those between requirements and code. Fortunately, recent advancements in Large Language Models (LLMs) can enable TLR approaches to achieve broad applicability. Still, it is a nontrivial problem how to provide the LLMs with the specific information needed to perform TLR. In this paper, we present LiSSA, a framework that harnesses LLM performance and enhances them through Retrieval-Augmented Generation (RAG). We empirically evaluate LiSSA on three different TLR tasks, requirements to code, documentation to code, and architecture documentation to architecture models, and we compare our approach to state-of-the-art approaches. Our results show that the RAG-based approach can significantly outperform the state-of-the-art on the code-related tasks. However, further research is required to improve the performance of RAG-based approaches to be applicable in practice.

## 52. LLM Assistance for Memory Safety

**Authors:** Nausheen Mohammed (Microsoft Research), Akash Lal (Microsoft Research), Aseem Rastogi (Microsoft Research), Subhajit Roy (IIT Kanpur), Rahul Sharma (Microsoft Research)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029895

**中文总结:** 利用 LLM 结合轻量静态分析做整程序变换，将 C 代码移植到安全 C 方言并推断/重写注解，以降低内存安全标注负担。

**Abstract:** Memory safety violations in low-level code, written in languages like C, continues to remain one of the major sources of software vulnerabilities. One method of removing such violations by construction is to port C code to a safe C dialect. Such dialects rely on programmer-supplied annotations to guarantee safety with minimal runtime overhead. This porting, however, is a manual process that imposes significant burden on the programmer and, hence, there has been limited adoption of this technique. The task of porting not only requires inferring annotations, but may also need refactoring/rewriting of the code to make it amenable to such annotations. In this paper, we use Large Language Models (LLMs) towards addressing both these concerns. We show how to harness LLM capabilities to do complex code reasoning as well as rewriting of large codebases. We also present a novel framework for whole-program transformations that leverages lightweight static analysis to break the transformation into smaller steps that can be carried out effectively by an LLM. We implement our ideas in a tool called MSA that targets the CheckedC dialect. We evaluate MSA on several micro-benchmarks, as well as real-world code ranging up to 20K lines of code. We showcase superior performance compared to a vanilla LLM baseline, as well as demonstrate improvement over a state-of-the-art symbolic (non-LLM) technique.

## 53. LLM Based Input Space Partitioning Testing for Library APIs

**Authors:** Jiageng Li (Fudan University), Zhen Dong (Fudan University), Chong Wang (Nanyang Technological University), Haozhen You (Fudan University), Cen Zhang (Georgia Institute of Technology), Yang Liu (Nanyang Technological University), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029822

**中文总结:** 提出 LISP，利用 LLM 理解库 API 代码并进行输入空间划分，再据此引导各分区测试输入生成，缓解传统搜索式方法易生成无效输入、符号执行难以扩展的问题。

**Abstract:** Automated library APIs testing is difficult as it requires exploring a vast space of parameter inputs that may involve objects with complex data types. Existing search based approaches, with limited knowledge of relations between object states and program branches, often suffer from the low efficiency issue, i.e., tending to generate invalid inputs. Symbolic execution based approaches can effectively identify such relations, but fail to scale to large programs. In this work, we present an LLM-based input space partitioning testing approach, LISP, for library APIs. The approach leverages LLMs to understand the code of a library API under test and perform input space partitioning based on its understanding and rich common knowledge. Specifically, we provide the signature and code of the API under test to LLMs, with the expectation of obtaining a text description of each input space partition of the API under test. Then, the generated text description is employed to guide the input generation process for each partition, ultimately resulting in test suites that systematically explore the program behavior of the API. We evaluate LISP on 10 popular open-source Java libraries (e.g., apache/commons-lang with 2.6k stars, guava with 48.8k stars on GitHub). Our experiment results show that LISP is effective in library API testing. It significantly outperforms state-of-the-art tool EvoSuite in terms of branch coverage. On average, LISP achieves 67.82% branch coverage, surpassing EvoSuite by 1.21 times. In total, LISP triggers 404 exceptions or errors in the experiments, and discovers 13 previously unknown vulnerabilities during evaluation, which have been assigned CVE IDs.

## 54. LLM-Agents Driven Automated Simulation Testing and Analysis of small Uncrewed Aerial Systems

**Authors:** Venkata Sai Aswath Duvvuru (Saint Louis University), Bohan Zhang (Saint Louis University, Missouri), Michael Vierhauser (University of Innsbruck), Ankit Agrawal (Saint Louis University, Missouri)

**Categories:** AI for Software Engineering, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029890

**中文总结:** 提出 AUTOSIMTEST，由多 LLM 智能体协作完成小型无人机仿真测试的场景设计、环境搭建、任务规划与结果分析，减轻人工端到端测试负担。

**Abstract:** Thorough simulation testing is crucial for validating the correct behavior of small Uncrewed Aerial Systems (sUAS) across multiple scenarios, including adverse weather conditions (such as wind, and fog), diverse settings (hilly terrain, or urban areas), and varying mission profiles (surveillance, tracking). While various sUAS simulation tools exist to support developers, the entire process of creating, executing, and analyzing simulation tests remains a largely manual and cumbersome task. Developers must identify test scenarios, set up the simulation environment, integrate the System under Test (SuT) with simulation tools, formulate mission plans, and collect and analyze results. These labor-intensive tasks limit the ability of developers to conduct exhaustive testing across a wide range of scenarios. To alleviate this problem, in this paper, we propose AUTOSIMTEST, a Large Language Model (LLM)-driven framework, where multiple LLM agents collaborate to support the sUAS simulation testing process. This includes: (1) creating test scenarios that subject the SuT to unique environmental contexts; (2) preparing the simulation environment as per the test scenario; (3) generating diverse sUAS missions for the SuT to execute; and (4) automatically analyzing simulation results and providing an interactive analytics interface. Further, the design of the framework is flexible for creating and testing scenarios for a variety of sUAS use cases, simulation tools, and SuT input requirements. We evaluated our approach by (a) conducting simulation testing of PX4 and ArduPilot flight-controller-based SuTs, (b) analyzing the performance of each agent, and (c) gathering feedback from sUAS developers. Our findings indicate that AUTOSIMTEST significantly improves the efficiency and scope of the sUAS testing process, allowing for more comprehensive and varied scenario evaluations while reducing the manual effort.

## 55. LLMs Meet Library Evolution: Evaluating Deprecated API Usage in LLM-based Code Completion

**Authors:** Chong Wang (Nanyang Technological University), Kaifeng Huang (Tongji University), Jian Zhang (Nanyang Technological University), Yebo Feng (Nanyang Technological University), Lyuye Zhang (Nanyang Technological University), Yang Liu (Nanyang Technological University), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029774

**中文总结:** 首次系统评估 7 个 LLM 在代码补全中使用已废弃 API 的问题，分析模型、提示与库等因素并提出 ReplaceAPI 等轻量修复方案。

**Abstract:** Large language models (LLMs), pre-trained or fine-tuned on large code corpora, have shown effectiveness in generating code completions. However, in LLM-based code completion, LLMs may struggle to use correct and up-to-date Application Programming Interfaces (APIs) due to the rapid and continuous evolution of libraries. While existing studies have highlighted issues with predicting incorrect APIs, the specific problem of deprecated API usage in LLM-based code completion has not been thoroughly investigated. To address this gap, we conducted the first evaluation study on deprecated API usage in LLM-based code completion. This study involved seven advanced LLMs, 145 API mappings from eight popular Python libraries, and 28,125 completion prompts. The study results reveal the status quo (i.e., API usage plausibility and deprecated usage rate) of deprecated API and replacing API usage in LLM-based code completion from the perspectives of model, prompt, and library, and indicate the root causes behind. Based on these findings, we propose two lightweight fixing approaches, ReplaceAPI and InsertPrompt, which can serve as baseline approaches for future research on mitigating deprecated API usage in LLM-based completion. Additionally, we provide implications for future research on integrating library evolution with LLM-driven software development.

## 56. Magika: AI-Powered Content-Type Detection

**Authors:** Yanick Fratantonio (Google), Luca Invernizzi (Google), Loua Farah (Google), Kurt Thomas (Google), Marina Zhang (Google), Ange Albertini (Google), Francois Galilee (Google), Giancarlo Metitieri (Google), Julien Cretin (Google), Alex Petit-Bianco (Google), David Tao (Google), Elie Bursztein (Google)

**Categories:** AI for Software Engineering, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029883

**中文总结:** 提出 AI 内容类型检测工具 Magika，以仅 1MB 权重的深度学习模型在 CPU 上运行；在 100 余种类型、超 100 万文件测试集上平均 F1 达 99%，优于现有工具并已开源落地。

**Abstract:** The task of content-type detection---which entails identifying the data encoded in an arbitrary byte sequence---is critical for operating systems, development, reverse engineering environments, and a variety of security applications. In this paper, we introduce Magika, a novel AI-powered content-type detection tool. Under the hood, Magika employs a deep learning model that can execute on a single CPU with just 1MB of memory to store the model's weights. We show that Magika achieves an average F1 score of 99% across over a hundred content types and a test set of more than 1M files, outperforming all existing content-type detection tools today. In order to foster adoption and improvements, we open source Magika under an Apache 2 license on GitHub and make our model and training pipeline publicly available. Our tool has already seen adoption by a major email provider for attachment scanning, and it has been integrated with VirusTotal to aid malware analysis.

## 57. Measuring the Runtime Performance of C++ Code Written by Humans using GitHub Copilot

**Authors:** Daniel Erhabor (University of Waterloo), Sreeharsha Udayashankar (University of Waterloo), Mei Nagappan (University of Waterloo), Samer Al-Kiswany (University of Waterloo)

**Categories:** AI for Software Engineering, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029749

**中文总结:** 对 32 名开发者开展用户研究，发现使用 GitHub Copilot 辅助编写的 C++ 代码在测试数据上运行时性能显著慢于不使用 Copilot 的代码。

**Abstract:** GitHub Copilot is an artificially intelligent program- ming assistant used by many developers. While a few studies have evaluated the security risks of using Copilot, there has not been any study to show if it aids developers in producing code with better runtime performance. We evaluate the runtime performance of C++ code produced when developers use GitHub Copilot versus when they do not. To this end, we conducted a user study with 32 participants where each participant solved two C++ programming problems, one with Copilot and the other without it and measured the runtime performance of the participants’ solutions on our test data. Our results suggest that using Copilot may produce C++ code with a statistically significantly slower runtime performance.

## 58. Metamorphic-Based Many-Objective Distillation of LLMs for Code-related Tasks

**Authors:** Annibale Panichella (Delft University of Technology)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029766

**中文总结:** 发现蒸馏后代码 LLM 对等价蜕变代码的鲁棒性显著下降，提出 MORPH，将蜕变测试与多目标优化结合，在代码克隆与漏洞检测蒸馏中平衡准确率、效率与鲁棒性。

**Abstract:** Knowledge distillation compresses large language models (LLMs) into more compact and efficient versions that achieve similar accuracy on code-related tasks. However, as we demonstrate in this study, compressed models are four times less robust than the original LLMs when evaluated with metamorphic code. They have a 440% higher probability of misclassifying code clones due to minor changes in the code fragment under analysis, such as replacing parameter names with synonyms. To address this issue, we propose MORPH, a method that combines metamorphic testing with many-objective optimization for a robust distillation of LLMs for code. MORPH efficiently explores the models’ configuration space and generates Paretooptimal models that effectively balance accuracy, efficiency, and robustness to metamorphic code. Metamorphic testing measures robustness as the number of code fragments for which a model incorrectly makes different predictions between the original and their equivalent metamorphic variants (prediction flips). We evaluate MORPH on two tasks—code clone and vulnerability detection—targeting CodeBERT and GraphCodeBERT for distillation. Our comparison includes MORPH, the state-of-theart distillation method AVATAR, and the fine-tuned non-distilled LLMs. Compared to AVATAR, MORPH produces compressed models that are (i) 47% more robust, (ii) 25% more efficient (fewer FLOPs), while maintaining (iii) equal or higher accuracy (up to +6%), and (iv) similar model size.

## 59. Model Editing for LLMs4Code: How Far are We?

**Authors:** Xiaopeng Li (National University of Defense Technology), Shangwen Wang (National University of Defense Technology), Shasha Li (National University of Defense Technology), Jun Ma (National University of Defense Technology), Jie Yu (National University of Defense Technology), Xiaodong Liu (National University of Defense Technology), Jing Wang (National University of Defense Technology), Bin Ji (National University of Defense Technology), Weimin Zhang (National University of Defense Technology)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029902

**中文总结:** 首次系统评估模型编辑技术在代码 LLM 知识修正中的效果，构建 CLMEEval 基准与数据集，对比多种 SOTA 编辑方法在不同代码任务上的适用性与局限。

**Abstract:** Large Language Models for Code (LLMs4Code) have been found to exhibit outstanding performance in the software engineering domain, especially the remarkable performance in coding tasks. However, even the most advanced LLMs4Code can inevitably contain incorrect or outdated code knowledge. Due to the high cost of training LLMs4Code, it is impractical to re-train the models for fixing these problematic code knowledge. Model editing is a new technical field for effectively and efficiently correcting erroneous knowledge in LLMs, where various model editing techniques and benchmarks have been proposed recently. Despite that, a comprehensive study that thoroughly compares and analyzes the effectiveness of all state-of-the-art model editing techniques for adapting the knowledge within LLMs4Code models across various code-related tasks is notably absent. To bridge this gap, we perform the first systematic study on applying state-of-the-art model editing approaches to repair the inaccuracy of LLMs4Code. To that end, we introduce a benchmark named CLMEEval, which consists of two datasets, i.e., CoNaLa-Edit (CNLE) with 21K+ code generation samples and CodeSearchNet-Edit (CSNE) with 16K+ code summarization samples. With the help of CLMEEval, we evaluate six advanced model editing techniques on three LLMs4Code: CodeLlama (7B), CodeQwen1.5 (7B), and Stable-Code (3B). Our findings include that the external memorization-based GRACE approach achieves the best knowledge editing effectiveness and specificity (the editing does not influence untargeted knowledge), while generalization (whether the editing can generalize to other semantically-identical inputs) is a universal challenge for existing techniques. Furthermore, building on in-depth case analysis, we introduce an enhanced version of GRACE called A-GRACE, which incorporates contrastive learning to better capture the semantics of the inputs. Results demonstrate that A-GRACE notably enhances generalization while maintaining similar levels of effectiveness and specificity compared to the vanilla GRACE.

## 60. Neurosymbolic Modular Refinement Type Inference

**Authors:** Georgios Sakkas (UC San Diego), Pratyush Sahu (UC San Diego), Kyeling Ong (University of California, San Diego), Ranjit Jhala (University of California at San Diego)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029908

**中文总结:** 提出神经符号代理 XO，用大语言模型为 Haskell 包自动生成精炼类型注解并以 LiquidHaskell 验证，将原本需专家数天至数周的标注工作自动化。

**Abstract:** Refinement types -- a type-based generalization of Floyd-Hoare logics -- are an expressive and modular means of statically ensuring a wide variety of correctness, safety, and security properties of software. However, their expressiveness and modularity means that to use them, a developer must laboriously \emph{annotate} all the functions in their code with potentially complex type specifications that specify the contract for that function. We present XO, a neurosymbolic agent that uses LLMs to automatically generate refinement type annotations for all the functions in an entire package or module, using the refinement type checker LiquidHaskell as an oracle to verify the correctness of the generated specifications. We curate a dataset of three Haskell packages where refinement types are used to enforce a variety of correctness properties from data structure invariants to low-level memory safety and use this dataset to evaluate XO. Previously these packages required expert users several days to weeks to annotate with refinement types. Our evaluation shows that when even using models with relatively smaller models like the 3 billion parameter StarCoder LLM, by using fine-tuning, carefully chosen contexts, our neurosymbolic agent generates refinement types for up to 94\% of the functions across entire libraries automatically in just a few hours, thereby showing that LLMs can drastically shrink the human effort needed to use formal verification.

## 61. NIODebugger: A Novel Approach to Repair Non-Idempotent-Outcome Tests with LLM-Based Agent

**Authors:** Kaiyao Ke (University of Illinois at Urbana-Champaign)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029812

**中文总结:** 提出 NIODebugger，首个面向非幂等结果（NIO） flaky 测试的 LLM 智能体修复框架，经检测、探索、修复三阶段定位并消除状态污染根因。

**Abstract:** Flaky tests, characterized by inconsistent results across repeated executions, present significant challenges in software testing, especially during regression testing. Recently, there has been emerging research interest in non-idempotent-outcome (NIO) flaky tests—tests that pass on the initial run but fail on subsequent executions within the same environment. Despite progress in utilizing Large Language Models (LLMs) to address flaky tests, existing methods have not tackled NIO flaky tests. The limited context window of LLMs restricts their ability to incorporate relevant source code beyond the test method itself, often overlooking crucial information needed to address state pollution, which is the root cause of NIO flakiness. This paper introduces NIODebugger, the first framework to utilize an LLM-based agent for fixing flaky tests. NIODebugger features a three-phase design: detection, exploration, and fixing. In the detection phase, dynamic analysis provides critical information (such as stack traces and custom test execution logs) from multiple test runs, which helps in understanding accumulative state pollution. During the exploration phase, the LLM-based agent identifies and provides instructions for extracting relevant source code associated with test flakiness. In the fixing phase, NIODebugger repairs the tests using the information gathered from the previous phases. NIODebugger can be integrated with multiple LLMs, achieving patching success rates ranging from 11.63% to 58.72%. Its best-performing variant, NIODebugger-GPT-4, successfully generated correct patches for 101 out of 172 previously unknown NIO tests across 20 large-scale open-source projects. We submitted pull requests for all generated patches; 58 have been merged, only 1 was rejected, and the remaining 42 are pending. The implementation of NIODebugger is provided as a Maven plugin accessible at https://github.com/NIOTester/NIODebugger.

## 62. Planning a Large Language Model for Static Detection of Runtime Errors in Code Snippets

**Authors:** Smit Soneshbhai Patel (University of Texas at Dallas), Aashish Yadavally (University of Texas at Dallas), Hridya Dhulipala (University of Texas at Dallas), Tien N. Nguyen (University of Texas at Dallas)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029953

**中文总结:** 提出 ORCA，引导 LLM 在控制流图上自主规划并模拟执行代码片段，以静态方式检测在线代码片段中的运行时错误。

**Abstract:** Large Language Models (LLMs) have been excellent in generating and reasoning about source code and the textual descriptions. They can recognize patterns, syntax, and semantics in code, making them effective in several software engineering tasks. However, they exhibit weaknesses in reasoning about the program execution. They primarily operate on static code representations, failing to capture the dynamic behavior and state changes that occur during program execution. In this paper, we advance the capabilities of LLMs in reasoning about program execution. We propose ORCA, a novel approach that instructs an LLM to autonomously formulate a plan to navigate through a control flow graph (CFG) for predictive execution of (in)complete code snippets. It acts as a predictive interpreter to ``execute'' the code. As a downstream task, we use ORCA to statically identify any runtime errors for online code snippets. Early detection of runtime errors and defects in these snippets is crucial to prevent costly fixes later in the development cycle after they were adapted into a codebase. In our novel technique, we guide the LLM to pause at the branching point, focusing on the state of the symbol tables for variables' values, thus minimizing error propagation in the LLM's computation. We also instruct the LLM not to stop at each step in its execution plan, resulting the use of only one prompt to the LLM, thus much cost-saving. Our empirical evaluation showed that ORCA is effective and improves over the state-of-the-art approaches in predicting the execution traces and in runtime error detection.

## 63. Prompt-to-SQL Injections in LLM-Integrated Web Applications: Risks and Defenses

**Authors:** Rodrigo Resendes Pedro (INESC-ID / IST, Universidade de Lisboa), Miguel E. Coimbra (INESC-ID; Instituto Superior Técnico - University of Lisbon), Daniel Castro (INESC-ID / IST, Universidade de Lisboa), Paulo Carreira (INESC-ID / IST, Universidade de Lisboa), Nuno Santos (INESC-ID; Instituto Superior Técnico - University of Lisbon)

**Categories:** AI for Software Engineering, Security and Vulnerability

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029790

**中文总结:** 系统刻画 LLM 集成 Web 应用中的 prompt-to-SQL 注入风险，在 7 个 LLM 与 5 个真实应用中发现漏洞，并讨论防御措施。

**Abstract:** Large Language Models (LLMs) have found widespread applications in various domains, including web applications with chatbot interfaces. Aided by an LLM-integration middleware such as LangChain, user prompts are translated into SQL queries used by the LLM to provide meaningful responses to users. However, unsanitized user prompts can lead to SQL injection attacks, potentially compromising the security of the database. In this paper, we present a comprehensive examination of prompt-to-SQL (P2SQL) injections targeting web applications based on frameworks such as LangChain and LlamaIndex. We characterize P2SQL injections, exploring their variants and impact on application security through multiple concrete examples. We evaluate seven state-of-the-art LLMs, demonstrating the risks of P2SQL attacks across language models. By employing both manual and automated methods, we discovered P2SQL vulnerabilities in five real-world applications. Our findings indicate that LLM-integrated applications are highly susceptible to P2SQL injection attacks, warranting the adoption of robust defenses. To counter these attacks, we propose four effective defense techniques that can be integrated as extensions to the LangChain framework.

## 64. QEDCartographer: Automating Formal Verification Using Reward-Free Reinforcement Learning

**Authors:** Alex Sanchez-Stern (University of Massachusetts at Amherst), Abhishek Varghese (University of Massachusetts), Zhanna Kaufman (University of Massachusetts), Shizhuo Zhang (University of Illinois Urbana-Champaign), Talia Lily Ringer (University of Illinois Urbana-Champaign), Yuriy Brun (University of Massachusetts)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029816

**中文总结:** 提出 QEDCartographer，结合监督与强化学习并利用证明分支结构做无奖励搜索以自动合成 Coq 证明；在 CoqGym 上比基线多证明 186 个定理。

**Abstract:** Formal verification is a promising method for producing highly reliable software, but the difficulty of manually writing verification proofs severely limits its utility in practice. Recent methods have automated some proof synthesis by guiding a search through the proof space using machine learning and a theorem prover. Unfortunately, the theorem prover provides only the crudest estimate of progress, resulting in effectively undirected search. This makes proofs hard to find, and, when they are found, longer than necessary. Reinforcement learning could help estimate progress, but sparse rewards make this method ineffective. To address this problem, we create QEDCartographer, an novel automated proof-synthesis tool that combines supervised and reinforcement learning. QEDCartographer's key insight is that incorporating the branching structure of proofs into its learning enables reward-free search, mitigating the sparse reward challenge. We evaluate QEDCartographer on the CoqGym benchmark of 68,501 theorems from 124 open-source Coq projects. QEDCartographer proves 186 more theorems than Proverbot9001, a state-of-the-art proof synthesis tool, an increase of 8%. Further, the tools are complementary, together proving 12% more theorems than Proverbot9001 alone. For theorems both can prove, QEDCartographer produces 26% shorter proofs 27% faster.

## 65. Rango: Adaptive Retrieval-Augmented Proving for Automated Software Verification

**Authors:** Kyle Thompson (University of California, San Diego), Nuno Saavedra (INESC-ID and IST, University of Lisbon), Pedro Carrott (Imperial College London), Kevin Fisher (University of California San Diego), Alex Sanchez-Stern (University of Massachusetts), Yuriy Brun (University of Massachusetts), João F. Ferreira (INESC-ID and IST, University of Lisbon), Sorin Lerner (University of California at San Diego), Emily First (University of California, San Diego)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029818

**中文总结:** 提出 Coq 自动证明合成工具 Rango，每步检索相关前提与项目内相似证明并自适应微调 LLM 上下文；发布 CoqStoq 数据集，在基准上合成 27.7% 证明，较先前方法多 10%。

**Abstract:** Formal verification using proof assistants, such as Coq, allows for high-quality software. However, the verification process is expensive, requiring significant expertise and manual effort to write proofs. Recent work has explored automating proof synthesis using machine learning, and even more recently, large language models (LLMs), showing that retrieving relevant premises (such as lemmas and definitions) is helpful for these models. We present Rango, a fully automated proof synthesis tool for Coq that uses, not only relevant premises but also similar proofs from the current project. Rango uses retrieval augmentation at every step of the proof to automatically determine which proofs and premises to include in the context of its fine-tuned LLM. In this way, Rango adapts to the project _and_ to the evolving state of the proof. We create a new dataset, CoqStoq, of 2,205 open-source Coq projects from GitHub, which includes both training data and a curated evaluation benchmark of well-maintained projects. On this benchmark, Rango synthesizes 27.7% of the proofs, which is 10% more proofs than prior state-of-the-art tool Tactician. Our evaluation also shows that adding relevant proofs to the context in Rango leads to a 45% increase in the number of theorems proven.

## 66. Reasoning Runtime Behavior of a Program with LLM: How Far Are We?

**Authors:** Junkai Chen (Zhejiang University), Zhiyuan Pan (Zhejiang University), Xing Hu (Zhejiang University), Zhenhao Li (York University), Ge Li (Peking University), Xin Xia (Huawei)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029885

**中文总结:** 提出 REval 框架，评估 code LLM 对程序运行时中间行为推理及逻辑一致性；大规模实验显示多数模型在运行时行为推理上表现不佳。

**Abstract:** Large language models for code (i.e., code LLMs) have shown strong code understanding and generation capabilities. To evaluate the capabilities of code LLMs in various aspects, many benchmarks have been proposed (e.g., HumanEval and ClassEval). Code reasoning is one of the most essential abilities of code LLMs, but existing benchmarks for code reasoning are not sufficient. Typically, they focus on predicting the input and output of a program, ignoring the evaluation of the intermediate behavior during program execution, as well as the logical consistency (e.g., the model should not give the correct output if the prediction of execution path is wrong) when performing the reasoning. To address these problems, in this paper, we propose a framework, namely REval, for evaluating code reasoning abilities and consistency of code LLMs with program execution. We utilize existing code benchmarks and adapt them to new benchmarks within our framework. A large-scale empirical study is conducted and most LLMs show unsatisfactory performance on both Runtime Behavior Reasoning (i.e., an average accuracy of 44.4\%) and Incremental Consistency Evaluation (i.e., an average IC score of 10.3). Evaluation results of current code LLMs reflect the urgent need for the community to strengthen the code reasoning capability of code LLMs.

## 67. RepairAgent: An Autonomous, LLM-Based Agent for Program Repair

**Authors:** Islem BOUZENIA (University of Stuttgart), Prem Devanbu (University of California at Davis), Michael Pradel (University of Stuttgart)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029914

**中文总结:** 提出首个基于 LLM 的自主程序修复智能体 RepairAgent，可自主规划并调用工具收集信息、生成修复并验证，在 Defects4J 上取得优异修复效果。

**Abstract:** Automated program repair has emerged as a powerful technique to mitigate the impact of software bugs on system reliability and user experience. This paper introduces RepairAgent, the first work to address the program repair challenge through an autonomous agent based on a large language model (LLM). Unlike existing deep learning-based approaches, which prompt a model with a fixed prompt or in a fixed feedback loop, our work treats the LLM as an agent capable of autonomously planning and executing actions to fix bugs by invoking suitable tools. RepairAgent freely interleaves gathering information about the bug, gathering repair ingredients, and validating fixes, while deciding which tools to invoke based on the gathered information and feedback from previous fix attempts. Key contributions that enable RepairAgent include a set of tools that are useful for program repair, a dynamically updated prompt format that allows the LLM to interact with these tools, and a finite state machine that guides the agent in invoking the tools. Our evaluation on the popular Defects4J dataset demonstrates RepairAgent’s effectiveness in autonomously repairing 164 bugs, including 39 bugs not fixed by prior techniques. Interacting with the LLM imposes an average cost of 270,000 tokens per bug, which, under the current pricing of OpenAI’s GPT-3.5 model, translates to 14 cents per bug. To the best of our knowledge, this work is the first to present an autonomous, LLM-based agent for program repair, paving the way for future agent-based techniques in software engineering.

## 68. Repository-Level Graph Representation Learning for Enhanced Security Patch Detection

**Authors:** Xin-Cheng Wen (Harbin Institute of Technology), Zirui Lin (Harbin Institute of Technology, Shenzhen), Cuiyun Gao (Harbin Institute of Technology), Hongyu Zhang (Chongqing University), Yong Wang (Anhui Polytechnic University), Qing Liao (Harbin Institute of Technology)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029757

**中文总结:** 提出仓库级安全补丁检测框架 RepoSPD，构建 RepoCPG 图并融合图与序列分支以捕捉跨文件补丁依赖。

**Abstract:** Software vendors often silently release security patches without providing sufficient advisories (e.g., Common Vulnerabilities and Exposures) or delayed updates via resources (e.g., National Vulnerability Database). Therefore, it has become crucial to detect these security patches to ensure secure software maintenance. However, existing methods face the following challenges: (1) They primarily focus on the information within the patches themselves, overlooking the complex dependencies in the repository. (2) Security patches typically involve multiple functions and files, increasing the difficulty in well learning the representations. To alleviate the above challenges, this paper proposes a \textit{Repo}sitory-level Security Patch Detection framework named \textit{RepoSPD}, which comprises three key components: 1) a repository-level graph construction, RepoCPG, which represents software patches by merging pre-patch and post-patch source code at the repository level; 2) a structure-aware patch representation, which fuses the graph and sequence branch and aims at comprehending the relationship among multiple code changes; 3) progressive learning, which facilitates the model in balancing semantic and structural information. To evaluate RepoSPD, we employ two widely-used datasets in security patch detection: SPI-DB and PatchDB. We further extend these datasets to the repository level, incorporating a total of 20,238 and 28,781 versions of repository in C/C++ programming languages, respectively, denoted as SPI-DB* and PatchDB*. We compare RepoSPD with six existing security patch detection methods and five static tools. Our experimental results demonstrate that RepoSPD outperforms the state-of-the-art baseline, with improvements of 11.90\%, and 3.10\% in terms of accuracy on the two datasets, respectively. These results underscore the effectiveness of RepoSPD in detecting security patches. Furthermore, RepoSPD can detect 151 security patches, which outperforms the best-performing baseline by 21.36\% with respect to accuracy.

## 69. Revisiting Unnaturalness for Automated Program Repair in the Era of Large Language Models

**Authors:** Aidan Z.H. Yang (Carnegie Mellon University), Sophia Kolak (Carnegie Mellon University), Vincent J. Hellendoorn (Carnegie Mellon University), Ruben Martins (Carnegie Mellon University), Claire Le Goues (Carnegie Mellon University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029753

**中文总结:** 利用大语言模型熵值改进自动程序修复的缺陷定位、补丁生成与排序，仅依赖上下文前缀后缀以降低训练数据泄露风险。

**Abstract:** Language models have improved by orders of magnitude with the recent emergence of Transformer-based Large Language Models (LLMs). LLMs have demonstrated their ability to generate "natural" code that is highly similar to code written by professional developers. One intermediate value an LLM can emit is entropy, which measures the naturalness of a token of code. We hypothesize that entropy can be used to improve the performance of Automated Program Repair (APR) tasks. While much progress has been made in Automated Program Repair (APR), fault localization techniques suffer from a lack of diversity in ranking scores, patch generation tools tend to be inefficient as all tests need to run before determining if a patch is likely to be correct, and patch ranking often suffers from the test-suite over-fitting problem. However, using an LLM directly for APR introduces concerns for training data leakage. In this work, we introduce a novel way of using the entropy of LLMs in combination with prior APR tools to improve all stages of APR. By using only the prefix and suffix context of a line or block of code to describe naturalness, we can use LLMs to localize faults and rank patches all while eliminating the dependency for test-suites. We show that entropy is highly complementary with prior fault localization tools. Our proposed method achieves a 108% top-1 score improvement over SBFL. When using entropy for patch ranking and classification, our proposed method can rank correct patches more effectively than state-of-the-art machine learning tools with an 49% improvement in top-1. Our work suggests that LLMs can be an effective addition to compliment prior APR tasks while minimizing both the test-suite over-fitting problem and the LLM data leakage problem.

## 70. RLCoder: Reinforcement Learning for Repository-Level Code Completion

**Authors:** Yanlin Wang (Sun Yat-sen University), Yanli Wang (Sun Yat-sen University), Daya Guo, Jiachi Chen (Sun Yat-sen University), Ruikai Zhang (Huawei Cloud Computing Technologies), Yuchi Ma (Huawei Cloud Computing Technologies), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11029811

**中文总结:** 提出 RLCoder，用强化学习在无标注条件下训练仓库级代码补全检索器，以目标代码困惑度反馈迭代提升检索质量。

**Abstract:** Repository-level code completion aims to generate code for unfinished code snippets within the context of a specified repository. Existing approaches mainly rely on retrieval-augmented generation strategies due to limitations in input sequence length. However, traditional lexical-based retrieval methods like BM25 struggle to capture code semantics, while model-based retrieval methods face challenges due to the lack of labeled data for training. Therefore, we propose RLCoder, a novel reinforcement learning framework, which can enable the retriever to learn to retrieve useful content for code completion without the need for labeled data. Specifically, we iteratively evaluate the usefulness of retrieved content based on the perplexity of the target code when provided with the retrieved content as additional context, and provide feedback to update the retriever parameters. This iterative process enables the retriever to learn from its successes and failures, gradually improving its ability to retrieve relevant and high-quality content. Considering that not all situations require information beyond code files and not all retrieved context is helpful for generation, we also introduce a stop signal mechanism, allowing the retriever to decide when to retrieve and which candidates to retain autonomously. Extensive experimental results demonstrate that RLCoder consistently outperforms state-of-the-art methods on CrossCodeEval and RepoEval, achieving 12.2\% EM improvement over previous methods. Moreover, experiments show that our framework can generalize across different programming languages and further improve previous methods like RepoCoder.

## 71. ROCODE: Integrating Backtracking Mechanism and Program Analysis in Large Language Models for Code Generation

**Authors:** Xue Jiang, Yihong Dong (Peking University), Yongding Tao (University of Electronic Science and Technology of China), Huanyu Liu (Xidian University), Zhi Jin (Peking University), Ge Li (Peking University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029868

**中文总结:** 提出 ROCODE，在 LLM 代码生成过程中集成回溯机制与程序分析，一旦出错立即回滚修正而非事后修订，避免自回归生成中错误累积与资源浪费。

**Abstract:** Large language models (LLMs) have achieved impressive performance in code generation recently, offering programmers revolutionary assistance in software development. However, due to the auto-regressive nature of LLMs, they are susceptible to error accumulation during code generation. Once an error is produced, LLMs can merely continue to generate the subsequent code conditioned on it, given their inability to adjust previous outputs. This generation process differs from the common practice in human coding, which involves review and adjustment during the coding process according to quality and requirements. Existing LLM-based approaches that typically consider post-revising after code generation fail to resolve errors in time, leading to the challenging resolution of accumulated errors and the significant wastage of resources. Ideally, LLMs should rollback and resolve the occurred error immediately during code generation, rather than proceed on the basis of the error and wait for post-revising after generation. In this paper, we propose \ourapproachbf, which integrates the backtracking mechanism and program analysis into LLMs for code generation. Specifically, we employ program analysis to perform incremental error detection during the generation process. When an error is detected, the backtracking mechanism is triggered to priming rollback strategies and constraint regeneration, thereby avoiding the recurrence of the same error. Experiments on multiple code generation benchmarks show that \ourapproachbf can significantly reduce the errors generated by LLMs, with a compilation pass rate of over 98.9\%. The test pass rate is improved by up to 23.8\% compared to the best baseline approach. Compared to the post-revising baseline, the cost is reduced by 19.3\%. Moreover, our approach is model-agnostic and achieves consistent improvements across six LLMs.

## 72. RustAssistant: Using LLMs to Fix Compilation Errors in Rust Code

**Authors:** Pantazis Deligiannis (Microsoft Research), Akash Lal (Microsoft Research), Nikita Mehrotra (Microsoft Research), Rishi Poddar (Microsoft Research), Aseem Rastogi (Microsoft Research)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029935

**中文总结:** 提出 RustAssistant，结合提示工程与 LLM—Rust 编译器迭代反馈自动修复编译错误；在开源 Rust 项目上峰值准确率约 74%，并发布编译错误数据集。

**Abstract:** The Rust programming language, with its safety guarantees, has established itself as a viable choice for low-level systems programming language over the traditional, unsafe alternatives like C/C++. These guarantees come from a strong ownership-based type system, as well as primitive support for features like closures, pattern matching, etc., that make the code more concise and amenable to reasoning. These unique Rust features also pose a steep learning curve for programmers. This paper presents a tool called RustAssistant that leverages the emergent capabilities of Large Language Models (LLMs) to automatically suggest fixes for Rust compilation errors. RustAssistant uses a careful combination of prompting techniques as well as iteration between an LLM and the Rust compiler to deliver high accuracy of fixes. RustAssistant is able to achieve an impressive peak accuracy of roughly 74% on real-world compilation errors in popular open-source Rust repositories. We also contribute a dataset of Rust compilation errors to enable further research.

## 73. Search-Based LLMs for Code Optimization

**Authors:** Shuzheng Gao (The Chinese University of Hong Kong), Cuiyun Gao (Harbin Institute of Technology), Wenchao Gu (The Chinese University of Hong Kong), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029800

**中文总结:** 将代码优化建模为搜索问题，提出基于 LLM 的搜索式优化方法，以克服一步生成难以捕获复杂优化策略的局限。

**Abstract:** The code written by developers usually suffers from efficiency problems and contain various performance bugs. These inefficiencies necessitate the research of automated refactoring methods for code optimization. Early research in code optimization employs rule-based methods and focuses on specific inefficiency issues, which are labor-intensive and suffer from the low coverage issue. Recent work regards the task as a sequence generation problem, and resorts to deep learning (DL) techniques such as large language models (LLMs). These methods typically prompt LLMs to directly generate optimized code. Although these methods show state-of-the-art performance, such one-step generation paradigm is hard to achieve an optimal solution. First, complex optimization methods such as combinatorial ones are hard to be captured by LLMs. Second, the one-step generation paradigm poses challenge in precisely infusing the knowledge required for effective code optimization within LLMs, resulting in under-optimized code. To address these problems, we propose to model this task from the search perspective, and propose a search-based LLMs framework named SBLLM that enables iterative refinement and discovery of improved optimization methods. SBLLM synergistically integrate LLMs with evolutionary search and consists of three key components: 1) an execution-based representative sample selection part that evaluates the fitness of each existing optimized code and prioritizes promising ones to pilot the generation of improved code; 2) an adaptive optimization pattern retrieval part that infuses targeted optimization patterns into the model for guiding LLMs towards rectifying and progressively enhancing their optimization methods; and 3) a genetic operator-inspired chain-of-thought prompting part that aids LLMs in combining different optimization methods and generating improved optimization methods. Our evaluation of SBLLM on a dataset of Python and C++ code demonstrates its effectiveness in improving code efficiency. Specifically, the results indicate that SBLLM can improve program execution efficiency by up to 109.59% and consistently outperform all baseline methods by 8.72% ∼ 28.06% and 1.15% ∼ 9.56% with different LLMs in terms of top-5 speedup rate on Python and C++, respectively.

## 74. SECRET: Towards Scalable and Efficient Code Retrieval via Segmented Deep Hashing

**Authors:** Wenchao Gu (The Chinese University of Hong Kong), Ensheng Shi (Xi’an Jiaotong University), Yanlin Wang (Sun Yat-sen University), Lun Du (Microsoft Research), Shi Han (Microsoft Research), Hongyu Zhang (Chongqing University), Dongmei Zhang (Microsoft Research), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11029856

**中文总结:** 提出 SECRET 分段深度哈希方法，将长哈希码拆分为短段并建立索引，提升大规模代码检索的可扩展性与效率。

**Abstract:** Code retrieval, which retrieves code snippets based on users’ natural language descriptions, is widely used by developers and plays a pivotal role in real-world software development. The advent of deep learning has shifted the retrieval paradigm from lexical-based matching towards leveraging deep learning models to encode source code and queries into vector representations, facilitating code retrieval according to vector similarity. Despite the effectiveness of these models, managing large-scale code bases presents significant challenges. Previous research propose deep hashing-based methods, which generate hash codes for queries and code snippets and use Hamming distance for rapid recall of code candidates. However, this approach’s reliance on linear scanning of the entire code base limits its scalability. To further improve the efficiency of large scale code retrieval, we propose a novel approach SECRET (Scalable and Efficient Code Retrieval via SegmEnTed deep hashing). SECRET converts long hash codes calculated by existing deep hashing approaches into several short hash code segments through an iterative training strategy. After training, SECRET recalls code candidates by looking up the hash tables for each segment, the time complexity of recall can thus be greatly reduced. Extensive experimental results demonstrate that SECRET can drastically reduce the retrieval time by at least 95% while achieving comparable or even higher performance of existing deep hashing approaches. Besides, SECRET also exhibits superior performance and efficiency compared to the classical hash table-based approach known as LSH under the same number of hash tables.

## 75. SeeAction: Towards Reverse Engineering How-What-Where of HCI Actions from Screencasts for UI Automation

**Authors:** Dehai Zhao (CSIRO's Data61), Zhenchang Xing (CSIRO's Data61), Qinghua Lu (Data61, CSIRO), Xiwei (Sherry) Xu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** AI for Software Engineering, Testing and Quality

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029891

**中文总结:** 提出 SeeAction 视觉模型，从录屏中识别 11 种命令、11 种控件并生成位置描述，联合学习实现 UI 操作结构化还原；在 7260 条跨 Word、Firefox 等应用的录屏—动作对上验证有效性与泛化性。

**Abstract:** UI automation is a useful technique for UI testing, bug reproduction and robotic process automation. Recording the user actions with an application assists rapid development of UI automation scripts, but existing recording techniques are intrusive, rely on OS or GUI framework accessibility support or assume specific app implementations. Reversing-engineering user actions from screencasts is non-intrusive, but a key reverse-engineering step is currently missing - recognize human-understandable structured user actions ([command] [widget][location]) from action screencasts. To fill the gap, we propose a deep learning-based computer vision model which can recognize 11 commands and 11 widgets, and generate location phrases from action screencasts, through joint learning and multi-task learning. We label a large dataset with 7260 video-action pairs, which record the user interactions with Word, Zoom, Firefox, Photoshop, and Window 10 Settings. Through extensive experiments, we confirm the effectiveness and generality of our model, and demonstrate the usefulness of a screencast-to-action-script tool built upon our model for bug reproduction.

## 76. Show Me Your Code! Kill Code Poisoning: A Lightweight Method Based on Code Naturalness

**Authors:** Weisong Sun (Nanjing University), Yuchen Chen (Nanjing University), Mengzhe Yuan (Nanjing University), Chunrong Fang (Nanjing University), Zhenpeng Chen (Nanyang Technological University), Chong Wang (Nanyang Technological University), Yang Liu (Nanyang Technological University), Baowen Xu (State Key Laboratory for Novel Software Technology, Nanjing University), Zhenyu Chen (Nanjing University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029807

**中文总结:** 提出轻量级代码投毒检测 KillBadCode，基于代码自然性被破坏的洞察，用 n-gram CodeLM 识别训练数据中的后门样本。

**Abstract:** Neural code models (NCMs) have demonstrated extraordinary capabilities in code intelligence tasks. Meanwhile, the security of NCMs and NCMs-based systems has garnered increasing attention. In particular, NCMs are often trained on large-scale data from potentially untrustworthy sources, providing attackers with the opportunity to manipulate them by inserting crafted samples into the data. This type of attack is called a code poisoning attack (also known as a backdoor attack). It allows attackers to implant backdoors in NCMs and thus control model behavior, which poses a significant security threat. However, there is still a lack of effective techniques for detecting various complex code poisoning attacks. In this paper, we propose an innovative and lightweight technique for code poisoning detection named KillBadCode. KillBadCode is designed based on our insight that code poisoning disrupts the naturalness of code. Specifically, KillBadCode first builds a code language model (CodeLM) on a lightweight n-gram language model and trains it on a few clean code snippets. Then, given poisoned data, KillBadCode utilizes CodeLM to identify those tokens in (poisoned) code snippets that will make the code snippets more natural after being deleted as trigger tokens. Considering that the removal of some normal tokens in a single sample might also enhance code naturalness, leading to a high false positive rate (FPR), we aggregate the cumulative improvement of each token across all samples. Finally, KillBadCode purifies the poisoned data by removing all poisoned samples containing the identified trigger tokens. We conduct extensive experiments to evaluate the effectiveness and efficiency of KillBadCode, involving two types of advanced code poisoning attacks (a total of five poisoning strategies) and datasets from four representative code intelligence tasks. The experimental results demonstrate that across 20 code poisoning detection scenarios, KillBadCode achieves an average FPR of 8.30% and an average Recall of 100%, significantly outperforming four baselines. More importantly, KillBadCode is very efficient, with a minimum time consumption of only 5 minutes, and is 25 times faster than the best baseline on average. These highlight the great potential of KillBadCode in efficiently killing various code poisoning attacks.

## 77. SOEN-101: Code Generation by Emulating Software Process Models Using Large Language Model Agents

**Authors:** Feng Lin (Concordia University), Dong Jae Kim (DePaul University), Tse-Hsun (Peter) Chen (Concordia University)

**Categories:** AI for Software Engineering, Software Engineering for AI, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029771

**中文总结:** 提出 FlowGen 多智能体框架，模拟瀑布、TDD 与 Scrum 流程生成代码；FlowGen_Scrum 在 HumanEval 等基准 Pass@1 达 75.2。

**Abstract:** Software process models are essential to facilitate collaboration and communication among software teams to solve complex development tasks. Inspired by these software engineering practices, we present FlowGen – a code generation framework that emulates software process models based on multiple Large Language Model (LLM) agents. We emulate three process models, FlowGen$_{Waterfall}$, FlowGen$_{TDD}$, and FlowGen$_{Scrum}$, by assigning LLM agents to embody roles (i.e., requirement engineer, architect, developer, tester, and scrum master) that correspond to everyday development activities and organize their communication patterns. The agents work collaboratively using chain-of-thought and prompt composition with continuous self-refinement to improve the code quality. We use GPT-3.5 as our underlying LLM and several baselines (RawGPT, CodeT, Reflexion) to evaluate code generation on four benchmarks: HumanEval, HumanEval-ET, MBPP, and MBPP-ET. Our findings show that FlowGen$_{Scrum}$ excels compared to other process models, achieving a Pass@1 of 75.2, 65.5, 82.5, and 56.7 in HumanEval, HumanEval-ET, MBPP, and MBPP-ET, respectively (an average of 15% improvement over RawGPT). Compared with other state-of-the-art techniques, FlowGen$_{Scrum}$ achieves a higher Pass@1 in MBPP compared to CodeT, with both outperforming Reflexion. Notably, integrating CodeT into FlowGen$_{Scrum}$ resulted in statistically significant improvements, achieving the highest Pass@1 scores. Our analysis also reveals that the development activities impacted code smell and exception handling differently, with design and code review adding more exception handling and reducing code smells. Finally, FlowGen models maintain stable Pass@1 scores across GPT-3.5 versions and temperature values, highlighting the effectiveness of software process models in enhancing the quality and stability of LLM-generated code.

## 78. Software Model Evolution with Large Language Models: Experiments on Simulated, Public, and Industrial Datasets

**Authors:** Christof Tinnes (Saarland University), Alisa Carla Welter (Saarland University), Sven Apel (Saarland University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029888

**中文总结:** 提出 RaMc，结合大语言模型、软件模型历史与检索增强生成支持模型补全与演化；在工业数据上语义正确率达 62.30%，类型正确率最高 86.19%。

**Abstract:** Modeling structure and behavior of software systems plays a crucial role in the industrial practice of software engineering. As with other software engineering artifacts, software models are subject to evolution. Supporting modelers in evolving software models with recommendations for model completions is still an open problem, though. In this paper, we explore the potential of large language models for this task. In particular, we propose an approach, \textsc{RaMc}, leveraging large language models, model histories of software systems, and retrieval-augmented generation for model completion. Through experiments on three datasets, including an industrial application, one public open-source community dataset, and one controlled collection of simulated model repositories, we evaluate the potential of large language models for model completion. We found that large language models are indeed a promising technology for supporting software model evolution (62.30% semantically correct completions on real-world industrial data and up to 86.19% type-correct completions). Furthermroe, we found that the general inference capabilities of large language models are useful, for example, when dealing with concepts for which there are few, noisy, or no examples at all.

## 79. Source Code Summarization in the Era of Large Language Models

**Authors:** Weisong Sun (Nanjing University), Yun Miao (Nanjing University), Yuekang Li (UNSW), Hongyu Zhang (Chongqing University), Chunrong Fang (Nanjing University), Yi Liu (Nanyang Technological University), Gelei Deng (Nanyang Technological University), Yang Liu (Nanyang Technological University), Zhenyu Chen (Nanjing University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029737

**中文总结:** 系统研究 LLM 时代代码摘要工作流，发现 GPT-4 自动评估最贴近人工，且高级提示技术未必优于简单 zero-shot 提示。

**Abstract:** To support software developers in understanding and maintaining programs, various automatic (source) code summarization techniques have been proposed to generate a concise natural language summary (i.e., comment) for a given code snippet. Recently, the emergence of large language models (LLMs) has led to a great boost in the performance of code-related tasks. In this paper, we undertake a systematic and comprehensive study on code summarization in the era of LLMs, which covers multiple aspects involved in the workflow of LLM-based code summarization. Specifically, we begin by examining prevalent automated evaluation methods for assessing the quality of summaries generated by LLMs and find that the results of the GPT-4 evaluation method are most closely aligned with human evaluation. Then, we explore the effectiveness of five prompting techniques (zero-shot, few-shot, chain-of-thought, critique, and expert) in adapting LLMs to code summarization tasks. Contrary to expectations, advanced prompting techniques may not outperform simple zero-shot prompting. Next, we investigate the impact of LLMs' model settings (including top\_p and temperature parameters) on the quality of generated summaries. We find the impact of the two parameters on summary quality varies by the base LLM and programming language, but their impacts are similar. Moreover, we canvass LLMs' abilities to summarize code snippets in distinct types of programming languages. The results reveal that LLMs perform suboptimally when summarizing code written in logic programming languages compared to other language types (e.g., procedural and object-oriented programming languages). Finally, we unexpectedly find that \codellama{} with 7B parameters can outperform advanced GPT-4 in generating summaries describing code implementation details and asserting code properties. We hope that our findings can provide a comprehensive understanding of code summarization in the era of LLMs.

## 80. SpecGen: Automated Generation of Formal Program Specifications via Large Language Models

**Authors:** Lezhi Ma (Nanjing University), Shangqing Liu (Nanyang Technological University), Yi Li (Nanyang Technological University), Xiaofei Xie (Singapore Management University), Lei Bu (Nanjing University)

**Categories:** AI for Software Engineering, Program Analysis and Verification, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029962

**中文总结:** 提出 SpecGen，利用 LLM 代码理解能力通过对话式两阶段流程自动生成复杂程序的形式化规范，摆脱对预定义模板与语法的依赖。

**Abstract:** In the software development process, formal program specifications play a crucial role in various stages, including requirement analysis, software testing, and verification. However, manually crafting formal program specifications is rather difficult, making the job time-consuming and labor-intensive. Moreover, it is even more challenging to write specifications that correctly and comprehensively describe the semantics of complex programs. To reduce the burden on software developers, automated specification generation methods have emerged. However, existing methods usually rely on predefined templates or grammar, making them struggle to accurately describe the behavior and functionality of complex real-world programs. To tackle this challenge, we introduce SpecGen, a novel technique for formal program specification generation based on Large Language Models (LLMs). Our key insight is to overcome the limitations of existing methods by leveraging the code comprehension capability of LLMs. The process of SpecGen consists of two phases. The first phase employs a conversational approach that guides the LLM to generate appropriate specifications for a given program, aiming to utilize the ability of LLM to generate high-quality specifications. The second phase, designed for where the LLM fails to generate correct specifications, applies four mutation operators to the model-generated specifications and selects verifiable specifications from the mutated ones through a novel heuristic selection strategy by assigning different weights of variants in an efficient manner. We evaluate SpecGen on two datasets, including the SV-COMP Java category benchmark and a manually constructed dataset containing 120 programs. Experimental results demonstrate that SpecGen succeeds in generating verifiable specifications for 279 out of 385 programs, outperforming the existing LLM-based approaches and conventional specification generation tools like Houdini and Daikon. Further investigations on the quality of generated specifications indicate that SpecGen can comprehensively articulate the behaviors of the input program.

## 81. SpecRover: Code Intent Extraction via LLMs

**Authors:** Haifeng Ruan (National University of Singapore), Yuntong Zhang (National University of Singapore), Abhik Roychoudhury (National University of Singapore)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029735

**中文总结:** 提出 SpecRover，在 LLM 智能体中迭代执行代码搜索与规范推断以提取代码意图，并由审查智能体验证补丁与置信度；在完整 SWE-Bench 2294 个 GitHub issue 上评估其程序改进能力。

**Abstract:** Autonomous program improvement typically involves automatically producing bug fixes and feature additions. Such program improvement can be accomplished by a combination of large language model (LLM) and program analysis capabilities, in the form of an LLM agent. Since program repair or program improvement typically requires a specification of intended behavior - specification inference can be useful for producing high quality program patches. In this work, we examine efficient and low-cost workflows for iterative specification inference within an LLM agent. Given a GitHub issue to be resolved in a software project, our goal is to conduct iterative code search accompanied by specification inference - thereby inferring intent from both the project structure and behavior. The intent thus captured is examined by a reviewer agent with the goal of vetting the patches as well as providing a measure of confidence in the vetted patches. Our approach SpecRover is built on the open-source LLM agent AutoCodeRover. In an evaluation on the full SWE-Bench consisting of 2294 GitHub issues, it shows more than 50% improvement in efficacy over AutoCodeRover. Compared to the open-source agents available, our work shows modest cost ($0.65 per issue) in resolving an average GitHub issue in SWE-Bench lite. The production of explanation by SpecRover allows for a better "signal" to be given to the developer, on when the suggested patches can be accepted with confidence. SpecRover also seeks to demonstrate the continued importance of specification inference in automated program repair, even as program repair technologies enter the LLM era.

## 82. Synthesizing Document Database Queries using Collection Abstractions

**Authors:** Qikang Liu (Simon Fraser University), Yang He (Simon Fraser University), Yanwen Cai (Simon Fraser University), Byeongguk Kwak (Simon Fraser University), Yuepeng Wang (Simon Fraser University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029877

**中文总结:** 提出面向文档数据库的查询合成方法，通过代数式 DSL 与集合抽象剪枝搜索空间，从少量输入输出示例自动生成查询；在 110 个基准中成功合成 108 个，平均耗时数十秒。

**Abstract:** Document databases are increasingly popular in various applications, but their queries are challenging to write due to the flexible and complex data model underlying document databases. This paper presents a synthesis technique that aims to generate document database queries from input-output examples automatically. A new domain-specific language is designed to express a representative set of document database queries in an algebraic style. Furthermore, the synthesis technique leverages a novel abstraction of collections for deduction to efficiently prune the search space and quickly generate the target query. An evaluation of 110 benchmarks from various sources shows that the proposed technique can synthesize 108 benchmarks successfully. On average, the synthesizer can generate document database queries from a small number of input-output examples within tens of seconds.

## 83. Template-Guided Program Repair in the Era of Large Language Models

**Authors:** Kevin Huang, Jian Zhang (Nanyang Technological University), Xiangxin Meng (Beihang University, Beijing, China), Yang Liu (Nanyang Technological University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**PDF:** https://ieeexplore.ieee.org/document/11029846

**中文总结:** 提出 NTR 两阶段神经模板修复框架，先微调 LLM 选择修复模板再引导补丁生成，更好融合传统模板修复与大模型能力。

**Abstract:** Recent advancements in automated program repair (APR) have been significantly driven by the application of Large Language Models (LLMs). In particular, the integration of LLMs with traditional template-based repair methods has demonstrated effective outcomes. Despite this, the synergy between the strengths of traditional methods and LLMs remains underexploited. This oversight originates from the indiscriminate use of templates and their insufficient coverage. Also, using small-scale LLMs within the zero-shot learning context proves to be suboptimal. To alleviate the limitations, we propose NTR (Neural Template Repair), a two-stage repair framework including template selection and patch generation, both of which are under the fine-tuning paradigm. In the template selection phase, we formulate it as a multiclass classification problem and fine-tune million-level LLMs for better selecting possible templates. During the patch generation phase, we leverage the chosen templates as probable directions (e.g., `Mutate Conditional Expression') to guide the fine-tuning process of LLMs at the billion-level scale for precise patch creation. Moreover, we incorporate a unique template to signify the absence of a suitable template and employ a probability-based prioritization of templates, thereby optimizing patch generation. This framework not only effectively addresses template mismatch issues, but also enables the billion-level LLMs to explore the patch space more efficiently, despite the GPU memory constraints. We evaluate NTR with different foundational models on Defects4J V1.2 and HumanEval-Java, the framework consistently demonstrates significant effectiveness. When utilizing StarCoder as the foundational model for patch generation, NTR fixes 128 and 129 bugs in Defects4J and HumanEval, outperforming the best baseline APR tool by 14 and 59 bugs. With the larger CodeLlama model, the fixed bugs rise to 139 and 136, respectively, exceeding the baseline by 25 and 66 bugs. Notably, the performance stems not only from the foundational models but also benefits greatly from our NTR framework. Specifically, NTR's implementation with StarCoder and CodeLlama leads to 22 and 23 additional fixes, which is beyond what the models achieve on their own. This emphasizes the success of our new perspective on utilizing templates to unlock the bug-fixing potential of LLMs.

## 84. Test Intention Guided LLM-based Unit Test Generation

**Authors:** Zifan Nan (Huawei), Zhaoqiang Guo (Software Engineering Application Technology Lab, Huawei, China), Kui Liu (Huawei), Xin Xia (Huawei)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029762

**中文总结:** 提出 IntUT，以显式测试意图（输入、mock 行为、期望结果）引导 LLM 生成单元测试；分支覆盖率提升 94%，行覆盖率提升 49%。

**Abstract:** The emergence of Large Language Models (LLMs) has accelerated the progress of intelligent software engineering technologies, which brings promising possibility for unit test generation. However, existing approaches on unit tests directly generated from Large Language Models (LLMs) often prove impractical due to their low coverage and insufficient mocking capabilities. This paper proposes IntUT, a novel approach that utilizes explicit test intentions (e.g. test inputs, mock behaviors, and expected results) to effectively guide the LLM to generate high-quality test cases. Our experimental results on three industry Java projects and live study demonstrate that prompting LLM with test intention can generate high-quality test cases for developers. Specifically, it achieves the improvements on branch coverage by 94% and line coverage by 49%. Eventually, we obtain developers' feedback on using IntUT to generate cases for 3 newly Java projects with over 80% line coverage and 30% efficiency improvement on writing unit test cases.

## 85. The Fact Selection Problem in LLM-Based Program Repair

**Authors:** Nikhil Parasaram (Uber Amsterdam), Huijie Yan (University College London), Boyu Yang (University College London), Zineb Flahy (University College London), Abriele Qudsi (University College London), Damian Ziaber (University College London), Earl T. Barr (University College London), Sergey Mechtaev (Peking University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029841

**中文总结:** 对 314 个 Python 缺陷开展 1.9 万余次提示实验，揭示七种缺陷相关事实对 LLM 程序修复均有益但事实数量与效果呈非单调关系。

**Abstract:** Recent research has shown that incorporating bug- related facts, such as stack traces and GitHub issues, into prompts enhances the bug-fixing capabilities of large language models (LLMs). Considering the ever-increasing context window of these models, a critical question arises: what and how many facts should be included in prompts to maximise the chance of correctly fixing bugs? To answer this question, we conducted a large-scale study, employing over 19K prompts featuring various combinations of seven diverse facts to rectify 314 bugs from open-source Python projects within the BugsInPy benchmark. Our findings revealed that each fact, ranging from simple syntactic details like code context to semantic information previously unexplored in the context of LLMs such as angelic values, is beneficial. Specifically, each fact aids in fixing some bugs that would remain unresolved or only be fixed with a low success rate without it. Importantly, we discovered that the effectiveness of program repair prompts is non-monotonic over the number of used facts; using too many facts leads to subpar outcomes. These insights led us to define the fact selection problem: determining the optimal set of facts for inclusion in a prompt to maximise LLM’s performance on a given task instance. We found that there is no one-size- fits-all set of facts for bug repair. Therefore, we developed a basic statistical model, named MANIPLE, which selects facts specific to a given bug to include in the prompt. This model significantly surpasses the performance of the best generic fact set. To underscore the significance of the fact selection problem, we benchmarked MANIPLE against the state-of-the-art zero-shot, non- conversational LLM-based bug repair methods. On our testing dataset of 157 bugs, MANIPLE repairs 88 bugs, 17% above the best configuration.

## 86. The Power of Types: Exploring the Impact of Type Checking on Neural Bug Detection in Dynamically Typed Languages

**Authors:** Boqi Chen (McGill University), José Antonio Hernández López (Linköping University), Gunter Mussbacher (McGill University), Daniel Varro (Linköping University / McGill University)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029776

**中文总结:** 研究类型检查对 Python 神经缺陷检测器的影响，指出将类型检查器易发现的缺陷纳入训练与评估会扭曲检测器性能估计。

**Abstract:** [Motivation] Automated bug detection in dynamically typed languages such as Python is essential for maintaining code quality. The lack of mandatory type annotations in such languages can lead to errors that are challenging to identify early with traditional static analysis tools. Recent progress in deep neural networks has led to increased use of neural bug detectors. In statically typed languages, a type checker is integrated into the compiler and thus taken into consideration when the neural bug detector is designed for these languages. [Problem] However, prior studies overlook this aspect during the training and testing of neural bug detectors for dynamically typed languages. When an optional type checker is used, assessing existing neural bug detectors on bugs easily detectable by type checkers may impact their performance estimation. Moreover, including these bugs in the training set of neural bug detectors can shift their detection focus toward the wrong type of bugs. [Contribution] We explore the impact of type checking on various neural bug detectors for variable misuse bugs, a common type targeted by neural bug detectors. Existing synthetic and real-world datasets are type-checked to evaluate the prevalence of type-related bugs. Then, we investigate how type-related bugs influence the training and testing of the neural bug detectors. [Findings] Our findings indicate that existing bug detection datasets contain a significant proportion of type-related bugs. Building on this insight, we discover integrating the neural bug detector with a type checker can be beneficial, especially when the code is annotated with types. Further investigation reveals neural bug detectors perform better on type-related bugs than other bugs. Moreover, removing type-related bugs from the training data helps improve neural bug detectors’ ability to identify bugs beyond the scope of type checkers.

## 87. The Seeds of the FUTURE Sprout from History: Fuzzing for Unveiling Vulnerabilities in Prospective Deep-Learning Libraries

**Authors:** Zhiyuan Li, Jingzheng Wu (Institute of Software, The Chinese Academy of Sciences), Xiang Ling (Institute of Software, Chinese Academy of Sciences), Tianyue Luo (Institute of Software, Chinese Academy of Sciences), ZHIQING RUI (Institute of Software, Chinese Academy of Sciences; University of Chinese Academy of Sciences), Yanjun Wu (Institute of Software, Chinese Academy of Sciences)

**Categories:** AI for Software Engineering, Testing and Quality, Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029791

**中文总结:** 提出 FUTURE 通用深度学习库模糊测试框架，利用已有库历史缺陷信息并微调 LLM 生成针对性 API 序列，面向新兴 DL 库在信息有限时高效发现安全漏洞。

**Abstract:** The widespread application of Large Language Models (LLMs) underscores the importance of Deep Learning (DL) technologies that rely on foundational DL libraries such as PyTorch and TensorFlow. Despite their robust features, these libraries face challenges with scalability and adaptation to rapid advancements in the LLM community. In response, tech giants like Apple and Huawei are developing their own DL libraries to enhance performance, increase scalability, and safeguard intellectual property. Ensuring the security of these libraries is crucial, with fuzzing being a vital solution. However, existing fuzzing frameworks struggle with target flexibility, effectively testing bug-prone API sequences, and leveraging the limited available information in new libraries. To address these limitations, we propose FUTURE, the first universal DL library fuzzing framework tailored for newly introduced and prospective DL libraries. FUTURE leverages historical bug information from existing libraries and fine-tunes LLMs for specialized code generation. This strategy helps identify vulnerabilities in new libraries and uses insights from these libraries to enhance security in existing ones, creating a cycle from history to future and back. To evaluate FUTURE's effectiveness, we conduct comprehensive evaluations on three newly introduced DL libraries. Results demonstrate that FUTURE significantly outperforms existing fuzzers in bug detection, success rate of bug reproduction, validity rate of code generation, and API coverage. Notably, FUTURE has detected 148 bugs across 452 targeted APIs, including 142 previously unknown bugs. Among these, 10 have been assigned CVE IDs. Additionally, FUTURE detects 7 bugs in PyTorch, demonstrating its ability to enhance security in existing libraries in reverse.

## 88. TIGER: A Generating-Then-Ranking Framework for Practical Python Type Inference

**Authors:** Chong Wang (Nanyang Technological University), Jian Zhang (Nanyang Technological University), Yiling Lou (Fudan University), Mingwei Liu (Fudan University), Weisong Sun (Nanyang Technological University), Yang Liu (Nanyang Technological University), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering, Program Analysis and Verification

**PDF:** https://ieeexplore.ieee.org/document/11029957

**中文总结:** 提出 TIGER 生成—排序两阶段 Python 类型推断框架，微调生成与相似度模型；在用户/库自定义类型 Top-5 准确率分别提升 11.2% 与 20.1%。

**Abstract:** Python’s dynamic typing system offers flexibility and expressiveness but can lead to type-related errors, prompting the need for automated type inference despite efforts like Python Enhancement Proposals (PEPs) to enhance type hinting. While existing learning-based approaches show promising inference accuracy, they struggle with practical challenges in comprehensively handling various types, including complex generics and (unseen) user/library-defined types. To address these challenges, we introduce TIGER, employing a two-stage generating-then-ranking (GTR) framework. By fine-tuning pre-trained code models, TIGER trains a generation model with a generative span masking objective and a similarity model with a contrastive training objective. This enables TIGER to execute the GTR inference, generating diverse candidates and then ranking them alongside user/library-defined types. Evaluation on the ManyTypes4Py dataset demonstrates TIGER’s effectiveness across different type categories, particularly excelling in (unseen) user-defined types (with improvements of 11.2% and 20.1% in Top-5 Exact Match). The evaluation results also confirm the robustness and efficiency of TIGER, highlighting the contributions of the employed two stages.

## 89. TOGLL: Correct and Strong Test Oracle Generation with LLMs

**Authors:** Soneya Binta Hossain (University of Virginia), Matthew B Dwyer (University of Virginia)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029748

**中文总结:** 大规模评估 LLM 生成测试预言的能力，微调 7 个代码 LLM 与 6 种提示后提出 TOGLL，可生成正确、多样且更强的测试预言以有效发现独特缺陷。

**Abstract:** Test oracles play a crucial role in software testing, enabling effective bug detection. Despite initial promise, neural methods for automated test oracle generation often result in a large number of false positives and weaker test oracles. While LLMs have shown impressive effectiveness in various software engineering tasks, including code generation, test case creation, and bug fixing, there remains a notable absence of large-scale studies exploring their effectiveness in test oracle generation. The question of whether LLMs can address the challenges in effective oracle generation is both compelling and requires thorough investigation. In this research, we present the first comprehensive study to investigate the capabilities of LLMs in generating correct, diverse, and strong test oracles capable of effectively identifying a large number of unique bugs. To this end, we fine-tuned seven code LLMs using six distinct prompts on a large dataset consisting of 110 Java projects. Utilizing the most effective fine- tuned LLM and prompt pair, we introduce TOGLL, a novel LLM-based method for test oracle generation. To investigate the generalizability of TOGLL, we conduct studies on 25 unseen large-scale Java projects. Besides assessing the correctness, we also assess the diversity and strength of the generated oracles. We compare the results against EvoSuite and the state-of-the-art neural method, TOGA. Our findings reveal that TOGLL can produce 3.8 times more correct assertion oracles and 4.9 times more exception oracles. Regarding bug detection effectiveness, TOGLL can detect 1,023 unique mutants that EvoSuite cannot, which is ten times more than what the previous SOTA neural-based method, TOGA, can detect. Additionally, TOGLL significantly outperforms TOGA in detecting real bugs from the Defects4J dataset.

## 90. Towards Better Answers: Automated Stack Overflow Post Updating

**Authors:** Yubo Mai (Zhejiang University), Zhipeng Gao (Shanghai Institute for Advanced Study - Zhejiang University), Haoye Wang (Hangzhou City University), Tingting Bi (The University of Melbourne), Xing Hu (Zhejiang University), Xin Xia (Huawei), JianLing Sun (Zhejiang University)

**Categories:** AI for Software Engineering

**PDF:** https://ieeexplore.ieee.org/document/11029872

**中文总结:** 提出 Soup，基于 Stack Overflow 评论自动预测有效编辑并更新帖子答案；微调 CodeLlama 完成有效评论—编辑预测与自动更新任务。

**Abstract:** Utilizing code snippets on Stack Overflow (SO) is a common practice among developers for problem-solving. Although SO code snippets serve as valuable resources, it is important to acknowledge their imperfections, reusing problematic code snippets can lead to the introduction of suboptimal or buggy code into software projects. \textit{SO comments} often point out weaknesses of a post and provide valuable insights to improve the quality of answers, while SO comments are usually missed and/or ignored, leaving these problematic code snippets untouched. In this work, we first investigate the task of automatic SO posts updating based on their associated comments. We introduce a novel framework, named \textbf{Soup} (\textbf{\underline{S}}tack \textbf{\underline{O}}verflow \textbf{\underline{U}}pdator for \textbf{\underline{P}}ost) for this task. \textbf{Soup} addresses two key tasks: Valid Comment-Edit Prediction (VCP) and Automatic Post Updating (APU). We fine-tuned a large language model, CodeLlama, using low-rank adaptation techniques to complete the VCP task, and constructed a dataset containing 78k valid comment-edit pairs for the APU task. Subsequently, we tested the performance of multiple large language models on the APU task. Extensive experimental results show the promising performance of our model over a set of benchmarks. Moreover, we also perform an in-the-wild evaluation on Stack Overflow, we submitted 50 edits generated by our approach to Stack Overflow posts and 21 of them have been verified and accepted by SO maintainers, further proving the practical value of \textbf{Soup}.

## 91. Towards Neural Synthesis for SMT-assisted Proof-Oriented Programming

**Authors:** Saikat Chakraborty (Microsoft Research), Gabriel Ebner (Microsoft Research), Siddharth Bhat (University of Cambridge), Sarah Fakhoury (Microsoft Research), Sakina Fatima (University of Ottawa), Shuvendu K. Lahiri (Microsoft Research), Nikhil Swamy (Microsoft Research)

**Categories:** AI for Software Engineering, Security and Vulnerability

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11030292

**中文总结:** 整理约 60 万行 F* 开源证明代码数据集（约 3.2 万类型导向合成任务）并提供可复现片段校验器，探索 AI 合成 SMT 辅助证明导向程序。

**Abstract:** Proof-oriented programs mix computational content with proofs of program correctness. However, the human effort involved in programming and proving is still substantial, despite the use of Satisfiability Modulo Theories (SMT) solvers to automate proofs in languages such as F*. Seeking to spur research on using AI to automate the construction of proof-oriented programs, we curate a dataset of 600K lines of open-source F* programs and proofs, including software used in production systems ranging from Windows and Linux, to Python and Firefox. Our dataset includes around 32K top-level F* definitions, each representing a type-directed program and proof synthesis problem---producing a definition given a formal specification expressed as an F* type. We provide a program-fragment checker that queries F* to check the correctness of candidate solutions. We believe this is the largest corpus of SMT-assisted program proofs coupled with a reproducible program-fragment checker. Grounded in this dataset, we investigate the use of AI to synthesize programs and their proofs in F*, with promising results. Our main finding in that the performance of fine-tuned smaller language models (such as Phi-2 or StarCoder) compare favorably with large language models (such as GPT-4), at a much lower computational cost. We also identify various type-based retrieval augmentation techniques and find that they boost performance significantly. With detailed error analysis and case studies, we identify potential strengths and weaknesses of models and techniques and suggest directions for future improvements.

## 92. Towards Understanding the Characteristics of Code Generation Errors Made by Large Language Models

**Authors:** Zhijie Wang (University of Alberta), Zijie Zhou (University of Illinois Urbana-Champaign), Da Song (University of Alberta), Yuheng Huang (University of Alberta, Canada), Shengmai Chen (Purdue University), Lei Ma (The University of Tokyo & University of Alberta), Tianyi Zhang (Purdue University)

**Categories:** AI for Software Engineering, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029951

**中文总结:** 在 HumanEval 上对六种 LLM 的代码生成错误做系统分析，建立涵盖语义与语法维度的错误分类体系，揭示错误多为跨行、多位置且与任务复杂度相关。

**Abstract:** Large Language Models (LLMs) have demonstrated unprecedented capabilities in code generation. However, there remains a limited understanding of code generation errors that LLMs can produce. To bridge the gap, we conducted an in-depth analysis of code generation errors across six representative LLMs on the HumanEval dataset. Specifically, we first employed open coding and thematic analysis to distill a comprehensive taxonomy of code generation errors. We analyzed two dimensions of error characteristics---semantic characteristics and syntactic characteristics. Our analysis revealed that LLMs often made non-trivial, multi-line code generation errors in various locations and with various root causes. We further analyzed the correlation between these errors and task complexity as well as test pass rate. Our findings highlight several challenges in locating and fixing code generation errors made by LLMs. In the end, we discussed several future directions to address these challenges.

## 93. Treefix: Enabling Execution with a Tree of Prefixes

**Authors:** Beatriz Souza (Universität Stuttgart), Michael Pradel (University of Stuttgart)

**Categories:** AI for Software Engineering, Testing and Quality

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029828

**中文总结:** 提出 Treefix，利用 LLM 迭代生成前缀树以启用不完整代码片段的执行，通过执行反馈逐步扩展可执行行数，优于 LExecutor 等学习引导执行方法。

**Abstract:** The ability to execute code is a prerequisite for various dynamic program analyses. Learning-guided execution has been proposed as an approach to enable the execution of arbitrary code snippets by letting a neural model predict likely values for any missing variables. Although state-of-the-art learning-guided execution approaches, such as LExecutor, can enable the execution of a relative high amount of code, they are limited to predicting a restricted set of possible values and do not use any feedback from previous executions to execute even more code. This paper presents Treefix, a novel learning-guided execution approach that leverages LLMs to iteratively create code prefixes that enable the execution of a given code snippet. The approach addresses the problem in a multi-step fashion, where each step uses feedback about the code snippet and its execution to instruct an LLM to improve a previously generated prefix. This process iteratively creates a tree of prefixes, a subset of which is returned to the user as prefixes that maximize the number of executed lines in the code snippet. In our experiments with two datasets of Python code snippets, Treefix achieves 25% and 7% more coverage relative to the current state of the art in learning- guided execution, covering a total of 84% and 82% of all lines in the code snippets.

## 94. Trust Dynamics in AI-Assisted Development: Definitions, Factors, and Implications

**Authors:** Sadra Sabouri (University of Southern California), Philipp Eibl (University of Southern California), Xinyi Zhou (University of Southern California), Morteza Ziyadi (Amazon AGI), Nenad Medvidović (University of Southern California), Lars Lindemann (University of Southern California), Souti Chattopadhyay (University of Southern California)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029928

**中文总结:** 混合方法研究开发者对 AI 代码建议的信任：可理解性与感知正确性是主要判据，但定义与评估存在落差，开发者最终仅保留约 52% 的原始建议。

**Abstract:** Software developers increasingly rely on AI code generation utilities. To ensure that "good" code is accepted into the code base and "bad" code is rejected, developers must know when to trust an AI suggestion. Understanding how developers build this intuition is crucial to enhancing developer-AI collaborative programming. In this paper, we seek to understand how developers (1) define and (2) evaluate the trustworthiness of a code suggestion and (3) how trust evolves when using AI code assistants. To answer these questions, we conducted a mixed-method study consisting of an in-depth exploratory survey with (n=29) developers followed by an observation study (n=10). We found that comprehensibility and perceived correctness were the most frequently used factors to evaluate code suggestion trustworthiness. However, the gap in developers' definition and evaluation of trust points to a lack of support for evaluating trustworthy code in real-time. We also found that developers often alter their trust decisions, keeping only 52% of original suggestions. Based on these findings, we extracted four guidelines to enhance developer-AI interactions. We validated the guidelines through a survey with (n=7) domain experts and survey members (n=8). We discuss the validated guidelines, how to apply them, and tools to help adopt them.

## 95. Unleashing the True Potential of Semantic-based Log Parsing with Pre-trained Language Models

**Authors:** Van-Hoang Le (The University of Newcastle), Yi Xiao, Hongyu Zhang (Chongqing University)

**Categories:** AI for Software Engineering, Evolution and Maintenance

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029829

**中文总结:** 提出 UNLEASH 语义日志解析方法，通过三项增强策略提升小型 PLM 性能，证明经优化的 RoBERTa 等模型可在更低成本下达到或超越 LLM 基线解析效果。

**Abstract:** Software-intensive systems often produce console logs for troubleshooting purpose. Log parsing, which aims at parsing a log message into a specific log template, typically serves as the first step toward automated log analytics. To better comprehend semantic information of log messages, many semantic-based log parsers have been proposed. These log parsers fine-tune a small pretrained language model (PLM) such as RoBERTa on a few labelled log samples. With the increasing popularity of large language models (LLMs), some recent studies also propose to leverage LLMs such as ChatGPT through in-context learning for automated log parsing, and obtain better results than previous semantic-based log parsers with small PLMs. In this paper, we show that semantic-based log parsers with small PLMs can actually achieve better or comparable performance to state-of-the-art LLM-based log parsing models while being more efficient and cost-effective. We propose UNLEASH, a novel semantic-based log parsing approach, which incorporates three enhancement methods to boost the performance of PLMs for log parsing, including (1) an entropy-based ranking method to select the most informative log samples; (2) a contrastive learning method to enhance the fine-tuning process; and (3) an inference optimization method to improve the log parsing performance. We evaluate UNLEASH on a set of large log datasets and the experimental results show that UNLEASH is effective and efficient, when compared to state-of-the-art log parsers.

## 96. Unseen Horizons: Unveiling the Real Capability of LLM Code Generation Beyond the Familiar

**Authors:** Yuanliang Zhang (National University of Defense Technology), Yifan Xie, Shanshan Li (National University of Defense Technology), Ke Liu, Chong Wang (National University of Defense Technology), Zhouyang Jia (National University of Defense Technology), Xiangbing Huang (National University of Defense Technology), Jie Song (National University of Defense Technology), Chaopeng Luo (National University of Defense Technology), Zhizheng Zheng (National University of Defense Technology), Rulin Xu (National University of Defense Technology), Yitong Liu (National University of Defense Technology), Si Zheng (National University of Defense Technology), Liao Xiangke (National University of Defense Technology)

**Categories:** AI for Software Engineering

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029836

**中文总结:** 提出 Unseen Horizons 评估框架，借鉴代码混淆在 token、AST、语义等多层次变换代码，用 LLM 未见过的代码更客观评估其代码生成真实能力，缓解训练数据泄露与时效性问题。

**Abstract:** Recently, large language models (LLMs) have shown strong potential in code generation tasks. However, there are still gaps before they can be fully applied in actual software development processes. Accurately assessing the code generation capabilities of large language models has become an important basis for evaluating and improving the models. Some existing works have constructed datasets to evaluate the capabilities of these models. However, there are three main gaps to objectively evaluate the real capability of LLMs: the exposure of target code, case timeliness, and dependency availability. The fundamental reason for these gaps is that the code in current datasets may have been exposed during the training phase of LLM, and due to the continuous training and development of LLM, their timeliness has been severely compromised. The key to solve the problem is to, as much as possible, evaluate the LLMs using code that they have not encountered before. Thus, the fundamental idea using in this paper is to draw on the concept of code obfuscation, changing code at different levels while ensuring the functionality and output. To this end, we build a code-obfuscation based benchmark OBFUSEVAL. We first collect 1,354 raw cases from five real-world projects, including function description and code. Then we use three-level strategy (symbol, structure and semantic) to obfuscate descriptions, code and context dependencies. We evaluate four LLMs on OBFUSEVAL and compared the effectiveness of different obfuscation strategy. We use official test suites of these projects to evaluate the generated code. The results show that after obfuscation, the average decrease ratio of test pass rate can up to 62.5\%.

## 97. Vulnerability Detection with Code Language Models: How Far Are We?

**Authors:** Yangruibo Ding (Columbia University), Yanjun Fu (University of Maryland), Omniyyah Ibrahim (King Abdulaziz City for Science and Technology), Chawin Sitawarin (University of California, Berkeley), Xinyun Chen, Basel Alomair (King Abdulaziz City for Science and Technology), David Wagner (UC Berkeley), Baishakhi Ray (Columbia University), Yizheng Chen (University of Maryland)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029911

**中文总结:** 揭示现有漏洞数据集质量差、标签不准、重复率高导致 code LM 漏洞检测评估不可靠；提出 PrimeVul 数据集，采用更严格标注、去重、时间切分与更贴近真实的评估设置。

**Abstract:** In the context of the rising interest in code language models (code LMs) and vulnerability detection, we study the effectiveness of code LMs for detecting vulnerabilities. Our analysis reveals significant shortcomings in existing vulnerability datasets, including poor data quality, low label accuracy, and high duplication rates, leading to unreliable model performance in realistic vulnerability detection scenarios. Additionally, the evaluation methods used with these datasets are not representative of real-world vulnerability detection. To address these challenges, we introduce PrimeVul, a new dataset for training and evaluating code LMs for vulnerability detection. PrimeVul incorporates a novel set of data labeling techniques that achieve comparable label accuracy to human-verified benchmarks while significantly expanding the dataset. It also implements a rigorous data de-duplication and chronological data splitting strategy to mitigate data leakage issues, alongside introducing more realistic evaluation metrics and settings. This comprehensive approach aims to provide a more accurate assessment of code LMs' performance in real-world conditions. Evaluating code LMs on PrimeVul reveals that existing benchmarks significantly overestimate the performance of these models. For instance, a state-of-the-art 7B model scored 68.26\% F1 on BigVul but only 3.09\% F1 on PrimeVul. Attempts to improve performance through advanced training techniques and larger models like GPT-3.5 and GPT-4 were unsuccessful, with results akin to random guessing in the most stringent settings. These findings underscore the considerable gap between current capabilities and the practical requirements for deploying code LMs in security roles, highlighting the need for more innovative research in this domain.

## 98. Weakly-supervised Log-based Anomaly Detection with Inexact Labels via Multi-instance Learning

**Authors:** Minghua He (Peking University), Tong Jia (Institute for Artificial Intelligence, Peking University, Beijing, China), Chiming Duan (Peking University), Huaqian Cai (Peking University), Ying Li (School of Software and Microelectronics, Peking University, Beijing, China), Gang Huang (Peking University)

**Categories:** AI for Software Engineering, Security and Vulnerability

**PDF:** https://ieeexplore.ieee.org/document/11029770

**中文总结:** 提出不精确标注策略与 MIDLog 弱监督日志异常检测方法，用多示例学习从时间段级粗标签推断条目级异常；在三个公开数据集上 F1 超过 85%。

**Abstract:** Log-based anomaly detection is essential for maintaining software availability. However, existing log-based anomaly detection approaches heavily rely on fine-grained exact labels of log entries which are very hard to obtain in real-world systems. This brings a key problem that anomaly detection models require supervision signals while labeled log entries are unavailable. Facing this problem, we propose a new labeling strategy called inexact labeling that instead of labeling an log entry, system experts can label a bag of log entries in a time span. Furthermore, we propose MIDLog, a weakly supervised log-based anomaly detection approach with inexact labels. We leverage the multi-instance learning paradigm to achieve explicit separation of anomalous log entries from the inexact labeled anomalous log set so as to deduce exact anomalous log labels from inexact labeled log sets. Extensive evaluation on three public datasets shows that our approach achieves an F1 score of over 85\% with inexact labels.

## 99. What Guides Our Choices? Modeling Developers' Trust and Behavioral Intentions Towards GenAI

**Authors:** Rudrajit Choudhuri (Oregon State University), Bianca Trinkenreich (Colorado State University), Rahul Pandita (GitHub, Inc.), Eirini Kalliamvakou (GitHub), Igor Steinmacher (NAU RESHAPE LAB), Marco Gerosa (Northern Arizona University), Christopher Sanchez (Oregon State University), Anita Sarma (Oregon State University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029764

**中文总结:** 构建开发者对 GenAI 工具信任与使用意愿的理论模型，调查 238 名软件开发者，分析信任影响因素及认知风格与采纳意图之间的关系，为 GenAI 工具集成提供依据。

**Abstract:** Generative AI (genAI) tools, such as ChatGPT or Copilot, are advertised to improve developer productivity and are being integrated into software development. However, misaligned trust, skepticism, and usability concerns can impede the adoption of such tools. Research also indicates that AI can be exclusionary, failing to support diverse users adequately. One such aspect of diversity is cognitive diversity—variations in users’ cognitive styles—that leads to divergence in perspectives and interaction styles. When an individual’s cognitive style is unsupported, it creates barriers to technology adoption. Therefore, to understand how to effectively integrate genAI tools into software development, it is first important to model what factors affect developers’ trust and intentions to adopt genAI tools in practice? We developed a theoretical model to (1) identify factors that influence developers’ trust in genAI tools and (2) examine the relationship between developers’ trust, cognitive styles, and their intentions to use these tools. We surveyed software developers (N=238) at two major global tech organizations and employed Partial Least Squares-Structural Equation Modeling (PLS-SEM) to evaluate our model. Our findings reveal that genAI’s system/output quality, functional value, and goal maintenance significantly influence developers’ trust in these tools. Furthermore, developers’ trust and cognitive styles influence their intentions to use these tools. We offer practical suggestions for designing genAI tools for effective use and inclusive user experience.

## 100. What Guides Our Choices? Modeling Developers' Trust and Behavioral Intentions Towards GenAI

**Authors:** Rudrajit Choudhuri (Oregon State University), Bianca Trinkenreich (Colorado State University), Rahul Pandita (GitHub, Inc.), Eirini Kalliamvakou (GitHub), Igor Steinmacher (NAU RESHAPE LAB), Marco Gerosa (Northern Arizona University), Christopher Sanchez (Oregon State University), Anita Sarma (Oregon State University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029764

**中文总结:** 构建开发者对 GenAI 工具信任与使用意愿的理论模型，调查 238 名软件开发者，分析信任影响因素及认知风格与采纳意图之间的关系，为 GenAI 工具集成提供依据。

**Abstract:** Generative AI (genAI) tools, such as ChatGPT or Copilot, are advertised to improve developer productivity and are being integrated into software development. However, misaligned trust, skepticism, and usability concerns can impede the adoption of such tools. Research also indicates that AI can be exclusionary, failing to support diverse users adequately. One such aspect of diversity is cognitive diversity—variations in users’ cognitive styles—that leads to divergence in perspectives and interaction styles. When an individual’s cognitive style is unsupported, it creates barriers to technology adoption. Therefore, to understand how to effectively integrate genAI tools into software development, it is first important to model what factors affect developers’ trust and intentions to adopt genAI tools in practice? We developed a theoretical model to (1) identify factors that influence developers’ trust in genAI tools and (2) examine the relationship between developers’ trust, cognitive styles, and their intentions to use these tools. We surveyed software developers (N=238) at two major global tech organizations and employed Partial Least Squares-Structural Equation Modeling (PLS-SEM) to evaluate our model. Our findings reveal that genAI’s system/output quality, functional value, and goal maintenance significantly influence developers’ trust in these tools. Furthermore, developers’ trust and cognitive styles influence their intentions to use these tools. We offer practical suggestions for designing genAI tools for effective use and inclusive user experience.

## 101. What You See Is What You Get: Attention-based Self-guided Automatic Unit Test Generation

**Authors:** Xin Yin (Zhejiang University), Chao Ni (Zhejiang University), xiaodanxu (College of Computer Science and Technology, Zhejiang university), Xiaohu Yang (Zhejiang University)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029864

**中文总结:** 提出 AUGER 两阶段方法：先用注意力机制预测缺陷倾向，再自引导生成单元测试触发错误，兼顾缺陷检测置信度与测试生成效率。

**Abstract:** Software defects heavily affect software's functionalities and may cause huge losses. Recently, many AI-based approaches have been proposed to detect defects, which can be divided into two categories: software defect prediction and automatic unit test generation. While these approaches have made great progress in software defect detection, they still have several limitations in practical application, including the low confidence of prediction models and the inefficiency of unit testing models. To address these limitations, we propose a WYSIWYG (i.e., What You See Is What You Get) approach: \textbf{A}ttention-based Self-guided Automatic \textbf{U}nit Test \textbf{G}en\textbf{ER}ation (AUGER), which contains two stages: defect detection and error triggering. In the former stage, \toolname first detects the proneness of defects. Then, in the latter stage, it guides to generate unit tests for triggering such an error with the help of critical information obtained by the former stage. To evaluate the effectiveness of \toolname, we conduct a large-scale experiment by comparing with the state-of-the-art (SOTA) approaches on the widely used datasets (i.e., Bears, Bugs.jar, and Defects4J). AUGER makes great improvements by 4.7\% to 35.3\% and 17.7\% to 40.4\% in terms of F1-score and Precision in defect detection, and can trigger 23 to 84 more errors than SOTAs in unit test generation. Besides, we also conduct a further study to verify the generalization in practical usage by collecting a new dataset from real-world projects.

## 102. Your Fix Is My Exploit: Enabling Comprehensive DL Library API Fuzzing with Large Language Models

**Authors:** Kunpeng Zhang (The Hong Kong University of Science and Technology), Shuai Wang (Hong Kong University of Science and Technology), Jitao Han (Central University of Finance and Economics), Xiaogang Zhu (The University of Adelaide), Xian Li (Swinburne University of Technology), Shaohua Wang (Central University of Finance and Economics), Sheng Wen (Swinburne University of Technology)

**Categories:** AI for Software Engineering, Testing and Quality

**PDF:** https://ieeexplore.ieee.org/document/11029835

**中文总结:** 提出基于 LLM 的深度学习库 API 全面模糊测试方法，应对 TensorFlow、PyTorch 等上千 API 与复杂输入/用法模式的测试难题。

**Abstract:** Deep learning (DL) libraries are widely used to form the basis of various AI applications in computer vision, natural language processing, and software engineering domains. Despite their popularity, DL libraries are known to have vulnerabilities, such as buffer overflows, use-after-free, and integer overflows, that can be exploited to compromise the security or effectiveness of the underlying libraries. While traditional fuzzing techniques have been used to find bugs in software, they are not well-suited for DL libraries. In general, the complexity of DL libraries and the diversity of their APIs make it challenging to test them thoroughly. To date, mainstream DL libraries like TensorFlow and PyTorch have featured over 1,000 APIs, and the number of APIs is still growing. Fuzzing all these APIs is a daunting task, especially when considering the complexity of the input data and the diversity of the API usage patterns. Recent advances in large language models (LLMs) have illustrated the high potential of LLMs in understanding and synthesizing human-like code. Despite their high potential, we find that emerging LLM-based fuzzers are less optimal for DL library API fuzzing, given their lack of in-depth knowledge on API input edge cases and inefficiency in generating test inputs. In this paper, we propose DFUZZ, a LLM-driven DL library fuzzing approach. We have two key insights: (1) With high reasoning ability, LLMs can replace human experts to reason edge cases (likely error-triggering inputs) from checks in an API's code, and transfer the extracted knowledge to test other (new or rarely-tested) APIs. (2) With high generation ability, LLMs can synthesize initial test programs with high accuracy that automates API testing. DFUZZ provides LLMs with a novel ''white-box view'' of DL library APIs, and therefore, can leverage LLMs' reasoning and generation abilities to achieve comprehensive fuzzing. Our experimental results on popular DL libraries demonstrate that DFUZZ is able to cover more APIs than SOTA (LLM-based) fuzzers on TensorFlow and PyTorch, respectively. Moreover, DFUZZ successfully detected 37 bugs, with 17 already confirmed as previously unknown bugs.
