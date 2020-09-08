# 创建合并请求[](#创建合并请求 "Permalink")

每个合并请求都从创建一个分支开始，您可以通过[命令行](#new-merge-request-from-your-local-environment) ，Git CLI 应用程序或[CODEChina WEB](#new-merge-request-from-a-new-branch-created-through-the-ui)完成分支的创建。

本文档介绍了创建合并请求的几种方法。

启动新的合并请求时，无论使用哪种方法，都将转到[**新合并请求**](#new-merge-request-page)页面，并在其中添加合并请求相关的信息。

如果将新分支推送到 CODEChina，不论使用哪种方法，都可以单击[**创建合并请求**](#create-merge-request-button)按钮并从此处启动合并请求。

## 新建合并请求[](#new-merge-request-page "Permalink")

在" **新合并请求"**页面上，首先填写**合并请求**的标题和描述，如果分支上已经有提交，则标题将用第一条提交消息的第一行预填充，描述将用提交消息中的任何其他行预填充。在所有情况下，标题都是唯一的必填字段。

在此处，您可以在其中填充信息（标题，描述，指派人，里程碑，标签，批准人），然后点击**创建合并请求** 。

在初始屏幕上，您还可以查看提交合并请求之前推送到分支的所有提交，管道和文件更改。

**提示：**您可以在创建合并请求之前将一次或多次推送到 CODEChina 中的分支。

## 创建合并请求按钮[](#create-merge-request-button "Permalink")

将新分支推送到 CODEChina 后，请访问 CODEChina 中的代码仓库，并在屏幕顶​​部看到一个提示，您可以从中单击**创建合并请求**按钮。

您还可以在以下页面的右上方看到" **创建合并请求"**按钮：

*   项目页
*   **代码>文件** 页
*   **合并请求** 页

这种情况下，系统将使用您将更改推送到的最新分支作为源分支，并将当前项目中的默认分支用作目标分支。

## 通过添加、编辑和上传文件来新建合并请求[](#new-merge-request-by-adding-editing-and-uploading-a-file "Permalink")

当您选择通过在界面上 编辑，添加或上传文件，在文件末尾，您会看到以下选项：添加**提交消息** ，选择该**提交**的**目标分支** ，然后选中**开始新建**复选框， **具有这些更改的合并请求** 。

同样，如果通过 Web IDE 更改文件，则在左侧边栏中导航到" **提交"**时，将看到这些相同的选项。

添加，编辑或上传文件后，请执行以下操作：

1.  在提交消息中描述您的更改
2.  选择一个现有分支以将您的提交添加到其中，或者，如果您想创建一个新分支，请键入新的分支名称（不带空格，大写字母或特殊字符）
3.  保持选中复选框以立即开始新的合并请求，或者取消选中该复选框以在开始合并请求之前向该分支添加更多更改
4.  单击 **提交变更**

如果您选择开始合并请求，则将转到" [**新合并请求"**页面](#new-merge-request-page) ，您可以在其中填写信息并提交合并请求。

合并请求将针对存储库的默认分支，如果要更改它，可以稍后通过编辑合并请求来进行更改。

## 来自新建分支的合并请求[](#new-merge-request-from-a-new-branch-created-through-the-ui "Permalink")

要通过界面快速开始处理文件，请导航至项目的" **代码">"分支"** ，然后单击" **新建分支"** ，将创建一个新分支，您可以开始编辑文件。

提交并推送后，您可以单击" [**创建合并请求"**](#create-merge-request-button)按钮以打开" [**新合并请求"**页面](#new-merge-request-page)， 将使用当前分支作为源，并使用当前项目中的默认分支作为目标来启动新的合并请求。

## 从本地新建合并请求[](#new-merge-request-from-your-local-environment "Permalink")

假设您已将代码仓库克隆到计算机中，并且想要开始处理文件更改，请先创建并签出一个新分支：

```markdown
git checkout -b my-new-branch 
```

处理文件更改，暂存并提交它们：

```markdown
git add .
git commit -m "My commit message" 
```

完成后，将分支推送到 CODEChina ：

```markdown
git push origin my-new-branch 
```

在输出中，GitLab 将提示您一个直接链接来创建合并请求：

```markdown
...
remote: To create a merge request for docs-new-merge-request, visit:
remote:   https://codechina.csdn.net/my-group/my-project/merge_requests/new?merge_request%5Bsource_branch%5D=my-new-branch 
```

复制该链接并将其粘贴到浏览器中，将显示" [**新合并请求"页面**](#new-merge-request-page) .

在通过命令行推送时 ，还可以向命令添加一些标志，以减少通过界面手动编辑合并请求的需要。

如果您没有通过命令行将分支推送到 CODEChina（例如，您使用 Git CLI 应用程序来推送更改），则可以通过单击" [**创建合并请求"**](#create-merge-request-button)按钮 [**创建合并请求**](#create-merge-request-button) 。

## 从 Issue 新建合并请求[](#new-merge-request-from-an-issue "Permalink")

您也可以[直接从 issue 创建一个新的合并请求](/docs/user/project/repo/web-editor.md#create-a-new-branch-from-an-issue) 。

## 从合并请求列表页新建合并请求[](#new-merge-request-from-the-merge-requests-page "Permalink")

您可以通过在项目中的" **合并请求"**页面上单击" **新建合并请求"**按钮来开始创建新的合并请求，然后选择包含更改的源项目和分支，以及要将更改合并到的目标项目和分支。单击**比较分支，然后继续**转到" [**新合并请求"**页面](#new-merge-request-page)并填写详细信息。

## 从 Fork 项目新建合并请求[](#new-merge-request-from-a-fork "Permalink")

Fork 项目在本地更改后，可以通过以下步骤从 fork 创建一个合并请求以贡献回主项目：

1.  转到**项目>您的项目，**然后选择代码仓库的分支
2.  转到**合并请求** ，然后点击**新建合并请求** 
3.  在" **源分支"**下拉列表框中，在分支的存储库中选择您的分支作为源分支
4.  在" **目标分支"**下拉列表框中，从上游存储库中选择分支作为目标分支
5.  输入凭据后，单击" **比较分支"，然后继续**将本地更改与上游存储库进行比较
6.  分配用户以查看您的更改，然后点击**提交合并请求** 

合并更改后，您的更改将按照规范添加到上游存储库和分支中. 合并工作后，如果您不想对上游项目做出任何其他贡献，则可以通过[删除分支关系](/docs/user/project/settings.md#removing-a-fork-relationship) ，在**项目设置> 高级设置**部分[中将 fork 与](/docs/user/project/settings.md#removing-a-fork-relationship)上游项目断开链接。

### 将补丁添加为电子邮件附件[](#adding-patches-when-creating-a-merge-request-via-e-mail "Permalink")

您可以通过将补丁添加为电子邮件的附件，将提交添加到正在创建的合并请求中。文件名以`.patch`结尾的所有附件都将被视为补丁程序，并将按名称顺序对其进行处理。

补丁的总大小不超过 2MB。

如果主题的源分支不存在，那么将从存储库的 HEAD 或指定的目标分支创建源分支以应用补丁。可以使用[`/target_branch`快速操作](/docs/user/project/quick-actions.md)指定目标分支。如果源分支已经存在，则将在其顶部应用补丁。

## 审查和管理合并请求[](#reviewing-and-managing-merge-requests "Permalink")

提交合并请求后，可以通过 CODEChina 进行[审查和管理](/docs/user/project/merge-request/reviewing.md)。