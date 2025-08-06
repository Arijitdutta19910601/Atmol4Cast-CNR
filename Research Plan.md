# Research Plan for Stay

## Project Title : 
### Study and Design of Data Collection System for Discovery of Potential Renewable Sources using IoT.

## Mobility Period Mission: 
### Probabilistic Data Driven Causality Inferencing and Graphical Neural Network based Forecasting.

## Participant Info

#### Name: Arijit Dutta
#### Affiliation: University of Calabria & ISAC-CNR Lamezia Terme
#### Primary Supervisor(s): Prof. Dr. Floriano De Rango and Dr. Claudia Roberta Calidonna
#### Supervisor in Host Institute: Dr. Irene Schicker
#### Grants and Funding: This project is jointly funded by Tech4You-CNR (Identification Code: ECS_00000009 | CUP: H23C22000370006), which comes under the scheme National Recovery and Resilience Planning (PNRR), Government of Italy, under the Next Generation EU (NGEU) instrument.

## Objectives / Goals

#### [Offshore LMT Data] 
####    ↓
#### [Preprocessing (Alignment, Cleaning, Normalization) & Feature Engineering (Lag Features, ETS Decomposition)]
####    ↓
#### [Dynamic Bayesian Network (DBN) Learning] / [Hidden Markov Model + Granger Causality]
####    ↓
#### [Probabilistic Causal Graphs (Inferred Temporal-Causal Structure)]
####    ↓
#### [Graph Construction (Nodes = Stations, Edges = Causal Links, Edge Weights = Causal Strength)]
####    ↓
#### [Regime Specific Anomaly Identification]
####    ↓
#### [DCRNN (Diffusion Convolutional Recurrent Neural Network) or STGCN (Spatio-Temporal Graph Convolutional Network)]
####    ↓
#### [Anomaly Detection Head (optional: via prediction uncertainty or classification)]
####    ↓
#### [Probabilistic Forecasting (Wind Speed Distributions) OR Traditional Deterministic Forecasting]
####    ↓
#### [Evaluation Metrics: CRPS, Brier Score, Reliability Diagrams, ROC Curves and AUC]
####    ↓
#### [Comparison with Numerical Weather Prediction (NWP) Models (e.g., WRF, ECMWF forecasts)]


## Context and Alignment

#### The previous projects of the Atmol4Cast-REN group of Geosphere Austria have profound experience and relevant evidence in Wind Data Forecasting. The projects, such as MEDEA, SSEA, Wind4Future, and WINDSOR, are some of the work they have done extensively on wind speed and energy forecasting for short-term and nowcasting. 

## Structure by Time (usually by month or phase)

### Month 1: Orientation, literature, data familiarization
#### Week 1: Spent time diving into relevant literature regarding forecasting techniques. According to the suggestions, the focus is also on AD, ETS, and CRPS implementation details.
#### Week 2: Purely focused on understanding the orographic context, wind characteristics, and the peculiarity of the terrain of the observatory of Lamezia Terme and the other locations in Italy. The details would be useful to do Data preprocessing and feature engineering before training the model with DBN.
#### Weeks 3 and 4: A brief plan and accomplishments, research goals were presented. A rework has also been initiated on some of the previous works according to suggestions. The focus is now completely shifted to the Offshore wind data from 2015 to 2018. 

### Month 2: Method development, prototyping

#### Weeks 1 and 2: Preprocessing of the LMT Wind Lidar data with the parameters as mentioned below:
#### wind speed data for 11 vertical levels, their corresponding wind directions, air temperature, humidity, and Pressure from 2015-01-01 to 2018-12-31
#### Removed Outliers and sensing Faults using STL Decomposition, Calculated Lagged features for 24 hours (144 steps, 10-minute data), and conducted a stationarity test and found the dataset to be stationary. Additionally calculated the residuals and the Trend.
#### We conducted residual analysis to determine the characteristics of the data, whether it is Gaussian/Normally Distributed or not. We plotted the Q-Q plot, evaluated the Shapiro-Wilk results, and conducted statistical Tests of D'Agostino and Anderson. The p-value proves the null hypothesis is true, hence it is non-Gaussian.
#### Weeks 3 and 4: As the dataset is found to be non-Gaussian, we applied the Box-Cox, Yeo-Johnson, and Quantile Transformation on the data and obtained the kurtosis and skewness values. It is validated that the closest Gaussian Transformation of the dataset happened through the Yeo-Johnson / Power transformation.

### Month 3: Testing, application, documentation

#### Weeks 1 and 2: Applied the ADF-Test to determine the stationarity of the transformed data again and found it is not seasonal. As we have multiple time series data, which could be used for regression, we applied Vector Autoregression (VAR) to capture the relationship between multiple quantities as they change over time. VAR is a type of stochastic process model. We categorically evaluated AIC (Akaike Information Criterion), BIC (Bayesian Information Criterion), FPE (Final Prediction Error), and HQIC (Hannan–Quinn) statistical measures. However, for the sake of the time series forecast, we considered the BIC to select the optimal lag order by evaluating the trade-off between the model's ability to fit the data (likelihood) and the number of parameters (model complexity).
#### Weeks 3 and 4: We evaluated the Granger Causality Matrix with the BIC ordered lag and defined the influences of each metric on each vertical level of wind speed.  Further, we incorporated the Hidden Markov Model to discover the hidden causal states with the regime switch, and using a graph, we depicted the influences of those metrics on the wind speed. We also identified the Anomalies and their distribution in each regime. Finally, ETS Modelling on the transformed data to Forecast is applied.

## Deliverables / Outputs

#### Platform: A seamless tool for wind energy forecasting visualisation which collects wind data from heterogeneous sources (Lidar, Meteo Mast, ATLAS, models, etc.), harmonizes preprocessing, and provides detailed analysis. The comparison between these models should provide the novel architecture's edge over other existing models.

#### Publications: At least one reputed Q1 journal article.

## Optional Additions

Expected meetings or collaborations

## Learning outcomes





## Literature:
#### https://onlinelibrary.wiley.com/doi/epdf/10.1002/we.2497
#### http://www.jethrobrowell.com/uploads/4/5/4/0/45405281/browell_eem2017.pdf
#### http://www.jethrobrowell.com/uploads/4/5/4/0/45405281/very_short_term_reveiw.pdf
#### https://royalsocietypublishing.org/doi/epdf/10.1098/rsta.2016.0101
#### https://alpnap.i-med.ac.at/alpnap.org_en.html
#### Calidonna, C. R., Dutta, A., D’Amico, F., Malacaria, L., Sinopoli, S., De Benedetto, G., Gullì, D., Ammoscato, I., De Pino, M., & Lo Feudo, T. (2025). Ten-Year Analysis of Mediterranean Coastal Wind Profiles Using Remote Sensing and In Situ Measurements. Wind, 5(2), 9. https://doi.org/10.3390/wind5020009 
