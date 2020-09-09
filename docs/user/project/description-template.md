# 描述模板[](#description-template "Permalink")

我们都知道，项目开发人员更有可能及时解决提交的 Issue。使用描述模板，您可以为 Issue 定义特定的上下文的模板，并为项目合并请求描述字段，并帮助从 Issue 中过滤掉许多不必要的噪音。

## 概览[](#overview "Permalink")

通过使用描述模板，用户可以选择描述模板创建新的 Issue 或合并请求，以帮助他们与其他贡献者进行有效沟通。

每个项目都可以定义自己的一组描述模板，这些模板将被添加到项目代码仓库的根目录中。

描述模板必须用[Markdown](/docs/user/markdown.md)编写，并存储在项目的存储库中的`.gitlab`目录下，且仅考虑默认分支的模板。

## 示例[](#use-cases "Permalink")

*   添加一个模板，该模板将用于特定项目的每个 Issue，并提供说明和指南，要求提供特定于该主题的信息。例如，如果您有一个用于跟踪新博客文章的项目，则可以要求标题，大纲，作者姓名，作者社交媒体信息等等。
*   在前面的示例之后，您可以为随新博客帖子提交的每个合并请求创建模板，要求提供有关帖子日期，前事数据，图像准则，相关问题的链接，审阅者姓名等信息。
*   您还可以为工作流的不同阶段创建 Issue 及合并请求模板，例如功能建议，功能改进或错误报告等。

## 创建 Issue 描述模板[](#creating-issue-templates "Permalink")

在代码仓库的`.gitlab/issue_templates/`目录内创建一个新的 Markdown（ `.md` ）文件，提交并推送到您的默认分支。

可以通过以下步骤新建一个 markdown 文件:

1.  单击`master`旁边的`+`按钮，然后单击**新建文件**
2.  将 Issue 模板的名称添加到`master`旁边的**文件名称**文本字段中，确保单词之间用下划线分隔，并且文件的扩展名为`.md` ，例如`feature_request.md` 
3.  提交并推送到您的默认分支

如果您的存储库中没有`.gitlab/issue_templates`目录，则需要创建它。

可以通过以下步骤创建`.gitlab/issue_templates`目录：

1.  单击`master`旁边的`+`按钮，然后选择**新建目录**
2.  将此新目录`.gitlab`并提交到默认分支
3.  再次单击`master`旁边的`+`按钮，然后选择**新建目录**
4.  将新目录命名为`issue_templates`，并提交到默认分支

要检查它是否正常工作，请[创建一个新 Issue](/docs/user/project/issues/manage.md#create-a-new-issue)，然后查看是否可以选择描述模板。

## 创建合并请求描述模板[](#creating-merge-request-templates "Permalink")

与 Issue 模板类似，在代码仓库的`.gitlab/merge_request_templates/`目录内创建一个新的 Markdown（ `.md` ）文件. 提交并推送到您的默认分支。

## 使用模板[](#using-the-templates "Permalink")

假设我们已经创建了`.gitlab/issue_templates/Bug.md`文件，在创建或编辑问题时，这将启用`Bug`下拉选项，选择`Bug`，`Bug.md`模板文件中的内容将被复制到 Issue 描述字段；可以通过"重置模板"按钮放弃您在选择模板后所做的任何更改，并将其恢复为初始状态。

## 描述模板示例[](#description-template-example "Permalink")

GitLab 社区版项目中提供了一些 Issue 及合并请求的描述模板，具体的可以参考[`.gitlab`文件夹](https://gitlab.com/gitlab-org/gitlab/tree/master/.gitlab)中的一些示例。

**提示：**可以在描述模板中使用[快速操作](/docs/user/project/quick-actions.md)来快速添加标签，指派人和里程碑。仅当提交问题或合并请求的用户有权执行相关操作时，才可以执行快速操作。

以下是一个 bug 的模板示例：

```markdown
Summary

(Summarize the bug encountered concisely)

Steps to reproduce

(How one can reproduce the issue - this is very important)

Example Project

(If possible, please create an example project here on GitLab.com that exhibits the problematic behaviour, and link to it here in the bug report)

(If you are using an older version of GitLab, this will also determine whether the bug has been fixed in a more recent version)

What is the current bug behavior?

(What actually happens)

What is the expected correct behavior?

(What you should see instead)

Relevant logs and/or screenshots

(Paste any relevant logs - please use code blocks (```) to format console output,
logs, and code as it's very hard to read otherwise.)

Possible fixes

(If you can, link to the line of code that might be responsible for the problem)

/label ~bug ~reproduced ~needs-investigation
/cc @project-manager
/assign @qa-tester 
```