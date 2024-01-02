# Movie Recommendation System

This project implements a Machine Learning-based Movie Recommendation System using popular Python libraries like scikit-learn, NumPy, and Pandas. The system leverages vectorized representation and cosine similarity to suggest movies similar to a given input movie.

## Overview

The recommendation system uses a dataset of movies and their features, and it employs machine learning techniques to determine similarity between movies. In this example, we'll use the movie "Iron Man" to demonstrate how the system suggests movies that share similarities.

## Features

- **Scikit-learn:** Utilizes scikit-learn for machine learning functionalities.
- **NumPy:** For efficient numerical operations and array manipulation.
- **Pandas:** For data manipulation and preprocessing.
- **Vectorized Representation:** Movies are represented as vectors to capture features.
- **Cosine Similarity:** Computes similarity between movies using cosine similarity metric.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/movie-recommendation-system.git
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Load the dataset:

    ```python
    import pandas as pd

    # Load your dataset
    dataset = pd.read_csv('movie_dataset.csv')
    ```

2. Use the Recommendation System:

    ```python
    from recommendation_system import MovieRecommendationSystem

    # Create an instance of the recommendation system
    recommender = MovieRecommendationSystem(dataset)

    # Get movie recommendations for "Iron Man"
    recommendations = recommender.get_recommendations("Iron Man")

    print("Recommended Movies:")
    for movie in recommendations:
        print("-", movie)
    ```

## Example

```python
# Example of using the Movie Recommendation System

from recommendation_system import MovieRecommendationSystem

# Assuming you have loaded your dataset into 'dataset'
recommender = MovieRecommendationSystem(dataset)

# Get recommendations for "Iron Man"
iron_man_recommendations = recommender.get_recommendations("Iron Man")

print("Recommended Movies for Iron Man:")
for movie in iron_man_recommendations:
    print("-", movie)
