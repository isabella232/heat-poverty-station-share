# NPR Heat Poverty Investigation

_Note: This is being made available early as a preview for reporters at NPR member stations. The full data and code will be made available when our story publishes on npr.org._

## Important data fields


`GEOID`: The Census ID number for this tract. Can be used to combine with other fields (income, education, age, etc.)

`GEO_ID`: GEOID written a longer way - sometimes you'll need to match with this format.

`median_hou`: Median household income for the Census tract as of 2017. If you want to dive deeper, it's Census variable `"B19013_001E": "Median household income in the past 12 months"`

`total_popu`: Population of the Census tract as of 2017

`white_popu`: White population of the Census tract as of 2017

`_median`: The median raster pixel heat value for the Census tract in degrees kelvin. Note this is __surface temperature__, not ambient temperature.


## Simplified files

Also in the `geojsons` folder is a folder called `simpl`. This has city .geojsons with simplified polygons for mapping on the web. These are used in NPR's web maps.


## Caveats
- There is a difference between poverty vs. low-income
- More detailed Census geography = larger MOE
- We're using surface temperature, not ambient temperature
- Only one day of data per city
- Not every city is counted
- Some cities split satellite scene paths/rows, so we took the image from the scene that contained most of the city. You'll need to filter out tracts without heat data in any data analysis/mapping you do.
