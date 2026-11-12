# econ3916-midterm-project-econometric-foundation

# Does Paying More For College Help You Earn More In the Future?
ECON 3916 Midterm Project - Lily Wang

## The Question
Among US colleges that mainly award bachelor's degrees, how much of the variation in median earnings of federal-aid recipients 10 years after entry in the 2009-2011 cohort is associated with net price after accounting for selectivity and share of undergrads receiving Pell grant?

## Data Sources
All data comes from the US Department of Education, plus one CPI dataset from FRED for price conversions

- **Earnings and current school data:** 'Most-Recent=Cohorts-Instituion.csv', originally from https://collegescorecard.ed.gov/data/. The data was downloaded 10-26-2026. The original file has 6,278 rows and 3,379 columns, but the file was too large so I kept a few useful columns and saved the modified version as 'Most-Recent-Cohorts-Institution-modified.csv' in Github.
- **Net price, admission rate, Pell share, sector for 2010:** 'MERGED2010_11_PP.csv', also from the College Scorecard's historical data files. Also saved a trimmed version on here.
- **Price index:** CPI-U for all items ('CPIAUCNS.csv') from FRED, https://fred.stlouisfed.org/series/CPIAUCNS.
- **Column definitions & cohort years:** 'CollegeScorecardDataDctionary.xlsc', from the scorecard's documentation page; a copy is saved here.

One row is one institution, and the two files are joined on 'UNITID'. 


## How to run
1. Open 'ECON3916 Midterm Project Econometric Foundation.ipynb' in Google Colab. Upload the csv files needed to your google drive - it mounts Google Drive.
2. Run the cells from top to bottom, and read text cell interpretations and explanations in between


## Headline finding
A school with $1,000 higher net price (in 2022 dollars) has about 0.5% higher median earnings, with a 95% confidence interval of roughly 0.3% to 0.7% (n=1,422 schools). Without adding any controls, the association is about double that at 1.1%, so other confounding factors contribute to that effect. This is a conditional association rather than the effect of raising a school's price; other factors that haven't been incorporated, such as program mix or regional differences may also be factors that we want to control for potentially. 

