# Roundhay - A Movie Recommendation System

Roundhay is a personalized **hybrid recommendation system** which combines both **content-based filtering** and **collaborative filtering** to generate movie recommendations. This repository provides an overview of how the system works, its approaches, and important concepts used throughout the project.

---

## Overview

Recommender systems can generally be classified into three types:

1. **Content-Based Filtering**  
   Recommends items that share attributes or features with items the user has liked in the past.

2. **Collaborative Filtering**  
   Recommends items based on user preferences:
   - **User-based**: Finds users with similar likes and suggests items they also liked.
   - **Item-based**: Finds items that are frequently liked together.

3. **Hybrid Systems**  
   Combines the strengths of content-based and collaborative filtering to produce better recommendations.

### Pros and Cons of Hybrid Systems

- **Pros**  
  - **Accuracy**: Often yield better recommendations than standalone systems.  
  - **Robustness**: Combining multiple methods helps minimize the weaknesses of each individual technique.

- **Cons**  
  - **Complexity**: Can be computationally expensive to implement and maintain multiple systems.  
  - **Tuning**: Requires careful optimization of thresholds or weights to achieve the best performance.

---

## Weighted Hybrid Recommendation System

In this project, I have implemented a **weighted hybrid recommendation system**, combining collaborative filtering and content-based filtering using a weighted score:

Shybrid = w1 x Scollab + w2 x Scontent

Where:
- \( Shybrid \) is the overall hybrid score.
- \( Scollab \) is the score from collaborative filtering.
- \( Scontent \) is the score from content-based filtering.
- \( w1 + w2 = 1 \).

The system predicts how a user would rate an item by:
- Analyzing ratings from similar users/items (**Collaborative Filtering**).
- Focusing on item attributes and a user’s past interactions (**Content-Based Filtering**).

---

## Glossary

### A) Cosine Similarity

A built-in function from `sklearn` that measures the similarity between two vectors by computing the cosine of the angle between them:

Cosine_similary (A,B) = A • B / ||A|| x ||B||

- **1** implies the vectors have the same direction (maximum similarity).  
- **0** implies the vectors are perpendicular (no similarity).  
- **-1** implies the vectors are opposite (for ratings only).

### B) One-Hot Encoding

A method of converting categorical variables into a binary vector, allowing machine learning algorithms to process and improve predictions.

---

## Dataset

The dataset used in this project is from **MovieLens**, which provides a large set of user ratings and metadata for movies.  
[MovieLens Dataset](https://grouplens.org/datasets/movielens/)

---
