# How-Does-a-Bike-Share-Navigate-Speedy-Success
Bike-Share Navigate Speedy

Data: 202004-divvy-tripdata.csv 
(Source: https://divvytripdata.s3.amazonaws.com/index.html)

Goal: Design marketing strategies aimed at converting casual riders into annual members. In order to do that, however, we need to understand how annual members and casual riders differ, why casual riders would buy a membership, and how digital media could aspect their marketing tactics.

Tools used: Spreadsheets.

Questions to Answer:

1.	How do annual members and casual riders use Cyclistic bikes differently? 
2.	Why would casual riders buy Cyclistic annual memberships?
3.	How can Cyclistic use digital media to influence casual riders to become members? 



Prepare:

*	Data is organized in spreadsheets using rows and columns
*	Data has two blank rows which has been identified using “filter” tool, Removed two rows which reduced the number of rows to 84,777 from 84,779
*	Data has no Duplicate Record. All 84,777 rows remain unique.
*	Data has no Extra White Spaces which has been checked using Trim Function.
*	Data Format of Column “started_at” and “ended_at” has been changed to ‘Date Time’. Formatted using Format > Number > Date Time.



The Data is all set and can proceed further part of analysis.

Process:

*	Tools: spreadsheets.
*	Data integrity has been ensured by verifying each columns with its corresponding Data Format.
*	Data is cleaned, Checked with “Conditional Formatting” tool

*	Created new column and Calculated the length of each ride by subtracting the column “started_at” from the column “ended_at” (=D2-C2) and formated as HH:MM:SS using Format > Number > Duration. 
*	Found 51 rows which has negative value for ‘ride_length’ when sorted, because ‘started_at’ time is greater than ‘ended_at’ time.
*	Removed 51 rows which reduced the number of rows to 84,727 from 84,777.
*	Found 8 rows which has Zero value for ‘ride_length’. Assuming those to be an incorrect data, removing those values changed the number of rows to 84,719 from 84,727.
*	Created a column called “day_of_week,” and calculate the day of the week that each ride started using the “WEEKDAY” command (for example, =WEEKDAY(C2,1)). Formatted as General or as a number with no decimals, noting that 1 = Sunday and 7 = Saturday.

Analyse:

*	Calculated the Mean (average) or ride_length using =AVERAGE (E: E), formatted it to duration.
*	Calculated the Maximum ride_length using =MAX (E: E), formatted it to duration.
*	Calculated the Minimum ride_length using =MIN (E: E), formatted it to duration.
*	Calculated number of rides in each day from ‘day_of_week’ using =COUNTIF (F: F, 1) for Sunday, formatted it to general.
*	Created a pivot table and calculated the average ride_length for members and casual riders. By setting rows = member casual; Values = Average of ride_length. 
*	Calculated the average ride_length for users by day_of_week. By setting columns = day_of_week; Rows = member casual; Values = Average of ride_length 
