# ACL 2025 软工 / Coding 相关论文

> 按统一筛选标准从 ACL 2025 主会（Long + Short Papers）录用论文中整理。共 **25** 篇。不含 Findings / Demo / Industry / Workshop。

## 各类数量

| 类别 | 数量 |
|------|------|
| Coding Agent / SWE | 6 |
| Testing / Analysis / Security | 5 |
| Program Repair / Debugging | 1 |
| Code Editing / IDE Assist | 2 |
| Verification / Program Analysis | 2 |
| Code Retrieval / Maintenance | 3 |
| Code Benchmark (practical) | 3 |
| Code Generation / SE-related | 3 |
| **合计** | **25** |

展示类型：无（Anthology 未区分 oral/poster）；体量标注 Long 24；Short 1

## Coding Agent / SWE（6）

### 1. [long] CompileAgent: Automated Real-World Repo-Level Compilation with Tool-Integrated LLM-based Agent System

- **作者（单位）**：Li Hu；Guoqiang Chen；Xiuwei Shang；Shaoyin Cheng；Benlong Wu；Gangyang Li；Xu Zhu；Weiming Zhang；Nenghai Yu
- **中文总结**：提出 CompileAgent，首个面向真实仓库级编译的 LLM Agent 框架。集成工具与流程策略，自动检索编译指令并处理编译错误。面向开源项目规模增长带来的手工编译难题。
- **Link**：https://aclanthology.org/2025.acl-long.103/
- **Abstract**：With open-source projects growing in size and complexity, manual compilation becomes tedious and error-prone, highlighting the need for automation to improve efficiency and accuracy. However, the complexity of compilation instruction search and error resolution makes automatic compilation challenging. Inspired by the success of LLM-based agents in various fields, we propose CompileAgent, the first LLM-based agent framework dedicated to repo-level compilation. CompileAgent integrates five tools and a flow-based agent strategy, enabling interaction with software artifacts for compilation instruction search and error resolution. To measure the effectiveness of our method, we design a public repo-level benchmark CompileAgentBench, and we also design two baselines for comparison by combining two compilation-friendly schemes. The performance on this benchmark shows that our method significantly improves the compilation success rate, ranging from 10\% to 71\%. Meanwhile, we evaluate the performance of CompileAgent under different agent strategies and verify the effectiveness of the flow-based strategy. Additionally, we emphasize the scalability of CompileAgent, further expanding its application prospects. The complete code and data are available at https://github.com/Ch3nYe/AutoCompiler.

### 2. [long] DARS: Dynamic Action Re-Sampling to Enhance Coding Agent Performance by Adaptive Tree Traversal

- **作者（单位）**：Vaibhav Aggarwal；Ojasv Kamal；Abhinav Japesh；Zhijing Jin；Bernhard Schölkopf
- **中文总结**：提出 DARS，通过动态动作重采样与自适应树遍历增强 coding agent。在复杂软件任务搜索中改善探索与决策。提升 agent 在编码任务上的表现。
- **Link**：https://aclanthology.org/2025.acl-long.973/
- **Abstract**：Large Language Models (LLMs) have revolutionized various domains, including natural language processing, data analysis, and software development, by enabling automation. In software engineering, LLM-powered coding agents have garnered significant attention due to their potential to automate complex development tasks, assist in debugging, and enhance productivity. However, existing approaches often struggle with sub-optimal decision-making, requiring either extensive manual intervention or inefficient compute scaling strategies. To improve coding agent performance, we present Dynamic Action Re-Sampling (DARS), a novel inference time compute scaling approach for coding agents, that is faster and more effective at recovering from sub-optimal decisions compared to baselines. While traditional agents either follow linear trajectories or rely on random sampling for scaling compute, our approach DARS works by branching out a trajectory at certain key decision points by taking an alternative action given the history of the trajectory and execution feedback of the previous attempt from that point. We evaluate our approach on SWE-Bench Lite benchmark, demonstrating that this scaling strategy achieves a pass@k score of 55\% with Claude 3.5 Sonnet V2. Our framework achieves a pass@1 rate of 47\%, outperforming state-of-the-art (SOTA) open-source frameworks.

### 3. [long] LocAgent: Graph-Guided LLM Agents for Code Localization

- **作者（单位）**：Zhaoling Chen；Robert Tang；Gangda Deng；Fang Wu；Jialong Wu；Zhiwei Jiang；Viktor Prasanna；Arman Cohan；Xingyao Wang
- **中文总结**：针对软件维护中的代码定位问题，提出图引导的 LocAgent。将代码库解析为异构图，帮助智能体在跨文件依赖中定位需修改位置。服务仓库级缺陷修复与变更定位。
- **Link**：https://aclanthology.org/2025.acl-long.426/
- **Abstract**：Code localization–identifying precisely where in a codebase changes need to be made–is a fundamental yet challenging task in software maintenance. Existing approaches struggle to efficiently navigate complex codebases when identifying relevant code snippets.The challenge lies in bridging natural language problem descriptions with the target code elements, often requiring reasoning across hierarchical structures and multiple dependencies.We introduce LocAgent, a framework that addresses code localization through a graph-guided agent.By parsing codebases into directed heterogeneous graphs, LocAgent creates a lightweight representation that captures code structures and their dependencies, enabling LLM agents to effectively search and locate relevant entities through powerful multi-hop reasoning.Experimental results on real-world benchmarks demonstrate that our approach significantly enhances accuracy in code localization.Notably, our method with the fine-tuned Qwen-2.5-Coder-Instruct-32B model achieves comparable results to SOTA proprietary models at greatly reduced cost (approximately 86\% reduction), reaching up to 92.7\% accuracy on file-level localization while improving downstream GitHub issue resolution success rates by 12\% for multiple attempts (Pass@10). Our code is available at \urlhttps://github.com/gersteinlab/LocAgent.

