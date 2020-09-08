# Cherry-pick[](#cherry-pick "Permalink")

Cherry-pick 是 Git 中非常强大的一个功能，通过在合并请求和提交详细信息中引入**Cherry-pick**来[挑选任何想要的提交](https://git-scm.com/docs/git-cherry-pick "Git Cherry-Pick 文档") 。

## Cherry-pick 一个合并请求[](#cherry-picking-a-merge-request "Permalink")

合并请求合并后，将可以使用**Cherry-pick**按钮来选择该合并中需要引入的更改。

[![Cherry-pick Merge Request](/docs/img/cherry_pick_changes_mr.png)](/docs/img/cherry_pick_changes_mr.png)

单击该按钮后，会出现一个弹窗，将显示一个分支过滤器搜索框，您可以在其中选择：

*   将更改直接选择到所选分支中
*   使用经过 Cherry-pick 的更改创建一个新的合并请求

### Cherry-pick 跟踪[](#cherry-pick-tracking "Permalink")

当您选择一个合并提交时，系统会向相关的合并请求讨论中添加系统注释，使新提交与现有合并请求相关联。

每个部署的关联合并请求列表都将包括 Cherry-pick 的合并提交。

## Cherry-pick 一个提交[](#cherry-picking-a-commit "Permalink")

您可以从提交详细信息页面中挑选一个提交：

[![Cherry-pick commit](/docs/img/cherry_pick_changes_commit.png)](/docs/img/cherry_pick_changes_commit.png)

与选择合并请求类似，您可以选择将更改直接选择到目标分支中，也可以选择创建新的合并请求以选择更改。

请注意，在进行 Cherry-pick 合并提交时，主线将始终是第一父级， 如果要使用其他主线，则需要从命令行执行。

这是一个使用第二个父级作为主线来 Cherry-pick 合并提交的示例：

```markdown
git cherry-pick -m 2 7a39eb0 
```