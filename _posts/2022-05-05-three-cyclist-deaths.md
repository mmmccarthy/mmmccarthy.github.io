---
layout: post
title:  "Chicago has already reached 3 bicyclist deaths in 2022, much earlier than in previous years"
date:   2022-05-05 21:00:00 -0600
permalink:  /chicago-reached-3-cyclist-deaths-earlier-than-previous-years/
categories: projects
tags:       [Vision Zero, safety, complete streets]
---

There have been [3 people killed so far this year](https://chi.streetsblog.org/2022/05/05/failure-to-create-safe-cycling-conditions-on-milwaukee-leads-to-second-bike-death-at-kilbourn/) while riding a bike in Chicago. This got me wondering how quickly we have reached 3 bicyclist deaths in prior years. 

I loaded my collection of IDOT crash data for years 2009 to 2017 ([available on GitHub](https://github.com/mmmccarthy/chivz/blob/master/idot_crashes/IDOT_Crashes_Chicago_2009_2017.rds)) to check it out. This data is delayed, but this allows for important corrections like serious injuries that later result in death. This is a problem in the more quickly updated data from the Chicago Police Department, where some known fatal crashes are still listed in the "incapacitating injury" category. These crashes will later be corrected when CPD sends the finalized data to IDOT, but that is a long process.

I did my analysis in an RMarkdown Notebook, which I'm including below. This notebook allows you to view the R code by clicking on the Code button above each table.

<iframe src="{{ "/html/cyclist-deaths-2022/explore_fatal_crashes_May5.html" | relative_url }}" height="2000" style="width:100%;" frameborder="0"></iframe>

