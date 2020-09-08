# 机密 Issue[](#confidential-issues "Permalink")

机密性 Issue 是指那些仅具有[足够权限](#permissions-and-access-to-confidential-issues)的项目成员可见的 Issue， 开源项目和公司都可以使用机密 Issue 来使安全漏洞不被公开或防止意外泄漏。

## 将 Issue 设置为私密[](#making-an-issue-confidential "Permalink")

您可以在创建 Issue 或编辑现有 Issue 的过程中将其设置为保密。

创建新 Issue 时，可以在文本区域下方的复选框中将问题标记为机密 Issue。选中该框，然后点击" **提交问题"**按钮以创建 Issue。对于现有 Issue ，可以对其进行编辑，然后选中机密复选框，并点击**保存更改** 。

[![Creating a new confidential issue](/docs/img/confidential_issues_create.png)](/docs/img/confidential_issues_create.png)

## 修改 Issue 的机密性[](#modifying-issue-confidentiality "Permalink")

有两种方法可以更改 Issue 的机密性：

第一种方法是编辑 Issue 并标记/取消标记机密复选框，保存 Issue 后，它将更改 Issue 的机密性；

第二种方法是在 Issue 详情页右侧找到"保密性"部分，然后单击**编辑**，在弹出的窗口中可以设置打开或关闭 Issue 的机密性。

每次 Issue 机密性的更改也会被系统作为评论自动记录在 Issue 的历史记录中。

[![Confidential issues system notes](/docs/img/confidential_issues_system_notes.png)](/docs/img/confidential_issues_system_notes.png)

## 机密 Issue 区别[](#indications-of-a-confidential-issue "Permalink")

> **注意：**如果您没有足够的权限，您将无法看到机密 Issue 。

我们可以通过以下几点来区分机密 Issue 和普通 Issue：

在 Issue 列表页面视图中，您可以在标记为机密的问题旁边看到斜线图标

[![Confidential issues index page](/docs/img/confidential_issues_index_page.png)](/docs/img/confidential_issues_index_page.png)

* * *

同样，在 Issue 详情页，您可以在 Issue 标题上方看到斜线图标，此外在下方的评论区域中也有一个提示框，表明您正在评论的 Issue 是机密的。

[![Confidential issue page](/docs/img/confidential_issues_issue_page.png)](/docs/img/confidential_issues_issue_page.png)

Issue 详情页右边栏也有一个 机密性的标识：

[![Sidebar confidential issue](/docs/img/sidebar_confidential_issue.png)](/docs/img/sidebar_confidential_issue.png)

## 机密 Issue 的访问权限[](#permissions-and-access-to-confidential-issues "Permalink")

对于机密 Issue ，有两种级别的访问权限。一般情况下，机密 Issue 仅对具有Reporter 访问权限的项目成员可见；但是，Guest 用户也可以创建机密 Issue ，但 Guest 只能查看到他们自己创建的机密 Issue 。

对于没有权限的用户，机密 Issue 在搜索结果中也会被隐藏。

## 由机密 Issue 创建的合并请求[](#merge-requests-for-confidential-issues "Permalink")

为了防止机密信息在帮助解决机密 Issue 的过程中从公共项目中泄露，我们可以通过创建私有 Fork 项目的合并请求来解决机密 Issue 。

创建的合并请求将针对私有 Fork 项目的默认分支，而不是公共上游项目的默认分支。这样可以防止合并请求、分支和提交进入公共代码仓库，避免过早地泄露机密信息。当准备好将机密提交公开时，可以通过打开从私有 Fork 项目到公共上游项目的合并请求来完成。

**最佳实践：**如果您在原始上游的同一组织或子组织中创建了一个长期的私有 Fork 项目，则公共项目的所有具有 Developer 权限的用户在私有项目中也将具有相同的权限，这样，所有有权查看机密 Issue 的开发人员都将拥有更简化的工作流程来解决这些 Issue 。

### 实现方式[](#how-it-works "Permalink")

在机密 Issue 中，将会显示**创建机密合并请求**按钮，单击它会打开一个下拉列表，您可以在其中选择**创建机密合并请求和分支**或**创建分支**。

**项目**下拉列表将显示用户至少是 Developer，并且合并请求已启用的全部私有 Fork 项目列表。

每当" **分支名称"**和" **源（分支或标记）"**字段更改时，将检查目标或源分支的可用性。 两个分支都应在所选的私有 Fork项目中可用。

单击**创建机密合并请求**按钮后，将在私有 Fork 项目中创建分支和合并请求，当选择**创建分支**时，将仅创建分支。

在私有 Fork项目中创建分支后，开发人员现在可以将代码推送到该分支以解决机密 Issue 。