# ICSE 2025 Research Track — Systems, Mobile, and Autonomy

Source: https://conf.researchr.org/track/icse-2025/icse-2025-research-track

Total in this category: 15 papers

## 1. A Differential Testing Framework to Identify Critical AV Failures Leveraging Arbitrary Inputs

**Authors:** Trey Woodlief (University of Virginia), Carl Hildebrandt (University of Virginia), Sebastian Elbaum (University of Virginia)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029848

**中文总结:** 提出 DiffTest4AV 差分测试框架，利用开放数据集探索自动驾驶长尾输入并在缺乏显式预言机时识别关键失效。

**Abstract:** The proliferation of autonomous vehicles (AVs) has made their failures increasingly evident. Testing efforts aimed at identifying the inputs leading to those failures are challenged by the input's long-tail distribution, whose area under the curve is dominated by rare scenarios. We hypothesize that leveraging emerging open-access datasets can accelerate the exploration of long-tail inputs. Having access to diverse inputs, however, is not sufficient to expose failures; an effective test also requires an oracle to distinguish between correct and incorrect behaviors. Current datasets lack such oracles and developing them is notoriously difficult. In response, we propose DiffTest4AV, a differential testing framework designed to address the unique challenges of testing AV systems: 1) for any given input, many outputs may be considered acceptable, 2) the long-tail contains an insurmountable number of inputs to explore, and 3) the AV's continuous execution loop requires for failures to persist in order to affect the system. DiffTest4AV integrates statistical analysis to identify meaningful behavioral variations, judges their importance in terms of the severity of these differences, and incorporates sequential analysis to detect persistent errors indicative of potential system-level failures. Our study on 5 versions of the commercially-available, road-deployed comma.ai OpenPilot system, using 3 available image datasets, demonstrates the capabilities of the framework to detect high-severity, high-confidence, long-running test failures.

## 2. Automating a Complete Software Test Process Using LLMs: An Automotive Case Study

**Authors:** Shuai Wang, Yinan Yu (Chalmers University of Technology), Robert Feldt (Chalmers | University of Gothenburg), Dhasarathy Parthasarathy (Volvo Group)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029843

**中文总结:** 面向车载 API 测试，将流程拆分为子任务并交由 LLM 分步完成，在 100 余个 API 上验证可稳定自动化整车软件测试链路。

**Abstract:** Vehicle API testing verifies whether the interactions between a vehicle's internal systems and external applications meet expectations, ensuring that users can access and control various vehicle functions and data. However, this task is inherently complex, requiring the alignment and coordination of API systems, communication protocols, and even vehicle simulation systems to develop valid test cases. In practical industrial scenarios, inconsistencies, ambiguities, and interdependencies across various documents and system specifications pose significant challenges. This paper presents a system designed for the automated testing of in-vehicle APIs. By clearly defining and segmenting the testing process, we enable Large Language Models (LLMs) to focus on specific tasks, ensuring a stable and controlled testing workflow. Experiments conducted on over 100 APIs demonstrate that our system effectively automates vehicle API testing. The results also confirm that LLMs can efficiently handle mundane tasks requiring human judgment, making them suitable for complete automation in similar industrial contexts.

## 3. Decictor: Towards Evaluating the Robustness of Decision-Making in Autonomous Driving Systems

**Authors:** Mingfei Cheng (Singapore Management University), Xiaofei Xie (Singapore Management University), Yuan Zhou (Zhejiang Sci-Tech University), Junjie Wang (Tianjin University), Guozhu Meng (Institute of Information Engineering, Chinese Academy of Sciences), Kairui Yang (DAMO Academy, Alibaba Group, China)

**Categories:** Software Engineering for AI, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029758

**中文总结:** 提出 Decictor 评估自动驾驶路径规划决策鲁棒性，通过非侵入变异与一致性检查生成使系统做出非最优决策的测试场景。

