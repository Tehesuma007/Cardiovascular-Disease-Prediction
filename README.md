# **Title:** Cardiovascular Disease Prediction

## **Overview:**
This notebook is a binary classification problem that utilizes various Python-based machine learning and data science libraries in an attempt to build a machine learning model that qill be used to build a simple web application capable of predicting whether or not someone has heart disease based on their last clinical parameters. Below is the approach we are going to follow:

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


### 1.Problem Definition
In a statement,
Given clinical parameters about a patient, can we predict whether or not they have heart disease?

### 2.Features
This is where we will get different information about each of the features in our data

**Let's Create a data dictionary**
{
-age - Patient age in years
-sex - (1 = male; 0 = female)
-cp - chest pain type
   *0: Typical angina: chest pain related decrease blood supply to the heart
   *1: Atypical angina: chest pain not related to heart
   *2: Non-anginal pain: typically esophageal spasms (non heart related)
   *3: Asymptomatic: chest pain not showing signs of disease
-trestbps - resting blood pressure (in mm Hg on admission to the hospital) 
   *anything above 130-140 is typically cause for concern
-chol - serum cholestoral in mg/dl
-serum = LDL + HDL + .2 * triglycerides
   *above 200 is cause for concern
-fbs - (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false)
   *>126' mg/dL signals diabetes
}
