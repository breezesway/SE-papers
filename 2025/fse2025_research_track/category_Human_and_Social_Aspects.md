# FSE 2025 Research Track — Human and Social Aspects

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 7 papers

## 1. 10 years later: revisiting how developers search for code

**Authors:** Kathryn Stolee (North Carolina State University), Tobias Welp (Google), Caitlin Sadowski, Sebastian Elbaum (University of Virginia)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715774

**中文总结:** 复现并扩展 2015 年代码搜索研究，对 1200+ 开发者调查并统计 10 万+ 工具用户行为；发现尽管有 AI 辅助，搜索频率未降，示例查找减少、探索与理解代码增多，并引入成功标准评估需求满足情况。

**Abstract:** Code search is an integral part of a developer’s workflow. In 2015, researchers published a paper reflecting on the code search practices of 27 developers. That paper had first-hand accounts for why those developers were using code search, and highlighted how often and in what situations developers were searching for code. In the past decade, much has changed in the landscape of developer support. New languages have emerged, AI for code generation has gained traction, auto-complete in the IDE has gotten better, Q&A forums have increased in popularity, and code repositories are larger than ever. It is worth considering whether those observations from almost a decade ago have stood the test of time. In this work, we replicate and expand on the prior survey with over 1,200 developers, and report code search usage statistics for over 100,000 tool users. Unlike the prior work, in our surveys, we include explicit success criteria to understand when code search is meeting their needs, and when it is not. We dive further into two common sub-categories of code search effort: when developers are looking for examples, and when they are using code search alongside code review. We find that developers continue to use code search frequently, and the frequency has not changed despite the introduction of AI-enhanced development support. Developers continue to use code search to find examples, but the frequency of example-seeking behavior has decreased. More often than before, developers are using code search to learn about and explore code. This has implications for future code search support in software development.

## 2. Automated Extraction and Analysis of Developer’s Rationale in Open Source Software

**Authors:** Mouna Dhaouadi, Bentley Oakes, Michalis Famelis

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729383

**中文总结:** 实例化 Kantara 架构，用预训练模型与 LLM 自动抽取开源项目中的决策与理由并检测推理冲突；在 Linux Kernel OMM-Killer 等六个活跃项目上验证可行，可辅助避免与历史决策冲突。

**Abstract:** Contributors to open-source software must deeply understand a project’s history to make coherent decisions which do not conflict with past reasoning. However, inspecting all related changes to a proposed contribution requires intensive manual effort, and previous research has not yet produced an automated mechanism to expose and analyze these conflicts. In this article, we propose such an automated approach for rationale analyses, based on an instantiation of Kantara, an existing high-level rationale extraction and management architecture. Our implementation leverages pre-trained models and Large Language Models, and includes structure-based mechanisms to detect reasoning conflicts and problems which could cause design erosion in a project over time. We show the feasibility of our extraction and analysis approach using the OMM-Killer module of the Linux Kernel project, and investigate the approach’s generalization to five other highly active open source projects. The results confirm that our automated approach can support rationale analyses with reasonable performance, by finding interesting relationships and to detect potential conflicts and reasoning problems. We also show the effectiveness of the automated extraction of decision and rationale sentences and the prospects for generalizing this to other open source projects. This automated approach could therefore be used by open source software developers to proactively address hidden issues and to ensure that new changes do not conflict with past decisions.

## 3. How Do Programming Students Use Generative AI?

**Authors:** Christian Rahe (University of Hamburg), Walid Maalej (University of Hamburg)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715762

**中文总结:** 对 37 名编程学生在受控环境下使用 ChatGPT 完成代码理解与改进练习进行观察。多数使用者最终会要求生成完整答案，并常陷入“提交错误生成代码→再求修复”的循环，支持对过度依赖生成式 AI 削弱能动性的担忧。

