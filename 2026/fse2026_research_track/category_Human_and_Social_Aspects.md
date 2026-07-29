# FSE 2026 Research Track — Human and Social Aspects

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 7 papers

## 1. Building Software by Rolling the Dice: A Qualitative Study of Vibe Coding

**Authors:** Yi-Hung Chou (University of California, Irvine), Boyuan Jiang (University of California, Irvine), Yiwen Chen (Independent), Mingyue Weng (Marketing Creative Associate), Victoria Jackson (University of Southampton), Thomas Zimmermann (University of California, Irvine), James Jones (University of California at Irvine)

**Categories:** Human and Social Aspects

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797105

**中文总结:** 对 20 个 vibe coding 视频（含约 16 小时直播会话、254 条提示）开展扎根理论研究，刻画从几乎不检查到审查改编 AI 代码的行为光谱，以及将调试/精炼视为「掷骰子」的随机性应对；指出不同心智模型影响提示策略、评估与信任，并为工具与教育提供启示。

**Abstract:** Large language models (LLMs) are reshaping software engineering by enabling vibe coding—building software primarily through prompts rather than writing code. Although widely publicized as a productivity breakthrough, little is known about how practitioners actually define and engage in these practices. To shed some light on this emerging phenomenon, we conducted a grounded theory study of 20 vibe-coding videos, including 7 live-streamed coding sessions (~16 hours, 254 prompts) and 13 opinion videos (~5 hours), supported by additional analysis of activity durations and intents of prompts. Our findings reveal a spectrum of behaviors: some vibe coders rely almost entirely on AI without inspecting code, while others examine and adapt generated outputs. Across approaches, all must contend with the stochastic nature of code generation, with debugging and refinement described as “rolling the dice.” Further, divergent mental models, shaped by developers’ expertise and engagement with AI, influence prompting strategies, evaluation practices, and levels of trust. These findings open new directions for research on the future of software engineering and point to practical opportunities for tool design and education.

## 2. How Do Developers Interact with AI? An Exploratory Study on Modeling Developer Programming Behavior

**Authors:** Yinan Wu (North Carolina State University), Ze Shi (Zane) Li (University of Oklahoma), Kathryn Stolee (North Carolina State University), Bowen Xu (North Carolina State University)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808120

**中文总结:** 对 76 名开发者开展混合方法研究，提出 S-IASE 模型从意图、动作、工具与情感刻画 AI 辅助编程行为；发现 AI 组更侧重生成与验证且情绪更稳定，并揭示依赖 AI 时的冒名者心态等细微体验。

**Abstract:** Artificial Intelligence (AI) is reshaping how developers adopt software engineering practices, yet the multi-dimensional nature of developer-AI interaction remains under-explored. Prior studies have primarily examined dimensions observable from developer activities such as “Prompt Crafting” and “Code Editing,” overlooking how hidden intentions and emotional dimensions intertwine with concrete actions during AI-assisted programming. Understanding the interplay is essential for improving developer experience and future AI assistant designs. To understand this phenomenon, we conducted a mixed-methods study with 76 developers. We first split developers into AI-assisted and non-AI groups. Each performed a programming task (either Python with API management or Java with SQL). Developers retrospectively labeled their self-reported intentions, tool-supported actions, and emotions (on a 7-point valence scale) from screen recordings, supplemented by participant surveys and interviews. Our user study resulted in a novel model, named S-IASE, with four dimensions to describe programming behavior for a given development state: intention, action, supporting tool, and emotion. Our analysis reveals several aggregated and sequential behavioral patterns. For example, for aggregated patterns, using AI assistants often led developers to focus more on actively “creating” code, evaluating, and verifying the generated results; for sequential patterns, AI-assisted participants showed emotionally stable development flows, as opposed to non-AI-assisted participants who experienced more fluctuating emotions. Interviews revealed further nuance: some developers reported impostor-like feelings, expressing guilt or self-doubt about relying on AI for programming. The uncovered patterns indicate that our model can provide actionable insights for improving AI assistants’ responsiveness, training developers in AI collaboration, and designing developer-centric AI studies. Our work bridges an important gap in understanding the complexities of developer-AI interaction in the programming context and sheds light on future developer-centric research directions.

## 3. Mitigating the Risk of Defects and Improving Knowledge Distribution with Code Reviewer Recommenders

**Authors:** Mohammadali Sefidi Esfahani (Concordia University), Peter Rigby (Concordia University; Meta)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797070

**中文总结:** 引入考虑整支评审团队知识的 CCSR 指标更准确评估评审推荐对引入缺陷风险的影响，并提出 AddExpertRec(Dt) 为高风险 PR 追加专家评审；仿真显示其可提升缺陷发现效果，同时平衡负载与知识传播。

**Abstract:** Defects are inevitable in software projects, leading to increased maintenance costs, user dissatisfaction, and a diminished software reputation. Code review is one of the most critical software quality assurance activities that reduces software defects and improves software quality. Prior works have quantified the impact of reviewer recommenders on the risk of inducing new defects based on the highest level of expertise among the developers in the reviewer team. However, our analysis shows that prior work overestimates the safety of a change and ignores the defect-finding effectiveness of the diverse knowledge of reviewers. In this study, we incorporate the knowledge of the entire reviewer team into the author’s level of expertise and introduce the novel Contribution-aware Changeset Safety Ratio (CCSR) outcome to assess the impact of code reviewer recommenders on the risk of inducing defects more accurately.

