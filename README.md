# Cyclistic ( A Capestone Project by Google Data analystics)
Course link: https://www.coursera.org/learn/google-data-analytics-capstone

# Introduction
Welcome to the Cyclistic bike-share analysis case study! In this case study, I will perform many real-world tasks of a junior
data analyst. I will work for a fictional company, Cyclistic, and meet different characters and team members. In order to
answer the key business questions, I have to follow the steps of the data analysis process: **ask, prepare, process, analyze,
share, and act**.

# Scenario
I am a junior data analyst working in the marketing analyst team at Cyclistic, a bike-share company in Chicago. The director
of marketing believes the company’s future success depends on maximizing the number of annual memberships. Therefore,
my team wants to understand how casual riders and annual members use Cyclistic bikes differently. From these insights,
my team will design a new marketing strategy to convert casual riders into annual members. But first, Cyclistic executives
must approve my recommendations, so they must be backed up with compelling data insights and professional data
visualizations.

# About the company
In 2016, Cyclistic launched a successful bike-share offering. Since then, program has featured more than 5,800 bicycles and 600 docking stations. Cyclistic sets itself apart by also offering reclining bikes, hand tricycles, and cargo bikes, making bike-share more inclusive to people with disabilities and riders who can’t use a standard two-wheeled bike. The majority of riders opt for traditional bikes; about 8% of riders use the assistive options. Cyclistic users are more likely to ride for leisure, but about 30% use them to commute to work each day.

# Characters and teams(Key Stakholders)

● Lily Moreno: The director of marketing (Primary Stakeholders)

● Cyclistic executive team (Primary Stakeholders)

● Cyclistic marketing analytics team (Secondary Stakeholders:)

# Ask
**Three questions will guide the future marketing program:**
1. How do annual members and casual riders use Cyclistic bikes differently?
2. Why would casual riders buy Cyclistic annual memberships?
3. How can Cyclistic use digital media to influence casual riders to become members?

**Guiding questions:**

1. What is the problem you are trying to solve?
2. How can your insights drive business decisions?

**Key tasks:**

1. Identify the business task
2. Consider key stakeholders
   
**Deliverable:**

A clear statement of the business task

