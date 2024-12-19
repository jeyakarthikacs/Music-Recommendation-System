# Music Recommendation System

This project demonstrates a basic implementation of a Song Recommendation System using collaborative filtering techniques. The system generates recommendations for both new and existing users based on user preferences or their past ratings. The recommendations are presented visually using bar plots to show predicted scores or accuracies for recommended songs.

## Features

1. **User-User Collaborative Filtering:**
   - Recommends songs for new users based on their preferences and similarities with existing users.

2. **Item-Item Collaborative Filtering:**
   - Recommends songs for existing users based on the similarity between songs they have already rated.

3. **Visualization:**
   - Displays the recommendation scores using bar plots for better interpretability.

## Installation

### Prerequisites
- Python 3.6 or later
- Required Python libraries:
  - pandas
  - numpy
  - scikit-learn
  - matplotlib

Install the required libraries using the following command:

```bash
pip install pandas numpy scikit-learn matplotlib
```

## Usage

### Code Execution
1. Clone the repository and navigate to the project directory.
2. Run the Python script to execute the recommendation system.

```bash
python song_recommendation.py
```

### Input and Output

#### Input:
- **Existing User:** Provide the `user_id` for whom recommendations should be generated.
- **New User:** Provide a list of `song_id`s (preferences) to generate recommendations.

#### Output:
- Recommendations are displayed in the console and visualized using bar plots.

#### Output:
Console output with recommendations:
```text
Item-Item Filtering Recommendations (Existing User):
17    0.902443
6     0.625021
19    0.624695
15    0.588148
8     0.582482
dtype: float64

User-User Filtering Recommendations (New User):
26    7.0
9     6.0
17    6.0
7     5.0
8     5.0
dtype: float64
```

Bar plots showing the recommended songs with predicted scores.

## Functions

### `get_user_user_recommendations_for_new_user(preferences)`
Generates song recommendations for a new user based on their preferences.

**Parameters:**
- `preferences` (list): A list of song IDs representing the user's preferences.

**Returns:**
- A Series of recommended song IDs with their scores.

### `get_item_item_recommendations_for_existing_user(user_id)`
Generates song recommendations for an existing user based on their past ratings.

**Parameters:**
- `user_id` (int): The ID of the user.

**Returns:**
- A Series of recommended song IDs with their scores.

### `plot_song_accuracy_comparisons(recommendations, title)`
Visualizes the recommendation scores as a bar plot.

**Parameters:**
- `recommendations` (Series): A Series of recommended song IDs with their scores.
- `title` (str): The title of the plot.

### `recommend_songs(user_id=None, preferences=None)`
Generates recommendations for either an existing user or a new user.

**Parameters:**
- `user_id` (int, optional): The ID of the existing user. Defaults to `None`.
- `preferences` (list, optional): A list of song IDs representing the new user's preferences. Defaults to `None`.

**Returns:**
- A Series of recommended song IDs with their scores.
