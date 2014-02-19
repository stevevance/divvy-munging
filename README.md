divvy-munging
=============
The primary file in this repo Divvy_Trips_And_Distances_2013.csv.zip. It contains a table, ready for import into a MySQL database, that combines Divvy’s year 2013 trip data (released February 11, 2014) with corrected station names, station IDs that match Divvy’s stations availability API, launch times (see notes), geographic coordinates, and estimated bicycling distance between stations (see notes). 

## Notes
Distances are in meters. The distance represents the Google Maps Bicycle directions distance for that station pair and no route was inspected before the algorithm’s route was accepted into the dataset. 

Launch dates prior to August 16, 2013, may be incorrect. I’m working to fix these. 

## Sex/gender distribution stats
69% of Divvy members are men, 31% are women, as of the end of 2013, and February 14, 2014. As of this writing, survey responses were not available. From Divvy. 

1.8% of male workers 16 years and older primarily used a bicycle to get to work, while 0.7% of female workers 16 years and older did. Both have a margin of error of ±0.1%. Considering there were 625,289 male workers 16+ (MOE of ±4,264) and 588,612 female workers 16+ (MOE of ±4,113), that's a ratio of 73.20% to 26.80%. American Community Survey, 2008-2012, table S08010, via American FactFinder.

In 2013, 79.05% of member trips were by male members and 20.95% by female members. From my analysis of the trip data. 

## Credits
The pairwise distance was created by Nick Bennet (with Google Maps product assistance from Smart Chicago Collaborative), and the SQL query to merge them by Eric Van Zanten. 