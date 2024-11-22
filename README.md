# XiaoXinPro13_hackintosh_OC
## Lenovo XiaoXin Pro13（S）i5-10210U/i7-10710U (for intel AX201) 
这份EFI基于[原作者](https://github.com/lovesakuratears/XiaoXinPro13_hackintosh_OC)的修改而来, 特别感谢[lovesakuratears](https://github.com/lovesakuratears)让这个电脑的EFI支持到了macos14+, 再次感谢lovesakuratears的热情回复和各位大佬的无私奉献!

`特别声明: 本人并非黑苹果专业户, 大部分步骤可能不专业, 请自行备份您的文件`
本项目仅仅只是修改原作者项目到修改intel-AX201网卡可以使用, 已更换博通或者其他白果卡请移步至原作者项目

|规格 | [详细信息](https://item.lenovo.com.cn/product/1007854.html) |
|:-: | :-:|
|电脑型号|联想小新pro13 笔记本电脑|
|操作系统|macOS Sonoma 14.4.1 (23E224) |
|处理器|英特尔 酷睿 i5 - 10210U|
|内存|16GB板载无法更换|
|硬盘|忆联AH530 |
|显卡|Intel HD Graphics CFL CRB|（UHD620）|
|显示器|13.3 英寸 IPS 2560x1600|
|声卡|Realtek ALC257|
|网卡|Intel AX201|
|网卡解决方案|itlwm 和 HeliPort|




`需要操作步骤请直接移步到下方具体步骤处`
`目前还搞不明白为什么AirportItlwm无法正确加载, 使用 itlwm 和 HeliPort 解决方案`
`成品EFI在release里面, 仓库里的EFI文件夹是原作者的EFI哦(博通和白果卡)!不要下错了`


## 项目基于
### EFI相关
[daliansky/XiaoXinPro-13-hackintosh](https://github.com/daliansky/XiaoXinPro-13-hackintosh)

[lovesakuratears/XiaoXinPro13_hackintosh_OC](https://github.com/lovesakuratears/XiaoXinPro13_hackintosh_OC)

### 网卡相关
[驱动内置英特尔无线网卡](https://github.com/daliansky/XiaoMi-Pro-Hackintosh/wiki/%E9%A9%B1%E5%8A%A8%E5%86%85%E7%BD%AE%E8%8B%B1%E7%89%B9%E5%B0%94%E6%97%A0%E7%BA%BF%E7%BD%91%E5%8D%A1)

[intel-wifi驱动下载](https://github.com/daliansky/XiaoMi-Pro-Hackintosh/wiki/%E9%A9%B1%E5%8A%A8%E5%86%85%E7%BD%AE%E8%8B%B1%E7%89%B9%E5%B0%94%E6%97%A0%E7%BA%BF%E7%BD%91%E5%8D%A1)

[intel-蓝牙驱动下载](https://github.com/OpenIntelWireless/IntelBluetoothFirmware/releases/tag/v2.4.0)

[蓝牙驱动安装官方指导](https://openintelwireless.github.io/IntelBluetoothFirmware/FAQ.html#what-additional-steps-should-i-do-to-make-bluetooth-work-on-macos-monterey-and-newer)



## 具体步骤
`如果你已经安装macos14+请跳过此步骤`
1.下载系统[镜像](https://macos.mediy.cn/macOS%20Sonoma%2014/)
`我下载的是14.4.1`与EFI原作者保持一致, 确保EFI正常工作, 其他系统暂不清楚兼容性问题(如果链接失效请自行查找对应版本的下载链接)

2.使用写盘工具写盘, 写完之后进入(我下的镜像自带windows内核PE), 使用DG进行EFI替换
`请注意, 务必替换三码`

3.下载成品EFI或者是自己去上面的对应链接中下载`kext`进行替换


配置文件编辑软件[OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools/releases)下载

`请注意, 我直接用这个软件编辑会导致报错, 使用vscode手动编辑的config文件`
`请注意, 我并没有安装Windows/Macos双系统, EFI文件中没有Windows文件夹, 需要自行添加`


## 其他
我去除了原作者config中关于博通和80211相关的驱动, 并且添加了AX201对应的itlwm 和 HeliPort, Bluetooth驱动
如果出现问题, 请去上述仓库中自行找到对应系统文件的版本进行替换


