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

#### [Onshore & Offshore Data] 
####    ↓
#### [Preprocessing (Alignment, Cleaning, Normalization) & Feature Engineering (Lag Features, ETS Decomposition)]
####    ↓
#### [Dynamic Bayesian Network (DBN) Learning]
####    ↓
#### [Probabilistic Causal Graphs (Inferred Temporal-Causal Structure)]
####    ↓
#### [Graph Construction (Nodes = Stations, Edges = Causal Links, Edge Weights = Causal Strength)]
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

### Month 2: Method development, prototyping

### Month 3: Testing, application, documentation

## Deliverables / Outputs

#### Platform: A seamless tool for wind energy forecasting visualisation which collects wind data from heterogeneous sources (Lidar, Meteo Mast, ATLAS, models, etc.), harmonizes preprocessing, and provides detailed analysis. The comparison between these model should provide the novel architecture's edge over other existing.

#### Publications: At least one reputed Q1 journal article.

## Optional Additions

Expected meetings or collaborations

## Learning outcomes





## Literature:
#### https://onlinelibrary.wiley.com/doi/epdf/10.1002/we.2497
#### http://www.jethrobrowell.com/uploads/4/5/4/0/45405281/browell_eem2017.pdf
#### http://www.jethrobrowell.com/uploads/4/5/4/0/45405281/very_short_term_reveiw.pdf
#### https://royalsocietypublishing.org/doi/epdf/10.1098/rsta.2016.0101
#### Calidonna, C. R., Dutta, A., D’Amico, F., Malacaria, L., Sinopoli, S., De Benedetto, G., Gullì, D., Ammoscato, I., De Pino, M., & Lo Feudo, T. (2025). Ten-Year Analysis of Mediterranean Coastal Wind Profiles Using Remote Sensing and In Situ Measurements. Wind, 5(2), 9. https://doi.org/10.3390/wind5020009 
