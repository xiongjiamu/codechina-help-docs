# 搜索[](#搜索 "Permalink")

## Issues 及合并请求[](#issues-and-merge-requests "Permalink")

如果要在多个项目的 Issue 或合并请求中搜索的话，可以使用屏幕左上角的" **Issue"**或" **合并请求"**链接（需要登录）。

由于 Issue 及合并请求的工作方式基本一致，因此以下说明两者均适用。

点击**Issue**时 ，您会立即看到分配给您的未解决 Issue：

[![Issues assigned to you](/docs/img/issues_assigned_to_you.png)](/docs/img/issues_assigned_to_you.png)

您可以浏览 **开放中**, **已关闭**, 或 **全部** issues。

您还可以使用搜索、过滤器字段对结果进行过滤，如下面的[过滤 Issue 及合并请求列表中所述](#filtering-issue-and-merge-request-lists) .

### 由您创建或分配给您的 Issue 及合并请求[](#issues-and-mrs-assigned-to-you-or-created-by-you "Permalink")

您还可以在屏幕上方的搜索框中找到由您创建或分配给您的 Issue 及合并请求的快捷入口：

[![shortcut to your issues and mrs](/docs/img/issues_mrs_shortcut.png)](/docs/img/issues_mrs_shortcut.png)

### Issue 或合并请求列表过滤[](#filtering-issue-and-merge-request-lists "Permalink")

请可以参考下步骤对项目和组织中的" **Issue**及**合并请求"**列表进行过滤筛选：

1.  单击字段**搜索或过滤结果…** 
2.  在出现的下拉菜单中，选择您要过滤的属性：
    *   作者
    *   指派人
    *   [里程碑](/docs/user/project/milestone.md)
    *   Release
    *   [标签](/docs/user/project/label.md)
    *   我的反应
    *   机密
    *   Epic
    *   关键词
3.  选择或键入用于过滤属性的运算符， 可以使用以下运算符：
    *   `=` ：是
    *   `!=` ：不是
4.  输入文本以按[过滤属性](#filters-autocomplete) 
5.  重复此过程以按多个属性对结果进行过滤筛选， 可通过逻辑`AND` 添加多个属性

例如，按作者`=` Jane 和 Milestone `!=` 12.6 进行过滤，以解决 Jane 是作者而里程碑不是 12.6 的问题.

[![filter issues in a project](/docs/img/issue_search_filter_v12_7.png)](/docs/img/issue_search_filter_v12_7.png)

### 按 **无** / **任何**过滤[](#filtering-by-none--any "Permalink")

一些过滤字段（例如里程碑和指派人）允许您按**无**或**任何**进行过滤。

[![filter by none any](/docs/img/issues_filter_none_any.png)](/docs/img/issues_filter_none_any.png)

选择" **无"**将返回该字段为空值的结果，即没有里程碑或没有指派人；

选择" **任意** "则相反，它返回该字段具有非空值的结果。

### 搜索特定内容[](#searching-for-specific-terms "Permalink")

您可以按标题或说明中包含的特定内容过滤 Issue 及合并请求。

*   语法
    *   以任何顺序搜索查找的单词，例如：搜索 Issue 以寻找`display bug` ，将以任何顺序返回匹配这两个单词的所有 Issue；
    *   要精确的查找内容，请使用双引号： `"display bug"`。
*   限制
    *   出于性能原因考虑，少于 3 个字符的单词将被忽略。 例如：在 Issue 中搜索`included in titles`与搜索`included titles`是一样的；
    *   每个查询只能搜索 4096 个字符或 64 个字词

### 按序号过滤[](#filtering-by-id "Permalink")

您可以按 ID 将" **问题"**列表过滤到单个实例。例如，输入过滤器`#10`仅返回问题#10；这同样适用于" **合并请求"**列表， 输入过滤器`#30`仅返回合并请求#30.

## 自动填充[](#filters-autocomplete "Permalink")

在许多页面（如 Issue，合并请求，Epic等）中提供了许多过滤器，您可以使用它们来缩小搜索范围。使用过滤器功能时，可以开始键入字符以显示相关用户或其他属性。

为了优化性能，至少需要三个字符才能开始搜索。例如，如果您要搜索指派人为" Simone Presley"的 Issue，则您需要至少输入" Sim"，然后系统才能自动完成并给出相关结果。

## 搜索历史记录[](#search-history "Permalink")

您可以通过单击搜索条左侧的下拉框来查看最近的搜索，单击搜索条目可以再次进行该搜索。此功能可用于 Issue 及合并请求，搜索结果存储在本地浏览器中。

[![search history](/docs/img/search_history.gif)](/docs/img/search_history.gif)

## 移除过滤条件[](#removing-search-filters "Permalink")

单击过滤器的（x）按钮或敲入退格键可以删除单个过滤器，整个搜索过滤器可以通过点击搜索框的（X）按钮，或通过`⌘`键`（Mac）+⌫`来清除。

如果要一次删除一个过滤条件，可以使用`⌥` （Mac）/ `Ctrl` + `⌫`键盘组合.

## 重复使用同一过滤条件[](#filtering-with-multiple-filters-of-the-same-type "Permalink")

某些过滤条件可以多次添加，包括但不限于指派人和标签。相同类型的多个过滤条件在使用通过"与"逻辑连接。例如，如果您要过滤`assignee:@sam assignee:@sarah` ，那么您的结果将仅包含分配给 Sam 和 Sarah 的内容。

## 快捷搜索入口[](#shortcut "Permalink")

您还可以在项目仪表板上方的搜索框中找到搜索的快捷入口，以快速访问在该项目的 Issue 或合并请求中由您创建或分配给您的内容：

## 待办事项[](#to-do-list "Permalink")

可以通过"待办事项"和"完成"来搜索您的[待办事项列表](/docs/user/todo.md) 。您可以按项目，作者，类型和操作[过滤](/docs/user/todo.md#filtering-your-to-do-list)它们。另外，您可以按[**标签优先级**](/docs/user/project/label.md#label-priority) ， **最后创建**和**最早创建**对其进行排序。

## 项目[](#projects "Permalink")

您可以从导航中项目菜单栏去搜索和发现项目，方法是依次点击**项目>浏览项目** ， 在" **按名称过滤** "字段上，输入要查找的项目或组织名称即可。

你也可以去找你的项目[ Star ](/docs/basic/create-project.md#star-a-project) （ **加星标的项目** ），并**探索**所有的公共和内部项目 GitLab.com 可用，从中你可以通过可视性筛选，通过**趋势** ，最好与**大多数明星**评分，或他们的**全部** .

您还可以按**名称** ， **最后创建** ， **最旧创建** ， **最后更新** ， **最新更新** ， **所有者**对搜索结果中的项目进行排序，并选择隐藏或显示**已归档的项目** 。

## 组织[](#org "Permalink")

与[项目搜索](#projects)类似，你可以通过导航中组织菜单栏去搜索和发现组织。

在" **按名称过滤** "字段上，输入要查找的组名，在您键入时为您过滤它们。

您也可以**浏览**所有的公共组织，您可以按照**最新创建的** ， **最早建立** ， **最后更新** ，或**最早的更新** 进行筛选过滤。

## 看板[](#issue-boards "Permalink")

在[看板](/docs/user/project/kanban.md) 中，您可以按**作者** ， **指派人** ， **里程碑**和**标签**过滤 Issue。您还可以从键入时加载的字段中**按名称过滤** 。

当您要添加**Issue**到看板中以便在看板中搜索时，请点击屏幕右上角的**添加 Issue**按钮，除了按**名称**过滤它们之外，您还可以从中找到一个模式窗口**作者** ， **受让人** ， **里程碑**和**标签** ，选择多个问题以添加到您选择的列表中。

## 高级全局搜索[](#advanced-global-search-starter "Permalink")

利用 Elasticsearch 进行更快，更高级的代码搜索。

## 高级语法搜索[](#advanced-syntax-search-starter "Permalink")

使用高级语法搜索可获得更具针对性的搜索结果。
