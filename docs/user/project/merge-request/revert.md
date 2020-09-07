# Revert[](#revert "Permalink")

您可以使用 Git 的强大功能，通过在合并请求和提交详细信息中单击 **Revert**按钮来[还原任何提交](https://git-scm.com/docs/git-revert "Git 恢复文档") 。

## Reverting 合并请求[](#reverting-a-merge-request "Permalink")

**注意：**仅对使用合并方法"合并提交"的项目显示 **Revert** 按钮，该方法可以在项目的**"项目设置">"常规">"合并请求"**下**设置**，无法通过 合并请求视图还原[快进提交](fast_forward_merge.html)。

合并请求合并后，将有一个**还原**按钮可用于还原该合并请求引入的更改.

[![Revert Merge Request](/docs/img/cherry_pick_changes_mr.png)](/docs//docs/img/cherry_pick_changes_mr.png)

单击该按钮后，将出现一个弹窗，您可以在其中选择将更改直接还原到所选分支中，也可以选择使用还原更改创建新的合并请求。

合并请求 Revert 后，**Revert**按钮将不再可用。

## Reverting 提及[](#reverting-a-commit "Permalink")

您可以从提交详细信息页面 Revert 提交：

[![Revert commit](/docs/img/cherry_pick_changes_commit_revert.png)](/docs/img/cherry_pick_changes_commit_revert.png)

与 Revert 合并请求类似，您可以选择将更改直接还原到目标分支中，也可以选择创建新的合并请求以还原更改。

提交 Revert 后，** Revert **按钮将不再可用。

请注意，Revert 合并提交时，主线将始终是第一父级，如果要使用其他主线，则需要从 git 客户端行执行。

这是一个使用第二个父级作为主线还原合并提交的快速示例：

```markdown
git revert -m 2 7a39eb0 
```