# ISSTA 2026 Research Track — Testing and Fuzzing

Source: https://conf.researchr.org/track/issta-2026/issta-2026-research-papers

Count: 31

## 1. A Dataset of Reproducible Flaky-Test Failures

**Authors:** Suzzana Rafi (George Mason University), MAHBUB-UL-HOQUE SUMON (Bangladesh Election Commission), Md Erfan, Maruf Morshed Khan, August Shi (The University of Texas at Austin), Wing Lam (George Mason University)

**Categories:** Testing and Fuzzing

**中文总结:** 发布可复现 flaky test 数据集 ReproFlake，含 1115 个跨四类别的测试及编译、运行、修复脚本与执行日志。该数据集为 flaky test 复现、修复与研究提供了首个端到端可复现实验环境。

**Abstract:** Flaky tests pass and fail non-deterministically when run on the same version of code. Although many techniques have been proposed to detect, debug, and repair flaky tests, reproducing their failures remains a major challenge due to their inherent nondeterminism. Many datasets related to flaky tests exist to help researchers study them, but these datasets are often composed of disjoint sets of flaky tests, where each dataset provides some unique information over the others, such as flaky tests of many different categories, failure logs of flaky tests, or flaky tests reported by developers vs. flaky tests found by automated tools. In this work, we aim to create a reproducible dataset of flaky tests, which are curated from both developer issue reports and a popular dataset of flaky tests. Compared to prior flaky test datasets, our dataset is the first to provide (1) a reproducible environment to compile the flaky tests, (2) scripts to run the tests to reproduce the failure, (3) scripts to automatically apply the flaky test fixes and ensure that the test is no longer flaky, and (4) execution logs of the flaky test passing and failing. We present ReproFlake, a dataset of 1115 reproducible flaky tests, spread across four different flaky test categories. We create guidelines to help others contribute to this reproducible dataset, as well as demonstrate how to use our dataset to understand the challenges with reproducing flaky test failures (i.e., challenges that researchers may face when using any of the prior flaky test datasets), the characteristics (e.g., location of the fix and its correlation with the flaky test category, as well as the difficulties researchers may face in using our dataset to collect additional information (e.g., code coverage) about flaky tests. Our findings show that error information helps identify flaky test categories and guide repairs, that unresolved compilation failures highlight challenges in building legacy projects, and that knowing typical fix locations helps prioritize repair efforts.


## 2. Belobog: Move Language Fuzzing Framework For Real-World Smart Contracts

**Authors:** Ziqiao Kong (Nanyang Technological University), Wanxu Xia (Beihang University), Zhengwei Li (Bitslab), Yi Lu (BitsLab), Pan Li (Bitslab), Liqun Yang (School of Cyber Science and Technology, Beihang University), Yang Liu (Nanyang Technological University), Xiapu Luo (Hong Kong Polytechnic University), Shaohua Li (The Chinese University of Hong Kong)

**Categories:** Testing and Fuzzing

**中文总结:** 提出首个 Move 智能合约类型感知 fuzzing 框架 Belobog，基于类型图生成合法交易并集成 concolic 执行器。在 109 个真实项目上检出 100% 关键与 79%  major 漏洞，并成功复现 Cetus 与 Nemo 事件。

**Abstract:** Move is a research-oriented programming language designed for secure and verifiable smart contract development and has been widely used in managing billions of digital assets in blockchains, such as Sui and Aptos. Move features a strong static type system and explicit resource semantics to enforce safety properties such as the prevention of data races, invalid asset transfers, and entry vulnerabilities. However, smart contracts written in Move may still contain certain vulnerabilities that are beyond the reach of its type system. It is thus essential to validate Move smart contracts. Unfortunately, due to its strong type system, existing smart contract fuzzers are ineffective in producing syntactically or semantically valid transactions to test Move smart contracts.

This paper introduces the first fuzzing framework, Belobog, for Move smart contracts. Belobog is type-aware and ensures that all generated and mutated transactions are well-typed. More specifically, for a target Move smart contract, Belobog first constructs a type graph based on Move’s type system, and then generates or mutates a transaction based on the graph trace derived from the type graph. In order to overcome the complex checks in Move smart contracts, we further design and implement a concolic executor in Belobog.

We evaluated Belobog on 109 real-world Move smart contract projects. The experimental results show that Belobog is able to detect 100% critical and 79% major vulnerabilities manually audited by human experts. We further selected two recent notorious incidents in the Move ecosystem, i.e., Cetus and Nemo. Belobog successfully reproduced full exploits for both of them, without any prior knowledge. Moreover, we applied Belobog on three ongoing auditing projects and found 2 critical, 2 major, and 3 medium new vulnerabilities, all acknowledged by the project developers.


## 3. Beyond the Surface: Towards Feature-Driven Fuzzing on the Chrome Browser

**Authors:** Chaoyuan Peng (Zhejiang University), Muhui Jiang (BlockSec), Yajin Zhou (The Chinese University of Hong Kong, Hong Kong SAR China), Lei Wu (Zhejiang University)

**Categories:** Testing and Fuzzing

**中文总结:** 提出面向浏览器特性的 fuzzing 框架 Feazzer，以 HTML 与扩展的混合程序及消息引导机制探索深层浏览器状态。在 Chromium 上覆盖率提升最多 231.1%，发现 39 个未知 bug（含 6 个 CVE）。

**Abstract:** Modern web browsers constitute complex software systems responsible for processing and rendering diverse web content. Despite extensive testing and security measures implemented by browser vendors and the community, the inherent complexity of these systems makes the complete elimination of vulnerabilities practically infeasible. Existing DOM and API fuzzing techniques inadequately address the expanded attack surface introduced by modern browser features and extensions, resulting in a substantial number of elusive vulnerabilities remaining undetected.

This paper presents Feazzer, an efficient feature-driven browser fuzzing framework designed to detect elusive vulnerabilities introduced by browser features. Our approach leverages hybrid programs comprising HTML and browser extensions with systematically clustered feature options to explore deep browser states that existing fuzzers fail to reach. We introduce a message-guided fuzzing mechanism that reduces feature conflicts and enhances the semantic quality of generated test cases. Our comprehensive evaluation across multiple Chromium versions demonstrates that Feazzer achieves up to 231.1% improvement in code coverage compared to state-of-the-art fuzzers. Feazzer has discovered 39 previously unknown bugs in Chromium, with 6 assigned CVEs and acknowledgment of over $55,000 in bug bounties from the vendor. Notably, 2 bugs are rated as critical and 27 as high severity, demonstrating the effectiveness of Feazzer in discovering impactful bugs.


## 4. CARE: Cascading Impact-Aware Compliance Test Suite Evolution under Regulatory Changes

**Authors:** Zhiyi Xue (East China Normal University), Xiaohong Chen (East China Normal University), Min Zhang (East China Normal University)

**Categories:** Testing and Fuzzing

**中文总结:** CARE 针对法规变更场景，构建 Rule-Requirement-Scenario-Test Case 四层级联关系模型，精准识别需更新的合规测试用例并最大化复用未受影响部分。多领域实验平均 F1 达 90.3%，较现有方法最高提升 164%。

**Abstract:** In response to frequent changes in regulatory rules, this paper proposes CARE, a cascading impact-aware framework for automated compliance testing evolution. Existing approaches often suffer from over-reuse or missed updates because they treat rule changes in isolation and ignore complex interdependencies across testing artifacts. CARE addresses this issue by constructing a unified four-layer cascading relation model spanning Rule-Requirement-Scenario-Test Case, enabling fine-grained traceability across abstraction levels. By explicitly modeling how rule changes propagate and amplify along this chain, the framework precisely identifies impacted scenarios and test cases that need updating, while safely maximizing the reuse of unaffected ones. Experiments conducted on real-world compliance testing tasks across multiple domains show that CARE achieves an average F1 of 90.3% on updated test suites, outperforming existing methods by up to 164% and approaching expert-level effectiveness. Ablation studies further demonstrate that explicit cascading impact modeling and handling are key contributors to these improvements. In addition, CARE substantially reduces manual effort and improves test maintenance efficiency, and indicates strong cross-domain generalization. This work highlights cascading impact propagation as a central challenge in regulation-driven test maintenance and shows that shifting from isolated rule handling to cascading impact-aware evolution is essential for achieving both high test quality and maintenance efficiency.


## 5. CLIR: Liveness-Driven and Structure-Aware Fuzzing for the Cranelift Compiler

**Authors:** Shangtong Cao (Beijing University of Posts and Telecommunications), Tianlei Song, Qiuping Yi (Beijing University of Posts and Telecommunications), Tianyu Chen (Microsoft Research Asia), Guoai Xu (Harbin Institute of Technology, Shenzhen), Ningyu He (Hong Kong Polytechnic University, Hong Kong SAR China), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Testing and Fuzzing

**中文总结:** CLIR 面向 Cranelift 编译器提出差分测试框架，集成 SSA 合法 IR 生成、活跃性引导指令精炼与跨架构诊断适配策略。72 小时内发现 24 个 bug，独特 bug 数较 cranelift-fuzzgen 等基线高 8–24 倍。

**Abstract:** Modern compilers are complex software systems that must correctly translate high-level programming languages into machine code across multiple architectures. Cranelift, a fast and modern compiler backend originally developed for WebAssembly and recently adopted as an experimental backend for Rust, has gained increasing importance due to its superior compilation speed compared to LLVM and comprehensive multi-architecture support, including x86-64, AArch64, s390x, and RISCV64. However, despite decades of development in compiler testing, testing Cranelift still illustrates unique challenges, i.e., (1) constructing valid IR under the strict enforcement of SSA form, (2) generating sequences with sufficient computational density to stress backend components, and (3) balancing broad backend coverage with efficient root cause analysis across heterogeneous architectures.

To address these challenges, we propose CLIR, a differential testing framework that integrates a syntax-preserving hierarchical generation strategy to guarantee SSA validity, a liveness-guided instruction refinement mechanism to maximize computational density, and a diagnosis-guided cross-architecture adaptation scheme to facilitate efficient root cause analysis across heterogeneous backends. Our comprehensive evaluation demonstrates that CLIR significantly outperforms existing state-of-the-art baselines, detecting 8×, 24×, and 8× more unique bugs than them, i.e., cranelift-fuzzgen, wasm-smith, and WASMaker, respectively, while RustSmith even uncovered zero bugs. Consequently, within 72 hours of testing, CLIR discovered 24 bugs, with 21 confirmed and 9 fixed spanning all target architectures.


## 6. Do Coverage and Mutation Scores of LLM-Generated Test Suites Correlate With Their Effectiveness? (Replicability Study)

**Authors:** Junda Zhao (Department of Mechanical and Industrial Engineering, University of Toronto), Shurui Zhou (University of Toronto), Eldan Cohen (Department of Mechanical and Industrial Engineering, University of Toronto)

**Categories:** Testing and Fuzzing

**中文总结:** 本文大规模复现 Inozemtseva 与 Papadakis 两项研究，检验 LLM 生成测试套件中覆盖率、变异分与真实缺陷检出率的相关性。发现这些代理指标的有效性高度依赖场景：回归测试设定下仍有参考价值，但被测代码本身含 bug 时则不可靠。

**Abstract:** Recent advances in large language models (LLMs) have driven growing interest in using LLMs to automate test generation. Prior work commonly evaluates generated test suites using proxy metrics such as code coverage and mutation score. However, studies by Inozemtseva et al. and Papadakis et al. show that, for human-written tests, correlations among coverage, mutation, and real-bug detection can largely vanish once test suite size is controlled, raising concerns about the validity of evaluations based on proxy metrics. It also remains unclear whether these conclusions carry over to LLM-generated tests, given that prevailing LLM-based test-generation workflows differ substantially from traditional approaches.

In this paper, we conduct a large-scale replication study of these two prior works using a wide range of test suites generated by a diverse set of LLMs, and re-examine the relationships among coverage, mutation, and real-bug detection effectiveness. Our findings diverge substantially from prior results. We show that the usefulness of coverage and mutation is highly context-dependent: in regression-style settings where the code provided to the LLM can be reasonably assumed bug-free, these metrics can provide meaningful signals when comparing across models; in another common scenario where the code-under-test may already be buggy and the goal is to expose the bug within code-under-test, they no longer serve as reliable indicators. We also find little evidence that test suite size is a dominant confounder for correlations among coverage, mutation, and real-bug detection for LLM-generated tests. Based on these findings, we discuss how to interpret results from prior studies and provide actionable guidance for evaluating LLM-based test generation.


## 7. Finding and Understanding Missed Optimizations in WebAssembly Optimizer (Experience Paper)

**Authors:** Ruiyang Xu (East China Normal University), Zetao Fan (East China Normal University), Shan Huang (East China Normal University), Ting Su (East China Normal University)

**Categories:** Testing and Fuzzing

**中文总结:** 针对 wasm-opt 适配 marker-based 检测与跨优化级别 differential testing，系统发现 24 种 missed optimizations（20 已修复），并分析 tree IR 设计对优化潜力的约束。

**Abstract:** As WebAssembly (\wasm) expands from web applications to high-performance domains, the standard optimizer, \texttt{wasm-opt}, is critical but frequently suffers from missed optimizations (MOs). This paper presents an experience report on detecting MOs in \texttt{wasm-opt} and understanding their root cause through the lens of \wasm’s tree-structured intermediate representation (tree IR). To this end, we adapt an established marker-based technique from C compilers, overcoming the constraints of \wasm’s structured control flow via a novel structure-aware instrumentation strategy. Complementing this, we design a cross-optimization differential testing strategy leveraging the monotonicity of optimization levels as an oracle. Together, these strategies enable the systematic identification of fine-grained MOs that are overlooked by existing cross-architecture methods. Our evaluation uncovered 24 distinct MOs (20 fixed), demonstrating the high actionability and effectiveness of our approach. Beyond detection, our root cause analysis reveals how \texttt{wasm-opt}’s tree IR and other design choices constrain its optimization potential. We conclude with architectural considerations and future directions for \texttt{wasm-opt} and similar optimizers.


## 8. From Natural Language to Executable Properties for Property-based Testing of Mobile Apps (Experience Paper)

**Authors:** Yiheng Xiong (Singapore Management University), Ting Su (East China Normal University), Jingling Sun (University of Electronic Science and Technology of China), Jue Wang (Nanjing University), Qin Li (Shanghai Key Laboratory of Trustworthy Computing, East China Normal University), Geguang Pu (East China Normal University, China), Zhendong Su (ETH Zurich)

**Categories:** Testing and Fuzzing

**中文总结:** 提出 iPBT，将自然语言 property 描述经 UI 语义 grounding 与 LLM 合成为可执行 mobile PBT property；在 124 条描述上准确率 95.2%，用户编写时间减少 56%。

**Abstract:** Property-based testing (PBT) is a popular software testing methodology and is effective in validating the functionality of mobile applications (apps for short). However, its adoption in practice remains limited, largely due to the manual effort and technical expertise required to specify executable properties. In this experience paper, we propose a novel structured property synthesis approach that automatically translates property descriptions in natural language into executable properties, and implement it in a tool named iPBT.   Our approach decomposes the problem into UI semantic grounding and executable property synthesis. It first builds an enriched widget context via multimodal LLMs to align visual elements with their functional semantics, and then uses an LLM with in-context learning to generate framework-specific executable properties. We evaluate \tool with a closed-source LLM (GPT-4o) and an open-source LLM (DeepSeek-V3) on 124 diverse property descriptions derived from an existing benchmark dataset. \tool achieves 95.2% (118/124) accuracy on both LLMs. Notably, an ablation study reveals that the enriched widget context contributes to an absolute improvement of up to 20.2% (from 75.0% to 95.2%). A user study with 10 participants demonstrates that \tool reduces the time required to write executable properties by 56%, suggesting substantially lower manual effort. Furthermore, evaluations on 1,180 linguistically diverse variations demonstrate \tool’s robustness (87.6% accuracy), indicating its capability to handle varied expressions.


## 9. Fuzzing FPGA Synthesis and Simulation Tools via LLM-Generated Syntax-Valid HDL Codes

**Authors:** He Jiang (Dalian University of Technology), Wen Zhao (Dalian University of Technology), Shikai Guo (Dalian Maritime University), Zhihao Xu (Monash University and Southeast University), Xiaochen Li (Dalian University of Technology), Rubing Huang (Macau University of Science and Technology (MUST))

**Categories:** Testing and Fuzzing

**中文总结:** 提出 PolyHDL，用 LLM prompt learning 与 primitive-cell 多样性反馈生成语法合法 HDL 以 fuzz FPGA 综合/仿真工具；一个月内报告 18 个有效缺陷，覆盖率较 SOTA 提升 13%+。

**Abstract:** Field-Programmable Gate Array (FPGA) synthesis and simulation tools, such as \textit{Vivado}, \textit{Quartus}, \textit{Yosys}, and \textit{Icarus Verilog}, are key components of Electronic Design Automation (EDA) toolchains, translating high-level Hardware Description Language (HDL) codes into low-level gate netlists. However, defects in these compilers can propagate into the synthesized netlists, leading to crashes and functionally incorrect or even insecure hardware implementations and posing significant security risks. Existing fuzz testing approaches face several challenges, including limited diversity in primitive-cell types and a lack of feedback-guided exploration. These issues restrict their ability to thoroughly exercise the compilers and expose deep-seated defects. To address these challenges, we propose PolyHDL, which leverages the prompting Large Language Models (LLMs) for generating valid HDL codes to detect compiler defects in FPGA synthesis and simulation tools. By leveraging prompt learning and integrating feedback-driven guidance from primitive-cell diversity, PolyHDL generates semantically valid HDL codes with diverse primitive-cell combinations, thereby addressing the aforementioned challenges. Furthermore, through equivalence check, PolyHDL effectively reveals potential compiler defects in FPGA synthesis and simulation tools. Experimental results demonstrate that PolyHDL successfully identified and reported 18 valid defects in widely used toolchains, including \textit{Vivado}, \textit{Yosys}, \textit{Icarus Verilog}, and \textit{Quartus} within one month, 16 of which were confirmed by the official technical support, and achieved a 13.1%–13.4% improvement in code coverage over the SOTA approach.


## 10. How Does Killing Surviving Mutants Help Detect Real Bugs with Assertion Generation? A Controlled Experiment

**Authors:** Hang Du (University of California at Irvine), Vijay Krishna Palepu, James Jones (University of California at Irvine)

**Categories:** Testing and Fuzzing

**中文总结:** 首次大规模 controlled experiment 直接度量 killing surviving mutants 对真实 bug 检测的因果影响；642 个 Defects4J bug 中 63 个可通过 principled mutant killing 检出。

**Abstract:** Killing surviving mutants is a central activity of mutation testing. This activity is motivated by the coupling-effect hypothesis: tests that expose simple artificial faults can also detect more complex, previously unseen real bugs. Despite these claimed benefits, automated studies have not directly measured the causal impact of mutant killing on real-bug detection. This limitation stems from open-ended mutant-killing strategies and a fundamental evaluation asymmetry that obscures causal attribution. In this work, we present the first large-scale controlled experiment that directly measures whether killing surviving mutants, without knowledge of future real bugs, would have enabled their detection. We model mutant killing as a selective, incremental process under realistic budget constraints, and we restrict test improvements to assertion augmentation. This restriction enables precise attribution of each test augmentation to a specific mutant-killing action. To support the experiment, we design a fully automated, fault-based assertion-augmentation technique that operates uniformly on mutants and real bugs and integrate it into Defects4J. Our controlled experiment yields several key empirical insights: (1) Across 642 Defects4J bugs, we find that 104 bugs would become detectable by adding an additional assertion to an existing passing, non-triggering test. (2) When coupling exists, a real bug is, on average, coupled with 21 surviving mutants, through which mutant killing can produce triggering tests. This number is substantially higher than the average of two mutants reported in prior studies. In those studies, coupling is inferred solely from documented bug-fixing tests rather than from tests derived via mutant killing. (3) Among these bugs, 63 of the 104 are detectable through principled mutant-killing (test augmentation) process. Notably, killing a randomly selected 30% of relevant surviving mutants, using only one assertion per mutant, suffices to detect 84.5% of these bugs. (4) By substituting mutants with real bugs and comparing their resulting assertion augmentation outputs, we find that real bugs induce broader behavioral effects than mutants, affecting more memory state locations, variables, and tests. (5) When mutation-derived assertions detect real bugs, they validate program outputs that overlap with, and are often strict subsets of, those affected by the real bugs. This offers a mechanistic explanation for why killing simple mutants can enable the detection of more complex real bugs.


## 11. IterTestQ: Assembly-Level, Cross-Platform Testing of Quantum Computing Platforms

**Authors:** Matteo Paltenghi (University of Stuttgart), Michael Pradel (CISPA Helmholtz Center for Information Security)

**Categories:** Testing and Fuzzing

**中文总结:** 提出 IterTestQ 首个跨平台量子计算平台测试方法，通过 ITE（Import-Transform-Export）生成等价 QASM 程序并用 crash/equivalence oracle 检测不一致；在四大平台发现 18 个 bug（15 已确认/修复）。

**Abstract:** Quantum computing platforms are susceptible to quantum-specific bugs, such as incorrectly ordering qubits or incorrectly implementing quantum abstractions. These bugs are difficult to detect and require specialized expertise. The field faces challenges due to a fragmented landscape of platforms and rapid development cycles that often prioritize new features over thorough testing, severely hindering the reliability of quantum software. To address these challenges, we present IterTestQ, the first cross-platform testing approach for quantum computing platforms. The key technical contribution is our novel ITE process, which generates equivalent quantum programs by iteratively (I)mporting them into platform-specific representations, (T)ransforming the program via optimizations and gate conversions, and (E)xporting the program again. To transfer programs across platforms and test cross-platform consistency, IterTestQ leverages QASM, an assembly-level representation supported by most platforms. The approach uses a crash oracle to detect failures during cross-platform transformations and an equivalence oracle to validate the semantic consistency of the generated assembly programs, which are expected to be equivalent by construction. We evaluate IterTestQ on four widely-used quantum computing platforms: Qiskit, PennyLane, Pytket, and BQSKit, revealing 18 bugs, 15 of which are already confirmed or fixed. Our results also demonstrate that IterTestQ complements existing quantum fuzzers (covering tens of thousands of otherwise uncovered lines), is efficient (with 0.00089 seconds per generated program), and that the ITE process is crucial for its effectiveness.


## 12. Mathematically-Guided Detection of Floating-Point Errors

**Authors:** Youshuai Tan (Macau University of Science and Technology), Zhanwei Zhang (The Hong Kong University of Science and Technology (Guangzhou)), Haonan Zhang (University of Waterloo), Lianyu Zheng (The Hong Kong University of Science and Technology (Guangzhou)), Zishuo Ding (The Hong Kong University of Science and Technology (Guangzhou)), Jinfu Chen (Wuhan University), Weiyi Shang (University of Waterloo)

**Categories:** Testing and Fuzzing

**中文总结:** MGDE 基于条件数理论定位数值不稳定原子操作，并将浮点错误检测建模为 Newton–Raphson 根求解以定向收敛至易错区域。在 GSL 88 个单输入函数上触发 80 个 bug，速度较 ATOMU/FPCC 分别快 41.71× 与 10.17×，并报告 16 个新 bug。

**Abstract:** Floating-point computations are important for modern scientific and engineering software, especially for safety-critical systems, yet only a small subset of inputs typically trigger substantial numerical errors. Detecting such error-inducing inputs and the underlying bugs is therefore essential for improving their security and reliability. Existing techniques commonly rely on either oracle-driven exploration that repeatedly compares against high-precision references or search-driven heuristics. Despite the improvements made, they remain limited by \textbf{(1) Expensive computation of high-precision oracles} and \textbf{(2) Lack of long-range convergence}, which often requires dense probing near narrow error-inducing regions and expensive computation.

We propose MGDE (\textbf{M}athematically-\textbf{G}uided \textbf{D}etection of floating-point \textbf{E}rrors), a method that replaces trial-and-error exploration with mathematically defined targets and directed convergence. MGDE first uses condition-number theory to identify numerically unstable atomic operations without invoking expensive high-precision oracles during exploration. MDGE exploits the observation that extreme condition numbers occur near structured boundaries (e.g., cancellation points and singularities), reformulating detection as a numerical root-finding problem. By solving the resulting objectives with the Newton–Raphson method, MGDE can steer inputs toward error-prone regions from far-away initializations.

We evaluate MGDE on GNU Scientific Library (GSL) functions and compare against two state-of-the-art baselines, ATOMU and FPCC, using triggered bugs as the primary metric. On 88 single-input functions, MGDE triggers 80 bugs across 47 functions, outperforming ATOMU (70 bugs in 46 functions) and FPCC (53 bugs in 42 functions). MGDE is also faster: ATOMU and FPCC require 41.71$\times$ and 10.17$\times$ more time, respectively. The advantage is even more significant for multi-input functions, where MGDE triggers nine bugs while FPCC triggers none, and achieves an average runtime of 0.6443 seconds per function compared to FPCC’s 100-second budget. Overall, MGDE substantially advances the state of the art in both effectiveness and efficiency, and we report 16 previously unknown GSL bugs, which have been confirmed by the GSL community.


## 13. Metamorphic Coverage

**Authors:** Jinsheng Ba (The Chinese University of Hong Kong, Shenzhen), Yuancheng Jiang (National University of Singapore), Manuel Rigger (National University of Singapore)

**Categories:** Testing and Fuzzing

**中文总结:** Metamorphic Coverage (MC) 度量蜕变测试中成对输入所执行的差异代码，比行覆盖更能反映测试有效性且比变异测试快 359×。MC 与 64 个蜕变测试发现 bug 中 50 个修复位置重叠，用作反馈指导可多发现 41% bug。

**Abstract:** Metamorphic testing is a widely used methodology that examines an expected relation between pairs of executions to automatically find bugs, such as correctness bugs. We found that code coverage cannot accurately measure the extent to which code is validated and mutation testing is computationally expensive for evaluating metamorphic testing methods. In this work, we propose Metamorphic Coverage (MC), a coverage metric that examines the distinct code executed by pairs of test inputs within metamorphic testing. Our intuition is that, typically, a bug can be observed if the corresponding code is executed when executing either test input but not the other one, so covering more differential code covered by pairs of test inputs might be more likely to expose bugs. While most metamorphic testing methods have been based on this general intuition, our work defines and systematically evaluates MC on five widely used metamorphic testing methods for testing database engines, compilers, and constraint solvers. The code measured by MC overlaps with the bug-fix locations of 50 of 64 bugs found by metamorphic testing methods, and MC has a stronger positive correlation with bug numbers than line coverage. MC is 4x more sensitive than line coverage in distinguishing testing methods’ effectiveness, and the average value of MC is 6x smaller than line coverage while still capturing the part of the program that is being tested. MC required 359x less time than mutation testing. Based on a case study for an automated database system testing approach, we demonstrate that when used for feedback guidance, MC significantly outperforms code coverage, by finding 41% more bugs. Consequently, this work might have broad applications for assessing metamorphic testing methods and improving test-case generation.


## 14. MG-Fuzz: Model-Guided Fuzzing for Unsafe Scenario Discovery in Autonomous Driving Systems

**Authors:** Yulong Lyu (Nanjing University), Ruiqi Hong (Nanjing University), Jiawan Wang (Nanjing University), Jun Sun (Singapore Management University), Lei Bu (Nanjing University)

**Categories:** Testing and Fuzzing

**中文总结:** MG-Fuzz 从 ADS 决策组件提取自动机模型，结合模型指标与安全指标做多目标模糊测试以发现危险驾驶场景。实验检测到 18 类不同不安全场景，显著拓宽相对 SOTA 工具的覆盖范围。

**Abstract:** As autonomous driving systems (ADS) are increasingly deployed in real-world environments, discovering diverse unsafe driving scenarios remains a fundamental yet difficult problem. Existing scenario generation and testing approaches often rely on black-box exploration or externally-observed heuristic feedback, which struggle to effectively guide the search toward high-risk scenarios induced by complex decision-making behaviors. A key difficulty stems from the fact that unsafe behaviors in ADS often arise from internal decision-making logic, which can induce structured and discontinuous responses that are hard to effectively explore using purely black-box guidance. Consequently, current tools tend to repeatedly discover a narrow set of similar unsafe scenario types, limiting their ability to expose diverse and previously unseen failure modes.

In this paper, we propose MG-Fuzz, a model-guided, multi-objective fuzzing framework for unsafe scenario discovery in autonomous driving systems. Our approach extracts an  automaton model that captures the core control logic of the ADS decision-making component, and leverages this model as structured guidance for search-based scenario exploration. To systematically drive the exploration process, MG-Fuzz integrates model-based metrics derived from the automaton with complementary safety metrics, enabling effective evaluation and prioritization of generated driving scenarios across diverse unsafe behavior types. MG-Fuzz has been developed and thoroughly evaluated through extensive experiments on autonomous driving systems.  Experimental evidence indicates that MG-Fuzz successfully detects 18 distinct types of unsafe driving scenarios, marking a substantial improvement in detection breadth relative to current state-of-the-art tools.


## 15. Names Are All You Need: Effective and Safe Regression Test Selection for Python

**Authors:** You Wang (Zhejiang University), Michael Pradel (CISPA Helmholtz Center for Information Security), Zhongxin Liu (Zhejiang University)

**Categories:** Testing and Fuzzing

**中文总结:** NameRTS 将 Python 程序建模为代码元素与 name 节点的二分图，以可达性做细粒度回归测试选择而无需调用图。在 500 commits 基准上平均跳过 69.90% 测试文件、端到端测试时间降 45.59%，99.6% commits 安全。

**Abstract:** Regression test selection (RTS) reduces the cost of regression testing by executing only those tests affected by a code change. Despite extensive study of RTS in statically typed languages such as Java, achieving effective and safe RTS in Python is challenging. Python’s dynamic typing makes precise call-graph construction difficult, which can cause call-graph-based RTS to miss affected tests, and hence, compromise safety. Python’s eager importing mechanism, in contrast, renders file-level dependency analysis overly conservative. This paper presents NameRTS, the first Python RTS approach based on fine-grained dependency analysis. NameRTS models a Python program as a bipartite graph of code element nodes (e.g., classes, functions, global variables) and name nodes (i.e., identifiers used to reference code elements), with edges capturing definitions and references. RTS is formulated as a reachability problem on this graph: a test is selected if any modified code element is reachable from the names used in that test. This design avoids call-graph construction, enabling a conservative analysis amenable to safety. To control dependency cascades introduced by coarse name matching, NameRTS applies two pruning strategies that leverage prior test executions and context information to refine name matching. To evaluate NameRTS, we construct the first Python RTS dataset with a ground truth indicating which test files are affected by each commit. It includes 500 commits drawn from 10 real-world Python projects. We compare NameRTS with the best-performing baseline, BabelRTS, an RTS technique based on coarse file-level dependencies. On this benchmark, NameRTS skips 69.90% of test files on average, outperforming BabelRTS by 146.5%. It also reduces end-to-end testing time by 45.59%, yielding a 107.7% improvement over BabelRTS. In terms of safety, NameRTS selects all affected tests for 99.6% of commits, with only rare misses in exceptional cases. In contrast, BabelRTS is safe for 76.6% of commits. These results demonstrate the effectiveness of NameRTS, paving the way for more efficient regression testing in Python.


## 16. NCFuzz: Configuration-guided Network Service Fuzzing

**Authors:** Xuesong Bai (University of California, Irvine), Hengkai Ye (Pennsylvania State University), Shenghan Zheng (Dartmouth College), Fenglu Zhang (China Telecom), Hong Hu (Pennsylvania State University), Zhou Li (University of California, Irvine)

**Categories:** Testing and Fuzzing

**中文总结:** NCFuzz 利用文档配置知识与配置-报文数据流关系引导网络服务模糊测试，专门发现非默认配置下的 ConfBug。在六种网络服务实现上覆盖率高于基线，并发现 5 个 ConfBug。

**Abstract:** Network services like FTP and DNS are critical components of modern dependable cyberspace infrastructure. Software fuzzing, especially network protocol fuzzing, is widely used to uncover flaws in these systems. However, conventional fuzzers focus on network messages, overlook one critical dimension, service configurations. Incorporating configurations into fuzzing is challenging due to complex semantics, trigger conditions, and resulting enlarged search space. We tackle the problem of finding bugs under non-default configurations, termed ConfBug, by designing a new fuzzer called NCFuzz. NCFuzz leverages two key observations: 1) software documentation contains rich information about configurations; 2) interactions between configuration and network messages can be tracked through code instrumentation and data-flow analysis. Using these insights, NCFuzz uses configuration knowledge and configuration-network-message relation to guide fuzzer towards new software states. Evaluations on six network service implementations show NCFuzz achieves higher coverage than baseline fuzzers. Five ConfBug were discovered during fuzzing.


