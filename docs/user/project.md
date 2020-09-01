# 项目[](#项目 "Permalink")

您可以创建用于托管代码库的项目，可以通过项目进行 Issue 管理，进行代码协作，并使用内置的  CI / CD 持续构建，测试和部署应用程序。

您可以设置您的项目为[公开](../../public_access/public_access.html)或[私有](../../public_access/public_access.html)，我们也不限制您创建的私有项目数量。

## 项目功能[](#项目功能 "Permalink")

创建项目时，您可以使用众多功能：

**代码仓库:**

*   [Issue](issues/index.html) ：与您的团队讨论问题内的实现
    *   [看板](issue_board.html) ：组织工作流程并确定其优先级
*   [代码仓库](repository/index.html) ：将代码托管在完全集成的平台中
    *   [分支](repository/branches/index.html) ：使用 Git 分支策略在代码上进行协作
    *   [受保护的分支机构](protected_branches.html) ：防止协作者弄乱历史记录或在未经审查的情况下推送代码
    *   [受保护的标签](protected_tags.html) ：控制谁有权创建标签，并防止意外更新或删除
    *   [储存库镜像](repository/repository_mirroring.html)
    *   [签署提交](gpg_signed_commits/index.html) ：使用 GPG 签署您的提交
    *   [部署令牌](deploy_tokens/index.html) ：管理基于项目的部署令牌，这些令牌允许永久访问存储库和 Container Registry.
*   [Web IDE](web_ide/index.html)

**Release 及合并请求：**

*   [Issue](issues/index.html) ：与您的团队讨论问题内的实现
    *   [发行板](issue_board.html) ：组织工作流程并确定其优先级
*   [合并请求](merge_requests/index.html) ：应用您的分支策略并获得团队的审查
    *   [合并请求批准](merge_requests/merge_request_approvals.html) ：实施更改之前[请求批准](merge_requests/merge_request_approvals.html)
    *   [修复合并中的冲突](merge_requests/resolve_conflicts.html) ：直接从网页中使用 Git diff 工具
    *   [审查应用程序](../../ci/review_apps/index.html) ：按分支实时预览合并请求中建议的更改结果
*   [标签](labels.html) ：按标签整理问题并合并请求
*   [时间跟踪](time_tracking.html) ：跟踪估计在完成问题或合并请求上花费的时间和时间
*   [里程碑](milestones/index.html) ：朝着目标日期迈进
*   [描述模板](description_templates.html) ：为项目定义特定于上下文的模板，并为您的项目合并请求描述字段
*   [斜杠命令（快速操作）](quick_actions.html) ：针对问题或合并请求的常见操作的文本快捷方式
*   [自动完成字符](autocomplete_characters.html) ：自动完成对用户，组，问题，合并请求和其他 GitLab 元素的引用
*   [Web IDE](web_ide/index.html)

** CI / CD：**

