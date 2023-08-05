---

author: aitx

title: 显示器 Display Device

time: 2022-10-30 周日

tags: 
  - 显示器
  - IPS
  - 分辨率

---

# VESA孔

VESA =  Video Electronics Standards Association，视频电子标准协会
VESA孔是指支持此显示器背部孔位是符合VESA标准的，可以更方便更换支架，支持壁挂。常用尺寸为75mm * 75mm，100mm * 100mm。

# OSD 屏幕菜单

OSD = on-screen display 屏上显示，就是屏幕菜单

# 视频接口

## VGA

Video Graphics Array，视频图形阵列，模拟信号的电脑显示标准。

## DVI

Digital Visual Interface，数字视频接口，可传输数字信号与模拟信号。

## HDMI

High Definition Multimedia Interface，高清多媒体接口。

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210310130903.png)

![](![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210310127141.png)
## DP

display port，显示接口。

![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210310129420.png)

# 屏幕尺寸

指的是对角线的长度

# 宽高比

主流宽高比是16:9，其他如4:3，16:10，21:9，32:9

# 像素 pixel

普通图片通常是由一个个像素构成，像素又由三基色（RGB）混合而成

# 分辨率 Resolution

显示分辨率是指水平像素和垂直像素的数量
1080 指的是 1920 X 1080，指的就是横向水平1920个像素点，纵向垂直1080个像素点。 
2K = 2560 X 1440  
4K = 3840 X 2160
注：K=1000, P = pixe

## 数字电视分辨率标准

- 高清HD（High Definition）：1280 * 720
- 全高清FHD（Full HD）：1920 * 1080

# PPI

pixel per inch，每英寸像素数，计算公式 PPI=√(X²+Y²)/ Z (X:长度像素数；Y:宽度像素数；Z:屏幕尺寸)

# DPI

dots per inch，每英寸点数（用于打印时），与PPI一样， dpi=(√(横向分辨率^2+纵向分辨率^2))/屏幕尺寸

# 帧数 frame

就是显卡输出给显示器的每秒画面数

# 帧率 FPS

frame per second 每秒帧数

# 刷新率 refresh rate

60HZ/144HZ，就是显示器在一秒内能显示的60次/144次的画面数

## EDID 显示器参数

扩展显示识别数据（extended display identification data），存储在显示器中的预置显示器参数。当显示器连接到电脑上时，会读取到此参数并供给用户选择参数。

## 检测刷新率

当我们买到显示器时，可以通过以下的方式检测是否刷新率虚标。
访问网[UFOTEST](https://www.testufo.com/) 右上角选择Frame Skipping 跳帧测试，然后选择相机调整[[相机 Camera#曝光|曝光]]时间，比如将曝光时间调整为1/10秒，则60HZ的显示器会显示6-8个白块，144HZ的显示器会显示15个白块。

# 响应时间

像素点在切换颜色时所花费的时间

## 黑白响应时间

纯黑，纯白之间的切换所花费时间

## 灰阶响应时间 GTG

GTG：grey to grey 灰到灰
从一个中间色到另一个中间色的转换时间

# 垂直同步

## 画面撕裂

首先，假设显示器从上到下逐行显示画面。理想的情况下，显卡输出帧率与显示器的刷新率一致，无画面撕裂；当显卡输出帧率 > 显示器的刷新率时，则显示器还在刷新当前帧时，显卡发送了最新的帧让显示器显示，则显示器下部分显示最新帧的内容，画面撕裂；当显卡输出帧率 < 显示器的刷新率时，则显示器画完当前帧时，显卡还未成下一帧，则显示器继续画上一帧，这时显卡生成好下一帧，则显示器下部显示最新帧，画面撕裂

## VSync

vertical sync垂直同步
显示器当主角，控制显卡的速率，当显示器还在会制画面时，不立即使用显卡生成的帧，让他等显示器完成后再使用。显然当显卡输出帧率 < 显示器的刷新率时，会重复画多个机同帧，这样会导致观感上的延迟。

## FreeSync

AMD推出的技术，基于VRR(Variable Refresh Rate)，解决**当显卡输出帧率 < 显示器的刷新率时**，导致的画面撕裂。现在显卡是主角，当显卡还没有生成最新的帧给显示器时，让显示器的刷新率变低，如144HZ的显示器变成67HZ等。

显然，此技术只能解决显卡输出帧率 < 显示器的刷新率的画面撕裂问题。当显卡输出帧率 > 显示器的刷新率时，这时候可以通过如下方法解决

- 限制显卡帧率（锁帧）
- 使用更高刷新率的显示器

# 色域 color space

色域，即色彩空间，就是显示器能显示的色彩范围，是颜色的某个完全的子集。图中最大色彩范转是人眼可见色彩范围。

[色域Wiki](https://en.wikipedia.org/wiki/Color_space)

## 色域容积

也称色域面积，指的是显示器的色彩范围占人类可见色彩范围面积。通常将些面积与某标准的色域面积作比较，得出120%sRGB。

## 色域覆盖

色域覆盖指的是重合率，指与某标准的重合率，所以最大只有100% sRGB。


![](https://raw.githubusercontent.com/pvisanhash/PicSiteRepo1/main/note/img/202210300232596.png)

## NTSC

National Television System Committee 美国国家电视系统委员会，制定的NTSC色域标准，NTSC色域容积更大

## sRGB

standard RGB，标准RGB，计算机行业常用

## DCI-P3

Digital Cinema Initiative-Protocal 3，数字影院计划-协议3，电影行业使用较多。

## Adobe RGB

印刷行业使用较多

# 色准 color distance/difference

显然，我们数据存储的某个RGB的值，显示器显示后的颜色与标准色越接近越好。色准是用△E来表示显示器显示颜色的准确度。

# 色深 color depth

> 色阶，表示图像亮度强弱的指数标准。像素由RGB调节自身的亮度强弱来构成，一个阶梯代表一个色阶。所以色阶越多，色彩显示越平滑。

比如8bit，指的是RGB中单个R（G/B）在色彩过渡时有2^8=256个色阶，则一个像素可显示(2^8)^3=2^24个颜色。

## FRC 抖动

Frame Rate Control，帧率控制，比如这里有个浅灰，有个深灰，现在要显示中间灰，则通过快速在两个颜色间变换，则能欺骗人眼认为是中间灰。所以10bit色深的显示器可能是8抖10。

# HDR

HDR = High Dynamic Range，高动态范围。
SDR = Standard Dynamic Range，标准动态范围。

自然中，光亮度强弱的范围很大，但在计算中只能记录相对小的范围的明暗信息，HDR相对SDR就能显示更多范围的明暗信息。

# LCD

Liquid Cystal Display 液晶显示器

## IPS

In-Plane Switching 平面转换型
优点：色彩好，广视角，响应速度快，普通用户常用
缺点：漏光

## VA

Vertical Alignment 垂直排列
优点：对比度高，广视角（低于IPS），色彩表现不如IPS，曲面屏常用
缺点：响应速度最差

## TN

Twisted Nematic 扭曲向列型
优点：响应速度最快，电竟常用
缺点：色彩表现最差，可视角度差

# OLED

有机发光二极管（Organic Light Emitting Diode）


