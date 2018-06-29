## 直播模块播放端不能打开采集端视频的原因

问题描述：

有客户将直播模块集成到APP中测试发现：APP第一次打开可以看到采集端视频，但是切换到后台后（不杀死APP进程）重新进入APP，发现采集端视频不能打开了。

具体情况：

直播模块播放端对象Clean后然后置空销毁。然后程序退到后台，之后切换到前台重新New 和初始化。发现调用VideoStart后接收不到采集端的视频了，调用VideoStart后如截图所示。

但是杀掉采集端APP这个进程重新进入就可以看到采集端视频。

解决方法：检查用来显示采集端视频的SurfaceView是否正常销毁了。注意直播模块的SurfaceView要使用pgLibLiveMultiView.Get 获取，以及使用pgLibLiveMultiView .Release销毁。

特别注意，ExtVideo模块使用的是pgLibView.Get 获取pgLibView .Release销毁。千万不要混淆。