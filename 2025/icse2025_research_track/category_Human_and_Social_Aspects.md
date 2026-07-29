# ICSE 2025 Research Track — Human and Social Aspects

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 33 papers

## 1. "Get Me In The Groove": A Mixed Methods Study on Supporting ADHD Professional Programmers

**Authors:** Kaia Newman (Carnegie Mellon University), Sarah Snay (University of Michigan), Madeline Endres (University of Massachusetts Amherst), Manasvi Parikh (University of Michigan), Andrew Begel (Carnegie Mellon University)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029725

**中文总结:** 混合方法研究 ADHD 程序员：分析 Reddit 论坛构建应对策略映射，并用 493 名专业开发者调查验证 ADHD 程序员在软件任务中的挑战与支持需求。

**Abstract:** Understanding the work styles of diverse programmers can help build inclusive workplaces, enabling all software engineers to excel. An estimated 10.6\% of programmers have \textit{Attention Deficit Hyperactivity Disorder} (ADHD), a condition characterized by differences in attention and working memory. Prior work has just begun to explore the impact of ADHD on software development, finding that inadequate support may negatively impact team productivity and employment. This prevents software development organizations from benefiting from ADHD-related strengths. To investigate these impacts, we conducted a two-phase mixed methods study. First, we qualitatively analyzed 99 threads (1,658 posts and comments) from \texttt{r/ADHD\_Programmers}, the largest public forum dedicated to the ADHD programmer community. We constructed a mapping that reveals how ADHD programmers apply personal strategies and organizational accommodations to address software task-specific challenges. Second, we conducted a large-scale survey of 239 ADHD and 254 non-ADHD professional programmers to validate how our qualitative data generalize to the worldwide developer population. Our results show that ADHD programmers are 1.8 to 4.4 times more likely to struggle more frequently than neurotypical developers with all challenges we consider, but especially with time management and design. Our findings have implications for inclusive and effective tool- and policy-building in software workplaces and motivate further research into the experiences of ADHD programmers.

## 2. Accessibility Issues in Ad-Driven Web Applications

**Authors:** Abdul Haddi Amjad (Virginia Tech), Muhammad Danish (Virginia Tech), Bless Jah (Virginia Tech), Muhammad Ali Gulzar (Virginia Tech)

**Categories:** Testing and Quality, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029732

**中文总结:** 大规模检测 43 万网页元素，发现 67% 网站因第三方广告引入更多无障碍违规，常见违反 WCAG 焦点可见与输入响应规则。

**Abstract:** Website accessibility is essential for inclusiveness and regulatory compliance. Although third-party advertisements (ads) are a vital revenue source for free web services, they introduce significant accessibility challenges. Leasing a website’s space to ad-serving technologies like DoubleClick results in developers losing control over ad content accessibility. Even on highly accessible websites, third-party ads can undermine adherence to Web Content Accessibility Guidelines (WCAG). We conduct the first-of-its-kind large-scale investigation of 430K website elements, including nearly 100K ad elements, to understand the accessibility of ads on websites. We seek to understand the prevalence of inaccessible ads and their overall impact on the accessibility of websites. Our findings show that 67% of websites experience increased accessibility violations due to ads, with common violations including Focus Visible (WCAG 2.4.7) and On Input (WCAG 3.2.2). Popular ad-serving technologies like Taboola, DoubleClick, and RevContent often serve ads that fail to comply with WCAG standards. Even when ads are WCAG compliant, 27% of them have alternative text in ad images that misrepresents information, potentially deceiving users. Manual inspection of a sample of these misleading ads revealed that user-identifiable data is collected on 94% of websites through interactions, such as hovering or pressing enter. Since users with disabilities often rely on tools like screen readers that require hover events to access website content, they have no choice but to compromise their privacy in order to navigate website ads. Based on our findings, we further dissect the root cause of these violations and provide design guidelines to both website developers and ad-serving technologies to achieve WCAG-compliant ad integration.

## 3. An Empirical Study on Package-Level Deprecation in Python Ecosystem

**Authors:** Zhiqing Zhong (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Shilin He (Microsoft Research), Haoxuan Wang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), BoXi Yu (The Chinese University of Hong Kong, Shenzhen), Haowen Yang (The Chinese University of Hong Kong, Shenzhen (CUHK-Shenzhen)), Pinjia He (Chinese University of Hong Kong, Shenzhen)

**Categories:** Evolution and Maintenance, Human and Social Aspects, Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11029884

**中文总结:** 混合方法实证研究 Python 生态包级 deprecation 的发布、接收与处理现状、对不活跃包的益处及开发者面临的挑战。

**Abstract:** Open-source software (OSS) plays a crucial role in modern software development. Utilizing OSS code can greatly accelerate software development, reduce redundancy, and enhance reliability. Python, a widely adopted programming language, is particularly renowned for its extensive and diverse third-party package ecosystem. However, a significant number of OSS packages within the Python ecosystem are in poor maintenance, leading to potential risks in terms of functionality and security. Consequently, it is essential to establish a deprecation mechanism that assists package developers and users in effectively managing these packages. To facilitate the establishment of the package-level deprecation mechanism, this paper presents a mixed-method empirical study, including data analysis and surveys. We investigate the current practices of announcing, receiving, and handling package-level deprecation in the Python ecosystem. We also assess the benefits of having deprecation announcements for inactively maintained packages. Furthermore, we investigate the challenges faced by package developers and users and their expectations for future deprecation practices. Our findings reveal valuable insights. For instance, 75.4\% of inactive package developers have no intention of releasing deprecation declarations for various reasons, while 89.5\% of users express a desire to be notified about the deprecation, highlighting a gap between developers and users; In many cases, no alternative solutions are available when deprecation occurs, emphasizing the need to explore practical approaches that enable seamless package handover and require less maintenance effort. We anticipate that our work will enhance the understanding of existing package-level deprecation patterns within the Python OSS realm and facilitate the development of deprecation practices for the Python community in the future.

## 4. An Exploratory Study of ML Sketches and Visual Code Assistants

**Authors:** Luis F. Gomes (Carnegie Mellon University), Vincent J. Hellendoorn (Carnegie Mellon University), Jonathan Aldrich (Carnegie Mellon University), Rui Abreu (Faculty of Engineering of the University of Porto, Portugal)

**Categories:** AI for Software Engineering, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029898

**中文总结:** 探索 IDE 内视觉代码助手原型，对 19 名数据科学家开展实验，发现 ML 工作流草图中流程图（52.6%）最常用并评估草图转代码可行性。

**Abstract:** This paper explores the integration of Visual Code Assistants in Integrated Development Environments (IDEs). In Software Engineering, whiteboard sketching is often the initial step before coding, serving as a crucial collaboration tool for developers. Previous studies have investigated patterns in SE sketches and how they are used in practice, yet methods for directly using these sketches for code generation remain limited. The emergence of visually-equipped large language models presents an opportunity to bridge this gap, which is the focus of our research. In this paper, we built a first prototype of a Visual Code Assistant to get user feedback regarding in-IDE sketch-to-code tools. We conduct an experiment with 19 data scientists, most of whom regularly sketch as part of their job. We investigate developers' mental models by analyzing patterns commonly observed in their sketches when developing an ML workflow. Analysis indicates that diagrams were the preferred organizational component (52.6\%), often accompanied by lists (42.1\%) and numbered points (36.8\%). Our tool converts their sketches into a Python notebook by querying an LLM. We use an LLM-as-judge setup to score the quality of the generated code, finding that even brief sketching can effectively generate useful code outlines. We also find a significant, positive correlation between sketch time and the quality of the generated code. We conclude the study by conducting extensive interviews to assess the tool's usefulness, explore potential use cases, and understand developers' needs. As noted by participants, promising applications for these assistants include education, prototyping, and collaborative settings. Our findings signal promise for the next generation of Code Assistants to integrate visual information, both to improve code generation and to better leverage developers' existing sketching practices.