**Abstract:** Autonomous Driving System (ADS) testing is crucial in ADS development, with the current primary focus being on safety. However, the evaluation of non-safety-critical performance, particularly the ADS’s ability to make optimal decisions and produce optimal paths for autonomous vehicles (AVs), is also vital to ensure the intelligence and reduce risks of AVs. Currently, there is little work dedicated to assessing the robustness of ADSs’ path-planning decisions (PPDs), i.e., whether an ADS can maintain the optimal PPD after an insignificant change in the environment. The key challenges include the lack of clear oracles for assessing PPD optimality and the difficulty in searching for scenarios that lead to non-optimal PPDs. To fill this gap, in this paper, we focus on evaluating the robustness of ADSs’ PPDs and propose the first method, Decictor, for generating non-optimal decision scenarios (NoDSs), where the ADS does not plan optimal paths for AVs. Decictor comprises three main components: Non-invasive Mutation, Consistency Check, and Feedback. To overcome the oracle challenge, Non-invasive Mutation is devised to implement conservative modifications, ensuring the preservation of the original optimal path in the mutated scenarios. Subsequently, the Consistency Check is applied to determine the presence of non-optimal PPDs by comparing the driving paths in the original and mutated scenarios. To deal with the challenge of large environment space, we design Feedback metrics that integrate spatial and temporal dimensions of the AV’s movement. These metrics are crucial for effectively steering the generation of NoDSs. Therefore, Decictor can generate NoDSs by generating new scenarios and then identifying NoDSs in the new scenarios. We evaluate Decictor on Baidu Apollo, an open-source and production-grade ADS. The experimental results validate the effectiveness of Decictor in detecting non-optimal PPDs of ADSs. It generates 63.9 NoDSs in total, while the best-performing baseline only detects 35.4 NoDSs.

## 4. Efficient Domain Augmentation for Autonomous Driving Testing Using Diffusion Models

**Authors:** Luciano Baresi (Politecnico di Milano), Davide Yi Xian Hu (Politecnico di Milano), Andrea Stocco (Technical University of Munich, fortiss), Paolo Tonella (USI Lugano)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029946

**中文总结:** 将扩散模型与物理仿真结合做自动驾驶 ODD 域增强，评估指令编辑、inpainting 等策略的有效性与开销，并验证合成场景对系统级泛化测试的价值。

**Abstract:** Simulation-based testing is widely used to assess the reliability of Autonomous Driving Systems (ADS), but its effectiveness is limited by the operational design domain (ODD) conditions available in such simulators. To address this limitation, in this work, we explore the integration of generative artificial intelligence techniques with physics-based simulators to enhance ADS system-level testing. Our study evaluates the effectiveness and computational overhead of three generative strategies based on diffusion models, namely instruction-editing, inpainting, and inpainting with refinement. Specifically, we assess these techniques' capabilities to produce augmented simulator-generated images of driving scenarios representing new ODDs. We employ a novel automated detector for invalid inputs based on semantic segmentation to ensure semantic preservation and realism of the neural generated images. We then perform system-level testing to evaluate the ADS's generalization ability to newly synthesized ODDs. Our findings show that diffusion models help increase the ODD coverage for system-level testing of ADS. Our automated semantic validator achieved a percentage of false positives as low as 3\%, retaining the correctness and quality of the generated images for testing. Our approach successfully identified new ADS system failures before real-world testing.

## 5. EP-Detector: Automatic Detection of Error-prone Operation Anomalies in Android Applications

**Authors:** Chenkai Guo (Nankai University, China), Qianlu Wang (College of Cyber Science, Nankai University), Naipeng Dong (The University of Queensland, Australia), Lingling Fan (Nankai University), Tianhong Wang (College of Computer Science, Nankai University), Weijie Zhang (College of Computer Science, Nankai University), EnBao Chen (College of Cyber Science, Nankai University), Zheli Liu (Nankai University), Lu Yu (National University of Defense Technology; Anhui Province Key Laboratory of Cyberspace Security Situation Awareness and Evaluation)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029849

**中文总结:** 首次系统刻画 Android 易误操作异常（EPA），从主体、客体与环境三维度归因，并提出动态 GUI 测试工具 EP-Detector 自动检测。

