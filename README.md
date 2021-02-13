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

> Summarize all of your findings from your exploration here, whether we plan on bringing them into your explanatory presentation or not.


## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.