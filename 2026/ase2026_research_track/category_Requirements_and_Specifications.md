# ASE 2026 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 6

## 1. A Scalable Rule-Based Deep Reinforcement Learning Framework for the Next Release Problem

**Authors:** Hemanth Gudaparthi (Governors State University, USA), Nan Niu (University of North Florida, USA), Prem Swaroopaanda Ramalingam (Governors State University, USA), Laxman Chowdary Kakara (Governors State University, USA)

**Categories:** Requirements and Specifications

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834348

**中文总结:** 提出可扩展的下一次发布规划框架，结合规则与双层深度强化学习（GRL+DRL）从需求描述中优先排序特性。在 Zoom、Webex、Teams 数据集上准确率最高 85.56%，复杂度为 O(m)。

**Abstract:** Next-release planning and feature selection remain critical challenges in the software deployment cycle, especially with the rapid introduction of updates and AI-driven functionalities. Selecting a subset of high-impact features that balances customer satisfaction with stakeholder business goals requires scalable models capable of producing near real-time predictions from requirements descriptions. However, uncertainty about which features truly align with customer needs makes this task difficult. This paper proposes a scalable feature prioritization framework that leverages rules derived from feature perplexity, probabilistic relevance, and customer-oriented criteria. We introduce a dual deep-reinforcement learning (DDRL) architecture that recommends high-value requirements through a hierarchical strategy. The first level applies graph reinforcement learning (GRL) guided by rule-based reasoning to structure tasks and reduce search space, while the second level uses deep reinforcement learning (DRL) to refine predictions. Experimental results on Zoom, Webex, and Teams datasets show that the approach maintains linear complexity (O(m)) compared to the cubic complexity (O(m^3)) of traditional graph-based methods, where m is the number of edges. The model achieves up to 85.56


## 2. Barista: Synthesizing Typestate Specifications with LLM Agents

**Authors:** Catarina Gamboa (Carnegie Mellon University, USA / University of Lisbon, Portugal), Paulo Canelas (Carnegie Mellon University, USA / University of Lisbon, Portugal), Ricardo Costa (University of Lisbon, Portugal), Márcio Caetano (University of Lisbon, Portugal), Jonathan Aldrich (Carnegie Mellon University, USA), Alcides Fonseca (University of Lisbon, Portugal)

**Categories:** Requirements and Specifications

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834427

**中文总结:** Barista 用 agent 工作流从 Java 类文档经 DFA 协议抽取、测试合成与验证驱动 refinement 生成 LiquidJava typestate 规约；35 类上 precision/recall 87.0%/68.3%，75% 规约可直接或微调用于编译期协议检查。

**Abstract:** Object-oriented classes encode implicit protocols that clients must follow, such as connecting a socket before sending data or opening a stream before reading.  
Mainstream programming languages like Java cannot validate the correct use of these protocols, but more advanced type systems, such as typestate systems, can detect these violations at compile time.  
However, these systems require a formalization of these implicit protocols.  
To overcome this limitation, we propose to extract object protocols from documentation using a combination of LLMs and test generation.  
We developed Barista, an agentic workflow that transforms class documentation into verifiable LiquidJava specifications through DFA-guided protocol extraction, test synthesis, and verification-driven refinement.  
We evaluated our approach on 35 Java classes with expert-written ground truth, achieving 87.0% precision and 68.3% recall, with 75% of specifications usable directly or with minor edits.  
Barista bootstraps these specifications for well-documented libraries, reducing the manual annotation burden and enabling compile-time protocol safety without specialized expertise.


## 3. Neuro-symbolic Requirements Elicitation: Utilizing Formal Verification Counterexamples as Contextual Prompts

**Authors:** Okba Tibermacine (National School of Artificial Intelligence, Sidi Abdallah, Algeria), Chouki Tibermacine (University of Southern Brittany, France)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834379

**中文总结:** 提出神经符号框架 C-GRiD：LLM 生成初版模型与候选性质，模型检测反例转自然语言向干系人追问缺失约束并迭代精炼；在 10 个基准上平均约束恢复召回 79.2%（含 25% 噪声干系人时 70.8%），优于一次性与模板基线。

**Abstract:** Incomplete and ambiguous requirements remain a common source of defects in safety-critical software systems. Formal methods provide rigorous correctness guarantees but rely on precise specifications, while Large Language Models (LLMs) enable flexible natural-language processing but lack logical consistency guarantees. Bridging the gap between informal stakeholder intent and formally verifiable specifications remains a key challenge in automated software engineering. This paper presents C-GRiD (Counterexample-Guided Requirements Discovery), a neuro-symbolic framework that integrates model checking into the requirements elicitation process. 
C-GRiD uses an LLM to synthesize an initial system model and a set of candidate requirements properties, which are then analyzed by a symbolic verifier. Counterexamples generated by the verifier are converted into structured natural-language queries that elicit missing constraints from stakeholders. This enables an iterative refinement loop that progressively reduces specification incompleteness while maintaining logical grounding of generated artifacts. We evaluate C-GRiD on 10 benchmark specifications using a controlled constraint-removal protocol to measure requirement recovery. Under a perfect oracle assumption, the framework achieves a mean constraint recovery recall of 79.2%. To assess robustness under realistic interaction settings, we introduce a simulated noisy stakeholder with a 25% error rate. In this setting, C-GRiD maintains a recall of 70.8%. Results show consistent improvements over one-shot and template-based baselines, demonstrating that counterexample-guided refinement can support the construction of more complete and logically grounded software specifications.


