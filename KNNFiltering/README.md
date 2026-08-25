
🎬 KNN Movie Recommendation System
📌 Overview

This project is a Movie Recommendation System built using K-Nearest Neighbors (KNN) and Item-Based Collaborative Filtering.

The system recommends movies that are similar to a selected movie based on user rating patterns from the MovieLens dataset.

🎯 Objective

The main goal is to recommend movies that users may like based on how other users have rated similar movies.

📂 Dataset

The project uses two MovieLens datasets:

movies.csv — contains movie IDs and movie titles.
ratings.csv — contains user IDs, movie IDs, and ratings.
🔄 Project Workflow
MovieLens Dataset
       ↓
Load movies and ratings
       ↓
Merge the datasets
       ↓
Count ratings for each movie
       ↓
Filter movies with at least 50 ratings
       ↓
Create Movie-User Rating Matrix
       ↓
Fill missing ratings with 0
       ↓
Convert to Sparse Matrix
       ↓
Apply KNN
       ↓
Use Cosine Distance
       ↓
Find Nearest Movies
       ↓
Generate Recommendations
🛠️ Technologies Used
Python
Pandas
NumPy
SciPy
Scikit-learn
Jupyter Notebook
🤖 Algorithm
K-Nearest Neighbors (KNN)

The NearestNeighbors algorithm is used to find movies that are closest to a selected movie.

The model uses:

NearestNeighbors(
    metric='cosine',
    algorithm='brute'
)

Cosine distance is used to compare the rating patterns of movies.

A smaller distance means the movies are more similar.

📊 Data Processing

Movies with fewer than 50 ratings are removed to reduce the effect of movies with insufficient rating information.

A movie-user matrix is then created:

             User 1  User 2  User 3  ...
Movie A        4       5       0
Movie B        5       4       3
Movie C        0       4       5

Missing ratings are replaced with 0.

The matrix is converted into a CSR sparse matrix for efficient processing.

🎬 Example Recommendation

For the movie Up (2009), the system generated:

WALL·E (2008)
Avatar (2009)
Inception (2010)
Iron Man (2008)
The Dark Knight (2008)

These recommendations are based on the similarity of their user-rating patterns.

🚀 How to Run
Install the required libraries:
pip install pandas numpy scipy scikit-learn jupyter
Open the Jupyter Notebook.
Make sure movies.csv and ratings.csv are available.
Run the notebook cells in order.
The system will generate movie recommendations for a selected movie.
📌 Key Concepts Learned
Data loading and preprocessing
Merging datasets
GroupBy and aggregation
Filtering data
Pivot tables
Sparse matrices
K-Nearest Neighbors
Cosine distance
Item-Based Collaborative Filtering
Movie recommendation systems
