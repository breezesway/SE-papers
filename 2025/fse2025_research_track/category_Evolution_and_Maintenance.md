# FSE 2025 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 2 papers

## 1. An Empirical Study on Release-Wise Refactoring Patterns

**Authors:** Shayan Noei (Queen's University), Heng Li (Polytechnique Montréal), Ying Zou (Queen's University, Kingston, Ontario)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715734

**中文总结:** 对 207 个开源 Java 项目归纳四类 release-wise 重构模式，发现晚期活跃模式代码质量最佳，成熟项目更倾向稳态活跃；开发者常固守单一模式，晚期活跃可安全复用。

**Abstract:** Refactoring is a technical approach to increase the internal quality of software without altering its external functionalities. Developers often invest significant effort in refactoring. With the increased adoption of continuous integration and development (CI/CD), refactoring activities may vary within and across different releases and be influenced by various release goals. For example, practitioners may consistently allocate refactoring activities throughout a release, or prioritize new features early on in a release and only pick up refactoring late in a release. Different approaches to allocating refactoring tasks may have different implications for code quality. However, there is a lack of existing work to understand how practitioners distribute their refactoring activities in a release and their impact. Therefore, we first empirically study the frequent release-wise refactoring patterns in 207 open-source Java projects and their characteristics. Then, we analyze how these patterns and their transitions affect code quality. We identify four major release-wise refactoring patterns: early active, late active, steady active, and steady inactive. We find that adopting the late active pattern—characterized by gradually increasing refactoring activities as the release approaches—leads to the best code quality. We observe that as projects mature, refactoring becomes more active, reflected in the increasing use of the steady active release-wise refactoring pattern and the decreasing utilization of the steady inactive release-wise refactoring pattern. While the steady active pattern shows improvement in quality-related code metrics (e.g., cohesion), it can also lead to more architectural problems. Additionally, we observe that developers tend to adhere to a single refactoring pattern rather than switching between different patterns. The late active pattern, in particular, can be a safe release-wise refactoring pattern that is used repeatedly. Our results can help practitioners understand existing release-wise refactoring patterns and their effects on code quality, enabling them to utilize the most effective pattern to enhance release quality.

## 2. Automatically fixing dependency breaking changes

**Authors:** Lukas Fruntke (University College London), Jens Krinke (University College London)

**Categories:** Evolution and Maintenance

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729366

**中文总结:** 比较 Agent 式工具调用与递归 zero-shot 提示两种 LLM 方法，在 BUMP 数据集上自动修复 Java 依赖破坏性变更；Agent 最高约 23%、zero-shot 约 19% 测试通过，表明该修复可行且可优化。

**Abstract:** Breaking changes in dependencies are a common challenge in software development, requiring manual intervention to resolve. This study examines how well Large Language Models (LLMs) automate the repair of breaking changes caused by dependency updates in Java projects. Although earlier methods have mostly concentrated on detecting breaking changes or investigating their impact, they have not been able to completely automate the repair process. We introduce and compare two new approaches: an agentic system that combines automated tool usage with LLMs, and a recursive zero-shot approach, employing iterative prompt refinement. Our experimental framework assesses the repair success of both approaches, using the BUMP dataset of curated breaking changes. We also investigate the impact of variables such as dependency popularity and prompt configuration on repair outcomes. Our results demonstrate a substantial difference in test suite success rates, with the agentic approach achieving a repair success rate of up to 23%, while the zero-shot prompting approach achieved a repair success rate of up to 19%. We show that automated program repair of breaking dependencies with LLMs is feasible and can be optimised to achieve better repair outcomes.
