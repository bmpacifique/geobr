# log history of geobr package development

-------------------------------------------------------
# geobr v1.0 (2019-07-30)

* Launch of **geobr** v1.0 on [CRAN](https://cran.r-project.org/web/packages/geobr/index.html) with the following data sets:
  * Country
  * States
  * Regions
  * Meso regions
  * Micro regions
  * Municipalities
  * Census weighting areas
  * Census tracts
  * Statistical Grid 

-------------------------------------------------------
# geobr v1.1 (2019-12-03)

### New data sets/functions
* data set `read_indigenous_land` to read official data of indigenous lands of all ethnicities according to stage of demarcation - closes issue #47 (2019-09-04).
* data set `read_disaster_risk_area` to read official data of areas exposed to risks of geodynamic and hydro-meteorological disasters capable of triggering landslides and floods - closes issue #14 (added in 2019-09-24).
* data set `read_biomes` to read official data of polygons of all of all biomes present in Brazilian territory - closes issue #45 (added in 2019-09-24).
* data set `read_amazon` to read official data of Brazil's Legal Amazon - closes issue #38 (added in 2019-10-07).
* data set `read_conservation_units` to read official data of Environmental Conservation Units - closes issue #59 (added in 2019-10-08).
* data set `read_urban_area` to read official data of urban footprint of Brazilian cities - closes issue #52 (added in 2019-10-17).
* data set of biomes (2019) available at scale 1:250.000. (added in 2019-10-31) - closes issue #72
* data set of `read_intermediate_region` (2017) (added in 2019-11-28)
* data set of `read_immediate_region` (2017) (added in 2019-11-28)
* function `download_metadata` simply the download of df with data set addresses.

### Minor changes
* Changes to `read_region` function to improve speed and remove `dplyr`dependency (added in 2019-10-22).
* Shows a single download progress bar when `*_code="all"`. This fixes the output of vignette and closes issue #42 (2019-08-05)

-------------------------------------------------------
# geobr v1.2 (2020-02-20)

### New data sets/functions
* data set `read_metro_area` to read official metropolitan areas - closes issue #2 (added in 2019-12).
* data set `read_municipal_seat` to read the spatial coordinates of municipal seats- closes issue #86 (added in 2019-12).
* function `lookup_muni` to look up municipality codes by their name, or the other way around. closes issue #58 (added in 2019-12)
* function `list_geobr` to list all the datasets available in geobr - Closes issue #57.
  
### Major changes
* MAJOR change of `geobr` to read `geopackage` files, instead of `.rds`. A structural change that will make it easier to maintain both versions of geobr in R and Python  (2020-02)
* All functions now have an additional argument `tp` as in data 'type'. This argument defaults to read data sets with 'simplified' borders, what makes the package much more efficient for downloading and plotting the data. Closes issue #76 (2020-02)
* Pretty much all functions now download the data for the entire country as a default. Closes issue #77. The only exceptions are `read_statistical_grid` and `read_census_tract`. These two functions do take a really long time to load the data for the whole country and it might crash R due to memory limits, so the user must be more 'aware' about her choice (2020-02)

 ### Minor changes
 * New utils.R script containing support functions to reduce code redundancy (2020-02)
 

  
  
  
