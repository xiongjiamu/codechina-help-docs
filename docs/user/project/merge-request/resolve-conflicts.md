# 解决合并冲突[](#resolve-conflicts "Permalink")

当合并请求中的两个分支具有无法自动合并的不同更改时，将导致合并冲突。

在大多数情况下，Git 能够自动合并分支之间的更改，但是在某些情况下，Git 需要您的帮助来手动解决冲突。通常，当人们更改了同一文件的相同部分时，这就需要手动来解决冲突了。

在解决所有冲突之前，系统将阻止合并请求。冲突可以在本地解决，许多情况下在 CODEChina 网页上也可以解决（有关何时可用的信息，请参见可解决的[冲突](#conflicts-available-for-resolution) ）。

[![Merge request widget](/docs/img/merge_request_widget.png)](/docs/img/merge_request_widget.png)

**注意：** CODEChina 通过在未自动合并到目标分支的源分支中创建合并提交来解决冲突，这样可以在合并更改之前在源分支对合并提交进行检查和测试，从而在更改进入目标分支前防止没有检查或破坏构建导致的意外。

## 交互模式[](#resolve-conflicts-interactive-mode "Permalink")

单击此按钮将显示有冲突的文件列表，突出显示冲突部分：

[![Conflict section](/docs/img/conflict_section.png)](/docs/img/conflict_section.png)

当所有冲突都标记为使用"我们的"或"他们的"时，则可以解决冲突。这将执行合并请求的目标分支到源分支的合并，并使用选择的选项解决冲突。如果源分支是`feature` ，目标分支是`master` ，则类似于执行`git checkout feature; git merge master` `git checkout feature; git merge master`本地`git checkout feature; git merge master` 。

## 内联编辑模式[](#resolve-conflicts-inline-editor "Permalink")

合并冲突编辑模式可以让您在 CODEChina 界面中解决更复杂的合并冲突，比如需要用户手动修改文件才能解决的冲突。使用**内联编辑**按钮打开编辑器. 确定更改后，请单击**提交到源分支**按钮。

[![Merge conflict editor](/docs/img/merge_conflict_editor.png)](/docs/img/merge_conflict_editor.png)

## 可解决的冲突[](#conflicts-available-for-resolution "Permalink")

CODEChina 界面只允许解决以下所有条件均成立的文件中的冲突：

*   该文件是文本，不是二进制
*   该文件采用 UTF-8 兼容编码
*   该文件尚未包含冲突标记
*   添加了冲突标记的文件大小不超过 200 KB
*   该文件在两个分支中位于相同路径下

如果该合并请求中有冲突的任何文件均不满足所有这些条件，则无法在界面中解决该合并请求的冲突。

此外，系统不会在路径之外的重命名中检测到冲突。例如，以下这些情况将不会造成冲突：在分支`a`执行`git mv file1 file2` ； 在分支`b` ，执行`git mv file1 file3` 。相反的，合并后，两个文件都将出现在分支中。