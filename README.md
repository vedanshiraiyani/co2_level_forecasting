# CO2 level forecasting

Forecasting is performed using the Mauna Lua CO2 dataset (monthly) using an MLP and compared the results with that of MA (Moving Average) and ARMA (Auto Regressive Moving Average) models. 

Main setting: Used previous “K” readings to predict next “T” reading. Example, if “K=3” and “T=1” then we use data from Jan, Feb, March and then predict the reading for April. 

The moving average(MA) and the auto regressive moving average (ARMA) are used from staatmodels library.
The MLP is built with 3 hidden layers. The input layer has "K" neurons (for previous "K" readings) and the output layer has "T" neurons (for predicting next "T" readings).

<h2>For MLP</h2>
<h5>The loss after 5000 epochs comes out to be as small as 5.75. The true v/s predicted graph for MLP can be seen below</h5>
<img src="https://github.com/vedanshiraiyani/co2_level_forecasting/assets/117573771/d04a9022-b24c-438d-92e1-517d2838c249", height=60%, width=60%>




<h2>For MA</h2>
<h5>The mean squared error comes out to be quite high as 24.7. The true v/s predicted graph for MA can be seen below</h5>
<img src="https://github.com/vedanshiraiyani/co2_level_forecasting/assets/117573771/118eb77d-04bc-4d26-95b5-317f0648702b", height=60%, width=60%>





<h2>For ARMA</h2>
<h5>The mean squared error comes out to be minimum which is 1.3. The true v/s predicted graph for ARMA can be seen below</h5>
<img src="https://github.com/vedanshiraiyani/co2_level_forecasting/assets/117573771/457b9452-e02e-463f-b12e-b881e49f7daa", height=60%, width=60%>


<br><br>

From the results we can see that the ARMA model outperforms the other two.
