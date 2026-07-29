# ASE 2025 Research Track — Human and Social Aspects

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 10

## 1. Advancing Automated Ethical Profiling in SE: a Zero-Shot Evaluation of LLM Reasoning

**Authors:** Patrizio Migliarini (University of L'Aquila, Italy), Mashal Afzal Memon (University of L’Aquila, Italy), Marco Autili (University of L'Aquila, Italy), Paola Inverardi (Gran Sasso Science Institute)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334414

**中文总结:** 提出全自动零样本框架评估 16 个 LLM 在 30 个真实伦理场景下的推理能力；平均理论一致率 73.3%、道德可接受性一致率 86.7%，表明 LLM 可作为 SE 流水线中的伦理推理组件。

**Abstract:** Large Language Models (LLMs) are increasingly integrated into software engineering (SE) tools for tasks that extend beyond code synthesis, including judgment under uncertainty and reasoning in ethically significant contexts. We present a fully automated framework for assessing ethical reasoning capabilities across 16 LLMs in zero-shot setting, using 30 real-world ethically charged scenarios. Each model is prompted to identify the most applicable ethical theory to an action, assess its moral acceptability, and explain the reasoning behind their choice. Responses are compared against expert ethicists’ choices using inter-model agreement metrics. Our results show that LLMs achieve an average Theory Consistency Rate (TCR) of 73.3% and Binary Agreement Rate (BAR) on moral acceptability of 86.7%, with interpretable divergences concentrated in ethically ambiguous cases. A qualitative analysis of free-text explanations reveals strong conceptual convergence across models despite surface-level lexical diversity. These findings support the potential viability of LLMs as ethical inference engines within SE pipelines, enabling scalable, auditable, and adaptive integration of user-aligned ethical reasoning.


## 2. An Empirical Study of Knowledge Transfer in AI Pair Programming

**Authors:** Alisa Carla Welter (Saarland University), Niklas Schneider (Saarland University), Tobias Dick (Saarland University), Kallistos Weis (Saarland University), Christof Tinnes (Siemens AG), Marvin Wyrich (Saarland University), Sven Apel (Saarland University)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334486

**中文总结:** 实证比较人类结对编程与 GitHub Copilot 结对中的知识转移；两者成功转移频率与主题类别相近，但开发者对 Copilot 建议的审查明显少于人类搭档。

**Abstract:** Knowledge transfer is fundamental to human collaboration and is therefore common in software engineering. Pair programming is a prominent instance. With the rise of AI coding assistants, developers now not only work with human partners but also, as some claim, with AI pair programmers. Although studies confirm knowledge transfer during human pair programming, its effectiveness with AI coding assistants remains uncertain. To analyze knowledge transfer in both human–human and human–AI settings, we conducted an empirical study where developer pairs solved a programming task without AI support, while a separate group of individual developers completed the same task using the AI coding assistant GitHub Copilot. We extended an existing knowledge transfer framework and employed a semi-automated evaluation pipeline to assess differences in knowledge transfer episodes across both settings. We found a similar frequency of successful knowledge transfer episodes and overlapping topical categories across both settings. Two of our key findings are that developers tend to accept GitHub Copilot’s suggestions with less scrutiny than those from human pair programming partners, but also that GitHub Copilot can subtly remind developers of important code details they might otherwise overlook.


## 3. Democratizing the Cryptocurrency Ecosystem by Just-In-Time Transformation of Mining Programs

**Authors:** Wei Liu (Nanjing University), Zhenhua Li (Tsinghua University), Feng Qian (University of Southern California), Feiyu Jin (Tsinghua University), Hao Lin (Tsinghua University), Yannan Zheng (Ant Group), Bo Xiao (Ant Group), Xiaokang Qin (Ant Group), Tianyin Xu (University of Illinois at Urbana-Champaign)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334723

**中文总结:** 提出 Vectra，通过 JIT 变换在 Web 架构上识别并合并同构指令以支持 RandomX 等依赖通用硬件的挖矿算法，旨在恢复加密货币生态中被 ASIC 垄断挤压的 Web 客户端算力参与性与软件民主化。

