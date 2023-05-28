# Appliance Energy Prediction

The data set is at 10 min for about 4.5 months. The house temperature and humidity conditions were monitored with a ZigBee wireless sensor network. Each wireless node transmitted the temperature and humidity conditions around 3.3 min. Then, the wireless data was averaged for 10 minutes periods. The energy data was logged every 10 minutes with m-bus energy meters. Weather from the nearest airport weather station (Chievres Airport, Belgium) was downloaded from a public data set from Reliable Prognosis (rp5.ru), and merged together with the experimental data sets using the date and time column. Two random variables have been included in the data set for testing the regression models and to filter out non predictive attributes (parameters)
## Project Files Description
This project includes a colab notebook, a data source and a presentation:
## Problem Statement
How much energy is consumed in indoor and outdoor appliances?

what is the coerration of humidity and temperature in indoor and outdoor environment?

Does the environment of sensor affects the way enegry is consumed by appliances?

Identify the appliances with low efficiency in home (which room) relationship between appliances and light

How weather is coerrated with the energy consumption in homes and why this study is important?

## Data Summary

The dataset given is a dataset from Appliance energyn , and we have to analysis the Energy consumed and the insights behind it.

Appliance energy is analytical studies How much energy consumed and realatioship between light and appliances

The above dataset has 19735 rows and 29 columns. There are no mising values and duplicate values in the dataset.

## Data Insights:

According to my idea, we will get a clear view of the appliances on monday appliances value is maximum

18th hour appliances value is more appliances value are correlated with winds value

if value of Press_mm_hg increase then decrease appliances value

Temperature columns - Temperature inside the house varies between 14.89 Deg & 29.85 Deg , temperatire outside (T6) varies between -6.06 Deg to 28.29 Deg . The reason for this variation is sensors are kept outside the house

Humidiy columns - Humidity inside house varies is between 20.60% to 63.36% with exception of RH_5 (Bathroom) and RH_6 (Outside house) which varies between 29.82% to 96.32% and 1% to 99.9% respectively.

Appliances - 75% of Appliance consumption is less than 100 Wh . With the maximum consumption of 1080 Wh , there will be outliers in this column and there are small number of cases where consumption is very high

Lights column - Intially I believed lights column will be able to give useful information . With 11438 0 (zero) enteries in 14801 rows , this column will not add any value to the model . I believed light consumption along with humidity level in a room will give idea about human presence in the room and hence its impact on Appliance consumption. Hence for now , I will dropping this column

Temperature - All the temperature variables from T1-T9 and T_out have positive correlation with the target Appliances . For the indoortemperatures, the correlations are high as expected, since the ventilation is driven by the HRV unit and minimizes air tempera-ture differences between rooms. Four columns have a high degree of correlation with T9 - T3,T5,T7,T8 also T6 & T_Out has high correlation (both temperatures from outside) . Hence T6 & T9 can be removed from training set as information provided by them can be provided by other fields.

Weather attributes - Visibility, Tdewpoint, Press_mm_hg have low correlation values

Humidity - There are no significantly high correlation cases (> 0.9) for humidity sensors.

Random variables have no role to play

## Conclusion
The best Algorithm to use for this dataset Extra Trees Regressor

The untuned model was able to explain 57% of variance on test set .

The tuned model was able to explain 63% of varaince on tese set which is improvement of 10%

The final model had 22 features

Feature reduction was not able to add to better R2 score

feb month has the highest energy consumption of appliances in home. This could mean people stayed more inside in the month feb. To find out if they stayed inside more because of weather conditions further analysis is made.

18th hour have most appliance value

All the temperature variables from T1-T9 and T_out have positive correlation with the target Appliances

All columns follow normal distribution except RH_6 and RH_out , primarly because these sensors are outside the house

## Credits
Rashul Lawania | Engineer | Machine Learning Enthusiast
