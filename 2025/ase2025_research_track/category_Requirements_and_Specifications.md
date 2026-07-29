# ASE 2025 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 2

## 1. RFCScope: Detecting Logical Ambiguities in Internet Protocol Specifications

**Authors:** Mrigank Pawagi (Indian Institute of Science, Bengaluru), Lize Shao (Rice University, USA), Hyeonmin Lee (University of Virginia), Yixin Sun (University of Virginia), Wenxi Wang (University of Virgina)

**Categories:** Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11334266

**中文总结:** 系统归纳 RFC 规范中七类逻辑歧义（不一致、欠指定等），提出 RFCScope 模块化 LLM 流水线进行跨文档上下文检测与推理校验；在 14 份近期 RFC 中发现 31 处新逻辑歧义。

**Abstract:** Internet protocol specifications, published as Requests for Comments (RFCs) by the IETF organization, are essential to ensuring the interoperability, security, and reliability of the Internet. However, ambiguities in these specifications, particularly logical ambiguities such as inconsistencies and under-specifications, can lead to critical misinterpretations and implementation errors. Unfortunately, such ambiguities remain largely overlooked and challenging to detect with existing tools.

In this paper, we present the first systematic study of verified technical errata from Standards Track RFCs over the past 11 years, identifying seven distinct subtypes of logical ambiguities. Building on these insights, we introduce RFCScope, the first scalable framework for detecting logical ambiguities in RFCs. RFCScope employs large language models (LLMs) through a modular pipeline that constructs targeted cross-document context, partitions specifications to preserve semantic integrity, applies bug-type-aware prompts for detection, and filters out false positives using structured reasoning validation.

RFCScope uncovers 31 new logical ambiguities spanning all seven subtypes across 14 recent RFCs. Eight of these have been confirmed by RFC authors, with three officially verified as technical errata. Our results demonstrate that RFCScope offers a practical solution for improving the clarity, consistency, and reliability of protocol standards through ambiguity detection.

Artifact on GitHub .


## 2. SPEC2CODE: Mapping Software Specification to Function-Level Code Implementation

**Authors:** Yuekun Wang (Singapore Management University), Lili Quan (Tianjin University), Xiaofei Xie (Singapore Management University), Junjie Wang (Tianjin University), Jianjun Chen (Tsinghua University)

**Categories:** Requirements and Specifications

**PDF:** https://ieeexplore.ieee.org/document/11334548

**中文总结:** 提出 Spec2Code，以 LLM 驱动两阶段相关过滤与聚类，再对规范需求（SR）与函数做约束级细粒度匹配，实现规范文档到函数级实现的自动映射。

**Abstract:** Software specifications, such as protocol standards defined in RFCs, play a critical role in ensuring the correctness of software systems. To check consistency, specification–implementation pairs are essential for testing and verification. However, existing efforts in specification-to-code mapping remain largely manual and are typically limited to the file level, lacking the fine-grained granularity needed for function-level analysis, which is crucial for effective consistency checking. To address this gap, we present Spec2Code, the first LLM-driven framework that automates fine-grained mapping from specifications to function implementations.

Given a specification document and a software codebase, Spec2Code first performs preprocessing to extract structured SRs and function-level code representations, along with contextual and dependency information. To ensure scalability, Spec2Code employs a two-stage process comprising relevance filtering and clustering-based SR organization to reduce the candidate pairs. For accuracy, Spec2Code performs fine-grained constraint-level matching on each candidate SR–function pair using LLMs, leveraging enriched context to determine whether a function fully, partially, or does not relate to an SR.

We evaluate Spec2Code on real-world implementations of HTTP and TLS protocols, including  \textit{Apache Httpd}, \textit{Nginx}, \textit{OpenSSL}, and \textit{BoringSSL}. Experimental results show that Spec2Code outperforms three state-of-the-art baselines, achieving up to 49%, 66%, and 66% improvement in precision, recall, and F1, respectively. Additionally, Spec2Code successfully recovers the mappings for 12 known inconsistency bugs and discovers 11 previously unreported inconsistencies using an integrated lightweight consistency verifier, 5 of which have been confirmed by project developers.