### 4. [long] Planning-Driven Programming: A Large Language Model Programming Workflow

- **作者（单位）**：Chao Lei；Yanchuan Chang；Nir Lipovetzky；Krista A. Ehinger
- **中文总结**：提出规划驱动的 LLM 编程工作流，将规划与代码实现结合。强调多步软件开发过程中的结构化规划。面向提升 LLM 完成编程任务的可靠性与流程性。
- **Link**：https://aclanthology.org/2025.acl-long.621/
- **Abstract**：The strong performance of large language models (LLMs) raises extensive discussion on their application to code generation. Recent research suggests continuous program refinements through visible tests to improve code generation accuracy in LLMs. However, these methods suffer from LLMs' inefficiency and limited reasoning capacity. In this work, we propose an LLM programming workflow (LPW) designed to improve both initial code generation and subsequent refinements within a structured two-phase workflow. Specifically, the solution generation phase formulates a solution plan, which is then verified through visible tests to specify the intended natural language solution. Subsequently, the code implementation phase drafts an initial code according to the solution plan and its verification. If the generated code fails the visible tests, the plan verification serves as the intended solution to consistently inform the refinement process for correcting bugs. Compared to state-of-the-art methods across various existing LLMs, LPW significantly improves the Pass@1 accuracy by up to 16.4\% on well-established text-to-code generation benchmarks. LPW also sets new state-of-the-art Pass@1 accuracy, achieving 98.2\% on HumanEval, 84.8\% on MBPP, 59.3\% on LiveCode, 62.6\% on APPS, and 34.7\% on CodeContests, using GPT-4o as the backbone. Our code is publicly available at: https://github.com/you68681/lpw.

### 5. [long] SoRFT: Issue Resolving with Subtask-oriented Reinforced Fine-Tuning

- **作者（单位）**：Zexiong Ma；Chao Peng；Pengfei Gao；Xiangxin Meng；Yanzhen Zou；Bing Xie
- **中文总结**：提出 SoRFT，用面向子任务的强化微调做 issue 解决。把软件工程问题拆解并强化训练，提升仓库级问题修复表现。面向真实 issue resolving 设定。
- **Link**：https://aclanthology.org/2025.acl-long.559/
- **Abstract**：Mainstream issue-resolving frameworks predominantly rely on commercial models, leading to high costs and privacy concerns. Existing training approaches for issue resolving struggle with poor generalization and fail to fully leverage open-source development resources. We propose **S**ubtask-**o**riented **R**einforced **F**ine-**T**uning (**SoRFT**), a novel training approach to enhance the issue resolving capability of LLMs. We decomposes issue resolving into structured subtasks: file localization, function localization, line localization, and code edit generation. SoRFT consists of two training stages: (1) **rejection-sampled supervised fine-tuning**, Chain of Thought (CoT) data is filtered using ground-truth before fine-tuning the LLM, and (2) **rule-based reinforcement learning**, which leverages PPO with ground-truth based rewards. We evaluate the SoRFT-trained model on SWE-Bench Verified and SWE-Bench Lite, achieving state-of-the-art (SOTA) performance among open-source models (e.g., resolve 21.4\% issues on SWE-Bench Verified with SoRFT-Qwen-7B). The experimental results demonstrate that SoRFT significantly enhances issue-resolving performance, improves model generalization, and provides a cost-efficient alternative to commercial models.

### 6. [long] UTBoost: Rigorous Evaluation of Coding Agents on SWE-Bench

- **作者（单位）**：Boxi Yu；Yuxuan Zhu；Pinjia He；Daniel Kang
- **中文总结**：指出 SWE-Bench 人工测试用例常不足，导致补丁可通过测试却未真正修复问题。提出 UTGenerator 自动扩充测试，并据此构建更严格的 coding agent 评测 UTBoost。提升对真实 GitHub issue 修复能力的评估可信度。
- **Link**：https://aclanthology.org/2025.acl-long.189/
- **Abstract**：The advent of Large Language Models (LLMs) has spurred the development of coding agents for real-world code generation.As a widely used benchmark for evaluating the code generation capabilities of these agents, SWE-Bench uses real-world problems based on GitHub issues and their corresponding pull requests.However, the manually written test cases included in these pull requests are often insufficient, allowing generated patches to pass the tests without resolving the underlying issue.To address this challenge, we introduce UTGenerator, an LLM-driven test case generator that automatically analyzes codebases and dependencies to generate test cases for real-world Python projects.Building on UTGenerator, we propose UTBoost, a comprehensive framework for test case augmentation.In our evaluation, we identified 36 task instances with insufficient test cases and uncovered 345 erroneous patches incorrectly labeled as passed in the original SWE Bench.These corrections, impacting 40.9\% of SWE-Bench Lite and 24.4\% of SWE-Bench Verified leaderboard entries, yield 18 and 11 ranking changes, respectively.