**Abstract:** Android applications are pervasively adopted and heavily relied on in our daily life, leading to the growing demand for enhanced user experiences, such as ease for operation and robustness. Nevertheless, developers continue to prioritize traditional functionality and performance, overlooking the pivotal role of user experience in real-world scenarios. For example, poorly designed page elements can lead to user confusion, resulting in unexpected outcomes, termed as the error-prone operation anomalies (EPAs). In this work, we undertake the first effort to uncover the underlying essence of the EPA problem. To achieve this objective, we investigated the root causes of EPAs from three dimensions, i.e., subject, object and environment. These causes were identified by multi-stage attribute capturing and precise similarity computation. In this process, the causes are categorized into fine-grained classes, namely confusing behaviours, unsuitable layout, and resource overload. Building upon these insights, we propose a dynamic GUI-based testing tool EP-Detector to facilitate detecting the EPAs in real-world apps. The EP-Detector is equipped with widget-exploration based target navigation and automatic test oracle, enabling it to detect error-prone page elements and simulate events with both comprehensiveness and precision. To systematically study the prevalence and severity of real-world EPAs, we conducted experiments on 53 popular Android apps with EP-Detector. The confirmed results not only validate the high precision and completeness of EP-Detector but also highlight that EPAs are prevalent in current apps, with at least one EPA existing in every two page widgets on average, and 28.3% of them may lead to security and functionality issues or risks. The EP-Detector is available at https://github.com/WordDealer/EP-Detector.

## 6. FixDrive: Automatically Repairing Autonomous Vehicle Driving Behaviour for $0.08 per Violation

**Authors:** Yang Sun (Singapore Management University), Chris Poskitt (Singapore Management University), Kun Wang (Zhejiang University), Jun Sun (Singapore Management University)

**Categories:** Software Engineering for AI, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029921

**中文总结:** 提出 FixDrive，分析近失或违规驾驶记录，用 μDrive 领域语言生成可泛化、可解释的自动驾驶策略修复，单次违规修复成本约 0.08 美元。

**Abstract:** Autonomous Vehicles (AVs) are advancing rapidly, with Level-4 AVs already operating in real-world conditions. Current AVs, however, still lag behind human drivers in adaptability and performance, often exhibiting overly conservative behaviours and occasionally violating traffic laws. Existing solutions, such as runtime enforcement, mitigate this by automatically repairing the AV's planned trajectory at runtime, but such approaches lack transparency and should be a measure of last resort. It would be preferable for AV repairs to generalise beyond specific incidents and to be interpretable for users. In this work, we propose FixDrive, a framework that analyses driving records from near-misses or law violations to generate AV driving strategy repairs that reduce the chance of such incidents occurring again. These repairs are captured in $\mu$Drive, a high-level domain-specific language for specifying driving behaviours according to event-based triggers. Implemented for the state-of-the-art autonomous driving system Apollo, FixDrive identifies and visualises critical moments from driving records, then uses a Multimodal Large Language Model (MLLM) with zero-shot learning to generate $\mu$Drive programs. We tested FixDrive on various benchmark scenarios, and found that the generated repairs improved the AV's performance with respect to following traffic laws, avoiding collisions, and successfully reaching destinations. Furthermore, the direct costs of repairing an AV---15 minutes of offline analysis and \$0.08 per violation---are reasonable in practice.

## 7. GARL: Genetic Algorithm-Augmented Reinforcement Learning to Detect Violations in Marker-Based Autonomous Landing Systems

**Authors:** Linfeng Liang (Macquarie University), Yao Deng (Macquarie University), Kye Morton (Skyy Network), Valtteri Kallinen (Skyy Network), Alice James (Macquarie University), Avishkar Seth (Macquarie University), Endrowednes Kuantama (Macquarie University), Subhas Mukhopadhyay (Macquarie University), Richard Han (Macquarie University), Xi Zheng (Macquarie University)

**Categories:** AI for Software Engineering, Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029873

**中文总结:** 提出 GARL 框架，将遗传算法与强化学习结合高效生成无人机自主着陆系统违规场景，性能较现有方法最高提升 18.35%。