**Abstract:** Democracy is crucial to a cryptocurrency ecosystem, as the diversity of miners (farms, personal computers, and web clients) underlays the credibility of the cryptocurrency. Among miners, web clients used to be the vast majority, e.g., 50M+ as of March 2018. As time went on, however, cryptomining was gradually monopolized by mining farms with dedicated hardware (e.g., ASICs), and web clients scaled down to ∼0.1M. To suppress mining farms, certain cryptocurrencies (like Monero) adopted new mining algorithms such as RandomX whose execution relies on general-purpose hardware architectures. Unfortunately, this further impairs web-based cryptomining as web clients cannot provide the desired architecture support to these algorithms. This paper explores how to revive software democracy of efficient web-based cryptomining, using a novel program transformation technique termed Vectra. Vectra employs just-in-time (JIT) transformations of mining programs for web architectures; it effectively identifies and merges isomorphic instructions upon execution. Vectra ensures correct transformations based on symbolic constraints of the instructions. Real-world deployments show that Vectra reduces WASM instructions by about 7× and achieves a 3×–16× speedup for web cryptomining in diverse execution environments, which translates to a high (69%–274%) return-on-investment (ROI) for common users.


## 4. From Characters to Structure: Rethinking Real-Time Collaborative Programming Models

**Authors:** Leon Freudenthaler (FH Campus Wien), Bernhard Taufner (FH Campus Wien), Karl M. Göschka (TU Wien)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334453

**中文总结:** 提出结构感知的实时协同编程传播模型，仅传输语法合法的代码变更而非逐键击字符；IntelliJ 插件实验显示相比 VS Code Live Share、Code With Me、Replit 显著降低消息量并保持可编译同步状态。

**Abstract:** Multiple programming tasks require synchronous collaboration between developers, giving rise to real-time collaborative programming tools that enable simultaneous editing of shared source code. However, most existing tools operate at the text level, propagating every keystroke–including syntactically invalid ones–without considering program structure. This results in excessive communication overhead, frequent propagation of build-breaking states, and poor synchronization. A major consequence is noticeable lag, especially under unstable network conditions, as collaborators are overwhelmed with unnecessary updates that disrupt their workflow and degrade the shared coding experience. In this paper, we introduce a novel structure-aware propagation model that transmits only syntactically valid code changes. For evaluation we implemented our tool as an IntelliJ plugin and evaluate it against three industry-standard tools–VS Code Live Share, Code With Me, and Replit–across eight representative programming scenarios. Our results show that it significantly lowers the number and size of propagated messages while maintaining consistent, buildable program states. Our findings demonstrate the potential of structure-aware propagation as a foundation for the next generation of real-time collaborative programming environments.


## 5. Interaction2Code: Benchmarking MLLM-based Interactive Webpage Code Generation from Interactive Prototyping

**Authors:** Jingyu Xiao (The Chinese University of Hong Kong), Yuxuan Wan (The Chinese University of Hong Kong), Yintong Huo (Singapore Management University, Singapore), Zixin Wang (The Chinese University of Hong Kong), Xinyi Xu (The Chinese University of Hong Kong), Wenxuan Wang (Hong Kong University of Science and Technology), Zhiyao Xu (Tsinghua University), Yuhang Wang (Southwest University), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334714

**中文总结:** 提出 Interaction-to-Code 任务与 Interaction2Code 基准（127 网页、374 交互），系统评估 MLLM 生成交互式网页代码的四类局限（交互生成不足、十种失败模式等），并提出四项增强策略。

**Abstract:** Multimodal Large Language Models (MLLMs) have demonstrated remarkable performance on the design-to-code task, i.e., generating UI code from UI mock-ups. However, existing benchmarks only contain static web pages for evaluation and ignore the dynamic interaction, limiting the practicality, usability and user engagement of the generated webpages.

To bridge these gaps, we present the first systematic investigation of MLLMs in generating interactive webpages. Specifically, we formulate the Interaction-to-Code task and establish the Interaction2Code benchmark, encompassing 127 unique webpages and 374 distinct interactions across 15 webpage types and 31 interaction categories. Through comprehensive experiments utilizing state-of-the-art (SOTA) MLLMs, evaluated via both automatic metrics and human assessments, we identify four critical limitations of MLLM on Interaction-to-Code task: (1) inadequate generation of interaction compared with full page, (2) prone to ten types of failure, (3) poor performance on visually subtle interactions, and (4) insufficient undestanding on interaction when limited to single-modality visual descriptions. To address these limitations, we propose four enhancement strategies: Interactive Element Highlighting, Failure-aware Prompting (FAP), Visual Saliency Enhancement, and Visual-Textual Descriptions Combination, all aiming at improving MLLMs’ performance on the Interaction-to-Code task. Our data and code are available in https://anonymous.4open.science/r/Interaction2Code-0E7C .


