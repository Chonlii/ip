# IP 工具箱

![GitHub Repo stars](https://img.shields.io/github/stars/jason5ng32/MyIP)
![GitHub](https://img.shields.io/github/license/jason5ng32/MyIP)
![GitHub contributors](https://img.shields.io/github/contributors/jason5ng32/MyIP)
![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/m/jason5ng32/MyIP)

在这里体验：[jason5ng32.github.io/MyIP](https://jason5ng32.github.io/MyIP/)

这是一个完全开源的 IP 信息查看器，可以查询本机 IP、查询任意 IP、查询国内外网站可用性等。这是我第一次用 Vue.js 练手的项目。如果你看着 `https://ip.skk.moe` 眼馋，那就用这个程序搭建一个属于自己的吧。

## 主要功能

1. 从 4 个来源显示本机的 IP，两个 IPv4 来源，两个 IPv6 来源
2. 显示所有 IP 的相关信息，包括国家、地区、ASN、地理位置等
3. 检测一些网站的可用性：Google, Github, Youtube, 网易, 百度
4. 检测 WebRTC 连接时使用的 IP
5. 可以通过小工具查询任意 IP 的信息
6. 根据可用性检测结果，返回目前是否可以访问全世界网络的提示

## 如何使用

开箱即用。直接下载所有代码，放到你本地或服务器上就行，没啥额外步骤。

## 高级用法

如果你在通过代理上网，可以考虑在你的代理配置里，增加下面的规则（请根据你使用的客户端进行修改），这样就可以实现同时查询真实 IP 和代理后的 IP：

```
# IP Testing
IP-CIDR,1.0.0.1/32,DIRECT,no-resolve
IP-CIDR6,2606:4700:4700::1111/128,DIRECT,no-resolve
DOMAIN-SUFFIX,ipify.org,Proxy
```

## 额外说明

这个程序的 90% 的代码不是我写的，是通过 ChatGPT 写的。大概来回 30 个回合，外加一些细微的手动修改，完成了全部代码。