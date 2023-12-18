---
title: "cao-preanalysis"
author: "Andrey Cao"
date: "2023-12-7"
output: html_document
editor_options: 
  markdown: 
    wrap: sentence
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## Authors

-   Andrey (Andy) Cao, [acao\@middlebury.edu](mailto:acao@middlebury.edu){.email}, [\@andreyjcao](https://github.com/andreyjcao), Middlebury College (Class of 2025)

## Abstract

This original [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler) examines the impacts of natural disasters on social media communication.
Focusing on X/Twitter data during Hurricane Dorian, Holler (2021) replicated the methods of Wang et al (2016) for the case of the hurricane's landfall on the U.S. mainland during the 2019 Atlantic Hurricane season.
Holler modified the methodology for normalizing tweet data by creating a normalized Tweet difference index and extended the methodology to test for spatial clustering with the local Getis-Ord statistic.
This replication of Holler (2021) conducted by Cao (2023) examines X/Twitter data during Hurricane Ida in 2021.
As a replication study, we aimed to successfully generate the figures and type of results produced in Holler (2021) with Hurricane Ida data.
We found differences in the computational environment that made packages such as 'rtweet' not compatible with the code of Holler (2021).
Additionally, the new lack of free access to X/Twitter data led us to alter the normalization of the data to use data from the Census API.

This study is a replication of this [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler)

### Study metadata (Hurricane Ida)

-   `Key words`: hurricane, ida, twitter, x
-   `Subject`: Social and Behavioral Sciences: Geography: Geographic Information Sciences
-   `Date created`: Replication started November 16, 2023
-   `Date modified`: December 13, 2023
-   `Spatial Coverage`: continental United States
-   `Spatial Resolution`: GPS coordinates
-   `Spatial Reference System`: NAD 1983
-   `Temporal Coverage`: 2021-08-29 to 2021-9-10
-   `Temporal Resolution`: Tweets are measured to the second (formatted as 'day hour:minute:second')
-   `Funding Name`: n/a
-   `Funding Title`: n/a
-   `Award info URI`: n/a
-   `Award number`: n/a

#### Original study spatio-temporal metadata (Hurricane Dorian data)

-   `Spatial Coverage`: continental United States
-   `Spatial Resolution`: GPS coordinates
-   `Spatial Reference System`: NAD 1983
-   `Temporal Coverage`: 2019-09-05 to 2019-09-10
-   `Temporal Resolution`: Tweets are measured to the second (formatted as 'day hour:minute:second')

## Study design

This is a replication of this [study of Hurricane Dorian](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler).
The original study archetype was observational, as it was comparing X/Twitter data for the trending news surrounding #Sharpiegate and Hurricane Dorian.

Holler (2021) focused on the research question surrounding whether the trending news and social media content (#Sharpiegate) regarding a false narrative of risk would cluster along the real hurricane (Dorian) track. 
Using a temporal analysis graph, a content analysis graph, a map of X/Twitter activity, and a hotspot map, Holler (2021) visualizes patterns of the observed tweets. 

## Materials and procedure

### Computational environment

This replication along with the study uses R and a variety of packages including:
"here", "svDialogs", "tidyverse", "tidytext", "tm", "igraph", "ggraph", 
"tidycensus", "sf", "spdep", "remote", and "rtweet."

To recreate the computational environment of Holler (2021), we used an R package
called "groundhog." Click [here](https://groundhogr.com/) to learn more. 

We also used the Census API for the new normalization. 
Click [here](https://www.census.gov/data/developers/data-sets.html) to learn more.

### Data and variables

Since the X/Twitter API is no longer accessible for free, we used older tweet
files that must remain private due to Twitter privacy regulations.
Contact [Professor Joseph Holler](https://github.com/josephholler) if you are
interested in getting access to these files.

#### Primary data (tevent_raw.RDS, tevent_raw2.RDS, tevent_raw3.RDS, tevent_raw4.RDS)

**Standard Metadata**

- `Title`: X/Twitter Data (Hurricane Ida)
- `Abstract`: Tweet data during Hurricane Ida (2021)
- `Spatial Coverage`: continental United States
- `Spatial Resolution`: GPS coordinates
- `Spatial Reference System`: NAD 1983
- `Temporal Coverage`: 2021-08-29 to 2021-09-10
- `Temporal Resolution`: Tweets are measured to the second (day hour:minute:second)
- `Lineage`: The data files were made using the X/Twitter API. Though the code to retrieve the data is within the study, new regulations of the API prevent that code from working. 
- `Distribution`: Cannot be distributed publicly, contact [Professor Joseph Holler](https://github.com/josephholler) for access
- `Constraints`: Legal constraints for privacy, X/Twitter data cannot be distributed publicly for user privacy
- `Data Quality`: n/a
- `Variables`: Here are the variables used within the study (out of a total of 90 variables)

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| status_id | unique status identifier | ID number for each status | character | ... | 1431923022718459904 to 1436353772679204866 | ... | no missing data |
| created_at | time of tweet | post time measured as (day hour:minute:second) | character | to the second | (2021-08-29 10:13:47) to (2021-09-10 15:40:00) | ... | no missing data |
| text | text of tweet | any characters contained within tweet | character | ... | ... | ... | no missing data |
| place_type | place type of tweet location | X/Twitter geographic place type | character | based on X/Twitter categorization | city, neighborhood, poi, or NA | NA | about 94.79% of place_type missing |
| coords_coords | coordinates | coordinates in a (x,y) format | list of numbers | ... | ... | c(NA, NA) | about 99.55% of coords_coords missing |
| bbox_coords | bounding box coordinates | eight coordinates that form edges of a region | list of numbers | ... | ... | c(NA, NA, NA, NA, NA, NA, NA, NA) | about 94.79% of bbox_coords missing |

### Prior observations

At the time of this preanalysis, we have obtained the full X/Twitter data we
are going to use for this study. We have no prior conception of the potential 
results that will come from this set of Hurricane Ida data except for brief
research on the path of the hurricane. Our main objective of this replication
is to use this data and successfully produce the figures featured in the original code. 

### Bias and threats to validity

The different normalization method (using Census API instead of X/Twitter data)
may make it harder for us to compare certain figures to the original study.
Additionally, the hotspot/cluster figure of the study may be affected by the
modifiable areal unit problem, so we should be aware of the state population data
we use during the normalization process. 

### Data transformations

Starting from the raw files, we will bind the four files (rbind function) and
then sort out the duplicates (distinct function).
Then we will convert geographic information into lat/long coordinates.
After, we will clean the text and parse out any stop words we would like to exclude.

Later, for the normalization, we must first add the county data.
Then, we will join the tweets to the county data. 
Lastly, we will create the spatial weight matrix along with the Getis-Ord G* Statistic.

## Analysis

We will conduct a replication study of the Dorian Twitter study using data from Hurricane Ida.
One objective of this replication is to adjust the computational environment in
case any of the packages have updated and are no longer usable with the code from
Holler (2021). Another main objective of this replication is to adjust the 
normalization process to use Census data rather than X/Twitter data. With these
improvements and modifications, the Hurricane Ida tweet data should produce 
four figures. Lastly, I will explain the replication with a discussion and 
conclusion section after the analysis. 

## Results

The computational environment adjustments will be in the first section of the code
and should be quite similar to the original Holler (2021) study other than the 
addition of the groundhog package. 
The normalization adjustment will affect the figure titled 'NDTI map,' as the
figure will reflect a weighting based on Census data. 
The discussion and conclusion will provide a thorough explanation of the
modifications along with explanation of unplanned deviations. 

## Discussion

If the adjustments to the computational environment are successful, then the code
should work with the Hurricane Ida with few adjustments to the rest of the code.
The new normalization should showcase results that are weighted using Census
population data and make it so Hurricane Ida data can be weighted without additional
X/Twitter data. 
The discussion and conclusion should help future researchers to understand our
modifications in this replication along with the context of the original study. 

## Integrity Statement

The authors of this preregistration state that they completed this preregistration to the best of their knowledge and that no other preregistration exists pertaining to the same hypotheses and research.

## Acknowledgements

This report is based upon the template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences, [DOI:[10.17605/OSF.IO/W29MQ](DOI:%5B10.17605/OSF.IO/W29MQ){.uri}](<https://doi.org/10.17605/OSF.IO/W29MQ>)

## References

This study is a replication of this [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler)
