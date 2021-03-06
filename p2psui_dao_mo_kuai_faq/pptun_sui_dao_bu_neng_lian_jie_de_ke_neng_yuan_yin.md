## PPTUN 隧道不能连接的可能原因和解决办法 {#pptun}

请查看**《Peergine P2P 隧道 v1.5.pdf》**理解隧道**出口端**和**入口端**的概念。

1.  隧道没有生效。重启所有客户端。
2.  客户端不在线。在网页上看设备是否在线。

1.  重启客户端并且在线，在**入口端**设备上查看配置的入口端**IP地址**和**端口**是否打开。
2.  验证在**出口端**设备上（创建隧道的设备）上是否可以正常访问配置的出口端**IP**地址和**端口**（一般是私网的TCP服务器地址和端口）。

1.  问题：部分隧道不可用。

解决办法：请配置更大的MaxSess 和MaxTunnel 后重启客户端。

问题原因：

同一个账号或者ID关联了大量隧道，超过了客户端配置文件中支持的最大隧道数，超过部分隧道将不能生效。

1.  部分入口端设备的隧道不可用，请检查是否有入口端设备上是否有端口冲突。