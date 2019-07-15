---
layout: post
title:  "Andersonville downzoning would lead to population loss, fewer affordable housing units"
tags:   [zoning and development]
---

The 47th Ward Zoning Advisory Council (ZAC) and Ald. Matt Martin are considering a proposal to downzone part of Andersonville from RT-4 to RS-3. Essentially, this would limit new housing to mostly single-family homes in an area known for its housing density, walkability, access to restauarants and small businesses, and proximity to 24-hour, frequent public transit.

I **oppose** the rezoning proposal outright. I want to address some of the points made by those backing the proposal. I feel compelled to respond because the proponents are using my work to back their idea.

## Properties Affected by Rezoning

The map below shows properties affected by the proposal in orange. All of these buildings would be downzoned to RS-3. Properties in blue are either already RS-3 or excluded from the downzoning because they are in B (Business) or C (Commercial) districts or a PD (Planned Development).

<iframe src="{{ "/html/wfcw/map.html" | relative_url }}" height="480" width="672"></iframe>

> This map was created using public data from the City of Chicago. View the [R source code](https://github.com/mmmccarthy/mmmccarthy.github.io/blob/master/html/wfcw/map.Rmd) or download the spatial data (GeoJSON) and source code as a [zip file](https://github.com/mmmccarthy/mmmccarthy.github.io/raw/master/html/wfcw/rsource.zip).
>
> ***Note:** The city's buildings dataset is not reliably accurate. Some buildings are listed with zero stories or units.*

## Preserving Historic Buildings

## Existing "Neighborhood Character"

## What about the Red Line?

## Loss of Population

## Process
### Gather Data
* City of Chicago Zoning Districts - includes zoning class (B-x, C-x, RT-4, RS-3, etc.)
* City of Chicago Building Footprints - includes # of stories and other characteristics

### Select Zoning Districts in the "SoFoZoCo" area

### Spatial Join Buildings to Zoning Districts

### Select Buildings in the "SoFoZoCo" area
I wasn't sure what "south side of Argyle" meant since Argyle is quite complicated here. Many of the buildings don't face Argyle. For buildings facing a perpendicular street, how far down that block should be included? I decided to select up to Ainslie to include all the possible intended buildings.