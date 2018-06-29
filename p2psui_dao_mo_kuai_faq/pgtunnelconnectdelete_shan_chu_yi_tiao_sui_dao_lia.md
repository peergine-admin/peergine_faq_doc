## pgTunnelConnectDelete: 删除一条隧道连接返回 -18 可能的原因 {#pgtunnelconnectdelete-18}

返回值PG_TUNNEL_ERROR_NOEXIST = -18, // 资源不存在

1）这个隧道确实不存在了

2）调用API传错了某个参数导致没法匹配到隧道。