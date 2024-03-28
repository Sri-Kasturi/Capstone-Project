# Capstone Project 

This dataset is about the car crash information between 2003-2020. The dataset comes from the Kaggle. The car crash dataset provides a detailed compilation of information related to common factors influencing road accidents, such as collision severity, weather conditions, road types, and contributing elements, offering valuable insights for the analysis and enhancement of overall road safety measures. Although I had totally different plans/topic of interest for my capstone, i surrendered to God's plan when my daughter/I were involved in a road accident mid-March which got both of us hospitalized and got us multiple fractures and restricted our mobility ( dependency based on cruthces, cast, walkers for the next 2 months). This has piqued my interest on road accidents in the US and what are the key factors that cause accidents and how could predictive modeling help identify the primry causes of road accidents. 

Link to the Jupyter notebook can be found here - https://github.com/Sri-Kasturi/Capstone-Project/blob/main/Capstone%20project%20-%20Sri%20Kasturi.ipynb 

Datasource: https://www.kaggle.com/datasets/jacksondivakarr/car-crash-dataset/data 

#### Data framework and Analysis -
I have used the CRISP-DM framework to analyze the data and below are the set of steps that I have followed to analyze the data -

Data understanding - Load the data. There are 53943 and 11 inputs in this dataset - For each observation, the dataset records 10 input variables that stand for both qualitative and quantitative attributes of the customer. There is one dervired/calculated boolean output variable that denotes “yes” or “no” revealing if the accident has resulted in an injury or not. 

Data cleansing and pre-processing -Data imputation tenchniques to identify missing and irrelevant data columns - drop columns, delete null values, fill in null values with most frequent data values, label encoder to get dummy values for categorical columns, quartiles to detect outliers and filter the data. I then used Exploratory Data Analysis (EDA) to visualize data accurately and identify important features for data preprocessing and model selection.

Data pre-processing - Used Correlation heatmaps to identify the key features

Model selection - First defined a baseline model using linear regression to get highlevel estimates on the model performance to set key metrics. Then, continued exploring different classification models to evaluate the performance of each of the models against the features. I then ran the assessment to compare which of these models had the optimal performance i.e., higher accuracy, Precison, and recall %

Evaluation - Overall assessment of the models have confirmed that the Logistic regression has the optimal performance in terms of accuracy% where as KNN had optimal performance in terms of precision scores.

#### Highlights from Exploratory Analysis:
- we observe a distinct pattern in the number of crashes throughout the day. Notably, the peak occurs during rush hours, particularly at 12 PM and 6 PM.
- Accidents during weekdays consistently exceeded that of weekends, suggesting potential variations in traffic patterns between the two.
-  The primary factor contributing to car accidents is mostly related to human factors, such as lack of concentration or losing control over the vehicle. 
- Further analysis on latitude/longitude parameters indicate that car accidents concentrate around a specific location (Longitude = -86, Latitude = 40). This suggests that this particular area experiences the highest frequency of accidents, implying heightened traffic activity in that part of the city.

#### Classification Model Performance -
Leveraged classification models: Logistic Regression,Decision Tree, Support Vector Machine (SVM), and K-Nearest Neighbors (KNN), AdaBoost, and Random Forest using three different scoring metrics: Accuracy, Precision score, and recall as well as the CV methods, with an objective to identify the model that most accurately predicts accidents that result in an injury that driver's could be more cognizant of. 

If we consider accuracy then Logistic Regressions has the optimal performance. But, considering that the dataset is highly imbalanced , I had continued to tweak the hyperparameters and used gridsearch methods to continue to refine the precision. If we consider precision, then KNN is the highest performance amongst other classification models. From a recall score perspective, KNN yields the highest performance.

#### Recommendations and Next Steps-
1. Inclusion of additional variables - expanding into driver demographics
The focus of the modeling has been on bank client information. I would liketo expand the analsyis by including features such as weather, age of driver, streaming api data,  vehicle type, traffic signal etc to look for any strong correlation on the primary factor and Injury type. By gathering more data, there could be other striking correlations found to provide evidence on nature of accidents subject to those specific parameters. 

2. Reference other data sources
Further analysis of the data with a broader set could be very beneficial i.e., getting additional source data on such as US accidents, road traffic accidents, road incidents that has a broader span of data could provide additional insights into the trends and major causes for accidents as they could inlcude additional parameters. 
