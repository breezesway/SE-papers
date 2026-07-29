# FSE 2026 Research Track — Systems, Mobile, and UI

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 10 papers

## 1. AccessDroid: Detecting Screen Reader Accessibility Issues in Android Applications via Semantics Trees

**Authors:** Hang Zhou (Nanjing University of Science and Technology), Wei Song (Nanjing University of Science and Technology)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797108

**中文总结:** 提出 AccessDroid，将 Android 屏幕阅读器无障碍问题归为语义分离、语义降级与语义缺失三类，基于语义树轻量检测歧义与内容缺失并生成诊断报告；在 50 款应用 361 屏上检出率超 95%、平均每页 15ms，精度较 LLM 方法提升 97.5%，召回高于 Accessibility Scanner。

**Abstract:** Screen readers are essential for visually impaired users to access mobile apps, yet inadequate developer support often leads to ambiguous or missing content. While prior work has primarily focused on missing content, ambiguity remains underexplored. This paper categorizes screen reader accessibility issues into three types: semantics separation, semantics downshift, and semantics missing. We propose \textsf{AccessDroid}, a lightweight approach that automatically detects both ambiguity and missing content issues in Android apps and generates diagnostic reports. Evaluated on 361 screens from 50 real-world Android apps, \textsf{AccessDroid} detects over 95% of screen reader accessibility issues with an average time of 15ms per page. \textsf{AccessDroid} improves precision by 97.5% over the \textsf{LLM} approach while incurring significantly lower time overhead. It also achieves 2.41% higher recall than the industrial-grade \textsf{Accessibility Scanner}, with comparable detection efficiency.

## 2. Behind Defective Mobile AR Apps: Studying Reviews and Bugs of Android AR Software with Comparison to Prior Bug Studies

**Authors:** Tahmid Rafi (University of Texas at San Antonio), Xueling Zhang (Rochester Institute of Technology), Jianwei Niu (University of Texas at San Antonio), Xiaoyin Wang (University of Texas at San Antonio)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797111

**中文总结:** 收集 Google Play 上 5,440 条用户评论与基于 Google ARCore 的开源 AR 应用 2,846 个 issue，分层归类并识别受影响功能；通过提交级 AST 分析评估修复复杂度与 API 变化，并对比用户报告症状与开发者跟踪症状的一致性。

**Abstract:** As Augmented Reality (AR) applications grow in popularity, understanding and addressing AR software bugs becomes crucial. AR applications, due to their interaction with the physical world, present unique challenges that differ from traditional software. In this study we collected 5, 440 user reviews from the Google Play Store and 2, 846 issues from open-source AR applications using Google ARCore. We categorized these into structured hierarchical categories and identified the features affected by each issue. To assess the complexity of bug fixes, we conducted a commit-level analysis, exploring API changes by parsing the source code and generating Abstract Syntax Trees (ASTs). Additionally, we compared the symptoms reported by users with those tracked by developers to understand their alignment

## 3. EfficientUICoder: A Bidirectional Token Compression Framework for Efficient MLLM-based UI Code Generation

**Authors:** Jingyu Xiao (The Chinese University of Hong Kong), Zhongyi Zhang (Huazhong University of Science and Technology, China), Yuxuan Wan (The Chinese University of Hong Kong), Yintong Huo (Singapore Management University, Singapore), Yang Liu (Nanyang Technological University), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808114

**中文总结:** 提出 EfficientUICoder，通过元素布局感知压缩、区域注意力精炼与自适应重复抑制对图像与代码双向压缩，面向 MLLM 的 UI2Code；在 34B 级模型上可达 55%–60% 压缩率，并将计算与推理时间分别最高降低约 44.9% 与 48.8%。

**Abstract:** Multimodal Large Language Models (MLLMs) have demonstrated exceptional performance in UI2Code tasks (i.e., generating code from UI mockups), significantly enhancing website development efficiency. However, UI2Code tasks incur substantially higher computational overhead compared to traditional code generation tasks. This overhead is primarily driven by the large number of input image tokens required to represent complex visual designs and the extensive volume of output code tokens needed to describe complete webpage structures. In this paper, we conduct a comprehensive preliminary study on popular MLLMs for UI2Code tasks, identifying significant redundancies in both image and code tokens. We observe that these redundancies not only exacerbate computational complexity but also hinder the model’s ability to focus on key UI elements, leading to excessively lengthy and often invalid HTML files.

