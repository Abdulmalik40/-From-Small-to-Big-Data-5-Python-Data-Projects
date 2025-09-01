
 U.S. Baby Names Analysis (1880–2018)
Overview
Explore over 139 years of baby naming trends in the United States using a dataset 

Dataset
Source: us_baby_names.csv
Time Span: 1880 to 2018

 Key Insights
Classic names ruled early decades; recent years show more diversity.
Gender-neutral names are on the rise.
A small number of names have remained in the top ranks for generations.

 Housing Data Exploration
Overview
An initial exploratory data analysis (EDA) of a housing dataset to understand property prices, locations, and key features.

Dataset
Source: housing.csv

 Key Insights
Housing prices and bedrooms have some missing data — handled with imputation or analysis-aware filtering.
Most homes are located near the ocean or in inland areas.
Median income and housing age show regional patterns.

Purpose
Great for learning EDA basics: inspecting data, handling missing values, and preparing for machine learning.



Movie Data Analysis (TMDB Dataset)
Overview
A deep dive into 44,691 movies from the TMDb (The Movie Database) API, analyzing financial performance, popularity, and audience ratings.

Dataset
Source: tmdb_5000_movies.csv (or similar)

Key Insights
High budget doesn’t always mean high revenue — some low-budget films are breakout hits.
Movies released in summer or December tend to earn more.
Audience ratings (vote average) are tightly clustered around 6–7/10.
 Purpose
Ideal for understanding entertainment industry trends and building predictive models (e.g., box office success).

 Tools Used
pandas, matplotlib, seaborn, Jupyter Notebook
  
Join ratings on same users but different movies
Compute cosine similarity:

Filter results for the input movie
Rank and return top 10 most similar movies