## Testing / Analysis / Security（5）

### 1. [long] Benchmarking LLMs and LLM-based Agents in Practical Vulnerability Detection for Code Repositories

- **作者（单位）**：Alperen Yildiz；Sin G Teo；Yiling Lou；Yebo Feng；Chong Wang；Dinil Mon Divakaran
- **中文总结**：提出面向代码仓库的实用漏洞检测基准 JITVul，强调跨过程/多跳调用等真实场景。评测 LLM 与基于 LLM 的 agent 在仓库级漏洞检测上的能力。
- **Link**：https://aclanthology.org/2025.acl-long.1490/
- **Abstract**：Large Language Models (LLMs) have shown promise in software vulnerability detection, particularly on function-level benchmarks like Devign and BigVul. However, real-world detection requires interprocedural analysis, as vulnerabilities often emerge through multi-hop function calls rather than isolated functions. While repository-level benchmarks like ReposVul and VulEval introduce interprocedural context, they remain computationally expensive, lack pairwise evaluation of vulnerability fixes, and explore limited context retrieval, limiting their practicality.We introduce JITVul, a JIT vulnerability detection benchmark linking each function to its vulnerability-introducing and fixing commits. Built from 879 CVEs spanning 91 vulnerability types, JITVul enables comprehensive evaluation of detection capabilities. Our results show that ReAct Agents, leveraging thought-action-observation and interprocedural context, perform better than LLMs in distinguishing vulnerable from benign code. While prompting strategies like Chain-of-Thought help LLMs, ReAct Agents require further refinement. Both methods show inconsistencies, either misidentifying vulnerabilities or over-analyzing security guards, indicating significant room for improvement.

### 2. [long] Can You Really Trust Code Copilot? Evaluating Large Language Models from a Code Security Perspective

- **作者（单位）**：Yutao Mou；Xiao Deng；Yuxiao Luo；Shikun Zhang；Wei Ye
- **中文总结**：从代码安全视角系统评测 Code Copilot/LLM 生成代码的风险。关注不安全代码与安全相关缺陷。为安全代码生成与评估提供实证依据。
- **Link**：https://aclanthology.org/2025.acl-long.849/
- **Abstract**：Code security and usability are both essential for various coding assistant applications driven by large language models (LLMs). Current code security benchmarks focus solely on single evaluation task and paradigm, such as code completion and generation, lacking comprehensive assessment across dimensions like secure code generation, vulnerability repair and discrimination. In this paper, we first propose CoV-Eval, a multi-task benchmark covering various tasks such as code completion, vulnerability repair, vulnerability detection and classification, for comprehensive evaluation of LLM code security. Besides, we developed VC-Judge, an improved judgment model that aligns closely with human experts and can review LLM-generated programs for vulnerabilities in a more efficient and reliable way. We conduct a comprehensive evaluation of 20 proprietary and open-source LLMs. Overall, while most LLMs identify vulnerable codes well, they still tend to generate insecure codes and struggle with recognizing specific vulnerability types and performing repairs. Extensive experiments and qualitative analyses reveal key challenges and optimization directions, offering insights for future research in LLM code security.

### 3. [long] Dynamic Scaling of Unit Tests for Code Reward Modeling

- **作者（单位）**：Zeyao Ma；Xiaokang Zhang；Jing Zhang；Jifan Yu；Sijia Luo；Jie Tang
- **中文总结**：研究为代码奖励建模动态扩展单元测试规模。用更多 LLM 生成的单元测试提升对候选代码解的筛选质量。服务代码生成验证与测试信号可靠性。
- **Link**：https://aclanthology.org/2025.acl-long.343/
- **Abstract**：Current large language models (LLMs) often struggle to produce accurate responses on the first attempt for complex reasoning tasks like code generation. Prior research tackles this challenge by generating multiple candidate solutions and validating them with LLM-generated unit tests. The execution results of unit tests serve as reward signals to identify correct solutions. As LLMs always confidently make mistakes, these unit tests are not reliable, thereby diminishing the quality of reward signals. Motivated by the observation that scaling the number of solutions improves LLM performance, we explore the impact of scaling unit tests to enhance reward signal quality. Our pioneer experiment reveals a positive correlation between the number of unit tests and reward signal quality, with greater benefits observed in more challenging problems. Based on these insights, we propose CodeRM-8B, a lightweight yet effective unit test generator that enables efficient and high-quality unit test scaling. Additionally, we implement a dynamic scaling mechanism that adapts the number of unit tests based on problem difficulty, further improving efficiency. Experimental results show that our approach significantly improves performance across various models on three benchmarks (e.g., with gains of 18.43 for Llama3-8B and 3.42 for GPT-4o-mini on HumanEval Plus). The parameters of CodeRM-8B and corresponding training data will be available upon publication.

