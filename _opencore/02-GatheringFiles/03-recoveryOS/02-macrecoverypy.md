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
Screenshots from here will be changed to include Windows host, so it would be easier for users.

<h2 align="center">Fetching recoveryOS files</h2>

You can use a macrecovery.py tool to fetch files for recoveryOS directly from Apple's servers. These files can be used to install macOS using the online method.

# Get macrecovery.py
``macrecovery.py`` is actually bundled with ``OpenCorePkg`` that you've downloaded earlier.

<p align="center">
  <img width="1275" height="1236" src="/assets/macrecovery/MacRecoveryFS-W.png">
</p>

# Get recoveryOS

You can fetch recoveryOS for the desired macOS version by running one of the following commands:

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

This is what your Terminal should look like after fetching: 

<p align="center">
  <img width="1275" height="1236" src="/assets/macrecovery/MacRecoveryCMD-W.png">
</p>

``macrecovery.py`` will get you the latest available update for specified macOS version. recoveryOS will be placed in `com.apple.recovery.boot` folder.
Once the recoveryOS is fetched, the output will be similar to this: 

<p align="center">
  <img width="1275" height="1236" src="/assets/macrecovery/MacRecoveryOS-W.png">
</p>

# Preparing your USB

After fetching recoveryOS, you should move your ``com.apple.recovery.boot`` folder to the root of your USB.

<p align="center">
  <img width="1275" height="1236" src="/assets/macrecovery/MacRecoveryUSB-W.png">
</p>


<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../index">&larr; Back Page</a>
    <a class="nav-button" href="../../../03-EFISanityCheck/">Next Page &rarr;</a>
  </div>
  <br>
</h2>
