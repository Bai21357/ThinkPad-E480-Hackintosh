<div align="center">
<img src="https://img.skk.moe/2020/02/01/15deff1c-62cc-45b9-aac2-2f6bb9a4350b.jpg" width="350px">

</div>

# ThinkPad-E480-Hackintosh

ThinkPad E480 黑苹果EFI文件 使用OpenCore 1.04

## 电脑配置

|规格|详细信息|
|-|-|
|型号|ThinkPad E480(20KNA004CD)|
|处理器|Intel® Core™ i5-8250U 1.6 GHz|
|内存|8GB DDR4 2666MHz X2|
|固态硬盘|PC005 Active 500GB M.2|
|集成显卡|Intel UHD Graphics 620|
|声卡|Conexant CX20753/4|
|有线网卡|Realtek R8111GUS|
|无线网卡|Realtek RTL8821CE -> BCM94352Z (DW1560)|

## 支持系统

支持macOS Sequoia (测试版本15.5) 
> 无线网卡在安装OCLP和修补后才可正常驱动 教程: [如何在macOS Sonoma和Sequoia黑苹果系统中驱动BCM94352](https://www.bilibili.com/opus/987828407802789892)

> 此处有个较为严重的Bug
> 网卡驱动后不可以在设置连接wifi,否则会报错,需要点击任务栏右上角wifi图标连接
> 在设置可以看到网络状态,但是不能在设置连接网络.

## 工作正常

- CPU：变频正常

- 硬盘：工作正常

- 集成显卡：显存已设置为3072MB。支持HDMI `2K@60Hz`、`1080P@60Hz`

- 声卡：AppleALC仿冒 注入ID:15，工作正常

- 有线网卡：工作正常

- 电池：电量、电池状态显示正常

- USB：读写文件、数据传输正常

- 触摸板：工作正常

- 小红点：工作正常

- 摄像头：工作正常

## 工作异常

- 读卡器无法正常驱动，且无解

## 已知Bug

- 休眠醒来后有概率触发wifi,蓝牙无法正常连接

- - Fn键未映射

## 注意事项：

1. BIOS中更改如下：

- Security
  - Secure Boot > Secure Boot: Disabled
  - Intel(R) SGX > Intel (R) SGX Control: Disabled

- Startup
  - UEFI/Legacy Boot: Both
  - UEFI/Legacy Boot Priority: UEFI First
  - Optional Key Display: Enabled

- Config
  - Storage > Controller Mode: AHCI mode

2. 安装完成后如需登录AppleID请修改机器三码。
   教程链接 : [macos配置备忘录](https://www.bilibili.com/opus/1068138626882207753)
## 更新

### 2025-08-08
OpenCore版本: 1.04
- 首次上传。

## 截图 

![图片](https://youke1.picui.cn/s1/2025/08/08/689618e97c534.png)

![图片](https://youke1.picui.cn/s1/2025/08/08/6896190aadcf5.png)

![图片](https://youke1.picui.cn/s1/2025/08/08/689618baae13d.png)

![图片](https://youke1.picui.cn/s1/2025/08/08/689614d90af7e.png)

## 致谢
  github [灰尘墨言](https://github.com/huichenmoyan).<br>   

 [Sukka](https://skk.moe/)
  
  以及广大为黑苹果做出贡献的人
