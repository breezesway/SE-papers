# ISSTA 2026 Research Track — Systems, Mobile, and UI

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 10

## 1. Are We Stuck? Modeling and Detecting Deadlocks in Multi-Autonomous Vehicle Systems

**Authors:** Mingfei Cheng (Singapore Management University), Xiaofei Xie (Singapore Management University), Lili Quan (Singapore Management University (SMU)), Yuan Zhou (Zhejiang Sci-Tech University)

**Categories:** Systems, Mobile, and UI

**中文总结:** 首次形式化多自动驾驶车辆系统中的死锁问题，并提出 WaitWatch 测试框架，通过时空轨迹交叉对齐与定向变异诱导循环等待。在三种 ADS 上平均生成 2.28 倍于最佳基线的死锁场景，揭示现有系统协作活性不足。

**Abstract:** Autonomous driving system (ADS) testing is essential to ensure the safety and reliability of autonomous vehicles (AVs) prior to deployment. As ADSs are increasingly deployed in multi-AV traffic environments, it becomes crucial to assess their cooperative performance, particularly with respect to deadlock, a fundamental liveness issue in concurrent systems that can lead to traffic congestion and prolonged stalling. However, the analysis and testing of ADSs’ cooperative capabilities with respect to deadlock remain largely underexplored. In this work, we present the first systematic study of deadlock in multi-AV systems. We formalize deadlock in autonomous driving using a time-indexed wait-for relation grounded in vehicles’ planned trajectories and road-region occupancy. Building on this formalization, we propose WaitWatch, a wait-for–oriented testing framework that steers scenario generation via spatio-temporal intersection alignment of executed trajectories to induce circular wait patterns. WaitWatch integrates a Deadlock Judge, Intersection Alignment Feedback, and Intersection Oriented Mutation to efficiently uncover latent deadlock scenarios. We conduct an extensive evaluation on three representative ADSs. Experimental results show that, on average, WaitWatch generates 2.28×more deadlock scenarios (DLSs) than the best-performing baseline. By shifting the focus from single-AV evaluation to multi-AV cooperation, our approach identifies a range of previously unknown deadlock behaviors, revealing significant limitations in the cooperative and liveness capabilities of current ADSs. Our findings highlight a fundamental safety–liveness trade-off in deadlock resolution and emonstrate the need for systematic deadlock-aware testing in the development and validation of autonomous driving systems.


## 2. Automated Program Repair for UI-centric Android Bugs: How Far are We?

**Authors:** Junayed Mahmud (University of Central Florida), Sparsh Pandey (University of Central Florida), Nadeeshan De Silva, Atish Kumar Dipongkor, Jingjing Wu (University of Minnesota), Oscar Chaparro (William & Mary), Mattia Fazzini (University of Minnesota), Kevin Moran (University of Central Florida)

**Categories:** Systems, Mobile, and UI

**中文总结:** 在含 46 个合成与 25 个真实缺陷的 Android UI 数据集上，系统评估五种 APR 技术（含 LLM 方法）的修复能力。结果表明现有 APR 在跨 presentation/logic 推理、事件驱动与 UI 状态理解方面存在显著局限。

**Abstract:** Substantial research effort has been devoted to developing techniques for automated program repair (APR) that suggest patches for localized buggy code – and more recent techniques have begun to leverage the capabilities of code-centric large language models (LLMs). However, the scope and diversity of bugs to which these techniques have historically been applied is limited. In particular, the research community currently lacks a  comprehensive understanding of the performance of APR techniques on bugs that arise in UI-centric programs, such as mobile apps. Bugs in UI centric programs carry with them unique challenges, including (i) the need to reason across interconnected subroutines that connect presentation and program logic, (ii) event driven programming paradigms, and (iii) the need to reason about program state through cues in the UI.

In this paper, we investigate the effectiveness of existing APR techniques when applied to fix bugs in UI-centric programs – specifically Android applications. To explore this phenomenon, we conduct a comprehensive empirical study with five existing program repair techniques (including those that utilize LLMs) on a hybrid dataset including 46 synthetic bugs, generated via an Android-specific mutation tool, and 25 real bugs systematically mined from issue reports of 13 popular Android applications. Our findings illustrate important current limitations in resolving UI-related issues in mobile apps. We synthesize these results to form a taxonomy of the limitations of existing program repair techniques. This taxonomy details important limitations and can inform future research efforts in designing automated program repair tools for UI-centric bugs in mobile apps.


