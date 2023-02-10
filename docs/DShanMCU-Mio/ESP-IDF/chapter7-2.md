
# Micro SD卡(SPI)

此章节讲述使用 **[Micro SD卡(SPI)]()** 的使用方法。

## 硬件准备

- Micro SD卡(≤2TB)    * 1
- SPI Micro SD卡模块  * 1

### 接线

按照下图的说明进行接线：

MicroSD Card Adapter pin | SPI pin | DShanMCU-Mio pin     |  Notes
-------------------------|---------|----------------------|-------------
 CS                      | CS      | GPIO15/GPIO8         |
 SCK                     | SCK     | GPIO16/GPIO12        |
 MOSI                    | MOSI    | GPIO17/GPIO11        |
 MISO                    | MISO    | GPIO18/GPIO13        |    


## 软件准备

本次实验的项目代码位于： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\06_storage\spi_sdcard` 

> 注意，不要将项目代码移动到其他地方，否则编译会报错。后续实验也请保持原有的目录结构进行学习，不要移动项目代码的位置。


## 打开项目工程

通过 vscode 或 终端控制台打开项目工程目录，以便进行后续操作。

## 关键代码解读

配套的驱动库：  `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\00_components\esp-idf-components\fs_100ask_drivers`


```c

// 初始化SD卡
fs_100ask_hal_init();

// 打开文件
fopen

// 关闭文件访问
fclose

// 重命名文件名
rename

// 读取文件内容
fgets

// 去初始化SD卡
fs_100ask_hal_deinit();
```

## 运行现象

直接点击编译即可，烧写到开发板之后，打开串口(波特率 115200)，即可看到输出信息，之后拔出SD卡接入到PC中查看。

## 修改默认的配置

打开 menuconfig，进入到下面所示的路径进行配置：

屏幕驱动配置：

```shell
# (Top) → Component config → 100ask components → 100ASK File system drivers setting    
(Top)
    → Component config
        → 100ask components
            → 100ASK File system drivers setting     
```
