# ISSTA 2025 Research Track — Testing and Fuzzing

Source: https://conf.researchr.org/track/issta-2025/issta-2025-papers#event-overview

Count: 30

## 1. A Large-scale Empirical Study on Fine-tuning Large Language Models for Unit Testing

**Authors:** ye shang (Nanjing University), Quanjun Zhang (School of Computer Science and Engineering, Nanjing University of Science and Technology), Chunrong Fang (Nanjing University), Siqi Gu (Nanjing University), Jianyi Zhou (Huawei Cloud Computing Technologies Co., Ltd.), Zhenyu Chen (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728951

**中文总结:** 对 37 个 LLM 在测试生成、断言生成与测试演化三类单元测试任务上进行大规模微调实证（5 个基准、8 项指标、超 3000 A100 GPU 小时）。微调 LLM 在几乎全部指标上优于现有 SOTA，大规模 decoder-only 模型整体最佳，prompt engineering 也展现出可观潜力，并给出数据泄露、缺陷检出与评测指标等实践指南。

**Abstract:** Unit testing plays a pivotal role in software development, improving software quality and reliability. However, generating effective test cases manually is time-consuming, prompting interest in unit testing research. Recently, Large Language Models (LLMs) have shown potential in various unit testing tasks, including test generation, assertion generation, and test evolution, but existing studies are limited in scope and lack a systematic evaluation of the effectiveness of LLMs.

To bridge this gap, we present a large-scale empirical study on fine-tuning LLMs for unit testing. Our study involves three unit testing tasks, five benchmarks, eight evaluation metrics, and 37 popular LLMs across various architectures and sizes, consuming over 3,000 NVIDIA A100 GPU hours. We focus on three key research questions: (1) the performance of LLMs compared to state-of-the-art methods, (2) the impact of different factors on LLM performance, and (3) the effectiveness of fine-tuning versus prompt engineering. Our findings reveal that LLMs outperform existing state-of-the-art approaches on all three unit testing tasks across nearly all metrics, highlighting the potential of fine-tuning LLMs in unit testing tasks. Furthermore, large-scale, decoder-only models achieve the best results across tasks, while encoder-decoder models perform better under the same parameter scale. Additionally, the comparison of the performance between fine-tuning and prompt engineering approaches reveals the considerable potential capability of the prompt engineering approach in unit testing tasks. We then discuss the concerned issues on the test generation task, including data leakage issues, bug detection capabilities, and metrics comparisons. Finally, we further pinpoint carious practical guidelines for LLM-based approaches to unit testing tasks in the near future. Overall, our work demonstrates the promising future of fine-tuning LLMs on unit testing tasks and reduces the manual efforts of unit testing experts in practical scenarios.

## 2. Are Autonomous Web Agents good testers?

**Authors:** Antoine Chevrot (Smartesting), Alexandre Vernotte (Smartesting), Jean-Rémy Falleri (Univ. Bordeaux, CNRS, Bordeaux INP, LaBRI, UMR 5800, Institut Universitaire de France), Xavier Blanc (Université de Bordeaux), Bruno Legeard (Université de Bourgogne Franche-Comté and Smartesting), Aymeric Cretin (Smartesting)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728879

**中文总结:** 研究将 Autonomous Web Agents（AWA）适配为 Autonomous Test Agents（ATA）执行端到端 Web 测试的可行性，提供适配框架、含 3 个应用 100 条用例的基准及实证评估。AWA 能部分自主复现测试场景，但在断言与错误处理上存在明显短板，尚难完全替代维护成本高的脚本化自动化或人工测试。

**Abstract:** Despite advances in automated testing, manual testing remains prevalent due to the high maintenance demands associated with test script fragility—scripts often break with minor changes in application structure. Recent developments in Large Language Models (LLMs) offer a potential alternative by powering Autonomous Web Agents (AWAs) that can autonomously interact with applications. These agents may serve as Autonomous Test Agents (ATAs), potentially reducing the need for maintenance-heavy automated scripts by utilising natural language instructions similar to those used by human testers.

This paper investigates the feasibility of adapting AWAs for end-to-end test execution. We contribute with (1) an adaptation framework transforming a well-known AWA into an ATA and analysing which modules support autonomous testing, (2) a benchmark of three web applications and a suite of 100 test cases, including both passing and mutated failing cases, to evaluate ATA performance, and (3) an empirical evaluation that quantifies ATA efficacy and identifies core limitations in autonomous testing agents.

Our findings reveal that while AWAs show promising results in replicating some test scenarios autonomously, limitations in handling assertions and errors indicate that further advancements are necessary before ATAs can fully replace manual testing. This work provides insights for developing more resilient and reliable autonomous testing systems, paving the way for robust, maintenance-free test automation.

## 3. AudioTest: Prioritizing Audio Test Cases

**Authors:** Yinghua Li (University of Luxembourg), Xueqi Dang (University of Luxembourg, SnT), Wendkuuni Arzouma Marc Christian OUEDRAOGO (University of Luxembourg), Jacques Klein (University of Luxembourg), Tegawendé F. Bissyandé (University of Luxembourg)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728907

**中文总结:** 针对音频分类测试人工标注成本高，提出专用测试优先级方法 AudioTest：融合时域、频域、感知与模型输出四类特征，并通过特征变换使易错样本在空间中更靠近以排序。在 96 个主体、自然与含噪数据集上，PFD/APFD 均优于基线，平均提升 12%–55%。

**Abstract:** Audio classification systems, powered by deep neural networks (DNNs), are integral to various applications that impact daily lives, like voice-activated assistants. Ensuring the accuracy of these systems is crucial since inaccuracies can lead to significant security issues and user mistrust. However, testing audio classifiers presents a significant challenge: the high manual labeling cost for annotating audio test inputs. Test input prioritization has emerged as a promising approach to mitigate this labeling cost issue. It prioritizes potentially misclassified tests, allowing for the early labeling of such critical inputs and making debugging more efficient. However, when applying existing test prioritization methods to audio-type test inputs, there are some limitations: 1) Coverage-based methods are less effective and efficient than confidence-based methods. 2) Confidence-based methods rely only on prediction probability vectors, ignoring the unique characteristics of audio-type data. 3) Mutation-based methods lack designed mutation operations for audio data, making them unsuitable for audio-type test inputs. To overcome these challenges, we propose AudioTest, a novel test prioritization approach specifically designed for audio-type test inputs. The core premise is that tests closer to misclassified samples are more likely to be misclassified. Based on the special characteristics of audio-type data, AudioTest generates four types of features: time-domain features, frequency-domain features, perceptual features, and output features. For each test, AudioTest concatenates its four types of features into a feature vector and applies a carefully designed feature transformation strategy to bring misclassified tests closer in space. AudioTest leverages a trained model to predict the probability of misclassification of each test based on its transformed vectors and ranks all the tests accordingly. We evaluate the performance of AudioTest utilizing 96 subjects, encompassing natural and noisy datasets. We employed two classical metrics, Percentage of Fault Detection (PFD) and Average Percentage of Fault Detected (APFD), for our evaluation. The results demonstrate that AudioTest outperforms all the compared test prioritization approaches in terms of both PFD and APFD. The average improvement of AudioTest compared to the baseline test prioritization methods ranges from 12.63% to 54.58% on natural datasets and from 12.71% to 40.48% on noisy datasets.

## 4. Automated Test Transfer Across Android Apps Using Large Language Models

**Authors:** Benyamin Beyzaei (UC Irvine), Saghar Talebipour (University of Southern California), Ghazal Rafiei (University of Southern California), Nenad Medvidović (University of Southern California), Sam Malek (University of California at Irvine)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728975

**中文总结:** 提出 LLMigrate，利用 LLM 在 Android 应用间迁移基于使用的 UI 端到端测试，应对源/目标应用差异大及 oracle 迁移不准等问题。实验显示迁移成功率 97.5%，相对从零编写减少 91.1% 人工，较最佳 prior 成功率提升 9.1%、工作量再降 38.2%。

