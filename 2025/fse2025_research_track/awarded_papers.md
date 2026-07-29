# FSE 2025 Research Track — Awarded Papers

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total: 13 papers

## Award breakdown

| Award | # Papers |
| --- | ---: |
| ACM SIGSOFT Distinguished Paper Award | 13 |

*Note: awards are taken from the conference program / Awards listing (ACM SIGSOFT Distinguished Paper Award).*

## Papers

## 1. A Causal Learning Framework for Enhancing Robustness of Source Code Models

**Authors:** Junyao Ye (Huazhong University of Science and Technology), Zhen Li (Huazhong University of Science and Technology), Xi Tang (Huazhong University of Science and Technology), Deqing Zou (Huazhong University of Science and Technology), Shouhuai Xu (University of Colorado Colorado Springs), Qiang Weizhong (Huazhong University of Science and Technology), Hai Jin (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729387

**中文总结:** 提出 CausalCode，用因果数据增强与正则化学习不变表示，抑制源码模型中的虚假相关；在 CodeBERT 与 GraphCodeBERT 的四项 SE 任务上，鲁棒性优于现有方法。

**Abstract:** Deep Learning (DL) models are useful for many software engineering tasks. However, these models are susceptible to adversarial attacks, partly because they learn spurious features that incur spurious correlations between these features and model predictions. In this paper, we tackle the problem with a novel causal learning framework, dubbed CausalCode, which leverages causal inference principles to mitigate spurious correlations. At a high level, CausalCode can be characterized as follows: (i) it uses causal data augmentation to generate intervention examples to disrupt spurious correlations; (ii) it leverages regularization to learn invariant representations that prefer causal features to spurious features; (iii) it can enhance the robustness of multiple DL models for source code-based software engineering tasks because it is task-agnostic and model-agnostic. To evaluate its effectiveness, we conduct experiments on two models, CodeBERT and GraphCodeBERT, with respect to four software engineering tasks. Experimental results show that CausalCode outperforms the state-of-the-art approaches in enhancing the robustness of these models.

## 2. COFFE: A Code Efficiency Benchmark for Code Generation

**Authors:** Yun Peng (The Chinese University of Hong Kong), Jun Wan (Zhejiang University), Yichen LI (The Chinese University of Hong Kong), Xiaoxue Ren (Zhejiang University)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715727

**中文总结:** 提出代码生成时间效率基准 COFFE（函数级 398、文件级 358 题），含压力测试用例生成与基于 CPU 指令数的 efficient@k 指标；评估 14 个主流 LLM 并总结四项发现与实践启示。

**Abstract:** Code generation has largely improved development efficiency in the era of large language models (LLMs). With the ability to follow instructions, current LLMs can be prompted to generate code solutions given detailed descriptions in natural language. Many research efforts are being devoted to improving the correctness of LLM-generated code, and many benchmarks are proposed to evaluate the correctness comprehensively. Despite the focus on correctness, the time efficiency of LLM-generated code solutions is under-explored. Current correctness benchmarks are not suitable for time efficiency evaluation since their test cases cannot well distinguish the time efficiency of different code solutions. Besides, the current execution time measurement is not stable and comprehensive, threatening the validity of the time efficiency evaluation. To address the challenges in the time efficiency evaluation of code generation, we propose COFFE, a code generation benchmark for evaluating the time efficiency of LLM-generated code solutions. COFFE contains 398 and 358 problems for function-level and file-level code generation, respectively. To improve the distinguishability, we design a novel stressful test case generation approach with contracts and two new formats of test cases to improve the accuracy of generation. For the time evaluation metric, we propose efficienct@k based on CPU instruction count to ensure a stable and solid comparison between different solutions. We evaluate 14 popular LLMs on COFFE and identify four findings. Based on the findings, we draw some implications for LLM researchers and software practitioners to facilitate future research and usage of LLMs in code generation.

## 3. Demystifying LLM-based Software Engineering Agents

**Authors:** Chunqiu Steven Xia (University of Illinois at Urbana-Champaign), Yinlin Deng (University of Illinois at Urbana-Champaign), Soren Dunn (University of Illinois Urbana-Champaign), Lingming Zhang (University of Illinois at Urbana-Champaign)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715754

**中文总结:** 提出无需复杂自主智能体的 Agentless，仅用定位、修复、补丁验证三阶段解决软件开发问题；在 SWE-bench Lite 上达到 32.67%（98 个正确修复）且成本约 $0.68，优于现有开源软件智能体，并被 OpenAI 用作展示基准。

**Abstract:** Recent advancements in large language models (LLMs) have significantly advanced the automation of software development tasks, including code synthesis, program repair, and test generation. More recently, researchers and industry practitioners have developed various autonomous LLM agents to perform end-to-end software development tasks. These agents are equipped with the ability to use tools, run commands, observe feedback from the environment, and plan for future actions. However, the complexity of these agent-based approaches, together with the limited abilities of current LLMs, raises the following question: Do we really have to employ complex autonomous software agents? To attempt to answer this question, we build Agentless – an agentless approach to automatically resolve software development issues. Compared to the verbose and complex setup of agent-based approaches, Agentless employs a simplistic three-phase process of localization, repair, and patch validation, without letting the LLM decide future actions or operate with complex tools. Our results on the popular SWE-bench Lite benchmark show that surprisingly the simplistic Agentless is able to achieve both the highest performance (32.67%, 98 correct fixes) and low cost ($0.68) compared with all existing open-source software agents! In fact, Agentless has already been adopted by OpenAI as the go-to approach to showcase the real-world coding performance of both GPT-4o and the new OpenAI o1 models . Furthermore, we manually classified the problems in SWE-bench Lite and found problems with exact ground truth patches or insufficient/misleading issue descriptions. As such, we construct SWE-bench Lite-𝑆 by excluding such problematic issues to perform more rigorous evaluation and comparison. Our work highlights the currently overlooked potential of a simplistic, cost-effective technique in autonomous software development. We hope Agentless will help reset the baseline, starting point, and horizon for autonomous software agents, and inspire future work along this crucial direction.

## 4. Expressing and Checking Statistical Assumptions

**Authors:** Alexi Turcotte (CISPA), Zheyuan Wu (Saarland University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729391

**中文总结:** 提出为统计库函数标注假设并自动插入假设检验的方法，实现为 Python/R 工具 prob-check-py 与 prob-check-r。在 128 个 Kaggle notebook 中发现 84.38% 至少违反一项假设，且在 11.51% 情形下若选对检验会得出不同结论。

**Abstract:** Literate programming environments like Jupyter and R Markdown notebooks, coupled with easy-to-use languages like Python and R, put a plethora of statistical methods right at a data analyst’s fingertips. But are these methods being used correctly? Statistical methods make statistical assumptions about samples being analyzed, and in many cases produce reasonable looking results even if assumptions are not met. We propose an approach that allows library developers to annotate functions with statistical assumptions, phrases them as hypotheses about the data, and inserts hypothesis tests investigating the likelihood that the assumption is met. As a proof of concept, we implement this approach in two tools: prob-check-py for Python, and prob-check-r for R. To evaluate these, we identify common hypothesis testing and statistical modeling functions in Python and R, annotate them with the relevant statistical assumptions, and run 128 Kaggle notebooks that use those methods to identify misuses. Our investigation reveals that at least one statistical assumption was violated in 84.38% of surveyed notebooks, and that assumptions were violated in 53.36% of calls to annotated functions. Moreover, had the appropriate hypothesis testing method been chosen given the characteristics of the data, a different conclusion would have been drawn in 11.51% of cases.

## 5. Gleipner: A Benchmark for Gadget Chain Detection in Java Deserialization Vulnerabilities

**Authors:** Bruno Kreyssig (Umeå University), Alexandre Bartel (Umeå University)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715711

**中文总结:** 归纳 Java 反序列化 gadget chain 检测的主要挑战，并构建首个大规模系统性合成基准 Gleipner。用其对七种既有方法评测，表明该基准能透明衡量工具成熟度，且现有工具仍难以应对多数挑战。

**Abstract:** While multiple recent publications on detecting Java Deserialization Vulnerabilities highlight an increasing relevance of the topic, until now no proper benchmark has been established to evaluate the individual approaches. Hence, it has become increasingly difficult to show improvements over previous tools and trade-offs that were made. In this work, we synthesize the main challenges in gadget chain detection. More specifically, this unveils the constraints program analysis faces in the context of gadget chain detection. From there, we develop Gleipner: the first synthetic, large-scale and systematic benchmark to validate the effectiveness of algorithms for detecting gadget chains in the Java programming language. We then benchmark seven previous publications in the field using Gleipner. As a result, it shows, that (1) our benchmark provides a transparent, qualitative, and sound measurement for the maturity of gadget chain detecting tools, (2) Gleipner alleviates severe benchmarking flaws which were previously common in the field and (3) state-of-the-art tools still struggle with most challenges in gadget chain detection.

## 6. Hallucination Detection in Large Language Models with Metamorphic Relations

**Authors:** Borui Yang (Beijing University of Posts ad Telecommunications), Md Afif Al Mamun (University of Calgary), Jie M. Zhang (King's College London), Gias Uddin (York University, Canada)

**Categories:** Software Engineering for AI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715735

**中文总结:** 提出无需外部资源的幻觉检测方法 MetaQA，利用蜕变关系与提示变异检测 LLM 回答是否自洽。在开源与闭源 LLM 上均优于 SelfCheckGPT，F1 提升幅度可达 0.154–0.368。

**Abstract:** Large Language Models (LLMs) are prone to hallucinations, e.g., factually incorrect information, in their responses. These hallucinations present challenges for LLM-based applications that demand high factual accuracy. Existing hallucination detection methods primarily depend on external resources, which can suffer from issues such as low availability, incomplete coverage, privacy concerns, high latency, low reliability, and poor scalability. There are also methods depending on output probabilities, which are often inaccessible for closed-source LLMs like GPT models. This paper presents MetaQA, a self-contained hallucination detection approach that leverages metamorphic testing and prompt mutation. Unlike existing methods, MetaQA operates without any external resources and is compatible with both open-source and closed-source LLMs. MetaQA is based on the hypothesis that if an LLM’s response is a hallucination, the designed metamorphic relations will be violated. We compare MetaQA with the state-of-the-art zero-resource hallucination detection method, SelfCheckGPT, across multiple datasets, and on two open-source and two closed-source LLMs. Our results reveal that MetaQA outperforms SelfCheckGPT in terms of precision, recall, and f1 score. For the four LLMs we study, MetaQA outperforms SelfCheckGPT with a superiority margin ranging from 0.041 - 0.113 (for precision), 0.143 - 0.430 (for recall), and 0.154 - 0.368 (for F1-score). For instance, with Mistral-7B, MetaQA achieves an average F1-score of 0.435, compared to SelfCheckGPT’s F1-score of 0.205, representing an improvement rate of 112.2%. MetaQA also demonstrates superiority across all different categories of questions.

## 7. Less is More: On the Importance of Data Quality for Unit Test Generation

**Authors:** Junwei Zhang (Zhejiang University), Xing Hu (Zhejiang University), Shan Gao (Huawei), Xin Xia (Zhejiang University), David Lo (Singapore Management University), Shanping Li (Zhejiang University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715778

**中文总结:** 系统梳理单元测试生成数据集中的噪声类型，并提出自动清洗框架 CleanTest。Methods2Test/Atlas 中噪声占比达 43.52%/29.65%；过滤后微调多种 LLM，在 Defects4J 上分支覆盖平均提升 67%/39%，缺陷检测亦改善。

**Abstract:** Unit testing is crucial for software development and maintenance. Effective unit testing ensures and improves software quality, but writing unit tests is time-consuming and labor-intensive. Recent studies have proposed deep learning (DL) techniques or large language models (LLMs) to automate unit test generation. These models are usually trained or fine-tuned on large-scale datasets. Despite growing awareness of the importance of data quality, there has been limited research on the quality of datasets used for test generation. To bridge this gap, we systematically examine the impact of noise on the performance of learning-based test generation models. We first apply the open card sorting method to analyze the most popular and largest test generation dataset, Methods2Test, to categorize eight distinct types of noise. Further, we conduct detailed interviews with 17 domain experts to validate and assess the importance, reasonableness, and correctness of the noise taxonomy. Then, we propose CleanTest, an automated noise-cleaning framework designed to improve the quality of test generation datasets. CleanTest comprises three filters: a rule-based syntax filter, a rule-based relevance filter, and a model-based coverage filter. To evaluate its effectiveness, we apply CleanTest on two widely-used test generation datasets, i.e., Methods2Test and Atlas. Our findings indicate that 43.52% and 29.65% of datasets contain noise, highlighting its prevalence. Finally, we conduct comparative experiments using four LLMs (i.e., CodeBERT, AthenaTest, StarCoder, and CodeLlama7B) to assess the impact of noise on test generation performance. The results show that filtering noise positively influences the test generation ability of the models. Fine-tuning the four LLMs with the filtered Methods2Test dataset, on average, improves its performance by 67% in branch coverage, using the Defects4J benchmark. For the Atlas dataset, the four LLMs improve branch coverage by 39%. Additionally, filtering noise improves bug detection performance, resulting in a 21.42% increase in bugs detected by the generated tests.

## 8. Mystique: Automated Vulnerability Patch Porting with Semantic and Syntactic-Enhanced LLM

**Authors:** Susheng Wu (Fudan University), Ruisi Wang (Fudan University), Bihuan Chen (Fudan University), Zhuotong Zhou (Fudan University), Yiheng Huang (Fudan University), JunPeng Zhao (Fudan University), Xin Peng (Fudan University)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715718

**中文总结:** Mystique 用语义切片与语法约束提取漏洞相关签名，再经微调 LLM 生成并迭代校验修补后的函数，实现跨分支漏洞补丁移植。函数级成功率 0.954、CVE 级 0.924，优于现有方法至少 12%+，并成功移植 34 个真实脆弱分支。

**Abstract:** Branching repositories facilitates efficient software development but can also inadvertently propagate vulnerabilities. When an original branch is patched, other unfixed branches remain vulnerable unless the patch is successfully ported. However, due to inherent discrepancies between branches, many patches cannot be directly applied and require manual intervention, which is time-consuming and leads to delays in patch porting, increasing vulnerability risks. Existing automated patch porting approaches are prone to errors, as they often overlook essential semantic and syntactic context of vulnerability and fail to detect or refine faulty patches. We propose Mystique, a novel LLM-based approach to address these limitations. Mystique first slices the semantic-related statements linked to the vulnerability while ensuring syntactic correctness, allowing it to extract the signatures for both the original patched function and the target vulnerable function. Mystique then utilizes a fine-tuned LLM to generate a fixed function, which is further iteratively checked and refined to ensure successful porting. Our evaluation shows that Mystique achieved a success rate of 0.954 at function level and of 0.924 at CVE level, outperforming state-of-the-art approaches by at least 13.2% at function level and 12.3% at CVE level. Our evaluation also demonstrates Mystique’s superior generality across various projects, bugs, and programming languages. Mystique successfully ported patches for 34 real-world vulnerable branches.

## 9. PDCAT: Preference-Driven Compiler Auto-Tuning

**Authors:** Mingxuan Zhu (Peking University), Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Dan Hao (Peking University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715756

**中文总结:** PDCAT 通过文档中的组合约束、公共/探索优化划分，以及偏置的启用概率，压缩编译器优化序列搜索空间。在 GCC 最新版与 cBench/PolyBench 上显著优于含 SRTuner 在内的四种方法，且各组件可提升对照技术的加速效果。

**Abstract:** Compilers are crucial software tools that usually convert programs in high-level languages into machine code. A compiler provides hundreds of optimizations to improve the performance of the compiled code, which are controlled by enabled or disabled optimization flags. However, the vast number of combinations of these flags makes it extremely challenging to select the desired settings for compiler optimization flags (i.e., an optimization sequence) for a given target program. In the literature, many auto-tuning techniques have been proposed to select a desired optimization sequence via different strategies across the entire optimization space. However, due to the huge optimization space, these techniques commonly suffer from the widely-recognized efficiency problem. To address this problem, in this paper, we propose a preference-driven selection approach PDCAT, which reduces the search space of optimization sequences through the following three components. In particular, PDCAT first identifies combined optimizations based on compiler documentation to exclude the optimization sequences violating the combined constraints, and then categorizes the optimizations into a common optimization set (whose optimization flags are fixed) and an exploration set containing the remaining optimizations. Finally, within the search process, PDCAT assigns distinct enable probabilities to the explored optimization flags and finally selects a desired optimization sequence. The former two components reduce the search space by removing invalid optimization sequences and fixing some optimization flags, whereas the latter performs a biased search in the search space. To evaluate the performance of the proposed approach PDCAT, we conduct an extensive experimental study on the latest version of the compiler GCC with two widely used benchmarks cBench and PolyBench. The results show that PDCAT significantly outperforms the four compared techniques, including the state-of-art technique SRTuner. Moreover, each component of PDCAT not only contributes to its performance but also improves the acceleration performance of compared techniques.

## 10. Pinning Is Futile: You Need More Than Local Dependency Versioning to Defend Against Supply Chain Attacks

**Authors:** Hao He (Carnegie Mellon University), Bogdan Vasilescu (Carnegie Mellon University), Christian Kästner (Carnegie Mellon University)

**Categories:** Security and Vulnerability

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available, Artifact-Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715728

**中文总结:** 通过对 npm 历史依赖解析的反事实模拟，发现固定直接依赖版本不仅增加维护过时/脆弱依赖的成本，在大图中还可能因 npm 解析机制提高暴露恶意更新的风险。论文进一步探讨集体 pinning 策略，并为生态与工具设计给出建议。

**Abstract:** Recent high-profile incidents in open-source software have greatly raised practitioner attention on software supply chain attacks. To guard against potential malicious package updates, security practitioners advocate pinning dependency to specific versions rather than floating in version ranges. However, it remains controversial whether pinning carries a meaningful security benefit that outweighs the cost of maintaining outdated and possibly vulnerable dependencies. In this paper, we quantify, through counterfactual analysis and simulations, the security and maintenance impact of version constraints in the npm ecosystem. By simulating dependency resolutions over historical time points, we find that pinning direct dependencies not only (as expected) increases the cost of maintaining vulnerable and outdated dependencies, but also (surprisingly) even increases the risk of exposure to malicious package updates in larger dependency graphs due to the specifics of npm’s dependency resolution mechanism. Finally, we explore collective pinning strategies to secure the ecosystem against supply chain attacks, suggesting specific changes to npm to enable such interventions. Our study provides guidance for practitioners and tool designers to manage their supply chains more securely.

## 11. QSF: Multi-Objective Optimization based Efficient Solving for Floating-Point Constraints

**Authors:** Xu Yang (College of Computer Science and Technology, National University of Defense Technology), Zhenbang Chen (College of Computer, National University of Defense Technology), Wei Dong (National University of Defense Technology), Ji Wang (National University of Defense Technology)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715739

**中文总结:** QSF 将浮点约束求解建模为多目标优化（未满足约束数量与违规模之和），并设计面向浮点数的进化变异算子。在 SMT-COMP 与真实浮点程序基准上相对 SOTA 加速可达数十至上百倍，并提升浮点程序符号执行性能。

**Abstract:** Floating-point constraint solving is challenging due to the complex representation and non-linear computations. Search-based constraint solving provides an effective method for solving floating-point constraints. In this paper, we propose QSF to improve the efficiency of search-based solving for floating-point constraints. The key idea of QSF is to model the floating-point constraint solving problem as a multi-objective optimization problem. Specifically, QSF considers both the number of unsatisfied constraints and the sum of the violation degrees of unsatisfied constraints as the objectives for search-based optimization. Besides, we propose a new evolutionary algorithm in which the mutation operators are specially designed for floating-point numbers, aiming to solve the multi-objective problem more efficiently. We have implemented QSF and conducted extensive experiments on both the SMT-COMP benchmark and the benchmark from real-world floating-point programs. The results demonstrate that compared to SOTA floating-point solvers, QSF achieved an average speedup of 15.72X under a 60-second timeout and an impressive 87.48X under a 600-second timeout on the first benchmark. Similarly, on the second benchmark, QSF delivered an average speedup of 25.74X and 106.76X, respectively, under the two timeout configurations. Furthermore, QSF has also enhanced the performance of symbolic execution for floating-point programs.

## 12. UnitCon: Synthesizing Targeted Unit Tests for Java Runtime Exceptions

**Authors:** Sujin Jang (KAIST), Yeonhee Ryou (KAIST), Heewon Lee (KAIST, Korea, South (The Republic of)), Kihong Heo (KAIST)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729362

**中文总结:** 提出 UNITCON，用静态分析估计候选测试语义以剪枝与排序搜索空间，合成针对 Java 运行时异常特定位置的定向单元测试。在 Java 程序集上显著优于现有面向回归覆盖的单元测试生成工具。

**Abstract:** We present UNITCON, a system for synthesizing targeted unit tests for runtime exceptions in Java programs. Targeted unit tests aim to reveal a bug at a specific location in the program under test. This capability benefits various tasks in software development, such as patch testing, crash reproduction, or static analysis alarm inspection. However, conventional unit test generation tools are mainly designed for regression tests by maximizing code coverage; hence they are not effective at such target-specific tasks. In this paper, we propose a novel synthesis technique that effectively guides the search for targeted unit tests. The key idea is to use static analysis to prune and prioritize the search space by estimating the semantics of candidate test cases. This allows us to efficiently focus on promising unit tests that are likely to reveal the target Exception. According to our experiments on a suite of Java programs, our approach significantly outperforms the state-of-the-art unit test generation tools.

## 13. Why the Proof Fails in Different Versions of Theorem Provers: An Empirical Study of Compatibility Issues in Isabelle

**Authors:** Xiaokun Luan (Peking University), David Sanan (Singapore Institute of Technology), Zhe Hou (Griffith University), Qiyuan Xu (Nanyang Technological University), Chengwei Liu (Nanyang Technological University), Yufan Cai (National University of Singapore), Yang Liu (Nanyang Technological University), Meng Sun (Peking University)

**Categories:** Program Analysis and Verification

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715787

**中文总结:** 以 Isabelle 为例，构建回归测试框架从 Archive of Formal Proofs 自动收集 12,079 个证明助手版本兼容性问题，归纳类型、症状、根因与修复策略。为缓解形式化证明维护中的兼容性障碍提供实证基础。

**Abstract:** Proof assistants are software tools for formal modeling and verification of software, hardware, design, and mathematical proofs. Due to the growing complexity and scale of formal proofs, compatibility issues frequently arise when using different versions of proof assistants. These issues result in broken proofs, disrupting the maintenance of formalized theories and hindering the broader dissemination of results within the community. Although existing works have proposed techniques to address specific types of compatibility issues, the overall characteristics of these issues remain largely unexplored. To address this gap, we conduct the first extensive empirical study to characterize compatibility issues, using Isabelle as a case study. We develop a regression testing framework to automatically collect compatibility issues from the Archive of Formal Proofs, the largest repository of formal proofs in Isabelle. By analyzing 12,079 collected issues, we identify their types and symptoms and further investigate their root causes. We also extract updated proofs that address these issues to understand the applied resolution strategies. Our study provides an in-depth understanding of compatibility issues in proof assistants, offering insights that support the development of effective techniques to mitigate these issues.
