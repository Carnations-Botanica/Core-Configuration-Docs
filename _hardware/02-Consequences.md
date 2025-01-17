---
layout: default
title: Consequences of Unsupported Hardware
description: Placeholder
nav_order: 2
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
</style>

<p align="center">
  <img width="650" height="200" src="../../assets/Headers/Header-ConsequencesOfUHW.png">
</p>

<h2 align="center">What running non-compatible hardware entails.</h2>
<br>

<h2 align="center">Graphics Related</h2>
<br>
<div align="center">
<a href=""><img src="../../assets/Carnations/HighSierraNoGPUAccel.gif" alt=""></a>
</div>
<p align="center">The most important and absolutely required aspect is a supported Graphics Processing Unit. When you run the Mac operating system without a properly supported graphics card, you are running the entire OS in VESA / VGA mode. This means you have 0 graphics acceleration, it is being done via CPU rendering, which as you can see above, is a non usable experience. Imagine if your Windows PC did not have a graphics card, that's basically what it is to OS X / macOS. If your GPU/iGPU is not in the support chart, you will basically be using the system as if no Graphics Processing Unit exists at all. The Mac operating system heavily relies on a GPU to properly use, because every Mac has always <i>had</i> a GPU that worked (iGPU), and makes heavy use of it for things like Drop Shadows, Gaussian Blur, Dock Transparency, Minimizing/Maximizing animations, and other Aqua effects. The experience is much worse than non accelerated Windows, and is considered to be unusable in this state.</p>

<p align="center">Speaking of Graphics Acceleration and its importance, this is actually why VirtualBox and VMware are not supported platforms for hosting OS X / macOS guests. With the requirement of a GPU, means the requirement of a Type 1 Hypervisor that can do GPU passthrough, which is essentially giving a real GPU to the Virtual Machine, this can only be done with platforms like Hyper-V and KVM on Linux hosts. <b>The above GIF is of a non accelerated Virtual Machine.</b></p>

<h2 align="center">Wi-Fi Related</h2>
<br>

<p align="center">Apple implements various features for seamless integration across devices (Continuity) in the Apple ecosystem; These features include but are not limted to:</p>

| Feature | Description | Min OS X Requirement |
| --- | --- | --- |
| AirDrop | Share and receive photos, documents, and more with other Apple devices that are nearby. | Mac OS X Lion (10.7+) |
| AirPlay | Stream your music, videos, photos, podcasts, and games from many Apple devices to speakers in multiple rooms or to your TV. | Mac OS X Snow Leopard (10.6+) |
| AirPrint | Allows users to print from Apple devices to AirPrint-enabled printers without installing drivers or connecting cables. | Mac OS X Lion (10.7+) |
| Continuity Camera | Use iPhone as a webcam for Mac | macOS Ventura (13+) |
| HomeKit | Platform developed by Apple that lets users configure, communicate with and control smart appliances using Apple devices. |  macOS Mojave (10.14+) |
| HandOff | With Handoff, you can start work on one device, then switch to another nearby device and pick up where you left off. | Mac OS X Yosemite (10.10+) |
| Instant Hotspot | Connect to the Personal Hotspot on your iPhone or iPad (Wi-Fi + Cellular) from your Mac, iPad, or another iPhone, without entering a password. | Mac OS X Yosemite (10.10+) |
| Universal Control | Use the keyboard, mouse, or trackpad of your Mac to control up to two other nearby Mac or iPad devices, and work seamlessly between them. | macOS Monterey (12.3+) |

<p align="center">OS X / macOS only supports a few specified Broadcom Wireless cards, and each version of OS X / macOS has different lists of supported cards.</p>
<p align="center">There is third-party support for Intel Wireless cards with <a href="https://github.com/OpenIntelWireless/itlwm">itlwm</a> which implements some capabilities up to Ventura (macOS 13) but Sonoma or Sequoia are not supported for continuity.</p>
<p align="center">It is common for most, if not all users to never really have continuity features working as it relies on a supported Bluetooth chipset as well.</p>

<h2 align="center">Bluetooth Related</h2>
<br>

{: .internalnote }
Same thing here, whoever is knowledgable on Bluetooth, and its various limitations or consequences of using things like USB dongles as opposed to PCIe or socketed chipsets and whatnot, I don't have any of this hardware so, nothing to write on my end, please delete both of these notes when committing text.

<p align="center">Placeholder Text.</p>

<h2 align="center">Storage Related</h2>
<br>

{: .internalnote }
For this, I wanted to note things like TRIM support, and example drives that would require NVMeFix or similar to EmeraldSDHC, pretty much cover basis of the types of storage and their range of support from OS X / macOS, don't have too much EXP on this either.

<p align="center">Placeholder Text.</p>

<br>
<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../01-Importance">&larr; Back Page</a>
    <a class="nav-button" href="../03-KnowYourHardware/index">Next Page &rarr;</a>
  </div>
  <br>
</h2>
