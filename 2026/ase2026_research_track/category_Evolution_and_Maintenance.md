# ASE 2026 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 8

## 1. A Selective Undo/Redo Algorithm for Dependency-Constrained Operation Histories Based on Change Propagation

**Authors:** Xiaoxiong Fan (Tsinghua University, China), Hou Tam (Tsinghua University, China), Hanxi Zhu (Tsinghua University, China), Song-Hai Zhang (Tsinghua University, China)

**Categories:** Evolution and Maintenance

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837482

**中文总结:** 针对依赖约束编辑历史，提出基于变更传播的选择性 undo/redo，在 slot+reducer 语义下局部传播切换影响而非全量重放；在 Godot 改造型游戏 IDE 编辑器中与重放基线语义一致，切换时前置条件评估约降 194×。

**Abstract:** Selective undo and redo let users disable or re-enable a specific historical operation while attempting to preserve unrelated later work. This is particularly valuable in interaction-heavy and collaborative editing environments, where mistakes may be discovered only after substantial later work has accumulated and where discarded edits are costly to reconstruct manually. Achieving this is significantly harder when operations are dependency-constrained: whether they remain valid after a toggle may depend on complex semantic conditions, and naively replaying long history suffixes after every toggle is too expensive for interactive use. To this end, we present a dependency-sensitive change-propagation algorithm that preserves a replay-style correctness target without full replay after every toggle. Our approach decomposes editor state into fine-grained slots with reducer-backed semantics, evaluates operation legality against prefix state, and propagates the effect of a toggle only through the affected neighborhood of later operations and state changes. We implement the mechanism in the scene editor of an in-house game IDE built on a heavily modified version of the Godot Engine. Across differential testing against two exact replay baselines and a validity-aware fuzzing campaign comprising 45 runs and 450,000 recorded actions, our change-propagation pipeline matched the reference semantics on all evaluated workloads. It substantially reduced toggle latency and semantic work relative to both baselines, including a reduction of about 194× in prerequisite evaluations. These results show that replay-style selective undo/redo can be made practical for operations with hard dependency constraints.


## 2. A Unified Model for Cross-Domain Clone Detection via Model Merging

**Authors:** Palash R. Roy (University of Saskatchewan, Canada), Banani Roy (University of Saskatchewan, Canada), Kevin A. Schneider (University of Saskatchewan, Canada), Chanchal K. Roy (University of Saskatchewan, Canada)

**Categories:** Evolution and Maintenance

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837415

**中文总结:** 系统评估 task-vector 合并（TIES 等）、层拼接与跨 tokenizer 对齐，在无需合并阶段再训练的前提下构建跨域 clone 检测器；同底座 TIES 在 UniXcoder 上综合 F1 达 0.865（约为多任务训练的 93%），对 AI 生成 clone 的泛化优于 WUDI 等多任务方案。

**Abstract:** The growing diversity of code clone types, from syntactic copies to cross-language semantic clones to AI-generated duplicates, has created a fragmentation crisis in clone detection. Current deep learning detectors are domain specialists that degrade significantly outside their training distribution. In our evaluation, F1 drops exceed 70% across domains. Deploying multiple specialized models is impractical, yet training a single cross-domain detector requires simultaneous access to all training data. To address this, we investigate model merging, a family of post-hoc techniques that operate solely on trained checkpoints. We systematically evaluate parameter merging with five task-vector methods (Task Arithmetic, TIES, DARE-TIES, WUDI, PCB), architecture merging via greedy layer stitching, and cross-tokenizer alignment. Our study spans four pre-trained code models, three benchmarks, and twelve merging configurations. Same-base TIES merging creates effective cross-domain detectors, validated across two model families and three random seeds. It reaches 0.865 combined F1 on UniXcoder, 93% of multi-task training performance without any training data at the merging step. WUDI achieves the highest in-distribution combined F1 at 0.899, but TIES generalizes better to unseen AI-generated clones. We therefore recommend TIES for the practical recipe. Cross-base merging yields only marginal and high-variance gains across all five methods. This indicates that task vector compatibility through a shared pre-trained base is the binding factor for effective merging in our setting. Merged encoder-based detectors also outperform zero-shot instruction-tuned code LLMs on GPTCloneBench (0.609 vs. 0.454 F1 for the strongest LLM baseline) at substantially lower per-pair inference cost. They also generalize up to 4× better than multi-task training to unseen AI-generated clones, suggesting a trade-off between in-domain performance and OOD robustness. This work provides one of the first systematic empirical studies of model merging for software engineering and a practical recipe for building cross-domain code clone detectors.


