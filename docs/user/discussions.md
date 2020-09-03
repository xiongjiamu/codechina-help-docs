# 讨论[](#讨论 "Permalink")

您可以在以下位置发表评论：

*   Issues
*   Epics
*   合并要求
*   提交
*   diff

除了标准的评论形式外，您还可以选择以话题讨论的方式创建评论， 收到回复后，评论也将是[话题讨论](#start-a-thread-by-replying-to-a-standard-comment) 的形式。

评论区域支持[Markdown](../markdown.html)和[快速操作](../project/quick_actions.html) ， 您可以随时编辑自己的评论，拥有" [maintainer"](../permissions.html)或更高[权限的](../permissions.html)用户也可以编辑其他人的评论。

您还可以通过回复评论通知电子邮件来回复评论，回复标准评论会创建另一个标准评论。回复主题评论会在主题中创建回复，电子邮件回复支持[Markdown](../markdown.html)和[快速操作](../project/quick_actions.html)。

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

    [![Commit diff discussion in merge request context](/../../docs/img/commit_comment_mr_context.png)](img/commit_comment_mr_context.png)

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

[!["Resolve thread" button](/../../docs/img/resolve_thread_button.png)](img/resolve_thread_button.png)

或者，您可以将每个评论单独标记为已解决。

[!["Resolve comment" button](/../../docs/img/resolve_comment_button.png)](img/resolve_comment_button.png)

### 在合并请求中所有未解决讨论转为 Issue[](#move-all-unresolved-threads-in-a-merge-request-to-an-issue "Permalink")

要在新 Issue 中解决当前自合并请求中的所有未解决的讨论时，可以单击" **再新问题中解决所有讨论"**的按钮。

[![Open new issue for all unresolved threads](/../../docs/img/btn_new_issue_for_all_threads.png)](img/btn_new_issue_for_all_threads.png)

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

[![Automatically resolve merge request diff threads when they become outdated](img/a283d966822ac6a760d1a650273fbb3b.png)](img/automatically_resolve_outdated_discussions.png)

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

您可以在评论中使用[快速操作](../project/quick_actions.html) ， 评论也将会显示提交评论后即将执行的操作。

要向评论添加更多评论，请照常开始写评论，然后单击**添加到评论**按钮，这会将评论添加到评论中。

### 提交评审[](#submitting-a-review "Permalink")

If you have any comments that have not been submitted, you will see a bar at the bottom of the screen with two buttons:

*   **舍弃** ： **舍弃**所有尚未提交的评论.
*   **完成审阅** ：打开准备提交审阅的评论列表. 单击**提交评论**将发布所有评论. 此时将执行所有提交的快速操作.

另外，要通过待审核的评论完成整个审核，请执行以下操作：

*   单击**评论**上的" **完成审阅"**按钮.
*   在非评论注释的文本中使用`/submit_review` [快速操作](../project/quick_actions.html) .

[![Review submission](img/c6daa1e81d653cfd0b476144f1f71874.png)](img/review_preview.png)

提交审阅将向合并请求的每个应通知用户发送一封电子邮件，其中包含与之相关的所有注释.

因此，回复此电子邮件将在关联的合并请求上创建一个新注释.

## Filtering notes[](#filtering-notes "Permalink")

