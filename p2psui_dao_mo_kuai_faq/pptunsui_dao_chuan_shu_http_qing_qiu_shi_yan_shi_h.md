## PPTUN隧道传输HTTP请求时延时很大的解决方案 {#pptun-http}

问题描述：

有客户创建了一条隧道用来请求HTTP数据，测试发现：局域网请求数据很快获得返回结果。但是在隧道中请求确需要10秒左右的时间。每次都是大约10才能请求完成。

解决方案：

通过抓包获取HTTP数据分析，发现他们的HTTP Response Header没有Content-Length

在HTTP Response Header中加入Content-Length后再请求同样的就可以很快获得回复了。