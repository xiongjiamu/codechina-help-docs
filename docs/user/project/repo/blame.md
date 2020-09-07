# balme[](#balme "Permalink")

[Git blame](https://git-scm.com/docs/git-blame)提供有关文件中每一行的更多信息，包括最后修改时间，作者和提交哈希。

您可以在项目中的每个文件中找到 **blame**按钮。

[![File blame button](/docs/img/file_blame_button_v12_6.png "Blame button")](/docs/img/file_blame_button_v12_6.png)

选择 **blame**按钮时，您会看到一个带有说明信息的文件页面：

[![Git blame output](/docs/img/file_blame_output_v12_6.png "Blame button output")](/docs/img/file_blame_output_v12_6.png)

如果将鼠标悬停在中的提交上，您将看到该提交的确切日期和时间。

## 历史提交 Blame[](#blame-previous-commit "Permalink")

要查看特定行的早期修订，请**在此更改**之前单击" **查看责备"，**直到找到您有兴趣查看的**更改**为止：

[![Blame previous commit](/docs/img/file_blame_previous_commit_v12_7.png "Blame previous commit")](/docs/img/file_blame_previous_commit_v12_7.png)

## 与 git 协作[](#associated-git-command "Permalink")

在`git`的命令行中，文件的`blame`则等效命令为`git blame <filename>`。例如，如果你想找到`README.md`在本地目录中的文件`blame`有关信息，可以运行以下命令：

```markdown
git blame README.md 
```

您将看到类似于以下内容的输出，其中包括 UTC 格式的提交时间：

```markdown
fb0fc7d6 (Someone     2019-11-07 22:21:22 +0100   1)
^764ca75 (Someone else              2019-10-05 23:40:24 -0600   2) # CODEChina Documentation
^764ca75 (Someone else              2019-10-05 23:40:24 -0600   3)
0e62ed6d (Someone                   2019-11-26 21:44:53 +0000   4) This project hosts the repository used to generate the CODEChina
0e62ed6d (Someone else              2019-11-26 21:44:53 +0000   5) documentation website 
```