---
layout: default
title: Miscellaneous Hardware
parent: Compatibility Charts
nav_order: 5
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
</style>

<p align="center">
  <img width="650" height="200" src="../../../../assets/Headers/Header-MiscSupportChart.png">
</p>

<h2 align="center">An info dump of obscure hardware support</h2>
<br>

<p align="center">This section includes hardware that doesn't fall into any of the previous categories.</p>

# Fingerprint Sensors

- Fingerprint sensors won't work with Hackintosh. This is because macOS requires a T1 or T2 security chip to enable fingerprint readers. Unless a method to emulate these chips is developed, fingerprint readers will remain unsupported.

# Windows Hello Face Recognition (FaceID)

- WFHR/FaceID won't work in macOS. There is chance that you could get your camera working, but that's it.

# CD-DVD ROM

- Nearly any SATA optical drive will work, though you may need to use a specific SMBIOS.

# Peripherals

- Peripherals working on macOS depend heavily on driver support. While the majority of USB peripherals are supported thanks to IOUSBHost stack, which includes HID device support (like your keyboard, mice, etc.), the same can't be said for specialized hardware.
Devices like RGB controllers, fingerprint sensors, or certain audio interfaces may not function without macOS-specific drivers.

<p align="center">You can continue below using the Nav Bar.</p>

<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../../04-Networking/index">&larr; Back Page</a>
    <a class="nav-button" href="../../../../opencore/01-Introduction">Next Page &rarr;</a>
  </div>
  <br>
</h2>