### 4. [long] LLM-Powered Test Case Generation for Detecting Bugs in Plausible Programs

- **作者（单位）**：Kaibo Liu；Zhenpeng Chen；Yiyang Liu；Jie M. Zhang；Mark Harman；Yudong Han；Yun Ma；Yihong Dong；Ge Li；Gang Huang
- **中文总结**：提出 TrickCatcher，用 LLM 为“看似正确但仍含缺陷”的程序生成测试用例。通过变体生成与规格驱动输入，揭露现有测试未覆盖的 bug。面向软件测试中难捉缺陷的检测。
- **Link**：https://aclanthology.org/2025.acl-long.20/
- **Abstract**：Detecting tricky bugs in plausible programs, those that pass existing test suites yet still contain bugs, remains a significant challenge in software testing. To address this problem, we propose TrickCatcher, an LLM-powered approach to generating test cases for uncovering bugs in plausible programs. TrickCatcher operates in three stages: First, it uses an LLM to generate program variants based on the program under test (PUT) and its specification. Second, it employs an LLM to construct an input generator from the specification for producing test inputs. Finally, these inputs are executed on both the PUT and its program variants to detect inconsistencies in their outputs. We evaluate TrickCatcher on two datasets, TrickyBugs and EvalPlus, which include 366 human-written and 151 AI-generated plausible programs with tricky bugs. TrickCatcher achieves recall, precision, and F1 scores that are 1.80\texttimes, 2.65\texttimes, and 1.66\texttimes those of the state-of-the-art baselines, respectively. Code and data used are available at https://github.com/RinCloud/TrickCatcher/.

### 5. [long] Teaching an Old LLM Secure Coding: Localized Preference Optimization on Distilled Preferences

- **作者（单位）**：Mohammad Saqib Hasan；Saikat Chakraborty；Santu Karmaker；Niranjan Balasubramanian
- **中文总结**：针对 LLM 生成代码的安全问题，蒸馏不安全/安全代码偏好数据并做局部偏好优化。让较小/既有模型学习安全编码。面向安全代码生成对齐。
- **Link**：https://aclanthology.org/2025.acl-long.1263/
- **Abstract**：LLM generated code often contains security issues. We address two key challenges in improving secure code generation. First, obtaining high quality training data covering a broad set of security issues is critical. To address this, we introduce a method for distilling a preference dataset of insecure and secure code pairs from frontier LLMs, along with a security reasoning that explains the issues and the fix. The key idea here is to make use of security knowledge sources to devise a systematic prompting strategy that ensures broad coverage. Second, aligning models to secure code requires focusing on localized regions of code. Direct preference optimization methods, like SimPO, are not designed to handle these localized differences and turn out to be ineffective. We address this with a new localized preference optimization algorithm that masks the security related tokens in both the winning (secure) and losing (insecure) responses. To prevent loss in code quality, we also add a regularizer. Evaluations show that both training on our dataset, DiSCo, and the new preference optimization algorithm, LPO, yield substantial reductions in code insecurity while also improving overall code quality. Code and dataset are available at https://github.com/StonyBrookNLP/disco-lpo.

## Program Repair / Debugging（1）

### 1. [long] Revisit Self-Debugging with Self-Generated Tests for Code Generation

- **作者（单位）**：Xiancai Chen；Zhengwei Tao；Kechi Zhang；Changzhi Zhou；Xinyu Zhang；Wanli Gu；Yuanpeng He；Mengdi Zhang；Xunliang Cai；Haiyan Zhao；Zhi Jin
- **中文总结**：重新审视基于自生成测试的 self-debugging。分析用模型自测反馈进行代码修复/调试的效果与局限。面向代码生成后的自动调试流程。
- **Link**：https://aclanthology.org/2025.acl-long.881/
- **Abstract**：Large language models (LLMs) have demonstrated significant advancements in code generation, yet they still face challenges when tackling tasks that extend beyond their basic capabilities. Recently, the concept of self-debugging has been proposed as a way to enhance code generation performance by leveraging execution feedback from tests. However, the availability of high-quality tests in real-world scenarios is often limited. In this context, self-debugging with self-generated tests emerges as a promising solution, though its limitations and practical potential have not been fully explored. To address this gap, we investigate the efficacy of self-debugging in code generation tasks. We propose and analyze two distinct paradigms for the self-debugging process: post-execution and in-execution self-debugging. Our findings reveal that post-execution self-debugging struggles with the test bias introduced by self-generated tests, which can lead to misleading feedback. In contrast, in-execution self-debugging enables LLMs to mitigate this bias and leverage intermediate states during program execution. By focusing on runtime information rather than relying solely on potentially flawed self-generated tests, this approach demonstrates significant promise for improving the robustness and accuracy of LLMs in code generation tasks.

