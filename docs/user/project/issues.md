# Issues[](#issues "Permalink")

问题是就想法和计划工作进行协作的基本介质。

## 概览[](#overview "Permalink")

CODEChina Issue 跟踪器是用于协作开发想法，解决问题和计划工作的高级工具。

通过 Issue，可以在以下各项之间，在实施之前和期间共享和讨论提案：

*   您和您的团队
*   外部合作者

它们还可以用于各种其他目的，根据您的需求和工作流程进行定制，Issue 始终与特定项目相关联.

**常见的用例包括：**

*   讨论新想法的实施
*   跟踪任务和工作状态
*   接受功能建议，问题，支持请求或错误报告
*   详细说明新的代码实现

另请参见[始终从 Issue 开始讨论](https://about.gitlab.com/blog/2016/03/03/start-with-an-issue/)。

## 认识 Issue[](#parts-of-an-issue "Permalink")

Issue 包含各种内容和元数据，从而在使用方式上具有很大的灵活性。每个 Issue 可以包含以下属性，但并非所有项目都是必须设置的。

*   **内容**
    *   标题
    *   描述和任务
    *   评论和其他活动
*   **人员**
    *   作者
    *   指派人
*   **状态**
    *   状态（打开或关闭）
    *   机密性
    *   任务（完成与未完成）
*   **规划和跟踪**
    *   里程碑
    *   截止日期
    *   时间跟踪
    *   标签
    *   投票数
    *   反应表情
    *   关联问题
    *   唯一的 Issue ID 和 URL


## 查看及管理 Issue[](#viewing-and-managing-issues "Permalink")

虽然您可以在[ Issue 页面](#issue-page)上查看和管理问题的全部详细信息，但也可以使用" [ Issue 列表"](#issues-list) ，["看板"](#issue-boards) ，Issue 引用 处理多个问题。

针对问题的关键操作包括：

*   [新建 Issue](/docs/user/project/issues/manage.md#create-a-new-issue)
*   [移动 Issue](/docs/user/project/issues/manage.md#moving-issues)
*   [关闭 Issue](/docs/user/project/issues/manage.md#closing-issues)
*   [删除 Issue](/docs/user/project/issues/manage.md#deleting-issues)

### Issue 详情页[](#issue-page "Permalink")

在 Issue 的详情页面上，您可以查看 Issue 的所有方面，如果有必要的[权限](/docs/user/permissions.md) ，可以对其进行修改。

### Issue 列表[](#issues-list "Permalink")

在" Issue 列表"上，可以查看当前项目中的所有问题。使用[搜索查询](/docs/user/search.md#filtering-issue-and-merge-request-lists)过滤 Issue 列表，包括特定的元数据，例如标签，指派人，状态等。从此视图，您还可以对显示的 Issue [进行批量](/docs/user/project/bulk-edit.md)更改。

您可以通过多种方式对问题列表进行排序，例如，通过问题创建日期，里程碑到期日期. 有关更多信息，请参见[排序和排序 Issue 列表](/docs/user/project/issues/sort.md)页面.

### 看板[](#issue-boards "Permalink")

[看板](/docs/user/project/kanban.md)中的其栏目根据标签来显示 Issue，它提供了可高度定制的工作流来管理问题的灵活性。

您可以在栏中重新排序 Issue，如果将 Issue 拖到另一列，则其关联的标签将更改以匹配新列的标签，整个看板可以被筛选为仅包括某个里程碑或总体标签中的问题。

### 相关的 Issue[](#related-issues-starter "Permalink")

您可以将两个 Issue 标记为"相关"，以便在查看一个 Issue 时，另一个 Issue 始终列在"相关 Issue"部分中，这可以帮助显示重要的上下文，例如过去的工作，依赖项或重复项等。

### 关联 Issue[](#crosslinking-issues "Permalink")

您可以通过引用另一个 Issue 来[关联 Issue](/docs/user/project/issues/crosslinking.md) ，也可以通过包括其 URL 或 ID 来合并请求。参考的 Issue 在活动流中显示有关参考的消息，并带有指向其他 Issue 或合并请求的链接。

### 相似 Issue[](#similar-issues "Permalink")

为了防止同一主题重复出现问题，在创建新 Isuue 时会搜索相似的 Issue。

在**新建 Issue**页面中键入标题时，系统会搜索用户在当前项目中有权访问的所有 Issue 的标题和描述，标题框下方最多显示五个类似问题（按最新更新排序）。

## 其他 Issue 操作[](#other-issue-actions "Permalink")

*   [从模板创建 Issue](/docs/user/project/description-template.md#using-the-templates)
*   [设置截止日期](/docs/user/project/issues/due-date.md)
*   [批量编辑问题](/docs/user/project/bulk-edit.md)——从 Issue 列表中选择多个 Issue，以批量更改其状态，指派人，里程碑或标签。