## 6. Multi-dimensional Assessment of CrowdSourced Testing Reports via LLMs

**Authors:** Yue Wang (NanJing University), Yuan Zhao (Laboratory of Data Intelligence and Interdisciplinary Innovation, Nanjing University), Shengcheng Yu (Technical University of Munich), Zhenyu Chen (Nanjing University)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334445

**中文总结:** 提出基于 LLM 的众测报告多维质量评估，除传统文本维度外新增充分性（adequacy）与竞争性（competitiveness），从多角度筛选高质量报告；实验表明该方法能有效辅助开发者审核海量众测提交。

**Abstract:** Crowdsourced testing can markedly enhance test coverage and the discovery rate of potential defects compared to traditional software testing, making it increasingly popular. However, with the widespread use of crowdsourced testing, more and more crowdworkers from various backgrounds are submitting a large number of testing reports to crowdsourced testing platforms, which hinders developers from effectively reviewing the reports. Facing a vast amount of reports with varying quality, manual review is not only time-consuming and labor-intensive but also increases costs. Therefore, how to efficiently review crowdsourced testing reports has become a major challenge. To address this challenge, we propose a multi-dimensional assessment method for crowdsourced testing reports based on large language models. This method not only inherits the textuality dimension widely used in traditional report assessment but also innovatively introduces two new dimensions: adequacy and competitiveness. It comprehensively assesses the quality of crowdsourced testing reports from multiple perspectives, aiming to better screen for high-quality crowdsourced testing reports. Through experimental analysis conducted on three different applications, we have proven the consistency of our method with human raters across various dimensions, and we have also observed an enhancement in the efficiency of report assessment.


## 7. "My productivity is boosted, but ..." Demystifying Users’ Perception on AI Coding Assistants

**Authors:** Yunbo Lyu (Singapore Management University), Zhou Yang (University of Alberta, Alberta Machine Intelligence Institute), Jieke Shi (Singapore Management University), Chang Jianming, Yue Liu (Monash University), David Lo (Singapore Management University)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334533

**中文总结:** 分析 VS Code Marketplace 中 1085 个 AI 编码助手（90% 近两年发布）及 32 个高安装量产品的用户评论，构建开发者真实使用场景下的关切与满意度分类体系；揭示「生产力提升但……」等典型价值与痛点。

**Abstract:** This paper aims to explore fundamental questions in the era when AI coding assistants like GitHub Copilot are widely adopted: \textit{what do developers truly value and criticize in AI coding assistants, and what does this reveal about their needs and expectations in real-world software development?} Unlike previous studies that conduct observational research in controlled and simulated environments, we analyze extensive, first-hand user reviews of AI coding assistants, which capture developers’ authentic perspectives and experiences drawn directly from their actual day-to-day work contexts. We identify 1,085 AI coding assistants from the Visual Studio Code Marketplace. Although they only account for 1.64% of all extensions, we observe a surge in these assistants: over 90% of them are released within the past two years. We then manually analyze the user reviews sampled from 32 AI coding assistants that have sufficient installations and reviews to construct a comprehensive taxonomy of user concerns and feedback about these assistants. We manually annotate each review’s attitude when mentioning certain aspects of coding assistants, yielding nuanced insights into user satisfaction and dissatisfaction regarding specific features, concerns, and overall tool performance. Built on top of the findings—including how users demand not just intelligent suggestions but also context-aware, customizable, and resource-efficient interactions—we propose five practical implications and suggestions to guide the enhancement of AI coding assistants that satisfy user needs.


## 8. The Cost of Downgrading Build Systems: A Case Study of Kubernetes

**Authors:** Gareema Ranjan (University of Waterloo), Mahmoud Alfadel (University of Calgary), Gengyi Sun (University of Waterloo), Shane McIntosh (University of Waterloo)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334660

**中文总结:** 以 Kubernetes 从 Bazel 降级至 Go Build 为案例，投入 3402 计算小时复现并分析构建性能权衡；Bazel 全量/增量构建更快（最多快 75%），但内存占用高 81%–351%，高并行下 CPU 负载亦更高。

**Abstract:** Build systems convert source code into deliverables. Since developers invoke builds frequently, the performance of build systems can impact productivity. Modern artifact-based build tools accelerate builds, yet prior work shows that teams may abandon them for alternatives that are easier to maintain. While prior work shows why downgrades are performed, the implications of downgrades remain largely unexplored.

