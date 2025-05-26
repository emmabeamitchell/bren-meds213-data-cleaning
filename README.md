# Cleaning the shorebird survey data 


## The data set

ARCTIC SHOREBIRD DEMOGRAPHICS NETWORK [https://doi.org/10.18739/A2222R68W](https://doi.org/10.18739/A2222R68W)

Data set hosted by the [NSF Arctic Data Center](https://arcticdata.io) data repository 

Field data on shorebird ecology and environmental conditions were collected from 1993-2014 at 16 field sites in Alaska, Canada, and Russia.

![Shorebird, copyright NYT](https://static01.nyt.com/images/2017/09/10/nyregion/10NATURE1/10NATURE1-superJumbo.jpg?quality=75&auto=webp)

Data were not collected every year at all sites. Studies of the population ecology of these birds included nest-monitoring to determine the timing of reproduction and reproductive success; live capture of birds to collect blood samples, feathers, and fecal samples for investigations of population structure and pathogens; banding of birds to determine annual survival rates; resighting of color-banded birds to determine space use and site fidelity; and use of light-sensitive geolocators to investigate migratory movements. 

Data on climatic conditions, prey abundance, and predators were also collected. Environmental data included weather stations that recorded daily climatic conditions, surveys of seasonal snowmelt, weekly sampling of terrestrial and aquatic invertebrates that are prey of shorebirds, live trapping of small mammals (alternate prey for shorebird predators), and daily counts of potential predators (jaegers, falcons, foxes). Detailed field methods for each year are available in the `ASDN_protocol_201X.pdf` files. All research was conducted under permits from relevant federal, state, and university authorities.

See `01_ASDN_Readme.txt` provided in the [course data repository](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-spring-2024-class-data) for full metadata information about this data set.

### Purpose 
The purpose of this repository is to practice data cleaning and metadata creation for the `ASDN_Snow_survey.csv` data. 

### File Structure

```
├── README.md
├── .gitignore
├── data-cleaning-class-example.qmd
├── eds213_data_cleaning_assign_Emma_Bea_Mitchell.qmd
├── data-cleaning.qmd   # Updated for data cleaning
├── data-cleaning_empty.qmd # Inclass data cleaning
└── data/
    ├── processed/                                          # Processed data/
    │   ├── snow_survey_fixed.csv                           # Inclass cleaned snow survey data
    │   └── snow_cover.csv                                  # Partially cleaned snow survey data
    │   └── species_present.csv                             # Species identified at site
    │   └── all_cover_fixed_EMMA_BEA_MITCHELL.csv           # Cleaned snow survey data for HW (all covers cleaned)
    └── raw/                                                # unprocessed data/
        ├── 01_ASDN_Readme.txt                              # Original metadata
        ├── ASDN_Daily_Species.csv                          # Species survey data
        └── ASDN_Snow_Survey                                # Snow cover survey data
```
Other data related data not contained within this repository are the following: `Bird_captures`, `Bird_eggs`, `Bird_nests`, `Bird_resights`, `Bird_sexes`, `Camp_info`, `Camp_assignment`, `Daily_pred_lemm`, `Daily_species`, `Daily_species_effort`, `Geodata`, `Inverts`, `Lemming_counts`,  `Lemming_nests`, `Lemming_trap`, `Pred_nests`, `Pred_point_counts`, `Study_Plot`, `Surface_water`, `Weather_HOBO`, `Weather_precip_manual`, `Weather_snow_manual`. This data can be found at this [link](https://arcticdata.io/catalog/view/doi:10.18739/A2222R68W). Other versions of the data exist in processing from the MEDS EDS-213 GitHub Repository: [bren-meds213-data-cleaning](https://github.com/UCSB-Library-Research-Data-Services/bren-meds213-data-cleaning)

#### Metadata
Metadata for the `all_cover_fixed_EMMA_BEA_MITCHELL.csv` file in this repository is as follows:

**Number of variables:** 11

**Number of rows:** 42,830

| Variable         | Description                        | Value               |
|---------------|------------------------------------|-----------------------|
| Site          | Four letter abbreviation for where data were collected                | Character      |
| Year        | Year data was collected          | Numeric                |
| Date          | Date data was collected        | Character |
| Plot       | Four letter abbreviation for where data was collected within each Site                      | Character  |
| Location  | Where data was collected within Each Plot                | Character            |
| Snow_cover         | Percent of snow cover                         | Numeric               |
| Water_cover          | Percent of water cover               | Numeric      |
| Land_cover        | Percent of land cover          | Numeric                |
| Observer          | Person who collected the data       | Character  |
| Notes       | Any notes by the Observer                      | Character   |
| Total_cover  | Total amount of cover (should always equal 100)              | Numeric           |

**Missing Data:** Missing data are written as NAs. For `Total_cover`, NAs are present in `Snow_cover`, `Water_cover`, `Land_cover`, 'Notes'

**No specialized formatting for this data**

### Sharing/Access Information:

#### Licenses/restrictions placed on the data:
The original data is licensed under the Creative Commons Attribution 4.0 International License. To view a copy of this license, visit http://creativecommons.org/licenses/by/4.0/.

#### Links to publications that cite or use the data:
[Annual adult survival drives trends in Arctic-breeding shorebirds but knowledge gaps in other vital rates remain](https://academic.oup.com/condor/article/122/3/duaa026/5857122)
[Life-history tradeoffs revealed by seasonal declines in reproductive traits of Arctic-breeding shorebirds](https://www.researchgate.net/publication/320616760_Life-history_tradeoffs_revealed_by_seasonal_declines_in_reproductive_traits_of_Arctic-breeding_shorebirds)
[Environmental and ecological conditions at Arctic breeding sites have limited effects on true survival rates of adult shorebirds](https://bioone.org/journals/the-auk/volume-135/issue-1/AUK-17-107.1/Environmental-and-ecological-conditions-at-Arctic-breeding-sites-have-limited/10.1642/AUK-17-107.1.full)

#### Links to other publicly accessible locations of the data:
Information for this data can be found on the NSF Arctic Data Center website [here](https://arcticdata.io/catalog/view/doi%3A10.18739%2FA2CD5M)

#### Project Citation must cite EDS-213 and Emma Bea Mitchell
