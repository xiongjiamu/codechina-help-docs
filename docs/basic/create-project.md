# 新建项目[](#create-a-project "Permalink")

开发中大多数工作都在一个[项目](/docs/user/project/repo.md)完成，文件和代码都保存在项目中，并且大多数功能都将在项目范围内使用。

## 新建一个项目[](#create-a-project "Permalink")

您可以按照以下步骤新建一个项目：

1.  点击导航栏中的加号图标并点击新建项目，这将打开" **新建项目"**页面
2.  在" **新建项目"**页面上，可以选择：
    *   创建一个[空白项目](#blank-projects) 
    *   使用可用的[项目模板](#project-templates)之一创建一个项目
    *   从其他第三方导入一个项目，目前支持 github 以及 url 导入这两种方式

**注意：**有关不能用作项目名称的单词列表，请参见[保留的项目和组名称](/docs/user/reserved.md) 。

### 空项目[](#blank-projects "Permalink")

要在" **新建项目"**页面上创建一个新的空白项目，请执行以下操作：

1.  在" **空白项目"**选项卡上，提供以下信息：
    *   **项目名称**在**项目名称**字段中. 您不能使用特殊字符，但可以使用空格，连字符，下划线甚至表情符号；添加名称时， **项目 URL**将自动填充(仅在项目名称不含中文时会自动填充)
    *   **项目 URL**字段中项目的路径是项目的 URL 路径
    *   使用" **项目描述"（可选）**字段，您可以为项目的仪表板输入描述，这将帮助其他人了解您的项目的含义；尽管不是必需的，但我们建议您还是填写上您的项目简介。
    *   更改" **可见性级别"**会修改用户的项目查看和访问权限
    *   选择**使用 README 初始化存储库**选项将创建一个 README 文件，以便 Git 存储库被初始化，具有默认分支并可以被克隆
2.  点击 **新建项目**

### 项目模板[](#project-templates "Permalink")

项目模板可以使用必要的文件预填充新项目，以使您快速入门。

有两种类型的项目模板：

*   [内置模板](#built-in-templates) ，来自以下组：
    *   [`project-templates`](https://gitlab.com/gitlab-org/project-templates)
    *   [`pages`](https://gitlab.com/pages)
*   [自定义项目模板](#custom-project-templates-premium)

#### 内置模板[](#built-in-templates "Permalink")

内置模板是项目模板，它们是：

*   在[`project-templates`](https://gitlab.com/gitlab-org/project-templates)和[`pages`](https://gitlab.com/pages)组中开发和维护
*   与 GitLab 一起发布

要在" **新建项目"**页面上使用内置模板，请执行以下操作：

1.  在" **从模板创建"**选项卡上，选择" **内置模板"**选项卡
2.  从可用的内置模板列表中，单击：
    *   **预览**按钮以查看模板源本身
    *   **使用模板**按钮开始创建项目
3.  通过填写项目的详细信息来完成创建项目， 该过程与创建[空白项目](#blank-projects)相同

#### 自定义项目模板[](#custom-project-templates-premium "Permalink")

自定义项目可以从**实例**选项卡，或在组级别从**组**选项卡，在**从模板**标签上的**创建** ，创建过程与内置模板创建项目基本一致。