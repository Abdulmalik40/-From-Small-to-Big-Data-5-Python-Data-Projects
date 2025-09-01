
 
 
 
 PySpark projects:

 Movie Recommendation System

Uses MovieLens 100K
 dataset.

Computes cosine similarity between movies based on user ratings.

Returns Top 10 similar movies for a given movie ID.

Run:

spark-submit movie_recommendation.py

 Degrees of Separation (Marvel Graph BFS)

Runs Breadth-First Search on the Marvel superhero graph (marvel-graph.txt).

Finds the shortest path (degrees) between two characters.

Uses Spark accumulators to detect target character.

Run:

spark-submit degrees_of_separation.py

Requirements

Python 3.x

Apache Spark

Datasets: ml-100k and marvel-graph.txt
