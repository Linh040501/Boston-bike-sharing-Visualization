# Boston Bike-Sharing Visualization

This project utilizes the Boston Blue Bikes dataset from [Blue Bikes System Data](https://bluebikes.com/system-data) to visualize insights and patterns in bike-sharing usage.

## Step 1: Data Cleaning Using R

**Packages Used:** `tidyverse`, `lubridate`, `dplyr`, `tidyr`, `geosphere`

- I selected the dataset from the official company website to ensure it is Reliable, Original, Comprehensive, Current, and Citable (ROCCC).

### Cleaning Process
- Inspected the dataset and identified an unusual value for `tripduration` (3401096).
  - Hypothesized it as an outlier or typo.
  - Calculated the Standard Deviation and used empirical rules and Chebyshev's theorem. Since the maximum value exceeded 3 standard deviations, the hypothesis was rejected.
- Removed extra spaces and blanks.
- Retained duplicates due to the nature of the dataset.
- Checked for spelling errors.
- Identified and addressed unformatted and missing data.
- Removed unwanted data.

### Preparation
- Added a time block column to the dataset.
- Calculated trip duration in minutes and hours.
- Joined the dataset with `dot_dataset` to assess the productivity of stations' dots.
- Calculated trip length using longitude and latitude.

## Step 2: Data Visualization

- Created a table showing the total number of trips for each station, including trip durations in minutes and hours. A filter allows viewers to adjust the timeline by day of the week.
- Designed a dynamic bar chart illustrating the trend of user types by counting trips throughout each hour of the day. Includes filters for user types and highlights peak hours.
- Developed a table displaying trends of total trips by weekday for two user types, including percentage calculations for each type.
- Created a bar chart showing total trips by weekday for each user type, separated by time of day (morning, afternoon, evening, and night).
- Produced a heatmap showing total trips across weekdays and hours.
- Generated two line charts comparing the trend of total rides for two user types, with side-by-side comparison and filters for the day of the week and season of the year.
- Built a map displaying total trips for each station and the number of dots. Calculated and ranked productivity of dots at each station.

## Step 3: Build Tableau Dashboard

### The Final Dashboard Contains:
- A count of total trips for two user types.
- A line chart showing trip trends, filterable by user type, day of the week, and season.
- A heatmap displaying the total number of trips across weekdays and hours. Click here to view the visualization:
https://public.tableau.com/views/Bostonbike-sharingAnalysis/Rankstationdockproductivity?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
