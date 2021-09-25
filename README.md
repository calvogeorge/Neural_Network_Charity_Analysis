# Neural_Network_Charity_Analysis

## Overview of the analysis  
The purpose of this repo is to use machine learning and neural networks to optimize where the resources of a charity foundation are best invested. Using neural networks we will create a model, train and use it to predict with funding request are more likely to be successful.  

## Results  
### Data Preprocessing  
**What variable(s) are considered the target(s) for your model?**  
Since the object of the analysis is to provide funding to charities likely to be successful, the target variable is IS_SUCCESSFUL.  

**What variable(s) are considered to be the features for your model?**  
The features of the model are 44 columns in the first model, that stem from these original columns:
-	APPLICATION_TYPE
-	AFFILIATION
-	CLASSIFICATION
-	USE_CASE
-	ORGANIZATION
-	STATUS
-	INCOME_AMT
-	SPECIAL_CONSIDERATIONS
-	ASK_AMT  

When were trying to improve the accuracy of our model we remove two additional features:
-	ASK_AMT – To many unique values.
-	STATUS – no variety in the values.  

**What variable(s) are neither targets nor features, and should be removed from the input data?**  
In the initial model EIN and NAME were removed for not being neither targets nor features. As mentioned in the previous answer in the optimization model ASK_AMT and STATUS were removed as well.  

### Compiling, Training, and Evaluating the Model  
**How many neurons, layers, and activation functions did you select for your neural network model, and why?**  
The initial model had 2 layers, with 80 and 30 neurons respectively and it use relu activation in the hidden layers and, sigmoid in the output layer.  

**Were you able to achieve the target model performance?**  
We were not able to achieve the target performance of 0.75, our best model was using kerastuner automated optimizer which achieved a 0.736, slightly short from the target.  

**What steps did you take to try and increase model performance?**  
First step was to reduce features and use the kerastuner automated optimizer, which brought us very close to the goal, the seconds attempt we kept the same features as the previous attempt and but increased the hiding layers to 3. This attempt didn’t improve much from the original. For the third attempt we increased the hiding layers to 5, and changes the activation methods, this attempt brought us to 0.70.  

## Summary  

After optimizing our model, we were able to achieve and accuracy level of 0.735 which is slightly lower than our target of 0.75, which we can consider optimal for the foundation to predict where to make investments. The model can continue to improve with more data. We can also further experiment removing features. We can also experiment with Machine Learning methods such as Random forest to determine if that model can achieve a better accuracy level.  
