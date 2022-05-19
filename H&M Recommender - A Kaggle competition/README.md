## Problem Statement

Recommender systems are everywhere nowadays. From Netflix to Facebook and Spotify, every technology related company seems to be building a recommender system of sorts. 

H&M Group is also no exception. In a Kaggle competition, hosted between February to May 2022, H&M provided several datasets for participants to build recommenders which can accurately predict what 12 products their customers will buy in the next 7 days.


## Executive Summary
A data science approach was used to guide the process. The problem statement was defined as building a recommender model which has high accuracy in predicting 

Data was provided purely from Kaggle by H&M. An exploratory data analysis was to evaluate and understand key trends, and top used words before coming up with the areas which will be visualized. 

Inferences are made at each visualisation and exploratory data analysis stage, and external reasons were made to give insights. 

With the data given, I have managed to come up with 5 models. Similar to what Kaggle discussion boards noted, I also noted that my best performing model seems to be a rule based model. 

I have went on to ensemble the 5 models, with great success in improving the evaluation metric further, and this was used as the final model for submission.

## Learning points
- 1) Google Colab has GPU and High RAM that needs to be requested. This can help to run high requirement notebooks.
- 2) Parquet, and memory saving techniques can be helpful to reduce size of data by up to 8 or 16 times.
- 3) Some tricks learnt – strings use 64 bytes, if converted to int64, it is only 8 bytes. Just need to add back the leading 0 afterwards before submission.
- 4) Others: conversion to int8 and float32 
- 5) RAPIDS cuDF can speed up running of notebook from 2hours to few minutes. Supported on Google Colab but need to run the code each time to install each time I restart
- 6) Kaggle discussion boards are a good place to learn first hand. If I have a group to work on, more ideas can be tested.


## Future works
#### Top models solutions are slowly appearing
I noted that there is a large improvement that the state of the art models have versus the silver and bronze and even the top 1000 category. Most of the winning solutions seems to be using Light GBM (LGBM) model of some sorts, however, in this area, there is relatively sparse documentation and reference on the coding, especially for using the Ranker function. I am hoping to pick up how I can improve my existing LGBM Ranker model.





