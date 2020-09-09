# 代码仓库[](#repository "Permalink")

[代码仓库](https://git-scm.com/book/en/v2/Git-Basics-Getting-a-Git-Repository)是用于将代码库存储在 CODEChina 中并通过版本控制对其进行更改的存储库。代码仓库是[项目](/docs/user/project.md)的一部分，它具有许多其他功能。 

## 新建一个代码仓库[](#create-a-repository "Permalink")

要创建一个新的代码仓库，您需要做的就是[创建一个新项目](/docs/basic/create-project.md)或 fork 一个现有项目。

创建新项目后，您可以通过界面或通过命令行添加新文件， 要从命令行添加文件，请遵循创建新项目时在屏幕上显示的说明。

> **重要提示：**出于安全原因，强烈建议您在使用命令行时[通过 SSH 与 CODEChina 连接](/docs/ssh.md) 。

## 文件[](#files "Permalink")

在 CODEChina 上我们使用代码仓库来存储您的文件，您将在代码仓库的文件树中在文件名旁边看到一个与其扩展名称想对应的图标。

### 新建和编辑文件[](#create-and-edit-files "Permalink")

通过将文件推送到 CODEChina，您就可以将代码库托管在代码仓库中。您可以使用用户界面也可以通过命令行将本地计算机与我们相连。

**从用户界面：**

用户界面允许您执行许多 Git 命令，而无在命令行中执行命令。您可以通过用户界面很容易的实现以下操作：

*   [新建文件](/docs/user/project/repo/web-editor.md#create-a-file)
*   [上传文件](/docs/user/project/repo/web-editor.md#upload-a-file)
*   [文件模板](/docs/user/project/repo/web-editor.md#template-dropdowns)
*   [新建目录](/docs/user/project/repo/web-editor.md#create-a-directory)
*   [新建合并请求](/docs/user/project/repo/web-editor.md#tips)
*   [查找文件](/docs/user/project/repo/file-find.md)
*   [blame](/docs/user/project/repo/blame.md))

### 查找文件[](#find-files "Permalink")

使用[文件查找器](/docs/user/project/repo/file-find.md)在代码仓库中搜索文件。

### 支持的语言标记[](#supported-markup-languages-and-extensions "Permalink")

我们支持多种标记语言（有时称为[轻量标记语言](https://en.wikipedia.org/wiki/Lightweight_markup_language) ），您可以将其用于存储库中文件的内容，它们主要用于文档目的。

只需为文件选择正确的扩展名，系统就会根据标记语言来渲染它们。

| 标记语言 | 扩展名 |
| --- | --- |
| 纯文本 | `txt` |
| [Markdown](/docs/user/markdown.md) | `mdown`, `mkd`, `mkdn`, `md`, `markdown` |
| [reStructuredText](https://docutils.sourceforge.io/rst.html) | `rst` |
| AsciiDoc | `adoc`, `ad`, `asciidoc` |
| [Textile](https://textile-lang.com/) | `textile` |
| [rdoc](http://rdoc.sourceforge.net/doc/index.html) | `rdoc` |
| [Org mode](https://orgmode.org/) | `org` |
| [creole](http://www.wikicreole.org/) | `creole` |
| [MediaWiki](https://www.mediawiki.org/wiki/MediaWiki) | `wiki`, `mediawiki` |

### 项目 Readme 和 Index 文件[](#repository-readme-and-index-files "Permalink")

当代码仓库中存在`README`或`index`文件时，我们将自动渲染他们的内容，用户无需打开它。

它们可以是纯文本，也可以具有[受支持的标记语言](#supported-markup-languages-and-extensions)的扩展名：

有关优先级的一些注意事项：

1.  当`README`文件和`index`文件同时存在时， `README`文件将始终优先
2.  如果存在多个具有不同扩展名的文件，则按字母顺序排列，但不带扩展名的文件例外，该扩展名始终优先。例如， `README.adoc`将优先于`README.md` ，而`README.rst`将优先于`README` 

### Jupyter Notebook files[](#jupyter-notebook-files "Permalink")

[Jupyter](https://jupyter.org/) Notebook（以前的 IPython Notebook）文件用于许多领域的交互式计算，并且包含用户会话的完整记录，并包括代码，叙述性文本，方程式和丰富的输出。

### OpenAPI viewer[](#openapi-viewer "Permalink")

如果文件名包含`openapi`或`swagger`且扩展名为`yaml` ， `yml`或`json` ，就可以使用其文件查看器呈现 OpenAPI 规范文件。以下示例都是正确的：

*   `openapi.yml`
*   `openapi.yaml`
*   `openapi.json`
*   `swagger.yml`
*   `swagger.yaml`
*   `swagger.json`
*   `gitlab_swagger.yml`
*   `openapi_gitlab.yml`
*   `OpenAPI.YML`
*   `openapi.Yaml`
*   `openapi.JSON`
*   `openapi.gitlab.yml`
*   `gitlab.openapi.yml`

然后，渲染它们：

1.  用户界面中导航至存储库中的 OpenAPI 文件.
2.  单击位于"显示源"和"编辑"按钮之间的"显示 OpenAPI"按钮（找到 OpenAPI 文件后，它将替换"显示渲染的文件"按钮）.

## 分支[](#branches "Permalink")

有关详细信息，请参见[分支](/docs/user/project/repo/branches.md) 。

## 提交[](#commits "Permalink")

[提交更改时](https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository) ，您会将这些更改引入分支机构。通过命令行，您可以在提交之前多次提交。

*   **提交消息：**提交消息对于标识正在更改的内容以及更重要的原因至关重要. 在 GitLab 中，您可以将关键字添加到提交消息中，以执行以下操作之一：
    *   **交叉链接问题和合并请求：** [交叉链接](/docs/user/project/issues/crosslinking.md#from-commit-messages)非常适合跟踪工作流程中与之相关的内容. 如果您在提交消息中提到问题或合并请求，它们将显示在各自的线程上
*   ** Cherry-pick 提交：**您可以直接从界面 [cherry-pick](/docs/user/project/merge-request/cherry-pick.md) 
*   **Revert 提交：**可以将提交从界面[还原](/docs/user/project/merge-request/revert.md#reverting-a-commit)到所选分支
*   **签署提交：**使用 GPG [签署您的提交](/docs/user/project/repo/gpg-sign.md) 

## 项目和仓库大小[](#project-and-repository-size "Permalink")

在项目的**详细信息**页面上报告项目的大小 报告的大小最多每 15 分钟更新一次，因此可能无法反映最近的活动。显示的文件大小包括存储库文件，工件和 LFS。

由于压缩，内务处理和其他因素，每个项目的项目规模可能会略有不同。

## 贡献者[](#contributors "Permalink")

代码库的所有贡献者都显示在项目的**代码>贡献者下**，按照协作者中的提交次数从多到少排序。

## 分析[](#repository-graph "Permalink")

代码仓库分析以可视方式显示存储网络的历史记录，包括分支和合并。这可以帮助您可视化存储库中使用的 Git 流策略：

在您项目的**分析**下找到它。

## 代码语言[](#repository-languages "Permalink")

对于每个代码仓库的默认分支，系统将确定使用了哪些编程语言，并将其显示在项目页面上。如果缺少此信息，将在更新项目上的默认分支后添加，此过程最多可能需要 5 分钟。

并非所有文件都被检测到，比如文档、供应商代码和大多数标记语言都不会被检测。可以通过重写默认值来调整此行为。例如，为了能够检测到“.proto”文件，请在存储库根目录下的“.gittributes”中添加以下内容：

```markdown
*.proto linguist-detectable=true 
```

## 锁定文件[](#locked-files-premium "Permalink")

使用文件锁定来锁定文件，以防止发生任何冲突的更改.

## Repository’s API[](#repositorys-api "Permalink")

您可以通过存储库 API访问您的存储库。

## 下载源码[](#download-source-code "Permalink")

可以从界面下载存储在代码仓库中的源代码，单击下载图标，将打开一个下拉列表，其中包含下载以下内容的链接：

*   **源代码：**允许用户在他们当前正在查看的分支上下载源代码。 可用扩展名： `zip` ， `tar` ， `tar.gz`和`tar.bz2` 
*   **目录：**仅在查看子目录时显示， 这使用户可以下载他们当前正在查看的特定目录， 也可以在`zip` ， `tar` ， `tar.gz`和`tar.bz2` 
*   **工件：**允许用户下载最新 CI 构建的工件