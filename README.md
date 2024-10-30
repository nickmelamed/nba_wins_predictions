# NBA Wins Predictions 

## Motivation and Overview

### Question 1: Does More 3s Lead to More Points? 

The NBA has been changed dramatically by the rapid rise in 3 point shooting, seeing the shot rise from 22.2% of team shots taken in 2011 all the way up to 39.2% in 2021. The rise has come in conjunction with the embrace of analytics in basketball, which dictate that since 3 > 2, shooting more 3s is the optimal team strategy. 

We want to see if this phenomenon holds true on the individual level. We are interested in exploring if shooting more 3s has a causal impact on an individual player’s scoring, not just a linear association. This has some real-world relevance because if players are shooting more 3s without merit, they would be well-served in changing their strategy, both for the betterment of themselves and of the team.

I will be using an unconfoundedness method, specifically outcome regression, to see if we can find a causal impact. 

As for why outcome regression, I wanted to use an unconfoundedness method since there isn’t a source of randomness to produce a natural experiment, and since we are accounting for a lot of confounders, I felt like creating a regression model that takes into account observable confounders that have a linear relationship made the most sense in terms of interpretability of results. 

We are faced with some limitations, as we cannot observe every single possible confounder, such as a team strategy of all players shooting more 3s. So, our utilization of the unconfoundedness assumption, while still likely valid, does operate under a level of uncertainty. If it turns out that these unobserved confounders have a lot of influence over our causal impact estimate, then we are left with a result that is unusable. 

### Question 2: 

Over the decades, the game has evolved in numerous distinct ways. The prior eras of basketball can be described in a few. The 1980s focused heavily on individual-focused play with Michael Jordan as the global icon of the Chicago Bulls, captivating the world with inhuman athleticism and scoring prowess. The 1990s combined the ability of physically dominant big men like Shaq with perimeter stars like Kobe. This current era of basketball (2010s-present) can be characterized by its offensive heavy nature in the small ball and three-point revolution, where teams employ smaller, agile players to create spacing for better shot creation. Teams, like the Golden State Warriors and Cavaliers, have found major success with their efficient shooting in players like Stephen Curry or Kyrie Irving. 

Defense has drastically changed in this area which affects statistics like blocking and steals. One example of this could be seen in hand-checking, a defensive technique in which a defending player uses their hand or arm to make contact with the offensive player they are guarding to slow their movement. It was a common defensive tactic used earlier, but the NBA has introduced rule changes to limit or eliminate hand checking to promote a more open and free-flowing style of play. The restrictions on hand checking have increased offensive freedom and enhanced scoring opportunities and place a greater emphasis on individual defensive skills, such as footwork, positioning, and anticipation, rather than relying on physical contact with the offensive player.

So despite all of these changes in the game, the same counting stats are used as the gold standard of player performance. Do these statistics warrant this praise? Or are they overrated in terms of predictability of performance? 


## Data

We will be using two datasets, the first one being a collection of team statistics from the 2022-2023 NBA season (`2023_teams.csv`), the second being a collection of individual player statistics from the 2022-2023 NBA season (`2023_players.csv`). 

Both of these datsets come courtesy of NBAstuffer.com, a NBA statistic aggregator. The links for the respective datasets are [here](https://www.nbastuffer.com/2022-2023-nba-team-stats/) and [here](https://www.nbastuffer.com/2022-2023-nba-player-stats/). Note that you should be on the "Regular Season" tab to access the correct CSV files. 

## Analysis

`main.ipynb`: Main narrative notebook that includes entire analysis as well as additional commentary. 