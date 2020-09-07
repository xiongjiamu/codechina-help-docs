# 分支[](#branches "Permalink")

分支是项目工作树的版本，您做的每组相关更改都将创建一个分支。这样可以使每组更改彼此独立，从而可以并行进行更改，而不会互相影响。

将更改推送到新分支后，您可以：

*   创建[合并请求](/docs/user/project/merge-request.md)
*   执行内联代码审查
*   与团队[讨论](/docs/user/discussions.md)实施情况

有关使用 CODEChina 管理分支的更多信息，请参见：

  - [默认分支](#default-branch)
  - [对比](#compare)
  - [删除已合并的分支](#delete-merged-branches)
  - [分支过滤搜索框](#branch-filter-search-box)

您也可以使用命令行管理分支。

## 默认分支[](#default-branch "Permalink")

创建新项目时 ，系统会将`master`设置为代码仓库的默认分支。您可以在项目的**项目设置>仓库>默认分支**下选择另一个分支作为项目的默认分支。

通过[ Issue 关闭模式](/docs/user/project/issues/manage.md#closing-issues-automatically)直接从合并请求中[关闭 Issue](/docs/user/project/issues/manage.md#closing-issues-automatically)时，目标是项目的**默认分支** 。

项目初始化时还对默认分支进行了[保护](/docs/user/project/protected-branch.md#protected-branches)，以防止意外删除和强制推送。

## 对比[](#compare "Permalink")

可以通过以下步骤对分支进行对比：

1.  进入项目页面
2.  在项目导航中选择**代码>Diff**
3.  使用[分支过滤搜索框](#branch-filter-search-box)选择要比较的[分支](#branch-filter-search-box)
4.  单击**比较**以内联查看更改

[![compare branches](/docs/img/compare_branches.png)](/docs/img/compare_branches.png)

## 删除已合并的分支[](#delete-merged-branches "Permalink")

[![Delete merged branches](/docs/img/delete_merged_branches.png)](/docs/img/delete_merged_branches.png)

此功能允许合并的分支被批量删除，作为此操作的一部分，只有已合并[但未受保护的](/docs/user/project/protected-branch.md)分支才会被删除。

这在清理那些合并请求时未自动删除的旧分支时非常好用。

## 分支过滤搜索框[](#branch-filter-search-box "Permalink")

[![Branch filter search box](/docs/img/branch_filter_search_box.png)](/docs/img/branch_filter_search_box.png)

此功能使您可以快速搜索和选择分支, 搜索结果按以下顺序显示：

*   名称与搜索字词完全匹配的分支
*   名称包含搜索词的其他分支，按字母顺序排序

当您有数百个分支时，可能需要更灵活的匹配模式。在这种情况下，您可以使用以下方法：

*   `^feature`将仅匹配以'feature'开头的分支名称
*   `feature$`将仅匹配以‘feature’结尾的分支名称