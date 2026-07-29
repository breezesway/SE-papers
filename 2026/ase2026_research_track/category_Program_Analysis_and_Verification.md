# ASE 2026 Research Track — Program Analysis and Verification

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 21

## 1. Adaptive Proof Refinement with LLM-Guided Strategy Selection

**Authors:** Minghai Lu (Purdue University United States), Zhe Zhou (Purdue University United States), Danning Xie (Meta United States), Songlin Jia (Purdue University United States), Benjamin Delaware (Purdue University United States), Tianyi Zhang (Purdue University United States)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 2. All or Nothing: How Library Type Annotations Affect Client-Side Errors in Python

**Authors:** Eric Asare (New York University Abu Dhabi United Arab Emirates), Luca (Di Grazia University of St. Gallen Switzerland), Sarah Nadi (New York University Abu Dhabi United Arab Emirates)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 3. Automated Lemma Discovery in Agentic Program Verification

**Authors:** Huan Zhao (National University of Singapore Singapore), Haoxin Tu (National University of Singapore Singapore), Zhengyao Liu (National University of Singapore Singapore), Martin C. (Rinard Massachusetts Institute of Technology United States), Abhik Roychoudhury (National University of Singapore Singapore)

**Categories:** Program Analysis and Verification

**中文总结:** 提出 LLM Agent LemmaNet，结合源码语义离线与证明过程在线发现/适配辅助引理，加速 deductive verification。在 SV-COMP 及 Linux kernel 等真实项目上显著优于现有 proof agent。

**Abstract:** Deductive verification provides strong correctness guarantees for code by extracting verification conditions (VCs) and writing formal proofs for them. The expertise-intensive task of VC proving is the main bottleneck in this process, and has been partly automated owing to recent advances in Large Language Model (LLM) agents. However, existing proof agents are not able to discover helper lemmas – auxiliary lemmas that aid in proving – and thus fall short as programs grow in size and complexity. In this paper, we argue that VC proving for program verification is more than a purely mathematical task, and benefits considerably from program comprehension. Our key insight is that human proof engineers often discover and apply helper lemmas based on their understanding of the program semantics, which are \emph{not} directly reflected in the VCs produced by VC generators. Inspired by this insight, we propose an LLM agent, \textsc{LemmaNet}, that discovers helper lemmas in two ways. Specifically, the agent first synthesizes lemmas \emph{offline} by directly analyzing the source code and specifications and then relating this semantic understanding to the mechanical, verbose encoding produced by VC generators. As the proof unfolds, \textsc{LemmaNet} then adapts existing helper lemmas \emph{online} to accommodate evolving proof states, enabling the agent to effectively discharge complex VCs on-the-fly. We implement \textsc{LemmaNet} on top of an existing proof agent \textsc{AutoRocq} for \textsc{Rocq} and the \textsc{Frama-C} ecosystem, and evaluate it on SV-COMP and established real-world subjects, including modules of the Linux kernel, Contiki OS, standard C++ library, and X.509 parser. Our experimental results demonstrate that \textsc{LemmaNet} significantly outperforms state-of-the-art approaches, highlighting the importance of program comprehension-aided lemma discovery in agentic program verification.


## 4. Best-Effort GR(1) Synthesis: Exploiting Environmental Cooperation under Unrealizability

**Authors:** Sirui Liu (National University of Defense Technology China), Yating Zhang (National University of Defense Technology China), Chi Hu (China Academy of Engineering Physics China), Wei Dong (National University of Defense Technology China)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 5. Beyond Text Matching: Towards Reference-Free Evaluation for Human-Oriented Binary Reverse Engineering

**Authors:** Xiuwei Shang (University of Science and Technology of China China), Li Hu, Jiang Xiao (Huazhong University of Science and Technology), Jieke Shi (Singapore Management University Singapore), Junda He (Singapore Management University Singapore), Zhou Yang (University of Alberta; CIFAR AI Chair; Alberta Machine Intelligence Institute Canada), Shaoyin Cheng (University of Science and Technology of China China), Guoqiang Chen (University of Science and Technology of China China), Weiming Zhang (University of Science and Technology of China China), David Lo (Singapore Management University Singapore)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 6. Clarity: From Formal System Designs to Verified RL Controllers

**Authors:** Austin O'Quinn (Ohio State University United States), Conor Snedeker (Ohio State University United States), Max Taylor (Boise State University United States), Lance Joneckis (Idaho National Lab United States), Christopher Stewart (The Ohio State University, USA United States)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 7. Conflict Extraction in Probabilistic Datalog Analyses

**Authors:** Siyu Chen, Chungha Sung (Amazon, USA United States), Xuyang Li (Purdue University United States), Jingbo Wang (Purdue University United States)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 8. Fully Automating Template Polyhedral Analysis by Leveraging LLMs

**Authors:** Renjie Huang (National University of Defense Technology China), Liqian Chen (National University of Defense Technology China), Hongfei Fu (Shanghai Jiao Tong University China), Banghu Yin (College of Computer, National University of Defense Technology, Changsha, China China), Dengping Wei (National University of Defense Technology China), Ji Wang (National University of Defense Technology China)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 9. GPU-Accelerated Belief Propagation for Program Analysis

