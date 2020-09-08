# 保护分支[](#protected-branch "Permalink")

[权限](/docs/user/permissions.md)基本上是围绕对代码仓库和分支具有读或写权限的想法定义的，为了对某些分支机加进一步的限制，可以对其进行保护。

## 概览[](#overview "Permalink")

默认情况下，受保护的分支将执行以下四个简单的操作：

*   它会阻止除具有 maintainer 权限的用户之外的所有用户创建它（如果尚未创建）
*   它可以防止除具有**允许的**权限的用户以外的其他任何人推送
*   它可以防止**任何人**强行推送分支
*   它可以防止**任何人**删除分支

## 配置保护分支[](#configuring-protected-branches "Permalink")

要保护分支，您需要至少具有 maintainer 权限级别，请注意，默认情况下`master`分支是受保护的。

1.  导航到项目的**"项目设置"➔"仓库"**
2.  滚动查找" **受保护的分支"**部分并展开
3.  从" **分支"**下拉菜单中，选择要保护的分支，然后单击" **保护"** 
4.  完成后，受保护的分支将出现在"受保护的分支"列表中

## 启用允许合并及允许推送设置[](#using-the-allowed-to-merge-and-allowed-to-push-settings "Permalink")

使用"允许推送"和"允许合并"设置，您可以控制不同角色可以在受保护分支中执行的操作。例如，您可以将"允许推送"设置为" None "，将"允许合并"设置为" developer + maintainer "，以要求*每个人都*提交合并请求，以请求更改进入受保护分支。

但是，有些工作流程不需要这样做，只有防止强行推动和移除分支才有用。对于这些工作流程，您可以通过将"允许推送"设置为" developer + maintainer "来允许具有写访问权的每个人推送到受保护的分支。

您可以在创建受保护的分支时设置"允许推送"和"允许合并"选项，也可以在之后通过从"已保护"区域的下拉列表中选择所需的选项来设置。

如果在创建受保护的分支时未选择任何这些选项，则默认情况下会将它们设置为" maintainer "。

## 通配保护分支[](#wildcard-protected-branches "Permalink")

您可以指定一个通配符保护的分支，该分支将保护所有与通配符匹配的分支。 例如：

| 通配符保护的分支 | 匹配分支 |
| --- | --- |
| `*-stable` | `production-stable`, `staging-stable` |
| `production/*` | `production/app-server`, `production/load-balancer` |
| `*gitlab*` | `gitlab`, `gitlab/staging`, `master/gitlab/production` |

受保护的分支设置（如" developer 可以推送"）适用于所有匹配的分支。

两个不同的通配符可能会匹配同一分支。例如， `*-stable` `production-stable`和`production-*`都将与`production-stable`分支匹配，在这种情况下，如果*这些*受保护的分支有这样一个设定"允许推送"，然后`production-stable`也将继承这一设置。

如果单击受保护分支的名称，将显示所有匹配分支的列表。

## 新建保护分支[](#creating-a-protected-branch "Permalink")
 
当受保护的分支或通配符受保护的分支设置为" [**不允许任何人** **推送"时**](#using-the-allowed-to-merge-and-allowed-to-push-settings) ，只要允许 developer（和具有较高[权限级别的](/docs/user/permissions.md)用户）[**合并**](#using-the-allowed-to-merge-and-allowed-to-push-settings) ，就可以创建新的受保护分支。

可以通过用户界面创建新分支：

1.  打开**代码>分支**
2.  单击**新建分支**
3.  填写分支名称，然后选择一个现有的分支，新分支将基于该分支。仅接受现有的受保护分支和已经在受保护分支中的提交。

## 删除保护分支[](#deleting-a-protected-branch "Permalink")

有时可能需要删除或清理受保护的分支，具有[ maintainer ](/docs/user/permissions.md)并具有[ maintainer ](/docs/user/permissions.md)用户可以通过 Web 界面手动删除受保护的分支：

1.  打开**代码>分支**
2.  单击您要删除的分支旁边的删除图标
3.  为了防止意外删除，需要额外的确认

    [![Delete protected branches](/docs/img/protected_branches_delete.png)](/docs/img/protected_branches_delete.png)

只能通过 Web 界面而不是 Git 删除受保护的分支，这意味着您不能从命令行或 Git 客户端应用程序中意外删除受保护的分支。