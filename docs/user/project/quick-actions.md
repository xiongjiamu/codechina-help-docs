# 快速操作[](#quick-actions "Permalink")

快速操作是针对 Issue 、Epic、合并请求和提交的常见操作的文本快捷方式，通常可通过在 CODEChina 用户界面中单击按钮或下拉菜单来完成。您可以在 Issue、史诗、合并请求和提交的说明中或讨论中输入这些命令，每个命令应放在单独的行上，以便正确检测和执行。

## Issue、合并请求及 Epic 的快速操作[](#quick-actions-for-issues-merge-requests-and-epics "Permalink")

以下快速操作适用于其中的描述，讨论和评论部分：

*   Issues
*   合并请求
*   Epics

| 命令 | Issue | 合并请求 | Epic | Action |
| --- | --- | --- | --- | --- |
| `/assign @user` | ✓ | ✓ |   | 分配一个用户|
| `/assign me` | ✓ | ✓ |   | 分配自己|
| `/award :emoji:` | ✓ | ✓ | ✓ | 切换表情符号奖|
| `/close` | ✓ | ✓ | ✓ | Close|
| `/confidential` | ✓ |   |   | 保密|
| `/copy_metadata <!merge_request>` | ✓ | ✓ |   | 从项目中的另一个合并请求中复制标签和里程碑|
| `/copy_metadata <#issue>` | ✓ | ✓ |   | Copy labels and milestone from another issue in the project|
| `/create_merge_request <branch name>` | ✓ |   |   | 从当前问题开始创建一个新的合并请求|
| `/done` | ✓ | ✓ | ✓ | 将待办事项标记为已完成|
| `/due <date>` | ✓ |   |   | 设置截止日期有效的`<date>`示例包括`in 2 days` （ `this Friday`和`December 31st` |
| `/estimate <<W>w <DD>d <hh>h <mm>m>` | ✓ | ✓ |   | 设置时间估计例如， `/estimate 1w 3d 2h 14m` |
| `/label ~label1 ~label2` | ✓ | ✓ | ✓ | 添加一个或多个标签标签名称也可以不使用波浪号（ `~` ）开头，但是不支持混合语法|
| `/lock` | ✓ | ✓ |   | 锁定螺纹|
| `/merge` |   | ✓ |   | 合并更改根据项目设置，这可能是管道成功时|
| `/milestone %milestone` | ✓ | ✓ |   | 设定里程碑|
| `/move <path/to/project>` | ✓ |   |   | 将此问题移到另一个项目|
| `/relabel ~label1 ~label2` | ✓ | ✓ | ✓ | 用指定的标签替换现有的标签|
| `/remove_due_date` | ✓ |   |   | 删除到期日|
| `/remove_estimate` | ✓ | ✓ |   | 删除时间估计|
| `/remove_iteration` | ✓ |   |   | 删除迭代（ [在 GitLab 13.1 中引入](https://gitlab.com/gitlab-org/gitlab/-/issues/196795) ） |
| `/remove_milestone` | ✓ | ✓ |   | 删除里程碑|
| `/remove_time_spent` | ✓ | ✓ |   | 消除花费的时间|
| `/remove_zoom` | ✓ |   |   | 从此问题中删除 Zoom 会议（ [在 GitLab 12.4 中引入](https://gitlab.com/gitlab-org/gitlab/-/merge_requests/16609) ）|
| `/reopen` | ✓ | ✓ | ✓ | Reopen|
| `/shrug <comment>` | ✓ | ✓ | ✓ | 将注释附加到`¯\＿(ツ)＿/¯` |
| `/spend <time(-<h>h <mm>m)> <date(<YYYY-MM-DD>)>` | ✓ | ✓ |   | 减去花费的时间（可选）指定花费时间的日期例如`/spend time(-1h 30m)`或`/spend time(-1h 30m) date(2018-08-26)` |
| `/spend <time(<h>h <mm>m)> <date(<YYYY-MM-DD>)>` | ✓ | ✓ |   | 增加花费的时间（可选）指定花费时间的日期例如`/spend time(1h 30m)`或`/spend time(1h 30m) date(2018-08-26)` |
| `/subscribe` | ✓ | ✓ | ✓ | 订阅通知|
| `/tableflip <comment>` | ✓ | ✓ | ✓ | 在`(╯°□°)╯︵ ┻━┻`添加注释|
| `/target_branch <local branch name>` |   | ✓ |   | 设置目标分支|
| `/title <new title>` | ✓ | ✓ | ✓ | 更改标题|
| `/todo` | ✓ | ✓ | ✓ | 添加待办事项|
| `/unassign` | ✓ | ✓ |   | 删除所有受让人|
| `/unlabel ~label1 ~label2` or `/remove_label ~label1 ~label2` | ✓ | ✓ | ✓ | 删除所有或特定标签|
| `/unlock` | ✓ | ✓ |   | 解锁线程|
| `/unsubscribe` | ✓ | ✓ | ✓ | 退订通知|
| `/wip` |   | ✓ |   | 切换"进行中"状态|

## 自动补全字符[](#autocomplete-characters "Permalink")

许多快速操作都需要一个参数，例如：用户名，里程碑和标签。与从列表中选择项目相比， [自动完成字符](/docs/user/project/autofill.md)可以使输入参数更加容易。

## 快速操作参数[](#quick-actions-parameters "Permalink")

设置快速操作参数的最简单方法是使用自动完成功能，如果您手动输入参数，则该参数必须用双引号（ `"` ）括起来，除非它仅包含以下字符：

1 ASCII 字母
2 数字（0-9）
3 下划线（ `_` ），连字符（ `-` ），问号（ `?` ），点（ `.` ）或`&` （ `&` ）

参数也区分大小写，自动完成功能会自动处理此问题，并自动插入引号。

## 提交消息的快速操作[](#quick-actions-for-commit-messages "Permalink")

以下快速操作适用于提交消息：

| 命令 | Action |
| --- | --- |
| `/tag v1.2.3 <message>` | 使用可选消息标记此提交 |