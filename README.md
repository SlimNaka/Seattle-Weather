##Seattle vs. NYC Rain Battle

The purpose of this project is to hopefully prove to my friend up who lives in Queens and always complains about how rainy Seattle is from his one visit in late November.

Data:
We will use daily precipitation measured in Seattle and New York from January 1, 2020 to January 1, 2024.
The data sets were downloaded from the National Centers for Environmental Information Online search tool: https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND.
The data sets seattle_rain.csv and ny_rain.csv can be accessed from the weather folderLinks in the DATA 3320 Github repository: https://github.com/galenegan/DATA-3320/tree/main/weather.
You can also consult the data documentation: https://www.ncei.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf.

Data prep: Seattle_Weather.ipynb

I deleted all columns EXCEPT station number, name, precipitation, and date and changed the latter column's type to datetime.

I then took the average amount of rainfall per day for both cities and joined the dataframes, keeping date and precipitation.

I then tidied the newly joined dataframe, by "melting" to include columns "DATE", "CITY", and "PRCP".

I then renamed the entries in the "CITY" column to be "NYC" or "SEA" and made all columns to be lowercase.

Clean data: clean_seattle_nyc_weather.csv
