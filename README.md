# Boston Bike-Sharing Visualization
Click here to view the visualization: https://public.tableau.com/views/Bostonbike-sharingAnalysis/Rankstationdockproductivity?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link

This project utilizes the Boston Blue Bikes dataset, sourced from [Blue Bikes System Data](https://bluebikes.com/system-data), to analyze and visualize patterns in bike-sharing usage in the year 2022. 

**Tools:** Rstudio, Tableau.

## Step 1: Data Cleaning Using R

**Packages Utilized:** `tidyverse`, `lubridate`, `dplyr`, `tidyr`, `geosphere`

- The dataset was selected from the official website to ensure it adheres to the principles of Reliability, Originality, Comprehensiveness, Currency, and Citatability (ROCCC).

### Data Cleaning Process
1, In the initial phase, we perform these tasks
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
<img width="820" alt="Preparation Data" src="https://github.com/user-attachments/assets/3534bd16-3859-4089-906b-aed76e0a3c47">
- Created a dynamic bar chart illustrating the trend of user types by counting trips per hour. Added filters for user types and highlighted peak activity hours.
  ![Trends by hours of Day and Customer Type](https://github.com/user-attachments/assets/2c9a945e-9fc8-4081-86b6-47b2d4f41ea3)

- Constructed a table showing trip trends by weekday for two user types, including percentage calculations.
![Trend by Weekday and Usertype](https://github.com/user-attachments/assets/aa96a57f-4c63-40d6-9d7b-a2eb21c79af3)


- Designed a bar chart depicting trip trends by weekday for each user type, segmented by time of day (morning, afternoon, evening, night).
![Weekday Trend by Usertype and Time Blocks](https://github.com/user-attachments/assets/5998286f-5572-4033-b2a1-5a2e50500d53)

  
- Generated a heatmap representing total trips across weekdays and hours.
![Heatmap](https://github.com/user-attachments/assets/43ac54e8-ce16-4522-ae47-0e613bd1b5d2)


- Produced two line charts comparing total rides for two user types, with a side-by-side comparison and filters for day of the week and season.
![Comparision_ side by side](https://github.com/user-attachments/assets/1a55bf7b-a765-461b-bc2e-7d0fbaacf4a1)

  
- Created a map displaying the total trips for each station and the number of dots, with an analysis of dot productivity and subsequent ranking.
  ![Rank station dock productivity](https://github.com/user-attachments/assets/d55010ce-ac59-4d60-b53f-3527ce157962)


## Step 3: Building the Tableau Dashboard

### The Final Dashboard Features:
- Total trip counts segmented by user type.
- A line chart illustrating trip trends, filterable by user type, day of the week, and season.
- A heatmap visualizing total trips by weekdays and hours.
![final dashboard (1)](https://github.com/user-attachments/assets/e8a90fa0-4c54-4981-9161-6520e95c6507)

