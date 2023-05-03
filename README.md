# aidTech_Movie-Recomendation-System
Movie Recommendation System using K-Nearest Neighbors Algorithm
This is a movie recommendation system that uses the K-Nearest Neighbors algorithm to recommend movies to users based on their ratings of other movies. The dataset used in this system is the movies.csv file, which contains information about movies and user ratings.

The following steps were taken to build the recommendation system:

Load the dataset into a Pandas dataframe.
Check for missing values and duplicates, and remove duplicates.
Convert the dataframe into a pivot table to get the user-item matrix.
Convert the pivot table to a sparse matrix using the csr_matrix function from the scipy.sparse module.
Train the K-Nearest Neighbors model using the sparse matrix and the NearestNeighbors class from the sklearn.neighbors module.
Define a function to get movie recommendations for a movie based on its similarity to other movies.
Define a function to get movie recommendations for a user based on the user's ratings of other movies.
Test the model by getting recommendations for a movie or user.
The get_movie_recommendations function is used to get movie recommendations for a movie. It takes a movie_id parameter and an optional num_recommendations parameter, which specifies the number of recommendations to return (default is 5). The function first finds the k nearest neighbors of the movie using the K-Nearest Neighbors algorithm, then gets the indices of the recommended movies and their titles.

The get_user_recommendations function is used to get movie recommendations for a user. It takes a user_id parameter and an optional num_recommendations parameter, which specifies the number of recommendations to return (default is 5). The function first gets the ratings of the user for all movies, then finds the k nearest neighbors of the user based on these ratings, and finally gets the indices of the recommended movies and their titles.

To evaluate the model's performance, Mean Absolute Error (MAE) or Root Mean Squared Error (RMSE) can be used on a testing set. However, this implementation assumes that there are no users in the dataset, and therefore cannot be evaluated using these metrics.

Overall, this movie recommendation system can be useful for movie streaming platforms to suggest movies to users based on their ratings of other movies.