## 3. Bridging User Feedback and System Diagnosis: Reproducing Mobile Performance Issues from Reviews

**Authors:** Zhengquan Li (The Hong Kong University of Science and Technology (Guangzhou)), Zhenhao Li (York University), Sidong Feng (Monash University), Cuiyun Gao (Harbin Institute of Technology, Shenzhen), Tao Zhang (Macau University of Science and Technology, Macao SAR China), Zishuo Ding (The Hong Kong University of Science and Technology (Guangzhou))

**Categories:** Systems, Mobile, and UI

**中文总结:** 提出 RevPerf，从语义检索互补的用户评论中合成性能问题描述，再由执行 Agent 自动生成并执行复现命令，结合日志/GUI/资源监控检测性能异常。在构建数据集上复现成功率 72.73%，较最佳基线高 27.28 个百分点。

**Abstract:** Mobile application performance is a vital factor for user experience. Yet, performance issues are notoriously difficult to detect in development environments, where they often manifest less conspicuously, making their diagnosis more challenging. In this setting, app reviews from users with diverse device configurations can provide timely and context-rich information about emerging performance issues. However, unlike structured bug reports, app reviews are written by end-users and tend to be more ambiguous, with individual reviews often providing only partial descriptions of the underlying issue. To bridge this gap, we present RevPerf, the first approach to automatically reproduce mobile application performance issues by leveraging and synthesizing information from app reviews. RevPerf retrieves complementary reviews via semantic retrieval and uses prompt engineering to integrate them, enriching the original review with performance issue details. An execution agent is then employed to generate and execute commands to reproduce the issue. After executing all necessary steps, the system incorporates multifaceted detection methods to identify performance issues by monitoring Android logs, GUI changes, and system resource utilization during the reproduction process. Experimental results demonstrate that our proposed framework achieves a 72.73% success rate in reproducing performance issues on the constructed dataset, outperforming the best baseline by 27.28%.


## 4. Characterizing and Repairing Obsolete Android GUI Tests under UI Evolution

**Authors:** Shiwen Song (Singapore Management University), Yiheng Xiong (Singapore Management University), Wenbo Guo (Nanyang Technological University), Manqi Sun (The University of Hong Kong), Jiaolong Kong (Singapore Management University), Xiaofei Xie (Singapore Management University)

**Categories:** Systems, Mobile, and UI

**中文总结:** 本文构建含 736 个过时 Android GUI 测试的基准，并提出 GUIRevive，通过语义感知推理与目标导向 UI 探索修复控件识别歧义和控件不可达问题。成功修复 86.4% 的过时测试，工业部署修复率达 93%。

**Abstract:** Graphical user interface (GUI) tests are widely used in regression testing of mobile applications (apps) to validate app behavior from the user’s perspective. However, frequent app evolution, such as UI redesigns and feature updates, often renders existing GUI tests obsolete, even when underlying functionality remains unchanged. Automatically repairing such tests is critical for maintaining test suites and reducing substantial manual effort. Despite the practical importance, there is still a lack of a systematic understanding of the characteristics of obsolete GUI tests and a publicly available benchmark to support their study. To fill this gap, we construct a benchmark comprising 736 obsolete GUI tests collected from 36 real-world mobile apps across 668 historical versions. We then conduct a large-scale empirical study that reveals two major challenges in repairing obsolete GUI tests: First, identifying the intended target widget is difficult because widget attributes are frequently missing or unstable, and visually similar widgets may correspond to different functionalities. Second, the target widget is often no longer directly reachable from the failure state, as it may be hidden behind additional UI interactions or relocated to another screen. To address these challenges, we further propose GUIRevive, an automated GUI test repair approach that addresses semantic ambiguity in widget identification and target unreachability under UI evolution by integrating semantic-aware reasoning, functionality-preserving validation, and goal-guided UI exploration. Our evaluation shows that GUIRevive successfully repairs 86.4% of obsolete GUI tests and significantly outperforms state-of-the-art repair techniques by up to 220%.  Moreover, GUIRevive has been deployed in industrial settings, achieving a 93% repair success rate on industrial mobile apps.


