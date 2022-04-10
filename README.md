# Predicting Used Car Prices Using Exploratory Data Analysis and Machine Learning Techniques

## Introduction
Deciding whether a used car is worth the posted price when you see listings online can be difficult. Several factors, including 
* mileage 
* make 
* model 
* year etc... 
can influence the actual worth of a car. From the perspective of a seller, it is also a dilemma to price a used car appropriately. Based on existing data, the aim is to use machine learning algorithms to develop models for predicting used car prices

## About The Dataset 
In this project, we are using the dataset on used car sales from all over the United States from TrueCar. The features available in this dataset are Mileage, Make, Model, Year, State, and City.

## Data Pre-Processing
* Pruning: 
    A histogram of the dataset indicated many outliers, for example, cars with really low mileages that were unrepresentative of a “used" car. Therefore, we pruned our dataset to three standard deviations around the mean.

* One-Hot Encoding : 
    We converted the Make, Model, and State into one-hot vectors. Since we had over 2OOO unique cities in the dataset, we replaced the string representing the city with a boolean which was set if the population of the city was above a certain a threshold i.e. a major city

* Linearity: 
    To analyze the degree to which our features are linearly related to price, we plotted the Price against Mileage and Year for a particular Make and Model. There seemed to be a fair degree of linearity for these two features.

## Methodology
We utilized several classic and state-of-the-art methods,including ensemble learning techniques, with a 9O-1O split on test and training data. To reduce the time required for training, we used 5OOk examples from our dataset (of almost a million examples).

### This Project is divided in to 15 major steps which are as follows:

1. [Data description](#data-desc)
2. [Importing Libraries & setting up environment](#imp-lib)
3. [Loading dataset](#data-load)
4. [Data Cleaning & Preprocessing](#data-prep)
5. [Exploratory Data Analysis](#data-eda)
6. [OUtlier Detection & Removal](#data-out)
7. [Training & Test Split](#data-train)
8. [Cross Validation](#cross-val)
9. [Model Building](#data-model)
10. [Feature Selection](#model-eval)<br>
11. [Model Evaluation](#model-inter)
12. [Preparing The model for Deployment](#model-deployment)
13. [Preparing Flask and HTML files for Deployment](#model-deployment)
14. [Deploying the Model in Heroku ](#model-heroku)
15. [Conclusion](#data-conc)


## About Data 

This dataset consists of 8 input variables and a target variable. It has 6 categorical variables and 2 numeric variables. The detailed description of all the features are as follows:

**1 Price:** Shows the Price of the used car : This is the Target variable(Numeric)<br>
**2 Year:** Shows the Year of manufacturing of the Car : High corelation on the Target variable (Numeric)<br>
**3 Mileage:** Shows the Mileage of the used car : High corelation on the Target variable (Numeric)<br>
**4 City:** Shows The city which the car is from : Low corelation on the Target variable (Nominal)<br>
**5 State:** Shows The State which the car is from : Low corelation on the Target variable (Nominal)<br>
**6 Make:** shows who is the Manufacturer of the car : High corelation on the Target variable(Nominal)<br>
**7 Model:** Shows which model is the car : High corelation on the Target variable (Nominal)<br>
**8 Usage_level:** Shows the usge level of the car : Low,Medium,High : High corelation on the Target variable(Nominal)<br>
**9 City_imporatnce:** Shows which the car is have any city importance : Low corelation on the Target variable (Nominal)<br>

#### Target variable
* Price :
 It is the target variable, which we have to predict the price of the car with the help of Dependent variables having High corelation on the Target variable.

### Dependent variables
* Year
* Mileage
* Make
* Model
* Usage_level

## Python Libraries For This Project 
This project requires Python 3.x and the following Python libraries should be installed to get the project started:
- [Numpy](http://www.numpy.org/)
- [Pandas](http://pandas.pydata.org/)
- [matplotlib](https://matplotlib.org/)
- [scikit-learn](https://scikit-learn.org/stable/)
- [seaborn](https://seaborn.pydata.org/installing.html)
- [Flask](https://flask.palletsprojects.com/en/2.1.x/)

I also reccommend to install Anaconda, a pre-packaged Python distribution that contains all of the necessary libraries and software for this project which also include jupyter notebook to run and execute [IPython Notebook](http://ipython.org/notebook.html).

## Conclusion
 After going through all the steps above I concluded my project by deploying our model in Heroku using Flask and Python. 
 Heroku is a platform as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud.

 ## URL Of My Machine Learning Journey deployment in Heroku
    https://carpricepredict-technocolab.herokuapp.com/
