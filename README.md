# LaughterLens - Personalized Joke Recommendation System

## 📌 Project Description

LaughterLens is a collaborative filtering-based recommendation system designed to predict user preferences for jokes. Utilizing cosine similarity between users' ratings, the system suggests jokes that are most likely to be enjoyed by a particular user. It also provides a baseline comparison using a random recommender system for evaluating prediction accuracy. This project aims to offer a personalized joke recommendation experience to users based on their historical preferences.

## 📂 Dataset

The project uses the Jester Dataset (2006-15) which includes user ratings for jokes. The key aspects of the dataset are:

### Contains user ratings where:

- Rows represent individual users.
- Columns represent jokes (150 jokes in total).
- 99 indicates the joke was not rated by the user.
- The first column represents the number of jokes rated by each user.
### Contains the text of the jokes corresponding to the joke indices.

## 📌 Features

- Collaborative Filtering: Uses cosine similarity to find users with similar preferences and predicts ratings based on their ratings.
- **Baseline Comparison:** Implements a random recommender system for comparative analysis.
- **Top-K Similar Users:** Identifies the top 2,000 users most similar to a particular user.
- **Joke Recommendations:** Provides top-N joke recommendations for a specified user.
- **Evaluation Metrics:** Uses Mean Absolute Error (MAE) for evaluating prediction performance.

## 📂 Project Structure
```
│── LaughterLens
│   │── README.md                  # Project documentation
│   │── FINAL jester 2006-15.csv    # Joke ratings dataset
│   │── Dataset3JokeSet.csv         # Joke text dataset
│   │── RecommendationSystem.ipynb        # Main Python script for recommendation system
│   │── requirements.txt            # Dependencies
```
## 🔍 Requirements

- Python 3.x
- pandas
- numpy
- scikit-learn

### Install the dependencies via:
```
pip install -r requirements.txt
```

## 🚀 Usage

- Place the dataset files (FINAL jester 2006-15.csv and Dataset3JokeSet.csv) in the same directory as recpmmendationSystem.ipynb.
- Run the joke_recommender.py file to train the model and generate recommendations.

## 📊 Evaluation

**The model is evaluated using Mean Absolute Error (MAE) on the test set. Results are also compared against a baseline random recommender system for performance analysis.**

## 📌 How It Works
## Data Preprocessing:
- Replace 99 values with NaN to identify unrated jokes.
- Filter active users who have rated at least 80 jokes.
- Split the data into training and testing sets.

## Collaborative Filtering:
- Compute user-user similarity using cosine similarity.
- Predict ratings for jokes based on the weighted average of ratings from top-K similar users.

## Baseline System:
-Compare the performance with a random recommender system.

## Top-K User Recommendation:
- Identify and display the top 2,000 most similar users for each user.
  
## Top-N Joke Recommendations:
- Recommend top jokes based on predicted ratings.

## 📌 Future Improvements
- Implement matrix factorization techniques (e.g., SVD, ALS) for improved accuracy.
- Add content-based filtering using joke text data.
- Develop a web-based interface for interactive joke recommendations.

## 💡 Acknowledgments
**This project utilizes the Jester Dataset, a collection of joke ratings gathered from various users.**
