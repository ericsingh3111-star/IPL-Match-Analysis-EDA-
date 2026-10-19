# IPL-Match-Analysis-EDA-
Exploratory Data Analysis of Indian Premier League (IPL) match-level data using Python, Pandas, Seaborn and Matplotlib.  The project answers common cricket questions with data: which team wins the most, does winning the toss really help, which venues favour chasing, and who collects the most Player of the Match awards.
📌 Project Overview
Item	Details
Dataset	IPL.csv (match-level data)
Size	577 matches × 18 columns
Tools	Python, Pandas, NumPy, Seaborn, Matplotlib, Jupyter Notebook
Type	Exploratory Data Analysis (EDA)
📂 Repository Structure
ipl-match-analysis/
│
├── data/
│   └── IPL.csv              # Dataset
├── notebooks/
│   └── IPL_eda.ipynb        # Main analysis notebook
├── requirements.txt         # Python dependencies
├── .gitignore
└── README.md
📊 Dataset Description
Column	Description
id	Unique match ID
season	IPL season (year)
city	City where the match was played
date	Match date
team1, team2	Teams playing the match
toss_winner	Team that won the toss
toss_decision	Decision taken after the toss (bat / field)
result	Match result type (e.g. normal)
dl_applied	Whether Duckworth-Lewis method was applied (0/1)
winner	Winning team
win_by_runs	Winning margin in runs (if team batting first won)
win_by_wickets	Winning margin in wickets (if chasing team won)
player_of_match	Player of the Match
venue	Stadium name
umpire1, umpire2, umpire3	Match umpires (umpire3 is empty for all rows)

Missing values: city (7), winner (3), player_of_match (3), umpire3 (all 577).

❓ Questions Answered
Which team won the most matches?
What are the toss decision trends (bat vs field)?
How often does the toss winner also win the match?
Do teams win more by runs or by wickets?
Which players won the most Player of the Match awards?
Which venues hosted the most matches?
Which stadium saw the most successful chases?
Which team-vs-team matchup is the most frequent?
🔍 Key Findings
Toss isn't everything: the toss winner won the match only about 50.4% of the time, so winning the toss gives almost no guaranteed edge.
Most matches hosted: M Chinnaswamy Stadium (58), followed by Eden Gardens (54), Feroz Shah Kotla (53), Wankhede Stadium (49) and MA Chidambaram Stadium (48).
Most successful chases: Eden Gardens (32), then M Chinnaswamy Stadium (31) and Feroz Shah Kotla (28).
Most frequent matchup: Chennai Super Kings vs Mumbai Indians (22 matches).
Most wins: Mumbai Indians.
Most Player of the Match awards: Chris Gayle.
Some venues show a clear advantage for the team batting second.
🚀 How to Run
Clone the repository
bash
   git clone https://github.com/<your-username>/ipl-match-analysis.git
   cd ipl-match-analysis
Install dependencies
bash
   pip install -r requirements.txt
Launch Jupyter
bash
   jupyter notebook notebooks/IPL_eda.ipynb

Note: the notebook reads the data with pd.read_csv("IPL.csv", header=1). If you keep the CSV in the data/ folder, change the path to "../data/IPL.csv". The header=1 is there because the CSV has an extra first row above the column names.

🛠️ Tech Stack
Python 3
Pandas, NumPy
Matplotlib, Seaborn
Jupyter Notebook
