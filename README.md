# Movie Recommendation System

## Overview

This project is a movie recommendation system that uses collaborative filtering, specifically the Singular Value Decomposition (SVD) algorithm, to provide personalized movie recommendations. Inspired by concepts taught at a university level, this system implements a real-world collaborative filtering approach using a machine learning model trained with user-generated ratings data.

## How It Works

The recommendation system works by analyzing user-item interactions (ratings) to learn latent factors that represent both users and items. These latent factors are then used to predict unknown ratings and generate personalized movie recommendations for users. The system updates in real-time, incorporating new user ratings to continually refine the recommendations.

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

## Setup and Operation

### Prerequisites

Ensure you have the following libraries installed:
- pandas
- surprise
- tabulate

You can install them using pip:
```bash
pip install pandas surprise tabulate