## 17. Profiling-Guided Bayesian Optimization of JVM Configurations

**Authors:** Abdelrahman Baz (The University of Texas at Austin), Wing Lam (George Mason University), August Shi (The University of Texas at Austin)

**Categories:** Testing and Fuzzing

**中文总结:** PROBO 采集 44 项 JVM 运行时指标，经 metrics 模型与 performance 模型两阶段贝叶斯优化搜索降低回归测试时间。在 16 个 Java 项目上平均测试时间降 10.7%，较随机搜索与 BOCA 分别快 1.85× 与 2.49×。

**Abstract:** Regression testing is essential for maintaining software quality but often incurs substantial time costs. Prior work has demonstrated that tuning Java Virtual Machine (JVM) configuration flags can reduce test execution time, yet finding effective flag combinations remains challenging due to the vast configuration space and complex interactions between flags. Random search and direct modeling approaches that map flags to testing time have shown limited effectiveness in navigating this complex optimization landscape. We present PROBO (PROfiling-Guided Bayesian Optimization), an iterative approach that leverages JVM runtime metrics (such as garbage collection frequency, just-in-time (JIT) compilation rates, and memory allocation) to guide Bayesian optimization for testing time reduction. Unlike prior work that directly models the relationship from flags to testing time, PROBO decomposes the prediction problem through observable runtime behaviors: a metrics model predicts how flag configurations affect runtime metrics, and a performance model predicts how those metrics affect testing time. PROBO collects 44 runtime metrics using a profiler during test execution, and propagates feature importance scores through both models to identify which flags most strongly influence testing time-predictive metrics. Finally, PROBO generates candidate flag configurations through three complementary strategies guided by expected testing time improvement. We evaluate PROBO on 16 open-source Java projects, comparing against random search and BOCA (a Bayesian optimization baseline). PROBO achieves an average testing time reduction of 10.7% across all projects, outperforming random search (5.8%) by 1.85× and BOCA (4.3%) by 2.49×. PROBO successfully generates configurations that substantially reduce testing time for all 16 projects, with reductions ranging up to 27.4%. With a one-hour time budget for search, PROBO maintains its advantage with 8.0% average reduction, demonstrating practical applicability. Moreover, PROBO-generated configurations remain effective across software evolution, maintaining 8.8% average reduction over 88 future commits per project. Our analysis reveals that JIT compilation metrics, particularly Total Compilation Rate (methods compiled per second) and C1 Compilation Rate (first-tier JIT compilation rate), are the strongest predictors of testing time, accounting for 67.2% of consistently important metrics across projects.