## 5. Automated Accessibility Analysis of Dynamic Content Changes on Mobile Apps

**Authors:** Forough Mehralian (University of California at Irvine), Ziyao He (University of California, Irvine), Sam Malek (University of California at Irvine)

**Categories:** Testing and Quality, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029844

**中文总结:** 针对 Android 应用动态内容变化对读屏用户的无障碍障碍，先做形成性用户研究，再提出自动化检测框架 TIMESTUMP。

**Abstract:** With mobile apps playing an increasingly vital role in our daily lives, the importance of ensuring their accessibility for users with disabilities is also growing. Despite this, app developers often overlook the accessibility challenges encountered by users of assistive technologies, such as screen readers. Screen reader users typically navigate content sequentially, focusing on one element at a time, unaware of changes occurring elsewhere in the app. While dynamic changes to content displayed on an app’s user interface may be apparent to sighted users, they pose significant accessibility obstacles for screen reader users. Existing accessibility testing tools are unable to identify challenges faced by blind users resulting from dynamic content changes. In this work, we first conduct a formative user study on dynamic changes in Android apps and their accessibility barriers for screen reader users. We then present TIMESTUMP, an automated framework that leverages our findings in the formative study to detect accessibility issues regarding dynamic changes. Finally, we empirically evaluate TIMESTUMP on real-world apps to assess its effectiveness and efficiency in detecting such accessibility issues.

## 6. Automated Generation of Accessibility Test Reports from Recorded User Transcripts

**Authors:** Syed Fatiul Huq (University of California, Irvine), Mahan Tafreshipour (University of California at Irvine), Kate Kalcevich (Fable Tech Labs Inc.), Sam Malek (University of California at Irvine)

**Categories:** AI for Software Engineering, Human and Social Aspects

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029798

**中文总结:** 提出 Reca11，利用 GPT-4 等 LLM 从无障碍用户测试录音转写中自动提取可访问性与可用性问题，简化测试报告生成。

**Abstract:** Testing for accessibility is a significant step when developing software, as it ensures that all users, including those with disabilities, can effectively engage with web and mobile applications. While automated tools exist to detect accessibility issues in software, none are as comprehensive and effective as the process of user testing, where testers with various disabilities evaluate the application for accessibility and usability issues. However, user testing is not popular with software developers as it requires conducting lengthy interviews with users and later parsing through large recordings to derive the issues to fix. In this paper, we explore how large language models (LLMs) like GPT 4.0, which have shown promising results in context comprehension and semantic text generation, can mitigate this issue and streamline the user testing process. Our solution, called Reca11, takes in informal transcripts of test recordings and extracts the accessibility and usability issues mentioned by the tester. Our systematic prompt engineering determines the optimal configuration of input, instruction, context and demonstrations for best results. We evaluate Reca11's effectiveness on 36 user testing sessions across three applications. Based on the findings, we investigate the strengths and weaknesses of using LLMs in this space.

## 7. Between Lines of Code: Unraveling the Distinct Patterns of Machine and Human Programmers

**Authors:** Yuling Shi (Shanghai Jiao Tong University), Hongyu Zhang (Chongqing University), Chengcheng Wan (East China Normal University), Xiaodong Gu (Shanghai Jiao Tong University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029948

**中文总结:** 分析人机代码在词法多样性、简洁性、句法分段等差异，提出 DetectCodeGPT 改进 DetectGPT 以检测机器生成代码。

**Abstract:** Large language models have catalyzed an unprecedented wave in code generation. While achieving significant advances, they blur the distinctions between machine- and human-authored source code, causing integrity and authenticity issues of software artifacts. Previous methods such as DetectGPT have proven effective in discerning machine-generated texts, but they do not identify and harness the unique patterns of machine-generated code. Thus, its applicability falters when applied to code. In this paper, we carefully study the specific patterns that characterize machine and human-authored code. Through a rigorous analysis of code attributes such as lexical diversity, conciseness, and naturalness, we expose unique patterns inherent to each source. We particularly notice that the syntactic segmentation of code is a critical factor in identifying its provenance. Based on our findings, we propose a novel machine-generated code detection method called DetectCodeGPT, which improves DetectGPT by capturing the distinct stylized patterns of code. Diverging from conventional techniques that depend on external LLMs for perturbations, DetectCodeGPT perturbs the code corpus by strategically inserting spaces and newlines, ensuring both efficacy and efficiency. Experiment results show that our approach significantly outperforms state-of-the-art techniques in detecting machine-generated code.

## 8. ChatGPT Inaccuracy Mitigation during Technical Report Understanding: Are We There Yet?

**Authors:** Salma Begum Tamanna (University of Calgary, Canada), Gias Uddin (York University, Canada), Song Wang (York University), Lan Xia (IBM, Canada), Longyu Zhang (IBM, Canada)

**Categories:** Software Engineering for AI, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029792

**中文总结:** 构建 412 组技术报告问答基准，发现 RAG 增强 ChatGPT 仅 36.4% 回答正确；提出 CHIME，用 CFG 解析堆栈跟踪并改进查询验证以缓解技术文本理解幻觉。

**Abstract:** Hallucinations, the tendency to produce irrelevant/incorrect responses, are prevalent concerns in generative AI-based tools like ChatGPT. Although hallucinations in ChatGPT are studied for textual responses, it is unknown how ChatGPT hallucinates for technical texts that contain both textual and technical terms. We surveyed 47 software engineers and produced a benchmark of 412 Q&A pairs from the bug reports of two OSS projects. We find that a RAG-based ChatGPT (i.e., ChatGPT tuned with the benchmark issue reports) is 36.4% correct when producing answers to the questions, due to two reasons 1) limitations to understand complex technical contents in code snippets like stack traces, and 2) limitations to integrate contexts denoted in the technical terms and texts. We present CHIME (ChatGPT Inaccuracy Mitigation Engine) whose underlying principle is that if we can preprocess the technical reports better and guide the query validation process in ChatGPT, we can address the observed limitations. CHIME uses context-free grammar (CFG) to parse stack traces in technical reports. CHIME then verifies and fixes ChatGPT responses by applying metamorphic testing and query transformation. In our benchmark, CHIME shows 30.3% more correction over ChatGPT responses. In a user study, we find that the improved responses with CHIME are considered more useful than those generated from ChatGPT without CHIME

## 9. Code Today, Deadline Tomorrow: Procrastination Among Software Developers

**Authors:** Zeinabsadat Saghi (University of Southern California), Thomas Zimmermann (University of California, Irvine), Souti Chattopadhyay (University of Southern California)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029967

**中文总结:** 首次访谈研究开发者拖延现象（n=15），归纳 14 项负面与 8 项正面影响、三类触发因素及 19 种自我管理技巧。

