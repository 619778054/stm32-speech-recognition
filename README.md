# stm32-speech-recognition
基于STM32的孤立词语音识别

本设计研究孤立词语音识别系统及其在STM32嵌入式平台上的实现。识别流程是：预滤波、ADC、分帧、端点检测、预加重、加窗、特征提取、特征匹配。端点检测(VAD)采用短时幅度和短时过零率相结合。检测出有效语音后，根据人耳听觉感知特性,计算每帧语音的Mel频率倒谱系数(MFCC)。然后采用动态时间弯折(DTW)算法与特征模板相匹配,最终输出识别结果。先用Matlab对上述算法进行仿真，经多次试验得出算法中所需各系数的最优值。然后将算法移植到STM32嵌入式平台，移植过程中根据嵌入式平台存储空间相对较小、计算能力也相对较弱的实际情况，对算法进行优化。最终设计并制作出基于STM32的孤立词语音识别系统。

####实物图 欢迎界面
![Renderings](http://gk969.com/wp-content/uploads/2013/11/Speech-recognition-the-real-figure.jpg)

####模板训练界面
![Renderings](http://gk969.com/wp-content/uploads/2013/11/Template-training-UI.jpg)

####语音识别界面
![Renderings](http://gk969.com/wp-content/uploads/2013/11/Speech-recognition-UI.jpg)

####详细介绍：
http://gk969.com/stm32-speech-recognition/