## 18. PropCov: Effective Coverage Reporting for Property-Based Testing

**Authors:** Jesse Coultas (University of Illinois Chicago), Joseph Wiseman (University of Illinois Chicago), Luís Pina (University of Illinois Chicago)

**Categories:** Testing and Fuzzing

**中文总结:** PropCov 结合静态分析与 PBT 估算属性测试可达最大覆盖率，纠正 JaCoCo 等工具 86% 不可达误报并给出改进建议。在 25 个 Java 项目 293 个属性上仅漏 4% 可达代码，依建议增覆盖后在 4 个项目发现 4 个新 bug。

**Abstract:** Property-base testing (PBT), introduced by Haskell’s Quickcheck, is becoming more popular with successful ports for other languages, such as Java’s junit-quickcheck. With PBT, developers write a property test and a data generator. The data generator takes a source of non-determinism and uses it to output well-formed data. The property test exercises the System Under Test (SUT) using the random well-formed data from the generator to ensure a particular property always holds (e.g., data serialized and deserialized should be equal to the original data). The PBT framework then performs many trials, each generating fresh data and executing the property test. A test failure shows a bug to developers, typically in edge-cases. A passing test gives some assurance on the quality of the SUT with regards to the property being tested. Unfortunately, well-known test coverage tools that are instrumental for understanding unit testing work poorly for PBT.

