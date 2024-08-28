# Player-Performance-Analysis

## **Table of Contents**
1. [Project Overview]
2. [Data Source]
3. [Questions]
4. [Approach]
5. [Tools & Technologies]
6. [Results]
7. [Conclusion]

---

### **Project Overview**
_This analysis aims to examine player trends and team tendencies during Valorant Champions Seoul and uncover insights into the current state of the game. Through this analysis I discovered insightful information on the current state of the Valorant meta and identified key factors contributing to player performance and team success._

---

### **Data Source**
- **Source of data:** [vlr.gg](https://www.vlr.gg/stats/?event_group_id=all&event_id=2097&series_id=all&region=all&min_rounds=50&min_rating=1550&agent=all&map_id=all&timespan=all)
- **Scope of data:** Covers 34 matches, 80 players and ~2,300 data points.
- **Dataset:** This dataset was created by me and can be found [here](https://docs.google.com/spreadsheets/d/1yH3ZFo-Tlz2oqdMXROr_Z5Ip1KLwdGebf77dtt9TGak/edit?usp=sharing).
---

### **Questions**
_This project explores several key questions, including:_
- 1. How valuable is a player to their team?
- 2. What statistics indicate a top performing player? 
- 3. Is Neon actually meta defining?
- 4. How does map pick influence a team's performance
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
- Q1.1 To quantify how valuable a player is to their team, I focused on two metrics: How critical their performance is to their team's success and (BLANK). Seen below is a graph containing game-to-game impact: "Average Round Differential per game" is defined as the amount of additional rounds a team wins when a player is performing above average compared to when they're performing poorly. To quantify this we performed the following calculations:
- An "average performance" is quantifed as 14.2 kills, rounded up to 15 kills per map. This is derived from the average kills per map across all competitors in Champions Seoul. Any map a player has above 15 kills is considered above average, while any map a player has below 15 kills is considered below average.
- To calculate "Average Round Differential per game", we subtract the average rounds earned from underperformances from the average rounds earned from overperforming.
- E.G. DRX BuZz: 12.5 - 9.3 = 3.2 -> "DRX wins an average of 3.2 rounds per game when BuZz performs well compared to when he performs poorly."
- Lastly, this graph displays only players from the top 6 placing teams, I have excluded 2 players: FNC Boaster and EDG S1Mon for having a less than 0.0 Average Round Differential per game.

![alt text](https://github.com/shawnduong18/Player-Performance-Analysis/blob/82c88c2d8de1a79c8b9e7b7c327364be36ca48fc/Visuals/Round%20Differential.png)



