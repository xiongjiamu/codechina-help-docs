# 讨论[](#讨论 "Permalink")

您可以在以下位置发表评论：

*   Issues
*   Epics
*   合并要求
*   提交
*   diff

除了标准的评论形式外，您还可以选择以话题讨论的方式创建评论， 收到回复后，评论也将是[话题讨论](#start-a-thread-by-replying-to-a-standard-comment) 的形式。

评论区域支持[Markdown](/docs/user/markdown.md)和[快速操作](/docs/user/project/quick-actions.md) ， 您可以随时编辑自己的评论，拥有" [maintainer"](/docs/user/permissions.md)或更高权限的用户也可以编辑其他人的评论。

您还可以通过回复评论通知电子邮件来回复评论，回复标准评论会创建另一个标准评论。回复主题评论会在主题中创建回复，电子邮件回复支持[Markdown](/docs/user/markdown.md)和[快速操作](/docs/user/project/quick-actions.md)。

**注意：**每个对象最多只能有 5,000 条评论，例如：issue，epic 及合并请求。

## 可解决的评论及讨论[](#resolvable-comments-and-threads "Permalink")

讨论有助于跟踪计划和代码审查的进度。

合并请求，提交，提交差异和代码片中的每个评论或讨论初始状态都显示为未解决，具有Developer及以上权限的任何人或所检查的更改的作者都可以单独解决这些问题。即使该讨论已解决，如果非成员没有解决他们自己的响应，讨论也不会标记为解决；如果非成员解决了相同的答复，则讨论会被标记为已解决。

解决所有评论或讨论可以防止您忘记处理反馈，并可以隐藏不再相关的线程。

### 在合并请求的上下文中发起讨论[](#commit-threads-in-the-context-of-a-merge-request "Permalink")

对于具有基于提交的工作流的审阅者，在合并请求的上下文中将讨论添加到特定的提交差异上可能很有用。 在以下情况下，这些讨论将通过提交ID更改来保持不变：

*   Rebase后强行提交代码
*   修改提交的评论

可以按照以下步骤创建提交差异讨论：

1.  导航到合并请求的" **提交"**选项卡,将显示构成合并请求的提交列表

2.  进入选定的提交，单击" **更改"**选项卡（在该选项卡中，将仅显示与所选提交不同的内容），并提交评论

    [![Commit diff discussion in merge request context](/docs/img/commit_comment_mr_context.png)](/docs/img/commit_comment_mr_context.png)

3.  以这种方式创建的任何讨论都将显示在合并请求的"**讨论"**选项卡中，并且可以解决

以这种方式创建的线程将仅出现在原始合并请求中，而不是在项目的" **代码">"提交"**页面下的**提交**中。

**提示：**在合并请求内的讨论中引用的提交的链接时，它将在当前合并请求的上下文中自动转换为链接。

### 解决话题跳转[](#jumping-between-unresolved-threads "Permalink")

当合并请求中包含大量评论时，可能很难跟踪未解决的评论。 您可以使用讨论上"回复"字段旁边的"跳转"按钮在未解决的讨论之间快速跳转。

您还可以使用快捷键在讨论之间导航：

*   使用`n`跳到下一个未解决的线程.
*   使用`p`跳到上一个未解决的线程.

### 将评论或讨论标记为已解决[](#marking-a-comment-or-thread-as-resolved "Permalink")

您可以通过单击**讨论**底部的" **解决讨论"**按钮将其标记为已解决。

[!["Resolve thread" button](/docs/img/resolve_thread_button.png)](/docs/img/resolve_thread_button.png)

或者，您可以将每个评论单独标记为已解决。

[!["Resolve comment" button](/docs/img/resolve_comment_button.png)](/docs/img/resolve_comment_button.png)

### 在合并请求中所有未解决讨论转为 Issue[](#move-all-unresolved-threads-in-a-merge-request-to-an-issue "Permalink")

要在新 Issue 中解决当前自合并请求中的所有未解决的讨论时，可以单击" **再新问题中解决所有讨论"**的按钮。

[![Open new issue for all unresolved threads](/docs/img/btn_new_issue_for_all_threads.png)](/docs/img/btn_new_issue_for_all_threads.png)

