# Web IDE[](#web-ide "Permalink")

Web IDE 编辑器通过提供具有提交阶段的高级编辑器，可以更快，更轻松地为项目贡献更改。

## 打开 WebIDE[](#open-the-web-ide "Permalink")

您可以从代码仓库文件列表和合并请求中查看文件时打开 Web IDE。

[![Open Web IDE](/docs/img/open_web_ide.png)](/docs/img/open_web_ide.png)

## 查找文件[](#file-finder "Permalink")

通过文件查找器，您可以通过搜索快速打开当前分支中的文件. 使用键盘快捷键`Command-p` ， `Control-p`或`t` （当编辑器不在焦点时）启动文件查找器. 输入文件名或文件路径片段以开始查看结果。

## 语法高亮[](#syntax-highlighting "Permalink")

正如 IDE 所期望的那样，Web IDE 中多种语言的语法突出显示将使您的直接编辑更加容易。

Web IDE 当前提供：

*   基本语法着色，适用于各种编程，脚本和标记语言，例如 XML，PHP，C＃，C ++，Markdown，Java，VB，Batch，Python，Ruby 和 Objective-C
*   某些语言的 IntelliSense 和验证支持（显示错误和警告，提供智能补全，格式设置和概述）. 例如：TypeScript，JavaScript，CSS，LESS，SCSS，JSON 和 HTML

因为 Web IDE 基于[Monaco Editor](https://microsoft.github.io/monaco-editor/) ，所以您可以在[Monaco 语言](https://github.com/Microsoft/monaco-languages)存储库中找到更完整的受支持语言列表。 Monaco 在底层上使用[Monarch](https://microsoft.github.io/monaco-editor/monarch.html)库来突出显示语法。

**注意：**单个文件编辑基于[Ace 编辑器](https://ace.c9.io)

### 主题[](#themes "Permalink")

我们支持的语法突出显示的所有主题都添加到了 Web IDE 的代码编辑器中，您可以从个人资料首选项中选择一个主题。

主题仅在 Web IDE 文件编辑器中可用， [深色主题](https://gitlab.com/gitlab-org/gitlab/-/issues/209808)和[日光化深色主题](https://gitlab.com/gitlab-org/gitlab/-/issues/219228)除外，它们适用于整个 Web IDE 屏幕。

| 日光灯主题 | 日晒黑暗主题 | 黑暗主题 |
| --- | --- | --- |
| [![Solarized Light Theme](/docs/img/solarized_light_theme_v13_0.png)](/docs/img/solarized_light_theme_v13_0.png) | [![Solarized Dark Theme](/docs/img/solarized_dark_theme_v13_1.png)](/docs/img/solarized_dark_theme_v13_1.png) | [![Dark Theme](/docs/img/dark_theme_v13_0.png)](/docs/img/dark_theme_v13_0.png) |

## 配置 WebIDE[](#configure-the-web-ide "Permalink")

Web IDE 支持使用[`.editorconfig`文件](https://editorconfig.org/)配置某些编辑器设置，打开文件时，Web IDE 将在当前目录和所有父目录中查找名为`.editorconfig`的文件，如果找到配置文件并且其设置与文件的路径匹配，则将在打开的文件上强制执行这些设置。

Web IDE 当前支持以下`.editorconfig`设置：

*   `indent_style`
*   `indent_size`
*   `end_of_line`
*   `trim_trailing_whitespace`
*   `tab_width`
*   `insert_final_newline`

## 提交更改[](#commit-changes "Permalink")

进行更改后，单击左下角的" **提交"**按钮以查看已更改文件的列表。

完成更改后，可以添加提交消息，提交更改并直接创建合并请求。如果您没有对所选分支的写访问权，则会看到警告，但仍然可以创建新分支并启动合并请求。

要放弃特定文件中的更改，请在"更改"选项卡中单击该文件上的" **放弃更改"**按钮；要放弃所有更改，请单击更改侧栏右上角的删除图标。

## 查看更改[](#reviewing-changes "Permalink")

提交更改之前，可以通过切换到查看模式或从更改列表中选择文件来将它们与上一次提交进行比较。

当您打开合并请求时，还可以使用其他查看模式，如果您提交更改，该模式将向您显示合并请求 diff 的预览。

## 切换合并请求[](#switching-merge-requests "Permalink")

要在创作的和分配的合并请求之间切换，请单击侧栏顶部的下拉列表以打开合并请求列表。在切换到其他合并请求之前，您将需要提交或放弃所有更改。

## 切换分支[](#switching-branches "Permalink")

要在当前项目存储库的分支之间切换，请单击侧栏顶部的下拉列表以打开分支列表。在切换到其他分支之前，您需要提交或放弃所有更改。

## 编辑Markdown[](#markdown-editing "Permalink")

在 Web IDE 中编辑 Markdown 文件时，可以通过单击文件编辑器上方的" **预览 Markdown"**选项卡来预览更改. Markdown 预览支持[GFM](/docs/user/markdown.md#gitlab-flavored-markdown-gfm)。

您还可以通过将任何本地图像直接粘贴到 Markdown 文件中来上传它们，该图像将上传到同一目录，默认情况下命名为`image.png` 。 如果已经存在相同名称的另一个文件，则将数字后缀自动添加到文件名。

## 预览[](#live-preview "Permalink")

您可以使用 Web IDE 在浏览器中预览 JavaScript 项目，此功能使用 CodeSandbox 编译和捆绑用于预览 Web 应用程序的 JavaScript。

此外，对于公共项目，**在 CodeSandbox 打开**按钮可用于将项目内容转移到公共代码沙盒项目中，以便与其他人快速共享您的项目。

### WebIDE 配置文件[](#web-ide-configuration-file "Permalink")

为了启用 Web IDE 终端，您需要在存储库根目录内创建文件`.gitlab/.gitlab-webide.yml` . 该文件与 CI 配置文件的语法非常相似，但有一些限制：

*   无法定义全局块（即： `before_script`或`after_script` ）
*   只能将一个名为`terminal`作业添加到该文件中.
*   仅允许使用关键字`image` ， `services` ， `tags` ， `before_script` ， `script`和`variables`来配置作业
*   要连接到交互式终端， `terminal`作业必须仍然处于活动状态并且正在运行，否则终端将无法连接到作业的会话。默认情况下， `script`关键字的值是`sleep 60`以防止作业结束并为 Web IDE 提供足够的连接时间。 这意味着，如果您覆盖默认`script`值，则必须添加一个使作业保持运行`sleep`的命令，例如`sleep` 。