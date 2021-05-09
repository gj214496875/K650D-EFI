# K650D-OC-EFI

|   规格  |详细信息     |
|:---:|:---:|
|   CPU  |  Intel Haswell i7-4710MQ   |
|   显卡  |   Intel HD Graphics 4600 + NVIDIA GeForce GTX 850M（已屏蔽）  |
|   声卡  |   VIA VT1802P  |
|    网卡 |   RealtekRTL8111 + BCM94352HMB（更换） |
|    版本 |   big sur 11.3 |
#硬件驱动情况
* 显卡：必须屏蔽独显，只能驱动核显hd4600
* 声卡：使用AppleALC仿冒Apple内建声卡，配置layout-id为65
* 有线网卡：使用RealtekRTL8111.kext驱动就可以了
* 无线网卡+蓝牙：更换为Mini pci-e接口的博通 BCM94352HMB，需要用胶带屏蔽51针脚，使用AirportBrcmFixup+BrcmFirmwareData+BrcmPatchRAM3+BrcmBluetoothInjector驱动，可完美使用AirDrop HandOff SideCar等（新版AirportBrcmFixup驱动需要删除驱动包里的AirPortBrcm4360驱动）
* 睡眠+休眠：正常，可以正常休眠及键鼠唤醒
* USB：使用usbinjectall配合hackintool进行端口定制，可正常使用USB
* 内置键盘+触控板：使用ApplePS2SmartTouchPad驱动


