# 个人访问令牌[](#token "Permalink")

个人访问令牌在您定义的日期 UTC 午夜到期。

*   系统每天在世界标准时间 01:00 AM 进行检查，以识别将在 7 天内到期的个人访问令牌，并向这些令牌的所有者发送电子邮件通知。

## 创建个人访问令牌[](#creating-a-personal-access-token "Permalink")

您可以在 CODEChina 个人资料中创建任意数量的个人访问令牌：

1.  登录到 CODEChina
2.  点击右上角的头像，然后选择**设置** 
3.  在" **用户设置"**菜单上，选择" **访问令牌"** 
4.  选择令牌的名称和可选的到期日期.
5.  选择[所需的范围](#limiting-scopes-of-a-personal-access-token) 
6.  单击**创建个人访问令牌**按钮
7.  将个人访问令牌保存在安全的地方，离开或刷新页面后，将无法再次访问它

### 撤消个人访问令牌[](#revoking-a-personal-access-token "Permalink")

您可以随时单击" **活动个人访问令牌"**区域下的相应" **撤消"**按钮来撤消任何个人访问令牌。

### 令牌活动记录[](#token-activity "Permalink")

您可以从" **个人访问令牌"**页面**查看**上次使用**令牌的时间** ， 令牌使用情况的更新每 24 小时固定一次。对API 资源和GraphQL API 的请求将更新令牌的用法。

## 个人访问令牌可用范围[](#limiting-scopes-of-a-personal-access-token "Permalink")

可以使用一个或多个范围创建个人访问令牌，这些范围允许给定令牌可以执行各种操作，下表描述了可用范围：

| Scope | 引入 | Description |
| --- | --- | --- |
| `read_user` | [GitLab 8.15](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/5951) | 允许访问`/users`下的只读端点。本质上，允许用户 API中的任何`GET`请求 |
| `api` | [GitLab 8.15](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/5951) | 授予对 API 的完全读写访问权限，包括所有组和项目，容器注册表和程序包注册表 |
| `read_api` | [GitLab 12.10](https://gitlab.com/gitlab-org/gitlab/-/merge_requests/28944) | 授予对 API 的读取权限，包括所有组和项目，容器注册表和程序包注册表 |
| `read_registry` | [GitLab 9.3](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/11845) | 如果项目是私有的并且需要授权，则允许读取（拉出） 容器注册表图像 |
| `sudo` | [GitLab 10.2](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/14838) | 允许以系统中的任何用户身份执行 API 操作（如果经过身份验证的用户是管理员） |
| `read_repository` | [GitLab 10.7](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/17894) | 允许通过`git clone`对存储库进行只读访问（拉） |
| `write_repository` | [GitLab 11.11](https://gitlab.com/gitlab-org/gitlab-foss/-/merge_requests/26021) | 允许通过`git clone`对存储库进行读写访问（拉，推）。 启用 2FA 时，通过 HTTP 访问 Git 存储库是必需的 |