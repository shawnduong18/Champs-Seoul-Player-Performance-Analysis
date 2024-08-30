# Player-Performance-Analysis

## **Table of Contents**
1. [Project Overview]
2. [Preface]
3. [Data Source]
4. [Questions]
5. [Approach]
6. [Tools & Technologies]
7. [Results]
8. [Conclusion]

---

### **Project Overview**
_This analysis aims to examine player trends and team tendencies during Valorant Champions Seoul and uncover insights into the current state of the game. Through this analysis I discovered insightful information on the current state of the Valorant meta and identified key factors contributing to player performance and team success._

---

### **Preface**
_Valorant is a 5v5 character-based tactical FPS developed by Riot Games. Riot manages their own scene where organizations sign players to compete in their franchise. Teams play in the Valorant Champions Tour (VCT) attempting to qualify for international events against other franchise teams from other regions. This Player Performance Analysis examines data from Valorant Champions Seoul 2024, which is the final international tournament of the year. EDward Gaming came out as the victors this tournament._

---

### **Data Source**
- **Source of data:** [vlr.gg](https://www.vlr.gg/stats/?event_group_id=all&event_id=2097&series_id=all&region=all&min_rounds=50&min_rating=1550&agent=all&map_id=all&timespan=all)
- **Scope of data:** Covers 34 matches, 80 players and ~2,300 data points.
- **Dataset:** This dataset was created by me and can be found [here](https://docs.google.com/spreadsheets/d/1yH3ZFo-Tlz2oqdMXROr_Z5Ip1KLwdGebf77dtt9TGak/edit?usp=sharing).
---



### **Questions**
_This project explores several key questions, including:_
- 1. How valuable is a player to their team? 
- 2. Who are the top performers of this tournament?
- 3. Why were EDG so formidable?
---

### **Approach**
- Data inputted into Excel sheet from vlr.gg
- Create visualizations using Tableau

---


### **Tools & Technologies**
_This project was conducted using the following tools:_
- **Data Gathering**: Excel
- **Visualization Tools:** Tableau
___

- ### **Results**
- Q1.1 To quantify how valuable a player is to their team, I focused on two metrics: How critical their performance is to their team's success and how involved they are with their team's success. Seen below is a graph containing game-to-game impact: "Average Round Differential per game" is defined as the amount of additional rounds a team wins when a player is performing above average compared to when they're performing poorly. To quantify this we performed the following calculations:
- An "average performance" is quantifed as 14.2 kills, rounded up to 15 kills per map. This is derived from the average kills per map across all competitors in Champions Seoul. Any map a player has above 15 kills is considered above average, while any map a player has below 15 kills is considered below average.
- To calculate "Average Round Differential per game", we subtract the average rounds earned from underperformances from the average rounds earned from overperforming.
- E.G. DRX BuZz: 12.5 - 9.3 = 3.2 -> "DRX wins an average of an additional 3.2 rounds per game when BuZz performs well compared to when he performs poorly."
- Lastly, this graph displays only players from the top 6 placing teams, I have excluded 2 players: FNC Boaster and EDG S1Mon for having a less than 0.0 Average Round Differential per game.

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/Round%20Diff.png)

- Q1.2 To determine how involved a player is with their team's success, we use a metric called KAST % (Kill, Assist, Survive, Trade Percentage). This is calculated by the number of rounds a player fulfil's one of these actions divided by the total rounds they play. KAST is binary in which the player either had impact or had zero impact in a given round. The graph below displays the KAST % of every player that qualified for playoffs. 

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/KAST%25.png)
___
- Q2.1 To be considered as a top performer quantitatively, players must showcase impressive numbers in individual performance metrics throughout the tournament. Below EDG ZmjjKK, DRX BuZz, and SEN zekken display outstanding First Kills per Round (>= 0.2). FNC Derke and LEV aspas trails behind however they both dies first significantly less than the former, which may indiciate that both are taking either more efficient duels or are not throwing their life on the line to take space for their teams.

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/First%20Kills%20Per%20Round%20vs%20First%20Deaths%20Per%20Round.png)

- Q2.2 Another important statistic to recognize is clutch impact. Running clutch win percentage against Average Round Differential per game builds a picture of how impactful a player's clutches has been for their tournament run. The 3 players that standout the most is TE Biank (35%), DRX BeYn (28%), and TH ReiNs (22%). Their clutches have won a significant portion of rounds that enable their team to close out matches. It seems that the more well rounded a team is, the less dependent on clutches they are. Between these three players there is an inverse relationship between final placement in a tournament against both clutch win percentage and Average Round Differential per game.

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/Clutch%25%20vs%20Round%20Differential.png)

- Q2.3 Lastly we will touch on peak performances of select players throughout Champions Seoul. Average Combat Score is a measures overall performance through kills, headshot percentage, and economy. This not only allows us to identify which players are performing at a high level consistently, but also uncovers which players brought out their absolute best in a map. FNC Derke (257.4 ACS | 30 Kills), EDG ZmjjKK (250.8 ACS | 28 Kills), SEN TenZ (213.4 ACS | 29 Kills), TH ReiNs (214.2 ACS | 28 Kills), and LEV aspas (220.5 ACS | 29 Kills) show up as players with the highest individual peaks within a map.

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/acs%20vs%20kills%20max.png)
___
- Q3.1 EDG winning Valorant Champions Seoul 2024 was unexpected due to the perception of China being a weaker region, so now we'll be examining metrics that enabled EDG to find success.
- S1Mon is EDG's rookie who after 2 months of joining has won the biggest Valorant tournament of the year. As established before Initators like Mazino, c0m, and ReiNs are responsible for providing support to their teammates through utility usage. S1Mon has shown monsterous stats representing his ability to assist his teammmates. The graphic below shows that he is far and away the best performing initator at this tournament with the highest total assists and assists per round. S1mon is also in the top 5 players for KAST % at 76%, meaning he is high impact in many of EDG's rounds. Lastly S1Mon is the only player in this tournament to have a negative Average Round Differential, recall that this number only considers kills as its parameter. This means that S1Mon's ability to help his team win games is almost independent with how well he can shoot enemies. Although getting a high amount of kills is great, him scoring a high amount of kills may mean that he wasn't able to support his teammates properly or that he was the only player that can find any kills that map. Players can have off days and inconsistencies in their gunplay, however S1Mon can maximize his contributions to EDG's matches without ever feeling the need to frag out. He truly embodies what it means to be an initiator. 

  ![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/Assists.png)

