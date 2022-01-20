# 技术方案

- [技术方案](#技术方案)
  - [什么是 技术方案？](#什么是-技术方案)
  - [何时需要写技术方案](#何时需要写技术方案)
  - [技术方案 流程](#技术方案-流程)

## 什么是 技术方案？

针对存在和可预期的问题（技术、业务、团队）的不足、缺陷、需求的解决方案，确保问题有效解决，方案有效落地。

[正在讨论的技术方案列表](https://github.com/growing-web/rfcs/discussions/categories/solutions-discussions)

## 何时需要写技术方案

- 技术方案不会成为额外的负担，从技术方案的意义来看，当一个问题需要解决的时候，都需要技术方案。
- 需要他人帮助，了解你的思路才能给你提供帮助；

## 技术方案 流程

1. Fork 该存储库。
2. 根据这个仓库的 `0000-solutions-template.md` 模版来处理你的技术方案文本

   - 完善技术方案文本。

3. 在[GitHub Discussions 讨论](https://github.com/growing-web/rfcs/discussions/categories/solutions-discussions)中新建一个讨论话题，并确保将类别设置为 **Solutions Discussions**。

   - 在讨论中建立共识并整合反馈。
   - 给 Discussions 添加标签 `Solutions`，如果该方案还处于整理阶段，需要额外添加 `WIP` 标签。

4. 如果提案收到成员积极的反馈和建议，您可以讨论并修改后准备一个 PR。

   - 复制 `0000-solutions-template.md` 到 `active-rfcs/0000-my-solutions.md`（其中 **my-solutions** 是描述性的）。暂时不要分配编号，这将是 PR 编号，如果方案被接受，我们将相应地重命名文件。
   - 提交 PR，确保链接到[GitHub discussions 讨论](https://github.com/growing-web/rfcs/discussions) 中对应的讨论。

5. 最终，团队将决定技术方案是否是包含在 `Growing Web` 中的候选列表并进行合并。
