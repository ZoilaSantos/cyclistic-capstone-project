Cyclistic: Google Data Analytics Capstone Project 
-

Objective
- Identify differences between members and casual customers to inform recommendations for converting casual customers into members.

Data Cleaning (in Excel)
- Data Source: Public data provided by Motivate International Inc found at https://divvybikes.com/system-data
- License: https://ride.divvybikes.com/data-license-agreement

- data consisted of 12 files, each file included all trip entries for a month from March 2022 to February 2023, resulting in over 5 million entires
- data sorted with respect to the start_at column from oldest to newest entry
- checked for duplicate rows by using conditional formatting to highlight duplicate ride_ids and then sorting column by cell color: No duplicate ride_ids
- inserted 2 columns:
   - start_weekday: returns a value 1-7 where 1=Sunday and 7=Saturday
   - duration_sec: returns trip length in seconds
- deleted rows in duration_sec column that returned “#NUM!” --> this indicated an error when subtracting end_at and start_at columns where the "ride ended earlier than it started"
- checked for NULLS --> only occurred in the start_station_name, start_station_id, end_station_name, end_station_id columns
   - decided to leave rows containing these NULLs as the analysis would focus more on the duration and number of trips

Analysis (in SQL)
- All the code for this analysis can be found here: 

