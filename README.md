# Deep-learning-challenge

### Step 4: Write a Report on the Neural Network Model

# Overview of the analysis: Explain the purpose of this analysis.

The purpose of this analysis is to figure out if the money was utilized effectively (if there was a return on investment)

## Results: Using bulleted lists and images to support your answers, address the following questions:
# Data Preprocessing
# What variable(s) are the target(s) for your model?
The target for the model is the IS-SUCCESSFUL column, which indicates if the money was utilized effectively.

# What variable(s) are the features for your model?
The features of this model are:
-	NAME
-	APPLICATION_TYPE
-	AFFILIATION
-	CLASSIFICATION
-	USE_CASE
-	ORGANIZATION
-	STATUS
-	INCOME_AMT
-	SPECIAL_CONSIDERATIONS
-	ASK_AMT

# What variable(s) should be removed from the input data because they are neither targets nor features?
EIN should be removed since the numbers could possibly confuse the system into thinking that it is significant.
STATUS can be dropped since all the rows had a value of 1, this does not add any value to the data. 
SPECIAL_CONSIDERATIONS can also be dropped, since there is only a small number of cases that had any special considerations, and it cannot be quantified. 

## Compiling, Training, and Evaluating the Model

# How many neurons, layers, and activation functions did you select for your neural network model, and why?
For this model, I added and utilized a third hidden layer since this seemed to boost the accuracy. Also, after running several tests, activation functions for the 2nd and 3rd layers were changed to sigmoid, since this also boosted the accuracy above the 75% mark. The number of epochs remained the same for all tests (100).

# Were you able to achieve the target model performance?
Yes, I was able to run the model at an accuracy of 78%. 
 ![IMAGE_DESCRIPTION](url_of_image)

# What steps did you take in your attempts to increase model performance?
Converting the column NAME into data points seemed to have the largest impact on improving efficiency, as well as changing the 2nd and 3rd activation function to sigmoid. 
 
## Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
Overall, by increasing the accuracy to 78%, we are able to correctly classify each point of data 78% of the time. An applicant has a higher chance at being successful if they have the following factors:
-	If the applicant has applied more that 5 times (NAME appears more than 5 times)
-	The APPLICATION_TYPE is one of the following: T3 thru T10 or T19
-	The CLASSIFICATION is one the following: C1000, C2000, C3000, C1200 or C2100


