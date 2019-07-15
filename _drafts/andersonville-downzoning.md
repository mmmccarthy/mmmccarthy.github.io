---
layout: post
title:  "Proposed Andersonville downzoning: Who's affected and what could happen?"
tags:   [zoning and development]
---

The 47th Ward Zoning Advisory Council (ZAC) and Ald. Matt Martin are considering a proposal to downzone part of Andersonville from RT-4 to RS-3. Essentially, this would limit new housing to mostly single-family homes in an area known for its housing density, walkability, access to restauarants and small businesses, and proximity to 24-hour, frequent public transit.

I **oppose** the rezoning proposal outright. I want to address some of the points made by those backing the proposal.

## Properties Affected by Rezoning
The map below shows properties affected by the proposal in orange. All of these buildings would be downzoned to RS-3. Properties in blue are either already RS-3 or excluded from the downzoning because they are in B (Business) or C (Commercial) districts or a PD (Planned Development).

<iframe src="{{ "/html/wfcw/map.html" | relative_url }}" height="480" width="672"></iframe>

> This map was created using public data from the City of Chicago. View the [R source code](https://github.com/mmmccarthy/mmmccarthy.github.io/blob/master/html/wfcw/map.Rmd) or download the spatial data (GeoJSON) and source code as a [zip file](https://github.com/mmmccarthy/mmmccarthy.github.io/raw/master/html/wfcw/rsource.zip).
>
> ***Note:** The city's buildings dataset is not reliably accurate. Some buildings are listed with zero stories or units.*

## Historic Buildings
The downzoning proposal comes out of a [fight last summer](https://www.change.org/p/wfcw-block-club-save-1441-carmen-from-demolition) to save an historic *Orange-rated* [^1] home at 1441 W Carmen. Because the property is zoned RT-4, the developer could have built  Proponents of downzoning claim the proposal would save historic buildings, but that is simply wishful thinking. RS-3 does not provide any lasting protection for Orange-rated structures (or Red-rated ones, for that matter). It may be an economic disincentive for developers wishing to build multiple units, but there is still lots of value in new luxury single-family homes that are allowed under RS-3.

[^1]: "Orange-rated" refers to a structure's color grade in the Chicago Historic Resources Survey (1995). Red and Orange are the highest and second-highest grades, respectively, and demonstrate possibly historically- and architecturally-significant buildings. However, rated buildings are not necessarily protected as historic landmarks. Orange- and Red-rated buildings are subject to a 90-day demolition delay, meaning a demolition permit pulled for these buildings would be delayed. The delay is meant to give some time for preservationists, politicians, and city staff to work to avoid demolition of significant structures.

Additionally, this mass zoning change is overkill for the stated purpose of preserving historic homes. There are just 6 Orange-rated structures out of 328 properties that would be affected by the proposed downzoning.

A better solution might be to spot zone just those buildings considered historic as RS-3 and/or work toward actually landmarking these properties. 

## Neighborhood Character
The proponents want to preserve the neighborhood character of Andersonville, which they claim is represented by single-family homes. Let's look at the data. The city’s Building Footprints dataset (which admittedly excludes some of the properties in question and is not fully reliable) shows that buildings in the proposed re-zone typically have 2 to 12 units (first to third quartile) with an average of 9 units due to the presence of some very large buildings. If the downzoning were approved, I believe many of these smaller multi-unit buildings would be demolished and rebuilt as expensive single-family homes or deconverted. The cumulative effects of these rebuilds and deconversions with a prohibition on new multi-unit buildings are ultimately loss of population, density, and the “neighborhood character” and walkability that is so desired.

## Transit-oriented Development
The housing density allowed under RT-4 zoning is very supportive of high-frequency public transportation. The area considered for downzoning is between the 24-hour Red Line and the 24-hour 22 Clark bus. Additionally, the CTA plans to rebuild the Red Line structure and the Argyle station that serves this area as part of the $2.1 billion Red-Purple Modernization Phase 1 project.

I believe it is short-sighted and irresponsible to make dense, multi-family housing more expensive and more difficult to build in an area well-served by rapid transit. The major investment in rebuilding the Red Line makes this proposal even more irresponsible and ignorant of the wider planning context.

## Process
How did I do this analysis? You can [view the map source code](https://github.com/mmmccarthy/mmmccarthy.github.io/blob/master/html/wfcw/map.Rmd) or download the spatial data (GeoJSON) and source code as a [zip file](https://github.com/mmmccarthy/mmmccarthy.github.io/raw/master/html/wfcw/rsource.zip).

### 1 - Gather Data
I started by downloading the following datasets from the city's Data Portal:
* [City of Chicago Zoning Districts](https://data.cityofchicago.org/Community-Economic-Development/Boundaries-Zoning-Districts-current-/7cve-jgbp) - includes zoning class (B-x, C-x, RT-4, RS-3, etc.)
* [City of Chicago Building Footprints](https://data.cityofchicago.org/Buildings/Building-Footprints-current-/hz9b-7nh8) - includes # of stories and other characteristics

Both datasets can be downloaded as shapefiles for use with GIS software. I used QGIS to select only the areas of interest (both files are large, which will slow down your GIS software) and to join the two sets of data so that each building can be associated with its zoning district. The following instructions are for QGIS version 3.4. ArcGIS software uses similar terms.

### 2 - Select Zoning Districts in the "SoFoZoCo" area
For this step I am only concerned with reducing the file size and making the zoning districts file easier to work with.

Load both shapefiles (or GeoJSON) into QGIS by Layer > Add Layer > Add Vector Layer or simply drag-and-drop. To orient myself and to find the boundary streets, I used the [QuickMapServices](https://plugins.qgis.org/plugins/quick_map_services/) plugin to add a basemap from OpenStreetsMap. Then I used the Select Features tool on the Zoning dataset to select roughly all the zoning districts within the boundary. Once what you need is selected, right-click on the layer and choose 

![](/assets/wfcw/gis1.png)


![](/assets/wfcw/gis2.png)

### 3 - Spatial Join Buildings to Zoning Districts

### Select Buildings in the "SoFoZoCo" area
I wasn't sure what "south side of Argyle" meant since Argyle is quite complicated here. Many of the buildings don't face Argyle. For buildings facing a perpendicular street, how far down that block should be included? I decided to select up to Ainslie to include all the possible intended buildings.