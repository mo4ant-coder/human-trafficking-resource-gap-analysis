# Data Dictionary

## Final Gap Analysis Dataset

**File:** `final_gap_analysis_fy2024.csv`

This dataset combines 2024 National Human Trafficking Hotline reporting data, U.S. Census population and socioeconomic data, and OVC-funded award data. It is the primary analytical dataset used in the resource-gap analysis.

| Column | Description |
|---|---|
| `state` | State or jurisdiction name |
| `state_abbr` | Two-letter state or jurisdiction abbreviation |
| `signals_received` | Number of signals received by the National Human Trafficking Hotline |
| `cases_identified` | Number of trafficking cases identified by the Hotline |
| `victims_involved` | Number of victims involved in identified cases |
| `population` | Estimated 2024 population |
| `cases_per_100k` | Identified Hotline cases per 100,000 residents |
| `median_household_income` | Median household income from the 2024 ACS 5-year estimates |
| `poverty_rate` | Percentage of the population below the poverty level |
| `unemployment_rate` | Unemployment rate |
| `ovc_organizations` | Number of organizations receiving qualifying OVC trafficking-related awards |
| `ovc_awards` | Number of qualifying OVC trafficking-related awards |
| `total_award_amount` | Total award value associated with the qualifying OVC awards |
| `organizations_per_1m` | OVC-funded organizations per 1 million residents |
| `awards_per_1m` | OVC-funded awards per 1 million residents |
| `cases_per_funded_organization` | Identified Hotline cases divided by the number of OVC-funded organizations |
| `resource_position` | Classification based on reported case rate and OVC-funded organizational density |
| `resource_pressure_signal` | Indicates whether a jurisdiction falls into both the higher-reporting and lower-resource-density thresholds |

## Derived Measures

### Cases per 100K residents

Calculated as:

`identified cases / population × 100,000`

This measure adjusts reported case counts for population size so jurisdictions of different sizes can be compared more directly.

### Organizations per 1M residents

Calculated as:

`OVC-funded organizations / population × 1,000,000`

This measures the density of qualifying federally funded organizations relative to population.

### Awards per 1M residents

Calculated as:

`OVC-funded awards / population × 1,000,000`

This provides additional context on the distribution of federally funded awards.

### Cases per Funded Organization

Calculated as:

`identified cases / OVC-funded organizations`

This is a secondary descriptive measure. It is not interpreted as the number of cases handled by each organization because the data do not establish which organizations served which cases.

### Resource Pressure Signal

A jurisdiction receives a potential resource-pressure signal when it meets both conditions:

- Reported Hotline case rate is in the upper quartile.
- OVC-funded organizational density is in the lower quartile.

This is a screening measure for further investigation and should not be interpreted as proof of inadequate services.

## Data Sources

### National Human Trafficking Hotline

State-level 2024 reporting data.

https://humantraffickinghotline.org/en/statistics

### U.S. Census Bureau

2024 American Community Survey 5-year estimates.

Population and socioeconomic measures were retrieved through the Census API.

https://www.census.gov/data/developers/data-sets/acs-5year/2024.html

### Office for Victims of Crime / USAspending

Federal award data for trafficking-related OVC programs, including Assistance Listing numbers 16.320 and 16.035.

https://www.ovc.ojp.gov/program/human-trafficking/grants-funding

https://www.usaspending.gov/

## Important Interpretation Notes

The National Human Trafficking Hotline data represent reported activity and identified cases, not the prevalence of human trafficking.

The OVC-funded organization measure represents federally funded organizations captured through the selected award programs. It is not a complete inventory of trafficking service providers.

The analysis identifies potential patterns for further investigation and does not establish causation, service shortages, or unmet need.