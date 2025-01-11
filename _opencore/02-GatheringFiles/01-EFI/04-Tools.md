---
layout: default
title: Tools
parent: EFI Setup
grand_parent: Gathering Files
description: 
nav_order: 4
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
  <img width="650" height="200" src="../../../../assets/Headers/Header-OpenCore-Tools.png">
</p>

<h2 align="center">These add functionality to OpenCore.</h2>
<br>

For our purposes of building a minimal and initial EFI, you can delete all included Tools. You may only ever need to add ``OpenShell.efi`` if a Helper, requests you to provide additional information about the system, that can be retrieved from OpenShell.

**The rest of this page documents all known Tools and their purpose for safe keeping.**

<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../03-Kexts/">&larr; Back Page</a>
    <a class="nav-button" href="../05-Resources/">Next Page &rarr;</a>
  </div>
  <br>
</h2>

| Tool | Purpose | Requirement |
| BootKicker.efi | Display Apple BootPicker menu (for Macs with compatible firmware). | <span style="color: #ff4d4f;">No</span> |
| ChipTune.efi | Test BeepGen protocol and generate audio signals of different style and length. | <span style="color: #ff4d4f;">No</span> |
| CleanNvram.efi | Reset NVRAM alternative bundled as a standalone tool. | <span style="color: #ff4d4f;">No</span> |
| ControlMsrE2.efi | Check CFG Lock (MSR 0xE2 write protection) consistency across all cores and change such hidden options on selected platforms. | <span style="color: #ff4d4f;">No</span> |
| CsrUtil.efi | Simple implementation of SIP-related features of Apple csrutil. | <span style="color: #ff4d4f;">No</span> |
| FontTester.efi | Render the console font pages which the Builtin renderer provides. | <span style="color: #ff4d4f;">No</span> |
| GopStop.efi | Test GraphicsOutput protocol with a simple [scenario](https://github.com/acidanthera/OpenCorePkg/tree/master/Application/GopStop). | <span style="color: #ff4d4f;">No</span> |
| KeyTester.efi | Test keyboard input in SimpleText mode. | <span style="color: #ff4d4f;">No</span> |
| ListPartitions.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| MmapDump.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| OpenControl.efi | Unlock and lock back NVRAM protection for other tools to be able to get full NVRAM access when launching from OpenCore. | <span style="color: #ff4d4f;">No</span> |
| OpenShell.efi | UEFI Shell, added to the boot picker. | <span style="color: #ffab52;">Conditional</span> |
| ResetSystem.efi | Utility to perform system reset. Takes reset type as an argument: coldreset, firmware, shutdown, warmreset.<br>Defaults to coldreset. | <span style="color: #ff4d4f;">No</span> |
| RtcRw.efi | Utility to read and write RTC (CMOS) memory. | <span style="color: #ff4d4f;">No</span> |
| TpmInfo.efi | Check Intel PTT (Platform Trust Technology) capability on the platform, which allows using fTPM 2.0 if enabled.<br>The tool does not check whether fTPM 2.0 is actually enabled. | <span style="color: #ff4d4f;">No</span> |

<h2 align="center">
  <br>
  <div>
    <a class="top-button" href="#">&uarr; Go to the Top &uarr;</a>
  </div>
  <br>
</h2>
