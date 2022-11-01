# ESP-IDF简介

ESP-IDF(全称：Espressif IoT Development Framework) 是乐鑫官方推出的物联网开发框架，支持 Windows、Linux 和 macOS 操作系统，适用于 ESP32、ESP32-S、ESP32-C 和 ESP32-H 系列 SoC。它基于 C/C++ 语言提供了一个自给自足的 SDK，方便用户在这些平台上开发通用应用程序。ESP-IDF 目前已服务支持数以亿计的物联网设备，并已开发构建了多种物联网产品，例如照明、消费电子大小家电、支付终端、工控等各类物联网设备。[^1]

乐鑫公司官方对ESP-IDF的总结介绍：[^1]

- 免费开源：ESP-IDF 相关资源已在 GitHub 上免费开放。用户可在 Apache 2.0 许可下以源代码形式获取 ESP-IDF 的大多数组件，或通过兼容许可证获取第三方组件。
- 专业稳定：ESP-IDF 具有清晰、严格的发布流程和支持策略，确保用户选择使用稳定的发布版本，并可持续获得适用于其应用的重要修复程序。每个稳定的发布版本均经过严格的测试流程，以确保版本稳定，客户可快速实现量产。
- 功能丰富的软件组件：ESP-IDF 集成了大量的软件组件，包括 RTOS、外设驱动程序、网络栈、多种协议实现技术以及常见应用程序的使用助手。它提供了典型应用程序所需的大部分构建块，用户在开发应用时只需专注于业务逻辑即可。 ESP-IDF 不仅具有免费开源的开发工具，还支持 Eclipse 和 VSCode 等 IDE，确保其易于开发人员使用。
- 丰富的文档和示例资源：ESP-IDF 提供详尽的软件组件使用和设计文档，有助于开发人员充分理解 ESP-IDF 功能，并从中挑选最适合构建其应用程序的模块。ESP-IDF 包含 100 多个示例，详细说明了其组件及硬件外设的功能和用法。它们经过了严格的测试和维护，是用户开启应用开发的有效参考。

## ESP-IDF相关学习资料

在我们学习的过程中，使用我们 [资料包](https://forums.100ask.net/t/topic/1285#h-1) 中的资料已经足够你学习，如果你想深入学习可以根据这节的文档了解更多的内容。

DshanMCU-Mio(澪) 学习资料包下载地址：[https://forums.100ask.net/t/topic/1285#h-1]

### 100ASK交流社区

遇到问题时可以在我们的[交流社区](https://forums.100ask.net/c/esp/49) 提问，会有专业的老师或者热心的同学一起帮你解决问题！

除了提问之外也可以浏览大家分享的各种创意项目，当然你也可以在这里留下你的成果展示分享给大家！

- 百问网交流社区： [https://forums.100ask.net/c/esp/49](https://forums.100ask.net/c/esp/49)

### ESP-IDF官方项目仓库

ESP-IDF 的官方仓库地址是： [https://github.com/espressif/esp-idf](https://github.com/espressif/esp-idf)

#### ESP-IDF官方文档

在乐鑫公司的官方网站中提供了一个文档入口，我们可以在这里浏览关于esp-idf的官方文档资料，我们在开发或者学习的时候，对于某些方面或者函数用法不太清楚的时候，绝大多数时候你都可以在这里得到你想要的答案。

- ESP-IDF编程指南： [https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/index.html](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/index.html)

- ESP-IDF版本说明：[https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/versions.html](https://docs.espressif.com/projects/esp-idf/zh_CN/latest/esp32s3/versions.html)


[^1]:https://www.espressif.com.cn/zh-hans/products/sdks/esp-idf
