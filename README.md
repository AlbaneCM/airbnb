# airbnb
first_project


First Data Science project

Goal: to train on concepts reviewed so far on Python, Pandas, NumPy, Seaborn, Matlplotlib. This project mainly applies data visualization notions. 

Web scraping and machine learning have not been reviewed yet. 

Data used: airbnb - coming from hotel industry, this was the available data that made the most sense. 
Data: http://insideairbnb.com/get-the-data.html

Goal for this project: replicate some basic analysis I could have performed on hotels. 

1. a/ Overall: 
Option: to be able to chose a marketplace to analyse among several ones. I chose 10 main cities: 5 in Canada and 5 in the US - similarly to the Fairmont hotels marketplace. 

1. b/ On Jupyter Notebook: 
First, loaded all csv files. They are all too heavy to load on GitHub so I included one of the lightest ones: Ottawa. 

2. Tried to clean unusable data such as numeric or date columns that were texts. 

3. The first part of the project contains some basic information that was allowing me to purely train on the concepts I learned in the Data Science codecademy program. i.e. quantile divisions, distribution modality, median, variance, standard deviation. 

Regarding some of these I had started a separate file on the New York marketplace only analyzing further into details these such as New York having a bimodal distribution etc. Which I removed when I finalized the option to easily switch from 1 market to another. 

4. Map representation. I was curious to visually picture where the most concentrated and the priciest boroughs were. Originally tried with mapleaflet but the csv files were too heavy to work (or I couldn't make it work!) - thus the google map screenshots. 

5. Boroughs definition 
	Most marketplaces have a very high number of neighbourhoods making them not usable. 
	I tried to automatize defining them, dividing them by equal numbers of units among 5 different boroughs. 
	They are divided geographically: either by latitude or longitude, depending whether the market is wider in latitude or longitude. 

6. Description: 10 main points about the marketplace. 
Tried to start from most generalistic information to more detailed
	1. Number of units in market
	2. Number of boroughs per market and list of them
		Only New York has boroughs defined
	3. Number of neighbourhoods
		Most marketplaces have a very high number of neighbourhoods making them not usable. 
	4. Number of hosts
	5. Number of listings per host
	6. Room types definition
	7. First and last listing date
	8. Average price
	Way to train on violinplots
		8. a/ Price range 
		8. b/ Price range by roomtype
		8. c/ Price range by borough 
	9. Charging for additional persons (over 2 adults)
		9. a/ Percentage of units charging for additional adults 
		9. b/ How many adults are usually included in room rate
		9. c/ Fee range charged per extra adult by neigbourhood
	10. Cleaning fee 
		10. a/ Percentage of units charging for cleaning fee 
		10. b/ Cleaning fee range per neighbourhood 
		Way to train on indicating maximum outliers
		10. c/ Details of listings that don't charge a cleaning fee
			-> Number of units by borough
			-> Number of units by room type 


7. Second part: putting in correlation some of the data found 
	7. 1/ Do units that don't charge a cleaning fee have a lower ranking? 
		Compared both ranking scores on average: for units charging and those which do not. 
		Then reviewed the differences by Rating Category to either confirm or identify where differences in both scores were coming from.  
		Generally speaking: for all marketplaces, cleanliness is the category ranked the lowest and the one recording the highest difference between the two compared types. Units charging for a cleaning fee tend to have the highest scores 
	7. 2/ Do units which charge for a cleaning fee tend to charge a lower room rate to compensate? 
		Compared average room rate of units charging for cleaning fee to those which don't.  
		Curious to review if units charging for a cleaning fee were deducting it from the room rate to be more attractive. 
		Generally: True in every studied marketplaces, but in New York or Montreal!

		Additionally, verifying whether - verifying which option is more affordable: units not charging cleaning fee and priced higher, or units charging for cleaning but priced lower. 
	
	8. Further unit description
		1. Average size by room type by neighbourhood 
		Not indicated often - pure curiosity 
		2. a/ Part of hosts that are superhosts 
		   b/ By borough
		   c/ Average number of listings per host per borough 
	   3. Number of units per year 
	   	  Easily showing when each marketplace boomed, by room type 




Thank you so much for going through this :-) 

--> overall question: when writing "if statements", should I always make them as part of functions, or can I just let them as just ifs, like I did in most cases?
Thank you! 

