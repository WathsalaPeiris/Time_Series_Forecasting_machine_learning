# Time_Series_Forecasting_machine_learning
This project describes few methods that can be used in predicting time series data. 
The aim of this project is to find out how the changes of Consumer Price Index (CPI) affect to changes of Wage Price Index (WPI) in Australia. For both indexes CPI and WPI, the percentage change from previous quarter for quarters from 1998 through to 2022 has beedn used in this analysis.

# Main sections
Part 1 - Tableau visualisation for forecasting CPI percentage changes
Part 2 - Predicting WPI percentage change using a Linear Regression model
Part 3 - Forecasting WPI percentage change using an Arima model
Part 4 - Predicting WPI percenatge using LSTM Neural network model

# Part 1 - tableau
In this section below points are visualised:
1. CPI percentage changes from previous quarter by main city in Austrlaia and by year (2009 - 2022)
2. The realtionship between CPI percentage change and WPI percentage change - From the two time series plotted in one graph shows that a shift in CPI will reflect a shift towards same direction within next few quarters but the size of the change is not same.
3. Used Tableau buit-in functions to forecast CPI percentage change.
4. https://public.tableau.com/app/profile/wathsala.peiris/viz/CPIandWPIpercentagechangesinAustralia/Story1?publish=yes

# Part 2 - Linear Regression model
In this section the viewer can see an attempt to predict 2023 Quarter1 WPI percentage change based by fitting a Linear regresson model. The WPI time series was considered as a univariate time series in this section and predicted only based on its previous values. The effect of CPI is not considered here.
Before fitting the LR model, the Augmented Dickey Fuller Test was applied to test for stationary of the time series. Originaly time series was not stationary and therefore time series was detrended using first differenced method. After detrending the time series has become stationary based on ADF test. The autocorrelation and partial autocorrelation was not that strong after detrending. Then fitted a linear rgression model for the detrended time series.

# Part 3 - Arima model
Repeated the same steps as per Part 2 except fitting Linear Regression model. Instead of Linear Regresson model, an arima model was fitted in this section. Using the Arima model the time series was forecasted for the last 20 quarters. In this section also, the effect of CPI was not considered.

# Part 4 - LSTM neural network model
In this section a Keras sequantial model was developed to predict WPI changes using previous WPI changes and CPI changes. When plotted the Actuals and predictions, this model looks more accurate than previous two models, linear regression and arima model done in Section 2 and 3.

# Requirments
tableau workbook has been uploaded so if anyone interested can download and open in tableau. Also the link to the publish is provided.
The python codes for section 2 and 3 can be run in jupyter notebook importing some common libraries such as pandas, sklearn, etc.
The python codes for section 4 needs to import Tensorflow - If need to use Google colab, please make sure the importing csv file paths are correct. Because this file uses the outcome of the section 2 and 3 codes. Those output csv files are uploaded in this repository as well. 




