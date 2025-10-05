# Movie Recommendation System

This project implements a **movie recommendation system** using collaborative filtering techniques with the `Surprise` library and deep learning for Neural Matrix Factorization (NeuMF). It suggests movies to users based on their past ratings and similarities with other users.

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

- **Recommendation Models**:  
  The system evaluates multiple models:  

  - **User-Based Collaborative Filtering (UBCF)**: Finds similar users and recommends their liked items  
  - **Item-Based Collaborative Filtering (IBCF)**: Recommends items similar to the user’s historical preferences  
  - **SVD (Singular Value Decomposition)**: Matrix factorization to discover latent patterns in user-item interactions  
  - **NeuMF (Neural Matrix Factorization)**: Combines Generalized Matrix Factorization (GMF) and Multi-Layer Perceptron (MLP) components for neural recommendation  

- **Evaluation**:  
  The system evaluates model performance using **top-K recommendation metrics**:  
  - **Precision@K** – fraction of recommended items in the top K that are relevant  
  - **Recall@K** – fraction of relevant items retrieved in the top K  
  - **NDCG@K** – normalized discounted cumulative gain, accounting for ranking position  

  **K-values evaluated:** `[5, 10, 15, 20]`  

  The evaluation generates visual comparison plots:  
  - `ModelCompK10.png` – compares models at K=10  
  - `performance.png` – radar chart showing Precision, Recall, and NDCG for all models  
  - Additional plots for each metric across different K-values  

- **Movie Recommendation**:  
  - Generates personalized movie recommendations for any user based on the trained models  

---

## Project Structure

- `main.ipynb` – Jupyter Notebook containing the full workflow:  
  1. Loading and exploring the dataset  
  2. Preprocessing the data for modeling  
  3. Training and evaluating multiple recommendation models  
  4. Evaluating top-K recommendation metrics (Precision, Recall, NDCG)  
  5. Generating visual comparison plots  
  6. Recommending movies for users  

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/asicoltd/Movie-Recommendation-System.git
cd Movie-Recommendation-System
````

2. Install dependencies (make sure you have Python 3.x):

```bash
pip install pandas numpy scikit-learn matplotlib seaborn scikit-surprise tensorflow
```

3. Open the notebook:

```bash
jupyter notebook main.ipynb
```

---

## Usage

1. Explore the dataset and visualize ratings.
2. Train the recommendation models (UBCF, IBCF, SVD, NeuMF).
3. Evaluate model performance using **Precision@K, Recall@K, and NDCG@K**.
4. Generate plots comparing models and metrics for multiple K-values.
5. Generate personalized recommendations for a user, e.g.:

```python
recommend_movies(user_id=1, num_recommendations=5)
```

---

## Results

The system can:

* Identify top-rated and most popular movies
* Recommend movies that a user is likely to enjoy based on past ratings
* Compare multiple models using **Precision@K, Recall@K, and NDCG@K**
* Visualize model performance across K-values with comparison plots

---
