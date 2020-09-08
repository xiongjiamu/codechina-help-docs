# 里程碑[](#milestone "Permalink")

## 概览[](#overview "Permalink")

CODEChina 中的里程碑是一种跟踪 Issue 及合并请求并在一定时期内实现更广泛目标的方法。

里程碑使您可以将 Isuue 及合并请求组织到一个紧密联系的组中，并带有一个可选的开始日期和一个可选的截止日期。

## 用户敏捷 Sprint[](#milestones-as-agile-sprints "Permalink")

里程碑可用作敏捷 Sprint，因此您可以跟踪所有问题并合并与特定冲刺有关的请求. 为此：

1.  设置里程碑的开始日期和截止日期，以代表敏捷冲刺的开始和结束
2.  将里程碑标题设置为敏捷 sprint 的名称，例如`November 2018 sprint` 
3.  通过将问题的右侧边栏关联到所需的里程碑，将问题添加到敏捷 Sprint中

## 用里程碑来 Release[](#milestones-as-releases "Permalink")

同样，里程碑可以用作 Release，为此：

1.  设置里程碑到期日期以表示发布的发布日期，并将里程碑开始日期保留为空白
2.  将里程碑标题设置为您的发行版，例如`Version 9.4` 
3.  通过关联问题右侧的期望里程碑，将问题添加到您的发行中

此外，您可以将里程碑与 CODEChina 的[Releases 功能](/docs/user/project/releases.md#associate-milestones-with-a-release)集成.

## 项目里程碑和组织里程碑[](#project-milestones-and-group-milestones "Permalink")

您可以将**项目里程碑**分配给问题或仅合并该项目中的请求，要查看项目里程碑列表，请在项目中转到 **问题>里程碑** 。

您可以将**组里程碑**分配给该**组**中任何项目的任何发行或合并请求，要查看组里程碑列表，请在组中转到 **组织设置>里程碑** 。

## 新建里程碑[](#creating-milestones "Permalink")

**注意：**创建里程碑需要[ Developer 或更高](/docs/user/permissions.md)级别的权限。

### 新建项目里程碑[](#new-project-milestone "Permalink")

可以通过以下步骤创建**项目里程碑** ：

1.  在一个项目中，转到 ** Issue >里程碑** 
2.  单击 **新里程碑**
3.  输入标题，可选描述，可选开始日期和可选截止日期
4.  单击 **新建里程碑**

### 新建组织里程碑[](#new-group-milestone "Permalink")

可以通过以下步骤创建**组织里程碑** ：

1.  在一个小组中，进入到 **组织设置>里程碑** 
2.  单击 **新里程碑**
3.  输入标题，可选描述，可选开始日期和可选截止日期
4.  单击 **新建里程碑**

## 编辑里程碑[](#editing-milestones "Permalink")

**注意：**编辑里程碑需要[ Developer 或更高的](/docs/user/permissions.md)权限级别。

可以通过以下步骤编辑里程碑：

1.  在项目中进入** Issue > 里程碑** ，或在组织中进入**组织设置 > 里程碑**
2.  单击里程碑标题
3.  单击**编辑**按钮

您可以通过单击" **删除"**按钮来删除里程碑。

### 将项目里程碑提升为组织里程碑[](#promoting-project-milestones-to-group-milestones "Permalink")

如果要在同一个组织中将里程碑从几个项目扩展到更多项目，则可能需要在同一组中的多个项目中共享里程碑。如果以前创建了一个项目里程碑，现在要使其可用于同一组中的其他项目，则可以将其升级为组里程碑。

在项目里程碑列表页面，您可以将项目里程碑升级为组里程碑。这会将具有相同名称的该组中所有项目中的所有项目里程碑合并为一个组里程碑，以前已分配给这些项目里程碑之一的所有问题和合并请求现在都将分配给新的组里程碑。注意：此操作不能撤消，更改是永久的。

**警告：**将项目里程碑提升为组里程碑时，某些信息会丢失。组里程碑视图上并非项目里程碑视图上的所有功能都可用，如果将项目里程碑升级为组里程碑，则将失去这些功能。请参阅" [里程碑"](#milestone-view)视图以查看组里程碑视图中缺少哪些功能。

## 设置里程碑[](#assigning-milestones-from-the-sidebar "Permalink")

可以为每个 Issue 及合并请求分配一个里程碑，里程碑在边栏中的每个 Issue 及合并请求页面上可见，它们在看板上也可见。您可以在页面右侧为对象分配或取消里程碑。您也可以在讨论中[快速](/docs/user/project/quick-actions.md)执行此操作。 [如前所述](#project-milestones-and-group-milestones) ，对于给定的发布或合并请求，可以选择项目里程碑和组里程碑并将其分配给对象。

## 按里程碑过滤 Issue 及合并请求[](#filtering-issues-and-merge-requests-by-milestone "Permalink")

### 在列表页过滤[](#filtering-in-list-pages "Permalink")

在项目 Issue、合并请求列表页面和用户的 Issue 及合并请求列表页面中，可以按组里程碑和项目里程碑进行[筛选](/docs/user/search.md#issues-and-merge-requests) .

### 在看板上过滤[](#filtering-in-issue-boards "Permalink")

*   在[项目看板上](/docs/user/project/kanban.md) ，您可以在[搜索和过滤器栏中](/docs/user/search.md#issue-boards)按组里程碑和项目里程碑进行[筛选](/docs/user/search.md#issue-boards) 

### 特殊里程碑过滤[](#special-milestone-filters "Permalink")

在按里程碑进行筛选时，除了选择特定的项目里程碑或组里程碑之外，还可以选择特殊的里程碑筛选器：

*   **无** ：显示问题或没有分配里程碑的合并请求
*   **任何** ：显示问题或合并具有指定里程碑的请求
*   **即将到来的** ：显示已分配的公开里程碑的问题或合并请求，该里程碑具有下一个即将到来的到期日（即将来的最近到期日）
*   **已开始** ：显示具有打开的指定里程碑且开始日期在今天之前的问题或合并请求

## 认识里程碑[](#milestone-view "Permalink")

里程碑视图显示标题和描述，这些标签下面还包含显示以下内容的标签：

*   **Issue** ：显示分配给里程碑的所有问题， 这些内容显示在名为：
    *   未开始的问题（未解决和未分配）
    *   进行中的问题（未解决和已分配）
    *   已完成的问题（已关闭）
*   **合并请求** ：显示分配给里程碑的所有合并请求. 这些将显示在名为：
    *   进行中的工作（开放且未分配）
    *   等待合并（打开和未分配）
    *   拒绝（关闭）
    *   合并后
*   **参与者** ：显示分配给该里程碑的所有问题的指派人
*   **标记**: 显示分配给该里程碑的所有问题包含的标记