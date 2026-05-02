# Flash Drought Detection in Wildlife Management Areas

A generalized implementation of the SESR-based three-criterion 
flash drought detection framework (Christian et al. 2019, 2022, 2023), 
applied to Wildlife Management Areas across contrasting climate regimes.

## Associated Publication
Ongondo, F. (2026). Flash drought detection and vegetation stress 
response in Wildlife Management Areas across contrasting climate 
regimes using MERRA-2 and Landsat remote sensing.
*Remote Sensing of Environment* (under review).

## Repository Contents
| File | Description |
|------|-------------|
| `detecting_flashdrought_ecological_impact.py` | Generalized SESR flash drought detection pipeline |

## Input Data

All input data used in this study are publicly available 
and can be downloaded from the following sources:

**MERRA-2 Reanalysis (ET, PET, Root-zone soil moisture)**
- Provider: NASA Goddard Earth Sciences Data and Information 
  Services Center (GES DISC)
- Variables: ET, PET, RZSM (April–October, 1980–2014)
- Access: https://gmao.gsfc.nasa.gov/reanalysis/MERRA-2/
- Registration required (free NASA Earthdata account)

**Landsat Surface Reflectance (NDVI)**
- Provider: U.S. Geological Survey (USGS)
- Sensors: Landsat 5 TM and Landsat 7 ETM+ 
  (16-day composites, 1985–2014)
- Access: https://earthexplorer.usgs.gov/
- Registration required (free USGS EarthExplorer account)

**Wildlife Management Area Boundaries**
- Mississippi WMA boundaries: Mississippi Department of 
  Wildlife, Fisheries and Parks (MDWFP)
  https://www.mdwfp.com/
- Idaho WMA boundaries: Idaho Department of Fish and Game (IDFG)
  https://idfg.idaho.gov/

## How to Use This Code

1. Download MERRA-2 ET, PET, and RZSM data for your study period
2. Download Landsat NDVI composites for your study area
3. Obtain boundary shapefiles for your study units
4. Edit the CONFIGURATION block at the top of the script:
   - Set file paths to your downloaded data
   - Define your study units and shapefiles
   - Adjust temporal settings if needed
5. Run: `python detecting_flashdrought_ecological_impact.py`

## Requirements
Python >= 3.8
numpy
pandas
scipy
netCDF4
geopandas
shapely
## Citation
If you use this code, please cite:

Ongondo, F. (2026). Flash drought detection and vegetation stress 
response in Wildlife Management Areas. *Remote Sensing of Environment* 
(under review).

And the original framework:

Christian, J.I., et al. (2019). A methodology for flash drought 
identification. *Journal of Hydrometeorology*, 20(5), 833–846.

## License
MIT — see LICENSE file
