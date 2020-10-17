@ Copyright 2020 Matthew Mingyeom Cho

# F1 Race Prediction Model

Amazon Web Services explain it best in their 2018 Formula 1 Case Study: "Formula 1 is a data-driven sport. During each race, 120 sensors on each car generate 3 GB of data, and 1,500 data points are generated each second ... Formula 1’s data scientists are training deep-learning models with 65 years of historical race data to extract critical race performance statistics, make race predictions, and give fans insight into the split-second decisions and strategies adopted by teams and drivers."

Being able to accurately predict Formula 1 race results can be a great asset to the sport and the motor racing industry in general. Hence why for this reserach project, I decided to build an F1 race prediction model using deep learning and Tensorflow in Python. There were two major steps involved: (1) dataset creation and (2) building the prediction model.

## 1. Dataset creation

The first step of building the F1 prediction model was to retrieve relevant features and data for training and testing. After comparing multiple online F1 datasets, I found that [Ergast API](http://ergast.com/mrd/) provides the most comprensive historical record of F1 data since the beginning of the World Championships in 1950. Once the data tables were downloaded as CSV files (view in "raw_data" folder above), they were preprocessed to generate a single data table containing potential input and output features (view in "dataset.csv" file above). 

This is shown in the [dataset_creation.ipynb](https://github.com/mattcho1157/f1_race_prediction_model/blob/main/dataset_creation.ipynb) Jupyter Notebook file above.

## 2. Prediction model

After preprocessing the data and filtering the features engineered, I trained an initial basic model with 2 hidden layers, which was then evaluated to further refine the data structures find any abnormal outliers. Subsequently, the hyperparameters of the initial model were tuned via random search to find the optimal model for predicting F1 race results. The accuracy of the final model was 85% - a highly successful result given the volatility and unpredictability of F1 races. An evaluation and recommendations for potential extensions and improvements to this model have also been explored.

This is shown in the [prediction_model.ipynb](https://github.com/mattcho1157/f1_race_prediction_model/blob/main/prediction_model.ipynb) Jupyter Notebook file above.
