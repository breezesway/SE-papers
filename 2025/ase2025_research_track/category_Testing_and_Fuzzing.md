# ASE 2025 Research Track — Testing and Fuzzing

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 40

## 1. Algernon: A Flag-Guided Hybrid Fuzzer for Unlocking Hidden Program Paths

**Authors:** Peng Deng (Fudan University), Lei Zhang (Fudan University), Jingqi Long (Fudan University), Wenzheng Hong (Independent), Zhemin Yang (Fudan University), Yuan Zhang (Fudan University), Donglai Zhu (Fudan University), Min Yang (Fudan University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334345

**中文总结:** 提出 Algernon 动态 flag 引导混合模糊测试，自动识别 flag 变量并将复杂 flag-check 约束分解为原子约束顺序求解，以高效解锁受内部状态 guarding 的隐藏路径。

**Abstract:** Fuzz testing is a widely used method for finding security issues in software. However, certain code paths can only be explored under specific program states. Flag variables, which represent internal states, are crucial in influencing program behavior through flag-guarded branches. Unfortunately, existing fuzzing tools struggle to efficiently explore them due to the implicit data dependency between flag variables and the input. As a result, they commonly lack awareness of the dependency between program input and the assignments of critical flag variables, leading to a blind or random approach to satisfy flag-checking constraints, which greatly impacts the fuzzing efficiency.

To address this issue, this paper proposes a dynamic flag-guided hybrid fuzzing approach, which automates the identification of flag variables and provides guidance for fuzz testing. Specifically, we first design a pre-fuzzing program analysis to recognize flag variables and a novel data structure to present how flag variables guard code branches. Then, we propose a new constraint-solving approach by separating complex flag-checking constraints into a set of atomic ones and sequentially solving them by traversing our FDG to locate execution paths that could assign the flag variables with the desired values.

We implement a prototype tool, called Algernon, and evaluate it on 20 popular open-source programs. Across all tested programs, Algernon outperforms QSYM, Angora, AFL++, and INVSCOV in terms of both code coverage and vulnerability discovery, demonstrating the effectiveness of our approach. During our experiments, Algernon successfully found 30 zero-day vulnerabilities with 11 CVE IDs assigned.


## 2. ARG: Testing Query Rewriters via Abstract Rule Guided Fuzzing

**Authors:** Dawei Li (Beihang University), Yuxiao Guo (Beihang University), Qifan Liu (Beihang University), Jie Liang (Beihang University), Zhiyong Wu (Tsinghua University, China), Jingzhou Fu (School of Software, Tsinghua University), Chi Zhang (Tsinghua University), Yu Jiang (Tsinghua University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334334

**中文总结:** 提出 ARG 抽象规则引导模糊测试，跟踪查询重写抽象规则覆盖并以反馈动态调整 SQL 生成，激活更多重写逻辑以检测 DBMS 查询重写器崩溃与语义错误。

**Abstract:** Query rewriters transform a query into a more efficient yet semantically equivalent form, which is vital for optimizing query execution. Despite its importance, query rewriting is inherently complex, influenced by factors including rewrite rule design, rule interactions, and semantic preservation. Consequently, its implementation struggles to prevent problems, which may result in system crashes or incorrect query results. Existing DBMS testing approaches are generally designed for broad bug detection. However, due to the diversity of rewrite rules, they cover only a limited subset of rewrite scenarios, potentially overlooking critical bugs.

In this paper, we propose Abstract Rule Guided (ARG) fuzzing to detect bugs in query rewrites. The key idea is to use feedback from abstract rules to guide query generation, thereby activating more rewriting logic and enhancing bug detection. Abstract rules provide a unified representation of the patterns (e.g., AST structures and related constraints) that trigger rewrites, as well as the resulting transformations. We track abstract rules to identify which patterns have been covered. This feedback is then used to dynamically adjust query generation, prioritizing unexplored patterns to avoid redundancy and expose more rewriting logic. We implemented ARG to test four popular query rewrites, namely Calcite, WeTune, SQLSolver, and LearnedRewrite. ARG discovered 38 previously unknown bugs, consisting of 4 crashes, 13 invalid SQL outputs, and 21 semantic deviations. Among them, 19 have been confirmed, while the remaining cases are still under investigation. We also compared ARG against popular DBMS testing tools. In 24 hours, ARG triggered 76% and 1017% more written rules, triggered 13 and 15 more bugs than SQLsmith and SQLancer, respectively.


## 3. Automated Combinatorial Test Generation for Alloy

**Authors:** Agustín Borda (University of Rio Cuarto, CONICET and Guangdong Technion-Israel Institute of Technology), Germán Regis (University of Rio Cuarto and CONICET), Nazareno Aguirre (University of Rio Cuarto/CONICET, Argentina, and Guangdong Technion-Israel Institute of Technology, China), Marcelo F. Frias (Dept. of Software Engineering Instituto Tecnológico de Buenos Aires), Pablo Ponzio (Dept. of Computer Science FCEFQyN, University of Rio Cuarto)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334715

**中文总结:** 提出 COMBA，自动划分 Alloy 规约状态空间并基于组合覆盖准则（参数 t）生成测试，无需用户干预即可系统性评估形式规约的 wanted/unwanted 场景。

**Abstract:** Specifications are an essential component of software development, and getting specifications right, especially \emph{formal specifications}, can be very challenging. While the use of tools such as model finders and model checkers can be very effective for specification analysis through property checking, researchers have also realized that by the explicit provision of wanted and unwanted specification scenarios, in the style of testing in programs, specification assessment can be significantly enhanced. Thus, various testing and test generation techniques have been recently proposed for assessing formal specifications.

In this paper, we present such a specification testing approach, in the form of a novel combinatorial testing technique for Alloy specifications, called COMBA. COMBA implements an automated partitioning of the state space of Alloy specifications solely based on elements of the specification (thus not requiring user intervention), and defines a family of test criteria, that indicate how such partitions are to be covered. The coverage of the partitions is defined by a family of combinatorial criteria that, given a positive integer $t$, require to cover through test cases all feasible $t$-uples of elements from different partitions. Finally, COMBA introduces an efficient algorithm to generate test cases that satisfy the combinatorial criteria. By leveraging on incremental SAT solving techniques, COMBA achieves significantly better performance in test generation.

We experimentally assess COMBA against existing test generation approaches for Alloy, using a large number of Alloy specifications with known errors. The results show COMBA runs faster, produces smaller test suites, and finds a significantly larger number of real bugs than related approaches.


## 4. Automated Generation of Issue-Reproducing Tests by Combining LLMs and Search-Based Testing

**Authors:** Konstantinos Kitsios (University of Zurich), Marco Castelluccio (Mozilla), Alberto Bacchelli (University of Zurich)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334449

**中文总结:** 提出 BLAST，结合 LLM 与搜索式测试从 issue-patch 对自动生成复现测试；在 Python 基准上 151/426（35.4%）成功，优于 SOTA 23.5%。

**Abstract:** When a software issue is patched, it is important to have a test validating that the patch resolves the issue. Such a test fails in the unpatched code and passes in the patched code, hence called an issue-reproducing test. However, as with testing in general, the writing of issue-reproducing tests is frequently omitted by developers, making its automation an area of interest. We propose BLAST, a tool for automatically generating issue- reproducing tests from issue-patch pairs by combining LLMs and search-based software testing (SBST). For the LLM part, we complement the issue description and the patch by extracting relevant context through git history analysis, static analysis, and SBST-generated tests. For the SBST part, we adapt SBST for generating issue-reproducing tests; the issue description and the patch are fed into the SBST optimization through an interme- diate LLM-generated seed, which we deserialiaze into SBST- compatible form. BLAST successfully generates issue-reproducing tests for 151/426 (35.4%) of the issues from a curated Python benchmark, outperforming the state-of-the-art (23.5%). Additionally, to measure the real-world impact of BLAST, we built a GitHub bot that runs BLAST whenever a new pull request (PR) linked to an issue is opened, and if BLAST generates an issue- reproducing test, the bot proposes it as a comment in the PR. We deployed the bot in three open-source repositories for three months, gathering data for 32 PRs and proposing tests in 11 of them. By analyzing developers’ feedback, we discuss challenges and opportunities for researchers and tool builders.


## 5. BCFuzz: Bytecode-Driven Fuzzing for JavaScript Engines

**Authors:** Jiming Wang (SKLP, Institute of Computing Technology, CAS & University of Chinese Academy of Sciences), Chenggang Wu (Institute of Computing Technology at Chinese Academy of Sciences; University of Chinese Academy of Sciences; Zhongguancun Laboratory), Jikai Ren (SKLP, Institute of Computing Technology, CAS & University of Chinese Academy of Sciences), Yuhao Hu (SKLP, Institute of Computing Technology, CAS & University of Chinese Academy of Sciences), Yan Kang (Institute of Computing Technology at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Xiaojie Wei (SKLP, Institute of Computing Technology, CAS), Yuanming Lai (Institute of Computing Technology at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Mengyao Xie (SKLP, Institute of Computing Technology, CAS), Zhe Wang (Institute of Computing Technology at Chinese Academy of Sciences; Zhongguancun Laboratory)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334349

**中文总结:** 提出 BCFuzz 字节码驱动 JS 引擎模糊测试，解析探测识别生成特定字节码的必要条件，并对低频字节码做保留/调度/变异；72 小时在 4 个主流引擎发现大量新缺陷。

**Abstract:** The interpreter and the Just-In-Time (JIT) compiler are two core components of modern JavaScript engines, both of which take bytecodes as input. Most bugs in these components are closely related to specific bytecodes. Therefore, effective fuzzing should pay close attention to how bytecode is generated and exercised. However, previous work fails to consider this aspect and instead focuses primarily on the syntactic and semantic validity of test cases. This causes two major issues: 1) certain bytecodes are never exercised during fuzzing; 2) some bytecodes are exercised infrequently. In this paper, we propose BCFuzz, a bytecode-driven fuzzing approach designed to enhance the diversity of generated bytecode and increase testing opportunities for low-frequency bytecodes. Specifically, we introduce a parser-oriented probing technique to identify the necessary conditions for generating specific bytecodes and use this information to enhance the input generation process. To better test low-frequency bytecodes, we propose bytecode-aware seed preservation, scheduling, and mutation strategies. We evaluate BCFuzz on four mainstream JavaScript engines. In 72 hours of testing, BCFuzz discovers 1.73$\times$ and 1.67$\times$ more bugs than DIE and Fuzzilli, respectively. In total, BCFuzz uncovered 21 previously unknown bugs. Of these, 17 have already been fixed and one has been assigned a CVE. All the discovered bugs are related to bytecodes.


## 6. Clarifying Semantics of In-Context Examples for Unit Test Generation

**Authors:** Chen Yang (Tianjin University), Lin Yang (Tianjin University), Ziqi Wang (Tianjin University), Dong Wang (Tianjin University), Jianyi Zhou (Huawei Cloud Computing Technologies Co., Ltd.), Junjie Chen (Tianjin University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334234

**中文总结:** 提出 CLAST，通过程序分析与 LLM 重写将复杂单元测试分解并澄清语义，使其更适合作为 ICL 示例；在四个开源与三个工业项目中全面优于 UTgen，在保留原测试有效性的同时显著提升语义清晰度。

**Abstract:** Recent advances in large language models (LLMs) have enabled promising performance in unit test generation through in-context learning (ICL). However, the quality of in-context examples significantly influences the effectiveness of generated tests—poorly structured or semantically unclear test examples often lead to suboptimal outputs. In this paper, we propose CLAST, a novel technique that systematically refines unit tests to improve their semantic clarity, thereby enhancing their utility as in-context examples. The approach decomposes complex tests into logically clearer ones and improves semantic clarity through a combination of program analysis and LLM-based rewriting. We evaluated CLAST on four open-source and three industrial projects. The results demonstrate that CLAST largely outperforms UTgen, the state-of-the-art refinement technique, in both preserving test effectiveness and enhancing semantic clarity. Specifically, CLAST fully retains the original effectiveness of unit tests, while UTgen reduces compilation success rate (CSR), pass rate (PR), and test coverage (Cov) by an average of 12.90%, 35.82%, an 4.65%, respectively. Over 85.33% of participants in our user study preferred the semantic clarity of CLAST-refined tests. Notably, incorporating \tech-refined tests as examples effectively improves ICL-based unit test generation approaches such as RAGGen and TELPA, resulting in an average increase of 25.97% in CSR, 28.22% in PR, and 45.99% in Cov for generated tests, compared to incorporating UTgen-refined tests. The insights from the follow-up user study not only reinforce CLAST’s potential impact in software testing practice but also illuminate avenues for future research.


## 7. Comprehend, Imitate, and then Update: Unleashing the Power of LLMs in Test Suite Evolution

**Authors:** Tangzhi Xu (Nanjing University), Jianhan Liu (Nanjing University), Yuan Yao (Nanjing University), Cong Li (ETH Zurich), Feng Xu (Nanjing University), Xiaoxing Ma (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334264

**中文总结:** 提出 CommitUp，模仿人类「理解代码变更—检索相似示例—更新测试」流程，用 LLM 自动化修复过时的方法级测试代码；在真实 Java 项目上编译、运行无失败与完整覆盖率更新的成功率分别达 96.4%、94.4%、93.1%。

**Abstract:** Software testing plays a crucial role in software engineering, ensuring the reliability and correctness of evolving systems.Well-maintained test suites are essential for ensuring software quality.However, in modern development cycles that emphasize rapid feature iteration, the co-evolution of test suites often lags behind, leading to more appearance of obsolete tests.To this end, automated approaches for updating obsolete test code have been proposed, and recent approaches have achieved the state-of-the-art performance with the support of large language models (LLMs). This paper presents CommitUp, a new approach that leverages LLMs to effectively automate method-level obsolete test code updates.CommitUp mimics how humans solve the problem, first comprehending the code modifications, searching for similar examples to imitate, and finally performing the update.We evaluate CommitUp on a curated dataset from real-world Java projects. The results demonstrate the superior performance of CommitUp, achieving 96.4%, 94.4%, 93.1% success rates for generating compilable, runtime failure-free, and full coverage updates, respectively. We believe our study can provide new insight into LLM-based test code update. The dataset and code are available at https://anonymous.4open.science/r/CommitUp .


## 8. DebCovDiff: Differential Testing of Coverage Measurement Tools on Real-World Projects

**Authors:** Wentao Zhang (University of Illinois Urbana-Champaign), Jinghao Jia (University of Illinois Urbana-Champaign), Erkai Yu (University of Illinois Urbana-Champaign), Darko Marinov (University of Illinois at Urbana-Champaign), Tianyin Xu (University of Illinois at Urbana-Champaign)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334524

**中文总结:** 提出 DebCovDiff，以 Debian 包为输入对 Gcov 与 LLVM-cov 做差分测试，覆盖行覆盖及两种高级覆盖指标，并设计鲁棒 oracle 过滤细微差异；在真实项目上首次系统揭示覆盖率度量工具的缺陷。

**Abstract:** Measuring code coverage is a critical practice in software testing. Incorrect or misleading coverage information reported by automatic tools can increase the software development cost and lead to negative consequences especially for safety-critical software. Ensuring the correctness of coverage measurement tools is therefore important. Prior studies have applied various techniques to find bugs in Gcov and LLVM-cov, the two most widely used coverage tools for C/C++. However, those studies had two limiting factors. First, they used only small, often synthetic, programs, potentially missing bugs in real-world scenarios. Second, they focused only on basic line coverage, neglecting advanced metrics that are both more complex to implement and commonly required for safety-critical software.

This paper presents the first empirical study of coverage measurement tools for real-world projects. We implement DebCovDiff, a testing framework that takes Debian packages as the input programs and performs differential testing of Gcov and LLVM-cov, for line coverage and two advanced coverage metrics. We design robust differential oracles to (1) filter out discrepancies arising from subtle differences in the tool output presentation, (2) overcome the nondeterministic nature of certain packages, and (3) support advanced coverage metrics. From results on 47 Debian packages, we identify 34 new bugs, including 2 crashing bugs and 32 deeper bugs that produce wrong coverage reports.


## 9. DNAFuzz: Descriptor-Aware Fuzzing for USB Drivers

**Authors:** Zhengshu Wang (Hubei University), Peng He (Hubei University), Fuchen Ma (Tsinghua University), Yuanliang Chen (Tsinghua University), Shuoshuo Duan (Shuimu Yulin Technology Co., Ltd), Yiyuan Bai (Shuimu Yulin Technology Co., Ltd), Yu Jiang (Tsinghua University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334375

**中文总结:** 提出 DNAFuzz，解析 USB 描述符的类型、标签与范围约束并据此生成语义感知的 fuzz 载荷，提高通过主机输入校验的有效测试用例比例；在多版本 Linux USB 驱动上优于现有 fuzzer 并发现漏洞。

**Abstract:** USB is an interface standard widely used in modern operating systems to connect computers to various external devices. External devices can launch attacks by injecting random data into the host via USB, resulting in memory errors or even system-level crashes. Fuzzing has been proven to be an effective method to detect USB driver vulnerabilities. However, existing fuzzing methods generate testing inputs without considering the format and semantic of USB descriptors, which define device functionalities. Thus, many test cases fail to pass the host’s input validation mechanism, resulting in ineffective testing. In this paper, we propose DNAFuzz, a USB driver fuzzer that generates descriptor-aware payload. First, it utilizes USB specifications to parse USB descriptors and extracts the precise input types, tags, and range constraints of each descriptor item. Then, based on the extracted item attributes and the interpreted semantic information of the descriptors, DNAFuzz guides the payload generation. This approach improves the quality of test cases and the fuzzing effectiveness. Currently, we have tested DNAFuzz on multiple versions of Linux kernel USB drivers, and compared it with state-of-the-art fuzzers such as USBFuzz and Syzkaller. Results show that DNAFuzz significantly improves input quality, successfully increasing the proportion of tests with execution times exceeding 2 seconds by 358% and 65%. In addition, DNAFuzz detected 15 bugs, 11 of which have been fixed or confirmed by the corresponding maintainers.


## 10. Do LLMs Generate Useful Test Oracles? An Empirical Study with an Unbiased Dataset

**Authors:** Davide Molinelli (USI Lugano; Schaffhausen Institute of Technology), Luca Di Grazia (University of St. Gallen), Alberto Martin-Lopez (Software Institute - USI, Lugano), Michael D. Ernst (University of Washington), Mauro Pezze (Università della Svizzera italiana (USI) and Università degli Studi di Milano Bicocca)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334509

**中文总结:** 基于 135 个 Java 项目、13,866 条截断日期后的无偏测试 oracle 数据，实证表明 LLM 能生成有效 test oracle 并显著提升变异测试分数，缓解 EvoSuite/Randoop 等隐式与回归 oracle 的语义盲区。

**Abstract:** The oracle problem — the efficient generation of thorough test oracles — is still an open problem. Popular test case generators, like EvoSuite and Randoop, rely on implicit, rule-based, and regression oracles that miss failures that depend on the semantics of the program under test. Specified test oracles shift the costs of generating oracles to the production of formal specifications.

Large Language Models (LLMs) have the potential to over-come these limitations. The few studies of using LLM to automatically generate test oracles validate LLMs on modest-sized public benchmarks, such as Defects4J, that are likely to be included in the LLM training benchmark, with severe threats to the validity of the results.

This paper presents an empirical study of the effectiveness of LLMs in generating test oracles. We report the results of experimenting with 13,866 test oracles that we mined from 135 Java projects, and that were created after the cut-off dates of the training of the LLMs used in the experiments, and are thus unbiased.

The results of the experiments that we report in this paper indicate that LLMs indeed generate effective oracles that largely increase the mutation score of the test cases, reaching a mutation score comparable to the score of human-designed test oracles. Our results also indicate that the test prefix and the methods called in the program under test provide sufficient information to generate good oracles, while additional code context does not bring relevant benefits. These findings provide actionable insights into using LLMs for automatic testing and highlight their current limitations in generating complex oracles.


## 11. DRIFT: Debug-based Trace Inference for Firmware Testing

**Authors:** Changming Liu (Northeastern University), Alejandro Mera (Northeastern University), Meng Xu (University of Waterloo), Engin Kirda (Northeastern University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334624

**中文总结:** 提出 DRIFT，利用 ARM Cortex-M 广泛可用的 Debug Monitor 做半主机式二进制固件 fuzz，以轻量静态分析提供紧凑完整覆盖率反馈，避免传统 HiL 对高端 trace 硬件与慢速执行的依赖。

**Abstract:** Binary firmware fuzzing has garnered attention in recent years. Compared to source-code-based approaches, binary approaches require less semantic information and are therefore more applicable. This is particularly relevant in firmware analysis, as most firmware vendors distribute only binaries, withholding source code due to proprietary concerns.

Pivoting away from the traditional hardware-in-the-loop (HiL) methodology, researchers are exploring more efficient ways to engage real hardware for fuzzing. However, existing approaches have inherent drawbacks, such as reliance on high-end hardware features, inability to recover complete coverage, and slow execution speeds. We propose DRIFT, a novel approach for on-device binary firmware testing that follows the semihosting methodology. DRIFT addresses all the aforementioned drawbacks. Instead of relying on high-end hardware tracing units or debug probes, DRIFT leverages the Debug Monitor—a CPU feature widely available in nearly all ARM Cortex-M chips. Additionally, DRIFT delivers compact and complete coverage feedback for fuzzing. DRIFT achieves this by employing lightweight static analysis of the firmware. The pre-knowledge gained from this analysis is directly embedded into the binary, enabling the firmware to trace itself. This self-tracing approach minimizes interference from the workstation, significantly boosting fuzzing performance.

We designed DRIFT to be highly flexible, accommodating a number of hardware resource limitations. When applied to new firmware, DRIFT discovered three previously unknown bugs that were not identified by existing binary fuzzing techniques. Furthermore, DRIFT outperforms all state-of-the-art binary firmware fuzzers in terms of speed and fidelity, trailing only SHiFT, an approach that requires source code.


## 12. DualFuzz: Detecting Vulnerability in Wi-Fi NICs through Dual-Directional Fuzzing

**Authors:** Yuanliang Chen (Tsinghua University), Fuchen Ma (Tsinghua University), Yanyang Zhao (Tsinghua University), Yuanyi Li (Shuimu Yulin Technology Co., Ltd), Yu Jiang (Tsinghua University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334315

**中文总结:** 提出 DualFuzz，构建传输-接收交互模型 TRModel 并同步 fuzz Wi-Fi NIC 收发双向逻辑，配合延迟引导 fuzz 与活性/等价检测；在 8 款主流 NIC 上发现传统单向 fuzz 遗漏的漏洞。

**Abstract:** Wi-Fi Network Interface Cards (NICs) are vital for enabling wireless connectivity across a wide range of devices. Ensuring their security is critical, as vulnerabilities can expose entire networks to threats. Fuzzing is a promising technique for detecting such flaws. However, existing Wi-Fi fuzzers typically test transmission and reception separately, overlooking their interactions and resulting in inefficient testing.

In this work, we present DualFuzz, a dual-directional fuzzing framework designed to simultaneously test both transmission and reception processes in Wi-Fi NICs. First, DualFuzz automatically identifies interaction behaviors within Wi-Fi NICs and constructs a Transmission-Reception Model (TRModel) to characterize Wi-Fi frames that influence these interactions. Leveraging this model, DualFuzz utilizes latency guided fuzzing to efficiently coordinate exploring transmission and reception interaction logics. Finally, we propose liveness and equivalence detectors that enable real-time monitoring to identify abnormal states and uncover potential vulnerabilities in Wi-Fi NICs. We implemented and evaluated DualFuzz on eight widely used Wi-Fi NICs, incorporating chipsets from various manufacturers (e.g., Intel and Realtek). Compared to state-of-the-art Wi-Fi fuzzers like OwFuzz, wpaspy, and Greyhound, DualFuzz detects 75%, 163%, and 250% more vulnerabilities, respectively. In total, it uncovered 21 previously unknown vulnerabilities, 7 of which have been assigned CVEs. All have been confirmed and fixed by the corresponding maintainers.


## 13. Enhancing LLM’s Ability to Generate More Repository-Aware Unit Tests Through Precise Context Injection

**Authors:** Xin Yin (Zhejiang University), Chao Ni (Zhejiang University), Xinrui Li (Zhejiang University), Liushan Chen (Douyin Co., Ltd.), Guojun Ma (Douyin Co., Ltd.), Xiaohu Yang (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334603

**中文总结:** 提出 RATester，集成 gopls 在 Go 单测生成中动态查找未知标识符的定义与文档注释并注入 LLM，避免固定上下文模式的冗余或不足；在真实 Go 项目上显著优于基线的覆盖率与生成效率。

**Abstract:** Recently, Large Language Models (LLMs) have gained attention for their ability to handle a broad range of tasks, including unit test generation. Despite their success, LLMs may exhibit hallucinations when generating unit tests for focal methods or functions due to their lack of awareness regarding the project’s global context. While many studies have explored the role of context, they often extract fixed patterns of context for different models and focal methods, which may not be suitable for all generation processes (e.g., excessive irrelevant context could lead to redundancy, preventing the model from focusing on essential information). To overcome this limitation, we propose RATester, which integrates the language server gopls to provide dynamic definition lookup to assist the LLM. When RATester encounters an unfamiliar identifier, it first leverages gopls to fetch relevant definitions and documentation comments, and then uses this global knowledge to guide the LLM. We evaluate the effectiveness and efficiency of RATester compared to baseline approaches by constructing a new Golang dataset from real-world projects. On our dataset, RATester achieves an average line coverage of 26.25%, representing an improvement of 16.30% to 165.69% over the baselines. Furthermore, RATester shows superior performance in mutation testing, successfully killing 25 to 147 more mutants than the baseline approaches.


## 14. Exact Inference for Quantum Circuits: A Testing Oracle for Quantum Software Stacks

**Authors:** Kanguk Lee (KAIST), Jaemin Hong (KAIST), Sukyoung Ryu (KAIST)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334221

**中文总结:** 提出 QASMInfer，为 OpenQASM 2.0 量子电路精确推断输出概率分布，作为量子软件栈变换器与模拟器的统一测试 oracle；可支持动态电路并检测非崩溃类缺陷。

**Abstract:** Quantum software stacks (QSSs), which provide quantum circuit transformers and simulators, enable circuit transformations and the execution of circuits on classical computers. Despite their importance, they have not been effectively tested yet, leaving the correctness in question. The main obstacle to testing is the absence of a testing oracle to determine the correct behavior of transformers and simulators. While previous studies have employed differential and metamorphic testing to circumvent the necessity for an oracle, they have failed to detect non-crash bugs. In this work, we address this gap by introducing QASMInfer, an exact inference system for quantum circuits, which computes the probability distribution of possible circuit outcomes. By supporting circuits written in OpenQASM 2.0, the de facto standard quantum assembly language used by most QSSs, QASMInfer acts as a unified testing oracle for multiple QSSs. Our design of QASMInfer achieves three key goals: (1) support for dynamic circuits, an important class of quantum circuits, (2) efficiency, and (3) reliability. For efficiency, we introduce two optimizations and an efficient matrix representation. For reliability, we prove physical consistency, ensuring that QASMInfer’s inference results adhere to the physical principles of quantum computing. To simplify the proof, we introduce OpenQASMCore, a core language for OpenQASM, and perform exact inference for OpenQASM by desugaring it to OpenQASMCore. Our implementation and proof are fully mechanized in the Coq proof assistant. Testing six real-world QSSs using QASMInfer revealed 20 bugs, including 15 non-crash bugs, demonstrating QASMInfer’s effectiveness as a testing oracle.


## 15. Execution-Aware Program Reduction for WebAssembly via Record and Replay

**Authors:** Doehyun Baek (University of Stuttgart), Daniel Lehmann (Google, Germany), Ben L. Titzer (Carnegie Mellon University), Sukyoung Ryu (KAIST), Michael Pradel (CISPA Helmholtz Center for Information Security)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334546

**中文总结:** 提出 RR-Reduce 与 Hybrid-Reduce，基于 record-and-replay 利用执行行为做 WebAssembly 程序缩减；在 28 个触发三引擎 bug 的程序上平均缩至原大小的 1.20%。

**Abstract:** WebAssembly (Wasm) programs may trigger bugs in their engine implementations. To aid debugging, program reduction techniques try to produce a smaller variant of the input program that still triggers the bug. However, existing execution-unaware program reduction techniques struggle with large and complex Wasm programs, because they rely on static information and apply syntactic transformations, while ignoring the valuable information offered by the input program’s execution behavior.

We present RR-Reduce and Hybrid-Reduce, novel execution-aware program reduction techniques that leverage execution behaviors via record and replay. RR-Reduce identifies a bug- triggering function as the target function, isolates that function from the rest of the program, and generates a reduced program that replays only the interactions between the target function and the rest of the program. Hybrid-Reduce combines a complementary execution-unaware reduction technique with RR-Reduce to further reduce program size.

We evaluate RR-Reduce and Hybrid-Reduce on 28 Wasm programs that trigger a diverse set of bugs in three engines. On average, RR-Reduce reduces the programs to 1.20% of their original size in 14.5 minutes, which outperforms the state of the art by 33.15× in terms of reduction time. Hybrid-Reduce reduces the programs to 0.13% of their original size in 3.5 hours, which outperforms the state of the art by 3.42× in terms of reduced program size and 2.26× in terms of reduction time. We envision RR-Reduce as the go-to tool for rapid, on-demand debugging in minutes, and Hybrid-Reduce for scenarios where developers require the smallest possible programs.


## 16. FailMapper: Automated Generation of Unit Tests Guided by Failure Scenarios

**Authors:** ruiqi dong (Swinburne University of Technology), Zehang Deng (Swinburne University of Technology), Xiaogang Zhu (Adelaide University), Xiaoning Du (Monash University), Huai Liu (Swinburne University of Technology), Shaohua Wang (Central University of Finance and Economics), Sheng Wen (Swinburne University of Technology), Yang Xiang (Digital Research & Innovation Capability Platform, Swinburne University of Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334488

**中文总结:** 提出 FailMapper，归纳九类失败场景并设计对应触发策略，以 Monte Carlo Tree Search 系统探索故障空间来指导单元测试生成；相比单纯追求覆盖率更能有效生成触发 bug 的测试。

**Abstract:** The automation of unit test generation has become a critical task for improving the overall efficiency of software development testing. Many existing techniques attempt to generate a sufficient number of test cases to achieve high code coverage. However, it has been shown that a high coverage does not necessarily guarantee effective bug discovery. A potential enhancement is to guide the unit test generation based on bug properties. However, this solution is challenged by the large number and diversity of bug types, making it difficult to comprehensively summarize bug properties.

We observe that, failures, presented as the results of bugs, manifest in a limited number of scenarios. Therefore, instead of bug properties, in this paper, we propose an innovative framework, named FailMapper, which uses failure scenarios to guide the generation of unit tests. We summarize nine failure scenarios, and design the corresponding failure-triggering test strategies. This significantly improves the efficacy of generating test cases towards triggering bugs. To systematically explore possible failure scenarios, FailMapper employs the Monte Carlo Tree Search (MCTS) algorithm to search the faults that may lead to a failure. Experiments demonstrate that, on 50 known bugs in the Defects4J benchmark, FailMapper can detect much more bugs than five typical unit testing approaches, including EvoSuite, Randoop, CoverUp, HITS, and SymPrompt (40 versus at most 12, out of all 50 bugs). FailMapper can also reveal 36 previously undiscovered bugs, further demonstrating its effectiveness. The experimental results clearly show that our new framework can significantly enhance the overall efficacy of unit testing.


## 17. FlakyGuard: Automatically Fixing Flaky Tests at Industry Scale

**Authors:** Chengpeng Li (University of Texas at Austin), Farnaz Behrang (Uber Technologies), August Shi (The University of Texas at Austin), Peng Liu (Uber Technologies)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334450

**中文总结:** 提出 FlakyGuard，将代码建模为图并选择性图遍历为 LLM 提供恰当上下文以修复 flaky test；在工业仓库上修复 47.6% 可复现 flaky test，51.8% 补丁被开发者接受，成功率比 SOTA 至少高 22%。

**Abstract:** Flaky tests that non-deterministically pass or fail waste developer time and slow release cycles. While large language models (LLMs) show promise for automatically repairing flaky tests, existing approaches like FlakyDoctor fail in industrial settings due to the context problem: providing either too little context (missing critical production code) or too much context (overwhelming the LLM with irrelevant information). We present FlakyGuard, which addresses this problem by treating code as a graph structure and using selective graph exploration to find only the most relevant context. Evaluation on real-world flaky tests from industrial repositories shows that FlakyGuard repairs 47.6% of reproducible flaky tests with 51.8% of the fixes accepted by developers. Besides it outperforms state-of-the-art approaches by at least 22% in repair success rate. Developer surveys confirm that 100% find FlakyGuard’s root cause explanations useful.


## 18. Function Clustering-Based Fuzzing Termination: Toward Smarter Early Stopping

**Authors:** Liang Ding (University of Science and Technology of China), Wenzhang Yang (Institute of AI for industries), Yinxing Xue (Institute of AI for Industries, Chinese Academy of Sciences)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334636

**中文总结:** 提出基于函数聚类的 fuzzing 早停准则，用 LLM 编码函数并融合多指标确定聚类数，建立聚类与漏洞分布关系以更智能地决定何时停止 fuzzing；相比函数覆盖率等传统指标避免过度或过早终止。

**Abstract:** Fuzzing is a testing technique that generates a large number of inputs to cause program crashes. As large language models grow, so do the programs developed with their assistance, leading to an exponential increase in code complexity and function counts. Performing comprehensive fuzz testing on all functions has become increasingly challenging and resource-intensive. Current methods for determining when to stop fuzz testing activities rely on metrics such as function coverage, vulnerability function coverage or crash count. However, these metrics fail to account for the scale of the functions under test. For example, function coverage may lead to excessive testing on non-critical functions, while vulnerability function coverage can result in premature termination if the estimated number of vulnerability functions is too low.

This paper introduces a novel fuzzing testing termination criterion based on function clustering. We compare our criterion with three existing methods.Fisrt, by leveraging langurage model for function encoding and a multi-metric fusion algorithm for determining the number of clusters, we establish a relationship between function clustering and vulnerability distribution. Second, our experiments on eight function libraries demonstrate that the proposed termination criterion significantly improves testing efficiency, reducing fuzzing time by 1.4–7.2 hours (5–30%) across different configurations while maintaining minimal bug loss (averaging 0.25 bugs), outperforming existing criteria like vulnerability function coverage-based approaches.


## 19. HFUZZER: Testing Large Language Models for Package Hallucinations via Phrase-based Fuzzing

**Authors:** Yukai Zhao, Menghan Wu (Zhejiang University), Xing Hu (Zhejiang University), Xin Xia (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334594

**中文总结:** 提出 HFUZZER 短语 fuzzing 框架，从包信息或 coding task 提取短语引导 LLM 生成多样相关编码任务以测试包幻觉；在多 LLM 上有效触发更多非存在包的推荐，助力防御供应链攻击。

**Abstract:** Large Language Models (LLMs) are widely used for code generation, but they face critical security risks when applied to practical production due to package hallucinations, in which LLMs recommend non-existent packages. These hallucinations can be exploited in software supply chain attacks, where malicious attackers exploit them to register harmful packages. It is critical to test LLMs for package hallucinations to mitigate package hallucinations and defend against potential attacks. Although researchers have proposed testing frameworks for fact-conflicting hallucinations in natural language generation, there is a lack of research on package hallucinations. To fill this gap, we propose HFUZZER, a novel phrase-based fuzzing framework to test LLMs for package hallucinations. HFUZZER adopts fuzzing technology and guides the model to infer a wider range of reasonable information based on phrases, thereby generating enough and diverse coding tasks. Furthermore, HFUZZER extracts phrases from package information or coding tasks to ensure the relevance of phrases and code, thereby improving the relevance of generated tasks and code. We evaluate HFUZZER on multiple LLMs and find that it triggers package hallucinations across all selected models. Compared to the mutational fuzzing framework, HFUZZER identifies 2.36× more unique hallucinated packages. Additionally, when testing the model GPT-4o, HFUZZER finds 46 unique hallucinated packages. Further analysis shows that LLMs are prone to package hallucinations not only when generating code but also when assisting with environment configuration.


## 20. Interleaved Learning and Exploration: A Self-Adaptive Fuzz Testing Framework for MLIR

**Authors:** Zeyu Sun (Institute of Software, Chinese Academy of Sciences), Jingjing Liang (East China Normal University), Weiyi Wang (Institute of Software, Chinese Academy of Sciences), Chenyao Suo (Tianjin University), Junjie Chen (Tianjin University), Fanjiang Xu (Institute of Software at Chinese Academy of Sciences)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334665

**中文总结:** 提出 FLEX 自适应 MLIR fuzzing 框架，交错神经网络程序生成、扰动采样与崩溃/非崩溃样本反馈增强；30 天发现 80 个未知 bug（含多种 parser 根因），24 小时活动亦优于四类 SOTA fuzzer。

**Abstract:** MLIR (Multi-Level Intermediate Representation) has rapidly become a foundational technology for modern com- piler frameworks, enabling extensibility across diverse domains. However, ensuring the correctness and robustness of MLIR itself remains challenging. Existing fuzzing approaches—based on manually crafted templates or rule-based mutations—struggle to generate sufficiently diverse and semantically valid test cases, making it difficult to expose subtle or deep-seated bugs within MLIR’s complex and evolving code space. In this paper, we present FLEX, a novel self-adaptive fuzzing framework for MLIR. FLEX leverages neural networks for program generation, a perturbed sampling strategy to encourage diversity, and a feedback-driven augmentation loop that iteratively improves its model using both crashing and non-crashing test cases. Starting from a limited seed corpus, FLEX progressively learns valid syntax and semantics and autonomously produces high-quality test inputs. We evaluate FLEX on the upstream MLIR compiler against four state-of-the-art fuzzers. In a 30-day campaign, FLEX discovers 80 previously unknown bugs—including multiple new root causes and parser bugs—while in 24-hour fixed-revision comparisons, it detects 53 bugs (over 3.5× as many as the best baseline) and achieves 28.2% code coverage, outperforming the next-best tool by 42%. Ablation studies further confirm the critical role of both perturbed generation and diversity augmentation in FLEX ’s effectiveness.


## 21. Learning from the Past: Real-World Exploit Migration for Smart Contract PoC Generation

**Authors:** Kairan Sun (Nanyang Technological University), Zhengzi Xu (Imperial Global Singapore), Kaixuan Li (Nanyang Technological University), Lyuye Zhang (Nanyang Technological University), Yebo Feng (Nanyang Technological University), Daoyuan Wu (Lingnan University), Yang Liu (Nanyang Technological University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334698

**中文总结:** 提出基于漏洞迁移的智能合约 PoC 生成：从已记录安全事件中抽取关键信息，将已验证 exploit 模式迁移到相似漏洞代码，而非从零合成；利用合约高复用率，能生成覆盖真实事件复杂交易依赖的 PoC。

**Abstract:** Smart contract vulnerabilities continue to cause significant financial losses, despite the implementation of security measures such as manual audits and bug bounty platforms. A critical component often required by these security measures is the proof-of-concept (PoC) exploit, which validates vulnerability exploitability, assesses impact severity, and guides developers in fixes. Existing tools have explored automated PoC generation with techniques like symbolic execution, fuzzing, and program synthesis. However, these approaches frequently fail to generate PoCs for vulnerabilities exploited in real-world incidents, primarily due to their limitations in handling complex transaction dependencies, navigating vast on-chain state spaces, or requiring extensive manual specifications.

Our migration-based approach extracts critical information from documented security incidents and applies it to generate PoCs for similar vulnerable code. This approach leverages proven exploit patterns rather than generating PoCs from scratch. This approach is motivated by two key observations: the prevalence of code reuse in smart contracts (up to 90% at the function level) and the increasing availability of documented PoCs for real-world incidents. Our approach operates in three phases: \textit{(1)} abstracting essential components (i.e., environment properties, attack logic, and verification checks) from existing PoCs into templates, \textit{(2)} given a new target contract, selecting suitable templates with adapted values through clone-detection and property-feasibility analysis, and \textit{(3)} generating and validating PoCs in simulated environments. Our evaluation demonstrates both effectiveness and efficiency: our approach successfully generates valid PoCs for 62 out of 67 manually validated cases without false positives. Our approach also achieves significant performance gains, completing analysis in 3.8 hours compared to 133.2 and 210.5 hours required by existing tools. By the submission date, we have validated 256 vulnerable contracts on-chain, including 64 cross-chain cases, demonstrating the ability of our tool to migrate PoCs across diverse blockchain environments.


## 22. LLMs for Automated Unit Test Generation and Assessment in Java: The AgoneTest Framework

**Authors:** Andrea Lops (Polytechnic University of Bari, Italy), Fedelucio Narducci (Polytechnic University of Bari), Azzurra Ragone (University of Bari), Michelantonio Trizio (Wideverse), Claudio Bartolini (Wideverse s.r.l.)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334272

**中文总结:** 提出 AgoneTest 框架与 Classes2Test 数据集，用 LLM 为 Java  focal class 自动生成单元测试，并以变异覆盖率、test smell 等指标综合评估；可编译测试中，LLM 生成测试在覆盖与缺陷检出上可匹敌甚至超越人工测试。

**Abstract:** Unit testing is an essential but resource-intensive step in software development, ensuring individual code units function correctly. This paper introduces AgoneTest, an automated system designed to generate and evaluate unit test suites for real-world Java projects using Large Language Models (LLMs). We provide a newly developed Classes2Test dataset, which maps Java focal classes to their test counterparts, and a framework that integrates advanced evaluation metrics, such as mutation coverage and test smells, for a comprehensive assessment. Experimental results show that, for the subset of tests that compile, LLM-generated tests can match or exceed human-written tests in terms of coverage and defect detection. Enhanced prompting strategies also contribute to test quality. AgoneTest automatically evaluates the potential of LLMs in automating software testing, offering insights for future improvements in model design, prompt engineering, and testing practices.


## 23. LSPFuzz: Hunting Bugs in Language Servers

**Authors:** Hengcheng Zhu (The Hong Kong University of Science and Technology), Songqiang Chen (The Hong Kong University of Science and Technology), Valerio Terragni (University of Auckland), Lili Wei (McGill University), Yepang Liu (Southern University of Science and Technology), Jiarong Wu, Shing-Chi Cheung (Hong Kong University of Science and Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334451

**中文总结:** 提出 LSPFuzz 面向 Language Server 的灰盒混合 fuzz：两阶段对源码做语法感知变异、再上下文感知调度编辑器操作，系统性探索代码与 LSP 交互组合；在四种主流 language server 上优于基线并发现此前未知缺陷。

**Abstract:** The Language Server Protocol (LSP) has revolutionized the integration of code intelligence in modern software development. There are approximately 300 LSP server implementations for various languages and 50 editors offering LSP integration. However, the reliability of LSP servers is a growing concern, as crashes can disable all code intelligence features and significantly impact productivity, while vulnerabilities can put developers at risk even when editing untrusted source code. Despite the widespread adoption of LSP, no existing techniques specifically target LSP server testing. To bridge this gap, we present LSPFuzz, a grey-box hybrid fuzzer for systematic LSP server testing. Our key insight is that effective LSP server testing requires holistic mutation of source code and editor operations, as bugs often manifest from their combinations. To satisfy the sophisticated constraints of LSP and effectively explore the input space, we employ a two-stage mutation pipeline: syntax-aware mutations to source code, followed by context-aware dispatching of editor operations. We evaluated LSPFuzz on four widely used LSP servers. LSPFuzz demonstrated superior performance compared to baseline fuzzers, and uncovered previously unknown bugs in real-world LSP servers. Of the 51 bugs we reported, 42 have been confirmed, 26 have been fixed by developers, and two have been assigned CVE numbers. Our work advances the quality assurance of LSP servers, providing both a practical tool and foundational insights for future research in this domain.


## 24. Metamorphic Testing for Audio Content Moderation Software

**Authors:** Wenxuan Wang (Hong Kong University of Science and Technology), Yongjiang Wu (The Chinese University of Hong Kong), Junyuan Zhang (The Chinese University of Hong Kong), Shuqing Li (The Chinese University of Hong Kong), Yun Peng (The Chinese University of Hong Kong), Wenting Chen (City University of Hong Kong), Shuai Wang (Hong Kong University of Science and Technology), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334513

**中文总结:** 提出 MTAM 音频内容审核软件的蜕变测试框架，基于 2000 条音频试点定义 14 条蜕变关系（音频特征扰动与启发式扰动），检测 pitch/噪声等细微改动导致的审核绕过；揭示主流音频 moderation 工具对对抗输入的脆弱性。

**Abstract:** The rapid growth of audio-centric platforms and applications such as WhatsApp and Twitter has transformed the way people communicate and share audio content in modern society. However, these platforms are increasingly misused to disseminate harmful audio content, such as hate speech, deceptive advertisements, and explicit material, which can have significant negative consequences (e.g., detrimental effects on mental health). In response, researchers and practitioners have been actively developing and deploying audio content moderation tools to tackle this issue. Despite these efforts, malicious actors can bypass moderation systems by making subtle alterations to audio content, such as modifying pitch or inserting noise. Moreover, the effectiveness of modern audio moderation tools against such adversarial inputs remains insufficiently studied. To address these challenges, we propose MTAM, a \underline{M}etamorphic \underline{T}esting framework for \underline{A}udio content \underline{M}oderation software. Specifically, we conduct a pilot study on $2000$ audio clips and define 14 metamorphic relations across two perturbation categories: Audio Features-Based and Heuristic perturbations. MTAM applies these metamorphic relations to toxic audio content to generate test cases that remain harmful while being more likely to evade detection. In our evaluation, we employ MTAM to test five commercial textual content moderation software and an academic model against three kinds of toxic content. The results show that MTAM achieves up to $38.6%$, $18.3%$, $35.1%$, $16.7%$, and $51.1%$ error finding rates (EFR) when testing commercial moderation software provided by Gladia, Assembly AI, Baidu, Nextdata, and Tencent respectively, and it obtains up to $45.7%$ EFR when testing the state-of-the-art algorithms from the academy. In addition, we leverage the test cases generated by MTAM to retrain the model we explored, which largely improves model robustness (nearly $0%$ EFR) while maintaining the accuracy on the original test set.


## 25. Navigating the Labyrinth: Path-Sensitive Unit Test Generation with Large Language Models

**Authors:** Dianshu Liao (the Australian National University), Xin Yin (Zhejiang University), Shidong Pan (Columbia University & New York University), Chao Ni (Zhejiang University), Zhenchang Xing (CSIRO's Data61), Xiaoyu Sun (Australian National University, Australia)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334655

**中文总结:** 提出路径敏感单元测试框架 JUnitGenie，从 Java 项目抽取代码知识并构造结构化 prompt 引导 LLM 覆盖深层控制流；在 10 个真实项目 2258 个复杂 focal method 上生成有效测试并提升覆盖率。

**Abstract:** Unit testing is essential for software quality assurance, yet writing and maintaining tests remains time-consuming and error-prone. To address this challenge, researchers have proposed various techniques for automating unit test generation, including traditional heuristic-based methods and more recent approaches that leverage large language models (LLMs) for test synthesis. However, these existing approaches are inherently path-insensitive because they rely on fixed heuristics or limited contextual information and fail to reason about deep control-flow structures. As a result, they often struggle to achieve adequate coverage, particularly for deep or complex execution paths. In this work, we present a path-sensitive framework, JUnitGenie, to fill this gap by combining code knowledge with the semantic capabilities of LLMs in guiding context-aware unit test generation. After extracting code knowledge from Java projects, JUnitGenie distills this knowledge into structured prompts to guide the generation of high-coverage unit tests. We evaluate JUnitGenie  on 2,258 complex focal methods from ten real-world Java projects. The results show that JUnitGenie generates valid tests and improves branch and line coverage by 29.60% and 31.00% on average over both heuristic and LLM-based baselines. We further demonstrate that the generated test cases can uncover real-world bugs, which were later confirmed and fixed by developers.


## 26. ORFuzz: Fuzzing the "Other Side" of LLM Safety – Testing Over-Refusal

**Authors:** Haonan Zhang (Zhejiang University), Dongxia Wang (Zhejiang University), Yi Liu (Nanyang Technological University), Kexin Chen (Zhejiang University), Jiashui Wang (Zhejiang University), Xinlei Ying (Ant Group), Long Liu (Ant Group), Wenhai Wang (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334477

**中文总结:** 提出首个 LLM 过度拒绝（over-refusal）进化测试框架 ORFuzz，集成安全类别种子选择、推理 LLM 自适应变异与 human-aligned 评判 OR-JUDGE；过度拒绝检出率约为基线 2 倍以上，并构建 ORFuzzSet 基准。

**Abstract:** Large Language Models (LLMs) have been found to show over-refusal problems-erroneously rejecting benign queries due to overly conservative safety measures-a critical functional flaw that undermines their reliability and usability. Current methods for testing this behavior are demonstrably inadequate, suffering from flawed benchmarks and limited test generation capabilities, as highlighted by our empirical user study. To the best of our knowledge, this paper introduces the first evolutionary testing framework, ORFUZZ, for the systematic detection and analysis of LLM over-refusals. ORFUZZ uniquely integrates three core components: (1) safety category-aware seed selection for comprehensive test coverage, (2) adaptive mutator optimization using reasoning LLMs to generate effective test cases, and (3) OR-JUDGE, a human-aligned judge model validated to accurately reflect user perception of toxicity and refusal. Our extensive evaluations demonstrate that ORFUZZ generates diverse, validated over-refusal instances at a rate (6.98% average) more than double that of leading baselines, effectively uncovering vulnerabilities. Furthermore, ORFUZZ’s outputs form the basis of ORFUZZSET, a new benchmark of 1,786 highly transferable test cases that achieves a superior 57.37% average over-refusal rate across 14 diverse LLMs, significantly outperforming existing datasets. ORFUZZ and ORFUZZSET provide a robust automated testing framework and a valuable community resource, paving the way for developing more reliable and trustworthy LLM-based software systems. The code of this paper is available at: https://github.com/HotBento/ORFuzz .


## 27. PALM: Synergizing Program Analysis and LLMs to Enhance Rust Unit Test Coverage

**Authors:** Bei Chu (Nanjing University), Yang Feng (Nanjing University), Kui Liu (Huawei), Hange Shi (Nanjing University), Zifan Nan (Huawei), Zhaoqiang Guo (Software Engineering Application Technology Lab, Huawei, China), Baowen Xu (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334728

**中文总结:** 提出 PALM，用程序分析提取 Rust 函数分支条件构成路径约束，与上下文一并构造 prompt 引导 LLM 生成高覆盖单元测试；在 15 个开源 crate 上，数小时内覆盖率显著高于 SBST/concolic 及固定 prompt LLM 基线。

**Abstract:** Unit testing is essential for ensuring software reliability and correctness. Classic Search-Based Software Testing (SBST) methods and concolic execution-based approaches for generating unit tests often fail to achieve high coverage due to difficulties in handling complex program units, such as branching conditions and external dependencies. Recent work has increasingly utilized large language models (LLMs) to generate test cases, improving the quality of test generation by providing better context and correcting errors in the model’s output. However, these methods rely on fixed prompts, resulting in relatively low compilation success rates and coverage.

This paper presents PALM, an approach that leverages large language models (LLMs) to enhance the generation of high-coverage unit tests. PALM performs program analysis to identify branching conditions within functions, which are then combined into path constraints. These constraints and relevant contextual information are used to construct prompts that guide the LLMs in generating unit tests. We implement the approach and evaluate it in 15 open-source Rust crates. Experimental results show that within just two or three hours, PALM can significantly improve test coverage compared to classic methods, with increases in overall project coverage exceeding 50% in some instances and its generated tests achieving an average coverage of 72.30%, comparable to human effort (70.94%), highlighting the potential of LLMs in automated test generation. We submitted 91 PALM-generated unit tests targeting new code. Of these submissions, 80 were accepted, 5 were rejected, and 6 remain pending review. The results demonstrate the effectiveness of integrating program analysis with AI and open new avenues for future research in automated software testing.


## 28. Reflective Unit Test Generation for Precise Type Error Detection with Large Language Models

**Authors:** Chen Yang (Tianjin University), Ziqi Wang (Tianjin University), Yanjie Jiang (Peking University), Lin Yang (Tianjin University), Yuteng Zheng (Tianjin University), Jianyi Zhou (Huawei Cloud Computing Technologies Co., Ltd.), Junjie Chen (Tianjin University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334592

**中文总结:** 提出 RTED，结合逐步类型约束分析与反射式验证引导 Python 单测生成以精确检出类型错误；在 BugsInPy 与 TypeBugs 上多检出 22–29 个基准缺陷，并在 6 个开源项目中发现 12 个未知类型错误。

**Abstract:** Type errors in Python often lead to runtime failures, posing significant challenges to software reliability and developer productivity. Existing static analysis tools aim to detect such errors without execution but frequently suffer from high false positive rates. Recently, unit test generation techniques offer great promise in achieving high test coverage, but they often struggle to produce bug-revealing tests without tailored guidance. To address these limitations, we present RTED, a novel type-aware test generation technique for automatically detecting Python type errors. Specifically, RTED combines step-by-step type constraint analysis with reflective validation to guide the test generation process and effectively suppress false positives. We evaluated RTED on two widely-used benchmarks, BugsInPy and TypeBugs. Experimental results show that RTED can detect 22$\sim$29 more benchmarked type errors than four state-of-the-art techniques. RTED is also capable of producing fewer false positives, achieving an improvement of 173.9% $\sim$ 245.9% in precision. Furthermore, we applied RTED to six real-world open-source Python projects, and successfully discovered 12 previously unknown type errors, demonstrating RTED’s practical value.


## 29. Risk Estimation in Differential Fuzzing via Extreme Value Theory

**Authors:** Rafael Baez (University of Texas at El Paso), Alejandro Olivas (University of Texas at El Paso), Nathan K Diamond (University of Texas at El Paso), Marcelo F. Frias (Dept. of Software Engineering Instituto Tecnológico de Buenos Aires), Yannic Noller (Ruhr University Bochum), Saeid Tizpaz-Niari (University of Illinois Chicago)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334570

**中文总结:** 将极值理论（EVT）用于差分 fuzzing 尾部风险估计，基于已观测差异推断继续运行后更大差异/漏报的概率；在 Java 库侧信道信息泄露差分测试上验证有效性。

**Abstract:** Differential testing is a highly effective technique for automatically detecting software bugs and vulnerabilities when the specifications are not available, or they involve an analysis over multiple executions simultaneously. Differential fuzzing, in particular, operates as a random process, observing differences in outputs or behaviors between similar inputs to generate the next inputs. However, this process lacks any guarantees on the worst-case outcome: from a differential fuzzing campaign that has observed a certain difference, what is the risk of observing larger differences if we run the fuzzer for one or more steps?

This paper investigates the application of Extreme Value Theory (EVT) to address the risk of missing or underestimating differential bugs. The key observation is that differential fuzzing as a random process resembles the maximum distribution of observed differences. Hence, EVT, a branch of statistics dealing with extreme values, is an ideal framework to analyze the tail of the differential fuzzing campaign to contain the risk. We perform experiments on a set of real-world Java libraries and use a differential fuzzing that finds information leaks via side channels in these libraries. We first explore the feasibility of EVT for this task and the optimal hyperparameters for EVT distributions. We then compare EVT-based extrapolation against baseline statistical methods like Markov’s and Chebyshev’s inequalities, and the Bayes factor. EVT-based extrapolations outperform the baseline techniques in 14.3% of cases, and it ties with the baseline in 64.2% of cases. Finally, we evaluate the accuracy and performance gains of EVT-enabled differential fuzzing in real-world Java libraries, where we reported an average saving for tens of millions of byte-code executions.


## 30. RSFuzz: A Robustness-Guided Swarm Fuzzing Framework Based on Behavioral Constraints

**Authors:** Ruoyu Zhou (School of Computer Science and Technology, Xidian University, Xi'an, China; Shaanxi Key Laboratory of Network and System Security, Xidian University, Xi'an, China), Zhiwei Zhang (School of Computer Science and Technology, Xidian University, Xi'an, China; Shaanxi Key Laboratory of Network and System Security, Xidian University, Xi'an, China), Haocheng Han (School of Computer Science and Technology, Xidian University, Xi'an, China; Shaanxi Key Laboratory of Network and System Security, Xidian University, Xi'an, China), Xiaodong Zhang (University of Chinese Academy of Science), Zehan Chen (School of Computer Science and Technology, Xidian University, Xi’an, China; Shaanxi Key Laboratory of Network and System Security , Xidian University), Jun Sun (Singapore Management University), Yulong Shen (Xidian University), Dehai Xu (Yiqiyin (Hangzhou) Technology Co., Ltd. Xi'an Branch, Xi'an, China)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334416

**中文总结:** 提出 RSFuzz，以行为约束的鲁棒性度量引导多机器人集群 fuzzing，在巨大可组合参数空间中发现触发逻辑漏洞的失败场景；针对集群协作状态难以建模与评估的问题。

**Abstract:** Multi-robot swarms play an essential role in complex missions including battlefield reconnaissance, agricultural pest monitoring, as well as disaster search and rescue. Unfortunately, given the complexity of swarm algorithms, logical vulnerabilities are inevitable and often lead to severe safety and security consequences. Although various methods have been presented for detecting logical vulnerabilities through software testing, when they are used in swarm environments, these techniques face significant challenges: 1) Due to the swarm’s vast composable parameter space, it is extremely difficult to generate failure-triggering scenarios, which is crucial to effectively expose logical vulnerabilities; 2) Because of the swarm’s high flexibility and dynamism, it is challenging to model and evaluate the global swarm state, particularly in terms of cooperative behaviors, which makes it difficult to detect logical vulnerabilities.

In this work, we propose RSFuzz, a robustness-guided swarm fuzzing framework designed to detect logical vulnerabilities in multi-robot systems. It leverages the robustness of behavioral constraints to quantitatively evaluate the swarm state and guide the generation of failure-triggering scenarios. In addition, RSFuzz identifies and targets key swarm nodes for perturbations, effectively reducing the input space. Upon the RSFuzz framework, we construct two swarm fuzzing schemes, Single Attacker Fuzzing (SA-Fuzzing) and Multiple Attacker Fuzzing (MA-Fuzzing), which employ single and multiple attackers, respectively, during fuzzing to disturb swarm mission execution. We evaluated RSFuzz’s performance with three popular swarm algorithms in simulated environments. The results show that RSFuzz outperforms the state-of-the-art with an average improvement of 17.75% in effectiveness and a 38.4% increase in efficiency. We also validated some detected vulnerabilities in real-world environments. Our code and data are publicly available.


## 31. SATORI: Static Test Oracle Generation for REST APIs

**Authors:** Juan C. Alonso (Universidad de Sevilla), Alberto Martin-Lopez (Software Institute - USI, Lugano), Sergio Segura (SCORE Lab, I3US Institute, Universidad de Sevilla, Seville, Spain), Gabriele Bavota (Software Institute @ Università della Svizzera Italiana), Antonio Ruiz-Cortés (University of Seville)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334625

**中文总结:** 提出 SATORI，基于 OpenAPI 与 LLM 静态推断 REST API 响应字段预期行为生成测试 oracle，并可转为 Postman 断言；在 17 个工业 API 操作上 F1 74.3%，优于需执行的 AGORA+。

**Abstract:** REST API test case generation tools are evolving rapidly, with growing capabilities for the automated generation of complex tests. However, despite their strengths in test data generation, these tools are constrained by the types of test oracles they support, often limited to crashes, regressions, and noncompliance with API specifications or design standards. This paper introduces SATORI (Static API Test ORacle Inference), a black-box approach for generating test oracles for REST APIs by analyzing their OpenAPI Specification. SATORI uses large language models to infer the expected behavior of an API by analyzing the properties of the response fields of its operations, such as their name and descriptions. To foster its adoption, we extended the PostmanAssertify tool to automatically convert the test oracles reported by SATORI into executable assertions. Evaluation results on 17 operations from 12 industrial APIs show that SATORI can automatically generate up to hundreds of valid test oracles per operation. SATORI achieved an F1-score of 74.3%, outperforming the state-of-the-art dynamic approach AGORA+ (69.3%)—which requires executing the API—when generating comparable oracle types. Moreover, our findings show that static and dynamic oracle inference methods are complementary: together, SATORI and AGORA+ found 90% of the oracles in our annotated ground-truth dataset. Notably, SATORI uncovered 18 bugs in popular APIs (Amadeus Hotel, Deutschebahn, FDIC, GitLab, Marvel, OMDb and Vimeo) leading to documentation updates by the API maintainers.


## 32. State Field Coverage: A Metric for Oracle Quality

**Authors:** Facundo Molina (IMDEA Software Institute), Nazareno Aguirre (University of Rio Cuarto/CONICET, Argentina, and Guangdong Technion-Israel Institute of Technology, China), Alessandra Gorla (IMDEA Software Institute)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334305

**中文总结:** 提出 state field coverage 指标，通过衡量 oracle 在测试执行中可访问的对象状态字段比例来评估 oracle 质量；该指标可指导改进 oracle，使高覆盖的 oracle 更可能检出软件缺陷。

**Abstract:** The effectiveness of the testing process to reveal software defects not only depends on the characteristics of the test inputs and how thoroughly these exercise the software, but also on the quality of the oracles used to determine whether the software behaves as expected or not.  Therefore, assessing the quality of oracles is crucial to improve the overall effectiveness of the testing process.  Direct and indirect metrics have been used to assess oracle quality, but they either lack the provision of a comprehensive output that can be used to guide the improvement of the oracles, or are designed for specific types of oracles, thus lacking generality.

In this paper, we introduce \emph{state field coverage}, a novel metric to assess the quality of oracles.  Essentially, the state field coverage metric measures the proportion of the objects states, as statically defined in the corresponding classes, that may be accessed by an oracle during test execution.  The main intuition of our metric is that oracles with a higher state field coverage are more likely to detect faults in the software under analysis, as they inspect a large portion of the object states to determine whether tests pass or not.

We implement a mechanism to statically compute our state field coverage metric.  As a statically computed metric, it can be computed efficiently, and provides direct guidance on how to improve test oracles, by pointing to the state field definitions that are not examined by the test oracles.  We also evaluate state field coverage in a series of experiments comprising oracles realized in 273 representation invariants and 249,027 test assertions.  Our results show that state field coverage is a well-suited metric for assessing the quality of oracles, since it is highly correlated with the ability of the oracles to detect faults, as measured by mutation score.


## 33. TEPHRA: Principled Discovery of Fuzzer Limitations

**Authors:** Vasil Sarafov (μCSRL, CODE Research Institute, University of the Bundeswehr Munich), David Markvica (μCSRL, CODE Research Institute, University of the Bundeswehr Munich), Stefan Brunthaler (Munich Computer Systems Research Laboratory (uCSRL), CODE Research Institute, University of the Bundeswehr Munich)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334676

**中文总结:** 提出 TEPHRA 方法论，用语义引导合成生成含各类障碍的无 bug 程序以系统评估 fuzzer 能力；对 31 个当代 fuzz 系统消耗 37.4 CPU 年评估，揭示浮点条件、字符串等共性盲区并发现 AFL++ 等 fuzzer 自身缺陷。

**Abstract:** Fuzz testing has proven effective in discovering non- trivial bugs in complex, real-world systems, with coverage-guided greybox fuzzing being a key contributor to this success. Existing research has largely focused on developing new heuristics to increase code coverage, and current benchmarks measure coverage increase or the number of bugs found. However, there is a notable lack of investigation into programming constructs that systematically hinder or prevent fuzzing heuristics from achieving coverage, commonly referred to as “obstacles” or “roadblocks”.

This work makes two key contributions. First, we introduce TEPHRA, a principled methodology that uses semantics-guided synthesis to generate bug-free programs with diverse obstacles and evaluate a fuzzer’s ability to overcome them. Second, we use TEPHRA to generate obstacles and empirically evaluate 31 contemporary fuzzing systems, consuming 37.4 CPU years. Our analysis reveals limitations in current fuzzing heuristics and uncovers bugs in the fuzzers themselves, including AFL++. All evaluated fuzzers struggle with certain obstacles, such as floating- point conditionals and character strings. We also find that signed integers are more challenging than unsigned, and some heuristics are overtuned for 32- and 64-bit types, neglecting 8- and 16- bit integers. Overall, we observe a single difficult construct can significantly degrade a fuzzer’s performance.


## 34. Terminator: enabling efficient fuzzing of closed-source GUI programs by automatic coverage-guided termination

**Authors:** Jonas Zabel (Fraunhofer SIT | ATHENE), Philip Kolvenbach, Steven Arzt (Fraunhofer SIT; ATHENE)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334615

**中文总结:** 提出 Terminator，面向闭源 GUI 文件处理程序自动进行 coverage-guided 终止判定，无需源码或手工 harness 即可高效 fuzz；通过分析 CPU 使用等运行时信号确定输入处理完成时机并强制结束进程。

**Abstract:** When fuzzing a proprietary file-processing program, one typically executes the whole program repeatedly with sampled input files, and distinguishes between normal and abnormal termination. While this works well for many command-line utilities, it is more complicated for programs that usually do not terminate after input file processing. Many real-world applications are examples of such programs, in particular, those with a graphical user interface (GUI), such as image editors, media players and document viewers. In these cases, the fuzzer has to define the scope of the execution and forcefully terminate the program under test.

In order to efficiently fuzz test file-processing programs with a GUI, a standard approach is to define a dedicated testing harness, which executes the file processing in isolation and strips irrelevant program parts. However, this either requires the source code of the program or an expert’s effort in reverse engineering. Alternative approaches work on the unmodified binary of the program, and use a heuristic to decide when the input processing is likely done. For example, one can terminate the program after a fixed timeout or once its CPU usage has dropped below a threshold. We show that these heuristics, while simple to implement, are inefficient and ineffective.

We present Terminator, a fully-automated approach to facilitate efficient fuzzing of closed-source file-processing programs with a GUI. Terminator modifies the binary of the program under test so that it automatically terminates when code coverage stops increasing without user interaction. Consequently, Terminator (1) ensures that the program terminates soon after the input processing instead of waiting for user interaction, and, at the same time, (2) prevents premature termination during input processing. We show that Terminator outperforms the timeout and CPU usage heuristics and significantly increases fuzzing efficiency.


## 35. Unit Test Update through LLM-Driven Context Collection and Error-Type-Aware Refinement

**Authors:** Yuanhe Zhang (Zhejiang University), Zhiquan Yang (Zhejiang University), Shengyi Pan (Zhejiang University), Zhongxin Liu (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334559

**中文总结:** 提出 TestUpdater，用 LLM 驱动上下文收集与按错误类型精炼，在代码变更后即时自动修复并增强单元测试；模拟开发者推理流程，较规则式方法能更好处理复杂变更并提升生成测试正确性。

**Abstract:** Unit testing is critical for ensuring software quality and software system stability. The current practice of manually maintaining unit tests suffers from low efficiency and the risk of delayed or overlooked fixes. Therefore, an automated approach is required to instantly update unit tests, with the capability to both repair and enhance unit tests. However, existing automated test maintenance methods primarily focus on repairing broken tests, neglecting the scenario of enhancing existing tests to verify new functionality. Meanwhile, due to their reliance on rule-based context collection and the lack of verification mechanisms, existing approaches struggle to handle complex code changes and often produce test cases with low correctness. To address these challenges, we propose TestUpdater, a novel Large Language Model (LLM) based approach that enables automated just-in-time test updates in response to production code changes. By emulating the reasoning process of developers, TestUpdater first leverages the LLM to analyze code changes and identify relevant context, which it then extracts and filters. This LLM-driven context collector can flexibly gather accurate and sufficient context, enabling better handling of complex code changes. Then, through carefully designed prompts, TestUpdater guides the LLM step by step to handle various types of code changes and introduce new dependencies, enabling both the repair of broken tests and the enhancement of tests. Finally, emulating the debugging process, we introduce an error-type-aware iterative refinement mechanism that executes the LLM-updated tests and repairs failures, which significantly improves the overall correctness of test updates. Since existing test repair datasets lack scenarios of test enhancement, we further construct a new benchmark, Updates4J, with 195 real-world samples from 7 projects, enabling execution-based evaluation of test updates. Experimental results show that TestUpdater achieves a compilation pass rate of 94.4% and a test pass rate of 84.6%, outperforming the state-of-the-art method Synter by 15.4% and 16.9%, respectively. Furthermore, TestUpdater exhibits 12.5% higher branch coverage and 14.1% greater line coverage than Synter.


## 36. Using Active Learning to Train Predictive Mutation Testing with Minimal Data

**Authors:** Miklos Borsi (Karlsruhe Institute of Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334622

**中文总结:** 提出 AL-PMT，以主动学习训练预测性 mutation testing 模型，大幅削减所需标注 mutant 执行结果；在 80% 以上项目中仅观察 10% mutant kill 状态即可达到最优性能 98%。

**Abstract:** Mutation testing is a powerful method of evaluating test suite adequacy. Despite growing industry attention, wide-scale application is frequently limited by the high runtime cost of mutation testing. A set of predictive models have been proposed to mitigate this cost issue, intending to replace the actual execution of a mutated program’s test suite with a predicted result of the tests’ outcome. These predictive models ingest static code features, dynamic execution features, or code and documentation text to produce the predictions. Feature-based models can require a large amount of training data and mutants executed by test cases to become operational. We propose active learning-based predictive mutation testing (AL-PMT) as a way to dramatically reduce the amount of training data needed for a performant model. We conduct experiments to compare AL-PMT’s performance with a non-active learning model and find that AL-PMT quickly converges to improved or on-par performance compared to the baseline of the foundational PMT. AL-PMT achieves 98% of its best possible performance in over 80% of examined projects, while observing only 10% of each project’s mutant set kill status. In addition to training in a fraction of the data required for previous models, AL-PMT is organized in a way that is more amenable to a potential industry application scenario. Besides not requiring the building, running and full mutation testing of several other projects or versions for training data, AL-PMT is able to identify challenging mutants and select them for execution. As such, we expand on the coverage metric provided by basic predictive mutation testing with the ability to guide the targeted execution of important mutants and guiding attention of developers to remaining survived ones. This addresses the rarely mentioned cost of human developer time on fixing the findings of mutation testing, rather than just the computational time spent producing the mutants.


## 37. Using Fourier Analysis and Mutant Clustering to Accelerate DNN Mutation Testing

**Authors:** Ali Ghanbari (Auburn University), Sasan Tavakkol (Google Research)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334573

**中文总结:** 提出 DM#，利用 Fourier 分析量化 DNN mutant 行为并聚类，仅测试各簇代表 mutant 以复用 kill/survive 结论；在 14 个不同规模模型上平均加速 mutation testing 28.38%。

**Abstract:** Deep neural network (DNN) mutation analysis is a promising approach to evaluating test set adequacy. Due to the large number of generated mutants that must be tested on large datasets, mutation analysis is costly. In this paper, we present a technique, named DM#, for accelerating DNN mutation testing using Fourier analysis. The key insight is that DNN outputs are real-valued functions suitable for Fourier analysis that can be leveraged to quantify mutant behavior using only a few data points. DM# uses the quantified mutant behavior to cluster the mutants so that the ones with similar behavior fall into the same group. A representative from each group is then selected for testing, and the result of the test, e.g., whether the mutant is killed or survived, is reused for all other mutants represented by the selected mutant, obviating the need for testing other mutants. 14 DNN models of sizes ranging from thousands to millions of parameters, trained on different datasets, are used to evaluate DM# and compare it to several baseline techniques. Our results provide empirical evidence on the effectiveness of DM# in accelerating mutation testing by 28.38%, on average, at the average cost of only 0.72% error in mutation score. Moreover, on average, DM# incurs 11.78, 15.16, and 114.36 times less mutation score error compared to random mutant selection, boundary sample selection, and random sample selection techniques, respectively, while generally offering comparable speed-up.


## 38. WEST: Specification-Based Test Generation for WebAssembly

**Authors:** Dongjun Youn (KAIST), Shin Wonho (KAIST), Sukyoung Ryu (KAIST)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334667

**中文总结:** 提出 WEST，从 SpecTec 机械化 Wasm 规范自动生成符合语法/验证规则并覆盖执行语义的测试程序；可灵活适配完整或子集规范并集成多种测试生成策略，减轻运行时一致性测试的手工负担。

**Abstract:** WebAssembly (Wasm) is a low-level binary instruction format designed for safe and high-performance execution across diverse computing environments and runtimes. As Wasm evolves with new features and proposals, testing the correctness and conformance of Wasm runtimes has become increasingly complex. Manually constructing test suites is labor-intensive and difficult to scale, especially as the specification grows in complexity. While fuzzing-based approaches offer partial automation, they often lack a principled connection to the formal specification, and adapting to evolving or restricted subsets of the specification typically requires manual intervention.

In this paper, we present WEST, a specification-based test generation framework that automatically produces Wasm test cases from mechanized specifications written in SpecTec, a Wasm-specific specification language. Given any full or subset variant of the Wasm specification as input, WEST aims to systematically generate test programs that conform to the input grammar and validation rules, and capture the runtime behavior defined by its execution semantics. The framework allows flexible integration of different test generation strategies. For instance, we demonstrate both top-down and bottom-up approaches for generating Wasm modules, but the architecture is compatible with other generation techniques as well. The framework enables the creation of customized test cases for engines that support only subsets of the Wasm specification. We evaluate WEST across multiple specification variants and engine configurations, demonstrating that it produces valid and diverse test cases. As a result, it reveals 18 bugs across five Wasm engine implementations, 10 of which are confirmed and fixed. We believe that this work provides a solid foundation for future specification-driven test generation and fuzzing.


## 39. WingMuzz: Blackbox Testing of IoT Protocols via Two-dimensional Fuzzing Schedule

**Authors:** Xiaogang Zhu (Adelaide University), Enze Dai (Swinburne University of Technology), Xiaotao Feng (360 Vulnerability Research Institute), Shaohua Wang (Central University of Finance and Economics), Xin Xia (Zhejiang University), Sheng Wen (Swinburne University of Technology), Kwok-Yan Lam (Nanyang Technological University, Singapore), Yang Xiang (Digital Research & Innovation Capability Platform, Swinburne University of Technology)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://ieeexplore.ieee.org/document/11334343

**中文总结:** 提出 WINGMUZZ，利用与 IoT 协议同规的开源实现的 greybox 覆盖率反馈指导闭源 IoT 协议黑盒 fuzz，采用二维调度（wingmate 选择与开源侧覆盖引导）；提升无源码 IoT 协议 fuzz 的有效反馈与探索效率。

**Abstract:** The Internet of Things (IoT) is widely used in various sectors but is often prone to vulnerabilities. With the proprietary nature of IoT devices, their source code and firmware are frequently unavailable for open review, rendering blackbox fuzzing a viable approach. However, the effectiveness of blackbox fuzzing is often challenging due to the lack of feedback, especially the information of code coverage. In this paper, we propose WINGMUZZ to provide blackbox fuzzing of IoT protocols with effective feedback. The key is to guide blackbox fuzzing by utilizing runtime information from greybox fuzzing on counterpart open-source code. This is based on our observation that IoT protocols and open-source code conform to the same specifications, indicating that inputs exploring different code regions on open-source code may also discover new coverage on IoT protocols. WINGMUZZ uses a two-dimensional fuzzing schedule to optimize the process of fuzzing IoT protocols. The first dimension involves scheduling open-source implementations, referred to as wingmates, so that similar ones are preferred to guide blackbox fuzzing. The second dimension utilizes coverage-guided greybox fuzzing to test open-source code. This solution can bridge the performance gap between blackbox fuzzing and greybox fuzzing on IoT protocols. We evaluate the performance of WINGMUZZ across eight IoT protocols and compare it with six widely-used blackbox fuzzers. On average, WINGMUZZ can discover 42.1%, 26.92%, 25.01%, 34.95%, 23.56% and 11.63% more edges than Boofuzz, Spike, Peach, SNIPUZZ, Pulsar and ChatAFL, respectively. Additionally, WINGMUZZ exposes 10 bugs in IoT protocols while other fuzzers expose no more than 3 bugs. It also exposes 2 new protocol vulnerabilities in IoT devices while other fuzzers cannot identify any.


## 40. ZendDiff: Differential Testing of PHP Interpreter

**Authors:** Yuancheng Jiang (National University of Singapore), Jianing Wang (National University of Singapore), Qiange Liu (Beihang University), Yeqi Fu (National University of Singapore), Jian Mao (Beihang University), Roland H. C. Yap (National University of Singapore), Zhenkai Liang (National University of Singapore)

**Categories:** Testing and Fuzzing

**PDF:** https://ieeexplore.ieee.org/document/11334388

**中文总结:** 提出 ZendDiff，利用 PHP JIT 与非 JIT 双执行路径做差分测试，结合程序状态探测、JIT 感知变异与双重验证检测解释器逻辑 bug；覆盖率与 opcode 执行量优于官方 CI 测试套件并能发现静默错误。

**Abstract:** The PHP interpreter, powering over 70% of websites on the internet, plays a crucial role in web development. Existing approaches to finding bugs in PHP primarily focus on detecting explicit security issues through crashes or sanitizer-based oracles, but fail to identify logic bugs that silently lead to incorrect results. We observe that the introduction of Just-In-Time (JIT) compila- tion mode in PHP presents an opportunity for differential testing, as it provides an alternative implementation of the same language specification. To shed light on this, we propose ZendDiff, an automatic differential testing framework that efficiently detects logic bugs in the PHP interpreter by comparing JIT and non- JIT execution results. Our differential testing incorporates three key techniques: program state probing for fine-grained execution state comparison, JIT-aware program mutation for sufficiently exercising JIT functionality, and dual verification to handle non- deterministic behaviors in PHP programs. Our experimental results demonstrate that ZendDiff outperforms the official test suite used in PHP’s continuous integration, achieving higher code coverage and executing more Zend opcodes. Through ablation studies, we validate the effectiveness of these techniques. To date, ZendDiff has identified 51 previously unknown logic bugs in the PHP interpreter, with 37 already fixed and 3 confirmed by PHP developers. ZendDiff has been acknowledged by the PHP developers, and offers a practical tool for automatically discovering logic bugs in the PHP interpreter.