**Abstract:** The pervasiveness of mobile apps in everyday life necessitates robust testing strategies to ensure quality and efficiency, especially through end-to-end usage-based tests for mobile apps’ user interfaces (UIs). However, manually creating and maintaining such tests can be costly for developers. Since many apps share similar functionalities beneath diverse UIs, previous works have shown the possibility of transferring UI tests across different apps within the same domain, thereby eliminating the need for writing the tests manually. However, these methods have struggled to accommodate real-world variations, often facing limitations in scenarios where source and target apps are not very similar or fail to accurately transfer test oracles. This paper introduces an innovative technique, LLMigrate, which leverages Large Language Models (LLMs) to efficiently transfer usage-based UI tests across mobile apps. Our experimental evaluation shows LLMigrate can achieve a 97.5% success rate in automated test transfer, reducing the manual effort required to write tests from scratch by 91.1%. This represents an improvement of 9.1% in success rate and 38.2% in effort reduction compared to the best-performing prior technique, setting a new benchmark for automated test transfer.

## 5. Detecting Isolation Anomalies in Relational DBMSs

**Authors:** Rui Yang (Institute of Software, Chinese Academy of Sciences), Ziyu Cui (Institute of Software at Chinese Academy of Sciences), Wensheng Dou (Institute of Software Chinese Academy of Sciences), Yu Gao (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Jiansen Song (Institute of Software at Chinese Academy of Sciences), Xudong Xie (Institute of Software Chinese Academy of Sciences, China), Jun Wei (Institute of Software at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728953

**中文总结:** 提出黑盒隔离检查器 IsoRel：用隔离无关的 SQL 插桩记录行访问，构建关系型事务依赖图并匹配 Adya 异常模式。在 MySQL、PostgreSQL、MariaDB、CockroachDB、TiDB 各隔离级别上共检出 48 种违反声明隔离级别的独特异常。

**Abstract:** Relational Database Management Systems (DBMSs) utilize transactions to ensure data consistency and integrity, while providing multiple isolation levels to strike a balance between consistency and performance. However, isolation anomalies in relational DBMSs can undermine their claimed isolation levels, and lead to severe consequences, e.g., incorrect query results and database states. Existing isolation checkers can only work on simple 𝑘𝑒𝑦-𝑣𝑎𝑙𝑢𝑒-like data models and the associated 𝑟𝑒𝑎𝑑 (𝑘𝑒𝑦) and 𝑤𝑟𝑖𝑡𝑒 (𝑘𝑒𝑦, 𝑣𝑎𝑙𝑢𝑒) operations. Therefore, they cannot be directly applied to relational DBMSs that support relational data models and complex SQL operations. In this paper, we propose a novel black-box Isolation checker for Relational DBMSs, IsoRel, which can support relational data models and complex SQL operations. To infer dependencies among transactions in relational DBMSs, we first design an isolation-agnostic SQL instrumentation approach to record the data rows accessed by each SQL statement by utilizing two auxiliary columns in each database table. We then utilize the recorded data rows of each SQL statement to construct a transaction dependency graph for relational transactions, and identify isolation anomalies based on anomaly patterns. We evaluate IsoRel on five widely-used relational DBMSs, i.e., MySQL, PostgreSQL, MariaDB, CockroachDB, and TiDB, and all their supported isolation levels. Our evaluation reveals a total of 48 unique isolation anomalies that violate the isolation levels defined by Adya.

## 6. Effective REST APIs Testing with Error Message Analysis

**Authors:** Lixin Xu (Nanjing University, China), Huayao Wu (Nanjing University), Zhenyu Pan, Tongtong Xu (Huawei), Shaohua Wang (Central University of Finance and Economics), Xintao Niu (Nanjing University), Changhai Nie (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728964

**中文总结:** EmRest 黑盒测试 REST API：组合采样参数赋值策略，统计 4xx/5xx 错误信息推断输入约束与异常场景并分配测试资源。16 个真实 API 上半数覆盖率优于 SOTA，并独有发现 226 个 bug。

**Abstract:** REST APIs are essential in building modern enterprise systems, while effectively examining their behaviors remains challenging due to the difficulty in inferring constraints from the specifications. To generate valid test inputs for REST APIs, existing approaches are typically feedback-driven, leveraging HTTP status codes received to guide further test input generation. However, these approaches overlook the potentially valuable information described in error messages accompanying HTTP status codes, leading to inefficiencies in exploring the input space of REST APIs. In this paper, we propose EmRest, a black-box testing approach that leverages error message analysis to enhance both valid and exceptional test input generation for REST APIs. For each operation under test, EmRest first identifies all possible value assignment strategies for each of its input parameters. It then repeatedly applies combinatorial testing to sample test inputs based on these strategies, and statistically analyzes the error messages (of 400-range status code) received to infer and exclude invalid combinations of value assignment strategies (i.e., constraints of the input space). Additionally, EmRest seeks to mutate valid value assignment strategies that are finally identified to generate test inputs for exceptional testing. The error messages (of 500-range status code) received are categorized to identify bug-prone operations, for which more testing resources are allocated. Our experimental results on 16 real-world REST APIs demonstrates the effectiveness of EmRest. It achieves higher operation coverage than state-of-the-art approaches in 50% of APIs, and detects 226 unique bugs that cannot be found by the other approaches.

## 7. FANDANGO: Evolving Language-Based Testing

**Authors:** José Antonio Zamudio Amaya (CISPA Helmholtz Center for Information Security), Marius Smytzek (CISPA Helmholtz Center for Information Security), Andreas Zeller (CISPA Helmholtz Center for Information Security)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728915

**中文总结:** FANDANGO 用遗传算法替代 ISLa 的符号约束求解，在形式化输入规范下进化生成满足语义约束的测试输入，并允许用完整 Python 表达约束。实验显示其比 ISLa 快一到三个数量级，且精度不降。

**Abstract:** Language-based fuzzers leverage formal input specifications ( languages ) to generate arbitrarily large and diverse sets of valid inputs for a program under test. Modern language-based test generators combine grammars and constraints to satisfy syntactic and semantic input constraints. ISLa, the leading input generator in that space, uses symbolic constraint solving to solve input constraints. Using solvers places ISLa among the most precise fuzzers but also makes it slow.

In this paper, we explore search-based testing as an alternative to symbolic constraint solving. We employ a genetic algorithm that iteratively generates candidate inputs from an input specification, evaluates them against defined constraints, evolving a population of inputs through syntactically valid mutations and retaining those with superior fitness until the semantic input constraints are met. This evolutionary procedure, analogous to natural genetic evolution, leads to progressively improved inputs that cover both semantics and syntax. This change boosts the efficiency of language-based testing: In our experiments, compared to ISLa, our search-based FANDANGO prototype is faster by one to three orders of magnitude without sacrificing precision.

The search-based approach no longer restricts constraints to constraint solvers’ (miniature) languages. In FANDANGO, constraints can use the whole Python language and library . This expressiveness gives testers unprecedented flexibility in shaping test inputs. It allows them to state arbitrary goals for test generation : “Please produce 1,000 valid test inputs where the voltage field follows a Gaussian distribution but never exceeds 20 mV.”

➡️ Watch our teaser at https://www.youtube.com/watch?v=JXMk-XhuKPY

➡️ See the press release at https://cispa.de/en/fandango-release

➡️ Read our paper at https://dl.acm.org/doi/10.1145/3728915

and, of course,

➡️ Check out Fandango at https://fandango-fuzzer.github.io/

## 8. FreeWavm: Enhanced WebAssembly Runtime Fuzzing Guided by Parse Tree Mutation and Snapshot

**Authors:** Peng Qian (Zhejiang University), Xinlei Ying (Ant Group), Jiashui Wang (Zhejiang University), Long Liu (Ant Group), Lun Zhang (GoPlus Security), Jianhai Chen (Zhejiang University), Qinming He (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728877

**中文总结:** FreeWavm 将 WebAssembly 字节码转为解析树，按结构感知策略变异并自动修复，再结合快照加速进化式 fuzzing。在多个 Wasm runtime 上发现 69 个未知缺陷（24 个已分配 CVE），结构相关崩溃触发能力优于现有方法。

**Abstract:** WebAssembly, recognized as a low-level and portable language, has been widely embraced in areas as diverse as browsers and blockchains, emerging as a revolutionary force for Internet evolution. Unfortunately, defects and flaws in WebAssembly runtimes bring about unexpected results when running WebAssembly applications. A family of solutions have been proposed to detect vulnerabilities in WebAssembly runtimes, with fuzzing emerging as the most promising and persuasive approach. Despite its potential, fuzzing faces significant challenges due to the grammatical complexity of WebAssembly runtimes, which lacks an in-depth understanding of the unique module-based code structure and thus generates test inputs that struggle to tap into the deep logic within a WebAssembly runtime, limiting its effectiveness in unveiling vulnerabilities.

To bridge this gap, we introduce FreeWavm, a novel framework for fuzzing WebAssembly runtimes by aggressively mutating the structure of WebAssembly code. Technically, we transform the WebAssembly bytecode into a parse tree format that captures complex characteristics of code structure. To generate meaningful test inputs for WebAssembly runtime fuzzing, we design a structure aware mutation module that engages in a customized node prioritization strategy to screen out interesting nodes in the parse tree, and then applies specific structure mutations. To ensure the validity of the mutated test inputs, FreeWavm is equipped with an automated repair mechanism to patch the mutated parse tree. Furthermore, we take advantage of parse tree snapshots to facilitate input evolution and the overall fuzzing process. Extensive experiments are conducted to evaluate FreeWavm on multiple WebAssembly runtimes. Empirical results show that FreeWavm effectively triggers structure-specific crashes in WebAssembly runtimes, outperforming other counterparts. FreeWavm has identified 69 previously unknown bugs, 24 of which are assigned CVEs thus far.

## 9. GoPV: Detecting Blocking Concurrency Bugs Related to Shared-Memory Synchronization in Go

**Authors:** Wei Song (Nanjing University of Science and Technology), Xiaofan Xu (Nanjing University of Science and Technology), Jeff Huang (Texas A&M University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728979

**中文总结:** GoPV 通过静态并发分析与（后）支配关系分析，检测 Go 共享内存同步原语误用导致的死锁、goroutine 泄漏等阻塞型并发缺陷。在 8 个基准上全命中，并在 21 个大型项目中 2.78 小时内发现 17 个真实 bug。

**Abstract:** Go is a popular concurrent programming language that employs both message-passing and shared-memory synchronization primitives for interaction between different threads known as goroutines. However, the misuse of the synchronization primitives can easily lead to blocking concurrency bugs, including deadlocks, goroutine leaks. While blocking concurrency bugs related to message passing have received increasing attention, little work focuses on the blocking concurrency bugs caused by the misuse of shared-memory synchronization primitives. In this paper, we present GoPV, a static analyzer and an open-source tool, which performs concurrency analysis and (post-)dominator analysis to determine blocking concurrency bugs by ascertaining whether the synchronization primitives are misused. We evaluate GoPV on eight benchmark programs and 21 large real-world Go projects. The experimental results demonstrate that GoPV not only successfully detects all blocking concurrency bugs related to shared-memory synchronization in the eight benchmark programs, but also discovers 17 such bugs in the 21 large Go applications within 2.78 hours.

## 10. GUIPilot: A Consistency-based Mobile GUI Testing Approach for Detecting Application-specific Bugs

**Authors:** Ruofan Liu (Shanghai Jiao Tong University; National University of Singapore), Xiwen Teoh (National University of Singapore), Yun Lin (Shanghai Jiao Tong University), Guanjie Chen (Shanghai Jiao Tong University), Ruofei Ren (Shanghai Jiao Tong University), Denys Poshyvanyk (William & Mary), Jin Song Dong (National University of Singapore)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728909

**中文总结:** GUIPilot 对比移动端设计稿与实现：屏幕层用部件对齐算法检测布局/位置偏差，流程层借助 vision-language model 的 visual prompt 推断操作并验证跳转。在 80 个应用、160 份设计稿上屏幕不一致检测精确率 94.5%、召回 99.6%，流程检测零误报。

**Abstract:** GUI testing is crucial for ensuring the reliability of mobile applications. State-of-the-art GUI testing approaches are successful in exploring more application scenarios and discovering \textit{general} bugs such as application crashes. However, industrial GUI testing also needs to investigate \textit{application-specific} bugs such as deviations in screen layout, widget position, or GUI transition from the GUI design mock-ups created by the application designers. These mock-ups specify the expected screens, widgets, and their respective behaviors. Validating the consistency between the GUI design and the implementation is labor-intensive and time-consuming, yet, this validation step plays an important role in industrial GUI testing.

In this work, we propose GUIPilot, an approach for detecting inconsistencies between the mobile design and their implementations. The mobile design usually consists of design mock-ups that specify (1) the expected screen appearances (e.g., widget layouts, colors, and shapes) and (2) the expected screen behaviors, regarding how one screen can transition into another (e.g., labeled widgets with textual description). Given a design mock-up and the implementation of its application, GUIPilot reports both their screen inconsistencies as well as process inconsistencies. On the one hand, GUIPilot detects the screen inconsistencies by abstracting every screen into a widget container where each widget is represented by its position, width, height, and type. By defining the partial order of widgets and the costs of replacing, inserting, and deleting widgets in a screen, we convert the screen-matching problem into an optimizable widget alignment problem. On the other hand, we translate the specified GUI transition into stepwise actions on the mobile screen (e.g., click, long-press, input text on some widgets). To this end, we propose a \textit{visual prompt} for the vision-language model to infer widget-specific actions on the screen. By this means, we can validate the presence or absence of expected transitions in the implementation. Our extensive experiments on 80 mobile applications and 160 design mock-ups show that (1) GUIPilot can achieve 94.5% precision and 99.6% recall in detecting screen inconsistencies, outperforming the state-of-the-art approach, such as GVT, by 66.2% and 56.6% respectively, and (2) GUIPilot reports zero errors in detecting process inconsistencies. Furthermore, our industrial case study on applying GUIPilot on a trading mobile application shows that GUIPilot has detected nine application bugs, and all the bugs were confirmed by the original application experts.

## 11. Intention-based GUI Test Migration for Mobile Apps using Large Language Models

**Authors:** Shaoheng Cao (Nanjing University), Minxue Pan (Nanjing University), Yuanhong Lan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728978

**中文总结:** ITeM 用 LLM 两阶段框架做移动端 GUI 测试迁移：先生成测试意图，再动态推理在目标 App 上完成操作，从而应对源/目标交互逻辑不一致。在 35 个 Android 应用、280 项迁移任务上效果与效率均优于基于 widget 匹配的现有方法。

**Abstract:** Graphical User Interface (GUI) testing is one of the primary quality assurance methods for mobile apps. Manually constructing high-quality test cases for GUI testing is costly and labor-intensive, leading to the development of various automated approaches that migrate test cases from a source app to a target app. Existing approaches predominantly treat this test migration task as a widget-matching problem, which performs well when the interaction logic between apps remains consistent. However, they struggle with variations in interaction logic for specific functionalities, a common scenario across different apps. To address this limitation, a novel approach named ITeM is introduced in this paper for the test migration task. Unlike existing works that model the problem as a widget-matching task, ITeM seeks a novel pathway by adopting a two-stage framework with the comprehension and reasoning capability of Large Language Models: first, a transition-aware mechanism for generating test intentions; and second, a dynamic reasoning-based mechanism for fulfilling these intentions. This approach maintains effectiveness regardless of variations across the source and target apps’ interaction logic. Experimental results on 35 real-world Android apps across 280 test migration tasks demonstrate the superior effectiveness and efficiency of ITeM compared to state-of-the-art approaches.

## 12. KEENHash: Hashing Programs into Function-aware Embeddings for Large-scale Binary Code Similarity Analysis

**Authors:** Zhijie Liu (ShanghaiTech University, China), Qiyi Tang (Tencent Security Keen Lab), Sen Nie (Tencent Security Keen Lab), Shi Wu (Tencent Security Keen Lab), Liangfeng Zhang (School of Information Science and Technology, ShanghaiTech University), Yutian Tang (University of Glasgow, United Kingdom)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728911

**中文总结:** KEENHash 用 LLM 生成函数级 embedding，经 K-Means 与 Feature Hashing 压缩为固定长度程序向量，实现可扩展的程序级二进制相似度分析。比最新函数级匹配工具快 215 倍；53 亿次相似度评估仅需 395.83 秒，大规模克隆检索与恶意软件检测均显著优于 4 种 SOTA。

**Abstract:** Binary code similarity analysis (BCSA) is a crucial research area in many fields such as cybersecurity. Specifically, function-level diffing tools are the most widely used in BCSA: they perform (similar) function matching one by one for evaluating the similarity between binary programs (binaries). However, such methods need a high time complexity, making it unscalable in large-scale scenarios (e.g., 1/n-to-n searching). Towards effective and efficient program-level BCSA, we propose KEENHash, a novel hashing approach that hashes binaries into program-level representations through large language model (LLM)-generated function embeddings. KEENHash condenses a binary into one compact and fixed-length program embedding using K-Means and Feature Hashing, allowing us to do effective and efficient large-scale program-level BCSA, surpassing the previous state-of-the-art methods. The experimental results show that KEENHash is 215 times faster than the state-of-the-art function matching tool while maintaining effectiveness. Furthermore, in a large-scale scenario with 5.3 billion similarity evaluations, KEENHash takes only 395.83 seconds while the tool will cost 56 days. We also evaluate KEENHash on the program clone search of large-scale BCSA across extensive datasets in 202,305 binaries. Compared with 4 state-of-the-art methods, KEENHash outperforms all of them by at least 23.16%, and displays remarkable superiority over them in the large-scale BCSA security scenario of malware detection.

## 13. KRAKEN: Program-Adaptive Parallel Fuzzing

**Authors:** Anshunkang Zhou (Hong Kong University of Science and Technology), Heqing Huang (City University of Hong Kong), Charles Zhang (Hong Kong University of Science and Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728882

**中文总结:** KRAKEN 在并行 fuzzing 运行时依据覆盖率等反馈动态优化策略，逐程序逼近最优并行配置。相对 6 个 SOTA 并行 fuzzer，给定时间内覆盖率多 54.7%、缺陷多 70.2%；在 37 个开源项目中发现 192 个 bug，其中 119 个已获 CVE。

**Abstract:** Parallel fuzzing, which utilizes multicore computers to accelerate the fuzzing process, has been widely used in industrial-scale software defect detection. However, specifying efficient parallel fuzzing strategies for programs with different characteristics is challenging due to the difficulty of reasoning about fuzzing runtime statically. Existing efforts still use pre-defined tactics for various programs, resulting in suboptimal performance.

In this paper, we propose KraKen, a new program-adaptive parallel fuzzer that improves fuzzing efficiency through dynamic strategy optimization. The key insight is that the inefficiency in parallel fuzzing can be observed during runtime through various feedbacks, such as code coverage changes, which allows us to adjust the adopted strategy to avoid inefficient path searching, thus gradually approximating the optimal policy.  Based on the above insight, our key idea is to view the task of finding the optimal strategy as an optimization problem and gradually approach the best program-specific strategy on the fly by maximizing certain objective functions.  We have implemented Kraken in C/C++ and evaluated it on 19 real-world programs against 6 state-of-the-art parallel fuzzers. Experimental results show that Kraken can achieve 54.7% more code coverage and find 70.2% more bugs in the given time. Moreover, Kraken has found 192 bugs in 37 popular open-source projects, and 119 of them are assigned with CVE IDs.

## 14. MLLM-Based UI2Code Automation Guided by UI Layout Information

**Authors:** Fan Wu (Harbin Institute of Technology, Shenzhen), Cuiyun Gao (Harbin Institute of Technology), Shuqing Li (The Chinese University of Hong Kong), Xin-Cheng Wen (Harbin Institute of Technology), Qing Liao (Harbin Institute of Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728925

**中文总结:** 提出 MLLM 框架 LayoutCoder，通过元素关系构建、UI 布局树解析与布局引导代码融合，从真实网页截图生成结构保真的 UI 代码。新建含350个网站的 Snap2Code 基准，相较最优基线 BLEU 与 CLIP 平均分别提升10.14%和3.95%。

**Abstract:** Converting user interfaces into code (UI2Code) is a crucial step in website development, which is time-consuming and labor-intensive. The automation of UI2Code is essential to streamline this task, beneficial for improving the development efficiency. There exist deep learning-based methods for the task; however, they heavily rely on a large amount of labeled training data and struggle with generalizing to real-world, unseen web page designs. The advent of Multimodal Large Language Models (MLLMs) presents potential for alleviating the issue, but they are difficult to comprehend the complex layouts in UIs and generate the accurate code with layout preserved. To address these issues, we propose LayoutCoder, a novel MLLM-based framework generating UI code from real-world webpage images, which includes three key modules: (1) Element Relation Construction, which aims at capturing UI layout by identifying and grouping components with similar structures; (2) UI Layout Parsing, which aims at generating UI layout trees for guiding the subsequent code generation process; and (3) Layout-Guided Code Fusion, which aims at producing the accurate code with layout preserved. For evaluation, we build a new benchmark dataset which involves 350 real-world websites named Snap2Code, divided into seen and unseen parts for mitigating the data leakage issue, besides the popular dataset Design2Code. Extensive evaluation shows the superior performance of LayoutCoder over the state-of-the-art approaches. Compared with the best-performing baseline, LayoutCoder improves 10.14% in the BLEU score and 3.95%  in the CLIP score on average across all datasets.

## 15. Porting Software Libraries to OpenHarmony: Transitioning from TypeScript or JavaScript to ArkTS

**Authors:** Bo Zhou (Northeastern University), Jiaqi Shi (Northeastern University), Ying Wang (Northeastern University), Li Li (Beihang University), Li Tsz On (The Hong Kong University of Science and Technology), Hai Yu (Northeastern University, China), Zhiliang Zhu (Northeastern University, China)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728941

**中文总结:** 提出项目级自动移植工具 ArkAdapter，构建 ArkTS 适配知识库并以依赖结构与语法不匹配粒度确定适配优先级，配合 LLM few-shot 学习处理 TS/JS 到 ArkTS 的复杂语法交互。定位精度86.84%、召回100%，79库中70个（88.6%）通过 ArkCompiler 与 OpenHarmony 官方审核。

**Abstract:** OpenHarmony emerges as a potent force in the mobile app domain, poised to stand alongside established industry giants. ArkTS is its main language, enhancing TypeScript (TS) and JavaScript (JS) with strict typing for improved performance. Developers are encouraged to port popular TS/JS libraries to OpenHarmony, supported by detailed guidelines. However, this requires a deep understanding of ArkTS syntax, following porting specifications, and making manual changes. An automated solution is crucial to streamline this process and foster a robust software ecosystem.

As a new programming language, ArkTS currently lacks essential analysis tools for automated analysis and porting of software libraries. However, the rise of Large Language Models (LLMs) shows promise for effectively addressing automated porting tasks. There are two challenges in using LLMs to automate the porting of TS/JS libraries to OpenHarmony: (1) \emph{LLMs have limited exposure to ArkTS code, making it difficult for them to grasp the syntactical differences between ArkTS and JS/TS, as well as the various adaptation scenarios.} (2) \emph{Project-level code adaptation often involves correcting numerous syntax mismatches, which complicates matters for LLMs as they must handle the interactions between different mismatches and interdependent code.} In response, we introduce \texttt{ArkAdapter}, a project-level automatic code adaptation approach. \texttt{ArkAdapter} addresses \textit{Challenge 1} by establishing an adaptation knowledge repository for ArkTS syntax comprehension. It expands a collection of real code adaptation examples based on expert experience across various scenarios, improving the adaptation capabilities of LLMs through few-shot learning. \texttt{ArkAdapter} overcomes \textit{Challenge 2} based on an adaptation priority strategy by considering both the dependency structure and the granularity of syntax-mismatching code. This strategy helps prevent interference among various syntax mismatches and their interdependent code. Evaluation shows \texttt{ArkAdapter} achieves high precision (86.84%) and full recall rates (100%) in locating syntax-mismatching code. 80.14% code adaptions inferred by \texttt{ArkAdapter} with LLM exactly or plausibly match the actual adaptations made by OpenHarmony developers. We utilized \texttt{ArkAdapter} to port 79 widely-used TS/JS libraries. \textbf{70 ArkTS libraries (88.6%) were validated by \emph{ArkCompiler}, passed tests, and were approved by the reviewers of the OpenHarmony’s library central repository}, showcasing its potential to streamline the porting process and enhance the growth of the OpenHarmony software landscape.

## 16. Program Feature-based Benchmarking for Fuzz Testing

**Authors:** Miao Miao (The University of Texas at Dallas), Sriteja Kummita (Fraunhofer Institute for Mechatronic Systems Design (Fraunhofer IEM)), Eric Bodden (Heinz Nixdorf Institute at Paderborn University; Fraunhofer IEM), Shiyi Wei (University of Texas at Dallas)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728899

**中文总结:** 从25篇灰盒 fuzz 研究中提炼7个影响 fuzz 效果的控制流/数据流程序特征，构建 FeatureBench：153个程序、10个可配置细粒度参数。评估11个 fuzzer 表明，性能随程序特征及其强度显著变化，凸显特征感知评测的必要性。

**Abstract:** Fuzzing is a powerful software testing technique renowned for its effectiveness in identifying software vulnerabilities. Traditional fuzzing evaluations typically focus on overall fuzzer performance across a set of target programs, yet few benchmarks consider how fine-grained program features influence fuzzing effectiveness. To bridge this gap, we introduce FeatureBench, a novel benchmark designed to generate programs with configurable, fine-grained program features to enhance fuzzing evaluations. We reviewed 25 recent grey-box fuzzing studies, extracting 7 program features related to control-flow and data-flow that can impact fuzzer performance. Using these features, we generated a benchmark consisting of 153 programs controlled by 10 fine-grained configurable parameters. We evaluated 11 fuzzers using this benchmark, with each fuzzer representing either distinctly claimed improvements or serving as a widely used baseline in fuzzing evaluations. The results indicate that fuzzer performance varies significantly based on the program features and their strengths, highlighting the importance of incorporating program characteristics into fuzzing evaluations.

## 17. QTRAN: Extending Metamorphic-Oracle based Logical Bug Detection Techniques for Multiple-DBMS Dialect Support

**Authors:** Li Lin (Xiamen University), Qinglin Zhu (School of Informatics, Xiamen University), Hongqiao Chen (School of Informatics, Xiamen University), Zhuangda Wang (Xiamen University), Rongxin Wu (Xiamen University), Xiaoheng Xie (Ant Group)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728908

**中文总结:** 提出 LLM 驱动的 QTRAN，以 transfer 与 mutation 两阶段将现有 MOLT 自动扩展到8种 DBMS 方言，翻译并变异 SQL 对以满足 metamorphic relation。99%以上语句对有效，发现24个逻辑 bug，其中16个为唯一新缺陷。

**Abstract:** Metamorphic testing is a widely used method to detect logical bugs in Database Management Systems (DBMSs), referred to herein as MOLT (Metamorphic-Oracle based Logical Bug Detection Techinique). This technique involves constructing SQL statement pairs, including original and mutated queries, and assessing whether the execution results conform to predefined metamorphic relations to detect logical bugs. However, current MOLTs rely heavily on specific DBMS grammars to generate valid SQL statement pairs, which makes it challenging to adapt these techniques to various DBMSs with different grammatical structures. As a result, only a few popular DBMSs, such as PostgreSQL, MySQL, and MariaDB, are supported by existing MOLTs, with extensive manual effort required to expand to other DBMSs. Given that many DBMSs remain inadequately tested, there is a pressing need for a method that enables effortless extension of MOLTs across diverse DBMSs.

In this paper, we propose QTRAN, a novel LLM-powered approach that automatically extends existing MOLTs to various DBMSs. Our key insight is to translate SQL statement pairs to target DBMSs for metamorphic testing from existing MOLTs using LLMs. To address the challenges of LLMs’ limited understanding of dialect differences and metamorphic mechanisms, we propose a two-phase approach comprising the transfer and mutation phases. QTRAN tackles these challenges by drawing inspiration from the developer’s process of creating a MOLT, which includes understanding the grammar of the target DBMS to generate original queries and employing a mutator for customized mutations. The transfer phase is designed to identify potential dialects and leverage information from SQL documents to enhance query retrieval, enabling LLMs to translate original queries across different DBMSs accurately. During the mutation phase, we gather SQL statement pairs from existing MOLTs to fine-tune the pretrained model, tailoring it specifically for mutation tasks. Then we employ the customized LLM to mutate the translated original queries, preserving the defined relationships necessary for metamorphic testing.

We implement our approach as a tool and apply it to extend four state-of-the-art MOLTs for eight DBMSs: MySQL, MariaDB, TiDB, PostgreSQL, SQLite, MonetDB, DuckDB, and ClickHouse. The evaluation results show that over 99% of the SQL statement pairs transfered by QTRAN satisfy the metamorphic relations required for testing. Furthermore, we have detected 24 logical bugs among these DBMSs, with 16 confirmed as unique and previously unknown bugs. We believe that the generality of QTRAN can significantly enhance the reliability of DBMSs.

## 18. Quantum Concolic Testing

**Authors:** Shangzhou Xia (Kyushu University), Jianjun Zhao (Kyushu University), Fuyuan Zhang (Kyushu University), Xiaoyu Guo (Kyushu University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728926

**中文总结:** 提出首个面向量子程序的 concolic 测试框架，为量子控制语句生成路径约束、符号化量子变量，并集成量子约束求解器与 Qiskit 引导新输入探索。实验显示可提升分支覆盖率、生成高质量量子输入并有效检测 bug。

**Abstract:** This paper presents the first concolic testing framework explicitly designed for quantum programs. The framework introduces quantum constraint generation methods for quantum control statements that quantify quantum states and offers a symbolization method for quantum variables. Based on this framework, we generate path constraints for each concrete execution path of a quantum program. These constraints guide the exploration of new paths, with a quantum constraint solver determining outcomes to create novel input samples, thereby enhancing branch coverage. Our framework has been implemented in Python and integrated with Qiskit for practical evaluation. Experimental results show that our concolic testing framework improves branch coverage, generates high-quality quantum input samples, and detects bugs, demonstrating its effectiveness and efficiency in quantum programming and bug detection.

## 19. REACCEPT: Automated Co-evolution of Production and Test Code Based on Dynamic Validation and Large Language Models

**Authors:** Jianlei Chi, Xiaotian Wang (Harbin Engineering University), Yuhan Huang (Xidian University), Lechen Yu (Microsoft), Di Cui (Xidian University), Jianguo Sun (Xidian University), Jun Sun (Singapore Management University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728930

**中文总结:** 提出 REACCEPT，结合 LLM、经验驱动提示模板、动态验证与 RAG，全自动完成生产代码与测试代码（PT）协同演化，既能识别也能更新过时测试。在 537 个 Java 项目上，对已识别过时测试的更新准确率达 60.16%，较 SOTA 方法 CEPROT 提升约 90%。

**Abstract:** Synchronizing production and test code, known as PT co-evolution, is critical for software quality in the software development lifecycle. Existing methods for automatic PT co-evolution either utilize predefined heuristic rules or rely on simple application of machine learning techniques. Due to the limitations of underlying techniques, existing methods either only partially automate PT co-evolution (e.g., only automate obsolete test code identification) or result in low accuracy.

In this paper, we propose REACCEPT, a novel approach that leverages large language models and dynamic validation to fully automate PT co-evolution (i.e., capable of both identifying and updating obsolete test cases). REACCEPT relies on experience-based prompt template generation, dynamic validation, and retrieval-augmented generation techniques to accomplish automated PT co-evolution. To evaluate REACCEPT’s effectiveness, we extensive experiments with a dataset of 537 Java projects and compared REACCEPT’s performance with several state-of-the-art methods. Results show that REACCEPT achieved an update accuracy of 60.16% on correctly identified obsolete test code, surpassing the state-of-the-art technique CEPROT by 90%. This confirms that REACCEPT can effectively assist developers in maintaining test code, improving overall software quality and reducing maintenance effort.

## 20. Structure-Aware, Diagnosis-Guided ECU Firmware Fuzzing

**Authors:** Qicai Chen (Fudan University, China), Kun Hu (School of Computer Science, Fudan University), Sichen Gong (Fudan University, China), Bihuan Chen (Fudan University), kevin kong (Fudan University), Haowen Jiang (Fudan University, China), Bingkun Sun (Fudan University), You Lu (Fudan University), Xin Peng (Fudan University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728914

**中文总结:** 提出结构感知、诊断引导的 ECU 固件模糊测试框架，同时覆盖 CAN 外部总线与 SPI 板载总线输入，并以双核 MCU 外设仿真器处理实时 SPI 通信；利用诊断协议采集故障码、错误变量等内部状态作反馈。10 块 ECU 中 9 块兼容，在 3 块代表 ECU 上发现 9 个此前未知的安全关键缺陷并已修复。

**Abstract:** Electronic Control Units (ECUs), providing a wide range of functions from basic control functions to safety-critical functions, play a critical role in modern vehicles. Fuzzing has emerged as an effective approach to ensure the functional safety and automotive security of ECU firmwares. However, existing fuzzing approaches focus on the inputs from other ECUs through external buses (e.g., CAN), but neglect the inputs from internal peripherals through on-board buses (e.g., SPI). Due to the restricted input space exploration, they fail to comprehensively fuzz ECU firmwares. Moreover, existing fuzzing approaches often lack visibility into ECU firmwares’ internal states but rely on limited feedback (e.g., message timeouts or hardware indicators), hindering their effectiveness.

To address these limitations, we propose a structure-aware, diagnosis-guided framework, \tool, to comprehensively and effectively fuzz ECU firmwares. Specifically, \tool simultaneously considers external buses (i.e., CAN) and on-board buses (i.e., SPI). It leverages the structure of CAN and SPI to effectively mutate CAN messages and SPI sequences, and incorporates a dual-core microcontroller-based peripheral emulator to handle real-time SPI communication. In addition, \tool implements a new feedback mechanism to guide the fuzzing process. It leverages automotive diagnostic protocols to collect ECUs’ internal states, i.e., trouble codes, error-related variables, and exception contexts. Our compatibility evaluation on ten ECUs from three major Tier 1 automotive suppliers has indicated that our framework is compatible with nine ECUs. Our effectiveness evaluation on three representative ECUs has demonstrated that our framework detects nine previously unknown safety-critical faults, which have been patched by technicians from the suppliers.

## 21. STRUT: Structured Seed Case Guided Unit Test Generation for C Programs using LLMs

**Authors:** Jinwei Liu (Xidian University), Chao Li (Beijing Institute of Control Engineering; Beijing Sunwise Information Technology), Rui Chen (Beijing Institute of Control Engineering; Beijing Sunwise Information Technology), Shaofeng Li (Xidian University), Bin Gu (Beijing Institute of Control Engineering), Mengfei Yang (China Academy of Space Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728970

**中文总结:** 提出 STRUT，以结构化测试用例为桥梁引导 LLM 为 C 程序生成单元测试，再规则转换为可执行代码，缓解 C 语言复杂特性下直接 codegen 的低通过率问题。执行通过率 96.01%，行覆盖率 77.67%、分支覆盖率 63.60%，显著优于 LLM 基线与符号执行工具 SunwiseAUnit。

**Abstract:** Unit testing plays a crucial role in bug detection and ensuring software correctness. It helps developers identify errors early in development, thereby reducing software defects. In recent years, large language models (LLMs) have demonstrated significant potential in automating unit test generation. However, using LLMs to generate unit tests faces many challenges. 1) The execution pass rate of the test cases generated by LLMs is low. 2) The test case coverage is inadequate, making it challenging to detect potential risks in the code. 3) Current research methods primarily focus on languages such as Java and Python, while studies on C programming are scarce, despite its importance in the real world. To address these challenges, we propose STRUT, a novel unit test generation method. STRUT utilizes structured test cases as a bridge between complex programming languages and LLMs. Instead of directly generating test code, STRUT guides LLMs to produce structured test cases, thereby alleviating the limitations of LLMs when generating code for programming languages with complex features. First, STRUT analyzes the context of focal methods and constructs structured seed test cases for them. These seed test cases then guide LLMs to generate a set of structured test cases. Subsequently, a rule-based approach is employed to convert the structured set of test cases into executable test code. We conducted a comprehensive evaluation of STRUT, which achieved an impressive execution pass rate of 96.01%, along with 77.67% line coverage and 63.60% branch coverage. This performance significantly surpasses that of the LLMs-based baseline methods and the symbolic execution tool SunwiseAUnit. These results highlight STRUT’s superior capability in generating high-quality unit test cases by leveraging the strengths of LLMs while addressing their inherent limitations.

## 22. Tratto: A Neuro-Symbolic Approach to Deriving Axiomatic Test Oracles

**Authors:** Davide Molinelli (USI Lugano; Schaffhausen Institute of Technology), Alberto Martin-Lopez (Software Institute - USI, Lugano), Elliott Zackrone (University of Washington), Beyza Eken (Sakarya University), Michael D. Ernst (University of Washington), Mauro Pezze (Università della Svizzera italiana (USI) and Università degli Studi di Milano Bicocca and CIT Constructor Institute of Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728960

**中文总结:** Tratto 结合符号模块（约束合法 token 搜索空间）与微调 Transformer（增量生成断言），从源码与文档自动生成公理化测试 oracle。实验显示准确率达 73%、F1 为 61%，可生成约 3 倍于现有符号方法的 oracle，且误报约为 GPT-4 few-shot + CoT 的 1/10。

**Abstract:** This paper presents Tratto, a neuro-symbolic approach that generates assertions (boolean expressions) that can serve as axiomatic oracles, from source code and documentation. The symbolic module of Tratto takes advantage of the grammar of the programming language, the unit under test, and the context of the unit (its class and available APIs) to restrict the search space of the tokens that can be successfully used to generate valid oracles. The neural module of Tratto uses transformers fine-tuned for both deciding whether to output an oracle or not and selecting the next lexical token to incrementally build the oracle from the set of tokens returned by the symbolic module. Our experiments show that Tratto outperforms the state-of-the-art axiomatic oracle generation approaches, with 73% accuracy, 72% precision, and 61% F1-score, largely higher than the best results of the symbolic and neural approaches considered in our study (61%, 62%, and 37%, respectively). Tratto can generate three times more axiomatic oracles than current symbolic approaches, while generating 10 times less false positives than GPT4 complemented with few-shot learning and Chain-of-Thought prompting.

## 23. Understanding Model Weaknesses: A Path to Strengthening DNN-Based Android Malware Detection

**Authors:** Haodong Li (Beijing University of Posts and Telecommunications), Xiao Cheng (Macquarie University), Yanjie Zhao (Huazhong University of Science and Technology), Guosheng Xu (Beijing University of Posts and Telecommunications), Guoai Xu (Harbin Institute of Technology, Shenzhen), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728884

**中文总结:** MalTutor 针对恶意软件家族不平衡导致 DNN 检测器过拟合的问题，将预测不确定性纳入课程学习：先训低不确定性样本再逐步引入难例。在不平衡数据集上准确率提升 31.0%、F1 提升 138.8%，多类恶意应用平均检测准确率提升 133.9%。

**Abstract:** Android malware detection remains a critical challenge in cybersecurity research. Recent advancements leverage AI techniques, particularly deep neural networks (DNNs), to train a detection model, but their effectiveness is often compromised by the pronounced imbalance among malware families in commonly used training datasets. This imbalance leads to overfitting in dominant categories and poor performance in underrepresented ones, increasing predictive uncertainty for less common malware families. To address the suboptimal performance of many DNN models, we introduce MalTutor, a novel framework that enhances model robustness through an optimized training process. Our primary insight lies in transforming uncertainties from ‘‘liabilities’’ into ‘‘assets’’ by strategically incorporating them into DNN training methodologies. Specifically, we begin by evaluating the predictive uncertainty of DNN models throughout various training epochs, which guides our sample categorization. Incorporating Curriculum Learning strategies, we commence training with easy-to-learn samples with lower uncertainty, progressively incorporating difficult-to-learn ones with higher uncertainty. Our experimental results demonstrate that MalTutor significantly improves the performance of models trained on imbalanced datasets, increasing accuracy by 31.0%, elevating the F1 score by 138.8%, and specifically boosting the average accuracy in detecting various types of malicious apps by 133.9%. Our findings provide valuable insights into the potential benefits of incorporating uncertainty to improve the robustness of DNN models for  prediction-oriented software engineering tasks.

## 24. Understanding Practitioners’ Expectations on Clear Code Review Comments

**Authors:** Junkai Chen (Singapore Management University, Singapore), Zhenhao Li (York University), Qiheng Mao (Zhejiang University), Xing Hu (Zhejiang University), Kui Liu (Huawei), Xin Xia (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728931

**中文总结:** 基于文献与从业者调研提出 CRC 清晰度三维属性 RIE（Relevance、Informativeness、Expression），并发现九种语言开源项目中 28.8% 评论至少在一维不清晰。ClearCRC 用预训练语言模型自动评估清晰度，平衡准确率最高 73.04%、F1 最高 94.61%。

**Abstract:** The code review comment (CRC) is pivotal in the process of modern code review. It provides reviewers with the opportunity to identify potential bugs, offer constructive feedback, and suggest improvements. Clear and concise code review comments (CRCs) facilitate the communication between developers and is crucial to the correct understanding of the issues identified and proposed solutions. Despite the importance of CRCs’ clarity, there is still a lack of guidelines on what constitutes a good clarity and how to evaluate it. In this paper, we conduct a comprehensive study on understanding and evaluating the clarity of CRCs. We first derive a set of attributes related to the clarity of CRCs, namely RIE attributes (i.e., Relevance, Informativeness, and Expression), as well as their corresponding evaluation criteria based on our literature review and survey with practitioners. We then investigate the clarity of CRCs in open-source projects written in nine programming languages and find that a large portion (i.e., 28.8%) of the CRCs lack the clarity in at least one of the attributes. Finally, we explore the potential of automatically evaluating the clarity of CRCs by proposing ClearCRC. Experimental results show that ClearCRC with pre-trained language models is promising for effective evaluation of the clarity of CRCs, achieving a balanced accuracy up to 73.04% and a F-1 score up to 94.61%.

## 25. Unlocking Low Frequency Syscalls in Kernel Fuzzing with Dependency-based RAG

**Authors:** Zhiyu Zhang (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Longxing Li (Institute of Information Engineering, Chinese Academy of Sciences, China), Ruigang Liang (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences), Kai Chen (Institute of Information Engineering at Chinese Academy of Sciences; University of Chinese Academy of Sciences)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728913

**中文总结:** SyzGPT 用依赖检索增强生成（DRAG）让 LLM 自动为内核 fuzzing 合成覆盖低频 syscall（LFS）的种子：从文档抽依赖、按依赖检索语料作上下文并周期性修复种子。生成种子有效率 87.84%，相较 7 个 SOTA fuzzer 平均提升代码覆盖率 17.73%、LFS 覆盖率 58%、漏洞发现 323.22%，独立发现 26 个未知内核 bug。

**Abstract:** Most coverage-guided kernel fuzzers test operating system kernels based on syscall sequence synthesis. However, there are still syscalls rarely or not covered (called low frequency syscalls, LFS) in a period of fuzzing, meaning the relevant code branches remain unexplored. This is due to the complexity dependencies of the LFS and mutation uncertainty, which makes it difficult for fuzzers to generate corresponding syscall sequences. Since many kernel fuzzers can dynamically learn syscall dependencies from the current corpus based on the choice table mechanism, providing comprehensive and high-quality seeds could help fuzzers cover LFS. However, constructing such seeds relies heavily on expert experience to resolve the syscall dependencies.

In this paper, we propose SyzGPT, the first kernel fuzzing framework to automatically generate effective seeds for LFS via Large Language Model (LLM). We leverage a dependency-based retrieval-augmented generation (DRAG) method to unlock the potential of LLM and design a series of steps to improve the effectiveness of the generated seeds. First, SyzGPT automatically extracts syscall dependencies from the existing documentation via LLM. Second, SyzGPT retrieves programs from the fuzzing corpus based on the dependencies to construct adaptive context for LLM. Last, SyzGPT periodically generates and repairs seeds with feedback to enrich the fuzzing corpus for LFS. We propose a novel set of evaluation metrics for seed generation in kernel domain. Our evaluation shows that SyzGPT can generate seeds with a high valid rate of 87.84% and can be extended to offline and fine-tuned LLMs. Compared to seven state-of-the-art kernel fuzzers, SyzGPT improves code coverage by 17.73%, LFS coverage by 58.00%, and vulnerability detection by 323.22% on average. Besides, SyzGPT independently discovered 26 unknown kernel bugs (10 are LFS-related), with 11 confirmed.

## 26. Validating Network Protocol Parsers with Traceable RFC Document Interpretation

**Authors:** Mingwei Zheng (Purdue University), Danning Xie (Purdue University), Qingkai Shi (Nanjing University), Chengpeng Wang (Purdue University), Xiangyu Zhang (Purdue University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728955

**中文总结:** 利用 LLM 将 RFC 文档系统翻译为形式化报文规范作准 oracle，迭代校验 C/Python/Go 协议解析器实现，并将缺陷回溯至文档段落以解决可追溯性。在 9 个协议上优于 SOTA，发现 69 个 bug（35 个已确认）。

**Abstract:** Validating the correctness of network protocol implementations is highly challenging due to the oracle and the traceability problems. The former determines when a protocol implementation can be considered buggy, especially when the bugs do not cause any observable symptoms. The latter allows developers to understand how an implementation violates the protocol specification, thereby facilitating bug fixes. Unlike existing works that rarely take both problems into account, this work considers both and provides an effective solution using recent advances in large language models (LLMs). Our key observation is that network protocols are often released with structured specification documents, a.k.a. RFC documents, which can be systematically translated to formal protocol message specifications via an LLM. Such specifications, which may contain errors due to the hallucination of LLM, are used as a quasi-oracle to validate protocol parsers. The validation results in return gradually refine the oracle. Since the oracle is derived from the document, any bugs we find in a protocol implementation can be traced back to the document, thus addressing the traceability problem. We have extensively evaluated our approach using nine network protocols and their implementations written in C, Python, and Go. The results show that our approach outperforms the state-of-the-art and has detected 69 bugs with 35 confirmed. The project also demonstrates the potential for fully automating software validation based on natural language specifications, a process previously considered predominantly manual due to the need to understand specification documents and derive expected outputs for test inputs.

## 27. WildSync: Automated Fuzzing Harness Synthesis via Wild API Usage Recovery

**Authors:** Wei-Cheng Wu (Dartmouth College), Stefan Nagy (University of Utah), Christophe Hauser (Dartmouth College)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728918

**中文总结:** WildSync 从开源项目 AST 提取未测 API 的真实用法模式，并合成融入 OSS-Fuzz 的新 fuzzing harness。为 24 个库生成 469 个新 harness，覆盖 1.3k+ 函数与近 2 万行代码，发现 7 个此前未检出的 bug。

**Abstract:** Fuzzing stands as one of the most practical techniques to test software efficiently. When applying fuzzing to software library APIs, high-quality fuzzing harnesses are essential, enabling fuzzers to execute the APIs with precise sequences and function parameters. Although software developers commonly rely on manual efforts to create fuzzing harnesses, there has been a growing interest in automating this process. Existing works are often constrained in their scalability and effectiveness due to their reliance on compiler-based analysis or runtime execution traces, which require manual setup and configuration. Our investigation of multiple actively fuzzed libraries reveals that a large number of exported API functions externally used by various open-source projects still remain untested by existing harnesses or unit-test files. The lack of testing for these API functions increases the risk of vulnerabilities going undetected, potentially leading to security issues.

In order to address the lack of coverage affecting existing fuzzing methods, we propose a novel approach to automatically generate fuzzing harnesses by extracting usage patterns of untested functions from real-world scenarios, using techniques based on lightweight Abstract Syntax Tree parsing to extract API usage from external source code. Then, we integrate the usage patterns into existing harnesses to construct new ones covering these untested functions. We have implemented a prototype of this concept named WildSync, enabling the automatic synthesis of fuzzing harnesses for C/C++ libraries on OSS-Fuzz. In our experiments, WildSync successfully produced 469 new harnesses for 24 actively fuzzed libraries on OSS-Fuzz, and also extended to 3 wildly used libraries that can be later integrated into OSS-Fuzz. This results in a significant increase in test coverage spanning over 1.3k functions and nearly 20k lines of code, while also identifying 7 previously undetected bugs.

## 28. xFUZZ: A Flexible Framework for Fine-Grained, Runtime-Adaptive Fuzzing Strategy Composition

**Authors:** DongSong Yu (Zhongguancun Laboratory), Yiyi Wang (Tsinghua University, Huazhong University of Science and Technology), Chao Zhang (Tsinghua University), Yang Lan, Zhiyuan Jiang (National University of Defense Technology), Shuitao Gan (Labortory for Advanced Computing and Intelligence Engineering), Zheyu Ma (Tsinghua University), Wende Tan (Tsinghua University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728873

**中文总结:** xFUZZ 将输入/变异调度策略拆为可运行时切换的细粒度插件，并以 Sliding-Window Thompson Sampling 自适应组合。相较 SOTA fuzzer，独特漏洞发现提升 10.07%、代码覆盖率提升 4.94%，在测试集中率先检出 21/37 个漏洞。

**Abstract:** Fuzzing is one of the most efficient techniques for detecting vulnerabilities in software. Existing approaches struggle with performance inconsistencies across different targets and rely on rigid, coarse-grained fuzzing strategy composition, limiting the flexibility to adaptively combine the strengths of different fuzzing strategies at runtime. To address these challenges, we present xFUZZ, a flexible and extensible fuzzing framework supporting fine-grained, runtime-adaptive strategy composition. xFUZZ integrates popular input scheduling and mutation scheduling strategies as fine-grained, independently switchable plugins, allowing users to adaptively replace any plugins throughout the fuzzing campaign. Furthermore, we introduce an adaptive algorithm based on Sliding-Window Thompson Sampling, which dynamically selects the optimal composition of the fuzzing strategy during the fuzzing campaign. Experimental results show that xFUZZ outperforms state-of-the-art fuzzers by achieving a 10.07% increase in unique vulnerability discovery and a 4.94% improvement in code coverage. Notably, xFUZZ is the first to detect 21 out of 37 vulnerabilities in the test suite, establishing its effectiveness across varied targets.

## 29. You Name It, I Run It: An LLM Agent to Execute Tests of Arbitrary Projects

**Authors:** Islem BOUZENIA (University of Stuttgart), Michael Pradel (University of Stuttgart)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728922

**中文总结:** ExecutionAgent 是 LLM 智能体，通过 meta-prompting 收集技术指南并迭代执行命令，自动为任意项目生成构建与测试脚本。在 14 种语言、50 个开源项目上成功运行 33 个测试套件，结果与 ground truth 偏差仅 7.5%，成功率约为此前最佳方法的 6.6 倍。

**Abstract:** The ability to execute the test suite of a project is essential in many scenarios, e.g., to assess code quality and code coverage, to validate code changes made by developers or automated tools, and to ensure compatibility with dependencies. Despite its importance, executing the test suite of a project can be challenging in practice because different projects use different programming languages, software ecosystems, build systems, testing frameworks, and other tools. These challenges make it difficult to create a reliable, universal test execution method that works across different projects. This paper presents ExecutionAgent, an automated technique that prepares scripts for building an arbitrary project from source code and running its test cases. Inspired by the way a human developer would address this task, our approach is a large language model-based agent that autonomously executes commands and interacts with the host system. The agent uses meta-prompting to gather guidelines on the latest technologies related to the given project, and it iteratively refines its process based on feedback from the previous steps. Our evaluation applies ExecutionAgent to 50 open-source projects that use 14 different programming languages and many different build and testing tools. The approach successfully executes the test suites of 33/50 projects, while matching the test results of ground truth test suite executions with a deviation of only 7.5%. These results improve over the best previously available technique by 6.6x. The costs imposed by the approach are reasonable, with an execution time of 74 minutes and LLM costs of 0.16 dollars, on average per project. We envision ExecutionAgent to serve as a valuable tool for developers, automated programming tools, and researchers that need to execute tests across a wide variety of projects.

## 30. ZTaint-Havoc: From Havoc Mode to Zero-Execution Fuzzing-Driven Taint Inference

**Authors:** Yuchong Xie (Hong Kong University of Science and Technology), Wenhui Zhang (Hunan University, Changsha, China), Dongdong She (HKUST (The Hong Kong University of Science and Technology))

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728916

**中文总结:** ZTaint-Havoc 将 AFL++ havoc 变异形式化，在零额外程序执行的前提下同步完成 Fuzzing-Driven Taint Inference，识别影响程序行为的热字节。插桩开销仅 3.84%–12.58%，24 小时 fuzzing 在 FuzzBench/UniBench 上相对 vanilla AFL++ 平均提升边覆盖率 2.97%–6.12%，最高达 33.71%–51.12%。

**Abstract:** Fuzzing is a popular software testing technique for discovering vulnerabilities. A central problem in fuzzing is identifying hot bytes that can influence program behavior. Taint analysis can track the data flow of hot bytes in a white-box fashion, but it often suffers from stability issues and cannot run on large real-world programs. Fuzzing-Driven Taint Inference (FTI) is a simple black-box technique to track hot bytes for fuzzing. It monitors the dynamic program behaviors of program execution instances and further infers hot bytes in a black-box fashion. However, this method requires additional O(N) program executions and incurs a large run-time overhead.

We observe that a widely used mutation scheme in fuzzing–havoc mode can be adapted into a lightweight FTI with zero additional program execution. In this work, we first present a computational model of the havoc mode that formally describes its mutation process. Based on this model, we show that the havoc mode can simultaneously launch FTI while generating and executing new testcases. Further, we propose a novel FTI called ZTaint-Havoc that doesn’t need any additional program execution. ZTaint-Havoc incurs minimal instrumentation overhead of 3.84% on UniBench and 12.58% on FuzzBench, respectively. In the end, we give an effective mutation algorithm using the hot bytes identified by ZTaint-Havoc.

We conduct a comprehensive evaluation to investigate the computational model of havoc mode. Our evaluation result justifies that it is feasible to adapt the havoc mode to an efficient FTI without any additional program execution. We further implement our approach as a prototype ZTaint-Havoc based on the havoc mode of AFL++. We evaluate ZTaint-Havoc on two fuzzing datasets FuzzBench and UniBench. Our extensive evaluation results show that ZTaint-Havoc improves edge coverage by up to 33.71% on FuzzBench and 51.12% on UniBench over vanilla AFL++, with average improvements of 2.97% and 6.12% respectively, in 24-hour campaigns.
