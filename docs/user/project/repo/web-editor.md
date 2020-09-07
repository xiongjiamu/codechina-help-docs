# 文件编辑[](#文件编辑 "Permalink")

有时，直接从 CODEChina 界面进行快速更改要比克隆项目并使用 Gi​​t 命令行工具更容易。接下来，我们重点介绍如何从文件浏览器创建新文件，目录，分支或标记，以上所有这些操作都可以通过一个下拉菜单获得。

## 创建文件[](#create-a-file "Permalink")

在项目的文件页面中，单击分支下拉列表右侧的" +"按钮，从下拉列表中选择**新文件** 

[![New file dropdown menu](/docs/img/web_editor_new_file_dropdown.png)](/docs/img/web_editor_new_file_dropdown.png)

在**文件名**框中输入文件名，然后在编辑器区域中添加文件内容；添加描述性提交消息并选择一个分支，分支字段将默认为您在文件浏览器中查看的分支；如果输入新的分支名称，将出现一个复选框，允许您在提交更改后启动新的合并请求。

当您完成新文件的内容后，请单击底部的" **提交更改** "。

### 文件模板[](#template-dropdowns "Permalink")

启动新项目时，新项目可能也需要一些通用文件，CODEChina 将在仓库中提示您新建这些文件。

[![First file for your project](/docs/img/web_editor_template_dropdown_first_file.png)](/docs/img/web_editor_template_dropdown_first_file.png)

当单击`LICENSE`或`.gitignore`等时，将显示一个下拉列表，为您提供适合您的项目的模板。

[![MuLan license selected](/docs/img/web_editor_template_dropdown_mulan_license.png)](/docs/img/web_editor_template_dropdown_mulan_license.png)

许可证，更新日志，贡献指南等文件也都可以通过项目页面上的按钮添加。

## 上传文件[](#upload-a-file "Permalink")

当内容为文本时，创建文件将十分方便。但是，这不适用于二进制数据，例如图像，PDF 或其他文件类型，在这种情况下，您可以选择上传文件。

在项目的文件页面中，单击分支下拉列表右侧的" +"按钮，从下拉菜单中选择**上传文件** 。

弹出上传对话框后，有两种方法可以上传文件：可以在弹出窗口中拖放文件；也可以使用**点击上传**链接，选择要上传的文件后，将显示文件预览。

输入提交消息，选择一个分支，并在准备好后单击**上传文件** 。

## 新建目录[](#create-a-directory "Permalink")

为了使代码仓库中的文件井井有条，您可以创建一个目录将相关的文件都归类到同一个目录中。

在项目的文件页面中，单击分支下拉列表右侧的" + "号，从下拉菜单中选择 **新建目录**。

在新目录对话框中，输入目录名称，提交消息并选择目标分支，单击**创建目录**完成新建目录操作。

## 新建分支[](#create-a-new-branch "Permalink")

有多种方法可从 CODEChina 的界面创建分支。

### 从 Issue 创建一个新分支[](#create-a-new-branch-from-an-issue "Permalink")

如果您的开发工作流程要求每个合并请求都存在 Issue，则可以直接从该 Issue 快速创建分支，以加快流程。新分支及其以后的合并请求将被标记为与此问题相关，合并后将自动关闭 Issue。您可以在 Issue 说明下方看到 **创建合并请求**下拉列表。

**注意：**如果已经有一个具有相同名称的分支或一个引用的合并请求，或者您的项目具有活动的 Fork 关系，则不会看到 **创建合并请求**按钮。如果您想显示此按钮，则可能的解决方法是删除项目的 fork 关系，删除后，Fork 关系将无法恢复，您将不再能够将合并请求发送到源仓库。

该下拉列表包含选项**创建合并请求和分支**以及**创建分支** 

[![New Branch Button](/docs/img/web_editor_new_branch_from_issue_v_12_6.png)](/docs/img/web_editor_new_branch_from_issue_v_12_6.png)

选择这些选项之一后，将基于项目的默认分支（默认为`master`创建新的分支或分支与合并请求. 分支名称将基于 Issue 的标题，并作为前缀具有其内部 ID。因此，上面的示例屏幕快照将创建一个名为`1-webpack`的分支。

当您在一个空的项目中单击**创建分支**按钮时，CODEChina 会自动创建一个`master`分支， `README.md`提交一个空白的`README.md`文件，并根据 Issue 标题创建并将您重定向到新分支（如果您的项目已经配置了）。

创建分支后，您可以编辑代码仓库中的文件以解决此 Issue。当基于新创建的分支创建合并请求时，描述字段将自动显示[ Issue 关闭模式](/docs/user/project/issues/manage.md#closing-issues-automatically) `Closes #ID` ，其中`ID`为 Issue 的 ID，一旦合并请求被合并， Issue 将自动关闭。

### 从项目页新建分支[](#create-a-new-branch-from-a-projects-dashboard "Permalink")

如果要在创建新的合并请求之前对多个文件进行更改，则可以预先创建一个新的分支。在项目页的" + "号下拉列表中选择 **新建分支** "。

[![New branch dropdown](/docs/img/web_editor_new_branch_dropdown.png)](/docs/img/web_editor_new_branch_dropdown.png)

输入新的**分支名称** ，更改**从模板创建**字段以选择该新分支将来自哪个分支、标记或提交 SHA（可选）。如果您开始键入现有的分支或标签，则此字段将自动完成。单击**创建分支** ，您将返回到该新分支上的文件列表页。

[![New branch page](/docs/img/web_editor_new_branch_page.png)](/docs/img/web_editor_new_branch_page.png)

现在，您可以根据需要更改任何文件。当您准备好将更改合并回 master 分支时，可以使用页面顶部的"创建合并请求"按钮，在创建分支或修改文件后，该按钮将会在页面显示一段时间。

## 新建 Tag[](#create-a-new-tag "Permalink")

Tag 可用于标记主要的里程碑，例如 Release 版本，候选版本等等。您可以从分支或提交 SHA 创建 Tag，在项目的文件页面上，从下拉列表中选择" **新建标签** "。

给标签起一个名字，例如`v1.0.0` 。选择您要从中创建此新标签的分支或 SHA，您可以选择添加一条消息及 Release说明(可选)，发行说明支持 Markdown 格式，您也可以上传附件。单击**创建标签** ，创建成功后将返回标签列表页。

## 提示[](#tips "Permalink")

创建或上传新文件或创建新目录时，均可触发新的合并请求，而不是直接提交给 master。在**目标分支**字段中输入新的分支名称，您会注意到出现一个复选框，标有**通过这些更改启动新的合并请求** ，提交更改后，您将进入新的合并请求表单。

如果你*不*希望使用您的主电子邮件地址通过 Web 编辑器创建的提交，您可以从**用户设置>编辑个人资料**页面选择使用其他的链接的电子邮件地址。