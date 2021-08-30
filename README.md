---
title: "NBA Forecasts"
author: "Coffy Andrews-Guo"
date: "8/29/2021"
output: html_document:
---

```{r setup, include=TRUE}
library(dplyr)
library(tidyverse)

nba <- read_csv("nba_elo_latest.csv")

```

## Introduction

In this article, How Our NBA Predictions Work, it describes a predictive modeling for NBA team ratings. The programmers used a combined framework system named "CARM-Elo". This predictive model used game results from Elo which tracks teams winnings, margin of victory and where the game was played. The CARMELO framework provides player projections during off season and season plays in the predictive model. 

This file contains links to the data behind [The Complete History Of The NBA] <https://projects.fivethirtyeight.com/complete-history-of-the-nba/> and our [NBA Predictions] <https://projects.fivethirtyeight.com/2020-nba-predictions/>

The sample table  

```{r, echo=TRUE}
nba %>%
  filter(team1 == "BRK") %>%
  select(date, team1, team2, elo1_pre, elo1_post, raptor1_pre, score1)

```

## Conclusion
The sample table depicts the team talent ratings for Brooklyn Nets, BRK. The predictive model uses various metrics on individual players effect on team's offensive or defense efficiency.  
