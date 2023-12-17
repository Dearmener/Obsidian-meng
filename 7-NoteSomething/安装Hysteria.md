[自建hysteria服务器教程 · Alvin9999/new-pac Wiki · GitHub](https://github.com/Alvin9999/new-pac/wiki/%E8%87%AA%E5%BB%BAhysteria%E6%9C%8D%E5%8A%A1%E5%99%A8%E6%95%99%E7%A8%8B)
**hysteria 1一键部署管理脚本：**
```shell
bash <(curl -fsSL https://git.io/hysteria.sh)
```

> 如果输入安装命令后提示curl: command not found，那是因为服务器系统没有自带curl命令，安装一下curl。
> CentOS系统安装curl命令：yum install -y curl
> Debian/Ubuntu系统安装curl命令：apt-get install -y curl
> 安装完成后，输入hihy可进入管理页面。脚本来自[emptysuns/Hi_Hysteria](https://github.com/emptysuns/Hi_Hysteria)。

---

复制上面的**脚本代码**到VPS服务器里，复制代码用鼠标右键的复制，然后在vps里面右键粘贴进去，因为ctrl+c和ctrl+v无效。接着按回车键，脚本会自动安装，以后只需要运行这个快捷命令就可以出现下图的界面进行设置，快捷管理命令为：hihy

![](https://camo.githubusercontent.com/abace40e198b76beb2a6f86629232455ebb383bb9b4211f9da270167d38c7802/68747470733a2f2f666173746c792e6a7364656c6976722e6e65742f67682f416c76696e393939392f706163322f76756c74722f6879312e706e67)

如上图出现管理界面后，**输入数字1来安装**。

![](https://camo.githubusercontent.com/4c518a31299bf3a87556b0d55806498e3ed8b928990413b7aa47ce1997739f9d/68747470733a2f2f666173746c792e6a7364656c6976722e6e65742f67682f416c76696e393939392f706163322f76756c74722f6879322e706e67)

选择数字3来安装证书，如果有域名，可以选择数字1或者3来安装证书，没有域名就选择数字3

![](https://camo.githubusercontent.com/003ad44c8865d67f693118593abf74983ac8563e66104f316df16a3e89e2b7cf/68747470733a2f2f666173746c792e6a7364656c6976722e6e65742f67682f416c76696e393939392f706163322f76756c74722f6879332e706e67)

自签证书默认是wechat.com 回车即可

![](https://camo.githubusercontent.com/fe5795ba2a12a2a2451cdb5de7fc49842586360b71163634794afa4c2bdc0cc9/68747470733a2f2f666173746c792e6a7364656c6976722e6e65742f67682f416c76696e393939392f706163322f76756c74722f6879342e706e67)

账号端口也可以回车，或者输入想要的端口号

协议类型很重要：没有域名只能选择数字1的upd协议类型，其它2个都用不了。如果有域名，那么会多一个选择，可以选择udp或者wechat-video，如果选择wechat-video后需要填写自己的域名。faketcp模式需要电脑是linux。

![](https://camo.githubusercontent.com/62a3238668196d56826c6db669ecc842e5bc4023d690fa79991af3ee552440df/68747470733a2f2f666173746c792e6a7364656c6976722e6e65742f67682f416c76696e393939392f706163322f76756c74722f6879352e706e67)

延迟、上传、下载都可以用默认的配置，也可以自己修改，默认就回车

接着会提醒输入认证口令，就是密码，可以自己输入想要的

![](https://camo.githubusercontent.com/0775e3b09097ea8d6ce27fb9d32165e91136aa227b0bd84771e4b14e197f0a77/68747470733a2f2f666173746c792e6a7364656c6976722e6e65742f67682f416c76696e393939392f706163322f76756c74722f6879362e706e67)

一般提示安装成功，请查看下方配置详细信息就说明安装成功了。如果失败会有相应的提示，一般解决方法就是卸载脚本后重新安装。

![](https://camo.githubusercontent.com/cf8629b42712041f306d58b96a26364bc7a3538c8df4ec00249b3cf552b73fcd/68747470733a2f2f666173746c792e6a7364656c6976722e6e65742f67682f416c76696e393939392f706163322f76756c74722f6879372e706e67)

带大括号的就是整个配置信息，需要复制下来，用鼠标右键有复制。在电脑上新建一个**config.json**的文件，把配置信息粘帖进去。需要**注意**的是：**有两行必须删除**，不然会无法启动hysteria客户端。这两行信息是：

"acl": "acl/routes.acl",

"mmdb": "acl/Country.mmdb",

**连带标点符号一起删除。**

有了配置文件，接下来就是下载hysteria客户端。

**hysteria 2一键部署管理脚本：**
```shell
wget -N --no-check-certificate https://raw.githubusercontent.com/flame1ce/hysteria2-install/main/hysteria2-install-main/hy2/hysteria.sh && bash hysteria.sh
```
接下来只需要默认回车即可
> 如果输入安装命令后提示wget: command not found，那是因为服务器系统没有自带wget命令，安装一下wget。
> CentOS系统安装curl命令：yum install -y wget
> Debian/Ubuntu系统安装curl命令：apt-get install -y wget

hysteria官方客户端下载地址：[https://github.com/apernet/hysteria/releases](https://github.com/apernet/hysteria/releases)

## 如何使用
使用Hysteria协议需要安装对应的软件，如果使用Clash，需要替换clash core

### 如何替换clash core
1. 从[Releases · MetaCubeX/Clash.Meta · GitHub](https://github.com/MetaCubeX/Clash.Meta/releases)这里下载相应平台的内核，Windows就下载带有Windows的64位软件即可
	 ![[Pasted image 20231012100215.png]]
	下载完成后，解压获得
	![[Pasted image 20231012100500.png]]
	将其改名为`clash-win64.exe`
1. 打开本机Clash的文件目录
	`Clash for Windows\resources\static\files\win\x64`
3. 替换其中的`clash-win64.exe`为解压后的文件。
4. 重启clash即可
5. 