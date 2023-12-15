---
title: "cao-preanalysis"
author: "Andrey Cao"
date: "2023-12-7"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

### Authors

- Andrey (Andy) Cao, acao@middlebury.edu, [@andreyjcao](https://github.com/andreyjcao), Middlebury College (Class of 2025)

### Abstract

*Write a brief abstract about your research project.*

This study is a replication of this [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler)


### Study metadata (Hurricane Ida)

- `Key words`: hurricane, ida, twitter, x
- `Subject`: Social and Behavioral Sciences: Geography: Geographic Information Sciences
- `Date created`: Replication started November 16, 2023
- `Date modified`: December 13, 2023
- `Spatial Coverage`: continental United States
- `Spatial Resolution`: GPS coordinates
- `Spatial Reference System`: NAD 1983
- `Temporal Coverage`: 2021-08-29 to 2021-9-10
- `Temporal Resolution`: Tweets are measured to the second (formatted as 'day hour:minute:second')
- `Funding Name`: n/a
- `Funding Title`: n/a
- `Award info URI`: n/a
- `Award number`: n/a

#### Original study spatio-temporal metadata (Hurricane Dorian data)

- `Spatial Coverage`: continental United States
- `Spatial Resolution`: GPS coordinates
- `Spatial Reference System`: NAD 1983
- `Temporal Coverage`: 2019-09-05 to 2019-09-10
- `Temporal Resolution`: Tweets are measured to the second (formatted as 'day hour:minute:second')

## Study design

Describe how the study relates to prior literature, **replication study**

Also describe the original study archetype, e.g. is it **observational**, **experimental**, **quasi-experimental**, or **exploratory**?

Enumerate specific **hypotheses** to be tested or **research questions** to be investigated here, and specify the type of method, statistical test or model to be used on the hypothesis or question.

## Materials and procedure

### Computational environment

Define the hardware, operating system, and software requirements for the research.
Include citations to important software projects, plugins or packages and their versions.

### Data and variables

Describe the **data sources** and **variables** to be used.
Data sources may include plans for observing and recording **primary data** or descriptions of **secondary data**.
For secondary data sources with numerous variables, the analysis plan authors may focus on documenting only the variables intended for use in the study.

Primary data sources for the study are to include ... .
Secondary data sources for the study are to include ... .

Each of the next subsections describes one data source.

#### Primary data (tevent_raw.RDS, tevent_raw2.RDS, tevent_raw3.RDS, tevent_raw4.RDS)

**Standard Metadata**

- `Abstract`: Tweet data during Hurricane Ida (2021)
- `Spatial Coverage`: continental United States
- `Spatial Resolution`: GPS coordinates
- `Spatial Reference System`: NAD 1983
- `Temporal Coverage`: 2021-08-29 to 2021-09-10
- `Temporal Resolution`: Tweets are measured to the second (day hour:minute:second)

- `Lineage`: Describe and/or cite data sources and/or methodological steps planned to create this data source.
  - sampling scheme, including spatial sampling
  - target sample size and method for determining sample size
  - stopping criteria for data collection and sampling (e.g. sample size, time elapsed)
  - de-identification / anonymization
  - experimental manipulation
  
- `Distribution`: Cannot be distributed publicly, contact [Professor Joseph Holler](https://github.com/josephholler) for access
- `Constraints`: Legal constraints for privacy, X/Twitter data cannot be distributed publicly for user privacy
- `Data Quality`: n/a
- `Variables`:

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| variable1 | ... | ... | ... | ... | ... | ... | ... |
| variable2 | ... | ... | ... | ... | ... | ... | ... |


### Prior observations  

Prior experience with the study area, prior data collection, or prior observation of the data can compromise the validity of a study, e.g. through p-hacking.
Therefore, disclose any prior experience or observations at the time of study pre-registration here, with example text below:

At the time of this study pre-registration, the authors had _____ prior knowledge of the geography of the study region with regards to the ____ phenomena to be studied.
This study is related to ____ prior studies by the authors

For each primary data source, declare the extent to which authors had already engaged with the data:

- [ ] no data collection has started
- [ ] pilot test data has been collected
- [ ] data collection is in progress and data has not been observed
- [ ] data collection is in progress and __% of data has been observed
- [ ] data collection is complete and data has been observed. Explain how authors have already manipulated / explored the data.

For each secondary source, declare the extent to which authors had already engaged with the data:

- [ ] data is not available yet
- [ ] data is available, but only metadata has been observed
- [ ] metadata and descriptive statistics have been observed
- [ ] metadata and a pilot test subset or sample of the full dataset have been observed
- [ ] the full dataset has been observed. Explain how authors have already manipulated / explored the data.

If pilot test data has been collected or acquired, describe how the researchers observed and analyzed the pilot test, and the extent to which the pilot test influenced the research design.

### Bias and threats to validity

Given the research design and primary data to be collected and/or secondary data to be used, discuss common threats to validity and the approach to mitigating those threats, with an emphasis on geographic threats to validity.

These include:
  - uneven primary data collection due to geographic inaccessibility or other constraints
  - multiple hypothesis testing
  - edge or boundary effects
  - the modifiable areal unit problem
  - nonstationarity
  - spatial dependence or autocorrelation
  - temporal dependence or autocorrelation
  - spatial scale dependency
  - spatial anisotropies
  - confusion of spatial and a-spatial causation
  - ecological fallacy
  - uncertainty e.g. from spatial disaggregation, anonymization, differential privacy

### Data transformations

Starting from the raw files, we 

Describe all data transformations planned to prepare data sources for analysis.
This section should explain with the fullest detail possible how to transform data from the **raw** state at the time of acquisition or observation, to the pre-processed **derived** state ready for the main analysis.
Including steps to check and mitigate sources of **bias** and **threats to validity**.
The method may anticipate **contingencies**, e.g. tests for normality and alternative decisions to make based on the results of the test.
More specifically, all the **geographic** and **variable** transformations required to prepare input data as described in the data and variables section above to match the study's spatio-temporal characteristics as described in the study metadata and study design sections.
Visual workflow diagrams may help communicate the methodology in this section.

Examples of **geographic** transformations include coordinate system transformations, aggregation, disaggregation, spatial interpolation, distance calculations, zonal statistics, etc.

Examples of **variable** transformations include standardization, normalization, constructed variables, imputation, classification, etc.

Be sure to include any steps planned to **exclude** observations with *missing* or *outlier* data, to **group** observations by *attribute* or *geographic* criteria, or to **impute** missing data or apply spatial or temporal **interpolation**.

### Analysis

Describe the methods of analysis that will directly test the hypotheses or provide results to answer the research questions.
This section should explicitly define any spatial / statistical *models* and their *parameters*, including *grouping* criteria, *weighting* criteria, and *significance thresholds*.
Also explain any follow-up analyses or validations.

We will conduct a replication study of the Dorian Twitter study using data from Hurricane Ida.
One aspect of the 

Adjust the computational environment

bind RDS files to make replication easier

Change normalization process (census data instead of twitter data)

To better the reproducibility study of Malcomb (2014), I will be expanding the written analysis and more directly addressing discrepancies between the original study and the reproduction. 

My revision to the reproducibility study of Malcomb (2014) will prioritize adding the discussion, conclusion, and 'rationale for the updated report' sections. 
Adding these three sections at the end of the study will improve the understanding of the reproduction by describing the changes made, the reasoning behind each choice, as well as the results of each change. 
This will provide the most updated conclusions of the reproducibility study. 

In addition to more comprehensive written analysis of the reproduction, I will also address the confusion caused by the inconsistent figure labeling of the original study. 
In order to clearly represent the differences between the original study and the reproduction, I will add figures and comments to demonstrate the inconsistency with the figure labels.

## Results

The resulting replications should perform the 

The addition of a comprehensive discussion section will analyze each choice and deviation (along with the corresponding result) within the reproduction study and compare them to the original study.
The discussion section will also help explain the reasoning behind each choice/deviation.
The conclusion section will help to explain the significance of the reproduction while also addressing the study's effect on the broader scientific community. 
The rationale section will reiterate how the changes made in this version of the study improved the first reproduction of Malcomb (2014).  

Within the code, I will create figures based on the figure labels presented in the original study. 
With annotations, I will then note the discrepancies between the original labels and the figures of the original and the reproductions. 
The addition of figures and annotations will be accompanied by additions to the discussion section to strengthen clarity of the study.

## Discussion

Describe how the results are to be interpreted *vis a vis* each hypothesis or research question.

If the discussion, conclusion, and rationale sections showcase the changes, the results, and an understanding of the reproduction, then the study will have a more clear and organized analysis for future reproductions.
If the code and the discussion addresses the inconsistent labeling of the original study's figures, then the study will have a more direct explanation for the discrepancies between the original study and the equations used for the reproduction.


## Integrity Statement
The authors of this preregistration state that they completed this preregistration to the best of their knowledge and that no other preregistration exists pertaining to the same hypotheses and research.

If a prior registration *does* exist, explain the rationale for revising the registration here.

## Acknowledgements

This report is based upon the template for Reproducible and Replicable Research in Human-Environment and Geographical Sciences, DOI:[10.17605/OSF.IO/W29MQ](https://doi.org/10.17605/OSF.IO/W29MQ)

## References

This study is a replication of this [study](https://github.com/GIS4DEV/OR-Dorian) conducted by [Professor Joseph Holler](https://github.com/josephholler)

