
# 3.52寸墨水屏(SPI、无触摸)

此章节讲述使用 **[3.52寸墨水屏(SPI、无触摸)](https://item.taobao.com/item.htm?id=683875901407)** 的使用方法。

## 硬件准备

- [3.52寸墨水屏(SPI、无触摸)](https://item.taobao.com/item.htm?id=683875901407)    * 1
- [屏幕配套排线](https://item.taobao.com/item.htm?id=683875901407)  * 1

### 接线

屏幕模块的一端是防呆接口，将配套的排线接入到屏幕这边之后，另一端按照下图的说明进行接线：

E-paper display Pin      | SPI pin | DShanMCU-Mio pin     |  Notes
-------------------------|---------|----------------------|-------------
 BUSY                    |         | GPIO7                | 获取屏幕状态(繁忙/空闲)
 RESET                   |         | GPIO6                |
 D/C                     |         | GPIO5                |
 CS                      | CS      | GPIO10               |
 SCLK                    | SCK     | GPIO12               |
 SDI                     | MOSI    | GPIO11               |
 GND                     |         | GND                  | 
 VCC                     |         | 3.3V                 |          


### 屏幕资料

屏幕对应规格书位置： `DShanMCU-Mio_ESP-IDF_Data\06_技术手册\3.52寸墨水屏规格书\百问网3.52寸墨水屏规格书.pdf`


## 软件准备

本次实验的项目代码位于： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\05_display\E-paper\epd-240x360\00_epd_simple_test` 

> 注意，不要将项目代码移动到其他地方，否则编译会报错。后续实验也请保持原有的目录结构进行学习，不要移动项目代码的位置。


## 打开项目工程

通过 vscode 或 终端控制台打开项目工程目录，以便进行后续操作。

## 关键代码解读

屏幕配套的驱动库有两个： 

- 屏幕驱动库： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\00_components\esp-idf-components\epd_100ask_drivers`
- 画布库： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\00_components\esp-idf-components\epd_100ask_paint`

> 可以将画布理解为屏幕驱动的显存部分，通过其可以更好的管理、修改需要显示的数据。画布库是纯软件实现，不和具体的硬件绑死，也就是适用于后续其他更多的屏幕。


```c

// 初始化屏幕
epd_100ask_hal_init();

// 初始化画布
// 参数1： paint 需要是静态 、全局或动态分配的内存。
// 参数1： color 是指定初始化时默认的颜色
//         预设的颜色有：  #define EPD_100ASK_COLOR_WHITE     0xFF
//                        #define EPD_100ASK_COLOR_BLACK     0x00
epd_100ask_paint_init(paint, color);

// 将整个屏幕刷为指定的颜色
epd_100ask_hal_display_clear(color);

// 显示事先经过转换的图片，后面两个参数分别是指定图片的 宽(w) 和 高(h)
epd_100ask_hal_display_image(gImage_full_screen_test, 240, 360);

/* 刷新屏幕。注意：需要调用此函数才能在屏幕上显示出你要显示的数据
   刷新类型有：
        EPD_100ASK_LUT_GC (全局刷新，正常使用建议调用GC波形刷屏)
        EPD_100ASK_LUT_DU (局部刷新，长时间用DU波形刷屏会有低影，建议每调用DU波形刷屏5~10次后改用GC波形刷屏)
        EPD_100ASK_LUT_5S (不常用)
*/
epd_100ask_hal_refresh(EPD_100ASK_LUT_GC);

/* 局部刷新
    参数1：指定起始的x轴方向的坐标位置
    参数2：指定起始的y轴方向的坐标位置
    参数3：图片的宽度
    参数4：图片的高度
    参数5：图片数据
   之后需要使用 EPD_100ASK_LUT_DU 刷新类型。
*/
epd_100ask_hal_display_partial(0, y_offset, 32, 96, gImage_number_1);
epd_100ask_hal_refresh(EPD_100ASK_LUT_DU);  // 想要局部刷新时，使用此刷新类型


/*画布部分*/

// 在画布上画点
epd_100ask_paint_draw_point(10, 80, EPD_COLOR_BLACK, DOT_PIXEL_1X1, DOT_FILL_AROUND);

// 在画布上画线条
epd_100ask_paint_draw_line(20, 70, 70, 120, EPD_COLOR_BLACK, DOT_PIXEL_1X1, LINE_STYLE_SOLID);

// 在画布上画矩形
epd_100ask_paint_draw_rectangle(20, 70, 70, 120, EPD_COLOR_BLACK, DOT_PIXEL_1X1, DRAW_FILL_EMPTY);

// 在画布上画圆形
epd_100ask_paint_draw_circle(45, 95, 20, EPD_COLOR_BLACK, DOT_PIXEL_1X1, DRAW_FILL_EMPTY);

// 画布的数据刷为指定的颜色
epd_100ask_paint_clear(EPD_100ASK_COLOR_WHITE);

// 将画布的内容传输到屏幕
epd_100ask_hal_display_image(paint, w, h);

// 刷新屏幕
epd_100ask_hal_refresh();

```

## 运行现象

直接点击编译即可，烧写到开发板之后，打开串口(波特率 115200)，即可看到输出信息和屏幕颜色一致。

## 修改默认的配置

打开 menuconfig，进入到下面所示的路径进行配置：

屏幕驱动配置：

```shell
# (Top) → Component config → 100ask components → 100ASK EPD setting     
(Top)
    → Component config
        → 100ask components
            → 100ASK EPD setting      
```

画布配置：

```shell
# (Top) → Component config → 100ask components → 100ASK EPD  paint setting   
(Top)
    → Component config
        → 100ask components
            → 100ASK EPD  paint setting      
```


## 运行LVGL项目工程

上面的示例能得到现象之后，便可打开此项目，打开后直接编译、烧写即可查看到屏幕中心区域输出了LVGL的版本信息，但是还没有按键控制的功能，也就是只能单纯的进行显示，在后面的章节我们会将讲解 **LVGL+FC手柄** 的综合示例。

这里的给出的项目代码位于： `DShanMCU-Mio_ESP-IDF_Data\02_examples\esp-idf-learn\05_display\E-paper\epd-240x360\00_epd_simple_test` 


> LVGL视频教程：[https://www.bilibili.com/video/BV1Ya411r7K2](https://www.bilibili.com/video/BV1Ya411r7K2) <br>LVGL文档教程：[http://lvgl.100ask.net](http://lvgl.100ask.net)
