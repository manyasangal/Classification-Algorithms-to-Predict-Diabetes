
1. INTRODUCTION

Diabetes  is a chronic disease . It may cause many complications. According to the growing morbidity in recent years, in 2040, the world’s diabetic patients will reach 642 million, which means that one of the ten adults in the future is suffering from diabetes. There is no doubt that this alarming figure needs great attention. With the rapid development of machine learning, machine learning has been applied to many aspects of medical health. In this study, we used decision tree, random forest and neural network to predict diabetes mellitus. 


3. DATA
The data contains following 9 fields:

1)Pregnancies  
2)Glucose  
3)BloodPressure  
4)Skin Thickness  
5)Insulin  
6)BMI  
7)Diabetes Pedigree Function  
8)Age  
9)Outcome  


4.DATA MODELING

1) Split the data into training and test data.
2) Train the model on training Data and validate on Test Data
3) At the first instance I have taken all variables as predictors and looking at the results I will start the elimination process. 
4) I first applied Logistic Regression to train Training Data.
5) glm model gives Probability of 'Outcome' being a Yes. i.e. a patient is predicted to have diabetes.
6) I took 0.5 as the threshold probability for this model.
7) I then construct a Confusion Matrix to determine the accuracy of this model.<br/>
Looking at the summary(glmModel) we can see that Skin Thickness and Age are not significant. 
9) Confusion Matrix shows an accuracy of 76.5% which is not good enough.
10) So now I will remodel after eliminationg the non significant variables.
11) So I decided to remove the non significant variable  from my training Data and Test Data and remodel.
12) I have also plotted ROC curve for this model. ROC cusrve is plot of (1-specificity) on x axis and sensitivity on y axis.
Higher the area under the curve, better is the model.<br/>
Even after cleaning data , I can see that the accuracy remains almost the same.
14) I still decide to go ahead with the clean data and apply other models like kNN and Random Forest to see how they work.
15) May be LOgistic is just not the right model for this data.
16) I apply knn next with value of k=5. We can change values of k to get a better accuracy. Keeping K too
less will consider very few neighbours and might not give right model(Will lead to Overfitting).
Keeping k to a very big value will include far off points also and might not give the right model as well.<br/>
From the confusion matrix of the above knn model see that  we get an accuracy of  97%  These statistics represent a very good predictive model as the values are very high.
18) Now we apply Random Forest to predict the values of outcome.
19) Random forest gives us an accuracy of 79.6% which is not very good.
20) So we can conclude that kNN is the best model for this which gives us an accuracy of about 96% which is very high.




