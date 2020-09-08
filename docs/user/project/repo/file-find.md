# 文件查找[](#file-finder "Permalink")

文件查找器功能使您可以使用 CODEChina 在代码仓库中搜索文件。

您可以在项目的**文件**部分中找到**查找文件**按钮。

[![Find file button](/docs/img/file_finder_find_button_v12_10.png)](/docs/img/file_finder_find_button_v12_10.png)

如果您喜欢使用快捷键，我们还支持[键盘快捷键](/docs/user/shortcutkey.md) ，您可以从项目中的*任何地方*调用它。

在** Issue ** ， **合并请求** ， **里程碑**甚至项目设置中，按`t`键启动文件搜索功能。

开始输入您要搜索的内容，就会看到系统的搜索结果。您可以使用向上/向下箭头向上和向下搜索结果，使用`Esc`可以关闭搜索并返回 **文件**。

## 实现原理[](#how-it-works "Permalink")

文件查找器功能由[模糊过滤器](https://github.com/jeancroy/fuzz-aldrin-plus)库提供支持。

它通过突出显示来实现模糊搜索，并试图通过识别人们在搜索时使用的模式来提供直观的结果。

例如，假设有[Awesome-project]https://codechina.csdn.net/codechina/awesome-project/-/tree/master ，并且我们要打开`app/models/model.rb`文件。

使用模糊搜索，我们首先输入使我们更接近文件的字母。

**提示：**要缩小搜索范围，请在搜索词中包含`/` .

[![Find file button](/docs/img/file_finder_find_file_v12_10.png)](/docs/img/file_finder_find_file_v12_10.png)