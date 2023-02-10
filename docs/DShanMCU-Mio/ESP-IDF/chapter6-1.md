
# 3.5寸LCD屏幕(SPI、无触摸)

此章节讲述使用 **[百问网3.5寸LCD屏幕(SPI)](https://item.taobao.com/item.htm?id=683875901407)** 的使用方法。

## 硬件准备

- [百问网3.5寸LCD屏幕(SPI、无触摸)](https://item.taobao.com/item.htm?id=683875901407)    * 1
- [屏幕配套排线](https://item.taobao.com/item.htm?id=683875901407)  * 1

### 接线

屏幕模块的一端是防呆接口，将配套的排线接入到屏幕这边之后，另一端按照下图的说明进行接线：

TFT LCD display Pin      | SPI pin | DShanMCU-Mio pin     
-------------------------|---------|----------------------
 GND                     |         | GND                  
 PWM                     |         | GPIO7                
 RESET                   |         | GPIO6                
 MOSI                    | MOSI    | GPIO11               
 SCK                     | SCK     | GPIO12               
 RS                      |         | GPIO5                
 CS                      | CS      | GPIO10               
 MISO                    | MISO    | -                    
 VCC                     |         | 3.3V                 


### 屏幕资料

屏幕对应规格书位置： `DShanMCU-Mio_ESP-IDF_Data\06_技术手册\3.5寸TFT LCD屏幕\百问网3.5寸液晶显示屏规格书.pdf`


## 软件准备

本次实验的项目代码位于： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\05_display\LCD\ST7796S-320x480\00_lcd_simple_test` 

> 注意，不要将项目代码移动到其他地方，否则编译会报错。后续实验也请保持原有的目录结构进行学习，不要移动项目代码的位置。


## 打开项目工程

通过 vscode 或 终端控制台打开项目工程目录，以便进行后续操作。

## 关键代码解读

屏幕配套的驱动库位于： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\00_components\esp-idf-components\tft_lcd_100ask_drivers`

```c

// 初始化 LCD
tft_lcd_100ask_hal_init();

/* 将整个屏幕刷为指定的颜色
   预定义的颜色有：
        #define TFT_LCD_COLOR_BLACK     0x0000
        #define TFT_LCD_COLOR_WHITE     0xFFFF
        #define TFT_LCD_COLOR_BLUE      0xF800
        #define TFT_LCD_COLOR_RED       0x07E0
        #define TFT_LCD_COLOR_GREEN     0x001F
*/
tft_lcd_100ask_hal_clear(color);

```

## 运行现象

直接点击编译即可，烧写到开发板之后，打开串口(波特率 115200)，即可看到输出信息和屏幕颜色一致。

## 修改默认的配置

打开 menuconfig，进入到下面所示的路径进行配置：

```shell
# (Top) → Component config → 100ask components → 100ASK SPI TFT LCD setting      
(Top)
    → Component config
        → 100ask components
            → 100ASK SPI TFT LCD setting      
```

## 运行LVGL项目工程

上面的示例能得到现象之后，便可打开此项目，打开后直接编译、烧写即可查看到屏幕中心区域输出了LVGL的版本信息，但是还没有按键控制的功能，也就是只能单纯的进行显示，在后面的章节我们会将讲解 **LVGL+FC手柄** 的综合示例。

这里的给出的项目代码位于： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\05_display\LCD\ST7796S-320x480\01_lcd_lvgl` 


> LVGL视频教程：[https://www.bilibili.com/video/BV1Ya411r7K2](https://www.bilibili.com/video/BV1Ya411r7K2) <br>LVGL文档教程：[http://lvgl.100ask.net](http://lvgl.100ask.net)
