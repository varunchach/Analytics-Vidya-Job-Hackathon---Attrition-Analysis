# Analytics-Vidya Job-Hackathon Employee Attrition-Analysis

This is about hackathon which is organized by Analytics Vidya where we were given problem to predict the employee attrition. It was a imbalanced classification problem.


### Problem Statement :- Predicting Employee Attrition    

In recent years, attention has increasingly been paid to human resources (HR), since worker quality and skills represent a growth factor and a real competitive advantage for companies. After proving its mettle in sales and marketing, artificial intelligence is also becoming central to employee-related decisions within HR management. Organizational growth largely depends on staff retention. Losing employees frequently impacts the morale of the organization and hiring new employees is more expensive than retaining existing ones. 

You are working as a data scientist with HR Department of a large insurance company focused on sales team attrition. Insurance sales teams help insurance companies generate new business by contacting potential customers and selling one or more types of insurance. The department generally sees high attrition and thus staffing becomes a crucial aspect. 

To aid staffing, you are provided with the monthly information for a segment of employees for 2016 and 2017 and tasked to predict whether a current employee will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not, given:


1. Demographics of the employee (city, age, gender etc.)
2. Tenure information (joining date, Last Date)
3. Historical data regarding the performance of the employee (Quarterly rating, Monthly business acquired, designation, salary)


### Raw data format
The data was at monthly level where all the parameters pertaining to employee were measured.
I didnt find missing values in the given data.

![Raw_data_format](https://user-images.githubusercontent.com/58731031/142766986-3868c241-8d09-45f8-82dc-0971ef41af06.PNG)


## Exploratory Data Analysis 

### Attrition on the basis of tenure

![image](https://user-images.githubusercontent.com/58731031/142766599-75999de7-3a6b-4ed4-b91d-add9949fa6c0.png)

People with Bachelor degree tend to stay less than those who haven't attrited yet.

### Average Business value
![image](https://user-images.githubusercontent.com/58731031/142766691-03d599ed-3766-490f-b7e0-bcdd59d39be3.png)

There was clear distinguishing fctor between attritors and non-attritors. As we can see attritors were not able to bring much value to business compared to non-attritors.


### Age wise distribution
![image](https://user-images.githubusercontent.com/58731031/142766716-55ad6860-a469-4a5e-b041-f312be6acc55.png)

Our population was focused in the age groups 20-40. 


I have created multiple variables which helped me to understand saggergation between attritors and non-attritors like what was their maximum rating ,what was minimum rating ,tenure in days, average business value , average monthly salary and more.

### Variable mutual information values after filtering highly correlated variables (>0.85)
![image](https://user-images.githubusercontent.com/58731031/142766736-a1595c4e-01be-424f-93da-7fac0ee12a07.png)


### Correlogram of the variables
![image](https://user-images.githubusercontent.com/58731031/142766753-4331f51e-cc51-40bd-8226-0c50f907ae43.png)


After trying out 4 algorithmic approacheson train data
1. Logistic :- 59% F1- beta Score
2. XGBoost Classifier :- 70% F1-beta score
3. LightGBM :-71% F1-beta score
4. CatBoost Classifier :- 72% F1-beta score.

I found that catboost was best classifier among all.

### Catboost plot:-
![CatBoost_plot](https://user-images.githubusercontent.com/58731031/142767682-4ef479a7-d998-422b-b0ab-5a27ff3683af.png)

















