# Nfl Db:
	
There are around 1,696 players in the NFL; each and everyone of those players are assigned to a team. There are 32 teams, and each team is assigned to a division and a conference. Each team also has an owner.

The purpose of this database is to store the statistics of teams and players in the NFL. Having these statistics in a database will allow for careful examination of different aspects of players and teams. Querying and data manipulation of these statistics and data will allow insight and conclusions about various statistical aspects of the NFL. 

## Conditions: 

Top 20 offensive players, based on overall yardage, in the following positions were selected: 
 - QB, RB, WR, and TE.

* Top 10 defensive players based off number of sacks were selected.
* Top 10 defensive players based off number of interceptions were selected.
* Statistics are up to date as of the final week 13 Monday night game.

# ERD

![NFL Database ER Diagram](https://github.com/pto3/DB/blob/master/erd.png)	

# Database Requirements Specifications:

### Team -
	
The team table will include a team name and city. Each team has a city it's assigned to, and also has a name associated with it. Each team also has stats that are associated with it, such as: their average rushing, average passing yards, and so on and so forth. A team is constructed of 53 players, which produce the stats that each team produces on a weekly basis. The team entity has a 1:N relationship.

### Team Stats -
	
Team stats table will consist of stats that each team produces, such as: wins/losses, passing yards, and rushing yards.  Team stats table will have a one to many relationship with the teams table. This is due to the fact that one entity of stats is related to many teams. This makes it a one to many relationship. 

### Division -
	
Division table will be a representation of all the divisions in the NFL along with each team in each division. The NFL has 8 divisions within two conferences:AFC North, AFC South, AFC East, AFC West, NFC North, NFC South, NFC East, NFC West. The division table and the team table has a one to many relationship. This is due to the fact that there are 4 teams in each division and each team is associated to one division. 

### Player -
	
There are about 1,696 players in the NFL, each team has 53 players on it. Each player also has stats associated with them. Each player table has a one to many relationship with team and a one to one relationship with player stats table. There are many players associated to one team and there is one player associated to one entity of stats. 

### Player Stats -
	
Player stats are a vital part of the NFL, it is usually an indication of whether a player is performing well or not. The player stats table has a one to one relationship to the players table. This is due to the fact that each each player has a relationship to one entity of stats. Whether it be a defensive player or an offensive one. They have one entity of stats associated with them .

### Game - 
	
There are generally 16 nfl games per week, excluding bye weeks. Every one of these games has 2 teams and scoring summaries. This game table will store each game, the current week the game is being played in, the two teams playing in this game and the scores of those two teams. This table has a many to many relationship with the teams table.


### Owner -
	
The owner table will give a unique id to each owner in the league as well as store the first and last name of each owner. The owner table is associated with the team entity and has a one to many relationship with this table.



