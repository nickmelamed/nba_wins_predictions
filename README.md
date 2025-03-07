# NBA Wins Predictions 

## Motivation and Overview

### Question 1: Does More 3s Lead to More Points? 

The NBA has been changed dramatically by the rapid rise in 3 point shooting, seeing the shot rise from 22.2% of team shots taken in 2011 all the way up to 39.2% in 2021. The rise has come in conjunction with the embrace of analytics in basketball, which dictate that since 3 > 2, shooting more 3s is the optimal team strategy. 

We want to see if this phenomenon holds true on the individual level. We are interested in exploring if shooting more 3s has a causal impact on an individual player’s scoring, not just a linear association. This has some real-world relevance because if players are shooting more 3s without merit, they would be well-served in changing their strategy, both for the betterment of themselves and of the team.


### Question 2: Do Advanced Statistics Have Predictive Value for Wins? 

Advanced metrics, or statistics that take basic counting stats and transform them into a singular, useful value, have become a hallmark of team and player evaluation. Look no further than MVP voting, beat articles, and draft evaluations to see that advanced metrics are widely wielded. There is clearly sentiment that these statistics are incredibly useful. But is this true? 

If advanced statistics have predictive value when it comes to winning, then teams are making the right choice by evaluating their own and other team's performances using these metrics. If they are not, then the analytics-heavy teams are in trouble...


## Data

We will be using two datasets, the first one being a collection of individual player statistics from the 2022-2023 NBA season (`2023_players.csv`), the second being a collection of team statistics from the 2022-2023 NBA season (`2023_teams.csv`). 

Both of these datsets come courtesy of NBAstuffer.com, a NBA statistic aggregator. The links for the respective datasets are [here](https://www.nbastuffer.com/2022-2023-nba-player-stats/) and [here](https://www.nbastuffer.com/2022-2023-nba-team-stats/). Note that you should be on the "Regular Season" tab to access the correct CSV files. 

## Analysis

`Q1_main.ipynb`: Main narrative notebook for Question 1 that includes entire analysis as well as additional commentary. <br><br>
`Q2_main.ipynb`: Main narrative notebook for Question 2 that includes entire analysis as well as additional commentary. 

## Q2_dependencies (Dependencies/Installation)

`environment.yml` and `Makefile` are used for `Q2_main.ipynb` because I use pymc which requires certain dependencies. So, to make sure these run properly for Q2_main.ipynb, run `make env` in your terminal/shell to set up the conda environment.

Then use resulting Q2_main kernel to run all analysis notebooks. 

Alternatively, you can use the `environment.yml` file and set up the environment the traditional way using `conda`. 