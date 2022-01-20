# RFCs

- [RFCs](#rfcs)
  - [什么是 RFC？](#什么是-rfc)
  - [RFC 的生命周期](#rfc-的生命周期)
  - [何时遵循这个过程](#何时遵循这个过程)
    - [什么是实质性的改变？](#什么是实质性的改变)
    - [有些变化不需要 RFC](#有些变化不需要-rfc)
  - [创建 RFC 之前](#创建-rfc-之前)
  - [RFC 流程](#rfc-流程)
  - [RFC 实施](#rfc-实施)
  - [RFC 审查](#rfc-审查)
  - [RFC 灵感](#rfc-灵感)
  - [RFC 参考](#rfc-参考)

## 什么是 RFC？

"RFC"（征求意见稿）过程的目的是为新功能进入框架提供一个一致且可控的途径。

许多变化，包括错误修复和文档改进都可以通过正常的 GitHub 拉动请求工作流程来实现和审查。

但有些变化是**实质性**的，我们要求这些变化要经过通过一些设计过程，并在 `Growing Web` 团队和社区中产生共识。

## RFC 的生命周期

一个 RFC 会经历以下阶段。

- **待定：** 当 RFC 被提交为 PR 时。
- **激活：** 当 RFC PR 被合并且正在实施时。
- **落地：** 当 RFC 的提议修改内容已经实际发布时。
- **拒绝：** 当一个 RFC PR 没有被合并就被关闭。

[待处理的 RFC 列表](https://github.com/growing-web/rfcs/discussions/categories/rfc-discussions)

## 何时遵循这个过程

如果你打算对下列项目进行**实质性**修改，你需要遵循这个过程。

- [growing-web](https://github.com/growing-web/growing-web)

我们限制了这些仓库的 RFC 流程，以便以一种更易于管理的方式测试该流程，并可能在未来将其扩展至覆盖 `Growing Web`组织下的更多项目。目前，如果你想对其他项目提出修改建议，请使用他们各自的 issue 提问。

### 什么是实质性的改变？

**实质性**的改变包括但不限制于以下内容：

- 创造新的 API。
- 改变现有 API 的语义或行为。
- 移除已经作为发布版本的一部分功能。
- 引入新的用法或惯例，即使它们不包括对 `Growing Web` 本身的代码修改。

### 有些变化不需要 RFC

- 严格改进客观、数值质量标准的添加（警告删除、加速、更好的平台覆盖、更多并行性、捕获更多错误等）。
- 修复客观上不正确的行为。
- 改写、重组、重构或以其他方式"改变格式不会改变意义"。
- 增加或删除注释。
- 只有可能被其他 `Growing Web` 的开发者注意到的添加/修改，对 `Growing Web` 的用户来说是不可见的。

如果您在未通过 RFC 流程的情况下提交 PR 以实现新功能，则可能会以请求先提交 RFC 来关闭它。

## 创建 RFC 之前

匆忙提出的 RFC 可能会降低其被接受的机会。低质量的提案、先前被拒绝的功能提案或不适合近期路线图的提案可能会很快被拒绝，这可能会让没有准备的贡献者失去动力。所以在 RFC 之前打下一些基础可以使过程更加顺畅。通常最好的做法是事先征求其他项目开发人员的反馈，以确定 RFC 是否可取，对项目产生一致的影响需要共同努力建立共识。

## RFC 流程

简而言之，要为 `Growing Web` 添加一个主要功能，首先必须将 RFC 作为 markdown 文件合并到 RFC 存储库中。那时 RFC 是 **活跃的** ，并且可以以最终包含到 `Growing Web` 的目标来实现。

1. Fork 该 RFC 存储库。
2. 根据这个仓库的 `0000-rfc-template.md` 模版来处理你的 RFC 文本

   - 完善 RFC 文本，**注意：** 没有令人信服的动机、缺乏对设计影响的理解、或者对缺点或替代方案不诚实的 RFC 往往不受欢迎。

3. 在[GitHub Discussions 讨论](https://github.com/growing-web/rfcs/discussions/categories/rfc-discussions)中新建一个讨论话题，并确保将类别设置为 **RFC Discussions**。

   - 在讨论中建立共识并整合反馈，获得广泛支持的 RFC 比那些没有收到任何评论的 RFC 更有可能取得进展。
   - 给 Discussions 添加标签 `RFC：under discussions`，如果该提案还处于整理阶段，需要额外添加 `WIP` 标签。

4. 如果提案收到成员积极的反馈和建议，您可以讨论并修改后准备一个 PR。

   - 复制 `0000-rfc-template.md` 到 `active-rfcs/0000-my-feature.md`（其中 **my-feature** 是描述性的）。暂时不要分配 RFC 编号，这将是 PR 编号，如果 RFC 被接受，我们将相应地重命名文件。
   - 提交 PR，确保链接到[GitHub discussions 讨论](https://github.com/growing-web/rfcs/discussions) 中对应的讨论。

5. 最终，团队将决定 RFC 是否是包含在 `Growing Web` 中的候选列表并进行合并。

## RFC 实施

RFC 的作者没有义务实施它。当然，欢迎 RFC 作者（与任何其他开发人员一样）在 RFC 被接受后提交 PR 以供审查。

如果有的话，一个活跃的 RFC 应该列出实现 PR 的链接。对实际实现的反馈应该在实现 PR 而不是原始的 RFC PR 中进行。

## RFC 审查

团队的成员将尝试定期审查一些开放的 RFC 拉取请求。如果核心团队成员认为 RFC PR 已准备好被接受为活动状态，他们可以使用 GitHub 的审查功能批准 PR，以表明他们对 RFC 的批准。

## RFC 灵感

`Growing Web` 的 RFC 流程灵感来源于：

- [Vue RFC 流程](https://github.com/vuejs/rfcs)
- [Rust RFC 流程](https://github.com/rust-lang/rfcs)

## RFC 参考

- [Vue Discussions](https://github.com/vuejs/rfcs/discussions/369)