**Authors:** Haoyu Feng (Peking University China), Xin Zhang (Peking University China)

**Categories:** Program Analysis and Verification

**中文总结:** 提出 GPU 加速信念传播框架 FastLBP，支持灵活更新策略与逻辑约束的程序分析。在 SmartFL 与 BINGO 上分别获得平均 17.42× 与 2.82× 加速，且保持精度。

**Abstract:** Belief Propagation (BP) is a widely used approximate inference algorithm in probabilistic graphical models (PGMs), but is computationally expensive when applied to large-scale program analysis. Existing GPU-based approaches are unable to support flexible update strategies and have yet to integrate logical constraints with GPU acceleration, leading to challenges in both generality and efficiency. We present FastLBP, a GPU-accelerated BP framework for program analysis. We propose a unified representation for specifying flexible update strategies required in program analysis, along with a dependency analysis algorithm to enable parallel execution. Furthermore, we implement BP with local structures on GPUs by assigning individual threads to message computations and utilizing a memory-efficient representation. Experiments on SmartFL and BINGO show that FastLBP achieves average speedups of $17.42\times$ and $2.82\times$ over CPU-based approaches on SmartFL and BINGO, respectively, and $6.14\times$ over GPU-based approach on SmartFL, while preserving accuracy. Moreover, FastLBP supports update strategies that existing GPU-based approaches cannot support, demonstrating its improved generality for real-world program analysis.


## 10. Inferring the Shape of Data Frames in R Programs using Abstract Interpretation

**Authors:** Oliver Gerstl (Ulm University Germany), Florian Sihler (Ulm University Germany), Matthias Tichy (Ulm University Germany)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 11. Learning the Lexical Structure of Black-Box Systems by Parsing Systematic String Edit Mutations

**Authors:** Moeketsi Raselimo (Humboldt-Universität zu Berlin), Lars Grunske (Humboldt-Universität zu Berlin Germany), Bernd Fischer (Stellenbosch University South Africa)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 12. Maximal Format-Free Data Repair

**Authors:** Zijian Luo (University of Sydney, Australia Australia), Xi Wu (The University of Sydney Australia), Hong Jin (Kang University of Sydney Australia), Alan Fekete (University of Sydney Australia), Rahul Gopinath (University of Sydney Australia)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 13. On the Effects of Customized Configurations of Static Code Analysis Tools: A Prospective Cohort Study of SonarQube Cloud

**Authors:** Sabato Nocera (University of Salerno Italy), Sira Vegas (Universidad Politecnica de Madrid Spain), Giuseppe Scanniello (University of Salerno Italy)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 14. PL4SA: Optimized Partial Library Selection for Efficient Static Analysis

**Authors:** Guohao Feng (Nanjing University China), Yifei Lu (State Key Laboratory for Novel Software Technology, Nanjing University, China), Minxue Pan (Nanjing University China)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 15. Precise and Efficient Static Data Race Detection

**Authors:** Pei Wang (Tsinghua University China), Zhihang Sun (Tsinghua University China), Fei He (Tsinghua University China)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 16. Quick Bug Detection through Black-Box Checking: A Systematic Evaluation

**Authors:** Bram Pellen (Radboud University Netherlands), María Belén (Rodríguez University of Twente Netherlands), Frits Vaandrager (Radboud University Netherlands), Petra (van den Bos University of Twente, The Netherlands Netherlands)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 17. RFC2TLA+: Extracting and Verifying Formal Models from RFC Documents using Continuous LLM Feedback

**Authors:** Guozhen Ding (University of Toronto Canada), Kexin Li (University of Toronto Canada), Ilya Grishchenko (University of California, Santa Barbara Canada), David Lie (University of Toronto, Canada Canada)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 18. SIMD-Accelerated Sparse Bit-Vectors for Pointer Analysis

**Authors:** Zhaoyang Tan (Zhejiang University China), Peisen Yao (Zhejiang University China), Kui Ren (Zhejiang University China)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 19. Sound and Efficient Statistical Model Checking for Probabilities and Bounded Rewards

**Authors:** Hao Bu (Ant Group; Zhejiang University China), Lin Huang (Ant Group China), Tao Wei (Ant Group), Jingyi Wang (Zhejiang University China)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 20. VARIES: Verification Harness Synthesis and Efficient Scheduling for Unsoundness Detection in Rust Libraries

**Authors:** Huan Li (Zhejiang University China), Xing Hu (Zhejiang University China), Xin Xia (Zhejiang University China), Xinyu Wang (Zhejiang University)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 21. Verifier-in-the-Loop LLM Solving of Heap Constraints for Concolic Execution

**Authors:** Shaoran Xia (Fudan University China), Leyi Cheng (Soochow University China), Caihua Dong (Fudan University China), Dongdong She (HKUST (The Hong Kong University of Science and Technology) Hong Kong SAR China), Bo Wang (Beijing Jiaotong University China), Xin Peng (Fudan University China), Zhen Dong (Fudan University China)

**Categories:** Program Analysis and Verification

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)
