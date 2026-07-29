# FSE 2026 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 8 papers

## 1. Automating Dockerfile Refactoring to Multi-Stage Builds

**Authors:** Dongjin Chen (Nanjing University of Aeronautics and Astronautics), Wenhua Yang (Nanjing University of Aeronautics and Astronautics), Minxue Pan (Nanjing University), Yu Zhou (Nanjing University of Aeronautics and Astronautics)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797098

**中文总结:** 提出自动化方法，经静态分析识别技术栈与构建/运行依赖，并用图像膨胀、结构低效与安全风险综合门控后，将单阶段 Dockerfile 重构为多阶段构建；在 521 个真实项目上成功率为 60.3%，生成镜像平均缩小 52.2%、高危漏洞减少 50.0%。

**Abstract:** Containerization has become a cornerstone of modern software deployment, yet many projects still ship single-stage Dockerfiles that bundle compilers, build tools, and temporary files into production images, thereby hurting performance and security. Multi-stage builds are recommended, yet uptake appears uneven, plausibly because refactoring legacy Dockerfiles demands nontrivial reasoning about build lifecycles and dependency separation. This paper presents \tool, an automated refactoring approach that converts single-stage Dockerfiles into optimized multi-stage builds. \tool first performs static analysis to identify the technology stack and to infer build-time and runtime dependencies. It then applies a lightweight gate that estimates refactoring benefit from a composite of image bloat, structural inefficiency, and security risk, proceeding only when refactoring is warranted. Finally, it synthesizes a multi-stage Dockerfile that isolates build tooling, copies only the artifacts needed at runtime, and applies production hardening. Evaluated on 521 real-world single-stage projects, \tool successfully produced working multi-stage Dockerfiles for 60.3% of targets. The resulting images were, on average, 52.2% smaller and contained 50.0% fewer high-risk vulnerabilities than the originals, outperforming baselines. \tool lowers the barrier to multi-stage adoption at scale, yielding leaner images with reduced attack surface and improved maintainability. We release the tool, its knowledge assets, and the evaluation dataset to support reproducibility and future research.

## 2. Break to Adapt: Knowledge-Based Updates of Breaking Dependencies in JavaScript

**Authors:** Yifan Xia, Chengwei Liu, Zifan Xie, Lyuye Zhang, Peiyu Liu, Kangjie Lu, Yang Liu, Wenhai Wang, Shouling Ji

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808116

**中文总结:** 提出 BDUpdater，从 JavaScript 库仓库挖掘并结构化 breaking change records，定位受影响客户端代码并在无编译反馈下引导 LLM 迁移；在 13 个流行库与 84 个客户端上恢复 90.5% 的破坏性依赖更新，语义高度接近开发者改写，平均每客户端成本约 $0.05。

**Abstract:** Modern software libraries continually evolve to maintain activeness, improve performance, and enhance security. This evolution frequently introduces major version updates that include incompatible modifications (breaking changes), which often cause downstream projects to fail and significantly increase the effort required for maintenance. To reduce this burden on developers, recent studies propose automated approaches that leverage API characterization techniques and compilation error reports to guide LLM-based updates. However, these methods rely on static typing and compilation feedback, which are not available in dynamic languages such as JavaScript. As a result, when applied to JavaScript, they degrade to a knowledge-free setting and cannot effectively support automated dependency updates. In this paper, we propose a knowledge-based approach that mines explicit update knowledge, referred to as breaking change records, from library repositories to support automated dependency updates in the presence of breaking changes (i.e., breaking dependency updates). We first conduct an empirical investigation of how breaking change records are maintained in top-ranked JavaScript libraries. Our study reveals that 83.8% of libraries maintain such records within their repositories, often spread across multiple locations. However, the quality of these records varies considerably, with issues such as implicit references to changed objects and vague adaptation instructions. To address this issue, we systematically characterize breaking change records by identifying recurring patterns in both their locations and the types of information they convey. Building on these insights, we develop BDUpdater, an agent-based framework that aggregates repository sources and refines raw records into structured breaking change lists, thereby mitigating the absence of API differencing tools. Leveraging this mined knowledge, BDUpdater pinpoints changed objects and statically identifies the affected client code, while supplying fine-grained change information to LLMs to guide accurate client code migration in the absence of compilation error messages. Our evaluation on 13 popular JavaScript libraries and 84 clients shows that BDUpdater recovers 90.5% of the breaking dependency updates with high semantic equivalence to developer-authored adaptations, while incurring an average cost of only $0.05 per client.

