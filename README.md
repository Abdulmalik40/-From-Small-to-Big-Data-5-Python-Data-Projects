
 
 
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
  
 PySpark projects:

 Movie Recommendation System

Uses MovieLens 100K
 dataset.

Spark Projects: Degrees of Separation & Movie Recommendations
Two powerful Apache Spark applications demonstrating graph processing and collaborative filtering for recommendations.

Built using PySpark, these projects analyze large-scale datasets to solve real-world problems:

Find the shortest path between fictional characters (BFS in Spark)
Recommend similar movies using cosine similarity
 Project 1: Degrees of Separation (Marvel Superheroes)
 Problem
How many degrees of separation are there between two Marvel characters based on comic book co-appearances?

This project implements a Breadth-First Search (BFS) algorithm on a graph of superheroes to find the shortest path from a starting character to a target.

 Dataset
marvel-graph.txt: A tab-separated file where:
First column = Hero ID
Subsequent columns = IDs of heroes they appeared with
Inspired by Marvel Comics data from the Stanford Network Analysis Project (SNAP) 

 How It Works
Start: Character ID 5306 (e.g., Loki)
Target: Character ID 14 (e.g., Spider-Man)
Uses BFS iterations to propagate through the graph
Employs a Spark accumulator to detect when the target is found
Nodes are colored:
GRAY: Being explored
BLACK: Already processed
WHITE: Not yet discovered
🛠️ Key Spark Concepts Used
flatMap() for spreading the search
reduceByKey() to merge duplicate nodes
Accumulators for global counters
In-memory distributed graph traversal

 Project 2: Movie Recommendation System
 Problem
Given a movie, recommend other movies that are most similar in terms of user ratings.

Uses cosine similarity to compute how closely two movies are rated across users.

 Dataset
ml-100k/u.data: User ratings (user ID, movie ID, rating, timestamp)
ml-100k/u.item: Movie metadata (ID, title, genre, etc.)
From the classic MovieLens 100K dataset
 How It Works
Join ratings on same users but different movies
Compute cosine similarity:

Filter results for the input movie
Rank and return top 10 most similar movies
