# Movie-Rating-Prediction

### Project Overview
In this project, we built a machine learning model to predict movie ratings based on features like Director, Actors, and Movie Name.
We used Random Forest Regressor and handled categorical variables with One-Hot Encoding.

### Tech Stack
- Python
- Pandas
- Scikit-learn (sklearn)
- Jupyter Notebook

### Steps Followed
#### 1. Data Preprocessing
- Selected important features:
['Movie Name', 'Director', 'Actor 1', 'Actor 2', 'Actor 3']
- Target variable:
['Rating']
- Handled categorical data using One-Hot Encoding to convert text into numerical form.

#### 2. Train-Test Split
Divided the dataset into 80% training and 20% testing.

#### 3. Model Building
Used Random Forest Regressor with n_estimators=100 and random_state=42.
Trained the model on preprocessed training data.

#### 4. Evaluation
Calculated two metrics:
RMSE (Root Mean Squared Error): 0.837
R² Score (Coefficient of Determination): 0.27

### Results & Observations
- R² score was low (around 27%), meaning the model explains only a small part of the rating variability.
- RMSE was around 0.837, suggesting that the predictions had a moderate error.
- Model training was slow due to a very large number of features (34694 columns) after One-Hot Encoding.
- High dimensionality caused performance issues and overfitting risk.

### Improvements Suggested
- Feature Engineering: Group rare directors and actors into 'Others' to reduce columns.
- Dimensionality Reduction: Apply PCA or Feature Selection.
- Better Models: Try Gradient Boosting or XGBoost.
- More Features: Add genre, budget, release year, etc., for better predictions.

### Conclusion
We built a Random Forest model to predict movie ratings based on movie-related information.
While the model runs successfully, it struggles due to the high number of features.
Future improvements should focus on reducing dimensions and enhancing feature quality to achieve better accuracy.
