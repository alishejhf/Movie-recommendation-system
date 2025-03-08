# Movie-recommendation-system

## Overview
This project implements a movie recommendation system using K-Means clustering and cosine similarity. It clusters users based on their movie ratings and then recommends similar movies using cosine similarity.

## Dataset
The dataset consists of two main CSV files:

1. **Ratings Data (`ratings.csv`)**
   - `userId`: ID of the user.
   - `movieId`: ID of the movie.
   - `rating`: Rating given by the user (on a scale of 0.5 to 5.0).
   - `timestamp`: Timestamp of when the rating was given.

2. **Movies Data (`movies.csv`)**
   - `movieId`: iD of the movie.
   - `title`: Title of the movie.
   - `genres`: Genres associated with the movie.
  
## How It Works

### 1. Data Preprocessing
- A **user-movie matrix** is created, where rows represent users and columns represent movies.

### 2. K-Means Clustering
- The **Elbow Method** is used to determine the optimal number of clusters.
- The dataset is clustered into **7 user groups** using the K-Means algorithm.
- Each user is assigned a cluster based on their movie preferences.

### 3. Movie Recommendations
- A **cosine similarity matrix** is calculated for movies based on user ratings.
- For each cluster, the **top 3 highest-rated movies** are selected.
- For each of these movies, the **5 most similar movies** are recommended based on cosine similarity.

## Sample Output
```
Cluster #0:
- If you liked **Five Easy Pieces (1970)**, you might also like: Ruby in Paradise (1993), Out of the Past (1947), Affliction (1997), Days of Heaven (1978), Only the Lonely (1991)
- If you liked **Paths of Glory (1957)**, you might also like: Gerry (2002), Leaves of Grass (2009), Begin Again (2013), Maze Runner: Scorch Trials (2015), Manchester by the Sea (2016)
- If you liked **All Quiet on the Western Front (1930)**, you might also like: Henry V (1989), Last Picture Show, The (1971), Intimate Strangers (Confidences trop intimes) (2004), Assassination of Richard Nixon, The (2004), Nobody Knows (Dare mo shiranai) (2004)
```

## Author
**Alisher Aldamzharov**
