# FSE 2025 Research Track — Mining Software Repositories

Source: https://conf.researchr.org/track/fse-2025/fse-2025-research-papers?#event-overview

Total in this category: 3 papers

## 1. Core Developer Turnover in the Rust Package Ecosystem: Prevalence, Impact, and Awareness

**Authors:** Meng Fan (Beijing Institute of Technology), Yuxia Zhang (Beijing Institute of Technology), Klaas-Jan Stol (Lero; University College Cork; SINTEF Digital), Hui Liu (Beijing Institute of Technology)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729392

**中文总结:** 对 Rust 包生态中 36,991 个包的核心开发者流失做大规模实证，发现流失普遍且多数包仅有一名核心开发者，会显著降低质量与维护效率甚至导致废弃；开发者调研强调上游依赖健康状态的透明与及时通知。

**Abstract:** Continued contributions of core developers in open source software (OSS) projects are key for sustaining and maintaining successful OSS projects. A major risk to the sustainability of OSS projects is developer turnover. Prior studies have explored developer turnover at the level of individual projects. A shortcoming of such studies is that they ignore the impact of developer turnover on downstream projects. Yet, an awareness of the turnover of core developers offers useful insights to the rest of an open source ecosystem. This study performs a large-scale empirical analysis of code developer turnover in the Rust package ecosystem. We find that the turnover of core developers is quite common in the whole Rust ecosystem with 36,991 packages. This is particularly worrying as a vast majority of Rust packages only have a single core developer. We found that core developer turnover can significantly decrease the quality and efficiency of software development and maintenance, even leading to deprecation. This is a major source of concern for those Rust packages that are widely used. We surveyed developers’ perspectives on the turnover of core developers in upstream packages. We found that developers widely agreed that core developer turnover can affect project stability and sustainability. They also emphasized the importance of transparency and timely notifications regarding the health status of upstream dependencies. This study provides unique insights to help communities focus on building reliable software dependency networks.

## 2. Scientific Open-Source Software Is Less Likely To Become Abandoned Than One Might Think! Lessons from Curating a Catalog of Maintained Scientific Software

**Authors:** Addi Malviya-Thakur (The University of Tennessee, Knoxville / Oak Ridge National Laboratory), Reed Milewicz (Sandia National Laboratories), Mahmoud Jahanshahi (University of Tennessee), Lavinia Francesca Paganini (Eindhoven University of Technology), Bogdan Vasilescu (Carnegie Mellon University), Audris Mockus (University of Tennessee)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729369

**中文总结:** 作者从约 0.5M 活跃仓库中筛选并分类大规模科学软件目录，建模领域、基础设施层等对可持续性的影响，并与匹配的非科学 OSS 对比。基础设施层、上游依赖与出版物提及与更长寿命相关；科学开源项目寿命反而长于匹配对照。

**Abstract:** Scientific software is increasingly essential to support scientific innovation and in many ways it is distinct from other types of software. Unmaintained, buggy, and hard to use software, a perception often associated with scientific software, can hinder scientific progress, yet, in contrast to other types of software, its sustainability is poorly understood. This may partly stem from the absence of an extensive collection of scientific software projects from diverse domains that represent different layers of the software infrastructure as existing curation efforts are fragmented by science domain and/or are small in scale and lack key attributes. We, therefore, aim to curate a large and diverse collection scientific software, including key likely precursors of sustainability and create models of sustainability to understand and inform future research and practice. We first filter 0.5M most active repositories (from over 200M) and use advanced language models to classify software projects into distinct scientific domains and infrastructure layers. After validation, we model how the domain, layer, and other attributes of scientific software affect its sustainability. We further obtain a matched sample of nonscientific software repositories and investigate the differences between scientific and nonscientific software sustainability. We find that infrastructural layers, upstream dependencies, and mentioned publications are associated with a longer lifespan, while projects started further in the past, having bursty activity had shorter lifespan. Against common expectations, science projects have a longer lifetime than matched Open source software (OSS) projects.

## 3. Who Will Stop Contributing to OSS Projects? Predicting Company Turnover Based on Initial Behavior

**Authors:** Mian Qin (Beijing Institute of Technology), Yuxia Zhang (Beijing Institute of Technology), Klaas-Jan Stol (Lero; University College Cork; SINTEF Digital), Hui Liu (Beijing Institute of Technology)

**Categories:** Mining Software Repositories

**PDF:** https://dl.acm.org/doi/pdf/10.1145/3729393

**中文总结:** 以 Linux 内核等为对象研究企业参与 OSS 后的退出现象：约每年 12% 企业停止贡献，其中约六分之一曾为核心贡献者。基于早期行为特征训练 TCN 预测退出，AUC 约 0.76，并在 Rust 与 OpenStack 上保持稳定。

**Abstract:** Open Source Software (OSS) projects are no longer only developed by volunteers. Instead, many organizations, from early-stage startups to large global enterprises, actively participate in many well-known projects. The survival and success of OSS projects rely on long-term contributors, who have extensive experience and knowledge. While prior literature has explored volunteer turnover in OSS, there is a paucity of research on company turnover in OSS ecosystems. Given the intensive involvement of companies in OSS and the different nature of corporate contributors vis-a-vis volunteers, it is important to investigate company turnover in OSS projects. This study first explores the prevalence and characteristics of companies that discontinue contributing to OSS projects, and then develops models to predict companies’ turnover. Based on a study of the Linux kernel, we analyze the early-stage behavior of 1,322 companies that have contributed to the project. We find that approximately 12% of companies discontinue contributing each year; one-sixth of those used to be core contributing companies (those that ranked in the top 20% by commit volume). Furthermore, withdrawing companies tend to have a lower intensity and scope of contributions, make primarily perfective changes, collaborate less, and operate on a smaller scale. We propose a Temporal Convolutional Network (TCN) deep learning model based on these indicators to predict whether companies will discontinue. The evaluation results show that the model achieves an AUC metric of .76 and an accuracy of .71. We evaluated the model in two other OSS projects, Rust and OpenStack, and the performance remains stable.
