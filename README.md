# 在联想G50-70上安装macOS
## 写在前面
* 因为在家闲着无聊，就决定试着在这台老设备上安装macOS。
* 由于文件太乱，所以我决定将EFI都放在[`Releases`](https://github.com/Moore2253/Install-MacOS-On-Lenovo-G50-70/releases)里，所以源代码只有`README.md`这一个文件。
* 本来想顺便写个文字安装教程，但我懒得继续写下去了，就算了吧。
## 机型配置
* 设备名：Lenovo G50-70 （20351）
* 仿冒机型：MacbookPro11,1 （视网膜显示屏，13 英寸，2013 年末）
* 处理器：Intel i5-4288u 双核 2.60Ghz   （4代U的机子能健在已经是丫霸的了）
* 运行内存：8GB 1600Mhz DDR3   （4GB已经不够用了，问就是微软！再加1根吧）
* 当前安装的Windows版本：Windows10 22H2 19045.4170   （这个CPU只能windows10了，11卡死）
* 当前安装的macOS版本：macOS Big Sur 11.7.10   （苹果官方只允许这个版本了，修补其它机型装更新的版本冒一堆问题）
* 当前使用的引导版本：OpenCore 099 开发版  （诈尸更新）
* 声卡：Conexant SmartAudio HD   （正常驱动）
* 无线网卡：Qualcomm Atheros AR956x Wireless Network Adapter   （正常驱动）
* 有线网卡：Realtek PCIe GBE Family Controller (RTL8168)  （正常驱动）
* 核显卡：Intel Iris Graphics 5100 1536MB  （正常驱动）
* 独显卡：AMD redeon HD 8500M / R5 M230 （无法驱动）
* 蓝牙：Qualcomm Atheros AR3012 Bluetooth 4.0  （能用？不能用？时好时坏）
* 硬盘：tigo S320 128GB   （更换成了固态硬盘，机械已经带不动了）
## 更新随笔
* 2024年3月  说来话长，原账号[@Moore2253](https://github.com/Moore2253)被我弄2FA弄炸了，验证不进去，没法登录，只好创小号，刚好把这老机子翻了出来，顺手更新oc到099，上传到这里备份。
* 2021年11月 配置基本完工，再次升级OpenCore，bug fix。
* 2021年10月 继续完善和升级OpenCore，重新注入三码，新增一些可以驱动的kext，修复引导的一些bug。
* 2021年9月 我在GitHub查找同机型的efi时看到[`@mirifi2k`](https://github.com/mirifi2k/)的[这篇文章](https://www.tonymacx86.com/threads/guide-lenovo-g50-80-80l0-and-catalina-10-15-2.288303/)使用`OpenCore`引导了Mac，然后我将它下载下来进行测试，发现能正常引导我的Mac，并且一部分硬件已经驱动，所以我在此efi基础上加以修改，使其能更完美的使用OpenCore引导我这台Hackintosh。
* 2021年8月 再次尝试更新，更新很成功，升级Clover，修复一些失效的驱动，修复和添加ACPI。
* 2021年7月 尝试更新Big Sur，但出现了一些问题，放弃更新继续优化Clover。
* 2021年6月 配置有了一些进展，网络、声音、显示等基本正常，升级到Catalina，日用基本OK。
* 2021年5月 首次接触macOS Mojave和Clover，对其进行配置。