**Abstract:** Procrastination, the action of delaying or postponing something, is a well-known phenomenon that is relatable to all. While it has been studied in academic settings, little is known about why software developers procrastinate. How does it affect their work? How can developers manage procrastination? This paper presents the first investigation of procrastination among developers. We conduct an interview study with (n=15) developers across different industries to understand the process of procrastination. Using qualitative coding, we report the positive and negative effects of procrastination and factors that triggered procrastination, as perceived by participants. We validate our findings using member checking. Our results reveal 14 negative effects of procrastination on developer productivity. However, participants also reported eight positive effects, four impacting their satisfaction. We also found that participants reported three categories of factors that trigger procrastination: task-related, personal, and external. Finally, we present 19 techniques reported by our participants and studies in other domains that can help developers mitigate the impacts of procrastination. These techniques focus on raising awareness and task focus, help with task planning, and provide pathways to generate team support as a mitigation means. Based on these findings, we discuss interventions for developers and recommendations for tool building to reduce procrastination. Our paper shows that procrastination has unique effects and factors among developers compared to other populations.

## 10. Decoding the Issue Resolution Process In Practice via Issue Report Analysis: A Case Study of Firefox

**Authors:** Antu Saha (William & Mary), Oscar Chaparro (William & Mary)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029751

**中文总结:** 分析 Firefox 356 份 issue 报告中的讨论，刻画实践中问题解决的阶段序列，提炼 47 种实例化模式以解码真实 issue 解决流程。

**Abstract:** Effectively managing and resolving software issues is critical for maintaining and evolving software systems. Development teams often rely on issue trackers and issue reports to track and manage the work needed during issue resolution, ranging from issue reproduction and analysis to solution design, implementation, verification, and deployment. Despite the issue resolution process being generally known in the software engineering community as a sequential list of activities, it is unknown how developers implement this process in practice and how they discuss it in issue reports. This paper aims to enhance our understanding of the issue resolution process implemented in practice by analyzing the issue reports of Mozilla Firefox. We qualitatively and quantitatively analyzed the discussions found in 356 Firefox issue reports, to identify the sequences of stages that developers go through to address various software problems. We analyzed the sequences to identify the overall resolution process at Firefox and derived a catalog of 47 patterns that represent instances of the process. We analyzed the process and patterns across multiple dimensions, including pattern complexity, issue report types, problem categories, and issue resolution times, resulting in various insights about Mozilla's issue resolution process. We discuss these findings and their implications for different stakeholders on how to better assess and improve the issue resolution process.

## 11. Deep Learning-based Code Reviews: A Paradigm Shift or a Double-Edged Sword?

**Authors:** Rosalia Tufano (Università della Svizzera Italiana), Alberto Martin-Lopez (Software Institute - USI, Lugano), Ahmad Tayeb, Ozren Dabic (Software Institute, Università della Svizzera italiana (USI), Switzerland), Sonia Haiduc, Gabriele Bavota (Software Institute @ Università della Svizzera Italiana)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029823

**中文总结:** 通过对照实验评估深度学习自动代码审查对审查质量、审查耗时与审查者信心的影响，揭示 AI 生成审查意见融入代码审查流程的实际效应与潜在风险。

**Abstract:** Several techniques have been proposed to (partially) automate code review. Early support consisted in recommending the most suited reviewer for a given change or in prioritizing the review tasks. With the advent of deep learning in software engineering, the level of automation has been pushed to new heights, with approaches able to provide feedback on source code in natural language as a human reviewer would do. Also, recent work documented open source projects adopting Large Language Models (LLMs) as co-reviewers. Although the research in this field is very active, little is known about the actual impact of including automatically generated code reviews in the code review process. While there are many aspects worth investigating (e.g., is knowledge transfer between developers affected?), in this work we focus on three of them: (i) review quality, i.e., the reviewer's ability to identify issues in the code; (ii) review cost, i.e., the time spent reviewing the code; and (iii) reviewer’s confidence, i.e., how confident is the reviewer about the provided feedback. We run a controlled experiment with 29 professional developers who reviewed different programs with/without the support of an automatically generated code review. During the experiment we monitored the reviewers’ activities, for over 50 hours of recorded code reviews. We show that reviewers consider valid most of the issues automatically identified by the LLM and that the availability of an automated review as a starting point strongly influences their behavior: Reviewers tend to focus on the code locations indicated by the LLM rather than searching for additional issues in other parts of the code. The reviewers who started from an automated review identified a higher number of low-severity issues while, however, not identifying more high- severity issues as compared to a completely manual process. Finally, the automated support did not result in saved time and did not increase the reviewers’ confidence.

## 12. Enhancing Code Generation via Bidirectional Comment-Level Mutual Grounding

**Authors:** Yifeng Di (Purdue University), Tianyi Zhang (Purdue University)

**Categories:** AI for Software Engineering, Program Analysis and Verification, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029958

**中文总结:** 提出基于代码注释的双向互 grounding 交互式代码生成方法，通过迭代注释与反馈对齐开发者意图，显著提升多种 LLM 的 Pass@1。

**Abstract:** Large Language Models (LLMs) have demonstrated unprecedented capability in code generation. However, LLM-generated code is still plagued with a wide range of functional errors, especially for complex programming tasks that LLMs have not seen before. Recent studies have shown that developers often struggle with inspecting and fixing incorrect code generated by LLMs, diminishing their productivity and trust in LLM-based code generation. Inspired by the mutual grounding theory in communication, we propose an interactive approach that leverages code comments as a medium for developers and LLMs to establish a shared understanding. Our approach facilitates iterative grounding by interleaving code generation, inline comment generation, and contextualized user feedback through editable comments to align generated code with developer intent. We evaluated our approach on two popular benchmarks and demonstrated that our approach significantly improved multiple state-of-the-art LLMs, e.g., 16.9\% Pass@1 improvement for code-davinci-002 on HumanEval. Furthermore, we conducted a user study with 12 participants in comparison to two baselines: (1) interacting with GitHub Copilot, and (2) interacting with a multi-step code generation paradigm called Multi-Turn Program Synthesis. Participants completed the given programming tasks 16.7\% faster and with 10.5\% improvement in task success rate when using our approach. Both results show that interactively refining code comments enables the collaborative establishment of mutual grounding, leading to more accurate code generation and higher developer confidence.

## 13. Exploring the Robustness of the Effect of EVO on Intention Valuation through Replication

**Authors:** Yesugen Baatartogtokh (University of Massachusetts Amherst), Kaitlyn Cook (Smith College), Alicia M. Grubb (Smith College)

**Categories:** Human and Social Aspects, Requirements and Specifications

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029947

**中文总结:** 对目标建模可视化工具 EVO 进行伪精确复现研究（n=60），检验其对意图评估加速效应的稳健性；即便被试对需求工程熟悉度较低，使用 EVO 仍显著更快完成目标建模决策且未损害质量。

**Abstract:** The development of high-quality software depends on precise and comprehensive requirements that meet the objectives of stakeholders. Goal modeling techniques have been developed to fill this gap by capturing and analyzing stakeholders' needs and allowing them to make trade-off decisions; yet, goal modeling analysis is often difficult for stakeholders to interpret. Recent work found that when subjects are given minimal training on goal modeling and access to a color visualization, called EVO, they are able to use EVO to make goal modeling decisions faster without compromising quality. In this paper, we evaluate the robustness of the empirical evidence for EVO and question the underlying color choices made by the initial designers of EVO. We conduct a pseudo-exact replication ($n = 60$) of the original EVO study, varying the experimental site and the study population. Even in our heterogeneous sample with less a priori familiarity with requirements and goal modeling, we find that individuals using EVO answered the goal-modeling questions significantly faster than those using the control, expanding the external validity of the original results. However, we find some evidence that the chosen color scheme is not intuitive and make recommendations for the goal modeling community.

