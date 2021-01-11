---
title: Installation Guide
nav_order: 3
has_children: true
---

# Install UMI

umi is a Rhino plugin that works with only with the Windows version of Rhino 6 or 7.

## System Requirements

| Requirement                | Minimum                                                                               | Recommended              |
|:---------------------------|:--------------------------------------------------------------------------------------|:-------------------------|
| RAM                        | 4 GB of free RAM                                                                      | 8 GB of total system RAM |
| Disk space          2.5 GB | SSD drive with at least 5 GB of free space                                            |                          |
| Monitor resolution         | 1024x768                                                                              | 1920×1080                |
| Operating system           | Officially released 64-bit versions of the following:<br>Microsoft Windows 8 or later |                          |

## Hardware

Windows computer with hardware capable of running CAD software

## Software

| Software   | Use     |
|:-----------|:--------|
| EnergyPlus | Editing |

[QGIS](https://qgis.org/en/site/index.html) or ArcGIS if participant has license
Rhinoceros 3D (https://www.rhino3d.com/download/) Note: UMI has been mostly tested with
Rhino version 6 but it should also work with Rhino 7.
[Umi for Rhino](http://web.mit.edu/sustainabledesignlab/projects/umi/index.html) Ubem.io

# Install using the `msi` installer

The
[umi installer](https://umireleases.blob.core.windows.net/latest-release/UMI.msi) is the
recommended tool to install umi. Use it to install and maintain umi on different versions
of Rhino, and easily remove umi.


<div class="code-example" markdown="1">

1. [Download the installer](https://umireleases.blob.core.windows.net/latest-release/UMI.msi)
   **.msi**.

   In Chrome, it is possible that the file will be blocked. Simply click on `...` and
   select "Keep".

   ![blocked](/umiverse-docs/assets/images/blocked.png "UMI.msi was blocked because it
   could harm your device")

   If
   [Microsoft Defender](https://docs.microsoft.com/en-us/windows/security/threat-protection/microsoft-defender-antivirus/microsoft-defender-antivirus-in-windows-10)
   is activated on your computer, the following window could also appear:

   ![harm](/umiverse-docs/assets/images/harm.png "Microsoft Defender SmartScreen")

   To dismiss, click on "Show more" and then click on "Keep anyway". This will allow you
   to run the msi installer.

2. Run the installer and follow the wizard steps.

When you run Rhino for the first time after the install, Rhino will check for
compatibility of the plugin.

For more information, see
[Run UMI for the first time](run-first-time)

</div>

{: .important }

> It is necessary to have administrative privileges to install UMI.