## 3. BDiff: Block-Aware and Accurate Text-Based Code Differencing

**Authors:** Yao Lu (National University of Defense Technology, China), Wanwei Liu (National University of Defense Technology, China), Tanghaoran Zhang (National University of Defense Technology, China), Kang Yang (National University of Defense Technology, China), Yang Zhang (National University of Defense Technology, China), Wenyu Xu (National University of Defense Technology, China), Longfei Sun (National University of Defense Technology, China), Xinjun Mao (National University of Defense Technology, China), Shuzheng Gao (Chinese University of Hong Kong, China), Michael R. Lyu (Chinese University of Hong Kong, China)

**Categories:** Evolution and Maintenance

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837431

**中文总结:** 提出 BDiff 块感知文本 diff 算法，识别块级与行级编辑动作并最小化编辑脚本。实验表明其 diff 质量优于含 LLM 在内的基线，且 LLM 在质量与时效上不可靠。

**Abstract:** Code differencing is a fundamental technique in software engineering. Traditional line-level differencing tools (e.g., Git Myers algorithm) cannot accurately identify block-level edit actions (EAs) such as block move and copy, which are common in real development. They split multi-line block edits into fragmented line-wise changes, raising developers’ cognitive overhead during code review. This paper presents BDiff, a text-based differencing algorithm capable of identifying two types of block-level EAs and five types of line-level EAs. Building on traditional differencing algorithms, we first construct a candidate set containing all possible line and block mappings. Leveraging the Kuhn-Munkres algorithm, we then compute the optimal mapping set and derive a minimal edit script (ES) that closely aligns with the original developer intent. To evaluate BDiff, we selected five state-of-the-art tools, including large language models (LLMs), as baselines, and adopted a combined qualitative and quantitative approach to assess their performance in terms of ES size, result quality, and running time. Experimental results show that BDiff produces higher-quality differencing results than baseline tools while maintaining competitive runtime performance. Our experiments also show the unreliability of LLMs in code differencing tasks and their infeasibility in terms of runtime efficiency. Based on the proposed algorithm, we have implemented an open-sourced visual differencing tool.


## 4. Beyond Syntactic Differencing: Semantic-Aware Scheduling for Cross-Configuration Incremental Builds

**Authors:** Xiaolong Dai (Nanjing University, China), Shanshan Li (Nanjing University, China), Jun Lyu (Nanjing University, China), Xintao Niu (Nanjing University, China)

**Categories:** Evolution and Maintenance

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837533

**中文总结:** 提出 SIBS：用语义距离估计配置切换的重编译代价，并将跨配置增量构建调度建模为 ATSP 全局优化；21 个真实可配置系统中 17 个较 SOTA 调度器缩短构建时间，几何平均约降 27.7%。

**Abstract:** Modern configurable software systems are routinely built and tested across thousands of configuration variants to ensure correctness under diverse settings. Reusing build artifacts across configurations is therefore crucial to reduce redundant effort, yet remains challenging. Existing approaches estimate rebuild cost using syntactic option differences and apply greedy scheduling, which often misestimate true costs and yield suboptimal build orders. We present SIBS, the first semantics-aware scheduling framework for incremental builds across configurations, addressing both inaccurate cost estimation and the limitations of greedy scheduling. The key idea is a semantic distance metric that models the impact of configuration changes on rebuild scope by capturing option-level effects on code generation, accounting for global configuration headers, and propagating changes through dependency graphs. This enables cost-aware global scheduling formulated as an Asymmetric Traveling Salesman Problem (ATSP). Across 21 real-world systems and five independently sampled configuration batches, SIBS reduces observed build time relative to the state-of-the-art build scheduler in 17 systems. On average, it saves 196s (21%), with a median saving of 40s (3%), and achieves a 27.7% geometric-mean reduction in build time across projects. Batch-level reductions range from 25.7% to 29.3% , and the scheduling overhead remains modest (median 3.1s; mean 12.9s). These results demonstrate that semantics-aware cost modeling and global scheduling provide substantial and robust efficiency gains across diverse configurable systems.


