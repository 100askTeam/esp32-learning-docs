# 第一章 ESP-IDF和ESP32-S3简介

## ESP32简介
### 什么是ESP32

ESP32是乐鑫信息科技（上海）股份有限公司(后文简称为乐鑫公司)研发，搭载了Wi-Fi和蓝牙的32位[系统单芯片](https://baike.baidu.com/item/%E7%B3%BB%E7%BB%9F%E5%8D%95%E8%8A%AF%E7%89%87/4497794) (System-on-a-chip，缩写SoC 或 SOC，其他译名有芯片系统、系统级芯片、片上系统)。ESP32的整体表现比较优秀[^1]：

- 性能稳定。工作温度范围达到 –40°C 到 +125°C。集成的自校准电路实现了动态电压调整，可以消除外部电路的缺陷并适应外部条件的变化。
- 高度集成。ESP32 将天线开关、RF balun、功率放大器、接收低噪声放大器、滤波器、电源管理模块等功能集于一体。ESP32 只需极少的外围器件，即可实现强大的处理性能、可靠的安全性能，和 Wi-Fi & 蓝牙功能。
- 超低功耗。ESP32 专为移动设备、可穿戴电子产品和物联网应用而设计，具有业内高水平的低功耗性能，包括精细分辨时钟门控、省电模式和动态电压调整等。
- Wi-Fi & 蓝牙解决方案。ESP32 可作为独立系统运行应用程序或是主机 MCU 的从设备，通过 SPI / SDIO 或 I2C / UART 接口提供 Wi-Fi 和蓝牙功能。


总的来说，ESP32是功能丰富的Wi-Fi & 蓝牙的通用MCU，适用于多样的物联网应用。

除此之外ESP32常常被某些开发板当作Wi-Fi和蓝牙的模组使用，称得上是多才多艺、物美价廉。

### ESP32模组

ESP32芯片有不同的型号，并且一直在推陈出新，以下是目前几种常见的型号：

- ESP32-D0WDQ6：最常见的型号，双核心。
- ESP32-C3：单核心 RISC-V 处理器，支持 Wi-Fi 4 和蓝牙5.0。
- ESP32-S3：双核心 LX7 处理器，支持 Wi-Fi 4 和蓝颜 5.0。

乐鑫公司有推出各种各样的 ESP32 模组，像下面这款 ESP32 WROOM-32 模组(后文简称 WROOM 模组)，是目前最常见的模组，常常被各种厂家在其基础上造出自己的开发板：

![DshanMCU-Mio_esp-idf_chapter1_images_001](_images/chapter1_images/DshanMCU-Mio_esp-idf_chapter1_images_001.jpg)

WROOM模组再加上直流电源管理芯片和UART转USB芯片，就能组成一个最基本的ESP32开发板。

![DshanMCU-Mio_esp-idf_chapter1_images_002](_images/chapter1_images/DshanMCU-Mio_esp-idf_chapter1_images_002.jpg)

也有的开发板不使用现成的模组，像我们在学习时使用的 DshanMCU-Mio(澪) 开发板，就是自行整合ESP32芯片和储存单元。我们将在下一节的文章了解 DshanMCU-Mio(澪) 开发板以及其开发套件。


## ESP32-S3开发平台

为了让广大电子爱好者更好更方便地学习 EPS32 开发，百问网 DShan MCU 团队打造了一系列高性价比地学习套件和周边模块。当前已经支持了 STM32 平台，灵动微平台(MM32)。我们的开发平台采用最小版+底板的设计形式，保留了官方原汁原味的兼容性的同时可以让学习、开发者能够更好地动手操作硬件、进行更多地拓展性实验；甚至融合到自己的项目中，拿去参加比赛等用途。

百问网 DShan MCU 系列提供了丰富的历程、文档和教程，基于我们的平台能确保所有的代码程序开箱即用，甚至可以将我们文档中的示例和实验应用在自己的产品研发、项目开发或者比赛中。

百问网 DShan MCU 系列资源、资料会保持活跃更新状态，如果你在学习时遇到任何相关的问题可以在我们的 [交流社区](https://forums.100ask.net/) 提问，会有专业的老师或者热心的同学一起帮你解决问题！

### DshanMCU-Mio(澪)开发板

DshanMCU-Mio(澪)开发板由百问网 DShan MCU 团队设计研发，有以下主要特点：

- 有文档教程在：Arduino 开发环境中学习、开发
- 有文档教程在：ESP-IDF 开发环境中学习、开发
- 有文档教程在：Micropython 开发环境中学习、开发
- 存储资源拉满：高达支持8MB的RAM和128MB的FLASH
- 自动下载电路
- USB OTG接口
- 全IO引出
- 按键和LED排列整齐，丝印清晰查看方便
- 可用来学习AI
- 支持百问网墨水屏和彩屏


![DshanMCU-Mio(澪)](https://forums.100ask.net/uploads/default/original/2X/a/ab36f2c93141cfbf2620d3fea4ef5978bf37ba9f.jpeg)


【图】 DshanMCU-Mio(澪)引脚图


#### DshanMCU-Mio(澪)功能参数表
| 功能 | 描述 |
| ----------- | ----------- |
| 主控        |  ESP32-S3     |
| 内存        |  512KBytes + 2M-8MBytes PSARM(选配)     |
| FLASH       |  8M-128MBytes (选配)   |
| KEY         |  连接到引脚0     |
| I2C         |  支持任意IO    |
| UART        |  支持任意IO     |
| PWM         |  支持任意IO     |
| 双USB       |  1. USAR: 板载 USB转TTL <br> 2.USB：USB OTG     |
| 5V          |  USB供电输入、对外供电输出     |
| 3.3V        |  3.3V输出，最大电流 600mA     |
| 墨水屏      |  支持局刷、快刷，提供LVGL开发教程、示例    |
| SPI彩屏     |  SPI接口，提供LVGL开发教程、示例     |

### DshanMCU-Mio(澪)开发套件

【图】 DshanMCU-Mio(澪)引脚图（墨水屏）

| 配置 | 描述 |
| ----------- | ----------- |
| 核心板        |  DshanMCU-Mio(澪)     |
| 底板        |  100ASK_ESP32-S3_Base-Board    |
| 显示屏        |  3.52寸SPI接口黑白两色墨水屏  |

【图】 DshanMCU-Mio(澪)引脚图（SPI彩屏）

| 配置 | 描述 |
| ----------- | ----------- |
| 核心板        |  DshanMCU-Mio(澪)     |
| 底板        |  100ASK_ESP32-S3_Base-Board    |
| 显示屏        |  3.5寸SPI接口TFT彩屏  |


### 100ASK_ESP32-S3_Base-Board

100ASK_ESP32-S3_Base-Board 是百问网 DShan MCU 团队针对 DshanMCU-Mio(澪) 在多开发平台上学习开发而量身定制的底板。可以用于在 Arduino、ESP-IDF、Micropython平台上进行学习、开发，通过100ASK_ESP32-S3_Base-Board能让我们能学习更多的内容做更多地实验；同时强大的拓展性，能让使用者能做更多的DIY。下面是100ASK_ESP32-S3_Base-Board的功能说明：

【图】 100ASK_ESP32-S3_Base-Board功能说明


| 接口 | 描述 |
| ----------- | ----------- |
| 2.54mm排针 引出   |  ESP32-S3     |
| 墨水屏接口        |  ESP32-S3     |
| TFT屏接口         |  ESP32-S3     |
| TFT屏触摸接口      |  ESP32-S3     |


### 配套模块

### 拓展配件

3.52寸SPI接口无触摸黑白两色支持快刷局刷墨水屏

3.5寸SPI接口电阻触摸彩屏


## ESP-IDF简介

ESP-IDF(全称：Espressif IoT Development Framework) 是乐鑫官方推出的物联网开发框架，支持 Windows、Linux 和 macOS 操作系统，适用于 ESP32、ESP32-S、ESP32-C 和 ESP32-H 系列 SoC。它基于 C/C++ 语言提供了一个自给自足的 SDK，方便用户在这些平台上开发通用应用程序。ESP-IDF 目前已服务支持数以亿计的物联网设备，并已开发构建了多种物联网产品，例如照明、消费电子大小家电、支付终端、工控等各类物联网设备。[^2]

乐鑫公司官方对ESP-IDF的总结介绍：[^2]

- 免费开源：ESP-IDF 相关资源已在 GitHub 上免费开放。用户可在 Apache 2.0 许可下以源代码形式获取 ESP-IDF 的大多数组件，或通过兼容许可证获取第三方组件。
- 专业稳定：ESP-IDF 具有清晰、严格的发布流程和支持策略，确保用户选择使用稳定的发布版本，并可持续获得适用于其应用的重要修复程序。每个稳定的发布版本均经过严格的测试流程，以确保版本稳定，客户可快速实现量产。
- 功能丰富的软件组件：ESP-IDF 集成了大量的软件组件，包括 RTOS、外设驱动程序、网络栈、多种协议实现技术以及常见应用程序的使用助手。它提供了典型应用程序所需的大部分构建块，用户在开发应用时只需专注于业务逻辑即可。 ESP-IDF 不仅具有免费开源的开发工具，还支持 Eclipse 和 VSCode 等 IDE，确保其易于开发人员使用。
- 丰富的文档和示例资源：ESP-IDF 提供详尽的软件组件使用和设计文档，有助于开发人员充分理解 ESP-IDF 功能，并从中挑选最适合构建其应用程序的模块。ESP-IDF 包含 100 多个示例，详细说明了其组件及硬件外设的功能和用法。它们经过了严格的测试和维护，是用户开启应用开发的有效参考。


### ESP-IDF相关学习资料

在我们学习的过程中，使用我们资料包中的资料已经足够你学习，如果你想深入学习可以根据这节的文档了解更多的内容。

#### 100ASK交流社区

遇到问题时可以在我们的[交流社区](https://forums.100ask.net/c/esp/49) 提问，会有专业的老师或者热心的同学一起帮你解决问题！

除了提问之外也可以浏览大家分享的各种创意项目，当然你也可以在这里留下你的成果展示分享给大家！

- 百问网交流社区： [https://forums.100ask.net/c/esp/49](https://forums.100ask.net/c/esp/49)

#### ESP-IDF官方项目仓库

ESP-IDF 的官方仓库地址是： [https://github.com/espressif/esp-idf](https://github.com/espressif/esp-idf)

#### ESP-IDF官方文档

在乐鑫公司的官方网站中提供了一个文档入口，我们可以在这里浏览关于esp-idf的官方文档资料，我们在开发或者学习的时候，对于某些方面或者函数用法不太清楚的时候，绝大多数时候你都可以在这里得到你想要的答案。

- ESP-IDF编程指南： [https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/index.html](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/index.html)

- ESP-IDF版本说明：[https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/versions.html](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/versions.html)




[^1]:https://www.espressif.com.cn/zh-hans/products/socs/esp32
[^2]:https://www.espressif.com.cn/zh-hans/products/sdks/esp-idf
