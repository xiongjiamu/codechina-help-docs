# SSH密钥[](#ssh "Permalink")

Git 是一个分布式版本控制系统，这意味着您可以在本地工作. 此外，您还可以将更改共享或"推送"到其他服务器. CODEChina 支持使用 SSH 密钥在 Git 及其服务器之间进行安全通信.

SSH 协议提供的这种安全机制，并允许您向 CODEChina 远程服务器进行身份验证，而无需每次都提供用户名或密码，我们推荐您使用这种方式来作为您推拉代码的凭据。

通过阅读本文档可以帮助您配置安全的 SSH 密钥，这些密钥可用于帮助保护与 CODEChina 代码仓库的安全连接。

*   如果您需要有关创建 SSH 密钥的信息，请从我们的[ SSH 密钥选项](#options-for-ssh-keys)开始
*   如果您有专用于 CODEChina 帐户的 SSH 密钥，则可能对[使用非默认 SSH 密钥对路径](#working-with-non-default-ssh-key-pair-paths)感兴趣
*   如果您已经有了 SSH 密钥对，则可以转到[将 SSH 密钥添加到 CODEChina 帐户的方法](#adding-an-ssh-key-to-your-gitlab-account) 

## 环境要求[](#requirements "Permalink")

为了支持 SSH，CODEChina 需要安装 OpenSSH 客户端，该客户端已预装在 GNU / Linux 和 macOS 上，但未预先安装在 Windows 上。

我们要求您使用 SSH 6.5 或更高版本，因为它不包括现在不安全的 MD5 签名。您可以通过下命令查看系统上安装的 SSH 版本：

```
ssh -V 
```

## SSH 密钥选项[](#options-for-ssh-keys "Permalink")

CODEChina 支持使用 RSA，DSA，ECDSA 和 ED25519 密钥。

**提示：**现有文档表明 ED25519 更安全，如果使用 RSA 密钥，则美国国家科学技术研究院[出版物 800-57 第 3 部分（PDF）](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-57Pt3r1.pdf)建议密钥大小至少为 2048 位。

因此，我们主要介绍 ED25519 和 RSA 这两种密钥的使用方法。

## 查看现有的 SSH 密钥[](#review-existing-ssh-keys "Permalink")

如果您已有 SSH 密钥，则可以使用它们来与 CODEChina 的代码库进行连接。 默认情况下，Linux 和 macOS 系统上的 SSH 密钥存储在用户的主目录中的`.ssh/`子目录中，下表包括每种 SSH 密钥算法的默认文件名：

| 算法 | 公钥 | 私钥 |
| --- | --- | --- |
| ED25519（首选） | `id_ed25519.pub` | `id_ed25519` |
| RSA（至少 2048 位密钥大小） | `id_rsa.pub` | `id_rsa` |
| DSA（已弃用） | `id_dsa.pub` | `id_dsa` |
| ECDSA | `id_ecdsa.pub` | `id_ecdsa` |

有关建议，请查看[SSH 密钥的选项](#options-for-ssh-keys) 。

## 生成 SSH 密钥[](#generating-a-new-ssh-key-pair "Permalink")

SSH 密钥的生成方式如下：

*   ED25519 密钥，请查看[ED25519 SSH 密钥](#ed25519-ssh-keys)
*   RSA 密钥，请查看[RSA SSH 密钥](#rsa-ssh-keys) 

### ED25519 SSH keys[](#ed25519-ssh-keys "Permalink")

[Practical Cryptography With Go](https://leanpub.com/gocrypto/read#leanpub-auto-chapter-5-digital-signatures) 一书中表明 [ED25519](https://ed25519.cr.yp.to/) 密钥比 RSA 密钥更为安全。

2014年 OpenSSH 6.5 引入 ED25519 SSH 密钥后，当前任何操作系统都可用使用这种密钥。

您可以使用以下命令创建和配置 ED25519 密钥：

```
ssh-keygen -t ed25519 -C "<comment>" 
```

`-C`（例如带引号注释的电子邮件地址）是标记 SSH 密钥的可选方法。

您将看到类似于以下内容的响应：

```
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/user/.ssh/id_ed25519): 
```

要获得指导，请继续执行[常见步骤](#common-steps-for-generating-an-ssh-key-pair) .

### RSA SSH 密钥[](#rsa-ssh-keys "Permalink")

如果您使用 RSA 密钥生成 SSH 密钥，则我们建议您至少使用 [ 2048 位](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-57Pt3r1.pdf)的密钥大小. 默认情况下， `ssh-keygen`命令创建一个 1024 位 RSA 密钥.

您可以使用以下命令创建和配置 RSA 密钥，如果需要，可以生成建议的最小密钥大小`2048`：

```
ssh-keygen -t rsa -b 2048 -C "email@example.com" 
```

`-C`标志（例如带引号注释的电子邮件地址）是标记 SSH 密钥的可选方法。

您将看到类似于以下内容的响应：

```
Generating public/private rsa key pair.
Enter file in which to save the key (/home/user/.ssh/id_rsa): 
```

要获得指导，请继续执行[常见步骤](#common-steps-for-generating-an-ssh-key-pair) 。

**注意：**如果您使用 7.8 或更低版本的 OpenSSH，请参考与[编码](#rsa-keys-and-openssh-from-versions-65-to-78)相关的问题。

### SSH 密钥生成步骤[](#common-steps-for-generating-an-ssh-key-pair "Permalink")

无论是创建[ED25519](#ed25519-ssh-keys)还是创建[RSA](#rsa-ssh-keys)密钥，您都从`ssh-keygen`命令开始。此时，您将在命令行中看到以下消息（以 ED25519 密钥为例）：

```
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/user/.ssh/id_rsa): 
```

如果您还没有 SSH 密钥对并且也没有生成[部署密钥](#deploy-keys) ，您可以按照系统提示的建议选择 SSH 密钥存储的文件和目录，SSH 客户端将使用默认配置来生成您的 SSH 密钥。

当然，您也可以将新生成的 SSH 密钥保存在其他位置。您可以选择要分配的目录和文件名，您还可以为专用的[特定主机](#working-with-non-default-ssh-key-pair-paths) 生成SSH 密钥。

在选择 SSH 密钥的保存路径后，您可以为 SSH 密钥设置[密码](https://www.ssh.com/ssh/passphrase/) ：

```
Enter passphrase (empty for no passphrase):
Enter same passphrase again: 
```

如果成功，您将看到有关`ssh-keygen`命令将标识和私钥保存在何处的确认信息。

如有需要，您也可以使用以下命令更新密码：

```
ssh-keygen -p -f /path/to/ssh_key 
```

### OpenSSH 6.5 ~ 7.8 的 RSA 密钥[](#rsa-keys-and-openssh-from-versions-65-to-78 "Permalink")

在 OpenSSH 7.8 之前，RSA 密钥的默认公共密钥指纹基于 MD5，因此并不安全。

如果您的 OpenSSH 版本介于 6.5 至 7.8（含）之间，请使用`-o`选项运行`ssh-keygen` ，以更安全的 OpenSSH 格式保存您的 SSH 私钥。

如果您已经具有可用于 CODEChina 的 RSA SSH 密钥，请考虑对其进行升级以使用更安全的密码加密格式。 您可以使用以下命令进行操作：

```
ssh-keygen -o -f ~/.ssh/id_rsa 
```

或者，您可以使用以下命令以更安全的加密格式生成新的 RSA 密钥：

```
ssh-keygen -o -t rsa -b 4096 -C "email@example.com" 
```

**注意：**ED25519 已将密钥加密为更安全的 OpenSSH 格式。

## 在您的 CODEChina 账号中添加 SSH 密钥[](#adding-an-ssh-key-to-your-account "Permalink")

现在，您可以将创建好的 SSH 密钥复制到您的 CODEChina 帐户。您可以参考以下步骤：

1.  从以文本格式保存 SSH 密钥的位置复制您的**公共** SSH 密钥，以下命令可以将 ED25519 的信息保存到指定操作系统的剪贴板中：

    **macOS:**

    ```
    pbcopy < ~/.ssh/id_ed25519.pub 
    ```

    **Linux（需要 xclip 软件包）：**

    ```
    xclip -sel clip < ~/.ssh/id_ed25519.pub 
    ```

    **Windows 上的 Git Bash：**

    ```
    cat ~/.ssh/id_ed25519.pub | clip 
    ```

    如果您使用的是 RSA 密钥，相应地替换即可。

2.  打开`https://codechina.csdn.net`并登录
3.  选择右上角的头像，然后单击**设置**
4.  单击 **SSH 密钥**.
5.  将复制的公共密钥粘贴到**密钥**文本框中.
6.  在**标题**文本框中设置您密钥的名称，例如 *工作笔记本电脑*或 *家用电脑* 
7.  在"过期于"中设置密钥的过期日期（可选）
8.  单击**添加密钥**按钮

按照上述步骤添加的 SSH 密钥即使"过期"后在工作流程中仍然有效，由于配置的到期日期信息并不包含在 SSH 密钥本身中，因此您仍然可以根据需要导出公共 SSH 密钥。

**注意：**如果您手动复制了公共 SSH 密钥，请确保复制了整个密钥，以`ssh-ed25519` （或`ssh-rsa` ）开头，并以您的电子邮件地址结尾。

## 测试 SSH 密钥是否能够正常工作[](#testing-that-everything-is-set-up-correctly "Permalink")

要测试是否正确添加了 SSH 密钥，可以在终端中运行以下命令：

```
ssh -T git@codechina.csdn.net
```

在您第一次通过 SSH 方式连接到 CODEChina的时候，将会询问您是否信任将要连接的 CODEChina host地址。当确认 `yes` 后，会将 CODEChina 作为已知主机添加到受信任的 hosts 地址中：

```
The authenticity of host 'codechina.csdn.net (121.36.6.22)' can't be established.
ECDSA key fingerprint is SHA256:HbW3g8zUjNSksFbqTiUWPWg2Bq1x8xdGUrliXFzSnUw.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added 'codechina.csdn.net' (ECDSA) to the list of known hosts. 
```

一旦添加到已知主机列表中，将不再要求您再次验证 CODEChina 主机的真实性。 再次运行以上命令时，您将只收到*欢迎使用 CODEChina 的`@username` ！* 信息。

如果未出现欢迎消息，则可以通过使用以下命令在详细模式下运行`ssh`来解决问题：

```
ssh -Tv git@codechina.csdn.net 
```

## 使用非默认路径的 SSH 密钥[](#working-with-non-default-ssh-key-pair-paths "Permalink")

如果您为 SSH 密钥对使用了非默认文件路径，请配置 SSH 客户端以指向 CODEChina 私有 SSH 密钥。

可以运行以下命令进行配置：

```
eval $(ssh-agent -s)
ssh-add <path to private SSH key> 
```

以上设置将会保存到`~/.ssh/config`文件中。以下是两个专用于 CODEChina 的 SSH 密钥示例：

```
# CODEChina
  Host codechina.csdn.net
  Preferredauthentications publickey
  IdentityFile ~/.ssh/codechina_rsa

# Github instance
  Host github.com
  Preferredauthentications publickey
  IdentityFile ~/.ssh/example_github_rsa 
```

公共 SSH 密钥对于 CODEChina 必须是唯一的，因为它们将绑定到您的账号中。 SSH 密钥是通过 SSH 推送代码时唯一的标识符，这是为什么它需要唯一地映射到单个用户的原因。

## 为项目设置 SSH 密钥[](#per-repository-ssh-keys "Permalink")

如果要根据正在使用的项目代码仓库使用不同的密钥，则可以在代码仓库中执行以下命令：

```
git config core.sshCommand "ssh -o IdentitiesOnly=yes -i ~/.ssh/private-key-filename-for-this-repository -F /dev/null" 
```

这不使用 SSH 代理，并且至少需要 Git 2.10.

## 多账号设置[](#multiple-accounts-on-a-single-gitlab-instance "Permalink")

[为项目设置 SSH 密钥](#per-repository-ssh-keys)方法还适用于在 CODEChina 中使用多个账号的情况。

此外，您也可以直接在`~.ssh/config`为主机分配别名。 如果在`.ssh/config`中的`Host`块之外设置了`IdentityFile` ，则 SSH 和作为扩展的 Git 将无法登录. 这是 SSH 组装`IdentityFile`条目的方式，因此不能通过将`IdentitiesOnly`设置为`yes`来更改. `IdentityFile`条目应指向 SSH 密钥对的私钥。

**注意：**私钥和公钥应仅由用户读取，通过运行以下`chmod 0400 ~/.ssh/<example_ssh_key>`在 Linux 和 macOS 上完成此操作： `chmod 0400 ~/.ssh/<example_ssh_key>`和`chmod 0400 ~/.ssh/<example_sh_key.pub>` 。

```
# User1 Account Identity Host <user_1.codechina.csdn.net>
  Hostname codechina.csdn.net
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<example_ssh_key1>

# User2 Account Identity Host <user_2.codechina.csdn.net>
  Hostname codechina.csdn.net
  PreferredAuthentications publickey
  IdentityFile ~/.ssh/<example_ssh_key2> 
```

**注意：**为提高效率和透明度，示例`Host`别名定义为`user_1.codechina.csdn.net`和`user_2.codechina.csdn.net` 。 高级配置难以维护，使用这种别名在使用其他工具（如`git remote`子命令）时会更容易理解。 SSH 可以将任何字符串理解为`Host`别名，因此`Tanuki1`和`Tanuki2`尽管提供了很少的上下文指向它们，也可以使用.

克隆`CODEChina`代码仓库通常如下所示：

```
git clone git@gcodechina.csdn.net:repo-org/repo.git 
```

要为`user_1`克隆它，请将`codechina.csdn.net`替换为 SSH 别名`user_1.codechina.csdn.net` ：

```
git clone git@<user_1.codechina.csdn.net>:repo-org/repo.git 
```

使用`git remote`命令可以修复以前克隆的代码仓库。

以下的示例假定远程代码仓库被别名为`origin`：

```
git remote set-url origin git@<user_1.codechina.csdn.net>:repo-org/repo.git 
```

### Eclipse[](#eclipse "Permalink")

如果使用的是[EGit](https://www.eclipse.org/egit/) ，则可以[将 SSH 密钥添加到 Eclipse](https://wiki.eclipse.org/EGit/User_Guide#Eclipse_SSH_Configuration) .

### Windows系统[](#options-for-microsoft-windows "Permalink")

如果您运行的是 Windows 10， [适用于 Linux](https://docs.microsoft.com/en-us/windows/wsl/install-win10)的[Windows 子系统（WSL）](https://docs.microsoft.com/en-us/windows/wsl/install-win10)及其最新的[WSL 2](https://docs.microsoft.com/en-us/windows/wsl/install-win10#update-to-wsl-2)版本，则支持安装不同的 Linux 发行版，其中包括 Git 和 SSH 客户端。

对于当前版本的 Windows，您还可以通过[Git for Windows](https://gitforwindows.org)安装 Git 和 SSH 客户端。

替代工具包括：

*   [Cygwin](https://www.cygwin.com)
*   [PuttyGen](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html)

## 故障排除[](#troubleshooting "Permalink")

如果在 Git Clone 上，系统会提示您输入密码，例如`git@codechina.csdn.net's password:`，则表明您的 SSH 设置有问题。

*   确保您正确地生成了 SSH 密钥，并将公共 SSH 密钥添加到了您 CODEChina 账号的 SSH 密钥中
*   尝试使用`ssh-agent`手动注册您的私有 SSH 密钥，如本文档前面所述
*   尝试通过运行`ssh -Tv git@codechina.csdn.net`调试连接