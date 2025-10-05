# Movie Recommendation System

This project implements a **movie recommendation system** using collaborative filtering techniques with the `Surprise` library in Python. It suggests movies to users based on their past ratings and similarities with other users.

---

## Dataset

The system uses a movie ratings dataset in CSV format containing:

- `userId`: Unique ID for each user  
- `movieId`: Unique ID for each movie  
- `rating`: Rating given by a user (typically 1–5)  
- `title`: Movie title  

The dataset is loaded and analyzed within the notebook.

---

## Features

- **Data Exploration**:  
  - Visualizes rating distributions  
  - Identifies most-rated movies  
  - Analyzes user and movie statistics  

- **Collaborative Filtering Model**:  
  - Uses the `Surprise` library for collaborative filtering  
  - Trains a model to predict user ratings for unseen movies  

- **Evaluation**:  
  - Calculates **RMSE (Root Mean Squared Error)** to assess prediction accuracy  

- **Movie Recommendation**:  
  - Generates personalized movie recommendations for any given user  

---

## Project Structure

- `main.ipynb` – Jupyter Notebook containing the full workflow:  
  1. Loading and exploring the dataset  
  2. Preprocessing the data for modeling  
  3. Training and evaluating a collaborative filtering model  
  4. Recommending movies for users  

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/asicoltd/Movie-Recommendation-System.git
cd Movie-Recommendation-System
````

2. Install dependencies (make sure you have Python 3.x):

```bash
pip install pandas numpy scikit-learn matplotlib seaborn scikit-surprise
```

3. Open the notebook:

```bash
jupyter notebook main.ipynb
```

---

## Usage

1. Explore the dataset and visualize ratings.
2. Train the collaborative filtering model using Surprise.
3. Evaluate the model performance using RMSE.
4. Generate recommendations for a user by calling the recommendation function, e.g.:

```python
recommend_movies(user_id=1, num_recommendations=5)
```

---

## Results

The system can:

* Identify top-rated and most popular movies
* Recommend movies that a user is likely to enjoy based on past ratings
* Provide RMSE as an evaluation metric for prediction accuracy

---
