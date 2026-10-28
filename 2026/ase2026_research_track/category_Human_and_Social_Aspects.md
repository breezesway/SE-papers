# ASE 2026 Research Track — Human and Social Aspects

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 8

## 1. A Low-Cost Human-in-the-Loop Investigation of Toxicity on GitHub at Scale

**Authors:** Rahat Rizvi Rahman (Virginia Commonwealth University, USA), Mia Mohammad Imran (Missouri University of Science and Technology, USA), Kostadin Damevski (Virginia Commonwealth University, USA)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837505

**中文总结:** 提出 HITL 标注流水线：本地小 LLM 输出毒性预测与可解释事件类别分，Random Forest 校验器仅将高风险对话送人工复核；在 12.4 万条 issue/PR 对话上规模化标注并复验、修正既有小规模毒性研究结论。

**Abstract:** Toxic interactions in open source discussions can alienate contributors and threaten project sustainability, yet prior empirical studies of GitHub toxicity have been limited in scale, raising questions about their generalizability. Scaling up is difficult because toxicity on GitHub is often implicit and context-dependent, making both fully manual annotation and LLM-based labeling unreliable. We present a human-in-the-loop (HITL) annotation methodology that makes large-scale, domain-calibrated toxicity labeling practical. A single call to a small, local LLM produces both a toxicity prediction and a set of interpretable event category scores. A lightweight Random Forest validator then uses those scores to flag the small subset of conversations most likely to be mislabeled, directing human review only where it is needed. The validator outperforms confidence-based and multi-LLM baselines while adding low annotation cost. We apply this pipeline to over 124,000 GitHub issue and pull request conversations. Using the resulting dataset, we evaluate key findings from prior small-scale research, confirming some and qualifying others, and present new insights into the prevalence, characteristics, and dynamics of toxicity across diverse open source projects.


## 2. Evaluating the Maintainability of ViewModel Tests using Multi-modal DSLs: An Industrial Mixed-Methods Study

**Authors:** Mario Fuksa (University of Stuttgart, Germany), Sandro Speth (TU Munich, Germany), Steffen Becker (University of Stuttgart, Germany)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834370

**中文总结:** 工业混合方法研究评估多模态 DSL（ViMoTest）对 ViewModel 测试可维护性的影响。定量显示其降低测试规格与规模，定性反馈表明可视化断言与重构能力减轻维护认知负担。

**Abstract:** As in many modern software engineering domains, the quality of an application's Graphical User Interface (GUI) is fundamentally verified by automated testing. 
One established approach to mitigate testing challenges is to leverage architectural patterns, such as Model-View-ViewModel (MVVM), to decouple presentation logic and test it in isolation. 
However, developing these ViewModel tests in general-purpose languages (GPLs) often forces engineers to write excessive boilerplate code for test setup and complex assertion chains. 
While multi-modal domain-specific languages (DSLs) show promise in mitigating these GPL-related issues, empirical evidence of their impact on test maintainability in practice is lacking. 
To address this gap, we present an industrial mixed-methods study evaluating how abstracting GUI tests to the ViewModel level via multi-modal DSLs impacts maintenance overhead in practice, using the ViMoTest method as our representative realization. 
After establishing industrial applicability via a pre-study comprising action research and a case study, we conducted a task-based evaluation with industry experts, triangulated with semi-structured interviews and a questionnaire. 
Quantitative results indicate that the ViMoTest method shows a strong tendency to reduce test specification effort and size compared to a C++ engineering baseline. 
Furthermore, qualitative expert feedback indicates that visual assertions and robust refactoring capabilities reduce cognitive load during structural test evolution. 
Overall, this study provides empirical evidence that multi-modal DSLs positively impact the maintainability of ViewModel tests.


## 3. Fragmented Markers, Mixed Results: A Systematic Review of AI Coding Assistants and Developer Productivity

**Authors:** Annemarie Wittig (Leipzig University, Germany), Alina Mailach (Leipzig University, Germany), Norbert Siegmund (Leipzig University, Germany)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834386

**中文总结:** 通过分阶段系统文献综述，梳理 AI 编程助手对开发者生产力的影响证据。识别出 187 种异质生产力指标且研究间高度碎片化，表明助手可能提升生产力但尚无法得出简单、与上下文无关的结论。

**Abstract:** AI coding assistants are increasingly embedded in software engineering practice, yet the literature still offers no cumulative, easily interpretable picture of their effects on software developer productivity. The central problem is not a lack of studies, but a lack of comparability: prior work operationalizes productivity through heterogeneous markers, settings, and reporting styles, making cross-study conclusions difficult. To address this, we conduct a staged systematic literature review. In the first stage, we synthesize studies that explicitly examine developer productivity. In the second, we extend the scope to productivity-related developer outcomes using SPACE as a theory-informed lens, capturing human-centered evidence that explicit productivity studies often omit. Across both stages, we analyze how productivity is operationalized, which confounding factors are discussed, and how reported effects are distributed. We identify 187 unique productivity and productivity-related markers, while individual studies typically only use five, revealing a broad but highly fragmented evidence base. Explicit productivity research is dominated by time-, output-, and artifact-oriented proxies, whereas the broader SPACE-aligned corpus makes satisfaction, psychological aspects, and well-being substantially more visible. Reported effects are often positive, but this pattern is stronger in perceived and tendency-based findings than in objective or statistically evaluated ones. Overall, the literature suggests that AI coding assistants can support productivity, but current evidence does not yet support simple, context-independent conclusions. The key contribution of this review is therefore a structured basis for making productivity evidence more interpretable, multidimensional, and comparable across studies.


