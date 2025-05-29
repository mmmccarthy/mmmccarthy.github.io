---
layout: post
title:  "Funny bugs I've found recently"
date:   2025-05-01 12:00:00 -0600
permalink:  /funny-bugs/
categories: blog
tags:       [bugs, fun]
---

This is a bug in GISDK, a fun mix of Geographic Information Systems (GIS) and Software Development Kit (SDK), a compiled apparenly VB-like language used in Caliper's TransCAD software. 
Note that it uses `=` for both equality and assignment. 

```
  // GUI passes year
  shared year
  Input text 10, 1, "Year", year

  //     ...

// called within a main function that is called several times
  shared year
  year = if (year = null) then "2020" else i2s(year)
  file_path = year + "SE_DATA.bin"
```

Did you catch it? Perhaps it helps to know that the `i2s()` (integer to string) function throws an error when it gets anything but an integer as input.
In this case, the user input of the scenario year in a text box is passed to a shared variable `year`. Shared is a way to give a variable wider scope, allowing the variable to be accessed in any other function or Macro (user-created functions) as long as they declare the shared variable before accessing it. Global scope allows a variable to be accessed from anywhere in the program. 

When this second snippet runs, `year` is often pointing to the string "2020" and is not null. I2s hates getting a string and throws an error.

I had plans to get dinner and drinks with friends on a Friday and texted the group that I had a fun computer bug to tell them about. I nearly forgot but my scheme worked and my friend Desmond asked me about the bug.

This is is also GISDK, and it's a little gnarlier. It's gone undetected for at least 5 years, probably more. 

This one has a lot to do with an abstraction in travel demand modeling called external zones. Travel analysis zones (TAZs) aggregate the travel behavior of hundreds or thousands of people living or working in a particular neighborhood or set of blocks. Models need a way to represent traffic that is coming in, going out, or passing through their region without also representing the people and households of every area these trips might start or end in. External zones truncate trips at major roads around a cordon of the modeled region and aggregate all trips starting or ending on a particular corridor. These external zones don't typically have any data about the number of people or households attached to them.

A client asked us why his regional model was reporting the wrong number of households in the model. It seemed like such a basic thing to calculate in a model, so I went to check the code that writes out this number.

```
// HH1, HH2, HH3, HH4 are vectors of the values for fields in the TAZ households data
numTAZ 			= R2I(VectorStatistic(HH1,"Count",))

dim totHH[numTAZ]
totHH = HH1 + HH2 + HH3 + HH4

totalHouses = 0

for ii = 1 to numTAZ do
  totalHouses 	= NZ(totalHouses) + NZ(totHH[ii])
end
```

Think of tabular data that you might calculate in Excel. You have a table of households by size, perhaps from the Census. TAZ is traffic analysis zone, an abstraction I should have told you about earlier. Most zones are internal with defined geography and a known number of people and households. These zones are used to generate aggreate trips made by all people living or working within the defined zone.

| TAZ | HH1 | HH2 | HH3 | HH4 |
|:---:|:---:|:---:|:---:|:---:|
|101|5|36|62|20|
|102|178|400|53|70|
|103|0|0|0|0|

Since we only have households by size, we need to sum four columns and then take the sum of total households in each row. This script does just that by looping through each row, calculating total households, and adding to a running total of households.

But the external zones I mentioned previously come in here. This particular scenario's TAZ file used null values for the external zones. Modelers tend to list the external zones at the bottom of the table and give them high ID numbers to distinguish them from internal zones.

| TAZ | HH1 | HH2 | HH3 | HH4 |
|:---:|:---:|:---:|:---:|:---:|
|900|-|-|-|-|
|902|-|-|-|-|
|903|-|-|-|-|





