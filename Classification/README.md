classification

K-Nearest Neighbors (KNN) Classification - Iris Dataset

1. Project Overview  
This project is about using the K-Nearest Neighbors (KNN) algorithm to classify iris flowers into one of three species: Setosa, Versicolor, or Virginica. The classification is based on four numerical features — sepal length, sepal width, petal length, and petal width.

2. Objective  
The goal is to predict the correct species of a flower based on its measurements using KNN, understand how distance-based classification works, and tune the model to get the best performance.

3. Dataset  
- Built-in iris dataset from sklearn  
- 150 total samples  
- 4 features per sample (all numeric)  
- 3 target classes (0 = Setosa, 1 = Versicolor, 2 = Virginica)

4. Steps Followed

4.1 Loading and Exploring the Data  
Used sklearn's load_iris function to load the data.  
Checked feature names, class distribution, and printed a few rows.  
Converted it into a pandas DataFrame for easier manipulation and added species names.  
Used pairplot to see how features separate the classes.

4.2 Preprocessing  
Split the dataset into training and testing sets (80/20 split) using train_test_split.  
Applied feature scaling using StandardScaler because KNN relies on distance and unscaled features can mislead the model.

4.3 Model Building  
Initialized a KNeighborsClassifier model with k=3 as a starting point.  
Trained the model on scaled training data.  
Predicted on the test set and evaluated using accuracy score, confusion matrix, and classification report.

4.4 Tuning K (Hyperparameter)  
Tested k values from 1 to 20.  
Plotted k vs test accuracy.  
Selected the best k based on maximum accuracy from the graph.  
Retrained the model using the selected value of k.

4.5 Saving the Final Model  
Used joblib to save both the final trained model and the scaler.  
This allows future predictions without retraining the model or redoing the preprocessing.

5. Evaluation  
The model gave high accuracy on the test set.  
Setosa was classified perfectly.  
Some minor confusion was observed between Versicolor and Virginica which is expected due to overlapping features.  
Overall performance was good and the classifier generalizes well.


# Conclusion  
This mini-project helped me understand how KNN works on a real-world dataset. I learned the importance of scaling features, tuning the number of neighbors, evaluating performance using different metrics, and saving models for future use.
