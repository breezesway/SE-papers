# FSE 2025 Research Track — Software Engineering for AI

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 18 papers

## 1. A Causal Learning Framework for Enhancing Robustness of Source Code Models

**Authors:** Junyao Ye (Huazhong University of Science and Technology), Zhen Li (Huazhong University of Science and Technology), Xi Tang (Huazhong University of Science and Technology), Deqing Zou (Huazhong University of Science and Technology), Shouhuai Xu (University of Colorado Colorado Springs), Qiang Weizhong (Huazhong University of Science and Technology), Hai Jin (Huazhong University of Science and Technology)

**Categories:** Software Engineering for AI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729387

**中文总结:** 提出 CausalCode，用因果数据增强与正则化学习不变表示，抑制源码模型中的虚假相关；在 CodeBERT 与 GraphCodeBERT 的四项 SE 任务上，鲁棒性优于现有方法。

**Abstract:** Deep Learning (DL) models are useful for many software engineering tasks. However, these models are susceptible to adversarial attacks, partly because they learn spurious features that incur spurious correlations between these features and model predictions. In this paper, we tackle the problem with a novel causal learning framework, dubbed CausalCode, which leverages causal inference principles to mitigate spurious correlations. At a high level, CausalCode can be characterized as follows: (i) it uses causal data augmentation to generate intervention examples to disrupt spurious correlations; (ii) it leverages regularization to learn invariant representations that prefer causal features to spurious features; (iii) it can enhance the robustness of multiple DL models for source code-based software engineering tasks because it is task-agnostic and model-agnostic. To evaluate its effectiveness, we conduct experiments on two models, CodeBERT and GraphCodeBERT, with respect to four software engineering tasks. Experimental results show that CausalCode outperforms the state-of-the-art approaches in enhancing the robustness of these models.

## 2. An adaptive language-agnostic pruning method for greener language models for code

