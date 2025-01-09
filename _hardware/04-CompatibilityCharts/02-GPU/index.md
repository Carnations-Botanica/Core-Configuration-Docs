---
layout: default
title: GPU Support Chart
parent: Compatibility Charts
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

  .intel-next-button-container,
  .nvidia-next-button-container {
    text-align: right;
  }

  .intel-next-button,
  .nvidia-next-button {
    margin: 10px;
  }
</style>

<p align="center">
  <img width="650" height="200" src="../../../../assets/Headers/Header-GPUSupportChart.png">
</p>

<h2 align="center">Important Notes for everyone!</h2>
<h2 align="center">Please make sure you read these.</h2>
<br>

{: .warning }
If your card falls under the Hopper (Datacenter GPUs), Blackwell (RTX 50xx), Ada Lovelace (RTX 40xx), Ampere (RTX 30xx) or Turing (RTX 20xx) generations of NVIDIA RTX, your card is completely unsupported. Your options are using a supported Intel iGPU, or purchasing an AMD dedicated Graphics Card if you are on an AMD CPU. OpenCore Legacy Patcher will not solve this issue, RTX has never had support.

{: .important }
The Intel iGPU chart page is currently a work in progress, and information may be incorrect. If you seem to spot an error or have better information, please feel free to make a pull request for the Intel Support Chart page! Intel experts needed for validity of Initial and Latest support. This note should go away sooner or later.

{: .note }
The NVIDIA support charts are mainly here for legacy OS X users for preservation, such cases include but are not limited to: Audio Engineers, Film Editors, and Photographers using legacy licensed software. As of High Sierra (10.13), all NVIDIA GPUs (except for Kepler, dropped in Big Sur due to Metal 1 support) were dropped from Mac OS X. High Sierra is no longer viable as an operating system, and if you only have NVIDIA graphics, you cannot use modern macOS.

{: .note }
The importance of these charts are to quickly reference what Graphics Processing Units are supported, what version they first began their support on, and the latest release that still have kernel extensions for said GPU. We also keep track of non supported GPUs to quickly reference they are not supported. This area is a major point of Pull Requests, help out if you can! We're interested in learning what GPUs work when spoofed as their supported counterparts.

{: .note }
When reading these support charts, keep in mind that the most powerful card of the generation is at the top, and it's sorted down by boost clock speed. When it comes to Intel iGPUs, it is similarly sorted. NVIDIA charts are also sorted by card number. This makes it really easy to quickly scroll down until you find your device.

<br>
<p align="center">Start by choosing the Brand for your GPU/iGPU</p>

<h2 align="center">
  <br>
  <div class="intel-next-button-container">
    <a class="intel-next-button" href="../01-Intel">Intel &rarr;</a>
  </div>
  <div class="nvidia-next-button-container">
    <a class="nvidia-next-button" href="../02-AMD">AMD &rarr;</a>
  </div>
  <div class="navigation-container">
    <a class="nav-button" href="../../01-CPU/index/">&larr; Back Page</a>
    <a class="nav-button" href="../03-NVIDIA">NVIDIA &rarr;</a>
  </div>
  <br>
</h2>
