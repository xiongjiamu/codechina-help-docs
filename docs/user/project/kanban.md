# 看板[](#issue-boards "Permalink")

我们也提供了种组织工作、提高效率的 Issue 看板，看板也支持将工作拆分为可执行的小任务，并使用看板实现工作的流转。

## 概览[](#overview "Permalink")

看板是一个软件项目管理工具，用于计划，组织和可视化功能或产品发布的工作流程，它可以用作[看板](https://en.wikipedia.org/wiki/Kanban_(development))或[Scrum 板](https://en.wikipedia.org/wiki/Scrum_(software_development))。

它结合了 Issue 跟踪和项目管理功能，将所有内容保持在同一位置，因此您无需在不同平台之间切换即可组织工作流程。

使用看板，您可以将 Issue 组织在与其分配的标签相对应的列表中，从而在这些列表将 Issue 可视化。

您定义流程，我们会为您进行组织：您添加标签，然后创建相应的列表以提取现有 Issue。准备就绪后，可以将 Issue 从一个步骤拖放到下一个步骤。

[![GitLab issue board - Core](/docs/img/issue_boards_core.png)](/docs/img/issue_boards_core.png)

### 看板的功能[](#advanced-features-of-issue-boards "Permalink")

*   每个项目创建多个看板

## 工作方式[](#how-it-works "Permalink")

看板功能通过将 CODEChina 现有的[发行跟踪功能](/docs/user/project/issues.md#issues-list)和[标签](/docs/user/project/label.md)用作 Scrum 板的列表而建立。

使用看板，您可以对 Issue 有不同的看法，同时保持在问题跟踪器中看到的相同过滤和排序功能。看板基于其项目的标签结构，因此它使用相同的描述性标签来指示在板上的位置，从而在整个开发生命周期中保持一致性。

问题板向您显示团队正在处理的问题，分配给每个人的问题以及这些问题在工作流中的位置。

从创建 Issue，托管代码，执行审阅，构建，测试和部署这些您都可以再一个平台完成，看板可帮助您在 CODEChina 中可视化和管理整个过程。

## 用户示例[](#use-cases "Permalink")

有多种方法可以使用针对自己喜欢的工作流程量身定制看板，一下是看板的一些常见用例：

### 单个看板示例[](#use-cases-for-a-single-issue-board "Permalink")

借助 CODEChina 工作流程，您可以讨论 Issue 中的提案，使用标签对其进行分类，然后在其中使用问题委员会进行组织并确定优先级。

例如，让我们考虑以下简化的开发工作流程：

1.  您有一个托管应用程序代码库的代码仓库，您的团队成员正在积极贡献代码
2.  您的**后端**团队将开始新的实施工作，收集反馈和批准，并将其传递给**前端**团队
3.  前端完成后，新功能将部署到要测试的**预发布**环境中
4.  成功后，它将部署到**生产** 环境

如果您具有标签" **后端** "，" **前端** "，" **暂存** "和" **生产** "，以及带有每个列表的看板，则可以：

*   可视化从开发生命周期开始到部署到生产的整个实现流程
*   通过垂直移动优先顺序排列列表中的 Issue
*   在列表之间移动 Issue，以根据您设置的标签进行整理
*   通过选择一个或多个现有 Issue，将多个 Issue 添加到看板的列表中

[![issue card moving](/docs/img/issue_board_move_issue_card_list.png)](/docs/img/issue_board_move_issue_card_list.png)

### 多个看板示例[](#use-cases-for-multiple-issue-boards "Permalink")

借助[多个看板](#multiple-issue-boards) ，每个团队可以拥有自己的看板来单独组织其工作流程。

#### Scrum team[](#scrum-team "Permalink")

每个团队只有一个看板，现在您可以在流程的每个部分中解决 Issue，例如： **To Do** ， **Doing**和**Done** 。

#### 组织讨论[](#organization-of-topics "Permalink")

创建列表以按主题对 Issue 进行排序，并快速在主题或组织之间（例如**UX** ， **Frontend**和**Backend**之间）进行更改。更改反映在各个方面，因为更改列表会相应更新每个 Issue 的标签。

#### 高级团队移交[](#advanced-team-handover "Permalink")

例如，假设我们有一个 UX 小组，其看板包含：

*   **Todo**
*   **Doing**
*   **Frontend**

完成操作后，他们将卡移至**Frontend** ，前端团队的看板看起来像：

*   **Frontend**
*   **Doing**
*   **Done**

由 UX 团队**整理的**卡片准备就绪后，会自动显示在" **前端"**列中。

**注意：**有关更广泛的用例，请参阅博客文章[GitLab 工作流程，概述](https://about.gitlab.com/blog/2016/10/25/gitlab-workflow-an-overview/#gitlab-workflow-use-case-scenario)；对于一个真实的用例示例，您可以了解为什么[Codepen 决定采用发行版](https://about.gitlab.com/blog/2017/01/27/codepen-welcome-to-gitlab/#project-management-everything-in-one-place)来改善多个[发行版](https://about.gitlab.com/blog/2017/01/27/codepen-welcome-to-gitlab/#project-management-everything-in-one-place)的工作流程。

#### 快速指派[](#quick-assignments "Permalink")

为每个团队成员创建列表，然后将 Issue 快速拖放到每个团队成员的列表中。

## 看板术语[](#issue-board-terminology "Permalink")

**看板**代表您的** Issue **的独特视图。它可以有多个列表，每个列表由卡代表的 Issue 组成。

**列表**是问题板上的一列，显示与某些属性匹配的问题。除了默认的"打开"和"关闭"列表外，每个其他列表还显示与您选择的标签匹配的问题，在每个列表的顶部，您可以看到属于该问题的数量。列表类型包括：

*   **开** （默认）：不属于其他列表中的一个所有打开的问题， 始终显示为最左边的列表
*   **已关闭** （默认）：所有已关闭的问题，始终显示为最右边的列表
*   **标签列表** ： **标签的**所有未解决问题

**卡**是列表中的一个框，它代表一个 Issue，您可以将卡片从一个列表拖动到另一个列表，以更改其标签，卡上显示的信息包括：

*   Issue 标题
*   相关标签
*   Issue 数量
*   指派人

## 权限[](#permissions "Permalink")

具有[报告者和更高角色的](/docs/user/permissions.md)用户可以使用看板的所有功能来创建或删除列表，并将问题从一个列表拖动到另一个列表。

### 多看板[](#multiple-issue-boards "Permalink")

多看板允许给定项目或组使用多个看板，对于具有多个团队的大型项目，或者在使用代码仓库托管多个产品代码的情况下，这将非常有用。

使用菜单顶部的搜索框，您可以过滤列出的看板。

当您有十个或更多的板可用时，菜单中还会显示**最近**部分，其中包含最后四个被访问板的快捷方式。

当您在具有多个看板的项目或组中重新访问看板时，系统会自动加载您上次访问的板。

#### 创建看板[](#create-an-issue-board "Permalink")

可以通过以下步骤创建新的看板：

1.  点击"看板"页面左上角的具有当前板名称的下拉菜单
2.  点击 **创建新板**
3.  输入新板的名称

#### 删除看板[](#delete-an-issue-board "Permalink")

要删除当前活动的看板：

1.  单击"发行板"页面左上角的具有当前板名称的下拉菜单
2.  单击**删除看板**
3.  单击**删除**进行确认

### 全屏模式[](#focus-mode "Permalink")

单击右上角的按钮可打开和关闭全屏模式，在全屏模式下，导航 UI 处于隐藏状态，使您可以集中精力处理板上的问题。

## Blocked issues[](#blocked-issues "Permalink")

如果一个问题被另一个问题阻止，则其标题旁边会出现一个图标，指示其阻止状态。

[![Blocked issues](/docs/img/b1edf28a1aa5c59ffa779a574c4fc548.png)](/docs/img/issue_boards_blocked_icon_v12_8.png)

## 看板可进行的操作[](#actions-you-can-take-on-an-issue-board "Permalink")

    *   [新建列表](#create-a-new-list)
    *   [删除列表](#delete-a-list)
    *   [添加 Issue](#add-issues-to-a-list)
    *   [从列表中移除 Issue](#remove-an-issue-from-a-list)
    *   [筛选](#filter-issues)出现在问题板上的问题
    *   [拖动 Issue](#drag-issues-between-lists)
    *   [选择多个卡片](#multi-select-issue-cards)
    *   [在列表中排序](#issue-ordering-in-a-list)
    *   拖动列表并重新排序
    *   更改问题标签（通过在列表之间拖动问题）
    *   解决问题（将其拖动到" **完成"**列表中）

如果您无法执行上述某些操作，请确保您具有正确的[权限](#permissions) 。

### 初次使用看板[](#first-time-using-an-issue-board "Permalink")

第一次打开看板时，会显示默认列表（" **打开"**和" **关闭"** ）以及欢迎消息，其中提供了两个选项，您可以：

*   创建一组预定义的标签（默认情况下： **To Do**和**Doing** ），并在看板创建其对应的列表
*   退出并使用自己的列表

[![issue board welcome message](/docs/img/issue_board_welcome_message.png)](/docs/img/issue_board_welcome_message.png)

如果选择使用并创建预定义列表，则它们将显示为空，因为与它们关联的标签要到那时才存在，这意味着系统无法自动填充它们。当然，如果标签存在的话，则会创建该列表，并填充具有该标签的问题。

### 新建列表[](#create-a-new-list "Permalink")

通过单击看板右上角的**添加列表**按钮来创建新列表。

然后，选择标签以从中创建列表，新列表将被插入列表的末尾，在**完成**之前。移动和重新排序列表就像拖动列表一样简单。

要为尚不存在的标签创建列表，请选择**创建新标签**来**创建标签**，这将立即创建标签并将其添加到下拉列表中。现在，您可以选择它来创建列表。

### 删除列[](#delete-a-list "Permalink")

要从看板上删除列表，请使用列表标题中的删除图标，将出现一个确认对话框供您确认删除操作。

删除列表对 Issue 和标签没有任何影响，只是删除了列表视图。如果需要，您随时可以将其添加回去。

### 添加问题到列表[](#add-issues-to-a-list "Permalink")

您可以通过单击**看板**右上角的**添加问题**按钮将 Issue 添加到列表中，这将打开一个模式窗口，您可以在其中查看不属于任何列表的所有问题。

通过单击卡片选择一个或多个问题，然后单击" **添加问题"**以将其添加到所选列表中，您可以通过按标签筛选来限制要添加到列表中的问题。

### 从列表中移除 Issue[](#remove-an-issue-from-a-list "Permalink")

从列表中删除 Issue 可以通过单击卡片，然后单击侧边栏中的**从**面板中**删除**按钮来完成，相应的标签被删除。

### 过滤 Issue[](#filter-issues "Permalink")

你应该能够使用问题板顶部的过滤器来只显示你想要的结果。这与问题跟踪程序中使用的过滤类似，因为问题和标签中的元数据在问题板中重复使用。

### 创建工作流[](#create-workflows "Permalink")

通过对列表重新排序，可以创建工作流程。由于看板的列表基于标签，因此可以与您现有的看板一起使用。因此，如果您已经用"后端"和"前端"标记了事物，则问题在创建它们时会出现在列表中。此外，这意味着您可以通过更改标签轻松地在列表之间移动某些内容。

使用看板的典型工作流程为：

1.  您已经[创建了](/docs/user/project/label.md#label-management)标签并对其进行了[优先排序](/docs/user/project/label.md#label-priority)以便可以轻松地对问题进行分类
2.  您遇到很多问题（理想情况下是带有标签的）
3.  您访问看板并开始[创建列表](#create-a-new-list)以创建工作流程
4.  您可以在列表中四处移动问题，以便您的团队知道谁应该处理什么问题
5.  当一个团队的工作完成时，可以将问题拖到下一个列表中，以便其他人来接手
6.  最终解决问题后，该问题将移至" **完成"**列表并自动关闭

例如，您可以基于"前端"标签和"后端"标签创建一个列表，设计师可以通过将问题添加到"前端"列表来开始处理问题。这样，每个人都知道设计师现在正在处理该问题。然后，一旦完成，设计师所要做的就是将其拖到下一个列表"后端"，后端开发人员最终可以在该列表中进行选择。完成后，将其移至**完成** ，以解决问题。

访问问题时可以清楚地看到此过程，因为每次移动到另一个列表时，标签都会更改，并且会被记录系统。

### 在列表间拖动问题[](#drag-issues-between-lists "Permalink")

在列表之间拖动问题时，根据源列表和目标列表，会发生不同的行为：

|   | 打开 | 要关闭 | 标记`B`列表 | 分配受让人`Bob`清单 |
| --- | --- | --- | --- | --- |
| 从开放 | - | 问题已结案 | `B` added | `Bob` assigned |
| 从关闭 | 问题重新开放 | - | 问题重新开放
`B`添加 | 问题重新开放
`Bob`分配 |
| 从标签`A`列表 | `A` removed | 问题已结案 | `A` removed
`B` added | `Bob` assigned |
| 从受让人`Alice`名单 | `Alice` unassigned | 问题已结案 | `B` added | `Alice` unassigned
`Bob` assigned |

### 选择多个问题卡片[](#multi-select-issue-cards "Permalink")

您可以选择多个问题卡片，然后将组拖动到列表中的另一个位置或另一个列表中。这样可以更快地一次重新排序许多问题。

要选择并移动多张问题卡片：

1.  在 Windows 或 Linux使用`Ctrl`选择每个卡+ `Click`，或者在 MacOS 使用`Cmd` + `Click`
2.  将所选卡中的一张拖到另一个位置或列表，所有所选卡都将移动

### 列表中对问题排序[](#issue-ordering-in-a-list "Permalink")

访问看板时，问题在任何列表中都显示为有序。您可以通过拖放问题来更改顺序，更改后的顺序将保存到系统中，以便以后访问同一板的任何人都可以看到新的排序结果，但也有一些例外：

给定问题首次出现在任何面板中（即用户首次加载包含该问题的面板）时，将根据[优先级顺序](/docs/user/project/label.md#label-priority)对该列表中的其他问题进行[排序](/docs/user/project/label.md#label-priority) 。

此时，系统会为该问题分配一个相对顺序值，该值代表其相对于列表中其他问题的相对顺序，每当您拖放该问题的重新排序时，其相对顺序值都会相应更改。

同样，当问题由用户加载时，在任何板上出现的任何时间，都会使用更新的相对顺序进行排序（这是第一次出现从上述优先顺序中提取问题的问题）。这意味着，如果您给定板上的任何用户将问题`A`拖放到问题`B`上方的顺序进行了重新排序，每当随后将这两个问题加载到任何板（例如，可以是不同的项目板或不同的组板）中时，都将维持该排序。

此顺序还会影响[问题列表](/docs/user/project/issues/sort.md) ，在看板上更改排序会更改发行列表中的顺序，反之亦然。

## Tips[](#tips "Permalink")

需要记住的几件事：

*   在列表之间移动问题会从其来源列表中删除标签，并从其去往列表中添加标签
*   如果一个问题有多个标签，则它可以存在于多个列表中
*   如果标记了问题，则会自动用问题填充列表
*   单击卡片内的问题标题，将您转到该问题
*   单击卡内的标签可快速筛选整个问题板，并仅显示所有带有该标签的列表中的问题
*   出于性能和可见性的原因，每个列表默认显示前 20 个问题。如果问题超过 20 个，请开始向下滚动，然后出现下 20 个问题