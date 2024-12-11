What the Code Does
This project implements a recommendation system to predict movie ratings using a technique called Matrix Factorization with Singular Value Decomposition (SVD). The core idea behind this approach is to predict missing ratings in a user-item matrix, which is often sparse (many missing ratings). Here's a breakdown of what the code does:

Data Preprocessing: The code begins by loading a movie ratings dataset and performing basic data cleaning. It removes any missing values and duplicates to ensure that the data used for training the model is clean.

Matrix Normalization: The user-item matrix, which represents ratings of movies by users, is normalized by subtracting the average rating for each user. This step helps in removing biases in individual users' rating patterns, ensuring more accurate predictions.

Matrix Factorization using SVD: The heart of the model is the Singular Value Decomposition (SVD) technique. The matrix is decomposed into three smaller matrices, capturing the underlying patterns of user preferences and item characteristics. By using only the top k singular values, we reduce the dimensionality and make the problem computationally feasible.

Rating Prediction: Using the decomposed matrices, the code reconstructs the rating matrix and predicts missing ratings that were not present in the original dataset.

Model Evaluation: The model is evaluated by calculating two common metrics used in regression tasks: Root Mean Squared Error (RMSE) and Mean Absolute Error (MAE). These metrics help assess how well the predicted ratings match the actual ratings.

Visualization: The code generates a scatter plot comparing the actual ratings to the predicted ratings, along with a perfect prediction line. This visual representation helps to quickly evaluate the model’s performance and see how closely the predictions align with real user ratings.

Through this approach, the project demonstrates how to build a simple but effective movie recommendation system using SVD for matrix factorization.