## 4. Refine2Diff: Detecting Protocol Specification–Implementation Inconsistencies via Specification-Driven Code Refinement

**Authors:** Yuekun Wang (Singapore Management University, Singapore), Lili Quan (Singapore Management University, Singapore), Xiaofei Xie (Singapore Management University, Singapore)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834437

**中文总结:** 提出 Refine2Diff：以规范驱动对实现做上下文感知 refinement 得到参考实现，通过原/精化实现的行为差异暴露协议规范–实现不一致，并配合 refinement 引导的 PoC；在 10 个真实协议实现上检测精度 0.84（PoC 确认后 0.98），发现 30 个未知不一致缺陷（22 个已确认）。

**Abstract:** Detecting specification–implementation inconsistencies is critical and fundamentally challenging due to the semantic gap between natural-language specifications and executable code. Existing approaches often require substantial manual effort to translate specification requirements into formal properties for verification or testing. While recent LLM-based methods have shown promise in automating this process, they suffer from hallucination and unreliable reasoning, producing false positives. To address these limitations, we present Refine2Diff, a novel framework for automatically detecting and validating specification–implementation inconsistencies in network protocols. Rather than relying solely on a direct binary judgment from an LLM, we use the specification as an instruction to refine the implementation, thereby exposing inconsistencies through observable behavioral differences between the original and refined implementations. Specifically, Refine2Diff performs context-aware refinement to construct a reference implementation and supports refinement-guided PoC generation by deriving preconditions that trigger behavioral differences and satisfying them through specification-guided mutation. We evaluate Refine2Diff on 10 real-world implementations spanning six network protocols. For inconsistency detection, Refine2Diff achieves a precision of 0.84 (1.4× higher than the strongest baseline), improving further to 0.98 after the PoC-based confirmation. For PoC generation, Refine2Diff achieves an 82% success rate, outperforming all baselines by 3×–9× while requiring up to 5.7× fewer executions. In total, Refine2Diff uncovers 30 previously unknown inconsistency bugs, 22 confirmed by developers.


## 5. SpecFSM: Extracting and Repairing Finite State Machines from Protocol Specification Documents

**Authors:** Xiangdong Li (Beijing University of Posts and Telecommunications, Beijing, China), DaWei Huang (Beijing University of Posts and Telecommunications, Beijing, China), Jingjing Guan (Beijing University of Posts and Telecommunications, Beijing, China), Hui Li (Beijing University of Posts and Telecommunications, Beijing, China)

**Categories:** Requirements and Specifications

**Artifact badges:** Artifacts Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3834331

**中文总结:** 提出 SpecFSM，从自然语言协议规格自动提取并修复有限状态机，正确状态转移数平均提升 54.7%。

**Abstract:** Finite state machines (FSMs) are a fundamental abstraction for modeling dynamic system behavior and are widely used in protocol analysis. However, automatically extracting FSMs from natural-language specifications remains challenging. Protocol documents are often lengthy and structurally complex, with state-transition descriptions scattered across the text. As a result, large language models (LLMs) operating under incomplete context are prone to generating spurious transitions and logically flawed FSMs. In this paper, we propose SpecFSM, a framework for the automatic extraction and repair of protocol FSMs from natural-language specifications. SpecFSM combines state completion, evidence tracing, and formal verification into a unified pipeline that infers missing states, constrains incorrect transitions, and repairs logical defects in the extracted models. Experiments on multiple protocol documents show that SpecFSM improves the average number of correctly extracted state transitions by 54.7% over existing methods, while producing FSMs with stronger logical validity and better interpretability.


## 6. Specification-Guided Synthesis of Deadlock-Free Communication Protocol Refinements with Large Language Models

**Authors:** Yang Li (University of Oxford, UK), Ping Hou (University of Oxford, UK), Nobuko Yoshida (University of Oxford, UK)

**Categories:** Requirements and Specifications

**Artifact badges:** Artifacts Available, Artifacts Reusable

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3832783.3837469

**中文总结:** 提出 Syntropy，在 MPST 规约约束下用 LLM 综合无死锁通信协议 refinement；有效变体率 95.6%–99.5%，在多 LLM 上生成多样非平凡 refinement。

**Abstract:** Ensuring behavioural correctness in communication protocols is a central challenge in distributed software systems, as subtle inconsistencies can lead to deadlocks. In such settings, protocol refinement – the safe substitution of a protocol that preserves correctness and compatibility with other components – is essential. Large language models (LLMs) have demonstrated strong capabilities in code generation and program synthesis, yet lack mechanisms to reliably produce outputs with correct behaviour. Formal specification approaches, such as multiparty session types (MPST), offer rigorous  
guarantees, including deadlock freedom, but provide limited support for automatically constructing protocol refinements. In this paper, we present Syntropy, a framework for synthesising protocol refinements guided by MPST specifications and LLMs. It incorporates refinement constraints directly into the generation process, ensuring the generated variants satisfy these guarantees. Our comprehensive evaluation indicates that Syntropy achieves 95.6%–99.5% validity while maintaining high syntactic correctness, and produces diverse, non-trivial refinements across multiple LLMs.

