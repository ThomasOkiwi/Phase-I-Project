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