**Abstract:** Programming students have a widespread access to powerful Generative AI tools like ChatGPT. While this can help understand the learning material and assist with exercises, educators are voicing more and more concerns about an over-reliance on generated outputs and lack of critical thinking skills. It is thus important to understand how students actually use generative AI and what impact this could have on their learning behavior. To this end, we conducted a study including an exploratory experiment with 37 programming students, giving them monitored access to ChatGPT while solving a code understanding and improving exercise. While only 23 of the students actually opted to use the chatbot, the majority of those eventually prompted it to simply generate a full solution. We observed two prevalent usage strategies: to seek knowledge about general concepts and to directly generate solutions. Instead of using the bot to comprehend the code and their own mistakes, students often got trapped in a vicious cycle of submitting wrong generated code and then asking the bot for a fix. Those who self-reported using generative AI regularly were more likely to prompt the bot to generate a solution. Our findings indicate that concerns about potential decrease in programmers’ agency and productivity with Generative AI are justified. We discuss how researchers and educators can respond to the potential risk of students uncritically over-relying on generative AI. We also discuss potential modifications to our study design for large-scale replications.

## 4. Prompts Are Programs Too! Understanding How Developers Build Software Containing Prompts

**Authors:** Jenny T. Liang (Carnegie Mellon University), Melissa Lin (Carnegie Mellon University), Nikitha Rao (Carnegie Mellon University), Brad A. Myers (Carnegie Mellon University)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729342

**中文总结:** 基于对 20 名开发者的扎根理论访谈，本文将部分 prompt 视为程序并提出 prompt programming 概念，归纳 14 条观察。与传统编程不同，开发者构建的是 FM 行为心智模型且难以稳定形成，提示需专门工具与工程实践支持。

**Abstract:** The introduction of generative pre-trained models, like GPT-4, has introduced a phenomenon known as prompt engineering, whereby model users repeatedly write and revise prompts while trying to achieve a task. Using these AI models for intelligent features in software applications require using APIs that are controlled through developer-written prompts. These prompts have powered AI experiences in popular software products, potentially reaching millions of users. Despite the growing impact of prompt-powered software, little is known about its development process and its relationship to programming. In this work, we argue that some forms of prompts are programs, and that the development of prompts is a distinct phenomenon in programming. We refer to this phenomenon prompt programming. To this end, we develop an understanding of prompt programming using Straussian grounded theory through interviews with 20 developers engaged in prompt development across a variety of contexts, models, domains, and prompt complexities. Through this study, we contribute 14 observations about prompt programming. For example, rather than building mental models of code, prompt programmers develop mental models of the FM’s behavior on the prompt and its unique qualities by interacting with the model. While prior research has shown that experts have well-formed mental models, we find that prompt programmers who have written dozens of prompts still struggle to develop reliable mental models, causing a rapid and unsystematic development process. Taken together, our observations indicate that prompt programming is significantly different from traditional software development, motivating the creation of tools to support prompt programming. Our findings have implications for software engineering practitioners, educators, and researchers.

## 5. Revolutionizing Newcomers' Onboarding Process in OSS Communities: The Future AI Mentor

**Authors:** Xin Tan (Beihang University), Xiao Long, Yinghao Zhu (Beihang University), Lin Shi (Beihang University), Xiaoli Lian (Beihang University, China), Li Zhang (Beihang University)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715767

**中文总结:** 通过与 19 名 OSS 新人的 Design Fiction，提炼 32 条 AI mentor 设计策略，并原型 OSSerCopilot 获积极可用性反馈。文献综述显示“发现感兴趣项目”等高期望能力现有研究仍薄弱，为新人入职辅导工具指明方向。

