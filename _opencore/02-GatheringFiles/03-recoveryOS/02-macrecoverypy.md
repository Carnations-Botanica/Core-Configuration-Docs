---
layout: default
title: Using macrecovery
parent: Fetching recoveryOS
grand_parent: Gathering Files
description: Placeholder
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
</style>

<p align="center">
  <img width="650" height="200" src="../../../../../assets/Headers/Header-Placeholder.png">
</p>

{: .internalnote }
This page still requires the macrecovery img on the top


You can use macrecovery.py to fetch files for recoveryOS, which can be used to install macOS using the online method. This script allows you to download the necessary files from Apple's servers for creating a bootable macOS installation.

## Get macrecovery.py

macrecovery.py is actually included in the OpenCorePkg that you’ve already downloaded.

<p align="center">
  <img width="1275" height="1236" src="/assets/macrecovery/MacRecFolderStructure.png">
</p>

## Get recoveryOS

You can download the recoveryOS for the desired macOS version by running one of the following commands:

| macOS Version | Command | 
| --- | --- |
| Lion (10.7) | python3 ./macrecovery.py -b Mac-2E6FAB96566FE58C -m 00000000000F25Y00 download |
| Mountain Lion (10.8) | python3 ./macrecovery.py -b Mac-7DF2A3B5E5D671ED -m 00000000000F65100 download |
| Mavericks (10.9) | python3 ./macrecovery.py -b Mac-F60DEB81FF30ACF6 -m 00000000000FNN100 download |
| Yosemite (10.10) | python3 ./macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000GDVW00 download |
| El Capitan (10.11) | python3 ./macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000GQRX00 download |
| Sierra (10.12) | python3 ./macrecovery.py -b Mac-77F17D7DA9285301 -m 00000000000J0DX00 download |
| High Sierra (10.13) | python3 ./macrecovery.py -b Mac-7BA5B2D9E42DDD94 -m 00000000000J80300 download |
| Mojave (10.14) | python3 ./macrecovery.py -b Mac-7BA5B2DFE22DDD8C -m 00000000000KXPG00 download |
| Catalina (10.15) | python3 ./macrecovery.py -b Mac-00BE6ED71E35EB86 -m 00000000000000000 download |
| Big Sur (11) | python3 ./macrecovery.py -b Mac-42FD25EABCABB274 -m 00000000000000000 download |
| Monterey (12) | python3 ./macrecovery.py -b Mac-FFE5EF870D7BA81A -m 00000000000000000 download |
| Ventura (13) | python3 ./macrecovery.py -b Mac-4B682C642B45593E -m 00000000000000000 download |
| Sonoma (14) | python3 ./macrecovery.py -b Mac-226CB3C6A851A671 -m 00000000000000000 download |
| **Sequoia (15)** | python3 ./macrecovery.py -b Mac-937A206F2EE63C01 -m 00000000000000000 download |

macrecovery.py will get you the latest available update for specified macOS version.
Once this is done, you should get the output similar to this: 
<p align="center">
  <img width="1275" height="1236" src="/assets/macrecovery/MacRecDownloaded.png">
</p>

{: .internalnote }
I need the photo for formatting options here, may add it later

## Format your USB

Once you fetch the files using macrecovery, you need to format your USB as FAT32 (MS-DOS (FAT)) with GUID Scheme.

After you format your USB, you should move your `com.apple.recovery.boot` file to the root of your USB.
<p align="center">
  <img width="1275" height="1236" src="/assets/macrecovery/MacRecFolder.png">
</p>


<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../index">&larr; Back Page</a>
    <a class="nav-button" href="../../../03-EFISanityCheck/">Next Page &rarr;</a>
  </div>
  <br>
</h2>