In this paper, we present PropCov, a tool for understanding coverage in PBT that also provides suggestions for coverage improvement. PropCov employs a novel combination of static analysis with PBT to approximate the maximum possible coverage, providing an effective measure of the PBT coverage and making suggestions to developers of where to improve existing tests. PropCov features an easily extensible architecture that can support new languages, build systems, and PBT frameworks. We evaluated PropCov using 25 Java projects using junit-quickcheck or jqwik, totaling 293 properties, and found that existing tools report missed coverage that is impossible to reach (86% of lines that JaCoCo reports as not covered), which leads developers to consider hundreds of extra lines of code (2910). Unlike existing coverage tools, PropCov results are accurate — only 7.5% of all properties contain unfeasible code, and PropCov only misses 4% of reachable code. Using PropCov’s suggestions, we increased the coverage of 42 tests over 7 projects and found 4 new bugs in 4 projects.


## 19. Re-evaluating Detection of Equivalent Mutants Using LLMs: We Should Properly Measure How Far We Are

**Authors:** Arjun Tandon (Indraprastha Institute of Information Technology Delhi), Mehmet Fırat Dündar, Milkiyas Gebremichael Gebru, Darko Marinov (University of Illinois at Urbana-Champaign), Yiling Lou (University of Illinois at Urbana-Champaign), Wenxi Wang (University of Virgina)

