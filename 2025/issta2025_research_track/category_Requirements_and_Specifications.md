# ISSTA 2025 Research Track — Requirements and Specifications

Source: https://conf.researchr.org/track/issta-2025/issta-2025-papers#event-overview

Count: 1

## 1. NADA: Neural Acceptance-driven Approximate Specification Mining

**Authors:** Weilin Luo (Sun Yat-sen University), Tingchen Han (Sun Yat-Sen University), Junming Qiu (Sun Yat-sen University), Hai Wan (Sun Yat-sen University), Jianfeng Du (Guangdong University of Foreign Studies), Bo Peng (Sun Yat-Sen University), Guohui Xiao (Southeast University), Yanan Liu (SUN YAT-SEN UNIVERSITY)

**Categories:** Requirements and Specifications

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728956

**中文总结:** 将 FSA 接受性映射为神经网络推理过程（neural acceptance），提出 NADA，在含噪正负例上通过连续松弛与梯度下降直接搜索近似有限状态自动机。F1 平均提升41.63%，速度约为次优方法的19.8倍。

**Abstract:** It is hard to mine high-quality finite-state automata (FSAs) only from positive examples because of a search space explosion and an overgeneralization problem induced by a lack of negative examples. To tackle the overgeneralization problem, we suggest modeling the problem as searching for approximate FSAs from positive and negative examples with noise, where the noise originates from synthetic negative examples used to reject overgeneralized results. To obtain an effective search bias in the exploding search space and alleviate the wrong search bias resulting from noise, we bridge FSA acceptance to neural network inference. Our key contribution is to design a neural network whose parameter assignment corresponds to an FSA, and its neural inference process, named after neural acceptance, is able to simulate FSA acceptance. The neural acceptance provides a way to efficiently quantify how well an FSA fits noisy data. We propose NADA, a neural acceptance-driven approach, to directly search approximate FSAs guided by accepting positive examples and rejecting synthetic negative examples. NADA is based on a proper continuous relaxation of the discrete search space of FSAs and an efficient gradient descent-based search algorithm. Experimental results demonstrate that, compared with state-of-the-art approaches, NADA significantly improves the quality of mined FSAs (on average improves $41.63$% F1 score). Besides, NADA is $19.8$X faster than the approach mining sub-high-quality FSAs.
