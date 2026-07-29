# ICSE 2026 Research Track — Awarded Papers

Source: https://conf.researchr.org/track/icse-2026/icse-2026-research-track?#event-overview

Total: 24 papers

## Award breakdown

| Award | # Papers |
| --- | ---: |
| Distinguished Paper Award | 22 |
| Artifact Award Winner | 2 |

*Note: a paper may receive more than one award.*

## Papers

## 1. An Eye for AI: Eye-Tracking the Micro-Interruptions of GenAI Code Suggestions

**Authors:** Tarek Alakmeh (University of Zurich), Sarah D'Angelo (Google), Thomas Fritz (University of Zurich)

**Categories:** AI for Software Engineering

**Awards:** Artifact Award Winner

**中文总结:** 首例眼动研究 GenAI 代码建议对开发者认知的影响，约半数建议未被查看、已查看中 75% 未采用，每条建议引入约 0.9 秒微中断；呼吁更上下文感知的低干扰建议设计。

**Abstract:** Generative AI code suggestion tools, such as GitHub Copilot, are increasingly integrated into developer workflows. While these tools promise productivity gains, the actual impact on developer cognition and task performance has been mixed. In this paper, we present the first in-depth eye-tracking study of how developers interact with generative AI code suggestions during programming. We recruited 35 professionals and student developers and recorded their gaze behavior, code suggestion interactions, and code editing activity during programming sessions. By combining high-resolution eye-tracking data with fine-grained logging of AI-generated suggestions, we quantify the cognitive costs of reviewing code suggestions. Our findings show that approximately half of the generated suggestions are not even looked at. From the suggestions that were looked at, over 75% are not used. Although suggestions are only reviewed briefly (~0.9 seconds on average), each suggestion introduces a micro-interruption that disrupts developer flow. We discuss opportunities for more efficient and context-aware generative AI code suggestions that minimize cognitive overhead.

## 2. TypeCare: Boosting Python Type Inference Models via Context-Aware Re-Ranking and Augmentation

**Authors:** Wonseok Oh (Korea University), Hakjoo Oh (Korea University)

**Categories:** Software Engineering for AI

**Awards:** Artifact Award Winner

**中文总结:** 提出 TypeCare 后处理框架，通过上下文重排序与候选增强提升现有 Python 类型推断模型，对复杂类型 top-1 准确率最高提升 40.1%。

**Abstract:** Type annotations improve Python code quality by enabling better readability, static analysis, and developer productivity. However, manually annotating existing code is labor-intensive and error-prone. While recent learning-based models have advanced automatic type inference, they struggle with rare or complex types that are underrepresented in training data. We present TypeCare, a model-agnostic post-processing technique that refines the outputs of existing type inference models using code context, without requiring retraining or fine-tuning. TypeCare combines two key components: (1) Re-Ranking, which prioritizes semantically and syntactically relevant types, and (2) Augmentation, which generates additional contextually plausible candidates. Applied to three state-of-the-art type inference models—TypeT5, Tiger, and TypeGen—TypeCare consistently improves top-1 accuracy, achieving up to 40.1% gains on complex types that existing models often fail to predict correctly.

## 3. "Making Our Life Less Monotonous" or "Just Tick Things Off": An Exploratory Multi-Method Study of Toil

**Authors:** Tom Kafoe (Independent Researcher), Lina Ochoa (Eindhoven University of Technology), Sharath Siravuru (ING), Alexander Serebrenik (Eindhoven University of Technology)

**Categories:** Human and Social Aspects

**Awards:** Distinguished Paper Award

**中文总结:** 通过灰文献与公司访谈探索 SRE 中 toil（重复手工运维）的定义与影响，发现业界虽认同减 toil 有益，但在成本、复杂度与岗位影响上存在消除阻力。

**Abstract:** Google introduced Site Reliability Engineering (SRE) as a DevOps approach focused on service reliability. A key concept in SRE is toil defined as manual, repetitive, automatable, and reactive tasks that arise in production service management, scale with service growth, and provide no lasting value. As SRE adoption expands beyond Google, organisations adapt SRE practices and terminology, leading to inconsistencies in how toil is defined and perceived. Understanding toil is crucial, as it is assumed to directly impact both operational efficiency and well-being of engineers, ultimately influencing the reliability and scalability of production services. In this study, we examine toil in light of Google’s claim that “less toil is better". We explore how different developers define toil, its perceived impact, and whether reducing toil is seen as beneficial. To this end, we analyse grey literature, for a broad, practical perspective of toil and its effects, and conduct semi-structured interviews at the Company to triangulate the previous findings. We observe that while Google’s toil definition has been widely adopted, it has been expanded to include additional technical attributes (e.g., routine, time-consuming, persistent) and human aspects (e.g., mundane, not just unwanted work). Practitioners generally view toil negatively, citing its impact on organisations’ growth, teams’ efficiency, and morale. However, while toil elimination is generally praised, we also observe resistance stemming from concerns over cost, complexity, and the possible negative impact this elimination can have on employees predominantly working on toil.

## 4. "Maybe We Need Some More Examples:" Individual and Team Drivers of Developer GenAI Tool Use