## 5. CodeFault: Predicting Fault Risks from Code Changes via Multi-modal Learning

**Authors:** Yifan Xiao (Peking University, China), Shijie Li (China Southern Power Grid, China), Yu Huang (Peking University, China)

**Categories:** Evolution and Maintenance

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837462

**中文总结:** 提出 CodeFault，将代码变更语义与运行时日志模式通过分层故障谱对齐（HFSA）与谱引导跨模态注意力（SGCA）融合，做即时缺陷风险预测；在 Defects4J 等 3.1 万样本与 55 个 GitHub Actions 仓库的 CI/CD 对上分别达到 0.891/0.843 AUC，并可用蒸馏版在无日志场景部署。

**Abstract:** Just-In-Time defect prediction identifies fault-inducing code changes but relies solely on static code properties, missing runtime fault patterns. Meanwhile, log-based anomaly detection captures runtime behaviors but lacks visibility into causal code modifications. This disconnect delays fault identification and complicates root cause analysis. We present CodeFault, a multi-modal fault prediction framework that fuses code change semantics with runtime log patterns through two novel mechanisms. Hierarchical Fault Spectrum Alignment (HFSA) projects both modalities into a shared, two-level fault taxonomy space—four coarse and eight fine-grained categories—providing a structured information bottleneck that enables principled cross-modal knowledge transfer. Spectrum-Guided Cross-Modal Attention (SGCA) performs token-level fusion conditioned on fault spectrum agreement, avoiding the degeneracy of pooled-vector approaches while focusing attention on fault-relevant token pairs. A dual-granularity contrastive objective further leverages the taxonomy structure to separate fault-inducing from benign embeddings at both instance and fault-type levels. We evaluate CodeFault on two complementary testbeds. On the public benchmark of 31,142 samples from Defects4J, BugsInPy, and ManySStuBs4J, CodeFault reaches 0.891 AUC-ROC and 0.857 F1-score against 15 prior-art baselines and 2 self-constructed strong late-fusion controls, improving over the strongest code-only baseline by 5.1% AUC and over the strongest late-fusion control by 3.1% AUC (Wilcoxon signed-rank test, Cliff's δ ≥ 0.73). On 2,147 real co-occurring CI/CD pairs collected from 55 GitHub Actions repositories with the CI build outcome as ground truth—the largest non-synthetic CI/CD fault test set in JIT defect prediction to date—CodeFault reaches 0.843 AUC, +4.3% over JIT-Smart, retaining 94.6% of the synthetic-set headline. The framework generalizes to unseen projects with 2.5% average AUC improvement and maintains 97.9% AUC under realistic 15% positive rates. A knowledge-distilled code-only variant achieves 0.862/0.831 AUC on synthetic/real test sets without log inputs, enabling pre-commit deployment.


## 6. DepUpgrade: Automating Dependency Upgrade through State-Path Exploration

**Authors:** Xiangxi Ma (Beihang University, China), Yifan An (Beihang University, China), Wentong Tian (Beihang University, China), Xuanqi Wang (Beihang University, China), Qingao Dong (Beihang University, China), Xiang Gao (Beihang University, China), Hailong Sun (Beihang University, China)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837442

**中文总结:** 将依赖升级建模为状态路径探索，结合编译反馈与 API 迁移知识在可回滚的中间状态间搜索修复；123 项基准全修复率 96.7%，18 个真实项目中 15 个完全修复。

**Abstract:** Third-party dependencies frequently introduce API breaking changes, and upgrading them causes compilation or runtime failures in client applications. Existing approaches have explored automating dependency upgrades, but struggle with fixing complex issues. This is mainly because traditional methods lack semantic adaptability, while recent prompt-only LLM-based migration approaches often suffer from hallucinations and fail to navigate multi-step, cascading repairs. To solve this problem, in this paper, we propose DepUpgrade, a framework that models dependency upgrade as a state-path exploration problem. A state is a snapshot of the client codebase at a particular point during migration. Transitions between states are validated via compiler feedback and rolled back if regressions occur. Instead of performing a single-pass generation, DepUpgrade systematically explores a search space of intermediate states with the goal of reaching a successful state. DepUpgrade achieves this goal in three steps: API migration knowledge extraction, repair task formulation and state-path exploration. We evaluate DepUpgrade on a benchmark of 123 migration tasks and 18 real-world projects. Experimental results demonstrate that our framework achieves an unprecedented 96.7% full repair rate on the benchmark, outperforming other baselines. On the real-world projects, DepUpgrade fully repairs 15 of the 18 projects and leaves 31 of the 1,085 initial compilation errors unresolved.


## 7. Latent Reuse in Agent Skills: Multi-modal Clone Detection at Ecosystem Scale

**Authors:** Jiaying Zhu (Nanyang Technological University, Singapore), Lyuye Zhang (Nankai University, China / Nanyang Technological University, Singapore), Wenbo Guo (Nanyang Technological University, Singapore), Yang Liu (Nanyang Technological University, Singapore)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837468

**中文总结:** SkillReuse 多模态克隆检测（YAML/ prose/ code）与 SkillReuse-Bench；F1 0.939，在 137470 skill 上发现 106 万克隆对、66.8% skill 涉及跨作者复用，安全相关 skill 图扩展暴露单 skill 扫描会漏掉的 16587 链接。

**Abstract:** An agent skill is a reusable package for extending an LLM agent, typically a SKILL.md file that combines YAML metadata, natural-language instructions, and executable code. Public repositories now host over two million skills, yet existing tools analyze each artifact in isolation, and registries do not track reuse created through copying, renaming, or adaptation. Detecting these links is difficult because reuse may appear in one channel while the others change; conventional single-channel clone detectors can therefore miss such adaptations. We present SkillReuse, a multi-modal clone detector that combines global lexical matching with channel-specific representations for YAML, prose, and code, then uses logistic regression to produce clone scores and interpretable clone-type labels. We also introduce SkillReuse-Bench, an annotated benchmark of 300 skill pairs spanning exact copies, renamed copies, adaptations, and semantic equivalents. On SkillReuse-Bench, SkillReuse reaches an F1 of 0.939 with 0.952 precision, improving over TF-IDF and delivering 4.2× higher recall on Type-4 semantic clones than MinHash. Applied to all 137,470 skills that pass the content filter, SkillReuse identifies 1.06 million clone pairs involving 66.8% of the analyzed skills; 95.3% of these pairs cross author boundaries. Among skills in the analyzed name-based clone families, 67% are superseded by a higher-quality variant. Tracing 938 security-relevant skills through the clone graph surfaces 16,587 clone links spanning 6,376 related skills that per-skill scanners alone would miss.


## 8. We Must Have Missed This Comment: Detecting and Repairing Stale Function References in Linux Kernel Comments

**Authors:** Kexin Sun (Nanjing University, China), Yunbo Lyu (Singapore Management University, Singapore), Xutong Ma (Inria, France), Hongyu Kuang (Nanjing University, China), Ratnadira Widyasari (Singapore Management University, Singapore), He Zhang (Nanjing University, China), Xiaoxing Ma (Nanjing University, China), Julia Lawall (Inria, France), David Lo (Singapore Management University, Singapore)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837474

**中文总结:** 提出 ReCite 三阶段流程：检测注释中无法解析的函数形符号、沿 Git 追溯演化、结合历史与上下文用 LLM 生成修复建议；在 Linux v6.18-rc1 发现 869 处陈旧引用，抽样 200 条中 89% 修复建议有用、42.5% 可直接应用，75 个补丁中 50 个已合入。

**Abstract:** As the Linux kernel evolves, code comments may become outdated, as the functions they reference can be refactored or removed independently without corresponding updates to the comments. Such stale function references can mislead maintainers and thus hinder code comprehension. Prior work on detecting code-comment inconsistency mainly focused on addressing semantic misalignment between Javadoc comments and their directly annotated functions, making them inapplicable to this type of externally induced staleness in the Linux kernel. Therefore, we propose ReCite, a three-stage approach to identify and repair such stale references: (1) detecting unresolved function-form symbols —symbols in comments that appear to reference functions but for which no matching function can be found in the current codebase, (2) tracing the evolution history of each unresolved symbol through the Git history, and (3) generating LLM-based repair suggestions grounded in the evolution history and current code context. On Linux kernel v6.18-rc1, ReCite detects 869 stale references with generated repair suggestions. A manual evaluation on 200 sampled repairs shows that 178 (89.0%) provide useful repair guidance, with 85 (42.5%) directly applicable. Of our 75 submitted patches, 50 have been accepted. We also empirically study all unresolved function-form symbols.

