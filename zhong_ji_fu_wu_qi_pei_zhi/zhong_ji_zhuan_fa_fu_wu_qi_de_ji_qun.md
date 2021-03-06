## **中继转发服务器的集群**

## ***域名解析均衡机制***
 在客户端通过配置文件或者编程接口（API）配置独立的中继转发服务器的域名（与P2P服务器的域名分离），这样中继转发服务器可以与P2P服务器分开部署到不同的物理服务器主机上。
 
 当有多台中继转发服务器时，配置中继转发服务器的专用域名解析到多台中继转发服务器的IP地址上（一个域名可以解析多个IP地址）。当客户端请求域名解析时，域名服务器返回包含多个IP地址的列表，客户端从IP地址列表中随机选取一个IP地址使用，这样客户端就可以从多台中继转发服务器中，随机均衡选取一台使用。
 
 通过“域名解析均衡机制”就可以简单实现中继转发服务器的集群（没有部署集群服务器的时候使用）。


## ***集群系统分配机制***
 如果系统部署了集群服务器，那么还可以在“域名解析均衡机制”的基础上叠加通过集群分配中继转发服务器给客户端的机制。
   
 每当客户端登录到P2P服务器时，集群会从中继转发服务器列表中选择负荷富余的中继转发服务器下发到客户端使用。
 
 客户端优先使用通过“集群系统分配机制”下发的中继转发服务器。如果没有部署集群服务器或者集群没有下发中继转发服务器，则客户端使用通过“域名解析均衡机制”获取的中继转发服务器。

 客户端所要做的工作：在客户端通过配置文件或者编程接口（API）配置独立的中继转发服务器的域名（与P2P服务器的域名分离）