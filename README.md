Airbnb: First Data Science project

Goal: analyze Airbnb's data while training on concepts reviewed so far on Python, Pandas, NumPy, Seaborn, Matlplotlib.  

Data used: airbnb - coming from hotel industry, this was the available data that made the most sense. 
Data: http://insideairbnb.com/get-the-data.html

*Note: Comments & analysis are about the New York marketplace despite the possibility of changing marketplace, for the sake of this exercise. 

1. Choose a number corresponding to the city to explore: 
Option to chose a marketplace to analyze among 10 cities. Choosing a number rather than typing an actual city will be less prone to errors.
I chose 10 main cities: 5 in Canada and 5 in the US - similarly to the Fairmont hotels marketplace. 

Amended to pick only the csv file needed so the site would load faster. 
I included one of the lightest csv files on GitHub for reference: Ottawa. 

2. Tried to clean unusable data such as numeric or date columns that were texts. 

3. The first part of the project contains some basic information that was allowing me to purely train on the concepts I learned in the Data Science codecademy program. i.e. quantile divisions, distribution modality, median, variance, standard deviation. 

Regarding some of these I had started a separate file on the New York marketplace only analyzing further into details these such as New York having a bimodal distribution etc. Which I removed when I finalized the option to easily switch from 1 market to another. 

4. Map representation. I was curious to visually picture where the most concentrated and the priciest boroughs were. Originally tried with mapleaflet but the csv files were too heavy to work (or I couldn't make it work!) - thus the google map screenshots. 

5. Boroughs definition 
	Most marketplaces have a very high number of neighbourhoods making them not usable. 
	I tried to automatize defining them, dividing them by equal numbers of units among 5 different boroughs. 
	They are divided geographically: either by latitude or longitude, depending whether the market is wider in latitude or longitude. 

6. Description: some main points about the marketplace. 
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
	##. Summary of main points about marketplace
	-
	Training on violinplots
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
		From here onwards: data added recently, so organization is not as clear, and I am amending it on a daily basis as I find better ways to display it (i.e. what I just did for 6. review_scores but not yet for 7.). Goal is to train on things I have not included before in this project, or things I want to review, or as I am discovering as I continue the path on Codecademy. 		  
	  	3. Average number of listings per host per borough 
		4. Number of units per year 
	   	  Easily showing when each marketplace boomed, by room type 
		5. Average length of stay per borough
		6. a/Correlation between average score and response time 
		  Reviewing overall scores and verifying whether communication is the score impacting overall results
		  Comments here apply to New York. 
Unsurprisingly, hosts who take the longest to respond generally have lower Overall scores ratings. Difference in ratings between regular and super hosts is drastic: up to 5 pts difference for host response within an hour. Hosts who are superhosts (naturally) have  higher scores."
However, communication is not necessarily the score dragging scores down as they are generally similar between regular and superhosts.
		7. Correlation between profile picture and number of reviews by month: 
		Do guests who don't have profile pictures have less visitors per month?
		a/ Overall
		There isn't a big difference in number of reivew per month overall between hosts who do and those who don't have a profile picture.
		b/ By borough
		Comments here apply to New York. 
However when looking at details by borough, it seems Queens recorded a particularly high number of reviews for per month (3.2 without profile picture vs 2.0 with one, on average), skewing all other boroughs' average which do indicate there is a lower number of reviews per month when the host doesn't have a profile picture.
		8. Average LOS required by borough by bed type
		Comments here apply to New York. 
The average length of stay requested overall is 7.4 nights, with Manhattan having the highest one: 9.0. Futons are actually the bed type requesting the highest minimum night stay, higher than real beds (+0.5pts), and Airbeds require a higher length of Stay than Couches, which require the lowest number of nights stay.
		9. Average rating by borough by bed type
		Comments here apply to New York.
Staten Island and Brooklyn record the highest rating scores overall. Manhattan records a score below average: 93.7. 
This table doesn't take into account the number of reviews written by borough.
		10. Weekly price discount
		Training further on calculating aggregate functions
		Comments here apply to New York.
Despite Brooklyn and Manhattan having the highest number of units offering weekly discounts, they are the ones offering the lowest discounts - particularly Manhattan.
	9. (4. in Jupyter) Hypothesis Testing		
		1. Do superhosts have more than 1 listing, and is the different significant?
		1. Note: I know I had calculated part of superhosts before - I plan to amend the first one with this one, as this one is cleaner.
		2. a/ Do instant bookable units allow to charge a higher rate? 
		Yes, the price difference is significant between units that are instantly bookable and those that aren't. 
		2. b/ Is this difference driven by hotel rooms' prices (estimated to be higher) 
		Tukey's Range Test shows we can reject this hypothesis - the price difference is significant among all room types (except between private and shared rooms). 
		Use of dictionary to loop through each room type and create variables with price corresponding accordinlgy
	>> Rest: Work in progress: 
	getting list of most popular amenities in order to use them for machine learning, linear regression model 
		
	


