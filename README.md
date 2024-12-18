# Movie Recommender System

## Overview
The Movie Recommender System is a hybrid recommendation system that combines **demographic data** and **user preferences** to provide highly personalized movie suggestions. It uses **Singular Value Decomposition (SVD)** for collaborative filtering and incorporates user feedback for real-time refinement of recommendations.

## Objectives
- Build a recommendation system that leverages **age groups** and **user feedback**.
- Use collaborative filtering to predict ratings for unseen movies.
- Provide an interactive experience for users to rate movies and get personalized recommendations.

## Features
1. **Age-Based Recommendations**:
   - Recommends movies highly rated by users in the same age group as the target user.
2. **Personalized Recommendations**:
   - Users rate a subset of movies and the system refines its recommendations based on their feedback.
3. **Interactive Workflow**:
   - Users can input their age and rate movies in real time, enhancing engagement and accuracy.

## Dataset
The project uses the **MovieLens 100k dataset**, which includes:
- **User data (`u.user`)**: Contains demographics like age, gender and occupation.
- **Movie data (`u.item`)**: Includes movie titles and metadata.
- **Ratings data (`u.data`)**: User-item interactions with ratings on a scale of 1–5.

## How It Works
1. **Data Preprocessing**:
   - Merge user demographics, movie metadata and user-item interaction data.
   - Bin users into age groups (e.g., `18-24`, `25-34`).
2. **Model Training**:
   - Train an SVD model using the Surprise library to predict ratings for unseen movies.
3. **Interactive Recommendation**:
   - Step 1: Recommend movies based on the user's age group.
   - Step 2: Collect user feedback by asking for ratings of recommended movies.
   - Step 3: Refine recommendations using collaborative filtering.

## Technologies Used
- **Python**: Programming language.
- **Surprise Library**: For collaborative filtering with SVD.
- **Pandas and NumPy**: For data preprocessing and manipulation.


## Example Workflow
1. Enter your age: `29`
   - Output: Age-group recommendations based on the `25-34` group.
2. Rate movies:
   - Input ratings for movies like *Star Wars (1977)* or *The Godfather (1972)*.
3. View final recommendations:
   - Output includes personalized movie suggestions with predicted ratings.

## Results
The system combines demographic data and user preferences to:
- Recommend relevant and diverse movies.
- Improve accuracy through feedback-driven refinement.


```

## Future Enhancements
1. **Cold-Start Problem**:
   - Add content-based filtering to recommend movies for users with no prior interactions.
2. **Real-Time Feedback**:
   - Allow users to continuously refine recommendations based on dynamic feedback.
3. **Scalability**:
   - Test the system on larger datasets like MovieLens 1M or Netflix Prize.


