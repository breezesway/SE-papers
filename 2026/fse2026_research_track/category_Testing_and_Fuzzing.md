# FSE 2026 Research Track — Testing and Fuzzing

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 43 papers

## 1. A Tuple-Oriented Sampling Method for Generating Small Pairwise Covering Arrays in Configurable Software Systems

**Authors:** Kaichen Chen (South China University of Technology), Yi Xiang (South China University of Technology), Haining Wang (South China University of Technology), Jiatong Ma (South China University of Technology), Fujian Feng (Guizhou Minzu University), Miqing Li (University of Birmingham), Han Huang (Sun Yat-Sen University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808176

**中文总结:** 提出 DivSampCA，以元组导向自适应采样提升配置多样性，并用全覆盖策略用尽量少的配置覆盖剩余 pairwise 元组；在 121 个可配置系统实例上，71% 达到最小覆盖阵列（平均小 15.54%），65% 最快（平均时间降 42.36%）。

**Abstract:** Pairwise testing is the most commonly used combinatorial interaction testing (CIT) technique to verify highly configurable systems, aiming to select the minimum number of testing configurations to cover all valid pairwise combinations of option values. The core problem of pairwise testing is the pairwise covering array generation (PCAG) problem. Existing PCAG methods typically struggle to generate small-scale pairwise covering arrays (PCA) for instances with complex constraints, or they require excessive computational time. To address these limitations, we propose \textit{DivSampCA}, which employs a tuple-oriented adaptive sampling technique to enhance the diversity of the sampled configurations. Moreover, \textit{DivSampCA} employs a novel full coverage strategy to ensure that the remaining uncovered pairwise tuples are covered with as few configurations as possible. We validate our method on 121 publicly available configurable system instances, and the experimental results show that \textit{DivSampCA} achieves the smallest covering array in 71% of the instances, which is on average 15.54% smaller than that of other algorithms. Moreover, it is the fastest in 65% of the instances, reducing the average time by 42.36%. These results indicate that \textit{DivSampCA} can generate smaller covering arrays in a shorter time and represents a significant advancement in solving the PCAG problem.

## 2. ACME: Automated Clause Mapping Engine for Testing Emerging Database Systems

**Authors:** Yuancheng Jiang (National University of Singapore), Jianing Wang (Shandong University), Chuqi Zhang (National University of Singapore), Roland H. C. Yap (National University of Singapore), Zhenkai Liang (National University of Singapore), Manuel Rigger (National University of Singapore)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797134

**中文总结:** 提出 ACME，借助 LLM 自动发现新兴 SQL-like 数据库与关系型参考库之间的子句映射，经测试查询校验并形式化为 AST 变换后做差分测试；在 4 个新兴数据库上发现 57 个未知缺陷（17 逻辑缺陷、40 内部错误），其中 50 已修复、5 已确认。

**Abstract:** A growing number of emerging database management systems, such as time-series and streaming databases, have been developed to support specialized workloads with enhanced performance and functionality. However, these systems are often less mature than traditional relational databases, making them more prone to logic bugs and internal errors that affect correctness and reliability. To address this, we propose an enhanced differential testing framework designed for emerging SQL-like databases. Our key insight is that many of these systems are conceptually extensions of relational databases, allowing us to uncover bugs by comparing query results with those from more robust relational systems. To bridge the differences in syntax and semantics between emerging and relational databases, we leverage Large Language Models (LLMs) to automate the discovery of supported clauses and generate clause mappings that translate system-specific features into equivalent expressions in SQL. Our approach proceeds in three steps: (i) collecting and analyzing the syntax of clauses supported by both the emerging database system and a relational reference system, (ii) constructing clause mappings via LLMs, validating them through testing queries, and formalizing them into Abstract Syntax Tree (AST) transformations or mapping functions, and (iii) generating semantically equivalent but syntactically varied queries to expand the scope of differential testing. To ensure the reliability of LLM-generated clause mappings, we introduce a testing query mechanism that re-prompts incorrect mappings after runtime verification. We implemented this approach in a tool called ACME and applied it to four widely used emerging database systems, uncovering 57 previously unknown bugs, including 17 logic bugs and 40 internal errors. Of these, 50 have been fixed and 5 confirmed by vendors. Our results demonstrate the practicality and effectiveness of ACME in improving the reliability of emerging database systems through scalable, LLM-assisted differential testing.

## 3. Adaptive Mutation Scheduling with Deep Reinforcement Learning for Smart Contract Fuzzing

**Authors:** Qianqian Pang (zhejang university), Xin Yin (Zhejiang University), Tingting Bi (The University of Melbourne), Lingfeng Bao (Zhejiang University), Chao Ni (Zhejiang University), Xiaohu Yang (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808121

**中文总结:** 提出 FuzzMaster，结合深度强化学习与轻量概率调度，依据覆盖率、调用序列与漏洞信号动态优先高影响变异；在 VeriSmart/SmartBugs 上检测率 66.2%（精度 100%），并在真实 Ethereum 合约中发现 97 个、覆盖 6 类漏洞。

**Abstract:** Smart contracts underpin a wide range of decentralized applications—from financial services to supply-chain management—but their immutability and direct control of assets magnify the impact of any security bugs. Although many fuzz approaches have been proposed and have demonstrated their effectiveness in uncovering vulnerabilities, existing methods often rely on unguided random mutation scheduling, generate redundant inputs, and fail to adapt to smart contract-specific characteristics. To overcome these challenges, we present FuzzMaster, a feedback-driven fuzzing framework that combines deep reinforcement learning (DRL) with lightweight probabilistic scheduling to steer mutation selection at runtime intelligently. By continuously analyzing execution feedback—code coverage, function-call sequences, and vulnerability signals—FuzzMaster’s DRL agent and probabilistic tables prioritize high-impact mutations and avoid wasted effort on redundant seeds. On standard VeriSmart and SmartBugs benchmarks, FuzzMaster achieves a 66.2% detection rate with 100% precision (versus 46.9% for ItyFuzz and 43.1% for Confuzzius) and uncovers most bugs within the first second of execution. Meanwhile, in real-world Ethereum contracts, FuzzMaster identified 97 vulnerabilities in 6 categories. These results demonstrate that dynamic, vulnerability-aware mutation scheduling can dramatically improve both the efficiency and effectiveness of smart contract fuzz testing.

## 4. An Empirical Study of Fuzz Harness Degradation

**Authors:** Philipp Görz (Ruhr-University Bochum), Joschua Schilling (CISPA Helmholtz Center for Information Security), Nicolai Bissantz (Ruhr-University Bochum), Thorsten Holz (Max Planck Institute for Security and Privacy)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808172

**中文总结:** 对 OSS-Fuzz 中 510 个 C/C++ 项目的 fuzz harness 开展实证研究，发现整体覆盖与找 bug 能力衰减有限且在可持续构建时仍具持久性，同时系统归类退化根因；并为 OSS-Fuzz/Fuzz Introspector 增加自动检测 harness 退化的新指标。

**Abstract:** Fuzzing is a widely used technique to automatically test software for potential faults. To fuzz software projects efficiently and effectively, they must use fuzz harnesses , i.e., small programs that connect the fuzzer to the project’s code under test. However, as projects evolve, it is unclear whether fuzz harnesses are maintained in lockstep or left to stagnate, and whether unmaintained fuzz harnesses gradually degrade in terms of code coverage and bug-finding effectiveness.

In this paper, we focus on OSS-Fuzz, the largest continuous fuzzing platform in practice, which provides harnesses for 510 open-source C/C++ projects, many of them security-critical. These harnesses are usually contributed by project maintainers or external developers, yet their ongoing maintenance is not always ensured. Our analysis shows that, overall, harnesses exhibit only a small reduction in coverage and retain surprising longevity in their ability to uncover bugs. This holds even without explicit updates, as long as they continue to build.  At the same time, we identify specific cases where harnesses degrade, analyze their root causes, and categorize them systematically. Finally, we extend OSS-Fuzz and Fuzz Introspector, a companion project to investigate fuzzer performance, with new metrics to automatically detect harness degradation, enabling more effective monitoring of fuzzing quality in evolving projects.

## 5. Automated Knowledge-Aware Test Reuse

**Authors:** Ziyuan Zhang (Zhejiang University), Yi Gao (Zhejiang University), Xing Hu (Zhejiang University), Xin Xia (Zhejiang University), Shanping Li (The State Key Laboratory of Blockchain and Data Security, Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808146

**中文总结:** 提出 KATRER，将库建模为融合语义与结构的异构图并用 Test Fingerprint 对齐 API，经协同 LLM 流水线做语义兼容校验与逐步替换以实现跨库测试复用；在两领域五库生成大量子测试，语法正确性与执行成功率较基线提升 17.46%，并在 CuPy/cuML 发现 22 个未知缺陷（8 已修复）。

**Abstract:** The quality of foundational libraries is critical for the reliability of modern software ecosystems. However, developers often have insufficient time for testing due to various reasons. Recent studies show that 68% of deep learning libraries lack unit tests, and their absence negatively impacts libraries health. While automated test generation techniques have been proposed, they frequently produce invalid inputs or semantically inconsistent assertions due to missing domain knowledge. An alternative is cross-library test reuse, as many libraries in scientific computing and machine learning expose functionally similar APIs. Nevertheless, effective test reuse requires careful semantic alignment rather than naive “copy-and-paste”, as subtle API mismatches and incomplete domain knowledge often yield invalid tests. To address these challenges, we present KATRER, a knowledge-aware framework for automated test reuse. KATRER models each library as a heterogeneous graph that integrates semantic and structural information and introduces a Test Fingerprint representation for tests, which captures code, docstrings, usage examples, pre-/post-conditions, and invoked APIs. This enables accurate API alignment and prevents invalid calls. KATRER further employs a collaborative LLM pipeline that verifies semantic compatibility, performs stepwise API substitution, and validates test correctness. We evaluate KATRER among five libraries in two domains, generating 13,191 sub-tests from 1,484 source tests, with 7,257 retained after filtering. KATRER improves syntactic correctness and execution success by 17.46% compared to baselines, while uncovering 22 previously unknown defects in CuPy and cuML, 8 of which have already been fixed. These results demonstrate that knowledge-aware test reuse substantially reduces manual adaptation effort and enhances the robustness of widely used libraries.

## 6. Binvariants: Enhancing Fuzzing of Closed-source Binary Executables via Register-level Likely Invariants

**Authors:** Zao Yang (University of Utah), Stefan Nagy (University of Utah)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797078

**中文总结:** 提出 Binvariants，首次将寄存器级 likely data invariants 引入仅二进制 fuzzing，从 CPU 寄存器状态挖掘不变量并以违反信号引导探索；在 25 个基准上相对仅覆盖引导触发超 27× 独特不变量违反、平均多覆盖 52% 代码区域，并发现 143 个缺陷（含覆盖方法漏掉的 20 个）。

**Abstract:** Closed-source software is ubiquitous in everyday computing, underscoring the need for robust security vetting of “binary-only” executable code. While code-coverage-guided fuzzing has long proven effective at unearthing software bugs, fuzzing in open-source contexts has since evolved beyond code coverage as its principal guiding metric. State-of-the-art fuzzing advancements demonstrate that likely data invariants—data-level properties which, if violated, expose unusual and often bug-preceding program states—significantly widen fuzzing’s reach to defects ordinarily occluded by coverage-only testing. Unfortunately, current invariant-guided fuzzing universally depends on source-level abstractions, rendering it unportable to binary-only targets. Consequently, closed-source software fuzzing—and more importantly, binary-only bug discovery—remain stalled at now-obsolete coverage-only techniques, even as open-source software fuzzing advances well past them.

To bridge this longstanding gap, this paper introduces register-level likely invariants: the first technique to integrate likely data invariants within binary-only fuzzing. In contrast to contemporary source-level data invariant mining, our approach operates directly on CPU registers, capturing the low-level program states that themselves encode higher-level data relationships. From these low-level states, we automatically derive likely data invariants and expose their violations as fuzzer-observable signals via runtime instrumentation, steering fuzzing into states often unreachable by code coverage alone. In doing so, our approach surfaces qualitatively different states, complementing traditional coverage-guided fuzzing with distinct bug-finding capabilities.

We implement our approach as a prototype, Binvariants, and evaluate its performance across 25 benchmark applications: 7 closed-source, as well as 18 open-source programs compiled as binary-only executables. Our results show that, compared to driving binary fuzzing solely via code coverage, register-level likely invariants helps fuzzing trigger over 27× more unique invariant violations beyond coverage-only fuzzing, thereby exercising a mean 52% more distinct code regions. Moreover, our approach uncovers 143 total bugs versus coverage-only fuzzing’s 137—including 20 missed by code coverage—demonstrating how register-level likely invariants extends binary-only fuzzing’s reach into execution states beyond what coverage alone is capable of.

## 7. Can Old Tests do New Tricks for Resolving SWE Issues?

**Authors:** Yang Chen (University of Illinois at Urbana-Champaign), Toufique Ahmed (IBM), Reyhaneh Jabbarvand (University of Illinois at Urbana-Champaign), Martin Hirzel (IBM Research)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808148

**中文总结:** 提出 TestLoc，利用 issue 报告并将回归测试最小化到高相关子集，以增强复现测试生成与补丁验证；可插入任意 agentic 修复流水线，在 SWE-Bench Lite/Verified 上使 Otter 复现率相对提升 6.2%–9.0%、Agentless 解决率相对提升 9.4%–12.9%，且每实例额外成本极低。

**Abstract:** Test suites in real-world projects are often large and achieve high code coverage, yet they remain insufficient for detecting all bugs. The abundance of unresolved issues in open-source project trackers highlights this gap. While regression tests are typically designed to ensure past functionality is preserved in the new version, they can also serve a complementary purpose: debugging the current version. Specifically, regression tests can (1) enhance the generation of reproduction tests for newly reported issues, and (2) validate that patches do not regress existing functionality. We present TestLoc, a fully automated technique that leverages issue tracker reports and strategically reuses regression tests for both bug reproduction and patch validation.

A key contribution of TestLoc is its ability to automatically minimize the regression suite to a small, highly relevant subset of tests. Due to the predominance of LLM-based debugging techniques, this minimization is essential as large test suites exceed context limits, introduce noise, and inflate inference costs. TestLoc can be plugged into any agentic bug repair pipeline and orthogonally improve overall performance. As a proof of concept, we show that TestLoc leads to a $6.2%-9.0%$ relative increase in issue reproduction rate within the Otter framework and a $9.4%-12.9%$ relative increase in issue resolution rate within the Agentless framework on SWE-Bench Lite and SWE-Bench Verified benchmarks, capturing fixes that were correctly produced by agents but not submitted as final patches. Compared to the benefits, the cost overhead of using TestLoc is minimal, i.e., $0.02 and $0.05 per SWE-Bench instance, using GPT-4o and Claude-3.7-Sonnet models, respectively.

## 8. CASCADE: Detecting Inconsistencies between Code and Documentation with Automatic Test Generation

**Authors:** Tobias Kiecker (Humboldt-Universität zu Berlin), Jan Arne Sparka (Humboldt-Universität zu Berlin), Martin Reuter (Humboldt-Universität zu Berlin), Albert Ziegler (XBow), Lars Grunske (Humboldt-Universität zu Berlin)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808175

**中文总结:** 提出 CASCADE：用 LLM 从文档生成单测，并仅在「现有代码失败且由文档生成的代码通过同一测试」时报告文档-代码不一致以降低误报；在多语言开源仓库中发现 12 个未知不一致，其中 8 个已被维护者修复。

**Abstract:** Maintaining consistency between code and documentation is a crucial yet frequently overlooked aspect of software development. Even minor mismatches can confuse API users, introduce new bugs, and increase overall maintenance effort. This creates demand for automated solutions that can assist developers in identifying code-documentation inconsistencies. However, since automatic reports still require human confirmation, false positives carry serious consequences: wasting developer time and discouraging practical adoption.

We introduce CASCADE (Consistency Analysis for Source Code And Documentation through Execution), a novel tool for detecting inconsistencies with a strong emphasis on reducing false positives. CASCADE leverages Large Language Models (LLMs) to generate unit tests directly from natural-language documentation. Since these tests are derived from the documentation, any failure during execution indicates a potential mismatch between the documented and actual behavior of the code. To minimize false positives, CASCADE also generates code from the documentation to cross-check the generated tests. By design, an inconsistency is reported only when two conditions are met: the existing code fails the test, while the code generated from the documentation passes the same test.

We evaluated CASCADE on a novel dataset of inconsistent and consistent code-documentation pairs drawn from open-source Java projects. Further, we applied CASCADE to additional Java, C#, and Rust repositories, where we uncovered 12 previously unknown inconsistencies, of which 8 have subsequently been fixed by maintainers, demonstrating both CASCADE’s precision and its applicability to real-world codebases.

## 9. ChainDelta: Automatic Patch-based Exploit Generation for Ethereum with Fuzzing Agents

**Authors:** Mingxi Ye (Sun Yat-sen University), Yuhong Nan (Sun Yat-sen University), Zhijie Zhong (School of Software Engineering, Sun Yat-sen University), Jianzhong Su (Sun Yat-sen University), Xingwei Lin (Zhejiang University), Peilin Zheng (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808157

**中文总结:** 提出 ChainDelta，结合导向模糊测试、智能体环境配置与状态感知差分消毒，基于以太坊安全补丁自动生成利用；在真实补丁基准上成功率 70%、误报率 12.5%，并在实战审计中发现 4 个未公开漏洞并获赏金。

**Abstract:** Given the critical nature of Ethereum, exploiting 1-day vulnerabilities that are patched but not yet widely deployed is essential. Meanwhile, Automatic Patch-based Exploit Generation (APEG) is a promising technique for this, as it helps developers understand root causes, verify fixes in downstream forks, and detect incomplete patches. However, existing exploit generation tools can not work well for vulnerabilities on Ethereum due to three key unique challenges: (1) navigating complex and cross-language exploit paths hidden within patches, (2) synthesizing complicated and stateful environment configurations, and (3) handling non-deterministic inconsistencies between blockchain nodes that lead to false alarms.

To address these challenges, we introduce \textit{ChainDelta}, a novel fuzzing agent framework driven by Large Language Models to automatically generate exploits based on Ethereum security patches. \textit{ChainDelta} consists of three core modules: a directed fuzzer utilizes call graph analysis to guide testing towards vulnerable code based on the patch information; an agent-based environment fuzzer acts as an expert to automatically set up the necessary blockchain states to trigger vulnerabilities; and finally, a state-aware sanitizer performs differential analysis while monitoring the blockchain transient state to distinguish true inconsistencies from benign non-determinism.

We evaluate \textit{ChainDelta} on a diverse benchmark with real-world vulnerability patches, covering a wide range of types such as data racing and denial-of-service. \textit{ChainDelta} successfully generated exploits with a 70% success rate and only a 12.5% false positive rate. An ablation study confirms the contribution of each module to the overall performance. To demonstrate its practical impacts, we conducted a real-world auditing campaign on top of \textit{ChainDelta}, leading to the discovery of four previously undisclosed vulnerabilities with bug bounties.

## 10. Clotho: Measuring Task-Specific Pre-Generation Test Adequacy for LLM Inputs

**Authors:** Juyeon Yoon (Korea Advanced Institute of Science and Technology), Somin Kim (Korea Advanced Institute of Science and Technology), Robert Feldt (Chalmers | University of Gothenburg), Shin Yoo (KAIST)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797114

**中文总结:** 提出 Clotho，利用隐藏状态与 GMM 在生成前估计任务相关输入难度并优先标注参考集；平均仅标注 5.4% 输入即可达 ROC-AUC 0.716，且开源模型学到的充分性可迁移到专有模型，使 top-100 暴露失败数提升约 126.8%。

**Abstract:** Software increasingly relies on the emergent capabilities of Large Language Models (LLMs), from natural language understanding to program analysis and generation. Yet testing them on specific tasks remains difficult and costly: many prompts lack ground truth, forcing reliance on human judgment, while existing uncertainty and adequacy measures typically require full inference. A key challenge is to assess input adequacy in a way that reflects the demands of the task, ideally before even generating any output. We introduce Clotho, a task-specific, pre-generation adequacy measure that estimates input difficulty directly from hidden LLM states. Given a large pool of unlabelled inputs for a specific task, Clotho uses a Gaussian Mixture Model (GMM) to adaptively sample the most informative cases for human labelling. Based on this reference set the GMM can then rank unseen inputs by their likelihood of failure. In our empirical evaluation across eight benchmark tasks and three open-weight LLMs, Clotho can predict failures with a ROC-AUC of 0.716, after labelling reference sets that are on average only 5.4% of inputs. It does so without generating any outputs, thereby reducing costs compared to existing uncertainty measures. Comparison of Clotho and post-generation uncertainty measures shows that the two approaches complement each other. Crucially, we show that adequacy scores learned from open-weight LLMs transfer effectively to proprietary models, extending the applicability of the approach. When prioritising test inputs for proprietary models, Clotho reveals 126.8% more failures, on average, in the top 100 inputs compared to random selection.

## 11. Cost-Effective Testing of MPC Compilers

**Authors:** Sebastian Watzinger (TU Wien), Valentin Wüstholz (ConsenSys), Deepak Garg (MPI-SWS), Maria Christakis (TU Wien)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808206

**中文总结:** 提出 BabelFuzz，用表达力强的中间表示生成种子程序并翻译到主流语言做差分测试，低成本覆盖多种 MPC 编译器；在四个编译器上发现 24 个新逻辑缺陷，并可复现先前工作已修复的全部缺陷。

**Abstract:** Secure multi-party computation (MPC) enables privacy-preserving computations using secret data, with applications ranging from health care and finance to machine learning and blockchains. MPC compilers translate high-level function descriptions to the low-level representations required for the actual execution, making them critical for both usability and scalability of MPC. However, these compilers may contain logic bugs that cause them to quietly produce wrong outputs, the consequences of which could be catastrophic given the sensitive applications of this technology. Testing MPC compilers in order to find these severe bugs is, therefore, paramount.

With only a single testing tool currently available (which is not publicly available in its entirety and has several serious limitations), this issue is far from resolved. In this paper, we present BabelFuzz, a cost-effective framework for testing MPC compilers. By introducing an expressive intermediate representation (IR) for its seed-program generation, BabelFuzz is able to support multiple compilers that use different input languages, while keeping the development effort of adding new targets low. Even better, this approach allows us to translate our IR to mainstream languages, which provides a powerful differential-testing oracle for highly efficient bug detection.

BabelFuzz not only found 24 new logic bugs across four MPC compilers, but it is also able to rediscover every fixed bug the previous state of the art in testing MPC compilers found.

## 12. Cross-Refactoring-Type Test Program Migration for Refactoring Engines

**Authors:** Chunhao Dong (Beijing Institute of Technology), Yanjie Jiang (Tianjin University), Yang Zhang (Hebei University of Science and Technology), Yuxia Zhang (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808151

**中文总结:** 提出 EngineTest，利用其他重构类型的缺陷报告与 LLM 迁移生成目标重构的测试程序，并结合差分测试与 LLM 不一致检查；在 Eclipse/NetBeans/IntelliJ IDEA 上发现 77 个未知缺陷，其中 30 个获厂商确认。

**Abstract:** Refactoring engines are an essential part of modern IDEs, supporting automated or semi-automated software refactorings. However, these refactoring engines suffer from software defects, just like other complex software systems, and buggy refactoring engines may silently inject fatal errors into software projects.  Consequently, thorough testing of refactoring engines is highly desirable. To this end, this paper proposes an automated approach called \textit{EngineTest} to test Java refactoring engines. Unlike existing approaches, it is the first in this line to leverage both LLMs and bug reports of refactoring types other than the targeted refactoring type. The key rationale is that the same mistake, e.g., ignoring the potential \textit{name shadowing}, may result in similar errors in multiple refactoring types.  Consequently, we may retrieve a bug report for a refactoring type, leverage LLMs to figure out the underlying reason, and request LLMs to generate test programs for other types of refactorings.  Finally, we run the test cases and validate them with differential testing and LLM-based inconsistent checking. We evaluate the proposed approach with widely used state-of-the-practice refactoring engines in Eclipse, NetBeans, and IntelliJ IDEA. Our evaluation results demonstrate that a total of 77 previously unknown bugs have been identified, and 30 of them have been manually confirmed by the tool vendors.

## 13. CuFuzz: An API-Knowledge-Graph Coverage-Driven Fuzzing Framework for CUDA Libraries

**Authors:** Ximing Fan (School of cyber science and engineering, Sichuan University, China), Yong Fang (Sichuan University), Peng Jia (Sichuan University), Yang Liu (Nanyang Technological University), Yijia Xu (Sichuan University), Xi Peng (Huawei Theory Lab), Yuhao Zhou (Fudan University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808170

**中文总结:** 提出 CuFuzz，从文档构建 API 知识图并以覆盖位图引导 harness 生成与参数解耦变异，面向 CUDA 库模糊测试；相对 Fuzz4all 平均 API 覆盖与边覆盖分别提升约 2.97×/4.0×，发现 4 个未知缺陷并获 2 个 CVE。

**Abstract:** In the AI-driven era, NVIDIA CUDA libraries have become indispensable for accelerating compute-intensive tasks, yet their security assessment remains critically understudied due to closed-source code and unique programming paradigms. Existing efforts primarily target CUDA compiler vulnerabilities (e.g., NVCC), but overlook broader library-specific risks. This paper addresses the challenges of fuzzing CUDA libraries: (1) the absence of guidance narrows the set of APIs that generated harnesses can reach; and (2) input mutation remains inefficient for LLM-generated harnesses.

A new tool called CuFuzz has been proposed, aimed at uncovering potential vulnerabilities in the CUDA libraries. CuFuzz has the ability to generate testing harnesses for various CUDA library functions from scratch, perform efficient parameter mutation, and adapt to the needs of multiple CUDA libraries. First, LLMs are used to extract semantic relationships from CUDA documentation and sample codes, constructing a knowledge graph that prioritizes API interactions and contextual dependencies. The API coverage bitmap is proposed to guide the fuzzer to explore under-tested library functions. In addition to harness generation, the API knowledge graph is also combined with compiler diagnostics to repair erroneous harnesses, thereby improving compilation success rates. Subsequently, CuFuzz employs the LLMs to analyze and decouple parameter dependencies, separates out the mutable parameters, and performs parameter-isolated mutation on them to enhance mutation efficiency.

Evaluated across three CUDA releases (12.4, 12.7, and 13.0) on eight widely adopted libraries (e.g., cuBLAS, cuFFT), CuFuzz achieves 2.97x higher API coverage and 4.0x superior API edge coverage relative to baseline (Fuzz4all), on average. The experiments uncovered 4 unknown bugs, validated by NVIDIA’s security team and obtained 2 CVEs.

## 14. Denoising Fault Localization with Test Line Proximity

**Authors:** Marius Smytzek (CISPA Helmholtz Center for Information Security), Andreas Zeller (CISPA Helmholtz Center for Information Security)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808110

**中文总结:** 提出基于时间邻近性的统计缺陷定位加权：越接近失败执行的语句权重越高，以缓解多断言测试中的歧义相关；在 310 个真实程序上相对基线常见相对提升 200%–400%，并可接入现有 SFL 公式。

**Abstract:** When a program fails, statistical fault localization (SFL) provides important debugging hints by identifying the locations whose execution most correlates with failures. However, such correlations can be weakened if a test contains both passing and failing assertions, creating ambiguous and misleading associations. Likewise, if multiple lines correlate with the same strength, SFL provides little guidance to disambiguate between them.

This paper proposes a novel proximity-based weighting scheme for SFL that assigns different weights to locations in the test subject based on temporal proximity to a failure. The more recently a subject line is executed before the test fails, the higher its weight. We operationalize a known heuristic into a lightweight statistical form compatible with existing SFL formulas. Our approach applies to any test , from simple single-line tests (where it preserves SFL behavior), to single-assertion tests with multiple lines (where it benefits from temporal proximity), to complex multi-assertion tests (where it provides the most benefit by distinguishing failing from passing assertions). Once computed, the weights can be integrated into any existing SFL technique.

Our evaluation of proximity-weighted fault localization on 310~real-world programs shows that it consistently outperforms fault localization techniques across all test types. Proximity-weighted fault localization shows per-subject relative improvements of 200%–400%, meaning that, for a typical subject, it provides 3 to 5 times the baseline effectiveness. These improvements represent substantial gains over baseline techniques. Our approach can be integrated into existing fault localization techniques to improve performance, making it a valuable addition to automated debugging.

## 15. Detecting Bugs in Rust Compiler Fix Suggestions via Constraint-Violation-Guided Mutation

**Authors:** Zixi Liu (Nanjing University), Yang Feng (Nanjing University), Jialiang Jiang (Nanjing University), Baowen Xu (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797128

**中文总结:** 提出 SugBreaker，以约束违反引导变异向合法 Rust 程序注入类型/借用/生命周期错误，触发并迭代验证 rustc 修复建议；已发现 12 个缺陷（11 个确认或已修复），且对核心检查模块覆盖与建议触发率优于基线工具。

**Abstract:** Rust is a modern systems programming language that ensures memory safety through unique mechanisms, including ownership, borrowing, and lifetime annotations. These features prevent critical vulnerabilities but also impose strict constraints that many developers find difficult to understand. To mitigate this challenge, the Rust compiler, rustc, provides rich diagnostics and fix suggestions. However, recent studies reveal that diagnostic issues account for about 20% of all reported rustc bugs. Our analysis of rustc’s suggestion bugs fixed over the past three years shows that most of them originated from errors in Rust-specific core modules, such as the type checker and borrow checker, rather than from simple mistakes in the general diagnostic logic, like suggesting an incorrect variable name or mismatched parentheses. The impact of diagnostic issues, especially bugs in rustc’s fix suggestion, should not be underestimated, as they can mislead developers and reduce rustc’s usability, and in severe cases may even lead to rustc crashes. Existing testing tools, however, provide little support for systematically evaluating the correctness and reliability of these suggestions.

To address this gap, in this paper, we present SugBreaker, an automated testing framework specifically designed to validate rustc’s suggestions. We propose a constraint-violation-guided mutation approach that injects type-related, borrow-related, and lifetime-related errors into valid Rust programs to trigger compiler diagnostics and iteratively verify the correctness of suggested fixes. SugBreaker has already detected 12 bugs, and 11 of them have been confirmed or fixed; all of them are triggered by different rustc error messages. Compared with a series of rustc testing baseline tools, SugBreaker achieves broader coverage of rustc’s core checking modules and a higher suggestion trigger rate, which further confirms the effectiveness and efficiency of SugBreaker for testing rustc’s fix suggestions.

## 16. Eidolon: Perform Noise-Aware Fuzzing on FHE Libraries via Equivalence Expression Transformation

**Authors:** Zhensheng Xian, Zhen Yan, Yuanliang Chen, Xuelian Cao, Fuchen Ma, Dalong Shi, Yu Jiang

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808109

**中文总结:** 提出 Eidolon，面向全同态加密库做噪声预算感知的模糊测试，并以等价表达式变换为预言机检测计算不一致；在 SEAL、OpenFHE、HELib、TFHE 上相对现有加密模糊器显著提升覆盖率，发现 20 个未知缺陷（10 个已修复、12 个获 CVE）。

**Abstract:** Ensuring data privacy during computation is a critical challenge in many security systems. Fully Homomorphic Encryption (FHE) addresses this gap by enabling multiple operations on encrypted data without decryption, thus ensuring privacy is preserved throughout computation. However, existing cryptographic testing tools are unable to test the core functionality of FHE, which is the execution of computations on encrypted data. They are expertly designed to generate structured data for testing cryptographic algorithms. This structural mismatch, combined with a lack of awareness of FHE-specific noise management, leads them to generate invalid test inputs that fail to probe FHE libraries’ core logic.

To address this gap, we propose Eidolon, a noise-aware fuzzer. It directs mutations toward arithmetic expressions that explore the computational space defined by the noise budget. As its test oracle, Eidolon leverages Equivalence Expressions Transformation, which transforms a standard arithmetic expression into two  mathematically identical but structurally different forms (e.g., Factored, Horner) to detect inconsistencies in their outputs. We evaluated Eidolon on SEAL, OpenFHE, HELib, and TFHE. Compared with existing cryptographic fuzzers, Eidolon achieves 39.2%, 61.0%, and 99.0% higher final code coverage than CLFuzz, Cryptofuzz, and CDF, respectively. In total, Eidolon uncovered 20 previously unknown bugs, 10 of which have been fixed and 12 assigned CVEs.

## 17. Empirical Insights of Test Selection Metrics under Multiple Testing Objectives and Distribution Shifts

**Authors:** Jingyu ZHANG (Hong Kong Metropolitan University), Fan Wang (City University of Hong Kong), Jacky Keung (City University of Hong Kong), Yihan Liao (City University of Hong Kong), Yan Xiao (Sun Yat-sen University), Lei Ma (The University of Tokyo & University of Alberta)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797086

**中文总结:** 对 15 种深度学习测试选择指标开展大规模实证研究，覆盖故障检测、性能估计与重训指导三类目标及五类 OOD 与三种模态；共 1640 组实验场景，为多目标、多分布偏移下的指标选用提供统一基准与统计结论。

**Abstract:** Deep learning (DL)-based systems can exhibit unexpected behavior when exposed to out-of-distribution (OOD) scenarios, posing serious risks in safety-critical domains such as malware detection and autonomous driving. This underscores the importance of thoroughly testing such systems before deployment. To this end, researchers have proposed a wide range of test selection metrics designed to effectively select inputs. However, prior evaluations of metrics reveal three key limitations: (1) narrow testing objectives, for example, many studies assess metrics only for fault detection, leaving their effectiveness for performance estimation unclear; (2) limited coverage of OOD scenarios, with natural and label shifts are rarely considered; (3) Biased dataset selection, where most work focuses on image data while other modalities remain underexplored. Consequently, a unified benchmark that examines how these metrics perform under multiple testing objectives, diverse OOD scenarios, and different data modalities is still lacking. This leaves practitioners uncertain about which test selection metrics are most suitable for their specific objectives and contexts. To address this gap, we conduct an extensive empirical study of 15 existing metrics, evaluating them under three testing objectives (fault detection, performance estimation, and retraining guidance), five types of OOD scenarios (corrupted, adversarial, temporal, natural, and label shifts), three data modalities (image, text, and Android packages), and 13 DL models. In total, our study encompasses 1,640 experimental scenarios, offering a comprehensive evaluation and statistical analysis.

## 18. Evaluating LLM-based Regression Test Generation

**Authors:** Jing Liu (Max Planck Institute for Security and Privacy), Seongmin Lee (UCLA), Eleonora Losiouk (University of Padua), Marcel Böhme (MPI for Security and Privacy)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808129

**中文总结:** 将即时回归测试生成视为机器翻译任务，提出反馈引导的零样本原型 Cleverest（及与模糊结合的 ClevFuzz）；在 46 个提交上平均不到 2 分钟即可比 24 小时的 WAFLGo 发现更多缺陷，且 commit message 表达力对效果影响显著。

**Abstract:** Large Language Models (LLMs) have shown tremendous promise in automated software engineering. In this paper, we investigate the opportunities of LLMs for just-in-time regression test generation for programs, like parsers, interpreters, or compilers, that take highly structured, human-readable inputs. When a new bug fix or code change is committed, the repository (as part of the CI/CD workflow) runs an LLM for a few minutes to generate regression test cases for that commit that exercise the changed code and potentially trigger any bugs.

Specifically, we investigate LLM-based regression test generation as a \emph{machine translation task} that takes the developer-provided commit message, the code change, and the name of the input format (e.g., XML) and produces regression test cases for the described change in the given input format. In our experiments testing 46 commits to Mujs, Libxml2, Poppler, JerryScript, Z3, and PHP, our feedback-directed, zero-shot LLM-based prototype Cleverest performed unexpectedly well, even if we did \emph{not} provide the code change. In under 2 minutes, on average, Cleverest found more bugs than the state-of-the-art directed greybox fuzzer WAFLGo in 24 hours, even though WAFLGo started with a commit-reaching seed corpus in the majority of cases. If we amplify the Cleverest-generated test cases using those as a seed corpus in coverage-guided greybox fuzzing, the number of bugs found almost doubles. We call the integration with fuzzing as ClevFuzz .

In addition, we found that some commit messages are more expressive than others, thus we wonder how this impacts the effectiveness of Cleverest. Our results above demonstrate that Cleverest picks up on the change intention. For instance, if the commit message describes that this patch changes how floating point variables are treated in the MuJS JavaScript interpreter, then Cleverest generates JavaScript programs that contain floating point variables. To study the impact of expressiveness, we change the commit messages minimally to reduce and increase the information in the commit message, respectively, and find a substantial impact on effectiveness. For instance, adding 18 words on average (max. 46) to make ineffective commit messages more expressive almost doubled the number of bugs found.

## 19. Failing with Purpose: Dangling Coverage-Guided Negative Test Generation from a Mechanized P4 Type System

**Authors:** Jaehyun Lee (KAIST), Seokhun Jeong (KAIST), Sukyoung Ryu (KAIST)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797109

**中文总结:** 将 P4 类型系统用 SpecTec 形式化，定义 dangling premises 与 dangling coverage，并实现覆盖引导的负向测试模糊器；相对 P4C 套件提升 33.02%p 覆盖，发现 29 个编译器前端未知缺陷且用例已并入官方测试集。

**Abstract:** A type checker must reject ill-typed programs in addition to accepting well-typed programs. Negative type checker tests, programs expected to be rejected, validate that a type checker enforces the language’s typing rules as intended. We focus on negative type checker tests for P4, a domain-specific language for programmable network devices, whose type system encodes design principles and hardware constraints of the network dataplane. Failing to reject an ill-typed P4 program risks violating these principles and constraints, leading to unexpected errors. A comprehensive negative test suite covering subtle and diverse ill-typed conditions is thus important. However, constructing comprehensive negative tests is challenging: the negative input space lacks systematic characterization, and existing P4 program generators do not target subtle type errors.

This paper addresses the problem in three steps. (i) We mechanize the P4 type system using the SpecTec framework. Unlike the informal official P4 specification, the mechanized type system is formal and machine-readable. Mechanization enables a systematic analysis of the type system. (ii) Across the mechanized type system, we identify dangling premises, which are premises in the typing rules that, when violated, cause type errors. Based on them, we propose dangling coverage, a novel metric for quantifying negative test coverage. (iii) Finally, we implement a coverage-guided fuzzer that mutates well-typed P4 programs into ill-typed programs that increase dangling coverage. Our method identifies 939 dangling premises that characterize distinct ill-typed conditions in the P4 type system. The fuzzer generates a negative test suite achieving 33.02%p higher dangling coverage than the existing P4C reference compiler’s test suite. The generated tests also reveal 29 previously unknown bugs in the compiler frontend, demonstrating the effectiveness of both the coverage metric and the fuzzer. The tests generated by our fuzzer are now integrated into the P4C test suite.

## 20. From Particles to Perils: SVGD-Based Hazardous Scenario Generation for Autonomous Driving Systems Testing

**Authors:** Linfeng Liang, Xiao Cheng, Tsong Yueh Chen, Xi Zheng

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808153

**中文总结:** 提出 PtoP，以自适应随机种子结合 SVGD 粒子在高维交通初始条件空间中生成多样高风险场景；作为可插拔框架与在线测试结合，在 CARLA 上相对基线最高提升违规率 27.68%、多样性 9.6%、地图覆盖 16.78%。

**Abstract:** Simulation-based testing of autonomous driving systems (ADS) must reveal realistic, diverse failures that arise from dense traffic and complex interactions among heterogeneous dynamic obejcts (vehicles, cyclists, and pedestrians). The effectiveness of ADS testing is highly sensitive to the choice of initial conditions (seeds). However, existing search-based seeding approaches (e.g., genetic algorithms) struggle in the high-dimensional spaces induced by dense and heterogeneous traffic, collapsing into a limited set of modes and leaving many realistic failure scenarios undiscovered.

We present PtoP, a novel framework for testing autonomous driving systems. At its core, PtoP couples adaptive random seed generation—which produces seeds that hit diverse initial failure modes—with Stein Variational Gradient Descent (SVGD) to explore diverse, failure-inducing initial conditions. Each particle represents the initial state of a dynamic object. SVGD jointly leverages gradient-driven attraction toward high-hazard regions and kernel-mediated repulsion to maintain diversity among particles, producing risk-seeking yet well-distributed seeds that span multiple distinct failure modes. Beyond seed generation, PtoP serves as a plug-and-play framework that integrates seamlessly with online testing techniques (e.g., reinforcement learning–based testers) and, by providing principled seeds, boosts their overall testing effectiveness. We evaluate PtoP in CARLA—a state-of-the-art simulator—on two autonomous driving systems: an industry-grade stack (Apollo) and an end-to-end ADS native to CARLA. When combined with state-of-the-art baselines, PtoP substantially increases the safety-violation rate (by up to 27.68%), scenario diversity (by up to 9.6%), and map coverage (by up to 16.78%) over the baselines. Our framework and all associated data are available at https://anonymous.4open.science/r/PtoP-75B3 .

## 21. From Suspicious Signals to Crashes: Guiding Bug-driven GUI Testing via Code-inspired Tracing

**Authors:** Mengzhuo Chen (Institute of Software, Chinese Academy of Sciences), Zhe Liu (Institute of Software, Chinese Academy of Sciences), Chunyang Chen (TU Munich), Junjie Wang (Institute of Software at Chinese Academy of Sciences), Boyu Wu (Institute of Software at Chinese Academy of Sciences), Yuekai Huang (Institute of Software, Chinese Academy of Sciences), Jun Hu (Institute of Software, Chinese Academy of Sciences), Qing Wang (Institute of Software at Chinese Academy of Sciences)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808158

**中文总结:** 提出 TraceDroid，从崩溃启发式定位可疑代码与 GUI 控件，经 ATG 与 LLM 路径补全生成可疑路径并执行以暴露崩溃；在 70 个真实崩溃上召回率 77%（超最佳基线 28%），并在 Google Play 应用中发现 21 个未知崩溃。

**Abstract:** Mobile applications frequently suffer from crash bugs that are triggered under specific GUI interaction sequences. Existing automated GUI testing techniques mainly emphasize increasing coverage through diverse exploration strategies, but they often fail to reach the precise interaction contexts that lead to crashes, resulting in low bug detection efficiency. This paper proposes TraceDroid, a novel automated GUI testing approach that leverages suspicious code-level signals to guide dynamic exploration. Instead of treating static analysis as an independent detection method, TraceDroid uses heuristic rules distilled from real crash reports to detect suspicious code segments, associate them with GUI widgets, and collect code-level interaction signals. It then constructs the Activity Transition Graph (ATG), performs rough path generation, and employs LLM-based executable path completion to produce a set of suspicious paths. Finally, TraceDroid executes these paths through global path planning, local path generation, and execution-aware monitoring to efficiently expose crashes. We evaluate TraceDroid on 70 real crash bugs across 42 open-source apps, comparing it with 15 state-of-the-art baselines. TraceDroid achieves the best performance, with a recall of 77%, exceeding the best baseline by 28%, while maintaining comparable or higher coverage. Furthermore, TraceDroid successfully detects 21 previously unknown crash bugs in 116 popular Google Play apps, of which 15 have been fixed and 6 confirmed by developers, demonstrating its effectiveness in real-world scenarios.

## 22. Generalizing Test Cases for Comprehensive Test Scenario Coverage

**Authors:** Binhang Qi (National University of Singapore), Yun Lin (Shanghai Jiao Tong University), Xinyi Weng (Shanghai Jiao Tong University), Chenyan Liu (Shanghai Jiao Tong University; National University of Singapore), Hailong Sun (Beihang University), Gordon Fraser (University of Passau), Jin Song Dong (National University of Singapore)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808216

**中文总结:** 提出 TestGeneralizer，从焦点方法与初始测试推断需求并泛化场景模板以生成覆盖更全的测试用例；在 12 个 Java 项目上显著优于 EvoSuite 等基线，现场提交的 27 个用例中 16 个被官方仓库接受。

**Abstract:** Test cases are essential for software development and maintenance. In practice, developers derive multiple test cases from an implicit pattern based on their understanding of requirements and inference of diverse test scenarios, each validating a specific behavior of the focal method. However, producing comprehensive tests is time-consuming and error-prone: many important tests that should have accompanied the initial test are added only after a significant delay, sometimes only after bugs are triggered.

Existing automated test generation techniques largely focus on code coverage. Yet in real projects, practical tests are seldom driven by code coverage alone, since test scenarios do not necessarily align with control-flow branches. Instead, test scenarios originate from requirements, which are often implicitly embedded in a project’s design and implementation. Given a focal method, its underlying requirement can often be inferred from relevant project knowledge and the initial test that reflects the developer’s intent.

In this work, we propose TestGeneralizer, a framework for generalizing test cases to comprehensively cover test scenarios. TestGeneralizer orchestrates three stages: (1) enhancing the understanding of the requirement and scenario behind the focal method and initial test; (2) generating a test scenario template and crystallizing it into various test scenario instances; and (3) generating and refining executable test cases from these instances. To ensure accuracy and completeness, TestGeneralizer combines rule-based prompts, automatically optimized via a prompt auto-tuning technique, with crucial project knowledge retrieved through program analysis.

We evaluate TestGeneralizer against three state-of-the-art baselines (EvoSuite, gpt-o4-mini, and ChatTester) on 12 open-source Java projects, covering 506 multi-test focal methods and 1,637 test scenarios. TestGeneralizer achieves significant improvements: +64.00% and +56.87% over EvoSuite, +34.63% and +29.37% over gpt-o4-mini, and +28.70% and +20.05% over ChatTester, in mutation-based and LLM-assessed scenario coverage, respectively. In a field study, we submitted 27 generalized tests overlooked by developers; 16 were accepted and merged into official repositories, demonstrating the practical usefulness of TestGeneralizer.

## 23. iCoRe: An Iterative Correlation-Aware Retriever for Bug Reproduction Test Generation

**Authors:** JunyiWang (Zhejiang University), Jialun Cao (Hong Kong University of Science and Technology), Zhongxin Liu (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808193

**中文总结:** 提出 iCoRe，面向 bug 复现测试生成做迭代、关联感知的上下文检索，区分源码与测试用例、融合语义与调用关系，并用生成执行反馈 refinement；在 SWT-bench Lite 上 Fail-to-Pass 达 42.0%，相对已有检索方法提升 31.7%。

**Abstract:** Automatically generating bug reproduction tests (BRT) from issue descriptions is crucial for facilitating software maintenance. Large Language Model (LLM)-based approaches have shown great potential for this task. Their effectiveness heavily relies on retrieving high-quality context from the codebase. The retrieval phase of existing approaches relies on either traditional methods like BM25 or modern LLM-driven strategies. The LLM-based retrieval strategies typically involve equipping an LLM with tools to autonomously explore the code repository or having it select the most relevant files and code snippets from a provided list as context. However, these retrieval methods suffer from three key limitations: (1) They often employ a unified strategy for retrieving both source code and test cases, overlooking their distinct retrieval requirements. (2) They focus solely on semantic similarity, ignoring function call relationships that reflect behavioral relevance, which often leads to the retrieval of irrelevant context. (3) The retrieval lacks a feedback loop from the generation phase, preventing it from refining the context based on execution results. These limitations collectively result in low-quality context, thereby hindering the accuracy of bug reproduction. To address these challenges, we propose iCoRe, an iterative, correlation-aware context retrieval approach. iCoRe is explicitly designed to be aware of three key correlations: 1) the correlation between source code and test cases, which requires differentiated retrieval, 2) the correlation between textual semantics and function call structures for accurate relevance assessment, and 3) the correlation between the retrieval and generation phases, which enables iterative feedback and refinement. To evaluate iCoRe, we integrate it with an LLM-based BRT generator and conduct a comprehensive evaluation on the SWT-bench Lite benchmark. Experimental results show that our method achieves a Fail-to-Pass rate of 42.0%, representing a significant 31.7% relative improvement over existing retrieval methods.

## 24. In Bugs We Trust? On Measuring the Randomness of a Fuzzer Benchmarking Outcome

**Authors:** Ardi Madadi (Max Planck Institute for Security and Privacy), Seongmin Lee (UCLA), Cornelius Aschermann (Ruhr-University Bochum), Marcel Böhme (MPI for Security and Privacy)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797112

**中文总结:** 引入 concordance（基于 mean split-half reliability）度量 fuzzer 评测结果的可重复性，在 FuzzBench 与 Magma 上发现覆盖率评测一致性强于 bug 评测；并验证高 concordance 可在缩短活动或缩小基准集时仍保持结论，从而降低碳排放。

**Abstract:** In Google’s FuzzBench platform, we find that the outcome of coverage-based evaluation more strongly agrees with the outcome of a bug-based evaluation than an independent bug-based evaluation itself. Recently, Böhme et al. found that despite a very strong correlation between coverage achieved and bugs found, there is no strong agreement between the outcome of a coverage- and a bug-based evaluation: The fuzzer best at achieving coverage may be the worst at finding bugs. However, in trying to explain this moderate agreement, we wondered whether the outcome of bug-based benchmarking itself is perhaps much more “noisy” and turned to applied statistics to develop the tools necessary to investigate our hypothesis.

In this paper, we call this degree of “noisyness” of a benchmarking outcome as the \emph{concordance} of the benchmarking procedure and quantify it using a measure of statistical reliability widely-used in psychology, called \emph{mean split-half reliability}, i.e., the expected agreement on benchmark outcome between two random halfs of the benchmark set. In our experiments with FuzzBench and Magma, we find that the concordance of coverage-based benchmarking is consistently strong while that of bug-based benchmarking is weak on FuzzBench and moderate on Magma. In contrast to FuzzBench, for the Magma benchmark set, which was designed for bug-based evaluation, a coverage-based evaluation does \emph{not} predict the outcome of a bug-based evaluation better than an independent bug-based evaluation.

We investigate concordance as a measure of benchmarking efficiency, as in green fuzzer benchmarking. We empirically confirm, the resources of a procedure with higher concordance can be reduced more substantially (in terms of campaign length or benchmark set size) while maintaining a similar benchmark outcome than a procedure with lower concordance. We report the corresonding savings in terms of carbon emissions.

## 25. IntentTester: Intent-Driven Multi-Agent Framework for Cross-Library Test Migration

**Authors:** Yi Gao (Zhejiang University), Ziyuan Zhang (Zhejiang University), Xing Hu (Zhejiang University), Xiaohu Yang (Zhejiang University), Xin Xia (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797096

**中文总结:** 提出 IntentTester，将单测抽象为语言无关的 TDL，经仓库图语义对齐与 LLM 迭代验证实现跨库跨语言测试迁移；在九个项目上生成 2,776 个语法正确测试（85% 正确），并暴露若干已确认或已修复的未知缺陷。

**Abstract:** Unit tests capture both functional checks and domain-specific knowledge, but this knowledge remains locked within individual projects and is rarely reused across libraries with overlapping functionality. Existing migration techniques based on structural code mappings (e.g., API signatures) often break down under divergent designs or cross-language settings, resulting in non-executable migrated tests. In this paper, we present IntentTester, a multi-agent framework for intent-driven test reuse. Instead of translating raw code, IntentTester abstracts tests into a language-agnostic Test Description Language (TDL), aligns them with semantically related entities and dependencies in a repository graph, and synthesizes executable tests through LLM-guided reasoning and iterative validation. This design enables cross-library and cross-language migration without manual intervention, producing migrated tests that existing structure-mapping approaches cannot achieve. We evaluate IntentTester on nine open-source projects across three domains (JSON, HTML, Time) and two languages (Java, Python). IntentTester generates 2,776 syntactically correct tests with 85% correctness; in comparison, the two baselines achieve 51% and 43%. Among them, 2,410 tests execute successfully, yielding a 74% effectiveness rate. Beyond higher success rates, IntentTester also surfaced previously unknown defects—including stack overflows, null dereferences, and parsing inconsistencies, several acknowledged or patched by maintainers. Our results show that intent-driven migration shifts the focus from code mappings to semantic alignment, allowing practical cross-library and cross-language test reuse while improving test quality and exposing implementation flaws.

## 26. Interrogation Testing of CHC Solvers

**Authors:** David Kaindlstorfer (TU Wien, Austria), Anastasia Isychev (TU Wien), Valentin Wüstholz (ConsenSys), Maria Christakis (TU Wien)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797104

**中文总结:** 提出首个面向 CHC 求解器的 interrogation testing 工具 HornGator，利用求解器见证构造新实例并结合历史知识库提升实例多样性；在五个主流求解器上发现 21 个已确认唯一缺陷（18 个已修复，8 个最高严重级别）。

**Abstract:** A Constrained Horn Clause (CHC) is a specific type of logic formula that contains uninterpreted predicates. CHC formulas are often used by static program analyzers to encode program properties, which are then verified using CHC solvers. The solvers themselves are complex tools and may contain bugs, which can lead to verifying unsafe programs, flagging safe programs as unsafe, or providing analyzers with incorrect invariants and counterexamples. It is, therefore, crucial to develop techniques for systematically testing CHC solvers.

In this paper, we present the first interrogation-testing technique for CHC solvers, which we implement in a tool called HornGator. Our technique uses witnesses generated by the solver under test to form new CHC instances. It also integrates a knowledge base maintaining a history of past solver queries. All this information helps HornGator generate more diverse instances, thereby improving its bug-finding effectiveness. As a result, HornGator found 21 unique bugs in five state-of-the-art CHC solvers, all of which are confirmed by the developers, 18 are fixed, and eight are of the highest severity.

## 27. It Takes Two: Option-Aware Directed Greybox Fuzzing for Vulnerability PoC Generation

**Authors:** Susheng Wu, Xin Hu, Yiheng Cao, Zhuotong Zhou, Yiheng Huang, Yijian Wu, Bihuan Chen, Zhijia Zhao, Xin Peng

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808105

**中文总结:** 提出 CoupleFuzz，将 PoC 输入定义为选项输入与文件输入的组合，经静态选项知识提取与污点引导的交叉 fuzzing 协同逼近目标；在 22 个真实漏洞上比最佳传统 DGF 多生成 15 个 PoC（约 3.1×），平均加速 5.6×，并确认 6 个 0-day 与 1 个 CVE。

**Abstract:** Static analysis tools can identify potential vulnerabilities, but they often fall short in providing concrete proofs-of-concept (PoCs) to validate their findings. Directed greybox fuzzing (DGF) has emerged as a promising solution by systematically guiding execution toward suspicious code locations and generating reproducible PoCs that can trigger the target vulnerabilities. However, DGF tools often overlook the influence of configurable options on reaching target locations. Besides, option-aware greybox fuzzing (GF) tools suffer from ineffective option extraction to target locations, and inefficient coordination between options and file fuzzing.

To address these limitations, we present CoupleFuzz, a novel option-aware DGF tool that redefines PoC inputs as the combination of option input (OI) and file input (FI). CoupleFuzz adopts a two-phase workflow. The static analysis phase extracts option knowledge for guiding the fuzzing. The option-aware fuzzing phase employs taint analysis to dynamically prioritize effective option combinations and file bytes to target locations, and introduces a novel \emph{cross-guided fuzzing} strategy that coordinates OI and FI fuzzing modules and enables each module to adapt to and benefit from its counterpart’s advances, iteratively driving execution toward the target locations efficiently. Our evaluation has demonstrated that CoupleFuzz significantly outperforms the state-of-the-art DGF tools in generating PoCs for 22 real-world vulnerabilities, generating 15 (a 3.1$\times$ improvement) more PoCs than the best traditional DGF baseline and achieves an average speedup of 5.6$\times$ to reach target locations, with 6 0-day vulnerabilities confirmed by developers and 1 CVE identifier assigned.

## 28. MR-Coupler: Automated Metamorphic Test Generation via Functional Coupling Analysis

**Authors:** Congying Xu (The Hong Kong University of Science and Technology, China), Hengcheng Zhu (The Hong Kong University of Science and Technology), Songqiang Chen (The Hong Kong University of Science and Technology), Jiarong Wu, Valerio Terragni (University of Auckland), Shing-Chi Cheung (Hong Kong University of Science and Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808213

**中文总结:** 提出 MR-Coupler，利用源码中方法功能耦合自动构造蜕变关系与测试用例，经三种耦合模式与测试放大、变异分析校验；在 100 个人工 MTC 与 50 个真实缺陷上有效 MTC 生成率逾 90%，并检出 44% 真实缺陷。

**Abstract:** Metamorphic testing (MT) is a widely recognized technique for alleviating the oracle problem in software testing. However, its adoption is hindered by the difficulty of constructing effective metamorphic relations (MRs), which often require domain-specific or hard-to-obtain knowledge. In this work, we propose a novel approach that leverages the functional coupling between methods, which is readily available in source code, to automatically construct MRs and generate metamorphic test cases (MTCs). Our technique, MR-Coupler, identifies functionally coupled method pairs, employs large language models to generate candidate MTCs, and validates them through test amplification and mutation analysis. In particular, we leverage three functional coupling patterns to avoid expensive enumeration of possible method pairs, and a novel validation mechanism to reduce false alarms. Our evaluation of MR-Coupler on 100 human-written MTCs and 50 real-world bugs shows that it generates valid MTCs for over 90% of tasks, improves valid MTC generation by 64.90%, and reduces false alarms by 36.56% compared to baselines. Furthermore, the MTCs generated by MR-Coupler detect 44% of the real bugs. Moreover, the code structures of these MTCs closely follow the human-written MR skeletons. Our results highlight the effectiveness of leveraging functional coupling for automated MR construction and the potential of MR-Coupler to facilitate the adoption of MT in practice. We also released the tool and experimental data to support future research.

## 29. OCPPuzz: Specification-driven Fuzzing of Charging Station Management Systems with Large Language Model

**Authors:** Jongchan Hong (Sungkyunkwan University), Jaewon Kim (Sungkyunkwan University), Sungjae Hwang (Sungkyunkwan University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797091

**中文总结:** 提出 OCPPuzz，结合启发式与 LLM 从 OCPP 规范提取消息结构、约束与状态转移，对充电站管理系统做规范驱动模糊测试；在四个开源 CSMS 上报告 930 个实现缺陷（492 已确认），并向 OCA 报告 134 个规范问题。

**Abstract:** Electric vehicles (EVs) are being rapidly adopted, with over 61,000 publicly accessible charging stations deployed across the United States as of 2024. A core component of this infrastructure is the Charging Station Management System (CSMS), which is responsible for security-critical tasks such as user authentication and billing. Given its importance, the CSMS has become a target of real-world attacks that have resulted in financial losses, data breaches, and denial-of-service(DoS) incidents. Nevertheless, research on CSMS security remains limited, and automated testing tools are lacking. Testing CSMS is challenging because they communicate with charging stations (CS) using the Open Charge Point Protocol (OCPP). Effective testing must contend with OCPP’s complexity: 1) messages containing up to 48 fields, 2) inter- and intra-message field dependencies, and 3) its stateful nature, which requires tracking the states of both CS and CSMS during testing.

To address these challenges, we present OCPPuzz, a specification-based fuzzing framework for CSMS. OCPPuzz automatically extracts message structures, field constraints, and dependency rules from the OCPP specification, as well as valid CS-CSMS state transitions described in its use case diagrams. To handle specifications expressed in natural language and semi-formal diagrams, OCPPuzz combines heuristic rule-based extraction with large language models (LLMs). We evaluated OCPPuzz on four open-source CSMS implementations and uncovered numerous deviations from the OCPP specification that led to critical security issues, including DoS and free charging. We reported 930 implementation bugs to the corresponding vendors, of which 492 have been acknowledged so far. In addition, we reported 134 specification bugs in OCPP to the Open Charge Alliance (OCA); 79 have been committed for fixes and 85 acknowledged for further investigation. We expect additional acknowledgments and fixes in the near future.

## 30. OdoTest: An Automated Testing Approach for Odometry Systems

**Authors:** Jixiang Zhou, Mingfei Cheng, Shuncheng Tang, An Guo, Xiaofei Xie, Yinxing Xue, Lijun Zhang

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808128

**中文总结:** 提出 OdoTest，首个面向里程计模型的自动化测试框架，基于特定蜕变关系与变换算子模拟传感器/标定扰动并生成高效场景；可有效暴露多样条件下的错误行为，且用生成场景再训练可降低估计误差。

**Abstract:** Accurate odometry estimation is critical for the reliable operation of intelligent systems. Despite the remarkable progress of deep learning–based odometry models in controlled environments, real-world degradations such as IMU noise, visual impairments, and calibration errors often lead to significant estimation failures. Conventional testing methods, constrained by limited datasets and costly manual labeling, are insufficient for systematically revealing these vulnerabilities. In this paper, we propose OdoTest, the first automated testing framework for odometry models. OdoTest leverages odometry-specific metamorphic relations and introduces transformation operators that simulate realistic sensor and calibration perturbations, enabling the generation of transformed test datasets that expose model weaknesses. An odometry-oriented scenario generation strategy further improves testing efficiency. We evaluate OdoTest across multiple odometry models, and the results demonstrate that it can effectively detect erroneous behaviors under diverse odometry-specific conditions. Additionally, retraining with the generated scenarios improves odometry precision and reduces estimation errors, highlighting OdoTest’s potential for enhancing model reliability.

## 31. PROGnosticator: Testing Source-to-Source Code Translators via Construct-oriented Fuzzing

**Authors:** Yeaseen Arafat (University of Utah), Stefan Nagy (University of Utah)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797135

**中文总结:** 提出面向源到源翻译器的 Construct-oriented Fuzzing（PROGnosticator），用 LLM 枚举语言核心构造并生成针对性程序，无需依赖文法或种子；在 7 个翻译器上发现 77 个缺陷（64 个未知）。

**Abstract:** To ease software interoperability and migration, developers are increasingly embracing transpilers: automated tools for converting source code from one language to another. Unfortunately, differences in language constructs, syntax, and semantics leave transpilers facing many translation bugs, emitting incorrect or nonfunctional translations. Thorough, proactive transpiler testing is thus critical to the reliability of emergent translation-oriented development. While fuzzers excel in testing adjacent classes of language processors (e.g., compilers), current fuzzers remain tied to only the specific code patterns expressed in their inputs— hardcoded grammars or seed programs—which are costly to curate and extend, constraining their testing to just narrow subsets of language constructs. Worse yet, their generated programs are often overly complex, requiring non-trivial reduction to pinpoint the exact code patterns behind transpiler errors. Evaluating current and future transpilers thus demands a rigorous, input-independent fuzzing strategy—systematically exercising languages’ broad range of code constructs without needing costly per-language expertise or re-engineering.

To bridge this gap, we present Construct-oriented Fuzzing: a language-agnostic yet construct-aware approach for systematically testing transpilers. Motivated by our insights from past transpiler bugs, revealing most translation errors embody construct-specific mishandling, our approach explicitly targets the vast space of code patterns derived from core language constructs. Harnessing large language models’ code understanding and synthesis, we (1) automatically enumerate a language’s core constructs, before (2) generating self-contained programs exercising them individually—and combinations thereof—precisely testing transpilers’ many edgecases whilst eschewing cumbersome grammars or seeds. In evaluating our prototype, PROGnosticator, against four state-of-the-art compiler and transpiler fuzzers across seven transpilers for C, Go, and JavaScript, we show how our approach attains high per-language validity as well as construct-usage diversity—exposing 77 total transpiler bugs, of which 64 are previously unknown, with 63 since confirmed or fixed by developers.

## 32. QuanForge: A Mutation Testing Framework for Quantum Neural Networks

**Authors:** Minqi Shao (Kyushu University), Shangzhou Xia (Kyushu University), Jianjun Zhao (Kyushu University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808135

**中文总结:** 提出 QuanForge，面向量子神经网络的变异测试框架，引入统计变异杀死判据与 9 类门/参数级变异算子；可有效识别弱测试套件并定位脆弱电路区域。

**Abstract:** With the growing synergy between deep learning and quantum computing, Quantum Neural Networks (QNNs) have emerged as a promising paradigm by leveraging quantum parallelism and entanglement. However, testing QNNs remains underexplored due to their complex quantum dynamics and limited interpretability. Developing a mutation testing technique for QNNs further requires addressing stochastic factors, including the inherent randomness of mutation operators and quantum measurements. To tackle these challenges, we propose \textbf{QuanForge}, a mutation testing framework specifically designed for QNNs. We first introduce statistical mutation killing to provide a more reliable criterion. QuanForge incorporates nine post-training mutation operators at both gate and parameter levels, capable of simulating various potential errors in quantum circuits. Finally, a mutation generation algorithm is formalized, which systematically produces effective mutants, thereby enabling a robust and reliable mutation analysis. Through extensive experiments on benchmark datasets and QNN architectures, we show that QuanForge can effectively identify weak test suites and localize vulnerable circuit regions. We also analyze the generation capability of different operators, providing guidance for future mutant design and structural assessment of QNNs.

## 33. RAT: Retrieval-Augmented Testing of Certificate Revocation List Parsers in TLS Implementations

**Authors:** Chu Chen (Qufu Normal University), Qianxin Cheng (Qufu Normal University), Pinghong Ren (Qufu Normal University), Hairong Yu (Qufu Normal University), Cong Tian (Xidian University), Zhenhua Duan (Xidian University), Xu Lu (Xidian University), Bin Yu (Xidian University), WenSheng Wang (Xidian University), Jin Liu (Xi'an University of Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808212

**中文总结:** 提出 RAT，用 LLM 检索历史缺陷并对照 RFC 5280 生成 ASN.1 感知测试用例，系统评估 TLS 实现中的 CRL 解析器；在 OpenSSL 等实现上发现 23 个新问题。

**Abstract:** Transport Layer Security (TLS) implementations form the backbone of  countless software systems, spanning from web browsers, email clients,  cloud services, and Internet of Things software, by enabling secure authentication and encrypted communication. However, their reliability hinges on the integrity of components like Certificate Revocation List (CRL), which revokes compromised certificates to prevent attackers from exploiting expired or unauthorized credentials. Despite CRL’s critical role, CRL parsers, which decode CRL data for validation, remain overlooked in security research, exposing TLS-dependent software to potential threats. To address this gap, we introduce Retrieval-Augmented Testing (RAT), a framework powered by Large Language Models (LLMs), to systematically evaluate CRL parsers in mainstream TLS implementations such as OpenSSL, GnuTLS, and wolfSSL. RAT begins with leveraging an LLM to retrieve historical bug reports and cross-reference them with Request for Comments (RFC) 5280 specifications,  generating structured test cases via an Abstract Syntax Notation One-aware mutation engine. These test cases are then fed into CRL parsers, and RAT employs an LLM to normalize their outputs. By analyzing these normalized results, RAT detects discrepancies and uncovers latent risks in CRL parsers. Our work makes the following contributions: (1) Unlike prior work focusing on certificate validation, this is the first study to systematically assess CRL parsers; (2) We propose RAT, a novel testing framework that leverages an LLM to integrate insights from retrieved bug reports and RFC 5280, enabling automated test-case generation; and (3) We have implemented an open-source prototype of RAT and experiments uncovered 23 new bugs, features, enhancements, fixes in commits, and x509s, demonstrating RAT’s potential to bolster the security foundation of TLS-powered systems worldwide.

## 34. Reducing Coverage-Equivalent Inputs in Grammar-based Fuzzing by Avoiding Recurrent Rule Sequences

**Authors:** Jaehan Yoon (Sungkyunkwan University), Yunji Seo (Korea University), Hakjoo Oh (Korea University), Sooyoung Cha (Sungkyunkwan University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808210

**中文总结:** 提出 RSFuzz，自动识别并避免导致覆盖等价输入的递归产生式序列以增强基于文法的模糊测试；集成到随机与概率模糊器后额外检出大量崩溃，并提升行覆盖、减少重复覆盖输入。

**Abstract:** We present RSFuzz, a new technique to enhance grammar-based fuzzing by reducing the generation of coverage-equivalent inputs during testing. Grammar-based fuzzers apply production rules from a given grammar to generate well-structured inputs for the target program. However, a key limitation is that many existing fuzzers still produce a large number of “coverage-equivalent” inputs—those that revisit already explored program paths—thereby restricting their ability to uncover new bugs and improve coverage. To address this issue, RSFuzz automatically identifies recurrent sequences of production rules that cause coverage-equivalent inputs and prevents their reuse during fuzzing. A key challenge in practice lies in the large number of coverage-equivalent input groups, each with many inputs, making it difficult to identify the underlying recurrent sequences. RSFuzz tackles this challenge with a customized algorithm that iteratively groups coverage-equivalent inputs, selects promising groups, and extracts recurrent sequences for each group based on accumulated data while running any grammar-based fuzzer. We integrated RSFuzz with existing random and probabilistic fuzzers and evaluated it on eight real-world programs using JavaScript and JSON input formats. Experimental results show that incorporating RSFuzz with both fuzzers exclusively detects 108 and 31 crashes with distinct stack traces, increases line coverage by 6.5% and 5.1%, and reduces duplicate-coverage input generation by 29.7% and 37.7%, respectively, compared to their performance without RSFuzz.

## 35. Revealing Regressions: A Comparative Study of State-Capture Strategies in Validating Program Behavior

**Authors:** Hang Du, Vijay Krishna Palepu, James Jones

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797107

**中文总结:** 系统比较程序状态捕获策略对回归揭示能力的影响；发现人工断言常未充分利用状态，暴露中间返回值、精选 getter 与加深提取可平均提升约 35.7% 的回归检测效果。

**Abstract:** A central challenge in software testing is deciding which parts of a program’s state to check as evidence of correct behavior to reveal regressions. These checks are embodied as test oracles, typically as assertions in test cases. State observation strategies play a decisive role in shaping how effectively regressions can be revealed. Such strategies range from exhaustive memory snapshots to selective attribute checks via getter methods and nullability checks. These strategies are deeply embedded in both research and practice: academic work has explored heuristic- and serialization-based oracles, while industry has widely adopted snapshot testing. Despite their importance, the effects of different state-capture choices remain poorly understood from a scientific perspective. In this work, we present an experimental framework for systematically analyzing these design choices along the dimensions of observation scope, extraction approach, and extraction depth. Using this framework, we conduct an empirical study across twelve real-world projects, measuring how state-capture strategies influence regression-revealing capability and the richness of oracle information. Our findings reveal that human-written assertions often under-utilize available program state, achieving well below the fault-revealing potential of systematic observation strategies. Simple design choices, such as exposing unchecked intermediate return values, carefully selecting getters, and deepening state extraction, can yield measurable improvements (avg. 35.7%) in regression detection without needing to observe an overwhelmingly large amount of program-state data. Additionally, we highlight the challenges of observability, assertion desirability, and the trade-offs of capturing richer program states. Such insights show how small design choices can yield major differences in regression detection and potentially offer concrete directions for both tool builders and practitioners.

## 36. SnakeCharmer: Automatic Fuzzing Harness Generation for Pure and Hybrid Python Libraries

**Authors:** Gabriel Sherman (University of Utah), Stefan Nagy (University of Utah)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797066

**中文总结:** 提出 SnakeCharmer，首个面向纯 Python 与含 C/C++ 扩展混合库的自动化 fuzzing harness 生成方法，结合静态接口分析、运行时类型与异常过滤；在 21 个库上覆盖率相对多类基线最高达约 1.87×，并发现 20 个新缺陷（18 个已确认/修复）。

**Abstract:** With Python’s rising popularity, ensuring the correctness of its ever-growing ecosystem of software libraries is more critical than ever. Recently, fuzzing has become a de facto technique for vetting software libraries, enabled via the use of harnesses: small wrapper programs that inject fuzzer-generated test cases into the library under test. While harness creation has shed its reliance on human expertise and is now fully automated for languages such as C and C++, Python remains uniquely challenging—both for pure Python libraries as well as hybrid ones combining Python with native C/C++ extensions—due to (1) limited visibility across language boundaries, (2) the absence of reliable bug oracles, and (3) incomplete type information. Consequently, attempts at automating harnessing for Python fail to both uphold critical runtime behaviors and produce the structured call and data flows needed for effective fuzzing, leaving much of today’s Python ecosystem largely unvetted.

To overcome these challenges and broaden fuzzing’s reach across Python libraries, this paper introduces SnakeCharmer: the first automated harness generation approach for both pure and hybrid Python libraries. At its core, SnakeCharmer leverages static analysis to first capture key interface information from both Python and native code components, subsequently enriching it with runtime-captured type information and exception behaviors. During fuzzing, SnakeCharmer further distinguishes between expected exceptions and true library bugs, filtering out benign exceptions that would otherwise derail testing progress. Together, these techniques significantly enhance the scope and effectiveness of fuzzing across the Python library ecosystem, enabling the automated discovery of bugs in code previously inaccessible to existing Python fuzzing efforts.

We evaluate SnakeCharmer alongside today’s leading Python auto-harnessing approach, PyRTFuzz; the actively fuzzed expert-written harnesses from both OSS-Fuzz and PolyFuzz; and the harnesses generated by Google’s own state-of-the-art LLM-driven automatic harnessing approach, OSS-Fuzz-Gen. Across 21 diverse Python libraries, SnakeCharmer attains type-recovery precision and exception-filtering accuracy of 95% and 97%, respectively, further attaining 1.48×, 1.87×, 1.78×, and 1.40× the code coverage of the fuzzing harnesses from PyRTFuzz, OSS-Fuzz, PolyFuzz, and OSS-Fuzz-Gen, respectively. Further, SnakeCharmer finds 16, 24, and 24 more Python library bugs than all expert- and LLM-created harnesses as well as PyRTFuzz, respectively—uncovering a total of 20 new bugs, with 18 since confirmed or fixed by developers.

## 37. SQLiFuzz: Uncovering SQL Injection in Any Web Applications

**Authors:** I Putu Arya Dharmaadi (University of Groningen), Thuan Pham (University of Melbourne), Fadi Mohsen (University of Groningen), Fatih Turkmen (University of Groningen)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808149

**中文总结:** 提出 SQLiFuzz，通过反向代理统一 GUI/API 请求收集、数据库代理作神谕，以及反馈驱动的请求/参数优先 fuzzing，实现易部署的通用 SQL 注入检测；在基准与 10 个真实应用上检出多数已知案例并发现 9 个被 SOTA 遗漏的新漏洞。

**Abstract:** SQL injection (SQLi) is one of the most critical and prevalent security vulnerabilities, as it enables attackers to manipulate backend databases, bypass authentication, and even gain complete control of the underlying system. Since web applications are the primary target for SQL injection, the web developers must test to ensure the applications are robust to this attack. Recently, there have been several advanced solutions using fuzzing approaches to test SQL injection vulnerability; however, our preliminary analysis reveals key limitations that reduce their effectiveness: they primarily focus on GUI-based inputs while neglecting API endpoints, rely on less effective request selection strategies, and require complex configurations to deploy.

To address these gaps, we propose SQLiFuzz, a universal and simple-to-deploy SQL injection fuzzer that operates across both GUI (web pages) and API entry points. SQLiFuzz introduces three key innovations: (i) a reverse proxy that unifies request collection and fuzzing and integrates seamlessly with existing crawlers and API scanners, (ii) a database proxy that enables request–query matching and serves as a reliable oracle, and (iii) a feedback-driven fuzzer that prioritizes potentially vulnerable requests and parameters and validates exploitability through database responses. We evaluate SQLiFuzz on six security benchmarks and ten real-world applications. SQLiFuzz successfully detected the majority of known SQLi cases in the benchmarks and uncovered nine new vulnerabilities, which had been overlooked by state-of-the-art tools, in the real-world applications. These results highlight SQLiFuzz’s ability to reveal SQLi across diverse architectures while maintaining practicality and ease of deployment.

## 38. Structure-Aware Delta Debugging with Geometric-Information Weights

**Authors:** Yonggang Tao, Jingling Xue

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808195

**中文总结:** 提出 Structure-Aware Delta Debugging（SADD），用几何体积、决策均匀性与有效分支复杂度等结构信号为元素赋权，并实例化为 SA_ddmin 与 SA_ProbDD；在 HDD/Perses 的 C 与 XML 基准上相对 ddmin/ProbDD/WDD 显著缩短约减时间（如 HDD 上 C 基准最高约 57%）。

**Abstract:** Delta debugging is a fundamental technique for automatically minimizing failure-inducing inputs. ProbDD augments ddmin by replacing its deterministic partitioning with a probability-guided search. Recently, Weighted Delta Debugging (WDD) augments ddmin (W_ddmin) or ProbDD (W_ProbDD) with token-based weighting to address size disparities, but it can conflate syntactic size with structural complexity: elements with similar token counts may differ substantially in syntactic structure or semantic significance.

We introduce Structure-Aware Delta Debugging (SADD), which quantifies element importance using geometric and information-theoretic properties of program structure. SADD defines a unified weight function that combines three complementary signals—geometric volume, decision uniformity, and effective branch complexity. We instantiate SADD in two algorithms: SA_ddmin, which augments ddmin with structure-aware partitioning, and SA_ProbDD, which injects structural weights into ProbDD’s probabilistic selection.

We evaluate SADD against ddmin, W_ddmin, W_ProbDD, and ProbDD within two state-of-the-art delta debugging frameworks, HDD and Perses, using 62 real-world C and XML benchmarks. Under HDD, our approach substantially reduces average delta debugging times: 57.12% (SA_ddmin vs. ddmin), 15.04% (SA_ddmin vs. W_ddmin), and 14.64% (SA_ProbDD vs. ProbDD) on C benchmarks, and 30.12% (SA_ddmin vs. ddmin) and 20.10% (SA_ProbDD vs. ProbDD) on XML benchmarks. On C under Perses, it achieves 7.02% (SA_ProbDD vs. ProbDD). In other cases—such as XML programs with simpler, flatter structures where WDD’s token counting suffices, or under Perses, which already applies structural transformations before ddmin—the gains are limited or absent. An ablation study shows that geometric volume provides the foundation, while information-theoretic metrics add complementary, context-sensitive refinements. Overall, modeling structural complexity improves delta debugging precisely when input hierarchies exhibit diversity that token counts alone cannot capture.

## 39. TestTailor: Generating High-Coverage Tests via Path-Proximal Tests with LLMs

**Authors:** Xiaoxuan Zhou (Northeastern University), Yiling Lou (University of Illinois at Urbana-Champaign), Jinhao Dong (Peking University), Dan Hao (Peking University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797140

**中文总结:** 提出 TestTailor，利用 path-proximal 测试与符号约束生成细粒度路径引导提示，驱动 LLM 覆盖难达分支；在 CODAMOSA 的 486 个 Python 模块上相对 CoverUp 平均提升语句/分支覆盖 5.01%/4.17% 且 API 成本约降 60%。

**Abstract:** Automated unit testing is essential for ensuring software quality. Achieving high code coverage through automated unit test generation remains challenging, especially for hard-to-cover branches guarded by complex or deeply nested conditions. Traditional search-based approaches often stagnate at fitness plateaus, while recent LLM-based techniques provide mostly coarse-grained prompts, leaving models to guess how to reach uncovered targets. To address these limitations, we present TestTailor, a neuro-symbolic framework that exploits fine-grained, path-oriented guidance to guide LLM-based test generation. The key idea is to exploit path-proximal tests (i.e., existing test cases whose execution paths closely resemble the target uncovered path) and to analyze their divergence points. By combining this analysis with symbolic constraints (i.e., constraints collected from the target uncovered path using symbolic execution), TestTailor derives actionable path guidance and encodes them into concise prompts that tell the LLM not only what remains uncovered, but also how to reach it. We evaluate TestTailor on the widely used CODAMOSA benchmark comprising 486 Python modules. Results show that TestTailor consistently outperforms state-of-the-art baselines, improving statement coverage by 5.01% and branch coverage by 4.17% on average compared to the best baseline CoverUp, while reducing API cost by about 60%. Against the hybrid LLM-search-based technique CODAMOSA, TestTailor achieves even larger gains of 12.78% and 13.09% in statement and branch coverage, respectively. Moreover, TestTailor attains the highest coverage accuracy (85.2% vs. 75.3% for CoverUp and 63.8% for TELPA), and demonstrates robustness across different LLM backbones. These results highlight that TestTailor transforms vague coverage goals into precise path-level instructions, enabling LLMs to generate high-coverage test suites more efficiently and accurately.

## 40. Towards Automated Crowdsourced Testing via Personified-LLM

**Authors:** Shengcheng Yu (Technical University of Munich), Yuchen Ling (Nanjing University), Chunrong Fang (Nanjing University), Zhenyu Chen (Nanjing University), Chunyang Chen (TU Munich)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808173

**中文总结:** 提出 PersonaTester，将测试心态、探索策略与交互习惯三维 persona 注入 LLM 智能体，以可控可复现方式模拟众包 GUI 测试行为；相对无 persona 基线更一致且更具多样性，触发更多崩溃与功能缺陷。

**Abstract:** The rapid proliferation and increasing complexity of software demand robust quality assurance, with graphical user interface (GUI) testing playing a pivotal role. Crowdsourced testing has proven effective in this context by leveraging the diversity of human testers to achieve rich, scenario-based coverage across varied devices, user behaviors, and usage environments. In parallel, automated testing, particularly with the advent of large language models (LLMs), offers significant advantages in controllability, reproducibility, and efficiency, enabling scalable and systematic exploration. However, automated approaches often lack the behavioral diversity characteristic of human testers, limiting their capability to fully simulate real-world testing dynamics. To address this gap, we present PersonaTester, a novel personified-LLM-based framework designed to automate crowdsourced GUI testing. By injecting representative personas, defined along three orthogonal dimensions: testing mindset, exploration strategy, and interaction habit, into LLM-based agents, PersonaTester enables the simulation of diverse human-like testing behaviors in a controllable and repeatable manner. Experimental results demonstrate that PersonaTester faithfully reproduces the behavioral patterns of real crowdworkers, exhibiting strong intra-persona consistency and clear inter-persona variability (117.86% – 126.23% improvement over the baseline). Moreover, persona-guided testing agents consistently generate more effective test events and trigger more crashes (100+) and functional bugs (11) than the baseline without persona, thus substantially advancing the realism and effectiveness of automated crowdsourced GUI testing.

## 41. TUSR: A Test Unit–Based Framework for Repairing Obsolete GUI Test Scripts

**Authors:** Shaoheng Cao (Nanjing University), Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808214

**中文总结:** 提出 TUSR，以「测试单元」（服务于单一测试意图的连续动作序列）替代逐步修复来修复过时 GUI 脚本；在 20 款 Android 应用的 262 条脚本上显著优于现有黑盒与白盒修复方法。

**Abstract:** Graphical User Interface (GUI) testing is a primary technique for testing mobile applications. Among existing testing methods, script-based testing is widely adopted because test scripts can be replayed across devices and versions. However, as mobile apps evolve, frequent changes to GUI appearance and interaction logic often render scripts written for earlier versions obsolete. Existing repair approaches typically follow a stepwise framework, repairing scripts action by action. While effective for minor GUI appearance changes, they struggle when interaction logic is modified. In this paper, we present TUSR, a test unit–based repair framework that fundamentally departs from the stepwise paradigm. TUSR introduces the concept of a “Test Unit”—a contiguous sequence of test actions serving a single testing intention—and repairs scripts at the unit level. It first splits scripts into test units using a multi-modal LLM with a rule-based correction mechanism to ensure consistency, then conducts dynamic repair guided by a Chain-of-Thought prompt enhanced with reflective memory. Experiments on 20 real-world Android applications, covering 262 test scripts and 3,485 actions, demonstrate that TUSR significantly outperforms state-of-the-art black-box and white-box repair approaches.

## 42. WalleTruth: Visual-oriented Software Testing for Web3 Wallet Browser Extensions

**Authors:** Xiaohui Hu (Huazhong University of Science and Technology), Ningyu He (Hong Kong Polytechnic University), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797150

**中文总结:** 提出面向浏览器钱包扩展的视觉导向测试框架 WalleTruth，归纳 12 类攻击向量与 21 种具体攻击策略；在 39 款主流扩展上均发现可被滥用窃取资产的风险，已报告并推动 26 个问题修复。

**Abstract:** Serving as the first touch point for users to the cryptocurrency world, cryptocurrency wallets allow users to manage, receive, and transmit digital assets on blockchains and interact with emerging decentralized finance (DeFi) applications. Unfortunately, cryptocurrency wallets have always been the prime targets for attackers, and incidents of wallet breaches have been reported from time to time. Although some recent studies have characterized the vulnerabilities and scams related to wallets, they have generally been characterized in coarse granularity, overlooking potential risks inherent in detailed designs of cryptocurrency wallets, especially from perspectives including user interaction and advanced features. To fill the void, in this paper, we present a fine-grained security analysis on browser-based cryptocurrency wallets. To pinpoint security issues of components in wallets, we design Walletruth, a visual-oriented testing framework specifically for browser-based wallet extensions. We have identified 12 attack vectors that can be abused by attackers to exploit cryptocurrency wallets and exposed 21 concrete attack strategies. By applying Walletruth on 39 widely-adopted browser-based wallet extensions, we astonishingly figure out all of them can be abused to steal crypto assets from innocent users. Identified potential attack vectors were reported to developers timely and 26 issues have been patched already. It is, hence, urgent for our community to take action to mitigate threats related to cryptocurrency wallets.

## 43. WebTestPilot: Agentic End-to-End Web Testing against Natural Language Specification by Inferring Oracles with Symbolized GUI Elements

**Authors:** Xiwen Teoh (National University of Singapore), Yun Lin (Shanghai Jiao Tong University), Duc-Minh Nguyen (Shanghai Jiao Tong University), Ruofei Ren (Shanghai Jiao Tong University), Wenjie Zhang (National University of Singapore), Jin Song Dong (National University of Singapore)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797115

**中文总结:** 提出神经符号方法 WebTestPilot，将关键 GUI 元素抽象为符号变量以约束断言生成并推导隐式测试预言；在注入缺陷的 Web 应用基准上任务完成率 99%、缺陷检测精确率与召回均 96%，实部署中发现 8 个缺陷。

**Abstract:** Visual language model (VLM) agents show great promise in automating graphical user interface (GUI) testing against requirements in natural language. However, the probabilistic nature of language models can have inherent hallucinations. Therefore, given a detected inconsistency between the requirement and the web application, it is hard to distinguish whether it stems from the hallucination or a real application bug. Addressing this issue presents two core technical challenges: (1) limited capability and accuracy in deriving implicit test oracles, where the agent must act as its own oracle to implicitly decide if the application’s behavior is correct without guidance, and (2) limited reliability due to probabilistic inference, where an LLM’s inconsistent reasoning undermines its trustworthiness as an oracle.

We introduce WebTestPilot, a neurosymbolic LLM-based approach that addresses both challenges through symbolization. WebTestPilot detects and abstracts critical GUI elements of a web application into symbolic variables. This design improves reliability by constraining assertion generation to operations grounded in explicitly defined symbols, thereby reducing unconstrained or inconsistent reasoning. At the same time, it improves accuracy by representing application states and their relationships in a structured symbolic form, which increases the likelihood of the agent recognizing data, causal, and temporal dependencies across states. Together, these capabilities enable WebTestPilot to generate reliable and accurate test oracles that capture meaningful implicit expectations derived from test requirements. To advance research in this area, we build a benchmark of bug-injected web apps for evaluating NL-to-E2E testing. The results show that WebTestPilot achieves a task completion rate of 99%, with 96% precision and 96% recall in bug detection, outperforming the best baseline (+70 precision, +27 recall). The agent generalizes across diverse natural language inputs (i.e., those containing typos, grammatical errors, redundant sentences, stylistic restyling, or abbreviations) and model scales (3B–72B). In a real-world deployment with a no-code platform, WebTestPilot discovered 8 bugs during development, including data binding, UI, and navigation issues.