# Prepare
I will use Cyclistic’s historical trip data to analyze and identify trends. Downloaded the previous 12 months of Cyclistic trip data
using this [link.](https://divvy-tripdata.s3.amazonaws.com/index.html) The data has been made available by
Motivate International Inc. under this [licence.](https://www.divvybikes.com/data-license-agreement)

**Guiding questions**

**1.Where is your data located?**

The data is located in my device and downloaded from (https://divvy-tripdata.s3.amazonaws.com/index.html).

**2.How is the data organized?**

seperated into 12 Each month in its own csv file, each file contains 13 columns (ride_id, rideable_type, started_at,	ended_at,	start_station_name,	start_station_id,	end_station_name,	end_station_id,	start_lat,	start_lng,	end_lat,	end_lng,	member_casual) 


**3.Are there issues with bias or credibility in this data ROCCC?**

There is no bias because the data set represents cyclists, but there is some loss in the names of the stations. Is this due to the lack of sufficient signage or another reason that we will see during the analysis

**4.How are you addressing licensing, privacy, security, and accessibility?**

According to the company, it owns a license to the dataset. In addition, the data contains personal information about the riders

**5.How did you verify the data’s integrity?**

All the files have consistent columns and each column has the correct type of data.

**6.How does it help you answer your question?**

It have some key insights about the riders and their riding style and type

**7.Are there any problems with the data?**

You are missing some information such as the name of the stations so It would be good to have some updated information about the bike station

# PROCESS
For this project I am going to use Jupyter notebook to combine all the datasets into one dataset and perform data cleaning and manipulation.
We are using jupyter notebook as it is a large file conataining more than 50000000 rows which is not possible to read using excel. 

I combined all the datasets using **concat()** function.

To better understand the data structure I used the **info()** function to get the following summary about the dataframe:
1. dataset contained a combination of numerical, textual and categorial data types.
2. It contained 5859061 observations and 16 columns namely(ride_id, rideable_type, started_at, ended_at,	start_station_name, start_station_id, end_station_name,	 
   end_station_id, start_lat,	start_lng,	end_lat,	end_lng,	member_casual,	ride_length, day_of_week)
3. Datatypes: floats64 = 4, int64 = 1, object = 11.
   
I started to clean and manipulate the dataset:
1. I changed the datatype of (started at and ended at) from object to datetime.
2. Created 3 new column: year, month, weekday.
3. Removed column which were not required.
4. Made sure the dataset didn't contained any null values by using the dropna() function.
   
 **FILE:**  [LINK](https://github.com/STINSON101/Google-Data-Analytics-cape-stone-project/blob/main/CYCLISTIC%20(Google%20Data%20Analytics%20Capestone%20project).ipynb)

# ANALYZE AND SHARE
**Descriptive Analysis:**
We'll conduct descriptive analysis, which helps understand the central tendencies and distribution of the data. This provides an overview of the patterns and trends within the data and can reveal surprising insights. [click here](https://github.com/STINSON101/Google-Data-Analytics-cape-stone-project/blob/main/CYCLISTIC%20(Google%20Data%20Analytics%20Capestone%20project).ipynb)

**Identifying Trends and Relationships:**
In this step, we'll identify key trends, patterns, and relationships between different variables in our data. This may involve looking at correlations between variables, analyzing patterns over time, or identifying factors that influence a particular outcome. with help of tableau we have created visuals to better understand and identify patterns and trends to view [click here](https://public.tableau.com/views/CyclisticGoogledataAnalyticsproject/membershipdistribution?:language=en-US&:display_count=n&:origin=viz_share_link)

**The analysis question is: How do annual members and casual riders use Cyclistic bikes differently?**

1. As we can see in the first pie chart it shows membership distribution of annal member and casual rider, we can see that majority of bike users are Annual member which covers **60.73%** and **39.27%** of casual riders.
2. In the bar chart we identify a trend that shows us monthly ride trend by the bike users, we can see that in the month of august annual member recorded highest number of rides and in the month of july casual members recorded the highest.
3. Third chart shows us the frequency of rides by weekdays by annual members and casual riders, we can see that the casual riders ride more during the weekends and the annual members ride during the week days, mostly the peak days are tuesday, wednesday, thursday for annual members and saturday and sunday for casual riders.
4. In the 4th chart we can gain insgihts relating to member type and the bike type they use for ride, w can observe that annual members use classic bikes more over electirc bikes but none use docked bikes. on the other hand casual riders all types of bike but majority use classic and than electricm thirdly electric.
5. In the 5th chart we are going to observe the weekly trend of the user type according to which type of bike they use, we see that both the users use classic bike more than electric bikes.

     ![Dashboard 1](https://github.com/STINSON101/Google-Data-Analytics-cape-stone-project/assets/129893981/0147bfd7-98d8-416d-a2ac-07417f921a8f)
![Cyclistic (1)](https://github.com/STINSON101/Google-Data-Analytics-cape-stone-project/assets/129893981/afdd55a3-760d-455b-a3f0-82c1a0552526)
![cyclistic (2)](https://github.com/STINSON101/Google-Data-Analytics-cape-stone-project/assets/129893981/a9a73f2e-c867-43e7-b3c1-c58b0fa355f2)


# Act
Now that we have finished creating visualizations, lets act on our findings. 

**Guiding questions**

**1. What is your final conclusion based on your analysis?**

Casual riders most active time of the year is period from April to October
Casual riders prefer to use bikes on Weekends
Casual riders amke use of all bike types.
   
**2. How could your team and business apply your insights?**

Let's make recommendations based on the analysis.To convert more casual riders to members we would recommend **creating new types of memberships.** It can be season membership from April to October or opportunity to free use annual membership for a few months in a year. I would also suggest giving premium privilges to annual members so that it can bring a sense of importance of annual membeship to casual riders.
