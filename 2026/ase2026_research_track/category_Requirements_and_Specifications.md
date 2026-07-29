# ASE 2026 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 6

## 1. A Scalable Rule-Based Deep Reinforcement Learning Framework for the Next Release Problem

**Authors:** Hemanth Gudaparthi (Governors State University United States), Nan Niu (University of North Florida United States), Prem Swaroopaanda (Ramalingam Governors State University United States), Laxman Chowdary (Kakara Governors State University United States)

**Categories:** Requirements and Specifications

**中文总结:** 提出可扩展的下一次发布规划框架，结合规则与双层深度强化学习（GRL+DRL）从需求描述中优先排序特性。在 Zoom、Webex、Teams 数据集上准确率最高 85.56%，复杂度为 O(m)。

**Abstract:** Next-release planning and feature selection remain critical challenges in the software deployment cycle, especially with the rapid introduction of updates and AI-driven functionalities. Selecting a subset of high-impact features that balances customer satisfaction with stakeholder business goals requires scalable models capable of producing near real-time predictions from requirements descriptions. However, uncertainty about which features truly align with customer needs makes this task difficult. This paper proposes a scalable feature prioritization framework that leverages rules derived from feature perplexity, probabilistic relevance, and customer-oriented criteria. We introduce a dual deep-reinforcement learning (DDRL) architecture that recommends high-value requirements through a hierarchical strategy. The first level applies graph reinforcement learning (GRL) guided by rule-based reasoning to structure tasks and reduce search space, while the second level uses deep reinforcement learning (DRL) to refine predictions. Experimental results on Zoom, Webex, and Teams datasets show that the approach maintains linear complexity ($O(m)$) compared to the cubic complexity ($O(m^3)$) of traditional graph-based methods, where $m$ is the number of edges. The model achieves up to 85.56% accuracy and superior decision quality (false negatives at just 11.28%), outperforming GraphRL, REST, and NSGA-II in stakeholder-driven next-release planning.


## 2. Barista: Synthesizing Typestate Specifications with LLM Agents

**Authors:** Catarina Gamboa (Carnegie Mellon University and University of Lisbon Portugal), Paulo Canelas (Carnegie Mellon University / SonarSource United States), Ricardo Costa (University of Lisbon Portugal), Marcio Caetano (University of Lisbon Portugal), Jonathan Aldrich (Carnegie Mellon University United States), Alcides Fonseca (LASIGE; University of Lisbon Portugal)

**Categories:** Requirements and Specifications

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 3. Neuro-symbolic Requirements Elicitation: Utilizing Formal Verification Counterexamples as Contextual Prompts

**Authors:** Okba Tibermacine (National School of Artificial Intelligence Algeria), Chouki Tibermacine (IRISA, CNRS and University of Southern Brittany France)

**Categories:** Requirements and Specifications

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 4. Refine2Diff: Detecting Protocol Specification–Implementation Inconsistencies via Specification-Driven Code Refinement

**Authors:** Yuekun Wang (Singapore Management University), Lili Quan (Singapore Management University (SMU) Singapore), Xiaofei Xie (Singapore Management University Singapore)

**Categories:** Requirements and Specifications

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 5. SpecFSM: Extracting and Repairing Finite State Machines from Protocol Specification Documents

**Authors:** Xiangdong Li (Beijing University of Posts and Telecommunications China), DaWei Huang (Beijing University of Posts and Telecommunications China), Jingjing Guan (Beijing University of Posts and Telecommunications China), Hui Li (Beijing University of Posts and Telecommunications China)

**Categories:** Requirements and Specifications

**中文总结:** 提出 SpecFSM，从自然语言协议规格自动提取并修复有限状态机，正确状态转移数平均提升 54.7%。

**Abstract:** Finite state machines (FSMs) are a fundamental abstraction for modeling dynamic system behavior and are widely used in protocol analysis. However, automatically extracting FSMs from natural-language specifications remains challenging. Protocol documents are often lengthy and structurally complex, with state-transition descriptions scattered across the text. As a result, large language models (LLMs) operating under incomplete context are prone to generating spurious transitions and logically flawed FSMs. In this paper, we propose SpecFSM, a framework for the automatic extraction and repair of protocol FSMs from natural-language specifications. SpecFSM combines state completion, evidence tracing, and formal verification into a unified pipeline that infers missing states, constrains incorrect transitions, and repairs logical defects in the extracted models. Experiments on multiple protocol documents show that SpecFSM improves the average number of correctly extracted state transitions by 54.7% over existing methods, while producing FSMs with stronger logical validity and better interpretability.


## 6. Specification-Guided Synthesis of Deadlock-Free Communication Protocol Refinements with Large Language Models

**Authors:** Li Yang (Institute of Software, Chinese Academy of Sciences China), Ping Hou (University of Oxford United Kingdom), Nobuko Yoshida (University of Oxford United Kingdom)

**Categories:** Requirements and Specifications

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)