## 5. ChromaEyes: Detecting Inconsistencies of User Interface Elements between Light and Dark Modes of Web Applications

**Authors:** K C Shweta, Byungchul Tak (Kyungpook National University), Tegawendé F. Bissyandé, Dongsun Kim (Korea University, South Korea)

**Categories:** Systems, Mobile, and UI

**中文总结:** ChromaEyes 通过分析 UI 元素的语义角色与功能含义，检测 Web 应用明暗模式转换中的界面不一致问题，而非依赖像素级对比。在 196 个真实 Web 应用的 2009 组截图上截图级准确率达 96.19%。

**Abstract:** Dark mode interfaces in web applications have gained widespread adoption because of improved user comfort and reduced power consumption. While these interfaces can be implemented through built-in support or browser extensions that convert light mode layouts, inconsistencies frequently arise during the conversion process, including invisible UI elements, misplaced components, and incorrect color mappings. Despite the prevalence of these issues, no existing approaches systematically detect such inconsistencies between light and dark mode interfaces. Our preliminary study shows that popular commercial vision language models and accessibility issue detectors are ineffective for this task. This paper presents ChromaEyes, a novel approach to automatically detecting inconsistencies of graphical user interface elements between light and dark mode layouts of web applications. Detecting such inconsistencies is inherently challenging given that, since mode conversion intentionally changes colors and contrast, UI elements in light and dark modes are expected to look different. Thus, pixel-wise or visual comparison cannot distinguish intentional adaptations from actual errors. ChromaEyes addresses this challenge by analyzing semantic roles and functional meanings of UI elements, enabling accurate correspondence detection between visually distinct but functionally equivalent components. We evaluate our approach on 2,009 screenshot pairs captured from 196 real web applications (147 with native dark mode support and 49 with browser extension-based conversion). ChromaEyes achieves 96.19% accuracy at the screenshot level and 97.95% at the application level, significantly outperforming vision-language models (e.g., GPT-4o) and state-of-the-art accessibility issue detectors (e.g., OwlEye, axe DevTools).


## 6. Fixed-Point Guided ADS Scenario Generation via Multi-Modal LLM Reasoning and Software Testing

**Authors:** xudong zhang, Shihao Zhu (State Key Laboratory of Computer Science,Institute of Software,Chinese Academy of Sciences,China), Yan Cai (Key Laboratory of System Software (Chinese Academy of Sciences), Beijing, China;Institute of Software, Chinese Academy of Sciences, Beijing, China)

**Categories:** Systems, Mobile, and UI

**中文总结:** 提出 InvarGen，用多模态 LLM 从事故视频提取 Scenario Fixed Points 并引导 intelligent fuzzing 与 structural mutation 生成 ADS 测试场景；较最佳基线多发现 37.5% 违规类型。

**Abstract:** Robust scenario generation is essential for systematically testing Autonomous Driving Systems (ADS) under rare and safety-critical conditions. However, existing methods face a dilemma: search-based approaches often lack semantic guidance, while specification-based methods rely on unscalable manual rules. Current LLM-driven techniques, meanwhile, primarily act as surface-level scene translators without explicit behavioral grounding. We present \textbf{InvarGen}, a framework that bridges these gaps by utilizing multi-modal LLMs as \textbf{parametric specification generators}. Central to \textbf{InvarGen} is the concept of \textit{Scenario Fixed Points}—dynamic safety invariants (e.g., context-aware headway thresholds) automatically extracted and formalized from unstructured accident videos. Unlike static templates, these fixed points adaptively constrain the search space, guiding a hybrid evolutionary process: \textit{Intelligent Fuzzing} exploits boundary parameters to trigger specific violations, while \textit{Structural Mutation} ensures the global exploration of diverse environmental contexts. Evaluation across 1,400 synthesized scenarios based on 200 real-world accidents demonstrates that \textbf{InvarGen} outperforms LLM-driven and traditional search-based baselines in multiple dimensions. It discovers up to \textbf{37.5% more unique violation types} than the best baseline, achieves a \textbf{30% fixed-point violation rate}, and improves semantic diversity by \textbf{25%}. It also maintains \textbf{100% compatibility} with OpenX standards, ensuring cross-platform simulation on Carla and Panosim. Ablation studies confirm that all components are statistically essential. These results highlight the promise of fixed-point semantics as a principled bridge between unstructured LLM reasoning and rigorous robustness testing.


