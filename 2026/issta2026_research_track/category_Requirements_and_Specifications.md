# ISSTA 2026 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 2

## 1. COEUR : COhesion and Exhaustiveness of User stories Representations

**Authors:** Marius Ortega (De Vinci Higher Education and Onepoint), Hassan Imhah (Onepoint), Nédra Mellouli (De Vinci Higher Education), Christophe Rodrigues (De Vinci Higher Education), Nicolas Travers (De Vinci Higher Education)

**Categories:** Requirements and Specifications

**中文总结:** COEUR 提出 Cohesion 与 Exhaustiveness 两项可自动计算的用户故事质量指标，分别评估 backlog 结构组织与需求—方案语义对齐。噪声实验与 LLM 生成场景验证表明其优于 INVEST、QUS 等传统指标集。

**Abstract:** User Stories are key artifacts in Requirement and Software Engineering. Despite their wide adoption, their writing in industrial contexts tends to diverge from the principles initially stated in Agile methodologies. In this context, sets of metrics such as INVEST or QUS emerged to qualify these items. In this paper, we argue that the said sets of metrics are only partially efficient at capturing the quality of user stories contextualized in a project, and that their actual adoption in business contexts is limited due to multiple aspects: their unfitness to specific contexts, the difficulty of implementation requiring human intervention, the absence of reproducibility or their misalignment with actual quality of user stories. Such limitations, prevent practitioners from efficiently applying them for downstream tasks such as LLM-based user story generation. To address these challenges, we introduce COEUR , a framework comprising two metrics: Cohesion and Exhaustiveness . These metrics are designed to mirror core Product Owner responsibilities. Specifically, Cohesion evaluates the structural organization and logical grouping of the backlog, while Exhaustiveness monitors the semantic alignment between the elicited needs and the proposed technical solutions. Aditionnaly, they are quantitative, reproducible, and automatically computable. To evaluate COEUR , we conduct four empirical experiments organized into two validation tracks. The first track utilizes two noising-based experiments to assess our metrics sensitivity to requirement degradation. The second track evaluates their performance in generative contexts through two standard learning paradigms for LLM: In-Context Learning (ICL) and Supervised Fine-Tuning (SFT), both applied to our user story generation task. Subsequently, COEUR provides a turnkey measurement of Product Backlog’s quality for both project monitoring by human experts and LLM benchmarking applied to automatic user stories generation.


## 2. On the Role of Large Language Models in Robustness-Guided Requirement Falsification

**Authors:** Ali Kaya (Åbo Akademi University), Ivan Porres (Åbo Akademi University)

**Categories:** Requirements and Specifications

**中文总结:** 在鲁棒性引导的需求证伪框架中引入 LLM 顾问式候选输入生成器，配合准入门控确保输入合法。GPT-P 在 ARCH-COMP 19 条需求中 16 条完美证伪、19 条均至少一次证伪，表现因上下文线索类别而异。

**Abstract:** Robustness-guided falsification supports the validation of cyber-physical systems by searching for system traces that violate formal temporal requirements. Existing falsification methods typically treat candidate generation as numerical search over an input  space, guided by quantitative robustness feedback. This paper studies a different mechanism: a guarded advisory proposer that uses a Large Language Model to generate candidate inputs. The LLM-based proposer suggests candidates inputs using the following information: the requirement to validate, the interface of the system under test, and previously evaluated robustness history.  Admission gates ensure that only valid candidate inputs are  considered for execution. We evaluate this approach on 19  falsification requirements from the ARCH-COMP 2024 CPS benchmark and on five synthetic problems. The results show that LLM-based proposing is sensitive to model choice and context representation. Among the tested variants, GPT-P, which uses a GPT model with the plain context representation, is the most reliable representative variant. On ARCH-COMP, GPT-P reaches perfect falsification on 16 of 19 requirements, obtains at least one falsification on all 19 requirements, and, on 8 requirements, uses the fewest executions among the reported tools that also achieve perfect falsification. However, its performance is heterogeneous. We explain this behavior through three classes of falsification problems: informative context cues, ambiguous context cues with strong robustness gradient, and ambiguous context cues with weak robustness gradient. Synthetic benchmark problems reproduce these classes under controlled mechanisms. Overall, GPT-P performs best on the informative-context-cue class, where the requirement and SUT interface expose useful candidate hypotheses that the LLM can exploit before extensive robustness-feedback search is needed. To our knowledge, this use of semantic context cues for candidate input proposal is not supported by existing robustness-guided falsification methods.