## Code Editing / IDE Assist（2）

### 1. [long] M2RC-EVAL: Massively Multilingual Repository-level Code Completion Evaluation

- **作者（单位）**：Jiaheng Liu；Ken Deng；Congnan Liu；Jian Yang；Shukai Liu；He Zhu；Peng Zhao；Linzheng Chai；Yanan Wu；JinKe JinKe；Ge Zhang；Zekun Moore Wang；Guoan Zhang；Yingshui Tan；Bangyu Xiang；Zhaoxiang Zhang；Wenbo Su；Bo Zheng
- **中文总结**：提出 M2RC-EVAL，大规模多语言仓库级代码补全评测。评估模型在真实仓库上下文中的补全能力。服务 IDE/仓库级代码补全研究。
- **Link**：https://aclanthology.org/2025.acl-long.763/
- **Abstract**：Repository-level code completion has drawn great attention in software engineering, and several benchmarks have been introduced. However, existing repository-level code completion benchmarks usually focus on a limited number of languages (\ensuremath<5), which cannot evaluate the general code intelligence abilities across different languages for existing code Large Language Models (LLMs). Besides, the existing benchmarks usually report overall average scores of different languages, where the fine-grained abilities in different completion scenarios are ignored. Therefore, to facilitate the research of code LLMs in multilingual scenarios, we propose a massively multilingual repository-level code completion benchmark covering 18 programming languages (called M2RC-EVAL), and two types of fine-grained annotations (i.e., bucket-level and semantic-level) on different completion scenarios are provided, where we obtain these annotations based on the parsed abstract syntax tree. Moreover, we also curate a massively multilingual instruction corpora M2RC-INSTRUCT dataset to improve the repository-level code completion abilities of existing code LLMs. Comprehensive experimental results demonstrate the effectiveness of our M2RC-EVAL and M2RC-INSTRUCT.

### 2. [short] CoRet: Improved Retriever for Code Editing

- **作者（单位）**：Fabio James Fehr；Prabhu Teja S；Luca Franceschi；Giovanni Zappella
- **中文总结**：提出面向代码编辑的稠密检索模型 CoRet，融合代码语义、仓库结构与调用图。按实现功能/修 bug 等自然语言请求检索相关代码片段。对接 SWE-bench 等仓库级编辑场景。
- **Link**：https://aclanthology.org/2025.acl-short.62/
- **Abstract**：In this paper, we introduce CoRet, a dense retrieval model designed for code-editing tasks that integrates code semantics, repository structure, and call-graph dependencies. The model focuses on retrieving relevant portions of a code repository based on natural language queries such as requests to implement new features or fix bugs. These retrieved code chunks can then be presented to an user or to a second code-editing model or agent. To train CoRet, we propose a loss function explicitly designed for repository-level retrieval. On SWE-bench and Long Code Arena's bug localisation datasets, we show that our model substantially improves retrieval recall by at least 15 percentage points over existing models, and ablate the design choices to show their importance in achieving these results.

## Verification / Program Analysis（2）

### 1. [long] Can LLMs Reason About Program Semantics? A Comprehensive Evaluation of LLMs on Formal Specification Inference

- **作者（单位）**：Thanh Le-Cong；Bach Le；Toby Murray
- **中文总结**：全面评测 LLM 能否从程序推断形式化规格/理解程序语义。检验模型对程序行为规约的推理能力。服务程序分析与规格推断相关软工问题。
- **Link**：https://aclanthology.org/2025.acl-long.1068/
- **Abstract**：Large Language Models (LLMs) are increasingly being used to automate programming tasks. However, the capabilities of LLMs in reasoning about program semantics are still inadequately studied, leaving substantial potential for further exploration. This paper introduces FormalBench, a comprehensive benchmark designed to evaluate the reasoning abilities of Large Language Models (LLMs) on program semantics. Specifically, it utilizes the task of synthesizing formal program specifications as a proxy measure for assessing the semantic reasoning of LLMs. This task requires both comprehensive reasoning over all possible program executions and the generation of precise, syntactically correct expressions that adhere to formal syntax and semantics. Using this benchmark, we evaluated the ability of LLMs to synthesize consistent and complete specifications. Our findings show that LLMs perform well with simple control flows but struggle with more complex structures, especially loops, even with advanced prompting. Additionally, LLMs exhibit limited robustness against semantic-preserving transformations. We also highlight common failure patterns and design self-repair prompts, improving success rates by 25\%. FormalBench is packaged as an executable library and has been released at https://github.com/thanhlecongg/FormalBench/.

### 2. [long] From Informal to Formal – Incorporating and Evaluating LLMs on Natural Language Requirements to Verifiable Formal Proofs

