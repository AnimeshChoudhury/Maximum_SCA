# Preparation of monthly Maximum Snow Cover Extent of North Western Himalayan Region
The Himalayan region is one of the most crucial mountain systems across the globe, which has significant importance in terms of the largest depository of snow and glaciers for fresh water supply, river runoff, hydropower, rich biodiversity, climate, and many more socioeconomic developments. This region directly or indirectly affects millions of lives and their livelihoods but has been considered one of the most climatically sensitive parts of the world.This study used the most recent version (V6) of the Level-3 MODIS/Terra 8-day composite snow Cover product MOD10A2 (https://nsidc.org/data/MOD10A2/versions/6), with a 500 m spatial resolution from March 2000 to February 2020. This dataset is freely available (https://search.earthdata.nasa.gov/search) and provides the maximum extent of snow cover over an 8-day period in 1200 km × 1200 km tiles. 

The whole study area covers Four tiles of MOD10A2 product: h24v06, h24v05, h23v05, and h25v06. The DN value of the respective classes are given below.
### pixel values 
#### 1: no decision
#### 11: night
#### 25: no snow
#### 37: lake
#### 39: ocean
#### 50: cloud
#### 100: lake ice
#### 200: snow
#### 254: detector saturated
#### 255: fill

step 1: Data downloaded and kept at their respective folders.  
step 2: All the datafiles are sorted according to the dates which is present in the filenames.  
step 3: Four files from four tiles are merged (mosaic) for each date to generate a single image for each date.
step 4: The images produced in the step 3 are reprojected to ESPG:4326.  
step 5: Rerojected images are then clipped with Shapefile's maximum extent which gives us us rectangular image of the study region.  
step 6: These rectangular images are again clipped according to the exact boundary of the study area using the shapefile.  
step 7: The data prepared in the above step is introduced to the function to generate monthly maximum snow cover extent.  
  
The function considers all the data files for a particular month and checks the DN value of each pixel. In a month, maximum four observation is possible and if a pixel has a DN value 200 in any one of the four observation, is considered as snow. All the other pixels are masked. This logic is applied to the all data files and monthly maximum snow cover extent is prepared.  
  
  
For more information about this study please read our research article: Choudhury, A.; Yadav, A.C.; Bonafoni, S. A Response of Snow Cover to the Climate in the Northwest Himalaya (NWH) Using Satellite Products. Remote Sens. 2021, 13, 655. https://doi.org/10.3390/rs13040655  

