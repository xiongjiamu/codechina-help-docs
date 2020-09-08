# 自动填充字符[](#autofill "Permalink")

自动完成字符填充提供了一种在 Markdown 字段中输入字段值的快速方法，当您开始在 Markdown 字段中使用以下字符之一键入单词时，CODEChina 将针对一组匹配值逐步自动完成， 字符串匹配不区分大小写。

| 字符 | 自动补全内容 |
| --- | --- |
| `~` | Labels |
| `%` | Milestones |
| `@` | 用户和组 |
| `#` | Issues |
| `!` | 合并要求 |
| `&` | Epics |
| `$` | 代码片 |
| `:` | Emoji表情 |
| `/` | 快速行动 |

弹出列表中最多显示 5 个最相关的匹配项，当您从列表中选择一个项目时，该值将输入到该字段中。输入的字符越多，匹配结果就越精确。

与" [快速操作"](/docs/user/project/quick-actions.md)结合使用时，字符自动完成将会十分有用。

## 举例[](#example "Permalink")

假设您的项目中包括以下用户：

| 用户名 | 昵称 |
| --- | --- |
| alessandra | 罗斯·格兰特 |
| lawrence.white | 凯尔西·克鲁克 |
| leanna | 罗斯玛丽·罗甘（Rosemarie Rogahn） |
| logan_gutkowski | 李·沃克特 |
| shelba | 约瑟芬·海利 |

在" Issue "讨论中，输入`@l`将显示以下弹出列表，需要注意的是这里并不包括用户`shelba` ，因为该列表仅包含与问题最相关的 5 个用户。

[![Popup list which includes users whose username or name contains the letter `l`](/docs/img/autocomplete_characters_example1_v12_0.png)](/docs/img/autocomplete_characters_example1_v12_0.png)

如果继续输入`@le` ，弹出列表将更改为以下内容。现在，弹出窗口仅包括用户名中出现`le`或用户名中的单词的用户。

[![Popup list which includes users whose username or name contains the string `le`](/docs/img/autocomplete_characters_example2_v12_0.png)](/docs/img/autocomplete_characters_example2_v12_0.png)