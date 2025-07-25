1. Project Title: KNN Regression - Predicting House Prices (California Housing)

2. Objective:
   The goal of this project was to predict the median house value in California districts using K-Nearest Neighbors Regression. The prediction is based on 8 features like median income, average number of rooms, population, etc.

3. Dataset:
   I used the California Housing dataset from sklearn.datasets. It contains 20,640 samples and 8 numerical features. The target variable is median_house_value, which is scaled in 100,000s of dollars.

4. Steps Followed:

   a. Loaded the dataset using fetch_california_housing()
   b. Performed EDA: checked shape, feature info, target distribution
   c. Scaled the features using StandardScaler to ensure fair distance-based comparison
   d. Split the data into train-test sets (80-20 split)
   e. Trained a baseline KNeighborsRegressor model (with k=5)
   f. Evaluated performance using R² score, MAE, MSE, RMSE
   g. Tuned the hyperparameter k by plotting error metrics for values from 1 to 30
   h. Found that k=14 gave the best performance
   i. Trained and saved the final model using joblib

5. Metrics:

   Final model performance with k=14

   * R² Score: 0.6835
   * MAE: 0.44
   * MSE: 0.41
   * RMSE: 0.64

6. Observations:

   * After tuning, model performance improved slightly.
   * R² score shows that 68% of the variance in house prices is explained by the features.
   * RMSE of 0.64 means the average prediction error is around \$64,000, which is decent considering the natural variance in housing data.

7. Why KNN:

    KNN is simple, intuitive, and non-parametric.
    It works well for problems where similar input patterns are expected to give similar outputs.
    However, it is sensitive to feature scale and suffers in high-dimensional or sparse data.
    This made it a good starting point for this regression task.

8. Plot:

   I plotted both R² Score and RMSE vs. k values. This helped visually identify the best k`.
   From the graphs, k=14 showed the highest R² and lowest RMSE.

9. Conclusion:

   This project helped me understand how KNN can be applied to regression problems and how important scaling and hyperparameter tuning are. Though KNN is not the most powerful for large regression tasks, it performs reasonably well with careful preprocessing and tuning.

10. Model:

Final trained model is saved as knn_regressor_california.pkl using joblib for later reuse.


