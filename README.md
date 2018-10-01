## Team Turnstile Jumpers - Project Benson

### Datasets
1. MTA Turnstile Data
   1. Downloaded data from: http://web.mta.info/developers/turnstile.html
      1. May 26, 2018 thru June 16, 2018, inclusive
      2. Documentations at: http://web.mta.info/developers/resources/nyct/turnstile/ts_Field_Description.txt
2. Google API Data
3. Census Data

### Tools
1. Python, Pandas, Matplotlib, Seaborn
2. Google API


### Notebooks in repo:
1. benson-data-cleaning.ipynb: handles importing and cleaning of MTA data
2. api-census-collection.ipynb: Gets geocodes for each station from Google Maps API. Also gets income tax data from U.S. 2016 Census. Merges the two sets of data to get the number of high income (>$100,000 / year) residents in the same zipcode as a subway station. 
3. benson-Hir.ipynb :calculation for median daily weekday to weekend traffic ratio
4. select_stations.ipynb: Filters subway stations on our criteria of weekday/weekend ratio, high income residents, and median daily traffic. Also makes final plots, including scatter plots and bar chart.
5. Heatmap.ipynb: plots heatmaps of chosen stations 
5. Appendix:
   - Appendix-EDA.ipynb: EDA that didn't make the final cut
   
### .csv files in repo:
1. 16zpallagi.csv: 2016 U.S. Census data containing zipcode and number of residents in that zipcode who earned over $100,000 in 2016.
2. Week_ratio.csv: Data from Pandas dataframe with ratio of median daily weekday traffic to median daily weekend traffic
3. filtered.csv: Our final list of stations
4. ny-zip-income.csv: 16zpallagi.csv filtered down to zipcodes in New York City, and columns containing data on zipcode, income range ('agi_stub'), and number of residents falling in to an income range.
5. pared_turnstile.csv: MTA turnstile data with zipcode, number of high income residents, and an engineered feature showing how much traffic a station experienced in a given four hour period.
6. raw_turnstile_data.csv: MTA turnstile data downloaded directly from the website. Four data files concatendated with no data cleaning done.
7. turnstile_data_by-station-day.csv: MTA turnstile data showing traffic summed over each day for each station.
8. zipcodes.csv: Subway station name, zipcode, and number of high income residents in the zipcode of each station.
  