*   [CI / CD](../../ci/README.html) ：内置的持续集成，交付和部署工具
    *   [容器注册表](../packages/container_registry/index.html) ：开箱即用地构建和推送 Docker 映像
    *   [自动部署](../../topics/autodevops/stages.html#auto-deploy) ：配置 CI / CD 以自动设置应用程序的部署
    *   [启用和禁用 CI / CD](../../ci/enable_or_disable_ci.html)
    *   [Pipelines](../../ci/pipelines/index.html) ：从 UI 配置和可视化 GitLab CI / CD 管道
        *   [计划的Pipeline](../../ci/pipelines/schedules.html) ：计划管道以在选定的时间开始
        *   [Pipeline图](../../ci/pipelines/index.html#visualize-pipelines) ：通过WEB查看整个管道
        *   [作业工件](../../ci/pipelines/job_artifacts.html) ：定义，浏览和下载作业工件
        *   [Pipeline设置](../../ci/pipelines/settings.html) ：设置 Git 策略（选择从作业中的 GitLab 提取存储库的默认方式），超时（定义可以运行作业的最长时间（以分钟为`.gitlab-ci.yml` ）） `.gitlab-ci.yml`自定义路径，测试覆盖率分析，管道的可见性等
    *   [Kubernetes 集群集成](clusters/index.html) ：将您的 项目与 Kubernetes 集群连接
    *   [功能标志](../../operations/feature_flags.html) ：功能标志允许您通过动态切换某些功能来以不同的方式发布项目
*   [Pages](pages/index.html) ：使用[Pages](pages/index.html)构建，测试和部署您的静态网站

**其他特性：**

*   [Wiki](wiki/index.html) ：在集成的 Wiki 中记录您的项目
*   [代码片](../snippets.html) ：存储，共享和协作代码片段
*   [价值流分析](cycle_analytics.html) ：查看您的开发生命周期
*   [分析](insights/index.html) ：配置对您的项目至关重要的见解
*   [语法高亮](highlighting.html) ：一种自定义代码块的替代方法，可替代默认语言选择
*   [Release](releases/index.html) ：一种跟踪项目中可交付成果的方式，可作为源，构建输出，其他元数据和与代码的发行版本相关的其他工件的快照
*   [代码所有者](code_owners.html) ：为某些文件指定代码所有者
*   [License](../compliance/license_compliance/index.html) ：批准和拒绝项目的许可证.
*   [依赖项列表](../application_security/dependency_list/index.html) ：查看项目依赖项.
*   [要求](requirements/index.html) ：要求使您可以创建标准来检查产品.
*   [静态站点编辑器](static_site_editor/index.html) ：无需事先了解代码库或 Git 命令，即可在静态网站上快速编辑内容.

### 项目集成[](#项目集成 "Permalink")

[将您的项目](integrations/index.html)与 Jira，Mattermost，Kubernetes，Slack 等进行[集成](integrations/index.html) 。

## 新建项目[](#新建项目 "Permalink")

了解如何在 CODEChina 中[创建一个新项目](../../basics/create-project.html) .

### Fork 项目[](#fork项目 "Permalink")

您可以[Fork 一个项目](repository/forking_workflow.html) ，以便：

*   通过 Fork 项目并创建从分支到上游项目的合并请求来进行代码协作
*   Fork 一个项目并在该基础上进行开发

### Star 项目[](#star项目 "Permalink")

您可以star 一个项目，以便您更容易找到经常使用的项目。 项目拥有的 star 数量可以看做其受欢迎的程度。

可以通过以下操作 star 项目：

1.  进入要 star 项目的主页
2.  在页面的右上角，点击**Star** 

您可以通过以下操作查看已经 star 的项目：

1.  单击导航栏中的**项目** 
2.  单击**Star 的项目**
3.  显示您 Star 项目的信息，包括：

    *   项目描述，包括名称，描述和图标
    *   项目 Star 的次数
    *   项目 Fork 的次数
    *   打开的合并请求数
    *   未解决 Issue 的数量

### 浏览项目[](#浏览项目 "Permalink")

您可以探索其他设置为公开的项目。操作方式为：

1.  单击导航栏中的**项目** 
2.  单击**探索项目**

我们将为您显示一个项目列表，按上次更新日期排序。 要查看具有最多[Star](#star-a-project)项目，请单击 **最多Star** ；要查看过去一个月中评论数量最多的项目，请点击**趋势** 。

## 项目设置[](#项目设置 "Permalink")

项目设置允许您设置项目的可见性级别、访问级别，并执行诸如归档、重命名或转移项目的操作。

了解更多有关[项目设置](settings/index.html)的文档。

## 导入/导出项目[](#i导入导出项目 "Permalink")

*   [导入项目](import/index.html) from:
    *   [从Github导入](import/github.html)
    *   [从Bitbucket导入](import/bitbucket.html)
*   [导出项目](settings/import_export.html#exporting-a-project-and-its-data)


## 删除项目[](#删除项目 "Permalink")

可以通过以下操作删除一个项目：

1.  打开**项目设置>常规设置** 
2.  展开**高级**部分
3.  向下滚动到**删除项目**部分
4.  点击 **删除项目**
5.  通过输入所需的文本来确认删除操作

### 延迟删除[](#延迟删除 "Permalink")

默认情况下，删除项目后会延迟 7 天才真的会删除项目。在此期间项目为待删除状态， 管理员可以在这段时间内恢复项目。


## 项目成员[](#项目成员 "Permalink")

了解如何[将成员添加到您的项目中](members/index.html) 

## 退出项目[](#退出项目 "Permalink")

当项目属于组织时（即项目在[组织的命名空间下](../group/index.html#命名空间) ）， **退出项目**将仅显示在项目的页面上. 如果您选择退出项目，那么您将不再是项目成员，并且将无法继续参与项目。

## 项目首页[](#项目首页 "Permalink")

项目首页会根据项目的可见性设置和用户权限来显示不同的内容：

对于公共项目以及私有项目中[有权查看该项目代码](../permissions.html#project-members-permissions)的项目成员：

*   显示[`README`文件或索引文件的](repository/#repository-readme-and-index-files)内容（如果有），然后显示项目存储库中的目录列表
*   如果项目不包含这些文件中的任何一个，则访问者将看到存储库的文件和目录列表

对于没有权限查看项目代码的用户：

*   显示项目 Wiki（如果有）
*   显示项目的 Issue 列表

## 路径重定向[](#路径重定向 "Permalink")

当项目仓库路径变更时，从旧路径平稳过渡到新路径至关重要，我们提供两种重定向方式：Web 以及 Git 推/拉重定向。

这两种方式根据项目的情况，可能会有所不同。

当重命名一个用户、一个组织或者一个仓库时：

*   命名空间及其下的任何内容（例如项目）的现有 Web URL 将重定向到新 URL
*   命名空间下项目的现有 Git 远程 URL 将重定向到新的远程 URL，每次将其推/拉到修改过路径的代码仓库时，都会显示一条警告消息：提示您更新远程仓库地址。 这也就意味着在重命名后，任何自动化脚本或 Git 客户端将继续工作
*   只要原来的路径还没有被其他用户、组织或者项目占用，路径重定向功能将一直能够正常使用

## 项目 API[](#项目api "Permalink")

您的项目可以使用许多[API](../../api/README.html) ：

*   [话题](../../api/discussions.html)
*   [基本信息](../../api/projects.html)
*   [导入/导出项目](../../api/project_import_export.html)
*   [看板](../../api/boards.html)
*   [标签](../../api/labels.html)
*   [Markdown](../../api/markdown.html)
*   [合并请求](../../api/merge_requests.html)
*   [里程碑](../../api/milestones.html)