## 操作场景
为提升用户在云服务器上的软件安装效率，减少下载和安装软件的成本，腾讯云提供了 YUM 下载源。在 CentOS 环境下，用户可通过 `yum` 命令快速安装软件。对于 YUM 下载源，用户不需要添加软件源，可以直接安装软件包。

## 操作步骤

### 安装软件

1. 使用 root 账号登录云服务器。
2. 执行以下命令，安装软件。
>! 从 CentOS 7 系统开始，MariaDB 成为 YUM 源中默认的数据库安装包。如果您的操作系统为 CentOS 7 及以上版本，使用 `yum` 命令安装 MySQL 包时将无法使用 MySQL。您可以选择使用完全兼容的 MariaDB，或者 [点此参阅](https://www.linode.com/docs/databases/mysql/how-to-install-mysql-on-centos-7) 进行较低版本的 MySQL 的安装。
>
```
yum install 软件名称
``` 
安装软件的过程中，系统将自动搜索相关的软件包和依赖关系，并在界面中提示用户确认搜索到的软件包是否合适。
例如，您执行 `yum install PHP` 命令，安装 PHP 后，界面显示如下图：
![](https://main.qcloudimg.com/raw/18c4a59a3e0e92b0dcafff662d1e3673.png)
4. 确认软件包合适无误后，输入 `y`，开始安装软件。
界面提示 `Complete` 即安装完成。如下图所示：
![](https://main.qcloudimg.com/raw/fb2fbd8becd4576f67b47226a82ee033.png)

### 查看已安装软件的信息

软件安装完成后，可根据实际需求，执行不同的命令，查看信息。
- 执行以下命令，查看软件包具体的安装目录。
```
rpm -ql 软件名
```
例如，您执行 `rpm -ql PHP` 命令，查看 PHP 具体的安装目录。如下图所示：
![](https://main.qcloudimg.com/raw/fda98060c9f6ba359d7e705de8d336bb.png)
- 执行以下命令，查看软件包的版本信息。
```
rpm -q
```
例如，您执行 `rpm -q PHP` 命令，查看 PHP 的版本信息。如下图所示：
![](https://main.qcloudimg.com/raw/35e1ecee46bc55a5d2510dce59360ecc.png)


