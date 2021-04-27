# Google Fit App using **Streamlit**

**This repo contains the project which predicts how much calories you burn.**

## 1. Problem Statement: 
A few months back I started using **Google Fit app.** This App counts your daily walking distnce-steps, running distance-steps, cycling distance-steps.
Your **Heart points**, **calories** and many more things. So I downloded my google fit dataset from **takeout.google.com** website.

I wanted to predict how much **calories** we will burn if we give a walking, running and cycling distance.
I used **Artificial Neural Network** to train my model.

## 2. Model Trainning:
To train my model I downloded additional dataset from kaggle. After that I dropped unncessary columns. 
Using **Simple Imputer** module from scikit-learn library I handeled missing values, after that I had to use **Stander Scaler** to scale column values.

**Parameters:**

    a. Number of Units = 60
  
    b. Activation function = Rectified Linear Unit(Relu)
    e

    c. Regularizer lambda value = 0.001
    
    d. Optimizer = Adamax
    
    e. Loss = mean_squared_error
    
    f. metrics = mean absoulte error, mean absoulte percentage error.
    
    g. batch size = 1
    
    h. No of epochs = 200
    
   
**Loss:**


At epochs 1- 
    
    a. mean squared error = 3183943.2643
    
    b. Mean absolute error = 1759.6287
    
    c. Mean absolute percentage error = 95.6408%
    

At epochs 200-

    a. mean squared error = 457.76
    
    b. Mean absolute error = 14. 70
    
    c. Mean absolute percentage error = 0.79%


**Why did I used regularization?**

On training dataset I got mean absoulte percenatge erroe as 0.79% but when I evaluted my model on testing dataset I got MAPE as 52.46%. So that means my model was having high variance, to reduce the high variance we can perform following steps:

1. Add more training datset
2. Regularization
3. Drop out 
4. Data Augmentation

I had limited number of training datset so I coulden't use that. I tried Drop out but it wasn't that much effective and data aumentation is possible on image or video dataset so I tried **Regularization** and I got mean absolute percentage error as 50.67%
















