#
Seattle vs. NYC: Who Has More Rain?

##Authors:
Sean Nakagomi, instructed by Dr. Galen Egan

##Requirements:
This project was created using Python via Google Colab.

##Introduction:
The purpose of this project is to hopefully prove to my friend who lives in Queens, NYC that Seattle is not as rainy as popularly believed, and that it is comparable to NYC, perhaps even raining less than the Big Apple.

##Data:
We will use daily precipitation measured in Seattle and New York from January 1, 2020 to January 1, 2024.
The data sets were downloaded from the National Centers for Environmental Information Online search tool: https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND.
The data sets seattle_rain.csv and ny_rain.csv can be accessed from the weather folderLinks in the DATA 3320 Github repository: https://github.com/galenegan/DATA-3320/tree/main/weather.
You can also consult the data documentation: https://www.ncei.noaa.gov/pub/data/cdo/documentation/GHCND_documentation.pdf.

##Data prep: Seattle_Weather.ipynb

I deleted all columns EXCEPT station number, name, precipitation, and date and changed the latter column's type to datetime.

I then took the average amount of rainfall per day for both cities and joined the dataframes, keeping date and precipitation.

I then tidied the newly joined dataframe, by "melting" to include columns "DATE", "CITY", and "PRCP".

I then renamed the entries in the "CITY" column to be "NYC" or "SEA" and made all columns to be lowercase.

Clean data: clean_seattle_nyc_weather.csv


##Data analysis: Seattle_NYC_Analysis

Used the 5 number summary of each city to see which city had the most rainfall in our 4-year time period.

Created a graph of both cities to see the number of inches of rain each city received over time.

Looked at how many times each city received the following: 0 inches, greater than 0.5 inches, greater than 1 inch, and between 0.01 and 0.25 inches.

Created two histograms, one focusing on non-zero precipitation values and one focusing solely on non-zero precipitation values.

##Licence:
MIT License

Copyright (c) 2024 Sean Nakagomi

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
