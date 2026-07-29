# ASE 2026 Research Track — Debugging and Fault Diagnosis

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 11

## 1. ARMOR: A Robust Self-Supervised Framework for Root Cause Analysis in Microservices under Missing Modality

**Authors:** Wenzhuo Qian (Zhejiang University China), Hailiang Zhao (Zhejiang University China), Ziqi Wang (Zhejiang University China), Zhipeng Gao (Shanghai Institute for Advanced Study - Zhejiang University China), Jiayi Chen (Zhejiang University China), Zhiwei Ling (Zhejiang University China), Shuiguang Deng (Zhejiang University; Alibaba-Zhejiang University Joint Institute of Frontier Technologies China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 2. Bifrost: Empowering Pretrained Language Model with Fallibility Representation for Log-Based Fault Diagnosis

**Authors:** Minghua He (Peking University China), Tong Jia (Institute for Artificial Intelligence, Peking University, Beijing, China China), Lingzhe Zhang (Peking University, China China), Chiming Duan (Peking University China), Xinlong Zhao (Peking University), Leyi Pan (Tsinghua University China), Cheng Wang (Alibaba Group), Kangjin Wang (Alibaba Group China), Yinghao Yu (Alibaba Group China), Liping Zhang (Alibaba Group China), Yifan Wu (Peking University China), Ying Li (School of Software and Microelectronics, Peking University, Beijing, China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 提出 Bifrost 日志表示学习方法，通过自监督对比学习捕获多层次“可故障性”特征。在公开与工业 MLaaS 系统上，异常检测 F1、根因定位 HR@k、故障识别 Macro-F1 均显著优于现有 PLM。

**Abstract:** Log-based fault diagnosis is crucial for runtime debugging and maintenance. Existing fault diagnosis methods use language models pre-trained on natural language (PLMs) for log representation. However, system faults are reflected in the multi-level structure of system logs. PLMs pre-trained on natural language struggle to comprehensively capture multi-level fault information, failing to meet the requirements of fault diagnosis. We refer to this information as fallibility representations. To address this problem, we propose a novel log representation learning method, Bifrost. It draws inspiration from the log analysis experience of Site Reliability Engineers and meticulously designs strategies based on self-supervised contrastive learning to learn the fallibility representations of logs. Across three public systems and one industrial ML-as-a-Service system, the log representations produced by Bifrost outperform existing PLMs by average margins of 9.83% in F1 for anomaly detection, 18.28% in HR@k for root cause localization, and 20.88% in Macro-F1 for fault identification.


## 3. EffiHolmes: Differential Profiling-Guided Repository Level Time Inefficiency Fix Localization

**Authors:** Haowen Yang (Hong Kong University of Science and Technology China), Yun Peng (The Chinese University of Hong Kong Hong Kong SAR China), Zishuo Ding (The Hong Kong University of Science and Technology (Guangzhou) China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 4. Enhancing Trace-Based Root Cause Analysis for Microservice Systems via Code Change Understanding

**Authors:** Min Zhang (Fudan University China), Chenxi Zhang (Xidian University China), Senyu Xie (Fudan University China), Shihong Chen (McDonald's China), Lei Wu (McDonald's China China), Xin Peng (Fudan University China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 5. GALA: Graph-Augmented LLM Agents for Root Cause Analysis and Incident Response in Microservices

**Authors:** Yifang Tian (University of Toronto Canada), Yaming Liu (University of Toronto Canada), Zichun Chong (University of Toronto Canada), Zihang Huang (University of Toronto Canada), Yiran Li (University of Toronto Canada), Hans-Arno Jacobsen (University of Toronto Canada)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 6. How Quantum Bugs Live and Die: A Lifecycle-Based Empirical Study of Bugs in Quantum Software

**Authors:** Yasai Shi, Xiangxin Meng (Bytedance China), Xiangjie Huang (Beihang University China), Jian Zhang (Beihang University China), Tianyu Wo, Xu Wang (Beihang University China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** 构建含 2429 个缺陷的 QBugsSet 生命周期基准，对比量子软件与经典缺陷的分布、修复延迟与传播特征。发现量子特有缺陷更难修复且前沿 LLM 端到端完整修复率仅 3.82%。

**Abstract:** Despite growing evidence that bugs in quantum software exhibit distinctive characteristics, existing studies are typically scoped to individual frameworks or single quality attributes and do not examine how quantum-specific bugs behave across the broader software lifecycle. To address this gap, we construct QBugsSet, a lifecycle-based benchmark containing 2,429 bugs and 1,793 realistic negative samples, mined from real GitHub bug-fixing commits in the Qiskit, Cirq, and PennyLane ecosystems, and use it to conduct a comprehensive empirical study comparing quantum-specific and classical bugs across lifecycle distribution, bug-fix latency and pre-fix spatial propagation, repair burden, and LLM-based debugging effectiveness. We find that quantum-specific bugs are more concentrated in semantically critical stages, tend to persist longer before repair (median 17 vs. 7 days), and more often require coordinated multi-hunk repairs (37.8% vs. 27.3%). These lifecycle characteristics highlight a practical limitation of current automation: even the best frontier LLM achieves an end-to-end full repair rate of only 3.82% on quantum-specific bugs, compared with 8.51% on classical bugs. Overall, these findings provide evidence-based guidance for future debugging support that integrates stronger quantum-aware semantic reasoning with broader repository context.


## 7. HyTri: Hybrid Triage of CI Failures via LLM Guided Semantic Reasoning and Change Attribution

**Authors:** Lior Broide (Ben-Gurion University of the Negev Israel), Argaman Mordoch (Ben-Gurion University of the Negev Israel), Roni Stern (Ben-Gurion University of the Negev Israel)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 8. Needle in the Repo: Diagnosing Maintainability Failures in AI-Generated Repository Edits

**Authors:** Haichao Zhu (Reality Vison United States), Qian Zhang (University of California at Riverside United States), Jiyuan Wang (Tulane University United States), Zhaorui Yang (University of California, Riverside United States), Yuxin Qiu (University of California at Riverside United States)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 9. ReLog: Execution-Aware Logging with Runtime Feedback for LLM-Oriented Debugging

**Authors:** Xin Wang (The Hong Kong University of Science and Technology (Guangzhou) China), Yang Feng (Hong Kong University of Science and Technology China), Xiaoqian Jiao (Hong Kong University of Science and Technology China), Yang Zhang (Hebei University of Science and Technology China), Zhenhao Li (York University Canada), Zishuo Ding (The Hong Kong University of Science and Technology (Guangzhou) China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 10. TELLER: Non-intrusive Cross-Layer Root-Cause Analysis for LLM Inference

**Authors:** Ruilin Xu (Sun Yat-sen University China), Junyi Li (Sun Yat-sen University China), Pengfei Chen (Sun Yat-sen University), Zongxuan Xie (Sun Yat-sen University China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 11. When Does AI Actually Help in Incident Response? Identifying Good First Messages in Cloud Service Incidents

**Authors:** Minghua Ma (Microsoft United States), Rujia Wang (Microsoft), Chetan Bansal (Microsoft Research United States), Saravan Rajmohan (Microsoft), Yingnong Dang (Microsoft Azure United States), Hongyu Zhang (Chongqing University China)

**Categories:** Debugging and Fault Diagnosis

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)
