# Data Cleaning

## Duplicate Records

- Identified 312 exact duplicate business records with different Row IDs in the Sales dataset.
- Removed exact duplicates from the clean dataset while preserving the raw data.
- Removed Row ID from the clean analytical dataset since it holds no business value after duplicate validation.

## Missing Values

- Checked missing values across all columns.
- Removed the `parent_zcta` column from the US Zips working dataset because the entire column contains missing values.
- Identified 17 missing values in both the population and density fields of the US Zips dataset.
- Excluded these 17 records from population-based analysis.

## Date Validation

- Identified critical anomalies in the Sales Ship Date field.
- Found ship dates are 2,000–3,431 days after order dates (Order years 2021–2024 vs Ship years 2026–2030).
- Excluded Ship Date from shipping-performance and shipping-duration analysis because the timeline is unreliable.
- Retained the original raw values in the source data.

## Data Validation

- Reviewed 194 records in the Geographic lookup that could not be matched to the US Zips reference table.
- Left the Latitude, Longitude, and County fields blank rather than inferring data, as this unmatched information is no longer useful.
