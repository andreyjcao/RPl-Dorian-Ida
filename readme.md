# Replication of Holler (2021) Hurricane Dorian Twitter Study with Hurricane Ida Data

## Contributors

- Andrey Cao, acao@middlebury.edu, [@andreyjcao](https://github.com/andreyjcao), Middlebury College (Class of 2025)

## Abstract

This original [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler) examines the impacts of natural disasters on social media communication. 
Focusing on X/Twitter data during Hurricane Dorian, Holler (2021) replicated the methods of Wang et al (2016) for the case of the hurricane's landfall on the U.S. mainland during the 2019 Atlantic Hurricane season. 
Holler modified the methodology for normalizing tweet data by creating a normalized Tweet difference index and extended the methodology to test for spatial clustering with the local Getis-Ord statistic. 
This replication of Holler (2021) conducted by Cao (2023) examines X/Twitter data during Hurricane Ida in 2021. 
As a replication study, we aimed to successfully generate the figures and type of results produced in Holler (2021) with Hurricane Ida data. 
We found differences in the computational environment that made packages such as 'rtweet' not compatible with the code of Holler (2021). 
Additionally, the new lack of free access to X/Twitter data led us to alter the normalization of the data to use data from the Census API. 

This study is a replication of this [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler)

## Study Metadata

- `Key words`: hurricane, ida, twitter, x
- `Subject`: Social and Behavioral Sciences: Geography: Geographic Information Sciences
- `Date created`: 2023-11-16
- `Date modified`: 2023-12-15
- `Spatial Coverage`: United States
- `Spatial Resolution`: GPS coordinates
- `Spatial Reference System`: NAD 1983
- `Temporal Coverage`: 2021-08-29 to 2021-09-10
- `Temporal Resolution`: Tweets are measured to the second (formatted as 'day hour:minute:second')
- `Funding Name`: n/a
- `Funding Title`: n/a
- `Award info URI`: n/a
- `Award number`: n/a

## Compendium structure and contents

This research compendium is structured with four main directories:

- `data`: contains subdirectories for `raw` data and `derived` data.
- `docs`: contains subdirectories for `manuscript`, `presentation`, and `report`
- `procedure`: contains subdirectories for `code` or software scripts, information about the computational `environment` in which the research was conducted, and non-code research `protocols`
- `results`: contains subdirectories for `figures`, formatted data `tables`, or `other` formats of research results.

The data, procedures, and results of this repository are outlined in three tables:
- Data: [data/data_index.csv](data/data_index.csv)
- Procedures: [procedure/procedure_index.csv](procedure/procedure_index.csv)
- Results: [results/results_index.csv](results/results_index.csv)

Important local **documents** include:
- Pre-analysis plan: [docs/report/preanalysis.md](docs/report/preanalysis.md)
- Study report: [docs/report/report.pdf](docs/report/report.pdf)
- Manuscript: [docs/manuscript/manuscript.pdf](docs/manuscript/manuscript.pdf)
- Presentation: [docs/presentation/presentation.pdf](docs/presentation/presentation.pdf)

## References

This study is a replication of this [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler)

Wang, Z., X. Ye, and M. H. Tsou. 2016. Spatial, temporal, and content analysis of Twitter for wildfire hazards. *Natural Hazards* 83 (1):523–540. DOI:[10.1007/s11069-016-2329-6](https://doi.org/10.1007/s11069-016-2329-6).

#### Compendium reference

The [template_readme.md](template_readme.md) file contains more information on the design of this template and references used in the design.
The [Template_LICENSE](Template_LICENSE) file provides the BSD 3-Clause license for using this template.
> Kedron, P., & Holler, J. (2023). Template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences. [https://doi.org/10.17605/OSF.IO/W29MQ](https://doi.org/10.17605/OSF.IO/W29MQ)


