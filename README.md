# Multi-Class-Happiness-Classification
Classifying the happiness of the residents of a city based on a survey

The government of the Smarticon city (name withheld) commissioned a survey and collected various attributes of residents along with their happiness level (Very Happy, Pretty Happy and Not Happy). Objective of this survey was to help government to classify residents based on their happiness level. The Government then wants to come up with more specific and relevant policies for respective group of residence based on their level of happiness.


##Problem Description
With the survey, Smarticon government has access to more than 13000 responses. But scaling up the survey to every citizen is very cost prohibitive in nature. Hence, it was required to build a model to predict the happiness levels of the citizens and then build policies on those classes. 

<br>
##Data Set
|Variable|Description
|---|---
|ID			                |Unique ID
|Var1			              |Categorical variable with 7 levels
|Work_Profile		        |Working Status
|Work_Score		          |Occupational Score
|Divorce			            |Ever been divorced or separated
|Widowed			            |Ever been widowed
|Education		            |Highest year of school completed
|Residence_Region	      |"Region of residence, at age 16"
|Babies			            |Household members less than 6 years old
|Kids			              |Household members 6 to 12 years old
|Young			              |Household members 13 to 17 years old
|Family_Income		        |Total family income
|Engagement_Religion	    |How often attends religious services
|Var2			              |Categorical variable with 3 levels
|Watch_TV		            |Hours per day watching tv
|Gender			            |1 (Female)/ 0 (Male)
|Unemployed		          |(1/0) if unemployed in last 10 years
|Happy			              |General Happiness
|alcohol_consumption	    |Alcohol Consumption Behaviour

<br>
##Evaluation Metric
Predictions were evaluated against the actual happiness status for the test dataset. Each level of happiness has associated points (see below)

|Happy	|Points
|---|---
|Very Happy	|15
|Pretty Happy	|10
|Not Happy	|5

Mis-classifying a person as more happy is a bigger problem, it leads to less budget allocation for people development by government whereas mis-classifying as less happier is a lesser problem. The scoring grid for each observation is as below:

|Actual_Point - Predicted_Point	|Score
|---|---
|0	|50
|5	|10
|10	|5
|-5	|-5
|-10	|-10

Final score was calculated as (Sum of Scores)/(n*50), where n is number of observation in test data set.

[![Binder](http://mybinder.org/badge.svg)](http://mybinder.org/repo/pronojitsaha/Multi-Class-Happiness-Classification)
