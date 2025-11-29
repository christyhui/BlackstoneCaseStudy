# BlackstoneCaseStudy

This project is an attempt to simulate what Blackstone Data Scientists may do when trying to evaluate county-level residential property markets in California for purchase and development.

The goal is to identify counties with high growth potential and positive market trends.

Project currently utilizes the data included in the table below:

## Data Sources

| Dataset | Source / Link | Description | Notes |
|---------|---------------|-------------|-------|
| ACS 5-Year Demographics | \[U.S. Census](https://www.census.gov/programs-surveys/acs/) | County-level population, age, race, income, education, housing | Pulled via Census API; cleaned and aggregated to county level |
| LODES RAC/WAC | \[LEHD](https://lehd.ces.census.gov/data/) | County-level employment by residence (RAC) and workplace (WAC) | Aggregated from block-level to county; 2018–2022 |
| IRS Migration | \[IRS](https://www.irs.gov/statistics/soi-tax-stats-migration-data) | County-to-county inflow/outflow, adjusted gross income (AGI) | Used to measure population movement trends; combined all years into single dataframe |
| Housing Affordability Index (HAI) | \[CAR](https://www.car.org/marketdata/data) | Percentage of households able to afford median-priced home | Quarterly data; only last 5 years used; removed aggregate regions like "LA Metro" |
| Median Home Prices | \[CAR](https://www.car.org/marketdata/data) | Median price of existing detached homes | Monthly data; currency symbols cleaned; converted to float |
| Median DOM (Days on Market) | \[CAR](https://www.car.org/marketdata/data) | Historical median days on market for existing detached homes | Monthly data; cleaned and converted to numeric |
| Unsold Inventory Index (UII) | \[CAR](https://www.car.org/marketdata/data) | Index measuring supply-demand balance of single-family homes | Monthly data; merged with other datasets for analysis |



