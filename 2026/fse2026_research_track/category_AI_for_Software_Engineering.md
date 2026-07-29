# FSE 2026 Research Track — AI for Software Engineering

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 58 papers

## 1. AdaDec: A Uncertainty-Guided Lookahead Decoding Framework for LLM-based Code Generation

**Authors:** He Kaifeng (SUN YAT-SEN UNIVERSITY), Mingwei Liu (Sun Yat-Sen University), Chong Wang (Nanyang Technological University), Zike Li (Sun Yat-Sen University), Yanlin Wang (Sun Yat-sen University), Xin Peng (Fudan University), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808142

**中文总结:** 提出 AdaDec，在高不确定性解码步对 token 执行 pause-then-rerank 的前瞻重排，并学习模型特定不确定性阈值；在 HumanEval+、MBPP+ 与 DevEval 上相对贪心解码 Pass@1 最高绝对提升 20.9%，并优于 AdapT 等自适应解码方法且更低开销。

**Abstract:** Code generation with large language models (LLMs) is highly sensitive to token selection during decoding, particularly at uncertain decision points that influence program logic. While standard strategies such as greedy decoding treat all tokens uniformly, they overlook code-specific uncertainty patterns, leading to suboptimal performance. This paper presents an empirical study revealing that many generation errors stem from token ranking mistakes at high-uncertainty steps, where the correct token is present but not top-ranked.

Motivated by these findings, we propose AdaDec, a lookahead-based uncertainty-guided adaptive decoding framework that integrates a token-level \textit{pause-then-rerank} mechanism driven by token uncertainty. AdaDec learns model-specific uncertainty thresholds and applies a lookahead-based reranking strategy when uncertainty is high. Experiments on HumanEval+, MBPP+, and DevEval benchmarks show that AdaDec improves Pass@1 accuracy by up to 20.9% in absolute terms over greedy decoding, and consistently outperforms state-of-the-art adaptive decoding methods such as AdapT, while reducing computational cost and latency through efficient, selective pausing. Our results highlight the promise of uncertainty-aware adaptive decoding for improving both the reliability and efficiency of LLM-based code generation.

## 2. Aligning with Human Coding Preferences for Improving Code Generation

