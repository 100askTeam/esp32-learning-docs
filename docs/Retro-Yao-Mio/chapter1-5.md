# retro-go-yao-mio 的配置

在第一章中我们已经说明过，为了避免混淆这里再说明一下：Retro-Yao-Mio是开发套件(硬件)，retro-go-yao-mio 是为其量身定制的软件项目。

## 语言

retro-go-yao-mio 当前还不支持中文及中文界面。

## 主题

retro-go-yao-mio 支持主题切换，主题文件保存在SD卡的这个目录： `/retro-go/themes`

### 删除主题

如果你需要删除某些主题，请将sd卡中的 `/retro-go/themes` 相应主题目录删除即可。

### 添加主题

支持DIY主题，请在下面列出的地址获取我们对主题支持的仓库：

- Github：[https://github.com/100askTeam/retro-go-themes](https://github.com/100askTeam/retro-go-themes)

建议参考 retro-go-themes 定制你的主题。

如果你需要获取我们定制的最新主题请下面列出的地址获取发布版本：

- Github：[https://github.com/100askTeam/retro-go-themes/releases](https://github.com/100askTeam/retro-go-themes/releases)

之后将 retro-go-themes 中的 `themes` 目录下的内容复制到sd卡中的 `/retro-go/themes` 目录下即可(若提示文件重复则选择覆盖)。


## ROMs(游戏文件)

ROMs是游戏模拟器使用的游戏文件，没有他们游戏模拟器就无法发挥作用。

!> 我们提供的ROMs可以在 [sd卡资料包](https://forums.100ask.net/t/topic/2991#sd-3) 获取，**仅供学习交流使用**(如有冒犯请联系我们马上对其进行删除)。如果你需要更多的ROMs请自行解决，我们不对更多的ROMs进行收集分享，敬请谅解。

### 修改ROMs

修改ROMs非常简单，所有的ROMs存放在SD卡的这个目录中：`/roms`，这个目录中将游戏类型进行了目录分类，按照自己的需求进行操作相应的目录即可。

| 目录 | 模拟器类型 | 文件后缀 |
| :---- | :---- | :---- |
| nes | Nintendo Entertainment System | .nes .fc .fds .nsf |
| snes | Super Nintendo | .smc .sfc |
| gb | Nintendo Gameboy | .gb .gbc |
| gbc | Nintendo Gameboy Color | .gbc .gb |
| gw | Nintendo Game & Watch | .gw |
| sms | Sega Master System | .sms .sg |
| gg | Sega Game Gear | .gg |
| md | Sega Mega Drive | .md .gen .bin  |
| col | Coleco ColecoVision | .col |
| pce | NEC PC Engine | .pce |
| lnx | Atari Lynx | .lnx |
| doom | DOOM | .wad |

