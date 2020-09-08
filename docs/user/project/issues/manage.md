# 管理 Issue[](#managing-issues "Permalink")

Issue 是通过想法和计划进行协工作的基本要素。 [创建](#create-a-new-issue) ， [移动](#moving-issues) ， [关闭](#closing-issues)和[删除](#deleting-issues) Issue 是 Issue 中的关键操作。

## 创建 Issue[](#create-a-new-issue "Permalink")

创建新 Issue 时，系统将提示您填写 Issue 的数据和字段，如下所示。如果您清楚要分配给Issue 的值，则可以使用" [快速操作"](/docs/user/project/quick-actions.md)功能输入相应的内容，而不用从列表中选择它们。

### 获取新建 Issue 的表单[](#accessing-the-new-issue-form "Permalink")

有多种方法可以从项目中获取"新建 Issue"表单：

*   进入**项目** > ** Issue** > **新建 Issue** ：
*   从项目中**未解决的 Issue**中，点击**新建 Issue**以在同一项目中创建一个新的 Issue
*   在**项目的仪表板中** ，单击加号（ **+** ）打开带有一些选项的下拉菜单，选择**新建 Issue**以在该项目中创建一个 Issue：
*   在**看板**中，通过单击列表顶部的加号（ **+** ）创建新 Issue，将新建一个带有对应标签的 Issue

### 认识新建 Issue 的表单[](#elements-of-the-new-issue-form "Permalink")

[![New issue from the issues list](/docs/img/new_issue_v13_2.png)](/docs/img/new_issue_v13_2.png)

创建新 Issue 时，可以填写以下字段：

1. **标题**
2. **描述**
3. **问题机密性设置**
4. **指派人**
5. **截止日期**
6. **里程碑**
7. **标记**

## 移动 Issue[](#moving-issues "Permalink")

移动 Issue 会将其复制到新位置（项目），并在旧项目中将其关闭，但不会被删除。这两个 Issue 上还将添加一个系统注释，以指示它来自何处。

移动 Issue 的按钮位于 Issue 详情页右侧最底部。

## 关闭 Issue[](#closing-issues "Permalink")

当您确定 Issue 已解决或不再需要解决时，可以使用"关闭"按钮关闭该 Issue。

您还可以通过在看板中将从其拖放到**已关闭**列表中来**关闭** Issue。

### 自动关闭 Issue[](#closing-issues-automatically "Permalink")

**注意：**由于性能原因，从现有代码仓库的第一次推送将禁用自动关闭 Issue 功能。

当提交或合并请求解决了一个或多个 Issue 时，在将提交或合并请求推送到项目的默认分支时将会自动关闭这些 Issue。

如果提交消息或合并请求描述包含与[定义的模式](#default-closing-pattern)相匹配的文本，则匹配文本中引用的所有 Issue 均将被关闭。将提交推送到项目的[**默认**分支时](/docs/user/project/repo/branches.md#default-branch) ，或者将提交或合并请求合并到默认分支时，Issue 就会自动关闭。

例如，如果合并请求描述中包含`Closes #4, #6, Related to #5`，则合并合并请求时问题`#4`和`#6`将自动关闭，但不会合并`#5`，只会将其标记为相关 Issue ，但不会自动关闭。

如果 Issue 与 合并请求位于不同的代码仓库中，则需要提供完整的 Issue URL地址：

```markdown
Closes #4, #6, and https://codechina.csdn.net/<username>/<projectname>/issues/<xxx> 
```

#### 默认关闭表达式[](#default-closing-pattern "Permalink")

如果未指定，将使用如下所示的表达式来用作默认 Issue 关闭的表达式：

```markdown
\b((?:[Cc]los(?:e[sd]?|ing)|\b[Ff]ix(?:e[sd]|ing)?|\b[Rr]esolv(?:e[sd]?|ing)|\b[Ii]mplement(?:s|ed|ing)?)(:?) +(?:(?:issues? +)?%{issue_ref}(?:(?: *,? +and +| *,? *)?)|([A-Z][A-Z0-9_]+-\d+))+) 
```
这将匹配以下关键字：

*   Close, Closes, Closed, Closing, close, closes, closed, closing
*   Fix, Fixes, Fixed, Fixing, fix, fixes, fixed, fixing
*   Resolve, Resolves, Resolved, Resolving, resolve, resolves, resolved, resolving
*   Implement, Implements, Implemented, Implementing, implement, implements, implemented, implementing

请注意， `%{issue_ref}`是在源代码中定义的复杂正则表达式，可以匹配对以下内容的引用：

*   本地 Issue（ `#123` ）.
*   跨项目 Issue（ `group/project#123` ）.
*   指向 Issue 的链接（ `https://gitlab.example.com/group/project/issues/123` ）.

例如以下提交消息：

```markdown
Awesome commit message

Fix #20, Fixes #21 and Closes group/otherproject#22.
This commit is also related to #17 and fixes #18, #19
and https://codechina.csdn.net/group/otherproject/issues/23. 
```
将在提交被推送到的项目中关闭`#18` ， `#19` ， `#20`和`#21` ，以及`group/otherproject`项目中`#22`和`#23`，`#17`将不会关闭，因为它与关闭模式不匹配，当从命令行与`git commit -m`一起使用时，它可以处理多行/多行提交消息。

#### 禁用自动关闭 Issue[](#disabling-automatic-issue-closing "Permalink")

可以在[项目的设置中](/docs/user/project/settings.md)禁用项目的自动关闭 Issue 功能。引用的问题仍将按原样显示，但不会自动关闭。

这仅影响被新合并请求或提交关联的 Issue，已经解决的 Issue 仍然保持原样，禁用自动关闭 Issue 的设置仅影响当前项目中的合并请求，并不会阻止其他项目从通过跨项目的 Issue将其关闭。

## 删除 Issue[](#deleting-issues "Permalink")

具有项目 [Owner](/docs/user/permissions.md) 权限的用户可以通过编辑 Issue 并单击删除按钮来删除 Issue。
