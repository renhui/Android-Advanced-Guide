## 作为一个Android程序员，精通音视频开发，寒冬再冷也冻不到你

**前言**

如今音视频的知识纷繁复杂，自己学习非常困难，既需要非常扎实的基础知识，又需要有很多的工程经验。

而音视频从业者基本上有两个层面：一个层面是搞音视频算法，这类人非常少，需要有深的数学能力和算法背景，这类人一般都会选择去大公司，薪水百万是最low 的。


另一个层面是搞工程，这类人相对较多，他们有扎实的理论基础，很强的技术功底，对音频、视频都非常熟悉。这些人工资要比一般开发者高20%左右；随着5G时代的到来，音视频慢慢变成人们日常生活中的必需品。所以，现在有大量的公司开始寻找音视频人才，一个稍好点的音视频人才现在可能会有3-4家公司抢着要。因此，对音视频人才的需求也从小众变成了大众，这更多的是大家对未来市场的预期导致的结果。

可在目前的确没有比较系统的教程或者书籍，网上的博客文章也都是比较零散的，在此小编花费大量时间收集和整理，终于将音视频方面的知识点整理成了一个专题，今天借此文章分享给对音视频感兴趣的小伙伴。

我们先来看看一个方向性的学习指南

> 1. 在 Android 平台绘制一张图片，使用至少 3 种不同的 API，ImageView，SurfaceView，自定义 View
> 2. 在 Android 平台使用 AudioRecord 和 AudioTrack API 完成音频 PCM 数据的采集和播放，并实现读写音频 wav 文件
> 3. 在 Android 平台使用 Camera API 进行视频的采集，分别使用 SurfaceView、TextureView 来预览 Camera 数据，取到 NV21 的数据回调
> 4. 学习 Android 平台的 MediaExtractor 和 MediaMuxer API，知道如何解析和封装 mp4 文件
> 5. 学习 Android 平台 OpenGL ES API，了解 OpenGL 开发的基本流程，使用 OpenGL 绘制一个三角形
> 6. 学习 Android 平台 OpenGL ES API，学习纹理绘制，能够使用 OpenGL 显示一张图片
> 7. 学习 MediaCodec API，完成音频 AAC 硬编、硬解
> 8. 学习 MediaCodec API，完成视频 H.264 的硬编、硬解
> 9. 串联整个音视频录制流程，完成音视频的采集、编码、封包成 mp4 输出
> 10. 串联整个音视频播放流程，完成 mp4 的解析、音视频的解码、播放和渲染
> 11. 进一步学习 OpenGL，了解如何实现视频的剪裁、旋转、水印、滤镜，并学习 OpenGL 高级特性，如：VBO，VAO，FBO 等等
> 12. 学习 Android 图形图像架构，能够使用 GLSurfaceviw 绘制 Camera 预览画面
> 13. 深入研究音视频相关的网络协议，如 rtmp，hls，以及封包格式，如：flv，mp4
> 14. 深入学习一些音视频领域的开源项目，如 webrtc，ffmpeg，ijkplayer，librtmp 等等
> 15. 将 ffmpeg 库移植到 Android 平台，结合上面积累的经验，编写一款简易的音视频播放器
> 16. 将 x264 库移植到 Android 平台，结合上面积累的经验，完成视频数据 H264 软编功能
> 17. 将 librtmp 库移植到 Android 平台，结合上面积累的经验，完成 Android RTMP 推流功能
> 18. 上面积累的经验，做一款短视频 APP，完成如：断点拍摄、添加水印、本地转码、视频剪辑、视频拼接、MV 特效等功能

相信我，如果你认真把所有任务都完成了，你一定会成为音视频人才招聘市场的香饽饽～～


如何才能更好地学好以上知识呢？



作为一名音视频行业的10年老兵，我有一些思考分享给大家，希望能对你有所帮助。

下面正是要给大家分享我花了86天整理的关于音视频开发入门到精通，已整理成PDF文档，**有需要完整版的可以加入我们音视频技术交流群** **933971311** **免费获取。**