## 14. Formally Verified Cloud-Scale Authorization

**Authors:** Aleks Chakarov (Amazon Web Services), Jaco Geldenhuys (Amazon Web Services), Matthew Heck (Amazon Web Services), MIchael Hicks (Amazon), Samuel Huang (Amazon Web Services), Georges-Axel Jaloyan (Amazon Web Services), Anjali Joshi (Amazon), K. Rustan M. Leino (Amazon), Mikael Mayer (Automated Reasoning Group, Amazon Web Services), Sean McLaughlin (Amazon Web Services), Akhilesh Mritunjai (Amazon.com), Clement Pit-Claudel (EPFL), Sorawee Porncharoenwase (Amazon Web Services), Florian Rabe (Amazon Web Services), Marianna Rapoport (Amazon Web Services), Giles Reger (Amazon Web Services), Cody Roux (Amazon Web Services), Neha Rungta (Amazon Web Services), Robin Salkeld (Amazon Web Services), Matthias Schlaipfer (Amazon Web Services), Daniel Schoepe (Amazon), Johanna Schwartzentruber (Amazon Web Services), Serdar Tasiran (Amazon, n.n.), Aaron Tomb (Amazon), Emina Torlak (Amazon Web Services, USA), Jean-Baptiste Tristan (Amazon), Lucas Wagner (Amazon Web Services), Michael Whalen (Amazon Web Services and the University of Minnesota), Remy Willems (Amazon), Tongtong Xiang (Amazon Web Services), Taejoon Byun (University of Minnesota), Joshua M. Cohen (Princeton University), Ruijie Fang (University of Texas at Austin), Junyoung Jang (McGill University), Jakob Rath (TU Wien), Hira Taqdees Syeda, Dominik Wagner (University of Oxford), Yongwei Yuan (Purdue University)

**Categories:** Security and Vulnerability, Evolution and Maintenance, Human and Social Aspects, Architecture and Design

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029876

**中文总结:** 使用 Dafny 形式化验证重建每秒十亿次调用的云级授权引擎，2024 年无事故上线并使客户性能提升三倍。

**Abstract:** All critical systems must evolve to meet the needs of a growing and diversifying user base. But supporting that evolution is challenging at increasing scale: Maintainers must find a way to ensure that each change does only what is intended, and will not inadvertently change behavior for existing users. This paper presents how we addressed this challenge for a cloud-scale authorization engine, invoked 1 billion times per second, by using formal verification. Over a period of four years, we built a new authorization engine, one that behaves functionally the same as its predecessor, using the verification-aware programming language Dafny. We can now confidently deploy enhancements and optimizations while maintaining the highest assurance of both correctness and backward compatibility. We deployed the new engine in 2024 without incident and customers immediately enjoyed a threefold performance improvement. The methodology we followed to build this new engine was not an off-the-shelf application of an existing verification tool, and this paper presents several key insights: 1) Rather than prove correct the existing engine, written in Java, we found it more effective to \emph{write a new engine} in Dafny, a language built for \emph{verification from the ground up}, and then compile the result to Java. 2) To ensure performance, debuggability, and to gain trust from stakeholders, we needed to generate readable, \emph{idiomatic} Java code, essentially a transliteration of the source Dafny. 3) To ensure that the specification matches the system's actual behavior, we performed \emph{extensive differential and shadow testing} throughout the development process, ultimately comparing against $10^{15}$ production samples prior to deployment. Our approach demonstrates how formal verification can be effectively applied to evolve critical legacy software at scale.

## 15. Hints Help Finding and Fixing Bugs Differently in Python and Text-based Program Representations

**Authors:** Ruchit Rawal (Max Planck Institute for Software Systems), Victor-Alexandru Padurean (Max Planck Institute for Software Systems), Sven Apel (Saarland University), Adish Singla (Max Planck Institute for Software Systems), Mariya Toneva (Max Planck Institute for Software Systems)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029721

**中文总结:** 对 753 名参与者开展众包实验，比较测试用例、概念性与详细提示在 Python 与文本化程序表示下对找错与修错的影响，发现提示效果因表示形式与用户算法理解能力而异。

**Abstract:** With the recent advances in AI programming assistants such as GitHub Copilot, programming is not limited to classical programming languages anymore--programming tasks can also be expressed and solved by end-users in natural text. Despite the availability of this new programming modality, users still face difficulties with algorithmic understanding and program debugging. One promising approach to support end-users is to provide hints to help them find and fix bugs while forming and improving their programming capabilities. While it is plausible that hints can help, it is unclear which type of hint is helpful and how this depends on program representations (classic source code or a textual representation) and the user's capability of understanding the algorithmic task. To understand the role of hints in this space, we conduct a large-scale crowd-sourced study involving 753 participants investigating the effect of three types of hints (test cases, conceptual, and detailed), across two program representations (Python and text-based), and two groups of users (with clear understanding or confusion about the algorithmic task). We find that the program representation (Python vs. text) has a significant influence on the users' accuracy at finding and fixing bugs. Surprisingly, users are more accurate at finding and fixing bugs when they see the program in natural text. Hints are generally helpful in improving accuracy, but different hints help differently depending on the program representation and the user's understanding of the algorithmic task. These findings have implications for designing next-generation programming tools that provide personalized support to users, for example, by adapting the programming modality and providing hints with respect to the user's skill level and understanding.

## 16. How Scientists Use Jupyter Notebooks: Goals, Quality Attributes, and Opportunities

**Authors:** Ruanqianqian (Lisa) Huang (University of California, San Diego), Savitha Ravi (UC San Diego), Michael He (UCSD), Boyu Tian (University of California, San Diego), Sorin Lerner (University of California at San Diego), Michael Coblenz (University of California, San Diego)

**Categories:** Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029931

**中文总结:** 通过观察 20 名科学家日常使用 Jupyter 笔记本，梳理其目标、质量属性与保障质量的策略，并总结 AI 工具融入方式；据此提出改进计算笔记本与面向科学家的编程系统的设计建议。

**Abstract:** Computational notebooks are intended to prioritize the needs of scientists, but little is known about how scientists interact with notebooks, what requirements drive scientists' software development processes, or what tactics scientists use to meet their requirements. We conducted an observational study of 20 scientists using Jupyter notebooks for their day-to-day tasks, finding that scientists prioritize different quality attributes depending on their goals. A qualitative analysis of their usage shows (1) a collection of goals scientists pursue with Jupyter notebooks, (2) a set of quality attributes that scientists value when they write software, and (3) tactics that scientists leverage to promote quality. In addition, we identify ways scientists incorporated AI tools into their notebook work. From our observations, we derive design recommendations for improving computational notebooks and future programming systems for scientists. Key opportunities pertain to helping scientists create and manage state, dependencies, and abstractions in their software, enabling more effective reuse of clearly-defined components.

## 17. Investigating the Impact of Interpersonal Challenges on Feeling Welcome in OSS