When a pull request is risky, a natural mitigation is to add an expert reviewer. We are unaware of any works that have quantified the impact of adding a reviewer to risky PRs. We propose the novel AddExpertRec(D t ) strategy that recommends an additional expert reviewer for defect-prone pull requests to reduce the likelihood of introducing new defects when the risk is above the threshold D t . The simulation results show that AddExpertRec(D t ) can enhance the defect finding effectiveness of existing recommenders while still balancing reviewer workload and spreading knowledge to reduce the impact of turnover. Ultimately, our results give managers the ability to select a recommender strategy that best suits their project needs based on their resource constraints. The scripts and data are available in our replication package.

## 4. Multi-LLM Persona Generation for Virtual Focus Groups in Software Engineering: A Controlled, Multi-Domain Study of Emotional Requirements Elicitation

**Authors:** Guangrui Fan (Taiyuan University of Science and Technology), Dandan Liu (Universiti Malaya), Lihu Pan (Taiyuan University of Science and Technology), Rui Zhang (Taiyuan University of Science and Technology), Qian Guo (Taiyuan University of Science and Technology)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808098

**中文总结:** 在多领域对照实验中评估多 LLM 虚拟焦点小组抽取情感需求，发现异质多模型配置相对单模型提升经盲测验证的 AI-only 需求约 14.7%；与 Emotional Goal Modeling、真人焦点组互补，消融表明约 55% 增益来自模型多样性本身。

**Abstract:** This paper presents a controlled, multi-domain evaluation of using multiple Large Language Models (LLMs) to automate and augment the elicitation of emotional requirements in software engineering. We study an anchor domain (mental-health journaling) alongside personal finance and fitness, and disentangle gains from iterative workflow versus true model plurality by comparing four AI configurations (one-shot vs. iterative; single-, two-, and three-model pipelines) against two human baselines: a standard human focus group and Emotional Goal Modeling (EGM). Outputs are assessed with blind human ratings (relevance, clarity, feasibility, innovation) and group-dynamics coding that includes productive, resolution-oriented conflict and empathy events. Across domains, heterogeneous-provider plurality increases persona dispersion and fosters productive conflict in AI-mediated focus groups, yielding more AI-only requirements that pass blind validation than single-model workflows (pooled C3–C1 uplift: +14.7%). To isolate plurality from provider capability, we add two same-model ablation controls in the anchor domain: (i) C1-MV (same-model multi-voice) and (ii) C3-SM (same-model three-step). In a small-sample evaluation (two seeds each), the resulting difference-in-differences on validated share indicating that a substantial portion (~55%) of the C3 uplift persists net of provider heterogeneity. EGM consistently improves clarity and feasibility through explicit goal tracing, while human groups contribute authenticity and language fit; together they form a complementary, auditable pipeline in which supportive reframing (empathy) and productive disagreement help convert dialog into implementable requirements.

## 5. On the Road to Personalized Code Intelligence: Portraiting and Assisting Developers Based on Their In-IDE Behaviors

**Authors:** Yuhong Liu (Beihang University), YUNHE SU, Zhipeng Peng (Beihang University), Zhiwen Luo (Beihang University), Lin Shi (Beihang University), Zhi Jin (Wuhan University), Li Zhang (Beihang University)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797147

**中文总结:** 提出 IDE 内嵌基础设施 VirtualME，从日志行为聚合任务级行为并刻画四维开发者画像，再注入 CoT agent 做个性化仓库知识问答；在真实轨迹基准上相对通用基线五维平均提升 33.80%。

**Abstract:** With the advent of powerful large language models (LLMs), research in automated software engineering has increasingly focused on leveraging these models to achieve a deeper semantic understanding of code or to engineer sophisticated agent-based processes. The predominant goal of these efforts is to enhance developer productivity through automated assistance. However, this research trajectory has largely overlooked a critical factor: the developers themselves. Programming is a deeply human and individualized activity; developers exhibit significant variation in their coding styles, tool-chain preferences, domain-specific expertise, and problem-solving strategies. Consequently, the current paradigm of one-size-fits-all code intelligence systems struggles to accommodate the unique characteristics and needs of individual developers. To address this gap, we introduce VirtualME, a novel IDE-embedded data infrastructure designed to model the developer by continuously capturing and interpreting their dynamic programming behaviors and preferences. VirtualME contains three components. (1) Log-level Behavior Extraction: it captures and extracts developers’ log-level behaviors (edits, navigations, etc.) from IDE. (2) Task-level Behavior Recognition: it aggregates log-level behaviors into task-level behaviors (“skimming API docs”, “iterative debugging”, etc.) via a multi-agent pipeline. (3) Developer-personality Measurement: it builds a rule engine to distill a four-dimensional developer persona: technology stack, ability, behavioral habits, and learning style. On top of VirtualME, we propose a solution for personalized repository-level knowledge Q&A by integrating the developer persona into a Chain-of-Thought (CoT) guided agent. We evaluated VirtualME by building a multi-repository benchmark with real-world developer trajectories, balancing correctness and personalization. Experimental results show that VirtualME-enhanced answers outperform generic baselines on five dimensions: correctness, cognitive-level fit, technology-stack relevance, behavioral-pattern alignment, and stylistic preference, yielding an average 33.80% improvement. Our results demonstrate that abundant, continuous developer-behavior data can unlockPersonalized Code Intelligence. By integrating this personalized understanding into the code intelligence loop, our approach paves the new way for adaptive and personalized code intelligence.

