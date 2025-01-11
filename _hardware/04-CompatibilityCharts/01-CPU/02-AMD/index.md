---
layout: default
title: AMD
parent: CPU Support Chart
grand_parent: Compatibility Charts
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

  .toc-button {
    margin: 10px;
    align: center;
  }

  .top-button {
    margin: 10px;
    align: center;
  }

  .bottom-button {
    margin: 10px;
    align: center;
  }
</style>

<p align="center">
  <img width="650" height="200" src="../../../../../assets/Headers/Header-AMDBased.png">
</p>

{: .internalnote }
We need to pick through and remove non viable CPUs that would not make a working system combination, for example, there are some Laptop CPUs that do not make sense to have on this list, as the iGPU is not supported, thus they would not be able to technically use OS X / macOS in any reasonable way.

{: .internalnote }
Still missing older than Ryzen data such as Bulldozer, Jaguar, and Puma 

{: .note }
> No Mac computer has ever shipped with an AMD CPU. Many programs use libraries or CPU features that AMD CPUs cannot handle. Programs affected include, but are not limited to: Discord Krisp, Adobe CC applications, Corel Painter, and others. Carnations Botanica has a Kernel Extension to resolve such issues via <a href="https://github.com/Carnations-Botanica/IntelMKLFixup/">IntelMKLFixup</a> by <a href="https://github.com/whatdahopper">Kaitlyn</a>
>
> AMD CPUs utilize SVM (Secure Virtual Machine), while Intel CPUs utilize VT-x (Virtualization Extensions) for programs like Docker, Virtualbox, VMware, Parallels, UTM, QEMU, and others. This means you will not have the ability to virtualize on your AMD-based Hac. This is currently an open issue. Possible workarounds are using older versions of software that utilize their own Hypervisor and not Apple HV / Hypervisor.framework, but this is unsafe.
>
> The XNU Kernel will not boot OOB with an AMD CPU. In addition to standard configuration of OpenCore, there are various Kernel Patches to add for the successful booting of XNU and therefore OS X / macOS on AMD CPUs. This preserves the "Vanilla" aspect of OS X / macOS by applying kernel patches on the fly, instead of using a custom built kernel in a "Distro", which are no longer supported in favor of OpenCore's ability to patch the kernel. These patches can be found <a href="https://github.com/AMD-OSX/AMD_Vanilla">here</a> by <a href="https://github.com/Shaneee">Shaneee</a> as <b>AMD Vanilla Patches</b>.

<br>

<h2 align="center">Quick Navigation</h2>

<h2 align="center">
  <br>
  <div>
    <a class="toc-button" href="#desktop">&darr; Go to Desktop CPUs &darr;</a>
    <a class="toc-button" href="#laptop">&darr; Go to Laptop CPUs &darr;</a>
    <br>
    <br>
    <a class="bottom-button" href="#-">&darr; Go to Bottom &darr;</a>
  </div>
  <br>
</h2>

# Desktop

## Ryzen 9000 series (Granite Ridge)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 9950X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 9900X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 9800X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 9700X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 9600X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 8000 series (Phoenix)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 8700G | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8700F | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8600G | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8500G | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8400F | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8300G | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 7000 series (Raphael)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 7950X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7950X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7900X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7900X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7900 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 7945 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7800X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7700X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7700 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 7745 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7600X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7600X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7600 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 7645 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7500F | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 5000 series (Vermeer, Cezanne)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 5950X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5900XT | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5900X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5900 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 5945 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 5845 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5800X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5800XT | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5800X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5800 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5700X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5700X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5700 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5700G | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 5700GE | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| PRO 5645 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600X3D | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600G | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 5600GT | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600GE | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 5500 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5500GT | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5300G | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 5300GE | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 5100 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 4000 series (Renoir)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 4800S | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4700G | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 4700GE | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 4700S | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4600G | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 4600GE | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 4500 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4300G | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 4300GE | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 4100 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Athlon 300 series (Picasso)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| PRO 300GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| 320GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| 3000G | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| Gold PRO 3150GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| Gold 3150GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| Gold PRO 3150G | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| Gold 3150G | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |

