# VanillaGlobalChannel - 香草跨服频道

![开源协议](https://img.shields.io/github/license/Vanilla-Non-Benefit-Community/VanillaGlobalChannel?style=for-the-badge)
![Stars](https://img.shields.io/github/stars/Vanilla-Non-Benefit-Community/VanillaGlobalChannel?style=for-the-badge)
![Last Commit](https://img.shields.io/github/last-commit/Vanilla-Non-Benefit-Community/VanillaGlobalChannel?style=for-the-badge)
[![Star History Chart](https://api.star-history.com/svg?repos=Vanilla-Non-Benefit-Community/VanillaGlobalChannel&type=Date)](https://star-history.com/#Vanilla-Non-Benefit-Community/VanillaGlobalChannel&Date)

## 写在前面

关于这个异地跨服聊天系统，有什么建议或者Bug的话，最好是发issues里面哦

如果不想发issue，嫌麻烦可以直接加我QQ 3401286177 私聊反馈给我也可以，看到就会回复

停更了很长一段时间，最近回来打算再重构一下然后更新一些内容

## 开发理念

国内Minecraft服务器有成千上万个，但是服务器与服务器之间似乎并没有多少联系。大多数的服务器都是在独自埋头苦干，没有与其他服务器建立密切的合作关系。并且，即使希望与其他服务器合作，也要承担相应的风险。

> 1-5-1: 每个MCBBS的会员只允许有一个服务器宣传帖，每个服务器、群组服、联合团队只允许有一个宣传帖，
> 同一账号或同一服务器、群组服、联合团队发布超过一个主题帖时，超额的帖子将直接删帖发卡警告并判为违规多帖宣传。

那什么是联合团队呢？大家心知肚明，不必多言。
https://www.mcbbs.net/thread-1234992-1-1.html

许多人也认为这样的规则并不合理，并且不合理的规则也不只是1-5-1。
大家都憋了很久了，那就起身反抗吧？
可是小服有反抗的能力吗？没有，不吃MCBBS的宣传，死路一条。
如果你会做视频，或者是先前积累了足够的玩家基数，那倒可以放手一搏，无所谓。
不过这样的服务器往往不会参与抗争，因为他们从抗争中并不能获得什么，已经足够安稳了，为什么要给自己找麻烦？

所以，不能是所有人都这么远远的看着吧，总得有人站出来带个头。
那我来负责把贵坛的水搅浑好了，既然版规1-5-1说的**这么明确**了，
就让我来抹掉它的界限。

我希望开发一系列插件，帮助服务器与服务器之间建立合作，
也帮助大家解决服务器宣传的问题，打破垄断。

**祝 早日摆脱泥潭，以上。**

## 功能简介

香草跨服聊天频道，是一个真正意义上的**MC跨服聊天**系统，
传统的跨服聊天插件基于**Bungeecord/Velocity**等群组核心本身进行消息广播，
然而，这个插件则是基于**Springboot**搭建的中央消息广播服务器实现其跨服聊天的功能。
因此，服务器与服务器之间即使不处于同一个群组环境下，或者不处于同一个网络环境中，
仍然能够实现跨服聊天！
一定要找个什么东西来比喻一下的话，这就像是MC内置的简易聊天室吧，就像早期的QQ那样。
目前支持的服务端：
Bungeecord/Bukkit/Velocity/Nukkit
所有基于Bukkit/Nukkit的服务端理论上都能够正常使用！例如Loliserver，Purpur，Mohist，Spigot, NukkitX, PNX…

## 使用效果

![image](https://user-images.githubusercontent.com/77883323/173993829-7ef82ba4-ab3c-4b8a-9205-df129dedd2da.png)

## 部署方式

(提示：Bungeecord服务端需要在服务端启动脚本里面添加 -Dfile.encoding=UTF-8 启动参数，否则中文会乱码哦)

**不同服务端插件生成的配置文件夹名字不同**
Bukkit服务端：BukkitVGC
Nukkit服务端：NukkitVGC
Bungeecord服务端：Bungeecord-VanillaGlobalChannel
Velocity服务端：velocityglobalchannel
**但是配置文件内容一致！**

### 接入大型公开聊天服务器(普通服主推荐方案！)

目前存在的大型公开聊天服务器如下：

MikkoAyaka搭建的频道：43.248.79.66:30004 (氛围温馨，正版公益服居多，素质高，聊天人数较少)刀鸽搭建的频道：r9-1.s.imc.re:34021 (多为Nukkit服，需要接入请联系QQ: 3523206925)XXXXX搭建的频道：xx.xx.xx.xx:xxxxx (这里是简要介绍频道特点)

1. 下载VanillaGlobalChannel-Plugin插件，根据自己服务端类型下载对应的插件。
2. 将插件安装到你的服务端，重启服务端一次，然后关闭，会生成相应的插件配置文件。
3. 联系中央服务器供应方，获取你的服务器ID，账号，密码并在配置文件中填写，修改中央服务器IP，按需要修改一下其他配置，然后保存。
4. 再次启动群组，不出意外的话，至此应该成功连接上你自己的中央服务器了。

### 搭建自己专属的聊天服务器(推荐中大型服务器团队采用该方案！)

1. 下载VanillaGloalChannel-Springboot整合包，放到你的服务器(主机/vps)上。
2. 配置好整合包文件夹内的application.yml，确保对应的端口开放了TCP协议！
3. 右键 启动.bat 用记事本打开，修改java路径，需要使用java17及以上。
4. 双击启动，至此，你专属的中央聊天转发服务器已经部署完毕
5. 下载VanillaGlobalChannel-Plugin插件，根据自己服务端类型下载对应的插件。
6. 将插件安装到你的服务端，重启服务端一次，然后关闭，会生成相应的插件配置文件。
7. 填写好你自己的服务器ID，账号，密码，修改中央服务器IP，按需要修改一下其他配置，然后保存。
8. 再次启动群组，不出意外的话，至此应该成功连接上你自己的中央服务器了。

## 如何下载

在Github-Release栏目里找到最新版本，按需下载即可~

## 关于源码

**开源协议** GNU Affero General Public License v3.0
[https://choosealicense.com/licenses/agpl-3.0/#]

都看到最后了，那就麻烦你给我点个Star呗，孩子第一次写这种稍微正经点的东西，
给个鼓励嘛 一颗星星换一次更新怎么样，很划算吧！