## 6. The Interaction of Complexity and Provenance in Code Review Decisions: Evidence from a Controlled Experiment

**Authors:** Neha Singh (University of Zurich), Francesco Sovrano (USI Lugano, Switzerland), Vincent Hellendoorn (Google DeepMind, USA), Alberto Bacchelli (IfI, University of Zurich)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808165

**中文总结:** 通过 385 人被试的组间实验研究代码复杂度与修订来源标签（人类 vs AI）对评审合规决策的影响；发现高复杂度显著增加对错误修订的过度接受，且在高复杂度下 AI 标签会进一步加剧该效应。

**Abstract:** Modern code review platforms increasingly embed suggested code revisions, including those generated by AI. While such features promise efficiency, they may also change how developers evaluate changes, particularly when code is complex or when suggestions are labeled by source. Prior studies have examined trust and automation bias in software engineering, but it remains unclear how code complexity and perceived authorship (human vs. AI) jointly shape developers’ review decisions. We present the results of a between-subjects experiment with 385 participants, who were asked to review a code revision. The study controlled for code complexity (low vs. high), provenance labels (human vs. AI), and revision correctness. We analyzed developers’ review decisions through compliance patterns: acceptance of correct or rejection of incorrect code revisions (appropriate-compliance), acceptance of incorrect code revisions (over-compliance), and rejection of correct code revisions (under-compliance). Our findings show that higher code complexity significantly (p<.05) increases over-compliance. While provenance alone had no main effect, its influence emerged in interaction: under high-complexity conditions, reviewers were substantially more likely to accept incorrect revisions labeled as AI-authored. This work contributes: (i) empirical evidence that higher code complexity increases the likelihood of accepting incorrect suggestions, (ii) analysis of provenance showing no main effect on overall acceptance but a trend toward higher over-compliance under AI labels, and (iii) evidence of a significant interaction where complex, AI-labeled revisions led to more frequent acceptance of incorrect suggestions—an effect absent under human labels. Together, these results highlight the need for review systems that surface complexity cues and promote more accurate evaluation of AI-labeled suggestions.

## 7. ToxiShield: Promoting Inclusive Developer Communication through Real-Time Toxicity Filtering

**Authors:** Md Awsaf Alam Anindya (Bangladesh University of Engineering and Technology), Showvik Biswas (Bangladesh University of Engineering and Technology), Anindya Iqbal (Bangladesh University of Engineering and Technology Dhaka, Bangladesh), Jaydeb Sarker (University of Nebraska at Omaha), Amiangshu Bosu (Wayne State University)

**Categories:** Human and Social Aspects

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808130

**中文总结:** 提出 ToxiShield，一款面向 GitHub PR 的浏览器扩展，集成毒性检测、细粒度分类解释与建设性改写三模块；BERT 检测准确率达 98%，人工评估验证其可用性，助力代码审查中的包容性沟通。

**Abstract:** Toxic interactions during code reviews can undermine teamwork and hinder productivity in software engineering (SE) teams. While prior studies explore toxicity detection and empirical investigation, they lack real-time detoxification tools to support the SE community. To address this gap, we present ToxiShield, a browser extension for GitHub pull requests that is built using three modules: i) Toxicity Filter – to identify whether a text is toxic, ii) Communication coach – to facilitate just-in-time fine-grained toxicity categorization with explanations, and iii) The Reframer – that generates a revised, constructive alternative of a toxic text. For each module, we trained and evaluated multiple deep learning and Large Language Models (LLMs) to identify the best choice. A BERT-based binary detection model, trained on 38,761 code review samples, achieves 98% accuracy and an F1-score of 97% and is the selected one for the Toxicity Filter module. For the Communication Coach, prompt-tuned Claude 3.5 Sonnet achieved the best performance with 39% MCC and 42% F1  in multiclass toxicity classification with detailed reasoning. For Reframer, we evaluated five LLMs using a fine-tuning strategy on a dataset of 10,120 code review comments. The fine-tuned Llama 3.2 model achieves 95.27% style transfer accuracy, 97.03% fluency, 67.07% content preservation, and an 84% J-score. We further validated ToxiShield through a human evaluation using the Technology Acceptance Model with 10 participants, confirming its perceived usefulness and ease of adoption. ToxiShield sets a benchmark for advancing constructive communication in software engineering, driving inclusivity and healthier collaboration in open-source communities.
