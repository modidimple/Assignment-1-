
**Problem Statement**
In modern-day America, mental health has emerged as a significant concern. According to a 2020 
survey conducted by the American Psychology Association, almost 19% of adults reported a 
decline in their mental well-being compared to the previous year. Anxiety has the ability to distort 
one's thinking patterns, resulting in negative thoughts, self-doubt, excessive rumination, and 
difficulties with concentration and decision-making. Similarly, depression involves negative 
thinking patterns, such as self-criticism, feelings of worthlessness, guilt, and recurrent thoughts 
of death or suicide. Therefore, it is vital to comprehend the underlying factors that contribute to 
poor mental health and seek effective strategies to address them. With this project, our objective 
is to utilize machine learning models to predict anxiety and depression by analyzing 
sociodemographic variables. 

**Research Question**

What socio-demographic factors contribute to poor mental health(anxiety/depression), and the 
use of machine learning models to predict mental health scores based on demographic 
information. 

**Hypothesis**

We hypothesize that factors such as lower income, lower education level, higher/lower than 
average BMI, minority race, and poor communities contribute to a higher probability of mental 
health conditions. These vulnerable socioeconomic groups are more likely to experience stress 
due to financial, job, housing, and healthcare insecurities. 

**Dataset**

- 2021 NaƟonal Health Interview, in the category of Sample Adult Interview
- Survey Link to the dataset: https://www.cdc.gov/nchs/nhis/2021nhis.htm
-  Number of observaƟons: 29482

  **Dependent variable**
  Mental Health Score
  **Independent variable**
  Age, sex, education, insurance coverage(inscov), anxiety frequency, 
 anxiety level, depression frequency, depression level, orient (Sexual Orientation), Marital Status 
 (Marital), Military, Citizenship, Income_wage, BMI, LGBT, Mental Health Condition 
  Ever(mh_ever)

  **Assumptions**
  
  In our pursuit to establish a connection between demographic information and 
 mental health, it is essential to have a quantitative measure for assessing mental health 
conditions. To begin with, we examine variables that are associated with mental health 
conditions. Given that we possess data on the severity and occurrence rate of anxiety and 
depression, we formulate a mental health score for each instance utilizing the following 
approach. 

**Score** = (Anxiety level* Anxiety frequency) +(Depression level*Depression level*Depression 
frequency). 

**The mental health score is designed to reflect the severity of a person's mental health condition, 
with higher scores indicating a more unfavorable state.**

**Machine Learning**

We employed machine learning to see if we can effectively predict mental health score using 
demographics information. To do this, we frame both a regression and a classification task. For 
regression, we aim to directly predict mental health score, which is a continuous variable. For 
classification task, we split the dataset based on the mean mental health score from the dataset, 
yielding a threshold for classification task. To achieve the best possible performance on each 
model, we take some values like MSE, accuracy scores, and accuracy means. 
12 For Regression type, we will compare performance between Linear regression, LASSO, Bagging, 
Regression Tree. For Classification type, we will compare between Logistic Regression, Random 
Forest, KNN, Decision Tree Classifier. 

**Regression**

| Model               | MSE    | Score                |
|---------------------|--------|----------------------|
| Linear Regression   | 11.81  | R squared value = 0.063 |
| LASSO               | 12.00  | Best alpha after CV = 0.01 |
| Bagging Decision Tree | 14.485 | -                   |
| Random Forest       | 12.261 | -                   |
|                    | 11.5   | This is the best model in terms of MSE (after CV) |

**Classification**

| Algorithm                 | AUC mean | AUC std | Accuracy Mean | Accuracy std |
|---------------------------|----------|---------|---------------|--------------|
| Logistics Regression      | 63.55    | 2.34    | 66.66         | 1.89         |
| Random Forest             | 59.49    | 1.40    | 62.91         | 1.13         |
| KNN                       | 55.01    | 1.29    | 60.83         | 1.60         |
| Decision Tree Classifier  | 53.91    | 2.56    | 57.89         | 1.83         |

**Performance Evaluation**

Linear Regression analysis: The mean squared error (MSE) is a measure of the average squared 
difference between the predicted and actual values. In this case, the MSE value is 11.81. Lower 
MSE values indicate better model performance, as they represent smaller errors between the 
predicted and actual values. The R squared value is 0.063, which indicates that approximately 
6.3% of the variance in the score can be explained by the features included in the model. A higher 
13
R-squared value indicates a better fit of the model to the data. So we need to evaluate other 
model options for better outcome. 




  
  
