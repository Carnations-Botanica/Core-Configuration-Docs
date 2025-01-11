---
layout: default
title: Kexts
parent: EFI Setup
grand_parent: Gathering Files
description: 
nav_order: 3
has_children: false
has_toc: false
---

<style>
  .navigation-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 100%;
  }
  
  .nav-button {
    margin: 10px;
  }

  .top-button {
    margin: 10px;
    align: center;
  }
</style>

<p align="center">
  <img width="650" height="200" src="../../../../assets/Headers/Header-OpenCore-Kexts.png">
</p>

<h2 align="center">Everything you need to know.</h2>
<br>

A kext is short for **K**ernel **ext**ension. These extensions make it possible to extend the functionality of the operating system without having to recompile the kernel itself. Kexts are similar to drivers in Windows because they allow the kernel to communicate with the computer's hardware and are often used to add support for new hardware or improve existing hardware features.

Kext files are actually bundles that contain multiple files, similar to ZIP archives, but are not compressed - that's why they appear as folders in Windows or Linux. In OS X / macOS, you can view the contents of a kext file by right-clicking it and selecting “Show Package Contents”, in other OS, you can simply treat them like folders.

However, Apple has started to [reduce](https://support.apple.com/guide/deployment/system-and-kernel-extensions-in-macos-depa5fb8376f/web){:target="_blank"} the use of kexts, especially since macOS Big Sur, as they can cause security issues. For us, they are essential to get OS X / macOS running.

We want to make sure we're always grabbing the most minimal amount of kexts for our purposes of booting recoveryOS as a sanity check. You'll find you will always need the following:

- [Lilu](https://github.com/acidanthera/Lilu/)

- [VirtualSMC](https://github.com/acidanthera/VirtualSMC/)

Lilu is a patching engine that plugin kexts will use. Many popular hackintosh kernel extensions are Lilu plug-ins meaning it is a requirement, while VirtualSMC provides your system with the SMC device of a real Mac computer, which is required to pass the [DSMOS]() test during boot. From the charts below, you will be able to determine what else you will require to boot your system.

**The rest of this page documents all known Kexts and their purpose for safe keeping.**

You will NOT need every single kext. Focus on maintaining the minimal amount of kexts to boot the recoveryOS environment. Much later, we can figure out what is missing and add additional kexts based on your hardware.

<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../02-Drivers/">&larr; Back Page</a>
    <a class="nav-button" href="../04-Tools/">Next Page &rarr;</a>
  </div>
  <br>
</h2>

---

# **CPU Related**
You may have noticed that Macs have always come with a very limited variety of hardware. This is because the operating system is not designed for broad compatibility, but rather for maximum customization. After all, why support more hardware if you are the sole manufacturer? We don't have the exact hardware that was built into Macs. Therefore we need to patch the kernel according to our hardware and have to deal with Apple's System Management Controller (SMC).

## [VirtualSMC](https://github.com/acidanthera/VirtualSMC){:target="_blank"}
Acidanthera's VirtualSMC emulates Apple's SMC found on real Macs inside the kernel. It is essential for running macOS on non-native hardware. VirtualSMC is the basis for other kexts, some of which have to be downloaded separately. VirtualSMC comes bundled with several plugins, which are listed below.
VirtualSMC supports all macOS versions (OS X 10.4 Tiger to macOS 15 Sequoia).
<!--Add later, probably in troubleshooting/panic section: Why does VirtualSMC show in every page fault kernel panic?
In most cases VirtualSMC is unrelated to any kernel panic you experience. The reason it is present in stacktrace is becauase VirtualSMC wraps kernel_trap to emulate SMC device. -->

* ### SMCBatteryManager
SMCBatteryManager is a VirtualSMC plugin that provides detailed battery information, including the current percentage. As the name suggests, it requires you to have a battery, therefore you shouldn't use it on Desktops.
SMCBatteryManager supports all macOS versions (OS X 10.4 Tiger to macOS 15 Sequoia).

* ### SMCDellSensors
SMCDellSensors is a plugin for VirtualSMC. This plugin is specifically designed to support Dell laptops and desktops by providing sensor data to macOS. As the name suggests, it requires you to have a system manufactured by Dell. Don't use it if you don't have a Dell machine.
SMCDellSensors supports OS X 10.7 Lion to macOS 15 Sequoia.

* ### SMCLightSensor
SMCLightSensor is a plugin for VirtualSMC. This plugin is specifically designed to provide ambient light sensor data to macOS, allowing the system to adjust screen brightness and other settings based on the surrounding light conditions. This kext requires a light sensor, which is typically found only in higher-end laptops. If your laptop doesn’t support automatic brightness adjustment in Windows, this kext won’t function. When in doubt, it’s best to skip it.
SMCLightSensor supports OS X 10.6 Snow Leopard to macOS 15 Sequoia.

* ### SMCProcessor
SMCProcessor is a VirtualSMC plugin used to read CPU temperature on Intel based systems (Penryn and newer).
SMCProcessor supports OS X 10.7 Lion to macOS 15 Sequoia.

* ### SMCSuperIO
SMCSuperIO is a VirtualSMC plugin that can read and edit fan speeds. It may require additional patching. 
SMCLightSensor supports OS X 10.6 Snow Leopard to macOS 15 Sequoia.

---

### [SMCAMDProcessor & AMDRyzenCPUPowerManagement](https://github.com/trulyspinach/SMCAMDProcessor){:target="_blank"}
SMCAMDProcessor is the counterpart to SMCProcessor that comes bundled with AMDRyzenCPUPowerManagement. 
AMDRyzenCPUPowerManagement (that is actually not a VirtualSMC plugin) provides power management features for AMD Processors. SMCAMDProcessor is a VirtualSMC plugin that collects sensor data - however, you can't use it without AMDRyzenCPUPowerManagement.
In addition, these kexts allow PState editing and manual switching of clock speeds inside the bundled AMD Power Gadget tool.
Note that SMCAMDProcessor & AMDRyzenCPUPowermanagement don't work as intended on AMD based laptops. Using these kexts may result in increased temperatures and reduced battery life.

In theory, SMCAMDProcessor and AMDRyzenCPUPowerManagement support OS X 10.8 Mountain Lion up to macOS 15 Sequoia. However, AMD support (without a lot of patching) is only available in macOS 10.13 High Sierra to macOS 15 Sequoia.

---

### [SMCProcessorAMD](https://github.com/macos86/SMCProcessorAMD){:target="_blank"}
SMCProcessorAMD is very similar to SMCAMDProcessor. The key difference is that SMCAMDProcessor is dependent on AMDRyzenCPUPowerManagement - if you don't want to use AMDRyzenCPUPowerManagement for some reason (e.g. you own a laptop), you can use SMCProcessorAMD.
SMCProcessorAMD supports OS X 10.7 Mountain Lion up to macOS 15 Sequoia. However, AMD support (without a lot of patching) is only available in macOS 10.13 High Sierra to macOS 15 Sequoia.

---

### [AsusSMC](https://github.com/hieplpvip/AsusSMC){:target="_blank"}
AsusSMC is a VirtualSMC plugin that provides support for built-in Ambient Light Sensors (ALS), keyboard backlight control, battery sensors and Fn key support on Asus laptops. As the name suggests, this only applies to Asus laptops.
In theory, AsusSMC supports OS X 10.8 Mountain Lion up to macOS 15 Sequoia.

---

### [YogaSMC](https://github.com/zhen-zen/YogaSMC){:target="_blank"}
Just as AsusSMC, YogaSMC is a VirtualSMC plugin that provides sensor readings to the SMC. As the name suggests, this only applies to Lenovo laptops. Make sure to read the readMe if you have such a Lenovo laptop.
It is not known to us which versions YogaSMC supports. Please let us know which ones are possible.

---

### [BigSurface](https://github.com/Xiashangning/BigSurface){:target="_blank"}
BigSurface is, among other things, a VirtualSMC plugin that provides sensor data to the SMC on certain Surface devices. Read the ReadMe if you have a Microsoft device.
In theory, BigSurface supports macOS 10.12 Sierra up to macOS 15 Sequoia.

---

### [SMCRadeonSensors](https://github.com/ChefKissInc/SMCRadeonSensors){:target="_blank"}
SMCRadeonSensors is a VirtualSMC plugin that provides temperature readings on AMD GPUs.
SMCRadeonSensors supports macOS 10.14 Mojave up to macOS 15 Sequoia.

# **Graphics Related**

## [WhateverGreen](https://github.com/acidanthera/WhateverGreen/){:target="_blank"}
Whatevergreen (known years ago as NvidiaGraphicsFixup, IntelGraphicsFixup, IntelGraphicsDVMTFixup, CoreDisplayFixup and Shiki) provides a [range of patches and fixes](https://github.com/acidanthera/WhateverGreen/?tab=readme-ov-file#features) for GPUs from all manufacturers (ATI/AMD, Intel, Nvidia). The primary purpose of WhateverGreen is to address issues that arise when macOS does not natively support certain GPUs. Almost all GPUs (apart from completely unsupported cards as well as AMD APUs and Navi22) benfit from it. 
WhateverGreen supports OS X 10.6 Snow Leopard to macOS 15 Sequoia.

---

## [NootedRed](https://github.com/ChefKissInc/NootedRed){:target="_blank"}
NootedRed provides support for Vega-based APUs. Oversimplified, it patches existing Vega drivers that exist for dGPUs. This is possible because APUs and dGPUs are designed very similarly. However, NootedRed comes with several issues that make smooth operation not always possible. Furthermore, the author of the kext does not accept issues anymore - you're on your own using this kext.

---

## [NootRX](https://github.com/ChefKissInc/NootRXNootedRX){:target="_blank"}
NootRX is a kext providing patches for Navi21, -22 and -23 based GPUs. Just as NootedRed, NootRX comes with issues. WhateverGreen is able to provide patches for Navi21 and -23, NootRX is only necessary for Navi22. Just as for NootedRed, the author of the kext disabled the issue section - you're on your own using this kext.

{: .note }
If you want to use an eGPU, you should take a look at [Kryptonite](https://github.com/mayankk2308/kryptonite?tab=readme-ov-file){:target="_blank"}. However, the further process of using this kext is not covered in this guide.


# Other CPU related kexts

## General
- RestrictEvents -> Not really CPU related, but should fit best in this category
- AppleMCEReporterDisabler
- CryptexFixup
- Whatever this is https://github.com/benbaker76/HWPEnable
- telemetrap
- VoodooTSCSync
- MouSSE https://forums.macrumors.com/threads/mp3-1-others-sse-4-2-emulation-to-enable-amd-metal-driver.2206682/

## Intel
- CPUTopologyRebuild
- CPUTscSync
- CPUFriend

## AMD
- Seey6's CPUTSCSync
- 

# USB
- USBMap
- USBToolBox
- USBInjectAll
- GUX
- RyzenGUX
- XLNCUSBFIX
- XHCIunsupported
- USB3 legacy? https://applelife.ru/threads/nastrojka-usb-v-10-11-i-novee.627190/page-3#post-537459

# Audio

## AppleALC

## VoodooHDA


# Networking kexts
Using your computer without internet will be difficult. Unfortunately, MacOS is sometimes very picky when it comes to internet and especially WiFi.

## Ethernet
Unfortunately, macOS hardly supports any Ethernet controller, apart from some [Aquantia controllers](https://www.insanelymac.com/forum/topic/330614-marvell-aquantia-10-gb-ethernet-support-thread/){:target="_blank"}. Fortunately, various kexts have been written in the community. Make sure to read the ReadMe to make sure that your controller is actually supported.

{: .note }
The documentation for Ethernet extensions is old, scattered and sometimes very confusing. Therefore, without owning test equipment, it is not really possible to say from which version and up to which controllers are supported. If you find out something, feel free to let us know.
If you have a really rare internet controller that is not listed here and is not considered completely unsupported, feel free to descend the [rabbithole on Insanelymac](https://www.insanelymac.com/forum/files/category/5-lan-and-wireless/?sortby=file_name&sortdirection=asc){:target="_blank"}.

* ### [AppleIGB](https://github.com/Shaneee/AppleIGB){:target="_blank"}
Adds support for some Intel controllers commonly found on AMD mainboards. Unfortunately [known for its instability](https://github.com/Shaneee/AppleIGB?tab=readme-ov-file#known-current-issues). If you end up having issues, it's recommended to use a [custom fork of IntelMausi](https://github.com/mbarbierato/IntelMausi/tree/Intgegration).

* ### [AppleRTL8169Ethernet](https://www.insanelymac.com/forum/files/file/370-applertl8169ethernetkext/){:target="_blank"}
Adds support for old controllers (RTL8101E, RTL8131E, RTL8168, RTL8169/RTL8110) that were dropped with an update for [IONetworkingFamily](https://github.com/koush/IONetworkingFamily.kext) in OS X 10.6 Snow Leopard.

* ### [AtherosE2200Ethernet](https://github.com/Mieze/AtherosE2200Ethernet){:target="_blank"}
Adds support for Qualcomm Atheros Killer E2200 controllers.

* ### [AtherosL1cEthernet](https://github.com/al3xtjames/AtherosL1cEthernet){:target="_blank"}
Adds support for Qualcomm Atheros AR813x/815x controllers.


* ### [BCM5722D](https://github.com/chris1111/BCM5722D){:target="_blank"}
Adds support for Broadcom BCM5722 NetXtreme and NetLink family controllers.


* ### [IntelMausi](https://github.com/acidanthera/IntelMausi){:target="_blank"}
Derived from [IntelMausiEthernet](https://github.com/Mieze/IntelMausiEthernet), this kext adds support for a large amount of Intel Ethernet controllers. Take a look at the ReadMe to see if your controller is included. IntelMausi comes bundled with IntelSnowMausi, which provides support for older OS X versions.
IntelMausi supports OS X 10.9 Mavericks to macOS 15 Sequoia, while IntelSnowMausi supports OS X 10.6 Snow Leopard to OS X Mountain Lion.

  
* ### [RealtekRTL8100](https://github.com/Mieze/RealtekRTL8100){:target="_blank"}
Adds support for Realtek RTL8100 based controllers.


* ### [RealtekRTL8111](https://github.com/Mieze/RTL8111_driver_for_OS_X){:target="_blank"}
Adds support for RTL8111/8168 based controllers. Make sure to read the documentation if you want to boot older macOS versions.


* ### [LucyRTL8125Ethernet](https://github.com/Mieze/LucyRTL8125Ethernet){:target="_blank"}
A kext specifically designed for Realtek RTL8125 2.5GBit Ethernet controllers.

* ### [AzulNX2Ethernet](https://github.com/Goldfish64/AzulNX2Ethernet){:target="_blank"}
Adds support for (formerly Broadcom) NetXtreme II server-grade network cards.

## WiFi

### Broadcom
- BRCMFixup
- BRCMPatchRAM

### Intel
- OpenIntelWireless

### Qualcom
- ATH9K
- Atheros40 (Mojave+)

## Other networking kexts
Wireless USB BigSur Adapter https://github.com/chris1111/Wireless-USB-Big-Sur-Adapter
Mediatek https://github.com/chris1111/D-LinkUtility-Package
Horndis https://github.com/Edwardwich/HoRNDIS
NullEthernet https://github.com/RehabMan/OS-X-Null-Ethernet

# Storage kexts

## NVMe

### [NVMeFix](https://github.com/acidanthera/NVMeFix){:target="_blank"}
NVMeFix is a set of patches designed to improve the compatibility of non-Apple NVMe SSDs with macOS. It works by modifying the Apple NVMe storage driver, known as IONVMeFamily. 

## SATA

## [CtlnaAHCIPort](https://github.com/dortania/OpenCore-Install-Guide/blob/master/extra-files/CtlnaAHCIPort.kext.zip){:target="_blank"}
Just as Sata-unsupported, this kext adds a variety of SATA controllers. Note that this kext contains needed binaries for some entirely unsupported controllers - if SATA-unsupported does not work on your system, you may want to try this kext.

## [SATA-unsupported](https://github.com/RehabMan/hack-tools/tree/master/kexts/SATA-unsupported.kext){:target="_blank"}
A codeless kext adding a variety of SATA personalities to macOS.

## [RyzenSata](https://github.com/Carnations-Botanica/RyzenSata){:target="_blank"}
Similar to SATA-unsupported, this kext adds SATA personalities to macOS. Corresponding SATA personalities are often found on AMD laptops. If you own an AMD laptop with a SATA interface, you will probably benefit from this kext.

## IDE/ATA
### [AppleIntelPIIXATA](https://github.com/PureDarwin/AppleIntelPIIXATA){:target="_blank"}
Provides IDE/ATA support for controllers dropped in BigSur.

<!--
ATA injector?
-->

## Floppy
Yes, for real. Theres a [floppy kext](https://github.com/Goldfish64/VoodooFloppy){:target="_blank"}. We don't know if the kext works - please let us know if you seriously have a floppy drive.

## Card readers
- Sinetek-rtsx
- VoodooSDHC
- RealtekCardReader
- EmeraldSDHC

# Laptop specific kexts
## Sensor Data
- SMCBatteryManager
- ECEnabler
- CrosEC
- YogaSMC
- SMCDellSensors
- AsusSMC

## Input

<!-- In progress -->

### PS2:
Acidanthera's VoodooPS2 - 10.10+
 - Elans
 - Alps
 - Synaptics
 - SentelicFSP
Rehabman VoodooPS2 - Older versions of macOS
 - Synaptics
VoodooPS2 Alps - Older versions of macOS
 - Alps

### SMBus:
VoodooSMBus - 10.14+ (Note that I am working on a new thingy for this)
 - Elans
VoodooRMI - 10.10+
 - Synaptics
 - Comes with it's own version of VoodooSMBus that supports 10.10+

### I2C:
VoodooI2C - 10.11+ with anyone of the following satellites
 - Precision/HID Multitouch: VoodooI2CHID
 - Synaptics: VoodooRMI
 - Alps: AlpsHID
 - Elan: VoodooI2CElan
 - AtmelMXT Touchpads: VoodooI2CAtmelMXT
 - FTE: VoodooI2CFTE

# Misc
- MacHyperVSupport.kext
- FeatureUnlock
- DebugEnhancer

<h2 align="center">
  <br>
  <div>
    <a class="top-button" href="#">&uarr; Go to the Top &uarr;</a>
  </div>
  <br>
</h2>
