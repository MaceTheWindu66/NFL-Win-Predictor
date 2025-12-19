# NFL-Win-Predictor
A stacking ensemble model that predicts if the home team will win or lose an NFL game.  
This project is continuously being updated to be made better. Will eventually be uploaded to a website to display predictions.  

## Current Evaluation Metric Scores:  
> Accuracy: 69.5%  
> ROC-AUC: .69  
> F1: .72

## About this Project  
This project is a personal project facilitated by my Graduate Machine Learning class, where we were tasked to tackle an ML problem that we thought was interesting. I love sports, especially football, and building predictive models for sports I find to be a super fun challenge. Given the nature and unpredictability of football, I've given myself a target accuracy of 70%, which would be considered very good. Considering most models struggle to reliably get above 65%, I think this challenge will push me to seriously consider all different areas of engineering artificial intelligence to score higher and perform more efficiently.  

## Data Analysis  

This project had tons of interesting opportunities for EDA where my domain expertise in football certainly helped. I added a multitude of rolling / season stats, such as QB Rating, Rush/Pass yards, EPA (Expected Points Added per Play), among many other stats.  

To squeeze extra accuracy out of the data, I looked at the data distributions and, as I expected, the distributions throughout seasons were not stationary. Thus, I found it best to switch the dataset to a Time Series dataset instead of a random split. Rolling/Seasonal stats have severely weak signals at the beginning of the year (the data pool for the first few games is simply not reliable in the NFL). Thus, time series splits and including week numbers in the dataset is essential in a problem such as predicting NFL games, that way the model can learn about the shifting distributions of data throughout seasons.  

