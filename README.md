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

The following outlines my data cleaning process:

1. I kept only the columns needed for my analysis. Those specific columns and their descriptions are listed above.
2. I filtered out any columns that didn't have complete data. I noticed that most of the columns with partial data didn't contain information about what kind of elemental dragons were taken throughout the game. Since this information is critical in my analysis of netural objectives, I decided to drop all rows that were incomplete.
3. I grouped the data by `gameid` and `teamname` so that each row in the dataframe contains information about a single game. Since I wanted to analyse team objectives and not player statistics, this was the best way to store the data. 
4. I created a new column called `soultype` which specifies the type of elemental dragon soul buff a team got. In League of Legends, a team can get a buff called the dragon soul when they take 4 elemental dragons. There are 6 types of elemental dragons, and therefore 6 types of elemental dragon souls. Each of these 6 souls provide different types of buffs. If a team was unable to get the buff, the value in the column is 'none'.

The head of the cleaned dataframe is displayed below.


| gameid                | teamname                      | league   | side   |   result |   gamelength |   firstdragon |   dragons |   elementaldrakes |   infernals |   mountains |   clouds |   oceans |   chemtechs |   hextechs |   elders | soultype   |
|:----------------------|:------------------------------|:---------|:-------|---------:|-------------:|--------------:|----------:|------------------:|------------:|------------:|---------:|---------:|------------:|-----------:|---------:|:-----------|
| ESPORTSTMNT01_2690210 | Fredit BRION Challengers      | LCKC     | Blue   |        0 |         1713 |             0 |         1 |                 1 |           0 |           0 |        0 |        0 |           0 |          1 |        0 | none       |
| ESPORTSTMNT01_2690210 | Nongshim RedForce Challengers | LCKC     | Red    |        1 |         1713 |             1 |         3 |                 3 |           2 |           1 |        0 |        0 |           0 |          0 |        0 | none       |
| ESPORTSTMNT01_2690219 | Liiv SANDBOX Challengers      | LCKC     | Red    |        1 |         2114 |             1 |         4 |                 4 |           0 |           2 |        1 |        0 |           0 |          1 |        0 | mountains  |
| ESPORTSTMNT01_2690219 | T1 Challengers                | LCKC     | Blue   |        0 |         2114 |             0 |         1 |                 1 |           0 |           1 |        0 |        0 |           0 |          0 |        0 | none       |
| ESPORTSTMNT01_2690227 | Gen.G Challengers             | LCKC     | Red    |        0 |         1972 |             0 |         1 |                 1 |           0 |           0 |        0 |        0 |           0 |          1 |        0 | none       |

### Univariate Analysis

Now, I want to explore the distributions of single variables.

First, I'm going to look at the distribution of the total number of dragons (both elemental and elder) that a team takes per game.

<iframe
  src="figs/total-dragons-dist.html"
  width="800"
  height="600"
  frameborder="0"
></iframe>

### Bivariate Analysis

### Interesting Aggregates




## Assessment of Missingness

### NMAR Analysis

### Missingness Dependency



## Hypothesis Testing