**Abstract:** Automated Uncrewed Aerial Vehicle (UAV) landing is crucial for autonomous UAV services such as monitoring, surveying, and package delivery. It involves detecting landing targets, perceiving obstacles, planning collision-free paths, and controlling UAV movements for safe landing. Failures can lead to significant losses, necessitating rigorous simulation-based testing for safety. Traditional offline testing methods, limited to static environments and predefined trajectories, may miss violation cases caused by dynamic objects like people and animals. Conversely, online testing methods require extensive training time, which is impractical with limited budgets. To address these issues, we introduce GARL, a framework combining a genetic algorithm (GA) and reinforcement learning (RL) for efficient generation of diverse and real landing system failures within a practical budget. GARL employs GA for exploring various environment setups offline, reducing the complexity of RL's online testing in simulating challenging landing scenarios. Our approach outperforms existing methods by up to 18.35% in violation rate and 58% in diversity metric. We validate most discovered violation types with real-world UAV tests, pioneering the integration of offline and online testing strategies for autonomous systems. This method opens new research directions for online testing, with our code available at https://anonymous.4open.science/r/drone_testing-5CF0/.

## 8. Janus: Detecting Rendering Bugs in Web Browsers via Visual Delta Consistency

**Authors:** Chijin Zhou (Tsinghua University), Quan Zhang (Tsinghua University), Bingzhou Qian (National University of Defense Technology), Yu Jiang (Tsinghua University)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029880

**中文总结:** 提出视觉增量一致性测试准则，并实现浏览器渲染模糊测试器 Janus；通过对比轻微修改 HTML 后各浏览器渲染变化是否一致来发现渲染缺陷。

**Abstract:** Rendering lies at the heart of our modern web experience. However, the correctness of browser rendering is not always guaranteed, often leading to rendering bugs. Traditional differential testing, while successful in various domains, falls short when applied to rendering bug detection because an HTML file is likely yield different rendered outcomes across different browsers. This paper introduces Visual Delta Consistency, a test oracle to detect rendering bugs in web browsers, aiming to make rendered pages across browsers comparable. Our key insight is that any modifications made to an HTML file should uniformly influence rendering outcomes across browsers. Specifically, when presented with two HTML files that differ only by minor modifications, the reaction of all browsers should be consistent, i.e., either all browsers render them identically or all render them differently. Based on this insight, We implemented it as a practical fuzzer named Janus. It constructs pairs of slightly modified HTML files and observes the change statuses of the corresponding rendered pages across browsers for bug detection. We evaluated it on three widely-used browsers, i.e., Chrome, Safari, and Firefox. In total, Janus detected 34 rendering bugs, out of which 26 confirmed with 8 fixed by the developers.

## 9. LLM-Agents Driven Automated Simulation Testing and Analysis of small Uncrewed Aerial Systems

**Authors:** Venkata Sai Aswath Duvvuru (Saint Louis University), Bohan Zhang (Saint Louis University, Missouri), Michael Vierhauser (University of Innsbruck), Ankit Agrawal (Saint Louis University, Missouri)

**Categories:** AI for Software Engineering, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029890

**中文总结:** 提出 AUTOSIMTEST，由多 LLM 智能体协作完成小型无人机仿真测试的场景设计、环境搭建、任务规划与结果分析，减轻人工端到端测试负担。

**Abstract:** Thorough simulation testing is crucial for validating the correct behavior of small Uncrewed Aerial Systems (sUAS) across multiple scenarios, including adverse weather conditions (such as wind, and fog), diverse settings (hilly terrain, or urban areas), and varying mission profiles (surveillance, tracking). While various sUAS simulation tools exist to support developers, the entire process of creating, executing, and analyzing simulation tests remains a largely manual and cumbersome task. Developers must identify test scenarios, set up the simulation environment, integrate the System under Test (SuT) with simulation tools, formulate mission plans, and collect and analyze results. These labor-intensive tasks limit the ability of developers to conduct exhaustive testing across a wide range of scenarios. To alleviate this problem, in this paper, we propose AUTOSIMTEST, a Large Language Model (LLM)-driven framework, where multiple LLM agents collaborate to support the sUAS simulation testing process. This includes: (1) creating test scenarios that subject the SuT to unique environmental contexts; (2) preparing the simulation environment as per the test scenario; (3) generating diverse sUAS missions for the SuT to execute; and (4) automatically analyzing simulation results and providing an interactive analytics interface. Further, the design of the framework is flexible for creating and testing scenarios for a variety of sUAS use cases, simulation tools, and SuT input requirements. We evaluated our approach by (a) conducting simulation testing of PX4 and ArduPilot flight-controller-based SuTs, (b) analyzing the performance of each agent, and (c) gathering feedback from sUAS developers. Our findings indicate that AUTOSIMTEST significantly improves the efficiency and scope of the sUAS testing process, allowing for more comprehensive and varied scenario evaluations while reducing the manual effort.

