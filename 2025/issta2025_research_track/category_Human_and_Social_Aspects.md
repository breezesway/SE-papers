# ISSTA 2025 Research Track — Human and Social Aspects

Source: https://conf.researchr.org/track/issta-2025/issta-2025-papers#event-overview

Count: 2

## 1. Fixing Outside the Box: Uncovering Tactics for Open-Source Security Issue Management

**Authors:** Lyuye Zhang (Nanyang Technological University), Wu Jiahui, Chengwei Liu (Nanyang Technological University), Kaixuan Li (Nanyang Technological University), Xiaoyu Sun (Australian National University, Australia), Lida Zhao (Nanyang Technological University), Chong Wang (Nanyang Technological University), Yang Liu (Nanyang Technological University)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728977

**中文总结:** 基于 21,187 个 GitHub issue，论文归纳开源漏洞修复的 44 类层次化战术，并评估其有效性与成本。发现 44% 的社区常用策略（如换库、绕过）未被现有工具支持，且 54% 的 CVE 缺少修复建议，而 issue 中 93% 的方案可直接借鉴。

**Abstract:** In the rapidly evolving landscape of software development, addressing security vulnerabilities in open-source software (OSS) has become critically important. However, existing research and tools from both academia and industry mainly relied on limited solutions, such as vulnerable version adjustment and adopting patches, to handle identified vulnerabilities. However, far more flexible and diverse countermeasures have been actively adopted in the open-source communities. A holistic empirical study is needed to explore the prevalence, distribution, preferences, and effectiveness of these diverse strategies.

To this end, in this paper, we conduct a comprehensive study on the taxonomy of vulnerability remediation tactics (RT) in OSS projects and investigate their pros and cons. This study addresses this oversight by conducting a comprehensive empirical analysis of 21,187 issues from GitHub, aiming to understand the range and efficacy of remediation tactics within the OSS community. We developed a hierarchical taxonomy of 44 distinct RT and evaluated their effectiveness and costs. Our findings highlight a significant reliance on community-driven strategies, like using alternative libraries and bypassing vulnerabilities, 44% of which are currently unsupported by cutting-edge tools. Additionally, this research exposes the community’s preferences for certain fixing approaches by analyzing their acceptance and the reasons for rejection. It also underscores a critical gap in modern vulnerability databases, where 54% of CVEs lack fixing suggestions—a gap that can be significantly mitigated by leveraging the 93% of actionable solutions provided through GitHub issues.

## 2. Gamifying Testing in IntelliJ: A Replicability Study

**Authors:** Philipp Straubinger (CQSE GmbH), Tommaso Fulcini (Politecnico di Torino), Giacomo Garaccione (Politecnico di Torino), Luca Ardito (Politecnico di Torino), Gordon Fraser (University of Passau)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728983

**中文总结:** 在 TypeScript 场景下对 IntelliJ 插件 IntelliGame 进行 174 人对照复现实验。使用 gamification 的开发者编写与执行更多测试、工具使用更积极，覆盖率和 mutation score 更高，验证了游戏化能提升测试投入与效果。

**Abstract:** Gamification is an emerging technique to enhance motivation and performance in traditionally unengaging tasks like software testing. Previous studies have indicated that gamified systems have the potential to improve software testing processes by providing testers with achievements and feedback. However, further evidence of these benefits across different environments, programming languages, and participant groups is required. This paper aims to replicate and validate the effects of IntelliGame, a gamification plugin for IntelliJ IDEA to engage developers in writing and executing tests. The objective is to generalize the benefits observed in earlier studies to new contexts, i.e., the TypeScript programming language and a larger participant pool. The replicability study consists of a controlled experiment with 174 participants, divided into two groups: one using IntelliGame and one with no gamification plugin. The study employed a two-group experimental design to compare testing behavior, coverage, mutation scores, and participant feedback between the groups. Data was collected through test metrics and participant surveys, and statistical analysis was performed to determine the statistical significance. Participants using IntelliGame showed higher engagement and productivity in testing practices than the control group, evidenced by the creation of more tests, increased frequency of executions, and enhanced utilization of testing tools. This ultimately led to better code implementations, highlighting the effectiveness of gamification in improving functional outcomes and motivating users in their testing endeavors. The replication study confirms that gamification, through IntelliGame, positively impacts software testing behavior and developer engagement in coding tasks. These findings suggest that integrating game elements into the testing environment can be an effective strategy to improve software testing practices.
