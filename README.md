# NBA Data Pipeline

NBA box score data refreshed daily via Airflow on Google Cloud 

*Note: The pipeline is still active while the NBA Season is suspended but the data will not update until an additional game is played.*<br>
___
***Dataset Details***
* Dataset starts on 1/1/2010
  * Includes Playoff Games but not Pre-Season Games

| TEAM_NAME        | OUTCOME           | MINUTES_PLAYED  | MADE_FIELD_GOALS        | ATTEMPTED_FIELD_GOALS           | MADE_THREE_POINT_FIELD_GOALS  |ATTEMPTED_THREE_POINT_FIELD_GOALS        | MADE_FREE_THROWS           | ATTEMPTED_FREE_THROWS  | OFFENSIVE_REBOUNDS        | 
|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| Team Name     | Win / Loss      |   Team Minutes | Team FGM      | Team FGA      |   Team 3PM | Team 3PA      | Team FTM      |   Team FTA | Team ORB      | 

| DEFENSIVE_REBOUNDS        | ASSISTS           | STEALS  | BLOCKS        | TURNOVERS           | PERSONAL_FOULS  |POINTS        | GAME_ID           | DATE  | 
|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| Team DRB      | Team AST      |   Team STL | Team BLK      | Team TOV      |   Team Fouls | Team PTS     | Unique Game ID      |   Date of Game |

* Composite Key: Team Name + Game ID
* Data Updates for the Prior Day @ 7:30 AM [Eastern Standard Time]
___
### System Architecture 

<img src="Images/System Architecture.png" alt="drawing" height = "450" width="650"/>
<br>



![alt text](https://github.com/dzipkowi/NBA-Data-Pipeline/blob/master/Images/Airflow_v2.png "Airflow")


___
Google's Cloud Composer is not free | Please contribute if you can :) 
<br>
[![Donatecoins](http://donatecoins.org/btc/14RvVFQcBzU33S41Hqpw1ZkA733AVuYAmB.svg)](http://donatecoins.org/btc/14RvVFQcBzU33S41Hqpw1ZkA733AVuYAmB)

