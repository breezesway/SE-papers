# ASE 2026 Research Track — Debugging and Fault Diagnosis

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 13

## 1. ARMOR: A Robust Self-Supervised Framework for Root Cause Analysis in Microservices under Missing Modality

**Authors:** Wenzhuo Qian (Zhejiang University, China), Hailiang Zhao (Zhejiang University, China), Ziqi Wang (Zhejiang University, China), Zhipeng Gao (Zhejiang University, China), Jiayi Chen (Zhejiang University, China), Zhiwei Ling (Zhejiang University, China), Shuiguang Deng (Zhejiang University, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834338

**中文总结:** 提出 ARMOR：模态不对称编码器 + 缺失感知门控融合与 mask 重建自监督，联合优化异常检测、故障分诊与根因定位；在数据完整时达 SOTA，在严重模态缺失下仍保持稳健诊断精度。

**Abstract:** Automated incident management is critical for microservice reliability. While recent unified frameworks leverage multimodal data for joint optimization, they unrealistically assume perfect data completeness. In practice, network fluctuations and agent failures frequently cause missing modalities. Existing approaches relying on static placeholders introduce imputation noise that masks anomalies and degrades performance. To address this, we propose ARMOR, a robust self-supervised framework designed for missing modality scenarios. ARMOR features: (i) a modality-specific asymmetric encoder that isolates distribution disparities among metrics, logs, and traces; and (ii) a missing-aware gated fusion mechanism utilizing learnable placeholders and dynamic bias compensation to prevent cross-modal interference from incomplete inputs. By employing self-supervised auto-regression with mask-guided reconstruction, ARMOR jointly optimizes anomaly detection (AD), failure triage (FT), and root cause localization (RCL). AD and RCL require no fault labels, while FT relies solely on failure-type annotations for the downstream classifier. Extensive experiments demonstrate that ARMOR achieves state-of-the-art performance under complete data conditions and maintains robust diagnostic accuracy even with severe modality loss.


## 2. Bifrost: Empowering Pretrained Language Model with Fallibility Representation for Log-Based Fault Diagnosis

**Authors:** Minghua He (Peking University, China), Tong Jia (Peking University, China), Lingzhe Zhang (Peking University, China), Chiming Duan (Peking University, China), Xinlong Zhao (Peking University, China), Leyi Pan (Tsinghua University, China), Cheng Wang (Alibaba Group, China), Kangjin Wang (Alibaba Group, China), Yinghao Yu (Alibaba Group, China), Liping Zhang (Alibaba Group, China), Yifan Wu (Peking University, China), Ying Li (Peking University, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834433

**中文总结:** 提出 Bifrost 日志表示学习方法，通过自监督对比学习捕获多层次“可故障性”特征。在公开与工业 MLaaS 系统上，异常检测 F1、根因定位 HR@k、故障识别 Macro-F1 均显著优于现有 PLM。

**Abstract:** Log-based fault diagnosis is crucial for runtime debugging and maintenance. Existing fault diagnosis methods use language models pre-trained on natural language (PLMs) for log representation. However, system faults are reflected in the multi-level structure of system logs. PLMs pre-trained on natural language struggle to comprehensively capture multi-level fault information, failing to meet the requirements of fault diagnosis. We refer to this information as fallibility representations. To address this problem, we propose a novel log representation learning method, Bifrost. It draws inspiration from the log analysis experience of Site Reliability Engineers and meticulously designs strategies based on self-supervised contrastive learning to learn the fallibility representations of logs. Across three public systems and one industrial ML-as-a-Service system, the log representations produced by Bifrost outperform existing PLMs by average margins of 9.83% in F1 for anomaly detection, 18.28% in HR@k for root cause localization, and 20.88% in Macro-F1 for fault identification.


## 3. COBug: A Bug Localization Pipeline for COBOL: Does It Work? An Exploratory Study

**Authors:** Kavyasri Gajula (Indian Institute of Technology Tirupati, India), Phanindra Kodela (Indian Institute of Technology Tirupati, India), Sridhar Chimalakonda (Indian Institute of Technology Tirupati, India)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837518

**中文总结:** 提出 COBug 流水线与 552 查询、12 个 X-COBOL 仓库的可控 benchmark（独立生成 bug 报告与机械 ground truth）；LOO 评估下词法 IR、LambdaMART、冻结 CodeBERT 等均未在 Holm 校正后显著优于仓库匹配随机基线（MAP≈0.15 vs 0.123）。

**Abstract:** Bug localization, the task of ranking source files according to their likelihood of containing a reported bug, is a central software maintenance problem. Despite COBOL’s continued industrial importance, file-level bug localization for COBOL lacks a controlled benchmark for reproducible evaluation. We present COBug, a COBOL bug-localization pipeline with a controlled static benchmark, independently generated bug reports, and mechanically traceable source-level ground truth. Using COBug, we find that standard lexical, learned, and embedding-based methods do not reliably exceed a repository-matched random-ranking floor. The benchmark comprises 552 deterministic queries from 12 X-COBOL repositories, each linked to one isolated source transformation, a mechanically traceable ground-truth file, and a symptom-focused bug report generated independently of the target source file. We evaluate lexical retrieval, classical and learning-to-rank re-ranking, and frozen CodeBERT under strict Leave-One-Repository-Out evaluation with repository-grouped inner validation. Across five seeds, lexical IR achieves MAP (=MRR) 0.1508 against a mean repository-matched random floor of 0.1229. LambdaMART achieves the highest aggregate MAP (0.1625), whereas standalone frozen CodeBERT retrieval remains near the random floor (MAP 0.1236). However, after Holm correction, no evaluated method significantly exceeds the random floor, and no pairwise comparison remains significant. A separate LLM-based semantic-fault pilot admitted 15 of 29 adjudicated candidates, but none of the three generators covered all five fault types required by the predefined gate. The semantic pilot is therefore excluded from the localization evaluation and retained only as admission evidence. A structured OpenCBS/ODC comparison further bounds the benchmark’s representativeness by identifying the injected categories that correspond to recreated real COBOL defects and those that do not.


## 4. EffiHolmes: Differential Profiling-Guided Repository Level Time Inefficiency Fix Localization

**Authors:** Haowen Yang (Hong Kong University of Science and Technology, Guangzhou, China), Yun Peng (Chinese University of Hong Kong, Hong Kong), Zishuo Ding (Hong Kong University of Science and Technology, Guangzhou, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834353

**中文总结:** 提出 EffiHolmes，以差分 profiling 定位热点、抽取紧凑执行路径并用 LLM 启发式 bridging 修复点；新建 RepoEffi-Bench（140 个 Python 低效 issue）上显著优于检索/agent/profiling 基线。

**Abstract:** Large software systems often suffer from time inefficiencies, leading  
to excessive execution time despite functional correctness. Local-  
izing the fix locations of such inefficiency issues is notoriously  
difficult. Applying existing fault localization paradigms to this task  
presents significant challenges. Unlike functional bugs, time ineffi-  
ciencies do not cause crashes or test failures. They therefore provide  
neither binary oracles nor stack-trace localization clues, making  
traditional fault localization and recent LLM-based methods not ap-  
plicable. While runtime profiling provides alternative clues, it faces  
some challenges in repository-level settings. Single-run profiling  
is non-discriminative, failing to distinguish inefficiency hotspots  
(i.e., time-consuming functions) from execution noise. Furthermore,  
existing profilers struggle to extract the execution paths relevant  
to inefficiency from the vast background execution. Crucially, even  
with the extracted execution paths, a semantic gap still persists  
between the observed inefficiency and where to fix.  
In this paper, we propose EffiHolmes, an LLM-based frame-  
work for localizing fix locations of repository-level time inefficiency  
issues. First, it employs differential profiling (default vs. scaled  
workloads) to pinpoint inefficiency hotspots. Second, to extract  
the execution paths relevant to inefficiency, it performs execution  
path extraction, constructing compact execution paths that connect  
hotspots to the reported inefficient function. Third, to bridge the  
gap between the hotspots and fix locations, it employs guided LLM  
reasoning with domain heuristics to locate the inefficiency logic.  
To facilitate the evaluation, we introduce RepoEffi-Bench, the first  
benchmark for repository-level inefficiency localization, consisting  
of 140 high-quality time inefficiency issues collected from popular  
Python repositories. The results show that EffiHolmes consis-  
tently outperforms state-of-the-art retrieval-based, agent-based,  
and profiling-based baselines, with gains of 4.29 pp on GPT-5.1 file-  
level Acc@3 and 15.00 pp on qwen3-4b function-level Acc@5 over  
the best baseline. It also remains robust across model capacities.


## 5. Enhancing Trace-Based Root Cause Analysis for Microservice Systems via Code Change Understanding

**Authors:** Min Zhang (Xidian University, China / Fudan University, China), Chenxi Zhang (Xidian University, China), Senyu Xie (Fudan University, China), Shihong Chen (McDonald's, China), Lei Wu (McDonald's, China), Xin Peng (Fudan University, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837424

**中文总结:** 提出 DeltaRCA，将 LLM 变更影响分析与 trace 谱定位结合于异构图传播，实现 RCA 左移；200 个注入故障上平均 Top-1/Top-3 为 63%/79%，优于现有 trace RCA。

**Abstract:** Microservice architecture has become the dominant design pattern for modern web applications. However, the dynamic structure, complex inter-service invocations, and continuous updates of microservices make root cause analysis (RCA) particularly challenging. Existing RCA methods typically rely on runtime monitoring data such as traces and metrics, and adopt techniques including deep learning, graph analysis, and spectrum analysis. However, most of these methods overlook software changes, even though code and deployment updates are often the underlying causes of production failures. This paper introduces the idea of RCA left-shifting, which shifts part of the diagnostic effort to the development stage by proactively understanding change semantics before failures occur. Based on this insight, we propose DeltaRCA, a trace-based RCA approach that integrates large language model (LLM)-driven change impact analysis with spectrum-based root cause localization. DeltaRCA uses an LLM agent to identify semantically affected operations from code changes. This information is incorporated into a heterogeneous graph to guide the weight propagation process in spectrum-based fault localization. We evaluate DeltaRCA on two microservice benchmarks with 200 injected fault cases. The results show that DeltaRCA outperforms state-of-the-art methods, achieving 63% Top-1 and 79% Top-3 accuracy on average. Furthermore, ablation analysis demonstrates that incorporating change understanding significantly improves localization precision.


## 6. GALA: Graph-Augmented LLM Agents for Root Cause Analysis and Incident Response in Microservices

**Authors:** Yifang Tian (University of Toronto, Canada), Yaming Liu (University of Toronto, Canada), Zichun Chong (University of Toronto, Canada), Zihang Huang (University of Toronto, Canada), Yiran Li (University of Toronto, Canada), Hans-Arno Jacobsen (University of Toronto, Canada)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834335

**中文总结:** 提出 GALA+ 图增强 LLM 智能体框架，以服务依赖图约束探索并结合 STRIX 多模态遥测评分，输出根因排序、事件摘要与分层处置建议；在两个微服务基准上 AC@1 较最佳 LLM 基线提升超过 25 个百分点，SURE-Score 与 SRE 人工评价亦领先。

**Abstract:** Microservice root cause analysis (RCA) requires correlating failures across heterogeneous telemetry within complex service dependency graphs. Existing methods often rely on a single telemetry modality; recent LLM-based approaches can suffer from unconstrained exploration and hallucination; and most systems stop at fault ranking without producing actionable incident response. We present GALA+, a graph-augmented LLM agentic framework centered on graph-guided investigation, which uses service dependencies to bound exploration and refine diagnosis through localized multi-modal evidence. For initial hypothesis generation, GALA+ combines complementary telemetry signals with STRIX, a novel trace- and graph-structure-aware scoring module. GALA+ then produces ranked diagnoses, incident summaries, and stratified action recommendations. We further introduce SURE-Score, a human-guided evaluation framework co-developed with industry SRE experts for assessing RCA-specific output quality beyond conventional text similarity metrics. On two microservice benchmarks, GALA+ consistently achieves the strongest overall results, surpassing the best LLM-based baseline by more than 25 percentage points in AC@1, while also receiving the highest ratings from both SURE-Score and independent human SRE evaluation.


## 7. HERO: Hypothesis-Centered Root-Cause Analysis for Microservice Incidents

**Authors:** Jiewei Lyu (Sun Yat-sen University, China), Junquan Yi (Sun Yat-sen University, China), Shu Liang (Tencent, China), Pengfei Chen (Sun Yat-sen University, China), Long Pan (Tencent, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837509

**中文总结:** 提出 Hero 假设中心 RCA：有界假设空间实例化、信念状态跟踪与歧义引导取证；在 OpenRCA 上 SR 79.77（较最强 ReAct 基线 +23.20），工业数据集 SR 85.00，且平均少用 1.04 步动作。

**Abstract:** Root-cause analysis (RCA) in cloud-native microservice systems is challenging because it requires integrating heterogeneous observability signals and deciding what to inspect next under limited diagnosis budgets. Existing large language model (LLM)-based RCA agents either rely heavily on predefined workflows, whose effectiveness is constrained by incomplete Standard Operating Procedure (SOP) coverage, or adopt open-ended diagnosis, which remains brittle when multiple plausible root-cause hypotheses are consistent with the observed evidence. We present Hero, a hypothesis-centered RCA framework that formulates diagnosis as controlled discrimination among competing hypotheses via bounded hypothesis-space instantiation, explicit belief-state tracking, and ambiguity-guided evidence acquisition. We evaluate Hero on OpenRCA and a real-world industrial incident dataset against representative workflow-based and open-ended baselines. On OpenRCA with DeepSeek-V3, Hero achieves an S R of 79.77, outperforming the strongest ReAct-style baseline by 23.20 points while using 1.04 fewer actions on average. On the industrial dataset, it reaches an S R of 85.00 and remains the best-performing method. These results suggest that explicitly controlling competing hypotheses is an effective and practically promising abstraction for microservice RCA, especially in real-world, production-style incidents with incomplete workflow coverage and high diagnostic ambiguity.


## 8. How Quantum Bugs Live and Die: A Lifecycle-Based Empirical Study of Bugs in Quantum Software

**Authors:** Yasai Shi (Beihang University, China), Xiangxin Meng (Beihang University, China), Xiangjie Huang (Beihang University, China), Jian Zhang (Beihang University, China), Tianyu Wo (Beihang University, China), Xu Wang (Beihang University, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834439

**中文总结:** 构建含 2429 个缺陷的 QBugsSet 生命周期基准，对比量子软件与经典缺陷的分布、修复延迟与传播特征。发现量子特有缺陷更难修复且前沿 LLM 端到端完整修复率仅 3.82%。

**Abstract:** Despite growing evidence that bugs in quantum software exhibit distinctive characteristics, existing studies are typically scoped to individual frameworks or single quality attributes and do not examine how quantum-specific bugs behave across the broader software lifecycle. To address this gap, we construct QBugsSet, a lifecycle-based benchmark containing 2,429 bugs and 1,793 realistic negative samples, mined from real GitHub bug-fixing commits in the Qiskit, Cirq, and PennyLane ecosystems, and use it to conduct a comprehensive empirical study comparing quantum-specific and classical bugs across lifecycle distribution, bug-fix latency and pre-fix spatial propagation, repair burden, and LLM-based debugging effectiveness. We find that quantum-specific bugs are more concentrated in semantically critical stages, tend to persist longer before repair (median 17 vs. 7 days), and more often require coordinated multi-hunk repairs (37.8% vs. 27.3%). These lifecycle characteristics highlight a practical limitation of current automation: even the best frontier LLM achieves an end-to-end full repair rate of only 3.82% on quantum-specific bugs, compared with 8.51% on classical bugs. Overall, these findings provide evidence-based guidance for future debugging support that integrates stronger quantum-aware semantic reasoning with broader repository context.


## 9. HyTri: Hybrid Triage of CI Failures via LLM Guided Semantic Reasoning and Change Attribution

**Authors:** Lior Broide (Ben-Gurion University of the Negev, Israel), Argaman Mordoch (Ben-Gurion University of the Negev, Israel), Roni Stern (Ben-Gurion University of the Negev, Israel)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837467

**中文总结:** HyTri 融合 LLM 引导的故障语义与根因假设、变更归因信号做置信加权聚类；新建 MFCI-Benchmark，在 MFCI 与 multifault Defects4J 上优于现有 triage 基线，浅栈 trace 场景仍稳健。

**Abstract:** Continuous Integration (CI) builds execute large test suites that often yield multiple simultaneous failures, many originating from a common underlying fault.  
Test failure triage -- grouping failing tests by their root cause -- is therefore critical for reducing debugging effort.  
Existing approaches work poorly in CI builds with multiple faults, and either lack 
semantic reasoning or ignore highly informative structural and change-aware signals. 
To address these limitations, we propose HyTri, a framework that integrates LLM-guided causal reasoning into test failure triage. 
HyTri derives similarity signals that consider failure semantics and hypothesized root causes. It fuses these signals using confidence weighting and error-type adjustment into a unified similarity measure that is used to cluster the failing tests.  
To evaluate HyTri we created Multi-Fault CI Build Benchmark (MFCI-Benchmark), a novel benchmark for test failure triage algorithms comprising synthesized multi-fault CI builds from well-known bug repositories.  
Experimental results over MFCI-Benchmark and the multifault Defects4J fault localization benchmark showed that HyTri outperforms existing baselines, maintaining strong performance even in datasets where stack traces are shallow and uninformative.


## 10. Needle in the Repo: Diagnosing Maintainability Failures in AI-Generated Repository Edits

**Authors:** Haichao Zhu (Qualcomm, USA), Qian Zhang (University of California at Riverside, USA), Jiyuan Wang (Tulane University, USA), Zhaorui Yang (University of California at Riverside, USA), Yuxin Qiu (University of California at Riverside, USA)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834401

**中文总结:** 提出 NITR 探针–oracle 框架，在行为正确的前提下用功能测试+结构 oracle 诊断 AI 仓库级编辑的可维护性；23 种编码配置平均仅 36.2% 通过，13.3% 功能全过却结构失败，架构类压力（依赖控制 4.3%）最难。

**Abstract:** AI coding agents can now complete complex programming tasks, but existing evaluations largely emphasize behavioral correctness and often overlook maintainability risks such as weak modularity or testability. Automation without accountability shifts invisible cost downstream because hidden maintainability failures incurred today are deferred to the developers who must extend, debug, and sustain these systems tomorrow, raising significant technical and organizational concerns for software engineering. We present Needle in the Repo (NITR), a diagnostic, probe-and-oracle framework for evaluating whether behaviorally correct repository edits preserve maintainable structure. The key idea is to distill recurring software engineering wisdom into controlled probes embedded in small, realistic multi-file codebases, with each probe designed so that success depends primarily on one targeted maintainability dimension. Each probe is paired with a hidden evaluation harness that combines (i) functional tests for required behavior, and (ii) structural oracles that encode the targeted maintainability constraint and return interpretable diagnoses. Using NITR, we extensively evaluate 23 coding configurations across GPT, Claude, Gemini, and Qwen families in both direct-inference and agent-based settings. We find that current AI coding systems remain far from robust. On average, all AI coding configurations solve only 36.2% of cases, the best reaches 57.1%, and performance drops from 53.5% on micro cases to 20.6% on multi-step cases. The hardest pressures are architectural rather than local edits, especially dependency control (4.3%) and responsibility decomposition (15.2%). Moreover, 64/483 outcomes (13.3%) pass all functional tests yet fail the structural oracle. Under our harness, agent-mode configurations improve average performance from 28.2% to 45.0%, but do not eliminate the architectural failures. These results show that progress in code generation is not yet progress in maintainable code evolution, and that NITR exposes a critical failure surface largely missed by conventional evaluation.


## 11. ReLog: Execution-Aware Logging with Runtime Feedback for LLM-Oriented Debugging

**Authors:** Xin Wang (Hong Kong University of Science and Technology, Guangzhou, China), Yang Feng (Hong Kong University of Science and Technology, Guangzhou, China), Xiaoqian Jiao (Hong Kong University of Science and Technology, Guangzhou, China), Yang Zhang (Hebei University of Science and Technology, China), Zhenhao Li (York University, Canada), Zishuo Ding (Hong Kong University of Science and Technology, Guangzhou, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837463

**中文总结:** 提出 ReLog，以运行时反馈迭代生成/执行/评估/精化日志，以下游缺陷定位与修复效用替代与开发者日志的文本相似度；在 Defects4J 直接/间接调试设定下 F1 达 0.520/0.408，直接设定修复 97 个缺陷，优于全部基线。

**Abstract:** Logging statements are essential for software debugging and maintenance. However, existing approaches to automatic logging generation rely on static analysis and produce statements in a single pass without considering runtime behavior. They are also typically evaluated by similarity to developer-written logs, assuming these logs form an adequate gold standard. This assumption is increasingly limiting in the LLM era, where logs are consumed not only by developers but also by LLMs for downstream tasks. As a result, optimizing logs for human similarity does not necessarily reflect their practical utility.  
To address these limitations, we introduce ReLog, an iterative logging generation framework guided by runtime feedback. ReLog leverages LLMs to generate, execute, evaluate, and refine logging statements so that runtime logs better support downstream tasks. Instead of comparing against developer-written logs, we evaluate ReLog through downstream debugging tasks, including defect localization and repair. We construct a benchmark based on Defects4J under both direct and indirect debugging settings. Results show that ReLog consistently outperforms all baselines, achieving an F1 score of 0.520 and repairing 97 defects in the direct setting, and the best F1 score of 0.408 in the indirect setting where source code is unavailable. Additional experiments across multiple LLMs demonstrate the generality of the framework, while ablations confirm the importance of iterative refinement and compilation repair. Overall, our work reframes logging as a runtime-guided, task-oriented process and advocates evaluating logs by their downstream utility rather than textual similarity.


## 12. TELLER: Non-intrusive Cross-Layer Root-Cause Analysis for LLM Inference

**Authors:** Ruilin Xu (Sun Yat-sen University, China), Junyi Li (Sun Yat-sen University, China), Pengfei Chen (Sun Yat-sen University, China), Zongxuan Xie (Sun Yat-sen University, China)

**Categories:** Debugging and Fault Diagnosis

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837440

**中文总结:** 提出 TELLER，无侵入采集 NVTX/CUPTI 与服务日志，重建 per-request 调用链并用 Trace Pair Encoding 压缩因果切片，多模态模型定位异常算子并生成解释；适度 TPE 词表在压缩 >80% 步长同时取得最佳跨节点/栈内 RCA 表现。

**Abstract:** Large language model (LLM) inference has evolved from an offline workload into a continuously operated software service, yet root-cause analysis remains difficult because a single request spans the inference engine, Python/C++ backend, host CUDA APIs, GPU kernels, and distributed communication. Existing profilers expose raw timelines, while log-based diagnosis often misses cross-layer execution semantics and request-level structure. We present TELLER, a non-intrusive trace- and log-aware LLM inference root-cause analysis framework. TELLER first collects NVTX/CUPTI traces and service logs without modifying model binaries, then reconstructs per-request call-chain trees and aligns log lines with the corresponding execution steps. We introduce a dependency-aware causal-context slice that preserves parent-child structure, temporal order, and communication relations, and a Trace Pair Encoding (TPE) tokenizer that compresses such slices into compact structural token sequences with parent, depth, and duration attributes. On top of these representations, TELLER combines numeric candidate localization with a multimodal root-cause model that jointly predicts abnormal steps, localizes suspicious operators, and generates natural-language explanations. Experiments on multi-node GPU inference workloads show a clear compression-accuracy trade-off: a moderate TPE vocabulary reduces per-step trace length by more than 80% while achieving the best overall performance on both horizontal (cross-node communication) and vertical (within-node execution stack) views, whereas more aggressive compression substantially degrades diagnosis quality. Further analyses under low-fault priors, strengthened baselines, modality ablations, explanation-quality checks, and tracing overhead show that TELLER provides a practical triage and evidence-localization substrate for LLM inference RCA.


## 13. When Does AI Actually Help in Incident Response? Identifying Good First Messages in Cloud Service Incidents

**Authors:** Minghua Ma (Microsoft, USA), Rujia Wang (Microsoft, USA), Chetan Bansal (Microsoft, USA), Saravan Rajmohan (Microsoft, USA), Yingnong Dang (Microsoft, USA), Hongyu Zhang (Chongqing University, China)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837473

**中文总结:** 基于 5 个云服务四年数千起生产 incident 定义「优质首条消息」（GFM），发现引入 AI 后线程中位长度增 7× 但 AI 噪声率最低，仅约 1/5 incident 含 GFM 且内容比发帖者类型更重要；LLM 排序器 σ-rank 将 GFM 排进约 20 条机器消息前三的概率达 89%，可约 7× 减轻阅读负担。

**Abstract:** Modern cloud services increasingly rely on agentic software operations, where AI agents, rule-based automation (monitoring alerts, health checks, template runbooks), and human engineers coordinate incident response through shared discussion threads. As these systems mature, the on-call engineer faces a growing volume of machine-generated messages and must quickly identify which ones actually help, under minutes-level time pressure where every moment spent reading noise delays mitigation. We study this problem across thousands of production incidents from 5 cloud services over four years (2022 to 2026). We define a good first message (GFM): the first machine-generated message in an incident discussion thread whose specific content demonstrably influences the on-call engineer’s next investigation action. Three findings emerge. First, incident threads grew 7× longer (from a median of 4 to 30 messages) as AI agents were introduced, yet noise (messages lacking substantive technical content) decreased : among the three actor types, AI agents, rule-based automation, and humans, AI produces the lowest noise rate. Second, AI agents and automation are complementary, covering different workflow roles (e.g., diagnosis vs. monitoring) rather than duplicating each other. Third, only about one in five incidents contains a GFM; influence varies dramatically by functional role but far less by actor type: what a message says matters more than who posted it. We further show that GFMs can be surfaced automatically: σ-rank, an LLM ranker whose prompt encodes domain knowledge from the empirical study, places the GFM in the top 3 of ∼20 machine messages 89% of the time, reducing the engineer’s noise-reading burden by 7×. These results provide the first empirical evidence of how deployed AI output is actually consumed during live incidents and offer a practical mechanism to cut through information overload in time-critical incident response.

