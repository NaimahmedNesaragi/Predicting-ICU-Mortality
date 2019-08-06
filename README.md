# Isaac_Kim_Project_03

Doctors and nurses working in the ICU can use all of the help they can get, and this project attempts to do so by creating a model they can use to help predict patient mortality, so they can better allocate available resources.

The data came from PhysioNet for a competition (in 2012), and it consists of 3 sets of 4000 text files (train, test, and a final validation set where the target was withheld from competitors). The text files have time series measurements, but some of the measurements are measured once, many times, different hospitals take different measurements, and generally the data was incredibly messy and a hassle to deal with.

I attmped to engineer standard deviation and anomaly features.
The overall cleaning, imputing data, and adding standard deviation features is done in the Import Data notebook. Time series anomaly detection using FBProphet is in the Anomaly notebook. In it you will find some interactive plots of the anomaly detectin using the module Altair. Most of the code was run on AWS or my separate home computer.
Finally, the major machine learning project was done in ICU Model Data notebook. That is the one you should primarily look at. 

Overall, the anomaly detection was a good idea, but it was so resource intensive that it was difficult to pull off (if I had more time, I am almost positive I could have better cleaned the data to make the anomaly features useful). Imputing missing data using MICE and intelligently using Lasso or OLS to select features made a big difference. And of course, of all the models (including ensemble methods), XGBoost was the clear winner. 
