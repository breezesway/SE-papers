# ICSE 2026 Research Track — Software Engineering for AI

Source: https://conf.researchr.org/track/icse-2026/icse-2026-research-track?#event-overview

Total in this category: 29 papers

## 1. A Comprehensive Study of Deep Learning Model Fixing Approaches

**Authors:** Hanmo You (Tianjin University), Zan Wang (Tianjin University), Zishuo Dong (College of Intelligence and Computing, Tianjin University), Luanqi Mo (College of Intelligence and Computing, Tianjin University), Jianjun Zhao (Kyushu University), Junjie Chen (Tianjin University)

**Categories:** Software Engineering for AI

**Awards:** Distinguished Paper Award

**中文总结:** 对 16 种深度学习模型修复方法开展大规模实证，覆盖模型/层/神经元级修复及其对鲁棒性、公平性与向后兼容性的影响；发现模型级修复最有效，但尚无方法能同时最优修复并保持所有其他性质。

**Abstract:** Deep Learning (DL) has been widely adopted in diverse industrial domains, including autonomous driving, intelligent healthcare, and aided programming. Like traditional software, DL systems are also prone to faults, whose malfunctioning may expose users to significant risks. Consequently, numerous approaches have been proposed to address these issues. In this paper, we conduct a large-scale empirical study on 16 state-of-the-art DL model fixing approaches, spanning model-level, layer-level, and neuron-level categories, to comprehensively evaluate their performance. We assess not only their fixing effectiveness (their primary purpose) but also their impact on other critical properties, such as robustness, fairness, and backward compatibility. To ensure comprehensive and fair evaluation, we employ a diverse set of datasets, model architectures, and application domains within a uniform experimental setup for experimentation. We summarize several key findings with implications for both industry and academia. For example, model-level approaches demonstrate superior fixing effectiveness compared to others. No single approach can achieve the best fixing performance while improving accuracy and maintaining all other properties. Thus, academia should prioritize research on mitigating these side effects. These insights highlight promising directions for future exploration in this field.

## 2. A First Look at Model Supply Chain: From the Risk Perspective

**Authors:** Ziqian Chen (Fudan University), Zekai Chen (Fudan University), Susheng Wu (Fudan University), Bihuan Chen (Fudan University), Wenyan Song (Carnegie Mellon University), Yiheng Huang (Fudan University), Zhuotong Zhou (Fudan University), Yiheng Cao (Fudan University), Xin Peng (Fudan University)

**Categories:** Software Engineering for AI

**中文总结:** 基于 Hugging Face 构建首个 182 万模型、54 万依赖关系的模型供应链图谱并系统刻画使用、演化、质量与风险，为模型维护者、消费者与平台设计提供可操作启示。

**Abstract:** The rapid proliferation of publicly available artificial intelligence models on platforms such Hugging Face has formed a complex model supply chain, where base models are continually transformed, e.g., by fine-tuning, quantization, and merging, into new derived models. Despite its critical importance for reuse, provenance, and risk management, this supply chain remains poorly characterized at scale. We construct the first comprehensive model supply chain based on models on Hugging Face as of June 25, 2025, which consists of 1.82 million models as well as 0.54 million dependency relations. Then, we conduct the first systematic study to characterize the usage, evolution, quality, and risk of this model supply chain. Finally, we provide actionable implications for model maintainers, consumers, platform designers, and researchers to foster this new direction in the era of AI.

## 3. A Semantic-based Optimization Approach for Repairing LLMs: Case Study on Code Generation

