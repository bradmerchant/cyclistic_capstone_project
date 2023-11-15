# cyclistic_capstone_project
Overview of steps taken for the Google Data Analytics Certificate Capstone Project

In this scenario, I'm tasked with trying to understand how Cyclistic's two different customer types use their bikes differently: annual members and casual riders. The CEO of Cyclistic believes that annual members are key to the company's growth and long-term success. So once the differences between the two customer types is understood, my job is to make recommendations for next steps to drive more member growth.

Cyclistic’s data was organized into monthly tables. There was some older data from 2019 and earlier that was organized by quarter, but I chose to work with more recent data to take post-covid customer habits into account; I used data for the months of July 2022 through June 2023. I also used data going back to July of 2020 to identify long-term historical trends.

There were some NULL values found in the location data columns, but they wouldn't impact my analysis too much. I was mainly focused on broader differences between the two customer types: subscribers and casual riders.
  start_station_name = 14.84%
  start_station_id = 14.85%
  end_station_name = 15.84%
  end_station_id = 15.85%
  end_lat = .10%
  end_lng = .10%

I also created the following columns:
  'started_at_cst' = converted the 'started at' timestamp from UTC to Chicago/Central timezone
  'hour' = extracted the hour from 'cst_started_at'
  'dow' = extracted the day of the week from 'cst_started_at'
  'weekday_weekend' = identified whether the trip started on a weekday or a weekend day
  'month' = extracted the month from 'cst_started_at'
  'trip_duration' = difference between the 'started_at' and 'ended_at' columns

Once the data was clean, I used SQL to slice the data to be able to look at the usage differences between annual members and casual riders. I exported these results into Google Sheets, where I then created the visuals in my presentation.
