- `Title`: X/Twitter Data (Hurricane Ida)
- `Abstract`: Tweet data during Hurricane Ida (2021)
- `Spatial Coverage`: continental United States
- `Spatial Resolution`: GPS coordinates
- `Spatial Reference System`: NAD 1983
- `Temporal Coverage`: 2021-08-29 to 2021-09-10
- `Temporal Resolution`: Tweets are measured to the second (day hour:minute:second)
- `Lineage`: However, due to new restraints from X/Twitter API, we can no longer use this method for free. Nonetheless, here are some steps to how one may get the raw files. 
- 
- Describe and/or cite data sources and/or methodological steps taken or planned to create this data source, e.g.:
  - sampling scheme, including spatial sampling
  - target sample size and method for determining sample size
  - stopping criteria for data collection and sampling (e.g. sample size, time elapsed)
  - de-identification / anonymization
  - experimental manipulation
 
  - 
- `Distribution`: Cannot be distributed publicly, contact [Professor Joseph Holler](https://github.com/josephholler) for access
- `Constraints`: Legal constraints for privacy, X/Twitter data cannot be distributed publicly for user privacy
- `Data Quality`: n/a

- `Variables`: For each variable, enter the following information. If you have two or more variables per data source, you may want to present this information in table form (shown below)
  - `Label`: variable name as used in the data or code
  - `Alias`: intuitive natural language name
  - `Definition`: Short description or definition of the variable. Include measurement units in description.
  - `Type`: data type, e.g. character string, integer, real
  - `Accuracy`: e.g. uncertainty of measurements
  - `Domain`: Expected range of Maximum and Minimum of numerical data, or codes or categories of nominal data, or reference to a standard codebook
  - `Missing Data Value(s)`: Values used to represent missing data and frequency of missing data observations
  - `Missing Data Frequency`: Frequency of missing data observations: not yet known for data to be collected

| Label | Alias | Definition | Type | Accuracy | Domain | Missing Data Value(s) | Missing Data Frequency |
| :--: | :--: | :--: | :--: | :--: | :--: | :--: | :--: |
| status_id | unique status identifier | ID number for each status | character | ... | 1431923022718459904 to 1436353772679204866 | ... | no missing data |
| created_at | time of tweet | post time measured as (day hour:minute:second) | character | to the second | (2021-08-29 10:13:47) to (2021-09-10 15:40:00) | ... | no missing data |
| text | text of tweet | any characters contained within tweet | character | ... | ... | ... | no missing data |
| place_type | place type of tweet location | X/Twitter geographic place type | character | based on X/Twitter categorization | city, neighborhood, poi, or NA | NA | about 94.79% of place_type missing |
| coords_coords | coordinates | ... | ... | ... | ... | ... | ... |
| bbox_coords | bound box coordinates | ... | ... | ... | ... | ... | ... |
