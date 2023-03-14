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
- goal                  Set to 1 if shot was a goal. Otherwise 0

### Defs

    column name               definition

- timeSinceLastEvent
  - Time between the shot and the event that took place before the shot
  - Check for colinearity with speedFromLastEvent
- shotAngleAdjusted
  - The absolute value of the shot angle
- shotAnglePlusRebound  
  - The difference in angle between the previous shot and this shot if this shot is a rebound. Is otherwise set to 0
  - Check for colinearity with shotAnglePlusReboundSpeed
- shotType
  - Type of the shot. (Slap, Wrist, etc)
- shotOnEmptyNet
  - Set to 1 if the shot was on an empty net. Otherwise 0.
- shotAnglePlusReboundSpeed The shotAnglePlusRebound variable divded by time between the last shot and this one. (How fast the angle changed)
- speedFromLastEvent
  - The distance between the shot location and the previous event's location divded by the number of seconds between them
- distanceFromLastEvent
  - The distance between the shot location and the previous event's location in feet
  - Check for colinearity with speedFromLastEvent
- homeSkatersOnIce
  - The number of skaters on the ice for the home team. Does not count the goalie
  - use to derive strength state var
- awaySkatersOnIce
  - The number of skaters on the ice for the away team. Does not count the goalie
  - use to derive strength state var
- lastEventxCord_adjusted
  - Adjusts the last event's x coordinate similar to the other adjusted coordinate variables
- lastEventyCord_adjusted
  - Adjusts the last event's y coordinate similar to the other adjusted coordinate variables
- offWing
  - Set to 1 if the shot is from the left side of the ice and the shooter is a right shot, or vice-versa. Otherwise 0
- arenaAdjustedShotDistance	
  - The shot distance adjusted for arena recording bias. Uses the same methodology as War On Ice proposed by Schuckers and Curro. blog.war-on-ice.com/

### Maybes

- shotRush
  - Set to 1 if the shot was on a rush. (If the last event was in another zone and within 4 seconds)
- isHomeTeam
  - Set to 1 if the shooting team is the home team
- lastEventCategory
  - The type of event before the shot.Shot, hit, etc.
- lastEventTeam	The team that did the last event. HOME or AWAY.
  - If last event was a faceoff is the team that won the faceoff