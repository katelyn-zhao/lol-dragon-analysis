# League of Legends Dragon Analysis

Author: Katelyn Zhao

## Overview

A comprehensive data science project completed for DSC80 at UCSD. The project encompasses all components of statistical analysis, starting with exploratory data analysis, followed by hypothesis testing and prediction models. The primary focus of this project is to analyse the relationships between in game neutral objectives (specifically Elemental Dragons) and game outcome. 

## Introduction

### Gameplay

League of Legends (LoL) is a multiplayer online battle arena (MOBA) game developed and published by Riot Games. It has become one of the most popular and influential video games in esports. 

In League of Legends, two teams of five players each compete to destroy the opposing team's Nexus, a structure located in the heart of their base, protected by turrets and defensive structures. Each player controls a unique character known as a "champion" each with distinct abilities, playstyles, and roles. Players gain gold and experience by defeating enemy minions, enemy champions, enemy structures, and neutral objectives, which they use to purchase items that enhance their champion's abilities and strength.

### Data

In this project, I will focus mainly on neutral objectives (specifically Elemental Dragons) and how they effect game outcome. To do this, I will use data collected from Oracle's Elixir. I will use the game data specifically from the year 2022, containing 148992 rows and 131 columns. 

### Columns

The columns that are relevant to the analysis are as follows:

- `gameid`: a unique id for every individual game

- `league`: the regional league in which the game was played

- `teamname`: the name of the team that played in each specific game

- `side`: the side of the map the team's Nexus resides

- `result`: the outcome of the game

- `gamelength`: the length of the game in seconds

- `firstdragon`: binary variable where 1 indicates the team got the first dragon and 0 indicates that the team did not get the first dragon

- `dragons`: the total number of dragons a team takes throughout the entire game (elemental and elder)

- `elementaldrakes`: the total number of elemental dragons a team takes throughout the game

- `infernals`: the total number of infernal dragons a team takes

- `mountains`: the total number of mountain dragons a team takes

- `clouds`: the total number of cloud dragons a team takes

- `oceans`: the total number of ocean dragons a team takes

- `chemtechs` : the total number of chemtech dragons a team takes

- `hextechs`: the total number of hextech dragons a team takes

- `elders`: the total number of elder dragons a team takes


## Data Cleaning and Exploratory Analysis

### Data Cleaning


The head of the cleaned dataframe is displayed below.

| gameid           | teamname           | league   | side   |   result |   gamelength |   firstdragon |   dragons |   elementaldrakes |   infernals |   mountains |   clouds |   oceans |   chemtechs |   hextechs |   elders |
|:-----------------|:-------------------|:---------|:-------|---------:|-------------:|--------------:|----------:|------------------:|------------:|------------:|---------:|---------:|------------:|-----------:|---------:|
| 8401-8401_game_1 | Oh My God          | LPL      | Blue   |        1 |         1365 |             0 |         2 |                 0 |           0 |           0 |        0 |        0 |           0 |          0 |        0 |
| 8401-8401_game_1 | ThunderTalk Gaming | LPL      | Red    |        0 |         1365 |             0 |         1 |                 0 |           0 |           0 |        0 |        0 |           0 |          0 |        0 |
| 8401-8401_game_2 | Oh My God          | LPL      | Blue   |        1 |         1444 |             0 |         2 |                 0 |           0 |           0 |        0 |        0 |           0 |          0 |        0 |
| 8401-8401_game_2 | ThunderTalk Gaming | LPL      | Red    |        0 |         1444 |             0 |         1 |                 0 |           0 |           0 |        0 |        0 |           0 |          0 |        0 |
| 8402-8402_game_1 | FunPlus Phoenix    | LPL      | Blue   |        1 |         1893 |             0 |         4 |                 0 |           0 |           0 |        0 |        0 |           0 |          0 |        0 |


### Univariate Analysis

### Bivariate Analysis

### Interesting Aggregates




## Assessment of Missingness

### NMAR Analysis

### Missingness Dependency



## Hypothesis Testing




## 