**Authors:** Xin Yin (Zhejiang University), Chao Ni (Zhejiang University), Xiaohu Yang (Zhejiang University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808113

**中文总结:** 系统分析 SFT 与 DPO 在不同代码偏好场景下的作用，并提出 Adaptive Preference Optimization（APO）动态放大偏好、抑制非偏好并鼓励探索更优解；在六类代码偏好任务上验证理论假设，APO 持续匹配或超越现有 SFT 与 S&D 策略。

**Abstract:** Large Language Models (LLMs) have demonstrated remarkable potential in automating software development tasks. While recent advances leverage Supervised Fine-Tuning (SFT) and Direct Preference Optimization (DPO) to align models with human preferences, the optimal training strategy remains unclear across diverse code preference scenarios. This paper systematically investigates the roles of SFT and DPO in aligning LLMs with different code preferences. Through both theoretical analysis and empirical observation, we hypothesize that SFT excels in scenarios with objectively verifiable optimal solutions, while applying SFT followed by DPO (S&D) enables models to explore superior solutions in scenarios without objectively verifiable optimal solutions. Based on the analysis and experimental evidence, we propose Adaptive Preference Optimization (APO), a dynamic integration approach that adaptively amplifies preferred responses, suppresses dispreferred ones, and encourages exploration of potentially superior solutions during training. Extensive experiments across six representative code preference tasks validate our theoretical hypotheses and demonstrate that APO consistently matches or surpasses the performance of existing SFT and S&D strategies. Our work provides both theoretical foundations and practical guidance for selecting appropriate training strategies in different code preference alignment scenarios.

## 3. Automated Repair of TEE Partitioning Issues via DSL-Guided and LLM-Assisted Patching

**Authors:** Chengyan Ma (Singapore Management University), Jieke Shi (Singapore Management University), Ruidong Han (Singapore Management University), Ye Liu (Singapore Management University), FENG Li, Yuqing Niu, David Lo (Singapore Management University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808207

**中文总结:** 提出 TEERepair，用 DSL 编码 TEE 安全修复规则为带占位符的补丁模板，再由 LLM 合成上下文感知补丁并生成测试客户端验证；在 PartitioningE-Bench 上精度 95.29%、召回 91.01%，并在 20 个真实 TEE 项目中提交 5 个修复 PR（2 已合并）。

**Abstract:** Trusted Execution Environments (TEEs) provide hardware-based isolation to protect sensitive data and computations from potentially compromised operating systems (OS). However, TEE applications inevitably interact with the untrusted OS through SDK interfaces, and improper partitioning can introduce severe vulnerabilities such as data leakage and code injection. While prior work has proposed static analysis tools to detect such issues, automated repair remains largely unexplored. This problem is particularly challenging due to three TEE-specific factors: the lack of standardized secure development guidelines, the difficulty of extracting semantic information from low-level C code, and the absence of mature testing and validation methods. In this work, we present TEERepair, a framework for automatically repairing bad partitioning issues in TEE applications. Our approach tackles the above challenges by introducing a domain-specific language (DSL) to encode repair rules that express and capture common TEE security patterns, which are instantiated as patch templates with placeholders for context-specific variables. We then leverage large language models (LLMs) to reason about code semantics and synthesize context-aware patches, and further generate test clients to validate the repairs. We evaluate TEERepair on the TEE Partitioning Errors Benchmark (PartitioningE-Bench), achieving an overall precision of 95.29% and recall of 91.01%, with improvements of 37.04% in precision and 51.68% in recall over an LLM-only baseline. Furthermore, applying TEERepair to 20 real-world TEE projects, we submitted 5 repair pull requests, 2 of which have been confirmed and merged by project maintainers.

## 4. Balancing Latency and Accuracy of Code Completion via Local-Cloud Model Cascading

**Authors:** Lu Hanzhen (Zhejiang University), Lishui Fan (Zhejiang University), Jiachi Chen (Zhejiang University), Qiuyuan Chen (Tencent Technology), Zhao Wei (Tencent), Zhongxin Liu (Zhejiang University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797088

**中文总结:** 提出 MCCom，默认用本地小模型、仅在用户行为信号判定补全失败时级联云端大模型，并结合两阶段推测解码与迭代检索；自训 121M 小模型达 7B SOTA 约 73.8% 性能，在 RepoEval/StmtEval 上最高降延迟 47.9%、平均少用 LLM 46.3%，且大模型精确匹配率平均提升 8.9%。

**Abstract:** Line-level code completion aims to complete the current line in real-time as developers type. Low latency is crucial to maintaining a seamless and uninterrupted coding experience, enabling developers to remain in a productive flow. However, existing approaches face a fundamental trade-off: large language models (LLMs) provide high-quality suggestions but require expensive computational resources to ensure acceptable inference latency. In contrast, static-analysis-based methods and small language models respond quickly but often generate suboptimal completions. To fill this gap, our idea is to rely on the small model by default and only escalate the large model when necessary to achieve latency-accuracy trade-offs. Based on this idea, we propose MCCom(Model-Cascading-based code Completion), a framework that cascades a local small model with a high-performance cloud large model for code completion. Realizing effective model cascading requires answering two non-trivial questions, i.e., when to invoke the large model and how to enable effective collaboration between small and large models. For the first question, we leverage a valuable but easily overlooked signal, i.e., user actions, during code completion to accurately identify failed completions. This deferral decision allows us to invoke the large model only when necessary, reducing both latency and cloud-side computation costs. To enable effective collaboration, MCCom employs a two-stage speculative decoding strategy and an iterative retrieval mechanism that collectively accelerate and improve the quality of completions. Due to the lack of high-quality small models for code completion, we also train a lightweight model with only 121M parameters to implement MCCom. The small model achieves an average of 73.8% of the performance of the state-of-the-art 7B model. We evaluate MCCom on the RepoEval benchmark and a new benchmark, StmtEval, collected from real-world projects. Experimental results show that our approach not only reduces inference latency by up to 47.9% and cuts down LLM usage by an average of 46.3%, but also improves the exact match rate of the large model by an average of 8.9%.

## 5. Bash-Commenter: Leveraging Syntax-Aware Preference Optimization to Reinforce Large Language Model for Bash Code Comment Generation

**Authors:** Lei Yu (Institute of Software, Chinese Academy of Sciences, University of Chinese Academy of Sciences, China), Jingyuan Zhang (Institute of Software, Chinese Academy of Sciences, University of Chinese Academy of Sciences, China), Xin Wang (Institute of Software, Chinese Academy of Sciences, University of Chinese Academy of Sciences), Li Yang (Institute of Software, Chinese Academy of Sciences), Fengjun Zhang (Institute of Software, Chinese Academy of Sciences, China), Peng Wang (Institute of Software, Chinese Academy of Sciences, University of Chinese Academy of Sciences), Jia Xu (Institute of Software, Chinese Academy of Sciences, University of Chinese Academy of Sciences), Jiajia Ma (Institute of Software, Chinese Academy of Sciences, China)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808102

**中文总结:** 提出基于 LLaMA-3.1-8B 的 Bash-Commenter，经持续预训练、复杂多行脚本 SFT，以及基于 AST 原子扰动构造偏好对的 Syntax-Aware Preference Optimization（SAPO）生成 Bash 注释；在单行/多行基准上多项指标优于现有方法，人工评估亦显示更高正确性、完整性与自然度。

**Abstract:** Bash script comprehension is a significant challenge in Linux environments due to Bash’s syntactic freedom and complex command structures. Despite its critical role in system administration and development, Bash scripts often lack adequate comments, hindering code readability and maintainability. Existing approaches to automated Bash comment generation face two main challenges: (1) Limited training datasets that inadequately represent real-world Bash usage patterns, particularly for complex multi-line scripts; and (2) Insufficient understanding of Bash-specific concepts by Large Language Models (LLMs). Our empirical analysis shows that even after standard training, LLMs still struggle to precisely understand complex Bash command semantics, leading to inaccurate comments. To address these challenges, we propose Bash-Commenter, an advanced comment generation method based on LLaMA-3.1-8B that employs a three-stage pipeline. First, we perform Continual Pre-training (CPT) on large-scale Bash script data to enhance the model’s foundational understanding of Bash syntax and semantics, addressing the second challenge. Second, to overcome data limitations (the first challenge), we construct a comprehensive dataset of complex, multi-line scripts and then perform Supervised Fine-tuning (SFT). Finally, to resolve the subtle semantic errors that persist, we introduce Syntax-Aware Preference Optimization (SAPO). This method automatically constructs preference pairs by applying single, atomic operations (e.g., modifying a command option or removing an argument) to a script’s Abstract Syntax Tree (AST), creating minimal pairs of correct and subtly incorrect scripts. This final optimization stage enables fine-grained command semantics learning and context-dependent quality assessment, significantly improving comment accuracy. We evaluate Bash-Commenter on single-line Bash commands and multi-line Bash scripts. Our method outperforms state-of-the-art baselines, achieving 33.40% BLEU-4, 58.26% METEOR, and 57.03% ROUGE-L for 1,064 single-line commands, and 22.15% BLEU-4, 43.89% METEOR, and 32.80% ROUGE-L for 1,046 multi-line scripts. Moreover, human evaluation demonstrates the superior quality of comments generated by Bash-Commenter in terms of correctness, completeness, and naturalness.

## 6. Boosting LLMs for Mutation Generation

**Authors:** Bo Wang (Beijing Jiaotong University), Ming Deng (Beijing Jiaotong University), Mingda Chen (Beijing Jiaotong University), Chengran Yang (Singapore Management University, Singapore), Youfang Lin (Beijing Jiaotong University), Mark Harman (Meta Platforms, Inc. and UCL), Mike Papadakis (University of Luxembourg), Jie M. Zhang (Mistral AI and King's College London)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808156

**中文总结:** 提出 SMART，结合真实缺陷向量库上的 RAG、聚焦代码分块，以及与真实缺陷配对变异的监督微调以提升 LLM 变异测试；在 Defects4J/ConDefects 的 1,991 个 Java 缺陷上显著提高有效性、非重复与可编译率，真实缺陷检出率达 92.61%，并改善测试优先级与故障定位。

**Abstract:** LLM-based mutation testing is rapidly emerging as a promising testing technology, but existing approaches typically rely on a fixed set of mutations as few-shot examples or none at all. This can result in generic low-quality mutations, missed context-specific mutation patterns, substantial numbers of redundant and uncompilable mutants, and limited semantic similarity to real bugs. To overcome these limitations, we introduce SMART. SMART integrates retrieval-augmented generation (RAG) on a vectorized dataset of real-world bugs, focused code chunking, and supervised fine-tuning using mutations coupled with real-world bugs. We conducted an extensive empirical study of SMART using 1,991 real-world Java bugs from the Defects4J and ConDefects datasets, comparing SMART to the state-of-the-art LLM-based approaches, LLMut and LLMorpheus.

The results reveal that SMART substantially improves mutation validity, effectiveness, and efficiency (even enabling small-scale 7B-scale models to match/surpass large models like GPT-4o). We also demonstrate that SMART significantly impacts downstream Software Engineering applications to test case prioritization and fault localization. More specifically, SMART improves validity (weighted average generation rate) from 42.89% to 65.6%. It raises the non-duplicate rate from 87.38% to 95.62%, and the compilable rate from 88.85% to 90.21%. In terms of effectiveness, it achieves a real bug detection rate of 92.61% (vs. 57.86% for LLMut) and improves the average Ochiai coefficient from 25.61% to 38.44%. For fault localization, it locates 64 more bugs by MUSE and 57 bugs by Metallaxis as Top-1.

## 7. Cascaded Code Editing: Large-Small Model Collaboration for Effective and Efficient Code Editing

**Authors:** Chaozheng Wang, Zezhou Yang, Shuzheng Gao, Cuiyun Gao Harbin Institute of Technology, Shenzhen, Li Zongjie, Yichen LI, Ting Peng, Hailiang Huang, Yuetang Deng, Michael Lyu

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808101

**中文总结:** 提出级联代码编辑：大模型生成简洁 edit sketch，小模型将其应用到原代码，并构建超 10 万实例的 sketch 应用数据集与专项训练；在 Aider 上相对 DeepSeek R1 直接编辑提升 Pass@2 11.1%，同时降低执行时间与成本约 13%/19%。

**Abstract:** Code editing constitutes a fundamental practice in software development, wherein developers modify existing codebases according to natural language requirements. Accurate code editing necessitates a comprehensive understanding of both the existing codebase and the modification requirements.  Although large language models (LLMs) have demonstrated promising performance in code editing tasks, they suffer from substantial inefficiency by generating entire modified files that largely consist of unchanged code. While smaller models could potentially address this inefficiency, they typically lack the capacity to effectively comprehend long code contexts required for accurate editing. To ensure both effectiveness and efficiency, we propose to decompose code editing into a two-stage cascade: \textbf{edit sketch generation}, wherein a large model first produces concise sketches representing the requisite modifications (the more challenging phase), and \textbf{edit sketch application}, wherein a smaller model integrates these sketches into the original code to produce the final output edited code (the simpler phase). This cascaded design reduces the number of tokens generated by the large model, as the majority of the output is handled by the smaller, more efficient model, thereby enhancing overall efficiency. However, the effectiveness of this approach is constrained by current small models’ limited capabilities in handling long-context scenarios and cross-file dependencies, which are essential for accurate sketch application in real-world codebases. To address these limitations and enhance smaller models’ sketch application capabilities, we introduce the first large-scale sketch application dataset comprising over 100K training instances and 800M tokens, along with a human-evaluated benchmark, and propose specialized training strategies including curriculum-based long-context training and multi-file augmentation. Our comprehensive experiments demonstrate that our cascaded framework inherently reduces inference costs compared to direct editing with large models. Furthermore, combining large models with our fine-tuned smaller models can achieve even superior performance. For instance, on the Aider benchmark, employing DeepSeek R1 as the edit sketch generation model alongside a fine-tuned Qwen2.5 Coder 14B model for the application phase improves Pass@2 11.1% compared to direct editing with DeepSeek R1 alone. Additionally, the cascaded approach reduces execution time and cost by 13% and 19%, respectively, demonstrating both performance gains and efficiency improvements.

## 8. Casting a SPELL: Sentence Pairing Exploration for LLM Limitation-breaking

**Authors:** Yifan Huang, Xiaojun Jia (Nanyang Technological University), Wenbo Guo (Nanyang Technological University), Yuqiang Sun (Nanyang Technological University), Yihao Huang (National University of Singapore, Singapore), Chong Wang (Nanyang Technological University), Yang Liu (Nanyang Technological University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797063

**中文总结:** 提出 SPELL，以时分选择策略组合先验句子构造越狱提示，专门评估恶意代码生成方向的安全对齐弱点；在 GPT-4.1/Claude-3.5/Qwen2.5-Coder 上分别达到 83.75%/19.38%/68.12% 攻击成功率，并在 Cursor 等工具中生成可被检测器判定为恶意的代码。

**Abstract:** Large language models (LLMs) have revolutionized software development through AI-assisted coding tools, enabling developers with limited programming expertise to create sophisticated applications. This democratization of software development has significantly lowered the barriers to entry for complex programming tasks. However, the same accessibility extends to malicious actors who may exploit these powerful tools to generate harmful software, including malware, ransomware, and other security threats. Existing jailbreaking research primarily focuses on general attack scenarios against LLMs, with limited exploration of malicious code generation as a jailbreak target and insufficient technical expertise to evaluate whether generated outputs align with specified malicious objectives. To address this gap, we propose SPELL, a comprehensive testing framework for LLM developer and Secure Team, specifically designed to evaluate the weakness of security alignment in malicious code generation. Our framework employs a time-division selection strategy that systematically constructs jailbreaking prompts by intelligently combining sentences from a prior knowledge dataset, balancing exploration of novel attack patterns with exploitation of successful techniques. Extensive evaluation across three advance code models (GPT-4.1, Claude-3.5, and Qwen2.5-Coder) demonstrates SPELL’s effectiveness, achieving attack success rates of 83.75%, 19.38%, and 68.12% respectively across eight malicious code categories. The generated prompts successfully produce malicious code in real-world AI development tools such as Cursor, with outputs confirmed as malicious by state-of-the-art detection systems at rates exceeding 73%, including 4 instances flagged as extremely dangerous by all detection tools. These findings reveal significant security gaps in current LLM implementations and provide valuable insights for improving AI safety alignment in code generation applications.

## 9. CertiCoder: Towards MISRA-Compliant C Code Generation with LLMs

**Authors:** Min Gou, Zhiyu Yao, Hualong Ma, Ende Zhang, Jian Zhou, Fei He

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797120

**中文总结:** 提出 CertiCoder，经规则微调、冷启动 SFT 与规则感知偏好优化，使 LLM 生成兼顾功能与 MISRA C:2012 合规的 C 代码；在 Qwen2.5-Coder（3B–14B）上将合规性从近零提升至可度量的 J₁，并普遍保持功能正确性。

**Abstract:** Large language models (LLMs) are increasingly applied to code generation in IDEs, CI pipelines, and automated workflows. Existing evaluations, however, have largely focused on functionality, with comparatively limited attention to compliance with established safety standards. This gap is particularly critical for \texttt{C}, where programmes may compile and pass unit tests yet still violate MISRA C:2012, a widely adopted guideline in safety-critical domains. We present \textbf{CertiCoder}, a post-training framework with \emph{rule-aware optimization} that transforms tool-verified outcomes into per-rule contrasts and trains models through three stages: rule tuning, cold-start supervised fine-tuning, and rule-aware preference optimization. This design helps models not only distinguish compliant from violating outputs but also associate violations with specific rules. To support reproducible assessment, we construct a Codeforces-derived \texttt{C} benchmark with frozen splits, multi-level decontamination, and metrics that jointly measure MISRA compliance ($S_{1}$), functional correctness ($F_{1}$), and their conjunction ($J_{1}$). On Qwen2.5-Coder backbones (3B–14B), CertiCoder substantially improves compliance from near-zero to measurable $J_{1}$ levels and generally preserves functional correctness, outperforming non–rule-aware baselines such as SFT and SafeCoder. To our knowledge, this makes CertiCoder among the first post-training frameworks to explicitly optimize both compliance and correctness, offering a practical step toward more auditable and extensible use of LLMs in safety-critical software systems.

## 10. Chiseling Out Efficiency: Structured Skeleton Supervision for Efficient Code Generation

**Authors:** Yu Yu, Zhihong Sun, Jia Li, Yao Wan, Chuanyi Li, Hongyu Zhang, Ruyun Wang, Tao Huang, Zhi Jin, Ge Li, Chen Lyu

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808194

**中文总结:** 提出 EffiSkel，从词法、AST 与运行剖析中抽取效率骨架，并以多任务学习联合优化代码生成与骨架预测；在 Mercury 上相对 EffiCoder/CodeDPO 提升 Efficiency Ratio 与 Average Speedup。

**Abstract:** \textit{Large Language Models} (LLMs) are capable of generating syntactically correct and functionally complete programs, greatly streamlining software development. However, recent studies reveal that these programs typically execute substantially slower than human-optimized counterparts. Existing approaches to bridging this efficiency gap typically involve either iteratively optimizing code after generation or fine-tuning models on corpora of efficient code. Yet, these methods expose the model to efficiency signals only by mimicking complete, optimized solutions, without explicitly encoding the structural code patterns essential for achieving high runtime performance. Addressing this gap presents two core challenges: (1) extracting and representing latent, efficiency-oriented structural patterns embedded within complex syntax and control flows, and (2) effectively learning these patterns without destabilizing the semantic training of LLMs. To tackle these challenges, we propose EffiSkel, an \textit{effi}ciency \textit{skel}eton-guided framework that explicitly extracts and learns efficiency skeletons—abstract, reusable structural patterns underpinning efficient code—by leveraging three complementary strategies: lexical analysis based on token-frequency saliency, syntactic analysis using similarity over Abstract Syntax Trees (ASTs), and dynamic line-level profiling of execution time. These skeletons are integrated into a multi-task learning regime that jointly optimizes code generation and skeleton prediction, introducing an explicit inductive bias toward efficiency-aware code generation. Experiments across multiple programming languages and benchmarks demonstrate that EffiSkel significantly enhances both functional correctness and efficiency, resulting on \textit{Mercury} with DeepSeek-Coder (7B) a +11.11% (vs. EffiCoder) and +3.71% (vs. CodeDPO) higher Efficiency Ratio (ER), and a +0.36 (vs. EffiCoder) and +0.22 (vs. CodeDPO) increase in Average Speedup (AS). These results highlight the effectiveness of explicitly modeling efficiency skeletons in improving the runtime performance of code generated by LLMs.

## 11. CodeCureAgent: Automatic Classification and Repair of Static Analysis Warnings

**Authors:** Pascal Joos (CISPA Helmholtz Center for Information Security), Islem BOUZENIA (CISPA Helmholtz Center for Information Security), Michael Pradel (CISPA Helmholtz Center for Information Security)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808140

**中文总结:** 提出 CodeCureAgent，以 LLM 智能体迭代检索与编辑来分类、抑制误报并修复真实静态分析警告，经构建/警告消失/测试三重验证；在 1000 条 SonarQube 警告上合理修复率 96.8%，人工抽查正确修复率 86.3%。

**Abstract:** Static analysis tools are widely used to detect bugs, vulnerabilities, and code smells. Traditionally, developers must resolve these warnings manually by analyzing the warning, deciding whether to fix or suppress it, and validating the correctness of the code change. Because this process is tedious, developers sometimes ignore warnings, leading to an accumulation of warnings and a degradation of code quality. Prior work suggests techniques to automatically repair static analysis warnings, but these are limited to specific analysis rules, cannot perform multi-file edits, and rely on weak validation mechanisms. This paper presents CodeCureAgent, an approach that harnesses LLM-based agents to automatically analyze, classify, and repair static analysis warnings. Unlike previous work, our method does not follow a predetermined algorithm. Instead, we adopt an agentic framework that iteratively invokes tools to gather additional information from the codebase (e.g., via code search) and edit the codebase to resolve the warning. CodeCureAgent detects and suppresses false positives, while fixing true positives when identified. We equip CodeCureAgent with a three-step heuristic to approve patches: (1) build the project, (2) verify that the warning disappears without introducing new warnings, and (3) run the test suite. We evaluate CodeCureAgent on a dataset of 1,000 SonarQube warnings found in 106 Java projects and covering 291 distinct rules. Our approach produces plausible fixes for 96.8% of the warnings, outperforming state-of-the-art baseline approaches by 30.7% and 29.2% in plausible-fix rate, respectively. Manual inspection of 291 cases reveals a correct-fix rate of 86.3%, showing that CodeCureAgent can reliably repair static analysis warnings. The approach incurs LLM costs of about 2.9 cents (USD) and an end-to-end processing time of about four minutes per warning. We envision CodeCureAgent helping to clean existing codebases and being integrated into CI/CD pipelines to prevent the accumulation of static analysis warnings.

## 12. Coding in a Bubble? Evaluating LLMs in Resolving Context Adaptation Bugs During Code Adaptation

**Authors:** Tanghaoran Zhang, Xinjun Mao, Shangwen Wang, Yuxin Zhao, Yao Lu, Zezhou Tang, Wenyu Xu, Longfei Sun, Changrong Xie, Kang Yang, Yue Yu

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797148

**中文总结:** 提出 CtxBugGen，通过四步流程系统生成上下文适配缺陷（CtxBugs）以评估 LLM；实证显示最佳模型 Kimi-K2 的 Pass@1 仅 55.93%，且 CtxBugs 可使适配性能下降最高约 30%，暴露跨上下文推理不足。

**Abstract:** Code adaptation is a fundamental but challenging task in software development, requiring developers to modify existing code for new contexts. A key challenge is to resolve \textit{\textbf{Context Adaptation Bugs (CtxBugs)}}, which occurs when code correct in its original context violates constraints in the target environment. Unlike isolated bugs, \textit{CtxBugs} cannot be resolved through local fixes and require cross-context reasoning to identify semantic mismatches. Overlooking them may lead to critical failures in adaptation. Although Large Language Models (LLMs) show great potential in automating code-related tasks, their ability to resolve \textit{CtxBugs} remains a significant and unexplored obstacle to their practical use in code adaptation.

To bridge this gap, we propose \textit{CtxBugGen}, a novel framework for generating \textit{CtxBugs} to evaluate LLMs. Its core idea is to leverage LLMs’ tendency to generate plausible but context-free code when contextual constraints are absent. The framework generates \textit{CtxBugs} through a four-step process to ensure their relevance and validity: (1) Selection of four established context-aware adaptation tasks from the literature, (2) Perturbation via task-specific rules to induce \textit{CtxBugs} from LLMs while ensuring their plausibility, (3) Generation of candidate variants by prompting LLMs without any context constraints and (4) Identification of valid \textit{CtxBugs} through syntactic differencing and test execution in the target context. Based on the benchmark constructed by \textit{CtxBugGen}, we conduct an empirical study with four state-of-the-art LLMs. Our results reveal their unsatisfactory performance in \textit{CtxBug} resolution. The best performing LLM, Kimi-K2, achieves 55.93% on Pass@1 and resolves just 52.47% of \textit{CtxBugs}. The presence of \textit{CtxBugs} degrades LLMs’ adaptation performance by up to 30%. Failure analysis indicates that LLMs often overlook \textit{CtxBugs} and replicate them in their outputs. This suggests that LLMs overly focus on the local code correctness of the reused code while ignoring its compatibility in the target context. Our study highlights a critical weakness in LLMs’ cross-context reasoning and emphasize the need for new methods to enhance their context awareness for reliable code adaptation.

## 13. Comment Traps: How Defective Commented-out Code Augment Defects in AI-Assisted Code Generation

**Authors:** Yuan Huang, Yukang Zhou, Xiangping Chen, Zibin Zheng

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797102

**中文总结:** 评估 GitHub Copilot 与 Cursor 如何受有缺陷注释代码（CO code）影响：上下文中的缺陷 CO code 可使生成缺陷代码比例高达 58.17%，且工具会推理补全不完整缺陷模式；即使明确要求忽略，缺陷降幅也不超过 21.84%。

**Abstract:** With the rapid development of large language models in code generation, AI-powered editors such as GitHub Copilot and Cursor are revolutionizing software development practices. At the same time, studies have identified potential defects in the generated code. Previous research has predominantly examined how code context influences the generation of defective code, often overlooking the impact of defects within commented-out code (CO code). AI coding assistants’ interpretation of CO code in prompts affects the code they generate. This study evaluates how AI coding assistants, GitHub Copilot and Cursor, are influenced by defective CO code. The experimental results show that defective CO code in the context causes AI coding assistants to generate more defective code, reaching up to 58.17 percent. Our findings further demonstrate that the tools do not simply copy the defective code from the context. Instead, they actively reason to complete incomplete defect patterns and continue to produce defective code despite distractions such as incorrect indentation or tags. Even with explicit instructions to ignore the defective CO code, the reduction in defects does not exceed 21.84 percent. These findings underscore the need for improved robustness and security measures in  AI coding assistants.

## 14. CrypFormBench: Benchmarking Formal Analysis Capability of Large Language Models for Cryptographic schemes

**Authors:** Zhaoxuan Li (Institute of Information Engineering, Chinese Academy of Sciences;School of Cyber Security, University of Chinese Academy of Sciences), Qionglu Zhang (State Key Laboratory of Information Security, Institute of Information Engineering Chinese Academy of Sciences, Beijing, China), Hengyuan Liu (State Key Laboratory of Information Security, Institute of Information Engineering Chinese Academy of Sciences, Beijing, China), Xiaoyan Gu (State Key Laboratory of Information Security, Institute of Information Engineering Chinese Academy of Sciences, Beijing, China), Xianhui Lu (State Key Laboratory of Information Security, Institute of Information Engineering Chinese Academy of Sciences, Beijing, China), Hongbo Liu (State Key Laboratory of Information Security, Institute of Information Engineering Chinese Academy of Sciences, Beijing, China), Bingzheng Wang (State Key Laboratory of Information Security, Institute of Information Engineering Chinese Academy of Sciences, Beijing, China), Haihui Fan (State Key Laboratory of Information Security, Institute of Information Engineering Chinese Academy of Sciences, Beijing, China), Ziming Zhao (Zhejiang University), Rui Zhang (Taiyuan University of Science and Technology), Li Zhou (Institute of Software, Chinese Academy of Sciences)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808184

**中文总结:** 提出 CrypFormBench，含 700 实例、7 种形式化语言与 677 个方案，系统评估 LLM 在密码方案形式化分析中的解释、生成、补全、转换与纠错能力；多数模型在解释/补全尚可但生成与跨语言转换较弱，仅 Claude-3.5 总分超 50。

**Abstract:** Manual formal analysis of cryptographic schemes is a labor-intensive and expertise-demanding task. While model-checking tools (e.g., Scyther and Tamarin) and computational-security tools (e.g., CryptoVerif and EasyCrypt) significantly enhance the automation of security proofs, they still require experts to abstract schemes and write formal descriptions in specialized languages. Large language models (LLMs) can offer a promising alternative, while their effectiveness in this domain remains unexplored, and the absence of standardized evaluation methodologies makes their capabilities difficult to assess. To address the gaps, we introduce CrypFormBench (C.F.B for short), a comprehensive benchmark supporting both symbolic and computational security, designed to systematically evaluate 5 core capabilities of LLMs in formal analysis of cryptographic schemes, including formal code interpretation, generation, completion, transformation, and correction. It comprises 700 instances covering 7 mainstream formal languages and 677 schemes, supporting the verification of 160 security properties. The evaluation of 9 state-of-the-art LLMs reveals that most of them perform well in code interpretation and completion due to their code-awareness advantages, but struggle to achieve code generation, cross-language transformation, and false-positive correction. Overall, LLMs exhibit limited effectiveness in formal analysis of cryptographic schemes, with only Claude-3.5 scoring above 50 out of 100. Based on our findings, we propose practical recommendations for the model design and usage, such as fine-tuning and few-shot mechanisms, to bolster LLMs’ effectiveness in securing cryptographic schemes. Taken together, our analysis of LLMs’ formal analysis capabilities in cryptographic schemes highlights current progress and outlines directions for future improvements.

## 15. Detecting Code-Comment Inconsistencies in Smart Contracts by Combining LLM and Program Analysis

**Authors:** Jiashuo Zhang (Peking University, China), Jiachi Chen (Zhejiang University), Ting Zhang (Peking University), Yue Li (Peking University), Daoyuan Wu (Lingnan University), Yanlin Wang (Sun Yat-sen University), Jianbo Gao (Peking University), Ting Chen (University of Electronic Science and Technology of China), Zhong Chen

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808112

**中文总结:** 提出 SmartComment，将 LLM 与注释传播、上下文抽取、程序变体及差分分析结合，检测智能合约代码-注释不一致；在 1000 个真实合约上检出 203 个有效不一致（精度 79.9%），F1 由 58.7% 提升至 81.3%。

**Abstract:** Smart contracts have attracted rapid development and widespread application. Due to the complexity of real-world smart contracts, it is error-prone to correctly enforce all intended functionalities in code implementations, resulting in unintended functional behaviors and security issues in practice. Code-comment inconsistency detection has emerged as an important solution to these issues, which leverages the redundant functional specifications in comments to detect code implementations that violate developers’ intentions. However, existing inconsistency detection solutions are typically pattern-based and limited to fixed types of inconsistencies, which prevents them from detecting the diverse inconsistencies between real-world code implementations and casually written comments. To bridge the gap, this paper presents SmartComment, the first technique that combines LLMs with program analysis techniques for detecting code-comment inconsistencies in smart contracts. SmartComment introduces an LLM-driven workflow which simulates real-world interactions between code reviewers and developers to identify inconsistencies. It incorporates various program analysis techniques into the workflow, including comment propagation and code context extraction for generating input context for inconsistency detection, as well as program variant generation and differential analysis for inconsistency confirmation. Our evaluation results show that SmartComment detects 203 valid inconsistencies from a dataset of 1,000 real-world contracts with a precision of 79.9%, highlighting its effectiveness in detecting prevalent and diverse real-world inconsistencies. Compared to previous work, SmartComment achieves both higher precision and recall, detecting over 90% of inconsistencies that existing methods fail to identify. Furthermore, an ablation experiment demonstrates the effectiveness of incorporating program analysis techniques into SmartComment, improving the F1-score from 58.7% to 81.3%.

## 16. Do Not Treat Code as Natural Language: Implications for Repository-Level Code Generation and Beyond

**Authors:** Minh Le-Anh (FPT Software AI Center), Huyen Nguyen (Hanoi University of Science and Technology), Khanh An Tran (Hanoi University of Science and Technology), Nam Le Hai (Hanoi University of Science and Technology), Linh Ngo Van (Hanoi University of Science and Technology), Nghi D. Q. Bui (Google Research), Xuan-Bach D. Le (University of Melbourne)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797144

**中文总结:** 提出 Hydra，以结构感知层次索引与依赖感知检索（DAR）替代 NLP 式切块/相似检索，并混合提供必要依赖与用法示例；在 DevEval/RepoExec 上将 Pass@1 相对最强基线提升逾 5%，甚至使小模型逼近更大模型。

**Abstract:** Large language models for code (CodeLLMs) have demonstrated remarkable success in standalone code completion and generation, sometimes even surpassing human performance, yet their effectiveness diminishes in repository-level settings where cross-file dependencies and structural context are essential. Existing Retrieval-Augmented Generation (RAG) approaches often borrow strategies from NLP, relying on chunking-based indexing and similarity-based retrieval. Chunking results in the loss of coherence between code units and overlooks structural relationships, while similarity-driven methods frequently miss functionally relevant dependencies such as helper functions, classes, or global variables. To address these limitations, we present Hydra, a repository-level code generation framework that treats code as structured code rather than natural language. Our approach introduces (i) a structure-aware indexing strategy that represents repositories as hierarchical trees of functions, classes, and variables, preserving code structure and dependencies, (ii) a lightweight dependency-aware retriever (DAR) that explicitly identifies and retrieves the true dependencies required by a target function, and (iii) a hybrid retrieval mechanism that combines DAR with similarity-based retrieval to provide both essential building blocks and practical usage examples. Extensive experiments on the challenging DevEval and RepoExec benchmarks, both requiring function implementation from real-world repositories with complex large repository context, show that Hydra achieves state-of-the-art performance across open- and closed-source CodeLLMs. Notably, our method establishes a new state of the art in repository-level code generation, surpassing strongest baseline by over 5% in Pass@1 and even enabling smaller models to match or exceed the performance of much larger ones that rely on existing retrievers.

## 17. ExpeRepair: Dual-Memory Enhanced LLM-based Repository-Level Program Repair

**Authors:** Fangwen Mu, Junjie Wang, Lin Shi, Song Wang, Shoubin Li, Qing Wang

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808181

**中文总结:** 提出 ExpeRepair，以情景记忆与语义记忆双通道积累历史修复经验，并动态组合上下文提示做仓库级程序修复；在 SWE-Bench Lite/Verified 上 Pass@1 分别达 60.3% 与 74.6%，刷新开源方法 SOTA。

**Abstract:** Automatically repairing software issues remains a fundamental challenge at the intersection of software engineering and AI. Although recent advancements in Large Language Models (LLMs) have demonstrated potential for repository-level repair tasks, current methodologies exhibit two notable limitations: (1) they often address issues in isolation, neglecting to incorporate insights from previously resolved issues, and (2) they rely on static, rigid prompting strategies that constrain their ability to generalize across diverse and evolving issue scenarios. We propose ExpeRepair, a novel LLM-based program repair framework inspired by the dual memory systems of human cognition, where episodic and semantic memory synergistically support learning and decision-making. Unlike existing methods, ExpeRepair continuously learns from historical repair experiences via dual-channel knowledge accumulation, enabling it to adaptively reuse past knowledge during inference. Specifically, ExpeRepair organizes prior repair knowledge into two complementary memories: an episodic memory that stores concrete repair demonstrations, and a semantic memory that encodes abstract, reflective insights. At inference time, ExpeRepair activates both memory systems by retrieving relevant demonstrations from episodic memory and recalling high-level repair insights from semantic memory. It further enhances adaptability through dynamic prompt composition, synergistically integrating both memory types to replace static prompts with context-aware, experience-driven prompts. We evaluate ExpeRepair on two benchmarks: SWE-Bench Lite and SWE-Bench Verified. Experimental results show that ExpeRepair achieves Pass@1 scores of 60.3% and 74.6% on the two benchmarks, respectively, establishing new state-of-the-art performance among open-source methods. We have open-sourced ExpeRepair at https://github.com/ExpeRepair/ExpeRepair .

## 18. From Specifications to Implementation in the Gen-AI Era: Lessons from a Project-based Software Engineering Course

**Authors:** Yingying Wang (University of British Columbia), Masih Beigi Rizi (University of British Columbia), Fatemeh Khashei (University of British Columbia), Julia Rubin (The University of British Columbia)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797092

**中文总结:** 基于项目制软件工程课程与 Copilot/Cursor 独立案例研究，分析学生在需求到评审全流程中使用生成式 AI 的体验；发现 AI 未取代 SE 教育，反而使需求、设计、评审与系统测试更关键，并给出后续课程与实践建议。

**Abstract:** This paper investigates experiences, educational needs, and approaches for integrating Generative AI tools in an upper-level project-based undergraduate course on Software Engineering. We report on our course setup, our analysis of students’ experience in the last offering of the course, and an independent case study that we conducted to identify strengths, weaknesses, and strategies for using IDE-embedded AI tools, specifically GitHub Copilot and Cursor, when implementing a project equivalent in size and complexity to those typically carried out by the students in the course.

Our results show that students utilize AI tools in all stages of project development: from requirements, through design, to implementation, testing, and code review, to generate and refine artifacts and to learn unfamiliar concepts. Students have mixed levels of satisfaction with using the tools, both as chat interfaces and as IDE-embedded solutions. We found no correlation between the degree of students’ reliance on AI and their grades. While Generative AI tools simplify repetitive development tasks and help quickly ramp up when working with unfamiliar frameworks and programming languages, these tools are still far from replacing software engineers or rendering software engineering education unnecessary. In fact, in the new AI-empowered reality, skills such as requirements engineering, design, code review, and systematic testing become more relevant than ever. We conclude the paper with a set of suggestions for future offerings of this and similar Software Engineering courses and for using AI in Software Engineering more broadly. We see a promising future for AI-empowered Software Engineering, where humans lead creative work and AI manages repetitive implementation tasks and programming language nuances.

## 19. GraphQLify: Automated and Type Safety-Preserving GraphQL API Adoption

**Authors:** Saleh Amareen (Wayne State University), Arif Rahman (Wayne State University), Sazzadur Rahaman (University of Arizona, Tucson, Arizona, USA), Amiangshu Bosu (Wayne State University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797141

**中文总结:** 提出 GraphQLify，经静态分析与类型推断自动将现有 API 迁移为嵌入式 GraphQL 服务以保持端到端类型安全；在 834 个 API 上零失败且无类型不匹配，五次串行调用场景下数据获取可提速 2–4 倍。

**Abstract:** This paper introduces GraphQLify, an automated framework for facilitating the migration of existing APIs to GraphQL. While prior works in this area targeted relational databases, resource description frameworks (RDF), or machine-parsable API specifications, GraphQLify takes a new approach by leveraging static source code analysis for type inference. This approach helps generate GraphQL schemas, maintaining end-to-end type safety, a key premise of using GraphQL over REST. Since the separate GraphQL servers generated by existing techniques work as adapters to existing APIs, they incur performance overhead due to dynamic request binding and network latency. On the other hand, \textit{GraphQLify} generates an embedded server to directly invoke existing API code, and therefore provides better performance.   During our evaluation with 834 APIs from nine popular OSS projects, GraphQLify successfully converted all while matching the types from the original APIs. While OASGraph, the current state-of-the-art, had 3.5% failure rates and 42% type mismatches in our evaluation, both numbers are at 0% for GraphQLify.  Finally, our evaluation suggests that for application workflows requiring five sequential API calls, clients can reduce data fetching time by a factor of 2 to 4 by using the GraphQLify-generated APIs over REST counterparts.

## 20. Hallucinations in LLM-based Code Summarization: Unveiling, Detection, and Mitigation

**Authors:** Guanghua Wan (Huazhong University of Science and Technology), Yuanning Feng (Huazhong University of Science and Technology), Yao Wan (Huazhong University of Science and Technology), Zhaoyang Chu (University College London (UCL)), Zhangqian Bi (Huazhong University of Science and Technology), Junxiao Han (Hangzhou City University), Zhou Zhao (Zhejiang University), Hongyu Zhang (Chongqing University), Pingpeng Yuan (Huazhong University of Science and Technology), Xuanhua Shi (Huazhong University of Science and Technology), Hai Jin (Huazhong University of Science and Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808139

**中文总结:** 构建 Hallu-Eval 数据集并分别提出 Hallu-Det 与 Hallu-Shield，系统揭示、检测与缓解 LLM 代码摘要幻觉；扰动代码可将幻觉率推至 97%，检测 F1 达 0.95，推理期缓解可将 DeepSeek-Coder 幻觉率相对降低约 10.6%。

**Abstract:** Code summarization plays a vital role in program comprehension and software maintenance by generating natural language descriptions to summarize the semantics of code. While Large Language Models (LLMs) have shown remarkable performance in this area, recent empirical studies reveal a critical limitation: LLMs are prone to hallucinations, producing summaries that are factually inaccurate or unfaithful to the source code, potentially misleading developers. In this paper, we propose to unveil, detect, and mitigate hallucinations in LLM-based code summarization.  First, we construct Hallu-Eval, a novel dataset for unveiling hallucination phenomena and rigorously evaluating the effectiveness of hallucination detection and mitigation in LLM-based code summarization. It comprises both original code snippets to capture naturally occurring hallucinations and their semantically perturbed counterparts, which are designed to systematically induce challenging logical hallucinations, all complemented with manual hallucination annotations. Next, we propose Hallu-Det, a synergistic approach that combines direct entity-level detection to identify explicit hallucinations with a synonymous mutation-based refinement to reliably confirm or refute more ambiguous cases.  Finally, we introduce Hallu-Shield, an inference-time mitigation approach that leverages an external value model to guide LLMs toward producing more faithful summaries—without costly retraining of the LLM itself.  Extensive experiments show that Hallu-Eval effectively triggers hallucinations, increasing the hallucination rate of models such as Qwen2.5-Coder-7B from 17% to 97% on perturbed code. Our detection approach, Hallu-Det, achieves the best performance among baselines, reaching an F1-score of 0.95 for summaries generated by Qwen2.5-Coder-7B. Moreover, our mitigation method, Hallu-Shield, reduces hallucination rates—for example, from 66% to 59%, a 10.6% relative reduction, on DeepSeek-Coder-6.7B—while simultaneously improving summary quality, achieving a 71.5% win rate in a side-by-side evaluation using an LLM as a judge.

## 21. In Line with Context: Repository-Level Code Generation via Context Inlining

**Authors:** Chao Hu (Shanghai Jiao Tong University), Wenhao Zeng (Shanghai Jiao Tong University), Yuling Shi (Shanghai Jiao Tong University), Beijun Shen (Shanghai Jiao Tong University), Xiaodong Gu (Shanghai Jiao Tong University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797094

**中文总结:** 提出 InlineCoder，通过将未完成函数内联进调用图，把仓库级生成转化为函数级任务，并用 draft anchor 驱动上游内联与下游检索；在 DevEval 与 RepoExec 上相对最强基线平均提升 EM 29.73%、ES 20.82%、BLEU 49.34%。

**Abstract:** Repository-level code generation has attracted growing attention in recent years. Unlike function-level code generation, it requires the model to understand the entire repository, reasoning over complex dependencies across functions, classes, and modules. However, existing approaches such as retrieval-augmented generation (RAG) or context-based function selection often fall short: they primarily rely on surface-level similarity and struggle to capture the rich dependencies that govern repository-level semantics. In this paper, we introduce InlineCoder, a novel framework for repository-level code generation. InlineCoder enhances the understanding of repository context by inlining the unfinished function into its call graph, thereby reframing the challenging repository understanding as an easier function-level coding task. Given a function signature, InlineCoder first generates a \textit{draft} completion, termed an anchor, which approximates downstream dependencies and enables perplexity-based confidence estimation. This anchor drives a bidirectional inlining process: (\emph{i}) Upstream Inlining, which embeds the anchor into its callers to capture diverse usage scenarios; and (\emph{ii}) Downstream Retrieval, which integrates the anchor’s callees into the prompt to provide precise dependency context. The enriched context, combining draft completion with upstream and downstream perspectives, equips the LLM with a comprehensive repository view. Extensive experiments on the DevEval and RepoExec benchmarks demonstrate that InlineCoder substantially outperforms a wide range of state-of-the-art baselines, with average relative gains of 29.73% in EM, 20.82% in ES, and 49.34% in BLEU on RepoExec compared to the strongest baseline. These results highlight its effectiveness in understanding repository contexts as well as its generalization across domains.

## 22. Influence-Aware Bayesian-Inspired Token Reweighting for Improved Code Generation

**Authors:** YUQI ZHU (Academy of Military Sciences), Ge Li (Peking University), Hong Mei (Peking University), Zhi Jin (Peking University, Wuhan University), Jia Li (Wuhan University), Qibin Zheng (Advanced Institute of Big Data, Beijing), Jieyuan Zhang (Academy of Military Sciences)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808200

**中文总结:** 提出 I-BAYGEN，识别并量化对正确性影响大的 influential tokens，以额外推理路径做 Bayesian-inspired 后验估计并用影响力重加权自奖励；在竞赛级编程基准上相对非加权奖励方法最高提升 47.2% 准确率。

**Abstract:** Large language models (LLMs) have achieved remarkable progress in code generation, yet the structural properties of programming languages introduce distinctive challenges. In particular, program correctness is disproportionately influenced by a subset of structurally critical tokens, such as API names, variable identifiers, and control-flow keywords, termed as influential tokens. Errors in predicting these tokens often propagate and accumulate through subsequent decoding steps, leading to substantial degradation in overall correctness. Addressing the heterogeneous difficulty of predicting such tokens is therefore crucial for improving the reliability of code generation. To address this challenge, we introduce Influence-Aware Bayesian Code Generation (I-BAYGEN), a framework that explicitly handles influential tokens. The framework consists of two components. First, it identifies influential tokens using a loss-based detection mechanism, and measures the influential degree of each token in three ways. Second, to handle the influential tokens, we explicitly steer additional reasoning paths as the evidence to obtain the posterior token distribution during code generation, which can be treated as Bayesian inference. To optimize the posterior likelihood, we involve the influence scores as weights to enhance the self-rewarding, making the LLM pay more attention to the identified influential tokens. Using the influence-based reweighting mechanism, the framework provides differentiated treatment to tokens based on their difficulty, with influential tokens receiving enhanced attention through refined reward structures and deeper reasoning processes. Comprehensive experiments on competition-level programming benchmarks demonstrate that I-BAYGEN achieves up to 47.2% relative improvement in accuracy over state-of-the-art approaches employing non-weighted rewards. Moreover, qualitative analysis reveals that the framework produces reasoning paths that are more interpretable and logically coherent, effectively addressing heterogeneous token difficulty in code generation.

## 23. Knowledge-Graph-Driven Data Synthesis for Low-Resource Software Development: A HarmonyOS Case Study

**Authors:** Mingwei Liu, Zheng Pei, Yanlin Wang, Zihao Wang, Zikang Li, Enci Lin, Xin Peng, Zibin Zheng

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808133

**中文总结:** 提出 APIKG4Syn，基于 API 知识图谱在无需可执行代码的情况下合成面向低资源框架的问答–代码数据，并用 UE 引导的 MCTS 挖掘多 API 组合；以 HarmonyOS 为案例微调后 Qwen 的 pass@1 达 25.00%，超过未微调 GPT 基线 17.59%。

**Abstract:** In low-resource framework software development (e.g., HarmonyOS), large language models (LLMs) typically lack exposure during pre-training, leading to poor performance when generating code for such frameworks. While LLMs often preserve code logic across different programming languages, they tend to fail on framework- specific APIs and syntax errors. This suggests that pre-training enables LLMs to master general algorithms, but they remain unfamiliar with the syntax and API characteristics of unseen low-resource languages or frameworks. Consequently, even large-scale commercial models such as GPT-4o struggle to produce correct code without prior knowledge of these elements. Inspired by these challenges, we introduce APIKG4Syn, a framework that leverages API knowledge graphs to generate API-Oriented question–code pairs without requiring executable code for low-resource framework. APIKG4Syn provides both single-API information and multi-API information, the latter identified through uncertainty estimation (UE)-guided Monte Carlo Tree Search (MCTS), to construct a comprehensive dataset for fine-tuning LLMs in low-resource scenarios. To evaluate APIKG4Syn, we select HarmonyOS as a case study and develop the first HarmonyOS benchmark for code generation. Experimental results demonstrate that Qwen fine-tuned with APIKG4Syn achieves a pass@1 of 25.00%, surpassing the untuned GPT baseline at 17.59%. These findings underscore the effectiveness of API-Oriented data in improving LLM performance for low-resource software development.

## 24. LLM-Assisted Input-Requirement-Aware Differential Testing of Array Programming Frameworks

**Authors:** Zhichao Zhou (School of Information Science and Technology, ShanghaiTech University), Jingzhu He (ShanghaiTech University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808162

**中文总结:** 提出 ArrayDiff，用 LLM 迁移 NumPy API 语义约束并构建输入需求感知的 API 调用生成器，以搜索进化有效且复杂的调用序列做差分测试；在五组 AP 配对上检出 47 个有效输入差异与 39 个无效输入差异，其中 23 个确认为缺陷或文档问题。

**Abstract:** Array programming (AP) frameworks (e.g., NumPy and Octave) are widely adopted in scientific computing. Critical defects can jeopardize the entire ecosystem. The stability of API designs enables differential testing on various implementations (e.g., two versions). However, two primary obstacles remain. First, current test generation cannot effectively generate valid inputs, as the APIs (e.g., matrix multiplication) have type constraints and semantic requirements. Second, unit testing approaches test APIs independently, but they share a core N-dimensional array structure (ndarray) as inputs. Modifying one API may alter the ndarray’s properties, breaking the correctness of others. We propose a differential testing tool for array programming, called ArrayDiff. We first collect semantic requirements from NumPy’s APIs and leverage LLMs to transfer NumPy’s requirements to other frameworks. Then, we propose an input-requirement-aware API call generator (IRA-ACG). Based on IRA-ACG, ArrayDiff employs search algorithms to evolve tests while ensuring valid inputs. ArrayDiff can generate valid and complex API call sequences to detect potential differences. We evaluate ArrayDiff and its ablation versions on five AP pairs. They detect 47 valid-input differences and 39 invalid ones, with 23 confirmed as bugs or document issues. IRA-ACG boosts the detection of valid-input differences, which constitute most confirmed bugs. Comparing ArrayDiff with TitanFuzz (LLM-based fuzzer) and Ghostwriter (unit tester) confirms the benefits of IRA-ACG and sequence-level testing.

## 25. LoCaL: Countering Surface Bias in Code Evaluation Metrics

**Authors:** Simantika Bhattacharjee Dristi (University of Virginia), Matthew B Dwyer (University of Virginia)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797089

**中文总结:** 揭示参考型代码评估指标对表面特征的强偏差，并提出 LoCaL 基准（3117 对代码，差分模糊打分）；四类 SOTA CEM 在 LoCaL 上性能显著下降，表明暴露表面–功能错配样本有助于构建更稳健的指标。

**Abstract:** With the increasing popularity of large language models (LLMs) and LLM-based agents, reliable and effective code evaluation metrics (CEMs) have become crucial for progress across several software engineering tasks. While popular benchmarks often provide test cases to assess the correctness of generated code, crafting and executing test cases is expensive. Reference-based CEMs provide a cheaper alternative by scoring a candidate program based on its functional similarity to a reference. Although prior research has focused on reporting the weak correlation between these CEMs and functional correctness, the causes are only assumed, and plausible solutions remain unexplored. In this work, we critically evaluate four state-of-the-art reference-based CEMs, revealing their strong bias towards surface-level features rather than code functionality. Despite this surface bias, current evaluation datasets for these CEMs rarely include code pairs that are surface-similar yet functionally dissimilar, or functionally similar yet surface-dissimilar. To mitigate this gap, we propose LoCaL ( Looks Can Lie), a CEM evaluation benchmark, with 3117 code pairs at both the method and program levels. Each pair is labeled with a functional similarity score and aims to target regions where CEMs are likely to perform poorly. The functional similarity scores are calculated through differential fuzzing, which eliminates the need for predefined test cases and, at the same time, improves the reliability of the scores by executing an order of magnitude more tests than prior work. We find that all four CEMs show significant performance degradation on LoCaL, compared to the baselines. Finally, based on our findings, we draw the implication that exposing CEMs to LoCaL-like data might facilitate the development of metrics that are robust to surface bias.

## 26. Mitigating Prompt-Induced Cognitive Biases in General-Purpose AI for Software Engineering

**Authors:** Francesco Sovrano (USI Lugano, Switzerland), Gabriele Dominici (Università della Svizzera italiana (USI)), Alberto Bacchelli (IfI, University of Zurich)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808115

**中文总结:** 构建 PROBE-SWE 动态基准评估 SE 决策中 prompt 诱发的认知偏见，发现常见提示工程策略未能显著降低偏见敏感度；提出先显式抽取 SE 最佳实践公理再注入推理线索的端到端方法，平均降低约 51% 偏见敏感度。

**Abstract:** Prompt-induced cognitive biases are changes in a general-purpose AI (GPAI) system’s decisions caused solely by biased wording in the input (e.g., framing, anchors), not task logic. In software engineering (SE) decision support (where problem statements and requirements are natural language) small phrasing shifts (e.g., popularity hints or outcome reveals) can push GPAI models toward suboptimal decisions. We study this with PROBE-SWE, a dynamic benchmark for SE that pairs biased and unbiased versions of the same SE dilemmas, controls for logic and difficulty, and targets eight SE-relevant biases (anchoring, availability, bandwagon, confirmation, framing, hindsight, hyperbolic discounting, overconfidence). We ask whether prompt engineering mitigates bias sensitivity in practice, focusing on actionable techniques that practitioners can apply off-the-shelf in real environments. Testing common strategies (e.g., chain-of-thought, self-debiasing) on popular GPAI systems, we find no statistically significant reductions in bias sensitivity. We then adopt a Prolog-style view of the reasoning process: solving SE dilemmas requires making explicit any background axioms and inference assumptions (i.e., SE best practices) that are usually implicit in the prompt. So, we hypothesize that bias-inducing features short-circuit assumptions elicitation, pushing GPAI models toward biased shortcuts. Building on this, we introduce an end-to-end method that elicits best practices and injects axiomatic reasoning cues in a prompt before answering, reducing overall bias sensitivity by ≈51% on average (𝑝 < .001). Finally, we report a thematic analysis that surfaces linguistic patterns associated with heightened bias sensitivity, clarifying when GPAI use is less advisable for SE decision support and where to focus future countermeasures.

## 27. Natural Language-Focused Software Engineering via Code-Documentation Equivalence

**Authors:** Aryaz Eghbali (CISPA Helmholtz Center for Information Security, Germany), Zhongxin Liu (Zhejiang University), Michael Pradel (CISPA Helmholtz Center for Information Security)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808211

**中文总结:** 提出 documentation-to-code equivalence 概念及自动生成等价文档的 Documentary；在函数级片段上可生成 65.5% 等价文档，并使 LLM 输出预测准确率提高 12.8%–24.5%，仅改文档即可成功完成代码修改的案例也更多。

**Abstract:** Source code documentation is an integral part of software development and maintenance, as it helps in understanding the code and facilitates communication among developers. However, existing documentation is often incomplete, outdated, or inaccurate, which can lead to misunderstandings and errors. In the era of large language models (LLMs), which are being extensively used for software engineering tasks, the quality of documentation becomes even more critical, as documentation provides important context for the models. In this paper, we introduce the notion of documentation-to-code equivalence, a novel property that captures whether documentation accurately and completely describes the code it documents. We present a novel approach, called Documentary, to automatically generate equivalent documentation for a given code snippet. Our evaluation shows that Documentary can generate such documentation for 65.5% of the evaluated, function-level code snippets. To show the benefits of documentation-to-code equivalence, we describe and evaluate two software engineering tasks tasks: code understanding and code editing. Our results show document-to-code equivalence allows an LLM to predict the output of a function with 12.8–24.5% higher accuracy, when compared to human-written documentation and documentation generated by a baseline approach. Likewise, the property helps developers successfully perform code changes by modifying only the documentation, rather than the code itself, in 1.2–12.8% more cases than the baselines.

## 28. Not All RAGs Are Created Equal: A Component-Wise Empirical Study for Software Engineering Tasks

**Authors:** Qiang Ke (Huazhong University of Science and Technology), Yanjie Zhao (Huazhong University of Science and Technology), Hongjin Leng (Xiamen University Malaysia), Shengming Zhao (Fudan University), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808190

**中文总结:** 对 SE 场景 RAG 管线做组件级实证研究，系统评估查询处理、检索、上下文精炼与生成器共 20+ 配置；发现检索侧尤其检索算法对最终性能影响常大于生成器选择，经典 BM25 跨任务表现稳健，并给出实践优化优先级。

**Abstract:** While Retrieval-Augmented Generation (RAG) is increasingly adopted to ground Large Language Models (LLMs) in software artifacts, the optimal configuration of its components remains an open question for software engineering (SE) tasks. The lack of systematic guidance forces practitioners into costly, ad-hoc experimentation. This paper presents a comprehensive, component-wise empirical study that dissects the RAG pipeline, evaluating over 20 distinct models and methods. Our study systematically isolates and evaluates 4 query processing techniques, 7 retrieval models spanning sparse, dense, and hybrid paradigms, 4 context refinement methods, and 5 distinct generators. We test these components on a suite of 3 core SE tasks: code generation, summarization, and repair. Our empirical findings reveal a crucial insight: the retriever-side components, particularly the choice of the retrieval algorithm, often exert a more significant influence on final system performance than the selection of the generator model. Strikingly, the classic lexical retriever BM25 demonstrates exceptionally robust performance across diverse tasks. Our analysis provides a practical, data-driven roadmap for researchers and practitioners, offering clear guidance on prioritizing optimization efforts when constructing effective RAG systems for software engineering contexts.

## 29. One Size Does Fit All: Exploring Model Fusion for Software Engineering Tasks

**Authors:** Yinggang Qiu (National University of Defense Technology), Yihao Qin, Mingyang Geng (National University of Defense Technology), Shangwen Wang (National University of Defense Technology), Dezun Dong (NUDT)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808198

**中文总结:** 系统评估软件工程场景下的模型融合，并提出 Scaling-Masks 改进 TALL-Masks，通过放大弱特征避免其在参数融合中被强特征淹没；同任务融合相近编程语言通常有效，跨任务/跨语言融合易退化，Scaling-Masks 在漏洞检测等场景显著提升融合性能。

**Abstract:** Large language models (LLMs) have achieved remarkable performance in software engineering (SE), and fine-tuning LLM for specific SE tasks has gradually become a new paradigm. However, storing fine-tuned checkpoints for multiple tasks incurs heavy storage and deployment complexity. Model fusion, which operates on fine-tuned parameters, offers excellent parameter compression and scalability, yet its effectiveness in the SE domain remains underexplored, making such an investigation essential for guiding the development of customized fusion techniques for the SE domain. To bridge this gap, we conduct a systematic study of model fusion in the SE contexts and reveal the following major findings: (1) when fusing programming languages (PLs) within the same task, model fusion usually works well and can enhance the performance of PLs with fewer data when PLs share similar features. (2) when fusing SE tasks of the same category within a same PL, all methods except TALL-Masks generally suffer substantial performance degradation on specific tasks; (3) when fusing SE tasks of different categories across different PLs, all existing model fusion methods exhibit significant performance degradation on certain tasks. In our evaluation results, TALL-Masks, which introduces a mask for each task to extract the most relevant dimensions from the fusion parameters, achieves promising performance. However, during parameters fusion, weak features (i.e., small variation in fine-tuned parameters) are easily overshadowed by strong ones (i.e., large variation in fine-tuned parameters) during parameter fusion, causing the constructed masks to fail to extract the most relevant parameters. To overcome this situation, we propose an improved version of TALL-Masks, called Scaling-Masks. The key idea is to amplify weak features to prevent them from being overshadowed by strong ones, which is achieved by scaling the value range of weak features to match that of strong features. Experimental results demonstrate that Scaling-Masks can significantly improve fusion performance for tasks with extremely weak features without affecting other tasks, with normalized accuracy improved by 63.49% for vulnerability detection when fusing SE tasks of different categories and 24.02% for PHP when fusing PLs in the code repair task.

## 30. One Size Does Not Fit All: Revisiting Code Context Engineering for Repository-Level Code Generation

**Authors:** Yichen LI (ByteDance), Qiye Lin (Harbin Institute of Technology, Shenzhen), Yun Peng (The Chinese University of Hong Kong), Zhihan Jiang (The Chinese University of Hong Kong), Jinyang Liu (Chinese University of Hong Kong), Chaozheng Wang (The Chinese University of Hong Kong), Yintong Huo (Singapore Management University, Singapore), Cuiyun Gao (Harbin Institute of Technology, Shenzhen)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808138

**中文总结:** 对仓库级代码生成中相似检索、静态分析与导航式三类上下文工程范式做首次大规模独立对比，并提出 Dependency Collection Rate 等指标；发现静态分析性价比最优，导航式在强模型上上限最高但成本高 10–20 倍。

**Abstract:** Large Language Models (LLMs) have demonstrated remarkable capabilities in code generation at the function or file level. However, they achieve limited performance on repository-level code generation due to the complicated repository context where a substantial amount of files and functions exist. To address this challenge, code context engineering methods are proposed to accurately extract the relevant code context required by repository-level code generation. These methods belong to three dominant paradigms: 1) Similarity-based In-Context Learning (ICL), which retrieves similar code examples in the repository as demonstrations; 2) Static Analysis, which captures relevant code context based on structural dependencies in the repository; and 3) Navigation-based Paradigms, which invokes LLMs to dynamically explore repositories for context identification.

Despite the prevalence of code context engineering approaches, their individual contributions are often coupled within complex agents in repository-level code generation, making it difficult to isolate and evaluate the effectiveness of three paradigms. This paper presents the first large-scale and systematic empirical study that compares three code context engineering paradigms independently. We evaluate seven representative code context engineering methods based on the three paradigms, with eight popular LLMs on repository-level code generation. We also propose a new metric named Dependency Collection Rate (DCR) and efficiency metrics to enable the direct comparison of code context engineering methods, rather than observing their impacts only on the final code generation performance.

Our findings reveal fundamental trade-offs: static analysis provides the most reliable effectiveness-efficiency trade-off, while navigation-based approaches with powerful models achieve the highest performance ceiling but require powerful models and incur 10-20× higher computational costs. Based on these findings, we provide actionable implications for AI coding researchers and software developers to guide the design and deployment of context-aware coding tools.

## 31. Pig: Leveraging Large Language Models for Python Library Migrations

**Authors:** Miryeong Kang (Korea University), Wonseok Oh (Korea University), Gabin An (Korea University), Hakjoo Oh (Korea University)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797072

**中文总结:** 提出 Pig，以 API 级切片、失败模式引导提示、选择性提取与回植四步流水线用 LLM 自动化 Python 库迁移；在 364 个 API 迁移任务上将基线平均成功率提升 53.5%。

**Abstract:** We present Pig, a novel approach to automating Python library migration by leveraging large language models (LLMs). Library migration is an increasingly common task in modern Python development, yet it remains tedious and error-prone due to the lack of general solutions that can handle diverse libraries without relying on documentation or code examples. To address this challenge, Pig employs a four-step pipeline that effectively harnesses the capabilities of LLMs. First, Pig decomposes the migration task into smaller units by performing API-level slicing, allowing the LLM to focus on minimal, relevant context. Second, it guides LLMs using prompts informed by common failure patterns in naive LLM-based migrations and plausible API candidates. Third, Pig selectively extracts the migration-related code fragments from the LLM outputs. Finally, it transplants the migrated code back into the original program with post-processing to ensure semantic correctness and consistency. We demonstrate the effectiveness of Pig by evaluating it on 364 API-level migration tasks, where it improves the average success rate of the baseline approach by 53.5% across seven different LLM models.

## 32. PlayCoder: Making LLM-Generated GUI Code Playable

**Authors:** Zhiyuan Peng (Shanghai Jiao Tong University), Wei Tao (LightSpeed), Xin Yin (Zhejiang University), Chenhao Ying (Shanghai Jiao Tong University), Yuan Luo (Shanghai Jiao Tong University), Yiwen Guo (Unaffiliated)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808097

**中文总结:** 提出面向 GUI 应用的 Play@k 指标与交互评测代理 PlayTester，并构建多代理仓库感知框架 PlayCoder 闭环生成与修复可玩代码；显著提升功能正确性，Play@3 可达 17.2%。

**Abstract:** Large language models (LLMs) have transformed code generation, but their ability to generate code for applications with graphical user interfaces (GUIs), particularly games, remains underexplored. To explore their performance on applications with GUI, we construct a repository-aware evaluation dataset from 35 GUI applications. Prior code-generation benchmarks assess correctness using test cases, but this is insufficient for GUI applications. These applications are interactive and event-driven, and their correctness depends on stateful behavior over sequences of user actions. Consequently, evaluation should account for interaction flows and UI state transitions rather than relying solely on pass or fail test outcomes. To enable more reliable assessment beyond simple execution and unit tests, we propose Play@k, which measures whether at least one of k generated candidates yields an application that can be played end-to-end without logical errors. We further develop an LLM-based agent, PlayTester, that automates interactive evaluation by driving the GUI through task-oriented playthroughs and checking for logic violations. Through systematic evaluation, we demonstrate that 10 state-of-the-art code LLMs struggle to generate logically correct GUI applications, achieving near-zero Play@3 scores despite high compilation rates. To address these challenges, we introduce PlayCoder, a multi-agent, repository-aware framework that writes, evaluates and refines GUI application code via closed-loop control. PlayCoder substantially improves functional correctness and semantic alignment for both open-source and closed-source models, achieving up to 37.5% Exec@3 and 17.2% Play@3. Case studies show that it detects silent logic flaws missed by traditional metrics and repairs them through targeted edits. These results indicate that coupling an end-to-end GUI testing agent with repository-aware automated program repair is an effective path toward reliable GUI code generation.

## 33. Project-Level C-to-Rust Translation via Pointer Knowledge Graphs

**Authors:** Zhiqiang Yuan (Fudan University), Wenjun Mao (Fudan University), Zhou, Xiyue Shang (Fudan University), Chong Wang (Nanyang Technological University), Yiling Lou (University of Illinois at Urbana-Champaign), Xin Peng (Fudan University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808169

**中文总结:** 提出 C-Rust Pointer Knowledge Graph 与 PtrTrans，注入全局指针用法与所有权等语义以指导项目级 C→Rust 翻译；相较规则与 LLM 方法将 unsafe 使用降低 99.9%，功能正确性平均高 29.3%。

**Abstract:** Translating C code into Rust is an effective way to ensure its memory safety. Rule-based translation produces Rust code that remains unsafe and fails to leverage Rust’s safety features. LLM-based methods can generate more idiomatic and safer Rust as LLMs are trained on large amounts of human-written code. Although promising, existing LLM-based methods still struggle with project-level C-to-Rust translation. They typically partition a C project into smaller units (e.g., functions) based on the call graph and translate them bottom-up to resolve dependencies. However, this bottom-up, unit-by-unit paradigm often fails to handle pointer translation due to the lack of a global perspective on pointer usage. To address this, we propose a novel C-Rust Pointer Knowledge Graph (KG) that enriches a code-dependency graph with two types of pointer semantics: (i) pointer-usage information, recording global behaviors such as points-to flows and lower-level struct usage by higher-level units; and (ii) Rust-oriented annotations, encoding ownership, mutability, nullability, and lifetimes. Based on the C-Rust Pointer KG and its synergy with LLMs, we further propose PtrTrans,  a project-level C-to-Rust translation technique. In PtrTrans, the C-Rust Pointer KG provides LLMs with comprehensive pointer semantics from a global perspective, thus guiding LLMs towards generating safe and idiomatic Rust code from a given C project. Our experiments show that PtrTrans reduces unsafe usages in translated Rust by 99.9% compared to both rule-based translation and LLM-based rewriting, while achieving an average 29.3% higher functional correctness than fuzzing-enhanced LLM methods.

## 34. ProofFusion: Improving Neural Theorem Proving via Adaptive Retrieval-Augmented Reasoning

**Authors:** Manqing Zhang (Northwestern Polytechnical University), Yunwei Dong (Northwestern Polytechnical University, School of Computer Science and Engineering), Lingru Zhou (Northwestern Polytechnical University), Bingxu Xiao (Northwestern Polytechnical University), Yepang Liu (Southern University of Science and Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797139

**中文总结:** 提出 ProofFusion，以证明语义检索与双轨重排融合增强神经定理证明且无需重训，并按能力自适应决定是否检索；在 26 个 Coq 项目上平均多证 6.89% 定理，可解释证明目标比例达 82.1%。

**Abstract:** Interactive theorem proving (ITP) is a powerful approach to ensuring the correctness of complex software systems. However, it often requires substantial manual effort, which makes it costly to use in practice. Recently, neural network based approaches have shown promise in automatically generating proof tactics. Nevertheless, existing methods suffer from a long-tailed distribution in tactic usage within the training data. A few frequent tactics dominate the probability distribution, while many rare yet crucial ones are consistently suppressed in the model’s candidate ranking. This distributional bias can cause potentially provable goals to be prematurely abandoned during proof search. In addition, the decision making process of neural networks when generating tactics lacks explicit reasoning traces, making it difficult for humans to explain or verify the underlying logic. To address these limitations, we propose ProofFusion, an adaptive retrieval-augmented reasoning framework that improves the proving capability of neural theorem provers without requiring retraining. Our key insight is inspired by the way human provers tackle a new theorem by consulting similar previously proven theorems to guide their own reasoning. Specifically, we develop a proof semantic-aware retriever that searches a knowledge base for semantically similar historical proof goals together with their tactic, producing a traceable set of reference decisions. We then employ a dual-track reranking fusion mechanism to integrate both the original predictions of the neural model and the retrieved reference tactics. Furthermore, to mitigate potential noise introduced by retrieval, we design a capability-adaptive retrieval mechanism that dynamically determines when retrieval should be applied. We conduct a systematic evaluation on 10,782 theorems from 26 Coq projects in a real ITP environment. Experimental results show that ProofFusion increases the number of theorems proved by four state-of-the-art neural theorem provers by an average of 6.89%, and increases the number of previously unprovable theorems solved by an average of 17.50%. In addition, it substantially improves the explainability of proof steps, achieving an average explainable proof goal proportion of 82.1% across the four provers. Together, these results demonstrate that ProofFusion is a practical and effective complement to existing neural theorem proving systems, enhancing both performance and explainability.

## 35. RealBench: A Repo-Level Code Generation Benchmark Aligned with Real-World Software Development Practices

**Authors:** Jia Li (Wuhan University), Hongyi Deng (Peking University), Yiran Zhang (Nanyang Technological University), Kechi Zhang (Peking University, China), Tianqi Shao (Peking University), Tiankuo Zhao (Wuhan University), Weinan Wang (Peking University), Zhi Jin (Wuhan University), Ge Li (Peking University), Yang Liu (Nanyang Technological University), Yingtao Fang (Wuhan University), Yihong Dong (Peking University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797106

**中文总结:** 提出对齐工业实践的仓库级代码生成基准 RealBench，同时提供自然语言需求与 UML 设计；评估显示仓库级性能显著下降，小仓宜整体生成、复杂仓宜按模块生成，详细系统设计对任务至关重要。

**Abstract:** Writing code requires significant time and effort in software development. To automate this process, researchers have made substantial progress using Large Language Models (LLMs) for code generation. Many benchmarks like HumanEval and EvoCodeBench have been created to evaluate LLMs by requiring them to generate code from natural language requirements. However, in enterprise applications and team development, developers typically write code based on structured designs or specifications rather than raw natural language descriptions. This gap between existing benchmarks and real industry development practices means that current benchmark scores may not accurately reflect how much code generation can help automate software development tasks.

To address this gap, we propose RealBench, a repository-level code generation benchmark aligned with real-world industry software development practices. Each example includes both natural language requirements and UML diagrams as system design, matching how developers typically receive specifications.  Based on the constructed benchmarks, we conduct a systematic evaluation of advanced LLMs’ code generation capabilities when provided with structured system designs. Specifically, we design three generation strategies to evaluate advanced LLMs on RealBench and propose two evaluation granularities with five metrics. The experimental results reveal key insights in current LLMs’ capabilities for repo-level code generation aligned with real-world software development practices. First, we notice that regarding repo-level code generation, LLMs show much worse performance and there are significant performance gaps among LLMs. Second, LLMs are good at finding and creating modules defined in UML diagrams, but the quality of generated modules is often poor due to grammar and logic errors. Third, generating the entire repository at once is the best generation strategy on smaller repositories, while generating a complex repository with the module-by-module strategy works better compared to other strategies. Fourth, the detailed system design is very important for repository-level code generation tasks through conducting ablation studies on system designs. Lastly, we discuss the frequent error types in generated repositories to provide insights for optimizing repo-level code generation.

## 36. Recommending Usability Improvements with Multimodal Large Language Models

**Authors:** Sebastian Lubos (Graz University of Technology), Alexander Felfernig (Graz University of Technology), Damian Garber (Graz University of Technology), Viet-Man Le (Graz University of Technology), Manuel Henrich (UNiQUARE Software Development GmbH)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797121

**中文总结:** 提出用多模态 LLM 结合有限应用上下文与交互录屏，按 Nielsen 启发式识别可用性问题并按严重度排序改进建议；用户研究表明可低成本辅助可用性改进，适合缺乏专家的场景。

**Abstract:** Usability describes quality attributes of application user interfaces that determine how effectively users can interact with them. Traditional usability evaluation methods require considerable expertise and resources, which can be challenging, especially for small teams and organizations. Automating usability evaluation could make it more accessible and help to improve the user experience. The recent emergence of powerful multimodal large language models (MLLMs) has opened new opportunities for automating usability evaluation and recommendation of improvements. These models can process visual inputs such as images and videos alongside textual context, which enables the identification of usability issues and the generation of actionable suggestions to resolve these issues.

In this paper, we present a novel automated approach that uses limited application context and screen recordings of user interactions as input to an MLLM. The model automatically identifies and describes usability issues based on Nielsen’s usability heuristics, and provides corresponding explanations and improvement recommendations. To reduce the developer effort of manual prioritization, the recommendations are ranked by severity. The quality and practical usefulness of the generated recommendations were evaluated based on a user study that involved software engineers as participants. The evaluation focused on the highest-ranked suggestions provided by the model. The results demonstrate the potential of our approach to provide low-effort usability improvement recommendations. This makes it a promising complement to traditional evaluation methods, especially in settings with limited access to usability experts. In this sense, the approach serves as a basis for future integration into development tools to enable automated usability evaluation within software engineering workflows.

## 37. Red Teaming LLMs via Linguistic-Aware Fuzzing

**Authors:** Shuai Yuan (University of Electronic Science and Technology of China), Nian Luo (University Of Electronic Science And Technology Of China), Jingling Sun (University of Electronic Science and Technology of China), Yihao Huang (National University of Singapore, Singapore), Chengyu Zhang (Loughborough University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808204

**中文总结:** 提出 Lingfuzz，在词法与句法层变异恶意指令以持续红队测试对齐 LLM，同时保持恶意意图；在 JailbreakBench 上触发率达 81.3%，多样性超先前工作三倍以上，对模型演进更不敏感。

**Abstract:** Safety alignment aims to prevent Large Language Models (LLMs) from producing harmful content. However, safety alignment remains vulnerable to malicious instructions. Red teaming is a critical methodology for identifying such vulnerabilities in LLMs. Existing approaches often rely on jailbreak templates or rule-based transformation, limiting the diversity of generated tests and the continued testing capability of these test approaches. To address these limitations, we propose Lingfuzz, a linguistic-aware fuzzing framework for continuing red teaming LLMs. The key idea of this framework is to mutate the existing malicious instructions at the lexical and syntactic levels, while keeping the malicious intentions of the instructions. Such mutations enable generating diverse malicious instructions due to the unlimited space of lexical and syntactic choices, while having a continued testing capability by iteratively mutating the mutants. We evaluated Lingfuzz on three aligned GPT-series LLMs. The results show that Lingfuzz triggers safety alignment vulnerabilities in 81.3% of the cases in JailbreakBench benchmark. The malicious instructions generated by Lingfuzz have more than three times higher diversity than previous work according to the self-BLEU metric, while keeping the similar effectiveness in triggering safety alignment vulnerabilities. Lingfuzz also demonstrates strong continued testing capability by showing five times less sensitivity to the LLM evolution than other approaches.

## 38. ReDef: Do Code Language Models Truly Understand Code Changes for Just-in-Time Software Defect Prediction?

**Authors:** Doha Nam (Korea Advanced Institute of Science and Technology), Taehyoun Kim (Korea Advanced Institute of Science and Technology; Agency for Defense Development), Duksan Ryu (Jeonbuk National University), Jongmoon Baik (Korea Advanced Institute of Science and Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808179

**中文总结:** 构建基于 revert 的高置信 JIT 缺陷数据集 ReDef，并系统评估代码语言模型对变更的理解；compact diff 编码效果更优，但反事实扰动显示模型多依赖表层线索而非真正变更语义。

**Abstract:** Just-in-Time software defect prediction (JIT-SDP) plays a critical role in prioritizing risky code changes during code review and continuous integration. However, existing datasets often suffer from noisy labels and low precision in identifying bug-inducing commits. To address this, we present ReDef (Revert-based Defect dataset), a high-confidence benchmark of function-level modifications curated from 22 large-scale C/C++ projects. Defective cases are anchored by revert commits, while clean cases are validated through post-hoc history checks. Ambiguous instances are conservatively filtered out via a GPT-assisted triage process involving multiple votes and audits. This pipeline yields 3,164 defective and 10,268 clean modifications, offering substantially more reliable labels than prior resources. Beyond dataset construction, we provide a systematic evaluation of how Code Language Models (CLMs)—specifically CodeBERT, CodeT5+, UniXcoder, and Qwen2.5—reason about code modifications. We first investigate which input encodings most effectively expose change information under five different strategies. We then design four counterfactual perturbation strategies (e.g., swapping added/deleted blocks, inverting diff polarity) to serve as diagnostic probes. We posit that if models genuinely capture change semantics, such distortions should lead to a clear decline in predictive performance. Our results show that compact diff-style encodings consistently outperform whole-function formats across all CLMs, supported by rigorous statistical confirmation. However, under counterfactual tests, performance remains effectively stable, revealing that what appears to be robustness in fact reflects a reliance on superficial cues rather than true semantic understanding. These findings indicate that, at least in code-change understanding tasks, current CLMs remain limited in their ability to genuinely comprehend the relational dynamics of code modifications.

## 39. Reducing Cost of LLM Agents with Trajectory Reduction

**Authors:** Yuan-An Xiao (Peking University), Pengfei Gao (ByteDance), Chao Peng (Tencent), Yingfei Xiong (Peking University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797084

**中文总结:** 提出推理时轨迹压缩方法 AgentDiet，自动剔除代理轨迹中的无用、冗余与过期信息；在编码代理上降低输入 token 约 40%–60%、计算成本约 21%–36%，且性能基本不变。

**Abstract:** Multi-turn agent systems based on Large Language Models (LLMs) have been increasingly popular for software engineering tasks. While LLM agents show decent effectiveness, the high computational cost of input tokens due to the ever-growing trajectory remains an efficiency concern for their applications. Efficiency is largely neglected in existing studies and agent products, and this paper fills the gap by introducing an inference-time trajectory reduction approach to reduce the cost of agents.

Through analyzing existing agent trajectories, we demonstrate that useless, redundant, and expired information is widespread in all trajectories, which can be identified and reduced without harming the agent’s performance. We then design a simple yet effective trajectory reduction approach, AgentDiet, which automatically removes such waste information. We implement AgentDiet on a top-performing coding agent, and the evaluation on two LLMs and two benchmarks shows that AgentDiet can reduce input tokens by 39.9% ~ 59.7%, or the final computational cost by 21.1% ~ 35.9%, while maintaining the same agent performance. This indicates that trajectory reduction is a promising direction for agent systems.

## 40. ReFLAIR: Detecting Responsive Layout Reflow Issues using Multimodal Generative AI

**Authors:** Yirui He (University of California, Irvine), Ziyao He (University of California, Irvine), Syed Fatiul Huq (University of California, Irvine), Sam Malek (University of California at Irvine)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808136

**中文总结:** 提出 ReFLAIR，用多模态生成式 AI 动态检测响应式布局回流导致的信息或功能丢失；在 24 个网页上较五种 SOTA 方法提升精度约 21%、召回约 55%。

**Abstract:** With over 60 percent of global Internet traffic originating from mobile devices, Responsive Web Design (RWD) has become essential for ensuring seamless user experiences across diverse screen sizes and resolutions. The Web Content Accessibility Guidelines require that both information and functionality remain accessible when reflow occurs. However, existing checkers or research tools have limitations: they either employ static analysis that fails to capture how content is actually displayed to users or focus on only one accessibility aspect, such as keyboard operation. Consequently, no prior study has comprehensively addressed both information and functionality loss during reflow for Graphical User Interfaces (GUIs). This paper introduces ReFLAIR (Reflow Fault Localization using AI-based Responsive analysis), a multimodal generative AI–driven approach for dynamically detecting reflow issues that cause loss of information or functionality in the GUI. ReFLAIR systematically extracts informative and actionable widgets, compares their presence and behavior across original and reflowed layouts, and employs both scrolling and large language model–guided expansion to uncover hidden interface widgets. We evaluate ReFLAIR on a dataset of 24 diverse webpages drawn from popular sites, prior benchmarks, and newly released websites. Results show that ReFLAIR outperforms five state-of-the-art techniques, improving precision by 20.91% and recall by 55.38%, while maintaining reasonable computational and runtime cost. An ablation study confirms that dynamic exploration (i.e., scrolling and expansion) is essential for high accuracy. In summary, our approach contributes to accessibility testing by providing an effective, scalable, and cost-efficient solution for identifying reflow issues in RWD.

## 41. RepoReasoner: Evaluating Repository-Level Code Reasoning Ability of Long-Context Language Models

**Authors:** Yanlin Wang, Suiquan Wang, Yanli Wang, Bowen Zhang, Daya Guo, Jiachi Chen, Zibin Zheng

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808131

**中文总结:** 提出仓库级代码推理基准 RepoReasoner，含输出预测与调用链预测两项任务；评估显示即便完美上下文最佳模型 Pass@1 仅约 69%，架构理解薄弱且存在记忆化依赖。

**Abstract:** Recent advances in large language models (LLMs) have significantly improved their ability to handle complex software engineering tasks at the repository level. However, existing benchmarks for evaluating code reasoning ability operate almost exclusively at the function level, where all necessary information is provided within a single, localized context. This approach fails to capture the complexity of real-world software development, where developers must reason about dependencies and logic scattered across entire repositories, creating a critical gap between current evaluation methodologies and real-world challenges. To bridge this gap, we introduce \bench, a benchmark designed to evaluate repository-level code reasoning ability. Moving beyond self-contained code snippets, \bench assesses LLMs’ ability to navigate, retrieve, and synthesize information distributed across multiple files through two tasks: (1) \textbf{Output Prediction}, which evaluates fine-grained, stateful reasoning by tracing complex, cross-file execution paths to predict a function’s final output, and (2) \textbf{Call Chain Prediction}, which assesses high-level architectural understanding by identifying the correct sequence of files involved in an execution from noisy context. We construct our benchmark using a multi-stage pipeline that leverages dynamic analysis of pytest execution traces to capture true, runtime-dependent call chains, and employs LLM-based I/O rewriting to create logically equivalent instances that prevent memorization. Our extensive evaluation of seven state-of-the-art LLMs reveals that repository-level reasoning remains a fundamental challenge. Even with perfect context, the best-performing model (DeepSeek-R1) achieves only 69.1% Pass@1 on Output Prediction, indicating that complex reasoning—not just retrieval—is the primary bottleneck. LLMs struggle with high-level architectural understanding, exhibiting high precision but low recall (F1 < 0.51) in call chain reconstruction. Counterintuitively, simply increasing context length can be counterproductive, as noise sometimes outweighs the benefits of additional information. All models show significant performance drops on our I/O-rewritten data, confirming partial reliance on memorization rather than genuine reasoning. These findings highlight the need for future research to focus on enhancing architectural comprehension and robust reasoning capabilities in repository-level code analysis.

## 42. Reward-Free Code Alignment from Pretrained or Fine-Tuned LLM: Unpacking the Trade-offs for Code Generation

**Authors:** Sanjeepan Sivapiran, Gias Uddin

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808123

**中文总结:** 实证研究 DPO 与 BoNBoN 在预训练与微调起点上的代码对齐权衡；预训练→对齐提升更大，微调→对齐提升有限甚至退化，非功能需求相对更易持续改善。

**Abstract:** Large Language Model (LLM) alignment trains an LLM using preference data to produce outputs that better reflect human values (e.g., to mitigate toxic or biased responses). While LLM alignment techniques are studied for non-coding tasks, we know little about their usefulness for coding tasks. Intuitively, for code generation tasks using LLMs, alignment techniques could help with coding solutions that better align with developer preferences, such as more secure code, supporting better coding practices, etc. However, it is unclear whether LLM code alignment could support both functional requirements (producing executable, correct code) and non-functional requirements (code readability, style, maintainability). It is also unknown whether alignment for a code LLM should begin with base pretrained version or the finetuned (i.e., instruction-tuned) version of the LLM. In this paper, we offer insights on the above two research questions by conducting an empirical study. We studied five state-of-the-art (SOTA) LLMs using two widely used LLM alignment techniques: Direct Preference Optimization (DPO) and BoNBoN. For each training record, we created a preference pair as accepted and rejected instances by using the SelfCodeAlign pipeline. DPO and BoNBoN are reward-free models, i.e., they eliminate the need for multiple reward scores for output preferences. We tuned each LLM using the two alignment techniques in two settings: pretrained and finetuned versions of an LLM. We evaluated functional requirements using four SOTA benchmarks (HumanEval+, MBPP+, EvalPerf, EvoEval) and non-functional requirements using the SOTA benchmark, CODAL. We find that pretrained-to-aligned pathways achieve larger improvements in the aligned variant over its pretrained variant (CodeLlama-7b: +75% non-functional, Llama3-8b: +42% functional). But the pretrained variant is generally less accurate than its finetuned variant. However, finetuned-to-aligned offers smaller performance improvements or, in some cases, degradation in the aligned variant than its finetuned variant.  This means that while the base pretrained version is less accurate than its base finetuned variant, alignment reduces the performance gap between pretrained and finetuned variants. Non-functional requirements improve more consistently than functional requirements via alignment. Based on these findings, we provide nine recommendations to guide alignment for code LLMs.

## 43. ScanCoder: Leveraging Human Attention Patterns to Enhance LLMs for Code

**Authors:** Yueke Zhang (Vanderbilt University), Yifan Zhang (Vanderbilt University), Zihan Fang (Vanderbilt University), Greg Trafton (Naval Research Laboratory), Daniel Levin (Vanderbilt University), Kevin Leach (Vanderbilt University), Yu Huang (Vanderbilt University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808150

**中文总结:** 提出 ScanCoder，用少量眼动数据经 ACT-R 认知仿真大规模生成类人注意力模式，并据此做认知引导微调以强化关键语义 token；在 CodeXGLUE 上跨模型一致提升，CrystalBLEU 完成指标提升约 39%、BERTScore 摘要提升约 22%，且可将 C++ 认知模式迁移到 Java 任务。

**Abstract:** Code comprehension is a fundamental challenge in software engineering that impacts developer productivity and software quality. While Large Language Models (LLMs) demonstrate strong capabilities in code generation and summarization, they process code differently from human developers, who employ strategic attention patterns focused on semantically critical elements. Recent research has successfully integrated human attention patterns captured through eye-tracking into AI models for software engineering tasks, however, existing human-AI approaches face critical limitations that prevent widespread practical deployment, particularly for LLM enhancement.  Existing approaches to incorporate human cognitive insights face scalability limitations due to resource-intensive eye-tracking studies and lack empirical validation for cross-language generalizability.

We present \textit{ScanCoder}, a framework that integrates cognitive simulation with LLM enhancement through (1) generating human-like attention patterns at scale using minimal eye-tracking data via cognitive simulation with Adaptive Character of Thought-Rational (ACT-R) architecture, and (2) cognitively-guided fine-tuning that emphasizes tokens according to their cognitive salience and attention order. Our approach demonstrates cross-language transfer by applying C++-derived cognitive patterns to enhance Java programming tasks. Comprehensive evaluation on CodeXGLUE benchmarks shows consistent improvements across different LLM architectures, achieving gains of 39% for CrystalBLEU completion metrics and 22% for BERTScore summarization. Mechanistic analysis reveals that cognitive guidance reshapes model attention in task-dependent ways, increasing focus on semantically critical tokens by 2.5×. This work establishes the first scalable framework for integrating simulated human cognitive patterns into LLM training, enabling more interpretable and effective code understanding.

## 44. Still Manual? Automated Linter Configuration via DSL-Based LLM Compilation of Coding Standards

**Authors:** zejun zhang (Nanjing University), Yixin Gan (Nanjing University), Zhenchang Xing (CSIRO's Data61), Tian Zhang (Nanjing University), Yi Li (Nanyang Technological University), Qinghua Lu (Data61, CSIRO), Xiwei (Sherry) Xu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797064

**中文总结:** 提出将自然语言编码规范经 DSL 编译为与语言/工具无关的 linter 配置的 LLM 方法，覆盖解析、匹配、一致性校验与配置生成；在 Checkstyle/Java 上细粒度配置生成指标约 70% 且精度相对基线翻倍以上，并推广到 ESLint/JavaScript。

**Abstract:** Coding standards are essential for maintaining consistent and high-quality code across teams and projects. Linters help developers enforce these standards by detecting code violations. However, manual linter configuration is complex and expertise-intensive, and the diversity and evolution of programming languages, coding standards, and linters lead to repetitive and maintenance-intensive configuration work. To reduce manual effort, we propose a domain-specific language (DSL)-driven, LLM-based compilation approach to automate configuration generation for coding standards, independent of programming languages, coding standards, and linters. Inspired by compiler design, we first design a DSL to express coding rules in a tool-agnostic, structured, readable, and precise manner. Then, we build linter configurations into DSL configuration instructions. For a given natural language coding standard, the compilation process parses it into DSL coding standards, matches them with the DSL configuration instructions to set configuration names, option names and values, verifies consistency between the standards and configurations, and finally generates linter-specific configurations. Experiments with Checkstyle for Java coding standard show that our approach achieves over 90% precision and recall in DSL representation, with accuracy, precision, recall, and F1-scores close to 70% (with some exceeding 70%) in fine-grained linter configuration generation. Notably, our approach outperforms baselines by over 100% in precision. An ablation study confirms the effectiveness of the main components of our approach. A user study further shows that our approach improves developers’ efficiency in configuring linters for coding standards. Finally, we demonstrate the generality of the approach by generating ESLint configurations for JavaScript coding standards, showcasing its broad applicability across other programming languages, coding standards, and linters. We developed a lightweight, general-purpose AI skill, which is publicly available on GitHub: LintConfig .

## 45. SWE Data Construction, Automatically!

**Authors:** Lianghong Guo, Yanlin Wang, Caihua Li, Wei Tao, Pengyu Yang, Jiachi Chen, Haoyu Song, Duyu Tang, Zibin Zheng

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797119

**中文总结:** 提出 SWE-Factory，全自动构建 GitHub issue 解决评测数据：恢复缺失二进制测试文件、用多智能体 SWE-Builder 构建环境，并以退出码标准化 fail2pass 校验；在 671 个跨语言 issue 上以低成本产出有效实例，且用收集数据训练后模型在 SWE-bench Verified 解析率可从 5.8% 升至 21.0%。

**Abstract:** Constructing large-scale datasets for the GitHub issue resolution task is crucial for both training and evaluating the software engineering capabilities of Large Language Models (LLMs). However, the existing GitHub issue resolution data construction pipeline is challenging and labor-intensive. We identify three key limitations in existing pipelines: (1) test patches collected often omit binary file changes; (2) the manual construction of evaluation environments is labor-intensive; and (3) the fail2pass validation phase requires manual inspection of test logs and writing custom parsing code to extract test status from logs. In this paper, we propose SWE-Factory, a fully automated issue resolution data construction pipeline, to resolve these limitations. First, our pipeline automatically recovers missing binary test files and ensures the correctness of test patches. Second, we introduce SWE-Builder, a LLM-based multi-agent system that automates evaluation environment construction. Third, we introduce a standardized, exit-code-based log parsing method to automatically extract test status, enabling a fully automated fail2pass validation. Experiments on 671 real-world GitHub issues across four programming languages show that our method can effectively construct valid evaluation environments for GitHub issues at a reasonable cost. For example, with GPT-4.1 mini, our SWE-Builder constructs 337 valid task instances out of 671 issues, at $0.047 per instance. Our ablation study further shows the effectiveness of different components of SWE-Builder. We also demonstrate through manual inspection that our exit-code- based fail2pass validation method is highly accurate, achieving an F1 score of 0.99. Additionally, we conduct an exploratory experiment to investigate whether we can use SWE-Factory to enhance models’ software engineering ability. After training five models on 2,809 Python task instances collected by our method, all models show improved software engineering ability. For example, the resolve rate of a trained Qwen2.5-Coder-14B-Instruct on SWE-bench Verified increases from 5.8% to 21.0%. We hope our method can accelerate the construction of large-scale, high-quality GitHub issue resolution datasets for both training and evaluation.

## 46. SWR-Bench: Assessing LLM Performance in Real-World Code Review Comment Generation

**Authors:** Zhengran Zeng (Peking University), Ruikai Shi (Peking University), Keke Han (Peking University), Yixin Li (Peking University), Kaicheng Sun (Northwestern Polytechnical University), Yidong Wang (Peking University), Zhuohao Yu (Peking University), Rui Xie (Peking University), Wei Ye (Peking University), Shikun Zhang (Peking University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808144

**中文总结:** 提出 swrbench，含 1000 个经人工核验的真实 PR、完整项目上下文，以及与人类高度一致（约 90%）的 LLM 客观评测；系统评估显示现有 ACR/LLM 偏弱，而简单多评审聚合可将 F1 最高提升 43.67%。

**Abstract:** Automated Code Review (ACR) is crucial for software quality, yet existing benchmarks often fail to reflect real-world complexities, hindering the evaluation of modern Large Language Models (LLMs). Current benchmarks frequently focus on fine-grained code units, lack complete project context, and use inadequate evaluation metrics. To address these limitations, we introduce swrbench, a new benchmark comprising 1000 manually verified Pull Requests (PRs) from GitHub, offering PR-centric review with full project context. swrbench employs an objective LLM-based evaluation method that aligns strongly with human judgment (~90% agreement) by verifying if issues from a structured ground truth are covered in generated reviews. Our systematic evaluation of mainstream ACR tools and LLMs on swrbench reveals that current systems underperform, and ACR tools are more adept at detecting functional errors. Subsequently, we propose and validate a simple multi-review aggregation strategy that significantly boosts ACR performance, increasing F1 scores by up to 43.67%. Our contributions include the swrbench benchmark, its objective evaluation method, a comprehensive study of current ACR capabilities, and an effective enhancement approach, offering valuable insights for advancing ACR research.

## 47. TLR: Codebase-Level C Memory Management Error Repair with Large Language Models

**Authors:** Xiao Cheng (Macquarie University), Zhihao Guo (UTS), Huan Huo (University of Technology Sydney), Yulei Sui (University of New South Wales)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797085

**中文总结:** 提出 TLR，以 typestate 引导的上下文检索增强 LLM，对 C 代码库级内存管理错误做修复，缓解跨过程推理与上下文窗口限制；在超百万行的 14 个开源项目中修复 49 个真实错误中的 37 个，显著优于 SAVER、ProveNFix 与 SWE-agent，并修复 3 个已获开发者采纳的零日缺陷。

**Abstract:** Memory management errors in C remain a leading source of software vulnerabilities due to the inherent complexity of manual memory handling. Traditional Automated Program Repair (APR) largely relies on rule- or template-based techniques, which require expert-crafted specifications and often struggle to generalize. Recently, Large Language Models (LLMs) have emerged as a complementary approach, leveraging broad exposure to codebases and programming idioms to synthesize fixes that can extend beyond existing templates and rules. This paper introduces TLR, a novel framework that augments LLM-based repair with typestate-guided context retrieval. By using a finite typestate automaton to track error-propagation paths and memory state transitions, our approach provides the LLM with focused, semantically rich context for codebase-level memory error repair, effectively addressing both interprocedural reasoning and LLM context window limitations. Our framework has successfully repaired 37 out of 49 real-world memory errors derived from 14 open-source projects that collectively comprise over a million lines of code. Compared to state-of-the-art memory error APR tools, SAVER and ProveNFix, our approach correctly fixes 14.50× and 2.36× more errors, respectively. Moreover, TLR outperforms current open-source state-of-the-art LLM-based SWE-agent 1.0 by repairing 94% more errors. We have also successfully repaired three critical zero-day memory errors, with fixes that have been accepted and implemented by the original developers. These results highlight a promising paradigm for codebase-level program repair through program analysis-guided, retrieval-augmented LLMs, combining formal verification strengths with neural model adaptability.

## 48. Towards Automated Smart Contract Generation: Evaluation, Benchmarking, and Retrieval-Augmented Repair

**Authors:** Zaoyu Chen, Haoran Qin, Nuo Chen, Xiangyu Zhao, Lei Xue, Xiapu Luo, Xiao-Ming Wu

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797068

**中文总结:** 提出 SolBench（差分模糊强调功能正确性的 Solidity 评测）与 Retrieval-Augmented Repair（RAR），按执行错误检索相关合约片段以低成本补全函数；评测显示缺失合约内关键细节是主失败模式，RAR 在提升准确率同时显著降低上下文开销。

**Abstract:** Smart contracts, predominantly written in Solidity and executed on blockchains like Ethereum, are immutable, making functional correctness paramount: once deployed, bugs and vulnerabilities become permanent. Despite rapid progress in transformer-based code LLMs, existing evaluations of Solidity code completion rely heavily on surface-form metrics (e.g., BLEU, CrystalBLEU) or hand-grading, which poorly correlate with functional correctness. Unlike Python, Solidity lacks large-scale and execution-based benchmarks, hindering systematic assessment and optimization of LLMs for smart contract development.

To bridge this research gap, we introduce \textbf{SolBench}, a comprehensive benchmark and automated testing pipeline for Solidity, designed to emphasize functional correctness via differential fuzzing. SolBench contains 28,825 functions from 7,604 contracts collected from Etherscan (genesis–2024), spanning 10 popular domains. We benchmark 14 diverse LLMs (open/closed, 1.3B–671B parameters, general/code-specific, with/without reasoning). The dominant failure mode is missing crucial details (e.g., type definitions, state variables) in intra-contract context. Providing full-contract context mitigates this and improves code completion accuracy.

However, full-context inference can be prohibitively expensive in practice. Generating outputs with large context windows using state-of-the-art models often incurs significant costs, rendering naive context scaling economically impractical. Crucially, most of a contract is irrelevant to implementing a given function; only a small subset of details is needed. To exploit this, we propose \textbf{Retrieval-Augmented Repair} (RAR), which integrates retrieval into code repair: it uses the executor’s error messages to extract only the most relevant snippets from the full contract. RAR sharply reduces input length for function completion, improving accuracy while significantly cutting computational cost. We further analyze retrieval and code repair strategies within RAR, showing substantial improvements in accuracy and efficiency. SolBench and our RAR framework enable principled evaluation and cost-effective improvement of Solidity code generation. Dataset and code are available at https://anonymous.4open.science/r/SolBench-A144 .

## 49. TransAgent: Enhancing LLM-Based Code Translation via Fine-Grained Execution Alignment

**Authors:** Zhiqiang Yuan (Fudan University), Weitong Chen (Fudan University), Hanlin Wang (Fudan University), Xin Peng (Fudan University), Zhenpeng Chen (Tsinghua University), Yiling Lou (University of Illinois at Urbana-Champaign)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797099

**中文总结:** 提出 TransAgent，通过源–目标代码细粒度执行对齐定位易错块的多 Agent 代码翻译系统；在防泄漏基准上翻译准确率相对 UniTrans 最高提升 33.3%，程序修复平均优于 Agentless 56.7%。

**Abstract:** Code translation transforms code between programming languages while preserving functionality, which is critical in software development and maintenance. While traditional learning-based code translation methods have limited effectiveness due to the lack of sufficient parallel training data, Large Language Models (LLMs) have recently advanced this field with their strong code generation and comprehension capabilities. However, code translated by LLMs still suffers from diverse quality issues, such as syntax and semantic errors. In this work, we propose \ourtool{}, a novel multi-agent system that eliminates the errors during LLM-based code translation. The main insight of \ourtool{} is to localize error-prone code blocks via fine-grained execution alignment between source and target code. We evaluate \ourtool{} on a newly constructed benchmark of recent programming tasks to mitigate data leakage. \ourtool{} outperforms the latest \unitrans{} by up to 33.3% in translation accuracy and achieves an average improvement of 56.7% over \agentless{} in program repair performance. We also conduct an ablation study and evaluate \ourtool{} across different LLMs, demonstrating its effectiveness and strong generalizability.

## 50. TransLibEval: Demystify Large Language Models’ Capability in Third-party Library-targeted Code Translation

**Authors:** Pengyu Xue (Shandong University), Kunwu Zheng (Shandong University), Zhen Yang (Shandong University), Yifei Pei (Shandong University), Linhao Wu (Shandong University), Jiahui Dong (Shandong University), Xiapu Luo (Hong Kong Polytechnic University), Yan Xiao (Sun Yat-sen University), Fei Liu (Shandong University), Yuxuan Zhang (Shandong University), Xiran Lyu (Shandong University), Xianhang Li (Shandong University), Xuanyu Zhu (Shandong University), Chengyi Wang (Shandong University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797137

**中文总结:** 构建首个面向第三方库的代码翻译基准 TransLibEval（200 个跨 Python/Java/C++ 真实任务），系统评估七种 LLM 与六种策略；相对无库场景平均 CA 下降超 60%，并揭示大量此前被掩盖的第三方引用错误。

**Abstract:** In recent years, Large Language Models (LLMs) have been widely studied in the code translation field on the method, class, and even repository levels. However, most of these benchmarks are limited in terms of Third-Party Library (TPL) categories and scales, making TPL-related errors hard to expose and hindering the development of targeted solutions. Considering the high dependence (over 90%) on TPLs in practical programming, demystifying and analyzing LLMs’ code translation performance involving various TPLs becomes imperative.

To address this gap, we construct TransLibEval, the first benchmark dedicated to library-centric code translation. It consists of 200 real-world tasks across Python, Java, and C++, each explicitly involving TPLs from diverse categories such as data processing, machine learning, and web development, with comprehensive dependency coverage and high-coverage test suites. We evaluate seven recent LLMs of commercial, general, and code-specialized families under six translation strategies of three categories: Direct, IR-guided, and Retrievalaugmented. Experimental results show a dramatic performance drop compared with library-free settings (average CA decline over 60%), while diverse strategies demonstrate heterogeneous advantages. Furthermore, we analyze 4,831 failed cases from GPT-4o, one of the State-of-the-Art (SOTA) LLMs, revealing numerous third-party reference errors that were obscured previously. These findings highlight the unique challenges of library-centric translation and provide practical guidance for improving TPL-aware code intelligence.

## 51. Understanding and Predicting Accepted Code Suggestions in AI-Assisted Programming

**Authors:** Jing Jiang (Beihang University), Liehao Li (Beihang University), Jinyun Hou (Beihang University), Xin Tan (Beihang University), Li Zhang (Beihang University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808125

**中文总结:** 基于 6.6 万条工业级开发者–AI 交互，量化分析代码建议被接受与拒绝的特征差异，并提出 CSAP 在展示前预测接受与否；在不平衡/平衡数据上准确率达 0.973/0.922，显著优于 LLM 基线与在产过滤器。

**Abstract:** AI-assisted programming tools are widely adopted, yet their practical utility is often undermined by undesired suggestions that interrupt developer workflows and cause frustration. While existing research has explored developer-AI interactions when programming qualitatively, a significant gap remains in quantitative analysis of developers’ acceptance of AI-generated code suggestions, partly because the necessary fine-grained interaction data is often proprietary. To bridge this gap, this paper conducts an empirical study using 66,329 industrial developer-AI interactions from a large technology company. We analyze features that are significantly different between accepted code suggestions and rejected ones. We find that accepted suggestions are characterized by significantly higher historical acceptance counts and ratios for both developers and projects, longer generation intervals, shorter preceding code context in the project, and older IDE versions. Based on these findings, we introduce \emph{CSAP} (Code Suggestion Acceptance Prediction) to predict whether a developer will accept the code suggestion before it is displayed. Our evaluation of \emph{CSAP} shows that it achieves the accuracy of 0.973 and 0.922 on imbalanced and balanced dataset respectively. Compared to a large language model baseline and an in-production industrial filter, \emph{CSAP} relatively improves the accuracy by 12.6% and 69.5% on imbalanced dataset, and improves the accuracy by 87.0% and 140.1% on balanced dataset. Our results demonstrate that targeted personalization is a powerful approach for filtering out code suggestions with predicted rejection and reduce developer interruption. To the best of our knowledge, it is the first quantitative study of code suggestion acceptance on large-scale industrial data, and this work also sheds light on an important research direction of AI-assisted programming.

## 52. Understanding, Detecting, and Repairing Real-World In-Context-Learning-Based Text-to-SQL Errors

**Authors:** Jiawei Shen (East China Normal University), Chengcheng Wan (East China Normal University), Ruoyi Qiao (East China Normal University), Jiazhen Zou (East China Normal University), Hang Xu (East China Normal University), Yuchen Shao (East China Normal University, Shanghai Innovation Institute), Yueling Zhang (East China Normal University), Weikai Miao (East China Normal University), Geguang Pu (East China Normal University, China)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808171

**中文总结:** 首次全面研究 ICL 式 Text-to-SQL 错误，归纳 7 类共 27 种错误类型，并发现现有修复开销高、误修多；提出 MapleDoctor，多修 13.8% 查询、几乎无误修且开销降低 67.4%。

**Abstract:** Large language models (LLMs) have been adopted for text-to-SQL tasks, utilizing their in-context learning (ICL) capability to translate natural language questions into SQL queries. However, such a technique faces correctness problems. In this paper, we conduct the first comprehensive study of text-to-SQL errors of ICL-based techniques. Our study covers four representative ICL-based techniques, five basic repairing methods, two benchmarks, and two LLM settings. We find that text-to-SQL errors are widespread and summarize 27 error types of 7 categories. We also find that existing repairing attempts have limited correctness improvement while having high computational overhead and many mis-repairs. Based on these findings, we propose MapleDoctor, a novel text-to-SQL error detection and repairing framework. The evaluation demonstrates that MapleDoctor outperforms existing solutions by repairing 13.8% more queries with neglectable mis-repairs and reducing 67.4% overhead. The artifact is publicly available at GitHub.

## 53. Unfulfilled Promises: LLM-Based Detection of OS Compatibility Issues in Infrastructure as Code

**Authors:** Georgios-Petros Drosos (ETH Zurich), Georgios Alexopoulos (University of Athens), Thodoris Sotiropoulos (ETH Zurich), Dimitris Mitropoulos (University of Athens), Zhendong Su (ETH Zurich)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797097

**中文总结:** 提出 crOSsible，用 LLM 从模块文档合成/修复集成测试并在 8 大 Linux 发行版 13 个版本上做跨 OS 测试；12 小时内在 259 个热门 Ansible 模块中发现 36 个未知缺陷（含 22 个可移植性问题），平均覆盖率提升 12.3%。

**Abstract:** Modern infrastructures rely on Infrastructure as Code (IaC) systems to keep complex deployments consistent, reproducible, and scalable at production scale. The reliability of these infrastructures, however, depends on the correctness of their building blocks, which are reusable components (modules) that each performs a dedicated task, such as installing a package, managing an OS user, or configuring a service, and reconciling its state with the desired specification. A central promise of these components is portability: a specification written once should correctly manage the targeted resource on every OS the IaC component supports. When this property is violated, defects can propagate across entire infrastructures, causing outages, security vulnerabilities, and costly misconfigurations.

In this work, we introduce crOSsible, the first automated framework for cross-OS testing of IaC modules. crOSsible leverages large language models (LLMs) to synthesize and repair integration tests from structured module documentation, and executes them across 13 versions of 8 major Linux distributions. While our techniques are generally applicable to different IaC systems, we instantiate and evaluate them on Ansible, the most widely used IaC framework for managing individual servers. Evaluation across 259 popular Ansible modules demonstrates both effectiveness and real-world impact. In just 12 hours of testing, crOSsible uncovered 36 previously unknown bugs, including 22 portability violations. In total, 27 issues have been confirmed by maintainers, with 11 already fixed. The discovered issues range from crashes to dangerous soundness defects where modules reported success despite leaving systems misconfigured. Beyond bug discovery, crOSsible improved the code coverage of Ansible modules by 12.3% on average, systematically exercising OS-specific code paths that existing tests missed.

## 54. UNICS: Multilingual Code Search via Unified Pseudocode and Contrastive Transfer Learning

**Authors:** Ye Fan (Nanjing University), Jidong Ge (Nanjing University), Chuanyi Li (Nanjing University), Liguo Huang (Southern Methodist University), Bin Luo (Nanjing University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797067

**中文总结:** 提出 UNICS：先以伪代码统一表示预训练跨语言算法级语义，再经切片多任务迁移并挖掘 hard positive/动态 hard negative；在多语言与跨语言基准上达 SOTA，零样本迁移到低资源语言表现更均衡。

**Abstract:** While pre-trained models have achieved remarkable success in code search, their multilingual capabilities remain a major hurdle, plagued by data imbalance, cross-lingual semantic interference, and the loss of critical information from existing unified representations like Abstract Syntax Trees (ASTs) or Intermediate Representations (IRs). Furthermore, conventional contrastive learning strategies often rely on simplistic hard negative sampling while overlooking the potential of mining hard positives to learn code’s intrinsic semantic invariance. To address these challenges, we introduce UNICS, a framework for multilingual code search built on a two-stage training strategy. In the first stage, UNICS is pre-trained on a novel dataset we constructed, which uses pseudo-code as a unified representation to learn a cross-lingual, algorithm-level logic that preserves full semantic fidelity. The second stage employs a multi-task transfer learning strategy that adapts this general knowledge to specific languages by decomposing code into semantic slices (e.g., API calls, function bodies) and incorporating tasks for hard positive mining and cross-lingual dynamic hard negative sampling. Experimental results demonstrate that UNICS achieves state-of-the-art performance across multiple multilingual and cross-lingual benchmarks, showcasing superior generalization and performance balance, especially in zero-shot transfer tasks to low-resource languages.

## 55. Validating LLM-Generated SQL Queries Through Metamorphic Prompting

**Authors:** Li Lin (Zhejiang University), Qinglin Zhu (School of Informatics, Xiamen University), Jintai Hong (School of Informatics, Xiamen University), Chong Wang (Nanyang Technological University), Yang Liu (Nanyang Technological University), Rongxin Wu (Xiamen University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797146

**中文总结:** 提出 MRSQLGen，基于幻觉分类的变形提示改写输入，并藉蜕变关系与多次执行行为一致性（多数投票）检测意图违背型 SQL 幻觉；在 Spider 与 Bird 上对五种 LLM 的检测精确率与召回均优于现有方法。

**Abstract:** Large Language Models (LLMs) can translate natural language (NL) into SQL, enabling non-experts to query databases via conversational interfaces. However, the generated SQL often contains intent-violating hallucinations—queries that are syntactically valid and executable, yet semantically misaligned with the user’s question. These failures are especially risky in real-world settings where users cannot verify the correctness.

In this paper, we propose MRSQLGen, a framework for detecting intent-violating hallucinations, built on the metamorphic prompting paradigm. MRSQLGen rewrites the input prompt using task-specific transformation rules derived from a hallucination taxonomy, and validates the generated SQL by checking behavioral consistency across multiple executions. Each transformation is associated with a metamorphic relationship (MR) that defines the expected relation between results; discrepancies are aggregated through a majority-vote strategy to robustly flag hallucinations without ground-truth SQL. We evaluate MRSQLGen on two benchmarks (Spider and Bird) using five representative LLMs, including GPT-4o. Experimental results demonstrate that MRSQLGen consistently outperforms state-of-the-art hallucination detection techniques, achieving higher precision and recall in detecting hallucinated SQL queries.

## 56. VerilogASTBench: Benchmark Construction of Verilog AST Dataset with Dual-Stage AST Semantic Enhancement Framework

**Authors:** luping zhang (Nanjing University of Posts and Telecommunications), Chao Chen (Nanjing University of Posts and Telecommunications), Dapeng Yan (Nanjing University of Posts and Telecommunications), Hui Xu (Shenzhen Institute for Advanced Study, University of Electronic Science and Technology of China), Mingsheng Cao (University of Electronic Science and Technology of China), Jingkuan Song (University of Electronic Science and Technology of China), Zhikuang Cai (Nanjing University of Posts and Telecommunications), Yufeng Guo (Nanjing University of Posts and Telecommunications)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797073

**中文总结:** 提出基于 AST 的 Verilog 语义增强解析与自动修复框架，结合静态分析角色推断、结构化提示生成描述与编译器反馈修复；成功修复 15.24% 缺陷代码并构建 31.8 万样本 RTL 基准，微调模型在多评测上显著提升。

**Abstract:** With the increasing complexity and scale of integrated circuit (IC) designs, automated circuit design methods are essential for Verilog implementation. Although Large Language Models (LLMs) perform well in general-purpose coding such as C++ and Python, their performance in Verilog is constrained by domain-specific semantic and structural rules as well as the scarcity of high-quality training datasets. To address these issues, this work proposes a semantically enhanced Verilog code parsing and automatic repair framework based on Abstract Syntax Tree (AST). First, an advanced register-transfer level (RTL) analysis framework was developed to achieve semantic enhancement through static analysis–driven functional role inference and attribute annotation. Second, enhanced AST information is used to construct structured prompts and generate semantically rich module descriptions via an Application Programming Interface (API) for dataset construction. Finally, an AST-guided automatic Verilog repair framework was designed, which leverages enhanced AST analysis for precise defect localization and intelligent repair through compiler feedback loops. Experimental results indicate that the proposed method successfully repaired 15.24% of defective Verilog code, resulting in a high-quality RTL benchmark dataset containing 318,021 samples. Models fine-tuned on this dataset demonstrate significant performance improvements across three benchmarks, achieving average improvements of 13.76% and 16.95% on Eval-Machine pass@1 and pass@5, 8.97% and 14.56% on Eval-Human pass@1 and pass@5, and 15.70% and 12.20% on RTLLM V1.1 Syntax-VCS and Func.

## 57. ViBR: Automated Bug Replay from Video-based Reports Using Vision-Language Models

**Authors:** Sidong Feng (Monash University), Dingbang Wang (University of Connecticut), Nikola Tomic (Technical University of Munich), Tingting Yu (University of Connecticut), Aldeida Aleti (Monash University), Chunyang Chen (TU Munich)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808152

**中文总结:** 提出 ViBR，结合 CLIP 动作分割与 VLM 区域感知 GUI 状态对比，从界面录屏直接自动复现缺陷而无需触摸指示或预建 UI 图；成功复现 73.7% 的缺陷录屏，显著优于现有基线。

**Abstract:** Bug reports play a critical role in software maintenance by helping users convey encountered issues to developers. Recently, GUI screen capture videos have gained popularity as a bug reporting artifact due to their ease of use and ability to retain rich contextual information. However, automatically reproducing bugs from such recordings remains a significant challenge. Existing methods often rely on fragile image-processing heuristics, explicit touch indicators, or pre-constructed UI transition graphs, which require non-trivial instrumentation and app-specific setup. This paper presents ViBR, a lightweight and fully automated approach that reproduces bugs directly from GUI recordings. Specifically, ViBR combines CLIP-based embedding similarity for action segmentation with Vision-Language Models (VLMs) for region-aware GUI state comparison and guided bug replay. Experimental results show that ViBR successfully reproduces 73.7% of bug recordings, significantly outperforming state-of-the-art baselines and ablation variants.

## 58. VisionScratch: LLM-Based Automated Feedback Generation Using Code-Produced Videos for Scratch Programs

**Authors:** Yuan Si (University of Waterloo), Daming Li (Independent Researcher), Hanyuan Shi (N/A), Jialu Zhang (University of Waterloo)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808163

**中文总结:** 提出 VisionScratch，首个同时利用 Scratch 积木代码与游戏运行视频的多模态反馈系统，经视觉–语言对齐定位关键问题并做最小 AST 级修复与 VM 验证；在真实项目上识别与修复质量显著优于现有 LLM 工具。

**Abstract:** Block-based programming environments such as Scratch are increasingly popular in programming education, in particular for young learners. While the use of blocks helps prevent syntax errors, semantic bugs remain common and difficult to debug. Existing tools for Scratch debugging rely heavily on predefined rules or user manual inputs, and crucially, they ignore the platform’s inherently visual nature.

We introduce VisionScratch, the first multimodal feedback generation system for Scratch that leverages both the project’s block code and its generated gameplay video to diagnose and repair bugs. VisionScratch uses a two-stage pipeline: a vision-language model first aligns visual symptoms with code structure to identify a single critical issue, then proposes minimal, abstract syntax tree level repairs that are verified via execution in the Scratch virtual machine.

We evaluate VisionScratch on a set of real-world Scratch projects against state-of-the-art LLM-based tools and human testers. Results show that gameplay video is a crucial debugging signal: VisionScratch substantially outperforms prior tools in both bug identification and repair quality, even without access to project descriptions or goals. This work demonstrates that video can serve as a first-class specification in visual programming environments, opening new directions for LLM-based debugging beyond symbolic code alone.
