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

{: .internalnote }
Whoever is knowledgable on Wi-Fi, please explain the consequences of using specific third party kexts, and what you can and cannot do, I want to include information like one-way AirDrop, no working AirPlay, and other handoff features that will not work due to the usage of a specific kext or hardware that simply does not support the feature.

<p align="center">Placeholder Text.</p>

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