**Authors:** Jian Gu (Monash University), Aldeida Aleti (Monash University), Chunyang Chen (TU Munich), Hongyu Zhang (Chongqing University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 STAR 语义靶向 LLM 修复方法，通过统计归因定位缺陷神经元并用解析公式计算补丁；较 MINT/SGD 修复成功率更高、速度提升 2.4–7.0 倍且副作用更小。

**Abstract:** Language Models (LMs) are widely used in software engineering for code generation, but they may produce code with errors. Rather than repairing the generated code, a more thorough way is to address the underlying failures of models. LM repair offers a lightweight solution to this challenge: it requires minimal data, reduces computational costs, and reduces the side effects. Unlike full retraining, LM repair focuses on applying tailored updates to targeted neurons, making it ideal for scenarios with limited resources, high-performance demands, or strict safety requirements. In this paper, we propose \ul{S}emantic \ul{T}argeting for \ul{A}nalytical \ul{R}epair (\textsc{STAR}), a pioneering and novel semantic-based optimization approach for repairing LLMs. \textsc{STAR} realizes the main operations of repairing LMs in an optimization process, including locating buggy neurons'', solving neuron patches'', and patching ``buggy neurons''. Correspondingly, it computes the deltas of weight matrix as the prior information to guide optimization; and attributes the targeted layers and neurons leveraging statistical insights. The neuron patches are computed with a solid semantic-based analytical formula, which directly bridges the changes to logits with the deltas of neurons, by steering latent representations. Compared to the prior work of LM repair (\textsc{MINT}) and optimization methods (\textsc{SGD}), \textsc{STAR} integrates their strengths while mitigating their limitations. By implementing LM repair as an optimization-based process, \textsc{STAR} supports solving multiple failures together, significantly improving the usefulness. Evaluated on coding tasks using popular code LMs, \textsc{STAR} demonstrates superior effectiveness compared with the state-of-the-art. For instance, on CoNaLa, \textsc{STAR} obtained $10.5% \sim 19.9%$ improvements in ExactMatch score. Besides, \textsc{STAR} exhibits better efficiency, achieving an average speedup of $2.4 \sim 7.0$ times in solving each model failure. In terms of side effects, namely the balance between generalization and specificity, \textsc{STAR} outperforms prior work by a significant margin. Additionally, we conducted assessments on the overfitting risk of LM repair as well as the cumulative impact. Further, we analyzed the differences with pipeline-based methods and explained the reason why \textsc{STAR} is better and how it mitigated the common limitations of LM repair.

## 4. AgentSpec: Customizable Runtime Enforcement for Safe and Reliable LLM Agents

**Authors:** Haoyu Wang (School of Computing and Information Systems, Singapore Management University), Chris Poskitt (Singapore Management University), Jun Sun (Singapore Management University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 AgentSpec 领域特定语言，以触发器-谓词-执行机制在运行时约束 LLM agent；在代码/具身/自动驾驶场景分别阻止 90%+ 不安全执行、消除全部危险动作并实现 AV 100% 合规。

**Abstract:** Agents built on LLMs are increasingly deployed across diverse domains, automating complex decision-making and task execution. However, their autonomy introduces safety risks, including security vulnerabilities, legal violations, and unintended harmful actions. Existing mitigation methods, such as model-based safeguards and early enforcement strategies, fall short in robustness, interpretability, and adaptability. To address these challenges, we propose AgentSpec, a lightweight domain-specific language for specifying and enforcing runtime constraints on LLM agents. With AgentSpec, users define structured rules that incorporate triggers, predicates, and enforcement mechanisms, ensuring agents operate within predefined safety boundaries. We implement AgentSpec across multiple domains, including code execution, embodied agents, and autonomous driving, demonstrating its adaptability and effectiveness. Our evaluation shows that AgentSpec successfully prevents unsafe executions in over 90% of code agent cases, eliminates all hazardous actions in embodied agent tasks, and enforces 100% compliance by autonomous vehicles (AVs). Despite its strong safety guarantees, AgentSpec remains computationally lightweight, with overheads in milliseconds. By combining interpretability, modularity, and efficiency, AgentSpec provides a practical and scalable solution for enforcing LLM agent safety across diverse applications. We also automate the generation of rules using LLMs and assess their effectiveness. Our evaluation shows that the rules generated by OpenAI o1 achieve a precision of 95.56% and recall of 70.96% for embodied agents, successfully identify 87.26% of the risky code, and prevent AVs from breaking laws in 5 out of 8 scenarios.

## 5. Aligning Requirement for Large Language Model's Code Generation

**Authors:** Zhao Tian (Tianjin University), Junjie Chen (Tianjin University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 Specine，借鉴需求工程对齐 LLM 对编程规格的理解，识别错位规格并提升 LLM 感知规格；在四个 LLM 与五个竞赛基准上 Pass@1 平均较最强基线提升 29.60%。

**Abstract:** Code generation refers to the automatic generation of source code based on a given programming specification, which has garnered significant attention particularly with the advancement of large language models (LLMs). However, due to the inherent complexity of real-world problems, the LLM-generated code often fails to fully align with the provided specification. While state-of-the-art agent-based techniques have been proposed to enhance LLM code generation, they overlook the critical issue of specification perception, resulting in persistent misalignment issues. Given that accurate perception of programming specifications serves as the foundation of the LLM-based code generation paradigm, ensuring specification alignment is particularly crucial. In this work, we draw on software requirement engineering to propose Specine, a novel specification alignment technique for LLM code generation. Its key idea is to identify misaligned input specifications, lift LLM-perceived specifications, and align them to enhance the code generation performance of LLMs. Our comprehensive experiments on four state-of-the-art LLMs across five challenging competitive benchmarks by comparing with ten state-of-the-art baselines, demonstrate the effectiveness of Specine. For example, Specine outperforms the most effective baseline, achieving an average improvement of 29.60% across all subjects in terms of Pass@1.

## 6. AtPatch: Debugging Transformers via Hot-Fixing Over-Attention

**Authors:** Shihao Weng (Nanjing University), Yang Feng (Nanjing University), Jincheng Li (Nanjing University), Yining Yin (Nanjing University), Xiaofei Xie (Singapore Management University), Jia Liu (Nanjing University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 AtPatch，借鉴热补丁思想在推理时动态重分配 Transformer 注意力图以缓解后门与不公平 over-attention；无需改参或重训，较现有方法更有效且更好保留原功能。

**Abstract:** Transformer-based deep neural networks (DNNs) affected by backdoor attacks and unfairness typically exhibit anomalous attention patterns, leading to over-attend to backdoor triggers or protected attributes. Existing neuron-editing mitigation strategies often struggle to handle such situation and most of them lack flexibility and tend to distort feature representations. Motivated by such over-attention phenomenon and software engineering paradigms such as delta debugging and hot patching, we propose AtPatch, a hot-fix method that dynamically redistributes attention maps during model inference. Specifically, for a given input, AtPatch first extracts the attention map from the model’s inference process. Then, it uses a pre-trained detector to identify anomalous columns and replace them with unified benign attention. Then, AtPatch rescales other columns to mitigate the impact of over-attention. Finally, AtPatch returns the redistributed attention map to the model for continued inference. Notably, if the detector does not report any anomalous columns, AtPatch directly returns the original attention map to the model. Unlike existing techniques, AtPatch selectively redistributes the attention map, making it better at preserving the model’s original functionality. Furthermore, AtPatch’s on-the-fly nature allows it to work without modifying model parameters or retraining, making it better suited for deployed models. We conducted extensive experiments to validate AtPatch. Experimental results show that, compared to existing methods, AtPatch can more effectively mitigate backdoor attacks and unfairness while better preserving the model’s original functionality.

## 7. Attention Pruning: Automated Fairness Repair of Language Models via Surrogate Simulated Annealing

**Authors:** Vishnu Asutosh Dasu (Pennsylvania State University), Md Rafi Ur Rashid (Pennsylvania State University), Vipul Gupta (Pennsylvania State University), Saeid Tizpaz-Niari (University of Illinois Chicago), Gang (Gary) Tan (Pennsylvania State University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 Attention Pruning，以代理 DNN 建模注意力头状态与公平/效用关系，再用模拟退火搜索最优剪枝子集；性别偏见最多降低 40%，优于 SOTA 偏见缓解策略。

**Abstract:** This paper explores pruning attention heads as a post-processing bias mitigation method for large language models (LLMs). Modern AI systems such as LLMs are expanding into sensitive social contexts and socio-economic decision-making where fairness concerns become especially crucial. Since LLMs develop their decision-making patterns by training on massive datasets of human-generated content, they naturally encode and perpetuate societal biases. While modifying training datasets and algorithms is expensive and requires significant resources, post-processing techniques—such as selectively deactivating attention heads in pre-trained LLMs—can provide feasible and effective approaches to improve fairness. However, identifying the optimal subset of parameters to prune presents a combinatorial challenge within the immense parameter space of LLMs, requiring efficient solutions that efficiently balance competing objectives across the frontiers of model fairness and utility. We explore a search-based program repair approach via simulated annealing to address the computational challenges. Given the prohibitive evaluation costs in billion-parameter LLMs, we develop surrogate deep neural networks that efficiently model the relationship between attention head states (active/inactive) and their corresponding fairness/utility metrics. This allows us to perform optimization over the surrogate models and efficiently identify optimal subsets of attention heads for pruning rather than directly searching through the LLM parameter space. This paper introduces Attention Pruning, a fairness-aware surrogate simulated annealing approach to prune attention heads in LLMs that disproportionately contribute to bias while minimally impacting overall model utility. Our experimental evaluation shows that Attention Pruning achieves a reduction of up to $40%$ in gender bias and outperforms state-of-the-art bias mitigation strategies. Warning: This paper contains content that some readers may find offensive and harmful.

## 8. Beyond Correctness: Exposing LLM-generated Logical Flaws in Reasoning via Multi-step Automated Theorem Proving

**Authors:** Xinyi Zheng (Huazhong University of Science and Technology), Ningke Li (National University of Singapore), Xiaokun Luan (Peking University), Kailong Wang (Huazhong University of Science and Technology), Ling Shi (Nanyang Technological University), Meng Sun (Peking University), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI

**中文总结:** 提出 MATP，将 NL 推理译为 FOL 并用自动定理证明逐步验证逻辑有效性；在 10,830 条推理实例上较 prompting 基线步骤验证提升 42 个百分点以上。

**Abstract:** Large Language Models (LLMs) have demonstrated impressive reasoning capabilities, leading to their adoption in high-stakes domains such as healthcare, law, and scientific research. However, their reasoning often contains subtle logical errors masked by fluent language, posing significant risks for critical applications. While existing approaches like fact-checking, self-consistency methods, and rule-based validation provide partial solutions, they fail to detect complex logical flaws in multi-step reasoning. To overcome these challenges, we present MATP, an evaluation framework for systematically verifying LLM reasoning via Multi-step Automatic Theorem Proving. MATP translates natural language reasoning into First-Order Logic (FOL) and applies automated theorem provers to assess step-by-step logical validity. This approach identifies hidden logical errors and provides fine-grained classifications of reasoning correctness. Evaluations on a benchmark comprising 10,830 reasoning instances generated by 10 LLMs across tasks from PrOntoQA-OOD, ProofWriter, and FOLIO show that MATP surpasses prompting-based baselines by over 42 percentage points in reasoning step verification. It further reveals model-level disparities, with reasoning models generating more logically coherent outputs than general models. These results demonstrate MATP’s potential to enhance the trustworthiness of LLM-generated reasoning.

## 9. Checking Unsupervised Learning for Nondeterminism and Inconsistency via SMT Solving

**Authors:** Muyeed Ahmed (New Jersey Institute of Technology), Iulian Neamtiu (New Jersey Institute of Technology)

**Categories:** Software Engineering for AI

**中文总结:** 提出 Ocelot，将无监督学习实现的非确定/不一致检查归约为 Z3 可满足性，自动隔离非确定 kernel 并生成 witness 数据集；在 Scikit-learn/MATLAB/R 多种聚类与异常检测算法中暴露问题与回归。

**Abstract:** Unsupervised Learning (UL) implementations are widely used, but prone to issues such as nondeterminism and inconsistency, which makes them unreliable and exploitable. Moreover, the lack of a specification (or ground truth) makes UL implementations hard to verify or test: when they produce diverging results on a dataset, they do so subtly and silently, which gives users a false sense of security, and complicates developers’ job of tracing the error to its root cause. We introduce an approach, Ocelot, that reduces nondeterminism/inconsistency checking to satisfiability checking in Z3. Given the Python code of an UL implementation, Ocelot automatically isolates a nondeterministic “kernel” (variables and code), which forms the basis for a Z3 specification. A Z3-found solution acts as a “witness” dataset – a typically small dataset that can be used to reliably reproduce the error. Ocelot has exposed sources of nondeterminism and inconsistency in popular implementations (Scikit-learn, MATLAB, and R) of well-known Clustering algorithms (Affinity Propagation, DBSCAN, HAC, and K-means) and Anomaly Detection algorithms (Isolation Forest, Local Outlier Factor). Moreover, Ocelot has exposed regressions (changes in semantics) in the evolution of these implementations.

## 10. Comfrey: Mitigating Integration Failures in LLM-enabled Software at Run-Time

**Authors:** Yuchen Shao (East China Normal University, Shanghai Innovation Institute), Yuheng Huang (The University of Tokyo), Jiazhen Zou (East China Normal University), Yuling Shi (Shanghai Jiao Tong University), Long Yang (East China Normal University), Lei Ma (The University of Tokyo & University of Alberta), Ting Su (East China Normal University), Chengcheng Wan (East China Normal University)

**Categories:** Software Engineering for AI

**中文总结:** 提出运行时中间层 Comfrey，自动检测并修复 LLM/RAG 与软件组件的集成失败；在开源应用中检测75.1%、阻止63.3%潜在失败，开销仅8.4%。

**Abstract:** Due to the unrestricted outputs of LLMs and strict requirements of software components, integration failures are widespread in software that incorporates LLM agents and retrieval-augmented generation (RAG). Even seemingly correct LLM/RAG responses can trigger software misbehaviors if they violate these requirements. In this paper, we conduct an empirical study to understand integration failures in real-world LLM-enabled applications. Guided by this study, we present Comfrey, a runtime framework that adapts the LLM agent and RAG responses to meet software requirements, serving as a middle layer between AI and software components. It automatically detects and resolves potential integration failures through a three-stage workflow, ensuring component compatibility. Our evaluation with a variety of open-source applications demonstrates that Comfrey detects 75.1% and prevents 63.3% of potential integration failures with 8.4% overhead, significantly outperforming the baselines. The artifact is available on Anonymous GitHub.

## 11. DNN Modularization via Activation-Driven Training

**Authors:** Tuan Ngo (University of Southern California), Abid Hassan (University of Southern California), Saad Shafiq (University of Southern California), Nenad Medvidović (University of Southern California)

**Categories:** Software Engineering for AI

**中文总结:** 提出激活驱动模块化训练 MODA，通过层激活调节实现 DNN 内在模块化；训练时间少22%，模块权重重叠少至1/24，替换模块时目标类精度平均提升12%。

**Abstract:** Deep Neural Networks (DNNs) tend to accrue technical debt and suffer from significant retraining costs when adapting to evolving requirements. Modularizing DNNs offers the promise of improving their reusability. Previous work has proposed techniques to decompose DNN models into modules both during and after training. However, these strategies yield several shortcomings, including significant weight overlaps and accuracy losses across modules, restricted focus on convolutional layers only, and added complexity and training time by introducing auxiliary masks to control modularity. In this work, we propose MODA, an activation-driven modular training approach. MODA promotes inherent modularity within a DNN model by directly regulating the activation outputs of its layers based on three modular objectives: intra-class affinity, inter-class dispersion, and compactness. MODA is evaluated using three well-known DNN models and five datasets with varying sizes. This evaluation indicates that, compared to the existing state-of-the-art, using MODA yields several advantages: (1) MODA accomplishes modularization with 22% less training time; (2) the resultant modules generated by MODA comprise up to 24x fewer weights and 37x less weight overlap while (3) preserving the original model’s accuracy without additional fine-tuning; in module replacement scenarios, (4) MODA improves the accuracy of a target class by 12% on average while ensuring minimal impact on the accuracy of other classes.

## 12. Evaluating the effectiveness of LLM-based interoperability

**Authors:** Rodrigo Falcão (Fraunhofer IESE), Stefan Schweitzer (Fraunhofer Institute for Experimental Software Engineering), Julien Siebert (Fraunhofer IESE), Emily Calvet (Fraunhofer Institute for Experimental Software Engineering), Frank Elberzhager (Fraunhofer Institute for Experimental Software Engineering)

**Categories:** Software Engineering for AI

**中文总结:** 评估13个开源 LLM 在农业互操作场景下运行时自主互联；qwen2.5-coder:32b 在 DIRECT/CODEGEN 策略下 pass@1 分别达≥0.99/≥0.89，单位换算场景 CODEGEN 仍有效。

**Abstract:** Background: Systems of systems are becoming increasingly dynamic and heterogeneous, and this adds pressure on the long-standing challenge of interoperability. Besides its technical aspect, interoperability has also an economic side, as development time efforts are required to build the interoperability artifacts. Objectives: With the recent advances in the field of large language models (LLMs), we aim at analyzing the effectiveness of LLM-based strategies to make systems interoperate autonomously, at runtime, without human intervention. Method: We selected 13 open source LLMs and curated four versions of a dataset in the agricultural interoperability use case. We performed three runs of each model with each version of the dataset, using two different strategies. Then we compared the effectiveness of the models and the consistency of their results across multiple runs. Results: qwen2.5-coder:32b was the most effective model using both strategies DIRECT (average pass@1 ≥ 0.99) and CODEGEN (average pass@1 ≥ 0.89) in three out of four dataset versions. In the fourth dataset version, which included an unit conversion, all models using the strategy DIRECT failed, whereas using CODEGEN qwen2.5-coder:32b succeeded with an average pass@1 = 0.75. Conclusion: Some LLMs can make systems interoperate autonomously. Further evaluation in different domains is recommended, and further research on reliability strategies should be conducted.

## 13. Fairness Is Not Just Ethical: Performance Trade-Off via Data Correlation Tuning to Mitigate Bias in ML Software

**Authors:** Ying Xiao, Shangwen Wang (National University of Defense Technology), Sicen Liu (Southern University of Science and Technology), Dingyuan Xue (Southern University of Science and Technology), Xian Zhan (Southern University of Science and Technology), Yepang Liu (Southern University of Science and Technology), Jie M. Zhang (King's College London)

**Categories:** Software Engineering for AI

**中文总结:** 提出预处理偏差缓解方法 CoT，通过 Phi 系数调整数据相关并多目标优化；未特权群体 TPR 平均提升17.5%，SPD/AOD/EOD 等偏差指标平均降超50%。

**Abstract:** Traditional software fairness research typically emphasizes ethical and social imperatives, neglecting that fairness fundamentally represents a core software quality issue arising directly from performance disparities across sensitive user groups. Recognizing fairness explicitly as a software quality dimension yields practical benefits beyond ethical considerations, notably improved predictive performance for unprivileged groups, enhanced out-of-distribution generalization, and increased geographic transferability in real-world deployments. Nevertheless, existing bias mitigation methods face a critical dilemma: while pre-processing methods offer broad applicability across model types, they generally fall short in effectiveness compared to post-processing techniques. To overcome this challenge, we propose Correlation Tuning (CoT), a novel pre-processing approach designed to mitigate bias by adjusting data correlations. Specifically, CoT introduces the Phi-coefficient, an intuitive correlation measure, to systematically quantify correlation between sensitive attributes and labels, and employs multi-objective optimization to address the proxy biases. Extensive evaluations demonstrate that CoT increases the true positive rate of unprivileged groups by an average of \textbf{17.5%} and reduces three key bias metrics, including statistical parity difference (SPD), average odds difference (AOD), and equal opportunity difference (EOD), by more than \textbf{50%} on average. CoT outperforms state-of-the-art methods by three and ten percentage points in single attribute and multiple attributes scenarios, respectively. We will publicly release our experimental results and source code to facilitate future research.

## 14. FM4MC: Improving Feature Models for Microservice Chains—Towards More Efficient Configuration and Validation

**Authors:** Uwe Gropengießer (Technical University of Darmstadt), Paul Wolfart (Technical University of Darmstadt), Julian Liphardt (Technical University of Darmstadt), Max Mühlhäuser (Technical University of Darmstadt)

**Categories:** Software Engineering for AI

**中文总结:** 提出 FM4MC，将微服务链 Feature Model 切片为 PFM 并按复杂度选择性 SAT 求解；典型场景验证加速23×，极端可达1000×。

**Abstract:** AI-based applications deployed as microservice chains pose challenging configuration problems, as their Feature Models (FMs) quickly grow to sizes where state-of-the-art validation approaches become infeasible. We propose FM4MC, a correctness-preserving method that validates such models efficiently by (i) slicing them into Partial Feature Models (PFMs) and (ii) applying SAT solving selectively based on estimated complexity. This combination drastically reduces the number of solver calls while retaining exact results. Our evaluation on synthetic FMs, sampled to reflect realistic heavy-tail size distributions, shows that FM4MC validates large models up to 23× faster in typical scenarios, reaches speedups of more than 100×, and scales in extreme cases even to 1,000× faster than state-of-the-art techniques. These results demonstrate that FM4MC makes configuration and validation feasible for microservice-based AI applications under mission-critical time constraints, where existing approaches become impractical.

## 15. Imitation Game: Reproducing Deep Learning Bugs Leveraging an Intelligent Agent

**Authors:** Mehil Shah (Dalhousie University), Masud Rahman (Dalhousie University), Foutse Khomh (Polytechnique Montréal)

**Categories:** Software Engineering for AI

**中文总结:** 提出 RepGen 智能体，通过 LLM 迭代生成-验证-精炼复现深度学习 bug，在 106 个真实 bug 上复现率 80.19%，较 SOTA 提升约 20%，开发者研究亦显著降时降认知负荷。

**Abstract:** Despite their wide adoption in various domains (e.g., healthcare, finance, software engineering), Deep Learning (DL)-based applications suffer from many bugs, failures, and vulnerabilities. Reproducing these bugs is essential for their resolution, but it is extremely challenging due to the inherent nondeterminism of DL models and their tight coupling with hardware and software environments. According to recent studies, only about 3% of DL bugs can be reliably reproduced using manual approaches. To address these challenges, we present RepGen, a novel, automated, and intelligent approach for reproducing deep learning bugs. RepGen constructs a learning-enhanced context from a project, develops a comprehensive plan for bug reproduction, employs an iterative generate-validate-refine mechanism, and thus generates such code using an LLM that reproduces the bug at hand. We evaluate RepGen on 106 real-world deep learning bugs and achieve a reproduction rate of 80.19%, a 19.81% improvement over the state-of-the-art measure. A developer study involving 27 participants shows that RepGen improves the success rate of DL bug reproduction by 23.35%, reduces the time to reproduce by 56.8%, and lowers participants’ cognitive load.

## 16. MazeBreaker: Multi-Agent Reinforcement Learning for Dynamic Jailbreaking of LLM Security Defenses

**Authors:** Zhihao Lin, Wei Ma (Singapore Management University), Mingyi Zhou (Beihang University), Yanjie Zhao (Huazhong University of Science and Technology), Haoyu Wang (Huazhong University of Science and Technology), Yang Liu (Nanyang Technological University), Jun Wang (Post Luxembourg), Li Li (Beihang University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 MazeBreaker，用多智能体强化学习根据攻击反馈动态越狱 LLM 安全防御，在 13 种模型上效果优于 6 个 SOTA 越狱方法，尤其针对强对齐商业模型。

**Abstract:** In recent years, the application of Large Language Models~(LLMs) has become increasingly widespread, along with growing concerns about their security. To assess the security of LLMs, researchers have proposed various jailbreak attack algorithms, but only rely on the models’ internal information or face limitations in exploring the unsafe behavior, highlighting the need for a more adaptive and generalizable approach. Inspired by the game of rats escaping a maze, we introduce a novel jailbreak attack approach, MazeBreaker, where attackers dynamically learn to find the exit based on feedback and their accumulated experience to compromise the target LLMs’ security defenses. Our method is the first to systematically learn from the feedback of attack attempts on target LLMs through a multi-agent reinforcement learning system, enabling strategic exploration of the model’s unsafe boundaries without a reference oracle. We compared our approach with six state-of-the-art jailbreak attack methods, testing it on 13 different architectures of open-source and commercial models. The results show that our method performs exceptionally well in terms of attack effectiveness, especially for the commercial models (GPT-3.5-turbo, GPT-4o-mini, GLM-4-air and Claude-3.5-sonnet) with strong safety alignment. We hope this study will help academia and industry better test the security of large language models and promote adherence to safety and ethical standards. Code and data are available on our repository: https://anonymous.4open.science/r/MazeBreaker .

## 17. ModularEvo: Evolving Multi-Task Models via Neural Network Modularization and Composition

**Authors:** Wenrui Long (Beihang university), Binhang Qi (Beihang University), Hailong Sun (Beihang University), ZongZhen Yang (Beihang University), Ruobing Zhao (Beihang University), Xiang Gao (Beihang University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 ModularEvo，将多任务 DNN 模块化解耦并按需部署与模块化微调，长期演化场景性能绝对提升 2.34% 且推理加速 2.22 倍。

**Abstract:** Training a general multi-task deep neural network (DNN) model, such as a large language model, and deploying it across diverse downstream tasks has become a common practice. In long-term deployment scenarios, downstream tasks can change over time, such as new data distributions and requirements, leading to the fine-tuning of the model accordingly, i.e., evolving the model. However, traditional full-parameter fine-tuning methods adapt the model to individual tasks, resulting in degradation of the original knowledge. Although parameter-efficient fine-tuning methods could mitigate this problem, they still isolate new knowledge in external, separate parameters. As a result, the base model gains little cumulative benefit from downstream updates. These limitations stem from the indiscriminate model deployment and fine-tuning. Inspired by modular design principles in software engineering, we propose ModularEvo, a framework that enables on-demand deployment and co-evolution of multi-task models and modules across diverse downstream tasks. ModularEvo first decomposes the model into task-specific modules, each retaining a subset of relevant weights and functionality. These modules, instead of the entire model, are deployed on downstream tasks on demand. During long-term deployment, each module is independently optimized to adjust to the change of the corresponding task. Unlike conventional fine-tuning methods, ModularEvo applies modular fine-tuning to update only the task-relevant weights within modules. Furthermore, new knowledge acquired by modules is periodically integrated into the model, enabling the co-evolution of both the model and modules. We evaluate ModularEvo through extensive experiments on three Transformer models and six downstream tasks involving both classification and generation tasks. Results demonstrate the effectiveness of ModularEvo in model performance and inference efficiency in evolution scenarios. Compared to state-of-the-art baselines, ModularEvo achieves an absolute performance gain of 2.34% in multi-round evolution scenarios, and a 2.22 times speedup in inference.

## 18. PreServe: Intelligent Management for LMaaS Systems via Hierarchical Prediction

**Authors:** Zhihan Jiang (The Chinese University of Hong Kong), Yujie Huang (The Chinese University of Hong Kong), Guangba Yu (The Chinese University of Hong Kong), Junjie Huang (The Chinese University of Hong Kong), Jiazhen Gu (Chinese University of Hong Kong), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Software Engineering for AI

**Awards:** Distinguished Paper Award

**中文总结:** 提出 LMaaS 管理框架 PreServe，通过服务负载与请求负载的分层预测构建负载 anticipator，优化资源分配与路由。真实生产数据评估显示尾延迟降低 41.3% 以上、资源消耗平均减少 49.38%。

**Abstract:** Large Language Models (LLMs) have revolutionized fields such as natural language processing and software engineering, fueling the growth of Language-Model-as-a-Service (LMaaS) platforms hosted by industry leaders like OpenAI. These platforms handle millions of queries daily, requiring efficient management to reduce serving latency and meet Service Level Objectives (SLOs) while optimizing resource utilization. However, conventional cloud service management techniques, originally designed for traditional workloads, are suboptimal for LMaaS due to its dynamic service workloads and variable request loads. To address this, we propose PreServe, a tailored LMaaS management framework centered on hierarchical prediction. PreServe incorporates a service workload predictor to estimate periodic token density at a coarse granularity and a novel request load predictor to assess the resource demand of individual LLM requests, enabling the construction of a load anticipator for each LLM instance. By integrating both long-term and short-term predictions, PreServe adjusts resource allocation in advance, mitigating the risks of instance under- or over-provisioning. Moreover, PreServe optimizes request routing by considering both current and anticipated future instance loads, ensuring balanced load distribution across instances. Evaluations on real-world LMaaS production datasets demonstrate that PreServe outperforms state-of-the-art approaches, achieving over 41.3% reduction in tail latency, an average 49.38% decrease in resource consumption, and incurring only 0.23% additional overhead.

## 19. Revisiting "Revisiting Neuron Coverage for DNN Testing: A Layer-Wise and Distribution-Aware Criterion": A Critical Review and Implications on DNN Coverage Testing

**Authors:** Jinhan Kim (Università della Svizzera italiana), Nargiz Humbatova (Università della Svizzera italiana), Gunel Jahangirova (King's College London), Shin Yoo (KAIST), Paolo Tonella (USI Lugano)

**Categories:** Software Engineering for AI

**中文总结:** 对 ICSE 2023 提出的 DNN 覆盖率准则 NLC 进行批判性复审，指出其违反单调性与测试顺序无关性等原则，并质疑实证评估有效性。通过再实验提出改进建议并讨论对 DNN 覆盖率测试研究的影响。

**Abstract:** We present a critical review of Neural Coverage (NLC), a state-of-the-art DNN coverage criterion by Yuan et al. at ICSE 2023. While NLC proposes to satisfy eight design requirements and demonstrates strong empirical performance, we question some of their theoretical and empirical assumptions. We observe that NLC deviates from core principles of coverage criteria, such as monotonicity and test suite order independence, and could more fully account for key properties of the covariance matrix. Additionally, we note threats to the validity of the empirical study, related to the ground truth ordering of test suites. Through our empirical validation, we substantiate our claims and propose improvements for future DNN coverage metrics. Finally, we conclude by discussing the implications of these insights.

## 20. Smoke and Mirrors: Jailbreaking LLM-based Code Generation via Implicit Malicious Prompts

**Authors:** Sheng Ouyang (National University of Defense Technology), Yihao Qin (National University of Defense Technology), Bo Lin (National University of Defense Technology), Liqian Chen (National University of Defense Technology), Xiaoguang Mao (National University of Defense Technology), Shangwen Wang (National University of Defense Technology)

**Categories:** Software Engineering for AI

**中文总结:** 提出 CodeJailbreaker，将恶意意图隐式编码在 commit message 等 covert channel 而非显式 instruction 中，绕过 LLM 代码生成的安全机制。在 RMCBench 上攻击效果显著优于传统显式 jailbreak。

**Abstract:** The proliferation of Large Language Models (LLMs) has revolutionized natural language processing and significantly impacted code generation tasks, enhancing software development efficiency and productivity. Notably, LLMs like GPT-4 have demonstrated remarkable proficiency in text-to-code generation tasks. However, the growing reliance on LLMs for code generation necessitates a critical examination of the security implications associated with their outputs. Existing research efforts have primarily focused on verifying functional correctness, overlooking the crucial aspect of code security. This paper introduces a jailbreaking approach, CodeJailbreaker, targeting LLM-based code generation to expose security vulnerabilities. The basic observation is that existing security mechanisms for LLMs are built through the instruction-following paradigm, where malicious intent is explicitly articulated within the instruction of the prompt. Consequently, CodeJailbreaker explores to construct a prompt whose instruction is benign and the malicious intent is implicitly encoded in a covert channel, i.e., the commit message, to bypass the safety mechanism. Experiments on the recently-released RMCBench benchmark demonstrate that CodeJailbreaker markedly surpasses the conventional jailbreaking strategy, which explicitly conveys malicious intents in the instructions, in terms of the attack effectiveness across three code generation tasks. This study challenges the traditional safety paradigms in LLM-based code generation, emphasizing the need for enhanced safety measures in safeguarding against implicit malicious cues.

## 21. SpecOps: A Fully Automated AI Agent Testing Framework in Real-World GUI Environments

**Authors:** Syed Yusuf Ahmed (Purdue University), Shiwei Feng (Purdue University), Chanwoo Bae (Purdue University), Calix Barrus (University of Texas at San Antonio), Xiangyu Zhang (Purdue University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 SpecOps，四阶段（用例生成、环境搭建、执行、验证）全自动测试真实 GUI 环境 LLM agent 的框架。在 5 个 agent 上 F1 0.89、发现 164 个真实 bug，单次测试成本低于 $0.73、耗时不到 8 分钟。

**Abstract:** Autonomous AI agents powered by large language models (LLMs) are increasingly deployed in real-world applications, where reliable and robust behavior is critical. However, existing agent evaluation frameworks either rely heavily on manual efforts, operate within simulated environments, or lack focus on testing complex, multimodal, real-world agents. We introduce SpecOps, a novel, fully automated testing framework designed to evaluate GUI based AI agents in real-world environments. SpecOps, decomposes the testing process into four specialized phases—test case generation, environment setup, test execution, and validation—each handled by a distinct LLM-based specialist agent. This structured architecture addresses key challenges including end-to-end task coherence, robust error handling, and adaptability across diverse agent platforms including CLI tools, web apps, and browser extensions. In comprehensive evaluations across five diverse real-world agents, SpecOps, outperforms baselines including general-purpose agentic systems such as AutoGPT and LLM crafted automation scripts in planning accuracy, execution success, and bug detection effectiveness. SpecOps identifies 164 true bugs on the real-world agents with an F1 score of 0.89. Costing under $0.73 and runtime of under eight minutes per test, it demonstrates its practical viability and superiority in automated, real-world agent testing.

## 22. SustainDiffusion: Optimising the Social and Environmental Sustainability of Stable Diffusion Models

**Authors:** Giordano d'Aloisio (University of L'Aquila), Tosin Fadahunsi (University College London), Jay Choy (University College London), Rebecca Moussa (University College London), Federica Sarro (University College London)

**Categories:** Software Engineering for AI

**中文总结:** 提出基于搜索的 SustainDiffusion，联合优化 Stable Diffusion 的超参数与提示结构，在保持图像质量的同时显著降低性别/族裔偏见与能耗（如 SD3 偏见降约 68%/59%，能耗降 48%）。

**Abstract:** Background: Text-to-image generation models are widely used across numerous domains. Among these models, Stable Diffusion (SD) – an open-source text-to-image generation model – has become the most popular, producing over 12 billion images annually. However, the widespread use of these models raises concerns regarding their social and environmental sustainability. Aims: To reduce the harm that SD models may have on society and the environment, we introduce SustainDiffusion, a search-based approach designed to enhance the social and environmental sustainability of SD models. Method: SustainDiffusion searches the optimal combination of hyperparameters and prompt structures that can reduce gender and ethnic bias in generated images while also lowering the energy consumption required for image generation. Importantly, SustainDiffusion maintains image quality comparable to that of the original SD model. Results: We conduct a comprehensive empirical evaluation of SustainDiffusion, testing it against six different baselines using 56 different prompts. Our results demonstrate that SustainDiffusion can reduce gender bias in SD3 by 68%, ethnic bias by 59%, and energy consumption (calculated as the sum of CPU and GPU energy) by 48%. Additionally, the outcomes produced by SustainDiffusion are consistent across multiple runs and can be generalised to various prompts. Conclusions: With SustainDiffusion, we demonstrate how enhancing the social and environmental sustainability of text-to-image generation models is possible without fine-tuning or changing the model’s architecture.

## 23. TACO: Trust Assessment of Large Language Models in Coding Assistance Tasks

**Authors:** Shihao Weng (Nanjing University), Yang Feng (Nanjing University), Jincheng Li (Nanjing University), Yining Yin (Nanjing University), Zhenlun Zhang (Nanjing University), Lyuxi Liu (University of Virginia), Jia Liu (Nanjing University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 TACO 框架，联合评估 LLM 在编码辅助任务中的代码质量与意图对齐，并发布 TACO-Judge/TACO-Eval 基准以支持可解释信任评估。

**Abstract:** Large Language Models (LLMs) have rapidly become integral to software development workflows, particularly in coding assistance tasks (CAT) such as debugging, implementation, and code optimization. However, the trustworthiness of LLM-generated responses remains a critical concern, as hallucinations (incorrect or misleading outputs) can severely hinder developer productivity and software reliability. In this paper, we introduce TACO, a comprehensive framework for trust assessment of LLMs in CAT scenarios. TACO jointly evaluates both the code quality and the alignment with user intent of LLM responses, enabling fine-grained and interpretable trust evaluation. We construct two new benchmarks: TACO-Judge, a human-annotated dataset for validating evaluation methods, and TACO-Eval, a large-scale benchmark for assessing LLM performance on real-world CAT problems. Through extensive experiments, we (1) demonstrate the accuracy and practical value of TACO via both benchmark evaluation and user study, (2) validate its fairness and reliability through self-preference analysis and interpreter consistency with real execution, and (3) compare the trustworthiness of several state-of-the-art LLMs in CAT scenarios. Our results highlight both the promise and limitations of current LLMs, and establish TACO as a reliable tool for their evaluation in software engineering contexts.

## 24. The Hidden Cost of Readability: How Code Formatting Silently Consumes Your LLM Budget

**Authors:** Dangfeng Pan, Zhensu Sun (Singapore Management University), Cenyuan Zhang (Monash University), David Lo (Singapore Management University), Xiaoning Du (Monash University)

**Categories:** Software Engineering for AI

**Awards:** Distinguished Paper Award

**中文总结:** 实证表明 LLM 在格式化与去格式化代码上性能相当，去除格式元素平均可减 24.5% 输入 token，并提供双向格式转换工具以兼顾人类可读与 LLM 效率。

**Abstract:** Source code is usually formatted with elements like indentation and newlines to improve readability for human developers. However, these visual aids do not seem to be beneficial for large language models (LLMs) in the same way since the code is processed as a linear sequence of tokens. Furthermore, these additional tokens can lead to increased computational costs and longer response times for LLMs. If such formatting elements are non-essential to LLMs, we can reduce such costs by removing them from the code. To figure out the role played by formatting elements, we conduct a comprehensive empirical study to evaluate the impact of code formatting on LLM performance and efficiency. Through large-scale experiments on Fill-in-the-Middle Code Completion tasks across four programming languages (Java, Python, C++, C#) and ten LLMs—including both commercial and open-source models—we systematically analyze token count and performance when formatting elements are removed. Key findings indicate that LLMs can maintain performance across formatted code and unformatted code, achieving an average input token reduction of 24.5% with negligible output token reductions. This makes code format removal a practical optimization strategy for improving LLM efficiency. Further exploration reveals that both prompting and fine-tuning LLMs can lead to significant reductions (up to 36.1%) in output code length without compromising correctness. To facilitate practical applications, we develop a bidirectional code transformation tool for format processing, which can be seamlessly integrated into existing LLM inference workflows, ensuring both human readability and LLM efficiency.

## 25. Toward Systematic Counterfactual Fairness Evaluation of Large Language Models: The CAFFE Framework

**Authors:** Alessandra Parziale (Gran Sasso Science Institute), Gianmario Voria (University of Salerno), Valeria Pontillo (Gran Sasso Science Institute), Gemma Catolino (University of Salerno), Andrea De Lucia (University of Salerno), Fabio Palomba (University of Salerno)

**Categories:** Software Engineering for AI

**中文总结:** 提出反事实公平性测试框架 CAFFE，形式化测试用例并自动生成输入变体，在三种 LLM 架构上比现有蜕变测试覆盖更广、检测更可靠。

**Abstract:** Nowadays, Large Language Models (LLMs) are foundational components of modern software systems. As their influence grows, concerns about fairness have become increasingly pressing. Prior work has proposed metamorphic testing to detect fairness issues, applying input transformations to uncover inconsistencies in model behavior. This paper introduces an alternative perspective for testing counterfactual fairness in LLMs, proposing a structured and intent-aware framework coined CAFFE (Counterfactual Assessment Framework for Fairness Evaluation). Inspired by traditional non-functional testing, CAFFE (1) formalizes LLM-Fairness test cases through explicitly defined components, including prompt intent, conversational context, input variants, expected fairness thresholds, and test environment configuration, (2) assists testers by automatically generating targeted test data, and (3) evaluates model responses using semantic similarity metrics. Our experiments, conducted on three different architectural families of LLM, demonstrate that CAFFE achieves broader bias coverage and more reliable detection of unfair behavior than existing metamorphic approaches.

## 26. Training on Clean Data but Getting Backdoored Models! A Poisoning Attack on Code Encoders

**Authors:** Yiran Xiao (Yangzhou University), Xiangyue Liu (Yangzhou University), Zhou Yang (University of Alberta, Alberta Machine Intelligence Institute), Lili Bo (Yangzhou University), Xiaobing Sun (Yangzhou University)

**Categories:** Software Engineering for AI

**中文总结:** 揭示预训练代码编码器可在发布阶段被投毒，即使用户在干净数据上微调仍会继承后门，三任务平均攻击成功率 91.62% 且性能几乎无损。

**Abstract:** Transformer-based code encoders like CodeBERT learn general knowledge from vast amounts of unlabeled source code. These encoders can convert input code into meaningful representations (i.e., code embeddings) and support a series of downstream tasks. Specifically, users can fine-tune a code encoder on certain datasets and obtain strong model performance on corresponding tasks. Re cent studies have exposed critical security vulnerabilities in this widely-adopted paradigm: attackers can inject backdoors into mod els by poisoning the fine-tuning datasets with carefully crafted triggers (e.g., dead code snippets), causing the model to produce attacker-specified outputs when these triggers are present. However, backdoor attacks rely on a strong and often unrealistic assumption: attackers can directly poison the fine-tuning data and developers will unknowingly use these compromised datasets. It motivates us to propose a novel method and expose a new stealthy backdoor attack scenario: attackers can directly poison and release poisoned encoders; even when users fine-tune the poisoned encoder on clean datasets, the obtained model inherits the backdoor! This method bypasses the aforementioned unrealistic assumption and is thus easier to operate. Additionally, it fundamentaly undermines existing defenses that focus on detecting user-side data poisoning as the latter does not happen at all. As a proof-of-concept, we evaluate the proposed attack on three popular pre-trained models across three software engineering tasks. Experiments show that the attack is both (1) effective: the average attack success rate can reach 91.62% and (2) stealthy: the decrease in model performance is 1.26%, unnoticeable by users. We additionally show that existing popular defenses cannot alarm the users when triggers appear in model inputs. These findings expose a critical blind spot in pre-trained code models and highlight the urgent need for automated defenses.

## 27. TypeCare: Boosting Python Type Inference Models via Context-Aware Re-Ranking and Augmentation

**Authors:** Wonseok Oh (Korea University), Hakjoo Oh (Korea University)

**Categories:** Software Engineering for AI

**Awards:** Artifact Award Winner

**中文总结:** 提出 TypeCare 后处理框架，通过上下文重排序与候选增强提升现有 Python 类型推断模型，对复杂类型 top-1 准确率最高提升 40.1%。

**Abstract:** Type annotations improve Python code quality by enabling better readability, static analysis, and developer productivity. However, manually annotating existing code is labor-intensive and error-prone. While recent learning-based models have advanced automatic type inference, they struggle with rare or complex types that are underrepresented in training data. We present TypeCare, a model-agnostic post-processing technique that refines the outputs of existing type inference models using code context, without requiring retraining or fine-tuning. TypeCare combines two key components: (1) Re-Ranking, which prioritizes semantically and syntactically relevant types, and (2) Augmentation, which generates additional contextually plausible candidates. Applied to three state-of-the-art type inference models—TypeT5, Tiger, and TypeGen—TypeCare consistently improves top-1 accuracy, achieving up to 40.1% gains on complex types that existing models often fail to predict correctly.

## 28. VADA: A Multicultural Benchmark for Value-Aware Data Generation and Alignment Evaluation in LLMs

**Authors:** Zhenlun Zhang (Nanjing University), Yang Feng (Nanjing University), Shihao Weng (Nanjing University), Yining Yin (Nanjing University), Jincheng Li (Nanjing University), Jia Liu (Nanjing University)

**Categories:** Software Engineering for AI

**中文总结:** 提出 VADA 多元文化价值对齐评测框架，覆盖中/欧/伊斯兰 25 维价值并含 11865 自动标注案例，集成评估准确率超 93.6%。

**Abstract:** As large language models (LLMs) are increasingly integrated into intelligent software systems that range from educational assistants to legal advisory tools, ensuring their alignment with diverse cultural values becomes a critical software engineering challenge. Traditional software engineering methods such as unit testing and formal verification fall short in specifying or validating complex normative expectations such as fairness, cultural sensitivity, and moral appropriateness. Addressing this gap, we introduce VADA, a value-aware development and evaluation framework for systematically testing and benchmarking LLMs under multiple cultural value systems. VADA incorporates a modular scenario-question generation pipeline that constructs culturally grounded test cases spanning 25 value dimensions across Chinese, European, and Islamic ethical frameworks. It further includes a Bayesian ensemble evaluation framework that aggregates alignment judgments from multiple diverse LLM-based evaluators, assigning dimension-specific trust weights based on their observed reliability. We also develop a lightweight supervised evaluator fine-tuned on VADA-generated data, providing a scalable and deployable alternative to multi-model ensemble evaluation. We construct a large-scale benchmark containing 11,865 automatically annotated cases, along with a human-labeled subset of 1000 instances for validation and evaluation. Empirical results demonstrate that VADA substantially outperforms existing prompting-based evaluators, achieving over 93.6 percent accuracy and high agreement with human annotations. Ablation studies confirm the complementary benefits of evaluator diversity and reliability-aware aggregation. Furthermore, VADA enables comparative audits of state-of-the-art LLMs, uncovering alignment inconsistencies across cultural dimensions. Results highlight VADA’s effectiveness as a foundation for robust value-aware evaluation and development of LLMs.

## 29. Why Attention Fails: A Taxonomy of Faults in Attention-Based Neural Networks

**Authors:** Sigma Jahan (Dalhousie University), Saurabhsingh Rajput (Dalhousie University), Tushar Sharma (Dalhousie University), Masud Rahman (Dalhousie University)

**Categories:** Software Engineering for AI

**中文总结:** 基于 555 个真实故障构建 attention 网络专属故障分类（7 类），超半数源于 attention 特有机制，并提出覆盖 33% Attention 故障的诊断启发式。

**Abstract:** Attention mechanisms are at the core of modern neural architectures, powering systems ranging from ChatGPT to autonomous vehicles and driving a major economic impact. However, high-profile failures, such as ChatGPT’s nonsensical outputs or Google’s suspension of Gemini’s image generation due to attention weight errors, highlight a critical gap: existing deep learning fault taxonomies might not adequately capture the unique failures introduced by attention mechanisms. This gap leaves practitioners without actionable diagnostic guidance. To address this gap, we present the first comprehensive empirical study of faults in attention-based neural networks (ABNNs). Our work is based on a systematic analysis of 555 real-world faults collected from 96 projects across ten frameworks, including GitHub, Hugging Face, and Stack Overflow. Through our analysis, we develop a novel taxonomy comprising seven attention-specific fault categories, not captured by existing work. Our results show that over half of the ABNN faults arise from mechanisms unique to attention architectures. We further analyze the root causes and manifestations of these faults through various symptoms. Finally, by analyzing symptom–root cause associations, we identify four evidence-based diagnostic heuristics that explain 33.0% of attention-specific faults, offering the first systematic diagnostic guidance for attention-based models.