## 7. FuncDroid: Towards Inter-Functional Flows for Comprehensive Mobile App GUI Testing

**Authors:** Jinlong He (Institute of Software, Chinese Academy of Sciences), xiachangwei (Institute of Software, Chinese Academy of Sciences), Binru Huang (Institute of Software, Chinese Academy of Sciences), Jiwei Yan (Institute of Software, Chinese Academy of Sciences), Jun Yan (Institute of Software, Chinese Academy of Sciences), Jian Zhang (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Systems, Mobile, and UI

**中文总结:** 提出 FuncDroid，基于 Functional Flow Graph 与长短期视图引导探索跨功能 GUI 流；覆盖率 +28%、bug 数 +107%，并在商业 app 中发现 18 个未知非 crash 功能 bug。

**Abstract:** As mobile application (app) functionalities grow increasingly complex and their iterations accelerate, ensuring high reliability presents significant challenges. While functionality-oriented GUI testing has attracted growing research attention, existing approaches largely overlook interactions across functionalities, making them ineffective at uncovering deep bugs hidden in inter-functional behaviors. To fill this gap, we first design a \textbf{F}unctional \textbf{F}low \textbf{G}raph (\textbf{FFG}), a behavioral model that explicitly captures an app’s functional units and their inter-functional interactions. Based on the FFG, we further introduce an \textit{inter-functional-flow-oriented GUI testing} approach with the dual goals of precise model construction and deep bug detection. This approach is realized through a \textit{long–short-term-view-guided testing} process. By combining two complementary test-generation views, it can adaptively refine functional boundaries and systematically explore inter-functional flows under diverse triggering conditions. We implement our approach in a tool called \textbf{FuncDroid}, and evaluate it on two benchmarks: (1) a widely‑used open‑source benchmark with 50 reproducible crash bugs and (2) a diverse set of 52 popular commercial apps. Experimental results demonstrate that FuncDroid significantly outperforms state‑of‑the‑art baselines in both coverage (+28%) and bug detection number (+107%). Moreover, FuncDroid successfully uncovers 18 previously unknown non‑crash functional bugs in commercial apps, confirming its practical effectiveness.


## 8. LogNexus: Effective Log Compression via Unified Redundancy Encoding

**Authors:** Yang Liu (School of Software Engineering, Sun Yat-sen University), Kaiming Zhang (School of Software Engineering, Sun Yat-sen University), Zhuangbin Chen (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Systems, Mobile, and UI

**中文总结:** LogNexus 提出统一冗余编码范式，构建 Unified Redundancy Tree 联合提取结构与变量模式以压缩日志。在 16 个数据集上 14 个压缩率最高（提升 9.48%–89.13%），速度最快达 1.51×–40.06×，且解压可完整还原全部 token。

**Abstract:** State-of-the-art log compressors typically rely on a decoupled “parse-then-compress” workflow, where parsing is optimized for semantic accuracy (i.e., event identification) rather than storage efficiency. Through a comprehensive empirical study, we reveal that this architectural decoupling prevents the exploitation of deep correlations between static templates and dynamic variables. To address it, we propose LogNexus based on the principle of unified redundancy encoding, a new log compression paradigm that co-designs structural extraction and variable encoding. LogNexus constructs a Unified Redundancy Tree (URT) using a hierarchical strategy that progressively mines frequent “structure+variable” patterns in logs. Such a design captures deep contextual redundancies ignored by traditional methods while minimizing computational overhead by pre-emptively encoding dominant patterns. Extensive evaluation on 16 benchmark datasets demonstrates that LogNexus establishes a new state-of-the-art. It achieves the highest compression ratio on 14 datasets (outperforming baselines by 9.48% to 89.13%) and the fastest speed (1.51× to 40.06× faster than competitors). Furthermore, when configured in non-chunked mode to maximize global pattern discovery, LogNexus boosts its compression ratio by 285.13%, which is 27.08% higher than the best baseline, while retaining a 2.43× speed advantage. The decompression audit further shows that LogNexus successfully restores every token on all 16 datasets.


## 9. RippleGUItester: Change-Aware Exploratory Testing

**Authors:** Yanqi Su (Technical University of Munich), Michael Pradel (CISPA Helmholtz Center for Information Security), Chunyang Chen (TU Munich)

**Categories:** Systems, Mobile, and UI

**中文总结:** 提出 RippleGUItester，以代码变更为起点做 LLM 变更影响分析与 GUI 差分测试，并用多模态检测区分回归与预期行为变更。在 Firefox、Godot 等四系统数百次变更中发现 26 个未知 bug，16 个已修复。

**Abstract:** Software systems evolve continuously through frequent code changes, yet such changes often introduce unintended bugs despite extensive testing and code review. Existing testing approaches are largely constrained to predefined execution paths or rely on unguided exploration, leaving many change-induced issues undetected. To address this challenge, we present RippleGUItester, a change-driven testing system that treats a code change as the epicenter of a ripple effect and explores its broader, user-visible impacts via the GUI. Given a code change, RippleGUItester performs LLM-based change-impact analysis to generate and enrich realistic test scenarios, executes these scenarios on both pre-change and post-change versions of the system, and applies differential analysis to identify behavioral differences. Crucially, RippleGUItester employs multimodal bug detection, comparing visual GUI changes and interpreting them in the context of natural-language change intents to distinguish unintended bugs from intended behavioral updates. We evaluate our approach on hundreds of real-world code changes across four widely used software systems: Firefox, Zettlr, JabRef, and Godot. Our results show that the proposed approach uncovers bugs introduced by code changes that were missed by existing test suites, CI pipelines, and code review. In total, we identify 26 previously unknown bugs that still exist in the latest versions of the evaluated systems. After reporting, 16 bugs have been fixed, 2 have been confirmed, 6 are still under discussion, and 2 were marked as intended. We envision RippleGUItester being applied before or shortly after a code change is merged, enabling earlier detection of regressions.


## 10. You are deceived in the pocket: Intrusive Advertisements in Mobile Applications: An Exploratory Study

**Authors:** Miaoying Cai (DISSec, NDST, College of Cyber Science, Nankai University, China), Dongsun Kim (Korea University, South Korea), Lingling Fan (Nankai University), Xiangyu Zhang (DISSec, NDST, College of Cyber Science, Nankai University, China), Sen Chen (Nankai University)

**Categories:** Systems, Mobile, and UI

**中文总结:** 基于状态转移逻辑提出移动侵入式广告形式化分类体系并开发自动检测工具。分析 6000+ Android 应用确认侵入式广告普遍存在，并对比各司法辖区政策标准发现显著不一致。

**Abstract:** Mobile advertising has become the primary monetization module for the Android ecosystem. However, this growth is accompanied by increasingly complex intrusive advertisements that undermine user agency through sophisticated behavioral interference. Current detection research remains confined to the web context, failing to address the unique in-app characteristics of mobile intrusive ads. Existing ad analysis tools struggle to distinguish voluntary human actions from forced interactions due to the absence of intent-aware modeling. Furthermore, existing marketplace policies and legal frameworks lack unified terminology and enforceable rules, leading to inconsistent oversight.

In this paper, we conduct an exploratory study to systematically investigate and model these behaviors. We propose a formal taxonomy grounded in state-transition logic and develop an automated tool to identify intrusive patterns. Our analysis of more than 6,000 apps confirms the prevalence of mobile intrusive ads. Additionally, we perform a comparative analysis of mainstream regulations, uncovering significant misalignments in policy standards across different jurisdictions. Our study establishes a critical theoretical and practical foundation for ecosystem governance, enabling more effective detection and evidence-based policy refinement.

