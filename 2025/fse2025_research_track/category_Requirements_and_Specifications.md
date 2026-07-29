# FSE 2025 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 3 papers

## 1. Incorporating Verification Standards for Security Requirements Generation from Functional Specifications

**Authors:** Xiaoli Lian (Beihang University, China), Shuaisong Wang (Beihang University), Hanyu Zou (Beihang University), Fang Liu (Beihang University), Jiajun Wu (Beihang University), Li Zhang (Beihang University)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729347

**中文总结:** 提出 F2SRD，在 OWASP ASVS 验证需求引导下，先检索适用 VR 再构造结构化提示驱动 GPT-4，从功能规格自动派生安全需求。相对两种基线，生成的 SR 在启发性、多样性与具体性上更优。

**Abstract:** In the current software-driven era, ensuring privacy and security is critical. Despite this, the specification of security requirements for software is still largely a manual and labor-intensive process. Engineers are tasked with analyzing potential security threats based on functional requirements (FRs), a procedure prone to omissions and errors due to the expertise gap between cybersecurity experts and software engineers. To bridge this gap, we introduce F2SRD ( Function-to-S ecurity Requirement Derivation), an automated approach that proactively derives security requirements (SRs) from functional specifications under the guidance of relevant security verification requirements (VRs) drawn from the well recognized OWASP Application Security Verification Standard (ASVS). F2SRD operates in two main phases: Initially, we develop a VR retriever trained on a custom database of FR-VR pairs, enabling it to adeptly select applicable VRs from ASVS. This targeted retrieval informs the precise and actionable formulation of SRs. Subsequently, these VRs are used to construct structured prompts that direct GPT-4 in generating SRs. Our comparative analysis against two established models demonstrates F2SRD’s enhanced performance in producing SRs that excel in inspiration, diversity, and specificity—essential attributes for effective security requirement generation. By leveraging security verification standards, we believe that the generated SRs are not only more focused but also resonate stronger with the needs of engineers.

## 2. Scene Flow Specifications: Encoding and Monitoring Rich Temporal Safety Properties of Autonomous Systems

**Authors:** Trey Woodlief (University of Virginia, United States), Felipe Toledo, Matthew B Dwyer (University of Virginia), Sebastian Elbaum (University of Virginia)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729382

**中文总结:** 本文刻画自动驾驶安全属性所需表达力，命名并支持含跨时刻符号实体的 scene flow properties，扩展领域特定语言以编码丰富时序约束。在 114 条规范中覆盖率由约 76% 提升至 96%；运行时监控在 30 次测试中发现 3 个 SOTA AV 违反 scene flow 属性逾 40 次。

**Abstract:** To ensure the safety of autonomous systems, it is imperative for them to abide by their safety properties. The specification of such safety properties is challenging because of the gap between the input sensor space (e.g., pixels, point clouds) and the semantic space over which safety properties are specified (e.g. people, vehicles, road). Recent work utilized scene graphs to overcome portions of that gap, enabling the specification and synthesis of monitors targeting many safe driving properties for autonomous vehicles. However, scene graphs are not rich enough to express the many driving properties that include temporal elements (i.e., when two vehicles enter an intersection at the same time, the vehicle on the left shall yield…), fundamentally limiting the types of specifications that can be monitored. In this work, we characterize the expressiveness required to specify a large body of driving properties, identify property types that cannot be specified with current approaches, which we name scene flow properties , and construct an enhanced domain-specific language that utilizes symbolic entities across time to enable the encoding of the rich temporal properties required for autonomous system safety. In analyzing a set of 114 specifications, we find that our approach can successfully encode 110 (96%) specifications as compared to 87 (76%) under prior approaches, an improvement of 20 percentage points. We implement the specifications in the form of a runtime monitoring framework to check the compliance of 3 state-of-the-art autonomous vehicles finding that they violated scene flow properties over 40 times in 30 test executions, including 34 violations for failing to yield properly at intersections.

## 3. Unlocking Optimal ORM Database Designs: Accelerated Tradeoff Analysis with Transformers

**Authors:** Md Rashedul Hasan (University of Nebraska-Lincoln), Mohammad Rashedul Hasan (University of Nebraska-Lincoln), Hamid Bagheri (University of Nebraska-Lincoln)

**Categories:** Requirements and Specifications

**Artifact badges:** Artifact-Available

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729344

**中文总结:** 提出 DesignTradeoffSculptor，将 ORM 数据库设计权衡探索建模为 NLP 任务，用 Transformer 剔除次优设计以加速 Pareto 分析。可发现主流 ORM 工具遗漏的最优设计，分析效率提升超 98%（约 15 天降至 18 分钟）。

**Abstract:** Optimizing object-relational database mapping (ORM) design is crucial for performance and scalability in modern software systems. However, widely used ORM tools offer limited support for exploring performance tradeoffs, often enforcing a single design and overlooking alternatives, which can lead to suboptimal outcomes. While systematic tradeoff analysis can reveal Pareto-optimal designs, its high computational cost and poor scalability hinder practical adoption. This paper presents DesignTradeoffSculptor, an extensible tool suite for efficient, scalable tradeoff analysis in ORM database design. Leveraging advanced Transformer-based deep learning models—trained and fine-tuned on formally analyzed database designs—and framing design exploration as a Natural Language Processing task, DesignTradeoffSculptor efficiently identifies and removes suboptimal designs, sharply reducing the number of candidates requiring costly tradeoff analysis. Experiments show that DesignTradeoffSculptor uncovers optimal designs missed by leading ORM tools and improves analysis efficiency by over 98.21%, reducing tradeoff analysis time from 15 days to just 18 minutes, demonstrating the transformative potential of integrating formal methods with deep learning.
