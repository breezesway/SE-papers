# ASE 2025 Research Track — Systems, Mobile, and UI

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 24

## 1. ADPerf: Investigating and Testing Performance in Autonomous Driving Systems

**Authors:** Tri Minh-Triet Pham (Concordia University), Diego Elias Costa (Concordia University, Canada), Weiyi Shang (University of Waterloo), Jinqiu Yang (Concordia University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334384

**中文总结:** 系统测量 Apollo 多传感器融合感知模块延迟，提出 ADPerf 通过修改点云生成测试场景以触发 LiDAR 检测延迟增加，评估对障碍物可用性与轨迹预测的影响。

**Abstract:** Perception is crucial to the operation of autonomous driving systems (ADSs), which rely on multiple sensors, such as cameras and LiDARs, combined with code logic and deep learning models to detect obstacles for time-sensitive decisions. Consequently, the latency of the perception module is critical to the safety and effectiveness of ADSs. However, the latency of the perception module and its resilience to various changes in the LiDAR point cloud are not yet fully understood. In this work, we present the first comprehensive investigation measuring and modeling the availability of an industry-grade ADS multi-sensor fusion (MSF) perception module i.e., Apollo. Learning from this investigation, we introduce ADPerf, a tool modifying the point cloud data (PCD) to generate simple and realistic testing scenarios for LiDAR detection which can increase the detection latency. Increasing latency decreases the availability of the detected obstacles, decreasing the accuracy of the obstacle-dependent decisions in ADSs. We conduct a study to assess the effects of ADPerf-generated PCD on the availability of widely-used LiDAR-based 3D obstacle detections, and in turn, trajectory predictors. Our evaluation highlights the need to assess the availability of perception components, especially LiDAR-based detectors, and their robustness to various noises and modifications as they can be a major bottleneck to the performance of the ADS system. Such an adverse outcome will also further propagate to other modules, reducing the overall reliability of ADSs.


## 2. A Multi-Modality Evaluation of the Reality Gap in Autonomous Driving Systems

**Authors:** Stefano Carlo Lambertenghi (Technische Universität München, fortiss GmbH), Mirena Flores Valdez (Technical University of Munich), Andrea Stocco (Technical University of Munich, fortiss)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334703

**中文总结:** 对比 SiL、ViL、混合现实与真实道路四种 ADS 测试模态在驱动、感知与行为保真度上的差异；MR 在提升感知 realism 同时兼顾安全，并识别 reality gap 出现的条件。

**Abstract:** Simulation-based testing is a cornerstone of Autonomous Driving System (ADS) development, offering safe and scalable evaluation across diverse driving scenarios. However, discrepancies between simulated and real-world behavior, known as the reality gap, challenge the transferability of test results to deployed systems. In this paper, we present a comprehensive empirical study comparing four representative testing modalities: Software-in-the-Loop (SiL), Vehicle-in-the-Loop (ViL), Mixed-Reality (MR), and full real-world testing. Using a small-scale physical vehicle equipped with real sensors (camera and LiDAR), and its digital twin, we implement each setup and evaluate two ADS architectures (modular and end-to-end) across diverse driving scenarios involving real obstacles, road topologies, and indoor environments. We systematically assess the impact of each testing modality along three dimensions of the reality gap: actuation, perception, and behavioral fidelity. Our results show that while SiL and ViL setups simplify critical aspects of real-world dynamics and sensing, MR testing improves perceptual realism without compromising safety or control. Importantly, we identify the conditions under which failures do not transfer across testing modalities and isolate the underlying dimensions of the gap responsible for these discrepancies. Our findings offer actionable insights into the respective strengths and limitations of each modality and outline a path toward more robust and transferable validation of autonomous driving systems.


## 3. AppBDS: LLM-Powered Description Synthesis for Sensitive Behaviors in Mobile Apps

**Authors:** Zichen Liu (Arizona State University), Xusheng Xiao (Arizona State University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334675

**中文总结:** 提出 AppBDS，结合程序分析与 LLM，基于 UI-Fused Call Graph、隐私政策与 PP-KB 相似应用知识，为移动应用敏感权限行为生成代码语义与 UI 上下文驱动的详细解释。

**Abstract:** As mobile applications (i.e., apps) increasingly manage a wide variety of user needs, their access to sensitive data intensifies privacy concerns among users. While app markets employ permissions to regulate the private data access, the lack of explanation of permission uses render this mechanism less successful. Existing techniques that extract explanatory sentences from app descriptions to inform users about sensitive behaviors are also limited, as many app behaviors remain unexplained in their descriptions. To tackle these issues, we propose AppBDS, a novel approach that integrates program analysis with Large Language Models (LLM) to process code semantics and UI contexts, complemented by privacy policies and information from similar apps, to generate detailed explanations for apps’ sensitive behaviors. Specifically, AppBDS integrates code semantics with UI contexts to build a UI-Fused Call Graph (UCG) for each app. Additionally, AppBDS summarizes permission-related propositions from privacy policies and utilizes similar apps’ information from a curated knowledge base (PP-KB) to improve LLMs’ domain knowledge in explaining permission uses. In particular, AppBDS curates the PP-KB by using LLMs to extract permissionrelated propositions and infer permission descriptions of apps from a wide range of categories. Our evaluation results on 270 real apps indicate that AppBDS significantly outperforms state-of-the-art approaches in terms of factuality and semantic richness, as validated through extensive experiments and manual inspection.


## 4. Argus: Resilience-Oriented Safety Assurance Framework for End-to-End ADSs

**Authors:** Dingji Wang (Fudan University), You Lu (Fudan University), Bihuan Chen (Fudan University), Shuo Hao (Fudan University), Haowen Jiang (Fudan University, China), Yifan Tian (Fudan University), Xin Peng (Fudan University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334287

**中文总结:** 提出 Argus 运行时弹性安全框架，持续监控端到端 ADS 轨迹并在 EGO 车辆不安全时由 hazard mitigator 接管控制；集成 TCP、UniAD、VAD 等系统并验证有效提升 resilience。

**Abstract:** End-to-end autonomous driving systems (ADSs), with their strong capabilities in environmental perception and generalizable driving decisions, are attracting growing attention from both academia and industry. However, once deployed on public roads, ADSs are inevitably exposed to diverse driving hazards that may compromise safety and degrade system performance. This raises a strong demand for resilience of ADSs, particularly the capability to continuously monitor driving hazards and adaptively respond to potential safety violations, which is crucial for maintaining robust driving behaviors in complex driving scenarios.

To bridge this gap, we propose a resilience-oriented runtime framework, named Argus, to mitigate the driving hazards, thus preventing potential safety violations and improving the driving performance of an ADS. Argus continuously monitors the trajectories generated by the ADS for potential hazards and, whenever the EGO vehicle is deemed unsafe, seamlessly takes control via a hazard mitigator. We integrate Argus with three state-of-the-art end-to-end ADSs, i.e., TCP, UniAD and VAD. Our evaluation has demonstrated that Argus effectively and efficiently enhances the resilience of ADSs, improving the driving score of ADSs by 150.30% on average, and preventing 64.38% of the violations, with little additional time overhead.


## 5. Automated Detection of Web Application Navigation Barriers for Screen Reader Users

**Authors:** Shubhi Jain (University of California, Irvine), Syed Fatiul Huq (University of California, Irvine), Ziyao He (University of California, Irvine), Sam Malek (University of California at Irvine)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334511

**中文总结:** 提出 A11yNavigator，利用 NVDA 模拟 Tab/Arrow/Quick Nav 三种屏幕阅读器导航策略，检测网页元素能否被定位与激活；在 26 个网站上发现 WAVE/Lighthouse 遗漏的动态无障碍问题。

**Abstract:** An estimated 43.3 million people worldwide live with blindness and rely on screen readers (SRs) to access the web. To support accessible development, software teams often rely on automated tools like WAVE and Lighthouse to detect accessibility issues. However, these tools primarily rely on static rule-based analysis and are largely limited to detecting labeling errors relevant to screen reader users. They fail to capture dynamic accessibility issues—specifically, whether user interface (UI) elements can be located and activated using a screen reader, which is essential for accessing core webpage functionality. To address this gap, we present A11yNavigator, an automated accessibility testing tool that simulates screen reader navigation to detect UI elements that cannot be either (1) located or (2) activated via the screen reader. A11yNavigator leverages NVDA, one of the most widely used screen readers, and supports three common navigation strategies: Tab, Arrow, and Quick Navigation keys. We evaluate A11yNavigator across 26 real-world websites and demonstrate its effectiveness in uncovering issues missed by existing tools. Our results highlight its high precision and recall in detecting barriers that go beyond static analysis.


## 6. Beyond Static GUI Agent: Evolving LLM-based GUI Testing via Dynamic Memory

**Authors:** Mengzhuo Chen (Institute of Software, Chinese Academy of Sciences), Zhe Liu (Institute of Software, Chinese Academy of Sciences), Chunyang Chen (TU Munich), Junjie Wang (Institute of Software at Chinese Academy of Sciences), Yangguang Xue (University of Chinese Academy of Sciences), Boyu Wu (Institute of Software at Chinese Academy of Sciences), Yuekai Huang (Institute of Software, Chinese Academy of Sciences), Libin Wu (Institute of Software Chinese Academy of Sciences), Qing Wang (Institute of Software at Chinese Academy of Sciences)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334687

**中文总结:** 提出 MemoDroid 三层动态记忆插件（情节/反思/策略），使 LLM GUI 测试能跨应用复用成功经验、规避无效操作并优先探索易错功能，可轻量集成到现有 GUI 测试框架。

**Abstract:** The development of Large Language Models (LLMs) enables LLM-based GUI testing to interact with graphical user interfaces by understanding GUI screenshots and generating actions, which are widely applied in industry and academia. However, current approaches test each app in isolation, lacking mechanisms for experience accumulation and reuse. This limitation often causes GUI testing approaches to miss deeper exploration and fail to trigger bug-prone functionalities. To address this, we propose MemoDroid, a three-layer memory mechanism that augments LLM-based GUI testing with the ability to evolve through repeated interaction. MemoDroid designs episodic memory to capture functional-level testing traces, reflective memory to summarize failure patterns and redundant behaviors, and strategic memory to synthesize cross-app exploration strategies. These memory layers are dynamically retrieved and injected into LLM prompts at runtime, enabling the agent to reuse successful behaviors, avoid ineffective actions, and prioritize bug-prone paths. We implement MemoDroid as a lightweight plugin, which can be integrated into existing LLM-based GUI testing approaches. We evaluate MemoDroid on real-world apps from 15 diverse categories. Results show that MemoDroid enhances GUI testing performance across five baseline methods, with activity and code coverage increasing by 79% - 96% and 81% - 97%, and bug detection improving by 57% - 198%. Ablation studies confirm the contributions of each memory layer. Furthermore, MemoDroid detects 49 new bugs in 200 real-world apps, with 35 confirmed fixes and 14 acknowledged by developers, showing its practical value in memory-driven GUI testing.


## 7. Characterizing and Repairing Color-Related Accessibility Issues in Android Apps

**Authors:** Jiahao Gu (Xiamen University), Huaxun Huang (Xiamen University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334532

**中文总结:** 先实证归纳 Android 开发者修复颜色相关无障碍问题的常见配色策略，并提出 DroidPalette，将策略编码为自动化修复流程，结合 Android 框架与第三方库候选属性生成用户与开发者均可接受的对比度修复补丁。

**Abstract:** As Android apps become increasingly prevalent in daily life, a common issue in the development process is the configuration of UI colors, leading to color-related accessibility issues that make the text or images on the app’s UI difficult to see due to low color contrast. Such color-related accessibility issues are among the top issues in apps, having a negative impact on vision and user experience. However, state-of-the-art approaches are based on predefined rules and lack an understanding of strategies for alternative colors, therefore failing to generate patches acceptable to both app users and developers. To address this research gap, we first conducted an empirical study to explore common strategies used by app developers when fixing real-world color-related accessibility issues. Based on these findings, we proposed DroidPalette, an automated approach for repairing color-related accessibility issues in Android apps. DroidPalette encodes the common strategies used by app developers for selecting issue-fixing colors, as identified in our empirical study, and combines this with the candidate issue-fixing attributes identified from the Android framework and third-party libraries to generate patches. We evaluated DroidPalette on 316 color-related accessibility issues across 105 real-world Android apps, achieving a success rate of 67.72%. Encouragingly, out of 13 patches submitted to GitHub repositories, 8 have received positive feedback from app developers.


## 8. Debun: Detecting Bundled JavaScript Libraries on Web using Property-Order Graphs

**Authors:** Seojin Kim (North Carolina State University), Sungmin Park (Korea University), Jihyeok Park (Korea University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334587

**中文总结:** 提出 Debun，利用打包后仍保留的属性操作顺序构建 Property-Order Graph（POG）做函数级指纹，检测全局不可达的 bundled JS 库及版本；在 68 个高流量网站上库检测 F1 达 91.76%，较现有工具提升 1.39 倍。

**Abstract:** Detecting front-end JavaScript libraries in web applications is essential for website profiling, vulnerability detection, and dependency management. However, bundlers like Webpack transpile code in various ways, altering the original directory and code structure, which complicates library detection. While state-of-the-art techniques utilize property pattern-based library detection at runtime, they face two key limitations: (1) they cannot detect libraries inaccessible from the global object, and (2) they have limitations in granular version detection. To address these challenges, we present DEBUN, a scalable technique for detecting JavaScript libraries and their versions using function-level fingerprints. Our key insight is that bundlers preserve the property names and execution order of property operations, even after transpilation. To leverage this, we introduce the property-order graph (POG), which represents the execution order of property operations within a function body. We evaluate DEBUN on 68 high-traffic websites with 78 front-end JavaScript libraries. Our approach outperforms existing tools, achieving a 91.76% F1-score in library detection (1.39x higher) and an 82.52% F1-score in version identification with inclusion match (1.38x higher).


## 9. Don't Mess with Bro's Cheese! An Empirical Study of Resource Conflict in Android Multi-window

**Authors:** Chenkai Guo (Nankai University, China), Huimin Zhao (College of Cryptology and Cyber Science, Nankai University), Tianhong Wang (College of Computer Science, Nankai University), Naipeng Dong (The University of Queensland, Australia), Qingqing Dong (College of Cryptology and Cyber Science, Nankai University), Jiarui Che (College of Computer Science, Nankai University), Yaqiong Qiao (College of Cryptology and Cyber Science, Nankai University), Xiangyang Luo (State Key Laboratory of Mathematical Engineering and Advanced Computing), Zheli Liu (Nankai University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334722

**中文总结:** 首次系统研究 Android 多窗口资源冲突（MRC），按触发模式与资源状态分三类；提出静态分析工具 MRC-Detector，在 F-Droid 与 Google Play 共 15 万+ App 中发现大量功能与安全风险。

**Abstract:** The multi-window mode in Android has greatly improved productivity and usability by allowing multiple apps to run concurrently. However, alongside the advantages, such mode also introduces unforeseen risks in both functionality and security. In this work, we present the first systematic study to identify a previously unexplored class of issues, termed Multi-window Resource Conflicts (MRCs). Such conflicts occur when multiple app windows access the same system resource concurrently, potentially leading to crashes, functionality failures or unintended behaviors. To enhance the robustness and security of Android multi-window execution, we conduct a systematic and in-depth empirical study on the MRCs. We begin with a comprehensive root cause analysis, categorizing MRCs into three fundamental types based on their triggering patterns and affected resource states. To enable large-scale detection, we develop MRC-Detector, a static analysis framework that automatically identifies MRC issues in Android apps. Our manual verification confirms its high accuracy and effectiveness. We apply the MRC-Detector to the detection of over $150k$ real-world apps from F-droid and Google Play, uncovering the prevalence of MRC risks. Additionally, the distribution of MRC issues is analyzed in depth across multiple dimensions, including MRC type, APK size, app source and security classification. We further investigated the recognition and confirmation from developers and received $14$ positive responses from vendors and project maintainers. Finally, comprehensive mitigation strategies are discussed. The materials of the study are available at: https://github.com/Huimilia/MRC .


## 10. Generating Failure-Based Oracles to Support Testing of Reported Bugs in Android Apps

**Authors:** Jack Johnson (University of Minnesota), Junayed Mahmud (University of Central Florida), Oscar Chaparro (William & Mary), Kevin Moran (University of Central Florida), Mattia Fazzini (University of Minnesota)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334637

**中文总结:** 构建 AndroB2O，利用 LLM 对 bug 报告与 GUI 屏幕的多模态推理，自动为非崩溃功能失败生成断言式测试 oracle；填补 Android bug 报告验证中 oracle 创建长期缺乏自动化的空白。

**Abstract:** In the context of mobile apps, bug report management tasks have been shown to be among the most time-consuming and intellectually intensive software maintenance activities. As such, researchers have developed tools to automate the reproduction, validation, and localization of reported bugs. However, one complex, time-consuming, and important task that lacks automated support is the creation of test oracles for reported functional failures that manifest through the GUI. This is challenging task–requiring nuanced, multi-modal reasoning about bug descriptions, affected GUI components, and the characteristics of the related erroneous program state(s).

To explore the feasibility of automating this task, we conduct a empirical investigation into how the multi-modal (i.e., text and GUI-related code) reasoning capabilities of Large Language Models (LLMs) can be used to automatically generate assertion-based test oracles for non-crashing, functional failures described in Android app bug reports. Building upon the findings of this study, we construct and evaluate AndroB2O, an automated, LLM-based approach that, given a bug report and the GUI screen associated with the reported failure as inputs, generates failure-based oracles (FBOs) in the form of test assertions. The approach first identifies the GUI elements related to the failure and then defines assertions that aim to confirm the absence of the failure based on the elements’ properties. To evaluate AndroB2O, we create the first dataset of Android bug reports containing test cases with GUI interactions and test oracles that reveal reported failures. The results of our evaluation on 152 failures show that AndroB2O is able to generate FBOs that successfully identify the failure (and hence can confirm it’s absence) in 61.2% of the cases. We integrated AndroB2O with ReBL, a failure reproduction tool, to evaluate its effectiveness in automated generation of test cases complete with oracles for reported failures, and obtained promising results.


## 11. GlassWing: A Tailored Static Analysis Approach for Flutter Android Apps

**Authors:** Xiangyu Zhang (DISSec, NDST, College of Cyber Science, Nankai University, China), Yucheng Su (Intelligence and Offensive Defense Lab, Xiaohongshu Inc., China), Lingling Fan (Nankai University), Miaoying Cai (DISSec, NDST, College of Cyber Science, Nankai University, China), Sen Chen (Nankai University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334412

**中文总结:** 提出 GlassWing，首个面向 Flutter Android 的定制静态分析，通过数据流分析揭示 Dart-Java 隐式跨语言调用；在 1,023 个真实 app 上显著增强 Soot 等现有分析器的完整性。

**Abstract:** The variety of mobile operating systems available in the market has led to the emergence of cross-platform frameworks, which simplify the development and deployment of mobile applications across multiple platforms simultaneously. Among these, the Flutter framework promoted by Google has become the most widely used cross-platform development framework. To date, no work has provided support for the static analysis of Flutter applications on the Android platform. State-of-the-art static analyzers fail to “see” the implicit invocation between the Dart language used by the Flutter framework and the Java used by the native Android platform, posing a significant threat to the completeness of the mobile software analysis. In this paper, we present GlassWing, the first tailored approach to static analysis for Flutter Android apps. GlassWing leverages a data-flow-oriented approach to conduct key program semantic extraction of Flutter apps and discloses the implicit Dart-Java invocation relations, thereby making cross-language invocation visible. Extensive evaluation on 1,023 popular real-world Flutter apps indicates that GlassWing enhances static analysis of Flutter apps integrated with Soot by parsing 141% more Jimple code lines, extending the call graph with more edges and nodes, and revealing almost 3X sensitive data leaks that were previously undetected with FlowDroid. GlassWing sheds light on downstream research fields for Flutter apps (e.g., program graph analysis, taint analysis, and malicious software analysis). Many current and future Android analysis initiatives can be enhanced by seamlessly incorporating GlassWing’s insights.


## 12. GUIFuzz++: Unleashing Grey-box Fuzzing on Desktop Graphical User Interfacing Applications

**Authors:** Dillon Otto (University of Utah), Tanner Rowlett (University of Utah), Stefan Nagy (University of Utah)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334307

**中文总结:** 提出 GUIFuzz++，首个通用桌面 GUI 灰盒 fuzzer，填补 AFL++ 等无法测 GUI、移动 Monkey 无法移植桌面生态的空白；可对桌面图形界面代码做大规模自动化 bug 发现。

**Abstract:** Desktop applications represent one of today’s largest software ecosystems, accounting for over 96% of workplace computing and supporting essential operations across critical sectors such as healthcare, commerce, industry, and government. Though modern software is increasingly being vetted through fuzzing—an automated testing technique for large-scale bug discovery—a major component of desktop applications remains universally under-vetted: the Graphical User Interface (GUI). Existing desktop-based fuzzers like AFL++ and libFuzzer are limited to non-GUI interfaces (e.g., file- or buffer-based inputs), rendering them wholly incompatible with GUIs. Conversely, mobile app GUI fuzzers like Android’s Monkey and iOS’s XCMonkey rely on platform-specific SDKs and event-handling, rendering them fundamentally unportable to the broader, more complex landscape of desktop software. For these reasons, desktop GUI code remains largely under-tested, burdening users with numerous GUI-induced errors that should, in principle, be just as discoverable as any other well-fuzzed class of software bugs.

This paper introduces GUIFuzz++: the first general-purpose fuzzer for desktop GUI software. Unlike desktop fuzzers that randomly mutate file- or buffer-based inputs, GUIFuzz++ exclusively targets GUI interactions—clicks, scrolls, key presses, window navigation, and more—to uncover complex event sequences triggering GUI-induced program errors. Central to our approach is a novel GUI Interaction Interpreter: a middle-layer translating fuzzer-generated random inputs into distinct GUI operations, enabling successful non-GUI fuzzers like AFL++ to be easily ported to testing GUIs. Beyond supporting today’s most popular GUI development frameworks like QT, GTK, and Xorg, we introduce a suite of enhancements capitalizing on ubiquitous Software Accessibility Technologies, significantly boosting GUI fuzzing precision as well as GUI bug-finding effectiveness.

We integrate GUIFuzz++ as a prototype atop state-of-the-art GUI-agnostic fuzzer AFL++, and perform a large-scale ablation study of its fundamental components and enhancements. In an evaluation across 12 popular, real-world GUI applications, GUIFuzz++ uncovers 23 previously-unknown GUI-induced bugs— with 14 thus far confirmed or fixed by developers.


## 13. HybridSIMD: A Super C++ SIMD Library with Integrated Auto-tuning Capabilities

**Authors:** Haolin Pan (Institute of Software, Chinese Academy of Sciences;School of Intelligent Science and Technology, HIAS, UCAS, Hangzhou;University of Chinese Academy of Sciences), Xulin Zhou (Institute of Software, Chinese Academy of Sciences; University of Chinese Academy of Sciences), Mingjie Xing (Institute of Software, Chinese Academy of Sciences), Yanjun Wu (Institute of Software, Chinese Academy of Sciences)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334306

**中文总结:** 提出 HybridSIMD，统一 C++ SIMD 库接口并实现算子级跨库协同优化与内置 autotuning；缓解现有 SIMD 生态碎片化与可变向量长度支持不足导致的硬件利用率问题。

**Abstract:** Single Instruction, Multiple Data (SIMD) technology is crucial for enhancing computational efficiency in High-Performance Computing (HPC) and Artificial Intelligence (AI). While automatic vectorization methods offer ease of use, they suffer from limitations in hardware utilization due to compilers’ static analysis capabilities. Manual vectorization, on the other hand, allows for fine-grained control and potentially better hardware utilization, but manual approaches using low-level intrinsics specifically introduce challenges in portability and development complexity. Existing C++ SIMD libraries aim to address these issues but introduce new challenges such as performance and usability fragmentation and underutilization of hardware potential due to limited support for variable vector element counts. To overcome these limitations, this paper introduces HybridSIMD, a novel unified and autotunable SIMD library. HybridSIMD is designed to resolve both fragmentation and hardware underutilization by enabling operator-level hybrid collaborative optimization across different SIMD libraries through a unified interface. A built-in auto-tuning mechanism, leveraging static analysis and hierarchical search, automatically optimizes and tunes programs for high performance across diverse hardware platforms without human intervention. Experimental results across six real-world HPC benchmarks on AVX2, AVX512, and NEON architectures demonstrate that HybridSIMD outperforms state-of-the-art SIMD libraries. Notably, the highest speedups achieved by HybridSIMD are 185.34$\times$ on AVX2, 97.80$\times$ on AVX512, and 71.32$\times$ on NEON, showcasing superior computational efficiency and adaptability.


## 14. IMUFUZZER: Resilience-based Discovery of Signal Injection Attacks on Robotic Aerial Vehicles

**Authors:** Sudharssan Mohan (University of Texas at Dallas), Kyeongseok Yang (Korea University), Zelun Kong (The University of Texas at Dallas), Yonghwi Kwon (University of Maryland), Junghwan Rhee (University of Central Oklahoma), Tyler Summers (University of Texas at Dallas), Hongjun Choi (DGIST), Heejo Lee (Korea University), Chung Hwan Kim (University of Texas at Dallas)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334621

**中文总结:** 提出 IMUFUZZER，基于 resilience 反馈的 fuzzing 在高保真 RAV 仿真中为 IMU 传感器生成逼真噪声并规划任务路径；自动发现依赖物理状态的信号注入攻击及致任务失败场景。

**Abstract:** Robotic aerial vehicles (RAVs), particularly drones, are crucial in civil and military sectors. However, researchers have found that adversaries can inject noise into sensor measurements and cause physical impacts on the RAVs like crashes. Although identifying such signal injection attacks is essential to evaluate and improve the robustness of an RAV, it is challenging to discover them since their impact depends on the RAV’s physical states and the search space of noise signals and physical states is vast due to its dynamic nature.

This paper proposes IMUFUZZER, a feedback-driven fuzzing framework, to automatically test an RAV system and discover signal injection attacks. IMUFUZZER generates realistic noise signals for various inertial measurement unit (IMU) sensors, and monitors their impact on RAV control to detect mission failures, leveraging a high-fidelity RAV simulator. To find the physical states that attacks depend on, IMUFUZZER generates various mission paths that the RAV will fly through. We develop a novel feedback mechanism to quantify the resilience of the RAV against attacks and efficiently guide the fuzzing process to find signal injection attacks. Using IMUFUZZER, we have discovered 23 successful signal injection attacks on popular RAV control software (ArduPilot). We evaluate the correctness and effectiveness of our feedback-based sensor fuzzing and demonstrate the feasibility of the discovered attacks through physical experiments.


## 15. It's Not Easy Being Green: On the Energy Efficiency of Programming Languages

**Authors:** Nicolas van Kempen (University of Massachusetts Amherst, USA), Hyuk-Je Kwon (University of Massachusetts Amherst), Dung Nguyen (University of Massachusetts Amherst), Emery D. Berger (University of Massachusetts Amherst and Amazon Web Services)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334459

**中文总结:** 直接检验「编程语言选择是否因果影响能耗」：修正并改进既有测量方法，建立区分语言/实现、应用实现、核心数与内存活动等因素的因果模型；控制这些变量后，先前研究中语言间显著能耗差异基本消失。

**Abstract:** Does the choice of programming language affect energy consumption? Previous highly visible studies have established associations between certain programming languages and energy consumption. A causal misinterpretation of this work has led academics and industry leaders to use or support certain languages based on their claimed impact on energy consumption. This paper tackles this causal question directly. It first corrects and improves the measurement methodology used by prior work. It then develops a detailed causal model capturing the complex relationship between programming language choice and energy consumption. This model identifies and incorporates several critical but previously overlooked factors that affect energy usage. These factors, such as distinguishing programming languages from their implementations, the impact of the application implementations themselves, the number of active cores, and memory activity, can significantly skew energy consumption measurements if not accounted for. We show—via empirical experiments, improved methodology, and careful examination of anomalies—that when these factors are controlled for, notable discrepancies in prior work vanish. Our analysis suggests that the choice of programming language implementation has no significant impact on energy consumption beyond execution time.


## 16. MIMIC: Integrating Diverse Personality Traits for Better Game Testing Using Large Language Model

**Authors:** Yifei Chen (McGill University), Sarra Habchi (Cohere, Canada), Lili Wei (McGill University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334487

**中文总结:** 提出 MIMIC，为 LLM 游戏测试 agent 注入多样人格特质以模拟不同玩家策略，提升测试覆盖与游戏内交互多样性；在 Minecraft 等游戏中任务完成率与解法多样性优于现有 RL/IL/LLM agent。

**Abstract:** Modern video games pose significant challenges for traditional automated testing algorithms, yet intensive testing is crucial to ensure game quality. To address these challenges, researchers designed gaming agents using Reinforcement Learning, Imitation Learning, or Large Language Models. However, these agents often neglect the diverse strategies employed by human players due to their different personalities, resulting in repetitive solutions in similar situations. Without mimicking varied gaming strategies, these agents struggle to trigger diverse in-game interactions or uncover edge cases.

In this paper, we present MIMIC, a novel framework that integrates diverse personality traits into gaming agents, enabling them to adopt different gaming strategies for similar situations. By mimicking different playstyles, MIMIC can achieve higher test coverage and richer in-game interactions across different games. It also outperforms state-of-the-art agents in Minecraft by achieving a higher task completion rate and providing more diverse solutions. These results highlight MIMIC’s significant potential for effective game testing.


## 17. NATE: A Network-Aware Testing Enhancer for Network-Related Fault Detection in Android Apps

**Authors:** Yuanhong Lan (Nanjing University), Shaoheng Cao (Nanjing University), Yifei Lu (State Key Laboratory for Novel Software Technology, Nanjing University, China), Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334452

**中文总结:** 首次系统研究 154 个 Android 网络相关缺陷（来自 42 款应用）的触发模式与成因，并据此提出 NATE：以好奇心驱动强化学习注入有效网络事件，增强现有 Android 测试以发现网络相关故障。

**Abstract:** Nowadays, Android apps are becoming much more network-dependent, with increasingly network-related faults being observed, severely undermining user experience. Given such faults scattered in modern apps and requiring complex network patterns to trigger, their detection is challenging. To date, we still lack a general and in-depth understanding of such faults. To fill this gap, we conduct the \textit{first} systematic study on 154 real-world network-related bugs filtered from 42 diverse representative Android apps to investigate their characteristics, influences, triggering patterns, and origins. Notable findings and implications have been revealed that shed light on further research on tackling such faults. While existing Android testing approaches struggle with detecting such faults due to a lack of effective network events and efficient injection, we propose NATE on the basis of our study, a network-aware testing enhancer to empower existing general Android testing approaches to detect network-related faults. Based on curiosity-driven reinforcement learning, NATE conducts network-aware guidance to inject effective network events, enabling testing approaches to explore network-related extra app functionalities and detect network-related faults. Based upon two state-of-the-art general Android testing approaches, experiments conducted on 12 large, active apps demonstrate the effectiveness and efficiency of NATE, with 1.7-5.7 times faults detected, 8.8% and 12.5% more code covered. Among the network-related faults detected by NATE, 20 have been explicitly confirmed as real-world bugs, with 6 of them already resolved. Notably, 15 of them were found by NATE for the first time, while none were detected by the original general testing approaches.


## 18. On the (In)Security of Non-resettable Device Identifiers in Custom Android Systems

**Authors:** Zikan Dong (Beijing University of Posts and Telecommunications), Liu Wang (Huazhong University of Science and Technology), Guoai Xu (Harbin Institute of Technology, Shenzhen), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334468

**中文总结:** 提出 IDRADAR，可扩展扫描定制 Android ROM 中通过系统属性/settings 等隐蔽通道暴露的不可重置设备标识；在 1814 个 ROM 中发现 3477 个属性与 1336 个 settings 缺乏访问控制，可被第三方 app 无权限追踪用户。

**Abstract:** User tracking is critical in the mobile ecosystem and relies on device identifiers to build user profiles. Early versions of Android allowed third-party apps to easily access non-resettable identifiers such as serial numbers and IMEI. As privacy concerns grew, Google has tightened identifier access in native Android. In response, stakeholders in custom Android systems introduced covert channels (e.g., system properties and settings) to maintain consistent and stable identifier access across systems and devices, which undoubtedly increases privacy risks. This paper examines the introduction of such channels through system customization and their vulnerability due to poor access control. We present IDRADAR, a scalable and accurate approach for identifying vulnerable properties and settings in custom Android systems. Applying our approach to 1,814 custom ROMs, we identified 8,192 system properties and 3,620 settings that store non-resettable device identifiers. Among these, 3,477 properties and 1,336 settings lack adequate access control and could be exploited by third-party apps to track users without permissions. Further validation on real devices demonstrates the effectiveness of our approach. Compared to state-of-the-art, IDRADAR offers improved scalability and analytical capabilities. Additionally, we investigate the root causes of the access control deficiencies and observe that such vulnerabilities frequently recur across devices from the same OEMs. We have reported our findings to the respective vendors and received positive confirmations. Our work underscores the need for greater scrutiny of covert access to device identifiers and better solutions to safeguard user privacy during system customizations.


## 19. On the Robustness Evaluation of 3D Obstacle Detection Against Specifications in Autonomous Driving

**Authors:** Tri Minh-Triet Pham (Concordia University), Bo Yang (Concordia University), Jinqiu Yang (Concordia University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334247

**中文总结:** 提出 SORBET，依据 LiDAR 规格与物体颜色/材质特性对点云施加规范扰动，测试自动驾驶 3D 障碍物检测鲁棒性；评估五种模型（含 Apollo L4）并分析检测偏差对规划决策的影响。

**Abstract:** Autonomous driving systems (ADSs) rely on real-time data from various sensors, including cameras and LiDAR, to make time-critical decisions using deep neural networks. The accuracy of these decisions is crucial for the widespread adoption of ADSs, as errors can have serious consequences. LiDAR-based detection, in particular, is sensitive to point cloud data (PCD) noises from various sources. However, the robustness of the current 3D detection against specification-based perturbations remains unevaluated. These perturbations are derived from the specification of LiDAR sensors and previous research on LiDAR’s ability to capture objects of different colors and materials. They can manifest as very subtle sensor-based noises or obstacle-specific perturbations. Hence, we propose SORBET, a framework that tests the robustness of 3D obstacle detection in ADS against such perturbations to the PCD to evaluate the robustness of LiDAR-based 3D obstacle detection. We applied SORBET to evaluate the robustness of five classic 3D obstacle detection models, including one from an industry-grade Level 4 ADS (Baidu’s Apollo). Furthermore, we studied how the deviated obstacle detection results would propagate and negatively impact trajectory prediction. Our evaluation emphasizes the importance of testing 3D obstacle detection against specification-based perturbations. We find that even very subtle changes in the PCD (i.e., removing two points) may introduce a non-trivial decrease in the detection performance. Furthermore, such a negative impact will further propagate to other modules, and endanger the safety of the ADS.


## 20. Profile Coverage: Using Android Compilation Profiles to Evaluate Dynamic Testing

**Authors:** Jakob Bleier (TU Wien), Felix Kehrer (TU Wien), Jürgen Cito (TU Wien), Martina Lindorfer (TU Wien)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334694

**中文总结:** 提出 profile coverage 指标，利用 Google Play 的 Cloud Profiles 衡量动态测试对真实用户常用方法的覆盖，并开发无需改 app 的轻量追踪器 ProfTrace；Top 1000 应用中 99.89% 含用法派生 cloud profile。

**Abstract:** The rising complexity of Android apps makes comprehensive dynamic testing infeasible, especially for third-party apps. Knowing which methods are exercised by real users typically requires costly user studies or access to usage telemetry. We show that Android’s compilation profiles,  specifically Cloud Profiles collected by the Google Play Store, offer a readily available, underutilized source of such information. These operational profiles aggregate which methods are commonly executed across users and guide ahead-of-time compilation during app installation. We provide the first in-depth characterization of Baseline Profiles and Cloud Profiles and show that over 99.89% of the top 1000 apps include usage-derived cloud profiles.

Based on this insight, we introduce profile coverage, a novel metric that measures how well dynamic testing exercises the methods real users interact with. This metric builds on the idea of operational coverage and enables a more holistic evaluation of automated test input generators. To enable profile coverage measurements, we develop a lightweight tracer, ProfTrace, based on Linux kernel uprobes that requires no app or system modifications. We demonstrate its utility by comparing three tools and a no-interaction baseline on 50 popular apps, showing that profile coverage reveals differences that traditional code coverage misses. For instance, in Candy Crush, automated testing achieves only 2.22% method coverage, but 21.39% profile coverage—indicating better alignment with user behavior than traditional code coverage would suggest.


## 21. VRExplorer: A Model-based Approach for Automated Virtual Reality Scene Testing

**Authors:** Zhu Zhengyang (Sun Yat-sen University), Hong-Ning Dai (Hong Kong Baptist University), Hanyang Guo (School of Software Engineering, Sun Yat-sen University), Zeqin Liao (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334628

**中文总结:** 提出 VRExplorer 模型驱动 VR 场景测试工具，以 Entity-Action-Task（EAT）框架建模交互，结合 NavMesh 路径规划与概率有限状态机系统探索并执行决策；在 11 个代表性 VR 应用上验证有效性与覆盖率。

**Abstract:** With the proliferation of Virtual Reality (VR) markets, VR applications are rapidly expanding in scale and complexity, thereby driving an urgent need for assuring VR software quality. Different from traditional mobile applications and computer software, VR testing faces unique challenges due to diverse interactions with virtual objects, complex 3D virtual environments, and intricate sequences to complete tasks. All of these emerging challenges hinder existing VR testing tools from effectively and systematically testing VR applications. In this paper, we present VRExplorer, a novel model-based testing tool to effectively interact with diverse virtual objects and explore complex VR scenes. Particularly, we design the Entity, Action, and Task (EAT) framework for modeling diverse VR interactions in a generic way. Built upon the EAT framework, we then present the VRExplorer agent, which can achieve effective scene exploration by incorporating meticulously designed path-finding algorithms into Unity’s NavMesh. Moreover, the VRExplorer agent can also systematically execute interaction decisions on top of the Probabilistic Finite State Machine (PFSM). Experimental evaluation on 11 representative VR projects shows that VRExplorer consistently outperforms the state-of-the-art (SOTA) approach VRGuide by achieving significantly higher coverage and better efficiency. Specifically, VRExplorer yields up to 122.8% and 52.8% improvements over VRGuide in terms of executable lines of code (ELOC) coverage and method (function) coverage, respectively. Furthermore, ablation results also verify the essential contributions of each designed module. More importantly, our VRExplorer has successfully detected two functional bugs and one non-functional bug from real-world projects.


## 22. VRTestSniffer: Test Smell Detector for Virtual Reality (VR) Software Projects

**Authors:** Faraz Gurramkonda (University of Michigan-Dearborn), Avishak Chakroborty (University of Michigan-Dearborn), Bruce Maxim (University of Michigan - Dearborn), Mohamed Wiem Mkaouer (University of Michigan - Flint), Foyzul Hassan (University of Michigan at Dearborn)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334364

**中文总结:** 提出 VRTestSniffer，面向 Unity VR 项目的静态 test smell 检测工具，扩展 tsDetect 共识别 17 类 VR 测试坏味；F1 达 95.61%，弥补 VR 测试上下文不足与 smell 覆盖有限的问题。

**Abstract:** Abstract—Virtual Reality (VR) is an emerging technology increasingly adopted in sectors such as gaming, education, border security, and industrial training. However, testing VR applications presents unique challenges due to factors like active user interaction, hardware dependencies, and immersive environments. Recent studies suggest that developers often write fewer test cases for VR applications, and these limited test cases frequently exhibit test smells. Current research on VR test smell detection can only identify a small subset of test smells and often lacks the necessary context for comprehensive detection. This highlights a critical gap in current testing practices for VR applications and underscores the need for approaches tailored to detecting and addressing quality issues in VR test cases. To address this research gap, we developed VRTestSniffer, a static analysis-based tool that extends test smell detection capabilities specifically for Unity-based VR applications. VRTestSniffer can detect 17 test smell categories, building upon those identified by the state-of-the-art tool tsDetect, and achieves an F1-score of 95.61%. It leverages abstract syntax trees (ASTs), control flow graphs (CFGs), and data flow graphs (DFGs) to enhance detection accuracy by capturing both control and data dependencies specific to VR testing patterns. In parallel, we conducted an empirical analysis of real-world VR projects to examine the prevalence and characteristics of these test smells. Our findings reveal that a few smelly test categories are linked to poorly structured or overly complex functional code. We believe that VRTestSniffer, along with the empirical insights derived from this study, can help VR developers write more effective, reliable, and maintainable test cases. To support further research and replication, our tool, dataset, and analysis results are publicly available at [1].


## 23. When Autonomous Vehicle Meets V2X Cooperative Perception: How Far Are We?

**Authors:** An Guo (Nanjing University), Shuoxiao Zhang (Nanjing University), Enyi Tang (Nanjing University), Xinyu Gao, Haomin Pang (Guangzhou University), Haoxiang Tian (Nanyang Technological University, Singapore), Yanzhou Mu, Wu Wen (Guangzhou University), Chunrong Fang (Nanjing University), Zhenyu Chen (Nanjing University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11338520

**中文总结:** 对 V2X 协同感知做首次系统实证，总结六种 prevalent 错误模式并评估传感器类型、融合方案与通信条件等组件对 ego 车辆感知的影响；为自动驾驶协同感知软件的质量保障提供实证基线。

**Abstract:** Perceiving the complex driving environment precisely is crucial to the safe operation of autonomous vehicles. With the tremendous advancement of deep learning and communication technology, Vehicle-to-Everything (V2X) cooperative perception has the potential to address limitations in sensing distant objects and occlusion for a single-agent perception system. V2X cooperative perception systems are software systems characterized by diverse sensor types and cooperative agents, varying fusion schemes, and operation under different communication conditions. Therefore, their complex composition gives rise to numerous operational challenges. Furthermore, when cooperative perception systems produce erroneous predictions, the types of errors and their underlying causes remain insufficiently explored.

To bridge this gap, we take an initial step by conducting an empirical study of V2X cooperative perception. To systematically evaluate the impact of cooperative perception on the ego vehicle’s perception performance, we identify and analyze six prevalent error patterns in cooperative perception systems. We further conduct a systematic evaluation of the critical components of these systems through our large-scale study and identify the following key findings: (1) The LiDAR-based cooperation configuration exhibits the highest perception performance; (2) Vehicle-to-infrastructure (V2I) and Vehicle-to-vehicle (V2V) communication exhibit distinct cooperative perception performance under different fusion schemes; (3) Increased cooperative perception errors may result in a higher frequency of driving violations; (4) Cooperative perception systems are not robust against communication interference when running online. Our results reveal operational vulnerabilities in critical components of cooperative perception systems. We hope that our findings can better promote the design and repair of cooperative perception systems.


## 24. Who's to Blame? Rethinking the Brittleness of Automated Web GUI Testing from a Pragmatic Perspective

**Authors:** Haonan Zhang (University of Waterloo), Kundi Yao (University of Waterloo), Zishuo Ding (The Hong Kong University of Science and Technology (Guangzhou)), Lizhi Liao (Memorial University of Newfoundland), Weiyi Shang (University of Waterloo)

**Categories:** Systems, Mobile, and UI

**PDF:** https://ieeexplore.ieee.org/document/11334505

**中文总结:** 经验论文剖析 Web GUI 自动化测试脆弱性根因：Mind2Web 遗留用例在当前版本大量失败，81.7% 修复用例六个月内再次破损；LLM 在类人诊断上下文下可修复相当比例 brittle 测试，但复杂场景仍需人工。

**Abstract:** Automated web GUI testing is important for software quality, however, its effectiveness is often undermined by test case brittleness, especially in continuously evolving real-world applications. In this experience paper, we pragmatically investigate the root causes of brittleness. We first analyze why legacy test cases, derived from the Mind2Web dataset, fail when executed on current web application versions. Our findings reveal that brittleness stems from multifaceted factors, including test script design, web application complexity, and automation framework limitations. A longitudinal study further shows that 81.7% of repaired tests break again within six months, primarily due to similar recurring issues, highlighting the persistent nature of brittleness. We further demonstrate that Large Language Models, when provided with human-like diagnostic context, can successfully repair a substantial portion of these brittle tests, though human expertise remains important for more complex scenarios. Our findings emphasize that brittleness is a multifaceted problem requiring collaboration between different parts involved in the automation testing.

