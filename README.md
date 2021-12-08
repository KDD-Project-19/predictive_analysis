**Covid-19 :  Predicitve Analysis** 

This project is part of the Knowledge Discovery in Databases (ITCS - 6162) course from University of North Carolina at Charlotte.


**INTRODUCTION:**

**Project Domain:**

Pandemic, Disease(Covid-19)

**Project Proposal:**

Covid-19 is a contagious disease that became a pandemic in 2020 mainly spreading through close contact with the infected person. Our objective here is to do descriptive analysis on a merged daily data of Belgium people for all age groups. Correlations will be examined between positive cases, hospitalizations,vaccinations and death rate. Based on the knowledge, a linear regression model will be used to predict the progression of the disease as vaccinations increase with accuracy.

**Team Members:**

1.Swathi Rajendran

2.Shreya Sekhar

3.Naga Bhanu Santosh Kumar Rayasam

4.Sasidhar Atluri

**DATA RESOURCE:**

**Data:**

https://data.gov.be/en/dataset/1030d556bc6489a9d1e85994e25d6bd01d53ce6b

**Data Description:**

https://epistat.sciensano.be/COVID19BE_codebook.pdf

**INTRODUCTION TO DATASET:**

We are working on the Covid-19 data of belgium. The dataset contains data from the beginning of covid i.e, from march 2020 to september 2021.

**The Dataset Contains the Following Predictors:**

DATE-  The dates of positive cases, deaths, vaccinations taken

NR_REPORTING- Number of hospitals reporting

TOTAL_IN- Total number of patients hospitalized due to covid-19 at the time of reporting

TOTAL_IN_ICU- Total number of patients in the ICU due to covid-19 at the time of reporting

TOTAL_IN_RESP- Total number of patients under respiratory support due to covid-19 at the time of reporting

TOTAL_IN_ECMO- Total number of patients on ECMO due to covid-19 at the time of reporting

NEW_IN- Number of patients hospitalized in the past 24 hours due to covid-19

NEW_OUT- Number of patients discharged in the past 24 hours cured from covid-19

TESTS_ALL- Total number of performed tests

TESTS_ALL_POS- Total number of positive tests

DEATHS- Total number of deaths due to covid-19

COUNT- Number of people receiving the covid-19 vaccine

REGION_CATEG- Region of residence of positive cases, vaccine taken, death, hospitalized

BRAND_CATEG- Vaccines brands which are nationally authorized or included in the WHO listings

DOSE_CATEG- Dose identifier (for vaccines requiring 2 doses: A for first dose, B for second dose; C for vaccine requiring only 1 dose; E for extra dose of vaccine if needed)

**INSTALLATION:**

Anaconda 4.10.1. Distribution

Python 3.9.5 

Jupyter Notebook

**CRISP-DM PROCESS:**

The Cross Industry Standard Process for Data Mining (CRISP-DM) is a six-phase process model that describes the data science lifecycle.It's like a set of guardrails that assist you to arrange, organize, and execute your data science (or machine learning) ventures.
The six major phases of CRISP-DM process are:

Business understanding 

Data understanding 

Data preparation

Modeling 

Evaluation 

Deployment 
 
**Business Understanding:**

The beginning of every project is to understand the problem statement and figure out what we need to accomplish. We must first specify the objectives of our problem statements and identify the requirements, hence transforming them into a data mining problem definition.

Our target population is the General public, Community members, Healthcare workers, and Vulnerable populations. Using the regional day-to-day covid-19 data from Belgium about the number of positive cases, Hospital details, mortality rate and, Vaccination data, we perform Exploratory Data Analysis on the merged data. A linear regression model will help us predict the number of positive cases based on the increase in vaccination rate with accuracy.
 
**Data Understanding:**

The main goal of this deliverable was to perform descriptive analysis on regional covid-19 data from Belgium by preparing and preprocessing the dataset, merging different datasets, and performing Exploratory Data Analysis on the combined dataset, which included comparing data such as the number of covid cases in different regions and the number of vaccines administered in each region. After preprocessing our data for modeling, the next step would be to do predictive analysis on the dataset by using linear regression to accurately forecast the number of positive cases based on the rise in vaccination rate.

Covid19BE_HOSP.csv

Covid19BE_MORT.csv

Covid19BE_NH.csv

Covid19BE_tests.csv

Covid19BE_VACC.csv

Combined to : Clean.csv after cleaning.
 
**Data Preparation:**

Our dataset was of four different entities consisting of the number of positive cases, mortality rate, hospital details, vaccination details, which needed to be merged to form a useable single dataset.
Handling missing values:
On merging the datasets, we found a lot of empty data in our dataset which needs to be handled to get an efficient dataset, so we assigned NA values and 0 to the data, depending on its requirement. 

**Cleaning Data:**

