# 待办事项[](#待办事项 "Permalink")

当您登录到 CODEChina 时，通常需要看一下哪些内容需要花费较多时间、开始干活或知道需要注意的是哪些，而无需理会大量的电子邮件通知。这里是您工作的地方，因此能够快速下手开展工作尤为重要。待办事项就是这样一个工具，它在一个简单的仪表板中按时间顺序列出了等待您处理的内容。

[![To Do screenshot showing a list of items to check on](/docs/img/todos_index.png)](/docs/img/todos_index.png)

通过单击顶部导航右上角的对勾图标，可以快速访问待办事项列表. 如果计数为：

*   小于 100 的蓝色数字是待办事项的数量
*   大于或等于 100，则数字显示为 99+， 确切的数字显示在"任务列表"上

[![To Do icon](/docs/img/todos_icon.png)](/docs/img/todos_icon.png)

## 待办事项类型[](#what-triggers-a-to-do "Permalink")

在以下情况下，待办事项会显示在您的待办事项列表中：

*   分配给您的 Issue 或合并请求
*   在以下内容的描述或评论中`@到您`：
    *   Issue
    *   合并请求 
    *   Epic
*   在以下评论中`@到您`：
    *   提交
    *   设计
*   您的合并请求的 CI/CD pipeline 失败
*   当一个打开的合并请求冲突了，并且满足以下条件之一：
    *   你是作者
    *   是由您将其设置为在 pipeline 成功后自动合并的

待办事项触发器不受[通知电子邮件设置的影响](/docs/user/account/email-notify.md) 。

**注意：**当用户不再有权访问与待办事项相关的资源（例如 Issue，合并请求，项目或组织）时，出于安全原因，相关的待办事项将在一小时内删除。为了防止用户的权限被错误地收回导致数据丢失，删除操作会延迟处理。

### 直接处理[](#directly-addressing-a-to-do "Permalink")

如果在一行的开头直接@您，则您收到的待办事项将列为"直接处理"。比如在下面的这个评论内容中：

```
@alice What do you think? cc: @bob
 - @carol can you please have a look?
 >>>
@dan what do you think?
>>>

@erin @frank thank you!
```

接收直接处理的待办事项的人是`@alice` ， `@erin`和`@frank` 。直接处理的待办事项仅在过滤的时候会有所不同，其他时候在显示上并无差异。

### 手动新建待办事项[](#manually-creating-a-to-do "Permalink")

您还可以通过在以下位置单击" **添加待办事项"**按钮，将以下内容添加到"待办事项列表"中：

*   Issue
*   合并请求

[![Adding a To Do from the issuable sidebar](/docs/img/todos_add_todo_sidebar.png)](/docs/img/todos_add_todo_sidebar.png)

## 标记已完成[](#marking-a-to-do-as-done "Permalink")

针对下面任务采取的任何措施都会将相应的待办事项标记为已完成：

*   Issue
*   合并请求

取消待办事项的动作包括：

*   更换指派人
*   更改里程碑
*   添加/删除标签
*   对 Issue 发表评论

您的待办事项列表只有自己能看到，只有您自己的行为才会将其标记为已完成。如果您关闭了 Issue 或合并请求，那么您的待办事项也会自动标记为已完成。

为防止其他用户在不通知您的情况下关闭问题，当其他人关闭 Issue、合并或对以下任何一项采取了措施，则您的待办事项将保持待处理状态：

*   Issue
*   合并要求

每种任务只会产生一个待办事项，因此即使在一个问题中提到用户一百次也只会触发一个待办事项。

如果不需要做任何处理，您可以通过单击相应的**完成**按钮来手动将"待办事项"标记为已完成，它也将从您的"待办事项列表"中消失。

[![A To Do in the To-Do List](/docs/img/todos_todo_list_item.png)](/docs/img/todos_todo_list_item.png)

您还可以通过单击以下边栏中的" **标记为已完成**按钮将"待办事项" **标记为已完成** ：

*   Issue
*   合并请求

[![Mark as done from the issuable sidebar](/docs/img/todos_mark_done_sidebar.png)](/docs/img/todos_mark_done_sidebar.png)

您可以通过单击**全部标记为已完成**按钮将所有待办事项**标记为已完成** 。

## 过滤待办事项[](#filtering-your-to-do-list "Permalink")

您可以在待办事项列表中使用以下四种过滤器：

| 过滤条件 | 描述 |
| --- | --- |
| 按项目 | 按项目筛选 |
| 按组织 | 按组织筛选 |
| 按作者 | 按触发待办事项的作者过滤 |
| 按类型 | 按 Issue，合并请求，设计 |
| 按动作 | 按触发待办事项的动作过滤 |

您还可以同时按多个过滤条件之一进行过滤，[上面描述了](#what-triggers-a-to-do)可能的操作，包括：

*   任何行动
*   被指派
*   被@
*   添加
*   Pipelines
*   直接处理