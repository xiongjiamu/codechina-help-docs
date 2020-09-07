# 自定义Git属性[](#自定义Git属性 "Permalink")

CODEChina 支持定义自定义[Git 属性](https://git-scm.com/docs/gitattributes)，例如将哪些文件视为二进制文件，以及将哪种语言用于语法突出显示差异。

要定义这些属性，在代码仓库的根目录中创建一个名为`.gitattributes`的文件，并将其推送到项目的默认分支即可。

## 编码要求[](#encoding-requirements "Permalink")

`.gitattributes`文件*必须*使用 UTF-8 编码，并且*不能*包含字节顺序标记，如果使用其他编码语言则文件的内容将被忽略。

## 语法高亮[](#syntax-highlighting "Permalink")

`.gitattributes`文件可用于定义语法高亮显示文件和差异时使用的语言。