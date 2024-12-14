---
layout: default
title: Using gibMacRecovery
parent: Fetching recoveryOS
grand_parent: Gathering Files
description: Placeholder
nav_order: 1
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
  <img width="650" height="200" src="../../../../../assets/Headers/Header-Tools-gibMacRecovery.png">
</p>

For this tutorial we use a tool called [gibMacRecovery](https://github.com/corpnewt/gibMacRecovery) from [CorpNewt](https://github.com/corpnewt/)'s GitHub. Just as all other tools this is a Python script, so we have to get it first. Either downloading the main branch or cloning the repository as is via CLI.

Just like before, we have different scripts to choose from for different platforms. Again, choose the right one for your OS.

<p align="center">
  <img width="1275" height="1236" src="/assets/gibMacRecovery/gibmacRecoveryRepo.png">
</p>

Once we have started gibMacRecovery, we should see the following menu:

<p align="center">
  <img width="698" height="417" src="/assets/gibMacRecovery/gibmacRecoveryStart.png">
</p>

First, we want to choose option 1) to download the recovery catalog.
Afterwards, we want to choose option 2). Here we can select a macOS version to choose from.

<p align="center">
  <img width="697" height="459" src="/assets/gibMacRecovery/gibmacRecoveryCatalog.png">
</p>

{: .warning }
Its not possible to install OS X 10.4 Tiger to OS X 10.6 Snow Leopard using gibMacRecovery.

We now select the recovery environment for the operating system we want to install. After that, we return to the menu and finally select option 7) to download the recovery.

<p align="center">
  <img width="697" height="459" src="/assets/gibMacRecovery/gibmacRecoveryDownloading.png">
</p>

Once we finished downloading, we can close the program. We should now find a new folder in our Mac Recovery directory. Depending on the target version, the folder contains a large file called ``BaseSystem.dmg`` or ``RecoveryImage.dmg`` and a small associated chunklist.

<p align="center">
  <img width="528" height="340" src="/assets/gibMacRecovery/gibmacRecoveryResults.png">
</p>

We want to place the folder with the containing files in the root directory of our installation media, just next to our ``EFI`` folder. If everything worked, we can continue.

<p align="center">
  <img width="428" height="340" src="/assets/gibMacRecovery/gibmacRecoveryPlaced.png">
</p>

<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../index">&larr; Back Page</a>
    <a class="nav-button" href="../../../03-EFISanityCheck/">Next Page &rarr;</a>
  </div>
  <br>
</h2>