# Team 5 Mist 4610 Group Project 1

## Team Name: 
21484 Group 5 

## Team Members:

1. Grace Conn [@graceconn](https://www.github.com/graceconn)
2. Rhea Sabat [@rheasabat](https://www.github.com/rheasabat)
3. Bryce James [@brycejam](https://www.github.com/brycejam)
4. Adam Lebrun [@adam4l](https://www.github.com/adam4l)
5. Josh Horwitz [@Josh-Horwitz-1219](https://www.github.com/Josh-Horwitz-1219)

## Problem Description:

Our data model mirrors that of a high school soccer club. The central entity of our model is the club’s teams. These teams will have varying amounts of players, which is their main distinction from one another. In addition to teams, the club relies heavily on other entities such as its staff, coaches, players, matches, tournaments, sponsors, training facilities, and training sessions. We have been charged with modeling these relationships while also storing the data associated with these entities and relationships in a clear, readable, and accurate manner. Furthermore, we would like to use these relationships between the entities to gain insight and statistics about the club and its performance in different areas mentioned before such as matches and sponsors. 

## Data Model

Explanation of data model: 

  Our database is that of a hypothetical high school soccer club located in Athens, Georgia. The clubs entity is representative of the club to which the rest of the entities operate on behalf of. The club is called Velocity Vortex Athletics. 

	The staff entity is representative of the various staff members employed by the individual teams associated with Velocity Vortex Athletics. While the teams do operate under the Velocity Vortex Athletic Club umbrella, staff members are assigned to specific teams within the club. Accordingly, there is a one to many relationship between staff and teams, as one team can have many staff members assigned to it, while an employee can only work on behalf of one team within the club. 

	Next, we have the coaches table. This table keeps track of the various coaches associated with Velocity Vortex Athletics. Similar to the staff table, while the coaches do coach under the Velocity Vortex Athletics, they coach for particular teams within the club. Consequently, there is a one to many relationship between teams and coaches, as all teams have multiple coaches while coaches can only coach for one team.

	The central entity of our data model is the teams entity. Velocity Vortex Athletics has 15 teams that play on its behalf. For this reason, there is a one to many relationship between the teams and clubs table, as a club (Velocity Vortex Athletics in this case) can have many teams that play on its behalf while a team can play under the umbrella of only one club. 

	Teams are made up of players, which leads us to our next entity: the Players table. Since each team has many players and a player can only play for one team, there is a one to many relationship between players and teams. 

	Also important to keep track of are the various training sessions conducted by the various teams. Accordingly, we have a Training Session table, which keeps track of the start and end times, along with the date and location of various training sessions. Since one team can conduct many training sessions, while a particular training session can only be conducted by one team, there is a one to many relationship between training sessions and teams. Also important to keep track of with training sessions are the players who attend them. Since a training session can be attended by many players and one player can attend many training sessions, there is a many to many relationship between players and training sessions. It is for this reason that we added an associative entity between players and training sessions, which keeps track of the individual players that attend certain training sessions. In other words, if a player’s PlayerId is in the TrainingSessionsAttendance entity, they have attended at least one training session. Also attached to the TrainingSessions table is the TrainingFacilities table. Since one training facility can host many different training sessions, there is a one to many relationship between training facilities and training sessions. 


<img width="618" alt="Screenshot 2024-03-27 at 5 02 42 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/6281cb5c-8e6e-4c9d-96a7-bd8803d4ee68">


## Data Dictionary:

TBD

## Queries:

<img width="817" alt="Screenshot 2024-03-27 at 5 33 42 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/0f537459-1632-4694-9aa9-869c35de7fc6">

### Query 1  
This query lists the player's full name, name of the team they are on, and their team’s number of players for teams that have 5 or more wins.

<img width="613" alt="Screenshot 2024-03-27 at 4 57 14 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/2bb9df91-a4c4-4431-9f4f-520faf2fd590">

Including the number of players on each team in the query enables analysis of team composition and roster management practices. Teams with varying numbers of players may have different dynamics, strengths, and strategies. By examining the team size alongside their performance, coaches and team managers can assess the impact of roster decisions, player rotations, and recruitment strategies on team success.

### Query 2
This query lists the names of the sponsors and tournament locations for the sponsors who have 2 or more losses at that tournament location. 

<img width="621" alt="Screenshot 2024-03-27 at 5 09 28 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/0f43d584-d8fc-44ad-ad80-c9c7221ba1d9">
<img width="616" alt="Screenshot 2024-03-27 at 5 09 47 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/341ce883-4ea4-48a4-b32d-263735f2d729">

Sponsors invest in tournaments to gain visibility and association with successful events. By listing sponsors alongside tournament names with 2 or more losses, tournament organizers can assess the performance of sponsored events. Sponsors might be interested in knowing how their brand is associated with tournaments, including both successes and challenges. For sponsors, understanding the performance of tournaments they are associated with can help them make informed decisions about future sponsorship opportunities.

### Query 3
This query lists the match location if the number of wins is greater than or equal to 2. 

<img width="386" alt="Screenshot 2024-03-27 at 5 12 38 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/89404147-abc5-4d6a-b880-2c1efe91e74a">

By listing the number of wins for each match location, teams and coaches can assess their performance in different environments. Understanding win records at specific locations helps identify strengths and weaknesses, enabling teams to adjust strategies, training regimens, or player selections accordingly.

### Query 4
This query lists the names of the players' names, phone numbers, and team names for those who went to either the Keebler or Hudson facility and also won a match in Athens, Georgia.

<img width="621" alt="Screenshot 2024-03-27 at 5 14 18 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/44fc0779-af32-456e-86da-4c7e170eb376">

Connecting players who have won matches at specific locations fosters community building and networking opportunities within the sports organization. By facilitating interactions between successful players, organizers can encourage knowledge sharing, skill development, and camaraderie among participants. This networking aspect enhances the overall sense of belonging and engagement within the sports community, strengthening bonds between players, coaches, and organizers.

### Query 5
This query lists the staff name and team name they work with for teams that have less than the average amount of players and staff that have a bachelor's degree. 

<img width="625" alt="Screenshot 2024-03-27 at 5 17 01 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/fc7ca595-5ad9-4167-96ff-263e4f9fde29">

By identifying teams with less than the average number of players and staff with bachelor's degrees, the query assists in optimizing resource allocation within the sports organization. Teams with smaller player and staff rosters may require different levels of support and attention compared to larger teams. Identifying these teams allows managers to allocate resources, such as coaching staff or administrative support, more effectively to meet the specific needs of each team.

### Query 6
This query lists names of players names, and the names of the coaches, for those players that are older than the average age. 

<img width="583" alt="Screenshot 2024-03-27 at 5 19 46 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/6dff4d4e-51e7-49bb-ab0a-893c274e18f0">

Identifying players who are 16 years of age and older is essential for player development and management. At this age, players may be eligible for more advanced training programs, competitive leagues, or specialized coaching sessions tailored to their skill level and potential. By listing the names of these players alongside their coaches, team management can ensure that appropriate support and guidance are provided to help players reach their full potential. 

### Query 7
This query lists the players' name and their coaches and the amount of games they’ve played overall. 

<img width="769" alt="Screenshot 2024-03-27 at 5 21 13 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/409b54c4-c636-470a-a283-5abf82e7e1b4">
<img width="625" alt="Screenshot 2024-03-27 at 5 21 27 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/9515a32b-e115-4c62-a916-65d3f8c22d78">

Tracking the total number of games played by each player provides valuable insights into their level of experience, participation, and contribution to the team. This data allows coaches and team managers to assess player performance, consistency, and reliability over time. By listing players' names alongside their coaches and the total number of games played, team management gains a comprehensive understanding of player engagement and involvement in team activities.

### Query 8
This query lists the session ID, facility ID, facility name, and player name(players that are 16 and older) for all the trainings sessions that took place in January and February, where's players age is greater than the average age of players 

<img width="581" alt="Screenshot 2024-03-27 at 5 22 31 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/4700e289-c245-448a-b39e-aed30a00cf43">

This query aims to retrieve specific information from a database regarding training sessions that occurred in January and February. This data helps managers identify how many training sessions occurred in those two months. This lets managers know if there's a need for more training facilities or which training facilities are used more. Additionally knowing which players are older than the average age we can determine who does and doesn't rely on others to practice. 

### Query 9
This query lists the sponsor name and sponsor representative for the tournaments that took place at Eagle Crest Arena and Liberty Fields Arena.

<img width="622" alt="Screenshot 2024-03-27 at 5 23 49 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/d74bdd44-42cf-47bd-baf4-0dbf21a95a83">
<img width="623" alt="Screenshot 2024-03-27 at 5 24 01 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/c29fc353-74f1-46ae-a82f-69b0e6553ac6">

Associating sponsors with tournaments held at Eagle Crest Arena and Liberty Fields Arena facilitates relationship strengthening and engagement efforts. By identifying sponsors and their representatives in relation to these venues, tournament organizers can initiate and maintain communication channels more effectively. This allows for ongoing collaboration, feedback exchange, and partnership development, fostering long-term relationships that benefit both parties.

### Query 10
This query lists the age range, club name, team name, and number of players on each team. Order this by the teams having the most to least players. 

<img width="407" alt="Screenshot 2024-03-27 at 5 25 26 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/18e69ac0-18db-482a-809b-29fcf018ce3a">

Clubs need to allocate resources such as coaches, facilities, and equipment based on the size and composition of each team. Understanding the number of players in each team helps clubs make informed decisions on how to allocate to support their players’ development.

## Database information:

Name of the database: ns_Sp24_21484_Group5

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q#();