**Categories:** Testing and Fuzzing

**中文总结:** 重新评估 LLM 等价 mutant 检测（EMD）的泛化能力，发现原数据集存在 method 级数据泄露且 LLM 依赖多数投票捷径。跨算子、语言与新项目数据集上性能显著下降，呼吁采用更真实的跨方法评估设置。

**Abstract:** Mutation testing is a widely used approach for measuring quality of test suites. Equivalent mutant detection (EMD), i.e., determining if a mutant semantically behaves the same as the original code despite some syntactic differences, is a critical problem in mutation testing. A recent study has shown the great promise of LLM-based EMD techniques, reporting substantial improvements over traditional compiler- and machine-learning–based approaches. In this work, we revisit prior results and evaluate the generalization capabilities of LLM-based EMD techniques across two new datasets that differ from the original dataset in mutation operators, programming languages, and source projects. Contrary to prior findings, all studied LLM-based EMD techniques suffer substantial performance degradation on the new datasets. Through extensive analysis, we identify original-method–level data leakage in the original dataset as a key factor inflating earlier results and show that LLMs often rely on a method-wise majority-voting shortcut rather than reasoning about the semantic effects of individual mutations. Based on these findings, we call for the adoption of realistic cross-method evaluation settings and the development of mutation-centric semantic reasoning in future LLM-based EMD research.


## 20. Repair-Driven Greybox Fuzzing

**Authors:** Bachir Bendrissou (Imperial College London), Alastair F. Donaldson, Cristian Cadar (Imperial College London)

**Categories:** Testing and Fuzzing

