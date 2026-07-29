# ISSTA 2026 Research Track — Human and Social Aspects

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 3

## 1. Evaluating the Impact of Explainable AI on Trust in AI-Assisted Code Review

**Authors:** Zhenhan Gao (Technical University of Munich), Marvin Muñoz Barón, Umm-e Habiba (Technical University Munich), Daniel Graziotin (University of Hohenheim), Stefan Wagner (Technical University of Munich)

**Categories:** Human and Social Aspects

**中文总结:** 通过 34 人 within-subjects 用户研究评估 XAI 对 AI 辅助 code review 中开发者信任与采纳的影响；完整解释提升信任但 moderate 解释获最高 AI 一致率（89.22%）。

**Abstract:** Background: The use of large language models (LLMs) for automated code review has brought significant change to a time-consuming part of software engineering. Prior work has shown that LLM-based code tools can improve code quality and enable more robust software development processes. As the tools get more powerful, the explanations behind their decisions remain hard to understand. Developers struggle to assess the validity of LLM-generated code reviews, making it difficult to gauge how much trust they should place in them. While the application of automated code review with LLMs has been extensively researched, the inclusion of Explainable AI (XAI) for transparency in code reviews and its impact on trust are yet to be explored. Objective: We aim to address this research gap by collecting empirical evidence on the influence of XAI on the trust of software developers in AI-assisted code reviews. Method: We conducted a within-subjects user study with 34 participants from diverse programming backgrounds, comparing three experimental LLM-based automated code review systems with varying levels of XAI support: Condition A (detailed explanation and review feedback), Condition B (review feedback only), and Condition C (no explanations). Participants were shown a series of real-world code change requests along with the AI-generated code reviews. During the study, we measured trust perceptions for each system using a questionnaire, agreement with the AI recommendation, the reasoning for accepting or rejecting the code change, and the time taken to review the code change. Results: Our quantitative results show that the level of explanation significantly influences both the level of trust of software developers and their agreement with AI recommendations, but in different ways. Full explanations (Condition A) yield the highest perceived trust (M = 3.99/5) but not the highest agreement with AI recommendations, whereas moderate explanations (Condition B) achieve the highest AI agreement (89.22%). This could suggest that more explanations prompt developers to question AI recommendations more frequently. In contrast, providing no explanations (Condition C) results in the lowest levels of trust and agreement. We also find that the level of explanation did not significantly impact the time taken to accept or reject a code change. Across all conditions, the most commonly cited reasons for code change decisions were changes in code readability and the correctness of the implementation. Conclusion: Overall, these findings indicate that incorporating XAI into the code review process significantly changes the trust perceptions and agreement with AI recommendations for software developers. These results provide insights for the design and evaluation of trustworthy AI-based code review systems, and support researchers in the design of studies on the human factors of AI-assisted software development.


## 2. The Discreet Charm of the Bugeoisie: A First Look at Bug Reports Created by Researchers

**Authors:** Ji young Kim, Jana Dragovic (University of Illinois Urbana-Champaign), Alessandro Botta (University of Texas at Dallas), T. M. Rithwanul Islam (Jahangirnagar University), Alaa Mohamad (American University of Beirut), Karim Sharaf (The Egyptian E-Learning University-Alexandria University), Sejuti Sharmin Siddiqui, Divyanshi Joshi (Maharaja Agrasen Institute of Technology), Harini Anand (PES University), Nurjemal Saryyeva (National University of Singapore), Shubham Chapagain (Tribhuvan University), Saad Nasir (American International University-Bangladesh), Darko Marinov (University of Illinois at Urbana-Champaign), Bogdan Alexandru Stoica

**Categories:** Human and Social Aspects

**中文总结:** 首次系统研究 ISSTA 2025 论文中研究者提交的 bug 报告（Bugeoisie），分析其创建时间、解决状态及论文声称的可验证性。发现独立核查 bug 数量极为困难，呼吁会议与作者改进 artifact 披露规范。

**Abstract:** Many ISSTA papers present automated tools to find bugs in software, including in open-source projects. Some researchers create public bug reports for the bugs they deem worth reporting, e.g., new bugs found by the tools. We focus on studying bug reports created by researchers and coin the term Bugeoisie to refer to such bug reports. We collect the Bugeoisie for ISSTA 2025 by reading the papers, examining the artifacts, and contacting the authors, while trying to “chase” bug report links. This process turns out to be surprisingly challenging because only a few authors make such links readily available. We then analyze the Bugeoisie to understand when the bug reports were created and how they were resolved up until now. For most papers that make claims about the number of bugs found, reported, or confirmed, independently checking those claims is again surprisingly challenging. Our findings point out to the important changes that conference organizers and reviewers may want to require for the Bugeoisie. We also provide some suggestions for paper authors to prepare and describe their Bugeoisie in their papers and artifacts.


## 3. Unpacking AI Agent Participation in Issue-Centered Collaboration in Open-Source Software Development

**Authors:** Kaiwen Zhi (East China University of Science and Technology), Guisheng Fan (East China University of Science and Technology, Shanghai Engineering Research Center of Smart Energy), Wentao Chen (East China University of Science and Technology)

**Categories:** Human and Social Aspects

**中文总结:** 基于 83 个 GitHub 仓库 issue 事件数据，用动态 issue 熵区分 agent 与人类协作复杂度。发现 agent 相关协作复杂度与开发产出关联更强且引入缺陷更少，但与 issue 解决效率的关系高度依赖上下文。

**Abstract:** The increasing participation of AI agents in open-source software development raises questions about their role in collaborative processes. This paper investigates how AI agent participation relates to the structure and outcomes of issue-centered collaboration in open-source software projects. We adopt a process-level perspective by modeling issue handling as sequences of events and extending dynamic issue entropy to distinguish between agent-related and non-agent-related contributions. Using large-scale issue event data from 83 GitHub repositories, we construct a project–month panel dataset and analyze associations between collaboration complexity and development outcomes. Our results show that agent-related collaboration complexity is more strongly associated with development output than human-only collaboration complexity, and is associated with fewer newly introduced defects. In contrast, its relationship with issue resolution efficiency is highly context-dependent. These findings highlight the importance of considering collaboration structure when evaluating the impact of AI agents in open-source software development.

