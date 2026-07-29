# FSE 2026 Research Track — Software Engineering for AI

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 12 papers

## 1. Beyond Language Boundaries: Uncovering Programming Language Families for Code Language Models

**Authors:** Shangbo Yun (Shanghai Jiao Tong University), Jianghong Huang (Shanghai Jiao Tong University), Xiaodong Gu (Shanghai Jiao Tong University), Beijun Shen (Shanghai Jiao Tong University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797138

**中文总结:** 基于 21 项语言学特征与 LLM 生成的跨语言对齐代码嵌入，对 19 种语言做层次聚类揭示编程语言族谱（如 C/C++/Java/Swift 成簇、Go 为中心语言）；据此提出迁移学习、语言邻近课程学习与中心中介翻译，在四项代码智能任务上显著提升多语言代码 LLM。

**Abstract:** The rapid proliferation of diverse programming languages presents both opportunities and challenges for developing multilingual code LLMs. While existing techniques often train code LLMs by simply aggregating multilingual code data, few explore the deeper relationships between programming languages and how such relationships can be utilized to optimize the training and inference of code LLMs. In this work, we investigate two fundamental questions: (1) What are the deep linguistic relationships among programming languages? and (2) How can these relationships be leveraged to improve multilingual code LLMs? We propose an embedding-based framework to uncover the latent families of programming languages. Our approach begins by defining 21 primary linguistic features of programming languages, such as variable definition, control structures, and method declarations, and then employs LLMs to generate feature-aligned code samples across multiple languages. By embedding these semantically parallel code snippets from 19 languages, we construct a similarity matrix and perform hierarchical clustering to uncover inherent language relationships. Our analysis reveals clear hierarchical structures among programming languages. Closely related languages form well-defined clusters (\emph{e.g.}, C, C++, Java, and Swift group together), while Go exhibits as a central language with the highest cross-language similarity. Building on the uncovered language families, we propose three strategies to enhance multilingual LLM training: transfer learning across linguistically related languages, linguistic proximity-guided curriculum learning, and centroid-based intermediary code translation. Experiments on four code intelligence tasks demonstrate that our methods significantly improve multilingual LLM performance. This work offers a universal perspective on programming languages and advances more effective strategies for multilingual code LLM training.

## 2. Carbon-Taxed Transformers: A Green Compression Pipeline for Overgrown Language Models

**Authors:** Ajmain Inqiad Alam (University of Saskatchewan), Palash Ranjan Roy (University of Saskatchewan), Chanchal K. Roy (University of Saskatchewan), Banani Roy (University of Saskatchewan), Kevin Schneider (University of Saskatchewan)

**Categories:** Software Engineering for AI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797075

**中文总结:** 提出 Carbon-Taxed Transformers (CTT)，借鉴碳税思想对 SE 用语言模型做多架构压缩管线；在克隆检测、摘要与生成任务上最高可获约 49× 显存降低与 81% CO₂ 减排，同时保留约 98%/89%/最高 91%（文本）与 68%（pass@1）性能。

**Abstract:** The accelerating adoption of Large Language Models (LLMs) in software engineering (SE) has brought with it a silent crisis: unsustainable computational cost. While these models demonstrate remarkable capabilities in different SE tasks, they are unmanageably large, slow to deploy, memory-intensive, and carbon-heavy. This reality threatens not only the scalability and accessibility of AI-powered SE, but also its long-term environmental sustainability. The research challenge is clear: we must go beyond accuracy and address efficiency and environmental cost as first-class design constraints. To meet this challenge, we introduce Carbon-Taxed Transformers (CTT), a systematic multi-architectural compression principled pipeline ordering inspired by economic carbon taxation principles. Drawing from the economic concept of carbon pricing, CTT operationalizes a computational carbon tax that penalizes architectural inefficiencies and rewards deployment-ready compression. We evaluate CTT across three core SE tasks: code clone detection, code summarization, and code generation, with models spanning encoder-only, encoder-decoder, and decoder-only architecture. Our results show that CTT delivers on inference: (1) up to 49$\times$ memory reduction, (2) time reduction up to 8-10$\times$ for clone detection, up to 3$\times$ for summarization, and 4–7$\times$ for generation, (3) up to 81% reduction in CO$_2$ emissions and (4) CTT retains around 98% accuracy on clone detection, around 89% on summarization, and  up to 91% (textual metrics) and 68% (pass@1) for generation. Two ablation studies show that pipeline ordering and individual component contributions are both essential, providing empirical justification for CTT’s design and effectiveness. This work establishes a viable path toward responsible AI in SE through aggressive yet performance-preserving compression.

## 3. Compiling Code LLMs into Lightweight Executables

**Authors:** Jieke Shi (Singapore Management University), Junda He (Singapore Management University), Zhou Yang (University of Alberta; CIFAR AI Chair; Alberta Machine Intelligence Institute), Chengran Yang (Singapore Management University, Singapore), Mykhailo Klymenko (CSIRO's Data61), Thong Hoang (CSIRO's Data61), Xiwei (Sherry) Xu (Data61, CSIRO), Zhenchang Xing (CSIRO's Data61), David Lo (Singapore Management University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808196

**中文总结:** 提出 Ditto，结合乘积量化启发的模型压缩与 LLVM 中将 GEMV 替换为 BLAS 的编译优化，将 Code LLM 编译为轻量可执行程序；相对原推理管线最高加速 10.5×、降内存 6.4×，pass@1 平均仅损失 0.27%。

**Abstract:** The demand for better prediction accuracy and higher execution performance in neural networks continues to grow. The emergence and success of Large Language Models (LLMs) have led to the development of many cloud-based tools for software engineering tasks such as code suggestion. While effective, cloud deployment raises concerns over privacy, latency, and reliance on connectivity. Running LLMs locally on personal devices such as laptops would address these issues by enabling offline use and reducing response time. However, local deployment is challenging: commodity devices lack high-performance accelerators like GPUs and are constrained by limited memory and compute capacity, making it difficult to execute large models efficiently.

We present Ditto, a novel method for optimizing both the model size of Code LLMs and their inference programs, particularly for statically-typed programming languages such as C. Our approach integrates two key components: (1) a model compression technique inspired by product quantization, which clusters model parameters into codebooks and quantizes them to lower bit widths while ensuring that outputs remain within a bounded error, as well as synthesizing the inference program for the quantized model; and (2) a compilation pass integrated into LLVM that automatically detects and replaces unoptimized General Matrix-Vector Multiplication (GEMV) operations—the most computationally intensive component in code models—with implementations from Basic Linear Algebra Subprograms (BLAS) libraries, which are highly optimized for runtime performance. The output of Ditto is an optimized and compiled executable for running selected Code LLMs. We evaluate Ditto on three popular Code LLMs—Code Llama, MagicCoder, and OpenCodeInterpreter, achieving up to 10.5× faster inference and 6.4× lower memory usage compared with their original inference pipeline, while maintaining accuracy close to that of the full-precision models (with an average loss of only 0.27% in pass@1). Furthermore, Ditto outperforms the state-of-the-art int8 quantization baseline, achieving up to 6.61% higher pass@1 accuracy, 2.2× speedup, and 1.6× memory usage reduction, which demonstrates the effectiveness of our approach.

## 4. DualCodeDetect: Zero-Shot LLM-Generated Code Detection via Dual-Channel Perturbation

**Authors:** Zhengdao Li, Xiuwei Shang, Zhenkan Fu, Shikai Guo, Weiming Zhang, Nenghai Yu, Kejiang Chen

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808166

**中文总结:** 提出 DualCodeDetect，通过标识符核外周扰动与语义保持结构变换双通道放大 LLM 生成码与人工码差异；在两数据集、六类代码 LLM 上平均 AUROC 达 0.8535，显著优于既有零样本检测方法。

**Abstract:** The rapid advancement of large language models (LLMs) in code generation has greatly improved software development efficiency, but it has also raised concerns about misuse, making the distinction between human-written and LLM-generated code an urgent task. However, existing detection methods for LLM-generated content, particularly perturbation-based zero-shot methods, are primarily designed for natural language scenarios and fail to transfer effectively to the task of detecting generated code. When directly applied to code, they face two major challenges: (1) the low-entropy nature of code restricts the perturbation space and weakens discriminative signals; and (2) prior perturbation methods often compromise semantic integrity or executability, leading to substantial performance degradation. To address these issues, we propose DualCodeDetect, a novel zero-shot detection framework that amplifies the differences between LLM-generated and human-written code through a dual-channel perturbation mechanism. In the semantic channel, we design an identifier perturbation strategy based on outside-nucleus sampling, which disrupts the strong consistency of LLMs in identifier selection. In the structural channel, empirical analysis reveals that LLM-generated code exhibits greater uniformity in stylistic features; leveraging this insight, we construct a rule-based library of semantics-preserving code transformations to introduce structural perturbations that further magnify statistical disparities. In experiments conducted across two datasets and six representative code LLMs, DualCodeDetect achieves an average AUROC of 0.8535 under both T=0.2 and T=1.0 temperature settings, demonstrating significant superiority over existing detection methods.

## 5. DuCodeMark: Dual-Purpose Code Dataset Watermarking via Style-Aware Watermark–Poison Design

**Authors:** Yuchen Chen, Yuan Xiao, Chunrong Fang, Zhenyu Chen, Baowen Xu

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797076

**中文总结:** 提出 DuCodeMark，经 AST 风格变换构造隐秘触发-目标对，并向返回类型样本注入可抑制投毒特征，实现源码与二进制双场景数据集水印；在 72 组设置下可稳健验证（p<0.05），移除水印后 Pass@1 下降约 28.6%。

**Abstract:** The proliferation of large language models for code (CodeLLMs) and open-source contributions has heightened concerns over unauthorized use of source code datasets. While watermarking provides a viable protection mechanism by embedding ownership signals, existing methods rely on detectable trigger–target patterns and are limited to source-level tasks, overlooking binary-level scenarios such as decompilation. In this paper, we propose DuCodeMark, a stealthy and robust dual-purpose watermarking method for code datasets that generalizes across both source-level and binary-level code tasks. DuCodeMark parses each code sample into an abstract syntax tree (AST), applies language-specific style transformations to construct stealthy trigger–target pairs, and injects repressible poisoned features into a subset of return-typed samples to enhance robustness against watermark removal or evasion. These features remain inactive during normal training but are activated upon watermark removal, degrading model performance. For verification, DuCodeMark employs a black-box method based on the independent-samples $t$-test. We conduct a comprehensive evaluation of DuCodeMark across 72 settings spanning two code tasks, two programming languages, three CodeLLMs, and six decoding temperatures. The results demonstrate that it consistently achieves strong verifiability ($p < 0.05$), high stealthiness (suspicious rate $\leq$ 0.36), robustness against both watermark and poisoning attacks (recall $\leq$ 0.57), and a substantial drop in model performance upon watermark removal (Pass@1 drops by 28.6%), underscoring its practicality and resilience.

## 6. Failure-Based Testing for Deep Reinforcement Learning Agents

**Authors:** Weibin Lin, Jiangtao Meng (Beihang University), Zheng Zheng (Beihang University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808185

**中文总结:** 提出 Prior Random Testing（PRT），利用任务难度诱导的失败先验优先探测易失败输入区域，以黑盒方式测试 DRL 智能体；在三个基准上相对模糊/搜索/生成等方法在首次失败成本与用例多样性上均位居前列。

**Abstract:** Deep Reinforcement Learning (DRL) agents have been widely adopted across diverse domains to address challenging decision-making problems, such as autonomous driving and robotic control. Given that many of these applications are safety- and security-critical, rigorous testing of DRL agents is indispensable. Existing testing methods are typically guided by reward signals to detect failures. However, for well-trained agents, whose performance approaches optimal levels in standard operating conditions, reward signals remain generally high, making current methods ineffective at uncovering critical failures.

To address the challenges, we propose a novel failure-based method that leverages task-induced failure insights to improve the efficiency of DRL agent testing. Since DRL agents are inherently designed with human-defined tasks, they provide valuable cues about task difficulty. By intuition, a DRL agent is more likely to fail when confronted with a more difficult task, so we prioritize testing the most difficult task. Building on this foundation, we propose Prior Random Testing, a black-box failure-based testing method that enables targeted prioritization while preserving the diversity of generated test cases. Guided by task-induced failure insights, PRT prioritizes failure-prone regions of the input domain, thereby facilitating efficient failure detection.

PRT is evaluated on three widely used benchmarks and compared with different state-of-the-art methods including fuzzing, search-based and generative-based methods. PRT ranks among the top performers in terms of both the cost for finding the first failure and the diversity of test cases.

## 7. Fairness Testing of Large Language Models in Role-Playing

**Authors:** Xinyue Li (Peking University), Zhenpeng Chen (Tsinghua University), Jie M. Zhang (Mistral AI and King's College London), Ying Xiao, Li Tianlin, Weisong Sun (Nanyang Technological University), Yang Liu (Nanyang Technological University), Yiling Lou (University of Illinois at Urbana-Champaign), Xuanzhe Liu (Peking University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808106

**中文总结:** 针对 LLM 角色扮演场景开展公平性测试，自动生成 550 种社会角色与 33000 条角色定向问题；对 10 个先进模型共检出 107580 条偏见响应，并公开数据集与脚本以支持后续研究。

**Abstract:** Large Language Models (LLMs) have become foundational in modern language-driven software applications, profoundly influencing daily life. A critical technique in leveraging their potential is role-playing, where LLMs simulate diverse roles to enhance their real-world utility. However, while research has highlighted the presence of social biases in LLM outputs, it remains unclear whether and to what extent these biases emerge during role-playing scenarios. In this paper, we conduct an empirical study on fairness testing of LLMs in role-playing scenarios. To enable this testing, we use LLMs to generate 550 social roles spanning a comprehensive set of 11 demographic attributes, producing 33,000 role-specific questions that target various forms of bias. These questions, covering Yes/No, multiple-choice, and open-ended formats, are designed to prompt LLMs to adopt specific roles and respond accordingly. We employ a combination of rule-based and LLM-based strategies to identify biased responses, rigorously validated through human evaluation. Using the generated questions as the test cases, we conduct extensive evaluations of 10 advanced LLMs. The evaluation reveal 107,580 biased responses across the studied LLMs, with individual models yielding between 7,579 and 16,963 biased responses, underscoring the prevalence of bias in role-playing contexts. To support future research, we have publicly released the dataset, along with all scripts and experimental results.

## 8. Neuron-Guided Interpretation of Code LLMs: Where, Why, and How?

**Authors:** Zhe Yin (Shanghai Jiao Tong University), Xiaodong Gu (Shanghai Jiao Tong University), Beijun Shen (Shanghai Jiao Tong University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797083

**中文总结:** 在神经元与层层面解析 code LLM，定位语言专属与跨语言通用表示：底层偏语法、高层偏跨语言语义；据此改进神经元引导微调、概念层克隆检测与迁移式代码摘要，均一致提升多语言代码 LLM 表现。

**Abstract:** Code language models have demonstrated strong capabilities across a wide range of code intelligence tasks. Nevertheless, the majority of existing research prioritizes performance improvements on benchmark datasets while overlooking the interpretability of model internals. They often treat code LLMs as black boxes, which results in limited transparency, reduced controllability, and uncertain reliability. In this work, we investigate the inner mechanisms of code LLMs at both neuron and layer levels, aiming to localize network regions that encode programming language-specific and language-agnostic semantic representations of code. Our study employs two state-of-the-art models, Llama-3.1-8B and Qwen2.5-Coder-32B, across five widely-used programming languages: C++, Java, Python, Go, and JavaScript. We analyze neuron activation patterns in response to multilingual code inputs and examine the contributions of different layers during output generation. Our empirical results indicate that: (1) code LLMs exhibit neurons specialized for individual programming languages as well as a universal set supporting general code generation; and (2) lower layers predominantly capture syntactic structures specific to each language, while higher layers abstract into semantic representations that generalize across languages. We further exploit these insights to enhance three downstream tasks: neuron-guided fine-tuning for code generation, clone detection using concept-layer embeddings, and transfer learning guided by concept-layer representations for code summarization. Experimental evaluations show that each strategy consistently improves the performance of multilingual code LLMs.

## 9. PuzzleMark: Implicit Jigsaw Learning for Robust Code Dataset Watermarking in Neural Code Completion Models

**Authors:** Haocheng Huang (Soochow University), Yuchen Chen (Nanjing University), Weisong Sun (Nanyang Technological University), Peizhuo Lv (Nanyang Technological University), Yuan Xiao (Nanjing University), Chunrong Fang (Nanjing University), Yang Liu (Nanyang Technological University), Xiaofang Zhang (Soochow University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797122

**中文总结:** 提出 PuzzleMark，按代码复杂度选择载体并以变量名拼接替代共现模式为代码数据集隐式水印；黑盒 t 检验验证成功率 100%、误报率 0%，对检测与攻击具有强隐蔽性与鲁棒性。

**Abstract:** Constructing and curating high-quality code datasets requires significant resources, making them valuable intellectual property. Unfortunately, these datasets currently face severe risks of unauthorized use. Although digital watermarking offers a post hoc mechanism for copyright authentication, existing methods are predominantly based on the co-occurrence pattern, which is not robust and is susceptible to watermark detection and removal attacks. In this paper, we propose PuzzleMark, a robust watermarking method for code datasets. To reduce the risk of watermark exposure, PuzzleMark introduces a carrier selection strategy that leverages code complexity to evaluate the suitability of code snippets as watermark carriers, and selects those with high suitability for watermarking. To enhance the robustness of the watermark, PuzzleMark proposes a novel concatenation pattern to replace the traditional co-occurrence pattern, and implements two watermarking strategies through variable name concatenation. PuzzleMark adaptively embeds watermarks based on the inherent characteristics of the code, making it more stealthy while maintaining design simplicity. For watermark verification, PuzzleMark employs an independent-samples $t$-test to verify suspicious models under a black-box setting. Experimental results demonstrate that PuzzleMark achieves a 100% verification success rate and a 0% false positive rate, with negligible impact on model performance. Both our human study and our evaluation using four state-of-the-art watermark detection methods show that PuzzleMark exhibits strong imperceptibility, with an average suspicious rate $\leq$ 0.24 and an average recall $\leq$ 30.41%, respectively. Furthermore, the consistent retention of verifiability under two attack scenarios further corroborates the robustness of PuzzleMark. As a practical digital watermarking method, PuzzleMark provides strong protection for the intellectual property of code datasets and offers new insights for future research.

## 10. TSGuard: Automated User-Centric Incident Diagnosis for AI Workloads in the Cloud

**Authors:** Yitao Yang (The Chinese University of Hong Kong), Yangtao Deng (The Chinese University of Hong Kong), Yifan Xiong (Microsoft Research), Baochun Li (University of Toronto), Hong Xu (The Chinese University of Hong Kong), Peng Cheng (Microsoft Research Asia)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797149

**中文总结:** 提出用户侧多 Agent 系统 TSGuard，离线挖掘值班经验构建知识库、在线结构化推理与试错诊断云上 AI 工作负载故障；在公有云生产事故上诊断准确率提升 19.8%，平均验证时间减少 63.4%。

**Abstract:** AI workloads incur frequent failures and incidents from the underlying infrastructure. The current incident management workflow follows a provider-centric paradigm, where users report incidents to the infrastructure provider who then conducts troubleshooting. Due to the large number of incidents and the manual nature of the troubleshooting process, the provider often takes several days to resolve an incident, resulting in operational delays and productivity loss.

To address these challenges, we present TSGuard, a user-centric multi-agent system that delivers immediate incident diagnosis to users who deploy the workloads. The core innovation of TSGuard is twofold: (1) constructing domain-specific knowledge bases by mining historical on-call experiences in the offline phase, and (2) mimicking human expert diagnosis via structured reasoning and iterative trial-and-error in the online phase. Evaluation using production incident records from public cloud A demonstrates that TSGuard significantly outperforms state-of-the-art baselines, improving diagnostic accuracy by 19.8%. Furthermore, TSGuard reduces the average verification time by 63.4% compared to sequential benchmark execution baseline.

## 11. Unveiling AI-Driven Web Applications: Insights into Characteristics, Functionality, and Compliance

**Authors:** Liuhuo Wan, Zicong Liu (University of Queensland), Chuan Yan (University of Queensland), Liujia Wan (Northeastern University), Naipeng Dong (The University of Queensland, Australia), Zi Huang (University of Queensland), Guangdong Bai (City University of Hong Kong)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808168

**中文总结:** 首次对五大主流 Web 应用市场的插件开展跨平台大规模研究，刻画功能与安装分布、用户关切及 AI 伦理合规；发现市场分布不均、AI 插件问题影响体验，且大量插件未遵循既有 AI 伦理原则。

**Abstract:** Collaborative platforms such as Google Workspace, Microsoft Teams, and Zoom increasingly rely on third-party applications (referred to as plugins) to extend their core functionalities, with AI-assisted plugins emerging as a key driver of productivity. Despite their popularity and rapid adoption, Little is known about the characteristics of the marketplace, the potential security and privacy risks that concern users, and the compliance of plugins with AI ethics guidelines. In this paper, we present the first large-scale, cross-platform study of plugins from five major web application marketplaces, covering domains from office productivity to software development. We systematically examine the distribution characteristics of current plugins, analyze users’ concerns, and assess their compliance with emerging AI regulations. Our findings indicate that (i) the current marketplaces exhibit an uneven distribution of functionality and installations, (ii) AI-assisted plugins face a range of emerging issues that negatively impact user experience, and (iii) a significant proportion of plugins fail to comply with established AI ethics principles. Our work highlights the need for stricter policies and security auditing to maintain plugin functionality.

## 12. Verifying Structural Robustness of Deep Neural Network

**Authors:** Hai Duong (George Mason University), Thanh Le (National Institute of Information and Communications Technology (NICT)), Lam Nguyen (CMC Applied Technology Institute (CATI)), ThanhVu Nguyen (George Mason University)

**Categories:** Software Engineering for AI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797095

**中文总结:** 提出 VeriS，将线性位置不变/可变等结构扰动重写为可与现有工具对接的局部鲁棒性子问题，以验证 DNN 的结构鲁棒性；在图像、音频与医疗共 5508 个验证问题上成功验证约 78% 的结构规范。

**Abstract:** Neural network verification has emerged as a useful technique for improving the reliability of deep learning systems. Current verification approaches primarily focus on local robustness, where perturbations are applied independently to each input element. Despite its common use, local robustness does not capture perturbations that exhibit coordinated relationships between input elements. Such perturbations arise from systematic transformations or filtering operations that preserve structural characteristics of the data. These perturbations, which we call “structural robustness”, represent a significant gap in existing verification capabilities.

This work focuses on structural robustness verification by formalizing two important classes of structured perturbations: linear position-invariant and linear position-varying. Those perturbations allow input elements to be modified in coordinated ways while preserving essential data structure. The main challenge is that structural perturbations cannot be directly expressed using standard interval-based specification formats that existing verification tools typically support.

To address this limitation, we introduce VeriS, a technique that reformulates structural robustness into standard local robustness problems by creating specialized subnetworks that encode perturbation behavior and integrates them with the original network architecture. VeriS enables verification across continuous spaces defined by structural robustness specifications while maintaining compatibility with existing verification tools. VeriS also introduces optimizations that significantly enhance verification performance such as converting complex operations into standard representations.

We implement and evaluate VeriS on benchmarks involving neural networks across three domains: image classification, audio processing, and healthcare applications. Our evaluation, which encompasses 5508 verification problems, demonstrates that VeriS successfully verifies 78% of structural robustness specifications when integrated with state-of-the-art verification tools. These results show that VeriS enables the verification of complex structural perturbations that were previously beyond the reach of existing neural network verification.