**中文总结:** 提出 repair-driven greybox fuzzing 及 RepairFuzz：先用 AFL++ 字节级变异破坏输入，再用 CPCT+ 语法修复恢复合法结构。在 Lua/PHP/JS/Ruby 四类解释器上发现 10 个已确认新 bug，其中 9 个未被 Nautilus、Grammarinator 或 AFL++ 发现。

**Abstract:** We present repair-driven greybox fuzzing, a new approach to greybox fuzzing that combines the strengths of unstructured, byte-level input mutation and grammar-guided input generation. By increasing input diversity while preserving input validity, repair-driven fuzzing promises to improve bug-finding ability for systems under test such as programming language interpreters that consume highly structured inputs. Our idea is to first mutate an input using a standard byte-level mutator, typically leading to an invalid input, and then repair the input using a grammar. Aggressively breaking and then repairing an input provides an effective way to reach parts of the input space that would be left unexplored by both byte-level and idiomatic grammar-based mutations. We put this idea into practice via RepairFuzz, a new greybox fuzzer based on AFL++, leveraging the byte level mutations of AFL++ and using the CPCT+ error recovery algorithm for input repair. We present a large experimental evaluation applying RepairFuzz to six SUTs covering four different programming language input formats (Lua, PHP, JavaScript and Ruby), and present an experimental comparison with AFL++, Nautilus, and Grammarinator, the state-of-the-art in standard greybox fuzzing and grammar-guided fuzzing. Our evaluation shows that RepairFuzz was able to find 10 confirmed bugs that were previously-unknown, including 9 that could not be found using Nautilus, Grammarinator, or AFL++ directly or in combination. Further, RepairFuzz yields absolute increases in code coverage for several SUTs and substantial complementary code coverage across all.


## 21. RESTOR: Automated Test Oracle Generation for RESTful APIs via Reinforcement Learning

**Authors:** Xun Zhou (Fudan University), Zhen Dong (Fudan University), Mingyu Ren (Fudan University), Qiang Li (ByteDance), JunJie Li (ByteDance), Sifan Wang (ByteDance), Xiaolong Yu (ByteDance), Chaofeng Sha (Fudan University), Xin Peng (Fudan University)

**Categories:** Testing and Fuzzing

**中文总结:** 提出 RESTOR，用 GRPO 微调轻量 LLM，从单条 REST API 请求-响应对生成可执行测试断言。工业数据集上关键字段识别 F1 达 85.42%，生产部署将核心业务的自动化用例采纳率从 74.1% 提升至 90% 以上。

**Abstract:** Automated testing for REST APIs has witnessed rapid advancements, yet existing techniques often rely heavily on formal specifications or massive execution logs, rendering them ineffective in agile industrial environments characterized by cold-start features and isolated traffic samples. In this paper, we present RESTOR, a framework that utilizes Group Relative Policy Optimization (GRPO) to fine-tune a lightweight Large Language Model for generating executable test assertions from single request-response pairs. By employing a novel data augmentation pipeline that constructs semantic constraints and valid/invalid logic variations, RESTOR enables the model to internalize testing common sense and distinguish business logic from dynamic noise. Comprehensive evaluations on industrial datasets demonstrate that RESTOR significantly outperforms large-scale generalist models (e.g., DeepSeek-V3.1). Specifically, it achieves a superior F1-score of 85.42% in key field identification by maintaining a high Precision of 81.30%, effectively mitigating the over-generation issues observed in baselines. Moreover, expert reviews confirm its reliability, showing that RESTOR produces the highest volume of semantically Exact Match assertions while minimizing factual errors on noisy data. Finally, deployment in a production environment at a large-scale technology company validates its practical impact: the system raised the automated test case adoption rate from 74.1% to over 90% in core business lines, substantially reducing manual QA effort in high-frequency CI/CD workflows.


## 22. RPCSpecter: Detecting Blockchain RPC Bugs through a Specification-Driven, Constraint-Aware Fuzzing Approach

**Authors:** Yuming Xiao (Sun Yat-sen University), Yuhong Nan (Sun Yat-sen University), Zhijie Zhong (Sun Yat-sen University), Mingxi Ye (Sun Yat-sen University), Zibin Zheng (Sun Yat-sen University)

**Categories:** Testing and Fuzzing

**中文总结:** 提出 RPCSpecter，从 RPC 规范抽取约束、约束引导变异与双向断言三阶段 fuzz 区块链 RPC 实现。在 Ethereum/Solana 共 6 个客户端上发现 26 个未知 bug，其中 1 个获 $3000 漏洞赏金。

**Abstract:** Blockchain Remote Procedure Calls (RPCs) serve as the primary interface for interaction between decentralized applications and blockchain networks. Despite their critical role, existing RPC implementations are prone to bugs that are often challenging to detect using traditional testing methods. In this paper, we introduce RPCSpecter, an automated framework for constraint-aware fuzz testing of blockchain RPC Implementations. The core of RPCSpecter is a three-stage process: (1) Constraint Extraction, where implicit semantic dependencies from the documented RPC specifications are parsed and converted into executable constraints, (2) Constraint-Guided Mutation, which generates diverse and semantically valid test inputs based on these constraints, and (3) Bidirectional Assertion, which validates both valid and invalid RPC responses through dynamic checks and self-learning mechanisms. We evaluate RPCSpecter   on both Ethereum and Solana, two predominant platforms in the Blockchain ecosystem, with a total of 6 clients, such as Geth, Besu and Agave. The results show that RPCSpecter uncovers a total of 26 previously unknown bugs, including critical errors that are undetectable by existing fuzzers or manual testing, as well as multiple silent semantic inconsistencies. Particularly, 4 of them have been acknowledged, and one of the bugs affecting three major Ethereum clients is confirmed as a vulnerability, with a $3,000 bounty-award. Additionally, we demonstrate how RPCSpecter’s constraint-driven approach significantly improves the efficiency and effectiveness of fuzz testing by systematically guiding mutation to explore boundary conditions and rare edge cases. Our research provides a more robust, scalable, and automated solution for enhancing the reliability and security of blockchain RPC implementations.


## 23. SimiFuzz: Seed–Worker Scheduling for Parallel Fuzzing via Contextual Bandits

**Authors:** Yijia Guo (Zhejiang Normal University), Zhiguo Ding (Zhejiang Normal University), Hong Liang (Zhejiang University), Ming Zhong (Zhejiang Normal University), Dandan Zhao (Zhejiang Normal University), Xuhong Zhang (Zhejiang University), Bo Zhang (China Electric Power Research Institute), Shouling Ji (Zhejiang University), Hao Peng (Zhejiang Normal University)

**Categories:** Testing and Fuzzing

**中文总结:** 提出 SimiFuzz，用 LinUCB 上下文 bandit 在线学习 seed–worker 配对，平衡个体效率与组内冗余。基于 AFL++ 在 8 个目标 24 小时 10 并行 worker 活动中边覆盖平均提升 28.84%，多发现 29 个唯一 bug 与 9 个 CVE。

**Abstract:** Parallel fuzzing is now a standard way to scale vulnerability discovery, yet its efficiency is still limited by ineffective task allocation among workers. Existing approaches mainly aim to reduce conflicts, yet none explicitly captures the interaction between seeds and workers: the same seed can yield very different gains on different workers due to their divergent exploration states. As a result, parallel fuzzing can drift toward over-isolation that wastes shared progress, or excessive overlap that duplicates effort.

To address this challenge, we present SimiFuzz, a context-aware scheduling framework that learns to assign \emph{seed–worker} pairs online. SimiFuzz encodes each assignment with a compact context vector that jointly models seed characteristics, worker state, and seed–worker interaction. On top of this representation, SimiFuzz employs a LinUCB-based contextual bandit to score candidate pairs, balancing individual worker efficiency against group-level redundancy to maximize collective progress. To handle non-stationary fuzzing dynamics, SimiFuzz adopts a time-slice feedback mechanism that aggregates coverage gains within fixed intervals, combining globally new edges with cross-learning progress to form stable reward signals. We implement SimiFuzz on top of AFL++ and evaluate it on eight real-world targets. Across 24-hour campaigns with 10 parallel workers, SimiFuzz improves average edge coverage by 28.84% and achieves the best final coverage on all targets, while detecting 29 more unique bugs and 9 more CVEs.


