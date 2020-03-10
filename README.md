# Gathering weather data for JHU's COVID19 infection data

I realized this morning that a part of my approach is kind of a) faulty and b) resource-intensive when it doesn't have to be, so I'm going to re-work some of the code and structure and what-not later. Also, I'll have to investigate why some of these Chinese cities aren't returning data.<br>
<br>
Further description coming soon.

Weather data is very generously Powered by Dark Sky: https://darksky.net/poweredby/

JHU's time_series_19-covid-Confirmed.csv was taken, and repurposed it to get weather data for the dates and locations that are listed.

<b>The following csv files are generated:<br></b>
  tMax.csv       - pulling 'temperatureHigh' from API call<br>
  tMin.csv       - pulling 'temperatureLow' from API call<br>
  humidity.csv   - pulling 'humidity' from API call, and multiplying by 100<br>
  uv.csv         - pulling 'uvIndex' from API call<br>
  cloud.csv      - pulling 'cloudCover' from API call and mulitplying by 100<br>
  precip.csv     - pulling 'precipProbability' from API call and multiplying by 100<br>
  dew.csv        - pulling 'dewPoint' from API call<br>
  pressure.csv   - pulling 'pressure" from API call<br>
  wind.csv       - pulling 'windSpeed' from API call<br>
  ozone.csv      - pulling 'ozone' from API call<br>
  

Please see https://darksky.net/dev/docs for meaning and units of each value. Where applicable, units are pulled in SI units.


The JSON returned hourly values and daily values. For the purposes of this project, daily values were used. Each value recorded in each cell is the mediian value for the day of the given column, along with the 14 preceding days, for the location of the given row.




=======
# Below is JHU's original information for the README.md


# 2019 Novel Coronavirus COVID-19 (2019-nCoV) Data Repository by Johns Hopkins CSSE


This is the data repository for the 2019 Novel Coronavirus Visual Dashboard operated by the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE). Also, Supported by ESRI Living Atlas Team and the Johns Hopkins University Applied Physics Lab (JHU APL).

<br>

<b>Visual Dashboard (desktop):</b><br>
https://www.arcgis.com/apps/opsdashboard/index.html#/bda7594740fd40299423467b48e9ecf6
<br><br>
<b>Visual Dashboard (mobile):</b><br>
http://www.arcgis.com/apps/opsdashboard/index.html#/85320e2ea5424dfaaa75ae62e5c06e61
<br><br>
<b>Lancet Article:</b><br>
[An interactive web-based dashboard to track COVID-19 in real time](https://doi.org/10.1016/S1473-3099(20)30120-1)
<br><br>
<b>Provided by Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE):</b><br>
https://systems.jhu.edu/
<br><br>
<b>Data Sources:</b><br>
* World Health Organization (WHO): https://www.who.int/ <br>
* DXY.cn. Pneumonia. 2020. http://3g.dxy.cn/newh5/view/pneumonia.  <br>
* BNO News: https://bnonews.com/index.php/2020/02/the-latest-coronavirus-cases/  <br>
* National Health Commission of the People’s Republic of China (NHC): <br>
 http://www.nhc.gov.cn/xcs/yqtb/list_gzbd.shtml <br>
* China CDC (CCDC): http://weekly.chinacdc.cn/news/TrackingtheEpidemic.htm <br>
* Hong Kong Department of Health: https://www.chp.gov.hk/en/features/102465.html <br>
* Macau Government: https://www.ssm.gov.mo/portal/ <br>
* Taiwan CDC: https://sites.google.com/cdc.gov.tw/2019ncov/taiwan?authuser=0 <br>
* US CDC: https://www.cdc.gov/coronavirus/2019-ncov/index.html <br>
* Government of Canada: https://www.canada.ca/en/public-health/services/diseases/coronavirus.html <br>
* Australia Government Department of Health: https://www.health.gov.au/news/coronavirus-update-at-a-glance <br>
* European Centre for Disease Prevention and Control (ECDC): https://www.ecdc.europa.eu/en/geographical-distribution-2019-ncov-cases 
* Ministry of Health Singapore (MOH): https://www.moh.gov.sg/covid-19
* Italy Ministry of Health: http://www.salute.gov.it/nuovocoronavirus

<br>
<b>Additional Information about the Visual Dashboard:</b><br>
https://systems.jhu.edu/research/public-health/ncov/
<br><br>

<b>Contact Us: </b><br>
* Email: jhusystems@gmail.com
<br><br>

<b>Terms of Use:</b><br>

This GitHub repo and its contents herein, including all data, mapping, and analysis, copyright 2020 Johns Hopkins University, all rights reserved, is provided to the public strictly for educational and academic research purposes.  The Website relies upon publicly available data from multiple sources, that do not always agree. The Johns Hopkins University hereby disclaims any and all representations and warranties with respect to the Website, including accuracy, fitness for use, and merchantability.  Reliance on the Website for medical guidance or use of the Website in commerce is strictly prohibited.
