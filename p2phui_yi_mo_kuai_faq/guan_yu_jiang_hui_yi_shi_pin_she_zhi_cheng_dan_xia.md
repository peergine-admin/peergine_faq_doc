## 关于将会议视频设置成单向的方法

版本20之前。可以在VideoStart时设置参数，如果是希望视频是自从A发送到B，那么需要在A设置onlyInput，在B设置OnlyOutput。

在版本20之后，因为支持了同时打开两条视频，所以可以在初始化的sVideoParam中对两条视频流分别设置不同的参数值：sVideoParam 的中添加(VideoFlag){0}(LVideoFlag){0}

![](..\assets\cusersctkjdocumentstencent_fil.png)

版本20之前可以打开两条不同的视频流，但是同一时刻只能打开一条视频流。版本20之后可以同时打开两条不同的流，两条流使用不同的回调事件，不同的函数分别打开。

比如：  sVideoParam =&quot;(Code){3}(Mode){2}(FrmRate){66}(VideoFlag){0}&quot; +                &quot;(LCode){3}(LMode){3}(LFrmRate){66}(LVideoFlag){0}&quot;

在VideoStart 设置的只能设置主码流的参数，如果在VideoStart设置了非Normal的值，则VideoStart的Flag优先生效。 码流L的参数只能由LVideoFlag设置。

这两个参数默认是0