To address these challenges, we propose EfficientUICoder, a bidirectional compression framework designed for efficient UI code generation. First, we introduce an Element and Layout-aware Token Compression method, which preserves essential UI element and layout information by detecting element regions and constructing a UI element tree for efficient representation. Second, we design a Region-aware Token Refinement strategy that refines selected tokens by leveraging attention scores to evaluate semantic importance, discarding lowattention tokens from selected region while integrating high-attention tokens from unselected regions. Third, we develop an Adaptive Duplicate Token Suppression mechanism, which dynamically modulates token probabilities during decoding by tracking HTML/CSS code structure frequencies and applying exponential penalty strategies to minimize repetitive generation. Extensive experiments demonstrate that EfficientUICoder achieves a 55%-60% compression ratio without compromising the quality of the generated webpages, effectively reducing output code redundancy. In terms of efficiency, EfficientUICoder achieves superior improvements, reducing computational cost by up to 44.9%, generated tokens by up to 41.4%, prefill time by up to 46.6%, and inference time by up to 48.8% on 34B-level MLLMs.

## 4. Evaluating Risk and Confidence in Performance Bounds of Configuration Sampling Strategies

**Authors:** Kallistos Weis (Saarland University), Martina Maggio (Saarland University, Germany / Lund University, Sweden), Norbert Siegmund (Leipzig University), Sven Apel (Saarland University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808147

**中文总结:** 提出基于后验风险与后验置信度的概率框架，量化配置采样策略识别最优/最差配置的保证强度；在七个可配置系统上比较五种策略，发现统计递归搜索在相同预算下具有更紧的最优情形保证。

**Abstract:** Modern software usually exposes a large number of configuration options to the user, which gives rise to enormous configuration spaces in practice. Appropriate choices for these options dramatically influence the performance of the software (throughput, memory consumption, execution time, etc.). However, due to the sheer size of the configuration space, systematically identifying the best or worst-performing configurations is computationally infeasible through exhaustive exploration. Instead, practitioners rely on budgeted sampling strategies, such as uniform random sampling or statistical recursive search, to explore the configuration space under fixed measurement budgets in an attempt to find the best or worst configuration. A fundamental limitation of existing sampling strategies is the lack of quantifiable guarantees that the selected configuration truly reflects best-case (or worst-case) performance. In this paper, we define the basic concepts of \emph{posterior risk} and \emph{posterior confidence} and present a probabilistic framework to evaluate how well sampling strategies identify the best- or worst-performing configuration of a software system. We evaluate our framework by comparing five representative sampling strategies on seven real-world configurable software systems. Using our framework, we find that statistical recursive search yields consistently tighter best-case guarantees—higher posterior confidence and lower posterior risk—than the alternatives at the same budget. Our results demonstrate the potential of our framework as a principled basis for reporting, comparing, and refining sampling strategies, and as a tool for practitioners to select strategies and budgets with quantified guarantees across systems and sample sizes. Extended ablations—including additional sampling strategies and per-system breakdowns—are available in the supplementary material.

## 5. GUIMigrator: Semantics-Preserving Transpilation from Android XML to Compose and SwiftUI

**Authors:** Yi Gao (Zhejiang University), Xing Hu (Zhejiang University), Xiaohu Yang (Zhejiang University), Xin Xia (Zhejiang University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808215

**中文总结:** 提出 GUIMigrator，经 Semantic UI Transpiler 将 Android XML 布局语义保持地转译为 Jetpack Compose 与 SwiftUI；在 31 个应用上视觉相似度分别约 82%/78%，相对 GPT-4 结构保真更好，并减少超 90% 手工迁移工作量。

**Abstract:** Constructing user interfaces (UIs) is one of the most resource-intensive tasks in mobile development, often consuming more than half of overall effort. Although declarative frameworks such as Jetpack Compose (Android) and SwiftUI (iOS) have become mainstream, the majority of existing Android apps still rely on legacy XML-based layouts. Migrating these UIs to declarative paradigms is essential for maintainability and cross-platform reuse, but manual migration is costly, error-prone, and difficult to scale. We present GUIMigrator, a semantics-preserving framework that automates the migration of Android XML-based UIs to Jetpack Compose and SwiftUI. We design the Semantic UI Transpiler, which abstracts layout structures and resource semantics from legacy XML and systematically re-expresses them using the component abstractions and idioms of modern declarative frameworks. This design ensures that migrated UIs preserve both visual fidelity and functional equivalence, while generating idiomatic, compilable code that maintains cross-platform consistency with minimal manual intervention. By separating semantic interpretation from platform-specific realization, GUIMigrator provides a deterministic yet extensible basis for cross-platform modernization, avoiding the unpredictability of purely generative approaches. We evaluate GUIMigrator on 31 open-source applications across ten domains. Results show that GUIMigrator achieves high migration completeness and visual similarity (Compose average 82%, SwiftUI 78%), outperforms a GPT-4 baseline in structural fidelity, and reduces manual development effort by over 90%. These findings demonstrate that GUIMigrator provides an effective and practical solution for reusing Android UIs across modern declarative frameworks, advancing automated cross-platform UI development.

## 6. Look Before You Leap: Context-Sensitive GUI Grounding for Boosting Automated Extended Reality (XR) Testing

**Authors:** Shuqing Li (The Chinese University of Hong Kong), Binchang Li (Harbin Institute of Technology), Yepang Liu (Southern University of Science and Technology), Cuiyun Gao (Harbin Institute of Technology, Shenzhen), Jianping Zhang (The Chinese University of Hong Kong), Shing-Chi Cheung (Hong Kong University of Science and Technology), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808134

**中文总结:** 提出 Orienter，首个面向 XR 的零样本上下文敏感可交互 GUI 元素检测框架，先理解场景语义再经反馈反思完成检测与可交互性分类；在新建 100 款 Steam 应用基准上 F1 大幅优于 GPT-4o 等，引导测试覆盖更多 IGE 且有效交互显著增加。

**Abstract:** In recent years, Extended Reality (XR) has emerged as a transformative technology, offering users immersive and interactive experiences across diversified virtual or virtual-real environments. Users can interact with XR applications (apps) through interactable GUI elements (IGEs) on the stereoscopic three-dimensional (3D) graphical user interface (GUI). IGE constitutes the fundamental element of XR GUI, embodying rich semantic information. The accurate recognition and precise understanding of these IGEs is instrumental, serving as the foundation of GUI grounding, which can facilitates downstream tasks, including automated XR testing. A straightforward XR test generator can interact randomly within the app’s 3D environment, making it trapped in uninteractable space and resulting in an ineffective and inefficient testing process. In contrast, a more intelligent test generator, informed by the accurate locations and semantics of IGEs, can make wiser decisions on interaction targets and orders, forming test sequences that cover more functionalities faster. The most recent IGE detection approaches in SE are designed for 2D mobile apps and typically train a supervised object detection model based on a large-scale manually-labeled GUI dataset, usually with a pre-defined set of clickable GUI element categories like buttons and spinners. Such approaches can hardly be applied to IGE detection in XR apps, due to a multitude of challenges including complexities posed by open-vocabulary and heterogeneous IGE categories, intricacies of context-sensitive interactability, and the necessities of precise spatial perception and visual-semantic alignment for accurate IGE detection results. Thus, it is necessary to embark on the IGE research tailored to XR apps.

In this paper, we propose the first zero-shot cOntext-sensitive inteRactable GUI ElemeNT detection framework for Extended Reality apps, named Orienter. By imitating human behaviors, Orienter observes and understands the semantic contexts of XR app scenes first, before performing the detection. The detection process is iterated within a feedback-directed validation and reflection loop. Specifically, Orienter contains three components, including (1) Semantic context comprehension for capturing the apps’ GUI context, (2) Reflection-directed IGE candidate detection for identifying and localizing valid GUI elements based on multi-perspective description guided IGE detection, as well as feedback-directed reflection, and (3) Context-sensitive interactability classification which integrates semantic contexts for interactability prediction. To evaluate our approach and facilitate follow-up research, we spend more than three months constructing the first benchmark dataset which contains 1,552 images from 100 industrial-setting apps on Steam, with 4,470 interactable annotations across 766 semantics categories. Extensive experiments on the dataset demonstrate that Orienter is more effective than the state-of-the-art GUI element detection approaches (i.e., GPT-4o, OmniParser, YOLO v8, CenterNet2, Faster R-CNN, UIED, etc. ), surpassing their F1 Score by up to 3.7× and 121.4× (1.4× and 46.2× on average) in distinguishing the interactibility and semantics of the IGEs, respectively. Orienter is beneficial for boosting the performance of automatic testing by isolating the interactable action space from the whole space, regardless of the testing strategies employed. Experiments demonstrate that Orienter-guided testing covers 103.1% more IGEs with 125.7% more effective interactions than testing without action space isolation.

## 7. Phantom Rendering Detection: Identifying and Analyzing unnecessary UI computations

**Authors:** Zhihao Lin, Mingyi Zhou, Bo Sun, Han Hu, Gang Fan, Li Li

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797101

**中文总结:** 刻画移动端「幻影渲染」（屏外无用 UI 计算）问题，并提出 HapPRDetection，以 CPU Retired Instructions 细粒度采样与差分分析自动检测；在 OpenHarmony 热门应用中发现多起问题，单次操作最高浪费约 40% 指令。

**Abstract:** Modern mobile applications have high-resolution user interfaces (UI) and heavy computations, resulting in significant energy consumption and latency, especially on older devices. Precisely measuring the performance of mobile operations (e.g., the number of CPU instructions) and detecting performance issues are critical for mobile software engineering. In this study, we characterize a previously underexplored class of performance issues on mobile called Phantom Rendering, which occurs when mobile applications perform unnecessary UI-related offscreen computations but do not visually render them. For example, the animation component stops visually rendering on the screen but continues to refresh in the background. This problem represents a root-level disconnection between UI-related offscreen computational effort and visual rendering, inherent to dual-thread rendering architectures, which has been employed across most modern mobile platforms such as Android, iOS, and OpenHarmony. However, this is hard to automatically detect due to a lack of fine-grained performance measurements and detection methods. To address the challenges, we propose HapPRDetection that contains a fine-grained performance profiler that can sample CPU Retired Instructions, the CPU instructions that have completed their execution and are no longer in the pipeline, and algorithms for automated detection of Phantom Rendering through differential analysis and hierarchical attribution. Our approach advances performance analysis methodology by bridging the semantic gap between fine-grained computational measurements (i.e., the number of CPU Retired Instructions at the function level) and high-level rendering behavior. Through our evaluation of the top-22 real-world mobile applications by download volume in OpenHarmony with 193 test steps, we show that Phantom Rendering issues occur in 19 test cases across 8 applications and that they range up to 40% of wasted CPU instructions in each problematic operation. We provide new insights into mobile rendering efficiency and our detection strategy offers practical solutions to identify and resolve Phantom Rendering during the mobile development loop. Our approach and implementation are available at https://anonymous.4open.science/r/PhantomRendering-8356 .

## 8. SmartDispatch: Dynamic Substitution of NumPy-style APIs on Heterogenous CPU-GPU Systems

**Authors:** Jinku Cui (North Carolina State University), Yueming Hao (Meta), Shuyin Jiao (North Carolina State University), Jiajia Li (North Carolina State University), Xu Liu (North Carolina State University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808189

**中文总结:** 提出 SmartDispatch，在异构 CPU-GPU 上运行时将 NumPy 风格 API 动态替换为语义等价的 GPU/其他库实现，并结合微基准确定替换阈值；在真实 ML 基准上无需改代码即可获得 1.3×–5.8× 加速。

**Abstract:** The popularity of Python in various application domains has driven widespread adoption of NumPy-style APIs. To accelerate performance, libraries such as PyTorch, JAX, CuPy, and cuPyNumeric offer GPU-compatible counterparts to NumPy functions. However, substituting NumPy with these alternatives is not always beneficial due to overheads from type conversion, data transfer, and kernel launch costs. We present SmartDispatch, a runtime framework that dynamically substitutes NumPy-style API calls with semantically equivalent implementations from other libraries to improve performance. Our system includes a knowledge base of equivalent APIs, a hardware-aware microbenchmarking component to identify substitution thresholds, and a runtime substitution tool. Evaluation on four platforms with varying CPU-GPU architectures using machine learning models from real-world benchmarks shows that consistent performance gains (1.3× to 5.8×) can be achieved without requiring code modification, demonstrating the effectiveness of cross-library substitution in heterogeneous environments.

## 9. SwarmBox: A Plug-and-Play Drone Swarm Framework for Streamlined Development and Comprehensive Analysis

**Authors:** Minki Lee (Pohang University of Science and Technology), Seojin Lee (Daegu Gyeongbuk Institute of Science and Technology), Seulbae Kim (Pohang University of Science and Technology)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808100

**中文总结:** 提出开源测试床 SwarmBox，以即插即用软件架构、跨层涌现行为分析器与可配置实验环境支撑无人机集群开发与可复现评测；可降低样板工程、暴露传统调试难以捕获的交互故障，并缩小仿真到实物的部署鸿沟。

**Abstract:** Drone swarms are emerging as paradigm-shifting technology with the potential to redefine traditional robot missions such as logistics, surveillance, and disaster response, through their ability to coordinate large numbers of autonomous drones. Yet, progress in swarm research and development is constrained by a fragmented development ecosystem; every new algorithm must be validated on a bespoke testbed, introducing significant and redundant engineering overhead, while producing results that are difficult to reproduce or compare. As a remedy, we present SwarmBox, an open-source testbed framework that provides a shared foundation for swarm robotics. SwarmBox streamlines swarm research and development by providing three key capabilities: (1) a plug-and-play software architecture that decouples high-level swarm logic from low-level flight control and platform dependencies; (2) a swarm-level integrated analyzer that exposes emergent behaviors across drones and system layers to facilitate debugging and analysis; and (3) a configurable experimentation environment that supports diverse missions and communication topologies to promote fair and reproducible benchmarking.

Our evaluation demonstrates these benefits in practice. SwarmBox reduces software engineering effort by eliminating boilerplate code, abstracting low-level system details into coherent APIs, and simplifying swarm coordination into a uniform process. It improves fault diagnosis efficiency and uniquely exposes inter-agent interaction failures that traditional debugging methods cannot capture. It enables reproducible benchmarking by allowing systematic comparison of different swarm algorithms. It proves its generality and scalability by supporting diverse mission scenarios ranging from centralized coordination to fully decentralized swarms. Finally, its hardware abstraction layer minimizes the simulation-to-real gap, enabling unmodified application code to be seamlessly deployed on both simulation and physical drones. Together, these capabilities establish SwarmBox as a practical foundation for reproducible, community-driven swarm robotics research.

## 10. Unleashing HPC Application Performance through Software Deployment: A Joint Model of Software Parallelism and Co-location

**Authors:** Yuxin Ren (Huawei Technologies), li zhou (Huawei Technologies), Chumin Sun (Huawei Technologies), Rui Fan (Huawei Technologies), Jie Sun (Huawei Technologies), Ning Jia (Huawei Technologies), Xinwei Hu (Huawei Technologies)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808183

**中文总结:** 提出联合建模软件并行与共置干扰的 CPU 映射性能模型与嵌套迭代装箱搜索，自动优化 HPC 多组件部署；在商用超 5 万核集群上相对默认映射提升约 26.5%，并减少人工调优人月。

**Abstract:** Software deployment is a critical software engineering practice, particularly for high performance computing (HPC) software. The deployment determines the software execution performance because the deployment maps a number of software components to multiple CPUs in a server. Inappropriate mapping decreases software parallelism and increases resource contention due to software co-location on the same CPUs. However, calculating the mapping to maximize the software performance is challenging, primarily due to the lack of a joint performance model that accounts for both software parallelism and co-location. Consequently, existing industry practice has to rely on experienced engineers to manually tune the mapping during deployment, resulting in substantial human resource waste of man-months and suboptimal software performance.

This paper proposes a holistic approach to mapping multiple CPUs among multiple software components to achieve better applicability and performance. We develop a performance model for predicting performance impact of different CPU mapping configurations, along with a search algorithm to identify the best mapping scheme. Our performance model jointly considers software parallelism and co-location, breaks the performance estimation into regularized execution and interference coefficient to improve accuracy, and integrates expert knowledge to reduce the model complexity. Our search algorithm employs nested iterative packing algorithm to explore all possible mapping schemes, thereby uncovering the optimal solution. Evaluation on a multi-module HPC application shows 17% better performance than its default CPU mapping Our solution has been deployed in a commercial HPC cluster with more than 50K CPU cores, delivering 26.5% performance improvement and saving many man-months effort spent on performance tuning.