**Authors:** Courtney Miller (Carnegie Mellon University), Rudrajit Choudhuri (Oregon State University), Mara Ulloa (Northwestern University), Sankeerti Haniyur (Microsoft Corporation), Robert DeLine (Microsoft Research), Margaret-Anne Storey (University of Victoria), Emerson Murphy-Hill (Microsoft), Christian Bird (Microsoft Research), Jenna L. Butler (Microsoft Research)

**Categories:** Human and Social Aspects

**Awards:** Distinguished Paper Award

**中文总结:** 对 27 团队 54 名开发者配对访谈，发现 GenAI 工具使用差异主要来自工具认知（协作者 vs 功能）、参与方式与遇挫策略，并揭示“生产力压力悖论”。

**Abstract:** Despite the widespread availability of generative AI tools in software engineering, developer adoption remains uneven. This unevenness is problematic because it hampers productivity efforts, frustrates management’s expectations, and creates uncertainty around the future roles of developers. Through paired interviews with 54 developers across 27 teams – one frequent and one infrequent user per team – we demonstrate that differences in usage result primarily from how developers perceive the tool (as a collaborator vs. feature), their engagement approach (experimental vs. conservative), and how they respond when encountering challenges (with adaptive persistence vs. quick abandonment). Our findings imply that widespread organizational expectations for rapid productivity gains without sufficient investment in learning support creates a “Productivity Pressure Paradox” undermining the very productivity benefits that motivate adoption.

## 5. A Comprehensive Study of Deep Learning Model Fixing Approaches

**Authors:** Hanmo You (Tianjin University), Zan Wang (Tianjin University), Zishuo Dong (College of Intelligence and Computing, Tianjin University), Luanqi Mo (College of Intelligence and Computing, Tianjin University), Jianjun Zhao (Kyushu University), Junjie Chen (Tianjin University)

**Categories:** Software Engineering for AI

**Awards:** Distinguished Paper Award

**中文总结:** 对 16 种深度学习模型修复方法开展大规模实证，覆盖模型/层/神经元级修复及其对鲁棒性、公平性与向后兼容性的影响；发现模型级修复最有效，但尚无方法能同时最优修复并保持所有其他性质。

**Abstract:** Deep Learning (DL) has been widely adopted in diverse industrial domains, including autonomous driving, intelligent healthcare, and aided programming. Like traditional software, DL systems are also prone to faults, whose malfunctioning may expose users to significant risks. Consequently, numerous approaches have been proposed to address these issues. In this paper, we conduct a large-scale empirical study on 16 state-of-the-art DL model fixing approaches, spanning model-level, layer-level, and neuron-level categories, to comprehensively evaluate their performance. We assess not only their fixing effectiveness (their primary purpose) but also their impact on other critical properties, such as robustness, fairness, and backward compatibility. To ensure comprehensive and fair evaluation, we employ a diverse set of datasets, model architectures, and application domains within a uniform experimental setup for experimentation. We summarize several key findings with implications for both industry and academia. For example, model-level approaches demonstrate superior fixing effectiveness compared to others. No single approach can achieve the best fixing performance while improving accuracy and maintaining all other properties. Thus, academia should prioritize research on mitigating these side effects. These insights highlight promising directions for future exploration in this field.

## 6. Accelerating IC3 Verification by Exploiting Unsatisfiable Cores and Satisfying Models

**Authors:** Xinyi Gong (National University of Defense Technology), Liangze Yin (National University of Defense Technology), Yuhan Li (National University of Defense Technology), Ke Kang (National University of Defense Technology), Wei Dong (National University of Defense Technology), Shanshan Li (National University of Defense Technology), Ji Wang (National University of Defense Technology)

**Categories:** Dependability and Security

**Awards:** Distinguished Paper Award

**中文总结:** 提出通过复用不可满足核与满足模型加速 IC3 验证，构建 UCL/SML 库预判定新约束可满足性；在 Kind2 基准上可将求解器调用减少一个数量级并实现 4.35 倍加速且内存更低。

**Abstract:** The IC3 algorithm represents a groundbreaking advancement in the field of model checking. However, its heavy reliance on numerous and frequent constraint-solving calls poses significant challenges when verifying complex programs. We observe that many of the constraints solved within IC3 share remarkable similarities. Based on this observation, we propose an IC3 acceleration verification method by reusing unsatisfiable cores and satisfying models of previous constraints. This method constructs an Unsatisfiable Core Library (UCL) and a Satisfying Model Library (SML) to store and index crucial unsatisfiable cores and satisfying models generated during the verification process. When a new constraint-solving request is received, our method preemptively determines the satisfiability of the constraint using the existing unsatisfiable cores and satisfying models. This approach can significantly reduce the number of required solver calls, thereby enhancing the verification efficiency. We have implemented our method on Kind2 and evaluated it on the standard benchmark suite of Kind2. Experimental evaluation demonstrates that, for those complex examples, our method can reduce the number of solver calls by an order of magnitude, and achieves a 4.35-fold speedup with even less memory consumption.

## 7. Accurate Inference of Termination Conditions

**Authors:** Biting Huang (Tsinghua University), Zhilei Han (Tsinghua University), Fei He (Tsinghua University)

**Categories:** Dependability and Security

**Awards:** Distinguished Paper Award

**中文总结:** 提出首个精确推断程序终止条件的方法，迭代剔除非终止状态并用数据驱动证明器验证，配合循环集泛化加速收敛；显著优于 Acabar 并生成更准确的终止条件。