- **作者（单位）**：Jialun Cao；Yaojie Lu；Meiziniu Li；Haoyang Ma；Haokun Li；Mengda He；Cheng Wen；Le Sun；Hongyu Zhang；Shengchao Qin；Shing-Chi Cheung；Cong Tian
- **中文总结**：聚焦将自然语言需求转化为可验证形式化证明/规约。拆解形式化验证相关子任务并构建大规模指令数据评测 LLM。面向软件正确性与形式化验证应用。
- **Link**：https://aclanthology.org/2025.acl-long.1310/
- **Abstract**：The research in AI-based formal mathematical reasoning has shown an unstoppable growth trend. These studies have excelled in mathematical competitions like IMO and have made significant progress. However, these studies intertwined multiple skills simultaneously—problem-solving, reasoning, and writing formal specifications—making it hard to precisely identify the LLMs' strengths and weaknesses in each task. This paper focuses on formal verification, an immediate application scenario of formal reasoning, and breaks it down into sub-tasks. We constructed 18k high-quality instruction-response pairs across five mainstream formal specification languages (Coq, Lean4, Dafny, ACSL, and TLA+) in six tasks by distilling gpt-4o and evaluated against ten open-sourced LLMs, including recent popular DeepSeek-R1. We found that LLMs are good at writing proof segments when given either the code, or the detailed description of proof steps. Also, the fine-tuning brought about a nearly threefold improvement at most. And interestingly, we observed that fine-tuning with formal data also enhances abilities in mathematics, reasoning, and coding. We hope our findings inspire further research.

## Code Retrieval / Maintenance（3）

### 1. [long] CoIR: A Comprehensive Benchmark for Code Information Retrieval Models

- **作者（单位）**：Xiangyang Li；Kuicai Dong；Yi Quan Lee；Wei Xia；Hao Zhang；Xinyi Dai；Yasheng Wang；Ruiming Tang
- **中文总结**：提出 CoIR，系统覆盖代码信息检索任务的综合基准。统一评测代码检索模型。为维护、复用与辅助开发中的检索能力提供标准测评。
- **Link**：https://aclanthology.org/2025.acl-long.1072/
- **Abstract**：Despite the substantial success of Information Retrieval (IR) in various NLP tasks, most IR systems predominantly handle queries and corpora in natural language, neglecting the domain of code retrieval. Code retrieval is critically important yet remains under-explored, with existing methods and benchmarks inadequately representing the diversity of code in various domains and tasks. Moreover, many models have begun to overfit existing leaderboards, limiting their generalizability and real-world applicability. Addressing this gap, we present CoIR (**Co**de **I**nformation **R**etrieval Benchmark), a robust and comprehensive benchmark specifically designed to assess code retrieval capabilities. CoIR comprises ten meticulously curated code datasets, spanning eight distinctive retrieval tasks across seven diverse domains. We first discuss the construction of CoIR and its diverse dataset composition. Further, we evaluate ten widely used retrieval models using CoIR, uncovering significant difficulties in performing code retrieval tasks even with state-of-the-art systems. CoIR also introduces a simple yet effective python framework, which additionally defines various advanced modes to facilitate researchers in evaluating their models. It shares the same data schema as other popular benchmarks like MTEB and BEIR, enabling seamless cross-benchmark evaluations. Through CoIR, we aim to invigorate research in the code retrieval domain, providing a versatile benchmarking tool that encourages further development and exploration of code retrieval systems.

### 2. [long] ETF: An Entity Tracing Framework for Hallucination Detection in Code Summaries

- **作者（单位）**：Kishan Maharaj；Vitobha Munigala；Srikanth G. Tamilselvam；Prince Kumar；Sayandeep Sen；Palani Kodeswaran；Abhijit Mishra；Pushpak Bhattacharyya
- **中文总结**：提出 ETF 与 CodeSumEval，检测代码摘要中的幻觉。追踪实体以发现摘要偏离代码原意的内容。服务代码文档/维护中的摘要质量保障。
- **Link**：https://aclanthology.org/2025.acl-long.1480/
- **Abstract**：Recent advancements in large language models (LLMs) have significantly enhanced their ability to understand both natural language and code, driving their use in tasks like natural language-to-code (NL2Code) and code summarisation. However, LLMs are prone to hallucination—outputs that stray from intended meanings. Detecting hallucinations in code summarisation is especially difficult due to the complex interplay between programming and natural languages. We introduce a first-of-its-kind dataset, CodeSumEval, with \textasciitilde10K samples, curated specifically for hallucination detection in code summarisation. We further propose a novel Entity Tracing Framework (ETF) that a) utilises static program analysis to identify code entities from the program and b) uses LLMs to map and verify these entities and their intents within generated code summaries. Our experimental analysis demonstrates the framework's effectiveness, leading to a 73\% F1 score. The proposed approach provides a method for detecting hallucinations by tracing entities from the summary to the code, allowing us to evaluate summary accuracy and localise the error within the summary.

### 3. [long] OASIS: Order-Augmented Strategy for Improved Code Search

