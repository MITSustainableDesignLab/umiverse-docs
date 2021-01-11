---
title: Setup a project
parent: Get started
nav_order: 3
---

# Setup a project

## Opening/Creating a project

When working with UMI projects, it is important to use the umi functions and **NOT** the
Rhino commands for "Opening" and "Saving" a project. Umi creates it’s own file system
(\*.umi) which is a package containing all relevant files and data needed for a project.

To create a new project, simply click on the UMI button and select "open project" or "new
project" and browse to the folder location of your choice. Once a project has been opened.

![first-kd95h2j87.png](/umiverse-docs/assets/images/first-kd95h2j87.png "The umi menu")  
{: .d-flex.flex-justify-around }

{: .important}

> Working units must be in `Meters`. To change them, in Rhino, go to > File — Properties —
> Units — Model Units : Change to "meters".

## Choose a weather file

Weather data for the appropriate region of interest can be downloaded from the following:
- [EnergyPlus weather data](https://energyplus.net/weather)
- [OneBuilding.org](http://climate.onebuilding.org/)

An `.epw` is necessary.


## Saving a Project

All umi project geometry, settings, and simulation results are stored in a single .umi
file called an umi bundle. The location of the bundle is specified when you create a new
project, and whenever you save your Rhino document, this bundle is re-exported
automatically in the background. The bundle includes the project's Rhino scene file, the
epw weather file, building modeling templates as well as all simulation results in an
SQLite data base, so you don't need to include those separately if you transfer the bundle
to a different computer.

{: .note }
> Please note that an *.umi* file is just a compressed Windows.zip file, meaning that you  
> can access all data related to your project directly. The purpose of the bundle is to  
> streamline your workflow and to share and archive project data.

If you wish to change the location of the current umi bundle, use the UmiBundleSaveAs
Rhino command. There is no toolbar button to invoke this command - you have to type it
manually into the Rhino command window.

To export a copy of the current umi bundle without making it the "working" copy, use the
UmiBundleSaveCopy Rhino command. Like the UmiBundleSaveAs command, there is no toolbar
button for this command, and you will have to type it in yourself.

To export a project's building template library, use the "Export" button of the umi site
settings tab:

![site-config-dbe56713.png](/umiverse-docs/assets/images/site-config-dbe56713.png)

To export a project's geometry, use the standard Rhino SaveAs command (this is the command
invoked by selecting File > Save As... from the Rhino menubar). **The project's working
Rhino document will change, and standard geometry saves will now modify this new
version.**