**Abstract:** We present the first approach to infer accurate termination conditions of programs. It builds on a simple but effective framework where non-terminating states are iteratively identified and removed, and a termination prover is employed to validate the current condition. We instantiate the framework with data-driven provers and design a multi-way data sharing mechanism to enhance their interaction. Our proofs show that this method is correct, accurate, terminating, and relatively complete. Additionally, we introduce generalization techniques for recurrent sets to accelerate the iteration process. Evaluation on a benchmark of programs from the literature shows that our implementation significantly outperforms the state-of-the-art tool Acabar, producing much more accurate termination conditions, with the proposed techniques playing a crucial role in speeding up the convergence of the process.

## 8. An Empirical Study on Static Application Security Testing (SAST) Tools for Python

**Authors:** Liu Zhuohang (Nankai University), Zhi Wang (Nankai University), Haotong Liu (Nankai University), Wanpeng Li (University of Liverpool)

**Categories:** Testing and Analysis

**Awards:** Distinguished Paper Award

**中文总结:** 评估 8 款 Python SAST 工具在合成与真实漏洞数据集上的表现；单工具在真实集最多检出 40%，全部工具聚合仅 66.7%，并给出根因分析与改进建议。

**Abstract:** Python is currently the most popular programming language and ensuring the security of Python applications has become a critical concern. Static Application Security Testing (SAST) tools have been introduced to address this need, claiming to support a wide range of Common Weakness Enumerations (CWEs). However, the ability of these tools to detect real-world vulnerabilities in Python programs has not been comprehensively evaluated. In this paper, we selected eight SAST tools from 117 existing ones based on well-designed criteria. Based on the synthetic and real-world dataset, we evaluated and compared these SAST tools from different perspectives including effectiveness and efficiency. Our results reveal significant limitations in current SAST tools: although perform well on the synthetic dataset, a single tool detects no more than 40% of the vulnerabilities in our real-world dataset. Even when aggregating the outputs of all evaluated tools, only 66.7% of the real-world vulnerabilities are identified. To further understand these shortcomings, we performed a root cause analysis of the detection results and identified useful insights for both SAST tool developers and users, focusing on tool development, evaluation, and selection.

## 9. Automating Just-In-Time Python Type Annotation Updating

**Authors:** Zhipeng Xue (Zhejiang University), Zhipeng Gao (Shanghai Institute for Advanced Study - Zhejiang University), Xing Hu (Zhejiang University), Jingyuan Chen (Zhejiang University), Xin Xia (Zhejiang University), Shanping Li (Zhejiang University)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出 TypeUp 实现 Python Just-In-Time 类型注解更新，结合 LLM 推理与相似变更学习；较 TypeGen 提升 41.9%，野外评估 25 条更新中 20 条已获开发者确认。

**Abstract:** Type annotations are more and more popular in Python projects to avoid type errors caused by Python’s dynamic typing feature. However, when developers change source code, these type annotations are often neglected or overlooked, resulting in outdated and inconsistent type annotations. Such obsolete type annotations can hinder program comprehension, mislead developers, and even introduce bugs in the future. Therefore, it is necessary to avoid and correct these inconsistent type annotations from the very beginning. In this work, we argue that obsolete type annotations can be reduced and even avoided by automatically updating type annotations alongside code changes. We refer to this task as “Just-In-Time (JIT) type annotation updating”. To solve this task, we propose a novel LLM-based approach named TypeUp (Type Annotation Updator) to automate this task. TypeUp can automatically generate new type annotations based on the old type annotations and corresponding code changes. Specifically, TypeUp guides LLM to perform type annotation updates by eliciting its knowledge and logical reasoning power and learning from similar code changes. The evaluation results show that TypeUp outperforms state-of-the-art type infer approach (i.e., TypeGen) by 41.9% on our task. Moreover, we conducted an in-the-wild evaluation with real-world software projects, 20 out of 25 type annotation updates generated by our approach have already been confirmed by developers, showing our approach’s practical value in real-world environments.

## 10. Can SAT Solvers Keep Up With the Linux Kernel's Feature Model?

**Authors:** Elias Kuiter (University of Magdeburg), Urs-Benedict Braun (University of Magdeburg), Thomas Thüm (TU Braunschweig), Sebastian Krieter (TU Braunschweig, Germany), Gunter Saake (University of Magdeburg, Germany)

**Categories:** Requirements and Modeling

**Awards:** Distinguished Paper Award

**中文总结:** 实证分析 Linux 内核 feature model 与历史 SAT 求解器性能，发现即便最优求解器仍无法跟上内核增长，性能约每 7 年减半；警示产品线分析将日益困难。

**Abstract:** The Linux kernel is a highly relevant, yet also highly configurable software system. Kernel developers keep track of this configurability in a feature model, which defines the features of Linux and their dependencies. To support kernel developers in various activities, many (semi-)automated product-line analyses have been proposed over the years. Under the hood, these analyses can often be computed with SAT solvers. Yet, the Linux kernel has constantly been growing in complexity for decades, which increasingly hampers its efficient analysis. At the same time, SAT solvers have been improving in performance for decades, which eases analysis. In this paper, we investigate empirically whether SAT solvers can keep up with the Linux kernel’s feature model. To this end, we analyze historic feature models of Linux with historic SAT solvers from several sources. We find that SAT solvers are generally not able to keep up with Linux. Even the optimal SAT solver is slowing down by 10% every year, meaning that its performance halves every seven years. We conclude that the Linux kernel will become increasingly difficult to analyze if its growth is not counteracted.