## 24. Systematically Cover SQL Syntactic Structures via k-Sequence

**Authors:** Hongtao Zhou (Institute of Software Chinese Academy of Sciences), Yingying Zheng (Institute of Software at Chinese Academy of Sciences), Yu Gao (Institute of Software, Chinese Academy of  Sciences), Jiansen Song (Institute of Software at Chinese Academy of Sciences), Xudong Xie (Institute of Software Chinese Academy of Sciences, China), Rui Yang (Institute of Software, Chinese Academy of Sciences), Ziyu Cui (Institute of Software at Chinese Academy of Sciences), Wensheng Dou (Institute of Software Chinese Academy of Sciences), Jun Wei (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Testing and Fuzzing

**中文总结:** 提出 k-sequence 覆盖准则同时刻画 SQL 派生中的父子与兄弟结构关系，并实现定向 fuzzer KSeqFuzz。在 MySQL、MariaDB、TiDB、OceanBase 上发现 58 个新 bug（含 6 个严重 crash），24 小时活动多检出 26% 唯一 bug。

**Abstract:** Testing Relational Database Management Systems (RDBMSs) is inherently challenging because SQL, the primary language for interacting with RDBMSs, exhibits a vast and highly complex grammar with hundreds of interdependent production rules in the Extended Backus–Naur Form. While existing grammar-based testing techniques have made progress in covering SQL syntactic structures, they predominantly focus on \textit{parent-child relationships} in derivation paths, which capture \textit{vertical} expansions from a non-terminal to its alternatives. However, they overlook an equally critical dimension, \textit{sibling-like relationships}, which capture co-occurring alternatives across derivation paths. This oversight results in insufficient coverage of intricate syntactic interactions that may trigger unique behaviors or latent bugs in RDBMSs.

In this work, we propose \textit{k-sequence}, a novel coverage criterion that characterizes syntactic structures as ordered sequences of $k$ alternatives encountered during derivation. By simultaneously capturing both \textit{vertical parent-child} and \textit{horizontal sibling-like} relationships in the SQL syntactic structures, \textit{k-sequence} provides a unified framework for comprehensive SQL syntactic coverage. Based on this criterion, we develop KSeqFuzz, a directed fuzzing approach that systematically generates SQL statements to explore previously unseen \textit{k-sequence}s, achieving deeper and broader testing coverage. We implement and evaluate KSeqFuzz on four widely-deployed RDBMSs, i.e., MySQL, MariaDB, TiDB, and OceanBase. In total, KSeqFuzz detects 58 new unique bugs, including 6 critical crashes. Evaluation results demonstrate that KSeqFuzz outperforms state-of-the-art baselines, detecting 26% more unique bugs during 24-hour testing campaigns.


## 25. SyzDiversity: Diversity-Guided Linux Kernel Fuzzing

**Authors:** Kun Hu (School of Computer Science, Fudan University), Jiaji Qin (Fudan University), Chaofeng Sha (Fudan University), Bihuan Chen (Fudan University), Shuoran Bai (Harbin Engineering University), Qicai Chen (Fudan University, China), Chenglin Wang (Fudan University), Xin Peng (Fudan University), Wenyun Zhao (Fudan University)

**Categories:** Testing and Fuzzing

**中文总结:** SyzDiversity 提出多样性引导的 Linux 内核模糊测试框架，利用 PoC 种子、社区流行率（CPR）感知的 MAB 调度与 CPR 引导变异提升种子多样性。在 v5.15/v6.14 上相较 SOTA 覆盖率提升 17.4%、漏洞发现能力提升 9.1×，发现 32 个新漏洞（12 个已确认）。

**Abstract:** Linux kernel vulnerabilities can pose severe security threats to the entire software ecosystem. While coverage-guided kernel fuzzers have been proposed to uncover such vulnerabilities, their code coverage and bug-finding capability are still limited due to the lack of seed diversity, which is caused by the compounding effect of initial seed generation, seed scheduling, and seed mutation. To address this limitation, we propose a diversity-guided kernel fuzzer SyzDiversity. Specifically, to mitigate overvaluation of early seeds, SyzDiversity leverages proof-of-concept (PoC) seeds derived from real-world vulnerabilities as initial seeds, and further partitions these seeds into multiple communities. Moreover, to improve diversity guidance in seed scheduling, it leverages a novel metric, community popularity rate (CPR), to model community diversity, and introduces a CPR-aware hierarchical Multi-Armed Bandit (MAB) algorithm that integrates CPR and code coverage as reward signals to prioritize the scheduling of diverse seed communities and seeds. Further, to efficiently populate sparse communities or break through community boundaries, it adopts a CPR-guided seed mutation strategy that adaptively allocates higher mutation frequencies to communities that are more conducive to the diversity evolution of the seeds. Our extensive experiments on Linux kernel versions v5.15 and v6.14 has demonstrated that SyzDiversity improves code coverage and bug-finding capability by 17.4% and 9.1×, respectively, compared to the state-of-the-art kernel fuzzers. It has discovered 32 unique new vulnerabilities, with 12 of them confirmed.


## 26. Testing Computation Pushdown in Distributed Database Systems

**Authors:** Jinsheng Ba (The Chinese University of Hong Kong, Shenzhen), Zuming Jiang (The University of Hong Kong, Hong Kong SAR China), Zhendong Su (ETH Zurich)

**Categories:** Testing and Fuzzing

**中文总结:** CPE（Controlled Pushdown Execution）通过白盒禁止特定下推算子并对比执行结果，系统验证分布式 DBMS 的计算下推正确性。在 CockroachDB、TiDB、YugabyteDB 上发现 25 个未知 bug（14 个逻辑错误），为历史 bug 数的 3× 且可复现全部历史 bug。

**Abstract:** Computation pushdown is a critical technique in distributed database management systems (DBMSs), enabling certain operations to be executed closer to the data to reduce network overhead and improve performance. However, its behavior depends on multiple factors beyond the input query itself, such as data distribution and resource utilization. This makes it difficult to validate correctness using only input queries in a black-box manner. Existing testing methods that rely solely on query manipulation cannot effectively control or predict pushdown behavior, and are therefore insufficient. In this paper, we introduce \emph{Controlled Pushdown Execution (CPE)}, a white-box method that enables systematic validation of computation pushdown. CPE modifies the source code of DBMSs to forbid a specific pushdown operator and compares the results. Any discrepancy reveals a bug. Our study shows that CPE can control all supported operators across different systems. We applied CPE to three production-grade distributed DBMSs: CockroachDB, TiDB, and YugabyteDB. CPE found 25 previously unknown and unique bugs, 14 of which are logic bugs—incorrect results. CPE finds 3$\times$ more bugs than historical bugs and can reproduce all historical bugs. Beyond computation pushdown, the core insight of controllable execution can generalize to other contexts (\emph{e.g.}, transaction schedule), providing a systematic way to uncover subtle logic bugs.


## 27. Testing Method Relocation Algorithms via Template-Based Systematic Structural Traversal and Precondition Filtering

**Authors:** Chunhao Dong (Beijing Institute of Technology), Yanjie Jiang (Tianjin University), Yang Zhang (Hebei University of Science and Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** Testing and Fuzzing

**中文总结:** RelocTest 结合模板驱动结构遍历与 LLM 引导补全生成方法搬迁测试用例，并用 LLM 前置条件提取器剪枝无效用例。在 7 个主流重构引擎上发现 56 个未知 bug，其中 19 个已获厂商确认。

**Abstract:** Method relocation refactorings, primarily Move Method and Pull Up/Push Down Method, are indispensable for reducing coupling and enhancing cohesion. Despite their widespread automation in modern refactoring engines, these algorithms remain notoriously error-prone, posing significant risks to software reliability. A primary challenge in testing them lies in the vast search space of complex program structures and the intricate preconditions required for safe method relocation. To address this, we propose \textsc{RelocTest}, a comprehensive testing framework that combines template-driven structural traversal with automated precondition filtering. \textsc{RelocTest}  systematically explores the input space by populating  program templates specially designed for method relocation through a two-stage generation process: (1) \textit{Skeleton Synthesis}, which systematically traverses diverse syntactic structures, and (2) \textit{LLM-Guided Completion}, which leverages Large Language Models to inject diverse, executable code into these skeletons. This hybrid strategy ensures high structural coverage while maintaining test case validity. Furthermore, to optimize testing efficiency, we introduce an \textit{LLM-based Precondition Extractor} that analyzes the implementation of method relocation algorithms to identify and prune test cases destined for rejection. We evaluated \textsc{RelocTest}  on 7 mainstream refactoring engines. Our approach successfully uncovered 56 previously unknown bugs, with 19 already confirmed by tool vendors, demonstrating its effectiveness in hardening industrial-strength refactoring tools.


## 28. Testing Static Taint Analyzers with Equivalence Modulo Taint

**Authors:** Maria Christakis (TU Wien), Anastasia Isychev (TU Wien), Samuel Pilz (TU Wien), Florian Tesarek (TU Wien), Valentin Wüstholz (ConsenSys)

**Categories:** Testing and Fuzzing

**中文总结:** EMT（Equivalence Modulo Taint）以源-汇流一致性定义程序等价，TaintCC 据此生成等价变体测试单个静态污点分析器。在 FlowDroid、Mariana Trench、Pysa、Semgrep 上发现 16 个唯一 bug，无需 ground-truth 标注。

**Abstract:** Static taint analyzers are widely used to detect security vulnerabilities, yet their complexity makes them prone to soundness and precision bugs. Validating these analyzers is challenging because ground-truth taint flows are rarely available and differential testing requires multiple comparable tools.  To address this challenge, we introduce Equivalence Modulo Taint (EMT), a testing oracle for static taint analysis that defines program equivalence in terms of preserved source-sink flows rather than full program semantics. EMT enables testing a single analyzer without ground-truth labels by checking consistency of reported flows across equivalent-modulo-taint program variants. Based on EMT, we present TaintCC, a framework that generates equivalent-modulo-taint variants through semantically equivalent, taint-oblivious, and taint-aware transformations targeting common sources of taint-analysis bugs. We evaluate TaintCC on four widely used analyzers—FlowDroid, Mariana Trench, Pysa, and Semgrep—and discover 16 unique bugs, demonstrating that even mature analyzers, whether academic or industrial, remain susceptible to reliability issues.


## 29. Uncovering Business Logic Bugs via Semantics-Driven Unit Test Generation (Experience Paper)

**Authors:** Chen Yang (Tianjin University), Junjie Chen (Tianjin University)

**Categories:** Testing and Fuzzing

**中文总结:** SeGa 从产品需求文档构建语义知识库，检索功能条目并推导细粒度业务场景引导 LLM 生成单元测试以暴露业务逻辑 bug。在 4 个工业 Go 项目 60 个真实 bug 上比 4 种 LLM 方法多检出 22–25 个，生产部署另发现 16 个已确认 bug。

**Abstract:** Business logic bugs violate intended business semantics and are particularly prevalent in enterprise software. Yet most existing unit test generation techniques are code-centric, making such bugs difficult to expose. We present SeGa, a semantics-driven unit test generation technique for uncovering business logic bugs. SeGa constructs a semantic knowledge base from product requirement documents, represented as a set of functionality entries that group related requirements under a common business intent. Given a focal method, SeGa retrieves the relevant functionality entries and derives fine-grained business scenarios with explicit preconditions, triggering actions, expected outcomes, and semantic constraints to guide LLM-based test generation. We evaluate SeGa on four industrial Go projects containing 60 real-world business logic bugs. SeGa detects 22~25 more bugs than four state-of-the-art LLM-based techniques and improves precision by 26.9%~34.3%. Deployment across 6 production repositories further uncovers 16 previously unknown business logic bugs that were confirmed and fixed by developers, demonstrating SeGa’s practical value. From our industrial study, we summarize a series of lessons and suggestions for practical use and future research.


## 30. WASCII: Bridging WebAssembly Specifications and Implementations through LLM-Enhanced Validation

**Authors:** Yeqi Fu (National University of Singapore), Kaihang Ji (National University of Singapore), Yuanpeng Wang (Peking University), Zong Cao (Imperial Global Singapore), Jiahao Liu (National University of Singapore), Ding Li (Peking University), Yao Guo (Peking University), Zhenkai Liang (National University of Singapore)

**Categories:** Testing and Fuzzing

**中文总结:** WASCII 从 Wasm 自然语言规范构建 Check Tree，对齐运行时源码并经 Clean Room 执行验证后做跨运行时差分测试。在 7 个主流运行时上发现 209 处行为差异，33 个为未知规范一致性问题（18 个已修复）。

**Abstract:** The rapid evolution of WebAssembly (Wasm) has led to significant implementation inconsistencies between its specification and the behavior of various Wasm runtimes, posing critical threats to application reliability and security. Verifying that a runtime’s implementation adheres to the natural-language specification is a profound challenge. While Large Language Models (LLMs) offer a promising way to bridge the semantic gap between specification text and source code, their inherent fallibility makes them untrustworthy for direct verification.

In this paper, we introduce WASCII, a novel framework for bridging specification and implementation with execution-based validation. Our approach first constructs a Check Tree from the natural-language specification, which captures the validation rules that runtimes must enforce. We then align runtime code to the Check Tree, and employ a Clean Room design with execution-based validation to ensure the correctness of the bridging. The validated test cases are then used for cross-runtime differential testing to identify behavioral inconsistencies. Evaluated on seven major Wasm runtimes, WASCII identified 209 differential behaviors, among which 33 are confirmed as previously unknown specification conformance issues, with 18 already fixed by developers. These results demonstrate that our approach is a highly effective strategy for discovering subtle yet critical bugs in complex systems.


## 31. WITFuzz: Validity-Preserving Greybox Fuzzing for WebAssembly Interface Type Binding Generators

**Authors:** Hanqin Guan (Peking University), Ningyu He (Hong Kong Polytechnic University, Hong Kong SAR China), Shangtong Cao (Beijing University of Posts and Telecommunications), Yifeng Cai (Peking University; Beijing Tongming Lake Information Technology Application Innovation Center), Yao Guo (Peking University), Ding Li (Peking University)

**Categories:** Testing and Fuzzing

**中文总结:** WITFuzz 对 WIT AST 做结构感知有效性保持变异，并以覆盖率引导的 LLM 策略合成扩展变异池，配合多层构建 oracle 检测 bindgen 两阶段构建破坏。在 12 个 bindgen 上发现 40 个未知 bug（35 个为基线未检出）。

**Abstract:** In the WebAssembly component model, interfaces written in WebAssembly Interface Types (WIT) are packaged and consumed as build-time dependencies, and binding generators (bindgens) translate them into language-specific bindings. Although a WIT package can be spec-valid, it can still break builds—by crashing or timing out during bindgen execution (Phase I), or by causing downstream toolchains to reject the generated bindings after generation appears to succeed (Phase II). Testing bindgens at scale is challenging because WIT is strongly typed and constraint-rich, and Phase II failures require language-specific checking.

We present WITFuzz, a validity-preserving greybox fuzzer for WIT bindgens. WITFuzz mutates resolved WIT abstract syntax trees via structure-aware rewrites expressed in a small domain-specific language, and propagates correlated updates to maintain WIT validity. To overcome coverage plateaus, WITFuzz expands its strategy pool online using coverage-guided, LLM-assisted synthesis, admitting only strategies that pass local validation. WITFuzz further uses a build-aware, multi-layer oracle that combines in-loop checks with selective asynchronous compilation/typechecking of generated bindings to capture non-crashing build breakers. Across 12 bindgens, WITFuzz achieves the highest coverage and uncovers 40 previously unknown Phase I and Phase II build-breaking bugs, including 35 missed by all baselines.

