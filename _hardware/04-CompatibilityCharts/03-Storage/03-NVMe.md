---
layout: default
title: NVMes
parent: Storage Support Chart
grand_parent: Compatibility Charts
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
</style>

<p align="center">
  <img width="650" height="200" src="../../../../assets/Headers/Header-Storage-NVMe.png">
</p>
<br>

{: .important }
NVMe storage devices can sometimes require additional patches or kexts for full functionality, particularly when it comes to ensuring proper support for TRIM and enabling the drive to be recognized correctly by macOS.

{: .warning}
Many NVMe drives will require [NVMeFix.kext](https://github.com/acidanthera/NVMeFix) to function properly.

# Recommended NVMes

| Drive Name | Notes |
| WD_BLACK SN750 | One of the best choices |
| Western Digital SN700 | One of the best choices |
| WD_BLACK SN850/SN850X| One of the best choices |

# Samsung

{: .important }
Many Samsung NVMe drives are known to cause issues, so it's best to avoid using them if possible. If you already have an Samsung NVMe, it's best to use it as an storage-only drive. You shouldn't install macOS on it.

| Drive Name | Notes |
| Samsung 950 Pro | Should be used as an storage-only NVMe |
| Samsung 960 Evo/Pro | Should be used as an storage-only NVMe |
| Samsung 970 Evo/Pro | Samsung released an firmware update that should make this NVMe work with macOS |
| Samsung 980 Pro | Should be used as an storage-only NVMe |

# Western Digital

{: .important }
The situation is quite different with WD drives — almost anything from WD will work.

| Drive Name | Notes |
| WD Blue SN550 | Should work without any problems |
| WD Black SN700 | Should work without any problems |
| WD Black SN720 | Should work without any problems |
| WD Black SN750 | Should work without any problems |
| WD Black SN850 | Should work without any problems |

# Kingston

| Drive Name | Notes |
| Kingston NV1 | May require [NVMeFix.kext](https://github.com/acidanthera/NVMeFix) to function properly | 
| Kingston NV2 | May require [NVMeFix.kext](https://github.com/acidanthera/NVMeFix) to function properly | 

# Crucial

| Drive Name | Notes |
| Crucial P1 | Working fine with TRIM enabled |
| Crucial P2 | May require [NVMeFix.kext](https://github.com/acidanthera/NVMeFix) to function properly | 

# Intel

| Drive Name | Notes |
| Intel 660p | Working fine with TRIM enabled |
| Intel 760p | Working fine with TRIM enabled |

# ADATA

| Drive Name | Notes |
| ADATA XPG SX8200 |

# HP

| Drive Name | Notes |
| HP EX920 |  

# Other

| Drive Name | Notes |
| KingDian S280 | Working fine with TRIM enabled |
| Kingchuxing | Working fine with TRIM enabled |

# Unsupported NVMes

| Drive Name | Notes |
| SKHynix P31 | Incompatible |
| Samsung PM9xx | These NVMe drives are often found in OEM devices, those will not work |
| Micron 2200V | Incompatible |
| Phison E12 (controller) | These controllers are known to have problems, avoid if possible |

<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../index">&larr; Back Page</a>
    <a class="nav-button" href="../../04-Networking/index">Next Page &rarr;</a>
  </div>
  <br>
</h2>