## 11. Evaluating Generated Commit Messages with Large Language Models

**Authors:** Qunhong Zeng (Beijing Institute of Technology), Yuxia Zhang (Beijing Institute of Technology), Zexiong Ma (Peking University), Bo Jiang (Bytedance Network Technology), Ningyuan Sun (ByteDance), Klaas-Jan Stol (Lero; University College Cork; SINTEF Digital), Xingyu Mou (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 系统评估 LLM 作为提交信息质量评判者；CoT+few-shot 的 LLM 评估接近人工水平，显著优于 BLEU/ROUGE 等传统指标。

**Abstract:** Commit messages are essential in software development as they serve to document and explain code changes. Yet, their quality often falls short in practice, with studies showing significant proportions of empty or inadequate messages. While automated commit message generation has advanced significantly, particularly with Large Language Models (LLMs), the evaluation of generated messages remains challenging. Traditional reference-based automatic metrics like BLEU, ROUGE-L, and METEOR have notable limitations in assessing commit message quality, as they assume a one-to-one mapping between code changes and commit messages, leading researchers to rely on resource-intensive human evaluation. This study investigates the potential of LLMs as automated evaluators for commit message quality. Through systematic experimentation with various prompt strategies and state-of-the-art LLMs, we demonstrate that LLMs combining Chain-of-Thought reasoning with few-shot demonstrations achieve near human-level evaluation proficiency. Our LLM-based evaluator significantly outperforms traditional metrics while maintaining acceptable reproducibility, robustness, and fairness levels despite some inherent variability. This work conducts a comprehensive preliminary study on using LLMs for commit message evaluation, offering a scalable alternative to human assessment while maintaining high-quality evaluation.

## 12. HoarePrompt: Structural Reasoning About Program Correctness in Natural Language

**Authors:** Dimitrios Stamatios Bouras (Peking University), Yihan Dai (Peking University), Tairan Wang (University College London), Yingfei Xiong (Peking University), Sergey Mechtaev (Peking University)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出 HoarePrompt，将最强后置条件与 k-induction 思想用于 LLM 逐步推断程序状态并检验自然语言需求，在 CoCoClaNeL 上 MCC 比 Zero-shot-CoT 提升 61%。

**Abstract:** While software requirements are often expressed in natural language, verifying the correctness of a program against such requirements is a hard and underexplored problem. Large language models (LLMs) are promising candidates for addressing this challenge, however our experience shows that they are ineffective in this task, often failing to detect even straightforward bugs. To address this gap, we introduce HoarePrompt, a novel approach that adapts fundamental ideas from program verification to natural language artifacts. Inspired from the strongest postcondition calculus, HoarePrompt employs a systematic, step-by-step process in which an LLM generates natural language descriptions of reachable program states at various code points. To manage loops, we propose few-shot-driven k-induction, an adaptation of the k-induction method widely used in model checking. Once program states are described, HoarePrompt leverages the LLM to assess whether the program, annotated with these state descriptions, conforms to the natural language requirements. For evaluating the quality of classifiers of program correctness with respect to natural language requirements, we constructed CoCoClaNeL, a challenging dataset of solutions to programming competition problems. Our experiments show that HoarePrompt improves the MCC by 61% compared to directly using Zero-shot-CoT prompts for correctness classification. Furthermore, HoarePrompt outperforms a classifier that assesses correctness via LLM-based test generation by an MCC increase of 106%. The inductive reasoning mechanism contributes a 26% boost to MCC, underscoring its effectiveness in managing loops.

## 13. PreServe: Intelligent Management for LMaaS Systems via Hierarchical Prediction

**Authors:** Zhihan Jiang (The Chinese University of Hong Kong), Yujie Huang (The Chinese University of Hong Kong), Guangba Yu (The Chinese University of Hong Kong), Junjie Huang (The Chinese University of Hong Kong), Jiazhen Gu (Chinese University of Hong Kong), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Software Engineering for AI

**Awards:** Distinguished Paper Award

**中文总结:** 提出 LMaaS 管理框架 PreServe，通过服务负载与请求负载的分层预测构建负载 anticipator，优化资源分配与路由。真实生产数据评估显示尾延迟降低 41.3% 以上、资源消耗平均减少 49.38%。

**Abstract:** Large Language Models (LLMs) have revolutionized fields such as natural language processing and software engineering, fueling the growth of Language-Model-as-a-Service (LMaaS) platforms hosted by industry leaders like OpenAI. These platforms handle millions of queries daily, requiring efficient management to reduce serving latency and meet Service Level Objectives (SLOs) while optimizing resource utilization. However, conventional cloud service management techniques, originally designed for traditional workloads, are suboptimal for LMaaS due to its dynamic service workloads and variable request loads. To address this, we propose PreServe, a tailored LMaaS management framework centered on hierarchical prediction. PreServe incorporates a service workload predictor to estimate periodic token density at a coarse granularity and a novel request load predictor to assess the resource demand of individual LLM requests, enabling the construction of a load anticipator for each LLM instance. By integrating both long-term and short-term predictions, PreServe adjusts resource allocation in advance, mitigating the risks of instance under- or over-provisioning. Moreover, PreServe optimizes request routing by considering both current and anticipated future instance loads, ensuring balanced load distribution across instances. Evaluations on real-world LMaaS production datasets demonstrate that PreServe outperforms state-of-the-art approaches, achieving over 41.3% reduction in tail latency, an average 49.38% decrease in resource consumption, and incurring only 0.23% additional overhead.

## 14. ProxyWar: Dynamic Assessment of LLM Code Generation in Game Arenas

**Authors:** Xinyu Wang (The University of Adelaide), Wenjun Peng (The University of Adelaide), Qi Wu (University of Adelaide)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出 ProxyWar 框架，将 LLM 生成代码嵌入竞技游戏环境，通过自动化测试、迭代修复与多智能体锦标赛评估功能正确性与策略表现。揭示静态 benchmark 分数与动态实战表现存在显著差距。

**Abstract:** Large language models (LLMs) have revolutionized automated code generation, yet the evaluation of their real-world effectiveness remains limited by static benchmarks and simplistic metrics. We present ProxyWar , a novel framework that systematically assesses code generation quality by embedding LLM-generated agents within diverse, competitive game environments. Unlike existing approaches, ProxyWar evaluates both functional correctness and strategic performance, combining automated testing, iterative code repair, and multi-agent tournaments to provide a holistic view of code quality. Applied to a range of state-of-the-art coders and games, our approach uncovers notable discrepancies between benchmark scores and actual performance in dynamic settings, revealing overlooked limitations and opportunities for improvement. These findings highlight the need for richer, competition-based evaluation of code generation. Looking forward, ProxyWar lays a foundation for research into LLM-driven algorithm discovery and adaptive problem solving, including the potential for models to outperform hand-crafted agents. All code and evaluation environments will be released to foster further research and reproducibility.

## 15. Remediating Superfluous Re-Rendering in React Applications

**Authors:** Farideh Khalili, Satyajit Gokhale (Amazon), Alexi Turcotte (CISPA), Dale Xu (Boston University), Frank Tip (Northeastern University)

**Categories:** Evolution

**Awards:** Distinguished Paper Award

**中文总结:** 识别 5 种导致 React 多余重渲染的反模式，提出静态分析与自动重构规则。7,758 个仓库中 92.1% 存在至少一种反模式，23 个项目实验平均减少 33.3% 渲染操作与 20.54% 渲染时间且基本保持行为不变。

**Abstract:** React is an extremely popular framework for constructing user interfaces (UIs). A React UI is organized as a tree of components, each of which is defined by a function that returns a literal written in JSX, a syntactic extension of JavaScript consisting of a combination of XML tags, executable JavaScript code, and references to sub-components. React supports incremental re rendering by maintaining an in-memory representation of a web page’s Document Object Model (DOM) and automatically calculating a set of minimal changes that must be applied to the DOM when state changes occur. However, React’s semantics are complex and subtle, and programmers often write code that gives rise to unnecessary re-rendering, which hurts performance and responsiveness. We identify 5 React anti-patterns that give rise to unnecessary re-rendering, present a static analysis for detecting them, and rewrite rules that suggest how to refactor the code to improve rendering performance. The static analysis is potentially unsound, so developers should carefully review the suggested refactorings. A survey of 7,758 React repositories showed that 92.1% of them exhibit at least one anti-pattern, and careful experimental evaluation on 23 React projects revealed that the suggested refactoring reduces the number of rendering operations by 33.3% on average while preserving application behavior in all but one case. With a small increase in code complexity, we find an average reduction in rendering time of 20.54%, and three case studies reveal that the refactorings can greatly improve application responsiveness as the number of components scales.

## 16. SEAlign: Alignment Training for Software Engineering Agent

**Authors:** Kechi Zhang (Peking University, China), Huangzhao Zhang (Verdent AI), Ge Li (Peking University), Jinliang You (Peking University), Jia Li, Yunfei Zhao (Peking University), Zhi Jin (Peking University, Wuhan University)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出面向真实软件工程的 alignment 框架 SEAlign，利用高质量工作流步骤与 MCTS 多步决策对齐及关键动作偏好优化。在 HumanEvalFix、SWE-Bench-Lite/Verified 达 SOTA，并成功自动化生成多个小型应用。

**Abstract:** Recent advances in code generation models have demonstrated impressive capabilities in automating software development tasks, yet these models still struggle in real-world software engineering scenarios. Although current training methods, particularly post-training, excel at solving competitive programming problems, they fail to adequately prepare models for the complexities of practical software development. This misalignment raises the critical question: Are existing alignment training methods well suited for real-world software engineering tasks? In this study, we identify this issue and propose SEAlign, a novel alignment framework designed to bridge the gap between code generation models and real-world software development tasks. SEAlign leverages the unique characteristics of software engineering processes, including high-quality workflow steps, to enhance model capabilities. Our framework further employs Monte Carlo Tree Search for fine-grained alignment in multi-step decision processes, followed by preference optimization on critical actions to ensure models meet real-world requirements. We evaluate SEAlign on three standard agentic benchmarks for real-world software engineering, including HumanEvalFix, SWE-Bench-Lite, and SWE-Bench-Verified. Experimental results demonstrate state-of-the-art performance with minimal training overhead. In addition, we develop an agent-based software development platform using SEAlign, which successfully automates the creation of several small applications. Human evaluations of these applications highlight significant improvements in both task performance and user experience. Our findings underscore the potential of SEAlign to accelerate the adoption of large code models in real-world software development. We believe that this research makes a meaningful step towards fully automated software engineering.

## 17. Synthetic Repo-level Bug Dataset for Training Automated Program Repair Models

**Authors:** Minh V. T. Pham (FPT Software AI Center), Huy N. Phan (FPT Software AI Center), Hoang Nhat Phan (Nanyang Technological University), Cuong Chi Le (The University of Texas at Dallas), Tien N. Nguyen (University of Texas at Dallas), Nghi D. Q. Bui (Google Research)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出用 LLM 定向改写生成可验证合成 bug 的数据流水线，构建 SWE-Synth 仓库级 bug-fix 数据集，训练效果可比 SWE-Gym 且更易扩展。

**Abstract:** Automated program repair (APR) aims to autonomously fix software bugs, yet its effectiveness is hampered by the lack of diverse, real-world bug datasets essential for model training. Although combining large-scale mining with human effort can yield such datasets, the associated costs limit scalability. To address this, we introduce a novel, scalable synthetic data pipeline that leverages large language models (LLMs) to generate synthetic bugs through targeted LLM-based code rewriting. Our pipeline is also capable of synthesizing valuable intermediate repair steps and enriches the training signal toward correct fixes. Using our method, we create SWE-Synth, a large and contextually rich dataset of bug-fix pairs that are natural, scalable, automated verifiable, and contain intermediate repair steps. Training LLMs on our synthetic dataset yields context-aware repair strategies, that achieve repair accuracy equivalent to those trained on manually curated datasets from Github like SWE-Gym while delivering superior scalability with effortless bug synthesis, as demonstrated on popular benchmarks (SWE-Bench and BugsInPy).

## 18. The Hidden Cost of Readability: How Code Formatting Silently Consumes Your LLM Budget

**Authors:** Dangfeng Pan, Zhensu Sun (Singapore Management University), Cenyuan Zhang (Monash University), David Lo (Singapore Management University), Xiaoning Du (Monash University)

**Categories:** Software Engineering for AI

**Awards:** Distinguished Paper Award

**中文总结:** 实证表明 LLM 在格式化与去格式化代码上性能相当，去除格式元素平均可减 24.5% 输入 token，并提供双向格式转换工具以兼顾人类可读与 LLM 效率。

**Abstract:** Source code is usually formatted with elements like indentation and newlines to improve readability for human developers. However, these visual aids do not seem to be beneficial for large language models (LLMs) in the same way since the code is processed as a linear sequence of tokens. Furthermore, these additional tokens can lead to increased computational costs and longer response times for LLMs. If such formatting elements are non-essential to LLMs, we can reduce such costs by removing them from the code. To figure out the role played by formatting elements, we conduct a comprehensive empirical study to evaluate the impact of code formatting on LLM performance and efficiency. Through large-scale experiments on Fill-in-the-Middle Code Completion tasks across four programming languages (Java, Python, C++, C#) and ten LLMs—including both commercial and open-source models—we systematically analyze token count and performance when formatting elements are removed. Key findings indicate that LLMs can maintain performance across formatted code and unformatted code, achieving an average input token reduction of 24.5% with negligible output token reductions. This makes code format removal a practical optimization strategy for improving LLM efficiency. Further exploration reveals that both prompting and fine-tuning LLMs can lead to significant reductions (up to 36.1%) in output code length without compromising correctness. To facilitate practical applications, we develop a bidirectional code transformation tool for format processing, which can be seamlessly integrated into existing LLM inference workflows, ensuring both human readability and LLM efficiency.

## 19. Think Like Human Developers: Harnessing Community Knowledge for Structured Code Reasoning

**Authors:** Chengran Yang (Singapore Management University, Singapore), Zhensu Sun (Singapore Management University), Hong Jin Kang (University of Sydney), Jieke Shi (Singapore Management University), David Lo (Singapore Management University)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出 SVRC 框架，从社区讨论抽取并按 SDLC 结构化推理链，微调 CodeThinker 在 LiveCodeBench 中等难度 pass@1 提升 42.86%。

**Abstract:** Large Language Models (LLMs) have significantly advanced automated code generation, yet they struggle with complex coding tasks requiring multi-step logical reasoning. High-quality reasoning data is crucial for improving LLMs’ reasoning capabilities, but such datasets remain scarce. Existing approaches either rely on computationally expensive reinforcement learning (RL) or error-prone reasoning chains synthesized by LLMs, posing challenges in scalability and accuracy. To address this challenge, we propose SVRC (Structured and Validated Reasoning Chains for Code Generation), a novel framework that mines, restructures, and enriches reasoning chains from community-driven discussions on software engineering platforms. SVRC refines unstructured and incomplete discussions of coding problems by aligning them with Software Development Life Cycle (SDLC) principles, ensuring that reasoning chains capture real-world problem-solving strategies and support iterative refinement. To evaluate the effectiveness of SVRC, we introduce CodeThinker, an LLM fine-tuned on 12,444 reasoning-augmented samples generated by SVRC. Experiments on LiveCodeBench show that CodeThinker surpasses its base model by 42.86% on medium-level code problems in terms of pass@1 and outperforms GPT-4o-mini and GPT-4o by 73.14% and 115.86%, respectively. Our ablation study further highlights that each component of SVRC contributes to the reasoning capabilities of CodeThinker.

## 20. Towards Understanding and Characterizing Vulnerabilities in Intelligent Connected Vehicles through Real-World Exploits

**Authors:** Yuelin Wang (College of Intelligence and Computing, Tianjin University), Yuqiao Ning (China Automobile Data of Tianjin Co., Ltd. China Automotive Technology&Research Center Co.,Ltd.), Yanbang Sun (College of Intelligence and Computing, Tianjin University), Xiaofei Xie (Singapore Management University), Zhihua Xie (College of Intelligence and Computing, Tianjin University), Yang Chen (China Automobile Data of Tianjin Co., Ltd. China Automotive Technology&Research Center Co.,Ltd.), Zhen Guo (China Automobile Data of Tianjin Co., Ltd. China Automotive Technology&Research Center Co.,Ltd.), Shihao Xue (China Automobile Data of Tianjin Co., Ltd. China Automotive Technology&Research Center Co.,Ltd.), Junjie Wang (Tianjin University), Sen Chen (Nankai University)

**Categories:** Analytics

**Awards:** Distinguished Paper Award

**中文总结:** 基于 649 个真实智能网联汽车漏洞做首项大规模实证，补充 1 个新位置与 13 种新漏洞类型，并公开数据集支持后续研究。

**Abstract:** Intelligent Connected Vehicles (ICVs) are a core component of modern transportation systems, and their security is crucial as it directly relates to user safety. Despite prior research, most existing studies focus only on specific sub-components of ICVs due to their inherent complexity. As a result, there is a lack of systematic and comprehensive understanding of ICV vulnerabilities. Moreover, much of the current literature relies on human subjective analysis, such as surveys and interviews, which tends to be high-level and unvalidated, leaving a significant gap between theoretical findings and real-world attacks. To address this issue, we conducted the first large-scale empirical study on ICV vulnerabilities. We began by analyzing existing ICV security literature and summarizing the prevailing taxonomies in terms of vulnerability locations and types. To evaluate their real-world relevance, we collected a total of 649 exploitable vulnerabilities, including 592 from eight ICV vulnerability discovery competitions, Anonymous Cup, between January 2023 and April 2024, covering 48 different vehicles. The remaining 57 vulnerabilities were submitted daily by researchers. Based on this dataset, we assessed the coverage of existing taxonomies and identified several gaps, discovering one new vulnerability locations and 13 new vulnerability types. We further categorized these vulnerabilities into 6 threat types (e.g., privacy data breach) and 4 risk levels (ranging from low to critical), and analyzed common attack surfaces in ICVs. This study provides a comprehensive and data-driven analysis of ICV vulnerabilities, offering actionable insights for researchers, industry practitioners, and policymakers. To support future research, we have made our vulnerability dataset publicly available.

## 21. UniCoR: Modality Collaboration for Robust Cross-Language Hybrid Code Retrieval

**Authors:** Yang Yang (Central South University, China), Li Kuang (Centrel South University), Jiakun Liu (Harbin Institute of Technology), Zhongxin Liu (Zhejiang University), Yingjie Xia (Hangzhou Dianzi University), David Lo (Singapore Management University)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出 UniCoR 自监督跨模态混合代码检索框架，通过多视角对比学习与分布一致性提升跨语言泛化，MRR/MAP 平均提升 8.64%/11.54%。

**Abstract:** Effective code retrieval is indispensable and it has become an important paradigm to search code in hybrid mode using both natural language and code snippet. Nevertheless, it remains unclear whether existing approaches can effectively leverage such hybrid queries, particularly in cross-language contexts. We conduct a comprehensive empirical study of representative code models and reveal three challenges: (1) insufficient semantic understanding; (2) inefficient fusion in hybrid code retrieval; and (3)weak generalization in cross-language scenarios. To address these challenges, we propose UniCoR, a novel self-supervised framework that learns unified code representation representations framework designed to learn unified and robust code representations. Firstly, we design a multi-perspective supervised contrastive learning module to enhance semantic understanding and modality fusion. It aligns representations from multiple perspectives, including code-to-code, natural language-to-code, and natural language-to-natural language, enforcing the model to capture a semantic essence among modalities. Secondly, we introduce a representation distribution consistency learning module to improve cross-language generalization, which explicitly aligns the feature distributions of different programming languages, enabling language-agnostic representation learning. Extensive experiments on both empirical benchmark and large-scale benchmark show that UniCoR outperforms all baseline models, achieving an average improvement of 8.64% in MRR and 11.54% in MAP over the best-performing baseline. Furthermore, UniCoR exhibits stability in hybrid code retrieval and generalization capability in cross-language scenarios.

## 22. Well Begun is Half Done: Location-Aware and Trace-Guided Iterative Automated Vulnerability Repair

**Authors:** Zhenlei Ye (Yangzhou University), Xiaobing Sun (Yangzhou University), Sicong Cao (Nanjing University of Posts and Telecommunications), Lili Bo (Yangzhou University), Bin Li (Yangzhou University)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出 LoopRepair，先定位需补丁位置并以污点覆盖与是否引入新漏洞评估候选补丁质量，在 VulnLoc+ 上生成 27 个 plausible 补丁。

**Abstract:** The advances of large language models (LLMs) have paved the way for automated software vulnerability repair approaches, which iteratively refine the patch until it becomes plausible. Nevertheless, existing LLM-based vulnerability repair approaches face notable limitations: 1) they ignore the concern of locations that need to be patched but only concerning the repair content. 2) they lack quality assessment for generated candidate patches in the iterative process. To tackle the two limitations, we propose LoopRepair, an LLM-based approach that provides information about where should be patched first. Furthermore, LoopRepair improves the iterative repair strategy by assessing the quality of test-failing patches and selecting the best patch for the next iteration. We introduce two dimensions to assess the quality of patches: whether they introduce new vulnerabilities and the taint statement coverage. We evaluated LoopRepair on a real-world C/C++ vulnerability repair dataset VulnLoc+, which contains 40 vulnerabilities and their Proof-of-Vulnerability. The experimental results demonstrate that LoopRepair exhibits substantial improvements compared with the Neural Machine Translation (NMT)-based, Program Analysis-based, and LLM-based state-of-the-art vulnerability repair approaches. Specifically, LoopRepair is able to generate 27 plausible patches, which is comparable to or even 8 to 22 more plausible patches than the baselines. In terms of correct patch generation, LoopRepair repairs 8 to 13 additional vulnerabilities compared with existing approaches.