**Authors:** Bianca Trinkenreich (Colorado State University), Zixuan Feng (Oregon State University, USA), Rudrajit Choudhuri (Oregon State University), Marco Gerosa (Northern Arizona University), Anita Sarma (Oregon State University), Igor Steinmacher (NAU RESHAPE LAB)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029838

**中文总结:** 基于 Linux 基金会 706 份多样性调查，用结构方程模型分析人际挑战对开源贡献者欢迎感的影响及其在性别、种族与残障群体间的差异。

**Abstract:** The sustainability of open source software (OSS) projects hinges on contributor retention. Interpersonal challenges can inhibit a feeling of welcomeness among contributors, particularly from underrepresented groups, which impacts their decision to continue with the project. How much this impact is, varies among individuals, underlining the importance of a thorough understanding of their effects. Here, we investigate the effects of interpersonal challenges on the sense of welcomeness among diverse populations within OSS, through the diversity lenses of gender, race, and (dis)ability. We analyzed the large-scale Linux Foundation Diversity and Inclusion survey (n = 706) to model a theoretical framework linking interpersonal challenges with the sense of welcomeness through Structural Equation Models Partial Least Squares (PLS-SEM). We then examine the model to identify the impact of these challenges on different demographics through Multi-Group Analysis (MGA). Finally, we conducted a regression analysis to investigate how differently people from different demographics experience different types of interpersonal challenges. Our findings confirm the negative association between interpersonal challenges and the feeling of welcomeness in OSS, with this relationship being more pronounced among gender minorities and people with disabilities. We found that different challenges have unique impacts on how people feel welcomed, with variations across gender, race, and disability groups. We also provide evidence that people from gender minorities and with disabilities are more likely to experience interpersonal challenges than their counterparts, especially when we analyze stalking, sexual harassment, and gender. Our insights benefit OSS communities, informing potential strategies to improve the landscape of interpersonal relationships, ultimately fostering more inclusive and welcoming communities.

## 18. LiCoEval: Evaluating LLMs on License Compliance in Code Generation

