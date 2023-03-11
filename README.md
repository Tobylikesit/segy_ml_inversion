# Seismic Inversion using Machine Learning

This repository contains python notebooks used for seismic inversion using machine learning techniques.

## Data

The data used in this project consists of post-stack seismic data from a survey in the ?. The data is provided in SEGY format and includes seismic traces as well as few well logs.

## Preprocessing

Before training the machine learning models, the data is preprocessed in several steps:
- Data is loaded and converted to a format suitable for training.
- Data is resampled to reduce computational requirements.
- Data is split into training and testing sets. (K-fold is applied only for TCN)

## Models

Several machine learning models are implemented and evaluated:
- Support Vector Regression (SVR)
- Random Forest Regression (RFR)
- Convolutional Neural Network (CNN)
- Temporal Convolutional Network (TCN)
- Linear Regression

## Results

The performance of each model is evaluated using the root mean squared error (MSE) metric:
- SVR: 0.1791
- RFR: 0.1607
- CNN: 0.1542
- TCN: 0.1497
- Linear Regression: 0.1497

## Conclusion

Based on the results, the TCN and Linear Regression models perform the best. However, the performance of all models could be improved by using more spatial data, such as multiple wells, and by increasing the resolution of the seismic data. 

## Dependencies

The code requires the following packages:
- numpy
- pandas
- scikit-learn
- tensorflow
- keras
- matplotlib
- obspy
- segyio

## Usage

To run the code, first install the required packages. Then, download the SEGY data and place it in the `data` folder. Finally, run the Jupyter notebooks in the main folder.

## License

This project is not licensed.

