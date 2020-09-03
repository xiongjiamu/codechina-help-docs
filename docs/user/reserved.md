# 预留命名空间[](#预留命名空间 "Permalink")

出于系统安全、商标及知识保护等方面的考虑，在设置用户或组织的命名空间时并非所有的名称都会被允许。

有关不允许用作组名或项目名的单词的列表，请参阅`TOP_LEVEL_ROUTES` ， `PROJECT_WILDCARD_ROUTES`和`GROUP_ROUTES`列表下的[`path_regex.rb`](https://gitlab.com/gitlab-org/gitlab/blob/master/lib/gitlab/path_regex.rb)文件：

*   `TOP_LEVEL_ROUTES` ：是为用户名或顶级组织保留的名称
*   `PROJECT_WILDCARD_ROUTES` ：是为子组或项目保留的名称
*   `GROUP_ROUTES` ：是为所有组或项目保留的名称

## 预留的项目名[](#reserved-project-names "Permalink")

当前无法创建具有以下名称的项目：

*   `\-`
*   `badges`
*   `blame`
*   `blob`
*   `builds`
*   `commits`
*   `create`
*   `create_dir`
*   `edit`
*   `environments/folders`
*   `files`
*   `find_file`
*   `gitlab-lfs/objects`
*   `info/lfs/objects`
*   `new`
*   `preview`
*   `raw`
*   `refs`
*   `tree`
*   `update`
*   `wikis`

## 预留的组织名[](#reserved-group-names "Permalink")

当前，以下是顶级组织的预留名称：

*   `\-`
*   `.well-known`
*   `404.html`
*   `422.html`
*   `500.html`
*   `502.html`
*   `503.html`
*   `abuse_reports`
*   `admin`
*   `api`
*   `apple-touch-icon-precomposed.png`
*   `apple-touch-icon.png`
*   `assets`
*   `autocomplete`
*   `dashboard`
*   `deploy.html`
*   `explore`
*   `favicon.ico`
*   `favicon.png`
*   `files`
*   `groups`
*   `health_check`
*   `help`
*   `import`
*   `invites`
*   `jwt`
*   `login`
*   `oauth`
*   `profile`
*   `projects`
*   `public`
*   `robots.txt`
*   `s`
*   `search`
*   `sent_notifications`
*   `slash-command-logo.png`
*   `snippets`
*   `unsubscribes`
*   `uploads`
*   `users`
*   `v2`

这些组名不能用作子组名：

*   `\-`