## 3. Bringing Managed Language Support to WebAssembly with External Library Linking

**Authors:** Shuyao Jiang (The Chinese University of Hong Kong), Ruiying Zeng (Fudan University), Yangfan Zhou (Fudan University), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808182

**中文总结:** 提出 WALL-E，以客户端—服务器式外部库链接将托管语言库在原生运行时接入 Wasm，避免双层虚拟机嵌套或重编译；无需改框架即可支持十种托管语言，较运行时嵌套方案加速达数百倍且通信开销低。

**Abstract:** WebAssembly (Wasm) has emerged as a powerful bytecode format for running applications with near-native performance in portable and secure environments. However, while Wasm currently supports compiled languages like C, C++, and Rust, it lacks robust support for managed languages such as Python, Java, and JavaScript. This limitation hinders the deployment of applications in domains like machine learning and data processing that rely heavily on managed language ecosystems. To address this, we propose WALL-E, a novel framework to integrate managed languages into Wasm environments without complex runtime nesting or recompilation. WALL-E employs a unique external library linking strategy, using a client-server architecture to connect Wasm modules with managed language libraries running in their native runtimes. This approach preserves the native execution speed and language feature compatibility of managed languages by eliminating the overhead associated with double-layer virtual machines. Our evaluation shows that WALL-E supports ten managed languages without framework modifications and achieves a speedup of hundreds of times over the runtime nesting solution, with low communication overhead. WALL-E enhances the practicality of Wasm in cloud and edge computing, enabling efficient multi-language applications.

## 4. Co-Evolution of Types and Dependencies: Towards Repository-Level Type Inference for Python Code

