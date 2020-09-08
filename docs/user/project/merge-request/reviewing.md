# 评审及管理合并请求[](#评审及管理合并请求 "Permalink")

合并请求是在项目中更改文件的主要方法，通过[创建并提交合并请求](/docs/user/project/merge-request/create-merge-request.md)来提出更改，然后将其审核并接受（或拒绝）。

## 评审合并请求[](#view-project-merge-requests "Permalink")

打开 **项目>合并请求**列表，可以查看项目中的所有**合并请求**，并且您可以快速按打开和关闭可用的选项卡来进行过滤，您还可以[搜索和过滤结果](/docs/user/search.md#filtering-issue-and-merge-request-lists)。

[![Project merge requests list view](/docs/img/project_merge_requests_list_view.png)](/docs/img/project_merge_requests_list_view.png)

## 半线性历史合并请求[](#semi-linear-history-merge-requests "Permalink")

每个合并创建一个合并提交，但是只有在可能进行快速合并的情况下才合并分支。这样可以确保如果合并请求构建成功，则合并后目标分支构建也将成功。

进入到项目设置页，在 **合并请求：合并方法**下选择 **使用半线性历史** **合并合并**选项，然后保存更改。

## 查看不同版本文件变更[](#view-changes-between-file-versions "Permalink")

**更改**选项卡位于主要合并请求详细信息下方，并且在讨论选项卡旁边，显示了分支或提交之间文件的更改。这种对文件更改的视图也称为**diff** ，默认情况下，差异视图将合并请求分支中的文件与目标分支中的文件进行比较。

Diff 视图包含以下内容:

*   文件的名称和路径
*   添加和删​​除的行数
*   用于以下选项的按钮：
    *   文件讨论显示/隐藏开关，在查看用于内联评论时非常有用
    *   在合并请求的分支中编辑文件
    *   显示完整文件，方便您要查看上下文中文件其余部分的更改
    *   查看当前提交时的文件
*   对于有更改的行，将突出显示详细的更改内容

[![Example screenshot of a source code diff](/docs/img/merge_request_diff_v13_2.png)](/docs/img/merge_request_diff_v13_2.png)

### 合并请求 diff 导航[](#merge-request-diff-file-navigation "Permalink")

在 **更改**选项卡中查看更改时，可以使用文件树或文件列表来浏览差异。 在具有许多更改的大型差异中滚动时，可以使用文件树或文件列表快速跳转到任何更改的文件。

[![Merge request diff file navigation](/docs/img/merge_request_diff_file_navigation.png)](/docs/img/merge_request_diff_file_navigation.png)

### 逐个文件查看 diff[](#file-by-file-diff-navigation "Permalink")

对于较大的合并请求，有时一次查看单个文件可能会很有用。要启用单个文件 diff 导航时，请从右上角导航栏上的头像，单击**"设置"** ，然后转到左侧边栏上的**"偏好设置"** ， 向下滚动到" **个性化"**部分，然后**在合并请求的"更改"标签上**选择**"一次显示一个文件"** . 点击**保存更改**以应用.

从那里，在查看合并请求的" **更改"**选项卡时，一次只能看到一个文件. 然后，您可以单击按钮上**一个**和**下一个**以查看其他已更改的文件.

[![File-by-file diff navigation](/docs/img/file_by_file_v13_2.png)](/docs/img/file_by_file_v13_2.png)

### 合并请求提交导航[](#merge-requests-commit-navigation "Permalink")

要在合并请求中的**提交**之间无缝导航，请从 **提交**选项卡中，单击其中一个提交以打开单提交视图，之后您可以通过单击页面右上角的**Prev**和**Next**按钮或使用`X`和`C`键盘快捷键在提交之间进行切换。

### 合并请求 diff 时展开[](#incrementally-expand-merge-request-diffs "Permalink")

默认情况下，差异仅显示文件中已更改的部分。要查看更改上方或下方的更多未更改行，请单击" **向上** **扩展"**或" **向下扩展"**图标，您也可以单击**显示未更改的行**以展开整个文件。

当查看合并请求的**更改**选项卡时，如果仅重命名了某个文件，则可以通过单击**显示文件内容**展开它以查看全部**内容** 。

### 隐藏空白更改[](#ignore-whitespace-changes-in-merge-request-diff-view "Permalink")

如果单击**隐藏空白更改**按钮，则可以看到没有空白更改的差异（如果有的话），在查看某个提交的页面上也支持这个功能。

> **提示：**您可以在合并请求的差异页面上附加`?w=1` ，以忽略任何空格更改。

## 行内代码评审[](#perform-inline-code-reviews "Permalink")

我们提供了一种在合并请求中更改文件的任何部分中进行注释讨论的方法，可以在"合并请求"差异页面左侧单击**评论**按钮以展开差异行并留下评论，就像更改行一样。

[![Comment on any diff file line](/docs/img/comment-on-any-diff-line.png)](/docs/img/comment-on-any-diff-line.png)

## 关联功能[](#associated-features "Permalink")

还有大量与合并请求关联的功能：

| 功能 | 描述 |
| --- | --- |
| [批量编辑合并请求](/docs/user/project/bulk-edit.md) | 同时更新多个合并请求的属性 |
| [Cherry-pick 变更](/docs/user/project/merge-request/cherry-pick.md) | 只需在合并的合并请求或提交中单击**Cherry-pick**按钮，即可在页面中 Cherry-pick 任何**选择** |
| [快进合并](/docs/user/project/merge-request/fast-forward.md) | 有关线性 Git 历史记录以及接受合并请求而不创建合并提交的方法 |
| [合并请求版本](/docs/user/project/merge-request/versions.md) | 选择并比较合并请求差异的不同版本 |
| [解决冲突](/docs/user/project/merge-request/resolve-conflicts.md) |可以在界面中来解决某些合并请求冲突 |
| [Revert 更改](/docs/user/project/merge-request/revert.md) | 从合并请求中的任何提交还原更改 |

## Tips[](#tips "Permalink")

以下是一些可帮助您在命令行中更有效地处理合并请求的 Tips：

### 本地合并合并请求[](#checkout-merge-requests-locally "Permalink")

合并请求包含来自代码仓库的所有历史记录，以及添加到与合并请求关联的分支的其他提交。以下是一些在本地检出合并请求的技巧。

请注意，即使源项目是目标项目的分支（甚至是私有分支），也可以在本地签出合并请求。

#### 通过别名设置签出合并请求[](#checkout-locally-by-adding-a-git-alias "Permalink")

将以下别名添加到`~/.gitconfig` ：

```markdown
[alias]
    mr = !sh -c 'git fetch $1 merge-requests/$2/head:mr-$1-$2 && git checkout mr-$1-$2' - 
```

现在，您可以从任何代码仓库和任何远程签出特定的合并请求，例如，执行以下操作可以从`origin`远程服务器签出 ID 为 5 的合并请求请：

```markdown
git mr origin 5 
```

这会将合并请求提取到本地`mr-origin-5`分支中，并检出它。

#### 通过在 config 文件中添加代码仓库签出[](#checkout-locally-by-modifying-gitconfig-for-a-given-repository "Permalink")

在`.git/config`文件中找到适用于 remote 的部分，找到类似下面的这段配置：

```markdown
[remote "origin"]
  url = https://codechina.csdn.net/codechina/awsome-project.git
  fetch = +refs/heads/*:refs/remotes/origin/* 
```

您可以使用以下方式打开文件：

```markdown
git config -e 
```

现在，将以下行添加到上面的部分：

```markdown
fetch = +refs/merge-requests/*/head:refs/remotes/origin/merge-requests/* 
```

最后，它应如下所示：

```markdown
[remote "origin"]
  url = https://codechina.csdn.net/codechina/awsome-project.git
  fetch = +refs/heads/*:refs/remotes/origin/*
  fetch = +refs/merge-requests/*/head:refs/remotes/origin/merge-requests/* 
```

现在，您可以获取所有合并请求：

```markdown
git fetch origin

...
From https://codechina.csdn.net/codechina/awsome-project.git
 * [new ref]         refs/merge-requests/1/head -> origin/merge-requests/1
 * [new ref]         refs/merge-requests/2/head -> origin/merge-requests/2
... 
```

并检查特定的合并请求：

```markdown
git checkout origin/merge-requests/1 
```

以上所有操作均可通过[`git-mr`](https://gitlab.com/glensc/git-mr)脚本完成。