# Anime Recommendation System using Content-Based Filtering
This project builds a Content-Based Recommender System using anime metadata and user ratings. It provides personalized anime suggestions by measuring similarity between titles based on genres, types, and other textual features.

🤖 What is a Recommender System?
A recommender system is an algorithm designed to suggest relevant items to users. These systems are widely used in platforms like Netflix, Amazon, and Spotify to personalize user experiences.

🔸 Types of Recommender Systems:
Content-Based Filtering:
Recommends items similar to those the user has liked in the past, based on item features.

Collaborative Filtering:
Recommends items based on user behavior patterns and ratings (e.g., users who liked X also liked Y).

Hybrid Models:
Combines content-based and collaborative filtering for better performance.

📁 Dataset Overview
File Used: anime.csv

Features Included:

anime_id

name

genre

type (TV, Movie, OVA, etc.)

episodes

rating (user rating score)

members (popularity based on user counts)

📊 Project Workflow
1. Data Loading and Exploration
Loaded the anime dataset using pandas

Inspected dataset structure with .info() and .describe()

Verified presence of key fields such as genre and rating

2. Data Cleaning and Preprocessing
Removed duplicates and rows with missing genre or name

Standardized and cleaned genre text for consistency

Extracted useful features for content similarity

3. Feature Engineering
Used TF-IDF Vectorizer to convert textual genres into numerical vectors

Computed cosine similarity between anime based on these vectors

4. Recommendation Function
Built a function to:

Take an anime title as input

Retrieve top N most similar anime using cosine similarity

Returns a list of recommendations with matching scores

🔎 Why Content-Based Filtering?
Requires only item metadata (e.g., genres, type) — no user history needed

Works well for cold-start items (new anime with no user ratings)

Easy to interpret and explain to end users

🧠 Sample Use Case
Input: "Naruto"

Output: Top 10 anime with similar genre composition and popularity

🛠️ Libraries Used
pandas, numpy – data loading and manipulation

scikit-learn – TfidfVectorizer, cosine similarity

scipy.stats – skewness checks and data validation

📂 Files
recomender_anime.ipynb — Notebook containing complete implementation

anime.csv — Dataset with anime metadata

📌 Key Takeaways
TF-IDF + Cosine Similarity is a simple yet powerful way to build a content-based recommender.

Genre-based recommendations provide good results when user data is unavailable.

Easy to expand into hybrid models by adding user ratings or collaborative signals.
