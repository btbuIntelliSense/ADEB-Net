# This warehouse offers source code and datasets for the ADE-BGI, the paper title entitled: Multivariable High-dimension Time-series Predictor via Adaptive Dual-graph-attention Encoder-decoder with Global Bayesian Inference.
p{
text-align: justify;
text-justify: inter-ideograph;
Abstract: High-dimensional multivariate time series (HMTS) forecasting methods focus on forecasting tasks in multi-factor fusion contexts. Existing HMTS forecasting methods lack attention to the global information of the sample dimension and have limited represent learning ability to the data, resulting in the network's inability to comprehend the relationship between similar events and its limited ability to mine the data's potential information. In this study, a brand-new model is put forth under the name Adaptive Dual-graph-attention Encoder-decoder with Global Bayesian Inference (ADE-BGI). In particular, the Dual-graphic Representation Module (DRM) determines the relationships between its analogous events and the relationships between its variables. The Adaptive Encoder-decoder Forecasting Module (AEFM) modifies the network's substructure using Bayesian inference and the dual-attention to filter the critical information of the sample and variable dimensions. The experimental results demonstrate that the proposed model achieves optimal results over three datasets, including stock prices, air quality, and traffic conditions, with relatively short, medium, and lengthy data volumes and forecasting strides, and its performance is enhanced by an average of 50%, 8.35%, and 46.13%. More experimental results demonstrate that the proposed model has enhanced forecasting accuracy and generalizability and has application potential and promise.}
# The roles of the six python program files are as follows:
  (1) main.py: main program, scheduling training, Bayesian optimization count setting. Run this program to start the ADE-BGI.<br>(2) layers.py: covers each neural network module and layer of the ADE-BGI, including the DRM and the AEFM.<br>(3) networks.py: the transmission of layers of the neural network.<br>(4) neural_trainer.py: the training, validation and testing process of the neural network.<br>(5) ParameterSet.py: parameter setting.<br>(6) losses.py: contains loss functions and evaluation metrics. 　
# The description of each dataset in the data folder is as follows:
  (1) Constituent Shares of the Shanghai Stock Exchange 50 Dataset (CSSSED)<br>  The CSSSED describes how the four price variables of the Constituent Shares of the Shanghai Stock Exchange 50 (000016) change over time. The dataset uses the 50 constituent stocks when the stock opens from May 2022 to August 2022, with 84-time steps, and the variables include opening price, closing price, highest price, and lowest price. The 50 constituent stocks are subject to the August 31, 2022, announcement by Eastmoney.com (https://www.eastmoney.com/). Since the constituent stocks of SSE 50 are adjusted every six months (January and July each year), the short-term prices of constituent stocks are more meaningful. The three-dimensional state of data can be expressed as (50, 84, 4). The total data volume (i.e., s×t×v) is 16800.<br>(2) Chinese Urban Air Quality Dataset (CUAQD)<br>  The CUAQD describes in 100 cities in China in the first 21 days of March 2022, three variables including AQI, PM2.5, and PM2.5 24-hour moving average change over time. With 504-time points, the sampling frequency is 1 hour. There is a small number of missing values, and the KNN algorithm (K=3) is used for interpolation. The three-dimensional state of data can be expressed as (100, 504, 3). The total data volume is 151200.<br>(3) PEMS-08<br>  The PEMS-08 describes traffic conditions detected by detectors deployed on highways in major metropolitan areas of California, USA. It has 170 detectors, the time is from July to August 2016 and the sampling frequency is 5 minutes (i.e., there are 17856-time points), considering three traffic measurements, namely total flow, average speed, and average occupancy. We used a subset of it in the main experiment, taking the amount of data from the previous four weeks(i.e., 8064-time points). The three-dimensional state of data can be expressed as (170, 8064, 3). The total data volume is 4112640.
