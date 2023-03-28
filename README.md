# NYPD_602

## Abstract: 
In this data set we can notice the "NYPD crime data historic", Crime is an illegal act, we heard about of different types of crimes which were happend in the different places. Here i am going to classify the NYPD crime report, in this data set includes types of crimes, data and time of occurance, place where the crime was happend, and even the suspect gender, age, race as well as vicytim age, gender, race. The data what we have from the year of 2006 to 2019, So our main intention is define in the past decade is the crime rate is raised or decreased. At what time the crime rate is high, which type of crime happening oftenly. 

## Data Discription:
This is an open source data, which is taken from the NYC open data. This data set cointains the crime data history of the New York City which contains the data from 2006 to 2019. All valid felony, misdemeanor, and violation offences recorded to the New York City Police Department (NYPD) are included in this collection.
## Features:
## Below are all the variables in the dataset, followed by its description: 
CMPLNT_NUM =  Randomly generated persistent ID for each complaint

CMPLNT_FR_DT = Exact date of occurrence for the reported event (or starting date of occurrence, if CMPLNT_TO_DT exists)

CMPLNT_FR_TM  = Exact time of occurrence for the reported event (or starting time of occurrence, if CMPLNT_TO_TM exists)

CMPLNT_TO_DT  = Ending date of occurrence for the reported event, if exact time of occurrence is unknown

CMPLNT_TO_TM  = Ending time of occurrence for the reported event, if exact time of occurrence is unknown

ADDR_PCT_CD  =  The precinct in which the incident occurred

RPT_DT  =  Date event was reported to police

KY_CD  =  Three digit offense classification code

OFNS_DESC  =  Description of offense corresponding with key code

PD_CD  =   Three digit internal classification code (more granular than Key Code)

PD_DESC  =   Description of internal classification corresponding with PD code (more granular than Offense Description)

CRM_ATPT_CPTD_CD  =  Indicator of whether crime was successfully completed or attempted, but failed or was interrupted prematurely 

LAW_CAT_CD  =  Level of offense: felony, misdemeanor, violation

BORO_NM  =  The name of the borough in which the incident occurred

LOC_OF_OCCUR_DESC  =   Specific location of occurrence in or around the premises; inside, opposite of, front of, rear of

PREM_TYP_DESC  =  Specific description of premises; grocery store, residence, street, etc.

JURIS_DESC =  Description of the jurisdiction code

JURISDICTION_CODE =  Jurisdiction responsible for incident. Either internal, like Police(0), Transit(1), and Housing(2); or external(3), like Correction, Port Authority, etc.

PARKS_NM  =  Name of NYC park, playground or greenspace of occurrence, if applicable (state parks are not included)

HADEVELOPT =  Name of NYCHA housing development of occurrence, if applicable

HOUSING_PSA = Development Level Code

X_COORD_CD =  X-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet (FIPS 3104)

Y_COORD_CD  = Y-coordinate for New York State Plane Coordinate System, Long Island Zone, NAD 83, units feet (FIPS 3104)

SUSP_AGE_GROUP =  Suspect’s Age Group

SUSP_RACE =  Suspect’s Race Description

SUSP_SEX  =  Suspect’s Sex Description

TRANSIT_DISTRICT =  Transit district in which the offense occurred.

Latitude =  Midblock Latitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326)

Longitude  =  Midblock Longitude coordinate for Global Coordinate System, WGS 1984, decimal degrees (EPSG 4326)

Lat_Lon =  	 Geospatial Location Point (latitude and Longitude combined)

PATROL_BORO  =  The name of the patrol borough in which the incident occurred

STATION_NAME = Transit station name

VIC_AGE_GROUP = Victim’s Age Group

VIC_RACE = Victim’s Race Description

VIC_SEX = Victim’s Sex Description


### Dataset Source Link: https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i

## Data Set:
Data Source Link: https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i
In this Dataset we have 35 columns and more than a 7 million rows.

## Data Cleanup:
This data set contains the 7.3 million rows and the 35 columns, we dont need all the columns to perform the models on the data, so we droped the unwanted columns and took the data chunk size as 10000, because it is an huge to perform all modelds, it's consuming more time to perform, so I took the chunk size as 10000 ionly.
## EDA:
In this notebook i performed EDA on NYDP crime data histroic.
1) Top Areas of crime, Here i shown the top ares where the crimes was happend.
2) Top crime types, we have multiple types of crimes in the data set, so i plotted the top crimes which were held.
3) Age category of the suspects was plotted 
4) Gender category of the suspect
5) The locations were plotted in a map where the crimes was happend frequently
6) The Race of suspects also plotted based on the dataset

## Modelings & Scores:
Here i have performed the total of 5 models 
1)  Decision Tree Classifier:
Here I choose this classifier as it divides the data into different nodes. And it create a model that predicts the value of target variable by learning simple decision rules. This model has descriptive decision making skills as I have more categorical variables.
Accuracy Score: 0.768
ROC Curve Score : 0.857

2) Logistic Regression:
It is an basic model and performs reliable then any other models. When the target variable is categorical the we use this model to predict.
Accuracy Score: 99.7
Roc Curve Score:  0.99995

3)Logistic Regression with K-Means:
K-mean is a clustering part. discover categories in the data that haven't been explicitly categorized.
Multidimensional data can be used, but it must first be reduced in dimensionality before being used for k-means.
Accuracy Score: 0.592
Roc Curve Score:  0.603

4) Random Forest Classifier:
As i have used decision tree model , I want to check whether random forest works good or not. As it combination of decision tree or subsamples of the data set. And used to improve the predicted accuracy scores and also control overfitting.
 Accuracy Score: 0.8695
 ROC Curve Score: 0.9463

5)k-Nearest Neighbors (Knn):
It is a simple supervised classification algorithm where we can use to assign a class to a new datapoint. 
This can be used for regression as well. It doesn’t make any assumptions on the data distribution, hence it is not parametric.
Accuracy Score: 0.8185
ROC Curve Score: 0.8957

## Further Explorations:
As of now, I have considered only chunked data for my project I got these scores i.e., up to 10000, But if I have considered the whole dataset the score may get improved.
I have used 5 models for the modeling, here we can use different complex models like neural networks but it may lead to different problems.
Here we can also use ensemble models for modeling to get an improved score, but we are not sure it may or may not be improved.

## Conclusion:
After performing all the models, i highest accuracy i got in the model is Logistic regression model, with the approximate values of 0.99, neither it could be performed with the high rate of accuracy or it is a ideal. After that Random forest classifier model got the better result values 


## Refrences: 
### https://github.com/appliedecon/data602-lectures
### https://stackoverflow.com/questions/45332410/roc-for-multiclass-classification 



