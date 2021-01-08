---
layout: default
title: Get started
parent: ubem.io
nav_order: 2
---
# Get started
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

# Data Requirements
The key intent of UBEM.io is to receive an input geometric file defining the urban building context of interest, and output an umi for Rhino file for simulations and scenario analysis in UMI for Rhino. Within UBEM.io, users will be able to segment/group the building stock into desired archetypes, and assign relevant building simulation templates from our database/library. The assigned building templates will be reflected in the umi file automatically, eliminating the need for manual assignments. Umi allows various urban-scale simulations, including energy and daylighting.

There are three main types of data required in the workflow: 1) Weather data, 2) Geometry data, and 3) Non-geometric data.

## Weather Data
Weather data for the appropriate region of interest can be downloaded from the following:
- [EnergyPlus weather data](https://energyplus.net/weather)
- [OneBuilding.org](http://climate.onebuilding.org/)

## Geometry 
Geometry files can exist in different formats, and cities/municipalities around the world manage these files differently. Common file formats include geographical information system (GIS)  shapefiles, CityGML files, CityJSON, etc. Alternatively, geometry data can also be extracted from open data sources such as OpenStreetMaps. For this workshop, we will be working primarily with shapefiles. The basic requirements is a GIS file with building footprints, heights, and program/use type (for each footprint). Specific data requirements are as follows:

Geographical Information Systems (GIS) ShapeFiles :
Shapefile (.shp) with all associated files (.dbf .cpg .prj .shx) should be included
Shapefile should contain building footprint polygons, with each polygon representing one building, and includes all available data/attributes for the building (see: Required columns / attribute fields).
EPSG: 4326 - WGS 84 - Geographic Coordinate Reference System preferred, but UBEM.io should support other projections. 
Shapefile should minimally contain:
At least one categorical column or attribute field to categorize/group the building stock into appropriate archetypes (example include program type or zoning) 
At least one numerical column or attribute field to categorize/group the building stock (example include year built or building age)
Other required columns / attribute fields:
ID: Unique identifier for each building footprint polygon. If the ID field is not present, UBEM.io will automatically generate one sequentially, but this will be hard for the city to compare back to at the end). The ID must be in the first column. Refactor the attribute table if you need to change this. 
Height:  height of each building in meters (if difficult to obtain, obtain by multiplying floors or number of storeys by a standard floor-to-floor height, which can be done easily in QGIS or ArcGIS)
Program Type / End Use: For each building footprint polygon. Examples include residential, commercial, and mixed-use, etc.
Year Built /Age
Additional columns / attribute fields that enhance models:
Storey: Number of storeys for the building. Necessary if you do not have height data. 
Window-to-wall (WWR) ratio: If you have the data, great. Otherwise, it can be assigned in UBEM.io, based on archetype / category. Defaults to 40% for all of north, south, east and west elevations. UBEM.io assumes WWR is similar across all elevations (currently does not have functionality to assign different WWR for each elevation)

## Non-Geometric Data
Non-geometric data is necessary to characterise the building properties. Typical non-geometric data includes envelope and fenestration/glazing properties, as well as systems (heating, ventilation and air-conditioning). These non-geometric properties will aid the creation of building simulation templates for the simulation engine. These data can be obtained from building audits, records, specifications, as-built models, or simply best-estimates. 

Non-Geometric Data: Creating UMI Building Templates
Define key parameters for building energy simulation
Need to be developed for different building use types or construction and age
Three ways to create templates:
From an existing EnergyPlus idf file via archetypal 
By editing an existing template to match your parameters using the UMI Template Editor
From scratch using the UMI Template Editor

Typical data required for creating building templates (in UMI for Rhino) include: 
Construction assembly (such as typical roof, wall, floor construction materials and thickness) 
Glazing (window) properties
Equipment and lighting loads
HVAC equipment and schedules
Occupancy schedules and density

## Key terms for defining templates:

Building Templates:
Entire collection of interior and exterior features of the structure.
Templates may consist of one or more zones, with each zone having different parameters.
Zones:
Groups of enclosed surfaces that typically have different space conditioning parameters, and can each interact with each other thermally and have a common air mass at roughly the same temperature.
One or more rooms within a building.
Zones may consist of one or more surfaces but need to be closed
Surfaces:
Walls, roofs, ceilings, floors, partitions, windows, shading devices, etc.
Surfaces consist of a series of materials called a “construction”.
One or more surfaces make up a zone.
Materials:
Define the thermal properties for layers that are used to put together a construction.
One or more material layers make a construction.
Material:Regular
Has thermal mass.
Thickness, conductivity, density, and specific heat.
Material:Regular-R
Has no thermal mass.
Thickness, conductivity, density, and specific heat.
Material:Air
Also no thermal mass, just resistance.
Cannot be an outside layer, no absorptances.
Otherwise, modeled same as Material:Regular-R

[OneBuilding.org]: http://climate.onebuilding.org/

[EnergyPlus weather data]: https://energyplus.net/weather