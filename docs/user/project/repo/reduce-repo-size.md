# 减少仓库大小[](#reduce-repo-size "Permalink")

代码仓库会随着时间变得越来越大，将大文件加到 Git 代码仓库后：

*   由于每个人都必须下载文件，因此获取存储库的速度变慢
*   它们占用服务器上的大量存储空间
*   会[达到](#storage-limits) Git 仓库的存储限制

重写代码仓库可能会删除不需要的历史记录，从而使代码仓库变得更小。[`git filter-repo`](https://github.com/newren/git-filter-repo)是用于快速重写 Git 存储库历史记录的工具，建议同时使用以下两种工具：

*   [`git filter-branch`](https://git-scm.com/docs/git-filter-branch).
*   [BFG](https://rtyley.github.io/bfg-repo-cleaner/).

**危险：**重写代码仓库历史记录是一种破坏性操作，在开始之前，请确保备份您的代码仓库。备份存储库的最佳方法是[导出项目](/docs/user/project/import.md#exporting-a-project-and-its-data) 。

## 在从代码仓库历史记录中净化文件[](#purge-files-from-repository-history "Permalink")

为了使克隆项目更快，建议重写分支和标签以删除不需要的文件。

1.  使用受支持的程序包管理器或从源代码[安装`git filter-repo`](https://github.com/newren/git-filter-repo/blob/main/INSTALL.md)

2.  使用`--bare`克隆代码仓库的新副本：

    ```markdown
    git clone --bare https://example.gitlab.com/my/project.git 
    ```

3.  使用`git filter-repo` ，从代码仓库的历史记录中清除所有文件

    要清除大文件，可以使用`--strip-blobs-bigger-than`选项：

    ```markdown
    git filter-repo --strip-blobs-bigger-than 10M 
    ```
    要清除使用 Git LFS 存储的大文件，可以使用`--blob--callback`选项. 下面的示例使用回调从 Git LFS 指针读取文件大小，并删除大于 10MB 的文件

    ```markdown
    git filter-repo --blob-callback '
      if blob.data.startswith(b"version https://git-lfs.github.com/spec/v1"):
        size_in_bytes = int.from_bytes(blob.data[124:], byteorder="big")
        if size_in_bytes > 10*1000:
          blob.skip()
      ' 
    ```

    要按路径清除特定的大文件，可以组合使用`--path`和`--invert-paths`选项：

    ```markdown
    git filter-repo --path path/to/big/file.m4v --invert-paths 
    ```

    有关更多示例和完整文档，请参见[`git filter-repo`](https://htmlpreview.github.io/?https://github.com/newren/git-filter-repo/blob/docs/html/git-filter-repo.html#EXAMPLES)文档。

4.  运行`git filter-repo`会删除所有 remote，要为您的项目还原 remote，请运行：

    ```markdown
    git remote add origin https://codechina.csdn.net/<namespace>/<project_name>.git 
    ```

5.  强制推送更改以覆盖 CODEChina 上的所有分支：

    ```markdown
    git push origin --force --all 
    ```

    [受保护的分支](/docs/user/project/protected-branch.md)将导致此操作失败。要继续的话，您必须删除分支保护，推送，然后重新启用受保护的分支。

6.  要从标记的 Release 中删除大文件，请强制将更改推送到CODEChina上的所有标记：

    ```markdown
    git push origin --force --tags 
    ```

    [受保护的标签](/docs/user/project/protected-tag.md)将导致此操作失败. 要继续，您必须删除标签保护，推送，然后重新启用受保护的标签.

7.  手动执行项目整理

**注意：**为提高性能我们缓存了项目统计信息，您可能需要等待 5 到 10 分钟才能看到存储利用率下降。

## 在代码仓库中净化文件[](#purge-files-from-repo-storage "Permalink")

要减少代码仓库的大小，必须删除 CODEChina 内部引用包含大文件的提交。在完成这些步骤之前，请[从存储库历史记录中清除文件](#purge-files-from-repository-history) .

除了[分支](/docs/user/project/repo/branches.md)和标签（这是一种 Git 引用）之外，系统还会自动创建其他引用，[代码仓库清理](#repository-cleanup)可用于从 CODEChina 中删除它们.

以下为内部参考文献：

*   `refs/merge-requests/*`用于合并请求
*   `refs/pipelines/*` 用于 pipelines
*   `refs/environments/*`用于环境

这意味着在获取时通常不包含它们，这使得获取速度更快。另外， `refs/keep-around/*`是隐藏的 refs，以防止与讨论相关的提交被删除并且根本无法被获取。但是，可以从项目导出内的 Git 捆绑包访问这些引用：

1.  使用受支持的程序包管理器或从源代码[安装`git filter-repo`](https://github.com/newren/git-filter-repo/blob/main/INSTALL.md) 

2.  [从项目中](/docs/user/project/import.md#exporting-a-project-and-its-data)生成一个新的[导出](/docs/user/project/import.md#exporting-a-project-and-its-data)并下载

3.  使用`tar`解压缩备份：

    ```markdown
    tar xzf project-backup.tar.gz 
    ```

    这将包含一个由[`git bundle`](https://git-scm.com/docs/git-bundle)创建的`project.bundle`文件

4.  从包中克隆存储库的新副本：

    ```markdown
    git clone --bare --mirror /path/to/project.bundle 
    ```

5.  使用`git filter-repo` ，从代码仓库的历史记录中清除所有文件。因为我们正在尝试删除内部引用，所以我们将依靠每次运行生成的`commit-map`来告诉我们要删除哪些内部引用。

    **注意：** `git filter-repo`每次运行都会创建一个新的`commit-map`文件，并覆盖前一次运行的`commit-map`
    
    **每次**运行都将需要此文件，每次运行`git filter-repo`都要执行下一步

    要清除所有大文件，可以使用`--strip-blobs-bigger-than`选项：

    ```markdown
    git filter-repo --strip-blobs-bigger-than 10M 
    ```

    要按路径清除特定的大文件，可以组合使用`--path`和`--invert-paths`选项

    ```markdown
    git filter-repo --path path/to/big/file.m4v --invert-paths 
    ```

    有关更多示例和完整文档，请参见[`git filter-repo`](https://htmlpreview.github.io/?https://github.com/newren/git-filter-repo/blob/docs/html/git-filter-repo.html#EXAMPLES)文档

6.  运行[代码仓库清理](#repository-cleanup) 

## 代码仓库清理[](#repository-cleanup "Permalink")

代码仓库清理允许您上传对象的文本文件，并且 CODEChina 将删除对这些对象的内部 Git 引用。您可以使用[`git filter-repo`](https://github.com/newren/git-filter-repo)生成对象列表（在`commit-map`文件中），该对象列表可与存储库清理一起使用。

要清理代码仓库：

1.  转到项目的代码仓库
2.  进入 **项目设置>仓库>仓库清理** 
3.  上载对象列表，例如，一个`commit-map`文件
4.  点击**开始清理**

这将：

*   删除所有对旧提交的内部 Git 引用
*   针对存储库运行`git gc` 

完成后，您将收到一封电子邮件。

当在使用代码仓库清理时，需要注意：

*   项目统计信息已缓存，您可能需要等待 5 到 10 分钟才能看到存储利用率下降
*   Housekeeping 会精简2周以上的松散物品，这意味着在最近 2 周内添加的对象将不会被立即删除
*   此过程将从 CODEChina 的缓存和数据库中删除一些重写提交的副本，但是覆盖范围仍然存在许多空白，并且某些副本可能会无限期地存在

## 仓库大小限制[](#storage-limits "Permalink")

仓库大小限制由管理员在实例上设置。

当项目达到其大小限制时，您不能：

*   推送到项目
*   创建一个新的合并请求
*   合并现有的合并请求
*   上载 LFS 对象

您仍然可以：

*   创造新问题
*   克隆项目

如果超出存储库大小限制，则可以尝试：

1.  删除一些数据
2.  进行新的提交
3.  推回代码仓库
   
也许您还可以：

*   将一些 blob 移到 LFS
*   从历史记录中删除一些旧的依赖项更新

实际上，在提交中删除文件并不会减小存储库的大小，因为早期的提交和 Blob 仍然存在。

您需要做的是重写历史记录，我们建议使用开源社区维护的工具[`git filter-repo`](https://github.com/newren/git-filter-repo) 