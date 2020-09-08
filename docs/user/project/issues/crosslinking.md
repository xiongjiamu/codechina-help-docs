# 关联Issue[](#crosslinking-issue "Permalink")

可以访问 Issue 页面了解更多关于 Issue 的内容。

## 在提交信息中关联[](#from-commit-messages "Permalink")

每次在提交消息中提及 Issue 时，您都会在开发工作流的两个阶段之间建立一种关系： Issue 本身以及与该 Issue 相关的第一次提交。

如果 Issue 和您要提交的代码都在同一项目中，则只需在提交消息中添加`#xxx` ，其中`xxx`是 Issue 编号。如果它们不在同一项目中，则可以将完整的 URL 添加到问题中（ `https://codechina.csdn.net/<username>/<projectname>/issues/<xxx>` ）。

```markdown
git commit -m "this is my commit message. Ref #xxx" 
```

或

```markdown
git commit -m "this is my commit message. Related to https://codechina.csdn.net/<username>/<projectname>/issues/<xxx>" 
```

**注意：**将您的第一次提交与您的 Issue 相关联，对于分析跟踪您的过程将非常重要。它将测量该 Issue 从计划到实施所花费的时间，即从创建 Issue 到进行第一次提交之间的时间。

## 在 Issue 中关联[](#from-related-issues "Permalink")

在合并请求及在其他 Issue 中提及相关 Issue 对您的团队成员和协作者了解有关同一主题的未解决 Issue 将很有帮助。

如上所述，当您从提交消息中提到 Issue时，您可以执行此操作。

当在 Issue `#222`提到 Issue `#111`时，Issue `#111`还将在其跟踪器中显示一条通知，也就是说，您只需提及一次即可在两个Issue 中均显示该关系。在[合并请求中](#from-merge-requests)提及 Issue 时，也是如此。

## 在合并请求中关联[](#from-merge-requests "Permalink")

在合并请求中提及 Issue 与在 Issue 中关联是一样的步骤。

当您在合并请求说明中提到 Issue 时，它就会[将 Issue 和合并请求链接在一起](#from-related-issues)。此外，您还可以[将 Issue 设置](/docs/user/project/issues/manage.md#closing-issues-automatically)为在合并请求合并后立即[自动关闭](/docs/user/project/issues/manage.md#closing-issues-automatically) 。