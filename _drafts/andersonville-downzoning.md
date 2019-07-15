---
layout: post
title:  "Proposed Andersonville downzoning: Who's affected and what could happen?"
tags:   [zoning and development]
---

The 47th Ward Zoning Advisory Council (ZAC) and Ald. Matt Martin are considering a proposal to downzone part of Andersonville from RT-4 to RS-3. Essentially, this would limit new housing to mostly single-family homes in an area known for its housing density, walkability, access to restauarants and small businesses, and proximity to 24-hour, frequent public transit.

I **oppose** the rezoning proposal outright. I want to address some of the points made by those backing the proposal.

Here's the proposal:
>  [Downzone] Andersonvile to RS-3 from the South side of Foster through to the South side of Argyle. From the East side of Clark through to the West side of Broadway. Rezoning does not include any B (business) districts or pockets that are already RS-3.

## What's currently there?
Most of the affected parcels are currently in the [RT-4 zoning district](https://secondcityzoning.org/zone/RT-4/), which allows two-flats and multi-unit buildings. Since zoning law typically sets maximums, single-family homes ("detached house") are always permitted in RT-4 districts.

The relevant zoning specifications for the RT-4 district are:

|Characteristic                 |Limit                       |
|-------------------------------|----------------------------|
|Floor area ratio               |1.2                         |
|Max. building height           |38 ft.                      |
|Lot area per unit (density)	|1,000 sq ft/dwelling unit<br>1,000 sq ft/efficiency unit<br>500 sq ft/SRO unit |

RT-4 allows multiple units, depending on the lot size.

Let's use *1441 W. Carmen* as an example lot. It started this whole thing, which I'll explain in a bit.

The city's [Building Footprints dataset](https://data.cityofchicago.org/Buildings/Building-Footprints-current-/hz9b-7nh8) shows us what's currently built:
|Zone       |RT-4 |
|Stories    |2    | 
|Units      |2    |
|Year Built |1906 |

What we really need to know is the lot area. Specifications for parcels of real estate are kept by the Cook County Assessor for the purpose of calculating property taxes. You can find a [GIS shapefile of parcels](https://datacatalog.cookcountyil.gov/GIS-Maps/Historical-ccgisdata-Parcels-2016/a33b-b59u) in the Cook County Data Portal. In this case, I went to the assessor's website and looked up the address, which yields an estimated lot size of **8,500 square feet**.

With a minimum area per unit of 1,000 sq ft. and a 8,500 sq ft. lot, you could build **at most** 8 units, so long as all of the other requirements like setbacks are met.

This is a huge lot, for the record. A "standard Chicago lot" of 125&times;25 feet or 3,125 sq ft. in an RT-4 district could be a 3-flat, at most.


## What would be allowed?
The [RS-3 zoning district](https://secondcityzoning.org/zone/RS-3/) permits single-family homes and allows *some* two-flats.

The relevant [zoning specifications](https://secondcityzoning.org/zoning_rules/) for the RS-3 district are:

|Characteristic                 |Limit                       |
|-------------------------------|----------------------------|
|Floor area ratio               |0.9                         |
|Max. building height           |30 ft.                      |
|Lot area per unit (density)    |2,500 sq ft                 |
|Minimum lot area               |2,500 sq ft                 |

You'll notice that the **minimum lot area** and the **lot area required per unit** are the same. This means only one unit is allowed. However, there is the following exception:

> **17-2-0303-B Exemption**
>
> In the RS3 district the minimum lot area per dwelling unit may be reduced to 1,500 square feet when 60% or more of the zoning lots fronting on the same side of the street between the two nearest intersecting streets have been lawfully improved with buildings containing more than one dwelling unit. This exemption will only allow for the establishment of a two unit building.
>
> *from the Chicago Zoning Ordinance*

So yes, you *can* build a two-flat in RS-3 *if* there is a super-majority of existing 2+ unit buildings on your side of the street, but it is literally the exception to the rule.

## Properties Affected by Rezoning
The map below shows properties affected by the proposal in orange. All of these buildings would be downzoned to RS-3. Properties in blue are either already RS-3 or excluded from the downzoning because they are in B (Business) or C (Commercial) districts or a PD (Planned Development).

<iframe src="{{ "/html/wfcw/map.html" | relative_url }}" height="480" width="672"></iframe>

> This map was created using public data from the City of Chicago. View the [R source code](https://github.com/mmmccarthy/mmmccarthy.github.io/blob/master/html/wfcw/map.Rmd) or download the spatial data (GeoJSON) and source code as a [zip file](https://github.com/mmmccarthy/mmmccarthy.github.io/raw/master/html/wfcw/rsource.zip).
>
> ***Note:** The city's buildings dataset is not reliably accurate. Some buildings are listed with zero stories or units.*

## Historic Buildings
The downzoning proposal comes out of a [fight last summer](https://www.change.org/p/wfcw-block-club-save-1441-carmen-from-demolition) to save an historic *Orange-rated* [^1] home at 1441 W. Carmen. Because the property is zoned RT-4, the developer could have built  Proponents of downzoning claim the proposal would save historic buildings, but that is simply wishful thinking. RS-3 does not provide any lasting protection for Orange-rated structures (or Red-rated ones, for that matter). It may be an economic disincentive for developers wishing to build multiple units, but there is still lots of value in new luxury single-family homes that are allowed under RS-3.

[^1]: "Orange-rated" refers to a structure's color grade in the Chicago Historic Resources Survey (1995). Red and Orange are the highest and second-highest grades, respectively, and demonstrate possibly historically- and architecturally-significant buildings. However, rated buildings are not necessarily protected as historic landmarks. Orange- and Red-rated buildings are subject to a 90-day demolition delay, meaning a demolition permit pulled for these buildings would be delayed. The delay is meant to give some time for preservationists, politicians, and city staff to work to avoid demolition of significant structures.

Additionally, this mass zoning change is overkill for the stated purpose of preserving historic homes. There are just 6 Orange-rated structures out of 328 properties that would be affected by the proposed downzoning.

A better solution might be to spot zone just those buildings considered historic as RS-3 and/or work toward actually landmarking these properties. 

## Neighborhood Character
The proponents want to preserve the neighborhood character of Andersonville, which they claim is represented by single-family homes. Let's look at the data. The city’s Building Footprints dataset (which admittedly excludes some of the properties in question and is not fully reliable) shows that buildings in the proposed re-zone typically have 2 to 12 units (first to third quartile) with an average of 9 units due to the presence of some very large buildings. If the downzoning were approved, I believe many of these smaller multi-unit buildings would be demolished and rebuilt as expensive single-family homes or deconverted. The cumulative effects of these rebuilds and deconversions with a prohibition on new multi-unit buildings are ultimately loss of population, density, and the “neighborhood character” and walkability that is so desired.

## Transit-oriented Development
The housing density allowed under RT-4 zoning is very supportive of high-frequency public transportation. The area considered for downzoning is between the 24-hour Red Line and the 24-hour 22 Clark bus. Additionally, the CTA plans to rebuild the Red Line structure and the Argyle station that serves this area as part of the $2.1 billion Red-Purple Modernization Phase 1 project.

I believe it is short-sighted and irresponsible to make dense, multi-family housing more expensive and more difficult to build in an area well-served by rapid transit. The major investment in rebuilding the Red Line makes this proposal even more irresponsible and ignorant of the wider planning context.

----------

# Data Analysis Process
How did I do this analysis? You can [view the map source code](https://github.com/mmmccarthy/mmmccarthy.github.io/blob/master/html/wfcw/map.Rmd) or download the spatial data (GeoJSON) and source code as a [zip file](https://github.com/mmmccarthy/mmmccarthy.github.io/raw/master/html/wfcw/rsource.zip).

### 1 - Gather Data
I started by downloading the following datasets from the city's Data Portal:
* [City of Chicago Zoning Districts](https://data.cityofchicago.org/Community-Economic-Development/Boundaries-Zoning-Districts-current-/7cve-jgbp) - includes zoning class (B-x, C-x, RT-4, RS-3, etc.)
* [City of Chicago Building Footprints](https://data.cityofchicago.org/Buildings/Building-Footprints-current-/hz9b-7nh8) - includes # of stories and other characteristics

Both datasets can be downloaded as shapefiles for use with GIS software. I used [QGIS](https://www.qgis.org/en/site/) to select only the areas of interest (both files are large, which will slow down your GIS software) and to join the two sets of data so that each building can be associated with its zoning district. The following instructions are for QGIS version 3.4. ArcGIS software uses similar terms.

### 2 - Select Zoning Districts in the "SoFoZoCo" area
For this step I am only concerned with reducing the file size and making the zoning districts file easier to work with.

Load both shapefiles (or GeoJSON) into QGIS by Layer > Add Layer > Add Vector Layer or simply drag-and-drop. To orient myself and to find the boundary streets, I used the [QuickMapServices](https://plugins.qgis.org/plugins/quick_map_services/) plugin to add a basemap from OpenStreetsMap. Then I used the Select Features tool on the Zoning dataset to select roughly all the zoning districts within the boundary. Once what you need is selected, right-click on the layer and choose **Export > Save Selected Features As...** to save a new, smaller shapefile.

![](/assets/wfcw/gis1.png)

With a smaller selection of Zoning Districts, I then selected only the buildings within the selected districts. I used a plugin called [Select Within](https://plugins.qgis.org/plugins/SelectWithin/) to help with this, as sometimes polygons/points/lines on the edge of a large polygon would not be selected. In ArcGIS, use Select by Location to select Buildings polygons with centroids in the selected Zoning districts polgons.

The result is much more manageable, but still covers a larger area than the proposed downzoning.

![](/assets/wfcw/gis2.png)

### 3 - Spatial Join Buildings to Zoning Districts
Now that we have more manageable files to work with, we can quickly join the zoning districts (RT-4, RS-3) to the applicable buildings/parcels of land.

To do this in QGIS, click **Vector** on the top menu, then **Data Management Tools > Join Attributes by Location**.

The **Input Layer** is what you'd like to join attributes to. For this project, the input is the **Buildings** data.

The **Join Layer** contains additional attributes. This is the **Zoning Districts** file. We just need the type of zoning district from the `zone_class` attribute. Add `zone_class` in the **Fields to add** section.

For **Geometric Predicate** I kept the default (Intersects). I kept the default for all remaining options.



### Select Buildings in the "SoFoZoCo" area
I wasn't sure what "south side of Argyle" meant since Argyle is quite complicated here. Many of the buildings don't face Argyle. For buildings facing a perpendicular street, how far down that block should be included? I decided to select up to Ainslie to include all the possible intended buildings.