- **作者（单位）**：Zuchen Gao；Zizheng Zhan；Xianming Li；Erxin Yu；Haotian Zhang；Bin Chen；Yuqun Zhang；Jing Li
- **中文总结**：提出 OASIS，用顺序增强策略改进代码搜索。提升按查询检索相关代码的效果。服务软件维护中的代码检索需求。
- **Link**：https://aclanthology.org/2025.acl-long.904/
- **Abstract**：Code embeddings capture the semantic representations of code and are crucial for various code-related large language model (LLM) applications, such as code search. Previous training primarily relies on optimizing the InfoNCE loss by comparing positive natural language (NL)-code pairs with in-batch negatives. However, due to the sparse nature of code contexts, training solely by comparing the major differences between positive and negative pairs may fail to capture deeper semantic nuances. To address this issue, we propose a novel order-augmented strategy for improved code search (OASIS). It leverages order-based similarity labels to train models to capture subtle differences in similarity among negative pairs. Extensive benchmark evaluations demonstrate that our OASIS model significantly outperforms previous state-of-the-art models focusing solely on major positive-negative differences. It underscores the value of exploiting subtle differences among negative pairs with order labels for effective code embedding training.

## Code Benchmark (practical)（3）

### 1. [long] Benchmarking Long-Context Language Models on Long Code Understanding

- **作者（单位）**：Jia Li；Xuyuan Guo；Lei Li；Kechi Zhang；Ge Li；Jia Li；Zhengwei Tao；Fang Liu；Chongyang Tao；Yuqi Zhu；Zhi Jin
- **中文总结**：提出 LongCodeU，从多任务评测长上下文模型对长代码的理解能力。面向真实软件工程中长代码库理解需求。填补长代码理解严格评测空白。
- **Link**：https://aclanthology.org/2025.acl-long.1324/
- **Abstract**：Current advanced long-context language models offer great potential for real-world software engineering applications. However, progress in this critical domain remains hampered by a fundamental limitation: the absence of a rigorous evaluation framework for long code understanding. To gap this obstacle, we propose a long code understanding benchmark LongCodeU from four aspects (8 tasks) to evaluate LCLMs' long code understanding ability required for practical applications, including code unit perception, intra-code unit understanding, inter-code unit relation understanding, and long code documentation understanding. We evaluate 9 popular LCLMs on LongCodeU (i.e., 6 general models and 3 code models). Our experimental results reveal key limitations in current LCLMs' capabilities for long code understanding. Particularly, the performance of LCLMs drops dramatically when the long code length is greater than 32K, falling far short of their claimed 128K to 1M context windows. In the four aspects, inter-code unit relation understanding is the most challenging for LCLMs. Our study provides valuable insights for optimizing LCLMs and driving advancements in software engineering.

### 2. [long] Can Language Models Replace Programmers for Coding? REPOCOD Says `Not Yet'

- **作者（单位）**：Shanchao Liang；Nan Jiang；Yiran Hu；Lin Tan
- **中文总结**：提出 REPOCOD，用更接近真实世界的仓库级编码任务评测 LLM。发现现有短补全/合成基准难以代表真实编程，当前模型尚难替代程序员。强调真实代码库设定下的差距。
- **Link**：https://aclanthology.org/2025.acl-long.1204/
- **Abstract**：Recently, a number of repository-level code generation benchmarks–such as CoderEval, DevEval, RepoEval, RepoBench, and LongCode-Arena–have emerged to evaluate the capabilities of large language models (LLMs) beyond standalone benchmarks like HumanEval and MBPP. Thus, a natural question is, would LLMs have similar performance in real world coding tasks as their performance in these benchmarks? Unfortunately, one cannot answer this question, since these benchmarks consist of short completions, synthetic examples, or focus on limited scale repositories, failing to represent real-world coding tasks.To address these challenges, we create RepoCod, a Python code-generation benchmark containing complex tasks with realistic dependencies in real-world large projects and appropriate metrics for evaluating source code. It includes 980 whole-function generation tasks from 11 popular projects, 50.8\% of which require repository-level context. RepoCod includes 314 developer-written test cases per instance for better evaluation. We evaluate ten LLMs on RepoCod and find that none achieves more than 30\% pass@1 on RepoCod, indicating the necessity of building stronger LLMs that can help developers in real-world software development. In addition, we found that retrieval-augmented generation achieves better results than using target function dependencies as context.

### 3. [long] FEA-Bench: A Benchmark for Evaluating Repository-Level Code Generation for Feature Implementation

- **作者（单位）**：Wei Li；Xin Zhang；Zhongxin Guo；Shaoguang Mao；Wen Luo；Guangyue Peng；Yangyu Huang；Houfeng Wang；Scarlett Li
- **中文总结**：提出 FEA-Bench，评测仓库级代码生成中的功能/特性实现能力。超越函数级补全，对接真实仓库中的 feature implementation。为 repo-level SE 能力提供专门基准。
- **Link**：https://aclanthology.org/2025.acl-long.839/
- **Abstract**：Implementing new features in repository-level codebases is a crucial application of code generation models. However, current benchmarks lack a dedicated evaluation framework for this capability. To fill this gap, we introduce FEA-Bench, a benchmark designed to assess the ability of large language models (LLMs) to perform incremental development within code repositories. We collect pull requests from 83 GitHub repositories and use rule-based and intent-based filtering to construct task instances focused on new feature development. Each task instance containing code changes is paired with relevant unit test files to ensure that the solution can be verified. The feature implementation requires LLMs to simultaneously possess code completion capabilities for new components and code editing abilities for other relevant parts in the code repository, providing a more comprehensive evaluation method of LLMs' automated software engineering capabilities.Experimental results show that LLMs perform significantly worse in the FEA-Bench, highlighting considerable challenges in such repository-level incremental code development.

