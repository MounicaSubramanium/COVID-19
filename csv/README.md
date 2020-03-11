Please see https://darksky.net/dev/docs for description of the various fields that are captured.<br>
All of the following details pertain to data from the 'daily' element in the JSON file that is returned.<br>
Where applicable, the units that are returned are in SI units<br><br>
The data is all very generously Powered by Dark Sky: https://darksky.net/poweredby/<br><br>

The following csv files are included:<br><br>
tMax.csv<br>
'temperatureHigh' field, proveded as degrees Celsius<br><br>

tMin.csv<br>
'temperatureLow' field, provided as degrees Celsius<br><br>

humidity.csv<br>
'humidity' field, provided as relative humidity (percente out of 100)<br><br>

uv.csv<br>
'uvIndex' field, provided as UV index. Honestly, I'm not sure what the units here are.<br><br>

cloud.csv<br>
'cloudCover' field, provided as The percentage of sky occluded by clouds (out of 100)<br><br>

precip.csv<br>
'precipProbability' field, provided as the probability of precipitation occurring (out of 100)<br><br>

dew.csv<br>
'dewPoint' field, provided as degrees Fahrenheit (according to the documentation) I made the request for SI units<br>
Frankly, I don't know enough about this to know if the numbers look like Fahrenheit or Celsius<br><br>

pressure.csv<br>
'pressure" field, provided as sea-level air pressure in millibars<br><br>

wind.csv
'windSpeed' field, provided as wind speed in miles per hour (according to the documentation). Again as above,<br>
I made the request for SI units. I don't know enough to know which one is more likely.<br><br>

ozone.csv
'ozone' field, provided as columnar density of total atmospheric ozone at the given time in Dobson units
