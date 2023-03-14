# model features

## Original Feature List

Int64Index: 121458 entries, 0 to 121470
Data columns (total 26 columns):
     Column                     Non-Null Count   Dtype  
---  ------                     --------------   -----  
 0   goal                       121458 non-null  int64  
 1   isHomeTeam                 121458 non-null  float64
 2   timeSinceLastEvent         121458 non-null  int64  
 3   shotAngleAdjusted          121458 non-null  float64
 4   xCordAdjusted              121458 non-null  int64  
 5   yCordAdjusted              121458 non-null  int64  
 6   shotAnglePlusRebound       121458 non-null  float64 - eh
 7   shotAngleReboundRoyalRoad  121458 non-null  int64  - kill
 8   shotType                   121458 non-null  object
 9   shotOnEmptyNet             121458 non-null  int64  
 10  shotAnglePlusReboundSpeed  121458 non-null  float64
 11  shotRebound                121458 non-null  int64  - keep if not keep shotangleplusrebound
 12  shotRush                   121458 non-null  int64  
 13  speedFromLastEvent         121458 non-null  float64
 14  lastEventxCord_adjusted    121458 non-null  int64  
 15  lastEventyCord_adjusted    121458 non-null  int64  
 16  distanceFromLastEvent      121458 non-null  float64
 17  arenaAdjustedShotDistance  121458 non-null  float64
 18  arenaAdjustedYCordAbs      121458 non-null  float64
 19  arenaAdjustedXCordABS      121458 non-null  float64
 20  homeSkatersOnIce           121458 non-null  int64  
 21  awaySkatersOnIce           121458 non-null  int64  
 22  awayPenalty1TimeLeft       121458 non-null  int64  
 23  homePenalty1TimeLeft       121458 non-null  int64  
 24  offWing                    121458 non-null  int64  
 25  game_strength_state        121458 non-null  object

## Features

The target variable is 'goal'. 'goal' data is binary with the outcome for any shot being either 0 for no goal or 1 for a goal scored.

<!-- Binary classification modeling will derive probabili us to model derive probabilities  -->

### Defs

    column name               definition

- timeSinceLastEvent    Time between the shot and the event that took place before the shot
- xCordAdjusted         Adjusts the x coordinate as if all shots were at the right end of the rink. Usually makes the coordinate a positive number
- yCordAdjusted         Adjusts the y coordinate as if all shots were at the right end of the rink.
- shotAngleAdjusted     The absolute value of the shot angle
- shotAnglePlusRebound  The difference in angle between the previous shot and this shot if this shot is a rebound. Is otherwise set to 0
- d
- d
- d
- d
- 

### Maybes

- x
- d