## 概念：用户名，ID，P2P隧道，出口端，入口端，域。 {#id-p2p}

**用户名**：

有时也叫ID，是服务器用来区别不同登录客户端的字符串字段。

**ID**：

有时也叫用户名，P2P隧道客户端用来登录到P2P隧道服务器的字符串字段。

**P2P隧道**：

我们把端口到端口的P2P通道叫做隧道，具体概念请参看《Peergine P2P 隧道 v1.5.pdf》。

**出口端**：

隧道会有出口，我们把P2P隧道流量的出口设备称为P2P隧道出口端。一般是可以直接连到TCP服务器的那一端。具体概念请参看《Peergine P2P 隧道 v1.5.pdf》。

**入口端**：

隧道会有入口，我们把P2P隧道流量的入口设备称为P2P隧道入口端。一般是和TCP服务器不在同一个私网或者不能直接连到TCP服务器的设备。具体概念请参看《Peergine P2P 隧道 v1.5.pdf》。

**域**：

只有在同一个域中的用户之间才能建立隧道。只有部分域具有管理员权限。