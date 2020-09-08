# Squash合并[](#Squash合并 "Permalink")

使用 squash 合并，您可以将所有合并请求的提交合并为一个并保留干净的历史记录。

## 概览[](#overview "Permalink")

通过 squash，您可以在接受合并请求时整理分支的提交历史记录，它将合并请求中的所有更改作为单个提交，然后使用为项目设置的合并方法合并该提交。

换句话说，squash 合并后将会变成一长串提交：

[![List of commits from a merge request](/docs/img/squash_mr_commits.png)](/docs/img/squash_mr_commits.png)

合并为单个提交：

[![A squashed commit followed by a merge commit](/docs/img/squash_squashed_commit.png)](/docs/img/squash_squashed_commit.png)

压缩的提交的提交消息将是：

*   取自合并中的第一条多行提交消息
*   如果找不到多行提交消息，则合并请求的标题

**注意：**仅在至少 2 次提交时，此选项才生效。由于没有什么可压缩的，因此如果只有 1 次提交，则提交消息不会更改。

可以在合并合并请求之前对其进行自定义。

**注意：**在此示例中，压缩的提交之后是合并提交，因为此示例代码仓库的合并方法使用了合并提交。

Squash 也适用于快进合并策略，有关更多详细信息，请参见[压缩和快进合并](#squash-and-fast-forward-merge) 。

## 示例[](#use-cases "Permalink")

在功能分支上工作时，有时您想提交当前进度，但实际上并不关心提交消息。 这些"进行中的提交"不一定包含重要的信息，因此，您不想将其包含在目标分支中。

使用 squash 合并，当准备好要合并的合并请求时，您要做的就是在按下合并之前将 Squash 启用，以将合并请求中的提交加入到单个提交中。

这样，您的基本分支的历史记录将保留有意义的提交消息，并且：

*   在有需要的情况下， [Revert](revert.md)更为简单
*   合并的分支将保留完整的提交历史记录

## 合并时启用 Squash[](#enabling-squash-for-a-merge-request "Permalink")

可以创建或编辑合并请求的任何人都可以选择将其压缩在合并请求表单上：

[![Squash commits checkbox on edit form](/docs/img/squash_edit_form.png)](/docs/img/squash_edit_form.png)

然后可以在接受合并请求时覆盖它：

[![Squash commits checkbox on accept merge request form](/docs/img/squash_mr_widget.png)](/docs/img/squash_mr_widget.png)

## Squash 提交的元数据[](#commit-metadata-for-squashed-commits "Permalink")

Squash 的提交具有以下元数据：

*   消息： Squash 提交消息或自定义消息
*   作者：合并请求的作者
*   提交者：发起 Squash 的用户

## Squash 和快进合并[](#squash-and-fast-forward-merge "Permalink")

当项目[启用](fast_forward.md#enabling-fast-forward-merges)了[快进合并设置时](fast_forward.md#enabling-fast-forward-merges) ，合并请求必须能够不 Squash 而进行快速转发以进行 Squash，这是因为 Squash 仅在接受合并请求时可用，因此即使 Squash 本身可以被认为等同于重新 Rebase，也可能需要在 Squash 之前对合并请求进行重新基准化。