On merging the dataset, we found a few duplicate data and unwanted columns of data, so we cleaned the data by dropping the unwanted rows and columns.
Categorical Data Conversion:
Our dataset consists of a few object data types which need to be converted into categorical data for further EDA and Predicting purposes. So, the data columns like REGION, BRAND, and DOSE were converted into categorical data.

**Standardizing Data:**

The dataset had values varying from a high range and were in a need for standardising. So, the data would be standardized using StandardScaler.

**Removal of Outliers:**

The dataset had outliers, which gave us extremely high RMSE value, making our model unfit, so they had to be removed.


**Exploratory Data Analysis:**

Exploratory Data Analysis has been performed on the dataset showing relation to domain and problem statement. Visualization of the dataset has been done by plotting several graphs helping us to find the relationship between the data’s present in the dataset and to analyse the dataset for a better understanding. 

Visualizations have been done to compare these aspects.

Brand of vaccinations vs the dose taken - Bar Plot

The comparison between the brand of vaccinations and the dose of vaccine would help us get a clarity about the preferred brand of vaccine as well as the dose of the vaccine taken. As vaccines are a key part of our research, analysing this statistic is useful to us.

Region vs Positive cases - Violin Plot

The comparison between Region and positive cases is to find the number of cases per region.

Region vs Vaccination count - Strip Plot

The comparison between Region and vaccination count gives us information about the number of people vaccinated in a particular region.

Positive cases vs Deaths - Joint Plot

The comparison between the positive cases and deaths provides data about the number of people who died after getting affected by covid-19.

Region vs Death - Swarm Plot

The comparison between region and death would help us find the number of people who died due to covid-19 in a particular region.

These are few comparisons that are necessary for the statistical analysis of the covid-19 data and visualizing them would help us to correlate and understand the data better.

**Modelling - Linear Regression:**

Linear regression quantifies the relationship between one or more predictor variable(s) and one outcome variable. Linear regression is used here for the predictive analysis of our dataset. 

Our dataset is split into training and test datasets with a ratio of 70:30. The training and test is a dataset fitted into the linear regression model to predict the new positive cases of Covid-19 and the count of vaccinations.

A scatter plot is used to represent a comparison between the number of positive cases and the vaccination rate. The scatter plot gives us a clear picture of the decrease in the number of cases with the increase in vaccination rates.

Hence, this helps us conclude that the number of cases will decrease with the increase in vaccination rate as people will be immune to the disease and would be safer if vaccinated properly.

**Evaluation:**

We have used CRISP-DM Process for data mining and did Exploratory data analysis on the data, on certain aspects of it, providing us with the visualizable graphical correlation between particular data details, presenting us with Covid-19 statistics of Belgium. We have also done a predictive analysis on the number of Covid-19 positive cases and compared it to the vaccination count to check whether there is a decrease in the test cases with the increase in the vaccination rate.

We have measured the results and efficiency of the model using different error detecting methods:-

Mean absolute error (MAE):0.4661438639788965,
Mean square error (MSE): 0.8588527950844399,
Root mean square error (RMSE): 0.9267431117005618,

Which are low values that indicate the model has accurately predicted the labels.
 
**Conclusion:**

The motto is to perform predictive analysis on merged daily data for Belgium people of all age groups. We have taken the data from the Belgium government website since it would be the most accurate and would yield robust ground results from our model.

The datasets we have are the individual data with the details about the hospitalizations, vaccines, mortality, and tests-related information. The Primary key columns that could be used for the datasets are not the same, hence we have merged datasets with the use of unique yet similar columns as pairs, dropped unwanted data columns, and ended up aggregating them all together.

There is a lot of gap between the available Covid-19 data and vaccination data, since covid-19 cases started in March 2020 but vaccination only started after late September 2020, to overcome this we have added some default data values for the missing data in the vaccination information.

As for the data preparation, we had to perform data cleaning such as removal of null values, removal of unwanted columns, removal of duplicate values, grouping the datasets concerning a unique key and merging them, categorizing the data, removal of outliers, standardizing the data. On preparing the data with the above-mentioned works, we get our final dataset with no unwanted or repeated value which would be accurate and would have no discrepancies.

We evaluated our model on the basis of MAE, MSE, RSME and got good results from it by obtaining low respective values as mentioned in the evaluation.

Instructions to use the project: The dataset has also been provided along with the source code file(ipynb file). It has to be downloaded and imported into the ipynb file which is to run on a jupyter notebook. On executing the notebook, the user would be able to use our work and would be able to modify it to their needs.

**Future Work:**

The future scope is to utilize the economic, cultural, and geographical features in our dataset to more accurately predict the reason for the spread of disease. 

We could also work on finding the most effective vaccine which is widely chosen, by analyzing the count of the vaccine in a particular region.



 
 
 
 





 
 
 
 
 

 











































 
 
 
 
 
 



 
 








































