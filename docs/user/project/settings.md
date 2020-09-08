# 项目设置[](#settings "Permalink")

**注意：**只有项目 maintainer [有权](/docs/user/permissions.md)访问项目设置。

您可以通过导航到项目的主页并点击**设置**来调整[项目](/docs/user/project.md)设置。

## 常规设置[](#general-settings "Permalink")

在项目的常规设置下，您可以找到与项目功能有关的所有内容。

### General project settings[](#general-project-settings "Permalink")

调整项目的名称，描述，头像，默认分支和主题：

项目描述还部分支持[标准 Markdown](/docs/user/markdown.md#standard-markdown-and-extensions-in-gitlab) ，您可以使用[强调](/docs/user/markdown.md#emphasis) ， [链接](/docs/user/markdown.md#links)和[换行符](/docs/user/markdown.md#line-breaks)为项目描述添加更多上下文。

#### 合规性框架[](#compliance-framework-premium "Permalink")

您可以选择一个框架标签来标识您的项目具有某些合规性要求或需要其他监督. 可用的标签包括：

*	GDPR - General Data Protection Regulation
*	HIPAA - Health Insurance Portability and Accountability Act
*	PCI-DSS - Payment Card Industry-Data Security Standard
*	SOC 2 - Service Organization Control 2
*	SOX - Sarbanes-Oxley

### 共享和权限[](#sharing-and-permissions "Permalink")

对于您的代码仓库，您可以设置例如公共访问，存储库功能，文档，访问权限等等。要从您的项目中执行此操作，请转到**"项目设置"** >" **常规设置"** ，然后展开" **可见性"，"项目功能"，"权限"**部分。

现在，您可以更改项目可见性，如果将" **项目可见性"**设置为公开，则可以将某些功能的访问权限限制为" **仅项目成员"** 。 此外，您可以选择[允许用户请求访问权限](/docs/user/project/member.md#project-membership-and-requesting-access)的选项。

**警告：**如果降低项目的可见性级别，则该操作将取消该项目的所有分支的链接。

使用开关启用或禁用以下功能：

| Option | 更多访问限制选项 | Description |
| --- | --- | --- |
| **Issues** | ✓ | 激活 GitLab 问题跟踪器 |
| **Repository** | ✓ | 启用 [仓库](/docs/user/project/repo.md) 功能 |
| **合并请求** | ✓ | 启用[合并请求](/docs/user/project/merge-request.md)功能； 另请参阅[合并请求设置](#merge-request-settings) |
| **Forks** | ✓ | 允许 fork 项目 |
| **Git 大文件存储** |   | 允许使用大文件 |
| **Packages** |   | Supports configuration of a package registry functionality |
| **Wiki** | ✓ | 启用单独的[文档](/docs/user/project/wiki.md)系统 |
| **指标仪表板** | ✓ | 控制对指标仪表板的访问 |

一些功能取决于其他功能：

*   如果禁用" ** Issue "**选项，则还将删除以下功能：
    *   **看板**
    *   [**服务台**](#service-desk-starter)**注意：**禁用" ** Issue "**选项后，您仍然可以从合并请求访问**里程碑** .
  
*   此外，如果您同时禁用**Issues**和**合并请求** ，则将无法再访问：
    *   **标签**
    *   **大事记**

*   如果禁用**代码仓库**功能，还将为您的项目禁用以下功能：
    *   **合并请求**
    *   **pipeline**
    *   **docker**
    *   **Git 大文件存储**
    *   **environment**
*   指标仪表板访问要求同时阅读项目环境和部署，有权访问指标仪表板的用户还可以访问环境和部署。

#### 禁用邮件通知[](#disabling-email-notifications "Permalink")

项目 Owner 可以通过选中" **禁用电子邮件通知"**复选框来**禁用**与项目相关的所有[电子邮件通知](/docs/user/account/email-notify.md#gitlab-notification-emails)。

### 合并请求设置[](#merge-request-settings "Permalink")

设置项目的合并请求设置：

*   设置合并请求方法（合并提交， [快速合并](/docs/user/project/merge-request/fast-forward.md) ）
*   添加合并请求[描述模板](/docs/user/project/description-template.md#description-templates) 
*   启用合并请求批准
*   启用 [只有全部讨论内容解决后才允许合并](/docs/user/discussions.md#only-allow-merge-requests-to-be-merged-if-all-threads-are-resolved)
*   默认启用`合并后删除分支`
*   配置建议的更改提交信息


### 服务台[](#service-desk-starter "Permalink")

为您的项目启用服务台以提供客户支持

### 导出项目[](#export-project "Permalink")

可以在 CODEChina 中导出您的项目

### 高级设置[](#advanced-settings "Permalink")

在这里，您可以运行内部管理，存档，重命名，传输， [删除派生关系](#removing-a-fork-relationship)或删除项目。

#### 归档项目[](#archiving-a-project "Permalink")

归档项目后，所有用户都将其设为只读，并表明该项目已不再处于主动维护状态。也可以取消归档已归档的项目，只有项目 Owner 才[有权](/docs/user/permissions.md)归档项目。

归档项目后，存储库，问题，合并请求和所有其他功能均为只读，归档的项目也隐藏在项目列表中。

可以通过以下步骤归档一个项目：

1.  进入到您项目的 **项目设置>常规设置** 
2.  在" **高级"下** ，单击" **展开"** 
3.  在" **存档项目"**部分中，单击" **存档项目"**按钮
4.  根据要求确认操作

#### 取消项目归档[](#unarchiving-a-project "Permalink")

取消归档项目会删除对项目的只读限制，并使其在项目列表中可用。只有项目 Owner 才[有权](/docs/user/permissions.md)取消归档项目。

要查找已归档的项目：

1.  以具有项目 Owner 的用户身份登录到 CODEChina
2.  如果你：
    *   拥有项目的 URL，在浏览器中打开项目的页面.
    *   没有项目的 URL：1.单击**项目>浏览项目** ；1.在" **排序项目"**下拉框中，选择" **显示存档的项目"** ；1.在**按名称过滤**字段中，提供项目的名称；1.单击指向项目的链接以打开其" **详细信息"**页面

接下来，要取消归档项目：

1.  进入到您项目的 **项目设置>常规设置** .
2.  在 **归档项目**, 点击 **展开**.
3.  在" **取消存档项目"**部分中，单击" **取消存档项目"**按钮
4.  根据要求确认操作

#### 重命名一个项目[](#renaming-a-repository "Permalink")

**注意：**只有项目维护者才[有权](/docs/user/permissions.md#project-members-permissions)重命名代码仓库。不要与项目名称混淆，也可以从[常规项目设置中](#general-project-settings)进行更改。

项目的存储库名称定义其 URL（您用于通过浏览器访问该项目的 URL）及其在安装服务器的文件磁盘上的位置。

要重命名存储库：

1.  进入到您项目的 **项目设置>常规设置** 
2.  在" **高级"下** ，单击" **展开"** 
3.  在"重命名存储库"下，根据您的喜好更改"路径"
4.  Hit **重命名项目**

请记住，这可能会带来意想不到的副作用，因为使用旧网址的每个人都无法推送或拉动。

#### 转移项目[](#transferring-an-existing-project-into-another-namespace "Permalink")

**注意：**只有项目 Owner 才[有权](/docs/user/permissions.md)转移项目。

在以下情况下，您可以将现有项目转移到[组织中](/docs/user/org.md) ：

*   您至少对该组具有** maintainer ** [权限](/docs/user/permissions.md#project-members-permissions) 
*   您至少是要转让的项目的** Owner ** 
*   将项目转移到的组必须允许创建新项目

开源通过以下操作进行项目的转移操作：

1.  进入到您项目的 **项目设置>常规设置**
2.  在" **高级"下** ，单击" **展开"**
3.  在"传输项目"下，选择要将项目传输到的命名空间
4.  按照说明键入项目路径，以确认传输

完成后，您将被带到新项目的命名空间。

#### 删除项目[](#remove-a-project "Permalink")

**注意：**只有项目所有者和管理员才[有权](/docs/user/permissions.md#project-members-permissions)删除项目.

删除项目：

1.  进入到您项目的 **项目设置>常规设置>高级** 
2.  在"删除项目"部分中，单击" **删除项目"**按钮
3.  根据要求确认操作

这个动作：

*   删除包含所有相关资源（问题，合并请求等）的项目

#### 删除 fork 项目关系[](#removing-a-fork-relationship "Permalink")

Fork 是为您不是项目成员的项目做贡献的好方法，如果您想自己使用 fork，而无需将[合并请求](/docs/user/project/merge-request.md)发送到上游项目，则可以安全地删除 fork 关系。

**注意：**删除后，将无法恢复 fork 关系。您将不再能够将合并请求发送到源，并且如果有人 fork 了您的项目，他们的分支也将失去关系。

您可以通过以下操作来删除 fork 项目关系：

1.  进入到您项目的**项目设置>常规设置>高级** .
2.  在" **删除 fork 关系"下** ，单击删除按钮
3.  按照说明键入项目的路径，以确认删除操作

**注意：**只有项目 Owner [有权](/docs/user/permissions.md#project-members-permissions)删除 fork 关系。