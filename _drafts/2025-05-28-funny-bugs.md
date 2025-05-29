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
