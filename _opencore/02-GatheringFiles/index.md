---
layout: default
title: Gathering Files
description: This section goes over how to gather all the files required by OpenCore, and specifics for hardware.
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
  <img width="650" height="200" src="../../../assets/Headers/Header-GatheringFiles.png">
</p>

<h2 align="center">Where to source OpenCore, Where to install it to.</h2>
<br>

## **Fetching OpenCorePkg**

To begin, you will want to go to the **[OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)** Github page. On the right side, you will see a ``Releases`` tab. This will take you to the latest version that is available for download. We recommend downloading the ``DEBUG`` variant so you can get the best logs when requesting support.

The contents of the zip will contain roughly the following files:

```bash
├── Docs
│   ├── AcpiSamples
│   │   ├── Binaries
│   │   └── Source
│   ├── Changelog.md
│   ├── Configuration.pdf
│   ├── Differences.pdf
│   ├── Sample.plist
│   └── SampleCustom.plist
├── IA32
├── Utilities
└── X64
    └── EFI
        ├── BOOT
        │   └── BOOTx64.efi
        └── OC
            ├── ACPI
            ├── Drivers
            ├── Kexts
            ├── OpenCore.efi
            ├── Resources
            └── Tools
```

## **Preparing the USB Drive**

What you'll want to do, is begin by selecting the appropriate folder for your systems architecture. For this example, we will be using ``X64`` instead of ``IA32``.

Move the ``EFI`` folder that exists within the architecture of choice, and drop it to the root of your recently freshly formatted USB drive. This is what your two windows would look like in preparation to copy it over:

<br>
<p align="center">
  <img width="100%" height="100%" src="../../../assets/OpenCore/EFIToUSBInitial.png">
  <p align="center"><i>LEFT: OpenCore ZIP opened in X64 folder, RIGHT: Root of Freshly formatted USB stick.</i></p>
</p>

<br>
Once you're done, this is what the root of your USB should look like:

<br>
<p align="center">
  <img width="100%" height="100%" src="../../../assets/OpenCore/InitialUSBPostEFIDrop.png">
</p>
<br>

Don't worry if you don't have hidden folders/items enabled as it won't affect the USBs ability to boot. We'll now need to navigate to the following path:

{: .important }
``USB`` is how your flash drive will be referenced from now on.

```bash
USB/EFI/OC/
```

## **Using Sample.plist for configuration**

Now, you'll need to quickly browse for ``Sample.plist`` within ``Docs/`` folder of the OpenCore ZIP file you unpacked earlier.

<br>
<p align="center">
  <img width="100%" height="100%" src="../../../assets/OpenCore/ZIPSampleHIghlighted.png" alt="">
</p>
<br>

Copy and paste this ``Sample.plist`` onto ``USB/EFI/OC/Sample.plist`` like so:

<br>
<p align="center">
  <img width="100%" height="100%" src="../../../assets/OpenCore/USBSampleInitial.png" alt="">
</p>
<br>

You must now rename the file to ``config.plist``, as this is the actual property list that OpenCore is looking for and will load as the configuration file.

<br>
<p align="center">
  <img width="100%" height="100%" src="../../../assets/OpenCore/USBEFIConfigurationFileRename.png">
</p>
<br>

You now have a configuration file that OpenCore can load and use. You can open this properly list file later on in an appropriate property list editor.

Before we can continue, we must do an initial run through the contents of ``USB/EFI/OC`` to actually configure each folder with attention, as we won't begin modifying the OpenCore configuration itself until we're done preparing. When you are ready to continue, press below.

<h2 align="center">
  <br>
  <div class="navigation-container">
    <a class="nav-button" href="../../01-Introduction/">&larr; Back Page</a>
    <a class="nav-button" href="../01-EFI/index">Next Page &rarr;</a>
  </div>
  <br>
</h2>