# **一、初级入门篇**

**（一）绘制图片** 

1. ImageView 绘制图片

2. SurfaceView 绘制图片

3. 自定义 View 绘制图片

![20201214140853](https://github.com/renhui/Android-Advanced-Guide/blob/main/img/20201214140853.jpg)

**（二）AudioRecord API详解**

![20201214144727](\img\20201214144727.jpg)

**（三）使用 AudioRecord 实现录音，并生成wav**

- 创建一个AudioRecord对象
- 初始化一个buffer
- 开始录音
- 创建一个数据流，一边从AudioRecord中读取声音数据到初始化的buffer，一边将buffer中数据导入数据流。
- 关闭数据流
- 停止录音

![20201214144850](\img\20201214144850.jpg)

**（四）用 AudioTrack 播放PCM音频**

1. AudioTrack 基本使用

- MODE_STATIC模式
- MODE_STREAM模式

2. AudioTrack 详解

- 音频流的类型
- Buffer分配和Frame的概念
- AudioTrack构造过程

3. AudioTrack 与 MediaPlayer 的对比

- 区别
- 联系
- SoundPool

![20201214144950](\img\20201214144950.jpg)

**（五）使用 Camera API 采集视频数据**

1.预览 Camera 数据

2.取到 NV21 的数据回调



**（六）使用 MediaExtractor 和 MediaMuxer API 解析和封装 mp4 文件**

1.MediaExtractor API介绍

2.MediaMuxer API介绍

3.使用情境

![20201214145037](\img\20201214145037.jpg)

**（七）** **MediaCodec API 详解**

1.MediaCodec 介绍

2.MediaCodec API 说明

3.MediaCodec 流控

- 流控基本概念
- Android 硬编码流控
- Android 流控策略选择

![20201214145137](\img\20201214145137.jpg)

 由于文章篇幅受限，剩余内容过多，文中插图有限，下文只能截图目录展示 

# **二、中级进阶篇**

- Android OpenGL ES 开发（一）: OpenGL ES 介绍
- Android OpenGL ES 开发（二）: OpenGL ES 环境搭建
- Android OpenGL ES 开发（三）: OpenGL ES 定义形状
- Android OpenGL ES 开发（四）: OpenGL ES 绘制形状
- Android OpenGL ES 开发（五）: OpenGL ES 使用投影和相机视图
- Android OpenGL ES 开发（六）: OpenGL ES 添加运动效果
- Android OpenGL ES 开发（七）: OpenGL ES 响应触摸事件
- Android OpenGL ES 开发（八）: OpenGL ES 着色器语言GLSL
- Android OpenGL ES 开发（九）: OpenGL ES 纹理贴图
- Android OpenGL ES 开发（十）: 通过GLES20与着色器交互
- 使用 OpenGL 显示一张图片
- GLSurfaceviw 绘制 Camera 预览画面及实现拍照
- 使用OpenGL ES 完成视频的录制，并实现视频水印效果

![20201214145240](\img\20201214145240.jpg)

# **三、高级探究篇**

**

- 深入学习音视频编码，如H.264，AAC，研究使用开源编解码库，如x.264，JM 等

- 深入研究音视频相关的网络协议，如 rtmp，hls，以及封包格式，如：flv，mp4

- 深入学习一些音视频领域的开源项目，如 webrtc，ffmpeg，ijkplayer，librtmp 等等

- 将 ffmpeg 库移植到 Android 平台，结合上面积累的经验，编写一款简易的音视频播放器

- 将 x264 库移植到 Android 平台，结合上面积累的经验，完成视频数据 H264 软编功能

- 将 librtmp 库移植到 Android 平台，结合上面积累的经验，完成 Android RTMP 推流功能
  

**音视频编解码技术**

- 音视频编解码技术（一）：MPEG-4/H.264 AVC 编解码标准
- 音视频编解码技术（二）：AAC 音频编码技术



**流媒体协议**

- 流媒体协议（一）：HLS 协议
- 流媒体协议（二）：RTMP协议


**多媒体文件格式**

- 多媒体文件格式（一）：MP4 格式
- 多媒体文件格式（二）：FLV 格式
- 多媒体文件格式（三）：M3U8 格式
- 多媒体文件格式（四）：TS 格式
- 多媒体文件格式（五）：PCM / WAV 格式

![20201214145325](\img\20201214145325.jpg)

![20201214145334](\img\20201214145334.jpg)

# **FFmpeg 学习记录** 

- FFmpeg命令行工具学习(一)：查看媒体文件头信息工具ffprobe
- FFmpeg命令行工具学习(二)：播放媒体文件的工具ffplay
- FFmpeg命令行工具学习(三)：媒体文件转换工具ffmpeg
- FFmpeg命令行工具学习(四)：FFmpeg 采集设备
- FFmpeg命令行工具学习(五)：FFmpeg 调整音视频播放速度
- ![20201214145417](\img\20201214145417.jpg)

- FFmpeg 学习(一)：FFmpeg 简介
- FFmpeg 学习(二)：Mac下安装FFmpeg
- FFmpeg 学习(三)：将 FFmpeg 移植到 Android平台
- FFmpeg 学习(四)：FFmpeg API 介绍与通用 API 分析
- FFmpeg 学习(五)：FFmpeg 编解码 API 分析
- FFmpeg 学习(六)：FFmpeg 核心模块 libavformat 与 libavcodec 分析

![20201214145531](\img\20201214145531.jpg)


FFmpeg 结构体学习(一)：AVFormatContext 分析

FFmpeg 结构体学习(二)：AVStream 分析

FFmpeg 结构体学习(三)：AVPacket 分析

FFmpeg 结构体学习(四)：AVFrame 分析

FFmpeg 结构体学习(五)：AVCodec 分析

FFmpeg 结构体学习(六)：AVCodecContext 分析

FFmpeg 结构体学习(七)：AVIOContext 分析

FFmpeg 结构体学习(八)：FFMPEG中重要结构体之间的关系

![20201214145618](\img\20201214145618.jpg)

 **更多目录截图** 

![20201214145700](\img\20201214145700.jpg)

![20201214145651](\img\20201214145651.jpg)

![20201214145705](\img\20201214145705.jpg)

***\*最后\****

##### 如何做好音视频入门到精通，规划学习方向？

音视频开发学习手册可以帮助你查漏补缺，有方向有针对性的学习，为之后技能提升做准备。

说句实话，音视频自学起来困难重重，学习成本非常高，且效率低。主要有两方面的原因。

一方面是音视频知识庞杂，通俗易懂的资料非常少；

另一方面，网上充斥着大量的错误信息，使得很多初学者掉到坑里就爬不出来了。

但如果学到的知识不成体系，遇到问题时只是浅尝辄止，不再深入研究，那么很难做到真正的技术提升。建议先制定学习计划，根据学习计划把知识点关联起来，形成一个系统化的知识体系。

我搜集整理了这几年抖音，以及斗鱼，爱奇艺，等公司的音视频项目实战，把音视频开发的要求和技术点梳理成一份大而全的“ Android音视频”学习 Xmind（实际上比预期多花了不少精力），包含知识脉络 + 分支细节。

![20201214145811](\img\20201214145811.png)

**在搭建这些技术框架的时候，还整理了音视频开发进阶项目实战教程，会比自己碎片化学习效果强太多。**

![20201214145933](img\20201214145933.jpg)

***\*最后提醒：以上整理的音视频进阶学习PDF和音视频开发视频，均可以免费分享，有需要的朋友！\****

***\*扫码进群！联系管理员免费获取！加入我们的圈子领取资料，和我们一起学习交流吧！~\****

![20201214150013](img\20201214150013.png)

 **赶紧加入我们Android音视频进阶学习交流群：****933971311** **和我们一起学习交流吧！** 