在 GitLab 11.5 中[引入](https://gitlab.com/gitlab-org/gitlab-foss/-/issues/26723) .

对于活动注释和用户注释等具有许多注释的问题，有时很难找到有用的信息. 有一种方法可以针对合并请求和问题从单个注释和线程中过滤注释.

从合并请求的" **讨论"**选项卡，或史诗/问题概述中，找到页面右侧的过滤器下拉菜单，您可以从中选择以下选项之一：

*   **显示所有活动** ：显示所有用户评论和系统注释（问题更新，对其他问题的提及，对描述的更改等）.
*   **仅显示评论** ：仅在列表中显示用户评论.
*   **仅显示历史记录** ：仅显示活动记录.

[![Notes filters dropdown options](img/5a26f77375b52645c2387aec1f77a777.png)](img/index_notes_filters.png)

在给定问题或 MR 中选择过滤器之一后，GitLab 将保存您的首选项，这样当您从已登录的任何设备再次访问同一页面时，该首选项将保持不变.

## Suggest Changes[](#suggest-changes "Permalink")

在 GitLab 11.6 中[引入](https://gitlab.com/gitlab-org/gitlab-foss/-/issues/18008) .

作为审阅者，您可以在 Merge Request Diff 线程中使用简单的 Markdown 语法建议代码更改. 然后，合并请求作者（或具有适当[权限的](../permissions.html)其他用户）能够通过单击来应用这些建议，这将在应用了这些建议的用户创作的合并请求中生成提交.

1.  选择要更改的代码行，添加新注释，然后单击工具栏中的" **插入建议"**图标：

    [![Add a new comment](img/d7cb226977bb46d9aaa1c1d7e195025a.png)](img/suggestion_button_v12_7.png)

2.  在注释中，将您的建议添加到预填充的代码块中：

    [![Add a suggestion into a code block tagged properly](img/44cad341f814ae94da18480c3dc1d2be.png)](img/make_suggestion_v12_7.png)

3.  单击**开始审查**或**加入审查** ，以您的评论添加到[审查](#merge-request-reviews) ，或者**现在添加注释** ，注释立即加入到线程.

    注释中的"建议"可由合并请求作者直接从合并请求中应用：

    [![Apply suggestions](img/0dd0fc53dcaa34b76a16be18538c1a35.png)](img/apply_suggestion_v12_7.png)

一旦作者应用了一个建议，它将被标记为"已**应用"**标签，该线程将被自动解析，并且 GitLab 将创建一个新的提交，并将建议的更改直接推送到合并请求分支中的代码库中. 这样做需要[开发人员许可](../permissions.html) .

### Multi-line Suggestions[](#multi-line-suggestions "Permalink")

在 GitLab 11.10 中[引入](https://gitlab.com/gitlab-org/gitlab-foss/-/issues/53310) .

审阅者还可以通过调整范围偏移，在合并请求差异线程中使用单个"建议"来建议对多行进行更改. 偏移量相对于 diff 线程的位置，并指定应用建议时要被建议替换的范围.

[![Multi-line suggestion syntax](img/317167b85f9604b741e71e57b1702b6c.png)](img/multi-line-suggestion-syntax.png)

在上面的示例中，建议涵盖了注释行上方的三行和注释行下方的四行. 应用时，它将用建议的更改从注释行*上方的* 3 行替换为注释行*下方*的 4 行.

[![Multi-line suggestion preview](img/590715bab1c8704d5a4c16437c011ed5.png)](img/multi-line-suggestion-preview.png)

**注意：**涵盖多行的建议仅限于已注释差异行*上方的* 100 行和*下方*的差异行*下方*的 100 行，每个建议最多可更改 200 行.

### Code block nested in Suggestions[](#code-block-nested-in-suggestions "Permalink")

如果您需要提出涉及[受限制的代码块](../markdown.html#code-spans-and-blocks)的建议，请将您的建议换成四个反引号，而不是通常的三个.

[![A comment editor with a suggestion with a fenced code block](img/a4e7c4f55411323814dd3b9cb30ab9f8.png)](img/suggestion_code_block_editor_v12_8.png)

[![Output of a comment with a suggestion with a fenced code block](img/db0182b2e43670178e35b1a3485ca25e.png)](img/suggestion_code_block_output_v12_8.png)

### Configure the commit message for applied Suggestions[](#configure-the-commit-message-for-applied-suggestions "Permalink")

在 GitLab 12.7 中[引入](https://gitlab.com/gitlab-org/gitlab/-/issues/13086) .

GitLab 在应用建议时使用默认的提交消息： `Apply %{suggestions_count} suggestion(s) to %{files_count} file(s)`

例如，假设用户将 3 条建议应用于 2 个不同的文件，则默认的提交消息将是： **将 3 条建议应用于 2 个文件**

可以自定义这些提交消息，以遵循您可能拥有的任何准则. 为此， **请**在项目的" **常规"**设置中展开" **合并请求"**选项卡，然后更改" **合并建议"**文本：

[![Custom commit message for applied Suggestions](img/182928c540d17ccf275438850fc7592d.png)](img/suggestions_custom_commit_messages_v13_1.jpg)

除了静态文本，您还可以使用以下变量：

| Variable | Description | 输出示例 |
| --- | --- | --- |
| `%{branch_name}` | 建议所应用到的分支的名称. | `my-feature-branch` |
| `%{files_count}` | 应用了建议的文件数. | **2** |
| `%{file_paths}` | 应用了建议文件的路径. 路径用逗号分隔. | `docs/index.md, docs/about.md` |
| `%{project_path}` | 项目路径. | `my-group/my-project` |
| `%{project_name}` | 项目的可读名称. | **我的项目** |
| `%{suggestions_count}` | 应用的建议数. | **3** |
| `%{username}` | 应用建议的用户的用户名. | `user_1` |
| `%{user_full_name}` | 应用建议的用户的全名. | **用户 1** |

例如，要自定义提交消息以输出**Addresses user_1 的评论** ，请将自定义文本设置为`Addresses %{username}'s review` .

**注意：** [＃25381](https://gitlab.com/gitlab-org/gitlab/-/issues/25381)将为每个应用的建议（以及批量建议）引入自定义提交消息.

### Batch Suggestions[](#batch-suggestions "Permalink")

版本历史

*   在 GitLab 13.1 中作为[Alpha 功能](https://about.gitlab.com/handbook/product/#alpha) [引入](https://gitlab.com/gitlab-org/gitlab/-/issues/25486) .
*   它部署在功能标记后面，默认情况下处于禁用状态.
*   在 GitLab.com 上已禁用.
*   要在 GitLab 自管实例中使用它，请让 GitLab 管理员[启用它](#enable-or-disable-batch-suggestions) .

您可以一次应用多个建议，以减少为满足审阅者的请求而添加到分支的提交数量.

1.  要启动将在一次提交中应用的一批建议，请单击" **将建议添加到批处理"** ：

    [![A code change suggestion displayed, with the button to add the suggestion to a batch highlighted.](img/f12701028e6548c505318ef2d4e378db.png "Add a suggestion to a batch")](img/add_first_suggestion_to_batch_v13_1.jpg)

2.  根据需要向批处理中添加尽可能多的其他建议：

    [![A code change suggestion displayed, with the button to add an additional suggestion to a batch highlighted.](img/f60803ec89d6ae84310e181507eb2ad8.png "Add another suggestion to a batch")](img/add_another_suggestion_to_batch_v13_1.jpg)

3.  要删除建议，请单击" **从批处理中删除"** ：

    [![A code change suggestion displayed, with the button to remove that suggestion from its batch highlighted.](img/e28a69b4996ee400ca3df4431df0ab13.png "Remove a suggestion from a batch")](img/remove_suggestion_from_batch_v13_1.jpg)

4.  将所有建议添加到您的喜好中后，准备好后，请点击**应用建议** ：

    [![A code change suggestion displayed, with the button to apply the batch of suggestions highlighted.](img/ed8bdb5d349320bc1d470f096578dfe7.png "Apply a batch of suggestions")](img/apply_batch_of_suggestions_v13_1.jpg)

#### Enable or disable Batch Suggestions[](#enable-or-disable-batch-suggestions "Permalink")

批处理建议部署在**默认情况下禁用**的功能标志的后面. [有权访问 GitLab Rails 控制台的 GitLab 管理员](../../administration/feature_flags.html)可以为您的实例启用它.

要启用它：

```
# Instance-wide
Feature.enable(:batch_suggestions) 
```

禁用它：

```
# Instance-wide
Feature.disable(:batch_suggestions) 
```

## Start a thread by replying to a standard comment[](#start-a-thread-by-replying-to-a-standard-comment "Permalink")

在 GitLab 11.9 中[引入](https://gitlab.com/gitlab-org/gitlab-foss/-/issues/30299)

要回复标准（非线程）评论，可以使用" **回复评论"**按钮.

[![Reply to comment button](img/d198d958fcf8be60727c232ff69b9713.png)](img/reply_to_comment_button.png)

仅当您有权回复现有主题或从标准评论启动主题时，才会显示" **回复评论"**按钮.

单击" **回复评论"**按钮将使回复区域成为焦点，您可以键入回复.

[![Reply to comment feature](img/9f29552692cfb04d323dc62cc4bc1d1e.png)](img/reply_to_comment.gif)

提交回复后，回复非线程注释将把非线程注释转换为线程. 该转换被认为是对原始评论的修改，因此在其下方会出现一条有关上次编辑时间的注释.

此功能仅适用于"问题"，"合并请求"和"事件". 尚不支持提交，摘要和合并请求差异线程.

## Assign an issue to the commenting user[](#assign-an-issue-to-the-commenting-user "Permalink")

在 GitLab 13.1 中[引入](https://gitlab.com/gitlab-org/gitlab/-/issues/191455) .

您可以将问题分配给发表评论的用户.

在评论中，单击" **更多操作"**菜单，然后单击" **分配给评论用户"** .

再次单击按钮以取消分配评论者.

[![Assign to commenting user](img/9b6a8d0d96113fcaadd766cecfbecdbc.png)](img/quickly_assign_commenter_v13_1.png)