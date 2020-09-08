# Wiki[](#wiki "Permalink")

每个项目都内置了一个称为 Wiki 的独立文档系统。 默认情况下，所有新项目都启用此功能，您可以在项目的**Wiki**下找到它。

如果您不想将文档保留在代码仓库中，但确实希望将其保留在代码所在的项目中，则 Wiki 非常方便。

您可以在 Web 界面中或[使用 Git 在本地](#adding-and-editing-wiki-pages-locally)创建 Wiki 页面，因为每个 Wiki 都是单独的 Git 存储库。

## 创建 Home [](#first-time-creating-the-home-page "Permalink")

首次访问 Wiki 时，系统将指示您创建主页 Home 。它是查看 Wiki 时的默认页面，没有 Home 页的话您将看到的是 Wiki 的文件列表。您只需要填写**内容**部分，然后单击**创建页面** ，您以后可以随时对其进行编辑，因此继续写欢迎信息。

## 新建 Wiki [](#creating-a-new-wiki-page "Permalink")

**注意：**需要 developer [权限](/docs/user/permissions.md) 

通过单击可在所有 Wiki 页面中找到的" **新页面"**按钮来创建新页面。

系统将要求您为新的 Wiki 页面填写标题。

您可以通过在标题中使用" /"指示子目录来为 Wiki 页面指定完整路径，任何丢失的目录将自动创建。例如， `docs/my-page`的标题将创建一个 Wiki 页面，其路径为`/wikis/docs/my-page` 。

输入页面名称后，就该填写其内容了. Wiki 支持 Markdown，RDoc，AsciiDoc 和 Org。对于基于 Markdown 的页面，所有[Markdown 功能](/docs/user/markdown.md)均受支持，对于链接，则存在一些[特定](/docs/user/markdown.md#wiki-specific-markdown)于[Wiki 的](/docs/user/markdown.md#wiki-specific-markdown)行为。

在 Web 界面中，提交消息是可选的，但是 Wiki 是基于 Git 的，并且需要提交消息，因此如果您不输入消息，则会为您创建一条。

当你都准备好了后，点击**建立页面** 就可以完成新页面的新建操作。

### 附件存储大小[](#attachment-storage "Permalink")

 通过界面上传到 Wiki 的任何文件都将存储在 Wiki Git 存储库中，如果您在本地克隆 Wiki 存储库，该文件将可用。

### 页面标题中的特殊字符[](#special-characters-in-page-titles "Permalink")

Wiki 页面作为文件存储在 Git 代码仓库中，因此某些字符具有特殊含义：

*   存储页面时，空格会转换为连字符
*   显示页面时，连字符（ `-` ）转换回空格
*   不能使用斜杠（ `/` ），因为它们用作路径分隔符

### 文件及目录的长度限制[](#length-restrictions-for-file-and-directory-names "Permalink")

许多常见的文件系统[的文件名和目录名限制为 255 个字节](https://en.wikipedia.org/wiki/Comparison_of_file_systems#Limits) ，尽管 Git 和 CODEChina 都支持超出这些限制的路径，但是它们的存在使这些文件系统上的用户无法在本地检出 Wiki 存储库。

为了避免这种情况，通过界面和 API 编辑页面时会强制执行以下限制：

*   页面标题为 245 个字节（文件扩展名保留 10 个字节）
*   255 个字节的目录名称

请注意：

*   非 ASCII 字符占用多个字节
*   仍然可以通过 Git 在本地创建超出限制的文件和目录，但这可能会在其他人的计算机上中断.

## 编辑 Wiki [](#editing-a-wiki-page "Permalink")

**注意：**需要 developer [权限](/docs/user/permissions.md) 

要编辑页面，只需单击" **编辑"**按钮，然后您可以更改其内容；完成后，单击" **保存更改"**以使更改生效。

### 添加目录[](#adding-a-table-of-contents "Permalink")

要从 Wiki 页面中的标题生成目录，请使用`[[_TOC_]]`标签。

## 删除 Wiki [](#deleting-a-wiki-page "Permalink")

**注意：**需要 maintainer [权限](/docs/user/permissions.md)

仅在编辑页面时才能找到" **删除"**按钮，单击它并确认您要删除页面。

## 移动 Wiki [](#moving-a-wiki-page "Permalink")

通过在[编辑](#editing-a-wiki-page)表单的 Wiki 页面标题中指定完整路径，可以将 Wiki 页面从一个目录移动到另一个目录。

为了将 Wiki 页面移动到根目录，必须在 Wiki 页面标题前加上斜杠（ `/` ）字符。

## 查看 Wiki 列表[](#viewing-a-list-of-all-created-wiki-pages "Permalink")

每个 Wiki 都有一个侧边栏，从中可以找到所创建页面的简短列表，该列表按字母顺序排列。

如果页面很多，则不会在侧边栏中列出所有页面， 单击**查看所有页面**以**查看所有页面** 。

## 查看 Wiki 历史[](#viewing-the-history-of-a-wiki-page "Permalink")

Wiki 页面随时间的变化记录在 Wiki 的 Git 存储库中，您可以通过单击**页面历史**按钮来查看它们。

从历史记录页面中，您可以看到页面的修订版（Git commit SHA）、作者、提交消息以及上次更新时间，要查看页面的先前版本的外观，请在" **页面版本"**列中单击修订号。

### 查看 Wiki 版本差异[](#viewing-the-changes-between-page-versions "Permalink")

类似于版本化的差异文件视图，您可以看到在给定的 Wiki 页面版本中所做的更改：

1.  进入到您感兴趣的 Wiki 页面
2.  单击**页面历史记录**以查看所有页面版本
3.  单击" **更改"**列中的提交消息以获取您感兴趣的版本

## 本地添加和编辑 Wiki[](#adding-and-editing-wiki-pages-locally "Permalink")

由于 Wiki 基于 Git 存储库，因此您可以像在其他所有 Git 存储库中一样在本地克隆它们并进行编辑。

在右侧栏上，单击" **克隆存储库"，**然后按照屏幕上的说明进行操作。

根据您要使用的标记语言，您在本地添加到 Wiki 的文件必须具有以下受支持的扩展名之一，否则当推送到 CODEChina 时将不会显示这些文件：

*   Markdown 扩展名： `.mdown` ， `.mkd` ， `.mkdn` ， `.md` ， `.markdown` 
*   AsciiDoc 扩展名： `.adoc` ， `.ad` ， `.asciidoc` 
*   其他标记扩展名： `.textile` ， `.rdoc` ， `.org` ， `.creole` ， `.wiki` ， `.mediawiki` ， `.rst` 

## 自定义侧边栏[](#customizing-sidebar "Permalink")

在项目的 Wiki 页面上，有一个右侧导航，默认情况下呈现带有层次结构的完整 Wiki 页面列表。

您可以创建一个名为`_sidebar`的文件以完全替换默认导航，进行自定义设置。

`_sidebar`示例（使用 Markdown 格式）：

```markdown
### [Home](home)
 - [Hello World](hello)
- [Foo](foo)
- [Bar](bar)
 ---

- [Sidebar](_sidebar) 
```