# Our SC1015 Repository: NEOs and Their Impact

## About
This is a mini project for the module, Introduction to Data Science & Artificial Intelligence (SC1015). We will be analysing near-Earth Objects (NEOs) such as asteroids and their impact in our project. 

## Our Files 

Viewed in the following order: 

1. [Data Cleaning](https://github.com/afreenrafi/SC1015-Project/blob/main/Data%20Cleaning.ipynb)
    - Cleaned our data by removing irrelevant columns, removing any duplicates, removed outliers and null datapoints 
    - Definitions of our variables are given under "Dataset Columns With Definitions"

2. [Data Splitting and Resampling](https://github.com/afreenrafi/SC1015-Project/blob/main/Data%20Splitting%20And%20Resampling.ipynb)
    - Split our dataset into train and test sets
    - Resampled our data into 4 different datasets: Original, Oversampled, SMOTETomek, Bootstrapping

3. [Exploratory Analysis](https://github.com/afreenrafi/SC1015-Project/blob/main/Exploratory%20Analysis.ipynb)
    - Created an Impact Risk column 
    - Basic statistics on our dataset
    - Compared different variables with Impact Risk using violin plot, histogram and box plot 
    - Used pair plot to compare all variables against one another 
    - Used bar plot heat map to find correlation between variables and Impact Risk 
    - Categroised Impact Risk into: Low, Medium, High
    - Used strip plot to compare variables with Impact Risk categories 

4. [Logistic Regression](https://github.com/afreenrafi/SC1015-Project/blob/main/Logistic%20Regression.ipynb)
    - Imported 4 different train datasets (original and resampled)
    - Calculated metrics: Accuracy, Precision, Recall and F1-Score 
    - Plotted confusion matrixes 
    - Plotted learning curves

5. [Neural Network](https://github.com/afreenrafi/SC1015-Project/blob/main/Neural%20Network.ipynb)
    - Imported 4 different train datasets (original and resampled)
    - Calulated metrics: Accuracy, Precision, Recall and F1-Score
    - Created neural network models for the 4 different datasets (original and resampled)
    - Plotted Loss, Accuracy, Precision and Recall histories 
    - Plotted train vs test performances 
    - Plotted test performances between different resampling methods 
    - Plotted training histories between different resampling methods 

## Contributers 
- @gwenionna - EDA, Logistic Regression 
- @ZhiXin18 - Data Cleaning, Data Splitting and Resampling, Neural Network
- @afreenrafi - EDA, Logistic Regression 

## Problem Statement 
How might we predict which NEOs pose a high risk of impact to Earth?

## Dataset Columns With Definitions
1. Neo Reference ID: A unique identifier assigned to each Near Earth Object (NEO) by the NeoWs API. This ID is used to reference and identify specific NEOs within the database.
2. Est Dia in M(min): The estimated minimum diameter of the NEO in meters.
3. Est Dia in M(max): The estimated maximum diameter of the NEO in meters.
4. Relative Velocity km per sec: The relative velocity of the NEO with respect to Earth, measured in kilometers per second. This parameter indicates the speed at which the NEO is approaching or receding from Earth.
5. Miss Dist.(kilometers): The closest miss distance of the NEO from Earth, measured in kilometers.
6. Perihelion Distance: The perihelion distance of the NEO's orbit, representing the closest distance between the NEO and the Sun.
7. Aphelion Dist: The aphelion distance of the NEO's orbit, representing the farthest distance between the NEO and the Sun.
8. Perihelion Time: The time of perihelion passage of the NEO's orbit.
9. Mean Anomaly: The mean anomaly of the NEO's orbit, representing the fraction of the orbital period that has elapsed since the last perihelion passage.
10. Mean Motion: The mean motion of the NEO's orbit, representing the average angular velocity of the NEO along its orbit.
11. Hazardous: A binary indicator that specifies whether the NEO is classified as hazardous or not based on its orbit and size. A value of "1"/True indicates that the NEO is classified as hazardous, while a value of "0"/False indicates that it is not considered hazardous.

## Reasoning behind the classification of Low, Medium and High Impact Risks
We generated different thresholds for the 3 levels of impact risk. We have added the histograms for our Impact Risk thresholds. Next, we used this thershold to categorise Low, Medium and High risks NEOs.

## Conclusion 

1. Strong correlation between Impact Risk and characteristics of NEOs
2. Managed to categorise NEOs into different risk levels
3. Both our models were able to mostly correctly identify NEO risk
4. Multiple factors beyond speed and hazard level also influence risk of NEOs 

## Things we learnt

1. EDA techniques such as strip plots and bar plot heat maps
2. Learnt how to resample data into oversampled, smotetomek and bootstrapped 
3. Logistic Regression
4. Learnt to plot a learning curve for logistic regression 
5. Neural Network

## References 

1. https://medium.com/@satyarepala/understanding-logistic-regression-a-step-by-step-explanation-9a404344964b
2. https://towardsdatascience.com/understanding-logistic-regression-step-by-step-704a78be7e0a
3. https://www.analyticsvidhya.com/blog/2021/08/conceptual-understanding-of-logistic-regression-for-data-science-beginners/
4. https://www.aitude.com/multiclass-classification-on-highly-imbalanced-dataset/
5. https://machinelearningmastery.com/multi-class-imbalanced-classification/
6. https://machinelearningmastery.com/multi-class-classification-tutorial-keras-deep-learning-library/
7. https://machinelearningmastery.com/tutorial-first-neural-network-python-keras/
8. https://www.geeksforgeeks.org/introduction-to-resampling-methods/
9. https://www.kaggle.com/datasets/lovishbansal123/nasa-asteroids-classification (our kaggle dataset)
