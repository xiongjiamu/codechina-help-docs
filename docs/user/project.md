# 项目[](#项目 "Permalink")

您可以创建用于托管代码库的项目，可以通过项目进行 Issue 管理，进行代码协作，并使用内置的  CI / CD 持续构建，测试和部署应用程序。

您可以设置您的项目为公开或私有，我们也不限制您创建的私有项目数量。

## 项目功能[](#projects-features "Permalink")

创建项目时，您可以使用众多功能：

**代码仓库:**

*   [Issue](/docs/user/project/issues.md) ：与您的团队讨论问题内的实现
    *   [看板](/docs/user/project/kanban.md) ：组织工作流程并确定其优先级
*   [代码仓库](/docs/user/project/repo.md) ：将代码托管在完全集成的平台中
    *   [分支](/docs/user/project/repo/branches.md) ：使用 Git 分支策略在代码上进行协作
    *   [受保护的分支机构](/docs/user/project/protected-branch.md) ：防止协作者弄乱历史记录或在未经审查的情况下推送代码
    *   [受保护的标签](/docs/user/project/protected-tag.md) ：控制谁有权创建标签，并防止意外更新或删除
    *   储存库镜像
    *   [签署提交](/docs/user/project/repo/gpg-sign.md) ：使用 GPG 签署您的提交
    *   部署令牌 ：管理基于项目的部署令牌，这些令牌允许永久访问存储库和 Container Registry.
*   [Web IDE](/docs/user/project/webide.md)

**Release 及合并请求：**

*   [Issue](/docs/user/project/issues.md) ：与您的团队讨论问题内的实现
    *   [发行板](/docs/user/project/kanban.md) ：组织工作流程并确定其优先级
*   [合并请求](/docs/user/project/merge-request.md) ：应用您的分支策略并获得团队的审查
    *   合并请求批准 ：实施更改之前请求批准
    *   [修复合并中的冲突](/docs/user/project/merge-request/resolve-conflicts.md) ：直接从网页中使用 Git diff 工具
    *   审查应用程序 ：按分支实时预览合并请求中建议的更改结果
*   [标签](/docs/user/project/label.md) ：按标签整理问题并合并请求
*   [时间跟踪](/docs/user/project/time-track.md) ：跟踪估计在完成问题或合并请求上花费的时间和时间
*   [里程碑](/docs/user/project/milestone.md) ：朝着目标日期迈进
*   [描述模板](/docs/user/project/description-template.md) ：为项目定义特定于上下文的模板，并为您的项目合并请求描述字段
*   [斜杠命令（快速操作）](/docs/user/project/quick-actions.md) ：针对问题或合并请求的常见操作的文本快捷方式
*   [自动完成字符](/docs/user/project/autofill.md) ：自动完成对用户，组，问题，合并请求和其他 GitLab 元素的引用
*   [Web IDE](/docs/user/project/webide.md)

**其他特性：**

*   [Wiki](/docs/user/project/wiki.md) ：在集成的 Wiki 中记录您的项目
*   代码片 ：存储，共享和协作代码片段
*   价值流分析 ：查看您的开发生命周期
*   分析：配置对您的项目至关重要的见解
*   语法高亮 ：一种自定义代码块的替代方法，可替代默认语言选择
*   [Release](/docs/user/project/releases.md) ：一种跟踪项目中可交付成果的方式，可作为源，构建输出，其他元数据和与代码的发行版本相关的其他工件的快照
*   代码所有者 ：为某些文件指定代码所有者
*   License ：批准和拒绝项目的许可证
*   依赖项列表 ：查看项目依赖项
*   要求 ：要求使您可以创建标准来检查产品
*   静态站点编辑器 ：无需事先了解代码库或 Git 命令，即可在静态网站上快速编辑内容

### 项目集成[](#项目集成 "Permalink")

将您的项目与 Jira，Mattermost，Kubernetes，Slack 等进行集成。

## 新建项目[](#新建项目 "Permalink")

了解如何在 CODEChina 中[创建一个新项目](/docs/basic/create-project.md) 。

### Fork 项目[](#fork项目 "Permalink")

您可以Fork 一个项目 ，以便：

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

了解更多有关[项目设置](/docs/user/project/settings.md)的文档。

## 导入/导出项目[](#i导入导出项目 "Permalink")

*   [导入项目](/docs/user/project/import.md) from:
    *   [从Github导入](/docs/user/project/import/github.md)
    *   [从Bitbucket导入](/docs/user/project/import/by-url.md)
*   导出项目

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

了解如何[将成员添加到您的项目中](/docs/user/project/member.md) 

## 退出项目[](#退出项目 "Permalink")

当项目属于组织时（即项目在[组织的命名空间下](/docs/user/org.md#命名空间) ），**退出项目**将仅显示在项目的页面上。如果您选择退出项目，那么您将不再是项目成员，并且将无法继续参与项目。

## 项目首页[](#项目首页 "Permalink")

项目首页会根据项目的可见性设置和用户权限来显示不同的内容：

对于公共项目以及私有项目中[有权查看该项目代码](/docs/user/permissions.md#project-members-permissions)的项目成员：

*   显示[`README`文件或索引文件的](/docs/user/project/repo.md#repository-readme-and-index-files)内容（如果有），然后显示项目存储库中的目录列表
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