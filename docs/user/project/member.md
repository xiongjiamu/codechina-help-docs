# 项目成员[](#member "Permalink")

您可以在所有项目中管理组和用户及其访问级别，您还可以个性化为每个项目赋予每个用户的访问级别。

您应该具有 Maintainer 或 Owner[权限](/docs/user/permissions.md)，才能将新用户添加或导入到项目中。

要查看，编辑，添加和删除项目的成员，请转到项目的**项目设置>项目成员设置** 。

## 继承的用户[](#inherited-membership "Permalink")

当您的项目属于某个组织时，组织成员将从该组继承该项目的成员资格和权限级别。

[![Project members page](/docs/img/project_members.png)](/docs/img/project_members.png)

从上图可以得出以下几点：

*   有 3 个成员可以访问该项目
*   User0 是记者，并且已从包含当前项目的组`demo`继承了他们的权限
*   对于 User1，没有组的指示，因此它们直接属于我们正在检查的项目
*   管理员是**所有**组的所有者和所有者，所以有提示表明其在父组织和继承的所有者权限

您可以使用右侧的下拉列表过滤此列表：

[![Project members filter](/docs/img/project_members_filter_v12_6.png)](/docs/img/project_members_filter_v12_6.png)

*   **仅显示直接成员**仅显示 User1
*   **仅显示继承的成员将**显示 User0 和 Administrator

## 添加成员[](#add-a-user "Permalink")

点击 **邀请用户** 按钮，在弹窗中按要求设置好用户、权限及访问过期时间(可选)。

[![Search for people](/docs/img/add_user_search_people.png)](/docs/img/add_user_search_people.png)

选择用户以及您要赋予该用户的[权限级别](/docs/user/permissions.md)，您可以选择多个用户。

[![Give user permissions](/docs/img/add_user_give_permissions.png)](/docs/img/add_user_give_permissions.png)

完成后，点击**邀请** ，这些**用户**将立即使用您在上面授予他们的权限添加到您的项目中。

[![List members](/docs/img/add_user_list_members.png)](/docs/img/add_user_list_members.png)

现在，您可以删除现有用户或更改其对项目的访问级别。

## 导入用户[](#import-users-from-another-project "Permalink")

您可以通过单击 **导入**按钮，将另一个项目的用户导入您自己的项目中。

在下拉菜单中，您只能看到您具有 maintainer 权限的项目。

选择需要导入的组织，然后单击**导入项目成员**，将会出现一条简短的消息，通知您导入已成功，并且新成员现在位于项目的成员列表中。请注意，导入的成员将保留他们在原项目中的权限。

## 申请项目权限[](#project-membership-and-requesting-access "Permalink")

项目所有者可以：

*   允许非项目成员请求访问该项目
*   防止非项目成员请求访问

可以进入**项目设置 > 可见性，项目功能，权限**然后单击**允许用户请求访问权限** 启用该设置。

CODEChina 用户可以请求成为项目成员，进入到您要加入的项目，然后单击项目名称右侧的" **申请权限"按钮。

申请权限后：

*   将通过电子邮件向最多十个项目 maintainer 通知该请求，电子邮件被发送给最近活跃的 maintainer
*   任何项目 maintainer 都可以在成员页面上批准或拒绝该请求

**注意：**如果项目没有任何 maintainer，则将通知发送给该项目组的最近活跃的 owner。

如果您在批准请求之前改变主意，只需单击" **撤回访问请求"**按钮。

## 与组共享项目[](#share-project-with-group "Permalink")

此外，您可以[与整个组共享一个项目](/docs/user/project/member/share.md)，而不需要一个一个地添加用户。

## 从项目中删除成员[](#remove-a-member-from-the-project "Permalink")

只有[Owner](/docs/user/permissions.md#group-members-permissions)权限的[用户](/docs/user/permissions.md#group-members-permissions)才能管理项目成员。

如果要删除的成员在项目中具有直接成员资格，则可以从项目中删除用户；如果成员资格是从父组继承的，则该成员只能从父组本身中删除。

删除成员时，您可以决定是从所已经分配给当前用户的 Issue 及合并请求中取消分配，还是保留分配。

*   当用户离开私有项目并且您希望撤消他们对所有问题和已分配的合并请求的访问时，从所有问题和合并请求中**取消分配已删除的成员**可能会有所帮助
*   **保留问题和合并请求的分配**可能对于接受公共贡献的项目很有帮助，在这些项目中，用户不必成为成员就可以为问题和合并请求做出贡献

通过以下步骤可以在项目中删除一个成员:

1.  在一个项目中，进入到 **项目设置 > 项目成员设置**页
2.  点击**删除** 要删除的项目成员旁边的按钮，将出现" **删除成员"**弹窗
3.  （可选）选中" **也从相关问题中取消分配此用户并合并请求"**复选框
4.  单击 **删除成员**即可