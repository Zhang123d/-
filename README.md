# 大模型安全论文阅读笔记 · LLM Security Paper Notes

面向关注大模型安全的研究者，记录论文的方法理解、实验评价与开放问题。当前从越狱攻防、因果发现和可解释性切入。

Chinese paper reading notes on LLM security, with a focus on methods, experimental evidence, and open research questions.

## 从这里开始

### Causal Analyst：从因果视角理解大模型越狱攻防

**论文：** *A Causal Perspective for Enhancing Jailbreak Attack and Defense* · NDSS 2026

这篇笔记沿着「可读提示特征 → 表示融合 → 图学习 → 攻防应用」梳理方法，并重点讨论一个问题：

> 应用收益中，因果图、特征知识与额外训练各自贡献了多少？

笔记包含：

- 数据规模的区分：5,000 个提示与跨 7 个模型的 35,000 次测试尝试。
- 方法关系：提示分类、图学习与文字解释如何衔接。
- 实验证据：原文已有的长度控制消融、Vanilla Extractor 对照，以及收益归因仍可继续追问的地方。
- 开放问题：数据覆盖、特征标注与图结构稳定性如何影响解释结论。

**[阅读完整笔记](https://github.com/Zhang123d/paper-reading-notes/blob/main/causal-analyst/README.md)** · [论文页面](https://www.ndss-symposium.org/ndss-paper/a-causal-perspective-for-enhancing-jailbreak-attack-and-defense/) · [作者代码](https://github.com/Master-PLC/Causal-Analyst)

## 笔记索引

| 论文 | 会议 | 主题 | 阅读切入点 |
| --- | --- | --- | --- |
| [Causal Analyst](https://github.com/Zhang123d/paper-reading-notes/blob/main/causal-analyst/README.md) | NDSS 2026 | 大模型安全、越狱攻防、因果发现 | 因果图的作用能否与特征知识、额外训练区分？ |

当前收录 1 篇笔记。

## 阅读方式

每篇笔记围绕三个层次展开：

1. **论文提出了什么：** 问题、方法、数据与实验设计。
2. **我怎样理解：** 贡献评价、关键假设与方法间的联系。
3. **还需要什么证据：** 已有对照能说明什么，哪些问题仍需验证。

笔记中的个人评价与论文结论分别标明。涉及复现时，需另外说明实验设置与实际完成情况。

## 交流与纠错

欢迎通过 [Issue](https://github.com/Zhang123d/paper-reading-notes/issues) 指出理解偏差、补充相关实验，或推荐适合对照阅读的论文。讨论时附上笔记段落、原文位置或实验依据，便于一起核对。

论文与配图的来源见各篇笔记。
