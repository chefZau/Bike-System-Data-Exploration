# Ford GoBike System Data Exploration

## by Luca Zhou

This project has two parts that demonstrate the importance and value of data visualization techniques.

1. We will use **Matplotlib** and  **Seaborn** to systematically explore a selected dataset, starting from plots of single variables and building up to stories of multiple variables.
2. We will produce a short presentation that illustrates interesting properties, trends, and relationships discovered in the first part. The primary method of conveying our findings will be through transforming our **exploratory visualizations** from the first part into polished, **explanatory visualizations**.

## Objectives

* Supplement statistics with visualizations to build understanding of data.
* Choose appropriate plots, limits, transformations, and aesthetics to explore a dataset, allowing us to understand distributions of variables and relationships between features.
* Use design principles to create effective visualizations for communicating findings to an audience.

## Prerequisite

We will use Python 3, and the IDE we will be using is Jupyter Notebooks. Uses the Anaconda distribution to install Python is highly recommended since it includes all necessary Python libraries and Jupyter Notebooks. Besides, the following libraries are expected to be used in this project:

* NumPy
* pandas
* Matplotlib
* Seaborn

## Dataset

The dataset we will be using is the [Ford GoBike System Data](https://www.fordgobike.com/system-data). It includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. Since the website is currently unavailable, here is the link to the CSV file: [201902-fordgobike-tripdata.csv](https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv).

* Note that this dataset will require some data wrangling to make it tidy for analysis. The linked system covers multiple cities, and numerous data files will need to be joined together if a full year’s coverage is desired.
* If you’re feeling adventurous, try adding analysis from other cities, following links from [www.bikeshare.com](https://www.bikeshare.com/data/) or [this github link](https://github.com/BetaNYC/Bike-Share-Data-Best-Practices/wiki/Bike-Share-Data-Systems).

The Features included in the Data are as follows :

| Feature       | Definition    |
| ------------- |:-------------:|
| duration_sec | trip duration (in seconds) |
| start_time | start time and date |
| end_time | end time and date |
| start_station_id | start station id |
| start_station_name | start station name |
| start_station_latitude | start station latitude |
| start_station_longitude | start station longitude |
| end_station_id | end station id |
| end_station_name | end station name |
| end_station_latitude | end station latitude |
| end_station_longitude | end station longitude |
| bike_id | bike id |
| user_type | user type (subscriber or customer. “subscriber”: member or “customer”: casual) |
| member_birth_year | member year of birth |
| member_gender | member gender |
| bike_share_for_all_trip | bike share for all trips or not |

Derieved Features:

| Feature       | Definition    |
| ------------- |:-------------:|
| distance | distance between starting and ending position |
| hour | the hour hand of feature ``start_time`` |
| day_name | the day of the week, derieved from ``start_time`` |
| age | the age of the user; derieved from ``member_birth_year`` |
| locality | the city of the starting position |

## Summary of Findings

This research's primary purpose is to find the factors that can increase the usage of shared bicycles. The study will launch around in the following aspects:

1. The duration of using shared bikes per person.
2. The driving distance on using shared bikes per person.
3. The usage of shared bikes per hour in a day.
4. The daily usage of shared bikes in a week.
5. Popular spots to use shared bikes.
6. Under different locations, genders, and age groups, are the conclusions obtained from the above consistent.

After exploring the above fields separately, we found out:

1. Most people would consider using the bikes when the trip is less than 1.43 kilometers.
2. On average, a user did a ride in no more than 11.73 minutes.
3. On weekdays, most bike usages occur during the daytime, and it peaked at 7 am to 9 am and 4 pm to 6 pm. While on weekends, the peak of the usages tends to shift to early afternoon.
4. Most bike usages were coming from the modernized area; Namely, San Fransico, Berkeley, and San Jose — the closer to the waterfront, the higher the user density.
5. The hourly usage distribution of using the bicycles almost the same for each gender. However, when observing female users' usages, the weekends' distribution was multimodal (instead of unimodal).
6. When group by city and gender, women have the highest median in duration, followed by other gender groups and male. Moreover, the locality's highest median is Emeryville, San Francisco, San Jose, Berkeley, and Oakland.

## Key Insights for Presentation

The above findings suggest that most users choose to use the shared bicycles when the trips are quick and not too far away. Most bike usages were coming from Emeryville, San Francisco, San Jose, Berkeley, and Oakland. It would be great if we increase new stations every 1.5 kilometers in these cities. Since the number of usages depends on the time of the day and week, we need to give each station different bikes based on the distribution of uses.