**Authors:** Weiwei Xu (Peking University), Kai Gao (Peking University), Hao He (Carnegie Mellon University), Minghui Zhou (Peking University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029777

**中文总结:** 建立 LiCoEval 基准评估 LLM 生成代码的许可证合规性，定义“显著相似”标准以判定复制关系；评估 14 个主流 LLM，发现即使最优模型仍有 0.88%–2.01% 输出与开源代码显著相似。

**Abstract:** Recent advances in Large Language Models (LLMs) have revolutionized code generation, leading to widespread adoption of AI coding tools by developers. However, LLMs can generate license-protected code without providing the necessary license information, leading to potential intellectual property violations during software production. This paper addresses the critical, yet underexplored, issue of license compliance in LLM-generated code by establishing a benchmark to evaluate the ability of LLMs to provide accurate license information for their generated code. To establish this benchmark, we conduct an empirical study to identify a reasonable standard for "striking similarity" that excludes the possibility of independent creation, indicating a copy relationship between the LLM output and certain open-source code. Based on this standard, we propose an evaluation benchmark LiCoEval, to evaluate the license compliance capabilities of LLMs. Using LiCoEval, we evaluate 14 popular LLMs, finding that even top-performing LLMs produce a non-negligible proportion (0.88% to 2.01%) of code strikingly similar to existing open-source implementations. Notably, most LLMs fail to provide accurate license information, particularly for code under copyleft licenses. These findings underscore the urgent need to enhance LLM compliance capabilities in code generation tasks. Our study provides a foundation for future research and development to improve license compliance in AI-assisted software development, contributing to both the protection of open-source software copyrights and the mitigation of legal risks for LLM users.

## 19. Measuring the Runtime Performance of C++ Code Written by Humans using GitHub Copilot

**Authors:** Daniel Erhabor (University of Waterloo), Sreeharsha Udayashankar (University of Waterloo), Mei Nagappan (University of Waterloo), Samer Al-Kiswany (University of Waterloo)

**Categories:** AI for Software Engineering, Human and Social Aspects

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029749

**中文总结:** 对 32 名开发者开展用户研究，发现使用 GitHub Copilot 辅助编写的 C++ 代码在测试数据上运行时性能显著慢于不使用 Copilot 的代码。

**Abstract:** GitHub Copilot is an artificially intelligent program- ming assistant used by many developers. While a few studies have evaluated the security risks of using Copilot, there has not been any study to show if it aids developers in producing code with better runtime performance. We evaluate the runtime performance of C++ code produced when developers use GitHub Copilot versus when they do not. To this end, we conducted a user study with 32 participants where each participant solved two C++ programming problems, one with Copilot and the other without it and measured the runtime performance of the participants’ solutions on our test data. Our results suggest that using Copilot may produce C++ code with a statistically significantly slower runtime performance.

## 20. Navigating the Testing of Evolving Deep Learning Systems: An Exploratory Interview Study

**Authors:** Hanmo You (Tianjin University), Zan Wang (Tianjin University), Bin Lin (Hangzhou Dianzi University), Junjie Chen (Tianjin University)

**Categories:** Software Engineering for AI, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029900

**中文总结:** 对 22 名工业界深度学习开发者进行半结构化访谈，探索持续演化 DL 系统的测试挑战、现有应对实践与未来支持需求，总结最佳实践与研究方向。

**Abstract:** Deep Learning (DL) systems have been widely adopted across various industrial domains such as autonomous driving and intelligent healthcare. As with traditional software, DL systems also need to constantly evolve to meet ever-changing user requirements. However, ensuring the quality of these continuously evolving systems presents significant challenges, especially in the context of testing. Understanding how industry developers address these challenges and what extra obstacles they are facing could provide valuable insights for further safeguarding the quality of DL systems. To reach this goal, we conducted semi-structured interviews with 22 DL developers from diverse domains and backgrounds. More specifically, our study focuses on exploring the challenges developers encounter in testing evolving DL systems, the practical solutions they employ, and their expectations for extra support. Our results highlight the difficulties in testing evolving DL systems and identify the best practices for DL developers to address them. Additionally, we pinpoint potential future research directions to enhance testing effectiveness in evolving DL systems.

## 21. Preserving Privacy in Software Composition Analysis: A Study of Technical Solutions and Enhancements

**Authors:** Huaijin Wang (Ohio State University), Zhibo Liu (Hong Kong University of Science and Technology), Yanbo Dai (The Hong Kong University of Science and Technology (Guangzhou)), Shuai Wang (Hong Kong University of Science and Technology), Qiyi Tang (Tencent Security Keen Lab), Sen Nie (Tencent Security Keen Lab), Shi Wu (Tencent Security Keen Lab)

**Categories:** Program Analysis and Verification, Evolution and Maintenance, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029940

**中文总结:** 系统梳理软件成分分析（SCA）中的隐私保护技术方案，分析工业界“轻量本地 SCA”与远程深度分析在隐私、精度与厂商资产保护之间的权衡，并提出增强思路。

**Abstract:** Software composition analysis (SCA) denotes the process of identifying open-source software components in an input software application. SCA has been extensively developed and adopted by academia and industry. However, we notice that the modern SCA techniques in industry scenarios still need to be improved due to privacy concerns. Overall, SCA requires the users to upload their applications’ source code to a remote SCA server, which then deeply inspects the applications and reports the component usage to users. This process is privacy-sensitive since the applications may contain sensitive information, such as proprietary algorithms, trade secrets, and user data. Moreover, applications' source code is generally deemed proprietary, and users do not want to share it with the SCA vendor. To protect customers' privacy, contemporary SCA vendors often propose to deploy a "lite" version of SCA service on the customer side. To avoid the leakage of SCA vendors' valuable assets (e.g., code, model, and data), the "lite" SCA usually only performs a shallow analysis with limited accuracy. Privacy concerns have prevented the SCA technology from being used in real-world scenarios. Therefore, academia and the industry demand privacy-preserving SCA solutions. For the first time, we analyze the privacy requirements of SCA and provide a landscape depicting possible technical solutions with varying privacy gains and overheads. In particular, given that de facto SCA frameworks are primarily driven by code similarity-based techniques, we explore combining several privacy-preserving protocols to encapsulate the similarity-based SCA framework. Among all viable solutions, we find that multi-party computation (MPC) offers the strongest privacy guarantee and plausible accuracy; it, however, incurs high overhead ($184\times$). We optimize the MPC-based SCA framework by reducing the amount of crypto protocol transactions using program analysis techniques. The evaluation results show that our proposed optimizations can reduce the MPC-based SCA overhead to only 8.5% without sacrificing SCA’s privacy guarantee or accuracy.

## 22. Relationship Status: “It’s complicated” Developer-Security Expert Dynamics in Scrum

**Authors:** Houda Naji (Ruhr University Bochum), Marco Gutfleisch (Ruhr University Bochum), Alena Naiakshina (Ruhr University Bochum)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029892

**中文总结:** 通过访谈 14 名开发者与 13 名安全专家，揭示 Scrum 中双方协作的三种沟通模式与五项共性挑战及改进方向。

**Abstract:** The high number of cyber threats poses significant challenges, with impactful software exploits ranging from data theft to ransomware deployment. Unfortunately, past research highlighted limited security expertise within development teams. Collaboration between developers and security experts, therefore, emerges as one of the few workable means to address this gap. In this paper, we explore the complex interplay between developers and security experts within Scrum, one of the most widely adopted frameworks which actively promotes collaboration, to shed light on their working relationship, challenges, and potential avenues for improvement. To this end, we conducted a qualitative interview study with 14 developers and 13 security experts. Our qualitative results reveal three communication patterns and five shared challenges between the groups affecting the develop-security expert collaboration. Top challenges include consistent interaction difficulties and the lack of workable means to balance business and security needs. As a result, we found that three core Scrum values (openness, respect, courage) are missing from this relationship. Based on our results, we propose recommendations for fostering a healthy collaboration between developers and security experts, both within and beyond Scrum.

## 23. Studying Programmers Without Programming: Investigating Expertise Using Resting State fMRI

**Authors:** Zachary Karas (Vanderbilt University), Benjamin Gold (Vanderbilt University), Violet Zhou (University of Michigan), Noah Reardon (University of Michigan), Thad Polk (University of Michigan), Catie Chang (Vanderbilt University), Yu Huang (Vanderbilt University)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029944

**中文总结:** 分析 150 名参与者（含 96 名程序员）静息态 fMRI 数据，发现程序员在语言与数学相关脑区间存在更强功能连接，无需编程任务即可区分编程经验。

**Abstract:** Expert programmers are more effective at coding activities, but the reasons for this remain elusive. Accordingly, recent research has used neuroimaging such as fMRI to analyze how expert programmers might think as they perform coding activities. Those experiments have all involved specific programming tasks (i.e., comprehension), but have been unable to detect systematic differences based on coding experience. By using tasks, however, those studies may limit the number and type of brain networks involved. In Cognitive Neuroscience, researchers commonly analyze resting-state data, in which participants’ brain activity is recorded as they lay idle in the scanner. The brain’s functional organization is plastic, and can change with experience. These changes can be measured at rest, making this a suitable data type for studying how programming activities affect neural organization over time. In this paper, we analyzed the resting state scans from 150 participants, 96 of whom were programmers. We found increased connectivity in programmers between brain regions involved in language, math, and the temporal attention. Non-programmers demonstrated more connectivity with regions involved in social and emotional cognition. We found that as years of programming experience increases, connectivity decreases between two regions associated with visual processing during reading and articulation, respectively.

## 24. Trust Dynamics in AI-Assisted Development: Definitions, Factors, and Implications

**Authors:** Sadra Sabouri (University of Southern California), Philipp Eibl (University of Southern California), Xinyi Zhou (University of Southern California), Morteza Ziyadi (Amazon AGI), Nenad Medvidović (University of Southern California), Lars Lindemann (University of Southern California), Souti Chattopadhyay (University of Southern California)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029928

**中文总结:** 混合方法研究开发者对 AI 代码建议的信任：可理解性与感知正确性是主要判据，但定义与评估存在落差，开发者最终仅保留约 52% 的原始建议。

**Abstract:** Software developers increasingly rely on AI code generation utilities. To ensure that "good" code is accepted into the code base and "bad" code is rejected, developers must know when to trust an AI suggestion. Understanding how developers build this intuition is crucial to enhancing developer-AI collaborative programming. In this paper, we seek to understand how developers (1) define and (2) evaluate the trustworthiness of a code suggestion and (3) how trust evolves when using AI code assistants. To answer these questions, we conducted a mixed-method study consisting of an in-depth exploratory survey with (n=29) developers followed by an observation study (n=10). We found that comprehensibility and perceived correctness were the most frequently used factors to evaluate code suggestion trustworthiness. However, the gap in developers' definition and evaluation of trust points to a lack of support for evaluating trustworthy code in real-time. We also found that developers often alter their trust decisions, keeping only 52% of original suggestions. Based on these findings, we extracted four guidelines to enhance developer-AI interactions. We validated the guidelines through a survey with (n=7) domain experts and survey members (n=8). We discuss the validated guidelines, how to apply them, and tools to help adopt them.

## 25. UML is Back. Or is it? Investigating the Past, Present, and Future of UML in Open Source Software

**Authors:** Joseph Romeo (Software Institute - USI, Lugano, Switzerland), Marco Raglianti (Software Institute - USI, Lugano), Csaba Nagy, Michele Lanza (Software Institute - USI, Lugano)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029930

**中文总结:** 挖掘约 1.3 万个 GitHub 项目分析二十年来 UML 使用演变，确认开源中 UML 仍被低估但出现复苏迹象。

**Abstract:** Since its inception, UML, the Unified Modeling Language, has been touted as the way to go when it comes to designing and documenting software systems. While being an integral part of many university software engineering programs, UML has found little consideration among developers, especially in open source software. Reasons for this include that UML shares some shortcomings with other forms of documentation (e.g., limited availability, outdatedness, inadequate level of detail). We present a study to investigate the evolution and the current situation regarding the use of UML in open source projects. We mined and analyzed ~13k GitHub projects, developing strategies and heuristics to identify UML files through their extensions and contents, for a quantitative analysis of two decades of evolution of the usage of UML. We explored the popularity of UML, derived characteristics of projects leveraging UML, and analyzed the authors, creators and maintainers, of UML artifacts. Our study confirms that UML is indeed still under-utilized. At the same time we found evidence of a resurgence coinciding with the popularity of human-readable text-based formats, defined and used by tools like PlantUML and Mermaid. We discuss how identifying and addressing the new challenges implied by this resurgence could impact the future of UML.

## 26. Understanding Architectural Complexity, Maintenance Burden, and Developer Sentiment---a Large-Scale Study

**Authors:** Yuanfang Cai (Drexel University), Lanting He (Google), Yony Kochinski (Google), Jun Qian (Google), Ciera Jaspan (Google), Nan Zhang (Google), Antonio Bianco (Google)

**Categories:** Evolution and Maintenance, Human and Social Aspects, Mining Software Repositories, Architecture and Design

**PDF:** https://ieeexplore.ieee.org/document/11029733

**中文总结:** 对某公司 1252 个 C++/Java 项目开展大规模研究，量化架构复杂度、维护活动与 7200 份开发者调查情感之间的统计关联。

**Abstract:** Intuitively, the more complex a software system is, the harder it is to maintain. Statistically, it is not clear which complexity metrics correlate with maintenance effort; in fact, it is not even clear how to objectively measure maintenance burden, so that developers' sentiment and intuition can be supported by numbers. Without effective complexity and maintenance metrics, it remains difficult to objectively monitor maintenance, control complexity, or justify refactoring. In this paper, we report a large-scale study of 1252 projects written in C++ and Java from Company_X. We collected three categories of metrics: (1) architectural complexity, measured using propagation cost (PC), decoupling level (DL), and structural anti-patterns; (2) maintenance activity, measured using the number of changes, lines of code (LOC) written, and active coding time (ACT) spent on feature-addition vs. bug-fixing, and (3) developer sentiment on complexity and productivity, collected from 7200 survey responses. We statistically analyzed the correlations among these metrics and obtained significant evidence of the following findings: 1) the more complex the architecture is (higher propagation cost, more instances of anti-patterns), the more LOC is spent on bug-fixing, rather than adding new features; 2) developers who commit more changes for features, spend more lines of code on features, or spend more time on features also feel that they are less hindered by technical debt and complexity. To the best of our knowledge, this is the first large-scale empirical study establishing the statistical correlation among architectural complexity, maintenance activity, and developer sentiment. The implication is that, instead of solely relying upon developer sentiment and intuition to detect degraded structure or increased burden to evolve, it is possible to objectively and continuously measure and monitor architectural complexity and maintenance difficulty, increasing feature delivery efficiency by reducing architectural complexity and anti-patterns.

## 27. Understanding the Response to Open-Source Dependency Abandonment in the npm Ecosystem

**Authors:** Courtney Miller (Carnegie Mellon University), Mahmoud Jahanshahi (University of Tennessee), Audris Mockus (University of Tennessee), Bogdan Vasilescu (Raj Reddy Associate Professor of Software and Societal Systems, Carnegie Mellon University, USA), Christian Kästner (Carnegie Mellon University)

**Categories:** Evolution and Maintenance, Human and Social Aspects

**Awards:** Award Winner

**PDF:** https://ieeexplore.ieee.org/document/11029865

**中文总结:** 大规模分析 npm 广泛使用包的依赖弃用现象，发现弃用常见、大量下游项目暴露且常未响应；并给出透明度与项目 sunset 实践建议。

**Abstract:** Many developers relying on open-source digital infrastructure expect continuous maintenance, but even the most critical packages can become unmaintained. Despite this, there is little understanding of the prevalence of abandonment of widely-used packages, of subsequent exposure, and of reactions to abandonment in practice, or the factors that influence them. We perform a large-scale quantitative analysis of all widely-used npm packages and find that abandonment is common among them, that abandonment exposes many projects which often do not respond, that responses correlate with other dependency management practices, and that removal is significantly faster when a projects end-of-life status is explicitly stated. We end with recommendations to both researchers and practitioners who are facing dependency abandonment or are sunsetting projects, such as opportunities for low-effort transparency mechanisms to help exposed projects make better, more informed decisions.

## 28. Unveiling the Energy Vampires: A Methodology for Debugging Software Energy Consumption

**Authors:** Enrique Barba Roque (TU Delft), Luís Cruz (TU Delft), Thomas Durieux (TU Delft)

**Categories:** Human and Social Aspects

**Awards:** Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029858

**中文总结:** 提出软件能耗调试方法论以定位能耗热点，并以 Redis 为例发现 Alpine 较 Ubuntu 某些操作多耗 20.2% 电力，根因为 musl 与 glibc 的 memcpy 实现差异。

**Abstract:** Energy consumption in software systems is becoming increasingly important, especially in large-scale deployments. However, debugging energy-related issues remains challenging due to the lack of specialized tools. This paper presents an energy debugging methodology for identifying and isolating energy consumption hotspots in software systems. We demonstrate the methodology's effectiveness through a case study of Redis, a popular in-memory database. Our analysis reveals significant energy consumption differences between Alpine and Ubuntu distributions, with Alpine consuming up to 20.2% more power in certain operations. We trace this difference to the implementation of the `memcpy` function in different C standard libraries (musl vs. glibc). By isolating and benchmarking `memcpy`, we confirm it as the primary cause of the energy discrepancy. Our findings highlight the importance of considering energy efficiency in software dependencies and demonstrate the capability to assist developers in identifying and addressing energy-related issues. This work contributes to the growing field of sustainable software engineering by providing a systematic approach to energy debugging.

## 29. User Personas Improve Social Sustainability by Encouraging Software Developers to Deprioritize Antisocial Features

**Authors:** Bimpe Ayoola (Dalhousie University), Miikka Kuutila (Dalhousie University), Rina R. Wehbe (Dalhousie University), Paul Ralph (Dalhousie University)

**Categories:** Human and Social Aspects, Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11029937

**中文总结:** 通过 79 名学生的随机对照实验评估用户画像与利益相关者地图对功能优先级的影响，发现用户画像能促使开发者降低反社会功能优先级，从而提升软件社会可持续性。

**Abstract:** \textit{Background}: Sustainable software development involves creating software in a manner that meets present goals without undermining our ability to meet future goals. In a software engineering context, sustainability has at least four dimensions: ecological, economic, social, and technical. No interventions for improving social sustainability in software engineering have been tested in rigorous lab-based experiments, and little evidence-based guidance is available. \textit{Objective}: The purpose of this study is to evaluate the effectiveness of two interventions---stakeholder maps and persona models---for improving social sustainability by improving software feature prioritization. \textit{Method}: We conducted a randomized controlled factorial experiment with 79 undergraduate computer science students. Participants were randomly assigned to one of four groups and asked to prioritize a backlog of prosocial, neutral, and antisocial user stories for a shopping mall's digital screen display and facial recognition software. Participants received either persona models, a stakeholder map, both, or neither. We compared the differences in prioritization levels assigned to prosocial and antisocial user stories using Cumulative Link Mixed Model regression. \textit{Results}: Participants who received persona models gave significantly lower priorities to anti-social user stories but no significant difference was evident for pro-social user stories. The effects of the stakeholder map were not significant. The interaction effects were not significant. \textit{Conclusion}: Providing aspiring software professionals with well-crafted persona models causes them to de-prioritize anti-social software features. The impact of persona modelling on sustainable software development therefore warrants further study with more experience professionals. Moreover, the novel methodological strategy of assessing social sustainability behavior through backlog prioritization appears feasible in lab-based settings.

## 30. What Guides Our Choices? Modeling Developers' Trust and Behavioral Intentions Towards GenAI

**Authors:** Rudrajit Choudhuri (Oregon State University), Bianca Trinkenreich (Colorado State University), Rahul Pandita (GitHub, Inc.), Eirini Kalliamvakou (GitHub), Igor Steinmacher (NAU RESHAPE LAB), Marco Gerosa (Northern Arizona University), Christopher Sanchez (Oregon State University), Anita Sarma (Oregon State University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029764

**中文总结:** 构建开发者对 GenAI 工具信任与使用意愿的理论模型，调查 238 名软件开发者，分析信任影响因素及认知风格与采纳意图之间的关系，为 GenAI 工具集成提供依据。

**Abstract:** Generative AI (genAI) tools, such as ChatGPT or Copilot, are advertised to improve developer productivity and are being integrated into software development. However, misaligned trust, skepticism, and usability concerns can impede the adoption of such tools. Research also indicates that AI can be exclusionary, failing to support diverse users adequately. One such aspect of diversity is cognitive diversity—variations in users’ cognitive styles—that leads to divergence in perspectives and interaction styles. When an individual’s cognitive style is unsupported, it creates barriers to technology adoption. Therefore, to understand how to effectively integrate genAI tools into software development, it is first important to model what factors affect developers’ trust and intentions to adopt genAI tools in practice? We developed a theoretical model to (1) identify factors that influence developers’ trust in genAI tools and (2) examine the relationship between developers’ trust, cognitive styles, and their intentions to use these tools. We surveyed software developers (N=238) at two major global tech organizations and employed Partial Least Squares-Structural Equation Modeling (PLS-SEM) to evaluate our model. Our findings reveal that genAI’s system/output quality, functional value, and goal maintenance significantly influence developers’ trust in these tools. Furthermore, developers’ trust and cognitive styles influence their intentions to use these tools. We offer practical suggestions for designing genAI tools for effective use and inclusive user experience.

## 31. What Guides Our Choices? Modeling Developers' Trust and Behavioral Intentions Towards GenAI

**Authors:** Rudrajit Choudhuri (Oregon State University), Bianca Trinkenreich (Colorado State University), Rahul Pandita (GitHub, Inc.), Eirini Kalliamvakou (GitHub), Igor Steinmacher (NAU RESHAPE LAB), Marco Gerosa (Northern Arizona University), Christopher Sanchez (Oregon State University), Anita Sarma (Oregon State University)

**Categories:** AI for Software Engineering, Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029764

**中文总结:** 构建开发者对 GenAI 工具信任与使用意愿的理论模型，调查 238 名软件开发者，分析信任影响因素及认知风格与采纳意图之间的关系，为 GenAI 工具集成提供依据。

**Abstract:** Generative AI (genAI) tools, such as ChatGPT or Copilot, are advertised to improve developer productivity and are being integrated into software development. However, misaligned trust, skepticism, and usability concerns can impede the adoption of such tools. Research also indicates that AI can be exclusionary, failing to support diverse users adequately. One such aspect of diversity is cognitive diversity—variations in users’ cognitive styles—that leads to divergence in perspectives and interaction styles. When an individual’s cognitive style is unsupported, it creates barriers to technology adoption. Therefore, to understand how to effectively integrate genAI tools into software development, it is first important to model what factors affect developers’ trust and intentions to adopt genAI tools in practice? We developed a theoretical model to (1) identify factors that influence developers’ trust in genAI tools and (2) examine the relationship between developers’ trust, cognitive styles, and their intentions to use these tools. We surveyed software developers (N=238) at two major global tech organizations and employed Partial Least Squares-Structural Equation Modeling (PLS-SEM) to evaluate our model. Our findings reveal that genAI’s system/output quality, functional value, and goal maintenance significantly influence developers’ trust in these tools. Furthermore, developers’ trust and cognitive styles influence their intentions to use these tools. We offer practical suggestions for designing genAI tools for effective use and inclusive user experience.

## 32. When Quantum Meets Classical: Characterizing Hybrid Quantum-Classical Issues Discussed in Developer Forums

**Authors:** Jake Zappin (William and Mary), Trevor Stalnaker (William & Mary), Oscar Chaparro (William & Mary), Denys Poshyvanyk (William & Mary)

**Categories:** Program Analysis and Verification, Human and Social Aspects, Mining Software Repositories

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029802

**中文总结:** 对 531 个开发者论坛问题进行首个混合量子-经典计算实证研究，构建涵盖软件故障、硬件失败、库错误与开发者失误的分类体系。

**Abstract:** Recent advances in quantum computing have sparked excitement that this new computing paradigm could solve previously intractable problems. However, due to the faulty nature of current quantum hardware and quantum-intrinsic noise, the full potential of quantum computing is still years away. Hybrid quantum-classical computing has emerged as a possible compromise that achieves the best of both worlds. In this paper, we look at hybrid quantum-classical computing from a software engineering perspective and present the first empirical study focused on characterizing and evaluating recurrent issues faced by developers of hybrid quantum-classical applications. The study comprised a thorough analysis of 531 real-world issues faced by developers -- including software faults, hardware failures, quantum library errors, and developer mistakes -- documented in discussion threads from forums dedicated to quantum computing. By qualitatively analyzing such forum threads, we derive a comprehensive taxonomy of recurring issues in hybrid quantum-classical applications that can be used by both application and platform developers to improve the reliability of hybrid applications. The study considered how these recurring issues manifest and their causes, determining that hybrid applications are crash-dominant (74% of studied issues) and that errors were predominantly introduced by application developers (70% of issues). We conclude by identifying recurring obstacles for developers of hybrid applications and actionable recommendations to overcome them.

## 33. Who’s Pushing the Code: An Exploration of GitHub Impersonation

**Authors:** Yueke Zhang (Vanderbilt University), Anda Liang (Vanderbilt University), Xiaohan Wang (Vanderbilt University), Pamela J. Wisniewski (Vanderbilt University), Fengwei Zhang (Southern University of Science and Technology), Kevin Leach (Vanderbilt University), Yu Huang (Vanderbilt University)

**Categories:** Human and Social Aspects

**PDF:** https://ieeexplore.ieee.org/document/11029973

**中文总结:** 首次探索 GitHub 身份冒充影响，访谈 17 名贡献者发现认知不足且现有提交签名等最佳实践难以广泛落地。

**Abstract:** GitHub is one of the largest open-source software (OSS) communities for software development and collaboration. Impersonation in the OSS communities refers to the malicious act of assuming another user's identity, often aiming to gain unauthorized access to code, manipulate project outcomes, or spread misinformation. With several recent real-world attacks resulting from impersonation, this issue is becoming and increasingly problematic concern within the OSS community. We present the first exploration of the impact of impersonation in GitHub. Specifically, we conduct structured interviews with 17 real-world OSS contributors about their perception of impersonation and corresponding mitigations. Our study reveals that, in general, GitHub users lack awareness of impersonation and underestimate the severity of its implications. After witnessing the impersonation, they show significant concern for the OSS community. Meanwhile, we also demonstrate that the current best practices (i.e., commit signing) that might mitigate impersonation must be improved to increase widespread acceptance and adoption. We also present and discuss participant perceptions of potential ways to mitigate GitHub impersonation. We collect a dataset comprising 12.5 million commits to investigate the current status of impersonation. Interestingly, we also find out that impersonation is not currently detected. We observe that existing commit histories treat impersonation behavior identically to pull request events, resulting in a lack of detection methods for impersonation.
