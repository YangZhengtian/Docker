# docker 镜像Aliyun加速

* 注册Aliyun并登陆，进入Docker镜像仓库: <https://cr.console.aliyun.com>。
* 选择 *Docker Hub 镜像站点*，得到自己专属加速地址。
* 运行Docker，在设置中找到*Daemon*栏，在*Insecure registers:*中输入*register.mirrors.aliyuncs.com*，将专属加速地址copy到*Registry mirrors* 中。
* Apply应用重启Docker。

