# IPL Score Prediction

## 1. Project Overview
This project aims to predict the total score of a cricket team at the end of their innings during an IPL (Indian Premier League) match. The model is built using historical data from IPL seasons 1 to 9 (2008-2016) and tested on data from season 10 (2017). The model uses various machine learning algorithms to predict the score based on input features such as the batting and bowling teams, overs, runs, wickets, and other match statistics.


## 2. Data Understanding
### 2.1 Data Collection
The dataset used for this project is an IPL dataset (ipl.csv) containing match statistics for each ball bowled in a match. The dataset includes:
●	Batting team

●	Bowling team

●	Overs (current over in the match)

●	Runs scored in that over

●	Wickets taken in that over

●	Runs in last 5 overs

●	Wickets in last 5 overs

●	Total score of the batting team at the end of the innings

●	Date of the match

### 2.2 Data Exploration
●	The dataset contains multiple columns such as match ID, venue, batsman, bowler, striker, non-striker, etc.

●	We perform basic data exploration, such as checking the shape of the dataset, data types, and the first few records, to understand the structure of the data.


## 3. Data Preprocessing
### 3.1 Data Cleaning
●	Removing Unwanted Columns: Columns that are not relevant for predicting the score, such as match ID, venue, batsman, bowler, striker, and non-striker, are removed.

●	Filtering Consistent Teams: Only matches involving consistent teams (e.g., Chennai Super Kings, Mumbai Indians, etc.) are retained.

●	Removing Early Match Data: Data from the first 5 overs of each match is removed to focus on more relevant match situations.

●	Date Conversion: The 'date' column is converted from string format to a datetime object for easier analysis.

### 3.2 Feature Selection
●	Correlation Heatmap: A heatmap is used to visualize the correlation between the features, ensuring the most relevant features are selected for the model.

### 3.3 Encoding Categorical Features
●	One-Hot Encoding: The categorical variables, bat_team and bowl_team, are encoded into numerical features using one-hot encoding. This creates binary columns for each team, representing whether a team is batting or bowling.

### 3.4 Splitting Data into Training and Testing Sets
●	The data is split into a training set (seasons 1-9, i.e., 2008-2016) and a test set (season 10, i.e., 2017). This ensures that the model is trained on historical data and tested on more recent data.