**Authors:** Shuo Sun (Institute of Software, Chinese Academy of Sciences), Shixin Zhang (Institute of Software, Chinese Academy of Sciences), Jiwei Yan (Institute of Software at Chinese Academy of Sciences), Jun Yan (Institute of Software, Chinese Academy of Sciences), Jian Zhang (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797103

**中文总结:** 提出 PyTIR，用实体依赖图（EDG）建模仓库级类型依赖并迭代共演化类型与依赖，结合类型检查器在环校正；在 12 个复杂 Python 仓库上 TypeSim/TypeExact 达 0.89/0.84，并消除工具引入的新类型错误 92.7%。

**Abstract:** Python’s dynamic typing mechanism, while promoting flexibility, is a significant source of runtime type errors that plague large-scale software, which inspires the automatic type inference techniques. Existing type inference tools have achieved advances in type inference within isolated code snippets. However, repository-level type inference remains a significant challenge, primarily due to the complex inter-procedural dependencies that are difficult to model and resolve. To fill this gap, we present PyTIR, a novel approach based on LLMs that achieves repository-level type inference through the co-evolution of types and dependencies. PyTIR constructs an Entity Dependency Graph (EDG) to model the objects and type dependencies across the repository. During the inference process, it iteratively refines types and dependencies in EDG for accurate type inference. Our key innovations are: (1) an EDG model designed to capture repository-level type dependencies; (2) an iterative type inference approach where types and dependencies co-evolve in each iteration; and (3) a type-checker-in-the-loop strategy that validates and corrects inferences on-the-fly, thereby reducing error propagation. When evaluated on 12 complex Python repositories,PyTIR significantly outperformed prior works, achieving a \textit{TypeSim} score of 0.89 and a \textit{TypeExact} score of 0.84, representing a 27% and 40% relative improvement over the strongest baseline. More importantly, PyTIR removed new type errors introduced by the tool by 92.7%. This demonstrates a significant leap towards automated, reliable type annotation for real-world Python development.

## 5. Deployability-Centric Infrastructure-as-Code Generation: Fail, Learn, Refine, and Succeed through LLM-Empowered DevOps Simulation

**Authors:** Tianyi Zhang (Australian National University), Shidong pan (New York University), zejun zhang (Nanjing University), Zhenchang Xing (CSIRO's Data61), xiaoyu sun (The Australian National University)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797142

**中文总结:** 构建面向可部署性的 DPIaC-Eval（153 场景/58 服务）并提出 IaCGen，经格式/语法/实部署迭代反馈生成 IaC；使首试部署成功率从约 20–30% 提升至 10 轮内 54.6–91.6%，但意图对齐与安全合规仍偏低。

**Abstract:** Infrastructure-as-Code (IaC) generation holds significant promise for automating cloud infrastructure provisioning. Recent advances in Large Language Models (LLMs) present a promising opportunity to democratize IaC development by generating deployable infrastructure templates from natural language descriptions. However, current evaluation focuses on syntactic correctness while ignoring deployability, the critical measure of the utility of IaC configuration files. Six state-of-the-art LLMs performed poorly on deployability, achieving only 20.8$\sim$30.2% deployment success rate on the first attempt. In this paper, we construct DPIaC-Eval, the first deployability-centric IaC template benchmark consists of 153 real-world scenarios cross 58 unique services. Also, we propose an LLM-based deployability-centric framework, dubbed IaCGen, that uses iterative feedback mechanism encompassing format verification, syntax checking, and live deployment stages, thereby closely mirroring the real DevOps workflows. Results show that IaCGen can makes all evaluated models reach 54.6$\sim$91.6% in 10 iterations. Additionally, human-in-the-loop feedback that provide direct guidance for the deployability errors, can further boost the performance to over 90% passItr@25 on all evaluated LLMs. Furthermore, we explore the trustworthiness of the generated IaC templates on user intent alignment and security compliance. The poor performance (25.2% user requirement coverage and 8.4% security compliance rate) indicates a critical need for continued research in this domain.

## 6. GAER: Graph Auto-Encoders for Unsupervised Software Architecture Recovery

**Authors:** Rakhshanda Jabeen (Electrolux Professional), Morgan Ericsson (Linnaeus University), Jonas Nordqvist (Linnaeus University), Anna Wingkvist (Linnaeus University)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808187

**中文总结:** 提出 GAER，将软件建模为异构依赖图并用图自编码器无监督恢复模块架构，融合结构依赖与文件夹/代码语义特征；在十个有真值架构的开源系统上平均较 SOTA 提升约 30% 的恢复准确度。

**Abstract:** Recovering the modular architecture of software systems from source code is a longstanding challenge, especially when documentation is incomplete or outdated. Manual recovery is labor-intensive, error-prone, and does not scale to large systems. While automated approaches have been proposed, many rely on handcrafted heuristics or focus narrowly on either structural or semantic information, which limits their ability to capture the full range of architectural signals.

We introduce GAER, an unsupervised architecture recovery approach based on graph auto-encoders (GAEs) that frames architecture recovery as a representation learning problem. Software systems are modeled as heterogeneous graphs with typed dependencies, while folder hierarchies and code semantics are incorporated as node features. We evaluate two encoder variants, GAT and GCN, and find that GAT generally yields more accurate and stable decompositions. Experiments on ten open-source systems with ground-truth architectures show that GAER improves recovery accuracy by about 30% on average across evaluation metrics compared to a state-of-the-art method. By automatically deriving architectural views that integrate multiple signals, GAER reduces the manual effort required to maintain architectural documentation and supports more effective system understanding.

## 7. Small is Beautiful: A Practical and Efficient Log Parsing Framework

**Authors:** Minxing Wang (Singapore Management University), Yintong Huo (Singapore Management University, Singapore)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797145

**中文总结:** 提出 EFParser，面向小规模 LLM 的无监督日志解析框架，以双缓存自适应更新与校正模块抑制冗余模板与错误注入；在大规模公开数据集上相对 SOTA 平均提升 12.5%，甚至超越部分大模型基线且保持高效。

**Abstract:** Log parsing is a fundamental step in log analysis, partitioning raw logs into constant templates and dynamic variables. While recent semantic-based parsers leveraging Large Language Models (LLMs) exhibit superior generalizability over traditional syntax-based methods, their effectiveness is heavily contingent on model scale. This dependency leads to significant performance collapse when employing smaller, more resource-efficient LLMs. Such degradation creates a major barrier to real-world adoption, where data privacy requirements and computational constraints necessitate the use of succinct models. To bridge this gap, we propose EFParser, an unsupervised LLM-based log parser designed to enhance the capabilities of smaller models through systematic architectural innovation. EFParser introduces a dual-cache system with an adaptive updating mechanism that distinguishes between novel patterns and variations of existing templates. This allows the parser to merge redundant templates and rectify prior errors, maintaining cache consistency. Furthermore, a dedicated correction module acts as a gatekeeper, validating and refining every LLM-generated template before caching to prevent error injection. Empirical evaluations on public large-scale datasets demonstrate that EFParser outperforms state-of-the-art baselines by an average of 12.5% across all metrics when running on smaller LLMs, even surpassing some baselines utilizing large-scale models. Despite its additional validation steps, EFParser maintains high computational efficiency, offering a robust and practical solution for real-world log analysis deployment.

## 8. Understanding the Limitations of C/C++ Binary Third-Party Library Detection Tool: An Empirical Study at Scale

**Authors:** CHENGYUE LIU, Zhengzi Xu (Imperial Global Singapore), Kaixuan Li (Nanyang Technological University), Wu Jiahui (Nanyang Technological University, Singapore), Sihao Qiu (Institute of Information Engineering Chinese Academy of Sciences & University of Chinese Academy of Sciences, China), Siyuan Li (University of Chinese Academy of Sciences & Institute of Information Engineering Chinese Academy of Sciences, China), Siyang Xiong (Desay SV Automotive Singapore Pte. Ltd.), Yang Xiao (Chinese Academy of Sciences), Yang Liu (Nanyang Technological University)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808096

**中文总结:** 构建迄今最大公开二进制 SCA 基准（38,228 用例、1,873 库）并系统评估 11 款工具；平均召回低于 60%、精确率约 75%，特征级分析揭示编译丢特征与库间高重叠是根本障碍，并给出设计与实践建议。

**Abstract:** Detecting third-party libraries (TPLs) in C/C++ binaries is essential for ensuring software security and compliance, particularly in safety- and performance-critical domains. While numerous academic and commercial Software Composition Analysis (SCA) tools have been proposed, their true capabilities remain unclear due to the absence of large-scale benchmarks and systematic evaluation. Equally lacking is a deeper understanding of why these tools often underperform, which limits both research progress and practical adoption.

We address this gap with a large-scale study of binary SCA tools. We construct the largest publicly available benchmark to date, encompassing 38,228 test cases across 1,873 libraries drawn from a defined scope of 13,675 libraries. Using this benchmark, we systematically evaluate 11 representative tools, covering all open source research prototypes and widely adopted commercial solutions, across versions, architectures, and feature-database scales. Beyond aggregate performance metrics, we perform the first fine-grained, feature-level analysis to identify the intrinsic challenges of binary TPL detection. Our results show that existing tools perform unsatisfactorily, with average recall below 60% and precision around 75%. Feature-level analysis reveals fundamental obstacles: binaries lose most source-code features during compilation, and libraries exhibit high feature overlap due to functional similarity and dependency propagation. These findings explain current shortcomings, and we build on them to provide design recommendations, research directions, and practical guidance for managing open-source risks in binary software.
