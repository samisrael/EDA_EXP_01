**Experiment 1: EDA in IPL Dataset**

**Aim:**
To perform Exploratory Data Analysis (EDA) on the IPL matches dataset and derive insights about matches per season, winning teams, toss decisions, and top venues.

**Algorithm / Procedure:**

**1.Import Libraries**
  Import pandas for data handling.
  Import matplotlib and seaborn for visualization.
  
**2.Load Dataset**
  Use pd.read_csv() to load the IPL matches dataset.
  Check dataset shape using .shape.
  View first 5 rows using .head().
  
**3.Matches per Season (Univariate Analysis)**
  Group data by season and count matches.
  Plot a bar chart to visualize growth/decline in matches.
  
**4.Top Winning Teams (Univariate Analysis)**
  Use value_counts() on the winner column.
  Plot top 5 winning teams in a bar chart.
  
**5.Toss Decisions (Univariate Analysis)**
  Count toss decision preferences (bat vs field).
  Plot results using a bar chart.
  
**6.Top Venues (Univariate Analysis)**
  Count matches per venue.
  Display top 5 venues with a horizontal bar chart.
  
**7.Draw Insights**
  Observe patterns in toss decisions.
  Identify teams with consistent winning trends.
  
  
  **Program**
  
```
import matplotlib.pyplot as plt
import seaborn as sns
matches = pd.read_csv("matches.csv")
print("Dataset Shape:",matches.shape)
print("columns:",matches.columns)
print(matches.head())
matches_per_season = matches['season'].value_counts().sort_index()
matches_per_season
plt.figure()
matches_per_season.plot(kind='bar')
plt.xlabel("Season")
plt.ylabel("Number of Matches")
plt.title("Matches Played Per IPL Season")
plt.show()
team_wins = matches['winner'].value_counts()
team_wins
top_5_teams = team_wins.head(5)
top_5_teams
plt.figure()
top_5_teams.plot(kind='bar')
plt.xlabel("Team")
plt.ylabel("Number of Wins")
plt.title("Top 5 Winning Teams in IPL")
plt.xticks(rotation=45)
plt.show()
toss_decision_counts = matches['toss_decision'].value_counts()
toss_decision_counts
plt.figure()
toss_decision_counts.plot(kind='bar')
plt.xlabel("Toss Decision")
plt.ylabel("Number of Times Chosen")
plt.title("Toss Decision Preference in IPL")
plt.show()
venue_counts = matches['venue'].value_counts()
venue_counts
```

  **Output**
  
<img width="485" height="529" alt="image" src="https://github.com/user-attachments/assets/3baf60b6-4855-46fa-8133-e9e812f81f8d" />

<br>
  
<img width="206" height="248" alt="image" src="https://github.com/user-attachments/assets/0bd879a5-1638-414b-a75a-9c10878d1801" />

<br>
  
<img width="492" height="355" alt="image" src="https://github.com/user-attachments/assets/d55bfed4-51e0-4c60-ba6b-2014e54361b2" />


<br>
  
<img width="281" height="335" alt="image" src="https://github.com/user-attachments/assets/d6e8d0a3-b8f7-41a6-9059-5fa6a33007c8" />

<br>

<img width="572" height="501" alt="image" src="https://github.com/user-attachments/assets/74027407-2bd0-4581-97d0-0c2f33009646" />

<br>

<img width="468" height="331" alt="image" src="https://github.com/user-attachments/assets/4818a0c3-dc64-4185-8824-21d7694b1c27" />


<br>

<img width="484" height="762" alt="image" src="https://github.com/user-attachments/assets/b856fa99-18f1-4283-a47a-752b323215c2" />






 **Result**
 <br>
  This experiment is executed successfully


