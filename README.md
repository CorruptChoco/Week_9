# Week_9
## Overview of the statistical analysis
In this analysis we used Python to pull information from a SQLite database. We then queried that database to find out temperature information for the months of June and December for the years 2010-2017.

## Results
||June Temps|December Temps|
| :------------- |:-------------:|:-------------:|
|count|	1700.000000|1517.000000|
|mean|	74.944118|71.041529|
|std	|3.257417|3.745920|
|min	|64.000000|56.000000|
|25%	|73.000000|69.000000|
|50%	|75.000000|71.000000|
|75%	|77.000000|74.000000|
|max	|85.000000|83.000000|

* There are more observations in June than in December
* On average it is colder in December than in June by about 4 degrees
* There is more volatility in temperature range during December than in June. The standard deviation in higher as well a higher delta between minimum temperature and maximum temperature.

## Summary
We have found data showing that on this island in Hawaii temperature holds very well. With a maximum temperature of 85 and a minimum of 56 between the two months shown we can see that temperature volatility is not a large issue. Over half the time the temperature is above 71 degrees.

To look even further we could use filters to help us out.
* `.filter(Measurement.station == 'USC00519281')` could be used to filter to only a specific measurement station.
* `.filter(Measurement.prcp <= 0.05)` could be used to only look at days of low precipitation.
