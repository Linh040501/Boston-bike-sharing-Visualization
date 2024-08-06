# Boston Bike-Sharing Visualization

This project utilizes the Boston Blue Bikes dataset, sourced from [Blue Bikes System Data](https://bluebikes.com/system-data), to analyze and visualize patterns in bike-sharing usage.

## Step 1: Data Cleaning Using R

**Packages Utilized:** `tidyverse`, `lubridate`, `dplyr`, `tidyr`, `geosphere`

- The dataset was selected from the official website to ensure it adheres to the principles of Reliability, Originality, Comprehensiveness, Currency, and Citatability (ROCCC).

### Data Cleaning Process
- Performed an initial examination of the dataset and identified an anomalous value in the `tripduration` column (3401096).
  - Hypothesized that this could be an outlier or a typographical error.
  - Applied statistical methods including Standard Deviation calculations and Chebyshev's theorem. The value exceeded 3 standard deviations, confirming it as an outlier.
- Removed extraneous spaces and blanks from the dataset.
- Retained duplicates due to the dataset’s inherent characteristics.
- Corrected spelling errors and addressed formatting inconsistencies.
- Identified and managed missing or unformatted data.
- Eliminated irrelevant data points.

### Data Preparation
- Introduced a time block column for enhanced temporal analysis.
- Calculated trip durations in both minutes and hours.
- Merged the dataset with `dot_dataset` to evaluate the productivity of bike-sharing stations.
- Computed trip lengths using geographic coordinates (longitude and latitude).

## Step 2: Data Visualization

- Developed a table presenting total trips per station, with trip durations in minutes and hours. Included a filter to adjust the timeline by day of the week.
- Created a dynamic bar chart illustrating the trend of user types by counting trips per hour. Added filters for user types and highlighted peak activity hours.
- Constructed a table showing trip trends by weekday for two user types, including percentage calculations.
- Designed a bar chart depicting trip trends by weekday for each user type, segmented by time of day (morning, afternoon, evening, night).
- Generated a heatmap representing total trips across weekdays and hours.
- Produced two line charts comparing total rides for two user types, with a side-by-side comparison and filters for day of the week and season.
- Created a map displaying the total trips for each station and the number of dots, with an analysis of dot productivity and subsequent ranking.

## Step 3: Building the Tableau Dashboard

### The Final Dashboard Features:
- Total trip counts segmented by user type.
- A line chart illustrating trip trends, filterable by user type, day of the week, and season.
- A heatmap visualizing total trips by weekdays and hours.

Click here to view the visualization:
https://public.tableau.com/views/Bostonbike-sharingAnalysis/Rankstationdockproductivity?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
