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
TBD

<img width="618" alt="Screenshot 2024-03-27 at 5 02 42 PM" src="https://github.com/Josh-Horwitz-1219/MIST-4610-Project-1-/assets/163042495/6281cb5c-8e6e-4c9d-96a7-bd8803d4ee68">


## Data Dictionary:

TBD

## Queries:

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

### Query 7

### Query 8

### Query 9

### Query 10

## Database information:

Name of the database: ns_Sp24_21484_Group5

Additional information: Each query listed above is marked in the database using stored procedures which can be called using the following format: CALL TP_Q#();
