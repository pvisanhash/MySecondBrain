---

author: aitx

title: 安装Windows11与Manjaro双系统

time: 2022-08-09 周三

tags: 
  - Windows11
  - Manjaro
  - Windows
  - Win
  - Linux
  - 双系统

---

# 1 安装Windows11

下载[Win11镜像](https://www.microsoft.com/zh-cn/software-download/windows11 win11)

下载[Ventoy工具](https://www.ventoy.net/cn/download.html ventoy)

下载[微PE工具](https://www.wepe.com.cn/download.html 微PE)

将下载的微PE制作U盘工具

将下载的Ventoy制作U盘工具,然后将Win11镜像放入其中

插入微PE U盘,重启电脑,调整Boot设备,选择微PE这一项,使用分区精灵进行分区,建议将ESP分区调整为500M

> ESP = EFI System Partition = Extensible Firmware Interface System Partition = 其实就是系统Boot分区
> 
> MSR = Microsoft Reserved Partition

插入Ventoy U盘,重启电脑,调整Boot设备,选择Ventoy这一项,选择Win11镜像进行安装

安装过程中建议关闭网络并跳过联网,键盘按住shift+F10，弹出cmd命令框,输入以下命令即可

```cmd
OOBEBYPASSNRO
```

# 安装Manjaro

下载[Manjaro镜像](https://manjaro.org/download/ Manjaro下载)

将下载的Manjaro镜像放到Ventoy的U盘中

插入Ventoy U盘,重启电脑,调整Boot设备,选择Ventoy这一项,选择Manjaro镜像进行安装

其中分区是比较重要的点:

```properties

/boot/efi ,fat32 一般是300M/500M.相当于Windows的ESP分区,标记为boot

/,ext4 ,根分区根据实际的来,相当于Windows的C盘,标记为root

/swap 一般是实际内存的1.5~2倍,相当于Windows的虚拟内存,标记为swap

/home ,ext4,家目录根据实际的来,
```

选择办公套件，建议选择`LibreOffice`，尽管`FreeOffice`与`Microsoft Office`系列很相似，但是Bug比较多，而且不是免费的。

