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

## Normalized Difference Built-up Index (NDBI) :
***NDBI***  targets built-up areas to recognize maximum reflectance in the shortwave infrared (SWIR) wavelengths that are coming out. Like the previous two indices ***NDVI & NDWI***, this index is also based on band ratioing and provides inputs for modern urban planning. <br>
***NDBI*** uses the NIR and SWIR bands to emphasize manufactured built-up areas, and it uses the following ratioing:<br>

***NDBI = (SWIR - NIR) / (SWIR + NIR)*** <br>

The values range from -1 to +1. <br>
Positive values signify built-up structures, whereas negative values represent water, soil, or vegetation. <br>

## Enhanced Vegetation Index (EVI) :
***EVI*** is similar to ***NDVI*** and can be used to quantify vegetation greenness. <br>

Additionally, ***EVI*** corrects for some atmospheric conditions and canopy background noise and is more sensitive in areas with dense vegetation. <br>

It incorporates an ***“L” value*** to adjust for ***canopy background***, ***“C” values*** as coefficients for ***atmospheric resistance***, and values from the ***blue band (B)***.  These enhancements allow for index calculation as a ratio between the R and NIR values, while reducing the background noise, atmospheric noise, and saturation in most cases. 
***EVI*** is given by the following ratio ***(Landsat Missions, USGS)***: <br>

***EVI = G * ((NIR - R) / (NIR + C1 * R – C2 * B + L))*** <br>

***In Landsat 4-7, EVI = 2.5 * ((Band 4 – Band 3) / (Band 4 + 6 * Band 3 – 7.5 * Band 1 + 1)).*** <br>

***In Landsat 8-9, EVI = 2.5 * ((Band 5 – Band 4) / (Band 5 + 6 * Band 4 – 7.5 * Band 2 + 1)).*** <br>

The value range typically spans from -1 to 1, where healthy, dense vegetation registers approximately between 0.20 and 0.80. <br>

## Normalized Burn Ratio (NBR) :
***NBR*** was designed to highlight burned areas and estimate fire severity. <br>
It uses near-infrared (NIR) and shortwave-infrared (SWIR) wavelengths. <br>

***NBR = (NIR - SWIR) / (NIR + SWIR)*** <br> 

Pre-fire, healthy vegetation has very high near-infrared reflectance and low reflectance in the shortwave infrared portion of the spectrum. <br>
Recently burned areas, on the other hand, have relatively low reflectance in the near-infrared and high reflectance in the shortwave infrared band. <br>
A high NBR value generally indicates healthy vegetation, while a low value indicates bare ground and recently burned areas. <br>
##### Source: https://gsp.humboldt.edu/olm/Courses/GSP_216/lessons/Spectral-Enhancements/NBR.html

## Soil Adjusted Vegetation Index (SAVI) :
SAVI is a remote sensing metric used to measure plant health while minimizing background soil brightness interference. <br>
It is similar to NDVI but is used in areas where vegetative cover is low (< 40%). <br>
When a significant amount of the soil surface is exposed, the soil reflectance can influence the NDVI values. 
Light reflected from the soil can have a significant effect on NDVI values (changing the values by up to 20%) 

SAVI is given by the following ratio:

***SAVI = [(NIR - Red) / (NIR + Red + L)] * (1 + L)*** <br>

***"L"*** is a ***correction factor*** which ranges from 0 for very high vegetation cover to 1 for very low vegetation cover. <br>
An ***"L"*** value of 0.5 is typically used for intermediate vegetation cover. <br>
When ***"L"*** is equal to zero SAVI becomes the same equation as ***NDVI***. <br>


