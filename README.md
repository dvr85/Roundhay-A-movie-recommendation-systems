# Roundhay - A movie recommendations system

Roundhay is a personalized hybrid recommendations system which combines both content-based filtering and collaborative filtering. 

# Context

Recommendation systems are classified into:

A) Content-Based Filtering: Recommends the items which are similar to what the user liked in the past by analyzing the item’s attributes.

B) Collaborative Filtering: Recommends the items based on the user’s preferences; either user-based which finds the similar users with same likes or item-based which finds items that are often liked together.

C) Hybrid Systems: Recommends the items by combining both content-based filtering and collaborative filtering to leverage the combined strengths of the individual filtering techniques.

Pros of Hybrid Systems:

* Accuracy: Better recommendations than the standalone systems.
* Robustness: Combinations of the filtering methods minimizes the weakness of individual techniques.

Cons of Hybrid Systems:

* Complexity: Computationally expensive while implementing and maintaining multiple systems.
* Tuning: Demands careful tuning of thresholds or weights to optimize performance.


There are several approaches of hybrid systems. In this project, I have used weighted hybrid recommendations system.


Weighted Hybrid Recommendations System:

A hybrid recommendation technique which utilizes the weighted sum of separate recommendation scores. 

Shybrid = w1 x Scollab + w2 x Scontent

Where,
	Shybrid = Score of Hybrid Systems (Weight sum of individual scores).
	 Scollab = Score of Collabrative Filtering.
	Scontent = Score of Content based Filtering.
	w1 + w2 = 1

In this project, we predict how a user would rate an item based on ratings from similar users or items (Collaborative Filtering) and focuses on item attributes and the past interactions of the user (Content-based Filtering).


# Glossary:

A) Cosine Similarity:

A build-in function from sklearn which measures the similarity between two vectors which calculates the cosine angle between the vectors. 

Cosine_similary (A,B) = A • B / ||A|| x ||B||

If cosine similarity = 1, the two vectors are exactly the same direction (Maximum similarity).
If cosine  similarity = 0, the two vectors are perpendicular to each other (No similarity).
If cosine  similarity = -1, the two vectors are opposite (For ratings only).

B) One-Hot Encoding:

This encoding converts the categorical variable into binary form which can be provided to machine learning algorithms to improve predictions.


Dataset:

MovieLens : https://grouplens.org/datasets/movielens/
