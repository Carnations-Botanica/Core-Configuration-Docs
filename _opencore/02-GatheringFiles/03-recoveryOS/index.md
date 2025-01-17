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

This section will help you fetch the recoveryOS used for installing macOS.

# Why are we using recoveryOS ?
The recoveryOS is a lightweight operating system provided by Apple that helps users repair their macOS installations, recover lost files, or **reinstall macOS**. By using it, we can 'trick' the OS into thinking that macOS was already installed on our PC, allowing us to have it 'reinstall' macOS for us, i.e., fetch it from the official Apple Servers. recoveryOS can also be helpful for executing certain commands, such as disabling SIP (**S**ystem **I**ntegrity **P**rotection)...

# macrecovery.py or gibMacRecovery
`macrecovery.py` is the tool bundled with `OpenCorePkg` used to fetch recoveryOS from online servers. `gibMacRecovery` is a wrapper around macrecovery that automates most of the CLI switches, and may be easier to use, as it can automatically download Python and get the recoveryOS for you with less hustle. Check the following pages to see which one suits you best.

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