## 10. MARQ: Engineering Mission-Critical AI-based Software with Automated Result Quality Adaptation

**Authors:** Uwe Gropengießer (Technical University of Darmstadt), Elias Dietz (Technical University of Darmstadt), Florian Brandherm (Technical University of Darmstadt), Achref Doula (Technical University of Darmstadt), Osama Abboud (Munich Research Center, Huawei), Xun Xiao (Munich Research Center, Huawei), Max Mühlhäuser (Technical University of Darmstadt)

**Categories:** Software Engineering for AI, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029961

**中文总结:** 提出 MARQ 框架，支持工程师声明不同结果质量与资源需求的 AI 服务链，并在运行时根据资源约束自动优化切换，适用于边缘与移动等场景。

**Abstract:** AI-based mission-critical software exposes a blessing and a curse: its inherent statistical nature allows for flexibility in result quality, yet the mission-critical importance demands adherence to stringent constraints such as execution deadlines. This creates a space for trade-offs between the Quality of Result (QoR)—a metric that quantifies the quality of a computational outcome—and other application attributes like execution time and energy, particularly in real-time scenarios. Fluctuating resource constraints, such as data transfer to a remote server over unstable network connections, are prevalent in mobile and edge computing environments—encompassing use cases like Vehicle-to-Everything, drone swarms, or social-VR scenarios. We introduce a novel approach that enables software engineers to easily specify alternative AI service chains—sequences of AI services encapsulated in microservices aiming to achieve a predefined goal—with varying QoR and resource requirements. Our methodology facilitates dynamic optimization at runtime, which is automatically driven by the MARQ framework. Our evaluations show that MARQ can be used effectively for the dynamic selection of AI service chains in real-time while maintaining the required application constraints of mission-critical AI software. Notably, our approach achieves a 100x acceleration in service chain selection and an average 10% improvement in QoR compared to existing methods.

## 11. Mobile Application Coverage: The 30% Curse and Ways Forward

**Authors:** Faridah Akinotcho (University of British Columbia, Canada), Lili Wei (McGill University), Julia Rubin (The University of British Columbia)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**Artifact badges:** Artifact-Available

**PDF:** https://ieeexplore.ieee.org/document/11029955

**中文总结:** 通过两位专家深入探索 103 个 Android 应用的大规模实验，揭示 GUI 驱动测试约 30% 覆盖率上限的根因：设备配置与外部资源依赖使即便人工也难以覆盖剩余 70% 代码。

**Abstract:** Testing, security analysis, and other dynamic quality assurance approaches rely on mechanisms that invoke software under test, aiming to achieve high code coverage. A large number of invocation mechanisms proposed in the literature, in particular for Android mobile applications, employ GUI-driven application exploration. However, studies show that even the most advanced GUI exploration techniques can cover only around 30% of a real- world application. This paper aims to investigate “the remaining 70%”. By conducting a large-scale experiment involving two human experts, who thoroughly explored 61 benchmark and 42 popular apps from Google Play, we show that achieving a substantially larger coverage for real-world applications is impractical even if we factor out known GUI-based exploration issues, such as the inability to provide semantic inputs and the right order of events. The main reasons preventing humans from covering the entire application include application dependencies on device configurations and external resources. Thus, future investment into GUI-based exploration strategies is unlikely to lead to substantial improvements in coverage. To chart possible ways forward and explore approaches to satisfy/bypass these dependencies, we thoroughly analyze code-level properties guarding them. Our analysis shows that a large fraction of the dependencies could actually be successfully bypassed with relatively simple beyond- GUI exploration techniques. We hope our study can inspire future work in this area and also provide a realistic benchmark for evaluating this work.

