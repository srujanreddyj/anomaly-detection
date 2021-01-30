# Anomaly Detection

### Project Goal
To learn more about anomaly detection methods and their importance in real-time business.


### Problem Description
Energy consumption has increased tremendously over the past decade. There will be more demand as new societies continue to get 24x7 electricity. This raises an important issue of detecting sudden spikes due to any reason. Detecting anomalies in electricity consumption can help all the stakeholders in the process, and thereby conserving our energy. 
We are provided with data of electric consumption values across various sites and activities. We are asked to come up with a methodology to detect anomalies beforehand. 

### Data Source
Data downloaded from Scheider Electric.
The data consisted of 5 CSV files.
Training data with timestamp and values of electric units for respective meter ids.
Weather data with a timestamp, temperature, site ids, and distance.
Holidays CSV files consisted of Date, type of holiday, and site_ids.
Metadata CSV file consisted of site Id, meter_id, Meter Description, units, surface, and activity.
The submission file had the true values of whether it is an anomaly or not.

### Dependencies
pandas
NumPy
scipy
Sckit-learn
Random forests
Isolation forests
XGBoost
Plotly
RAPIDS AI


### MODELS and METHODOLOGY USED
I used XGBoost to predict consumption values on weekdays and Isolation forest for weekends.
To predict an anomaly, I have used a rule-based method where if an error crosses a threshold, I marked it as an anomaly if that lies in the tail ends of the distribution.

### FUTURE SCOPE
This work can be further improved using a more rule-based approach to decide the right anomalies for each site and meter id. Using PCA and more feature engineering can give us more accurate predictions and then using rule-based hand-holding can help us achieving in more accuracy.
There is a lot of research going on in detecting anomalies in various sectors. The neural networks, GANs (novel unsupervised learning methods) are becoming more efficient in identifying anomalies. These methods can be very well be used to tabular data as well.


### CONCLUSION
This was a huge learning opportunity for me, where I had to come with a real and useful business case and make a rule-based decision and not just following a machine learning metric to define accuracy.
It has become very important to handle large data in prediction and python couldn't handle very comfortably and, hence other big data technologies like pyspark should be used.
