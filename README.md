# Neural_Network_Charity_Analysis

# Overview
Alphabet Soup, a non-profit, is reviewing the impact of previous donations in preparation of vetting new potential recipients. Unfortunatley, not every donation is impactful and Alphabet Soup wants to predict whether potential recipients will be high risk. 

# Purpose
Using machine learning and neural networks, we use the features in a dataset of more than 34,000 organizations that have received funding from Alphabet Soup
over the years to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

# Results

* Data Preprocessing 
  * The target variable for our model is the "IS_SUCCESSFUL" variable. This variable indicates whether the money was used effectively, which is the goal of Alphabet
Soup.

  * The variables that are considered to be the features for our model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, SPECIAL_CONSIDERATIONS, ASK_AMT and INCOME_AMT. These features all may provide training for our model to best predict if a donation was successful. 

  * The EIN and NAME are neither targets nor features, and were removed from the input data as they are arbitrary identifiers of each organization.

* Compiling, Training, and Evaluating the Model

  * For the original model, we selected 2 hideen layers, the first with 80 neurons and the second with 30 neurons, and used the relu activation function given that
we had about 40 columns with features. The original model had about a 63% accuracy. 

![original model code](https://user-images.githubusercontent.com/99205688/177055943-d7a711c2-4df2-4994-9fdf-b9b70c020417.PNG)

![original model accuracy](https://user-images.githubusercontent.com/99205688/177055946-932b8b38-ad1d-485c-9b67-75a1936857b6.PNG)

  * To try to reach at least 75% accuracy, I made three attempts to modify the model but could not reach the target model perfomance of 75%. 

  * On the first attempt, the number of neurons was increased to try to increase accuracy. 

![attempt 1 code](https://user-images.githubusercontent.com/99205688/177055987-1f2b0db6-cb57-42b0-82f0-c38744fab4dc.PNG)

![attept 1 accuracy](https://user-images.githubusercontent.com/99205688/177055962-ba116cf5-1762-435e-97c8-e278ee93a470.PNG)

  * On the second attempt, I increased the number of hidden layers. 

![attempt 2 code](https://user-images.githubusercontent.com/99205688/177055999-e812bb54-0ba9-470f-80a1-046d4c1a55f7.PNG)

![attemp 2 accuracy](https://user-images.githubusercontent.com/99205688/177056003-7955e65e-c387-4d3f-ae85-bc35c3902622.PNG)

  * On the third attempt, I kept the additional neurons and hidden layers, and tried changing the activation function in the hidden layers by changing to the sigmoid function. Although these items were modified, the accuracy rate never went above 58% perent in the three tests.

![attempt 3 cpde](https://user-images.githubusercontent.com/99205688/177056059-88bcbf44-93a5-4020-b012-8d52a9ed8257.PNG)

![attempt 3 accuracy](https://user-images.githubusercontent.com/99205688/177056061-2cdfb110-159e-44cc-83a5-7874db8976a1.PNG)

# Summary

Overall, the modifications to the model did not increase it's performance to the target 75% threshold. Adding neurons, hidden layers, and changing the activation
function did not optimize it's performance. This could be due to the data, and perhaps dropping some additional columns of data could help the model perform
better with less features. If continuing to work with the entire dataset, given the size of the dataset and number of features, trying a random forest model might produce more accurate outcomes as the the random forest model predicts the classification based on a consensus of the weak learners and can deal with large datasets quickly. 
