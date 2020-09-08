# 截止日期[](#due-date "Permalink")

截止日期在 Issue 中可用于跟踪 deadlines 以确保功能的按期交付。您至少需要 Reporter 权限才可以编辑截止日期，但任何具有 Issue 查看权限的用户都可以看到截止日期。

## 设置截止日期[](#setting-a-due-date "Permalink")

创建或编辑 Issue 时，您可以点击**截止日期**字段，然后出现一个日历来帮助您选择所需的日期。要删除日期，请选择日期文本并将其删除即可。该日期的时区与服务器的时区有关，与用户的时区无关。

您还可以通过 Issue 侧边栏设置截止日期。在 Issue 详情页的右侧找到**截止日期**，然后单击**编辑**以选择截止日期或删除现有的日期，您所作的更改将立即保存。

设置截止日期的最后一种方法是直接在 Issue 的描述或评论中使用[快速操作](/docs/user/project/quick-actions.md) ：

*   `/due <date>` ：设置到期日， 有效的`<date>`示例包括`in 2 days` 、`this Friday`和`December 31st` 
*   `/remove_due_date` ：删除到期日

## 截止日期的用法[](#making-use-of-due-dates "Permalink")

设置了截止日期的 Issue 可以在 Issue 跟踪器中轻松查看到，并在它们旁边显示了截止日期，日期过期的 Issue 会将图标和日期显示为红色。您可以从右侧的下拉菜单中按截止日期倒叙/顺序对 Issue 进行排序。

截止日期也会出现在您的[待办事项清单中](/docs/user/todo.md) .

未解决 Issue 在截止日期的前一天，系统将向该 Issue 的所有参与者发送电子邮件，与截止日期一样，"截止日期前的一天"由服务器的时区来确定。

截止日期的问题也可以导出为 iCalendar，可以将 URL 添加到日历应用 app 中。通过单击以下页面上的**订阅日历**按钮可以访问该 URL：

*   在**分配的 Issue **页面上，链接在该页面的右上方
*   在**项目 Issue **页面上
