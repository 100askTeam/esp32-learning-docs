# ESP32简介
## 什么是ESP32
ESP32是乐鑫信息科技（上海）股份有限公司(后文简称为乐鑫公司)研发，搭载了Wi-Fi和蓝牙的32位[系统单芯片](https://baike.baidu.com/item/%E7%B3%BB%E7%BB%9F%E5%8D%95%E8%8A%AF%E7%89%87/4497794) (System-on-a-chip，缩写SoC 或 SOC，其他译名有芯片系统、系统级芯片、片上系统)。ESP32的整体表现比较优秀[^1]：

- 性能稳定。工作温度范围达到 –40°C 到 +125°C。集成的自校准电路实现了动态电压调整，可以消除外部电路的缺陷并适应外部条件的变化。
- 高度集成。ESP32 将天线开关、RF balun、功率放大器、接收低噪声放大器、滤波器、电源管理模块等功能集于一体。ESP32 只需极少的外围器件，即可实现强大的处理性能、可靠的安全性能，和 Wi-Fi & 蓝牙功能。
- 超低功耗。ESP32 专为移动设备、可穿戴电子产品和物联网应用而设计，具有业内高水平的低功耗性能，包括精细分辨时钟门控、省电模式和动态电压调整等。
- Wi-Fi & 蓝牙解决方案。ESP32 可作为独立系统运行应用程序或是主机 MCU 的从设备，通过 SPI / SDIO 或 I2C / UART 接口提供 Wi-Fi 和蓝牙功能。


总的来说，ESP32是功能丰富的Wi-Fi & 蓝牙的通用MCU，适用于多样的物联网应用。

除此之外ESP32常常被某些开发板当作Wi-Fi和蓝牙的模组使用，称得上是多才多艺、物美价廉。

## ESP32模组

ESP32芯片有不同的型号，并且一直在推陈出新，以下是目前几种常见的型号：

- ESP32-D0WDQ6：最常见的型号，双核心。
- ESP32-C3：单核心 RISC-V 处理器，支持 Wi-Fi 4 和蓝牙5.0。
- ESP32-S3：双核心 LX7 处理器，支持 Wi-Fi 4 和蓝颜 5.0。

乐鑫公司有推出各种各样的 ESP32 模组，像下面这款 ESP32 WROOM-32 模组(后文简称 WROOM 模组)，是目前最常见的模组，常常被各种厂家在其基础上造出自己的开发板：

![DShanMCU-Mio_MicroPython_chapter1_images_001](_images/chapter1_images/DShanMCU-Mio_MicroPython_chapter1-1_images_001.jpg)

WROOM模组再加上直流电源管理芯片和UART转USB芯片，就能组成一个最基本的ESP32开发板。

![DShanMCU-Mio_MicroPython_chapter1_images_002](_images/chapter1_images/DShanMCU-Mio_MicroPython_chapter1-1_images_002.jpg)

也有的开发板不使用现成的模组，像我们在学习时使用的 DshanMCU-Mio(澪) 开发板，就是自行整合ESP32芯片和储存单元。我们将在下一节的文章了解 DshanMCU-Mio(澪) 开发板以及其开发套件。

[^1]:https://www.espressif.com.cn/zh-hans/products/socs/esp32
