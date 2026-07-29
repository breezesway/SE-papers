# FSE 2025 Research Track — Systems, Mobile, and UI

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 2 papers

## 1. Detecting and Handling WoT Violations by Learning Physical Interactions from Device Logs

**Authors:** Bingkun Sun (Fudan University), Shiqi Sun (Northwestern Polytechnique University), Jialin Ren (Fudan University), Mingming Hu (Fudan University), Kun Hu (School of Computer Science, Fudan University), Liwei Shen (Fudan University), Xin Peng (Fudan University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3715743

**中文总结:** 提出 SysGuard，用动态概率图模型学习设备日志中的物理交互图，并结合 LLM 因果分析过滤无关依赖，以检测与处理 WoT 违规；在两个真实系统上显著优于现有方法，消融显示 LLM 因果分析明显提升准确率。

**Abstract:** The Web of Things (WoT) system standardizes the integration of ubiquitous IoT devices in physical environments, enabling various software applications to automatically sense and regulate the physical environment. While providing convenience, the complex interactions among software applications and physical environment make the WoT system vulnerable to violations caused by improper actuator operations, which may cause undesirable or even harmful results, posing serious risks to user safety and security. In response to this critical concern, many previous efforts have be made. However, existing works primarily focus on analyzing software application behaviors, with insufficient consideration of the physical interactions, multi-source violations, and environmental dynamics in such ubiquitous software systems. As a result, they fail to comprehensively detect the impact of actuator operations on the dynamic environment, thus limiting their effectiveness. To address these limitations, we propose SysGuard, a violation detecting and handling approach. SysGuard employs the dynamic probabilistic graphical model (DPGM) to model the physical interactions as the physical interaction graph (PIG). In the offline phase, SysGuard takes device description models and history device logs as input to capture physical interactions by learning the PIG. In this process, a large language model (LLM) based causal analysis method is further introduced to filter out the device dependencies unrelated to physical interaction by analyzing the device interaction scenarios recorded in device logs. In the online phase, SysGuard processes user-customized violation rules, and monitors runtime device logs to predict violation states and generates handling policies by inferring the PIG. Evaluation on two real-world WoT systems shows that SysGuard significantly outperforms existing state-of-the-art works, achieving high performance in both violation detecting and handling. It also confirms the runtime efficiency and scalability of SysGuard. Ablation experiment on our constructed dataset demonstrates that the LLM-based causal analysis significantly improve the performance of SysGuard, with the accuracy increasing in both violation detecting and handling.

## 2. TracePicker: Optimization-based Trace Sampling for Microservice-based Systems

**Authors:** Shuaiyu Xie (School of Computer Science, Wuhan University, China), Jian Wang (Wuhan University), Maodong Li (School of Computer Science, Wuhan University, China), Peiran Chen (School of Computer Science, Wuhan University, China), Jifeng Xuan (Wuhan University), Bing Li (Wuhan University)

**Categories:** Systems, Mobile, and UI

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729351

**中文总结:** 提出 TracePicker，对异常调用链优先保留，并将正常链采样拆为配额分配与分组采样两个优化问题，用动态规划与进化算法降低信息损失。相对已有尾部采样方法在采样质量与耗时上均更优。

**Abstract:** Distributed tracing is a pivotal technique for software operators to understand and diagnose issues within microservice-based systems, offering a comprehensive view of user requests propagated through various services. However, the unprecedented volume of traces imposes expensive storage and analytical burdens for online systems. Conventional tracing implementations typically use random sampling with a fixed probability for each trace, posing a risk of losing valuable traces. To circumvent this loss, several tail-based sampling methods have been proposed to sample traces based on their content. Nevertheless, these methods primarily evaluate traces on an individual basis, neglecting the collective attributes of the sample set, including its comprehensiveness, balance, and consistency. To address these issues, we propose TracePicker, an optimization-based online sampler designed to enhance the quality of sampled data while mitigating storage burden. TracePicker employs a streaming anomaly detector to capture and retain anomalous traces that are crucial for troubleshooting. For normal traces, the sampling process is segmented into quota allocation and group sampling, formulating both as optimization problems. By solving these problems using dynamic programming and evolution algorithms, TracePicker selects a high-quality subset of data, minimizing overall information loss. Experimental results demonstrate that TracePicker outperforms existing tail-based sampling methods in terms of both sampling quality and time consumption.
