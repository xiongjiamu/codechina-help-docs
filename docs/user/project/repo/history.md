# 文件历史记录[](#file-history "Permalink")

Git 文件历史记录提供与文件关联的提交历史记录的信息，您可以在项目中的每个文件中找到**历史记录**按钮。

[![File history button](/docs/img/file_history_button_v12_6.png "History button")](/docs/img/file_history_button_v12_6.png)

当选择**历史记录**按钮时，您将看到提交列表，如果将鼠标悬停在提交时间上，您将看到上次修改提交的确切日期和时间。

## 在 git 中使用[](#associated-git-command "Permalink")

如果要从`git`查看文件历史记录，则可以使用`git log <filename>`命令。例如，如果要在本地目录中找到有关`README.md`文件的`history`信息，请运行以下命令：

```markdown
git log README.md 
```

您将看到类似于以下内容的输出，其中包括 UTC 格式的提交时间：

```markdown
commit 0e62ed6d9f39fa9bedf7efc6edd628b137fa781a
Author: Someone <someone@codechina.csdn.net>
Date:   Tue Nov 26 21:44:53 2019 +0000

    Deemphasize GDK as a doc build tool

commit 418879420b1e3a4662067bd07b64bb6988654697
Author: Marcin Sedlak-Jakubowski <someone_else@codechina.csdn.net>
Date:   Mon Nov 4 19:58:27 2019 +0100

    Fix typo

commit 21cc1fef11349417ed515557748369cfb235fc81
Author: Jacques Erasmus <someone_else@codechina.csdn.net>
Date:   Mon Oct 14 22:13:40 2019 +0000

    Add support for modern JS

    Added rollup to the project

commit 2f5e895aebfa5678e51db303b97de56c51e3cebe
Author: Achilleas Pipinellis <codechina@codechina.csdn.net>
Date:   Fri Sep 13 14:03:01 2019 +0000

    Remove gitlab-foss Git URLs as we don't need them anymore

    [ci skip] 
```