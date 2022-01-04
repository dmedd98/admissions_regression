# Deep Learning Regression with Admissions Data

### Created by Dillon Medd

#### Project Goals
 With the given [graduate admissions dataset](https://www.kaggle.com/mohansacharya/graduate-admissions?select=Admission_Predict_Ver1.1.csv), I have set out to create a deep learning regression model that will predict the likelihood of an applicant applying to graduate school will be accepted. The target variable used is "Chance_of_admit" and is a continious variable between 0 and 1. This type of algorithm would be able to give further insight into the graduate admissions world.
 
 ### Exploratory Data Analysis
 
  Our dataset contains information from 500 students, there is no null data. For each student there are 7 different contributing factors that go into their chance of being admitted. Take a look at the correlations in the heatmap below.
  
  ![image](https://user-images.githubusercontent.com/79603572/146800880-36cfb1cb-a285-4ef5-8db7-2c93f7adaaa9.png)
  
 As shown above, CGPA (Cumalitve Grade Point Average) is the highest correlated factor with admittance percentage, let's take a look at a scatter plot comparing CGPA and admittance chance.
 
 ![image](https://user-images.githubusercontent.com/79603572/146801301-5e7b0847-b7c6-4feb-b133-0e6b26fe5560.png)
 
 University Rating was also highly correlated with chance of admittance, let's include that information in another scatter plot.
 
 ![image](https://user-images.githubusercontent.com/79603572/146801642-b1cdbf92-6251-4072-863b-199785d3df9e.png)

 Seems like a lot of the top CGPA came from students are highly rated universities, this could be an example of Multicollinearity between variables.
 
 ### Linear Regression Model
 
For comparison purposes, I started with a Linear Regession model, trained with 80% of the data (400 students). Below is a visualization of the predictions and actual values from the remaining test set. This model returned an R-Squared Value of 0.829 and a Mean Squared Error of .0034

![image](https://user-images.githubusercontent.com/79603572/146804327-5064851c-0d4a-4428-bb76-6b8033e0999f.png)

### Deep Learning Model with Tensor Flow

Using a Sequential Model, I experimented with the hyperparamters and structure of the Nueral Network. While the model unfortunately could not better the Linear Regression Model in terms of R-Squared, likely due to the fact that Neural Networks perform better with very large datasets (500 datapoints is relatively small), I was still happy to report a .819 R-Squared and a Mean Squared Error of .0036. Below you can find a visualziation showing Mean Average Error for the model based on the amount of Epochs, which lead to the final model containing 40, as well as the comparison of predictions with actual chance of admitance.

![image](https://user-images.githubusercontent.com/79603572/146805757-507cf5fa-e9ef-4289-bf32-ef946fa98e3f.png)
![image](https://user-images.githubusercontent.com/79603572/146805776-7ca23b5a-f0b6-4e62-8372-12ad2dd2f452.png)


### Thank you
Dillon Medd
  - [Github](https://github.com/dmedd98)
  - [LinkedIn](https://www.linkedin.com/in/dillon-medd/)

 

