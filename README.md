# Challenge 18 - Tableau

## **[Link to Tableau]()**

## Data
I collected December 2022, January 2023 and February 2023 data from the [New York CitiBike data website](https://s3.amazonaws.com/tripdata/index.html).

This data had the fields:
- Ride ID
- Rideable type
- Started at
- Ended at
- Start station name
- Start station ID
- End station name
- End station ID
- Start latitude
- Start longitude
- End latitude
- End Longitude
- Member or casual ride

In [`reduced_data.ipynb`](reduce_data.ipynb), I combined the three CSV files. Due to the size limit of Tableau being 1 GB, and these being the smallest three file sizes of the last year (and together being 1.01 GB in size), I had to reduce the data to get a smaller file size. To do so, I:
- removed the `ride_id` column as it was unused
- converted the `member_casual` column to `True`/`False` rather than strings
- mapped the values of the `rideable_type` column to single characters rather than full strings
    - "classic_bike"  -> "C"
    - "electric_bike" -> "E"
    - "docked_bike"   -> "D"
- dropped all rows that were missing any data (~15,000)

These actions reduced the combined file size down to an acceptable 829 MB and the row count from 5,257,001 to 5,242,112.

## Tableau
The single csv file was then added to Tableau and visualizations were created to explore different phenomena. Due to the size-limited amount of data, I was unable to examine long trends over the seasons or year.