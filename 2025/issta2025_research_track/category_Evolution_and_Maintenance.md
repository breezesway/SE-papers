# ISSTA 2025 Research Track — Evolution and Maintenance

Source: https://conf.researchr.org/track/issta-2025/issta-2025-papers#event-overview

Count: 5

## 1. More Effective JavaScript Breaking Change Detection via Dynamic Object Relation Graph

**Authors:** Dezhen Kong (Zhejiang University), Jiakun Liu (Singapore Management University), Chao Ni (Zhejiang University), David Lo (Singapore Management University), Lingfeng Bao (Zhejiang University)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728980

**中文总结:** 系统分析现有 JavaScript 破坏性变更检测工具的漏检与误报根因，提出 Diagnose：基于 API 探索与强制执行类型分析迭代构建对象关系图，并在新版本重建图进行对比。相较实证研究所用基线，多检出60.2%破坏性变更且误报更少。

**Abstract:** JavaScript libraries are characterized by their widespread use, frequent code changes, and a high tolerance for backward incompatible changes. Awareness of such breaking changes can help developers adapt to version updates and avoid negative impacts. Several tools have been targeted to or can be used to detect breaking change detection in the JavaScript community. However, these tools detect breaking changes using different ways, and there are currently no systematic reviews of these approaches. From a preliminary study on popular JavaScript libraries, we find that existing approaches, including simple regression testing, model-based testing and type differencing cannot detect many breaking changes but can produce plenty of false positives. We discuss the reasons for missing breaking changes and producing false positives.

Based on the insights from our findings, we propose a new approach named Diagnose that iteratively constructs an object relation graph based on API exploration and forced execution-based type analysis. Diagnose then refine the graphs and reconstruct the graphs in the newer versions of the libraries to detect breaking changes. By evaluating approach on the same set of libraries used in the empirical study, we find that Diagnose can detect much more breaking changes (60.2%) and produce fewer false positives. Therefore, Diagnose is suitable for practical use.

## 2. PatchScope: LLM-Enhanced Fine-Grained Stable Patch Classification for Linux Kernel

**Authors:** Rongkai Liu (Central South University), Heyuan Shi (Central South University), Shuning Liu (Central South University, China), Chao Hu (Central South University), Sisheng Li (Central South University, China), Yuheng Shen (Tsinghua University), Runzhe Wang (Alibaba Group), Xiaohai Shi (Alibaba Group), Yu Jiang (Tsinghua University)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728944

**中文总结:** 针对现有工具无法判断 stable patch 应合并至哪个 LTS 版本的问题，提出 PatchScope：用 LLM 从 commit 与代码变更生成 patch 语义描述，再以预训练语言模型与两阶段分类器预测合并状态，并采用动态加权损失缓解类别不平衡。在 Linux 5.10 与 6.6 上可有效预测 patch 合并去向。

**Abstract:** Stable patch classification plays a crucial role in vulnerability management for the Linux kernel, significantly contributing to the stability and security of Long-term support~(LTS) versions. Although existing tools have effectively assisted in assessing whether patches should be merged into stable versions, they cannot determine which stable patches should be merged into which LTS versions. This process still requires the maintainers of the distribution community to manually screen based on the requirements of their respective versions. To address this issue, we propose PatchScope, which is designed to predict the specific merge status of patches. Patchscope consists of two components: patch analysis and patch classification. Patch analysis leverages Large Language Models~(LLMs) to generate detailed patch descriptions from the commit message and code changes, thereby deepening the model’s semantic understanding of patches. Patch classification utilizes a pre-trained language model to extract semantic features of the patches and employs a two-stage classifier to predict the merge status of the patches. The model is optimized using the dynamic weighted loss function to handle data imbalance and improve overall performance. Given that the primary focus is maintaining Linux kernel versions 5.10 and 6.6, we have conducted comparative experiments based on these two versions. Experimental results demonstrate that Patchscope can effectively predict the merge status of patches.

## 3. Productively Deploying Emerging Models on Emerging Platforms: A Top-Down Approach for Testing and Debugging

**Authors:** Siyuan Feng (Shanghai Jiao Tong University), Jiawei Liu (University of Illinois at Urbana-Champaign), Ruihang Lai (Carnegie Mellon University), Charlie F. Ruan (Carnegie Mellon University), Yong Yu (Shanghai Jiao Tong University), Lingming Zhang (University of Illinois at Urbana-Champaign), Tianqi Chen

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728957

**中文总结:** 提出自顶向下 ML 部署方法与工具 TapML：以 test carving 自动化算子级测试，并通过从成熟源平台向 Metal、Vulkan、WebGPU 等目标平台逐步迁移计算来缩小调试范围。一年内实践部署105个新兴模型至5个平台，显著提升开发效率与部署质量。

**Abstract:** While existing machine learning (ML) frameworks still focus on established platforms, like running CUDA on server-grade GPUs, there have been growing demands to enable emerging AI applications in a broader set of scenarios, such as running Large Language Models (LLMs) within browsers and mobile phones. However, deploying emerging models on new platforms (such as Metal, Vulkan, and WebGPU) presents significant software engineering challenges due to rapid model evolution and the limited tooling and best practices available for these platforms.

Previous practice for ML model deployment typically follows a bottom-up fashion, where engineers first implement individual required operators and then put them together. However, this traditional development approach fails to meet the productivity requirements when deploying emerging ML systems, with the testing and debugging part as a bottleneck. To this end, we introduce TapML, a top-down approach and tooling designed to streamline the deployment of ML systems on diverse platforms, optimized for developer productivity. While the traditional bottom-up approach requires developers to craft manual tests, TapML automates operator-wise testing using test carving for creating realistic testing data with better quantity and quality. Furthermore, TapML adopts a migration-based strategy to gradually implement and offload model computations from the mature source platform to the target platform, minimizing the debugging scope for compounded bugs to single operators.

