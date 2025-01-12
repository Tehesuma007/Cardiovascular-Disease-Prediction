# Title: Predicting Heart Disease Using Machine Learning

## Overview:
This is an end to end binary classification project that seeks to predict if a patient has heart disease or not based on medical attributes provided in the dataset.
We are going to build our model using the following classifiers: Logistic Regression Classifier, KNeighbors Classifier and Random Forest Classifier

## Approach
1. Problem definition
2. Features
3. Data Overview and Exploration
4. Data Cleaning and Feature Engineering
5. Data Visualization
6. Modelling
7. Hyperparemeter Tuning
8. Evaluation
9. Feature Importance

## Tools and Libraries
- Pandas
- Numpy
- Scikit-learn
- Matplotlib


### 1. Problem Definition
>In a statement,
Given clinical parameters about a patient, can we predict whether or not they have heart disease?

### 2. Features
This is where we will get different information about each of the features in our data

**Let's Create a data dictionary**

- age - Patient age in years  <br/>
- sex - (1 = male; 0 = female) <br/>
- cp - chest pain type <br/>
   * 0: Typical angina: chest pain related decrease blood supply to the heart <br/>
   * 1: Atypical angina: chest pain not related to heart <br/>
   * 2: Non-anginal pain: typically esophageal spasms (non heart related) <br/>
   * 3: Asymptomatic: chest pain not showing signs of disease <br/>
- trestbps - resting blood pressure (in mm Hg on admission to the hospital) <br/> 
   * anything above 130-140 is typically cause for concern <br/>
- chol - serum cholestoral in mg/dl <br/>
- serum = LDL + HDL + .2 * triglycerides <br/>
   * above 200 is cause for concern <br/>
- fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) <br/>
   * >126' mg/dL signals diabetes <br/>
- restecg - resting electrocardiographic results <br/>
   - 0: Nothing to note <br/>
   - 1: ST-T Wave abnormality <br/>
         - can range from mild symptoms to severe problems <br/>
         - signals non-normal heart beat <br/>
   - 2: Possible or definite left ventricular hypertrophy <br/>
         - Enlarged heart's main pumping chamber <br/>
- thalach - maximum heart rate achieved <br/>
- exang - exercise induced angina (1 = yes; 0 = no) <br/>
- oldpeak - ST depression induced by exercise relative to rest looks at stress of heart during excercise unhealthy heart will stress more <br/>
- slope - the slope of the peak exercise ST segment <br/>
  * 0: Upsloping: better heart rate with excercise (uncommon) <br/>
  * 1: Flatsloping: minimal change (typical healthy heart) <br/>
  * 2: Downsloping: signs of unhealthy heart <br/>
- ca - number of major vessels (0-3) colored by flourosopy <br/>
  * colored vessel means the doctor can see the blood passing through <br/>
  * the more blood movement the better (no clots) <br/>
- thal - thalium stress result <br/>
  * 1,3: normal <br/>
  * 6: fixed defect: used to be defect but ok now <br/>
  * 7: reversable defect: no proper blood movement when excercising <br/>
- target - have disease or not (0=absence, 1=presence) - the predicted attribute <br/>

### 3. Data Overview and Exploration
The dataset contains medical data on patients, with each row representing a patient and each column representing a feature. A preliminary inspection revealed:
- A mix of numerical and categorical data
- No missing values, ensuring completeness
- Some features with potential outliers (e.g., blood pressure)

### 4. Data Cleaning and Feature Engineering
We performed the following steps to prepare the data for modeling:
- **Handling Missing Values**: No missing values were present.
- **Scaling**: Continuous features like blood pressure, cholesterol, and glucose levels were scaled to standardize ranges.
- **Feature Encoding**: Categorical variables were encoded to ensure compatibility with machine learning models.

### 5. Data Visualization
Data visualization helped uncover patterns and relationships within the data:
- **Correlation Heatmap**: Showed relationships between features and identified key predictors like chest pain (`cp`) and maximum heart rate achieved (`thalach`).
- **Cross-Tabulations**: Analyzed relationships between categorical variables (e.g., gender and disease prevalence).
- **Histograms**: Displayed distributions of key features such as age, highlighting a focus on middle-aged and older individuals.

### 6. Modeling
We implemented several machine learning models to predict cardiovascular disease:
- Logistic Regression  
- Random Forest Classifier  
- Gradient Boosting Classifier  
- XGBoost  
Each model was trained on the cleaned and processed data. Cross-validation was used to assess performance and mitigate overfitting.

### 7. Hyperparameter Tuning
Hyperparameter tuning was conducted using grid search. For the Random Forest and XGBoost models, we optimized:
- Number of trees
- Maximum depth of trees
- Learning rate (for XGBoost)
- Number of estimators
- Maximum number of features  

These optimizations improved the predictive accuracy of the models.

### 8. Evaluation
The models were evaluated using:
- **Accuracy**: Proportion of correct predictions  
- **Precision**: Ability to avoid false positives  
- **Recall**: Ability to detect true positives  
- **F1-Score**: Balance between precision and recall  

The Random Forest model achieved the highest accuracy (~82%) and demonstrated balanced performance across precision and recall.

### 9. Feature Importance
Key features influencing predictions were identified using feature importance scores:
- **Chest Pain (`cp`)**  
- **Slope**  
- **Maximum Heart Rate Achieved (`thalach`)**  

These features align with medical knowledge, reinforcing the model's validity.

---

### Conclusion
Our cardiovascular disease prediction model, particularly the Random Forest classifier, demonstrated robust performance. Key predictors like chest pain, maximum heart rate, and slope highlight the model's alignment with established medical insights. This tool has the potential to assist in early identification and prevention of cardiovascular disease, providing valuable support in healthcare decision-making.
