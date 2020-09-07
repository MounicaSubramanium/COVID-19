# Gathering weather data for JHU's COVID19 infection data

<br>
<b>The CSV files of the weather data are in the './csv' directory</b><br>
<br>
Please consider sponsoring this project, as the API calls to gather the data points do cost money.<br>
Click on the 'Sponsor' button on the repository page to learn more.<br><br>
---<br>
<b>update 9/6/2020:</b> Added dates for the rest of August 2020.<br><br>
Also, data collection changed to gather data into a SQLite database, and then exporting to CSV,<br>
instead of writing directly to CSV files. This actually speeds up the runtime, as there is no longer a need to write<br>
files during runtime to save progress. If you want to see the database, it's in './sql/weather.db'.<br>
It's nothing fancy. It's just the different tables of the US and Global data points.<br>
Given this change, the more recently gathered data points have more significant figures, as there are now<br>
decimal points where there weren't before. <br><br>
A little housekeeping in trying to organize some of the workspace has been done, too. The Jupyter Notebooks<br>
used in this process have been moved to the './notebooks' directory. Also, in the './misc' folder, I've put<br>
a document where I've listed various papers/publications that I've found that reference the data here.<br>
---<br>
<b>update 8/29/2020:</b> Added CSV files for JHU's Global locations.<br>
Many of these locations are entire countries, so they probably aren't practically useful for many data analysis purposes. Please keep this in mind.<br>
---<br>
<b>update 8/15/2020:</b> It has been a number of months since I've done an update.<br>
JHU has two main timeline series: US and global.<br>
For right now, this update is for the US timeseries. Maybe sometime soon, I'll also do a global breakout. We'll see.<br>
I understand that some people have run some analyses on these data. Please see the note below regarding how some locations have inaccurate Latitude and Longitude (and therefore inaccurate weather data).<br>
Again, I mention that although this is a good faith effort on my part, none of my work has been reviewed or validated (at least to my knowledge).<br>
---<br>
<b>update 3/27/2020:</b> JHU has changed some of its grouping for certain regions and/or countries.<br>
I may start to manually break down some of the more significant regions in the US,<br>
Such as Seattle, NYC, etc, and elsewhere. I need to think about how I want to do this.<br>
---<br>
<br>
<br>
<b>The generated files with the weather data are in the './csv' directory</b><br>
This is all just raw data. I have not done any analysis yet.<br>

Weather data is very generously Powered by Dark Sky: https://darksky.net/poweredby/

JHU's time_series_19-covid-Confirmed.csv was taken, and repurposed it to get weather data for the dates and locations that are listed.

Please see https://darksky.net/dev/docs and/or https://github.com/imantsm/COVID-19/blob/master/csv/README.md for the meaning and unit of each value. Where applicable, units are pulled in SI units.

<b>The following csv files are generated in the './csv' folder:<br></b>
  tMax_US.csv       - pulling 'temperatureHigh' from API call<br>
  tMin_US.csv       - pulling 'temperatureLow' from API call<br>
  humidity_US.csv   - pulling 'humidity' from API call, and multiplying by 100<br>
  uv_US.csv         - pulling 'uvIndex' from API call<br>
  cloud_US.csv      - pulling 'cloudCover' from API call and mulitplying by 100<br>
  precip_US.csv     - pulling 'precipProbability' from API call and multiplying by 100<br>
  dew_US.csv        - pulling 'dewPoint' from API call<br>
  pressure_US.csv   - pulling 'pressure" from API call<br>
  wind_US.csv       - pulling 'windSpeed' from API call<br>
  ozone_US.csv      - pulling 'ozone' from API call<br>
  sunrise_US.csv    - pulling 'sunriseTime' from API call<br>
  sunset_US.csv     - pulling 'sunsetTime' from API call<br>

<b>Values of -1000 are dummy values for when there was some sort of error in the JSON response.<br>
Also, make note that the Latitude and Longitude for some locations/rows are 0, 0.<br>
The weather data for those will not be accurate, because the data are pulled based on the <br>
provided Latitude and Longitude, not the place name.</b><br><br>


The JSON returned hourly values and daily values. For the purposes of this project, daily values were used. The header for each column was taken and passed as a Unix time value to retrieve data for that date.<br><br><br>

Also, don't bother trying anything with my API key. It is reset with every push. If you want to try it for yourself, Dark Sky very generously offers 1,000 free API calls per day. https://darksky.net/poweredby/



=======
# Read the README file from the original JHU branch at the following link: https://github.com/CSSEGISandData/COVID-19/blob/master/README.md <br>
<br>
Their original readme invluded the following Acknowledgements and Terms of Use:<br><br>
<b>Acknowledgements:</b>
We are grateful to the following organizations for supporting our Center’s COVID-19 mapping and modeling efforts:
Financial Support: Johns Hopkins University, National Science Foundation (NSF), Bloomberg Philanthropies, Stavros Niarchos Foundation;
Resource support: AWS, Slack, Github; Technical support: Johns Hopkins Applied Physics Lab (APL), Esri Living Atlas team

<b>Additional Information about the Visual Dashboard:</b>
https://systems.jhu.edu/research/public-health/ncov/

<b>Contact Us: </b>

* Email: jhusystems@gmail.com



<b>Terms of Use:</b>

1. This data set is licensed under the Creative Commons Attribution 4.0 International (CC BY 4.0) by the Johns Hopkins University on behalf of its Center for Systems Science in Engineering.  Copyright Johns Hopkins University 2020.

2. Attribute the data as the "COVID-19 Data Repository by the Center for Systems Science and Engineering (CSSE) at Johns Hopkins University" or "JHU CSSE COVID-19 Data" for short, and the url: https://github.com/CSSEGISandData/COVID-19.  

3. For publications that use the data, please cite the following publication: "Dong E, Du H, Gardner L. An interactive web-based dashboard to track COVID-19 in real time. Lancet Inf Dis. 20(5):533-534. doi: 10.1016/S1473-3099(20)30120-1"
