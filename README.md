divvy-munging
=============

Merging pairwise station distances with 2013 trip data. The pairwise distance was created by Nick Bennet, and the SQL query to merge them by Eric Van Zanten. 

The file is Divvy_Trips_And_Distances_2013.csv and is 145 MB.

Important: The distance represents the Google Maps Bicycle directions distance for that station pair and no route was inspected before the algorithm’s route was accepted into the dataset. 

Divvy released trip data for all trips taken by annual members and 24-hour pass holders for the 2013 operation year, which is June 28 to December 31. 

Distances are in meters unless marked otherwise. 

Station IDs in files that Divvy didn't produce may be erroneous so don't trust them. However, the station names are correct. 

## Sex/gender distribution
69% of Divvy members are men, 31% are women, as of the end of 2013, and February 14, 2014. As of this writing, survey responses were not available. From Divvy. 

1.8% of male workers 16 years and older primarily used a bicycle to get to work, while 0.7% of female workers 16 years and older did. Both have a margin of error of ±0.1%. Considering there were 625,289 male workers 16+ (MOE of ±4,264) and 588,612 female workers 16+ (MOE of ±4,113), that's a ratio of 73.20% to 26.80%. American Community Survey, 2008-2012, table S08010, via American FactFinder.

In 2013, 79.05% of member trips were by male members and 20.95% by female members. From my analysis of the trip data. 