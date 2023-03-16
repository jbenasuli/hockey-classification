# Modeling Expected Goals in the NHL

Building a classification model to value shots in the NHL.

## Overview


## Business and Data Understanding

### Stakeholders & Business Problem

Many NHL teams are still resistant to using advanced analytics despite the quality and quantity of game data greatly improving in recent years
Reliance on older, less advanced metrics such as simply counting shot volume puts coaching and front office staffs at a disadvantage
Our firm, Hockey Data LLC, has been contracted by an NHL team to build them an xG model 
Our xG model provides insights into individual and team performance allowing stakeholders to better understand the game and make better decisions

### Data and Methodology

- Data is comprised of individual shot data from the 2021-2022 NHL season
- All unblocked, "Fenwick", shots are included in our analysis
  - Blocked shots are not included, as the NHL records the location of the player blocking a shot instead of where the shot was taken for blocks
- Shot data was sourced from moneypuck.com
  - Moneypuck shot data tracks 124 features for each individual shot instance
  - Data is compiled by scraping from the ESPN and NHL websites
  - Includes additional metrics derived from scraped league data
- Our target variable is Goal
  - This problem is treated as binary classification as we want to know the probability of any given shot to go in (1) or not (0)
- Features include shot type, shot location, game strength state (i.e. is the shooting team on a powerplay)

  
Explain your stakeholder audience and dataset choice here

## Modeling

### Evaluation

## Conclusion

### Future Recommendations

## Repo Structure

├── imgs
├── .gitignore
├── NHL-Expected-Goals-Notebook.pdf
├── NHL-Expected-Goals-Presentation.pdf
├── NHL-Expected-Goals.ipynb
└── README.md
