# FSE 2026 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/fse-2026/fse-2026-research-papers#event-overview

Total in this category: 3 papers

## 1. Automated Repair of Requirements for Cyber-Physical Systems in Simulink Requirements Tables

**Authors:** Aren Babikian (University of Toronto), Alessio Di Sandro (University of Toronto), Federico Formica (McMaster University), Claudio Menghi (University of Bergamo; McMaster University), Marsha Chechik (University of Toronto)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808208

**中文总结:** 提出利用系统执行数据修复 CPS 中与实现错位的需求、以恢复需求—系统一致性的框架，面向 MATLAB Simulink Requirement Tables 中基于时间实值信号的声明式需求；在六个真实案例、12 条需求上两种实现均能产出正确且有用的修复需求。

**Abstract:** The development of complex software systems, such as cyber-physical systems (CPSs), involves the continuous evolution of both system implementations and their requirements. These two artifacts often proceed independently, creating a risk of misalignment between a system and its requirements. For example, a system may be updated due to implementation-level concerns, resulting in a new version that no longer satisfies its original requirements. Traditional compliance recovery techniques, such as automated program repair, address this problem by modifying the system while assuming that the requirements are correct. However, faulty or outdated requirements are a well-documented challenge in practice, motivating the complementary task of requirements repair. In this paper, we propose a framework that leverages system execution data to repair misaligned requirements of CPSs, thereby restoring requirement-to-system compliance. Our approach evaluates the correctness of declarative requirements expressed over time-based, real-valued signals using the MATLAB Simulink Requirement Tables language. We evaluate two implementations of our framework on six real-world case studies covering 12 requirements. The results confirm the effectiveness of the proposed framework in producing correct and useful repaired requirements.

## 2. Speculate: Generating REST API Specifications Using LLMs

**Authors:** Krishanu Singh (IIT Delhi), Kushagra Karar (IIT Delhi), Abhilash Jindal (IIT Delhi, India), Guowei Yang (University of Queensland)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3797118

**中文总结:** 提出 Speculate，将轻量静态分析与 LLM 结合从源码自动生成 REST API 规约，以减轻对特定语言/框架的绑定；在 19 个跨语言与框架的真实仓库上精度与召回均优于现有工具。

**Abstract:** REST APIs are widely used for accessing web services. To support their use and testing, developers often write API specifications in open formats like OpenAPI. However, writing these specifications manually is tedious and error-prone, leading to incomplete or outdated specifications that can hinder both API usage and automated testing. Existing tools attempt to generate API specifications from source code using static or dynamic analysis. Unfortunately, these tools are often tightly coupled to specific languages and frameworks, making them hard to generalize and extend. This paper presents Speculate, the first approach to combine lightweight static analysis with large language models(LLMs) to automatically generate REST API specifications from source code.By leveraging LLMs trained on diverse codebases, Speculate generalizes easily across languages and frameworks. We evaluate Speculate on 19 real-world web repositories spanning two programming languages and three REST frameworks. Our results show that Speculate outperforms existing tools on both precision and recall across all dimensions.

## 3. SpecWeaver: End-to-End HTTP API Specification Inference Across Multi-Layer Routing in Production Web Services

**Authors:** Wenbo Hu (Institute of Information Engineering at Chinese Academy of Sciences), Jie Lu (SKLP, Institute of Computing Technology, Chinese Academy of Sciences), Jingting Chen (Institute of Information Engineering, Chinese Academy of Sciences), Feng Li (Key Laboratory of Network Assessment Technology, Institute of Information Engineering, Chinese Academy of Sciences, China; School of CyberSpace Security at University of Chinese Academy of Sciences, China), Chenghang Shi (SKLP, Institute of Computing Technology, CAS), Xiaonan Shi (Institute of Information Engineering, Chinese Academy of Sciences and School of Cyber Security, University of Chinese Academy of Sciences), Jinchen Wang (Institute of Information Engineering, Chinese Academy of Sciences and School of Cyber Security, University of Chinese Academy of Sciences), Wei Huo (Institute of Information Engineering at Chinese Academy of Sciences)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3808202

**中文总结:** 提出 SpecWeaver，首个在生产多层级路由下自动抽取并统一配置路由与代码 handler 以推断端到端 HTTP API 规约的工具；在 10 个生产应用上高精度抽取重写/分发规则，贡献 5116 个未文档化 API，并使测试覆盖提升 328.6%、发现 305 个缺陷。

**Abstract:** HTTP API specifications are essential for modern web development, yet existing tools fail in production environments due to multi-layer routing. Production deployments employ infrastructure-level and framework-level routing that apply sequential rewrite and dispatch rules, creating a gap between client-visible external paths and internal paths. To address this challenge, we present SpecWeaver, the first tool to automatically extract and unify heterogeneous configuration-defined routing rules with code-level handlers. Our approach combines routing component information gathering, iterative configuration discovery using LLMs, and routing extraction from diverse configuration files to construct a routing graph representation that captures end-to-end routing relationships. Evaluated on 10 production applications, SpecWeaver extracts 36,361 rewrite rules and 48,394 dispatch rules with 99.44%/100% precision, materializes 8,288 external API paths, contributes 5,116 previously undocumented APIs with 160 unauthenticated endpoints, helps an existing testing tool improve testing coverage by 328.6% compared to the baseline, and discovers 305 bugs.