**Authors:** Mootez Saad (Dalhousie University), José Antonio Hernández López (Linköping University), Boqi Chen (McGill University), Daniel Varro (Linköping University / McGill University), Tushar Sharma (Dalhousie University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715773

**中文总结:** 提出语言无关剪枝方法 ALPINE，为 Transformer 代码模型自适应压缩输入序列；在缺陷预测与克隆检测上平均减少约 50% FLOPs、58.1% 内存，吞吐提升 28.1%，CO₂ 最多降 44.85%，同时保留最高约 98.1% 原性能。

**Abstract:** Language models of code have demonstrated remarkable performance across various software engineering and source code analysis tasks. However, their demanding computational resource requirements and consequential environmental footprint remain as significant challenges. This work introduces ALPINE, an a daptive programming l anguage-agnostic p run in g techniqu e designed to substantially reduce the computational overhead of these models. The proposed method offers a pluggable layer that can be integrated with all Transformer-based models. With ALPINE, input sequences undergo adaptive compression throughout the pipeline, reaching a size that is up to times 3 less their initial size, resulting in significantly reduced computational load. Our experiments on two software engineering tasks, defect prediction and code clone detection across three language models CodeBERT, GraphCodeBERT, and UniXCoder show that ALPINE achieves up to a 50% reduction in FLOPs, a 58.1% decrease in memory footprint, and a 28.1% improvement in throughput on average. This led to a reduction in CO 2 by up to 44.85%. Importantly, it achieves a reduction in computation resources while maintaining up to 98.1% of the original predictive performance. These findings highlight the potential of ALPINE in making language models of code more resource-efficient and accessible while preserving their performance, contributing to the overall sustainability of their adoption in software development. Also, it sheds light on redundant and noisy information in source code analysis corpora, as shown by the substantial sequence compression achieved by ALPINE.

## 3. An Empirical Study of Code Clones from Commercial AI Code Generators

**Authors:** Weibin Wu (Sun Yat-sen University), Haoxuan Hu (Sun Yat-sen University, China), Zhaoji Fan (Sun Yat-sen University), Yitong Qiao (Sun Yat-sen University, China), Yizhan Huang (The Chinese University of Hong Kong), Yichen LI (The Chinese University of Hong Kong), Zibin Zheng (Sun Yat-sen University), Michael Lyu (Chinese University of Hong Kong)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729397

**中文总结:** 对三款商业 AI 代码生成器做克隆实证研究，Type-1/Type-2 克隆率最高达 7.50%；表明存在版权侵权与脆弱代码传播风险，且生成克隆具有一定稳定性。

**Abstract:** Deep learning (DL) has revolutionized various software engineering tasks, including code generation and program repair. The emergence of AI code generators has pushed the boundaries of automatic programming to synthesize entire programs based on user-defined specifications in natural language. However, it remains a mystery if these AI code generators rely on copy-and-paste programming practices, with possible implications for copyright infringement and code cloning. In this work, we conduct an empirical study on three state-of-the-art commercial AI code generators to investigate the existence of code clone issues. Our experimental results show that the total Type-1 and Type-2 clone rates of the state-of-the-art commercial AI code generators can reach up to 7.50%, indicating marked code clone issues. Furthermore, it is observed that AI code generators risk infringing copyrights and propagating vulnerable code resulting from cloning code and show a certain degree of stability in generating code clones.

## 4. Automated Trustworthiness Oracle Generation for Machine Learning Text Classifiers

**Authors:** Lam Nguyen Tung (Monash University, Australia), Steven Cho (The University of Auckland, New Zealand), Xiaoning Du (Monash University), Neelofar Neelofar (Royal Melbourne Institure of Techonlogy (RMIT)), Valerio Terragni (University of Auckland), Stefano Ruberto (JRC European Commission), Aldeida Aleti (Monash University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729376

**中文总结:** 提出 TOKI，用解释方法提取决策词并基于词嵌入检验与预测类别的语义相关性，以自动生成文本分类可信度预言；相对仅依赖置信度准确率高 142%，并指导出比 A2T 更有效的对抗攻击。

**Abstract:** Machine learning (ML) for text classification has been widely used in various domains, such as toxicity detection, chatbot consulting, and review analysis. These applications can significantly impact ethics, economics, and human behavior, raising serious concerns about trusting ML decisions. Several studies indicate that traditional uncertainty metrics, such as model confidence, and performance metrics, like accuracy, are insufficient to build human trust in ML models. These models often learn spurious correlations during training and predict based on them during inference. When deployed in the real world, where such correlations are absent, their performance can deteriorate significantly. To avoid this, a common practice is to test whether predictions are made reasonably based on valid patterns in the data, Along with this, a challenge known as the trustworthiness oracle problem has been introduced. So far, due to the lack of automated trustworthiness oracles, the assessment requires manual validation, based on the decision process disclosed by explanation methods. However, this approach is time-consuming, error-prone, and not scalable. To address this problem, we propose TOKI, the first automated trustworthiness oracle generation method for text classifiers. TOKI automatically checks whether the words contributing the most to a prediction are semantically related to the predicted class. Specifically, we leverage ML explanation methods to extract the decision-contributing words and measure their semantic relatedness with the class based on word embeddings. As a demonstration of its practical usefulness, we also introduce a novel adversarial attack method that targets trustworthiness vulnerabilities identified by TOKI. We compare TOKI with a naive baseline based solely on model confidence. To evaluate their alignment with human judgement, experiments are conducted on human-created ground truths of approximately 6,000 predictions. Additionally, we compare the effectiveness of TOKI-guided adversarial attack method with A2T, a state-of-the-art adversarial attack method for text classification. Results show that (1) relying on prediction uncertainty metrics, such as model confidence, cannot effectively distinguish between trustworthy and untrustworthy predictions, (2) TOKI achieves 142% higher accuracy than the naive baseline, and (3) TOKI-guided adversarial attack method is more effective with fewer perturbations than A2T.

## 5. Automatically Detecting Numerical Instability in Machine Learning Applications via Soft Assertions

**Authors:** Shaila Sharmin (Iowa State University), Anwar Hossain Zahid (Iowa State University), Subhankar Bhattacharjee (Iowa State University), Chiamaka Igwilo (Iowa State University), Miryung Kim (UCLA and Amazon Web Services), Wei Le (Iowa State University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729394

**中文总结:** 提出 neural assertions：在单元测试中训练模型预测如何变换输入以触发数值不稳定，并据此引导变异；在 GRIST 与 15 个真实 ML 应用上优于 5 个 SOTA fuzzer，并发现含错误输出的数值缺陷。

**Abstract:** Machine learning (ML) applications have become an integral part of our lives. ML applications extensively use floating-point computation and involve very large/small numbers; thus, maintaining the numerical stability of such complex computations remains an important challenge. Numerical bugs can lead to system crashes, incorrect output, and wasted computing resources. In this paper, we introduce a novel idea, namely neural assertions , to encode safety/error conditions for the places where numerical instability can occur. A neural assertion is an ML model automatically trained using the dataset obtained during unit testing of unstable functions. It takes the values at the unstable functions and reports how to transform the values in order to trigger the instability. We developed a tool that uses outputs of neural assertions as signals to effectively mutate inputs to trigger numerical instability in ML applications. In the evaluation, we used the GRIST benchmark, a total of 79 programs, as well as 15 real-world ML applications from GitHub. We compared our tool with 5 state-of-the-art (SOTA) fuzzers. We found all the GRIST bugs and outperformed the baselines. We found 13 numerical bugs in real-world code, one of which had already been confirmed by the GitHub developers. While the baselines mostly found the bugs that report NaN and INF , Neural Assertion Fuzzer found numerical bugs with incorrect output. We showed one case where the Tumor Detection Model , trained on Brain MRI images, should have predicted “tumor”, but instead, it incorrectly predicted “no tumor” due to the numerical bugs. Our replication package is located at this private Figshare link .

## 6. Bridging Operator Semantic Inconsistencies: A Source-level Cross-framework Model Conversion Approach

**Authors:** Xingpei Li (National University of Defense Technology, China), Yan Lei (Chongqing University), Zhouyang Jia (National University of Defense Technology), Yuanliang Zhang (National University of Defense Technology), Haoran Liu (National University of Defense Technology), Liqian Chen (National University of Defense Technology), Wei Dong (National University of Defense Technology), Shanshan Li (National University of Defense Technology)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729361

**中文总结:** 提出 ModelX，在源码层逐层动态对齐相关代码以弥合跨框架算子语义不一致（约 47% 算子存在）；PyTorch→Paddle 等价转换 624/686 算子，52 个模型平均指标差距均低于 3.4%。

**Abstract:** Driven by the widespread use of deep learning (DL) frameworks, cross-framework model conversion supports a diverse ecosystem and facilitates efficient application development. However, interestingly, existing works commonly use intermediate representations (e.g., computation graphs or APIs) for cross-framework model conversion. Due to the lack of the ability to capture operator execution details compared to source code, it is difficult for these intermediate representations to bridge semantic inconsistencies in operators. These inconsistencies change operator behavior and potentially cause poor performance and errors in converted models. Thus, we present the first comprehensive study to analyze features and dependencies of source code related to operator semantic inconsistencies, finding that 47% of sampled operators exhibit semantic inconsistencies across DL frameworks, and the related code snippets are distributed across layers of DL frameworks without inter-layer dependencies. These findings suggest that bridging operator semantic inconsistencies layer-by-layer is feasible. Based on the findings, we propose ModelX: a source-level cross-framework model conversion approach that bridges operator semantic inconsistencies by dynamically aligning related code snippets independently within each layer, focusing on model conversion at a much finer-grained level (i.e., source code) instead of intermediate representations. The large-scale experiments on the conversion from PyTorch to Paddle show that ModelX equivalently converts 624 out of 686 sampled PyTorch operators, and yields better performance over two state-of-the-art model conversion approaches and popular large language models. Furthermore, we achieve minimal metric gaps (avg. all under 3.4%) across 52 models in the three most popular application fields (i.e., vision, text, and audio), showing that ModelX is highly robust.

## 7. Code Red! On the Harmfulness of Applying Off-the-shelf Large Language Models to Programming Tasks

**Authors:** Ali Al-Kaswan (Delft University of Technology, Netherlands), Sebastian Deatc (Delft University of Technology), Begüm Koç (Delft University of Technology), Arie van Deursen (TU Delft), Mali Izadi (Delft University of Technology)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729380

**中文总结:** 构建软件工程有害场景分类体系与提示数据集，并用自动评估器系统测量各类 LLM 生成有害内容的倾向；发现模型族与对齐策略差异显著，代码专用模型未必更安全，更大模型通常更少输出有害信息。

**Abstract:** Nowadays, developers increasingly rely on solutions powered by Large Language Models (LLM) to assist them with their coding tasks. This makes it crucial to align these tools with human values to prevent malicious misuse. In this paper, we propose a comprehensive framework for assessing the potential harmfulness of LLMs within the software engineering domain. We begin by developing a taxonomy of potentially harmful software engineering scenarios and subsequently, create a dataset of prompts based on this taxonomy. To systematically assess the responses, we design and validate an automatic evaluator that classifies the outputs of a variety of LLMs both open-source and closed-source models, as well as general-purpose and code-specific LLMs. Furthermore, we investigate the impact of models’ size, architecture family, and alignment strategies on their tendency to generate harmful content. The results show significant disparities in the alignment of various LLMs for harmlessness. We find that some models and model families, such as Openhermes, are more harmful than others and that code-specific models do not perform better than their general-purpose counterparts. Notably, some fine-tuned models perform significantly worse than their base-models due to their design choices. On the other side, we find that larger models tend to be more helpful and are less likely to respond with harmful information. These results highlight the importance of targeted alignment strategies tailored to the unique challenges of software engineering tasks and provide a foundation for future work in this critical area.

## 8. Detecting and Reducing the Factual Hallucinations of Large Language Models with Metamorphic Testing

**Authors:** Weibin Wu (Sun Yat-sen University), Yuhang Cao (Sun Yat-sen University), Ning Yi (Sun Yat-sen University), Rongyi Ou (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715784

**中文总结:** 提出 DrHall，借鉴软件蜕变测试，用蜕变关系驱动 LLM 走不同执行路径以检测问答中的事实幻觉；在自然与代码语言三类数据集上优于已有方法，并可通过多样路径采样提升纠错成功率。

**Abstract:** Question answering (QA) is a fundamental task of a large language model (LLM), which requires LLM to automatically answer human-posed questions in natural language. However, LLMs are known to distort facts and make non-factual statements (hallucination) when dealing with QA tasks, which may affect the deployment of LLMs in real-life situations. In this work, we present DrHall, a method for the detection of factual errors in black-box large language models inspired by metamorphosis testing in software testing. We believe that the model’s hallucination answer is unstable. It is easier to produce different answers to the hallucination by using metamorphic relation (MR) to make the model take different execution paths for re-execution. We empirically evaluate DrHall on three datasets covering natural and code language data, finding that it outperforms existing methods and baselines, often by a large gap. In addition, by transforming DrHall using diverse path sampling, we obtain error correction methods with higher success rates. Our results demonstrate the potential of using MR to mitigate LLM hallucination.

## 9. Element-Based Automated DNN Repair with Fine-Tuned Masked Language Model

**Authors:** Xu Wang (Beihang University; Zhongguancun Laboratory; Ministry of Education), Mingming Zhang (Beihang University), Xiangxin Meng (Beihang University), Jian Zhang (Nanyang Technological University), Yang Liu (Nanyang Technological University), Chunming Hu (Beihang University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715716

**中文总结:** 提出 MLM4DNN，用微调 Masked Language Model 预测 DNN 源码中九类关键元素的正确修复。在含 51 个缺陷模型的 Benchmark_APR4DNN 上优于动态与零样本基线，且将该方法迁移到多种 LLM 后修复效果一致提升。

**Abstract:** Deep Neural Networks (DNNs) are prevalent across a wide range of applications. Despite their success, the complexity and opaque nature of DNNs pose significant challenges in debugging and repairing DNN models, limiting their reliability and broader adoption. In this paper, we propose MLM4DNN, an element-based automated DNN repair method. Unlike previous techniques that focus on post-training adjustments or rely heavily on predefined bug patterns, MLM4DNN repairs DNNs by leveraging a fine-tuned Masked Language Model (MLM) to predict correct fixes for nine predefined key elements in DNNs. We construct a large-scale dataset by masking nine key elements from the correct DNN source code and then force the MLM to restore the correct elements to learn the deep semantics that ensure the normal functionalities of DNNs. Afterwards, a light-weight static analysis tool is designed to filter out low-quality patches to enhance the repair efficiency. We introduce a patch validation method specifically for DNN repair tasks, which consists of three evaluation metrics from different aspects to model the effectiveness of generated patches. We construct a benchmark, $Benchmark_{APR4DNN}$, including 51 buggy DNN models and an evaluation tool that outputs the three metrics. We evaluate MLM4DNN against six baselines on $Benchmark_{APR4DNN}$, and results show that MLM4DNN outperforms all state-of-the-art baselines, including two dynamic-based and four zero-shot learning-based methods. After applying the fine-tuned MLM design to several prevalent Large Language Models (LLMs), we consistently observe improved performance in DNN repair tasks compared to the original LLMs, which demonstrates the effectiveness of the method proposed in this paper.

## 10. Eliminating Backdoors in Neural Code Models for Secure Code Understanding

**Authors:** Weisong Sun (Nanjing University), Yuchen Chen (Nanjing University), Chunrong Fang (Nanjing University), Yebo Feng (Nanyang Technological University), Yuan Xiao (Nanjing University), An Guo (Nanjing University), Quanjun Zhang (School of Computer Science and Engineering, Nanjing University of Science and Technology), Zhenyu Chen (Nanjing University), Baowen Xu (Nanjing University), Yang Liu (Nanyang Technological University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715782

**中文总结:** 提出 EliBadCode，通过触发词筛选、样本级位置识别、Greedy Coordinate Gradient 反演与 unlearning 清除神经代码模型中的后门。在三类安全关键代码理解任务上可将先进攻击的平均 ASR 从 99.76% 降至 2.64%，同时几乎不损伤正常功能。

**Abstract:** Neural code models (NCMs) have been widely used for addressing various code understanding tasks, such as defect detection and clone detection. However, numerous recent studies reveal that such models are vulnerable to backdoor attacks. Backdoored NCMs function normally on normal/clean code snippets, but exhibit adversary-expected behavior on poisoned code snippets injected with the adversary-crafted trigger. It poses a significant security threat. For example, a backdoored defect detection model may misclassify user-submitted defective code as non-defective. If this insecure code is then integrated into critical systems, like autonomous driving systems, it could jeopardize life safety. However, there is an urgent need for effective techniques to detect and eliminate backdoors stealthily implanted in NCMs. To address this issue, in this paper, we innovatively propose a backdoor elimination technique for secure code understanding, called EliBadCode. EliBadCode eliminates backdoors in NCMs by inverting/reverse-engineering and unlearning attacker-crafted backdoor triggers. Specifically, EliBadCode first filters the model vocabulary for trigger tokens based on the naming conventions of specific programming languages to reduce the trigger search space, thereby enhancing the efficiency of the trigger inversion. Then, EliBadCode introduces a sample-specific trigger position identification method, which can reduce the interference of non-backdoor ( adversarial ) perturbations for subsequent trigger inversion, thereby producing effective inverted backdoor triggers efficiently. Backdoor triggers can be viewed as backdoor ( adversarial ) perturbations . Subsequently, EliBadCode employs a Greedy Coordinate Gradient algorithm to optimize the inverted trigger and designs a trigger anchoring method to purify the inverted trigger. Finally, EliBadCode eliminates backdoors through model unlearning. We evaluate the effectiveness of EliBadCode in eliminating backdoors implanted in multiple NCMs used for three safety-critical code understanding tasks. The results demonstrate that EliBadCode can effectively eliminate backdoors while having minimal adverse effects on the normal functionality of the model. For instance, on defect detection tasks, EliBadCode substantially decreases the average Attack Success Rate (ASR) of the advanced backdoor attack from 99.76% to 2.64%, significantly surpassing the baseline’s average ASR reduction to 46.38%. The clean model produced by EliBadCode exhibits an average decrease in defect prediction accuracy of only 0.01% (the same as the baseline).

## 11. Hallucination Detection in Large Language Models with Metamorphic Relations

**Authors:** Borui Yang (Beijing University of Posts ad Telecommunications), Md Afif Al Mamun (University of Calgary), Jie M. Zhang (King's College London), Gias Uddin (York University, Canada)

**Categories:** Software Engineering for AI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715735

**中文总结:** 提出无需外部资源的幻觉检测方法 MetaQA，利用蜕变关系与提示变异检测 LLM 回答是否自洽。在开源与闭源 LLM 上均优于 SelfCheckGPT，F1 提升幅度可达 0.154–0.368。

**Abstract:** Large Language Models (LLMs) are prone to hallucinations, e.g., factually incorrect information, in their responses. These hallucinations present challenges for LLM-based applications that demand high factual accuracy. Existing hallucination detection methods primarily depend on external resources, which can suffer from issues such as low availability, incomplete coverage, privacy concerns, high latency, low reliability, and poor scalability. There are also methods depending on output probabilities, which are often inaccessible for closed-source LLMs like GPT models. This paper presents MetaQA, a self-contained hallucination detection approach that leverages metamorphic testing and prompt mutation. Unlike existing methods, MetaQA operates without any external resources and is compatible with both open-source and closed-source LLMs. MetaQA is based on the hypothesis that if an LLM’s response is a hallucination, the designed metamorphic relations will be violated. We compare MetaQA with the state-of-the-art zero-resource hallucination detection method, SelfCheckGPT, across multiple datasets, and on two open-source and two closed-source LLMs. Our results reveal that MetaQA outperforms SelfCheckGPT in terms of precision, recall, and f1 score. For the four LLMs we study, MetaQA outperforms SelfCheckGPT with a superiority margin ranging from 0.041 - 0.113 (for precision), 0.143 - 0.430 (for recall), and 0.154 - 0.368 (for F1-score). For instance, with Mistral-7B, MetaQA achieves an average F1-score of 0.435, compared to SelfCheckGPT’s F1-score of 0.205, representing an improvement rate of 112.2%. MetaQA also demonstrates superiority across all different categories of questions.

## 12. Has My Code Been Stolen for Model Training? A Naturalness Based Approach to Code Contamination Detection

**Authors:** Haris Ali Khan (Beijing Institute of Technology), Yanjie Jiang (Peking University), Qasim Umer (Information and Computer Science Department, King Fahd University of Petroleum & Minerals (KFUPM), Dhahran 31261, Saudi Arabia), Yuxia Zhang (Beijing Institute of Technology), Waseem Akram (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715765

**中文总结:** 提出 Natural-DaCoDe，结合代码自然性与模型表现，检测源码是否被用于训练代码补全等模型，以缓解难例污染/易例干净样本的误判。相较现有方法平均准确率提升 61.78%，并在方法名建议任务上仍优。

**Abstract:** It is often valuable to know whether a given piece of source code has or hasn’t been used to train a given deep learning model. On one side, it helps avoid data contamination problems that may exaggerate the performance of evaluated models. Conversely, it facilitates copyright protection by identifying private or protected code leveraged for model training without permission. To this end, automated approaches have been proposed for the detection, known as {data contamination detection}. Such approaches often heavily rely on the confidence of the involved models, assuming that the models should be more confident in handling contaminated data than cleaned data. However, such approaches do not consider the nature of the given data item, i.e., how difficult it is to predict the given item. Consequently, difficult-to-predict contaminated data and easy-to-predict cleaned data are often misclassified. As an initial attempt to solve this problem, this paper presents a naturalness-based approach, called Natural-DaCoDe , for code-completion models to distinguish contaminated source code from cleaned ones. Natural-DaCoDe leverages code naturalness to quantitatively measure the difficulty of a given source code for code-completion models. It then trains a classifier to distinguish contaminated source code according to both code naturalness and the performance of the code-completion models on the given source code. We evaluate Natural-DaCoDe with two pre-trained large language models (e.g., ChatGPT and Claude ) and two code-completion models that we trained from scratch for detecting contamination data. Our evaluation results suggest that Natural-DaCoDe substantially outperformed the state-of-the-art approaches in detecting contaminated data, improving the average accuracy by 61.78%. We also evaluate Natural-DaCoDe with method name suggestion task, and it remains more accurate than the state-of-the-art approaches, improving the accuracy by 54.39%. It may suggest that Natural-DaCoDe could be applied to various source code related tasks besides code complete.

## 13. IRepair: An Intent-Aware Approach to Repair Data-Driven Errors in Large Language Models

**Authors:** Sayem Mohammad Imtiaz (Iowa State University), Astha Singh (Dept. of Computer Science, Iowa State University), Fraol Batole (Tulane University), Hridesh Rajan (Tulane University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715775

**中文总结:** 提出 IRepair，借鉴程序切片思想对 LLM 最敏感层做动态切片，从而有意图地修复数据驱动错误（如毒性）。在 GPT2/GPT-Neo 上毒性缓解修复效果较 DPO 提升 43.6%，对通用性能干扰减少 46%。

**Abstract:** Not a day goes by without hearing about the impressive feats of large language models (LLMs), and equally, not a day passes without hearing about their challenges. LLMs are notoriously vulnerable to biases in their dataset, leading to issues such as toxicity, harmful responses, and factual inaccuracies. While domain-adaptive training has been employed to mitigate these issues, these techniques often address all model parameters indiscriminately during the repair process, resulting in poor repair quality and reduced model versatility. In this paper, drawing inspiration from fault localization via program slicing, we introduce a novel dynamic slicing-based intent-aware LLM repair strategy, IRepair. This approach selectively targets the most error-prone sections of the model for repair. Specifically, we propose dynamically slicing the model’s most sensitive layers that require immediate attention, concentrating repair efforts on those areas. This method enables more effective repairs with potentially less impact on the model’s overall versatility by altering a smaller portion of the model. Furthermore, dynamic selection allows for a more nuanced and precise model repair compared to a fixed selection strategy. We evaluated our technique on three models from the GPT2 and GPT-Neo families, with parameters ranging from 800M to 1.6B, in a toxicity mitigation setup. Our results show that IRepair repairs errors 43.6% more effectively while causing 46% less disruption to general performance compared to the closest baseline, direct preference optimization. Our empirical analysis also reveals that errors are more concentrated in a smaller section of the model, with the top 20% of layers exhibiting 773% more error density than the remaining 80%. This highlights the need for selective repair. Additionally, we demonstrate that a dynamic selection approach is essential for addressing errors dispersed throughout the model, ensuring a robust and efficient repair.

## 14. Medusa: A Framework for Collaborative Development of Foundation Models with Automated Parameter Ownership Assignment

**Authors:** Dezhi Ran (Peking University), Yuan Cao (Peking University), Yuzhe Guo (Beijing Jiaotong University), Yuetong Li (The University of Chicago), Mengzhou Wu (Peking University), Simin Chen (University of Texas at Dallas), Wei Yang (UT Dallas), Tao Xie (Peking University)

**Categories:** Software Engineering for AI

**Artifact badges:** Artifact-Available, Artifact-Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729385

**中文总结:** 提出 Medusa，以类 Git 分支管理协同微调，并通过参数所有权分配生成合并感知 mask 引导 masked fine-tuning，减少重叠参数冲突。在多个模型与数据集上，合并后绝对性能较 SOTA 事后合并方法平均提升 3.19%。

**Abstract:** Foundation models (FMs) become the backbone of intelligent systems. Collaborative development of FMs enables multiple teams to fine-tune different aspects of an FM simultaneously. However, conflicts in model updates across teams, particularly when modifying overlapping parameters, pose significant challenges to maintaining model performance. In this paper, we propose \toolname{}, a novel framework designed to support collaborative FM development by managing model branches and introducing a structured system of parameter ownership. Medusa tracks fine-tuning efforts as separate branches, similar to Git, allowing developers to work on different tasks without destabilizing the base model. Instead of passively merging parameters from already fine-tuned models, \toolname{} proactively controls the merging through our parameter ownership assignment algorithm to generate merging-aware masks to guide the fine-tuning process, ensuring that only specific branches can modify designated parameters. \toolname{} approximates the optimal assignment even as model complexity increases, ensuring scalability in large, fine-tuned models. We conduct extensive evaluations on five datasets and three large models with state-of-the-art post-training model merging approaches to investigate the efficacy of \toolname{}. Evaluation results show that \toolname{} substantially and generally improves the effectiveness of collaborative model development, across different models, fine-tuning methods, and datasets. Specifically, with automated parameter ownership assignment and masked fine-tuning, \toolname{} outperforms state-of-the-art post-training model merging approaches by improving 3.19% absolute model performance after merging. Ablation studies further demonstrate the efficacy of algorithms in \toolname{}.

## 15. NLP Libraries, Energy Consumption and Runtime - An Empirical Study

**Authors:** Rajrupa Chattaraj (Indian Institute of Technology Tirupati, India), Sridhar Chimalakonda (Indian Institute of Technology Tirupati)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729396

**中文总结:** 本文实证比较 NLTK、spaCy、Gensim 在六类 NLP 预处理任务上的能耗与运行时，最多约 93% 的库–任务组合存在显著差异。Gensim 在 tokenization/stemming 更节能，spaCy 在 POS/NER 更优，说明预处理阶段仍有较大绿色优化空间。

**Abstract:** In the realm of natural language processing (NLP), the rising computational demands of modern models bring energy efficiency to the forefront of sustainable computing. Pre-processing tasks, such as tokenization, stemming, and POS tagging, are critical steps in transforming raw text into structured formats suitable for machine learning models. However, despite their widespread use in numerous NLP pipelines, little attention has been given to their energy consumption. Motivation: The increasing adoption of resource-intensive NLP models like LLMs and deep learning frameworks emphasizes the importance of optimizing every phase of the NLP pipeline, including pre-processing, which is frequently overlooked in energy studies. Analyzing pre-processing energy consumption is crucial for achieving a more sustainable and eco-friendly NLP ecosystem. Objective: This empirical study aims to evaluate and compare the energy consumption and runtime performance of three popular NLP libraries— NLTK , spaCy , and Gensim —across six common pre-processing tasks. Methodology: We conducted a comprehensive comparison using three distinct datasets and six pre-processing tasks. Energy consumption was measured using the Intel-RAPL and NVIDIA-SMI interfaces, while runtime performance was recorded across all library-task combinations. Results: The results reveal substantial discrepancies in energy consumption across the three libraries, with up to 93% of cases exhibiting significant variations. Gensim showed superior efficiency in tokenization and stemming, while spaCy excelled in tasks like POS tagging and Named Entity Recognition (NER). These findings underscore the potential for optimizing NLP pre-processing tasks for energy efficiency. Conclusion: Our study highlights the untapped potential for improving energy efficiency in NLP pipelines. These insights emphasize the need for more focused research into energy-efficient NLP techniques, especially in the pre-processing phase, to support the development of greener, more sustainable computational models.

## 16. RegTrieve: Reducing System-Level Regression Errors for Machine Learning Systems via Retrieval-Enhanced Ensemble

**Authors:** Junming Cao, Xuwen Xiang, Mingfei Cheng, Bihuan Chen, Xinyan Wang, You Lu, Chaofeng Sha, Xiaofei Xie, Xin Peng

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729358

**中文总结:** RegTrieve 用检索增强集成同时缓解单模型与多模型系统级更新引入的回归错误。在多种模型更新场景中显著降低系统级回归，几乎不影响系统准确率，平均优于所有基线约 20.43%。

**Abstract:** Multiple machine learning (ML) models are often incorporated into real-world ML systems. However, updating an individual model in these ML systems frequently results in regression errors, where the new model performs worse than the old model for some inputs. While model-level regression errors have been widely studied, little is known about how regression errors propagate at system level. To address this gap, we propose RegTrieve, a novel retrieval-enhanced ensemble approach to reduce regression errors at both model and system level. Extensive experiments across various model update scenarios show that RegTrieve significantly reduces system-level regression errors with almost no impact on system accuracy, outperforming all baselines by 20.43% on average.

## 17. Smaller but Better: Self-Paced Knowledge Distillation for Lightweight yet Effective LCMs

**Authors:** Yujia Chen (Harbin Institute of Technology, Shenzhen), Yang Ye (Huawei Cloud Computing Technologies Co., Ltd.), Zhongqi Li (Huawei Cloud Computing Technologies Co., Ltd.), Yuchi Ma (Huawei Cloud Computing Technologies), Cuiyun Gao (Harbin Institute of Technology, Shenzhen)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729405

**中文总结:** 提出 SODA，通过正确/错误知识传递、多视角反馈与自适应知识更新的自步知识蒸馏，将大型代码模型能力迁移到轻量学生模型。学生模型平均 Pass@1 提升 65.96%，所构建的 SodaCoder（<7B）在七种语言上平均超过 ChatGPT。

**Abstract:** Large code models (LCMs) have remarkably advanced the field of code generation. Despite their impressive capabilities, they still face practical deployment issues, such as high inference costs, limited accessibility of proprietary LCMs, and adaptability issues of ultra-large LCMs. These issues highlight the critical need for more accessible, lightweight yet effective LCMs. Knowledge distillation (KD) offers a promising solution, which transfers the programming capabilities of larger, advanced LCMs (Teacher) to smaller, less powerful LCMs (Student). However, existing KD methods often lack consideration of fault knowledge and rely on static seed knowledge, which limits their effectiveness. In this paper, we propose a novel Self-Paced knOwledge DistillAtion framework, named SODA, aims at developing lightweight yet Effective student LCMs via continually transferring the programming capabilities from advanced teacher LCMs. SODA consists of three stages in one cycle: (1) Correct-and-Fault Knowledge Delivery stage aims at improving the student model’s capability to recognize errors while ensuring its basic programming skill during the knowledge transferring, which involves correctness-aware supervised learning and fault-aware contrastive learning methods. (2) Multi-view Feedback stage aims at measuring the quality of results generated by the student model from two views, including model-based and static tool-based measurement; (3) Feedback-based Knowledge Update stage aims at updating the student model adaptively by generating new questions at different difficulty levels, in which the difficulty levels are categorized based on the feedback in the last stage. By performing the training cycle iteratively, the student model is continuously refined through learning more advanced programming skills from the teacher model. We compare SODA with four state-of-the-art KD approaches in the code generation task across seven programming languages. Experimental results show that SODA improves the student model by 65.96% in terms of average Pass@1, outperforming the best baseline PERsD by 29.85%. Based on the proposed SODA framework, we develop SodaCoder, a series of lightweight yet effective LCMs with less than 7B parameters, which outperform 15 LCMs with less than or equal to 16B parameters. Notably, SodaCoder-DS 6.7B, built on DeepseekCoder-6.7B, even surpasses the prominent ChatGPT on average Pass@1 across seven programming languages (66.4 vs. 61.3).

## 18. Software Fairness Dilemma: Is Bias Mitigation a Zero-Sum Game?

**Authors:** Zhenpeng Chen, Xinyue Li, Jie M. Zhang, Weisong Sun, Ying Xiao, Li Tianlin, Yiling Lou, Yang Liu

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729350

**中文总结:** 系统评估表格数据上 8 种偏见缓解方法，发现公平性改进往往呈零和：弱势群体收益伴随特权群体收益下降。仅对弱势群体施加先进缓解可提升其收益且不明显损害特权群体与整体性能，为非零和公平路径提供证据。

**Abstract:** Fairness is a critical requirement for Machine Learning (ML) software, driving the development of numerous bias mitigation methods. Previous research has identified a leveling-down effect in bias mitigation for computer vision and natural language processing tasks, where fairness is achieved by lowering performance for all groups without benefiting the unprivileged group. However, it remains unclear whether this effect applies to bias mitigation for tabular data tasks, a key area in fairness research with significant real-world applications. This study evaluates eight bias mitigation methods for tabular data, including both widely used and cutting-edge approaches, across 44 tasks using five real-world datasets and four common ML models. Contrary to earlier findings, our results show that these methods operate in a zero-sum fashion, where improvements for unprivileged groups are related to reduced benefits for traditionally privileged groups. However, previous research indicates that the perception of a zero-sum trade-off might complicate the broader adoption of fairness policies. To explore alternatives, we investigate an approach that applies the state-of-the-art bias mitigation method solely to unprivileged groups, showing potential to enhance benefits of unprivileged groups without negatively affecting privileged groups or overall ML performance. Our study highlights potential pathways for achieving fairness improvements without zero-sum trade-offs, which could help advance the adoption of bias mitigation methods.
