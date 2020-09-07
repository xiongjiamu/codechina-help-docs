# 与组织共享项目[](#share-projects-with-other-groups "Permalink")

您可以与其他组织共享项目，这样就可以通过一个操作将一个组织的全部用户添加到项目中。

## 用户项目集合[](#groups-as-collections-of-users "Permalink")

组织主要用于创建项目集合，但是您还可以利用组织的以下特定：组定义了*用户*集合，即组成员。

## 与组成员共享项目[](#sharing-a-project-with-a-group-of-users "Permalink")

授予某个组织的用户（例如"工程"）访问项目（例如" Acme 项目"）的主要机制是使"工程"组成为" Project Acme"的所有者，但是，如果" Acme 项目"已经属于另一个组织，比如"开源"，这种情况下该怎么办？这里我们就可以使用与组成员共享项目这个功能了。

与"工程"组共享" Acme 项目"：

1.  对于" Acme 项目"，请点击**项目设置**，进入到**项目成员设置**
2.  点击"邀请组"按钮
3.  添加具有您选择的最大访问权限级别的"工程"组
4.  点击**邀请**按钮
5.  与"工程"共享"项目 Acme"后，该项目将出现在"工程"的组织中

请注意，您只能共享项目给符合以下条件的组织：

*   您具有明确定义的成员资格的组织
*   包含嵌套子组或项目的组织，您在其组织中具有明确定义的角色

## 最大访问权限[](#maximum-access-level "Permalink")

在上面的示例中，"工程"成员的最大" Developer "访问级别意味着"工程"中具有较高访问级别的用户（" Maintainer "或" Owner "）将仅对" Acme 项目"具有"开发者"访问权限'。

## 与私有组织共享项目[](#sharing-public-project-with-private-group "Permalink")

与私有组共享公共项目时，项目的 Owner 和 Maintainer 将在`members`页面上看到该组的名称。 所有者还可以在 Issue 或合并请求中使用@功能时，还可以看到他们无权访问的私人群组的成员。

## 禁用与组织共享项目[](#share-project-with-group-lock "Permalink")

可以禁用与组织共享项目以防止一个组织中的项目与另一个组共享一个项目。

了解更多有关[使用组锁共享的信息](/docs/user/org.md#锁定与组织共享功能) 