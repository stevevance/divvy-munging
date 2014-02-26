divvy-munging
=============
The primary file in this repo Divvy_Trips_And_Distances_2013.csv.zip. It contains a table, ready for import into a MySQL database, that combines Divvy’s year 2013 trip data (released February 11, 2014) with corrected station names, station IDs that match Divvy’s stations availability API, launch times, geographic coordinates, precalculated member age, and estimated bicycling distance between stations (see notes). 

## Need support?
* Review pages on the Bike Sharing Data Hackpad: [Divvy Data II](https://bikesharingdata.hackpad.com/Divvy-Data-II-February-11-2014-WQz3gHkxo0M?r=1) and [Chicago data & experiences](https://bikesharingdata.hackpad.com/Chicago-data-experiences-f1ym6mXft2d)
* Ask for it on Twitter with the [#DivvyData](https://twitter.com/search?q=%23divvydata) hashtag. 
* Post in the [Divvy Data Google group](https://groups.google.com/forum/#!forum/divvydata). 
* Come to [Open Gov Hack Night]([http://opengovhacknight.org) on Tuesday nights at the Merchandise Mart
* Contact [Steven Vance](http://twitter.com/stevevance), repo creator if the above methods don't work

## Notes
Distances are in meters. The distance represents the Google Maps Bicycle directions distance for that station pair and no route was inspected before the algorithm’s route was accepted into the dataset. 

Launch dates prior to August 16, 2013, may be incorrect. I’m working to fix these. 

"Trips that did not include a start or end date were removed from original table" is standard language Alta Bicycle Share uses across all data releases. In the case of Divvy's 2013 data, there were no trips without a start or end date removed from the original table. In general, these kinds of trips would occur from missing/stolen bikes.

## Basic stats

### Sex/gender distribution stats
69% of Divvy members are men, 31% are women, as of the end of 2013, and February 14, 2014. As of this writing, survey responses were not available. From Divvy. 

1.8% of male workers 16 years and older primarily used a bicycle to get to work, while 0.7% of female workers 16 years and older did. Both have a margin of error of ±0.1%. Considering there were 625,289 male workers 16+ (MOE of ±4,264) and 588,612 female workers 16+ (MOE of ±4,113), that's a ratio of 73.20% to 26.80%. American Community Survey, 2008-2012, table S08010, via American FactFinder.

In 2013, 79.05% of member trips were by male members and 20.95% by female members. From my analysis of the trip data. 

## Credits
The pairwise distance was created by Nick Bennet (with Google Maps product assistance from Smart Chicago Collaborative), and the SQL query to merge them by Eric Van Zanten. 
