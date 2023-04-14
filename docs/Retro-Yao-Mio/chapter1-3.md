# Retro Yao-Mio 学习套件

Retro Yao-Mio 学习套件包括硬件和学习资料包两部分。

## 硬件清单

Retro Yao-Mio 学习套件硬件清单包括：

| 名称 | 规格 | 数量 | 说明 |
|:---| :--- | :--- | :--- |
| Retro-Yao-Mio底板 | 180mm*68mm | 1 |不包含扬声器、屏幕、电池、SD卡、DShanMCU-Mio开发板 |
| ShanMCU-Mio开发板 | 180mm*68mm | 1 | 已焊接排针，作为主控/核心板对接到Retro-Yao-Mio底板上 |
| IO拓展座子 | 2*15P,2.54毫米间距双排弯头母座，卧式通孔 | 1 | IO拓展接插件，需自行焊接在底板背面（自主拓展使用，不承诺能接入第三方模块使用，对于第三方模块或者实验只提供咨询参考建议） |
| 扬声器 | 8Ω1w, 1.25-2P母端公壳 | 2 | 扬声器 |
| 电池 | 聚合物锂电池 3.7v 1200mah, 1.25-2P母端公壳 | 1 | 供电 |
| LCD屏幕 | 84.10±0.2mm * 54.46±0.2mm | 1 | 3.5寸(320*480) SPI无触摸TFT LCD屏|
| LCD屏幕连接线 | 70mm | 1 | 掌机底板专用连接线 |
| LCD屏幕连接线 | 150mm | 1 | 通用连接线 | 
| 屏幕固定螺丝 | m2 * 5mm | 4 | 固定屏幕用 |
| Retro-Yao-Mio底板固定螺柱| M3单头六角塑料螺柱 | 4 | 不使用外壳时，起支撑作用 |
| Micro SD卡 | 32GB | 1 | 存储设备，需格式化为FAT32格式 |
| 天线 | IPEX天线 | 1 | 信号增益 |
| 按键帽 | 12 * 12mm、6 * 6mm 两种规格 | 14 | 共有三种类型的按键帽，提高按键使用体验与美观 |
| 数据线 | USB Tyep-C | 1 | 烧录或者充电使用 |
| 读卡器 | USB 2.0 | 1 | 读卡器 |


### 组装学习套件

这里有三种情况：

1. 购买的是一整套 Retro Yao-Mio 学习套件，那么不需要组装，开箱即用。
2. 已经有了 DShanMCU-Mio 开发板，但是没有 Retro Yao-Mio 底板，那么需要购买一整套包括配件的 Retro Yao-Mio 底板，有了底板之后只需要将 DShanMCU-Mio 插入到 Retro Yao-Mio 底板背面的排母即可。
3. 后续使用过程中由于各种原因导致某些配件损坏，需要更换，请按需选购并且参考原装状态进行更换。

## 学习资料包

Retro Yao-Mio 学习底板只是一个学习底板，其单独并不能实验，核心部分是 DShanMCU-Mio 开发板，因此在 Retro Yao-Mio 学习底板来看 DShanMCU-Mio 是其核心板。

后续的学习、开发其实就是在对 DShanMCU-Mio 进行操作，Retro Yao-Mio 学习底板是 DShanMCU-Mio 的外设。因此Retro Yao-Mio的资料在 DShanMCU-Mio 开发板的资料包的子目录中。

!> 注意：如果你是零基础，需要从头开始学习，请在阅读 DShanMCU-Mio 教程之后再继续阅读这之后的内容：[DShanMCU-Mio(澪) + ESP-IDF 开发教程文档](DShanMCU-Mio/ESP-IDF/chapter1-1)

获取 DShanMCU-Mio 开发板的资料包请阅读：[获取DShanMCU-Mio学习资料包](DShanMCU-Mio/ESP-IDF/chapter2-1)

