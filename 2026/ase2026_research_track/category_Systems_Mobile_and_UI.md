# ASE 2026 Research Track — Systems, Mobile, and UI

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 7

## 1. Assessing Uncertainty in Performance Modeling: Conformal Prediction vs. Bayesian Regression

**Authors:** Stefan Jahns (Leipzig University, Germany), Johannes Dorn (Leipzig University, Germany), Max Weber (Leipzig University, Germany), Sven Apel (Saarland University, Germany), Norbert Siegmund (ScaDS.AI, Germany / Leipzig University, Germany)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837425

**中文总结:** 比较四种 conformal prediction 与 Bayesian 标准 P4 在可配置系统性能预测中的不确定性量化；conformal 在 8 个真实场景中 6 个优于 SOTA，置信区间窄 46%–75%，且可 plug-and-play 增强现有点估计模型。

**Abstract:** Most software systems today are configurable. As a consequence, predicting performance is inherently challenging due to the sheer number of configurations exhibiting individual performance variations. When predicting the performance of unseen configurations, it is imperative to know how reliable such predictions are. Bayesian methods have been shown to be able to quantify the uncertainty in their estimates, but require prior information about performance distributions and, more importantly, are constrained in their learning technique, effectively limiting their practical applicability. Conformal prediction, an entirely novel approach to uncertainty quantification in this area, augments existing learning algorithms via a statistical post-hoc analysis. This allows us to provide uncertainty estimates even for point-estimate algorithms, such as random forests or deep neural networks. The goal of this study is to evaluate how assumptions of conformal predictions regarding sample size and distribution, as well as the heterogeneity of learning algorithms, affect their applicability to software performance prediction. We conduct a comprehensive study comparing four conformal prediction variants against P4, the current standard for uncertainty-aware performance prediction, analyzing accuracy, scalability, and uncertainty quantification. Our results show that conformal prediction consistently outperforms the state of the art across six out of eight real world scenarios, producing correct confidence intervals that are 46–75 % narrower, and thus more certain. Notably, conformal prediction can be used to enrich existing techniques, with post-hoc uncertainty quantification in a plug and play fashion.


## 2. Discovering Performance Archetypes: Critical-Path-Aware Pattern Analysis and Regression Detection

**Authors:** Kaveh Shahedi (Polytechnique Montréal, Canada), Heng Li (Polytechnique Montréal, Canada), Maxime Lamothe (Polytechnique Montréal, Canada), Foutse Khomh (Polytechnique Montréal, Canada)

**Categories:** Systems, Mobile, and UI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834426

**中文总结:** 提出关键路径感知的性能 archetype 方法，融合静态特征、动态 trace 与内核资源数据；在 6 个 C/C++ 应用上发现 13 类跨域性能模式，并用于回归检测 F1 0.867，较仅用资源信号提升 60.4%。

**Abstract:** Software performance analysis and prediction requires integrating multiple signals, as code structure alone cannot capture runtime behavior shaped by execution frequency, resource contention, and I/O patterns. We present a critical-path-aware performance analysis methodology that automatically discovers recurring performance patterns by synthesizing static code features, dynamic execution traces, and kernel-level resource data. In a preliminary study across six real-world C/C++ applications (SQLite, OpenSSL, Zstandard, FFmpeg, cURL, and jq), we first empirically confirm that static complexity metrics explain only 10.4% of the variance (ρ 2 ) in critical path execution time, quantifying a gap that, while theoretically expected, had not been measured systematically across applications. Motivated by this finding, we analyze nearly 80,000 critical execution paths and address two research questions. First, we discover 13 distinct performance archetypes : recurring behavioral patterns that appear consistently across different applications, independent of their domain or implementation. Five of these patterns are near-universal and appear in at least five of the six applications studied. Notably, three of these archetypes are present in all six applications, and together, these common patterns account for 56.4% of all observed paths. Each archetype maps to specific resource profiles and optimization strategies that transfer across domains. Second, we leverage these archetypes within a multi-signal regression detection framework that triangulates path structure, resource consumption, and archetype deviations, achieving an F1-score of 0.867 and a 60.4% improvement over resource-only methods.


## 3. Less Is More: Tuning Configurable Systems with Imperfect Fidelity

**Authors:** Yulong Ye (University of Birmingham, UK), Miqing Li (University of Birmingham, UK), Tao Chen (University of Birmingham, UK)

**Categories:** Systems, Mobile, and UI

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifacts Available, Artifacts Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834376

**中文总结:** 提出可配置系统 fidelity 概念与 MFTune：在廉价 imperfect-fidelity 环境广泛探索再深度 tune perfect-fidelity；相对 10 种 SOTA 调参器在 83.33% 场景更优（最高 +19.34%），并节省大量测量预算（19 个月 24×7 实验）。

