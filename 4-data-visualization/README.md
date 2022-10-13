# Ford GoBike System Data Analysis
#### by Nanli


## Dataset

The Ford GoBike System dataset includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area. Data columns such as ride durations, start and end names, station locations, and customer information are provided in the dataset. 

The [data source](https://video.udacity-data.com/topher/2020/October/5f91cf38_201902-fordgobike-tripdata/201902-fordgobike-tripdata.csv) is linked here.

The original data columns: 
1. duration_sec
2. start_time
3. end_time
4. start_station_id
5. start_station_name
6. start_station_latitude
7. start_station_longitude  
8. end_station_id
9. end_station_name
10. end_station_latitude
11. end_station_longitude
12. bike_id
13. user_type  
14. member_birth_year  
15. member_gender  
16. bike_share_for_all_trip            

In the preliminary data wrangling process, I first cleaned the data by changing data types and checking for duplications, then I conducted feature engineering by creating new features that will be more intuitive for analysis and visualizations. 

Eventually, the data columns I am using:
1. duration_sec
2. start_time
3. end_time
4. start_station_id
5. start_station_name
6. start_station_latitude
7. start_station_longitude
8. end_station_id
9. end_station_name
10. end_station_latitude
11. end_station_longitude
12. bike_id
13. user_type
14. member_birth_year
15. member_gender
16. bike_share_for_all_trip
17. dow (day of the week)
18. hour
19. duration_min
20. distance
21. member_age

There are 183,412 rides in the dataset, and it contains one-month rides from 2019-02-01 to 2019-02-28.


## Summary of Findings

My univariate exploration analysis is mainly focusing on temporal and spatial features, where I discovered the distribution of the rides by day of the week, hours of the day, and the distribution of duration and distance. 

Following the bivariate and multivariate exploration, I expanded the analysis by adding variables such as the user type, member ages, and member gender. In addition, I combined multiple key features, for example, I explored the distribution for the day of the week and hour of the day, and the number of rides for the top busiest stations at different time slots of the day.

The findings are summarized below:

`1. People use the Ford GoBike System mainly for commuting purposes.`
 
>From the number of rides by day of the week, there are more rides during weekdays, I guess in San Francisco Bay area, people use shared bikes for work quite often, while during weekends, the number of rides decreases. 
 
>The peak hours are during morning office time 7 am to 9 am, and after work time 4 pm to 6 pm, at 8 am and 5 pm the number of rides per hour reaches the highest points. Between 10 am to 3 pm, the number of bike riders is very steady, and after 6 pm, the number decreased hour by hour till midnight.

`2. The majority of the rides are within 50mins and less than 8km.`

>The ride duration and distance are long-tailed distributions that are right-skewed. There are outliers where rides have long durations and long distances.
 
`3. Market St at 10th and San Francisco Caltrain Station 2 are the two busiest stations.`

`4. Subscribers ride almost 10 times more than normal customers.`

`5. Subscribers ride bikes mainly during weekdays, while normal customers also ride during the weekend.`

>The subscribers mainly use bikes for commuting, there are few rides during off-peak hours on weekdays and the whole day during weekends.

>Normal customers use bikes for commuting purposes as well, more of the ride during off-peak hours on weekdays compared with subscribers, while during weekends, there are quite a lot of customers ride shared bikes.

`6. Male riders take more rides compared with female riders.`

`7. Users of different gender and ages have similar riding distances and durations.`

`8. There is a positive linear relation between riding durations and distances.`
>The correlation between distance and duration is positive but small (0.13), while the number increased to 0.47 for durations less than 100mins and distances less than 15km.

`9. San Francisco Caltrain Station 2 is the busiest station on weekdays in the mornings for the start station and the afternoons for the end station. Powell St BART Station and Market St at 10th Street are relatively busy during the weekend.`

`10. Montgomery St BART Station is a popular end station in the mornings during weekdays.`

In the explanatory explanation, I will include temporal and spatial analysis results, the relationship between riding durations and distances, the different riding habits of subscribers and normal customers, and the assumptions based on bike stations. I will not focus too much on user demographics, because user genders and ages make little difference to the conclusions.



## Key Insights for Presentation

`1. Temporal Analysis`
>The number of rides by hours and by day of the weeks have clear temporal trends, I concluded that users use GoBike System mainly for commuting purposes. For different user types, the riding behaviors are also different. I would include the heatmap for rides during the day and weeks for customers and subscribers, rather than simply plot the rides by day or weeks for different user types. The former shows customers also use bikes for casual reasons quite often.
 
`2. Spatial Analysis`
>The busiest start and end stations are a good start to rule out the stations I would like to focus on, which are San Francisco Caltrain Station 2, Montgomery St BART Station, Market St at 10th St, etc. Then the subplots that involved both hours and weekdays added insights into the location information for these stations. For example, San Francisco Caltrain Station 2 is close to residential areas, and Montgomery St BART Station is close to office areas. The bar plot needs some polish, I would add titles and adjust the size to fit the presentation slides.
 
`3. Duration and Distance`
>Riding durations and distances are not very much related to member demographics. But the duration and distance are positively linear related. I would include the histogram of distance and duration for different user groups directly to show the relations.

