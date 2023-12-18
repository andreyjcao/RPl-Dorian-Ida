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