**Abstract:** Onboarding newcomers is vital for the sustainability of open-source software (OSS) projects. To lower barriers and increase engagement, OSS projects have dedicated experts who provide guidance for newcomers. However, timely responses are often hindered by experts’ busy schedules. The recent rapid advancements of AI in software engineering have brought opportunities to leverage AI as a substitute for expert mentoring. However, the potential role of AI as a comprehensive mentor throughout the entire onboarding process remains unexplored. To identify design strategies of this “AI mentor,” we applied Design Fiction as a participatory method with 19 OSS newcomers. We investigated their current onboarding experience and elicited 32 design strategies for future AI mentor. Participants envisioned AI mentor being integrated into OSS platforms like GitHub, where it could offer assistance to newcomers, such as “recommending projects based on personalized requirements” and “assessing and categorizing project issues by difficulty.” We also collected participants’ perceptions of a prototype, named “OSSerCopilot,” that implemented the envisioned strategies. They found the interface useful and user-friendly, showing a willingness to use it in the future, which suggests the design strategies are effective. Finally, in order to identify the gaps between our design strategies and current research, we conducted a comprehensive literature review, evaluating the extent of existing research support for this concept. We find that research is relatively scarce in certain areas where newcomers highly anticipate AI mentor assistance, such as “discovering an interested project.” Our study has the potential to revolutionize the current newcomer-expert mentorship and provides valuable insights for researchers and tool designers aiming to develop and enhance AI mentor systems.

## 6. The Landscape of Toxicity: An Empirical Investigation of Toxicity on GitHub

**Authors:** Jaydeb Sarker (University of Nebraska at Omaha), Asif Kamal Turzo (Wayne State University), Amiangshu Bosu (Wayne State University)

**Categories:** Human and Social Aspects

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715744

**中文总结:** 对 2,828 个分层抽样的 GitHub OSS 项目做毒性大规模混合方法研究，发现脏话最常见，其次为钓鱼与侮辱；热度与毒性正相关、问题解决率负相关，企业赞助项目更少毒、游戏项目毒性约高七倍，且历史发毒者更易再犯并成为攻击目标。

**Abstract:** Toxicity on GitHub can severely impact Open Source Software (OSS) development communities. To mitigate such behavior, a better understanding of its nature and how various measurable characteristics of project contexts and participants are associated with its prevalence is necessary. To achieve this goal, we conducted a large-scale mixed-method empirical study of 2,828 GitHub-based OSS projects randomly selected based on a stratified sampling strategy. Using ToxiCR, an SE domain-specific toxicity detector, we automatically classified each comment as toxic or non-toxic. Additionally, we manually analyzed a random sample of 600 comments to validate ToxiCR’s performance and gain insights into the nature of toxicity within our dataset. The results of our study suggest that profanity is the most frequent toxicity on GitHub, followed by trolling and insults. While a project’s popularity is positively associated with the prevalence of toxicity, its issue resolution rate has the opposite association. Corporate-sponsored projects are less toxic, but gaming projects are seven times more toxic than non-gaming ones. OSS contributors who have authored toxic comments in the past are significantly more likely to repeat such behavior. Moreover, such individuals are more likely to become targets of toxic texts.

## 7. Towards Understanding Fine-Grained Programming Mistakes and Fixing Patterns in Data Science

**Authors:** Weihao Chen (Purdue University), Jia Lin Cheoh (Purdue University), Manthan Keim (Purdue University), Sabine Brunswicker (Purdue University), Tianyi Zhang (Purdue University)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729352

**中文总结:** 基于竞赛中 67 人六周内 390 个 Jupyter Notebook 的细粒度日志，结合 10 名数据科学程序员访谈，刻画此前未充分报告的细粒度编程错误与修复模式。为面向数据科学编程的工具支持提出新机会。

**Abstract:** Programming is an essential activity in data science (DS). Compared with conventional programmers, DS programmers often use different environments (e.g., Jupyter Notebook, R Markdown) instead of traditional IDEs. Thus, it’s crucial to understand what kinds of mistakes they make and how they debug and fix these errors. In order to provide effective tool support to improve their productivity, previous studies have analyzed DS code from public code-sharing platforms such as GitHub and Kaggle. However, they only accounted for code changes committed to the version history, omitting many programming mistakes that are resolved before code commits. To bridge the gap, we present an in-depth analysis of the fine-grained logs of a DS competition, which includes 390 Jupyter Notebooks written by 67 participants over six weeks. In addition, we conducted semi-structured interviews with 10 DS programmers from different domains to understand the reasons behind their programming mistakes. In this work, we identified several unique programming mistakes and fix patterns that were not reported before, highlighting several future opportunities for designing new tool support for DS programming.
