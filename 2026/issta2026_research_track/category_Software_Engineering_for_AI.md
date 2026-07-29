# ISSTA 2026 Research Track — Software Engineering for AI

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 37

## 1. AgentInspect: Diagnosing Behavioral Failures in Artificial Intelligence Agents

**Authors:** Ruchira Manke (Tulane University), Mohammad Wardat (Oakland University, USA), Foutse Khomh (Polytechnique Montréal), Hridesh Rajan (Tulane University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 AgentInspect 框架，结合覆盖率引导输入生成、工具行为模拟与确定性轨迹分析，自动检测 LangChain Agent 的六类行为失效。在 35 个 GitHub Agent 上高精确率、高召回率识别关键鲁棒性缺陷，模拟环境可暴露真实工具响应下未出现的失效模式。

**Abstract:** Effectively testing Artificial Intelligence (AI) agents remains a fundamental challenge due to their stochastic reasoning, vast and diverse input space, reliance on external tools, and operation in dynamic execution environments; factors that demand new testing methodologies explicitly tailored to the complex and interactive nature of agent-based systems. This work presents a novel methodology for testing AI agents, with a particular focus on assessing their behavioral robustness under varied operational conditions. Our approach relies on following key technical innovations: (1) a coverage-guided test input generation strategy based on agent-specific coverage criteria, (2) a capture-and-simulate mechanism that systematically emulates abnormal tool behaviors to mimic real-world execution failures, and (3) a deterministic behavioral failure detection approach that enables consistent identification of failures across different test inputs. We developed AgentInspect, a framework that automatically detects six categories of behavioral failures in LangChain-based AI agents by analyzing their execution trajectories across two evaluation settings: a baseline setting using real tool responses and a simulated setting incorporating synthetic tool responses. To evaluate our approach, we curated a benchmark of 35 AI agents obtained from GitHub. Our results show that AgentInspect consistently identifies different behavioral failures with high precision and recall across both baseline and simulated execution settings. In particular, the simulated setting exposes failure modes that do not emerge during baseline execution with real tool responses, thereby enabling a more comprehensive assessment of agent robustness. Our findings highlight AgentInspect’s effectiveness in revealing critical failures and its practical utility for systematic robustness evaluation of AI agents.


## 2. ARQ: A Mixed-Precision Quantization Framework for Accurate and Certifiably Robust DNNs

**Authors:** Yuchen Yang (University of Illinois Urbana-Champaign), Yifan Zhao (University of Illinois Urbana-Champaign), Shubham Ugare (University of Illinois Urbana-Champaign / Meta), Gagandeep Singh (University of Illinois Urbana-Champaign), Sasa Misailovic (University of Illinois Urbana-Champaign)

**Categories:** Software Engineering for AI

**中文总结:** 提出混合精度量化框架 ARQ，利用强化学习结合 randomized smoothing 在压缩 DNN 的同时保持可证明鲁棒性。量化后模型在约 1.5% 指令开销下达到与原浮点模型相当的精度与认证半径。

**Abstract:** Mixed precision quantization has become an important technique for optimizing the execution of deep neural networks (DNNs). Certified robustness, which provides provable guarantees about a model’s ability to withstand different adversarial perturbations, has rarely been addressed in quantization due to the unacceptably high cost of certifying robustness. This paper introduces ARQ, an innovative mixed-precision quantization method that not only preserves the clean accuracy of the smoothed classifiers, but also maintains their certified robustness. ARQ uses reinforcement learning to find accurate and robust DNN quantization, while efficiently leveraging randomized smoothing, a popular class of statistical DNN verification algorithms. ARQ consistently performs better than multiple state-of-the-art quantization techniques across all the benchmarks and the input perturbation levels. The performance of ARQ quantized networks reaches that of the original DNN with floating-point weights, while with only$~1.5%$ instructions and the highest certified radius. ARQ code is available at https://anonymous.4open.science/r/ARQ-35CB .


## 3. A Temporal Reasoning Benchmarking Framework for LRMs via Difficulty-controlled and Dynamic Test Generation

**Authors:** shide zhou (Huazhong University of Science and Technology), Kailong Wang (Huazhong University of Science and Technology), Ling Shi (Nanyang Technological University), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI

**中文总结:** 提出 TRACE 测试框架，以 Allen 区间代数建模时序推理并支持难度可控的动态测试生成与 trace 验证。在 TRACEBench 上模型性能与难度强负相关（r≈−0.97），并发现中型模型约 28% 的答案属于虚假猜测。

**Abstract:** Defining the reasoning boundaries and ensuring the reliability of Large Reasoning Models (LRMs) remains a critical challenge. Current benchmarks primarily rely on static datasets susceptible to data contamination or synthetic tasks lacking fine-grained difficulty control. Furthermore, standard outcome-based evaluations often conceal reasoning flaws by neglecting the reasoning process. To address these limitations, we introduce TRACE, a testing framework that models temporal reasoning as constraint satisfaction problems via Allen’s Interval Algebra. This approach enables precise regulation of logical complexity and incorporates a Trace-Based Verification Oracle to validate reasoning faithfulness. Using this framework, we construct TRACEBench, an extensive benchmark comprising 1,200 synthesized test instances across graded difficulty levels. We employ TRACE to evaluate six widely used LRMs on TRACEBench. The results confirm a strong negative correlation between model performance and our difficulty metric (Pearson’s 𝑟 ≈ −0.97), validating the effectiveness of our difficulty control mechanism. Moreover, our trace-based analysis exposes significant discrepancies between reasoning validity and final answers, revealing a high spurious guessing rate of approximately 28% in mid-sized models. In addition, we diagnose scale-dependent failure modes, ranging from Degenerative Loops in small models to Reasoning Explosion in advanced architectures. TRACE thus provides a robust, automated platform for benchmarking the true temporal reasoning capabilities of LRMs.


## 4. CAST: A Compiler-Based Framework for Systematically Testing LLM Compositional Safety

**Authors:** Lu Yan (Purdue University), Zhuo Zhang (Columbia University), Xiangzhe Xu (Purdue University), Shengwei An (Virginia Tech), Guangyu Shen (Purdue University), Zhou Xuan, Xuan Chen (Purdue University), Xiangyu Zhang (Purdue University)

**Categories:** Software Engineering for AI

**中文总结:** CAST 提出组合式安全测试框架，通过编译器式中间表示 CAIR 将恶意代码生成意图分解为可重组的子任务，系统评估 LLM 在长程多步工作流中的安全性。在四个前沿 LLM 上成功测试用例数较基线最高增加 365%。

**Abstract:** Large language models (LLMs) are increasingly used in software pipelines, raising concerns about harmful behaviors in security-critical domains. Existing safety evaluations predominantly probe models with single prompts or short interactions, and therefore do not capture how safety behaves under multi-step workflows where individual requests are composed into complex behavior. This paper introduces compositional safety, the property that an LLM remains safe not only against isolated malicious prompts, but also under structured, long-horizon decompositions of harmful intents. we propose CAST, a systematic testing framework designed to evaluate the compositional safety of LLMs in the domain of malicious code. Drawing inspiration from modern compiler infrastructures, CAST decouples test case generation from test execution using a novel intermediate representation, CAIR. This architecture allows the framework to automatically refine high-level testing intents into granular sub-tasks that serve as unit tests for the model’s alignment. These components are subsequently instantiated by the System Under Test (SUT) and reassembled to verify if the model can be driven to realize the original harmful goal. We evaluate CAST on four state-of-the-art LLMs across three security-critical testbeds. Our results demonstrate that CAST systematically exposes severe safety violations in strongly aligned models that resist conventional red-teaming, achieving up to a 365% increase in successful test cases compared to baseline testing strategies.


## 5. CID: Clean-Seed-Free Backdoor Defense via Counterfactual Invariance for Neural Code Models

**Authors:** Junyao Ye (Huazhong University of Science and Technology), Zhen Li (Huazhong University of Science and Technology), Xi Tang (Huazhong University of Science and Technology), Shulin Li (Huazhong University of Science and Technology), Shi Liang (Huazhong University of Science and Technology), Deqing Zou (Huazhong University of Science and Technology), Hai Jin (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI

**中文总结:** CID 无需预先可信干净种子集，利用语义充分性与触发器必要性两类反事实探针从混合数据中提取高纯度干净样本，再基于 Mahalanobis 聚类检测神经代码模型后门。在四种 SE 任务与三种架构上表现优于现有防御基线。

**Abstract:** Neural code models, which automate foundational software engineering tasks such as code classification and generation, are critically vulnerable to backdoor attacks. Yet, existing defenses face a dual failure: they struggle with sophisticated threats spanning injection-based and semantically-equivalent transformation (\textit{SET-based}) backdoor attacks, and they rely on a restrictive assumption—a trusted, pre-verified \emph{in-distribution} clean seed set—that can be costly and difficult to obtain and audit in practice. This paper introduces Counterfactual Invariance-based Defense (CID), a clean-seed-free backdoor defense—requiring no \emph{a priori} trusted \emph{in-distribution} clean data—grounded in \emph{operational} counterfactual invariance tests. CID’s core insight is that clean and poisoned samples exhibit \emph{asymmetric counterfactual behavior}: clean predictions degrade under semantic context corruption (semantic sufficiency), whereas backdoor predictions change when a localized trigger is neutralized (trigger necessity). Accordingly, CID applies two orthogonal probes—a contextual intervention to test semantic sufficiency and a structural neutralization test guided by a gradient-based probe to test trigger necessity—to extract a high-purity clean seed set directly from a mixed dataset. This seed set then enables Mahalanobis-based clustering in representation space to partition the full dataset. Evaluated across four software engineering tasks and three model architectures, and further validated on multilingual code summarization, CID achieves strong poison detection performance among evaluated baselines while keeping false positives low in most settings. By eliminating reliance on \emph{a priori} trusted \emph{in-distribution} clean seed data, CID provides a practical pathway toward more secure deployment of neural code models.


## 6. Code-MUE: Measuring Code LLM' Uncertainty through Execution-based Semantic Interaction Graphs

**Authors:** xiaoning ren, Yinxing Xue (Institute of AI for Industries, Chinese Academy of Sciences), Lei Ma (The University of Tokyo & University of Alberta), Yuheng Huang (The University of Tokyo)

**Categories:** Software Engineering for AI

**中文总结:** Code-MUE 基于执行结果构建语义交互图，用 Von Neumann 熵量化 Code LLM 输出的语义不确定性，无需访问模型内部。在八个 LLM 上与功能正确性的 Spearman 相关最高达 -0.98，显著优于文本与嵌入基线。

**Abstract:** As Code Large Language Models (LLMs) become central to modern software engineering, their inherent stochasticity poses significant real-world risks, where even minor errors can lead to severe functional, security, or safety consequences. Reliable automation, therefore, demands the ability to distinguish between confident, well-supported predictions and stochastic guessing. However, existing uncertainty estimation methods face a critical gap: white and grey-box techniques are often inapplicable to closed-source models, while standard “black-box” text metrics fail to capture the unique fragility of code, where syntactic variation does not always imply semantic divergence. To bridge this syntax-semantics gap, we introduce Code-MUE, a purely black-box framework that measures uncertainty through execution-based Semantic Interaction Graphs. Unlike prior approaches that rely on superficial textual similarity, Code-MUE grounds uncertainty in observable runtime behavior, calculating the Von Neumann entropy of the solution space to quantify global semantic diversity. A large-scale empirical study across eight state-of-the-art LLMs demonstrates that Code-MUE achieves a strong negative correlation with functional correctness (Spearman’s correlation up to -0.98), significantly outperforming lexical and embedding-based baselines while enabling robust risk detection and selective prediction in practical workflows.


## 7. CONCUR: Benchmarking LLMs for Concurrent Code Generation

**Authors:** Jue Huang (University of Queensland), Tarek Mahmud (Assistant Professor, Texas A&M University-Kingsville), Corina S. Păsăreanu, Guowei Yang (University of Queensland)

**Categories:** Software Engineering for AI

**中文总结:** CONCUR 构建面向并发代码生成的评测基准，含 43 道教材级并发题及 72 个变异体共 115 题，覆盖死锁、竞态等并发特有缺陷。对多种 LLM 的评估揭示当前模型在并发代码生成上的显著不足。

**Abstract:** Leveraging Large Language Models (LLMs) for code generation has increasingly emerged as a common practice in the domain of software engineering. Relevant benchmarks have been established to evaluate the code generation capabilities of LLMs. However, existing benchmarks focus primarily on sequential code, lacking the ability to effectively evaluate LLMs on concurrent code generation. Compared to sequential code, concurrent code exhibits greater complexity and possesses unique types of bugs, such as deadlocks and race conditions, that do not occur in sequential code. Therefore, a benchmark for evaluating sequential code generation cannot be useful for evaluating concurrent code generation with LLMs. To address this gap, we designed a benchmark CONCUR specifically aimed at evaluating the capability of LLMs to generate concurrent code. CONCUR consists of a base set of 43 concurrency problems derived from a standard concurrency textbook, together with 72 validated mutant variants, resulting in 115 total problems. The base problems serve as the semantic core of the benchmark, while the mutants expand linguistic and structural diversity. We conducted an evaluation of a range of LLMs on CONCUR, highlighting limitations of current models. Overall, our work provides a novel direction for evaluating the capability of LLMs to generate code with focus on concurrency.


## 8. Contamination Means Overestimation? A Fine-grained Empirical Study in Code Intelligence

**Authors:** Zhen Yang (Shandong University), Hongyi Lin (Shandong University), Yifan He (Shandong University), Junqi Wang (Shandong University), Zeyu Sun (National Key Laboratory of Space Integrated Information System, Institute of Software, Chinese Academy of Sciences), Shuo Liu, Jie Xu (Shandong University), Pengpeng Wang (Columbia University), Zhongxing Yu (Shandong University), Qingyuan Liang (Peking University)

**Categories:** Software Engineering for AI

**中文总结:** 本文细粒度划分 input-only、output-only、unpaired、paired 四类数据污染场景，系统评估 RoBERTa、GPT-2、LLaMA、StarCoder 在代码翻译、生成与摘要任务上的影响。发现污染并非必然导致性能高估，LLM 在 paired 污染下受影响最显著。

**Abstract:** In recent years, code intelligence has gained increasing importance in the field of automated software engineering. Meanwhile, the widespread adoption of Pretrained Language Models (PLMs) and Large Language Models (LLMs) has raised concerns regarding data contamination and its potential impact on model performance evaluation. Previous studies mainly focused on sample-level contamination, ignoring partial contamination scenarios that are pervasive in code intelligence. This paper fills this gap and presents a systematic empirical study to investigate the fine-grained data contamination on mainstream code tasks. Our study involves diverse representative PLMs: RoBERTa and GPT-2, and LLMs: LLaMA and StarCoder, covering three major tasks: code translation, code generation, and code summarization, across two Programming Languages (PLs): Java and Python. We categorize contamination scenarios into four types according to the code intelligence practice, namely input-only, output-only, unpaired, and paired contamination settings, and construct corresponding experimental and control groups for exploration.

Experimental results show that, under the pre-training, fine-tuning, and inference paradigm adopted by PLMs, even deliberately injecting paired contamination does not lead to significant performance overestimation. But direct inference or small-scale fine-tuning uncovers the contamination effects. In contrast, LLMs with pre-training and inference paradigm are significantly affected by the paired contamination. Apart from the above, other contamination scenarios have no impact on both PLMs and LLMs. Our findings challenge the conventional belief that contamination inevitably leads to performance overestimation, providing new insights into the evaluation and deployment of code intelligence models.


## 9. Cracking Query Bottlenecks: Towards Efficiency-Oriented Text-to-SQL Generation

**Authors:** Li Lin (Zhejiang University), Yunfeng Shen (Zhejiang University), Lingfeng Bao (Zhejiang University), Rongxin Wu (Xiamen University), Yang Liu (Nanyang Technological University)

**Categories:** Software Engineering for AI

**中文总结:** EESQLBench 为 Text-to-SQL 引入专家优化 SQL 作为效率基准，用 Cost Reachability 等指标同时评估正确性与查询开销。六种 LLM 虽语义正确率高，但在查询效率上存在显著差距，常出现缺失访问剪枝等问题。

**Abstract:** Text-to-SQL models translate natural language questions into SQL, enabling non-technical users to access databases. However, most existing research focuses on correctness, neglecting query efficiency. In this paper, we address the challenge of evaluating the execution efficiency of generated SQL in Text-to-SQL by introducing EESQLBench, a novel benchmark designed to assess both correctness and efficiency. EESQLBench pairs each natural language question with an expert-optimized SQL query, providing a reliable efficiency baseline. We evaluate six representative large language models (LLMs), including four open-source models (SQLCoder, CodeLlama, DeepSeek-Coder, and DeepSeek-R1) and two closed-source models (GPT-5.2 and Gemini-2.5-Pro), using cost-based metrics including Cost Reachability (CR) and Acceptable Reachability at $k$ (AR@$k$). Our results reveal that current LLMs, despite achieving high correctness, struggle to produce efficient queries. We observe substantial efficiency gaps between models and emphasize that semantic correctness alone does not guarantee query efficiency. Furthermore, we provide insights into common inefficiency patterns in LLM-generated SQL queries, such as missing access pruning and inefficient subquery logic.


## 10. Datura: Progressive Red Teaming Testing for Tool Invocation Chain in LLM Agents

**Authors:** Yuchen Shao (East China Normal University, Shanghai Innovation Institute), Ziqun Bao (East China Normal University), Yuheng Huang (The University of Tokyo), Yuling Shi (Shanghai Jiao Tong University), Mingyu Weng (East China Normal University), Yiwen Sun (East China Normal University), Long Yang (East China Normal University, Shanghai Innovation Institute), Lei Ma (The University of Tokyo & University of Alberta), Ting Su (East China Normal University), Chengcheng Wan (East China Normal University)

**Categories:** Software Engineering for AI

**中文总结:** Datura 通过五阶段工作流对 LLM Agent 的工具调用链进行渐进式红队测试，每步输入看似合法但串联达成有害目标。在五种 LLM 与五种防御机制下攻击成功率达 94.86%–99.59%，显著优于现有基线。

**Abstract:** LLM agents that invoke external tools face critical safety vulnerabilities when malicious manipulations exploit their implicit trust in tool outputs and metadata. However, identifying these vulnerabilities through testing is challenging due to the need to bypass safety guardrails with semantically legitimate inputs, the difficulty in characterizing successful attacks amid implicit tool trust, and the requirement to maintain logical consistency across fragile state-dependent execution chains.

In this paper, we first conduct an empirical study to investigate how external tools influence the reasoning of agents. Guided by the findings, we propose Datura, an automated red teaming testing framework that exposes safety vulnerabilities through chained tool manipulation. Through a five-stage workflow, Datura dynamically generates test cases where each individual step appears legitimate yet collectively achieves harmful outcomes. We evaluate Datura across five LLMs and 740 safety-critical tasks under five defense including real-world safety mechanisms. Datura achieves 94.86–99.59% attack success rate, outperforming the strongest baseline by 7.56–24.32 percentage points, and maintains 78.78–95.54% effectiveness across defenses where baselines drop to near-zero. The artifact is available on Anonymous GitHub.


## 11. DDOR: Delta Debugging for Explainable Overrefusal Testing and Repair

**Authors:** Zhou Qinyan (Southeast University), Peixin Zhang (Singapore Management University), Jun Sun (Singapore Management University), Haonan Zhang (Zhejiang University), Dongxia Wang (Zhejiang University)

**Categories:** Software Engineering for AI

**中文总结:** DDOR 用 delta debugging 在黑盒设置下定位触发过度拒绝的最小片段 mRTF，并据此生成规模化过度拒绝测试集与定向 prompt 修复方案。可在保持有害输入安全性的同时显著降低 LLM 对良性查询的误拒率。

**Abstract:** While safety alignment and guardrails help large language models (LLMs) avoid harmful outputs, they can also induce overrefusal, i.e., unwarranted rejection of benign queries that merely appear risky. We present DDOR (Delta Debugging for OverRefusal), a fully automated and causally grounded framework for overrefusal testing and repair in a black-box setting, where only model inputs and outputs are accessible and internal safety mechanisms remain opaque. DDOR applies delta debugging to localize minimal refusal-triggering fragments (mRTFs) that provide phrase-level, explainable evidence for why a refusal occurs. Conditioned on these mRTFs, DDOR generates diverse, context-rich prompts and performs multi-oracle validation to filter intrinsically unsafe or ambiguous cases, producing scalable and model-specific overrefusal test suites (approximately 1K cases per model). Beyond evaluation, we further leverage localized mRTFs to perform targeted prompt repair, substantially reducing overrefusal while preserving the original intent and maintaining safety on genuinely harmful inputs. Overall, DDOR offers a practical end-to-end solution to both evaluate and mitigate overrefusal, improving LLM usability without sacrificing safety.


## 12. Do Large Language Models Understand Code like Humans?

**Authors:** Xiaokai Rong (University of Texas at Dallas), Aashish Yadavally (University of Central Florida), Hridya Dhulipala (University of Texas at Dallas), Anh H. N. Nguyen, Tien N. Nguyen

**Categories:** Software Engineering for AI

**中文总结:** 本文引入语义自一致性等代理指标量化模型代码可理解性，并与多组人类评分对比。LLM 与专业开发者理解性对齐最强，但与不同经验学生群体对齐较弱，角色条件 prompt 无法改善后者。

**Abstract:** Code understandability is a critical aspect of software quality. Prior research has largely focused on this attribute from a human-centric perspective, while it should be viewed as a relational property arising from the interaction between a reader and the code. With the increasing adoption of large language models (LLMs) in software engineering, we posit that the notion of “reader” should be generalized to encompass both humans and models. Building on this relational perspective, we extend the concept of code understandability to distinguish between human and model code understandability, aiming to investigate the alignment between the two. To this end, we use a dataset from a prior study containing human-rated judgments of understandability across diverse participant groups, and evaluate multiple open and closed-source LLMs. To operationalize model code understandability, we introduce four proxies: P0, based on program comprehension-focused question answering; and P1–P3, based on program intent summarization (derived from our proposed semantic self-consistency). Our findings show that LLMs exhibit stronger alignment with general human code understandability than previously used shallow machine learning baselines. Stratified analyses further reveal that model code understandability aligns most closely with professional developers, but significantly less with other student groups. Role-conditioned prompting does not improve the alignment for the latter, suggesting that current LLMs cannot accurately mimic the perspectives of human readers with varying expertise. Finally, we demonstrate that semantic self-consistency is a reliable and extensible measure for quantifying model code understandability, with broad implications in both software engineering research and practice.


## 13. Don’t Use a Cannon to Kill a Fly: Lightweight Model Editing for LLMs to Correct Deprecated API Recommendations

**Authors:** Guancheng Lin (City University of Hong Kong), Xiao Yu (Zhejiang University), Jacky Keung (City University of Hong Kong, Hong Kong SAR China), Xing Hu (Zhejiang University), Xin Xia (Zhejiang University), Alex X. Liu

**Categories:** Software Engineering for AI

**中文总结:** 本文在 EDAPIBench 上系统评估 10 种模型编辑方法更新 LLM 中过时 API 知识的效果，并提出 AdaLoRA-L 仅编辑 API 特定层以保护通用知识。AdaLoRA-L 在生成最新 API 的同时显著改善编辑特异性。

**Abstract:** Pre-trained or fine-tuned on large code corpora, Large Language Models (LLMs) have demonstrated strong performance in code completion tasks. However, their embedded knowledge is constrained by the timeliness of training data, which often includes code using deprecated APIs. Consequently, LLMs frequently generate deprecated APIs that will no longer be supported in future versions of third-party libraries. While retraining LLMs on updated codebases could refresh their API knowledge, this approach is computationally expensive. Recently, lightweight model editing methods have emerged to efficiently correct specific knowledge in LLMs. However, it remains unclear whether these methods can effectively update deprecated API knowledge and enable edited models to generate up-to-date APIs. To address this gap, we conduct the first systematic study applying 10 state-of-the-art model editing techniques to update deprecated API knowledge in three LLMs: Qwen2.5-Coder, CodeGemma, and DeepSeek-Coder. We introduce EDAPIBench, a dedicated benchmark featuring over 70 deprecated APIs from 8 popular Python libraries, with more than 3,000 editing instances. Our results show that the parameter-efficient fine-tuning method AdaLoRA achieves the best performance in enabling edited models to generate correct, up-to-date APIs, but falls short in Specificity (i.e., the editing influences untargeted knowledge). To resolve this, we propose AdaLoRA-L, which defines Common API Layers'' (layers within the LLMs with high importance across all APIs, storing general knowledge and excluded from editing) and restricts edits exclusively to Specific API Layers'' (layers with high importance only for the target API, storing the API-specific knowledge). Experimental results demonstrate that AdaLoRA-L significantly improves Specificity while maintaining comparable performance across other evaluation metrics.


## 14. Efficient Grammar-Constrained Decoding via Parser Stack Classification

**Authors:** Yongmin Li (Peking University), Yihong Dong (Peking University), Jia Li (Tsinghua University), Ge Li (Peking University)

**Categories:** Software Engineering for AI

**中文总结:** PSC 将词汇表全部 token 的语法接受条件预合并为 parser stack 单次分类，使每步 mask 计算复杂度与词表大小无关。复杂编程语言语法下 mask 计算最高快 700 倍，端到端 LLM 吞吐接近无约束解码。

**Abstract:** LLMs are widely used to generate structured output like source code or JSON. Grammar-constrained decoding (GCD) can guarantee the syntactic validity of the generated output, by masking out tokens that violate rules specified by a context-free grammar. However, the online computational overhead of existing GCD methods, with latency typically scaling linearly with vocabulary size, limits the throughput of LLMs, especially for models with large vocabularies. To address this issue, we propose PSC, a novel grammar-constrained decoding method. By combining acceptance conditions of all vocabulary tokens into a single classifier of the parser stack during preprocessing, PSC can compute the complete vocabulary mask by checking the parser stack exactly once per decoding step, with time complexity independent of the vocabulary size. Experiments show that PSC computes masks up to 700× faster than baselines on complex programming language grammars, and up to 30× faster for schema-conformant JSON; end-to-end LLM throughput with PSC approaches that of unconstrained decoding.


## 15. Fairness Invariants: A Relational Approach to Explaining and Mitigating Fairness Bugs

**Authors:** Ranit Debnath Akash, Ashish Kumar (Pennsylvania State University), Gang (Gary) Tan, Saeid Tizpaz-Niari (University of Illinois Chicago)

**Categories:** Software Engineering for AI

**中文总结:** 提出 REMI，将 counterfactual fairness 视为 relational invariant 发现，用双向关系解释定位个体公平性 bug 并以规则缓解；在符号与神经网络程序上 83%+ 定位准确率，歧视决策最多降 70%。

**Abstract:** Data-driven software systems are increasingly deployed in high-stakes socio-economic domains, from criminal justice to financial lending. However, these systems often exhibit individual discrimination—unjustified disparities in which a program yields different outcomes for similar individuals who differ only in their protected attributes (e.g., race, gender, age). While existing research has focused on detecting and quantifying these bugs, there remains a critical lack of principled mechanisms to explain and localize individual fairness bugs. Current explanation techniques are largely designed for single-input decisions rather than the relational nature of discrimination, which inherently involves a comparison between an original and a counterfactual pair.

We present REMI, a framework for the automated localization, explanation, and mitigation of individual fairness bugs. Inspired by loop-invariant synthesis in formal methods, we treat counterfactual fairness as a relational invariant discovery problem. We introduce a bidirectional relational explanation framework that learns over paired examples (𝑥, 𝑥′) to identify regions of the input space where fairness is violated. Unlike traditional one-way implication pairs used in invariant inference, our approach enforces bidirectional constraints: requiring identical outcomes for both original and counterfactual samples. REMI utilizes three data-alignment techniques to infer interpretable rule-based models that act as “fairness invariants.” These rules serve as guardrails to selectively block or relabel unfair predictions without requiring model retraining. Our evaluation on symbolic and neural network programs demonstrates that REMI localizes ground-truth fairness bugs in over 83% of cases, significantly outperforming state-of-the-art baselines and reducing discriminatory decisions in black-box models by up to 70%


## 16. Function Calling as a Flexible LLM Defense Add-On: Capability and Application Exploration

**Authors:** Zhenlan Ji (Nara Institute of Science and Technology), Daoyuan Wu (Lingnan University, Hong Kong SAR China), Wenxuan Wang (Hong Kong University of Science and Technology), Pingchuan Ma (Zhejiang University of Technology), Shuai Wang (Hong Kong University of Science and Technology), Lei Ma (The University of Tokyo & University of Alberta), Juergen Rahmel (HSBC)

**Categories:** Software Engineering for AI

**中文总结:** 探索将 function calling 作为 LLM 可插拔轻量防御，通过定义恶意动作函数拦截有害输出；在 DSPEC 真实应用数据集上显著优于现有防御且对 helpfulness 影响极小。

**Abstract:** Large language models (LLMs) exhibit impressive capabilities but are susceptible to adversarial attacks that induce harmful outputs. Although various defenses have been proposed, their practicality is restricted by substantial runtime overhead or degraded model helpfulness. Moreover, LLM applications typically have diverse and evolving security requirements that cannot be fully anticipated during the design of static defenses. These limitations call for a flexible, low-overhead defense mechanism that can be easily customized to meet task-specific needs.

In this paper, we explore function calling (FC)—a built-in mechanism in modern LLMs for invoking custom tools—as a lightweight and adaptable defense add-on. We show that by defining functions representing malicious actions, LLMs equipped with FC can intercept harmful prompts by triggering these function calls instead of generating unsafe content. Extensive experiments across mainstream LLMs demonstrate that FC substantially improves defense effectiveness with minimal impact on model helpfulness. To further assess FC’s practical utility, we also introduce DSPEC, a new dataset reflecting real-world LLM applications with specific defense requirements. Our evaluations on DSPEC show that FC substantially outperforms existing defenses in this realistic setting. Besides, we also explore the practical applications of FC in various scenarios, including universal defense frameworks and multi-agent systems, further demonstrating its versatility and effectiveness in enhancing LLM security.


## 17. Fuzzing the Boundary Between Models and Code in Hybrid AI-enabled Systems

**Authors:** Xinyu Gao (Nanjing University), Yang Feng (Nanjing University), Yuchen Lu (Nanjing University), Zhenqian Liu (Nanjing University), Zhenyu Chen (Nanjing University), Baowen Xu (Nanjing University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 Neude，面向 hybrid AI-enabled 系统联合程序执行与神经网络 coverage 做 coverage-guided fuzzing，并配合 metamorphic relations 自动检 bug；在 Pylot 自动驾驶系统上揭示模型-代码交互脆弱性。

**Abstract:** Deep learning (DL) techniques are increasingly integrated into traditional software systems, giving rise to hybrid AI-enabled systems that combine neural models with program logic. While these systems exhibit remarkable capabilities, their complex and heterogeneous architectures pose significant challenges for reliability and testing, particularly in safety-critical domains such as autonomous driving. Existing testing approaches either target traditional code or isolate neural networks, overlooking failures arising from their interactions. In this paper, we present Neude, a lightweight and extensible coverage-guided fuzzing framework specifically designed for hybrid AI-enabled systems. Unlike existing tools, Neude combines observations of program execution and neural model coverage to guide input mutations toward unexplored state spaces, enabling systematic evaluation of the entire hybrid pipeline. Moreover, Neude employs domain-aware mutation operators coupled with metamorphic relations, allowing automated bug detection without manual assertions. We evaluate Neude on Pylot, a complex autonomous driving system with tightly coupled neural and program components. Experimental results show that Neude uncovers diverse faults, and further analysis reveals how model uncertainty propagates through deterministic program logic to trigger downstream module failures. Our findings highlight the fragility of current hybrid architectures, calling for a paradigm shift from model-centric testing to system-centric quality assurance that accounts for the intricate interplay between neural and procedural components.


## 18. Insecure Coding Preferences in Long-Term Memory: Security Risks for LLM-based Code Generation

**Authors:** Yuchen Chen (Nanjing University), Wei Cheng (Nanjing University of Aeronautics and Astronautics), Yuan Xiao (Nanjing University), Zhou Yang (University of Alberta; CIFAR AI Chair; Alberta Machine Intelligence Institute), Weifeng Sun (Singapore Management University, Singapore), Chunrong Fang (Nanjing University), Xiang Chen (Nantong University), Baowen Xu (Nanjing University), David Lo (Singapore Management University), Zhenyu Chen (Nanjing University)

**Categories:** Software Engineering for AI

**中文总结:** 首次系统实证 LLM 长期记忆中不安全编码偏好会持久提升漏洞代码生成风险 11–14% 并降低安全警告；显式安全需求可缓解 20–34% 漏洞率。

**Abstract:** LLM-based systems are increasingly incorporating long-term memory to improve cross-session continuity and output consistency. However, the persistence of long-term memory may introduce additional risks in security-sensitive code generation: once insecure coding preferences are stored, they may silently and persistently influence security-critical choices in subsequent generations. In this study, we conduct the first systematic empirical study to evaluate the impact of insecure coding preferences stored in long-term memory on the security of LLM-based code generation. We study two widely used commercial LLMs (i.e., ChatGPT and Gemini) and examine the impact of long-term memory from multiple perspectives. Our results show that insecure coding preferences stored in long-term memory significantly increase the risk of generating vulnerable code by 11.3%–13.8%. Moreover, they reduce the likelihood that models proactively issue security warnings when producing vulnerable code, leading to a 5.4–14.5 percentage-point decrease. Further analysis reveals that these insecure memory entries are difficult to overwrite through normal interactions and can broadly influence model outputs even when prompts are phrased differently. Finally, we evaluate a mitigation strategy based on explicit security requirements, which reduces vulnerability rates by 19.7%–33.6% but may incur a functional performance drop of up to 15.9%. Based on these findings, we provide actionable suggestions to improve the security of long-term memory in LLM-based code generation.


## 19. Is "Knowing It's Malicious'' Enough? Evaluating LLMs for Fine-Grained Malware Behavior Auditing

**Authors:** Xinran Zheng (University College London), Xingzhi Qian (University College London), Yiling He (University College London), Shuo Yang (The University of Hong Kong), Lorenzo Cavallaro (University College London)

**Categories:** Software Engineering for AI

**中文总结:** 提出 MalEval 评估框架，用 expert audit report 与 context-driven IR 分解 malware auditing 为四阶段可验证任务；揭示 LLM 依赖表面线索、难组合证据链等能力边界。

**Abstract:** Automated malware classifiers achieve strong detection performance, but auditing requires more than flagging a sample: analysts must explain malicious behaviors and justify them with concrete code evidence, a requirement that traditional signature-based methods and learning-based XAI often fail to satisfy in a human-interpretable manner. Large Language Models (LLMs) appear well-suited for this task due to their code reasoning and summarization ability, yet it is unclear whether their reasoning capabilities are up to the auditing. In particular, evaluating them faces three hurdles: (1) the lack of detailed, human-written behavior ground truth for reliable benchmarking; (2) the scale of real-world applications’ codebases typically exceed the context limits of current models, which cannot be fully processed at once; and (3) the absence of reliable mechanisms to verify whether LLM-generated behavioral claims are faithfully supported by concrete code evidence.

Together, these obstacles make benchmarking LLM-based auditing non-trivial, leaving their true capabilities and failure modes opaque. To bridge this gap, we introduce MalEval, an evaluation framework for systematically measuring the reasoning fidelity of LLMs in malware auditing. We pair real-world application codebases with expert-written audit reports to obtain fine-grained, behavior-level ground truth. Large codebases are compressed into unified behavior-relevant program contexts via a context-driven intermediate representation that preserves essential call relations. Both expert reports and model outputs are then mapped, through constrained reasoning, into structured evidence chains linking code-level facts to high-level behaviors in a common, comparable space. Built on this foundation, MalEval decomposes auditing into 4 stage-wise auditing tasks, allowing each intermediate judgment to be independently verified under limited context windows. We leverage MalEval to evaluate seven widely used LLMs and uncover clear capability boundaries: models rely on surface cues over verifiable evidence, struggle to compose dispersed facts into coherent attack chains, and are highly sensitive to context formulation. These findings shift the focus from optimizing isolated outputs to designing LLM and agentic workflows that can reliably support malware auditing.


## 20. Learning from the Test: Self-Referential Differential Testing for Deep RL Agents

**Authors:** Junda He (Singapore Management University), Jieke Shi (Singapore Management University), Zhou Yang (University of Alberta; CIFAR AI Chair; Alberta Machine Intelligence Institute), Mingfei Cheng (Singapore Management University), David Lo (Singapore Management University)

**Categories:** Software Engineering for AI

**中文总结:** Delta 对 DRL 智能体分两阶段测试：先收集安全测试数据，再用离线 RL 训练 challenger 并与 AUT 做差分测试以发现最优性缺陷。在五个环境中平均发现 2517 个最优性问题，较基线提升 50.2%。

**Abstract:** Deep Reinforcement Learning (DRL) has achieved significant success in complex decision-making problems. As DRL systems are increasingly deployed in real-world applications, ensuring their quality and reliability is paramount. Current works primarily focus on detecting safety-critical failures, often neglecting policy optimality, which can lead to reduced efficiency, user distrust, and economic losses. This oversight, compounded by the inherent “testing oracle problem” for optimality, leaves a significant gap in comprehensively evaluating DRL systems. To address this gap, we propose Delta (Differential Testing for DRL Agents), a novel and comprehensive framework that automatically identifies both safety-critical and optimality bugs in DRL agents. Delta employs a two-phase approach: (1) Safety Testing, where the Agent Under Test (AUT) is evaluated for catastrophic failures while collecting data from its decision-making policy, and (2) Optimality Testing, where this collected data from the prior phase is used to train a challenger agent via Offline Reinforcement Learning. Differential testing is then performed by comparing the challenger agent against the AUT; instances, where the challenger achieves higher cumulative rewards indicate optimality issues in the AUT. We demonstrate Delta’s effectiveness across five environments. We investigate the effectiveness of three offline RL algorithms (BC, BCQ, and CQL) in generating challenger agents. Experimental results demonstrate that safety testing datasets are valuable for training competent DRL agents. Challenger agents trained with BCQ proved most effective for identifying optimality issues within the framework of Delta. Across the five environments, Delta uncovered an average of 2,517 optimality issues, outperforming the baseline methods by 50.2%.


## 21. LogicHunter: Testing LLM Agent Frameworks with an Agentic Oracle

**Authors:** Minghui Long (Huazhong University of Science and Technology), Yanjie Zhao (Huazhong University of Science and Technology), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI

**中文总结:** LogicHunter 对 LangChain、LlamaIndex、CrewAI 等 LLM agent 框架做规约驱动模糊测试，并用 ReAct 式 Agentic Oracle 主动查文档与源码判定缺陷。发现 40 个未知 bug（30 已确认），Oracle 精度 90.9%，远超被动基线 27.9%。

**Abstract:** Large Language Model (LLM) agent frameworks such as LangChain, LlamaIndex, and CrewAI have become critical infrastructure powering production AI systems, yet they remain severely under-tested due to fundamental challenges in automated testing. Unlike traditional software, where crashes serve as reliable oracles, defects in these pure Python frameworks manifest as ordinary exceptions or silent semantic failures, creating profound oracle ambiguity. This problem is exacerbated by strict type governance through Pydantic schemas and complex protocol requirements that cause existing fuzzers to generate overwhelming invalid inputs, while traditional test generators produce only trivial cases with weak regression assertions.

We present LogicHunter, a fuzzing framework that addresses both the generation and oracle challenges through active specification-aware testing. LogicHunter employs specification-driven generation that systematically fuses formal type constraints with authentic usage patterns from real-world repositories, synthesizing inputs that are valid by construction yet semantically extreme, equipped with behavioral probes to expose silent failures. To resolve oracle ambiguity, we introduce the Agentic Oracle, which transcends passive classification by actively retrieving documentation, navigating source code, and inspecting runtime states through a ReAct-based architecture with Dual-Layer State Management and Dual-Stream Memory. Evaluated on three widely deployed frameworks, LogicHunter discovered 40 previously unknown bugs with 30 confirmed and 26 fixed by developers, while state-of-the-art baselines found none. The Agentic Oracle achieves 90.9% precision, surpassing the best passive approach at 27.9% by 63 percentage points.


## 22. Lookahead-then-Verify: Reliable Constrained Decoding for Diffusion LLMs under Context-Free Grammars

**Authors:** Yitong Zhang (Beihang University), Yongmin Li (Peking University), Yuetong Liu (Beihang University), Jia Li (Tsinghua University), Xiaoran Jia (Beijing Institute of Technology), Zherui Li (Beijing University of Posts and Telecommunications), Ge Li (Peking University)

**Categories:** Software Engineering for AI

**中文总结:** LAVE 针对扩散 LLM 在 CFG 约束解码时利用并行 token 分布做 lookahead 验证，确保中间输出可扩展为合法句子。在四个 dLLM 与三个基准上显著提升语法正确率，运行时开销可忽略。

**Abstract:** Diffusion Large Language Models (dLLMs) have demonstrated promising generative capabilities and are increasingly used to produce formal languages defined by context-free grammars, such as source code and chemical expressions. However, as probabilistic models, they still struggle to generate syntactically valid outputs reliably. A natural and promising direction to address this issue is to adapt constrained decoding techniques to enforce grammatical correctness during generation. However, applying these techniques faces two primary obstacles. On the one hand, the non-autoregressive nature of dLLMs renders most existing constrained decoding approaches inapplicable. On the other hand, current approaches specifically designed for dLLMs may allow intermediate outputs that are impossible to complete into valid sentences, which significantly limits their reliability in practice.

To address these challenges, we present LAVE, a constrained decoding approach specifically designed for dLLMs. Our approach leverages a key property of dLLMs, namely their ability to predict token distributions for all positions in parallel during each forward pass. Whenever a new token is proposed by model, LAVE performs lookahead using these distributions to efficiently and reliably verify the validity of the proposed token. This design ensures reliable constraints by reliably preserving the potential for intermediate outputs to be extended into valid sentences. Extensive experiments across four widely used dLLMs and three representative benchmarks demonstrate that LAVE consistently outperforms existing baselines and achieves substantial improvements in syntactic correctness, while incurring negligible runtime overhead.


## 23. PackMonitor: Towards Zero Package Hallucinations via Decoding-Time Monitoring

**Authors:** Xiting Liu (Tsinghua University), Yuetong Liu (Beihang University), Yitong Zhang (Beihang University), Jia Li (Tsinghua University), Shi-Min Hu (Tsinghua University)

**Categories:** Software Engineering for AI

**中文总结:** PackMonitor 在解码时监控 LLM 输出，于安装命令生成阶段用 Context-Aware Parser 触发 Package-Name Intervenor，将解码空间限制在权威包列表并配合 DFA-Caching。五种 LLM 上包幻觉率降至零且推理延迟开销可忽略。

**Abstract:** As Large Language Models (LLMs) are increasingly integrated into software development workflows, their trustworthiness has become a critical concern. However, in dependency recommendation scenarios, the reliability of LLMs is undermined by widespread package hallucinations, where models often recommend hallucinated packages. Recent studies have proposed a range of approaches to mitigate this issue. Nevertheless, existing approaches typically merely reduce hallucination rates rather than eliminate them, leaving persistent software security risks.

In this work, we argue that package hallucinations are theoretically preventable based on the key insight that package validity is decidable through finite and enumerable authoritative package lists. Building on this, we propose PackMonitor, the first approach capable of fundamentally eliminating package hallucinations by continuously monitoring the model’s decoding process and intervening when necessary. To implement this in practice, PackMonitor addresses three key challenges: (1) determining when to trigger intervention via a Context-Aware Parser that continuously monitors model outputs and selectively activates  intervening only during installation command generation; (2) resolving how to intervene by employing a Package-Name Intervenor that strictly limits the decoding space to an authoritative package list; and (3) ensuring monitoring efficiency through a DFA-Caching Mechanism that enables scalability to millions of packages with negligible overhead. Extensive experiments on five widely used LLMs demonstrate that PackMonitor is a training-free, plug-and-play solution that consistently reduces package hallucination rates to zero while maintaining low-latency inference and preserving original model capabilities.


## 24. Provably Lossless Acceleration of DNN Mutation Testing via Memoization

**Authors:** Ali Ghanbari (Auburn University), Ben Greenman (University of Utah), Sasan Tavakkol (Google Research), Shibbir Ahmed (Texas State University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 Mure，通过 memoization 复用 DNN 原模型与 mutant 的公共前缀计算，实现可证明无损的 DNN mutation testing 加速。在 15 个模型上平均降低 44.54% 计算开销，且 mutation score 与穷举测试等价。

**Abstract:** Mutation analysis has recently reemerged in the context of deep neural networks (DNNs) as a promising, but notoriously costly, approach for assessing test dataset adequacy. Existing techniques speed up DNN mutation testing through lossy approximations that trade efficiency for mutation score accuracy. This paper introduces Mure, the first provably lossless framework for accelerating DNN mutation testing via memoization. Mure is based on the idea that DNN mutants and the original model share substantial redundant computation, so during mutation testing, it executes only the mutated suffixes of each mutant and reuses the common prefix from the original model, which is computed only once. We give a formal account of memoized mutation testing, and prove that Mure is sound, i.e., it produces results equivalent to exhaustive vanilla mutation testing, and identify basic conditions under which speed-up is guaranteed. We have implemented Mure and evaluated it on 15 DNN models of various architectures, complexities, and sizes ranging from a few thousands to millions of parameters. This provides empirical evidence that Mure reduces the computational cost of mutation testing by 44.54%, on average. We also observed that while state-of-the-art techniques tend to yield higher acceleration (up to 88.97%, on average), they come at the cost of some error in mutation score. We further analyze the effect of mutation generation selection ratio on the effectiveness of Mure and observed predictable reductions in memoization opportunities with increasing the percentage of mutated neurons. We observed that Mure offers more than 20% speed-up even when as high as 5% of the neurons are mutated.


## 25. ScratchNet: A Multi-modal Benchmark for Evaluating and Advancing LLMs on Scratch Programming Tasks

**Authors:** Yuan Si (University of Waterloo), Simeng Han (Stanford University), Daming Li (Independent Researcher), Hanyuan Shi (Independent Researcher), Jialu Zhang (University of Waterloo)

**Categories:** Software Engineering for AI

**中文总结:** 发布 ScratchNet 可执行基准，含 100 个高复杂度 Scratch 项目及测试套件、块级最小编辑约束与多媒体资产，三层协议评估 LLM 修复。为块语言程序理解、调试与修复提供可复现评测与后训练闭环。

**Abstract:** Large language models (LLMs) have achieved impressive performance on text-based programming tasks, yet they remain unreliable for block-based languages like Scratch. Scratch programs feature deeply nested, non-linear structures, event-driven concurrency across multiple sprites, and tight coupling between code and multimedia assets, properties that are fundamentally different from those of textual code. As a result, LLMs frequently misinterpret Scratch semantics and propose large, invasive edits that are syntactically valid yet semantically misaligned when repairing buggy programs.

We introduce ScratchNet, the first executable benchmark designed to systematically evaluate and advance LLM-based repair methods for Scratch programs, spanning program understanding, debugging, analysis, and repair. The benchmark comprises 100 carefully curated Scratch projects from the public repository, each chosen for high structural and semantic complexity. Every project is paired with executable test suites, bug descriptions and corresponding fixes, block-level edit constraints that define minimal semantically correct repairs, and associated multimedia assets. We construct the benchmark via a human-in-the-loop pipeline that combines automated project mining with expert validation of trigger mechanism–outcome semantics and representative bug patterns, with particular focus on event ordering, concurrency, and state management.

To enable rigorous and reproducible evaluation, we propose a three-layer, executable protocol that measures functional correctness via VM-level execution, repair quality in terms of minimality and semantic fidelity using block-level edit distance and behavioral trajectory comparisons, and explanation quality through structured rubrics assessing alignment between the model’s reasoning and its patch. Using this benchmark, we investigate fundamental research questions such as the impact of domain-specific fine-tuning on repair success, the effectiveness of different training data sources, and the ability of models to generalize to unseen bug types. Our benchmark establishes a reproducible foundation and a closed-loop framework for evaluating and post-training LLMs on block-based programming tasks.


## 26. Seeing is Coding: On the Effectiveness of Vision Language Models in Code Understanding

**Authors:** Yuling Shi (Shanghai Jiao Tong University), Chaoxiang Xie (Hohai University), Zhensu Sun (Singapore Management University), Yeheng Chen (Shanghai Jiao Tong University), Chenxu Zhang (Imperial College London), Longfei Yun (UC San Diego), Chengcheng Wan (East China Normal University), Hongyu Zhang (Chongqing University), David Lo (Singapore Management University), Xiaodong Gu (Shanghai Jiao Tong University)

**Categories:** Software Engineering for AI

**中文总结:** 首次系统评估 MLLM 以渲染图像理解代码的可行性：最高 8× token 压缩仍有效，语法高亮在 4× 压缩下提升补全，克隆检测对视觉压缩高度鲁棒。揭示图像模态代码表示的效率潜力与局限。

**Abstract:** Large Language Models (LLMs) have achieved remarkable success in source code understanding, yet as software systems grow in scale, computational efficiency has become a critical bottleneck. Currently, these models rely on a text-based paradigm that treats source code as a linear sequence of tokens, which leads to a linear increase in context length and associated computational costs. The rapid advancement of Multimodal LLMs (MLLMs) introduces an opportunity to optimize efficiency by representing source code as rendered images. Unlike text, which is difficult to compress without losing semantic meaning, the image modality is inherently suitable for compression. By adjusting resolution, images can be scaled to a fraction of their original token cost while remaining recognizable to vision-capable models. To explore the feasibility of this approach, we conduct the first systematic study on the effectiveness of MLLMs for code understanding. Our experiments reveal that: (1) MLLMs can effectively understand code with substantial token reduction, achieving up to 8x compression; (2) MLLMs can effectively leverage visual cues such as syntax highlighting, improving code completion performance under 4x compression; and (3) Code-understanding tasks like clone detection exhibit exceptional resilience to visual compression, with some compression ratios even slightly outperforming raw text inputs. Our findings highlight both the potential and current limitations of MLLMs in code understanding, which points out a shift toward image-modality code representation as a pathway to more efficient inference.


## 27. SEER: Self-Enhancing Chain-of-Thought Compression for Reasoning Models

**Authors:** Kerui Huang, Shuhan Liu (Zhejiang University), Xing Hu (Zhejiang University), Tongtong Xu (Nanjing University), Lingfeng Bao (Zhejiang University), Xin Xia (Zhejiang University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 SEER 自适应 CoT 压缩框架：Best-of-N 去循环、数据驱动过滤后微调，在代码生成等 SE 任务上平均缩短推理链 41.6% 并提升性能。发现过长 CoT 常致截断与 n-gram 退化循环。

**Abstract:** Chain-of-Thought (CoT) prompting can substantially improve the reasoning ability of large language models (LLMs), but it often comes with high inference cost due to long and poorly controlled reasoning traces. This overhead is particularly problematic in software engineering tasks (e.g., code generation), where both latency and output reliability matter.

To better understand this trade-off, we conduct an empirical study on widely used code generation benchmarks and observe that many modern reasoning models produce excessively verbose CoTs (often thousands of tokens), which frequently leads to truncation and unstable generation. Using a strict n-gram repetition detector, we find that the vast majority of truncations are associated with degenerate looping behaviors. Moreover, longer CoT does not necessarily yield better outcomes: failed generations tend to be longer than successful ones, indicating diminishing or even negative returns from overlong reasoning.

Motivated by these findings, we propose SEER (Self-Enhancing Efficient Reasoning), a self-enhancing framework for adaptive CoT compression. SEER improves the conciseness of reasoning while preserving output quality, without relying on external compression tools. SEER refines self-generated CoT data via Best-of-N sampling to suppress looping and redundant traces, then applies a lightweight, data-driven filter to encourage concise yet correct reasoning. It then fine-tunes the model on the filtered data to internalize concise reasoning behaviors. Across three software engineering tasks, SEER reduces CoT length by 41.6% on average while improving task performance, largely by reducing truncation and mitigating reasoning loops.


## 28. SpectraDL: A Historical Issue-Driven, Test Specification-Assisted Transfer Testing Approach for Deep Learning Frameworks via LLMs

**Authors:** Shifan Liu (University of Science and Technology Beijing), Chang-ai Sun (University of Science and Technology Beijing), Fulei Wu (University of Science and Technology Beijing), Wing-Kwong Chan (City University of Hong Kong)

**Categories:** Software Engineering for AI

**中文总结:** 提出 SpectraDL，从算子文档抽取测试规约、将历史 issue 转为 bug pattern，并以语义+结构双检索做跨框架迁移测试。在四个主流 DL 框架中发现 125 个未知 bug，107 个获开发者确认。

**Abstract:** Deep learning (DL) frameworks provide diverse fundamental algorithmic units as operators, which are critical infrastructure for constructing various intelligent software. Due to the fact that open source development paradigm is widely adopted by mainstream frameworks, bugs may repeatedly occur across operators and even frameworks. Although some efforts have been reported that large language models (LLMs) are leveraged to exploit historical issues to generate test cases for cross-framework testing, existing approaches suffer from the following limitations: 1) the generated test cases have low fault detection capability since they mainly rely on inputs or contexts from historical issues without considering the underlying root causes; 2) an effective mechanism is missing to determine the appropriate scope in a targeted framework for applying generated test cases. To overcome these limitations, we propose SpectraDL, a historical issue-driven, test specification-assisted transfer testing approach for DL frameworks. SpectraDL first extracts rigorous test specifications for each operator from official documentation, and then extracts and transforms historical issues and associated pull requests into structured fault representations (i.e., bug patterns). A dual retrieval mechanism based on semantic intent and structural input-space features is designed to transfer these bug patterns for testing related operators across frameworks. We evaluated SpectraDL with four mainstream DL frameworks, and experimental results have shown that SpectraDL successfully detected 125 previously unknown bugs, with 107 confirmed by developers. The results confirm that SpectraDL delivers a promising transfer testing approach for DL frameworks.


## 29. StateTree: A Tree-Based Modeling Approach for Fault Detection in Recurrent Neural Networks

**Authors:** Xinyu Gao (Nanjing University), Shuoxiao Zhang (Nanjing University), Minghui Wei (Nanjing University), Xiao Zhang (Nanjing University), An Guo (The Hong Kong Polytechnic Universituy, Hong Kong SAR China), Enyi Tang (Nanjing University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 StateTree，构建 Abstract State Tree 抽象 RNN 决策行为并引导测试探索未见路径。能准确抽象 RNN 决策、检出数百故障，以其测试用例重训练可超越现有 RNN 覆盖率方法的鲁棒性提升。

**Abstract:** Recurrent Neural Networks (RNNs) have become a core component of modern intelligent software due to their strong ability to model temporal dependencies. As RNNs are increasingly deployed in safety-critical domains, ensuring their reliability is crucial. However, most existing testing techniques are designed for feedforward networks and struggle with RNNs. The stateful nature, recurrent feedback, and long-term dependencies of RNNs make it difficult for existing testing methods to capture decision logic and temporal behaviors, which in turn makes detecting fault-inducing behaviors that emerge through temporal decision evolution challenging.

To address these challenges, we propose StateTree, a tree-based abstract modeling approach for systematic testing of RNN-based systems. StateTree constructs an Abstract State Tree (AST) that captures major RNN decision behaviors, where each root-to-leaf path represents an abstract decision for intuitive interpretation and structured exploration. Using the AST, StateTree guides the testing process toward both major and previously unseen paths to reveal erroneous behaviors. Experiments show that StateTree accurately abstracts RNN decisions, detects hundreds of faults, and retraining with its identified test cases improves robustness beyond existing RNN coverage methods, demonstrating its effectiveness in both fault detection and model performance enhancement.


## 30. TensorLock: Recovering Model Dependency for Model Supply Chain

**Authors:** Susheng Wu (Fudan University), Ziqian Chen (Fudan University), Chengyuan Li (Fudan University), Kaifeng Huang (Tongji University), Zekai Chen (Fudan University), Yijian Wu (Fudan University), Bihuan Chen (Fudan University), Yiheng Cao (Fudan University), Zhuotong Zhou (Fudan University), Yiheng Huang (Fudan University), Xin Peng (Fudan University)

**Categories:** Software Engineering for AI

**中文总结:** TensorLock 通过连通性聚类与类型感知指纹识别，自动恢复模型托管平台上的依赖关系图。聚类 ARI 达 0.96、依赖识别 DF1 达 0.82，在 289 个孤立模型中恢复 189 条缺失依赖（42 条获作者确认）。

**Abstract:** The public models on the model hosting platforms have undergone exponential growth, allowing developers to build upon existing models rather than training from scratch. These models are continuously reused, modified, and re-distributed similar to traditional software components, breeding a dense and rapidly evolving model supply chain. However, while enjoying the benefits of model reuse, developers also inherit supply risks ranging from legal liabilities to security threats. To mitigate these risks, a well-established model dependency graph can significantly benefit supply chain risk governance. Unfortunately, although model hosting platforms offer mechanisms for dependency disclosure, such declarations are optional and frequently missing.

To address this challenge, we propose a novel model dependency recovering framework TensorLock. It works in two phases; i.e., (1) model clustering, and (2) type-aware dependency identification within theseclusters. In the first phase, TensorLock performs connectivity-based clustering to accommodate the open-ended dependency topology, grouping models with dependency relations. In the second phase, TensorLock employs a divide-and-conquer strategy, leveraging distinct type-specific fingerprints to first identify data-free dependencies (Quantization and Merging), and then resolve data-driven Fine-Tuning dependencies. Our evaluation demonstrates that TensorLock substantially outperforms state-of-the-art approaches, achieving an ARI of 0.96 in clustering and a DF1 of 0.82 in dependency identification, improving over the best baselines by at least 39% and 193%, respectively. Additionally, we apply TensorLock to 289 supposedly isolated models and recover 189 previously missing model dependencies, with 42 model authors confirming our findings.


## 31. Test Case Prioritization for DNNs via Neural Collapse Instability

**Authors:** Chunyu Liu, Mingyuan Li (lnformation Securty Center, State Key Laboratory of Networking and Switching Technology, Beijing University of Posts and Telecommunications), Yang LI, Wenmin Li (State Key Laboratory of Networking and Switching Technology, Beijing University of Posts and Telecommunications), Fei Gao (State Key Laboratory of Networking and Switching Technology, Beijing University of Posts and Telecommunications; National Engineering Research Center of Disaster Backup and Recovery, Beijing University of Posts and Telecommunications), Tengfei Tu (State Key Laboratory of Networking and Switching Technology, Beijing University of Posts and Telecommunications), Su-Juan Qin (State Key Laboratory of Networking and Switching Technology, Beijing University of Posts and Telecommunications)

**Categories:** Software Engineering for AI

**中文总结:** NCIP 基于 Neural Collapse 思想，通过晚训 checkpoint 的预测一致性而非单点置信度对 DNN 测试用例排序。在多数据集/架构上 RAUC 提升 2.34%–13.57%，RAUC-500 提升 4.61%–31.77%，显著优于现有基线。

**Abstract:** With the widespread deployment of deep neural networks (DNNs) in safety-critical domains, reducing the cost of model validation under limited testing budgets has become increasingly important. Existing test case prioritization techniques often rely on single-checkpoint confidence signals derived from output probabilities. However, DNNs can be confidently wrong, and the confidence margin between the predicted and competing classes is frequently small, which weakens early fault discovery. To address this limitation, we propose a \textbf{N}eural-\textbf{C}ollapse-\textbf{I}nspired \textbf{P}rioritization (\textbf{NCIP}) framework that replaces absolute confidence with cross-checkpoint consistency in the terminal training regime, where model geometry becomes highly structured. NCIP introduces two key components. First, it selects a coherent set of late training checkpoints by measuring the equiangularity of classifier weights, quantified as the standard deviation of pairwise cosine similarities among class weight vectors. Second, it prioritizes test inputs by their prediction variability across the selected checkpoints, surfacing boundary-adjacent and failure-prone samples that are unstable under checkpoint-induced decision boundary shifts. Extensive experiments across multiple datasets and architectures show that NCIP consistently improves early fault discovery over strong baselines, achieving \textbf{2.34%–13.57%} RAUC gains and \textbf{4.61%–31.77%} RAUC-$500$ gains under the same testing budget. NCIP further attains the best average performance across all dataset model pairs.


## 32. Test Case Selection for Deep Neural Networks: A Replication Study on LLMs for Code (Replicability Study)

**Authors:** Ali Asgari (TU Delft), Mitchell Olsthoorn (Delft University of Technology), Annibale Panichella (Delft University of Technology)

**Categories:** Software Engineering for AI

**中文总结:** 大规模复现研究将 13 种 DNN 测试用例选择（TCS）策略应用于 17 个代码 LLM 的克隆检测、漏洞检测与技术债预测任务。发现仅部分视觉 DNN 结论可泛化，特征驱动不确定性方法 consistently 优于熵基线，效果因任务与模型而异。

**Abstract:** Test case selection (TCS) techniques have been widely studied to support the operational evaluation of deep neural networks (DNNs) under limited testing budgets, where labeling cost is a primary concern and uncovering model failures early is a key objective. Although prior studies report promising results, existing empirical evaluations focus almost exclusively on vision-based DNNs and datasets. As observed in recent surveys, models and datasets specifically designed for software engineering tasks have not been considered, leaving it unclear whether prior findings generalize to LLM code models.

This paper presents a large-scale replication study of TCS techniques in the context of LLM code models. We re-examine established TCS strategies originally proposed for DNNs and complement them with statistical sampling strategies that have not previously been evaluated for TCS. We assess their effectiveness on three code-related classification tasks: clone detection, vulnerability detection, and technical debt prediction. The study spans 17 fine-tuned language models, 7 predictive features, and 13 selection strategies, and evaluates performance along two dimensions: operational accuracy estimation and early failure discovery.

The results indicate that only a subset of findings reported for vision-based DNNs generalize when TCS is applied to LLMs for code. In particular, feature-driven uncertainty measures consistently outperform entropy-based baselines, and statistical sampling strategies improve robustness without sacrificing accuracy estimation or failure discovery. At the same time, performance varies substantially across tasks and models, indicating that the effectiveness of TCS techniques is context-dependent. Overall, this study provides empirical evidence on the replicability of TCS techniques beyond vision-based deep learning and offers insights into their use for the operational evaluation of LLMs for code.


## 33. Testing Retrieval-Augmented Generation Systems with Chunk Coverage

**Authors:** Jinhan Kim (Università della Svizzera italiana), Samuele Pasini (Università della Svizzera italiana), Paolo Tonella (USI Lugano)

**Categories:** Software Engineering for AI

**中文总结:** Chunk Coverage（CC）提出无需 oracle 的 RAG 检索组件测试充分性准则，度量测试套件对语料 chunk 的覆盖比例并指导测试选择。CC 引导测试达 50% 覆盖率速度比随机快 1.9×、比冗余策略快 6.9×，APFD 提升 10%–25%。

**Abstract:** Retrieval-Augmented Generation (RAG)-based systems are increasingly deployed in high-stakes settings where correct behaviour depends not only on the language model but also on the retrieval component that selects external documents at inference time. While existing RAG evaluation metrics assess retrieval and generation quality on a per-query basis, typically relying on query-level test oracles such as reference answers or relevance annotations, they provide limited insight into whether a test suite adequately exercises the retrieval behaviour of the system as a whole. In this paper, we introduce Chunk Coverage (CC), an oracle-independent test adequacy criterion for testing the retrieval component of RAG systems. CC measures the fraction of corpus chunks that are retrieved at least once across a test suite, providing a structural view of which parts of the retrieval space have been exercised. We further show how CC can be used to guide test selection and generation by prioritising queries that expand coverage of previously unexercised retrieval regions. We evaluate CC on clinical and financial RAG system scenarios. CC-guided testing reaches 50% of attainable coverage up to 1.9 times faster than random selection and up to 6.9 times faster than redundancy-biased strategies. Moreover, CC improves fault detection effectiveness (APFD) by 10% to 25% over random, indicating earlier discovery of distinct retrieval faults. These results show that CC captures retrieval diversity relevant to effective testing without requiring test oracles.


## 34. Toward Secure Code Generation: Bridging Correctness and Security via Task-Adaptive Vulnerability Modeling and Execution-Based Benchmarking

**Authors:** Jiexin Wang (South China University of Technology), Liuwen Cao (South China University of Technology), Xitong Luo (South China University of Technology), Yang Cao (South China University of Technology), Zhenghao Li (South China University of Technology), Yunyi Xiao (South China University of Technology), Mengchen Zhao (South China University of Technology), Adam Jatowt (University of Innsbruck), Yi Cai (School of Software Engineering, South China University of Technology, Guangzhou, China)

**Categories:** Software Engineering for AI

**中文总结:** CodeSecEval 提供 255 个可执行 Python 安全编码任务（77 类 CWE），SecAwareCoder 通过任务自适应威胁建模与执行反馈引导安全代码生成。多 LLM 骨干上 Pass@1 与安全鲁棒性 consistently 优于 prompt 与分析器基线。

**Abstract:** Large language models (LLMs) are increasingly used for program synthesis, yet they often generate code that is functionally plausible but insecure. Progress in secure code generation has been hindered by benchmarks that are small, non-executable, leak mitigation details, or rely on noisy analyzers and subjective judgments, making it difficult to measure whether security improves without sacrificing correctness. We address these gaps with CodeSecEval, an execution-based benchmark for secure code generation, comprising 255 Python tasks spanning 77 CWE categories. Each task provides paired insecure and secure implementations together with executable functional and vulnerability-targeted security tests, enabling precise and reproducible evaluation of secure code generation and insecure-code repair. Building on CodeSecEval, we propose SecAwareCoder, an agent-based framework that shifts code generation toward secure-by-construction synthesis. SecAwareCoder performs task-adaptive threat modeling to identify security-sensitive regions and derive task-grounded vulnerability hypotheses, uses these hypotheses to guide both constraint-aware code generation and security-aware test synthesis, and leverages execution feedback for targeted refinement. Experiments across multiple LLM backbones show that SecAwareCoder consistently improves Pass@1 and security robustness over prompting and analyzer-driven baselines, narrowing the security–correctness gap in LLM code generation.


## 35. Understanding and Improving Model Editing for Secure Code Generation

**Authors:** Weifeng Sun (Singapore Management University, Singapore), Quanjun Zhang (Nanjing University of Science and Technology), Yuchen Chen (Nanjing University), Chengran Yang (Singapore Management University, Singapore), Gou Tan (School of Systems Science and Engineering, Sun Yat-sen University, Guangzhou, China), David Lo (Singapore Management University)

**Categories:** Software Engineering for AI

**中文总结:** 首次系统评估模型编辑作为 LLM 安全代码生成硬化机制，对比 CoSec 等推理时方法。编辑在已知漏洞上安全比提升 15%–25%，SafeEdit 后处理将 Pass@1 比 UltraEdit 提升 44.40%–156.07% 且基本保持安全性。

**Abstract:** Large language models (LLMs) are widely used for code generation, yet they can reproduce vulnerable code implementations learned from insecure patterns in training data. Prior work has primarily explored \emph{inference-time hardening} to reduce insecure generations without updating the target model. While effective, this paradigm couples security behavior to the auxiliary component and incurs additional runtime overhead. This paper presents the first systematic empirical study of applying \emph{model editing} as the \emph{model-level} hardening mechanism for secure code generation. Unlike inference-time interventions, model editing updates a small subset of parameters to inject security-relevant knowledge directly into the target LLM. We evaluate 3 state-of-the-art editing methods across diverse LLM families and compare them with CoSec, a representative inference-time hardening approach, focusing on: (i) security effectiveness and robustness, (ii) generalization to unseen vulnerabilities, and (iii) functional correctness on general programming tasks. Our results show that model editing yields substantially larger security gains than CoSec on seen vulnerability types, improving security ratios by 15%–25% over vanilla models, and these gains remain stable under prompt perturbations. However, security improvements do not always transfer reliably to unseen vulnerabilities and induce functional regressions on general programming tasks, even for UltraEdit, the best-performing editing method in our evaluation. To mitigate this side effect, we propose SafeEdit, an effective post-edit refinement method that combines functional tuning with edit-aware regularization, which improves Pass@1 by 44.40%–156.07% over UltraEdit and largely preserves (and even improves) security. Moreover, SafeEdit and CoSec are complementary: combining them can further improve security under stochastic decoding while maintaining strong functional correctness. Finally, we analyze efficiency and key design factors, showing that model editing is more efficient than CoSec and sensitive to editing depth, parameter location, and injected context. Overall, our work provides evidence-backed guidance for applying model editing to secure code generation.


## 36. What Makes In-Context Examples Effective for Code Generation?

**Authors:** Dongze Li (The Hong Kong University of Science and Technology and Guangzhou HKUST Fok Ying Tung Research Institute), Songqiang Chen (The Hong Kong University of Science and Technology), Jialun Cao (The Hong Kong University of Science and Technology and Guangzhou HKUST Fok Ying Tung Research Institute), Shing-Chi Cheung (Hong Kong University of Science and Technology)

**Categories:** Software Engineering for AI

**中文总结:** 通过受控实验系统分析 ICL 代码示例各属性对 LLM 代码生成的影响。发现 LLM 难以从相似题解提取泛化洞察，但 I/O 演示等上下文信息显著有效，语义化标识符命名比格式更关键（去除描述性命名可降 30 个百分点）。

**Abstract:** In-Context Learning (ICL) has emerged as a promising solution to enhance the code generation capabilities of Large Language Models (LLMs) by incorporating code examples inside the prompt to let LLMs learn from demonstrations. However, despite their effectiveness gains, it remains unclear which specific properties of ICL-provided code examples (e.g., solution insight, essential contextual information, identifier naming styles, code formatting) drive these gains. This paper systematically investigates the impact of different sources and internal features of code examples on ICL for code generation through controlled experiments on contest-style programming questions and repository-level tasks. Our results show that while LLMs struggle to extract generalizable problem-solving insights from provided solutions to similar questions or repository snippets, their retrieval-augmented ICL performance can significantly benefit from explicit contextual information, such as input/output demonstrations, required helper functions, and namespace information. Through targeted mutation operators, we further find that identifier naming is substantially more critical than code formatting or low-level implementation details, with the elimination of descriptive variable names causing performance drops of up to 30 percentage points. Finally, we demonstrate that LLMs significantly prefer semantically meaningful identifier names and that adherence to surface-level naming conventions is far less important than semantic clarity. These findings provide practical guidelines for constructing effective ICL code examples and highlight challenges in reflection-based learning for code generation.


## 37. When Optimizations Backfire: The Paradox of Plaintext Optimizations in Privacy-Preserving ML Compilers

**Authors:** Yichen Li (Southern University of Science and Technology), Jin Tan (Ant Group), Dongwei Xiao (Hong Kong University of Science and Technology, Hong Kong SAR China), Yiteng Peng (Hong Kong University of Science and Technology), Pingchuan Ma (Zhejiang University of Technology), Junming Ma (Ant Group), Shoumeng Yan (Ant Group), Shuai Wang (Hong Kong University of Science and Technology), Fengwei Zhang (Southern University of Science and Technology)

**Categories:** Software Engineering for AI

**中文总结:** Hopta 通过选择性启用/禁用 Plaintext-Domain Optimization Passes 的流水线变异检测 CMLC 优化缺陷，并用 profile 引导代码化简隔离根因。在 SecretFlow-SPU 上发现 11 个优化缺陷，编译电路成本最高增加 310.2%。

**Abstract:** Growing concerns about data security and privacy have fueled the widespread adoption of Privacy-Preserving Machine Learning (PPML). Cryptography-based PPML, which allows computation directly on encrypted data, significantly mitigates data leakage risks. To facilitate its adoption, Ciphertext Machine Learning Compilers (CMLCs) automate the translation of high-level ML procedures into low-level circuits for encrypted data. Recently, CMLCs have increasingly adopted infrastructure from Plaintext Machine Learning Compilers (PMLCs). While integrating Plaintext-Domain Optimization Passes (PDOPs) into CMLCs offers potential performance, usability, and extensibility benefits, our study shows it can also lead to severe performance regressions — a risk that has been largely overlooked.

To address this, we introduce Hopta, a hybrid domain optimization defects tester and analyzer, aiming to find optimization bugs that can degrade the performance of compiled circuits from CMLCs. We carefully design two core components: (1) an optimization pipeline mutation mechanism to detect optimization defects by selectively enabling/disabling PDOPs, and (2) a profile-guided code reduction tool that efficiently simplifies defect-triggering programs to isolate optimization defects and facilitate debugging. Applying Hopta to SecretFlow-SPU, a production-grade CMLC, we identified 11 optimization defects (spanning matrix indexing, arithmetic/boolean conversion, and cost model deviation) that led to substantial performance regressions, with compiled circuits incurring up to 310.2% increased cost. Our comprehensive analysis provides empirical insights into fundamental differences between plaintext and ciphertext domain optimization strategies, offering crucial guidance for future CMLC development. We conclude with a brief discussion of extensions to other hybrid ML compilers, underscoring the methodology’s compiler-agnostic nature. This work establishes a new research direction for enhancing CMLC performance and the practical deployment of privacy-preserving ML systems.

