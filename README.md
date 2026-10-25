# Agent Skill 恶意检测 · 论文阅读笔记

当前重点阅读 **Agent Skill 的恶意检测**：关注技能说明、代码与配置如何共同形成恶意行为，以及检测方法怎样建立证据、控制误报并适应真实生态。

**6 篇精读笔记 · 46 项既往背景文献与工具 · 时间线与关系图**

## 当前重点：Agent Skill 恶意检测

| 论文 | 会议 / 阅读版本 | 研究主题 | 阅读关注点 |
| --- | --- | --- | --- |
| [MalSkills](malskills/README.md) | ASE 2026录用；arXiv v2 | 神经符号检测、跨文件依赖、恶意技能 | 如何把说明、配置与脚本中的分散线索连成恶意行为证据？ |

后续笔记优先采用「**标题与作者、论文与代码 → 背景及切入点 → 创新与实现 → 实验设置与结论**」的故事线，重点解释方法如何实现，尽量贴近原文并保留出处。

### 方向调整说明 · 2026-10-25

此前以大模型越狱攻防为主要阅读方向；从本次起，后续阅读重点调整为 **Agent Skill 恶意检测与智能体供应链安全**。已有越狱笔记及背景资料继续保留，作为理解提示注入、代理分析和检测对抗的基础。

## 既往研究背景：大模型越狱

**[大模型越狱：背景与历史研究](jailbreak-background/README.md)**

从已读论文的引言与相关工作出发，按年份汇总攻击、护栏和防御。核心贡献依据原文，出处保留论文名与 PDF 页码。

[研究时间线](jailbreak-background/README.md#timeline) · [核心文献表](jailbreak-background/README.md#literature) · [主要论文关系图](jailbreak-background/README.md#relations) · [文献索引](jailbreak-background/资料/文献索引.json)

## 既往精读：大模型越狱攻防

| 论文 | 会议 / 版本 | 研究主题 | 阅读关注点 |
| --- | --- | --- | --- |
| [Causal Analyst](causal-analyst/README.md) | NDSS 2026 | 可读提示特征、因果图、越狱攻防 | 图结构、特征知识与额外训练的收益如何区分？ |
| [TRAP](trap/README.md) | arXiv v1，2026 | 黑盒越狱、策略树、经验复用 | 跨任务共享偏好是否实现了当前任务的策略匹配？ |
| [Best-of-N](best-of-n/README.md) | NeurIPS 2025 | 随机增强、多模态、查询预算 | 预算内至少成功一次与固定输入重复有效有何区别？ |
| [DUALBREACH](dualbreach/README.md) | NDSS 2026 | 双重越狱、本地代理、多目标优化 | 如何同时面对外部护栏与目标模型，并减少在线试探？ |
| [GCG](gcg/README.md) | arXiv v2，2023 | 对抗后缀、离散搜索、跨任务与跨模型迁移 | 自动搜索的后缀，能否用于未见问题和陌生模型？ |

## 阅读路径

围绕当前方向，先读 **[MalSkills](malskills/README.md)**，理解「敏感操作提取 → 依赖图 → 上下文推理」；后续重点核对检测证据、数据标签、误报与漏报、跨文件覆盖和生态评估。

补充既往越狱基础时，可通过[背景表与关系图](jailbreak-background/README.md)建立全貌：**Causal Analyst** 关注提示特征与结果，**TRAP** 关注策略选择，**Best-of-N** 关注随机采样与预算，**DUALBREACH** 关注护栏与模型两道防线。

想理解自动化后缀搜索与迁移攻击的基础，可以从 **[GCG](gcg/README.md)** 开始，再与后续方法对照。

论文事实附原文出处，个人理解与评价在笔记中另行说明；图表来源见各篇说明。

欢迎通过 [Issue](https://github.com/Zhang123d/paper-reading-notes/issues) 补充文献或指出理解偏差，并附上原文页码以便核对。
