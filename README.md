##Overview

1. Data Extraction
2. Data Transformation
3. Data Infrastructure
4. Feature Engineering
  4.1 Feature Selection
  4.2 Hyperparameter Tuning
5. Time Series Analysis
6. Model Experimentation and Optimization

#Dataset Overview:
Source: https://www.gdeltproject.org/
GDELT project provides a medium to access the global news. GDELT project breaks down the access and
language barriers and offer a near real time insights into the world around us. GDELT project makes
massive computations and fetches us the information from every corner of the world. It binds the news
from over 100 languages and more than 300 categories of events.
Examples of event types: Political, Criminal, Business, Education, Protests, Riots etc.,
The GDELT Project is an initiative to construct a catalog of human societal-scale behavior and beliefs across
all countries of the world, connecting every person, organization, location, count, theme, news source,
and event across the planet into a single massive network that captures what's happening around the
world, what its context is and who's involved, and how the world is feeling about it, every single day.
There are two versions of datasets in the GDELT Project:
Version 1: Contains all the news data from 1979 to present. It is one of the world’s biggest dataset with
almost quarter billion records.
Version 2: An updating stream of data which updates every 15 minutes fetching us the news from all
over the world of the past 15 minutes.

Key Terms of Dataset: 
Event: An event is defined as an action that an actor (Actor1) takes on another actor (Actor2). An actor can be a person, organization, company or location. 
Actor 1 and Actor 2 could be any person, location, organization, theme etc., 
Example: Kartik is passionate about Machine Learning. Here Actor1 is Kartik and Actor 2 is Machine Learning. 
Mention: A mention is an article or any source that talks about an event. 
Goldstein scale represents the level of conflict or cooperation. It ranges between -10 to 10 where -10 represents extreme Conflict and +10 represents extreme cooperation. 
Average Tone:  average “tone” of all documents containing one or more mentions of this event. 
QuadClass: This field specifies this primary classification for the event type, allowing analysis at the highest level of aggregation. The numeric codes in this field map to the Quad Classes as follows: 1=Verbal Cooperation, 2=Material Cooperation, 3=Verbal Conflict, 4=Material Conflict.

#Data Engineering:
1. Used Google Big Query to extract Quarter billion datapoints from GDELT dataset.
2. Used PySpark, Python and Amazon Athena to transform the data by eliminating all unnecessary columns.
3. Created an end to end architecture to extract, preprocess and generate quality insights of the dataset and create a UI to display the visualizations using Amazon EC2 server
4. Created a Flask framework to work with dynamic version 2 dataset which updates every 15 minutes and display dynamic visualizations on a UI which keeps updating every 15 minutes. (Using crontab services) 
5. Generated a time series analysis to observe trends and patterns in the dataset
6. Optimized the model using feature engineering techniques and experimenting with several Machine learning and deep learning algorithms.
  6.1 Support Vector Machines
  6.2 Logistic Regression
  6.3 Sequential Neural Network
  6.4 Sequential Neural Network with Standardized dataset
  6.5 Complex Neural Network Topology
  6.6 Feature Selection
     6.6.1 Chi Squared
     6.6.2 Tree Based Selection
     6.6.3 Recursive Feature Elimination
     6.6.4 Lasso
  6.7 Hyperparameter Tuning
     6.7.1 Grid Search
     6.7.2 Randomized Search
2. 
