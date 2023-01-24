在上一章节中，我们了解了什么是ESP32、什么是Arduino。我们已经对这两个方面有了一定的了解，万事俱备，只欠东风。在正式开始学习或者说编程之前，我们还需要将我们的开发环境搭建起来。

搭建开发环境我们离不开两个东西： 硬件平台+软件平台。

下面我们就来动手将我们的 DshanMCU-Mio(澪) + Arduino IDE 开发环境搭建起来。这其中我们提供了多种系统平台的搭建方法，你只需要选择你常用的一种平台即可，比如你的PC使用的是Windwos系统，那么只需要看 Windows 平台的部分即可。

在搭建环境之前，我们需要先获取到学习资料包，下面我们先来看看 DshanMCU-Mio(澪) 的学习资料。

# 获取学习资料

[DShanMCU-Mio(澪)](https://forums.100ask.net/t/topic/1033)学习资料 [百度云盘](http://wiki.100ask.org/BeginnerLearningRoute#.E7.99.BE.E5.BA.A6.E7.BD.91.E7.9B.98.E4.BD.BF.E7.94.A8.E6.95.99.E7.A8.8B) 或 [阿里云盘](https://www.aliyundrive.com) 下载

| 下学习平台 | 下载链接 | 提取码 |
| :--- | :--- | --- |
| Arduino | 百度云盘：[https://pan.baidu.com/s/1rpC0JZj6wZ2wea3NyPXTvQ?pwd=root](https://pan.baidu.com/s/1rpC0JZj6wZ2wea3NyPXTvQ?pwd=root)<br> 阿里云盘：[https://www.aliyundrive.com/s/rUaAUeA8H1m](https://www.aliyundrive.com/s/rUaAUeA8H1m) | 百度云盘：root <br> 阿里云盘：k61h |
| ESP-IDF| 百度云盘：[https://pan.baidu.com/s/1lNVxmixhmOdPFSmtCMUMbg?pwd=root ](https://pan.baidu.com/s/1lNVxmixhmOdPFSmtCMUMbg?pwd=root) <br> 阿里云盘：[https://www.aliyundrive.com/s/V1SsoMJWzk6](https://www.aliyundrive.com/s/V1SsoMJWzk6) | 百度云盘：root <br> 阿里云盘：bt63 |
| Micropython | TODO | TODO |

> 获取最新的学习资料包，可以在上面的云盘下载来链接中获取，也可以关注我们的git仓库获取，同时非常欢迎提交你的 issues 或 Pull requests ！

示例、组件、库源码地址：

| 仓库名称 | 源码地址 | 说明 |
| :--- | :--- | --- |
| esp-arduino-learn  | [https://github.com/100askTeam/esp-arduino-learn](https://github.com/100askTeam/esp-arduino-learn) | Arduino 平台学习资料包 |
| esp-idf-learn | [https://github.com/100askTeam/esp-idf-learn](https://github.com/100askTeam/esp-idf-learn) | ESP-IDF 平台学习资料包 |
| esp-idf-components | [https://github.com/100askTeam/esp-idf-components](https://github.com/100askTeam/esp-idf-components) | ESP-IDF 平台的学习资料包的组件作为[esp-idf-learn](https://github.com/100askTeam/esp-idf-learn) 的子模块，也可以单独在自己的项目中使用！ |
| esp-micropython-learn | TODO | MicroPython 平台学习资料包 |


> 注意：在云盘下载的压缩包是一个git仓库，建议新建一个分支，或者拷贝一份用以备份，也就是一个用来同步最新的资料，一个用来学习使用。关于git的使用教程，请参阅：1. 文档教程[http://download.100ask.org/tools/Software/git/how_to_use_git.html](http://download.100ask.org/tools/Software/git/how_to_use_git.html)。 2.视频教程：[https://www.bilibili.com/video/BV1CL4y1A7YG](https://www.bilibili.com/video/BV1CL4y1A7YG)