#Enhanced Divvy data

Divvy is hosting its [second annual Data Challenge in 2015](http://www.divvybikes.com/datachallenge), with submissings due March 18, 2015 (prizes include an Xbox One and a Windows phone). Divvy Munging is a small project to provide modified & enhanced data so entrants can create a project faster.

## 2014

### Data
* [Divvy's data, a package of 2013 and 2014 trips](https://s3.amazonaws.com/divvy-data/datachallenge/datachallenge.zip) (64 MB) or browse the unzipped datasets in the [2014 Divvy data folder](https://github.com/stevevance/divvy-munging/tree/master/data_from_divvy).
* [Ginormous CSV of all possible route shapes](https://dl.dropboxusercontent.com/u/18777370/Divvy_RouteShapes_ALL-FINAL.csv) by Drew DePriest (using MapQuest Directions). Distances are in feet.

### Notes
* Divvy occasionally moves stations (but station IDs persist). There isn't yet a list of station moves. 

### Stats
Contribute your stats by opening an issue or submitting a pull request. 

## 2013
This enhances the Divvy dataset by adding Google Maps-calculated distances between every station pair. 

### Data
* CSV version:  [Divvy_Trips_and_Distances_2013.csv.zip](https://www.dropbox.com/sh/tsv5xv9qsvbaopd/BU0byzT42w/Divvy_Trips_and_Distances_2013.csv.zip)
* SQL version: [Divvy_Trips_and_Distances_2013.sql.zip](https://www.dropbox.com/sh/tsv5xv9qsvbaopd/5F8RmEjMpe/Divvy_Trips_and_Distances_2013.sql.zip). 
* [Hourly weather from Weather Underground](https://www.dropbox.com/sh/tsv5xv9qsvbaopd/d4yjDfXdiU/chicago_wunderground.txt) via GT Wrobel

This "master file" contains a table, ready for import into a MySQL database, that combines Divvy’s year 2013 trip data (released February 11, 2014) with corrected station names, station IDs that match Divvy’s stations availability API, launch times, geographic coordinates, precalculated member age, and estimated bicycling distance between stations (see notes). 

### Notes
* Distances are in meters. The distance represents the Google Maps Bicycle directions distance for that station pair and no route was inspected before the algorithm’s route was accepted into the dataset. [More about this distance data](https://groups.google.com/forum/#!topic/divvydata/97NdnxCydbw).
* Launch dates were corrected (there used to be a message here that said don't trust them)
* From Divvy's readme: "Trips that did not include a start or end date were removed from original table" is standard language Alta Bicycle Share uses across all data releases. In the case of Divvy's 2013 data, there were no trips without a start or end date removed from the original table. In general, these kinds of trips would occur from missing/stolen bikes.

### Basic stats

Looking for more stats? Check [here](http://j.mp/1flsRDz), [here](http://j.mp/1kFbO6H), and [here](http://j.mp/1mywA6s).

### Sex/gender distribution stats
69% of Divvy members are men, 31% are women, as of the end of 2013, and February 14, 2014. As of this writing, survey responses were not available. From Divvy. 

1.8% of male workers 16 years and older primarily used a bicycle to get to work, while 0.7% of female workers 16 years and older did. Both have a margin of error of ±0.1%. Considering there were 625,289 male workers 16+ (MOE of ±4,264) and 588,612 female workers 16+ (MOE of ±4,113), that's a ratio of 73.20% to 26.80%. American Community Survey, 2008-2012, table S08010, via American FactFinder.

In 2013, 79.05% of member trips were by male members and 20.95% by female members. From my analysis of the trip data. 

## Credits
The pairwise distance was created by Nick Bennet (with assistance from Smart Chicago Collaborative), and the SQL query to merge them by Eric Van Zanten. 

## Need support?
* Review pages on the Bike Sharing Data Hackpad: [Divvy Data II](https://bikesharingdata.hackpad.com/Divvy-Data-II-February-11-2014-WQz3gHkxo0M?r=1) and [Chicago data & experiences](https://bikesharingdata.hackpad.com/Chicago-data-experiences-f1ym6mXft2d)
* Ask for it on Twitter with the [#DivvyData](https://twitter.com/search?q=%23divvydata) hashtag. 
* Post in the [Divvy Data Google group](https://groups.google.com/forum/#!forum/divvydata). 
* Come to [Open Gov Hack Night]([http://opengovhacknight.org) on Tuesday nights at the Merchandise Mart
* Contact [Steven Vance](http://twitter.com/stevevance), repo creator if the above methods don't work out