或者，当您的项目仅[在解决所有讨论](#only-allow-merge-requests-to-be-merged-if-all-threads-are-resolved)后才接受合并请求[时](#only-allow-merge-requests-to-be-merged-if-all-threads-are-resolved) ，在合并请求部件中会有一个创建一个新 Issue 以便稍后解决的选项。

### 将单个讨论转变成 Issue[](#moving-a-single-thread-to-a-new-issue "Permalink")

要从单个讨论创建新 Issue时，可以使用" **在新问题中解决此讨论"**按钮。

您将会跳转到预填充了讨论内容的新 Issue，类似于为一次委派多个讨论而创建的 Issue。创建 Issue 将把该讨论标记为已解决，并在合并请求讨论中添加引用新 Issue 的评论。


### 只有全部讨论内容解决后才允许合并[](#only-allow-merge-requests-to-be-merged-if-all-threads-are-resolved "Permalink")

在解决所有讨论之前，将不允许合并合并请求。

要使该设置生效，需要进入项目的设置页面，选中" **仅在解决所有讨论后才允许合并请求"**复选框，然后单击" **保存"**即可。

从现在开始，直到所有讨论解决后，您才能从网页上进行合并操作。

### Automatically resolve merge request diff threads when they become outdated[](#automatically-resolve-merge-request-diff-threads-when-they-become-outdated "Permalink")

在 GitLab 10.0 中[引入](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/14053) .

您可以在使用新的推送修改的行上自动解决合并请求差异线程.

导航到您的项目的设置页面，选中" **使用推送更改的行上**的**自动解析合并请求差异线程"**复选框，然后单击" **保存"**以使更改生效.

[![Automatically resolve merge request diff threads when they become outdated](/docs/img/a283d966822ac6a760d1a650273fbb3b.png)](/docs/img/automatically_resolve_outdated_discussions.png)

从现在开始，如果推送使 diff 部分过时，默认情况下将解决 diff 上的所有线程. 不变的线上线程和顶级可解析线程不会自动解析.

## 提交的讨论[](#commit-threads "Permalink")

您可以在项目的**代码> 提交**下向特定提交添加评论和讨论。

**注意：**如果在强制推送后更改了提交 ID，则以这种方式创建的讨论将丢失。

## 讨论的讨论[](#threaded-discussions "Permalink")

虽然可解决的讨论仅适用于合并请求的文件diff，但也可以添加与文件diff无关的讨论， 您可以针对 Issue，提交，摘要及合并请求添加一个看起来像讨论的特定讨论。

要开始讨论，请单击" **评论"**按钮切换下拉列表，选择" **开始讨论"，**并在准备发布评论时单击" **开始讨论** "按钮。

这将以单个讨论的形式发起评论，使您可以更大的范围进行特定的讨论。

## 图片的讨论[](#image-threads "Permalink")

有时讨论会围绕图片展开。使用图片讨论，您可以轻松地定位图像的特定坐标并在其周围开启讨论。图片讨论在合并请求详情和提交的详情页面中可用。

要启动图片讨论，请将鼠标悬停在图片上。当您的鼠标指针转换为图标时，表示该图片可用于讨论，此时只需单击图片上的任意位置以创建新的讨论即可。

单击图片后，将显示新建评论输入框，保存评论后，您会在图像顶部看到一个新的徽章，此徽章代表您的讨论。

## 锁定讨论[](#lock-discussions "Permalink")

对于有较多贡献者参与的大型项目，在以下场景中禁用讨论将会非常地有帮助：

*   项目维护者已经解决了该问题，无需更多的后续反馈
*   项目维护者已经将新讨论指向了新的 Issue 或合并请求
*   参与讨论者的讨论内容比较随意、辱骂或是无益的产品建议

在这些情况下，项目中具有开发者权限或更高权限的用户可以使用边栏中的"锁定"按钮来锁定/解锁 问题或合并请求. 对于问题，具有记者权限的用户可以锁定/解锁。

在锁定的问题或合并请求中，只有团队成员才能添加新评论和编辑现有评论，非团队成员无法添加或编辑评论。

## 合并请求评审[](#merge-request-reviews "Permalink")

查看"合并请求"差异时，您可以开始审阅，您可以在"合并请求"中创建**仅**在发布之前才对**您可见的**评论，以便您可以将所有评论作为单个操作提交。

### 开始评审[](#starting-a-review "Permalink")

为了开始审阅，只需像往常一样在合并请求的" **更改"**选项卡下对差异添加评论，然后单击" **开始审阅"**按钮。

当开始审阅后，审阅内容部分中所有的评论都会被标记为`Pending`，同时所有审阅中的评论都会显示两个按钮：

*   **完成审阅** ：提交**审阅中的**所有评论，使其他用户可以看到它们
*   **立即添加评论** ：提交常规评论，而不是审阅的一部分

您可以在评论中使用[快速操作](/docs/user/project/quick-actions.md) ，评论也将会显示提交评论后即将执行的操作。

要向评论添加更多评论，请照常开始写评论，然后单击**添加到评论**按钮，这会将评论添加到评论中。
