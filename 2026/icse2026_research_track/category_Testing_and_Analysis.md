# ICSE 2026 Research Track — Testing and Analysis

Source: https://conf.researchr.org/track/icse-2026/icse-2026-research-track?#event-overview

Total in this category: 72 papers

## 1. An Empirical Study on Static Application Security Testing (SAST) Tools for Python

**Authors:** Liu Zhuohang (Nankai University), Zhi Wang (Nankai University), Haotong Liu (Nankai University), Wanpeng Li (University of Liverpool)

**Categories:** Testing and Analysis

**Awards:** Distinguished Paper Award

**中文总结:** 评估 8 款 Python SAST 工具在合成与真实漏洞数据集上的表现；单工具在真实集最多检出 40%，全部工具聚合仅 66.7%，并给出根因分析与改进建议。

**Abstract:** Python is currently the most popular programming language and ensuring the security of Python applications has become a critical concern. Static Application Security Testing (SAST) tools have been introduced to address this need, claiming to support a wide range of Common Weakness Enumerations (CWEs). However, the ability of these tools to detect real-world vulnerabilities in Python programs has not been comprehensively evaluated. In this paper, we selected eight SAST tools from 117 existing ones based on well-designed criteria. Based on the synthetic and real-world dataset, we evaluated and compared these SAST tools from different perspectives including effectiveness and efficiency. Our results reveal significant limitations in current SAST tools: although perform well on the synthetic dataset, a single tool detects no more than 40% of the vulnerabilities in our real-world dataset. Even when aggregating the outputs of all evaluated tools, only 66.7% of the real-world vulnerabilities are identified. To further understand these shortcomings, we performed a root cause analysis of the detection results and identified useful insights for both SAST tool developers and users, focusing on tool development, evaluation, and selection.

## 2. AssertFlip: Reproducing Bugs via Inversion of LLM-Generated Passing Tests

**Authors:** Lara Khatib (University of Waterloo), Noble Saji Mathews (University of Waterloo, Canada), Mei Nagappan (University of Waterloo)

**Categories:** Testing and Analysis

**中文总结:** 提出 AssertFlip，先让 LLM 生成通过 buggy 行为的 passing test 再反转为 bug 复现测试（BRT）；在 SWT-Bench-Verified 上 fail-to-pass 成功率 43.6%，优于已知方法。

**Abstract:** Bug reproduction is critical in the software debugging and repair process, yet the majority of bugs in open-source and industrial settings lack executable tests to reproduce them at the time they are reported, making diagnosis and resolution more difficult and time-consuming. To address this challenge, we introduce AssertFlip, a novel technique for automatically generating Bug Reproducible Tests (BRTs) using large language models (LLMs). Unlike existing methods that attempt direct generation of failing tests, AssertFlip first generates passing tests on the buggy behaviour and then inverts these tests to fail when the bug is present. We hypothesize that LLMs are better at writing passing tests than ones that crash or fail on purpose. Our results show that AssertFlip outperforms all known techniques in the leaderboard of SWT-Bench, a benchmark curated for BRTs. Specifically, AssertFlip achieves a fail-to-pass success rate of 43.6% on the SWT-Bench-Verified subset.

## 3. Automated Network-Level Fault Injection Testing of Microservice Architectures

