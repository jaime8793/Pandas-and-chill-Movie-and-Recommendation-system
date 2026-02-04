# Pandas-and-chill-Movie-and-Recommendation-system

# MovieLens Recommendation System

**Team:** Pandas and Chill (GROUP 2)
**Project Phase:** Phase 4 - Advanced Machine Learning
**Date:** February 2026

## Project Overview
This project involves the development of a Collaborative Filtering Recommendation System for "CineStream," a fictional movie streaming platform. By analyzing over 100,000 ratings from the MovieLens dataset, we have built a model capable of generating personalized "Top-5" movie suggestions for users.

The goal is to solve the "choice overload" problem, reducing the time users spend browsing and increasing overall platform engagement.

## Key Objectives
* **Reduce Churn:** Target a 25% reduction in user churn by providing relevant content.
* **Improve UX:** Decrease average browsing time from 20+ minutes to under 5 minutes.
* **Boost Engagement:** Drive a 30% increase in monthly watch time through hyper-personalized suggestions.

## Dataset
We utilized the **MovieLens Small Dataset** provided by the GroupLens Research Lab at the University of Minnesota.
* **Size:** 100,836 ratings and 3,683 tag applications.
* **Dimensions:** 610 users x 9,724 movies.
* **Sparsity:** ~98.3% (Simulates real-world sparse user-item interaction matrices).
* **Files:**
    * `ratings.csv`: User ratings on a 0.5 to 5.0 scale.
    * `movies.csv`: Movie titles and genre metadata.
    * `tags.csv`: User-generated tags.

## Tech Stack & Libraries
The project is implemented in **Python** using Jupyter Notebooks.

* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`, `wordcloud`
* **Machine Learning:** `scikit-learn`
* **Recommendation Engine:** `scikit-surprise` (Industry standard for explicit rating data)

## Installation & Setup

1. **Clone the repository:**
    ```bash
    git clone <repository-url>
    cd movielens-recommendation
    ```

2. **Install dependencies:**
    It is recommended to use a virtual environment.
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn scikit-surprise wordcloud
    ```

3. **Run the Notebook:**
    ```bash
    jupyter notebook Recommendation_systems.ipynb
    ```

## Methodology (CRISP-DM)
This project follows the **Cross-Industry Standard Process for Data Mining (CRISP-DM)** lifecycle:

1. **Business Understanding:** Defined the problem of decision paralysis on streaming platforms.
2. **Data Understanding:** Analyzed rating distributions and calculated matrix sparsity (98.3%).
3. **Data Preparation:** Merged datasets, handled constraints, and prepared the User-Item matrix.
4. **Modeling:** Implemented Collaborative Filtering (KNN/SVD) using the `Surprise` library.
5. **Evaluation:** Assessed model performance using RMSE (Root Mean Squared Error) to ensure rating prediction accuracy.

## Key Insights
* **Rating Bias:** The average movie rating is 3.50, indicating a negative skew where users generally rate movies they enjoy.
* **Sparsity:** The high sparsity confirms the need for matrix factorization or dimensionality reduction techniques rather than simple memory-based lookups.
* **User Behavior:** Explicit ratings provide a strong signal for preference, but the "Long Tail" of movies requires a robust recommendation engine to surface hidden gems.

## Contributors
* **Pandas and Chill (Group 2)**

---
*Disclaimer: This project is for educational purposes as part of the Phase 4 Advanced Machine Learning curriculum.*