## 12. PacDroid: A Pointer-Analysis-Centric Framework for Security Vulnerabilities in Android Apps

**Authors:** Menglong Chen (Nanjing University), Tian Tan (Nanjing University), Minxue Pan (Nanjing University), Yue Li (Nanjing University)

**Categories:** Security and Vulnerability, Systems, Mobile, and Autonomy

**Awards:** Best Artifact, Award Winner

**Artifact badges:** Artifact-Functional, Artifact-Available, Artifact-Reusable

**PDF:** https://ieeexplore.ieee.org/document/11029859

**中文总结:** 提出以指针分析为核心的 Android 静态分析框架 PacDroid，统一处理别名、过程间传播与 ICC 等特性，在精度、速度与鲁棒性上优于 FlowDroid 等主流框架。

**Abstract:** General frameworks such as FlowDroid, IccTA, P/Taint, Amandroid, and DroidSafe have significantly advanced the development of static analysis tools for Android security by providing fundamental facilities for them. However, while these frameworks have been instrumental in fostering progress, they often operate with inherent inefficiencies, such as redundant computations, reliance on separate tools, and unnecessary complexity, which are rarely scrutinized by the analysis tools that depend on them. This paper introduces PacDroid, a new static analysis framework for detecting security vulnerabilities in Android apps. PacDroid employs a simple yet effective pointer-analysis-centric approach that naturally manages alias information, interprocedural value propagation, and all Android features it supports (including ICC, lifecycles, and miscs), in a unified manner. Our extensive evaluation reveals that PacDroid not only outperforms state-of-the-art frameworks in achieving a superior trade-off between soundness and precision (F-measure) but also surpasses them in both analysis speed and robustness; moreover, PacDroid successfully identifies 77 real security vulnerability flows across 23 real-world Android apps that were missed by all other frameworks. With its ease of extension and provision of essential facilities, PacDroid is expected to serve as a foundational framework for various future analysis applications for Android.

## 13. Scenario-Driven and Context-Aware Automated Accessibility Testing for Android Apps

**Authors:** Yuxin Zhang (Tianjin University), Sen Chen (Nankai University), Xiaofei Xie (Singapore Management University), Zibo Liu (College of Intelligence and Computing, Tianjin University), Lingling Fan (Nankai University)

**Categories:** Testing and Quality, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029746

**中文总结:** 提出 A11yScan，以场景驱动 UI 探索提升 Android 无障碍测试覆盖率，并以运行时上下文感知检测降低误报与漏报。

**Abstract:** Mobile accessibility is increasingly important nowadays as it enables people with disabilities to use mobile applications to perform daily tasks. Ensuring mobile accessibility not only benefits those with disabilities but also enhances the user experience for all users, making applications more intuitive and user-friendly. Although numerous tools are available for testing and detecting accessibility issues in Android applications, a large number of false negatives and false positives persist due to limitations in the existing approaches, i.e., low coverage of UI scenarios and lack of consideration of runtime context. To address these problems, in this paper, we propose a scenario-driven exploration method for improving the coverage of UI scenarios, thereby detecting accessibility issues within the application, and ultimately reducing false negatives. Furthermore, to reduce false positives caused by not considering the runtime context, we propose a context-aware detection method that provides a more fine-grained detection capability. Our experimental results reveal that A11yScan can detect 1.7X more issues surpassing current state-of-the-art approaches like Xbot (3,991 vs. 2,321), thereby reducing the false negative rate by 41.84\%. Additionally, it outperforms established UI exploration techniques such as SceneDroid (952 vs. 661 UI scenarios), while achieving comparable activity coverage to recent leading GUI testing tools like GPTDroid on the available dataset (73\% vs. 71\%). Meanwhile, with the context-aware detection method, A11yScan effectively reduces the false positive rate by 21\%, validated with a 90.56\% accuracy rate through a user study.

## 14. TacDroid: Detection of Illicit Apps through Hybrid Analysis of UI-based Transition Graphs

