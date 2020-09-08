# 标记[](#label "Permalink")

## 概览[](#overview "Permalink")

随着Issue、合并请求和Epic数量的增长，跟踪这些项目将变得越来越困难，尤其是随着您的组织从只有几个人发展到成百上千人后。这里就出现了标记，它们可以帮助您组织和标记工作，以便您可以跟踪和找到您感兴趣的工作项。

标记是[看板](/docs/user/project/kanban.md)的关键部分，通过使用标记，您可以：

*   使用颜色和描述性标题（例如`bug` ， `feature request`或`docs`对 Epic，Issue 及合并请求进行分类
*   动态过滤和管理 Epic、 Issue 及合并请求
*   [搜索 Issue 列表、合并请求和史诗](/docs/user/search.md#issues-and-merge-requests)以及[看板](/docs/user/search.md#issue-boards) 

## 项目标记和组织标记[](#project-labels-and-group-labels "Permalink")

我们有两种类型的标记：

*   **项目标记**只能分配给该项目，并且只能合并该项目中的请求
*   可以将**组织标记**分配给选定组或其子组中的任何项目中的 Issue及合并请求
    *   也可以将它们分配给所选组或其子组中的 Epic

## 分配/取消分配标记[](#assign-and-unassign-labels "Permalink")

每个 Issue、合并请求和 Epic 都可以分配任意数量的标记，您可以在标记管理中根据需要分配或取消分配标记。

可以通过以下步骤将标记分配给 Issue、请合并请求或 Epic：

1.  在 Issue 的标记部分，点击**编辑** ，然后：
    *   在列表中，单击所需的标记，每个标记都带有复选框
    *   通过输入搜索查询并单击搜索来查找标记，然后点击它们，您可以反复搜索并添加更多标记
2.  单击**X**或标记部分之外的任何位置，然后将应用标记

您也可以使用[`/assign @username`快速操作](/docs/user/project/quick-actions.md)来分配标记。

## Label management[](#label-management "Permalink")

具有 Reporter 或更高[权限级别](../permissions.html)的用户可以创建和编辑标记。

### 项目标记[](#project-labels "Permalink")

通过转到项目并单击** Issue > 标记**来查看项目标记列表，该列表包括在项目级别定义的所有标记，以及从直接父组继承的所有标记。您可以通过在顶部输入搜索查询并点击搜索。

可以通过以下步骤创建一个新的项目标记：

1.  进入到项目中的" ** Issue ">"标记** "
2.  单击**新建标记**按钮
    *   输入标题
    *   （可选）输入描述
    *   （可选）通过单击可用颜色来选择背景颜色，或输入特定颜色的十六进制颜色值
3.  单击**创建标记**以创建标记

您也可以从 Issue 或合并请求中创建新的项目标记，在 Issue或合并请求的右侧栏中的标记部分：

1.  单击 **编辑**
2.  单击 **创建项目标记**
    *   填写名称字段，请注意，如果以此方式创建标记，则无法指定描述。您可以稍后通过编辑标记来添加描述（请参见下文）
    *   （可选）通过单击可用颜色来选择颜色，或输入特定颜色的十六进制颜色值
3.  单击 **创建项目标记**

创建标记后，您可以点击编辑，或通过单击三个点旁边的" **订阅"**按钮，然后选择" **删除"** 

#### 将项目标记提升为组织标记[](#promote-a-project-label-to-a-group-label "Permalink")

如果您以前创建了项目标记，现在想在同组织中的其他项目也使用这个标记的话，可以将其升级为组标记。

如果同一组中的其他项目具有相同标题的标记，则它们将全部与新的组标记合并；如果存在具有相同标题的组标记，则它也会被合并。

所有 Issue 、合并请求、看板，发行板过滤器以及带有旧标记的标记订阅都将分配给新的组标记.

警告： **警告：**提升标记是永久性的操作，不能撤消.

要将项目标记提升为组标记：

1.  导航到项目中的" **问题">"标记** "
2.  单击**订阅**按钮旁边的三个点，然后选择**升级为组标记** 

### 组织标记[](#group-labels "Permalink")

通过转到组织并单击** Issue >标记**来查看组标记列表，该列表包括仅在组级别定义的所有标记。它没有列出项目中定义的任何标记，您可以通过在顶部输入搜索查询并点击搜索。

要创建**组标记**，可以进入到**组织** **组织设置>标记** ，并按照与[创建项目标记](#project-labels)相同的过程进行操作即可。

### 创建默认标记[](#generate-default-labels "Permalink")

如果项目或组织没有标记，则可以从标记列表页面生成一组默认的项目或组织标记。如果列表为空，该页面将显示一个**生成默认标记**按钮，单击该按钮会将以下默认标记添加到项目中：

*   `bug`
*   `confirmed`
*   `critical`
*   `discussion`
*   `documentation`
*   `enhancement`
*   `suggestion`
*   `support`

## 订阅标记[](#subscribing-to-labels "Permalink")

在项目标记列表页面和组标记列表页面中，您可以单击任何标记右侧的**订阅**以启用该标记的通知。只要将标记分配给 Issue 或合并请求，您就会收到通知。

如果要从项目内订阅组标记，则可以选择仅订阅项目或整个组织的标记通知。

## 标记优先级[](#label-priority "Permalink")

标记可以具有相对优先级，在 Issue 及合并请求列表页面的" **标记优先级"**和" **优先级"**排序顺序中使用。 组标记和项目标记的优先级都在项目级别进行，不能从组标记列表中进行。

在项目标记列表页面上，在标记上加上星号以表明它具有优先级。

[![Labels prioritized](/docs/img/labels_prioritized_v12_1.png)](/docs/img/labels_prioritized_v12_1.png)

在列表中上下拖动已加星标的标记以更改其优先级，列表中位置越高表示优先级较高。

[![Drag to change label priority](/docs/img/labels_drag_priority_v12_1.png)](/docs/img/labels_drag_priority_v12_1.gif)

如果您按`Label priority`排序，将使用以下排序顺序：

1.  具有较高优先级标记的项目
2.  没有优先标记的项目

注意，只会检查优先级最高的标记，而忽略优先级较低的标记。

如果您按`Priority`排序，则将使用以下排序顺序：

1.  具有里程碑的截止日期的项目，最早分配的[里程碑](/docs/user/project/milestone.md)在此列出
2.  具有里程碑的项目，没有截止日期
3.  具有较高优先级标记的项目
4.  没有优先标记的项目

## 故障排除[](#troubleshooting "Permalink")

### 以`_duplicate<number>`结尾的标记[](#some-label-titles-end-with-_duplicatenumber "Permalink")

在特定情况下，可以在同一名称空间中创建具有重复标题的标记，这些重复标记的标题后面会加上`_duplicate<number>` 。如果愿意，可以安全地更改这些标记的标题。