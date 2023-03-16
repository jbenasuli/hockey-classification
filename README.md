# Modeling Expected Goals in the NHL

Building a classification model to value shots in the NHL.

## Overview

Expected goals (xG) models are used to estimate the value of any given shot taken. The value of assigned to a shot is the


## Business and Data Understanding

### Stakeholders & Business Problem

- Many NHL teams are still resistant to using advanced analytics despite the quality and quantity of game data greatly improving in recent years
- Reliance on older, less advanced metrics such as simply counting shot volume puts coaching and front office staffs at a disadvantage
- Our firm, Hockey Data LLC, has been contracted by an NHL team to build them an xG model 
- Our goal in building this model is to provide stakeholders with a tool to better evaluate past results and predict future performance
- Understanding how many goals individuals and teams as a whole can be expected generate can provide insight and drive strategic decision making in numerous ways:
  - Front offices can use it when evaluating players they are considering signing and valuing contracts during negotiations
  - Coaches can use it to help optimize their own lineups and to better understand a given opponents' game and plan adjustments accordingly
  - Players can use it to better understand their own performance and gain insights into how they can tweak their own game to produce better individual and in turn team results

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
- All features included in the model and their individual importances are displayed in chart below 

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