- 3.2 ZmjjKK has cemented himself as one of the best entry players this tournament with the highest First Kills Per Round and highest First Kills Total, however ZmjjKK is not the only player capable of entrying. CHICHOO is also excellent at finding first bloods, but what makes his case different from ZmjjKK is that he dies a lot less than his teammate. In fact CHICHOO dies a lot less than any other player attempting to draw first blood, he holds the best First Kill Success Percentage (65.8%) for players with over 25 first kills which is over 10% the average First Kill Success Percentage. Why this is important to EDG's success is it allows EDG to use him in three different ways. Firstly, CHICHOO can adopt the traditional lurking style and find first bloods by taking control of the map, second EDG could attack on two fronts by having CHICHOO entry the bombsite while ZmjjKK causes chaos on the other side of the map. Lastly if EDG want to immediately hit a bombsite CHICHOO can join his four teammates in a push and draw first blood. S1Mon also has almost an identical First Blood Success Percentage (64.4%), but has almost 20 less attempts than CHICHOO. CHICHOO's consistency is signficant since it adds depth to EDG's playbook that not many other teams can replicate easily. A good example of a team that cannot accomplish this is LEVIATÁN as every player that other than aspas has a below average first blood rate., which makes them seem one-dimensional tactically. 

  
___

### **Conclusion**
- 1.  How valuable is a player to their team? 
- Player value was measured by two metrics, firstly we'll discuss the Average Round Differential Per Game statistic. Looking at the graph, we can see that all the players from LEVIATÁN far exceed the average Round Differential Per Game. This detail says that all players of LEV are capable of taking over a game when they perform well. aspas, c0m, and Mazino top this statistic, individually earning their team 5-7 rounds per map when they earn above 15 kills. This makes sense as LEV's system and tacitcs are built to support aspas, and rely on his individual performance to win rounds for them. Furthermore c0m and Mazino are the support initators that give aspas the utility he needs to take fights, their Round Differential Per Game being high indicates that they are adept at taking advantage of the space that aspas creates through trades or multikills. Their impact is felt through multiple matches, resulting in a top three finish at Champions Seoul. We notice that the teams that finished top 2 (EDG and TH) have a more spreadout distribution of Round Differential Per Game. This indiciates that these teams rely less on individual performance compared to LEV, but rather on teamplay to win their games.

- Next KAST was also used to measure how much impact players had in rounds. EDG, the Champions of this tournament have 3 players of the top 5 that have the highest KAST %. Which shows how well the EDG players move together and use each other to close out rounds, this contributes to EDG overall success in their tournament run. Another important thing to point out is how each of the top 4 placing teams (EDG, TH, LEV, SEN) all have multiple players in the top half of KAST % rankning, while FNATIC only has Alfajer who is only barely above the average KAST %. Otherwise FNATIC not even close to the other teams. What this says about FNATIC is that they aren't effective at setting up fights with each other or trading Derke when he entries. This makes Derke's ability to find a high number of first kills and dying less an even more impressive statistic and a crucial reason why FNATIC made it as far as they did in Champions Seoul. 
     
- 2. Who are the top performers of this tournament?
- The top performers of this tournament are players their teams undoubtly would not have gone as far as they had without this player. Firstly LEV aspas, his team wins an average of 5.9 more rounds if he has above 15 kills in a map. Furthermore aspas is able to find a respectable amount of first kills while minizing the amount of times that he gives first blood to the enemy team. Lastly, he also had one of the best individual performances (29 kills) against Team Heretics. Next we'll be discussing FNATIC Derke. As stated before Derke displays impressive stats similar to aspas, however he is doing this with less support from his team. Derke holds the highest kills (30 kills) in one map in the entire tournament. ReiNs is an initator player from Heretics that has brought unparalleled value in this tournament. His Round Differential suggests that when he plays well, Heretics win an average of 4.1 additional rounds. Next he is the player on his team with the highest KAST % on his own team. Lastly, he boasts an impressive clutch percentage that leads to him winning impactful rounds for his team. He is performing well individual while simultaneously providing his team with support. EDG performed off the back of solid fundamentals and a good read of the Valorant meta, however a good portion of their success can be credited to their duelist EDG ZmjjKK. Zmjjkk's brings value not through the sheer number of kills he has or the impact of clutches, as stated before Zmjjkk is player with the highest Kills Per Round out of any player. Getting the first blood in a round is extremely crucial as it dramatically increases the chance EDG win the round. This is accompanied by the high amount of first deaths per round, but EDG are able to recover from this by immediately trading or converting player disadvantages which is established by the high KAST % at three of their players had. 
     

     
- 3.  Why were EDG so formidable?
      
---
