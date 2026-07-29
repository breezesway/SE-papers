# FSE 2025 Research Track — Testing and Fuzzing

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 21 papers

## 1. A Mixed-Methods Study of Model-Based GUI Testing in Real-World Industrial Settings

**Authors:** Shaoheng Cao (Nanjing University), Renyi Chen (Samsung Electronics（China）R&D Centre), Wenhua Yang (Nanjing University of Aeronautics and Astronautics), Minxue Pan (Nanjing University), Xuandong Li (Nanjing University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715789

**中文总结:** 与工业伙伴开展为期两月的混合方法纵向研究，对比基于模型的 GUI 测试与脚本测试的短/长期效果；揭示有效性、可维护性及工程师认知随时间变化，并为学界与工业采纳 MBT 提供启示。

**Abstract:** Model-based testing (MBT) has been an important methodology in software engineering, attracting extensive research attention for over four decades. However, despite its academic acclaim, studies examining the impact of MBT in industrial environments—particularly regarding its long-term effects—remain limited and yield unclear results. This gap may contribute to the challenges in establishing a study environment for implementing and applying MBT in production settings to evaluate its impact over time. To bridge this gap, we collaborated with an industrial partner to undertake a comprehensive, longitudinal empirical study employing mixed methods. Over two months, we implemented our MBT tool within the corporation, assessing the short- and long-term effectiveness and efficiency of MBT compared to script-writing-based testing. Through a mix of quantitative and qualitative methods—spanning experimental data, questionnaire surveys, and interviews—our study uncovers several insightful findings. These include differences in effectiveness and maintainability between short- and long-term MBT application, the evolving perceptions and expectations of engineers regarding MBT, and more. Leveraging these insights, we propose actionable implications for both the academic and industrial communities, aimed at bolstering confidence in MBT adoption and investment for software testing purposes.

## 2. Adaptive Random Testing with Qgrams: the Illusion Comes True

**Authors:** Matteo Biagiola (Università della Svizzera italiana), Robert Feldt (Chalmers | University of Gothenburg), Paolo Tonella (USI Lugano)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715740

**中文总结:** 提出基于 Qgrams 聚合历史执行的 Adaptive Random Testing，将多样性度量复杂度从二次降为线性；在 6 个 Web 应用上平均比随机测试多覆盖 4×、比传统距离 ART 多 3.5× 独特目标。

**Abstract:** Adaptive Random Testing (ART) has faced criticism, particularly for its computational inefficiency, as highlighted by Arcuri and Briand. Their analysis clarified how ART requires a quadratic number of distance computations as the number of test executions increases, which limits its scalability in scenarios requiring extensive testing to uncover faults. Simulation results support this, showing that the computational overhead of these distance calculations often outweighs ART’s benefits. While various ART variants have attempted to reduce these costs, they frequently do so at the expense of fault detection, lack complexity guarantees, or are restricted to specific input types, such as numerical or discrete data. In this paper, we introduce a novel framework for adaptive random testing that replaces pairwise distance computations with a compact aggregation of past executions, such as counting the Qgrams observed in previous runs. Test case selection then leverages this aggregated data to measure diversity (e.g., entropy of Qgrams), allowing us to reduce the computational complexity from quadratic to linear. Experiments with a benchmark of six web applications, show that ART with Qgrams covers, on average, 4× more unique targets than random testing, and 3.5× more than ART using traditional distance-based methods.

## 3. Automated Soap Opera Testing Directed by LLMs and Scenario Knowledge: Feasibility, Challenges, and Road Ahead

**Authors:** Yanqi Su (Australian National University), Zhenchang Xing (CSIRO's Data61), Chong Wang (Nanyang Technological University), Chunyang Chen (TU Munich), Xiwei (Sherry) Xu (Data61, CSIRO), Qinghua Lu (Data61, CSIRO), Liming Zhu (CSIRO’s Data61)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715752

**中文总结:** 构建基于 LLM 与 Scenario Knowledge Graph 的多 Agent（Planner/Player/Detector）系统以自动化 soap opera 探索性测试；实验显示有潜力但仍落后人工，并展望神经符号协同与人机共学路线。

**Abstract:** Exploratory testing (ET) harnesses tester’s knowledge, creativity, and experience to create varying tests that uncover unexpected bugs from the end-user’s perspective. Although ET has proven effective in system-level testing of interactive systems, the need for manual execution, has hindered large-scale adoption. In this work, we explore the feasibility, challenges and road ahead of automated scenario-based ET (a.k.a soap opera testing). We conduct a formative study, identifying key insights for effective manual soap opera testing and challenges in automating the process. We then develop a multi-agent system leveraging LLMs and a Scenario Knowledge Graph (SKG) to automate soap opera testing. The system consists of three multi-modal agents, Planner, Player, and Detector that collaborate to execute tests and identify potential bugs. Experimental results demonstrate the potential of automated soap opera testing, but there remains a significant gap compared to manual execution, especially under-explored scenario boundaries and incorrectly identified bugs. Based on the observation, we envision road ahead for the future of automated soap opera testing, focusing on three key aspects: the synergy of neural and symbolic approaches, human-AI co-learning, and the integration of soap opera testing with broader software engineering practices. These insights aim to guide and inspire the future research.

## 4. Automated Unit Test Refactoring

**Authors:** Yi Gao (Zhejiang University), Xing Hu (Zhejiang University), Xiaohu Yang (Zhejiang University), Xin Xia (Zhejiang University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715750

**中文总结:** 提出 UTRefactor，结合测试气味知识库、DSL 规则与 CoT 引导 LLM 逐步消除 Java 测试气味，并有检查点处理多气味场景；在 879 个测试上将气味从 2375 降至 265（降 89%），显著优于直接 LLM 与规则工具。

**Abstract:** Test smells arise from poor design practices and insufficient domain knowledge, which can lower the quality of test code and make it harder to maintain and update. Manually refactoring of test smells is time-consuming and error-prone, highlighting the necessity for automated approaches. Current rule-based refactoring methods often struggle in scenarios not covered by predefined rules and lack the flexibility needed to handle diverse cases effectively. In this paper, we propose a novel approach called UTRefactor, a context-enhanced, LLM-based framework for automatic test refactoring in Java projects. UTRefactor extracts relevant context from test code and leverages an external knowledge base that includes test smell definitions, descriptions, and DSL-based refactoring rules. By simulating the manual refactoring process through a chain-of-thought approach, UTRefactor guides the LLM to eliminate test smells in a step-by-step process, ensuring both accuracy and consistency throughout the refactoring. Additionally, we implement a checkpoint mechanism to facilitate comprehensive refactoring, particularly when multiple smells are present. We evaluate UTRefactor on 879 tests from six open-source Java projects, reducing the number of test smells from 2,375 to 265, achieving an 89% reduction. UTRefactor outperforms direct LLM-based refactoring methods by 61.82% in smell elimination and significantly surpasses the performance of a rule-based test smell refactoring tool. Our results demonstrate the effectiveness of UTRefactor in enhancing test code quality while minimizing manual involvement.

## 5. ChangeGuard: Validating Code Changes via Pairwise Learning-Guided Execution

**Authors:** Lars Gröninger (University of Stuttgart), Beatriz Souza (Universität Stuttgart), Michael Pradel (University of Stuttgart)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifact-Available, Artifact-Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715760

**中文总结:** 提出 ChangeGuard，通过成对学习引导执行对比修改前后函数的运行时行为，以验证代码变更是否保语义；在手动标注与自动化改造数据集上精度 77.1%、召回 69.5%，远高于项目回归测试的 7.6% 召回。

**Abstract:** Code changes are an integral part of the software development process. Many code changes are meant to improve the code without changing its functional behavior, e.g., refactorings and performance improvements. Unfortunately, validating whether a code change preserves the behavior is non-trivial, particularly when the code change is performed deep inside a complex project. This paper presents ChangeGuard, an approach that uses learning-guided execution to compare the runtime behavior of a modified function. The approach is enabled by the novel concept of pairwise learning-guided execution and by a set of techniques that improve the robustness and coverage of the state-of-the-art learning-guided execution technique. Our evaluation applies ChangeGuard to a dataset of 224 manually annotated code changes from popular Python open-source projects and to three datasets of code changes obtained by applying automated code transformations. Our results show that the approach identifies semantics-changing code changes with a precision of 77.1% and a recall of 69.5%, and that it detects unexpected behavioral changes introduced by automatic code refactoring tools. In contrast, the existing regression tests of the analyzed projects miss the vast majority of semantics-changing code changes, with a recall of only 7.6%. We envision our approach being useful for detecting unintended behavioral changes early in the development process and for improving the quality of automated code transformations.

## 6. CoverUp: Effective High Coverage Test Generation for Python

**Authors:** Juan Altmayer Pizzorno (University of Massachusetts Amherst), Emery D. Berger (University of Massachusetts Amherst and Amazon Web Services)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729398

**中文总结:** 提出 CoverUp，通过覆盖率分析与 LLM 对话迭代优化，生成高覆盖 Python 回归测试；相对 CodaMosa 模块中位行+分支覆盖率 80% vs 47%，相对 MuTAP 总体 90% vs 77%，迭代引导贡献近 40% 成功案例。

**Abstract:** Testing is an essential part of software development. Test generation tools attempt to automate the otherwise labor-intensive task of test creation, but generating high-coverage tests remains a challenge. This paper proposes CoverUp, a novel approach to driving the generation of high-coverage Python regression tests. CoverUp iteratively improves test coverage, interleaving coverage analysis with dialogs with the LLM that steer it to refine tests so that they increase coverage of lines and branches. We evaluate our prototype CoverUp implementation across a benchmark of challenging code derived from open-source Python projects, and show that CoverUp substantially improves on the state of the art. Compared to CodaMosa, a hybrid search/LLM-based test generator, CoverUp achieves a per-module median line+branch coverage of 80% (vs. 47%). Compared to MuTAP, a mutation/LLM-based test generator, CoverUp achieves an overall line+branch coverage of 90% (vs. 77%). We show that CoverUp’s iterative, coverage-guided approach is crucial to its effectiveness, contributing to nearly 40% of its successes.

## 7. De-duplicating Silent Compiler Bugs via Deep Semantic Representation

**Authors:** Junjie Chen (Tianjin University), Xingyu Fan (Tianjin University), Chen Yang (Tianjin University), Shuang Liu (Renmin University of China), Jun Sun (Singapore Management University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729375

**中文总结:** 提出黑盒静默编译器缺陷去重方法 BLADE，通过对触发失败与正常程序的中间表示学习提取失败相关语义并用模型解释定位；在 GCC/LLVM 四数据集上相对两种已有黑盒方法平均分别提升 36% 与 12%，接近白盒 SOTA。

**Abstract:** The compiler bug duplication problem (where many test failures are caused by the same compiler bug) can lead to huge waste of time and resource in diagnosing test failures produced by compiler testing. It is particularly challenging with regard to the silent compiler bugs that do not produce any error messages. To address this problem, multiple white-box techniques were proposed, but they are inapplicable in many practical scenarios. Black-box techniques are more practical, but the existing ones are less effective as they often rely on irrelevant syntactic information. To bridge this gap, we propose a novel black-box technique (BLADE), which aims to improve the effectiveness of black-box de-duplication by extracting failure-relevant semantic information from failure-triggering test programs in a black-box manner. It first learns failure-relevant semantic information based on intermediate representation learning by employing the classification of failure-triggering and failure-free test programs as the auxiliary objective, and then extracts such information based on model interpretation. Our experiments on four widely-used datasets (collected from GCC and LLVM) show that BLADE significantly outperforms the two existing black-box techniques with an average improvement of 36% and 12% in identifying unique silent compiler bugs when analyzing the same number of test failures respectively, and achieves competitive effectiveness with the state-of-the-art white-box techniques.

## 8. Directed Testing in MLIR: Unleashing Its Potential by Overcoming the Limitations of Random Fuzzing

**Authors:** Weiyuan Tong (Northwest University), Zixu Wang (Northwest University), Zhanyong Tang (Northwest University), Jianbin Fang (National University of Defense Technology), Yuqun Zhang (Southern University of Science and Technology), Guixin Ye (Northwest University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729372

**中文总结:** 提出 MLIRTracer，自高层 tosa IR 自上而下、有向探索易出错区域，以克服随机模糊对下游方言缺陷检测不足的问题；共发现 73 个缺陷，其中 61 个已被 MLIR 开发者修复。

**Abstract:** MLIR is a new way of creating compiler infrastructures that can be easily reused and extended. Current MLIR fuzzing methods focus primarily on test case generation or mutation using randomly selected passes. However, they often overlook the hierarchical structure of MLIR, resulting in inefficiencies in bug detection, especially for issues triggered by downstream dialects. Random testing lacks a focused approach to exploring the code space, resulting in wasted resources on normal components and overlooking bug-prone areas. To address these limitations, we introduce MLIRTracer, a top-down fuzzing approach that targets the highest level of MLIR programs (tosa IR) with a directed testing strategy. Our method systematically traverses the hierarchical code space of MLIR, from tosa IR to the lower levels, while prioritizing tests of bug-prone areas through directed exploration. MLIRTracer has successfully detected 73 bugs, with 61 already resolved by the MLIR developers.

## 9. Doc2OracLL: Investigating the Impact of Documentation on LLM-based Test Oracle Generation

**Authors:** Soneya Binta Hossain (University of Virginia), Raygan Taylor (Dillard University), Matthew B Dwyer (University of Virginia)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729354

**中文总结:** 系统研究 Javadoc 对 LLM 测试预言生成的影响，微调 10 个模型并分析不同注释组件与来源；多数情况下加入文档提升预言准确性，描述与 return 标签最有价值，仅用 Javadoc 即可在 Defects4J 上比先前方法多检出 19%–94% 真实缺陷。

**Abstract:** Code documentation is a critical aspect of software development, serving as a bridge between human understanding and machine-readable code. Beyond assisting developers in understanding and maintaining code, documentation also plays a critical role in automating various software engineering tasks, such as test oracle generation (TOG). In Java, Javadoc comments provide structured, natural language documentation embedded directly in the source code, typically detailing functionality, usage, parameters, return values, and exceptions. While prior research has utilized Javadoc comments in test oracle generation (TOG), there has not been a thorough investigation into their impact when combined with other contextual information, nor into identifying the most relevant components for generating correct and strong test oracles, or understanding their role in detecting real bugs. In this study, we dive deep into investigating the impact of Javadoc comments on TOG. We start by fine-tune 10 large language models with three different prompt pairs designed to investigate the impact of Javadoc comments when using with other contextual information. We conduct a systematic analysis to assess the impact of different Javadoc components on TOG. For investigating the generalizability of the Javadoc comments from various sources, we also generate Javadoc comments using GPT-3.5 model. Finally, we perform a thorough bug detection study using Defects4J to understand the role of Javadoc comments in real-world bug detection. Our results show that, in most cases, incorporating Javadoc comments improves the accuracy of test oracles, aligning closely with ground truth. We found that Javadoc comments alone can nearly match the performance achieved when using both Javadoc comments and MUT code. We find that the description and the return tags of the Javadoc comments are most valuable in TOG. Finally, when using just Javadoc comments our method detects between 19% and 94% more real-world bugs in Defects4J than prior methods.

## 10. Less is More: On the Importance of Data Quality for Unit Test Generation

**Authors:** Junwei Zhang (Zhejiang University), Xing Hu (Zhejiang University), Shan Gao (Huawei), Xin Xia (Zhejiang University), David Lo (Singapore Management University), Shanping Li (Zhejiang University)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715778

**中文总结:** 系统梳理单元测试生成数据集中的噪声类型，并提出自动清洗框架 CleanTest。Methods2Test/Atlas 中噪声占比达 43.52%/29.65%；过滤后微调多种 LLM，在 Defects4J 上分支覆盖平均提升 67%/39%，缺陷检测亦改善。

**Abstract:** Unit testing is crucial for software development and maintenance. Effective unit testing ensures and improves software quality, but writing unit tests is time-consuming and labor-intensive. Recent studies have proposed deep learning (DL) techniques or large language models (LLMs) to automate unit test generation. These models are usually trained or fine-tuned on large-scale datasets. Despite growing awareness of the importance of data quality, there has been limited research on the quality of datasets used for test generation. To bridge this gap, we systematically examine the impact of noise on the performance of learning-based test generation models. We first apply the open card sorting method to analyze the most popular and largest test generation dataset, Methods2Test, to categorize eight distinct types of noise. Further, we conduct detailed interviews with 17 domain experts to validate and assess the importance, reasonableness, and correctness of the noise taxonomy. Then, we propose CleanTest, an automated noise-cleaning framework designed to improve the quality of test generation datasets. CleanTest comprises three filters: a rule-based syntax filter, a rule-based relevance filter, and a model-based coverage filter. To evaluate its effectiveness, we apply CleanTest on two widely-used test generation datasets, i.e., Methods2Test and Atlas. Our findings indicate that 43.52% and 29.65% of datasets contain noise, highlighting its prevalence. Finally, we conduct comparative experiments using four LLMs (i.e., CodeBERT, AthenaTest, StarCoder, and CodeLlama7B) to assess the impact of noise on test generation performance. The results show that filtering noise positively influences the test generation ability of the models. Fine-tuning the four LLMs with the filtered Methods2Test dataset, on average, improves its performance by 67% in branch coverage, using the Defects4J benchmark. For the Atlas dataset, the four LLMs improve branch coverage by 39%. Additionally, filtering noise improves bug detection performance, resulting in a 21.42% increase in bugs detected by the generated tests.

## 11. Liberating libraries through automated fuzz driver generation: Striking a Balance Without Consumer Code

**Authors:** Flavio Toffalini (EPFL, Switzerland and Ruhr-Universität Bochum, Germany), Nicolas Badoux (EPFL), Zurab Tsinadze (EPFL), Mathias Payer (EPFL)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729365

**中文总结:** 提出 libErator，通过静态分析、快速丢弃无效驱动与有效驱动选择，在有限算力下平衡 fuzz driver 生成与深度测试。在 11 个开源库上覆盖优于既有自动方法，确认 16 个缺陷，真阳性率约 20%（约为此前 SOTA 的两倍）。

**Abstract:** Harnessing fuzzers to test software libraries requires developers to write fuzz drivers, specialized programs that exercise valid library usage. Given a driver, fuzzers generate interesting inputs that trigger the library’s bugs. Writing fuzz drivers manually is a cumbersome process and these drivers frequently hit a coverage plateau, calling for more diverse drivers. To alleviate the need for human expert knowledge, emerging automatic driver generation techniques invest computational time for tasks besides input generation. Therefore, to maximize the number of bugs found, it is crucial to allocate computation resources carefully between generating valid drivers and testing them thoroughly. Current works model driver generation and testing as a single problem, i.e., they mutate both the driver’s code and input together. This simple approach is limited, as many libraries need a combination of non-trivial library usage and complex inputs. For example, consider a JPEG manipulation library, bugs appear when specific library functions and corrupted images are coincidentally tested together, which, if both are mutated synchronously is difficult to trigger. We introduce libErator, a novel library testing approach that balances constrained computational resources to achieve two goals (a) quickly generate valid fuzz drivers and (b) deeply test these drivers to find bugs. To achieve these goals, libErator employs three main techniques. First, we leverage insights from a novel static analysis to improve the likelihood of generating meaningful drivers. Second, we design a method to quickly discard non-functional drivers, further reducing resources wasted on unfruitful drivers. Finally, we show an effective driver selection method that avoids redundant tests. We deploy libErator on 11 open-source libraries and evaluate it against manually written and automatically generated drivers. We show that libErator reaches comparable coverage to manually written drivers and, on average, exceeds coverage from existing automated driver generation techniques. More importantly, libErator automatically finds 16 confirmed bugs, 10 of which are already fixed and upstreamed. Among the bugs found, one was assigned a CVE while others contributed to the project test suites, thus showcasing the ability of libErator to create valid library usages. Finally, since driver synthesis may find invalid errors, we assess the true positive ratio of libErator at 20%, double the state of the art.

## 12. LlamaRestTest: Effective REST API Testing with Small Language Models

**Authors:** Myeongsoo Kim (Georgia Institute of Technology), Saurabh Sinha (IBM Research), Alessandro Orso (University of Georgia, USA)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715737

**中文总结:** 提出 LlamaRestTest，微调两个基于 Llama3-8b 的小模型，结合服务器响应持续生成真实输入并挖掘参数依赖。在 12 个真实服务上，小模型可媲美甚至超过更大模型与多种 SOTA REST 测试工具的覆盖与内部错误发现能力。

**Abstract:** Modern web services rely heavily on REST APIs, typically documented using the OpenAPI specification. The widespread adoption of this standard has resulted in the development of many black-box testing tools that generate tests based on these specifications. Recent advancements in Natural Language Processing (NLP), particularly with Large Language Models (LLMs), have enhanced REST API testing by extracting actionable rules and generating input values from the human-readable portions of the specification. However, these advancements overlook the potential of continuously refining the identified rules and test inputs based on server responses. To address this limitation, we present LlamaRestTest, a novel approach that employs two custom LLMs to generate realistic test inputs and uncover parameter dependencies during the testing process by incorporating server responses. These LLMs are created by fine-tuning the Llama3-8b model, using mined datasets of REST API example values and inter-parameter dependencies. We evaluated LlamaRestTest on 12 real-world services (including popular services such as Spotify), comparing it against RESTGPT, a GPT-powered specification-enhancement tool, as well as several state-of-the-art REST API testing tools, including RESTler, MoRest, EvoMaster, and ARAT-RL. Our results demonstrate that fine-tuning enables smaller LLMs to outperform much larger models in detecting actionable rules and generating inputs for REST API testing. We also evaluated different tool configurations, ranging from the base Llama3-8B model to fine-tuned versions tailored for REST API testing, and explored multiple quantization techniques, including 2-bit, 4-bit, and 8-bit integer formats, to improve efficiency and performance. Our study shows that small language models can perform similar to, or better than, large language models in REST API testing, striking a balance between effectiveness and efficiency. Furthermore, LlamaRestTest outperforms state-of-the-art REST API testing tools in code coverage achieved and internal server errors identified, even when those tools utilize enhanced specifications generated by RESTGPT. Finally, through an ablation study, we show that each of the novel components of LlamaRestTest contributes to its overall performance.

## 13. LLMDroid: Enhancing Automated Mobile App GUI Testing Coverage with Large Language Model Guidance

**Authors:** Chenxu Wang (Huazhong University of Science and Technology), Tianming Liu (Monash Univerisity), Yanjie Zhao (Huazhong University of Science and Technology), Minghui Yang (OPPO), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715763

**中文总结:** 提出 LLMDroid，将移动 GUI 测试分为自主探索与 LLM 引导两阶段，仅在覆盖停滞时查询 LLM 以降低成本。应用于三款开源 Android 测试工具后，代码/Activity 覆盖平均提升 26.16%/29.31%，并可在约 $0.18/小时达到接近最优效果。

**Abstract:** With the rapid development of Large Language Models (LLMs), their integration into automated mobile GUI testing has emerged as a promising research direction. However, existing LLM-based testing approaches face significant challenges, including time inefficiency and high costs due to constant LLM querying. To address these issues, this paper introduces LLMDroid, a novel testing framework designed to enhance existing automated mobile GUI testing tools by leveraging LLMs more efficiently. The workflow of LLMDroid comprises two main stages: Autonomous Exploration and LLM Guidance. During Autonomous Exploration, LLMDroid utilizes existing testing tools while leveraging LLMs to summarize explored pages. When code coverage growth slows, it transitions to LLM Guidance to strategically direct testing towards unexplored functionalities. This approach minimizes LLM interactions while maximizing their impact on test coverage. We applied LLMDroid to three popular open-source Android testing tools and evaluated it on 14 top-listed apps from Google Play. Results demonstrate an average increase of 26.16% in code coverage and 29.31% in activity coverage. Furthermore, our cost analysis reveals that LLMDroid achieves optimal performance at $4.77 per hour using GPT-4o, with a cost-effective alternative achieving 78% of optimal performance at just $0.18 per hour. These findings highlight LLMDroid’s effectiveness in enhancing automated mobile app testing and its potential for widespread adoption.

## 14. MendelFuzz: The Return of the Deterministic Stage

**Authors:** Han Zheng (EPFL), Flavio Toffalini (EPFL, Switzerland and Ruhr-Universität Bochum, Germany), Marcel Böhme (MPI for Security and Privacy), Mathias Payer (EPFL)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifact-Available, Artifact-Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715713

**中文总结:** MendelFuzz 改进灰盒 fuzzer 的确定性变异阶段：发现约 20% 种子与 0.5% 字节贡献了绝大多数覆盖增益，并据此裁剪无效输入。实现已成为 AFL++ 默认选项，在 FuzzBench/Magma 上优于现有方法，并发现 8 个新 CVE。

**Abstract:** Can a fuzzer cover more code with minimal corruption of the initial seed? Before a seed is fuzzed, the early greybox fuzzers first systematically enumerated slightly corrupted inputs by applying every mutation operator to every part of the seed, once per generated input. The hope of this so-called “deterministic” stage was that simple changes to the seed would be less likely to break the complex file format; the resulting inputs would find bugs in the program logic well beyond the program’s parser. However, when experiments showed that disabling the deterministic stage achieves more coverage, i.e., applying multiple mutation operators at the same time to a single input, most fuzzers disabled the deterministic stage by default. Instead of ignoring the deterministic stage, we analyze its potential and substantially improve deterministic stage exploration. Our deterministic stage is now the default in AFL++, reverting the earlier decision of dropping deterministic exploration. We start by investigating the overhead and the contribution of the deterministic stage to the discovery of coverage-increasing inputs. While the sheer number of generated inputs explains the overhead, we find that only a few critical seeds (20%), and only a few critical bytes in a seed (0.5%) are responsible for the vast majority of the coverage-increasing inputs (83% and 84%, respectively). To cope with this issue, we develop an efficient technique, called MendelFuzz, to identify these critical seeds / bytes so as to prune a large number of unnecessary inputs. MendelFuzz retains the benefits of the classic deterministic stage by only enumerating a tiny part of the total deterministic state space. We evaluate MendelFuzz implementation on two benchmarking frameworks, FuzzBench and Magma. Our evaluation shows that MendelFuzz outperforms state-of-the-art fuzzers with and without the (old) deterministic stage enabled, both in terms of coverage and bug finding. MendelFuzz also discovered 8 new CVEs on exhaustively fuzzed security-critical applications. Finally, MendelFuzz has been independently evaluated and integrated into AFL++ as default option.

## 15. Multi-Modal Traffic Scenario Generation for Autonomous Driving System Testing

**Authors:** Zhi Tu (Purdue University), Liangkun Niu (Purdue University), Wei Fan (Purdue University), Tianyi Zhang (Purdue University)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729348

**中文总结:** TrafficComposer 结合自然语言描述与交通场景图像，在 CARLA/LGSVL 等仿真器中自动生成 ADS 测试场景。在 120 个场景基准上准确率 97.0%，生成场景可直接发现 37 个缺陷，并作为初始种子使两类 fuzzing 多发现 33%–124% 缺陷。

**Abstract:** Autonomous driving systems (ADS) require extensive testing and validation before deployment. However, it is tedious and time-consuming to construct traffic scenarios for ADS testing. In this paper, we propose TrafficComposer, a multi-modal traffic scenario construction approach for ADS testing. TrafficComposer takes as input a natural language description of a desired traffic scenario and a complementary traffic scene image. Then, it generates the corresponding traffic scenario in a simulator, such as CARLA and LGSVL. Specifically, TrafficComposer integrates high-level dynamic information about the traffic scenario from the NL description and intricate details about the surrounding vehicles, pedestrians, and the road network from the image. The information from the two modalities is complementary to each other and helps generate high-quality traffic scenarios for ADS testing. On a benchmark of 120 traffic scenarios, TrafficComposer achieves 97.0% accuracy, outperforming the best-performing baseline by 7.3%. Both direct testing and fuzz testing experiments on six ADSs prove the bug detection capabilities of the traffic scenarios generated by TrafficComposer. These scenarios can directly discover 37 bugs and help two fuzzing methods find 33%–124% more bugs serving as initial seeds.

## 16. On-Demand Scenario Generation for Testing Automated Driving Systems

**Authors:** Songyang Yan (Xi'an Jiaotong University), Xiaodong Zhang (Xidian University), Kunkun Hao (Synkrotron, Inc.), Haojie Xin (Xi'an Jiaotong University), Yonggang Luo (Chongqing Changan Automobile Co. Ltd), Jucheng Yang (Chongqing Changan Automobile Co. Ltd), Ming Fan (Xi'an Jiaotong University), Chao Yang (Xidian University), Jun Sun (Singapore Management University), Zijiang Yang (University of Science and Technology of China and Synkrotron, Inc.)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715722

**中文总结:** OSG 框架从真实交通数据学习，用 Risk Intensity Regulator 定量调控场景风险，并结合改进启发式搜索保证多样性，按需生成不同危险程度的 ADS 测试场景。在 Carla 上验证可跨风险级别比较 ADS，并揭示不同风险下事故类型差异。

**Abstract:** The safety and reliability of Automated Driving Systems (ADS) are paramount, necessitating rigorous testing methodologies to uncover potential failures before deployment. Traditional testing approaches often prioritize either natural scenario sampling or safety-critical scenario generation, resulting in overly simplistic or unrealistic hazardous tests. In practice, the demand for natural scenarios (e.g., when evaluating the ADS’s reliability in real-world conditions), critical scenarios (e.g., when evaluating safety in critical situations), or somewhere in between (e.g., when testing the ADS in regions with less civilized drivers) varies depending on the testing objectives. To address this issue, we propose the On-demand Scenario Generation (OSG) Framework, which generates diverse scenarios with varying risk levels. Achieving the goal of OSG is challenging due to the complexity of quantifying the criticalness and naturalness stemming from intricate vehicle-environment interactions, as well as the need to maintain scenario diversity across various risk levels. OSG learns from real-world traffic datasets and employs a Risk Intensity Regulator to quantitatively control the risk level. It also leverages an improved heuristic search method to ensure scenario diversity. We evaluate OSG on the Carla simulators using various ADSs. We verify OSG’s ability to generate scenarios with different risk levels and demonstrate its necessity by comparing accident types across risk levels. With the help of OSG, we are now able to systematically and objectively compare the performance of different ADSs based on different risk levels.

## 17. Standing on the Shoulders of Giants: Bug-Aware Automated GUI Testing via Retrieval Augmentation

**Authors:** Mengzhuo Chen (Institute of Software, Chinese Academy of Sciences), Zhe Liu (Institute of Software, Chinese Academy of Sciences), Chunyang Chen (TU Munich), Junjie Wang (Institute of Software at Chinese Academy of Sciences), Boyu Wu (University of Chinese Academy of Sciences, Beijing, China), Jun Hu (Institute of Software, Chinese Academy of Sciences), Qing Wang (Institute of Software at Chinese Academy of Sciences)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715755

**中文总结:** 提出 BugHunter，用 MLLM 与 RAG 从相似应用的 bug 报告中检索知识并生成探索路径，引导自动化 GUI 测试优先覆盖易触发缺陷的路径。相对最优基线缺陷检出提升约 60%，并在 Google Play 应用中新发现 49 个崩溃缺陷。

**Abstract:** In software development, similar apps often encounter similar bugs due to shared functionalities and implementation methods. However, current automated GUI testing methods mainly focus on generating test scripts to cover more pages by analyzing the internal structure of the app, without targeted exploration of paths that may trigger bugs, resulting in low efficiency in bug discovery. Considering that a large number of bug reports on open source platforms can provide external knowledge for testing, this paper proposes Bu g Hu n te r, a novel bug-aware automated GUI testing approach that generates exploration paths guided by bug reports from similar apps, utilizing a combination of multimodal large language models (MLLMs) and Retrieval-Augmented Generation (RAG). Instead of focusing solely on coverage, BugHunter dynamically adapts the testing process to target bug paths, thereby increasing bug detection efficiency. BugHunter first builds a high-quality bug knowledge base from historical bug reports. Then it retrieves relevant reports from this large bug knowledge base using a two-stage retrieval process, and generates test paths based on similar apps’ bug reports. BugHunter also introduces a local and global path-planning mechanism to handle differences in functionality and UI design across apps, and the ambiguous behavior or missing steps in the online bug reports. We evaluate BugHunter on 121 bugs across 71 apps and compare its performance against 16 state-of-the-art baselines. BugHunter achieves 60% improvement in bug detection over the best baseline, with comparable or higher coverage against the baselines. Furthermore, bu g successfully detects 49 new crash bugs in real-world apps from Google Play, with 33 bugs fixed, 9 confirmed, and 7 pending feedback.

## 18. TerzoN: Human-in-the-Loop Software Testing with a Composite Oracle

**Authors:** Matthew C. Davis (Carnegie Mellon University), Amy Wei (University of Michigan), Brad A. Myers (Carnegie Mellon University), Joshua Sunshine (Carnegie Mellon University)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729359

**中文总结:** 提出 Composite Oracle（隐式、基于属性与基于示例）及实现系统 TerzoN，统一展示三类预言机结果并发现断言不一致。相对 fast-check 的人机实验中，参与者多发现约 72% 缺陷、准确描述量翻倍，测试速度提升约 16%。

**Abstract:** Software testing is difficult, tedious, and costs an estimated $48–87 billion USD/year in US labor. Automatic test generation tools aim to ease this burden but have important trade-offs. Fuzzers use an implicit oracle that can detect obviously invalid results. However, there is no general solution to the oracle problem, and an implicit oracle cannot automatically evaluate correctness. Test suite generators like EvoSuite use the program under test as the oracle and therefore cannot evaluate correctness. Property-based testing (PBT) tools evaluate correctness, but users find it difficult to come up with properties to test, and to understand whether the properties are correct. Consequently, adoption of these tools has been narrow, and test suites continue to be created manually by practitioners, who often use an example-based oracle to specify correct input and output examples. To help bridge the gaps among oracles and tools, we present a Composite Oracle that incorporates implicit, property-based, and example-based oracles. To help us understand the practical properties of a Composite Oracle, we built TerzoN, an Automatic Test sUite Generator (ATUG) that implements a Composite Oracle. TerzoN displays all the test results in an integrated view composed from the results of the 3 types of oracles and finds some types of test assertion inconsistencies that might otherwise lead to misleading test results. We evaluated TerzoN with its Composite Oracle in a randomized controlled human trial with 14 professional software engineers using a popular industry tool, fast-check, as the control. Participants using TerzoN elicited 72% more bugs (p<0.01), accurately described more than twice the number of bugs (p<0.01) and tested 16% more quickly (p<0.05).

## 19. Understanding and Characterizing Mock Assertions in Unit Tests

**Authors:** Hengcheng Zhu (The Hong Kong University of Science and Technology), Valerio Terragni (University of Auckland), Lili Wei (McGill University), Shing-Chi Cheung (Hong Kong University of Science and Technology), Jiarong Wu, Yepang Liu (Southern University of Science and Technology)

**Categories:** Testing and Fuzzing

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715741

**中文总结:** 对 11 个流行 Java 项目中 4,652 个测试用例的 mock 断言进行首次实证研究，发现其多用于验证外部资源交互与关键路径是否被执行，并与传统断言互补。结果为支持 mock 断言的自动化测试生成奠定基础。

**Abstract:** Mock assertions provide developers with a powerful means to validate program behaviors that are unobservable to test assertions. Despite their significance, they are rarely considered by automated test generation techniques. Effective generation of mock assertions requires understanding how they are used in practice. Although previous studies highlighted the importance of mock assertions, none provide insight into their usages. To bridge this gap, we conducted the first empirical study on mock assertions, examining their adoption, the characteristics of the verified method invocations, and their effectiveness in fault detection. Our analysis of 4,652 test cases from 11 popular Java projects reveals that mock assertions are mostly applied to validating specific kinds of method calls, such as those interacting with external resources and those reflecting whether a certain code path was traversed in systems under test. Additionally, we find that mock assertions complement traditional test assertions by ensuring the desired side effects have been produced, validating control flow logic, and checking internal computation results. Our findings contribute to a better understanding of mock assertion usages and provide a foundation for future related research such as automated test generation that support mock assertions.

## 20. UnitCon: Synthesizing Targeted Unit Tests for Java Runtime Exceptions

**Authors:** Sujin Jang (KAIST), Yeonhee Ryou (KAIST), Heewon Lee (KAIST, Korea, South (The Republic of)), Kihong Heo (KAIST)

**Categories:** Testing and Fuzzing

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729362

**中文总结:** 提出 UNITCON，用静态分析估计候选测试语义以剪枝与排序搜索空间，合成针对 Java 运行时异常特定位置的定向单元测试。在 Java 程序集上显著优于现有面向回归覆盖的单元测试生成工具。

**Abstract:** We present UNITCON, a system for synthesizing targeted unit tests for runtime exceptions in Java programs. Targeted unit tests aim to reveal a bug at a specific location in the program under test. This capability benefits various tasks in software development, such as patch testing, crash reproduction, or static analysis alarm inspection. However, conventional unit test generation tools are mainly designed for regression tests by maximizing code coverage; hence they are not effective at such target-specific tasks. In this paper, we propose a novel synthesis technique that effectively guides the search for targeted unit tests. The key idea is to use static analysis to prune and prioritize the search space by estimating the semantics of candidate test cases. This allows us to efficiently focus on promising unit tests that are likely to reveal the target Exception. According to our experiments on a suite of Java programs, our approach significantly outperforms the state-of-the-art unit test generation tools.

## 21. VLATest: Testing and Evaluating Vision-Language-Action Models for Robotic Manipulation

**Authors:** Zhijie Wang (University of Alberta), Zhehua Zhou (University of Macau), Norman Song, Yuheng Huang (The University of Tokyo), Zhan Shu (University of Alberta), Lei Ma (The University of Tokyo & University of Alberta)

**Categories:** Testing and Fuzzing

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729343

**中文总结:** 提出 VLATest，对视觉-语言-动作（VLA）机器人操控模型进行场景模糊测试与评估。对七个代表性 VLA 模型的实证表明其鲁棒性不足，并量化障碍物、光照、相机姿态与未见物体等因素的影响。

**Abstract:** The rapid advancement of generative AI and multi-modal foundation models has shown significant potential in advancing robotic manipulation. Vision-language-action (VLA) models, in particular, have emerged as a promising approach for visuomotor control by leveraging large-scale vision-language data and robot demonstrations. However, current VLA models are typically evaluated using a limited set of hand-crafted scenes, leaving their general performance and robustness in diverse scenarios largely unexplored. To address this gap, we present VLATest, a fuzzing framework designed to generate robotic manipulation scenes for testing VLA models. Based on VLATest, we conducted an empirical study to assess the performance of seven representative VLA models. Our study results revealed that current VLA models lack the robustness necessary for practical deployment. Additionally, we investigated the impact of various factors, including the number of obstacles, lighting conditions, camera poses, and unseen objects, on the VLA model’s performance. Our findings highlight the limitations of existing VLA models, emphasizing the need for further research to develop reliable and trustworthy VLA applications.
