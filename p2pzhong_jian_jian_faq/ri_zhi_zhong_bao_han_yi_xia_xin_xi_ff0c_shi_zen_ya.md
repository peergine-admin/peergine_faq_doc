## 日志中包含以下信息，是怎么回事？

30338984: CPGClassLive: HelperSendCmd, uPrivID=0, Cmd=0, uPartMask=0x0, uLoadFree=0, uPeer=219816

30338984: CPGClassLive: HelperSendInitForce send failed, uPeer=219816

30338984: CPGClassLive: HelperSendInitForce end

30339984: CPGClassLive: HelperSendCmd, uPrivID=0, Cmd=0, uPartMask=0x0, uLoadFree=0, uPeer=219816

30339984: CPGClassLive: HelperSendInitForce send failed, uPeer=219816

30339984: CPGClassLive: HelperSendInitForce end

是表示对象没有同步，一般是SDK中VideoStart失败等情况。