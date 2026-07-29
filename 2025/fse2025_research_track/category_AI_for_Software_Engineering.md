# FSE 2025 Research Track — AI for Software Engineering

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 23 papers

## 1. A Knowledge Enhanced Large Language Model for Bug Localization

**Authors:** Yue Li (Nanjing University), Bohan Liu (Nanjing University), Ting Zhang (Singapore Management University), Zhiqi Wang (Nanjing University), David Lo (Singapore Management University), Lanxin Yang (Nanjing University), Jun Lyu (Nanjing University), He Zhang (Nanjing University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729356

**中文总结:** 提出 KEPT，从项目文档与历史代码构建知识图谱，经 soft-position embedding 与可见矩阵注入 LLM 以增强缺陷定位；在 7 个开源项目 6000+ 缺陷报告上相对 Locus 与 CodeT5 显著提升 MRR/MAP/Top@N。

**Abstract:** A significant number of bug reports are generated every day as software systems continue to develop. Large Language Models (LLMs) have been used to correlate bug reports with source code to locate bugs automatically. The existing research has shown that LLMs are effective for bug localization and can increase software development efficiency. However, these studies still have two weaknesses. First, these models fail to capture context information about bug reports and source code. Second, these models are unable to understand the domain-specific expertise inherent to particular projects, such as version information in projects that are composed of alphanumeric characters without any semantic meaning. To address these challenges, we propose a K nowledge E nhanced P re- T rained model using project documents and historical code, called KEPT , for bug localization. Project documents record, revise, and restate project information that provides rich semantic information about those projects. Historical code contains rich code semantic information that can enhance the reasoning ability of LLMs. Specifically, we construct knowledge graphs from project documents and source code. Then, we introduce knowledge graphs to the LLM through soft-position embedding and visible matrices, enhancing its contextual and professional reasoning ability. To validate our model, we conducted a series of experiments on seven open-source software projects with over 6,000 bug reports. Compared with the traditional model ( ie Locus ), \ourapproach performs better by 33.2% to 59.5% in terms of mean reciprocal rank, mean average precision, and Top@N. Compared with the best-performing LLM ( ie CodeT5 ) \ourapproach achieves an improvement of 36.6% to 63.7%. The results indicate that introducing knowledge graphs can enhance the effectiveness of the LLM in bug localization.

## 2. AlphaTrans: A Neuro-Symbolic Compositional Approach for Repository-Level Code Translation and Validation

**Authors:** Ali Reza Ibrahimzada (University of Illinois Urbana-Champaign), Kaiyao Ke (University of Illinois Urbana-Champaign), Mrigank Pawagi (Indian Institute of Science, Bengaluru), Muhammad Salman Abid (Cornell University), Rangeet Pan (IBM Research), Saurabh Sinha (IBM Research), Reyhaneh Jabbarvand (University of Illinois at Urbana-Champaign)

**Categories:** AI for Software Engineering

**Artifact badges:** Artifact-Available, Artifact-Functional

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729379

**中文总结:** 提出神经符号方法 AlphaTrans，按程序分析碎片化并以逆调用序做仓库级代码与测试翻译，多层校验功能保持；在 10 个真实项目上 99.1% 片段语法正确、25.8% 通过运行/功能验证，并支持人工修复报告。

**Abstract:** Code translation transforms programs from one programming language (PL) to another. One prominent use case is application modernization to enhance maintainability and reliability. Several rule-based transpilers have been designed to automate code translation between different pairs of PLs. However, the rules can become obsolete as the PLs evolve and cannot generalize to other PLs. Recent studies have explored the automation of code translation using Large Language Models (LLMs). One key observation is that such techniques may work well for crafted benchmarks but fail to generalize to the scale and complexity of real-world projects with inter- and intra-class dependencies, custom types, PL-specific features, etc. We propose AlphaTrans, a neuro-symbolic approach to automate \emph{repository-level} code translation. AlphaTrans translates both source and test code, and employs multiple levels of validation to ensure the translation preserves the functionality of the source program. To break down the problem for LLMs, AlphaTrans leverages program analysis to decompose the program into fragments and translates them in the reverse call order. We leveraged AlphaTrans to translate ten real-world open-source projects consisting of <836, 8575, 2719> classes, methods, and tests. AlphaTrans translated the entire repository of these projects consisting of 6899 source code fragments. 99.1% of the translated code fragments are syntactically correct, and AlphaTrans validates the translations’ runtime behavior and functional correctness for 25.8%. On average, the integrated translation and validation take 36 hours (min=4, max=122) to translate a project, showing its scalability in practice. For the syntactically or semantically incorrect translations, AlphaTrans generates a report including existing translation, stack trace, test errors, or assertion failures. We provided these artifacts to two developers to fix the translation bugs in four projects. They were able to fix the issues in 20.1 hours on average (5.5 hours for the smallest and 34 hours for the largest project) and achieve all passing tests. Without AlphaTrans, translating and validating such big projects could take weeks, if not months.

## 3. Beyond Functional Correctness: Investigating Coding Style Inconsistencies in Large Language Models

**Authors:** Yanlin Wang (Sun Yat-sen University), Tianyue Jiang (Sun Yat-sen University), Mingwei Liu (Sun Yat-Sen University), Jiachi Chen (Sun Yat-sen University), Mingzhi Mao (Sun Yat-sen University), Xilin Liu (Huawei Cloud), Yuchi Ma (Huawei Cloud Computing Technologies), Zibin Zheng (Sun Yat-sen University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715749

**中文总结:** 实证比较主流 Code LLM 与人类代码在可读性、简洁性与鲁棒性上的风格差异，归纳不一致分类；并分析成因、给出缓解方案，强调不应只关注功能正确性。

**Abstract:** Large language models (LLMs) have brought a paradigm shift to the field of code generation, offering the potential to enhance the software development process. However, previous research mainly focuses on the accuracy of code generation, while coding style differences between LLMs and human developers remain under-explored. In this paper, we empirically analyze the differences in coding style between the code generated by mainstream Code LLMs and the code written by human developers, and summarize coding style inconsistency taxonomy. Specifically, we first summarize the types of coding style inconsistencies by manually analyzing a large number of generation results. We then compare the code generated by Code LLMs with the code written by human programmers in terms of readability, conciseness, and robustness. The results reveal that LLMs and developers have different coding styles. Additionally, we study the possible causes of these inconsistencies and provide some solutions to alleviate the problem.

## 4. Beyond PEFT: Layer-Wise Optimization for More Effective and Efficient Large Code Model Tuning

**Authors:** Chaozheng Wang (The Chinese University of Hong Kong), jiafeng (University of Electronic Science and Technology of China), Shuzheng Gao (Chinese University of Hong Kong), Cuiyun Gao (Harbin Institute of Technology, Shenzhen), Li Zongjie (Hong Kong University of Science and Technology), Ting Peng (Tencent Inc.), Hailiang Huang (Tencent Inc.), Yuetang Deng (Tencent), Michael Lyu (Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729341

**中文总结:** 在五项含公有/私有数据的代码智能任务上发现 PEFT 与全参微调差距显著（尤其私有数据）；提出逐层更新的 LWO，无需额外组件，私有行级补全相对 LoRA 准确率/BLEU 提升 22%/12%，训练时间平均减 42.7%。

**Abstract:** Large Code Models (LCMs) have demonstrated remarkable effectiveness across various code intelligence tasks. Supervised fine-tuning is essential to optimize their performance for specific downstream tasks. Compared with the traditional full-parameter fine-tuning (FFT) method, Parameter-Efficient Fine-Tuning (PEFT) methods can train LCMs with substantially reduced resource consumption and have gained widespread attention among researchers and practitioners. While existing studies have explored PEFT methods for code intelligence tasks, they have predominantly focused on a limited subset of scenarios, such as code generation with publicly available datasets, leading to constrained generalizability of the findings. To mitigate the limitation, we conduct a comprehensive study on exploring the effectiveness of the PEFT methods, which involves five code intelligence tasks containing both public and private data. Our extensive experiments reveal a considerable performance gap between PEFT methods and FFT, which is contrary to the findings of existing studies. We also find that this disparity is particularly pronounced in tasks involving private data. To improve the tuning performance for LCMs while reducing resource utilization during training, we propose a Layer-Wise Optimization (\method) strategy in the paper. /method incrementally updates the parameters of each layer in the whole model architecture, without introducing any additional component and inference overhead. Experiments across five LCMs and five code intelligence tasks demonstrate that LWO trains LCMs more effectively and efficiently compared to previous PEFT methods, with significant improvements in tasks using private data. For instance, in the line-level code completion task using our private code repositories, LWO outperforms the state-of-the-art LoRA method by 22% and 12% in terms of accuracy and BLEU scores, respectively. Furthermore, \method can enable more efficient LCM tuning, reducing the training time by an average of 42.7% compared to LoRA.

## 5. Calibration of Large Language Models on Code Summarization

**Authors:** Yuvraj Virk (UC Davis), Prem Devanbu (University of California at Davis), Toufique Ahmed (IBM Research)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729400

**中文总结:** 将代码摘要质量建模为校准问题：仅凭 LLM 摘要估计其是否足够像人类撰写；在多模型、多语言与多设定下探索可靠置信度预测方法。

**Abstract:** A good summary can often be very useful during program comprehension. While a brief, fluent, and relevant summary can be helpful, it does require significant human effort to produce. Often, good summaries are unavailable in software projects, thus making maintenance more difficult. There has been a considerable body of research into automated AI-based methods, using Large Language models (LLMs), to generate summaries of code; there also has been quite a bit work on ways to measure the performance of such summarization methods, with special attention paid to how closely these AI-generated summaries resemble a summary a human might have produced. Measures such as BERTScore and BLEU have been suggested and evaluated with human-subject studies. However, prior work has noted that LLM-produced summaries can be too long, disfluent, irrelevant, etc: generally, too dissimilar to what a human might say. Given an LLM-produced code summary, how can we judge if a summary is good enough? Given some input source code, and an LLM-generated summary, existing approaches can help judge brevity, fluency and relevance; however, it’s difficult to gauge whether an LLM-produced summary sufficiently resembles what a human might produce, without a “golden” human-produced summary to compare against. Prior research indicates that human-produced summaries are generally preferred by human-raters, so we explore this issue in this paper. We study this resemblance question as a calibration problem: given just the summary from an LLM, can we compute a confidence measure, that provides a reliable indication of whether the summary sufficiently resembles what a human would have produced in this situation? We examine this question using several LLMs, for several languages, and in several different settings. Our investigation suggests approaches to provide reliable predictions of the likelihood that an LLM-generated summary would sufficiently resemble a summary a human might write for the same code.

## 6. COFFE: A Code Efficiency Benchmark for Code Generation

**Authors:** Yun Peng (The Chinese University of Hong Kong), Jun Wan (Zhejiang University), Yichen LI (The Chinese University of Hong Kong), Xiaoxue Ren (Zhejiang University)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715727

**中文总结:** 提出代码生成时间效率基准 COFFE（函数级 398、文件级 358 题），含压力测试用例生成与基于 CPU 指令数的 efficient@k 指标；评估 14 个主流 LLM 并总结四项发现与实践启示。

**Abstract:** Code generation has largely improved development efficiency in the era of large language models (LLMs). With the ability to follow instructions, current LLMs can be prompted to generate code solutions given detailed descriptions in natural language. Many research efforts are being devoted to improving the correctness of LLM-generated code, and many benchmarks are proposed to evaluate the correctness comprehensively. Despite the focus on correctness, the time efficiency of LLM-generated code solutions is under-explored. Current correctness benchmarks are not suitable for time efficiency evaluation since their test cases cannot well distinguish the time efficiency of different code solutions. Besides, the current execution time measurement is not stable and comprehensive, threatening the validity of the time efficiency evaluation. To address the challenges in the time efficiency evaluation of code generation, we propose COFFE, a code generation benchmark for evaluating the time efficiency of LLM-generated code solutions. COFFE contains 398 and 358 problems for function-level and file-level code generation, respectively. To improve the distinguishability, we design a novel stressful test case generation approach with contracts and two new formats of test cases to improve the accuracy of generation. For the time evaluation metric, we propose efficienct@k based on CPU instruction count to ensure a stable and solid comparison between different solutions. We evaluate 14 popular LLMs on COFFE and identify four findings. Based on the findings, we draw some implications for LLM researchers and software practitioners to facilitate future research and usage of LLMs in code generation.

## 7. CRISPE: Semantic-Guided Execution Planning and Dynamic Reasoning for Enhancing Code Coverage Prediction

**Authors:** Hridya Dhulipala (University of Texas at Dallas), Aashish Yadavally (University of Texas at Dallas), Smit Soneshbhai Patel (University of Texas at Dallas), Tien N. Nguyen (University of Texas at Dallas)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729401

**中文总结:** 提出 CRISPE，以语句语义与当前已覆盖语句相对可行覆盖选项的观察引导 LLM 模拟执行规划，预测代码覆盖；在真实数据上精确匹配与语句匹配均优于基线，并可下游用于不完整代码的运行时错误预测。

**Abstract:** While LLMs excel in understanding source code and descriptive texts for tasks like code generation, code completion, etc., they exhibit weaknesses in predicting dynamic program behavior, such as code coverage and runtime error detection, which typically require program execution. Aiming to advance the capability of LLMs in reasoning and predicting the program behavior at runtime, we present CRISPE (short for Coverage Rationalization and Intelligent Selection ProcedurE), a novel approach for code coverage prediction that guides an LLM in simulating program execution via an execution plan based on two key factors: (1) program semantics of each statement type, and (2) the observation of current set of covered statements at the current “execution” step relative to all feasible code coverage options. We frame code coverage prediction as a process of semantic-guided execution-based planning, where feasible coverage options are utilized to assess whether the LLM is heading in the correct reasoning. We enhance the traditional generative task with the retrieval-based framework on feasible options of code coverage. Our experiments on real-world data show that CRISPE achieves high accuracy in coverage prediction in terms of both exact-match and statement-match coverage metrics, improving over the baselines. We also show that with semantic-guiding and dynamic reasoning from CRISPE, the LLM generates more correct planning steps. To demonstrate CRISPE’s usefulness, we used it in the downstream task of predicting runtime error(s) for the given inputs of incomplete code snippets.

## 8. CXXCrafter: An LLM-Based Agent for Automated C/C++ Open Source Software Building

**Authors:** Zhengmin Yu (Fudan University), Yuan Zhang (Fudan University), Ming Wen (Huazhong University of Science and Technology), Yinan Nie (Fudan University), Zhang Wenhui (Fudan University), Min Yang (Fudan University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729386

**中文总结:** 基于对 C/C++ 项目构建挑战的实证，提出 LLM 智能体 CXXCrafter 自动处理依赖、构建系统与错误修复；在开源软件上构建成功率 78%，可大幅节省人工并便于规模化应用。

**Abstract:** Project building is pivotal to support various program analysis tasks, such as generating intermediate represen- tation code for static analysis and preparing binary code for vulnerability reproduction. However, automating the building process for C/C++ projects is a highly complex endeavor, involving tremendous technical chal- lenges, such as intricate dependency management, diverse build systems, varied toolchains, and multifaceted error handling mechanisms. Consequently, building C/C++ projects often proves difficult in practice, hindering the progress of crucial downstream applications. Unfortunately, research on facilitating the building of C/C++ projects remains insufficient. The emergence of Large Language Models (LLMs) offers promising solutions to the above-mentioned challenges. Trained on extensive corpora, LLMs can help unify diverse build systems through their comprehension capabilities and address complex errors by leveraging tacit knowledge storage. Moreover, LLM-based systems, such as agents, can be systematically designed to dynamically interact with the environment, effectively managing dynamic building issues. Motivated by these opportunities, we conduct an empirical study to systematically analyze the current challenges in the C/C++ project building process. Particularly, we observe that most popular C/C++ projects encounter an average of five errors when relying solely on the build systems. Based on our study, we develop an automated build system called CXXCrafter to specifically address the above-mentioned challenges. Our evaluation on open-source software demonstrates that CXXCrafter achieves a success rate of 78% in project building. Specifically, among the Top100 dataset, 72 projects are built successfully by both CXXCrafter and manual efforts, 3 by CXXCrafter only, and 14 manually only. Despite the slightly lower performance, CXXCrafter can save tremendous manual efforts and can also be easily applied to a wider range of applications automatically.

## 9. DeclarUI: Bridging Design and Development with Automated Declarative UI Code Generation

**Authors:** Ting Zhou (Huazhong University of Science and Technology), Yanjie Zhao (Huazhong University of Science and Technology), Xinyi Hou (Huazhong University of Science and Technology), Xiaoyu Sun (Australian National University, Australia), Kai Chen (Huazhong University of Science and Technology), Haoyu Wang (Huazhong University of Science and Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715726

**中文总结:** 提出 DeclarUI，融合 CV、多模态 LLM 与编译器驱动迭代优化，从 UI 设计生成声明式 UI 代码并用 Page Transition Graphs 建模页面交互；在 React Native 上 PTG 覆盖率 96.8%、编译成功率 98%，并可泛化到 Flutter 与 ArkUI。

**Abstract:** Declarative UI frameworks have gained widespread adoption in mobile app development, offering benefits such as improved code readability and easier maintenance. Despite these advantages, the process of translating UI designs into functional code remains challenging and time-consuming. Recent advancements in multimodal large language models (MLLMs) have shown promise in directly generating mobile app code from user interface (UI) designs. However, the direct application of MLLMs to this task is limited by challenges in accurately recognizing UI components and comprehensively capturing interaction logic. To address these challenges, we propose DeclarUI, an automated approach that synergizes computer vision (CV), MLLMs, and iterative compiler-driven optimization to generate and refine declarative UI code from designs. DeclarUI enhances visual fidelity, functional completeness, and code quality through precise component segmentation, Page Transition Graphs (PTGs) for modeling complex inter-page relationships, and iterative optimization. In our evaluation, DeclarUI outperforms baselines on React Native, a widely adopted declarative UI framework, achieving a 96.8% PTG coverage rate and a 98% compilation success rate. Notably, DeclarUI demonstrates significant improvements over state-of-the-art MLLMs, with a 123% increase in PTG coverage rate, up to 55% enhancement in visual similarity scores, and a 29% boost in compilation success rate. We further demonstrate DeclarUI’s generalizability through successful applications to Flutter and ArkUI frameworks. User studies with professional developers confirm that DeclarUI’s generated code meets industrial-grade standards in code availability, modification time, readability, and maintainability. By streamlining app development, improving efficiency, and fostering designer-developer collaboration, DeclarUI offers a practical solution to the persistent challenges in mobile UI development.

## 10. Demystifying LLM-based Software Engineering Agents

**Authors:** Chunqiu Steven Xia (University of Illinois at Urbana-Champaign), Yinlin Deng (University of Illinois at Urbana-Champaign), Soren Dunn (University of Illinois Urbana-Champaign), Lingming Zhang (University of Illinois at Urbana-Champaign)

**Categories:** AI for Software Engineering

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715754

**中文总结:** 提出无需复杂自主智能体的 Agentless，仅用定位、修复、补丁验证三阶段解决软件开发问题；在 SWE-bench Lite 上达到 32.67%（98 个正确修复）且成本约 $0.68，优于现有开源软件智能体，并被 OpenAI 用作展示基准。

**Abstract:** Recent advancements in large language models (LLMs) have significantly advanced the automation of software development tasks, including code synthesis, program repair, and test generation. More recently, researchers and industry practitioners have developed various autonomous LLM agents to perform end-to-end software development tasks. These agents are equipped with the ability to use tools, run commands, observe feedback from the environment, and plan for future actions. However, the complexity of these agent-based approaches, together with the limited abilities of current LLMs, raises the following question: Do we really have to employ complex autonomous software agents? To attempt to answer this question, we build Agentless – an agentless approach to automatically resolve software development issues. Compared to the verbose and complex setup of agent-based approaches, Agentless employs a simplistic three-phase process of localization, repair, and patch validation, without letting the LLM decide future actions or operate with complex tools. Our results on the popular SWE-bench Lite benchmark show that surprisingly the simplistic Agentless is able to achieve both the highest performance (32.67%, 98 correct fixes) and low cost ($0.68) compared with all existing open-source software agents! In fact, Agentless has already been adopted by OpenAI as the go-to approach to showcase the real-world coding performance of both GPT-4o and the new OpenAI o1 models . Furthermore, we manually classified the problems in SWE-bench Lite and found problems with exact ground truth patches or insufficient/misleading issue descriptions. As such, we construct SWE-bench Lite-𝑆 by excluding such problematic issues to perform more rigorous evaluation and comparison. Our work highlights the currently overlooked potential of a simplistic, cost-effective technique in autonomous software development. We hope Agentless will help reset the baseline, starting point, and horizon for autonomous software agents, and inspire future work along this crucial direction.

## 11. Demystifying Memorization in LLM-based Program Repair via a General Hypothesis Testing Framework

**Authors:** Jiaolong Kong (Singapore Management University), Xiaofei Xie (Singapore Management University), Shangqing Liu (Nanyang Technological University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729390

**中文总结:** 将 LLM 程序修复中的记忆化检测形式化为假设检验框架，并设计真实补丁匹配与大幅变异后重评估两种方法；发现 Defects4J 上大量正确补丁与真实修复完全一致，且变异后仍常复现原修复，现有检测器 AUROC 多低于 0.5。

**Abstract:** Large Language Models (LLMs) have achieved remarkable success in various applications, particularly in code-related tasks such as code generation and program repair, setting new performance benchmarks. However, the extensive use of large training corpora raises concerns about whether these achievements stem from genuine understanding or mere memorization of training data—a question often overlooked in current research. This paper aims to study the memorization issue within LLM-based program repair by investigating whether the correct patches generated by LLMs are the result of memorization. The key challenge lies in the absence of ground truth for confirming memorization, leading to various ad-hoc methods designed for its detection. To address this challenge, we first propose a general framework that formalizes memorization detection as a general hypothesis testing problem, where existing approaches can be unified by defining a \textit{low-probability event} under the \textit{null hypothesis} that the data is not memorized. The occurrence of such an event leads to the rejection of the null hypothesis, indicating potential memorization. Based on this framework, we design two specific methods (i.e., low-probability events) to detect potential memorization: 1) basic ground-truth matching, and 2) reassessment after substantial code mutation. We investigate the memorization issue in LLM-based program repair using two datasets: Defects4J, a widely used benchmark that is likely included in the training data, and GitBug-Java, a new dataset that is unlikely to be part of the training data. Our findings reveal that a significant portion of correct patches exactly match the ground truths in Defects4J (e.g., 78.83% and 87.42% on GPT-3.5 and CodeLlama-7b, respectively). Moreover, even after significant modifications to the buggy code, where the original repairs should not be generated, a considerable percentage of bugs (e.g., 81.82% on GPT-3.5 and 88.24% on CodeLlama-7b) continue to be fixed exactly as in the original bug fixes, indicating a high likelihood of memorization. Furthermore, we evaluate existing memorization detection methods and demonstrate their ineffectiveness in this context (e.g., most AUROCs are below 0.5). The theoretical analysis under our hypothesis testing framework shows that their defined events may not meet the requirements for being low-probability. The study highlights the critical need for more robust and rigorous evaluations in LLM-based software engineering research, ensuring a clear distinction between true problem-solving capabilities and mere memorization.

## 12. DiSCo: Towards Decompiling EVM Bytecode to Source Code using Large Language Models

**Authors:** Xing Su (National Key Lab for Novel Software Technology, Nanjing University, China), Hanzhong Liang (National Key Lab for Novel Software Technology, Nanjing University, China), Hao Wu, Ben Niu (State Key Laboratory of Information Security, Institute of Information Engineering, China), Fengyuan Xu (National Key Lab for Novel Software Technology, Nanjing University, China), Sheng Zhong (National Key Lab for Novel Software Technology, Nanjing University, China)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729373

**中文总结:** 提出首个基于 LLM 的 EVM 字节码反编译流水线 DiSCo，经逻辑不变中间表示、类型感知图语义增强与规范引导提示生成 Solidity；编译成功率约 75%，差分模糊通过率约 50%，在理解与攻击复现上优于基线。

**Abstract:** Understanding the Ethereum smart contract bytecode is essential for ensuring cryptoeconomics security. However, existing decompilers primarily convert bytecode into pseudocode, which is not easily comprehensible for general users, potentially leading to misunderstanding of contract behavior and increased vulnerability to scams or exploits. In this paper, we propose DiSCo, the first LLMs-based EVM decompilation pipeline, which aims to enable LLMs to understand the opaque bytecode and lift it into smart contract code. DiSCo introduces three core technologies. First, a logic-invariant intermediate representation is proposed to reproject the low-level bytecode into high-level abstracted units. The second technique involves semantic enhancement based on a novel type-aware graph model to infer stripped variables during compilation, enhancing the lifting effect. The third technology is a flexible method incorporating code specifications to construct LLM-comprehensible prompts for source code generation. Extensive experiments illustrate that our generated code guarantees a high compilability rate at 75%, with differential fuzzing pass rate averaging at 50%. Manual validation results further indicate that the generated solidity contracts significantly outperforms baseline methods in tasks such as code comprehension and attack reproduction.

## 13. Divide-and-Conquer: Generating UI Code from Screenshots

**Authors:** Yuxuan Wan (The Chinese University of Hong Kong), Chaozheng Wang (The Chinese University of Hong Kong), Yi Dong (The Chinese University of Hong Kong), Wenxuan Wang (Chinese University of Hong Kong), Shuqing Li (The Chinese University of Hong Kong), Yintong Huo (Singapore Management University), Michael Lyu (Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729364

**中文总结:** 提出 DCGen，将网页截图分段后分别生成描述再重组为完整 UI 代码，以缓解 MLLM 的元素遗漏、扭曲与错排；在真实网站上视觉相似度最多提升 14%，人工评估显示可更快实现更接近设计的页面。

**Abstract:** Websites are critical in today’s digital world, with over 1.11 billion currently active and approximately 252,000 new sites launched daily. Converting website layout design into functional UI code is a time-consuming yet indispensable step of website development. Manual methods of converting visual designs into functional code present significant challenges, especially for non-experts. To explore automatic design-to-code solutions, we first conduct a motivating study on GPT-4o and identify three types of issues in generating UI code: element omission, element distortion, and element misarrangement. We further reveal that a focus on smaller visual segments can help multimodal large language models (MLLMs) mitigate these failures in the generation process. In this paper, we propose DCGen, a divide-and-conquer-based approach to automate the translation of webpage design to UI code. DCGen starts by dividing screenshots into manageable segments, generating descriptions for each segment, and then reassembling them into complete UI code for the entire screenshot. We conduct extensive testing with a dataset comprised of real-world websites and various MLLMs and demonstrate that DCGen achieves up to a 14% improvement in visual similarity over competing methods. Human evaluations show that DCGen can help developers implement webpages significantly faster and more similar to the UI designs. To the best of our knowledge, DCGen is the first segment-aware MLLM-based approach for generating UI code directly from screenshots.

## 14. Enhancing Web Accessibility: Automated Detection of Issues with Generative AI

**Authors:** Ziyao He (University of California, Irvine), Syed Fatiul Huq (University of California, Irvine), Sam Malek (University of California at Irvine)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729371

**中文总结:** 基于 WCAG 可测成功准则，提出用生成式 AI 抽取页面元素并经 LLM 检测可访问性问题的自动化工具。评估精度 95.2%、召回 87.69%，在真实网站上平均比现有工具组合多发现 8 类违规。

**Abstract:** Websites are integral to people’s daily lives, with billions in use today. However, due to limited awareness of accessibility and its guidelines, developers often release web apps that are inaccessible to people with disabilities, who make up around 16% of the global population. To ensure a baseline of accessibility, software engineers rely on automated checkers that assess a webpage’s compliance based on predefined rules. Unfortunately, these tools typically cover only a small subset of accessibility guidelines and often overlook violations that require a semantic understanding of the webpage. The advent of generative AI, known for its ability to comprehend textual and visual content, has created new possibilities for detecting accessibility violations. We began by studying the most widely used guideline, WCAG, to determine the testable success criteria that generative AI could address. This led to the development of an automated tool called \name, which extracts elements from a page related to each success criterion and inputs them into an LLM prompted to detect accessibility issues on the web. Evaluations of \name showed its effectiveness, with a precision of 95.2% and a recall of 87.69%. Additionally, when tested on real websites, \name identified an average of 8 more types of accessibility violations than the combination of existing tools.

## 15. Impact of Request Formats on Effort Estimation: Are LLMs Different than Humans?

**Authors:** Gül Calikli (University of Glasgow), Mohammed Alhamed (Applied Behaviour Systems LTD (Hexis), United Kingdom)

**Categories:** AI for Software Engineering

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715771

**中文总结:** 复现人类实验，检验 GPT-4、Gemini 1.5 Pro、Llama 3.1 在工作量估计中从传统请求格式切换到替代格式时的反应。LLM 同样给出更低估计并表现出类似锚定偏差的模式，与软件从业者行为一致。

**Abstract:** Expert judgment is the dominant strategy used for software development effort estimation. Yet, expert-based judgment can provide over-optimistic effort estimates, leading to projects’ poor budget planning and cost. and time overruns. Large Language Models (LLMs) are good candidates to assist software professionals in effort estimation. However, their effective leveraging for software development effort estimation requires thoroughly investigating their limitations and to what extent they overlap with those of (human) software practitioners. One primary limitation of LLMs is the sensitivity of their responses to prompt changes. Similarly, empirical studies showed that changes in the request format (e.g., rephrasing) could impact (human) software professionals’ effort estimates. In this paper, we replicated a series of experiments, which were initially conducted with (human) software professionals in the literature, to see how LLMs’ effort estimates change due to the transition from the traditional request format (i.e., ”How much effort is required to complete X?”) to the alternative request format (i.e., ”How much can be completed in Y work hours?”). Our experiments involved three different LLMs (GPT-4, Gemini 1.5 Pro, Llama 3.1) and 88 software project specifications (per treatment in each experiment), resulting in 880 prompts, in total that we prepared using 704 user stories from 3 open-source projects (Hyperledger Fabric, Mulesoft Mule, Spring XD). Our findings align with the original experiments conducted with software professionals: The first four experiments showed that LLMs provide lower effort estimates due to transitioning from the traditional to the alternative request format. The findings of the fifth and first experiments detected that LLMs display patterns analogous to anchoring bias, a human cognitive bias defined as the tendency to stick to the anchor (i.e., the ”Y work-hours” in the alternative request format).

## 16. Integrating Large Language Models and Reinforcement Learning for Non-Linear Reasoning

**Authors:** Yoav Alon (University of Bristol), Cristina David (University of Bristol)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715761

**中文总结:** 提出由强化学习 Agent 引导 LLM 探索解空间的架构，使 LLM 专注下一步并支持非线性回溯，以缓解长期规划不足。在程序等价任务上相对 Chain of Thought 与 Tree of Thoughts 表现更好。

**Abstract:** Large Language Models (LLMs) were shown to struggle with long-term planning, which may be caused by the limited way in which they explore the space of possible solutions. We propose an architecture where a Reinforcement Learning (RL) Agent guides an LLM’s space exploration: (1) the Agent has access to domain-specific information, and can therefore make decisions about the quality of candidate solutions based on specific and relevant metrics, which were not explicitly considered by the LLM’s training objective; (2) the LLM can focus on generating immediate next steps, without the need for long-term planning. We allow non-linear reasoning by exploring alternative paths and backtracking. We evaluate this architecture on the program equivalence task, and compare it against Chain of Thought (CoT) and Tree of Thoughts (ToT). We assess both the downstream task, denoting the binary classification, and the intermediate reasoning steps. Our approach compares positively against CoT and ToT.

## 17. LLM-based Method Name Suggestion with Automatically Generated Context-Rich Prompts

**Authors:** Waseem Akram (Beijing Institute of Technology), Yanjie Jiang (Peking University), Yuxia Zhang (Beijing Institute of Technology), Haris Ali Khan (Beijing Institute of Technology), Hui Liu (Beijing Institute of Technology)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715753

**中文总结:** 提出 ContextCraft，根据功能描述检索相似示例并抽取可能出现的名字 token、语义枢轴词与评估结果，自动构造上下文丰富提示以驱动 LLM 建议方法名。在 43k Java/Python 方法上较 RNN-att-Copy 精确匹配提升 52%，编辑距离降低 32%。

**Abstract:** Accurate method naming is crucial for code readability and maintainability. However, manually creating concise and meaningful names remains a significant challenge. To this end, in this paper, we propose an approach based on Large Language Model (LLMs) to suggest method names according to function descriptions. The key of the approach is ContextCraft , an automated algorithm for generating context-rich prompts for LLM that suggests the expected method names according to the prompts. For a given query (functional description), it retrieves a few best examples whose functional descriptions have the greatest similarity with the query. From the examples, it identifies tokens that are likely to appear in the final method name as well as their likely positions, picks up pivot words that are semantically related to tokens in the according method names, and specifies the evaluation results of the LLM on the selected examples. All such outputs (tokens with probabilities and position information, pivot words accompanied by associated name tokens and similarity scores, and evaluation results) together with the query and the selected examples are then filled in a predefined prompt template, resulting in a context-rich prompt. This context-rich prompt reduces the randomness of LLMs by focusing the LLM’s attention on relevant contexts, constraining the solution space, and anchoring results to meaningful semantic relationships. Consequently, the LLM leverages this prompt to generate the expected method name, producing a more accurate and relevant suggestion. We evaluated the proposed approach with 43k real-world Java and Python methods accompanied by functional descriptions. Our evaluation results suggested that it significantly outperforms the state-of-the-art approach RNN-att-Copy , improving the chance of exact match by 52% and decreasing the edit distance between generated and expected method names by 32%. Our evaluation results also suggested that the proposed approach worked well for various LLMs, including ChatGPT-3.5, ChatGPT-4, ChatGPT-4o, Gemini-1.5, and Llama-3.

## 18. MiSum: Multi-Modality Heterogeneous Code Graph Learning for Multi-Intent Binary Code Summarization

**Authors:** Kangchen Zhu (National university of Defense Technology), Zhiliang Tian (National University of Defense Technology), Shangwen Wang (National University of Defense Technology), Weiguo Chen (National University of Defense Technology), Zixuan Dong (National University of Defense Technology), mingyue leng (National University of Defense Technology), Xiaoguang Mao (National University of Defense Technology)

**Categories:** AI for Software Engineering

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715780

**中文总结:** MiSum 面向多意图二进制代码摘要，构建统一多模态异构代码图（MM-HCG）融合汇编与伪代码，并用意图感知注意力生成定制摘要。在多种架构与优化级别上 BLEU/METEOR/ROUGE-L 优于现有基线，人工评估亦支持逆向工程师理解多元意图。

**Abstract:** The current landscape of binary code summarization predominantly revolves around the generation of a single summarization, limiting the scope of understanding and usability for reverse engineers. The existing approaches often fail to address the multifaceted needs of users, such as detailed insights into usage patterns, implementation nuances, and design rationale, as highlighted in the domain of source code summarization. Consequently, the necessity of multi-intent binary code summarization, an essential way to enhance the efficacy of reverse engineering processes, is underscored. To address this gap, our basic observation is that the two types of information essential for binary code summarization (i.e., the assembly code and pseudo code) can complement each other well. Specifically, the assembly code, characterized by its low-level nature, intricately delineates the execution logic, whereas the pseudo code, operating at a higher level, retains valuable contextual information. Based on this insight, we propose MiSum, a novel multi-modality heterogeneous code graph alignment and learning method to integrate information from both assembly code and pseudo code. MiSum introduces a unified multi-modality heterogeneous code graph (MM-HCG) that achieves alignment between assembly code graph and pseudo code graph and carries low-level execution details and high-level structural information. To fuse the graph information, we propose MM-HCG heterogeneous graph learning with heterogeneous mutual attention and message passing, which caters to important code blocks and discovers inter-dependencies between different forms of codes. We also propose an intent-aware summary generator with an intent-aware attention mechanism to produce customized summaries corresponding to multiple intents. Extensive experiments, including evaluations across various architectures and optimization levels, demonstrate that MiSum outperforms state-of-the-art baselines in BLEU, METEOR, and ROUGE-L metrics. Human evaluations further validate its ability to effectively support reverse engineers in understanding diverse binary code intents, providing a significant advancement in the field of binary code analysis.

## 19. No More Labelled Examples? An Unsupervised Log Parser with LLMs

**Authors:** Junjie Huang (The Chinese University of Hong Kong), Zhihan Jiang (The Chinese University of Hong Kong), Zhuangbin Chen (Sun Yat-sen University), Michael Lyu (Chinese University of Hong Kong)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729377

**中文总结:** LUNAR 是无需标注样例的 LLM 日志解析方法，通过混合排序检索仅参数不同的 Log Contrastive Units（LCU），并设计对比提示让模型抽取日志结构。在大规模公开数据集上准确率与效率均显著优于现有解析器，便于开箱部署。

**Abstract:** Log parsing serves as an essential prerequisite for various log analysis tasks. Recent advancements in this field have improved parsing accuracy by leveraging the semantics in logs through fine-tuning large language models (LLMs) or learning from in-context demonstrations. However, these methods heavily depend on labeled examples to achieve optimal performance. In practice, collecting sufficient labeled data is challenging due to the large scale and continuous evolution of logs, leading to performance degradation of existing log parsers after deployment. To address this issue, we propose LUNAR, an unsupervised LLM-based method for efficient and off-the-shelf log parsing. Our key insight is that while LLMs may struggle with direct log parsing, their performance can be significantly enhanced through comparative analysis across multiple logs that differ only in their parameter parts. We refer to such groups of logs as Log Contrastive Units (LCUs). Given the vast volume of logs, obtaining LCUs is difficult. Therefore, LUNAR introduces a hybrid ranking scheme to effectively search for LCUs by jointly considering the commonality and variability among logs. Additionally, LUNAR crafts a novel parsing prompt for LLMs to identify contrastive patterns and extract meaningful log structures from LCUs. Experiments on large-scale public datasets demonstrate that LUNAR significantly outperforms state-of-the-art log parsers in terms of accuracy and efficiency, providing an effective and scalable solution for real-world deployment.

## 20. RePurr: Automated Repair of Block-Based Learners' Programs

**Authors:** Sebastian Schweikl (University of Passau), Gordon Fraser (University of Passau)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715786

**中文总结:** RePurr 是首个基于进化搜索的 Scratch 积木程序自动修复方法，面向学习者语义错误与不完整程序。在真实学员程序上可有效改进与修复，但系统级测试、故障定位效率及塑性手术假设等仍构成根本挑战。

**Abstract:** Programming is increasingly taught using dedicated block-based programming environments such as Scratch. While the use of blocks instead of text prevents syntax errors, learners can still make semantic mistakes implying a need for feedback and help. Since teachers may be overwhelmed by help requests in a classroom, may not have the required programming education themselves, and may simply not be available in independent learning scenarios, automated hint generation is desirable. Automated program repair can provide the foundation for automated hints, but relies on multiple assumptions: (1) Program repair usually aims to produce localized patches for fixing single bugs, but learners may fundamentally misunderstand programming concepts and tasks or request help for substantially incomplete programs. (2) Automated tests are required to identify broken statements and to validate generated patches, but block-based programming environments do not come with support for automated tests. (3) The plastic surgery hypothesis assumes that the code necessary for repairs already exists in the codebase. Block-based programs tend to be small and may lack this necessary redundancy. In order to study whether automated program repair of block-based programs is nevertheless feasible, in this paper we introduce, to the best of our knowledge, the first automated program repair approach for Scratch programs based on evolutionary search. Empirical evaluation on a set of real learners’ programs demonstrates that the repair can effectively improve and fix learners’ programs, but block-based programs nevertheless pose fundamental challenges: The system-test like nature of automated tests for small block-based programs challenges fault localization, the overall efficiency of the repair, and the suitability of automatically generated tests. While the plastic surgery hypothesis can be recovered in a learning scenario using model and student solutions, the repair faces fundamentally incomplete and broken programs rather than single bugs.

## 21. SmartNote: An LLM-Powered, Personalised Release Note Generator That Just Works

**Authors:** Farbod Daneshyan (Peking University), Runzhi He (Peking University), Jianyu Wu (Peking University), Minghui Zhou (Peking University)

**Categories:** AI for Software Engineering

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729345

**中文总结:** 提出 SmartNote，用 LLM 结合代码、提交与 PR 信息聚合变更，并对提交分类与重要性打分，生成面向项目领域与受众的个性化 release notes。人工与自动评估显示其在完整性、清晰度、简洁性与组织性上优于或可比 DeepRelease 与 Conventional Changelog。

**Abstract:** The release note is a crucial document outlining changes in new software versions. It plays a key role in helping stakeholders recognise important changes and understand the implications behind them. Despite this fact, many developers view the process of writing software release notes as a tedious and dreadful task. Consequently, numerous tools (e.g., DeepRelease and Conventional Changelog) have been developed by researchers and practitioners to automate the generation of software release notes. However, these tools fail to consider project domain and target audience for personalisation, limiting their relevance and conciseness. Additionally, they suffer from limited applicability, often necessitating significant workflow adjustments and adoption efforts, hindering practical use and stressing developers. Despite recent advancements in natural language processing and the proven capabilities of large language models (LLMs) in various code and text-related tasks, there are no existing studies investigating the integration and utilisation of LLMs in automated release note generation. Therefore, we propose SmartNote, a novel and widely applicable release note generation approach that produces high-quality, contextually personalised release notes using LLM technology. SmartNote aggregates changes and uses an LLM to describe and summarise the changes using code, commit, and pull request details. It categorises and scores (for significance) commits to generate structured and concise release notes of prioritised changes. Our human and automatic evaluations reveal that SmartNote outperforms or achieves comparable performance to DeepRelease (state-of-the-art), Conventional Changelog (off-the-shelf), and the projects’ original release notes across four quality metrics: completeness, clarity, conciseness, and organisation. In both evaluations, SmartNote ranked first for completeness and organisation, while clarity ranked first in the human evaluation. A further evaluation demonstrates that SmartNote is effective in terms of context awareness and applicability.

## 22. The Struggles of LLMs in Cross-lingual Code Clone Detection

**Authors:** Micheline Bénédicte MOUMOULA (University of Luxembourg), Abdoul Kader Kaboré (University of Luxembourg), Jacques Klein (University of Luxembourg), Tegawendé F. Bissyandé (University of Luxembourg)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715764

**中文总结:** 评估五种 LLM 与八种提示在跨语言代码克隆检测上的表现，发现简单样例 F1 可达 0.99，但复杂挑战与跨语言“克隆”语义理解仍弱。用嵌入模型将多语言代码映射到同一空间后训练分类器，在 XLCoST 与 CodeNet 上分别高出 LLM 约 1 与 20 个百分点。

**Abstract:** With the involvement of multiple programming languages in modern software development, cross-lingual code clone detection has gained traction within the software engineering community. Numerous studies have explored this topic, proposing various promising approaches. Inspired by the significant advances in machine learning in recent years, particularly Large Language Models (LLMs), which have demonstrated their ability to tackle various tasks, this paper revisits cross-lingual code clone detection. We evaluate the performance of five (05) LLMs and eight prompts (08) for the identification of cross-lingual code clones. Additionally, we compare these results against two baseline methods. Finally, we evaluate a pre-trained embedding model to assess the effectiveness of the generated representations for classifying clone and non-clone pairs. The studies involving LLMs and Embedding models are evaluated using two widely used cross-lingual datasets, XLCoST and CodeNet. Our results show that LLMs can achieve high F1 scores, up to 0.99, for straightforward programming examples. However, they not only perform less well on programs associated with complex programming challenges but also do not necessarily understand the meaning of “code clone” in a cross-lingual setting. We show that embedding models used to represent code fragments from different programming languages in the same representation space enable the training of a basic classifier that outperforms all LLMs by ~1 and ~20 percentage points on the XLCoST and CodeNet datasets, respectively. This finding suggests that, despite the apparent capabilities of LLMs, embeddings provided by embedding models offer suitable representations to achieve state-of-the-art performance in cross-lingual code clone detection.

## 23. Zero-Shot Cross-Domain Code Search without Fine-Tuning

**Authors:** Keyu Liang, Zhongxin Liu (Zhejiang University), Chao Liu (Chongqing University), Zhiyuan Wan (Zhejiang University), David Lo (Singapore Management University), Xiaohu Yang (Zhejiang University)

**Categories:** AI for Software Engineering

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729357

**中文总结:** 提出 CodeBridge，零样本、无需微调的跨域代码搜索方法：用 LLM 为代码生成注释、为查询生成代码，并融合 query-code、query-comment 与 generated code-code 三种相似度。平均 MRR 相对 CoCoSoDa 与 UniXcoder 分别提升约 21.4% 与 24.9%，可比或优于需微调的 RAPID。

**Abstract:** Code search is a crucial task in software engineering, aiming to retrieve code snippets that are semantically relevant to a natural language query. Recently, Pre-trained Language Models (PLMs) have shown remarkable success and are widely adopted for code search tasks. However, PLM-based methods often struggle in cross-domain scenarios. When applied to a new domain, they typically require extensive fine-tuning with substantial data. Even worse, the data scarcity problem in new domains often forces these methods to operate in a zero-shot setting, resulting in a significant decline in performance. RAPID, which generates synthetic data for model fine-tuning, is currently the only effective method for zero-shot cross-domain code search. Despite its effectiveness, RAPID demands substantial computational resources for fine-tuning and needs to maintain specialized models for each domain, underscoring the need for a zero-shot, fine-tuning-free approach for cross-domain code search. The key to tackling zero-shot cross-domain code search lies in bridging the gaps among domains. In this work, we propose to break the query-code matching process of code search into two simpler tasks: query-comment matching and code-code matching. We first conduct an empirical study to investigate the effectiveness of these two matching schemas in zero-shot cross-domain code search. Our findings highlight the strong complementarity among the three matching schemas, i.e., query-code, query-comment, and code-code matching. Based on the findings, we propose CodeBridge, a zero-shot, fine-tuning-free approach for cross-domain code search. Specifically, CodeBridge first employs zero-shot prompting to guide Large Language Models (LLMs) to generate a comment for each code snippet in the codebase and produce a code for each query. Subsequently, it encodes queries, code snippets, comments, and the generated code using PLMs and assesses similarities through three matching schemas: query-code, query-comment, and generated code-code. Lastly, CodeBridge leverages a sampling-based fusion approach that combines these three similarity scores to rank the final search outcomes. Experimental results show that our approach outperforms the state-of-the-art PLM-based code search approaches, i.e., CoCoSoDa and UniXcoder, by an average of 21.4% and 24.9% in MRR, respectively, across three datasets. Our approach also yields results that are better than or comparable to those of the zero-shot cross-domain code search approach RAPID, which requires fine-tuning.
