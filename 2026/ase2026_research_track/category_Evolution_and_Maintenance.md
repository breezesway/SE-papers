# ASE 2026 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/ase-2026/ase-2026-research-track#event-overview

Count: 6

## 1. A Unified Model for Cross-Domain Clone Detection via Model Merging

**Authors:** Palash Ranjan (Roy University of Saskatchewan Canada), Banani Roy (University of Saskatchewan Canada), Kevin Schneider (University of Saskatchewan Canada), Chanchal K. (Roy University of Saskatchewan Canada)

**Categories:** Evolution and Maintenance

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 2. BDiff: Block-Aware and Accurate Text-Based Code Differencing

**Authors:** Yao Lu (National University of Defense Technology), Wanwei Liu (National University of Defense Technology China), Tanghaoran Zhang (National University of Defense Technology China), Kang Yang (National University of Defense Technology China), Yang Zhang (National University of Defense Technology, China China), Wenyu Xu (National University of Defense Technology China), Longfei Sun (National University of Defense Technology China), Xinjun Mao (National University of Defense Technology China), Shuzheng Gao (Chinese University of Hong Kong China), Michael Lyu (CUHK, Hong Kong)

**Categories:** Evolution and Maintenance

**中文总结:** 提出 BDiff 块感知文本 diff 算法，识别块级与行级编辑动作并最小化编辑脚本。实验表明其 diff 质量优于含 LLM 在内的基线，且 LLM 在质量与时效上不可靠。

**Abstract:** Code differencing is a fundamental technique in software engineering practice and research. While researchers have proposed text-based differencing techniques capable of identifying line changes over the past decade, existing methods exhibit a notable limitation in identifying edit actions (EAs) that operate on text blocks spanning multiple lines. Such EAs are common in developers' practice, such as moving a code block for conditional branching or duplicating a method definition block for overloading. Existing tools represent such block-level operations as discrete sequences of line-level EAs, compelling developers to manually correlate them and thereby substantially impeding the efficiency of change comprehension. To address this issue, we propose BDiff, a text-based differencing algorithm capable of identifying two types of block-level EAs and five types of line-level EAs. Building on traditional differencing algorithms, we first construct a candidate set containing all possible line mappings and block mappings. Leveraging the Kuhn-Munkres algorithm, we then compute the optimal mapping set that can minimize the size of the edit script (ES) while closely aligning with the original developer's intent. To validate the effectiveness of BDiff, we selected five state-of-the-art tools, including large language models (LLMs), as baselines and adopted a combined qualitative and quantitative approach to evaluate their performance in terms of ES size, result quality, and running time. Experimental results show that BDiff produces higher-quality differencing results than baseline tools while maintaining competitive runtime performance. Our experiments also show the unreliability of LLMs in code differencing tasks regarding result quality and their infeasibility in terms of runtime efficiency. We have implemented a web-based visual differencing tool.


## 3. CodeFault: Predicting Fault Risks from Code Changes via Multi-modal Learning

**Authors:** Yifan Xiao (Peking University China), Shijie Li (China Southern Power Grid Company Limited), Yu Huang (Vanderbilt University United States)

**Categories:** Evolution and Maintenance

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 4. DepUpgrade: Automating Dependency Upgrade through State-Path Exploration

**Authors:** An Yifan, Xiangxi Ma (Beihang University China), Wentong Tian (Beihang University China), Xuanqi Wang (Beihang University China), Qingao Dong (Beihang university China), Xiang Gao (Beihang University China), Hailong Sun (Beihang University China)

**Categories:** Evolution and Maintenance

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 5. Latent Reuse in Agent Skills: Multi-modal Clone Detection at Ecosystem Scale

**Authors:** Jiaying Zhu (Nanyang Technological University), Lyuye Zhang (Nanyang Technological University Singapore), Wenbo Guo (Nanyang Technological University), Yang Liu (Nanyang Technological University Singapore)

**Categories:** Evolution and Maintenance

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)


## 6. “We Must Have Missed This Comment”: Detecting and Repairing Stale Function References in Linux Kernel Comments

**Authors:** Kexin Sun (Nanjing University), Yunbo Lyu (Singapore Management University Singapore), Xutong Ma (Inria Paris France), Hongyu Kuang (Nanjing University China), Ratnadira Widyasari (Singapore Management University, Singapore), He Zhang (Nanjing University China), Xiaoxing Ma (Nanjing University China), Julia Lawall (Inria France), David Lo (Singapore Management University Singapore)

**Categories:** Evolution and Maintenance

**中文总结:** （目前没有摘要，因此没有总结）

**Abstract:** (摘要暂未在 researchr 页面提供)
