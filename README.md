# Movie-Recommendation-system
MovieLens 100k Movie Recommendation System

Overview

A user-based collaborative filtering system for recommending movies using the MovieLens 100k dataset
.
It predicts which movies a user may like based on ratings from similar users.

Features

User-Movie rating matrix

Cosine similarity between users

Top-N personalized recommendations

Model evaluation using Precision@K

Data visualization for ratings, genres, and user demographics

Dataset

Users: u.user – age, gender, occupation

Movies: u.item – title, genres, IMDb link

Ratings: u.data, u1.base, u1.test – user ratings

Installation
git clone <repository-url>
pip install pandas numpy matplotlib seaborn scikit-learn


Place the dataset in:

Downloads/archive (2)/ml-100k/

Usage
from recommendation_system import load_data, create_user_item_matrix, get_recommendations

train_df, test_df = load_data()
train_user_item_matrix = create_user_item_matrix(train_df)
recommendations = get_recommendations(user_id=69, user_item_matrix=train_user_item_matrix, user_similarity_df=user_similarity_df, n_recommendations=10)
print(recommendations)

Visualizations

Movie rating distribution

Number of ratings per movie

User age and gender distribution

Genre distribution

Ratings by gender for top movies

Evaluation

Uses Precision@K metric

Considers movies with rating ≥ 4 as relevant

Average precision calculated for all users in the test set

Libraries

pandas, numpy

matplotlib, seaborn

scikit-learn
