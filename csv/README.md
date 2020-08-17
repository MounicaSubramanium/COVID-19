<b>Values of -1000 are dummy values for when there was some sort of error in the JSON response.<br>
This will eventually be investigated and corrected. The -1000 values are not valid and should be ignored for now.</b><br><br>
Please see https://darksky.net/dev/docs for description of the various fields that are captured.<br>
All of the following details pertain to data from the 'daily' element in the JSON file that is returned.<br>
Where applicable, the units that are returned are in SI units<br><br>
The data is all very generously Powered by Dark Sky: https://darksky.net/poweredby/<br><br>

The following csv files are included:<br><br>
<b>tMax_US.csv<br></b>
'temperatureHigh' field, provided as degrees Celsius<br><br>

<b>tMin_US.csv<br></b>
'temperatureLow' field, provided as degrees Celsius<br><br>

<b>humidity_US.csv<br></b>
'humidity' field, provided as relative humidity (percent out of 100)<br><br>

<b>uv_US.csv<br></b>
'uvIndex' field, provided as UV index. Honestly, I'm not sure what the units here are. The units are not clear in the API documentation. I'll try to find out.<br><br>

<b>cloud_US.csv<br></b>
'cloudCover' field, provided as The percentage of sky occluded by clouds (out of 100)<br><br>

<b>precip_US.csv<br></b>
'precipProbability' field, provided as the probability of precipitation occurring (out of 100)<br><br>

<b>dew_US.csv<br></b>
'dewPoint' field, provided as degrees Celsius<br><br>

<b>pressure_US.csv<br></b>
'pressure" field, provided as sea-level air pressure in Hectopascals<br><br>

<b>wind_US.csv</b><br>
'windSpeed' field, provided as wind speed in meters per second.<br><br>

<b>ozone_US.csv<br></b>
'ozone' field, provided as columnar density of total atmospheric ozone at the given time in Dobson units<br><br>

<b>sunrise_US.csv</b><br>
'sunriseTime' field, provided as Unix time (https://en.wikipedia.org/wiki/Unix_time)<br><br>

<b>sunset_US.csv</b><br>
'sunsetTime' field, provided as Unix time<br><br>
