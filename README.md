# FIN 377 Final Project - Swish Insights

### Link to Website:
https://brandon4106.github.io/Fin_377_Swish_Insights

## Repository Setup

### Code used for scraping:

1. runboxscores.ipynb
2. getstatsfromboxscore.ipynb

### Code used for exploration, analysis, and modeling:

1. CreatingModels.ipynb

## Project Overview

The main goal of this project is to train a model that can aid sports bettors with bets for the NBA season. In particular, the model will do an in depth analysis of one team and try to make a profit on the spread for the games in March, the holdout set. The model will accomplish this by using the statistics it's learned throughout the season, in the training set. This analysis requires a significant amount of scraping for the one team we have selected the Celtics as well as additional scraping to build predictions for the Celtics opponents.

In setting up a machine learning pipeline, it is necessary to establish your X and y variables. For this project, our X variables were data statistics on the Celtics and the statistics of the Celtic's opponent right before their game was played. For instance, what is the Celtic's average win percentage, what was their offensive rating of the last 10 games, how are they currently ranked in the conference, how many key players are missing from both team? With this, our goal is to predict (y variables) the difference in the teams' scores (Celtic's score - opponents score). From here, depending on our prediction, our model will place a bet on the spread a sports betting platform has placed. If our model thinks the Celtics will win the spread, it will bet on the Celtics, and vice versa. For this project, we are assuming a constant bet size of 100; however, there is a place to change this within the code.

## Extra Links

### Links to sources we used to obtain data:

1. https://www.actionnetwork.com/nba/odds/boston-celtics
2. https://www.basketball-reference.com/boxscores/

### Link to the slideshow presentation:
https://docs.google.com/presentation/d/1yIrZOARtgEcDt4hhq3I2KpJM72dGAiEVx83RGe7Qf4g/edit#slide=id.g2d13450eb15_1_452






