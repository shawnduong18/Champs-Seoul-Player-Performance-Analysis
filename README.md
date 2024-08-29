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
_Valorant is a 5v5 character-based tactical FPS developed by Riot Games. Riot manages their own scene where organizations sign players to compete in their franchise. Teams play in the Valorant Champions Tour (VCT) attempting to qualify for international events against other franchise teams from other regions. This Player Performance Analysis examines data from Valorant Champions Seoul 2024, which is the final international tournament of the year._

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
- 3. Is Neon actually meta defining?
- 4. How does map pick influence a team's performance
- 5. Why were EDG so formidable?
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

- Q2.1 To be considered as a top performer quantitatively, players must showcase impressive numbers in individual performance metrics throughout the tournament. Below EDG ZmjjKK, DRX BuZz, and SEN zekken display outstanding First Kills per Round (>= 0.2). FNC Derke and LEV aspastrails behind however they both dies first significantly less than the former, which may indiciate that both are taking either more efficient duels or are not throwing their life on the line to take space for their teams.

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/First%20Kills%20Per%20Round%20vs%20First%20Deaths%20Per%20Round.png)

- Q2.2 Another important statistic to recognize is clutch impact. Running clutch win percentage against Average Round Differential per game builds a picture of how impactful a player's clutches has been for their tournament run. The 3 players that standout the most is TE Biank (35%), DRX BeYn (28%), and TH ReiNs (22%). Their clutches have won a significant portion of rounds that enable their team to close out matches. It seems that the more well rounded a team is, the less dependent on clutches they are. Between these three players there is an inverse relationship between final placement in a tournament against both clutch win percentage and Average Round Differential per game.

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/Clutch%20Percentage%20vs%20Round%20Differential.png)

- Q2.3 Lastly we will touch on peak performances of select players throughout Champions Seoul. Average Combat Score is a measures overall performance through kills, headshot percentage, and economy. This not only allows us to identify which players are performing at a high level consistently, but also uncovers which players brought out their absolute best in a map. FNC Derke (257.4 ACS | 30 Kills), EDG Zmjjkk (250.8 ACS | 28 Kills), DRZ BuZz (241.3 ACS | 24 Kills), TH ReiNs (214.2 ACS | 28 Kills), and SEN zekken (252.2 ACS | 27 Kills) show up once again as top performers. 

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/main/Visuals/Maximum%20Kills%20vs%20Average%20Combat%20Score.png)
