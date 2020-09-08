# Releases[](#releases "Permalink")

要在源代码历史记录中引入检查点，可以在发布时分配[Git 标签](https://git-scm.com/book/en/v2/Git-Basics-Tagging) 。但是，在大多数情况下，您的用户不仅需要原始源代码，他们需要 CI / CD 系统输出的已编译对象或其他资产。

*Release*是与代码的发行版本相关联的源代码，构建输出，工件和其他元数据的快照。

您可以在任何分支上创建一个 Release，创建时：

*   系统将自动归档源代码，并将其与 release 关联
*   系统会自动创建一个 JSON 文件，其中列出了发行版中的所有内容，因此您可以比较和审核发行版。该文件称为[发布证据](#release-evidence) 
*   您可以添加发行说明以及与发行版关联的标签的消息

创建发行版后，您可以将[里程碑与其关联](#associate-milestones-with-a-release) ，并附加[发行附件](#release-assets) ，例如运行手册或软件包。

## 查看 Release[](#view-releases "Permalink")

要查看版本列表：

*   转到**项目> 项目简介**，在下方有发行版本信息
*   在项目的概述页面上，如果存在至少一个版本，请单击版本数
    *   在公共项目上，此数字对所有用户可见
    *   在私有项目上，具有 Reporter [权限](/docs/user/permissions.md)或更高权限的用户可以看到此数字

## 创建 Release[](#create-a-release "Permalink")

可以在 CODEChina 界面中直接创建发布。

**注意：**只有具有 developer 权限或更高权限的用户才能创建发行版。

可以通过以下步骤创建新版本：

1.  转到**项目> 项目简介** ，然后单击**创建发行版**；或在发行列表中右上角单击**新建发布**按钮
2.  在[**标签名称**](#tag-name)框中，输入一个名称
3.  单击**从创建列表**，并选择需要创建发行版的分支
4.  在" **消息"**框中，输入与标签关联的消息
5.  （可选）在" [**发行说明"**](#release-notes-description)字段中，输入发行说明。您可以使用 Markdown 并将文件拖放到此字段
    *   如果将此字段留空，则只会创建一个标签
    *   如果您填充它，将同时创建标签和发行版
6.  单击 **创建标签**

如果创建了发行​​版，则可以在**项目> 项目简介** 对其进行查看。如果创建了标签，则可以在**仓库>标签**查看它。

现在，您可以编辑发布以[添加里程碑](#associate-milestones-with-a-release)和[发布附件](#release-assets)。

## 编辑 Release[](#edit-a-release "Permalink")

**注意：**只有具有 developer 权限或更高权限的用户才能编辑发行版。

可以通过以下步骤编辑发行版：

1.  转到**项目> 项目简介**，点击 发行版本旁边的数字并进入到 发行版本列表
2.  在您要修改的发行版的右上角，单击" **编辑此发布"** 按钮
3.  在" **编辑版本"**页面上，更改版本的详细信息
4.  单击 **保存更改**

您可以编辑发行标题，注释，关联的里程碑和资产链接。

## 在 Tag 上添加发行信息[](#add-release-notes-to-git-tags "Permalink")

如果你有一个已经存在的 Tag，你可以在这个 Tag 上添加发行信息，您可以在用户界面中来执行此操作。

在界面中，您可以通过以下步骤向新的 Git 标签添加发行说明：

1.  导航到您项目的**代码> Tags**
2.  单击 **新建标记**
3.  在**发行说明**字段中，输入发行说明。您可以使用 Markdown 并将文件拖放到此字段
4.  单击 **创建标签**

在界面中，您可以通过以下步骤将发行说明添加到现有的 Git 标签：

1.  导航到您项目的**代码> Tags** 
2.  单击**编辑发行说明** 
3.  在**发行说明**字段中，输入发行说明。您可以在此字段中使用 Markdown，并将文件拖放到该字段中
4.  单击 **保存更改**

## 关联发行与里程碑[](#associate-milestones-with-a-release "Permalink")

您可以将一个版本与一个或多个项目里程碑相关联。

您可以在用户界面中执行此操作，具体的步骤如下：

1.  转到**项目> 项目简介**，点击 发行版本旁边的数字并进入到 发行版本列表
2.  在您要修改的发行版的右上角，单击" **编辑此发行版"** 
3.  从" **里程碑"**列表中，选择要关联的每个里程碑，您可以选择多个里程碑
4.  单击 **保存更改**

## 当发布时通知我[](#get-notified-when-a-release-is-created "Permalink")

当您的项目创建新版本时，将通过电子邮件通知您。

可以通过以下步骤订阅发布通知：

1.  进入项目页面
2.  单击**通知设置** 
3.  在列表中，点击**自定义** 
4.  勾选 **新发布** 复选框
5.  关闭对话框并保存

## 认识发行[](#release-fields "Permalink")

创建或编辑发行版时，以下字段可用：

### Tag 名称[](#tag-name "Permalink")

发行标签名称应包括发行版本，我们建议您在发行版中使用[语义版本控制](https://semver.org/)。 使用`(Major).(Minor).(Patch)`。

例如，对于 GitLab 版本`10.5.7` ：

*   `10`代表主要版本. 主要版本是`10.0.0` ，但通常称为`10.0` .
*   `5`代表次要版本. 次要版本为`10.5.0` ，但通常称为`10.5` .
*   `7`代表补丁号码.

版本号的任何部分都可以是多个数字，例如`13.10.11` .

### 发行描述[](#release-notes-description "Permalink")

每个版本都有说明，您可以添加任何您喜欢的文本，但是我们建议您添加一个变更日志来描述发行版本的内容。这可以帮助用户快速扫描您发布的每个版本之间的差异。

**注意：** [Git 的标记消息](https://git-scm.com/book/en/v2/Git-Basics-Tagging)和发行说明描述无关；说明支持[Markdown](/docs/user/markdown.md) 。

### 发布资产[](#release-assets "Permalink")

当前，您可以将以下类型的资产添加到每个版本：

*   [Source code](#source-code)
*   [Links](#links)

我们将在未来支持更多的资产类型，包括诸如预装包，合规性/安全证据或容器图像之类的对象等。

### 源代码[](#source-code "Permalink")

我们会根据给定的 Git 标签自动生成`zip` ， `tar.gz` ， `tar.bz2`和`tar`归档的源代码， 这些是只读资产。

### 链接[](#links "Permalink")

链接是任何可以指向您喜欢的任何内容的URL：文档、构建的二进制文件或其他相关材料。这些可以是来自 CODEChina 的内部或外部链接。

链接的四种类型是" Runbook"，" Package"，" Image"和" Other"。

## 发布证据[](#release-evidence "Permalink")

每次创建发行版时，CODEChina 都会拍摄与之相关的数据快照。此数据保存在 JSON 文件中，称为*发布证据* ， 它包括链接的里程碑和问题，并且可以促进内部流程，例如外部审核。

要访问发布证据，请在"发布"页面上，单击" **证据集合"**标题下列出的 JSON 文件的链接。

**注意：**禁用问题跟踪器后，将无法下载发布证据。

这是发行证据的一个示例：

```markdown
{  "release":  {  "id":  5,  "tag_name":  "v4.0",  "name":  "New release",  "project":  {  "id":  20,  "name":  "Project name",  "created_at":  "2019-04-14T11:12:13.940Z",  "description":  "Project description"  },  "created_at":  "2019-06-28 13:23:40 UTC",  "description":  "Release description",  "milestones":  [  {  "id":  11,  "title":  "v4.0-rc1",  "state":  "closed",  "due_date":  "2019-05-12 12:00:00 UTC",  "created_at":  "2019-04-17 15:45:12 UTC",  "issues":  [  {  "id":  82,  "title":  "The top-right popup is broken",  "author_name":  "John Doe",  "author_email":  "john@doe.com",  "state":  "closed",  "due_date":  "2019-05-10 12:00:00 UTC"  },  {  "id":  89,  "title":  "The title of this page is misleading",  "author_name":  "Jane Smith",  "author_email":  "jane@smith.com",  "state":  "closed",  "due_date":  "nil"  }  ]  },  {  "id":  12,  "title":  "v4.0-rc2",  "state":  "closed",  "due_date":  "2019-05-30 18:30:00 UTC",  "created_at":  "2019-04-17 15:45:12 UTC",  "issues":  []  }  ],  "report_artifacts":  [  {  "url":"https://gitlab.example.com/root/project-name/-/jobs/111/artifacts/download"  }  ]  }  } 
```

### 收集发布证据[](#collect-release-evidence-premium-only "Permalink")

创建发布后，将自动收集发布证据。在"发布"页面上可以看到证据收集快照，以及收集证据的时间戳。
