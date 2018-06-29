## 怎样定位直播模块登录超时的问题？

登录超时一般是网络问题，主要排查方向是设备的网络连接。设备能不能连接到公共网络。

1.  Ping 服务器看看是否域名能够正常解析，我们的测试服务器地址是 connect.peergine.com ,客户自己搭建服务器后就ping客户本身的服务器域名或者地址。
2.  如果能ping通后检测防火墙问题，看是否配置了一些防火墙规则限制了P2P流量。

如果还是不通。请提交问题到我们的讨论群，同时提交日志和描述状态信息，必要时提供远程服务。

1.  目前需要排除的是防火墙对P2P的影响，请在设备上使用telnet connect.peergine.com 443 看看是否有反应，请将局域网防火墙关闭试试能不能登录。如果还是不行换台设备试试，或者换个网络试试。
2.  在嵌入式系统中，某些shell在输入回车键后在字符串中输入‘\n’或者‘\r’,如果这个时候输入服务器地址的环节直接按回车会导致服务器地址是”\n” ,导致登录超时。