## 4. On the Reliability of Code Comprehension Proxies

**Authors:** Erfan Arvan (New Jersey Institute of Technology, USA), Nadeeshan De Silva (William & Mary, USA), Oscar Chaparro (William & Mary, USA), Martin Kellogg (New Jersey Institute of Technology, USA)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834425

**中文总结:** 用 Delphi 五名工程师共识建立八段代码可理解性排序，再让 44 名学生产生 14 种文献常用理解代理并做相关分析；输入输出题与用时类代理更可靠，而语法类问题代理普遍不可靠，质疑部分既有可理解性研究结论。

**Abstract:** Prior work on code comprehension uses different comprehension proxies —for example, Likert-scale ratings or answers to input-output questions about program snippets, usually collected from students, to approximate whether code is comprehensible to software engineers, but the relative reliability of these proxies is not known. This paper investigates the relative reliability of a collection of proxies common in the extant literature with a pair of human studies. First, we conducted an expert-consensus study with a panel of five professional software engineers to establish a ground-truth comprehensibility ranking of eight code snippets by adapting the Delphi expert-consensus protocol. The Delphi protocol is widely used for expert consensus under conditions of uncertainty in other domains such as medicine and national-security forecasting, but to our knowledge, this is its first application to code comprehension research. Second, we conducted a study with 44 student participants who completed comprehension tasks, allowing us to measure 14 comprehension proxies derived from the literature on the same set of eight code snippets. Finally, we conducted a correlation analysis on the results, concluding that proxies 1) derived from input-output questions and 2) that measure response time rather than accuracy are especially reliable. We also found that proxies derived from questions about program syntax (rather than semantics) are especially unreliable, regardless of measurement strategy, which draws into question the reliability of parts of the existing comprehensibility literature.


## 5. Programming by Chat: A Large-Scale Behavioral Analysis of 11,579 Real-World AI-Assisted IDE Sessions

**Authors:** Ningzhi Tang (University of Notre Dame, USA), Chaoran Chen (University of Notre Dame, USA), Zihan Fang (Vanderbilt University, USA), Gelei Xu (University of Notre Dame, USA), Maria Dhakal (University of Notre Dame, USA), Yiyu Shi (University of Notre Dame, USA), Collin McMillan (University of Notre Dame, USA), Yu Huang (Vanderbilt University, USA), Toby Jia-Jun Li (University of Notre Dame, USA)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834377

**中文总结:** 分析 Cursor/Copilot 等 11,579 次提交到公开仓库的 IDE 聊天（74,998 条消息、899 开发者）；发现对话式编程呈渐进规格化、认知劳动外包给 AI，以及通过计划外化与约束协商管理 AI 自主性三大组织方式转变。

**Abstract:** IDE-integrated AI coding assistants, which operate conversationally within developers' working codebases with access to project context and multi-file editing, are rapidly reshaping software development. However, empirical investigation of this shift remains limited: existing studies largely rely on small-scale, controlled settings or analyze general-purpose chatbots rather than codebase-aware IDE workflows. We present, to the best of our knowledge, the first large-scale study of real-world conversational programming in IDE-native settings, analyzing 74,998 developer messages from 11,579 chat sessions across 1,300 repositories and 899 developers using Cursor and GitHub Copilot. These chats were committed to public repositories as part of routine development, capturing in-the-wild behavior. Our findings reveal three shifts in how programming work is organized: conversational programming operates as progressive specification, with developers iteratively refining outputs rather than specifying complete tasks upfront; developers redistribute cognitive work to AI, delegating diagnosis, comprehension, and validation rather than engaging with code and outputs directly; and developers actively manage the collaboration, externalizing plans into persistent artifacts, and negotiating AI autonomy through context injection and behavioral constraints. These results provide foundational empirical insights into AI-assisted development and offer implications for the design of future programming environments.


## 6. Same Scrutiny, More Time: Eye Tracking Insights into Reviewing LLM-Labelled Code

**Authors:** Ranim Khojah (Chalmers University of Technology, Sweden / University of Gothenburg, Sweden), Francisco Gomes de Oliveira Neto (Chalmers University of Technology, Sweden / University of Gothenburg, Sweden), Mazen Mohamad (RISE Research Institutes of Sweden, Sweden / Chalmers University of Technology, Sweden), Julian Frattini (Chalmers University of Technology, Sweden / University of Gothenburg, Sweden), Philipp Leitner (Chalmers University of Technology, Sweden / University of Gothenburg, Sweden)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834423

