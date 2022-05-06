---
layout: post
title:  "Chicago has already reached 3 bicyclist deaths in 2022, much earlier than in previous years"
date:   2022-05-05 21:00:00 -0600
permalink:  /chicago-reached-3-cyclist-deaths-earlier-than-previous-years/
categories: projects
tags:       [Vision Zero, safety, complete streets]
---

There have been [3 people killed so far this year](https://chi.streetsblog.org/2022/05/05/failure-to-create-safe-cycling-conditions-on-milwaukee-leads-to-second-bike-death-at-kilbourn/) while riding a bike in Chicago. This got me wondering how quickly we have reached 3 bicyclist deaths in prior years. 

I loaded my collection of IDOT crash data for years 2009 to 2017 ([available on GitHub](https://github.com/mmmccarthy/chivz/blob/master/idot_crashes/IDOT_Crashes_Chicago_2009_2017.rds)) to check it out. This data is delayed, but this allows for important corrections like serious injuries that later result in death. This is a problem in the more quickly updated data from the Chicago Police Department, where some known fatal crashes are still listed in the "incapacitating injury" category. These crashes will later be corrected when CPD sends the finalized data to IDOT, but that is a long process. I also repeated the analysis with more recent city data through 2021, available on the [Chicago Data Portal](https://data.cityofchicago.org/Transportation/Traffic-Crashes-Crashes/85ca-t3if). 

I did my analysis in an RMarkdown Notebook, which I'm including below. This notebook allows you to view the R code by clicking on the Code button above each table.

<iframe src="{{ "/html/cyclist-deaths-2022/explore_fatal_crashes_May5.html" | relative_url }}" height="1850" style="width:100%;" frameborder="0"></iframe>

In the last table above, I notice [Carla Aiello's crash](https://chi.streetsblog.org/2019/11/06/human-protected-bike-lane-vigil-tonight-will-honor-woman-37-killed-by-turning-trucker/) on Milwaukee Ave near the same intersection as the most recent crash in 2022 was also the third fatal crash of 2019, but that crash happened in November.

As far as I can tell, there has not been a year in recent memory where 3 cyclists have died on Chicago streets before early May. We typically reach that number of deaths later in the summer, which is when we typically see more cyclist deaths as the weather warms up. It's a double gut punch because some of the most recent cyclist deaths have happened in spots known to city officials and people who bike and walk nearby as particularly dangerous, yet the city has not done nearly enough to tame deadly driver behavior.
