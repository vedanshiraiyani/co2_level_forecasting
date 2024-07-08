# CO2 level forecasting

Forecasting is performed using the Mauna Lua CO2 dataset (monthly) using an MLP and compared the results with that of MA (Moving Average) and ARMA (Auto Regressive Moving Average) models. 

Main setting: Used previous “K” readings to predict next “T” reading. Example, if “K=3” and “T=1” then we use data from Jan, Feb, March and then predict the reading for April. 

The moving average(MA) and the auto regressive moving average (ARMA) are used from staatmodels library.
The MLP is built with 3 hidden layers. The input layer has "K" neurons (for previous "K" readings) and the output layer has "T" neurons (for predicting next "T" readings).

<h2>For MLP</h2>
<h5>The loss after 5000 epochs comes out to be as small as 5.75. The true v/s predicted graph for MLP can be seen below</h5>
![download](https://github.com/vedanshiraiyani/co2_level_forecasting/assets/117573771/2cf8ca52-2674-4400-8dcf-cfbcd3082e9b)



<h2>For MA</h2>
<h5>The mean squared error comes out to be quite high as 24.7. The true v/s predicted graph for MA can be seen below</h5>
![download](https://github.com/vedanshiraiyani/co2_level_forecasting/assets/117573771/e7947d0c-7bb6-41a2-8a04-f32bd1ac3096)




<h2>For ARMA</h2>
<h5>The mean squared error comes out to be minimum which is 1.3. The true v/s predicted graph for ARMA can be seen below</h5>
![download (1)](https://github.com/vedanshiraiyani/co2_level_forecasting/assets/117573771/457b9452-e02e-463f-b12e-b881e49f7daa)


<br><br>

From the results we can see that the ARMA model outperforms the other two.