**中文总结:** 通过 Wizard-of-Oz 眼动实验发现：标注为 LLM 生成的代码会延长审查注视时间，但审查细致程度未变；审查者会依据逻辑正确性等准则调整策略。

**Abstract:** Modern software development increasingly involves the use of large language models (LLMs) to generate code.  
Despite their rapid advancement, LLMs remain prone to errors and hallucinations, emphasizing the importance of careful code inspection.  
However, in practice, developers' trust in LLM-generated code and their willingness to review it thoroughly may not align with these recommendations, which is a gap that remains largely unexplored.  
In this study, we conduct a Wizard-of-Oz experiment to examine how software engineers behave when code is explicitly labelled as LLM-generated during a code review task. We collect both behavioral data and participant feedback through eye-tracking and exit interviews.  
Combining Bayesian data analysis with qualitative analysis, we found that while the thoroughness of code review did not change for participants, they spent more time fixating on LLM-labelled code,  
indicating that the label itself influences attention.  
Practitioners also adapted their review strategy for LLM-labelled code by assessing the code based on specific criteria (e.g., logical correctness), or using the prompt to guide their review. These findings inform LLM-based tool design on labelling while incorporating the prompt as a software artifact.  
Our study reveals a gap between reviewers' intentions and actual reviewing behaviour, highlighting the need for software companies to revisit their AI policies (particularly regarding LLM-assisted development) to better support developers in reviewing LLM-generated code.


## 7. To Ban or Not to Ban? How Open Source Projects Govern GenAI Contributions

**Authors:** Wenhao Yang (Peking University, China), Runzhi He (Peking University, China), Minghui Zhou (Peking University, China)

**Categories:** Human and Social Aspects

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837448

**中文总结:** 对 67 个高可见度开源项目的 GenAI 治理材料做多阶段质性分析，归纳三类治理取向与 12 种策略及政策工具；表明治理需协同问责、验证、审查能力、代码溯源与平台基础设施，而非简单禁止 AI 贡献。

**Abstract:** Generative AI (GenAI) is playing an increasingly important role in open source software (OSS). Beyond completing code and documentation, GenAI is increasingly involved in issues, pull requests, code reviews, and security reports. Yet, cheaper generation does not mean cheaper review — and the resulting maintenance burden has pushed OSS projects to experiment with GenAI-specific rules in contribution guidelines, security policies, and repository instructions, even including a total ban on AI-assisted contributions. However, governing GenAI in OSS is far more than a ban-or-not question. The responses remain scattered, with neither a shared governance framework in practice nor a systematic understanding in research. Therefore, in this paper, we conduct a multi-stage analysis on various qualitative materials related to GenAI governance retrieved from 67 highly visible OSS projects. Our analysis identifies recurring concerns across contribution workflows, derives three governance orientations, and maps out 12 governance strategies and their policy instruments. We show that governing GenAI in OSS extends well beyond banning — it requires coordinated responses across accountability, verification, review capacity, code provenance, and platform infrastructure. Overall, our work distills dispersed community practices into a structured overview, providing a conceptual baseline for researchers and a practical reference for maintainers and platform designers.


## 8. Toward Inclusive Programming Support for Novice Programmers with Dyslexia: Insights from a Comparative Study

**Authors:** Zihan Fang (Vanderbilt University, USA), Janice Chung (Vanderbilt University, USA), Ruijia Chen (University of Wisconsin-Madison, USA), Marcia Barnes (Vanderbilt University, USA), Yuhang Zhao (University of Wisconsin-Madison, USA), Yu Huang (Vanderbilt University, USA)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834414

**中文总结:** 对 24 名新手（12 名阅读障碍、12 名对照）开展眼动与混合方法研究，比较代码与自然语言理解任务；阅读障碍组在代码理解上认知负荷更高但组间表现差距小于英语任务，为 AI 编程工具检测过载并自适应解释与反馈提供实证依据。

**Abstract:** Programming attracts a diverse range of learners, including individuals with dyslexia, a learning difficulty that affects reading, writing, and spelling despite average intelligence and educational opportunities. Although prior work has examined dyslexia in natural-language and code comprehension, we still know little about how dyslexic learners engage with code relative to natural language, and what this implies for inclusive programming environments. This gap is especially important in the AI era, as novice programmers increasingly rely on AI-powered coding and learning tools that may not address the distinct comprehension and cognitive support needs of learners with dyslexia.  
To address this gap, we conducted an eye-tracking study with a mixed-methods design involving 24 novice programmers (12 with dyslexia, 12 without) who completed paired code-comprehension and English-comprehension tasks. We found that although the two groups showed similar overall visual scanning patterns, eye-gaze features suggest higher cognitive effort among dyslexic novices during code comprehension. We also found that the performance gap between dyslexic and neurotypical learners was smaller in code comprehension than in English comprehension, suggesting that programming-specific representations may reshape, rather than eliminate, dyslexia-related challenges. In addition, dyslexic novices reported lower confidence, viewed general training methods as less effective, and described difficulties with symbolic elements and structurally complex code.  
These findings provide an empirical basis for designing AI-assisted programming tools that can detect cognitive overload and adapt explanations, feedback, and task support to better support dyslexic novices.

