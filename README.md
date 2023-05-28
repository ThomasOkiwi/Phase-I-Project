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
Budget_file
Budget file containt information on the cost of production and the revenue realised after the sale of the movies.This file will be key in calculation of profit and losses the the individual movie incurred.
Budget_file.head()
id	release_date	movie	production_budget	domestic_gross	worldwide_gross
0	1	Dec 18, 2009	Avatar	$425,000,000	$760,507,625	$2,776,345,279
1	2	May 20, 2011	Pirates of the Caribbean: On Stranger Tides	$410,600,000	$241,063,875	$1,045,663,875
2	3	Jun 7, 2019	Dark Phoenix	$350,000,000	$42,762,350	$149,762,350
3	4	May 1, 2015	Avengers: Age of Ultron	$330,600,000	$459,005,868	$1,403,013,963
4	5	Dec 15, 2017	Star Wars Ep. VIII: The Last Jedi	$317,000,000	$620,181,382	$1,316,721,747
