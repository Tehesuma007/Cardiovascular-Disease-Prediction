# **Title:** Cardiovascular Disease Prediction

## **Overview:**
This notebook is a binary classification problem that utilizes various Python-based machine learning and data science libraries in an attempt to build a machine learning model that will be used to build a simple web application capable of predicting whether or not someone has heart disease based on their last clinical parameters. Below is the approach we are going to follow:

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

## 3. Data Overview and Exploration

