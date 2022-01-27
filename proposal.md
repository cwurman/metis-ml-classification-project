# Metis Classification Project Proposal
#### Chaya Wurman

## Question
**Can we predict whether or not individuals are at high risk for having a stroke?**
This is the main question that I will be attempting to answer. Given a person's health, demographic, and medical data, can we predict whether or not that person has had a stroke in their lifetime?

Strokes are caused by many medical and lifestyle factors, and knowing which factors are highly correlated with strokes can help better predict those who are at higher risk. There are a large number of factors that have been found to be correlated with strokes, such as high blood pressure, obesity, drug use, race, diabetes, etc. Being able to identify if a person is at risk for having a stroke, and understanding which factors truly are the most predictive, could help medical professionals mitigate risk in their patients before that life threatening event happens.

## Data Description
I plan to use the CDC NHANES (National Health and Nutrition Examination Survey) dataset to answer this question. The dataset can be found on Kaggle [here](https://www.kaggle.com/cdc/national-health-and-nutrition-examination-survey?select=demographic.csv), and is documented on the CDC website [here](https://www.kaggle.com/cdc/national-health-and-nutrition-examination-survey?select=demographic.csv). 

A single sample in this project represents one person, and a comprehensive overview of their entire current health & nutritional status at the time of taking the NHANES survey. The data set contains information including:
 - Demographics (age, race, marital status, education level)
 - Diet (what types of foods the subject is eating, eating patterns)
 - Examination (blood pressure, grip strength, oral health data)
 - Labs Data (Fluoride, Cholesterol,  Urine flow rate)
 - Medications (current prescription medications, mental health state)
 - Questionnare (medical history, alcohol use, consumer behavior, food insecurity, income, etc)

I will be attempting to predict a single feature in this dataset, in the questionnare section: *Has a doctor or other health professional ever told {you/SP} that {you/s/he} . . .had a stroke?* 

There are approximately 10.2k rows in this dataset, representing 10k patients. However, the effective size of the data I'll be able to use will be about 5k patients, as there are only 5000 examples where the label in question, whether or not the patient has had a stroke, has valid data. There are approximately 2000 columns in the dataset total, so I will be doing some significant feature selection to find only the subset of columns to use.

## Tools

I plan to mostly use the basic tools that we are using for assignments in this course: Python & sklearn for model development, and matplotlib for visualization. If possible, I'll experiment with using some other visualization tools.

## MVP Goal
For the MVP of this project, I'll aim to have selected 10 or so columns that are predictive of patients having strokes, and train a Logistic Regression model on them. There will be some work done in the early stages of this to figure out which initial columns will be the most helpful to pull out, so I'm hoping to have a somewhat predictive model that from those features.

Once I have that MVP, I'm hoping to:
 - Better tune the model by seeing which other features may also be relevant
 - Experiment with different classification algorithms and see if there is a model type that is a best performer
 - See if I can train the model on different types of data (what if I just use demographics/income data? or just medical data? ) and see if those subsets alone are still predictive of patient strokes.