We have been practicing TapML to build our real-world framework for deploying emerging models on emerging platforms for more than a year. Through serious deployments of 105 emerging models in 27 distinct model architectures across 5 emerging platforms, we showcase the effectiveness of TapML in enhancing developer productivity while ensuring the quality of deployed models. Furthermore, we summarize comprehensive case studies from our real-world development, offering best practices for developing emerging ML systems.

## 4. SWE-GPT: A Process-Centric Language Model for Automated Software Improvement

**Authors:** Yingwei Ma (Alibaba Group), Rongyu Cao (Tongyi Lab, Alibaba, China), Yongchang Cao (Tongyi Lab, Alibaba, China), Yue Zhang (Tongyi Lab, Alibaba, China), Jue Chen (Tongyi Lab, Alibaba, China), Yibo Liu (Tongyi Lab, Alibaba, China), Yuchen Liu (Tongyi Lab, Alibaba, China), Binhua Li (Tongyi Lab, Alibaba, China), Fei Huang (Tongyi Lab, Alibaba, China), Yongbin Li (Tongyi Lab, Alibaba, China)

**Categories:** Evolution and Maintenance

**Awards:** ACM SIGSOFT Distinguished Paper Award

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728981

**中文总结:** 发布开源软件改进专用模型 SWE-GPT（7B/72B），从真实代码提交活动中学习仓库理解、缺陷定位、补丁生成等动态流程。SWE-GPT 72B 在 SWE-bench Verified 上解决 30.20% 的 GitHub issue，相对 Llama 3.1 405B 提升 22.76%，接近 GPT-4o 的 31.80%。

**Abstract:** Large language models (LLMs) have demonstrated remarkable performance in code generation, significantly enhancing the coding efficiency of developers. Recent advancements in LLM-based agents have led to significant progress in end-to-end automatic software engineering (ASE), particularly in software maintenance (e.g., fixing software issues) and evolution (e.g., adding new features). Despite these encouraging advances, current research faces two major challenges. First, state-of-the-art performance primarily depends on closed-source models like GPT-4, which significantly limits the technology’s accessibility, and potential for customization in diverse software engineering tasks. This dependence also raises concerns about data privacy, particularly when handling sensitive codebases. Second, these models are predominantly trained on static code data, lacking a deep understanding of the dynamic interactions, iterative problem-solving processes, and evolutionary characteristics inherent in software development. Consequently, they may face challenges in navigating complex project structures and generating contextually relevant solutions, which can affect their practical utility in real-world scenarios.

To address these challenges, our study adopts a software engineering perspective. We recognize that real-world software maintenance and evolution processes encompass not only static code data but also developers’ thought processes, utilization of external tools, and the interaction between different functional personnel. Our objective is to develop an open-source large language model specifically optimized for software improvement, aiming to match the performance of closed-source alternatives while offering greater accessibility and customization potential. Consequently, we introduce the \textbf{SWE-GPT} series, comprising SWE-GPT 7B and SWE-GPT 72B. By learning from and simulating real-world code submission activities, SWE-GPT systematically incorporates the dynamic interactions and iterative problem-solving inherent in software development process—such as repository understanding, fault localization, and patch generation—thereby achieving a more comprehensive understanding of software improvement processes. We conducted experimental evaluations using SWE-bench Verified benchmark (comprising 500 real GitHub issues), recently proposed by OpenAI. The results demonstrate that \textbf{SWE-GPT 72B successfully resolves 30.20% of the GitHub issues}, marking a significant improvement in automatic issue resolution (22.76% relative improvement compared to Llama 3.1 405B), approaching the performance of closed-source models (31.80% issues of GPT-4o resolved). Notably, SWE-GPT 7B resolves 18.20% of the issues, surpassing the 17.20% resolution rate of Llama 3.1 70B, highlighting the potential for applying smaller models to ASE tasks.

## 5. What Happened in This Pipeline? Diffing Build Logs With CiDiff

**Authors:** Nicolas Hubner (University of Bordeaux, LaBRI, UMR 5800, F-33400, Talence, France), Jean-Rémy Falleri (Univ. Bordeaux, CNRS, Bordeaux INP, LaBRI, UMR 5800, Institut Universitaire de France), Raluca Uricaru (Univ. Bordeaux, Bordeaux INP, CNRS, LaBRI, UMR5800, F-33400 Talence, France), Thomas Degueule (CNRS), Thomas Durieux (TU Delft)

**Categories:** Evolution and Maintenance

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3728966

**中文总结:** CiDiff 针对 CI 构建日志设计专用 diff 算法，替代通用 LCS-diff 以辅助回归诊断。在 17,906 个 CI 回归案例上，中位输出缩小约 20%、待查新行减少约 60%，70% 案例用户更偏好 CiDiff。

**Abstract:** Continuous integration (CI) is widely used by developers to ensure the quality and reliability of their software projects. However, diagnosing a CI regression requires comparing and analyzing lengthy logs of passing and failing builds, which can be laborious. As off-the-shelf diff algorithms produce suboptimal results, in this work we introduce a new diff algorithm specifically tailored to build logs called CiDiff. We evaluate CiDiff against the baseline LCS-diff on a novel dataset of 17,906 CI regressions, using quantitative metrics and a user study. Our algorithm reduces the output size by about 20% and the number of new lines to inspect by about 60% in the median case, with reasonable overhead. Finally, our algorithm is favored by the majority of participants in 70% of the regression cases, whereas LCS-diff is preferred in only 5% of the cases.
