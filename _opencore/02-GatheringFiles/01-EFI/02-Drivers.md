---
layout: default
title: Drivers
parent: EFI Setup
grand_parent: Gathering Files
description: 
nav_order: 2
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
  <img width="650" height="200" src="../../../../assets/Headers/Header-OpenCore-Drivers.png">
</p>

<h2 align="center">What's required, what's not?</h2>
<br>

Well, for our initial purpose of creating a minimal EFI that we can then build upon, you'll find you truly only need the following:

- OpenRuntime.efi
- OpenHfsPlus.efi
- OpenPartitionDxe.efi

But, you only need ``OpenPartitionDxe.efi`` if you are booting the recovery environment of Mac OS X 10.7 through 10.9

You can also replace ``OpenHfsPlus.efi`` with the proprietary HFS+ Driver from Apple. It is simply not bundled with OpenCorePkg for obvious reasons. You can find [HfsPlus.efi](https://github.com/acidanthera/OcBinaryData/raw/refs/heads/master/Drivers/HfsPlus.efi) on Github via the [OcBinaryData](https://github.com/acidanthera/OcBinaryData/tree/master/Drivers) Drivers folder within a repository by [Acidanthera](https://github.com/acidanthera).

``OpenRuntime.efi`` is not optional. It is required for proper OpenCore injection.

**The rest of this page documents all known Drivers and their purpose for safe keeping.**

<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../01-ACPI/index">&larr; Back Page</a>
    <a class="nav-button" href="../03-Kexts/">Next Page &rarr;</a>
  </div>
  <br>
</h2>

<br>

<h2 align="center">Drivers provided in OpenCorePkg</h2>
<br>

| Driver | Purpose | Requirement |
| ArpDxe.efi | Networking protocol driver | <span style="color: #ff4d4f;">No</span> |
| AudioDxe.efi | Setting up a boot chime | <span style="color: #ff4d4f;">No</span> |
| BiosVideo.efi | Basic video driver for Pre-UEFI systems.<br>This driver does not give you acceleration in macOS! | <span style="color: #ff4d4f;">No</span> |
| CrScreenshotDxe.efi | Tool to take Screenshots | <span style="color: #ff4d4f;">No</span> |
| Dhcp4Dxe.efi | Networking protocol driver | <span style="color: #ff4d4f;">No</span> |
| DnsDxe.efi | Networking protocol driver | <span style="color: #ff4d4f;">No</span> |
| DpcDxe.efi | Networking protocol driver | <span style="color: #ff4d4f;">No</span> |
| Ext4Dxe.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| FirmwareSettingsEntry.efi | Used to boot UEFI Settings, adds boot entry. | <span style="color: #ff4d4f;">No</span> |
| HiiDatabase.efi | Used to fix graphic issues on Pre-UEFI systems | <span style="color: #ff4d4f;">No</span> |
| HttpBootDxe.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| HttpDxe.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| HttpUtilitiesDxe.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| Ip4Dxe.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| MnpDxe.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| NvmExpressDxe.efi | Unknown Purpose | <span style="color: #ff4d4f;">No</span> |
| OpenCanopy.efi | GUI for OpenCore UI<br>Do not add this for initial installation.<br>Requires further manual setup. | <span style="color: #ff4d4f;">No</span> |
| OpenHfsPlus.efi | Open source HFS+ driver for macOS<br>Don't use on systems that lack RDRAND support.<br>slower than HFS+ from Apple | <span style="color: #ffab52;">Conditional</span> |
| OpenLegacyBoot.efi | Used to boot legacy OS from Pre-UEFI systems | <span style="color: #ff4d4f;">No</span> |
| OpenLinuxBoot.efi | Used to allow dual-booting Linux through OpenCore<br>Do not add this for initial installation. | <span style="color: #ff4d4f;">No</span> |
| OpenNtfsDxe.efi | Driver to read NTFS drives<br> | <span style="color: #ff4d4f;">No</span> |
| OpenPartitionDxe.efi | Required to boot recovery on OS X 10.7 through 10.9.<br>Not required for OS X Yosemite (10.10) and newer. | <span style="color: #ffab52;">Conditional</span> |
| OpenRuntime.efi | Replacement for [AptioMemoryFix.efi](https://github.com/acidanthera/AptioFixPkg)<br>An extension for OpenCore to help with patching boot.efi for NVRAM fixes and better memory management. | <span style="color: #8ffc74;">Yes</span> |
| OpenUsbKbDxe.efi | Used for OpenCore picker on legacy systems running DuetPkg. | <span style="color: #ff4d4f;">No</span> |
| OpenVariableRuntimeDxe.efi | The emulated NVRAM driver. | <span style="color: #ff4d4f;">No</span> |
| Ps2KeyboardDxe.efi | PS2 Driver for Keyboard Devices. | <span style="color: #ff4d4f;">No</span> |
| Ps2MouseDxe.efi | PS2 Driver for Mouse Devices. | <span style="color: #ff4d4f;">No</span> |
| ResetNvramEntry.efi | Adds boot entry to reset NVRAM.<br>Be careful, make sure you can safely do this.<br>On some hardware, NVRAM variables are used to boot. | <span style="color: #ff4d4f;">No</span> |
| SnpDxe.efi | Implementation of driver entry point and driver binding protocol. | <span style="color: #ff4d4f;">No</span> |
| TcpDxe.efi | TCPv4 I/O and TCPv6 I/O services | <span style="color: #ff4d4f;">No</span> |
| ToggleSipEntry.efi | OpenCore plugin implementing OC_BOOT_ENTRY_PROTOCOL to add a configurable Toggle SIP entry to the boot picker menu. | <span style="color: #ff4d4f;">No</span> |
| Udp4Dxe.efi | produces EFI UDP(User Datagram Protocol) Protocol upon EFI IPv4 Protocol, to provide basic UDPv4 I/O services | <span style="color: #ff4d4f;">No</span> |
| UsbMouseDxe.efi | Used for enabling USB mouse on GUI interface provided by OpenCanopy.<br>Don't add this for initial installation. | <span style="color: #ff4d4f;">No</span> |
| XhciDxe.efi | Responsible for managing the behavior of XHCI controller.<br>Don't add this unless your machine doesn't support UEFI.<br>It is for adding external USB 3 PCI card support. | <span style="color: #ff4d4f;">No</span> |

<h2 align="center">Third-Party Drivers</h2>
<br>

| Driver | Purpose | Requirement |
| [HfsPlus.efi](https://github.com/acidanthera/OcBinaryData/raw/refs/heads/master/Drivers/HfsPlus.efi) | Apple’s proprietary driver for HFS volumes. | <span style="color: #ffab52;">Conditional</span> |
| [HfsPlusLegacy.efi](https://github.com/acidanthera/OcBinaryData/raw/refs/heads/master/Drivers/HfsPlusLegacy.efi) | HFS+ driver for systems that lack RDRAND support. | <span style="color: #ffab52;">Conditional</span> |
| [HfsPlus32.efi](https://github.com/acidanthera/OcBinaryData/raw/refs/heads/master/Drivers/HfsPlus32.efi) | HfsPlus driver for 32-bit CPUs. | <span style="color: #ffab52;">Conditional</span> |
| EnhancedFatDxe.efi | FAT filesystem driver from FatPkg. This driver is embedded in all UEFI firmware and cannot be used from OpenCore. | <span style="color: #ff4d4f;">No</span> |
| [btrfs_x64.efi](https://github.com/acidanthera/OcBinaryData/raw/refs/heads/master/Drivers/btrfs_x64.efi) | BTRFS Driver from rEFInd 0.13.2 | <span style="color: #ff4d4f;">No</span> |
| [ext4_x64.efi](https://github.com/acidanthera/OcBinaryData/raw/refs/heads/master/Drivers/ext4_x64.efi) | EXT4 Driver from rEFInd 0.13.2 | <span style="color: #ff4d4f;">No</span> |
| [EnableGop.efi](https://github.com/acidanthera/OpenCorePkg/tree/master/Staging/EnableGop) | Provides standalone GOP driver for EFI era Mac Pro and iMac. | <span style="color: #ff4d4f;">No</span> |
| [ExFatDxe.efi](https://github.com/acidanthera/OcBinaryData/raw/refs/heads/master/Drivers/ExFatDxe.efi) | Proprietary ExFAT file system driver for Bootcamp support commonly found in Apple firmware. | <span style="color: #ff4d4f;">No</span> |

<h2 align="center">
  <br>
  <div>
    <a class="top-button" href="#">&uarr; Go to the Top &uarr;</a>
  </div>
  <br>
</h2>
