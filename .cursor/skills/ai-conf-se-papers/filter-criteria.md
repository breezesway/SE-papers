# SE / Coding 论文筛选标准

与项目根目录 `se_paper_filter_prompt.md` 保持一致。执行本 skill 时按此精筛。

## 总体原则

1. 只要「与软工实践联系强」的论文；宁缺毋滥。
2. 优先保留 Coding Agent / AI for SE；其它代码相关工作需明显服务软件开发、维护、测试、缺陷、仓库级任务等。
3. 不要为了召回而放宽到「凡是提到 code / agent / vulnerability 都算」。
4. 去重；只保留主会 Research Track（排除 workshop / blog / journal track / demo，除非用户明确要求）。

## 必须保留（INCLUDE）

### A. Coding Agent / SWE（最高优先级，基本全留）

- software engineering agents、coding agents、SWE-bench 及其变体
- 仓库级（repository-level / repo-level）开发、修 bug、实现 feature、localization
- GitHub issue / pull request 相关自动化
- AI software engineer / developer agents、OpenHands 类平台
- 真实软件工程流程中的交互式 coding agents、环境配置、测试反馈、execution-free reward 等

### B. 强软工向（非 agent，但联系紧，可保留）

- 单元测试生成 / 测试补全（unit test generation）
- 程序修复 / debugging（program repair, bug fixing）面向真实代码
- 静态分析 + LLM 检测安全漏洞（**software** vulnerability，非模型 jailbreak）
- 软件故障根因分析（root cause of software failures）
- IDE/代码编辑辅助（实时编辑、edit sequences、code completion 用于开发场景）
- 代码检索/重排服务维护与修 bug（code retrieval for maintenance）
- 形式化验证/可验证代码生成（面向软件正确性）
- 贴近工程实践的代码评测（LiveCodeBench / BigCodeBench / SWE 类、真实项目单测基准）
- 安全代码生成（secure code generation for software）

## 必须排除（EXCLUDE）

1. 纯 Code LLM 预训练 / 数据配方 / tokenizer / scaling laws（训练模型本身为主）
2. 泛化 LLM/Agent，但任务不是写软件：web/computer-use/game/science/GUI agent（除非明确做 SE）；无 SE 场景的工作流/agent 搜索框架
3. 「code」只是副作用：数学奥赛写代码、科学公式 discovery、通用推理顺带测 code
4. 同名干扰：speech/video/audio/predictive/neural/sparse/channel coding；ML 的 jailbreak/backdoor/hallucination defense
5. 硬件描述为主（Verilog/RTL）且非软件 SE
6. 纯模型结构/搜索/inference scaling，仅用 codegen 当实验床
7. 过宽的 code understanding 选择题榜、多语言 code 能力榜——除非对接仓库/issue/测试/修复/开发流程

## 灰区（DEFAULT = DROP）

仅当摘要明确指向软件开发/维护流程才升格，并写明理由：

- Paper2Code / 科研代码复现（弱 SE）
- chart-to-code / visualization coding（弱 SE）
- 代码美学、watermark、IP 保护
- 二进制/汇编（仅明确软件安全分析/逆向时保留）
- 数据科学 agent：默认 drop，用户要求放宽才留
- 同态加密等垂直域 secure codegen：默认可标「可选」或 drop

## 两阶段流程

**Step 1 召回**：标题+摘要关键词，例如  
`software engineering, SWE-bench, coding agent, repository-level, GitHub issue, program repair, unit test, static analysis, code generation, code completion, code review, secure code, verifiable code, LiveCodeBench, BigCodeBench, OpenHands`  
并用排除词丢掉明显噪声。

**Step 2 精筛**：Agent/SWE 按 A 保留并剔泛 agent；其它类必须能回答「这解决的是哪个软件工程问题？」否则丢弃。

## 跨会议尺度

- **ACL / EMNLP**：仍按是否服务软件工程判断；排除 code-switching、programming language linguistics 等
- **ICML / NeurIPS**：方法论文挂 code 实验时偏严；优先 agent/SWE/测试修复
- **ICLR**：可参考仓库内 `iclr2025_se_coding/`、`iclr2026_se_coding/` 已有尺度
