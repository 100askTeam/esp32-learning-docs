# Retro Yao-Mio 的注意事项

Retro-Yao-Mio是一个学习套件，我们(深圳百问网科技有限公司)对其所提供的一切软硬件资源仅限于用于学习交流用途，请勿用作其他用途。如果你将其用于其他用途而造成的任何问题与损失，后果自负、责任自负，我们(深圳百问网科技有限公司)不承担任何后果与法律责任。

## 使用注意事项

- Retro Yao-Mio 相关的文档、视频教程都是免费公开的，如果你在学习过程中遇到问题请前往[百问网技术交流社区](https://forums.100ask.net/c/esp/49)发贴留言求助，超出Retro Yao-Mio硬件范围以及教程范围的问题我们不承诺都能百分百都能解给出答案或建议。
- Retro Yao-Mio 底板目前只支持插入 DShanMCU-Mio 开发板，请勿使用其他开发板，否则由此造成的后果自负。
- 只有 Retro Yao-Mio 底板上的 Type-C 接口能给接在 Retro Yao-Mio 底板上电池充电，DShanMCU-Mio上的 Type-C 接口不能为电池充电。
- 请不要边充电边使用。
- 在给电池充电时，DShanMCU-Mio(核心板)上的 Type-C 接口需要断开。也就是 Retro Yao-Mio 底板上和DShanMCU-Mio 上的 Type-C 接口不能同时接上并通电。
- Retro Yao-Mio 整机不防水、防摔，即使有外壳也不防水、防摔，请注意防水、防潮、防摔。
- 在给 Retro Yao-Mio 充电时，其正面右下角的背面有微微发烫，属于正常现象。
- 当WiFi或蓝牙的信号非常弱时，请检查 DShanMCU-Mio 是否已经接上天线。
- 请使用Retro-Yao-Mio学习套件配套的电池，否则由此造成的后果与损失自负。
- 请勿自行对 Retro Yao-Mio 开发套件的硬件进行改造，否则由此造成的后果与损失自负。
- 教程部分目前都是围绕ESP-IDF开展，主要是在ESP-IDF框架上结合 Retro Yao-Mio 的硬件资源进行开发、学习，暂无计划包括其他框架。
- 教程部分不包括游戏模拟器部分的讲解。如果之后有支持会另外声明。
- Retro Yao-Mio 底板预留的IO拓展接口，已经将 DShanMCU-Mio 开发板多余的IO引脚全部引出，需要使用的同学请自行焊接，后续在使用拓展接口时遇到的拓展开发问题(比如接第三方模块进行开发)，不在我们的服务范围内，但是你仍可以 [百问网技术交流社区](https://forums.100ask.net/c/esp/49) 中发贴求助，我们不承诺能百分百能解给出答案或建议。
- 你购买的Retro Yao-Mio并不包含外壳部分的附加服务，我们是秉着开源、自愿取用的原则而分享出来，仅供学习参考交流，我们不保证外壳模型的可靠性及安全性，因此如果你使用此外壳模型而造成的任何问题与损失，后果自负、责任自负。
- ROMs是游戏模拟器使用的游戏文件，没有他们游戏模拟器就无法发挥作用。我们提供的ROMs可以在 [sd卡资料包](https://forums.100ask.net/t/topic/2991#sd-3) 获取，**仅供学习交流使用**(如有冒犯请联系我们马上对其进行删除)。如果你需要更多的ROMs请自行解决，我们不对更多的ROMs进行收集分享，敬请谅解。
- 淘宝和群聊不提供实时以及一对一答疑服务，如果有问题请前往[百问网技术交流社区](https://forums.100ask.net/c/esp/49)发贴留言求助，超出Retro Yao-Mio硬件范围以及教程范围的问题我们不承诺都能百分百都能解给出答案或建议。
- 百问网技术交流社区地址： [https://forums.100ask.net/c/esp/49](https://forums.100ask.net/c/esp/49)

!> 淘宝和群聊不提供实时以及一对一答疑服务，在学习我们百问网提供的学习资料或者和视频的过程中，如果遇到问题请前往 [百问网技术交流社区](https://forums.100ask.net/c/esp/49) 发贴留言求助，超出Retro Yao-Mio硬件范围以及教程范围的问题我们不承诺都能百分百能解给出答案或建议。


## 软件开源协议

Retro Yao-Mio 中运行的是 [retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio)， 其基于开源项目 [retro-go](https://github.com/ducalex/retro-go) 进行二次开发定制而来。

[retro-go](https://github.com/ducalex/retro-go) 的开源协议为 [GPL-2.0 license](https://github.com/ducalex/retro-go/blob/master/COPYING)，并且 Retro Yao-Mio 已经获得 [retro-go作者的书面许可](https://github.com/ducalex/retro-go/issues/70)，同时 [retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio) 也严格遵守 [GPL-2.0 license](https://github.com/100askTeam/retro-go-yao-mio/blob/master/COPYING)。

- retro-go开源仓库地址：[https://github.com/ducalex/retro-go](https://github.com/ducalex/retro-go)
- 百问网 retro-go-yao-mio 开源仓库地址：[https://github.com/100askTeam/retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio)


## 软件更新

Retro Yao-Mio 支持 [retro-go](https://github.com/ducalex/retro-go) 和 [retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio)。但是如果你使用 [retro-go](https://github.com/ducalex/retro-go) 请确保你有一定的适配或者移植能力，因为目前还没有将 [retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio) 的移植合并到 [retro-go](https://github.com/ducalex/retro-go) 。因此如果你使用 [retro-go](https://github.com/ducalex/retro-go) 出现自己解决不了的问题时，请使用我们百问网是配好的 [retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio)。

在后续我们会将 retro-go-yao-mio 的配置以及新的功能尝试合入到 retro-go，但是对于我们 Retro Yao-Mio 套件，我们会优先保证 [retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio) 保持最新的状态，也就是如果你需要使用我们定制推出的最新的功能请使用 [retro-go-yao-mio](https://github.com/100askTeam/retro-go-yao-mio) 而不是 retro-go。

Retro Yao-Mio 的固件可以通过OTA在线升级(该功能未完成)，如果你想离线升级，请在这里获取最新的发布版：[https://github.com/100askTeam/retro-go-yao-mio/releases](https://github.com/100askTeam/retro-go-yao-mio/releases)。

离线升级教程：[Retro Yao-Mio 镜像文件的获取与烧写](Retro-Yao-Mio/chapter1-4)。

> retro-go-yao-mio 的主/次版本号遵循 retro-go 的发布。也就是只有当 retro-go 的主/次版本号发生变化时， retro-go-yao-mio 的主/次版本号才会发生变化，否则 retro-go-yao-mio 的其他更新只会变化修订版本号。比如，假设 retro-go 当前版本为 1.38.1，那么 retro-go-yao-mio 也是 1.38.1，如果 retro-go-yao-mio 在这之后发布了更新，那么下一个版本为 1.38.2，直到 retro-go 发布 1.39， retro-go-yao-mio的版本号才会变为 1.39，以此类推。由此可见，当你使用 retro-go-yao-mio 的主次版本号和的 retro-go 一致时，那么也就是相当于享受了 retro-go 相应的新特性。

> retro-go-yao-mio 的 master 分支会与 retro-go 的 master 保持一样，其所有的修改位于 yao-mio 分支，发布版本也是基于 yao-mio 分支。
