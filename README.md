# Introduction
### Objective of the project
The main objective of the project is to identify movie genres on demand,advise Microsoft Movies Production studio On the best genres to invest in.

#### Problem Statement
Movie production is a large capital investment; like any other investiment, it comes with a potential risk. Choice of a the type of movie to invest in is important to avoid capital loss. In order to mitigate the risk of financial loss, it is important to have analytical insight on the genres and the market behaviour.

##### Inporting libraries 
import pandas as pd 
import sqlite3
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline

### Data Understanding
The data provided has historical information from various movie producton studios: movie ratings, actors, generes, cost of proction and the revenue earned, both from World wide marked and domestic market.The dataset is suited for the project since it asnswers most question for investors like the cost of production and the expected profit.Furthermore, the dataset is large enough to provide near accurate infomation

##### Loading Files 
Revenue_File= pd.read_csv("bom.movie_gross.csv.gz",)
Budget_file= pd.read_csv("tn.movie_budgets.csv")
df3=pd.read_csv("name.basics.csv")
Genre_File=pd.read_csv("title.basics.csv")
df6=pd.read_csv("title.crew.csv")
df7=pd.read_csv("title.principals.csv")
Movie_rating=pd.read_csv("title.ratings.csv")
Movie_vote=pd.read_csv("tmdb.movies.csv")

###### Budget_file
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/8525cd62-6c30-495c-a400-313c28b8da71)
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/95a8144f-e321-4c13-b905-efe3815251da)


## DATA CLEANING
This is the section of checking data, removing outliers and duplicteds vallue that would otherwise lead to a wrong conclusion
#### Movie_vote
Thisfile contains vote rating for the movies which is import to understand the customers likes and dislikes based on the content.
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/fc422e03-c3e4-4a94-9289-9581577a293f)


![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/0a52dd7a-f4ea-4fbb-9427-74c75c03fd51)
Columns domestict_ gross and foreign_gross   are sting yet mathematical operation ases supposed to be done.

![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/2fa22de1-814b-4b08-a6c1-400259e3dca1)

Missing values in the repective columns are now replaced by median. This is to enure the data replced do not fall too far from the mean.
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/8593b431-3b31-4600-a9ee-92f12abdc613)

## DATA ANALYSIS
This section deals with data manupulation in order to solve the given problem. In this case, advise Microsft on the type of movie to produce. This section will include recomendetions and conclusion based on the results from the data.
### Caculatiting the profit of producing a movie
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/9966d2ce-bcb8-469d-ad2d-9710faa7e8c9)
From the table, there are some movies that brought profit like, Avatar while some lead lo loses eg.Return to the Land of Wonders
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/fccb10c0-033e-4b25-8cc4-07bceb0a3de1)
Above are the top 20 most profitable genres

#### Movie Genre Ratings
 Below is the top 20 rated genres 
 ![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/d307e763-5f7a-4d04-bdbd-bd1a03cdd40d)


#### Relationship between Genre rating and profit earnerd 
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/64860fd1-79bb-4279-a7c5-7b689c7f3a94)

### Corelation between Genre rating and profit reveue
![image](https://github.com/ThomasOkiwi/Phase-I-Project/assets/133016687/e84ed263-d61c-40f5-9a98-1a8607fbb8a8)

## Conclusiions
1. Horror movies takes the least rating in the grenre
2. Action movies made the lowest prorit margins
3. Adventure drama and sports genres were among the to profit earners
4. Comedy, fantacy and adventure genres we the most liked by audiences. These grenres had the top rating
5. Higher rated movie, are likely to make more prfits than lower ratred onces
## Recomendations
1. It is important to consider genres that are liked by many viewers before investiong in movie production industries. From the study above, action, horror, war movies have least rating and coresponding low revenue.
2. When producing a sequel movies. It is important to take note of the viever reviview and comment before release of the net sequel.
3. Based on the outcome of the study, Microsoft Production Studiio may consider producing adventure, Comedy, drama, fantasy and romance. This are the top earnig grenres as well as top rated ones.


