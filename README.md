# Accidents-Data-Exploration
A exploratory data analysis for accidents that occured all across USA
# Introduction
Accidents happen all the time, but no one expects them to. It's why they're accidents. Everyone has an opinion on how accidents occur, but no one thinks about it until after the fact. Accidents and their consequences are a major problem in society today. To solve this matter, we can observe and analyse accident factors. By accident factors I mean the external factors that lead to accidents. My goal with this report is to categorize what contributes to accidents, in order to provide insight into how accidents happen , and gather information that can be shown graphically to help break down the aspects that lead to these unfortunate situations. We can then use these insights to potentially prevent future accidents by addressing potential risk factors.
# Dataset
Data used is freely available on the Kaggle website .  This accident dataset is a nation wide vehicle accident dataset that spans 49 states in the United States. The accident data collected spans over 1.5 million data sets from February 2016 to December 2020, and is based on a variety of open data sets made available through various government portals.
# Analysis of Dataset	
The dataset consist of 1516064 rows and 47 columns. The first part of this analysis was getting an overview of the data and to see what different aspects contribute directly during an accident. Some of the aspects that I feel is directly related to an accident is being discussed below.
# Time of Accident

We used the pandas datetime  function to convert the original string ‘Start_Time’ column to timestamp. Next, Hour of the day was extracted using ‘functions.hour’ and aggregated to count the number of accidents which happened during each hour.
Starting with a general analysis to determine the time of most accidents occurring, the data were grouped according to various time stamp of the accident  and presented in  a histogram showing the number of accidents that occurred at each time of day.






![image](https://user-images.githubusercontent.com/37774930/172074372-bd33baad-0023-4f0e-b637-93ce8d3badfa.png)








			         Fig 2.1 Distribution of accidents throughout the day

A higher percentage of accidents occur between 7 AM to 9AM in the morning and 3 PM to 5 PM in the evening probably because people tend to be in a hurry to get to work and return from work.The safest time to travel can be depicted to be between 8pm to 5am as less accidents tends to happen during that time. 



![image](https://user-images.githubusercontent.com/37774930/172074384-cf9089b6-688c-4127-b975-1b673b9b3ea6.png)





			      			 Fig 2.2 Distribution of accidents throughout the week
We used ‘functions.dayofweek’ to extract the ‘day’ on which each accident happened, aggregated to get the count for the number of accidents for each day.  When looking at the data pattern in Fig 2.2 across the week, it's clear that there are a lot more accidents on weekdays, which are Monday through Friday in the United States. On the contrary, on weekends, such as Saturday and Sunday, there are fewer accidents.
To further our finding, Figures 2.4 and 2.5 show how the number of accidents dispersed across weekend and weekdays, respectively, During weekends the graph  reverses over the count of accident on a weekday. On weekends, the number of accidents is much lower, especially during peak hours, whereas on weekdays, the number of accidents is over three times higher.

  		              
      ![image](https://user-images.githubusercontent.com/37774930/172074401-3d904ea4-e699-4609-aaa4-d65a73bf3a56.png)



                        Fig 2.3 Distribution of accidents on a weekend                                         
Accidents rise progressively from low points in January and February to a high point in October and December. In comparison to the second half of the year, the first half of the year had a lower number of accidents. Monthly accident rates have risen gradually from February's lows, culminating in the fourth quarter of the year.
 



![image](https://user-images.githubusercontent.com/37774930/172074410-1827901b-d367-47d1-bbe7-d0b389efac0a.png)





		                        Fig 2.5 Distribution of accidents over each month 


Weather impact on accidents

The Temperature column contains temperature during each time a accident happen. Since most accidents tend to happen during the end of year as depicted in the Fig2.6, cold temperature might play a bog role in that. 
On plotting a graph, it is visible that the accidents tend to happen in cold temperatures rather than warm temperatures. I have encoded all the temperature less than 70 degree fahrenheite as cold climate. 

			Fig 2.6 Distribution of accidents in different climate


The dataset contains 128 unique entries for the column 'Weather Condition,' as well as null values. We selected the top 12 weather conditions and averaged them to obtain the total number of accidents for each weather condition after filtering out the null values. In general, we assume that terrible weather will result in more accidents, yet we can observe that when the weather is clear, there are more accidents. This might be due to the fact that when the weather is terrible, people drive more carefully.The weather for the majority of the accidents was clear, followed by overcast and mostly cloudy, according to the map. In contrast to clear skies, overcast and mostly cloudy skies are tolerable causes for accidents, implying that meteorological conditions do not play a significant influence. 
                        
                          		    			















			FIg 2.7 Distribution of accidents over weather condition
		Fig 2.8 Heatmap correlation of accidents over weather condition 	



Location impact on accidents
The dataset contains 1516064 rows hence 1516064 accidents occurred in the given timeframe in the US.  Fig 2.7 shows the distribution of accidents over the top twenty states with the highest number of accidents.  Results showed that California had the highest  number of accidents followed by Florida and Oregon amongst all the states in the country. 
				Fig 2.9 Distribution of accidents over states
To further our standing the accidents time over each cities were done and Los Aneles had the most accident followed by Miami. One of the most important factor to note is the fact that New York is not in the top accident proned city in USA. On further analysis of dataset, it was found that New York city data was not present in the dataset. There is an exponential decrease in the number of accidents per city. About 4 percent of the cities record more than 1000 accidents per year. Over 1300 cities have reported just 1 accident throughout the year. 










							Fig 2.10 Distribution of accidents over cities




Accidents' proximity to traffic objects is also included in the dataset. The most common type of accident is Traffic Signal (44.7%), followed by Junction (20.4%), Crossing (19.7%), Station (5%), and Stop (3.7 percent ). As a result, states and traffic cops must concentrate their efforts in these locations in order to prevent accidents. If the issues are related to infrastructure issues, these must be addressed.
					





Severity of Accidents


The Severity is the most intriguing aspect of the dataset. The severity of the accident is determined by its impact. The graph below gives us details of the severity of each accident.  Around 80% of the accidents are of average severity. It is followed by high severity which is around 10%.  A very low percentage is formed by the very low severity(1) which is 1.86% altogether.  As we can clearly see the majority of the accidents had a severity of 2 (average) or 3 (above average), which is regrettable. There aren't many accidents that aren't fatal (0 and 1). Severity 3&4 have a significant influence. Accidents of severity 2 are more common than those of severity 3 and 4. Incidents of severity 3&4 are more likely to result in fatalities, while accidents with severity 2 are more likely to result in injuries.      		           


		     
				Fig 2.12 Severity of each accident



I have plotted the severity  for each state individually. From the below plot, we can conclude that the accidents with most severity occurred in Wyoming followed by Delaware and Colorado. The highest accidents prone state such as California and Florida are pretty low with the overall severity of accidents.
 

 			 	  Fig 2.13 Severity of accidents in each state
