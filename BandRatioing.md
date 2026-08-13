# Band Ratioing Defined
***Band ratioing*** in Remote Sensing is used to display spectral variations. 
Spectral band ratioing enhances the desired compositional information while suppressing other types of information, such as the terrain slope and grain-size differences.

**Band ratioing** is a technique in which DN values in one spectral band is divided from the corresponding values in another band. The resultant image is commonly known as a ratioed image.

# Different Indices
## Normalized Difference Vegetation Index (NDVI) :
The ***NDVI*** is a band ratioing involving visible red and near-infrared bands of satellite images and determines the vegetation cover over a particular area. It is a simple numerical indicator used to assess whether the target being observed contains live green vegetation.

***NDVI = (NIR - Red) / (NIR + Red)*** <br> 

In **Landsat 4-7**, ***NDVI*** = ***(Band 4 – Band 3) / (Band 4 + Band 3)***. <br>

In **Landsat 8-9**, ***NDVI*** = ***(Band 5 – Band 4) / (Band 5 + Band 4)***. <br>

The results span from -1.0 to +1.0, where <br>
**-1.0 to 0**:   Indicates Water bodies, clouds, snow, or non-living structures like concrete and roads. <br>
**0 to 0.2**:    Indicates Bare soil, rocks, or sand with little to no vegetation.<br>
**0.2 to 0.4**:  Indicates Sparse or stressed vegetation like dry grasslands and shrubs.<br>
**0.6 to 1.0**:  Indicates Dense, robust vegetation like temperate crops, thick and healthy forests, and tropical rainforests.<br><br>

## Normalized Difference Water Index (NDWI) :
***NDWI*** has been computed using the specified bands of the LISS III images (GREEN and NIR). 
It is a metric used to detect and monitor water bodies or measure liquid water absorption in vegetation. <br>
To monitor changes related to water content in water bodies, using green and NIR wavelengths, defined by **McFeeters (1996)** following ratioing is used: <br>

***NDWI = (Green - NIR) / (Green + NIR)*** <br> 

To monitor changes in the water content of leaves, using near-infrared (NIR) and short-wave infrared (SWIR) wavelengths, as proposed by **Gao (1996)** following ratioing is used: <br>

***NDWI = (NIR - SWIR) / (NIR + SWIR)*** <br> 

***NDWI*** values likely range between −1 and 1 <br>

## Normalized Difference Built-up Index (NDBI)
***NDBI***  targets built-up areas to recognize maximum reflectance in the shortwave infrared (SWIR) wavelengths that are coming out. Like the previous two indices ***NDVI & NDWI***, this index is also based on band ratioing and provides inputs for modern urban planning. <br>
***NDBI*** uses the NIR and SWIR bands to emphasize manufactured built-up areas, and it uses the following ratioing:<br>

***NDBI = (SWIR - NIR) / (SWIR + NIR)*** <br>

The values range from -1 to +1. <br>
Positive values signify built-up structures, whereas negative values represent water, soil, or vegetation. <br>


