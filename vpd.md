## 准备

RackNerd便宜服务器1台

- 成立于 2017 年，美国老牌服务器供应商
- 优先选择洛杉矶Los Angeles DC02、圣何塞San Jose
- 终身续费同价
- 3天内免费更换1次IP，不用担心失联
- 终身免费流量翻倍：只需要简单的福利回帖操作，就能翻倍
- 支付方式灵活，支持 PayPal、信用卡、支付宝
- 7x24小时客服，支持中文



| CPU  | 内存  | SSD硬盘 |      月流量带宽      |   优惠价格    |                           点击购买                           |
| :--: | :---: | :-----: | :------------------: | :-----------: | :----------------------------------------------------------: |
| 1 核 |  1 G  |  25 G   |  2 TB流量/月 @1Gbps  | **$10.6/年**  | **[官网链接](https://my.racknerd.com/aff.php?aff=17562&pid=923)** |
| 2 核 | 2.5 G |  45 G   |  3 TB流量/月 @1Gbps  | **$18.66/年** | **[官网链接](https://my.racknerd.com/aff.php?aff=17562&pid=924)** |
| 3 核 |  4 G  |  65 G   | 6.5 TB流量/月 @1Gbps | **$29.98/年** | **[官网链接](https://my.racknerd.com/aff.php?aff=17562&pid=925)** |
| 5 核 |  6 G  |  100 G  | 10 TB流量/月 @1Gbps  | **$44.98/年** | **[官网链接](https://my.racknerd.com/aff.php?aff=17562&pid=926)** |
| 6 核 |  8 G  |  150 G  | 20 TB流量/月 @1Gbps  | **$62.49/年** | **[官网链接](https://my.racknerd.com/aff.php?aff=17562&pid=927)** |



IP地址纯净度查询：https://www.ping0.cc/



## 流量翻倍教学

### 01-LET论坛注册账号

官方地址：https://lowendtalk.com/
注册理由what do you want to join？：

```bash
Hello, I would like to register for the forum and purchase a cost-effective VPS. Thank you！
```

![image-20251230152217151](img/image-20251230152217151.png) 

![image-20251230152257514](img/image-20251230152257514.png) 

如果没有使用魔法，注册信息填写完之后会报验证错误：the captcha was not completed correctly.please try again.

![image-20251230152438131](img/image-20251230152438131.png) 

注册信息提交之后，邮箱会收到一封验证邮件

![image-20251230152516309](img/image-20251230152516309.png) 

![image-20251230152539398](img/image-20251230152539398.png) 

确认邮箱之后，大概过了20分钟左右才正式被激活。

![image-20251230152603056](img/image-20251230152603056.png) 



### 02-获取RackNerd订单号

登录RackNerd后台，点击【view email log】可以看到之前购买服务器发送的发票邮件

https://my.racknerd.com/index.php?rp=/login

找到对应的服务器，复制invoice

![image-20251230152829106](img/image-20251230152829106.png) 



### 03-LET论坛回帖申请

RackNerd流量翻倍帖子(任意可以）：

https://lowendtalk.com/discussion/211640/trending-now-racknerd-s-black-friday-new-deals-new-locations-new-hardware-100-s-of-giveaways#latest

如果注册账号还没有被激活，会看到以下页面，无法进行发帖或回复帖子

![image-20251230153148013](img/image-20251230153148013.png) 

注册账号激活之后，再次打开申请帖子，拉到最底部回复帖子模板：

把12345678，换成你的订单号

```
Hello, I would like to double my bandwidth.
Invoice #12345678
Thanks!
```

![image-20251230153311772](img/image-20251230153311772.png) 

正常大概3个工作日内，如果官方dustinc回复如下信息，说明流量翻倍成功。

实测11月4日提交，11月17日回复翻倍成功！可能这段时间促销旺季比较忙。

登录LET论坛，在消息提醒里面可以看到回复信息

![image-20251230153424825](img/image-20251230153424825.png) 

点开之后就会跳转到回复的具体内容，类似这样的就算翻倍成功啦！

![image-20251230153502751](img/image-20251230153502751.png) 

### 04-确认是否翻倍？

登录RackNerd后台，点开【Services】，打开翻倍的服务器

翻倍前流量

![image-20251230153541633](img/image-20251230153541633.png) 

翻倍后流量

![image-20251230153607758](img/image-20251230153607758.png) 



## 搭建vpn

SSH工具连接服务器

- 名称：任意自定义
- 主机：服务器的ip地址
- 端口：基本都是22
- 用户名：root
- 密码：服务器的root密码

### 系统升级组件安装

```bash
apt update -y && apt install -y curl && apt install -y socat
```

### Hysteria2 一键安装脚本（开源安全）

```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/flame1ce/hysteria2-install/main/hysteria2-install-main/hy2/hysteria.sh && bash hysteria.sh
```

**输入“1”：安装 Hysteria 2**

```bash
#############################################################
#                  Hysteria 2 一键安装脚本                  #
#############################################################

 1. 安装 Hysteria 2
 2. 卸载 Hysteria 2
 ------------------------------------------------------------
 3. 关闭、开启、重启 Hysteria 2
 4. 修改 Hysteria 2 配置
 5. 显示 Hysteria 2 配置文件
 ------------------------------------------------------------
 0. 退出脚本

请输入选项 [0-5]: 1
```

![image-20251230170315126](img/image-20251230170315126.png) 

![image-20251230170337585](img/image-20251230170337585.png) 

### 配置Hysteria 2协议

⦁ 输入“1”：必应自签证书 （默认）
⦁ 回车：设置 Hysteria 2 端口为随机端口
⦁ 输入“1”：单端口 （默认）
⦁ 回车：设置 Hysteria 2 密码为随机密码
⦁ 设置Hysteria 2 的伪装网站地址：输入“www.bing.com”

```bash
aws.com
amd.com
bing.com
go.microsoft.com
snap.licdn.com
devblogs.microsoft.com
cdn.bizibly.com
www.apple.com
ts1.tc.mm.bing.net
fpinit.itunes.apple.com
catalog.gamepass.com
gray-config-prod.api.arc-cdn.net
apps.mzstatic.com
tag.demandbase.com
r.bing.com
tag-logger.demandbase.com
cdn-dynmedia-1.microsoft.com
services.digitaleast.mobi
gray.video-player.arcpublishing.com
azure.microsoft.com
beacon.gtv-pub.com
```

日志

```bash
Hysteria 2 安装成功！
Hysteria 2 协议证书申请方式如下：

 1. 必应自签证书 （默认）
 2. Acme 脚本自动申请
 3. 自定义证书路径

请输入选项 [1-3]: 1
将使用必应自签证书作为 Hysteria 2 的节点证书
设置 Hysteria 2 端口 [1-65535]（回车则随机分配端口）：
将在 Hysteria 2 节点使用的端口是：11075
Hysteria 2 端口使用模式如下：

 1. 单端口 （默认）
 2. 端口跳跃

请输入选项 [1-2]: 1
将继续使用单端口模式
设置 Hysteria 2 密码（回车跳过为随机字符）：
使用在 Hysteria 2 节点的密码为：db53d5f1
请输入 Hysteria 2 的伪装网站地址 （去除https://） [默认首尔大学]：www.bing.com
使用在 Hysteria 2 节点的伪装网站为：www.bing.com
```

![image-20251230170601908](img/image-20251230170601908.png) 

### 保存Hysteria 2协议节点链接

![image-20251230170704332](img/image-20251230170704332.png) 



## 客户端配置

- Windows（v2rayN）：https://github.com/2dust/v2rayN/releases （下载v2rayN-windows-64-SelfContained.zip版）
- Android（v2rayNG）：https://github.com/2dust/v2rayNG/releases
- Mac（v2rayN）：https://github.com/2dust/v2rayN/releases
- IOS（shadowrocket）：https://apps.apple.com/app/shadowrocket/id932747118

扫描二维码、或复制粘贴链接导入客户端



## 如何查看更改配置

还是输入安装代码，可以【修改配置】、【显示配置文件】等

```bash
wget -N --no-check-certificate https://raw.githubusercontent.com/flame1ce/hysteria2-install/main/hysteria2-install-main/hy2/hysteria.sh && bash hysteria.sh
```

![image-20251230170842114](img/image-20251230170842114.png) 

郑重声明：请合理使用科学上网，用于学习、科研、外贸等，严格遵守当地相关规定！