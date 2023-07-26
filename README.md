# 北京联通IPTV播放列表

本仓库是基于 [北京联通 IPTV 列表](https://raw.githubusercontent.com/dandeliono/bj-unicom-iptv-/master/bj-unicom-iptv-udpxy.m3u) 。我们通过使用 GitHub Actions，每天0点自动拉取最新的 IPTV 列表，并将其中的 rtp://ip:port 格式替换为更友好的 udpxy 地址。

## 如何使用

你可以直接使用以下链接来获取替换后的 IPTV 列表：

[https://raw.githubusercontent.com/dandeliono/bj-unicom-iptv/master/bj-unicom-iptv-udpxy.m3u](https://raw.githubusercontent.com/dandeliono/bj-unicom-iptv/master/bj-unicom-iptv-udpxy.m3u)

如果你需要修改 udpxy 的 IP 地址和端口，可以通过修改 GitHub Actions 来实现。在本仓库中的 `.github/workflows/replace_m3u.yml` 文件中，你可以找到 `sed` 命令替换 rtp 地址的部分。在此部分的命令中，你可以将 `http://192.168.31.1:4022` 替换为你希望的 udpxy 的 IP 地址和端口。

## 帮助和支持

如果你在使用过程中遇到任何问题或需要帮助，请随时在 Issues 中提出你的问题。我们会尽力回答你的疑问并提供支持。

欢迎感兴趣的开发者参与项目贡献，提供更多改进和功能增强。在你提交 Pull Request 之前，请确保你的修改是经过测试和审查的。



## 节目源来源:
[北京联通IPTV列表](https://gist.github.com/sdhzdmzzl/93cf74947770066743fff7c7f4fc5820)

Author: [sdhzdmzzl](https://github.com/sdhzdmzzl) 

## 节目源维护：
节目源失效，新增，变化，可提交[issue](https://github.com/wuwentao/bj-unicom-iptv/issues/new)反馈变化
或提交merge request,共同维护与更新准确的节目源列表

## 节目源统计：
***合计***：   165个
- 高清： 54个
- 4K:    2个
- 标清： 109个

## 主要修改
* 重排序所有节目频道，按***画质+分类***排列
* 节目源标题增加关键字来排序并区分节目源
* 标识***高清***为1080p
* 标识***4K***为4K
* 无标识则为***标清***
* 重命名部分频道名称以及错误频道名称
* 验证所有节目源并核对节目名称有效 @2020.03.04
* 增加台标 @2021.10.26
* 增加EPG电子节目单 @2021.10.26
* 二次分组分类，增加
  -  [高清]央视
  -  [高清]卫视
  -  [高清]北京
  -  [高清]北京IPTV
  -  *少儿*
  -  央视
  -  卫视
  -  北京
  -  北京IPTV

> - 部分小众频道可能在北京不同的区域会有所区别，例如:  ***朝阳，密云，房山***
> - MacOS 上使用***IINA***播放器，会有小部分节目源出现闪退，偶尔能播放，但使用***VLC/MPV***则播放正常

# 北京联通IPTV播放列表

https://github.com/wuwentao/bj-unicom-iptv

# 北京电信IPTV播放列表

https://github.com/wuwentao/bj-telecom-iptv

# 北京移动IPTV播放列表

https://github.com/wuwentao/bj-mobile-iptv


# 在路由器上使用udpxy组播转单播
直接下载[bj-unicom-iptv.m3u](bj-unicom-iptv.m3u)播放列表文件，本地打开文件，查找关键字 `rtp://`，并全部替换为: `http://192.168.2.1:8012/rtp/` 即可使用使用PC播放器播放或者导入电视盒子
>其中***192.168.2.1:8012***为局域网udpxy的IP和端口

# 局域网观看北京联通IPTV方法
详情请参考：
[IPTV中继原理](iptv.md)

或参考OpenGG方法：
[北京联通IPTV的完美方案](https://exp.newsmth.net/topic/357dabb5a4dc6d5c4c75f96a30209cd9/1)

# 参考列表

[OpenGG联通IPTV列表（已停止更新）](https://github.com/OpenGG/bj-unicom-iptv)

[sdhzdmzzl北京联通IPTV m3u列表(更新中)](https://gist.github.com/sdhzdmzzl/93cf74947770066743fff7c7f4fc5820)   

[EPG台标](http://epg.51zmt.top:8000/)

[iptvtools生成EPG台标m3u](https://github.com/huxuan/iptvtools)

[北京电信IPTV播放列表](http://m.newsmth.net/article/DigiHome/833031)

[Throwing Star LAN Tap](https://greatscottgadgets.com/throwingstar/)

[IPTV直播源抓包教程，DIY Throwing Star Lan Tap](https://www.znds.com/tv-1137126-1-1.html)

[5毛钱打造自己的Throwing Star LAN Tap](https://www.freebuf.com/articles/89552.html)

[Udp、Rtp协议头配图解析](https://blog.csdn.net/nihenbuhao/article/details/60585079)

[Huawei组播原理及IPTV组网介绍](https://wenku.baidu.com/view/6e40036d011ca300a6c39072.html)

[IGMP基础](https://cshihong.github.io/2018/02/12/IGMP%E5%9F%BA%E7%A1%80/)

[组播IP地址到底是谁的IP](https://www.zhihu.com/question/27233903)

