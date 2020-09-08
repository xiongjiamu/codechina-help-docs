# 操作Issue[](#操作Issue "Permalink")

请参考[ Issue 文档](/docs/user/project/issues.md)以了解更多关于 Issue 的介绍。

## Issue的元素[](#parts-of-an-issue "Permalink")

下图说明了问题的构成，请注意，根据查看问题的用户权限不同，某些部分看起来可能会略有不同或不存在。

您可以在一个屏幕上找到该 Issue 的所有信息。

[![Issue view](/docs/img/issues_main_view_numbered.png)](/docs/img/issues_main_view_numbered.png)

*   **1.** [新建 Issue, 关闭 issue (重新开启 issue, 报告 issue)](#new-issue-close-issue-reopen-issue-report-issue)
*   **2.** [新建待办事项](#to-do)
*   **3.** [指派](#assignee)
*   **4.** [里程碑](#milestone)
*   **5.** [工时统计](#time-tracking)
*   **6.** [截止日期](#due-date)
*   **7.** [标签](#labels)
*   **8.** [机密性](#confidentiality)
*   **9.** [锁定 Issue](#lock-issue)
*   **10.** [参与者](#participants)
*   **11.** [通知](#notifications)
*   **12.** [移动 Issue](#reference)
*   **13.** [编辑 Issue](#edit)
*   **14.** [Issue 描述](#description)
*   **15.** [相关合并请求](#related-merge-requests)
*   **16.** [点赞](#award-emoji)
*   **17.** [查看全部活动](#show-all-activity)
*   **18.** [创建合并请求](#create-merge-request)
*   **19.** [Issue 历史](#issue-history)
*   **20.** [评论](#comments)
*   **21.** [提交评论，开启新的讨论，关闭 Issue](#submit-comment-start-a-thread-or-comment-and-close)

Issue 从状态（打开或关闭）开始，然后是作者，并包括许多其他功能，在上图中编号，下面将逐一进行解释。

当 Issue 由其他用户更改时，Issue 页面的许多元素都会自动刷新，例如标题和说明。评论和系统评论也会根据各种操作和内容更新自动更新。

### 新建 Issue, 关闭 issue (重新开启 issue, 报告 issue)[](#new-issue-close-issue-reopen-issue-report-issue "Permalink")

单击" **新建 Issue"**将打开一个新窗口，可以在同一项目中创建一个新 Issue。单击**关闭 Issue**将关闭此 Issue，但不会被删除。如果 Issue 已经关闭，您仍然可以访问它，并且按钮将显示**重新开启 issue** ，您可以单击以重新打开 Issue，重新开放的 Issue 与其他任何 Issue 都没有不同。

如果您无权修改 Issue，则" **关闭 Issue"**按钮将替换为" **举报 Issue"** ，您可以单击该按钮以[提交](/docs/user/abuse.md)有关该 Issue [的滥用情况报告](/docs/user/abuse.md)； 如果您有权修改 Issue，但仅在关闭 Issue后，它也会显示.

### 待办事项[](#to-do "Permalink")

您可以在[待办事项列表](/docs/user/todo.md)添加待办事项或从中删除待办事项。具体可以执行的操作取决于待办事项是否已在"任务列表"中，如果问题是：

*   已在您的待办事项清单上：该按钮标有" **标记为已完成"** ，单击按钮以从您的任务列表中删除该问题
*   不在您的待办事项清单上：该按钮标有**添加待办事项** ，单击按钮将问题添加到您的"任务列表"中

### 指派[](#assignee "Permalink")

可以将问题分配给：

*   您自己
*   其他用户

可以根据需要频繁更改指派人，指派人应对该 Issue 负责，直到将其重新分配给其他人至解决该 Issue 为止。分配给某人后，Issue 将显示在其分配的 Issue 列表中。

**提示：**如果用户不是该项目的成员，则只有他们自己创建的 Issue 才能够分配给他们。

### 里程碑[](#milestone "Permalink")

选择一个[里程碑](/docs/user/project/milestone.md) ，并将 Issue 归类到其中。

### 工时统计[](#time-tracking "Permalink")

使用[快速行动](/docs/user/project/quick-actions.md)来[跟踪估计和花费在 Issue 上的时间](/docs/user/project/time-track.md) ，您可以添加解决 Issue [所需时间](/docs/user/project/time-track.md#estimates)的[估计](/docs/user/project/time-track.md#estimates)，还可以添加解决 Issue[所花费的时间](/docs/user/project/time-track.md#time-spent) 。

### 截止日期[](#due-date "Permalink")

当您的工作时间很紧时，有一种方法来为实现和解决 Issue 设置截止日期将尤为重要。这可以在[截止日期](/docs/user/project/issues/due-date.md)元素中完成，截止日期可以根据需要进行多次更改。

### 标签[](#labels "Permalink")

通过给 Issue 加上[标签](/docs/user/project/label.md)来对其进行分类，它们有助于组织工作流程，并使您能够更顺畅的使用看板。

还可以为组织标签分配 Issue ，组织标签允许您对同一组内的所有项目使用相同的标签，它们的工作原理完全相同，并且可立即用于该组织的所有项目。

**提示：**如果标签尚不存在，可以单击**编辑** ，它会打开一个下拉菜单，从中可以选择**创建新标签** 。

### 机密性[](#confidentiality "Permalink")

您可以[将 Issue 设置为机密](/docs/user/project/issues/confidential.md)， 设置后，未经授权的用户将无法访问该 Issue，也不会在项目看板或 Issue 列表中看到该 Issue。

### 锁定 Issue[](#lock-issue "Permalink")

您可以[锁定 Issue 中的讨论](/docs/user/discussions.md) ，以防止添加更多评论。

### 参与者[](#participants "Permalink")

涉及该 Issue 的所有用户，他们要么参与了该 Issue 的[讨论](/docs/user/discussions.md) ，要么在描述或讨论中被提及。

### 通知[](#notifications "Permalink")

单击图标以启用/禁用该 Issue 的[通知](/docs/user/account/email-notify.md#issue--epics--merge-request-events) ，如果您以任何方式参与了该 Issue，它将自动启用。

*   **启用**: 如果您不是该 Issue 的参与者，但想要了解该 Issue 的进展，您可以启用并订阅该 Issue 的更新通知
*   **禁用** ：如果您正在接收有关该 Issue 的更新通知，但不再希望接收它们，请禁用该通知

### 编辑[](#edit "Permalink")

单击此图标可编辑当前 Issue ，您将有权访问与创建 Issue 时的全部字段，如果用户没有编辑 Issue 的权限，则不会显示此图标。

### 描述[](#description "Permalink")

纯文本标题和 Issue 描述位于 Issue 页面的顶部，该描述完全支持[Markdown](/docs/user/markdown.md#gitlab-flavored-markdown-gfm) ，支持许多格式。问题历史记录中列出了对 Issue 描述的更改记录。

### 提及[](#mentions "Permalink")

您可以使用`@username`或`@groupname`提及用户或组织，除非他们设置禁用了所有通知，否则它们将通过待办事项和电子邮件得到通知，这是在通知设置中控制的。

自己的提及（当前登录的用户）将以不同的颜色突出显示，使您可以轻松查看涉及到的评论，帮助您快速关注它们。

**提示：**避免在问题中提及`@all`并合并请求，因为它会向该项目组的所有成员发送电子邮件通知，产生垃圾邮件。

### 相关的合并请求[](#related-merge-requests "Permalink")

该 Issue 的描述或 Issue 讨论中提到的[合并请求](/docs/user/project/issues/crosslinking.md#from-merge-requests)在此处列为[相关合并请求](/docs/user/project/issues/crosslinking.md#from-merge-requests) ，另外，如果当前 Issue 在另一个合并请求中被提及，则该合并请求也将在此处列出。

### 点赞[](#award-emoji "Permalink")

您可以为该 Issue 点赞， 有"顶"和"踩"两种快捷方式，或者您可以单击浅灰色的"笑脸"图标并从可用的[Markdown Emoji](/docs/user/markdown.md#emoji)下拉列表中选择其他表情。

**提示：在讨论中**发布"+1"作为评论会对该 Issue 的所有参与/订阅者造成垃圾邮件，也会使讨论内容显得混乱，因此不建议这样做.。给 Issue 点赞是一种让他们知道您的反应而不会发送垃圾邮件的方法，我们更建议您使用这种方式。

### 显示所有活动[](#show-all-activity "Permalink")

您可以通过单击**显示所有活动**并选择以下任一内容来过滤 Issue 历史记录中**显示的内容** ：

*   **仅显示评论** ，仅显示讨论并隐藏 Issue 的更新
*   **仅显示历史记录** ，仅显示更新并隐藏讨论

此外:

*   您可以使用`@username`或`@groupname`提及用户或组，除非他们已[禁用](#notifications)其配置文件设置中的[所有通知](#notifications) ，否则它们将通过待办事项和电子邮件得到[通知](#notifications) 
*   自己的提及（当前登录的用户）将以不同的颜色突出显示，使您可以轻松查看涉及到的评论，帮助您快速关注它们。

### 创建合并请求[](#create-merge-request "Permalink")

通过一个操作同时完成创建一个新的分支和**草稿**合并请求， 默认情况下，该分支将被命名为`issuenumber-title` ，但是您可以选择任何名称，并且系统会验证该分支是否已经被使用。创建的合并请求将自动继承 Issue 的里程碑和标签，并设置为在合并时自动关闭 Issue 。

（可选）您可以选择仅创建一个[新分支](/docs/user/project/repo/web-editor.md#create-a-new-branch-from-an-issue) ，并以该 Issue 命名。

### Issue 历史记录[](#issue-history "Permalink")

所有向该 Issue 提交的评论和更新都会被列出在 Issue 历史记录中，如上面介绍的，可以通过过滤条件筛选 Issue 历史记录。

#### 动态排序[](#activity-sort-order "Permalink")

您可以颠倒 Issue 动态的默认顺序，上方的 Issue 动态将按照您的选择排序。您的排序方式将通过本地存储保存，并自动应用于您查看的每一个 Issue 。

要更改 Issue 动态排序顺序，请单击**按时间倒叙**下拉菜单，然后选择最旧或最新的优先显示。

### 评论[](#comments "Permalink")

通过在讨论中发布评论来协作解决 Issue ，评论框将完全支持Markdown。

### 提交评论，开启新的讨论，关闭 Issue[](#submit-comment-start-a-thread-or-comment-and-close "Permalink")

撰写评论后，您可以：

*   单击**评论** ，您的评论将被发布
*   选择从下拉列表中**启动新的讨论** ，并在当前 Issue 的主讨论中启动一个新的[讨论]来讨论更具体的点，可邀请其他参与者直接回复您的讨论，并将相关评论分组在一起。

您也可以从此处关闭 Issue ，无需滚动到 Issue 页面的顶部再关闭 Issue。