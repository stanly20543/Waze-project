## **Waze Project**
Waze’s free navigation app makes it easier for drivers around the world to get to where they want to go. 
 
This project is designed to help prevent user churn on the Waze app and focuses on monthly user churn
Churn quantifies the number of users who have uninstalled the Waze app or stopped using the app. 

Developing a churn prediction model will help prevent churn, improve user retention, and grow Waze’s business. 
An accurate model can also help identify specific factors that contribute to churn and answer questions, who are the users most likely to churn?

### **Part1: Clean and investigate data**

 -**Target**:<br> 
 To get clear insights, the data must be inspected, organized, and prepared for analysis.<br>

 -**Conclusion**:<br>
  Users who churned drove farther and longer in fewer days than retained users. They also used the app about half as many times as retained users over the same period.<br>
  The median user who churned drove 698 kilometers each day they drove last month, which is about 240% the per-drive-day distance of retained users.

### **Part2: Explore and analyze data**

-**Target**:<br>
 Exploratory data analysis and data visualization<br>

-**Conclusion**:<br>
 The variables `activity_days` and `driving_days` had negative correlation with user churn. The more days user used app and drove, the less they churned.<br> 
 The variable `km_per_drinving_day` had a positive correlation with user churn. The farther a user drove on each driving day, the more likely they were to churn.<br>
 The proportion of churned users to retained users is consistent between device types.

### **Part3: Statistic analysis**

-**Target**:<br>
 To analyze the relationship between mean amount of rides and device type. <br>

-**COnclusion**:<br>
 There is not a statistically significant difference in mean number of rides between iPhone users and Android users.<br>

### **Part4: Build logistic regression model**

-**Target**:<br>
 To build a regression model to predict user churn based on a variety of variables.

-**Conclusion**:<br>
 `activity_days` is the most important feature in the model. It had a negative correlation with user churn. But it is not strong enough to be a preductor, as the _recall score_ being 64% and the _precision_ being 68% for churned user.<br>
 
### **Part5: Build tree-base model**

-**Target**:<br>
 To build machine learning models to predict user churn.<br>

-**Conclusion**:<br>
 In the XGB model we got the _recall score_ as 96% and the _precision_ as 86% more than the scores from the logistic regression model for churned user.<br>
 As the result, tree-base model is better than logistic regression model but it is no good enough for business decisions. To improve model, it would be helpful to have more data to know how users interact with the app.