**Abstract:** Configuration tuning is essential for optimizing the performance of highly configurable systems, e.g., throughput or runtime, under a given environment. Yet, this is a challenging process as there can be many options to tune, and configuration measurement is often highly expensive. In this paper, we demonstrate the phenomenon of “less can be more”: system configuration tuning can be greatly improved with much superior budget utilization by partially tuning under the imperfect-fidelity—an environment that is similar, but cheaper to measure, compared with the concerned perfect-fidelity of environment under which the system should be tuned. We codify a conceptual framework of fidelity for configurable systems, drawing on which allows us to propose MFTune, a tuner that proactively explores in the space of >10 4 possible imperfect-fidelity settings to approximate a useful one, which strikes for the wideness of tuning. This creates high-quality seeds for the perfect-fidelity, which in turn ensures the tuning depth. Experiment results against 10 state-of-the-art tuners, obtained from running diverse real-world systems for 19 months 24 × 7, show that MFTune performs considerably better on 83.33% cases with up to 19.34% improvement while achieving hours of budget saving in general.


## 4. Panorama: Unveiling Latent Dependencies for Microservice Autoscaling via Meta-learning

**Authors:** Zhuangbin Chen (Sun Yat-sen University, China), Hongjiang Feng (Sun Yat-sen University, China), Yang Liu (Sun Yat-sen University, China), Juzheng Zheng (Sun Yat-sen University, China), Xiaoyu He (Sun Yat-sen University, China), Zibin Zheng (Sun Yat-sen University, China)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837485

**中文总结:** 提出 Panorama，显式建模资源干扰（RID）与执行阻塞（EBD）等 latent 依赖，并用混合注意力+元学习快速适应负载变化；在四套微服务基准上较 SOTA 最多降 68% 资源消耗、响应时间改善 42%。

**Abstract:** Existing autoscaling approaches primarily leverage direct service calls to model the propagation effects of scaling decisions across inter-service dependencies. However, the intricate and implicit service interactions (i.e., latent dependencies) often go beyond such direct invocations, rendering suboptimal scaling actions and poor adaptability. To address these limitations, we propose Panorama, a novel autoscaling framework that explicitly unveils and exploits indirect service interactions. In particular, we formalize two fundamental categories of latent dependencies, i.e., resource interference dependencies (RIDs), which emerge from shared infrastructure resources, and execution blocking dependencies (EBDs), which stem from temporal constraints in the execution logic of business workflows. Panorama employs a hybrid attention mechanism to model these multifaceted service dependencies alongside temporal dynamics. We also design a meta-learning paradigm to enable rapid adaptation to evolving workload patterns and dependency structures without extensive retraining. Evaluation across four representative microservice benchmarks shows that Panorama consistently outperforms state-of-the-art baselines, achieving up to 68% reduction in resource consumption while improving response time by 42%. This highlights the critical importance of explicitly modeling latent dependencies for effective microservice resource management.


## 5. Smart Brain: Semantic Anomaly Detection for Operational Time Series in Large Scale Service Systems

