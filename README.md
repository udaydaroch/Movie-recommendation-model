# Movie Recommendation System

## Overview

This project is a movie recommendation system that uses collaborative filtering, specifically the Singular Value Decomposition (SVD) algorithm, to provide personalized movie recommendations. Inspired by concepts taught at a university level, this system implements a real-world collaborative filtering approach using a machine learning model trained with user-generated ratings data.

## How It Works

The recommendation system works by analyzing user-item interactions (ratings) to learn latent factors that represent both users and items. These latent factors are then used to predict unknown ratings and generate personalized movie recommendations for users. The system updates in real-time, incorporating new user ratings to continually refine the recommendations.

### Detailed Explanation of the SVD Model

1. **User-Item Interaction Matrix:**
   - The system starts with a matrix where rows represent users and columns represent movies. The entries in this matrix are the ratings given by users to movies.

   R = [ 5 3 0 ]
       [ 4 0 0 ]
       [ 1 1 0 ]

2. **Matrix Factorization:**
   - Using SVD, the interaction matrix \( R \) is decomposed into three matrices \( U \), \( \Sigma \), and \( V^T \):

   \[
   R \approx U \Sigma V^T 
   \]

   - \( U \): User matrix representing users in the latent feature space.
   - \( \Sigma \): Diagonal matrix with singular values representing the importance of each latent feature.
   - \( V^T \): Movie matrix representing movies in the latent feature space.

3. **Latent Features:**
   - **User Latent Features (U):** Capture user preferences.
   - **Movie Latent Features (V^T):** Capture movie characteristics.

4. **Prediction:**
   - The predicted rating for a user and a movie is computed by the dot product of the user's and movie's latent feature vectors.

   \[
   \hat{r}_{ui} = U_u \cdot V_i
   \]

5. **Model Training:**
   - The model is trained on the existing ratings data to learn these latent features. The Surprise library is used for this purpose.

### Real-time Updates

- The model retrains with new user ratings, ensuring the recommendations remain up-to-date.

## Features

- **Collaborative Filtering**: Utilizes the SVD algorithm for collaborative filtering.
- **Real-time Updates**: The model retrains with new user ratings, ensuring up-to-date recommendations.
- **Excludes Rated Movies**: Recommendations exclude movies the user has already rated or disliked.
- **Genre-based Filtering**: Users can filter recommendations by their preferred genre.
- **Interactive User Experience**: Users can rate movies and receive new recommendations based on their updated preferences.

## Technologies Used

- **Python**: Programming language for the implementation.
- **Surprise Library**: For building and training the SVD model.
- **Pandas**: For data manipulation and handling.
- **Tabulate**: For displaying tabular data in a readable format.

## Data

Initially, the system is trained using generated fake data. However, it will be trained with real data soon to provide more accurate and realistic recommendations.

### Example of Generated Data

1. **Movies Data:**
   - A list of movies with metadata such as movie ID, title, genres, director, actors, release year, plot summary, duration, language, country, and average rating.

2. **Ratings Data:**
   - User interactions with movies, represented by user ID, movie ID, rating, and timestamp.

## Setup and Operation

### Prerequisites

Ensure you have the following libraries installed:
- pandas
- surprise
- tabulate

You can install them using pip:
```bash
pip install pandas surprise tabulate
