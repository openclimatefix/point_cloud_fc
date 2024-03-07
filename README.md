# Forecasting Point Cloud Intensity

### Aims
- The aim of this project is to forecast the intensity of a point cloud.
- This should be done using the EUMETSAT Geostationary satelite.
- A forecast should be made for up to 8-48 hours ahead.
- The model should use state of the art deep learning.
- This should also be built in a way that can be productionised.
- All repsective lag features and production style simulations should be done.
- To keep this project simple, we will only be forecasting the intensity of the point cloud by using the EUMETSAT Geostationary satelite.

The goal is use this data as an "NWP" style in the pv-site-prediction model which will pass in this forecasted point cloud intensity as a feature. 

This project will be done in the following steps:
- Data Collection
- Data Preprocessing
- Model Building
- Model Training
- Model Evaluation
- Model Deployment

We can use HRV and non-HRV data. For HRV data we can use a 2D convolutional layer to extract features For non-HRV a 3D model can be used. It will be interesting to see how these two models compare and how much additional improvement there will be using multiple channels.

Keeping the model 2D should increase the speeed to run and train the model.


## Inputs

EUMETSAT images should be used, which are cropped around a single point. Experiments could be done to find the optimal grid size (20x20km should be a good start). The past 2 hours of history (also to be determined) should be passed into the model to forecast that single point.


## Outputs

Forecast for cloud intensity for a specific point.

