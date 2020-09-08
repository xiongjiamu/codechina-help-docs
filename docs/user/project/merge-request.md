# 合并请求[](#merge-request "Permalink")

合并请求使您可以可视化并协作对作为对指定 Git 分支的提交而存在的源代码的建议更改。

合并请求（ **MR** ）是代码协作和版本控制的基础。顾名思义，它就是一个*将*一个分支*合并*到另一个分支的*请求* 。

## 用户示例[](#use-cases "Permalink")

第一种情况，假设您是一个团队中的软件开发人员：

1.  您签出新分支，并通过合并请求提交更改
2.  您从团队中收集反馈
3.  您可以使用"代码质量"报告来进行优化代码的实现
4.  您可以在 CI / CD 中使用"JUnit 测试"报告来验证您的更改
5.  通过"许可证合规性"报告，可以避免使用许可证与您的项目不兼容的依赖项
6.  您要求您的经理批准
7.  您的经理：
    1.  拉取提交并进行最终审查
    2.  批准合并请求
    3.  将其设置为在 pipeline 成功时合并
8.  您的更改将通过手动操作 CI / CD 部署到生产中
9.  您的实施已成功交付给客户

第二种情况，假设您是为您公司网站编写网页的 Web 开发人员：

1.  您签出新分支，并通过合并请求提交新页面
2.  您从审稿人那里收集反馈
3.  您的更改将通过 Review Apps 进行预览
4.  您要求您的网页设计师实施
5.  您要求您的经理批准
6.  一旦批准，您的合并请求将被[squash](/docs/user/project/merge-request/squash.md) ，并[部署到暂存中](https://about.gitlab.com/blog/2016/08/26/ci-deployment-and-environments/)
7.  您的生产团队[cherry-pick](/docs/user/project/merge-request/cherry-pick.md)合并提交到生产中

## 概览[](#overview "Permalink")

合并请求（也称为" MR"）显示有关建议的更改的大量信息， MR 的主体包含其描述以及其小部件（显示有关 CI / CD 管道的信息，如果存在的话），然后是与该 MR 合作的人员的讨论内容。

MR 还包含导航选项卡，从中可以查看线程上正在进行的讨论，提交列表，代码更改以及内联代码审阅。

## 合并请求导航[](#merge-request-navigation-tabs-at-the-top "Permalink")

在合并请求中将显示" **讨论区"** ，" **提交"** 和" **更改"**的导航选项卡。

[![Merge request tab positions](/docs/img/merge_request_tab_position_v12_6.png)](/docs/img/merge_request_tab_position_v12_6.png)

## 新建合并请求[](#creating-merge-requests "Permalink")

点击了解 [如何创建一个新的合并请求](/docs/user/project/merge-request/create-merge-request.md)

## 管理和查看合并请求[](#reviewing-and-managing-merge-requests "Permalink")

查看和管理合并请求

## 在合并请求中测试和报告[](#testing-and-reports-in-merge-requests "Permalink")

有关合并请求中的测试选项和报告更改的信息

## 合并请求认证[](#authorization-for-merge-requests "Permalink")

使用 CODEChina 进行合并请求的主要方法有两种：

1.  在单个存储库中使用[受保护的分支](/docs/user/project/protected-branch.md)
2.  使用权威项目的分支