## Code Generation / SE-related（3）

### 1. [long] DebateCoder: Towards Collective Intelligence of LLMs via Test Case Driven LLM Debate for Code Generation

- **作者（单位）**：Jizheng Chen；Kounianhua Du；Xinyi Dai；Weiming Zhang；Xihuai Wang；Yasheng Wang；Ruiming Tang；Weinan Zhang；Yong Yu
- **中文总结**：提出 DebateCoder，通过测试用例驱动的多模型辩论提升代码生成。用执行反馈促进集体智能式改进。面向带测试验证的代码生成质量提升。
- **Link**：https://aclanthology.org/2025.acl-long.589/
- **Abstract**：With the impressive reasoning and text generation capabilities of large language models (LLMs), methods leveraging multiple LLMs to debate each other have garnered increasing attention. However, existing debate-based approaches remain limited in effectiveness in structured and detailed domains represented by code generation due to several reasons: 1) Reliance on different instances of the same LLM for debate, neglecting the potential benefits of integrating diverse models with varied internal knowledge for more comprehensive code generation, 2) under-utilization of test cases, and 3) reliance on third-party LLM moderators for result consolidation and decision-making, probably introducing hallucinations and judgment errors. To address these challenges, we propose DebateCoder to collect intelligence of LLMs via test case-driven debate for code generation. In DebateCoder, test cases serve as a medium for models to analyze code and identify bugs, while opposing models generate test cases to challenge each other's code during the debate process. These test cases, along with their execution results, are elaborately leveraged to refine and enhance the code through a novel contrastive analysis process. Furthermore, DebateCoder leverages test case outcomes to assess code quality and determine convergence criteria. Unlike previous approaches, DebateCoder emphasizes the collaborative improvement of both models through competitive debate and interactive analysis. Abundant experimental results on two datasets demonstrate the effectiveness of DebateCoder.

### 2. [long] ExploraCoder: Advancing Code Generation for Multiple Unseen APIs via Planning and Chained Exploration

- **作者（单位）**：Yunkun Wang；Yue Zhang；Zhen Qin；Chen Zhi；Binhua Li；Fei Huang；Yongbin Li；Shuiguang Deng
- **中文总结**：提出 ExploraCoder，经规划与链式探索为多个未见 API 生成代码。提升对陌生 API 的适应与调用能力。面向真实开发中需探索新 API 的场景。
- **Link**：https://aclanthology.org/2025.acl-long.887/
- **Abstract**：Large language models face intrinsic limitations in coding with APIs that are unseen in their training corpora. As libraries continuously evolve, it becomes impractical to exhaustively retrain LLMs with new API knowledge. This limitation hampers LLMs from solving programming problems which require newly introduced or privately maintained libraries. Inspired by exploratory programming paradigm in human behavior, we propose **ExploraCoder**, a training-free framework that empowers LLMs to invoke multiple unseen APIs in code solution by (1) planning a complex problem into several API invocation subtasks, and (2) experimenting with correct API usage at intermediate steps through a novel chain-of-API-exploration. We conduct evaluation on program synthesizing tasks involving complex API interactions. Experimental results demonstrate that ExploraCoder significantly improves performance for models lacking prior API knowledge, achieving absolute increases of up to 11.99\% over retrieval-based approaches and 17.28\% over pretraining-based methods in pass@10.

### 3. [long] WAFFLE: Fine-tuning Multi-Modal Model for Automated Front-End Development

- **作者（单位）**：Shanchao Liang；Nan Jiang；Shangshu Qian；Lin Tan
- **中文总结**：提出 Waffle，微调多模态模型以自动化前端开发（UI 到 HTML/代码）。处理层级结构与视觉设计到代码的鸿沟。面向前端工程自动化。
- **Link**：https://aclanthology.org/2025.acl-long.1208/
- **Abstract**：Web development involves turning UI designs into functional webpages, which can be difficult for both beginners and experienced developers due to the complexity of HTML's hierarchical structures and styles. While Large Language Models (LLMs) have shown promise in generating source code, two major challenges persist in UI-to-HTML code generation: (1) effectively representing HTML's hierarchical structure for LLMs, and (2) bridging the gap between the visual nature of UI designs and the text-based format of HTML code. To tackle these challenges, we introduce Waffle, a new fine-tuning strategy that uses a structure-aware attention mechanism to improve LLMs' understanding of HTML's structure and a contrastive fine-tuning approach to align LLMs' understanding of UI images and HTML code. Models fine-tuned with Waffle show up to 9.00 pp (percentage point) higher HTML match, 0.0982 higher CW-SSIM, 32.99 higher CLIP, and 27.12 pp higher LLEM on our new benchmark WebSight-Test and an existing benchmark Design2Code, outperforming current fine-tuning methods.