**Authors:** Hang Cui (University of Chinese Academy of Sciences, China / Computer Network Information Center at Chinese Academy of Sciences, China), Zexin Wang (Computer Network Information Center at Chinese Academy of Sciences, China), Jingjing Li (Computer Network Information Center at Chinese Academy of Sciences, China), Juncheng Hu (Jilin University, China), Haotian Si (Independent Researcher, China), Cenjie Hu (Shenyang Institute of Automation at Chinese Academy of Sciences, China), Quan Zhou (Beijing Academy of Science and Technology, China), Yongchang Hu (Huawei Technologies, China), Lei Han (Huawei Technologies, China), Dan Pei (Tsinghua University, China), Changhua Pei (Computer Network Information Center at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Gaogang Xie (Computer Network Information Center at Chinese Academy of Sciences, China)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837436

**中文总结:** 提出 Smart Brain 两阶段语义异常检测：先抽取可解释时序异常模式证据，再结合指标语义与运维规则给出可行动决策与自然语言解释；在基准与工业监控场景上较分数流水线更贴合运维语义且可解释性更强。

**Abstract:** Time series anomaly detection is a core component of operational automation in large scale service systems. However, most existing methods model anomalies as numerical deviations in the data space, while real software operations require decisions over whether an observed behavior constitutes an actionable abnormal event. This mismatch often leads to brittle thresholds, excessive false alerts, and outputs that are difficult for operators to interpret and act upon. In this paper, we argue that practical anomaly detection should move from point-centric data anomaly detection to semantic anomaly detection. We present Smart Brain, a two stage framework for semantic anomaly detection in operational time series. Stage I extracts structured temporal evidence by recognizing interpretable anomaly patterns. Stage II combines the extracted evidence with metric semantics and operator authored rules to produce semantic anomaly decisions and human-readable explanations. Through evaluation on benchmark datasets and real industrial monitoring scenarios, we show that Smart Brain improves operationally meaningful anomaly identification while providing stronger interpretability and deployment suitability than score centric pipelines. Beyond the framework itself, our study offers practical lessons for building anomaly detection systems in production software environments, highlighting the importance of semantic grounding, structured evidence, and lightweight adaptation to evolving services.


## 6. Source-Free Detection and Impact Analysis of Compiler Optimization Problems in Mobile Applications

**Authors:** Han Hu (Independent Researcher, Hong Kong), Xiaoheng Xie (Independent Researcher, Hong Kong), Bo Sun (Huawei, China), Jian Gu (Monash University, Australia), Gang Fan (Independent Researcher, Hong Kong), Li Li (Beihang University, China)

**Categories:** Systems, Mobile, and UI

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834340

**中文总结:** 提出 OptDetect 无源码从 APK 原生库检测低优化级别（O0/O1）片段；830 个 Google Play 头部应用中 91.7% 受影响，修复案例 CPU 指令中位降 20.5%–32%，并揭示第三方库大量以低优化分发。

**Abstract:** Mobile apps frequently suffer from frame drops, overheating, and excessive power consumption. While developers optimize algorithms and debug code, a critical bottleneck often goes unnoticed: native libraries compiled with low optimization levels (O0/O1 instead of O2/O3). Because these libraries execute without functional errors, the resulting performance degradation remains hidden in production apps. We present OptDetect, a source-free framework that detects compiler optimization problems directly from app binaries. OptDetect handles mixed optimization levels through binary disassembly, chunk-level classification, and weighted score aggregation, achieving 93.0% accuracy on controlled datasets and 81.9% on real-world datasets. Applying OptDetect to 21,972 native libraries from 830 top-ranked Google Play apps, we find that 30.5% of libraries use low optimization levels, affecting 91.7% of apps. Through case studies on 12 production apps, fixing detected issues reduces CPU instructions by 10-63% (median: 20.5%) for commercial apps and 15-58% (median: 32%) for open-source apps. Performance complaints decrease in 5 of 6 commercial apps, and ratings increase in 5 of 6. Further investigation reveals that widely-used third-party libraries are themselves distributed at low optimization levels, with 49.7% of 1,073 libraries in a major repository exhibiting this problem. These findings show that compiler optimization problems are common, source-free detectable, and practically consequential in mobile app ecosystems.


## 7. Tracing the Invisible: Semantic Message Flow Discovery via Data Contracts in Real-World Distributed Systems

**Authors:** Youlong Chen (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China / Zhongguancun Laboratory, China), Jie Lu (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Mingtao Huang (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Chenghang Shi (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Yongheng Huang (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Haofeng Li (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China), Dong Liu (Zhongguancun Laboratory, China), Mengna Ma (Zhongguancun Laboratory, China), Yong Liu (Zhongguancun Laboratory, China / Qi An Xin Technology Group, China), Qinfen Hao (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China / Zhongguancun Laboratory, China), Lian Li (Institute of Computing Technology at Chinese Academy of Sciences, China / University of Chinese Academy of Sciences, China / Zhongguancun Laboratory, China)

**Categories:** Systems, Mobile, and UI

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834372

**中文总结:** 提出 Hermes，以消息类型为语义契约，用 LLM 合成路由逻辑并精确发现从发送 API 到 handler 的消息流；在 10 个真实系统上达 88.6% 精度与 99.6% 召回，安全审计发现 121 条污点路径并确认 56 个零日（53 已修复、7 获 CVE）。

**Abstract:** Distributed systems rely on complex messaging middleware, posing significant challenges for static analysis tools. Existing approaches often require manually specifying communication patterns between message senders and handlers—a process that is tedious, error-prone, and ill-suited to capture the semantic complexity of real-world systems with diverse routing logic.  
This paper introduces Hermes, an automated framework that leverages Large Language Models (LLMs) to bridge the semantic gap in distributed tracing. Key to our approach is the insight that "message types" serve as semantic contracts. Hermes leverages these types to synthesize latent routing logic into high-level communication patterns, which subsequently guide the precise discovery of concrete message flows from sender APIs to handlers.  
Evaluation on 10 real-world systems demonstrates that Hermes significantly outperforms existing approaches, achieving 88.6% precision and 99.6% recall in flow discovery.  
Applying Hermes to security auditing revealed 121 verified taint paths spanning 57 distinct sinks. These findings led to 56 confirmed zero-day vulnerabilities, of which 53 have been fixed and 7 assigned CVE IDs.

