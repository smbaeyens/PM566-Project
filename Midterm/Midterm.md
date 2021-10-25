Midterm
================
Sylvia Baeyens
due 10/22/2021

## Introduction

(provide background on your dataset and formulated question)

## Methods

In order to answer the main question, multiple datasets were acquired
from various sources. The data can be organized into 3 categories:
anemia data, meat consumption data, and country data.

# Anemia Data

The data sets related to the prevalence of anemia in 15-49 year old
women in low and middle income countries (LMIC) were exported from
ghdx.healthdata.org. This data was collected by the Institute of Health
Metrics and Evaluation with the funding from the Bill and Melinda Gates
Foundation between January 2000 and December 2019. It was published in
2021. There were three different csv files in this set, one for mild
anemia, one for moderate anemia, and one for severe anemia. The data
sets detailed the prevalence of each kind of anemia every year in 82
LMICs at a 5x5km level. These csv’s were downloaded from the site
manually and read into data tables in the R code. From there, variable
names were changed to improve ease of merging. Instead of keeping the
data at the 5x5km level, the mean anemia prevalence was found by country
and year. Finally, the three data tables (moderate, mild, and severe)
were merged into the data table “TotalAnemia”. This table included all
82 countries and the mild, moderate, and severe percentages of anemia
prevalence for every year from 2000 to 2019. No values were found to be
missing or unreasonable.

# Meat Consumption Data

The data set related to meat food supply quantity in terms of kilograms
per capita per year was exported from ourworldindata.org. This data was
sourced from data published by the United Nations Food and Agricultural
Organization (FAO) in 2020. The data was collected from 1961 to 2017.
This csv file was also exported manually from the website and read into
a data table within the R code. It contains data from 215 countries and
was not found to have any missing values. The data only had 4 variables:
the country name, 3 letter country code, year, and meat food supply
quantity; these variables were renamed for ease of use and to match the
names of the anemia data table.

# country data & final data table

Following preliminary data cleanup and wrangling, the TotalAnemia and
meatData data tables were merged together by country and year to create
a new data table: TotalData. All observations from the TotalAnemia data
table were kept. To add a final level of analysis, a country code data
set was downloaded and read in by the R code. This csv file was found on
datahub.io, and lists every country, along with its three letter country
code, continent, and other identifying information; only the three
letter code and continent were selcted for. This country code data set
was then merged with the TotalData set by code, so that every
observation now included the continent as well.

Final data cleanup and wrangling was now performed. Any observations
missing meat consumption values were removed. The data table was now
left with data for 69 LMICs, for a total of 1258 observations. When
looking at summaries and visualizations of the various variables, no
data looked unreasonable. The results of these summary statistics are
printed below:

## Preliminary Results

(provide summary statistics in tabular form and publication-quality
figures, take a look at the kable function from knitr to write nice
tables in Rmarkdown)

## Conclusion
