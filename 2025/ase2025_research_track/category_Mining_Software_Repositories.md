# ASE 2025 Research Track — Mining Software Repositories

Source: https://conf.researchr.org/track/ase-2025/ase-2025-papers#event-overview

Count: 1

## 1. Diplomatist: What Do Cross-language Dependencies Reflect Software Ecosystem Health?

**Authors:** Fanyi Meng (Shenyang University of Technology), Ying Wang (Northeastern University), Chun Yong Chong (Monash University Malaysia), Hai Yu (Northeastern University, China), Zhiliang Zhu (Northeastern University, China)

**Categories:** Mining Software Repositories

**PDF:** https://ieeexplore.ieee.org/document/11334465

**中文总结:** 提出 Diplomatist，系统识别 Java 等宿主语言与 JavaScript/Python/Ruby/PHP/C/C++ 等客体语言的跨语言依赖，构建跨语言调用 API 知识库以追踪客体库版本，并分析其对软件生态健康的影响。

**Abstract:** In large-scale software development, multilingual projects, those involving multiple interacting programming languages, have become increasingly common in both industry and the open-source community. Research indicates that cross-language dependencies in these projects can increase the likelihood of risks, such as functionality defects and security vulnerabilities. While most existing studies focus on cross-language dependencies between host languages and specific guest languages (e.g., C/C++), interactions between host languages and a broader range of guest languages, as well as the broader impact of such dependencies on software ecosystems, remain underexplored.

To address the above limitations, in this paper, we develop a technique, \textsc{Diplomatist}, to identify and analyze cross-language dependencies between host languages, such as Java, and guest languages, including JavaScript, Python, Ruby, PHP, and C/C++. \textsc{Diplomatist} automatically analyzes \textit{cross-language invocation APIs} and constructs a large-scale knowledge repository to standardize code features for identifying library versions across various guest languages, enabling host languages to trace the guest language libraries they invoke. Evaluation shows that \textsc{Diplomatist} achieved an average precision of 88.9% and a recall of 91.5% on a high-quality benchmark, indicating its high accuracy in detecting cross-language dependencies. Using \textsc{Diplomatist}, we identified 435,258 Java libraries that indirectly or transitively depend on libraries from other ecosystems. \textsc{Diplomatist} provides a list of cross-language pivotal libraries that contribute to preserving the long-term health and sustainability of software ecosystems. Moreover, we conduct a case study to examine the impact of the risks introduced due to cross-language dependencies on programming language ecosystems, by analyzing a full-picture of the cross-language dependency graph. Our findings show that fragile projects or libraries can propagate security issues across ecosystems via these dependencies, impacting 13,739 downstream projects in the \textit{Maven} ecosystem. We utilized \textsc{Diplomatist} to provide remediation suggestions to relevant project developers. Issue reports of some subjects have been confirmed by developers.

