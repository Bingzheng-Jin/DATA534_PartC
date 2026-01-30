# DATA534_PartC
Individual contribution: Part C (standardize + filter)

# DATA 534 – Part C Contribution

This repository contains my **individual contribution** to the DATA 534 group project.

## Scope (Part C only)
Part C focuses on **data cleaning and standardization**, including:

- `mw_standardize()`: standardize raw WDS-like data into a tidy structure
- `mw_filter()`: convenient filtering by province, indicator keyword, and year range

> This repository intentionally includes **Part C only** for contribution tracking.

## Files
- `R/mw_standardize.R`
- `R/mw_filter.R`

## Quick test

```r
raw_df <- data.frame(
  GEO = c("British Columbia", "Ontario"),
  REF_DATE = c("2019", "2020"),
  VALUE = c("12.3", "10.5"),
  stringsAsFactors = FALSE
)

std <- mw_standardize(raw_df)
mw_filter(std, province = "Ontario")
