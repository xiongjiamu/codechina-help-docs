# Draft[](#draft "Permalink")

如果合并请求尚未准备好进行合并（可能是由于持续的开发或需要开放讨论），则可以将其标记为**Draft**来阻止在合并之前接受该合并请求，**Draft**合并请求的"合并"按钮将会被禁用，从而防止其被合并，并且在删除"**Draft: / WIP:**"标志之前它将一直保持禁用都状态。

[![Blocked Merge Button](/docs/img/draft_blocked_merge_button_v13_2.png)](/docs/img/draft_blocked_merge_button_v13_2.png)

## 给合并请求添加 Draft/WIP 标记[](#adding-the-draft-flag-to-a-merge-request "Permalink")

对在进行中（WIP）合并请求可以添加** Draft: **或** WIP: ** 的标记。具体的添加方式如下：

*   将`[Draft]` ， `Draft:`或`(Draft)`到合并请求标题的开头，单击标题框下的" **以草稿开始标题：** "，在编辑合并请求的描述时将具有相同的效果
*   **不推荐使用**将`[WIP]`或`WIP:`添加到合并请求标题的开头，**WIP**仍然有效，但我们推荐使用**Draft**
*   在合并请求的讨论中添加`/wip` [快速操作](/docs/user/project/quick-actions.md#quick-actions-for-issues-merge-requests-and-epics)注释 ，可以重复进行并切换合并请求的状态。请注意，注释中的任何其他文本都将被丢弃
*   将`draft:`或`Draft:`添加到针对合并请求的源分支的提交消息的开头，这不会切换合并请求的状态，并且在另一次提交中再次执行将无效

## 移除合并请求中的 Draft/WIP 标记[](#removing-the-draft-flag-from-a-merge-request "Permalink")

与上述类似，当准备合并请求时，可以通过以下几种方式移除" `Draft`标记：

*   从合并请求标题的开头删除`[Draft]` ， `Draft:`或`(Draft)` ，在编辑合并请求的描述时，在标题框下单击**从标题中删除草稿：前缀** ，将具有相同的效果
*   在合并请求的讨论中添加`/wip` [快速操作](/docs/user/project/quick-actions.md#quick-actions-for-issues-merge-requests-and-epics) 注释，可以重复进行并切换合并请求的状态。请注意，注释中的任何其他文本都将被丢弃
*   点击靠近合并请求描述底部的*移除 WIP 状态**按钮，该按钮对至少具有 Developer 权限的用户才可见

## 通过 WIP 过滤合并请求[](#includingexcluding-wip-merge-requests-when-searching "Permalink")

查看/搜索合并请求列表时，可以通过在搜索框中添加" WIP"过滤器，然后选择"是"（包括）或"否"（排除）来选择包括或排除 WIP 合并请求 