**Authors:** Delano Flipse (Delft University of Technology (TU Delft)), Hakan Simsek (ASML), Jérémie Decouchant (Delft University of Technology (TU Delft)), Burcu Kulahcioglu Ozkan (Delft University of Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出网络级微服务故障注入测试方法 Reynard，动态建模系统弹性行为并剪枝故障组合空间；在工业系统中发现未知弹性缺陷且开销低、易集成现有基准。

**Abstract:** Microservice architectures are inherently vulnerable to partial failures, and they rely on resilience patterns to tolerate them. However, it is challenging to design and implement the resilience logic. Unforeseen interactions with faulty services can lead to errors in dependent services, resulting in incorrect system behavior. Fault injection testing techniques aim to uncover these errors by examining the system’s behavior in response to different fault combinations. However, existing automated techniques primarily focus on service-level fault injection, which limits their broader applicability. We present an automated fault-injection testing method that operates at the network level, enabling broad applicability. The method models the system’s resilience behaviors dynamically through the observed test executions and uses this information to reduce the set of fault combinations to explore. We implemented our method in a prototype tool, called Reynard. Our evaluation demonstrates that Reynard efficiently explores system executions by significantly reducing the number of fault combinations to test. It incurs minimal overhead and can be easily integrated into existing benchmarks. Furthermore, we applied Reynard to test an industrial system, showcasing its applicability and effectiveness in a real-world context. Moreover, we uncovered a previously unknown resilience bug.

## 4. BFix: Automated Safe Memory-Leak Fixing for Binary Code

**Authors:** Wen Zhang (University of Georgia), Botang Xiao (University of Georgia), Qingchen Kong (University of Georgia), Boyang Yi (University of Georgia), Suxin Ji (University of Georgia, USA), Yage Hu (University of Georgia), Songlan Wang (University of Georgia), Wenwen Wang (University of Georgia)

**Categories:** Testing and Analysis

**中文总结:** 提出 BFix，首个二进制级内存泄漏自动修复工具，克服无源码场景的分析挑战；修复效果与效率接近源码级 SOTA，对二进制体积与性能影响可忽略。

**Abstract:** Fixing memory leaks in software is crucial to improving system efficiency, reliability, and stability. Nevertheless, manually fixing memory leaks is not only time-consuming but also error-prone. Recent research has proposed program repair techniques to fix memory leaks automatically. However, a common limitation of prior techniques is that they cannot tackle memory leaks in binary code. Given the huge popularity of binary code, it is highly necessary to fix its hidden memory leaks. To this end, this paper presents BFix, the first-ever binary-level memory-leak fixing tool. BFix creates effective binary analysis techniques to overcome the unique technical challenges of automatically and safely fixing memory leaks in binaries. Our experiments show that BFix can achieve promising fixing effectiveness and efficiency, comparable to state-of-the-art source-level fixing tools. Meanwhile, it has a negligible impact on binary code size and performance.

## 5. Boosting Gas Revenues of Ethereum Miners

**Authors:** Togzhan Barakbayeva (HKUST), Soroush Farokhnia (Hong Kong University of Science and Technology), Amir K. Goharshady (University of Oxford), Sergei Novozhilov (The Hong Kong University of Science and Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出随机化框架优化 Ethereum 矿工 gas 收入，通过采样排列 profiling、决策树学习交易 gas 依赖并编码为 ILP 求解最优区块组成；应对交易顺序影响 gas 的组合爆炸问题。

**Abstract:** In cryptocurrency networks, transaction-fee revenue serves as the primary financial incentive for miners to participate in the consensus mechanism, securing the network by validating transactions and extending the blockchain. Maximizing this revenue is therefore a key optimization problem for miners. While this has been studied for UTXO blockchains like Bitcoin, where transaction fees are fixed, we focus on Ethereum, where the challenge is significantly greater. On Ethereum, the fee paid by a transaction depends on its execution cost (gas), which can change based on the ordering of preceding transactions in a block. This creates a combinatorial explosion, as miners must select not only a subset of transactions but also their optimal permutation to maximize revenue. In this work, we present a randomized framework to address this problem. Our approach first uses randomized testing, executing sample permutations of pending transactions to profile their gas usage. From this data, we employ decision trees to learn transaction interdependencies, identifying a small “neighborhood” of transactions that influence each other’s execution costs. These dependencies are then encoded as a set of logical rules that predict gas usage based on local transaction ordering. Finally, we translate these rules and other constraints (e.g., block gas limit, nonce ordering) into an integer linear programming (ILP) instance, which we solve to find a block composition that maximizes total tip revenue. Our experimental results demonstrate significant gains: our method outperforms real-world Ethereum miners by an average of 73.45 percent per block, which corresponds to roughly 63 million USD per annum.

## 6. Bounded Exhaustive Random Program Generation for Testing Solidity Compilers

**Authors:** Haoyang Ma (Hong Kong University of Science and Technology), Alastair F. Donaldson (Imperial College London), Qingchao Shen (Tianjin University), Yongqiang Tian (Monash University), Junjie Chen (Tianjin University), Shing-Chi Cheung (Hong Kong University of Science and Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出 bounded exhaustive random program generation 与工具 Erwin，基于 bug-prone qualifier 模板约束 Solidity 编译器测试空间；发现 26 个 bug（23 未知、18 确认、10 已修复）。

**Abstract:** By July 2025, smart contracts have collectively overseen assets about $120 billion. Since Solidity is the leading language for developing smart contracts, ensuring the correctness of Solidity compilers is critically important. However, Solidity compilers are prone to bugs, with recent studies revealing that combinations of qualifiers in Solidity programs are the primary cause of compiler crashes, accounting for 40.48% of all historical crashes. While random program generators are widely used for compiler testing, they are less effective at finding Solidity compiler bugs because they explore the unbounded space of possible programs rather than concentrating on the specific subspace related to bug-prone qualifiers. A promising idea for finding qualifier-related bugs is to bound the search space based on empirical evidence of where such bugs are likely to occur, specifically focusing test generation to target subspaces with rich combinations of qualifiers. To address this, we propose bounded exhaustive random program generation, a novel approach that dynamically bounds the search space, enhancing the likelihood of uncovering Solidity compiler bugs. Specifically, our method bounds the search space by generating valid program templates that abstract those programs using bug-prone qualifiers and then applies these templates to guide program generation for compiler testing. Mechanisms are devised to address the technical challenges regarding validity and efficiency. We have implemented our novel generation approach in a new tool, Erwin. We have used Erwin to find and report 26 bugs across two Solidity compilers, solc and solang, and one Solidity static analyzer, slither. Among these, 23 were previously unknown, 18 have been confirmed, and 10 have been fixed. Evaluation results demonstrate that Erwin outperforms state-of-the-art Solidity fuzzers in bug detection and complements developer-written test suites by covering 4,599 edges and 14,824 lines of the solc compiler that were missed by solc’s unit tests.

## 7. Breaking Single-Tester Limits: Multi-Agent LLMs for Multi-User Feature Testing

**Authors:** Sidong Feng (Monash University), Changhao Du (Jilin University), huaxiao liu (Jilin University), Qingnan Wang (Jilin University), Zhengwei Lv (ByteDance), Mengfei Wang (ByteDance), Chunyang Chen (TU Munich)

**Categories:** Testing and Analysis

**中文总结:** 提出 MAdroid 多 agent LLM 框架（Coordinator/Operator/Observer）自动化多用户交互功能测试；41 个任务中 82.9% 成功、动作相似度 96.8%，回归测试发现 11 个多用户 bug。

**Abstract:** The growing dependence on mobile phones and their apps has made multi-user interactive features—like chat calls, live streaming, and video conferencing—indispensable for bridging the gaps in social connectivity caused by physical and situational barriers. However, automating these interactive features for testing is fraught with challenges, owing to their inherent need for timely, dynamic, and collaborative user interactions, which current automated testing methods inadequately address. Inspired by the concept of agents designed to autonomously and collaboratively tackle problems, we propose MAdroid, a novel multi-agent approach powered by the Large Language Models (LLMs) to automate the multi-user interactive task for app feature testing. Specifically, MAdroid employs two functional types of multi-agents: user agents (Operator) and supervisor agents (Coordinator and Observer). Each agent takes a specific role: the Coordinator directs the interactive task; the Operator mimics user interactions on the device; and the Observer monitors and reviews the task automation process. Our evaluation, which included 41 multi-user interactive tasks, demonstrates the effectiveness of our approach, achieving 82.9% of the tasks with 96.8% action similarity, outperforming the ablation studies and state-of-the-art baselines. Additionally, a preliminary investigation underscores MAdroid’s practicality by helping identify 11 multi-user interactive bugs during regression app testing, confirming its potential value in real-world software development contexts.

## 8. Characterizing Regression Bug‑Inducing Changes and Improving LLM‑Based Regression Bug Detection

**Authors:** Xuezhi Song (Fudan University), Yijian Wu (Fudan University), Bihuan Chen (Fudan University), Zhengjie Lu (Fudan University), Shuning Liu (Fudan University), Xin Peng (Fudan University)

**Categories:** Testing and Analysis

**中文总结:** 分析 280 个 Java 回归 bug 的引入变更与根因（内在错误 vs 兼容性错误），验证 LLM 检测能力有限并构建 LLM4Reg 显著提升精度、召回与解释能力。

**Abstract:** Regression bugs are common in real-world software projects. Although several studies have characterized various aspects of these bugs, a detailed analysis of the characteristics of code changes that introduce regression bugs is still lacking. It is also not clear whether and how regression bugs can be identified, in the era of wide usage of large language models (LLMs), in code commits during software development in the first place. To fill this gap, our study systematically analyzes 280 regression bugs from open-source Java projects, examining both the root causes and the associated development activities of regression bug-inducing changes, while also evaluating the effectiveness of LLMs in detection such commits and explaining their underlying causes. Our findings indicate that regression bugs are usually triggered by a single atomic development activity, with feature changes or additions, and bug fixes appearing more frequently in regression bug-inducing commits. Additionally, performance improvements and refactoring are often responsible for the introduction of bugs. We develop a taxonomy that categorizes the root causes of regression bugs into two types: intrinsic errors, such as logic errors and unchecked null references, and compatibility errors, where otherwise correct changes inadvertently violate assumptions or dependencies in other parts of the system. Furthermore, we verify that LLMs have limited ability to detect regression bugs. Based on our findings, we construct LLM4Reg that substantially improves the precision, recall, and explanation capabilities of LLM-based regression bug detection.

## 9. CombCT: Compiler Testing via Combinatorial Testing

**Authors:** Chuan Luo (Beihang University), Shaoke Cui (Beihang University), Jiahao Yan (Beihang University), Junjie Chen (Tianjin University), Chenyao Suo (Tianjin University), Wei Wu (Central South University; Xiangjiang Laboratory), Chanjuan Liu (Dalian University of Technology), Chunming Hu (Beihang University)

**Categories:** Testing and Analysis

**中文总结:** 提出 CombCT，首次将组合测试用于探索编译器优化序列以发现缺陷；在 GCC/LLVM 上检出更多序列相关 bug，并发现14个此前未知缺陷（13个已确认或修复）。

**Abstract:** Compilers, as fundamental software, are essential for various applications, making their reliability crucial. Modern compilers like GCC and LLVM offer numerous optimizations to improve performance. Empirical studies present that most bugs occur during compiler optimization, especially with specific optimization sequences, yet little attention has been paid to this in compiler testing. The vast optimization sequence space challenges existing methods, leaving this important research direction in its early stages and in need of effective solutions. In this work, we propose a novel and effective compiler testing approach dubbed CombCT, aimed at boosting compiler testing. CombCT is the first approach that leverages the power of combinatorial testing for compiler testing, making it be capable of effectively exploring optimization sequences. Besides, CombCT incorporates three new techniques, i.e., dynamic optimization sequence adaption, partial sequence selection, and diversity augmentation, to enhance its effectiveness. Extensive experiments on various versions of GCC and LLVM demonstrate that CombCT detects much more unique bugs, which are caused by certain optimization sequences, than current state-of-the-art methods, indicating its superiority. Moreover, CombCT has disclosed 14 previously unknown bugs in the latest versions of GCC and LLVM, 13 of which have been confirmed or fixed, showing its practical value.

## 10. Configuration-Sensitive Linux Kernel Fuzzing

**Authors:** Yuheng Shen, Jianzhong Liu (Tsinghua University), Yuhan Chen (Central South Sniversity), Yifei Chu (Tsinghua University), Qiang Zhang (Hunan University), Guoyu Yin (Central South University), Heyuan Shi (Central South University), Yu Jiang (Tsinghua University)

**Categories:** Testing and Analysis

**中文总结:** 提出内核模糊测试器 CSGO，联合变异运行时参数与系统调用以触达更深内核状态；平均覆盖率提升21%，发现21个未知 bug（8个已修复）。

**Abstract:** Fuzzing operating system kernels to discover deep and complex bugs is difficult to accomplish, as kernels reside between hardware and user applications, exposing a variety of input vectors that affect their internal state. Previous approaches mainly use a kernel’s system call interface to deliver test payloads into the kernel, but reaching states and triggering bugs also require collaborative efforts from other input vectors, such as runtime parameters. Kernel runtime parameters greatly affect the execution behavior of the kernel under test, as they alter internal execution flows and thus require kernel fuzzers to manipulate them in conjunction with invoking system calls to effectively root out bugs. In this paper, we present CSGO, a kernel fuzzer that discovers more in-depth bugs through fuzzing kernel runtime parameters in conjunction with system calls. CSGO’s approach is achieved through the following designs. First, CSGO generates valid test case generation syntax for kernel configurations by extracting available parameters exposed by the kernel. Then, for the extracted parameters, CSGO statically deduces relations between the configurations and kernel system calls for initial generation guidance. Finally, during fuzzing, CSGO dynamically refines the relations between the configurations and system calls by interpreting execution feedback. We implemented CSGO and evaluated its approach on recent versions of the Linux kernel. Our results show that CSGO achieves an average of 21% improvement in overall coverage compared with existing state-of-the-art kernel fuzzers and triggers 21 previously unknown bugs, with 8 fixed by kernel maintainers.

## 11. Context-Free Grammar Inference for Complex Programming Languages in Black Box Settings

**Authors:** Feifei Li (Tsinghua Shenzhen International Graduate School), Xiao Chen (University of Newcastle), xiaoyu sun (The Australian National University), Xi Xiao (Tsinghua University), Shaohua Wang (Central University of Finance and Economics), Yong Ding (School of Computer Science & lnformation Security, Guilin University of Electronic Technology, Guilin, Gusngxi, China), Sheng Wen (Swinburne University of Technology), Qingli (Peng Cheng Laboratory)

**Categories:** Testing and Analysis

**中文总结:** 提出 Crucio，通过分解森林提取短样本在黑盒场景推断 C/C++/Java 等复杂语言文法；是唯一能在合理时间内完成推断的方法，recall 与 F1 显著优于 Arvada 等 SOTA。

**Abstract:** Grammar inference for complex programming languages remains a significant challenge, as existing approaches fail to scale to real-world datasets within practical time constraints. In our experiments,none of the state-of-the-art tools, including Arvada, Treevada and Kedavra were able to infer grammars for complex languages such as C, C++, and Java within 48 hours. Arvada and Treevada perform grammar inference directly on full-length input examples, which proves inefficient for large files commonly found in such languages. While Kedavra introduces data decomposition to create shorter examples for grammar inference, its lexical analysis still relies on the original inputs. Additionally, its strict no-overgeneralization constraint limits the construction of complex grammars. To overcome these limitations, we propose Crucio, which builds a decomposition forest to extract short examples for lexical and grammar inference via a distributional matrix. Experimental results show that Crucio is the only method capable of successfully inferring grammars for complex programming languages (where the number of nonterminals is up to 17× greater than in prior benchmarks) within reasonable time limits. On the prior simple benchmark, Crucio achieves an average recall improvement of 1.37× and 1.19× over Treevada and Kedavra, respectively, and improves F1 scores by 1.21× and 1.13×.

## 12. Context-Free Property Oriented Fuzzing

**Authors:** Jiaqiang Yao (College of Computer, National University of Defense Technology), Meixi Liu (National University of Defense Technology, Changsha, China), Zhenbang Chen (College of Computer, National University of Defense Technology), Yongchao Xing (College of Computer, National University of Defense Technology), Jinjian Luo (College of Computer, National University of Defense Technology), Yunlai Luo (National University of Defense Technology), Guofeng Zhang (College of Computer, National University of Defense Technology), Yufeng Zhang (Hunan University), Ji Wang (National University of Defense Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出面向上下文无关属性的模糊测试框架 CFPOFuzz，含基于监控状态与控制流的变异算法；生成首个目标输入速度提升3.83×，发现7个零日漏洞。

**Abstract:** Fuzzing is effective for finding software bugs. However, the bugs specified in context-free properties are difficult for the existing fuzzers. These bugs are triggered when the program execution contains specific sequences of operations, e.g., push and pop operations on the stack, and locking and unlocking operations on the lock. As far as we know, existing approaches do not support fuzzing for non-regular context-free properties, which are more expressive and can be used to specify bugs in many scenarios. This paper proposes a general runtime monitoring-based fuzzing framework for the bugs expressed as context-free properties. We propose two algorithms to improve fuzzing’s effectiveness and efficiency with respect to the context-free property. The algorithm for preserving input mutants leverages the state transition information of the property’s monitors. The other algorithm for mutating the input seed combines control flow information with state transition information to prioritize the different parts of the input. We have implemented our framework CFPOFuzz for C/C++ programs. The results of the extensive experiments on real-world C/C++ programs indicate our method’s effectiveness and efficiency. Compared with coverage-oriented fuzzing, our method achieves 3.83x speedups for generating the first target input triggering the bugs. Our method found 7 unknown zero-day bugs.

## 13. CoReX: Context-Aware Refinement-Based Slicing for Debugging Regression Failures

**Authors:** Sahar Badihi (University of British Columbia, Canada), Julia Rubin (The University of British Columbia)

**Categories:** Testing and Analysis

**中文总结:** 提出面向回归失败调试的 CoReX，在双版本切片中保留理解失败所需上下文并剔除冗余计算；在相关指标上优于现有 dual-version 切片方法。

**Abstract:** Troubleshooting regression failures is one of the most frequent yet time-consuming development tasks. To help with this task, numerous approaches aim to narrow down developers’ attention to the subset of code statements relevant to the failure. The most prominent of these approaches are based on program slicing, as slicing not only identifies a subset of relevant statements but also maintains the flow of information between these statements. By surveying more than 50 practitioners from eight different countries, we observe that existing dual-version slicing-based approaches have two main limitations: (a) to minimize the number of statements presented to the developer, they omit contextual information required to truly understand the failure and (b) to keep information propagation between the statements in the slice intact, they include lengthy computations that are not necessary to understand the failure. We use these observations to define a new dual-version slicing approach for regression scenarios, called CoReX. We quantitatively evaluate CoReX on a large number of subjects and metrics used in prior work, calculating the reduction rate it achieves and its alignment with developers’ expectations. The results of our evaluation show that CoReX outperforms other existing dual-version slicing techniques on both metrics. We believe our work provides grounds for efficient integration of slicing-based approaches into development workflows.

## 14. D-BUNDLR: Destructing JavaScript Bundles for Effective Static Analysis

**Authors:** Wenyuan Xu (Aarhus University), Alexi Turcotte (CISPA), Cristian-Alexandru Staicu (CISPA Helmholtz Center for Information Security)

**Categories:** Testing and Analysis

**中文总结:** 提出 D-Bundlr，解包 JavaScript bundle 并还原库源码以恢复静态分析；使 CodeQL 在已知漏洞基准上恢复89%检出，popular 网站扫描多产出约3200条告警。

**Abstract:** Static analysis for vulnerability detection in JavaScript is an extensively studied research area. However, state-of-the-art approaches ignore bundling, an emerging development practice, akin to compilation, which allows developers to merge code from different providers, while also applying optimizations to reduce code size. A typical bundle heavily reuses single-letter identifiers and extensively relies on dynamic JavaScript features to emulate code dependencies, thus, hindering static analysis. In this work, we propose a reverse engineering approach that relies on domain-specific code transformations to unpack bundles and replace reidentified libraries with their source code. Our technique applies lightweight static analysis to dissect bundles into individual components, machine learning to identify libraries, and dynamic analysis to verify that libraries were correctly identified. We implement this approach in a tool called D-Bundlr, and evaluate it by comparing the output of CodeQL (a popular static analysis tool) before and after debundling. For a JavaScript code benchmark with known vulnerabilities, our approach allows CodeQL to recover 89% of the vulnerabilities and 83% of all alerts that were also detected in the source code, but were dormant in bundles. Similarly, for real-world bundles where we can retrieve the source code, D-Bundlr recovered 33% of the original alerts. When applied to bundles extracted from the 100,000 most popular websites, D-Bundlr identifies 34,445 instances corresponding to 63 unique libraries, and causes CodeQL to produce around 3.2K more security alerts than on packed bundles. We additionally illustrate how attackers can exploit some of our zero-day findings, causing unwanted security effects such as advertisement space hijacking.

## 15. Debugging Performance Issues in WebAssembly Runtimes via Mutation-based Inference

**Authors:** Ruiying Zeng (Fudan University), Shuyao Jiang (The Chinese University of Hong Kong), Wenxuan Zhao (Fudan University), Yangfan Zhou (Fudan University)

**Categories:** Testing and Analysis

**中文总结:** 提出变异推断工具 WarpL，对比原程序与性能正常 mutant 的机器码定位 Wasm 运行时次优编译指令；12个真实问题中10个定位到精确根因，并诊断 Wasmtime 6个未知问题。

**Abstract:** Performance debugging in WebAssembly (Wasm) runtimes is essential for ensuring the robustness of Wasm, especially since performance issues have frequently occurred in Wasm runtimes, which can significantly degrade the capabilities of hosted services. Many performance issues in Wasm runtimes result from suboptimal compilation of input Wasm programs, for which existing performance debugging methods primarily designed for application-level inefficiencies are not well-suited. In this paper, we present WarpL, a novel mutation-based approach that aims to identify the exact suboptimal instruction sequences responsible for the performance issues in Wasm runtimes, thereby narrowing down the root causes. Specifically, WarpL obtains a functionally similar mutant in which the performance issue does not manifest, and isolates the exact suboptimal instructions by comparing the machine code of the original and mutated programs. We implement WarpL as an open-source tool and evaluate it on 12 real-world performance issues across three widely used Wasm runtimes. WarpL identified the exact causes in 10 out of 12 issues. Notably, we have used WarpL to successfully diagnose six previously unknown performance issues in Wasmtime.

## 16. DeFT: Maintaining Determinism and Extracting Unit Tests for Autonomous Driving Planning

**Authors:** Yuqi Huai (University of California, Irvine), Yuntianyi Chen (University of California, Irvine), Ziwen Wan (University of California, Irvine), Alfred Chen (University of California, Irvine), Joshua Garcia (University of California, Irvine)

**Categories:** Testing and Analysis

**中文总结:** 提出 DeFT，从非确定性 ADS 场景测试中提取规划模块确定性单元测试；可复现658次碰撞失败，失败复现时间减少43.69%–77.64%。

**Abstract:** An Autonomous Driving System (ADS) is a complex software system often composed of multiple modules, each responsible for its own set of tasks. The ADS planning module is responsible for planning the future driving trajectories (i.e., making decisions on how to drive) of the autonomous vehicle and is historically the most buggy ADS module. In recent years, many approaches have been proposed to test an ADS in complex virtual scenarios through simulation, and these scenarios have been effective in revealing ADS’ suboptimal decisions. However, due to the randomness of events that occur during the real-time execution of an ADS, test scenarios tend to produce varying outcomes and, in turn, make ADS testing non-deterministic, flaky, and unpredictable. To address this challenge, we propose and evaluate DeFT, an approach that extracts deterministic test cases for the ADS planning module from non-deterministic system-level scenario tests. DeFT monitors the messages being exchanged by ADS modules during executions of system-level scenario tests and reconstructs inputs to reproduce the executions of the planning module. By using DeFT, we find planning module tests can (1) more accurately reproduce planning module executions that occurred during system-level scenario tests, (2) be used to deterministically detect the same 658 collision failures revealed by system-level scenario tests, and (3) reduced time needed to reproduce failure by 43.69% to 77.64%.

## 17. Dependency-aware Residual Risk Analysis

**Authors:** Seongmin Lee (UCLA), Marcel Böhme (MPI for Security and Privacy)

**Categories:** Testing and Analysis

**中文总结:** 提出考虑覆盖元素依赖关系的 discovery probability 估计器以更准确评估测试残余风险；median absolute error 约为 Good-Turing 估计器的1/5，可避免约7×无效测试时间。

**Abstract:** However much we test a software system, some \emph{residual risk} of undiscovered bugs always remains. If we model test generation as a sampling process, a residual risk can be defined as the probability that the next test input reveals a bug. This risk is upper-bounded by the \emph{discovery probability (DP)}, i.e., the probability that the next test input covers new code, which itself is upper-bounded by the \emph{coverage rate}, i.e., the expected number of new coverage elements per test input. Prior work introduced the \emph{Good-Turing estimator (GoTu)} to estimate residual risk via coverage rate. However, we find that GoTu substantially overestimates, leading to undue optimism in bug finding because (i) the coverage rate is only a loose upper bound, and (ii) it ignores \emph{dependencies} among coverage elements. We propose \emph{dependency-aware DP estimation} for residual risk analysis. Our estimator directly estimates DP \emph{and} accounting for coverage dependencies using Ma and Chao’s sample coverage estimation. A naive implementation requires space proportional to the number of coverage elements and executions, which can be prohibitively large. To make it practical, we introduce two optimizations: dependency-aware node removal, which reduces the number of coverage elements to observe, and online singleton cluster maintenance, which eliminates the need to record observed coverage elements in each execution. A comparison of our estimator and GoTu on real-world software from FuzzBench demonstrates a substantial reduction in estimation error. If we stopped the campaign when the estimate of residual risk falls below a certain threshold, GoTu would lead a tester to waste $7\times$ more time than our estimator before deciding to stop. Our estimator achieves a median absolute error of only one-fifth that of GoTu. Finally, our bug-based analysis shows that our estimator achieves one to two orders of magnitude lower error than GoTu in residual risk estimation.

## 18. DyMA-Fuzz: Dynamic Direct Memory Access Abstraction for Re-hosted Monolithic Firmware Fuzzing

**Authors:** Guy Farrelly (The University of Adelaide, Adelaide), Michael Chesser (University of Adelaide), Seyit Camtepe (CSIRO Data61), Damith C. Ranasinghe (University of Adelaide)

**Categories:** Testing and Analysis

**中文总结:** 提出 DyMA-Fuzz，在重宿主固件 fuzzing 中抽象 DMA 接口并自动注入 fuzz 数据；覆盖率最高提升122%，发现 SOTA 遗漏漏洞。

**Abstract:** The rise of smart devices in critical domains—including automotive, medical, industrial—demands robust firmware testing. Fuzzing firmware in re-hosted environments is a promising method for automated testing at scale, but remains difficult due to the tight coupling of code with a microcontroller’s peripherals. Existing fuzzing frameworks primarily address input challenges in providing inputs for Memory-Mapped I/O or interrupts, but largely overlook Direct Memory Access (DMA), a key high-throughput interface used that bypasses the CPU. We introduce DyMA-Fuzz to extend recent advances in stream-based fuzz input injection to DMA-driven interfaces in re-hosted environments. It tackles key challenges—vendor-specific descriptors, heterogeneous DMA designs, and varying descriptor locations—using runtime analysis techniques to infer DMA memory access patterns and automatically inject fuzzing data into target buffers, without manual configuration or datasheets. Evaluated on 94 firmware samples and 8 DMA-guarded CVE benchmarks, DyMA-Fuzz reveals vulnerabilities and execution paths missed by state-of-the-art tools and achieves up to 122% higher code coverage. These results highlight DyMA-Fuzz as a practical and effective advancement in automated firmware testing and a scalable solution for fuzzing complex embedded systems.

## 19. E-Test: E'er-Improving Test Suites

**Authors:** Ketai Qiu (USI Università della Svizzera Italiana), Luca Di Grazia (University of St. Gallen), Leonardo Mariani (University of Milano-Bicocca), Mauro Pezze (Università della Svizzera italiana (USI) and Università degli Studi di Milano Bicocca)

**Categories:** Testing and Analysis

**中文总结:** 提出 E-Test，从生产监控执行中识别未测场景并用 LLM 增广测试套件；F1 达0.55，显著优于回归/现场测试（0.34）与 vanilla LLM（0.39）。

**Abstract:** Test suites are inherently imperfect, and testers can always enrich a suite with new test cases that improve its quality and, consequently, the reliability of the target software system. However, finding test cases that explore execution scenarios beyond the scope of an existing suite can be extremely challenging and labor-intensive, particularly when managing large test suites over extended periods. In this paper, we propose E-Test, an approach that reduces the gap between the execution space explored with a test suite and the executions experienced after testing by augmenting the test suite with test cases that explore execution scenarios that emerge in production. E-Test (i) identifies executions that have not yet been tested from large sets of scenarios, such as those monitored during intensive production usage, and (ii) generates new test cases that enhance the test suite. E-Test leverages Large Language Models (LLMs) to pinpoint scenarios that the current test suite does not adequately cover, and augments the suite with test cases that execute these scenarios. Our evaluation on a dataset of 1,975 scenarios, collected from highly-starred open-source Java projects already in production and Defects4J, demonstrates that E-Test retrieves not-yet-tested execution scenarios significantly better than state-of-the-art approaches. While existing regression testing and field testing approaches for this task achieve a maximum F1-score of 0.34, and vanilla LLMs achieve a maximum F1-score of 0.39, E-Test reaches 0.55. These results highlight the impact of E-Test in enhancing test suites by effectively targeting not-yet-tested execution scenarios and reducing manual effort required for maintaining test suites.

## 20. EchoFuzz: Empowering Smart Contract Fuzzing with Large Language Models

**Authors:** Juanen Li (Tsinghua University), Peng Qian (Zhejiang University), Guanyan Li (University of Oxford), Rui Wang (Beijing Normal University), Peixin Wang (East China Normal University), Zhiqing Tang (Beijing Normal University), Fuchen Ma (Tsinghua University), Yuanliang Chen (Tsinghua University), Lun Zhang (GoPlus Security)

**Categories:** Testing and Analysis

**中文总结:** 提出 LLM 引导智能合约 fuzzing EchoFuzz，生成漏洞函数调用序列 VFCS 并迭代引导探索；分支覆盖率提升29%、多发现62%漏洞，并发现37个未知漏洞。

**Abstract:** Smart contracts, serving as the cornerstone of decentralized applications on blockchain platforms, autonomously manage trillion-dollar digital assets across diverse domains, making them prime targets for malicious exploits. Fuzzing has emerged as a promising technique for detecting vulnerabilities in smart contracts, yet existing methods face two main challenges. (1) The logical gap in state transitions and combinatorial redundancy hinders effective tradeoffs between bug detection efficiency and state space exploration cost, leading to critical execution paths to be overlooked. (2) Rule-based sequence mutation strategies suffer from path redundancy and inadequate guidance from contract logic, resulting in performance bottlenecks that stall the exploration of in-depth vulnerability-oriented paths. To tackle these challenges, we propose EchoFuzz, an LLM-guided fuzzing framework that introduces Vulnerable Function Call Sequences (VFCS) - minimal, behavior-preserving execution paths that expose bugs through essential state transitions. EchoFuzz consists of two key procedures. First, we develop a chain-guided LLM approach that mimics the workflow of expert auditors, combining static analysis with logical understanding to generate contract-specific VFCS candidates that eliminate combinatorial redundancy. Second, we adopt an iterative fuzzing strategy that employs LLMs to adaptively promote exploration, taking advantage of the real-time feedback to steer the fuzzer towards unexplored branches. Experimental results show that EchoFuzz significantly outperforms the state-of-the-art methods, achieving 29% improvement in branch coverage and discovering 62% more vulnerabilities than the top competitors. In addition, EchoFuzz has discovered 37 previously unknown vulnerabilities in real-world smart contract projects, underscoring its robust performance and practicality.

## 21. Efficient Build Dependency Verification Using eBPF and Incremental Analysis

**Authors:** Yuta Saito (Waseda University), Kazunori Sakamoto (Tokyo Online Unicersity / Waseda University / National Institute of Informatics / WillBooster Inc.), Hironori Washizaki (Waseda University)

**Categories:** Testing and Analysis

**中文总结:** 提出 mkcheck2，结合 eBPF 系统调用追踪与增量分析验证构建依赖；开销较 ptrace 方案最高降99.7%，每 commit 平均分析时间从1267s 降至24s。

**Abstract:** Build systems are fundamental to modern software development, but maintaining correct dependency specifications remains a significant challenge. Dependency-related errors, including missing and redundant dependencies, account for over 50% of build errors in large-scale software projects. Existing tools for detecting such errors suffer from two major limitations: high runtime overhead due to ptrace-based system call tracing, and the need to verify all edges in the build dependency graph. This paper presents mkcheck2, a novel approach that combines extended Berkeley Packet Filter (eBPF)-based system call tracing with incremental analysis to enable efficient dependency verification. Our evaluation on a diverse set of open-source projects demonstrates that mkcheck2 reduces the overhead of dependency error detection by up to 99.7% compared to existing ptrace-based approaches while maintaining detection accuracy. Across the entire 300-project Make corpus, the incremental analysis technique lowers the mean analysis time per commit from 1267.49 seconds to just 23.56 seconds, making continuous dependency verification practical in real-world development environments.

## 22. Efficient Strong Updates For Path Sensitive Data Dependence Analysis

**Authors:** Yiyuan Guo (The Hong Kong University of Science and Technology, Ant Group), Charles Zhang (Hong Kong University of Science and Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出分阶段 must-kill 推断与树状数据结构，加速路径敏感数据依赖分析中的 strong update；显著提速并扩大可分析状态覆盖。

**Abstract:** Path-sensitive data dependence analysis is a powerful technique widely used in static vulnerability detection. One of the central challenges is how to resolve indirect data dependencies induced by pointer operations: the value loaded from a memory location may depend on different values stored before. Resolving indirect data dependencies in a path-sensitive manner significantly improves the analysis precision, but also induces high overhead that limits its scalability. We observe that much of the computation effort in path-sensitive data dependence analysis is spent on performing strong updates during load-store matching: a stored value propagates to a load statement only if it is not overwritten by other values stored to the same memory location during the propagation. Answering this question path-sensitively is extremely challenging and often leads to a state explosion that precludes efficient static analysis. To improve the efficiency for performing strong updates in path-sensitive data dependence analysis, our key insight is that the relation among multiple store statements could be determined in stages: most of the easy cases are handled efficiently by inferring a must-kill relation among the heap store statements, reserving the computationally expensive path-sensitive analysis for the rest. We design a tree-like data structure to encode both the control flow and alias information, which incrementally updates the relation during the analysis. Experiments have shown significant speed-ups and improved state coverage in static analysis through the algorithmic improvements of path-sensitive strong updates.

## 23. Enhancing Symbolic Execution with Self-Configuring Parameters

**Authors:** Minjong Kim (Sungkyunkwan University), Sooyoung Cha (Sungkyunkwan University)

**Categories:** Testing and Analysis

**中文总结:** 提出 ParaSuit 为每个程序自配置符号执行参数；在12个 C 程序上分支覆盖率平均高26%，独有发现4个 bug。

**Abstract:** We present ParaSuit, a self-configuring technique that enhances symbolic execution by autonomously adjusting its parameters tailored to each program under test. Modern symbolic execution tools are typically equipped with various external parameters to effectively test real-world programs. However, the need for users to fine-tune a multitude of parameters for optimal testing outcomes makes these tools harder to use and limits their potential benefits. Despite recent efforts to improve this tuning process, existing techniques are not self-configuring; they cannot dynamically identify which parameters to tune for each target program, and for each manually selected parameter, they sample a value from a fixed, user-defined set of candidate values that is specific to that parameter and remains unchanged across programs. The goal of this paper is to automatically configure symbolic execution parameters from scratch for each program. To this end, ParaSuit begins by automatically identifying all available parameters in the symbolic execution tool and evaluating each parameter’s impact through interactions with the tool. It then applies a specialized algorithm to iteratively select promising parameters, construct sampling spaces for each, and update their sampling probabilities based on data accumulated from symbolic execution runs using sampled parameter values. We implemented ParaSuit on KLEE and assessed it across 12 open-source C programs. The results demonstrate that ParaSuit significantly outperforms the state-of-the-art method without self-configuring parameters, achieving an average of 26% higher branch coverage. Remarkably, ParaSuit identified 11 unique bugs, four of which were exclusively discovered by ParaSuit.

## 24. Fine-Grained Analyses for Evolution-Aware Runtime Verification

**Authors:** Pengyue Jiang (Cornell University), Kevin Guan (Cornell University), M. Mahdi Khosravi (Middle East Technical University), Moustafa Ismail (Middle East Technical University), Marcelo d'Amorim (North Carolina State University), Owolabi Legunsen (Cornell University)

**Categories:** Testing and Analysis

**中文总结:** 提出 FineMOP，以细粒度分析加速演化感知运行时验证，减少无关 spec 重监控；较类级方法最高快4.86×，每修订少重监控81.04% spec，仍发现99.68%新违规。

**Abstract:** Runtime verification found many bugs by monitoring passing tests in many open-source projects against formal specifications (specs). But, RV is often too slow for use in continuous integration. So, evolution-aware techniques were proposed to speed up RV by re-monitoring only a subset of specs affected by code changes. These techniques use coarse-grained class-level analyses, so they can sub-optimally and imprecisely re-monitor unaffected specs. We propose FineMOP to speed up evolution-aware RV by using fine-grained analyses to re-monitor fewer unaffected specs. The key idea is simple: changes often do not require re-monitoring specs that are only related to unchanged parts of changed classes. We implement six variants of three fine-grained analyses in FineMOP and evaluate it on 1,104 revisions of 68 open-source Java projects. Compared with two class-level techniques, FineMOP is up to 4.86x faster, re-monitors up to 81.04% fewer specs per revision, and finds 99.68% of all new violations that these techniques find. Also, FineMOP and Regression Test Selection (RTS) are complementary: combining FineMOP with RTS is faster than FineMOP or RTS alone.

## 25. FrameShift: Resizing Fuzzer Inputs Without Breaking Them

**Authors:** Harrison Green (Carnegie Mellon University), Claire Le Goues (Carnegie Mellon University), Fraser Brown (CMU)

**Categories:** Testing and Analysis

**中文总结:** 提出 FrameShift，检测输入格式 relation field 以避免 frameshift 破坏性变异；集成 AFL++/LibAFL 后覆盖率有时提升超50%。

**Abstract:** Coverage-guided fuzzers are powerful automated bug-finding tools. They mutate program inputs, observe coverage, and save any input that hits an unexplored path for future mutation. Unfortunately, without knowledge of input formats—for example, the relationship between formats’ data fields and sizes—fuzzers are prone to generate destructive frameshift mutations. These time-wasting mutations yield malformed inputs that are rejected by the target program. To avoid such breaking mutations, this paper proposes a novel, lightweight technique that preserves the structure of inputs during mutation by detecting and using relation fields. Our technique, FrameShift, is simple, fast, and does not require additional instrumentation beyond standard coverage feedback. We implement our technique in two state-of-the-art fuzzers, AFL++ and LibAFL, and perform a 12+ CPU-year fuzzer evaluation, finding that FrameShift improves the performance of the fuzzer in each configuration, sometimes increasing coverage by more than 50%. Furthermore, through a series of case studies, we show that our technique is versatile enough to find important structural relationships in a variety of formats, even generalizing beyond C/C++ targets to both Rust and Python.

## 26. Fuzzing Java Optimizing Compilers with Complex Inter-Class Structures Guided by Heterogeneous Program Graphs

**Authors:** Shiyu Qiu (Huazhong University of Science and Technology), Ming Wen (Huazhong University of Science and Technology), Zifan Xie (Huazhong University of Science and Technology), Hai Jin (Huazhong University of Science and Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出 InterFuzz，以异构程序图 HPG 引导生成复杂类间结构的 Java 测试；在 HotSpot/ART/R8 发现24个新 bug（20确认，16与类间结构相关）。

**Abstract:** Modern Java compilers, such as Just-In-Time (JIT) and Ahead-OfTime (AOT) compilers, often infer and analyze complex inter-class structures to perform program optimizations while preserving semantic correctness. However, incorrect inference of these structures during compilation can lead to critical bugs, as observed in production compilers like HotSpot and R8. Despite their significance, existing Java fuzzing tools fail to adequately explore inter-class relationships, focusing instead on simpler intra-class or intra-method constructs. To bridge this gap, we present InterFuzz, the first fuzzing framework designed to systematically generate Java test cases with complex inter-class structures. InterFuzz introduces a novel concept of Heterogeneous Program Graph (HPG) to abstract and manipulate inter-class relationships. It then employs Inter-Class Mutators to construct intricate interactions, and utilizes Graph Complexity to guide test generation toward high-diversity code. Our evaluation shows that InterFuzz effectively uncovers compiler bugs that elude traditional fuzzers, having discovered 24 new bugs across HotSpot, ART, and R8, with 20 confirmed by developers—16 of which hinge on intricate inter-class structures.

## 27. Fuzzing JavaScript Engines by Fusing JavaScript and WebAssembly

**Authors:** Jiayi Lin (The University of Hong Kong), Changhua Luo (The University of Hong Kong; Wuhan University), Mingxue Zhang (Zhejiang University), Lanteng Lin (The University of Hong Kong), Penghui Li (Columbia University), Chenxiong Qian (University of Hong Kong)

**Categories:** Testing and Analysis

**中文总结:** 提出 Mad-Eye，融合 JavaScript 与 WebAssembly 的跨语言 fuzzing；在 V8/SpiderMonkey/JSC 发现21个未知漏洞（18确认，13已修复）。

**Abstract:** JavaScript engines are a fundamental part of modern browsers, and many efforts have been invested in testing them to enhance their security. However, the incorporation of WebAssembly into JavaScript engines introduces new attack surfaces that have not received sufficient attention. Existing fuzzers for JavaScript engines primarily focus on JavaScript, neglecting WebAssembly code and its interactions with JavaScript. We introduce Mad-Eye, the first fuzzer that can test the JavaScript-WebAssembly interaction using a novel cross-language code fusion technique. Evaluations of Mad-Eye on V8, SpiderMonkey, and JavaScriptCore detected 21 previously unknown vulnerabilities, with 18 confirmed and 13 fixed and merged into mainstream browsers, who acknowledged our reports with vulnerability bounties.

## 28. Generator Solving for Symbolic Execution

**Authors:** Siwei Wei (State Key Laboratory of Computer Science, Institute of Software, Chinese Academy of Sciences, and University of Chinese Academy of Sciences Beijing, China), Yan Cai (Institute of Software at Chinese Academy of Sciences)

**Categories:** Testing and Analysis

**中文总结:** 提出 generator solving：为符号执行中的 SMT 约束生成可重复采样解的生成器而非单次解，并实现 GenSlv，在 KLEE 等工具上可将分支覆盖提升最多一倍以上。

**Abstract:** Automated test input generation based on symbolic execution has garnered significant research interest. However, the main drawback of symbolic execution is its poor scalability. Since the overhead associated with constraint modeling and solving is high, generating only one test input per SMT query is inefficient. In this paper, we introduce the concept of generator solving. Instead of solving for only one particular solution, we propose to find a generator that can be called multiple times to continuously yield new test inputs. This approach offers several benefits: (1) it allows efficient generation of as many test inputs as needed, thereby significantly improving the input generation efficiency of symbolic execution methods; (2) the continuously generated inputs facilitate a more comprehensive exploration of the solution set, potentially triggering new program behaviors; and (3) compared to hybrid approaches based on mutation, using a generator ensures the satisfiability of the target constraints. We present three key techniques for generator solving: (1) reusing invertible model converters in Z3 as generators; (2) constructing hierarchical range-based samplers to sample solutions of range constraints; and (3) employing optimistic simplification strategies to enhance the generality of the solving process. We have implemented GenSlv, a prototypical generator solver specifically designed for automated test case generation based on symbolic execution. Evaluation results demonstrate that (1) GenSlv is effective in finding generators for constraints collected from real-world programs (specifically, GenSlv can find a generator for 97% of the constraints that have at least two different solutions), and (2) GenSlv significantly and consistently improves the performance of commonly used symbolic executors (including KLEE, Angr, TritonDSE, and SymCC) in terms of program coverage and vulnerability detection across various settings in symbolic execution and hybrid fuzzing tasks, with a maximum of more than twofold increase in branch coverage.

## 29. GPTrace: Effective Crash Deduplication Using LLM Embeddings

**Authors:** Patrick Herter (Fraunhofer AISEC), Vincent Ahlrichs (Fraunhofer AISEC), Ridvan Açilan (Technical University of Munich), Julian Horsch (Fraunhofer AISEC)

**Categories:** Testing and Analysis

**中文总结:** 提出 GPTrace，用 LLM 嵌入向量对崩溃相关数据进行相似度聚类以去重 fuzz 崩溃，在 30 万+ 崩溃样本上优于传统栈迹比对等基线。

**Abstract:** Fuzzing is a highly effective method for uncovering software vulnerabilities, but analyzing the resulting data typically requires substantial manual effort. This is amplified by the fact that fuzzing campaigns often find a large number of crashing inputs, many of which share the same underlying bug. Crash deduplication is the task of finding such duplicate crashing inputs and thereby reducing the data that needs to be examined. Many existing deduplication approaches rely on comparing stack traces or other information that is collected when a program crashes. Although various metrics for measuring the similarity of such pieces of information have been proposed, many do not yield satisfactory deduplication results. In this work, we present GPTrace, a deduplication workflow that leverages a large language model to evaluate the similarity of various data sources associated with crashes by computing embedding vectors and supplying those as input to a clustering algorithm. We evaluate our approach on over 300 000 crashing inputs belonging to 50 ground truth labels from 14 different targets. The deduplication results produced by GPTrace show a noticeable improvement over hand-crafted stack trace comparison methods and even more complex state-of-the-art approaches that are less flexible.

## 30. Hallucinating Certificates: Differential Testing of TLS Certificate Validation Using Generative Language Models

**Authors:** Muhammad Talha Paracha (Ruhr University Bochum), Kyle Posluns (Northeastern University), Kevin Borgolte (Ruhr University Bochum), Martina Lindorfer (TU Wien), David Choffnes (Northeastern University)

**Categories:** Testing and Analysis

**中文总结:** 提出 MLCerts，利用生成式语言模型“幻觉”合成 TLS 证书做差分测试，在 OpenSSL 等 5 个实现上发现的实现差异比 Transcert 多 30%、比 Frankencerts 多一个数量级。

**Abstract:** Certificate validation is a crucial step in Transport Layer Security (TLS), the de facto standard network security protocol. Prior research has shown that differentially testing TLS implementations with synthetic certificates can reveal critical security issues, such as accidentally accepting untrusted certificates. Leveraging known techniques, like random input mutations and program coverage guidance, prior work created corpora of synthetic certificates. By testing the certificates with multiple TLS libraries and comparing the validation outcomes, they discovered new bugs. In this paper, we introduce a new approach, MLCerts, to generate synthetic certificates for differential testing that leverages generative language models to more extensively test implementations. Recently, these models have become (in)famous for their applications in generating content, writing code, and conversing with users, as well as for “hallucinating” syntactically correct yet semantically nonsensical output. In our work, we provide and leverage two novel insights: (a) TLS certificates can be expressed in natural-like language, as they can be defined in the X.509 standard that aids human readability, and (b) differential testing can benefit from hallucinated malformed test cases. Using our approach MLCerts, we find significantly more distinct discrepancies between the five TLS implementations OpenSSL, LibreSSL, GnuTLS, MbedTLS, and MatrixSSL than the state-of-the-art benchmark Transcert (+30%; 20 vs 26, out of a maximum possible of 30) and an order of magnitude more than the seminal work Frankencerts (+1,200%; 2 vs 26). Finally, we show that the diversity of MLCerts-generated certificates reveals a range of previously unobserved and interesting behavior with security implications.

## 31. How Good are Input Grammar Miners? An Empirical Study

**Authors:** Leon Bettscheider (CISPA Helmholtz Center for Information Security), Andreas Zeller (CISPA Helmholtz Center for Information Security)

**Categories:** Testing and Analysis

**中文总结:** 对多种输入文法挖掘工具做系统评测，指出仅用短输入检验会高估精度，用 k-path 覆盖衡量深层多样性后多种方法在 JSON、Tiny-C 等语言上精度显著下降。

**Abstract:** To generate valid test inputs for a system, one needs a \emph{specification} of its input language—typically a \emph{context-free grammar} that describes input syntax. But where can one get such a grammar from? In the past years, the field of \emph{input grammar mining} has emerged, with creative approaches to extract input grammars from inputs, code, or both. But how good are these approaches? In particular; How \emph{accurate} are the grammars they mine? In this study, we systematically \emph{evaluate} grammar miners for these questions. Notably, we find that the previous evaluations conducted by the respective authors—producing a set of inputs from a golden grammar and having them checked by the mined grammar, or vice versa—are insufficient, as they have a strong bias towards short, possibly unrealistic inputs. We therefore also measure the \emph{diversity} of the mined grammars using \emph{$k$-path coverage} with varying depths~$k$ to find how many \emph{combinations} of grammar elements are actually represented. Ideally, a mined grammar should have perfect precision and recall regardless of the depth $k$. However, our results show that for all approaches presented so far, precision and recall can drop significantly compared to reported results when increasing~$k$ and thus checking for ``deeper'' diversity, especially for complex input languages such as Lisp, JSON, or Tiny-C. For instance, the Tiny-C grammar mined by Arvada achieves a precision of 75% when considering $k$-paths with $k = 1$ (the originally reported precision was 73%), but this drops to 46% for $k = 5$. White-box approaches based on program analysis, such as Mimid and Stalagmite, are more stable with varying depth $k$, but can be challenged by complex parsers such as mjs. Raising the bars for evaluation, our study shows that there is still room for improvement in grammar mining.

## 32. Hybrid Fault-Driven Mutation Testing for Python

**Authors:** Saba Alimadadi (Simon Fraser University), Golnaz Gharachorlu (University of Ottawa)

**Categories:** Testing and Analysis

**中文总结:** 提出 PyTation，结合 7 个面向 Python 反模式的变异算子与静/动态混合分析做变异测试，在 13 个项目上生成与通用工具互补的变异体并暴露高覆盖测试套件不足。

**Abstract:** Mutation testing is an effective technique for assessing the effectiveness of test suites by systematically injecting artificial faults into programs. However, existing mutation testing techniques fall short in capturing many types of common faults in dynamically-typed languages like Python. In this paper, we introduce a novel set of seven mutation operators that are inspired by prevalent anti-patterns in Python programs, designed to complement the existing general-purpose operators and broaden the spectrum of simulated faults. We propose a mutation testing technique that utilizes a hybrid of static and dynamic analyses to mutate Python programs based on these operators while minimizing equivalent mutants. We implement our approach in a tool called PyTation and evaluate it on 13 open-source Python applications. Our results show that PyTation generates mutants that complement those from general-purpose tools, exhibiting distinct behaviour under test execution and uncovering inadequacies in high-coverage test suites. We further demonstrate that PyTation produces a high proportion of unique mutants, a low cross-kill rate, and a low test overlap ratio relative to baseline tools, highlighting its novel fault model. PyTation also incurs few equivalent mutants, aided by dynamic analysis heuristics.

## 33. Is Call Graph Pruning Really Effective? An Empirical Re-evaluation

**Authors:** Mohammad Rafieian (The University of Texas at Dallas), Vlad Birsan (The University of Texas at Dallas), Kunal Katiya (Coppell High School), Dylan Zhong, Shiyi Wei (University of Texas at Dallas)

**Categories:** Testing and Analysis

**中文总结:** 重评调用图剪枝 ML 方法，指出原评测存在数据集与标签问题；新数据集与多框架实验显示剪枝提升精度但以显著覆盖损失为代价。

**Abstract:** Recently proposed call graph pruning techniques, which use machine learning to predict and reduce false positives in static call graphs, have reported impressive results and demonstrated practicality for downstream analyses. However, as we research the methodology of how datasets are created and how evaluation is conducted in these research projects, we identify many risk factors that may make the reported results incomplete or even invalid. We further investigate these factors and provide empirical evidence to demonstrate they indeed result in misleading results. Motivated by these findings, we propose an empirical re-evaluation of existing call graph pruning techniques to assess their effectiveness. We first construct a new dataset of real-world programs, applying three complementary labeling approaches, resulting in 41,952 labels. To provide a full picture of these techniques, we utilize three popular call graph analysis frameworks (WALA, Doop, and OPAL) and seven tool configurations. Our results show that pruning is not as effective as reported in prior work, improving precision at the cost of significant coverage loss. We further train more general models across analysis tools and configurations, and explore the impact of data splitting and balancing. We find these models often match or outperform the existing configuration-specific ones, indicating their applicability in more general settings. Finally, we highlight the open challenges and potential solutions, including the need for better datasets as well as improved feature engineering.

## 34. Is My RPC Response Reliable? Detecting RPC Bugs in Blockchain Client under Context

**Authors:** Zhijie Zhong (School of Software Engineering, Sun Yat-sen University), Yuhong Nan (Sun Yat-sen University), Mingxi Ye (Sun Yat-sen University), Qing Xue (Sun Yat-sen University), Jiashui Wang (Zhejiang University), Long Liu, Xinlei Ying, Zibin Zheng (Sun Yat-sen University)

**Categories:** Testing and Analysis

**中文总结:** 提出 EthCRAFT，通过探索区块链客户端状态空间构造上下文并对 RPC 做差分 fuzz，在以太坊客户端中发现 6 个新 bug 且 3 个获基金会漏洞赏金。

**Abstract:** Blockchain clients are fundamental software for running blockchain nodes. They provide users with various RPC (Remote Procedure Call) interfaces to interact with the blockchain. These RPC methods are expected to follow the same specification across different blockchain nodes, providing users with seamless interaction. However, there have been continuous reports on various RPC bugs that can cause unexpected responses or even Denial of Service weakness. Existing studies on blockchain RPC bug detection mainly focus on generating the RPC method calls for testing blockchain clients. However, a wide range of the reported RPC bugs are triggered in various blockchain contexts. To the best of our knowledge, little attention is paid to generating proper contexts that can trigger these context-dependent RPC bugs. In this work, we propose EthCRAFT, a Context-aware RPC Analysis and Fuzzing Tool for client RPC bug detection. EthCRAFT first proposes to explore the state transition program space of blockchain clients and generate various transactions to construct the context. EthCRAFT then designs a context-aware RPC method call generation method to send RPC calls to the blockchain clients. The responses of 5 different client implementations are used as cross-referring oracles to detect the RPC bugs. We evaluate EthCRAFT on real-world RPC bugs collected from the GitHub issues of Ethereum client implementations. Experiment results show that EthCRAFT outperforms existing client RPC detectors by detecting more RPC bugs. Moreover, EthCRAFT has found six new bugs in major Ethereum clients and reported them to the developers. One of the bug fixes has been written into breaking changes in the client’s updates. Three of our bug reports have been offered a vulnerability bounty by the Ethereum Foundation.

## 35. Learning without Forgetting: Towards Continual learning of Fault Localization Models in Industrial Software Systems

**Authors:** Chun Li (Nanjing University), Hui Li (Samsung Electronics (China) R&D Centre), Zhong Li (Nanjing University), Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Testing and Analysis

**中文总结:** 提出 Canto 持续学习框架，结合日志语义、故障特征与代表性样本混合训练，在工业级故障定位上比 6 个持续学习基线效果提升 17.30%–45.23%。

**Abstract:** Learning-based fault localization has achieved promising results. However, as software and tests are constantly evolving, models trained on old data become ineffective on new data. Particularly, in the context of system testing for large-scale software, each iteration generates a large volume of new data. This makes retraining the model from scratch incur an unacceptable time overhead, while merely fine-tuning on new data leads to catastrophic forgetting. Continual learning offers an effective method for models to avoid catastrophic forgetting during this iterative process. However, existing continual learning methods are not specifically designed for fault localization or for large-scale software system testing scenarios, which leads to their direct application yielding sub-optimal effectiveness. In response, we propose Canto, a novel continual learning framework specifically designed for large-scale software fault localization. Canto first extracts fine-grained program semantics from logs, then utilizes fault characteristics to enhance the weights of certain semantics. Finally, Canto uses an unsupervised algorithm to obtain corresponding embeddings and selects representative exemplars based on clustering. Subsequently, Canto mixes the representative exemplars with new samples for training and adjusts the loss weight according to the model’s degree of mastery over the sample. This allows the model to focus more on samples that are not yet well-mastered during the training process, thereby enabling it to learn new faults while mitigating the forgetting of old ones. In extensive evaluations against 6 continual learning baselines, Canto demonstrates superior performance, improving overall effectiveness by 17.30% to 45.23%.

## 36. LLM4Perf: Large Language Models Are Effective Samplers for Multi-Objective Performance Modeling

**Authors:** Xin Wang (The Hong Kong University of Science and Technology (Guangzhou)), Zhenhao Li (York University), Zishuo Ding (The Hong Kong University of Science and Technology (Guangzhou))

**Categories:** Testing and Analysis

**中文总结:** 提出 LLM4Perf 反馈式采样框架，用 LLM 做配置空间剪枝与策略 refinement，在 112 个评估场景中 68.8% 为最佳且还能增强传统采样方法。

**Abstract:** The performance of modern software systems is critically dependent on their complex configuration options. Building accurate performance models to navigate this vast configuration space requires effective sampling strategies, yet existing methods often struggle with multi-objective optimization and fail to leverage semantic information from documentation. The recent success of Large Language Models (LLMs) motivates the central question of this work: Can LLMs serve as effective samplers for multi-objective performance modeling? To explore this question, we present a comprehensive empirical study investigating the capabilities and characteristics of LLM-driven sampling. We design and implement LLM4Perf, a feedback-based framework, and use it to systematically evaluate LLM-guided sampling across four highly configurable, real-world systems. Our study reveals that the LLM-guided approach outperforms traditional baselines in most cases. Quantitatively, LLM4Perf achieves the best performance in nearly 68.8% (77 out of 112) of all evaluation scenarios, demonstrating its superior effectiveness. We find that this effectiveness stems from the LLM’s dual capabilities: configuration space pruning and feedback-driven strategy refinement. The strength of the pruning mechanism is further validated by the fact that it also enhances the performance of baseline methods in 91.5% (410 out of 448) of cases. Furthermore, we analyze how the selection of LLMs for different components and hyperparameters within LLM4Perf affects its overall effectiveness. Overall, this paper provides strong empirical evidence that LLMs can serve as powerful and effective samplers in performance engineering and offers concrete insights into the mechanisms driving their success.

## 37. LoopSCC: Summarizing Complex Multi-branch Nested Loops via Periodic Oscillation Interval

**Authors:** Kai Zhu (Institute of Information Engineering, Chinese Academy of Sciences; University of Chinese Academy of Sciences), Haofeng Li (SKLP, Institute of Computing Technology, CAS), Kuihao Yan (Institute of Information Engineering, Chinese Academy of Sciences), Rongqing Wang (Institute of Information Engineering, Chinese Academy of Sciences), Jiaming Guo (Institute of Information Engineering, Chinese Academy of Sciences), Haoran Yang (Institute of Information Engineering, Chinese Academy of Sciences), Jie Lu (Institute of Computing Technology, Chinese Academy of Sciences), Lei Yu (Institute of Software, Chinese Academy of Sciences, University of Chinese Academy of Sciences, China), Xiaoqi Jia (Institute of Information Engineering, Chinese Academy of Sciences), Chenkai Guo (Nankai University, China), Haichao Du (Institute of Information Engineering, Chinese Academy of Sciences), Qingjia Huang (Institute of Information Engineering, Chinese Academy of Sciences), Yamin Xie (Institute of Information Engineering，Chinese Academy of Science；University of Chinese Academy of Sciences), Jing Tang (Institute of Information Engineering, Chinese Academy of Sciences)

**Categories:** Testing and Analysis

**中文总结:** 提出 LoopSCC，用 SPath 图与 SCC 振荡区间摘要复杂多分支嵌套循环，集成 Angr 后在 11 个 IoT 项目发现 18 个未知漏洞（7 个获 CVE）。

**Abstract:** Analyzing programs with loops is a challenging task, suffering from potential issues such as the indeterminate number of iterations and exponential growth of control flow complexity. Loop summarization based on static symbolic analysis receives increasing focus in the field of loop program analysis. However, current loop summarization methods are only suitable for single-branch loops or multi-branch loops with simple cycles and fail to handle complex multi-branch nested loops with intricate non-functional variables and irregular jumps between multiple branches. In this paper, we propose a novel loop summarization approach based on symbolic analysis to address the complex loops mentioned above and develop a tool named LoopSCC. For a non-nested loop, LoopSCC constructs an \textit{SPath Graph}, where each node represents a path from entry to exit of the control flow graph of the loop and contracts it to an acyclic graph by collapsing each strongly connected component (SCC) into a single node. The summarization of a loop is the disjunction of the summaries of each path in the acyclic graph. For non-functional variables and irregular jumps, we iteratively model a valid value and refine the conditions until reaching the minimum. We introduce the oscillation interval, within which SPaths in the SCC can jump between one another. Outside this interval, no such jumps occur. This allows us to transform loop iteration transitions into a piecewise function, then summarize the interest variables according to the piecewise function. For nested loops, we construct summaries using the approaches above and apply them sequentially from the innermost loop to the outermost. Comparing state-of-the-art loop summarization tools, LoopSCC can handle more types of loops with 100% precision. We integrated LoopSCC with the symbolic execution tool, Angr, to enhance its efficiency, which enabled the detection of 18 previously unknown vulnerabilities across 11 IoT projects, 7 of which were assigned CVEs. The LoopSCC is publicly available at https://anonymous.4open.science/r/LoopSCC-386F .

## 38. LSPRAG: LSP-Guided RAG for Language-Agnostic Real-Time Unit Test Generation

**Authors:** Gwihwan Go (Tsinghua University), Quan Zhang (East China Normal University), Chijin Zhou (East China Normal University), Zhao Wei (Tencent), Yu Jiang (Tsinghua University)

**Categories:** Testing and Analysis

**中文总结:** 提出 LSPRAG，复用 LSP 实时检索符号定义/引用作为 LLM 单元测试上下文，在 Java/Go/Python 上 line coverage 相对基线最高提升 174%–213%。

**Abstract:** Automated unit test generation is essential for robust software development, yet existing approaches struggle to generalize across multiple programming languages and operate within real-time development. While Large Language Models (LLMs) offer a promising solution, their ability to generate high coverage test code depends on prompting a concise context of the focal method. Current solutions, such as Retrieval-Augmented Generation, either rely on imprecise similarity-based searches or demand the creation of costly, language-specific static analysis pipelines. To address this gap, we present LSPRAG, a framework for concise-context retrieval tailored for real-time, language-agnostic unit test generation. LSPRAG leverages off-the-shelf Language Server Protocol (LSP) back-ends to supply LLMs with precise symbol definitions and references in real time. By reusing mature LSP servers, LSPRAG provides an LLM with language-aware context retrieval, requiring minimal per-language engineering effort. We evaluated LSPRAG on open-source projects spanning Java, Go, and Python. Compared to the best performance of baselines, LspRag increased line coverage by up to 174.55% for Golang, 213.31% for Java, and 31.57% for Python.

## 39. Memory-Efficient Large Language Models for Program Repair with Semantic-Guided Patch Generation

**Authors:** Thanh Le-Cong (Singapore University of Technology and Design, Singapore), Xuan-Bach D. Le (University of Melbourne), Toby Murray (University of Melbourne)

**Categories:** Testing and Analysis

**中文总结:** 提出 FLAMES，用语义引导 best-first 搜索替代 beam search 做 LLM APR，在 Defects4J 上内存降最高 83% 且多修 10 个 bug（共 133 个）。

**Abstract:** Fixing software bugs is crucial yet demands significant resources from developers. Automated Program Repair (APR) is a promising solution to address this challenging task. The emergence of Large Language Models (LLMs) has opened a new era of LLM-based APR, substantially advancing the APR field further. LLM-based APR methods face significant challenges regarding memory inefficiency, hindering their scalability and effectiveness. This is largely due to the beam search utilized in the patch generation phase of LLM-based APR, which requires large beam sizes to search for more potentially good repair candidates. In this paper, we first show that increases in beam size, even for small-sized LLMs (1B-7B params), require extensive GPU usage, leading to up to 80% of recurring crashes due to memory overloads in LLM-based APR. Seemingly simple solutions to reduce memory consumption are (1) to quantize LLM models, i.e., converting the weights of an LLM from high-precision values to lower-precision ones, and (2) to make beam search sequential, i.e., forwarding each beam through the model sequentially and then concatenating them back into a single output. However, we show that these approaches still do not work via both theoretical analysis and experiments. To address this, we introduce FLAMES, a novel LLM-based APR technique that employs semantic-guided patch generation to enhance repair effectiveness and memory efficiency. Unlike conventional methods that rely on beam search, FLAMES utilizes greedy decoding to enhance memory efficiency while steering the search towards more potentially good repair candidates via a semanticguided best-first search algorithm. At each decoding step, FLAMES uses semantic feedback from test validation, such as the number of passing and failing test cases, to select the most promising token to explore further. Our empirical evaluation on Defects4J shows that FLAMES substantially reduces memory consumption by up to 83% compared to LLM-based APR without compromising time efficiency. Moreover, FLAMES correctly fixes 133 bugs on Defects4J, fixing 10 bugs more than the best baseline. Additionally, these improvements also generalize to the HumanEval-Java and TransformedD4J datasets, where FLAMES generates 12% and 36.5% more correct patches, respectively, than the best baseline.

## 40. Metamorphic Fuzzing for Multi-Agent Path Finding Algorithms

**Authors:** Luxia Lin (Institute of Software, Chinese Academy of Sciences, China), xudong zhang, Shihao Zhu (State Key Laboratory of Computer Science,Institute of Software,Chinese Academy of Sciences,China), Yan Cai (Institute of Software at Chinese Academy of Sciences)

**Categories:** Testing and Analysis

**中文总结:** 提出 MAPFFuzz 蜕变 fuzz 框架，联合变异地图与智能体配置并用语义 oracle 检测 MAPF 求解器完备性与最优性失败，在 PIBT 等求解器上发现大量次优与不可解案例。

**Abstract:** Multi-Agent Path Finding (MAPF) is a fundamental problem in multi-agent systems, with broad applications in warehouse logistics, robotics, and autonomous driving. Ensuring that MAPF solvers consistently return a solution whenever one exists and deliver high-quality plans is critical for real-world deployment. However, MAPF algorithms remain insufficiently tested. The high-dimensional, tightly coupled input space arising from map topology and agent configurations makes systematic testing extremely challenging. This paper introduces MAPFFuzz, a metamorphic fuzzing framework for systematically testing MAPF solvers to detect both completeness failures and optimality failures. MAPFFuzz uses semantics-aware mutation strategies that jointly perturb both maps and agent configurations, coupled with a lightweight feasibility verification mechanism to ensure valid scenarios. Additionally, it incorporates diversity-guided seed selection and leverages metamorphic relations as oracles to assess solution quality. We evaluate MAPFFuzz on four recent MAPF solvers: PIBT, HCA, PIBT+, and LaCAM*. Results show that MAPFFuzz can detect completeness failures and more than 400 cases with degree of suboptimality exceeding 25% with 100 agents on 128x128 map cases per solver. MAPFFuzz also identifies 37 scenarios unsolvable by LaCAM* even under a 30-second parallel optimization setting. These findings demonstrate that MAPFFuzz can reveal both completeness failures and significant solution degradations, even in state-of-the-art algorithms under generous time budgets.

## 41. META²V2V: Revealing Behavioural Deviations under Mutual Perception in Multi-Vehicle Autonomous Driving

**Authors:** Lejin Li (Kyushu University), Xiao-Yi Zhang (University of Science and Technology Beijing), Shuncheng Tang (University of Science and Technology of China), Zhenya Zhang (Kyushu University), Jianjun Zhao (Kyushu University)

**Categories:** Testing and Analysis

**中文总结:** 提出 META²V2V 蜕变测试框架，向 V2V 共享信息注入四类扰动并用 soundness/robustness MR 评估多车 ADS，相对随机测试多发现 733.3%/133.0% 违规场景。

**Abstract:** In next-generation traffic, multiple intelligent vehicles equipped with autonomous driving systems (ADS) operate simultaneously. These vehicles share real-time information through vehicle-to-vehicle (V2V) communication during operation and make decisions based on this mutual perception. In this paper, we present a novel METAmorphic testing framework to evaluate ADS performance in multi-vehicle scenarios, addressing the META information shared during V2V communication (META²V2V). META²V2V interacts with the shared information by systematically injecting four types of controlled common perturbations into V2V data streams and observing how these disruptions affect the vehicles’ mutual perception and subsequent interactions. META²V2V assesses ADS decisions from two aspects: soundness and robustness, by introducing soundness metamorphic testing relations (S-MRs) and robustness metamorphic relations (R-MRs), respectively. Specifically, S-MRs claim that the performance of ADS under perfect information should outperform that under perturbations, whereas R-MRs claim that the performance of ADS should not degrade too much under information perturbations. Furthermore, META²V2V employs multi-objective search-based testing conducted from two directions to efficiently generate test groups that violate S-MRs and R-MRs, respectively. Experimental results demonstrate that, compared to random testing, our approach can identify 733.3% and 133.0% more violations that reveal soundness and robustness issues.

## 42. MioHint: LLM-Assisted Request Mutation for Whitebox REST API Testing

**Authors:** Jia Li (The Chinese University of Hong Kong), Jiacheng Shen (Duke Kunshan University), Yuxin Su (Sun Yat-sen University), Michael Lyu (The Chinese University of Hong Kong)

**Categories:** Testing and Analysis

**中文总结:** 提出 MioHint，结合语句级数据依赖检索与 LLM 做白盒 REST API 请求变异，在 16 个服务上 line coverage 比 EvoMaster 平均高 4.95%，变异准确率提升 67 倍。

**Abstract:** Cloud applications heavily rely on APIs to communicate with each other and exchange data. To ensure the reliability of cloud applications, cloud providers widely adopt API testing techniques. Unfortunately, existing API testing approaches are insufficient to reach strict conditions, a problem known as fitness plateaus, due to the lack of a gradient provided by coverage metrics. To address this issue, we propose MioHint, a novel white-box API testing approach that leverages the code comprehension capabilities of LLM to boost API testing. The key challenge of LLM-based API testing lies in system-level testing, which emphasizes the dependencies between requests and targets across functions and files, thereby making the entire codebase the object of analysis. However, feeding the entire codebase to an LLM is impractical due to its limited context length and short memory. MioHint addresses this challenge by synergizing static analysis with LLMs. We retrieve relevant code with data-dependency analysis at the statement level, including def-use analysis for variables used in the target and function expansion for subfunctions called by the target. To evaluate the effectiveness of our method, we conducted experiments across 16 real-world REST API services. The findings reveal that MioHint achieves an average increase of 4.95% in line coverage compared to the baseline, EvoMaster, alongside a remarkable factor of 67x improvement in mutation accuracy. Furthermore, our method successfully covers over 57% of hard-to-cover targets, while in the baseline, the coverage is less than 10%.

## 43. Misbehavior Forecasting for Focused Autonomous Driving Systems Testing

**Authors:** M M Abid Naziri (North Carolina State University), Stefano Carlo Lambertenghi (Technische Universität München, fortiss GmbH), Andrea Stocco (Technical University of Munich, fortiss), Marcelo d'Amorim (North Carolina State University)

**Categories:** Testing and Analysis

**中文总结:** 提出 Foresee，用 misbehavior forecaster 识别仿真近失事件并局部 fuzz，在 CARLA 上比随机与 SOTA 预测器多暴露 128.70%/38.09% 失败且更快，可与 DriveFuzz 互补。

**Abstract:** Simulation-based testing is the standard practice for assessing the reliability of self-driving cars’ software before deployment. Existing bug-finding techniques are either unreliable or expensive. We build on the insight that near misses observed during simulations may point to potential failures. We propose Foresee, a technique that identifies near misses using a misbehavior forecaster that computes possible future states of the ego-vehicle under test. Foresee performs local fuzzing in the neighborhood of each candidate near miss to surface previously unknown failures. In our empirical study, we evaluate the effectiveness of different configurations of Foresee using several scenarios provided in the CARLA simulator on both end-to-end and modular self-driving systems and examine its complementarity with the state-of-the-art fuzzer DriveFuzz. Our results show that Foresee is both more effective and more efficient than the baselines. Foresee exposes 128.70% and 38.09% more failures than a random approach and a state-of-the-art failure predictor while being 2.49× and 1.42× faster, respectively. Moreover, when used in combination with DriveFuzz, Foresee enhances failure detection by up to 93.94%.

## 44. MutDafny: A Mutation-Based Approach to Assess Dafny Specifications

**Authors:** Isabel Amaral (INESC TEC, Faculty of Engineering, University of Porto), Alexandra Mendes (Faculty of Engineering, University of Porto & INESC TEC), José Campos (Faculty of Engineering of the University of Porto, Portugal)

**Categories:** Testing and Analysis

**中文总结:** 提出 MutDafny，用 32 个 Dafny 变异算子评估形式化规约强度，在 794 个项目中平均每 241 行代码发现一处需加强的真实弱规约。

**Abstract:** This paper explores the use of mutation testing to reveal weaknesses in formal specifications written in Dafny. In verification-aware programming languages, such as Dafny, despite their critical role, specifications are as prone to errors as implementations. Flaws in specs can result in formally verified programs that deviate from the intended behavior. We present MutDafny, a tool that increases the reliability of Dafny specifications by automatically signaling potential weaknesses. Using a mutation testing approach, we introduce faults (mutations) into the code and rely on formal specifications for detecting them. If a program with a mutant verifies, this may indicate a weakness in the specification. We extensively analyze mutation operators from popular tools, identifying the ones applicable to Dafny. In addition, we synthesize new operators tailored for Dafny from bugfix commits in publicly available Dafny projects on GitHub. Drawing from both, we equipped our tool with a total of 32 mutation operators. We evaluate MutDafny’s effectiveness and efficiency in a dataset of 794 real-world Dafny programs and we manually analyze a subset of the resulting undetected mutants, identifying five weak real-world specifications (on average, one at every 241 lines of code) that would benefit from strengthening.

## 45. No Shot in the Dark: Efficient Context-Free Language Reachability via Context-Aware Tabulation

**Authors:** Chenghang Shi (SKLP, Institute of Computing Technology, CAS), Lian Li (Institute of Computing Technology at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Testing and Analysis

**中文总结:** 提出 context-aware tabulation（CAT），在 CFL 可达性分析中加入受限上下文敏感性以剔除无效边，在三类客户端上加速 1.49x–2.13x 且内存降 24%–50%。

**Abstract:** Context-free language (CFL) reachability is a widely used framework for formulating static program analyses. Operating over edge-labeled graphs, the standard algorithm performs context-free tabulation by iteratively deriving new edges that summarize paths whose labels conform to the production rules of a context-free grammar. However, as the term ``context-free'' suggests, these derivations are made without considering the surrounding context of inferred edges, often resulting in unproductive edges that do not contribute to the final reachability result. In this paper, we present \emph{context-aware tabulation} (CAT), a novel approach that incorporates a restricted form of context sensitivity into CFL-reachability analysis to eliminate such unproductive edges. Comprehensive experiments on three widely studied clients show that CAT significantly accelerates reachability solving—achieving speedups of 1.75x, 1.49x, and 2.13x—and also reduces memory usage by 33.28%, 24.24%, and 50.15%, respectively, compared to a state-of-the-art solver.

## 46. NotDec: WebAssembly Decompilation With Inter-Procedural Type Recovery

**Authors:** Jikai Wang (Huazhong University of Science and Technology), Ningyu He (Hong Kong Polytechnic University), Tianming Liu (Huazhong University of Science and Technology), Junhai Wang (Huazhong University of Science and Technology), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出 NotDec WebAssembly 反编译框架，扩展类型检查、Retypd 过程间类型恢复与 Memory SSA，Juliet/Howard 重编译成功率 100%，结构体成员访问恢复率 85.33%。

**Abstract:** With WebAssembly widely supported in browsers, containers, IoT devices, and serverless platforms and increasingly adopted as a universal low‑level bytecode standard, auditing its hidden vulnerabilities and malicious intentions has become critical. Decompiling existing WebAssembly modules can help security researchers and end users understand binary behavior, but current tools suffer from verbose result, poor readability, and limited type recovery. We present NotDec, an advanced WebAssembly decompilation framework. NotDec extends the WebAssembly type checking algorithm to lift bytecode into an SSA‑based IR, applies the inter-procedural type recovery algorithm Retypd with pointer and numeric value differentiation methods to recover complex data structures, and leverages Memory SSA alongside semantics‑preserving structured control‑flow analysis to emit readable, semantically consistent C code. NotDec achieves 100% recompilation success rate on all 5,241 Juliet samples and all Howard dataset programs, significantly outperforming baselines including Ghidra (45.95% success rate). On type recovery accuracy, NotDec recovers 85.33% of struct member accesses in real-world programs, vastly exceeding Ghidra’s 9.24%. While the full inter-procedural version faces scalability challenges on large binaries, the intra-procedural variant NotDec_F demonstrates superior efficiency, consuming less than half of Ghidra’s memory and up to 97% less execution time on unoptimized binaries.

## 47. On Interaction Effects in Greybox Fuzzing

**Authors:** Konstantinos Kitsios (University of Zurich), Marcel Böhme (MPI for Security and Privacy), Alberto Bacchelli (IfI, University of Zurich)

**Categories:** Testing and Analysis

**中文总结:** 研究灰盒模糊测试中变异算子顺序的交互效应，发现顺序显著影响效果，并提出 MuoFuzz，通过学习的条件概率选择更有潜力的变异序列。在 FuzzBench 与 MAGMA 上覆盖率最高，并发现 AFL++ 与 MOPT 遗漏的 bug。

**Abstract:** A greybox fuzzer is an automated software testing tool that generates new test inputs by applying randomly chosen mutators (e.g., flipping a bit or deleting a block of bytes) to a seed input in random order, and adds all coverage-increasing inputs to the corpus of seeds. We hypothesize that the order in which mutators are applied to a seed input has an impact on the effectiveness of greybox fuzzers. In our experiments, we fit a linear model to a dataset that contains the effectiveness of all possible mutator pairs and indeed observe the conjectured interaction effect. This points us to more efficient fuzzing by choosing the most promising mutator sequence with higher likelihood. We propose MuoFuzz, a greybox fuzzer that learns and chooses the most promising mutator sequences. MuoFuzz learns the conditional probability that the next mutator will yield an interesting input given the previously selected mutator. Then, it samples from the learned probability using a random walk to generate mutator sequences. We compare the performance of MuoFuzz to AFL++, which uses a fixed selection probability, and MOPT, which optimizes the selection probability of each mutator in isolation. Experimental results on the FuzzBench and MAGMA benchmarks show that MuoFuzz achieves the highest code coverage, and finds four bugs missed by AFL++ and one missed by both AFL++ and MOPT.

## 48. On the Robustness of Fairness Practices: A Causal Framework for Systematic Evaluation

**Authors:** Verya Monjezi (University of Illinois Chicago), Ashish Kumar (Pennsylvania State University), Ashutosh Trivedi (University of Colorado Boulder), Gang (Gary) Tan (Pennsylvania State University), Saeid Tizpaz-Niari (University of Illinois Chicago)

**Categories:** Testing and Analysis

**中文总结:** 基于因果理论提出评估公平 ML 最佳实践鲁棒性的测试框架，在邻域数据集中检验公平性干预是否仍成立。跨多个公平敏感任务识别出在标签噪声、缺失数据与分布偏移下仍保持鲁棒的建议实践。

**Abstract:** Machine learning (ML) algorithms are increasingly deployed to make critical decisions in socioeconomic applications such as finance, criminal justice, and autonomous driving. However, due to their data-driven and pattern-seeking nature, ML algorithms may develop decision logic that disproportionately distributes opportunities, benefits, resources, or information among different population groups, potentially harming marginalized communities. In response to such fairness concerns, the software engineering and ML communities have made significant efforts to establish the best practices for creating fair ML software. These include fairness interventions for training ML models such as including sensitive features, selecting non-sensitive attributes, and applying bias mitigators. But how reliably can software professionals tasked with developing data-driven systems depend on these recommendations? And how well do these practices generalize in the presence of faulty labels, missing data, or distribution shifts? These questions form the core theme of this paper. We present a testing tool and technique based on causality theory to assess the robustness of best practices in fair ML software development. Given a practice—specified as a first-order logic property—and a socio-critical dataset that satisfies the property, our goal is to search for neighborhood datasets to determine whether the property continues to hold. This process is akin to testing the robustness of a neural network for image classification, except that the “image" is an entire dataset, and its “neighbors" are datasets in which certain causal hypotheses are altered. Since computing neighborhood datasets while accounting for various factors—such as noise, faulty labeling, and demographic shifts—is challenging, we utilize causal graph representations of the dataset and leverage a search algorithm to explore equivalent causal graphs to generate datasets. Our results across various fairness-sensitive tasks, derived from prevalent fairness-sensitive applications, identify best practices that preserve robustness under the varying factors.

## 49. Online and Interactive Bayesian Inference Debugging

**Authors:** Nathanael Nussbaumer (TU Wien), Markus Böck (TU Wien), Jürgen Cito (TU Wien)

**Categories:** Testing and Analysis

**中文总结:** 提出在线交互式贝叶斯推断调试方法及 IDE 内工具，降低概率程序调试所需时间与专业知识门槛。18 名有经验参与者的用户研究显示，该方法显著缩短推断调试任务耗时并降低难度。

**Abstract:** Probabilistic programming is a rapidly developing programming paradigm which enables the formulation of Bayesian models as programs and the automation of posterior inference. It facilitates the development of models and conducting Bayesian inference, which makes these techniques available to practitioners from multiple fields. Nevertheless, probabilistic programming is notoriously difficult as identifying and repairing issues with inference requires a lot of time and deep knowledge. Through this work, we introduce a novel approach to debugging Bayesian inference that reduces time and required knowledge significantly. We discuss several requirements a Bayesian inference debugging framework has to fulfill, and propose a new tool that meets these key requirements directly within the development environment. We evaluate our results in a study with 18 experienced participants and show that our approach to online and interactive debugging of Bayesian inference significantly reduces time and difficulty on inference debugging tasks.

## 50. Optimization-Aware Test Generation for Deep Learning Compilers

**Authors:** Qingchao Shen (Tianjin University), Zan Wang (Tianjin University), Haoyang Ma (Hong Kong University of Science and Technology), Yongqiang Tian (Monash University), Lili Huang (College of Intelligence and Computing, Tianjin University), Zibo Xiao (College of Intelligence and Computing, Tianjin University), Junjie Chen (Tianjin University), Shing-Chi Cheung (Hong Kong University of Science and Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出面向深度学习编译器的优化感知测试生成方法 OATest，从文档测试中提取模式并嵌入匹配的计算图结构以触发特定优化。在 TVM 与 ONNXRuntime 上发现 56 个未知 bug，其中 42 个已获确认。

**Abstract:** Deep Learning (DL) compilers have been widely utilized to optimize DL models for efficient deployment across various hardware. Due to their vital role in the DL ecosystem, ensuring their reliability is critical. Such model optimizations are often designed to match specific computational graph structures of a model. However, existing DL compiler fuzzing techniques do not generate tests for each optimization aware of its matched graph structures. In this paper, we proposed OATest, a novel technique that synthesizes optimization-aware tests by extracting patterns from documented tests and integrating them into diverse computational graph contexts. To address the key technical challenge of synthesizing valid and optimization-aware computational graphs, OATest introduces two synthesis strategies: (1) reusing compatible inputs/outputs from existing nodes and (2) creating new nodes with compatible inputs/outputs, establishing effective connections between patterns and contexts. OATest is evaluated on two popular DL compilers, TVM and ONNXRuntime, regarding the bugs revealed by crashes and inconsistencies. The experimental results show that OATest significantly outperforms the state-of-the-art DL compiler fuzzing techniques by detecting more bugs and covering more optimization code in TVM and ONNXRuntime. Particularly, OATest uncovers 56 previously unknown bugs, 42/24 of which have been confirmed/fixed by developers.

## 51. Parse this! Summoning Context-Sensitive Inputs with Goblin

**Authors:** Robert Lorch (The University of Iowa), Muhammad Daniyal Pirwani Dar (Stony Brook University), Cesare Tinelli (University of Iowa), Omar Chowdhury (Stony Brook University)

**Categories:** Testing and Analysis

**中文总结:** 提出上下文敏感输入生成语言与工具 Goblin，在 CFG 上标注语义约束并支持任意 SMT 理论求解，保证解的 soundness 与 completeness。集成到协议模糊器后验证了其在复杂约束输入生成上的有效性。

**Abstract:** Grammar-based fuzzers have shown immense promise in identifying bugs in software systems that have highly-structured and intricate input formats (\eg, XML). Many of the existing grammar-based fuzzers rely on context-free grammars (CFGs) to represent the target’s input structure. CFGs, however, are often insufficient to precisely capture many application input formats containing context-sensitive constraints. Application-specific fuzzers, albeit effective, lack generality to be adapted to new applications. In this paper, we present Goblin, a new input generation language and tool that helps bridge this gap. Given a context-free grammar annotated with semantic constraints, Goblin generates inputs that both conform to the grammar and satisfy the constraints. While a few prior techniques target this problem, our method is distinguished by: $(i)$ support for constraint solving over arbitrary SMT theories (e.g., bitvectors, integers, strings); $(ii)$ a minimal core input language with formal semantics that is smaller and less complex than prior work; and $(iii)$ a shift from global constraints to local, production rule constraints, which enables easier integration with certain fuzzing workflows. Goblin’s input generation approach is inspired by DPLL-style SAT solvers and enjoys the following formal guarantees: \emph{solution soundness}, \emph{solution completeness}, and \emph{refutation soundness}. In addition to comparing Goblin with prior work, we demonstrate its effectiveness by incorporating it into a grammar-based network protocol fuzzer.

## 52. Precise Static Identification of Ethereum Storage Variables

**Authors:** Sifis Lagouvardos (University of Athens), Yannis Bollanos (Dedaub), Michael Debono (Friendly Maltese Citizens), Neville Grech (Dedaub Limited), Yannis Smaragdakis (University of Athens)

**Categories:** Testing and Analysis

**中文总结:** 提出精确静态分析以从已部署 EVM 字节码识别链上 storage 数据结构，处理 mapping/array 等动态布局。相较 SOTA 工具精度 95.70%、召回至少 94.96%，且常比编译器自身 storage 描述更完整。

**Abstract:** Smart contracts are small programs that run autonomously on the blockchain, using it as their persistent memory. The predominant platform for smart contracts is the Ethereum VM (EVM). In EVM smart contracts, a problem with significant applications is to identify data structures (in blockchain state, a.k.a. ``storage''), given only the deployed smart contract code. The problem has been highly challenging and has often been considered nearly impossible to address satisfactorily. (For reference, the latest state-of-the-art research tool fails to recover nearly all complex data structures and scales to 50% of contracts.) Much of the complication is that the main on-chain data structures (mappings and arrays) have their locations derived dynamically through code execution. We propose sophisticated static analysis techniques to solve the identification of on-chain data structures with extremely high fidelity and completeness. Our analysis scales nearly universally and recovers deep data structures. Our techniques are able to identify the exact types of data structures with 95.70% precision and at least 94.96% recall, compared to a state-of-the-art tool managing 83.30% and 55.65% respectively. Strikingly, the analysis is often more complete than the storage description that the compiler itself produces, with full access to the source code.

## 53. Predicting Failures in Smart Human-Centric EcoSystems

**Authors:** Niccolò Puccinelli (Università della Svizzera Italiana), Davide Molinelli (Constructor Institute of Technology), Noura El Moussa (USI Lugano; Schaffhausen Institute of Technology), Matteo Ciniselli (Università della Svizzera Italiana), Mauro Pezze (Università della Svizzera italiana (USI) and Università degli Studi di Milano Bicocca)

**Categories:** Testing and Analysis

**中文总结:** 定义智能以人为中心生态系统（SHE）失败问题，提出 SEM 方法，用去噪自编码器与 Transformer 基于指标重构误差预测即将发生的系统级失败。旧金山拼车生态实验表明 SEM 可提前预警并支持持续学习泛化。

**Abstract:** Smart cities, smart grids, and in general Smart Human-centric Ecosystems (SHEs) emerge from the co-existence of many systems that operate according to independently owned specifications, and evolve over time. SHEs may fail despite the correct behavior of the systems that comprise the SHE. Fully testing SHEs on testbed to prevent failures in production is impossible, and scenarios that may lead to catastrophic SHE failures are unavoidable. In this paper we frame the core issues of SHE failures, and propose Smart human-centric Ecosystem Monitoring, SEM, an approach that predicts SHE failures to enable corrective actions for mitigating the catastrophic effects of failures. SEM identifies failure-prone scenarios from the reconstruction error of SHE indicators, that is, metric values that SEM collects from the SHE at constant frequency. SEM computes the reconstruction error with a suitably trained denoising autoencoder combined with a Transformer architecture. The results of experimenting with a peer-to-peer ride-sharing ecosystem operating in San Francisco confirm that SEM can effectively predict SHE failures early enough to activate preventing actions, and indicate the generalizability of SEM with continual learning. The main contributions of the paper are the definition and the exemplification of the impact of failures in SHEs, and an approach to detect incoming failures before otherwise inevitable disruptive effects.

## 54. PTV: Scalable Version Detection of Web Libraries and its Security Application

**Authors:** Xinyue Liu (Chongqing University), Haipeng Cai (University at Buffalo, SUNY), Lukasz Ziarek (University at Buffalo)

**Categories:** Testing and Analysis

**中文总结:** 提出 Web 库版本检测算法 PTV，从树森林中提取各版本最独特结构以压缩特征 footprint。在 556 库 30810 版本上空间需求最高降 99%，并在 200 个高流量网站检测到 190 个漏洞。

**Abstract:** Identifying the libraries used by a web application is an important task for sales intelligence, website profiling, and web security analysis. Recent work uses tree structures to represent the property relationships of the library at runtime, realizing automatic library identification without pinpointing versions. But when assessing the security risks associated with these web libraries or conducting fine-grained software analysis, it becomes essential to determine the specific version of the library in use. However, existing tree-based methods are not directly applicable to version detection due to the huge storage requirements for maintaining separate trees for a large number of versions. This paper proposes a novel algorithm to find the most unique structure out of each tree in a forest so that the footprint of the features can be greatly minimized. We implement this algorithm into a web library detection tool. Experimental evaluations on 556 web libraries, encompassing 30,810 versions, reveal that our tool reduces space requirements by up to 99%, achieves more precise version detection compared to existing tools, and detects 190 vulnerabilities on 200 top-traffic websites.

## 55. PyXray: Practical Cross-Language Call Graph Construction through Object Layout Analysis

**Authors:** Georgios Alexopoulos (University of Athens), Thodoris Sotiropoulos (ETH Zurich), Georgios Gousios (Endor Labs), Zhendong Su (ETH Zurich), Dimitris Mitropoulos (University of Athens)

**Categories:** Testing and Analysis

**中文总结:** 提出 PyXray，通过分析 Python 可调用对象内存布局中的原生函数指针动态构建跨语言调用图，无需执行输入。可在数分钟内分析 NumPy/PyTorch 等大型包，精度与召回显著优于静态分析，支持跨语言漏洞与膨胀分析。

**Abstract:** A great number of software packages combine code in high-level languages, such as Python, with binary extensions compiled from low-level languages such as C, C++ or Rust to either boost efficiency or enable specific functionalities. In this context, high-level function calls can trigger native (binary) code execution. This setup introduces challenges for call graph generation. Accurate call graphs are essential for various applications, including vulnerability management and software maintenance, as they help track execution paths, assess security risks, and identify unused or redundant code. This work tackles the problem of cross-language call graph construction in Python. Instead of relying on static analysis, which struggles with identifying Python-native interactions, we propose a dynamic analysis technique which does not require inputs to execute code. Our approach is based on two key insights: (1) when a binary extension is imported from Python code, all its objects (e.g., functions) are loaded into memory, and (2) the layout of callable Python objects contains pointers to the native functions they invoke. By analyzing these memory layouts for every loaded object, we identify corresponding graph edges, which link Python functions to the native functions they eventually invoke. This is an essential element for constructing call graphs across language boundaries. We implement this approach in PyXray, a tool that efficiently analyzes massive Python packages such as NumPy and PyTorch in minutes, while significantly outpeforming existing static analysis methods in terms of precision and recall. PyXray enables two key applications: (1) cross-language vulnerability management, by identifying whether a Python package potentially calls a vulnerable native function and (2) cross-language bloat analysis, by quantifying unnecessary code across Python and native components.

## 56. Repair Ingredients Are All You Need: Improving Large Language Model-Based Program Repair via Repair Ingredients Search

**Authors:** Jiayi Zhang (Nanyang Technological University), Kevin Huang, Jian Zhang (Beihang University), Yang Liu (Nanyang Technological University), Chunyang Chen (TU Munich)

**Categories:** Testing and Analysis

**中文总结:** 提出 agent 框架 ReinFix，在推理与修复阶段自主搜索内部（变量定义等）与外部（历史相似修复）repair ingredients。Defects4J V1.2 修复 146 个 bug，比 SOTA 多 32 个，在无泄露风险的新 benchmark 上仍最佳。

**Abstract:** Automated Program Repair (APR) that aims to automatically fix buggy programs has attracted much attention and blooms various kinds of techniques. Among these, Large Language Model-based (LLM-based) approaches have shown great promise. Recent advances demonstrate that directly leveraging LLMs (e.g., ChatGPT) without reliance on training data can achieve leading results. However, these techniques remain suboptimal in generating contextually relevant and accurate patches, as they often overlook repair ingredients crucial for practical program repair. In this paper, we propose ReinFix, a novel agent-based framework that enables LLMs to autonomously search for repair ingredients throughout both the reasoning and solution phases of bug fixing. In the reasoning phase, ReinFix integrates static analysis tools to retrieve internal ingredients, such as variable definitions, to assist the LLM in root cause analysis when it encounters difficulty understanding the context. During the solution phase, when the LLM lacks experience in fixing specific bugs, ReinFix searches for external ingredients from historical bug fixes with similar bug patterns, leveraging both the buggy code and its root cause to guide the LLM in identifying appropriate repair actions, thereby increasing the likelihood of generating correct patches. Evaluations on two popular benchmarks (Defects4J V1.2 and V2.0) demonstrate the effectiveness of our approach over SOTA baselines. Notably, ReinFix fixes 146 bugs, which is 32 more than the baselines on Defects4J V1.2. On Defects4J V2.0, ReinFix fixes 38 more bugs than the SOTA. Importantly, when evaluating on the new benchmarks that are free of data leakage risk, ReinFix also maintains the best performance.

## 57. RusyFuzz: Unhandled Exception Guided Fuzzing for Rust OS Kernel

**Authors:** Yuwei Liu (Ant Group), Yanhao Wang (Independent Researcher), Minghua Wang (Ant Group), Lin Huang (Ant Group), Purui Su (Institute of Software/CAS China), Tao Wei (Ant Group)

**Categories:** Testing and Analysis

**中文总结:** 提出面向 Rust OS 内核的 RusyFuzz，基于 MIR 中编译器插入断言做未处理异常引导的模糊测试，并用轻量日志插桩替代 KCOV。在 Asterinas、Redox、RuxOS 上发现 70 个已确认漏洞，bug 数约为 Trinity 两倍、覆盖率提升 14.4%。

**Abstract:** Rust’s strong type system and ownership model eliminate many traditional memory safety issues in OS kernels. However, logic errors—such as unchecked indexing and failed unwrap operations—can still cause panic!s that crash the entire system. Existing kernel fuzzers, designed primarily for C-based kernels and reliant on KCOV, treat all crashes uniformly and fail to account for Rust-specific failure modes. We present RusyFuzz, the first fuzzing framework tailored to Rust OS kernels that explicitly targets panic-prone code paths using an unhandled-exception-guided strategy. RusyFuzz analyzes the compiler-inserted assertions within the Rust MIR, performs backward slicing to link these assertions to system call arguments, and uses constraint solving to synthesize inputs that trigger panics. In the absence of built-in coverage support, RusyFuzz employs a lightweight, log-based instrumentation method to enable coverage-guided fuzzing. We evaluate RusyFuzz on three emerging Rust-based kernels: Asterinas, Redox OS, and RuxOS. RusyFuzz discovers 70 previously unknown and developer-confirmed vulnerabilities. Compared to Trinity, it uncovers over twice as many bugs while improving line coverage by 14.4%. These results demonstrate that unhandled-exception-guided fuzzing is critical for uncovering logic bugs and enhancing the reliability of Rust OS kernels, providing the first systematic methodology for detecting such vulnerabilities.

## 58. SAFE: Harnessing LLM for Scenario-Driven ADS Testing from Multimodal Crash Data

**Authors:** Siwei Luo (Macquarie University), Yang Zhang, Yao Deng (Macquarie University), Linfeng Liang (Macquarie University), Xi Zheng (Macquarie University)

**Categories:** Testing and Analysis

**中文总结:** 提出 SAFE 框架，结合 RAG、CoT 与自验证从多模态事故报告重建 ADS 测试场景。路网/参与者/环境提取准确率分别达 93.8%、80%、100%，在相同 ADS 设置下比 LCTGen/AC3R 多检出 39/71 个安全违规。

**Abstract:** Ensuring the safety of Autonomous Driving Systems (ADS) requires realistic and reproducible test scenarios, yet extracting such scenarios from multimodal crash reports remains a major challenge. Large Language Models (LLMs) often hallucinate and lose map structure, resulting in unrealistic road layouts and vehicle behaviors. To address this, we introduce SAFE, a novel Scenario-based ADS testing Framework via multimodal Extraction, which leverages Retrieval-Augmented Generation (RAG), knowledge-grounded prompting, Chain-of-Thought (CoT) reasoning, and self-validation to improve scenario reconstruction from multimodal crash data. SAFE achieves 93.8% accuracy in extracting road network details, 80.0% for actor information, and 100% for environmental context. In human studies, SAFE outperforms LCTGen and AC3R in reconstructing consistent road networks and vehicle behaviors. Under identical ADS and simulator settings, SAFE detects 39 and 71 more safety violations than LCTGen and AC3R, respectively, and reproduces 12 more real world crash cases than LCTGen. On 19 cases supported by AC3R, SAFE reproduces one additional crash case with statistically significant gains across five runs. It generates scenarios within 25 seconds and triggers violations after just 1 case (IDM), 3 cases (PPO), and 1 case (BeamNG). Unlike AC3R, SAFE is ontology-free and generalizes to a broader range of crash scenarios. Code: https://anonymous.4open.science/r/SAFE-8404/README.md

## 59. Scalpel: Automotive Deep Learning Framework Testing via Assembling Model Components

**Authors:** Yinglong Zou (Nanjing University), Juan Zhai (University of Massachusetts at Amherst), Chunrong Fang (Nanjing University), An Guo (The Hong Kong Polytechnic Universituy), Jiawei Liu (State Key Laboratory for Novel Software Technology, Nanjing University, China), Zhenyu Chen (Nanjing University)

**Categories:** Testing and Analysis

**中文总结:** 提出 Scalpel，在自动驾驶 DL 框架测试中通过组装 head/neck/backbone 等模型组件生成满足多输入/多模态/多级特征需求的测试模型。在 Apollo 发现 16  crash 与 21 个 NaN/不一致 bug，生成与检 bug 效率分别提升 27.44× 与 8.5×。

**Abstract:** Deep learning (DL) plays a key role in autonomous driving systems. DL models support perception modules, equipped with tasks such as object detection and sensor fusion. These DL models en- able vehicles to process multi-sensor inputs to understand complex surroundings. Deploying DL models in autonomous driving systems faces stringent challenges, including real-time processing, limited computational resources, and strict power constraints. To address these challenges, automotive DL frameworks (e.g., PaddleInference) have emerged to optimize inference efficiency. However, these frameworks encounter unique quality issues due to their more complex deployment environments, such as crashes stemming from limited scheduled memory and incorrect memory allocation. Unfortunately, existing DL framework testing methods fail to detect these quality issues due to the failure in deploying generated test input models, as these models lack three essential capabilities: (1) multi-input/output tensor processing, (2) multi-modal data processing, and (3) multi-level data feature extraction. These capabilities necessitate specialized model components, which existing testing methods neglect during model generation. To bridge this gap, we propose Scalpel, an automotive DL frameworks testing method that generates test input models at the model component level. Scalpel generates models by assembling model components (heads, necks, backbones) to support capabilities required by autonomous driving systems. Specifically, Scalpel maintains and updates a repository of model components, generating test inputs by selecting, mutating, and assembling them. Successfully generated models are added back to enrich the repository. Newly generated models are then deployed within the autonomous driving system to test automotive DL frameworks via differential testing. The experimental results demonstrate that Scalpel outperforms existing methods in both effectiveness and efficiency. In Apollo, Scalpel detects 16 crashes and 21 NaN & inconsistency bugs. All detected bugs have been reported to open-source communities, with 10 crashes confirmed. Scalpel achieves 27.44$\times$ and 8.5$\times$ improvements in model generation efficiency and bug detection efficiency. Additionally, Scalpel detects nine crashes and 16 NaN & inconsistency bugs in Autoware, which shows its excellent generalization.

## 60. StorFuzz: Using Data Diversity to Overcome Fuzzing Plateaus

**Authors:** Leon Weiß (Ruhr University Bochum), Tobias Holl (Ruhr University Bochum), Kevin Borgolte (Ruhr University Bochum)

**Categories:** Testing and Analysis

**中文总结:** 提出 StorFuzz，通过自动插桩 memory store 捕获“数据覆盖”以突破仅依赖控制流覆盖的 fuzzing 平台期，多样化饱和 corpus 引导探索。在 OSS-Fuzz 长期 campaign 上为 7 个项目发现 50 个新 bug，其中部分存在 14 年。

**Abstract:** Fuzzing is widely used to discover software bugs and vulnerabilities. Unfortunately, real-world long-running fuzzing campaigns often plateau and no progress can be made anymore, leaving code areas untested. State-of-the-art fuzzers leverage code coverage to measure progress and reach new areas, but this is insufficient to capture all program behavior, as code coverage may be the same for different behavior, thus preventing progress and masking bugs. In this paper, we introduce StorFuzz, a novel technique to overcome fuzzing plateaus and improve on code coverage by leveraging our new data coverage. StorFuzz automatically identifies and instruments memory stores to capture changes in program behavior invisible to control flow, which it uses to diversify the saturated corpora of plateaued campaigns. StorFuzz leverages this diversified corpus of test cases that changed internal states to improve navigation of the input space, which also enables conventional fuzzers to improve their code coverage. We implement StorFuzz in LibAFL and evaluate on FuzzBench, starting from a corpus, which is saturated by multimonth OSS-Fuzz fuzzing campaigns and LibAFL. We show that StorFuzz successfully generates new coverage for plateauing campaigns of widely-used and well-fuzzed software, leading to the discovery of 50 new bugs in 7 OSS-Fuzz projects, like VLC and PHP, with some bugs having been present in the code for 14 years . Our approach significantly outperforms both the state-of-the-art fuzzer LibAFL and data-guided fuzzer DDFuzz in 11 of 23 FuzzBench benchmarks, while performing equally on all others. StorFuzz is also complementary to WingFuzz, an approach guided by static data, as both fuzzers cover distinct code regions. We make StorFuzz and our artifacts available as open source to aid reproducibility and allow easy reuse by future work.

## 61. SymRadar: PoC-Centered Bounded Verification for Vulnerability Repair

**Authors:** Seungheon Han (UNIST), YoungJae Kim (UNIST), Yeseung Lee (UNIST), Jooyong Yi (UNIST)

**Categories:** Testing and Analysis

**中文总结:** 提出 SymRadar，在 PoC 附近对补丁函数做欠约束符号执行并支持多补丁批量验证，比现有 AVR 补丁验证方法更有效且高效。

**Abstract:** In this paper, we tackle the problem of patch verification. While automated vulnerability repair (AVR) techniques are gaining traction, it is not sufficient to merely generate patches; providing evidence of their correctness is also essential. However, the current state-of-the-art patch verification methods are not sufficiently effective. To address this issue, we propose SymRadar, a patch verification tool that performs under-constrained symbolic execution (UC-SE) on the patched function. Unlike standard UC-SE, SymRadar conducts UC-SE in the vicinity of the crash-inducing input. We demonstrate that SymRadar is more effective than existing patch verification methods. Another challenge in verifying patches generated by AVR tools is the large number of patches generated. To address this, we propose a novel optimization technique that allows SymRadar to handle multiple patches efficiently. Our experimental evaluation demonstrates that SymRadar is both effective and efficient in verifying patches generated by AVR tools.

## 62. TARIPlay: A Test Framework for AR Applications based on Interactive Area Detection in Playback Videos

**Authors:** Seyed Amir Mousavi (PhD Student at University of Texas at San Antonio), Xiaoyin Wang (University of Texas at San Antonio)

**Categories:** Testing and Analysis

**中文总结:** 提出 AR 测试框架 TARIPlay，从回放视频中检测、跟踪并筛选可交互区域以驱动自动化测试，分支覆盖率显著高于 Monkey（55.8% vs 41.98%）。

**Abstract:** As Augmented Reality (AR) becomes more and more embedded in daily life, ensuring the quality, safety, and reliability of AR applications is increasingly important. However, AR apps present unique challenges for automated testing. Unlike static GUI layouts in traditional mobile apps, AR apps acquire their interaction interface from the surrounding environment, which is volatile and non-deterministic. Recent advancements like ARCore Playback and ARKit Replay allow developers to reuse real-world scenarios by recording and playing back enriched videos, enabling more feasible automated AR testing. However, using playback videos introduces two major challenges: test inputs must be timed precisely, and interactive areas in the video are dynamic, irregular, and difficult to identify. To address these challenges, we propose TARIPlay, a framework that analyzes playback videos to detect, track, and filter proper interactive areas over time for automated testing. In particular, TARIPlay identifies viable test opportunities based on criteria like stability and visibility, then feeds this information to an automated testing engine to simulate user interactions. We perform an experiment with four open-source AR apps and nine playback videos. Evaluation results show that TARIPlay significantly outperforms the existing tool Monkey in test coverage (55.8% over 41.98% on branch coverage) of AR-related code, and can also be used to assess the quality of playback videos for testing suitability.

## 63. Temporal Specification Oriented Fuzzing for Trigger-Action-Programming Smart Home Integrations

**Authors:** Jinglin Dai (Nanjing University), Yifan Xiong (Nanjing University), Lezhi Ma (Nanjing University), Shangqing Liu (Nanjing University), Lei Bu (Nanjing University)

**Categories:** Testing and Analysis

**中文总结:** 提出 HAFuzz，将 LTL 时序规范与自适应 fuzzing 结合检测智能家居 IFTTT 类集成违规，典型场景下约 50ms 内发现违规并验证 3343 条规范。

**Abstract:** The convergence of Internet of Things (IoT) and Home Automation (HA) has revolutionized human-device interaction, typically through Trigger-Action Programming paradigms such as If This Then That (IFTTT). While empowering user-customized automation, this integration introduces critical challenges: unexpected behaviors from improper rule configurations, and cybersecurity threats propagated through interconnected rule chains. Although existing research demonstrates that linear temporal logic (LTL) specifications can formally characterize these risks for model checking verification, conventional methodologies suffer from two fundamental limitations: the inherent state space explosion problem constraining efficiency, and restricted expressiveness of model patterns hindering scalability. Furthermore, the HA-IoT domain notably lacks standardized benchmark datasets for validating LTL-related methods. To address these critical gaps, we propose HAFuzz - an innovative framework that synergizes formal modeling with adaptive fuzzing techniques for efficient temporal specification violation detection. We further incorporate manually curated specifications with large language model (LLM)-driven mutation generation, enabling systematic test case augmentation. Experimental evaluations demonstrate HAFuzz achieves violation detection within 50ms per integration under typical scenarios, showing superior efficiency improvement compared with conventional model checking approaches. Comprehensive validation involving 3,343 LTL specifications confirms HAFuzz’s accuracy and effectiveness in identifying critical violations, particularly in large-scale deployments characterized by intricate rule interdependencies and specifications that feature complex temporal logic patterns.

## 64. Test Flimsiness: Characterizing Flakiness Induced by Mutation to the Code Under Test

**Authors:** Owain Parry (University of Sheffield), Gregory Kapfhammer (Allegheny College), Michael Hilton (Carnegie Mellon University), Phil McMinn (University of Sheffield)

**Categories:** Testing and Analysis

**中文总结:** 首次系统刻画“flimsiness”（对被测代码变异诱发的测试不稳定），在 28 个 Python 项目中 54% 出现该现象，结合变异可发现远多于单纯重跑的 flaky 测试。

**Abstract:** Flaky tests, those that fail non-deterministically against the same version of code, pose a well-established challenge to software developers. In this paper, we characterize the overlooked phenomenon of test \textbf{FLIM}siness: \textbf{FL}akiness \textbf{I}nduced by \textbf{M}utations to the code under test. These mutations are generated by the same operators found in out-of-the-box mutation testing tools. Flimsiness has profound implications for researchers in software testing. While previous work analyzed the impact of pre-existing flaky tests on mutation testing, we reveal that mutations themselves can induce flakiness, exposing a previously neglected threat. This has impacts beyond mutation testing, calling into question the reliability of any technique that relies on deterministic test outcomes in response to mutations. On the other hand, flimsiness also presents an opportunity to surface potential flakiness that may otherwise remain hidden. Where prior work has perturbed the execution environment to augment rerunning or the test code to support benchmarking, our work advances these efforts by perturbing a third major source of flakiness: the code under test. We conducted an empirical study on over half a million test suite executions across 28 diverse Python projects. Our robust statistical analysis on more than 30 million mutant-test pairs unveiled flimsiness in 54% of projects, highlighting its prevalence. We found that augmenting the standard rerunning flaky test detection strategy with mutations to the code under test detects a substantially larger number of flaky tests (median 740 vs. 163) and uncovers many that the standard strategy is unlikely to detect.

## 65. TestifAI: Tomography-Based Testing for Deep Learning Systems

**Authors:** Arooj Arif (Northeastern University London), Tobias Hartung (Northeastern University London), Elena Botoeva (University of Kent), Alexandros Koliousis (Northeastern University London)

**Categories:** Testing and Analysis

**中文总结:** 提出 TestifAI，用部分模型断层扫描从低阶扰动测试结果重建高阶组合扰动下的鲁棒性，误差低于 7% 且推理次数减少 60–80%。

**Abstract:** As AI systems are increasingly deployed in safety-critical applica- tion domains (e.g., autonomous driving), associated risks increase too. Deep learning models underlying modern AI systems, therefore, must undergo thorough testing to ensure their correct behaviour. A single robustness test involves thousands of inferences to empir- ically verify if a model’s outputs remain stable under a bounded perturbation of its inputs. However, existing testing frameworks lack the means to systematically explore and summarise robustness across a combinatorial space of perturbations. We propose TestifAI, a deep learning testing framework for ef- ficient and accurate estimation of robustness against combinations of perturbations. TestifAI enables users to specify the operational conditions of an AI system as structured spaces of semantic input perturbations (e.g., image blur, brightness and zoom) and their dis- crete severity levels (e.g., low, medium and high). Within this space, users can query model robustness for any combination (e.g., “low blur, high brightness, and medium zoom”). To achieve efficiency and accuracy, TestifAI introduces partial model tomography, a novel ap- proach to reconstructing model behaviour in a multi-perturbation space from tests that apply only a small number of perturbations (lower-order projections). Namely, to estimate robustness against at least three perturbations, TestifAI trains an auxiliary model on the results of tests involving up to two perturbations only, hence avoid- ing execution of an exponential number of tests. Our experiments on five image and language classification tasks show that TestifAI can predict higher-order (3 and 4 perturbations) test outcomes from low-order (1 and 2 perturbations) observations with an aggregate robustness estimation error of less than 7%, while reducing the number of inferences by 60–80%.

## 66. Testing Deep Learning Libraries via Neurosymbolic Constraint Learning

**Authors:** M M Abid Naziri (North Carolina State University), Shinhae Kim (Cornell University), Feiran Qin (North Carolina State University), Saikat Dutta (Cornell University), Marcelo d'Amorim (North Carolina State University)

**Categories:** Testing and Analysis

**中文总结:** 提出神经符号方法 Centaur，动态学习 DL 库 API 输入约束并用 SMT 生成合法测试输入，在 PyTorch/TensorFlow 上覆盖更多分支并发现 23 个新 bug。

**Abstract:** Deep Learning (DL) libraries (e.g., Pytorch) are popular in the development of AI applications. These libraries are complex and contain bugs. Researchers have proposed various bug-finding techniques for such libraries. Yet, there is much room for improvement. A key challenge in testing DL libraries is the lack of API specifications. Prior testing approaches often inaccurately model the input specifications of DL APIs, resulting in missing valid inputs that could reveal bugs or false alarms from invalid inputs. To address this challenge, we develop Centaur - the first neurosymbolic technique to test DL library APIs using dynamically learned input constraints. Centaur leverages the key idea that formal API constraints can be learned from a small number of seed inputs, and that the learned constraints can be solved using SMT solvers to generate valid and diverse test inputs for the API. We develop a novel grammar that represents first-order logic formulae over API parameters and expresses tensor-related properties (e.g., shape, data type, etc.) as well as relational properties between parameters. We use the grammar to guide a Large Language Model (LLM) to enumerate syntactically correct candidate rules, which are then validated using valid inputs. Further, we develop a custom refinement strategy to prune the set of learned rules to eliminate spurious or redundant rules. The learned constraints are then used to systematically generate valid and diverse inputs for the API by SMT solving (such as Z3) and a specialized sampling technique. We evaluate Centaur for testing PyTorch and TensorFlow. Our results show that Centaur generates constraints more accurately compared to prior approaches, namely DocTer and ACETest. In terms of coverage, Centaur covers 203, 149, and 9608 more branches than TitanFuzz, ACETest and Pathfinder, respectively. Using Centaur, we also detect 23 new bugs in PyTorch and TensorFlow, out of which 11 are already confirmed.

## 67. Testora: Using Natural Language Intent to Detect Behavioral Regressions

**Authors:** Michael Pradel (CISPA Helmholtz Center for Information Security)

**Categories:** Testing and Analysis

**中文总结:** 提出 Testora，用 LLM 生成测试并借 PR 自然语言信息区分预期与非预期行为差异，在 Python 项目中发现 19 个回归 bug 且单 PR 成本约 $0.003。

**Abstract:** As software is evolving, code changes can introduce regression bugs or affect the behavior in other unintended ways. Traditional regression test generation is impractical for detecting unintended behavioral changes, because it reports all behavioral differences as potential regressions. However, most code changes are intended to change the behavior in some way, e.g., to fix a bug or to add a new feature. This paper presents Testora, an automated approach that detects regressions by comparing the intentions of a code change against behavioral differences caused by the code change. Given a pull request (PR), Testora queries an LLM to generate tests that exercise the modified code, compares the behavior of the original and modified code, and classifies any behavioral differences as intended or unintended. For the classification, we present an LLM-based technique that leverages the natural language information associated with the PR, such as the title, description, and commit messages – effectively providing a natural language oracle for regression testing. Applying Testora to PRs of complex and popular Python projects, we find 19 regression bugs and 11 PRs that, despite having another intention, coincidentally fix a bug. Out of 13 regressions reported to the developers, 10 have been confirmed and 8 have already been fixed. The costs of using Testora are acceptable for real-world deployment, with 12.3 minutes to check a PR and LLM costs of only $0.003 per PR. We envision our approach to be used before or shortly after a code change gets merged into a code base, providing a way to early on detect regressions that are not caught by traditional approaches.

## 68. Think Outside the Box: Automating Inter-App Functionality Testing via Memory Implanting and Reasoning

**Authors:** Mengzhuo Chen (Institute of Software, Chinese Academy of Sciences), Zhe Liu (Institute of Software, Chinese Academy of Sciences), Chunyang Chen (TU Munich), Junjie Wang (Institute of Software at Chinese Academy of Sciences), Yangguang Xue (University of Chinese Academy of Sciences), Boyu Wu (Institute of Software at Chinese Academy of Sciences), Libin Wu (Institute of Software Chinese Academy of Sciences), Qing Wang (Institute of Software at Chinese Academy of Sciences)

**Categories:** Testing and Analysis

**中文总结:** 提出 InterDroid，通过多模态检索与全局/局部记忆植入增强 LLM 跨应用 GUI 测试，在 100 个跨应用功能上覆盖与准确率大幅提升并发现 43 个新崩溃。

**Abstract:** Inter-app functionality requires multiple apps to collaborate to complete a functional task, which has become essential in modern software ecosystems. However, due to the dynamic updates and openness of modern apps, automated GUI testing based on predefined interaction models or trained on historical data is difficult to achieve inter-app testing. The low fault tolerance and context-dependent characteristics of inter-app functionality paths, lead the LLM-based GUI testing to have UI semantic mapping ambiguity and irreversible operation generating problem. To address these challenges, this paper proposes InterDroid, an automated GUI testing approach that enhances inter-app testing by implanting structured semantic knowledge into LLM’s memory. InterDroid retrieves relevant historical inter-app interactions using a multimodal retrieval method that integrates visual and textual GUI information, significantly improving retrieval accuracy. Inspired by the research on memory implantation in cognitive psychology, we design a memory implanting mechanism: global memory presents inter-app paths in a conversational form, simulating prior testing experience, and local memory tracks real-time state transitions. Additionally, InterDroid proposes a testing monitor that dynamically tracks testing progress and detects deviations, ensuring comprehensive test execution. InterDroid is designed as an integrable module that activates upon detecting the transition of the app to another app, allowing existing automated GUI testing tools to continue seamlessly after inter-app testing is completed. We evaluate InterDroid on 100 inter-app functionalities across 63 apps, comparing it with state-of-the-art GUI testing baselines. InterDroid achieves up to 133% improvement in page coverage, 124% in action coverage, and 268% in exact match accuracy over the best baseline. Furthermore, InterDroid detects 43 new crash bugs in real-world apps from Google Play, with 31 fixed and 12 confirmed by developers, demonstrating InterDroid’s effectiveness.

## 69. Uncovering Failures in Cyber-Physical System State Transitions: A Fuzzing-Based Approach Applied to sUAS

**Authors:** Theodore Chambers (University of Notre Dame), Arturo Miguel Russell Bernal (University of Notre Dame), Michael Vierhauser (University of Innsbruck), Jane Cleland-Huang (University of Notre Dame)

**Categories:** Testing and Analysis

**中文总结:** 提出 SAFUS fuzzing 流水线验证小型无人机状态转换与失效保护，在仿真与实机测试中均发现开发团队此前未检出的失败点并生成故障树。

**Abstract:** The increasing deployment of small Uncrewed Aerial Systems (sUAS) in diverse and often safety-critical environments demands rigorous validation of onboard decision logic under various conditions. In this paper, we present SAFUS, a fuzzing pipeline that validates core behavior associated with state transitions, automated failsafes, and human operator interactions in sUAS applications operating under various timing conditions and environmental disturbances. We create fuzzing scenarios to detect behavioral deviations, and then dynamically generate associated Fault Trees to visualize states, modes, and environmental factors that contribute to the failure, thereby helping project stakeholders to analyze the failure and identify its root causes. We validated SAFUS against a real-world sUAS system and were able to identify several points of failure not previously detected by the system’s development team. The fuzzing was conducted in a high-fidelity simulation environment, and outcomes were validated on physical sUAS in a real-world field testing setting. The findings from the study demonstrated SAFUS’ ability to uncover diverse state transition failures, and to provide a practical and scalable solution for detecting a broad range of state-related failures in an sUAS application.

## 70. Validating Mixed-Integer Programming Solvers

**Authors:** Xintong Zhou (University of Waterloo), Zhenyang Xu (University of Waterloo), Chengnian Sun (University of Waterloo)

**Categories:** Testing and Analysis

**中文总结:** 提出 Flip，用可行性驱动实例生成系统验证混合整数规划求解器，在 5 个主流求解器中发现 52 个已确认 bug（39 个已修复）。

**Abstract:** Mixed-integer programming (MIP) is a fundamental class of mathematical optimization problems with broad applications in various domains such as finance, engineering, and management science. MIP solvers, software systems that automatically solve MIP problems, serve as the computational backbone for these applications. Given their widespread use, ensuring the correctness of MIP solvers is crucial, as incorrect results—such as falsely determining feasibility or returning incorrect solutions—can lead to serious real-world consequences. Despite its importance, validating the correctness of MIP solvers remains largely unexplored in both theory and practice. This paper presents the first systematic effort to address this problem. We propose feasibility-driven instance generation, a novel and effective technique for generating MIP instances to validate solver behaviors. The core idea is to systematically construct diverse MIP instances that are provably feasible or infeasible by construction. These instances are then used to test MIP solvers for finding correctness bugs. We realize this methodology in Flip. To date, Flip has uncovered 52 confirmed bugs in five widely used MIP solvers, spanning both open-source and commercial systems. Among these, 39 have been promptly fixed by the developers. Our efforts and findings have been well acknowledged and appreciated by the MIP solver community.

## 71. Variability-Aware Fuzzing

**Authors:** Meah Tahmeed Ahmed (University of Texas at Dallas), Arnab Dev (University of Texas at Dallas), Shiyi Wei (University of Texas at Dallas)

**Categories:** Testing and Analysis

**中文总结:** 提出 VAFuzz，将变体感知动态分析融入配置 fuzzing，在 25 个程序中 21 个覆盖更高并发现更多包括未知漏洞在内的缺陷。

**Abstract:** Modern software systems often provide a vast configuration space to enhance reusability and adaptability, but this configurability also significantly complicates bug finding. While existing static and dynamic variability-aware analysis approaches systematically explore the configuration space, they often suffer from scalability limitations. Conversely, grey-box fuzzing has demonstrated remarkable success in vulnerability detection through lightweight, iterative input space exploration, yet the state-of-the-art configuration fuzzers overlook the potential of integrating variability-aware analysis within the fuzzing process. In this paper, we present VAFuzz, a novel variability-aware fuzzer that integrates principled dynamic variability-aware analysis within the fuzzing process to enhance configuration space exploration. VAFuzz introduces new variability-aware seed selection and mutations to drive the fuzzing process. These are enabled by a new presence condition seed queue that tracks coverage and crash contributions across the configuration space, and a map that captures the relationship between data seeds and presence conditions. Our evaluation on a diverse set of programs show that VAFuzz outperforms the state-of-the-art configuration fuzzers on 21 out of 25 programs in terms of code coverage. It also detects more vulnerabilities than these baselines, including previous unknown bugs.

## 72. VDBFuzz: Understanding and Detecting Crash Bugs in Vector Database Management Systems

**Authors:** Shenao Wang (Huazhong University of Science and Technology), Zhao Liu (360 AI Security Lab), Yanjie Zhao (Huazhong University of Science and Technology), Quanchen Zou (360 AI Security Lab), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Testing and Analysis

**中文总结:** 提出 VDBFuzz 专门 fuzz 向量数据库边界条件，在 8 个 VDBMS 上覆盖最高达 SOTA 3 倍并发现 19 个新崩溃 bug。

**Abstract:** Vector Database Management Systems~(VDBMSs) have become critical in LLM-integrated applications, powering tasks such as Retrieval-Augmented Generation~(RAG) and long-term memory. However, their inherent complexity—stemming from high-dimensional data structures, diverse indexing strategies, and heterogeneous implementations—makes them prone to reliability issues, particularly crash bugs caused by boundary condition failures such as invalid configurations and mismatched data dimensions. These bugs can result in severe consequences, including data loss, corrupted indexes, and cascading downstream failures. To address this gap, we propose VDBFuzz, the first fuzzing framework specifically designed to detect crash bugs in VDBMSs through systematic boundary value testing. VDBFuzz systematically leverages techniques to collect high-quality seeds, generate edge-case inputs, and explore complex API interactions. We evaluated VDBFuzz on 8 representative VDBMSs, including native systems (e.g., Weaviate, Milvus), libraries (e.g., Faiss, hnswlib), and extended systems (e.g., pgvector, sqlite-vec). VDBFuzz achieved up to 3x higher code coverage compared to state-of-the-art tools such as RESTler and Schemathesis, uncovering 19 previously unknown crash bugs, including 13 memory corruption and 6 runtime exceptions. These results highlight VDBFuzz’s effectiveness in improving the robustness and reliability of VDBMSs.