## 23. What Makes Code Generation Ethically Sourced?

**Authors:** Zhuolin Xu (Concordia University), Chenglin Li (Concordia University), Qiushi Li (Concordia University), Shin Hwei Tan (Concordia University)

**Categories:** AI for Software Engineering

**Awards:** Distinguished Paper Award

**中文总结:** 提出“伦理来源代码生成”（ES-CodeGen）概念并通过文献综述与 32 名从业者调查归纳 11 个维度，呼吁关注许可、隐私与代码质量等伦理问题。

**Abstract:** Several code generation models have been proposed to help reduce time and effort in solving software-related tasks. To ensure responsible AI, there are growing interests over various ethical issues (e.g., unclear licensing, privacy, fairness, and environment impact). These studies have the overarching goal of ensuring ethically sourced generation, which has gained growing attentions in speech synthesis and image generation. In this paper, we introduce the novel notion of Ethically Sourced Code Generation (ES-CodeGen) to refer to managing all processes involved in code generation model development from data collection to post-deployment via ethical and sustainable practices. To build a taxonomy of ES-CodeGen, we perform a two-phase literature review where we read 803 papers across various domains and specific to AI-based code generation. We identified 71 relevant papers with 10 initial dimensions of ES-CodeGen. To refine our dimensions and gain insights on consequences of ES-CodeGen, we surveyed 32 practitioners, which include six developers who submitted GitHub issues to opt-out from the Stack dataset (these impacted users have real-world experience of ethically sourcing issues in code generation models). The results lead to 11 dimensions of ES-CodeGen with a new dimension on code quality as practitioners have noted its importance. We also identified consequences, artifacts, and stages relevant to ES-CodeGen. Our post-survey reflection showed that most practitioners tend to ignore social-related dimensions despite their importance. Most practitioners either agreed or strongly agreed that our survey help improve their understanding of ES-CodeGen. Our study calls for attentions of various ethical issues towards ES-CodeGen.