**Authors:** Yanchen Lu (Zhejiang University), Hongyu Lin (Zhejiang University), Zehua He (Zhejiang University), Haitao Xu (Zhejiang University), Zhao Li (Hangzhou Yugu Technology), Shuai Hao (Old Dominion University), Liu Wang (Beijing University of Posts and Telecommunications), Haoyu Wang (Huazhong University of Science and Technology), Kui Ren (Zhejiang University)

**Categories:** Program Analysis and Verification, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029913

**中文总结:** 提出 TacDroid，融合动态与静态分析构建 UI 转移图，检测依赖动态资源加载的非法应用（色情、赌博、诈骗等）。

**Abstract:** Illicit apps have emerged as a thriving underground industry, driven by their substantial profitability. These apps either offer users restricted services (e.g., porn and gambling) or engage in fraudulent activities like scams. Despite the widespread presence of illicit apps, scant attention has been directed towards this issue, with several existing detection methods predominantly relying on static analysis alone. However, given the burgeoning trend wherein an increasing number of mobile apps achieve their core functionality through dynamic resource loading, depending solely on static analysis proves inadequate. To address this challenge, in this paper, we introduce TacDroid, a novel approach that integrates dynamic analysis for dynamic content retrieval with static analysis to mitigate the limitations inherent in both methods, i.e., the low coverage of dynamic analysis and the low accuracy of static analysis. Specifically, TacDroid conducts both dynamic and static analyses on an Android app to construct dynamic and static User Interface Transition Graphs (UTGs), respectively. These two UTGs are then correlated to create an intermediate UTG. Subsequently, TacDroid embeds graph structure and utilizes an enhanced Graph Autoencoder (GAE) model to predict transitions between nodes. Through link prediction, TacDroid effectively eliminates false positive transition edges stemming from misjudgments in static analysis and supplements false negative transition edges overlooked in the intermediate UTG, thereby generating a comprehensive and accurate UTG. Finally, TacDroid determines the legitimacy of an app and identifies its category based on the app's UTG. Our evaluation results highlight the outstanding accuracy of TacDroid in detecting illicit apps. It significantly surpasses the state-of-the-art work, achieving an F1-score of 96.73%. This work represents a notable advancement in the identification and categorization of illicit apps.

## 15. The Design Smells Breaking the Boundary between Android Variants and AOSP

**Authors:** Wuxia Jin (Xi'an Jiaotong University), Jiaowei Shang (Xi'an Jiaotong University), Jianguo Zheng (Xi'an Jiaotong University), Mengjie Sun (Xi’an Jiaotong University), Zhenyu Huang (Honor Device Co., Ltd.), Ming Fan (Xi'an Jiaotong University), Ting Liu (Xi'an Jiaotong University)

**Categories:** Evolution and Maintenance, Architecture and Design, Systems, Mobile, and Autonomy

**PDF:** https://ieeexplore.ieee.org/document/11029784

**中文总结:** 刻画破坏 Android 定制版与 AOSP 设计边界的反复设计坏味道，提出 DroidDS 自动检测并验证其与高维护成本相关。

**Abstract:** Phone vendors customize their Android variants to enhance system functionalities based on the Android Open Source Project (AOSP). While independent development, Android variants have to periodically evolve with the upstream AOSP and merge code changes from AOSP. Vendors have invested great effort to maintain their variants and resolve merging conflicts. In this paper, we characterize the design smells with recurring patterns that break the design boundary between Android variants and AOSP. These smells are manifested as problematic dependencies across the boundary, hindering Android variants' maintainability and co-evolution with AOSP. We propose the DroidDS for automatically detecting design smells. We collect 22 Android variant versions and 22 corresponding AOSP versions, involving 4 open-source projects and 1 industrial project. Our results demonstrate that: files involved in design smells consume higher maintenance costs than other files; these infected files are not merely the files with large code size, increased complexity, and object-oriented smells; the infected files have been involved in more than half of code conflicts induced by re-applying AOSP's changes to Android variants; a substantial portion of design issues could be mitigable. Practitioners can utilize our DroidDS to pinpoint and prioritize design problems for Android variants. Refactoring these problems will help keep a healthy coupling between diverse variants and AOSP, potentially improving maintainability and reducing conflict risks.
