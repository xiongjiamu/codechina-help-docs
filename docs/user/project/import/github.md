# 从Github导入[](#从Github导入 "Permalink")

使用导入器，您可以将 GitHub 代码仓库导入 CODEChina。

## 概览[](#overview "Permalink")

导入了项目的以下方面：

*   仓库描述
*   Git 存储库数据
*   Issue
*   拉取请求
*   Wiki
*   里程碑
*   标签
*   Release
*   拉取请求评论
*   定期发布和请求注释

保留对拉取请求和问题的引用，并且每个导入的存储库都保持可见性级别，除非该可见性级别受到限制 ，在这种情况下，它默认为默认项目可见性。

## 实现原理[](#how-it-works "Permalink")

导入 Issue 和拉取请求时，导入程序会尝试在数据库中查找其 GitHub 作者和 指派人（请注意，拉取请求在 CODEChina 中被称为"合并请求"）。

为了导入成功，在Github 项目导入前，至少需要项目中的每个作者和指派人都应该满足下列条件：

*   有一个 GitHub 帐户，其[主要电子邮件地址](https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/setting-your-commit-email-address)与其 CODEChina 帐户的电子邮件地址匹配。

如果在 CODEChina 的数据库中未找到项目中引用的用户，则会将项目创建者（通常是启动导入的用户）设置为作者/指派人，但是对于该项目中 Issue 的评论，还是会提及到 Github 原作者。

如果导入项目的命名空间不存在，则导入项目时会创建新的命名空间/组织；如果名称空间已经被占用，则会将该项目导入至启动导入过程的用户的命名空间里，命名空间/代码仓库名称也可以由具有权限的用户进行编辑。

有关更多技术细节，您可以参考使用 GitHub 导入器开发人员文档。