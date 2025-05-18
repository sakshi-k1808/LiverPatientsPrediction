# Liver Patient Prediction

This notebook performs analysis and builds classification models to predict liver patient status using the Indian Liver Patient Dataset.

##  Libraries Used

* `pandas`:  For data manipulation and analysis.
* `numpy`: For numerical computations.
* `seaborn` & `matplotlib.pyplot`: For data visualization.
* `imblearn.over_sampling.SMOTE`:  For handling class imbalance using the SMOTE technique.
* `sklearn.model_selection.train_test_split`: For splitting data into training and testing sets.
* `sklearn.preprocessing.StandardScaler`:  For feature scaling.
* `sklearn.ensemble.RandomForestClassifier`:  For building a Random Forest classification model.
* `sklearn.metrics`: For evaluating model performance (classification report, confusion matrix, accuracy score).
* `sklearn.neighbors.KNeighborsClassifier`:  For building a K-Nearest Neighbors classification model.

## Data

The dataset used is "Indian Liver Patient Dataset (ILPD).csv".  It contains various medical attributes and a target variable indicating liver patient status.

## Data Preprocessing

* Column names are assigned for better readability.
* Missing values in the `Albumin_and_Globulin_Ratio` column are handled (the notebook shows `fillna`).
* The dataset is analyzed for class imbalance. Due to the imbalance (approximately 71% class 1, 29% class 2), SMOTE is used to oversample the minority class.
* Categorical features (`Gender`) are converted into numerical using one-hot encoding.
* Data is split into training and testing sets.
* Features are scaled using StandardScaler.

##  Modeling

* Several classification models are trained and evaluated: Logistic Regression, Decision Tree Classifier, Random Forest Classifier, SVM, and KNN.
* Model performance is assessed using metrics like accuracy, precision, recall, and F1-score, with a focus on the F1-score and recall for the minority class (patients with liver disease) to ensure effective identification of positive cases.

## Results and Recommendations

* **Key Finding:** Models like SVM and KNN, especially when combined with SMOTE, offer a good balance of performance. Logistic Regression is also highlighted as a strong and interpretable alternative.
* **Recommendation:** Prioritize models that maximize the F1-score and recall for class 2 to minimize the risk of failing to identify patients with liver conditions.

##  Notebook Structure

1.  **Basic Checks:** Imports necessary libraries and loads the dataset.
2.  **Data Exploration (EDA):** Analyzes the data (head, shape, info, describe), checks for class distribution, and handles missing values.
3.  **Feature Engineering:** Encodes categorical features and potentially creates new features.
4.  **Data Balancing:** Applies SMOTE to address class imbalance.
5.  **Model Training and Evaluation:** Trains and evaluates various classification models.
6.  **Results and Conclusion:** Summarizes the findings and provides recommendations.# LiverPatientsPrediction
