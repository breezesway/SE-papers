# ISSTA 2025 Research Track — Debugging and Fault Diagnosis

Source: https://conf.researchr.org/track/issta-2025/issta-2025-papers#event-overview

Count: 3

## 1. A Low-Cost Feature Interaction Fault Localization Approach for Software Product Lines

**Authors:** Haining Wang (South China University of Technology), Yi Xiang (South China University of Technology), Han Huang (South China University of Technology), Jie Cao, Kaichen Chen (South China University of Technology), Xiaowei Yang (South China University of Technology)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728917

**中文总结:** 针对软件产品线（SPL）特征交互缺陷定位搜索空间指数膨胀的问题，提出基于反事实推理的 CRFL，结合对称不确定性过滤无关交互并避免重复生成同一交互。在 8 个公开 SPL 上将搜索空间减少 51%–88%，平均运行时间约为 SOTA 的 1/15.6，并可与语句级定位结合精确定位缺陷语句。

**Abstract:** In Software Product Lines (SPLs), localizing buggy feature interactions helps developers identify the root cause of test failures, thereby reducing their workload. This task is challenging because the number of potential interactions grows exponentially with the number of features, resulting in a vast search space, especially for large SPLs. Previous approaches have partially addressed this issue by constructing and examining potential feature interactions based on suspicious feature selections (e.g., those present in failed configurations but not in passed ones). However, these approaches often overlook the causal relationship between buggy feature interaction and test failures, resulting in an excessive search space and high-cost fault localization. To address this, we propose a low-cost Counterfactual Reasoning-Based Fault Localization (CRFL) approach for SPLs, which enhances fault localization efficiency by reducing both the search space and redundant computations. Specifically, CRFL employs counterfactual reasoning to infer suspicious feature selections and utilizes symmetric uncertainty to filter out irrelevant feature interactions. Additionally, CRFL incorporates two findings to prevent the repeated generation and examination of the same feature interactions. We evaluate the performance of our approach using eight publicly available SPL systems. To enable comparisons on larger real-world SPLs, we generate multiple buggy mutants for both BerkeleyDB and TankWar. Experimental results show that our approach reduces the search space by 51%-73% for small SPLs (with 6-9 features) and by 71%-88% for larger SPLs (with 13-99 features). The average runtime of our approach is approximately 15.6 times faster than that of a state-of-the-art method. Furthermore, when combined with statement-level localization techniques, CRFL can efficiently localize buggy statements, demonstrating its ability to accurately identify buggy feature interactions.

## 2. An Investigation on Numerical Bugs in GPU Programs Towards Automated Bug Detection

**Authors:** Ravishka Rathnasuriya (The University of Texas - Dallas), Nidhi Majoju (University of Texas at Dallas), Zihe Song (University of Texas at Dallas), Wei Yang (UT Dallas)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728950

**中文总结:** 基于 GitHub 上 397 个真实样本系统刻画 GPU 数值 bug（GPU-NB）的根因、症状、触发输入与修复策略，并给出初步检测工具 GPU-NBDetect。该工具覆盖六类 bug，在四个数学库的 186 个函数中发现 226 个疑似 bug，其中 60 个获开发者确认。

**Abstract:** General-purpose graphics processing unit (GPU) computing has emerged as a leading parallel computing paradigm, offering significant performance gains in various domains such as scientific computing and deep learning. However, GPU programs are susceptible to numerical bugs, which can lead to incorrect results or crashes. These bugs are difficult to detect, debug, and fix due to their dependence on specific input values or types and the absence of reliable error-checking mechanisms and oracles. Additionally, the unique programming conventions of GPUs complicate identifying the root causes of bugs, while fixing them requires domain-specific knowledge of GPU computing and numerical libraries. Therefore, understanding the characteristics of GPU numerical bugs is crucial for developing effective solutions.

In this paper, we conduct a comprehensive study of GPU programming numerical bugs (GPU-NBs) by analyzing 397 real-world bug samples from GitHub. We identify common root causes, symptoms, input patterns, test oracles that trigger these bugs and the strategies used to fix them. We also present GPU-NBDetect, a preliminary tool designed to detect numerical bugs across six distinct bug categories. GPU-NBDetect detected a total of 226 bugs across 186 mathematical functions in four libraries, with 60 confirmed by developers. Our findings lay the groundwork for developing detection and prevention techniques for GPU numerical bugs and offer insights for building more effective debugging and auto-repair tool.

## 3. DepState: Detecting Synchronization Failure Bugs in Distributed Database Management Systems

**Authors:** Cundi Fang (National University of Defense Technology), Jie Liang, Zhiyong Wu (Tsinghua University, China), Jingzhou Fu (School of Software, Tsinghua University), Zhouyang Jia (National University of Defense Technology), Chun Huang (National University of Defense Technology), Yu Jiang (Tsinghua University), Shanshan Li (National University of Defense Technology)

**Categories:** Debugging and Fault Diagnosis

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728965

**中文总结:** DepState 模拟分片与集群状态变化，在跨节点表间建立依赖以测试 DDBMS 同步流程。应用于 MySQL NDB/InnoDB Cluster 与 MariaDB Galera 发现 22 个新漏洞（11 已确认），24 小时内比 Jepsen、SQLsmith 等工具多发现 11 个同步失败 bug 并覆盖更多同步相关代码。

**Abstract:** DDBMSs are crucial for managing large-scale distributed data. Unlike single-node databases, they are deployed across clusters, distributing data among multiple nodes. The synchronization process is typically used in DDBMSs to maintain data consistency against data and cluster updates. Due to its complexity, bugs in the synchronization process are inevitable and can lead to failures. These failures may result in data inconsistencies, transaction errors, or even cluster crashes, all of which severely compromise the availability and reliability of DDBMSs. However, there has been relatively little focus on testing the DDBMS synchronization process.

In this paper, we propose DepState, a framework to detect synchronization failure bugs. DepState enhances the testing of synchronization processes by simulating the complexities of data sharding and the dynamic conditions of cluster environments. It establishes dependencies between tables across multiple nodes, closely reflecting real-world scenarios. Furthermore, the framework systematically introduces controlled variations in cluster states. We utilize DepState on three DDBMSs, namely MySQL NDB Cluster, MySQL InnoDB Cluster, and MariaDB Galera Cluster. DepState finds 22 new vulnerabilities, of which 11 have already been confirmed. We also compare DepState against state-of-the-art tools. DepState finds 11 more synchronization failure bugs and covers 37.5%-66.5%, 42.4%-83.3%, 36.8%-54.8%, and 27.8%-54.2% more lines in synchronization-related functions than Jepsen, SQLsmith, SQLancer, and Mozi in 24 hours.