## Ryzen 3000 series (Picasso, Matisse)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 3950X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3900XT | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3900X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3900 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3800XT | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3800X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3700X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3600XT | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3600X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3600 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3500X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3500 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 3400G | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3400G | High Sierra (10.13) | Sequoia (15) | Vega 11, Experimental iGPU Acceleration |
| 3400GE | High Sierra (10.13) | Sequoia (15) | Vega 11, Experimental iGPU Acceleration |
| PRO 3400GE | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 3350G | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 3350GE | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3300X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 3200G | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3200G | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 3200GE | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| PRO 3200GE | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 2000 series (Raven Ridge, Pinnacle Ridge)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 2700X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2700E | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2700 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2600E | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2600 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2500X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2400G | High Sierra (10.13) | Sequoia (15) | Vega 11, Experimental iGPU Acceleration |
| 2400GE | High Sierra (10.13) | Sequoia (15) | Vega 11, Experimental iGPU Acceleration |
| 2300X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2200G | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 2200GE | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| PRO 2100GE | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Athlon 200 series (Raven Ridge)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| PRO 200GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| 200GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| 220GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| 240GE | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |

## Ryzen 1000 series (Summit Ridge)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 1800X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 1700X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1700X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 1700 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1700 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1600X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 1600 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1600 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1500X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 1500 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1400 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1300X | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 1300 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| PRO 1200 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 1200 | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

<h2 align="center">
  <br>
  <div>
    <a class="top-button" href="#">&uarr; Go to Top &uarr;</a>
    <a class="bottom-button" href="#-">&darr; Go to Bottom &darr;</a>
  </div>
  <br>
</h2>

# Laptop

## Ryzen 8000 series (Hawk Point)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 8945HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8845HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8840HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8840U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8645HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8640HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8640U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8540U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 8440U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Athlon 7000 series (Mendocino)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| Silver 7120C | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| Silver 7120U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| Gold 7220C | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| Gold 7220U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 7000 series (Mendocino, Barcelo-R, Rembrandt-R, Phoenix, Dragon Range)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 7940HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7940H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7840HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7840H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7840U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7736U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7735HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7735H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7735U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7730U | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 7640HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7640H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7640U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7545U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7540U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7535HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7535H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7535U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7530U | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 7520U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7440U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7435HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7435H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7335U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7330U | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 7320U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7235HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 7235H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 6000 series (Rembrandt)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 6980HX | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6980HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6900HX | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6900HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6800H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6800HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6800U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6600H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6600HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 6600U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 5000 series (Lucienne, Cezanne and Barcelo)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 5980HX | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 5980HS | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 5900HX | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 5900HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5800H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5800HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5825U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5800U | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 5700U | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 5625U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5600U | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 5560U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5500U | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 5500H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5425U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5400U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5300U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 5125C | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Ryzen 4000 series (Renoir)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 4900H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4900HS | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4800H | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 4800HS | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 4980U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4800U | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 4700U | High Sierra (10.13) | Sequoia (15) | Vega 7, Experimental iGPU Acceleration |
| 4600H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4600HS | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 4680U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 4600U | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 4500U | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 4300U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Athlon Mobile 3000 series (Dali)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| PRO 3045B | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |
| Silver 3050C | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |
| Silver 3050e | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |
| Silver 3050U | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |
| PRO 3145B | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |
| Gold 3150C | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |
| Gold 3150U | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |

## Ryzen 3000 series (Dali, Picasso)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 3780U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3750H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3700C | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3700U | High Sierra (10.13) | Sequoia (15) | Vega 10, Experimental iGPU Acceleration |
| 3580U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3550H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3500C | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3500U | High Sierra (10.13) | Sequoia (15) | Vega 8, Experimental iGPU Acceleration |
| 3450U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3350U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3300U | High Sierra (10.13) | Sequoia (15) | Vega 6, Experimental iGPU Acceleration |
| 3250U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3250C | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 3200U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Athlon Mobile 200/300 series (Raven Ridge, Picasso)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 200U | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |
| 300U | High Sierra (10.13) | Sequoia (15) | Vega 3, Experimental iGPU Acceleration |

## Ryzen 2000 series (Raven Ridge)

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 2800H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2700U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2600H | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2500U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2300U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |
| 2200U | High Sierra (10.13) | Sequoia (15) | Requires a dGPU |

## Un-named AMD Zen-based APUs

| Name | Initial Support | Latest Support | Notes |
| --- | --- | --- | --- |
| 3020e | High Sierra (10.13) | Sequoia (15) | Experimental iGPU Acceleration |

<br>
<a id="-"></a>
<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../../../01-CPU/index">&larr; Back Page</a>
    <a class="nav-button" href="../../../02-GPU/index">Next Page &rarr;</a>
  </div>
  <br>
</h2>