In this paper, we describe a case study of the downgrade of build tools in the Kubernetes project, focusing on its downgrade from an artifact-based build tool (Bazel) to a language-specific solution (Go Build). We use 3,402 computational hours–equivalent to over four months of continuous experimentation–to reproduce and analyze the full and incremental builds of change sets during the downgrade period. On the one hand, we find that Bazel builds are faster than Go Build, completing full builds in 23.06–38.66 % less time and incremental builds in up to 75.19 % the other hand, Bazel builds impose a larger memory footprint than Go Build of 81.42–351.07 % and incremental builds, respectively. Bazel builds also impose a greater CPU load at parallelism settings above eight for full builds and above one for incremental builds. We estimate that downgrading from Bazel can increase CI resource costs by up to 76 % replicating our Kubernetes study on the four other projects that also downgraded from Bazel to older build tools. We observe that while build time penalties decrease, Bazel consistently consumes more memory. We conclude that abandoning artifact-based build tools, despite perceived maintainability benefits, tends to incur considerable performance costs for large projects. Our observations support more informed decision-making about build tool adoption and can help stakeholders to balance trade-offs, such as build maintainability and efficiency.


## 9. Understanding Feature Request Practice on GitHub via a Large-Scale Empirical Study

**Authors:** Jiajun Li (Nanjing University of Aeronautics and Astronautics), Wenhua Yang (Nanjing University of Aeronautics and Astronautics), Minxue Pan (Nanjing University), Yu Zhou (Nanjing University of Aeronautics and Astronautics)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334316

**中文总结:** 对 825 个热门 GitHub 仓库约 140 万 issue 开展 feature request 首次大规模实证研究，分析标注实践、生命周期与解决模式；发现标注不一致、时序趋势独特，且冗长并含大段代码的 request 往往更难处理。

**Abstract:** Feature requests are a key communication mechanism on GitHub, enabling users and developers to collaboratively shape the direction of open-source projects. Feature requests are prevalent and important, but have been underexplored in existing studies. There is limited understanding of how they are labeled, how they evolve, and how they are resolved. A deeper understanding of feature requests is critical, not only for improving issue triage and project management but also for fostering more effective collaboration within open-source communities. In this work, we present the first systematic and large-scale empirical study of feature requests. Drawing on 1.4 million issues from 825 popular GitHub repositories, we examine how feature requests are labeled, how their submission and backlog patterns change over a project’s lifecycle, how they differ from other types of issues in terms of resolution and engagement, and what factors contribute to their successful handling. Our findings reveal that labeling practices are often inconsistent across projects, that feature requests follow distinct temporal trends, and that those which are lengthy and contain large code snippets tend to be more difficult to resolve. By contrast, concise and clearly defined requests, particularly those submitted by experienced contributors and accompanied by active discussions, are more likely to be addressed. This study underscores the challenges of managing feature requests at scale and provides practical insights for maintainers, contributors, and researchers. To support future work in this area, we publicly release our dataset and analysis results.


## 10. Why AI Agents Still Need You: Findings from Developer-Agent Collaborations in the Wild

**Authors:** Aayush Kumar (Microsoft), Yasharth Bajpai (Microsoft), Sumit Gulwani (Microsoft), Gustavo Soares (Microsoft), Emerson Murphy-Hill (Microsoft)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11334577

**中文总结:** 观察 19 名开发者在 IDE 内用 SWE agent 处理 33 个真实 issue，约半数成功，增量协作与迭代修正优于 one-shot；揭示信任、联调与测试协作等人机协作挑战及 agent 设计启示。

**Abstract:** Software Engineering Agents (SWE agents) can autonomously perform development tasks on benchmarks like SWE Bench, but still face challenges when tackling complex and ambiguous real-world tasks. Consequently, SWE agents are often designed to allow interactivity with developers, enabling collaborative problem-solving. To understand how developers collaborate with SWE agents and the communication challenges that arise in such interactions, we observed 19 developers using an in-IDE agent to resolve 33 open issues in repositories to which they had previously contributed. Participants successfully resolved about half of these issues, with participants solving issues incrementally having greater success than those using a one-shot approach. Participants who actively collaborated with the agent and iterated on its outputs were also more successful, though they faced challenges in trusting the agent’s responses and collaborating on debugging and testing. These results have implications for successful developer-agent collaborations, and for the design of more effective SWE agents.

