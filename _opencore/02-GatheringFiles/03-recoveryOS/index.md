---
layout: default
title: Fetching recoveryOS
parent: Gathering Files
description: Placeholder
nav_order: 3
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

  .macrecoverypy-next-button-container {
    text-align: right;
  }

  .macrecoverypy-next-button {
    margin: 10px;
  }
</style>

<p align="center">
  <img width="650" height="200" src="../../../../assets/Headers/Header-FetchingrOS.png">
</p>

{: .internalnote }
This page requires an additional update

<h2 align="center">Placeholder Information</h2>

<h4 align="center">This page is a stub temporarily, but this page should:</h4>
<br>

1. Help the user fetch the recoveryOS ``.dmg`` for ``com.apple.recovery.boot``

2. Help the user understand why we are using recoveryOS, and let legacy OS X users who cannot use recoveryOS, how to go about things for that, and essentially have them skip this section.

3. Lightly touch on the two options below for getting recoveryOS, they are practically the same as they're both wrappers of macrecovery from inside of OpenCorePkg

## Why are we using recoveryOS ?
The recoveryOS is a lightweight operating system provided by Apple that helps users repair their macOS installations, recover lost files, or **reinstall macOS**. By using it, we can 'trick' the OS into thinking that macOS was already installed on this PC, allowing us to have it 'reinstall' macOS for us, i.e., fetch it from the official Apple servers. recoveryOS can also be helpful for executing certain commands, such as disabling SIP (**S**ystem **I**ntegrity **P**rotection)...

## Note for legacy OS X users





<h2 align="center">
  <br>
  <div class="macrecoverypy-next-button-container">
    <a class="macrecoverypy-next-button" href="../02-macrecoverypy">macrecovery.py &rarr;</a>
  </div>
  <div class="navigation-container">
    <a class="nav-button" href="../../02-PlatformSpecific/index">&larr; Back Page</a>
    <a class="nav-button" href="../01-gibMacRecovery">gibMacRecovery &rarr;</a>
  </div>
  <br>
</h2>