## 24. WhisperCatcher: Demystifying Unauthorized and Encrypted Private Data Transmission in Android Applications

**Authors:** Zhaoyu Qiu (Xi'an Jiaotong University), Ming Fan (Xi'an Jiaotong University), Bocan Ma (Xi'an Jiaotong University), Yutian Tang (University of Glasgow, United Kingdom), Lei Xue (Sun Yat-Sen University), Haijun Wang (Xi'an Jiaotong University), Ting Liu (Xi'an Jiaotong University)

**Categories:** Dependability and Security

**Awards:** Distinguished Paper Award

**中文总结:** 提出 WhisperCatcher，结合启动阶段流量语义引导静动态分析恢复加密隐私数据传输，F1 95.49%，大规模测量发现 4966 个应用存在同意前传数。

**Abstract:** The privacy issues associated with Android apps are increasingly raising our concerns. Unfortunately, a large portion of privacy breaches in Android apps cannot be accurately detected by existing approaches, especially private data that is collected without consent and transmitted in encrypted form. Even if existing studies are able to break the encryption at protocol level to recover the structure and content of traffic packets, they are still unable to understand the code layer encrypted data. To solve this problem, we propose WhisperCatcher, an automated tool for analyzing unauthorized and encrypted private data transmitted by apps. For each app, WhisperCatcher first captures the raw traffic generated during the app’s startup phase, before the user consents to the privacy policy, and then extracts the semantic information. Furthermore, it utilizes the traffic semantics to guide static code analysis and extracts transmission-related key functions. Finally, it performs dynamic instrumentation analysis and recovers the encrypted data, thereby identifying unauthorized private data transmissions. Extensive evaluations show that WhisperCatcher significantly outperforms existing tools, and it achieves the recall of 91.38% and F1-Score of 95.49%, respectively. In addition, we conduct a large-scale measurement analysis on 14,879 apps and WhisperCatcher identifies 13,966 traffic flows from 4,966 apps that transmit private data prior to obtaining user consent, among which 3,838 (27.48%) flows contain app-encrypted data. Our findings highlight the potential privacy leakage risks in Android apps, which should be brought to the attention of the community.
