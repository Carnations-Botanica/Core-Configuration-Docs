---
layout: default
title: AMD
parent: Platform Specific Files
grand_parent: Gathering Files
description: Placeholder
nav_order: 2
has_children: true
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
  <img width="650" height="200" src="../../../../assets/Headers/Header-Vendor-AMD.png">
</p>


<h2 align="center">Known AMD specific Files.</h2>
<br>

{: .warning }
This sections is currently a work in progress, and information here may be incorrect.

# ACPI

| SSDT Name | Notes |
| SSDT-PLUG-ALT | Generally needed on B550 and A520 motherboards |
| SSDT-EC | Needed on those systems with the afor mentioned `PNP0C09` devices (if you don't know if you do, you likely need this) |
| SSDT-USBX | Generally needed on AMD |

# Drivers

| Driver Name | Notes |
| placeholder | placeholder |
| placeholder | placeholder |
| placeholder | placeholder |
| placeholder | placeholder |

# Kexts

| Kext Name | Notes |
| AppleMCEReporterDisabler | Only use on Monterey (12) beta 6 and newer, beta 3 this is also required |
| GUX-RyzenXHCIFix/GenericUSBXHCI | Generally required on Ryzen Laptops with a 4xxx series or later |
| USBMap/UTBMap and USBToolBox | Rarely can cause stalls booting. Recommended to use the `Native Classes` option in USBToolBox to get a USBMap that doesn't require USBToolBox.kext. |

# Tools

| Tool Name | Notes |
| placeholder | placeholder |
| placeholder | placeholder |
| placeholder | placeholder |
| placeholder | placeholder |

<br>
<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../index">&larr; Back Page</a>
    <a class="nav-button" href="../../03-recoveryOS/index">Next Page &rarr;</a>
  </div>
  <br>
</h2>
