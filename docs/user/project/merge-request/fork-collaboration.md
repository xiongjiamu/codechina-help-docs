# 允许 Fork 项目协助提交合并请求[](#允许Fork项目协助提交合并请求 "Permalink")

当用户在 Fork 的项目上新建合并请求时，将为他们提供允许上游成员在源分支上与其进行协作的选项，这使得上游项目的成员可以在合并之前进行小规模修复或 Rebase 分支，从而减少了接受外部贡献的来回过程。

此功能适用于可公开访问的项目与 Fork 项目之间的合并请求。

当启用后，对项目目标分支具有合并访问权限的成员将被授予对合并请求的源分支的写权限。

## 启用允许上游项目成员修改提交[](#enabling-commit-edits-from-upstream-members "Permalink")

只有具有对源项目的推送访问权限的用户才能启用该功能，并且只有在合并请求打开时才能持续使用。启用后，上游成员也将能够重试合并请求的管道和作业：

1.  在创建或编辑合并请求时启用允许协助

    [![Enable contribution](/docs/img/allow_collaboration.png)](/docs/img/allow_collaboration.png)

2.  创建合并请求后，您将看到允许可以合并到目标分支的成员的提交

    [![Check that contribution is enabled](/docs/img/allow_collaboration_after_save.png)](/docs/img/allow_collaboration_after_save.png)

## 上游项目成员推送代码至 Fork 项目[](#pushing-to-the-fork-as-the-upstream-member "Permalink")

如果合并请求的创建者启用了允许上游成员进行协助贡献，则上游项目成员可以直接推送到 Fork 项目代码仓库的分支中。

假设现在有如下所示的 Fork 项目及合并请求分支：

*   Fork 的项目 URL 为`git@codechina.csdn.net:codechina/awesome-project.git`
*   合并请求的分支是`update-docs`

流程如下所示：

1.  首先，您需要获取合并请求引入的更改，单击**签出分支**按钮，其中包含可以运行的一些预填充命令
2.  使用复制按钮复制第一个命令并将其粘贴到您的终端中：

    ```markdown
    git fetch git@codechina.csdn.net:codechina update-docs
    git checkout -b codechina-awesome-project-update-docs FETCH_HEAD 
    ```
    以上命令将获取 Fork 项目的分支，然后基于所获取的分支创建本地分支

3.  在分支中完成你所需要进行的修改
4.  推送到分叉的项目：

    ```markdown
    git push git@codechina.csdn.net:codechina/awesome-project.git codechina-awesome-project-update-docs:update-docs 
    ```

    注意两个分支之间需要用冒号（ `:`）。上面的命令会将本地分支`codechina-awesome-project-update-docs`推送到`git@codechina.csdn.net:codechina/awesome-project.git`代码仓库的`update-docs`分支。