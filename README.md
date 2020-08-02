# XGBalling: Hacking Basketball Game Prediction with ML
### Predict March Madness tournament outcomes using XGBoost and counter-intuitive feature engineering
![The Rise of the Three](https://raw.githubusercontent.com/hussien-hussien/xgballing/master/visualizations/three_pointers.gif)


[In-depth Write up](medium.com) - [Paper](https://github.com/hussien-hussien/xgballing/blob/master/SS3850___FINAL_PROJECT_SUBMISSION.pdf)

## Introduction
Every year, the NCAA (National Collegiate Athletic Association) hosts a popular college basketball tournament dubbed 'March Madness'. Mostly in March, 68 Division-1 college basketball teams compete in a single-elimination style tournament with the final two teams competing for the national championship. Match-ups are determined by a committee using divisions (regions) and seeds (ranking). Teams with seeds 1–4 would all be randomly assigned to separate divisions, teams with seeds 5–9 would all be randomly assigned to separate divisions, and so on until each region has 16 teams.

It has become wildly popular for fans to predict the outcomes of each game, with an estimated 60 million Americans filling out a bracket each year. In fact, in 2014 Investor Warren Buffet's Berkshire Hathaway and Quicken Loans teamed up to offer $1 Billion to any fan who can perfectly predict the 2014 Men's Bracket. With 67 games, the likelihood of randomly guessing a bracket is 0.5⁶⁷% or, to put it another way, your odds are 1 in ~148 quintillions. Very unlikely.

In this post, we develop a simple yet powerful strategy for predicting the outcome of match-ups in the NCAA March Madness tournament. We analyze each team's regular-season stats against one another and test various machine learning algorithms such as Logistic Regression, SVM, K-Nearest Neighbours, and XGBoost algorithms to output a predicted match outcome. *Ultimately, we were able to predict game outcomes with 90% test accuracy using simple features engineering and a gradient boosted tree algorithm (XGBoost).*

## Notebook Layout
*Preprocessing, Feature Engineering, Baselines.ipynb* - is the preprocessing notebook. In Section 1, we explore the preliminary data and create baseline model (logistic regression) based on 2 basic parameters. In Section 2, we expand the parameters by engineering aggregate season stats, advanced stats and power rankings for each team. We use this data to create a new baseline with logistic regression and export it as a new dataset for the model fitting notebook.

*Model-Fitting.ipynb* - This is where we fit the models to the data prepared in the above notebook. We perform hyper-parameter tuning, cross validation, dimensionality and regularization to get the best out of the ML algos tested.

*court_viz.png* - Used to create heatmap of shots made/missed on court.

*visualizations_2.rmd* - R notebook where small amount of EDA was done and most visualizations were made. Shout out ggplot2.

## Future Work
Future work is extensive. I want to see whether we predicted any upsets or if the model is simply going with the favorites. There is so much more data to take into account that I had time to look at but I would love to get features out of them in the future. I'd also like to see how effective this would be as a sports betting tool based on historical betting spreads on the games in the test set.

If you have any questions or want to help move this project forward, you can find me at [hussien.net](https://www.hussien.net).
